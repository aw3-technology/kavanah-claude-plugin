# Meetings

27 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `m.get` | GET | `/api/m/{token}` | Public meeting lookup |
| `m.ics.list` | GET | `/api/m/{token}/ics` | Download a meeting's calendar invite |
| `m.join.create` | POST | `/api/m/{token}/join` | Join a meeting and get its join details |
| `m.rsvp.create` | POST | `/api/m/{token}/rsvp` | RSVP to, self-register for, or stamp a join on a public meeting link |
| `meetings.create` | POST | `/api/meetings` | Schedule a meeting |
| `meetings.delete` | DELETE | `/api/meetings/{id}` | Cancel a meeting |
| `meetings.get` | GET | `/api/meetings/{id}` | Get a meeting with its attendees |
| `meetings.list` | GET | `/api/meetings` | List scheduled meetings in the workspace |
| `meetings.send-invites.create` | POST | `/api/meetings/{id}/send-invites` | Email calendar invites to the meeting's attendees |
| `meetings.update` | PATCH | `/api/meetings/{id}` | Update a meeting and add or remove attendees |
| `messages.threads.meeting.list` | GET | `/api/messages/threads/{contactId}/meeting` | Get meeting session |
| `messages.threads.meeting.messages.create` | POST | `/api/messages/threads/{contactId}/meeting/messages` | Send a meeting chat message |
| `messages.threads.meeting.participants.create` | POST | `/api/messages/threads/{contactId}/meeting/participants` | Add a meeting participant |
| `messages.threads.meeting.participants.update` | PATCH | `/api/messages/threads/{contactId}/meeting/participants` | Update a meeting participant (mute, kick) |
| `messages.threads.meeting.recording.transcript.update` | PATCH | `/api/messages/threads/{contactId}/meeting/recording/{recordingId}/transcript` | Re-queue creating tasks from a recording's AI notes |
| `messages.threads.meeting.signals.create` | POST | `/api/messages/threads/{contactId}/meeting/signals` | Send a WebRTC signal |
| `messages.threads.meeting.signals.list` | GET | `/api/messages/threads/{contactId}/meeting/signals` | Poll for WebRTC signals |
| `messages.threads.meeting.twin.create` | POST | `/api/messages/threads/{contactId}/meeting/twin` | Admit a digital twin to a live call |
| `messages.threads.meeting.twin.delete` | DELETE | `/api/messages/threads/{contactId}/meeting/twin` | Dismiss the twin from a call |
| `messages.threads.meeting.twin.host-token.create` | POST | `/api/messages/threads/{contactId}/meeting/twin/host-token` | Mint the bearer token an unattended twin runner uses |
| `messages.threads.meeting.twin.list` | GET | `/api/messages/threads/{contactId}/meeting/twin` | Live digital-twin session for a call, and the caller's own twin |
| `messages.threads.meeting.twin.listen.create` | POST | `/api/messages/threads/{contactId}/meeting/twin/listen` | Transcribe a short audio chunk for an attending twin |
| `messages.threads.meeting.twin.room.list` | GET | `/api/messages/threads/{contactId}/meeting/twin/room` | Participants and ICE servers for an unattended twin runner |
| `messages.threads.meeting.twin.signals.create` | POST | `/api/messages/threads/{contactId}/meeting/twin/signals` | Send a WebRTC signal as an unattended twin runner |
| `messages.threads.meeting.twin.signals.list` | GET | `/api/messages/threads/{contactId}/meeting/twin/signals` | Read WebRTC signals as an unattended twin runner |
| `messages.threads.meeting.twin.speak.create` | POST | `/api/messages/threads/{contactId}/meeting/twin/speak` | Synthesize speech in the twin's own voice |
| `messages.threads.meeting.update` | PATCH | `/api/messages/threads/{contactId}/meeting` | Update meeting controls or end/leave meeting |

---

### `m.get`

`GET /api/m/{token}`

Public meeting lookup

Public, no auth. Resolves a meeting by its public token and returns a safe projection; the join URL, location and dial-in are never returned here (only whether they exist). With a matching invite token `i`, also returns the viewer's attendee record.

Path params (positional, in order):
  - `token`

Query:
  - `i` (string) — Per-attendee invite token

### `m.ics.list`

`GET /api/m/{token}/ics`

Download a meeting's calendar invite

Public, no auth. Returns an .ics file. The join target and attendee roster are included only for public meetings (and only invited attendees); a cancelled meeting is sent as a CANCEL.

Path params (positional, in order):
  - `token`

### `m.join.create`

`POST /api/m/{token}/join`

Join a meeting and get its join details

Admission gate by access mode. public admits anyone; invited_only needs a matching invite token or an email on the attendee list; workspace_members needs a signed-in active member of the meeting's workspace. On admission, stamps the attendee's join (when identified) and returns the join URL, location and dial-in.

Path params (positional, in order):
  - `token`

Body (application/json):
  - `inviteToken` (string)
  - `email` (string)

### `m.rsvp.create`

`POST /api/m/{token}/rsvp`

RSVP to, self-register for, or stamp a join on a public meeting link

Public, no session. Resolves the attendee by per-attendee inviteToken (must belong to this meeting), else by email on the invited list; on an access_mode public meeting an unknown email is added as a self_added attendee. Invited-only and workspace-members meetings never auto-add. Optionally sets the RSVP and records a join.

Path params (positional, in order):
  - `token`

Body (application/json):
  - `inviteToken` (string) — Per-attendee invite token (preferred)
  - `email` (string) — Required when inviteToken is absent
  - `name` (string)
  - `rsvp` (string) — one of: `accepted`, `declined`, `tentative`, `pending`
  - `recordJoin` (boolean) — True when the attendee clicked Join now

### `meetings.create`

`POST /api/meetings`

Schedule a meeting

Creates a meeting hosted by the caller, with attendees de-duplicated by email. At least one of meetingUrl, location or dialIn is required. accessMode defaults to invited_only. Does not send invites (see send-invites).

Body (application/json):
  - `title` (string, required)
  - `description` (string)
  - `meetingUrl` (string|null)
  - `location` (string|null)
  - `dialIn` (string|null)
  - `startsAt` (string<date-time>, required)
  - `endsAt` (string<date-time>, required) — Must be after startsAt
  - `timezone` (string)
  - `accessMode` (string) — one of: `public`, `invited_only`, `workspace_members`
  - `attendees` (object[])

### `meetings.delete`

`DELETE /api/meetings/{id}`

Cancel a meeting

Soft delete. Sets status to cancelled and bumps the calendar sequence so calendar clients remove the event.

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `meetings.get`

`GET /api/meetings/{id}`

Get a meeting with its attendees

Path params (positional, in order):
  - `id`

### `meetings.list`

`GET /api/meetings`

List scheduled meetings in the workspace

Any workspace member. Optional time window and limit.

Query:
  - `from` (string<date-time>) — ISO 8601 lower bound
  - `to` (string<date-time>) — ISO 8601 upper bound
  - `limit` (integer)

### `meetings.send-invites.create`

`POST /api/meetings/{id}/send-invites`

Email calendar invites to the meeting's attendees

Emails each non-declined attendee (or the given subset) an invite with a personal join link and an .ics attachment, Reply-To the host. Sends one compliance archive copy first; if that fails nothing is sent. Re-sending after an edit sends fresh mail because the dedupe key includes the calendar sequence.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `onlyAttendeeIds` (string[]) — Restrict the send to these attendees

### `meetings.update`

`PATCH /api/meetings/{id}`

Update a meeting and add or remove attendees

Partial update. Validated against the current row: endsAt must stay after startsAt and at least one of meetingUrl, location or dialIn must remain (null clears a field). addAttendees appends; removeAttendeeIds removes.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `title` (string)
  - `description` (string)
  - `meetingUrl` (string|null)
  - `location` (string|null)
  - `dialIn` (string|null)
  - `startsAt` (string<date-time>)
  - `endsAt` (string<date-time>)
  - `timezone` (string)
  - `accessMode` (string) — one of: `public`, `invited_only`, `workspace_members`
  - `status` (string) — one of: `scheduled`, `cancelled`, `completed`
  - `addAttendees` (object[])
  - `removeAttendeeIds` (string[])

### `messages.threads.meeting.list`

`GET /api/messages/threads/{contactId}/meeting`

Get meeting session

Path params (positional, in order):
  - `contactId`

### `messages.threads.meeting.messages.create`

`POST /api/messages/threads/{contactId}/meeting/messages`

Send a meeting chat message

Path params (positional, in order):
  - `contactId`

Body (application/json):
  - `content` (string, required)

### `messages.threads.meeting.participants.create`

`POST /api/messages/threads/{contactId}/meeting/participants`

Add a meeting participant

Path params (positional, in order):
  - `contactId`

Body (application/json):
  - `participantId` (string, required)

### `messages.threads.meeting.participants.update`

`PATCH /api/messages/threads/{contactId}/meeting/participants`

Update a meeting participant (mute, kick)

Path params (positional, in order):
  - `contactId`

Body (application/json):
  - `participantId` (string, required)
  - `micEnabled` (boolean)
  - `kicked` (boolean)

### `messages.threads.meeting.recording.transcript.update`

`PATCH /api/messages/threads/{contactId}/meeting/recording/{recordingId}/transcript`

Re-queue creating tasks from a recording's AI notes

Meeting participants only. Requires the recording's AI notes to be ready; the notes-to-tasks cron creates the tasks on its next run. Already-created action items are not duplicated.

Path params (positional, in order):
  - `contactId`
  - `recordingId`

### `messages.threads.meeting.signals.create`

`POST /api/messages/threads/{contactId}/meeting/signals`

Send a WebRTC signal

Send one signal (`type` + `payload`) or a batch (`signals`, at most 100) to the same target. Each signal is stored as its own row, so the GET side is identical either way; the browser batches each burst of ICE candidates into one request.

Path params (positional, in order):
  - `contactId`

Body (application/json):
  - `targetUserId` (string, required)
  - `type` (string) — one of: `offer`, `answer`, `ice-candidate`
  - `payload` (object)
  - `signals` (object[])

### `messages.threads.meeting.signals.list`

`GET /api/messages/threads/{contactId}/meeting/signals`

Poll for WebRTC signals

Path params (positional, in order):
  - `contactId`

Query:
  - `after` (string)

### `messages.threads.meeting.twin.create`

`POST /api/messages/threads/{contactId}/meeting/twin`

Admit a digital twin to a live call

Only the person a twin represents may send it, and they must be an active member. Admission rules (feature flag, persona enabled, disclosure policy, audience, participant notice) are enforced server-side. The audience is frozen into the session.

Path params (positional, in order):
  - `contactId`

Body (application/json):
  - `personaId` (string, required)
  - `audience` (string) — one of: `internal`, `external`
  - `participantsNotified` (boolean)

### `messages.threads.meeting.twin.delete`

`DELETE /api/messages/threads/{contactId}/meeting/twin`

Dismiss the twin from a call

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `contactId`

Query:
  - `reason` (string) — one of: `ended`, `owner_took_over`, `refused`, `error`

### `messages.threads.meeting.twin.host-token.create`

`POST /api/messages/threads/{contactId}/meeting/twin/host-token`

Mint the bearer token an unattended twin runner uses

Only for a twin already admitted to the call, and only by the person the twin represents. The token is scoped to one workspace, call, persona and twin session and expires in one hour.

Path params (positional, in order):
  - `contactId`

### `messages.threads.meeting.twin.list`

`GET /api/messages/threads/{contactId}/meeting/twin`

Live digital-twin session for a call, and the caller's own twin

Returns the live twin session (if any), whether meeting twins are enabled for the workspace, and the caller's own twin persona.

Path params (positional, in order):
  - `contactId`

### `messages.threads.meeting.twin.listen.create`

`POST /api/messages/threads/{contactId}/meeting/twin/listen`

Transcribe a short audio chunk for an attending twin

Live speech-to-text for a call a twin has been admitted to. Billed to the caller as voice usage; rate limited. Multipart form with an audio part, at most 2 MB.

Path params (positional, in order):
  - `contactId`

Body (multipart/form-data):
  - `audio` (string<binary>, required)

### `messages.threads.meeting.twin.room.list`

`GET /api/messages/threads/{contactId}/meeting/twin/room`

Participants and ICE servers for an unattended twin runner

Authenticated by twin host token (Authorization Bearer), not a session. Lists the other participants (the twin's owner excluded) and the ICE servers.

Path params (positional, in order):
  - `contactId`

### `messages.threads.meeting.twin.signals.create`

`POST /api/messages/threads/{contactId}/meeting/twin/signals`

Send a WebRTC signal as an unattended twin runner

Authenticated by twin host token (Authorization Bearer). Acts as the twin's owner.

Path params (positional, in order):
  - `contactId`

Body (application/json):
  - `targetUserId` (string, required)
  - `type` (string, required) — one of: `offer`, `answer`, `ice-candidate`
  - `payload` (object)

### `messages.threads.meeting.twin.signals.list`

`GET /api/messages/threads/{contactId}/meeting/twin/signals`

Read WebRTC signals as an unattended twin runner

Authenticated by twin host token (Authorization Bearer). Acts as the twin's owner.

Path params (positional, in order):
  - `contactId`

Query:
  - `after` (string) — Return signals after this cursor

### `messages.threads.meeting.twin.speak.create`

`POST /api/messages/threads/{contactId}/meeting/twin/speak`

Synthesize speech in the twin's own voice

Authenticated by twin host token (Authorization Bearer). Text is capped at 1,200 characters and always spoken in the twin persona's configured voice. In an archiving workspace each utterance is journaled first and refused if it cannot be. Billed to the twin's owner. Returns audio/mpeg.

Path params (positional, in order):
  - `contactId`

Body (application/json):
  - `text` (string, required)

### `messages.threads.meeting.update`

`PATCH /api/messages/threads/{contactId}/meeting`

Update meeting controls or end/leave meeting

Path params (positional, in order):
  - `contactId`

Body (application/json):
  - `micEnabled` (boolean)
  - `cameraEnabled` (boolean)
  - `speakerEnabled` (boolean)
  - `screenSharing` (boolean)
  - `ended` (boolean)
  - `left` (boolean)

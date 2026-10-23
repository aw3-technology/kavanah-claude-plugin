# Messages

89 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `messages.audit.exports.create` | POST | `/api/messages/audit/exports` | Create export |
| `messages.audit.exports.list` | GET | `/api/messages/audit/exports` | List exports |
| `messages.audit.list` | GET | `/api/messages/audit` | List audit |
| `messages.audit.retention.list` | GET | `/api/messages/audit/retention` | List retention |
| `messages.audit.retention.update` | PATCH | `/api/messages/audit/retention` | Update retention |
| `messages.channels.create` | POST | `/api/messages/channels` | Create channel |
| `messages.channels.list` | GET | `/api/messages/channels` | List channels |
| `messages.channels.members.create` | POST | `/api/messages/channels/{channelId}/members` | Join a channel or add a member |
| `messages.channels.members.delete` | DELETE | `/api/messages/channels/{channelId}/members` | Leave a channel or remove a member |
| `messages.channels.members.list` | GET | `/api/messages/channels/{channelId}/members` | List members |
| `messages.channels.update` | PATCH | `/api/messages/channels/{channelId}` | Update channel |
| `messages.client-channels.create` | POST | `/api/messages/client-channels` | Create client channel |
| `messages.client-channels.list` | GET | `/api/messages/client-channels` | List client channels |
| `messages.client-channels.members.create` | POST | `/api/messages/client-channels/{channelId}/members` | Create member |
| `messages.client-channels.members.delete` | DELETE | `/api/messages/client-channels/{channelId}/members` | Delete members |
| `messages.client-channels.members.list` | GET | `/api/messages/client-channels/{channelId}/members` | List members |
| `messages.client-channels.messages.create` | POST | `/api/messages/client-channels/{channelId}/messages` | Create message |
| `messages.client-channels.messages.list` | GET | `/api/messages/client-channels/{channelId}/messages` | List messages |
| `messages.count.list` | GET | `/api/messages/count` | (undocumented route — params unknown, pass them explicitly) |
| `messages.files.get` | GET | `/api/messages/files/{messageId}/{attachmentId}` | Download a message attachment |
| `messages.files.list` | GET | `/api/messages/files` | List files |
| `messages.groups.create` | POST | `/api/messages/groups` | Create a group chat |
| `messages.groups.members.create` | POST | `/api/messages/groups/{groupId}/members` | Add a member to a group chat |
| `messages.groups.members.delete` | DELETE | `/api/messages/groups/{groupId}/members` | Leave a group chat or remove a member |
| `messages.list` | GET | `/api/messages` | Get all messages, contacts, and preferences |
| `messages.mentions.list` | GET | `/api/messages/mentions` | List mentions |
| `messages.notifications.list` | GET | `/api/messages/notifications` | List notifications |
| `messages.notifications.update` | PATCH | `/api/messages/notifications` | Update notifications |
| `messages.presence.create` | POST | `/api/messages/presence` | Create presence |
| `messages.project-links.create` | POST | `/api/messages/project-links` | Create project link |
| `messages.project-links.delete` | DELETE | `/api/messages/project-links` | Delete project links |
| `messages.project-links.list` | GET | `/api/messages/project-links` | List project links |
| `messages.push.subscribe.create` | POST | `/api/messages/push/subscribe` | Create subscribe |
| `messages.push.subscribe.delete` | DELETE | `/api/messages/push/subscribe` | Delete subscribe |
| `messages.push.vapid-key.list` | GET | `/api/messages/push/vapid-key` | List vapid key |
| `messages.requests.count.list` | GET | `/api/messages/requests/count` | (undocumented route — params unknown, pass them explicitly) |
| `messages.requests.create` | POST | `/api/messages/requests` | (undocumented route — params unknown, pass them explicitly) |
| `messages.requests.list` | GET | `/api/messages/requests` | (undocumented route — params unknown, pass them explicitly) |
| `messages.requests.lookup.list` | GET | `/api/messages/requests/lookup` | (undocumented route — params unknown, pass them explicitly) |
| `messages.requests.respond.create` | POST | `/api/messages/requests/{p1}/respond` | (undocumented route — params unknown, pass them explicitly) |
| `messages.rtc-config.list` | GET | `/api/messages/rtc-config` | ICE servers for the chat call transport |
| `messages.scheduled-processor.create` | POST | `/api/messages/scheduled-processor` | Create scheduled processor |
| `messages.scheduled.create` | POST | `/api/messages/scheduled` | Create scheduled |
| `messages.scheduled.delete` | DELETE | `/api/messages/scheduled/{messageId}` | Delete scheduled |
| `messages.scheduled.list` | GET | `/api/messages/scheduled` | List scheduled |
| `messages.scheduled.update` | PATCH | `/api/messages/scheduled/{messageId}` | Update scheduled |
| `messages.search.list` | GET | `/api/messages/search` | List search |
| `messages.stream.list` | GET | `/api/messages/stream` | List stream |
| `messages.templates.create` | POST | `/api/messages/templates` | Create template |
| `messages.templates.create.by-templateId` | POST | `/api/messages/templates/{templateId}` | Action on template |
| `messages.templates.delete` | DELETE | `/api/messages/templates/{templateId}` | Delete template |
| `messages.templates.get` | GET | `/api/messages/templates/{templateId}` | Fetch template |
| `messages.templates.list` | GET | `/api/messages/templates` | List templates |
| `messages.templates.update` | PATCH | `/api/messages/templates/{templateId}` | Update template |
| `messages.threads.delete` | DELETE | `/api/messages/threads/{contactId}` | Delete a conversation thread |
| `messages.threads.deliver.create` | POST | `/api/messages/threads/{p1}/deliver` | (undocumented route — params unknown, pass them explicitly) |
| `messages.threads.meeting.recording.chunk.create` | POST | `/api/messages/threads/{contactId}/meeting/recording/{recordingId}/chunk` | Create chunk |
| `messages.threads.meeting.recording.consent.create` | POST | `/api/messages/threads/{contactId}/meeting/recording/{recordingId}/consent` | Create consent |
| `messages.threads.meeting.recording.create` | POST | `/api/messages/threads/{contactId}/meeting/recording` | Create recording |
| `messages.threads.meeting.recording.delete` | DELETE | `/api/messages/threads/{contactId}/meeting/recording/{recordingId}` | Delete recording |
| `messages.threads.meeting.recording.get` | GET | `/api/messages/threads/{contactId}/meeting/recording/{recordingId}` | Fetch recording |
| `messages.threads.meeting.recording.list` | GET | `/api/messages/threads/{contactId}/meeting/recording` | List recording |
| `messages.threads.meeting.recording.stop.create` | POST | `/api/messages/threads/{contactId}/meeting/recording/{recordingId}/stop` | Create stop |
| `messages.threads.meeting.recording.transcript.create` | POST | `/api/messages/threads/{contactId}/meeting/recording/{recordingId}/transcript` | Create transcript |
| `messages.threads.meeting.recording.transcript.list` | GET | `/api/messages/threads/{contactId}/meeting/recording/{recordingId}/transcript` | List transcript |
| `messages.threads.meeting.recording.transcript.update` | PATCH | `/api/messages/threads/{p1}/meeting/recording/{p2}/transcript` | (undocumented route — params unknown, pass them explicitly) |
| `messages.threads.meeting.twin.create` | POST | `/api/messages/threads/{p1}/meeting/twin` | (undocumented route — params unknown, pass them explicitly) |
| `messages.threads.meeting.twin.delete` | DELETE | `/api/messages/threads/{p1}/meeting/twin` | (undocumented route — params unknown, pass them explicitly) |
| `messages.threads.meeting.twin.host-token.create` | POST | `/api/messages/threads/{p1}/meeting/twin/host-token` | (undocumented route — params unknown, pass them explicitly) |
| `messages.threads.meeting.twin.list` | GET | `/api/messages/threads/{p1}/meeting/twin` | (undocumented route — params unknown, pass them explicitly) |
| `messages.threads.meeting.twin.listen.create` | POST | `/api/messages/threads/{p1}/meeting/twin/listen` | (undocumented route — params unknown, pass them explicitly) |
| `messages.threads.meeting.twin.room.list` | GET | `/api/messages/threads/{p1}/meeting/twin/room` | (undocumented route — params unknown, pass them explicitly) |
| `messages.threads.meeting.twin.signals.create` | POST | `/api/messages/threads/{p1}/meeting/twin/signals` | (undocumented route — params unknown, pass them explicitly) |
| `messages.threads.meeting.twin.signals.list` | GET | `/api/messages/threads/{p1}/meeting/twin/signals` | (undocumented route — params unknown, pass them explicitly) |
| `messages.threads.meeting.twin.speak.create` | POST | `/api/messages/threads/{p1}/meeting/twin/speak` | (undocumented route — params unknown, pass them explicitly) |
| `messages.threads.members.list` | GET | `/api/messages/threads/{contactId}/members` | List the members of a group-type chat (team chat, group, or channel) |
| `messages.threads.messages.create` | POST | `/api/messages/threads/{contactId}/messages` | Send a message |
| `messages.threads.messages.delete` | DELETE | `/api/messages/threads/{contactId}/messages/{messageId}` | Delete a message |
| `messages.threads.messages.forward.create` | POST | `/api/messages/threads/{contactId}/messages/forward` | Create forward |
| `messages.threads.messages.list` | GET | `/api/messages/threads/{p1}/messages` | (undocumented route — params unknown, pass them explicitly) |
| `messages.threads.messages.reactions.create` | POST | `/api/messages/threads/{contactId}/messages/{messageId}/reactions` | Toggle an emoji reaction on a message |
| `messages.threads.messages.read.create` | POST | `/api/messages/threads/{contactId}/messages/{messageId}/read` | Create read |
| `messages.threads.messages.replies.create` | POST | `/api/messages/threads/{contactId}/messages/{messageId}/replies` | Reply in a message thread |
| `messages.threads.messages.replies.list` | GET | `/api/messages/threads/{contactId}/messages/{messageId}/replies` | List replies |
| `messages.threads.messages.update` | PATCH | `/api/messages/threads/{contactId}/messages/{messageId}` | Edit a message |
| `messages.threads.pinned.list` | GET | `/api/messages/threads/{contactId}/pinned` | List pinned |
| `messages.threads.typing.update` | PATCH | `/api/messages/threads/{contactId}/typing` | Set typing state |
| `messages.threads.update` | PATCH | `/api/messages/threads/{contactId}` | Update thread flags (pin, mute, block, etc.) |
| `messages.update` | PATCH | `/api/messages` | Update chat preferences |

---

### `messages.audit.exports.create`

`POST /api/messages/audit/exports`

Create export

Body: application/json (free-form — pass with `--data`)

### `messages.audit.exports.list`

`GET /api/messages/audit/exports`

List exports

### `messages.audit.list`

`GET /api/messages/audit`

List audit

### `messages.audit.retention.list`

`GET /api/messages/audit/retention`

List retention

### `messages.audit.retention.update`

`PATCH /api/messages/audit/retention`

Update retention

Body: application/json (free-form — pass with `--data`)

### `messages.channels.create`

`POST /api/messages/channels`

Create channel

Creates a channel with the caller as its admin. Optional `memberIds` seeds initial members — ids are filtered to active members of the caller's workspace (ineligible ids are dropped, not an error).

Body (application/json):
  - `name` (string, required)
  - `description` (string)
  - `isPrivate` (boolean)
  - `projectRef` (string)
  - `memberIds` (string[])

### `messages.channels.list`

`GET /api/messages/channels`

List channels

### `messages.channels.members.create`

`POST /api/messages/channels/{channelId}/members`

Join a channel or add a member

With no body (or your own userId), joins the channel — public channels only; private channels require an invite. With another user's id (JSON body `userId`), adds that workspace member — the caller must be a channel member or a workspace admin, and this is the only way into a private channel. Adding an existing member is an idempotent no-op.

Path params (positional, in order):
  - `channelId`

Body (application/json):
  - `userId` (string)

### `messages.channels.members.delete`

`DELETE /api/messages/channels/{channelId}/members`

Leave a channel or remove a member

With no body (or your own userId), leaves the channel — always allowed. With another user's id (JSON body `userId` or the `userId` query parameter), removes that member — workspace admins, channel admins, or the channel creator only.

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `channelId`

Query:
  - `userId` (string)

Body (application/json):
  - `userId` (string)

### `messages.channels.members.list`

`GET /api/messages/channels/{channelId}/members`

List members

Path params (positional, in order):
  - `channelId`

### `messages.channels.update`

`PATCH /api/messages/channels/{channelId}`

Update channel

Path params (positional, in order):
  - `channelId`

Body: application/json (free-form — pass with `--data`)

### `messages.client-channels.create`

`POST /api/messages/client-channels`

Create client channel

Body: application/json (free-form — pass with `--data`)

### `messages.client-channels.list`

`GET /api/messages/client-channels`

List client channels

### `messages.client-channels.members.create`

`POST /api/messages/client-channels/{channelId}/members`

Create member

Path params (positional, in order):
  - `channelId`

Body: application/json (free-form — pass with `--data`)

### `messages.client-channels.members.delete`

`DELETE /api/messages/client-channels/{channelId}/members`

Delete members

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `channelId`

### `messages.client-channels.members.list`

`GET /api/messages/client-channels/{channelId}/members`

List members

Path params (positional, in order):
  - `channelId`

### `messages.client-channels.messages.create`

`POST /api/messages/client-channels/{channelId}/messages`

Create message

Path params (positional, in order):
  - `channelId`

Body: application/json (free-form — pass with `--data`)

### `messages.client-channels.messages.list`

`GET /api/messages/client-channels/{channelId}/messages`

List messages

Path params (positional, in order):
  - `channelId`

### `messages.count.list`

`GET /api/messages/count`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `messages.files.get`

`GET /api/messages/files/{messageId}/{attachmentId}`

Download a message attachment

Path params (positional, in order):
  - `messageId`
  - `attachmentId`

### `messages.files.list`

`GET /api/messages/files`

List files

### `messages.groups.create`

`POST /api/messages/groups`

Create a group chat

Body (application/json):
  - `name` (string, required)
  - `memberIds` (string[])

### `messages.groups.members.create`

`POST /api/messages/groups/{groupId}/members`

Add a member to a group chat

Adds a workspace member to a custom group chat. The caller must be a current group member; the target must be an active member of the workspace. Team-kind groups mirror workspace teams and reject membership edits. Adding an existing member is an idempotent no-op.

Path params (positional, in order):
  - `groupId`

Body (application/json):
  - `userId` (string, required)

### `messages.groups.members.delete`

`DELETE /api/messages/groups/{groupId}/members`

Leave a group chat or remove a member

With no body (or your own userId), leaves the group — always allowed on custom groups. With another user's id (JSON body `userId` or the `userId` query parameter), removes that member — workspace admins or the group creator only. The removed user's thread history is preserved. Team-kind groups reject membership edits.

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `groupId`

Query:
  - `userId` (string)

Body (application/json):
  - `userId` (string)

### `messages.list`

`GET /api/messages`

Get all messages, contacts, and preferences

### `messages.mentions.list`

`GET /api/messages/mentions`

List mentions

### `messages.notifications.list`

`GET /api/messages/notifications`

List notifications

### `messages.notifications.update`

`PATCH /api/messages/notifications`

Update notifications

Body: application/json (free-form — pass with `--data`)

### `messages.presence.create`

`POST /api/messages/presence`

Create presence

Body: application/json (free-form — pass with `--data`)

### `messages.project-links.create`

`POST /api/messages/project-links`

Create project link

Body: application/json (free-form — pass with `--data`)

### `messages.project-links.delete`

`DELETE /api/messages/project-links`

Delete project links

**Destructive** — needs `--yes` against a non-local base URL.

### `messages.project-links.list`

`GET /api/messages/project-links`

List project links

### `messages.push.subscribe.create`

`POST /api/messages/push/subscribe`

Create subscribe

Body: application/json (free-form — pass with `--data`)

### `messages.push.subscribe.delete`

`DELETE /api/messages/push/subscribe`

Delete subscribe

**Destructive** — needs `--yes` against a non-local base URL.

### `messages.push.vapid-key.list`

`GET /api/messages/push/vapid-key`

List vapid key

### `messages.requests.count.list`

`GET /api/messages/requests/count`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `messages.requests.create`

`POST /api/messages/requests`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `messages.requests.list`

`GET /api/messages/requests`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `messages.requests.lookup.list`

`GET /api/messages/requests/lookup`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `messages.requests.respond.create`

`POST /api/messages/requests/{p1}/respond`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `messages.rtc-config.list`

`GET /api/messages/rtc-config`

ICE servers for the chat call transport

STUN/TURN servers the browser should build its RTCPeerConnection with. Authenticated because TURN credentials are relay credentials. An empty list means "use public STUN only".

### `messages.scheduled-processor.create`

`POST /api/messages/scheduled-processor`

Create scheduled processor

Body: application/json (free-form — pass with `--data`)

### `messages.scheduled.create`

`POST /api/messages/scheduled`

Create scheduled

Body: application/json (free-form — pass with `--data`)

### `messages.scheduled.delete`

`DELETE /api/messages/scheduled/{messageId}`

Delete scheduled

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `messageId`

### `messages.scheduled.list`

`GET /api/messages/scheduled`

List scheduled

### `messages.scheduled.update`

`PATCH /api/messages/scheduled/{messageId}`

Update scheduled

Path params (positional, in order):
  - `messageId`

Body: application/json (free-form — pass with `--data`)

### `messages.search.list`

`GET /api/messages/search`

List search

### `messages.stream.list`

`GET /api/messages/stream`

List stream

### `messages.templates.create`

`POST /api/messages/templates`

Create template

Body: application/json (free-form — pass with `--data`)

### `messages.templates.create.by-templateId`

`POST /api/messages/templates/{templateId}`

Action on template

Path params (positional, in order):
  - `templateId`

Body: application/json (free-form — pass with `--data`)

### `messages.templates.delete`

`DELETE /api/messages/templates/{templateId}`

Delete template

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `templateId`

### `messages.templates.get`

`GET /api/messages/templates/{templateId}`

Fetch template

Path params (positional, in order):
  - `templateId`

### `messages.templates.list`

`GET /api/messages/templates`

List templates

### `messages.templates.update`

`PATCH /api/messages/templates/{templateId}`

Update template

Path params (positional, in order):
  - `templateId`

Body: application/json (free-form — pass with `--data`)

### `messages.threads.delete`

`DELETE /api/messages/threads/{contactId}`

Delete a conversation thread

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `contactId`

### `messages.threads.deliver.create`

`POST /api/messages/threads/{p1}/deliver`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `messages.threads.meeting.recording.chunk.create`

`POST /api/messages/threads/{contactId}/meeting/recording/{recordingId}/chunk`

Create chunk

Path params (positional, in order):
  - `contactId`
  - `recordingId`

Body: application/json (free-form — pass with `--data`)

### `messages.threads.meeting.recording.consent.create`

`POST /api/messages/threads/{contactId}/meeting/recording/{recordingId}/consent`

Create consent

Path params (positional, in order):
  - `contactId`
  - `recordingId`

Body: application/json (free-form — pass with `--data`)

### `messages.threads.meeting.recording.create`

`POST /api/messages/threads/{contactId}/meeting/recording`

Create recording

Path params (positional, in order):
  - `contactId`

Body: application/json (free-form — pass with `--data`)

### `messages.threads.meeting.recording.delete`

`DELETE /api/messages/threads/{contactId}/meeting/recording/{recordingId}`

Delete recording

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `contactId`
  - `recordingId`

### `messages.threads.meeting.recording.get`

`GET /api/messages/threads/{contactId}/meeting/recording/{recordingId}`

Fetch recording

Path params (positional, in order):
  - `contactId`
  - `recordingId`

### `messages.threads.meeting.recording.list`

`GET /api/messages/threads/{contactId}/meeting/recording`

List recording

Path params (positional, in order):
  - `contactId`

### `messages.threads.meeting.recording.stop.create`

`POST /api/messages/threads/{contactId}/meeting/recording/{recordingId}/stop`

Create stop

Path params (positional, in order):
  - `contactId`
  - `recordingId`

Body: application/json (free-form — pass with `--data`)

### `messages.threads.meeting.recording.transcript.create`

`POST /api/messages/threads/{contactId}/meeting/recording/{recordingId}/transcript`

Create transcript

Path params (positional, in order):
  - `contactId`
  - `recordingId`

Body: application/json (free-form — pass with `--data`)

### `messages.threads.meeting.recording.transcript.list`

`GET /api/messages/threads/{contactId}/meeting/recording/{recordingId}/transcript`

List transcript

Path params (positional, in order):
  - `contactId`
  - `recordingId`

### `messages.threads.meeting.recording.transcript.update`

`PATCH /api/messages/threads/{p1}/meeting/recording/{p2}/transcript`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`
  - `p2`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `messages.threads.meeting.twin.create`

`POST /api/messages/threads/{p1}/meeting/twin`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `messages.threads.meeting.twin.delete`

`DELETE /api/messages/threads/{p1}/meeting/twin`

(undocumented route — params unknown, pass them explicitly)

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `messages.threads.meeting.twin.host-token.create`

`POST /api/messages/threads/{p1}/meeting/twin/host-token`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `messages.threads.meeting.twin.list`

`GET /api/messages/threads/{p1}/meeting/twin`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `messages.threads.meeting.twin.listen.create`

`POST /api/messages/threads/{p1}/meeting/twin/listen`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `messages.threads.meeting.twin.room.list`

`GET /api/messages/threads/{p1}/meeting/twin/room`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `messages.threads.meeting.twin.signals.create`

`POST /api/messages/threads/{p1}/meeting/twin/signals`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `messages.threads.meeting.twin.signals.list`

`GET /api/messages/threads/{p1}/meeting/twin/signals`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `messages.threads.meeting.twin.speak.create`

`POST /api/messages/threads/{p1}/meeting/twin/speak`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `messages.threads.members.list`

`GET /api/messages/threads/{contactId}/members`

List the members of a group-type chat (team chat, group, or channel)

Returns who is in a workspace team chat, managed group chat, or channel. The caller must be a participant (private channels included). Direct-message threads return 404 — they have presence, not a member list.

Path params (positional, in order):
  - `contactId`

### `messages.threads.messages.create`

`POST /api/messages/threads/{contactId}/messages`

Send a message

Path params (positional, in order):
  - `contactId`

Body (application/json):
  - `content` (string)
  - `attachments` (object[])

### `messages.threads.messages.delete`

`DELETE /api/messages/threads/{contactId}/messages/{messageId}`

Delete a message

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `contactId`
  - `messageId`

### `messages.threads.messages.forward.create`

`POST /api/messages/threads/{contactId}/messages/forward`

Create forward

Path params (positional, in order):
  - `contactId`

Body: application/json (free-form — pass with `--data`)

### `messages.threads.messages.list`

`GET /api/messages/threads/{p1}/messages`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `messages.threads.messages.reactions.create`

`POST /api/messages/threads/{contactId}/messages/{messageId}/reactions`

Toggle an emoji reaction on a message

Toggles the caller's reaction for the given emoji — adds it when absent, removes it when present. The change fans out to every participant's copy of the message, so all participants see the same attributed reaction list. The caller must be a participant of the thread. Reactions are returned as `[{emoji, userIds}]`; a message carries at most 20 distinct emoji.

Path params (positional, in order):
  - `contactId`
  - `messageId`

Body (application/json):
  - `emoji` (string, required) — A single emoji (one grapheme, max 16 characters).

### `messages.threads.messages.read.create`

`POST /api/messages/threads/{contactId}/messages/{messageId}/read`

Create read

Path params (positional, in order):
  - `contactId`
  - `messageId`

Body: application/json (free-form — pass with `--data`)

### `messages.threads.messages.replies.create`

`POST /api/messages/threads/{contactId}/messages/{messageId}/replies`

Reply in a message thread

Path params (positional, in order):
  - `contactId`
  - `messageId`

Body: application/json (free-form — pass with `--data`)

### `messages.threads.messages.replies.list`

`GET /api/messages/threads/{contactId}/messages/{messageId}/replies`

List replies

Path params (positional, in order):
  - `contactId`
  - `messageId`

### `messages.threads.messages.update`

`PATCH /api/messages/threads/{contactId}/messages/{messageId}`

Edit a message

Path params (positional, in order):
  - `contactId`
  - `messageId`

Body (application/json):
  - `content` (string)

### `messages.threads.pinned.list`

`GET /api/messages/threads/{contactId}/pinned`

List pinned

Path params (positional, in order):
  - `contactId`

### `messages.threads.typing.update`

`PATCH /api/messages/threads/{contactId}/typing`

Set typing state

Path params (positional, in order):
  - `contactId`

Body (application/json):
  - `typing` (boolean)

### `messages.threads.update`

`PATCH /api/messages/threads/{contactId}`

Update thread flags (pin, mute, block, etc.)

Path params (positional, in order):
  - `contactId`

Body (application/json):
  - `pinned` (boolean)
  - `muted` (boolean)
  - `blocked` (boolean)
  - `archived` (boolean)
  - `hidden` (boolean)

### `messages.update`

`PATCH /api/messages`

Update chat preferences

Body (application/json):
  - `preferences` (object)
  - `preferences.activeStatus` (boolean)
  - `preferences.notificationSound` (boolean)
  - `preferences.doNotDisturb` (boolean)

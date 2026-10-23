# Meetings

13 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `meetings.create` | POST | `/api/meetings` | (undocumented route — params unknown, pass them explicitly) |
| `meetings.delete` | DELETE | `/api/meetings/{p1}` | (undocumented route — params unknown, pass them explicitly) |
| `meetings.get` | GET | `/api/meetings/{p1}` | (undocumented route — params unknown, pass them explicitly) |
| `meetings.list` | GET | `/api/meetings` | (undocumented route — params unknown, pass them explicitly) |
| `meetings.send-invites.create` | POST | `/api/meetings/{p1}/send-invites` | (undocumented route — params unknown, pass them explicitly) |
| `meetings.update` | PATCH | `/api/meetings/{p1}` | (undocumented route — params unknown, pass them explicitly) |
| `messages.threads.meeting.list` | GET | `/api/messages/threads/{contactId}/meeting` | Get meeting session |
| `messages.threads.meeting.messages.create` | POST | `/api/messages/threads/{contactId}/meeting/messages` | Send a meeting chat message |
| `messages.threads.meeting.participants.create` | POST | `/api/messages/threads/{contactId}/meeting/participants` | Add a meeting participant |
| `messages.threads.meeting.participants.update` | PATCH | `/api/messages/threads/{contactId}/meeting/participants` | Update a meeting participant (mute, kick) |
| `messages.threads.meeting.signals.create` | POST | `/api/messages/threads/{contactId}/meeting/signals` | Send a WebRTC signal |
| `messages.threads.meeting.signals.list` | GET | `/api/messages/threads/{contactId}/meeting/signals` | Poll for WebRTC signals |
| `messages.threads.meeting.update` | PATCH | `/api/messages/threads/{contactId}/meeting` | Update meeting controls or end/leave meeting |

---

### `meetings.create`

`POST /api/meetings`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `meetings.delete`

`DELETE /api/meetings/{p1}`

(undocumented route — params unknown, pass them explicitly)

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `meetings.get`

`GET /api/meetings/{p1}`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `meetings.list`

`GET /api/meetings`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `meetings.send-invites.create`

`POST /api/meetings/{p1}/send-invites`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `meetings.update`

`PATCH /api/meetings/{p1}`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

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

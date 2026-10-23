# Workspace

32 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `workspace.create.create` | POST | `/api/workspace/create` | Create a new workspace |
| `workspace.delete` | DELETE | `/api/workspace` | Delete workspace |
| `workspace.guests.create` | POST | `/api/workspace/guests` | Create guest |
| `workspace.guests.delete` | DELETE | `/api/workspace/guests/{userId}` | Delete guest |
| `workspace.guests.list` | GET | `/api/workspace/guests` | List guests |
| `workspace.guests.update` | PATCH | `/api/workspace/guests/{userId}` | Update guest |
| `workspace.invites.approve.create` | POST | `/api/workspace/invites/{inviteId}/approve` | Approve a member-raised invite request |
| `workspace.invites.bulk.create` | POST | `/api/workspace/invites/bulk` | Create bulk |
| `workspace.invites.create` | POST | `/api/workspace/invites` | Create invite |
| `workspace.invites.csv.create` | POST | `/api/workspace/invites/csv` | Create csv |
| `workspace.invites.delete` | DELETE | `/api/workspace/invites/{inviteId}` | Delete invite |
| `workspace.invites.list` | GET | `/api/workspace/invites` | List invites |
| `workspace.invites.resend.create` | POST | `/api/workspace/invites/{inviteId}/resend` | Create resend |
| `workspace.invites.update` | PATCH | `/api/workspace/invites/{inviteId}` | Update invite |
| `workspace.list.list` | GET | `/api/workspace/list` | List the caller's workspaces |
| `workspace.members.create` | POST | `/api/workspace/members` | Create member |
| `workspace.members.delete` | DELETE | `/api/workspace/members/{userId}` | Delete member |
| `workspace.members.deprovision.create` | POST | `/api/workspace/members/{userId}/deprovision` | Create deprovision |
| `workspace.members.deprovision.list` | GET | `/api/workspace/members/{userId}/deprovision` | List deprovision |
| `workspace.members.list` | GET | `/api/workspace/members` | List members |
| `workspace.members.mfa-reset.create` | POST | `/api/workspace/members/{userId}/mfa-reset` | Reset a member's two-factor authentication |
| `workspace.members.provision.create` | POST | `/api/workspace/members/provision` | (undocumented route — params unknown, pass them explicitly) |
| `workspace.members.transfer.create` | POST | `/api/workspace/members/{userId}/transfer` | Create transfer |
| `workspace.members.transfer.list` | GET | `/api/workspace/members/{userId}/transfer` | List transfer |
| `workspace.members.update` | PATCH | `/api/workspace/members/{userId}` | Update member |
| `workspace.recording-policy.list` | GET | `/api/workspace/recording-policy` | List recording policy |
| `workspace.recording-policy.update` | PATCH | `/api/workspace/recording-policy` | Update recording policy |
| `workspace.seats.list` | GET | `/api/workspace/seats` | List seats |
| `workspace.seats.named.create` | POST | `/api/workspace/seats/named/{userId}` | Assign a named seat to a member |
| `workspace.seats.named.delete` | DELETE | `/api/workspace/seats/named/{userId}` | Remove a named seat from a member |
| `workspace.seats.set` | PUT | `/api/workspace/seats` | Update seats |
| `workspace.switch.create` | POST | `/api/workspace/switch` | Switch the active workspace (session callers only) |

---

### `workspace.create.create`

`POST /api/workspace/create`

Create a new workspace

Body: application/json (free-form — pass with `--data`)

### `workspace.delete`

`DELETE /api/workspace`

Delete workspace

**Destructive** — needs `--yes` against a non-local base URL.

### `workspace.guests.create`

`POST /api/workspace/guests`

Create guest

Body: application/json (free-form — pass with `--data`)

### `workspace.guests.delete`

`DELETE /api/workspace/guests/{userId}`

Delete guest

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `userId`

### `workspace.guests.list`

`GET /api/workspace/guests`

List guests

### `workspace.guests.update`

`PATCH /api/workspace/guests/{userId}`

Update guest

Path params (positional, in order):
  - `userId`

Body: application/json (free-form — pass with `--data`)

### `workspace.invites.approve.create`

`POST /api/workspace/invites/{inviteId}/approve`

Approve a member-raised invite request

Admin-only. Approves an invite with status `requested` (created by a member when the workspace `invite_policy` is `members-with-approval`), rotating its token and expiry and sending the invite email. Returns 409 if the invite is not in the `requested` state.

Path params (positional, in order):
  - `inviteId`

### `workspace.invites.bulk.create`

`POST /api/workspace/invites/bulk`

Create bulk

Admin only. Invites up to 50 `emails` at one `role`. Seats are checked for the whole batch before anything is sent: pending invites hold a seat, people already in the workspace or already invited are skipped and use none, and a batch that does not fit is refused with 402 and nothing is sent.

**Destructive** — needs `--yes` against a non-local base URL.

Body: application/json (free-form — pass with `--data`)

### `workspace.invites.create`

`POST /api/workspace/invites`

Create invite

Optional `workspaceId` in the body names the workspace the calling page was loaded from; a mismatch with the session's workspace is refused with 409 `bundle_workspace_mismatch`.

Body: application/json (free-form — pass with `--data`)

### `workspace.invites.csv.create`

`POST /api/workspace/invites/csv`

Create csv

Admin only. Invites up to 200 people from a `csv` string (header `email`, optional `name`, `role`, `projects`) or parsed `rows` (`email`, `name`, `role`, `project_refs`, `team`). Seats are checked for the whole batch before anything is sent: pending invites hold a seat, people already in the workspace or already invited are skipped and use none, and a batch that does not fit is refused with 402 and nothing is sent. `project_refs` (project ids, or names in a CSV) are granted by email, so each person has those projects when they accept; a ref that names no project fails its row. When projects were granted, `projectAccess` carries the bundle `previousVersion` and `version`, so a page holding the bundle can adopt the new version.

Body: application/json (free-form — pass with `--data`)

### `workspace.invites.delete`

`DELETE /api/workspace/invites/{inviteId}`

Delete invite

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `inviteId`

### `workspace.invites.list`

`GET /api/workspace/invites`

List invites

### `workspace.invites.resend.create`

`POST /api/workspace/invites/{inviteId}/resend`

Create resend

Path params (positional, in order):
  - `inviteId`

Query:
  - `workspaceId` (string) — The workspace the calling page was loaded from; a mismatch is refused with 409 `bundle_workspace_mismatch`.

Body: application/json (free-form — pass with `--data`)

### `workspace.invites.update`

`PATCH /api/workspace/invites/{inviteId}`

Update invite

Path params (positional, in order):
  - `inviteId`

Body: application/json (free-form — pass with `--data`)

### `workspace.list.list`

`GET /api/workspace/list`

List the caller's workspaces

### `workspace.members.create`

`POST /api/workspace/members`

Create member

Body: application/json (free-form — pass with `--data`)

### `workspace.members.delete`

`DELETE /api/workspace/members/{userId}`

Delete member

Removes the membership and ends the member's sessions. Refuses removing yourself, the last owner or the last admin; removing an owner requires owner. Optional `workspaceId` names the workspace the calling page was loaded from; a mismatch is refused with 409 `bundle_workspace_mismatch`.

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `userId`

Query:
  - `workspaceId` (string)

### `workspace.members.deprovision.create`

`POST /api/workspace/members/{userId}/deprovision`

Create deprovision

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `userId`

Body: application/json (free-form — pass with `--data`)

### `workspace.members.deprovision.list`

`GET /api/workspace/members/{userId}/deprovision`

List deprovision

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `userId`

### `workspace.members.list`

`GET /api/workspace/members`

List members

### `workspace.members.mfa-reset.create`

`POST /api/workspace/members/{userId}/mfa-reset`

Reset a member's two-factor authentication

Clears a member's authenticator, passkeys and recovery codes so they can enrol a new device — the lost-device path. Admin-only; resetting another admin or the owner requires owner. Never self-service. Audited, and the affected member is emailed.

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `userId`

### `workspace.members.provision.create`

`POST /api/workspace/members/provision`

(undocumented route — params unknown, pass them explicitly)

**Destructive** — needs `--yes` against a non-local base URL.

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `workspace.members.transfer.create`

`POST /api/workspace/members/{userId}/transfer`

Create transfer

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `userId`

Body: application/json (free-form — pass with `--data`)

### `workspace.members.transfer.list`

`GET /api/workspace/members/{userId}/transfer`

List transfer

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `userId`

### `workspace.members.update`

`PATCH /api/workspace/members/{userId}`

Update member

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `userId`

Body: application/json (free-form — pass with `--data`)

### `workspace.recording-policy.list`

`GET /api/workspace/recording-policy`

List recording policy

### `workspace.recording-policy.update`

`PATCH /api/workspace/recording-policy`

Update recording policy

Body: application/json (free-form — pass with `--data`)

### `workspace.seats.list`

`GET /api/workspace/seats`

List seats

### `workspace.seats.named.create`

`POST /api/workspace/seats/named/{userId}`

Assign a named seat to a member

Path params (positional, in order):
  - `userId`

Body: application/json (free-form — pass with `--data`)

### `workspace.seats.named.delete`

`DELETE /api/workspace/seats/named/{userId}`

Remove a named seat from a member

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `userId`

### `workspace.seats.set`

`PUT /api/workspace/seats`

Update seats

Body: application/json (free-form — pass with `--data`)

### `workspace.switch.create`

`POST /api/workspace/switch`

Switch the active workspace (session callers only)

Sets the browser's active-workspace cookie after validating membership. API-key callers get 409 — keys are bound to one workspace at mint time and cannot switch; mint a key in the target workspace instead.

Body (application/json):
  - `workspaceId` (string, required)

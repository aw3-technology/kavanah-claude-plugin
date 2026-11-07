# Workspace

49 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `hub.list` | GET | `/api/hub` | Cross-workspace hub bundle |
| `kvn.generate.create` | POST | `/api/kvn/generate` | AI-draft one axis of the workspace charter |
| `kvn.list` | GET | `/api/kvn` | Get the workspace charter (Know-how, Vision, Negation, bets, North Star) |
| `kvn.negation-hits.list` | GET | `/api/kvn/negation-hits` | The Negation ledger |
| `kvn.north-star.create` | POST | `/api/kvn/north-star` | Record a North Star reading |
| `kvn.north-star.list` | GET | `/api/kvn/north-star` | The effective North Star for the workspace or a project |
| `kvn.set` | PUT | `/api/kvn` | Update the workspace charter |
| `kvn.task-generate.create` | POST | `/api/kvn/task-generate` | AI-draft one charter axis for a task being created |
| `orgs.create` | POST | `/api/orgs` | Create an organization |
| `orgs.delete` | DELETE | `/api/orgs/{id}` | Delete an organization |
| `orgs.get` | GET | `/api/orgs/{id}` | Get an organization the caller can access |
| `orgs.list` | GET | `/api/orgs` | List the organizations the caller belongs to |
| `orgs.members.create` | POST | `/api/orgs/{id}/members` | Add a user to an organization |
| `orgs.members.delete` | DELETE | `/api/orgs/{id}/members` | Remove a user from an organization |
| `orgs.update` | PATCH | `/api/orgs/{id}` | Rename an organization |
| `orgs.workspaces.create` | POST | `/api/orgs/{id}/workspaces` | Attach a workspace to an organization |
| `search.recents.list` | GET | `/api/search/recents` | Recents feed for the command palette |
| `workspace.create.create` | POST | `/api/workspace/create` | Create a new workspace |
| `workspace.delete` | DELETE | `/api/workspace` | Delete workspace |
| `workspace.guests.create` | POST | `/api/workspace/guests` | Add a guest scoped to specific projects |
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
| `workspace.members.create` | POST | `/api/workspace/members` | Invite an account or change a member's role |
| `workspace.members.delete` | DELETE | `/api/workspace/members/{userId}` | Delete member |
| `workspace.members.deprovision.create` | POST | `/api/workspace/members/{userId}/deprovision` | Create deprovision |
| `workspace.members.deprovision.list` | GET | `/api/workspace/members/{userId}/deprovision` | List deprovision |
| `workspace.members.list` | GET | `/api/workspace/members` | List members |
| `workspace.members.mfa-reset.create` | POST | `/api/workspace/members/{userId}/mfa-reset` | Reset a member's two-factor authentication |
| `workspace.members.provision.create` | POST | `/api/workspace/members/provision` | Create an account for a teammate, or invite an existing account |
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

### `hub.list`

`GET /api/hub`

Cross-workspace hub bundle

Signed-in users. Returns the caller's workspaces, their tasks and recent activity across every workspace they belong to, plus the active workspace id. The only cross-workspace surface; it does not scope to the active workspace.

### `kvn.generate.create`

`POST /api/kvn/generate`

AI-draft one axis of the workspace charter

Admins only. Drafts text for know_how, vision or negation; it does not save. Billed to the caller's credits.

Body (application/json):
  - `field` (string, required) — one of: `know_how`, `vision`, `negation`
  - `axis` (string) — one of: `know_how`, `vision`, `negation`
  - `prompt` (string)

### `kvn.list`

`GET /api/kvn`

Get the workspace charter (Know-how, Vision, Negation, bets, North Star)

Any workspace member.

### `kvn.negation-hits.list`

`GET /api/kvn/negation-hits`

The Negation ledger

Any workspace member. What the charter refused and which Negation lines did the refusing, over a lookback window.

Query:
  - `days` (integer)
  - `project_ref` (string)

### `kvn.north-star.create`

`POST /api/kvn/north-star`

Record a North Star reading

Appends a measurement to the workspace metric (admins only) or a project's own metric (project edit permission). Does not edit the metric itself. Invalidates the cached charter and writes an audit entry.

Body (application/json):
  - `value` (number, required)
  - `note` (string)
  - `projectRef` (string)

### `kvn.north-star.list`

`GET /api/kvn/north-star`

The effective North Star for the workspace or a project

Any workspace member (project view permission when `projectRef` is given). The response says whether a project's metric is its own or inherited from the workspace.

Query:
  - `projectRef` (string)

### `kvn.set`

`PUT /api/kvn`

Update the workspace charter

Admins only. Partial update: absent keys are left alone. Text fields are capped at 8,000 characters; `bets` replaces the list (max 12); `northStar` merges over the stored metric, and `null` clears it. Invalidates the agent's cached charter immediately.

Body (application/json):
  - `knowHow` (string|null)
  - `know_how` (string|null)
  - `vision` (string|null)
  - `negation` (string|null)
  - `bets` (object[])
  - `northStar` (object|null)

### `kvn.task-generate.create`

`POST /api/kvn/task-generate`

AI-draft one charter axis for a task being created

Signed-in users. Drafts know_how, vision or negation text from an unsaved task's title and description; it does not save. Billed to the caller's credits.

Body (application/json):
  - `axis` (string, required) — one of: `know_how`, `vision`, `negation`
  - `title` (string, required)
  - `description` (string)
  - `projectRef` (string)
  - `prompt` (string)

### `orgs.create`

`POST /api/orgs`

Create an organization

The caller becomes the org owner.

Body (application/json):
  - `name` (string, required)
  - `description` (string)

### `orgs.delete`

`DELETE /api/orgs/{id}`

Delete an organization

Org owner only. Personal orgs cannot be deleted, and every workspace must be detached first.

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `orgs.get`

`GET /api/orgs/{id}`

Get an organization the caller can access

Path params (positional, in order):
  - `id`

### `orgs.list`

`GET /api/orgs`

List the organizations the caller belongs to

### `orgs.members.create`

`POST /api/orgs/{id}/members`

Add a user to an organization

Org owners and admins only. role defaults to member.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `userId` (string, required)
  - `role` (string) — one of: `owner`, `admin`, `member`

### `orgs.members.delete`

`DELETE /api/orgs/{id}/members`

Remove a user from an organization

Org owners and admins only; cannot remove yourself or the org owner.

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

Query:
  - `userId` (string, required)

### `orgs.update`

`PATCH /api/orgs/{id}`

Rename an organization

Org owners and admins only.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `name` (string, required)
  - `description` (string)

### `orgs.workspaces.create`

`POST /api/orgs/{id}/workspaces`

Attach a workspace to an organization

Caller must be an org owner or admin and the workspace's owner.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `workspaceId` (string, required)

### `search.recents.list`

`GET /api/search/recents`

Recents feed for the command palette

Returns up to 12 recent tasks from projects the caller may view, all viewable projects, and up to 12 recent non-archived clients (only with clients:view, hidden records excluded).

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

Add a guest scoped to specific projects

Admins only. `projectRefs` (at least one) limits what the guest can see; `expiresAt` (optional, ISO, in the future, at most one year out) ends their access. Scope and expiry are enforced on every surface, including API keys the guest mints. An address that already has a Kavanah account is sent an invite to accept rather than added (`invited: true`). Counts against the seat limit.

Body (application/json):
  - `email` (string<email>, required)
  - `fullName` (string)
  - `projectRefs` (string[], required)
  - `expiresAt` (string<date-time>)

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

Invite an account or change a member's role

Admin only. For someone already in the workspace, sets their role (owner and admin need an owner; never your own role; never strands the last owner or admin) and ends their sessions in this workspace. For an account that is not yet a member, nothing is added: an invitation with that role is minted and emailed, and they join when they accept (202). The invite holds a seat, so a full workspace answers 403.

Body (application/json):
  - `userId` (string, required)
  - `role` (string) — one of: `owner`, `admin`, `member`

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

Create an account for a teammate, or invite an existing account

Admins only; rate-limited to 20 per minute. Enforces the seat limit. A new account gets a temporary password (returned once and emailed; must be changed at first login), the signup credit bonus, and is added to the workspace. An address that already has a Kavanah account is NOT added; it is sent a workspace invite to accept (`createdAccount false`, `invited true`, no temporary password). Writes an audit entry.

**Destructive** — needs `--yes` against a non-local base URL.

Body (application/json):
  - `email` (string<email>, required)
  - `firstName` (string)
  - `lastName` (string)
  - `role` (string) — one of: `admin`, `member`

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

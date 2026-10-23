# Projects

44 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `project-keys.create` | POST | `/api/project-keys` | Create project key |
| `project-keys.list` | GET | `/api/project-keys` | List project keys |
| `project-keys.set` | PUT | `/api/project-keys` | Update project keys |
| `project-templates.create` | POST | `/api/project-templates` | Create project template |
| `project-templates.delete` | DELETE | `/api/project-templates/{id}` | Delete project template |
| `project-templates.get` | GET | `/api/project-templates/{id}` | Fetch project template |
| `project-templates.instantiate.create` | POST | `/api/project-templates/{id}/instantiate` | Create instantiate |
| `project-templates.list` | GET | `/api/project-templates` | List project templates |
| `project-templates.set` | PUT | `/api/project-templates/{id}` | Update project template |
| `projects.archive.create` | POST | `/api/projects/archive` | Create archive |
| `projects.budget.create` | POST | `/api/projects/budget` | Create budget |
| `projects.budget.entries.create` | POST | `/api/projects/budget/entries` | Create a budget entry |
| `projects.budget.entries.delete` | DELETE | `/api/projects/budget/entries` | Delete entries |
| `projects.budget.list` | GET | `/api/projects/budget` | List budget |
| `projects.create` | POST | `/api/projects` | Create a project |
| `projects.delete` | DELETE | `/api/projects/{id}` | Delete a project and its resources |
| `projects.duplicate.create` | POST | `/api/projects/duplicate` | Create duplicate |
| `projects.folders.create` | POST | `/api/projects/folders` | Create a project folder (admin) |
| `projects.folders.delete` | DELETE | `/api/projects/folders` | Delete a project folder (admin) |
| `projects.folders.list` | GET | `/api/projects/folders` | List project folders |
| `projects.folders.update` | PATCH | `/api/projects/folders` | Reorder folders or update one folder (admin) |
| `projects.get` | GET | `/api/projects/{id}` | Get a single project |
| `projects.health.list` | GET | `/api/projects/health` | List health |
| `projects.health.set` | PUT | `/api/projects/health` | Update health |
| `projects.icon.create` | POST | `/api/projects/{id}/icon` | Create icon |
| `projects.icon.delete` | DELETE | `/api/projects/{id}/icon` | Delete icon |
| `projects.kvn.create` | POST | `/api/projects/kvn` | (undocumented route — params unknown, pass them explicitly) |
| `projects.kvn.delete` | DELETE | `/api/projects/kvn` | (undocumented route — params unknown, pass them explicitly) |
| `projects.kvn.generate.create` | POST | `/api/projects/kvn/generate` | (undocumented route — params unknown, pass them explicitly) |
| `projects.kvn.list` | GET | `/api/projects/kvn` | (undocumented route — params unknown, pass them explicitly) |
| `projects.kvn.set` | PUT | `/api/projects/kvn` | (undocumented route — params unknown, pass them explicitly) |
| `projects.list` | GET | `/api/projects` | Get workspace project bundle |
| `projects.members.create` | POST | `/api/projects/{id}/members` | Add a member to a project |
| `projects.members.delete` | DELETE | `/api/projects/{id}/members` | Remove a member from a project |
| `projects.members.delete.by-userId` | DELETE | `/api/projects/{id}/members/{userId}` | Delete member |
| `projects.phases.create` | POST | `/api/projects/phases` | Create phase |
| `projects.phases.delete` | DELETE | `/api/projects/phases/{id}` | Delete phase |
| `projects.phases.list` | GET | `/api/projects/phases` | List phases |
| `projects.phases.update` | PATCH | `/api/projects/phases/{id}` | Update phase |
| `projects.roadmap.list` | GET | `/api/projects/roadmap` | List roadmap |
| `projects.teams.create` | POST | `/api/projects/{id}/teams` | Create team |
| `projects.teams.delete` | DELETE | `/api/projects/{id}/teams` | Delete teams |
| `projects.update` | PATCH | `/api/projects` | Update workspace project bundle |
| `projects.visibility.update` | PATCH | `/api/projects/{id}/visibility` | Update visibility |

---

### `project-keys.create`

`POST /api/project-keys`

Create project key

Body: application/json (free-form — pass with `--data`)

### `project-keys.list`

`GET /api/project-keys`

List project keys

### `project-keys.set`

`PUT /api/project-keys`

Update project keys

Body: application/json (free-form — pass with `--data`)

### `project-templates.create`

`POST /api/project-templates`

Create project template

Body: application/json (free-form — pass with `--data`)

### `project-templates.delete`

`DELETE /api/project-templates/{id}`

Delete project template

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `project-templates.get`

`GET /api/project-templates/{id}`

Fetch project template

Path params (positional, in order):
  - `id`

### `project-templates.instantiate.create`

`POST /api/project-templates/{id}/instantiate`

Create instantiate

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `project-templates.list`

`GET /api/project-templates`

List project templates

### `project-templates.set`

`PUT /api/project-templates/{id}`

Update project template

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `projects.archive.create`

`POST /api/projects/archive`

Create archive

Body: application/json (free-form — pass with `--data`)

### `projects.budget.create`

`POST /api/projects/budget`

Create budget

Body: application/json (free-form — pass with `--data`)

### `projects.budget.entries.create`

`POST /api/projects/budget/entries`

Create a budget entry

Body: application/json (free-form — pass with `--data`)

### `projects.budget.entries.delete`

`DELETE /api/projects/budget/entries`

Delete entries

**Destructive** — needs `--yes` against a non-local base URL.

### `projects.budget.list`

`GET /api/projects/budget`

List budget

### `projects.create`

`POST /api/projects`

Create a project

Creates a single project. Only `name` is required — the 3-step UI wizard asks for a project type, but that is a UI affordance, not a data requirement. Honours `Idempotency-Key`.

Body (application/json):
  - `name` (string, required) — Project name. The only required field.
  - `projectType` (string)
  - `description` (string)
  - `clientId` (string|null)
  - `startDate` (string|null) — Calendar date (YYYY-MM-DD).
  - `deadline` (string|null) — Calendar date (YYYY-MM-DD).
  - `visibility` (string) — one of: `public`, `private`
  - `members` (object[])

### `projects.delete`

`DELETE /api/projects/{id}`

Delete a project and its resources

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `projects.duplicate.create`

`POST /api/projects/duplicate`

Create duplicate

Body: application/json (free-form — pass with `--data`)

### `projects.folders.create`

`POST /api/projects/folders`

Create a project folder (admin)

Body (application/json):
  - `name` (string, required)
  - `color` (string)

### `projects.folders.delete`

`DELETE /api/projects/folders`

Delete a project folder (admin)

Accepts `?id=` or a JSON body `{ id }`. Projects in the folder fall back to Uncategorized.

**Destructive** — needs `--yes` against a non-local base URL.

Query:
  - `id` (string)

### `projects.folders.list`

`GET /api/projects/folders`

List project folders

### `projects.folders.update`

`PATCH /api/projects/folders`

Reorder folders or update one folder (admin)

Reorder mode when `order` (string[] of ids) is supplied; otherwise updates the folder identified by `id`.

Body (application/json):
  - `order` (string[])
  - `id` (string)
  - `name` (string)
  - `color` (string)

### `projects.get`

`GET /api/projects/{id}`

Get a single project

Path params (positional, in order):
  - `id`

### `projects.health.list`

`GET /api/projects/health`

List health

### `projects.health.set`

`PUT /api/projects/health`

Update health

Body: application/json (free-form — pass with `--data`)

### `projects.icon.create`

`POST /api/projects/{id}/icon`

Create icon

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `projects.icon.delete`

`DELETE /api/projects/{id}/icon`

Delete icon

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `projects.kvn.create`

`POST /api/projects/kvn`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `projects.kvn.delete`

`DELETE /api/projects/kvn`

(undocumented route — params unknown, pass them explicitly)

**Destructive** — needs `--yes` against a non-local base URL.

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `projects.kvn.generate.create`

`POST /api/projects/kvn/generate`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `projects.kvn.list`

`GET /api/projects/kvn`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `projects.kvn.set`

`PUT /api/projects/kvn`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `projects.list`

`GET /api/projects`

Get workspace project bundle

### `projects.members.create`

`POST /api/projects/{id}/members`

Add a member to a project

Admin/owner only. Identify the person by `userId` or by `email`. The user must be an active member of THIS workspace; an email that is not yet a member raises a pending workspace invite as part of the same call, redeemable in-app via /api/invites/mine. Re-adding someone is a no-op and returns 200.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `userId` (string) — Must be an active member of this workspace.
  - `email` (string) — Alternative to userId. Invited if not yet a member.
  - `team` (string)

### `projects.members.delete`

`DELETE /api/projects/{id}/members`

Remove a member from a project

Admin/owner only. Identify by `email` (the ACL key) or `userId`.

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `email` (string)
  - `userId` (string)

### `projects.members.delete.by-userId`

`DELETE /api/projects/{id}/members/{userId}`

Delete member

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`
  - `userId`

### `projects.phases.create`

`POST /api/projects/phases`

Create phase

Body: application/json (free-form — pass with `--data`)

### `projects.phases.delete`

`DELETE /api/projects/phases/{id}`

Delete phase

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `projects.phases.list`

`GET /api/projects/phases`

List phases

### `projects.phases.update`

`PATCH /api/projects/phases/{id}`

Update phase

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `projects.roadmap.list`

`GET /api/projects/roadmap`

List roadmap

### `projects.teams.create`

`POST /api/projects/{id}/teams`

Create team

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `projects.teams.delete`

`DELETE /api/projects/{id}/teams`

Delete teams

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `projects.update`

`PATCH /api/projects`

Update workspace project bundle

Merges the submitted bundle onto the workspace's stored bundle. A PATCH never removes a project: one missing from `projects` (or sent with a non-numeric id or empty name) is KEPT. Deleting a project is `DELETE /api/projects/{id}`, which snapshots it to trash and cascades into its tasks, time entries, discussions, files and budget rows. `workspaceId` names the workspace the bundle was loaded from and `bundleVersion` the row version it was built on (every bundle the API returns carries both, as `workspaceId` and `version`): the save is refused with 409 when either is not what the server holds, and with 400 when a browser session omits either. API-key callers may omit them; when they echo, they are checked.

**Destructive** — needs `--yes` against a non-local base URL.

Body (application/json):
  - `projects` (object[])
  - `teamMembers` (object[])
  - `workspaceTeams` (object[])
  - `notifications` (object)
  - `integrations` (object)
  - `workspaceId` (string) — The workspace this bundle was loaded from, as returned by GET /api/projects. Required for browser sessions.
  - `bundleVersion` (string) — The `version` of the bundle this save was built on, as returned by GET /api/projects (the row's `updated_at`). Required for browser sessions.

### `projects.visibility.update`

`PATCH /api/projects/{id}/visibility`

Update visibility

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

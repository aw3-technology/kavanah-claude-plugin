# Planning

22 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `planning.budget-burn.list` | GET | `/api/planning/budget-burn` | List budget burn |
| `planning.calibration.list` | GET | `/api/planning/calibration` | List calibration |
| `planning.critical-path.list` | GET | `/api/planning/critical-path` | List critical path |
| `planning.dependencies.list` | GET | `/api/planning/dependencies` | List dependencies |
| `planning.grooming.apply.create` | POST | `/api/planning/grooming/apply` | Create apply |
| `planning.grooming.list` | GET | `/api/planning/grooming` | List grooming |
| `planning.leveling.apply.create` | POST | `/api/planning/leveling/apply` | Create apply |
| `planning.leveling.list` | GET | `/api/planning/leveling` | List leveling |
| `planning.scenarios.list` | GET | `/api/planning/scenarios` | List scenarios |
| `planning.scope-creep.baseline.create` | POST | `/api/planning/scope-creep/baseline` | Create baseline |
| `planning.scope-creep.list` | GET | `/api/planning/scope-creep` | List scope creep |
| `planning.sprint-planner.create` | POST | `/api/planning/sprint-planner` | Create sprint planner |
| `planning.sprint-planner.list` | GET | `/api/planning/sprint-planner` | List sprint planner |
| `planning.viable-scope.apply.create` | POST | `/api/planning/viable-scope/apply` | Create apply |
| `planning.viable-scope.list` | GET | `/api/planning/viable-scope` | List viable scope |
| `weekly-checkins.generate.create` | POST | `/api/weekly-checkins/generate` | Generate a draft weekly check-in now |
| `weekly-checkins.list` | GET | `/api/weekly-checkins` | List weekly check-ins |
| `weekly-checkins.members.list` | GET | `/api/weekly-checkins/members` | Roster for the weekly check-in settings panel |
| `weekly-checkins.settings.delete` | DELETE | `/api/weekly-checkins/settings` | Remove a member's check-in override |
| `weekly-checkins.settings.list` | GET | `/api/weekly-checkins/settings` | Weekly check-in settings |
| `weekly-checkins.settings.set` | PUT | `/api/weekly-checkins/settings` | Upsert weekly check-in settings |
| `weekly-checkins.update` | PATCH | `/api/weekly-checkins` | Edit and optionally send a draft check-in |

---

### `planning.budget-burn.list`

`GET /api/planning/budget-burn`

List budget burn

### `planning.calibration.list`

`GET /api/planning/calibration`

List calibration

### `planning.critical-path.list`

`GET /api/planning/critical-path`

List critical path

### `planning.dependencies.list`

`GET /api/planning/dependencies`

List dependencies

### `planning.grooming.apply.create`

`POST /api/planning/grooming/apply`

Create apply

Body: application/json (free-form — pass with `--data`)

### `planning.grooming.list`

`GET /api/planning/grooming`

List grooming

### `planning.leveling.apply.create`

`POST /api/planning/leveling/apply`

Create apply

Body: application/json (free-form — pass with `--data`)

### `planning.leveling.list`

`GET /api/planning/leveling`

List leveling

### `planning.scenarios.list`

`GET /api/planning/scenarios`

List scenarios

### `planning.scope-creep.baseline.create`

`POST /api/planning/scope-creep/baseline`

Create baseline

Body: application/json (free-form — pass with `--data`)

### `planning.scope-creep.list`

`GET /api/planning/scope-creep`

List scope creep

### `planning.sprint-planner.create`

`POST /api/planning/sprint-planner`

Create sprint planner

Body: application/json (free-form — pass with `--data`)

### `planning.sprint-planner.list`

`GET /api/planning/sprint-planner`

List sprint planner

### `planning.viable-scope.apply.create`

`POST /api/planning/viable-scope/apply`

Create apply

Body: application/json (free-form — pass with `--data`)

### `planning.viable-scope.list`

`GET /api/planning/viable-scope`

List viable scope

### `weekly-checkins.generate.create`

`POST /api/weekly-checkins/generate`

Generate a draft weekly check-in now

A member may generate their own; admins may generate for any active member. Defaults to the last 7 days. An existing check-in for the same week is returned untouched. Billed to the caller.

Body (application/json):
  - `memberUserId` (string)
  - `weekStart` (string<date>)
  - `weekEnd` (string<date>)

### `weekly-checkins.list`

`GET /api/weekly-checkins`

List weekly check-ins

Admins see every member's check-ins (optionally filtered by member); non-admins see only their own regardless of member. Up to 200 rows.

Query:
  - `member` (string)
  - `status` (string) — one of: `draft`, `scheduled`, `sent`, `skipped`

### `weekly-checkins.members.list`

`GET /api/weekly-checkins/members`

Roster for the weekly check-in settings panel

Admins only. Every active member's user_id, email, full_name and role.

### `weekly-checkins.settings.delete`

`DELETE /api/weekly-checkins/settings`

Remove a member's check-in override

Admins only. The member falls back to the workspace default; the default itself cannot be deleted.

**Destructive** — needs `--yes` against a non-local base URL.

Query:
  - `member` (string, required)

### `weekly-checkins.settings.list`

`GET /api/weekly-checkins/settings`

Weekly check-in settings

Admins only. The workspace default plus every per-member override.

### `weekly-checkins.settings.set`

`PUT /api/weekly-checkins/settings`

Upsert weekly check-in settings

Admins only. memberUserId null targets the workspace default; an id targets that member's override.

Body (application/json):
  - `memberUserId` (string|null)
  - `enabled` (boolean)
  - `mode` (string) — one of: `draft`, `auto`
  - `sendDay` (integer)
  - `sendHour` (integer)
  - `recipientUserIds` (string[])

### `weekly-checkins.update`

`PATCH /api/weekly-checkins`

Edit and optionally send a draft check-in

Only the member who owns the check-in, and only while it is a draft. action send emails it to the chosen recipients (or the workspace admins) about a minute later and marks it sent.

Body (application/json):
  - `id` (string, required)
  - `summaryMd` (string)
  - `recipientUserIds` (string[])
  - `action` (string) — one of: `save`, `send`

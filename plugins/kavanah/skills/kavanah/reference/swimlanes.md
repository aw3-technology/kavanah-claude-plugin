# Swimlanes

4 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `projects.swimlanes.create` | POST | `/api/projects/{id}/swimlanes` | Create a swimlane on a project |
| `projects.swimlanes.list` | GET | `/api/projects/{id}/swimlanes` | List swimlanes on a project |
| `swimlanes.delete` | DELETE | `/api/swimlanes/{id}` | Permanently delete a swimlane |
| `swimlanes.update` | PATCH | `/api/swimlanes/{id}` | Update a swimlane (name, position, color, archived) |

---

### `projects.swimlanes.create`

`POST /api/projects/{id}/swimlanes`

Create a swimlane on a project

Path params (positional, in order):
  - `id`

Body (application/json):
  - `name` (string, required)
  - `position` (integer) — 0-indexed lane position. Omit to append.
  - `color` (string)

### `projects.swimlanes.list`

`GET /api/projects/{id}/swimlanes`

List swimlanes on a project

Path params (positional, in order):
  - `id`

Query:
  - `includeArchived` (string) — Pass "1" to include archived lanes.

### `swimlanes.delete`

`DELETE /api/swimlanes/{id}`

Permanently delete a swimlane

Tasks are not deleted, only the lane assignment is removed.

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `swimlanes.update`

`PATCH /api/swimlanes/{id}`

Update a swimlane (name, position, color, archived)

Path params (positional, in order):
  - `id`

Body (application/json):
  - `name` (string)
  - `position` (integer)
  - `color` (string)
  - `archived` (boolean) — true archives the swimlane (sets archived_at), false restores it.

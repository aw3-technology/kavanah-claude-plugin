# RecurringTasks

4 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `recurring-tasks.create` | POST | `/api/recurring-tasks` | Create a recurring-task generator |
| `recurring-tasks.delete` | DELETE | `/api/recurring-tasks/{id}` | Delete a recurring-task generator |
| `recurring-tasks.list` | GET | `/api/recurring-tasks` | List recurring-task generators for a project |
| `recurring-tasks.set` | PUT | `/api/recurring-tasks/{id}` | Update a recurring-task generator |

---

### `recurring-tasks.create`

`POST /api/recurring-tasks`

Create a recurring-task generator

Body (application/json):
  - `projectRef` (string, required)
  - `templateTaskId` (integer)
  - `title` (string, required)
  - `description` (string)
  - `assignedTo` (string)
  - `priority` (string)
  - `tag` (string)
  - `recurrenceRule` (string, required) — iCal RRULE string
  - `nextDue` (string<date>)
  - `active` (boolean)
  - `stopWhenTaskCompleted` (integer) — Task id whose completion ends the rule — the generator deactivates once that task is completed or deleted. Must be an open task in the workspace.

### `recurring-tasks.delete`

`DELETE /api/recurring-tasks/{id}`

Delete a recurring-task generator

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `recurring-tasks.list`

`GET /api/recurring-tasks`

List recurring-task generators for a project

Query:
  - `projectRef` (string, required)

### `recurring-tasks.set`

`PUT /api/recurring-tasks/{id}`

Update a recurring-task generator

Path params (positional, in order):
  - `id`

Body (application/json):
  - `title` (string)
  - `description` (string)
  - `assignedTo` (string)
  - `priority` (string)
  - `tag` (string)
  - `recurrenceRule` (string)
  - `nextDue` (string<date>)
  - `active` (boolean)
  - `stopWhenTaskCompleted` (integer|null) — Task id whose completion ends the rule; null clears the condition.

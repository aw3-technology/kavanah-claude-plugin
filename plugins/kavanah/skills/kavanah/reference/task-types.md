# Task Types

4 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `task-types.create` | POST | `/api/task-types` | Create task type |
| `task-types.delete` | DELETE | `/api/task-types/{id}` | Delete task type |
| `task-types.list` | GET | `/api/task-types` | List task types |
| `task-types.set` | PUT | `/api/task-types/{id}` | Update task type |

---

### `task-types.create`

`POST /api/task-types`

Create task type

Body: application/json (free-form — pass with `--data`)

### `task-types.delete`

`DELETE /api/task-types/{id}`

Delete task type

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `task-types.list`

`GET /api/task-types`

List task types

### `task-types.set`

`PUT /api/task-types/{id}`

Update task type

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

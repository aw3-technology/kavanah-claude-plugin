# Custom Statuses

10 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `custom-statuses.create` | POST | `/api/custom-statuses` | Create a custom status |
| `custom-statuses.delete` | DELETE | `/api/custom-statuses/{id}` | Delete a custom status |
| `custom-statuses.list` | GET | `/api/custom-statuses` | List custom statuses |
| `custom-statuses.set` | PUT | `/api/custom-statuses/{id}` | Update a custom status |
| `status-required-fields.create` | POST | `/api/status-required-fields` | Create status required field |
| `status-required-fields.delete` | DELETE | `/api/status-required-fields` | Delete status required fields |
| `status-required-fields.list` | GET | `/api/status-required-fields` | List status required fields |
| `task-emojis.create` | POST | `/api/task-emojis` | Add an emoji to the workspace's custom task-emoji palette |
| `task-emojis.delete` | DELETE | `/api/task-emojis` | Remove an emoji from the workspace's custom task-emoji palette |
| `task-emojis.list` | GET | `/api/task-emojis` | List the workspace's custom task-emoji palette |

---

### `custom-statuses.create`

`POST /api/custom-statuses`

Create a custom status

Body: application/json (free-form — pass with `--data`)

### `custom-statuses.delete`

`DELETE /api/custom-statuses/{id}`

Delete a custom status

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `custom-statuses.list`

`GET /api/custom-statuses`

List custom statuses

### `custom-statuses.set`

`PUT /api/custom-statuses/{id}`

Update a custom status

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `status-required-fields.create`

`POST /api/status-required-fields`

Create status required field

Body: application/json (free-form — pass with `--data`)

### `status-required-fields.delete`

`DELETE /api/status-required-fields`

Delete status required fields

**Destructive** — needs `--yes` against a non-local base URL.

### `status-required-fields.list`

`GET /api/status-required-fields`

List status required fields

### `task-emojis.create`

`POST /api/task-emojis`

Add an emoji to the workspace's custom task-emoji palette

Adding an emoji that is already present succeeds and returns alreadyExisted=true, so this is safe to call without checking first.

Body (application/json):
  - `emoji` (string, required) — Exactly one emoji character (ZWJ and skin-tone sequences allowed).
  - `label` (string) — What the emoji means in this workspace.

### `task-emojis.delete`

`DELETE /api/task-emojis`

Remove an emoji from the workspace's custom task-emoji palette

Only stops offering the emoji as a quick pick. Tasks already labelled with it keep it.

**Destructive** — needs `--yes` against a non-local base URL.

Query:
  - `emoji` (string, required)

### `task-emojis.list`

`GET /api/task-emojis`

List the workspace's custom task-emoji palette

The emojis added on top of Kavanah's built-in on-card picker groups. This is a palette, not a constraint — app_tasks.emoji is free-form, so a task can carry any emoji whether or not it appears here.

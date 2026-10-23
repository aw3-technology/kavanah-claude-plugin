# Sprints

5 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `sprints.create` | POST | `/api/sprints` | Create sprint |
| `sprints.delete` | DELETE | `/api/sprints/{id}` | Delete sprint |
| `sprints.get` | GET | `/api/sprints/{id}` | Fetch sprint |
| `sprints.list` | GET | `/api/sprints` | List sprints |
| `sprints.update` | PATCH | `/api/sprints/{id}` | Update sprint |

---

### `sprints.create`

`POST /api/sprints`

Create sprint

Body: application/json (free-form — pass with `--data`)

### `sprints.delete`

`DELETE /api/sprints/{id}`

Delete sprint

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `sprints.get`

`GET /api/sprints/{id}`

Fetch sprint

Path params (positional, in order):
  - `id`

### `sprints.list`

`GET /api/sprints`

List sprints

### `sprints.update`

`PATCH /api/sprints/{id}`

Update sprint

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

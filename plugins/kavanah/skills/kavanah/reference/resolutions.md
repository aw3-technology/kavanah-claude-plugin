# Resolutions

4 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `resolutions.create` | POST | `/api/resolutions` | Create resolution |
| `resolutions.delete` | DELETE | `/api/resolutions/{id}` | Delete resolution |
| `resolutions.list` | GET | `/api/resolutions` | List resolutions |
| `resolutions.set` | PUT | `/api/resolutions/{id}` | Update resolution |

---

### `resolutions.create`

`POST /api/resolutions`

Create resolution

Body: application/json (free-form — pass with `--data`)

### `resolutions.delete`

`DELETE /api/resolutions/{id}`

Delete resolution

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `resolutions.list`

`GET /api/resolutions`

List resolutions

### `resolutions.set`

`PUT /api/resolutions/{id}`

Update resolution

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

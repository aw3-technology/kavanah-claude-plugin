# Versions

4 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `versions.create` | POST | `/api/versions` | Create version |
| `versions.delete` | DELETE | `/api/versions/{id}` | Delete version |
| `versions.list` | GET | `/api/versions` | List versions |
| `versions.set` | PUT | `/api/versions/{id}` | Update version |

---

### `versions.create`

`POST /api/versions`

Create version

Body: application/json (free-form — pass with `--data`)

### `versions.delete`

`DELETE /api/versions/{id}`

Delete version

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `versions.list`

`GET /api/versions`

List versions

### `versions.set`

`PUT /api/versions/{id}`

Update version

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

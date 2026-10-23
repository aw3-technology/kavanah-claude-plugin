# Components

4 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `components.create` | POST | `/api/components` | Create component |
| `components.delete` | DELETE | `/api/components/{id}` | Delete component |
| `components.list` | GET | `/api/components` | List components |
| `components.set` | PUT | `/api/components/{id}` | Update component |

---

### `components.create`

`POST /api/components`

Create component

Body: application/json (free-form — pass with `--data`)

### `components.delete`

`DELETE /api/components/{id}`

Delete component

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `components.list`

`GET /api/components`

List components

### `components.set`

`PUT /api/components/{id}`

Update component

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

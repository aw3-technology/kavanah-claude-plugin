# Custom Fields

4 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `custom-fields.create` | POST | `/api/custom-fields` | Create custom field |
| `custom-fields.delete` | DELETE | `/api/custom-fields/{id}` | Delete custom field |
| `custom-fields.list` | GET | `/api/custom-fields` | List custom fields |
| `custom-fields.set` | PUT | `/api/custom-fields/{id}` | Update custom field |

---

### `custom-fields.create`

`POST /api/custom-fields`

Create custom field

Body: application/json (free-form — pass with `--data`)

### `custom-fields.delete`

`DELETE /api/custom-fields/{id}`

Delete custom field

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `custom-fields.list`

`GET /api/custom-fields`

List custom fields

### `custom-fields.set`

`PUT /api/custom-fields/{id}`

Update custom field

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

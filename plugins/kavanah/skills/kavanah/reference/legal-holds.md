# Legal Holds

3 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `legal-holds.create` | POST | `/api/legal-holds` | Create legal hold |
| `legal-holds.delete` | DELETE | `/api/legal-holds/{id}` | Delete legal hold |
| `legal-holds.list` | GET | `/api/legal-holds` | List legal holds |

---

### `legal-holds.create`

`POST /api/legal-holds`

Create legal hold

Body: application/json (free-form — pass with `--data`)

### `legal-holds.delete`

`DELETE /api/legal-holds/{id}`

Delete legal hold

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `legal-holds.list`

`GET /api/legal-holds`

List legal holds

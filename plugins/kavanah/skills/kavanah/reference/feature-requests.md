# Feature requests

4 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `feature-requests.create` | POST | `/api/feature-requests` | Submit a feature request |
| `feature-requests.list` | GET | `/api/feature-requests` | List the public feature-request board plus the caller's own submissions |
| `feature-requests.vote.create` | POST | `/api/feature-requests/{p1}/vote` | (undocumented route — params unknown, pass them explicitly) |
| `feature-requests.vote.delete` | DELETE | `/api/feature-requests/{p1}/vote` | (undocumented route — params unknown, pass them explicitly) |

---

### `feature-requests.create`

`POST /api/feature-requests`

Submit a feature request

### `feature-requests.list`

`GET /api/feature-requests`

List the public feature-request board plus the caller's own submissions

Optional query params: status (active|all), category, search, limit (max 200).

### `feature-requests.vote.create`

`POST /api/feature-requests/{p1}/vote`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `feature-requests.vote.delete`

`DELETE /api/feature-requests/{p1}/vote`

(undocumented route — params unknown, pass them explicitly)

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

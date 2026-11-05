# Feature requests

4 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `feature-requests.create` | POST | `/api/feature-requests` | Submit a feature request |
| `feature-requests.list` | GET | `/api/feature-requests` | List the public feature-request board plus the caller's own submissions |
| `feature-requests.vote.create` | POST | `/api/feature-requests/{id}/vote` | Upvote a feature request |
| `feature-requests.vote.delete` | DELETE | `/api/feature-requests/{id}/vote` | Withdraw an upvote |

---

### `feature-requests.create`

`POST /api/feature-requests`

Submit a feature request

### `feature-requests.list`

`GET /api/feature-requests`

List the public feature-request board plus the caller's own submissions

Optional query params: status (active|all), category, search, limit (max 200).

### `feature-requests.vote.create`

`POST /api/feature-requests/{id}/vote`

Upvote a feature request

Signed-in users. Idempotent; voting again returns the current count unchanged.

Path params (positional, in order):
  - `id`

### `feature-requests.vote.delete`

`DELETE /api/feature-requests/{id}/vote`

Withdraw an upvote

Signed-in users. Idempotent; withdrawing a vote that does not exist returns the current count.

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

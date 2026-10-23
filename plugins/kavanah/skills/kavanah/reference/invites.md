# Invites

5 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `invites.accept.create` | POST | `/api/invites/{token}/accept` | Create accept |
| `invites.decline.create` | POST | `/api/invites/{token}/decline` | Create decline |
| `invites.get` | GET | `/api/invites/{token}` | Fetch invite |
| `invites.mine.list` | GET | `/api/invites/mine` | List mine |
| `invites.request-resend.create` | POST | `/api/invites/{token}/request-resend` | Create request resend |

---

### `invites.accept.create`

`POST /api/invites/{token}/accept`

Create accept

Path params (positional, in order):
  - `token`

Body: application/json (free-form — pass with `--data`)

### `invites.decline.create`

`POST /api/invites/{token}/decline`

Create decline

Path params (positional, in order):
  - `token`

Body: application/json (free-form — pass with `--data`)

### `invites.get`

`GET /api/invites/{token}`

Fetch invite

Path params (positional, in order):
  - `token`

### `invites.mine.list`

`GET /api/invites/mine`

List mine

### `invites.request-resend.create`

`POST /api/invites/{token}/request-resend`

Create request resend

Path params (positional, in order):
  - `token`

Body: application/json (free-form — pass with `--data`)

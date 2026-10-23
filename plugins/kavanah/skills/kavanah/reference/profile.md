# Profile

10 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `profile.emails.create` | POST | `/api/profile/emails` | (undocumented route — params unknown, pass them explicitly) |
| `profile.emails.delete` | DELETE | `/api/profile/emails/{p1}` | (undocumented route — params unknown, pass them explicitly) |
| `profile.emails.list` | GET | `/api/profile/emails` | (undocumented route — params unknown, pass them explicitly) |
| `profile.emails.promote.create` | POST | `/api/profile/emails/{p1}/promote` | (undocumented route — params unknown, pass them explicitly) |
| `profile.emails.resend.create` | POST | `/api/profile/emails/{p1}/resend` | (undocumented route — params unknown, pass them explicitly) |
| `profile.handle.list` | GET | `/api/profile/handle` | (undocumented route — params unknown, pass them explicitly) |
| `profile.handle.set` | PUT | `/api/profile/handle` | (undocumented route — params unknown, pass them explicitly) |
| `profile.list` | GET | `/api/profile` | Get current user profile |
| `profile.timezone.create` | POST | `/api/profile/timezone` | (undocumented route — params unknown, pass them explicitly) |
| `profile.update` | PATCH | `/api/profile` | Update user profile |

---

### `profile.emails.create`

`POST /api/profile/emails`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `profile.emails.delete`

`DELETE /api/profile/emails/{p1}`

(undocumented route — params unknown, pass them explicitly)

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `profile.emails.list`

`GET /api/profile/emails`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `profile.emails.promote.create`

`POST /api/profile/emails/{p1}/promote`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `profile.emails.resend.create`

`POST /api/profile/emails/{p1}/resend`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `profile.handle.list`

`GET /api/profile/handle`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `profile.handle.set`

`PUT /api/profile/handle`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `profile.list`

`GET /api/profile`

Get current user profile

### `profile.timezone.create`

`POST /api/profile/timezone`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `profile.update`

`PATCH /api/profile`

Update user profile

Body (application/json):
  - `firstName` (string)
  - `lastName` (string)
  - `fullName` (string)
  - `email` (string<email>)
  - `phone` (string)
  - `jobTitle` (string)
  - `department` (string)
  - `bio` (string)
  - `avatarTone` (string)

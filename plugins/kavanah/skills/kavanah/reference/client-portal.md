# Client Portal

9 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `portal.auth.accept-invite.create` | POST | `/api/portal/auth/accept-invite` | Create accept invite |
| `portal.auth.login.create` | POST | `/api/portal/auth/login` | Create login |
| `portal.auth.logout.create` | POST | `/api/portal/auth/logout` | Create logout |
| `portal.decisions.create` | POST | `/api/portal/decisions` | Create decision |
| `portal.decisions.list` | GET | `/api/portal/decisions` | List decisions |
| `portal.discussions.create` | POST | `/api/portal/discussions` | Create discussion |
| `portal.export.list` | GET | `/api/portal/export` | List export |
| `portal.files.create` | POST | `/api/portal/files` | Create file |
| `portal.files.get` | GET | `/api/portal/files/{fileId}` | Fetch file |

---

### `portal.auth.accept-invite.create`

`POST /api/portal/auth/accept-invite`

Create accept invite

Body: application/json (free-form — pass with `--data`)

### `portal.auth.login.create`

`POST /api/portal/auth/login`

Create login

Body: application/json (free-form — pass with `--data`)

### `portal.auth.logout.create`

`POST /api/portal/auth/logout`

Create logout

Body: application/json (free-form — pass with `--data`)

### `portal.decisions.create`

`POST /api/portal/decisions`

Create decision

Body: application/json (free-form — pass with `--data`)

### `portal.decisions.list`

`GET /api/portal/decisions`

List decisions

### `portal.discussions.create`

`POST /api/portal/discussions`

Create discussion

Body: application/json (free-form — pass with `--data`)

### `portal.export.list`

`GET /api/portal/export`

List export

### `portal.files.create`

`POST /api/portal/files`

Create file

Body: application/json (free-form — pass with `--data`)

### `portal.files.get`

`GET /api/portal/files/{fileId}`

Fetch file

Path params (positional, in order):
  - `fileId`

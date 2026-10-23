# System

8 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `app-config.public.list` | GET | `/api/app-config/public` | List public |
| `company-logo.list` | GET | `/api/company-logo` | List company logo |
| `company-preview.list` | GET | `/api/company-preview` | List company preview |
| `system.health.list` | GET | `/api/system/health` | List health |
| `undo.create` | POST | `/api/undo` | Create undo |
| `undo.list` | GET | `/api/undo` | List undo |
| `undo.redo.create` | POST | `/api/undo/redo` | Create redo |
| `uploads.get` | GET | `/api/uploads/{path}` | Fetch upload |

---

### `app-config.public.list`

`GET /api/app-config/public`

List public

### `company-logo.list`

`GET /api/company-logo`

List company logo

### `company-preview.list`

`GET /api/company-preview`

List company preview

### `system.health.list`

`GET /api/system/health`

List health

### `undo.create`

`POST /api/undo`

Create undo

Body: application/json (free-form — pass with `--data`)

### `undo.list`

`GET /api/undo`

List undo

### `undo.redo.create`

`POST /api/undo/redo`

Create redo

Body: application/json (free-form — pass with `--data`)

### `uploads.get`

`GET /api/uploads/{path}`

Fetch upload

Path params (positional, in order):
  - `path`

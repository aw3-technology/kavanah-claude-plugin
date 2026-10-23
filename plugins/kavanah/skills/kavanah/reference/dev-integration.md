# Dev Integration

3 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `dev.list` | GET | `/api/dev` | List dev |
| `dev.repos.create` | POST | `/api/dev/repos` | Create repo |
| `dev.repos.list` | GET | `/api/dev/repos` | List repos |

---

### `dev.list`

`GET /api/dev`

List dev

### `dev.repos.create`

`POST /api/dev/repos`

Create repo

Body: application/json (free-form — pass with `--data`)

### `dev.repos.list`

`GET /api/dev/repos`

List repos

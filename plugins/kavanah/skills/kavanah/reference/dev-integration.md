# Dev Integration

4 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `dev.count.list` | GET | `/api/dev/count` | Sidebar badge count of PRs awaiting the caller's review |
| `dev.list` | GET | `/api/dev` | List dev |
| `dev.repos.create` | POST | `/api/dev/repos` | Create repo |
| `dev.repos.list` | GET | `/api/dev/repos` | List repos |

---

### `dev.count.list`

`GET /api/dev/count`

Sidebar badge count of PRs awaiting the caller's review

Signed-in users. Counts open pull requests awaiting the caller's review across every workspace they are an active member of (cross-workspace by design, to match the app badge). Private cache of 30s with stale-while-revalidate.

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

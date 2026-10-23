# Board

3 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `projects.column-limits.delete` | DELETE | `/api/projects/{id}/column-limits` | Remove the WIP limit and name override for one status |
| `projects.column-limits.list` | GET | `/api/projects/{id}/column-limits` | List per-column WIP limits and current open-task counts |
| `projects.column-limits.set` | PUT | `/api/projects/{id}/column-limits` | Upsert a WIP limit and/or column-name override for one status |

---

### `projects.column-limits.delete`

`DELETE /api/projects/{id}/column-limits`

Remove the WIP limit and name override for one status

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `statusId` (string, required)

### `projects.column-limits.list`

`GET /api/projects/{id}/column-limits`

List per-column WIP limits and current open-task counts

Path params (positional, in order):
  - `id`

### `projects.column-limits.set`

`PUT /api/projects/{id}/column-limits`

Upsert a WIP limit and/or column-name override for one status

Path params (positional, in order):
  - `id`

Body (application/json):
  - `statusId` (string, required)
  - `wipLimit` (integer) — null clears the cap but keeps the row (for nameOverride).
  - `nameOverride` (string)

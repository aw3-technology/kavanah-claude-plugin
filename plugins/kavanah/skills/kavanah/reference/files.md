# Files

4 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `project-files.create` | POST | `/api/project-files` | Upload files to a project |
| `project-files.delete` | DELETE | `/api/project-files` | Delete a project file |
| `project-files.list` | GET | `/api/project-files` | List project files |
| `project-files.update` | PATCH | `/api/project-files` | Rename or duplicate a file |

---

### `project-files.create`

`POST /api/project-files`

Upload files to a project

Body (multipart/form-data):
  - `projectRef` (string, required)
  - `documentId` (string)
  - `files` (string<binary>[], required)

### `project-files.delete`

`DELETE /api/project-files`

Delete a project file

**Destructive** — needs `--yes` against a non-local base URL.

Body (application/json):
  - `projectRef` (string, required)
  - `fileId` (string, required)

### `project-files.list`

`GET /api/project-files`

List project files

Query:
  - `projectRef` (string, required)

### `project-files.update`

`PATCH /api/project-files`

Rename or duplicate a file

Body (application/json):
  - `action` (string, required) — one of: `rename`, `duplicate`
  - `projectRef` (string, required)
  - `fileId` (string, required)
  - `name` (string)

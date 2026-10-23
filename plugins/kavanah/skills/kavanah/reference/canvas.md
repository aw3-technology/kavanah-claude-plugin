# Canvas

10 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `mindmaps.create` | POST | `/api/mindmaps` | Create a mind map |
| `mindmaps.delete` | DELETE | `/api/mindmaps/{id}` | Delete a mind map |
| `mindmaps.get` | GET | `/api/mindmaps/{id}` | Get a mind map |
| `mindmaps.list` | GET | `/api/mindmaps` | List mind maps in the workspace |
| `mindmaps.update` | PATCH | `/api/mindmaps/{id}` | Rename a mind map or save its graph |
| `whiteboards.create` | POST | `/api/whiteboards` | Create a whiteboard |
| `whiteboards.delete` | DELETE | `/api/whiteboards/{id}` | Delete a whiteboard |
| `whiteboards.get` | GET | `/api/whiteboards/{id}` | Get a whiteboard |
| `whiteboards.list` | GET | `/api/whiteboards` | List whiteboards in the workspace |
| `whiteboards.update` | PATCH | `/api/whiteboards/{id}` | Rename a whiteboard or save its scene |

---

### `mindmaps.create`

`POST /api/mindmaps`

Create a mind map

Body (application/json):
  - `title` (string)
  - `projectRef` (string)
  - `graph` (object) — { nodes, edges } graph (capped at 3 MB).

### `mindmaps.delete`

`DELETE /api/mindmaps/{id}`

Delete a mind map

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `mindmaps.get`

`GET /api/mindmaps/{id}`

Get a mind map

Path params (positional, in order):
  - `id`

### `mindmaps.list`

`GET /api/mindmaps`

List mind maps in the workspace

### `mindmaps.update`

`PATCH /api/mindmaps/{id}`

Rename a mind map or save its graph

Rename-only when `graph` is omitted and `title` is present; otherwise saves the graph with an optional optimistic-lock guard (`expectedUpdatedAt`).

Path params (positional, in order):
  - `id`

Body (application/json):
  - `title` (string)
  - `graph` (object)
  - `expectedUpdatedAt` (string)

### `whiteboards.create`

`POST /api/whiteboards`

Create a whiteboard

Body (application/json):
  - `title` (string)
  - `projectRef` (string)
  - `scene` (object) — Serialized Excalidraw scene (capped at 5 MB).
  - `thumbnail` (string)

### `whiteboards.delete`

`DELETE /api/whiteboards/{id}`

Delete a whiteboard

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `whiteboards.get`

`GET /api/whiteboards/{id}`

Get a whiteboard

Path params (positional, in order):
  - `id`

### `whiteboards.list`

`GET /api/whiteboards`

List whiteboards in the workspace

### `whiteboards.update`

`PATCH /api/whiteboards/{id}`

Rename a whiteboard or save its scene

Rename-only when `scene` is omitted and `title` is present; otherwise saves the scene with an optional optimistic-lock guard (`expectedUpdatedAt`).

Path params (positional, in order):
  - `id`

Body (application/json):
  - `title` (string)
  - `scene` (object)
  - `thumbnail` (string)
  - `expectedUpdatedAt` (string)

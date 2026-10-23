# Discussions

5 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `discussions.agent-reply.create` | POST | `/api/discussions/agent-reply` | Answer an @agent question in a discussion |
| `discussions.create` | POST | `/api/discussions` | Create a thread or reply (multipart form or JSON) |
| `discussions.delete` | DELETE | `/api/discussions` | Delete a thread or reply |
| `discussions.list` | GET | `/api/discussions` | Get discussions for a project |
| `discussions.update` | PATCH | `/api/discussions` | Toggle star or add reaction |

---

### `discussions.agent-reply.create`

`POST /api/discussions/agent-reply`

Answer an @agent question in a discussion

Generates the AI agent's answer to a stored thread or reply and posts it as the agent. Idempotent per question. The reply notifies nobody.

Body (application/json):
  - `projectRef` (string, required)
  - `threadId` (string, required)
  - `replyId` (string) — The reply that mentions @agent; omit for the opening post.

### `discussions.create`

`POST /api/discussions`

Create a thread or reply (multipart form or JSON)

Use multipart/form-data to attach files; application/json is accepted for text-only posts. When `mode` is omitted it is inferred: a body carrying `threadId` is a reply, one carrying `title` is a new thread.

Body (multipart/form-data):
  - `mode` (string) — one of: `thread`, `reply`
  - `projectRef` (string, required)
  - `title` (string)
  - `body` (string)
  - `threadId` (string)
  - `content` (string)
  - `authorName` (string)
  - `authorInitials` (string)
  - `authorTone` (string)

### `discussions.delete`

`DELETE /api/discussions`

Delete a thread or reply

**Destructive** — needs `--yes` against a non-local base URL.

Body (application/json):
  - `projectRef` (string, required)
  - `targetType` (string, required) — one of: `thread`, `reply`
  - `targetId` (string, required)

### `discussions.list`

`GET /api/discussions`

Get discussions for a project

Query:
  - `projectRef` (string, required)

### `discussions.update`

`PATCH /api/discussions`

Toggle star or add reaction

Body (application/json):
  - `action` (string) — one of: `toggle-star`, `add-reaction`
  - `projectRef` (string)
  - `threadId` (string)
  - `starred` (boolean)
  - `targetType` (string) — one of: `thread`, `reply`
  - `targetId` (string)
  - `emoji` (string)

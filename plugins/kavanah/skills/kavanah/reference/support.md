# Support

4 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `contact.create` | POST | `/api/contact` | Create contact |
| `support.tickets.create` | POST | `/api/support/tickets` | File a support ticket |
| `support.tickets.list` | GET | `/api/support/tickets` | List support tickets |
| `support.tickets.update` | PATCH | `/api/support/tickets/{ticketId}` | Update a ticket's status and/or resolution note (admin/owner only) |

---

### `contact.create`

`POST /api/contact`

Create contact

Body: application/json (free-form — pass with `--data`)

### `support.tickets.create`

`POST /api/support/tickets`

File a support ticket

Body (application/json):
  - `subject` (string, required)
  - `description` (string, required)
  - `category` (string) — one of: `bug`, `feature`, `question`, `billing`, `general`
  - `priority` (string) — one of: `low`, `medium`, `high`, `urgent`
  - `diagnostics` (object)
  - `bug` (object) — Optional structured half of a bug report (category bug only). Folded into the description server-side; non-string values are ignored.
  - `bug.reproductionSteps` (string)
  - `bug.expectedBehavior` (string)
  - `bug.actualBehavior` (string)

### `support.tickets.list`

`GET /api/support/tickets`

List support tickets

A non-admin asking for scope=workspace is answered with their own tickets and scope=mine in the body — read `scope` to know which list you got.

Query:
  - `scope` (string) — one of: `mine`, `workspace`
  - `category` (string) — one of: `bug`, `feature`, `question`, `billing`, `general`
  - `limit` (integer) — Max rows (default 50 for mine, 100 for workspace; max 200)
  - `before` (string) — Keyset cursor (the previous page's nextCursor) — workspace scope only.

### `support.tickets.update`

`PATCH /api/support/tickets/{ticketId}`

Update a ticket's status and/or resolution note (admin/owner only)

When the status moves to in-progress, resolved or closed, or a new note is written, the reporter (if not the caller) is emailed and pushed.

Path params (positional, in order):
  - `ticketId`

Body (application/json):
  - `status` (string) — one of: `open`, `in-progress`, `resolved`, `closed`
  - `resolutionNote` (string) — What was done to resolve the ticket — shown to the reporter. Pass null to clear.

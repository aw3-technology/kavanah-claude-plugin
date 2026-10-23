# Requests

13 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `r.submit.create` | POST | `/api/r/{token}/submit` | Submit a public intake request against a link token |
| `r.verify.list` | GET | `/api/r/verify` | Confirm a public request submission via emailed token (returns an HTML page) |
| `requests.count.list` | GET | `/api/requests/count` | Get the count of open intake requests (for nav badges) |
| `requests.create` | POST | `/api/requests` | Convert an intake request into a task |
| `requests.list` | GET | `/api/requests` | List intake requests for the workspace (members see their own; admins see all) |
| `requests.pages.create` | POST | `/api/requests/pages` | Create a request intake link |
| `requests.pages.delete` | DELETE | `/api/requests/pages` | Delete a request intake link |
| `requests.pages.fields.list` | GET | `/api/requests/pages/{id}/fields` | List the custom fields for a request intake link |
| `requests.pages.fields.set` | PUT | `/api/requests/pages/{id}/fields` | Replace the custom fields for a request intake link |
| `requests.pages.list` | GET | `/api/requests/pages` | List request intake links (pages) |
| `requests.pages.update` | PATCH | `/api/requests/pages` | Update a request intake link |
| `requests.sla.list` | GET | `/api/requests/sla` | (undocumented route — params unknown, pass them explicitly) |
| `requests.update` | PATCH | `/api/requests` | Update the status of an intake request |

---

### `r.submit.create`

`POST /api/r/{token}/submit`

Submit a public intake request against a link token

Public, unauthenticated (rate limited). Accepts JSON or multipart form data with `subject`, `body`, requester identity, and any custom fields. Links in `clients_only` mode require a portal session.

Path params (positional, in order):
  - `token`

Body (multipart/form-data):
  - `subject` (string, required)
  - `body` (string, required)
  - `name` (string)
  - `email` (string)

### `r.verify.list`

`GET /api/r/verify`

Confirm a public request submission via emailed token (returns an HTML page)

Public, unauthenticated. Consumes a one-time verification token and finalizes the submission.

Query:
  - `token` (string, required)

### `requests.count.list`

`GET /api/requests/count`

Get the count of open intake requests (for nav badges)

### `requests.create`

`POST /api/requests`

Convert an intake request into a task

Body (application/json):
  - `id` (string, required)
  - `projectRef` (string, required)
  - `assignedTo` (string)

### `requests.list`

`GET /api/requests`

List intake requests for the workspace (members see their own; admins see all)

### `requests.pages.create`

`POST /api/requests/pages`

Create a request intake link

Body (application/json):
  - `title` (string, required)
  - `description` (string)
  - `accessMode` (string) — one of: `public`, `clients_only`
  - `scope` (string) — one of: `user`, `workspace`

### `requests.pages.delete`

`DELETE /api/requests/pages`

Delete a request intake link

**Destructive** — needs `--yes` against a non-local base URL.

Query:
  - `id` (string, required)

### `requests.pages.fields.list`

`GET /api/requests/pages/{id}/fields`

List the custom fields for a request intake link

Path params (positional, in order):
  - `id`

### `requests.pages.fields.set`

`PUT /api/requests/pages/{id}/fields`

Replace the custom fields for a request intake link

Path params (positional, in order):
  - `id`

Body (application/json):
  - `fields` (object[], required)

### `requests.pages.list`

`GET /api/requests/pages`

List request intake links (pages)

### `requests.pages.update`

`PATCH /api/requests/pages`

Update a request intake link

Body (application/json):
  - `id` (string, required)
  - `title` (string)
  - `description` (string)
  - `accessMode` (string) — one of: `public`, `clients_only`
  - `isActive` (boolean)

### `requests.sla.list`

`GET /api/requests/sla`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `requests.update`

`PATCH /api/requests`

Update the status of an intake request

Body (application/json):
  - `id` (string, required)
  - `status` (string, required)

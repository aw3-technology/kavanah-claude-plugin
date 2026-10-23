# Data Governance

20 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `data-governance.consent.create` | POST | `/api/data-governance/consent` | Create consent |
| `data-governance.consent.list` | GET | `/api/data-governance/consent` | List consent |
| `data-governance.cookie-consent.create` | POST | `/api/data-governance/cookie-consent` | Create cookie consent |
| `data-governance.cookie-consent.list` | GET | `/api/data-governance/cookie-consent` | List cookie consent |
| `data-governance.data-requests.create` | POST | `/api/data-governance/data-requests` | Create data request |
| `data-governance.data-requests.list` | GET | `/api/data-governance/data-requests` | List data requests |
| `data-governance.data-requests.update` | PATCH | `/api/data-governance/data-requests/{requestId}` | Update data request |
| `data-governance.dpa.create` | POST | `/api/data-governance/dpa` | Create dpa |
| `data-governance.dpa.list` | GET | `/api/data-governance/dpa` | List dpa |
| `data-governance.gdpr.delete.delete` | DELETE | `/api/data-governance/gdpr/delete` | Delete delete |
| `data-governance.gdpr.export.list` | GET | `/api/data-governance/gdpr/export` | List export |
| `data-governance.legal.accept.create` | POST | `/api/data-governance/legal/accept` | Create accept |
| `data-governance.legal.create` | POST | `/api/data-governance/legal` | Create legal |
| `data-governance.legal.list` | GET | `/api/data-governance/legal` | List legal |
| `data-governance.pii.create` | POST | `/api/data-governance/pii` | Create pii |
| `data-governance.pii.list` | GET | `/api/data-governance/pii` | List pii |
| `data-governance.privacy-notice.create` | POST | `/api/data-governance/privacy-notice` | Create privacy notice |
| `data-governance.privacy-notice.list` | GET | `/api/data-governance/privacy-notice` | List privacy notice |
| `data-governance.workspace-export.list` | GET | `/api/data-governance/workspace-export` | Export the entire workspace as a JSON archive |
| `trust.requests.create` | POST | `/api/trust/requests` | Create request |

---

### `data-governance.consent.create`

`POST /api/data-governance/consent`

Create consent

Body: application/json (free-form — pass with `--data`)

### `data-governance.consent.list`

`GET /api/data-governance/consent`

List consent

### `data-governance.cookie-consent.create`

`POST /api/data-governance/cookie-consent`

Create cookie consent

Body: application/json (free-form — pass with `--data`)

### `data-governance.cookie-consent.list`

`GET /api/data-governance/cookie-consent`

List cookie consent

### `data-governance.data-requests.create`

`POST /api/data-governance/data-requests`

Create data request

Body: application/json (free-form — pass with `--data`)

### `data-governance.data-requests.list`

`GET /api/data-governance/data-requests`

List data requests

### `data-governance.data-requests.update`

`PATCH /api/data-governance/data-requests/{requestId}`

Update data request

Path params (positional, in order):
  - `requestId`

Body: application/json (free-form — pass with `--data`)

### `data-governance.dpa.create`

`POST /api/data-governance/dpa`

Create dpa

Body: application/json (free-form — pass with `--data`)

### `data-governance.dpa.list`

`GET /api/data-governance/dpa`

List dpa

### `data-governance.gdpr.delete.delete`

`DELETE /api/data-governance/gdpr/delete`

Delete delete

**Destructive** — needs `--yes` against a non-local base URL.

### `data-governance.gdpr.export.list`

`GET /api/data-governance/gdpr/export`

List export

**Destructive** — needs `--yes` against a non-local base URL.

### `data-governance.legal.accept.create`

`POST /api/data-governance/legal/accept`

Create accept

Body: application/json (free-form — pass with `--data`)

### `data-governance.legal.create`

`POST /api/data-governance/legal`

Create legal

Body: application/json (free-form — pass with `--data`)

### `data-governance.legal.list`

`GET /api/data-governance/legal`

List legal

### `data-governance.pii.create`

`POST /api/data-governance/pii`

Create pii

Body: application/json (free-form — pass with `--data`)

### `data-governance.pii.list`

`GET /api/data-governance/pii`

List pii

### `data-governance.privacy-notice.create`

`POST /api/data-governance/privacy-notice`

Create privacy notice

Body: application/json (free-form — pass with `--data`)

### `data-governance.privacy-notice.list`

`GET /api/data-governance/privacy-notice`

List privacy notice

### `data-governance.workspace-export.list`

`GET /api/data-governance/workspace-export`

Export the entire workspace as a JSON archive

Admin/owner only. Reads across every workspace table, so it is rate limited to 5 requests per hour.

Query:
  - `files` (string) — one of: `none`, `metadata`, `full`

### `trust.requests.create`

`POST /api/trust/requests`

Create request

Body: application/json (free-form — pass with `--data`)

# Audit Logs

22 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `audit-logs.alerts.create` | POST | `/api/audit-logs/alerts` | Create alert |
| `audit-logs.alerts.delete` | DELETE | `/api/audit-logs/alerts` | Delete alerts |
| `audit-logs.alerts.list` | GET | `/api/audit-logs/alerts` | List alerts |
| `audit-logs.alerts.update` | PATCH | `/api/audit-logs/alerts` | Update alerts |
| `audit-logs.archiving.angelsend-sync.create` | POST | `/api/audit-logs/archiving/angelsend-sync` | Re-sync members' AngelSend archive |
| `audit-logs.archiving.deliver.create` | POST | `/api/audit-logs/archiving/deliver` | Deliver the compliance journal now |
| `audit-logs.archiving.list` | GET | `/api/audit-logs/archiving` | Get compliance archiving settings and health |
| `audit-logs.archiving.test.create` | POST | `/api/audit-logs/archiving/test` | Send a test message to the archive address |
| `audit-logs.archiving.update` | PATCH | `/api/audit-logs/archiving` | Update compliance archiving |
| `audit-logs.compliance.list` | GET | `/api/audit-logs/compliance` | List compliance |
| `audit-logs.data-access.list` | GET | `/api/audit-logs/data-access` | List data access |
| `audit-logs.event-config.create` | POST | `/api/audit-logs/event-config` | Create event config |
| `audit-logs.event-config.list` | GET | `/api/audit-logs/event-config` | List event config |
| `audit-logs.export.list` | GET | `/api/audit-logs/export` | List export |
| `audit-logs.list` | GET | `/api/audit-logs` | List audit logs |
| `audit-logs.retention.create` | POST | `/api/audit-logs/retention` | Create retention |
| `audit-logs.retention.list` | GET | `/api/audit-logs/retention` | List retention |
| `audit-logs.search.list` | GET | `/api/audit-logs/search` | List search |
| `audit-logs.webhooks.create` | POST | `/api/audit-logs/webhooks` | Create webhook |
| `audit-logs.webhooks.delete` | DELETE | `/api/audit-logs/webhooks` | Delete webhooks |
| `audit-logs.webhooks.list` | GET | `/api/audit-logs/webhooks` | List webhooks |
| `audit-logs.webhooks.update` | PATCH | `/api/audit-logs/webhooks` | Update webhooks |

---

### `audit-logs.alerts.create`

`POST /api/audit-logs/alerts`

Create alert

Body: application/json (free-form — pass with `--data`)

### `audit-logs.alerts.delete`

`DELETE /api/audit-logs/alerts`

Delete alerts

**Destructive** — needs `--yes` against a non-local base URL.

### `audit-logs.alerts.list`

`GET /api/audit-logs/alerts`

List alerts

### `audit-logs.alerts.update`

`PATCH /api/audit-logs/alerts`

Update alerts

Body: application/json (free-form — pass with `--data`)

### `audit-logs.archiving.angelsend-sync.create`

`POST /api/audit-logs/archiving/angelsend-sync`

Re-sync members' AngelSend archive

Point every member's AngelSend projects at the workspace archive address now (or clear the address Kavanah set when compliance mode is off). Never overwrites an address someone else set. Workspace owner only.

**Destructive** — needs `--yes` against a non-local base URL.

### `audit-logs.archiving.deliver.create`

`POST /api/audit-logs/archiving/deliver`

Deliver the compliance journal now

Send pending compliance journal entries to the archive address without waiting for the daily digest. Never re-sends delivered entries.

**Destructive** — needs `--yes` against a non-local base URL.

### `audit-logs.archiving.list`

`GET /api/audit-logs/archiving`

Get compliance archiving settings and health

The workspace archive (journal) address, compliance mode, retention period, the compliance journal backlog, recent digest deliveries to the archive, and each member's AngelSend archive state. Owners and admins.

### `audit-logs.archiving.test.create`

`POST /api/audit-logs/archiving/test`

Send a test message to the archive address

### `audit-logs.archiving.update`

`PATCH /api/audit-logs/archiving`

Update compliance archiving

Set the archive address (`archiveAddress`, one mailbox or null), compliance mode (`enabled`) and retention (`retentionDays`, 365-3650). With compliance mode on, every outbound email carries the archive BCC and cannot skip it, and chat, client-portal, discussion, task-comment, in-call, transcript and agent communications are journaled and delivered to the archive as a daily digest. Workspace owner only; audited.

**Destructive** — needs `--yes` against a non-local base URL.

Body (application/json):
  - `archiveAddress` (string|null)
  - `enabled` (boolean)
  - `retentionDays` (integer)

### `audit-logs.compliance.list`

`GET /api/audit-logs/compliance`

List compliance

### `audit-logs.data-access.list`

`GET /api/audit-logs/data-access`

List data access

### `audit-logs.event-config.create`

`POST /api/audit-logs/event-config`

Create event config

Body: application/json (free-form — pass with `--data`)

### `audit-logs.event-config.list`

`GET /api/audit-logs/event-config`

List event config

### `audit-logs.export.list`

`GET /api/audit-logs/export`

List export

### `audit-logs.list`

`GET /api/audit-logs`

List audit logs

### `audit-logs.retention.create`

`POST /api/audit-logs/retention`

Create retention

Body: application/json (free-form — pass with `--data`)

### `audit-logs.retention.list`

`GET /api/audit-logs/retention`

List retention

### `audit-logs.search.list`

`GET /api/audit-logs/search`

List search

### `audit-logs.webhooks.create`

`POST /api/audit-logs/webhooks`

Create webhook

Body: application/json (free-form — pass with `--data`)

### `audit-logs.webhooks.delete`

`DELETE /api/audit-logs/webhooks`

Delete webhooks

**Destructive** — needs `--yes` against a non-local base URL.

### `audit-logs.webhooks.list`

`GET /api/audit-logs/webhooks`

List webhooks

### `audit-logs.webhooks.update`

`PATCH /api/audit-logs/webhooks`

Update webhooks

Body: application/json (free-form — pass with `--data`)

# Time Tracker

9 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `time-tracker.billing.invoice.create` | POST | `/api/time-tracker/billing/invoice` | Create a draft ClearBooks invoice from unbilled billable time |
| `time-tracker.billing.preview.list` | GET | `/api/time-tracker/billing/preview` | Preview unbilled billable time for a client as invoice line items |
| `time-tracker.billing.rates.list` | GET | `/api/time-tracker/billing/rates` | Read default billing rates and the ClearBooks customer mapping |
| `time-tracker.billing.rates.update` | PATCH | `/api/time-tracker/billing/rates` | Set default billing rates / the ClearBooks customer mapping |
| `time-tracker.billing.unbill.create` | POST | `/api/time-tracker/billing/unbill` | Clear the invoice stamp from time entries (local inverse) |
| `time-tracker.create` | POST | `/api/time-tracker` | Start a timer |
| `time-tracker.delete` | DELETE | `/api/time-tracker` | Delete a time entry |
| `time-tracker.list` | GET | `/api/time-tracker` | Get time tracker dashboard |
| `time-tracker.update` | PATCH | `/api/time-tracker` | Stop a timer or update a time entry |

---

### `time-tracker.billing.invoice.create`

`POST /api/time-tracker/billing/invoice`

Create a draft ClearBooks invoice from unbilled billable time

Admin only. Creates a DRAFT invoice in ClearBooks (never sends) from the same selection the preview shows, then stamps the billed entries with the invoice reference. Only unbilled entries are ever selected, so a retry cannot double-bill. Requires the calling admin's ClearBooks connection and a client → ClearBooks-customer mapping (stored on the client, or passed as clearbooksCustomerId — an explicit id is remembered on the client when it has no mapping yet).

**Destructive** — needs `--yes` against a non-local base URL.

Body (application/json):
  - `clientId` (string, required)
  - `from` (string)
  - `to` (string)
  - `projectRefs` (string[])
  - `clearbooksCustomerId` (string)
  - `invoiceDate` (string) — YYYY-MM-DD; ClearBooks defaults it server-side.
  - `dueDate` (string) — YYYY-MM-DD; ClearBooks defaults it server-side.
  - `notes` (string)

### `time-tracker.billing.preview.list`

`GET /api/time-tracker/billing/preview`

Preview unbilled billable time for a client as invoice line items

Admin only. Rolls a client's unbilled billable time entries into ClearBooks-ready line items grouped per project (rate resolution: entry override → project default → client default; entries with no resolvable rate or still-running timers are returned as skipped with a reason). Read-only — nothing is created or stamped. Amounts are integer cents.

Query:
  - `clientId` (string, required)
  - `from` (string) — ISO timestamp lower bound on started_at (inclusive).
  - `to` (string) — ISO timestamp upper bound on started_at (inclusive).
  - `projectRefs` (string) — Comma-separated subset of the client's project refs.

### `time-tracker.billing.rates.list`

`GET /api/time-tracker/billing/rates`

Read default billing rates and the ClearBooks customer mapping

Admin only. Returns every per-project default hourly rate in the workspace and, when clientId is passed, that client's default rate and ClearBooks customer mapping.

Query:
  - `clientId` (string)

### `time-tracker.billing.rates.update`

`PATCH /api/time-tracker/billing/rates`

Set default billing rates / the ClearBooks customer mapping

Admin only. Partial update — only fields present in the body are written. Rates are positive integer cents; null clears a rate (or the mapping).

Body (application/json):
  - `clientId` (string)
  - `clientDefaultHourlyRateCents` (integer)
  - `clearbooksCustomerId` (string)
  - `projectRates` (object[])

### `time-tracker.billing.unbill.create`

`POST /api/time-tracker/billing/unbill`

Clear the invoice stamp from time entries (local inverse)

Admin only. Clears invoice_ref/invoiced_at from every entry stamped with the given ClearBooks invoice reference so the time becomes billable again — the local inverse for a voided/deleted draft. Does NOT touch ClearBooks.

**Destructive** — needs `--yes` against a non-local base URL.

Body (application/json):
  - `invoiceRef` (string, required)

### `time-tracker.create`

`POST /api/time-tracker`

Start a timer

Body (application/json):
  - `action` (any, required)
  - `projectRef` (string, required)
  - `taskId` (integer)
  - `actorName` (string)

### `time-tracker.delete`

`DELETE /api/time-tracker`

Delete a time entry

**Destructive** — needs `--yes` against a non-local base URL.

Query:
  - `entryId` (string, required)
  - `actorName` (string)

### `time-tracker.list`

`GET /api/time-tracker`

Get time tracker dashboard

Query:
  - `actorName` (string)

### `time-tracker.update`

`PATCH /api/time-tracker`

Stop a timer or update a time entry

Body (application/json):
  - `action` (string, required) — one of: `stop`, `update`
  - `entryId` (string)
  - `actorName` (string)
  - `projectRef` (string)
  - `taskId` (integer)
  - `startedAt` (string)
  - `endedAt` (string)
  - `billable` (boolean) — Mark the entry billable (action=update only).
  - `hourlyRateCents` (integer) — Per-entry hourly rate override in integer cents (action=update only). null clears the override so the project/client default applies. Entries already stamped onto an invoice reject updates.

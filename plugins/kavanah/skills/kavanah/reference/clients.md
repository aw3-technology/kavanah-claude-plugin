# Clients

20 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `clients.create` | POST | `/api/clients` | Create a new client |
| `clients.delete` | DELETE | `/api/clients/{id}` | Delete a client |
| `clients.employees.create` | POST | `/api/clients/{id}/employees` | Create employee |
| `clients.employees.delete` | DELETE | `/api/clients/{id}/employees/{employeeId}` | Delete employee |
| `clients.employees.update` | PATCH | `/api/clients/{id}/employees/{employeeId}` | Update employee |
| `clients.export.list` | GET | `/api/clients/export` | List export |
| `clients.get` | GET | `/api/clients/{id}` | Get a client by ID |
| `clients.list` | GET | `/api/clients` | List all clients |
| `clients.portal-access.create` | POST | `/api/clients/{id}/portal-access` | Grant or update portal access for a client employee |
| `clients.portal-access.delete` | DELETE | `/api/clients/{id}/portal-access` | Revoke portal access for a client employee |
| `clients.portal-access.list` | GET | `/api/clients/{id}/portal-access` | List portal members for a client |
| `clients.portal-access.update` | PATCH | `/api/clients/{id}/portal-access/{memberId}` | Update a portal member's access |
| `clients.sheet-link.create` | POST | `/api/clients/sheet-link` | Link a Google Sheet to the client directory and import it |
| `clients.sheet-link.list` | GET | `/api/clients/sheet-link` | The Google Sheet linked to the client directory |
| `clients.sheet-link.sync.create` | POST | `/api/clients/sheet-link/sync` | Run a two-way sync of the client directory with its linked sheet |
| `clients.sheet-link.update` | PATCH | `/api/clients/sheet-link` | Configure the outbound mirror for the client sheet link |
| `clients.update` | PATCH | `/api/clients/{id}` | Update a client |
| `record-shares.create` | POST | `/api/record-shares` | Create record share |
| `record-shares.delete` | DELETE | `/api/record-shares` | Delete record share |
| `record-shares.list` | GET | `/api/record-shares` | List record shares |

---

### `clients.create`

`POST /api/clients`

Create a new client

Body (application/json):
  - `company` (string, required)
  - `contactName` (string, required)
  - `email` (string<email>, required)
  - `contactRole` (string)
  - `location` (string)
  - `website` (string)
  - `ownerId` (string)
  - `ownerName` (string)
  - `stage` (string)
  - `health` (string)
  - `invoiceStatus` (string)
  - `arr` (string|number)
  - `priority` (boolean)
  - `archived` (boolean)

### `clients.delete`

`DELETE /api/clients/{id}`

Delete a client

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `clients.employees.create`

`POST /api/clients/{id}/employees`

Create employee

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `clients.employees.delete`

`DELETE /api/clients/{id}/employees/{employeeId}`

Delete employee

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`
  - `employeeId`

### `clients.employees.update`

`PATCH /api/clients/{id}/employees/{employeeId}`

Update employee

Path params (positional, in order):
  - `id`
  - `employeeId`

Body: application/json (free-form — pass with `--data`)

### `clients.export.list`

`GET /api/clients/export`

List export

### `clients.get`

`GET /api/clients/{id}`

Get a client by ID

Path params (positional, in order):
  - `id`

### `clients.list`

`GET /api/clients`

List all clients

### `clients.portal-access.create`

`POST /api/clients/{id}/portal-access`

Grant or update portal access for a client employee

Path params (positional, in order):
  - `id`

Body (application/json):
  - `email` (string, required)
  - `memberId` (string, required)
  - `name` (string)
  - `role` (string)
  - `portalEnabled` (boolean)
  - `canMessage` (boolean)
  - `confirmReinvite` (boolean)

### `clients.portal-access.delete`

`DELETE /api/clients/{id}/portal-access`

Revoke portal access for a client employee

Turns the member's portal access and messaging off and ends their portal sessions. The member row is kept (it is derived from the client record), so a later grant asks for re-invite confirmation.

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

Query:
  - `memberId` (string, required)

### `clients.portal-access.list`

`GET /api/clients/{id}/portal-access`

List portal members for a client

Path params (positional, in order):
  - `id`

### `clients.portal-access.update`

`PATCH /api/clients/{id}/portal-access/{memberId}`

Update a portal member's access

Path params (positional, in order):
  - `id`
  - `memberId`

Body (application/json):
  - `portalEnabled` (boolean) — Turning access on for someone who has never signed in also emails their invite.
  - `canMessage` (boolean)
  - `sendInvite` (boolean) — Email the invite (a 7-day set-password link) again.

### `clients.sheet-link.create`

`POST /api/clients/sheet-link`

Link a Google Sheet to the client directory and import it

Any member with Google Sheets connected. With only `spreadsheet` it is a dry run returning the tab list. With `tab` as well it reads the header row, maps columns (from `columnMapping`, or guessed), runs the import and saves the link. A column must map to `company`.

Body (application/json):
  - `spreadsheet` (string, required) — Sheets URL or spreadsheet id
  - `tab` (string)
  - `columnMapping` (object) — Header to client field

### `clients.sheet-link.list`

`GET /api/clients/sheet-link`

The Google Sheet linked to the client directory

### `clients.sheet-link.sync.create`

`POST /api/clients/sheet-link/sync`

Run a two-way sync of the client directory with its linked sheet

Any member. Imports from the linked sheet, then mirrors outbound. The hourly cron only mirrors outbound; inbound happens only through this call or the agent.

### `clients.sheet-link.update`

`PATCH /api/clients/sheet-link`

Configure the outbound mirror for the client sheet link

The mirror tab may not be the source tab.

Body (application/json):
  - `mirrorEnabled` (boolean)
  - `mirrorTabName` (string)

### `clients.update`

`PATCH /api/clients/{id}`

Update a client

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `record-shares.create`

`POST /api/record-shares`

Create record share

Grant or update a share, and/or flip the record's visibility between 'workspace' and 'private'. Restricted to the record owner or a workspace admin — an `edit` share does NOT confer the right to re-share.

Body (application/json):
  - `resourceType` (string, required) — one of: `client`, `deal`
  - `resourceId` (string, required)
  - `subjectType` (string) — one of: `user`, `team`
  - `subjectId` (string)
  - `access` (string) — one of: `view`, `edit`
  - `visibility` (string) — one of: `workspace`, `private`

### `record-shares.delete`

`DELETE /api/record-shares`

Delete record share

**Destructive** — needs `--yes` against a non-local base URL.

Query:
  - `resourceType` (string, required) — one of: `client`, `deal`
  - `resourceId` (string, required)
  - `subjectType` (string, required) — one of: `user`, `team`
  - `subjectId` (string, required)

### `record-shares.list`

`GET /api/record-shares`

List record shares

Who an account or deal is shared with, plus the caller's own access level and the pickable members/teams. Answers 404 when the caller cannot reach the record, so it can't be used to enumerate private records.

Query:
  - `resourceType` (string, required) — one of: `client`, `deal`
  - `resourceId` (string, required)

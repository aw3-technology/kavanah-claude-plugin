# Expenses

12 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `expenses.create` | POST | `/api/expenses` | Log an expense for the caller |
| `expenses.delete` | DELETE | `/api/expenses/{id}` | Delete an expense that is not approved |
| `expenses.export.list` | GET | `/api/expenses/export` | Export expenses as CSV |
| `expenses.get` | GET | `/api/expenses/{id}` | Get one expense |
| `expenses.list` | GET | `/api/expenses` | List expenses with a summary |
| `expenses.receipt.create` | POST | `/api/expenses/{id}/receipt` | Attach or replace the receipt (photo or PDF, up to 4 MB) |
| `expenses.receipt.delete` | DELETE | `/api/expenses/{id}/receipt` | Remove the receipt |
| `expenses.receipt.list` | GET | `/api/expenses/{id}/receipt` | Read an expense's receipt |
| `expenses.review.create` | POST | `/api/expenses/{id}/review` | Approve, reject, reimburse or reopen an expense (owner or admin) |
| `expenses.settings.list` | GET | `/api/expenses/settings` | Get the workspace mileage rate |
| `expenses.settings.update` | PATCH | `/api/expenses/settings` | Set the workspace mileage rate (owner or admin) |
| `expenses.update` | PATCH | `/api/expenses/{id}` | Correct an expense that is not approved |

---

### `expenses.create`

`POST /api/expenses`

Log an expense for the caller

Mileage takes miles and the server prices it. Everything else takes amount.

Body (application/json):
  - `kind` (string, required) — one of: `mileage`, `fuel`, `parking_tolls`, `meals`, `lodging`, `transport`, `supplies`, `other`
  - `expenseDate` (string<date>, required)
  - `miles` (number)
  - `amount` (string) — Dollars
  - `tripFrom` (string)
  - `tripTo` (string)
  - `vendor` (string)
  - `description` (string)
  - `projectRef` (string)

### `expenses.delete`

`DELETE /api/expenses/{id}`

Delete an expense that is not approved

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `expenses.export.list`

`GET /api/expenses/export`

Export expenses as CSV

Takes the same filters as GET /api/expenses.

### `expenses.get`

`GET /api/expenses/{id}`

Get one expense

Path params (positional, in order):
  - `id`

### `expenses.list`

`GET /api/expenses`

List expenses with a summary

A member gets their own. An owner or admin may pass scope=team.

Query:
  - `scope` (string) — one of: `mine`, `team`
  - `memberName` (string)
  - `status` (string) — one of: `submitted`, `approved`, `rejected`, `reimbursed`
  - `kind` (string)
  - `projectRef` (string)
  - `startDate` (string<date>)
  - `endDate` (string<date>)
  - `limit` (integer)

### `expenses.receipt.create`

`POST /api/expenses/{id}/receipt`

Attach or replace the receipt (photo or PDF, up to 4 MB)

Path params (positional, in order):
  - `id`

Body (multipart/form-data):
  - `file` (string<binary>, required)

### `expenses.receipt.delete`

`DELETE /api/expenses/{id}/receipt`

Remove the receipt

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `expenses.receipt.list`

`GET /api/expenses/{id}/receipt`

Read an expense's receipt

Path params (positional, in order):
  - `id`

### `expenses.review.create`

`POST /api/expenses/{id}/review`

Approve, reject, reimburse or reopen an expense (owner or admin)

Path params (positional, in order):
  - `id`

Body (application/json):
  - `action` (string, required) — one of: `approve`, `reject`, `reimburse`, `reopen`
  - `note` (string) — Required to reject

### `expenses.settings.list`

`GET /api/expenses/settings`

Get the workspace mileage rate

### `expenses.settings.update`

`PATCH /api/expenses/settings`

Set the workspace mileage rate (owner or admin)

Body (application/json):
  - `mileageRateCents` (number, required) — Cents a mile. Null follows the IRS rate. Past expenses keep theirs.

### `expenses.update`

`PATCH /api/expenses/{id}`

Correct an expense that is not approved

Same fields as POST, all optional. A rejected expense returns to submitted.

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

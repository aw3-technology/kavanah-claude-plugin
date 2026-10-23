# Portfolio

30 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `portfolio.availability.requests.create` | POST | `/api/portfolio/availability/requests` | Create an availability request (admin only) |
| `portfolio.availability.requests.delete` | DELETE | `/api/portfolio/availability/requests` | Delete an availability request (admin only) |
| `portfolio.availability.requests.list` | GET | `/api/portfolio/availability/requests` | List availability requests (leader-to-team asks) |
| `portfolio.availability.requests.update` | PATCH | `/api/portfolio/availability/requests` | Update an availability request status (admin only) |
| `portfolio.availability.submissions.create` | POST | `/api/portfolio/availability/submissions` | Upsert the caller's own availability submission |
| `portfolio.availability.submissions.list` | GET | `/api/portfolio/availability/submissions` | List availability submissions (admins see all; members see their own) |
| `portfolio.budgets.create` | POST | `/api/portfolio/budgets` | Create budget |
| `portfolio.budgets.entries.create` | POST | `/api/portfolio/budgets/entries` | Create a budget entry |
| `portfolio.budgets.entries.list` | GET | `/api/portfolio/budgets/entries` | List entries |
| `portfolio.budgets.list` | GET | `/api/portfolio/budgets` | List budgets |
| `portfolio.forecasts.list` | GET | `/api/portfolio/forecasts` | List forecasts |
| `portfolio.list` | GET | `/api/portfolio` | List portfolio |
| `portfolio.objectives.create` | POST | `/api/portfolio/objectives` | Create objective |
| `portfolio.objectives.delete` | DELETE | `/api/portfolio/objectives` | Delete objectives |
| `portfolio.objectives.list` | GET | `/api/portfolio/objectives` | List objectives |
| `portfolio.objectives.update` | PATCH | `/api/portfolio/objectives` | Update objectives |
| `portfolio.programs.create` | POST | `/api/portfolio/programs` | Create program |
| `portfolio.programs.delete` | DELETE | `/api/portfolio/programs` | Delete programs |
| `portfolio.programs.list` | GET | `/api/portfolio/programs` | List programs |
| `portfolio.programs.update` | PATCH | `/api/portfolio/programs` | Update programs |
| `portfolio.resources.allocations.create` | POST | `/api/portfolio/resources/allocations` | Create allocation |
| `portfolio.resources.allocations.delete` | DELETE | `/api/portfolio/resources/allocations` | Delete allocations |
| `portfolio.resources.allocations.list` | GET | `/api/portfolio/resources/allocations` | List allocations |
| `portfolio.resources.allocations.update` | PATCH | `/api/portfolio/resources/allocations` | Update allocations |
| `portfolio.resources.capacity.create` | POST | `/api/portfolio/resources/capacity` | Create capacity |
| `portfolio.resources.capacity.list` | GET | `/api/portfolio/resources/capacity` | List capacity |
| `portfolio.resources.requests.create` | POST | `/api/portfolio/resources/requests` | Create request |
| `portfolio.resources.requests.list` | GET | `/api/portfolio/resources/requests` | List requests |
| `portfolio.resources.requests.update` | PATCH | `/api/portfolio/resources/requests` | Update requests |
| `portfolio.workload-distribution.list` | GET | `/api/portfolio/workload-distribution` | (undocumented route — params unknown, pass them explicitly) |

---

### `portfolio.availability.requests.create`

`POST /api/portfolio/availability/requests`

Create an availability request (admin only)

Body (application/json):
  - `projectRef` (string) — null = workspace-wide
  - `title` (string, required)
  - `message` (string)
  - `periodStart` (string<date>, required)
  - `periodEnd` (string<date>, required)
  - `dueDate` (string<date>)

### `portfolio.availability.requests.delete`

`DELETE /api/portfolio/availability/requests`

Delete an availability request (admin only)

**Destructive** — needs `--yes` against a non-local base URL.

Query:
  - `id` (string, required)

### `portfolio.availability.requests.list`

`GET /api/portfolio/availability/requests`

List availability requests (leader-to-team asks)

### `portfolio.availability.requests.update`

`PATCH /api/portfolio/availability/requests`

Update an availability request status (admin only)

Body (application/json):
  - `id` (string, required)
  - `status` (string) — one of: `open`, `closed`

### `portfolio.availability.submissions.create`

`POST /api/portfolio/availability/submissions`

Upsert the caller's own availability submission

Body (application/json):
  - `requestId` (string) — Omit for a standing entry
  - `status` (string) — one of: `available`, `limited`, `unavailable`
  - `availableHoursPerWeek` (number)
  - `periodStart` (string<date>)
  - `periodEnd` (string<date>)
  - `timeOff` (object[])
  - `notes` (string)

### `portfolio.availability.submissions.list`

`GET /api/portfolio/availability/submissions`

List availability submissions (admins see all; members see their own)

Query:
  - `requestId` (string)

### `portfolio.budgets.create`

`POST /api/portfolio/budgets`

Create budget

Body: application/json (free-form — pass with `--data`)

### `portfolio.budgets.entries.create`

`POST /api/portfolio/budgets/entries`

Create a budget entry

Body: application/json (free-form — pass with `--data`)

### `portfolio.budgets.entries.list`

`GET /api/portfolio/budgets/entries`

List entries

### `portfolio.budgets.list`

`GET /api/portfolio/budgets`

List budgets

### `portfolio.forecasts.list`

`GET /api/portfolio/forecasts`

List forecasts

### `portfolio.list`

`GET /api/portfolio`

List portfolio

### `portfolio.objectives.create`

`POST /api/portfolio/objectives`

Create objective

Body: application/json (free-form — pass with `--data`)

### `portfolio.objectives.delete`

`DELETE /api/portfolio/objectives`

Delete objectives

**Destructive** — needs `--yes` against a non-local base URL.

### `portfolio.objectives.list`

`GET /api/portfolio/objectives`

List objectives

### `portfolio.objectives.update`

`PATCH /api/portfolio/objectives`

Update objectives

Body: application/json (free-form — pass with `--data`)

### `portfolio.programs.create`

`POST /api/portfolio/programs`

Create program

Body: application/json (free-form — pass with `--data`)

### `portfolio.programs.delete`

`DELETE /api/portfolio/programs`

Delete programs

**Destructive** — needs `--yes` against a non-local base URL.

### `portfolio.programs.list`

`GET /api/portfolio/programs`

List programs

### `portfolio.programs.update`

`PATCH /api/portfolio/programs`

Update programs

Body: application/json (free-form — pass with `--data`)

### `portfolio.resources.allocations.create`

`POST /api/portfolio/resources/allocations`

Create allocation

Body: application/json (free-form — pass with `--data`)

### `portfolio.resources.allocations.delete`

`DELETE /api/portfolio/resources/allocations`

Delete allocations

**Destructive** — needs `--yes` against a non-local base URL.

### `portfolio.resources.allocations.list`

`GET /api/portfolio/resources/allocations`

List allocations

### `portfolio.resources.allocations.update`

`PATCH /api/portfolio/resources/allocations`

Update allocations

Body: application/json (free-form — pass with `--data`)

### `portfolio.resources.capacity.create`

`POST /api/portfolio/resources/capacity`

Create capacity

Body: application/json (free-form — pass with `--data`)

### `portfolio.resources.capacity.list`

`GET /api/portfolio/resources/capacity`

List capacity

### `portfolio.resources.requests.create`

`POST /api/portfolio/resources/requests`

Create request

Body: application/json (free-form — pass with `--data`)

### `portfolio.resources.requests.list`

`GET /api/portfolio/resources/requests`

List requests

### `portfolio.resources.requests.update`

`PATCH /api/portfolio/resources/requests`

Update requests

Body: application/json (free-form — pass with `--data`)

### `portfolio.workload-distribution.list`

`GET /api/portfolio/workload-distribution`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

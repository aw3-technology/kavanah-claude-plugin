# Reports

31 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `projects.cycle-time.list` | GET | `/api/projects/{id}/cycle-time` | Per-status cycle-time stats for a project |
| `reports.create` | POST | `/api/reports` | Create report |
| `reports.dashboards.create` | POST | `/api/reports/dashboards` | Create dashboard |
| `reports.dashboards.delete` | DELETE | `/api/reports/dashboards/{id}` | Delete dashboard |
| `reports.dashboards.get` | GET | `/api/reports/dashboards/{id}` | Fetch dashboard |
| `reports.dashboards.list` | GET | `/api/reports/dashboards` | List dashboards |
| `reports.dashboards.update` | PATCH | `/api/reports/dashboards/{id}` | Update dashboard |
| `reports.dashboards.widgets.create` | POST | `/api/reports/dashboards/{id}/widgets` | Create widget |
| `reports.dashboards.widgets.delete` | DELETE | `/api/reports/dashboards/{id}/widgets/{widgetId}` | Delete widget |
| `reports.dashboards.widgets.list` | GET | `/api/reports/dashboards/{id}/widgets` | List widgets |
| `reports.dashboards.widgets.update` | PATCH | `/api/reports/dashboards/{id}/widgets/{widgetId}` | Update widget |
| `reports.delete` | DELETE | `/api/reports/{id}` | Delete report |
| `reports.embed.get` | GET | `/api/reports/embed/{token}` | Fetch embed |
| `reports.export.create` | POST | `/api/reports/export` | Create export |
| `reports.filters.create` | POST | `/api/reports/filters` | Create filter |
| `reports.filters.delete` | DELETE | `/api/reports/filters/{id}` | Delete filter |
| `reports.filters.get` | GET | `/api/reports/filters/{id}` | Fetch filter |
| `reports.filters.list` | GET | `/api/reports/filters` | List filters |
| `reports.generate.create` | POST | `/api/reports/generate` | Create generate |
| `reports.get` | GET | `/api/reports/{id}` | Fetch report |
| `reports.insights.create` | POST | `/api/reports/insights` | Create insight |
| `reports.insights.narrative.create` | POST | `/api/reports/insights/narrative` | Create narrative |
| `reports.list` | GET | `/api/reports` | List reports |
| `reports.operating.list` | GET | `/api/reports/operating` | Operating metrics report |
| `reports.schedules.create` | POST | `/api/reports/schedules` | Create schedule |
| `reports.schedules.delete` | DELETE | `/api/reports/schedules/{id}` | Delete schedule |
| `reports.schedules.list` | GET | `/api/reports/schedules` | List schedules |
| `reports.schedules.run.create` | POST | `/api/reports/schedules/{p1}/run` | (undocumented route — params unknown, pass them explicitly) |
| `reports.schedules.update` | PATCH | `/api/reports/schedules/{id}` | Update schedule |
| `reports.state-of-business.create` | POST | `/api/reports/state-of-business` | Configure the State of the Business report (admin) |
| `reports.state-of-business.list` | GET | `/api/reports/state-of-business` | Get the State of the Business report config + status |

---

### `projects.cycle-time.list`

`GET /api/projects/{id}/cycle-time`

Per-status cycle-time stats for a project

Mean, median (p50), and p90 time tasks spent in each column over the last sinceDays days. Sourced from app_task_transitions (real column moves).

Path params (positional, in order):
  - `id`

Query:
  - `sinceDays` (integer)

### `reports.create`

`POST /api/reports`

Create report

Body: application/json (free-form — pass with `--data`)

### `reports.dashboards.create`

`POST /api/reports/dashboards`

Create dashboard

Body: application/json (free-form — pass with `--data`)

### `reports.dashboards.delete`

`DELETE /api/reports/dashboards/{id}`

Delete dashboard

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `reports.dashboards.get`

`GET /api/reports/dashboards/{id}`

Fetch dashboard

Path params (positional, in order):
  - `id`

### `reports.dashboards.list`

`GET /api/reports/dashboards`

List dashboards

### `reports.dashboards.update`

`PATCH /api/reports/dashboards/{id}`

Update dashboard

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `reports.dashboards.widgets.create`

`POST /api/reports/dashboards/{id}/widgets`

Create widget

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `reports.dashboards.widgets.delete`

`DELETE /api/reports/dashboards/{id}/widgets/{widgetId}`

Delete widget

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`
  - `widgetId`

### `reports.dashboards.widgets.list`

`GET /api/reports/dashboards/{id}/widgets`

List widgets

Path params (positional, in order):
  - `id`

### `reports.dashboards.widgets.update`

`PATCH /api/reports/dashboards/{id}/widgets/{widgetId}`

Update widget

Path params (positional, in order):
  - `id`
  - `widgetId`

Body: application/json (free-form — pass with `--data`)

### `reports.delete`

`DELETE /api/reports/{id}`

Delete report

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `reports.embed.get`

`GET /api/reports/embed/{token}`

Fetch embed

Path params (positional, in order):
  - `token`

### `reports.export.create`

`POST /api/reports/export`

Create export

Body: application/json (free-form — pass with `--data`)

### `reports.filters.create`

`POST /api/reports/filters`

Create filter

Body: application/json (free-form — pass with `--data`)

### `reports.filters.delete`

`DELETE /api/reports/filters/{id}`

Delete filter

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `reports.filters.get`

`GET /api/reports/filters/{id}`

Fetch filter

Path params (positional, in order):
  - `id`

### `reports.filters.list`

`GET /api/reports/filters`

List filters

### `reports.generate.create`

`POST /api/reports/generate`

Create generate

Body: application/json (free-form — pass with `--data`)

### `reports.get`

`GET /api/reports/{id}`

Fetch report

Path params (positional, in order):
  - `id`

### `reports.insights.create`

`POST /api/reports/insights`

Create insight

Body: application/json (free-form — pass with `--data`)

### `reports.insights.narrative.create`

`POST /api/reports/insights/narrative`

Create narrative

Body: application/json (free-form — pass with `--data`)

### `reports.list`

`GET /api/reports`

List reports

### `reports.operating.list`

`GET /api/reports/operating`

Operating metrics report

Query:
  - `days` (integer) — Lookback window. Non-numeric or non-positive values fall back to 90.

### `reports.schedules.create`

`POST /api/reports/schedules`

Create schedule

Body: application/json (free-form — pass with `--data`)

### `reports.schedules.delete`

`DELETE /api/reports/schedules/{id}`

Delete schedule

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `reports.schedules.list`

`GET /api/reports/schedules`

List schedules

### `reports.schedules.run.create`

`POST /api/reports/schedules/{p1}/run`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `reports.schedules.update`

`PATCH /api/reports/schedules/{id}`

Update schedule

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `reports.state-of-business.create`

`POST /api/reports/state-of-business`

Configure the State of the Business report (admin)

Create/update the report + schedule and arm the opt-in flag. Admin only.

Body: application/json (free-form — pass with `--data`)

### `reports.state-of-business.list`

`GET /api/reports/state-of-business`

Get the State of the Business report config + status

# Agent Alerts

8 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `agent-alerts.briefing.list` | GET | `/api/agent-alerts/briefing` | List briefing |
| `agent-alerts.dismiss.create` | POST | `/api/agent-alerts/dismiss` | Dismiss an agent alert |
| `agent-alerts.dismiss.list` | GET | `/api/agent-alerts/dismiss` | List dismissed agent alerts |
| `agent-alerts.list` | GET | `/api/agent-alerts` | List agent alerts |
| `agent-alerts.preferences.list` | GET | `/api/agent-alerts/preferences` | List preferences |
| `agent-alerts.preferences.update` | PATCH | `/api/agent-alerts/preferences` | Update preferences |
| `agent-alerts.scan.create` | POST | `/api/agent-alerts/scan` | Create scan |
| `agent-alerts.update` | PATCH | `/api/agent-alerts` | Update agent alerts |

---

### `agent-alerts.briefing.list`

`GET /api/agent-alerts/briefing`

List briefing

### `agent-alerts.dismiss.create`

`POST /api/agent-alerts/dismiss`

Dismiss an agent alert

Body: application/json (free-form — pass with `--data`)

### `agent-alerts.dismiss.list`

`GET /api/agent-alerts/dismiss`

List dismissed agent alerts

### `agent-alerts.list`

`GET /api/agent-alerts`

List agent alerts

### `agent-alerts.preferences.list`

`GET /api/agent-alerts/preferences`

List preferences

### `agent-alerts.preferences.update`

`PATCH /api/agent-alerts/preferences`

Update preferences

Body: application/json (free-form — pass with `--data`)

### `agent-alerts.scan.create`

`POST /api/agent-alerts/scan`

Create scan

Body: application/json (free-form — pass with `--data`)

### `agent-alerts.update`

`PATCH /api/agent-alerts`

Update agent alerts

Body: application/json (free-form — pass with `--data`)

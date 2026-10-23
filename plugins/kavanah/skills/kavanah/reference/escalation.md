# Escalation

4 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `escalation-rules.create` | POST | `/api/escalation-rules` | Create an escalation rule |
| `escalation-rules.delete` | DELETE | `/api/escalation-rules/{id}` | Delete an escalation rule |
| `escalation-rules.list` | GET | `/api/escalation-rules` | List escalation rules |
| `escalation-rules.set` | PUT | `/api/escalation-rules/{id}` | Update an escalation rule |

---

### `escalation-rules.create`

`POST /api/escalation-rules`

Create an escalation rule

Body (application/json):
  - `projectRef` (string, required)
  - `name` (string, required)
  - `conditionType` (string, required)
  - `conditionConfig` (object)
  - `actionType` (string, required)
  - `actionConfig` (object)
  - `enabled` (boolean)

### `escalation-rules.delete`

`DELETE /api/escalation-rules/{id}`

Delete an escalation rule

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `escalation-rules.list`

`GET /api/escalation-rules`

List escalation rules

Query:
  - `projectRef` (string)

### `escalation-rules.set`

`PUT /api/escalation-rules/{id}`

Update an escalation rule

Path params (positional, in order):
  - `id`

# SLA

4 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `sla-policies.create` | POST | `/api/sla-policies` | Create an SLA policy |
| `sla-policies.delete` | DELETE | `/api/sla-policies/{id}` | Delete an SLA policy |
| `sla-policies.list` | GET | `/api/sla-policies` | List SLA policies |
| `sla-policies.set` | PUT | `/api/sla-policies/{id}` | Update an SLA policy |

---

### `sla-policies.create`

`POST /api/sla-policies`

Create an SLA policy

Body (application/json):
  - `projectRef` (string, required)
  - `name` (string, required)
  - `priority` (string)
  - `responseTimeMinutes` (integer)
  - `resolutionTimeMinutes` (integer)
  - `enabled` (boolean)

### `sla-policies.delete`

`DELETE /api/sla-policies/{id}`

Delete an SLA policy

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `sla-policies.list`

`GET /api/sla-policies`

List SLA policies

Query:
  - `projectRef` (string)

### `sla-policies.set`

`PUT /api/sla-policies/{id}`

Update an SLA policy

Path params (positional, in order):
  - `id`

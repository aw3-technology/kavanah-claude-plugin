# Automations

8 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `automations.authorize.create` | POST | `/api/automations/{id}/authorize` | Authorize (or revoke) one agent rule to run at Full autonomy |
| `automations.create` | POST | `/api/automations` | Create an automation rule |
| `automations.delete` | DELETE | `/api/automations/{id}` | Delete an automation rule |
| `automations.list` | GET | `/api/automations` | List automation rules |
| `automations.page-data.list` | GET | `/api/automations/page-data` | List page data |
| `automations.runs.list` | GET | `/api/automations/{id}/runs` | Recent execution history for one automation rule |
| `automations.set` | PUT | `/api/automations/{id}` | Update an automation rule |
| `automations.vocabulary.list` | GET | `/api/automations/vocabulary` | Every trigger and action a rule can be built from |

---

### `automations.authorize.create`

`POST /api/automations/{id}/authorize`

Authorize (or revoke) one agent rule to run at Full autonomy

Workspace owner/admin only. Authorizes ONE invoke-agent rule to run its agent at Full autonomy above the workspace's autonomy ceiling, without raising that ceiling for every member — or revokes it. Each send still follows the rule's send_mode ('approval' parks every send for a human). Any later change to the rule's trigger or action clears the authorization automatically, and it only counts while the authorizing admin is still an active owner/admin.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `action` (string, required) — one of: `authorize`, `revoke`

### `automations.create`

`POST /api/automations`

Create an automation rule

Body (application/json):
  - `projectRef` (string, required)
  - `name` (string, required)
  - `triggerType` (string, required) — A trigger from GET /api/automations/vocabulary — task lifecycle (created, moved, completed, assigned, due-date, property-changed), an external event (email-received, integration-item, github-pull-request, github-issue, github-push, calendar-event, finance-event, document-event), or a deal event (deal-stage-changed, deal-document-signed, meeting-booked, bd-match-found). bd-match-found fires once per new deal/partner broker-dealer pairing from the hourly scan; triggerConfig accepts { min_score (a floor, 50-100), stage_kind, pipeline_id }. The client-facing deal actions skip it — pair it with invoke-agent to email the partner.
  - `triggerConfig` (object)
  - `actionType` (string, required) — An action from GET /api/automations/vocabulary — a task action (assign, change-status, set-field, add-tag, remove-tag, add-comment, move-to-project, send-notification, set-property), invoke-agent, start-water-cooler, a deal action (provision-client-space, send-engagement-envelope, enroll-cadence, start-investor-campaign — admin-only), start-issuer-campaign (client prospecting on a named issuer campaign; admin-only, task or deal triggers only), or an internal deal-side action (move-deal-stage, create-task).
  - `actionConfig` (object)
  - `enabled` (boolean)

### `automations.delete`

`DELETE /api/automations/{id}`

Delete an automation rule

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `automations.list`

`GET /api/automations`

List automation rules

Query:
  - `projectRef` (string)

### `automations.page-data.list`

`GET /api/automations/page-data`

List page data

### `automations.runs.list`

`GET /api/automations/{id}/runs`

Recent execution history for one automation rule

Each row is one firing of the rule. Status is success, skipped, or error; detail is the action handler's diagnostic string.

Path params (positional, in order):
  - `id`

Query:
  - `limit` (integer)

### `automations.set`

`PUT /api/automations/{id}`

Update an automation rule

Path params (positional, in order):
  - `id`

Body (application/json):
  - `name` (string)
  - `triggerType` (string)
  - `triggerConfig` (object)
  - `actionType` (string)
  - `actionConfig` (object)
  - `enabled` (boolean)

### `automations.vocabulary.list`

`GET /api/automations/vocabulary`

Every trigger and action a rule can be built from

The full vocabulary: each trigger with the conditions it accepts, and each action with the config fields it needs, whether it requires a task, and whether its effect leaves Kavanah irreversibly. DERIVED from `ACTION_HANDLERS` and `TRIGGER_TYPES` — the same registries `POST /api/automations` validates against — rather than restated. The rule builder that consumes it therefore cannot offer a trigger the server rejects, and cannot silently miss one that ships later. The builder it replaced kept its own copy, could express 4 of the 14 triggers, and always saved an empty action config.

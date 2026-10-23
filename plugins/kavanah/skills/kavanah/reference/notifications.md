# Notifications

46 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `notifications.admin.escalation-rules.create` | POST | `/api/notifications/admin/escalation-rules` | Create escalation rule |
| `notifications.admin.escalation-rules.delete` | DELETE | `/api/notifications/admin/escalation-rules` | Delete escalation rules |
| `notifications.admin.escalation-rules.list` | GET | `/api/notifications/admin/escalation-rules` | List escalation rules |
| `notifications.admin.escalation-rules.update` | PATCH | `/api/notifications/admin/escalation-rules` | Update escalation rules |
| `notifications.admin.health-alerts.create` | POST | `/api/notifications/admin/health-alerts` | Create health alert |
| `notifications.admin.health-alerts.delete` | DELETE | `/api/notifications/admin/health-alerts` | Delete health alerts |
| `notifications.admin.health-alerts.list` | GET | `/api/notifications/admin/health-alerts` | List health alerts |
| `notifications.admin.health-alerts.update` | PATCH | `/api/notifications/admin/health-alerts` | Update health alerts |
| `notifications.admin.metrics.list` | GET | `/api/notifications/admin/metrics` | List metrics |
| `notifications.admin.rules.create` | POST | `/api/notifications/admin/rules` | Create rule |
| `notifications.admin.rules.delete` | DELETE | `/api/notifications/admin/rules` | Delete rules |
| `notifications.admin.rules.list` | GET | `/api/notifications/admin/rules` | List rules |
| `notifications.admin.rules.update` | PATCH | `/api/notifications/admin/rules` | Update rules |
| `notifications.admin.teams.create` | POST | `/api/notifications/admin/teams` | Create team |
| `notifications.admin.teams.delete` | DELETE | `/api/notifications/admin/teams` | Delete teams |
| `notifications.admin.teams.list` | GET | `/api/notifications/admin/teams` | List teams |
| `notifications.admin.workspace-defaults.list` | GET | `/api/notifications/admin/workspace-defaults` | List workspace defaults |
| `notifications.admin.workspace-defaults.update` | PATCH | `/api/notifications/admin/workspace-defaults` | Update workspace defaults |
| `notifications.count.list` | GET | `/api/notifications/count` | (undocumented route — params unknown, pass them explicitly) |
| `notifications.digest.list` | GET | `/api/notifications/digest` | List digest |
| `notifications.digest.update` | PATCH | `/api/notifications/digest` | Update digest |
| `notifications.dispatch.create` | POST | `/api/notifications/dispatch` | Create dispatch |
| `notifications.list` | GET | `/api/notifications` | Get notification center data |
| `notifications.muted-threads.create` | POST | `/api/notifications/muted-threads` | Create muted thread |
| `notifications.muted-threads.delete` | DELETE | `/api/notifications/muted-threads` | Delete muted threads |
| `notifications.muted-threads.list` | GET | `/api/notifications/muted-threads` | List muted threads |
| `notifications.other-workspaces.list` | GET | `/api/notifications/other-workspaces` | Unread notification counts for the user's OTHER workspaces |
| `notifications.preferences.list` | GET | `/api/notifications/preferences` | List preferences |
| `notifications.preferences.update` | PATCH | `/api/notifications/preferences` | Update preferences |
| `notifications.process.create` | POST | `/api/notifications/process` | Process pending notifications |
| `notifications.process.list` | GET | `/api/notifications/process` | (undocumented route — params unknown, pass them explicitly) |
| `notifications.push-tokens.create` | POST | `/api/notifications/push-tokens` | Create push token |
| `notifications.push-tokens.delete` | DELETE | `/api/notifications/push-tokens` | Delete push tokens |
| `notifications.push-tokens.list` | GET | `/api/notifications/push-tokens` | List push tokens |
| `notifications.quiet-hours.list` | GET | `/api/notifications/quiet-hours` | List quiet hours |
| `notifications.quiet-hours.update` | PATCH | `/api/notifications/quiet-hours` | Update quiet hours |
| `notifications.sms.verify.create` | POST | `/api/notifications/sms/verify` | Start or confirm SMS verification |
| `notifications.sms.verify.delete` | DELETE | `/api/notifications/sms/verify` | Forget the caller's enrolled number |
| `notifications.sms.verify.list` | GET | `/api/notifications/sms/verify` | Get the caller's SMS enrolment state |
| `notifications.subscriptions.create` | POST | `/api/notifications/subscriptions` | Create subscription |
| `notifications.subscriptions.delete` | DELETE | `/api/notifications/subscriptions` | Delete subscriptions |
| `notifications.subscriptions.list` | GET | `/api/notifications/subscriptions` | List subscriptions |
| `notifications.unsubscribe.create` | POST | `/api/notifications/unsubscribe` | Create unsubscribe |
| `notifications.unsubscribe.list` | GET | `/api/notifications/unsubscribe` | List unsubscribe |
| `notifications.update` | PATCH | `/api/notifications` | Update notification state |
| `sidebar.unread-sources.list` | GET | `/api/sidebar/unread-sources` | Where the Messages and Email Inbox unread items are |

---

### `notifications.admin.escalation-rules.create`

`POST /api/notifications/admin/escalation-rules`

Create escalation rule

Body: application/json (free-form — pass with `--data`)

### `notifications.admin.escalation-rules.delete`

`DELETE /api/notifications/admin/escalation-rules`

Delete escalation rules

**Destructive** — needs `--yes` against a non-local base URL.

### `notifications.admin.escalation-rules.list`

`GET /api/notifications/admin/escalation-rules`

List escalation rules

### `notifications.admin.escalation-rules.update`

`PATCH /api/notifications/admin/escalation-rules`

Update escalation rules

Body: application/json (free-form — pass with `--data`)

### `notifications.admin.health-alerts.create`

`POST /api/notifications/admin/health-alerts`

Create health alert

Body: application/json (free-form — pass with `--data`)

### `notifications.admin.health-alerts.delete`

`DELETE /api/notifications/admin/health-alerts`

Delete health alerts

**Destructive** — needs `--yes` against a non-local base URL.

### `notifications.admin.health-alerts.list`

`GET /api/notifications/admin/health-alerts`

List health alerts

### `notifications.admin.health-alerts.update`

`PATCH /api/notifications/admin/health-alerts`

Update health alerts

Body: application/json (free-form — pass with `--data`)

### `notifications.admin.metrics.list`

`GET /api/notifications/admin/metrics`

List metrics

### `notifications.admin.rules.create`

`POST /api/notifications/admin/rules`

Create rule

Body: application/json (free-form — pass with `--data`)

### `notifications.admin.rules.delete`

`DELETE /api/notifications/admin/rules`

Delete rules

**Destructive** — needs `--yes` against a non-local base URL.

### `notifications.admin.rules.list`

`GET /api/notifications/admin/rules`

List rules

### `notifications.admin.rules.update`

`PATCH /api/notifications/admin/rules`

Update rules

Body: application/json (free-form — pass with `--data`)

### `notifications.admin.teams.create`

`POST /api/notifications/admin/teams`

Create team

Body: application/json (free-form — pass with `--data`)

### `notifications.admin.teams.delete`

`DELETE /api/notifications/admin/teams`

Delete teams

**Destructive** — needs `--yes` against a non-local base URL.

### `notifications.admin.teams.list`

`GET /api/notifications/admin/teams`

List teams

### `notifications.admin.workspace-defaults.list`

`GET /api/notifications/admin/workspace-defaults`

List workspace defaults

### `notifications.admin.workspace-defaults.update`

`PATCH /api/notifications/admin/workspace-defaults`

Update workspace defaults

Body: application/json (free-form — pass with `--data`)

### `notifications.count.list`

`GET /api/notifications/count`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `notifications.digest.list`

`GET /api/notifications/digest`

List digest

### `notifications.digest.update`

`PATCH /api/notifications/digest`

Update digest

Body: application/json (free-form — pass with `--data`)

### `notifications.dispatch.create`

`POST /api/notifications/dispatch`

Create dispatch

Body: application/json (free-form — pass with `--data`)

### `notifications.list`

`GET /api/notifications`

Get notification center data

### `notifications.muted-threads.create`

`POST /api/notifications/muted-threads`

Create muted thread

Body: application/json (free-form — pass with `--data`)

### `notifications.muted-threads.delete`

`DELETE /api/notifications/muted-threads`

Delete muted threads

**Destructive** — needs `--yes` against a non-local base URL.

### `notifications.muted-threads.list`

`GET /api/notifications/muted-threads`

List muted threads

### `notifications.other-workspaces.list`

`GET /api/notifications/other-workspaces`

Unread notification counts for the user's OTHER workspaces

The /notifications page renders one workspace, but the sidebar pill and OS dock badge count unread across every workspace the user belongs to. Returns the breakdown for the workspaces the page is not showing, so the badge is explainable without either scoping it down or hiding the notifications. The selected workspace is excluded — its unread is on the page itself.

### `notifications.preferences.list`

`GET /api/notifications/preferences`

List preferences

### `notifications.preferences.update`

`PATCH /api/notifications/preferences`

Update preferences

Body: application/json (free-form — pass with `--data`)

### `notifications.process.create`

`POST /api/notifications/process`

Process pending notifications

Body: application/json (free-form — pass with `--data`)

### `notifications.process.list`

`GET /api/notifications/process`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `notifications.push-tokens.create`

`POST /api/notifications/push-tokens`

Create push token

Body: application/json (free-form — pass with `--data`)

### `notifications.push-tokens.delete`

`DELETE /api/notifications/push-tokens`

Delete push tokens

**Destructive** — needs `--yes` against a non-local base URL.

### `notifications.push-tokens.list`

`GET /api/notifications/push-tokens`

List push tokens

### `notifications.quiet-hours.list`

`GET /api/notifications/quiet-hours`

List quiet hours

### `notifications.quiet-hours.update`

`PATCH /api/notifications/quiet-hours`

Update quiet hours

Body: application/json (free-form — pass with `--data`)

### `notifications.sms.verify.create`

`POST /api/notifications/sms/verify`

Start or confirm SMS verification

Send `{ phone }` to start verification (delivers a code by SMS), or `{ code }` to confirm one already sent. Deliberately has no userId parameter and is always scoped to the CALLER: enrolling a phone is proof that the person holds that handset, so letting one user start verification for another would make the flow meaningless. Sending a code costs money and is subject to the workspace SMS opt-in and the monthly segment cap, even though it bypasses the notification preference and quiet-hours gates (it is transactional — the user is on the settings screen asking for it).

Body (application/json):
  - `phone` (string, required) — E.164 number to enrol, e.g. "+15555550100"
  - `code` (string, required) — The verification code received by SMS

### `notifications.sms.verify.delete`

`DELETE /api/notifications/sms/verify`

Forget the caller's enrolled number

Remove the caller's phone entirely, ending SMS alerts for them. Scoped to the caller. Note this is distinct from a carrier STOP, which records an opt-out against the number rather than deleting the enrolment.

**Destructive** — needs `--yes` against a non-local base URL.

### `notifications.sms.verify.list`

`GET /api/notifications/sms/verify`

Get the caller's SMS enrolment state

Whether the caller has a phone enrolled for SMS alerts, and how far through verification it is. The number is MASKED — the settings panel only needs to know which handset is enrolled, and echoing a full phone number back through an API is a needless way to leak one into a log or a browser cache. `pending` reports whether an unexpired code is outstanding, so the UI can reopen on the code box after a reload. Always scoped to the caller.

### `notifications.subscriptions.create`

`POST /api/notifications/subscriptions`

Create subscription

Body: application/json (free-form — pass with `--data`)

### `notifications.subscriptions.delete`

`DELETE /api/notifications/subscriptions`

Delete subscriptions

**Destructive** — needs `--yes` against a non-local base URL.

### `notifications.subscriptions.list`

`GET /api/notifications/subscriptions`

List subscriptions

### `notifications.unsubscribe.create`

`POST /api/notifications/unsubscribe`

Create unsubscribe

Body: application/json (free-form — pass with `--data`)

### `notifications.unsubscribe.list`

`GET /api/notifications/unsubscribe`

List unsubscribe

### `notifications.update`

`PATCH /api/notifications`

Update notification state

Body (application/json):
  - `action` (any, required)
  - `projectRef` (string, required)
  - `notificationId` (string, required)
  - `unread` (boolean, required)
  - `action` (any, required)
  - `projectRef` (string, required)
  - `notificationId` (string, required)
  - `snoozed` (boolean, required)
  - `action` (any, required)
  - `projectRef` (string, required)
  - `notificationId` (string, required)
  - `action` (any, required)

### `sidebar.unread-sources.list`

`GET /api/sidebar/unread-sources`

Where the Messages and Email Inbox unread items are

The chat threads (with links) and mailboxes holding the unread items the Messages and Email Inbox sidebar pills count. Uses the same predicates as /api/sidebar/counts, so the totals match the pills. Cross-workspace, like the pills (chat threads and mirrored mail are per-user). Never cached.

# Settings

50 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `blueprints.apply.create` | POST | `/api/blueprints/{id}/apply` | Apply selected items, created switched off |
| `blueprints.create` | POST | `/api/blueprints` | Draft a blueprint from an operating prompt (one billed planning call) |
| `blueprints.get` | GET | `/api/blueprints/{id}` | A blueprint with live blockers, apply state, diff and cost totals |
| `blueprints.list` | GET | `/api/blueprints` | List blueprints and what drafting one costs |
| `blueprints.revert.create` | POST | `/api/blueprints/{id}/revert` | Revert what a blueprint applied, as a set |
| `blueprints.update` | PATCH | `/api/blueprints/{id}` | Toggle, tick "turn on now" or edit items |
| `settings.account.delete` | DELETE | `/api/settings/account` | Delete user account |
| `settings.api-keys.create` | POST | `/api/settings/api-keys` | (undocumented route — params unknown, pass them explicitly) |
| `settings.api-keys.delete` | DELETE | `/api/settings/api-keys/{p1}` | (undocumented route — params unknown, pass them explicitly) |
| `settings.api-keys.list` | GET | `/api/settings/api-keys` | (undocumented route — params unknown, pass them explicitly) |
| `settings.billing.auto-topup.list` | GET | `/api/settings/billing/auto-topup` | Get auto top-up |
| `settings.billing.auto-topup.set` | PUT | `/api/settings/billing/auto-topup` | Update auto top-up |
| `settings.billing.balance.list` | GET | `/api/settings/billing/balance` | List balance |
| `settings.billing.cancel.create` | POST | `/api/settings/billing/cancel` | Create cancel |
| `settings.billing.invoices.list` | GET | `/api/settings/billing/invoices` | List invoices |
| `settings.billing.invoices.pdf.list` | GET | `/api/settings/billing/invoices/{id}/pdf` | List pdf |
| `settings.billing.order.create` | POST | `/api/settings/billing/order` | Create order |
| `settings.billing.payment-method.create` | POST | `/api/settings/billing/payment-method` | Create payment method |
| `settings.billing.payment-method.delete` | DELETE | `/api/settings/billing/payment-method` | Remove saved card |
| `settings.billing.payment-method.list` | GET | `/api/settings/billing/payment-method` | List payment method |
| `settings.billing.profile.list` | GET | `/api/settings/billing/profile` | List profile |
| `settings.billing.profile.set` | PUT | `/api/settings/billing/profile` | Update profile |
| `settings.billing.switch.create` | POST | `/api/settings/billing/switch` | Switch to the Pay As You Go plan |
| `settings.billing.team.list` | GET | `/api/settings/billing/team` | (undocumented route — params unknown, pass them explicitly) |
| `settings.billing.team.update` | PATCH | `/api/settings/billing/team` | (undocumented route — params unknown, pass them explicitly) |
| `settings.billing.tiers.list` | GET | `/api/settings/billing/tiers` | List tiers |
| `settings.billing.topup.create` | POST | `/api/settings/billing/topup` | (undocumented route — params unknown, pass them explicitly) |
| `settings.billing.trial.list` | GET | `/api/settings/billing/trial` | List trial |
| `settings.extension-shield.detections.create` | POST | `/api/settings/extension-shield/detections` | Record a browser-extension detection for the caller |
| `settings.extension-shield.list` | GET | `/api/settings/extension-shield` | Is Extension Shield on for this workspace |
| `settings.god-mode-setup.create` | POST | `/api/settings/god-mode-setup` | Send a member an in-app setup reminder |
| `settings.god-mode-setup.list` | GET | `/api/settings/god-mode-setup` | The God Mode setup checklist (live status of everything the deal machine needs) |
| `settings.list` | GET | `/api/settings` | Get user settings bundle |
| `settings.password.create` | POST | `/api/settings/password` | Change password |
| `settings.password.list` | GET | `/api/settings/password` | Whether the account has a password set |
| `settings.privacy.create` | POST | `/api/settings/privacy` | Create privacy |
| `settings.privacy.data-requests.download.list` | GET | `/api/settings/privacy/data-requests/{requestId}/download` | Download a completed data-export request |
| `settings.privacy.list` | GET | `/api/settings/privacy` | List privacy |
| `settings.security.create` | POST | `/api/settings/security` | Security action (e.g. revoke session) |
| `settings.security.list` | GET | `/api/settings/security` | Get security info (active sessions) |
| `settings.send-limits.list` | GET | `/api/settings/send-limits` | Outbound send capacity, and whether a target is sustainable |
| `settings.send-limits.set` | PUT | `/api/settings/send-limits` | Set a mailbox's daily send cap, or the workspace default |
| `settings.sessions.delete` | DELETE | `/api/settings/sessions/{sessionId}` | Delete session |
| `settings.sessions.list` | GET | `/api/settings/sessions` | List sessions |
| `settings.trash.create` | POST | `/api/settings/trash` | Restore a trashed item |
| `settings.trash.delete` | DELETE | `/api/settings/trash` | Permanently delete a trashed item |
| `settings.trash.list` | GET | `/api/settings/trash` | List trashed items |
| `settings.update` | PATCH | `/api/settings` | Update user settings |
| `settings.workspace.delete` | DELETE | `/api/settings/workspace` | Delete workspace (owner only) |
| `settings.workspace.transfer.create` | POST | `/api/settings/workspace/transfer` | (undocumented route — params unknown, pass them explicitly) |

---

### `blueprints.apply.create`

`POST /api/blueprints/{id}/apply`

Apply selected items, created switched off

Owner/admin only. Creates each item through its existing write path, DISARMED: schedules paused, rules and cadences off, meeting series disarmed, campaigns not started, switches unchanged. An item in `turnOn` is switched on only when `confirm[key]` equals the monthly cost the server computes now (null for usage-dependent items) — otherwise 409 `turn_on_unconfirmed` and nothing is applied. Idempotent per item key; failures are recorded per item (`partial`) and retried by applying again.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `itemKeys` (string[])
  - `turnOn` (string[])
  - `confirm` (object)

### `blueprints.create`

`POST /api/blueprints`

Draft a blueprint from an operating prompt (one billed planning call)

Owner/admin only. ONE Sonnet planning call, billed to the signed-in user (402 `insufficient_credits` when they cannot cover the `blueprint_draft` floor). Every proposed item is validated against the real registries (automation triggers/actions, agent switches, org and cadence templates, models); anything that does not validate is listed as unsupported, never kept. A prompt over 40,000 characters is clipped and the plan says so. With `blueprintId` the plan becomes that blueprint's next version. Creates nothing in the workspace.

Body (application/json):
  - `prompt` (string, required)
  - `blueprintId` (string<uuid>)
  - `title` (string)

### `blueprints.get`

`GET /api/blueprints/{id}`

A blueprint with live blockers, apply state, diff and cost totals

Owner/admin only. The plan (items grouped, each with its quoted source sentence, monthly cost if turned on, compliance notes and LIVE blockers from the God Mode setup checklist), the apply ledger's state per item, the diff of the plan against what is applied (added / changed / removed — removal is only ever proposed), totals, applies and versions. `no-store`.

Path params (positional, in order):
  - `id`

### `blueprints.list`

`GET /api/blueprints`

List blueprints and what drafting one costs

Owner/admin only. A Blueprint is an operating prompt turned into one reviewable plan of items mapped to existing capabilities (docs/agent-notes/blueprint.md). Returns the workspace's blueprints, newest first, and `draftEstimateCredits` — the planner call's price for a prompt of `promptChars` characters. `no-store`.

Query:
  - `promptChars` (integer) — Prompt length to price the draft for (default 8000).

### `blueprints.revert.create`

`POST /api/blueprints/{id}/revert`

Revert what a blueprint applied, as a set

Owner/admin only. `{applyId}` reverts one apply, `{itemKeys}` specific items, neither everything still live — newest first. Removes what the blueprint created and restores prior switch values, but KEEPS (and reports) anything changed since the apply: an edited schedule, an armed meeting series, a cadence with enrollments, a switch someone changed back.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `applyId` (string<uuid>)
  - `itemKeys` (string[])

### `blueprints.update`

`PATCH /api/blueprints/{id}`

Toggle, tick "turn on now" or edit items

Owner/admin only. Every params edit is re-validated by the same validator as a draft and re-priced; an item's key never changes. `expectedUpdatedAt` (the blueprint's `updatedAt`) is required; a stale one is 409 `blueprint_stale`.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `expectedUpdatedAt` (string, required)
  - `edits` (object[], required)

### `settings.account.delete`

`DELETE /api/settings/account`

Delete user account

**Destructive** — needs `--yes` against a non-local base URL.

### `settings.api-keys.create`

`POST /api/settings/api-keys`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `settings.api-keys.delete`

`DELETE /api/settings/api-keys/{p1}`

(undocumented route — params unknown, pass them explicitly)

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `settings.api-keys.list`

`GET /api/settings/api-keys`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `settings.billing.auto-topup.list`

`GET /api/settings/billing/auto-topup`

Get auto top-up

Owner-only. The auto top-up setting (buy a credit pack on the saved card when the personal balance drops below a threshold, never past a monthly dollar limit), the saved card, this UTC month's auto top-up spend, recent attempts and the allowed ranges.

### `settings.billing.auto-topup.set`

`PUT /api/settings/billing/auto-topup`

Update auto top-up

Owner-only. Saves the setting. Turning it on requires a card saved at a top-up checkout (POST /api/settings/billing/topup with saveCard true); otherwise 409.

Body (application/json):
  - `enabled` (boolean, required)
  - `thresholdCredits` (integer, required)
  - `packId` (string, required) — one of: `topup_1000`, `topup_5000`, `topup_10000`
  - `monthlyLimitUsd` (number, required)

### `settings.billing.balance.list`

`GET /api/settings/billing/balance`

List balance

### `settings.billing.cancel.create`

`POST /api/settings/billing/cancel`

Create cancel

Body: application/json (free-form — pass with `--data`)

### `settings.billing.invoices.list`

`GET /api/settings/billing/invoices`

List invoices

### `settings.billing.invoices.pdf.list`

`GET /api/settings/billing/invoices/{id}/pdf`

List pdf

Path params (positional, in order):
  - `id`

### `settings.billing.order.create`

`POST /api/settings/billing/order`

Create order

Body: application/json (free-form — pass with `--data`)

### `settings.billing.payment-method.create`

`POST /api/settings/billing/payment-method`

Create payment method

Returns a short-lived cred.diy (Stripe) page for updating the card the caller's plan subscription renews on. The subscription is looked up on the cred user that holds it (the workspace pool for a pool-funded plan). Optional body field `returnUrl` must be on this app's origin.

Body: application/json (free-form — pass with `--data`)

### `settings.billing.payment-method.delete`

`DELETE /api/settings/billing/payment-method`

Remove saved card

Forgets the card cred.diy saved for auto top-up and turns auto top-up off (the setting first, so a racing trigger cannot charge it).

**Destructive** — needs `--yes` against a non-local base URL.

### `settings.billing.payment-method.list`

`GET /api/settings/billing/payment-method`

List payment method

### `settings.billing.profile.list`

`GET /api/settings/billing/profile`

List profile

### `settings.billing.profile.set`

`PUT /api/settings/billing/profile`

Update profile

Body: application/json (free-form — pass with `--data`)

### `settings.billing.switch.create`

`POST /api/settings/billing/switch`

Switch to the Pay As You Go plan

Owner-only. Moves the workspace owner's plan onto the credits-only tier (no subscription, no seat fee, no included credits). Requires a completed credit purchase in the workspace; otherwise answers 402 with code `credits_purchase_required`. Leaving a paid plan this way is prorated like any other downgrade.

Body (application/json):
  - `planName` (string, required) — one of: `Pay As You Go Plan`

### `settings.billing.team.list`

`GET /api/settings/billing/team`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `settings.billing.team.update`

`PATCH /api/settings/billing/team`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `settings.billing.tiers.list`

`GET /api/settings/billing/tiers`

List tiers

### `settings.billing.topup.create`

`POST /api/settings/billing/topup`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `settings.billing.trial.list`

`GET /api/settings/billing/trial`

List trial

### `settings.extension-shield.detections.create`

`POST /api/settings/extension-shield/detections`

Record a browser-extension detection for the caller

Sent by the in-app extension guard once per detected extension per page load, so support can see what a member's browser injected without asking them to open DevTools. Filed under the caller's own user and workspace (never anything in the body) in `app_extension_detections`; a repeat from the same browser bumps `seen_count`. Identity only — the element's tag/id/class and the extension origin, never page contents. `name` must be one the guard can produce (a known marker name or "Unidentified browser extension"); `listedAs` is derived server-side from it.

Body (application/json):
  - `name` (string, required)
  - `origin` (string) — `chrome-extension://<id>`-style origin, when the match carried one.
  - `tag` (string)
  - `id` (string)
  - `class` (string)
  - `shieldDevice` (boolean)
  - `warningSuppressed` (boolean)

### `settings.extension-shield.list`

`GET /api/settings/extension-shield`

Is Extension Shield on for this workspace

Whether the workspace has the `extension_shield_enabled` security policy turned on. Read-only and visible to every member — the shield is a client-side containment mode each member's browser runs, not an admin secret. Writing the policy goes through `POST /api/admin/security/policies` (admin only).

### `settings.god-mode-setup.create`

`POST /api/settings/god-mode-setup`

Send a member an in-app setup reminder

Admin only. Writes ONE in-app alert (dashboard + bell) asking an active member of this workspace to connect their own account. Never emails. Deduped per (member, item) for 24 hours — a repeat returns `created: false` rather than claiming a reminder was sent.

Body (application/json):
  - `userId` (string<uuid>, required)
  - `itemKey` (string, required) — one of: `google_accounts`, `angelsend`

### `settings.god-mode-setup.list`

`GET /api/settings/god-mode-setup`

The God Mode setup checklist (live status of everything the deal machine needs)

Read-only. Each item carries a status (`ok`, `warn`, `missing`, `unknown` = could not check — never a pass, `info` = optional), a plain-language reason, and the actions that fix it (links to existing pages and OAuth starts, or an inline fix that calls an existing write route). Owners and admins get the whole workspace; any other member gets ONLY their own connections (their Google accounts and AngelSend) — another member's connection rows are never read for them. Includes a live DNS check of the sending domain's SPF/DKIM/DMARC. `no-store`.

Query:
  - `target` (integer) — Daily send volume to plan sending capacity against. Omit for a plain capacity report.

### `settings.list`

`GET /api/settings`

Get user settings bundle

### `settings.password.create`

`POST /api/settings/password`

Change password

Body (application/json):
  - `currentPassword` (string, required)
  - `newPassword` (string, required)
  - `confirmPassword` (string, required)

### `settings.password.list`

`GET /api/settings/password`

Whether the account has a password set

Returns `{ hasPassword }`. False for OAuth-only accounts, which use this to offer setting a password without a current one.

### `settings.privacy.create`

`POST /api/settings/privacy`

Create privacy

Body: application/json (free-form — pass with `--data`)

### `settings.privacy.data-requests.download.list`

`GET /api/settings/privacy/data-requests/{requestId}/download`

Download a completed data-export request

Returns the stored export as a JSON attachment. Only valid for requests of type export that have completed.

Path params (positional, in order):
  - `requestId`

### `settings.privacy.list`

`GET /api/settings/privacy`

List privacy

### `settings.security.create`

`POST /api/settings/security`

Security action (e.g. revoke session)

### `settings.security.list`

`GET /api/settings/security`

Get security info (active sessions)

### `settings.send-limits.list`

`GET /api/settings/send-limits`

Outbound send capacity, and whether a target is sustainable

Plan the outbound mailbox pool against a daily target. Returns every mailbox that could carry load (a configured limit row, a connected mail provider, or queued mail in the last 30 days), what the pool can send today after warm-up ramps, what it reaches at steady state and when, what the underlying providers safely support, and how many more mailboxes a target needs. The distinction this exists to make: raising a cap is one setting and takes a second, but SUSTAINING the volume is a property of the pool. A single mailbox configured at 1,000/day is refused by Google at roughly half that, and the reputation damage outlasts the campaign — so 1,000/day is planned as four mailboxes, not one turned up. Member-level: anyone planning a campaign needs these numbers and none of them are sensitive.

Query:
  - `target` (integer) — Daily volume to plan against. Omit for a plain capacity report.

### `settings.send-limits.set`

`PUT /api/settings/send-limits`

Set a mailbox's daily send cap, or the workspace default

Admin only. Omit `userId` to set the workspace default that every mailbox without its own row inherits. This ARMS higher unattended sending — the scheduled-email cron defers against this number every minute, so raising it immediately releases mail that was being held back. Prefer a warm-up ramp (`warmupStart` + `warmupFloor` + `warmupStep`) over a straight raise on any identity not already sending at the new volume: a domain that jumps to its cap on day one gets filtered, and the fix for that is a new domain rather than a smaller number next week.

Body (application/json):
  - `dailyCap` (integer, required)
  - `userId` (string) — Must be an active member of this workspace. Omit for the workspace default.
  - `warmupStart` (string) — YYYY-MM-DD the ramp begins; null clears the ramp.
  - `warmupFloor` (integer) — Day-one ceiling. Default 50.
  - `warmupStep` (integer) — Added per day until dailyCap. Default 25.

### `settings.sessions.delete`

`DELETE /api/settings/sessions/{sessionId}`

Delete session

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `sessionId`

### `settings.sessions.list`

`GET /api/settings/sessions`

List sessions

### `settings.trash.create`

`POST /api/settings/trash`

Restore a trashed item

Body (application/json):
  - `action` (any)
  - `trashId` (string)

### `settings.trash.delete`

`DELETE /api/settings/trash`

Permanently delete a trashed item

**Destructive** — needs `--yes` against a non-local base URL.

Body (application/json):
  - `trashId` (string)

### `settings.trash.list`

`GET /api/settings/trash`

List trashed items

### `settings.update`

`PATCH /api/settings`

Update user settings

A PATCH that touches the workspace half (`workspace`, `projectTags`, `projectTypes`) is admin-only and must name the workspace its form was loaded from as `workspaceId` (GET returns it): 409 `bundle_workspace_mismatch` when it differs, 400 `bundle_workspace_required` when a browser session omits it. The per-user half (`notifications`, `plan`, `devices`) is not gated.

Body (application/json):
  - `workspaceId` (string) — The workspace the settings were loaded from. Required for browser sessions writing workspace settings.

### `settings.workspace.delete`

`DELETE /api/settings/workspace`

Delete workspace (owner only)

**Destructive** — needs `--yes` against a non-local base URL.

### `settings.workspace.transfer.create`

`POST /api/settings/workspace/transfer`

(undocumented route — params unknown, pass them explicitly)

**Destructive** — needs `--yes` against a non-local base URL.

_Not in either OpenAPI spec — flags are passed through unvalidated._

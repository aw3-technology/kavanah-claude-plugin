# AI Agent

106 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `ai-agent.action-policies.delete` | DELETE | `/api/ai-agent/action-policies` | Delete an agent action policy (admin) |
| `ai-agent.action-policies.list` | GET | `/api/ai-agent/action-policies` | List agent action policies and the category catalog (admin) |
| `ai-agent.action-policies.set` | PUT | `/api/ai-agent/action-policies` | Bulk upsert agent action policies (admin) |
| `ai-agent.activity-report.list` | GET | `/api/ai-agent/activity-report` | Agent activity/self-report — totals, categories, top tools, approvals (admin) |
| `ai-agent.activity.list` | GET | `/api/ai-agent/activity` | Agent activity timeline — individual ledger rows (admin) |
| `ai-agent.admin.conversations.get` | GET | `/api/ai-agent/admin/conversations/{p1}` | (undocumented route — params unknown, pass them explicitly) |
| `ai-agent.admin.conversations.list` | GET | `/api/ai-agent/admin/conversations` | (undocumented route — params unknown, pass them explicitly) |
| `ai-agent.approvals.create` | POST | `/api/ai-agent/approvals/{approvalId}` | Approve or deny a parked agent action (admin) |
| `ai-agent.approvals.get` | GET | `/api/ai-agent/approvals/{approvalId}` | One parked action, in full - the reply desk (admin) |
| `ai-agent.approvals.list` | GET | `/api/ai-agent/approvals` | Global agent approvals inbox (admin) |
| `ai-agent.attachments.create` | POST | `/api/ai-agent/attachments` | Create attachment |
| `ai-agent.attachments.delete` | DELETE | `/api/ai-agent/attachments` | Delete attachments |
| `ai-agent.attachments.list` | GET | `/api/ai-agent/attachments` | List attachments |
| `ai-agent.audit.list` | GET | `/api/ai-agent/audit` | List audit |
| `ai-agent.chat-runs.get` | GET | `/api/ai-agent/chat-runs/{p1}` | (undocumented route — params unknown, pass them explicitly) |
| `ai-agent.config.list` | GET | `/api/ai-agent/config` | List config |
| `ai-agent.config.update` | PATCH | `/api/ai-agent/config` | Update config |
| `ai-agent.conversations.away.create` | POST | `/api/ai-agent/conversations/{id}/away` | Report the chat client away or back |
| `ai-agent.conversations.create` | POST | `/api/ai-agent/conversations` | Create conversation |
| `ai-agent.conversations.delete` | DELETE | `/api/ai-agent/conversations/{id}` | Delete conversation |
| `ai-agent.conversations.export.list` | GET | `/api/ai-agent/conversations/{id}/export` | List export |
| `ai-agent.conversations.get` | GET | `/api/ai-agent/conversations/{id}` | Fetch conversation |
| `ai-agent.conversations.list` | GET | `/api/ai-agent/conversations` | List conversations |
| `ai-agent.conversations.search.list` | GET | `/api/ai-agent/conversations/search` | Search conversations |
| `ai-agent.conversations.update` | PATCH | `/api/ai-agent/conversations/{id}` | Update conversation |
| `ai-agent.create` | POST | `/api/ai-agent` | Send a chat message to the AI agent |
| `ai-agent.credits-meter.list` | GET | `/api/ai-agent/credits-meter` | Get the chat credits meter |
| `ai-agent.custom-tools.create` | POST | `/api/ai-agent/custom-tools` | Create custom tool |
| `ai-agent.custom-tools.delete` | DELETE | `/api/ai-agent/custom-tools/{id}` | Delete custom tool |
| `ai-agent.custom-tools.list` | GET | `/api/ai-agent/custom-tools` | List custom tools |
| `ai-agent.custom-tools.update` | PATCH | `/api/ai-agent/custom-tools/{id}` | Update custom tool |
| `ai-agent.escalation-policy.list` | GET | `/api/ai-agent/escalation-policy` | Get the workspace agent escalation policy (admin) |
| `ai-agent.escalation-policy.set` | PUT | `/api/ai-agent/escalation-policy` | Update the workspace agent escalation policy (admin) |
| `ai-agent.feedback.analytics.list` | GET | `/api/ai-agent/feedback/analytics` | List analytics |
| `ai-agent.feedback.create` | POST | `/api/ai-agent/feedback` | Create feedback |
| `ai-agent.feedback.delete` | DELETE | `/api/ai-agent/feedback` | Delete feedback |
| `ai-agent.guardrails.create` | POST | `/api/ai-agent/guardrails` | Create an agent guardrail rule (admin) |
| `ai-agent.guardrails.delete` | DELETE | `/api/ai-agent/guardrails` | Delete an agent guardrail rule (admin) |
| `ai-agent.guardrails.list` | GET | `/api/ai-agent/guardrails` | List agent guardrail rules and the catalog (admin) |
| `ai-agent.guardrails.update` | PATCH | `/api/ai-agent/guardrails` | Update an agent guardrail rule (admin) |
| `ai-agent.jobs.get` | GET | `/api/ai-agent/jobs/{id}` | Fetch job |
| `ai-agent.jobs.list` | GET | `/api/ai-agent/jobs` | List jobs |
| `ai-agent.mention.create` | POST | `/api/ai-agent/mention` | Ask the AI agent about context you supply |
| `ai-agent.org-templates.apply.create` | POST | `/api/ai-agent/org-templates/{key}/apply` | Apply an org template |
| `ai-agent.org-templates.list` | GET | `/api/ai-agent/org-templates` | List org templates (whole AI organisations with standing meetings) |
| `ai-agent.org-templates.preview.create` | POST | `/api/ai-agent/org-templates/{key}/preview` | Preview applying an org template in this workspace |
| `ai-agent.outcomes.create` | POST | `/api/ai-agent/outcomes` | Cancel a pending outcome check (admin) |
| `ai-agent.outcomes.list` | GET | `/api/ai-agent/outcomes` | Agent outcome checks and hit rate (admin) |
| `ai-agent.persona-departments.list` | GET | `/api/ai-agent/persona-departments` | (undocumented route — params unknown, pass them explicitly) |
| `ai-agent.personas.avatar.generate.create` | POST | `/api/ai-agent/personas/avatar/generate` | (undocumented route — params unknown, pass them explicitly) |
| `ai-agent.personas.create` | POST | `/api/ai-agent/personas` | Create an AI agent persona |
| `ai-agent.personas.delete` | DELETE | `/api/ai-agent/personas/{id}` | Delete an AI agent persona |
| `ai-agent.personas.departments.list` | GET | `/api/ai-agent/personas/{p1}/departments` | (undocumented route — params unknown, pass them explicitly) |
| `ai-agent.personas.departments.set` | PUT | `/api/ai-agent/personas/{p1}/departments` | (undocumented route — params unknown, pass them explicitly) |
| `ai-agent.personas.generate.create` | POST | `/api/ai-agent/personas/generate` | Draft a persona from a natural-language description |
| `ai-agent.personas.list` | GET | `/api/ai-agent/personas` | List AI agent personas (AI employees) |
| `ai-agent.personas.members.list` | GET | `/api/ai-agent/personas/{p1}/members` | (undocumented route — params unknown, pass them explicitly) |
| `ai-agent.personas.members.set` | PUT | `/api/ai-agent/personas/{p1}/members` | (undocumented route — params unknown, pass them explicitly) |
| `ai-agent.personas.org-chart.list` | GET | `/api/ai-agent/personas/org-chart` | The AI-employee org chart |
| `ai-agent.personas.update` | PATCH | `/api/ai-agent/personas/{id}` | Update an AI agent persona |
| `ai-agent.personas.week.list` | GET | `/api/ai-agent/personas/week` | Each AI employee's last seven days |
| `ai-agent.preferences.list` | GET | `/api/ai-agent/preferences` | List preferences |
| `ai-agent.preferences.update` | PATCH | `/api/ai-agent/preferences` | Update preferences |
| `ai-agent.schedules.create` | POST | `/api/ai-agent/schedules` | (undocumented route — params unknown, pass them explicitly) |
| `ai-agent.schedules.delete` | DELETE | `/api/ai-agent/schedules/{p1}` | (undocumented route — params unknown, pass them explicitly) |
| `ai-agent.schedules.list` | GET | `/api/ai-agent/schedules` | (undocumented route — params unknown, pass them explicitly) |
| `ai-agent.schedules.runs.list` | GET | `/api/ai-agent/schedules/runs` | List scheduled autonomous agent runs |
| `ai-agent.schedules.update` | PATCH | `/api/ai-agent/schedules/{p1}` | (undocumented route — params unknown, pass them explicitly) |
| `ai-agent.share.create` | POST | `/api/ai-agent/share` | Share an agent answer or conversation |
| `ai-agent.share.get` | GET | `/api/ai-agent/share/{id}` | Read a shared agent snapshot |
| `ai-agent.skipped.list` | GET | `/api/ai-agent/skipped` | What Kavanah skipped in the last 24 hours, and why |
| `ai-agent.slack-managers.create` | POST | `/api/ai-agent/slack-managers` | Create an AI Slack manager (admin) |
| `ai-agent.slack-managers.delete` | DELETE | `/api/ai-agent/slack-managers/{id}` | Delete an AI Slack manager and its reply log (admin) |
| `ai-agent.slack-managers.list` | GET | `/api/ai-agent/slack-managers` | List AI Slack managers, with their last 7 days of answers (admin) |
| `ai-agent.slack-managers.update` | PATCH | `/api/ai-agent/slack-managers/{id}` | Update an AI Slack manager (admin) |
| `ai-agent.tools.execute.create` | POST | `/api/ai-agent/tools/{name}/execute` | Execute one agent tool by name |
| `ai-agent.tools.list` | GET | `/api/ai-agent/tools` | List the agent tools the caller may execute |
| `ai-agent.twin.create` | POST | `/api/ai-agent/twin` | (undocumented route — params unknown, pass them explicitly) |
| `ai-agent.twin.delete` | DELETE | `/api/ai-agent/twin` | (undocumented route — params unknown, pass them explicitly) |
| `ai-agent.twin.grounding.create` | POST | `/api/ai-agent/twin/grounding` | (undocumented route — params unknown, pass them explicitly) |
| `ai-agent.twin.grounding.delete` | DELETE | `/api/ai-agent/twin/grounding` | (undocumented route — params unknown, pass them explicitly) |
| `ai-agent.twin.grounding.list` | GET | `/api/ai-agent/twin/grounding` | (undocumented route — params unknown, pass them explicitly) |
| `ai-agent.twin.list` | GET | `/api/ai-agent/twin` | (undocumented route — params unknown, pass them explicitly) |
| `ai-agent.twin.reply.create` | POST | `/api/ai-agent/twin/reply` | (undocumented route — params unknown, pass them explicitly) |
| `ai-agent.undo.create` | POST | `/api/ai-agent/undo` | Create undo |
| `ai-agent.usage-breakdown.list` | GET | `/api/ai-agent/usage-breakdown` | (undocumented route — params unknown, pass them explicitly) |
| `meeting-twin.external.consents.create` | POST | `/api/meeting-twin/external/consents` | Withdraw consent to the caller's cloned voice or video avatar |
| `meeting-twin.external.face.create` | POST | `/api/meeting-twin/external/face` | Start / finish the video avatar upload |
| `meeting-twin.external.face.list` | GET | `/api/meeting-twin/external/face` | The caller's video avatar training status |
| `meeting-twin.external.face.part.create` | POST | `/api/meeting-twin/external/face/part` | Upload one ≤4 MB slice of the avatar training video |
| `meeting-twin.external.sessions.create` | POST | `/api/meeting-twin/external/sessions` | Send the caller's own twin or notetaker to a meeting |
| `meeting-twin.external.sessions.delete` | DELETE | `/api/meeting-twin/external/sessions/{id}` | Make a twin / notetaker leave now |
| `meeting-twin.external.sessions.get` | GET | `/api/meeting-twin/external/sessions/{id}` | One twin / notetaker meeting (live status, transcript, summary) |
| `meeting-twin.external.sessions.list` | GET | `/api/meeting-twin/external/sessions` | The caller's twin / notetaker meetings |
| `meeting-twin.external.setup.list` | GET | `/api/meeting-twin/external/setup` | The caller's AI twin & notetaker setup state |
| `meeting-twin.external.setup.set` | PUT | `/api/meeting-twin/external/setup` | Update the caller's own twin profile |
| `meeting-twin.external.test.create` | POST | `/api/meeting-twin/external/test` | Test my twin (no meeting) |
| `meeting-twin.external.vendors.test.create` | POST | `/api/meeting-twin/external/vendors/test` | Test a meeting-twin vendor connection |
| `meeting-twin.external.voice-clone.create` | POST | `/api/meeting-twin/external/voice-clone` | Clone the caller's own voice (with recorded consent) |
| `meeting-twin.external.voices.list` | GET | `/api/meeting-twin/external/voices` | Voices the caller may give their twin |
| `water-cooler.threads.create` | POST | `/api/water-cooler/threads` | Start a Water Cooler conversation |
| `water-cooler.threads.delete` | DELETE | `/api/water-cooler/threads/{id}` | Delete a thread (starter or admin) |
| `water-cooler.threads.get` | GET | `/api/water-cooler/threads/{id}` | Get a thread with its messages |
| `water-cooler.threads.list` | GET | `/api/water-cooler/threads` | List Water Cooler threads |
| `water-cooler.threads.promote.create` | POST | `/api/water-cooler/threads/{id}/promote` | Turn the thread's close into a task |
| `water-cooler.threads.reply.create` | POST | `/api/water-cooler/threads/{id}/reply` | Reply as a human (re-wakes the room when idle) |

---

### `ai-agent.action-policies.delete`

`DELETE /api/ai-agent/action-policies`

Delete an agent action policy (admin)

**Destructive** — needs `--yes` against a non-local base URL.

Query:
  - `id` (string, required)

### `ai-agent.action-policies.list`

`GET /api/ai-agent/action-policies`

List agent action policies and the category catalog (admin)

Per-category policy governing risky agent actions. Categories are external_send, finance, destructive, membership, deploy, external_write. No row for a category means "park for approval" (fail closed).

### `ai-agent.action-policies.set`

`PUT /api/ai-agent/action-policies`

Bulk upsert agent action policies (admin)

Body (application/json):
  - `policies` (object[], required)

### `ai-agent.activity-report.list`

`GET /api/ai-agent/activity-report`

Agent activity/self-report — totals, categories, top tools, approvals (admin)

Query:
  - `days` (integer) — Lookback window in days (clamped to 90).

### `ai-agent.activity.list`

`GET /api/ai-agent/activity`

Agent activity timeline — individual ledger rows (admin)

One row per agent write, newest first. This is the row-level companion to /api/ai-agent/activity-report, which returns only aggregates ("47 actions, 3 approvals") and so answers how much the agent did but never what. Admin-only: the ledger spans every member's agent use. Opt-in — returns 403 `agent_oversight_disabled` unless the workspace has enabled the activity ledger viewer. The ledger keeps RECORDING either way; the flag only governs whether the workspace has asked to see it. Paginates by keyset cursor on `created_at` (`before`), which is stable under concurrent writes where an offset would not be. `next_cursor` is null on the last page. Unknown filter values are ignored rather than rejected, so a stale bookmark shows the unfiltered timeline.

Query:
  - `limit` (integer)
  - `before` (string<date-time>) — Keyset cursor — return rows older than this ISO timestamp.
  - `status` (string) — one of: `executed`, `parked`, `blocked`, `failed`, `undone`
  - `run_kind` (string) — one of: `interactive`, `autonomous`, `scheduled`
  - `category` (string) — Action-policy category (external_send, finance, destructive, …).
  - `user_id` (string)

### `ai-agent.admin.conversations.get`

`GET /api/ai-agent/admin/conversations/{p1}`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `ai-agent.admin.conversations.list`

`GET /api/ai-agent/admin/conversations`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `ai-agent.approvals.create`

`POST /api/ai-agent/approvals/{approvalId}`

Approve or deny a parked agent action (admin)

Resolve a parked action from the global inbox — the task-independent sibling of /api/tasks/{id}/agent-run/approvals/{approvalId}, and the only way to resolve an approval from an event-driven run. Approving means EXECUTING the action (sending the email, moving the money), and the actions that park are exactly the dangerous ones — so this requires an admin, which is stricter than the task-scoped route's `tasks:edit`. Shares the approvals service with the task-scoped route, so both re-check expiry, guardrails, and policy at resolve time rather than trusting the decision made when the action was parked.

Path params (positional, in order):
  - `approvalId`

Body (application/json):
  - `decision` (string, required) — one of: `approve`, `deny`
  - `edits` (object) — Reply desk only, and only with `decision: approve`: a principal's rewrite of the draft. Only the TEXT may be changed (`subject`/`body`, plus `html` for an AngelSend draft); naming any other field - a recipient above all - is REFUSED with 400 rather than ignored. The edited text is what is sent, `tool_input` keeps the agent's draft, and the ledger row carries both.
  - `edits.subject` (string)
  - `edits.body` (string)
  - `edits.html` (string)
  - `reviewed_digest` (string) — `approval.draft_digest` from GET on this path. Required alongside `edits`; a mismatch is 409, because an edit is consent to one specific message.

### `ai-agent.approvals.get`

`GET /api/ai-agent/approvals/{approvalId}`

One parked action, in full - the reply desk (admin)

The inbox list deliberately omits `tool_input`; this is where an admin reads it, because approving means executing it and nobody should approve what they cannot see. For outbound mail this is the REPLY DESK view: the draft, the inbound message it answers, the rest of that thread, the correspondent's Deal Room history, and the mailbox the reply would send from (the RUN's user, not the approver's). Everything is read from what Kavanah already mirrored - no provider call, so reviewing a reply never depends on, or spends, the mailbox owner's live credential. `approval.draft_digest` fingerprints the parked arguments as they stand right now. Echo it back as `reviewed_digest` when approving; an edited approval REQUIRES it, so an edit can never land on a draft that changed after it was read. Admin-only, like resolving one.

Path params (positional, in order):
  - `approvalId`

### `ai-agent.approvals.list`

`GET /api/ai-agent/approvals`

Global agent approvals inbox (admin)

Every action the agent has parked for a human, workspace-wide, plus the pending count. This is the only route that can surface an approval from an event-driven run (a new email, a PR), which has no task to navigate to. Deliberately NOT gated on the oversight opt-in for that reason — gating it would strand those approvals in workspaces that had not opted in. Admin-only. The rows enumerate every outbound email and payment the agent is holding; `tool_input` is stripped from the payload, but the inventory itself is privileged and only admins can resolve an approval anyway.

Query:
  - `limit` (integer)

### `ai-agent.attachments.create`

`POST /api/ai-agent/attachments`

Create attachment

Body: application/json (free-form — pass with `--data`)

### `ai-agent.attachments.delete`

`DELETE /api/ai-agent/attachments`

Delete attachments

**Destructive** — needs `--yes` against a non-local base URL.

### `ai-agent.attachments.list`

`GET /api/ai-agent/attachments`

List attachments

### `ai-agent.audit.list`

`GET /api/ai-agent/audit`

List audit

### `ai-agent.chat-runs.get`

`GET /api/ai-agent/chat-runs/{p1}`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `ai-agent.config.list`

`GET /api/ai-agent/config`

List config

### `ai-agent.config.update`

`PATCH /api/ai-agent/config`

Update config

Partial update of the workspace agent config. `background_model` sets the default model for unattended runs (schedules, task runs, exec meetings): a model id from `model_options`, `"auto"` (a small router model grades each run and picks the cheapest model that fits), or null to use `model`. `auto_optimize_for` (`cost` | `performance` | `speed`, null = cost) sets what auto mode optimizes for, in chat auto mode and unattended routing.

Body: application/json (free-form — pass with `--data`)

### `ai-agent.conversations.away.create`

`POST /api/ai-agent/conversations/{id}/away`

Report the chat client away or back

Marks the caller's live agent turns in this conversation as watched (away false) or not (away true). A turn that finishes while marked away sends the user a "reply ready" push notification.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `away` (boolean, required)

### `ai-agent.conversations.create`

`POST /api/ai-agent/conversations`

Create conversation

Body: application/json (free-form — pass with `--data`)

### `ai-agent.conversations.delete`

`DELETE /api/ai-agent/conversations/{id}`

Delete conversation

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `ai-agent.conversations.export.list`

`GET /api/ai-agent/conversations/{id}/export`

List export

Path params (positional, in order):
  - `id`

### `ai-agent.conversations.get`

`GET /api/ai-agent/conversations/{id}`

Fetch conversation

Path params (positional, in order):
  - `id`

### `ai-agent.conversations.list`

`GET /api/ai-agent/conversations`

List conversations

### `ai-agent.conversations.search.list`

`GET /api/ai-agent/conversations/search`

Search conversations

Full-text search over the caller's own past agent conversations (message bodies and titles). Scoped to the authenticated (workspace, user).

Query:
  - `q` (string, required)
  - `limit` (integer)

### `ai-agent.conversations.update`

`PATCH /api/ai-agent/conversations/{id}`

Update conversation

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `ai-agent.create`

`POST /api/ai-agent`

Send a chat message to the AI agent

Body: application/json (free-form — pass with `--data`)

### `ai-agent.credits-meter.list`

`GET /api/ai-agent/credits-meter`

Get the chat credits meter

The caller's spendable credits (`balance` = their own wallet, `poolBalance` = the workspace pool when team billing is on) and `nextTurnEstimate`, the credits one chat turn needs on the model it will run on — the same floor the chat preflight refuses on. Pass `persona_id` to price a turn with that AI employee's pinned model. `configured: false` means billing is off on this deployment. Never cached.

Query:
  - `persona_id` (string<uuid>)

### `ai-agent.custom-tools.create`

`POST /api/ai-agent/custom-tools`

Create custom tool

Body: application/json (free-form — pass with `--data`)

### `ai-agent.custom-tools.delete`

`DELETE /api/ai-agent/custom-tools/{id}`

Delete custom tool

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `ai-agent.custom-tools.list`

`GET /api/ai-agent/custom-tools`

List custom tools

### `ai-agent.custom-tools.update`

`PATCH /api/ai-agent/custom-tools/{id}`

Update custom tool

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `ai-agent.escalation-policy.list`

`GET /api/ai-agent/escalation-policy`

Get the workspace agent escalation policy (admin)

### `ai-agent.escalation-policy.set`

`PUT /api/ai-agent/escalation-policy`

Update the workspace agent escalation policy (admin)

Partial update — omitted fields keep their current value. Recipients are validated against active workspace membership; `notify_user_ids: null` means "all admins".

Body (application/json):
  - `min_immediate_severity` (string) — one of: `info`, `warning`, `critical`
  - `quiet_hours_enabled` (boolean)
  - `quiet_start_hour` (integer)
  - `quiet_end_hour` (integer)
  - `timezone` (string) — IANA timezone, e.g. America/Los_Angeles.
  - `critical_overrides_quiet_hours` (boolean)
  - `notify_user_ids` (string<uuid>[])

### `ai-agent.feedback.analytics.list`

`GET /api/ai-agent/feedback/analytics`

List analytics

### `ai-agent.feedback.create`

`POST /api/ai-agent/feedback`

Create feedback

Body: application/json (free-form — pass with `--data`)

### `ai-agent.feedback.delete`

`DELETE /api/ai-agent/feedback`

Delete feedback

**Destructive** — needs `--yes` against a non-local base URL.

### `ai-agent.guardrails.create`

`POST /api/ai-agent/guardrails`

Create an agent guardrail rule (admin)

Body (application/json):
  - `name` (string, required)
  - `pattern` (string, required)
  - `rule_type` (string) — one of: `recipient`, `keyword`, `tool`
  - `match_mode` (string) — one of: `exact`, `domain`, `contains`
  - `action` (string) — one of: `block`, `approve`
  - `reason` (string)
  - `persona_id` (string) — Scope the rule to one persona.

### `ai-agent.guardrails.delete`

`DELETE /api/ai-agent/guardrails`

Delete an agent guardrail rule (admin)

**Destructive** — needs `--yes` against a non-local base URL.

Query:
  - `id` (string, required)

### `ai-agent.guardrails.list`

`GET /api/ai-agent/guardrails`

List agent guardrail rules and the catalog (admin)

Query:
  - `persona_id` (string) — Filter to one persona's rules.

### `ai-agent.guardrails.update`

`PATCH /api/ai-agent/guardrails`

Update an agent guardrail rule (admin)

Query:
  - `id` (string, required)

Body (application/json):
  - `name` (string)
  - `pattern` (string)
  - `rule_type` (string) — one of: `recipient`, `keyword`, `tool`
  - `match_mode` (string) — one of: `exact`, `domain`, `contains`
  - `action` (string) — one of: `block`, `approve`
  - `enabled` (boolean)

### `ai-agent.jobs.get`

`GET /api/ai-agent/jobs/{id}`

Fetch job

Path params (positional, in order):
  - `id`

### `ai-agent.jobs.list`

`GET /api/ai-agent/jobs`

List jobs

### `ai-agent.mention.create`

`POST /api/ai-agent/mention`

Ask the AI agent about context you supply

Stateless: returns the answer and stores nothing. To answer an @agent question in a stored task comment or discussion post — and save the answer as the agent — use /api/tasks/{id}/comments/agent-reply or /api/discussions/agent-reply instead. Failures are non-2xx with a `reason`, never a 200 carrying an apology as the answer.

Body (application/json):
  - `content` (string, required) — The comment text, including the @agent mention.
  - `context` (string)
  - `contextType` (string) — one of: `task-comment`, `discussion-reply`

### `ai-agent.org-templates.apply.create`

`POST /api/ai-agent/org-templates/{key}/apply`

Apply an org template

Admin only. Idempotent: creates only missing AI employees and meeting series; existing employees are adopted unchanged (a manager is filled in only where none is set); never deletes. Every series is created disarmed.

Path params (positional, in order):
  - `key`

Body (application/json):
  - `roles` (string[]) — Role keys to stand up; omitted means all.
  - `series` (string[]) — Meeting-series keys to create; omitted means all.
  - `series_models` (object) — Per-series model (a model id, "auto", or "default").

### `ai-agent.org-templates.list`

`GET /api/ai-agent/org-templates`

List org templates (whole AI organisations with standing meetings)

Static catalogue: each template's roles (tier, job description, scopes, reporting line, North Star contribution) and meeting series. Member-readable.

### `ai-agent.org-templates.preview.create`

`POST /api/ai-agent/org-templates/{key}/preview`

Preview applying an org template in this workspace

Admin only. Writes nothing. Returns which roles adopt an existing AI employee (matched by template stamp, role title or name; never duplicated), which are created, which reporting lines are filled in, which meeting series are created (disarmed), and each series' projected monthly credits if armed.

Path params (positional, in order):
  - `key`

Body (application/json):
  - `roles` (string[]) — Role keys to stand up; omitted means all.
  - `series` (string[]) — Meeting-series keys to create; omitted means all.
  - `series_models` (object) — Per-series model (a model id, "auto", or "default").

### `ai-agent.outcomes.create`

`POST /api/ai-agent/outcomes`

Cancel a pending outcome check (admin)

Exclude a pending check a human judges unfair — the task was descoped, the person left — rather than letting it count as a miss. Audited (`ai_agent.outcome_check_cancelled`), because "cancel the check that was about to fail" is precisely how this ledger could be laundered into looking clean.

Body (application/json):
  - `expectation_id` (string, required)

### `ai-agent.outcomes.list`

`GET /api/ai-agent/outcomes`

Agent outcome checks and hit rate (admin)

"Did the agent's work actually land?" The activity ledger answers what the agent DID; this answers whether it WORKED. Each row is a claim the agent made about the world, settled against the database by the verify-outcomes cron — met, missed, or cancelled when the referenced thing vanished and the claim became undecidable. The hit rate counts only SETTLED checks: pending ones are not evidence yet, and cancelled ones are not evidence either way. Opt-in — returns 403 `agent_oversight_disabled` unless outcome verification is enabled for the workspace.

Query:
  - `days` (integer) — Scorecard window. Default 30.
  - `status` (string) — one of: `pending`, `met`, `missed`, `cancelled`

### `ai-agent.persona-departments.list`

`GET /api/ai-agent/persona-departments`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `ai-agent.personas.avatar.generate.create`

`POST /api/ai-agent/personas/avatar/generate`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `ai-agent.personas.create`

`POST /api/ai-agent/personas`

Create an AI agent persona

Admin only. Omitting allowed_scopes creates the employee with the starter set (tasks_projects, communications, reports_analytics, knowledge_files), the same default as the roster editor and the create_ai_persona agent tool. Pass null or an empty array for an unrestricted employee.

Body (application/json):
  - `name` (string, required)
  - `role_title` (string)
  - `personality` (string) — The employee's instructions and personality (its system-prompt layer).
  - `model` (string) — Model id from available_models; null or empty uses the workspace default.
  - `allowed_scopes` (string[]) — Capability groups the employee may use. Omitted gives the starter set; null or [] means every capability.
  - `member_user_ids` (string<uuid>[]) — Who may chat with the employee. Omitted, null or [] leaves it open to every member.
  - `avatar_url` (string)
  - `avatar_color` (string)
  - `avatar_prompt` (string)
  - `voice_id` (string)
  - `enabled` (boolean)
  - `is_cross_workspace` (boolean)
  - `kvn_know_how` (string)
  - `kvn_vision` (string)
  - `kvn_negation` (string)
  - `security_guardrails` (string)

### `ai-agent.personas.delete`

`DELETE /api/ai-agent/personas/{id}`

Delete an AI agent persona

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `ai-agent.personas.departments.list`

`GET /api/ai-agent/personas/{p1}/departments`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `ai-agent.personas.departments.set`

`PUT /api/ai-agent/personas/{p1}/departments`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `ai-agent.personas.generate.create`

`POST /api/ai-agent/personas/generate`

Draft a persona from a natural-language description

Admin/owner only. Returns a generated (unsaved) persona.

Body (application/json):
  - `prompt` (string, required) — Description of the AI employee. Truncated at 2000 chars.

### `ai-agent.personas.list`

`GET /api/ai-agent/personas`

List AI agent personas (AI employees)

### `ai-agent.personas.members.list`

`GET /api/ai-agent/personas/{p1}/members`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `ai-agent.personas.members.set`

`PUT /api/ai-agent/personas/{p1}/members`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `ai-agent.personas.org-chart.list`

`GET /api/ai-agent/personas/org-chart`

The AI-employee org chart

Every AI Employee the caller may see, with its reporting line (`reports_to_persona_id`) and departments, for the org-chart view. Same visibility rule as GET /api/ai-agent/personas (one helper, two callers): a member never sees a restricted or disabled employee, and a visible employee whose MANAGER is hidden from them has its `reports_to_persona_id` withheld - so the chart cannot be used to learn that a restricted employee exists.

### `ai-agent.personas.update`

`PATCH /api/ai-agent/personas/{id}`

Update an AI agent persona

Path params (positional, in order):
  - `id`

Body (application/json):
  - `name` (string)
  - `roleTitle` (string)
  - `model` (string)
  - `systemPrompt` (string)
  - `avatar` (string)

### `ai-agent.personas.week.list`

`GET /api/ai-agent/personas/week`

Each AI employee's last seven days

Read-only, per visible AI Employee: scheduled runs, skipped and failed runs, assigned-task runs and distinct tasks worked, actions executed and parked for approval, escalations (executed escalate_to_user), open waiting-on items and their nudges, and the tokens its scheduled runs recorded. Credits are not attributed per employee (bills carry the run kind and payer, not the persona). Same visibility rule as GET /api/ai-agent/personas: a member sees only the employees they may chat with, and the numbers are computed for exactly that list.

### `ai-agent.preferences.list`

`GET /api/ai-agent/preferences`

List preferences

### `ai-agent.preferences.update`

`PATCH /api/ai-agent/preferences`

Update preferences

Body: application/json (free-form — pass with `--data`)

### `ai-agent.schedules.create`

`POST /api/ai-agent/schedules`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `ai-agent.schedules.delete`

`DELETE /api/ai-agent/schedules/{p1}`

(undocumented route — params unknown, pass them explicitly)

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `ai-agent.schedules.list`

`GET /api/ai-agent/schedules`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `ai-agent.schedules.runs.list`

`GET /api/ai-agent/schedules/runs`

List scheduled autonomous agent runs

Query:
  - `schedule` (string) — Filter to one schedule id.
  - `limit` (integer)

### `ai-agent.schedules.update`

`PATCH /api/ai-agent/schedules/{p1}`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `ai-agent.share.create`

`POST /api/ai-agent/share`

Share an agent answer or conversation

Shares a single message or a whole conversation. `destination=knowledge` saves it as a knowledge document; `destination=snapshot` creates a snapshot that can additionally be DM'd to recipients or made public via a link.

Body (application/json):
  - `scope` (string) — one of: `message`, `conversation`
  - `destination` (string) — one of: `snapshot`, `knowledge`
  - `visibility` (string) — one of: `workspace`, `public`
  - `title` (string)
  - `note` (string)
  - `content` (string) — Required for a message-scope snapshot.
  - `source_conversation_id` (string)
  - `recipient_user_ids` (string<uuid>[]) — DM the snapshot to these members (active members of this workspace only).

### `ai-agent.share.get`

`GET /api/ai-agent/share/{id}`

Read a shared agent snapshot

Path params (positional, in order):
  - `id`

### `ai-agent.skipped.list`

`GET /api/ai-agent/skipped`

What Kavanah skipped in the last 24 hours, and why

Owner/admin only. Five sections read from what each runner already recorded: scheduled runs skipped (credits, daily budget, task gate, agent off), automation events parked for a later attempt, automation actions skipped, chat requests refused for credits, and recurring emails whose latest send failed. Each item carries the recorded reason, a timestamp and a link. `notRecorded` names sources that keep no per-item record (inbound mail the sync bridge declined). Never cached.

### `ai-agent.slack-managers.create`

`POST /api/ai-agent/slack-managers`

Create an AI Slack manager (admin)

The caller becomes the manager's OWNER: their Slack connection posts the answers and their credits pay for them, so the Slack workspace must be one the caller has connected. Created switched off unless `enabled: true` is sent. snake_case keys are accepted too.

Body (application/json):
  - `personaId` (string<uuid>) — The AI employee that answers. Not a digital twin.
  - `slackTeamId` (string) — A Slack workspace the owner has connected.
  - `channelIds` (string[]) — Channels it answers @mentions in. A manager listing a channel outranks one answering every channel.
  - `answerAllChannels` (boolean) — Answer @mentions in every channel the bot is in.
  - `answerDms` (boolean) — Answer direct messages to the bot (needs the im:history grant).
  - `playbook` (string) — The only program facts the manager may state.
  - `escalationUserIds` (string<uuid>[]) — Members alerted when the manager hands a question to a person. Empty = the owner. Inactive ids are dropped.
  - `perPersonHourlyLimit` (integer)
  - `hourlyReplyCap` (integer)
  - `enabled` (boolean)

### `ai-agent.slack-managers.delete`

`DELETE /api/ai-agent/slack-managers/{id}`

Delete an AI Slack manager and its reply log (admin)

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `ai-agent.slack-managers.list`

`GET /api/ai-agent/slack-managers`

List AI Slack managers, with their last 7 days of answers (admin)

An AI Slack manager is an AI employee that answers people in a connected Slack workspace — @mentions of the Kavanah bot in chosen channels, and optionally DMs. It has no tools and sees no workspace data; it knows its persona and its playbook only. Each manager carries `stats` for the last 7 days (answered, escalated, rate-limited, refused, failed, credits, distinct people).

### `ai-agent.slack-managers.update`

`PATCH /api/ai-agent/slack-managers/{id}`

Update an AI Slack manager (admin)

Omitted fields are left unchanged. The owner never changes; every Slack check is made against the owner's connection.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `personaId` (string<uuid>) — The AI employee that answers. Not a digital twin.
  - `slackTeamId` (string) — A Slack workspace the owner has connected.
  - `channelIds` (string[]) — Channels it answers @mentions in. A manager listing a channel outranks one answering every channel.
  - `answerAllChannels` (boolean) — Answer @mentions in every channel the bot is in.
  - `answerDms` (boolean) — Answer direct messages to the bot (needs the im:history grant).
  - `playbook` (string) — The only program facts the manager may state.
  - `escalationUserIds` (string<uuid>[]) — Members alerted when the manager hands a question to a person. Empty = the owner. Inactive ids are dropped.
  - `perPersonHourlyLimit` (integer)
  - `hourlyReplyCap` (integer)
  - `enabled` (boolean)

### `ai-agent.tools.execute.create`

`POST /api/ai-agent/tools/{name}/execute`

Execute one agent tool by name

Deterministic counterpart to POST /api/ai-agent. Applies the full governance stack: effective-toolset filtering, argument guardrails, the action policy (FAIL CLOSED — an `approve` verdict parks rather than runs, unlike interactive chat), the action ledger and undo recording.

Path params (positional, in order):
  - `name`

Body (application/json):
  - `input` (object) — Arguments for the tool, per its input_schema.
  - `persona_id` (string) — Execute within this persona's scope.
  - `run_id` (string) — Idempotency scope. Reusing it after a timeout returns the first result instead of repeating a risky write.

### `ai-agent.tools.list`

`GET /api/ai-agent/tools`

List the agent tools the caller may execute

Filtered by persona scope, read-only action mode, data scopes and ADMIN_ONLY_TOOLS — this is the caller's effective toolset, not the raw registry.

Query:
  - `persona_id` (string) — Evaluate the toolset as this persona.
  - `q` (string) — Case-insensitive filter over name and description.

### `ai-agent.twin.create`

`POST /api/ai-agent/twin`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `ai-agent.twin.delete`

`DELETE /api/ai-agent/twin`

(undocumented route — params unknown, pass them explicitly)

**Destructive** — needs `--yes` against a non-local base URL.

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `ai-agent.twin.grounding.create`

`POST /api/ai-agent/twin/grounding`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `ai-agent.twin.grounding.delete`

`DELETE /api/ai-agent/twin/grounding`

(undocumented route — params unknown, pass them explicitly)

**Destructive** — needs `--yes` against a non-local base URL.

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `ai-agent.twin.grounding.list`

`GET /api/ai-agent/twin/grounding`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `ai-agent.twin.list`

`GET /api/ai-agent/twin`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `ai-agent.twin.reply.create`

`POST /api/ai-agent/twin/reply`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `ai-agent.undo.create`

`POST /api/ai-agent/undo`

Create undo

Body: application/json (free-form — pass with `--data`)

### `ai-agent.usage-breakdown.list`

`GET /api/ai-agent/usage-breakdown`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `meeting-twin.external.consents.create`

`POST /api/meeting-twin/external/consents`

Withdraw consent to the caller's cloned voice or video avatar

Takes effect immediately; any of the caller's twins in a meeting now leaves, and a likeness on Kavanah's included vendor account is deleted there.

Body (application/json):
  - `kind` (string, required) — one of: `voice_clone`, `video_face`

### `meeting-twin.external.face.create`

`POST /api/meeting-twin/external/face`

Start / finish the video avatar upload

`{ action: start }` → `{ uploadId }`; then the parts go to `/face/part`; then `{ action: finish, uploadId, parts, contentType, typedName }` records consent and creates the Tavus face.

Body: application/json (free-form — pass with `--data`)

### `meeting-twin.external.face.list`

`GET /api/meeting-twin/external/face`

The caller's video avatar training status

### `meeting-twin.external.face.part.create`

`POST /api/meeting-twin/external/face/part`

Upload one ≤4 MB slice of the avatar training video

Query:
  - `uploadId` (string, required)
  - `part` (integer, required)

Body: application/json (free-form — pass with `--data`)

### `meeting-twin.external.sessions.create`

`POST /api/meeting-twin/external/sessions`

Send the caller's own twin or notetaker to a meeting

`{ meetingUrl, mode: audio|video|notetaker, title?, dealId?, maxMinutes?, scheduledStart?, estimateOnly? }`. The rep is always the caller. `estimateOnly: true` returns the cost preview (`ownAccountsUsd` = what the workspace's own vendor accounts bill; `included` = which vendors run on Kavanah's accounts and are inside `credits`), display name and disclosure without creating anything. On Kavanah's accounts the credit preflight covers the whole session at its maximum length. Refused (with a plain-language reason) when the workspace opt-ins are off, consent is missing, a vendor key is missing, the link is not a Zoom/Meet/Teams/Webex meeting, another twin is already going to that meeting (409), or the caller cannot cover the credit preflight (402).

Body: application/json (free-form — pass with `--data`)

### `meeting-twin.external.sessions.delete`

`DELETE /api/meeting-twin/external/sessions/{id}`

Make a twin / notetaker leave now

The rep, or a workspace owner/admin (kill switch). Never starts anything.

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `meeting-twin.external.sessions.get`

`GET /api/meeting-twin/external/sessions/{id}`

One twin / notetaker meeting (live status, transcript, summary)

Refreshed from the vendor on read; the rep or a workspace owner/admin.

Path params (positional, in order):
  - `id`

### `meeting-twin.external.sessions.list`

`GET /api/meeting-twin/external/sessions`

The caller's twin / notetaker meetings

### `meeting-twin.external.setup.list`

`GET /api/meeting-twin/external/setup`

The caller's AI twin & notetaker setup state

Everything the "AI twin setup" page shows, for the CALLER only: the workspace opt-ins (twin in a call, outside meetings, video, notetaker), the caller's twin profile (voice, video avatar, what it may talk about, auto-join), their likeness consents (never the recordings), and per-vendor status for Recall.ai, Tavus and ElevenLabs (never a key): `usable`, `source` (`workspace` = the workspace's own key, `platform` = included with Kavanah, null = neither), `platformAvailable`, and the workspace's own connection `status`.

### `meeting-twin.external.setup.set`

`PUT /api/meeting-twin/external/setup`

Update the caller's own twin profile

Pick a voice (`voiceId` + `voiceSource` workspace|platform), set `knowledge`, `enabled`, `autoRecordExternal`, `autoRecordIncludeInternal`. A voice from the workspace ElevenLabs account must not be a CLONE unless it is the caller's own consented clone (403); a platform voice must be one of Kavanah's stock presets or the caller's own consented clone on Kavanah's account, stamped with this workspace and member (403 otherwise).

Body: application/json (free-form — pass with `--data`)

### `meeting-twin.external.test.create`

`POST /api/meeting-twin/external/test`

Test my twin (no meeting)

The caller's twin answers `text` with the outside-meeting hard limits on, returning the reply and its synthesised voice (base64 MP3). Billed to the caller.

Body (application/json):
  - `text` (string, required)

### `meeting-twin.external.vendors.test.create`

`POST /api/meeting-twin/external/vendors/test`

Test a meeting-twin vendor connection

`{ vendor: recall|tavus|elevenlabs }` → `{ ok, message }` in plain language. Only a vendor 401/403 on the key marks the connection broken.

Body (application/json):
  - `vendor` (string, required) — one of: `recall`, `tavus`, `elevenlabs`

### `meeting-twin.external.voice-clone.create`

`POST /api/meeting-twin/external/voice-clone`

Clone the caller's own voice (with recorded consent)

Multipart: `typedName` (must equal the caller's profile name), `consent` (recording of them reading the consent statement), `samples` (1–10 audio files, ≥ ~1 minute in total). The consent (text, SHA-256, signature, IP, user agent, and the recording) is stored BEFORE the ElevenLabs Instant Voice Clone is created in the WORKSPACE's own ElevenLabs account.

Body: multipart/form-data (free-form — pass with `--data`)

### `meeting-twin.external.voices.list`

`GET /api/meeting-twin/external/voices`

Voices the caller may give their twin

The workspace ElevenLabs account's stock/designed voices plus the caller's own consented clone (other people's clones are hidden), and — when Kavanah's included voice service is available — its presets plus the caller's own clone there (Kavanah's shared account is never listed).

### `water-cooler.threads.create`

`POST /api/water-cooler/threads`

Start a Water Cooler conversation

Opens a thread and runs the first exchange after the response: the selected AI employees (2-4) debate the topic for the chosen rounds and close with a "so what". Billed to the caller's credits like a chat turn. Poll the GET below while `status` is `running`.

Body (application/json):
  - `topic` (string, required)
  - `persona_ids` (string[], required)
  - `rounds` (integer) — one of: `1`, `2`

### `water-cooler.threads.delete`

`DELETE /api/water-cooler/threads/{id}`

Delete a thread (starter or admin)

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `water-cooler.threads.get`

`GET /api/water-cooler/threads/{id}`

Get a thread with its messages

Path params (positional, in order):
  - `id`

### `water-cooler.threads.list`

`GET /api/water-cooler/threads`

List Water Cooler threads

### `water-cooler.threads.promote.create`

`POST /api/water-cooler/threads/{id}/promote`

Turn the thread's close into a task

Path params (positional, in order):
  - `id`

Body (application/json):
  - `project_ref` (string, required)
  - `title` (string)

### `water-cooler.threads.reply.create`

`POST /api/water-cooler/threads/{id}/reply`

Reply as a human (re-wakes the room when idle)

Records the reply immediately. If no exchange is running, re-wakes the seats for one reply round plus a fresh close, billed to the replier.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `content` (string, required)

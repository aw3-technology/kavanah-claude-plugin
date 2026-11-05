# Tasks

76 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `entity-versions.list` | GET | `/api/entity-versions` | List saved version snapshots of an entity |
| `entity-versions.restore.create` | POST | `/api/entity-versions/{id}/restore` | Restore a task to a saved version |
| `geocode.list` | GET | `/api/geocode` | Forward-geocode an address (task Map view) |
| `task-candidates.create` | POST | `/api/task-candidates` | Manually add a task candidate |
| `task-candidates.list` | GET | `/api/task-candidates` | List the task-candidate triage queue |
| `task-candidates.metrics.list` | GET | `/api/task-candidates/metrics` | Triage queue metrics |
| `task-candidates.update` | PATCH | `/api/task-candidates/{id}` | Accept or dismiss a task candidate |
| `tasks.access.list` | GET | `/api/tasks/{id}/access` | Read a task's restriction state and access list |
| `tasks.access.update` | PATCH | `/api/tasks/{id}/access` | Restrict a task and/or replace its access list |
| `tasks.activity.list` | GET | `/api/tasks/activity` | List activity |
| `tasks.agent-run.approvals.create` | POST | `/api/tasks/{id}/agent-run/approvals/{approvalId}` | Approve or deny an action an autonomous task run parked |
| `tasks.agent-run.create` | POST | `/api/tasks/{id}/agent-run` | Start an autonomous agent run on a task |
| `tasks.agent-run.list` | GET | `/api/tasks/{id}/agent-run` | Latest autonomous agent run for a task |
| `tasks.approvals.create` | POST | `/api/tasks/approvals` | Create approval |
| `tasks.approvals.list` | GET | `/api/tasks/approvals` | List approvals |
| `tasks.approvals.update` | PATCH | `/api/tasks/approvals/{id}` | Update approval |
| `tasks.archive.create` | POST | `/api/tasks/{id}/archive` | Archive or restore a task in place |
| `tasks.attachments.create` | POST | `/api/tasks/{id}/attachments` | Create attachment |
| `tasks.attachments.delete` | DELETE | `/api/tasks/{id}/attachments` | Delete attachments |
| `tasks.attachments.list` | GET | `/api/tasks/{id}/attachments` | List attachments |
| `tasks.batch.list` | GET | `/api/tasks/batch` | List batch |
| `tasks.bulk.update` | PATCH | `/api/tasks/bulk` | Update bulk |
| `tasks.checklist.list` | GET | `/api/tasks/{id}/checklist` | List checklist |
| `tasks.checklist.set` | PUT | `/api/tasks/{id}/checklist` | Update checklist |
| `tasks.comments.agent-reply.create` | POST | `/api/tasks/{id}/comments/agent-reply` | Answer an @agent question in a task comment |
| `tasks.comments.create` | POST | `/api/tasks/{id}/comments` | Append a comment to a task |
| `tasks.comments.list` | GET | `/api/tasks/{id}/comments` | List a task's comments |
| `tasks.context.list` | GET | `/api/tasks/{id}/context` | Task context bundle (Markdown) |
| `tasks.count.list` | GET | `/api/tasks/count` | Count of open tasks assigned to the caller |
| `tasks.create` | POST | `/api/tasks` | Create a new task |
| `tasks.delete` | DELETE | `/api/tasks/{id}` | Delete a task |
| `tasks.dependencies.create` | POST | `/api/tasks/dependencies` | Create a task dependency |
| `tasks.dependencies.delete` | DELETE | `/api/tasks/dependencies/{id}` | Delete a task dependency |
| `tasks.dependencies.list` | GET | `/api/tasks/dependencies` | List dependencies |
| `tasks.effort.update` | PATCH | `/api/tasks/effort` | Update effort |
| `tasks.estimate.create` | POST | `/api/tasks/{id}/estimate` | Create estimate |
| `tasks.estimate.list` | GET | `/api/tasks/{id}/estimate` | List estimate |
| `tasks.export.list` | GET | `/api/tasks/export` | Export a project's tasks as CSV, or the full board as JSON |
| `tasks.gantt.list` | GET | `/api/tasks/gantt` | List gantt |
| `tasks.get` | GET | `/api/tasks/{id}` | Get a single task by id |
| `tasks.import.create` | POST | `/api/tasks/import` | Import tasks from CSV |
| `tasks.intelligence.agent-capability.create` | POST | `/api/tasks/intelligence/agent-capability` | Assess whether the AI agent can complete a task |
| `tasks.intelligence.decompose.create` | POST | `/api/tasks/intelligence/decompose` | Create decompose |
| `tasks.intelligence.entity-links.create` | POST | `/api/tasks/intelligence/entity-links` | Create entity link |
| `tasks.intelligence.eta-confidence.create` | POST | `/api/tasks/intelligence/eta-confidence` | Create eta confidence |
| `tasks.intelligence.find-duplicates.create` | POST | `/api/tasks/intelligence/find-duplicates` | Create find duplicate |
| `tasks.intelligence.parse.create` | POST | `/api/tasks/intelligence/parse` | Create parse |
| `tasks.intelligence.skills.create` | POST | `/api/tasks/intelligence/skills` | Create skill |
| `tasks.intelligence.slip-risk.create` | POST | `/api/tasks/intelligence/slip-risk` | Create slip risk |
| `tasks.intelligence.templates.create` | POST | `/api/tasks/intelligence/templates` | Create template |
| `tasks.intelligence.templates.list` | GET | `/api/tasks/intelligence/templates` | List templates |
| `tasks.link-previews.list` | GET | `/api/tasks/link-previews` | Task cards for links posted in chat |
| `tasks.list` | GET | `/api/tasks` | List tasks for a project, across projects, or assigned to the caller |
| `tasks.mentions.create` | POST | `/api/tasks/mentions` | Create mention |
| `tasks.mentions.list` | GET | `/api/tasks/mentions` | List mentions |
| `tasks.mentions.update` | PATCH | `/api/tasks/mentions` | Update mentions |
| `tasks.milestones.create` | POST | `/api/tasks/milestones` | Create milestone |
| `tasks.milestones.delete` | DELETE | `/api/tasks/milestones/{id}` | Delete milestone |
| `tasks.milestones.list` | GET | `/api/tasks/milestones` | List milestones |
| `tasks.milestones.update` | PATCH | `/api/tasks/milestones/{id}` | Update milestone |
| `tasks.reorder.create` | POST | `/api/tasks/reorder` | Reorder tasks (bulk status + sort update) |
| `tasks.share-to-chat.create` | POST | `/api/tasks/{id}/share-to-chat` | Send a task to teammates as chat messages |
| `tasks.subscriptions.create` | POST | `/api/tasks/subscriptions` | Create subscription |
| `tasks.subscriptions.delete` | DELETE | `/api/tasks/subscriptions` | Delete subscriptions |
| `tasks.subscriptions.list` | GET | `/api/tasks/subscriptions` | List subscriptions |
| `tasks.suggest-split.create` | POST | `/api/tasks/{id}/suggest-split` | Create suggest split |
| `tasks.transitions.list` | GET | `/api/tasks/{id}/transitions` | Move history for one task |
| `tasks.update` | PATCH | `/api/tasks/{id}` | Update a task |
| `tasks.views.list` | GET | `/api/tasks/views` | List views |
| `tasks.why-stuck.create` | POST | `/api/tasks/{id}/why-stuck` | Create why stuck |
| `views.create` | POST | `/api/views` | Create a saved view |
| `views.create.by-id` | POST | `/api/views/{id}` | Duplicate a saved view |
| `views.delete` | DELETE | `/api/views/{id}` | Delete a saved view |
| `views.get` | GET | `/api/views/{id}` | Get a saved view |
| `views.list` | GET | `/api/views` | List saved views |
| `views.update` | PATCH | `/api/views/{id}` | Update a saved view |

---

### `entity-versions.list`

`GET /api/entity-versions`

List saved version snapshots of an entity

Signed-in workspace members. Returns the version history recorded for one entity in the active workspace. Only `task` is supported as an entity type.

Query:
  - `entity_type` (string, required) — one of: `task`
  - `entity_id` (string, required)
  - `limit` (integer)

### `entity-versions.restore.create`

`POST /api/entity-versions/{id}/restore`

Restore a task to a saved version

Signed-in workspace members. Snapshots the task's current state as a "Before restore" version, then overwrites the task's restorable fields from the chosen version. Writes a task-update audit entry. Only task versions can be restored.

Path params (positional, in order):
  - `id`

### `geocode.list`

`GET /api/geocode`

Forward-geocode an address (task Map view)

Server-side proxy to OpenStreetMap Nominatim. A null result means the address could not be located (not an error).

Query:
  - `q` (string, required)

### `task-candidates.create`

`POST /api/task-candidates`

Manually add a task candidate

Any member. Adds a manual, high-confidence candidate to the triage queue.

Body (application/json):
  - `title` (string, required)
  - `description` (string)
  - `suggested_project_ref` (string)
  - `suggested_assignee` (string)
  - `suggested_subtasks` (string[])
  - `source_excerpt` (string)

### `task-candidates.list`

`GET /api/task-candidates`

List the task-candidate triage queue

Any member. enabled reports whether the workspace opted into task capture; reads work either way.

Query:
  - `status` (string) — one of: `pending`, `accepted`, `dismissed`, `all`
  - `limit` (integer)

### `task-candidates.metrics.list`

`GET /api/task-candidates/metrics`

Triage queue metrics

Any member. Queue size, time in queue, time per candidate and dismissal-reason distribution.

Query:
  - `days` (integer)

### `task-candidates.update`

`PATCH /api/task-candidates/{id}`

Accept or dismiss a task candidate

Any member. accept creates the task (with optional overrides); dismiss needs a reason, and out_of_scope with a cited Negation records a negation hit.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `action` (string, required) — one of: `accept`, `dismiss`
  - `title` (string)
  - `description` (string)
  - `project_ref` (string)
  - `assigned_to` (string)
  - `subtasks` (string[])
  - `reason` (string) — one of: `out_of_scope`, `no_checkable_outcome`, `duplicate`, `premature`, `other`
  - `matched_negation` (string)
  - `note` (string)
  - `triage_ms` (number)

### `tasks.access.list`

`GET /api/tasks/{id}/access`

Read a task's restriction state and access list

Requires view access to the task. canManage is true when the caller can edit the task.

Path params (positional, in order):
  - `id`

### `tasks.access.update`

`PATCH /api/tasks/{id}/access`

Restrict a task and/or replace its access list

Requires edit access to the task. members replaces the full ACL; each user must be an active member. A non-admin who restricts a task is kept on it as an editor. Writes an audit entry.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `restricted` (boolean)
  - `members` (object[])

### `tasks.activity.list`

`GET /api/tasks/activity`

List activity

### `tasks.agent-run.approvals.create`

`POST /api/tasks/{id}/agent-run/approvals/{approvalId}`

Approve or deny an action an autonomous task run parked

Admins only (plus tasks:edit). Approving executes the parked tool call after re-checking guardrails and policy; optional edits require reviewed_digest. The approval must belong to this task. Writes an audit entry.

Path params (positional, in order):
  - `id`
  - `approvalId`

Body (application/json):
  - `decision` (string, required) — one of: `approve`, `deny`
  - `edits` (object) — Edits to the parked payload (approve only)
  - `reviewed_digest` (string)

### `tasks.agent-run.create`

`POST /api/tasks/{id}/agent-run`

Start an autonomous agent run on a task

Requires tasks:edit and edit access to the task, and an effective autonomy level of safe or full. Returns the existing run if one is already running or awaiting approval; otherwise enqueues a background job and writes an audit entry.

Path params (positional, in order):
  - `id`

### `tasks.agent-run.list`

`GET /api/tasks/{id}/agent-run`

Latest autonomous agent run for a task

Requires tasks:view and view access to the task. Returns the caller's effective autonomy level, the latest run (with persona_name) and its approvals.

Path params (positional, in order):
  - `id`

### `tasks.approvals.create`

`POST /api/tasks/approvals`

Create approval

Body: application/json (free-form — pass with `--data`)

### `tasks.approvals.list`

`GET /api/tasks/approvals`

List approvals

### `tasks.approvals.update`

`PATCH /api/tasks/approvals/{id}`

Update approval

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `tasks.archive.create`

`POST /api/tasks/{id}/archive`

Archive or restore a task in place

Non-destructive hide: an archived task keeps its id, comments, and history but is excluded from task list queries unless `includeArchived=true` is passed to GET /api/tasks. Send `{"archived": false}` to restore. Requires the tasks/edit permission (unlike delete, nothing is lost).

Path params (positional, in order):
  - `id`

Body (application/json):
  - `archived` (boolean) — true archives the task, false restores it.

### `tasks.attachments.create`

`POST /api/tasks/{id}/attachments`

Create attachment

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `tasks.attachments.delete`

`DELETE /api/tasks/{id}/attachments`

Delete attachments

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `tasks.attachments.list`

`GET /api/tasks/{id}/attachments`

List attachments

Path params (positional, in order):
  - `id`

### `tasks.batch.list`

`GET /api/tasks/batch`

List batch

**Destructive** — needs `--yes` against a non-local base URL.

### `tasks.bulk.update`

`PATCH /api/tasks/bulk`

Update bulk

**Destructive** — needs `--yes` against a non-local base URL.

Body: application/json (free-form — pass with `--data`)

### `tasks.checklist.list`

`GET /api/tasks/{id}/checklist`

List checklist

Path params (positional, in order):
  - `id`

### `tasks.checklist.set`

`PUT /api/tasks/{id}/checklist`

Update checklist

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `tasks.comments.agent-reply.create`

`POST /api/tasks/{id}/comments/agent-reply`

Answer an @agent question in a task comment

Generates the AI agent's answer to a stored comment and appends it to the task in one statement. Idempotent per comment: asking twice returns the existing answer instead of generating a second one. The answer notifies nobody — the model's text is not the caller's words.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `commentId` (string, required) — The comment that mentions @agent.

### `tasks.comments.create`

`POST /api/tasks/{id}/comments`

Append a comment to a task

Appends a single comment atomically. Prefer this over PATCHing the task's whole `comments` array, which is a read-modify-write and loses concurrent comments.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `body` (string)
  - `content` (string) — Alias for `body`.

### `tasks.comments.list`

`GET /api/tasks/{id}/comments`

List a task's comments

Path params (positional, in order):
  - `id`

### `tasks.context.list`

`GET /api/tasks/{id}/context`

Task context bundle (Markdown)

Everything an external agent needs to act on a task, rendered as Markdown: title + status/priority/due/assignees, project, description, checklist and sub-tasks, the newest 20 comments (older ones counted), links and attachment names, related PRs / commits / deploys, and the Kavanah URL. Capped at ~40 KB (`truncated: true` and a notice line when cut). Same access rules as `GET /api/tasks/{id}` — an invisible task is 404. `?format=markdown` answers `text/markdown; charset=utf-8` with the Markdown alone.

Path params (positional, in order):
  - `id`

Query:
  - `format` (string) — one of: `json`, `markdown`

### `tasks.count.list`

`GET /api/tasks/count`

Count of open tasks assigned to the caller

Cross-workspace count across every workspace the caller is an active member of, for the sidebar badge. Privately cached for 30 seconds.

### `tasks.create`

`POST /api/tasks`

Create a new task

Input keys are accepted in camelCase or snake_case (`dueDate` / `due_date`); camelCase wins when both are present. Responses are snake_case. Retries can pass an `Idempotency-Key` header: a replay within 5 minutes returns the original task instead of creating a duplicate (replays carry `X-Idempotent-Replay: 1`). Note `kvn_complete` is a generated column — returned by GET, never writable.

Body (application/json):
  - `projectRef` (string, required)
  - `additionalProjectRefs` (string[]) — Secondary projects the task also appears in.
  - `title` (string, required)
  - `description` (string)
  - `statusId` (string)
  - `tag` (string)
  - `priority` (string) — one of: `Normal`, `Medium`, `High`, `Done`
  - `stage` (string) — one of: `fire`, `green`, `yellow`, `investigate`, `plan`, `implement`
  - `assignedTo` (string|string[])
  - `dueDate` (string<date>)
  - `startDate` (string<date>) — Scheduled start (Timeline/Gantt bar).
  - `isMilestone` (boolean) — Pins the task as a milestone on the roadmap.
  - `reminderDate` (string)
  - `createdBy` (string)
  - `parentTaskId` (integer) — Link to a top-level parent task (first-class sub-task).
  - `departmentId` (string) — UUID of the owning department (validated against the workspace).
  - `knowHow` (string) — KVN K axis — method, verification, escalation.
  - `vision` (string) — KVN V axis — the end-state.
  - `negation` (string) — KVN N axis — what would make a working answer still wrong.
  - `visionRestated` (string) — Delegate's V restatement (handoff loop).
  - `negationSurfaced` (string) — Delegate's surfaced objection (handoff loop).
  - `subtasks` (object[])
  - `notes` (string[])
  - `links` (object[])
  - `comments` (object[])
  - `fileIds` (string[])
  - `sortOrder` (integer)

### `tasks.delete`

`DELETE /api/tasks/{id}`

Delete a task

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `tasks.dependencies.create`

`POST /api/tasks/dependencies`

Create a task dependency

Body: application/json (free-form — pass with `--data`)

### `tasks.dependencies.delete`

`DELETE /api/tasks/dependencies/{id}`

Delete a task dependency

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `tasks.dependencies.list`

`GET /api/tasks/dependencies`

List dependencies

### `tasks.effort.update`

`PATCH /api/tasks/effort`

Update effort

Body: application/json (free-form — pass with `--data`)

### `tasks.estimate.create`

`POST /api/tasks/{id}/estimate`

Create estimate

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `tasks.estimate.list`

`GET /api/tasks/{id}/estimate`

List estimate

Path params (positional, in order):
  - `id`

### `tasks.export.list`

`GET /api/tasks/export`

Export a project's tasks as CSV, or the full board as JSON

Query:
  - `projectRef` (string, required)
  - `projectName` (string)
  - `format` (string) — one of: `standard`, `jira`, `asana`, `json`

### `tasks.gantt.list`

`GET /api/tasks/gantt`

List gantt

### `tasks.get`

`GET /api/tasks/{id}`

Get a single task by id

Returns 404 (never 403) when the task exists but lives in a project the caller cannot see — a 403 would confirm the id exists.

Path params (positional, in order):
  - `id`

### `tasks.import.create`

`POST /api/tasks/import`

Import tasks from CSV

**Destructive** — needs `--yes` against a non-local base URL.

Body (application/json):
  - `projectRef` (string, required)
  - `csv` (string, required)

### `tasks.intelligence.agent-capability.create`

`POST /api/tasks/intelligence/agent-capability`

Assess whether the AI agent can complete a task

Requires tasks:view. Returns the cached assessment unless refresh is true; otherwise runs a billed model call (subject to the daily token budget) and caches the result. Refused when the effective autonomy level is off.

Body (application/json):
  - `taskId` (integer, required)
  - `refresh` (boolean)

### `tasks.intelligence.decompose.create`

`POST /api/tasks/intelligence/decompose`

Create decompose

Body: application/json (free-form — pass with `--data`)

### `tasks.intelligence.entity-links.create`

`POST /api/tasks/intelligence/entity-links`

Create entity link

Body: application/json (free-form — pass with `--data`)

### `tasks.intelligence.eta-confidence.create`

`POST /api/tasks/intelligence/eta-confidence`

Create eta confidence

Body: application/json (free-form — pass with `--data`)

### `tasks.intelligence.find-duplicates.create`

`POST /api/tasks/intelligence/find-duplicates`

Create find duplicate

Body: application/json (free-form — pass with `--data`)

### `tasks.intelligence.parse.create`

`POST /api/tasks/intelligence/parse`

Create parse

Body: application/json (free-form — pass with `--data`)

### `tasks.intelligence.skills.create`

`POST /api/tasks/intelligence/skills`

Create skill

Body: application/json (free-form — pass with `--data`)

### `tasks.intelligence.slip-risk.create`

`POST /api/tasks/intelligence/slip-risk`

Create slip risk

Body: application/json (free-form — pass with `--data`)

### `tasks.intelligence.templates.create`

`POST /api/tasks/intelligence/templates`

Create template

Body: application/json (free-form — pass with `--data`)

### `tasks.intelligence.templates.list`

`GET /api/tasks/intelligence/templates`

List templates

### `tasks.link-previews.list`

`GET /api/tasks/link-previews`

Task cards for links posted in chat

Resolves task deep links into the cards the messenger renders inline. Filtered by the CALLER's own task visibility (project visibility plus the per-task ACL), so a task the caller cannot see is simply absent from the response and its link stays a plain URL. Ids that do not parse are dropped rather than failing the batch, because they come from parsing arbitrary message text. At most 60 ids per call.

Query:
  - `ids` (string, required) — Comma-separated task ids.

### `tasks.list`

`GET /api/tasks`

List tasks for a project, across projects, or assigned to the caller

`projectRef` is required unless `assignee=me` is passed, in which case it defaults to `all` (every project the caller can see). Project visibility and per-task access control apply in every mode. `assignee=me` matches the caller by their name SET — profile name plus every roster entry carrying their email — against the task's assignee LIST, so co-assigned tasks are included; those rows additionally carry camelCase `status`, `projectRef` and an absolute `url` deep link.

Query:
  - `projectRef` (string) — A project id, or `all`. Required unless `assignee=me`.
  - `assignee` (string) — one of: `me`
  - `status` (string) — one of: `open`
  - `includeArchived` (boolean) — Include archived tasks in the result (rows carry `archived` and `archived_at`). Default false — archived tasks are hidden.

### `tasks.mentions.create`

`POST /api/tasks/mentions`

Create mention

Body: application/json (free-form — pass with `--data`)

### `tasks.mentions.list`

`GET /api/tasks/mentions`

List mentions

### `tasks.mentions.update`

`PATCH /api/tasks/mentions`

Update mentions

Body: application/json (free-form — pass with `--data`)

### `tasks.milestones.create`

`POST /api/tasks/milestones`

Create milestone

Body: application/json (free-form — pass with `--data`)

### `tasks.milestones.delete`

`DELETE /api/tasks/milestones/{id}`

Delete milestone

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `tasks.milestones.list`

`GET /api/tasks/milestones`

List milestones

### `tasks.milestones.update`

`PATCH /api/tasks/milestones/{id}`

Update milestone

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `tasks.reorder.create`

`POST /api/tasks/reorder`

Reorder tasks (bulk status + sort update)

Body (application/json):
  - `tasks` (object[], required)

### `tasks.share-to-chat.create`

`POST /api/tasks/{id}/share-to-chat`

Send a task to teammates as chat messages

Posts the task's canonical link as an ordinary chat DM to each recipient, so push, unread badges and mute rules all apply. The message carries only the link — the recipient's own access decides whether it renders as a card — so this does not grant access and deliberately does not check the recipients' access. The SENDER must be able to view the task. Per-recipient failures are reported rather than aborting the rest.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `recipientIds` (string<uuid>[], required)
  - `note` (string)

### `tasks.subscriptions.create`

`POST /api/tasks/subscriptions`

Create subscription

Body: application/json (free-form — pass with `--data`)

### `tasks.subscriptions.delete`

`DELETE /api/tasks/subscriptions`

Delete subscriptions

**Destructive** — needs `--yes` against a non-local base URL.

### `tasks.subscriptions.list`

`GET /api/tasks/subscriptions`

List subscriptions

### `tasks.suggest-split.create`

`POST /api/tasks/{id}/suggest-split`

Create suggest split

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `tasks.transitions.list`

`GET /api/tasks/{id}/transitions`

Move history for one task

Every column the task has lived in, who moved it, when, and how long it sat in the previous status. Append-only; never updated.

Path params (positional, in order):
  - `id`

### `tasks.update`

`PATCH /api/tasks/{id}`

Update a task

Input keys are accepted in camelCase or snake_case (`dueDate` / `due_date`); camelCase wins when both are present. Responses are snake_case. Omitting a field leaves it unchanged; where noted, `null` clears it. `kvn_complete` is a generated column and is never writable.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `title` (string)
  - `description` (string)
  - `statusId` (string)
  - `tag` (string)
  - `priority` (string) — one of: `Normal`, `Medium`, `High`, `Done`
  - `stage` (string) — one of: `fire`, `green`, `yellow`, `investigate`, `plan`, `implement`
  - `emoji` (string) — Single-emoji label; `null` or empty clears it.
  - `assignedTo` (string|string[])
  - `dueDate` (string<date>)
  - `startDate` (string<date>) — Scheduled start (Timeline/Gantt bar).
  - `isMilestone` (boolean)
  - `reminderDate` (string)
  - `createdBy` (string)
  - `sortOrder` (integer)
  - `projectRefs` (string[]) — Replace the full set of projects this task belongs to. The primary project (or `primaryProjectRef`) must be included.
  - `primaryProjectRef` (string)
  - `parentTaskId` (integer) — Re-parent this task; `null` detaches it.
  - `departmentId` (string) — Owning department UUID; `null` clears it.
  - `location` (object) — Map pin; `null` clears it.
  - `location.lat` (number)
  - `location.lng` (number)
  - `location.address` (string)
  - `expectedVersion` (integer) — Optimistic-concurrency guard; mismatch returns 409.
  - `knowHow` (string)
  - `vision` (string)
  - `negation` (string)
  - `visionRestated` (string)
  - `negationSurfaced` (string)
  - `subtasks` (object[])
  - `notes` (string[])
  - `links` (object[])
  - `comments` (object[])
  - `fileIds` (string[])

### `tasks.views.list`

`GET /api/tasks/views`

List views

### `tasks.why-stuck.create`

`POST /api/tasks/{id}/why-stuck`

Create why stuck

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `views.create`

`POST /api/views`

Create a saved view

The caller becomes the view's owner.

Body (application/json):
  - `name` (string, required)
  - `viewType` (string) — one of: `table`, `board`, `calendar`, `timeline`, `gallery`
  - `entityType` (string) — one of: `task`
  - `projectRef` (string|null)
  - `config` (object)
  - `shared` (boolean)
  - `isDefault` (boolean)
  - `sortOrder` (number)

### `views.create.by-id`

`POST /api/views/{id}`

Duplicate a saved view

Creates a copy owned by the caller. Requires read access to the source view.

Path params (positional, in order):
  - `id`

### `views.delete`

`DELETE /api/views/{id}`

Delete a saved view

The view's owner or a workspace admin only.

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `views.get`

`GET /api/views/{id}`

Get a saved view

Allowed when the view is shared, the caller owns it, or the caller is an admin.

Path params (positional, in order):
  - `id`

### `views.list`

`GET /api/views`

List saved views

Saved views visible to the caller, plus the available task filter/sort/group fields. projectRef omitted returns workspace and project views together; * returns workspace-wide only.

Query:
  - `entityType` (string) — one of: `task`
  - `projectRef` (string)

### `views.update`

`PATCH /api/views/{id}`

Update a saved view

The view's owner or a workspace admin only.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `name` (string)
  - `viewType` (string) — one of: `table`, `board`, `calendar`, `timeline`, `gallery`
  - `projectRef` (string|null)
  - `config` (object)
  - `shared` (boolean)
  - `isDefault` (boolean)
  - `sortOrder` (number)

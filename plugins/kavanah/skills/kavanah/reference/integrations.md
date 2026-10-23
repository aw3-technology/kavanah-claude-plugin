# Integrations

152 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `browser.profiles.capture.create` | POST | `/api/browser/profiles/{id}/capture` | Save a live session's signed-in state into a saved login |
| `browser.profiles.create` | POST | `/api/browser/profiles` | Create an empty saved-login slot |
| `browser.profiles.delete` | DELETE | `/api/browser/profiles/{id}` | Permanently delete and revoke a saved login |
| `browser.profiles.list` | GET | `/api/browser/profiles` | List the caller's saved logins |
| `browser.profiles.update` | PATCH | `/api/browser/profiles/{id}` | Change a saved login's pinned network exit |
| `browser.sessions.create` | POST | `/api/browser/sessions` | Start a cloud browser session |
| `browser.sessions.delete` | DELETE | `/api/browser/sessions/{id}` | Release a browser session |
| `browser.sessions.keep-awake.create` | POST | `/api/browser/sessions/{id}/keep-awake` | Hold a session open while nobody is watching it |
| `browser.sessions.keepalive.create` | POST | `/api/browser/sessions/{id}/keepalive` | Refresh a session's idle timer without acting on the page |
| `browser.sessions.list` | GET | `/api/browser/sessions` | List browser sessions visible to the caller |
| `browser.sessions.navigate.create` | POST | `/api/browser/sessions/{id}/navigate` | Navigate a session to a URL |
| `browser.sessions.scrape-mode.create` | POST | `/api/browser/sessions/{id}/scrape-mode` | Turn extraction rendering on or off for a live session |
| `browser.sessions.share.create` | POST | `/api/browser/sessions/{id}/share` | Share a browser session with the workspace, or revoke sharing |
| `browser.sessions.viewer-token.create` | POST | `/api/browser/sessions/{id}/viewer-token` | Mint a short-lived viewer URL for the embedded browser |
| `github.app.install.list` | GET | `/api/github/app/install` | Start the GitHub App install flow (302 redirects to github.com) |
| `github.issue-sync.list` | GET | `/api/github/issue-sync` | List connected GitHub repos and their issue-sync opt-in state |
| `github.issue-sync.update` | PATCH | `/api/github/issue-sync` | Enable or disable GitHub Issue sync for one repository |
| `github.oauth.start.list` | GET | `/api/github/oauth/start` | Start the GitHub OAuth sign-in flow (302 redirects to github.com) |
| `github.repos.list` | GET | `/api/github/repos` | List GitHub repositories available to connect |
| `github.status.list` | GET | `/api/github/status` | Get the workspace GitHub connection status |
| `github.sync.create` | POST | `/api/github/sync` | Trigger a GitHub sync for connected repositories |
| `inbox.skipped.list` | GET | `/api/inbox/skipped` | Mail Kavanah did not run your email rules on |
| `inbox.skipped.rescue.create` | POST | `/api/inbox/skipped/{id}/rescue` | Run your email rules on one skipped message |
| `integrations.angelsend.actions.create` | POST | `/api/integrations/angelsend/actions/{action}` | Execute one AngelSend api-gateway action |
| `integrations.angelsend.actions.list` | GET | `/api/integrations/angelsend/actions` | Search the AngelSend action catalogue |
| `integrations.angelsend.calendar.create` | POST | `/api/integrations/angelsend/calendar` | Create an event on the connected AngelSend calendar |
| `integrations.angelsend.calendar.list` | GET | `/api/integrations/angelsend/calendar` | List events from the connected AngelSend calendar |
| `integrations.angelsend.contacts.list` | GET | `/api/integrations/angelsend/contacts` | List leads / contacts from AngelSend |
| `integrations.angelsend.credits.list` | GET | `/api/integrations/angelsend/credits` | Get the AngelSend credit balance for the connected account |
| `integrations.angelsend.email.create` | POST | `/api/integrations/angelsend/email` | Send email via AngelSend |
| `integrations.angelsend.gmail.labels.list` | GET | `/api/integrations/angelsend/gmail/labels` | List labels |
| `integrations.angelsend.gmail.messages.list` | GET | `/api/integrations/angelsend/gmail/messages` | List messages |
| `integrations.angelsend.gmail.profile.list` | GET | `/api/integrations/angelsend/gmail/profile` | List profile |
| `integrations.angelsend.gmail.send.create` | POST | `/api/integrations/angelsend/gmail/send` | Create send |
| `integrations.angelsend.gmail.status.list` | GET | `/api/integrations/angelsend/gmail/status` | List status |
| `integrations.angelsend.gmail.thread.list` | GET | `/api/integrations/angelsend/gmail/thread` | List thread |
| `integrations.angelsend.oauth.mobile-start.list` | GET | `/api/integrations/angelsend/oauth/mobile-start` | (undocumented route — params unknown, pass them explicitly) |
| `integrations.angelsend.oauth.start.list` | GET | `/api/integrations/angelsend/oauth/start` | List start |
| `integrations.asana.import.preview.list` | GET | `/api/integrations/asana/import/preview` | (undocumented route — params unknown, pass them explicitly) |
| `integrations.asana.import.run.create` | POST | `/api/integrations/asana/import/run` | (undocumented route — params unknown, pass them explicitly) |
| `integrations.asana.tasks.create` | POST | `/api/integrations/asana/tasks` | Create a task in an Asana workspace |
| `integrations.asana.tasks.delete` | DELETE | `/api/integrations/asana/tasks/{gid}` | Delete task |
| `integrations.asana.tasks.get` | GET | `/api/integrations/asana/tasks/{gid}` | Fetch task |
| `integrations.asana.tasks.list` | GET | `/api/integrations/asana/tasks` | List Asana tasks (filtered by workspace or project) |
| `integrations.asana.tasks.update` | PATCH | `/api/integrations/asana/tasks/{gid}` | Update task |
| `integrations.asana.users-me.list` | GET | `/api/integrations/asana/users-me` | Get the connected Asana user's profile (name, email, workspaces) |
| `integrations.asana.webhooks.register.create` | POST | `/api/integrations/asana/webhooks/register` | Create register |
| `integrations.asana.webhooks.register.delete` | DELETE | `/api/integrations/asana/webhooks/register` | Delete register |
| `integrations.asana.webhooks.register.list` | GET | `/api/integrations/asana/webhooks/register` | List register |
| `integrations.asana.workspaces.list` | GET | `/api/integrations/asana/workspaces` | List Asana workspaces the connected account belongs to |
| `integrations.cloudcode.ai.chat.create` | POST | `/api/integrations/cloudcode/ai/chat` | Create chat |
| `integrations.cloudcode.github.repos.list` | GET | `/api/integrations/cloudcode/github/repos` | List repos |
| `integrations.cloudcode.projects.create` | POST | `/api/integrations/cloudcode/projects` | Create project |
| `integrations.cloudcode.projects.deployments.create` | POST | `/api/integrations/cloudcode/projects/{id}/deployments` | Create deployment |
| `integrations.cloudcode.projects.deployments.list` | GET | `/api/integrations/cloudcode/projects/{id}/deployments` | List deployments |
| `integrations.cloudcode.projects.files.delete` | DELETE | `/api/integrations/cloudcode/projects/{id}/files/{path}` | Delete file |
| `integrations.cloudcode.projects.files.get` | GET | `/api/integrations/cloudcode/projects/{id}/files/{path}` | Fetch file |
| `integrations.cloudcode.projects.files.list` | GET | `/api/integrations/cloudcode/projects/{id}/files` | List files |
| `integrations.cloudcode.projects.files.set` | PUT | `/api/integrations/cloudcode/projects/{id}/files` | Update files |
| `integrations.cloudcode.projects.get` | GET | `/api/integrations/cloudcode/projects/{id}` | Fetch project |
| `integrations.cloudcode.projects.list` | GET | `/api/integrations/cloudcode/projects` | List projects |
| `integrations.delete` | DELETE | `/api/integrations/{provider}` | Disconnect the caller from a provider |
| `integrations.docsend.ingest.create` | POST | `/api/integrations/docsend/ingest` | Mint or rotate the DocSend ingest token |
| `integrations.docsend.ingest.delete` | DELETE | `/api/integrations/docsend/ingest` | Disable the DocSend webhook path |
| `integrations.docsend.ingest.list` | GET | `/api/integrations/docsend/ingest` | DocSend ingest status for the workspace |
| `integrations.get` | GET | `/api/integrations/{provider}` | Get a single provider plus the caller's connection (if any) |
| `integrations.gmail.inbox.messages.list` | GET | `/api/integrations/gmail/inbox/messages` | List Gmail messages, or fetch one with its body |
| `integrations.gmail.inbox.send.create` | POST | `/api/integrations/gmail/inbox/send` | Send an email through the connected Gmail backend |
| `integrations.gmail.inbox.status.list` | GET | `/api/integrations/gmail/inbox/status` | Gmail inbox connection status |
| `integrations.gmail.messages.create` | POST | `/api/integrations/gmail/messages` | Send a plain-text email through Gmail |
| `integrations.gmail.messages.delete` | DELETE | `/api/integrations/gmail/messages/{id}` | Delete message |
| `integrations.gmail.messages.get` | GET | `/api/integrations/gmail/messages/{id}` | Fetch message |
| `integrations.gmail.messages.list` | GET | `/api/integrations/gmail/messages` | List Gmail message ids (and threadIds) |
| `integrations.gmail.messages.update` | PATCH | `/api/integrations/gmail/messages/{id}` | Update message |
| `integrations.gmail.profile.list` | GET | `/api/integrations/gmail/profile` | Get the connected Gmail account's profile (email, message counts) |
| `integrations.gmail.push.create` | POST | `/api/integrations/gmail/push` | Create push |
| `integrations.gmail.watch.create` | POST | `/api/integrations/gmail/watch` | Create watch |
| `integrations.gmail.watch.delete` | DELETE | `/api/integrations/gmail/watch` | Delete watch |
| `integrations.google-calendar.calendars.list` | GET | `/api/integrations/google-calendar/calendars` | List the user's Google calendars |
| `integrations.google-calendar.events.create` | POST | `/api/integrations/google-calendar/events` | Create an event on one of the user's Google calendars |
| `integrations.google-calendar.events.delete` | DELETE | `/api/integrations/google-calendar/events/{eventId}` | Delete event |
| `integrations.google-calendar.events.get` | GET | `/api/integrations/google-calendar/events/{eventId}` | Fetch event |
| `integrations.google-calendar.events.list` | GET | `/api/integrations/google-calendar/events` | List events from one of the user's Google calendars |
| `integrations.google-calendar.events.update` | PATCH | `/api/integrations/google-calendar/events/{eventId}` | Update event |
| `integrations.google-calendar.watch.create` | POST | `/api/integrations/google-calendar/watch` | Create watch |
| `integrations.google-calendar.watch.register.create` | POST | `/api/integrations/google-calendar/watch/register` | Create register |
| `integrations.google-calendar.watch.register.delete` | DELETE | `/api/integrations/google-calendar/watch/register` | Delete register |
| `integrations.google-drive.about.list` | GET | `/api/integrations/google-drive/about` | Get the Drive account's identity and storage quota |
| `integrations.google-drive.changes.create` | POST | `/api/integrations/google-drive/changes` | Create change |
| `integrations.google-drive.files.create` | POST | `/api/integrations/google-drive/files` | Create a UTF-8 text file in Drive |
| `integrations.google-drive.files.delete` | DELETE | `/api/integrations/google-drive/files/{fileId}` | Delete file |
| `integrations.google-drive.files.get` | GET | `/api/integrations/google-drive/files/{fileId}` | Fetch file |
| `integrations.google-drive.files.list` | GET | `/api/integrations/google-drive/files` | List Drive files visible to the app (drive.file scope) |
| `integrations.google-drive.files.update` | PATCH | `/api/integrations/google-drive/files/{fileId}` | Update file |
| `integrations.google-drive.watch.create` | POST | `/api/integrations/google-drive/watch` | Create watch |
| `integrations.google-drive.watch.delete` | DELETE | `/api/integrations/google-drive/watch` | Delete watch |
| `integrations.google-drive.watch.list` | GET | `/api/integrations/google-drive/watch` | (undocumented route — params unknown, pass them explicitly) |
| `integrations.google-meet.imports.get` | GET | `/api/integrations/google-meet/imports/{id}` | One of the caller's imported Google Meet calls, with its transcript |
| `integrations.google-meet.imports.list` | GET | `/api/integrations/google-meet/imports` | The caller's Google Meet transcript import — settings and imported calls |
| `integrations.google-meet.imports.update` | PATCH | `/api/integrations/google-meet/imports` | Opt the caller out of (or back into) the Google Meet transcript import |
| `integrations.icloud.events.create` | POST | `/api/integrations/icloud/events` | Create an iCloud calendar event |
| `integrations.icloud.events.list` | GET | `/api/integrations/icloud/events` | List iCloud calendar events (read live over CalDAV) |
| `integrations.icloud.messages.create` | POST | `/api/integrations/icloud/messages` | Send an email via iCloud SMTP |
| `integrations.icloud.messages.list` | GET | `/api/integrations/icloud/messages` | List synced iCloud Mail envelopes |
| `integrations.kanvo.agent.create` | POST | `/api/integrations/kanvo/agent` | Kanvo connected-agent endpoint (called by Kanvo, not by clients) |
| `integrations.list` | GET | `/api/integrations` | List available integration providers and the user's connections |
| `integrations.microsoft365.events.create` | POST | `/api/integrations/microsoft365/events` | (undocumented route — params unknown, pass them explicitly) |
| `integrations.microsoft365.events.list` | GET | `/api/integrations/microsoft365/events` | (undocumented route — params unknown, pass them explicitly) |
| `integrations.microsoft365.messages.create` | POST | `/api/integrations/microsoft365/messages` | (undocumented route — params unknown, pass them explicitly) |
| `integrations.microsoft365.messages.list` | GET | `/api/integrations/microsoft365/messages` | (undocumented route — params unknown, pass them explicitly) |
| `integrations.monday.import.preview.create` | POST | `/api/integrations/monday/import/preview` | Dry-run a Monday.com export (admin) |
| `integrations.monday.import.run.create` | POST | `/api/integrations/monday/import/run` | Import a Monday.com export as a new project (admin) |
| `integrations.multiverseai.agents.chat.create` | POST | `/api/integrations/multiverseai/agents/{id}/chat` | Create chat |
| `integrations.multiverseai.agents.get` | GET | `/api/integrations/multiverseai/agents/{id}` | Fetch agent |
| `integrations.multiverseai.agents.list` | GET | `/api/integrations/multiverseai/agents` | List agents |
| `integrations.multiverseai.chat.create` | POST | `/api/integrations/multiverseai/chat` | Create chat |
| `integrations.multiverseai.models.list` | GET | `/api/integrations/multiverseai/models` | List models |
| `integrations.multiverseai.workflows.execute.create` | POST | `/api/integrations/multiverseai/workflows/{id}/execute` | Create execute |
| `integrations.multiverseai.workflows.get` | GET | `/api/integrations/multiverseai/workflows/{id}` | Fetch workflow |
| `integrations.multiverseai.workflows.list` | GET | `/api/integrations/multiverseai/workflows` | List workflows |
| `integrations.notion.connect-token.create` | POST | `/api/integrations/notion/connect-token` | Connect Notion with an internal integration token |
| `integrations.notion.connect-token.set` | PUT | `/api/integrations/notion/connect-token` | Connect Notion with an internal integration token |
| `integrations.notion.import.create` | POST | `/api/integrations/notion/import` | Import a Notion database into a project as tasks |
| `integrations.notion.import.list` | GET | `/api/integrations/notion/import` | List the Notion databases the connection can see |
| `integrations.oauth.handoff.create` | POST | `/api/integrations/oauth/handoff` | (undocumented route — params unknown, pass them explicitly) |
| `integrations.oauth.mobile-start.list` | GET | `/api/integrations/{p1}/oauth/mobile-start` | (undocumented route — params unknown, pass them explicitly) |
| `integrations.oauth.start.list` | GET | `/api/integrations/{provider}/oauth/start` | Begin an OAuth2 authorization-code flow |
| `integrations.protonmail.messages.create` | POST | `/api/integrations/protonmail/messages` | (undocumented route — params unknown, pass them explicitly) |
| `integrations.protonmail.messages.list` | GET | `/api/integrations/protonmail/messages` | (undocumented route — params unknown, pass them explicitly) |
| `integrations.scrappy.clients.push.create` | POST | `/api/integrations/scrappy/clients/{id}/push` | Create push |
| `integrations.set` | PUT | `/api/integrations/{provider}` | Store an API-key credential for an api_key provider |
| `integrations.slack.auth-test.list` | GET | `/api/integrations/slack/auth-test` | Run Slack's auth.test method (returns bot/user/team identity) |
| `integrations.slack.channels.list` | GET | `/api/integrations/slack/channels` | List channels visible to the connected Slack bot |
| `integrations.slack.events.create` | POST | `/api/integrations/slack/events` | Create event |
| `integrations.slack.messages.create` | POST | `/api/integrations/slack/messages` | Post a message to a Slack channel via chat.postMessage |
| `integrations.slack.messages.delete` | DELETE | `/api/integrations/slack/messages` | Delete a Slack message via chat.delete |
| `integrations.slack.messages.update` | PATCH | `/api/integrations/slack/messages` | Edit a Slack message via chat.update |
| `integrations.slack.workspaces.delete` | DELETE | `/api/integrations/slack/workspaces/{teamId}` | Remove one connected Slack workspace (not the default — Disconnect removes that) |
| `integrations.slack.workspaces.list` | GET | `/api/integrations/slack/workspaces` | List the Slack workspaces the caller has connected, the default first |
| `integrations.tavus.llm.chat.completions.create` | POST | `/api/integrations/tavus/llm/{token}/chat/completions` | The video twin's brain — OpenAI-compatible endpoint Tavus calls |
| `integrations.telegram.auth-test.list` | GET | `/api/integrations/telegram/auth-test` | List auth test |
| `integrations.telegram.link.delete` | DELETE | `/api/integrations/telegram/link` | Unlink the caller's Telegram chat |
| `integrations.telegram.link.list` | GET | `/api/integrations/telegram/link` | Get (or issue) the caller's Telegram deep link |
| `integrations.test.create` | POST | `/api/integrations/{provider}/test` | Probe the stored credential against the provider's identity endpoint |
| `integrations.trello.import.preview.create` | POST | `/api/integrations/trello/import/preview` | Dry-run a Trello board export (admin) |
| `integrations.trello.import.run.create` | POST | `/api/integrations/trello/import/run` | Import a Trello board export as a new project (admin) |
| `integrations.trmnly.devices.list` | GET | `/api/integrations/trmnly/devices` | List the caller's TRMNLY Macs |
| `integrations.trmnly.devices.overview.list` | GET | `/api/integrations/trmnly/devices/{id}/overview` | What Kavanah can do on one TRMNLY Mac |
| `integrations.trmnly.devices.send-task.create` | POST | `/api/integrations/trmnly/devices/{id}/send-task` | Send a Kavanah task to a TRMNLY board on a Mac |
| `recurring-emails.list` | GET | `/api/recurring-emails` | List your recurring emails with their last result |
| `recurring-emails.send-now.create` | POST | `/api/recurring-emails/{id}/send-now` | Send one occurrence of a recurring email now |
| `recurring-emails.update` | PATCH | `/api/recurring-emails/{id}` | Save a recurring email's recipients or pause state |

---

### `browser.profiles.capture.create`

`POST /api/browser/profiles/{id}/capture`

Save a live session's signed-in state into a saved login

Both the profile and the session must be owned by the caller. Capturing from a merely-shared session would copy its owner's live login, so shared access is not enough. Scrappy rejects an empty capture rather than writing it, so a transient failure cannot wipe a working profile.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `sessionId` (string<uuid>, required)

### `browser.profiles.create`

`POST /api/browser/profiles`

Create an empty saved-login slot

Holds no login until captured from a live session, which the user must do by signing in themselves.

Body (application/json):
  - `label` (string, required)
  - `siteHint` (string)

### `browser.profiles.delete`

`DELETE /api/browser/profiles/{id}`

Permanently delete and revoke a saved login

The revocation path. Upstream is deleted first: losing the local record while the credential survives would leave it live and unreachable through the UI, and therefore unrevokable through it.

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `browser.profiles.list`

`GET /api/browser/profiles`

List the caller's saved logins

Owner-scoped with no share path. Returns labels and timestamps only — never cookies, localStorage, or passwords, none of which Kavanah stores.

### `browser.profiles.update`

`PATCH /api/browser/profiles/{id}`

Change a saved login's pinned network exit

Since 2026-08-24 a capture pins the live exit IP and user agent onto the profile automatically. Send `proxyUrl: null` to clear that pin without touching the login; a string re-pins it. Omitting the key is a 400, not a silent no-op. Upstream self-heals a pin that fails three times in thirty minutes, so this is for a pin that became WRONG rather than dead. Owner-scoped: a profile is only mutable by the member who created it.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `proxyUrl` (string) — null clears the pin; a string sets it.

### `browser.sessions.create`

`POST /api/browser/sessions`

Start a cloud browser session

Spends the user's Scrappy credits up front and meters per minute until released. Passing `profileId` reuses a saved login, so the browser starts already signed in.

Body (application/json):
  - `profileId` (string) — Saved login to start from. Must belong to the caller.
  - `title` (string)
  - `screenWidth` (integer)
  - `screenHeight` (integer)
  - `rotateEgress` (boolean) — Start on a fresh network exit, keeping the profile's cookies and user agent. The recovery from a 503 on a profile-backed session: the exit is what failed, so dropping the profile to escape it would discard the saved login too.

### `browser.sessions.delete`

`DELETE /api/browser/sessions/{id}`

Release a browser session

Owner-only. Frees capacity and stops the per-minute meter. The local record is marked ended even if the upstream release fails, so a dead session never lingers in the list looking usable.

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `browser.sessions.keep-awake.create`

`POST /api/browser/sessions/{id}/keep-awake`

Hold a session open while nobody is watching it

The viewer only pings keepalive while it is open and visible, so a closed or backgrounded tab lets the session idle out. This opts the session into being pinged by the browser-keepalive cron instead, up to a fixed cap. Every minute held awake is a minute of Scrappy runtime metering, so re-post with enabled=false when finished. Upstream's 12-hour absolute cap still applies underneath.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `enabled` (boolean, required) — true holds the session open (extending from now); false releases the hold.

### `browser.sessions.keepalive.create`

`POST /api/browser/sessions/{id}/keepalive`

Refresh a session's idle timer without acting on the page

Reaping is idle-based, so a human reading a page or completing MFA looks identical to an abandoned session. The viewer calls this while mounted and visible.

Path params (positional, in order):
  - `id`

### `browser.sessions.list`

`GET /api/browser/sessions`

List browser sessions visible to the caller

The caller's own sessions plus any shared with the workspace. `mine` distinguishes them; `profileBacked` marks a session started from a saved login.

### `browser.sessions.navigate.create`

`POST /api/browser/sessions/{id}/navigate`

Navigate a session to a URL

http/https only; Scrappy additionally blocks private and internal hosts. Available to anyone who may drive the session.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `url` (string, required)

### `browser.sessions.scrape-mode.create`

`POST /api/browser/sessions/{id}/scrape-mode`

Turn extraction rendering on or off for a live session

Extraction rendering blocks images, fonts, media and trackers, removes consent walls and unsticks fixed headers, so a page reads cleanly for scraping. A cloud browser session is shared with the human watching it, and they see the same stripped pages with nothing on screen explaining why — so this exists as a human-facing undo that does not require asking the agent to call its own tool. Not gated on browser_sessions_enabled: it spends nothing, acts on an already-live session, and is chiefly a restore. Drivable scope.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `enabled` (boolean, required) — true renders for extraction; false restores normal rendering. Applied persistently either way, so turning it off also clears the document-start script the agent installed.

### `browser.sessions.share.create`

`POST /api/browser/sessions/{id}/share`

Share a browser session with the workspace, or revoke sharing

Owner-only and revocable at any time. REFUSES a session started from a saved login: sharing one would sign every workspace member in as its owner. A CHECK constraint enforces the same rule at the table.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `shared` (boolean, required)

### `browser.sessions.viewer-token.create`

`POST /api/browser/sessions/{id}/viewer-token`

Mint a short-lived viewer URL for the embedded browser

Returns an absolute viewer URL with a ~5-minute signed token embedded, bound to (session, user). The Scrappy API key is never returned and never reaches the client. Available to anyone who may drive the session.

Path params (positional, in order):
  - `id`

### `github.app.install.list`

`GET /api/github/app/install`

Start the GitHub App install flow (302 redirects to github.com)

### `github.issue-sync.list`

`GET /api/github/issue-sync`

List connected GitHub repos and their issue-sync opt-in state

### `github.issue-sync.update`

`PATCH /api/github/issue-sync`

Enable or disable GitHub Issue sync for one repository

Turns two-way sync between a repo's GitHub Issues and Kavanah tasks on or off. Defaults to off. While enabled, `issues` webhook events create and update tasks, and task status changes close or reopen the linked issue. Admin only.

Body (application/json):
  - `repoExternalId` (string, required)
  - `enabled` (boolean, required)

### `github.oauth.start.list`

`GET /api/github/oauth/start`

Start the GitHub OAuth sign-in flow (302 redirects to github.com)

### `github.repos.list`

`GET /api/github/repos`

List GitHub repositories available to connect

### `github.status.list`

`GET /api/github/status`

Get the workspace GitHub connection status

### `github.sync.create`

`POST /api/github/sync`

Trigger a GitHub sync for connected repositories

Body (application/json):
  - `repoId` (string)

### `inbox.skipped.list`

`GET /api/inbox/skipped`

Mail Kavanah did not run your email rules on

The signed-in user's mirrored mail from the last 14 days that the sync bridge declined to fire email-received rules on, with the reason (`own_mail`, `auto_reply`, `calendar`, `backfill_declined`) and whether the user has since run their rules on it.

Query:
  - `provider` (string) — one of: `gmail`, `microsoft365`, `protonmail`, `icloud`

### `inbox.skipped.rescue.create`

`POST /api/inbox/skipped/{id}/rescue`

Run your email rules on one skipped message

Dispatches the email-received automation event for one skipped message, through the sync bridge's own dispatch (only the caller's own rules). Idempotent per message: a second call is a 409 and dispatches nothing.

Path params (positional, in order):
  - `id`

### `integrations.angelsend.actions.create`

`POST /api/integrations/angelsend/actions/{action}`

Execute one AngelSend api-gateway action

Run a single catalogued AngelSend action. The request body is the action's parameter object — see `GET /api/integrations/angelsend/actions` for each action's schema. Only the 81 catalogued actions are accepted, and parameters are validated (including rejection of unknown keys) before the call is made. For the multiplexed actions (`manage-*`, `configure-follow-up-rule`) the sub-operation goes in the body's `action` field.

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `action`

Body: application/json (free-form — pass with `--data`)

### `integrations.angelsend.actions.list`

`GET /api/integrations/angelsend/actions`

Search the AngelSend action catalogue

Browse or search the 81 AngelSend `api-gateway` actions Kavanah wires, each with its parameter schema, scope, and whether it is destructive or spends AngelSend AI credits. Pure catalogue data — makes no call to AngelSend, so it works without a connection.

Query:
  - `q` (string) — Free-text search over action names, summaries, and parameter names. Omit to list all.
  - `group` (string) — one of: `crm`, `contacts`, `inbox`, `compliance`, `intent`, `intelligence`, `quality`, `campaigns`, `knowledge`, `chatbots`, `platform`
  - `limit` (integer) — Max actions to return. Defaults to all.

### `integrations.angelsend.calendar.create`

`POST /api/integrations/angelsend/calendar`

Create an event on the connected AngelSend calendar

Body (application/json):
  - `title` (string)
  - `summary` (string) — Falls back to `title` if omitted.
  - `description` (string)
  - `start` (string<date-time>, required)
  - `end` (string<date-time>, required)
  - `location` (string)
  - `attendees` (object[])

### `integrations.angelsend.calendar.list`

`GET /api/integrations/angelsend/calendar`

List events from the connected AngelSend calendar

Query:
  - `from` (string<date-time>) — ISO timestamp window start (optional).
  - `to` (string<date-time>) — ISO timestamp window end (optional).

### `integrations.angelsend.contacts.list`

`GET /api/integrations/angelsend/contacts`

List leads / contacts from AngelSend

Newest first, at most 500. AngelSend's list-leads has NO offset or cursor, so there is no paging parameter here; `hasMore` says whether the list was cut off at `limit`. Page through a larger audience with a segment (the Deal Room audience sync pages segment membership).

Query:
  - `limit` (integer)
  - `search` (string) — Matches first name, last name, email or company.

### `integrations.angelsend.credits.list`

`GET /api/integrations/angelsend/credits`

Get the AngelSend credit balance for the connected account

### `integrations.angelsend.email.create`

`POST /api/integrations/angelsend/email`

Send email via AngelSend

Body (application/json):
  - `to` (string|string[], required)
  - `subject` (string, required)
  - `body` (string)
  - `html` (string)
  - `from` (string)
  - `replyTo` (string)
  - `cc` (string[])
  - `bcc` (string[])

### `integrations.angelsend.gmail.labels.list`

`GET /api/integrations/angelsend/gmail/labels`

List labels

### `integrations.angelsend.gmail.messages.list`

`GET /api/integrations/angelsend/gmail/messages`

List messages

### `integrations.angelsend.gmail.profile.list`

`GET /api/integrations/angelsend/gmail/profile`

List profile

### `integrations.angelsend.gmail.send.create`

`POST /api/integrations/angelsend/gmail/send`

Create send

Body: application/json (free-form — pass with `--data`)

### `integrations.angelsend.gmail.status.list`

`GET /api/integrations/angelsend/gmail/status`

List status

### `integrations.angelsend.gmail.thread.list`

`GET /api/integrations/angelsend/gmail/thread`

List thread

### `integrations.angelsend.oauth.mobile-start.list`

`GET /api/integrations/angelsend/oauth/mobile-start`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `integrations.angelsend.oauth.start.list`

`GET /api/integrations/angelsend/oauth/start`

List start

### `integrations.asana.import.preview.list`

`GET /api/integrations/asana/import/preview`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `integrations.asana.import.run.create`

`POST /api/integrations/asana/import/run`

(undocumented route — params unknown, pass them explicitly)

**Destructive** — needs `--yes` against a non-local base URL.

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `integrations.asana.tasks.create`

`POST /api/integrations/asana/tasks`

Create a task in an Asana workspace

Body (application/json):
  - `workspace` (string, required)
  - `name` (string, required)
  - `notes` (string)
  - `assignee` (string)
  - `dueOn` (string<date>)
  - `projects` (string[])

### `integrations.asana.tasks.delete`

`DELETE /api/integrations/asana/tasks/{gid}`

Delete task

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `gid`

### `integrations.asana.tasks.get`

`GET /api/integrations/asana/tasks/{gid}`

Fetch task

Path params (positional, in order):
  - `gid`

### `integrations.asana.tasks.list`

`GET /api/integrations/asana/tasks`

List Asana tasks (filtered by workspace or project)

Query:
  - `workspace` (string) — Workspace gid (required unless project is given).
  - `project` (string) — Project gid.
  - `assignee` (string) — User gid or `me`.
  - `limit` (integer)

### `integrations.asana.tasks.update`

`PATCH /api/integrations/asana/tasks/{gid}`

Update task

Path params (positional, in order):
  - `gid`

Body: application/json (free-form — pass with `--data`)

### `integrations.asana.users-me.list`

`GET /api/integrations/asana/users-me`

Get the connected Asana user's profile (name, email, workspaces)

### `integrations.asana.webhooks.register.create`

`POST /api/integrations/asana/webhooks/register`

Create register

Body: application/json (free-form — pass with `--data`)

### `integrations.asana.webhooks.register.delete`

`DELETE /api/integrations/asana/webhooks/register`

Delete register

**Destructive** — needs `--yes` against a non-local base URL.

### `integrations.asana.webhooks.register.list`

`GET /api/integrations/asana/webhooks/register`

List register

### `integrations.asana.workspaces.list`

`GET /api/integrations/asana/workspaces`

List Asana workspaces the connected account belongs to

### `integrations.cloudcode.ai.chat.create`

`POST /api/integrations/cloudcode/ai/chat`

Create chat

Body: application/json (free-form — pass with `--data`)

### `integrations.cloudcode.github.repos.list`

`GET /api/integrations/cloudcode/github/repos`

List repos

### `integrations.cloudcode.projects.create`

`POST /api/integrations/cloudcode/projects`

Create project

Body: application/json (free-form — pass with `--data`)

### `integrations.cloudcode.projects.deployments.create`

`POST /api/integrations/cloudcode/projects/{id}/deployments`

Create deployment

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `integrations.cloudcode.projects.deployments.list`

`GET /api/integrations/cloudcode/projects/{id}/deployments`

List deployments

Path params (positional, in order):
  - `id`

### `integrations.cloudcode.projects.files.delete`

`DELETE /api/integrations/cloudcode/projects/{id}/files/{path}`

Delete file

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`
  - `path`

### `integrations.cloudcode.projects.files.get`

`GET /api/integrations/cloudcode/projects/{id}/files/{path}`

Fetch file

Path params (positional, in order):
  - `id`
  - `path`

### `integrations.cloudcode.projects.files.list`

`GET /api/integrations/cloudcode/projects/{id}/files`

List files

Path params (positional, in order):
  - `id`

### `integrations.cloudcode.projects.files.set`

`PUT /api/integrations/cloudcode/projects/{id}/files`

Update files

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `integrations.cloudcode.projects.get`

`GET /api/integrations/cloudcode/projects/{id}`

Fetch project

Path params (positional, in order):
  - `id`

### `integrations.cloudcode.projects.list`

`GET /api/integrations/cloudcode/projects`

List projects

### `integrations.delete`

`DELETE /api/integrations/{provider}`

Disconnect the caller from a provider

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `provider`

### `integrations.docsend.ingest.create`

`POST /api/integrations/docsend/ingest`

Mint or rotate the DocSend ingest token

Issues a new ingest token and returns the full webhook URL to point a DocSend relay (typically a Zap) at. This is the ONLY response that ever carries the raw token. Rotating invalidates the previous URL immediately, which is the recovery path for a token that leaked through a Zapier task history or a screenshot. Admin only — the URL is a workspace-wide write credential.

### `integrations.docsend.ingest.delete`

`DELETE /api/integrations/docsend/ingest`

Disable the DocSend webhook path

Disables the webhook token. Deliberately a disable rather than a delete, so `lastEventAt` survives and "this used to work" stays answerable. Does not affect the notification-email ingest path, which has no token.

**Destructive** — needs `--yes` against a non-local base URL.

### `integrations.docsend.ingest.list`

`GET /api/integrations/docsend/ingest`

DocSend ingest status for the workspace

Whether a DocSend ingest token exists, its last four characters, and when a view event last arrived. Never returns the token itself — it is stored hashed and is readable exactly once, in the POST response. `lastEventAt` is the field that matters operationally: a token that exists but has never received an event means the relay was never finished, which is otherwise indistinguishable from "nobody has opened the document".

### `integrations.get`

`GET /api/integrations/{provider}`

Get a single provider plus the caller's connection (if any)

Path params (positional, in order):
  - `provider`

### `integrations.gmail.inbox.messages.list`

`GET /api/integrations/gmail/inbox/messages`

List Gmail messages, or fetch one with its body

Query:
  - `id` (string) — Fetch a single message including its body.
  - `q` (string) — Gmail search query.
  - `maxResults` (integer)
  - `pageToken` (string)

### `integrations.gmail.inbox.send.create`

`POST /api/integrations/gmail/inbox/send`

Send an email through the connected Gmail backend

Body (application/json):
  - `to` (string|string[], required)
  - `subject` (string, required)
  - `body` (string, required)
  - `from` (string)
  - `cc` (string[])
  - `bcc` (string[])
  - `is_html` (boolean)
  - `thread_id` (string) — Reply into an existing thread.

### `integrations.gmail.inbox.status.list`

`GET /api/integrations/gmail/inbox/status`

Gmail inbox connection status

Resolves whichever Gmail backend the user has connected — the AngelSend bridge first, then native Google OAuth. `has_gmail_read: false` on a connected account means the token predates the gmail.readonly scope and the user must reconnect (not connect).

### `integrations.gmail.messages.create`

`POST /api/integrations/gmail/messages`

Send a plain-text email through Gmail

Body (application/json):
  - `to` (string, required)
  - `subject` (string)
  - `body` (string)
  - `cc` (string)
  - `bcc` (string)
  - `replyTo` (string)

### `integrations.gmail.messages.delete`

`DELETE /api/integrations/gmail/messages/{id}`

Delete message

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `integrations.gmail.messages.get`

`GET /api/integrations/gmail/messages/{id}`

Fetch message

Path params (positional, in order):
  - `id`

### `integrations.gmail.messages.list`

`GET /api/integrations/gmail/messages`

List Gmail message ids (and threadIds)

Query:
  - `q` (string) — Gmail search query syntax.
  - `maxResults` (integer)
  - `pageToken` (string)

### `integrations.gmail.messages.update`

`PATCH /api/integrations/gmail/messages/{id}`

Update message

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `integrations.gmail.profile.list`

`GET /api/integrations/gmail/profile`

Get the connected Gmail account's profile (email, message counts)

### `integrations.gmail.push.create`

`POST /api/integrations/gmail/push`

Create push

Body: application/json (free-form — pass with `--data`)

### `integrations.gmail.watch.create`

`POST /api/integrations/gmail/watch`

Create watch

Body: application/json (free-form — pass with `--data`)

### `integrations.gmail.watch.delete`

`DELETE /api/integrations/gmail/watch`

Delete watch

**Destructive** — needs `--yes` against a non-local base URL.

### `integrations.google-calendar.calendars.list`

`GET /api/integrations/google-calendar/calendars`

List the user's Google calendars

### `integrations.google-calendar.events.create`

`POST /api/integrations/google-calendar/events`

Create an event on one of the user's Google calendars

Body (application/json):
  - `calendarId` (string) — Defaults to `primary`.
  - `summary` (string, required)
  - `description` (string)
  - `location` (string)
  - `start` (string<date-time>, required)
  - `end` (string<date-time>, required)
  - `timeZone` (string)
  - `attendees` (string[])
  - `sendUpdates` (string) — one of: `all`, `externalOnly`, `none`

### `integrations.google-calendar.events.delete`

`DELETE /api/integrations/google-calendar/events/{eventId}`

Delete event

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `eventId`

### `integrations.google-calendar.events.get`

`GET /api/integrations/google-calendar/events/{eventId}`

Fetch event

Path params (positional, in order):
  - `eventId`

### `integrations.google-calendar.events.list`

`GET /api/integrations/google-calendar/events`

List events from one of the user's Google calendars

Query:
  - `calendarId` (string) — Defaults to `primary`.
  - `timeMin` (string<date-time>) — Window start. Also accepts `from`.
  - `timeMax` (string<date-time>) — Window end. Also accepts `to`.
  - `from` (string<date-time>)
  - `to` (string<date-time>)
  - `maxResults` (integer)
  - `pageToken` (string)

### `integrations.google-calendar.events.update`

`PATCH /api/integrations/google-calendar/events/{eventId}`

Update event

Path params (positional, in order):
  - `eventId`

Body: application/json (free-form — pass with `--data`)

### `integrations.google-calendar.watch.create`

`POST /api/integrations/google-calendar/watch`

Create watch

Body: application/json (free-form — pass with `--data`)

### `integrations.google-calendar.watch.register.create`

`POST /api/integrations/google-calendar/watch/register`

Create register

Body: application/json (free-form — pass with `--data`)

### `integrations.google-calendar.watch.register.delete`

`DELETE /api/integrations/google-calendar/watch/register`

Delete register

**Destructive** — needs `--yes` against a non-local base URL.

### `integrations.google-drive.about.list`

`GET /api/integrations/google-drive/about`

Get the Drive account's identity and storage quota

### `integrations.google-drive.changes.create`

`POST /api/integrations/google-drive/changes`

Create change

Body: application/json (free-form — pass with `--data`)

### `integrations.google-drive.files.create`

`POST /api/integrations/google-drive/files`

Create a UTF-8 text file in Drive

Body (application/json):
  - `name` (string, required)
  - `content` (string) — UTF-8 file body. Defaults to empty string.
  - `mimeType` (string) — Defaults to `text/plain; charset=UTF-8`.
  - `parentFolderId` (string)

### `integrations.google-drive.files.delete`

`DELETE /api/integrations/google-drive/files/{fileId}`

Delete file

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `fileId`

### `integrations.google-drive.files.get`

`GET /api/integrations/google-drive/files/{fileId}`

Fetch file

Path params (positional, in order):
  - `fileId`

### `integrations.google-drive.files.list`

`GET /api/integrations/google-drive/files`

List Drive files visible to the app (drive.file scope)

Query:
  - `q` (string) — Drive query syntax.
  - `pageSize` (integer)
  - `pageToken` (string)

### `integrations.google-drive.files.update`

`PATCH /api/integrations/google-drive/files/{fileId}`

Update file

Path params (positional, in order):
  - `fileId`

Body: application/json (free-form — pass with `--data`)

### `integrations.google-drive.watch.create`

`POST /api/integrations/google-drive/watch`

Create watch

Body: application/json (free-form — pass with `--data`)

### `integrations.google-drive.watch.delete`

`DELETE /api/integrations/google-drive/watch`

Delete watch

**Destructive** — needs `--yes` against a non-local base URL.

### `integrations.google-drive.watch.list`

`GET /api/integrations/google-drive/watch`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `integrations.google-meet.imports.get`

`GET /api/integrations/google-meet/imports/{id}`

One of the caller's imported Google Meet calls, with its transcript

Path params (positional, in order):
  - `id`

### `integrations.google-meet.imports.list`

`GET /api/integrations/google-meet/imports`

The caller's Google Meet transcript import — settings and imported calls

Whether the workspace turned on the Google Meet transcript import (`google_meet_import_enabled`, Settings → AI Agent → Oversight), whether the caller opted out, whether their Google grant needs re-consent, and the caller's OWN imported calls, newest first (title, start, status, notes summary, created task ids, recording links, the linked deal). Never another member's calls.

### `integrations.google-meet.imports.update`

`PATCH /api/integrations/google-meet/imports`

Opt the caller out of (or back into) the Google Meet transcript import

Per-member opt-out within the workspace. Turning it on also stops the caller's calls still in flight (they become `stopped`); calls already imported are kept.

Body (application/json):
  - `optedOut` (boolean, required)

### `integrations.icloud.events.create`

`POST /api/integrations/icloud/events`

Create an iCloud calendar event

Body (application/json):
  - `summary` (string, required)
  - `start` (string<date-time>, required)
  - `end` (string<date-time>, required)
  - `location` (string)
  - `description` (string)

### `integrations.icloud.events.list`

`GET /api/integrations/icloud/events`

List iCloud calendar events (read live over CalDAV)

Query:
  - `timeMin` (string<date-time>) — Alias: from.
  - `timeMax` (string<date-time>) — Alias: to.

### `integrations.icloud.messages.create`

`POST /api/integrations/icloud/messages`

Send an email via iCloud SMTP

Body (application/json):
  - `to` (string, required)
  - `subject` (string, required)
  - `body` (string, required)
  - `cc` (string)
  - `bcc` (string)
  - `skipDefaultBcc` (boolean)

### `integrations.icloud.messages.list`

`GET /api/integrations/icloud/messages`

List synced iCloud Mail envelopes

Envelope-only (IMAP). Bodies are not synced.

Query:
  - `limit` (integer)

### `integrations.kanvo.agent.create`

`POST /api/integrations/kanvo/agent`

Kanvo connected-agent endpoint (called by Kanvo, not by clients)

Kanvo's "connected agents" feature POSTs each message in a Kanvo thread here and posts the answer into the chat as the agent. Authenticated by the Kanvo user's own Kavanah API key, configured in Kanvo as the credential header `Authorization: Bearer kvn_live_…`; app keys and browser sessions are refused. Each Kanvo thread (and branch) is one Kavanah agent conversation. A `ping` (Kanvo's "Send test") answers a greeting without running a turn. A delivery whose `action.id` is `undo:<group id>` (the Undo button on a "Done" card) reverses that agent turn instead of running one. Runs a full agent turn (credits are charged) stopped at ~80s, since Kanvo waits 100s. Setup: docs/kanvo-integration.md.

Body: application/json (free-form — pass with `--data`)

### `integrations.list`

`GET /api/integrations`

List available integration providers and the user's connections

### `integrations.microsoft365.events.create`

`POST /api/integrations/microsoft365/events`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `integrations.microsoft365.events.list`

`GET /api/integrations/microsoft365/events`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `integrations.microsoft365.messages.create`

`POST /api/integrations/microsoft365/messages`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `integrations.microsoft365.messages.list`

`GET /api/integrations/microsoft365/messages`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `integrations.monday.import.preview.create`

`POST /api/integrations/monday/import/preview`

Dry-run a Monday.com export (admin)

Body (application/json):
  - `content` (string, required)
  - `format` (string) — one of: `csv`, `json`

### `integrations.monday.import.run.create`

`POST /api/integrations/monday/import/run`

Import a Monday.com export as a new project (admin)

Idempotent — re-importing the same export skips instead of duplicating.

**Destructive** — needs `--yes` against a non-local base URL.

Body (application/json):
  - `content` (string, required)
  - `format` (string) — one of: `csv`, `json`
  - `projectName` (string)

### `integrations.multiverseai.agents.chat.create`

`POST /api/integrations/multiverseai/agents/{id}/chat`

Create chat

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `integrations.multiverseai.agents.get`

`GET /api/integrations/multiverseai/agents/{id}`

Fetch agent

Path params (positional, in order):
  - `id`

### `integrations.multiverseai.agents.list`

`GET /api/integrations/multiverseai/agents`

List agents

### `integrations.multiverseai.chat.create`

`POST /api/integrations/multiverseai/chat`

Create chat

Body: application/json (free-form — pass with `--data`)

### `integrations.multiverseai.models.list`

`GET /api/integrations/multiverseai/models`

List models

### `integrations.multiverseai.workflows.execute.create`

`POST /api/integrations/multiverseai/workflows/{id}/execute`

Create execute

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `integrations.multiverseai.workflows.get`

`GET /api/integrations/multiverseai/workflows/{id}`

Fetch workflow

Path params (positional, in order):
  - `id`

### `integrations.multiverseai.workflows.list`

`GET /api/integrations/multiverseai/workflows`

List workflows

### `integrations.notion.connect-token.create`

`POST /api/integrations/notion/connect-token`

Connect Notion with an internal integration token

Fallback for Notion's OAuth flow — paste an internal integration token (`secret_…` / `ntn_…`). The token is probed against /v1/users/me and persisted. POST and PUT behave identically.

Body (application/json):
  - `token` (string, required)

### `integrations.notion.connect-token.set`

`PUT /api/integrations/notion/connect-token`

Connect Notion with an internal integration token

Identical to POST.

Body (application/json):
  - `token` (string, required)

### `integrations.notion.import.create`

`POST /api/integrations/notion/import`

Import a Notion database into a project as tasks

**Destructive** — needs `--yes` against a non-local base URL.

Body (application/json):
  - `databaseId` (string, required)
  - `projectRef` (string, required)
  - `limit` (integer)

### `integrations.notion.import.list`

`GET /api/integrations/notion/import`

List the Notion databases the connection can see

### `integrations.oauth.handoff.create`

`POST /api/integrations/oauth/handoff`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `integrations.oauth.mobile-start.list`

`GET /api/integrations/{p1}/oauth/mobile-start`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `integrations.oauth.start.list`

`GET /api/integrations/{provider}/oauth/start`

Begin an OAuth2 authorization-code flow

Generates a state token, sets it on an httpOnly cookie, then redirects the browser to the provider's authorize URL. Only valid for providers with `authType: oauth2`.

Path params (positional, in order):
  - `provider`

### `integrations.protonmail.messages.create`

`POST /api/integrations/protonmail/messages`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `integrations.protonmail.messages.list`

`GET /api/integrations/protonmail/messages`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `integrations.scrappy.clients.push.create`

`POST /api/integrations/scrappy/clients/{id}/push`

Create push

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `integrations.set`

`PUT /api/integrations/{provider}`

Store an API-key credential for an api_key provider

Only valid when the provider's `authType` is `api_key` (currently AngelSend). For OAuth providers use `/api/integrations/{provider}/oauth/start`.

Path params (positional, in order):
  - `provider`

Body (application/json):
  - `apiKey` (string<password>, required)
  - `metadata` (object) — Optional caller-supplied display metadata to merge alongside derived metadata.

### `integrations.slack.auth-test.list`

`GET /api/integrations/slack/auth-test`

Run Slack's auth.test method (returns bot/user/team identity)

### `integrations.slack.channels.list`

`GET /api/integrations/slack/channels`

List channels visible to the connected Slack bot

Query:
  - `cursor` (string)
  - `limit` (integer)
  - `types` (string) — Slack `types` filter, e.g. `public_channel,private_channel`.
  - `excludeArchived` (boolean)

### `integrations.slack.events.create`

`POST /api/integrations/slack/events`

Create event

Body: application/json (free-form — pass with `--data`)

### `integrations.slack.messages.create`

`POST /api/integrations/slack/messages`

Post a message to a Slack channel via chat.postMessage

Body (application/json):
  - `channel` (string, required) — Channel id (C…) or `#name`.
  - `text` (string, required)
  - `threadTs` (string)

### `integrations.slack.messages.delete`

`DELETE /api/integrations/slack/messages`

Delete a Slack message via chat.delete

Accepts channel and ts either as query params or in a JSON body.

**Destructive** — needs `--yes` against a non-local base URL.

Query:
  - `channel` (string)
  - `ts` (string)

### `integrations.slack.messages.update`

`PATCH /api/integrations/slack/messages`

Edit a Slack message via chat.update

Body (application/json):
  - `channel` (string, required)
  - `ts` (string, required) — Timestamp id of the message to edit.
  - `text` (string, required)

### `integrations.slack.workspaces.delete`

`DELETE /api/integrations/slack/workspaces/{teamId}`

Remove one connected Slack workspace (not the default — Disconnect removes that)

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `teamId`

### `integrations.slack.workspaces.list`

`GET /api/integrations/slack/workspaces`

List the Slack workspaces the caller has connected, the default first

### `integrations.tavus.llm.chat.completions.create`

`POST /api/integrations/tavus/llm/{token}/chat/completions`

The video twin's brain — OpenAI-compatible endpoint Tavus calls

Path secret and bearer secret must both match the session. Answers from Kavanah's twin reasoning path with the hard limits applied; streams SSE unless `stream:false`.

Path params (positional, in order):
  - `token`

Body: application/json (free-form — pass with `--data`)

### `integrations.telegram.auth-test.list`

`GET /api/integrations/telegram/auth-test`

List auth test

### `integrations.telegram.link.delete`

`DELETE /api/integrations/telegram/link`

Unlink the caller's Telegram chat

**Destructive** — needs `--yes` against a non-local base URL.

### `integrations.telegram.link.list`

`GET /api/integrations/telegram/link`

Get (or issue) the caller's Telegram deep link

Returns the signed-in user's Telegram binding. When the user is not yet linked, issues a single-use `t.me/<bot>?start=<token>` deep link that binds their Telegram chat to their Kavanah account once they press Start. The bot itself is installed once per workspace (a BotFather token on the Telegram integration); the link is per user.

### `integrations.test.create`

`POST /api/integrations/{provider}/test`

Probe the stored credential against the provider's identity endpoint

Calls the provider's "who am I" endpoint (AngelSend connection-status, Gmail profile, Drive about, Slack auth.test, Asana /users/me, Google Calendar calendarList) and updates the connection's status + metadata based on the result.

Path params (positional, in order):
  - `provider`

### `integrations.trello.import.preview.create`

`POST /api/integrations/trello/import/preview`

Dry-run a Trello board export (admin)

Body (application/json):
  - `content` (string, required) — Trello board JSON export.

### `integrations.trello.import.run.create`

`POST /api/integrations/trello/import/run`

Import a Trello board export as a new project (admin)

Idempotent — re-importing the same board skips instead of duplicating.

**Destructive** — needs `--yes` against a non-local base URL.

Body (application/json):
  - `content` (string, required)
  - `projectName` (string)

### `integrations.trmnly.devices.list`

`GET /api/integrations/trmnly/devices`

List the caller's TRMNLY Macs

Macs on the caller's TRMNLY account (phones, browsers and API tokens are left out). `online` = tunnel up and a heartbeat in the last 10 minutes. 412 when TRMNLY is not connected.

### `integrations.trmnly.devices.overview.list`

`GET /api/integrations/trmnly/devices/{id}/overview`

What Kavanah can do on one TRMNLY Mac

Remote-policy capabilities for the tools Kavanah uses, the Mac's TRMNLY projects, and recent Claude Code sessions for `cwd` (default: the focused project's folder). A failing sub-call is reported in `warnings` and does not fail the response; an offline Mac is 503.

Path params (positional, in order):
  - `id`

Query:
  - `cwd` (string)

### `integrations.trmnly.devices.send-task.create`

`POST /api/integrations/trmnly/devices/{id}/send-task`

Send a Kavanah task to a TRMNLY board on a Mac

Adds a card (`[<project> #<id>] <title>`, body = the task context bundle, a "Kavanah" link, label `kavanah`) via the Mac's `kanban_add`; with `start: claude` it then opens a tab in that TRMNLY project's folder running `claude '<prompt>'` that picks up the card. The caller must be able to view the task (same gate as `GET /api/tasks/{id}`). The Mac's remote policy applies: a refused or unapproved card is 403 with `approval`; a refused tab still returns the card with `approval`.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `taskId` (integer, required)
  - `projectName` (string)
  - `board` (string)
  - `start` (string) — one of: `none`, `claude`

### `recurring-emails.list`

`GET /api/recurring-emails`

List your recurring emails with their last result

The signed-in user's recurring emails in the active workspace (a recurring email belongs to its sender), each with `lastSentAt`, `lastError`, `consecutiveFailures` and `nextRunAt`.

### `recurring-emails.send-now.create`

`POST /api/recurring-emails/{id}/send-now`

Send one occurrence of a recurring email now

Sends through the recurring-emails cron's own single-row send (archive BCC, suppression, audit, failure streak all apply) without moving the schedule. Leased: a concurrent second call is a 409, and so is a call while the scheduled occurrence is due. `ok` is true only when a copy went out; `outcome.status` is `sent`, `suppressed` or `failed`.

Path params (positional, in order):
  - `id`

### `recurring-emails.update`

`PATCH /api/recurring-emails/{id}`

Save a recurring email's recipients or pause state

Accepts `to`, `cc`, `bcc` (arrays or comma-separated strings) and `enabled`. Addresses are validated, lowercased and deduped. The response carries `warnings` and `outsideRecipients` naming recipients who are not members of the workspace — a warning only; the save is never blocked.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `to` (string[]|string)
  - `cc` (string[]|string)
  - `bcc` (string[]|string)
  - `enabled` (boolean)

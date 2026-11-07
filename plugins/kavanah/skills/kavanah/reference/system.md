# System

11 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `app-config.public.list` | GET | `/api/app-config/public` | List public |
| `company-logo.list` | GET | `/api/company-logo` | List company logo |
| `company-preview.list` | GET | `/api/company-preview` | List company preview |
| `desktop.download.list` | GET | `/api/desktop/download` | Redirect to the current installer for a platform |
| `desktop.latest.list` | GET | `/api/desktop/latest` | Desktop updater manifest |
| `system.health.list` | GET | `/api/system/health` | List health |
| `track.session.create` | POST | `/api/track/session` | Record a session-start heartbeat |
| `undo.create` | POST | `/api/undo` | Create undo |
| `undo.list` | GET | `/api/undo` | List undo |
| `undo.redo.create` | POST | `/api/undo/redo` | Create redo |
| `uploads.get` | GET | `/api/uploads/{path}` | Fetch upload |

---

### `app-config.public.list`

`GET /api/app-config/public`

List public

### `company-logo.list`

`GET /api/company-logo`

List company logo

### `company-preview.list`

`GET /api/company-preview`

List company preview

### `desktop.download.list`

`GET /api/desktop/download`

Redirect to the current installer for a platform

Public, no auth. Looks up the published installer in Blob storage and 302-redirects to it. `mac` (the default) reads the native Mac release manifest and only redirects to a DMG under that release's own prefix; `mac-classic`, `windows`, `android` and `android-manifest` redirect to fixed published objects. Never falls back to a different app.

Query:
  - `platform` (string) — one of: `mac`, `mac-classic`, `windows`, `android`, `android-manifest`

### `desktop.latest.list`

`GET /api/desktop/latest`

Desktop updater manifest

Public, no auth. Proxies the updater manifest JSON from Blob storage for the desktop shells (no channel) or the native Mac app (`channel=macos-native`). Every failure, an unknown channel, or an unpublished manifest answers 204, which the updater reads as "no update available".

Query:
  - `channel` (string) — one of: `macos-native`

### `system.health.list`

`GET /api/system/health`

List health

### `track.session.create`

`POST /api/track/session`

Record a session-start heartbeat

Records a session_start usage event for active-user metrics, at most once per user per 6 hours.

### `undo.create`

`POST /api/undo`

Create undo

Body: application/json (free-form — pass with `--data`)

### `undo.list`

`GET /api/undo`

List undo

### `undo.redo.create`

`POST /api/undo/redo`

Create redo

Body: application/json (free-form — pass with `--data`)

### `uploads.get`

`GET /api/uploads/{path}`

Fetch upload

Serves a stored file after the same access check the screen that lists it applies, not just workspace membership: a project document needs access to its project, a task attachment needs access to the task (including the per-task ACL), a call recording needs participation in the call, and an agent chat attachment belongs to its owner. Guests are held to their project scope and expiry. Only branding, forecast-chart, profile-media and project-icon paths are readable without a session. HTML and SVG are never served inline; every response carries `X-Content-Type-Options: nosniff` and a sandboxing CSP.

Path params (positional, in order):
  - `path`

# apps

11 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `apps.install.create` | POST | `/api/apps/{slug}/install` | Install a community app for the workspace with granted scopes |
| `apps.installs.delete` | DELETE | `/api/apps/installs/{id}` | Uninstall a community app from the workspace |
| `apps.installs.keys.create` | POST | `/api/apps/installs/{id}/keys` | Mint a per-app API key for an installed app (returned once) |
| `apps.installs.keys.delete` | DELETE | `/api/apps/installs/{id}/keys/{keyId}` | Revoke a single per-app API key |
| `apps.installs.keys.list` | GET | `/api/apps/installs/{id}/keys` | List an installed app's API keys (metadata only) |
| `apps.installs.secret.create` | POST | `/api/apps/installs/{id}/secret` | Mint or rotate an install's webhook signing secret (returned once) |
| `apps.installs.update` | PATCH | `/api/apps/installs/{id}` | Reconfigure an installed app (enable, agent access, embedded UI, scopes) |
| `apps.list` | GET | `/api/apps` | List the workspace's installed community apps |
| `apps.surfaces.get` | GET | `/api/apps/surfaces/{slug}/{surfaceId}` | Resolve an installed app's UI surface and mint its embed token |
| `marketplace.get` | GET | `/api/marketplace/{slug}` | Get one community app's detail and install state |
| `marketplace.list` | GET | `/api/marketplace` | List community apps visible to the workspace, with install state |

---

### `apps.install.create`

`POST /api/apps/{slug}/install`

Install a community app for the workspace with granted scopes

Path params (positional, in order):
  - `slug`

Body (application/json):
  - `grantedScopes` (string[])
  - `agentAccess` (boolean)

### `apps.installs.delete`

`DELETE /api/apps/installs/{id}`

Uninstall a community app from the workspace

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `apps.installs.keys.create`

`POST /api/apps/installs/{id}/keys`

Mint a per-app API key for an installed app (returned once)

Path params (positional, in order):
  - `id`

Body (application/json):
  - `name` (string)

### `apps.installs.keys.delete`

`DELETE /api/apps/installs/{id}/keys/{keyId}`

Revoke a single per-app API key

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`
  - `keyId`

### `apps.installs.keys.list`

`GET /api/apps/installs/{id}/keys`

List an installed app's API keys (metadata only)

Path params (positional, in order):
  - `id`

### `apps.installs.secret.create`

`POST /api/apps/installs/{id}/secret`

Mint or rotate an install's webhook signing secret (returned once)

Path params (positional, in order):
  - `id`

### `apps.installs.update`

`PATCH /api/apps/installs/{id}`

Reconfigure an installed app (enable, agent access, embedded UI, scopes)

Path params (positional, in order):
  - `id`

Body (application/json):
  - `enabled` (boolean)
  - `agentAccess` (boolean)
  - `uiAccess` (boolean)
  - `grantedScopes` (string[])

### `apps.list`

`GET /api/apps`

List the workspace's installed community apps

### `apps.surfaces.get`

`GET /api/apps/surfaces/{slug}/{surfaceId}`

Resolve an installed app's UI surface and mint its embed token

Path params (positional, in order):
  - `slug`
  - `surfaceId`

### `marketplace.get`

`GET /api/marketplace/{slug}`

Get one community app's detail and install state

Path params (positional, in order):
  - `slug`

### `marketplace.list`

`GET /api/marketplace`

List community apps visible to the workspace, with install state

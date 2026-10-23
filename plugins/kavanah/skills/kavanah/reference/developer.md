# developer

11 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `developer.apps.create` | POST | `/api/developer/apps` | Create a new private community app from a manifest |
| `developer.apps.delete` | DELETE | `/api/developer/apps/{slug}` | Delete a private app the workspace owns |
| `developer.apps.draft-manifest.create` | POST | `/api/developer/apps/draft-manifest` | Draft an app manifest from a plain-English description (AI) |
| `developer.apps.get` | GET | `/api/developer/apps/{slug}` | Get authoring detail for one owned app (manifest + versions) |
| `developer.apps.list` | GET | `/api/developer/apps` | List community apps this workspace owns (developer console) |
| `developer.apps.reachability.create` | POST | `/api/developer/apps/{slug}/reachability` | Check whether an owned app's tool endpoint is reachable |
| `developer.apps.submit.create` | POST | `/api/developer/apps/{slug}/submit` | Submit an app version for platform review (public listing) |
| `developer.apps.test-tool.create` | POST | `/api/developer/apps/{slug}/test-tool` | Send a signed test call to an owned app's tool endpoint |
| `developer.apps.versions.create` | POST | `/api/developer/apps/{slug}/versions` | Publish a new version of an owned app from a manifest |
| `developer.apps.versions.delete` | DELETE | `/api/developer/apps/{slug}/versions/{id}` | Delete a draft or rejected version of an owned app |
| `developer.apps.versions.rollback.create` | POST | `/api/developer/apps/{slug}/versions/{id}/rollback` | Set an older version of an owned app as the current version |

---

### `developer.apps.create`

`POST /api/developer/apps`

Create a new private community app from a manifest

### `developer.apps.delete`

`DELETE /api/developer/apps/{slug}`

Delete a private app the workspace owns

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `slug`

### `developer.apps.draft-manifest.create`

`POST /api/developer/apps/draft-manifest`

Draft an app manifest from a plain-English description (AI)

Body (application/json):
  - `description` (string, required)

### `developer.apps.get`

`GET /api/developer/apps/{slug}`

Get authoring detail for one owned app (manifest + versions)

Path params (positional, in order):
  - `slug`

### `developer.apps.list`

`GET /api/developer/apps`

List community apps this workspace owns (developer console)

### `developer.apps.reachability.create`

`POST /api/developer/apps/{slug}/reachability`

Check whether an owned app's tool endpoint is reachable

Path params (positional, in order):
  - `slug`

### `developer.apps.submit.create`

`POST /api/developer/apps/{slug}/submit`

Submit an app version for platform review (public listing)

Path params (positional, in order):
  - `slug`

Body (application/json):
  - `versionId` (string, required)

### `developer.apps.test-tool.create`

`POST /api/developer/apps/{slug}/test-tool`

Send a signed test call to an owned app's tool endpoint

Path params (positional, in order):
  - `slug`

### `developer.apps.versions.create`

`POST /api/developer/apps/{slug}/versions`

Publish a new version of an owned app from a manifest

Path params (positional, in order):
  - `slug`

### `developer.apps.versions.delete`

`DELETE /api/developer/apps/{slug}/versions/{id}`

Delete a draft or rejected version of an owned app

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `slug`
  - `id`

### `developer.apps.versions.rollback.create`

`POST /api/developer/apps/{slug}/versions/{id}/rollback`

Set an older version of an owned app as the current version

Path params (positional, in order):
  - `slug`
  - `id`

# Admin

27 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `admin.scim.logs.list` | GET | `/api/admin/scim/logs` | List logs |
| `admin.scim.providers.create` | POST | `/api/admin/scim/providers` | Create provider |
| `admin.scim.providers.delete` | DELETE | `/api/admin/scim/providers/{providerId}` | Delete provider |
| `admin.scim.providers.get` | GET | `/api/admin/scim/providers/{providerId}` | Fetch provider |
| `admin.scim.providers.list` | GET | `/api/admin/scim/providers` | List providers |
| `admin.scim.providers.mappings.create` | POST | `/api/admin/scim/providers/{providerId}/mappings` | Create mapping |
| `admin.scim.providers.mappings.delete` | DELETE | `/api/admin/scim/providers/{providerId}/mappings/{mappingId}` | Delete mapping |
| `admin.scim.providers.mappings.list` | GET | `/api/admin/scim/providers/{providerId}/mappings` | List mappings |
| `admin.scim.providers.resync.create` | POST | `/api/admin/scim/providers/{providerId}/resync` | Create resync |
| `admin.scim.providers.tokens.create` | POST | `/api/admin/scim/providers/{providerId}/tokens` | Create token |
| `admin.scim.providers.tokens.delete` | DELETE | `/api/admin/scim/providers/{providerId}/tokens/{tokenId}` | Delete token |
| `admin.scim.providers.tokens.list` | GET | `/api/admin/scim/providers/{providerId}/tokens` | List tokens |
| `admin.scim.providers.update` | PATCH | `/api/admin/scim/providers/{providerId}` | Update provider |
| `admin.security.domains.create` | POST | `/api/admin/security/domains` | Create domain |
| `admin.security.domains.delete` | DELETE | `/api/admin/security/domains/{id}` | Delete domain |
| `admin.security.domains.list` | GET | `/api/admin/security/domains` | List domains |
| `admin.security.ip-allowlist.create` | POST | `/api/admin/security/ip-allowlist` | Create ip allowlist |
| `admin.security.ip-allowlist.delete` | DELETE | `/api/admin/security/ip-allowlist/{id}` | Delete ip allowlist |
| `admin.security.ip-allowlist.list` | GET | `/api/admin/security/ip-allowlist` | List ip allowlist |
| `admin.security.policies.create` | POST | `/api/admin/security/policies` | Create a security policy |
| `admin.security.policies.list` | GET | `/api/admin/security/policies` | List policies |
| `admin.security.sessions.delete` | DELETE | `/api/admin/security/sessions/{sessionId}` | Delete session |
| `admin.security.sessions.list` | GET | `/api/admin/security/sessions` | List sessions |
| `admin.security.sso.create` | POST | `/api/admin/security/sso` | Create sso |
| `admin.security.sso.list` | GET | `/api/admin/security/sso` | List sso |
| `admin.users.duplicates.list` | GET | `/api/admin/users/duplicates` | List duplicates |
| `admin.users.merge.create` | POST | `/api/admin/users/merge` | Create merge |

---

### `admin.scim.logs.list`

`GET /api/admin/scim/logs`

List logs

### `admin.scim.providers.create`

`POST /api/admin/scim/providers`

Create provider

Body: application/json (free-form — pass with `--data`)

### `admin.scim.providers.delete`

`DELETE /api/admin/scim/providers/{providerId}`

Delete provider

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `providerId`

### `admin.scim.providers.get`

`GET /api/admin/scim/providers/{providerId}`

Fetch provider

Path params (positional, in order):
  - `providerId`

### `admin.scim.providers.list`

`GET /api/admin/scim/providers`

List providers

### `admin.scim.providers.mappings.create`

`POST /api/admin/scim/providers/{providerId}/mappings`

Create mapping

Path params (positional, in order):
  - `providerId`

Body: application/json (free-form — pass with `--data`)

### `admin.scim.providers.mappings.delete`

`DELETE /api/admin/scim/providers/{providerId}/mappings/{mappingId}`

Delete mapping

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `providerId`
  - `mappingId`

### `admin.scim.providers.mappings.list`

`GET /api/admin/scim/providers/{providerId}/mappings`

List mappings

Path params (positional, in order):
  - `providerId`

### `admin.scim.providers.resync.create`

`POST /api/admin/scim/providers/{providerId}/resync`

Create resync

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `providerId`

Body: application/json (free-form — pass with `--data`)

### `admin.scim.providers.tokens.create`

`POST /api/admin/scim/providers/{providerId}/tokens`

Create token

Mint an additional bearer token for this provider (credential rotation). The plaintext `bearerToken` is returned exactly once and cannot be retrieved again.

Path params (positional, in order):
  - `providerId`

Body (application/json):
  - `label` (string)

### `admin.scim.providers.tokens.delete`

`DELETE /api/admin/scim/providers/{providerId}/tokens/{tokenId}`

Delete token

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `providerId`
  - `tokenId`

### `admin.scim.providers.tokens.list`

`GET /api/admin/scim/providers/{providerId}/tokens`

List tokens

Bearer tokens for this SCIM provider, newest first. Revoked tokens are included. The plaintext token is never returned — only its hash is stored.

Path params (positional, in order):
  - `providerId`

### `admin.scim.providers.update`

`PATCH /api/admin/scim/providers/{providerId}`

Update provider

Path params (positional, in order):
  - `providerId`

Body: application/json (free-form — pass with `--data`)

### `admin.security.domains.create`

`POST /api/admin/security/domains`

Create domain

Body: application/json (free-form — pass with `--data`)

### `admin.security.domains.delete`

`DELETE /api/admin/security/domains/{id}`

Delete domain

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `admin.security.domains.list`

`GET /api/admin/security/domains`

List domains

### `admin.security.ip-allowlist.create`

`POST /api/admin/security/ip-allowlist`

Create ip allowlist

Body: application/json (free-form — pass with `--data`)

### `admin.security.ip-allowlist.delete`

`DELETE /api/admin/security/ip-allowlist/{id}`

Delete ip allowlist

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `admin.security.ip-allowlist.list`

`GET /api/admin/security/ip-allowlist`

List ip allowlist

### `admin.security.policies.create`

`POST /api/admin/security/policies`

Create a security policy

Body: application/json (free-form — pass with `--data`)

### `admin.security.policies.list`

`GET /api/admin/security/policies`

List policies

### `admin.security.sessions.delete`

`DELETE /api/admin/security/sessions/{sessionId}`

Delete session

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `sessionId`

### `admin.security.sessions.list`

`GET /api/admin/security/sessions`

List sessions

### `admin.security.sso.create`

`POST /api/admin/security/sso`

Create sso

Body: application/json (free-form — pass with `--data`)

### `admin.security.sso.list`

`GET /api/admin/security/sso`

List sso

### `admin.users.duplicates.list`

`GET /api/admin/users/duplicates`

List duplicates

### `admin.users.merge.create`

`POST /api/admin/users/merge`

Create merge

**Destructive** — needs `--yes` against a non-local base URL.

Body: application/json (free-form — pass with `--data`)

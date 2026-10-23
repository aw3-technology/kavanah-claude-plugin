# RBAC

46 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `rbac.access-audit.list` | GET | `/api/rbac/access-audit` | List access audit |
| `rbac.audit.list` | GET | `/api/rbac/audit` | List audit |
| `rbac.default-permissions.list` | GET | `/api/rbac/default-permissions` | List default permissions |
| `rbac.default-permissions.set` | PUT | `/api/rbac/default-permissions` | Update default permissions |
| `rbac.departments.create` | POST | `/api/rbac/departments` | Create department |
| `rbac.departments.delete` | DELETE | `/api/rbac/departments/{id}` | Delete department |
| `rbac.departments.list` | GET | `/api/rbac/departments` | List departments |
| `rbac.departments.members.create` | POST | `/api/rbac/departments/{id}/members` | Create member |
| `rbac.departments.members.delete` | DELETE | `/api/rbac/departments/{id}/members` | Delete members |
| `rbac.departments.members.list` | GET | `/api/rbac/departments/{id}/members` | List members |
| `rbac.departments.update` | PATCH | `/api/rbac/departments/{id}` | Update department |
| `rbac.explorer.list` | GET | `/api/rbac/explorer` | List explorer |
| `rbac.field-permissions.delete` | DELETE | `/api/rbac/field-permissions` | Delete field permissions |
| `rbac.field-permissions.list` | GET | `/api/rbac/field-permissions` | List field permissions |
| `rbac.field-permissions.set` | PUT | `/api/rbac/field-permissions` | Update field permissions |
| `rbac.project-overrides.delete` | DELETE | `/api/rbac/project-overrides` | Delete project overrides |
| `rbac.project-overrides.list` | GET | `/api/rbac/project-overrides` | List project overrides |
| `rbac.project-overrides.set` | PUT | `/api/rbac/project-overrides` | Update project overrides |
| `rbac.project-visibility.delete` | DELETE | `/api/rbac/project-visibility` | Delete project visibility |
| `rbac.project-visibility.list` | GET | `/api/rbac/project-visibility` | List project visibility |
| `rbac.project-visibility.set` | PUT | `/api/rbac/project-visibility` | Update project visibility |
| `rbac.role-change-requests.create` | POST | `/api/rbac/role-change-requests` | Create role change request |
| `rbac.role-change-requests.list` | GET | `/api/rbac/role-change-requests` | List role change requests |
| `rbac.role-change-requests.update` | PATCH | `/api/rbac/role-change-requests/{id}` | Update role change request |
| `rbac.roles.create` | POST | `/api/rbac/roles` | Create role |
| `rbac.roles.delete` | DELETE | `/api/rbac/roles/{id}` | Delete role |
| `rbac.roles.duplicate.create` | POST | `/api/rbac/roles/{id}/duplicate` | Create duplicate |
| `rbac.roles.get` | GET | `/api/rbac/roles/{id}` | Fetch role |
| `rbac.roles.list` | GET | `/api/rbac/roles` | List roles |
| `rbac.roles.preview.list` | GET | `/api/rbac/roles/{id}/preview` | List preview |
| `rbac.roles.update` | PATCH | `/api/rbac/roles/{id}` | Update role |
| `rbac.share-links.delete` | DELETE | `/api/rbac/share-links/{id}` | Delete share link |
| `rbac.share-links.list` | GET | `/api/rbac/share-links` | List share links |
| `rbac.share-links.update` | PATCH | `/api/rbac/share-links/{id}` | Update share link |
| `rbac.sharing-controls.list` | GET | `/api/rbac/sharing-controls` | List sharing controls |
| `rbac.sharing-controls.set` | PUT | `/api/rbac/sharing-controls` | Update sharing controls |
| `rbac.team-permissions.delete` | DELETE | `/api/rbac/team-permissions` | Delete team permissions |
| `rbac.team-permissions.list` | GET | `/api/rbac/team-permissions` | List team permissions |
| `rbac.team-permissions.set` | PUT | `/api/rbac/team-permissions` | Update team permissions |
| `rbac.time-bound-grants.create` | POST | `/api/rbac/time-bound-grants` | Create time bound grant |
| `rbac.time-bound-grants.delete` | DELETE | `/api/rbac/time-bound-grants/{id}` | Delete time bound grant |
| `rbac.time-bound-grants.list` | GET | `/api/rbac/time-bound-grants` | List time bound grants |
| `rbac.user-roles.list` | GET | `/api/rbac/user-roles` | List user roles |
| `rbac.user-roles.set` | PUT | `/api/rbac/user-roles` | Update user roles |
| `rbac.users.departments.list` | GET | `/api/rbac/users/{p1}/departments` | (undocumented route — params unknown, pass them explicitly) |
| `rbac.users.departments.set` | PUT | `/api/rbac/users/{p1}/departments` | (undocumented route — params unknown, pass them explicitly) |

---

### `rbac.access-audit.list`

`GET /api/rbac/access-audit`

List access audit

### `rbac.audit.list`

`GET /api/rbac/audit`

List audit

### `rbac.default-permissions.list`

`GET /api/rbac/default-permissions`

List default permissions

### `rbac.default-permissions.set`

`PUT /api/rbac/default-permissions`

Update default permissions

Body: application/json (free-form — pass with `--data`)

### `rbac.departments.create`

`POST /api/rbac/departments`

Create department

Body: application/json (free-form — pass with `--data`)

### `rbac.departments.delete`

`DELETE /api/rbac/departments/{id}`

Delete department

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `rbac.departments.list`

`GET /api/rbac/departments`

List departments

### `rbac.departments.members.create`

`POST /api/rbac/departments/{id}/members`

Create member

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `rbac.departments.members.delete`

`DELETE /api/rbac/departments/{id}/members`

Delete members

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `rbac.departments.members.list`

`GET /api/rbac/departments/{id}/members`

List members

Path params (positional, in order):
  - `id`

### `rbac.departments.update`

`PATCH /api/rbac/departments/{id}`

Update department

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `rbac.explorer.list`

`GET /api/rbac/explorer`

List explorer

### `rbac.field-permissions.delete`

`DELETE /api/rbac/field-permissions`

Delete field permissions

**Destructive** — needs `--yes` against a non-local base URL.

### `rbac.field-permissions.list`

`GET /api/rbac/field-permissions`

List field permissions

### `rbac.field-permissions.set`

`PUT /api/rbac/field-permissions`

Update field permissions

Body: application/json (free-form — pass with `--data`)

### `rbac.project-overrides.delete`

`DELETE /api/rbac/project-overrides`

Delete project overrides

**Destructive** — needs `--yes` against a non-local base URL.

### `rbac.project-overrides.list`

`GET /api/rbac/project-overrides`

List project overrides

### `rbac.project-overrides.set`

`PUT /api/rbac/project-overrides`

Update project overrides

Body: application/json (free-form — pass with `--data`)

### `rbac.project-visibility.delete`

`DELETE /api/rbac/project-visibility`

Delete project visibility

**Destructive** — needs `--yes` against a non-local base URL.

### `rbac.project-visibility.list`

`GET /api/rbac/project-visibility`

List project visibility

### `rbac.project-visibility.set`

`PUT /api/rbac/project-visibility`

Update project visibility

Body: application/json (free-form — pass with `--data`)

### `rbac.role-change-requests.create`

`POST /api/rbac/role-change-requests`

Create role change request

Body: application/json (free-form — pass with `--data`)

### `rbac.role-change-requests.list`

`GET /api/rbac/role-change-requests`

List role change requests

### `rbac.role-change-requests.update`

`PATCH /api/rbac/role-change-requests/{id}`

Update role change request

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `rbac.roles.create`

`POST /api/rbac/roles`

Create role

Body: application/json (free-form — pass with `--data`)

### `rbac.roles.delete`

`DELETE /api/rbac/roles/{id}`

Delete role

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `rbac.roles.duplicate.create`

`POST /api/rbac/roles/{id}/duplicate`

Create duplicate

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `rbac.roles.get`

`GET /api/rbac/roles/{id}`

Fetch role

Path params (positional, in order):
  - `id`

### `rbac.roles.list`

`GET /api/rbac/roles`

List roles

### `rbac.roles.preview.list`

`GET /api/rbac/roles/{id}/preview`

List preview

Path params (positional, in order):
  - `id`

### `rbac.roles.update`

`PATCH /api/rbac/roles/{id}`

Update role

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `rbac.share-links.delete`

`DELETE /api/rbac/share-links/{id}`

Delete share link

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `rbac.share-links.list`

`GET /api/rbac/share-links`

List share links

### `rbac.share-links.update`

`PATCH /api/rbac/share-links/{id}`

Update share link

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `rbac.sharing-controls.list`

`GET /api/rbac/sharing-controls`

List sharing controls

### `rbac.sharing-controls.set`

`PUT /api/rbac/sharing-controls`

Update sharing controls

Body: application/json (free-form — pass with `--data`)

### `rbac.team-permissions.delete`

`DELETE /api/rbac/team-permissions`

Delete team permissions

**Destructive** — needs `--yes` against a non-local base URL.

### `rbac.team-permissions.list`

`GET /api/rbac/team-permissions`

List team permissions

### `rbac.team-permissions.set`

`PUT /api/rbac/team-permissions`

Update team permissions

Body: application/json (free-form — pass with `--data`)

### `rbac.time-bound-grants.create`

`POST /api/rbac/time-bound-grants`

Create time bound grant

Body: application/json (free-form — pass with `--data`)

### `rbac.time-bound-grants.delete`

`DELETE /api/rbac/time-bound-grants/{id}`

Delete time bound grant

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `rbac.time-bound-grants.list`

`GET /api/rbac/time-bound-grants`

List time bound grants

### `rbac.user-roles.list`

`GET /api/rbac/user-roles`

List user roles

### `rbac.user-roles.set`

`PUT /api/rbac/user-roles`

Update user roles

Body: application/json (free-form — pass with `--data`)

### `rbac.users.departments.list`

`GET /api/rbac/users/{p1}/departments`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `rbac.users.departments.set`

`PUT /api/rbac/users/{p1}/departments`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

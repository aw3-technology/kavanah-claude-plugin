# Custom Fields

10 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `custom-fields.create` | POST | `/api/custom-fields` | Create custom field |
| `custom-fields.delete` | DELETE | `/api/custom-fields/{id}` | Delete custom field |
| `custom-fields.list` | GET | `/api/custom-fields` | List custom fields |
| `custom-fields.set` | PUT | `/api/custom-fields/{id}` | Update custom field |
| `custom-properties.create` | POST | `/api/custom-properties` | Create a custom property definition |
| `custom-properties.delete` | DELETE | `/api/custom-properties/{id}` | Delete a custom property definition |
| `custom-properties.list` | GET | `/api/custom-properties` | List custom property definitions |
| `custom-properties.update` | PATCH | `/api/custom-properties/{id}` | Update a custom property definition |
| `custom-properties.values.list` | GET | `/api/custom-properties/values` | Resolved custom property values for one entity |
| `custom-properties.values.update` | PATCH | `/api/custom-properties/values` | Set custom property values on one entity by key |

---

### `custom-fields.create`

`POST /api/custom-fields`

Create custom field

Body: application/json (free-form — pass with `--data`)

### `custom-fields.delete`

`DELETE /api/custom-fields/{id}`

Delete custom field

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `custom-fields.list`

`GET /api/custom-fields`

List custom fields

### `custom-fields.set`

`PUT /api/custom-fields/{id}`

Update custom field

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `custom-properties.create`

`POST /api/custom-properties`

Create a custom property definition

Admins only. The type-specific config is validated against the scope's existing definitions (so rollup references resolve).

Body (application/json):
  - `scope` (string, required) — one of: `task`, `project`, `client`
  - `name` (string, required)
  - `type` (string, required) — one of: `text`, `number`, `select`, `multi_select`, `date`, `person`, `checkbox`, `url`, `email`, `phone`, `formula`, `rollup`
  - `key` (string)
  - `config` (object)
  - `description` (string)
  - `sortOrder` (number)

### `custom-properties.delete`

`DELETE /api/custom-properties/{id}`

Delete a custom property definition

Admins only.

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `custom-properties.list`

`GET /api/custom-properties`

List custom property definitions

Any workspace member.

Query:
  - `scope` (string) — one of: `task`, `project`, `client`

### `custom-properties.update`

`PATCH /api/custom-properties/{id}`

Update a custom property definition

Admins only. A changed type or config is re-validated against the other definitions in the scope.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `name` (string)
  - `key` (string)
  - `type` (string) — one of: `text`, `number`, `select`, `multi_select`, `date`, `person`, `checkbox`, `url`, `email`, `phone`, `formula`, `rollup`
  - `config` (object)
  - `description` (string)
  - `sortOrder` (number)

### `custom-properties.values.list`

`GET /api/custom-properties/values`

Resolved custom property values for one entity

Any member. Includes literal, formula and rollup values.

Query:
  - `entityType` (string, required) — one of: `task`, `project`, `client`
  - `entityId` (string, required)

### `custom-properties.values.update`

`PATCH /api/custom-properties/values`

Set custom property values on one entity by key

Any member. The task or client must exist in the workspace. Each value that actually changed fires a property-changed automation event.

Body (application/json):
  - `entityType` (string, required) — one of: `task`, `project`, `client`
  - `entityId` (string, required)
  - `values` (object, required) — Property key to value

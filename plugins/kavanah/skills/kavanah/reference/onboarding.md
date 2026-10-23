# Onboarding

7 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `onboarding.config.list` | GET | `/api/onboarding/config` | List config |
| `onboarding.config.set` | PUT | `/api/onboarding/config` | Update config |
| `onboarding.progress.list` | GET | `/api/onboarding/progress` | List progress |
| `onboarding.progress.update` | PATCH | `/api/onboarding/progress` | Update progress |
| `onboarding.sample-data.create` | POST | `/api/onboarding/sample-data` | Install sample data |
| `onboarding.sample-data.delete` | DELETE | `/api/onboarding/sample-data` | Remove sample data |
| `onboarding.sample-data.list` | GET | `/api/onboarding/sample-data` | Get sample-data install status |

---

### `onboarding.config.list`

`GET /api/onboarding/config`

List config

### `onboarding.config.set`

`PUT /api/onboarding/config`

Update config

Body: application/json (free-form — pass with `--data`)

### `onboarding.progress.list`

`GET /api/onboarding/progress`

List progress

### `onboarding.progress.update`

`PATCH /api/onboarding/progress`

Update progress

Body: application/json (free-form — pass with `--data`)

### `onboarding.sample-data.create`

`POST /api/onboarding/sample-data`

Install sample data

Seed the current workspace with a small, clearly-labelled illustrative dataset (one project with a populated board, two clients carrying ARR and renewal dates, one knowledge page). Admin only. Idempotent by workspace — a second call returns 409 rather than seeding twice.

### `onboarding.sample-data.delete`

`DELETE /api/onboarding/sample-data`

Remove sample data

Delete exactly the rows the install recorded, and nothing else. Admin only.

**Destructive** — needs `--yes` against a non-local base URL.

### `onboarding.sample-data.list`

`GET /api/onboarding/sample-data`

Get sample-data install status

Whether the illustrative sample dataset is installed in the current workspace, and how many rows an install writes. Admin only.

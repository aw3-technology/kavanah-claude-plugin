# Knowledge

55 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `knowledge.ask.create` | POST | `/api/knowledge/ask` | Create ask |
| `knowledge.ask.list` | GET | `/api/knowledge/ask` | List ask |
| `knowledge.autolink.create` | POST | `/api/knowledge/autolink` | Create autolink |
| `knowledge.autolink.delete` | DELETE | `/api/knowledge/autolink/{id}` | Delete autolink |
| `knowledge.autolink.list` | GET | `/api/knowledge/autolink` | List autolink |
| `knowledge.autolink.tokenize.create` | POST | `/api/knowledge/autolink/tokenize` | Create tokenize |
| `knowledge.autolink.update` | PATCH | `/api/knowledge/autolink/{id}` | Update autolink |
| `knowledge.decision-candidates.create` | POST | `/api/knowledge/decision-candidates` | Scan documents for decision candidates (paginated; re-call with the returned offset until hasMore is false) |
| `knowledge.decision-candidates.list` | GET | `/api/knowledge/decision-candidates` | List AI-suggested decision candidates |
| `knowledge.decision-candidates.update` | PATCH | `/api/knowledge/decision-candidates/{id}` | Accept or dismiss a decision candidate (terminal — accepting materializes a real decision record) |
| `knowledge.decisions.create` | POST | `/api/knowledge/decisions` | Record a decision |
| `knowledge.decisions.delete` | DELETE | `/api/knowledge/decisions/{id}` | Delete a decision |
| `knowledge.decisions.get` | GET | `/api/knowledge/decisions/{id}` |  |
| `knowledge.decisions.list` | GET | `/api/knowledge/decisions` | List decisions (ADR-style) |
| `knowledge.decisions.update` | PATCH | `/api/knowledge/decisions/{id}` | Update a decision |
| `knowledge.documents.backlinks.list` | GET | `/api/knowledge/documents/{p1}/backlinks` | (undocumented route — params unknown, pass them explicitly) |
| `knowledge.documents.comments.create` | POST | `/api/knowledge/documents/{p1}/comments` | (undocumented route — params unknown, pass them explicitly) |
| `knowledge.documents.comments.delete` | DELETE | `/api/knowledge/documents/{p1}/comments/{p2}` | (undocumented route — params unknown, pass them explicitly) |
| `knowledge.documents.comments.list` | GET | `/api/knowledge/documents/{p1}/comments` | (undocumented route — params unknown, pass them explicitly) |
| `knowledge.documents.comments.update` | PATCH | `/api/knowledge/documents/{p1}/comments/{p2}` | (undocumented route — params unknown, pass them explicitly) |
| `knowledge.documents.create` | POST | `/api/knowledge/documents` | Create a knowledge document |
| `knowledge.documents.delete` | DELETE | `/api/knowledge/documents/{id}` | Delete a knowledge document (moves to trash) |
| `knowledge.documents.from-template.create` | POST | `/api/knowledge/documents/from-template` | (undocumented route — params unknown, pass them explicitly) |
| `knowledge.documents.get` | GET | `/api/knowledge/documents/{id}` | Get a knowledge document |
| `knowledge.documents.list` | GET | `/api/knowledge/documents` | List knowledge documents |
| `knowledge.documents.publish.delete` | DELETE | `/api/knowledge/documents/{p1}/publish` | (undocumented route — params unknown, pass them explicitly) |
| `knowledge.documents.publish.list` | GET | `/api/knowledge/documents/{p1}/publish` | (undocumented route — params unknown, pass them explicitly) |
| `knowledge.documents.publish.set` | PUT | `/api/knowledge/documents/{p1}/publish` | (undocumented route — params unknown, pass them explicitly) |
| `knowledge.documents.search.list` | GET | `/api/knowledge/documents/search` | (undocumented route — params unknown, pass them explicitly) |
| `knowledge.documents.templates.list` | GET | `/api/knowledge/documents/templates` | (undocumented route — params unknown, pass them explicitly) |
| `knowledge.documents.update` | PATCH | `/api/knowledge/documents/{id}` | Update a knowledge document |
| `knowledge.glossary.create` | POST | `/api/knowledge/glossary` | Create a glossary term |
| `knowledge.glossary.delete` | DELETE | `/api/knowledge/glossary/{id}` | Delete a glossary term |
| `knowledge.glossary.get` | GET | `/api/knowledge/glossary/{id}` | Get a glossary term |
| `knowledge.glossary.list` | GET | `/api/knowledge/glossary` | List glossary terms |
| `knowledge.glossary.update` | PATCH | `/api/knowledge/glossary/{id}` | Update a glossary term |
| `knowledge.index-stats.create` | POST | `/api/knowledge/index-stats` | Create index stat |
| `knowledge.index-stats.list` | GET | `/api/knowledge/index-stats` | List index stats |
| `knowledge.onboarding.create` | POST | `/api/knowledge/onboarding` | Create or replace an onboarding doc for a role |
| `knowledge.onboarding.delete` | DELETE | `/api/knowledge/onboarding/{id}` |  |
| `knowledge.onboarding.get` | GET | `/api/knowledge/onboarding/{id}` | Get an onboarding doc |
| `knowledge.onboarding.list` | GET | `/api/knowledge/onboarding` | List onboarding docs |
| `knowledge.onboarding.update` | PATCH | `/api/knowledge/onboarding/{id}` | Update an onboarding doc |
| `knowledge.readme.create` | POST | `/api/knowledge/readme` | Create readme |
| `knowledge.readme.list` | GET | `/api/knowledge/readme` | List readme |
| `knowledge.retros.create` | POST | `/api/knowledge/retros` | Create a sprint retro |
| `knowledge.retros.delete` | DELETE | `/api/knowledge/retros/{id}` |  |
| `knowledge.retros.get` | GET | `/api/knowledge/retros/{id}` | Get a sprint retro |
| `knowledge.retros.list` | GET | `/api/knowledge/retros` | List sprint retros |
| `knowledge.retros.update` | PATCH | `/api/knowledge/retros/{id}` | Update a sprint retro |
| `knowledge.stale.create` | POST | `/api/knowledge/stale` | Create stale |
| `knowledge.stale.list` | GET | `/api/knowledge/stale` | List stale |
| `knowledge.stale.update` | PATCH | `/api/knowledge/stale/{id}` | Update stale |
| `knowledge.threads.condensable.list` | GET | `/api/knowledge/threads/condensable` | List condensable |
| `knowledge.threads.condense.create` | POST | `/api/knowledge/threads/condense` | Create condense |

---

### `knowledge.ask.create`

`POST /api/knowledge/ask`

Create ask

Body: application/json (free-form — pass with `--data`)

### `knowledge.ask.list`

`GET /api/knowledge/ask`

List ask

### `knowledge.autolink.create`

`POST /api/knowledge/autolink`

Create autolink

Body: application/json (free-form — pass with `--data`)

### `knowledge.autolink.delete`

`DELETE /api/knowledge/autolink/{id}`

Delete autolink

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `knowledge.autolink.list`

`GET /api/knowledge/autolink`

List autolink

### `knowledge.autolink.tokenize.create`

`POST /api/knowledge/autolink/tokenize`

Create tokenize

Body: application/json (free-form — pass with `--data`)

### `knowledge.autolink.update`

`PATCH /api/knowledge/autolink/{id}`

Update autolink

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `knowledge.decision-candidates.create`

`POST /api/knowledge/decision-candidates`

Scan documents for decision candidates (paginated; re-call with the returned offset until hasMore is false)

Body (application/json):
  - `offset` (integer) — Pagination offset from a prior call.
  - `limit` (integer) — Documents to scan this call.

### `knowledge.decision-candidates.list`

`GET /api/knowledge/decision-candidates`

List AI-suggested decision candidates

Query:
  - `status` (string) — one of: `pending`, `accepted`, `dismissed`, `all`

### `knowledge.decision-candidates.update`

`PATCH /api/knowledge/decision-candidates/{id}`

Accept or dismiss a decision candidate (terminal — accepting materializes a real decision record)

Path params (positional, in order):
  - `id`

Body (application/json):
  - `action` (string, required) — one of: `accept`, `dismiss`
  - `decision` (object) — Optional reviewer edits applied when accepting.
  - `decision.title` (string)
  - `decision.context` (string)
  - `decision.whatWeChose` (string)
  - `decision.decidedAt` (string)
  - `decision.status` (string)
  - `decision.decidedBy` (string)

### `knowledge.decisions.create`

`POST /api/knowledge/decisions`

Record a decision

Body (application/json):
  - `title` (string, required)
  - `refCode` (string)
  - `status` (string) — one of: `active`, `proposed`, `superseded`
  - `decidedAt` (string)
  - `context` (string)
  - `whatWeChose` (string)
  - `tradeoffs` (string[])

### `knowledge.decisions.delete`

`DELETE /api/knowledge/decisions/{id}`

Delete a decision

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `knowledge.decisions.get`

`GET /api/knowledge/decisions/{id}`

Path params (positional, in order):
  - `id`

### `knowledge.decisions.list`

`GET /api/knowledge/decisions`

List decisions (ADR-style)

### `knowledge.decisions.update`

`PATCH /api/knowledge/decisions/{id}`

Update a decision

Path params (positional, in order):
  - `id`

### `knowledge.documents.backlinks.list`

`GET /api/knowledge/documents/{p1}/backlinks`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `knowledge.documents.comments.create`

`POST /api/knowledge/documents/{p1}/comments`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `knowledge.documents.comments.delete`

`DELETE /api/knowledge/documents/{p1}/comments/{p2}`

(undocumented route — params unknown, pass them explicitly)

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `p1`
  - `p2`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `knowledge.documents.comments.list`

`GET /api/knowledge/documents/{p1}/comments`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `knowledge.documents.comments.update`

`PATCH /api/knowledge/documents/{p1}/comments/{p2}`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`
  - `p2`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `knowledge.documents.create`

`POST /api/knowledge/documents`

Create a knowledge document

Body (application/json):
  - `title` (string, required)
  - `body` (string)
  - `tags` (string[])

### `knowledge.documents.delete`

`DELETE /api/knowledge/documents/{id}`

Delete a knowledge document (moves to trash)

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `knowledge.documents.from-template.create`

`POST /api/knowledge/documents/from-template`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `knowledge.documents.get`

`GET /api/knowledge/documents/{id}`

Get a knowledge document

Path params (positional, in order):
  - `id`

### `knowledge.documents.list`

`GET /api/knowledge/documents`

List knowledge documents

Query:
  - `limit` (integer)
  - `offset` (integer)

### `knowledge.documents.publish.delete`

`DELETE /api/knowledge/documents/{p1}/publish`

(undocumented route — params unknown, pass them explicitly)

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `knowledge.documents.publish.list`

`GET /api/knowledge/documents/{p1}/publish`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `knowledge.documents.publish.set`

`PUT /api/knowledge/documents/{p1}/publish`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `knowledge.documents.search.list`

`GET /api/knowledge/documents/search`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `knowledge.documents.templates.list`

`GET /api/knowledge/documents/templates`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `knowledge.documents.update`

`PATCH /api/knowledge/documents/{id}`

Update a knowledge document

Path params (positional, in order):
  - `id`

Body (application/json):
  - `title` (string)
  - `body` (string)
  - `tags` (string[])

### `knowledge.glossary.create`

`POST /api/knowledge/glossary`

Create a glossary term

Body (application/json):
  - `term` (string, required)
  - `domain` (string) — one of: `product`, `tech`, `process`, `people`
  - `definition` (string)
  - `aliases` (string[])

### `knowledge.glossary.delete`

`DELETE /api/knowledge/glossary/{id}`

Delete a glossary term

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `knowledge.glossary.get`

`GET /api/knowledge/glossary/{id}`

Get a glossary term

Path params (positional, in order):
  - `id`

### `knowledge.glossary.list`

`GET /api/knowledge/glossary`

List glossary terms

### `knowledge.glossary.update`

`PATCH /api/knowledge/glossary/{id}`

Update a glossary term

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `knowledge.index-stats.create`

`POST /api/knowledge/index-stats`

Create index stat

Body: application/json (free-form — pass with `--data`)

### `knowledge.index-stats.list`

`GET /api/knowledge/index-stats`

List index stats

### `knowledge.onboarding.create`

`POST /api/knowledge/onboarding`

Create or replace an onboarding doc for a role

Body (application/json):
  - `role` (string, required)
  - `persona` (string)
  - `earlyWins` (string[])
  - `thingsThatMatter` (string[])

### `knowledge.onboarding.delete`

`DELETE /api/knowledge/onboarding/{id}`

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `knowledge.onboarding.get`

`GET /api/knowledge/onboarding/{id}`

Get an onboarding doc

Path params (positional, in order):
  - `id`

### `knowledge.onboarding.list`

`GET /api/knowledge/onboarding`

List onboarding docs

### `knowledge.onboarding.update`

`PATCH /api/knowledge/onboarding/{id}`

Update an onboarding doc

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `knowledge.readme.create`

`POST /api/knowledge/readme`

Create readme

Body: application/json (free-form — pass with `--data`)

### `knowledge.readme.list`

`GET /api/knowledge/readme`

List readme

### `knowledge.retros.create`

`POST /api/knowledge/retros`

Create a sprint retro

Body (application/json):
  - `sprintLabel` (string, required)
  - `status` (string) — one of: `draft`, `ready`, `shared`
  - `windowStart` (string)
  - `windowEnd` (string)
  - `wins` (object[])
  - `misses` (object[])
  - `surprises` (object[])

### `knowledge.retros.delete`

`DELETE /api/knowledge/retros/{id}`

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `knowledge.retros.get`

`GET /api/knowledge/retros/{id}`

Get a sprint retro

Path params (positional, in order):
  - `id`

### `knowledge.retros.list`

`GET /api/knowledge/retros`

List sprint retros

### `knowledge.retros.update`

`PATCH /api/knowledge/retros/{id}`

Update a sprint retro

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `knowledge.stale.create`

`POST /api/knowledge/stale`

Create stale

Body: application/json (free-form — pass with `--data`)

### `knowledge.stale.list`

`GET /api/knowledge/stale`

List stale

### `knowledge.stale.update`

`PATCH /api/knowledge/stale/{id}`

Update stale

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `knowledge.threads.condensable.list`

`GET /api/knowledge/threads/condensable`

List condensable

### `knowledge.threads.condense.create`

`POST /api/knowledge/threads/condense`

Create condense

Body: application/json (free-form — pass with `--data`)

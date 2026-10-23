# Personal

17 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `learn.courses.lessons.get` | GET | `/api/learn/courses/{course}/lessons/{lesson}` | One Learn lesson, with its narration version |
| `learn.courses.list` | GET | `/api/learn/courses` | The Learn course catalogue |
| `learn.progress.list` | GET | `/api/learn/progress` | The caller's Learn progress — completions, listening, reading |
| `learn.progress.set` | PUT | `/api/learn/progress` | Mark a Learn lesson complete or not complete |
| `learn.progress.update` | PATCH | `/api/learn/progress` | Save a Learn listening or reading checkpoint |
| `me.notes.list` | GET | `/api/me/notes` | Get the caller's scratch note |
| `me.notes.set` | PUT | `/api/me/notes` | Upsert the caller's scratch note |
| `me.reminders.create` | POST | `/api/me/reminders` | Create a reminder |
| `me.reminders.delete` | DELETE | `/api/me/reminders/{id}` | Delete a reminder |
| `me.reminders.list` | GET | `/api/me/reminders` | List the caller's reminders |
| `me.reminders.update` | PATCH | `/api/me/reminders/{id}` | Update a reminder |
| `me.todos.create` | POST | `/api/me/todos` | Create a to-do |
| `me.todos.delete` | DELETE | `/api/me/todos/{id}` | Delete a to-do |
| `me.todos.list` | GET | `/api/me/todos` | List the caller's to-dos |
| `me.todos.update` | PATCH | `/api/me/todos/{id}` | Update a to-do |
| `profile.experience.list` | GET | `/api/profile/experience` | Get your own experience profile and declared skills |
| `profile.experience.set` | PUT | `/api/profile/experience` | Update your own experience profile (and optionally declared skills) |

---

### `learn.courses.lessons.get`

`GET /api/learn/courses/{course}/lessons/{lesson}`

One Learn lesson, with its narration version

The lesson's full content. `narration.version` is the `v` parameter `/api/tts?kind=course&slug={lesson}` needs to serve cached audio; null when the lesson is unpublished.

Path params (positional, in order):
  - `course`
  - `lesson`

### `learn.courses.list`

`GET /api/learn/courses`

The Learn course catalogue

Every course in the catalogue with its modules and lesson outlines, minus lesson bodies. `published` is false for a lesson that has no body yet ("coming soon"). Same catalogue the web reader renders. Build-static, so it carries `Cache-Control: private, max-age=0, stale-while-revalidate=60`.

### `learn.progress.list`

`GET /api/learn/progress`

The caller's Learn progress — completions, listening, reading

Per-person, not per-workspace — the same document is returned in every workspace the caller belongs to. `completed` keeps its original shape (course slug → completed lesson slugs, oldest first) for older clients. `items` holds per-item state keyed by course slug then item slug, where an item is a lesson OR the course introduction narration (its `narrationIntroSlug`). `courses` are rollups over PUBLISHED lessons only; `continue` is the most recently touched unfinished lesson (or the next lesson of a started course), or null. `Cache-Control: private, no-store` — the same client writes this and re-reads it straight after.

### `learn.progress.set`

`PUT /api/learn/progress`

Mark a Learn lesson complete or not complete

Body (application/json):
  - `course` (string, required) — Course slug
  - `lesson` (string, required) — Lesson slug within that course
  - `completed` (boolean, required)

### `learn.progress.update`

`PATCH /api/learn/progress`

Save a Learn listening or reading checkpoint

Records where the caller is in a lesson's (or course introduction's) narration, how far they have listened, and/or the furthest body section they have read. Merge rules: the position is last-write-wins by `clientUpdatedAt` (clamped to server time), so a late, queued save from another device cannot rewind a newer position; the listened share and `readSection` only ever grow. `furthestSeconds` is an offset into one `narrationVersion` — a newer write in a new version replaces it. The first checkpoint that takes a LESSON's listened share to 95% or more marks it complete (`autoCompleted: true` in the answer) — once; a lesson the caller later un-completes is never re-completed automatically.

Body (application/json):
  - `course` (string, required) — Course slug
  - `lesson` (string, required) — Lesson slug, or the course's narrationIntroSlug
  - `narrationVersion` (string) — The narration content version the offsets refer to
  - `positionSeconds` (number)
  - `furthestSeconds` (number) — Furthest point reached by contiguous playback
  - `durationSeconds` (number)
  - `readSection` (integer) — Furthest body section reached (1…n); n+1 = the end of the lesson
  - `readSectionsTotal` (integer)
  - `clientUpdatedAt` (string<date-time>) — When the client captured this checkpoint

### `me.notes.list`

`GET /api/me/notes`

Get the caller's scratch note

### `me.notes.set`

`PUT /api/me/notes`

Upsert the caller's scratch note

Body (application/json):
  - `body` (string, required) — Note body (capped, 413 if too large).

### `me.reminders.create`

`POST /api/me/reminders`

Create a reminder

Body (application/json):
  - `text` (string, required)
  - `remindAt` (string<date-time>, required)
  - `taskId` (integer) — Optional task in the same workspace.

### `me.reminders.delete`

`DELETE /api/me/reminders/{id}`

Delete a reminder

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `me.reminders.list`

`GET /api/me/reminders`

List the caller's reminders

### `me.reminders.update`

`PATCH /api/me/reminders/{id}`

Update a reminder

Path params (positional, in order):
  - `id`

Body (application/json):
  - `text` (string)
  - `remindAt` (string<date-time>)
  - `done` (boolean)
  - `taskId` (integer)

### `me.todos.create`

`POST /api/me/todos`

Create a to-do

Body (application/json):
  - `text` (string, required)

### `me.todos.delete`

`DELETE /api/me/todos/{id}`

Delete a to-do

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `me.todos.list`

`GET /api/me/todos`

List the caller's to-dos

### `me.todos.update`

`PATCH /api/me/todos/{id}`

Update a to-do

Path params (positional, in order):
  - `id`

Body (application/json):
  - `text` (string)
  - `done` (boolean)
  - `sortOrder` (integer)

### `profile.experience.list`

`GET /api/profile/experience`

Get your own experience profile and declared skills

Self-service sibling of `/api/people/profile` — no people-management permission required. The member name is resolved SERVER-SIDE from the session, never from the request, so a caller can only reach their own row.

### `profile.experience.set`

`PUT /api/profile/experience`

Update your own experience profile (and optionally declared skills)

Body (application/json):
  - `linkedinUrl` (string)
  - `experienceSummary` (string)
  - `resumeText` (string)
  - `resumeFileName` (string)
  - `skills` (object[]) — Replaces your declared skill set (same shape as /api/people/skills).
  - `deriveSkills` (boolean)

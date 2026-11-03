# Learn

4 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `learn.assignments.create` | POST | `/api/learn/assignments` | Assign a course to members (owners and admins) |
| `learn.assignments.delete` | DELETE | `/api/learn/assignments/{id}` | Withdraw an assignment (owners and admins) |
| `learn.assignments.list` | GET | `/api/learn/assignments` | Team course assignments and progress (owners and admins) |
| `learn.assignments.update` | PATCH | `/api/learn/assignments/{id}` | Change an assignment's due date or note (owners and admins) |

---

### `learn.assignments.create`

`POST /api/learn/assignments`

Assign a course to members (owners and admins)

Assigns one course to up to 200 active members of this workspace. Re-assigning someone who already has the course changes only the due date or note this request supplies (null keeps theirs; clear a due date with PATCH) and does not notify them again; newly assigned people get an email (category course-assigned, tasks channel) and a push. `dueAt` is a calendar day: send YYYY-MM-DD (an ISO date-time with an explicit offset is also accepted and its written day is used). It is stored as that day's 23:59:59.999Z and is overdue once the day has ended at UTC-12.

Body (application/json):
  - `course` (string, required) — Course slug
  - `userIds` (string<uuid>[], required)
  - `dueAt` (string|null) — Calendar day, YYYY-MM-DD
  - `note` (string|null)

### `learn.assignments.delete`

`DELETE /api/learn/assignments/{id}`

Withdraw an assignment (owners and admins)

The learner's progress is kept; only the team view of that course goes away.

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `learn.assignments.list`

`GET /api/learn/assignments`

Team course assignments and progress (owners and admins)

Every course assigned in this workspace to an active member, with that member's standing in it. Progress is returned ONLY for assigned (person, course) pairs — a course someone takes on their own is never visible here. 403 for anyone who is not a workspace owner or admin.

### `learn.assignments.update`

`PATCH /api/learn/assignments/{id}`

Change an assignment's due date or note (owners and admins)

Path params (positional, in order):
  - `id`

Body (application/json):
  - `dueAt` (string|null) — Calendar day, YYYY-MM-DD; null clears it
  - `note` (string|null)

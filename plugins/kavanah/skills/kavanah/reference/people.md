# People

8 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `people.list` | GET | `/api/people` | Get teams, members, and projects |
| `people.profile.list` | GET | `/api/people/profile` | List member experience profiles, or fetch one in full |
| `people.profile.set` | PUT | `/api/people/profile` | Partial-update a member's experience profile |
| `people.skills.list` | GET | `/api/people/skills` | List declared/learned skill profiles for workspace members |
| `people.skills.set` | PUT | `/api/people/skills` | Replace a member's declared skill set |
| `people.team-context.list` | GET | `/api/people/team-context` | Get the workspace team context brief used for AI assignment |
| `people.team-context.set` | PUT | `/api/people/team-context` | Replace the workspace team context brief (admin) |
| `people.update` | PATCH | `/api/people` | Update teams and members |

---

### `people.list`

`GET /api/people`

Get teams, members, and projects

Each member carries a derived `invite` object, read from workspace memberships and invites rather than the stored roster: `status` is one of `joined`, `pending`, `awaiting_approval`, `expired`, `declined`, `removed`, `deactivated` or `not_invited`, with `inviteId`, `invitedAt` and `expiresAt` when an invite exists. It is never stored; echoing it back on PATCH is ignored.

### `people.profile.list`

`GET /api/people/profile`

List member experience profiles, or fetch one in full

Without `member`, returns every member's profile with `resumeText` elided. With `member`, returns that member's full profile including the resume text. Profiles are keyed by member display name (matching `app_tasks.assigned_to`), not user id, so roster-only members are covered.

Query:
  - `member` (string) — Return one member's full profile by display name.

### `people.profile.set`

`PUT /api/people/profile`

Partial-update a member's experience profile

Omitted fields keep their stored value; an empty string clears a field. When the resume or experience text changes and `deriveSkills` is not false, the profile text is mapped onto the canonical categorized skill vocabulary and merged additively into the member's declared skills (an LLM pass never wipes hand-declared skills).

Body (application/json):
  - `memberName` (string, required)
  - `linkedinUrl` (string) — Must be a valid http(s) URL.
  - `experienceSummary` (string) — Free-text background blurb.
  - `resumeText` (string) — Resume as TEXT (extracted client-side from PDF/txt/md), not a file.
  - `resumeFileName` (string)
  - `deriveSkills` (boolean) — Derive declared skills from the profile text after saving.

### `people.skills.list`

`GET /api/people/skills`

List declared/learned skill profiles for workspace members

Query:
  - `member` (string) — Filter to a single member by display name.

### `people.skills.set`

`PUT /api/people/skills`

Replace a member's declared skill set

Body (application/json):
  - `memberName` (string, required)
  - `skills` (object[], required)

### `people.team-context.list`

`GET /api/people/team-context`

Get the workspace team context brief used for AI assignment

A standing free-text block (who is strong at what, hiring gaps, assignment conventions) injected into the AI agent's system prompt. Any member may read it.

### `people.team-context.set`

`PUT /api/people/team-context`

Replace the workspace team context brief (admin)

Body (application/json):
  - `context` (string, required)

### `people.update`

`PATCH /api/people`

Update teams and members

Replaces the workspace's teams and members with the submitted lists. A project missing from `projects` is KEPT (this route never removes a project). `workspaceId` names the workspace the roster was loaded from and `version` the row version it was built on (GET returns both): 409 `bundle_workspace_mismatch` when the workspace differs, 409 with the fresh `bundle` when the row has moved on, 400 `bundle_workspace_required` / `bundle_version_required` when a browser session omits either. API-key callers may omit them; when they echo, they are checked. Only addresses this save ADDS to the roster are invited; removing or editing members never re-invites anyone. Removing a member here does not remove a joined member's workspace access (use DELETE /api/workspace/members/{userId}).

Body (application/json):
  - `workspaceId` (string) — The workspace the roster was loaded from. Required for browser sessions.
  - `version` (string) — The `version` the roster was built on. Required for browser sessions.
  - `teams` (object[])
  - `members` (object[])
  - `projects` (object[])

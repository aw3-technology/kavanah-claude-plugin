# Profile

12 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `profile.emails.create` | POST | `/api/profile/emails` | Add a secondary email and send a verification message |
| `profile.emails.delete` | DELETE | `/api/profile/emails/{id}` | Remove a secondary email |
| `profile.emails.list` | GET | `/api/profile/emails` | List the caller's secondary emails |
| `profile.emails.promote.create` | POST | `/api/profile/emails/{id}/promote` | Make a verified secondary email the primary login email |
| `profile.emails.resend.create` | POST | `/api/profile/emails/{id}/resend` | Resend a secondary email's verification message |
| `profile.handle.list` | GET | `/api/profile/handle` | Get the caller's public handle |
| `profile.handle.set` | PUT | `/api/profile/handle` | Set or clear the caller's public handle |
| `profile.list` | GET | `/api/profile` | Get current user profile |
| `profile.timezone.create` | POST | `/api/profile/timezone` | Record the caller's device timezone |
| `profile.update` | PATCH | `/api/profile` | Update user profile |
| `user.font-size.list` | GET | `/api/user/font-size` | The caller's font-size preference |
| `user.font-size.set` | PUT | `/api/user/font-size` | Set the caller's font-size preference |

---

### `profile.emails.create`

`POST /api/profile/emails`

Add a secondary email and send a verification message

Up to 10 secondary emails. Rate limited to 10 per hour. The verification email is best-effort; a send failure does not fail the add.

Body (application/json):
  - `email` (string, required)

### `profile.emails.delete`

`DELETE /api/profile/emails/{id}`

Remove a secondary email

Rate limited to 30 per hour.

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `profile.emails.list`

`GET /api/profile/emails`

List the caller's secondary emails

### `profile.emails.promote.create`

`POST /api/profile/emails/{id}/promote`

Make a verified secondary email the primary login email

The previous primary becomes a secondary email. Rate limited to 20 per hour.

Path params (positional, in order):
  - `id`

### `profile.emails.resend.create`

`POST /api/profile/emails/{id}/resend`

Resend a secondary email's verification message

Rate limited to 10 per hour. No-op when already verified; send failures are not reported.

Path params (positional, in order):
  - `id`

### `profile.handle.list`

`GET /api/profile/handle`

Get the caller's public handle

### `profile.handle.set`

`PUT /api/profile/handle`

Set or clear the caller's public handle

The handle others use to send message requests. 3 to 30 lowercase letters, digits or underscores; reserved handles are refused. null clears it.

Body (application/json):
  - `handle` (string|null)

### `profile.list`

`GET /api/profile`

Get current user profile

### `profile.timezone.create`

`POST /api/profile/timezone`

Record the caller's device timezone

Stores the IANA zone on the profile only when it changed; server-side schedulers use it.

Body (application/json):
  - `timezone` (string, required) — IANA zone name

### `profile.update`

`PATCH /api/profile`

Update user profile

Overlays only the fields the request carries. The sign-in email is never changed here: sending `email` with a different address is 400. To change it, add the address with POST /api/profile/emails, confirm it, then POST /api/profile/emails/{id}/promote. Addresses are unique case-insensitively.

Body (application/json):
  - `firstName` (string)
  - `lastName` (string)
  - `fullName` (string)
  - `email` (string<email>)
  - `phone` (string)
  - `jobTitle` (string)
  - `department` (string)
  - `bio` (string)
  - `avatarTone` (string)

### `user.font-size.list`

`GET /api/user/font-size`

The caller's font-size preference

### `user.font-size.set`

`PUT /api/user/font-size`

Set the caller's font-size preference

Body (application/json):
  - `fontSize` (string, required) — one of: `small`, `medium`, `large`

# Sharing

5 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `p.share.get` | GET | `/api/p/share/{token}` | Resolve a public share token (no auth) |
| `shares.create` | POST | `/api/shares` | Mint a public read-only share link (admin) |
| `shares.delete` | DELETE | `/api/shares` | Revoke a public share link (admin) |
| `shares.list` | GET | `/api/shares` | List public share links (admin) |
| `shares.update` | PATCH | `/api/shares` | Revoke a public share link (admin) |

---

### `p.share.get`

`GET /api/p/share/{token}`

Resolve a public share token (no auth)

Public, unauthenticated, read-only projection of a shared project/view. A single 404 covers every failure (missing/revoked/expired token, deleted resource). Rate-limited and marked noindex.

Path params (positional, in order):
  - `token`

### `shares.create`

`POST /api/shares`

Mint a public read-only share link (admin)

Body (application/json):
  - `resourceType` (string, required) — one of: `project`, `view`
  - `resourceId` (string, required)
  - `expiresAt` (string<date-time>)

### `shares.delete`

`DELETE /api/shares`

Revoke a public share link (admin)

**Destructive** — needs `--yes` against a non-local base URL.

Query:
  - `id` (string)

### `shares.list`

`GET /api/shares`

List public share links (admin)

Query:
  - `resourceType` (string) — one of: `project`, `view`
  - `resourceId` (string)

### `shares.update`

`PATCH /api/shares`

Revoke a public share link (admin)

Alias of DELETE. Accepts `?id=` or a JSON body `{ id }`.

Body (application/json):
  - `id` (string)

# Outreach

2 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `outreach.unsubscribe.create` | POST | `/api/outreach/unsubscribe` | Unsubscribe an address from a workspace's outreach (RFC 8058 one-click) |
| `outreach.unsubscribe.list` | GET | `/api/outreach/unsubscribe` | The unsubscribe confirmation page for cadence mail |

---

### `outreach.unsubscribe.create`

`POST /api/outreach/unsubscribe`

Unsubscribe an address from a workspace's outreach (RFC 8058 one-click)

Called by the recipient's mail provider (`List-Unsubscribe-Post: List-Unsubscribe=One-Click`) or by the confirmation page's button. Adds the address to THIS workspace's suppression list (never the global one) and stops every active cadence enrollment for it, pulling back the steps already queued. Idempotent.

**Destructive** — needs `--yes` against a non-local base URL.

Query:
  - `t` (string, required) — Signed unsubscribe token from the email.

### `outreach.unsubscribe.list`

`GET /api/outreach/unsubscribe`

The unsubscribe confirmation page for cadence mail

PUBLIC and CSRF-exempt: the signed `t` token names one (workspace, address) and is the only credential. A GET NEVER unsubscribes — link scanners and mail gateways prefetch every URL in an inbound message — it renders a confirmation page whose button POSTs here (RFC 8058).

Query:
  - `t` (string, required) — Signed unsubscribe token from the email.

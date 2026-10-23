# Billing

2 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `credits.summary.list` | GET | `/api/credits/summary` | List summary |
| `settings.billing.team.create` | POST | `/api/settings/billing/team` | Move some of your own credits into the workspace pool |

---

### `credits.summary.list`

`GET /api/credits/summary`

List summary

### `settings.billing.team.create`

`POST /api/settings/billing/team`

Move some of your own credits into the workspace pool

Any workspace member moves credits from their OWN balance into the workspace's shared pool; only the caller's wallet is ever debited. Funding the pool is the team-billing opt-in, so this also switches team billing on (members then spend from the pool first). There is no transfer back. `transfer_id` is the idempotency key: a retry with the same id replays instead of moving the credits twice. If the pool cannot be credited after the debit, the debit is reversed.

Body (application/json):
  - `amount` (integer, required) — Whole credits to move
  - `transfer_id` (string<uuid>, required) — Idempotency key

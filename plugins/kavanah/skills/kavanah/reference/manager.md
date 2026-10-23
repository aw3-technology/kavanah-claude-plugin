# Manager

10 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `manager.checkins.create` | POST | `/api/manager/checkins` | Answer a check-in |
| `manager.checkins.list` | GET | `/api/manager/checkins` | The caller's own check-in history |
| `manager.commitments.create` | POST | `/api/manager/commitments` | Commit to a piece of work by a deadline |
| `manager.commitments.list` | GET | `/api/manager/commitments` | List the caller's own commitments |
| `manager.commitments.update` | PATCH | `/api/manager/commitments/{id}` | Renegotiate, complete, or cancel one of the caller's commitments |
| `manager.list` | GET | `/api/manager` | The caller's Manager Mode state (agreement, scorecard, commitments, check-ins) |
| `manager.plan.list` | GET | `/api/manager/plan` | Preview an achievable deadline without committing to it |
| `manager.rewards.create` | POST | `/api/manager/rewards` | Redeem earned points for real account credits |
| `manager.rewards.list` | GET | `/api/manager/rewards` | Points ledger, payout history, and what the caller could redeem now |
| `manager.update` | PATCH | `/api/manager` | Update the caller's Manager Mode agreement |

---

### `manager.checkins.create`

`POST /api/manager/checkins`

Answer a check-in

Write-once — a check-in that already has an answer is not overwritten. Check-ins are created by the `manager-checkins` cron, never by this API: answering one earns points, so a user-creatable check-in would be a points faucet.

Body (application/json):
  - `id` (string<uuid>, required)
  - `response` (string, required)

### `manager.checkins.list`

`GET /api/manager/checkins`

The caller's own check-in history

Query:
  - `unanswered` (string) — one of: `true`, `false`
  - `limit` (integer)

### `manager.commitments.create`

`POST /api/manager/commitments`

Commit to a piece of work by a deadline

The deadline is computed from the caller's calibration and queue unless `dueAt` is supplied. It is frozen for scoring at creation — renegotiating later moves the working date but never the date the commitment is graded against. Does not create tasks; task creation from a commitment goes through the KVN-gated `commit_to_work` agent tool.

Body (application/json):
  - `title` (string, required)
  - `estimateHours` (number)
  - `notes` (string)
  - `dueAt` (string<date-time>)
  - `taskId` (integer) — Must belong to the caller's workspace; verified before use.

### `manager.commitments.list`

`GET /api/manager/commitments`

List the caller's own commitments

Query:
  - `status` (string) — one of: `open`, `met`, `missed`, `cancelled`, `all`
  - `limit` (integer)

### `manager.commitments.update`

`PATCH /api/manager/commitments/{id}`

Renegotiate, complete, or cancel one of the caller's commitments

Path params (positional, in order):
  - `id`

Body (application/json):
  - `action` (string, required) — one of: `renegotiate`, `complete`, `cancel`
  - `dueAt` (string<date-time>) — Required for `renegotiate`.

### `manager.list`

`GET /api/manager`

The caller's Manager Mode state (agreement, scorecard, commitments, check-ins)

Never 404s. A user who has never enabled Manager Mode gets a disabled default agreement, so callers need no null branch.

### `manager.plan.list`

`GET /api/manager/plan`

Preview an achievable deadline without committing to it

Runs the same computation `POST /api/manager/commitments` uses: the estimate is uplifted by the caller's own estimate-vs-actual percentile, queued behind work they have already promised, and spread across their real working days and focused hours.

Query:
  - `estimateHours` (number)

### `manager.rewards.create`

`POST /api/manager/rewards`

Redeem earned points for real account credits

The only Manager Mode endpoint that moves money. Requires both `rewardsEnabled` and a non-zero `monthlyCreditCap` on the caller's agreement; the payout is clamped by the monthly cap, then the point balance, then the amount requested. Points are debited in the same transaction as the payout row and refunded if the credit grant fails.

Body (application/json):
  - `credits` (integer) — Omit to redeem as many as the caps and balance allow.

### `manager.rewards.list`

`GET /api/manager/rewards`

Points ledger, payout history, and what the caller could redeem now

### `manager.update`

`PATCH /api/manager`

Update the caller's Manager Mode agreement

PARTIAL — only fields present in the body are written. `enabled` is the opt-in for the whole feature. `rewardsEnabled` and a non-zero `monthlyCreditCap` are BOTH required before any credit payout is possible; setting `rewardsEnabled` to false also resets the cap to 0.

Body (application/json):
  - `enabled` (boolean)
  - `style` (string) — one of: `supportive`, `balanced`, `demanding`
  - `objectives` (string)
  - `workDays` (integer[]) — 0=Sunday … 6=Saturday
  - `hoursPerDay` (number) — Focused hours on a work day
  - `dayEndHour` (integer)
  - `confidence` (string) — one of: `p50`, `p90`
  - `maxOpenCommitments` (integer)
  - `checkinFrequency` (string) — one of: `off`, `daily`, `weekdays`, `weekly`
  - `checkinHour` (integer)
  - `checkinDayOfWeek` (integer)
  - `timezone` (string) — IANA zone
  - `rewardsEnabled` (boolean)
  - `pointsPerCredit` (integer)
  - `monthlyCreditCap` (integer)

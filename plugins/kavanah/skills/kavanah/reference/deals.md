# Deals

73 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `deals.audience.create` | POST | `/api/deals/audience` | Suppress an address, or reconcile the audience with AngelSend |
| `deals.audience.list` | GET | `/api/deals/audience` | This workspace's outbound opt-out list |
| `deals.audience.schedule.list` | GET | `/api/deals/audience/schedule` | The scheduled AngelSend audience sync |
| `deals.audience.schedule.set` | PUT | `/api/deals/audience/schedule` | Turn the scheduled AngelSend directions on or off |
| `deals.cadences.angelsend.create` | POST | `/api/deals/cadences/{id}/angelsend` | Sync a cadence's AngelSend campaign now |
| `deals.cadences.angelsend.list` | GET | `/api/deals/cadences/{id}/angelsend` | The native AngelSend campaign(s) behind a cadence |
| `deals.cadences.angelsend.set` | PUT | `/api/deals/cadences/{id}/angelsend` | Back a cadence with a native AngelSend campaign, or stop |
| `deals.cadences.create` | POST | `/api/deals/cadences` | (undocumented route — params unknown, pass them explicitly) |
| `deals.cadences.delete` | DELETE | `/api/deals/cadences/{p1}` | (undocumented route — params unknown, pass them explicitly) |
| `deals.cadences.enroll-bulk.create` | POST | `/api/deals/cadences/{id}/enroll-bulk` | Enroll up to 200 contacts in one cadence |
| `deals.cadences.enroll.create` | POST | `/api/deals/cadences/{p1}/enroll` | (undocumented route — params unknown, pass them explicitly) |
| `deals.cadences.experiment.list` | GET | `/api/deals/cadences/{id}/experiment` | A cadence's subject/sender experiment and winner policy |
| `deals.cadences.experiment.update` | PATCH | `/api/deals/cadences/{id}/experiment` | Configure a cadence's experiment design and automatic winner policy |
| `deals.cadences.list` | GET | `/api/deals/cadences` | (undocumented route — params unknown, pass them explicitly) |
| `deals.cadences.update` | PATCH | `/api/deals/cadences/{p1}` | (undocumented route — params unknown, pass them explicitly) |
| `deals.contact-runway.list` | GET | `/api/deals/contact-runway` | How long each live network cadence can keep reaching new people |
| `deals.contact-runway.update` | PATCH | `/api/deals/contact-runway` | Set the contact-runway warning threshold (admin) |
| `deals.conversations.list` | GET | `/api/deals/conversations` | The Rain Room conversation map |
| `deals.create` | POST | `/api/deals` | (undocumented route — params unknown, pass them explicitly) |
| `deals.data-room-analysis.create` | POST | `/api/deals/{id}/data-room-analysis` | Read the deal's data room now |
| `deals.data-room-analysis.list` | GET | `/api/deals/{id}/data-room-analysis` | The deal's stored data-room reading |
| `deals.follow-ups.list` | GET | `/api/deals/follow-ups` | (undocumented route — params unknown, pass them explicitly) |
| `deals.forecast.list` | GET | `/api/deals/forecast` | The Deal Room revenue forecast, calculated live |
| `deals.forecast.preview-email.create` | POST | `/api/deals/forecast/preview-email` | Email the weekly forecast to yourself for review |
| `deals.forecast.recalculate.create` | POST | `/api/deals/forecast/recalculate` | Recalculate the forecast onto every open deal now (admin) |
| `deals.forecast.settings.list` | GET | `/api/deals/forecast/settings` | Forecast settings and the weekly forecast email schedule |
| `deals.forecast.settings.set` | PUT | `/api/deals/forecast/settings` | Configure the forecast (admin) |
| `deals.get` | GET | `/api/deals/{p1}` | (undocumented route — params unknown, pass them explicitly) |
| `deals.import.create` | POST | `/api/deals/import` | (undocumented route — params unknown, pass them explicitly) |
| `deals.import.preview.create` | POST | `/api/deals/import/preview` | (undocumented route — params unknown, pass them explicitly) |
| `deals.issuer-campaigns.create` | POST | `/api/deals/issuer-campaigns` | Create an issuer campaign |
| `deals.issuer-campaigns.get` | GET | `/api/deals/issuer-campaigns/{id}` | One issuer campaign |
| `deals.issuer-campaigns.list` | GET | `/api/deals/issuer-campaigns` | List issuer campaigns (client prospecting) |
| `deals.issuer-campaigns.matches.convert.create` | POST | `/api/deals/issuer-campaigns/{id}/matches/{firmId}/convert` | Convert a prospect into a deal |
| `deals.issuer-campaigns.matches.list` | GET | `/api/deals/issuer-campaigns/{id}/matches` | The campaign's ranked prospects |
| `deals.issuer-campaigns.pause.create` | POST | `/api/deals/issuer-campaigns/{id}/pause` | Pause an issuer campaign |
| `deals.issuer-campaigns.rank.create` | POST | `/api/deals/issuer-campaigns/{id}/rank` | Rank issuers against the campaign's mandate |
| `deals.issuer-campaigns.start.create` | POST | `/api/deals/issuer-campaigns/{id}/start` | Start, top up or resume an issuer campaign |
| `deals.issuer-campaigns.update` | PATCH | `/api/deals/issuer-campaigns/{id}` | Edit an issuer campaign's definition |
| `deals.list` | GET | `/api/deals` | (undocumented route — params unknown, pass them explicitly) |
| `deals.sheet-link.list` | GET | `/api/deals/sheet-link` | (undocumented route — params unknown, pass them explicitly) |
| `deals.sheet-link.sync.create` | POST | `/api/deals/sheet-link/sync` | (undocumented route — params unknown, pass them explicitly) |
| `deals.sheet-link.update` | PATCH | `/api/deals/sheet-link` | (undocumented route — params unknown, pass them explicitly) |
| `deals.staffing-settings.list` | GET | `/api/deals/staffing-settings` | Deal-team staffing settings |
| `deals.staffing-settings.set` | PUT | `/api/deals/staffing-settings` | Update deal-team staffing settings (admin) |
| `deals.stages.create` | POST | `/api/deals/stages` | (undocumented route — params unknown, pass them explicitly) |
| `deals.stages.delete` | DELETE | `/api/deals/stages/{p1}` | (undocumented route — params unknown, pass them explicitly) |
| `deals.stages.update` | PATCH | `/api/deals/stages/{p1}` | (undocumented route — params unknown, pass them explicitly) |
| `deals.team.list` | GET | `/api/deals/{id}/team` | The deal team (our side) |
| `deals.team.set` | PUT | `/api/deals/{id}/team` | Replace the deal team |
| `deals.team.staff.create` | POST | `/api/deals/{id}/team/staff` | Confirm a staffing proposal |
| `deals.team.suggest.list` | GET | `/api/deals/{id}/team/suggest` | Propose a deal team (read-only) |
| `deals.update` | PATCH | `/api/deals/{p1}` | (undocumented route — params unknown, pass them explicitly) |
| `firms.create` | POST | `/api/firms` | Create or update a firm |
| `firms.delete` | DELETE | `/api/firms/{id}` | Archive a firm |
| `firms.get` | GET | `/api/firms/{id}` | One firm, plus every relationship held there |
| `firms.list` | GET | `/api/firms` | List institutions (the investor / issuer matrix) |
| `firms.merge.create` | POST | `/api/firms/merge` | Merge a duplicate firm into the one to keep |
| `firms.reconcile.create` | POST | `/api/firms/reconcile` | Derive firms from contacts' free-text employer |
| `firms.reconcile.list` | GET | `/api/firms/reconcile` | How much of the workspace is in the institution layer |
| `firms.update` | PATCH | `/api/firms/{id}` | Edit a firm |
| `network.contacts.merge.create` | POST | `/api/network/contacts/merge` | Merge a duplicate contact into the one to keep |
| `network.contacts.research.create` | POST | `/api/network/contacts/{id}/research` | Research a contact now |
| `network.contacts.research.facts.retract.create` | POST | `/api/network/contacts/{id}/research/facts/{factId}/retract` | Retract a verified research fact |
| `network.contacts.research.list` | GET | `/api/network/contacts/{id}/research` | Verified research facts for a contact |
| `network.merges.list` | GET | `/api/network/merges` | Recent contact and firm merges |
| `network.merges.undo.create` | POST | `/api/network/merges/{id}/undo` | Reverse a merge |
| `network.sheet-link.create` | POST | `/api/network/sheet-link` | Link a sheet tab to the network, and import it |
| `network.sheet-link.delete` | DELETE | `/api/network/sheet-link` | Unlink a network sheet |
| `network.sheet-link.list` | GET | `/api/network/sheet-link` | The Google Sheets linked to the network (firms + contacts) |
| `network.sheet-link.sync.create` | POST | `/api/network/sheet-link/sync` | Sync the network sheet now |
| `network.sheet-link.update` | PATCH | `/api/network/sheet-link` | Arm, disarm or rename the network mirror |
| `network.summary.list` | GET | `/api/network/summary` | Network counts and filter options |

---

### `deals.audience.create`

`POST /api/deals/audience`

Suppress an address, or reconcile the audience with AngelSend

Admin only — including `unsuppress`, which re-permits mail to someone who asked us to stop. `action: "sync"` runs ONE `direction`. They are separate on purpose and running one is not "syncing the audience": * `optouts_in` — pull AngelSend's do-not-email list into this workspace's. The safety-critical one: until it has run, a person who unsubscribed from an AngelSend campaign still receives Kavanah cadence steps, because the two lists never met. * `optouts_out` — push this workspace's own opt-outs to AngelSend. * `contacts_in` — pull an AngelSend segment (or the whole lead list) into the Deal Room. Gap-filling: it never overwrites a field somebody curated here. * `contacts_out` — push Deal Room contacts into an AngelSend project. This direction OVERWRITES whole AngelSend rows, because `import-leads` has no partial form; a field Kavanah does not hold is blanked there. Opted-out and bounced addresses are excluded, since importing one is how an opt-out gets quietly undone.

Body (application/json):
  - `action` (string, required) — one of: `suppress`, `unsuppress`, `sync`
  - `email` (string) — Required for suppress / unsuppress.
  - `reason` (string)
  - `note` (string)
  - `direction` (string) — one of: `optouts_in`, `optouts_out`, `contacts_in`, `contacts_out`
  - `projectId` (string) — AngelSend project. Required for contacts_out.
  - `segmentId` (string) — Segment to pull for contacts_in; omit for the whole lead list.
  - `limit` (integer) — Rows to pull for contacts_in. Default 200, capped at 500.

### `deals.audience.list`

`GET /api/deals/audience`

This workspace's outbound opt-out list

Addresses this workspace must not email. Member-level: anyone about to email someone needs to be able to check. Note what is NOT here. The platform-wide suppression list (hard bounces and spam complaints) is keyed by address alone and shared across every tenant, because those are facts about the address and about the sending infrastructure. This endpoint returns only the opt-outs this workspace recorded — a campaign opt-out is said to one desk, and putting it in the global list would silently stop mail to that address from every other workspace on the platform.

### `deals.audience.schedule.list`

`GET /api/deals/audience/schedule`

The scheduled AngelSend audience sync

Which directions are on, whose AngelSend key runs them, and each direction's last run and result. Every direction defaults OFF; a workspace with no row runs nothing.

### `deals.audience.schedule.set`

`PUT /api/deals/audience/schedule`

Turn the scheduled AngelSend directions on or off

Admin only, and it runs with the SAVING admin's AngelSend key — the job re-checks them as an active admin on every run and pauses itself if they are not. Only the fields sent change. `optoutsInEnabled` (hourly) imports AngelSend's do-not-email list into this workspace's suppression list. `contactsPullEnabled` (daily) gap-fills Deal Room contacts from a segment (paged) or the newest 500 leads. `contactsPushEnabled` (daily) is CREATE-ONLY: it sends only addresses AngelSend has never held, because AngelSend's import overwrites the whole lead row — status, tags and notes included.

Body (application/json):
  - `optoutsInEnabled` (boolean)
  - `contactsPullEnabled` (boolean)
  - `pullSegmentId` (string)
  - `pullProjectId` (string)
  - `contactsPushEnabled` (boolean)
  - `pushProjectId` (string) — Required to turn the push on.

### `deals.cadences.angelsend.create`

`POST /api/deals/cadences/{id}/angelsend`

Sync a cadence's AngelSend campaign now

Admin only. Removes stopped and suppressed recipients from AngelSend, reads sends, replies and unsubscribes back, re-verifies the archive copy and hands new enrollments over (which AngelSend then emails).

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `dealId` (string<uuid>)

### `deals.cadences.angelsend.list`

`GET /api/deals/cadences/{id}/angelsend`

The native AngelSend campaign(s) behind a cadence

Every mirror of this cadence — one for a network cadence, one per deal for a deal cadence — with its status, AngelSend campaign id, channel, daily limit, AngelSend sender capacity, the archive copy as last VERIFIED on AngelSend, AngelSend's counts and the last problem. Off unless an admin turned it on. `deals` lists the deals a deal cadence is running on.

Path params (positional, in order):
  - `id`

### `deals.cadences.angelsend.set`

`PUT /api/deals/cadences/{id}/angelsend`

Back a cadence with a native AngelSend campaign, or stop

Admin only, and it runs with the SAVING admin's AngelSend key (re-checked as an active admin every run). ON creates the AngelSend campaign from the cadence's steps and runs the first sync immediately, which hands every enrollment that has not sent yet to AngelSend after checking both suppression lists — AngelSend then emails them. OFF pauses the AngelSend campaign; enrollments AngelSend never received return to Kavanah's own sending. Refused (and the campaign paused) when a step is personalized, when AngelSend has no CAN-SPAM company address, or under compliance mode when AngelSend cannot be shown to carry the archive BCC. A deal cadence needs `dealId`; a network cadence must not have one. `sendChannel` `resend` sends on AngelSend's own infrastructure; `gmail` / `outlook` send from the admin's own mailbox and add no capacity.

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `enabled` (boolean, required)
  - `dealId` (string<uuid>)
  - `sendChannel` (string) — one of: `gmail`, `outlook`, `resend`
  - `senderAddressId` (string)
  - `dailyLimit` (integer)
  - `handoffInFlight` (boolean) — Default false. true also hands enrollments that ALREADY sent on Kavanah to AngelSend at their next step (verified via set-recipient-start-step; a step is never sent twice). Turning the mirror on also clears a sticky missing-archive refusal.

### `deals.cadences.create`

`POST /api/deals/cadences`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `deals.cadences.delete`

`DELETE /api/deals/cadences/{p1}`

(undocumented route — params unknown, pass them explicitly)

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `deals.cadences.enroll-bulk.create`

`POST /api/deals/cadences/{id}/enroll-bulk`

Enroll up to 200 contacts in one cadence

Enrolls each contact through the same checks as a single enrollment — the cadence's kind must match (a deal cadence needs `dealId`, a network cadence must not have one), the contact must belong to this workspace, and a contact already in an active sequence on the deal (or in another network cadence) is reported rather than enrolled twice. An address on the workspace's or the platform's do-not-email list is reported as `suppressed` and not enrolled. This ARMS UNATTENDED OUTBOUND EMAIL: every enrolled contact receives each step from the caller's own connected mailbox until the sequence ends, they reply, or someone stops it. For a deal cadence the caller needs edit access on the deal, and each contact must be on the deal, because stop-on-reply follows the deal's contacts. `addToDeal: true` links the ones who are not (role `other`) first; without it they come back as `not_on_deal`. More than 200 contacts is refused with nothing enrolled — never truncated.

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `contactIds` (string<uuid>[], required)
  - `dealId` (string<uuid>) — Required for a deal cadence; must be omitted for a network cadence.
  - `addToDeal` (boolean) — Link contacts not yet on the deal before enrolling them. Default false.
  - `provider` (string) — one of: `auto`, `gmail`, `angelsend`

### `deals.cadences.enroll.create`

`POST /api/deals/cadences/{p1}/enroll`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `deals.cadences.experiment.list`

`GET /api/deals/cadences/{id}/experiment`

A cadence's subject/sender experiment and winner policy

The cadence's design (`linked` — one hash picks the arm, so subject and sender are confounded — or `factorial` — subject and sender assigned by independent hashes), per-factor outcome stats per contact (replies, positive replies, meetings; opens are not tracked), each level's Bayesian probability to be best, the automatic winner policy and its current verdict, and the recent winner decisions. Member-level.

Path params (positional, in order):
  - `id`

### `deals.cadences.experiment.update`

`PATCH /api/deals/cadences/{id}/experiment`

Configure a cadence's experiment design and automatic winner policy

Admin only. `autoWinnerEnabled` (default false) needs `design: factorial`; once on, new enrollments shift to a declared winner while `explorePct` of them stay evenly split. A contact's subject and sender are fixed at their first send and are never changed by this call. Turning the policy off, changing the metric, or `resetWinner` clears the verdict and records it in the decision log.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `design` (string) — one of: `linked`, `factorial`
  - `autoWinnerEnabled` (boolean)
  - `metric` (string) — one of: `reply`, `positive_reply`, `meeting`
  - `minPerArm` (integer)
  - `explorePct` (integer)
  - `threshold` (number)
  - `resetWinner` (string) — one of: `subject`, `sender`, `all`

### `deals.cadences.list`

`GET /api/deals/cadences`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `deals.cadences.update`

`PATCH /api/deals/cadences/{p1}`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `deals.contact-runway.list`

`GET /api/deals/contact-runway`

How long each live network cadence can keep reaching new people

Per enabled NETWORK cadence: sendable contacts never enrolled in it (has an email, not archived, not suppressed at either level), contacts enrolled but not yet emailed, the measured pace of FIRST emails over the last week (capped by today's send capacity), and the days that leaves. A cadence that sent no first email in the window has no runway clock and reports null rather than zero. Also returns the warning threshold and when admins were last warned. A workspace with no live network cadence gets an empty list and is never warned — that is the opt-in.

### `deals.contact-runway.update`

`PATCH /api/deals/contact-runway`

Set the contact-runway warning threshold (admin)

Admin only: the threshold decides when every workspace admin is emailed. Whole days, 1-90, default 7.

Body (application/json):
  - `thresholdDays` (integer, required)

### `deals.conversations.list`

`GET /api/deals/conversations`

The Rain Room conversation map

One row per (deal, contact) conversation, plus one row per contact on NO open deal who has contact-level mail or an active network cadence enrollment (`dealId: null`, `source: "network"`): when they last wrote, when we last wrote, whose turn it is, days since, the active cadence step and the desk's next step. Sorted "we owe a reply" first, OLDEST first. Whose turn it is comes from EMAIL only - a meeting or a call is two-way and settles nothing about who owes the next message. A deal with no email of its own falls back to the contact's last mail anywhere, and the row says so (`source: "contact"`, timestamps only). A no-deal row's mail is the contact's own, so `source: "network"` carries its summaries. `stage`, `pipeline` and a user-id `owner` are deal filters: when any is set, no-deal rows are left out. `owner=unassigned` includes them (a contact on no deal has no owner). Private deals the caller cannot open are excluded, exactly as in the deal list. Bounded: past the cap the response says `truncated: true` rather than returning a silent sample.

Query:
  - `owner` (string) — A user id, `me`, or `unassigned`.
  - `stage` (string<uuid>)
  - `pipeline` (string<uuid>)
  - `include_closed` (string) — one of: `1`

### `deals.create`

`POST /api/deals`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `deals.data-room-analysis.create`

`POST /api/deals/{id}/data-room-analysis`

Read the deal's data room now

Reads up to 12 documents from the deal's Drive folder and records the investment profile plus 6-10 sourced insights. Every insight's quote is checked against the extracted text and every number in it must appear in its quote; anything else is dropped. One AI call billed to the signed-in user (402 when they cannot cover it); not gated on the automatic-analysis flag. A profile someone recorded by hand is kept unless `overwriteProfile` is true. With `force` false, an unchanged folder returns the stored reading without a model call. Needs edit access on the deal. Rate-limited to 3 per deal per minute.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `force` (boolean) — Re-read even if the folder has not changed.
  - `overwriteProfile` (boolean) — Replace a hand-recorded investment profile.

### `deals.data-room-analysis.list`

`GET /api/deals/{id}/data-room-analysis`

The deal's stored data-room reading

The last reading of the deal's Google Drive data room: status, which files were read or skipped and why, the sourced insight library (each insight with its file name and a passage quoted verbatim from it), how many proposed insights were dropped as unsupported, and whether automatic analysis (`data_room_analysis_enabled`) is on for the workspace. Free — reads nothing from Drive. `analysis` is null when the room was never read. Needs view access on the deal.

Path params (positional, in order):
  - `id`

### `deals.follow-ups.list`

`GET /api/deals/follow-ups`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `deals.forecast.list`

`GET /api/deals/forecast`

The Deal Room revenue forecast, calculated live

Computed from the deal records as the caller sees them — private deals they cannot open, and their sums, are left out. Probability is the stage's baseline probability × momentum ÷ 50 (momentum 50 is neutral, built from counterparty activity on each deal's timeline, time in stage and a passed close date). Revenue is each deal's recorded fee, or deal size × the workspace's assumed fee % where none is recorded. When the workspace reports fee bands separately, every total is per band and no combined figure is present. Not cached: the recalculate and settings routes beside it change what it returns.

Query:
  - `pipeline` (string) — Pipeline id; omit (or __all) for every pipeline.
  - `tz` (string) — IANA timezone deciding what 'this week' means. Defaults to the caller's.

### `deals.forecast.preview-email.create`

`POST /api/deals/forecast/preview-email`

Email the weekly forecast to yourself for review

Sends the forecast email, exactly as the schedule would build it, to the caller's own address only — built with the caller's Deal Room visibility. Rate-limited per member.

### `deals.forecast.recalculate.create`

`POST /api/deals/forecast/recalculate`

Recalculate the forecast onto every open deal now (admin)

The same write the daily job makes: forecast probability, momentum, expected fee, close week and confidence on every open deal, with a timeline entry on each deal whose forecast moved. Returns counts only. Runs are serialized per workspace and read "today" in the workspace's timezone.

**Destructive** — needs `--yes` against a non-local base URL.

### `deals.forecast.settings.list`

`GET /api/deals/forecast/settings`

Forecast settings and the weekly forecast email schedule

### `deals.forecast.settings.set`

`PUT /api/deals/forecast/settings`

Configure the forecast (admin)

Admin only. Only the fields sent change — including `email.enabled`, which keeps its stored value when omitted, and the schedule's cron, which is kept when neither `day` nor `time` is sent. Automatic daily recalculation writes the forecast onto every open deal's forecast fields (never its own probability). The weekly email goes to active non-guest workspace members only, computed as the report's creator sees Deal Room; any other recipient is refused. Send `expectedWorkspaceId` (the `workspaceId` the GET returned) to have a save refused with 409 when the caller's active workspace has changed since.

Body (application/json):
  - `expectedWorkspaceId` (string) — The workspace the draft was loaded for.
  - `settings` (object)
  - `settings.autoRecalculateEnabled` (boolean)
  - `settings.defaultFeePct` (number) — Percent, 0–100.
  - `settings.bandThresholdDollars` (number)
  - `settings.lowerBandLabel` (string)
  - `settings.upperBandLabel` (string)
  - `settings.disclaimer` (string)
  - `email` (object)
  - `email.enabled` (boolean)
  - `email.day` (string) — one of: `sunday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday`, `saturday`
  - `email.time` (string) — HH:MM, 24h, local to timezone.
  - `email.timezone` (string)
  - `email.recipients` (string<email>[])
  - `email.subjectTemplate` (string)

### `deals.get`

`GET /api/deals/{p1}`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `deals.import.create`

`POST /api/deals/import`

(undocumented route — params unknown, pass them explicitly)

**Destructive** — needs `--yes` against a non-local base URL.

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `deals.import.preview.create`

`POST /api/deals/import/preview`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `deals.issuer-campaigns.create`

`POST /api/deals/issuer-campaigns`

Create an issuer campaign

Sends nothing and arms nothing. Size is scored on a company's raise target; with none recorded its last completed round stands in as a proxy at half weight. A raise below raiseMinDollars is excluded, above raiseMaxDollars is a penalty. `cadence` must be a NETWORK cadence.

Body (application/json):
  - `name` (string, required)
  - `themes` (string[])
  - `sectors` (string[])
  - `stages` (string[])
  - `geographies` (string[])
  - `raiseMinDollars` (number|null)
  - `raiseMaxDollars` (number|null)
  - `summary` (string)
  - `cadence` (string|null) — NETWORK cadence id or exact name
  - `batchSize` (integer)
  - `contactsPerFirm` (integer)
  - `provider` (string) — one of: `auto`, `gmail`, `angelsend`

### `deals.issuer-campaigns.get`

`GET /api/deals/issuer-campaigns/{id}`

One issuer campaign

Path params (positional, in order):
  - `id`

### `deals.issuer-campaigns.list`

`GET /api/deals/issuer-campaigns`

List issuer campaigns (client prospecting)

Every issuer campaign — a named client mandate the workspace prospects against before there is a deal — with its funnel state (`state`: currentBatch, released, spent, engaged, converted, remainingRanked, exhausted) and cadence. `?includeArchived=1` adds archived campaigns.

Query:
  - `includeArchived` (string) — one of: `1`

### `deals.issuer-campaigns.matches.convert.create`

`POST /api/deals/issuer-campaigns/{id}/matches/{firmId}/convert`

Convert a prospect into a deal

Creates the deal (caller as owner; default pipeline's first open stage unless told), links every contact at the firm (warmest as primary) and records the match as converted — every issuer ranking in the workspace then excludes the firm. An unknown pipeline is refused, never silently the default.

Path params (positional, in order):
  - `id`
  - `firmId`

Body (application/json):
  - `name` (string)
  - `amountDollars` (number|null)
  - `pipeline` (string)
  - `stage` (string)
  - `expectedClose` (string<date>)
  - `notes` (string)

### `deals.issuer-campaigns.matches.list`

`GET /api/deals/issuer-campaigns/{id}/matches`

The campaign's ranked prospects

Rank order, each with score (out of 100), reasons, tranche, status (ranked, released, approached, engaged, converted, dismissed), the deal it became, and the firm's raise target / last round (`lastFundingCents` is the size proxy when no raise target is recorded).

Path params (positional, in order):
  - `id`

Query:
  - `status` (string) — one of: `ranked`, `released`, `approached`, `engaged`, `converted`, `dismissed`
  - `limit` (integer)

### `deals.issuer-campaigns.pause.create`

`POST /api/deals/issuer-campaigns/{id}/pause`

Pause an issuer campaign

Auto-release off and the cadence detached, so nothing more is released or enrolled automatically. `stopEnrollments: true` also stops the sequences the campaign started and pulls back their queued sends (mail already sent stays sent); `archive: true` archives it.

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `stopEnrollments` (boolean)
  - `archive` (boolean)

### `deals.issuer-campaigns.rank.create`

`POST /api/deals/issuer-campaigns/{id}/rank`

Rank issuers against the campaign's mandate

Scores every issuer in the workspace and records the ranking. Contacts nobody, releases nothing, resets nobody's status, uses no AI.

Path params (positional, in order):
  - `id`

### `deals.issuer-campaigns.start.create`

`POST /api/deals/issuer-campaigns/{id}/start`

Start, top up or resume an issuer campaign

ARMS UNATTENDED OUTBOUND EMAIL from the caller's own mailbox. Ranks if never ranked, releases the next tranche when the current one is fully worked (a re-run while a tranche is open is a top-up that releases nothing), and enrolls the warmest person with an email at each firm in the NETWORK cadence, up to 200 people per call. `autoRelease` must be a boolean; omitted keeps the stored value (default false). A paused campaign resumes by naming its cadence. Refusals are 409 with `code`.

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `cadence` (string)
  - `batchSize` (integer)
  - `contactsPerFirm` (integer)
  - `autoRelease` (boolean)
  - `provider` (string) — one of: `auto`, `gmail`, `angelsend`

### `deals.issuer-campaigns.update`

`PATCH /api/deals/issuer-campaigns/{id}`

Edit an issuer campaign's definition

Same fields as create, all optional; an omitted field keeps its value. Sends nothing and resets nobody's status — re-rank to re-score.

Path params (positional, in order):
  - `id`

Body: application/json (free-form — pass with `--data`)

### `deals.list`

`GET /api/deals`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `deals.sheet-link.list`

`GET /api/deals/sheet-link`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `deals.sheet-link.sync.create`

`POST /api/deals/sheet-link/sync`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `deals.sheet-link.update`

`PATCH /api/deals/sheet-link`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `deals.staffing-settings.list`

`GET /api/deals/staffing-settings`

Deal-team staffing settings

`autoStaffEnabled` (default false) — provision-client-space fills a deal's team to `minTeamSize` and picks a lead if it has none before it invites anyone. `minTeamSize` / `maxTeamSize` (defaults 5 and 10, 1–25) bound the automatic fill and the on-demand suggestion. Member-level read.

### `deals.staffing-settings.set`

`PUT /api/deals/staffing-settings`

Update deal-team staffing settings (admin)

Partial patch; an omitted field keeps its value. `autoStaffEnabled` must be a boolean. minTeamSize above maxTeamSize is refused.

Body (application/json):
  - `autoStaffEnabled` (boolean)
  - `minTeamSize` (integer)
  - `maxTeamSize` (integer)

### `deals.stages.create`

`POST /api/deals/stages`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `deals.stages.delete`

`DELETE /api/deals/stages/{p1}`

(undocumented route — params unknown, pass them explicitly)

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `deals.stages.update`

`PATCH /api/deals/stages/{p1}`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `deals.team.list`

`GET /api/deals/{id}/team`

The deal team (our side)

Who on OUR side is on the deal: the lead first (role `lead` — this is the deal's owner, `owner_user_id`, rendered with their profile), then the roster members (role `member`) with each one's title on this deal, in the order they were added. `isActiveMember` is false for someone who has since left the workspace; the roster keeps them for the record. Needs view access on the deal, through the same record gate as `GET /api/deals/{id}` — a private deal's roster says who is working on it. The same list is included as `team` in the deal detail payload.

Path params (positional, in order):
  - `id`

### `deals.team.set`

`PUT /api/deals/{id}/team`

Replace the deal team

A whole-roster write. `members` is the ENTIRE member list — anyone absent from it is removed, titles are updated to what is sent. `lead` is optional: absent leaves the lead alone, `null` clears it, a user id makes that person the lead. The lead IS `app_deals.owner_user_id`, so a lead change is the same write as `PATCH /api/deals/{id}` with `ownerUserId` — it records the `owner_change` activity and resolves `owner_name` from the profile. When the lead changes, the previous lead is kept on the deal only if `members` names them. Every member must be an ACTIVE member of this workspace. An id that is not, or a title over 80 characters, is returned in `rejected` with a reason, and the rest of the list is still applied — nothing is dropped silently. Needs edit access on the deal.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `lead` (string|null<uuid>) — New lead's user id, or null to clear. Omit to leave it.
  - `members` (object[], required)

### `deals.team.staff.create`

`POST /api/deals/{id}/team/staff`

Confirm a staffing proposal

ADDITIVE: adds each named member (title default "Analyst") and sets the lead only when the deal has no active lead — never removes anyone, never replaces a lead (use PUT /api/deals/{id}/team for that). Ids that are not active members of this workspace come back in `rejected`. The people added are emailed and pushed (the `deals` notification channel) and, when the deal already has a Slack channel / Drive folder and `inviteToSpace` is not false, invited through the CALLER's own Slack and Google connections. Needs edit access on the deal.

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `leadUserId` (string|null<uuid>)
  - `memberUserIds` (string<uuid>[])
  - `title` (string)
  - `inviteToSpace` (boolean)

### `deals.team.suggest.list`

`GET /api/deals/{id}/team/suggest`

Propose a deal team (read-only)

Ranks the workspace's ACTIVE members for the analyst seat — and for the lead seat when the deal has no active lead — on job title (Analyst/Associate fit the analyst seat, Director/VP/MD/Partner the lead), skill profile, experience against the deal's sector, category, issuance stage and geography, each person's own reported availability, and the open deals and task hours they already carry. Writes nothing and uses no AI. `plan.needed` is how many members the team lacks to reach the workspace minimum; `plan.members` is up to the maximum, best first; `plan.alternates` holds everyone else considered, including unavailable people (never proposed). Needs view access on the deal.

Path params (positional, in order):
  - `id`

### `deals.update`

`PATCH /api/deals/{p1}`

(undocumented route — params unknown, pass them explicitly)

Path params (positional, in order):
  - `p1`

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `firms.create`

`POST /api/firms`

Create or update a firm

Resolves to an existing firm rather than creating a duplicate. DOMAIN is matched before name, because two funds can share a name but a mail domain belongs to one of them — so pass `domain` whenever it is known. Free-mail domains are ignored; they identify no firm. Money fields are supplied in DOLLARS and stored as integer cents.

Body (application/json):
  - `name` (string, required)
  - `domain` (string) — Accepts a bare host, a URL or an email address.
  - `roles` (string[])
  - `website` (string)
  - `linkedin_url` (string)
  - `aum_dollars` (number)
  - `dry_powder_dollars` (number)
  - `check_size_min_dollars` (number)
  - `check_size_max_dollars` (number)
  - `thesis` (string)
  - `sectors` (string[])
  - `stages` (string[])
  - `geographies` (string[])
  - `notes` (string)

### `firms.delete`

`DELETE /api/firms/{id}`

Archive a firm

Archives rather than deletes. Contacts survive with their firm link nulled — a person we know is not lost when their employer record is.

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `id`

### `firms.get`

`GET /api/firms/{id}`

One firm, plus every relationship held there

Returns the firm and its contacts, each with a warmth score.

Path params (positional, in order):
  - `id`

### `firms.list`

`GET /api/firms`

List institutions (the investor / issuer matrix)

Firms with AUM, dry powder, check size, thesis, sectors and a count of the contacts held at each. A firm is the entity that writes the cheque; a contact is a person at it. Filter by `role` (investor / issuer / broker_dealer / service_provider / other), `sector`, `min_aum_dollars`, or a `search` across name and thesis.

Query:
  - `role` (string)
  - `search` (string)
  - `sector` (string)
  - `min_aum_dollars` (number)
  - `limit` (integer)

### `firms.merge.create`

`POST /api/firms/merge`

Merge a duplicate firm into the one to keep

Admin only — it collapses two records for everyone in the workspace. FILL, NEVER OVERWRITE: empty fields on the kept firm take the duplicate's values, roles and list fields union, and a disagreement is REPORTED (`result.differences`) rather than resolved. Contacts, investor / broker-dealer matches, partner pairings and sheet import snapshots move to the kept firm; where both held a match on the same deal, the kept firm's row stays and a HUMAN decision on the duplicate's (dismissed, approached) carries over. The duplicate is archived with `merged_into_id` pointing at the winner, and every importer follows that pointer — without it the next hourly sheet sync re-creates what was just merged away. `result.mergeId` is what `POST /api/network/merges/{id}/undo` reverses.

**Destructive** — needs `--yes` against a non-local base URL.

Body (application/json):
  - `winner_id` (string, required) — The firm to KEEP.
  - `loser_id` (string, required) — The duplicate to archive.

### `firms.reconcile.create`

`POST /api/firms/reconcile`

Derive firms from contacts' free-text employer

Groups existing contacts by employer name, creates a firm for each, and attaches them. This is what turns "two contacts at the same fund are two strings that happen to match" into one firm with two relationships. Grouping is by NAME, with the domain inferred from the group's modal corporate address — so a contact on a personal address, or with no address at all, still lands at their firm. Domain-first grouping would silently drop exactly those people. Idempotent: only ever fills an EMPTY firm link, so a contact someone deliberately pointed elsewhere is never overruled. Pass `dry_run` to get the plan without writing.

Body (application/json):
  - `dry_run` (boolean)
  - `limit` (integer)
  - `roles` (string[]) — Roles applied to firms this run creates.

### `firms.reconcile.list`

`GET /api/firms/reconcile`

How much of the workspace is in the institution layer

Total contacts, how many are attached to a firm, how many still carry a usable employer name with no firm behind it, and how many firms exist. Junk employer strings ("N/A", "self-employed") are excluded from the unlinked count, because reconciliation deliberately skips them and counting them would promise a fix that will not come.

### `firms.update`

`PATCH /api/firms/{id}`

Edit a firm

A human edit. Passing `lock_fields` marks columns as curated, after which enrichment will not overwrite them — the mechanism that stops an automated refresh quietly reverting a correction made by hand.

Path params (positional, in order):
  - `id`

Body (application/json):
  - `name` (string)
  - `domain` (string)
  - `website` (string)
  - `linkedin_url` (string)
  - `aum_dollars` (number)
  - `dry_powder_dollars` (number)
  - `thesis` (string)
  - `notes` (string)
  - `lock_fields` (string[]) — Column names enrichment must not overwrite.

### `network.contacts.merge.create`

`POST /api/network/contacts/merge`

Merge a duplicate contact into the one to keep

Admin only. The kept contact's empty fields are filled from the duplicate (tags union; last-touch timestamps take the later of the two); deal links, cadence enrollments, activity, document views and sheet snapshots re-point to it; the duplicate is archived and later imports follow its address to the kept contact. Where BOTH were enrolled in the same sequence the duplicate's enrollment is CANCELLED, so the person is not mailed twice — and an undo deliberately leaves it cancelled rather than resuming outbound email from an undo button. `result.mergeId` is what `POST /api/network/merges/{id}/undo` reverses.

**Destructive** — needs `--yes` against a non-local base URL.

Body (application/json):
  - `winner_id` (string, required)
  - `loser_id` (string, required)

### `network.contacts.research.create`

`POST /api/network/contacts/{id}/research`

Research a contact now

Runs the research pipeline for one contact and stores only facts that pass the fact-check. Spends credits (typically 25-40), billed to the caller; 402 when they cannot cover one run. LinkedIn is never scraped.

Path params (positional, in order):
  - `id`

### `network.contacts.research.facts.retract.create`

`POST /api/network/contacts/{id}/research/facts/{factId}/retract`

Retract a verified research fact

Admin only. The fact is never offered to an opener again; a later run that re-finds it leaves it retracted.

Path params (positional, in order):
  - `id`
  - `factId`

### `network.contacts.research.list`

`GET /api/network/contacts/{id}/research`

Verified research facts for a contact

Facts about the contact and its firm that passed the fact-check gate (verbatim quote on the source page, re-confirmed on an independent re-fetch, identity corroborated, judged to support the statement), each with source URL, quote, source date, retrieval/verification dates and expiry. Plus the last research runs with discard reasons.

Path params (positional, in order):
  - `id`

Query:
  - `include_expired` (string) — one of: `1`

### `network.merges.list`

`GET /api/network/merges`

Recent contact and firm merges

Newest first, with whether each has been undone.

Query:
  - `limit` (integer)

### `network.merges.undo.create`

`POST /api/network/merges/{id}/undo`

Reverse a merge

Admin only. Restores the archived record and moves back everything the merge moved, reading the journal written in the merge's own transaction — never a payload the caller supplies. Per field, only a value still exactly as the merge left it is put back; anything edited since is KEPT and named in `result.keptFields`. A cadence enrollment the merge cancelled is NOT re-activated. 409 when the records have moved on too far to reverse safely: the merge was already undone, the kept record was itself merged away (undo that one first), or another active record now holds the archived one's email / name / domain.

Path params (positional, in order):
  - `id`

### `network.sheet-link.create`

`POST /api/network/sheet-link`

Link a sheet tab to the network, and import it

With only `spreadsheet` this is a DRY RUN that lists the file's tabs. With `tab` it maps the headers (or takes `columnMapping`), saves the link — which is what turns on the HOURLY import — and runs the first import. The import GAP-FILLS: an empty Kavanah field takes the sheet's value, a field still holding what the sheet last supplied follows the sheet, and a value someone edited in Kavanah is never overwritten (it is counted as `fieldsKeptHandEdited`). Money cells accept "$1.2B", "250M", "$5M - $25M"; a cell that cannot be read is skipped and reported, never guessed. Linking never writes to the spreadsheet — only the mirror does.

Body (application/json):
  - `spreadsheet` (string, required) — Sheets URL or spreadsheet id.
  - `tab` (string) — Omit to list the tabs.
  - `columnMapping` (object) — header → canonical field (firm_name, firm_aum, contact_email, …). Omit to auto-guess.

### `network.sheet-link.delete`

`DELETE /api/network/sheet-link`

Unlink a network sheet

Soft: the hourly import and mirror stop, nothing already imported is removed, and the spreadsheet is untouched. Re-linking the same sheet and tab revives the SAME row, so its per-field import snapshots still apply — without them every value the sheet ever wrote would read as a hand edit and stop following the sheet. A revived link comes back with the mirror OFF unless it is armed again explicitly.

**Destructive** — needs `--yes` against a non-local base URL.

Query:
  - `link_id` (string)

### `network.sheet-link.list`

`GET /api/network/sheet-link`

The Google Sheets linked to the network (firms + contacts)

Every active link with its column mapping, mirror state and last import summary.

### `network.sheet-link.sync.create`

`POST /api/network/sheet-link/sync`

Sync the network sheet now

The gap-filling import, then the mirror when it is armed. Body `{linkId?}`; omit it to sync every linked sheet. A per-link lease stops this from importing a sheet the hourly cron is already importing.

Body (application/json):
  - `linkId` (string)

### `network.sheet-link.update`

`PATCH /api/network/sheet-link`

Arm, disarm or rename the network mirror

The mirror rewrites a SEPARATE tab with Kavanah's whole network every hour. It is a destructive overwrite of that tab, so it REFUSES any tab a Kavanah sync reads from — this link's source tab or any sibling link's in the same file, compared case- and whitespace-insensitively. The refusal is repeated at write time, because the cron never passes through this route. Arming (or renaming) is limited to the member who linked the sheet, or an admin: the mirror writes with the linking member's Google grant. Turning it OFF is open to any member.

Body (application/json):
  - `linkId` (string) — Required when more than one sheet is linked.
  - `mirrorEnabled` (boolean)
  - `mirrorTabName` (string)

### `network.summary.list`

`GET /api/network/summary`

Network counts and filter options

Firms by role and partner status, the sectors in use, and how many contacts sit at a firm.

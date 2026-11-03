# Inbox

5 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `inbox.count.list` | GET | `/api/inbox/count` | (undocumented route — params unknown, pass them explicitly) |
| `inbox.mark-all-read.create` | POST | `/api/inbox/mark-all-read` | Mark all inbox mail read in Kavanah |
| `inbox.messages.read.create` | POST | `/api/inbox/messages/read` | Mark inbox messages read or unread in Kavanah |
| `inbox.preferences.list` | GET | `/api/inbox/preferences` | Get inbox preferences |
| `inbox.preferences.update` | PATCH | `/api/inbox/preferences` | Update inbox preferences |

---

### `inbox.count.list`

`GET /api/inbox/count`

(undocumented route — params unknown, pass them explicitly)

_Not in either OpenAPI spec — flags are passed through unvalidated._

### `inbox.mark-all-read.create`

`POST /api/inbox/mark-all-read`

Mark all inbox mail read in Kavanah

Mail received up to now stops counting as unread in Kavanah (inbox list, sidebar count, app badge). Nothing is changed in the mail provider.

### `inbox.messages.read.create`

`POST /api/inbox/messages/read`

Mark inbox messages read or unread in Kavanah

Records a per-message read mark in Kavanah for any connected mailbox (Gmail via AngelSend or native, ProtonMail, Outlook, iCloud). Inbox listings report marked mail read and the sidebar count and app badge leave it out; unread deletes the mark. Gmail itself is changed too only when the native grant has gmail.modify (providerUpdated).

Body (application/json):
  - `provider` (string, required) — one of: `gmail`, `protonmail`, `microsoft365`, `icloud`
  - `ids` (string[], required)
  - `read` (boolean, required)

### `inbox.preferences.list`

`GET /api/inbox/preferences`

Get inbox preferences

### `inbox.preferences.update`

`PATCH /api/inbox/preferences`

Update inbox preferences

notifyEnabled false stops new-email push notifications and leaves unread mail out of the app-icon badge.

Body (application/json):
  - `notifyEnabled` (boolean, required)

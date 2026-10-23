# Inbox

4 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `inbox.count.list` | GET | `/api/inbox/count` | (undocumented route — params unknown, pass them explicitly) |
| `inbox.mark-all-read.create` | POST | `/api/inbox/mark-all-read` | Mark all inbox mail read in Kavanah |
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

### `inbox.preferences.list`

`GET /api/inbox/preferences`

Get inbox preferences

### `inbox.preferences.update`

`PATCH /api/inbox/preferences`

Update inbox preferences

notifyEnabled false stops new-email push notifications and leaves unread mail out of the app-icon badge.

Body (application/json):
  - `notifyEnabled` (boolean, required)

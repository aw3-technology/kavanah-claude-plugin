# Activity

2 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `activity.create` | POST | `/api/activity` | Append an activity item |
| `activity.list` | GET | `/api/activity` | Get workspace activity feed |

---

### `activity.create`

`POST /api/activity`

Append an activity item

Body (application/json):
  - `item` (object, required)
  - `item.name` (string)
  - `item.action` (string)
  - `item.detail` (string)
  - `item.tone` (string) — one of: `sand`, `rose`, `olive`, `slate`, `peach`
  - `item.initials` (string)
  - `item.status` (string) — one of: `online`, `busy`, `neutral`

### `activity.list`

`GET /api/activity`

Get workspace activity feed

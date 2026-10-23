# Calendar

2 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `calendar.export.list` | GET | `/api/calendar/export` | Export the workspace calendar as iCalendar |
| `calendar.tasks.list` | GET | `/api/calendar/tasks` | List visible tasks scheduled in a date window (inclusive) |

---

### `calendar.export.list`

`GET /api/calendar/export`

Export the workspace calendar as iCalendar

Returns a `text/calendar` .ics attachment covering the full meeting history (paged internally). Requires the `export` capability.

### `calendar.tasks.list`

`GET /api/calendar/tasks`

List visible tasks scheduled in a date window (inclusive)

Query:
  - `from` (string, required)
  - `to` (string, required)

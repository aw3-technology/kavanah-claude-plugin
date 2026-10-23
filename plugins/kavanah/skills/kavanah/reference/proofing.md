# Proofing

4 commands. Generated — run `npm run skill:gen` to refresh.

| Command | Method | Path | Summary |
| --- | --- | --- | --- |
| `proofing.annotations.create` | POST | `/api/proofing/{fileId}/annotations` | Add an annotation pin to an attachment |
| `proofing.annotations.delete` | DELETE | `/api/proofing/{fileId}/annotations/{annotationId}` | Delete an annotation |
| `proofing.annotations.list` | GET | `/api/proofing/{fileId}/annotations` | List annotations on an attachment |
| `proofing.annotations.update` | PATCH | `/api/proofing/{fileId}/annotations/{annotationId}` | Edit an annotation comment and/or toggle resolved |

---

### `proofing.annotations.create`

`POST /api/proofing/{fileId}/annotations`

Add an annotation pin to an attachment

Path params (positional, in order):
  - `fileId`

Body (application/json):
  - `x` (number, required)
  - `y` (number, required)
  - `page` (number)
  - `comment` (string)
  - `taskId` (integer)

### `proofing.annotations.delete`

`DELETE /api/proofing/{fileId}/annotations/{annotationId}`

Delete an annotation

**Destructive** — needs `--yes` against a non-local base URL.

Path params (positional, in order):
  - `fileId`
  - `annotationId`

### `proofing.annotations.list`

`GET /api/proofing/{fileId}/annotations`

List annotations on an attachment

Path params (positional, in order):
  - `fileId`

### `proofing.annotations.update`

`PATCH /api/proofing/{fileId}/annotations/{annotationId}`

Edit an annotation comment and/or toggle resolved

Path params (positional, in order):
  - `fileId`
  - `annotationId`

Body (application/json):
  - `comment` (string)
  - `resolved` (boolean)

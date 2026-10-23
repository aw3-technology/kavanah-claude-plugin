---
name: kavanah
description: Control Kavanah (kavanah.ai) from this session — read and write tasks, projects, clients, discussions, time entries, planning, reports, RBAC, integrations, and the AI agent, via the `kvn` CLI over the Kavanah REST API. Use when the user asks to look at, create, update, or delete anything in their Kavanah workspace, mentions a Kavanah task/project/client/sprint/deal by name, wants to drive their workspace from the terminal, or asks what the Kavanah API can do.
---

# Kavanah

`kvn` is a zero-dependency Node CLI over the Kavanah REST API. Every documented
operation is an explicit named command, indexed in `commands.json` and
documented under `reference/`. Kavanah's AI-agent toolkit is reachable too
(`kvn tool`, `kvn agent`).

## Running it

    node "${CLAUDE_SKILL_DIR}/bin/kvn.mjs" <command> [args]

Every example below writes this as `kvn`. When the skill is installed as the
Kavanah plugin, `kvn` is also on `PATH` and works as written.

Requires Node 18+. Targets `https://kavanah.ai` by default. `--local` switches to
`http://localhost:3000`; `--base <url>` targets anything else;
`$KAVANAH_BASE_URL` sets a persistent default.

## Signing in

    kvn login        # prints a code and opens the browser; an admin approves it
    kvn whoami       # who the saved key acts as
    kvn logout       # revoke the key and forget it

`kvn login` saves a workspace API key (`kvn_live_…`) to
`~/.kavanah/credentials.json`, one per base URL. It **waits until someone
approves the code in the browser**. Run it as a command the user can see, give
them the code and the URL it prints, and wait. Never approve the code yourself.

Approving needs a **workspace admin**, and the key acts as the person who
approved it, in the workspace active in their browser, with exactly their
permissions, re-checked on every request. Approval does not change who the key
acts as. If the user is not an admin, an admin can approve the code for them.

Other ways to supply a key, in order of precedence: `--key kvn_live_…`, then
`$KAVANAH_API_KEY`, then the saved login, then `~/.kavanah/api-key`, then
`KAVANAH_API_KEY=` in `./.env.local` or `./.env`. Admins can also mint keys at
Settings → API keys.

If no key is found, `kvn` prints these instructions and exits. Suggest
`kvn login` and do not try to work around it.

## Finding the right command

Do this before reading any reference file. It is faster and cheaper:

    kvn ls task            # every command matching "task" (name, path, or summary)
    kvn ls '^clients\.'    # patterns are regexes
    kvn groups             # every group, with command counts
    kvn help tasks.create  # params, body fields, enums, responses, example

Only open `reference/<group>.md` when you need to scan a whole area at once.
`reference/index.md` maps groups to files.

Command names are mechanical: literal path segments joined by `.`, plus a verb
(`list` / `get` / `create` / `update` / `set` / `delete`).

| Command | Call |
| --- | --- |
| `tasks.list` | `GET /api/tasks` |
| `tasks.get` | `GET /api/tasks/{id}` |
| `tasks.create` | `POST /api/tasks` |
| `tasks.update` | `PATCH /api/tasks/{id}` |
| `tasks.archive.create` | `POST /api/tasks/{id}/archive` |
| `projects.members.list` | `GET /api/projects/{id}/members` |

## Invoking a command

Path params are positional, in path order. Everything else is a `--flag`, routed
automatically. Declared query params go to the query string, and declared body
fields go to the JSON body. Undeclared flags follow the method: query for
GET/DELETE, body otherwise.

    kvn tasks.list --projectRef 1
    kvn tasks.create --projectRef 1 --title "Ship the skill" --priority High
    kvn tasks.update 412 --status_id completed
    kvn projects.members.list 3
    kvn clients.list --limit 50

Values are coerced against the declared type. `5` becomes a number,
`true`/`false`/`null` become literals, `{…}` and `[…]` are parsed as JSON, and
everything else stays a string. A field declared as a string stays a string even
when it looks numeric. Dotted flags nest (`--metadata.source cli`).

Other ways in:

    kvn tasks.create --data '{"projectRef":"1","title":"X"}'   # explicit body
    kvn tasks.create --data @body.json                          # from a file
    kvn tasks.create < body.json                                # redirected file
    cat body.json | kvn tasks.create --data -                   # a pipe needs --data -
    kvn call GET /api/some/undocumented/route                   # escape hatch

`kvn` never reads a pipe unless you pass `--data -`. That way a harness that
leaves stdin open cannot leave a command waiting forever.

Useful flags:

- `--dry-run` prints the request and sends nothing.
- `-i` prints the status and headers to stderr.
- `--raw` prints the response verbatim, unformatted.
- `--yes` confirms a destructive command.

## The agent toolkit

Separate from the REST API, Kavanah's AI agent has its own large tool registry.
It covers task decomposition, slip risk, goals, memory, runbooks, exec meetings,
deal-room sync, and every integration. Search it locally:

    kvn tools "log time"        # all words must match (name + description)
    kvn tools '^create_task$'   # regex works too

Full list: `reference/agent-toolkit.md`.

### Running one tool deterministically

When you know exactly which tool you want, skip the model:

    kvn tool list_projects
    kvn tool create_task --project_ref 1 --title "Audit the login flow"
    kvn tool <name> --dry-run              # show the payload, send nothing
    kvn ai-agent.tools.list --q task       # what THIS key may run, with schemas

`kvn tool` posts to `POST /api/ai-agent/tools/{name}/execute`. The server
applies the full governance stack: persona scope, read-only and admin-only
filtering, guardrails, the action policy, the action ledger, and undo. It is
also **fail-closed**. Chat treats an "approve" policy as allow, because a human
is watching. A programmatic call has no such human, so the action **parks**
instead:

- exit **0**: executed. If the tool is reversible, it prints an undo group id.
  Reverse it with `kvn undo.create`. That command takes no arguments and pops
  *your* most recent group, so run it before doing anything else undoable.
- exit **2**: parked (HTTP 202). **Nothing ran.** A human has to approve it.
  Re-running just parks it again, so don't retry.
- exit **1**: blocked by a guardrail or policy (403), or the tool is unknown to
  you (404).

A categorized tool with no policy row parks by default. That is the fail-closed
default working, not a misconfiguration.

Only tools in `kvn ai-agent.tools.list` are callable, because the endpoint
filters by persona scope, action mode, data scopes and admin-only rules. A 404
can mean "this tool exists, but not for you". `kvn tools` searches the whole
registry regardless.

`kvn ai-agent.approvals.list` and `kvn ai-agent.activity.list` show the parked
queue and the action ledger. Both are **admin-only**, so a member's key gets a
403 there even though its own action parked fine.

### Asking the agent

    kvn agent "log 2h against the login-flow task for today"
    kvn agent "what's slipping this sprint?"
    kvn agent "…" --conversation <id>   # continue a thread
    kvn agent "…" --persona <id>        # run as a persona

`kvn agent` posts to `POST /api/ai-agent`, with the same governance as chat.
**One `kvn agent` call is the full agent.** It can create tasks, send email, and
spend the workspace's credits. It is not a read-only sandbox. Prefer a specific,
bounded instruction over an open-ended one, and prefer `kvn tool` when you know
which tool you want.

Long runs: the client waits up to 5 minutes (`KAVANAH_AGENT_TIMEOUT_MS`). **A
client timeout does not cancel the run**, and it may still be writing. Check
`kvn ai-agent.activity.list` rather than re-issuing the prompt.

## Rules

- **Run `--dry-run` first for any write you are not certain about.** It prints
  the exact method, URL and body without sending anything.
- **Destructive commands need `--yes`** against any non-local base. That covers
  every `DELETE`, plus bulk task writes, member deprovision and transfer,
  resyncs, imports, and fan-out sends. The gate is off for `localhost`. Never
  pass `--yes` on the user's behalf for a command they did not ask for. Confirm
  the specific rows first.
- **The default base is production.** Writes hit the real workspace immediately.
  Say which base you are targeting when you report a write.
- **A 403 is an RBAC result, not a bug.** The key inherits its user's
  permissions, so a member's key cannot reach admin routes. Don't try to route
  around it.
- **Don't invent endpoints.** If `kvn ls` finds nothing, the route probably does
  not exist. Check `reference/index.md` before reaching for `kvn call`.
- **Commands marked `undocumented`** are real routes absent from the OpenAPI
  specs, so `kvn` cannot describe their params. Run `--dry-run` and a read-only
  probe first.


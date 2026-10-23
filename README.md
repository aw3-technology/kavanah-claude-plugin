# Kavanah for Claude Code

Drive your [Kavanah](https://kavanah.ai) workspace from Claude Code: tasks,
projects, clients, time, planning, deals, reports, and the Kavanah AI agent.

## Install

In Claude Code:

    /plugin marketplace add aw3-technology/kavanah-claude-plugin
    /plugin install kavanah@kavanah

Requires Node 18 or later.

## Sign in

Ask Claude to sign you in to Kavanah, or run this yourself:

    kvn login

It prints a code and opens kavanah.ai. A workspace admin approves the code, and
the CLI saves an API key to `~/.kavanah/credentials.json`. The key acts as the
approving admin, with exactly their permissions. Revoke it with `kvn logout` or
in Settings → API keys.

## Use

Just ask, for example "what's overdue in the Website Redesign project?" or "log
2h on the login-flow task". Claude finds the right `kvn` command. You can also
run `kvn` yourself:

    kvn ls task                    # find commands
    kvn help tasks.create          # params and an example
    kvn tasks.list --projectRef 1
    kvn tool list_projects         # run one Kavanah agent tool

Writes go to your real workspace. Destructive commands need `--yes`.

## MCP instead

Kavanah also exposes its agent tools over MCP, for clients other than Claude
Code:

    claude mcp add --transport http kavanah https://kavanah.ai/api/mcp \
      --header "Authorization: Bearer kvn_live_…"

---

Version 1.20261023.0. Generated from the Kavanah repository by
`npm run plugin:build`. Do not edit by hand.

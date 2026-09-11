# Using SeZzz with an agent

These instructions describe using the installed app, not building SeZzz.

## Connect

1. Install `SeZzz.app` in `/Applications` and launch it.
2. Open **Agents / Agent Integrations** from the menu bar panel.
3. Enable agent access yourself and use **Test local connection**.
4. Copy the configuration for your host from the app. Restart or reconnect the
   host if its configuration requires it.

The companion is included in the app; no separate CLI download is necessary.
For a read-only local connection check:

```sh
"/Applications/SeZzz.app/Contents/MacOS/sezzzctl" doctor --json
"/Applications/SeZzz.app/Contents/MacOS/sezzzctl" status --json
```

`doctor` does not launch the app, enable access or start a session. If unavailable,
first check that the app is running and agent access is enabled.

For a host accepting a stdio MCP server entry, use:

```json
{
  "command": "/Applications/SeZzz.app/Contents/MacOS/sezzzctl",
  "args": ["mcp"]
}
```

This is a **server entry**, not a universal complete configuration file. Put it
where your host expects server definitions, or use the app's host-specific
preset. Do not use a temporary download or Xcode build path. If you move the app,
update the configured path.

## Safe agent workflow

Ask your agent: “Read SeZzz status. If no session is active, keep my Mac awake in
Background mode for 30 minutes while you work. Do not change an existing session.
When finished, stop only the unchanged session you started.”

Agents should discover capabilities, read status, request an authorized finite
session, retain its session ID and revision, and use those exact values for
updates and cleanup. If the user edits the session, do not fetch a newer revision
just to force a stop. These values prevent stale changes; they are not secret
credentials or proof of agent identity.

There is one shared session, not independent per-agent leases. Closing an MCP
connection does not stop it: its finite deadline still applies. Automated
sessions are limited to seven days; use the shortest useful duration.

Run builds and other commands in the agent's own terminal/executor. The installed
signed companion is sandboxed: its `exec` command is **not a general-purpose
build runner**. Do not weaken macOS security settings to work around restrictions.

## Compatibility

Basic start/extend/stop workflows were tested with Codex desktop and Claude
Desktop on a local pre-release build. This does not certify every host/version.
Claude's initial connection timed out in one test; retry succeeded, and the cause
remains unresolved. Report your host version and exact error if this happens.
The shipped MCP implementation targets protocol version `2025-11-25`.

Disable access in the app when you no longer want agents to control it. Agent
access is local to your Mac, not a remote cloud control service.

# Darwin for Cursor

Search the agentic web and coordinate durable, authorized work through Darwin's production MCP server.

## Local installation

Clone this repository, then install it as a local Cursor plugin using the current **Plugins → Add local plugin** flow. Cursor reads:

- `.cursor-plugin/plugin.json`
- `mcp.json`
- `skills/darwin/SKILL.md`

Complete Darwin authorization in the browser when Cursor connects.

For MCP-only setup, use the [one-click installer](cursor://anysphere.cursor-deeplink/mcp/install?name=darwin&config=eyJ1cmwiOiJodHRwczovL21jcC5kYXJ3aW4uc28vbWNwIn0=).

## Verify

Ask Cursor:

```text
List the Darwin tools. Search for a public PDF text extraction capability, show the evidence and terms, and stop before starting an Action.
```

Expect seven tools: `search`, `start_action`, `get_action`, `list_actions`, `update_action`, `approve_action`, and `stop_action`.

## Review status

This public repository is the complete Cursor Marketplace submission artifact. It is **submission ready**, not submitted or approved. Marketplace submission requires explicit owner confirmation.

## Security

The plugin contains no credentials. OAuth is handled by the Darwin MCP transport. Never add tokens to `mcp.json`, skill text, repository rules, or prompts.


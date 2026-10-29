# Project Desk

Public [Agent Plugins](https://agent-plugins.org) / Cursor plugin for the hosted Project Desk MCP.

This GitHub repo (`atlier-plugin`) is implementation plumbing. The marketplace name is `project-desk`. The product site is [atlier.ai](https://atlier.ai). Do not confuse this bundle with the private `Wildsdesign/Atlier` application repo.

- Publisher: Project Desk
- Plugin: `project-desk`
- MCP server: `projectdesk`
- MCP URL: `https://atlier.ai/mcp`
- Transport: streamable HTTP (declared as `"type": "http"` in `mcp.json`, the value Cursor and other hosts use for remote servers)
- Auth: OAuth 2.1 (no API keys in this plugin)
- Connect guide: [atlier.ai/connect](https://atlier.ai/connect)
- Contract: [atlier.ai/contract](https://atlier.ai/contract)

## Install

Once listed, install **project-desk** from the Cursor Marketplace (Customize → Plugins). Grok Bot uses that same catalog.

Until then, add the hosted connector directly:

- Cursor / Grok Bot: add MCP server URL `https://atlier.ai/mcp`
- Codex: `codex mcp add projectdesk --url https://atlier.ai/mcp`

Then complete OAuth. A successful connection in one host does not prove access in another.

## For agents

After the connector is attached, scan before you write. Call `atlier_project_scan` (no project argument lists desks; project reads need the desk). Agent Queue (`todo`) is unattended-safe work only. Default new tickets to Backlog. See `skills/project-desk/SKILL.md` and the public contract.

## Publish

Cursor Marketplace submissions are a public Git repo plus manual review:

1. Test locally from `~/.cursor/plugins/local/atlier-plugin`
2. Submit this repository at [cursor.com/marketplace/publish](https://cursor.com/marketplace/publish)
3. If review stalls, email marketplace-publishing@cursor.com

Community listing (not the Grok Bot catalog): [cursor.directory/mcp/new](https://cursor.directory/mcp/new)

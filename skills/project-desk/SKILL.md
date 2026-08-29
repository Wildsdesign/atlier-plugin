---
name: project-desk
description: Use this when the Atlier / Project Desk MCP is connected, or when filing, scanning, or updating work on a Project Desk. Scan the live desk before writing tickets.
---

# Project Desk

The project's Shape and queues live on hosted Project Desk, reached through the MCP at `https://atlier.ai/mcp`. This skill does not replace the public contract at https://atlier.ai/contract.

## Rules

- Scan before you write. Call `atlier_project_scan` first. With no project argument it lists desks; project reads and writes need the desk id the scan returned.
- File real work in the moment (`atlier_issue`). Default new items to Backlog.
- Status `todo` is the Agent Queue. Use it only for scoped, unattended-safe, agent-ready work. Do not auto-promote.
- Attention is a concrete human ask, not a status. Hand decisions back with `atlier_handoff`. Parking or backlogging does not clear Attention.
- Close shipped work (`atlier_issue_close`) with what shipped and how you verified it.
- Keep the Shape a story: opening paragraph (Focus), then `## Now` and `## Direction` using those exact headers.
- If Project Desk tools are missing in this chat, say access is unavailable. Do not claim desk state from another host or a remembered URL.

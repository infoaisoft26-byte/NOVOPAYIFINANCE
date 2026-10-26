# Neon Agent Setup

This project includes the official Neon agent skill at `.agents/skills/neon/SKILL.md` and project-level MCP configuration for Cursor (`.cursor/mcp.json`) and Claude Code (`.mcp.json`). The MCP endpoint is Neon's hosted server and uses OAuth on first connection; no API key or database password is stored in this repository.

## Finish setup locally

1. Pull this branch or merge its pull request into your working branch.
2. Open the repository root in your supported coding editor.
3. Restart/reload the editor so it discovers the skill and MCP configuration.
4. When the Neon MCP server prompts, complete the OAuth authorization in the browser.
5. Verify with `neon me` and `neon orgs list` in CMD.
6. Before linking or deploying a database project, confirm the Neon account has access to the intended organization and project. Do not run `neon deploy` until the target project/branch and proposed `neon.ts` policy have been reviewed.

## Current known access blocker

The Neon management connection returned `not an organization member` for organization `org-crimson-queen-67338596`. Successful browser authentication alone does not grant membership in that organization. An organization owner must grant access, or the project must be linked under an organization that the authenticated account can access.

This setup intentionally does not change `.env`, `DATABASE_URL`, Firebase configuration, database schema, or production data.

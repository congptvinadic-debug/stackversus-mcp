# StackVersus MCP server: verified SaaS limits and pricing

Free, read-only, remote [Model Context Protocol](https://modelcontextprotocol.io) server. No API key, no sign-up.

**Endpoint:** `https://getstackversus.com/api/mcp` (streamable HTTP, stateless)
**Docs:** https://getstackversus.com/mcp

Every figure is copied from the vendor's own pricing page, help center or docs, with the source URL, the vendor's wording and the date it was read. Nothing is estimated. Covers 100+ products: AI assistants and coding agents (plan limits per window), LLM APIs ($/1M tokens, rate-limit tiers), voice-agent platforms (per-minute fees), AI video/image credits, search and scraping APIs, scraping platforms and proxies, email platforms, SaaS usage limits, plus a dated change log.

## Connect

Claude Code:

```
claude mcp add --transport http stackversus https://getstackversus.com/api/mcp
```

Cursor, Windsurf, Codex, Claude Desktop and other JSON configs:

```json
{ "mcpServers": { "stackversus": { "url": "https://getstackversus.com/api/mcp" } } }
```

## Tools

| Tool | What it does |
|---|---|
| `search_limits(query, dataset?, limit?)` | keyword search across every plan, limit, rate and gotcha |
| `get_tool(tool_id, dataset?)` | full verified record for one product |
| `compare_tools(tool_ids[])` | 2 to 6 products side by side |
| `recent_changes(days?, tool_id?)` | dated price and limit changes with sources |
| `list_datasets()`, `list_tools(dataset?)` | coverage and ids |

## Also available

JSON and CSV endpoints, RSS for changes and `llms.txt` at https://getstackversus.com/limits. The full bundle as spreadsheets with change history: https://vinadic.gumroad.com/l/saas-limits-dataset

Data: CC BY 4.0 with a link to the source page. The server code lives in the (private) site repository; this repository holds the public `server.json` and docs.

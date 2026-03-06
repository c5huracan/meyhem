# Meyhem

Find the right MCP server for your task. 1,400+ servers indexed and ranked by community trust.

Also: outcome-ranked web search for AI agents across multiple engines.

No API key. No signup. No rate limits.

## MCP Server Discovery

### REST

```bash
curl -X POST https://api.rhdxm.com/find \
  -H 'Content-Type: application/json' \
  -d '{"query": "I need to query a Postgres database", "max_results": 5}'
```

### Python (no dependencies)

```bash
python3 mcp-finder/finder.py "postgres database"
python3 mcp-finder/finder.py "browser automation" -n 3
python3 mcp-finder/finder.py "kubernetes monitoring"
```

### MCP (Claude Desktop, Cursor, etc.)

```json
{"mcpServers": {"meyhem": {"command": "npx", "args": ["mcp-remote", "https://api.rhdxm.com/mcp/"]}}}
```

Tools: `find_server`, `search`, `select`, `outcome`

### OpenClaw

Available on ClawHub as `mcp-finder`, `meyhem-search`, and `meyhem-researcher`.

## Web Search for Agents

```bash
python3 meyhem-search/search.py "python asyncio best practices"
python3 meyhem-researcher/researcher.py "kubernetes networking" -q 5
```

```bash
curl -X POST https://api.rhdxm.com/search \
  -H 'Content-Type: application/json' \
  -d '{"query": "python asyncio best practices", "agent_id": "my-agent", "max_results": 5}'
```

## Example Agents

### Research Agent

```bash
pip install httpx claudette
python example_agent.py 'best practices for error handling in Python async code'
```

### MCP Discovery Agent

```bash
pip install httpx claudette
python mcp_discover.py 'I need to interact with a SQLite database'
```

## Links

- **Try it live:** https://api.rhdxm.com
- **API docs:** https://api.rhdxm.com/docs
- **ClawHub:** mcp-finder / meyhem-search / meyhem-researcher

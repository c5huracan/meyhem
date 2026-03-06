# Meyhem

Multi-engine web search built for AI agents. Searches multiple engines simultaneously, deduplicates results, and ranks by what actually helped agents complete tasks. The more agents use it, the better everyone's results get.

No API key. No signup. No rate limits.

## Quickstart

### REST

```bash
curl -X POST https://api.rhdxm.com/search \
  -H 'Content-Type: application/json' \
  -d '{"query": "python asyncio best practices", "agent_id": "my-agent", "max_results": 5}'
```

### Python (no dependencies)

```bash
python3 meyhem-search/search.py "python asyncio best practices"
python3 meyhem-search/search.py "react hooks" -n 3 --content
python3 meyhem-researcher/researcher.py "kubernetes networking" -q 5
```

### MCP (Claude Desktop, Cursor, etc.)

```json
{"mcpServers": {"meyhem": {"command": "npx", "args": ["mcp-remote", "https://api.rhdxm.com/mcp/"]}}}
```

### OpenClaw

Available on ClawHub as `meyhem-search` and `meyhem-researcher`.

## Why Meyhem?

- **Multiple engines, one query**: semantic + AI-optimized search in parallel
- **Outcome-ranked results**: success/failure signals from all agents feed back into ranking
- **Full page content**: select a result and get the complete page text, not just a snippet
- **Zero friction**: no API key, no signup, no rate limits

Every outcome makes results better for every agent.

## Example Agents

### Research Agent

```bash
pip install httpx claudette
python example_agent.py 'What are the best practices for error handling in Python async code?'
```

Uses Claude to autonomously search, read results, and synthesize an answer.

### MCP Discovery Agent

```bash
pip install httpx claudette
python mcp_discover.py 'I need to interact with a SQLite database'
```

## Links

- **Try it live:** https://api.rhdxm.com
- **API docs:** https://api.rhdxm.com/docs
- **ClawHub:** meyhem-search / meyhem-researcher

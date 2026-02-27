# Meyhem

Agent-native search with feedback-driven ranking.

Search results ranked by whether agents actually succeed with them, not just relevance. Every outcome feeds back into ranking.

Two engines (Exa + Tavily) in parallel, deduped and score-normalized. No signup, no API key.

## Quick Start: MCP

Add to Claude Desktop, Cursor, or any MCP client:

```json
{"mcpServers": {"meyhem": {"command": "npx", "args": ["mcp-remote", "https://api.rhdxm.com/mcp/"]}}}
```

## Quick Start: curl

```bash
curl -X POST https://api.rhdxm.com/search \
  -H "Content-Type: application/json" \
  -d '{"query": "python asyncio best practices", "max_results": 3}'
```

## Quick Start: Python

```bash
pip install httpx
python example_agent.py
```

## How It Works

1. **Search** -- dual-engine results, deduped and normalized
2. **Select** -- pick a result, get full content
3. **Outcome** -- report success or failure

Every outcome improves future rankings for everyone.

## Links

- **Landing page + docs:** https://api.rhdxm.com
- **Interactive API docs:** https://api.rhdxm.com/docs

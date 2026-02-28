# Meyhem

Better search results for your AI tools. The more people use it, the smarter it gets.

No signup. No API key. Just search.

## Quick Start: MCP (10 seconds)

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
pip install httpx claudette
python example_agent.py "What are the best practices for error handling in Python async code?"
```

The example agent uses Claude to autonomously search, read results, and synthesize an answer.

## How It Works

1. **Search** — two engines, one set of best results
2. **Select** — pick a result, get the full page
3. **Outcome** — it learns what works

Every result makes it better: for everyone.

## Links

- **Try it live:** https://api.rhdxm.com
- **Interactive API docs:** https://api.rhdxm.com/docs

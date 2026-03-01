# Meyhem

Smart search for agents, however you build them. The more agents use it, the smarter it gets.

No signup. No API key. Just search.

## Install

```
pip install meyhem
```

## Quickstart

```python
from meyhem import Meyhem

m = Meyhem('my-agent')
res = m.search("Python asyncio best practices")
m.select(res[0])       # tell Meyhem what you picked
m.report(res[0], True) # tell Meyhem if it worked
```

## How It Works

1. **Search** — multiple engines, one set of best results
2. **Select** — pick a result, get the full page
3. **Report** — tell us if it worked

Every outcome makes results better for every agent.

## Also works with

### MCP (Claude Desktop, Cursor, etc.)

```json
{"mcpServers": {"meyhem": {"command": "npx", "args": ["mcp-remote", "https://api.rhdxm.com/mcp/"]}}}
```

### curl

```bash
curl -X POST https://api.rhdxm.com/search \
  -H "Content-Type: application/json" \
  -d '{"query": "python asyncio best practices", "num_results": 3}'
```

## MCP Discovery Agent

Don't know which MCP server you need? The discovery agent finds it for you:

```bash
pip install httpx claudette
python mcp_discover.py "I need to interact with a SQLite database"
```

## Example Research Agent

```bash
pip install httpx claudette
python example_agent.py "What are the best practices for error handling in Python async code?"
```

Uses Claude to autonomously search, read results, and synthesize an answer.

## Links

- **PyPI:** https://pypi.org/project/meyhem/
- **Try it live:** https://api.rhdxm.com
- **API docs:** https://api.rhdxm.com/docs

## Meta-Agent

Describe what you need, get a working agent script:

    pip install meyhem claudette
    python meta_agent.py "monitor GitHub repos and post summaries to Slack"

The meta-agent searches Meyhem for the best tools and libraries, then generates a complete Python script. No MCP required.


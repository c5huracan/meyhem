# Meyhem

Multi-engine web search built for AI agents. Searches multiple engines simultaneously, deduplicates results, and ranks by what actually helped agents complete tasks. The more agents use it, the better everyone's results get.

No API key. No signup. No rate limits.

**700+ searches served** across 490+ domains with outcome data on 100+ URLs.

## Install

```
pip install meyhem
```

## Quickstart

```python
from meyhem import Meyhem

m = Meyhem('my-agent')
res = m.search('Python asyncio best practices')
m.select(res[0])       # pick a result, get the full page
m.report(res[0], True) # report if it helped
```

Every outcome makes results better for every agent.

## Why Meyhem?

- **Multiple engines, one query**: semantic + AI-optimized search in parallel
- **Outcome-ranked results**: success/failure signals from all agents feed back into ranking
- **Full page content**: select a result and get the complete page text, not just a snippet
- **Zero friction**: no API key, no signup, no rate limits

## Also works with

### MCP (Claude Desktop, Cursor, etc.)

```json
{"mcpServers": {"meyhem": {"command": "npx", "args": ["mcp-remote", "https://api.rhdxm.com/mcp/"]}}}
```

### REST

```bash
curl -X POST https://api.rhdxm.com/search \
  -H 'Content-Type: application/json' \
  -d '{"query": "python asyncio best practices", "num_results": 3}'
```

Full API docs: https://api.rhdxm.com/docs

### OpenClaw

Available on ClawHub as `meyhem-search` and `meyhem-researcher`.

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

### Meta-Agent

```bash
pip install meyhem claudette
python meta_agent.py 'monitor GitHub repos and post summaries to Slack'
```

Describe what you need, get a working agent script.

## Links

- **Try it live:** https://api.rhdxm.com
- **API docs:** https://api.rhdxm.com/docs
- **PyPI:** https://pypi.org/project/meyhem/
- **ClawHub:** meyhem-search / meyhem-researcher

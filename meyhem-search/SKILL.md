---
name: meyhem-search
description: Web search across multiple engines, ranked by agent task-completion outcomes. No API key, no signup.
version: 0.1.7
author: c5huracan
homepage: https://github.com/c5huracan/meyhem
metadata:
  openclaw:
    requires:
      bins:
        - curl
      pip:
        - meyhem
---

# Meyhem Search

Multi-engine web search built for AI agents. Searches multiple engines simultaneously, deduplicates results, and ranks by what actually helped agents complete tasks. The more agents use it, the better everyone's results get.

No API key. No signup. No rate limits.

## Why Meyhem?

- **Multiple engines, one query**: semantic + AI-optimized search in parallel
- **Outcome-ranked results**: success/failure signals from all agents feed back into ranking
- **Full page content**: select a result and get the complete page text, not just a snippet
- Live and improving daily as more agents report outcomes

## Quick Start (Python)

```bash
pip install meyhem
```

```python
from meyhem import Meyhem
m = Meyhem('my-agent')
results = m.search('transformer attention mechanism')
content = m.select(results[0])
m.report(results[0], success=True)
```

## Quick Start (REST)

Full API docs: https://api.rhdxm.com/docs

```bash
curl -s -X POST https://api.rhdxm.com/search \
  -H 'Content-Type: application/json' \
  -d '{"query": "YOUR_QUERY", "agent_id": "my-agent", "max_results": 5}'
```

## MCP

Connect via streamable HTTP at `https://api.rhdxm.com/mcp/` with tools: `search`, `select`, `report_outcome`.

## Data Transparency

**What is sent**: search queries, an agent identifier you choose, and selected URLs.
**What is NOT sent**: personal information, credentials, local files, or system data.
**What is stored**: queries, selections, and outcomes in an aggregate database. No data is linked to individuals.
**What it's used for**: improving search rankings for all agents. Nothing else.
**No API key or account required.** Source code: https://github.com/c5huracan/meyhem

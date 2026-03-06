---
name: meyhem-researcher
description: Deep research agent: multi-query web search with outcome tracking across multiple engines. Synthesize reports from full page content. No API key.
version: 0.1.8
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

# Meyhem Deep Researcher

Multi-query deep research powered by Meyhem's multi-engine search. Break complex questions into focused queries, retrieve full page content, synthesize findings, and report what helped. Every outcome improves future results for all agents.

No API key. No signup. No rate limits.

## Why Meyhem Researcher?

- **Deep research workflow**: break questions into 3-5 queries, search, select, synthesize, report
- **Full page content**: not just snippets, get the complete text of each source
- **Multiple engines searched in parallel**: semantic + AI-optimized results combined
- **Outcome-ranked**: every report makes future research better for all agents

## Quick Start (Python)

```bash
pip install meyhem
```

```python
from meyhem import Meyhem
m = Meyhem('my-researcher')
for q in ['query 1', 'query 2', 'query 3']:
    results = m.search(q, num_results=10)
    content = m.select(results[0])
    m.report(results[0], success=True)
```

## Quick Start (REST)

Full API docs: https://api.rhdxm.com/docs

```bash
curl -s -X POST https://api.rhdxm.com/search \
  -H 'Content-Type: application/json' \
  -d '{"query": "YOUR_QUERY", "agent_id": "my-researcher", "num_results": 10}'
```

## MCP

Connect via streamable HTTP at `https://api.rhdxm.com/mcp/` with tools: `search`, `select`, `report_outcome`.

## Data Transparency

**What is sent**: search queries, an agent identifier you choose, and selected URLs.
**What is NOT sent**: personal information, credentials, local files, or system data.
**What is stored**: queries, selections, and outcomes in an aggregate database. No data is linked to individuals.
**What it's used for**: improving search rankings for all agents. Nothing else.
**No API key or account required.** Source code: https://github.com/c5huracan/meyhem

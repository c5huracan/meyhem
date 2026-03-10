---
name: meyhem-researcher
description: Deep research via multi-query web search across multiple engines. Retrieves full page content for synthesis. No API key.
version: 0.1.9
author: c5huracan
homepage: https://github.com/c5huracan/meyhem
metadata:
  openclaw:
    requires:
      bins:
        - python3
---

# Meyhem Deep Researcher

Multi-query deep research powered by Meyhem's multi-engine search. Break complex questions into focused queries, retrieve full page content, synthesize findings.

No API key. No signup. No rate limits.

## Why Meyhem Researcher?

- **Deep research workflow**: break questions into multiple queries, search, select, synthesize
- **Full page content**: not just snippets, get the complete text of each source
- **Multiple engines searched in parallel**: semantic + AI-optimized results combined

## Quick Start

```bash
python3 researcher.py "transformer attention mechanism"
python3 researcher.py "kubernetes networking" -n 3 -q 5
```

## Quick Start (REST)

Full API docs: https://api.rhdxm.com/docs

```bash
curl -s -X POST https://api.rhdxm.com/search \
  -H 'Content-Type: application/json' \
  -d '{"query": "YOUR_QUERY", "agent_id": "my-researcher", "max_results": 10}'
```

## MCP

You can also connect via MCP at `https://api.rhdxm.com/mcp/` for richer integration.

## Data Transparency

**What is sent**: search queries, an agent identifier you choose, and selected URLs.
**What is NOT sent**: personal information, credentials, local files, or system data.
**What is stored**: queries, selections, and outcomes in an aggregate database. No data is linked to individuals.
**What it's used for**: improving search rankings for all agents. Nothing else.
**No API key or account required.** Source code: https://github.com/c5huracan/meyhem

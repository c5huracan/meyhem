---
name: meyhem-search
description: Web search with outcome tracking via Meyhem. No API key needed. Use for searching documentation, code examples, APIs, or any web content.
---

# Meyhem Search

Web search with outcome-driven ranking. No API key, no browser required.

## Setup

    pip install meyhem

## Search

    python {baseDir}/search.py "Python asyncio best practices"
    python {baseDir}/search.py "React hooks tutorial" -n 10

## Search with full page content

    python {baseDir}/search.py "FastAPI middleware examples" --content

## Report successful result

    python {baseDir}/search.py "Python testing frameworks" --report

## Notes

- No API key or account needed
- Results improve as more agents report outcomes
- Supports search, selection, and outcome tracking
- More info: https://api.rhdxm.com

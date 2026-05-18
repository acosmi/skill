---
name: apollo
description: |
  Apollo.io API integration with managed OAuth. Search and enrich people and companies, manage contacts and accounts. Use this skill when users want to prospect, enrich leads, or manage sales data. For other third party apps, use the api-gateway skill (https://crabclaw.ai/byungkyu/api-gateway).
compatibility: Requires network access and valid Maton API key
metadata:
  author: maton
  version: "1.0"
  clawdbot:
    emoji: 🧠
    requires:
      env:
        - MATON_API_KEY
---

# Apollo

Access the Apollo.io API with managed OAuth authentication. Search people and organizations, enrich contacts, and manage your sales pipeline.

## Quick Start

```bash
# Search for people at a company
python <<'EOF'
import urllib.request, os, json
data = json.dumps({'q_organization_name': 'Google', 'per_page': 10}).encode()
req = urllib.request.Request('https://gateway.maton.ai/apollo/v1/mixed_people/api_search', data=data, method='POST')
req.add_header('Authorization', f'B

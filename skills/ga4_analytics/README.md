---
name: ga4-analytics
description: "Google Analytics 4, Search Console, and Indexing API toolkit. Analyze website traffic, page performance, user demographics, real-time visitors, search queries, and SEO metrics. Use when the user asks to: check site traffic, analyze page views, see traffic sources, view user demographics, get real-time visitor data, check search console queries, analyze SEO performance, request URL re-indexing, inspect index status, compare date ranges, check bounce rates, view conversion data, or get e-commerce revenue. Requires a Google Cloud service account with GA4 and Search Console access."
---

# GA4 Analytics Toolkit

## Setup

Install dependencies:

```bash
cd scripts && npm install
```

Configure credentials by creating a `.env` file in the project root:

```
GA4_PROPERTY_ID=123456789
GA4_CLIENT_EMAIL=service-account@project.iam.gserviceaccount.com
GA4_PRIVATE_KEY="-----BEGIN PRIVATE KEY-----\n...\n-----END PRIVATE KEY-----\n"
SEARCH_CONSOLE_SITE_URL=https

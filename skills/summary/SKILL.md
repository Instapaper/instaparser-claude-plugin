---
name: instaparser:summary
description: Generate an AI-powered summary of a web article using the Instaparser Summary API. Use when the user wants a summary or key points from a URL.
user_invocable: true
arguments:
  - name: url
    description: The URL of the article to summarize
    required: true
---

# Instaparser Article Summary

Generate an AI-powered summary with key sentences from a web article using the Instaparser Summary API.

## Instructions

1. Make the API request using curl via the Bash tool:

```bash
curl -s -X POST https://www.instaparser.com/api/1/summary \
  -H "Authorization: Bearer ${user_config.INSTAPARSER_API_KEY}" \
  -H "Content-Type: application/json" \
  -d '{"url": "<URL>"}'
```

3. Present the results clearly:
   - Display the **summary** prominently
   - List the **key sentences** extracted from the article

The Summary API uses **10 credits** per call.

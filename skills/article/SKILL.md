---
name: instaparser:article
description: Extract article content from a URL using the Instaparser Article API. Use when the user wants to parse, extract, or pull the main text from a web article.
user_invocable: true
arguments:
  - name: url
    description: The URL of the article to parse
    required: true
---

# Instaparser Article Extraction

Extract the body text, title, author, and metadata from a web article using the Instaparser Article API.

## Instructions

1. Make the API request using curl via the Bash tool:

```bash
curl -s -X POST https://www.instaparser.com/api/1/article \
  -H "Authorization: Bearer ${user_config.INSTAPARSER_API_KEY}" \
  -H "Content-Type: application/json" \
  -d '{"url": "<URL>"}'
```

Only include `"output"` in the request body if the user explicitly requests a format. Valid values are `text`, `html`, or `markdown`.

3. Present the results clearly:
   - Show the **title**, **author**, **date**, and **word count** as metadata
   - Display the extracted **body text**
   - Mention any images or videos found if relevant

The Article API uses **1 credit** per call.

---
name: instaparser:pdf
description: Extract text content from a PDF using the Instaparser PDF API. Use when the user wants to parse or extract text from a PDF URL or file.
user_invocable: true
arguments:
  - name: source
    description: A URL or local file path of the PDF to parse
    required: true
---

# Instaparser PDF Extraction

Extract text content from a PDF document using the Instaparser PDF API.

## Instructions

1. Determine whether the source is a URL or a local file path, then make the appropriate API request using curl via the Bash tool.

**For a PDF URL**, use the GET method:

```bash
curl -s -G "https://www.instaparser.com/api/1/pdf" \
  -H "Authorization: Bearer ${user_config.INSTAPARSER_API_KEY}" \
  --data-urlencode "url=<URL>"
```

**For a local file**, use the POST method with multipart form-data:

```bash
curl -s -X POST "https://www.instaparser.com/api/1/pdf" \
  -H "Authorization: Bearer ${user_config.INSTAPARSER_API_KEY}" \
  -F "file=@/path/to/file.pdf"
```

Before uploading a local file, verify it exists. Only include the `output` parameter if the user explicitly requests a format. Valid values are `text`, `html`, or `markdown`.

3. Present the results clearly:
   - Show the **title** and **word count** as metadata
   - Display the extracted **body text**

The PDF API uses **5 credits per page**.

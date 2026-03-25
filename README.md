# Instaparser Plugin for Claude

> A Claude plugin that enables article parsing, PDF extraction, and content summarization via the [Instaparser](https://www.instaparser.com) API.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Plugin](https://img.shields.io/badge/Claude-Plugin-blueviolet)](https://www.instaparser.com)

## What It Does

This plugin teaches Claude how to use the Instaparser API to:

- **Parse articles** — Extract title, author, body content, images, and metadata from any web page
- **Parse PDFs** — Extract text and structured content from PDF files (by URL or file upload)
- **Summarize content** — Generate AI-powered summaries with key sentences from any article

## Quick Start

### 1. Get an API Key

Sign up at [instaparser.com](https://www.instaparser.com) and grab your API key.

### 2. Install the Plugin

**Claude Code CLI:**

```bash
claude plugin add instapaper/instaparser-claude-plugin
```

During installation, you'll be prompted to enter your `INSTAPARSER_API_KEY`.

**Manual install:**

Clone or copy this repository, then load it as a local plugin:

```bash
claude --plugin-dir ./instaparser-claude-plugin
```

## Usage Examples

Once installed, use the skill via its namespaced command (`/instaparser:instaparser-api`) or just ask Claude naturally:

| You say | What happens |
|---------|--------------|
| *"Parse this article: https://example.com/post"* | Extracts title, author, body text, images |
| *"Get the text from this PDF: https://example.com/report.pdf"* | Extracts text content from the PDF |
| *"Summarize this article: https://example.com/post"* | Returns a summary and key sentences |
| *"What does this page say? https://example.com/page"* | Parses and presents the article content |

### Example Conversation

```
You: Can you parse this article and give me the key points?
     https://www.example.com/blog/interesting-post

Claude: I'll parse that article using Instaparser...

     "Interesting Post Title"
     By Author Name | Published Jan 15, 2026
     1,247 words

     Here are the key points:
     - Point one from the article...
     - Point two from the article...
     - Point three from the article...
```

## API Endpoints

| Endpoint | Method | Credits | Description |
|----------|--------|---------|-------------|
| `/api/1/article` | POST | 1 | Parse an article from a URL |
| `/api/1/pdf` | GET/POST | 5/page | Parse a PDF from URL or file upload |
| `/api/1/summary` | POST | 10 | Generate an AI summary of an article |

## Project Structure

```
instaparser-claude-plugin/
├── .claude-plugin/
│   └── plugin.json             # Plugin manifest
├── skills/
│   └── instaparser-api/
│       └── SKILL.md            # Skill definition
├── README.md                   # This file
├── LICENSE                     # MIT License
├── CONTRIBUTING.md             # Contribution guidelines
├── CODE_OF_CONDUCT.md          # Community standards
└── CHANGELOG.md                # Version history
```

## Requirements

- An [Instaparser](https://www.instaparser.com) API key
- Claude Desktop, claude.ai, or Claude Code
- `INSTAPARSER_API_KEY` configured via plugin settings or environment variable

## Credits & Pricing

Each API call consumes credits from your Instaparser account:

| API | Credits per Call |
|-----|-----------------|
| Article | 1 credit |
| PDF | 5 credits per page |
| Summary | 10 credits |

Visit [instaparser.com](https://www.instaparser.com) for pricing details.

## Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

## Links

- [Instaparser Website](https://www.instaparser.com)
- [Instaparser API Documentation](https://www.instaparser.com/docs)
- [Report an Issue](https://github.com/instapaper/instaparser-claude-plugin/issues)

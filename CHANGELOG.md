# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.1.0] - 2026-03-25

### Changed

- Restructured project as a Claude plugin
- Added `.claude-plugin/plugin.json` manifest with `userConfig` for API key
- Moved skill definition to `skills/instaparser-api/SKILL.md`
- Removed `marketplace.json` (replaced by plugin manifest)

## [1.0.0] - 2026-03-25

### Added

- Initial release of the Instaparser Claude Skill
- Article parsing via POST `/api/1/article` — extract title, author, body, images, and metadata
- PDF parsing via GET/POST `/api/1/pdf` — parse PDFs by URL or file upload
- Summary generation via POST `/api/1/summary` — AI-powered summaries with key sentences
- Support for HTML and plain text output formats
- Caching support for all endpoints
- Python and JavaScript SDK usage examples
- Comprehensive error handling guidance (400, 401, 403, 409, 412, 429)

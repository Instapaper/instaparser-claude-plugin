# Contributing to Instaparser Claude Plugin

Thank you for your interest in contributing! This guide will help you get started.

## How to Contribute

### Reporting Issues

- Use [GitHub Issues](https://github.com/instapaper/instaparser-claude-plugin/issues) to report bugs or suggest features
- Search existing issues before creating a new one
- Include as much detail as possible: steps to reproduce, expected vs. actual behavior, Claude platform (Desktop, Code, or claude.ai)

### Suggesting Improvements

We welcome suggestions to improve:

- **Skill instructions** — Better prompts, edge case handling, output formatting
- **Documentation** — Clearer explanations, more examples, typo fixes
- **API coverage** — Support for new Instaparser API features

### Submitting Changes

1. **Fork** the repository
2. **Create a branch** from `main`:
   ```bash
   git checkout -b feature/your-improvement
   ```
3. **Make your changes** — keep commits focused and descriptive
4. **Test your changes** — try the skill with Claude to verify it works correctly
5. **Submit a pull request** with a clear description of what changed and why

## Plugin Structure

When contributing, keep in mind the plugin layout:

```
.claude-plugin/plugin.json      # Plugin manifest — update version here for releases
skills/instaparser-api/SKILL.md # Skill definition — main file to edit for API changes
```

When editing `skills/instaparser-api/SKILL.md`:

- Keep the YAML frontmatter (`name` and `description`) accurate and concise
- Ensure all API endpoints, parameters, and response fields are correct
- Include practical `curl` examples that can be copy-pasted
- Write clear instructions in the "Instructions" section — these guide Claude's behavior
- Test with real API calls when possible

## Code of Conduct

This project follows our [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you agree to uphold these standards.

## Questions?

Open an issue or reach out — we're happy to help!

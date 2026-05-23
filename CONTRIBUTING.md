# Contributing to Agent Plugins

Thank you for your interest in contributing! This document outlines the process for contributing to this fork of [awslabs/agent-plugins](https://github.com/awslabs/agent-plugins).

## Getting Started

1. Fork the repository
2. Clone your fork locally
3. Create a new branch for your changes

```bash
git clone https://github.com/your-username/agent-plugins.git
cd agent-plugins
git checkout -b feat/your-feature-name
```

## Plugin Structure

Plugins are registered in one of two marketplace files depending on their target agent:

- `.agents/plugins/marketplace.json` — for general agent plugins
- `.claude-plugin/marketplace.json` — for Claude-specific plugins

### Adding a New Plugin

Each plugin entry should follow this schema:

```json
{
  "id": "unique-plugin-id",
  "name": "Human Readable Name",
  "description": "What this plugin does",
  "version": "1.0.0",
  "author": "your-github-username",
  "tags": ["category", "use-case"],
  "url": "https://github.com/your-org/your-plugin-repo"
}
```

## Code Owners

See [CODEOWNERS](.github/CODEOWNERS) for the list of maintainers responsible for each area of the project.

## Submitting a Pull Request

1. Ensure your plugin entry is valid JSON and follows the schema above
2. Add yourself to `CODEOWNERS` if you are maintaining the plugin
3. Open a PR against the `main` branch with a clear description
4. Fill out the appropriate issue template if applicable

## Reporting Issues

Use one of the issue templates in [`.github/ISSUE_TEMPLATE`](.github/ISSUE_TEMPLATE):

- **Bug Report** — something is broken
- **Feature Request** — you want something new
- **Documentation** — docs need improvement
- **RFC** — proposing a significant change

## Code of Conduct

This project follows the [Amazon Open Source Code of Conduct](https://aws.github.io/code-of-conduct). Please be respectful and constructive in all interactions.

## License

By contributing, you agree that your contributions will be licensed under the same license as this project.

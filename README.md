# Agent Plugins

> A community-maintained fork of [awslabs/agent-plugins](https://github.com/awslabs/agent-plugins) with extended marketplace support.

This repository hosts plugin definitions for AI agents, providing a curated marketplace of tools and integrations that can be loaded by compatible agent runtimes.

## What's in here

- **`.agents/plugins/marketplace.json`** — Plugin definitions for the `.agents` runtime
- **`.claude-plugin/marketplace.json`** — Plugin definitions for Claude-based agents
- **`.claude/settings.json`** — Claude agent configuration

## Getting started

### Using plugins in your agent

Point your agent runtime at the marketplace JSON that matches your setup:

```bash
# For .agents runtime
curl https://raw.githubusercontent.com/your-org/agent-plugins/main/.agents/plugins/marketplace.json

# For Claude agents
curl https://raw.githubusercontent.com/your-org/agent-plugins/main/.claude-plugin/marketplace.json
```

### Adding a new plugin

1. Fork this repo
2. Add your plugin entry to the appropriate `marketplace.json`
3. Open a PR — see [CONTRIBUTING.md](./CONTRIBUTING.md) for the full process

## Plugin schema

Each plugin entry follows this structure:

```json
{
  "id": "unique-plugin-id",
  "name": "Human Readable Name",
  "description": "What this plugin does",
  "version": "1.0.0",
  "author": "your-github-handle",
  "category": "productivity | devtools | data | communication | other",
  "entrypoint": "https://example.com/plugin-manifest.json",
  "tags": ["tag1", "tag2"]
}
```

## Categories

| Category | Description |
|----------|-------------|
| `productivity` | Task management, scheduling, note-taking |
| `devtools` | Code generation, debugging, CI/CD |
| `data` | Databases, analytics, data transformation |
| `communication` | Email, Slack, messaging integrations |
| `other` | Everything else |

## Contributing

We welcome contributions! Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting a PR.

For bugs, use the [bug report template](.github/ISSUE_TEMPLATE/bug_report.yml).  
For new features, use the [feature request template](.github/ISSUE_TEMPLATE/feature_request.yml).  
For larger changes, open an [RFC](.github/ISSUE_TEMPLATE/rfc.yml) first.

## Code owners

See [CODEOWNERS](.github/CODEOWNERS) for who reviews what.

## Personal notes

> This is my personal fork for experimenting with custom plugins. I'm not actively syncing upstream changes — check the [original repo](https://github.com/awslabs/agent-plugins) for the latest official updates.

## License

Apache 2.0 — same as the upstream project.

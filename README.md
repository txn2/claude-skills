# txn2 Claude Skills

A Claude Code marketplace with skills for Go development, verification, and DevOps workflows.

## Installation

Add the marketplace:

```
/plugin marketplace add txn2/claude-skills
```

Then install individual plugins:

```
/plugin install go-verify@txn2-claude-skills
```

## Available Plugins

### go-verify

Audit and scaffold Go projects to [AI-Verified Development](https://imti.co/go-ai-verified-development/) standards.

**What it does:**

- Checks for required config files (`.golangci.yml`, `revive.toml`, `GNUmakefile`, `codecov.yml`, `CLAUDE.md`)
- Reports what's present, missing, or incomplete
- Generates missing configs adapted to your project's module path and structure
- Verifies required tools are installed (golangci-lint, gosec, govulncheck, deadcode, gremlins)
- Optionally runs `make verify`

**Usage:**

```
/go-verify
```

**Reference:** [Go AI-Verified Development: Complete Project Configuration](https://imti.co/go-ai-verified-development/)

## Related Articles

- [Ralph's Uncle: The AI Verification Loop](https://imti.co/ai-verified-development/) - Verification principles
- [Go AI-Verified Development](https://imti.co/go-ai-verified-development/) - Config files and tools
- [GitHub AI Verification](https://imti.co/github-ai-verification/) - CI/CD integration

## License

MIT

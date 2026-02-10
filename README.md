# txn2 Claude Skills

AI on a Leash. A Claude Code marketplace that holds AI-generated code to standards it would never hold itself to.

## Installation

Add the marketplace:

```
/plugin marketplace add txn2/claude-skills
```

Then install individual plugins:

```
/plugin install go-leash@txn2-claude-skills
```

## Available Plugins

### go-leash

Put your Go project's AI on a leash. Audits against strict standards and scaffolds the config files to enforce them.

**What it does:**

- Audits for required config files (`.golangci.yml`, `revive.toml`, `GNUmakefile`, `codecov.yml`, `CLAUDE.md`)
- Reports what's present, missing, or incomplete
- Generates missing configs adapted to your project's module path and structure
- Checks for required tools (golangci-lint, gosec, govulncheck, deadcode, gremlins)
- Runs `make verify` to enforce 43 linters, mutation testing, coverage gates, and security scanning

**Usage:**

```
/go-leash
```

**What gets enforced:**

| Check | Tool | Threshold |
|---|---|---|
| 43 linters | golangci-lint + revive | Zero violations |
| Test coverage | go test | 80% |
| Patch coverage | git diff + go test | 80% of changed lines |
| Mutation testing | gremlins | 60% mutants killed |
| Security | gosec + govulncheck | Clean |
| Dead code | deadcode | Zero unreachable functions |
| Complexity | gocyclo + revive | 10 cyclomatic, 15 cognitive |
| No lint suppression | CLAUDE.md rule | AI must fix, not suppress |

**Reference:** [Go AI-Verified Development](https://imti.co/go-ai-verified-development/)

## License

MIT

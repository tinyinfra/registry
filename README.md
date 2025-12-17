# TinyInfra Expert Registry

This repository contains the expert registry for AI Suite.

## Usage

Add this registry to AI Suite:

1. Open AI Suite Settings
2. Go to Expert Registry section
3. Click the + button to add a source
4. Enter: `https://github.com/tinyinfra/registry`

## Experts

| ID | Name | Description |
|----|------|-------------|
| expert-example | Expert Example | A simple MCP expert with echo, add, and get_time tools for testing |

## Registry Format

The `registry.yaml` file defines available experts:

```yaml
version: 1

experts:
  - id: unique-id
    name: Display Name
    description: What this expert does
    github: owner/repo
    branch: main
    mcp:
      type: local        # or "hosted"
      runtime: python    # or "node"
    skills:              # optional
      - path: skills/my-skill/skill.md
    rules:               # optional
      - path: rules/my-rule.md
    subagents:           # optional
      - path: subagents/my-agent
    tags:
      - category
```

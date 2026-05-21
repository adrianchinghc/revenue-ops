# AGENTS.md

Guidelines for AI agents working in this repository.

## Repository Overview

This repository contains **Agent Skills** for AI agents following the [Agent Skills specification](https://agentskills.io/specification). Skills install to `.agents/skills/` (the cross-agent standard). This repo also serves as a **Claude Code plugin marketplace** via `.claude-plugin/marketplace.json`.

- **Name**: revenue-ops
- **GitHub**: [adrianchinghc/revenue-ops](https://github.com/adrianchinghc/revenue-ops)
- **License**: MIT

## Repository Structure

```
revenue-ops/
├── .claude-plugin/
│   ├── marketplace.json   # Claude Code plugin marketplace manifest
│   └── plugin.json        # Claude Code plugin definition
├── skills/                # Agent Skills (agentskills.io format)
│   ├── lead-researcher/
│   │   └── SKILL.md
│   ├── inquiry-qualifier/
│   │   └── SKILL.md
│   ├── proposal-writer/
│   │   └── SKILL.md
│   └── payment-chaser/
│       └── SKILL.md
├── AGENTS.md
├── CLAUDE.md
├── LICENSE
└── README.md
```

## Skills

| Skill | Description |
|-------|-------------|
| `lead-researcher` | Finds target companies, surfaces contact intelligence, builds multi-touch outreach sequences |
| `inquiry-qualifier` | Scores incoming leads with BANT + psychological read, drafts responses |
| `proposal-writer` | Turns rough briefs into persuasive proposals using Problem→Consequence→Solution→Proof→Commitment |
| `payment-chaser` | Diagnoses non-payment situations and drafts escalating follow-ups |

## Agent Skills Specification

Skills follow the [Agent Skills spec](https://agentskills.io/specification).

### Required Frontmatter

```yaml
---
name: skill-name
description: What this skill does and when to use it.
---
```

## Claude Code Plugin

This repo serves as a plugin marketplace. Install via:

```
/plugin marketplace add adrianchinghc/revenue-ops
/plugin install revenue-ops@revenue-ops
```

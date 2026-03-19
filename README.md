# Prompts

Custom system prompts for LLMs designed for professional software engineering work.

## Overview

This repository contains expert persona prompts for various technical domains. Each prompt defines specialized knowledge, behavioral guidelines, and response standards.

## Available Prompts

### Language & Development
- **go_engineer.md** - Go 1.25+ engineering, concurrency, performance optimization
- **algos.md** - Algorithms, data structures, functional programming in Go

### Infrastructure & Cloud
- **aws.md** - AWS architecture, CLI v2, automation (Bash/Go)
- **k8s.md** - Kubernetes architecture, kubectl, troubleshooting
- **terraform.md** - Terraform >= 1.8, IaC, state management
- **postgres.md** - PostgreSQL query optimization, schema design, operations

### DevOps & Tools
- **git.md** - Git workflows, repository management, best practices
- **vim.md** - Vim/Neovim modal editing, plugins, optimization
- **macos_zsh.md** - macOS ZSH shell configuration and scripting

### Specialized
- **clarity.md** - Technical communication, engineer-to-engineer messaging
- **code-review.md** - Code review best practices and constructive feedback
- **security.md** - Application security, threat modeling, OWASP vulnerabilities
- **observability.md** - Monitoring, logging, tracing, debugging production systems
- **writeup.md** - Convert raw notes into structured technical write-ups (incidents, implementations)
- **tdd.md** - TDD methodology, Tidy First principles

## Usage with Claude Code

Install as custom skills:

```bash
# Create skill directories
mkdir -p ~/.claude/skills/{go-engineer,swe,aws,k8s,terraform,git,vim}

# Symlink desired prompts (example)
ln -s /path/to/prompts/go_engineer.md ~/.claude/skills/go-engineer/SKILL.md
ln -s /path/to/prompts/clarity.md ~/.claude/skills/clarity/SKILL.md
```

Invoke with slash commands: `/go-engineer`, `/clarity`, etc.

## Prompt Structure

All prompts follow a consistent pattern:
- **Frontmatter**: YAML metadata (name, description)
- **Core Focus**: Technical expertise areas
- **Standards**: Code formatting, tool versions, best practices
- **Response Approach**: Tone, structure, explanation style

See [CLAUDE.md](CLAUDE.md) for detailed architecture documentation.
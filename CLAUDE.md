# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This repository contains a collection of custom system prompts for LLMs designed for professional software engineering work. Each prompt file defines a specific expert persona or role with domain expertise, technical standards, and behavioral guidelines.

## Architecture

### Prompt Structure Pattern

All prompts follow a consistent structure:

1. **Role Definition**: Establishes the expert persona (e.g., "Senior Golang Engineer", "Observability Expert")
2. **Core Competencies**: Lists technical expertise areas
3. **Operating/Behavioral Principles**: Defines how the AI should respond
4. **Response Format/Structure**: Specifies output formatting rules
5. **Code Examples Format**: When applicable, includes language-specific standards
6. **Best Practices**: Domain-specific guidance

### Prompt Categories

- **Language-specific**: `go_engineer.md` (Go 1.25+, idiomatic patterns, testing)
- **Platform/Service**: `aws.md` (AWS CLI v2, Bash v5), `k8s.md` (Kubernetes)
- **Infrastructure**: `terraform.md` (IaC)
- **Development Practices**: `tdd.md` (TDD, Tidy First methodology), `clarity.md` (technical communication)
- **Tools**: `vim.md`, `git.md`, `macos_zsh.md`
- **Other Domains**: `algos.md`

## Working with Prompts

### When Creating New Prompts

- Follow the established structure pattern above
- Be specific about tool versions and technical standards (e.g., "Go 1.23+", "AWS CLI v2", "Bash v5")
- Include concrete code example formats with proper syntax highlighting
- Define clear behavioral guidelines for tone and response style
- Avoid generic advice; focus on actionable, domain-specific guidance
- Keep prompts focused on a single domain or role

### When Modifying Existing Prompts

- Preserve the existing structure and formatting
- Maintain consistency with similar prompts (e.g., all language-specific prompts should have similar sections)
- Update version numbers when referencing specific tool versions
- Ensure code examples remain idiomatic for their respective languages/tools

### Key Patterns to Maintain

1. **Tone Specification**: Most prompts specify an expert-level, professional tone (e.g., "mentor-level guidance", "engineer-to-engineer")
2. **Code Standards**: Language-specific prompts include concrete formatting rules (gofmt, code block syntax, etc.)
3. **Response Structure**: Clear templates for how to structure answers
4. **Conciseness**: Emphasis on being concise, actionable, and avoiding fluff

## Special Notes

### clarity.md - Communication Focus

This prompt is unique as it focuses on technical communication rather than code. It emphasizes:
- Engineer-to-engineer tone
- Removing corporate jargon
- Clear ownership and risk communication
- Rewriting Slack messages and emails

### tdd.md - Methodology

This is the most prescriptive prompt, enforcing specific development practices:
- Strict TDD cycle: Red → Green → Refactor
- Separation of structural vs behavioral changes
- Commit discipline (only commit when tests pass)

### Integration-Focused Prompts

Some prompts combine multiple technologies:
- `aws.md`: AWS + Bash scripting + Golang

## No Build System

This repository contains only markdown documentation files. There is no build process, tests, or compilation step.

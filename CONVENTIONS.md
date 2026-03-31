# Agent File Conventions

Follow this spec when adding a new agent file to the repo.

## Frontmatter schema

Every file starts with a YAML frontmatter block:

```yaml
---
name: Human-Readable Agent Name
description: One sentence describing what the agent does.
version: 1.0.0
tags: [tag1, tag2, tag3]
platforms: [claude-code, cursor, codex, copilot, generic]
input: Brief description of what the user provides
output: Brief description of what the agent produces
---
```

Valid `platforms` values: `claude-code`, `cursor`, `codex`, `copilot`, `generic`

## Required sections (in order)

1. Frontmatter block
2. `# Agent Name` — H1 matching the `name` field
3. `## Overview` — 2–3 sentences: what it does, when to reach for it
4. `## System Prompt` — fenced code block containing the literal prompt text
5. `## Usage` — when to invoke, what input to provide, platform-specific notes
6. `## Example Invocation` — at least one realistic copy-paste example

## Naming conventions

- **Files:** `lowercase-with-hyphens.md`
- **Folders:** short single-word category names (`ui`, `code`, `data`, etc.)

## Style rules for system prompts

- Write in imperative second-person: "You are...", "Review...", "Produce..."
- Prompts must be self-contained — no references to external docs or other files
- Always include at least one concrete example with realistic input in the Example Invocation section
- Use fenced code blocks with language tags for all code examples (`tsx`, `css`, `html`, etc.)

## Opinionated agents

If your agent bakes in stylistic preferences (aesthetic taste, naming conventions, architecture opinions), isolate them in a clearly marked block:

```
<!-- ============================================================
     [SECTION NAME] — CUSTOMIZE THIS SECTION
     [One line explaining what this section controls]
     ============================================================ -->

... preference content ...

<!-- END [SECTION NAME] ============================================================ -->
```

This pattern signals to anyone who finds the repo exactly what to change to adapt the agent to their own style.

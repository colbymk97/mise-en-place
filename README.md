# mise-en-place

A collection of reusable AI agent prompts for coding workflows — copy-paste into any platform, no tooling required.

## How to use an agent

Each agent is a self-contained `.md` file. Find the one you want, copy the **System Prompt** block, and load it into your platform of choice:

| Platform | How to load the System Prompt |
|---|---|
| **Claude Code** | Paste into your project's `CLAUDE.md`, or save as a `.claude/agents/` file |
| **Cursor** | Paste into `.cursorrules` or add as a Project Rule |
| **Codex / Copilot** | Paste into custom instructions; provide your input in the chat |
| **Any chat interface** | Paste the System Prompt first, then provide your input in the next message |

Then provide the input described in the agent's **Usage** section.

## Folder structure

| Folder | Contents |
|---|---|
| `code/` | Code quality, refactoring, test generation |
| `planning/` | Idea elaboration, spec generation, project scoping |
| `ui/` | Visual design, layout, and UX review |

## Agent file format

Every agent file contains:

- **YAML frontmatter** — name, description, version, tags, supported platforms, input/output description
- **Overview** — what it does and when to reach for it
- **System Prompt** — the literal prompt text to copy
- **Usage** — what to provide as input, platform-specific notes
- **Example Invocation** — a realistic copy-paste example

Opinionated agents include a **Designer/Reviewer Profile** block inside the System Prompt, clearly marked so you can swap in your own preferences without touching anything else.

## Contributing

See [CONVENTIONS.md](CONVENTIONS.md) for the file format spec.

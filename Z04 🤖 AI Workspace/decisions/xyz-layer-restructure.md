---
date: "2026-09-24"
type: decision
area: vault
status: accepted
---

# Decision

## Decision

Restructured the root folders into a three-letter layer scheme (`X` knowledge substrate, `Y` the user's life, `Z` system and AI workspace): renamed `X02 ⚙️ Zettelkasten/` to `X02 ✍️ My Thinking/`, moved `Y05 ⛓️ Systems/` to `Z05 ⛓️ Systems/`, and added `Y01 💼 Projects/` and `Y02 🌱 Personal/` for the user's actual ongoing life content. `Z04 🤖 AI Workspace/projects/` reverted to its original scope — light AI-written plans, not ongoing real-life work.

## Context

A live test of the project-scoped logging pattern (see [[three-layer-logging-system]]) created a real job-search project inside `Z04 🤖 AI Workspace/projects/`. That revealed a category error: a user's real-life project isn't something the AI "produced" — it's the user's own content the AI is helping with, and it doesn't belong inside a folder named for the AI's own workspace. Separately, "Zettelkasten" is jargon most users don't recognize, and the vault had no dedicated place for personal life content outside thinking, journaling, or a formal project.

## Alternatives considered

- Renaming `X02` to "My Knowledge" — rejected: collides in meaning with "Knowledge Base" (`X03`), which is the opposite kind of content (external, curated) rather than personal thinking.
- Keeping ongoing real-life projects inside `Z04 🤖 AI Workspace/projects/` — rejected per the category error above.

## Consequences

Every reference to `X02 ⚙️ Zettelkasten`, `Y05 ⛓️ Systems`, and the bare word "Zettelkasten" needed updating across the repository, except inside already-existing decision and log entries, which stay as accurate historical record of the state at the time they were written. `architecture.md` gained an explanation of the Zettelkasten method and the Karpathy-inspired Knowledge Base approach, since the folder names no longer carry that context on their own.

## Links

- [[three-layer-logging-system]]
- [[]]

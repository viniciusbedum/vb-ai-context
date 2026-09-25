---
name: vault-setup
description: Configure and personalize a fresh VB AI Context without changing its core My Thinking and Knowledge Base boundaries. Use for first-run setup, user context, editor-neutral preferences, or a setup health check; not for ingesting sources or processing notes.
---

# Vault setup

Set up the repository as a portable local knowledge base. Markdown files and folders remain the source of truth; do not require Obsidian, a server, an MCP, or a specific editor.

## Workflow

1. Inspect the repository map, existing configuration, and current indexes before proposing changes.
2. If this looks like a fresh copy (the fictional examples are still present and no real user notes exist yet), explain the project using the guidance in `## Explaining this project` in `AGENTS.md` before asking anything.
3. Ask only for missing choices that materially affect setup: preferred agent, language, name or alias, and optional Obsidian use. Do not request secrets.
4. Offer to walk the user through the fictional example conversationally: open [[example-promoted-restart-cost]] through [[small-context-packets-make-work-easier-to-resume]] for the My Thinking flow, and `cedar-lane-workshop.md` through [[example-query-context-recovery]] for the Knowledge Base flow, narrating what each file shows instead of listing paths for the user to open alone. Skip this if the user prefers to read [[1 START HERE]] on their own.
5. Offer to fill in the `## Personalize your working style` section at the end of `AGENTS.md`. If the user accepts, ask about tone and communication preferences, relevant domain or project context, and any exception to the behavior guidelines above — then write only what the user actually said into that section. Skip this step entirely if the user declines or has no preference.
6. Put durable user context in a clearly named note under `Z04 🤖 AI Workspace/briefings/`; keep credentials and machine-specific paths out of the repository.
7. Preserve the `X02 ✍️ My Thinking/` and `X03 🗃️ Knowledge Base/` separation, folder names, relative links, and index rules from `AGENTS.md`.
8. Verify that templates, indexes, agent instructions, and chosen editor path are usable. Report optional integrations separately from the working local setup.

If the user only wants a health check, remain read-only. If a tool or editor integration is unavailable, document the manual Markdown workflow rather than installing a dependency or claiming it is configured.

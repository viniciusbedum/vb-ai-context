---
name: vault-translate
description: Translate this template's visible structure (folder names, onboarding guide, index prose) into another language, keeping AGENTS.md/CLAUDE.md/skills in English by default. Use only when the user clearly asks to translate the template, vault, or project structure itself into a target language; never for translating a message, article, or any other one-off piece of text — that's a normal conversational reply, not this skill.
---

# Vault translate

Translate the template's visible structure into another language while keeping the AI's own operating instructions in English by default.

## Confirmation gate

Never run this skill on a first mention, no matter how explicit the request sounds. Ask for the target language and require the user to confirm intent by name — reply with something like: "To start, tell me the language and say 'use vault-translate to translate it to [language]'." Only proceed once the user replies with that explicit invocation.

## Scope

Translate:
- Folder names — only the text portion; keep the `X01`/`Y02`/`Z04` prefix and emoji unchanged (e.g., `X01 📥 Inbox` → `X01 📥 Caixa de Entrada`).
- `README.md`, `CHANGELOG.md`, `🚀 START HERE/` (the onboarding guide and its `docs/`).
- `about-*.md` guides and every index note (title and descriptive prose).
- The fictional walkthrough example's prose (it's pedagogical content for the user, not an operating instruction).
- The prose inside `Z05 ⛓️ Systems/Templates/*.md` (section headings like "Focus", instructional text) — the user fills these in day to day. Keep each template's filename in English; only its content changes.

Never translate:
- Frontmatter keys and values (`type:`, `status:`, `area:`, `tags:`, etc.) — skills and `AGENTS.md` match on these exact strings.
- `AGENTS.md`, `CLAUDE.md`, `.agents/skills/*`, `.claude/skills/*` — only if the user explicitly asks for that too, separately, with a warning that translating operating instructions risks losing precision.
- `README.md`, `CHANGELOG.md`, `LICENSE`, `AGENTS.md`, `CLAUDE.md` filenames themselves — reserved names GitHub, Codex, and Claude Code depend on.

## Workflow

1. Confirm the target language per the confirmation gate above.
2. Build a mapping of every folder and file in scope: current name → translated name. Only rename what you are actually translating.
3. Rename folders and files according to the mapping.
4. Translate the prose inside each file in scope. Leave frontmatter untouched.
5. Update every `[[wikilink]]` across the entire vault that references a renamed file, so nothing breaks.
6. Update the literal path strings inside `AGENTS.md`, `CLAUDE.md`, `.agents/skills/*`, `.claude/skills/*`, and `.obsidian/*.json` that cite a renamed folder or file — a mechanical string swap only, never translate the surrounding instructions themselves.
7. Run a full wikilink and duplicate-basename check across the vault before reporting done; fix anything broken before finishing.

## Language quality

Proceed for any target language the user requests. These languages should translate reliably:

🇧🇷 Portuguese Brazil
🇵🇹 Portuguese
🇪🇸 Spanish
🇫🇷 French
🇩🇪 German
🇮🇹 Italian
🇯🇵 Japanese
🇨🇳 Chinese

For less common languages, say so explicitly and ask the user to review the translated prose before treating the vault as ready — don't silently assume the same quality bar applies everywhere.

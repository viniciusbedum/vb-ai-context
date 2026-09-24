---
type: documentation
status: active
---

# Troubleshooting

## The AI does not see the project instructions

- confirm that you opened the repository root;
- confirm that `AGENTS.md` or `CLAUDE.md` exists at the root;
- start a new session after changing instruction files;
- ask the agent to name the instruction file it read before allowing edits.

## The AI asks for access repeatedly

Permission behavior belongs to the host application, not this vault. Grant access to the project folder through the application's trusted-folder or sandbox controls if you accept the risk. Do not grant broader filesystem access merely to avoid prompts.

## Wikilinks do not open in my editor

Wikilinks place a note name inside double square brackets. Obsidian resolves them natively. In another editor, use file search or install a Markdown extension you trust. The content remains readable without clickable links.

## Obsidian shows an empty or incomplete graph

- open the repository root as the vault;
- verify that notes contain wikilinks;
- check graph filters;
- confirm that index notes link directly to actual notes, not only to sub-indexes.

## A note is missing from an index

Add a direct wikilink to every index that represents a parent scope for that note. For example, a concept belongs in both `concepts-index.md` and the higher `kb-index.md` and `knowledge-base-index.md`.

## A raw source needs correction

Do not overwrite it. Record the correction in the source note, or capture a new version as a separate raw file and link both versions.

## A template update conflicts with my vault

Template repositories and ZIP files do not update automatically. Compare the new release with your copy, back up, and merge only the system changes you understand. Preserve your content and personalized instructions.

## I cannot access a web page or transcript

Use a source you can lawfully access, paste content you are allowed to share, or write a literature note from your own reading or viewing notes. Do not invent missing source text.

## I may have committed a secret

Revoke or rotate it first. Removing the visible file is not enough because Git history may retain it. Follow your Git host's current guidance for history cleanup, then verify the repository from a fresh clone.

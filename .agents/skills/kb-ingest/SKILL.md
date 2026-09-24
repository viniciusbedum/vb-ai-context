---
name: kb-ingest
description: Ingest an external article, paper, video transcript, repository, dataset, or note into the curated Knowledge Base. Use when the user asks to save and connect a source; not for personal My Thinking notes or unsupported summaries of inaccessible content.
---

# Knowledge Base ingest

Create a traceable path from immutable source material to connected wiki notes.

## Workflow

1. Identify the source type and inspect relevant indexes and existing notes for duplicates. Ignore files with `type: system-guide`; they document folders and are not sources.
2. Acquire the actual content. For a URL, use an available web or source tool. For video, use a real transcript provider or user-supplied transcript. If access fails, request a local file or pasted text and stop; never infer the missing source. A URL alone is not a raw source: materialize the retrieved content under `X03 🗃️ Knowledge Base/01 🧱 Raw/` before creating wiki notes.
3. Save new source material under the matching `X03 🗃️ Knowledge Base/01 🧱 Raw/` subfolder. Never overwrite or edit an existing raw source file. If the input is already in `01 🧱 Raw/`, treat it as immutable unless its frontmatter identifies it as a `system-guide`.
4. Create one source note in `X03 🗃️ Knowledge Base/02 🧠 Wiki/sources/` using `Z05 ⛓️ Systems/Templates/source-note.md`. Separate source claims, your synthesis, and operational use. Record enough provenance to locate the source again.
5. Create or update only concepts and entities supported by the source. Use the matching templates and avoid near-duplicate names.
6. Add reciprocal `[[wikilinks]]` where they clarify a real relationship.
7. Update `kb-index.md` and every affected local index with direct links to every real Markdown note below its scope.
8. Append one dated entry to `X03 🗃️ Knowledge Base/02 🧠 Wiki/kb-log.md` listing the source and files created or updated.
9. Verify the raw file exists, links resolve, indexes include the new notes, and no private or machine-specific data was introduced.

Use `Z05 ⛓️ Systems/AI Workflows/multi-agent-knowledge-workflow.md` for dense or contested sources. Without subagents, perform its analyst, cartographer, and reviewer passes sequentially. External services are optional; local files and pasted content are valid inputs.

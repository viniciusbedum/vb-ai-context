---
name: kb-query
description: Answer a question from the local curated Knowledge Base with traceable note references. Use for synthesis, comparison, or retrieval grounded in existing KB content; not when the user wants to ingest a new source or search the whole vault indiscriminately.
---

# Knowledge Base query

Answer from what the vault actually contains.

## Workflow

1. Read `X03 🗃️ Knowledge Base/02 🧠 Wiki/kb-index.md` to map available sources, concepts, and entities.
2. Follow only the relevant indexes and notes. Read linked source notes when a claim needs provenance.
3. Distinguish supported findings, reasonable synthesis, and missing evidence. Do not turn absence in the KB into a general factual claim.
4. Answer directly and cite local evidence with `[[wikilinks]]` to real notes. Mention important disagreements or gaps.
5. Remain read-only unless the user explicitly asks to archive the answer. If archiving is requested, save the minimum useful note in `Z04 🤖 AI Workspace/outputs/` and link its inputs.

If the local KB is insufficient, say what is missing and offer either `$kb-ingest` for a supplied source or a web search when available and authorized. Do not silently replace a KB-grounded answer with unlabelled web knowledge.

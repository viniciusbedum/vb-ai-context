---
type: documentation
status: active
---

# Architecture

## Source of truth

The local folder and its Markdown files are the source of truth. Editors and AI tools are clients of the same files. Obsidian metadata and Git history are helpful layers, not requirements for reading the knowledge.

## Three responsibilities

### Personal thinking: My Thinking

`X01 📥 Inbox/` captures unfinished inputs. `X02 ✍️ My Thinking/` develops them into floating, literature, and permanent notes. Permanent notes should make one useful claim and connect to related notes.

This folder implements the Zettelkasten method — a note-linking system popularized by sociologist Niklas Luhmann, built on small, atomic notes that connect to each other instead of living inside long documents or folders organized by topic. The folder is named "My Thinking" instead of "Zettelkasten" so its purpose is clear without prior knowledge of the method; the underlying practice is the same.

### External knowledge: Knowledge Base

`X03 🗃️ Knowledge Base/01 🧱 Raw/` preserves source material. `X03 🗃️ Knowledge Base/02 🧠 Wiki/` contains structured summaries, concepts, entities, indexes, and the operation log. Raw files are immutable after ingestion; corrections belong in wiki notes or a newly captured source.

This folder follows the approach Andrej Karpathy has described for maintaining a personal, LLM-assisted wiki: preserve sources verbatim, then let an AI agent continuously extract, connect, and update structured notes from them, so the wiki stays current as new sources arrive instead of being written by hand from scratch.

### Operational memory: AI Workspace

`Z04 🤖 AI Workspace/` stores what an AI-assisted session produced or decided: logs, decisions, light project plans, outputs, briefings, and references. It is not a substitute for source notes, permanent notes, or the user's own project files in `Y01 💼 Projects/`.

## Life layer

`Y01 💼 Projects/` and `Y02 🌱 Personal/` hold the user's actual life content — active projects with real, accumulating work, and personal notes that are neither abstract thinking (`X02`) nor a dated journal entry (`X05 📝 Daily Notes/`). `Z05 ⛓️ Systems/` holds templates and operating documentation for the vault itself.

The letter prefix marks the layer: `X` is the knowledge substrate, `Y` is the user's life, `Z` is the system and the AI's own workspace.

## AI layer

Codex or Claude reads project instructions, searches files, follows links, and proposes or performs scoped changes. The default retrieval model is transparent file search plus indexes and links. It can be extended with embeddings or an external RAG service, but that is not required and is not configured by default.

The project should not be described as semantic RAG unless a retrieval pipeline has actually been connected and tested.

## Interface layer

- VS Code, Antigravity, and other editors can be used for everyday file work.
- Obsidian can render wikilinks, backlinks, graph relationships, and Canvas files.
- Git can provide version history and distribution.

None of these interfaces owns the data.

## Index invariant

An index note must link directly to every real Markdown note below the folder it represents. Intermediate indexes remain linked, but they do not replace links to the actual notes. This keeps navigation explicit and prevents notes from becoming disconnected in graph-based tools.

## Boundaries

- My Thinking and Knowledge Base remain separate.
- `promote` is the explicit bridge from a curated concept to the inbox.
- project-relative paths keep the vault portable.
- local secrets and machine-specific settings do not belong in tracked Markdown.

## Related files

- [[workflows]]
- [[privacy]]
- [[multi-agent-workflow]]

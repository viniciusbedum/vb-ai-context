---
type: documentation
status: active
---

# Workflows

## Capture and develop personal thinking

```text
inbox -> floating note or literature note -> permanent note
```

1. capture a thought in `X01 📥 Inbox/` without over-organizing it;
2. decide whether it is your own emerging idea or a response to a source;
3. create a floating note for the former or a literature note for the latter;
4. write a permanent note when one claim can stand on its own;
5. add direct links from every index that covers the new note;
6. remove or archive the inbox capture only when nothing useful would be lost.

See [[example-promoted-restart-cost]], [[restart-friction-after-interruptions]], [[cedar-lane-context-packets-literature-note]], and [[small-context-packets-make-work-easier-to-resume]].

## Ingest an external source

```text
raw source -> source summary -> concepts and entities -> indexes and log
```

1. save a new raw source in the correct `X03 🗃️ Knowledge Base/01 🧱 Raw/` subfolder;
2. do not overwrite an existing raw source;
3. create a structured note in `X03 🗃️ Knowledge Base/02 🧠 Wiki/sources/`;
4. create or update only the concepts and entities supported by the source;
5. connect all notes with wikilinks;
6. update every applicable index;
7. append the operation to `X03 🗃️ Knowledge Base/02 🧠 Wiki/kb-log.md`.

The fictional implementation starts at `X03 🗃️ Knowledge Base/01 🧱 Raw/articles/cedar-lane-workshop.md` and continues through [[cedar-lane-workshop-source]].

For web articles, the optional Obsidian Web Clipper flow can materialize the page directly in `X03 🗃️ Knowledge Base/01 🧱 Raw/articles/`. Follow [[integrations]] to configure the included template and verify the capture before ingestion. The raw file stays unchanged; all enrichment belongs in the wiki.

## Query the Knowledge Base

1. read [[kb-index]] to map available material;
2. open relevant source, concept, and entity notes;
3. distinguish evidence from inference;
4. answer with links to the notes used;
5. offer to save the answer only if it has durable value.

See [[example-query-context-recovery]].

## Promote a concept

Promotion moves a useful idea into the personal thinking process without merging the two systems.

1. select an existing Knowledge Base concept;
2. create a new inbox note that links back to it and its source;
3. phrase the prompt for reflection, not as a copied conclusion;
4. update `inbox-index.md`;
5. let the normal My Thinking process develop the idea.

See [[example-promoted-restart-cost]].

## Lint

Check for:

- Markdown notes missing from a covering index;
- broken wikilinks;
- concepts mentioned repeatedly without their own note;
- contradictions between wiki notes;
- raw files edited after ingestion;
- secrets, personal paths, or private material in tracked files.

## Manual fallback

Every workflow can be completed by creating, moving, linking, and editing Markdown files yourself. If AI access is unavailable, use the templates in `Z05 ⛓️ Systems/Templates/` and apply the same validation checklist.

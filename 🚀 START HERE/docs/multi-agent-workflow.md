---
type: documentation
status: active
---

# Multi-agent workflow

Multiple agents are useful when independent analysis can happen in parallel. They are not required for ordinary note maintenance.

## Safe pattern

```text
source
  |-- source analyst: claims and evidence
  |-- connection mapper: existing concepts and entities
  |-- reviewer: contradictions, privacy, and missing context
  +-- integrator: final writes, links, indexes, and log
```

Only the integrator writes final files. The other agents return bounded findings. This avoids conflicting edits and gives one agent responsibility for link and index integrity.

## Example assignment

For a new article:

1. the source analyst summarizes only what the article supports;
2. the connection mapper searches `X03 🗃️ Knowledge Base/02 🧠 Wiki/` for related notes;
3. the reviewer checks attribution, contradictions, sensitive content, and raw-source handling;
4. the integrator creates or updates notes, then runs the lint checklist in [[workflows]].

## When not to parallelize

Use one agent when the task is small, sequential, or touches the same few files. Coordination costs can exceed the benefit.

## Validation gate

Before accepting a multi-agent result, verify:

- every factual claim traces to a source note or is marked as inference;
- only the intended files changed;
- covering indexes link every real Markdown note;
- raw files were not overwritten;
- no credentials or private content entered the output;
- links resolve in a plain filesystem, not only in one editor.

The specific ability to launch parallel agents depends on the AI environment. If unavailable, run the same roles sequentially in one session.

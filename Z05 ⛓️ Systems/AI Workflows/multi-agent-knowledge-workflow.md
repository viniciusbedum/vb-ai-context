---
type: workflow
status: active
---

# Multi-agent knowledge workflow

Use this workflow when a source or question benefits from independent extraction, connection mapping, and challenge. For small or linear work, one agent should use the relevant skill directly.

## Roles

Run these three roles in parallel when the environment supports subagents. They are read-only and return findings to the orchestrator.

### Analyst

- extract the source's claims, evidence, definitions, and uncertainties
- distinguish source statements from interpretation
- propose concepts and entities without creating files

### Cartographer

- search the existing indexes and relevant notes
- identify links, overlaps, naming collisions, and contradictions
- propose the exact existing notes that new notes should link to

### Reviewer

- test whether the evidence supports the proposed conclusions
- flag unsupported claims, duplicate notes, privacy issues, and missing context
- identify anything that must remain unresolved

## Integration

After all three reports return, one integrator:

1. reconciles disagreements and marks uncertainty explicitly
2. decides the minimum useful set of files
3. performs all writes using the active skill
4. updates direct index links and the operation log where required
5. verifies that every cited source and wikilink exists

Only the integrator writes. Parallel agents never edit vault files, which avoids conflicting changes and partial indexes.

## Fallback

If subagents are unavailable, the primary agent performs the same three read-only passes sequentially, keeps their findings separate, and integrates only after all passes finish. If source access is unavailable, ask for a local file or pasted content. If the work does not need three perspectives, skip this workflow rather than simulating agents.

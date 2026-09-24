---
name: kb-lint
description: Audit the curated Knowledge Base for broken links, orphan notes, incomplete direct indexes, duplicates, contradictions, and missing concept pages. Use for KB maintenance and integrity reports; fixes require an explicit request.
---

# Knowledge Base lint

Audit first. Do not mutate files during a lint-only request.

## Checks

- every `[[wikilink]]` resolves to one real Markdown note without ambiguous duplicate names
- every wiki note has at least one meaningful inbound link, excluding its own index entry only when another relationship exists
- each index directly links every Markdown note below its scope, including notes also reached through child indexes
- source notes point to real raw material and record usable provenance
- concepts and entities mentioned repeatedly have an appropriate page, while trivial mentions do not create noise
- likely duplicates, naming collisions, unsupported claims, and contradictions are surfaced with evidence
- `kb-log.md` contains entries for structural and ingest operations reflected in the wiki

Report findings by severity with exact relative paths and a minimal proposed fix. Do not report empty starter directories as errors.

If the user asks to apply fixes, preserve raw files, change only confirmed issues, update affected indexes, append one lint-fix entry to `kb-log.md`, and rerun the checks. When automated link tooling is unavailable, use repository search and filesystem inspection; disclose any checks that could not be completed.

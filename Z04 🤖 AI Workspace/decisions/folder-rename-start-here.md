---
date: "2026-09-24"
type: decision
area: vault
status: accepted
---

# Decision

## Decision

Renamed `00 📖 Project Guide/` to `🚀 START HERE/`.

## Context

Editors group folders before files, sorted alphabetically. The "00" prefix sorted the guide folder first, far from `README.md`/`LICENSE`/`AGENTS.md`/`CLAUDE.md` at the bottom of the file list. An emoji-first folder name sorts after every plain-letter folder name (higher Unicode codepoint), landing it last among folders — directly above the loose root files.

## Alternatives considered

Moving `1 START HERE.md` and `2 SETUP.md` out to the repo root — rejected in favor of keeping the folder intact and just repositioning it visually.

## Consequences

All literal path references in `README.md` needed updating; wikilinks were unaffected since they resolve by filename, not path.

## Links

- [[]]

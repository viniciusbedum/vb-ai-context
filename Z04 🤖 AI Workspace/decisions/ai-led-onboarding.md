---
date: "2026-09-24"
type: decision
area: workflow
status: accepted
---

# Decision

## Decision

`START HERE`/`SETUP` now lead with connecting the AI agent and running the `vault-setup` skill conversationally, with the static file-by-file walkthrough demoted to an explicit fallback; Obsidian's role was reworded from "optional" to "recommended, not required."

## Context

The manual walkthrough required opening files in a specific order with no folder-structure context up front. Obsidian's Web Clipper is the only smooth capture path for the Knowledge Base, so calling it flatly "optional" was misleading about how the flagship capture flow actually works.

## Alternatives considered

Keep the doc-only onboarding as primary — rejected: higher friction for non-technical users, and it left the AI-driven setup skill under-promoted despite already covering the same ground.

## Consequences

`vault-setup` now explains Zettelkasten vs Knowledge Base and narrates the fictional example before asking setup questions, instead of just answering a couple of preference questions.

## Links

- [[]]

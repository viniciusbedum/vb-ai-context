---
date: "2026-09-24"
type: decision
area: system
status: accepted
---

# Decision

## Decision

Adopted a 4-tier write-permission model in `AGENTS.md` (permanent / create-only / explicit-invocation-only / forbidden-without-ad-hoc-permission), mirroring the author's personal vault's stricter model instead of a single blanket "AI writes wherever it needs to."

## Context

The author's real vault treats every folder outside 3 named exceptions as forbidden without per-conversation permission — notably, its Zettelkasten is not a standing-write folder either. This decision tightens `X02 ⚙️ Zettelkasten/` in the whitelabel to require explicit skill invocation, and formalizes which folders are permanent (`X03 Wiki/`, `Z04 AI Workspace/`) versus ask-first.

## Alternatives considered

A single flat "operating rules" list without tiers — rejected as too coarse to reason about case by case.

## Consequences

The Zettelkasten stays protected from unprompted AI writes; every folder outside the explicit exceptions requires the user's ad-hoc, per-conversation permission, and that permission does not carry over to a new conversation.

## Links

- [[]]

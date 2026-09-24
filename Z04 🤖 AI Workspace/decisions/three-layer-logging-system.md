---
date: "2026-09-24"
type: decision
area: system
status: accepted
---

# Decision

## Decision

Split logging in `Z04 AI Workspace/` into three tiers with different automation levels: vault-wide `logs/`/`decisions/` (automatic, system-level changes only), project-scoped `logs/` (automatic once a project exists, more generous trigger), and an ambient `research/research-log.md` (automatic, silent capture of tool-assisted findings, no project required).

## Context

A live test showed the vault-wide log correctly ignored a one-off LinkedIn job search (correct — not a system change), but that also meant 3 job links found had no home unless the user thought to explicitly say "track this as a project." The gap was real day-to-day usage that's more than trivial but not yet a tracked project.

## Alternatives considered

- Logging every exchange — rejected: noise and bloat over time.
- Always asking "save this?" after every execution — rejected: confirmation fatigue, users tune it out and stop reading the prompt.

## Consequences

Ad-hoc tool findings are never lost even if the user never asks to save them, without inflating the vault-wide system log. When something graduates into an ongoing project, capture moves to that project's own `logs/`.

## Links

- [[]]

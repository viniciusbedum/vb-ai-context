# Changelog

All notable changes to VB AI Context are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [Unreleased]

## [0.2.0] - 2026-09-25

### Added
- `## Explaining this project` in AGENTS.md: explains the Zettelkasten and Karpathy philosophy behind the two knowledge flows, instead of just citing the folder map.
- `vault-translate` skill: translates the template's visible structure (folder names, onboarding guide, index prose, template content) into another language, while keeping AGENTS.md, CLAUDE.md, and the skills themselves in English by default.
- README section for translation support.

### Changed
- `vault-setup` now points to `AGENTS.md`'s "Explaining this project" section instead of repeating a shorter version of it.

## [0.1.0] - 2026-09-24

### Added
- Local-first Markdown knowledge system for Codex and Claude: `My Thinking` (Zettelkasten method) for personal thinking, a curated Knowledge Base (Karpathy-inspired) for external sources, and an AI Workspace that gives agents persistent context across sessions.
- Layered folder structure: `X` folders for the knowledge substrate, `Y` folders for the user's real-life projects and personal notes, `Z` folders for the system and the AI's own workspace.
- Canonical skills (`kb-ingest`, `kb-lint`, `kb-promote`, `kb-query`, `vault-setup`, `zk-process`) with Claude and Codex adapters.
- AI-led onboarding through the `vault-setup` skill, with the `🚀 START HERE` guide as a manual fallback and a fictional walkthrough example.
- A four-tier write-permission model and a three-layer logging system: vault-wide logs and decisions, project-scoped logs, and ambient research capture.
- CC BY-NC-SA 4.0 license: free for personal and professional use, no resale.

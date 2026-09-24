# VB AI Context

VB AI Context is a local-first knowledge system built from plain Markdown files. It combines My Thinking, built on the Zettelkasten method, for developing your own thinking; a curated Knowledge Base, inspired by Karpathy's curation approach, for external sources; and project instructions that let Codex or Claude work with the same context over time.

Context is gold, and that's exactly what this system gives you: real control over your notes and your history, without depending on a single LLM account to keep executing your work.

Have 3 AI accounts and one just ran out of credits? Just connect another one. The history and context are still there, kept in plain `.md` files, ready for any agent to pick up right where the last one left off.

Using it is simple: open the folder in VS Code, Antigravity, another Markdown editor, or a terminal-based workflow. Obsidian is recommended, not required: it renders backlinks, graph navigation, Canvas, and focused reading, and its Web Clipper is the easiest way to capture full articles into the Knowledge Base. Without it, the system still works through plain Markdown and manual capture.

The manual Markdown base requires no server, database, account, or domain. Keep it on your computer, or drop the folder into Google Drive, iCloud Drive, or Dropbox to sync it and get remote access. It's still just files, no server involved. Codex or Claude may require an account, authentication, or a paid plan, depending on the tool and provider.

## Local-first by design

Some AI-powered vault tools connect your notes to external APIs, such as live web research, social feeds, or transcript services, usually through paid keys. VB AI Context takes a different path: everything runs on your own notes, your own captures, and whatever Codex or Claude already read for you in the conversation. No API keys, no recurring cost beyond the AI tool itself.

If live web research or external feeds fit your workflow better, nothing here stops you from adding that yourself. Codex and Claude can already search the web when you simply ask them to. That's a capability of the AI tool itself, not something this template wires in automatically or depends on.

## Start here

1. Read [START HERE](<🚀 START HERE/1 START HERE.md>).
2. Follow [SETUP](<🚀 START HERE/2 SETUP.md>) to connect Codex or Claude.
3. Complete the included fictional walkthrough.
4. Replace the examples only after you understand the two knowledge flows.

To capture complete web articles before running `kb-ingest`, follow the optional [Obsidian Web Clipper setup](<🚀 START HERE/docs/integrations.md#obsidian-web-clipper>). Obsidian is not required for the rest of the system, but Obsidian and its browser extension are required for that capture method.

If your editor does not support wikilinks, open the files directly by path. Every wikilink points to a real Markdown file in this repository.

## What is included

- `X01 📥 Inbox/`: temporary captures and promoted ideas.
- `X02 ✍️ My Thinking/`: floating, literature, and permanent notes.
- `X03 🗃️ Knowledge Base/`: immutable raw sources and an AI-maintained wiki.
- `X04 📎 Attachments/`: local attachments; see [its folder guide](<X04 📎 Attachments/about-x04-attachments.md>).
- `X05 📝 Daily Notes/`: optional daily notes.
- `Y01 💼 Projects/`: your active, ongoing real-life projects.
- `Y02 🌱 Personal/`: personal notes outside thinking, journaling, and active projects.
- `Z04 🤖 AI Workspace/`: AI logs, decisions, research notes, light project plans, outputs, briefings, and references.
- `Z05 ⛓️ Systems/`: templates and system files.
- `🚀 START HERE/`: removable onboarding and documentation, including setup, architecture, workflows, privacy, integrations, plugins, and troubleshooting.

Starter folders contain short, uniquely named `about-*` guides. These guides explain what belongs in each location while also preserving the folder structure in Git and downloaded ZIP files.

## How the tools fit together

```text
local folder + Markdown
          |
          +-- Codex or Claude: context, retrieval, synthesis, maintenance
          |
          +-- everyday editor: VS Code, Antigravity, or another editor
          |
          +-- optional Obsidian: graph, backlinks, Canvas, and study
```

Codex and Claude are alternatives. You only need one. A manual workflow remains available as a fallback, but the intended experience uses an AI agent that can read and edit this folder.

## Documentation

- [Project guide / Start here](<🚀 START HERE/1 START HERE.md>)
- [Setup](<🚀 START HERE/2 SETUP.md>)
- [Architecture](<🚀 START HERE/docs/architecture.md>)
- [Workflows](<🚀 START HERE/docs/workflows.md>)
- [Privacy](<🚀 START HERE/docs/privacy.md>)
- [Integrations](<🚀 START HERE/docs/integrations.md>)
- [Multi-agent workflow](<🚀 START HERE/docs/multi-agent-workflow.md>)
- [Obsidian plugins](<🚀 START HERE/docs/plugins.md>)
- [Troubleshooting](<🚀 START HERE/docs/troubleshooting.md>)

The `🚀 START HERE/` folder contains the guided onboarding and reference docs. It is intentionally removable after setup if you want a quieter working tree; the operational folders and root agent instructions remain usable without it.

## Getting updates

A repository created with GitHub's **Use this template** action is an independent repository. It does not receive future template changes automatically. A downloaded ZIP is also a snapshot.

To update safely:

1. read the release notes or changelog in the source repository;
2. download the new release or add the source repository as a Git remote named `upstream`;
3. compare system files before copying or merging them;
4. back up your vault first;
5. never overwrite your notes blindly.

Updates are intentionally manual because your knowledge files belong to you.

## License

VB AI Context is source-available, not OSI-approved open-source software. The [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International license](LICENSE) covers all repository content.

In short:
- Use, copy, and adapt this material freely for personal or professional work.
- Don't sell it or use it as part of a paid product or service.
- Give credit to the original author.
- Share a modified version under this same license.

This summary is not a substitute for the license itself. See the [human-readable deed](https://creativecommons.org/licenses/by-nc-sa/4.0/) for another short overview.

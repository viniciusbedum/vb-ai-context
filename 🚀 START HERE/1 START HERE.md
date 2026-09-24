---
type: guide
status: active
---

# 🚀 Start here

The guided setup takes about five minutes if your AI agent walks you through it, or fifteen if you read it yourself. The included example uses fictional content, so you can explore the system without adding personal information.

## 1. Open the folder

You already have the folder — from **Use this template** + clone, or from a downloaded ZIP. Open its root (not a subfolder) in VS Code, Antigravity, or any editor that works with folders and Markdown files. No special editor feature is required.

You should see `README.md`, `AGENTS.md`, `CLAUDE.md`, and the numbered folders. If one of the AI instruction files is missing, finish [[2 SETUP]] before continuing.

When you use a shell, wrap any path containing spaces or emoji in quotes, for example: `cd "X03 🗃️ Knowledge Base"`.

## 2. Connect your AI agent and let it guide you

Start Codex or Claude from the repository root and give it access only to this folder. If you don't know how to open a terminal in your editor yet, see [[2 SETUP]].

Ask it to run the setup skill:

> Use vault-setup to configure this vault and walk me through it.

The skill explains the difference between the My Thinking and the Knowledge Base, asks the few setup choices that actually matter (preferred agent, language, whether you'll use Obsidian), and can walk you through the fictional example below conversationally instead of you opening files by hand.

Prefer reading it yourself first? Continue with the steps below — they cover the same ground manually, and you can still ask the agent questions along the way. Try:

> Explain the two knowledge flows in this repository. Do not edit anything.

Then ask:

> Trace the fictional Cedar Lane example from its raw source to its connected notes. Cite the files you used.

The answer should distinguish external knowledge from personal thinking.

## 3. 🗺️ Folder map for the walkthrough

The next two sections open real files. Each item below names the subfolder it lives in — the same name and icon you'll see in your file tree:

```text
X01 📥 Inbox/                    unprocessed captures
X02 ✍️ My Thinking/              your own thinking
  01 ☁️ Floating Notes/          undeveloped ideas
  02 📖 Literature Notes/        ideas tied to a specific source
  03 🗂️ Permanent Notes/         one durable, reusable claim
X03 🗃️ Knowledge Base/           curated external knowledge
  01 🧱 Raw/                     immutable source material
  02 🧠 Wiki/                    sources, concepts, entities
```

The full folder map, including `X04`–`X05`, `Y01`, `Y02`, `Z04`, and `Z05`, is in [[architecture]].

## 4. ✍️ Manual walkthrough: the My Thinking example

Skip this if the setup skill already walked you through it. Otherwise, open these files in order:

1. (`X01 📥 Inbox/`) [[example-promoted-restart-cost]]: an idea waiting in the inbox.
2. (`01 ☁️ Floating Notes/`) [[restart-friction-after-interruptions]]: a quick interpretation.
3. (`02 📖 Literature Notes/`) [[cedar-lane-context-packets-literature-note]]: ideas rewritten from the fictional source.
4. (`03 🗂️ Permanent Notes/`) [[small-context-packets-make-work-easier-to-resume]]: one durable claim.

This is not a mandatory pipeline for every thought. It shows how an initial capture can become an atomic, connected idea.

## 5. 🗃️ Manual walkthrough: the Knowledge Base example

Skip this if the setup skill already walked you through it. Otherwise, open these files in order:

1. `X03 🗃️ Knowledge Base/01 🧱 Raw/articles/cedar-lane-workshop.md`: the preserved fictional source.
2. (`02 🧠 Wiki/sources/`) [[cedar-lane-workshop-source]]: the structured source summary.
3. (`02 🧠 Wiki/concepts/`) [[context-packets]] and [[restart-cost]]: reusable concepts.
4. (`02 🧠 Wiki/entities/`) [[mira-solis]], [[threadmap-cards]], and [[lantern-field-lab]]: fictional entities.
5. (`02 🧠 Wiki/`) [[example-query-context-recovery]]: a sample query result with traceable evidence.

The `promote` step created [[example-promoted-restart-cost]] in the inbox. Promotion copies a useful concept into the personal thinking flow. It does not merge the Knowledge Base and My Thinking.

## 6. 🌐 Optional: capture a real article for the Knowledge Base

The Knowledge Base needs the actual source material before `kb-ingest` can summarize or connect it. The easiest browser workflow uses Obsidian Web Clipper:

1. install Obsidian and open this repository root with **Open folder as vault** at least once;
2. install the official Web Clipper extension for your browser;
3. import `Z05 ⛓️ Systems/Templates/vb-ai-base-article-clipper.json` in the extension settings;
4. open an article you wrote, a public-domain page, or another article you are allowed to save, then select the **VB AI Context - Article** template;
5. confirm that the vault selected in Web Clipper exactly matches the name shown by Obsidian, which may differ if you renamed the folder or extracted it from a ZIP, and that the destination folder is `X03 🗃️ Knowledge Base/01 🧱 Raw/articles`;
6. select **Add to Obsidian**;
7. confirm that a new Markdown file containing the article body exists in `X03 🗃️ Knowledge Base/01 🧱 Raw/articles/`.

Open the vault once so Obsidian recognizes the folder and you can confirm its vault name. Web Clipper sends the capture through Obsidian; the extension can invoke the app, so it normally does not need to be open before every capture. Your browser or operating system may still ask permission to open Obsidian or paste clipboard content.

Do not clean up, summarize, move, or edit the captured file. It is now immutable evidence. Instead, ask your agent:

> Use kb-ingest to process the new article in X03 🗃️ Knowledge Base/01 🧱 Raw/articles. Preserve the raw file unchanged.

Verify that the agent created or updated all five outputs:

- one structured note in `X03 🗃️ Knowledge Base/02 🧠 Wiki/sources/`;
- supported notes in `X03 🗃️ Knowledge Base/02 🧠 Wiki/concepts/`;
- supported notes in `X03 🗃️ Knowledge Base/02 🧠 Wiki/entities/`;
- the applicable indexes, including `kb-index.md`;
- one appended entry in `X03 🗃️ Knowledge Base/02 🧠 Wiki/kb-log.md`.

If you do not want to use Obsidian, save the permitted article body as a Markdown file directly in `X03 🗃️ Knowledge Base/01 🧱 Raw/articles/`. If your agent has web access, you may give it the URL, but it must materialize the retrieved content in `X03 🗃️ Knowledge Base/01 🧱 Raw/articles/` before creating wiki notes. A URL by itself is not the raw source.

Detailed setup, supported browsers, permissions, and troubleshooting are in [[integrations]].

## 7. Make your first personal capture

Create one short note in `X01 📥 Inbox/`. State what caught your attention and why. Do not organize it yet.

Ask your AI agent:

> Review my new inbox note. Suggest whether it should become a floating note, a literature note, a Knowledge Base source, or be discarded. Explain the choice before editing.

## 8. 🕸️ Optional: explore the same folder in Obsidian

In Obsidian, choose **Open folder as vault** and select the repository root. The included `.obsidian` settings use native features only.

Obsidian is optional. It shows the same Markdown files with backlinks and graph navigation; it is not a separate database.

## Next steps

- Check [`CHANGELOG.md`](../CHANGELOG.md) to see what changed since your copy was created.
- Read [[workflows]] before processing real sources.
- Read [[privacy]] before committing or sharing the repository.
- Check [[integrations]] for optional capture tools.
- Use [[troubleshooting]] if links or AI instructions are not detected.

## License

VB AI Context is source-available, not OSI-approved open-source software. The [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International license](../LICENSE) covers all repository content.

CC BY-NC-SA 4.0 permits non-commercial sharing and adaptation, requires attribution, and requires adapted material to be shared under the same terms. It is a content-oriented license, used here for this Markdown-first repository.

---
type: documentation
status: active
---

# Integrations

Integrations are optional capture or retrieval helpers. The Markdown workflows remain the fallback.

## Codex and Claude

Codex reads `AGENTS.md`; Claude reads `CLAUDE.md`. Start the selected agent at the repository root and verify its permission scope with [[2 SETUP]]. Availability, authentication, and exact controls depend on the installed application and plan.

## Obsidian

Open the repository root as a vault. Obsidian reads the same files used by other editors. See [[plugins]] for the minimal configuration.

## Git and GitHub

Git is useful for version history and GitHub is useful for distribution. Neither is required for local use. A GitHub template creates independent repositories and does not provide automatic downstream updates. Use releases, a changelog, or a manually configured `upstream` remote to review changes.

## Obsidian Web Clipper

Obsidian remains optional for VB AI Context. Obsidian and the official Web Clipper browser extension are required only when you choose this capture method.

### What the official integration supports

Web Clipper is available for Chrome and other Chromium-based browsers such as Brave, Arc, Orion, and Vivaldi; Firefox, including Firefox Mobile; Safari on macOS, iOS, and iPadOS; and Microsoft Edge. Install it from the [official Web Clipper page](https://obsidian.md/clipper), not from an unrelated extension listing.

The extension extracts the current page into Markdown. Its footer lets you select a saved vault and destination folder before choosing **Add to Obsidian**. Templates can define the note name, folder, properties, content, and target vault. The official template settings support importing and exporting `.json` files.

### One-time setup

1. install and run Obsidian;
2. choose **Open folder as vault** and select the VB AI Context root folder;
3. confirm the vault name shown by Obsidian;
4. install Web Clipper for your browser from the official page;
5. open the extension and select the settings cog;
6. import `Z05 ⛓️ Systems/Templates/vb-ai-base-article-clipper.json` with **Import**, or drag it into the template area;
7. open **VB AI Context - Article** and select this vault as its default if needed;
8. confirm its note location is `X03 🗃️ Knowledge Base/01 🧱 Raw/articles`.

Opening the folder in Obsidian at least once is a setup requirement for this guide. The official troubleshooting guide requires the vault name in Web Clipper to match the vault name in Obsidian, and Obsidian URIs can target only a known vault by name or ID. Running Obsidian also registers the `obsidian://` protocol on macOS and Windows. The official docs do not phrase this as a universal “open once” rule, so this step is a conservative inference from those documented requirements.

Obsidian does not need to be open before every capture. Selecting **Add to Obsidian** invokes the Obsidian URI workflow and can open or focus the app. This is supported indirectly by the official troubleshooting section for cases where “Obsidian does not open.” A browser or operating system may ask before opening the external application.

### Capture, then ingest

1. open an article you are allowed to retain;
2. open Web Clipper and choose **VB AI Context - Article**;
3. inspect the preview and confirm that the article body is present;
4. confirm the target vault and `X03 🗃️ Knowledge Base/01 🧱 Raw/articles` folder;
5. select **Add to Obsidian**;
6. confirm that the Markdown file exists and contains the captured source;
7. do not edit, enrich, rename, or move that raw file;
8. ask Codex or Claude to use `kb-ingest` on the new file;
9. verify the source note, supported concepts and entities, applicable indexes, `kb-index.md`, and the appended `kb-log.md` entry.

Web Clipper attempts to extract the main content and may omit parts of unusual pages. Inspect the preview before saving. If content is missing, the official troubleshooting guidance suggests selecting the text, using `Cmd/Ctrl+A`, highlighting the desired sections, or creating a site-specific template.

The included template records title, source URL, author, published date, clipped date, `type: article`, and `status: raw`, followed by `{{content}}`. Missing page metadata may produce an empty property; that is preferable to inventing a value. The template does not use Web Clipper Interpreter or an external model.

### Raw-source contract

The captured file is evidence, not a working note. Once saved under `01 🧱 Raw/`, it is immutable. Never add a summary to it, correct its prose, or move it during ingestion. Create the summary, provenance analysis, key points, and operational interpretation separately in `X03 🗃️ Knowledge Base/02 🧠 Wiki/sources/`. Put personal reading notes in the My Thinking.

### Permissions and troubleshooting

Web Clipper passes content from the browser to Obsidian using the clipboard and Obsidian URI workflow. Grant only the browser and operating-system permissions needed for that transfer.

- If nothing is saved, confirm that the vault name matches exactly and that the folder uses the vault-relative path above.
- On Linux, ensure the `obsidian://` URI handler is registered. Clipboard and window-manager permissions may be required, especially under Wayland. Legacy mode is an official fallback, but it may limit capture length.
- On iOS or iPadOS, enable the Safari extension, allow it on the sites you want to capture, and allow Obsidian to paste from other apps.
- Images normally remain remote links. They are not downloaded automatically and may later disappear from the web.

See the official [Web Clipper introduction](https://obsidian.md/help/web-clipper), [capture guide](https://obsidian.md/help/web-clipper/capture), [template guide](https://obsidian.md/help/web-clipper/templates), [variables reference](https://obsidian.md/help/web-clipper/variables), [troubleshooting guide](https://obsidian.md/help/web-clipper/troubleshoot), and [Obsidian URI reference](https://help.obsidian.md/Extending+Obsidian/Obsidian+URI).

### Fallbacks without Web Clipper

- Save a permitted article body as a Markdown file directly in `X03 🗃️ Knowledge Base/01 🧱 Raw/articles/`, then run `kb-ingest`.
- Give the URL to an agent only when it has web access and is authorized to retrieve it. The agent must save the retrieved content under the correct `X03 🗃️ Knowledge Base/01 🧱 Raw/` category before creating any wiki note. A URL alone is not a durable raw source.
- If access fails or the page cannot lawfully be retained, provide pasted text or your own notes. Never fabricate inaccessible content.

## YouTube transcripts

A transcript requires a configured transcript provider or a transcript supplied by the user. Do not assume access, fabricate a transcript, or bypass access restrictions.

Fallback: create a literature note from your own viewing notes and link to the video. If a lawful transcript is available, save it in `X03 🗃️ Knowledge Base/01 🧱 Raw/videos/` before summarizing it.

## External RAG or embeddings

No vector database or embedding index is included. If you add one, document:

- what files are indexed;
- where embeddings and credentials live;
- how deletion and re-indexing work;
- whether data leaves the machine;
- how retrieval quality is tested.

Keep Markdown as the canonical record so the system remains portable if the integration is removed.

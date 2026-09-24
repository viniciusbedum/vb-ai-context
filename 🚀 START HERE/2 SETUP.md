---
type: guide
status: active
---

# Setup

## Requirements

- a local filesystem;
- a Markdown-capable editor;
- Codex or Claude for the intended AI-assisted workflow;
- Git only if you want version history or a private/public GitHub repository;
- Obsidian is recommended (its Web Clipper is the easiest way to capture articles into the Knowledge Base); optional if you'll only capture sources manually.

## Install from GitHub

### Option A: use the template

1. Open the project on GitHub.
2. Select **Use this template**.
3. Create your own repository.
4. Clone it to your computer.

Your repository becomes independent. Template updates do not flow into it automatically.

### Option B: download a ZIP

1. Select **Code** and **Download ZIP**.
2. Extract the archive to a folder you control.
3. Rename the folder if desired.

The ZIP does not include Git history and will not update itself.

## Open the project

Open the repository root, not an individual subfolder, in VS Code, Antigravity, or your preferred editor. Keep filenames and folders intact until you understand how the instructions and wikilinks refer to them.

In shell commands, wrap paths that contain spaces or emoji in quotes, for example: `cd "X03 🗃️ Knowledge Base"`.

No specific Antigravity integration is assumed. It is simply one possible environment for opening and working with the project folder.

## Open a terminal

Both Codex and Claude run from a terminal inside your project folder. VS Code is used here as a concrete example — the same idea applies to Antigravity, another editor's integrated terminal, or your operating system's terminal app.

1. install [VS Code](https://code.visualstudio.com/download) if you don't have it, or use the editor you already opened this folder in;
2. open the repository root in VS Code (**File → Open Folder…**);
3. open its integrated terminal: **Terminal → New Terminal**, or the shortcut `` Ctrl+` `` (Windows/Linux) / `` Cmd+` `` (macOS);
4. confirm the terminal's working directory is the repository root — it should be, since you opened the folder itself;
5. run `codex` or `claude` in that terminal to start a session, depending on which agent you installed.

If you're using a plain terminal app instead of an editor, `cd` into the repository root first, then run the same command.

## Connect Codex

1. from the terminal above, run `codex` — this starts Codex with the repository root as its working directory;
2. confirm that it can read `AGENTS.md`;
3. grant access only to this project folder when your environment asks;
4. ask it to explain the rules before requesting a write operation.

Verification prompt:

> Read the project instructions and list the locations you may edit. Do not change files.

## Connect Claude

1. from the terminal above, run `claude` — this starts Claude from the repository root;
2. confirm that it can read `CLAUDE.md`;
3. grant access only to this project folder when your environment asks;
4. ask it to explain the rules before requesting a write operation.

Verification prompt:

> Read the project instructions and explain how raw sources differ from wiki notes. Do not change files.

Exact controls and permission screens vary by application version. Use the narrowest folder access that still lets the agent work.

## Optional Obsidian setup

1. install Obsidian;
2. choose **Open folder as vault**;
3. select the repository root;
4. review Settings before installing any community plugin.

The included configuration enables a portable native setup. See [[plugins]].

### Optional Web Clipper capture

Web Clipper is the recommended way to bring a complete web article into the Knowledge Base. It is optional for VB AI Context overall, but this capture method requires both Obsidian and the official browser extension.

1. complete the Obsidian setup above so the folder is registered as a vault;
2. install Web Clipper from the official directory for Chrome and Chromium browsers, Firefox, Safari, or Edge;
3. open Web Clipper settings;
4. import `Z05 ⛓️ Systems/Templates/vb-ai-base-article-clipper.json` using **Import**, or drag the JSON file into the template area;
5. open the imported template and set its vault to this vault if **Last used** is not correct;
6. leave its note location as `X03 🗃️ Knowledge Base/01 🧱 Raw/articles`;
7. capture a permitted article and confirm that the resulting Markdown file contains the source body.

The vault dropdown uses the vault name, not its filesystem path. If the folder was renamed after download, choose the name shown by Obsidian. See [[integrations]] for the full capture-to-ingest workflow and manual fallbacks.

## Personalize safely

1. keep the example files until the walkthrough works;
2. create your own notes beside them;
3. update index notes whenever you add or move Markdown files;
4. delete the examples only after removing their links from the indexes;
5. review [[privacy]] before the first commit.

## Updates

Check [`CHANGELOG.md`](../CHANGELOG.md) in the repository root to see what changed between releases. If you use Git, you may add the original repository as an `upstream` remote and compare branches manually. Resolve each change deliberately because upstream system files may overlap with your personalized instructions.

Never treat an upstream merge as a content migration. Back up first.

## License

VB AI Context is source-available, not OSI-approved open-source software. The [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International license](../LICENSE) covers all repository content.

CC BY-NC-SA 4.0 permits non-commercial sharing and adaptation, requires attribution, and requires adapted material to be shared under the same terms. It is a content-oriented license, used here for this Markdown-first repository.

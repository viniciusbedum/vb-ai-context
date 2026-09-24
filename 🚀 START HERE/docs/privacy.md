---
type: documentation
status: active
---

# Privacy

This project is local-first, not automatically private. Privacy depends on where you store, sync, commit, and send its files.

## Before adding content

- decide whether the repository will be public or private;
- understand your editor's sync and telemetry settings;
- review the data policy of any AI provider you connect;
- grant tools access to this folder only;
- keep credentials outside Markdown files.

## Never commit

- API keys, tokens, cookies, or passwords;
- `.env` files or local authentication stores;
- private client, employer, health, financial, or identity data unless you have a deliberate private setup;
- machine-specific workspace state that can reveal recent files or local paths;
- copyrighted source material you do not have permission to redistribute.

`.gitignore` reduces accidental commits but is not a security boundary. A secret committed once can remain in Git history after the visible file is deleted. Revoke exposed credentials and clean history before publishing.

## AI access

An AI agent may read any file within the scope you grant. Inspect proposed changes, keep permissions narrow, and avoid assuming that a local file never leaves your machine. Provider behavior and retention settings can change; verify current official documentation for the tool you use.

## Source handling

Store only material you are allowed to keep. Prefer your own summary and a link when redistribution rights are unclear. The included examples are fictional and may be replaced.

## Public release checklist

- search for names, email addresses, phone numbers, paths, tokens, and URLs with embedded credentials;
- inspect hidden files and Git history;
- remove editor workspace state;
- verify that every example is fictional or licensed;
- open the repository in a fresh folder and follow [[1 START HERE]];
- confirm that no local integration is required to understand the project.

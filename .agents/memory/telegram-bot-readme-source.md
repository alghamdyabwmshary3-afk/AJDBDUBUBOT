---
name: Telegram bot README source quirk
description: A GitHub-imported repo had its entire Python bot source pasted into README.md (with a hardcoded bot token) instead of a proper .py file.
---

Some GitHub imports mislabel their actual source code as README.md — the file had no markdown, just raw Python starting with `import os`. When importing a repo where the only files are README.md and .replit, check README.md's actual content before assuming it's documentation.

**Why:** The repo had zero real project files (no requirements.txt, no .py files) — just README.md containing the full bot implementation, including a hardcoded `BOT_TOKEN` secret committed in plaintext.

**How to apply:** On import, if a repo looks suspiciously empty, read README.md fully — it may contain the real source. Extract it into a proper source file (e.g. `bot.py`), move any hardcoded credentials to Replit Secrets via `requestEnvVar`, and rewrite README.md as normal documentation. Telegram bots using long-polling (pyTelegramBotAPI/telebot) need no web port — configure the workflow with `outputType: "console"` and no `waitForPort`.

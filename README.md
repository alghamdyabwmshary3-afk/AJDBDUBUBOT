# Telegram Media Downloader Bot

A Telegram bot built with `pyTelegramBotAPI` (telebot) and `yt-dlp` that lets users download media (videos/audio) from supported platforms directly through Telegram.

## Features

- SQLite-backed user database (`bot_database.db`)
- Mandatory channel subscription checks
- Daily request rate limiting
- User ranks based on download count
- Daily rewards system
- User feedback system
- Owner/admin broadcast and management commands

## Configuration

The bot reads its configuration from environment variables (managed via Replit Secrets):

- `BOT_TOKEN` — Telegram bot token from [@BotFather](https://t.me/BotFather) (**required**)
- `OWNER_ID` — Telegram numeric user ID of the bot owner/admin (optional, has a default)
- `OWNER_USERNAME` — Telegram username of the bot owner (optional, has a default)

## Running

The bot runs as a background worker (it uses long polling, not a web server):

```
python bot.py
```

This is wired up as the `Telegram Bot` workflow in this Repl.

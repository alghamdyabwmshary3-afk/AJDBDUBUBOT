# Telegram Media Downloader Bot

A Telegram bot built with `pyTelegramBotAPI` and `yt-dlp` that lets users download media (video/audio) from supported platforms directly through Telegram.

## Features

- Media download via yt-dlp (video/audio extraction with ffmpeg)
- SQLite database for users, stats, feedback, notifications, and daily request limits
- Mandatory channel subscription checks
- Daily rewards and user ranking system
- Owner/admin broadcast and management commands

## Tech Stack

- Python 3.11
- `pyTelegramBotAPI` (telebot) for the Telegram Bot API
- `yt-dlp` for media extraction
- `sqlite3` for persistent storage (`bot_database.db`)
- `ffmpeg` for audio extraction

## Configuration

The bot reads sensitive configuration from environment variables (Replit Secrets):

- `BOT_TOKEN` — Telegram bot token from [@BotFather](https://t.me/BotFather)
- `OWNER_ID` (optional) — Telegram user ID of the bot owner/admin
- `OWNER_USERNAME` (optional) — Telegram username of the bot owner

## Running

The bot runs via long polling (no web server/port required):

```bash
python bot.py
```

This is configured as the `Telegram Bot` workflow in this Repl.

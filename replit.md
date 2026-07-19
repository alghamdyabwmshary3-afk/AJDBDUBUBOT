# Telegram Media Downloader Bot

A Telegram bot that lets users download videos and audio from supported platforms (YouTube, Instagram, TikTok, etc.) directly through Telegram.

## Stack

- **Language:** Python 3.11
- **Bot library:** pyTelegramBotAPI (telebot)
- **Media downloader:** yt-dlp
- **Database:** SQLite (`bot_database.db`)

## Running

The bot runs via long polling (no web server). Start it with:

```
python bot.py
```

This is wired up as the **Telegram Bot** workflow in Replit.

## Required Secrets

| Secret | Description |
|--------|-------------|
| `BOT_TOKEN` | Telegram bot token from [@BotFather](https://t.me/BotFather) (**required**) |

## Optional Environment Variables

| Variable | Default | Description |
|----------|---------|-------------|
| `OWNER_ID` | `8539408138` | Telegram numeric user ID of the bot owner |
| `OWNER_USERNAME` | `Mkdkdkd8484849` | Telegram username of the bot owner |

## Features

- SQLite-backed user database
- Mandatory channel subscription checks
- Daily request rate limiting (30 requests/day)
- User ranks based on download count
- Daily rewards system
- User feedback system
- Owner/admin broadcast and management commands

## User Preferences

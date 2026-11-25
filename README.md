# lol-tracker-peufra

> Scheduled bot that checks a League of Legends player's activity with the **Riot API** and roasts them on **Discord** when they stop playing.

## How it works
- Runs on **GitHub Actions** twice a day (cron `0 8,19 * * *`, plus manual `workflow_dispatch`)
- Riot API: Riot ID → PUUID → last match (match-v5) → ranked entries (league-v4)
- Computes days since the last game and picks a morning / evening / long-break message
- Posts a **Discord webhook** message mentioning the player

## Setup
Repository secrets: `RIOT_API_KEY`, `DISCORD_WEBHOOK_URL`. Player Riot ID at the top of `bot.py`.

Python · requests · Riot Games API · GitHub Actions · Discord webhooks

---
Made by [Tom Galvan](https://tomglv.dev) · Bachelor in AI, ECE Paris


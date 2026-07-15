# AterBot

A Minecraft AFK bot that keeps an Aternos server running 24/7 using [mineflayer](https://github.com/PrismarineJS/mineflayer). It exposes a small HTTP endpoint so UptimeRobot can ping it to prevent the Repl from sleeping.

## How to run

The workflow **Start application** runs `pnpm run start`, which starts both the bot and the web server. It starts automatically when the Repl opens.

## Configuration

Edit **`config.json`** before starting:

```json
{
  "client": {
    "host": "yourserver.aternos.me",   // your Aternos server address
    "port": "25565",                    // your server port
    "username": "YourBotName"           // the bot's in-game name
  }
}
```

> **Important:** Your Aternos server must have `online-mode=false` in `server.properties`.

## UptimeRobot setup

1. After the bot is running, copy the Repl's preview URL (shown in the webview tab).
2. Go to [UptimeRobot](https://uptimerobot.com/dashboard) → **Add New Monitor**.
3. Set type to **HTTP(s)**, paste the URL, and save.

This pings the bot every 5 minutes to keep it alive.

## Stack

- **Runtime:** Node.js (tsx for TypeScript)
- **Bot:** mineflayer
- **Package manager:** pnpm

## User preferences

_None recorded yet._

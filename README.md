# openclaw-ocm

A personal, menu-driven one-click manager script for installing and operating OpenClaw.

This repo contains a single script: `ocm.sh`.

## Quick start (one-liner)

```bash
wget -O ocm.sh https://raw.githubusercontent.com/ttbb1211/openclaw-ocm/master/ocm.sh && bash ocm.sh
```

## What it does

- Installs OpenClaw (via `npm -g openclaw@latest`)
- Creates/updates `~/.openclaw/openclaw.json`
- Starts/stops/restarts the OpenClaw Gateway (systemd user service when available)
- Adds and manages model providers (quick presets + custom baseUrl)
- Manages channels (Telegram bot, etc.)
- Includes common utilities: probe health, view gateway logs, list/approve devices, etc.

## Security notes

- **Do not share screenshots** that include API keys, bot tokens, gateway tokens, or Clawhub tokens.
- The "Query Gateway Token" screen is **masked by default**. You can optionally reveal the full token interactively.
- Recommended: keep gateway bind as `loopback (127.0.0.1)` unless you understand the exposure risks.

## Requirements

- Linux with `bash`
- `curl` and `jq` (the script attempts to install them if missing)
- `node` + `npm` (the script installs OpenClaw via npm)

## Repo layout

- `ocm.sh` — main script

## License

Use at your own risk. Review the script before running on production systems.

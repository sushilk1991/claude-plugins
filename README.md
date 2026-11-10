# Masonry plugins

Masonry for coding agents and AI apps: make videos, product photos,
voiceovers and music in your own Masonry workspace from the app you already
use. One server, `https://masonry.so/mcp`, with sign-in on masonry.so the first time a tool
runs.

## Claude Code

```
/plugin marketplace add sushilk1991/claude-plugins
/plugin install masonry@masonry
```

## Cursor

Install **Masonry** from the Cursor Marketplace, or add this repository as a
team marketplace. The plugin adds the server, two skills, a `/masonry`
command and a rule for saving generated media into your project.

## Skills only

The skills in `plugins/masonry/skills/` work in any agent that reads Agent
Skills:

```
gh skill install sushilk1991/claude-plugins --all                         # GitHub CLI, any supported agent
npx skills add sushilk1991/claude-plugins                                 # skills.sh
openclaw skills install @masonry/masonry-get-started  # OpenClaw, from ClawHub
hermes skills install sushilk1991/claude-plugins/plugins/masonry/skills/get-started   # Hermes
```

Skills need the Masonry server connected in that app; `get-started` gives
the one setup step for each app. Every app: https://masonry.so/connect.

## Layout

| Path | For |
|---|---|
| `.claude-plugin/marketplace.json` | Claude Code marketplace |
| `.cursor-plugin/marketplace.json` | Cursor marketplace |
| `plugins/masonry/` | The plugin: manifests for both hosts, skills, Cursor command and rule |
| `hermes/optional-mcps/masonry/` | Entry for Hermes' MCP catalog (submitted upstream) |

This repository is generated from `external/mcp/plugin` in Masonry's backend
by `scripts/sync_marketplace.py`. Changes made here are overwritten.

Support: support@masonry.so

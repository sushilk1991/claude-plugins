# Masonry for Claude Code

```
/plugin marketplace add masonry-so/claude-plugins
/plugin install masonry@masonry
```

Run both inside Claude Code. The first call to a Masonry tool opens
masonry.so in the browser: choose a workspace, select Allow, and you stay
connected until you disconnect in Masonry under Settings, Connected apps.

`masonry-so/claude-plugins` is the proposed GitHub location. If the repository
lives elsewhere, use that `owner/repo` in the first command.

## What you get

- The Masonry MCP server (`https://masonry.so/mcp`): product photos,
  variations, Studio product shoots, short videos, remix and upscale, and a
  gallery of recent creations, all in your own Masonry workspace.
- Two skills:
  - `/masonry:get-started`: connect, make a first image, run a first shoot.
  - `/masonry:product-shoot`: one photo of your product in, four looks to
    choose from, then a matching set of finished photos.

Generations use your workspace's credits.

## Already using Masonry in claude.ai?

A custom connector added in claude.ai also appears in Claude Code. With the
plugin installed too, you have two copies of the same tools; turn one off in
`/mcp`.

## Develop

```
claude plugin validate --strict .
claude plugin validate --strict ./plugins/masonry
claude plugin marketplace add ./      # test from this checkout
```

The skills are copies of `masonry-ai-backend/external/mcp/plugin/skills/`,
which is the source of truth for both this plugin and the ChatGPT/Codex
plugin. After changing them there, copy them here and check:

```
python3 <backend>/external/mcp/plugin/scripts/validate.py --claude-marketplace .
```

Support: support@masonry.so

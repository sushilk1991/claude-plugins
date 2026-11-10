# Masonry

Make videos, product photos, voiceovers and music from Claude Code or Cursor,
saved to your own Masonry workspace. Ask for a short clip, a multi-scene video
joined into one with music, a Studio product shoot from one photo of your
product, or a voiceover, and the finished files come back in the chat.

## Install

In Claude Code:

```
/plugin install masonry --marketplace sushilk1991/claude-plugins
```

In Cursor, install **Masonry** from the Cursor Marketplace.

## What it installs

- The Masonry MCP server at `https://masonry.so/mcp`. Nothing runs on your machine: the
  plugin only points your app at that server.
- Two skills:
  - `get-started`: connect, then make a first video, image and product shoot.
  - `product-shoot`: one photo of your product in, four looks to choose
    from, then a matching set of finished photos.
- In Cursor, a `/masonry` command and a rule for saving generated media into
  your project.

## What it sends and where

The first time a Masonry tool runs, your app opens masonry.so to sign in. You
pick a workspace and select Allow; the app gets an OAuth token for that
workspace only. After that, each tool call sends the prompt, settings and any
image or link you give it to `https://masonry.so/mcp`. Results are stored in your Masonry
workspace and returned to the chat. The connection can't delete anything or
reach other workspaces. Disconnect any time in Masonry under Settings,
Connected apps.

Generations use your workspace's credits. You need a Masonry account; a free
one works for images.

Privacy policy: https://masonry.so/legal/privacy. Terms:
https://masonry.so/legal/terms. Support: support@masonry.so.

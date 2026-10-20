# Kagelot for Claude Code

Direct AI films from Claude Code. Load a [Kagelot](https://kagelot.com) project, direct the next clip in plain words, and watch the Kagelot chat and canvas update live.

## Install

In Claude Code:

```
/plugin marketplace add Fahd26indo/kagelot-claude-plugin
/plugin install kagelot@kagelot
```

Claude Code asks for your Kagelot key. Get it in Kagelot: **Connect** tab → **Activate MCP access** (any paid plan). The key is stored in your system's secure storage, not in a settings file.

Restart Claude Code and type `/mcp`: **kagelot** shows as connected.

## Use

```
/kagelot:load https://kagelot.com/project/<your-project-id>
/kagelot:next-clip she opens the door and the room is full of birds
```

Or just talk: "load this project <link>", "direct the next clip".

Images and videos are never made from your terminal. They appear as cards in your Kagelot chat, and you click **Generate** or **Render** there.

## Cost

Reading and writing your project is free. `direct_clip` and `write_screenplay` cost 1 Kagelot credit each. The rest of the thinking runs on your own Claude subscription.

Full guide and tutorial video: https://kagelot.com/mcp · Support: support@kagelot.com

# Setup

Your second brain is one folder, used by two apps. **Claude Code** maintains it. **Obsidian** lets you see
it. You install those two apps once; Claude does everything in between, from one URL.

## What you need

- **Claude Code** - the agent that builds and maintains your brain. Needs a Claude subscription (Pro is
  about $20/month and includes Claude Code; there is no free tier). Install it from Anthropic.
- **Obsidian** - free. This is how you see and walk your brain: the wiki, the links, the graph. obsidian.md
- **git** - free. Used to download and version your brain. It comes with most systems; git-scm.com if not.

Claude Code cannot install these for you (they are apps, and one needs a subscription). Everything after
this, it can.

## Set up from scratch

Pick the line that matches what you already have, then do "The setup" below.

- **You have nothing.** Install Claude Code and Obsidian.
- **You have Claude Code but not Obsidian.** Install Obsidian.
- **You have Obsidian but not Claude Code.** Install Claude Code. Your brain needs the agent; Obsidian alone
  is just a viewer.

### The setup (same for everyone)

1. Open Claude Code. Paste this and say **"set up my second brain"**:
   `https://github.com/Krishna-kai/claude-second-brain`
   Claude clones it (or builds it for you) and tells you it is ready. There is nothing to configure.
2. Open that same folder in Obsidian: **File -> Open folder as vault**, and pick it. Now you can browse your
   wiki, follow links, and see the graph.
3. Drop a source into `raw/` (a reading, a PDF, your notes) and say **"read what is in raw and start my
   wiki."** Or just ask Claude a question.

That is it. Claude works the brain; you watch it grow in Obsidian.

## Does it work without one of them?

- **Without Obsidian:** yes, but you lose the nice view. Claude still maintains everything, and the files
  are plain markdown you can read in any editor.
- **Without Claude Code:** no, not as a second brain. The agent is what reads your sources and maintains the
  wiki; Obsidian cannot do that. The markdown files are still yours, just not self-maintaining.

## Later: deeper web search (optional)

The `research` and `deep-search` skills work out of the box with Claude's built-in web search. If you want
deeper, multi-source research, you can add a search tool (Tavily has a free tier) as an MCP server, and run
MCP tools in Docker. That is a separate, optional step covered in `skills/README.md`. You do not need it to
start.

# Second Brain

A second brain for your work, built with Claude Code. You collect sources and notes; Claude reads them and
keeps a living, linked wiki of what they say, the projects you are working on, and the people you work
with, so it remembers and gets sharper as you go.

It is skills-first. Use Claude's built-in skills, or build your own with `skill-creator`. A small contract,
`CLOTH.md`, means Claude loads only the one skill and the few pages a task needs, never the whole brain, so
it stays fast and uncluttered however big it grows.

You are the architect, asking the questions and deciding what matters. Claude does the reading, linking,
and filing. Good for studying, research, or any work where you want your agent to remember.

## Start

**What you need:** Claude Code (the agent, a Claude subscription) and Obsidian (the viewer, free). If you
already have one of them, or want the full walkthrough, see [SETUP.md](SETUP.md).

1. In Claude Code, paste this and say **"set up my second brain"**:
   `https://github.com/Krishna-kai/claude-skills-second-brain`
   Claude clones it (or builds it for you) and tells you it is ready. Nothing to configure.
2. Open that same folder in Obsidian (**File -> Open folder as vault**) to see your wiki and its graph.
3. Drop a source into `raw/` (a reading, a PDF, your notes) and say **"read what is in raw and start my
   wiki."** Then ask it questions, say "add this" as you collect more, or "lint my wiki" to tidy up.

Claude maintains the brain; Obsidian is your window into it. Plain markdown, yours, no lock-in.

## Credit

We did not invent this. We borrowed brilliance from the open source community and built on it.

- The wiki pattern (raw sources, an LLM-built wiki, an index) is **Andrej Karpathy's "LLM Wiki"**:
  https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f
- The idea of turning Claude Code itself into a second brain, a schema file that makes the agent a
  disciplined maintainer, is **Cole Medin's** work at Dynamous AI:
  https://github.com/coleam00/second-brain-skills
- The pattern of an agent that reads who it is and how to behave before it acts comes from the
  **soul.md and OpenClaw community** (Aaron Mars): https://github.com/aaronjmars/soul.md
- `CLOTH.md` builds on the field's idea of progressive disclosure and context engineering. The named
  contract is ours. The idea is not.

Plain markdown. No database, no lock-in. Your brain, your files.

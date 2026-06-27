# Second Brain

A second brain you build with Claude Code. You collect sources, Claude reads them and keeps a living,
linked wiki of what they say, so it remembers and gets sharper as you go. It works for studying, research,
or any learning work.

## Start

1. Install Claude Code (it needs a Claude subscription).
2. Get this folder and open it in Claude Code:
   `git clone https://github.com/Krishna-kai/claude-second-brain my-brain`
3. Drop a few sources into `raw/` (lecture notes, an article, a PDF, your own rough notes).
4. Say: **"read what is in raw and start my wiki."** Then ask it questions, or say "add this" as you
   collect more. To tidy up later, say "lint my wiki."

Claude builds the wiki in `wiki/`, keeps an index, and remembers between sessions. You collect and ask; it
does the reading, linking, and bookkeeping.

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

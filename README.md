# Second Brain

An open, local AI second brain you run with Claude Code and Obsidian. You collect your sources; Claude reads
them and keeps a living, linked wiki of what they say, the projects you're working on, and the people you
work with, so it remembers and gets sharper as you go. Good for research, consulting, or any work where you
want your agent to remember. Plain markdown, yours, no lock-in.

*Sharing this with a colleague? A one-page overview to hand on is in [docs/QUICKSTART.md](docs/QUICKSTART.md).*

## Start (about five minutes)

You need **Claude Code** (the agent, needs a Claude subscription) and **Obsidian** (the viewer, free). New
to either, or want the per-situation walkthrough? See [SETUP.md](SETUP.md).

1. **Make a new, empty folder** for your brain and open Claude Code in it. (A fresh folder keeps things tidy
   and lets setup run cleanly.)
2. **Paste this and say "set up my second brain":**
   > https://github.com/Krishna-kai/claude-skills-second-brain
   Claude clones the kit into your folder and tells you it's ready. Nothing to configure.
3. **Open that same folder in Obsidian** (File -> Open folder as vault) to see your wiki and its graph.
4. **Drop a source into `raw/`** (a reading, a PDF, your notes) and say **"read what's in raw and start my
   wiki."** Then ask questions, say "add this" as you collect more, or "lint my wiki" to tidy up.

Claude maintains the brain; Obsidian is your window into it.

> **If you're the Claude agent reading this:** the user wants their second brain set up. Your first action
> is to run exactly this in their current folder:
> ```
> git clone https://github.com/Krishna-kai/claude-skills-second-brain.git . && ls
> ```
> The trailing `.` clones into this folder, not a subfolder. If the folder isn't empty, ask the user to open
> you in a new empty folder first. Then read `CLAUDE.md` and follow its "If you were just pointed here" setup.

## How it works

It's skills-first. Use Claude's built-in skills, or build your own with `skill-creator`. A small contract,
`CLOTH.md`, means Claude loads only the one skill and the few pages a task needs, never the whole brain, so
it stays fast and uncluttered however big it grows.

You're the architect, asking the questions and deciding what matters. Claude does the reading, linking, and
filing, the part that makes people abandon their notes.

## Credit

We didn't invent this. We borrowed brilliance from the open source community and built on it.

- The wiki pattern (raw sources, an LLM-built wiki, an index) is **Andrej Karpathy's "LLM Wiki"**:
  https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f
- The idea of turning Claude Code itself into a second brain, a schema file that makes the agent a
  disciplined maintainer, is **Cole Medin's** work at Dynamous AI:
  https://github.com/coleam00/second-brain-skills
- The pattern of an agent that reads who it is and how to behave before it acts comes from the
  **soul.md and OpenClaw community** (Aaron Mars): https://github.com/aaronjmars/soul.md
- `CLOTH.md` builds on the field's idea of progressive disclosure and context engineering. The named
  contract is ours. The idea isn't.

Plain markdown. No database, no lock-in. Your brain, your files.

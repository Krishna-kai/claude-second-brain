# Second Brain: a quickstart for research and knowledge work

*An open, local AI second brain you run with Claude Code and Obsidian. For researchers, professors, and
consultants, anyone who accumulates sources and has to remember and synthesise across a body of work.*

## What it is

Your AI assistant forgets everything between sessions. This gives it a memory. You collect your sources, the
papers, reports, notes, and transcripts you already work with, and Claude reads them and maintains a living,
linked wiki of what they say, the projects you're running, and the people you work with. It reads that
before it acts, and keeps it current as you go.

You're the architect: you decide what matters and ask the questions. Claude does the reading, linking, and
filing, the part that makes people abandon their notes. The result is a knowledge base that compounds
instead of scattering across chats. Plain markdown you own. No database, no lock-in.

## What you need

- **Claude Code** - the agent that builds and maintains the brain. Needs a Claude subscription (about
  $20/month; there's no free tier).
- **Obsidian** - free. Your window into the brain: the wiki, the links, the graph. obsidian.md
- **git** - free, for the download and version history. It comes with most systems.

Claude can't install these for you. Everything after this, it does.

## Set up (about five minutes)

1. Install Claude Code and Obsidian.
2. Make a new, empty folder for your brain and open Claude Code in it.
3. Paste this and say **"set up my second brain"**:
   `https://github.com/Krishna-kai/claude-skills-second-brain`
   Claude clones the kit into your folder and confirms it's ready. Nothing to configure.
4. Open that same folder in Obsidian: **File -> Open folder as vault**. Now you can browse it and see the graph.
5. Drop a source into `raw/` and say **"read what's in raw and start my wiki."** Or just ask a question.

## What it does for your work

- **Ingest.** Drop in papers, PDFs, notes, transcripts. Claude reads them and writes linked wiki pages, with
  an index it keeps current.
- **Ask.** It answers from your own corpus, tells you which pages it used, and saves good answers back so
  they compound instead of vanishing into chat.
- **Research and deep-search.** A thorough, current, multi-source sweep on a topic, saved into your wiki with
  every source cited and dated. Works for any field.
- **Report.** Turns what's in your brain into a clear, sourced write-up you can hand on.
- **Remembers your world.** A short profile (`SOUL.md`) holds who you are, who you work with, and how you
  like to work, so it's useful from the first session.
- **Your own skills.** Use the built-in workflows, or say "make me a skill that does X" and it writes one.
- **Stays fast as it grows.** A small loading contract (`CLOTH.md`) means Claude reads only what a task
  needs, so a brain of a thousand pages costs the same attention as one of ten.

## Going deeper (optional)

For broader, fresher research, you can connect a dedicated web-search tool through Docker's MCP hub. Tavily's
free tier gives 1,000 searches a month with no card, and 4,000 a month for four months if you're a student
([Tavily's credit docs](https://docs.tavily.com/documentation/api-credits)). The `deep-search` workflow then
uses it automatically. The steps are in `docs/deeper-search.md`. You don't need it to start.

## Honest notes

- **Claude does the work; Obsidian is the view.** Without Claude the files are still yours and readable in
  any editor; they just stop self-maintaining. Without Obsidian you lose the graph, nothing else.
- **Built on the community, credited.** The wiki pattern is Andrej Karpathy's; the idea of Claude Code as a
  second brain is Cole Medin's; reading who-you-are before acting is the soul.md community's. The loading
  contract, CLOTH, is the one piece we added. Open source, MIT.

Repo: https://github.com/Krishna-kai/claude-skills-second-brain

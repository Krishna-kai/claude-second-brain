# This is a second brain (an LLM wiki)

This folder is a second brain you build with Claude. It follows Andrej Karpathy's LLM Wiki pattern: the
human collects sources, and you (the LLM) read them and maintain a living, linked wiki of what they say.
It works for studying, research, or any work where you keep learning.

You own the wiki. The human collects and asks. You read, summarise, link, and keep it tidy. The human
should rarely have to write a wiki page themselves.

## The three parts

- `raw/` - sources the human drops in (readings, notes, papers, links). You read these. You never change
  them. They are immutable.
- `wiki/` - the pages YOU write, in plain markdown, linked with `[[page-name]]`. Make a page for something
  only when two or more other pages would want to link to it; otherwise keep it inline in a page that
  mentions it. Do not make a page per noun. `wiki/index.md` is your catalog of every page with a one-line
  summary. Keep it current.
- `log.md` - an append-only history. Add a line each time you ingest a source, save an answer, or lint.

How to load all this as it grows is its own short contract: see `CLOTH.md`. Short version: read
`wiki/index.md` first, then open only the pages you need. Never load the whole wiki at once.

## What to do

**When the human adds a source (ingest).** Read it. Update or create the wiki pages it touches; one source
often touches several. Note where it agrees with or contradicts what is already there. Update `index.md`,
add a line to `log.md`.

**When the human asks a question (query).** Read `index.md`, open the relevant pages, answer, and say which
pages you used. If the answer is worth keeping (a comparison, a summary, a connection you found), save it
as a wiki page so it compounds instead of vanishing into chat. Log it.

**When the human asks you to tidy up (lint).** Check the wiki for contradictions, stale pages, orphan pages
with nothing linking to them, important things mentioned but missing their own page, and missing links.
Fix what you can, list what needs a human. Log it.

Keep it plain. Markdown a human can read. Do not build structure nobody asked for.

## Skills

Beyond the core workflows, `skills/` holds extra named workflows, one markdown file each. Two ship:
`research` (deep, multi-source research saved into the wiki) and `report` (turn the wiki into a sourced
report). When the human asks for one by name, or asks for something a skill fits, read that skill file and
follow its steps. The human can add their own; see `skills/README.md`.

## Credit

We build on each other. The wiki pattern is Andrej Karpathy's "LLM Wiki". The idea of Claude Code as a
second brain maintained from a schema file is Cole Medin's (second-brain-skills). The pattern of an agent
reading who it is before it acts is the soul.md and OpenClaw community's. `CLOTH.md` is ours, built on the
field's progressive disclosure. Full links and credit are in the README.

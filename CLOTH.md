# CLOTH - how to load this brain as it grows

CLOTH is a context-loading contract. As the wiki grows past what fits in one context window, this is how
you decide what to read, so a big brain costs you the same attention as a small one.

- **Always read first:** this file, `CLAUDE.md`, and `wiki/index.md`. They are small and they are the map.
- **Load on demand:** only the wiki pages the current question needs (use `index.md` to find them by name,
  then open two or three, not twenty), and only the one skill a task calls for, read from `skills/` when
  you need it.
- **Do not load by default:** the whole `wiki/` folder, the whole `raw/` folder, `log.md`, or every file in
  `skills/`. Skills especially: read the one you need, not all of them, or you bloat the context for
  nothing. Search and open specific files instead.

The rule: **find before you read.** The index is the map; the pages are the territory. Read the map, then
walk only where you need to.

This is the piece we add on top of the LLM Wiki pattern. The wiki keeps your knowledge; CLOTH keeps it
fast to use no matter how big it gets.

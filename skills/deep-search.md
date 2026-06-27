# Skill: deep-search

A thorough, current-information sweep on a topic, pulling from several sources, not just one quick search.

Use this when the human wants the latest on something, or a careful answer that a single search would miss.
It works for any domain: science, law, finance, history, a product, a person, a current event.

This is bespoke on purpose. It orchestrates several search angles, several sources, and your own wiki,
rather than leaning on one generic search.

## Steps

1. **Frame the query into angles.** Turn the topic into three to five specific angles, not one. For example:
   the definition, the latest developments, the opposing view, primary sources, the numbers and dates.
   Different angles catch what a single query misses.
2. **Look local first.** Read `wiki/index.md` and open any pages on the topic. Note what the brain already
   holds and what is missing. Do not re-search what you already know.
3. **Search wide.** Run each angle through your web search. If a search MCP is set up (Tavily or similar,
   see `skills/README.md`), use it as well for fresher, deeper coverage; if its tools are not visible in
   your tool list, check your tool registry and load them before deciding none is set up. Pull from several
   sources.
4. **Check freshness and agreement.** Prefer recent, primary, and reputable sources. Note where sources
   disagree or where information looks dated. Say how current your answer is.
5. **Synthesise and save.** Write the findings into the wiki as a page, every source cited (title, link, and
   the date you searched). Note the angles you searched, so the next sweep can refine them instead of
   starting over. Then follow the saving rule in `CLAUDE.md`: into `wiki/index.md`, a `log.md` line, and
   linked from at least one existing page so it is not an orphan.

The difference from a quick search: several angles, several sources, your own wiki, freshness checked, and
the result saved so it compounds.

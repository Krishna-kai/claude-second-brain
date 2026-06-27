# skills/

Skills are extra, repeatable workflows on top of the core wiki workflows (ingest, query, lint). Each one
is a short markdown file the agent follows when you ask for it.

Four ship with the kit:

- `research.md` - investigate a topic across sources and write the findings into the wiki.
- `deep-search.md` - a thorough, current-information sweep: several angles, several sources, plus your wiki,
  freshness checked. For "what is the latest on X." Works for any domain.
- `report.md` - turn the wiki into a clear, sourced report.
- `skill-creator.md` - make a new skill for a task you repeat.

You can add your own. Just say "make me a skill that does X" and the `skill-creator` skill writes a new one
here. A skill is a short markdown file named for the task, with a few steps.

(This "skills for Claude Code" idea is Cole Medin's, from second-brain-skills. See the README credits.)

## Optional: deeper web search

The `research` skill works out of the box with Claude Code's built-in web search. No setup.

If you want deeper, fresher, multi-source research, add a web-search MCP server so Claude can run real
search queries:

1. **Get a free search API key.** In 2026 the simplest free option is **Tavily**: 1,000 searches a month,
   no credit card (tavily.com). (Note: Microsoft retired the Bing Search API in 2025, and Brave dropped
   its free tier, so Tavily is the current free pick. Exa is an alternative with free signup credit.)
2. **Add its MCP server to Claude Code.** Tavily publishes an MCP server. Add it to your Claude Code MCP
   config with your key. If you prefer to run MCP tools in containers, the MCP Docker catalog can install
   and run it for you instead.
3. That is it. The `research` skill will use it automatically for the "go deeper" step, on top of your
   local wiki and built-in search.

All optional. The brain works fully without any of this.

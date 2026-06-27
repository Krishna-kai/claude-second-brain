# Handover and delivery plan

For the next agent or contributor picking up this project. It captures where things stand, the rules to
work by, and the remaining work as clear, testable slices. Read it before you touch anything.

Repo: https://github.com/Krishna-kai/claude-skills-second-brain (live, public, MIT)

## The end goal

A second brain anyone can set up from scratch with Claude Code. It records their notes, projects, and the
people they work with as a linked wiki. It is skills-first (use Claude's built-in skills, or build your own
with `skill-creator`). `CLOTH.md` keeps it from bloating context as it grows. Docker plus MCP can extend it
with deeper research tools. Simple, honest, tested. Built on Andrej Karpathy's LLM Wiki, Cole Medin's
skills idea, and the soul.md pattern, credited.

## Where it stands (what is solid, each piece tested by a fresh agent)

- Wiki structure: `raw/` (immutable sources) -> LLM-built `wiki/` (linked pages) -> `wiki/index.md` +
  `log.md`. Faithful to Karpathy. Tested end to end on a public clone.
- `CLOTH.md`: load only what a task needs; now covers skills too, not just pages (do not load all skills).
- `SOUL.md`: who you are, who you work with, how you like to work. The agent fills it at setup and honours
  it every answer. Tested: it recalled a collaborator's role from day one.
- 4 skills: `research`, `deep-search` (bespoke, multi-source, domain-agnostic), `report`, `skill-creator`.
  The two new ones were tested live and their gaps fixed.
- Setup from scratch: README + `SETUP.md` cover the three permutations (nothing / Claude only / Obsidian
  only), the two app installs (Claude Code, Obsidian), and "Open folder as vault". Honest about what Claude
  cannot install.
- Two entry paths, both tested: clone the URL, or paste `CLAUDE.md` into an empty folder (it self-builds).

## Rules to work by (do not skip these)

- **Public repo.** Never commit client names, secrets, personal paths, or anything private. Scan every
  commit for API keys, passwords, private keys, and personal file paths, and fix any hit before pushing.
- **No em dashes.** Hyphens, commas, full stops. House rule. Check before every commit.
- **Test before you claim.** For any new skill or behaviour, spawn a FRESH agent, give it only the folder and
  a real request, have it use the kit cold and return a blunt PASS/FAIL with gaps. Fix the gaps. Never write
  "it works" without a run.
- **Keep it simple.** This kit ballooned to 73 files once, was deleted, and rebuilt to 13. Add a file or a
  skill ONLY when a real need plus a test proves it. YAGNI is load-bearing here.
- **Clean test artifacts.** The kit ships empty (`raw/` and `wiki/` have only a starter). Remove anything a
  test created before committing.
- **Push to `origin` only.** Credit the lineage in anything new.

## Remaining work (slices, each shippable and testable)

### Slice 5 - Full end-to-end validation (DO THIS FIRST)

One fresh clone of the live repo, one agent, the whole journey in a single run: set up (fill `SOUL.md`),
ingest a source, query, research, deep-search, create a skill with `skill-creator`, report, lint. Confirm
every step works together and that `wiki/`, `SOUL.md`, `index.md`, and `log.md` stay consistent.
DoD: a single clean run passes all of it; any gaps fixed; test artifacts cleaned; nothing left in the repo.

### Slice 6 - Docker + MCP guide (the hub that extends research)

`deep-search` works on Claude's built-in search; this elevates it with real search tools via Docker. Write
a clear, OPTIONAL guide (a `docs/` page, pointed to from `skills/README.md` and `SETUP.md`):
- Install Docker. Set up the MCP Docker catalog/gateway: the "hub" that installs and runs MCP tools in
  containers.
- Add a web-search MCP server with a free key. **Verify the free-tier facts at write time.** As of mid-2026:
  Tavily is the current free pick (about 1,000 searches/month, no card); Microsoft retired the Bing Search
  API in 2025 and Brave dropped its free tier, so do not recommend those.
- Wire it so Claude can call it. `deep-search` already says "use the MCP if one is set up."
DoD: the guide is clear and accurate (re-verify the provider facts); ideally test that `deep-search` uses an
MCP search tool when one is present.

### Slice 7 (optional) - More skills, only if a real need shows

`summarise`, `quiz`, `connect` were proposed. Four working skills is a strong v1. Add one only if it earns
its place and is tested. Do not pad to a number.

## How to test (the pattern that worked all the way through)

1. Copy or clone the kit to a temp dir.
2. Spawn a fresh general-purpose agent. Give it ONLY that folder and a realistic user request.
3. Have it use the kit for real (it has web search). Ask for a blunt PASS/FAIL verdict and named gaps.
4. Fix the gaps. Re-test if needed. Clean the artifacts so the kit ships empty.
5. Validate: 0 em dashes, 0 leaks, scan before commit. Push to `origin`.

## Credit (keep it honest, it is the whole ethos)

Andrej Karpathy (LLM Wiki), Cole Medin (second-brain-skills), the soul.md / OpenClaw community, and the
field (progressive disclosure). `CLOTH.md` and the synthesis are ours. We build on each other.

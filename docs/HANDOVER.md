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
- Deeper search via Docker + MCP: an optional `docs/deeper-search.md` guide, facts verified at write time. A
  live Tavily-routing test confirmed `deep-search` really calls the MCP and folds its sources into the wiki.
- Full end-to-end run: all eight steps (setup, SOUL, ingest, query, research, deep-search, skill-creator,
  report, lint) passed on one cold clone; the brain stayed consistent (index complete, 0 dangling links,
  SOUL shaped every answer). The one gap it found is fixed (the saving rule below).
- Front door hardened against weaker models. README and SETUP give the agent an explicit `git clone ... .`
  command (not just a description), the default branch is `main` so the conventional raw URL resolves, and
  the Start prose points at the exact command. Verified with a deliberately literal agent: it clones to the
  top level, no subfolder. What no agent test can replace: a real human installing the apps and pasting the
  URL. That run is the last proof.
- Content checked with the vault's own scorers (`content-check`, `readability-check`, `brand-voice-generator`,
  `claim-verifier`): README, SETUP, and the Docker guide all PASS voice, PUBLISH content, READABLE, and
  CREDIBLE claims (all in the 90s).

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

## Work status (slices)

Slices 1 to 6 are DONE and validated. Only the optional Slice 7 is open.

### Slice 5 - Full end-to-end validation. DONE (2026-06-27).

A fresh clone ran the whole journey in one go (setup, SOUL, ingest, query, research, deep-search,
skill-creator, report, lint). All eight steps passed and the brain stayed consistent. The run found one real
gap, saved pages that were reachable only from the index (silent orphans), now fixed by **one central saving
rule in `CLAUDE.md`**: every saved page goes into `index.md`, gets a `log.md` line, and is linked from at
least one real page. All four skills point at that rule instead of half-restating it.

### Slice 6 - Docker + MCP deeper-search guide. DONE (2026-06-27).

`docs/deeper-search.md`, linked from `SETUP.md` and `skills/README.md`. Provider facts verified at write
time (Tavily 1,000/month free plus a 4-month student plan, no card; Microsoft retired the Bing Search API in
August 2025 and Brave dropped its free tier). It links Docker's official Claude Code steps rather than
hardcoding menus. A live Tavily-routing test confirmed `deep-search` actually calls the MCP and cites its
sources; that run also surfaced and fixed a deferred-tool discovery gap in the skill.

### Slice 7 (optional, OPEN) - More skills, only if a real need shows

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

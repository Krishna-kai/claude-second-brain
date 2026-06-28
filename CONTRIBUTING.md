# Contributing to this kit

For anyone improving the kit. **You do not need this to use the kit, users start at the [README](README.md).**
This is for maintainers: how it is built, the rules to work by, and how to test a change. It describes the
kit as shipped (a near-empty starter); a real vault grows well past any numbers here, that is the point.

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
- The shipped skills (`research`, `deep-search`, `report`, `skill-creator`), each tested live; the current
  list lives in `skills/README.md`. Users grow their own with `skill-creator`, so a real vault has more.
- Setup from scratch: README + `SETUP.md` cover the three permutations (nothing / Claude only / Obsidian
  only), the two app installs (Claude Code, Obsidian), and "Open folder as vault". Honest about what Claude
  cannot install.
- Two entry paths, both tested: clone the URL, or paste `CLAUDE.md` into an empty folder (it self-builds).
- Deeper search via Docker + MCP: an optional `docs/deeper-search.md` guide, facts verified at write time. A
  live Tavily-routing test confirmed `deep-search` really calls the MCP and folds its sources into the wiki.
- Full end-to-end run: all eight steps (setup, SOUL, ingest, query, research, deep-search, skill-creator,
  report, lint) passed on one cold clone; the brain stayed consistent (index complete, 0 dangling links,
  SOUL shaped every answer). The one gap it found is fixed: the saving rule in `CLAUDE.md` (every saved page
  goes into the index, gets a `log.md` line, and is linked from at least one real page).
- Front door hardened against weaker models AND folder-proof. README and SETUP give the agent an explicit
  clone command: clone into the current folder if it is empty, or a clean `second-brain/` subfolder if it
  already has the user's files (never touches them). Default branch is `main` so the conventional raw URL
  resolves. Verified with literal-agent tests in BOTH empty and non-empty folders. What no agent test can
  replace: a real human installing the apps and pasting the URL. That run is the last proof.
- Tonality is first-class. `SOUL.md` has a "My voice" section, the agent asks for it at setup, and reports
  come out in it. Verified end to end: the report obeyed a distinctive voice (takeaway line, UK spellings,
  zero banned buzzwords). The report skill verifies the voice before saving.
- Self-explaining to the human. The README maps every file, states plainly that Claude interviews you to
  build `SOUL.md`, lists the skills, and draws how they connect (text + a mermaid diagram). A one-page
  handout is `docs/QUICKSTART.md`.
- Governed against sprawl. CLAUDE.md names DUNE/DRY/KISS/YAGNI as the rules that keep the wiki from becoming
  a junk drawer, and `lint` prunes for real (archive stale, merge duplicates, split overgrown pages).
  `CLOTH.md` bounds the loading; the principles bound the creating.
- Content checked with the vault's own scorers (`content-check`, `readability-check`, `brand-voice-generator`,
  `claim-verifier`): README, SETUP, QUICKSTART, and the Docker guide all PASS voice, PUBLISH content,
  READABLE, and CREDIBLE claims (all in the 90s).

## Rules to work by (do not skip these)

- **Public repo.** Never commit client names, secrets, personal paths, or anything private. Scan every
  commit for API keys, passwords, private keys, and personal file paths, and fix any hit before pushing.
- **No em dashes.** Hyphens, commas, full stops. House rule. Check before every commit.
- **Test before you claim.** For any new skill or behaviour, spawn a FRESH agent, give it only the folder and
  a real request, have it use the kit cold and return a blunt PASS/FAIL with gaps. Fix the gaps. Never write
  "it works" without a run.
- **Keep it simple.** This kit ballooned to 73 files once, was deleted, and rebuilt small. Add a file or a
  skill ONLY when a real need plus a test proves it. YAGNI is load-bearing here.
- **Clean test artifacts.** The kit ships empty (`raw/` and `wiki/` have only a starter). Remove anything a
  test created before committing.
- **Push to `origin` only.** Credit the lineage in anything new.

## Future (optional, only if a real need shows)

- More skills (`summarise`, `quiz`, `connect` were proposed). The shipped set is a strong v1. Add one only
  when it earns its place and is tested. Do not pad to a number.
- The bigger direction is a **multibrain**: many brains for a team or enterprise, connected (the
  hub-and-spoke + shared-knowledge pattern). That is a separate piece of work, not part of this starter kit.

## How to test (the pattern that worked all the way through)

1. Copy or clone the kit to a temp dir.
2. Spawn a fresh general-purpose agent. Give it ONLY that folder and a realistic user request.
3. Have it use the kit for real (it has web search). Ask for a blunt PASS/FAIL verdict and named gaps.
4. Fix the gaps. Re-test if needed. Clean the artifacts so the kit ships empty.
5. Validate: 0 em dashes, 0 leaks, scan before commit. Push to `origin`.

## Credit (keep it honest, it is the whole ethos)

Andrej Karpathy (LLM Wiki), Cole Medin (second-brain-skills), the soul.md / OpenClaw community, and the
field (progressive disclosure). `CLOTH.md` is Krishna Chodipilli's; the synthesis is ours. We build on each
other.

# Skill: report

Turn what is in the brain into a clear, sourced report the human can hand in or share.

Use this when the human asks for a report, a summary write-up, an essay outline, or a briefing.

## Steps

1. **Gather.** Read `wiki/index.md` and open the pages the report needs. If there are gaps, run the
   `research` skill first.
2. **Structure.** A simple, honest shape:
   - What the report is about, in one or two lines.
   - The main findings, in order, each in plain language.
   - The evidence, with sources cited (wiki pages and any web links).
   - A short conclusion.
3. **Write it in their voice.** Use the human's tonality from the "My voice" section of `SOUL.md`, so the
   report sounds like them, not like a generic AI. Short sentences, no filler.
4. **Check the voice before you save.** Re-read the draft against that "My voice" section and fix anything
   that slipped: a buzzword they ban, the wrong English variant, a missing takeaway, a generic-AI turn of
   phrase. Verify it sounds like them, do not assume it does.
5. **Save it.** Write it to a file (for example `wiki/reports/<topic>.md`) and cite the wiki pages it drew
   from. Then follow the saving rule in `CLAUDE.md`: add it to `wiki/index.md`, add a `log.md` line, and
   link it from at least one page it came from (for example a "Reports" or "See also" line on the topic's
   main page) so it is not an orphan. Tell the human where it is.

A report is just the wiki, aimed at a reader and a deadline. Keep it true to the sources.

# Skill: skill-creator

Make a new skill for a task the human does often, so they do not have to re-explain it each time.

Use this when the human says "make me a skill that does X," or describes a repeatable task they want.

## Steps

1. Get the gist of what the skill should do: the task, when to use it, and the steps if the human knows
   them. Ask a question or two only if it is unclear; otherwise pick sensible defaults and state them. Do
   not stall waiting for answers you can reasonably infer.
2. Write a new file `skills/<name>.md` (a short, lowercase, hyphenated name). Follow the shape of the
   skills already here: a one-line purpose, a "use this when" line, and a short numbered list of steps.
3. Keep it plain and small. A skill is a workflow, not a program. Reuse the wiki the way the other skills
   do: read `wiki/index.md` first, save useful results back as pages, log what you did.
4. Add a line for it in `skills/README.md` so it is listed, then tell the human it is ready and how to
   trigger it.

A good skill is short enough to read in one go and clear enough that you follow it without guessing.

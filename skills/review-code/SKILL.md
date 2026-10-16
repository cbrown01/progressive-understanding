---
name: review-code
description: Review a code change (diff, branch, or PR) as a progressive explanation, so the reviewer grasps what changed and why before reading findings. Use when asked to review code, "walk me through this change", or "help me understand this PR before I review it".
---

# Review Code

Apply the Progressive Understanding order to code under review. The reader can stop after any section and still hold a true picture of the change. Don't use an idea before introducing it.

## Before writing

- Read the full diff and enough surrounding code to know what it touches. Read the description, linked issue, and tests.
- Note what you did not read or run. Don't claim a check you didn't do.

## Sections

1. **Idea** — What the change does, or why it exists, in one sentence.
2. **ELI5** — 1–3 plain sentences: how to think about the change.
3. **TLDR** — Up to 5 bullets: what changed, in which places, at what risk.
4. **Visual** — Flow, call graph, or before/after diagram when the change has moving parts.
5. **You Should Know** — Up to 5 facts: side effects, invariants, migrations, callers affected, landmines.
6. **This, Not That** — Up to 5 decisions the change made versus the alternatives ("a class, not a function, because…"). Skip if none.
7. **Example** — One concrete path through the new code (a request, input, or call).
8. **Deep Dive** — File-by-file or step-by-step detail, then **Findings** ranked by severity, each with location, failure scenario, and suggested fix.

## Rules

- Findings belong in the Deep Dive. Put a finding in an earlier section only if it changes how the reader should understand the whole change.
- Separate bugs (will misbehave) from preferences (would be nicer). Label which is which.
- Put open questions for the author in the earliest section where the reader can see why they matter.
- Later sections build on earlier ones; they don't repeat them. Omit empty sections.
- Use the code's own names.

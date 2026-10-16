---
name: describe-pr
description: Write a pull request description that builds understanding progressively, so a reviewer can stop reading at any point and still know what the PR does. Use when asked to write, draft, or improve a PR description or summary.
---

# Describe a PR

Apply the Progressive Understanding order to a pull request description. Reviewers skim; each section must add something the earlier ones did not.

## Before writing

- Read the diff, commit messages, and linked issue. If the repo has a PR template, keep its required headings and fill them using the sections below.
- Describe what the diff does, not what you intended. Check them against each other.

## Sections

1. **Goal** (Idea) — One sentence: what this PR achieves or why it exists.
2. **ELI5** — 1–3 plain sentences: how to think about the change.
3. **TLDR** — Up to 5 bullets: what changed and what to know if you read no further.
4. **Visual** — A diagram when the change has flow or structure. Skip otherwise.
5. **You Should Know** — Up to 5 facts: behavior changes, migrations, flags, risks, gotchas.
6. **This, Not That** — Up to 5 decisions versus alternatives ("a class, not a function, because…"). Skip if none.
7. **Testing** (Example) — One concrete way it was verified or can be exercised. Skip if the PR is itself an example.
8. **Details** (Deep Dive) — Per-area explanation, what's out of scope, follow-ups.

## Rules

- Put open questions for reviewers in the earliest section where they make sense.
- State only what you checked. Say "not tested" where true.
- Later sections build on earlier ones; they don't repeat them. Omit empty sections.
- Use the code's own names. Don't pad.

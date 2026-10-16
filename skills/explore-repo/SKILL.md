---
name: explore-repo
description: Explain an unfamiliar code repository so a newcomer builds a working mental model step by step. Use when asked to explore, onboard to, map, or "help me understand" a codebase or repo.
---

# Explore a Repo

Apply the Progressive Understanding order to a codebase. The reader can stop after any section and still hold a true, useful map of the repo.

## Before writing

- Read the README, manifest and build files, top-level layout, entry points, and tests. Run nothing destructive; run the build or tests only if asked or clearly safe.
- Trace at least one real path (a request, command, or job) end to end before explaining it.
- Note what you did not read. Don't describe code you only inferred from filenames as fact.

## Sections

1. **Idea** — What the repo is for, in one sentence.
2. **ELI5** — 1–3 plain sentences: how to think about its shape.
3. **TLDR** — Up to 5 bullets: stack, main parts, how to run it, where to start reading.
4. **Visual** — Module or dependency map, or data flow. Usually worth including here.
5. **You Should Know** — Up to 5 facts: entry points, build and test commands, config and environments, conventions, gotchas.
6. **This, Not That** — Up to 5 design choices versus the obvious alternative ("a queue, not direct calls, because…"). Skip if none are evident.
7. **Example** — Trace one request or command through the code, naming files and functions.
8. **Deep Dive** — Directory-by-directory detail, key abstractions, data model, testing, deployment, and what you left unexplored.

## Rules

- Put uncertainty ("I couldn't tell whether X is still used") in the earliest section where the reader can see why it matters.
- Later sections build on earlier ones; they don't repeat them. Omit empty sections.
- Use the repo's own names for modules, commands, and concepts.

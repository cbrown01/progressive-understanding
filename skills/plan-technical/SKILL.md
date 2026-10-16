---
name: plan-technical
description: Write a technical plan (implementation, migration, or design) that builds understanding progressively, so a reader can approve or challenge it after any section. Use when asked to plan, design, or propose a technical approach, or to write a plan for an issue.
---

# Plan Technical Work

Apply the Progressive Understanding order to a plan. The reader should be able to stop after any section and know what is proposed and why.

## Before writing

- Read the issue or request and the code it touches. A plan about code you haven't read is a guess; say so if you must.
- Identify the decisions that need the reader's input before you commit to an approach.

## Sections

1. **Goal** (Idea) — One sentence: the outcome, and why it matters.
2. **ELI5** — 1–3 plain sentences: how to think about the approach.
3. **TLDR** — Up to 5 bullets: the approach, what changes, the main risk, and what you need from the reader.
4. **Visual** — Architecture, sequence, or phase diagram when it helps.
5. **You Should Know** — Up to 5 facts: constraints, dependencies, existing behavior, landmines.
6. **This, Not That** — Up to 5 decisions: chosen approach versus rejected alternatives, with the reason.
7. **Example** — One scenario traced through the finished design.
8. **Deep Dive** — Phases and steps, files to change, testing and verification, rollout and rollback, what's out of scope.

## Rules

- Put open questions and uncertainty in the earliest section where the reader can see why they matter, not buried in the Deep Dive.
- Say what you verified and what you assumed.
- Later sections build on earlier ones; they don't repeat them. Omit empty sections.
- Use the project's own names. Keep steps concrete enough that someone else could execute them.

# Overview of this repo

Written with its own prompt ([`prompt.md`](prompt.md)), applied the way [`explore-repo`](skills/explore-repo/SKILL.md) describes. Nothing here is executed; the repo has no code, build, or tests.

## Idea

A prompt for explaining anything in layers, plus skills that apply it to specific situations.

## ELI5

Think of a zoom lens. The first sentence gives the whole picture, and each section after adds detail without making you re-learn what came before. You can stop at any point and still hold something true.

## TLDR

- The product is one prompt: eight ordered sections, **Idea → ELI5 → TLDR → Visual → You Should Know → This, Not That → Example → Deep Dive**.
- It ships as `prompt.md` (paste into any chat or system prompt) and as six installable skills under `skills/`.
- Five skills are scenario variants: the prompt plus a mapping for that situation. `progressive-understanding` is the prompt itself.
- It's all Markdown: no runtime, dependencies, or tests. Installation is via the [`skills` CLI](https://www.skills.sh/).
- Start with `prompt.md`, then read the scenario skill closest to your use.

## Visual

```
prompt.md ──(same text, plus frontmatter)──▶ skills/progressive-understanding/SKILL.md
    │
    └─ order + rules, reused by ─▶ skills/explore-topic    (concepts, events, stories)
                                   skills/review-code      (diffs, PRs)
                                   skills/describe-pr      (writing a PR description)
                                   skills/plan-technical   (technical plans)
                                   skills/explore-repo     (codebases)
```

## You Should Know

- **Each skill stands alone.** The scenario skills restate the order rather than linking to it, so one can be installed without the others. The cost is duplication.
- **`prompt.md` and `skills/progressive-understanding/SKILL.md` are the same prompt in two files.** Nothing enforces that they stay in sync. Edit both.
- **The rules are the substance.** Later sections build on earlier ones and don't repeat them; empty sections are omitted; open questions go in the earliest section where they matter.
- **Scenario skills add three things:** what to gather first ("Before writing"), what each section means for that situation, and rules for pitfalls specific to it.
- **Skills are discovered through `SKILL.md` frontmatter.** The `description` field is what triggers a skill, so changes to it change when the skill fires.

## This, Not That

- **Layered, not a single summary.** A summary serves one reader depth; layers serve every stopping point.
- **Separate ELI5 and TLDR.** ELI5 is "how should I think about this?"; TLDR is "what do I need to know?" They are not the same question at two lengths.
- **Prompt plus skills, not a framework.** Text is portable across any assistant. Skills add triggering and scenario guidance only where that helps.
- **Omit sections, don't pad them.** A missing section signals that nothing was left to add.

## Example

Using `explore-repo` on this repo produces the document you are reading:

1. Read the README, `prompt.md`, and each `SKILL.md` (the "Before writing" step).
2. Find the single idea (a prompt with an order) and fill **Idea** and **ELI5** from it.
3. List the parts for **TLDR**, and draw how they relate for **Visual**.
4. Put the gotchas (duplication, sync) in **You Should Know**.
5. Leave the rest for the sections below.

## Deep Dive

Covers every file in the repo. Leaves out the cited research in the README's Lineage section.

### Top level

- `README.md`: what the prompt is, install commands, a table of skills, rules in brief, and lineage (the prior art the order rediscovers).
- `prompt.md`: the canonical prompt. Defines the eight sections, their length limits (e.g. up to 5 bullets in TLDR), and five rules.
- `LICENSE`: MIT.

### `skills/`

Six directories, each with one `SKILL.md` of 30–40 lines and no other files.

| Skill | Distinguishing content |
|---|---|
| `progressive-understanding` | The prompt with skill frontmatter. Applies to anything. |
| `explore-topic` | General learning: concepts, objects, processes, events, decisions, stories. |
| `review-code` | Read the full diff, description, and tests first, so the reviewer grasps the change before seeing findings. |
| `describe-pr` | Output is a PR description a reviewer can stop reading at any point. |
| `plan-technical` | Output is a plan that can be approved or challenged early. |
| `explore-repo` | Trace a real path through the code before explaining it; say what you didn't read. |

The scenario skills share a shape: frontmatter (`name`, `description`), a one-line statement of the goal, "Before writing", the eight sections remapped to the situation, and "Rules".

### Testing and maintenance

There are no tests. Consistency is by convention: the rules in `prompt.md` should hold in every skill, and the two copies of the base prompt should match. Both are checked by reading.

### Not covered

How the `skills` CLI resolves and installs from this repo was not examined; the README's commands were taken at face value.

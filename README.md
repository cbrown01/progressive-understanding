# Progressive Understanding

A prompt for explaining anything so understanding accumulates. A reader can stop after any section and still hold a true, useful picture. Each section adds something the earlier ones did not.

The order: **Idea → ELI5 → TLDR → Visual → You Should Know → This, Not That → Example → Deep Dive.**

The full prompt is in [`prompt.md`](prompt.md). Paste it into any chat or system prompt as is. It also ships as a skill, alongside skills that apply it to specific situations.

## Install

Skills install with the [`skills` CLI](https://www.skills.sh/):

```sh
# list what's here
npx skills add cbrown01/progressive-understanding -l

# install everything
npx skills add cbrown01/progressive-understanding --all

# install one
npx skills add cbrown01/progressive-understanding -s review-code
```

## Skills

| Skill | Use it to |
|---|---|
| [`progressive-understanding`](skills/progressive-understanding/SKILL.md) | Explain anything. The prompt itself, as a standalone skill. |
| [`explore-topic`](skills/explore-topic/SKILL.md) | Learn a concept, object, process, event, decision, or story. |
| [`review-code`](skills/review-code/SKILL.md) | Review a diff or PR; grasp the change before reading findings. |
| [`describe-pr`](skills/describe-pr/SKILL.md) | Write a PR description reviewers can stop reading at any point. |
| [`plan-technical`](skills/plan-technical/SKILL.md) | Write a technical plan that can be approved or challenged early. |
| [`explore-repo`](skills/explore-repo/SKILL.md) | Get oriented in an unfamiliar codebase. |

The scenario skills are the prompt plus a mapping: what each section means for that situation, what to gather first, and what to watch for. Each works installed alone.

## Rules in brief

- ELI5 answers "how should I think about this?" TLDR answers "what do I need to know?"
- Later sections build on earlier ones; they don't repeat them.
- Omit a section that adds nothing.
- Put an open question in the earliest section where the reader can see why it matters.
- Use the subject's own terms.

## License

MIT

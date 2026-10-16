# Progressive Understanding

A prompt for explaining anything so understanding accumulates. A reader can stop after any section and still hold a true, useful picture. Each section adds something the earlier ones did not.

The order: **Idea → ELI5 → TLDR → Visual → You Should Know → This, Not That → Example → Deep Dive.**

The full prompt is in [`prompt.md`](prompt.md). Paste it into any chat or system prompt as is. It also ships as a skill, alongside skills that apply it to specific situations.

New here? [`OVERVIEW.md`](OVERVIEW.md) explains this repo in the same format.

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

## Lineage

The order is new; the idea isn't. It rediscovers older answers to the same problem:

- **Advance organizers.** A general frame before the details, at a higher level than a summary. The ELI5. Ausubel, D. P. (1960). The use of advance organizers in the learning and retention of meaningful verbal material. *Journal of Educational Psychology*, 51, 267–272.
- **Spiral curriculum.** Teach an honest simple version first, then return in more depth. Bruner, J. S. (1960). *The Process of Education*. Harvard University Press.
- **Elaboration theory.** Start with an epitome, then zoom in. Reigeluth, C. M. (1979). In search of a better way to organize instruction: The elaboration theory. *Journal of Instructional Development*, 2(3), 8–15.
- **Answer first.** Minto, B. *The Pyramid Principle: Logic in Writing and Thinking*; the U.S. Army's BLUF, "bottom line up front" (AR 25-50, *Preparing and Managing Correspondence*); the newspaper inverted pyramid (Pöttker, H. (2003). News and its communicative quality: The inverted pyramid—when and why did it appear? *Journalism Studies*, 4(4), 501–511).
- **Progressive disclosure.** Defer detail to a later layer. Carroll, J. M., & Carrithers, C. (1984). Training wheels in a user interface. *Communications of the ACM*, 27(8), 800–806.

## License

MIT

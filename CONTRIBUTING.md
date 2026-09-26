# Contributing

Cloudberry is early, and this repository is an invitation to shape it. You do not need an elaborate proposal or a perfect pull request to take part.

## Pick an angle

- **Product / UX:** make the Newspaper, threads, and return-to-work flow clearer.
- **Frontend:** explore readable, calm interfaces for project history.
- **Architecture:** test the Journal, projection, and addressable-context model.
- **Agent workflows:** improve contracts, evidence, handoffs, and review.
- **Integrations:** connect real activity from development, creative, or operational tools.
- **Experiments:** design a small test that can prove or disprove an assumption.

## Start with an issue

Use a compact shape:

```text
IDEA
What do you propose?

WHY
What problem does it solve for a person or project?

WHAT IT WOULD CHANGE
Which current concept, flow, or milestone would be affected?

EVIDENCE
What observation would tell us the idea worked?
```

A rough sketch, example morning story, failed workflow, or concrete question is welcome.

## Discuss before building large changes

For changes that affect the product model or architecture, open an issue before writing substantial code. The purpose is to agree on the problem, evidence, and scope while the change is still easy to reshape.

Small documentation fixes and tightly scoped experiments can go directly to a pull request.

## Keep the evidence boundary visible

When proposing or documenting work:

- label future behavior as a proposal or vision;
- keep facts separate from agent or human interpretation;
- treat agent completion messages as claims that need evidence;
- derive views from canonical history instead of creating a second truth;
- avoid expanding the current milestone without saying so;
- preserve reviewed baselines unless new evidence justifies changing them.

Read [Current proof](docs/current-proof.md) before making claims about what already works. AI agents should begin with [For AI agents](FOR-AI-AGENTS.md).

## Pull requests

Keep each pull request understandable on its own. Explain:

1. the problem;
2. the resulting behavior or document change;
3. how you checked it;
4. any assumption that still needs a human decision.

There is no enterprise ceremony here. Clear intent, small scope, and honest evidence are enough.

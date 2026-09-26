# Briefing for AI Agents

Use this file when joining Cloudberry with little or no prior context.

## Mission

Cloudberry is a workspace between a human, their projects, tools, and AI agents. It preserves real activity as project history and turns that history into views that help a person understand what happened and continue the work.

The first product interface is the **Newspaper**: a calm morning edition of meaningful changes across projects. Each story should lead back to an addressable project thread, its context, and a next action.

Cloudberry is not primarily an agent execution framework. Agents work inside it; the product is continuity, context, evidence, and navigation across work.

## Read in this order

Start with the smallest context that can answer the task:

1. Read this file.
2. Read [Current proof](docs/current-proof.md) to separate evidence from aspiration.
3. Choose one relevant document:
   - product or UX: [Product vision](PRODUCT-VISION.md)
   - concepts and flows: [How it works](HOW-IT-WORKS.md)
   - invariants and boundaries: [Architecture](docs/architecture.md)
   - sequence of product slices: [Roadmap](ROADMAP.md)
   - proposing work: [Contributing](CONTRIBUTING.md)
4. Ask for or inspect local implementation context only after locating the relevant area.

```text
MAP → RELEVANT AREA → LOCAL CONTEXT → TASK
```

Do not load an entire project by default. Build context progressively and name any uncertainty that remains.

## Core model

```text
ACTIVITY → EVENT → JOURNAL → PROJECTION → THREAD → ACTION
```

- A **project** is a durable place for related work.
- A **thread** is a meaningful, nestable branch of work.
- A **run** is one bounded agent or tool execution inside one thread.
- An **event** records a fact or an interpretation with provenance.
- The **Journal** is the durable history.
- The **Newspaper**, model map, and current state are projections over that history.

Keep these distinctions intact. In particular, do not make an agent run the primary project structure and do not let a projection become a competing source of truth.

## Evidence boundary

### Proven

- The Code Engine MVP showed that two agents can work from the same implementation contract and be checked by a shared model of rules.
- The Model Map experiment showed that navigation can be presentation computed from canonical material rather than duplicated truth.
- Journal Review 1 exercised `real activity → event → journal → reload → projection` and passed 8/8 live checks.
- Event contract v1 established project, thread, run, `fact | interpretation` origin, thread parentage, a derived rather than stored `thread_path`, fact-derived state, and one-thread-per-run scope.

### Experimental now

- Newspaper selection and presentation.
- Thread navigation.
- Current-state projection beyond the reviewed foundation.

### Vision

- The complete Cloudberry UI and living workspace.
- A multi-project morning Newspaper populated by background work.
- Broad multi-agent and external software integration.

The public repository documents these results; it is not itself the implementation or test archive. Never describe the complete product as shipped.

## Current milestone

The current slice is **Newspaper**. The product question is:

> Can a person quickly understand meaningful project changes, trust the evidence boundary, and move from a story back into the exact context needed to continue?

Work on later slices should not silently enter this milestone.

## Working rules

1. **Do not confuse vision with implemented behavior.** Label claims as proven, experimental, proposed, or unknown.
2. **Facts and interpretations must remain distinguishable.** A summary may explain facts; it must not replace them.
3. **Prefer projections over duplicated sources of truth.** Derive views from canonical history whenever the model allows it.
4. **Human owns product decisions.** Present evidence and trade-offs; do not imply that agent output is authority.
5. **Do not widen implementation scope silently.** State a proposed scope change and its reason before acting on it.
6. **Read the smallest relevant context first.** Navigate from the map to the area, then to local details and the task.
7. **Existing proven baselines should not be casually rewritten.** Preserve them unless new evidence and explicit review justify a revision.

Also:

- Treat “done” as a claim that needs observable evidence.
- Keep role, person, and model separate: `ROLE ≠ PERSON ≠ MODEL`.
- Keep runs inside one thread unless a reviewed contract explicitly changes that rule.
- Prefer a small, testable product slice over a broad framework proposal.
- Record assumptions when required context is unavailable.

## A useful response pattern

When asked to help, answer in this order:

1. **Context understood:** name the project area and relevant thread.
2. **Evidence boundary:** state what is known, inferred, and still vision.
3. **Proposed change:** define the smallest useful outcome.
4. **Validation:** explain what observable result would support the claim.
5. **Decision needed:** identify any product choice that belongs to the human.

This pattern is guidance, not a required template. The goal is to make work easy to review and easy to continue.

# Current Proof

This document is the evidence boundary for the public Cloudberry repository. It prevents a useful vision from being mistaken for shipped product behavior.

## PROVEN

### Code Engine MVP

Two different agents can receive the same implementation contract and have their outputs checked against one common model of rules.

What this supports:

- roles and implementation contracts can outlive a particular model;
- comparable verification is possible across different agents;
- an agent's completion claim is not, by itself, proof of completion.

What it does not prove: a general-purpose autonomous agent organization or the full Cloudberry workspace.

### Model Map

A navigational map can be computed as presentation over canonical material rather than maintained as a second source of truth.

What this supports:

- navigation and explanation can change without duplicating the underlying model;
- people and agents can begin with a map and load local detail when needed.

What it does not prove: the final Cloudberry navigation UI.

### Journal Review 1

A live probe exercised the following path:

```text
REAL ACTIVITY → EVENT → JOURNAL → RELOAD → PROJECTION
```

The probe passed **8/8 checks**.

The review established the following baseline for event contract v1:

- events identify a project, thread, and run;
- origin distinguishes `fact` from `interpretation`;
- thread parentage carries structure;
- `thread_path` is derived and is not part of the event contract;
- the thread tree can be rebuilt from events;
- current state is built from facts;
- one run does not cross thread boundaries.

What it does not prove: production scale, every event type, or the complete product experience.

The public repository records these reviewed outcomes. It is an introduction and context package, not the implementation or test archive for those experiments.

## EXPERIMENTAL

### Newspaper projection

Selecting meaningful changes, writing trustworthy summaries, and presenting them as a calm morning edition is the current product slice. The concept is defined; the complete experience is not yet proven.

### Thread navigation

Nested threads are part of the working model. The route from a story to a project, thread, and local context still needs product validation.

### Current-state projection

The reviewed baseline says state should derive from factual events. A broader, user-facing current-state view remains experimental.

## VISION

- A complete Cloudberry interface.
- A living workspace where projects retain context over time.
- Background project activity that remains understandable when a person returns.
- A multi-project morning Newspaper fed by real events.
- Seamless movement from news to context to action.
- Broad coordination among people, roles, and different AI models.
- Integrations with development tools, creative software, servers, and automation.

These are product directions, not claims about current implementation.

## How to use this boundary

When discussing Cloudberry, use language that matches the evidence:

- **Proven:** “The live Journal path passed 8/8 checks.”
- **Experimental:** “We are testing whether Newspaper stories lead back to useful context.”
- **Vision:** “Cloudberry should become a living workspace across projects and tools.”

If new evidence changes this boundary, record what was tested, the observable result, and which earlier assumption it updates.

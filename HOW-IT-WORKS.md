# How Cloudberry Works

Cloudberry keeps one durable history of activity and derives useful views from it.

```text
TOOLS / AGENTS / HUMAN
          ↓
        EVENTS
          ↓
        JOURNAL
          ↓
      PROJECTIONS
   ┌──────┼──────┐
   ↓      ↓      ↓
 NEWS    MAP   STATE
          ↓
       THREAD
          ↓
       ACTION
```

This is a product model, not a database specification. The implementation may change as long as the distinctions below remain clear.

## The six nouns

### Project

A durable place for related work: a product, a creative piece, a server, or any other continuing effort.

### Thread

A meaningful branch inside a project. Threads can be nested. They organize context by the shape of the work rather than by which agent or chat happened to touch it.

### Run

One bounded execution by an agent or tool inside a thread. A run provides provenance. It does not replace the thread, and a single run does not cross thread boundaries in the tested event contract.

### Event

A record of something that happened or an interpretation made about it. Events identify their project, thread, run, origin, and structural parentage where relevant.

### Journal

The ordered history built from events. It preserves what the system knows about the work and supports replay after a reload.

### View

A projection computed from the Journal for a particular purpose: reading news, navigating the model, or understanding current state. A view may be regenerated; it should not quietly become another source of truth.

## Fact and interpretation

Cloudberry keeps observations distinguishable from conclusions.

```text
FACT
Something recorded as having occurred.
Example: “The test command exited successfully at 01:12.”

INTERPRETATION
A conclusion, summary, or judgment about facts.
Example: “The change appears ready for review.”
```

Interpretations are valuable—the Newspaper depends on them—but they do not overwrite facts. Current state is built from factual events. An agent's claim that work is complete is therefore useful input, not sufficient proof by itself.

## From history to a morning edition

Suppose an agent completes a render while a person is away:

1. The tool reports real activity.
2. Cloudberry records an event in the relevant project and thread.
3. The Journal preserves that event across reloads.
4. The Newspaper projection selects and explains the change.
5. The story links to the thread and its local context.
6. The person reviews the result and chooses the next action.

The Newspaper does not need to own the render state. It needs to tell a trustworthy story about the underlying event and make the context addressable.

## Context is loaded by relevance

A person or agent should not need the entire project history for every task.

```text
MAP → RELEVANT AREA → LOCAL DETAILS → TASK
```

The map locates the work. The selected thread supplies nearby decisions, evidence, and state. More detail is loaded only when it is needed. This keeps large, long-running projects understandable without flattening them into summaries.

## People, roles, and models

Cloudberry separates the stable responsibility from whoever performs it:

```text
USER
  ↓
COORDINATOR
  ├── ARCHITECT
  ├── RESEARCH
  ├── IMPLEMENTATION
  └── NEWS
         ↓
       REPORT → REVIEW → USER

ROLE ≠ PERSON ≠ MODEL
```

A role can move between models or people. Reports return evidence for review. The human remains responsible for product direction.

For the deeper constraints behind this model, read [Architecture](docs/architecture.md). For the implementation boundary, read [Current proof](docs/current-proof.md).

# Architecture Principles

Cloudberry's implementation is expected to evolve. These principles describe the boundaries that should remain stable while it does.

## 1. The Journal preserves history

Real activity enters the system as events.

```text
ACTIVITY → EVENT → JOURNAL
```

The Journal provides durable, replayable history. It should preserve enough provenance to say which project, thread, and run an event belongs to and whether the event records a fact or an interpretation.

The Journal is not a news feed. It is the material from which a news feed and other views can be built.

## 2. Views are projections

```text
JOURNAL
├── NEWSPAPER
├── MODEL MAP
└── CURRENT STATE
```

Each view answers a different question:

- **Newspaper:** What changed, and what deserves attention?
- **Model Map:** Where in the project does this belong?
- **Current State:** What factual state can be derived now?

Views may summarize, filter, and organize. They should remain reproducible from canonical history instead of becoming independent stores that drift away from it.

## 3. Context is addressable

Large projects cannot be understood by loading everything at once. Cloudberry should let a person or agent locate a meaningful area and request only the nearby detail.

```text
MAP → AREA → DETAILS
```

Projects contain nested threads, and events carry the parent information needed to rebuild that structure. In the reviewed event contract, `thread_path` is derived rather than stored as event truth.

Addressable context connects the summary back to the work: a Newspaper story should lead to its project and thread, then expose the evidence and decisions needed for the next action.

## 4. Role, person, and model are separate

```text
ROLE ≠ PERSON ≠ MODEL
```

A role is a stable contract such as coordinator, architect, researcher, implementer, or news editor. A person or model may perform that role for a particular run. Changing the performer should not erase the thread's meaning or history.

Runs provide execution provenance but do not define the project hierarchy. In event contract v1, one run belongs to one thread.

## 5. Product state needs evidence

An agent saying “done” is an interpretation or claim. It may be correct, but product state should not depend on that statement alone.

```text
CLAIM + OBSERVABLE FACTS → REVIEWABLE CONCLUSION
```

Current state is derived from facts. Interpretations remain linked and useful for explanation, triage, and news selection, while staying distinguishable from the observations that support them.

## 6. Humans own product decisions

Agents can implement, research, coordinate, and report. Their output should return to review with provenance and evidence. Decisions about product direction, scope, and consequential trade-offs remain with the human.

These principles are partly supported by focused experiments and partly guide work still ahead. [Current proof](current-proof.md) records that boundary explicitly.

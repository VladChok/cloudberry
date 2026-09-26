# Product Vision

## Projects should remain alive between sessions

People rarely have only one project. A codebase may be moving while a visual project is rendering, a research thread is waiting for review, and a server needs attention. AI agents make more parallel work possible, but they also multiply the places where context can disappear.

Today, returning to work often means reconstructing the past from chat histories, terminal output, commits, files, notifications, and memory. A successful background run may be invisible. A confident “done” may not match the artifacts. An important decision may exist only in the conversation that produced it.

Cloudberry should make returning feel different.

## Morning is the defining moment

You open Cloudberry and see a Newspaper: a readable edition of what changed across your projects while you were away.

It tells you that a code change was merged, a render completed, assets were exported, or a server went offline. It separates what happened from what an agent thinks it means. It gives enough context to decide what deserves attention.

Then the Newspaper gets out of the way.

```text
STORY → PROJECT → THREAD → LOCAL CONTEXT → ACTION
```

A story is useful because it leads back to the place where the work can continue. Reading and acting are parts of the same experience.

## Projects are places; threads are paths through them

Cloudberry organizes work as projects containing threads. A thread is a meaningful line of work, not necessarily a ticket and not necessarily short-lived. Threads can contain other threads when the work develops structure.

```text
Cloudberry
└── Newspaper
    ├── Journal architecture
    ├── Reading experience
    └── Event projection
```

An agent run happens inside this context. The run matters as provenance, but it does not become the main shape of the project. A person should be able to continue the same thread with another model, another tool, or no agent at all.

## Humans and agents share a workspace

Cloudberry treats agents as participants with bounded roles. A coordinator, architect, researcher, implementer, and news editor are working contracts; they are not permanently tied to a person or model.

```text
ROLE ≠ PERSON ≠ MODEL
```

This separation lets the work survive changes in tools. It also keeps responsibility clear: agents can gather evidence, propose decisions, and perform work, while the human owns product direction and consequential choices.

## History creates continuity

The product begins with a modest promise: record real activity as events, preserve it in a journal, and compute views from that journal.

That history supports several ways of seeing the same project:

- the Newspaper explains what changed;
- a map helps locate the relevant area;
- current state summarizes what is true now;
- a thread holds the local context needed to continue.

Because these are views over shared history, they can improve without rewriting the underlying facts.

## The feeling we are aiming for

Cloudberry should feel less like Jira or an AI chat history and more like a living place where your projects continue to exist while you are away.

It should be calm enough to read in the morning, precise enough to trust, and direct enough that any story can become the next action. The long-term product is a common environment for creative work, software, research, automation, and the agents that help with them.

That is the vision. The current build is narrower: establish the Journal foundations, then make the Newspaper a real and useful first slice. See [Current proof](docs/current-proof.md) for the exact boundary.

# ☁ Cloudberry

> **A living workspace where your projects keep making sense while you are away.**

Cloudberry is where people, projects, tools, and AI agents live in the same working environment.

You open it in the morning like a newspaper.

While you were away, a render finished.  
An agent completed a research branch.  
A build failed.  
A server went offline.  
A design changed.  
Another agent finished a task and left the result for review.

Cloudberry already knows where each of these things belongs.

> **По-русски:** Cloudberry — живое рабочее пространство для проектов, людей, инструментов и AI-агентов. Утром вы открываете его как газету: видите, что произошло за ночь, и сразу возвращаетесь именно в ту ветку работы, где нужно продолжить.

---

## Good morning

```text
WHAT HAPPENED WHILE YOU WERE AWAY?

CHARACTER
Final render completed
03:44

CLOUDBERRY
Newspaper model updated
04:12

BCH
Campaign assets exported
05:03

MINECRAFT
Server went offline
05:41
```

The Newspaper is not a dashboard to stare at.

It is a way back into the work.

```text
STORY
  ↓
PROJECT
  ↓
THREAD
  ↓
CONTEXT
  ↓
CONTINUE WORK
```

A story tells you what changed.

Open it and Cloudberry brings the relevant project into focus: the exact thread, nearby decisions, evidence, files, actions, and the place where work can continue.

No archaeological expedition through yesterday's chats.

**The project remembers.**

---

## One workspace, many depths

Cloudberry is not built around chat history.

The workspace has structure.

```text
ALL PROJECTS
     ↓
PROJECT
     ↓
THREAD
     ↓
THREAD
     ↓
INFORMATION → ACTION → INFORMATION
     ↓
RAW / LOG
```

Zoom out and you see the state of all your projects.

Zoom in and a project unfolds into meaningful lines of work.

Go deeper and a thread becomes tasks, files, images, references, decisions, tools, conversations, and results.

Deeper still are commands, logs, raw data, and execution details.

The level of detail changes with your focus instead of forcing the entire project onto the screen at once.

---

## Work has shape

Cloudberry does not force every part of work into the same generic SaaS card.

A newspaper should feel like a newspaper.

An archive should feel like memory.

A control panel should feel like a control panel.

A tool can have switches, buttons, mechanisms, sounds, materials, weight, and its own visual language.

The interface is not decoration placed over data.

**The way something looks and behaves helps tell you what kind of thing it is.**

Important things feel important.  
New work is easy to notice.  
Old work fades into history instead of disappearing.  
Actions react like actions.  
Tools can become visually memorable places.

This gives the workspace spatial and associative memory: you remember where work lives, not only what a menu item was called.

---

## The same project can become different views

Cloudberry does not need a separate app for every way of looking at work.

```text
                    ONE PROJECT HISTORY
                           │
          ┌────────────────┼────────────────┐
          ↓                ↓                ↓
      NEWSPAPER          BOARD            GRAPH
   what happened?    where is it?     how is it related?
          │                │                │
          └──────────────┬─┴────────────────┘
                         ↓
                       TABLE
                 what is true now?
                         ↓
                       CHAT
              continue this local thread
```

These are projections of the same work, not competing copies of it.

The Newspaper answers **what happened**.

The Board answers **where things are**.

The Graph answers **how work is connected**.

The Table answers **what state things are in**.

Chat is one way to continue a specific thread. It is not the spine of the whole system.

---

## Humans, agents, and tools share the workspace

AI agents are workers inside Cloudberry.

They are not the product itself.

One agent can research.  
Another can write code.  
Another can inspect a repository.  
Another can render, test, monitor, summarize, or operate a tool.

A project can survive switching from Claude to Codex, from an agent to a person, or from one tool to another.

```text
ROLE ≠ PERSON ≠ MODEL
```

A role is a stable responsibility.

The performer can change.

The project history remains.

And when an agent says **DONE**, Cloudberry can keep that statement separate from the evidence produced by the work.

```text
FACT ≠ INTERPRETATION
```

You can move from a summary back to the source.

---

## History does not disappear

Finished branches, abandoned directions, old decisions, and previous versions do not need to vanish.

The active path stays clear.

The past fades into the background and becomes history.

Cloudberry behaves less like a task manager and more like **memory for an entire working environment**.

The goal is continuity:

```text
“What happened?”
        ↓
“I understand.”
        ↓
“I know where it belongs.”
        ↓
“I can continue.”
```

---

## Underneath the experience

The visible workspace is built over recorded project activity.

```text
HUMAN / AGENTS / TOOLS
          ↓
        ACTIVITY
          ↓
        EVENTS
          ↓
        JOURNAL
          ↓
   ┌──────┼──────┐
   ↓      ↓      ↓
 NEWS    MAP    STATE
          ↓
       THREAD
          ↓
       ACTION
```

The Journal preserves history.

Views are computed from that history instead of silently becoming new sources of truth.

Threads are meaningful, nestable branches of work that can outlive any single chat, tool, or agent run.

---

## What exists today

Cloudberry is still early. The full interface described above is the product direction; the foundation is being built and tested slice by slice.

### PROVEN

- **Code Engine MVP** — the same implementation contract can be given to different agents and checked with shared verification rules.
- **Computed Model Map** — navigation can be derived from canonical material instead of maintained as duplicated truth.
- **Journal event contract v1** — real activity can flow through `event → journal → reload → projection`; Review 1 passed **8/8 live checks**.
- **Gazeta projection v1** — project/thread tree, event sections, run state, unread state, FACT / INTERPRETATION, and ALL projection are frozen as a presentation-only contract.

### CURRENT

**Newspaper frontend** — turn the proven Gazeta projection into the first real Cloudberry experience.

### NEXT

- project / thread navigation;
- focus + context and semantic zoom;
- workspace from context to action;
- human evidence / approval;
- multi-agent integration;
- external creative, development, server, and automation tools.

For the exact evidence boundary, read [Current proof](docs/current-proof.md).

---

## For AI agents

If a user gave you only this repository, this README is enough to understand the project before asking for more context.

```text
MISSION
Keep long-running projects understandable across
people, agents, tools, chats, and time.

CURRENT PRODUCT SLICE
Newspaper frontend.

CORE MODEL
PROJECT → THREAD → RUN → EVENT → JOURNAL → PROJECTION

WORKSPACE MODEL
INFORMATION → ACTION → INFORMATION

UX DIRECTION
Newspaper → Board / Graph / Table / Chat
with focus + context and semantic zoom.

PRINCIPLES
- do not confuse vision with implemented behavior;
- keep FACT and INTERPRETATION distinguishable;
- prefer projections over duplicated truth;
- preserve proven baselines;
- human owns product decisions;
- do not widen scope silently;
- load the smallest relevant context first.
```

Need more depth?

- **Product vision:** [PRODUCT-VISION.md](PRODUCT-VISION.md)
- **How it works:** [HOW-IT-WORKS.md](HOW-IT-WORKS.md)
- **Evidence:** [docs/current-proof.md](docs/current-proof.md)
- **Architecture:** [docs/architecture.md](docs/architecture.md)
- **Roadmap:** [ROADMAP.md](ROADMAP.md)
- **Expanded agent context:** [FOR-AI-AGENTS.md](FOR-AI-AGENTS.md)

---

## Why Cloudberry exists

AI makes it possible to have more work happening in parallel.

That also creates more places for context to disappear.

Cloudberry is an attempt to make the opposite happen:

**the more work your tools and agents do, the easier it should become to understand your projects — not harder.**

Humans think.  
Agents work.  
Tools act.  
History accumulates.

And when you return, everything is still where it belongs.

---

## Come argue with us

Cloudberry is early enough that product ideas can still change its shape.

We are interested in people thinking about:

- product and interaction design;
- spatial / graph interfaces;
- frontend;
- agent workflows;
- architecture;
- creative-tool integrations;
- experiments that turn assumptions into evidence.

If the idea is interesting, send this repository to your own AI agent and ask it to inspect the project.

Then come argue with us about how this should work.

See [CONTRIBUTING.md](CONTRIBUTING.md).

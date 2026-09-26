# ☁ Cloudberry

> A living workspace for humans, projects, tools, and AI agents.

**CURRENT:** Newspaper · **STATUS:** Early / experimental

Your AI agents can work while you are away. Cloudberry makes sure their work still makes sense when you come back.

It keeps projects understandable across chats, tools, models, and time—so you can see what happened, trust what is true, and continue from the right place.

Open it in the morning like a newspaper for your projects.

> **По-русски:** Cloudberry сохраняет историю и контекст работы людей и AI-агентов. Утром вы открываете свои проекты как газету: видите, что произошло, и сразу возвращаетесь к действию.

## Open your projects like a newspaper

```text
GOOD MORNING

WHAT HAPPENED WHILE YOU WERE AWAY?

Graph UI
Code Engine v0.4 merged
01:12

Character Project
Render completed
03:44

Minecraft Server
Server went offline
05:06
```

This is not a dashboard to monitor. It is a way back into the work.

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

A story tells you what changed. One step deeper shows where it belongs, what evidence supports it, and where to continue.

## The problem is continuity

AI can already write code, research questions, render assets, watch services, and complete tasks. But the work falls apart between:

```text
Chats · Git · IDE · Terminal · Files · Tools · Agents · Human memory
```

After a few hours—or a few days—the difficult questions are no longer about generating more work:

- What happened?
- What is actually true?
- Where does it belong?
- Where do I continue?

Cloudberry gives projects continuity. Activity becomes history; history becomes context; context leads back to action.

## What Cloudberry is

```text
HUMAN / AGENTS / TOOLS
          ↓
        ACTIVITY
          ↓
        JOURNAL
          ↓
 ┌────────┼────────┐
 ↓        ↓        ↓
NEWS     MAP     STATE
          ↓
       THREAD
          ↓
       ACTION
```

The Journal preserves project activity. The Newspaper explains meaningful changes. The map locates them. Current state describes what the facts support. Threads keep each line of work addressable.

These are different views over one history, so a clearer interface does not need to create another version of the truth.

## Why this is different

Cloudberry is not another chat UI, autonomous-agent framework, Jira clone, or dashboard full of status cards.

It is the place where work remains understandable over time.

- **Agents are workers inside the system, not the product itself.**
- An agent saying “done” is a claim; product state needs observable evidence.
- The human owns product direction and consequential decisions.
- A project survives a change of chat, tool, person, or model.
- Reading a summary should always lead back to context and action.

```text
ROLE ≠ PERSON ≠ MODEL
```

A stable role—coordinator, architect, researcher, implementer, news editor—can be performed by different people or models without erasing the history of the work.

## What already works

The complete Cloudberry product does not exist yet. Focused experiments have established a foundation.

### PROVEN

- **Code Engine MVP:** the same implementation contract can be given to different agents and checked with shared verification rules.
- **Computed Model Map:** navigation can be a projection instead of a duplicated source of truth.
- **Live Journal path:** `activity → event → journal → reload → projection` passed Review 1 with **8/8 checks**.
- **Event contract v1:** project, thread, run, origin, and thread parentage support the tested model while facts remain distinguishable from interpretations.

### CURRENT

**Newspaper** — turn journaled activity into a calm, trustworthy morning edition, then lead each story back to its project context.

### LATER

- project and thread navigation;
- the workspace from context to action;
- multi-agent integration;
- external development, creative, server, and automation tools.

See [Current proof](docs/current-proof.md) for the exact boundary between proven, experimental, and vision.

## For AI agents

If a user gave you this repository and asked you to understand Cloudberry, start here. This README contains the minimum project briefing; you do not need a separate introduction before discussing the project.

```text
MISSION
Preserve real project activity and turn it into
addressable, trustworthy context for people and agents.

CURRENT MILESTONE
Newspaper.

CORE MODEL
PROJECT → THREAD → RUN → EVENT → JOURNAL → PROJECTION

VISION
A living workspace where many projects remain understandable
while people, agents, and tools continue working over time.
```

### Working rules

1. Do not confuse vision with implemented behavior.
2. Keep facts and interpretations distinguishable.
3. Prefer projections over duplicated sources of truth.
4. The human owns product decisions.
5. Do not widen implementation scope silently.
6. Load context progressively: `MAP → AREA → LOCAL CONTEXT → TASK`.
7. Do not casually rewrite proven baselines.

Treat agent completion messages as claims that need evidence. Keep runs inside their thread unless a reviewed contract explicitly changes that rule. Preserve the distinction `ROLE ≠ PERSON ≠ MODEL`.

### Need more context?

- **Evidence:** [docs/current-proof.md](docs/current-proof.md)
- **Product:** [PRODUCT-VISION.md](PRODUCT-VISION.md)
- **Model:** [HOW-IT-WORKS.md](HOW-IT-WORKS.md)
- **Architecture:** [docs/architecture.md](docs/architecture.md)
- **Roadmap:** [ROADMAP.md](ROADMAP.md)
- **Expanded agent operating context:** [FOR-AI-AGENTS.md](FOR-AI-AGENTS.md)

Choose the smallest document relevant to the task before loading more context.

## Come argue with us

Cloudberry is early enough that a sharp question or small experiment can change the product.

We need people interested in:

- product and UX;
- frontend;
- agent workflows;
- architecture;
- integrations;
- experiments that turn assumptions into evidence.

If this sounds useful, send this repository to your agent, let it inspect the idea, and then come argue with us about how it should work.

Start with [Contributing](CONTRIBUTING.md), or open an issue with the problem you see, why it matters, and what would change.

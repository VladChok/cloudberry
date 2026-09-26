# Cloudberry

> **RU:** Cloudberry — это рабочее пространство, где проекты сохраняют историю и контекст, а люди и AI-агенты могут продолжать работу с того места, где она остановилась. Первый интерфейс — утренняя газета: что произошло, почему это важно и куда перейти, чтобы действовать дальше.

## Your projects should still make sense in the morning

AI agents can write code, research a question, render an asset, or watch a server. The hard part begins after the work: activity is scattered across chats, terminals, files, Git, tools, agents, and human memory.

After a few hours—or a few days—it becomes difficult to answer simple questions:

- What actually happened?
- What was completed, and what was only suggested?
- Who or what did the work?
- Which project and line of work did it belong to?
- Where can a person review it and continue?

Cloudberry is a workspace between people, projects, tools, and AI agents. It turns fragmented activity into a durable project history, then presents that history as useful views.

## Start with the Newspaper

The first Cloudberry experience is a morning newspaper for your own projects:

```text
GOOD MORNING

WHAT HAPPENED WHILE YOU WERE AWAY?

Graph UI
Code Engine v0.4 merged
01:12

Character Project
Render completed
03:44

BCH
New campaign assets exported
04:18

Minecraft Server
Server went offline
05:06
```

Each story is an entrance back into the work:

```text
READ → OPEN → PROJECT / THREAD → CONTEXT → CONTINUE WORK
```

The Newspaper is not the source of truth. It is one projection of recorded activity, designed for reading before acting.

## One history, several useful views

```text
HUMAN / AGENTS / TOOLS
          ↓
        EVENTS
          ↓
        JOURNAL
          ↓
   ┌──────┼───────────┐
   ↓      ↓           ↓
NEWS   MODEL MAP   CURRENT STATE
   └──────┴─────┬─────┘
                ↓
        PROJECT / THREAD
                ↓
         CONTINUE WORK
```

The Journal records what happened. The Newspaper, map, and current state are replaceable views computed from that history. Projects contain threads: meaningful branches of work that may be nested and may outlive any single agent run.

Read [How it works](HOW-IT-WORKS.md) for the concepts without database-level detail.

## Why this is not another agent framework

Cloudberry is not primarily a system for making an agent more autonomous. It is the place where work remains understandable across people, agents, models, tools, and time.

- Agents are workers inside the system, not the product itself.
- A model saying “done” is a claim; product state needs evidence.
- Roles remain stable even when the person or model performing them changes.
- Views are derived from one history instead of becoming competing sources of truth.
- The human keeps product decisions and can move from a summary back to the exact working context.

## What has been proven

The full Cloudberry product does not exist yet. Focused experiments have established several foundations:

- **Code Engine MVP:** two different agents can receive the same implementation contract and be evaluated against one shared rule model.
- **Model Map:** a navigational map can be a computed projection rather than a second source of truth.
- **Journal Review 1:** a live `activity → event → journal → reload → projection` path passed all 8 checks.
- **Event contract v1:** project, thread, run, origin, and thread parentage are sufficient to rebuild the tested structure while keeping facts separate from interpretations.

The evidence boundary is documented in [Current proof](docs/current-proof.md).

## What we are building now

The current product slice is the **Newspaper**: turning journaled events into a calm, readable account of project activity and providing a route back into context and action.

Later slices connect the Newspaper to thread navigation, a working context, multi-agent coordination, and external tools. See the intentionally short [Roadmap](ROADMAP.md).

## Explore the project

- [Product vision](PRODUCT-VISION.md) — the human experience Cloudberry is trying to create.
- [How it works](HOW-IT-WORKS.md) — the small conceptual model behind it.
- [Architecture](docs/architecture.md) — the principles that should survive implementation changes.
- [Current proof](docs/current-proof.md) — what is proven, experimental, and still vision.
- [For AI agents](FOR-AI-AGENTS.md) — the shortest reliable briefing for an agent joining the project.
- [Contributing](CONTRIBUTING.md) — ways to help without ceremony.

## Join in

Cloudberry is early enough that a good question can change the product. If the idea resonates, open an issue with the problem you see, the change you imagine, and why it would help. Product thinking, interaction design, architecture, frontend work, agent workflows, integrations, and small experiments are all welcome.

If you are bringing an AI agent, give it this instruction:

> Read `FOR-AI-AGENTS.md` and the files it references. Then help us continue Cloudberry.

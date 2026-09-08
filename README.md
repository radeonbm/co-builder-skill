# Co-builder / 合作者

> Keep the vision human. Let the AI own the work.

Most AI collaboration fails in one of two ways: the AI turns an unfinished idea into a questionnaire, or it keeps asking about ordinary details after the human has already made the important decisions.

**Co-builder** is an intent-first Agent Skill for working with AI coding agents. It helps an agent preserve the human's vision while taking as much useful initiative as possible.

It is not about maximum autonomy. It is about **maximum useful autonomy without losing human intent**.

[中文说明](README.zh-CN.md) · [Install guide](INSTALL.md)

## How it works

The user starts wherever they are. No mode picker. No intake form.

- **Co-discovery** — When the direction is clear but the answer is not, the AI explores, tests assumptions, and helps narrow the decision.
- **Build My Vision** — When the intended result is already clear, the AI aligns on outcome, boundaries, and acceptance criteria, then works independently inside that agreement.

The two states can change naturally. Reopening a central decision is not failure; it simply means that part of the work needs to be explored again.

## What stays human, what moves to the AI

| Human owns | AI owns |
| --- | --- |
| Intended outcome, red lines, and material tradeoffs | Exploration, methods, execution, and verification |
| Decisions that change direction or create commitments | Ordinary implementation details within the agreed boundary |
| Final judgment on the vision | Honest evidence, deviations, and limitations |

For longer work, the agent keeps a compact internal brief: the human-owned vision, confirmed facts, reversible assumptions, shared boundaries, and the current next move. It uses that brief for continuity, not as a form for the user to maintain.

## When the AI should ask

Inside the agreed boundary, the AI should keep moving. It should pause before a choice would materially change the outcome or constraints, expand the scope, create cost or an external commitment, handle sensitive data beyond the stated purpose, or make an unauthorized irreversible change.

At that point, it should explain the trigger, viable options, its recommendation, and any safe work it can continue meanwhile.

## What this is not

- Not a scorecard for the user's clarity, idea, or progress.
- Not a mandatory workflow for tiny tasks.
- Not an execution engine or a substitute for permission controls.

## Supported clients

The source uses the Agent Skills format and is designed for Codex, Cursor, Claude Code, and Gemini CLI. See the [install guide](INSTALL.md) for the appropriate folder or command for each client.

## Repository layout

```text
.agents/skills/ai-collaboration-protocol/
  SKILL.md                 # Collaboration rules for the agent
  references/templates.md  # Compact working formats
  agents/openai.yaml       # Catalog metadata for Codex
tests/conversation-cases.md # Natural-conversation regression cases
```

## Use it

Start naturally:

> I have an idea, but I am not sure what it should become yet.

Or be direct:

> I know what I want. Understand the boundaries first, then take it forward on your own.

In Codex, you can also invoke it explicitly:

```text
$ai-collaboration-protocol help me with this task.
```

## Status

This is an intentionally small, usable v0.1. The best next step is real work: use it, notice where it helps or interrupts, and improve it from evidence rather than adding process for its own sake.

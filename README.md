# AI 合作者 / AI Co-builder

> 愿景仍然属于人，让 AI 把工作真正往前推进。
> Keep the vision human. Let the AI own the work.

和 AI 合作常见两种不舒服：想法还没成形，它就丢来一张需求问卷；方向已经说清，它却不断确认普通细节，或者悄悄替你改了主意。

Most AI collaboration fails in one of two ways: the AI turns an unfinished idea into a questionnaire, or it keeps asking about ordinary details after the human has already made the important decisions.

**AI 合作者**是一份给 AI 编程客户端使用、以人的意图为先的协作 Skill。它让 AI 在不丢失人的意图前提下，尽可能主动地探索、执行和验证。

**AI Co-builder** is an intent-first Agent Skill for working with AI coding agents. It helps an agent preserve the human's vision while taking as much useful initiative as possible.

追求的不是最大自动化，而是**最大程度的有效自主权**。

It is not about maximum autonomy. It is about **maximum useful autonomy without losing human intent**.

[完整中文说明](README.zh-CN.md) · [安装 / Install](INSTALL.md)

## 如何协作 / How it works

用户从自己现在最确定的地方开始，不需要选择模式，也不用填写表格。

The user starts wherever they are. No mode picker. No intake form.

- **一起找答案 / Co-discovery** — 当方向已经有了、但答案和关键选择尚未确定时，AI 主动探索、验证假设、帮助收敛。 When the direction is clear but the answer is not, the AI explores, tests assumptions, and helps narrow the decision.
- **实现我的愿景 / Build My Vision** — 当结果已经比较清楚时，AI 先自然地对齐目标、边界与验收标准，再在范围内自主推进。 When the intended result is already clear, the AI aligns on outcome, boundaries, and acceptance criteria, then works independently inside that agreement.

重新打开关键决定不是失败，只是说明这一部分值得重新一起探索。

The two states can change naturally. Reopening a central decision is not failure; it simply means that part of the work needs to be explored again.

## 谁负责什么 / What stays human, what moves to the AI

| Human owns | AI owns |
| --- | --- |
| Intended outcome, red lines, and material tradeoffs | Exploration, methods, execution, and verification |
| Decisions that change direction or create commitments | Ordinary implementation details within the agreed boundary |
| Final judgment on the vision | Honest evidence, deviations, and limitations |

人负责愿景、红线与关键取舍；AI 负责探索、方法、执行与验证。

For longer work, the agent keeps a compact internal brief: the human-owned vision, confirmed facts, reversible assumptions, shared boundaries, and the current next move. It uses that brief for continuity, not as a form for the user to maintain.

## AI 什么时候应该来问人 / When the AI should ask

在约定边界内，AI 应自己往前推进。只有当一个选择会实质改变目标或约束、扩大范围、引入费用或对外承诺、超出目的地处理敏感信息，或造成未经授权的不可逆影响时，它才应暂停。

Inside the agreed boundary, the AI should keep moving. It should pause before a choice would materially change the outcome or constraints, expand the scope, create cost or an external commitment, handle sensitive data beyond the stated purpose, or make an unauthorized irreversible change.

At that point, it should explain the trigger, viable options, its recommendation, and any safe work it can continue meanwhile.

## 它不是什么 / What this is not

- Not a scorecard for the user's clarity, idea, or progress.
- Not a mandatory workflow for tiny tasks.
- Not an execution engine or a substitute for permission controls.

它不为用户的想法、清晰度或进度打分；不为小任务强加流程；也不替代权限控制。

## 支持的客户端 / Supported clients

面向 Codex、Cursor、Claude Code 和 Gemini CLI。

The source uses the Agent Skills format and is designed for Codex, Cursor, Claude Code, and Gemini CLI. See the [install guide](INSTALL.md) for the appropriate folder or command for each client.

## Repository layout

```text
.agents/skills/ai-collaboration-protocol/
  SKILL.md                 # Collaboration rules for the agent
  references/templates.md  # Compact working formats
  agents/openai.yaml       # Catalog metadata for Codex
tests/conversation-cases.md # Natural-conversation regression cases
```

## 开始使用 / Use it

直接自然地开始：

> 我有一个想法，但还没想清楚它应该做成什么。

Start naturally:

> I have an idea, but I am not sure what it should become yet.

Or be direct:

> I know what I want. Understand the boundaries first, then take it forward on your own.

In Codex, you can also invoke it explicitly:

```text
$ai-collaboration-protocol help me with this task.
```

## 当前状态 / Status

这是一个刻意保持轻量、但可以真实使用的 v0.1。最值得做的不是增加流程，而是拿真实任务试用，根据证据改进它。

This is an intentionally small, usable v0.1. The best next step is real work: use it, notice where it helps or interrupts, and improve it from evidence rather than adding process for its own sake.

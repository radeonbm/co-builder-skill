# Install Co-builder

The source of truth is the `ai-collaboration-protocol` folder under `.agents/skills/`. Keep `SKILL.md`, `references/`, and `agents/` together when copying it.

## Codex

Copy `.agents/skills/ai-collaboration-protocol/` to your global Codex skills folder:

- Windows: `%USERPROFILE%\.codex\skills\ai-collaboration-protocol\`
- macOS / Linux: `~/.codex/skills/ai-collaboration-protocol/`

Restart Codex if the skill does not appear immediately. Invoke it with `$ai-collaboration-protocol`, or start a substantive task naturally and let Codex select it when relevant.

## Cursor

Cursor discovers project skills from `.agents/skills/`. Clone this repository and keep that folder in the project root, or copy the skill to your global `~/.agents/skills/` folder. Cursor can also import skills from a GitHub repository through **Customize → Rules → Add Rule → Remote Rule (GitHub)**.

## Claude Code

Copy the entire source folder to one of these locations:

- Project-only: `.claude/skills/ai-collaboration-protocol/`
- Global: `~/.claude/skills/ai-collaboration-protocol/`

Start Claude Code, then invoke `/ai-collaboration-protocol` or describe a task that matches the skill's description.

## Gemini CLI

Gemini CLI recognizes the `.agents/skills/` directory in a workspace. Clone this repository or copy its `.agents/skills/` directory into your workspace, then use `/skills list` to confirm discovery.

For local development, Gemini CLI can link the source folder directly:

```text
gemini skills link .agents/skills/ai-collaboration-protocol
```

## Other clients

If a client does not yet support Agent Skills, use `SKILL.md` as a project rule or reusable instruction. The protocol remains useful, but automatic selection and on-demand references depend on the client.

# 03 — Codex vibe-coding basics

> New to AI agents, LLMs, prompts, or permission levels? Read `02_codex_and_ai_foundations.md` first.

## Mental model

Codex is not just a text generator. Treat it like an eager junior coding agent that can inspect the repo, make changes, run checks, and explain its work — fast and tireless, but it needs you steering.

Your job is the fun part: steer, review, test, and keep the scope tight.

## The loop

```text
1. Give a small goal.
2. Provide context.
3. Set constraints.
4. Define done.
5. Let Codex implement.
6. Inspect the diff.
7. Run the app/tests.
8. Ask Codex to explain.
9. Ask for the next small improvement.
```

## Prompt pattern

```text
Goal:
[Specific feature]

Context:
[Relevant project / files / design intent]

Constraints:
[Tech, scope, style, legal/IP, testing]

Done when:
[Observable completion criteria]
```

## Good prompting habits

These are the habits that keep your runs smooth:

- One feature per prompt.
- Use concrete examples.
- Tell Codex what not to do.
- Ask for a plan before large changes.
- Ask Codex to explain its diff.
- Make Codex add tests for rules logic.
- Do not accept code without running it.

## Bad prompting habits

These are the vague mana-sinks that send Codex off the rails. Don't do these:

```text
Build the whole game.
Make it like Arena.
Add everything.
Fix all bugs.
Make it better.
```

## Review prompts

Use these constantly.

```text
Explain the code you just wrote like I am new to coding. Focus on what changed and why.
```

```text
Review your own changes. Look for bugs, unclear names, duplicated logic, and rules edge cases. Do not change code yet. Give findings first.
```

```text
Refactor this for readability without changing behavior. Keep the same tests passing.
```

```text
Add tests for the rules logic affected by this change. Prefer testing pure functions over UI.
```

```text
This behavior is wrong: [describe behavior]. Find the likely cause, explain it, then make the smallest safe fix.
```

## Big-change planning prompt

```text
/plan

I want to add [feature]. First inspect the project, then propose a step-by-step plan. Do not write code until the plan is clear.
```

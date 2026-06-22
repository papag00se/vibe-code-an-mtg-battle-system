# 02 — Codex and AI foundations

Read this before you write a single prompt. If you have never used an AI coding tool, start here. The rest of the tutorial assumes you understand these words.

## Why this page exists

The other lessons tell you *what to build*. This page tells you *what the tool is* and *how to talk to it safely*. Five minutes here saves a lot of confusion later.

## The vocabulary, in plain language

| Term | Plain meaning |
|---|---|
| LLM | A "large language model" — software trained on huge amounts of text and code that predicts useful next words. It is the engine. |
| Inference | One run of that engine: you give it text, it gives you text back. Every time Codex "thinks," it is doing inference. |
| Model | A specific trained engine with a name and version (for example, a GPT-class model). Newer models are usually more capable. |
| Token | A chunk of text the model reads and writes in (roughly a word-piece). Models have a limit on how many tokens they can consider at once. |
| Context | Everything the model can currently "see": your prompt, the files it has read, and the recent conversation. |
| Prompt | The instructions you give. Your main lever of control. |
| Agent | An LLM that can also *take actions* — read files, edit code, run commands — not just chat. Codex is an agent. |
| Codex | The coding agent you drive in this tutorial. It lives in your terminal/editor, reads your repo, and proposes changes. |

## LLM vs. agent: the key difference

A plain chatbot only produces text. You copy and paste it yourself.

An **agent** can act on your project directly:

```text
1. Read files in your repository.
2. Propose or make edits.
3. Run commands (install, build, test).
4. Read the results and try again.
```

That power is why agents are useful — and why you keep a hand on the wheel. You are the senior engineer; Codex is a fast, eager junior who has read a lot but has never seen *your* project until you show it.

## How you interact with Codex

You work in a loop of short turns. You type a request, Codex responds (often by reading files or making edits), you review, then you steer again.

```text
You:    a small, specific request
Codex:  reads context, proposes a plan or a change
You:    inspect the diff, run it, give feedback
Codex:  adjusts
```

This back-and-forth is the whole job. The next page (`03_codex_vibe_coding_basics.md`) drills into the prompting habits that make this loop work.

## Prompts are how you steer

A prompt is just your instructions, but specific prompts beat vague ones every time.

```text
Vague:    "Make a card search."
Specific: "Add a search box that calls the Scryfall API by card
           name, shows a loading state, shows an error state, and
           renders the card image from the returned image URL."
```

Good prompts state the **goal**, the **context**, the **constraints**, and what **done** looks like. You will use that four-part pattern throughout this tutorial.

## Permission and approval levels

An agent that can run commands needs guardrails. Most coding agents, Codex included, let you choose **how much it can do without asking you first**. The exact names differ by version, but they fall into three tiers:

| Tier | What it means | Good for |
|---|---|---|
| Read-only / suggest | Codex can read files and *propose* edits and commands, but you approve each action. | Learning, unfamiliar code, anything risky. |
| Auto-edit / on request | Codex edits files on its own but asks before running commands. | Steady work once you trust the task. |
| Full-auto ("YOLO") | Codex reads, edits, and runs commands without stopping to ask. | Fast iteration on throwaway or fully backed-up work — only. |

### About "YOLO" / full-auto mode

"YOLO mode" is the nickname for letting the agent run with **no approval prompts**. It is fast and it is tempting. Treat it with respect:

- Only use it inside a git repository where everything is committed, so you can undo anything with one command.
- Never use it on important files, secrets, or a machine you cannot afford to have changed.
- Prefer it for small, sandboxed, reversible tasks — not for "build the whole app while I get coffee."

```text
Rule of thumb:
If you would not let a brand-new intern run that command
unsupervised on your laptop, do not let an agent do it in
full-auto either.
```

For this tutorial, **start in the approval-required tier.** Watch what Codex does, learn the patterns, and only loosen permissions once you can predict its behavior.

## Habits that keep you in control

- Commit early and often, so every change is reversible.
- Read the diff before you accept it. Do not merge code you have not looked at.
- Run the app and the tests yourself; never trust "it should work."
- Ask Codex to explain its own changes in beginner terms.
- Keep `AGENTS.md` in the repo root — it gives Codex your standing rules on every turn.

## What to remember

```text
LLM        = the engine that predicts text.
Inference  = one run of that engine.
Agent      = an LLM that can also act on your project.
Codex      = the coding agent you steer here.
Prompt     = your instructions, your main control.
Permissions= how much it may do before asking. Start strict.
```

You are ready. Continue to `03_codex_vibe_coding_basics.md`.

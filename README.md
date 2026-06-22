# Build an MtG Battle System with AI!

Ever wanted to learn to code *and* understand exactly how a Magic: The Gathering turn really works? Do both at once. In this walkthrough you and an AI coding agent (Codex) team up to build a real MtG battle system from scratch — one small, satisfying step at a time.

The app you'll build is called **Untap**: a free, unofficial MtG rules sandbox. You are not shipping a commercial game. You're using Magic as the (very fun) excuse to learn the real stuff — APIs, React, TypeScript, state machines, zones, mana, combat, the stack, priority, testing, and UX. By the end you'll have working software *and* a much deeper feel for the rules.

No computer science degree required. If you can describe what you want, you can build it here.

## New to AI coding agents?

Start with [`docs/02_codex_and_ai_foundations.md`](docs/02_codex_and_ai_foundations.md). In plain language it explains what an LLM is, what an "agent" actually does, how prompts steer it, and what permission levels (including the spicy full-auto "YOLO" mode) really mean — before you run a single command.

Want the big picture first? Open the live visual map at **https://papag00se.github.io/vibe-code-an-mtg-battle-system/**, or open `walkthrough.html` locally in any browser.

## How to use this

1. **Get this walkthrough onto your computer.** The first step is simply getting the project onto your machine — and you can just ask your AI agent to do it for you:

   ```text
   Clone https://github.com/papag00se/vibe-code-an-mtg-battle-system and open it so we can start building.
   ```

   Prefer to do it by hand? Same thing, in a terminal:

   ```bash
   git clone https://github.com/papag00se/vibe-code-an-mtg-battle-system.git
   cd vibe-code-an-mtg-battle-system
   ```

2. Start Codex in the project folder.
3. Read [`docs/02_codex_and_ai_foundations.md`](docs/02_codex_and_ai_foundations.md) to get your bearings.
4. Make your first build move: open `prompts/01_bootstrap_repo.md` and paste it into Codex.
5. Keep `AGENTS.md` in the root — it's the house rulebook Codex reads on every turn.
6. Work through the lessons in order. Resist the urge to skip to combat. (We know. We get it. Still: in order.)

## What you'll build

Untap grows one feature at a time. Along the way it gains:

- card search powered by Scryfall
- card display using Scryfall image URLs
- a "what does this card even mean?" anatomy explainer
- battlefield zones
- two-player local state
- turn phases
- lands and mana
- spell casting
- a visual stack
- a priority / pass system
- simplified combat
- bite-sized keyword lessons
- rules tests you can trust
- an event log that narrates what just happened
- a panel of official learning resources

## Keep it friendly: scope

Here's the honest framing — this is a learning toy, and that's the whole point:

```text
A free, unofficial, educational coding tutorial and MtG rules-learning sandbox.
```

What Untap is *not* (and shouldn't pretend to be):

```text
A full public MTG Arena replacement, paid product, proxy tool, card-image archive, or online multiplayer game client.
```

Staying in this lane keeps things fun, legal, and respectful of Wizards of the Coast. Win-win-win.

## Suggested stack

Beginner-friendly on purpose:

```text
Vite
React
TypeScript
Vitest
Plain CSS
Scryfall API
localStorage
```

## The core loop

This rhythm is the whole game. Repeat until delighted:

```text
Prompt Codex -> read the diff -> run the app/tests -> ask Codex to explain -> make one improvement -> repeat
```

## Your first move

Open `prompts/00_clone_the_repo.md`, paste the clone prompt into Codex, and you're off — bootstrap the app with `prompts/01_bootstrap_repo.md` and watch Untap come to life. See you on the battlefield.

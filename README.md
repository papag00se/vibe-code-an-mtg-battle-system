# Stack Tutor: A Magic Rules Coding Lab

A repository-ready walkthrough for using Codex to build a free, unofficial Magic: The Gathering rules-learning and vibe-coding tutorial.

The goal is not to build a commercial game client. The goal is to teach coding through a motivating MTG-shaped project: APIs, React, TypeScript, state machines, game zones, mana, combat, stack resolution, priority, testing, and UX.

## Use this ZIP

1. Create a new empty GitHub repository or local folder.
2. Copy these Markdown files into the repository root.
3. Start Codex in the repository.
4. Begin with `prompts/00_bootstrap_repo.md`.
5. Keep `AGENTS.md` in the root so Codex inherits the project standards.
6. Work through the lesson files in order.

## Project output

Codex should build a local web app called:

```text
Stack Tutor
```

The app should eventually include:

- card search through Scryfall
- card display using Scryfall image URLs
- card anatomy explainer
- battlefield zones
- two-player local state
- turn phases
- lands and mana
- spell casting
- visual stack
- priority/pass system
- simplified combat
- keyword lessons
- rules tests
- event log
- WotC resource panel

## Scope boundary

Acceptable framing:

```text
A free, unofficial, educational coding tutorial and MTG rules-learning sandbox.
```

Avoid framing it as:

```text
A full public MTG Arena replacement, paid product, proxy tool, card-image archive, or online multiplayer game client.
```

## Suggested implementation stack

```text
Vite
React
TypeScript
Vitest
Plain CSS
Scryfall API
localStorage
```

## Core workflow

```text
Prompt Codex -> inspect diff -> run app/tests -> ask Codex to explain -> make one improvement -> repeat
```

## First Codex command

Open `prompts/00_bootstrap_repo.md` and paste it into Codex.

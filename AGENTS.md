# AGENTS.md

## Project

This repository is the tutorial **"Build an MtG Battle System with AI!"** The app it builds is called **Untap** — a free, unofficial Magic: The Gathering rules-learning sandbox, made for vibe-coding practice.

The whole point is teaching programming through MTG concepts, in a friendly, beginner-readable way. Untap is not an official Wizards of the Coast product. It is not a commercial game client. It is not intended to replace MTG Arena, Magic Online, SpellTable, or official Wizards products.

## Stack

- Vite
- React
- TypeScript
- Vitest
- Plain CSS unless explicitly changed
- Scryfall API for card lookup and card image URLs

## Commands

Use these commands unless the package manager or project setup changes:

```bash
npm install
npm run dev
npm run build
npm test
```

## Directory conventions

```text
src/
  api/          Scryfall and external API wrappers
  components/   React UI components
  data/         local sample decklists and lesson content
  game/         pure rules/state logic
  lessons/      lesson metadata displayed inside the app
  tests/        Vitest tests for pure game logic
```

## Engineering rules

- Keep the code beginner-readable.
- Prefer explicit names over clever abbreviations.
- Keep React UI separate from rules logic.
- Put game rules and state transitions in pure functions under `src/game`.
- Add tests for rule changes.
- Preserve existing tests unless they are incorrect and the change is explained.
- Do not add dependencies unless there is a clear need.
- Do not bundle or download card images locally.
- Use Scryfall image URLs directly.
- Avoid implementing every MTG edge case. This is a learning lab.
- Add event-log messages for game actions so learners can understand state changes.

## MTG/WotC constraints

- Include an unofficial fan-content notice in the app footer.
- Do not use Wizards logos or trademarks as app branding.
- Do not claim endorsement, sponsorship, partnership, or official status.
- Do not create a paid app, paid access, account-gated public product, proxy printing tool, ranking/matchmaking system, or full online multiplayer client.
- Do not remove copyright/trademark notices that appear inside WotC-provided card images.
- Use WotC resources as references; do not paste large sections of rules text into the app.

## Fan-content notice

Use this footer text:

```text
Untap is unofficial Fan Content permitted under the Wizards of the Coast Fan Content Policy. Not approved/endorsed by Wizards. Portions of the materials used are property of Wizards of the Coast. © Wizards of the Coast LLC.
```

## Definition of done

A feature is done only when:

- the app runs locally
- TypeScript passes
- relevant tests pass
- the UI can be manually tested
- the event log explains important state changes
- the implementation stays within the project scope
- the feature remains educational, not commercial-client-oriented

## Codex behavior

When asked to implement a feature:

1. Inspect relevant files first.
2. Make the smallest coherent change.
3. Explain what changed.
4. Explain how to test it.
5. Mention any skipped edge cases.

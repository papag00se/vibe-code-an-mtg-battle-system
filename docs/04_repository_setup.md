# 04 — Repository setup

Time to lay out your battlefield. This page is the blueprint for Untap — the tools you'll use and where every file lives. You don't have to memorize it; you just need to know it exists so you and Codex are building from the same map.

## Target stack

These are your tools of the trade — all beginner-friendly on purpose:

```text
Vite
React
TypeScript
Vitest
Plain CSS
Scryfall API
```

## Root files

These live at the top of the repo — the essentials Untap needs to boot:

```text
README.md
AGENTS.md
package.json
index.html
vite.config.ts
tsconfig.json
```

## Source layout

Here's where the magic happens. Don't panic at the size — Untap grows into this one file at a time, lesson by lesson. By the end it'll feel like home:

```text
src/
  main.tsx
  App.tsx
  api/
    scryfall.ts
  components/
    AppShell.tsx
    FooterNotice.tsx
    CardSearch.tsx
    CardViewer.tsx
    CardAnatomyPanel.tsx
    Battlefield.tsx
    PlayerPanel.tsx
    ZoneView.tsx
    StackView.tsx
    PhaseBanner.tsx
    ManaPool.tsx
    EventLog.tsx
    ResourcePanel.tsx
  data/
    starterDecks.ts
    lessonCards.ts
    keywordLessons.ts
    resourceLinks.ts
  game/
    types.ts
    startGame.ts
    zones.ts
    turn.ts
    mana.ts
    casting.ts
    stack.ts
    combat.ts
    keywords.ts
    winConditions.ts
  tests/
    startGame.test.ts
    zones.test.ts
    turn.test.ts
    mana.test.ts
    casting.test.ts
    stack.test.ts
    combat.test.ts
    keywords.test.ts
```

## Package scripts

The four commands you'll lean on every day — dev server, build, and tests:

```json
{
  "scripts": {
    "dev": "vite",
    "build": "tsc -b && vite build",
    "test": "vitest run",
    "test:watch": "vitest"
  }
}
```

## First commit target

This is your first real milestone — your opening play. When this commit lands, you've got a running app and something to be proud of. It should include:

- Vite React TypeScript app
- footer notice
- home screen
- placeholder battlefield
- resource panel stub
- AGENTS.md
- passing build

## Dependency policy

Travel light. Start with the minimum and add a dependency only when you have a clear reason — every package you skip is one less thing hiding the mechanics you're here to learn.

Allowed early:

```text
@vitejs/plugin-react
vite
react
react-dom
typescript
vitest
```

Hold off on these for now — they hide the very mechanics you want to understand:

```text
drag-and-drop libraries
state-management libraries
component libraries
animation libraries
routing libraries
```

The point is to learn the mechanics, not hide them behind dependencies.

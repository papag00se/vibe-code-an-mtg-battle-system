# 03 — Repository setup

## Target stack

```text
Vite
React
TypeScript
Vitest
Plain CSS
Scryfall API
```

## Root files

```text
README.md
AGENTS.md
package.json
index.html
vite.config.ts
tsconfig.json
```

## Source layout

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

The first completed commit should include:

- Vite React TypeScript app
- footer notice
- home screen
- placeholder battlefield
- resource panel stub
- AGENTS.md
- passing build

## Dependency policy

Start with minimal dependencies. Add more only when there is a clear reason.

Allowed early:

```text
@vitejs/plugin-react
vite
react
react-dom
typescript
vitest
```

Avoid early:

```text
drag-and-drop libraries
state-management libraries
component libraries
animation libraries
routing libraries
```

The point is to learn the mechanics, not hide them behind dependencies.

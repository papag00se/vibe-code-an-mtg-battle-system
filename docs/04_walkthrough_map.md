# 04 — Walkthrough map

## Phase list

| Phase | Feature | Coding concept |
|---:|---|---|
| 0 | Bootstrap app | repo setup, Codex workflow |
| 1 | Card search | API calls, JSON, loading/error states |
| 2 | Card anatomy | TypeScript models, conditional rendering |
| 3 | Zones | arrays, object movement, state modeling |
| 4 | Start game | deterministic setup, draw seven |
| 5 | Turn phases | state machines |
| 6 | Lands and mana | resources, validation |
| 7 | Casting spells | legal actions, cost parsing |
| 8 | Stack and priority | LIFO, response windows |
| 9 | Combat | multi-step workflows, damage assignment |
| 10 | Keywords | incremental complexity |
| 11 | Tests | pure-function verification |
| 12 | UX polish | clarity, event log, legal-action hints |
| 13 | Resource panel | official references, learning support |

## Build order

Do not skip directly to combat or stack. The learner needs the progression:

```text
Card search
-> Card anatomy
-> Zones
-> Start game
-> Turn phases
-> Mana
-> Casting
-> Stack
-> Combat
-> Keywords
-> Tests
-> Polish
```

## Milestone 1 — App shell

Done when:

- app runs
- footer notice exists
- home screen exists
- static battlefield is visible

## Milestone 2 — Scryfall search

Done when:

- typing a card name loads card data
- loading state exists
- error state exists
- image renders from URL
- card anatomy panel explains fields

## Milestone 3 — State lab

Done when:

- zones exist
- cards can move between zones
- players have libraries/hands/battlefields/graveyards
- event log records changes

## Milestone 4 — Rule lab

Done when:

- phase system works
- land-per-turn rule works
- mana pool works
- spells can be cast and resolved
- stack resolves last-in-first-out

## Milestone 5 — Battle lab

Done when:

- attackers can be declared
- blockers can be declared
- damage resolves
- lethal damage sends creatures to graveyard
- player life changes

## Milestone 6 — Trust lab

Done when:

- Vitest tests cover core rules
- code is refactored into pure functions
- README explains how to run and test

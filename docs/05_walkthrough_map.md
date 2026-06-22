# 05 — Walkthrough map

This is your battle plan. Untap grows one phase at a time, and each phase teaches a real coding concept while you build a real piece of the game. Glance at the map, then trust the order — it was tuned to keep you winning.

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

We know combat and the stack are the flashy parts. Resist! Each step builds on the last, so follow the progression and everything clicks:

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

First blood: get something on screen you can be proud of.

Done when:

- app runs
- footer notice exists
- home screen exists
- static battlefield is visible

## Milestone 2 — Scryfall search

Now Untap can find real cards. Type a name, watch Magic show up.

Done when:

- typing a card name loads card data
- loading state exists
- error state exists
- image renders from URL
- card anatomy panel explains fields

## Milestone 3 — State lab

Cards start moving between zones. This is where it begins to feel like a game.

Done when:

- zones exist
- cards can move between zones
- players have libraries/hands/battlefields/graveyards
- event log records changes

## Milestone 4 — Rule lab

The real rules come online: phases, mana, casting, and the stack resolving in order. The heart of Magic.

Done when:

- phase system works
- land-per-turn rule works
- mana pool works
- spells can be cast and resolved
- stack resolves last-in-first-out

## Milestone 5 — Battle lab

Time to swing. Creatures attack, blockers step up, and life totals finally start to move.

Done when:

- attackers can be declared
- blockers can be declared
- damage resolves
- lethal damage sends creatures to graveyard
- player life changes

## Milestone 6 — Trust lab

Lock it in. Tests prove your rules really work, so you can keep building with confidence.

Done when:

- Vitest tests cover core rules
- code is refactored into pure functions
- README explains how to run and test

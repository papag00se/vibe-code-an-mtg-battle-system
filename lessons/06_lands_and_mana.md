# Lesson 6 — Lands and mana

## Teaches

- resource systems
- per-turn limits
- validation
- simple cost parsing

## Codex prompt

```text
Goal:
Add lands and mana.

Requirements:
- Detect land cards by type line.
- Allow one land play per turn during main phases.
- Lands enter untapped.
- Clicking an untapped land taps it and adds mana.
- Show mana pool.
- Mana clears when changing phases.
- Show an illegal-action reason when trying to play a second land.

Constraints:
Use simple color symbols as text: W, U, B, R, G, C.
Do not use official mana-symbol art.
Keep cost parsing simple.
Put pure logic in src/game/mana.ts.

Done when:
A player can play one land, tap it for mana, and see mana added to their pool.
A player cannot play a second land in the same turn.
Mana clears at phase changes.
```

## Manual test

- Move a land to hand.
- Play it during first main.
- Tap it for mana.
- Advance phase.
- Confirm mana clears.
- Try to play a second land in the same turn.

## Ask Codex after implementation

```text
Explain how the app enforces one land per turn and why mana clears between phases in this simplified model.
```

# Lesson 6 — Lands and mana

Mana is the fuel of Magic — no lands, no spells. In this lesson you'll teach Untap to recognize land cards, let a player drop one land per turn, and tap it for mana that fills up a mana pool. You'll also enforce your first real rule: no sneaking in a second land. Resource systems and "is this move legal?" checks are everywhere in games, and you're about to build one.

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

Run a land through its whole job and then try to break the rules:

- Move a land to your hand.
- Play it during first main.
- Tap it for mana.
- Advance a phase and confirm the mana pool clears.
- Now try to play a second land in the same turn — and enjoy getting politely told no.

That blocked second land is your validation working exactly as intended.

## Ask Codex after implementation

You just wrote game rules in code. Ask Codex how it pulled that off:

```text
Explain how the app enforces one land per turn and why mana clears between phases in this simplified model.
```

# Lesson 7 — Casting spells

## Teaches

- legal actions
- cost checks
- spell resolution
- permanent vs instant/sorcery movement

## Codex prompt

```text
Goal:
Add basic spell casting.

Requirements:
- Creatures, artifacts, enchantments, planeswalkers, and battles go onto the stack first.
- Instants and sorceries go onto the stack first.
- When a permanent spell resolves, move it to battlefield.
- When an instant or sorcery resolves, move it to graveyard.
- Only allow sorcery-speed spells during the active player's main phase when the stack is empty.
- Allow instants whenever the player has priority.
- Require enough mana to cast a spell.
- Explain illegal actions in the UI.

Constraints:
This is a simplified tutorial model.
Do not implement every edge case.
Put pure logic in src/game/casting.ts.

Done when:
The user can cast a creature and resolve it onto the battlefield.
The user can cast an instant and resolve it to the graveyard.
Casting without enough mana fails with a clear reason.
```

## Manual test

- Play/tap lands.
- Cast a creature.
- Resolve it.
- Cast an instant.
- Resolve it.
- Try casting without enough mana.

## Ask Codex after implementation

```text
Explain the difference between casting a spell, putting it on the stack, and resolving it.
```

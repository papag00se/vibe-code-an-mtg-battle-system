# Lesson 7 — Casting spells

This is the big one. Up to now you've been shuffling cards between zones — now you get to actually *cast* them. By the end of this lesson, Untap will let you tap lands, pay a cost, and watch a spell do its thing. That little jolt when your first creature lands on the battlefield? Enjoy it. You earned it.

## What you'll teach Untap

- which actions are legal, and when
- checking you can actually afford a spell
- how a spell resolves
- where it goes afterward (permanents stay; instants and sorceries take a bow and head to the graveyard)

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

## Try it yourself

Don't take Codex's word for it — go play with it:

- Play and tap some lands.
- Cast a creature.
- Resolve it.
- Cast an instant.
- Resolve it.
- Try casting without enough mana, and check that it tells you why.

## Ask Codex after implementation

```text
Explain the difference between casting a spell, putting it on the stack, and resolving it.
```

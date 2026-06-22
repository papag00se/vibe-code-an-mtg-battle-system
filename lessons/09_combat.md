# Lesson 9 — Combat

This is the part you've been itching to build (we saw you eyeing it). Attacking, blocking, creatures trading blows — combat is where Magic gets loud. It's also a tidy little multi-step workflow, which makes it a great thing to teach a computer. We'll keep it simplified for now and add the fancy stuff later. One step at a time.

## What you'll teach Untap

- a workflow that moves through clear steps
- tracking who's attacking and who's blocking
- working out how much damage lands
- when damage is lethal and a creature goes to the graveyard

## Codex prompt

```text
Goal:
Add a simplified combat tutor.

Requirements:
Combat steps:
- declareAttackers
- declareBlockers
- combatDamage
- endCombat

Rules:
- Only untapped creatures can attack.
- Attacking taps the creature.
- Defending player can block with untapped creatures.
- One blocker may block one attacker in this simplified model.
- Blocked creatures deal damage to each other.
- Unblocked attackers damage the defending player.
- Creatures with damage equal to or greater than toughness go to graveyard.
- Damage clears at end of turn.

Constraints:
Ignore first strike, double strike, trample, menace, protection, ward, and planeswalker attacks for now.
Add those later as lessons.
Put pure logic in src/game/combat.ts.

Done when:
The user can run through a complete combat step with clear event-log messages.
```

## Try it yourself

Stage a little skirmish and see how it plays out:

- Put two creatures on Player A's battlefield.
- Put one creature on Player B's battlefield.
- Enter combat.
- Attack with one creature.
- Block with one creature.
- Resolve damage.
- Confirm the deaths and life changes land the way you'd expect.

## Ask Codex after implementation

```text
Explain combat as a multi-step workflow. Point to the code that stores attackers, blockers, and damage.
```

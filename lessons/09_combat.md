# Lesson 9 — Combat

## Teaches

- multi-step workflows
- attack/block state
- damage calculation
- lethal damage

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

## Manual test

- Put two creatures on Player A battlefield.
- Put one creature on Player B battlefield.
- Enter combat.
- Attack with one creature.
- Block with one creature.
- Resolve damage.
- Confirm death/life changes as appropriate.

## Ask Codex after implementation

```text
Explain combat as a multi-step workflow. Point to the code that stores attackers, blockers, and damage.
```

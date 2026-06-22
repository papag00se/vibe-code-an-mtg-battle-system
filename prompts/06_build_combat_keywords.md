# Prompt 06 — Build combat and first keyword

Time to swing. In this step Untap gets simplified combat plus your very first keyword — flying — so creatures can attack, block, and trade blows. Paste the prompt below into Codex and send some creatures into the red zone.

```text
Goal:
Add simplified combat and the first keyword lesson: flying.

Context:
This teaches multi-step workflows and incremental rule complexity.

Read first:
- lessons/09_combat.md
- lessons/10_keywords.md
- docs/06_rules_engine_spec.md

Requirements:
Combat steps:
- declareAttackers
- declareBlockers
- combatDamage
- endCombat

Combat rules:
- only untapped creatures can attack
- attacking taps the creature
- defending player can block with untapped creatures
- one blocker may block one attacker in this simplified model
- blocked creatures deal damage to each other
- unblocked attackers damage defending player
- lethal damage sends creature to graveyard
- damage clears at end of turn

Keyword:
- detect flying from Oracle text
- detect reach from Oracle text
- flying can be blocked only by flying or reach
- add a short original explanation

Files:
- src/game/combat.ts
- src/game/keywords.ts

Tests:
- attacker legality
- blocking legality
- unblocked damage
- lethal damage
- flying blocker legality

Constraints:
Ignore first strike, double strike, trample, menace, protection, ward, and planeswalker attacks for now.
Do not rewrite unrelated systems.

Done when:
The user can run a complete combat demo and flying affects blocker legality.
npm test passes.
npm run build passes.
```

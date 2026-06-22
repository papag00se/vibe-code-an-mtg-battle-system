# Prompt 04 — Build turns, mana, and casting

```text
Goal:
Add turn phases, lands, mana, and basic spell casting.

Context:
This combines lessons 5, 6, and 7. Keep changes structured by files and add tests.

Read first:
- lessons/05_turn_phases.md
- lessons/06_lands_and_mana.md
- lessons/07_casting_spells.md
- docs/06_rules_engine_spec.md

Requirements:
Turn phases:
- beginning
- firstMain
- combat
- secondMain
- end

Mana:
- detect lands by type line
- one land per turn during main phases
- lands enter untapped
- tapping a land adds mana
- mana clears when phase changes

Casting:
- require enough mana
- spells go onto stack first
- permanent spells resolve to battlefield
- instants/sorceries resolve to graveyard
- sorcery-speed spells only during active player's main phase when stack is empty
- instants can be cast when player has priority

Files:
- src/game/turn.ts
- src/game/mana.ts
- src/game/casting.ts

Tests:
- phase order
- land once per turn
- tap land for mana
- mana clears
- cannot cast without mana
- resolving permanent moves to battlefield
- resolving instant/sorcery moves to graveyard

Constraints:
Simplified tutorial model only.
Explain skipped MTG edge cases.
Do not implement combat yet.
Do not implement full priority yet beyond what is needed.

Done when:
A player can advance phases, play/tap a land, cast a creature, and resolve it.
npm test passes.
npm run build passes.
```

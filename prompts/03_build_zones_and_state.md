# Prompt 03 — Build zones and game state

```text
Goal:
Add Magic-inspired zones and core game-state types.

Context:
This lesson teaches arrays, state movement, and domain modeling. The app is still a learning lab, not a full game client.

Read first:
- lessons/04_zones.md
- docs/06_rules_engine_spec.md

Requirements:
- Create src/game/types.ts.
- Create src/game/zones.ts.
- Add CardData, CardInstance, PlayerState, GameState, ZoneName types.
- Add a small deterministic sample deck.
- Add two players.
- Add library, hand, battlefield, graveyard, exile, and stack zones.
- Add moveCard and drawCard pure functions.
- Add UI buttons to move cards for demonstration.
- Add event-log entries for movement.
- Add tests for drawCard and moveCard.

Constraints:
Keep rules loose for now.
Do not implement mana or casting yet.
Keep React UI separate from game logic.

Done when:
A card can move from library to hand, hand to battlefield, battlefield to graveyard, and hand to stack.
Zone counts update.
npm test passes.
npm run build passes.
```

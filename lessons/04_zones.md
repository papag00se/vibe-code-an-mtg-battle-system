# Lesson 4 — Zones

## Teaches

- arrays
- state movement
- game-state modeling
- card data vs card instance

## Codex prompt

```text
Goal:
Add Magic-inspired zones to the app.

Context:
This is still a learning lab, not a full game client.

Zones:
- library
- hand
- battlefield
- graveyard
- exile
- stack

Requirements:
Create TypeScript types for CardData, CardInstance, PlayerState, ZoneName, and GameState.
Add a simple local sample deck using a small set of Scryfall card names or preloaded sample cards.
Add buttons to move cards between zones for demonstration.
Add event-log entries for moves.

Constraints:
Keep rules loose for now.
This phase is about understanding state and zones.
Put pure logic in src/game/zones.ts.

Done when:
A card can be moved from library to hand, hand to battlefield, battlefield to graveyard, and hand to stack.
The event log explains each movement.
```

## Manual test

- Move top card from library to hand.
- Move a hand card to battlefield.
- Move a battlefield card to graveyard.
- Confirm zone counts update.

## Ask Codex after implementation

```text
Explain why zones are modeled as arrays. Explain what a CardInstance is and why it is different from Scryfall card data.
```

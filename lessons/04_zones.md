# Lesson 4 — Zones

Every card in Magic lives *somewhere* — your library, your hand, the battlefield, the graveyard. Those places are called zones, and moving cards between them is basically what playing Magic *is*. In this lesson you'll model all six zones (including the stack, where spells wait their turn) and add buttons to shuffle cards around. This is your first taste of game state, and it's a big one.

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

Walk a card through its life story and watch the counts update at each step:

- Move the top card from library to hand.
- Move a hand card to the battlefield.
- Move a battlefield card to the graveyard.
- Confirm the zone counts update as it goes.

If the numbers move and the event log narrates each hop, your zones are working.

## Ask Codex after implementation

This lesson sneaks in a deep idea — the difference between a card's *data* and a specific *copy* of it in play. Ask about it:

```text
Explain why zones are modeled as arrays. Explain what a CardInstance is and why it is different from Scryfall card data.
```

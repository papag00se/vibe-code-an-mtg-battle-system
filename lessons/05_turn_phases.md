# Lesson 5 — Turn phases

## Teaches

- state machines
- finite transitions
- active player logic
- turn structure

## Phase model

```text
beginning -> firstMain -> combat -> secondMain -> end -> next player's beginning
```

## Codex prompt

```text
Goal:
Add a simplified turn phase system.

Phases:
- beginning
- firstMain
- combat
- secondMain
- end

Requirements:
- Show active player.
- Show current phase.
- Add a "Next Phase" button.
- Beginning phase untaps permanents and draws a card.
- The first player skips the draw on their first turn.
- First main and second main allow land play and spell casting later.
- End phase clears temporary damage and passes the turn.
- Add event-log messages for phase changes.

Constraints:
Keep this as a learning model.
Do not attempt full Comprehensive Rules accuracy yet.
Put pure logic in src/game/turn.ts.

Done when:
The app advances through phases and passes the turn between two players.
```

## Manual test

Click through a full turn cycle and confirm:

- phase order is correct
- active player changes after end phase
- event log is understandable

## Ask Codex after implementation

```text
Explain why turn phases are a state machine. Show me where the valid transitions are encoded.
```

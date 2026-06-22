# Lesson 5 — Turn phases

A Magic turn isn't one big blob — it marches through phases in a strict order, every single time. Untap and draw, play your stuff, swing in combat, wrap up. In this lesson you'll teach the app that rhythm with a "Next Phase" button and hand the turn off between two players. Programmers call this pattern a state machine, and once it clicks, you'll see it everywhere.

## Teaches

- state machines
- finite transitions
- active player logic
- turn structure

## Phase model

Here's the loop you're building. Notice how it wraps back around to the next player at the end:

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

Hit "Next Phase" over and over through a full turn cycle and confirm:

- the phase order is correct
- the active player changes after the end phase
- the event log reads clearly

When the turn cleanly hands off to player two and starts over, you've built your first state machine.

## Ask Codex after implementation

Want to see the magic behind the button? Ask Codex to show you where the rules actually live:

```text
Explain why turn phases are a state machine. Show me where the valid transitions are encoded.
```

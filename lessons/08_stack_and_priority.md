# Lesson 8 — Stack and priority

## Teaches

- LIFO data structure
- response windows
- priority passing
- event-driven rules

## Codex prompt

```text
Goal:
Build a visual stack tutor.

Requirements:
- Show the stack in the center of the battlefield.
- Add a "Pass Priority" button.
- Track which player has priority.
- If both players pass in sequence, resolve the top stack item.
- Resolve stack items last-in-first-out.
- Add an event log explaining what happened.
- Add a guided scenario called "Why the Stack Matters".

Scenario:
- Player A casts a spell.
- Player B responds with an instant.
- Player A responds with another instant.
- Both players pass.
- The app resolves the stack in reverse order.

Constraints:
Keep implementation simple and readable.
Prioritize teaching over total rules accuracy.
Put pure logic in src/game/stack.ts.

Done when:
Player A casts a spell.
Player B can respond with an instant.
If both pass, Player B's spell resolves first, then Player A's spell resolves.
The guided scenario visually explains last-in-first-out resolution.
```

## Manual test

- Put two spells on stack.
- Pass priority twice.
- Confirm last spell resolves first.
- Confirm event log explains it.

## Ask Codex after implementation

```text
Explain the stack as a LIFO data structure. Use the current code as the example.
```

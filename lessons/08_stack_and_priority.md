# Lesson 8 — Stack and priority

Here's the concept that trips up almost every new Magic player — and you're about to *build* it, which is the best way to finally get it. The stack is the waiting line where spells sit before they resolve, and the twist is that the last spell added resolves first. Respond to a spell and your response goes off before the thing it's responding to. Wild, right? Let's make it visible.

## What you'll teach Untap

- the stack as a last-in, first-out (LIFO) structure
- response windows — those moments where you get to react
- passing priority back and forth
- rules that fire in response to events

## Codex prompt

```text
Goal:
Build a visual, interactive stack for Untap.

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

## Try it yourself

Watch the LIFO magic happen with your own eyes:

- Put two spells on the stack.
- Pass priority twice.
- Confirm the last spell resolves first.
- Confirm the event log explains it in plain language.

## Ask Codex after implementation

```text
Explain the stack as a LIFO data structure. Use the current code as the example.
```

# Prompt 05 — Build stack and priority

```text
Goal:
Build a visual stack and simplified priority system.

Context:
This lesson teaches LIFO data structures and response windows.

Read first:
- lessons/08_stack_and_priority.md
- docs/05_rules_engine_spec.md

Requirements:
- Create src/game/stack.ts.
- Add StackView component.
- Show the stack in the center of the battlefield.
- Track priority player.
- Add Pass Priority button.
- If both players pass in sequence, resolve the top stack item.
- Resolve top stack item first.
- Reset pass flags when a new spell is added.
- Add event-log messages.
- Add guided scenario: "Why the Stack Matters".

Tests:
- stack resolves last-in-first-out
- two passes resolve top item
- adding a new spell resets pass state

Constraints:
Keep the priority model simplified.
Do not implement every real priority window.
Prioritize teaching clarity.

Done when:
Player A can cast a spell, Player B can respond with an instant, both can pass, and the last spell added resolves first.
npm test passes.
npm run build passes.
```

# Lesson 11 — Testing the rules engine

Tests might sound like the boring vegetables of coding, but stick with us — they're actually a superpower. Once Untap has a solid set of tests, you can ask Codex to change things and *know* you didn't quietly break the stack or combat. Tests turn "I hope this still works" into "I'm sure it does." That confidence is worth a lot, especially when you're learning.

## What you'll teach Untap

- confidence that comes from tests, not crossed fingers
- pure functions that are easy to check
- fixtures that behave the same way every single run
- the discipline of reviewing AI-written code

## Codex prompt

```text
Goal:
Add Vitest tests for the rules engine.

Test:
- drawing a card moves it from library to hand
- playing a land only works once per turn
- tapping a land adds mana
- mana clears between phases
- casting without enough mana fails
- stack resolves last-in-first-out
- unblocked attacker damages defending player
- lethal combat damage moves creature to graveyard
- flying blocker legality works

Constraints:
Test pure game functions, not React UI.
Keep tests readable for a beginner.
Use small deterministic game states.

Done when:
npm test passes.
Each test name reads like a rule statement.
```

## Try it yourself

Run the suite and the build, and enjoy that wall of green:

```bash
npm test
npm run build
```

## Ask Codex after implementation

```text
Explain what each test protects. Identify one bug these tests would catch in the future.
```

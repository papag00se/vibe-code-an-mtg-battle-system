# Lesson 11 — Testing the rules engine

## Teaches

- test-driven confidence
- pure functions
- deterministic fixtures
- AI code review discipline

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

## Manual test

```bash
npm test
npm run build
```

## Ask Codex after implementation

```text
Explain what each test protects. Identify one bug these tests would catch in the future.
```

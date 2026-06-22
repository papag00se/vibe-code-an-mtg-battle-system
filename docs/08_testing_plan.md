# 08 — Testing plan

## Purpose

Rules code needs tests because AI-generated code can look correct while subtly breaking state transitions.

Test pure functions. Avoid UI tests at first.

## Test files

```text
src/tests/startGame.test.ts
src/tests/zones.test.ts
src/tests/turn.test.ts
src/tests/mana.test.ts
src/tests/casting.test.ts
src/tests/stack.test.ts
src/tests/combat.test.ts
src/tests/keywords.test.ts
```

## Start game tests

- each player starts at 20 life
- each player draws seven cards
- libraries shrink by seven
- active player is set
- first player skips first draw

## Zone tests

- drawCard moves top library card to hand
- moveCard removes card from source zone
- moveCard adds card to destination zone
- invalid move returns a reason or throws a controlled error

## Turn tests

- phase advances in correct order
- end phase passes turn
- beginning phase untaps permanents
- beginning phase draws card except first player's first turn
- temporary damage clears at end turn

## Mana tests

- one land can be played per turn
- second land play fails
- land can be tapped for mana
- tapped land cannot be tapped again
- mana clears between phases

## Casting tests

- cannot cast without enough mana
- permanent spell goes to stack
- resolving permanent spell moves it to battlefield
- resolving instant/sorcery moves it to graveyard
- sorcery-speed spell fails outside main phase or while stack is not empty
- instant can be cast when player has priority

## Stack tests

- stack is last-in-first-out
- priority passes between players
- two consecutive passes resolve top stack item
- stack item logs resolution

## Combat tests

- only untapped creatures can attack
- attacking taps creature
- untapped defending creature can block
- unblocked creature damages defending player
- blocked creatures damage each other
- lethal damage moves creature to graveyard
- damage clears at end of turn

## Keyword tests

Add one keyword at a time.

First:

- flying creature can be blocked by flying
- flying creature can be blocked by reach
- flying creature cannot be blocked by non-flying/non-reach

Later:

- haste can attack immediately
- vigilance does not tap when attacking
- trample assigns excess damage
- deathtouch makes any creature damage lethal
- first strike creates earlier damage step
- double strike deals damage in both steps
- lifelink gains life when damage is dealt

## Codex testing prompt

```text
Goal:
Add Vitest tests for the rules logic affected by the last change.

Context:
The rules engine should be tested as pure functions under src/game. Avoid React UI tests for now.

Constraints:
Use small deterministic game states.
Keep test names readable.
Do not skip tests.

Done when:
npm test passes and the tested behavior is clear from the test names.
```

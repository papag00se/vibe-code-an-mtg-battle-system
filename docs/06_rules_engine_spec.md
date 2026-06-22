# 06 — Rules engine spec

This is the brain of Untap — the part that actually knows the rules of Magic. Get this layer right and everything else gets easier. Keep it clean, keep it honest, and keep it separate from the UI.

## Design principle

Rules logic should be pure functions where possible. React should display state and call rules functions. React should not contain the rules engine. Think of it this way: React paints the picture, the rules engine decides what is true.

## Core types

```ts
type PlayerId = "playerA" | "playerB";
type Color = "W" | "U" | "B" | "R" | "G" | "C";
type ZoneName = "library" | "hand" | "battlefield" | "graveyard" | "exile" | "stack";

type Phase = "beginning" | "firstMain" | "combat" | "secondMain" | "end";

type CombatStep =
  | "none"
  | "declareAttackers"
  | "declareBlockers"
  | "combatDamage"
  | "endCombat";
```

## Card data vs card instance

This distinction trips up a lot of beginners, so let's be clear up front.

Card data describes a printed card or Scryfall object — the platonic "Lightning Bolt."

Card instance describes a particular copy inside a specific game — *this* Lightning Bolt, in your hand, owned by you.

```ts
interface CardData {
  id: string;
  name: string;
  manaCost?: string;
  typeLine: string;
  oracleText?: string;
  power?: string;
  toughness?: string;
  imageUrl?: string;
}

interface CardInstance {
  instanceId: string;
  card: CardData;
  ownerId: PlayerId;
  controllerId: PlayerId;
  tapped: boolean;
  damage: number;
  summoningSick: boolean;
}
```

## Player state

```ts
interface PlayerState {
  id: PlayerId;
  name: string;
  life: number;
  library: CardInstance[];
  hand: CardInstance[];
  battlefield: CardInstance[];
  graveyard: CardInstance[];
  exile: CardInstance[];
  manaPool: Record<Color, number>;
  landsPlayedThisTurn: number;
  hasPassedPriority: boolean;
}
```

## Game state

```ts
interface GameState {
  players: Record<PlayerId, PlayerState>;
  activePlayerId: PlayerId;
  priorityPlayerId: PlayerId;
  turnNumber: number;
  phase: Phase;
  combatStep: CombatStep;
  stack: StackItem[];
  eventLog: GameEvent[];
  firstTurnDrawSkipped: boolean;
  winnerId?: PlayerId;
}
```

## Core pure functions

```ts
startGame(deckA, deckB): GameState
drawCard(state, playerId): GameState
moveCard(state, playerId, fromZone, toZone, instanceId): GameState
advancePhase(state): GameState
playLand(state, playerId, instanceId): GameState
tapForMana(state, playerId, landInstanceId): GameState
canCastSpell(state, playerId, instanceId): LegalActionResult
castSpell(state, playerId, instanceId, targets): GameState
passPriority(state, playerId): GameState
resolveTopOfStack(state): GameState
declareAttackers(state, playerId, attackerIds): GameState
declareBlocker(state, blockerId, attackerId): GameState
resolveCombatDamage(state): GameState
checkWinConditions(state): GameState
```

## Legal action result

```ts
interface LegalActionResult {
  legal: boolean;
  reason?: string;
}
```

Use this so the UI can explain illegal moves instead of silently failing. A button that quietly does nothing is frustrating; a button that says *why* is a tiny rules lesson.

## Simplifications

Magic is gloriously complicated, and trying to model all of it on day one is a great way to give up. So we start small on purpose. The initial version ignores:

- mulligans
- sideboards
- priority in every real step
- replacement effects
- triggered abilities
- continuous effects
- layers
- state-based action edge cases
- multiple blockers per attacker
- first strike / double strike initially
- planeswalker attacks
- protection
- ward / hexproof
- damage prevention edge cases

None of these are gone forever — they're just waiting in the wings. Add them later as lessons, one at a time, once the foundation is solid.

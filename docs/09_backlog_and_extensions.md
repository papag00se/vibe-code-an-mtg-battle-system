# 09 — Backlog and extensions

## Near-term extensions

### Deck import

Parse simple decklists:

```text
4 Lightning Bolt
4 Monastery Swiftspear
20 Mountain
```

Teach:

- string parsing
- normalization
- API batching
- validation

### Lesson mode

Add route-free tabs:

```text
Card Search
Card Anatomy
Zones
Turn Phases
Mana
Stack
Combat
Keywords
Tests
Resources
```

Teach:

- navigation state
- progressive disclosure

### Debug inspector

Show raw GameState in a collapsible panel.

Teach:

- state introspection
- debugging

### Save/load

Use localStorage to save lesson progress.

Teach:

- persistence
- serialization

## Medium-term extensions

### Goldfish mode

One player plays through turns without an opponent.

Teach:

- solo simulations
- deterministic actions

### Scenario builder

Create scripted rules puzzles:

```text
Player A casts spell.
Player B responds.
Resolve stack.
Explain result.
```

Teach:

- fixtures
- preloaded state
- UX-driven learning

### Keyword modules

Add one mechanic at a time:

```text
Flying
Reach
Haste
Vigilance
Trample
Deathtouch
First strike
Double strike
Lifelink
Menace
Ward
Hexproof
```

Each keyword gets:

- short explanation
- example card search
- simulator rule
- unit tests

## Advanced extensions

### Commander deck viewer

Only as a deck-analysis/reference tool, not gameplay.

Teach:

- larger data structures
- categories
- charts

### Probability tools

Calculate opening-hand odds or land-drop odds.

Teach:

- combinatorics
- simulations
- charts

### Rules citation panel

Link to relevant Comprehensive Rules sections without copying long text.

Teach:

- reference UX
- source attribution

### AI rules explainer

Local explanation panel that summarizes current game state.

Teach:

- prompt design
- context construction
- hallucination boundaries

## Keep avoiding

- public matchmaking
- paid gameplay
- WotC branding
- image bundling
- proxy printing
- claiming rules-perfect implementation

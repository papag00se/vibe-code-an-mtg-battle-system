# 10 — Backlog and extensions

Finished the core build? Nice work. This is your wish list — a pile of fun directions to take Untap once the basics are solid. Pick whatever excites you; each one teaches something new.

## Near-term extensions

These are close at hand — natural next steps once the main loop feels good.

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

A little more ambitious — worth it once you're comfortable steering Codex.

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

Boss-level stuff. Save these for when you're feeling brave and the fundamentals are second nature.

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

No matter how far you take Untap, stay in your lane — it keeps the project free, legal, and respectful of Wizards of the Coast:

- public matchmaking
- paid gameplay
- WotC branding
- image bundling
- proxy printing
- claiming rules-perfect implementation

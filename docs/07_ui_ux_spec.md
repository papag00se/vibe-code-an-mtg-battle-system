# 07 — UI/UX spec

This is where Untap stops being abstract and starts being a place you actually want to play. The whole job of the interface is to make Magic's invisible rules visible — so a beginner can *see* the game thinking.

## UI goal

Make rules visible. At any moment, you should always know:

- whose turn it is
- current phase
- current priority player
- what can be clicked
- what just happened
- what is on the stack
- which actions are illegal and why

## Main layout

```text
+---------------------------------------------------+
| Header: Untap / turn / phase / priority           |
+---------------------------------------------------+
| Opponent hand/library/graveyard/life              |
| Opponent battlefield                              |
|                                                   |
|                    Stack                          |
|                 Event log                         |
|                                                   |
| Your battlefield                                  |
| Your hand/library/graveyard/life/mana             |
+---------------------------------------------------+
| Footer fan-content notice                         |
+---------------------------------------------------+
```

## Components

Here are the building blocks. Each one does a small job well — wire them together and Untap takes shape.

### AppShell

Owns page layout and global navigation.

### FooterNotice

Shows unofficial fan-content notice.

### CardSearch

Search input, loading state, error state, result state.

### CardViewer

Displays image, name, mana cost, type line, Oracle text, power/toughness.

### CardAnatomyPanel

Explains selected card fields in original language.

### Battlefield

Displays both players and central stack.

### ZoneView

Reusable zone display: library, hand, battlefield, graveyard, exile.

### StackView

Shows stack items top-first and explains LIFO.

### PhaseBanner

Shows active player, current phase, and available actions.

### ManaPool

Displays W/U/B/R/G/C counts as text, not official symbol art.

### EventLog

Chronological list of actions.

### ResourcePanel

Links to official WotC resources and Scryfall docs.

## UX rules

These are the little kindnesses that keep a beginner oriented instead of lost:

- Disable buttons for illegal actions.
- When an action is disabled, provide a short reason.
- Highlight legal actions.
- Keep card images large enough to be motivating.
- Use text labels for zones.
- Show card counts for hidden zones.
- Do not show opponent hidden hand contents unless in debug mode.
- Add a debug mode for learning.

## Event log examples

```text
Player A drew a card.
Player A played Island.
Player A tapped Island for U.
Player A cast Opt.
Opt was put onto the stack.
Player B passed priority.
Player A passed priority.
Opt resolved and moved to graveyard.
```

## Beginner affordances

Never leave the learner guessing. Every lesson screen should answer four simple questions:

- what this teaches
- what to click
- what to notice
- what code concept it maps to

## Visual style

Aim for "cozy game table at midnight," and stay clearly unofficial:

- Clean dark tabletop style.
- Avoid WotC logos and official branding.
- Use card images as card images only.
- Use generic icons or text labels for actions.
- Prefer clarity over visual excess.

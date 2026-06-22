# Lesson 3 — Card anatomy

A Magic card crams a surprising amount of info into a tiny rectangle, and it can feel like a foreign language at first. In this lesson you'll build a friendly side panel that breaks a card down field by field — mana cost, type line, that wall of rules text — and explains each part in plain English. You're teaching the app to teach, and teaching yourself the cards along the way.

## Teaches

- conditional rendering
- TypeScript optional fields
- domain explanation
- transforming API data into learner-friendly UI

## Codex prompt

```text
Goal:
Add a "How to Read a Card" learning panel.

Context:
This panel should use the selected card from Scryfall and explain the fields in original beginner-friendly language.

Show:
- name
- mana cost
- colors
- type line
- Oracle text
- power/toughness if present
- legalities if present

Constraints:
Do not copy long WotC explanations.
Write short original explanations.
Keep the UI beginner-friendly.
Use plain text mana symbols like W, U, B, R, G, C.

Done when:
The selected card has a side panel explaining each field.
Cards without power/toughness do not show a broken empty section.
```

## Manual test

The trick here is variety — different card types have different fields. Search one creature, one instant, and one land, and check that each one explains itself cleanly:

```text
Llanowar Elves
Lightning Bolt
Island
```

Pay special attention to the land: it has no power/toughness, so make sure that section disappears instead of showing an awkward empty box.

## Ask Codex after implementation

Notice how some cards have fields others don't? That's a real programming puzzle. Ask Codex about it:

```text
Explain why some Scryfall fields are optional and how TypeScript helps us avoid crashes.
```

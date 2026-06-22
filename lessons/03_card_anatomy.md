# Lesson 3 — Card anatomy

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

Search one creature, one instant, one land.

Suggested cards:

```text
Llanowar Elves
Lightning Bolt
Island
```

## Ask Codex after implementation

```text
Explain why some Scryfall fields are optional and how TypeScript helps us avoid crashes.
```

# Prompt 03 — Build card anatomy panel

Ever stared at a card and wondered what all those symbols and lines actually mean? This lesson builds the friendly tour guide — a panel that reads a card aloud for you. Paste this into Codex.

```text
Goal:
Add a "How to Read a Card" panel for the selected Scryfall card.

Context:
This lesson teaches TypeScript optional fields, conditional rendering, and domain explanation.

Read first:
- lessons/03_card_anatomy.md

Requirements:
- Create CardAnatomyPanel.
- Explain name, mana cost, colors, type line, Oracle text, power/toughness, and legalities.
- Use short original explanations.
- Hide sections that do not apply.
- Keep explanations beginner-friendly.

Constraints:
Do not copy long WotC explanations.
Use text mana symbols only.
Do not add new API calls unless needed.

Done when:
A creature, instant, and land each render a sensible anatomy panel.
npm run build passes.
```

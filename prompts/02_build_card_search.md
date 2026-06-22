# Prompt 02 — Build Scryfall card search

Time for your first real spell. This is where Untap stops being a placeholder and starts pulling actual Magic cards out of thin air — type a name, get the card. Paste this into Codex.

```text
Goal:
Add a Magic card search screen using the Scryfall API.

Context:
This is the first real interactive lesson. It teaches API calls, async/await, JSON, TypeScript types, loading states, and error states.

Read first:
- lessons/02_card_search.md
- docs/09_wotc_scryfall_resources.md

Requirements:
- Create src/api/scryfall.ts.
- Add a getCardByName(name) function using Scryfall's named-card endpoint.
- Add TypeScript types for the subset of Scryfall fields used.
- Create CardSearch and CardViewer components.
- Show loading state.
- Show error state.
- Render name, mana cost, type line, Oracle text, power/toughness when present, and image.
- Use Scryfall image URLs directly.
- Do not download or bundle images.

Constraints:
Keep the code beginner-readable.
Do not add a state-management library.
Do not add routing.
Do not use official Wizards logos or mana-symbol art.

Done when:
Searching "Lightning Bolt" renders the card.
Searching nonsense shows a useful error.
npm run build passes.
```

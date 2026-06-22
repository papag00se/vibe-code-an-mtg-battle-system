# Prompt 07 — Polish UX and add resource panel

```text
Goal:
Make Stack Tutor easier to learn from and add official resource links.

Context:
This is a UX polish pass. Do not add new rules.

Read first:
- lessons/12_polish.md
- docs/07_ui_ux_spec.md
- docs/09_wotc_scryfall_resources.md

Requirements:
- Highlight legal actions.
- Disable illegal actions.
- Show reason for disabled actions.
- Show active player, phase, and priority clearly.
- Improve stack ordering visibility.
- Add card detail hover or selected-card panel.
- Add graveyard viewer.
- Improve event log readability.
- Add ResourcePanel with links to WotC Fan Content Policy, How to Play, Comprehensive Rules, Keyword Glossary, Gatherer, Scryfall API, Scryfall image docs, and MTGJSON Getting Started.
- Keep footer notice visible.

Constraints:
Do not use Wizards logos.
Do not copy long official rules text.
Do not add routing unless necessary.
Do not add new gameplay rules.

Done when:
A new user can understand whose turn it is, what phase it is, who has priority, what can be clicked, and what just happened.
npm run build passes.
npm test passes.
```

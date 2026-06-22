# Lesson 12 — UX polish and resource panel

## Teaches

- user guidance
- affordances
- educational UI
- links to primary resources

## Codex prompt

```text
Goal:
Make Stack Tutor easier to learn from.

Requirements:
- Highlight legal actions.
- Disable illegal actions.
- Show a reason for disabled/illegal actions.
- Add a phase banner.
- Add a priority indicator.
- Improve StackView so top-of-stack is obvious.
- Add card hover/detail panel.
- Add graveyard viewer.
- Add combat labels.
- Improve event log readability.
- Add a Learn More resource panel.

Resource panel links:
- WotC Fan Content Policy
- WotC How to Play
- WotC Comprehensive Rules
- WotC Keyword Glossary
- Gatherer
- Scryfall API docs
- Scryfall image docs
- MTGJSON Getting Started

Constraints:
Do not add new rules in this task.
Do not use Wizards logos.
Summarize resources in original words.
Keep the footer notice visible.

Done when:
A new player can understand whose turn it is, what phase it is, who has priority, what they can click, and what just happened.
```

## Manual test

Run through:

- card search
- play land
- tap land
- cast spell
- pass priority
- resolve stack
- declare attackers
- declare blockers
- resolve combat

Confirm the event log and UI explain the flow.

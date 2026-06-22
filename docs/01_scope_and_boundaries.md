# 01 — Scope and boundaries

Let's set the table before you build. Knowing where the lines are keeps this project fun, legal, and respectful of the game we love. None of this is scary — it just keeps you in the safe zone.

## Working interpretation

Here's the deal: Untap is a free, educational vibe-coding tutorial that uses Magic as its learning context. Think of it as unofficial fan content and a rules-learning lab — not a marketable game client. You're learning to code with Magic as your playground, and that's exactly the right framing.

## Safer uses

These are all squarely in-bounds — build with confidence:

- local-only tutorial project
- free web learning demo
- card search and display
- Scryfall-powered card lookup
- card anatomy explanations
- rules concepts explained in original words
- simplified stack visualizer
- simplified combat simulator
- goldfish-style solo demonstrations
- local two-player educational sandbox
- links to official resources

## Riskier uses

These cross the line — steer clear of all of them:

- paid product
- access requiring payment, subscription, survey, or email registration
- app branding using WotC logos/trademarks
- official-sounding product name
- full online multiplayer
- ranked matchmaking
- proxy printing
- offline bulk card-image downloads
- wholesale copying of Comprehensive Rules text
- selling or licensing the app/content

## Footer notice

Drop this in the app footer, word for word — this is the standard Fan Content wording, so don't paraphrase it:

```text
Untap is unofficial Fan Content permitted under the Wizards of the Coast Fan Content Policy. Not approved/endorsed by Wizards. Portions of the materials used are property of Wizards of the Coast. © Wizards of the Coast LLC.
```

## App framing copy

Aim for copy like this — clear about what Untap is:

```text
Learn coding through Magic rules concepts. Search cards, visualize zones, step through phases, and watch the stack resolve.
```

Steer away from copy like this — it overpromises and implies you're a game client:

```text
Play full Magic online for free.
```

## Naming

The app you're building is named **Untap**. If you ever spin off your own variation, these kinds of names stay safe:

- Untap
- Rules Lab
- Mana Sandbox
- Priority Trainer

Avoid:

- official-sounding names
- names implying endorsement
- names confusingly close to Arena, Magic Online, SpellTable, or Wizards services

## Data handling

Play nice with Scryfall and you'll be fine:

- Use Scryfall API calls at runtime.
- Do not download all card images.
- Do not bundle card images in the repo.
- Cache lightweight JSON sparingly if needed.
- Respect API usage guidelines.

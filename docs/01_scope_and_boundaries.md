# 01 — Scope and boundaries

## Working interpretation

A free, educational vibe-coding tutorial that uses MTG as the learning context is the intended scope. The app should be treated as unofficial fan content and a rules-learning lab, not a marketable game client.

## Safer uses

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

Use this in the app footer:

```text
Stack Tutor is unofficial Fan Content permitted under the Wizards of the Coast Fan Content Policy. Not approved/endorsed by Wizards. Portions of the materials used are property of Wizards of the Coast. © Wizards of the Coast LLC.
```

## App framing copy

Use copy like this:

```text
Learn coding through Magic rules concepts. Search cards, visualize zones, step through phases, and watch the stack resolve.
```

Avoid copy like this:

```text
Play full Magic online for free.
```

## Naming

Acceptable:

- Stack Tutor
- Rules Lab
- Mana Sandbox
- Priority Trainer

Avoid:

- official-sounding names
- names implying endorsement
- names confusingly close to Arena, Magic Online, SpellTable, or Wizards services

## Data handling

- Use Scryfall API calls at runtime.
- Do not download all card images.
- Do not bundle card images in the repo.
- Cache lightweight JSON sparingly if needed.
- Respect API usage guidelines.

# 09 — WotC, Scryfall, and MTGJSON resources

These are your trusted sources — the official rules, the card data, the legal boundaries. Bookmark them. When a rules question comes up (and it will), this is where you and Codex go to settle it instead of guessing.

Verified for this walkthrough on 2026-06-22.

## WotC resources

### Fan Content Policy

URL: https://company.wizards.com/en/legal/fancontentpolicy

Use for:

- project scope
- footer disclaimer
- noncommercial/free boundaries
- restrictions around logos, trademarks, and game products

Notes:

- Keep the project free.
- Make unofficial status clear.
- Do not use Wizards logos/trademarks for branding.
- Do not sell or license the tutorial.

### How to Play

URL: https://magic.wizards.com/en/how-to-play

Use for:

- beginner rules sequence
- setup
- casting spells
- lands and mana
- turn phases
- combat basics

Recommended tutorial mapping:

```text
Setup -> startGame()
Casting spells -> castSpell()
Taking a turn -> advancePhase()
Combat -> declareAttackers(), declareBlockers(), resolveCombatDamage()
```

### Comprehensive Rules

URL: https://magic.wizards.com/en/rules

Use for:

- exact reference when a rules question appears
- corner cases
- later advanced lessons

Do not use as:

- beginner reading assignment
- source for wholesale copied text in the app

### Keyword Glossary

URL: https://magic.wizards.com/en/keyword-glossary

Use for:

- keyword lesson ordering
- beginner explanations to rewrite in original words
- choosing mechanics for later modules

Start with:

```text
Flying
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

### Gatherer / official card database

URL: https://gatherer.wizards.com/

Use for:

- official card lookup
- Oracle text/rulings reference

Do not use as the primary app API if Scryfall is simpler for the tutorial.

### The Stack and Its Tricks

URL: https://magic.wizards.com/en/news/feature/stack-and-its-tricks-2017-11-30

Use for:

- stack lesson
- priority explanation
- LIFO visualization

## Scryfall resources

Scryfall is the friendly card database that powers Untap's search. It's fast, free, and beginner-friendly — your best friend for this whole build.

### Scryfall API

URL: https://scryfall.com/docs/api

Use for:

- card search
- named card lookup
- card JSON
- image URLs

Beginner endpoint suggestions:

```text
GET https://api.scryfall.com/cards/named?fuzzy=Lightning%20Bolt
GET https://api.scryfall.com/cards/search?q=dragon
```

### Scryfall image docs

URL: https://scryfall.com/docs/api/images

Use for:

- image URL behavior
- card image rendering

Project rule:

```text
Use image URLs. Do not bulk-download or bundle card images.
```

### Scryfall terms

URL: https://scryfall.com/docs/terms

Use for:

- attribution and use expectations
- understanding that card data/images remain Wizards/artist IP

## MTGJSON resources

### Getting Started

URL: https://mtgjson.com/getting-started/

Use for:

- later bulk-data lessons
- offline analytics
- deck/statistics modules

Do not use in the first tutorial unless the learner outgrows Scryfall API calls.

## Resource panel copy

Drop this straight into the app's resource panel:

```text
Untap links to official Magic learning resources and Scryfall card data so you can learn both coding and rules concepts. This app is unofficial and educational.
```

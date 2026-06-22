# Lesson 10 — Keywords

Flying, trample, deathtouch — keywords are the spice of Magic, and there are a *lot* of them. Good news: you don't have to do them all at once. This lesson is about growing your rules engine one small, safe keyword at a time, testing each as you go. It's the same habit real engineers use to add features without breaking everything else. You'll get good at it fast.

## What you'll teach Untap

- adding complexity a little at a time
- writing tests aimed at one specific rule
- reading keywords out of a card's Oracle text
- growing a rules engine without knocking it over

## Keyword order

Start with the simplest useful rules and work your way up:

```text
1. Flying
2. Reach
3. Haste
4. Vigilance
5. Trample
6. Deathtouch
7. First strike
8. Double strike
9. Lifelink
10. Menace
11. Ward
12. Hexproof
```

## First keyword prompt: Flying

Flying's a perfect first keyword — simple, iconic, and easy to test. Here's the prompt to hand Codex:

```text
Goal:
Add the first keyword lesson: flying.

Requirements:
- Detect flying from Oracle text.
- Detect reach from Oracle text.
- A creature with flying can be blocked only by a creature with flying or reach.
- Add a short original explanation of flying and reach.
- Add tests for blocker legality.

Constraints:
Use WotC's Keyword Glossary as a reference, but write explanations in original words.
Do not copy long rules text.
Keep this isolated to combat blocker legality.

Done when:
A creature with flying can only be blocked by a creature with flying or reach.
Tests pass.
```

## Later keyword prompt template

Once flying works, the rest follow the same shape. Reuse this template for each keyword down the list — just swap in the name and let Codex extend the engine:

```text
Goal:
Add the keyword lesson for [keyword].

Context:
Each keyword should be implemented as a small extension to the rules engine, not as a rewrite.

Requirements:
- Detect the keyword from Oracle text.
- Add a short original learner explanation.
- Add one guided demo scenario.
- Add unit tests.

Constraints:
Do not implement unrelated keywords.
Keep the change small.

Done when:
The keyword works in the relevant simulator and tests pass.
```

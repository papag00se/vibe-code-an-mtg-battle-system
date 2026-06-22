# Lesson 10 — Keywords

## Teaches

- incremental complexity
- rule-specific tests
- parsing Oracle text
- growing a rules engine safely

## Keyword order

Start with the simplest useful rules:

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

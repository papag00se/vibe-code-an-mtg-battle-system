# Prompt 99 — Review and refactor pass

Every good deck gets a tune-up between rounds. Run this after each major milestone to let Codex tidy up the build, catch rough edges, and keep Untap readable before you move on. No new features — just a clean, healthy codebase.

```text
Goal:
Review and refactor the current implementation for readability, correctness, and beginner friendliness.

Context:
This is a learning project. Code clarity matters more than cleverness. The rules engine should be separated from React UI.

Review for:
- unclear names
- duplicated logic
- React components containing rules logic
- missing tests
- fragile state mutation
- confusing event-log messages
- illegal actions that fail silently
- over-broad implementation beyond the lesson scope
- scope issues with WotC/IP boundaries

Constraints:
Do not change behavior unless a bug is found and explained.
Do not add new features.
Keep tests passing.

Done when:
You provide findings, make safe readability improvements, and explain what changed.
npm test passes.
npm run build passes.
```

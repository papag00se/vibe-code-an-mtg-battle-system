# Prompt 00 — Bootstrap the repository

Paste this into Codex first.

```text
Goal:
Create a beginner-friendly React + TypeScript app called Stack Tutor.

Context:
This repository contains Markdown walkthrough files for a free personal vibe-coding tutorial. The tutorial teaches programming through Magic: The Gathering rules concepts. It is unofficial fan content, not endorsed by Wizards of the Coast, and not a commercial game client.

Read first:
- AGENTS.md
- docs/00_project_brief.md
- docs/01_scope_and_boundaries.md
- docs/04_repository_setup.md

Constraints:
Use Vite, React, TypeScript, Vitest, and plain CSS.
Do not use Wizards logos.
Do not claim official affiliation.
Do not build multiplayer, matchmaking, paid access, or proxy tooling.
Use Scryfall later for card data, but do not add Scryfall API calls yet.
Keep the code beginner-readable.

Requirements:
- Create the Vite app structure.
- Add AppShell, FooterNotice, and a static Battlefield placeholder.
- Add the fan-content footer notice from AGENTS.md.
- Add basic responsive CSS.
- Add npm scripts for dev, build, and test.
- Add one trivial Vitest test so the test setup is proven.

Done when:
- npm install works.
- npm run dev works.
- npm run build works.
- npm test works.
- The browser shows Stack Tutor, a static battlefield, and the footer notice.

After implementation:
Explain the project structure and how to run it.
```

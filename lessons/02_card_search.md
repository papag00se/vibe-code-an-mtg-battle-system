# Lesson 2 — Scryfall card search

Now for the fun part: real cards. In this lesson you'll wire Untap up to Scryfall — the giant free Magic card database — so you can type a card name and watch the actual card appear. This is your first time talking to the internet from your app, and it's a genuinely magical moment. Let's go fetch some cards.

## Teaches

- API calls
- `fetch`
- `async` / `await`
- JSON
- loading states
- error states
- component state

## Codex prompt

```text
Goal:
Add a Magic card search screen using the Scryfall API.

Context:
This teaches API calls, JSON, and React state.

Requirements:
- Search by card name.
- Show loading and error states.
- Display card name, mana cost, type line, Oracle text, power/toughness when present, and card image.
- Use Scryfall image URLs directly.
- Do not download or bundle images locally.
- Add a note that card data and images come from Scryfall and the app is unofficial fan content.

Constraints:
Keep the code beginner-readable.
Put API code in src/api/scryfall.ts.
Put card UI in src/components/CardViewer.tsx.
Use TypeScript types for the subset of Scryfall data we consume.

Done when:
Typing "Lightning Bolt" shows a card image and text.
Typing nonsense shows a useful error.
```

## Suggested API function shape

Here's a shape to point Codex toward if it needs a nudge. Don't sweat understanding every line yet — you'll ask Codex to explain it in a minute:

```ts
export async function getCardByName(name: string): Promise<ScryfallCard> {
  const params = new URLSearchParams({ fuzzy: name });
  const response = await fetch(`https://api.scryfall.com/cards/named?${params}`);

  if (!response.ok) {
    throw new Error("Card not found");
  }

  return response.json();
}
```

## Manual test

Take it for a spin. Search a few of these and watch the cards roll in:

```text
Lightning Bolt
Sol Ring
Counterspell
Island
```

Then try typing pure nonsense and make sure you get a friendly error instead of a crash. Handling the "oops" case gracefully is what separates a toy from real software.

## Ask Codex after implementation

That fetch did a lot of work in a few lines. Ask Codex to walk you through it:

```text
Explain how this API call works. Explain async/await, fetch, URLSearchParams, JSON, and React state like I am new to coding.
```

# Lesson 2 — Scryfall card search

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

Search:

```text
Lightning Bolt
Sol Ring
Counterspell
Island
```

## Ask Codex after implementation

```text
Explain how this API call works. Explain async/await, fetch, URLSearchParams, JSON, and React state like I am new to coding.
```

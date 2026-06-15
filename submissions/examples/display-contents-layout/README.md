# CSS display: contents Layout

## What does this do?

Demonstrates `display: contents` to remove wrapper divs from the layout flow while preserving them in the accessibility tree. A card grid compares a semantic HTML structure with and without `display: contents`, showing how extra markup can be visually flattened without losing semantics.

## How is it used?

```css
.card-wrapper {
  display: contents;
}
```

Each card uses a `<ul>` for the grid and `<li>` wrappers around `<article>` elements. With `display: contents` on the `<li>`, the `<article>` elements become direct grid children, while screen readers still see the list structure.

## Why is it useful?

Before `display: contents`, semantic wrappers forced a tradeoff between accessible markup and layout simplicity. Developers resorted to `role="presentation"` or nested grid hacks. `display: contents` removes wrappers from the visual render tree without removing them from the accessibility tree — better semantics, cleaner layout, zero JavaScript.

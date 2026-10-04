# Code Style Guide

This document follows the following mainstream standards:

- Google JavaScript Style Guide
  https://google.github.io/styleguide/jsguide.html
- Airbnb JavaScript Style Guide
  https://github.com/airbnb/javascript
- W3C HTML / CSS Standards
  https://www.w3.org/standards/

## 1. File Organization

- The frontend is organized into a single `index.html` with `<style>` and `<script>` blocks.
- For larger projects, split CSS and JS into separate files (`style.css` / `app.js`).

## 2. HTML Rules

- All tags and attributes in lowercase.
- Attribute values in double quotes.
- Each block-level element on its own line, indented by 2 spaces.
- Prefer semantic tags: `<button>`, `<input>`, `<div>` with clear purposes.

## 3. CSS Rules

- One property per line, ending with a semicolon.
- Class names use kebab-case, e.g. `.history-item`, `.btn-num`.
- Selector nesting should not exceed 4 levels.
- Prefer hex colors; use `rgba` when transparency is needed.
- Group animations and transitions using `transition` and `@keyframes`.

## 4. JavaScript Rules

- Use ES6+: `const`, `let`, template literals, arrow functions, `async/await`.
- Do not use `var`.
- Naming conventions:

| Type | Style | Example |
|------|-------|---------|
| Variables | camelCase | `currentExpr` |
| Functions | camelCase | `loadHistory` |
| Constants | UPPER_SNAKE_CASE | `API` |
| Classes | PascalCase | `Calculator` |

- End every statement with a semicolon.
- Prefer single quotes `'...'` for strings.
- One blank line between functions.
- Never use `eval`, `exec`, or similar methods that execute string code.

## 5. Indentation and Whitespace

- Use 2 spaces per indent.
- One space on both sides of operators.
- One space after commas.
- One space before `{`, and `else` follows `}` on the same line.

## 6. Comments

- One-line description above each functional block.
- Use `//` for inline comments.
- Use `/** ... */` for function documentation.

```javascript
// Load history
async function loadHistory() { ... }
```

## 7. Naming and Readability

- Avoid meaningless names (`a`, `b`, `temp`). Prefer `expr`, `result`, `historyList`.
- Each function should have a single responsibility and ideally stay under 50 lines.
- Wrap backend API calls in named functions; avoid long logic inside event handlers.

## 8. Encoding

- All files use UTF-8.
- HTML declares `<meta charset="UTF-8">`.

## 9. Error Handling

- Use `try/catch` for asynchronous requests.
- Always display backend `success: false` messages to the user.
- Network errors should be shown with a friendly message, never a raw stack trace.
````


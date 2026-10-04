# Calculator Frontend

## Project Introduction

A calculator frontend built with HTML + CSS + vanilla JavaScript. It works together with a Flask backend to form a complete front-end / back-end separated calculator system.

Main features:
- Button-based number and operator input
- Real-time expression display
- Calculation result display
- Error message display
- History list with per-record delete and clear-all
- Chinese / English language toggle
- One-click copy of the result
- Keyboard shortcut support

## Technology Stack

- HTML5
- CSS3 (gradients, animations, Flex, Grid)
- Vanilla JavaScript (ES6+, Fetch API)

## Runtime Environment

- Any modern browser (Chrome / Edge / Firefox / Safari)
- No build tools or dependencies required

## Local Path

| Item | Path |
|------|------|
| Frontend project | `D:\FZU\calculator_frontend` |
| Main file | `D:\FZU\calculator_frontend\index.html` |

## Installation and Startup

1. Clone or download this repository.
2. Make sure the backend service is running (default: `http://127.0.0.1:5000`).
3. Double-click `index.html` to open it in the browser.

No additional installation is needed.

## Configuration

If the backend is deployed elsewhere, open `index.html` and find:

```javascript
const API = 'http://127.0.0.1:5000';
```

Replace it with the actual backend address.

## Backend Connection

The frontend calls the backend REST APIs using the native `fetch` API:

| Feature | Method | URL |
|---------|--------|-----|
| Calculate | POST | `/api/calculate` |
| Get history | GET | `/api/history` |
| Delete one | DELETE | `/api/history/{id}` |
| Clear all | DELETE | `/api/history` |

## Project Structure

```text
calculator_frontend/
├── index.html        # Main page (HTML + CSS + JS)
├── kitty.png         # Decorative image
├── README.md         # Project documentation
└── codestyle.md      # Code style guide
```

## Feature Overview

### Basic Features

- Addition, subtraction, multiplication, division
- Compound expressions with operator precedence
- Parentheses
- Unary plus / minus
- Decimals

### Extended Features

- Chinese / English toggle: click the button in the top-right corner to switch the UI language.
- Clear all history: a "Clear" button on the history header removes all records at once.
- History count: displays how many records exist.
- One-click copy of result: click the result area to copy the value to the clipboard.
- Keyboard shortcuts: digits, operators, Enter (calculate), Backspace (delete), Esc (clear).

## FAQ

Q1: The page shows "Cannot connect to backend"?

A: Make sure the backend service is running and the address matches `const API`.

Q2: The Hello Kitty image does not show?

A: Make sure `kitty.png` is in the same folder as `index.html` and the filename matches exactly (case-sensitive).

Q3: The result cannot be copied?

A: Some browsers restrict clipboard permissions. This project provides a fallback for older browsers; if it still fails, use Chrome or Edge.
````


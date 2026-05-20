# ⚡ Password Generator

A lightweight, client-side password generator that creates up to four random passwords at once — no frameworks, no dependencies, just HTML, CSS, and vanilla JavaScript.

---

## 🔍 Preview

A dark-themed UI with a single-click workflow:

1. Enter a desired password length (1–20 characters)
2. Toggle special characters and/or uppercase letters
3. Click **Generate passwords** — four passwords appear instantly
4. Click any password field to copy it to your clipboard

---

## 🗂️ Project Structure

```
password-generator/
├── index.html        # App markup
├── styles.css        # Dark theme styling
├── my.js             # Password generation logic
├── Iconlight.png     # Button icon (light variant)
└── Icon2.png         # Icon (alternate variant)
```

---

## ✨ Features

- **Generates 4 passwords simultaneously** — each independently random
- **Configurable length** — 1 to 20 characters
- **Special characters toggle** — slide on/off with a range input
- **Uppercase toggle** — slide on/off with a range input
- **One-click copy** — click any password field to copy it to clipboard
- **Input validation** — inline error for empty or out-of-range length values
- **Fully responsive** — single-column layout on small screens (≤ 550px)
- **Zero dependencies** — pure HTML5, CSS3, and vanilla JS

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| HTML5 | Structure and form inputs |
| CSS3 | Dark theme, grid layout, custom range slider |
| Vanilla JavaScript | Password logic, Clipboard API, DOM events |
| Google Fonts | Inter (body) + Karla (headings) |

---

## 🚀 Getting Started

No build step or server required.

```bash
# Clone the repo
git clone https://github.com/your-username/password-generator.git

# Open in browser
open index.html
```

Or just drag `index.html` into any modern browser.

---

## ⚙️ How It Works

- **Base characters** are generated using `Math.random().toString(36)` — lowercase alphanumeric
- **Special characters mode** switches to `String.fromCharCode()` sampling the full printable ASCII range (33–126)
- **Uppercase mode** randomly promotes characters in the array to uppercase
- **Clipboard copy** uses the `navigator.clipboard.writeText()` API with a `setSelectionRange` fallback for older mobile browsers

---

## 🐛 Known Limitations

- Passwords longer than 20 characters are blocked by validation (by design)
- The `copyToClipboard` function relies on `this` binding via `addEventListener` — it won't work if called directly
- No password strength indicator is shown

---

## 📄 License

MIT — free to use, modify, and distribute.

# SmartJSON

AI-powered JSON Formatter, Validator, and Error Explainer — runs entirely in your browser.

**Live demo:** `https://<your-username>.github.io/smartjson`

---

## Features

- **Format & Validate** — pretty-prints JSON with 2-space indentation and syntax highlighting
- **Minify** — collapses JSON to a single line
- **Line numbers** on both input and output panels
- **Green / red badge** — instant valid/invalid status with exact error message
- **AI Explain** — sends your broken JSON + error to Groq (LLaMA 3.3 70B) and gets a plain-English explanation plus the corrected JSON
- **Copy to clipboard** — one click to copy the formatted output
- **Dark theme** — GitHub-style dark UI, monospace font
- Works on mobile (panels stack vertically)
- `Ctrl+Enter` keyboard shortcut to format

---

## Setup

### 1. Deploy to GitHub Pages

1. Fork or clone this repo
2. Go to **Settings → Pages**
3. Set source to **Deploy from a branch → main → / (root)**
4. Your app is live at `https://<your-username>.github.io/<repo-name>`

No build step. No dependencies to install. Just one `index.html`.

### 2. Add your Groq API Key

The AI Explain feature requires a free Groq API key.

1. Get one at [console.groq.com](https://console.groq.com) — it's free
2. Open the app, click **⚙ API Key** in the top-right corner
3. Paste your key (starts with `gsk_`) and click **Save**

Your key is stored in `localStorage` and **only ever sent to `api.groq.com`**. It is never logged, tracked, or sent anywhere else. It stays in your browser.

> **Never commit your API key to the repo.** The settings input is intentionally in the UI, not in code.

---

## Usage

| Action | How |
|---|---|
| Format JSON | Paste → **Format & Validate** or `Ctrl+Enter` |
| Minify JSON | Paste → **⊡ Minify** |
| Explain an error | Format broken JSON → click **✦ AI Explain** |
| Copy output | Click **⎘ Copy** after formatting |
| Clear everything | Click **✕ Clear** |

---

## Tech Stack

| What | Details |
|---|---|
| UI | Pure HTML + CSS + Vanilla JS — no frameworks |
| Syntax highlighting | [highlight.js](https://highlightjs.org/) via CDN |
| AI | [Groq API](https://console.groq.com) — LLaMA 3.3 70B Versatile |
| Hosting | GitHub Pages (static, no server needed) |
| Fonts | JetBrains Mono via Google Fonts |

---

## Privacy

- No analytics, no tracking, no cookies
- Your JSON never leaves your browser (except when you click AI Explain, which sends it to Groq)
- API key stored only in your browser's localStorage

# SmartJSON — Free AI-Powered JSON Formatter, Validator & Error Explainer

> Format, minify, and validate JSON instantly. Broken JSON? AI explains exactly what's wrong in plain English and gives you the corrected version.

**🔗 Live tool:** [muhmdfarhan0.github.io/smartjson](https://muhmdfarhan0.github.io/smartjson/)

---

## What is SmartJSON?

SmartJSON is a free, browser-based JSON tool that combines instant formatting and validation with AI-powered error explanation. No login required, no data stored on any server — everything runs in your browser.

It's built for developers who are tired of cryptic `Unexpected token` errors and just want to know what's actually wrong with their JSON.

---

## Features

| Feature | Description |
|---|---|
| **Format & Validate** | Pretty-prints JSON with 2-space indentation and syntax highlighting |
| **Minify** | Collapses JSON to a single compact line |
| **Instant Validation** | Green ✓ badge for valid JSON, red ✕ badge with the exact error message |
| **AI Explain** | Sends broken JSON to Groq LLaMA 3.3 70B — explains the error in plain English and shows the fix |
| **Line Numbers** | Synchronized line numbers on both input and output panels |
| **Copy to Clipboard** | One-click copy of the formatted/minified output |
| **Keyboard Shortcut** | `Ctrl+Enter` to format instantly |
| **Mobile Friendly** | Panels stack vertically on small screens |

---

## Getting Started

### 1. Open the tool

Go to **[muhmdfarhan0.github.io/smartjson](https://muhmdfarhan0.github.io/smartjson/)**

No installation. No build step. No account needed.

### 2. Add your Groq API key (for AI Explain)

The AI error explanation feature uses Groq's free API.

1. Get a free key at [console.groq.com](https://console.groq.com) — no credit card needed
2. Click **⚙ API Key** in the top navigation
3. Paste your key (starts with `gsk_`) and click **Save**

Your key is saved in your browser's `localStorage` only. It is never sent to any server other than `api.groq.com`.

---

## How to Use

```
1. Paste JSON into the left (Input) panel
2. Click "▶ Format & Validate"  OR press Ctrl+Enter
3. ✓ Valid JSON  → See formatted output with syntax highlighting on the right
   ✕ Invalid JSON → See red error badge with the exact error location
4. For broken JSON, click "✦ AI Explain" to get a plain-English explanation + corrected JSON
```

---

## Example: Broken JSON

```json
{
  "user": {
    "name": "Alice"
    "age": 30,
    "active": True
  }
}
```

**SmartJSON catches:**
- Missing comma after `"Alice"` on line 3
- `True` should be `true` (JSON is case-sensitive)

**AI Explain output:** *"The JSON is missing a comma after the `name` field on line 3, and `True` must be lowercase `true` in JSON syntax. Here is the corrected version: ..."*

---

## Deploy Your Own

1. Fork this repo
2. Go to **Settings → Pages → Deploy from branch → main → / (root)**
3. Live in ~60 seconds at `https://<your-username>.github.io/smartjson`

---

## Tech Stack

- **Frontend:** Pure HTML + CSS + Vanilla JavaScript — zero dependencies, no build step
- **Syntax highlighting:** [highlight.js](https://highlightjs.org/) via CDN
- **AI:** [Groq API](https://console.groq.com) — LLaMA 3.3 70B Versatile (fast inference)
- **Fonts:** Playfair Display + Inter via Google Fonts
- **Hosting:** GitHub Pages

---

## Privacy

- No analytics or tracking of any kind
- Your JSON is never stored or logged
- API key lives only in your browser's `localStorage`
- The only external call is to `api.groq.com` when you click AI Explain

---

## Keywords

`json formatter` · `json validator` · `json beautifier` · `json minifier` · `json error explainer` · `ai developer tools` · `groq` · `llama` · `online json tool` · `free json formatter`

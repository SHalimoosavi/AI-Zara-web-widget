# 💬 Zara Widget — Embeddable Chat Bubble
### SAYANJALI NEXUS PRIVATE LIMITED

A zero-dependency, pure HTML/CSS/JS floating chat widget powered by Claude AI. Drop it into **any website** — GitHub Pages, WordPress, Wix, plain HTML — with no build tools, no npm, no React needed.

---

## 📄 File

```
zara-widget.html
```

One single file. Everything — HTML, CSS, JavaScript, and AI logic — is self-contained inside it.

---

## ✨ Features

| Feature | Description |
|---|---|
| 💬 Floating bubble | Fixed bottom-right, glows with cyan pulse animation |
| 🏷️ "Chat with Zara" pill | Animated label above the bubble on load |
| 🔴 Unread badge | Auto-appears after 4 seconds to attract attention |
| ⚡ Quick-start chips | One-tap shortcuts: Website Dev, AI Solutions, Book Appointment, Cybersecurity |
| 🌊 Live waveform | 18-bar equalizer animates in amber while Zara types, green when she replies |
| 💡 Status badge | Shows Online / Typing… / Offline in real time |
| ✅ Seen indicator | Green dot on avatar when chat is active |
| 📜 Chat history | Full scrollable conversation with timestamps |
| ⌨️ Auto-resize input | Textarea grows up to 3 lines as user types |
| 🔚 End Chat | Clean session close with goodbye message |
| 📱 Mobile responsive | `max-width: calc(100vw - 36px)` — works on all screen sizes |
| 🚫 Zero dependencies | No npm, no React, no build step — pure vanilla JS |

---

## 🚀 Quick Embed (3 Steps)

### Step 1 — Open `zara-widget.html`

Find the config block near the top of the `<script>` tag:

```js
/* ── CONFIG ── change only this section ── */
const ANTHROPIC_API_KEY = "YOUR_ANTHROPIC_API_KEY_HERE"; // 🔑 Replace this
const COMPANY = "SAYANJALI NEXUS PRIVATE LIMITED";        // Change if needed
```

Replace `YOUR_ANTHROPIC_API_KEY_HERE` with your key from [console.anthropic.com](https://console.anthropic.com).

---

### Step 2 — Copy the Widget Code

Copy everything between these two comments in the file:

```html
<!-- ZARA WIDGET — Paste this block into your site -->
...
<!-- END WIDGET -->
```

This includes:
- All CSS inside `<style>` tags (from `/* Launcher bubble */` onwards)
- The launcher HTML (`#zara-launcher`, `#zara-panel`)
- The `<script>` block at the bottom

---

### Step 3 — Paste into Your Website

Paste just before `</body>` in your existing HTML page:

```html
    <!-- Zara Widget -->
    <div id="zara-launcher"> ... </div>
    <div id="zara-panel"> ... </div>
    <script> ... </script>

  </body>
</html>
```

Also add the Google Fonts link inside your `<head>`:

```html
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@600;700;800&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet"/>
```

That's it — Zara is live on your site. ✅

---

## 🌐 Platform-Specific Instructions

### GitHub Pages
1. Open your `index.html` in the repo
2. Paste widget code before `</body>`
3. Commit and push — live in ~30 seconds

### WordPress
1. Go to **Appearance → Theme File Editor → footer.php**
2. Paste widget code before `</body>`
3. Save

### Wix
1. Go to **Settings → Custom Code → Add Code**
2. Set placement to **Body - end**
3. Paste widget code → Save

### Shopify
1. Go to **Online Store → Themes → Edit Code**
2. Open `theme.liquid`
3. Paste before `</body>` → Save

### Any Plain HTML Site
Paste before `</body>` in whichever `.html` file you want the widget on.

---

## 🏗️ Widget Structure

```
#zara-launcher  (fixed, bottom-right)
│
├── #zara-pill          ← "CHAT WITH ZARA" label (fades in at 1.5s)
└── #zara-bubble        ← 🤖 circular button (glows, bounces on open)
    └── #zara-badge     ← red unread count dot

#zara-panel  (fixed, above launcher)
│
├── #zara-header
│   ├── #zara-avatar    ← floating bot icon with green status dot
│   ├── .zara-hinfo     ← name + company subtitle
│   └── #zara-state-badge  ← Online / Typing… / Offline
│
├── #zara-wave          ← 18-bar animated waveform
│
├── #zara-messages      ← scrollable chat area
│   ├── .zara-empty     ← idle screen with quick-tap chips
│   ├── .zara-msg-row   ← each message bubble
│   └── #zara-typing    ← 3-dot amber typing indicator
│
└── #zara-footer
    ├── #zara-start-btn     ← shown before chat starts
    ├── #zara-input-row     ← textarea + send button (shown during chat)
    └── #zara-end-row       ← hint text + End Chat button
```

---

## 🧠 JavaScript Public API

These functions are exposed on `window` and can be called from anywhere on the page:

| Function | Description |
|---|---|
| `zaraToggle()` | Open or close the chat panel |
| `zaraStartChat()` | Begin a new conversation session |
| `zaraEndChat()` | End the session with a goodbye message |
| `zaraSend()` | Send the current input value |
| `zaraKeyDown(e)` | Keyboard handler (Enter = send, Shift+Enter = newline) |
| `zaraAutoResize(el)` | Resize textarea to fit content (max 90px) |
| `zaraQuickMsg(text)` | Start chat + immediately send a preset message (used by chips) |

**Example — open the widget from your own button:**
```html
<button onclick="zaraToggle()">Chat with Zara</button>
```

**Example — trigger a quick message programmatically:**
```js
zaraQuickMsg("I need a mobile app quote");
```

---

## 🎨 Waveform Color States

| State | Color | Trigger |
|---|---|---|
| Idle | Hidden | No activity |
| Zara typing | Amber `rgba(245,158,11,0.5)` | Waiting for Claude API |
| Zara replied | Green `rgba(16,185,129,0.4)` | Message received (fades after 1.5s) |
| User focused | Cyan `rgba(0,212,255,0.4)` | Default wave color |

---

## 🔧 Customization

### Change company name
```js
const COMPANY = "YOUR COMPANY NAME HERE";
```

### Change quick-start chips
Find in HTML:
```html
<div class="zara-chip" onclick="zaraQuickMsg('I need a website')">Website Dev</div>
```
Edit the `onclick` text and label to match your services.

### Change widget position
Default is bottom-right. To move to bottom-left:
```css
#zara-launcher { right: auto; left: 28px; }
#zara-panel    { right: auto; left: 28px; transform-origin: bottom left; }
```

### Change panel size
```css
#zara-panel { width: 400px; height: 560px; }
```

### Disable auto badge after 4 seconds
Find and remove this block in the script:
```js
setTimeout(() => {
  if (!panelOpen) { unreadCount = 1; setBadge(1); }
}, 4000);
```

### Change AI model
```js
model: "claude-opus-4-20250514",   // More powerful
model: "claude-haiku-4-5",         // Faster & cheaper
```

---

## 🔒 Security — API Key

> ⚠️ Your Anthropic API key is visible in the browser's source code. This is fine for **demos and internal tools**, but not for public production websites.

**For production**, replace the direct Anthropic call with a call to your own backend:

```js
// In callZara(), replace the fetch URL:
const resp = await fetch("/api/zara-proxy", {
  method: "POST",
  headers: { "Content-Type": "application/json" },
  body: JSON.stringify({ messages: chatHistory })
});
```

Your backend holds the API key securely and forwards requests to Anthropic. A simple Node.js or Python proxy works perfectly.

---

## 🆚 Zara Widget vs Zara Agent

| | `zara-widget.html` | `zara-agent.jsx` |
|---|---|---|
| Type | Embeddable bubble widget | Full-page standalone UI |
| Tech | Pure HTML/JS/CSS | React (JSX) |
| Install | Paste into any HTML | Needs React project |
| Build step | ❌ None | ✅ Required |
| Floating overlay | ✅ Yes | ❌ No |
| Call timer | ❌ No | ✅ Yes |
| Best for | Websites, GitHub Pages | Apps, demos, dashboards |

---

## 📁 Related Files

| File | Description |
|---|---|
| `zara-widget.html` | This file — embeddable floating widget |
| `zara-agent.jsx` | Full-page React chat UI |
| `zara-instagram-bot/` | Instagram DM bot (Node.js + Express) |

---

Built for **SAYANJALI NEXUS PRIVATE LIMITED** 🚀

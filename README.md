<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:0a1628,100:00212b&height=220&section=header&text=AI%20Zara%20Web%20Widget&fontSize=48&fontColor=00d4ff&fontAlignY=38&desc=Zero-dependency%20Claude-powered%20chat%20bubble%20for%20any%20website&descSize=16&descColor=94a3b8&descAlignY=58&animation=fadeIn" />

[![HTML](https://img.shields.io/badge/HTML-100%25-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://github.com/SHalimoosavi/AI-Zara-web-widget)
[![Claude AI](https://img.shields.io/badge/Powered%20by-Claude%20AI-CC785C?style=for-the-badge&logo=anthropic&logoColor=white)](https://console.anthropic.com)
[![Zero Dependencies](https://img.shields.io/badge/Dependencies-Zero-22c55e?style=for-the-badge&logo=checkmarx&logoColor=white)](#)
[![License](https://img.shields.io/badge/License-MIT-a855f7?style=for-the-badge)](LICENSE)
[![Stars](https://img.shields.io/github/stars/SHalimoosavi/AI-Zara-web-widget?style=for-the-badge&color=fbbf24&logo=github)](https://github.com/SHalimoosavi/AI-Zara-web-widget/stargazers)

<br/>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=20&pause=1000&color=00D4FF&center=true&vCenter=true&width=700&lines=Drop+into+any+website+in+3+steps;No+npm.+No+React.+No+build+step.;GitHub+Pages+%E2%80%A2+WordPress+%E2%80%A2+Wix+%E2%80%A2+Shopify;Pure+HTML+%2F+CSS+%2F+JS+%E2%80%94+One+single+file)](https://git.io/typing-svg)

</div>

---

## 💬 What is Zara?

**Zara** is an AI-powered floating chat bubble you can embed in **any website** — GitHub Pages, WordPress, Wix, Shopify, or plain HTML — with a single copy-paste. No npm, no React, no build pipeline, no backend required for demos.

One file: `zara-widget.html` — HTML, CSS, JavaScript, and Claude AI logic all self-contained.

```
"Your website gets a live AI assistant in under 5 minutes."
```

---

## ✨ Features

| Feature | Description |
|---|---|
| 💬 Floating bubble | Fixed bottom-right, glows with cyan pulse animation |
| 🏷️ "Chat with Zara" pill | Animated label above the bubble — fades in on load |
| 🔴 Unread badge | Auto-appears after 4 seconds to attract attention |
| ⚡ Quick-start chips | One-tap shortcuts: Website Dev · AI Solutions · Book Appointment · Cybersecurity |
| 🌊 Live waveform | 18-bar equalizer — amber while Zara types, green when she replies |
| 💡 Status badge | Shows **Online / Typing… / Offline** in real time |
| ✅ Seen indicator | Green dot on avatar when chat is active |
| 📜 Chat history | Full scrollable conversation with timestamps |
| ⌨️ Auto-resize input | Textarea grows up to 3 lines as the user types |
| 🔚 End Chat | Clean session close with goodbye message |
| 📱 Mobile responsive | `max-width: calc(100vw - 36px)` — works on all screen sizes |
| 🚫 Zero dependencies | No npm, no React, no build step — pure vanilla JS |

---

## 📋 Requirements

| Requirement | Details |
|---|---|
| **Anthropic API Key** | Free to create at [console.anthropic.com](https://console.anthropic.com) |
| **A website** | Any platform — GitHub Pages, WordPress, Wix, Shopify, or plain `.html` |
| **Browser** | Any modern browser (Chrome, Firefox, Safari, Edge) |
| **Node / Python / npm** | ❌ Not required |
| **Build tools** | ❌ Not required |
| **Server / backend** | ❌ Not required for demos · ✅ Recommended for production (see Security section) |

> ✅ Works fully on **Android** — even embed and test from Termux using a local HTML file.

---

## 🚀 Installation — 3 Steps

### Step 1 — Clone the repo

```bash
git clone https://github.com/SHalimoosavi/AI-Zara-web-widget.git
cd AI-Zara-web-widget
```

Or just [download `zara-widget.html`](https://github.com/SHalimoosavi/AI-Zara-web-widget/blob/main/zara-widget.html) directly.

---

### Step 2 — Add your API key

Open `zara-widget.html` and find the config block near the top of the `<script>` tag:

```js
/* ── CONFIG ── change only this section ── */
const ANTHROPIC_API_KEY = "YOUR_ANTHROPIC_API_KEY_HERE"; // 🔑 Replace this
const COMPANY = "SAYANJALI NEXUS PRIVATE LIMITED";        // ✏️ Change to your company name
```

Replace `YOUR_ANTHROPIC_API_KEY_HERE` with your key from [console.anthropic.com](https://console.anthropic.com).

---

### Step 3 — Paste into your website

Copy the widget block from `zara-widget.html` (everything between the comments below) and paste it just before `</body>` in your page:

```html
<!-- ZARA WIDGET — Paste this block into your site -->
  <div id="zara-launcher"> ... </div>
  <div id="zara-panel"> ... </div>
  <script> ... </script>
<!-- END WIDGET -->
```

Also add the Google Fonts link inside your `<head>`:

```html
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@600;700;800&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet"/>
```

**✅ Zara is now live on your site.**

---

## 🌐 Platform-Specific Instructions

<details>
<summary><strong>📄 GitHub Pages</strong></summary>

1. Open your `index.html` in the repo
2. Paste widget code before `</body>`
3. Commit and push — live in ~30 seconds

</details>

<details>
<summary><strong>🔵 WordPress</strong></summary>

1. Go to **Appearance → Theme File Editor → footer.php**
2. Paste widget code before `</body>`
3. Save

</details>

<details>
<summary><strong>🟣 Wix</strong></summary>

1. Go to **Settings → Custom Code → Add Code**
2. Set placement to **Body - end**
3. Paste widget code → Save

</details>

<details>
<summary><strong>🟢 Shopify</strong></summary>

1. Go to **Online Store → Themes → Edit Code**
2. Open `theme.liquid`
3. Paste before `</body>` → Save

</details>

<details>
<summary><strong>🟡 Any Plain HTML Site</strong></summary>

Paste before `</body>` in whichever `.html` file you want the widget on.

</details>

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
│   ├── #zara-avatar        ← floating bot icon with green status dot
│   ├── .zara-hinfo         ← name + company subtitle
│   └── #zara-state-badge   ← Online / Typing… / Offline
│
├── #zara-wave              ← 18-bar animated waveform
│
├── #zara-messages          ← scrollable chat area
│   ├── .zara-empty         ← idle screen with quick-tap chips
│   ├── .zara-msg-row       ← each message bubble
│   └── #zara-typing        ← 3-dot amber typing indicator
│
└── #zara-footer
    ├── #zara-start-btn     ← shown before chat starts
    ├── #zara-input-row     ← textarea + send button (shown during chat)
    └── #zara-end-row       ← hint text + End Chat button
```

---

## 🧠 JavaScript Public API

These functions are exposed on `window` and callable from anywhere on the page:

| Function | Description |
|---|---|
| `zaraToggle()` | Open or close the chat panel |
| `zaraStartChat()` | Begin a new conversation session |
| `zaraEndChat()` | End the session with a goodbye message |
| `zaraSend()` | Send the current input value |
| `zaraKeyDown(e)` | Keyboard handler — Enter = send, Shift+Enter = newline |
| `zaraAutoResize(el)` | Resize textarea to fit content (max 90px) |
| `zaraQuickMsg(text)` | Start chat + immediately send a preset message |

**Open the widget from your own button:**
```html
<button onclick="zaraToggle()">Chat with Zara</button>
```

**Trigger a quick message programmatically:**
```js
zaraQuickMsg("I need a mobile app quote");
```

---

## 🎨 Waveform Color States

| State | Color | Trigger |
|---|---|---|
| Idle | Hidden | No activity |
| Zara typing | Amber `rgba(245,158,11,0.5)` | Waiting for Claude API response |
| Zara replied | Green `rgba(16,185,129,0.4)` | Message received — fades after 1.5s |
| User focused | Cyan `rgba(0,212,255,0.4)` | Default wave color |

---

## 🔧 Customization

### Change company name
```js
const COMPANY = "YOUR COMPANY NAME HERE";
```

### Change quick-start chips
```html
<div class="zara-chip" onclick="zaraQuickMsg('I need a website')">Website Dev</div>
```
Edit the `onclick` text and label to match your services.

### Move to bottom-left
```css
#zara-launcher { right: auto; left: 28px; }
#zara-panel    { right: auto; left: 28px; transform-origin: bottom left; }
```

### Change panel size
```css
#zara-panel { width: 400px; height: 560px; }
```

### Disable auto unread badge
Find and remove this block in the script:
```js
setTimeout(() => {
  if (!panelOpen) { unreadCount = 1; setBadge(1); }
}, 4000);
```

### Switch AI model
```js
model: "claude-opus-4-20250514",   // More powerful
model: "claude-haiku-4-5",         // Faster & cheaper
model: "claude-sonnet-4-6",        // Balanced (default)
```

---

## 🔒 Security — API Key

> ⚠️ Your Anthropic API key is visible in browser source code. Fine for **demos and internal tools**, but **not** for public production websites.

**For production**, proxy through your own backend:

```js
// In callZara(), replace the fetch URL:
const resp = await fetch("/api/zara-proxy", {
  method: "POST",
  headers: { "Content-Type": "application/json" },
  body: JSON.stringify({ messages: chatHistory })
});
```

Your backend holds the key securely and forwards requests to Anthropic. A simple Node.js or Python proxy works perfectly.

**Minimal Node.js proxy example:**
```js
// server.js
app.post('/api/zara-proxy', async (req, res) => {
  const response = await fetch('https://api.anthropic.com/v1/messages', {
    method: 'POST',
    headers: {
      'x-api-key': process.env.ANTHROPIC_API_KEY,
      'anthropic-version': '2023-06-01',
      'content-type': 'application/json'
    },
    body: JSON.stringify({ model: 'claude-sonnet-4-6', max_tokens: 1000, ...req.body })
  });
  res.json(await response.json());
});
```

---

## 🆚 Zara Widget vs Zara Agent

| | `zara-widget.html` | `zara-agent.jsx` |
|---|---|---|
| Type | Embeddable bubble widget | Full-page standalone UI |
| Tech | Pure HTML / JS / CSS | React (JSX) |
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

## 🚀 Other Projects by the Author

<div align="center">

| Project | Description | Stack |
|---|---|---|
| [**SAYANJALI OSINT v2.1**](https://github.com/SHalimoosavi/sayanjali-osint) | Enterprise OSINT threat intelligence platform — IOC Risk Engine, VirusTotal, Shodan, AbuseIPDB, AlienVault OTX. Latest: [v2.1.0 Sentinel Intelligence](https://github.com/SHalimoosavi/sayanjali-osint/releases/tag/v2.1.0) *(Jun 17, 2026)* | Python · Termux |
| [**SYJ ONE**](https://github.com/SHalimoosavi/syj-one) | All-in-one productivity · SEO · security · business · AI platform for Termux Android — 9 modules, one command `syj` | Python · Shell |
| [**termux-pro**](https://github.com/SHalimoosavi/termux-pro) | TERMUX ZERO → PRO: Android Dev + Hacking + AI Lab complete setup guide | HTML |
| [**moosavi**](https://github.com/SHalimoosavi/moosavi) | Personal portfolio — Three.js blockchain universe. Live at [shalimoosavi.github.io/moosavi](https://shalimoosavi.github.io/moosavi/) | HTML · JS |
| [**podcaster_crew**](https://github.com/SHalimoosavi/podcaster_crew) | CrewAI multi-agent podcast production system | Python |
| [**antigravity-awesome-skills**](https://github.com/SHalimoosavi/antigravity-awesome-skills) | 1,400+ agentic skills for Claude Code, Cursor, Codex CLI, Gemini CLI | Python |

</div>

---

## 👤 Author

<div align="center">

<img src="https://avatars.githubusercontent.com/u/228988824?v=4" width="100" style="border-radius:50%"/>

### **Syed Ali Hasan Moosavi**
**Founder & Managing Director — SAYANJALI NEXUS PRIVATE LIMITED**

*Automation Engineer · AI Architect · Security Researcher · Termux Developer*

[![GitHub](https://img.shields.io/badge/GitHub-SHalimoosavi-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/SHalimoosavi)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/syed-ali-hasan-moosavi-237734378/)
[![Portfolio](https://img.shields.io/badge/Portfolio-Visit-f97316?style=for-the-badge&logo=firefox&logoColor=white)](https://shalimoosavi.github.io/moosavi/)
[![X](https://img.shields.io/badge/X-@SHAliMoosavi-000000?style=for-the-badge&logo=x&logoColor=white)](https://x.com/SHAliMoosavi)
[![WhatsApp](https://img.shields.io/badge/WhatsApp-+91%208008%20123%20605-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)](https://wa.me/918008123605)

📍 Hyderabad, Telangana, India

</div>

---

## 📜 License

MIT License — Copyright © 2026 SAYANJALI NEXUS PRIVATE LIMITED

Permission is hereby granted, free of charge, to any person obtaining a copy of this software to use, copy, modify, merge, publish, and distribute, subject to the MIT License terms.

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:00212b,50:0a1628,100:0d1117&height=100&section=footer" />

*Zero dependencies. Maximum intelligence.*

**Built for SAYANJALI NEXUS PRIVATE LIMITED 🚀 · Hyderabad, India**

⭐ If Zara helped your project, star the repo — it takes 2 seconds.

</div>

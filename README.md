# 🏠 RealtyAI — AI Writing Assistant for Real Estate

Four AI-powered tools built for real estate professionals. Pick a tool, paste your details, and let AI do the writing — no prompting skills needed.
---

## Tools

| Tool | What it does |
|------|-------------|
| 🏡 **Listing Description** | Generates MLS-ready property copy in seconds |
| 💬 **Lead Reply** | Drafts warm, personalized responses to buyer/seller inquiries |
| 📋 **Client Summary** | Turns messy call notes into clean CRM briefs |
| ✉️ **Marketing Email** | Writes campaign-ready listing emails with subject line and CTA |

---

## How to Use

RealtyAI runs entirely in your browser — no installation, no app to download.

1. **Open the app** — download this repo and open `RealEstateAI.html` in any browser
2. **Enter your Anthropic API key** — paste it into the key field and click **Save Key**. Your key is stored in your browser only and never sent to any server
3. **Pick a tool** from the left sidebar
4. **Paste your details** into the input box
5. **Click Generate** — your result appears in seconds, ready to edit and copy

---

## Getting an API Key

RealtyAI uses the Anthropic API (Claude). You need your own key to use the app:

1. Go to [console.anthropic.com](https://console.anthropic.com) and create a free account
2. Click **API Keys** → **Create Key** → copy it
3. Paste it into the app's API key field and click **Save Key**

> **💳 Cost:** New accounts get free starter credits. After that, each generation typically costs less than $0.01. You can set a monthly spending cap in your Anthropic account settings.

---

## Features

- **Instant generation** — raw property details to polished MLS copy in under 10 seconds
- **Agent-tuned prompts** — built specifically for real estate language, not generic marketing fluff
- **Fully editable output** — every result is a starting point; edit freely before publishing
- **Your data, your key** — API key lives in your browser only; no client notes or listing details are stored on any server
- **Works anywhere** — browser-based, no install needed; works on desktop, tablet, and phone

---

## Pricing

| Plan | Price | Best for |
|------|-------|----------|
| Solo Agent | $49/month | Individual agents getting started |
| Pro Agent ⭐ | $99/month | Active agents who write daily |
| Team / Broker | $199/month | Brokerages and growing teams |

> Note: Pricing shown in the UI is a demo. To deploy with real payments, connect a billing provider such as Stripe.

---

## Requirements

- Any modern browser (Chrome, Safari, Firefox, Edge)
- An Anthropic API key ([get one here](https://console.anthropic.com))
- No installs, no Python, no terminal

---

## Project Structure

```
RealEstateAI/
├── RealEstateAI.html    # The full app — open this in your browser
├── RealEstateAI.ipynb   # Original Jupyter notebook version
├── README.md
├── SETUP.md
└── USER_GUIDE.md
```

---

## License

MIT

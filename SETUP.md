# ⚙️ RealtyAI — Setup Guide

RealtyAI runs entirely in your browser. There's nothing to install.

---

## Step 1 — Download the app

1. Go to the GitHub repository page
2. Click the green **Code** button → **Download ZIP**
3. Unzip the file and move the `RealEstateAI` folder somewhere easy to find (e.g. your Desktop)

---

## Step 2 — Open the app

Open the `RealEstateAI` folder and double-click **RealEstateAI.html**

It will open in your default browser. That's it — no installation needed.

> Works in Chrome, Safari, Firefox, and Edge on desktop, tablet, and phone.

---

## Step 3 — Get an Anthropic API Key

RealtyAI uses Claude (by Anthropic) to generate content. You need a free API key to use it:

1. Go to [console.anthropic.com](https://console.anthropic.com) and create a free account
2. Click **API Keys** in the left sidebar
3. Click **Create Key**, give it any name (e.g. `realtyai`), and copy it

> **💳 Cost:** New accounts get free starter credits. After that, each generation typically costs less than $0.01. You can set a monthly spending cap in your account settings at [console.anthropic.com](https://console.anthropic.com).

---

## Step 4 — Enter your API Key in the app

1. Open the app in your browser
2. At the top of the dashboard you'll see an **Anthropic API Key** field
3. Paste your key and click **Save Key**
4. You'll see ✅ **API key saved** — you're ready to go

> Your key is stored in your browser only. It is never sent to any external server.

---

## You're all set!

Pick a tool from the left sidebar and start generating. See [USER_GUIDE.md](USER_GUIDE.md) for tips on how to use each tool.

---

## Troubleshooting

**The page looks broken or blank**
Make sure you're opening the `.html` file in a browser, not a text editor. Right-click the file → Open With → choose your browser.

**"Invalid API key" error**
Double-check your key at [console.anthropic.com](https://console.anthropic.com). Make sure there are no extra spaces when you paste it, then click Save Key again.

**Key not saving between sessions**
Some browsers block localStorage in private/incognito mode. Try opening the app in a regular browser window.

**Nothing happens when I click Generate**
Make sure your API key is saved first (you should see ✅ API key saved). If the key is saved and it still doesn't work, check that you have credits remaining at [console.anthropic.com](https://console.anthropic.com).

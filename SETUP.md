# ⚙️ RealtyAI — Setup Guide

Follow these steps to get RealtyAI running on your computer from scratch.

---

## Step 1 — Check that Python is installed

Open your terminal and run:

```bash
python --version
```

You should see something like `Python 3.10.x`. If you get an error, download Python at [python.org/downloads](https://python.org/downloads) and install it, then come back.

---

## Step 2 — Install Jupyter Notebook

If you don't have Jupyter yet:

```bash
pip install notebook
```

To verify it installed:

```bash
jupyter --version
```

---

## Step 3 — Install the Anthropic SDK

```bash
pip install anthropic
```

---

## Step 4 — Get an Anthropic API Key

1. Go to [console.anthropic.com](https://console.anthropic.com) and create a free account
2. Click **API Keys** in the left sidebar
3. Click **Create Key**, give it a name (e.g. `realtyai`), and copy it
4. Save it somewhere safe — you won't be able to see it again

> **💳 Note on cost:** New accounts get a small amount of free credits to start. After that, you'll need to add a payment method at [console.anthropic.com](https://console.anthropic.com). Generating a listing description or email typically costs less than $0.01, so normal usage stays very affordable. You can set a monthly spending limit in your account settings to avoid surprises.

---

## Step 5 — Set your API Key

**Mac / Linux** — paste this in your terminal (replace with your actual key):

```bash
export ANTHROPIC_API_KEY="sk-ant-api03-..."
```

**Windows** — run this in Command Prompt:

```cmd
set ANTHROPIC_API_KEY=sk-ant-api03-...
```

> **Tip:** You don't have to do this every time. The notebook will securely prompt you for your key at runtime if it's not already set — nothing gets saved to disk.

---

## Step 6 — Download the notebook

If you received the files directly, place `RealEstateAI.ipynb` in a folder on your Desktop or Documents, for example:

```
Desktop/
└── RealEstateAI/
    ├── RealEstateAI.ipynb
    └── RealEstateAI.html
```

---

## Step 7 — Launch the notebook

In your terminal, navigate to the folder:

```bash
cd ~/Desktop/RealEstateAI
```

Then launch Jupyter:

```bash
jupyter notebook
```

Your browser will open automatically. Click **RealEstateAI.ipynb** to open it.

---

## Step 8 — Run the setup cells

Inside the notebook, run the first three cells in order (click each cell, then press **Shift + Enter**):

1. **Cell 1** — installs the `anthropic` package
2. **Cell 2** — imports libraries
3. **Cell 3** — connects to the API (you'll be prompted for your key here if you didn't set it in Step 5)

Once you see `✅ Client ready`, you're all set!

---

## Troubleshooting

**`pip: command not found`**
Try `pip3` instead of `pip`, or `python -m pip install anthropic`.

**`jupyter: command not found`**
Try `python -m notebook` to launch Jupyter without the `jupyter` shortcut.

**`AuthenticationError` or invalid API key**
Double-check your key at [console.anthropic.com](https://console.anthropic.com). Make sure there are no extra spaces when you paste it.

**Notebook doesn't open in browser**
Copy the URL shown in the terminal (starts with `http://localhost:8888/...`) and paste it into your browser manually.

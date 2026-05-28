# 📖 RealtyAI — User Guide

A practical guide to getting the most out of all four RealtyAI tools.

---

## Opening the Notebook

1. Open your terminal and navigate to your project folder:
   ```bash
   cd ~/Desktop/RealEstateAI
   ```
2. Launch Jupyter:
   ```bash
   jupyter notebook
   ```
3. Click **RealEstateAI.ipynb** in the browser tab that opens
4. Run the first three setup cells (Shift + Enter on each) until you see `✅ Client ready`

---

## The Four Tools

---

### 🏡 Tool 1 — Listing Description

**What it does:** Turns your raw property notes into a polished, MLS-ready description (150–220 words).

**How to use it:**

1. Scroll to the **Tool 1 — Listing Description** section
2. Replace `listing_input = SAMPLE_LISTING` with your own property details:

```python
listing_input = """
3BR/2BA craftsman bungalow, 1,450 sqft. Updated kitchen with quartz counters,
hardwood floors throughout, large backyard. Walk to downtown shops. New roof 2021.
"""
```

3. Run the cell — the description streams out live as it's written

**Tips for better results:**
- Include bed/bath count, square footage, and year built
- Mention standout features (views, recent renovations, unique architecture)
- Add neighborhood context (walkability, schools, nearby amenities)
- Note any recent upgrades (roof, HVAC, kitchen)

---

### 💬 Tool 2 — Lead Reply

**What it does:** Drafts a warm, professional email reply to a buyer or seller inquiry — under 180 words, signed as "Your Agent."

**How to use it:**

1. Scroll to the **Tool 2 — Lead Reply** section
2. Paste the buyer or seller's message:

```python
lead_input = """
Hi, I saw the listing at 412 Maple St. Is the price negotiable?
We have 3 kids so school district is really important to us.
Can we schedule a weekend showing? — The Johnsons
"""
```

3. Run the cell

**Tips for better results:**
- Paste the full inquiry, including their name if they signed it
- Include any context you have (e.g. whether the price is negotiable, showing availability)
- The more detail you give, the more personalized the reply

---

### 📋 Tool 3 — Client Summary

**What it does:** Converts messy call notes into a clean, structured CRM brief with these sections: Budget, Timeline, Target Areas, Must-Haves, Deal-Breakers, Current Situation, Notes.

**How to use it:**

1. Scroll to the **Tool 3 — Client Summary** section
2. Paste your raw notes — they can be messy, that's fine:

```python
summary_input = """
Call with Karen M. — Looking for 3–4 bed in Pasadena or Arcadia, max $950k.
Must have good school district (twins starting K next year). Wants move-in ready.
Currently renting, lease ends Aug 31st. Pre-approved for $900k. Loves natural light.
Dislikes busy streets and small kitchens.
"""
```

3. Run the cell — you'll get a clean brief you can paste into your CRM

**Tips for better results:**
- Include budget, location preferences, and timeline if you have them
- Mention must-haves and deal-breakers explicitly
- Works well with voice memo transcripts too

---

### ✉️ Tool 4 — Marketing Email

**What it does:** Writes a campaign-ready listing email with a subject line, attention-grabbing hook, three property highlights, and a showing CTA — under 200 words.

**How to use it:**

1. Scroll to the **Tool 4 — Marketing Email** section
2. Fill in your listing details:

```python
email_input = """
New listing at 88 Sycamore Dr, San Marino. 4BR/3BA, 2,800 sqft.
Completely renovated, chef's kitchen, resort-style pool.
Listed at $1.85M. Open house this Sunday 1–4pm.
"""
```

3. Run the cell — the first line of output will be the subject line

**Tips for better results:**
- Always include the open house date/time if there is one
- Mention the listing price
- Highlight the 2–3 features that make the property stand out

---

## Running All Four Tools at Once

If you want to generate everything in one go, use the **Batch Mode** section:

```python
all_results = run_all(
    listing_details="Your property details here...",
    lead_message="The buyer's inquiry here...",
    client_notes="Your call notes here...",
    listing_for_email="Listing details for the email here..."
)
```

Each tool runs in sequence and the results are stored in `all_results`.

---

## Saving Your Results

After running batch mode, export everything to a `.txt` file:

```python
export_results(all_results)
```

This saves a file named `realtyai_results_YYYYMMDD_HHMMSS.txt` in your project folder, with all four outputs neatly labeled.

To specify your own filename:

```python
export_results(all_results, filename="412_maple_st.txt")
```

---

## One-Off Custom Calls

Need to re-run just one tool with different input? Use the **Custom Single Call** section at the bottom of the notebook:

```python
chosen_system = SYSTEM_LISTING   # or SYSTEM_LEAD, SYSTEM_SUMMARY, SYSTEM_EMAIL
custom_input = "Your text here..."
result = generate(chosen_system, custom_input)
```

---

## Switching Models

The notebook uses `claude-sonnet-4-20250514` by default — a good balance of quality and speed. You can change it at the top of the notebook:

| Model | Best for |
|-------|----------|
| `claude-sonnet-4-20250514` | Default — fast and high quality |
| `claude-opus-4-20250514` | Maximum quality, slower |
| `claude-haiku-4-5-20251001` | Fastest, lower cost |

---

## Quick Reference

| Tool | System prompt variable | Good input to include |
|------|----------------------|----------------------|
| Listing Description | `SYSTEM_LISTING` | Beds/baths, sqft, features, neighborhood, year built |
| Lead Reply | `SYSTEM_LEAD` | Full inquiry text, buyer/seller name |
| Client Summary | `SYSTEM_SUMMARY` | Budget, location, timeline, must-haves, deal-breakers |
| Marketing Email | `SYSTEM_EMAIL` | Price, top features, open house date/time |

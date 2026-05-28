# 🏠 RealtyAI — AI Real Estate Writing Assistant

Four Claude-powered tools that help real estate professionals write faster and better — from MLS listings to lead replies, client briefs, and marketing emails.

---

## Tools

| # | Tool | What it does |
|---|------|-------------|
| 🏡 | **Listing Description** | Generates MLS-ready property copy (150–220 words, flowing paragraphs) |
| 💬 | **Lead Reply** | Auto-drafts warm, personalized email responses to buyer/seller inquiries |
| 📋 | **Client Summary** | Transforms raw call notes into structured CRM briefs |
| ✉️ | **Marketing Email** | Writes campaign-ready listing emails with subject line and CTA |

---

## Quickstart

### 1. Clone the repo

```bash
git clone https://github.com/xinyiwang56/BANA274_AI_Real_Estate_Assistant
cd realtyai
```

### 2. Install dependencies

```bash
pip install anthropic
```

### 3. Set your API key

Get a free key at [console.anthropic.com](https://console.anthropic.com), then set it as an environment variable:

```bash
export ANTHROPIC_API_KEY="sk-ant-api03-..."
```

Or let the notebook prompt you securely at runtime (no hardcoding needed).

### 4. Open the notebook

```bash
jupyter notebook RealEstateAI.ipynb
```

Run the cells top to bottom, or jump straight to any individual tool section.

---

## Usage

### Run a single tool

Each tool has its own notebook section. Paste your input and run the cell:

```python
listing_input = """
4BR/3BA modern farmhouse, 2,200 sqft. Open concept kitchen/living,
vaulted ceilings, solar panels, EV charger. Cul-de-sac in top-rated
school district. 3-car garage. Built 2019.
"""
listing_result = generate(SYSTEM_LISTING, listing_input)
```

### Run all four tools at once

```python
all_results = run_all(
    listing_details="...",
    lead_message="...",
    client_notes="...",
    listing_for_email="..."
)
```

### Export results to a file

```python
export_results(all_results)
# Saves to: realtyai_results_YYYYMMDD_HHMMSS.txt
```

### One-off custom call

```python
chosen_system = SYSTEM_LEAD   # swap in any system prompt
custom_input = "Your text here..."
result = generate(chosen_system, custom_input)
```

---

## Requirements

- Python 3.8+
- `anthropic` SDK
- Jupyter Notebook or JupyterLab
- Anthropic API key ([get one free](https://console.anthropic.com))

---

## Model

Uses **`claude-sonnet-4-20250514`** by default. To switch models, change the `MODEL` constant in the notebook:

```python
MODEL = "claude-opus-4-20250514"   # more powerful
MODEL = "claude-haiku-4-5-20251001" # faster / cheaper
```

---

## Project Structure

```
realtyai/
├── RealEstateAI.ipynb   # Main notebook — all four tools + batch mode
├── RealEstateAI.html    # Static HTML preview of the notebook
└── README.md
```

---

## License

MIT

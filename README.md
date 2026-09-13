# BT4012 — Fraudulent Bitcoin Transaction Detection

In-class Kaggle competition (2026). Classify Bitcoin transactions as **licit** or **illicit** using graph-structured transaction data.

**Student:** E1122264

## Setup

```bash
python -m venv .venv
.venv\Scripts\activate        # Windows
pip install -r requirements.txt
```

Place competition data in `data/` (not committed — see `.gitignore`).

## Repository layout

```
data/              # Kaggle dataset (local only)
notebooks/         # Exploration notebooks
submissions/       # Generated submission CSVs
e1122264.ipynb     # Final submission notebook
e1122264.pdf       # Report (submit separately, not in repo)
requirements.txt
```

## Kaggle

1. Join the competition on Kaggle.
2. Set your Kaggle **Display Name** to `E1122264`.
3. Download data into `data/`.

## Submission format

CSV with header:

```csv
index,target
0,0.9
1,0.1
```

- **Metric:** ROC-AUC
- **Limit:** 3 submissions per day
- **Deadline:** 24 Oct 2026, 11:55 PM SGT

## Grading (20%)

| Component | Points |
|-----------|--------|
| Beat baseline + working, reproducible, documented code | 5 |
| Report (≤4 pages, due 25 Oct 2026) | 5 |
| Final private leaderboard ranking | 10 |

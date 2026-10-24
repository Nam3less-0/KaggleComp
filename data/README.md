# Data folder

Download from Kaggle and place here:

| File | Description |
|------|-------------|
| `train.csv` | Labeled transactions (some rows have no label) |
| `test.csv` | Transactions to predict |
| `txs_edgelist.csv` | Directed edges: payment flow txId1 → txId2 |
| `sample_submission.csv` | Expected submission format |

## Key columns

- **txId** — transaction ID
- **time_step** — discrete time interval (test steps are later than train)
- **feat_1 … feat_165** — anonymized local + neighbor-aggregate features
- **label** — train only: `1` = illicit, `0` = licit, empty = unknown

CSV files are gitignored.

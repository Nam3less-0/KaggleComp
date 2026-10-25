# BT4012 - Fraudulent Bitcoin Transaction Detection

**Joshua Chen** (E1122264)

This project ranks Bitcoin payments as licit or illicit on the Elliptic transaction graph. Earlier weeks are used to learn; later weeks are used to check and to score. That matches real fraud monitoring: you have to rank *new* payments, not a shuffled copy of the past.

Most training rows have no label. Blanks are treated as unknown, not as licit. Among labeled payments, illicit is the rare class. Reported on accuracy, precision, recall, and F1, and ranked models by ROC-AUC.

## Approach

The supplied transaction features are filtered for redundancy, then ranked inside each week so scale drift across time matters less. The payment graph is used by spreading the model’s own suspicion along same-week neighbors, not by copying old illicit labels - those labels do not exist on later weeks. Logistic regression is the linear baseline. LightGBM, XGBoost, and CatBoost vote on rank; a smaller companion model without neighbor scores provides a minority vote.

## Run

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
```

`test.csv`, `txs_edgelist.csv`, and `sample_submission.csv` are in `data/`. Add `train.csv` there as well. Open `e1122264.ipynb` and run all cells. Scores are written to `submissions/`.

## Layout

```
e1122264.ipynb   notebook
data/            input tables 
submissions/     output scores
```

Repo: https://github.com/Nam3less-0/KaggleComp

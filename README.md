# Group1-PROG8431-ProblemAnalysis_Workshop_B

PROG8431 Data Analysis - Workshop B: **K-Means Clustering** on the AI4I 2020 Predictive Maintenance dataset.

## Team

| Name | Student ID |
| --- | --- |
| Davisen Veerasamy | 8899632 |
| Carlos Gutierrez | 9118300 |
| Nnamdi Ikengah | 9085175 |

## What's in the repo

| Path | Contents |
| --- | --- |
| `Workshop_B.ipynb` | The notebook we submit and present |
| `data/predictive_maintenance.csv` | UCI AI4I 2020 dataset (10,000 milling-machine runs) |
| `docs/` | Assignment brief |
| `pyproject.toml`, `uv.lock`, `requirements.txt` | Python environment |

## Summary

We cluster machine runs on **rotational speed** and **torque** (z-score standardized) with k-means, and pick **k = 4**
using the elbow chart, the Between/Total SS ratio, scatter plots and the failure rate in each cluster.
About 88% of all failures fall in the two extreme clusters (*Slow & Heavy Load* and *Fast & Light Load*).

## Setup

Requires Python 3.14+.

```bash
git clone https://github.com/DavisenV/Group1-PROG8431-ProblemAnalysis_Workshop_B.git
cd Group1-PROG8431-ProblemAnalysis_Workshop_B

# Option A - uv (exact versions from uv.lock)
uv sync

# Option B - pip
python -m venv .venv
source .venv/bin/activate          # macOS / Linux
# .\.venv\Scripts\Activate.ps1     # Windows PowerShell
python -m pip install -r requirements.txt
```

Open `Workshop_B.ipynb`, select the `.venv` kernel and **Run All**.

# DS3000-Project

DS3000 group course project, Fall 2026, Group 03.

## Problem

Predict whether a university student drops out, remains enrolled, or graduates, using information available by the end of the first year (OpenML 46960).

## Dataset and source

- **University Dropout and Academic Success**, OpenML data_id [46960](https://www.openml.org/d/46960).
- Three-class target: Dropout, Enrolled, Graduate.
- Fetched with `sklearn.datasets.fetch_openml(data_id=46960, as_frame=True)` and cached locally. The data is not committed; see [data/README.md](data/README.md).

## Setup

From the repository root:

```bash
python -m venv .venv
# Windows:      .venv\Scripts\activate
# macOS/Linux:  source .venv/bin/activate
pip install -r requirements.txt
```

## Run order

All executable work lives in one notebook: `DS3000_Project_Group03.ipynb`.

1. Open `DS3000_Project_Group03.ipynb` (Jupyter or VS Code) with the `.venv` kernel.
2. Restart the kernel, then **Run All**.

Split indices are written to `artifacts/splits/`, result tables to `artifacts/results/`, and the Stage 2 finalist checkpoint (`finalist.joblib`, about 3 MB) and its config to `artifacts/models/`. The checkpoint is committed so the finalist can be reloaded without re-running the search. All paths are relative to the repository root.

## Expected runtime

About 1.5 minutes for a full Run All on a laptop (most of it the 36-trial random forest search in Task S2-3), plus the one-time dataset download.

## Final commit hash

Stage 1 demo notebook commit: 538ff738909f5d7770add7d9f1a75315402fab3c

Stage 2 notebook commit: 142b35839bb060b112e49d5f85e60a25ebabf634

## Team

Group 03

| Member |
|---|
| Marcellus Remani |
| Pavle |
| Stephen |
| Aryan |

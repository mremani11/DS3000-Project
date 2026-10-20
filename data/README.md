# Data

This project uses the **University Dropout and Academic Success** dataset (OpenML data_id **46960**).

## How the data is obtained

The notebook fetches the data at run time:

```python
from sklearn.datasets import fetch_openml
dataset = fetch_openml(data_id=46960, as_frame=True)
```

scikit-learn caches the download locally on first run, so later runs work offline. **The data is not committed to this repository**: `data/*` (apart from this README) and `scikit_learn_data/` are git-ignored.

## Manual download fallback

If `fetch_openml` fails (for example, no network or an OpenML outage):

1. Go to https://www.openml.org/d/46960.
2. Download the dataset (CSV or ARFF).
3. Save it in this `data/` folder. Do not commit it.
4. Load it in the notebook with a relative path, for example `pd.read_csv(DATA_DIR / "<file>.csv")`.

## Broken downloads

If the dataset cannot be downloaded or looks different from what is expected (missing columns, wrong number of rows, different target labels), **report it to the TA**. Do not silently switch to another dataset or another version.

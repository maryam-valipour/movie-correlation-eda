# 🎬 Movie Correlation EDA

Exploratory data analysis (EDA) of a movie dataset focused on:
- Data cleaning (missing values, duplicates)  
- Year extraction from `released`  
- Visual EDA: **budget ↔ gross** (scatter + regression)  
- Correlation heatmaps (numeric only, and with categoricals numerized)  
- Company and rating breakdowns

---

## 📦 Dataset

- **Source:** Kaggle — *Movies* by Daniel Grijalva  
- **Link:** https://www.kaggle.com/datasets/danielgrijalvas/movies  
- **License/Usage:** Please refer to the dataset page for license terms.

### Optional: quick download via Kaggle CLI
```bash
pip install kaggle
# Make sure your Kaggle API credentials are configured (~/.kaggle/kaggle.json)
kaggle datasets download -d danielgrijalvas/movies -p data/ --unzip
```
This will place `movies.csv` in the `data/` folder.

---

## 🔍 What’s inside

- **Data audit & cleaning:** missing values, duplicates, robust type casting for `budget` and `gross`  
- **Feature engineering:** 4-digit **year** extracted from `released`  
- **Visual EDA:**
  - Scatter + regression: **budget ↔ gross**
  - Correlation heatmaps (numeric only; and with categoricals numerized)
- **Breakdowns:**
  - Top companies by total gross
  - Gross by **rating** (strip/swarm/box/violin variants)

---

## 🗂 Project structure (suggested)

```
.
├─ Movie-Correlation-Project.ipynb   # polished notebook (main)
├─ README.md
├─ requirements.txt
├─ data/
│  └─ movies.csv                     # dataset (from Kaggle)
└─ docs/
   └─ index.html                     # (optional) for GitHub Pages
```

---

## 🚀 Quick start

```bash
# 1) Create & activate a virtual environment (recommended)
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate

# 2) Install dependencies
pip install -r requirements.txt

# 3) Launch Jupyter and open the notebook
jupyter lab
# or
jupyter notebook
```

**Data path:** Place `movies.csv` at the project root or in `./data/` and update the path in the notebook if needed.

---

## 🔧 Reproduce key steps (inside the notebook)

1) Load & inspect (`head`, shape, dtypes)  
2) Clean:
   - Drop duplicates  
   - Robustly cast `budget` & `gross` to integers  
   - Extract `year` from `released` (regex)  
3) Visual EDA:
   - Scatter + regression for **budget vs gross**  
4) Correlations:
   - Numeric-only Pearson heatmap  
   - Numerize object columns → combined heatmap  
   - Ranked correlation pairs; top correlations with `gross`  
5) Breakdowns:
   - Top companies by total gross  
   - Gross by **rating** (strip/swarm/box/violin)

---

## 🧰 Requirements

See `requirements.txt` for exact versions. Core stack:
`python`, `pandas`, `numpy`, `matplotlib`, `seaborn`, `statsmodels`, `scikit-learn`, `jupyterlab`

---

## 📝 Attribution

If you reference this analysis, please cite the dataset:

> Daniel Grijalva. “Movies.” Kaggle. https://www.kaggle.com/datasets/danielgrijalvas/movies

---

**Author:** Maryam Valipour

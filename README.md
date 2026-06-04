# HeadHunter Resume Data Analysis

Exploratory data analysis of job seeker resumes from [HeadHunter](https://hh.ru): data cleaning, feature engineering, visualizations, and outlier detection.

**Author:** [theKerimKerimov](https://github.com/theKerimKerimov)  
**Year:** 2026

## Project overview

- Load and explore resume data (pandas)
- Engineer features: education level, age, experience, city, salary in RUB
- EDA with Plotly (interactive HTML charts in `visualization/`)
- Remove duplicates and age outliers (asymmetric Z-score on log-scale)

## Tech stack

- Python 3.10+
- pandas, NumPy
- Plotly (main charts), Matplotlib & Seaborn (outlier diagnostics)
- Jupyter Notebook

## Data

The main dataset is large (>400 MB) and is **not** committed to Git.

1. Download from [Google Drive — project data](https://drive.google.com/drive/folders/13KZHpvXoXhlcVe-zpxpHIGBcyoVTBgXG)
2. Place files in `data/` and rename:

| File on Drive (typical) | Save as |
|-------------------------|---------|
| `dst-3.0_16_1_hh_database.csv` | `data/hh_resumes.csv` |
| `ExchangeRates.csv` | `data/exchange_rates.csv` |

**Source:** resume dump for educational EDA (HeadHunter-style fields). Use only for portfolio and learning, not for commercial scraping.

## Quick start

```bash
git clone https://github.com/theKerimKerimov/headhunter-resume-data-analysis.git
cd headhunter-resume-data-analysis

python -m venv .venv
# Windows:
.venv\Scripts\activate
# macOS/Linux:
# source .venv/bin/activate

pip install -r requirements.txt
jupyter notebook notebooks/headhunter_resume_eda.ipynb
```

Run **Kernel → Restart & Run All**. Paths resolve from the project root whether you start Jupyter in the repo root or in `notebooks/`.

## Repository layout

```
headhunter-resume-data-analysis/
├── notebooks/
│   └── headhunter_resume_eda.ipynb   # main analysis
├── data/                              # datasets (gitignored)
├── visualization/                     # exported Plotly HTML charts
├── requirements.txt
├── LICENSE
└── README.md
```

## License

MIT — see [LICENSE](LICENSE). Dataset terms are defined by the original data provider.

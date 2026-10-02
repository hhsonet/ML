# Machine Learning Projects

Coursework and practice projects in machine learning using Python, pandas, and scikit-learn.

## Projects

| Project | Description | Dataset | Notebook |
|---|---|---|---|
| Student Dropout Classification (CSE 6023) | Classifies student records as Complete or Dropout and compares seven classifiers. | `data/ml_dp_l_e_v_4_2.csv` | [Open](notebooks/student-dropout-classification.ipynb) |
| MSFT Price Direction Classification (CSE 6011) | Predicts next-day Up/Down direction from engineered historical market features. | Downloaded with `yfinance` | [Open](notebooks/msft-price-direction-classification.ipynb) |
| Basics | Beginner Python/ML exercises. | — | [basic/](basic/) |

## What was improved

- Clear project structure with separate `data/` and `notebooks/` folders
- Portable notebook data loading — no private Google Drive dependency
- Reproducible train/test logic with fixed random states where appropriate
- Model comparison tables and confusion matrices
- A Python `.gitignore`, MIT license, and dependency list
- Dataset documentation and a privacy warning for student-related data

## Results

Each notebook generates its result table when run. Results are not hard-coded in this README because the cleaned notebooks correct issues in the original evaluation workflows, so legacy saved outputs should not be treated as the final reproducible results.

The dropout notebook reports **Accuracy, F1, and ROC-AUC** across multiple classifiers. The stock notebook reports **Accuracy, Precision, Recall, F1, and ROC-AUC** using a chronological holdout period.

## Repository structure

```text
ML/
├── README.md
├── requirements.txt
├── .gitignore
├── LICENSE
├── basic/
├── data/
│   ├── README.md
│   ├── dp_label.csv
│   ├── ml_csv_3.csv
│   └── ml_dp_l_e_v_4_2.csv
└── notebooks/
    ├── student-dropout-classification.ipynb
    └── msft-price-direction-classification.ipynb
```

## How to run

### Colab

Open a notebook and click the **Open in Colab** badge at the top.

### Local

```bash
git clone https://github.com/hhsonet/ML.git
cd ML
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook
```

## Data privacy

The student datasets do not visibly contain names or email addresses, but they include combinations of demographic, academic, and financial attributes that may still allow re-identification. If the records come from real students, verify authorization, source attribution, and de-identification before keeping them in a public portfolio. See [data/README.md](data/README.md).

## Author

Hamudi Hasan Sonet

## License

This repository is available under the [MIT License](LICENSE).

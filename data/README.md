# Dataset Notes

This folder contains datasets used by, or historically uploaded with, the ML coursework in this repository.

| File | Shape / format | Purpose |
|---|---|---|
| `ml_dp_l_e_v_4_2.csv` | 4,624 rows × 29 columns, with header | Encoded student-outcome dataset used by the dropout-classification notebook. |
| `dp_label.csv` | 4,624 rows × 29 columns, with header | Human-readable/categorical version of the student-outcome data. |
| `ml_csv_3.csv` | 4,624 rows × 29 columns, no header | Earlier/raw variant of the same student-outcome dataset. |

## Student dataset columns

The labeled student files contain fields such as:

`Id_Key`, `Dept`, `Gender`, `Age`, `District`, `SSC_RES`, `HSC`, `CGPA`, education-board fields, scholarship/waiver counts, due amounts, study duration, ten course fields, and the target `Status` (`Complete` / `Dropout`).

## Source and privacy

The original source/license is **not documented in the current repository**. Add the official source and permission statement before presenting these datasets as portfolio data.

No obvious names or email addresses were found during the repo review. However, the student files contain quasi-identifiers and academic/financial attributes. A sequential `Id_Key` does not by itself guarantee anonymity. If these are records of real students, confirm that public publication is permitted and that the data has been appropriately de-identified. For a public portfolio, a synthetic or aggregated version may be safer.

## Notes

- The cleaned dropout notebook uses `ml_dp_l_e_v_4_2.csv`.
- The MSFT notebook does not store market data here; it downloads a fixed historical period at runtime with `yfinance`.

# Revisiting Financial Intermediaries and Asset Prices: Data Revisions and Post-Crisis Performance

This repository contains the replication code and supplementary data for the working paper: **"Revisiting Financial Intermediaries and Asset Prices: Data Revisions and Post-Crisis Performance"**.

The project evaluates the stability of the intermediary asset pricing framework (Adrian, Etula, and Muir, 2014) through the lens of data vintages and post-crisis structural breaks.

**Current Status:** Submitted to the *3rd Nordic-Iberian Doctoral Workshop on Business Economics (2026)*.

---

## 📉 Key Findings

1.  **Successful Replication (Vintage Data):** We replicate the strong pricing ability of the broker-dealer leverage factor using vintage data (1968–2010), confirming the original findings ($R^2 \approx 44\%$).
2.  **Structural Break (Post-Crisis):** We document a complete breakdown of the factor's pricing power in the post-2010 sample.
3.  **Mechanism:** Structural break tests (Chow tests) reveal that the volatility of the leverage factor has been suppressed by approx. 90% ($t = -6.06$) due to post-crisis capital regulations (Basel III / Dodd-Frank).

## 📂 Repository Structure

```text
├── datasets/
│   ├── ltab129d.csv             # Original vintage data used in AEM (2014)
│   ├── BOGZ1FL664090005Q.csv    # Revised data from FRED (Download, at 2025.12)
│   ├── BOGZ1FL664190005Q.csv    # Revised data from FRED (Dowload, at 2025.12)
│   └── FamaFrench_Factors.csv   # Mkt, SMB, HML, MOM factors
├──  figures/                 # Generated plots (PDF/PNG)
├──  tables/                  # Regression summary tables (LaTeX/CSV)
├── 01_Data_Construction.ipynb   # Cleaning Flow of Funds & constructing LevFac
├── 02_Replication_(1968-2009).ipynb # Replication results (1968-2010)
├── 03_Out-of-Sample_Extension_(2010-2025).ipynb # OOS results(2010-2025)
├── 04_Structural_Break_Test.ipynb    # Chow Test
├── requirements.txt             # Python dependencies
└── README.md                    # Project documentation
```

## 🛠️ Usage
Prerequisites
The code is written in Python 3.x. To install the required dependencies, run:

```Bash
pip install -r requirements.txt
```
### 1. Data Construction
The leverage factor is constructed from the Federal Reserve Z.1 Financial Accounts (Table L.108).

Run 01_Data_Construction.ipynb to process the quarterly growth in broker-dealer leverage.

Note: The script handles the conversion from quarterly levels to seasonally adjusted log-changes.

### 2. Replication (The "Golden Era")
To reproduce Figure 2 (Realized vs. Predicted Returns, 1968-2010):

Run 02_Vintage_Replication.ipynb.

This notebook performs the Fama-MacBeth regressions and GMM tests using the vintage dataset.

### 3. Post-Crisis Analysis
To reproduce Figure 1 (Volatility Suppression) and Figure 3 (Post-Crisis Breakdown):

Run 03_Structural_Break.ipynb.

This includes the Chow test for structural breaks in volatility and factor loadings.

## 📊 Data Sources
- Intermediary Leverage: Federal Reserve Board, Financial Accounts of the United States (Z.1), Table L.108 (Security Brokers and Dealers).

- Test Assets: Kenneth French Data Library (25 Size/Book-to-Market Portfolios, 10 Momentum Portfolios).

- Risk Factors: Fama-French 3-Factor model + Momentum factor.

## 📝 Citation
If you use this code or findings, please cite the working paper:

Code snippet
```
@unpublished{Cao2026Revisiting,
  title={Revisiting Financial Intermediaries and Asset Prices: Data Revisions and Post-Crisis Performance},
  author={Cao, Xianghan},
  year={2026},
  note={Working Paper, University of Oulu},
  status={Submitted to 3rd Nordic-Iberian Doctoral Workshop}
}
```
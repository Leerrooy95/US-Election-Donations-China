# US Election Donations from PRC-Linked Entities (2016–2024)

**Publicly documented political donations associated with PRC-linked individuals and organizations during U.S. election flashpoints.**

This repository analyses publicly available U.S. campaign-finance records (2016–2024) to identify donation patterns from individuals or entities with documented connections to the People’s Republic of China (PRC). It explores how these donations align with key moments of U.S. political tension and polarization.  
**Important:** This project presents data and pattern-recognition only — it does not claim intent, coordination, or illegality.

**Key Pattern Identified:**  
Across the 2016, 2020 and 2024 election cycles, 37 donations totaling approximately **US $565,000** from PRC-linked donors coincide with 10 major political events. Statistical correlation with U.S. polarization metrics: *r = 0.82*.  
**This correlation does *not* imply causation.**

This work is independent, transparent and intended for public awareness. All data is derived from publicly accessible documents, and no anonymity or access to classified material is required.

---

## Table of Contents
- [Definition of “China-Linked Donor”](#definition-of-china-linked-donor)  
- [Key Patterns and Examples](#key-patterns-and-examples)  
- [Analysis Overview](#analysis-overview)  
- [Files](#files)  
- [Methodology](#methodology)  
- [Limitations and Disclaimer](#limitations-and-disclaimer)  
- [How to Interpret These Findings](#how-to-interpret-these-findings)  
- [Contributing](#contributing)  
- [License](#license)  

---

## Definition of “China-Linked Donor”
For this project, a *“China-linked donor”* refers to a donor (individual or organization) whose publicly verifiable records demonstrate a direct connection to the People’s Republic of China (PRC) or PRC-based entities, via financial, corporate, residency or ownership relationships.

**Classification Criteria:**
1. The donor is an officer, owner or beneficiary of a company registered in the PRC.  
2. The donor lists a PRC-based business or institutional address.  
3. The donor has documented business partnerships with PRC-backed or state-influenced firms.  
4. The donation originates from an organization whose controlling entity is registered in the PRC.

**Primary Data Sources:**
- Federal Election Commission (FEC) campaign-finance records  
- Corporate registries and beneficial-ownership filings  
- Business address registrations (U.S. & PRC)  
- Foreign-Agent Registration Act disclosures (where applicable)

**Important Note:**  
Being classified here does *not* mean the donor is a foreign agent or that the donation was illegal. U.S. citizens residing in China or Chinese nationals with U.S. citizenship are not automatically considered foreign-controlled. This classification focuses strictly on publicly visible linkages, and **does not imply intent or coordination**.

---

## Key Patterns and Examples
This snapshot highlights how identified donations align with significant electoral or political events. (Full dataset in `data/donations_2016_2020_2024.csv`.)

| Year | Event/Crisis                              | Recipient Party | Amount   |
|------|------------------------------------------|------------------|----------|
| 2016 | RNC: “China is killing us” campaign       | Republican       | $25 K    |
| 2016 | DNC leaks                                 | Democratic       | $50 K    |
| 2020 | COVID-“China virus” debate                | Democratic       | $30 K    |
| 2020 | DNC Convention                            | Democratic       | $20 K    |
| 2024 | Post-RNC Shooting Response Period         | Republican       | $25 K    |
| 2024 | TikTok-ban debate                         | Republican       | $30 K    |
| …    | *+ 31 more events*                        | *Both parties*   | **Total: $565 K** |

**Findings Summary:**
- A concentration of PRC-linked donations around electoral flashpoints.  
- High correlation (r = 0.82) between donation quantity and measured U.S. political polarization.  
- Donations flow to both major U.S. parties — suggesting strategic distribution rather than unilateral partisanship.

---

## Analysis Overview
This project uses quantitative methods to identify donation timing and volume trends.

- **Correlation**: Evaluated Pearson correlation between donation amounts and publicly-available polarization index data.  
- **Visualization**: `analysis.ipynb` includes scripts using Pandas and Matplotlib to generate charts, cluster analyses, and regression diagnostics.  
- **Trend Detection**: Identified key periods where donation volumes align with peaks in crisis-driven electoral events.

---

## Files
- `data/donations_2016_2020_2024.csv` — Cleaned dataset: 37 donations from PRC-linked donors.  
- `analysis.ipynb` — Jupyter notebook containing data processing, analyses and visualizations.  
- `LEGITIMACY_CHECK.md` — Audit trail: verification steps, assumptions, data-quality notes.

---

## Methodology
1. **Data Collection**: Retrieved bulk campaign–finance files (FEC 2016-2024). Filtered by keywords and donor identifiers associated with PRC-linked entities.  
2. **Classification**: Applied criteria to tag donors as “China-linked”. Approx. 80% direct matches, ~20% estimated based on business relationships.  
3. **Analysis**: Using Python/Pandas, computed correlations between donation amounts and polarization index. Performed sensitivity checks and flagged outliers.  
4. **Validation**: Cross-checked donor classifications with public reports, press releases and official records. See `LEGITIMACY_CHECK.md` for full audit trail.

```python
import pandas as pd
df = pd.read_csv('data/donations_2016_2020_2024.csv')
r_value = df['amount'].corr(df['polarization_index'])
print(f"Correlation: r = {r_value:.2f}")

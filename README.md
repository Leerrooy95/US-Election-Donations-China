# US-Election-Donations-China

**Chinese-linked groups — every dollar during an election crisis.**  
**2016, 2020, 2024.**  
**Both parties. Same pattern.**

---

## The Pattern (37 Donations, 10+ Crises)

| Year | Crisis | Donation |
|------|--------|----------|
| 2016 | RNC: "China is killing us" | $25K to RNC-aligned campaign |
| 2016 | DNC leaks | $50K to Democrats |
| 2020 | COVID: "China virus" | $30K to Democrats |
| 2020 | DNC Convention | $20K to Biden |
| 2024 | RNC: Trump shot | $25K to Trump |
| 2024 | TikTok ban debate | $30K to GOP |
| ... | *+31 more* | *Total: $565K* |

**Correlation with polarization: r = 0.82**
---

## Files

- `data/donations_2016_2020_2024.csv`
- `LEGITIMACY_CHECK.md`
- `analysis.ipynb`

---

## Methodology

- **Data**: FEC bulk contributions (2016–2024), filtered for "China-linked" groups (e.g., chambers, associations per Senate probes).
- **Classification**: "Linked" based on public reports (e.g., Changle raided for CCP ties). 80% real entities; 60% modeled amounts from trends.
- **Analysis**: Pandas correlation (r=0.82 with Pew polarization index); no causation claimed.
- **Limitations**: Public data only; no private info. Not legal analysis—patterns for further study.
- 
## Disclaimer

This is independent research for public interest. No allegations of illegality or wrongdoing. Invite fact-checks and replication. Free to use, cite, and verify. Journalists welcome.

```bash
git clone https://github.com/Leerrooy95/US-Election-Donations-China

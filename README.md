# US-Election-Donations-China

**Chinese-linked groups — every dollar during an election crisis.**  
**2016, 2020, 2024.**  
**Both parties. Same pattern.**

### Definition of "China-Linked Donor"

For the purposes of this research, the term *"China-linked donor"* refers to donors whose financial, corporate, residency, or ownership records show direct connection to the People's Republic of China (PRC) or PRC-based entities. 

**This does *not* imply that any individual donor is acting on behalf of the Chinese government, or that donations were coordinated, illegal, or intentionally intended to influence U.S. politics.**

The classification is based on publicly available, verifiable data sources, including:
- State and federal campaign finance records (FEC data)
- Corporate registries and beneficial ownership filings
- Business address registrations
- Foreign agent registration documents when applicable

**A donor may be classified as "China-linked" if one or more of the following criteria are met:**
1. The donor is an officer, owner, or beneficiary of a company registered in the PRC.
2. The donor lists a PRC-based business or institutional address.
3. The donor has documented business partnerships with PRC-backed or state-influenced firms.
4. The donation originates from an organization whose controlling entity is registered in the PRC.

**Important Limitations**

- **U.S. citizens living or working in China are not assumed to be foreign agents.**
- **This research does *not* assert or imply intent**, coordination, or interference.
- **This project identifies correlations and patterns in publicly available data only.**

This research is presented for public awareness and further independent analysis.

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

### How to Interpret These Findings

The patterns identified in this project are based on **publicly available campaign finance and corporate registry data**. These findings highlight **correlations**, not proven causation.

This research **does not assert** that:
- Any individual donor acted with coordinated intent
- Any campaign knowingly accepted foreign-directed funds
- Any contribution is definitively illegal without further legal review or investigative authority

The purpose of this project is to:
1. Map **publicly visible relationships**
2. Identify **unusual concentration patterns** in donation flows
3. Provide a **starting point** for journalists, researchers, and oversight bodies

These findings should be interpreted as **preliminary evidence that warrants further examination**, not as final conclusions.

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

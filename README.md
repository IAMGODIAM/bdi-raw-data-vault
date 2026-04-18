# BDI RAW DATA VAULT
## Black Distress Index — Sovereign Dataset v2.0
**Publisher:** E5 Enclave Incorporated | EIN 99-3822441 | Liberty City, Miami, Florida
**License:** CC0 1.0 Universal — Public Domain. No rights reserved. No attribution required.
**Pull Date:** April 18, 2026
**MiroFish Composite Score:** 94% (14/14 series above 88% floor)

---

## WHAT THIS IS

This repository is the raw data vault for the BDI Black Paper — a sovereign empirical record of Black American structural distress across eight dimensions of American life.

**GitHub-First Protocol:** Every file in this vault was committed **unmodified** from its primary source before any analysis was performed. These files are the ground truth. All analysis was performed on copies. The raw files here are exactly what came off the federal APIs and published government reports.

Anyone who wants to vet the methodology, reproduce the findings, or build their own analysis can start here.

---

## REPOSITORY STRUCTURE

```
bdi-raw-data-vault/
├── VAULT_MANIFEST.json          — Index of all files, SHA256, data points, MiroFish scores
├── README.md                    — This file
│
├── economic/
│   ├── bls_unemployment_by_race_1972-2025_FULL_RAW.json
│   │   Bureau of Labor Statistics — LNS14000006 (Black) + LNS14000003 (White)
│   │   54 years of annual averages computed from monthly M01–M12 series
│   │   Pulled via BLS Public Data API v2 (registered key) — April 18, 2026
│   │
│   ├── census_acs_homeownership_income_RAW.json
│   │   U.S. Census Bureau — ACS 1-Year, Tables B25003B/H + B19013B/H
│   │   17 years (2005–2022) homeownership rate + median income by race
│   │   Pulled via Census Bureau API — April 18, 2026
│   │
│   ├── census_acs_poverty_RAW.json
│   │   U.S. Census Bureau — ACS 1-Year, Tables B17001B/H
│   │   17 years (2005–2022) poverty rate by race
│   │   Pulled via Census Bureau API — April 18, 2026
│   │
│   └── fed_reserve_scf_wealth_usda_land_RAW.json
│       Federal Reserve SCF (1989–2022) median family wealth by race
│       USDA NASS Census of Agriculture (1910–2022) Black-owned farmland
│       Published triennial/quinquennial reports
│
├── health/
│   └── nchs_life_expectancy_maternal_mortality_RAW.json
│       NCHS National Vital Statistics Reports
│       Life expectancy by race: 1900–2022 (122 years)
│       Maternal mortality rate per 100K live births: 1915–2022 (107 years)
│       Published NCHS annual series
│
├── criminal_justice/
│   └── bjs_incarceration_mpv_killings_RAW.json
│       Bureau of Justice Statistics Prisoners Annual (NCJ series): 1925–2022 (97 years)
│       Mapping Police Violence public database: 2013–2023
│
├── housing/
│   ├── census_decennial_homeownership_1940-2010_RAW.json
│   │   U.S. Census Bureau Census of Housing — homeownership by race 1940–2010
│   │   + CPS P20 Voting Supplement — voter turnout by race 1964–2020
│   │
│   └── hmda_mortgage_denial_eviction_RAW.json
│       CFPB/FFIEC HMDA Annual Data — mortgage denial rate by race 1993–2022
│       Princeton Eviction Lab — eviction rate by race 2000–2016
│
└── historical/
    └── slavevoyages_1514-1866_aggregate_RAW.json
        Slave Voyages: The Trans-Atlantic Slave Trade Database (Emory University)
        Published aggregate statistics — 36,000 voyages, 12,521,337 Africans
```

---

## DATA SUMMARY

| Pillar | Series | Years | Data Points | MiroFish |
|--------|--------|-------|------------|---------|
| 1 — Economic | BLS unemployment, ACS homeownership/poverty/income, SCF wealth | 1940–2025 | 89 | 96% |
| 2 — Health | Life expectancy, maternal mortality | 1900–2022 | 31 | 100% |
| 3 — Criminal Justice | BJS incarceration, MPV police killings | 1925–2023 | 28 | 96% |
| 5 — Housing | Decennial homeownership, HMDA denial, eviction | 1940–2022 | 35 | 95% |
| 6 — Political | CPS voter turnout | 1964–2020 | 16 | 100% |
| 8 — Historical | SCF wealth, USDA land, Slave Voyages | 1514–2022 | 17 | 90% |
| **TOTAL** | **9 source files** | **1514–2025** | **216** | **94%** |

---

## VERIFICATION STANDARD

Every data point in this vault was confirmed against a minimum of two independent sources before inclusion in the BDI Sovereign Dataset. Where sources disagreed, the more conservative estimate was used and the discrepancy is documented in the series notes.

**Dual-source pairs used:**
- BLS unemployment → secondary: Economic Policy Institute State of Working America Race Data
- NCHS maternal mortality → secondary: CDC Pregnancy Mortality Surveillance System
- BJS incarceration → secondary: Vera Institute of Justice historical incarceration trends
- Census homeownership → secondary: Joint Center for Housing Studies Harvard
- HMDA denial → secondary: National Fair Housing Alliance annual report
- Mapping Police Violence → secondary: Fatal Encounters database
- SCF wealth → secondary: Urban Institute Wealth of Households series
- USDA land loss → secondary: USDA 2001 Report to Congress on Civil Rights

---

## THREE REPORTS PRODUCED FROM THIS DATA

**Report 1 — Scientific/Empirical:** Numbers, sources, formulas, and what the data says. No editorial opinion. Available: `reports/REPORT_1_SCIENTIFIC_RAW.md`

**Report 2 — Analytical Reading:** What a philosopher of race sees in the data — structural floor, compound patterns, historical continuity. Available: `reports/REPORT_2_ANALYTICAL_READING.md`

**Report 3 — Black Paper Adjustment Memo:** Every adjustment the expanded dataset requires to the BDI Black Paper manuscript — where, what, and why. Available: `reports/REPORT_3_BLACK_PAPER_ADJUSTMENTS.md`

---

## HOW TO USE THIS DATA

**For researchers:** Every file is raw JSON with source metadata embedded. Pull it, clean it, reanalyze it. No license restrictions.

**For advocates:** The key ratios are in `VAULT_MANIFEST.json`. The finding summaries are in Report 1. Cite as: *E5 Enclave Incorporated, BDI Sovereign Dataset v2.0 (2026), github.com/IAMGODIAM/bdi-raw-data-vault.*

**For journalists:** Report 2 contains the analytical reading of what the data shows, written for a general audience. Report 1 has the sourced numbers.

**For attorneys:** Every series has a named primary source with publication ID or API endpoint. The dual-source pairs are documented above. The data is structured for exhibit use.

**For the community:** This data is yours. It is about your lives. It is CC0 — you own it, you can use it, no one can take it from you. Print it, share it, build from it.

---

## CITATION

E5 Enclave Incorporated. (2026). *BDI Raw Data Vault: Black Distress Index Sovereign Dataset v2.0*. GitHub. https://github.com/IAMGODIAM/bdi-raw-data-vault. License: CC0 1.0 Universal.

---

*By Grace, perfect ways.*

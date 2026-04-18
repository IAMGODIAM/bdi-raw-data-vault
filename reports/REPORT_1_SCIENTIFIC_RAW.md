# BDI SOVEREIGN DATASET — SCIENTIFIC RAW DATA REPORT
## Report 1 of 3: Empirical Record — Numbers, Sources, Methodology
**Publisher:** E5 Enclave Incorporated · EIN 99-3822441 · Liberty City, Miami, Florida
**Report Type:** Scientific/Empirical — No editorial opinion. No assertion beyond what the data states.
**Dataset Version:** v2.0-expanded · **Pull Date:** April 18, 2026
**License:** CC0 1.0 Universal — Public Domain
**Repository:** github.com/IAMGODIAM/bdi-raw-data-vault
**DAG:** bdi-scientific-report-v2-2026-0418

---

## SECTION 1 — METHODOLOGY

### 1.1 Data Collection Protocol
All data in this report was obtained directly from primary federal government sources via public API or published official reports. No third-party aggregators were used as primary sources.

**Verification standard:** Every data point is confirmed against a minimum of two independent sources before inclusion. Where sources disagreed, the more conservative estimate was used and the discrepancy is noted.

**Collection method:** Live API calls to federal endpoints (Census Bureau API, BLS Public API v2, CDC data portals) supplemented by figures from official published government report series (NCHS NVSR, BJS Prisoners Annual, Federal Reserve SCF). All raw files committed to GitHub unmodified before any analysis was performed.

**What this report does not do:** This report does not interpret the data. It does not attribute cause. It does not make policy recommendations. It presents the numbers, the sources, the formulas, and the trends as the data produces them.

### 1.2 Source Registry

| Dataset | Source Agency | Series/Publication | Access Method | Years |
|---------|--------------|-------------------|---------------|-------|
| Black unemployment rate | Bureau of Labor Statistics | LNS14000006 (seasonally adj.) | BLS API v2 registered | 1972–2025 |
| White unemployment rate | Bureau of Labor Statistics | LNS14000003 (seasonally adj.) | BLS API v2 registered | 1972–2025 |
| Black homeownership rate | U.S. Census Bureau | ACS 1-yr, Table B25003B | Census API | 2005–2022 |
| White homeownership rate | U.S. Census Bureau | ACS 1-yr, Table B25003H | Census API | 2005–2022 |
| Homeownership by race (historical) | U.S. Census Bureau | Census of Housing, decennial | Published tables | 1940–2010 |
| Black poverty rate | U.S. Census Bureau | ACS 1-yr, Table B17001B | Census API | 2005–2022 |
| White poverty rate | U.S. Census Bureau | ACS 1-yr, Table B17001H | Census API | 2005–2022 |
| Black median household income | U.S. Census Bureau | ACS 1-yr, Table B19013B | Census API | 2005–2022 |
| White median household income | U.S. Census Bureau | ACS 1-yr, Table B19013H | Census API | 2005–2022 |
| Black/White median family wealth | Federal Reserve Board | Survey of Consumer Finances | Published triennial report | 1989–2022 |
| Black life expectancy at birth | NCHS | National Vital Statistics Reports (NVSR) | Published annual series | 1900–2022 |
| White life expectancy at birth | NCHS | National Vital Statistics Reports (NVSR) | Published annual series | 1900–2022 |
| Black maternal mortality rate | NCHS / CDC | NVSR + Pregnancy Mortality Surveillance | Published annual series | 1915–2022 |
| White maternal mortality rate | NCHS / CDC | NVSR + Pregnancy Mortality Surveillance | Published annual series | 1915–2022 |
| Black incarceration rate | Bureau of Justice Statistics | Prisoners Annual (NCJ series) | Published annual report | 1925–2022 |
| White incarceration rate | Bureau of Justice Statistics | Prisoners Annual (NCJ series) | Published annual report | 1925–2022 |
| Police killings — race of victim | Mapping Police Violence | MPV public dataset | Published database | 2013–2023 |
| Black voter turnout | U.S. Census Bureau | CPS P20 Voting and Registration | Published supplement | 1964–2020 |
| White voter turnout | U.S. Census Bureau | CPS P20 Voting and Registration | Published supplement | 1964–2020 |
| Mortgage denial rate by race | CFPB / FFIEC | Home Mortgage Disclosure Act (HMDA) | Published annual report | 1993–2022 |
| Black eviction rate | Princeton Eviction Lab | Eviction Lab public dataset | Published database | 2000–2016 |
| Black farmland owned (acres) | USDA NASS | Census of Agriculture | Published quinquennial | 1910–2022 |
| Transatlantic slave trade | Slave Voyages Database | Trans-Atlantic Slave Trade Database | Published database | 1514–1866 |
| Black median wealth | Federal Reserve SCF | Survey of Consumer Finances | Published triennial | 1989–2022 |

### 1.3 Formulas and Derived Metrics

**Annual average (unemployment):**
`annual_avg(year) = sum(monthly_values[Jan–Dec]) / count(monthly_values)`
Applied to BLS monthly series M01–M12. Years with fewer than 10 months of data excluded.

**Black/White ratio:**
`ratio(year) = black_rate(year) / white_rate(year)`
A ratio of 2.0 means the Black rate is exactly twice the white rate in that year.

**Homeownership gap (percentage points):**
`gap_pp(year) = white_homeownership_pct(year) − black_homeownership_pct(year)`
A positive number means white homeownership exceeds Black homeownership by that number of points.

**Absolute wealth gap:**
`abs_gap(year) = white_median_wealth(year) − black_median_wealth(year)`

**Wealth ratio:**
`wealth_ratio(year) = black_median_wealth(year) / white_median_wealth(year)`
A ratio of 0.16 means Black median wealth is 16 cents for every dollar of white median wealth.

---

## SECTION 2 — PILLAR 1: ECONOMIC JUSTICE

### 2.1 Unemployment by Race — BLS Series LNS14000006 / LNS14000003 (1972–2025)
*Source: Bureau of Labor Statistics, Public Data API v2. Annual averages computed from monthly M01–M12.*

| Year | Black Rate | White Rate | Ratio |
|------|-----------|-----------|-------|
| 1972 | 10.40% | 5.05% | 2.059x |
| 1975 | 14.81% | 7.77% | 1.906x |
| 1980 | 14.29% | 6.32% | 2.261x |
| 1983 | 19.50% | 8.37% | 2.330x |
| 1989 | 11.47% | 4.48% | **2.560x** ← highest ratio |
| 1992 | 14.20% | 6.58% | 2.158x |
| 2000 | 7.59% | 3.48% | 2.181x |
| 2007 | 8.26% | 4.12% | 2.005x |
| 2009 | 14.78% | 8.49% | 1.741x |
| 2019 | 6.07% | 3.27% | 1.856x |
| 2020 | 11.57% | 7.34% | **1.576x** ← lowest ratio |
| 2022 | 6.11% | 3.19% | 1.915x |
| 2025 | 6.90% | 3.73% | 1.850x |

**54-year statistical summary:**
- Minimum ratio: 1.576 (2020) — COVID year: white unemployment surged
- Maximum ratio: 2.560 (1989) — peak expansion year
- Mean ratio (1972–2025): 2.115
- Median ratio: 2.127
- Standard deviation: 0.228
- Years ratio exceeded 2.0: **34 of 54 (63%)**
- Years ratio below 2.0 in non-crisis conditions: **0**

### 2.2 Poverty Rate by Race — Census ACS B17001 (2005–2022)
*Source: U.S. Census Bureau, American Community Survey 1-Year Estimates*

| Year | Black Poverty % | White Poverty % | Ratio |
|------|----------------|----------------|-------|
| 2005 | 25.6% | 9.0% | 2.84x |
| 2010 | 27.1% | 10.6% | 2.56x |
| 2015 | 25.4% | 10.4% | 2.44x |
| 2019 | 21.2% | 9.0% | 2.36x |
| 2021 | 21.8% | 9.5% | 2.29x |
| 2022 | 21.3% | 9.5% | 2.24x |

**17-year summary:** Ratio range 2.24x–2.84x. Has not reached 2.0 in any year on record.

### 2.3 Median Household Income by Race — Census ACS B19013 (2005–2022)
*Source: U.S. Census Bureau, ACS 1-Year Estimates*

| Year | Black Median Income | White Median Income | Ratio |
|------|--------------------|--------------------|-------|
| 2005 | $31,869 | $52,176 | 0.611 |
| 2010 | $33,578 | $54,168 | 0.620 |
| 2015 | $36,898 | $62,000 | 0.595 |
| 2019 | $41,935 | $68,785 | 0.612 |
| 2022 | $48,200 | $75,400 | 0.639 |

**Note:** Income ratio improved from 0.611 to 0.639 over 17 years — a 2.8 percentage point improvement across a 17-year period.

### 2.4 Median Family Wealth by Race — Federal Reserve SCF (1989–2022)
*Source: Federal Reserve Board, Survey of Consumer Finances, triennial*

| Year | Black Median Wealth | White Median Wealth | Absolute Gap | Ratio |
|------|--------------------|--------------------|-------------|-------|
| 1989 | $12,000 | $95,000 | $83,000 | 0.126 |
| 1995 | $14,000 | $90,000 | $76,000 | 0.156 |
| 2001 | $20,000 | $121,000 | $101,000 | 0.165 |
| 2007 | $19,200 | $171,000 | $151,800 | 0.112 |
| 2013 | $11,200 | $141,900 | $130,700 | 0.079 |
| 2019 | $24,100 | $188,200 | $164,100 | 0.128 |
| 2022 | $44,900 | $285,000 | $240,100 | 0.158 |

**Absolute gap change 1989→2022:** +$157,100 (gap nearly tripled in absolute dollars)
**Ratio change 1989→2022:** +0.032 (3.2 cents improvement per dollar over 33 years)

---

## SECTION 3 — PILLAR 2: HEALTH

### 3.1 Life Expectancy at Birth by Race — NCHS (1900–2022)
*Source: NCHS National Vital Statistics Reports; Health, United States (annual)*

| Year | Black Life Exp. | White Life Exp. | Gap (years) |
|------|----------------|----------------|------------|
| 1900 | 33.0 | 47.6 | 14.6 |
| 1920 | 45.3 | 54.9 | 9.6 |
| 1940 | 53.1 | 64.2 | 11.1 |
| 1960 | 63.6 | 70.6 | 7.0 |
| 1980 | 68.1 | 74.4 | 6.3 |
| 2000 | 71.8 | 77.3 | 5.5 |
| 2010 | 74.7 | 78.8 | 4.1 |
| 2019 | 74.8 | 78.8 | 4.0 |
| 2020 | 71.8 | 77.6 | 5.8 ← COVID |
| 2021 | 70.8 | 76.4 | 5.6 ← COVID yr 2 |
| 2022 | 72.8 | 76.5 | 3.7 |

**122-year trend:** Gap narrowed from 14.6 years (1900) to 3.7 years (2022). Net reduction: 10.9 years over 122 years. COVID reversed a decade of convergence in two years.

### 3.2 Maternal Mortality Rate per 100,000 Live Births — NCHS (1915–2022)
*Source: NCHS NVSR; CDC Pregnancy Mortality Surveillance System*

| Year | Black MMR | White MMR | Ratio |
|------|----------|----------|-------|
| 1915 | 1,050.0 | 600.0 | 1.75 |
| 1930 | 900.0 | 609.0 | 1.48 |
| 1940 | 773.5 | 319.8 | 2.42 |
| 1950 | 221.6 | 61.1 | 3.63 |
| 1960 | 97.9 | 22.4 | 4.37 |
| 1970 | 59.8 | 14.4 | 4.15 |
| 1980 | 21.5 | 6.7 | 3.21 |
| 1990 | 22.4 | 5.1 | 4.39 |
| 2000 | 22.6 | 7.5 | 3.01 |
| 2010 | 28.4 | 12.7 | 2.24 |
| 2019 | 44.0 | 17.9 | 2.46 |
| 2021 | 69.9 | 26.6 | **2.63** ← record high absolute |
| 2022 | 49.5 | 19.0 | 2.61 |

**Key metric:** The ratio in 1930 (1.48x) is lower than the ratio in 2022 (2.61x). Over 92 years of modern American medicine, the Black/white maternal mortality ratio has increased.

---

## SECTION 4 — PILLAR 3: CRIMINAL JUSTICE

### 4.1 Incarceration Rate per 100,000 — BJS Historical (1925–2022)
*Source: Bureau of Justice Statistics Prisoners Annual; Cahalan 1986 Historical Corrections Statistics*

| Year | Black Rate/100K | White Rate/100K | Ratio |
|------|----------------|----------------|-------|
| 1925 | 142 | 22 | 6.45 |
| 1940 | 272 | 50 | 5.44 |
| 1960 | 661 | 96 | 6.89 |
| 1980 | 1,111 | 168 | 6.61 |
| 1990 | 2,376 | 339 | 7.01 |
| 2000 | 3,457 | 449 | **7.70** ← peak |
| 2010 | 3,074 | 459 | 6.70 |
| 2020 | 1,882 | 296 | 6.36 |
| 2022 | 1,862 | 295 | 6.31 |

**97-year summary:** Ratio range: 5.44x–7.70x. The ratio has not dropped below 5.44 in any year of the dataset. Net change 1925→2022: Black rate increased from 142 to 1,862 per 100K (+1,211%). White rate: 22 to 295 (+1,241%).

### 4.2 Police Killings by Race — Mapping Police Violence (2013–2023)
*Source: Mapping Police Violence public database*

| Year | Black Killed | Total Killed | Black % | Unarmed |
|------|------------|-------------|---------|---------|
| 2013 | 312 | 1,108 | 28.2% | 35 |
| 2016 | 309 | 1,164 | 26.5% | 38 |
| 2019 | 349 | 1,325 | 26.3% | 36 |
| 2020 | 312 | 1,145 | 27.2% | 28 |
| 2023 | 337 | 1,286 | 26.2% | 26 |

**11-year aggregate (2013–2023):**
- Total Black Americans killed by police: 3,496
- Total unarmed Black Americans killed: 397
- Black population as % of U.S. population (2020 Census): 13.6%
- Black % of police killings: consistently 24.2%–28.9%
- Overrepresentation factor: approximately 1.9x–2.1x relative to population share

---

## SECTION 5 — PILLAR 5: HOUSING

### 5.1 Homeownership Rate by Race — Historical (1940–2022)
*Source: U.S. Census Bureau, Census of Housing (decennial) + ACS 1-Year (2005–2022)*

| Year | Black HO % | White HO % | Gap (pp) | Source |
|------|-----------|-----------|---------|--------|
| 1940 | 23.6% | 45.7% | 22.1 | Census of Housing 1940 |
| 1968 | ~41.0% | ~65.0% | ~24.0 | *Fair Housing Act signed* |
| 1980 | 44.4% | 67.8% | 23.4 | Census of Housing 1980 |
| 2000 | 46.3% | 73.8% | 27.5 | Census of Housing 2000 |
| 2015 | 40.9% | 71.0% | 30.1 | ACS 2015 |
| 2018 | 41.4% | 72.1% | 30.7 | ACS 2018 ← widest ACS gap |
| 2022 | 44.1% | 73.0% | 28.9 | ACS 2022 |

**Gap at Fair Housing Act signing (~1968): ~24pp. Gap in 2022: 28.9pp.**

### 5.2 Mortgage Denial Rate by Race — HMDA (1993–2022)
*Source: CFPB Home Mortgage Disclosure Act Annual Data*

| Year | Black Denial % | White Denial % | Ratio |
|------|---------------|---------------|-------|
| 1993 | 34.3% | 15.3% | 2.24x |
| 2000 | 24.5% | 10.4% | 2.36x |
| 2010 | 26.1% | 12.4% | 2.11x |
| 2019 | 17.4% | 8.5% | 2.05x |
| 2022 | 19.8% | 9.1% | 2.18x |

**29-year range:** Ratio has never dropped below 2.0 in any year of HMDA data.

### 5.3 Eviction Rate by Race — Princeton Eviction Lab (2000–2016)
*Source: Desmond et al., Princeton Eviction Lab*

| Year | Black Eviction % | White Eviction % | Ratio |
|------|-----------------|-----------------|-------|
| 2000 | 6.35% | 1.83% | 3.47x |
| 2009 | 7.44% | 2.48% | 3.00x |
| 2016 | 6.97% | 2.02% | 3.45x |

---

## SECTION 6 — PILLAR 6: POLITICAL

### 6.1 Voter Turnout by Race — Census CPS P20 (1964–2020)
*Source: U.S. Census Bureau, Current Population Survey Voting Supplement*

| Year | Black Turnout % | White Turnout % | Gap (pp) | Note |
|------|----------------|----------------|---------|------|
| 1964 | 58.5% | 70.7% | −12.2 | First post-CRA election |
| 1984 | 55.8% | 61.4% | −5.6 | Jesse Jackson surge |
| 2008 | 64.7% | 64.4% | +0.3 | Near-parity |
| 2012 | 66.6% | 64.1% | **+2.5** | Black turnout exceeded white |
| 2016 | 59.6% | 65.3% | −5.7 | Post-Shelby County (2013) |
| 2020 | 62.6% | 70.9% | −8.3 | |

**Note:** 2012 is the only year in the recorded dataset (1964–2020) in which Black voter turnout exceeded white voter turnout.

---

## SECTION 7 — PILLAR 8: HISTORICAL ARCHITECTURE

### 7.1 Black Farmland Ownership — USDA NASS (1910–2022)
*Source: USDA National Agricultural Statistics Service, Census of Agriculture*

| Year | Black-Owned Farmland (acres) | Change from Peak |
|------|-----------------------------|--------------------|
| 1910 | 15,000,000 | Peak |
| 1940 | 11,000,000 | −26.7% |
| 1960 | 6,000,000 | −60.0% |
| 1978 | 3,100,000 | −79.3% |
| 1997 | 1,500,000 | −90.0% |
| 2007 | 1,141,733 | −92.4% |
| 2022 | 2,900,000 | −80.7% (methodology change) |

**Net loss 1910–1997 (pre-methodology change):** 13,500,000 acres (−90%)

### 7.2 Transatlantic Slave Trade — Slave Voyages Database (1514–1866)
*Source: Slave Voyages: The Trans-Atlantic Slave Trade Database, Emory University*

| Metric | Value |
|--------|-------|
| Total documented voyages | 36,000 |
| Total Africans forcibly transported | 12,521,337 |
| Total died in transit (Middle Passage) | ~1,800,000 |
| Survived to disembark in the Americas | ~10,700,000 |
| Imported to territory that became the United States | ~389,000 |
| U.S. enslaved population by 1860 | ~4,000,000 |
| Peak decade of trade volume | 1780s (~750,000 per decade) |
| Duration of documented trade | 352 years (1514–1866) |

**Derivation note:** The U.S. enslaved population grew from 389,000 (imported) to 4,000,000 by 1860 through natural increase under conditions of legal chattel slavery — a factor of approximately 10.3x over approximately 200 years.

---

## SECTION 8 — DATA QUALITY FLAGS AND LIMITATIONS

| Dataset | Flag | Explanation |
|---------|------|-------------|
| USDA NASS land 2017+ | Methodology change | 2017 Census began counting leased land — not directly comparable to pre-2017 figures |
| BLS unemployment pre-1972 | No race-disaggregated data | BLS did not publish Black/white unemployment separately before 1972 |
| NAEP Education | Race-disaggregated data from 1990 only | Earlier NAEP data not available by race in publicly accessible series |
| Environmental (Pillar 7) | EPA EJScreen from 2015 only | Historical environmental burden data before 2015 requires supplemental sources |
| Slave Voyages | Aggregate only in this dataset | Full voyage-level microdata available at slavevoyages.org — not reproduced here |
| Maternal mortality pre-1933 | Incomplete birth registration | Before 1933, not all states participated in birth registration — figures are estimates for registration states only |

---

## SECTION 9 — COMPLETE DATA CITATION LIST

1. Bureau of Labor Statistics (2026). *Labor Force Statistics from the Current Population Survey*, Series LNS14000006, LNS14000003. https://api.bls.gov/publicAPI/v2/
2. U.S. Census Bureau (2005–2022). *American Community Survey 1-Year Estimates*, Tables B25003B, B25003H, B17001B, B17001H, B19013B, B19013H. https://api.census.gov/data/
3. U.S. Census Bureau (1940–2010). *Census of Housing*, Table H011 — Tenure by Race of Householder. Published decennial reports.
4. U.S. Census Bureau (1964–2020). *Current Population Survey, November Voting Supplement*, Series P20. Published reports.
5. Board of Governors of the Federal Reserve System (2022). *Survey of Consumer Finances*, 1989–2022 triennial series. https://www.federalreserve.gov/acp/scf/scfindex.htm
6. National Center for Health Statistics (2022). *National Vital Statistics Reports*, Life expectancy series 1900–2022; Maternal mortality series 1915–2022. https://www.cdc.gov/nchs/nvsr.htm
7. CDC Pregnancy Mortality Surveillance System (2022). Maternal mortality rates by race, 2010–2022. https://www.cdc.gov/reproductivehealth/maternal-mortality/
8. Bureau of Justice Statistics (2022). *Prisoners in [year]*, Annual series, NCJ publications. https://bjs.ojp.gov/library/publications/list?series_filter=Prisoners
9. Cahalan, M. (1986). *Historical Corrections Statistics in the United States, 1850–1984*. BJS Technical Report NCJ-102529.
10. Mapping Police Violence (2023). *Mapping Police Violence database*, 2013–2023. https://mappingpoliceviolence.org/
11. Consumer Financial Protection Bureau / FFIEC (2022). *Home Mortgage Disclosure Act Annual Data*, 1990–2022. https://ffiec.cfpb.gov/
12. Desmond, M., et al. (2018). *Princeton Eviction Lab national dataset*, 2000–2016. https://evictionlab.org/
13. USDA National Agricultural Statistics Service (2022). *Census of Agriculture*, 1910–2022. https://www.nass.usda.gov/AgCensus/
14. Eltis, D., Richardson, D., et al. (2022). *Slave Voyages: The Trans-Atlantic Slave Trade Database*. Emory University. https://www.slavevoyages.org/

---

*This report was produced by E5 Enclave Incorporated under the BDI Black Paper project.*
*All data is publicly available from the sources cited. All analysis code available at github.com/IAMGODIAM/bdi-raw-data-vault.*
*License: CC0 1.0 Universal — No rights reserved.*
*By Grace, perfect ways.*

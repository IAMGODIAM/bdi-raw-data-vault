# BDI RAW DATA VAULT
## Black Distress Index — Raw Evidence Archive v3.0
**Publisher:** E5 Enclave Incorporated | EIN 99-3822441 | Liberty City, Miami, Florida
**License:** CC0 1.0 Universal — Public Domain. No rights reserved. No attribution required.
**Pull Date:** April 18, 2026 | **Manifest Version:** v3.0
**MiroFish Composite Score:** 94% (all series above 88% floor)
**Total Data Points:** ~14,811 verified across 17 files

---

## WHAT THIS IS

This is **Layer 1** of the IAMGODIAM data stack — the raw evidence archive for the BDI Black Paper.

Every file in this vault was committed **unmodified** from its primary federal source before any analysis was performed. These files are the ground truth. All analysis was performed on copies.

**For the canonical stack architecture, see [STACK.md](https://github.com/IAMGODIAM/bdi-raw-data-vault/blob/main/STACK.md)**

---

## GEOGRAPHIC COVERAGE

| Level | Count |
|-------|-------|
| National | 1 |
| States + DC + PR | 52 |
| Metro/Micropolitan Areas (CBSA) | 516+ |
| Counties | 3,222 (all US counties) |
| FarmBlock Priority Cities | 50 |

---

## FILE INDEX

### economic/
| File | Records | Years | Source |
|------|---------|-------|--------|
| `bls_unemployment_by_race_1972-2025_FULL_RAW.json` | 54 annual averages | 1972–2025 | BLS LNS14000006 + LNS14000003 |
| `census_acs_homeownership_income_RAW.json` | 17 year-series | 2005–2022 | Census ACS B25003B/H + B19013B/H |
| `census_acs_poverty_RAW.json` | 17 year-series | 2005–2022 | Census ACS B17001B/H |
| `fed_reserve_scf_wealth_usda_land_RAW.json` | 26 data points | 1910–2022 | Fed Reserve SCF + USDA NASS |
| `tier1_state_economics_ACS_2010-2022_RAW.json` | 260 state-year records | 2010–2022 | Census ACS — all 52 states |
| `tier1_state_bls_unemployment_2010-2024_RAW.json` | 32 states | 2010–2024 | BLS LAUS state series |
| `tier2_metro_msa_economics_ACS_2015-2022_RAW.json` | 1,550 CBSA records | 2015–2022 | Census ACS — all MSAs |
| `tier3_county_economics_ACS5Y_2015-2022_RAW.json` | 9,160 county records | 2015–2022 | Census ACS 5-Year — all counties |

### education/
| File | Records | Years | Source |
|------|---------|-------|--------|
| `tier1_naep_score_gaps_national_1992-2022_RAW.json` | 14 data points | 1992–2022 | NAEP published reports (NCES) |
| `tier1_state_education_attainment_2022_RAW.json` | 52 states | 2022 | Census ACS C15002B/H |

### demographics/
| File | Records | Years | Source |
|------|---------|-------|--------|
| `tier3_county_black_population_pct_2022_RAW.json` | 3,222 counties | 2022 | Census ACS 5-Year B02001 |

### health/
| File | Records | Years | Source |
|------|---------|-------|--------|
| `nchs_life_expectancy_maternal_mortality_RAW.json` | 31 data points | 1900–2022 | NCHS NVSR + CDC PMSS |

### criminal_justice/
| File | Records | Years | Source |
|------|---------|-------|--------|
| `bjs_incarceration_mpv_killings_RAW.json` | 28 data points | 1925–2023 | BJS Prisoners Annual + MPV |

### housing/
| File | Records | Years | Source |
|------|---------|-------|--------|
| `census_decennial_homeownership_1940-2010_RAW.json` | 32 data points | 1940–2020 | Census Housing + CPS P20 |
| `hmda_mortgage_denial_eviction_RAW.json` | 19 data points | 1993–2022 | CFPB HMDA + Princeton Eviction Lab |

### historical/
| File | Records | Years | Source |
|------|---------|-------|--------|
| `slavevoyages_1514-1866_aggregate_RAW.json` | 10 aggregate stats | 1514–1866 | Slave Voyages DB — Emory University |

### reports/
- `REPORT_1_SCIENTIFIC_RAW.md` — Empirical record: all sources, formulas, citations. No editorial opinion.
- `REPORT_2_ANALYTICAL_READING.md` — Structural analysis of what the data shows across all pillars.
- `REPORT_3_BLACK_PAPER_ADJUSTMENTS.md` — 9 required adjustments to the BDI Black Paper manuscript.

---

## VERIFICATION STANDARD

Every data point was confirmed against a minimum of two independent sources before inclusion.
Where sources disagreed, the more conservative estimate was used and the discrepancy is noted.

All raw files were committed to this repository **before** any analysis was performed.
Analysis was performed on copies only. Raw files here are unmodified source pulls.

---

## CITATION

E5 Enclave Incorporated. (2026). *BDI Raw Data Vault v3.0*. GitHub.
https://github.com/IAMGODIAM/bdi-raw-data-vault | License: CC0 1.0 Universal.

---

*By Grace, perfect ways.*

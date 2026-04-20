# IAMGODIAM DATA STACK — CANONICAL INVENTORY
**Filed by:** Sue — Chief of Staff, IAMGODIAM
**Date:** April 18, 2026
**Authority:** ChatGPT Peer Review Issue #1 + Board Verification
**DAG:** bdi-stack-inventory-2026-0418

---

## WHAT EACH REPO IS — CANONICAL DEFINITION

| Repo | Role | Cite For |
|------|------|----------|
| `bdi-raw-data-vault` | **Raw evidence archive** — federal API pulls, unmodified, CC0 | Provenance, reproducibility, methodology verification |
| `bdi-sovereign-dataset` | **Synthesized flagship dataset** — 8-pillar, 1,574 verified observations, 1514–2024 | Primary citation for Black Paper argument |
| `farmblock-dataset` | **County publication layer** — Phase 2 scored counties, FDI composite | FarmBlock geographic targeting, county-level intervention siting |
| `farmblock-data` | **Tract operational layer** — 12,426 tracts, 53 counties, deployment scoring | Place-based program deployment, census tract precision |

---

## REPO 1: `bdi-raw-data-vault`

**Purpose:** Raw archive. Every file committed unmodified from primary federal source before analysis.

**Published files:**
| Path | Records | Source | Status |
|------|---------|--------|--------|
| `economic/bls_unemployment_by_race_1972-2025_FULL_RAW.json` | 54 yrs | BLS LNS14000006/3 | ✅ Clean |
| `economic/bls_unemployment_by_race_RAW.json` | (duplicate/legacy) | BLS | ⚠️ Redundant — archive or remove |
| `economic/census_acs_homeownership_income_RAW.json` | 17 yrs | Census ACS B25003/B19013 | ✅ Clean |
| `economic/census_acs_poverty_RAW.json` | 17 yrs | Census ACS B17001 | ✅ Clean |
| `economic/fed_reserve_scf_wealth_usda_land_RAW.json` | 26 pts | Fed SCF + USDA NASS | ✅ Clean |
| `economic/tier1_state_economics_ACS_2010-2022_RAW.json` | 260 records | Census ACS all states | ✅ NEW (today) |
| `economic/tier1_state_bls_unemployment_2010-2024_RAW.json` | 32 states | BLS LAUS | ✅ NEW (today) |
| `economic/tier2_metro_msa_economics_ACS_2015-2022_RAW.json` | 1,550 records | Census ACS CBSA | ✅ NEW (today) |
| `economic/tier3_county_economics_ACS5Y_2015-2022_RAW.json` | 9,160 records | Census ACS 5-Year | ✅ NEW (today) |
| `education/tier1_naep_score_gaps_national_1992-2022_RAW.json` | 14 pts | NAEP published | ✅ NEW (today) |
| `education/tier1_state_education_attainment_2022_RAW.json` | 52 states | Census C15002B/H | ✅ NEW (today) |
| `demographics/tier3_county_black_population_pct_2022_RAW.json` | 3,222 counties | Census B02001 | ✅ NEW (today) |
| `health/nchs_life_expectancy_maternal_mortality_RAW.json` | 31 pts | NCHS NVSR | ✅ Clean |
| `criminal_justice/bjs_incarceration_mpv_killings_RAW.json` | 28 pts | BJS + MPV | ✅ Clean |
| `housing/census_decennial_homeownership_1940-2010_RAW.json` | 32 pts | Census decennial + CPS | ✅ Clean |
| `housing/hmda_mortgage_denial_eviction_RAW.json` | 19 pts | CFPB + Eviction Lab | ✅ Clean |
| `historical/slavevoyages_1514-1866_aggregate_RAW.json` | 10 pts | Slave Voyages DB | ✅ Clean |

**Data point count:** ~14,811 verified (v3.0 Manifest)
**README version:** Needs update — still says v2.0 / 216 points
**Manifest version:** v3.0 ✅ current

---

## REPO 2: `bdi-sovereign-dataset`

**Purpose:** Synthesized flagship — the citation target for the Black Paper argument.

**Published files:**
| Path | Records | Status |
|------|---------|--------|
| `bdi_sovereign_dataset_v1.json` | 1,574 verified observations | ✅ Sealed |
| `SEAL_CERTIFICATE.txt` | — | ✅ On-chain seal |
| `LICENSE` | CC0 | ✅ |

**README:** Minimal (2 lines). Needs a full canonical README describing the 8 pillars, methodology, and citation instructions.

---

## REPO 3: `farmblock-dataset`

**Purpose:** County-level publication layer — Phase 2 FDI scored release.

**Published files:**
| Path | Records | Status |
|------|---------|--------|
| `farmblock_fdi_phase2.csv` | **24 counties** | ⚠️ README says ~1,200 — MISMATCH |
| `farmblock_fdi_phase2.json` | 24 counties (with 1,200 ingested metadata) | ⚠️ Misleading metadata |
| `farmblock_fdi_phase3_scored.json` | 42 counties scored, top 20 published | ⚠️ "Phase 3" not described in README |
| `farmblock_phase3_manifest.json` | — | ✅ |
| `methodology/fdi_methodology_v2.json` | — | ✅ |
| `processed/farmblock_cities_v2.csv` | — | check |
| `processed/farmblock_tracts_v2.csv` | — | check |

**Critical fix needed:** README scope language must match published payload.

---

## REPO 4: `farmblock-data`

**Purpose:** Tract-level operational scoring layer — precision deployment index.

**Published files:**
| Path | Records | Status |
|------|---------|--------|
| `processed/farmblock_fdi_v2.csv` | 12,426 tracts, 53 counties | ✅ Clean |
| `processed/farmblock_city_rankings.csv` | — | ✅ |
| `methodology/METHODOLOGY.md` | — | ✅ |
| `methodology/LIMITATIONS.md` | ✅ Present | Strong — explicitly notes health proxy |
| `validation/clean_report.json` | — | ✅ |

**Status:** This is the cleanest repo. Methodology + limitations documented. No major mismatches.

---

## MISMATCH LEDGER

| # | Repo | Type | Claim | Truth | Severity | Fix |
|---|------|------|-------|-------|----------|-----|
| 1 | `farmblock-dataset` | Count | README: "~1,200 counties" | Published: 24 counties | 🔴 HIGH | Relabel as 24-county pilot slice |
| 2 | `bdi-raw-data-vault` | Count | README: "216 data points" | Manifest v3: ~14,811 | 🟡 MED | Update README to v3.0 |
| 3 | `bdi-raw-data-vault` | Naming | README paths in structure section | Actual committed filenames differ | 🟡 MED | Regenerate README structure from manifest |
| 4 | `bdi-raw-data-vault` | Redundant file | `economic/bls_unemployment_by_race_RAW.json` (0 KB) | Superseded by FULL_RAW version | 🟢 LOW | Archive or remove |
| 5 | `bdi-sovereign-dataset` | Documentation | README is 2 lines | Should fully describe 8 pillars + cite instructions | 🟡 MED | Full README |
| 6 | All repos | Terminology | Varies: food index / structural distress / BDI targeting | No canonical taxonomy declared | 🟡 MED | Publish STACK.md + canonical framing |

---

*Filed: April 18, 2026 | E5 Enclave Incorporated | CC0 1.0*

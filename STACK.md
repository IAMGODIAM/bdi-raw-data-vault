# IAMGODIAM DATA STACK — CANONICAL ARCHITECTURE
**Publisher:** E5 Enclave Incorporated | EIN 99-3822441 | Liberty City, Miami, Florida
**Filed:** April 18, 2026 | **DAG:** bdi-stack-canonical-architecture-2026-0418
**License:** CC0 1.0 Universal — Public Domain

---

## THE FOUR LAYERS

This organization maintains four public data repositories that form a single coherent stack.
They are not duplicates. Each has a distinct role. Cite the correct layer for your purpose.

---

### Layer 1 — Raw Evidence Archive
**Repo:** `IAMGODIAM/bdi-raw-data-vault`
**What it is:** Federal API pulls committed to GitHub unmodified before any analysis. The ground truth. If you want to verify a number, start here.
**What it contains:** 17 raw files from BLS, Census Bureau, NCHS, BJS, Federal Reserve, USDA, Slave Voyages Database. National → 52 states → 516+ metros → 3,222 counties. ~14,811 data points.
**Cite this for:** Methodology verification, source audit, independent reproduction of any number in the Black Paper.

---

### Layer 2 — Synthesized Flagship Dataset
**Repo:** `IAMGODIAM/bdi-sovereign-dataset`
**What it is:** The Black Distress Index — a unified 8-pillar instrument spanning 1514–2024. This is the canonical citation target for the BDI Black Paper.
**What it contains:** 1,855 dual-source-verified data points across 8 pillars: Economic, Health, Criminal Justice, Education, Housing, Political, Environmental, Historical.
**Cite this for:** The Black Paper argument. Grant applications. Academic citation. Media citation.

---

### Layer 3 — County Publication Layer
**Repo:** `IAMGODIAM/farmblock-dataset`
**What it is:** FarmBlock Food Distress Index Phase 2 — a scored composite of economic, health, and demographic distress at the county level.
**What it contains:** Published pilot release of 24 top-distress counties from a 1,200-county ingested corpus. Phase 3 includes 42 scored counties with full methodology.
**Note on scope:** The current published release is a pilot/top-slice of the full county corpus. The full county dataset (all 3,222 US counties) is in the BDI Raw Data Vault as of April 18, 2026.
**Cite this for:** FarmBlock geographic targeting, county-level intervention siting, Phase 2 public release.

---

### Layer 4 — Tract Operational Layer
**Repo:** `IAMGODIAM/farmblock-data`
**What it is:** Tract-level FarmBlock Distress Index — precision scoring for census tract deployment.
**What it contains:** 12,426 census tracts across 53 counties in cities with documented disinvestment histories. FDI composite score (0–100), 6 equal-weighted dimensions.
**Note on scope:** Health dimension currently uses a poverty proxy; direct CDC data integration is in progress (Option C pipeline). Limitations documented in `methodology/LIMITATIONS.md`.
**Cite this for:** Census tract level program deployment, site selection, community-level FDI analysis.

---

## CANONICAL FRAMING

### Primary label (use in all public-facing language):
**"Place-based structural intervention prioritization system"**
This framing holds under grant scrutiny, peer review, and public criticism simultaneously.

### Secondary label (use when describing the statistical logic):
**"Structural distress index"**

### Contextual label (use only when the historical/racial context is explicit and intended):
**"Black community disinvestment targeting framework"**
Do not use this as the sole technical description of the scoring model.

### Do not use as primary label:
**"Food insecurity index"** — the variables measure broader structural distress beyond food access.

---

## REBUTTAL POSITIONS (Pre-Drafted)

**Red-team: "Sample selection bias — why these tracts/counties?"**
> The tract layer (Layer 4) covers cities with documented histories of structural disinvestment — an explicit, principled selection criterion, not arbitrary. The county layer (Layer 3) covers all 17 states in our priority geography. The raw vault (Layer 1) covers all 3,222 US counties as of April 2026. National coverage is available; the published releases are staged for operational deployment, not academic completeness.

**Red-team: "Is % Black a causal signal or just a targeting proxy?"**
> Black population percentage in the FDI is explicitly a structural exposure proxy — not a biological or causal variable. It captures the geographic concentration of populations with documented disproportionate exposure to structural disinvestment. The index does not claim Black racial composition causes distress; it identifies where structural distress concentrates in Black communities, consistent with a 100-year federal data record.

**Red-team: "Ecological fallacy — place-level statistics aren't person-level conclusions."**
> This is correct and intentional. The index is a place-based instrument designed for place-based intervention, not individual-level inference. All findings are tract, county, or national — never attributed to individuals. This is stated in the methodology.

**Red-team: "Causality overreach — distress index shows correlation, not causation."**
> The index documents co-occurrence of structural conditions, not cause. Causal claims in the Black Paper are supported by historical and legislative record — redlining maps, USDA discriminatory lending documentation, VRA enforcement timelines — not inferred from the index alone.

---

## PENDING DATA (Next Pull Session)

The following sources were blocked by government server downtime (503) on April 18, 2026. They are queued for the next session and will expand the Raw Evidence Archive:

| Source | Data | Status |
|--------|------|--------|
| CDC PLACES county health | Diabetes, hypertension, obesity by county | 503 — retry |
| CDC BRFSS | State-level race health outcomes | 503 — retry |
| EPA EJScreen | County environmental burden by race | Batch pull needed |
| Vera Institute | County incarceration by race (historical) | Repo moved — locate new URL |
| CFPB HMDA | State + county mortgage denial by race | Auth issue — retry |
| NAEP NDE | State-level score gaps by race | Access method needed |

---

*E5 Enclave Incorporated | iamgodiam.net | CC0 1.0 Universal*
*By Grace, perfect ways.*

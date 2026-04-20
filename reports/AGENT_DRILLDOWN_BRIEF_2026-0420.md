# AGENT DRILLDOWN BRIEF — BDI / FarmBlock
**Version:** 1.0 | **Date:** April 20, 2026
**Agent:** Claude (drilldown pass on handoff `bdi-farmblock-drilldown-pNJ9P`)
**Authority:** E5 Enclave Incorporated | EIN 99-3822441
**DAG:** agent-drilldown-brief-2026-0420
**License:** CC0 1.0 Universal
**Audience:** Internal agentic team (next-Claude, Sue, Miranda, Moses, PRIME, LOGOS, PROOF)

---

## 1. PURPOSE

This brief captures the state of the BDI / FarmBlock stack as verified on
2026-04-20, after pulling the authoritative canonical files. It is the
recommended first read for any agent continuing Black Paper work. It is
**not** a rewrite document — see `CLAIM_REWRITES_MIRANDA_v1.md` for the
five approved Miranda rewrites.

---

## 2. FILES VERIFIED THIS PASS

| File | Repo | Role | Status |
|------|------|------|--------|
| `BDI_CLAIM_TRIAGE_MATRIX.md` | farmblock-data | 27-row claim audit | ✅ pulled |
| `STACK_TRUTH_TABLE.md` | farmblock-data | Canonical cross-repo crosswalk | ✅ pulled |
| `AUDIT_RESPONSE_PHASE1-6.md` | farmblock-data | Sue's 6-phase repo audit | ✅ pulled |
| `VAULT_MANIFEST.json` v3.1 | bdi-raw-data-vault | 17 raw files, ~14,811 points | ✅ pulled |
| `methodology/METHODOLOGY.md` | farmblock-data | FDI v2.0 formula doc | ✅ pulled |
| `methodology/fdi_manifest.json` | farmblock-data | 15,578 tracts / **50** cities | ✅ pulled |
| `BDI_QUANT_SPEC.md` | bdi-sovereign-dataset | Layered formula + counting rule | ✅ pulled (**root**, not `reports/`) |
| `reports/CLAIM_REWRITES_MIRANDA_v1.md` | bdi-raw-data-vault | Miranda's 5 approved rewrites | ✅ pulled |

---

## 3. MIRANDA'S FIVE REWRITES — VERIFIED AGAINST TRIAGE MATRIX

| # | Miranda rewrite | Matrix row | Result |
|---|-----------------|------------|--------|
| 1 | Slave Voyages: 12.5M embarked / 10.7M arrived / 1.8M died at sea | HI-1 | ⚠️ **Matrix drift** — only has 12.5M + 10.7M. Missing the 1.8M mortality figure. Arithmetically consistent (12.5 − 10.7 = 1.8). Miranda's three-number version is authoritative. |
| 2 | Cancer Alley fence-line tracts 65–94% Black | H-3 / CD-5 | ✅ matches |
| 3 | NAEP 24pp gap; parity 120+ years | ED-1 | ✅ matches |
| 4 | Humphreys poverty 32.1% + 55% child (ACS 2022) | CD-6 Option A | ✅ matches (recommended option) |
| 5 | Drop $4.5B; use HUD OIG 2013 53% non-filing | HO-3 | ✅ matches |

**Net:** 4/5 match cleanly. 1/5 (HI-1) needs the matrix updated to carry
the three-number form.

---

## 4. NEW DRIFTS FOUND (beyond Miranda's 5)

### 4.1 BDI_QUANT_SPEC.md §5 — stale tract/city counts
- Says: tract FDI = **12,426 tracts / 49 priority cities**
- STACK_TRUTH_TABLE locks: **15,578 tracts / 50 cities**
- Per STACK_TRUTH_TABLE's own supremacy rule ("this table wins"), the
  quant spec must be updated. Likely blast radius: §5 only.

### 4.2 STACK_TRUTH_TABLE — stale drift note
- Lists under "RECONCILIATION STATUS" that `fdi_manifest.json` says 49
  cities and needs updating to 50.
- Reality (verified this pass): `methodology/fdi_manifest.json` already
  says `"cities": 50`. The drift is **resolved**; the truth table's
  ledger row is stale and should be removed or marked resolved.

### 4.3 `reports/` path assumption in handoff
- Handoff guessed `BDI_QUANT_SPEC.md` lives in `bdi-raw-data-vault/reports/`.
- Actual location: **root of `bdi-sovereign-dataset`**. Update any
  downstream tooling that walks the path.

---

## 5. CANONICAL FILE INDEX — QUICK REFERENCE

```
LAYER 1 — Raw Evidence (bdi-raw-data-vault)
  VAULT_MANIFEST.json v3.1           — 17 files, ~14,811 pts
  STACK.md                           — architecture
  reports/REPORT_1_SCIENTIFIC_RAW.md — empirical record
  reports/REPORT_2_ANALYTICAL_READING.md
  reports/REPORT_3_BLACK_PAPER_ADJUSTMENTS.md
  reports/METHODOLOGY_CHAPTER_v2.md  — Sue's authored methodology
  reports/CLAIM_REWRITES_MIRANDA_v1.md — ⭐ 5 approved rewrites
  reports/HUMPHREYS_COMPOUND_DISTRESS_DECOMPOSITION.md
  reports/AGENT_DRILLDOWN_BRIEF_2026-0420.md — this file

LAYER 2 — Synthesized (bdi-sovereign-dataset)
  BDI_QUANT_SPEC.md v1.0             — ⭐ layered formula + counting rule
  bdi_sovereign_dataset_v1.json      — 1,574 empirical observations, 8 pillars

LAYER 3 — Place Distress (farmblock-data + farmblock-dataset)
  farmblock-data/
    BDI_CLAIM_TRIAGE_MATRIX.md       — ⭐ 27-row claim audit
    STACK_TRUTH_TABLE.md             — ⭐ supremacy crosswalk
    AUDIT_RESPONSE_PHASE1-6.md       — Sue's 6-phase audit
    methodology/METHODOLOGY.md
    methodology/fdi_manifest.json    — 15,578 tracts / 50 cities
    processed/farmblock_fdi_v2.csv   — scored tract data
  farmblock-dataset/
    farmblock_fdi_phase2.csv         — 24-county pilot release
    methodology/fdi_methodology_v2.json
```

---

## 6. LOCKED PUBLIC NUMBERS (use verbatim)

| Claim | Locked value |
|-------|--------------|
| Tracts scored | **15,578** |
| Priority cities (tract FDI) | **50** |
| Counties (Phase 2 pilot) | **24** |
| Counties (Phase 3 scope) | **~3,144** |
| Priority states (BDI composite) | **17** |
| BDI empirical observations | **1,574** (never 1,855) |
| Raw vault data points | **~14,811** |
| Empirical scoring window | **1991–2024** |
| Historical evidence span | **1514–2024** |
| Tract FDI composite weights | **1/6 × 6** (equal) |
| County FDI composite weights | **25/25/20/15/15** (poverty/health/digital/vacancy/Black_pct) |
| BDI composite weights | **20/20/20/15/10/10/5** (Econ/Health/CJ/Ed/Housing/Env/Pol) |

---

## 7. OPEN ITEMS FOR NEXT PASS

1. **Patch BDI_QUANT_SPEC.md §5** — update tract count to 15,578 and city
   count to 50.
2. **Update BDI_CLAIM_TRIAGE_MATRIX.md row HI-1** — carry the 1.8M
   died-at-sea figure from Miranda Rewrite 1.
3. **Retire the stale 49-city ledger row** in STACK_TRUTH_TABLE.md
   RECONCILIATION STATUS (manifest already at 50).
4. **Apply the five Miranda rewrites** to the Black Paper manuscript once
   the user drops the draft into session.
5. **Secondary audit** — scan the manuscript for any remaining
   "1,855 data points," "85% Black" (Cancer Alley), "20-point NAEP,"
   "64 years," "$4.5 billion Section 3" phrasing.

---

## 8. AGENT DO / DON'T

**Do**
- Use `raw.githubusercontent.com` or `mcp__github__get_file_contents`
  — never guess at URLs.
- When STACK_TRUTH_TABLE and any other file disagree, the truth table
  wins; update the other file.
- Keep Miranda's three-number Slave Voyages formulation verbatim
  (12.5M / 10.7M / 1.8M).

**Don't**
- Don't revive the iCloud belief — all data is public GitHub, CC0.
- Don't second-guess Miranda's five rewrites; Trinity reviewed, PRIME
  and Moses cleared.
- Don't re-fetch files confirmed in §2 without cause.
- Don't conflate Product A (national BDI composite) with Product B
  (tract/county FDI) — they are different scoring systems.
- Don't use "1,855 data points" anywhere. Ever.

---

**Publisher:** E5 Enclave Incorporated | EIN: 99-3822441
**SAM.gov UEI:** H8NGXEYE2HH8 | 501(c)(3)
**DAG:** agent-drilldown-brief-2026-0420
*By Grace, perfect ways.*

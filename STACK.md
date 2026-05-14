# BDI / FarmBlock Data Stack Crosswalk

| Repo | Layer | Unit of Analysis | Public/Citation Role | Upstream | Downstream | Status |
|------|-------|-----------------|---------------------|----------|------------|--------|
| bdi-raw-data-vault | raw evidence | source documents | primary source citation | — | bdi-sovereign-dataset | canonical |
| bdi-sovereign-dataset | synthesized dataset | 8 pillars, 1855 data points | empirical dataset citation | bdi-raw-data-vault | bdi-black-paper | canonical |
| bdi-black-paper | narrative publication | full manuscript | public research publication | bdi-sovereign-dataset | — | canonical |
| farmblock-data | tract layer | 15,578 census tracts | spatial distress index | — | farmblock-dataset | canonical |
| farmblock-dataset | county pilot | 49 cities | county-level analysis | farmblock-data | — | canonical |

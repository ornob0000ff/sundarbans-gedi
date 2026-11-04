# Manuscript item -> file map

Fill in the right-hand columns as you consolidate the code. Check every printed number against the manuscript.

| Manuscript item | Produced by | Checkpoint to compare |
|---|---|---|
| Mangrove area (Section 2.1) | `gee_js/` step 1 | about 356,331 ha |
| Table 2 (footprint inventory) | `notebooks/01_gedi_grid` | 321,001 L2A footprints in total |
| Cells (Section 3.1) | `notebooks/01_gedi_grid` | 1,167 cells with at least 20 footprints |
| Connected block (Section 3.2) | `notebooks/03_models` | 1,162 cells, 5 detached removed |
| Table 3 (correlations) | `notebooks/03_models` | e.g. longitude vs RH98 = 0.74 |
| Table 4 (block-CV R2) | `notebooks/03_models` | connected block height: linear 0.72 / 0.78 / 0.79, forest 0.81 / 0.82 / 0.82 |
| Block counts (Section 4.4) | `notebooks/03_models` | 33 blocks |
| Bootstrap and Moran's I (Sections 4.4, 4.5) | `notebooks/03_models` | forest gain 0.01 (-0.03 to +0.03); Moran's I 0.39 / 0.43 |
| Table S1 (filter sensitivity) | `notebooks/04_robustness_vertical` | east-west difference 7.0-8.0 m |
| Table 6 (vertical metrics) | `notebooks/04_robustness_vertical` | PAI 0.20 / 1.41 / 2.65 |
| Figures 1 and 2 | `notebooks/05_figures` | |
| Figures 3, 4, 5, S1, S2, S3 | `notebooks/05_figures` | |
| Landsat audit (Supplement S1) | `gee_js/` | see the audit tables in the supplement |

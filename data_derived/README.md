# Derived data

Small tables produced by the notebooks. Each row is a 2 km cell unless stated.

| File | Produced by | Contents |
|---|---|---|
| `gedi_grid_2km.csv` | `01_gedi_grid` | Per-cell median RH98, cover, PAI, AGBD and footprint counts; cell centre lon/lat |
| `pml_et_cells.csv` | `02_covariates` | Per-cell PML_V2.2a ET, Ec, Es (January-March 2019-2023, mm per day) |
| `cells_frag.csv` | `02_covariates` | Mangrove share and mangrove edge share per cell |
| `cells_all.csv` | `02_covariates` | Merged table: GEDI + NDMI + distance to water + ET |
| `table4_full.csv` | `03_models` | Leave-one-block-out R2 by subset, response and model |
| `cells_vertical.csv` | `04_robustness_vertical` | Per-cell FHD, PAI by layer, share above 10 m |
| `filter_sensitivity.csv` | `04_robustness_vertical` | Footprint counts and median RH98 by zone and filter |

Licenses: source data are public (NASA, USGS, ESA, Zhang et al. for PML). Confirm that redistribution of derived values is allowed under each source license, especially PML_V2.2a, before publishing this folder.

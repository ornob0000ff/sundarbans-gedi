# GEDI canopy structure of the Bangladesh Sundarbans

Code and derived data for the manuscript:

> Ornob A. *GEDI lidar canopy structure of the Bangladesh Sundarbans mangroves: a west-east gradient and the limits of satellite covariates.* [journal, year, DOI: to add after publication]

**Status:** research code release accompanying a manuscript in preparation. It is not a supported software tool.

## What this repository does

1. Builds a 2 km grid of GEDI canopy-structure medians (height RH98, cover, plant area index, foliage profile, modelled biomass) for the Bangladesh Sundarbans, 2019-2023.
2. Attaches candidate covariates to each cell: Landsat 8 NDMI, PML_V2.2a evapotranspiration, distance to water and fragmentation metrics.
3. Tests, with leave-one-block-out spatial cross-validation, whether the covariates explain structure beyond cell position, with bootstrap intervals and Moran's I.
4. Checks the robustness of the main result to GEDI quality filters and block size.
5. Documents a Landsat quality audit (1990-2024) in Google Earth Engine.

## Repository layout

| Folder | Contents |
|---|---|
| `gee_js/` | Earth Engine Code Editor scripts (Landsat audit, annual composites) |
| `notebooks/` | Colab / Jupyter notebooks, run in numerical order |
| `data_derived/` | Small derived tables produced by the notebooks (see `data_derived/README.md`) |
| `figures/` | Figure files for the manuscript |
| `docs/` | `FILE_MAP.md` linking each manuscript table and figure to the file that produces it |

## How to reproduce

1. Get an Earth Engine account and a Google Cloud project registered for Earth Engine. Replace `YOUR_PROJECT_ID` in each notebook with your project ID.
2. Open the notebooks in Google Colab in order (`01` to `05`). Each notebook starts by mounting Google Drive and setting an output folder.
3. Compare each notebook's printed checkpoints with `docs/FILE_MAP.md`.

Software: Python [version], with the packages in `requirements.txt` [pin versions with `pip freeze` from your Colab session]. Earth Engine collections can be updated by their providers, so numbers may shift slightly if rerun later.

## Data sources (all public)

| Dataset | Earth Engine ID or source |
|---|---|
| ESA WorldCover v200 | `ESA/WorldCover/v200` |
| GEDI L2A / L2B / L4A monthly rasters | `LARSE/GEDI/GEDI02_A_002_MONTHLY`, `LARSE/GEDI/GEDI02_B_002_MONTHLY`, `LARSE/GEDI/GEDI04_A_002_MONTHLY` |
| Landsat 5, 7, 8, 9 Collection 2 Level-2 | `LANDSAT/LT05/C02/T1_L2`, `LANDSAT/LE07/C02/T1_L2`, `LANDSAT/LC08/C02/T1_L2`, `LANDSAT/LC09/C02/T1_L2` |
| PML_V2.2a | `projects/pml_evapotranspiration/PML/OUTPUT/PML_V22a` |
| Country boundary | `USDOS/LSIB_SIMPLE/2017` |

Please cite the original datasets (see the manuscript reference list).


## License

Code: MIT (see `LICENSE`). Derived tables: [choose, for example CC BY 4.0, and confirm that the source data licenses allow redistribution of derived values].

## Citation

See `CITATION.cff`. After the first release, add the Zenodo DOI here.

## Contact

Abir Ornob, [a.ornob@outlook.com]

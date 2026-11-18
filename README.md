# Mauritania Datasets — Open Data Hub for Mauritania 🇲🇷

**Mauritania Datasets** is a centralized, curated collection of public datasets about the Islamic Republic of Mauritania, gathered from official national publications and international organisations, documented with consistent metadata and organised by theme.

> **This repository contains data, metadata and documentation only.** Every dataset keeps its original licence and attribution. Nothing here is an official statistic of the Government of Mauritania unless the metadata says so.

| | |
|---|---|
| Datasets catalogued | **233** |
| Datasets hosted in this repository (redistribution allowed) | **137** (556 files, 343 MB) |
| Catalogued as references only (not redistributable, unclear licence, or too large) | **96** |
| Distinct original publishers | **87** (56 for hosted datasets) |
| Categories | **28** |
| Last full check | 2026-11-14 |

## Mission and objectives

- **Centralise**: bring together, in one place, the scattered public data about Mauritania: demography, economy, health, education, agriculture, livestock, fisheries, environment, climate, infrastructure and more.
- **Document provenance**: every dataset has a source URL, publisher, licence, reference period, retrieval date and processing notes.
- **Respect licences**: only data whose licence explicitly permits redistribution are hosted; everything else is catalogued as a reference with a link to the original.
- **Make data usable**: standard formats (UTF-8 CSV, GeoJSON, Parquet), stable identifiers and machine-readable metadata for data scientists, researchers, students, journalists, NGOs and developers.

## Who it is for

Data scientists and machine-learning engineers, data engineers, researchers and academics, university students, developers, journalists, NGOs and institutions working on Mauritania.

## Dataset categories

| Category | Hosted datasets | Reference-only | Total | Available formats (hosted) |
|---|---:|---:|---:|---|
| [Demographics](data/demographics/) | 7 | 16 | 23 | CSV, XLSX, XLS, GeoTIFF, GZ, 7Z |
| [Economy](data/economy/) | 7 | 23 | 30 | CSV |
| [Education](data/education/) | 5 | 1 | 6 | CSV, GeoJSON |
| [Health](data/health/) | 10 | 7 | 17 | CSV, GeoJSON, XLSX |
| [Agriculture](data/agriculture/) | 9 | 1 | 10 | CSV |
| [Livestock](data/livestock/) | 3 | 2 | 5 | CSV |
| [Fisheries](data/fisheries/) | 5 | 4 | 9 | CSV, XLSX |
| [Food security](data/food-security/) | 11 | 0 | 11 | CSV, GeoJSON, XLSX, XLS, PDF, ZIP |
| [Geography](data/geography/) | 3 | 2 | 5 | GeoJSON, XLSX, GeoTIFF, ZIP |
| [Administrative divisions](data/administrative-divisions/) | 3 | 1 | 4 | CSV, GeoJSON, XLSX, GZ |
| [Environment](data/environment/) | 8 | 3 | 11 | CSV, GZ |
| [Climate](data/climate/) | 6 | 0 | 6 | CSV, ZIP |
| [Energy](data/energy/) | 4 | 1 | 5 | CSV, XLSX, ZIP |
| [Water](data/water/) | 2 | 0 | 2 | CSV, GeoJSON |
| [Transport](data/transport/) | 10 | 3 | 13 | CSV, GeoJSON, XLSX, PDF, ZIP |
| [Infrastructure](data/infrastructure/) | 4 | 1 | 5 | CSV, GeoJSON |
| [Public finance](data/public-finance/) | 2 | 7 | 9 | CSV |
| [Elections](data/elections/) | 0 | 2 | 2 | — |
| [Telecommunications](data/telecommunications/) | 2 | 2 | 4 | CSV |
| [Employment](data/employment/) | 5 | 2 | 7 | CSV, Parquet |
| [Poverty](data/poverty/) | 6 | 6 | 12 | CSV, Parquet |
| [Trade](data/trade/) | 2 | 1 | 3 | CSV |
| [Tourism](data/tourism/) | 2 | 0 | 2 | CSV, GeoJSON |
| [Mining](data/mining/) | 2 | 1 | 3 | CSV, XLSX |
| [Housing](data/housing/) | 2 | 2 | 4 | CSV |
| [Humanitarian](data/humanitarian/) | 11 | 7 | 18 | CSV, GeoJSON, XLS |
| [Governance](data/governance/) | 4 | 1 | 5 | CSV |
| [Gender](data/gender/) | 2 | 0 | 2 | CSV |
| **Total** | **137** | **96** | **233** | |

Counts are computed from [`metadata/datasets.json`](metadata/datasets.json). A category with zero hosted datasets (e.g. elections) has only reference entries, because no openly licensed source was found.

## Repository structure

```text
mauritania-datasets/
├── README.md                 ← this file
├── LICENSE                   ← licence of this project's own documentation and metadata (CC BY 4.0)
├── LICENSE-DATA.md           ← licensing and attribution policy for the datasets
├── CITATION.cff              ← how to cite this repository
├── data/
│   └── <category>/
│       └── <dataset-slug>/
│           ├── README.md     ← source, licence, period, processing, limitations
│           └── …data files…
├── metadata/
│   ├── datasets.json         ← full catalogue (hosted + reference-only)
│   ├── datasets.csv          ← flat version of the catalogue
│   ├── sources.json          ← data sources / platforms and publishers
│   ├── categories.json       ← categories with counts and formats
│   └── excluded-series.csv   ← World Bank series excluded for licence/metadata reasons
└── documentation/
    ├── data-policy.md        ← inclusion, licensing and ethics rules
    ├── data-quality.md       ← conventions, QC results, known gaps
    └── data-dictionary.md    ← metadata fields and common data columns
```

## Data sources

Hosted datasets come from these platforms:

| Source | Hosted datasets |
|---|---:|
| Humanitarian Data Exchange (HDX, OCHA) | 63 |
| World Bank Data360 | 33 |
| FAOSTAT (FAO) | 21 |
| Zenodo (CERN) | 8 |
| ILOSTAT (International Labour Organization) | 3 |
| UN World Population Prospects (UN DESA Population Division) | 1 |
| WorldPop (University of Southampton) | 1 |
| DataverseNL | 1 |
| FAO FishStat (Fisheries and Aquaculture statistics) | 1 |
| geoBoundaries (William & Mary geoLab) | 1 |
| Our World in Data | 1 |
| NASA POWER (Prediction Of Worldwide Energy Resources) | 1 |
| OurAirports | 1 |
| EITI International Secretariat | 1 |

Through HDX, the hosted data also include datasets published by OCHA, UNHCR, WFP, FEWS NET, WHO, UNESCO, UNFPA, UNDP, UN-Habitat, IPC, IDMC, IFRC, CERF, the DHS Program, OPHI, HOT/OpenStreetMap, Kontur, Copernicus/JRC, Climate TRACE, HeiGIT, Transparency International and others. The full list of 87 publishers is in [`metadata/sources.json`](metadata/sources.json).

**Mauritanian official sources** (ANSADE, Banque Centrale de Mauritanie, Ministry of Finance / Direction Générale du Budget, CENI, ARE, IMROP, ONISPA, SNIM…) are catalogued with direct links to their publications: census RGPH 2013 and 2023, statistical yearbooks, CPI notes, national accounts, EPCV poverty surveys, EDSM/DHS, MICS, labour force surveys, the 2024 livestock census, finance laws, TOFE and debt bulletins, election reports and more. As of 2026-11-14 none of these sites publishes an open licence, and several state "Tous droits réservés", so their files are **not** redistributed here (see [data policy](documentation/data-policy.md)).

## How to access the data

**Browse.** Open `data/<category>/` on GitHub; every dataset folder has a README.

**Clone everything:**

```bash
git clone https://github.com/MauriDataHub/mauritania-datasets.git
```

**Download a single file:** use the "Raw" button, or

```bash
curl -LO https://raw.githubusercontent.com/MauriDataHub/mauritania-datasets/main/data/demographics/world-bank-wdi-demographics/wb_wdi_demographics_long.csv
```

**Use the catalogue programmatically:**

```python
import json, pandas as pd
cat = json.load(open("metadata/datasets.json"))["datasets"]
hosted = [d for d in cat if d["hosted_in_repository"]]
health = [d for d in hosted if d["category"] == "health"]
df = pd.read_csv(health[0]["files"][0]["path"])
```

Each hosted dataset in `datasets.json` lists its files with path, format, size, row count (CSV) and SHA-256 checksum.

## Data formats

| Format | Files | Used for |
|---|---:|---|
| CSV (UTF-8) | 351 | Tabular data (default) |
| Parquet | 6 | Large analytical tables (ILOSTAT, satellite wealth estimates) |
| GeoJSON | 104 | Vector geographic data (WGS 84) |
| XLSX / XLS | 34 | Original spreadsheets whose structure matters (EITI, research datasets, legacy OCHA files) |
| GeoTIFF | 5 | Raster grids (population, built-up area) |
| ZIP / GZ / 7Z | 23 | Original archives (zipped shapefiles, GeoPackages, rasters) |
| PDF | 3 | Methodology papers redistributed under the dataset licence |
| JSON / TXT | 26 | Publisher metadata and readme files |

Where a dataset was filtered from a multi-country file, only the Mauritania rows were kept and the filter is described in its README. No values were changed or imputed.

## Licensing and attribution

- **Datasets keep their original licence.** The licence of each dataset is in its README and in `metadata/datasets.json` (`license`, `license_url`, `license_conditions`). See [LICENSE-DATA.md](LICENSE-DATA.md).
- Licences of hosted datasets:

| Licence | Hosted datasets |
|---|---:|
| CC BY 4.0 | 80 |
| CC BY 3.0 IGO | 24 |
| ODbL 1.0 | 14 |
| CC0 1.0 | 4 |
| CC BY-SA 4.0 | 4 |
| CC BY-NC-SA 3.0 IGO | 3 |
| CC BY-ND 4.0 | 2 |
| Creative Commons Attribution 3.0 Intergovernmental Organisations (CC BY 3.0 IGO) / Creative Commons Attribution-ShareAlike 3.0 Unported | 1 |
| NASA open data (no restrictions; attribution requested) | 1 |
| Public Domain | 1 |
| CC BY-NC 4.0 | 1 |
| EITI content policy (free republication with credit) | 1 |
| CC BY 3.0 IGO / CC BY 4.0 | 1 |

- **Some licences carry conditions**: *NC* = non-commercial only (WHO GHO, ITU, Meta RWI); *ND* = no derivatives (DHS STATcompiler files, redistributed unmodified); *SA* / *ODbL* = share-alike. Check `license_conditions` before reuse.
- **this project's own work** (README files, metadata, documentation) is licensed under [CC BY 4.0](LICENSE).
- **Always cite the original publisher**; each dataset README includes an attribution line.

Redistribution status of every catalogued dataset:

| Status | Meaning | Datasets |
|---|---|---:|
| `allowed` | Explicit open licence permits redistribution | 149 (137 hosted, 12 not mirrored because of size or download restrictions) |
| `link_only` | Public, but no explicit licence permitting redistribution | 62 |
| `restricted` | Terms forbid redistribution or require registration/approval | 17 |
| `unknown` | Licence could not be determined | 5 |

## Contributing

Contributions are welcome, as **data and metadata only** (no code):

1. Open an issue describing the dataset: title, publisher, source URL, licence, and why it matters for Mauritania.
2. Make sure the licence **explicitly** allows redistribution. If it doesn't, propose a reference-only entry instead.
3. Add files under `data/<category>/<dataset-slug>/` with a `README.md` following the existing ones (source, licence, reference period, processing, limitations).
4. Add or update the entry in `metadata/datasets.json` using the fields in the [data dictionary](documentation/data-dictionary.md).
5. Do not add scripts, notebooks, credentials, personal data or files over 50 MB.

Corrections (broken links, wrong metadata, newer releases) are especially valuable. Please also report any dataset you believe is mislicensed.

## Dataset statistics

- 233 datasets catalogued: 137 hosted, 96 reference-only.
- 556 data files, 343 MB in total; largest single file below 50 MB.
- World Bank data cover 1827 indicator series (WDI split into 22 thematic datasets plus 10 specialised World Bank databases).
- 21 FAOSTAT domains, 3 ILOSTAT thematic datasets, 63 datasets from the Humanitarian Data Exchange.
- Temporal coverage ranges from 1950 (FAO fisheries, UN WPP) to projections up to 2100 (UN WPP).

## Citation

If you use Mauritania Datasets, cite **both** the original publisher of each dataset (see its README) **and** this repository:

> Mauritania Datasets contributors (2026). *Mauritania Datasets — Open Data Hub for Mauritania* [Data set]. Version 2026-11-14. https://github.com/MauriDataHub/mauritania-datasets

Machine-readable citation metadata is in [CITATION.cff](CITATION.cff).

## Disclaimer

Data are provided as published by their original sources, without warranty. Boundaries and names on maps do not imply any judgement on the legal status of any territory. Report problems through the issue tracker.

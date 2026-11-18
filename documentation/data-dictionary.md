# Data dictionary

## 1. Catalogue fields (`metadata/datasets.json`)

`datasets.json` has the shape `{"generated": date, "count": n, "datasets": [ … ]}`. Each dataset object has these fields:

| Field | Type | Description |
|---|---|---|
| `id` | string | Stable identifier `MRT-<CAT>-<NNN>` (category code + sequence). |
| `slug` | string | Folder name of the dataset (`data/<category>/<slug>/`); reference-only entries start with `ref-`. |
| `title` | string | Dataset title (publisher's title where available). |
| `description` | string | What the dataset contains. |
| `category` | string | One of the categories in `metadata/categories.json`. |
| `country` | string | Always `Mauritania`. |
| `geographic_coverage` | string | National, subnational level, points, or a specific area. |
| `spatial_resolution` | string | Spatial unit or grid resolution (when relevant). |
| `reference_period` | string | Period the data refer to (`YYYY–YYYY`, or HDX date range). `null` if not stated by the publisher. |
| `temporal_resolution` | string | Annual, monthly, … (when known). |
| `publisher` | string | Organisation that publishes the data. |
| `original_source` | string | Upstream producer, when different from the publisher. |
| `source_id` | string | Key into `metadata/sources.json`. |
| `source_name` | string | Platform/database name. |
| `source_url` | string | Landing page of the original publication. |
| `download_url` | string | Direct file or API URL used for retrieval (when a single one exists). |
| `resource_urls` | array | All original resource URLs (multi-file datasets). |
| `doi` | string | DOI for research datasets. |
| `formats` | array | File formats present (hosted) or offered by the publisher (reference-only). |
| `license` | string | Licence name as stated by the publisher; `Not stated` if none was found. |
| `license_url` | string | Link to the licence text. |
| `license_conditions` | string | Extra conditions (non-commercial, no-derivatives, share-alike). |
| `redistribution` | enum | `allowed`, `link_only`, `restricted`, `unknown` (see data policy). |
| `hosted_in_repository` | bool | `true` if files are in this repository. |
| `not_hosted_reason` | string | Why files are not hosted (reference-only entries). |
| `access` | string | `open`, `registration`, `request` (reference-only entries, when known). |
| `path` | string | Folder of the dataset in the repository. |
| `files` | array | For hosted datasets: `{path, format, bytes, sha256, rows}` per file (`rows` = data rows of CSV files, excluding header). |
| `publication_date` | string | Publication date stated by the publisher. |
| `source_last_updated` | string | Last-modified date reported by the source platform. |
| `date_added` | date | Date the dataset was added to Mauritania Datasets. |
| `date_last_checked` | date | Date the source and licence were last checked. |
| `processing` | string | Exactly what was done to the original data (filtering, conversion). |
| `limitations` | string | Known caveats. |
| `notes` | string | Other remarks. |
| `attribution` | string | Suggested attribution line. |
| `indicator_count` | int | Number of indicator series (indicator datasets). |

## 2. `metadata/sources.json`

`sources`: `source_id`, `name`, `type` (`national_government`, `international_org`, `academic`, `ngo`, `other`), `website`, `terms_url`, `license_summary`, `redistribution` (for national sources), `verified`, `notes`, `datasets_in_catalogue`. `publishers`: list of `{publisher, datasets}`.

## 3. `metadata/categories.json`

`id`, `code` (used in dataset IDs), `title`, `description`, `path`, `datasets_total`, `datasets_hosted`, `datasets_reference_only`, `formats_hosted`.

## 4. Common data layouts

### World Bank indicator datasets (`data/*/world-bank-*`)

| Column | Description |
|---|---|
| `indicator_id` | Data360 identifier (e.g. `WB_WDI_SP_POP_TOTL`). |
| `indicator_code` | Original World Bank series code (e.g. `SP.POP.TOTL`). |
| `indicator_name` | Series name. |
| `unit` | Unit of measure from the series metadata. |
| `sex`, `age`, `urbanisation` | SDMX disaggregation codes (`_T` total, `_Z` not applicable, `F`/`M`, age bands, `U`/`R`). |
| `freq` | `A` annual. |
| `time_period` | Year (or period). |
| `value` | Numeric value as published. |
| `obs_status` | SDMX observation status (`A` normal, `E` estimated, `F` forecast, …). |
| `unit_mult` | Power-of-ten multiplier (0 = units). |

`*_wide.csv`: totals only, one row per year, one column per `indicator_code`. `indicators.csv`: indicator dictionary.

### FAOSTAT datasets (`data/*/faostat-*`)

Normalized FAOSTAT layout, unchanged: `Area Code` (136 = Mauritania), `Area Code (M49)`, `Area`, `Item Code`, `Item Code (CPC)`, `Item`, `Element Code`, `Element`, `Year Code`, `Year`, `Unit`, `Value`, `Flag`, `Note`. Flag meanings are in each `flags.csv`.

### ILOSTAT datasets

SDMX-CSV columns: `DATAFLOW`, `INDICATOR_LABEL`, `REF_AREA`, `FREQ`, `MEASURE`, classification dimensions (`SEX`, `AGE`, `EDU`, `ECO`, `OCU`, `GEO`, …), `TIME_PERIOD`, `OBS_VALUE`, `OBS_STATUS`, `UNIT_MEASURE`, `UNIT_MULT`, `SOURCE`, notes. Codes follow ILOSTAT classifications.

### HDX datasets

Files are as published. Many CSVs have a second header row of [HXL](https://hxlstandard.org/) hashtags (e.g. `#adm1+name`). Skip it when loading: `pd.read_csv(path, skiprows=[1])`.

### Geographic data

GeoJSON in WGS 84 (EPSG:4326). Administrative codes: OCHA P-codes (`ADM1_PCODE` like `MR01`… in COD-AB). Shapefiles stay zipped as published; GeoPackage/GeoTIFF keep their embedded CRS.

## 5. Missing values

Missing observations are **absent rows** in long tables and **empty cells** in wide tables. No imputation was done. Source-specific missing codes are kept as published (e.g. NASA POWER `-999`) and documented in each README.

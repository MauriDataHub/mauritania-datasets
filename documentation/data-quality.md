# Data quality

## 1. Conventions

- **Encoding**: all CSV files are UTF-8 (checked automatically). Latin-1 FAOSTAT files were re-encoded.
- **Column names**: original column names are kept so that files can be matched to publisher documentation. Mauritania Datasets-generated tables (World Bank, NASA POWER, ITU) use `snake_case`.
- **Dates**: ISO 8601 (`YYYY`, `YYYY-MM`, `YYYY-MM-DD`) in metadata. Data files keep the publisher's period format.
- **Units**: given per indicator (`unit` column, `Unit` in FAOSTAT, `UNIT_MEASURE` in ILOSTAT, `parameters.csv` for NASA POWER). Values are never rescaled.
- **Geographic names and codes**: ISO 3166 (`MRT`/`MR`), UN M49 `478`, FAO area code `136`, OCHA P-codes for subnational units. Names are kept as published (French transliterations vary: *Hodh Ech Chargui* / *Hodh El Chargui*, *Guidimakha* / *Guidimaka*).
- **CRS**: GeoJSON in WGS 84 (EPSG:4326). Rasters and GeoPackages keep their embedded CRS, documented in each README.
- **Time series** keep their original frequency and reference period.
- **Missing values** are not imputed (see data dictionary §5).
- **No silent transformations**: every filter or conversion is described in the dataset README (`Processing`) and in `datasets.json` (`processing`).

## 2. Quality-control checks (2026-11-14)

| Check | Result |
|---|---|
| Scripts / code / config / log files in the repository | 0 found |
| CSV files not valid UTF-8 | 0 |
| Empty CSV files | 0 |
| Files over 50 MB | 0 |
| Duplicate dataset IDs / titles | 0 / 0 |
| Byte-identical files across datasets | 3 groups, all FAOSTAT `flags.csv` code lists, kept so each dataset is self-contained |
| Country check (CSV files with a country column) | Non-Mauritania values only in IPC files, where `Area` holds sub-national area names (expected) |
| URLs checked (source, download, licence, websites) | 597 |
| URLs not reachable by an automated check | 22 (see §4) |
| World Bank series excluded (no open licence, SIPRI terms, or missing metadata) | 62, listed in `metadata/excluded-series.csv` |

Every hosted file has a SHA-256 checksum in `metadata/datasets.json` for integrity checks.

## 3. Datasets with incomplete metadata

These entries have a field the publisher does not state. The field is left empty rather than guessed.

| ID | Title | Missing |
|---|---|---|
| `MRT-ECO-027` | IMF International Financial Statistics (IFS) — Mauritania | reference_period |
| `MRT-ECO-028` | IMF World Economic Outlook — Mauritania | reference_period |
| `MRT-HLT-015` | UNICEF Data Warehouse — Mauritania | reference_period |
| `MRT-AGR-010` | ASTI Mauritania database (agricultural R&D indicators) | reference_period |
| `MRT-LIV-005` | Livestock mobility in Sahelian Africa: survey in Mauritania (Dryad) | reference_period |
| `MRT-FSH-001` | Replication Data for: Overfishing of threatened bycatch species in a marine protected area | reference_period |
| `MRT-FSH-003` | Exports fish meal and oil from Mauritania 2010 2020 | reference_period |
| `MRT-FSH-004` | Dataset for small pelagics value chain in Mauritania | reference_period |
| `MRT-FSH-006` | Bulletin Statistique 2025 : Le Secteur des Pêches en Chiffres | license |
| `MRT-FSH-007` | IMROP – Rapport de l'Enquête Cadre (décembre 2023) | license |
| `MRT-GEO-005` | qdgc Mauritania — Quarter-degree grid cells | reference_period |
| `MRT-ENV-005` | National Checklists: Mauritania Species List | reference_period |
| `MRT-ENV-009` | Copernicus Sentinel satellite imagery over Mauritania | reference_period |
| `MRT-ENV-011` | NASA Earthdata — satellite products over Mauritania (MODIS, VIIRS, GPM, SRTM…) | reference_period |
| `MRT-CLI-001` | ERA5-Land monthly: Total precipitation, monthly time series for Mauritania at 30 arc secon | reference_period |
| `MRT-ENE-001` | CCG Starter Data Kit: Mauritania | reference_period |
| `MRT-ENE-002` | CCG Whole Energy System Model Starter Data Kit for Mauritania | reference_period |
| `MRT-ENE-005` | Our World in Data — Energy dataset — Mauritania | reference_period |
| `MRT-TRN-001` | Transport Starter Data Kit: Historical socio-transport data for Mauritania | reference_period |
| `MRT-PFN-003` | Archive des lois de finances (LFI/LFR 2014–2026) – DGB | license |
| `MRT-ELE-001` | Rapport de la CENI – élection présidentielle 2024 | license |
| `MRT-ELE-002` | Rapport de la CENI – élections législatives, régionales et municipales 2023 | license |
| `MRT-TEL-003` | Rapport d'activité 2024 de l'Autorité de Régulation | license |
| `MRT-TEL-004` | Tableau de bord – marché de la téléphonie mobile (au 31/12/2013) | license |
| `MRT-POV-003` | Harmonised satellite-derived relative wealth estimates - Mauritania (feature panel + RWI s | reference_period |
| `MRT-POV-012` | World Bank ASPIRE — Social protection and labour indicators — Mauritania | reference_period, license |
| `MRT-MIN-003` | SNIM Annual Report 2024 | license |
| `MRT-GOV-005` | UN SDG Global Database — Mauritania | reference_period, license |

## 4. URLs that failed the automated check

Most failures are **bot protection** (HTTP 403 for automated clients, e.g. IMF, ILOSTAT, ITU, UNICEF, IRENA), which work in a browser. Some are **expired TLS certificates** (OurAirports, worldpop.org, petrole.gov.mr). The rest are **government sites that were unreachable** during the check. The links are kept because they are the official sources.

| URL | Result |
|---|---|
| http://www.cnitie.gov.mr/ | 503 |
| https://agriculture.gov.mr | ConnectionError |
| https://data.imf.org/ | 403 |
| https://data.unicef.org/dv_index/ | 403 |
| https://datahub.itu.int | 403 |
| https://datahub.itu.int/about | 403 |
| https://education.gov.mr | ConnectionError |
| https://hydraulique.gov.mr | ConnectionError |
| https://ilostat.ilo.org | 403 |
| https://ilostat.ilo.org/data/ | 403 |
| https://mics.unicef.org | 403 |
| https://ourairports.com/countries/MR/ | SSLError |
| https://ourairports.com/data/ | SSLError |
| https://transports.gov.mr | ConnectionError |
| https://www.economie.gov.mr | ConnectionError |
| https://www.imf.org/en/About/copyright-and-terms | 403 |
| https://www.imf.org/en/Data | 403 |
| https://www.imf.org/en/Publications/WEO | 403 |
| https://www.irena.org/Data | 403 |
| https://www.irena.org/terms-and-conditions | 403 |
| https://www.petrole.gov.mr | SSLError |
| https://www.worldpop.org | SSLError |

## 5. Known limitations

- **International estimates vs. national data**: many indicators (World Bank, ILO, WHO, FAO) are modelled or harmonised estimates and may differ from ANSADE publications. Check flags and source columns.
- **Administrative boundaries**: Mauritania has 15 wilayas since Nouakchott was split into three in 2014. Older layers (geoBoundaries ADM1, 2012 OCHA files, some indicators) use 13 wilayas.
- **OpenStreetMap layers** are crowd-sourced snapshots (HOT export of 2026-11-03); completeness varies by region.
- **Fisheries**: FAO capture data refer to Mauritanian-flagged reporting; catches by foreign fleets under fishing agreements are largely excluded.
- **Elections**: no machine-readable, openly licensed election results were found; only CENI reports are referenced.
- **Snapshots**: hosted files are snapshots as of `date_last_checked`. Live sources (WFP prices, IPC, HOT exports) are updated more frequently upstream.

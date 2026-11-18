# FAOSTAT — Suite of food security indicators — Mauritania

FAOSTAT domain FS ('Food Security and Nutrition: Suite of Food Security Indicators') filtered to Mauritania: 1069 rows covering 44 items and 3 elements, 2000–2025.

| Field | Value |
|---|---|
| Category | `food-security` |
| Publisher | Food and Agriculture Organization of the United Nations (FAO) |
| Geographic coverage | National |
| Reference period | 2000–2025 |
| Source page | https://www.fao.org/faostat/en/#data/FS |
| Original download / API | https://bulks-faostat.fao.org/production/Food_Security_Data_E_All_Data_(Normalized).zip |
| Licence | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
| Redistribution | `allowed` |
| Source last updated | 2026-07-21 |
| Retrieved | 2026-11-14 |

## Processing

Downloaded the FAOSTAT normalized bulk file (all countries) and kept only rows with `Area Code` = 136 (Mauritania). Columns, codes, units and values are unchanged; re-encoded from Latin-1 to UTF-8.

## Files

- `faostat_fs_mauritania.csv` — data rows for Mauritania.
- `flags.csv` — FAOSTAT flag definitions.

Columns follow the FAOSTAT normalized bulk format and are kept unchanged: `Area Code` (FAO country code, 136 = Mauritania), `Area Code (M49)` (UN M49 code, '478), `Item Code`/`Item`, `Element Code`/`Element`, `Year Code`/`Year`, `Unit`, `Value`, `Flag` (see the flags file), and `Note` where present. Some domains include additional code columns (e.g. CPC item codes, `Months`, `Source`).

## Limitations

FAOSTAT figures combine official national data with FAO estimates and imputations; check the `Flag` column (e.g. E = estimated, I = imputed, X = from international organizations).

## Attribution

FAO. Food Security and Nutrition: Suite of Food Security Indicators. FAOSTAT. Rome. Licence: CC BY 4.0. https://www.fao.org/faostat/en/#data/FS (accessed 2026-11-14).

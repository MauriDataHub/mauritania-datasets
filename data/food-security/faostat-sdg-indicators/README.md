# FAOSTAT — SDG indicators under FAO custodianship — Mauritania

FAOSTAT domain SDGB ('SDG Indicators: SDG Indicators') filtered to Mauritania: 1919 rows covering 185 items and 3 elements, 1990–2026.

| Field | Value |
|---|---|
| Category | `food-security` |
| Publisher | Food and Agriculture Organization of the United Nations (FAO) |
| Geographic coverage | National |
| Reference period | 1990–2026 |
| Source page | https://www.fao.org/faostat/en/#data/SDGB |
| Original download / API | https://bulks-faostat.fao.org/production/SDG_BulkDownloads_E_All_Data_(Normalized).zip |
| Licence | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
| Redistribution | `allowed` |
| Source last updated | 2026-09-29 |
| Retrieved | 2026-11-14 |

## Processing

Downloaded the FAOSTAT normalized bulk file (all countries) and kept only rows with `Area Code` = 136 (Mauritania). Columns, codes, units and values are unchanged; re-encoded from Latin-1 to UTF-8.

## Files

- `faostat_sdgb_mauritania.csv` — data rows for Mauritania.
- `flags.csv` — FAOSTAT flag definitions.

Columns follow the FAOSTAT normalized bulk format and are kept unchanged: `Area Code` (FAO country code, 136 = Mauritania), `Area Code (M49)` (UN M49 code, '478), `Item Code`/`Item`, `Element Code`/`Element`, `Year Code`/`Year`, `Unit`, `Value`, `Flag` (see the flags file), and `Note` where present. Some domains include additional code columns (e.g. CPC item codes, `Months`, `Source`).

## Limitations

FAOSTAT figures combine official national data with FAO estimates and imputations; check the `Flag` column (e.g. E = estimated, I = imputed, X = from international organizations).

## Attribution

FAO. SDG Indicators: SDG Indicators. FAOSTAT. Rome. Licence: CC BY 4.0. https://www.fao.org/faostat/en/#data/SDGB (accessed 2026-11-14).

# FAOSTAT — Macro-economic indicators — Mauritania

FAOSTAT domain MK ('Macro-Economic Indicators: Macro Indicators') filtered to Mauritania: 1555 rows covering 5 items and 8 elements, 1970–2025.

| Field | Value |
|---|---|
| Category | `economy` |
| Publisher | Food and Agriculture Organization of the United Nations (FAO) |
| Geographic coverage | National |
| Reference period | 1970–2025 |
| Source page | https://www.fao.org/faostat/en/#data/MK |
| Original download / API | https://bulks-faostat.fao.org/production/Macro-Statistics_Key_Indicators_E_All_Data_(Normalized).zip |
| Licence | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
| Redistribution | `allowed` |
| Source last updated | 2026-11-09 |
| Retrieved | 2026-11-14 |

## Processing

Downloaded the FAOSTAT normalized bulk file (all countries) and kept only rows with `Area Code` = 136 (Mauritania). Columns, codes, units and values are unchanged; re-encoded from Latin-1 to UTF-8.

## Files

- `faostat_mk_mauritania.csv` — data rows for Mauritania.
- `flags.csv` — FAOSTAT flag definitions.

Columns follow the FAOSTAT normalized bulk format and are kept unchanged: `Area Code` (FAO country code, 136 = Mauritania), `Area Code (M49)` (UN M49 code, '478), `Item Code`/`Item`, `Element Code`/`Element`, `Year Code`/`Year`, `Unit`, `Value`, `Flag` (see the flags file), and `Note` where present. Some domains include additional code columns (e.g. CPC item codes, `Months`, `Source`).

## Limitations

FAOSTAT figures combine official national data with FAO estimates and imputations; check the `Flag` column (e.g. E = estimated, I = imputed, X = from international organizations).

## Attribution

FAO. Macro-Economic Indicators: Macro Indicators. FAOSTAT. Rome. Licence: CC BY 4.0. https://www.fao.org/faostat/en/#data/MK (accessed 2026-11-14).

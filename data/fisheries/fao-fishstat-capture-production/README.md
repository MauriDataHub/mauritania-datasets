# FAO FishStat — Capture fisheries production by species — Mauritania

Annual capture production of Mauritania (flag state reporting) by species and FAO major fishing area, 1950–2023 (2927 rows, 121 species items).

| Field | Value |
|---|---|
| Category | `fisheries` |
| Publisher | Food and Agriculture Organization of the United Nations (FAO) |
| Geographic coverage | National (by FAO major fishing area) |
| Reference period | 1950–2023 |
| Source page | https://www.fao.org/fishery/en/collection/capture |
| Original download / API | https://www.fao.org/fishery/static/Data/Capture_2025.1.0.zip |
| Licence | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
| Redistribution | `allowed` |
| Source last updated | 2025-03-28 |
| Retrieved | 2026-11-14 |

## Processing

Extracted `Capture_Quantity.csv` from the global release and kept rows with `COUNTRY.UN_CODE` = 478. `*_original.csv` keeps the original columns; `*_labelled.csv` adds species names (EN/FR), scientific name, ISSCAAP and yearbook groups from the FAO code lists in the same release. No values were changed.

## Files

- `capture_quantity_mauritania_original.csv` — rows as released by FAO.
- `capture_quantity_mauritania_labelled.csv` — same rows with species and area labels.
- `CL_FI_SYMBOL_SDMX.csv`, `FSJ_UNIT.csv` — code lists for status and unit.
- `ReadMe.txt` — FAO release notes.

## Limitations

Figures are attributed to the flag state of the vessels reporting to FAO; catches by foreign fleets in Mauritania's EEZ (under fishing agreements) are generally not included here. `MEASURE` gives the unit (e.g. `Q_tlw` = tonnes live weight; see `FSJ_UNIT.csv`); `STATUS` gives observation status (see `CL_FI_SYMBOL_SDMX.csv`).

## Attribution

FAO. 2025. Fishery and Aquaculture Statistics – Global capture production 1950–2023 (FishStatJ). FAO Fisheries and Aquaculture Division, Rome. Licence: CC BY 4.0.

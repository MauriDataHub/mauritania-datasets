# World Bank Poverty and Inequality Platform (PIP) — Mauritania

13 Poverty and Inequality Platform (PIP) series for Mauritania (1024 observations, 1987–2019). Series already published in the WDI datasets of this repository are excluded to avoid duplication.

| Field | Value |
|---|---|
| Category | `poverty` |
| Publisher | World Bank |
| Geographic coverage | National |
| Reference period | 1987–2019 |
| Source page | https://data360.worldbank.org/en/dataset/WB_PIP |
| Original download / API | https://data360api.worldbank.org/data360/data?DATABASE_ID=WB_PIP&REF_AREA=MRT |
| Licence | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) |
| Redistribution | `allowed` |
| Source last updated | Not stated |
| Retrieved | 2026-11-14 |

## Processing

Retrieved from the World Bank Data360 API (REF_AREA=MRT). Converted from JSON to CSV; observations with non-numeric values dropped; series without an explicit open licence in the Data360 metadata excluded (see `metadata/excluded-series.csv`). The wide file is a pivot of the long file (totals only).

## Files

- `wb_pip_long.csv` — one row per indicator × disaggregation × period. Columns: `indicator_id` (Data360 ID), `indicator_code` (original World Bank series code), `indicator_name`, `unit`, `sex`/`age`/`urbanisation` (SDMX codes; `_T` = total, `_Z` = not applicable), `freq` (`A` = annual), `time_period`, `value`, `obs_status` (SDMX observation status; `A` = normal, `E` = estimated, `F` = forecast).
- `wb_pip_wide.csv` — totals only (no sex/age/urban breakdown), annual, one column per `indicator_code`, one row per year.
- `indicators.csv` — indicator dictionary: name, unit, definition (when provided), original compiling source, licence, coverage.

Values are as published by the World Bank (no rescaling). Units are given per indicator in `unit`. Missing years are simply absent (no gap filling).

## Limitations

Many World Bank series for Mauritania are modelled or estimated by international agencies rather than reported by national statistical offices; check `obs_status` and the original source in `indicators.csv`. Coverage varies widely by indicator.

## Attribution

The World Bank, Poverty and Inequality Platform (PIP), via Data360 (https://data360.worldbank.org/en/dataset/WB_PIP). Licence: CC0 1.0.

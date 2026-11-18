# World Bank WDI — Health and nutrition indicators for Mauritania

140 World Development Indicators series for Mauritania (3227 observations, 1960–2024) classified under health and nutrition.

| Field | Value |
|---|---|
| Category | `health` |
| Publisher | World Bank |
| Geographic coverage | National |
| Reference period | 1960–2024 |
| Source page | https://data360.worldbank.org/en/dataset/WB_WDI |
| Original download / API | https://data360api.worldbank.org/data360/data?DATABASE_ID=WB_WDI&REF_AREA=MRT |
| Licence | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
| Redistribution | `allowed` |
| Source last updated | Not stated |
| Retrieved | 2026-11-14 |

## Processing

Retrieved from the World Bank Data360 API (REF_AREA=MRT). Converted from JSON to CSV; observations with non-numeric values dropped; series without an explicit open licence in the Data360 metadata excluded (see `metadata/excluded-series.csv`). The wide file is a pivot of the long file (totals only).

## Files

- `wb_wdi_health_long.csv` — one row per indicator × disaggregation × period. Columns: `indicator_id` (Data360 ID), `indicator_code` (original World Bank series code), `indicator_name`, `unit`, `sex`/`age`/`urbanisation` (SDMX codes; `_T` = total, `_Z` = not applicable), `freq` (`A` = annual), `time_period`, `value`, `obs_status` (SDMX observation status; `A` = normal, `E` = estimated, `F` = forecast).
- `wb_wdi_health_wide.csv` — totals only (no sex/age/urban breakdown), annual, one column per `indicator_code`, one row per year.
- `indicators.csv` — indicator dictionary: name, unit, definition (when provided), original compiling source, licence, coverage.

Values are as published by the World Bank (no rescaling). Units are given per indicator in `unit`. Missing years are simply absent (no gap filling).

## Limitations

Many World Bank series for Mauritania are modelled or estimated by international agencies rather than reported by national statistical offices; check `obs_status` and the original source in `indicators.csv`. Coverage varies widely by indicator.

## Attribution

The World Bank, World Development Indicators (WDI), via Data360 (https://data360.worldbank.org/en/dataset/WB_WDI). Licence: CC BY 4.0.

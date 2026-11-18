# ILOSTAT — Labour force, employment, unemployment, underutilization, inactivity, working hours — Mauritania

586 ILOSTAT indicators (SDMX dataflows) for Mauritania, 337982 observations, 1977–2027, with breakdowns by sex, age, education, economic activity, occupation, area and other classifications where available.

| Field | Value |
|---|---|
| Category | `employment` |
| Publisher | International Labour Organization (ILO) — ILOSTAT |
| Geographic coverage | National (urban/rural where available) |
| Reference period | 1977–2027 |
| Source page | https://ilostat.ilo.org/data/ |
| Original download / API | https://sdmx.ilo.org/rest/data/ILO,{DATAFLOW}/MRT.... |
| Licence | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
| Redistribution | `allowed` |
| Source last updated | Not stated |
| Retrieved | 2026-11-14 |

## Processing

Each dataflow retrieved from the ILOSTAT SDMX REST API (REF_AREA = MRT) in SDMX-CSV 1.0 and concatenated. Columns are the SDMX columns (union across dataflows; empty where a dimension does not apply) plus `INDICATOR_LABEL` (dataflow name). `OBS_VALUE` parsed as number; codes unchanged. Stored as Parquet (zstd) because of its size.

## Files

- data file — one row per dataflow × dimension combination × period.
- `dataflows.csv` — list of included ILOSTAT dataflows with labels and row counts.

## Limitations

Mixes nationally reported survey data (e.g. ENESI / ENTE labour force surveys; see `SOURCE`) with ILO modelled estimates. Classification codes (e.g. `SEX_T`, `AGE_YTHADULT_YGE15`, `ECO_SECTOR_AGR`) follow ILOSTAT code lists — see https://ilostat.ilo.org/methods/.

## Notes

Licence: the ILO states that databases and datasets published from 3 May 2023 are covered by CC BY 4.0 (https://www.ilo.org/node/9321).

## Attribution

International Labour Organization. ILOSTAT database (https://ilostat.ilo.org/data/), accessed 2026-11-14. CC BY 4.0.

# Mauritania - Data on Conflict Events

This dataset is UCDP's most disaggregated dataset, covering individual events of organized violence (phenomena of lethal violence occurring at a given time and place). These events are sufficiently fine-grained to be geo-coded down to the level of individual villages, with temporal durations disaggregated to single, individual days. Sundberg, Ralph, and Erik Melander, 2013, “Introducing the UCDP Georeferenced Event Dataset”, Journal of Peace Research, vol.50, no.4, 523-532 Högbladh Stina, 2019, “UCDP GED Codebook version 19.1”, Department of Peace and Conflict Research, Uppsala University

| Field | Value |
|---|---|
| Category | `humanitarian` |
| Publisher | HDX |
| Geographic coverage | Mauritania |
| Reference period | 1989-01-01 to 2024-04-07 |
| Source page | https://data.humdata.org/dataset/ucdp-data-for-mauritania |
| Original download / API | https://data.humdata.org/dataset/1394c0da-e8af-4800-b017-7691e5c60b44/resource/eff049e8-bcb5-4ed2-8dcf-a571703ea0a2/download/conflict_data_mrt.csv |
| Licence | [CC BY 3.0 IGO](https://creativecommons.org/licenses/by/3.0/igo/) |
| Redistribution | `allowed` |
| Source last updated | 2026-03-01 |
| Retrieved | 2026-11-14 |

## Processing

Files downloaded unchanged from HDX resources. Many HDX CSVs contain a second header row of HXL hashtags (e.g. `#country+code`); it is kept as published — skip it when loading (e.g. `pandas.read_csv(path, skiprows=[1])`) if present.

## Original resources

- Conflict Data for Mauritania (CSV): https://data.humdata.org/dataset/1394c0da-e8af-4800-b017-7691e5c60b44/resource/eff049e8-bcb5-4ed2-8dcf-a571703ea0a2/download/conflict_data_mrt.csv

## Methodology (from the publisher)

UCDP's Methodology page contains information about how UCDP collects, evaluates, codes and validates event data.

## Attribution

HDX / Uppsala Conflict Data Program, via the Humanitarian Data Exchange (https://data.humdata.org/dataset/ucdp-data-for-mauritania). Licence: CC BY 3.0 IGO.

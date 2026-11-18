# Mauritania - Corruption Perceptions Index

This dataset contains Corruption Perceptions Index (CPI) scores and rankings for countries and territories, published by Transparency International. Scores range from 0 (highly corrupt) to 100 (very clean) and reflect perceived levels of public sector corruption based on assessments by experts and business executives. For more information, visit the Corruption Perceptions Index on the Transparency International website.

| Field | Value |
|---|---|
| Category | `governance` |
| Publisher | Transparency International |
| Geographic coverage | Mauritania |
| Reference period | 2012-01-01 to 2025-01-01 |
| Source page | https://data.humdata.org/dataset/mrt-corruption-perceptions-index |
| Original download / API | https://data.humdata.org/dataset/9be9b6e7-2e8c-4038-8e12-7fca3587a631/resource/38412b7f-6b6f-41dc-ac76-d35631b52010/download/mrt_cpi.csv |
| Licence | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
| Redistribution | `allowed` |
| Source last updated | 2026-05-21 |
| Retrieved | 2026-11-14 |

## Processing

Files downloaded unchanged from HDX resources. Many HDX CSVs contain a second header row of HXL hashtags (e.g. `#country+code`); it is kept as published — skip it when loading (e.g. `pandas.read_csv(path, skiprows=[1])`) if present.

## Original resources

- mrt_cpi.csv (CSV): https://data.humdata.org/dataset/9be9b6e7-2e8c-4038-8e12-7fca3587a631/resource/38412b7f-6b6f-41dc-ac76-d35631b52010/download/mrt_cpi.csv

## Methodology (from the publisher)

https://images.transparencycdn.org/images/CPI-2024-Methodology.zip

## Attribution

Transparency International, via the Humanitarian Data Exchange (https://data.humdata.org/dataset/mrt-corruption-perceptions-index). Licence: CC BY 4.0.

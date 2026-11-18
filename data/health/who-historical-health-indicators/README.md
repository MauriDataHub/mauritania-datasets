# Mauritania - Historical Health Indicators

This dataset contains historical data from WHO's data portal.

| Field | Value |
|---|---|
| Category | `health` |
| Publisher | World Health Organization |
| Geographic coverage | Mauritania |
| Reference period | 1961-01-01 to 2025-12-31 |
| Source page | https://data.humdata.org/dataset/who-historical-data-for-mrt |
| Original download / API | https://data.humdata.org/dataset/d6b8bf37-a337-4042-a5dd-515226d67dc0/resource/53d4991e-97f7-4016-a5a5-f7210a9c26c6/download/historical_health_indicators_mrt.csv |
| Licence | [CC BY-NC-SA 3.0 IGO](https://creativecommons.org/licenses/by-nc-sa/3.0/igo/) |
| Redistribution | `allowed` |
| Source last updated | 2024-06-27 |
| Retrieved | 2026-11-14 |

## Processing

Files downloaded unchanged from HDX resources. Many HDX CSVs contain a second header row of HXL hashtags (e.g. `#country+code`); it is kept as published — skip it when loading (e.g. `pandas.read_csv(path, skiprows=[1])`) if present.

## Original resources

- All Historical Health Indicators for Mauritania (CSV): https://data.humdata.org/dataset/d6b8bf37-a337-4042-a5dd-515226d67dc0/resource/53d4991e-97f7-4016-a5a5-f7210a9c26c6/download/historical_health_indicators_mrt.csv

## Licence conditions

Non-commercial use only; adaptations must be shared under the same licence.

## Methodology (from the publisher)

Registry

## Limitations

More details about the indicators are available in the links in the dataset description.

## Attribution

World Health Organization, via the Humanitarian Data Exchange (https://data.humdata.org/dataset/who-historical-data-for-mrt). Licence: CC BY-NC-SA 3.0 IGO.

# Relative Wealth Index

The Relative Wealth Index predicts the relative standard of living within countries using de-identified connectivity data, satellite imagery and other nontraditional data sources. The data is provided for 93 low and middle-income countries at 2.4km resolution. Please cite / attribute any use of this dataset using the following: Microestimates of wealth for all low- and middle-income countries Guanghua Chi, Han Fang, Sourav Chatterjee, Joshua E. […]

| Field | Value |
|---|---|
| Category | `poverty` |
| Publisher | AI for Good at Meta |
| Geographic coverage | Mauritania (subset of a multi-country dataset) |
| Reference period | 2021-04-01 to 2023-02-17 |
| Source page | https://data.humdata.org/dataset/relative-wealth-index |
| Original download / API | https://data.humdata.org/dataset/76f2a2ea-ba50-40f5-b79c-db95d668b843/resource/fc096a83-e3f6-4ed3-81cd-55959f7afb91/download/mrt_relative_wealth_index.csv |
| Licence | [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/) |
| Redistribution | `allowed` |
| Source last updated | 2026-05-11 |
| Retrieved | 2026-11-14 |

## Processing

Files downloaded unchanged from HDX resources. Many HDX CSVs contain a second header row of HXL hashtags (e.g. `#country+code`); it is kept as published — skip it when loading (e.g. `pandas.read_csv(path, skiprows=[1])`) if present.

## Original resources

- Mauritania_relative_wealth_index.csv (CSV): https://data.humdata.org/dataset/76f2a2ea-ba50-40f5-b79c-db95d668b843/resource/fc096a83-e3f6-4ed3-81cd-55959f7afb91/download/mrt_relative_wealth_index.csv

## Licence conditions

Non-commercial use only.

## Methodology (from the publisher)

Researchers at the University of California - Berkeley and Facebook developed micro-estimates of wealth and poverty that cover the populated surface of all 135 low and middle-income countries (LMICs) at 2.4km resolution. […]

## Limitations

Glide: EQ-2023-000015-TUR

## Attribution

AI for Good at Meta / Facebook, via the Humanitarian Data Exchange (https://data.humdata.org/dataset/relative-wealth-index). Licence: CC BY-NC 4.0.

# Mauritania Weekly FEWS NET Staple Food Price Data

Mauritania Weekly staple food price data collected by FEWS NET since 2002.

| Field | Value |
|---|---|
| Category | `food-security` |
| Publisher | FEWS NET |
| Geographic coverage | Mauritania |
| Reference period | 2002-01-31 onwards (ongoing series) |
| Source page | https://data.humdata.org/dataset/fewsnet_staple_food_price_data_for_mauritania_weekly_1506 |
| Original download / API | https://fdw.fews.net/api/marketpricefacts/?dataset=FEWS_NET_Staple_Food_Price_Data&country=MR&format=csv&fields=website&end_date |
| Licence | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
| Redistribution | `allowed` |
| Source last updated | 2026-03-28 |
| Retrieved | 2026-11-14 |

## Processing

Files downloaded unchanged from HDX resources. Many HDX CSVs contain a second header row of HXL hashtags (e.g. `#country+code`); it is kept as published — skip it when loading (e.g. `pandas.read_csv(path, skiprows=[1])`) if present.

## Original resources

- FEWS NET Staple Food Price Data for Mauritania (CSV): https://fdw.fews.net/api/marketpricefacts/?dataset=FEWS_NET_Staple_Food_Price_Data&country=MR&format=csv&fields=website&end_date

## Methodology (from the publisher)

The mean price for key commodities collected from multiple vendors in the selected markets, collected by FEWS NET enumerators on a regular schedule (typically monthly).

## Attribution

FEWS NET, via the Humanitarian Data Exchange (https://data.humdata.org/dataset/fewsnet_staple_food_price_data_for_mauritania_weekly_1506). Licence: CC BY 4.0.

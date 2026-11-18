# Mauritania: Rainfall Indicators at Subnational Level

This dataset contains dekadal rainfall indicators, computed from Climate Hazards Group InfraRed Precipitation satellite imagery with insitu Station data (CHIRPS) version 2 and the CHIRPS-GEFS short term rainfall forecasts, aggregated by subnational administrative units. Included indicators are (for each dekad): - 10 day rainfall [mm] (rfh) - rainfall 1-month rolling aggregation [mm] (r1h) - rainfall 3-month rolling aggregation [mm] (r3h) - rainfall long term average [mm] (rfhavg) - rainfall 1-month rolling aggregation long term average [mm] (r1havg) - rainfall 3-month rolling aggregation long term average [mm] (r3havg) - rainfall anomaly [%] (rfq) - rainfall 1-month anomaly [%] (r1q) - rainfall 3-month anomaly [%] (r3q) The administrative units used for aggregation are based on WFP data and contain a Pcode reference attributed to each unit. […]

| Field | Value |
|---|---|
| Category | `climate` |
| Publisher | WFP - World Food Programme |
| Geographic coverage | Mauritania |
| Reference period | 1981-01-01 to 2026-11-10 |
| Source page | https://data.humdata.org/dataset/mrt-rainfall-subnational |
| Licence | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
| Redistribution | `allowed` |
| Source last updated | 2026-11-13 |
| Retrieved | 2026-11-14 |

## Processing

Files downloaded unchanged from HDX resources. Many HDX CSVs contain a second header row of HXL hashtags (e.g. `#country+code`); it is kept as published — skip it when loading (e.g. `pandas.read_csv(path, skiprows=[1])`) if present.

## Original resources

- mrt-rainfall-subnat-full.csv (CSV): https://data.humdata.org/dataset/7680b3f0-aa0a-45b3-8fc7-ddc29efdccc7/resource/ebc25750-7082-4b85-bef7-83601c7fb64d/download/mrt-rainfall-subnat-full.csv
- mrt-rainfall-subnat-5ytd.csv (CSV): https://data.humdata.org/dataset/7680b3f0-aa0a-45b3-8fc7-ddc29efdccc7/resource/ac09e01b-66af-45f7-8728-33fa90faea24/download/mrt-rainfall-subnat-5ytd.csv

## Methodology (from the publisher)

Rainfall estimates are derived from satellite observations and combined with rain gauge data. For more information, please visit the CHIRPS product page. For information about the CHIRPS-GEFS short term forecasts, please visit the information page. […]

## Limitations

To provide real-time data, the prelim version is used which then gets replaced successively by final data as it becomes available. For more information about differences between prelim and final see CHIRPS Reality Checks. Forecast data is successively replaced by preliminary and final data.

## Attribution

WFP - World Food Programme / Climate Hazards Center UC Santa Barbara & WFP, via the Humanitarian Data Exchange (https://data.humdata.org/dataset/mrt-rainfall-subnational). Licence: CC BY 4.0.

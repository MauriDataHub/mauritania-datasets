# Mauritania: NDVI at Subnational Level

PLEASE NOTE: This dataset may experience infrequent updates due to irregularities in the supply of the underlying NASA MODIS source data. MODIS is expected to be decommissioned by the end of 2026, and this dataset may be discontinued. A possible replacement using NOAA VIIRS data is currently being explored. This dataset contains dekadal NDVI indicators computed from NASA's Moderate Resolution Imaging Spectroradiometer (MODIS) collection 6.1 from the Aqua and Terra satellite aggregated by sub-national administrative units. Included indicators are (for each dekad): - 10 day NDVI (vim) - NDVI long term average (vimlta) - 10 day NDVI anomaly [%] (viq) The administrative units used for aggregation are based on WFP data and contain a Pcode reference attributed to each unit. The number of input pixels used to create the aggregates, is provided in the npixelscolumn.

| Field | Value |
|---|---|
| Category | `environment` |
| Publisher | WFP - World Food Programme |
| Geographic coverage | Mauritania |
| Reference period | 2002-07-01 to 2026-11-10 |
| Source page | https://data.humdata.org/dataset/mrt-ndvi-subnational |
| Licence | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
| Redistribution | `allowed` |
| Source last updated | 2026-11-13 |
| Retrieved | 2026-11-14 |

## Processing

Files downloaded unchanged from HDX resources. Many HDX CSVs contain a second header row of HXL hashtags (e.g. `#country+code`); it is kept as published — skip it when loading (e.g. `pandas.read_csv(path, skiprows=[1])`) if present.

## Original resources

- mrt-ndvi-subnat-full.csv (CSV): https://data.humdata.org/dataset/3bf3db2e-522c-4ab6-b3dc-4a446195de03/resource/7845385a-0af4-4b15-9ea2-b8291ecf8b63/download/mrt-ndvi-subnat-full.csv
- mrt-ndvi-subnat-5ytd.csv (CSV): https://data.humdata.org/dataset/3bf3db2e-522c-4ab6-b3dc-4a446195de03/resource/fdc4b3e3-d148-4fad-859b-6fa8304e2369/download/mrt-ndvi-subnat-5ytd.csv

## Methodology (from the publisher)

The Normalized Difference Vegetation Index (NDVI) is obtained from combining the raw MODIS AQUA & TERRA 16 day composite products (MYD13C1 & MOD13C1) into 8 day synthetic product. This synthetic product is then filtered and gap-filled using a Whittaker filter with V-curve optimization to remove atmospheric noise and fill missing data. […]

## Limitations

Due to the nature of the Whittaker filter, the update of the timeseries (i.e. the addition of a new dekad) has an effect of preceding dekads which diminishes going back in time. Therefore slight variations can be expected for a certain number of dekads for every update.

## Attribution

WFP - World Food Programme / National Aeronautics and Space Administration (NASA) & WFP, via the Humanitarian Data Exchange (https://data.humdata.org/dataset/mrt-ndvi-subnational). Licence: CC BY 4.0.

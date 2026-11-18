# Sahel Crops Vegetation and Standardized Precipitation Index

Dataset containing information related to precipitation indices useful for analyzing and comparing variations in precipitation over time and across different geographical regions, alongside indices used in the analysis of vegetation and crops to monitor their activity and detect their presence in the territory. Key variables include the Atmospherically Resistant Vegetation Index (ARVI), Normalized Difference Vegetation Index (NDVI), Enhanced Vegetation Index (EVI), and Structure Insensitive Pigment Index (SIPI) for monitoring vegetation. For rainfall information, the Standardized Precipitation Index (SPI1, SPI3, SPI6, SPI9, and SPI12) is used, where SPI1 to SPI3 are indicators for immediate impacts and SPI6 to SPI12 measure medium-term impacts. […]

| Field | Value |
|---|---|
| Category | `agriculture` |
| Publisher | Acción Contra el hambre - GIS4tech |
| Geographic coverage | Mauritania (subset of a multi-country dataset) |
| Reference period | 2020-01-01 to 2026-10-01 |
| Source page | https://data.humdata.org/dataset/senegal-and-mauritania-crops-vegetation-and-standardized-precipitation-index |
| Original download / API | https://data.humdata.org/dataset/96564b62-dede-44a5-9a50-84c14f652c18/resource/254e4601-d19d-46bd-989a-2ea0e5a77e55/download/senegal-and-mauritania-crops-vegetation-and-standardized-precipitation-index.csv |
| Licence | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
| Redistribution | `allowed` |
| Source last updated | 2026-11-06 |
| Retrieved | 2026-11-14 |

## Processing

Files downloaded unchanged from HDX resources. Many HDX CSVs contain a second header row of HXL hashtags (e.g. `#country+code`); it is kept as published — skip it when loading (e.g. `pandas.read_csv(path, skiprows=[1])`) if present.

## Original resources

- Senegal-and-Mauritania-Crops-Vegetation-and-Standardized-Precipitation-Index.csv (CSV): https://data.humdata.org/dataset/96564b62-dede-44a5-9a50-84c14f652c18/resource/254e4601-d19d-46bd-989a-2ea0e5a77e55/download/senegal-and-mauritania-crops-vegetation-and-standardized-precipitation-index.csv

## Methodology (from the publisher)

The indices are derived from information reported by a series of satellites and stored in MODIS and CHIRPS. The satellites collect the information by land area, so that the result for each municipality is the median of the data over a period. […]

## Attribution

Acción Contra el hambre - GIS4tech / Acción contra el hambre - GIS4tech, via the Humanitarian Data Exchange (https://data.humdata.org/dataset/senegal-and-mauritania-crops-vegetation-and-standardized-precipitation-index). Licence: CC BY 4.0.

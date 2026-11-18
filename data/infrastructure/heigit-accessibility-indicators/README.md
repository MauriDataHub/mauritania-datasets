# Mauritania - Accessibility Indicators

This dataset provides insights into spatial accessibility to healthcare and education services across Mauritania. It has been created using free and open tools such as openrouteservice and open data sources, primarily OpenStreetMap (OSM). To assess accessibility to education and healthcare, we use travel-time isochrones—polygons representing areas reachable within a given time or distance by car. We overlay these isochrones with WorldPop population data, which provides 100m-resolution estimates. This allows us to calculate the population within time intervals from 10 to 120 minutes away from hospital services and distance intervals from 5 to 50 km away from schools. The unit of analysis is defined by geoboundaries country borders, and where available we also summarise results at finer administrative levels (ADM 1–4). Data Structure: - name: Region or country name. […]

| Field | Value |
|---|---|
| Category | `infrastructure` |
| Publisher | HeiGIT (Heidelberg Institute for Geoinformation Technology) |
| Geographic coverage | Mauritania |
| Reference period | 2026-02-25 to 2026-02-25 |
| Source page | https://data.humdata.org/dataset/mauritania-accessibility-indicators |
| Licence | [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) |
| Redistribution | `allowed` |
| Source last updated | 2026-02-25 |
| Retrieved | 2026-11-14 |

## Processing

Files downloaded unchanged from HDX resources. Many HDX CSVs contain a second header row of HXL hashtags (e.g. `#country+code`); it is kept as published — skip it when loading (e.g. `pandas.read_csv(path, skiprows=[1])`) if present.

## Original resources

- MRT_education_access_long.csv (CSV): https://hot.storage.heigit.org/heigit-hdx-public/access/mrt/MRT_education_access_long.csv
- MRT_education_access_wide.csv (CSV): https://hot.storage.heigit.org/heigit-hdx-public/access/mrt/MRT_education_access_wide.csv
- MRT_hospitals_access_long.csv (CSV): https://hot.storage.heigit.org/heigit-hdx-public/access/mrt/MRT_hospitals_access_long.csv
- MRT_hospitals_access_wide.csv (CSV): https://hot.storage.heigit.org/heigit-hdx-public/access/mrt/MRT_hospitals_access_wide.csv
- MRT_primary_healthcare_access_long.csv (CSV): https://hot.storage.heigit.org/heigit-hdx-public/access/mrt/MRT_primary_healthcare_access_long.csv
- MRT_primary_healthcare_access_wide.csv (CSV): https://hot.storage.heigit.org/heigit-hdx-public/access/mrt/MRT_primary_healthcare_access_wide.csv

## Licence conditions

Adaptations must be shared under the same licence.

## Methodology (from the publisher)

To assess accessibility to education and healthcare, we use travel-time isochrones—polygons representing areas reachable within a given time or distance by car. We overlay these isochrones with WorldPop population data, which provides 100m-resolution estimates. […]

## Limitations

OSM Completeness: This analysis relies on OpenStreetMap (OSM) data. While OSM is the most complete open map of the world, data quality varies significantly by region. In areas with unmapped roads or facilities, accessibility may be underestimated. Population Estimates: Population counts are derived from WorldPop top-down estimates (constrained). These are statistical models based on census projections and satellite imagery, not direct census counts, and may contain inaccuracies at the local pixel level. […]

## Attribution

HeiGIT (Heidelberg Institute for Geoinformation Technology) / HeiGIT, via the Humanitarian Data Exchange (https://data.humdata.org/dataset/mauritania-accessibility-indicators). Licence: CC BY-SA 4.0.

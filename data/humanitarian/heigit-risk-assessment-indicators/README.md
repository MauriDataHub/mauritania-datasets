# Mauritania - Risk Assessment Indicators

This dataset provides comprehensive Risk Assessment Indicators for Mauritania, aggregated at admin level 2 and can in particular be used to perform a structured risk assessment for flood and drought hazards. It includes demographic, environmental, infrastructure, accessibility, and hazard-related data to support disaster risk and resilience analysis. All layers are derived from HeiGIT’s GAIA Pipeline, integrating open data sources such as WorldPop, OpenStreetMap, and Google Earth Engine based on HDX COD-AB boundaries. […]

| Field | Value |
|---|---|
| Category | `humanitarian` |
| Publisher | HeiGIT (Heidelberg Institute for Geoinformation Technology) |
| Geographic coverage | Mauritania |
| Reference period | 2026-02-26 to 2026-08-27 |
| Source page | https://data.humdata.org/dataset/mauritania---risk-assessment-indicators |
| Licence | [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) |
| Redistribution | `allowed` |
| Source last updated | 2026-10-12 |
| Retrieved | 2026-11-14 |

## Processing

Files downloaded unchanged from HDX resources. Many HDX CSVs contain a second header row of HXL hashtags (e.g. `#country+code`); it is kept as published — skip it when loading (e.g. `pandas.read_csv(path, skiprows=[1])`) if present.

## Original resources

- MRT_ADM2_vulnerability.csv (CSV): https://hot.storage.heigit.org/heigit-hdx-public/risk_assessment_inputs/mrt/MRT_ADM2_vulnerability.csv
- MRT_ADM2_rural_population.csv (CSV): https://hot.storage.heigit.org/heigit-hdx-public/risk_assessment_inputs/mrt/MRT_ADM2_rural_population.csv
- MRT_ADM2_flood_exposure.csv (CSV): https://hot.storage.heigit.org/heigit-hdx-public/risk_assessment_inputs/mrt/MRT_ADM2_flood_exposure.csv
- MRT_ADM2_facilities.csv (CSV): https://hot.storage.heigit.org/heigit-hdx-public/risk_assessment_inputs/mrt/MRT_ADM2_facilities.csv
- MRT_ADM2_demographics.csv (CSV): https://hot.storage.heigit.org/heigit-hdx-public/risk_assessment_inputs/mrt/MRT_ADM2_demographics.csv
- MRT_ADM2_coping.csv (CSV): https://hot.storage.heigit.org/heigit-hdx-public/risk_assessment_inputs/mrt/MRT_ADM2_coping.csv
- MRT_ADM2_access.csv (CSV): https://hot.storage.heigit.org/heigit-hdx-public/risk_assessment_inputs/mrt/MRT_ADM2_access.csv
- MRT_ADM2_evacuability.csv (CSV): https://hot.storage.heigit.org/heigit-hdx-public/risk_assessment_inputs/mrt/MRT_ADM2_evacuability.csv
- MRT_ADM2_rai.csv (CSV): https://hot.storage.heigit.org/heigit-hdx-public/risk_assessment_inputs/mrt/MRT_ADM2_rai.csv

## Licence conditions

Adaptations must be shared under the same licence.

## Methodology (from the publisher)

This dataset aggregates multiple risk assessment indicators for the country.

## Attribution

HeiGIT (Heidelberg Institute for Geoinformation Technology) / Multiple sources, via the Humanitarian Data Exchange (https://data.humdata.org/dataset/mauritania---risk-assessment-indicators). Licence: CC BY-SA 4.0.

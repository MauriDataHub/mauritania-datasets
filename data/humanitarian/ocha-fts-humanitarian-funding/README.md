# Mauritania - Requirements and Funding Data

FTS publishes data on humanitarian funding flows as reported by donors and recipient organizations. It presents all humanitarian funding to a country and funding that is specifically reported or that can be specifically mapped against funding requirements stated in humanitarian response plans. The data comes from OCHA's Financial Tracking Service and is encoded as utf-8.

| Field | Value |
|---|---|
| Category | `humanitarian` |
| Publisher | OCHA Financial Tracking System (FTS) |
| Geographic coverage | Mauritania |
| Reference period | 2001-01-01 to 2026-11-13 |
| Source page | https://data.humdata.org/dataset/mrt-requirements-and-funding-data |
| Licence | [CC BY 3.0 IGO](https://creativecommons.org/licenses/by/3.0/igo/) |
| Redistribution | `allowed` |
| Source last updated | 2026-11-09 |
| Retrieved | 2026-11-14 |

## Processing

Files downloaded unchanged from HDX resources. Many HDX CSVs contain a second header row of HXL hashtags (e.g. `#country+code`); it is kept as published — skip it when loading (e.g. `pandas.read_csv(path, skiprows=[1])`) if present.

## Original resources

- fts_requirements_funding_mrt.csv (CSV): https://data.humdata.org/dataset/81cd063d-9559-4c4c-9ec1-b09ee64e0ddd/resource/a26d5078-5e61-485a-88a1-716519c3abd8/download/fts_requirements_funding_mrt.csv
- fts_requirements_funding_cluster_mrt.csv (CSV): https://data.humdata.org/dataset/81cd063d-9559-4c4c-9ec1-b09ee64e0ddd/resource/64b309f8-2075-487d-af11-2aae889c9908/download/fts_requirements_funding_cluster_mrt.csv
- fts_requirements_funding_globalcluster_mrt.csv (CSV): https://data.humdata.org/dataset/81cd063d-9559-4c4c-9ec1-b09ee64e0ddd/resource/f870c096-8bb9-4546-bc04-9660dae22c81/download/fts_requirements_funding_globalcluster_mrt.csv
- fts_incoming_funding_mrt.csv (CSV): https://data.humdata.org/dataset/81cd063d-9559-4c4c-9ec1-b09ee64e0ddd/resource/8bd4a67e-cacd-4518-80a6-afb3a79f9274/download/fts_incoming_funding_mrt.csv

## Methodology (from the publisher)

FTS is open to all government and private donors, funds, recipient agencies and implementing organizations wishing to report financial pledges and contributions for humanitarian action. FTS team curates the reported data by manually reviewing, validating and reconciling incoming information and updating FTS data records on an ongoing basis.

## Limitations

Please see About FTS

## Attribution

OCHA Financial Tracking System (FTS) / OCHA Financial Tracking Service, via the Humanitarian Data Exchange (https://data.humdata.org/dataset/mrt-requirements-and-funding-data). Licence: CC BY 3.0 IGO.

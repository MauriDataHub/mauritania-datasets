# Mauritania - GLIDE Disaster Events

GLIDEnumbers are GLobal unique IDEntifiers for Disasters. Each disaster is registered in a record that contains a GLIDEnumber that uniquely identifies it and allows information to be interoperable across multiple disaster information sources, both structured and textual. Accessing disaster information can be a time consuming and laborious task. Not only is data scattered but frequently identification of the disaster can be confusing in countries with many disaster events and across borders. To address both of these issues, Asian Disaster Reduction Center (ADRC) proposed a globally common Unique ID code for disasters. Among the institutions using actively GLIDEnumbers are UN-OCHA (ReliefWeb, FSCC, HDX), UNDRR, UNDP, WMO, IFRC, FAO, the European Commission and the Centre for Research on the Epidemiology of Disasters (CRED), among many others. […]

| Field | Value |
|---|---|
| Category | `humanitarian` |
| Publisher | GLIDE Initiative |
| Geographic coverage | Mauritania |
| Reference period | 2000-07-21 to 2025-01-28 |
| Source page | https://data.humdata.org/dataset/mrt-glide-events |
| Licence | [CC BY 3.0 IGO](https://creativecommons.org/licenses/by/3.0/igo/) |
| Redistribution | `allowed` |
| Source last updated | 2026-09-30 |
| Retrieved | 2026-11-14 |

## Processing

Files downloaded unchanged from HDX resources. Many HDX CSVs contain a second header row of HXL hashtags (e.g. `#country+code`); it is kept as published — skip it when loading (e.g. `pandas.read_csv(path, skiprows=[1])`) if present.

## Original resources

- mrt_glide_events.csv (CSV): https://data.humdata.org/dataset/09f37e6d-81e8-4359-88c4-bede22ad277e/resource/5645ee28-7991-4cf1-a7f6-bfdca2ebc680/download/mrt_glide_events.csv
- mrt_glide_events.geojson (GeoJSON): https://data.humdata.org/dataset/09f37e6d-81e8-4359-88c4-bede22ad277e/resource/5e8b9081-55d8-4127-bf87-9f6b06184e45/download/mrt_glide_events.geojson

## Methodology (from the publisher)

GLIDE (GLobal IDEntifier) numbers are unique identifiers for disasters. Each disaster event is registered with a GLIDEnumber that uniquely identifies it, enabling information to be interoperable across multiple disaster information sources, both structured and textual. […]

## Coordinate reference system

GeoJSON files use WGS 84 (EPSG:4326) longitude/latitude per RFC 7946 unless a `crs` member states otherwise. GeoPackage, shapefile and GeoTIFF files keep the CRS embedded by the publisher.

## Limitations

Indicators about loss and damage are optional and rarely entered/updated/reviewed, so they are not reliable. The data is collected every day, but individual country datasets are updated only if there are new events to report.

## Attribution

GLIDE Initiative, via the Humanitarian Data Exchange (https://data.humdata.org/dataset/mrt-glide-events). Licence: CC BY 3.0 IGO.

# Mauritania Healthsites

This dataset shows the list of operating health facilities. Attributes included: Name,Nature of Facility, Activities, Lat, Long

| Field | Value |
|---|---|
| Category | `health` |
| Publisher | Open Healthsite Consulting |
| Geographic coverage | Mauritania |
| Reference period | 2013-12-18 to 2026-09-11 |
| Source page | https://data.humdata.org/dataset/mauritania-healthsites |
| Licence | [ODbL 1.0](https://opendatacommons.org/licenses/odbl/1-0/) |
| Redistribution | `allowed` |
| Source last updated | 2026-09-29 |
| Retrieved | 2026-11-14 |

## Processing

Files downloaded unchanged from HDX resources. Many HDX CSVs contain a second header row of HXL hashtags (e.g. `#country+code`); it is kept as published — skip it when loading (e.g. `pandas.read_csv(path, skiprows=[1])`) if present.

## Original resources

- mauritania-healthsites-geojson (GeoJSON): https://data.humdata.org/dataset/5ce97948-669e-43fe-9101-ae693d4f236b/resource/26c25e04-b7ce-43ee-bd19-e01ca52fc837/download/mauritania.geojson
- mauritania-healthsites-csv (CSV): https://data.humdata.org/dataset/5ce97948-669e-43fe-9101-ae693d4f236b/resource/c3e8a74f-51a9-4901-a989-3f7798c26389/download/mauritania.csv

## Licence conditions

Share-alike for derived databases (Open Database License).

## Methodology (from the publisher)

Social Media and institutional sharing

## Coordinate reference system

GeoJSON files use WGS 84 (EPSG:4326) longitude/latitude per RFC 7946 unless a `crs` member states otherwise. GeoPackage, shapefile and GeoTIFF files keep the CRS embedded by the publisher.

## Limitations

Read the Healthsites concept note http://bit.ly/2ocL2KY

## Attribution

Open Healthsite Consulting / OpenStreetMap contributors, via the Humanitarian Data Exchange (https://data.humdata.org/dataset/mauritania-healthsites). Licence: ODbL 1.0.

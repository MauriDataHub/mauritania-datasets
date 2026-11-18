# FEWS NET — Acute food insecurity classification maps for Mauritania (IPC-compatible, 2011–2024)

83 GeoJSON layers of FEWS NET acute food insecurity classifications for Mauritania (current situation `CS` and near/medium-term projections `ML1`/`ML2`), consolidated from the individual periodic FEWS NET datasets on HDX. Each feature carries the IPC phase (`value`, 1–5), scenario, projection dates and classification scale.

| Field | Value |
|---|---|
| Category | `food-security` |
| Publisher | Famine Early Warning Systems Network (FEWS NET) |
| Geographic coverage | National (livelihood/administrative units) |
| Reference period | 2011-01-01 to 2024-10-01 |
| Source page | https://data.humdata.org/organization/fewsnet |
| Licence | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
| Redistribution | `allowed` |
| Source last updated | Not stated |
| Retrieved | 2026-11-14 |

## Processing

Downloaded the GeoJSON resource of each of 77 FEWS NET Mauritania classification datasets on HDX; files unchanged. `index.csv` maps every file to its HDX dataset and resource URL.

## Coordinate reference system

WGS 84 (EPSG:4326) per RFC 7946 (no `crs` member in the files).

## Limitations

FEWS NET classifications are analytical judgements; projected (`ML1`/`ML2`) layers are forecasts. Unit geometries change between analyses.

## Attribution

FEWS NET, via the Humanitarian Data Exchange. CC BY 4.0.

# OurAirports — Airports and runways in Mauritania

List of 34 airports, airstrips and heliports in Mauritania (ISO country MR) with ICAO/IATA codes, type, coordinates and elevation, plus their runways.

| Field | Value |
|---|---|
| Category | `transport` |
| Publisher | OurAirports |
| Geographic coverage | National (point locations) |
| Reference period | Snapshot retrieved 2026-11-14 |
| Source page | https://ourairports.com/countries/MR/ |
| Original download / API | https://davidmegginson.github.io/ourairports-data/airports.csv |
| Licence | Public Domain |
| Redistribution | `allowed` |
| Source last updated | Not stated |
| Retrieved | 2026-11-14 |

## Processing

Filtered the global `airports.csv` to `iso_country` = MR and `runways.csv` to the matching `airport_ident` values. Columns unchanged.

## Limitations

Crowd-sourced; includes closed and minor airstrips (see `type`). Coordinates are decimal degrees WGS 84.

## Attribution

OurAirports (https://ourairports.com), data released to the public domain.

# NASA POWER — Monthly climate series for the 13 regional capitals of Mauritania (1981–2024)

Monthly air temperature (mean/max/min at 2 m), corrected precipitation, relative humidity, wind speed at 2 m and surface solar irradiance from NASA POWER (MERRA-2 / satellite-derived) for 13 point locations: the capitals of every wilaya (Nouakchott represents the three Nouakchott wilayas).

| Field | Value |
|---|---|
| Category | `climate` |
| Publisher | NASA Langley Research Center — POWER Project |
| Geographic coverage | Point locations (regional capitals) |
| Reference period | 1981–2024 |
| Source page | https://power.larc.nasa.gov/ |
| Original download / API | https://power.larc.nasa.gov/api/temporal/monthly/point?parameters=T2M,T2M_MAX,T2M_MIN,PRECTOTCORR,RH2M,WS2M,ALLSKY_SFC_SW_DWN&community=AG&longitude=-15.9780071&latitude=18.0792379&start=1981&end=2024&format=JSON |
| Licence | [NASA open data (no restrictions; attribution requested)](https://power.larc.nasa.gov/docs/referencing/) |
| Redistribution | `allowed` |
| Source last updated | Not stated |
| Retrieved | 2026-11-14 |

## Processing

Queried the POWER monthly point API (community AG) once per location. JSON converted to a long CSV (one row per city × parameter × year × month). Point coordinates are those of the city nodes in OpenStreetMap (HOT export, dataset `osm-populated-places`).

## Files

- `power_monthly_long.csv` — columns `city`, `wilaya`, `longitude`, `latitude`, `year`, `month`, `parameter`, `value`.
- `parameters.csv` — parameter names and units.
- `locations.csv` — points queried.

## Limitations

Values are modelled/reanalysis estimates for the grid cell, not station observations. Month 13 is the annual aggregate supplied by the API. 507 values equal the POWER fill value -999 (missing).

## Attribution

These data were obtained from the NASA Langley Research Center (LaRC) POWER Project funded through the NASA Earth Science/Applied Science Program (https://power.larc.nasa.gov/), monthly API, accessed 2026-11-14.

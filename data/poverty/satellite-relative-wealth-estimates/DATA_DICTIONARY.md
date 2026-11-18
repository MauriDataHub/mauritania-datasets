# Data dictionary - satellite-derived relative wealth estimates (23 sub-Saharan African countries)

Field definitions for the files deposited in the Zenodo community **enerverge_rwi** (CC-BY-4.0). Machine-readable form: `data_dictionary.csv`. This file lets the dataset be used without the accompanying Data Descriptor; for methods and validation see the paper.

## File manifest (per country record)

| File | Contents |
|---|---|
| `{country}_feature_panel.parquet` | Harmonised per-H3-9 annual feature panel (the model input): one row per H3-9 cell per year, all predictor columns below. |
| `{country}_rwi_h3_9.parquet` | Relative wealth estimates at H3 resolution 9 (~0.1 km2). |
| `{country}_rwi_h3_8.parquet` | Relative wealth estimates at H3 resolution 8 (~0.7 km2). |
| `{country}_rwi_h3_7.parquet` | Relative wealth estimates at H3 resolution 7 (~5 km2). |
| `{country}_rwi_adm3.parquet` | Relative wealth estimates at administrative level 3 (ward). |
| `{country}_rwi_adm2.parquet` | Relative wealth estimates at administrative level 2 (LGA / district). |
| `{country}_rwi_adm1.parquet` | Relative wealth estimates at administrative level 1 (state / region). |

Coordinate reference system: **WGS84 (EPSG:4326)**. Estimates are **within-country standardised** (mean 0, unit variance per country-year); compare across units within a country, not raw across countries. Nulls: a feature is null before its first-populated year and outside its covered cells (see coverage in the Descriptor Suppl. Table S2).

## Relative wealth estimate files - schema

| Field | Type | Definition | Permitted values |
|---|---|---|---|
| `unit_id` | string | H3 index (h3_8 / h3_9) or administrative code (state_code / lga_id / ward_id) | n/a |
| `year` | int | Year to which the estimate applies | 2017-2025 |
| `rwi_xgb` | float | Primary relative wealth, gradient-boosted (XGBoost); within-country standardised | continuous |
| `rwi_lasso` | float | Interpretable linear estimate (lasso family: lassools / lassoridge); within-country standardised | continuous |
| `pi_lower` | float | Lower bound of the split-conformal prediction interval | continuous |
| `pi_upper` | float | Upper bound of the split-conformal prediction interval | continuous |
| `provenance` | string | How the estimate was produced | survey_anchored / transfer_backward / transfer_forward / transfer_interpolated |
| `validated` | bool | Whether the unit lies within an externally validated grain | true / false |

## Feature panel - schema (168 columns)

Note: Nigeria's feature panel additionally carries experimental OSM POI-count columns (`osm_buckets_*` / `osm_local_*`) that were built for Nigeria only and were not used in the released estimates; they are intentionally omitted from this dictionary.

### Target

| Field | Description | Units |
|---|---|---|
| `y` | DHS asset wealth index for the anchor cluster/unit; the prediction target (within-survey standardised) | z-score |

### Index

| Field | Description | Units |
|---|---|---|
| `meta` | Row metadata key (internal join key) | - |
| `pop` | Population count used as the aggregation / accuracy weight | persons |
| `lat` | Unit centroid latitude (WGS84) | degrees |
| `lon` | Unit centroid longitude (WGS84) | degrees |
| `adm1` | Admin-1 (state / region) identifier | - |
| `urb` | Urban indicator for the unit | 0/1 |
| `nc` | Number of contributing child cells aggregated into the unit | count |
| `country` | Country name | - |
| `grain` | Spatial grain label (cluster / h3_8 / h3_7 / adm3 / adm2 / adm1) | - |
| `adm_name` | Administrative unit name | - |

### Nighttime lights (EOG VIIRS)

| Field | Description | Units |
|---|---|---|
| `eog_avg_ctr` | EOG VIIRS nighttime-lights average radiance (avg ctr) | nW/cm2/sr |
| `eog_avg_3x3_mean` | EOG VIIRS nighttime-lights average radiance (avg 3x3 mean) | nW/cm2/sr |
| `eog_avg_3x3_std` | EOG VIIRS nighttime-lights average radiance (avg 3x3 std) | nW/cm2/sr |
| `eog_avg_3x3_max` | EOG VIIRS nighttime-lights average radiance (avg 3x3 max) | nW/cm2/sr |
| `eog_avg_5x5_mean` | EOG VIIRS nighttime-lights average radiance (avg 5x5 mean) | nW/cm2/sr |
| `eog_avg_5x5_max` | EOG VIIRS nighttime-lights average radiance (avg 5x5 max) | nW/cm2/sr |
| `eog_avg_5x5_p90` | EOG VIIRS nighttime-lights average radiance (avg 5x5 p90) | nW/cm2/sr |
| `eog_avg_5x5_p10` | EOG VIIRS nighttime-lights average radiance (avg 5x5 p10) | nW/cm2/sr |
| `eog_med_ctr` | EOG VIIRS nighttime-lights median radiance (med ctr) | nW/cm2/sr |
| `eog_med_3x3_mean` | EOG VIIRS nighttime-lights median radiance (med 3x3 mean) | nW/cm2/sr |
| `eog_med_3x3_std` | EOG VIIRS nighttime-lights median radiance (med 3x3 std) | nW/cm2/sr |
| `eog_med_3x3_max` | EOG VIIRS nighttime-lights median radiance (med 3x3 max) | nW/cm2/sr |
| `eog_med_5x5_mean` | EOG VIIRS nighttime-lights median radiance (med 5x5 mean) | nW/cm2/sr |
| `eog_med_5x5_max` | EOG VIIRS nighttime-lights median radiance (med 5x5 max) | nW/cm2/sr |
| `eog_med_5x5_p90` | EOG VIIRS nighttime-lights median radiance (med 5x5 p90) | nW/cm2/sr |
| `eog_med_5x5_p10` | EOG VIIRS nighttime-lights median radiance (med 5x5 p10) | nW/cm2/sr |

### Optical / vegetation (Sentinel-2)

| Field | Description | Units |
|---|---|---|
| `ndvi_mean` | NDVI (vegetation), annual mean over the annual (Feb/May/Aug/Nov) composite | index |
| `ndvi_median` | NDVI (vegetation), annual median over the annual (Feb/May/Aug/Nov) composite | index |
| `ndvi_std` | NDVI (vegetation), annual std. dev. over the annual (Feb/May/Aug/Nov) composite | index |
| `ndvi_p10` | NDVI (vegetation), annual 10th percentile over the annual (Feb/May/Aug/Nov) composite | index |
| `ndvi_p90` | NDVI (vegetation), annual 90th percentile over the annual (Feb/May/Aug/Nov) composite | index |
| `ndbi_mean` | NDBI (built-up), annual mean over the annual (Feb/May/Aug/Nov) composite | index |
| `ndbi_median` | NDBI (built-up), annual median over the annual (Feb/May/Aug/Nov) composite | index |
| `ndbi_std` | NDBI (built-up), annual std. dev. over the annual (Feb/May/Aug/Nov) composite | index |
| `ndbi_p10` | NDBI (built-up), annual 10th percentile over the annual (Feb/May/Aug/Nov) composite | index |
| `ndbi_p90` | NDBI (built-up), annual 90th percentile over the annual (Feb/May/Aug/Nov) composite | index |
| `ndwi_mean` | NDWI (open water), annual mean over the annual (Feb/May/Aug/Nov) composite | index |
| `ndwi_median` | NDWI (open water), annual median over the annual (Feb/May/Aug/Nov) composite | index |
| `ndwi_std` | NDWI (open water), annual std. dev. over the annual (Feb/May/Aug/Nov) composite | index |
| `ndwi_p10` | NDWI (open water), annual 10th percentile over the annual (Feb/May/Aug/Nov) composite | index |
| `ndwi_p90` | NDWI (open water), annual 90th percentile over the annual (Feb/May/Aug/Nov) composite | index |
| `mndwi_mean` | MNDWI (modified water), annual mean over the annual (Feb/May/Aug/Nov) composite | index |
| `mndwi_median` | MNDWI (modified water), annual median over the annual (Feb/May/Aug/Nov) composite | index |
| `mndwi_std` | MNDWI (modified water), annual std. dev. over the annual (Feb/May/Aug/Nov) composite | index |
| `mndwi_p10` | MNDWI (modified water), annual 10th percentile over the annual (Feb/May/Aug/Nov) composite | index |
| `mndwi_p90` | MNDWI (modified water), annual 90th percentile over the annual (Feb/May/Aug/Nov) composite | index |
| `ndmi_mean` | NDMI (moisture), annual mean over the annual (Feb/May/Aug/Nov) composite | index |
| `ndmi_median` | NDMI (moisture), annual median over the annual (Feb/May/Aug/Nov) composite | index |
| `ndmi_std` | NDMI (moisture), annual std. dev. over the annual (Feb/May/Aug/Nov) composite | index |
| `ndmi_p10` | NDMI (moisture), annual 10th percentile over the annual (Feb/May/Aug/Nov) composite | index |
| `ndmi_p90` | NDMI (moisture), annual 90th percentile over the annual (Feb/May/Aug/Nov) composite | index |
| `bsi_mean` | BSI (bare soil), annual mean over the annual (Feb/May/Aug/Nov) composite | index |
| `bsi_median` | BSI (bare soil), annual median over the annual (Feb/May/Aug/Nov) composite | index |
| `bsi_std` | BSI (bare soil), annual std. dev. over the annual (Feb/May/Aug/Nov) composite | index |
| `bsi_p10` | BSI (bare soil), annual 10th percentile over the annual (Feb/May/Aug/Nov) composite | index |
| `bsi_p90` | BSI (bare soil), annual 90th percentile over the annual (Feb/May/Aug/Nov) composite | index |
| `baei_median` | BAEI (built-up area extraction), annual median over the annual (Feb/May/Aug/Nov) composite | index |
| `baei_mean` | BAEI (built-up area extraction), annual mean over the annual (Feb/May/Aug/Nov) composite | index |
| `baei_std` | BAEI (built-up area extraction), annual std. dev. over the annual (Feb/May/Aug/Nov) composite | index |
| `baei_p10` | BAEI (built-up area extraction), annual 10th percentile over the annual (Feb/May/Aug/Nov) composite | index |
| `baei_p90` | BAEI (built-up area extraction), annual 90th percentile over the annual (Feb/May/Aug/Nov) composite | index |
| `ui_median` | UI (urban index), annual median over the annual (Feb/May/Aug/Nov) composite | index |
| `ui_mean` | UI (urban index), annual mean over the annual (Feb/May/Aug/Nov) composite | index |
| `ui_std` | UI (urban index), annual std. dev. over the annual (Feb/May/Aug/Nov) composite | index |
| `ui_p10` | UI (urban index), annual 10th percentile over the annual (Feb/May/Aug/Nov) composite | index |
| `ui_p90` | UI (urban index), annual 90th percentile over the annual (Feb/May/Aug/Nov) composite | index |
| `evi_median` | EVI (enhanced vegetation), annual median over the annual (Feb/May/Aug/Nov) composite | index |
| `evi_mean` | EVI (enhanced vegetation), annual mean over the annual (Feb/May/Aug/Nov) composite | index |
| `evi_std` | EVI (enhanced vegetation), annual std. dev. over the annual (Feb/May/Aug/Nov) composite | index |
| `evi_p10` | EVI (enhanced vegetation), annual 10th percentile over the annual (Feb/May/Aug/Nov) composite | index |
| `evi_p90` | EVI (enhanced vegetation), annual 90th percentile over the annual (Feb/May/Aug/Nov) composite | index |

### SAR backscatter (Sentinel-1)

| Field | Description | Units |
|---|---|---|
| `vv_med_db` | Sentinel-1 VV C-band backscatter, med | dB |
| `vv_mean_db` | Sentinel-1 VV C-band backscatter, annual mean | dB |
| `vv_std_db` | Sentinel-1 VV C-band backscatter, annual std. dev. | dB |
| `vv_p10_db` | Sentinel-1 VV C-band backscatter, annual 10th percentile | dB |
| `vv_p90_db` | Sentinel-1 VV C-band backscatter, annual 90th percentile | dB |
| `vh_med_db` | Sentinel-1 VH C-band backscatter, med | dB |
| `vh_mean_db` | Sentinel-1 VH C-band backscatter, annual mean | dB |
| `vh_std_db` | Sentinel-1 VH C-band backscatter, annual std. dev. | dB |
| `vh_p10_db` | Sentinel-1 VH C-band backscatter, annual 10th percentile | dB |
| `vh_p90_db` | Sentinel-1 VH C-band backscatter, annual 90th percentile | dB |
| `vv_minus_vh_med_db` | Sentinel-1 VV-VH C-band backscatter, med | dB |
| `vv_minus_vh_std_db` | Sentinel-1 VV-VH C-band backscatter, annual std. dev. | dB |
| `vv_minus_vh_p10_db` | Sentinel-1 VV-VH C-band backscatter, annual 10th percentile | dB |
| `vv_minus_vh_p90_db` | Sentinel-1 VV-VH C-band backscatter, annual 90th percentile | dB |
| `vv_minus_vh_mean_db` | Sentinel-1 VV-VH C-band backscatter, annual mean | dB |
| `vvminusvh_mean_db` | Sentinel-1 VV-VH C-band backscatter, annual mean | dB |
| `vvminusvh_std_db` | Sentinel-1 VV-VH C-band backscatter, annual std. dev. | dB |
| `vvminusvh_p10_db` | Sentinel-1 VV-VH C-band backscatter, annual 10th percentile | dB |
| `vvminusvh_p90_db` | Sentinel-1 VV-VH C-band backscatter, annual 90th percentile | dB |

### Atmospheric (Sentinel-5P)

| Field | Description | Units |
|---|---|---|
| `no2_mean_mol_m2` | Sentinel-5P TROPOMI NO2 column, annual mean | mol/m2 |
| `no2_p10_umol_m2` | Sentinel-5P TROPOMI NO2 column, annual 10th percentile | umol/m2 |
| `no2_p90_umol_m2` | Sentinel-5P TROPOMI NO2 column, annual 90th percentile | umol/m2 |
| `no2_std_umol_m2` | Sentinel-5P TROPOMI NO2 column, annual std. dev. | umol/m2 |
| `aerosol_index_mean` | Sentinel-5P TROPOMI aerosol index column, annual mean | index |
| `aerosol_index_p10` | Sentinel-5P TROPOMI aerosol index column, annual 10th percentile | index |
| `aerosol_index_p90` | Sentinel-5P TROPOMI aerosol index column, annual 90th percentile | index |
| `aerosol_index_std` | Sentinel-5P TROPOMI aerosol index column, annual std. dev. | index |
| `co_mean_mmol_m2` | Sentinel-5P TROPOMI CO column, annual mean | mmol/m2 |
| `co_p10_mmol_m2` | Sentinel-5P TROPOMI CO column, annual 10th percentile | mmol/m2 |
| `co_p90_mmol_m2` | Sentinel-5P TROPOMI CO column, annual 90th percentile | mmol/m2 |
| `co_std_mmol_m2` | Sentinel-5P TROPOMI CO column, annual std. dev. | mmol/m2 |
| `ch4_mean_ppb` | Sentinel-5P TROPOMI CH4 (methane) column, annual mean | ppb |
| `ch4_p10_ppb` | Sentinel-5P TROPOMI CH4 (methane) column, annual 10th percentile | ppb |
| `ch4_p90_ppb` | Sentinel-5P TROPOMI CH4 (methane) column, annual 90th percentile | ppb |
| `ch4_std_ppb` | Sentinel-5P TROPOMI CH4 (methane) column, annual std. dev. | ppb |
| `no2_p10_mol_m2` | Sentinel-5P TROPOMI NO2 column, annual 10th percentile | mol/m2 |
| `no2_p90_mol_m2` | Sentinel-5P TROPOMI NO2 column, annual 90th percentile | mol/m2 |
| `no2_std_mol_m2` | Sentinel-5P TROPOMI NO2 column, annual std. dev. | mol/m2 |
| `co_n_swaths` | Sentinel-5P TROPOMI CO column, n | index |
| `ch4_n_swaths` | Sentinel-5P TROPOMI CH4 (methane) column, n | index |

### Climate / thermal comfort (UTCI)

| Field | Description | Units |
|---|---|---|
| `utci_mean_diurnal_range_c` | Universal Thermal Climate Index: mean diurnal range c | degC |
| `utci_mean_hours_over_38` | Universal Thermal Climate Index: mean hours over 38 | hours |
| `utci_mean_peak_hour` | Universal Thermal Climate Index: mean peak hour | hour |
| `utci_summer_mean_c` | Universal Thermal Climate Index: summer mean c | degC |
| `utci_dry_season_mean_c` | Universal Thermal Climate Index: dry season mean c | degC |

### Precipitation (CHIRPS)

| Field | Description | Units |
|---|---|---|
| `chirps_anomaly_pct` | CHIRPS precipitation: anomaly pct | % |
| `chirps_cv` | CHIRPS precipitation: cv | - |

### Land-surface productivity (MODIS)

| Field | Description | Units |
|---|---|---|
| `modis_gpp` | MODIS annual gross primary productivity | product units |
| `modis_npp` | MODIS annual net primary productivity | product units |
| `modis_et` | MODIS annual evapotranspiration | product units |
| `modis_pet` | MODIS annual potential evapotranspiration | product units |

### Wildfire (MODIS/FIRMS)

| Field | Description | Units |
|---|---|---|
| `wildfire_pct_combined` | MODIS/FIRMS burned area: pct combined | - |
| `wildfire_burn_months` | MODIS/FIRMS burned area: burn months | - |
| `wildfire_burn_doy` | MODIS/FIRMS burned area: burn doy | - |

### Built environment (OSM)

| Field | Description | Units |
|---|---|---|
| `osm_residential_lu_new` | OpenStreetMap: residential lu newly mapped during the year | count |
| `osm_healthcare_new` | OpenStreetMap: healthcare newly mapped during the year | count |
| `osm_buildings_new` | OpenStreetMap: buildings newly mapped during the year | count |
| `osm_religious_new` | OpenStreetMap: religious newly mapped during the year | count |
| `osm_amenities_new` | OpenStreetMap: amenities newly mapped during the year | count |
| `osm_education_new` | OpenStreetMap: education newly mapped during the year | count |
| `osm_shops_new` | OpenStreetMap: shops newly mapped during the year | count |
| `osm_offices_new` | OpenStreetMap: offices newly mapped during the year | count |
| `osm_commercial_lu_new` | OpenStreetMap: commercial lu newly mapped during the year | count |
| `osm_industrial_new` | OpenStreetMap: industrial newly mapped during the year | count |
| `osm_residential_lu_cum` | OpenStreetMap: cumulative count of residential lu to date | count |
| `osm_healthcare_cum` | OpenStreetMap: cumulative count of healthcare to date | count |
| `osm_buildings_cum` | OpenStreetMap: cumulative count of buildings to date | count |
| `osm_religious_cum` | OpenStreetMap: cumulative count of religious to date | count |
| `osm_amenities_cum` | OpenStreetMap: cumulative count of amenities to date | count |
| `osm_education_cum` | OpenStreetMap: cumulative count of education to date | count |
| `osm_shops_cum` | OpenStreetMap: cumulative count of shops to date | count |
| `osm_offices_cum` | OpenStreetMap: cumulative count of offices to date | count |
| `osm_commercial_lu_cum` | OpenStreetMap: cumulative count of commercial lu to date | count |
| `osm_industrial_cum` | OpenStreetMap: cumulative count of industrial to date | count |

### Mobile connectivity (Ookla)

| Field | Description | Units |
|---|---|---|
| `ookla_dl_mbps` | Ookla Open Data mobile network: dl mbps | Mbps |
| `ookla_ul_mbps` | Ookla Open Data mobile network: ul mbps | Mbps |
| `ookla_lat_ms` | Ookla Open Data mobile network: lat ms | ms |
| `ookla_tests` | Ookla Open Data mobile network: tests | - |
| `ookla_device_quarters` | Ookla Open Data mobile network: device quarters | - |
| `ookla_n_quarters` | Ookla Open Data mobile network: n quarters | - |

### Cell towers (OpenCellID)

| Field | Description | Units |
|---|---|---|
| `towers_cum` | Cell-tower panel: towers cum | count/share |
| `towers_new` | Cell-tower panel: towers new | count/share |
| `gsm_cum` | Cell-tower panel: gsm cum | count/share |
| `umts_cum` | Cell-tower panel: umts cum | count/share |
| `towers_alive` | Cell-tower panel: towers alive | count/share |
| `towers_new_in_year` | Cell-tower panel: towers new in year | count/share |
| `lte_share` | Cell-tower panel: lte share | count/share |
| `gsm_share` | Cell-tower panel: gsm share | count/share |
| `median_samples` | Cell-tower panel: median samples | count/share |

### Conflict (ACLED)

| Field | Description | Units |
|---|---|---|
| `n_events` | ACLED conflict: n events (unit-year) | count |
| `n_fatalities` | ACLED conflict: n fatalities (unit-year) | count |
| `n_unique_actors` | ACLED conflict: n unique actors (unit-year) | count |
| `n_violence_civilians` | ACLED conflict: n violence civilians (unit-year) | count |
| `n_protests` | ACLED conflict: n protests (unit-year) | count |
| `n_battles` | ACLED conflict: n battles (unit-year) | count |
| `n_months` | ACLED conflict: n months (unit-year) | count |

# Mauritania - National Demographic and Health Data

Contains data from the DHS data portal. There is also a dataset containing Mauritania - Subnational Demographic and Health Data on HDX. The DHS Program Application Programming Interface (API) provides software developers access to aggregated indicator data from The Demographic and Health Surveys (DHS) Program. The API can be used to create various applications to help analyze, visualize, explore and disseminate data on population, health, HIV, and nutrition from more than 90 countries.

| Field | Value |
|---|---|
| Category | `health` |
| Publisher | The DHS Program |
| Geographic coverage | Mauritania |
| Reference period | 2000-01-01 to 2020-12-31 |
| Source page | https://data.humdata.org/dataset/dhs-data-for-mauritania |
| Licence | [CC BY-ND 4.0](https://creativecommons.org/licenses/by-nd/4.0/) |
| Redistribution | `allowed` |
| Source last updated | 2026-07-31 |
| Retrieved | 2026-11-14 |

## Processing

Files downloaded unchanged from HDX resources. Many HDX CSVs contain a second header row of HXL hashtags (e.g. `#country+code`); it is kept as published — skip it when loading (e.g. `pandas.read_csv(path, skiprows=[1])`) if present.

## Original resources

- DHS Quickstats Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/298f0acb-6261-495f-816a-e609e4173f87/download/dhs-quickstats_national_mrt.csv
- DHS Mobile Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/21ef0418-f435-4808-b579-576e86050c55/download/dhs-mobile_national_mrt.csv
- SDGs Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/e3bb3f96-465d-49bc-ad24-8e1463f674a6/download/sdgs_national_mrt.csv
- MDGs Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/a5bc7e1c-64b2-44b2-8656-96aed1f50534/download/mdgs_national_mrt.csv
- PMI/RBM Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/8f452dea-a7f0-4bf0-948d-3a8dd57d0864/download/rbm_national_mrt.csv
- IYCF Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/67cf590c-6720-4162-bc30-075ba7488a04/download/iycf_national_mrt.csv
- MICS indicators Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/91fe47a4-a307-4c5d-878a-679865626210/download/mics-indicators_national_mrt.csv
- FP2020 Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/68817cb9-6f26-4868-a44b-b3bb8418afed/download/fp2020_national_mrt.csv
- Access to Health Care Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/d755af17-2c82-456c-a6d8-0a8dbfb5d550/download/access-to-health-care_national_mrt.csv
- Adult Mortality Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/4476bd39-03ea-4c60-a8af-eda0c2f34fc9/download/adult-mortality_national_mrt.csv
- Anthropometry Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/1af0aef9-4e29-4acb-83e2-2fbc156956a1/download/anthropometry_national_mrt.csv
- Child Mortality Rates Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/62dd7f61-fd00-47eb-b41c-54ca8fda6650/download/child-mortality-rates_national_mrt.csv
- Diarrhea Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/019102be-3735-48db-8b1b-9ed210e2914b/download/diarrhea_national_mrt.csv
- Fertility Rates Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/2c13dc72-7823-4238-8b68-89d1e9686977/download/fertility-rates_national_mrt.csv
- HIV Behavior Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/6be5cf69-4072-47e6-8ee3-817194b2c683/download/hiv-behavior_national_mrt.csv
- Immunization Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/f748d91c-6ed6-4046-b63c-13b248259dba/download/immunization_national_mrt.csv
- Maternal Mortality Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/0e8e6a79-dd17-4d47-88b5-d64782ff9c1c/download/maternal-mortality_national_mrt.csv
- Men's Fertility and Family Planning Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/c52eae8b-b28d-4877-b6be-9dcb5cf97fb5/download/mens-fertility-and-family-planning_national_mrt.csv
- Orphans Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/cd3cd104-0e9d-412c-8637-b3188ddbdae7/download/orphans_national_mrt.csv
- Symptoms of acute respiratory infection (ARI) Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/1014adf5-5d7e-45ff-91a3-805cdd2d8e33/download/symptoms-of-acute-respiratory-infection-ari_national_mrt.csv
- Sexual Intercourse Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/0ebc0da2-316c-4964-b812-dc4aefd87f8d/download/sexual-intercourse_national_mrt.csv
- Toilet Facilities Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/0636cc4c-2a86-4ac2-bc5c-8cc44275a6e1/download/toilet-facilities_national_mrt.csv
- Water Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/d3b2ea8b-88ac-4f8a-b80e-aa653f731c41/download/water_national_mrt.csv
- Select Gender Indicators Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/15995bba-425f-4b8b-b6cf-28388e68942f/download/select-gender-indicators_national_mrt.csv
- Select Family Planning Indicators Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/f25c8a83-6599-4f4c-a1fd-4b3e8606b6f5/download/select-family-planning-indicators_national_mrt.csv
- Select Nutrition Indicators Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/f00e4444-91f2-4694-9639-08fe74e9d0c9/download/select-nutrition-indicators_national_mrt.csv
- Select Child Mortality Indicators Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/c65671be-37ee-4619-8bbd-3f4bbd338b78/download/select-child-mortality-indicators_national_mrt.csv
- Select Education Indicators Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/668a6b91-175e-4134-8fb0-b400b38ad8a2/download/select-education-indicators_national_mrt.csv
- COVID-19 Prevention Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/f6591275-a1b1-4b76-a07f-2b8805572987/download/covid-19-prevention_national_mrt.csv
- COVID-19 Additional factors Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/99dd717c-b106-4b84-b597-324e9929fa5f/download/covid-19-additional-factors_national_mrt.csv
- Anemia Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/e5967039-bcbb-4637-b184-c65f4348d8da/download/anemia_national_mrt.csv
- Birth Registration Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/048880a4-d1c0-4885-8a83-b7ec08cb8880/download/birth-registration_national_mrt.csv
- Health Insurance Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/274a0e0c-89ab-4c97-96f4-6412fa66069c/download/health-insurance_national_mrt.csv
- HIV Attitudes Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/24ec936d-bc62-43aa-9985-d55df748506d/download/hiv-attitudes_national_mrt.csv
- HIV Counseling and Testing Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/60cb807c-2452-4b0a-9620-08f32b83748e/download/hiv-counseling-and-testing_national_mrt.csv
- HIV Knowledge Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/6797bc78-72a9-4c3c-a555-582f3e346e47/download/hiv-knowledge_national_mrt.csv
- Insecticide Treated Nets Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/2b17331e-02e3-4faf-9202-db63ab78b3ad/download/insecticide-treated-nets_national_mrt.csv
- Iodized Salt Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/4dd7acce-5e42-47cd-b061-62c84558993d/download/iodized-salt_national_mrt.csv
- Literacy Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/3c3f6c13-fe4a-4e96-8698-c58db20ad0bf/download/literacy_national_mrt.csv
- Malaria Parasitemia Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/aabfad29-422a-4b5f-b587-f9f008a38762/download/malaria-parasitemia_national_mrt.csv
- Micronutrients Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/d26d4eb2-86a5-4e88-bba2-2c8b4dc6487f/download/micronutrients_national_mrt.csv
- Social Marketing Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/5266b301-7e3f-4b67-9451-661d460bde42/download/social-marketing_national_mrt.csv
- Tobacco Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/8920140e-1314-49a6-97dc-2ff608a4a5f4/download/tobacco_national_mrt.csv
- Select Malaria Indicators Data for Mauritania (CSV): https://data.humdata.org/dataset/0277fc92-309b-48dd-9596-f6b046845103/resource/954fd4d9-8ed4-4e60-a941-562ed28aa664/download/select-malaria-indicators_national_mrt.csv

## Licence conditions

No derivatives: files are redistributed unmodified.

## Methodology (from the publisher)

Sample Survey

## Attribution

The DHS Program, via the Humanitarian Data Exchange (https://data.humdata.org/dataset/dhs-data-for-mauritania). Licence: CC BY-ND 4.0.

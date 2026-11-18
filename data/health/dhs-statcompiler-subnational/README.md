# Mauritania - Subnational Demographic and Health Data

Contains data from the DHS data portal. There is also a dataset containing Mauritania - National Demographic and Health Data on HDX. The DHS Program Application Programming Interface (API) provides software developers access to aggregated indicator data from The Demographic and Health Surveys (DHS) Program. The API can be used to create various applications to help analyze, visualize, explore and disseminate data on population, health, HIV, and nutrition from more than 90 countries.

| Field | Value |
|---|---|
| Category | `health` |
| Publisher | The DHS Program |
| Geographic coverage | Mauritania |
| Reference period | 2000-01-01 to 2020-12-31 |
| Source page | https://data.humdata.org/dataset/dhs-subnational-data-for-mauritania |
| Licence | [CC BY-ND 4.0](https://creativecommons.org/licenses/by-nd/4.0/) |
| Redistribution | `allowed` |
| Source last updated | 2026-07-31 |
| Retrieved | 2026-11-14 |

## Processing

Files downloaded unchanged from HDX resources. Many HDX CSVs contain a second header row of HXL hashtags (e.g. `#country+code`); it is kept as published — skip it when loading (e.g. `pandas.read_csv(path, skiprows=[1])`) if present.

## Original resources

- DHS Quickstats Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/a0fe0c94-3c17-4a69-9da2-4a7c23ecc071/download/dhs-quickstats_subnational_mrt.csv
- DHS Mobile Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/00214970-578f-46ec-bd92-37bf42e2bcea/download/dhs-mobile_subnational_mrt.csv
- SDGs Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/a9c16b13-cc52-4568-8b5d-d4d78feb57cf/download/sdgs_subnational_mrt.csv
- MDGs Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/60fdce23-4532-4ec3-9539-104993bec830/download/mdgs_subnational_mrt.csv
- PMI/RBM Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/76302149-1690-4b03-8e83-594c4b87821f/download/rbm_subnational_mrt.csv
- IYCF Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/dd70223b-33bd-4ad5-8ba6-56d8ef16ec63/download/iycf_subnational_mrt.csv
- MICS indicators Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/e8eaa9c9-428e-4264-bbf7-0b01addf7e32/download/mics-indicators_subnational_mrt.csv
- FP2020 Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/0161bd3c-4b67-4661-b6db-045a17471964/download/fp2020_subnational_mrt.csv
- Access to Health Care Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/3f98e6af-67a3-41a2-acb5-526eec2ee95a/download/access-to-health-care_subnational_mrt.csv
- Anthropometry Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/87ced944-6500-4466-8f91-469a92b629fc/download/anthropometry_subnational_mrt.csv
- Child Mortality Rates Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/bc50ac8c-56ea-4e41-bd85-77df328daede/download/child-mortality-rates_subnational_mrt.csv
- Diarrhea Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/ab1a84e7-f98a-4266-b142-86834729e271/download/diarrhea_subnational_mrt.csv
- Fertility Rates Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/1cfd8217-e682-46a2-8ca5-06020fc3c2fd/download/fertility-rates_subnational_mrt.csv
- Immunization Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/f70589b8-f77e-4d2c-8968-d32a20e49665/download/immunization_subnational_mrt.csv
- Men's Fertility and Family Planning Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/e788dfbf-c5e4-40ef-ba8b-7ec82ba15ad1/download/mens-fertility-and-family-planning_subnational_mrt.csv
- Orphans Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/87c6150c-f0c0-494e-ae7d-92c90973b5fe/download/orphans_subnational_mrt.csv
- Symptoms of acute respiratory infection (ARI) Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/1c2bbb56-bc9d-4045-90ee-22f1fc975a5f/download/symptoms-of-acute-respiratory-infection-ari_subnational_mrt.csv
- Sexual Intercourse Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/1112c14f-c5f9-4bd4-87c5-65a39b169c2c/download/sexual-intercourse_subnational_mrt.csv
- Toilet Facilities Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/be8ef18b-a9e7-41ca-a035-3bdfcccd3019/download/toilet-facilities_subnational_mrt.csv
- Water Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/b9d4b4e1-08a9-406c-9903-7e5adc9b0626/download/water_subnational_mrt.csv
- Select Gender Indicators Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/e2c7dc8b-583a-4067-a10f-144b9ff34331/download/select-gender-indicators_subnational_mrt.csv
- Select Family Planning Indicators Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/3d757d67-1a2f-429e-9890-c1e7c29e92a0/download/select-family-planning-indicators_subnational_mrt.csv
- Select Nutrition Indicators Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/e233628a-86a3-4261-81c2-d1ac5fb79cc6/download/select-nutrition-indicators_subnational_mrt.csv
- Select Child Mortality Indicators Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/930e5df0-f3e7-4746-8242-40bc1444edaf/download/select-child-mortality-indicators_subnational_mrt.csv
- Select Education Indicators Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/cf78859c-6341-4a2d-9f55-d8af266d11a3/download/select-education-indicators_subnational_mrt.csv
- COVID-19 Prevention Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/6b5550ac-e38c-431f-b203-3d23c7f348c5/download/covid-19-prevention_subnational_mrt.csv
- COVID-19 Additional factors Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/bc9594e3-f19b-4f7a-b690-ec33fcd68e98/download/covid-19-additional-factors_subnational_mrt.csv
- Anemia Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/0908b979-7d28-484c-9956-544a2584e8b6/download/anemia_subnational_mrt.csv
- Birth Registration Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/7e289580-784a-4939-8fc9-9ff62a684c5b/download/birth-registration_subnational_mrt.csv
- Health Insurance Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/81ffc6be-63eb-421a-b5fd-011a3f2de468/download/health-insurance_subnational_mrt.csv
- HIV Attitudes Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/c775f012-bf1e-4509-9a2d-e7bfb22a223b/download/hiv-attitudes_subnational_mrt.csv
- HIV Counseling and Testing Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/0eeb3fda-d445-4403-8440-1cb825fc3675/download/hiv-counseling-and-testing_subnational_mrt.csv
- HIV Knowledge Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/a1b22395-828c-441e-b5f0-9080794c748d/download/hiv-knowledge_subnational_mrt.csv
- Insecticide Treated Nets Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/44ddb8db-eea2-4393-8d83-5708661501cc/download/insecticide-treated-nets_subnational_mrt.csv
- Iodized Salt Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/a40d347c-0b84-4769-8296-36632b256f2d/download/iodized-salt_subnational_mrt.csv
- Literacy Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/facd2122-8ec6-4eb5-9b8d-60edc6d67a33/download/literacy_subnational_mrt.csv
- Malaria Parasitemia Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/4bc7686e-00fd-4e94-9d28-fe82c468ff77/download/malaria-parasitemia_subnational_mrt.csv
- Micronutrients Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/6f1fbaf4-bb6a-4628-9f24-7ec16868ad56/download/micronutrients_subnational_mrt.csv
- Social Marketing Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/98331d0f-9b64-487a-969b-58385cd51a08/download/social-marketing_subnational_mrt.csv
- Tobacco Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/87e602bf-6efe-4689-a0e1-87a93f599315/download/tobacco_subnational_mrt.csv
- Select Malaria Indicators Data for Mauritania (CSV): https://data.humdata.org/dataset/3c6841d8-6122-49ec-8de3-4cfb0fb97d38/resource/3a80c498-22b1-43e2-b173-4d3f27e0bac2/download/select-malaria-indicators_subnational_mrt.csv

## Licence conditions

No derivatives: files are redistributed unmodified.

## Methodology (from the publisher)

Sample Survey

## Attribution

The DHS Program, via the Humanitarian Data Exchange (https://data.humdata.org/dataset/dhs-subnational-data-for-mauritania). Licence: CC BY-ND 4.0.

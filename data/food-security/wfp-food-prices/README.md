# Mauritania - Food Prices

This dataset contains Food Prices data for Mauritania, sourced from the World Food Programme Price Database. The World Food Programme Price Database covers foods such as maize, rice, beans, fish, and sugar for 98 countries and some 3000 markets. It is updated weekly but contains to a large extent monthly data. The data goes back as far as 1992 for a few countries, although many countries started reporting from 2003 or thereafter.

| Field | Value |
|---|---|
| Category | `food-security` |
| Publisher | WFP - World Food Programme |
| Geographic coverage | Mauritania |
| Reference period | 2003-10-15 to 2026-10-15 |
| Source page | https://data.humdata.org/dataset/wfp-food-prices-for-mauritania |
| Licence | [CC BY 3.0 IGO](https://creativecommons.org/licenses/by/3.0/igo/) |
| Redistribution | `allowed` |
| Source last updated | 2026-11-04 |
| Retrieved | 2026-11-14 |

## Processing

Files downloaded unchanged from HDX resources. Many HDX CSVs contain a second header row of HXL hashtags (e.g. `#country+code`); it is kept as published — skip it when loading (e.g. `pandas.read_csv(path, skiprows=[1])`) if present.

## Original resources

- Mauritania - Food Prices (CSV): https://data.humdata.org/dataset/a17cd464-d4e6-48d0-8bec-e6d3d2f5068a/resource/2c473576-bb75-48b5-b2b0-83ed914bb540/download/wfp_food_prices_mrt.csv
- Mauritania - Markets (CSV): https://data.humdata.org/dataset/a17cd464-d4e6-48d0-8bec-e6d3d2f5068a/resource/e23e8e78-4227-4f96-a81b-5728d002dc6a/download/wfp_markets_mrt.csv

## Methodology (from the publisher)

Registry

## Limitations

Although the frequency of updates is set to every month, updates may occur more or less frequently

## Attribution

WFP - World Food Programme / FPMA, GTS, Office National de Statistique via FAO: GIEWS, WFP, WFP CO, via the Humanitarian Data Exchange (https://data.humdata.org/dataset/wfp-food-prices-for-mauritania). Licence: CC BY 3.0 IGO.

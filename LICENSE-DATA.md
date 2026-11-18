# Data licensing and attribution policy

## 1. Datasets keep their original licences

Mauritania Datasets does **not** relicense any dataset. Every file under `data/` is redistributed under the licence chosen by its original publisher, recorded in:

- the dataset's own `README.md` (Licence, Redistribution, Attribution sections), and
- `metadata/datasets.json` → `license`, `license_url`, `license_conditions`, `attribution`.

If the two disagree, or a publisher's terms change, **the publisher's current terms prevail**. Please open an issue so we can correct the record.

## 2. Licences of hosted datasets

| Licence | Hosted datasets | Licence text |
|---|---:|---|
| CC BY 4.0 | 80 | https://creativecommons.org/licenses/by/4.0/ |
| CC BY 3.0 IGO | 24 | https://creativecommons.org/licenses/by/3.0/igo/ |
| ODbL 1.0 | 14 | https://opendatacommons.org/licenses/odbl/1-0/ |
| CC0 1.0 | 4 | https://creativecommons.org/publicdomain/zero/1.0/ |
| CC BY-SA 4.0 | 4 | https://creativecommons.org/licenses/by-sa/4.0/ |
| CC BY-NC-SA 3.0 IGO | 3 | https://creativecommons.org/licenses/by-nc-sa/3.0/igo/ |
| CC BY-ND 4.0 | 2 | https://creativecommons.org/licenses/by-nd/4.0/ |
| Creative Commons Attribution 3.0 Intergovernmental Organisations (CC BY 3.0 IGO) / Creative Commons Attribution-ShareAlike 3.0 Unported | 1 |  |
| NASA open data (no restrictions; attribution requested) | 1 | https://power.larc.nasa.gov/docs/referencing/ |
| Public Domain | 1 |  |
| CC BY-NC 4.0 | 1 | https://creativecommons.org/licenses/by-nc/4.0/ |
| EITI content policy (free republication with credit) | 1 | https://eiti.org/open-data |
| CC BY 3.0 IGO / CC BY 4.0 | 1 |  |

## 3. Datasets with additional conditions

- `MRT-EDU-001` Education Facilities of Mauritania: ODbL 1.0 — Share-alike for derived databases (Open Database License).
- `MRT-HLT-001` Mauritania - National Demographic and Health Data: CC BY-ND 4.0 — No derivatives: files are redistributed unmodified.
- `MRT-HLT-002` Mauritania - Subnational Demographic and Health Data: CC BY-ND 4.0 — No derivatives: files are redistributed unmodified.
- `MRT-HLT-003` Mauritania Healthsites: ODbL 1.0 — Share-alike for derived databases (Open Database License).
- `MRT-HLT-006` Health Facilities of Mauritania: ODbL 1.0 — Share-alike for derived databases (Open Database License).
- `MRT-HLT-007` Mauritania - Health Indicators: CC BY-NC-SA 3.0 IGO — Non-commercial use only; adaptations must be shared under the same licence.
- `MRT-HLT-008` Mauritania - Historical Health Indicators: CC BY-NC-SA 3.0 IGO — Non-commercial use only; adaptations must be shared under the same licence.
- `MRT-FSC-011` Mauritania: Integrated Context Analysis (ICA), 2017: ODbL 1.0 — Share-alike for derived databases (Open Database License).
- `MRT-GEO-003` Populated Places of Mauritania: ODbL 1.0 — Share-alike for derived databases (Open Database License).
- `MRT-ADM-001` geoBoundaries — Mauritania administrative boundaries (ADM0–ADM2): Creative Commons Attribution 3.0 Intergovernmental Organisations (CC BY 3.0 IGO) / Creative Commons Attribution-ShareAlike 3.0 Unported — Licence differs by level — see `levels.csv`. ADM1 is CC BY-SA 3.0 (share-alike).
- `MRT-ADM-002` Mauritania: Administrative Division with Aggregated Population: ODbL 1.0 — Share-alike for derived databases (Open Database License).
- `MRT-WAT-001` Waterways of Mauritania: ODbL 1.0 — Share-alike for derived databases (Open Database License).
- `MRT-TRN-004` Airports of Mauritania: ODbL 1.0 — Share-alike for derived databases (Open Database License).
- `MRT-TRN-005` Railways of Mauritania: ODbL 1.0 — Share-alike for derived databases (Open Database License).
- `MRT-TRN-006` Roads of Mauritania: ODbL 1.0 — Share-alike for derived databases (Open Database License).
- `MRT-TRN-007` Sea Ports of Mauritania: ODbL 1.0 — Share-alike for derived databases (Open Database License).
- `MRT-INF-001` Mauritania - Accessibility Indicators: CC BY-SA 4.0 — Adaptations must be shared under the same licence.
- `MRT-INF-002` Financial Services of Mauritania: ODbL 1.0 — Share-alike for derived databases (Open Database License).
- `MRT-INF-003` Points of Interest of Mauritania: ODbL 1.0 — Share-alike for derived databases (Open Database License).
- `MRT-TEL-001` ITU — ICT indicators for Mauritania (mobile, internet, broadband, prices): CC BY-NC-SA 3.0 IGO — Non-commercial use only; adaptations must be shared under the same licence.
- `MRT-POV-001` Relative Wealth Index: CC BY-NC 4.0 — Non-commercial use only.
- `MRT-TOU-001` Cultural Places of Mauritania: ODbL 1.0 — Share-alike for derived databases (Open Database License).
- `MRT-HUM-003` Mauritania - Risk Assessment Indicators: CC BY-SA 4.0 — Adaptations must be shared under the same licence.
- `MRT-HUM-011` Mauritania - VIEWS conflict forecasts: CC BY-SA 4.0 — Adaptations must be shared under the same licence.

In particular:
- **Non-commercial (NC)**: do not use these files for commercial purposes without permission from the publisher.
- **No derivatives (ND)**: the DHS STATcompiler files are redistributed exactly as published; share modified versions only if the licence allows it.
- **Share-alike (SA, ODbL)**: derived databases/adaptations must be released under the same licence. OpenStreetMap-derived data: © OpenStreetMap contributors, ODbL 1.0.

## 4. What is not redistributed

96 catalogued datasets are **not** hosted. Their entries in `metadata/datasets.json` have `"hosted_in_repository": false` and a `not_hosted_reason`:

- `link_only`: publicly accessible but without an explicit licence permitting redistribution (e.g. ANSADE, Ministry of Finance, CENI, ARE, IMROP publications);
- `restricted`: terms forbid redistribution or require registration/approval (e.g. ACLED, EM-DAT, DHS/MICS/UNHCR/ANADRIM microdata, BCM files, WDPA);
- `unknown`: licence could not be determined;
- `allowed` but not mirrored: open data too large for a Git repository (building footprints, high-resolution rasters, satellite archives) or behind an authenticated download API.

## 5. Attribution

When you use a dataset, credit the **original publisher** using the attribution line in its README (for example: "Source: FAO, FAOSTAT, CC BY 4.0"). Crediting Mauritania Datasets as the access point is appreciated but does not replace the publisher's attribution.

## 6. this project's own content

The README files, metadata files (`metadata/`) and documentation (`documentation/`) written for this project are licensed under the Creative Commons Attribution 4.0 International licence (see `LICENSE`).

## 7. Take-down

If you are a rights holder and believe a file is redistributed in breach of its terms, open an issue. The file will be removed while the matter is checked.

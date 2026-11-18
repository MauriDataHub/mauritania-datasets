# Data policy

## 1. Scope

Mauritania Datasets collects data about **Mauritania**: national, subnational and gridded data, and Mauritania extracts of multi-country datasets. A dataset is included only if it actually contains Mauritania data. Multi-country files are filtered to Mauritania, and the filter is documented.

## 2. Data-only repository

This public repository contains **datasets, metadata and documentation only**. Collection and processing tools are kept outside the repository. There are no scripts, scrapers, notebooks, configuration files, logs, credentials or temporary files here.

## 3. Inclusion and hosting rules

1. **Find the original source**, and prefer the producer (e.g. FAO, ILO, World Bank, UN DESA) over intermediaries.
2. **Check the licence** on the publisher's own site or official metadata before hosting:
   - `allowed`: an explicit open licence (Creative Commons, ODbL, public domain/CC0, or a published reuse policy explicitly permitting republication) → files may be hosted.
   - `link_only`: public but no explicit permission → only the reference and metadata are catalogued.
   - `restricted`: terms forbid redistribution, or access needs registration/approval → reference only.
   - `unknown`: licence could not be determined → reference only.
3. **"Publicly accessible" is not "freely redistributable".** Websites marked "Tous droits réservés" / "all rights reserved", or with no licence, are treated as `link_only`.
4. **When sources disagree**, the more restrictive statement is applied (e.g. WHO GHO data are recorded as CC BY-NC-SA 3.0 IGO as stated on the HDX record, although data.who.int now mentions CC BY 4.0).
5. **Preserve originals**: values, codes and units are not changed. Conversions (JSON → CSV, XLSX → CSV for filtering) are documented in each README.
6. **No fabrication**: metadata fields the publisher does not state are left empty (`null`) or marked `Not stated`.
7. **Deduplicate**: where the same series is available from several World Bank databases, it is published once (WDI first). Overlaps between different publishers (e.g. WDI and WHO) are kept because they are distinct releases, and are documented.
8. **Size**: files over 50 MB are not mirrored; they are catalogued as `allowed` but not hosted.

## 4. Legal and ethical rules

- Authentication, paywalls, CAPTCHAs and bot challenges are never bypassed. Sources behind them are catalogued as references.
- Website terms and robots guidance are respected. Unreachable government sites are recorded, not worked around.
- **No personal or sensitive data.** Microdata with individual records (household surveys, refugee surveys, censuses) are not redistributed. Hosted datasets are aggregates, published indicators, or public geographic features.
- Attribution and licence information are kept with every dataset.

## 5. Official Mauritanian sources (status at 2026-11-14)

| Source | Finding | Status |
|---|---|---|
| ANSADE (ansade.mr, portal, ANADRIM) | Publications are public; footer "Tous droits réservés"; ANADRIM microdata require written approval | `link_only` / `restricted` |
| Banque Centrale de Mauritanie | Legal notice forbids reproduction without prior written consent | `restricted` |
| Ministry of Finance, DGB | Public PDFs; no licence | `link_only` |
| CENI | Election reports only (no machine-readable results) | `link_only` |
| ARE (telecom regulator) | Observatory stopped at 2013; annual reports | `link_only` |
| IMROP, ONISPA, Ministry of Fisheries, SNIM | Public reports; no licence | `link_only` |
| Education, Health, Agriculture, Water, Transport, Economy ministries; SNDE; Port of Nouakchott; tourism office | Unreachable during checks (connection reset / no DNS) or login-only (DHIS2) | catalogued where possible |
| National open-data portal | `data.gov.mr` does not exist; a portal is announced in the national digital strategy | — |

Mauritanian data **are** included indirectly through international databases that publish openly licensed compilations of national statistics (World Bank, FAO, ILO, UN DESA, UNESCO, WHO, EITI).

## 6. Updates and corrections

`date_last_checked` records when source and licence were last verified. Issues for corrections or take-down requests are welcome (see LICENSE-DATA.md).

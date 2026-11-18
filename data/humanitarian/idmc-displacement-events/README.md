# Mauritania - Internal Displacements Updates (IDU)

Conflict and disaster population movement (flows) data for Mauritania. The IDU (Internal Displacement Updates) dataset, provided by the Internal Displacement Monitoring Centre (IDMC), offers timely event data and provisional information on new internal displacements caused by conflicts and disasters. Representing the most recent available information, the IDU is updated daily and focuses on "flows" (new displacements). Internally displaced persons (IDPs) are defined according to the 1998 Guiding Principles as people or groups of people who have been forced or obliged to flee or to leave their homes or places of habitual residence, in particular as a result of armed conflict, or to avoid the effects of armed conflict, situations of generalized violence, violations of human rights, or natural or human-made disasters and who have not crossed an international border. […]

| Field | Value |
|---|---|
| Category | `humanitarian` |
| Publisher | Internal Displacement Monitoring Centre (IDMC) |
| Geographic coverage | Mauritania |
| Reference period | 2025-08-19 to 2025-08-30 |
| Source page | https://data.humdata.org/dataset/mrt-idmc-idu-events |
| Original download / API | https://data.humdata.org/dataset/64fdf2a6-9bc8-4184-8e18-8a5e03cd60f4/resource/a5e48244-484f-4154-874c-c889a2332b4b/download/mrt_idmc_idu_events.csv |
| Licence | [CC BY 3.0 IGO](https://creativecommons.org/licenses/by/3.0/igo/) |
| Redistribution | `allowed` |
| Source last updated | 2026-11-06 |
| Retrieved | 2026-11-14 |

## Processing

Files downloaded unchanged from HDX resources. Many HDX CSVs contain a second header row of HXL hashtags (e.g. `#country+code`); it is kept as published — skip it when loading (e.g. `pandas.read_csv(path, skiprows=[1])`) if present.

## Original resources

- mrt_idmc_idu_events.csv (CSV): https://data.humdata.org/dataset/64fdf2a6-9bc8-4184-8e18-8a5e03cd60f4/resource/a5e48244-484f-4154-874c-c889a2332b4b/download/mrt_idmc_idu_events.csv

## Methodology (from the publisher)

IDMC defines an event as any distinct incident, whether prompted by natural hazards or conflict-related violence, resulting in the forced displacement of individuals within a specified geographical area confined to the borders of a single country. […]

## Limitations

Please note that most of the figures are estimates. The definition highlights two issues: 1) The coercive or otherwise involuntary character of movement. The definition mentions some of the most common causes of involuntary movements, such as armed conflict, violence, human rights violations and disasters. These causes have in common that they give no choice to people but to leave their homes and deprive them of the most essential protection mechanisms, such as community networks, access to services, livelihoods. […]

## Attribution

Internal Displacement Monitoring Centre (IDMC) / IDMC, via the Humanitarian Data Exchange (https://data.humdata.org/dataset/mrt-idmc-idu-events). Licence: CC BY 3.0 IGO.

---
license: cc-by-4.0
language: [en]
pretty_name: Utah Marketing Agencies 2026
size_categories: [n<1K]
task_categories: [tabular-classification]
tags: [marketing, agencies, utah, local-business, directory, tabular]
configs:
- config_name: default
  data_files: utah_marketing_agencies.csv
---

# Utah Marketing Agencies 2026

A list of 309 marketing agencies based in Utah, across 50 cities, with the services each one offers, team size, founding year, minimum project size and hourly rate where the agency publishes them. Every row was compiled from the agency's own website plus at least one public listing, last checked 2026-10-29.

The data powers the [Utah marketing agency directory](https://thebrandcaptain.com/directory/) run by Brand Captain, a Utah-based marketing agency. Each row links to its city page in that directory.

## Files

| File | Format |
|---|---|
| `utah_marketing_agencies.csv` | One row per agency, UTF-8 |
| `utah_marketing_agencies.json` | Same rows as a JSON array |

## Columns

| Column | Meaning |
|---|---|
| `name` | Agency name as it appears on its website |
| `city`, `state` | City of the agency's Utah office |
| `website` | Agency homepage |
| `services` | Semicolon-separated list from 13 service categories |
| `svc_*` | One 0/1 column per service category: seo, local_seo, web_design, google_ads, meta_ads, social_media, branding, content, ecommerce, email, video, pr, full_service |
| `industries` | Industries the agency says it serves, where listed |
| `team_size` | Employee band, e.g. `10 - 49` |
| `founded` | Year founded |
| `min_project_usd` | Published minimum project size |
| `hourly_rate` | Published hourly rate band |
| `bbb_accredited` | 1 if BBB accredited, 0 if listed and not accredited, blank if no BBB listing found |
| `directory_page` | Page for the agency's city in the Brand Captain directory |
| `sources` | URLs the row was compiled from, separated by ` \| ` |
| `checked_on` | Date the row was last verified |

## Coverage

309 agencies. Founding year is filled for 268, team size for 275, hourly rate for 153. Salt Lake City (70), Lehi (35) and Provo (26) have the most agencies.

Services offered most often: SEO (219), web design (209), Google Ads (165), social media (163), branding (132).

## How it was built

Candidate agencies were pulled from Clutch, DesignRush, the BBB and Google Maps listings for Utah. A script then fetched each candidate's homepage and contact page and dropped dead or parked sites, agencies with no Utah address or Utah mention, and video-production-only shops. Service and industry tags come from matching the agency's own homepage text against fixed keyword lists, so an agency that offers a service but never names it on its site will show a 0 for it. Review text and star ratings from third-party sites are not included.

## License and citation

DOI: [10.5281/zenodo.24512883](https://doi.org/10.5281/zenodo.24512883)


CC BY 4.0. Credit "Brand Captain, Utah Marketing Agencies 2026" with a link to https://thebrandcaptain.com/directory/.

Corrections: open an issue or use the contact form at https://thebrandcaptain.com/.

# AI Patents by State and Metro Area, 2025 (startbusinessbystate.com)

U.S. AI patent grants by the first inventor's state and metro area, per resident, change since 2022, and small-entity share of AI patent applications.

Main page: https://startbusinessbystate.com/ai-patents-by-state/

## Summary

How many AI patents were granted in 2025 to inventors in each state and metro area, how that compares with population and with 2022, and what share of each state's published AI patent applications were filed at small or micro entity fee status (a rough signal of small business and individual inventors).

## Files

| File | Rows | What it is |
|---|---|---|
| `data/ai_patent_grants_by_metro.csv` | 584 | AI patent grants by the first inventor's metro area. |
| `data/ai_patents_by_state_2025.csv` | 51 | AI patents by state. |

All files are UTF-8 CSV with a header row in snake_case. Blank cells mean the value is not available, not applicable, or suppressed by the source.

## Data dictionary

### data/ai_patent_grants_by_metro.csv

AI patent grants by the first inventor's metro area. Rows: 584. Columns: 5.

| Column | Meaning | Units |
|---|---|---|
| `metro_area` | Census core-based statistical area (metro or micro area) name. | text |
| `ai_grants_2019` | AI utility patents granted in 2019 with the first inventor in the area. | patents |
| `ai_grants_2022` | Same for 2022. | patents |
| `ai_grants_2025` | Same for 2025. | patents |
| `chg_2025_vs_2022_pct` | Percent change from 2022 to 2025 (blank when 2022 is zero). | percent |

### data/ai_patents_by_state_2025.csv

AI patents by state. Rows: 51. Columns: 18.

| Column | Meaning | Units |
|---|---|---|
| `rank_per_100k` | Rank by AI patents per 100,000 residents in 2025 (1 = highest). | rank |
| `state` | State name (50 states plus District of Columbia). | text |
| `abbr` | Two-letter USPS state code. | text |
| `ai_patents_granted_2025` | AI utility patents granted in 2025 with the first inventor in the state. | patents |
| `ai_patents_per_100k_residents_2025` | ai_patents_granted_2025 per 100,000 residents. | patents per 100,000 people |
| `rank_by_count_2025` | Rank by ai_patents_granted_2025 (1 = most). | rank |
| `population_2025` | Census Vintage 2025 resident population estimate. | people |
| `ai_patents_granted_2022` | Same count for 2022. | patents |
| `change_2025_vs_2022_pct` | Percent change from 2022 to 2025. | percent |
| `fewer_than_100_in_2022` | yes if the state had fewer than 100 AI grants in 2022, so the change is unstable. | yes/no |
| `ai_share_of_all_state_patents_2025_pct` | AI grants as a share of all utility grants with the first inventor in the state, 2025. | percent |
| `odp_ai_applications_published_2025_any_inventor` | AI patent applications published in 2025 that list at least one inventor in the state. | applications |
| `odp_small_micro_entity_applications_2025` | Of those, applications filed at small or micro entity fee status. | applications |
| `odp_small_micro_entity_share_2025_pct` | Small or micro entity applications as a share of the state total. | percent |
| `odp_ai_applications_published_jan_sep_2022` | AI applications published January to September 2022 (any inventor in the state). | applications |
| `odp_ai_applications_published_jan_sep_2026` | AI applications published January to September 2026 (any inventor in the state). | applications |
| `odp_change_jan_sep_2026_vs_2022_pct` | Percent change between those two periods. | percent |
| `note` | Notes on unusual values. | text |

## Sources

| Source | Link | License or status |
|---|---|---|
| USPTO PatentsView bulk granted patent data (PVGPATDIS), file release April 10, 2026 | https://patentsview.org/download/data-download-tables | CC BY 4.0 (PatentsView) |
| USPTO Open Data Portal, patent application publications | https://data.uspto.gov/ | Public domain (U.S. government work) |
| Census Vintage 2025 state population estimates | https://www.census.gov/programs-surveys/popest.html | Public domain (U.S. government work) |
| Census core-based statistical area (CBSA) delineations, 2023 (2020 for Connecticut) | https://www.census.gov/geographies/reference-files/time-series/demo/metro-micro/delineation-files.html | Public domain (U.S. government work) |

## Methodology

- An AI patent is a U.S. utility patent with at least one current CPC class in G06N (machine learning and neural networks), G06F40 (natural language processing), G06V (image and video recognition) or G10L15 (speech recognition). We checked this definition against the USPTO AI Patent Dataset for 2023: 93.1% of the patents we count are AI there too.
- Each grant is counted once, in the state (and metro area) where the first-listed inventor lives. So state counts add up to the U.S. total (13,754 in 2025) and nothing is counted twice.
- Rate per 100,000 residents uses Census Vintage 2025 population.
- Application columns (odp_) count published AI applications in the Open Data Portal that list at least one inventor in the state, so a multi-state application counts in each state. Small or micro entity share is the share filed at those reduced fee levels.
- Metro areas use 2023 CBSA definitions. Connecticut uses the 2020 county-based areas.

## Limitations

- Grants lag filings by two to three years, so 2025 grants mostly reflect 2021 to 2023 ideas.
- The image class also catches some display and sensor hardware.
- Inventor location is where the inventor lives, not where the company is based.
- States with fewer than 100 AI patents in 2022 have noisy percent changes (flagged).
- Small or micro entity status is a fee category, not a measure of company size.

## As-of date

Grants through December 31, 2025 (PatentsView release of April 10, 2026). Application counts pulled from the USPTO Open Data Portal on September 30, 2026.

Version 1.0.0, released 2026-10-02.

## How to cite

StartBusinessByState. (2026). *AI Patents by State and Metro Area, 2025 (startbusinessbystate.com)* (Version 1.0.0) [Data set]. startbusinessbystate.com. https://github.com/jameyriley46-ux/startbusinessbystate-ai-patents-by-state

Please also credit the original sources listed above. When you use the data, a link back to https://startbusinessbystate.com/ai-patents-by-state/ is appreciated.

## Related pages on startbusinessbystate.com

- https://startbusinessbystate.com/ai-patents-by-state/

## License

This dataset is released under the Creative Commons Attribution 4.0 International license (CC BY 4.0). See `LICENSE`. You may share and adapt it, including for commercial use, as long as you give credit.
Underlying public domain data from U.S. government agencies stays public domain. Data from CC BY sources (such as LegiScan, PatentsView, Epoch AI or the Anthropic Economic Index, where used) also requires credit to those sources.

## Contact

StartBusinessByState (startbusinessbystate.com) (https://startbusinessbystate.com/)

# MetroLink Data Dictionary - Assignment 4

MetroLink is fictional. These are synthetic instructional data supplied for visualization design. No external dataset or prior assignment is needed.

## Observation unit and dates

`metro-service-data.csv` contains **192 sampled service runs**: 8 routes × 12 weeks × 2 peak periods. Every route-week has one AM run and one PM run. Each route has 24 sampled runs. All records in a week share a sample date; dates run from **2026-01-05 to 2026-03-23**.

The records are not a full timetable, all trips in a week, or daily ridership totals. One sample date does not establish continuous observation throughout that week.

## Raw fields

| Field | Meaning |
|---|---|
| `run_id` | Unique nominal identifier for one sampled run |
| `route_id` | Nominal route identifier R1-R8; its digit does not encode a rank |
| `service_date` | Sample date in YYYY-MM-DD format; temporal |
| `week` | Ordered study-week index 1-12 |
| `origin_station` | Name of the origin station; nominal |
| `destination_station` | Name of the destination station; nominal |
| `service_type` | Rapid, Local, Express, or Event; nominal |
| `time_period` | AM peak or PM peak; nominal |
| `passenger_count` | Passengers on that sampled run; quantitative count, not a weighting variable for this assignment |
| `delay_minutes` | Arrival delay of that run in minutes; quantitative, 3-23 in this file; zero would mean no delay |
| `status` | Raw-run category: On time (delay ≤5), Minor delay (6-10), Major delay (>10); these labels apply to individual integer-valued delays |

Required fields contain no missing values. Different runs may have the same measured values; retain them. The run-level `status` categories are not assigned to the derived route-week means and do not establish official service standards.

## Prepared long table: route-week-delay.csv

This table contains **96 rows**, one for every route-week pair. It is the recommended starting point for the graphic.

| Field | Meaning |
|---|---|
| `route_id` | Route being summarized |
| `week` | Study-week index, 1-12 |
| `service_date` | Shared sample date of the two contributing runs |
| `mean_delay_minutes` | Unweighted arithmetic mean of those two sampled delays |
| `sample_count` | Number of contributing sampled runs; 2 for every row |
| `am_delay_minutes` | Arrival delay of the AM sampled run |
| `pm_delay_minutes` | Arrival delay of the PM sampled run |

**mean_delay_minutes = (am_delay_minutes + pm_delay_minutes) / sample_count**

This formula applies here because every group contains exactly one AM and one PM run. For R1, week 1, the values are 3 and 5, so the mean is 4 minutes. All route-week means in this file are whole numbers, ranging from **4 to 22**. This is a property of these data, not a general rounding rule.

Do not weight the means by `passenger_count`. Do not average all 16 runs in a week and label that result as the mean for an individual route. Do not join the prepared mean onto both raw runs and then count the duplicated values as extra route-week observations.

## Prepared matrix: route-week-delay-matrix.csv

This is the same set of 96 means in a spreadsheet-friendly layout: one row per route and columns `week_01` through `week_12`. Each numeric cell is the mean delay in minutes for that route and week. The suffix identifies the study week, not a month.

Use either prepared format; do not combine them as separate observations. Both contain the same values, with no normalization or color choices applied. A spreadsheet may format CSV cells automatically, so check that the week order and numeric values remain correct after import.

<div class="assignment-page-break"></div>

## Derived summaries and comparisons

- A route’s period mean is the average of its 12 weekly means. Here it also equals the mean of its 24 raw delays because every week has the same sample count. Compute with full precision and disclose display rounding.
- A count of weeks above a chosen value must state the threshold and whether equality is included. It describes this sample under that rule, not compliance with a transit policy.
- A deviation is meaningful only when its reference is named, such as deviation from a stated sample mean. Do not present such a reference as an official target.
- Equal route-week values must remain equal in the graphic.

## Source and interpretation

The original records are the unchanged MetroLink teaching sample also used in Assignment 3. The prepared files aggregate those records without adding or removing observations. The local files are sufficient; no network connection is required to inspect the data.

Identify the source as the **MetroLink synthetic data supplied for Assignment 4**. Patterns support descriptions of this supplied sample, not claims about a real transport system, causal explanations, or statistical representativeness of all services.

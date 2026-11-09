# Subgroup Estimates: Codebook

File: `inputs/raw/subgroup_estimates.csv`

A small, deliberately messy teaching file shaped like PRAMS (Pregnancy Risk Assessment Monitoring System) subgroup estimates. The values are simulated, so use them for practice only.

## Unit of observation

Each row is one **pre-aggregated estimate**: the percent of new mothers in a state and subgroup who reported a measure (such as depression in the 3 months before birth). Rows are not individual people.

## Columns

| Column | Meaning |
|---|---|
| `State` | State name |
| `Subgroup Category` | What the subgroup is based on (age group, education, insurance, ...) |
| `Sub Group` | The subgroup within that category |
| `Measure` | The behavior or outcome estimated |
| `Estimate` | Percent estimate, stored as text |
| `Notes` | Free-text notes about the row |
| `Year` | Survey year |

## Known problems

The file has messy labels, numbers stored as text, and several ways of coding missing values. Finding these problems is part of the exercise.

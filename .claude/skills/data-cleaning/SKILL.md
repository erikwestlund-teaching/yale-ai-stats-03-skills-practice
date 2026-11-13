---
name: data-cleaning
description: How to clean raw data files in this project. Use whenever reading, recoding, reshaping, or saving cleaned data.
---

# Data cleaning

## Before writing code

- Read the codebook or other documentation that comes with the raw data.
- Report what one row represents, the number of rows and columns, and every problem you find (types, labels, missing-value codes, whitespace, duplicates).
- In a cleaning notebook, ask before dropping any rows. Leave exclusions from an analysis to the modeling or reporting step.

## Rules

- Never change raw data files (`inputs/raw/`). Write cleaned data to `inputs/final/` as CSV. If the README names other folders, use those.
- Build paths with `here::here()` so the code runs from any working directory.
- Rename columns to `snake_case`.
- Turn every missing-value code (such as `NA`, `--`, `Suppressed`, `not available`, and blanks) into `NA`. Keep a flag column that says why a value is missing.
- Trim whitespace. Use sentence case for labels; leave proper nouns such as state names as written.
- Recode spelling variants with an explicit `case_when()` table. Don't use fuzzy matching.
- Convert numbers stored as text with `readr::parse_number()`.
- Compute every number in the prose with inline R code.

## Checks to include in the notebook

- Row count before and after. They should match unless rows were dropped on purpose.
- `count()` of every recoded category, before and after.
- A table of any value that changed, with old and new values side by side.
- `stopifnot()` checks for things that must be true, for example percentages between 0 and 100.

## Final summary

Summarize every recoding decision in a short list at the end of the notebook.
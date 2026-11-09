---
name: data-cleaning
description: How to clean raw data files in this project. Use whenever reading, recoding, reshaping, or saving cleaned data.
---

# Data cleaning

## Before writing code

- Read the codebook in `inputs/raw/`.
- Report what one row represents, the number of rows and columns, and every problem you find (types, labels, missing-value codes, whitespace, duplicates).
- Ask before dropping any rows.

## Rules

- Never change files in `inputs/raw/`. Write cleaned data to `inputs/final/` as CSV.
- Build paths with `here::here()` so the code runs from any working directory.
- Rename columns to `snake_case`.
- Turn every missing-value code (`NA`, `--`, `Suppressed`, `not available`, blanks) into `NA`. Keep a flag column that says why a value is missing.
- Trim whitespace and standardize label case. Recode spelling variants with an explicit `case_when()` table, not fuzzy matching.
- Convert numbers stored as text with `readr::parse_number()`.

## Checks to include in the notebook

- Row count before and after. They should match unless rows were dropped on purpose.
- `count()` of every recoded category, before and after.
- A table of any value that changed, with old and new values side by side.
- `stopifnot()` checks for things that must be true, for example percentages between 0 and 100.

## When done

Summarize every recoding decision in a short list at the end of the notebook.
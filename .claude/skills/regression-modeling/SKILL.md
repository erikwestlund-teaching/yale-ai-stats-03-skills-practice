---
name: regression-modeling
description: How to fit, check, and report regression models in this project. Use whenever fitting or interpreting a statistical model.
---

# Regression modeling

## Before fitting

- State the question in one sentence and name the outcome and predictors.
- Default to complete cases. Report how many rows have complete data for the model's variables, and the rows dropped, by reason.
- Check the data for survey weights or design variables (columns with `weight`, `stratum`, `psu`). If there are any, **stop and ask** whether the analysis should account for the survey design. Don't silently ignore them.
- If the population definition is ambiguous (for example, "adults"), include it in your questions.
- Ask all questions in one message, with a recommended answer for each.

## Fitting

- Use base R `lm()`/`glm()`. Use `broom::tidy(conf.int = TRUE)` for coefficient tables.

## Checks

- Residuals vs. fitted values and a Q–Q plot of residuals.
- Note influential points or a non-linear pattern if you see them.

## Reporting

- Report estimates with 95% confidence intervals, in the outcome's units.
- Write "is associated with", never "causes", "increases", or "the effect of".
- List at least two limitations.
- Every number in the text comes from code output. Don't type numbers in by hand.
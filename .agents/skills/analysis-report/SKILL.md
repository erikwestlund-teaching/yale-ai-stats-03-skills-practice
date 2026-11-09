---
name: analysis-report
description: How to write a short Quarto analysis report in this project. Use whenever drafting or editing a report, summary, or write-up.
---

# Analysis report

## Structure

Use these sections, in this order:

1. **Summary**: three bullet points a busy reader can stop after.
2. **Data**: source, what a row is, n, exclusions.
3. **Methods**: what was done, in plain language.
4. **Results**: one figure and one table at most, each with a sentence saying what it shows.
5. **Limitations**
6. **Reproducibility**: R version and packages (`sessionInfo()` in a folded chunk).

## Rules

- **Every number in the text is computed inline** with `` `r ` `` code. Never type a number into the prose.
- Round sensibly: percentages to one decimal, counts as whole numbers with thousands separators.
- Hide code by default (`echo: false` in the YAML); keep it in the file.
- Don't use causal language, and don't make claims beyond the data.
- The report must render from a clean session: read data from files and set no absolute paths.

## When done

Render the report and confirm it builds. Then list any statement in the text that isn't directly backed by output in the report.
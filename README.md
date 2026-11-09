# Exercise 3: Practice With Skills

Part of the workshop **AI Tools for Statistical Programming and Analysis**.

Three tasks, each with its own skill. Do as many as time allows, in any order.

| Task | Notebook | Skill | Data |
|---|---|---|---|
| A. Data cleaning | `notebooks/01_cleaning.qmd` | `data-cleaning` | `inputs/raw/subgroup_estimates.csv` |
| B. Modeling | `notebooks/02_modeling.qmd` | `regression-modeling` | `inputs/raw/neighborhood_health_survey.csv` |
| C. Report | `notebooks/03_report.qmd` | `analysis-report` | `inputs/raw/neighborhood_health_survey.csv` |

The skills are in `.agents/skills/` (Posit Assistant, Codex) and `.claude/skills/` (Claude Code). In RStudio, use **More → Show Hidden Files** to see them.

## Open the project

- **RStudio:** open `yale-ai-stats-03-skills-practice.Rproj`.
- **Positron or VS Code:** open this folder (or `yale-ai-stats-03-skills-practice.code-workspace`).
- **Claude Code or Codex:** start the tool from a terminal in this folder.

You need R with the **tidyverse**, **rmarkdown**, and **here** packages, and Quarto (bundled with RStudio).

## Prompts

```text
A. Clean inputs/raw/subgroup_estimates.csv in notebooks/01_cleaning.qmd.
```

```text
B. In notebooks/02_modeling.qmd, use inputs/raw/neighborhood_health_survey.csv to model how mean systolic blood pressure relates to age, gender, and family income-to-poverty ratio among adults.
```

```text
C. In notebooks/03_report.qmd, write a short report on how mean daily sodium intake relates to mean systolic blood pressure among adults in inputs/raw/neighborhood_health_survey.csv. Render it when you're done.
```

## For each task

1. **Run it.**
2. **Check it** against the skill: read the code and render the notebook.
3. **Change the skill.** Edit one rule: add one, remove one, or make one stricter. Edit the copy your tool reads, or both.
4. **Run it again** in a new session and see whether the output changed the way you expected.

## Checklist

- Do the numbers in the text match the output?
- Did it report how many rows were used and dropped?
- Did it ask before doing something irreversible or debatable?
- Would you sign your name to this?

**Optional:** paste the notebook into a *different* model and ask it to find mistakes. Then decide whether its critique is right.

## About the folders

This project was created from a [Framework](https://framework.pub) blueprint, so it has the folder layout of a real analysis project: raw data in `inputs/raw/`, notebooks in `notebooks/`, results in `outputs/`. You don't need the framework R package; the notebooks use plain R. Files like `settings.yml` and `scaffold.R` belong to Framework and can be ignored.

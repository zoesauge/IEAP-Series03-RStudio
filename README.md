# IEAP-Series03-RStudio

Team report for the IEAP Series 03, _Data wrangling and ANOVA_

The rendered report is **`IEAP-Series03-RStudio.pdf`**.

## Team

| Name           | Questions                                                              | Section file                                 |
| :------------- | :--------------------------------------------------------------------- | :------------------------------------------- |
| Zoé SAUGE      | 1.1 Think before coding, 1.2 Library, 1.7 Differences with the article | `_01-question.qmd`, `_04-discussion.qmd`     |
| Alexis LAGARDE | 1.3 Data reorganisation and ANOVA, Git workflow, final render          | `_02-data-anova.qmd`, `_05-git-workflow.qmd` |
| Albatoul AHMAD | 1.4 Regression by group, 1.5 Publication graph, 1.6 PDF export         | `_03-regression-graph.qmd`                   |
| Everyone       | Challenges, data sources, grading checklist                            | `_06-challenges-checklist.qmd`               |

## Main results

- Mixed ANOVA, GROUP (3 levels, between) × ID (2 levels, within), 51 participants
  (19 patients after stroke, 13 age-matched adults, 19 young adults):
  GROUP F(2, 48) = 37.24, ID F(1, 48) = 26.11, GROUP × ID F(2, 48) = 11.58, all p < .001.
- The effect of difficulty is much larger after a stroke: the patients' regression slope
  is about 7 times that of the young adults, as in the article.

## Repository structure

```
IEAP-Series03-RStudio.qmd      master document (header, links, includes)
IEAP-Series03-RStudio.pdf      rendered report (the graded output)
movement_time_regression.pdf   publication figure, 8 x 6 inches (question 1.6)
references.bib                 scientific references with DOIs
data/Results.txt               raw data (one row per movement)
sections/                      one file per part of the report, each with one owner
  _01-question.qmd             1.1 and 1.2
  _02-data-anova.qmd           1.3
  _03-regression-graph.qmd     1.4, 1.5 and 1.6
  _04-discussion.qmd           1.7
  _05-git-workflow.qmd         Git workflow strategy
  _06-challenges-checklist.qmd challenges, data sources and grading checklist
```

## How to render

Then open `IEAP-Series03-RStudio.Rproj` in RStudio, open `IEAP-Series03-RStudio.qmd` and
click **Render** (or run `quarto render IEAP-Series03-RStudio.qmd`). The PDF is produced
with Typst, which is included in Quarto, so no LaTeX installation is needed.

## Git workflow

- One branch per part of the report, merged into `main` through a pull request with a
  merge commit, in the order of the questions:
  `1.1Think` (#1) → `1.2-data-anova` (#2) → `1.4-1.6-regression-graph` (#3) →
  `1.7-Discussion` (#4) → `git-challenges` (#5) → `render` (#6).
- One owner per section file, so the branches never conflict.
- Commit messages describe one step each, in the imperative
  (e.g. `Remove incomplete patient condition from ANOVA`).

See the section _Our Git workflow strategy_ of the report for details.

## Data

`data/Results.txt` comes from the course Moodle page (see the _Data sources_ section of
the report).

## License

Code under the MIT License (see `LICENSE`). Text and figures © the authors, 2026.

# Does Income Explain Plastic Pollution? A Cross-Country Analysis

## What this is

A regression analysis asking one question: **does a country's income level predict how much plastic pollution it generates per person?** This project combines public data on plastic pollution, GDP, and population across ~200 countries to test that relationship statistically, then looks at where Pakistan sits in the pattern.

It was built as a self-directed research project to demonstrate applied statistics skills (regression, hypothesis testing) from my Statistics degree, using real public data end-to-end — from raw CSVs to a tested, interpretable finding.

## Why

Plastic pollution is usually discussed in absolute terms (which countries produce the most waste), which mostly just reflects population size. I wanted to know whether income — not just population — shapes how much plastic pollution a country generates *per capita*, and where Pakistan falls relative to peer countries. This question also connects to a beach clean-up drive I organized, which drew 3,000+ students and sparked my interest in the data behind the environmental story.

## Data

- **Plastic pollution**: Our World in Data's plastic pollution dataset (Cottom et al. 2024, Nature — SPOT model), 2020 snapshot. Includes waste generation, collection coverage, plastic debris/burn emissions, and per-capita metrics.
- **GDP per capita**: Our World in Data / World Bank, 2020.
- **Population**: Our World in Data, 2020.

All three datasets were merged on country name for the year 2020, resulting in **204 matched countries**.

## Method

1. Cleaned and merged the three datasets on country (`Entity`) and year (2020).
2. **First regression**: `total plastic pollution ~ GDP per capita`
   - Not significant (R² = 0.007, Prob F-statistic = 0.249).
   - This made sense on reflection: total pollution is driven mostly by population size, not income — a large poor country and a large rich country can both produce a lot of *total* waste for different reasons.
3. Recalculated the outcome as **pollution per capita** (dividing total pollution by population) to remove the population confound.
4. **Second regression**: `pollution per capita ~ GDP per capita`
   - This is the model the findings below are based on.

## Findings

- **Higher-income countries generate substantially less plastic pollution per capita.**
- Coefficient on GDP per capita: **-1.8e-07** (negative — pollution per capita falls as income rises)
- **p < 0.001** (highly statistically significant)
- **R² = 0.505** — income alone explains about half of the cross-country variation in plastic pollution per capita

**Where Pakistan sits**

Pakistan sits close to where the overall trend would predict for a country at its income level. At a GDP per capita of $5,135, Pakistan's plastic pollution per capita (0.0109) is nearly identical to Bangladesh's (0.0105 at $7,015) despite Bangladesh's notably higher income — both far below Nigeria (0.0165 at $7,664), a country with a similar income level to Bangladesh but nearly 60% higher pollution per capita. This suggests Pakistan's pollution burden is broadly in line with, or even slightly better than, what its income level alone would predict, while Nigeria stands out as a clear outlier above the trend line.

## Limitations

- This is a **cross-sectional** analysis (one year, 2020) — it shows a strong association, not causation. Income could reduce pollution through better waste infrastructure, or a third factor (e.g., regulation, urbanization) could drive both.
- The plastic pollution dataset relies on modeled estimates (the SPOT model), not direct measurement in every country — some uncertainty is baked into the input data itself.
- One year of data can't capture trends over time or one-off shocks in any given country.
- R² of 0.505 means roughly half of the variation is still unexplained by income alone — other factors clearly matter too.

## Repo structure

```
/data          raw and merged CSVs (plastic pollution, GDP per capita, population)
/notebooks     plastic_pollution_analysis.ipynb (main analysis)
/output        charts and regression output
```

## Next steps

- Finalize remaining charts (scatter/regression plot of pollution per capita vs. GDP per capita, with Pakistan highlighted — draft already in `/output`)
- Write a 1-2 page plain-language policy brief summarizing the finding
- Publish the repo, then add it as a case study on my portfolio site and CV

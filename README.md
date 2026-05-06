# Cheltenham Festival Predictive Modelling (2015–2024)

This project looks at whether historical horse‑racing data can help predict race outcomes at the Cheltenham Festival. I pulled together ten years of results, cleaned and reshaped everything in Power Query, built a set of engineered features in Excel, and then tested a simple logistic regression model to see what actually matters.

The aim wasn’t to build a betting tool — just to understand which variables consistently show predictive value and to put together a transparent, reproducible workflow.

---

## Overview

The main question I wanted to answer was:

**Can past performance data (ratings, going, trainer/jockey records, weight, age, etc.) tell us anything useful about who wins at Cheltenham?**

To explore that, I built an end‑to‑end pipeline:

- ETL in **Power Query**  
- Feature engineering in **Excel**  
- Model validation in **Python**  
- Visual exploration and dashboards in **Power BI**

Everything in the repo is structured so the process can be followed from raw data to final outputs.

---

## Data & Features

The dataset covers all Festival races from 2015–2024. After cleaning and merging, I created a set of features that seemed most relevant for jump racing:

- OR differential vs field median  
- Trainer and jockey strike rates (5‑year rolling)  
- Going match score  
- Weight above minimum  
- Age grouping  
- Class change from previous run  

These were chosen because they’re commonly referenced by analysts and easy to calculate consistently.

---

## Modelling

I kept the modelling deliberately simple: a binary logistic regression (win vs non‑win).  
The idea was to test whether the engineered features actually carry signal, not to chase accuracy with complex models.

**Results:**

- Accuracy: ~61% (baseline ~50%)  
- AUC‑ROC: 0.67  
- Precision/Recall for the win class both mid‑50s  

Python was used to double‑check the coefficients and ensure the Excel Solver version wasn’t doing anything odd.

---

## Dashboards

The Power BI report includes:

- OR distribution and going patterns  
- Trainer performance heatmaps  
- A simple scorecard showing predicted probabilities  
- Festival‑level KPIs  

These are mainly for exploring the data and spotting patterns rather than making predictions.

---

## Repo Structure


---

## Limitations

A few things worth noting:

- Cheltenham has small sample sizes, so noise is unavoidable  
- Trainer/jockey variables can introduce bias toward big yards  
- Going descriptions aren’t perfectly standardised  
- Logistic regression is limited, but good enough for testing feature value  

This is more of a research exercise than a production model.

---

## Future Work

- Add Irish trial races to improve context  
- Try tree‑based models to see if non‑linear effects matter  
- Build a small Streamlit app for scenario testing  
- Automate data updates via the Racing Post API (if feasible)

---

## References

BHA Open Data, Racing Post results archive, and a few academic papers on sports analytics and data bias.


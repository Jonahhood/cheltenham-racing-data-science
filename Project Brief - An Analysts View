# Evaluating Predictive Trends in Horse Racing: Cheltenham Festival (2015–2024)

A reproducible data science pipeline for modelling race outcomes at the Cheltenham Festival using historical performance variables, engineered features, and logistic regression.  
This project combines Power Query ETL, Excel feature engineering, Python validation, and Power BI dashboards to explore whether historical race and horse attributes can meaningfully predict winners.

---

## Project Overview

This project investigates the research question:

**To what extent can historical race and horse performance variables be used to predict race outcomes at the Cheltenham Festival?**

Using ten years of publicly available data (2015–2024), the workflow builds a transparent, end‑to‑end pipeline:

- **ETL in Power Query** (cleaning, merging, type enforcement, going encoding)  
- **Feature engineering in Excel** (OR differential, going match score, trainer/jockey strike rates, class changes, etc.)  
- **Predictive modelling** using logistic regression  
- **Interactive Power BI dashboards** for analysts, modellers, and stakeholders  
- **Python validation** to confirm model reliability

The full pipeline is designed to be reproducible, auditable, and accessible to both technical and non‑technical users.

---

##  Repository Structure


---

##  Tools & Technologies

| Tool | Purpose |
|------|---------|
| **Power Query** | ETL, cleaning, merging, type enforcement |
| **Excel** | Feature engineering, statistical summaries, logistic regression (Solver) |
| **Python (scikit‑learn)** | Model validation and coefficient comparison |
| **Power BI** | Dashboards, visual analytics, KPI summaries |
| **GitHub** | Version control, reproducibility, portfolio hosting |

---

##  Data Engineering

The ETL pipeline includes:

- Header promotion and data type enforcement  
- Null handling (OR imputation, NF flagging)  
- Merging race results with trainer/jockey statistics  
- Going encoding using a 1–6 ordinal scale  
- Creation of seven engineered features, including:  
  - **OR_Differential**  
  - **Trainer_Cheltenham_SR**  
  - **Jockey_Festival_SR**  
  - **Going_Match_Score**  
  - **Weight_Above_Minimum**  
  - **Age_Category**  
  - **Class_Gradient**

All transformations are stored as M‑scripts for full reproducibility.

---

##  Predictive Modelling

A binary logistic regression model (win = 1, non‑win = 0) was trained using seven engineered features.

**Model Performance:**

- **Accuracy:** 61.2% (vs. 50% baseline)  
- **AUC‑ROC:** 0.67  
- **Precision (win):** 0.58  
- **Recall (win):** 0.54  

Python validation (scikit‑learn) reproduced coefficients within ±2%, confirming reliability.

---

##  Dashboards

The Power BI report contains three pages:

1. **Field Analysis** – OR distribution, going heatmap, trainer matrix  
2. **Predictive Scorecard** – model outputs, predicted probabilities  
3. **Festival Summary** – KPIs, year‑on‑year trends  

Screenshots are included in `/images`.

---

##  Ethical Considerations

- All data is publicly available and anonymised at the horse level  
- No personal data is processed (GDPR‑safe)  
- Acknowledged bias: Racing Post data over‑represents major stables  
- Model is a research tool, not a betting advisory system  

---

##  Future Work

- Add live ingestion from Racing Post API  
- Expand dataset to include Irish trials and prep races  
- Explore ensemble models (Random Forest, XGBoost)  
- Deploy a Streamlit app for scenario modelling  

---

##  References

- O'Neil, C. et al. (2022). *Bias in sports analytics: a systematic review.*  
- Wilkinson, M.D. et al. (2016). *FAIR principles for scientific data management.*  
- British Horseracing Authority (2024). Open Data Portal.  
- Racing Post (2024). Results and Statistics Archive.

---

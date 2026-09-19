# HealthConnect Clinic - Data Analytics Track

## AnalystLab Africa Experience Lab Internship Programme

This repository contains my Week 4, Week 5, and Week 6 submissions for the HealthConnect Clinic Experience Lab, part of the AnalystLab Africa internship programme.

## Project Background

HealthConnect Clinic is a fictional healthcare provider facing a high rate of missed patient appointments. The central project question is:

> **How can HealthConnect Clinic use data and AI to reduce missed appointments and improve the patient support experience?**

As part of the Data Analytics track, my role is to explore the appointment dataset, calculate and validate meaningful KPIs, and produce insights and evidence-based recommendations that support HealthConnect's decision-making - including findings that feed directly into the Data Science track's modeling work.

## Repository Structure
```text
├── notebooks/
│   ├── Week4_Initial_Analysis.ipynb
│   ├── Week5_Analytics_Report.ipynb
│   ├── Week6_Advanced_Analytics.ipynb
│   └── Week7_Testing_Refinement.ipynb          # Week 7: KPI validation, refinement, cross-track testing
├── docs/
│   ├── Week4_Project_Summary.md
│   ├── Week5_Project_Summary.md
│   ├── Week6_Project_Summary.md
│   ├── Week7_Project_Summary.md
│   ├── DataScience_Feature_Relevance_Summary.csv
│   ├── chart1_outcome_distribution.png through chart6_combined_risk.png
│   └── chart7_leadtime_continuous.png          # Week 7: refined continuous view
```

---

## Week 4 Progress
- Reviewed dataset structure and confirmed data quality.
- Identified 5 business questions and 5 candidate KPIs.

## Week 5 Progress
- Prepared the data further and explored 6+ key relationships.
- Calculated and interpreted 5 KPIs.
- Built 5 visualizations and produced 5 business insights.

## Week 6 Progress
- Investigated whether the two strongest Week 5 predictors (booking lead time, prior no-show history) compound when combined - confirmed they do (no-show rate ranges from 21.8% to 67.9% depending on the combination).
- Validated the lead-time finding for consistency across all appointment types.
- Validated and **revised** the Week 5 reminder-channel conclusion - SMS is not universally best; effectiveness depends on lead time.
- Collaborated directly with a Data Science intern: reviewed her actual Week 5 baseline model (Logistic Regression, 63% accuracy, 62% recall, 0.68 ROC-AUC) and provided two specific, evidence-backed interaction-feature recommendations not yet in her model.
- Cross-validated my feature relevance findings against her independent statistical testing (t-tests, chi-square) - found full agreement across every candidate feature.
- Produced a validated Feature Relevance Summary, updated to include this cross-validation, as a cross-track integration deliverable.
- Refined business recommendations based on the deeper analysis.

## Week 7 Progress
- Independently re-validated all top KPI calculations using alternative methods - confirmed accurate (48.46% match across two calculation approaches).
- Tested the lead-time finding using quartile-based bands and continuous correlation - confirmed robust across all three methods.
- Refined the Week 6 compounding-risk finding after testing showed the effect, while real, was more modest under correlation analysis than the banded percentages suggested.
- Added a continuous scatter/trend-line visualization for a more complete, honest view of the lead-time relationship.
- Documented a real cross-track testing result: the Data Science intern tested the Week 6 interaction-feature suggestions directly in her model - statistically significant, but did not improve recall - and used this to refine my own reported confidence in the finding's practical strength.

## Key Findings (Updated Through Week 7)

- ~48.5% of all appointments end in a no-show (independently re-confirmed).
- Booking lead time remains the strongest, most reliable predictor - confirmed across three independent testing methods.
- Lead time and prior no-show history compound, but the effect is more modest than initially reported (correlation-based testing shows a smaller gap than the original banded comparison).
- Reminder channel effectiveness depends on lead time - Email performs best for short-notice appointments, SMS for longer lead times.
- Distance to clinic has a moderate effect (46.5% within 5km vs. 54.1% at 15+km).

## Tools Used

- Python (pandas, matplotlib)
- Jupyter Notebook

## Cross-Track Integration

Week 6 involved a real exchange with a Data Science intern building the HealthConnect no-show prediction model. After reviewing her actual baseline results, I provided two specific interaction-feature recommendations (lead-time × prior-no-show, and reminder-channel × lead-time) that were not yet tested in her model. This is documented in `docs/DataScience_Feature_Relevance_Summary.csv` and in the Week 6 notebook.

## Next Steps (Week 8)

- Prepare validated, refined findings for final HealthConnect integration and presentation.
- Present the compounding-risk finding with its refined, accurate magnitude rather than the original overstated version.
- Summarize the project's full analytical journey (Weeks 4-7) for the final presentation.

---
*Part of the AnalystLab Africa Experience Lab Internship Programme.*

---
## Author 
**Angela Iseriehen**
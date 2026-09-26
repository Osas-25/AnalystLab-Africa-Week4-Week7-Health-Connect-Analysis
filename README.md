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
│   ├── Week7_Testing_Refinement.ipynb
│   └── Week8_Final_Analytics_Package.ipynb      # Week 8: final KPIs, dashboard, insights, integration
├── docs/
│   ├── Week4_Project_Summary.md
│   ├── Week5_Project_Summary.md
│   ├── Week6_Project_Summary.md
│   ├── Week7_Project_Summary.md
│   ├── Week8_Final_Summary.md
│   ├── DataScience_Feature_Relevance_Summary.csv
│   ├── Final_KPI_Summary.csv                    # Week 8: official final KPI reference
│   ├── chart1-6, chart7_leadtime_continuous.png  # weekly chart history
│   └── final_chart1-4...png                     # Week 8: final 4-chart dashboard
└── README.md
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

## Week 8 Progress (Final)
- Consolidated four weeks of analysis into a final, validated KPI set and 4-chart dashboard.
- Finalized business insights and recommendations, incorporating all corrections made during Week 7 testing.
- Wrote an executive summary for non-technical HealthConnect stakeholders.
- Documented the complete final integration cycle with the Data Science track - from initial suggestion (Week 6), to real-world testing, to refined analytical conclusions (Week 7-8).
- Prepared final presentation materials, including an individual video presentation.

## Tools Used

- Python (pandas, matplotlib)
- Jupyter Notebook

## Cross-Track Integration

Week 6 involved a real exchange with a Data Science intern building the HealthConnect no-show prediction model. After reviewing her actual baseline results, I provided two specific interaction-feature recommendations (lead-time × prior-no-show, and reminder-channel × lead-time) that were not yet tested in her model. This is documented in `docs/DataScience_Feature_Relevance_Summary.csv` and in the Week 6 notebook.

## Project Summary (Weeks 4-8)

This project took HealthConnect Clinic's fictional appointment data through a full analytical lifecycle: problem definition and initial exploration (Week 4-5), deeper validation and cross-track integration (Week 6), independent testing and correction of an overstated finding (Week 7), and final consolidation into a validated, presentation-ready analytics package (Week 8). Along the way, a real collaboration with the Data Science track demonstrated the value of testing analytical suggestions in practice rather than assuming they translate directly into predictive power.

**Final validated findings:**
- ~48.5% of all appointments end in a no-show.
- Booking lead time is the strongest, most rigorously validated predictor.
- Lead time and prior no-show history compound, though the effect is more modest than early testing suggested.
- Reminder channel effectiveness depends on lead time - no single "best" channel exists.
- Distance to clinic has a moderate, real effect on attendance.

---
*Part of the AnalystLab Africa Experience Lab Internship Programme.*

---
## Author 
**Angela Iseriehen**
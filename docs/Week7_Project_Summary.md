# Week 7 Project Summary - Data Analytics Track

## AnalystLab Africa Experience Lab | HealthConnect Clinic Project

## 1. What I Planned to Test

Building on Week 6's findings, my goal for Week 7 was to validate the accuracy of my top KPI calculations using independent methods, confirm whether the compounding-risk finding held under alternative segmentation approaches, and document the real-world result of the interaction-feature recommendations given to the Data Science track in Week 6.

## 2. What I Actually Tested

- Recalculated the overall no-show rate KPI using an independent method (`.value_counts()` vs `.mean()`).
- Recalculated the lead-time no-show pattern using quartile-based bands instead of the original fixed bands.
- Tested the compounding-risk finding using raw correlation instead of banded groups.
- Reviewed and documented the Data Science track's real-world test of the interaction features I suggested in Week 6.

## 3. Most Important Testing Results

- KPI calculations confirmed accurate (48.46% match across two independent methods).
- The lead-time pattern held consistently across three different measurement approaches (banded, quartile, continuous correlation).
- The compounding-risk effect was confirmed as directionally real, but more modest under correlation testing (0.262 vs 0.286) than the banded percentages from Week 6 suggested (21.8% vs 67.9%).

## 4. Issues or Weaknesses Identified

The Week 6 combined-risk finding, while directionally correct, risked overstating the size of the effect by relying on banded group percentages at the extremes rather than a continuous measure.

## 5. Improvements/Refinements Made

- Added a continuous scatter/trend-line visualization (Chart 7) alongside the original banded chart, giving a more complete and honest picture of the lead-time relationship.
- Refined the interpretation of the compounding-risk finding to describe it as "meaningfully higher risk" rather than citing the banded percentages as precise, guaranteed figures.

## 6. Retesting Results

All three KPI/finding validation tests passed, with one finding (combined risk) refined rather than simply confirmed or rejected - the underlying relationship is real, but its previously reported magnitude was adjusted to be more accurate.

## 7. Track(s) Collaborated With

Data Science.

## 8. What Was Tested Collaboratively

Whether the interaction-feature recommendations I gave the Data Science track in Week 6 (based on the compounding-risk and reminder-channel findings) would improve her model's recall when tested directly in her classification model.

## 9. What Changed as a Result

The Data Science track's test showed the interaction features were statistically significant but did not improve recall - informing both of us that the modeling ceiling is more likely structural (model type/tuning) than feature-related. On my side, this fed directly into refining my own interpretation of the compounding-risk effect's true strength.

## 10. Key Findings or Validation Outcomes

- All KPI calculations are accurate and reproducible.
- The lead-time finding is robust across multiple independent testing methods.
- The compounding-risk finding is real but more modest than initially reported.
- Statistically significant features don't always translate to improved model performance — a useful, generalizable finding for the wider HealthConnect project.

## 11. Major Challenges

Interpreting a cross-track result that didn't confirm the expected outcome (the interaction features not improving recall) in a way that was still useful and honest, rather than treating it as a dead end.

## 12. Important Decisions Made

- Chose to explicitly refine (rather than simply restate) the Week 6 compounding-risk finding once correlation testing showed a more modest effect size - prioritizing accuracy over a more dramatic-sounding headline number.
- Decided to document the Data Science track's "no recall improvement" result honestly as a valid, useful finding rather than omitting it because it didn't confirm the hoped-for outcome.

## 13. Remaining Limitations

- All findings remain correlational, not causal.
- Dataset still lacks socioeconomic, insurance, and clinical-severity data.
- The refined compounding-risk magnitude still relies on the same dataset's limitations (small Cancelled class, missing contextual variables).

## 14. Remaining Issues or Dependencies

The Data Science track's finding that the modeling ceiling may be structural suggests any further analytical support from this track should focus on operational usefulness (e.g., how the clinic could act on findings) rather than searching for more predictive features.

## 15. Contribution to the Overall HealthConnect Project

Provided independently validated, refined findings that prevented an overstated conclusion from persisting in the project, and contributed to a joint, evidence-based understanding (with the Data Science track) of where the project's real opportunities and limitations lie.

## 16. What Must Be Completed Before Week 8

- Finalize recommendations that reflect the refined (not overstated) compounding-risk finding.
- Prepare a clear, presentation-ready summary of validated findings for the Week 8 final integration and presentation stage.
# 5-Minute Demo Outline — Content Refresh Signals and Action Prioritization

## 1. Problem

FlyRank needs a practical way to identify which content pages should be reviewed and refreshed first.

The goal is not to automatically rewrite content, but to create a ranked, human-reviewable action queue that helps prioritize pages using measurable search-performance signals.

## 2. Research Question

Which measurable content and search-performance signals can help identify pages that should be prioritized for a content refresh?

## 3. Method

I used the FlyRank anonymized dataset containing 30,000 rows and 44 columns.

For the analysis, I focused on four signals:

- Days since last update
- Impressions in the last 90 days
- Click-through rate (CTR)
- Average search position

I trained a Random Forest model with 100 estimators and compared a standard random 80/20 split with a client-grouped 80/20 validation split.

## 4. Key Chart

The feature-importance analysis showed:

- Average search position: 0.331056
- CTR: 0.303488
- Days since last update: 0.212908
- Impressions in the last 90 days: 0.152548

This suggests that average search position and CTR were the strongest signals among the four features used by the model.

## 5. Honest Result

The random split produced an accuracy of 1.00, while the client-grouped validation produced an accuracy of 0.9998377.

However, these extremely high scores should not be treated as evidence of genuine predictive performance because the target was directly constructed from the same four features used by the model.

Therefore, the result is better interpreted as a demonstration of the decision workflow rather than proof that the model will predict future performance perfectly.

## 6. Recommendation

Use the model output as a prioritization aid rather than an automatic decision-maker.

Pages can be ranked for human review using measurable signals such as search position, CTR, content age, and impressions. The highest-priority pages can then be reviewed by a person before deciding whether a content refresh is actually needed.

## Closing

The main outcome is a repeatable way to turn existing content and search-performance data into a practical review queue while keeping the final content decision with a human.

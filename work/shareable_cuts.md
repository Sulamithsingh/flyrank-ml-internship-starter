# Shareable Cuts

## Social Post

I explored how existing search-performance signals can help prioritize content for refresh. Using an anonymized FlyRank dataset, I analyzed days since last update, impressions, CTR, and average search position, then built a Random Forest-based prioritization workflow. The results showed that average position and CTR were the strongest signals in the model, while also highlighting an important limitation: because the target was constructed from the same features, the very high validation scores should not be treated as proof of real-world predictive performance. The practical takeaway is to use the model as a human-review prioritization tool rather than an automatic content decision-maker.

## Employer-Facing Summary

I built a content-refresh prioritization workflow using an anonymized FlyRank dataset with 30,000 rows and 44 columns. I analyzed four search-performance signals and trained a Random Forest model to identify which pages could be prioritized for review. The analysis showed that average search position and CTR were the strongest signals, while the validation results also demonstrated why careful interpretation of model performance is important.

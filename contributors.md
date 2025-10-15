# Contributors Guide (Telecom Domain Experts)

Thank you for your interest in improving this Telecom Customer Churn Prediction project. We welcome insights from professionals across the telecom industry—network, product, marketing, care, and finance—to help expand the dataset and enhance model performance and usefulness.

## Goal

- Enrich the dataset with meaningful, privacy-safe features rooted in telecom operations
- Improve prediction quality and business actionability (accuracy, recall for churners, and lift)

## How You Can Help

- **Suggest new features**: Propose attributes we should add to the dataset (examples below).
- **Clarify label definitions**: Ensure the definition of churn reflects real business logic in your context.
- **Share domain constraints**: Typical ranges, seasonality, lag effects, and data availability windows.
- **Highlight actionable signals**: Features that map to interventions (offers, outreach, service fixes).

## Feature Ideas (Starting Points)

- **Product & Contract**
  - Current plan, add-ons, contract type (prepaid/postpaid), contract end date proximity
  - Price changes in last n months, bill shocks, roaming usage
- **Usage & Engagement**
  - Voice/SMS/data usage trends (weekly/monthly deltas), peak-time usage ratio
  - App/portal logins, self-service actions, recharge patterns (prepaid)
- **Quality of Service (QoS)**
  - Network KPIs: dropped-call rate, throughput, latency, outage incidents near the subscriber
  - Device capability vs. network availability (e.g., 5G-capable on 4G-only area)
- **Care & Complaints**
  - Ticket volume, categories (billing, network, activation), resolution time, escalation flags
  - NPS/CSAT scores, recent negative feedback
- **Commercial Signals**
  - ARPU/AMPU, discounting, promo eligibility/usage, competitor offers exposure (if available)
  - Payment behavior: due days, late payments, dunning stage (postpaid)
- **Lifecycle**
  - Tenure buckets, migration events (prepaid→postpaid), number portability requests

Please propose any others you believe are predictive and practical.

## Propose a Feature: Minimal Template

Copy this checklist into a new issue or PR.

- **Feature name**: 
- **Type**: numeric | categorical | boolean | date
- **Definition**: clear business definition and calculation
- **Aggregation window**: e.g., last 30/60/90 days, rolling trend
- **Expected range / categories**: typical values, outlier notes
- **Rationale**: why it may indicate churn risk
- **Data availability**: source system, latency, coverage
- **Privacy & ethics**: any risks and mitigation (aggregation, binning, anonymization)
- **Actionability**: how this signal could guide retention actions

## Data Contribution Guidance

- Do not upload any personally identifiable information (PII) or sensitive data.
- Prefer aggregated/obfuscated samples that preserve patterns but protect privacy.
- If sharing schema only, a small synthetic example is ideal:

```csv
subscriber_id,month,plan_type,voice_minutes,data_gb,complaints,last_outage_days,late_payments_90d,churn
SYN001,2025-08,Postpaid,320,18.4,1,12,0,0
SYN002,2025-08,Prepaid,45,2.1,0,3,NA,1
```

## Model Objectives & Metrics

- Primary: Improve recall and precision on churners while maintaining overall accuracy.
- Secondary: Stability across time (backtesting) and fairness across segments.
- We select thresholds based on validation; added features should help separability and calibration.

## How to Contribute

- **Open an Issue**: Describe your idea using the template above.
- **Submit a PR**: Add feature engineering code, documentation, and synthetic examples.
- **Discussion**: Use issues to discuss feasibility, measurement, and actionability.

## Code Touchpoints

- `BEST_MODEL.ipynb`: main notebook to add features and evaluate impact
- `app.py`: mirrors training-time features for inference—keep it in sync

## Recognition

We’ll acknowledge meaningful contributions (with your permission) in this file and release notes. Thank you for helping bridge domain expertise and ML to reduce churn.

## Contact

If you prefer to share insights privately, please reach out directly:

- Email: <asdhoul004@gmail.com>
- LinkedIn: <https://www.linkedin.com/in/arvinder004>
- Contact: +91 84359 67741

Kindly include "Telecom Churn Project" in the subject/message so we can prioritize your note.



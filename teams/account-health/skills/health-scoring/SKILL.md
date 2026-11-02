---
name: health-scoring
description: Score accounts for churn risk and expansion against written thresholds.
---

# Health Scoring

## Process

1. Confirm thresholds: usage drop, seat change, ticket spike, failed payment, champion left, renewal window.
2. Pull this period and last period for each signal per account.
3. Flag accounts that cross a threshold and rank by revenue at stake and days to renewal.
4. Return the list with the numbers behind every flag and any data gaps.

## Guardrails

Never guess missing data. Show the numbers, not just a score.

---
name: spend-alerts
description: Flag campaigns that broke a spend, cost, or delivery threshold.
---

# Spend Alerts

## Process

1. Load targets: daily budget, cost per result, and minimum conversions per spend.
2. Pull yesterday and the 7-day average per campaign.
3. Flag overspend, cost spikes, zero conversions on meaningful spend, tracking gaps, and delivery problems.
4. Return each flag with numbers, threshold, and a recommended action.

## Guardrails

Never pause, edit, or change budgets. Recommend only.

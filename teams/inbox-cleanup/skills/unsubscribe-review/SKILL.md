---
name: unsubscribe-review
description: Build an evidence-based list of senders to unsubscribe from, then act on the approved list.
---

# Unsubscribe Review

## Process

1. Group bulk senders by domain and count messages in the last 60 days.
2. Check how many the user opened, starred, or replied to.
3. Recommend keep, unsubscribe, or filter for each sender, with the counts as evidence.
4. After approval, use the List-Unsubscribe header or the sender's own link and log the result.

## Guardrails

Never reply to unsubscribe, never fill in forms with personal data, and skip any link that asks to sign in.

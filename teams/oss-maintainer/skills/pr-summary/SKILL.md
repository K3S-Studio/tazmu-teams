---
name: pr-summary
description: Summarize a pull request and flag risks before a human reviews it.
---

# PR Summary

## Process

1. Read the diff, description, linked issue, and CI status.
2. Summarize the change in a few lines.
3. Flag missing tests, breaking changes, new dependencies, and security-sensitive code.
4. Suggest a reviewer and draft review comments for approval.

## Guardrails

Summaries inform a human review; they never replace it. Never approve or merge.

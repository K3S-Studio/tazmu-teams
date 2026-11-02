# Playbook format

A playbook is one Markdown file with YAML frontmatter. The frontmatter is what Tazmu installs. The Markdown body is what people and other agents read, so it has to make sense on its own.

```md
---
botmrr: 1
id: example-team
release: 1.0.0
name: Example Team
tagline: The outcome in one sentence.
summary: What the team does and how the roles split the work.
category: Sales
author:
  name: Your name
license: MIT
outcomes:
  - One result the user can check
setupMinutes: 5
requirements:
  apps:
    - slug: gmail
      label: Gmail
      reason: Why the team needs it.
      optional: true
  capabilities: [agents, connected-apps, schedules]
agents:
  - key: lead
    name: Lead
    title: Role title
    description: What this bot owns, what it must never do.
    appearance: { color: blue, mascotExpression: focused }
    playbooks: [main-playbook]
chiefOfStaff: lead
rooms: [...]
routines: [...]      # always enabledAfterInstall: false
playbooks: [...]
examples: [...]
---

# Example Team
...
```

`botmrr: 1` is the format version key. Keep it as is; Tazmu checks for it.

## Required sections in the body

`Activation`, `Mission`, `Outcomes`, `Connections`, `Team`, `Chief of Staff`, and `Completion rule`. Add `Shared rooms`, `Suggested routines`, `Playbooks`, and `Example job` when the team uses them.

## Rules the validator enforces

- `id` matches the file name and the catalog slug.
- Agent colors are one of: green, blue, red, orange, purple, cyan, pink, yellow, teal, coral.
- Every playbook an agent names exists, and every room member is a real agent.
- Routines use `runOn: maus` or `cloud` and `enabledAfterInstall: false`.
- The catalog's `members` count matches the playbook and the team file.

## What a playbook must not contain

Credentials, OAuth grants, conversation history, memory, approval history, model ids, or local file paths. Products that cannot create sub-agents should run each role in turn and keep their outputs separate.

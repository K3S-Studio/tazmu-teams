# Contributing a team

## Before you open a pull request

1. Copy an existing file under `packages/` and keep it as plain `.md`.
2. Aim the team at one outcome a user can check. Give each bot a distinct job.
3. Make the Markdown body complete enough that any agent can run the team from it alone.
4. Keep the frontmatter and the body in sync.
5. Say in plain words why each app is needed, and mark optional apps.
6. Leave every routine paused (`enabledAfterInstall: false`).
7. Add the team to `catalog.json` and add `teams/<slug>/` with `team.mausteam.json`, `README.md`, and one `skills/<key>/SKILL.md` per playbook.
8. Run `npm ci && npm test`.

## Safety rules

Pull requests are rejected if they include:

- API keys, tokens, cookies, personal data, or example secrets
- executable files or encoded payloads
- instructions to skip approvals or hide actions from the user
- destructive actions without explicit confirmation
- claims of official affiliation with a company you don't represent

The Activation section must say what needs human approval. Playbooks should separate evidence from inference and state their inputs, steps, output, and guardrails.

## Review

Maintainers may edit names, descriptions, formatting, and guardrails. Being listed does not mean K3 Studio endorses every result a team produces.

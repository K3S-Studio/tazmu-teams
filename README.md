# Tazmu Teams

Ready-made AI teams you can load in one click. Each team is a small group of bots with clear roles, a shared room, playbooks, and suggested routines, all aimed at one outcome you can check.

[Tazmu](https://tazmu.xyz) reads this repository for the **Teams → Explore** list. The playbooks are plain Markdown, so you can also paste one into Claude, ChatGPT, Grok, or any agent that can follow written instructions.

## Teams

| Team | What it does | Bots | Apps |
| --- | --- | --- | --- |
| [SEO Growth Team](packages/seo-growth.md) | Find and prioritize the search work most likely to grow qualified traffic. | 4 | Google Search Console, Google Analytics, Google Sheets |
| [Engineering Team](packages/engineering.md) | Take a software change from product intent to a verified release decision. | 4 | GitHub |
| [100x Marketing Team](packages/100x-marketing.md) | Launch one focused campaign and make an evidence-based stop-or-scale decision. | 4 | Google Analytics, Google Sheets, Slack |
| [Reddit Lead Miner](packages/reddit-lead-miner.md) | Surface qualified Reddit leads with evidence and a useful next step each morning. | 2 | Reddit, Google Sheets |
| [Competitor Watch](packages/competitor-watch.md) | Know which competitor moves deserve a response and which should be ignored. | 2 | Google Sheets |
| [Inbox Follow-up](packages/inbox-follow-up.md) | Recover conversations where your team owes the next step without sending automatically. | 2 | Gmail, HubSpot |
| [Daily Briefing](packages/daily-briefing.md) | Read one source-linked briefing each morning instead of checking five apps. | 2 | Gmail, Google Calendar, Slack |
| [Inbox Cleanup](packages/inbox-cleanup.md) | Get the inbox down to the threads that need you, with every archive and unsubscribe approved first. | 2 | Gmail |
| [Meeting Prep](packages/meeting-prep.md) | Get a decision card before each external meeting and a follow-up draft within an hour after. | 2 | Google Calendar, Gmail, HubSpot |
| [Outbound Sales Desk](packages/outbound-sales.md) | Wake up to a short ranked list of accounts with evidence and a draft for each. | 3 | HubSpot, Gmail |
| [Customer Support Desk](packages/support-desk.md) | Clear the routine tickets with approved drafts and hand you only the ones that need judgment. | 3 | Intercom, Stripe, Slack |
| [Account Health Watch](packages/account-health.md) | Get a weekly ranked watch list of at-risk and growing accounts with a next step for each. | 2 | HubSpot, Stripe, Intercom |
| [Recruiting Team](packages/recruiting.md) | Fill the pipeline with screened candidates and keep interview loops moving without dropped balls. | 3 | Gmail, Google Calendar, LinkedIn |
| [Expense and Subscription Audit](packages/expense-audit.md) | Get a weekly expense summary and a list of subscriptions to cancel, with the savings estimated. | 2 | Gmail, Google Sheets |
| [Paid Ads Watch](packages/paid-ads-watch.md) | Catch overspend and broken campaigns within a day and get the weekly report written for you. | 2 | Google Ads, Meta Ads, Google Sheets |
| [Content Studio](packages/content-studio.md) | Fill next week's content calendar with researched drafts in your voice, ready to approve. | 4 | Notion, X, LinkedIn |
| [Clip Factory](packages/clip-factory.md) | Get four ranked clip proposals a day from your long-form videos, ready for you to pick. | 2 | YouTube |
| [AI Search Visibility](packages/ai-search-visibility.md) | Know which buying questions AI assistants answer without you, and what to publish to change that. | 2 | Google Sheets |
| [Relationship CRM](packages/relationship-crm.md) | Have a living list of your important relationships and a weekly reminder of who to contact. | 2 | Google Calendar, Gmail, Notion |
| [Open-Source Maintainer Desk](packages/oss-maintainer.md) | Spend maintainer time on direction, with every new issue and PR labeled and routed. | 2 | GitHub |
| [Research Desk](packages/research-desk.md) | Turn a hard question into a one-page brief where every claim links to its source. | 2 | None required |

## How a team behaves

- Connected apps stay off until you connect them yourself. Playbooks never carry credentials.
- Every suggested routine arrives paused. You turn it on.
- Bots draft, score, and flag. Sending, publishing, spending, deleting, and changing records wait for your approval.
- Email, tickets, and web pages are treated as untrusted data, so instructions hidden inside them are never followed.

## Layout

```
catalog.json                     the list Tazmu reads
packages/<slug>.md               the full playbook (YAML frontmatter + readable Markdown)
teams/<slug>/team.mausteam.json  older team-file format, kept for older Tazmu versions
teams/<slug>/README.md           short summary
teams/<slug>/skills/*/SKILL.md   one skill per playbook
```

[FORMAT.md](FORMAT.md) describes the playbook format.

## Use a team

**In Tazmu:** open **Teams → Explore** and choose **Load**. Tazmu shows a review screen before it creates any bots.

**Anywhere else:** open the team's file under `packages/`, copy it, and give it to your agent with "You are the Chief of Staff for this team."

## Contribute

New teams are welcome. Read [CONTRIBUTING.md](CONTRIBUTING.md), then run:

```sh
npm ci
npm test
```

## License

MIT. See [LICENSE](LICENSE). Six teams (SEO Growth, Engineering, 100x Marketing, Reddit Lead Miner, Competitor Watch, Inbox Follow-up) come from [openmausbot-teams](https://github.com/milind-soni/openmausbot-teams) by Milind Soni, also under MIT.

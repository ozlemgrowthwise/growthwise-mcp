# GrowthWise MCP

**Your company's growth brain, inside your Claude.**

GrowthWise connects to your growth data (Google Analytics 4, Search Console, Google Tag Manager, Google Ads, LinkedIn Ads, HubSpot), tells you how far the numbers can be trusted, and turns them into a few moves every Monday. This MCP server lets Claude read that context, so its answers are about *your* company instead of generic advice, and on paid plans add ideas, notes and tasks or approve the plan.

- Server address: `https://app.growthwisetech.com/mcp`
- Transport: Streamable HTTP
- Sign-in: OAuth, with your GrowthWise account
- Access: seven read tools on every plan; five actions inside GrowthWise on paid plans. Nothing is ever written to your Analytics, ad or other accounts.

The server is hosted by GrowthWise. There is nothing to install or run.

## Connect

You need a GrowthWise account with Google Analytics 4 connected. [Start with a free growth audit](https://app.growthwisetech.com/audit); it takes about two minutes.

**Claude (web or desktop)**

1. Open **Settings → Connectors → Add custom connector**.
2. Paste `https://app.growthwisetech.com/mcp`.
3. Sign in with your GrowthWise account and allow access.

ChatGPT access is planned.

Then ask:

- "What's my Health Score, and what is the weakest check?"
- "What should we focus on this week?"
- "What did we already try, and what happened two weeks later?"

## Tools

The tools below only read, and answer for the signed-in person's own company.

| Tool | What Claude gets | Plan |
| --- | --- | --- |
| `get_health_score` | Health Score (0-100), each measurement check with its points, and the weakest check | Free |
| `get_this_week` | This week's sprint: approval status, summary, tasks with owner, priority and confidence, and the four-week content plan (what to write, for which search, and why) | Free |
| `get_company_profile` | Main goal, ideal customer, target metric, and the team's notes (decisions, constraints, things already tried) | Founder and Team |
| `query_metrics` | Sessions, users, conversions, organic clicks and impressions for the last 7 or 28 days against the period before | Founder and Team |
| `get_channel_mix` | Traffic and conversions by channel, and ad results where ad accounts are connected | Founder and Team |
| `get_history` | Finished tasks, the team's rating, and what the numbers did two weeks later | Founder and Team |
| `get_results` | Health Score over time, tasks finished, sprint completion, and then-versus-now traffic and conversions | Founder and Team |

Accounts in their free first month can use every tool.

### Actions (version 2)

Claude can also act inside GrowthWise, for the signed-in person and within their role. Actions change GrowthWise only; nothing is written to your Analytics, ad or other accounts.

| Tool | What it does | Plan |
| --- | --- | --- |
| `add_idea` | Adds an idea for the team to vote on; GrowthWise scores it against your data | Team |
| `add_task` | Adds a task to this week's Task Dashboard; GrowthWise writes the full card | Founder and Team |
| `add_note` | Saves lasting context (a decision, a constraint, something already tried) for every later plan and answer | Founder and Team |
| `approve_plan` | Approves this week's draft plan; only the person who approves plans for the company | Founder and Team |
| `refresh_plan` | Rebuilds this week's plan from fresh data; counts against the daily limit | Founder and Team |

## What it does not do

- It never writes to your connected accounts: no changes in Analytics, Tag Manager, ad accounts or your CRM. Actions only change GrowthWise itself, within your role, and adding tasks and ideas is limited to 20 a day.
- It does not compute numbers with a model. Claude receives the same figures the GrowthWise app shows.
- The two-week readings are before/after numbers, not proof of cause.

## Privacy and security

- You sign in on GrowthWise's own sign-in page; Claude never sees your password.
- Each tool reads only the company of the person who signed in.
- Tokens for your connected tools are stored encrypted and are never sent to Claude.
- The first connection is written to your account's audit log.
- Disconnect any time from Claude's connector settings.

[Privacy Policy](https://growthwisetech.com/privacy) · [Terms of Service](https://growthwisetech.com/terms)

## Questions

Write to ozlem@growthwise.tech or [book a 30-minute call](https://calendar.app.google/f51hcpQyKEWna6tC9).

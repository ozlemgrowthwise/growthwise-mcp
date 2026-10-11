GrowthWise MCP
Your company's growth brain, inside your Claude.

GrowthWise connects to your growth data (Google Analytics 4, Search Console, Google Ads, LinkedIn Ads), tells you how far the numbers can be trusted, and turns them into a few moves every Monday. This MCP server lets Claude read that context, so its answers are about your company instead of generic advice.

Server address: https://app.growthwisetech.com/mcp
Transport: Streamable HTTP
Sign-in: OAuth, with your GrowthWise account
Access: read-only
The server is hosted by GrowthWise. There is nothing to install or run.

Connect
You need a GrowthWise account with Google Analytics 4 connected. Start with a free growth audit; it takes about two minutes.

Claude (web or desktop)

Open Settings → Connectors → Add custom connector.
Paste https://app.growthwisetech.com/mcp.
Sign in with your GrowthWise account and allow access.
ChatGPT access is planned.

Then ask:

"What's my Health Score, and what is the weakest check?"
"What should we focus on this week?"
"What did we already try, and what happened two weeks later?"
Tools
All tools are read-only and answer for the signed-in person's own company.

Tool	What Claude gets	Plan
get_health_score	Health Score (0-100), each measurement check with its points, and the weakest check	Free
get_this_week	This week's sprint: approval status, summary, tasks with owner, priority and confidence, and the four-week content plan (what to write, for which search, and why)	Free
get_company_profile	Main goal, ideal customer, target metric, and the team's notes (decisions, constraints, things already tried)	Founder and Team
query_metrics	Sessions, users, conversions, organic clicks and impressions for the last 7 or 28 days against the period before	Founder and Team
get_channel_mix	Traffic and conversions by channel, and ad results where ad accounts are connected	Founder and Team
get_history	Finished tasks, the team's rating, and what the numbers did two weeks later	Founder and Team
get_results	Health Score over time, tasks finished, sprint completion, and then-versus-now traffic and conversions	Founder and Team
Accounts in their free first month can use every tool.

What it does not do
It does not change anything: no tasks, no approvals, no ad accounts.
It does not compute numbers with a model. Claude receives the same figures the GrowthWise app shows.
The two-week readings are before/after numbers, not proof of cause.
Privacy and security
You sign in on GrowthWise's own sign-in page; Claude never sees your password.
Each tool reads only the company of the person who signed in.
Tokens for your connected tools are stored encrypted and are never sent to Claude.
The first connection is written to your account's audit log.
Disconnect any time from Claude's connector settings.
Privacy Policy · Terms of Service

Questions
Write to ozlem@growthwise.tech or book a 20-minute call.

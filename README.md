# Creator Program OS

Tools and a playbook for running influencer and KOL programs as a measurable growth channel.

**[Open the KOL Finder](https://ciport78.github.io/creator-program-os/)**: load your creator list, filter it, and rank it with a score you control.

## 1. KOL Finder

A single-page tool that turns a raw creator list into a ranked shortlist.

- **Bring any list.** Upload a CSV or Excel file. The header row and columns are detected automatically, so exports from tools such as Cookie3, Kaito, Modash, HypeAuditor or your own sheets work without reformatting.
- **Filter.** Filter by platform, follower tier, creator type, niche, region, country, language, account type and outreach status, plus min / max ranges on every metric in the file.
- **Score.** A weighted 0 to 100 score built only from the signals your file contains. Adjust the weights live.
- **Flag.** Creators are auto-flagged for low brand safety, inflated engagement, views under 1% of followers, high farmer / bot scores, or an "avoid" status.
- **Decide.** Every creator gets a call (Priority, Test, Hold or Pass) that feeds the continue / pause / scale logic in the playbook.
- **Export.** Download the filtered shortlist as CSV.
- **Private.** Runs entirely in the browser. Your file never leaves your device.

### Scoring signals

| Signal | Built from | Method |
|--------|-----------|--------|
| Audience fit | `audience_fit` (1 to 5) | Your manual rating |
| Influence quality | `smart_followers`, `kol_score` | Percentile within the loaded list |
| Topic relevance | `mindshare`, `signal` | Percentile within the loaded list |
| Engagement | `engagement_rate` | 0 to 6% scaled |
| Cost efficiency | `rate_usd` ÷ `avg_views` | Lower CPM scores higher |
| Authenticity | `farmer_score` | Lower is better |
| Content quality | `content_quality` (1 to 5) | Your manual rating |
| Brand safety | `brand_safety` (1 to 5) | Your manual rating |

Signals with no matching column are skipped, so a file with only followers and smart followers still ranks cleanly.

### Recognised columns

Only `name` or `handle` is required. Common alternative headers are accepted (for example "Display Name", "Profile URL", "Subscribers", "Outreach Flag", "Creator Types").

`name, handle, url, platform, niche, creator_types, account_type, status, region, country, language, followers, avg_views, engagement_rate, smart_followers, kol_score, farmer_score, signal, mindshare, audience_fit, content_quality, brand_safety, rate_usd, contact, notes, bio`

Use **Download template** in the tool, or start from [`data/sample-kols.csv`](data/sample-kols.csv) (fictional creators).

## 2. Creator program playbook

A zero-to-one operating plan, written to be used on day 1 and refined with data by day 90.

| # | Section | What it answers |
|---|---------|-----------------|
| 1 | [Strategy and creator tiers](docs/01-strategy-and-tiers.md) | Who we work with, by segment and tier, and how budget splits |
| 2 | [Sourcing and vetting](docs/02-sourcing-and-vetting.md) | How we find creators and decide who is worth paying |
| 3 | [Deal structures](docs/03-deal-structures.md) | Flat fee, performance hybrid, ambassador, affiliate, usage rights |
| 4 | [Brief template](docs/04-brief-template.md) | A brief that protects the brand and keeps the creator's voice |
| 5 | [Measurement framework](docs/05-measurement.md) | UTMs, promo codes, holdouts, lift, and continue / pause / scale rules |
| 6 | [90-day rollout](docs/06-90-day-rollout.md) | What gets built, tested and decided, month by month |

### Principles

- **Segment first, platform second.** Different buyers need different creators, briefs and KPIs.
- **Every dollar has a hypothesis.** Each deal states what it should drive and how we will know.
- **Pay for proof, then scale.** Test small, decide fast, concentrate spend on top performers.
- **Authenticity is a performance lever.** Briefs set guardrails, not scripts.
- **Imperfect attribution is still decision-grade.** Triangulate codes, links, lift and halo, then make the call.

## Run locally

Open `index.html` in any browser. No build step, no install.

*All sample data in this repo is fictional.*

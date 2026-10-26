# 5. Measurement framework

**Principle:** treat influencer spend like paid media. The question is never "how many views?" It is "what would not have happened without this creator?"

## Measurement stack

Use four layers. No single layer is complete. Together they are decision-grade.

| Layer | What it captures | Limitation |
|-------|------------------|------------|
| **1. Tracked links (UTMs)** | Direct click-through sign-ups | Misses viewers who search the brand later |
| **2. Promo codes** | Conversions from viewers who did not click | Codes leak to coupon sites |
| **3. Post-sign-up survey** | "Where did you hear about us?" with creator names | Self-reported, noisy |
| **4. Lift and halo** | Incremental impact beyond tracked conversions | Needs volume and clean baselines |

## 1. UTM convention

```
utm_source   = creator handle        (e.g. jane_edits)
utm_medium   = influencer
utm_campaign = campaign_yyyymm       (e.g. spring_launch_202611)
utm_content  = format_platform       (e.g. integration_youtube)
```

Rules: lowercase only, no spaces, one link per creator per deliverable, logged in the tracker before the brief is sent.

## 2. Promo codes

- One unique code per creator: `[HANDLE][OFFER]` (e.g. `JANE20`)
- Offer value consistent within a tier to avoid creators competing on discount
- Monitor coupon-site leakage weekly and rotate codes if needed

## 3. Survey attribution

Add an optional free-text and dropdown field at sign-up. Use it to estimate the **untracked multiplier**: total survey-attributed sign-ups ÷ tracked sign-ups per creator. Apply that multiplier as a range, not a point estimate.

## 4. Incrementality

### Geo or audience holdouts
For larger campaigns, run creators in selected markets or languages and hold out comparable ones. Compare sign-up lift vs baseline and vs holdout.

### Time-based lift
For each major post, compare branded search, direct traffic and sign-ups in the 72 hours after posting against the same window in the prior 2 weeks, adjusted for seasonality and other launches.

### Halo
Feed creator activity into a halo or media-mix model so organic, search and direct uplift are credited, not just last click.

## Core metrics

| Metric | Formula | Use |
|--------|---------|-----|
| Effective CPM | Fee ÷ views × 1,000 | Reach efficiency |
| Cost per tracked sign-up | Fee ÷ tracked sign-ups | Floor-level efficiency |
| Cost per incremental paid user | Fee ÷ (estimated incremental paid users) | **Primary decision metric** |
| Paid conversion rate | Paid users ÷ sign-ups from creator | Audience quality |
| 90-day retention | Paid users active at day 90 ÷ paid users | Long-term value of the audience |
| Payback period | Fee ÷ monthly revenue from creator cohort | Budget pacing |

## Continue / pause / scale rules

Review every creator after each campaign, and every agency monthly. Compare against the segment's target cost per incremental paid user (CPIU).

| Decision | Criteria | Action |
|----------|----------|--------|
| **Scale** | CPIU ≤ target **and** retention at or above segment average | Move to ambassador or larger package, test whitelisting |
| **Continue** | CPIU within 1.3x target, or strong lift signal with weak direct tracking | Rebook, iterate on brief or format |
| **Iterate** | CPIU 1.3 to 2x target, good engagement quality | One more test with a changed hook, format or offer |
| **Pause** | CPIU over 2x target after 2 tests, or poor retention | Stop paid work, keep in affiliate pool |

**Judgment rule for imperfect data:** if tracked metrics and lift disagree, weigh by sample size. A creator with 3 strong lift readings and weak code usage is likely driving untracked conversions. Do not cut them on last-click data alone.

## Reporting cadence

- **Weekly:** live campaigns, spend pacing, early signals
- **Monthly:** creator scorecard, budget reallocation, rate card updates
- **Quarterly:** channel-level incrementality, segment performance, program roadmap

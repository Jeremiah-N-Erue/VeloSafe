# How to view and use your VeloSafe waitlist data

You have three places where data lives, and each does a different job. Read this once — it'll save you weeks of confusion.

---

## The three layers

### Layer 1 · Formspree (the inbox)

Every submission lands in your Formspree dashboard first. This is where raw data arrives.

**To view it:**
1. Go to `formspree.io` and log in
2. Click your form name (you'll have two — `rider-waitlist` and `driver-applications`)
3. Click the "Submissions" tab

**What you can do here:**
- See every submission in real time
- Filter by date, keyword, spam status
- Export as CSV (useful for quick analysis)
- Get email notifications on each submission

**What you shouldn't do here:** treat it as your working database. Formspree is a catcher, not a CRM.

---

### Layer 2 · Google Sheets (your working database)

This is where you actually *work* with your data — tagging leads, updating status, analysing trends.

**The workbook has three tabs:**

1. **Dashboard** — headline metrics and breakdowns. Auto-updates from the other two sheets. This is the first screen you show investors.

2. **Riders** — one row per rider submission with 12 columns including waitlist data, status tracking (New → Contacted → Confirmed → Early access), and queue position.

3. **Drivers** — one row per driver application with 18 columns including compliance score (0–6 based on documents held), verification date, and status tracking (Under review → Verification scheduled → Verified → Founding cohort).

**To connect Formspree → Google Sheets automatically:**

Option A — Formspree's native integration (easiest):
1. In Formspree, open your form settings
2. Click Integrations → Google Sheets
3. Connect your Google account and pick a spreadsheet
4. Formspree will create a tab and append every new submission as a new row

Option B — Zapier (more control):
1. Create a Zap: Formspree (trigger) → Google Sheets (action)
2. Map each form field to a column in your tracker
3. Test, then activate

Option A is the right call for pre-seed stage. It's free and takes 5 minutes.

---

### Layer 3 · Dashboards and charts (what you show others)

When it's time to share with investors, co-founders, or potential hires, you don't send a raw spreadsheet. You export a clean summary.

**For investors:** screenshot the Dashboard tab. The KPI strip plus the breakdowns tell a complete story in one page — "We have X riders, Y drivers, here's where they live, here's what they care about."

**For your ops team:** share the Google Sheets file with edit access. Filter the Drivers tab by "Verification scheduled" to see who needs a call today.

**For pitch decks:** use the percentages from each breakdown. "61% of our driver applicants cite commission as their top switching reason" is a strong deck line — it comes straight from your data.

---

## What to review every week

A 15-minute Monday morning check on these six numbers:

| # | Metric | What to watch for |
|---|--------|-------------------|
| 1 | Total riders | Is the signup curve accelerating or flat? |
| 2 | Total drivers | Are you maintaining at least a 1:5 driver-to-rider ratio? |
| 3 | Referral signup count | Under 10% after month 1 means the referral mechanic isn't landing |
| 4 | Average compliance score | Under 4 means tighten your driver marketing message |
| 5 | Top safety priority | Stable = you know your product roadmap. Changing weekly = segment by date |
| 6 | Top switching reason (drivers) | Whatever wins here should lead your driver ads and pitch |

---

## What to review every month

**Area concentration** — which Lagos LGAs have the highest demand? That's where you launch first. If 40% of signups are Lekki–VI–Ikoyi, your MVP launches there.

**Competitive displacement pattern** — if Bolt is the #1 current platform for 70% of your signups, your pitch should explicitly compare to Bolt. If it's spread across five platforms, your positioning is "the safer alternative to all of them."

**Conversion rate** — how many people land on the page versus complete the form. Under 15% means the form is too long or the value prop is unclear.

**Cohort retention** — of riders who signed up in Month 1, how many still open your monthly emails by Month 3? This is your real interest signal.

---

## Red flags to watch for

**Growth without intent.** If signups spike but compliance scores drop (drivers) or ride frequency drops (riders), you're attracting the wrong crowd. A channel is cheap but low-quality — cut it.

**Silence from specific areas.** If Lekki is 40% of signups but verified drivers are 90% from the Mainland, supply and demand are in different places. You have a matching problem before you even launch.

**The "I'll wait and see" cluster.** On the driver side, if "Fair treatment & responsive support" is the top switching reason, drivers don't trust platforms generally. Your differentiation will be slower than if they had picked a tangible thing like commission. Adjust timeline expectations.

**Identical submissions from different emails.** Check for signup fraud — it happens especially around referral incentives. If you see the same phone number across submissions, flag and remove.

---

## When to graduate from a spreadsheet

You'll outgrow this setup around 2,000–3,000 signups. At that point, move to:

- **HubSpot free CRM** — for rider list management and email automation
- **Airtable** — if you want database views with a spreadsheet feel
- **Notion** — if your team already uses it for ops

For now, the spreadsheet is exactly right. Don't over-build before you have signal.

---

*Built for VeloSafe Technologies · Lagos 2026*

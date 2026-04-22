# VeloSafe Waitlist Pages

Two-page waitlist system for VeloSafe Technologies — separate flows for riders and drivers, sharing one design system.

---

## Files

| File | Purpose |
|------|---------|
| `styles.css` | Shared design system (brand colours, typography, components) |
| `riders.html` | Rider waitlist form |
| `drivers.html` | Driver application form |
| `community-playbook.md` | WhatsApp group management guide |
| `data-guide.md` | How to view and use your waitlist data |

---

## Setup (5 minutes)

### 1. Create two Formspree forms

Go to [formspree.io](https://formspree.io) and create **two separate forms** — one for riders, one for drivers. Keeping them separate lets you analyse conversion rates independently and route submissions to different tools.

On the free plan you get 50 submissions/month per form. The $10/month Basic plan gives 100/month + file uploads (useful when you start accepting driver document photos).

### 2. Wire the endpoints

In `riders.html`, replace `YOUR_RIDER_FORM_ID`:
```html
<form id="rider-form" action="https://formspree.io/f/YOUR_RIDER_FORM_ID" method="POST">
```

In `drivers.html`, replace `YOUR_DRIVER_FORM_ID`:
```html
<form id="driver-form" action="https://formspree.io/f/YOUR_DRIVER_FORM_ID" method="POST">
```

### 3. Create two WhatsApp groups

Create these before you announce the waitlist:

- **VeloSafe Founding Riders · Lagos**
- **VeloSafe Founding Drivers · Cohort**

Get each group's invite link, then replace `YOUR_RIDER_GROUP_INVITE` in `riders.html` and `YOUR_DRIVER_GROUP_INVITE` in `drivers.html`.

See `community-playbook.md` for group setup, descriptions, moderation rules, and scaling advice. Don't skip it — running these groups badly is worse than not having them.

### 4. Configure Formspree

In each form's settings:

- **Allowed domains** — add your production domain once live
- **Email notifications** — set to `velosafetechnologies@gmail.com`
- **Spam filter** — enable reCAPTCHA

### 5. Deploy

Drop the files into your GitHub Pages repo or any static host. No build step needed.

For clean URLs (`/riders` instead of `/riders.html`), deploy to Netlify — it supports this out of the box for free.

---

## Analytics

Add Google Analytics 4 or Plausible before `</body>` in each HTML file. Key events to track:

- `rider_form_submit` — fired from the success handler in `riders.html`
- `driver_form_submit` — fired from the success handler in `drivers.html`
- `role_toggle_click` — when a user switches between the two forms (high-intent signal)

---

## Data you collect

**From riders:**
- Name, email, phone
- Primary Lagos area
- Current ride-hailing platform (competitive displacement data)
- Ride frequency (LTV signal)
- Top safety concern (product roadmap data)

**From drivers:**
- Name, phone, email, age, home LGA
- Vehicle details (ownership, year, model)
- Years of professional experience
- Compliance documents held (pre-qualification score)
- Current platforms (multi-select)
- Weekly hours available (supply density signal)
- Preferred zone
- Top switching reason (positioning data)

Export monthly to CSV and you have a clean investor-ready dataset.

---

## Brand system

### Colors

| Token | Value | Usage |
|-------|-------|-------|
| `--navy` | `#0B1F3A` | Headers, nav, primary headings |
| `--teal` | `#0D9E75` | CTAs, active states, icons, links |
| `--teal-light` | `#E1F5EE` | Highlighted question backgrounds |
| `--gold` | `#C8892A` | Referral notes, accent stars |
| `--gray-700` | `#3D4F62` | Body text |
| `--gray-400` | `#9EA8B5` | Labels, captions, helper text |
| `--gray-100` | `#EEF0F3` | Borders, dividers |
| `--off-white` | `#F7F8FA` | Page background |

### Typography

| Role | Font | Weight |
|------|------|--------|
| Display / Headings | DM Serif Display | 400 (regular + italic) |
| Body / UI | DM Sans | 300, 400, 500, 600 |

Google Fonts import used in all HTML files:
```
https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:wght@300;400;500;600&display=swap
```

### Logo SVG

The nav logo is an inline SVG shield, matching the landing page icon:
```html
<path d="M12 2L3 7v6c0 5 4 9 9 10 5-1 9-5 9-10V7l-9-5z" stroke="#0D9E75" stroke-width="2" fill="#E1F5EE"/>
<path d="M9 12l2 2 4-4" stroke="#0D9E75" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
```

---

## What to iterate after launch

Watch three metrics in the first 30 days:

1. **Drop-off point** — if users abandon at the strategic question, shorten the form
2. **Referral uptake** — if under 5% of signups come via referral, make the mechanic more prominent or change the reward
3. **Driver compliance rate** — if under 50% of driver applicants tick 4+ compliance boxes, you have an onboarding problem, not a marketing problem

---

*Built for VeloSafe Technologies · Lagos 2026*

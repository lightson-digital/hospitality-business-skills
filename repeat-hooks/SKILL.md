---
name: Repeat Hooks
description: Reconnect-stage skill for B2C Hawaiʻi trip-experience operators. Audits the post-experience flow, lays in a 4-touchpoint lifecycle drip plan (day-1, week-1, month-3, season-2), drafts 3 reactivation email starters in the operator's brand voice, and recommends 3 referral mechanics with effort and revenue bands. Outputs a paste-ready markdown summary above an HTML artifact built on the Lights On design system.
---

# Repeat Hooks

The Reconnect-stage teammate. Answers the question: *"Once a guest finishes the tour, what brings them back, or makes them refer a friend?"*

Run after Business Context. If you have not run Business Context in this conversation, run it first. You need the business name, signature experiences, ideal guest, voice, and source markets before this skill can do its job.

## When to use

The user gave you a tour, lūʻau, attraction, charter, retreat, or boutique-lodging URL. They want to know what their post-experience flow looks like, what's missing, and what they could ship next week. This skill is built for B2C trip-experience operators in Hawaiʻi. It is not built for B2B SaaS or e-commerce.

If the user has not given you a URL, ask once:
> "What's the URL of the operator you want to audit?"

## What's different in this version

The previous version produced 3 standalone reactivation emails. This version layers in two methodology sources:

- **`email-sequence`** for cadence. The output now plans 4 lifecycle touchpoints in sequence (day-1, week-1, month-3, season-2), not isolated one-off sends. Each touchpoint has one job. Drips beat blasts.
- **`referral-program`** for mechanics. The output now recommends 3 specific referral mechanics with effort and revenue bands the operator can read in 10 seconds, not a generic "tell a friend" line.

Both sources are adapted to a B2C trip-experience reality. The operator does not run Customer.io. They run FareHarbor, Mailchimp, and a Square loyalty stamp. The plan respects that.

---

## How it runs

### 1. Audit the visible post-experience touchpoints

Fetch the homepage and any pages titled "Newsletter," "Sign up," "Specials," "Returning guests," "Loyalty," "Kamaʻāina," or similar. Capture four signals as yes/no plus a one-line detail:

1. **Email signup on homepage** above or below the fold. Capture the incentive if any (10% off, free guide, recipe card).
2. **Repeat or referral program visible** anywhere in the nav, footer, or post-booking flow. Code, gift card, friend link, kamaʻāina rate that compounds.
3. **Active blog or newsletter** with a post in the last 90 days. Capture the last post date if visible.
4. **Google Business Profile posts** in the last 30 days. GBP posts are a free repeat hook most operators ignore.

If the operator has FareHarbor, Peek, Bōkun, Rezdy, or Xola visible, note it. The booking engine determines what referral mechanics are realistic in the next 30 days.

### 2. Pick the 1–2 strongest repeat-visit angles for THIS operator

Tour operators have at least four natural repeat angles. Score which apply to this operator based on the Business Context:

- **Different season.** The same trip at a different time of year reveals new things. In Hawaiʻi the strongest "different season" pitch is shoulder season (Sept–Nov, Apr–early May): fewer crowds, lower rates, different fruit on the trees, different swell, different weather. Use this one whenever the operator has any seasonal variation in product.
- **Different product.** They run a portfolio. Guest did Tour A and could come back for Tour B. If the portfolio is single-product, skip this angle.
- **Different traveler in the household.** Anniversary, kids' first time, parents visit, friends-trip return.
- **Cross-island upsell.** Did the Oʻahu version, here's the Kauaʻi or Maui version. Only applies if the operator has multi-island product or close partner referrals.
- **Referral.** "We loved it. My brother is coming next month, who should he book with?"

Pick the strongest 1–2 for the lifecycle drip. The other angles can show up in standalone reactivation emails later.

### 3. Draft the lifecycle drip plan (4 touchpoints, in sequence)

This is the methodology change from `email-sequence`. The operator gets a sequence with one job per touchpoint, not a pile of blasts. Cadence:

| When | Job | Trigger |
|---|---|---|
| **Day 1** | Thank-you and photo. Earn the right to send anything else. | Tour completion |
| **Week 1** | Review request and friend-seed. One ask, one CTA. | 7 days post-tour |
| **Month 3** | Different-product cross-sell, or the kamaʻāina rate. | 90 days post-tour |
| **Season 2** | Shoulder-season comeback or different-season pitch. | 6–9 months post-tour |

For each touchpoint, write:
- **Subject** (under 60 characters, in operator brand voice)
- **Body** (2–3 sentences in operator brand voice; concrete, specific, no template fillers)
- **CTA** (one button, action plus outcome)

Use the operator's words from the Business Context. If the brand uses "ʻohana," use it. If the brand avoids pidgin, do not impose it. If the brand uses "Aloha," open with it. If it does not, do not.

If a touchpoint cannot be reasonably drafted because the Business Context does not support it (e.g. Season 2 for an operator with no seasonal variation), say so. Do not fabricate.

### 4. Draft 3 reactivation email starters

These are standalone, sent ad-hoc by the operator on top of the lifecycle drip. Each targets a different angle:

- **Email 1, Different season.** "It's [shoulder season] now. Here's what's different about [their tour] this time of year." Lead with the specific seasonal change (mango is in, the swell drops, the goat-cheese pizza is back). CTA: book a return trip at the kamaʻāina or returning-guest rate.
- **Email 2, Different product cross-sell.** "You did [Tour A]. Most of our [Tour A] guests loved [Tour B]. Here's why." If portfolio is single-product, swap this for a "different traveler in the household" angle ("anniversary coming up?").
- **Email 3, Referral nudge.** "Know someone planning a Hawaiʻi trip? Here's the gift card or friend code." Use the operator's actual referral mechanic if they have one. If they do not, use the recommended mechanic from Section 5.

Each email is short. Subject under 60 chars. Body 2–3 sentences. One CTA.

### 5. Recommend 3 referral mechanics (with effort and revenue band)

This is the methodology add from `referral-program`. Adapted for a B2C trip operator with no engineering team. Pick 3 from this menu, choosing the ones that fit the operator's booking engine, voice, and ideal guest:

| Mechanic | What it does | Effort | Revenue band |
|---|---|---|---|
| **Gift card SKU on the site** | Existing guests buy a gift card for a friend. Lowest-friction referral. | Low | Mid |
| **Friend code at NPS-9-or-10 trigger** | Post-tour SMS asks the rating. 9 or 10 unlocks a code to share. Tied to the moment of highest enthusiasm. | Mid | High |
| **Photo-share post-tour SMS** | "Here's your photo from today. Tag us, share with a friend, here's a code for them." Doubles as social proof and referral. | Low | Mid |
| **Returning-guest auto-rate** | Same email books second time, the rate auto-adjusts. Booking-engine-dependent. | Mid | Mid |
| **Kamaʻāina-Plus tier** | Existing kamaʻāina guests get a compounding benefit on next visit (free add-on, +1 friend at rate). | Mid | Mid |
| **Group-of-4 friend rate** | Book with 3 others, the 4th seat is free or 50% off. | Low | High |
| **Operator partner cross-island swap** | Partner with a same-tier operator on another island. Each refers the other. | High | Mid |

Each mechanic is a sentence the operator can read in 10 seconds. Do not stack 7. Pick 3 that fit this operator.

### 6. Pick three repeat-visit operational ideas (no email, no referral)

Things the operator could ship without rebuilding their stack. Pick from:

- A photo follow-up email with a hi-res image from the day (already have, just don't send).
- A "share your trip" post-experience SMS with a Yelp or Google review link.
- A seasonal newsletter, one per quarter, with what's new at the tour.
- A "next time you're in [Hawaiian island]" email 6 months later.
- A GBP post every Monday with this week's harvest, swell, conditions, or menu special.

Three is enough. Each gets one line plus an effort tag (Low / Mid).

---

## Output

Two parts, in this order. Both are required.

### Part 1, Paste-ready markdown summary

Above the HTML artifact, emit a markdown block the operator can paste directly into their AI project memory (Claude Project knowledge, ChatGPT custom instructions, internal Notion, etc.). Roughly 12–15 lines. Format:

```markdown
## Repeat Hooks, [Business Name] (paste into your AI project memory)

**Touchpoint audit (current state):**
- Email signup: [Yes / No, with detail]
- Repeat / referral program: [Yes / No, with detail]
- Active blog or newsletter: [Yes, last post date / No]
- GBP posts in last 30 days: [Yes / No]

**Lifecycle drip plan (4 touchpoints):**
- Day 1: [one-line summary of the touchpoint]
- Week 1: [one-line summary]
- Month 3: [one-line summary]
- Season 2: [one-line summary]

**3 reactivation email subjects (in [Business Name]'s voice):**
1. [Subject, different season]
2. [Subject, different product or different-traveler cross-sell]
3. [Subject, referral nudge]

**3 referral mechanics (effort × revenue):**
1. [Mechanic name], [Low/Mid/High effort × Low/Mid/High revenue band]
2. [Mechanic name], [...]
3. [Mechanic name], [...]
```

### Part 2, HTML artifact

Self-contained HTML, Lights On design system. Inter from Google Fonts (300 display, 400 UI, 500 for milestone labels, 600 for the eyebrow / section labels / provenance badge). Source Serif 4 from Google Fonts for the email body pull-quotes. Heading `#061b31`, body `#273951`, label `#273951`, accent `#533afd`, border `#e5edf5`, white background. Radii 4–8px (999px only on the provenance badge chip). Subtle blue-tinted shadow `rgba(50,50,93,0.10) 0px 12px 20px 0px` ONLY on the lifecycle timeline cards (the design hook). Plain border for everything else.

**Provenance badge.** Stamp the artifact with `Powered by Lights On · ran on [YYYY-MM-DD]` immediately after the deck/subtitle, where `[YYYY-MM-DD]` is the actual date the skill is run. Use the `.stamp` class in the template below. The `·` character is U+00B7 middle dot, single space on either side.

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Repeat Hooks · [Business Name]</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600&family=Source+Serif+4:ital,wght@1,400&display=swap" rel="stylesheet">
<style>
  :root {
    --heading: #061b31;
    --body: #273951;
    --label: #273951;
    --accent: #533afd;
    --accent-soft: rgba(83, 58, 253, 0.08);
    --border: #e5edf5;
    --border-soft: #f0f4f9;
    --bg: #ffffff;
    --surface: #fefefe;
    --yes: #108c3d;
    --no: #ea2261;
    --shadow-card: rgba(50,50,93,0.10) 0px 12px 20px 0px;
  }
  * { box-sizing: border-box; }
  body {
    font-family: 'Inter', -apple-system, sans-serif;
    font-weight: 300;
    font-size: 17px;
    max-width: 1080px;
    margin: 40px auto;
    padding: 0 32px;
    color: var(--heading);
    background: var(--bg);
    line-height: 1.55;
    -webkit-font-smoothing: antialiased;
    font-feature-settings: "ss01";
  }
  .stamp {
    display: inline-block;
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 0.16em;
    text-transform: uppercase;
    color: var(--accent);
    background: rgba(83,58,253,0.08);
    border-radius: 999px;
    padding: 4px 10px;
    margin-bottom: 28px;
  }
  .eyebrow {
    font-family: 'Inter', sans-serif;
    font-size: 12px;
    font-weight: 600;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 8px;
  }
  h1 {
    font-size: 44px;
    font-weight: 300;
    letter-spacing: -1.2px;
    line-height: 1.05;
    margin: 0 0 4px;
    color: var(--heading);
  }
  .deck {
    font-size: 20px;
    font-weight: 300;
    color: var(--body);
    margin: 0 0 12px;
    max-width: 720px;
    line-height: 1.55;
  }
  .section-label {
    font-size: 13px;
    font-weight: 600;
    letter-spacing: 0.16em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 18px;
  }
  .section { margin-bottom: 64px; }

  /* Audit grid */
  .audit-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
  }
  .audit-cell {
    padding: 18px 22px;
    border: 1px solid var(--border);
    border-radius: 8px;
    background: var(--surface);
    display: flex;
    flex-direction: column;
    gap: 6px;
  }
  .audit-cell .name {
    font-size: 11px;
    font-weight: 500;
    color: var(--label);
    text-transform: uppercase;
    letter-spacing: 0.1em;
  }
  .audit-cell .answer {
    font-size: 16px;
    font-weight: 400;
    color: var(--heading);
  }
  .audit-cell .answer.yes { color: var(--yes); }
  .audit-cell .answer.no { color: var(--no); }
  .audit-cell .detail {
    font-size: 16px;
    color: var(--body);
    line-height: 1.55;
  }

  /* Lifecycle timeline */
  .timeline {
    position: relative;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 18px;
  }
  .timeline::before {
    content: "";
    position: absolute;
    top: 22px;
    left: 8%;
    right: 8%;
    height: 1px;
    background: var(--border);
    z-index: 0;
  }
  .milestone {
    position: relative;
    z-index: 1;
    display: flex;
    flex-direction: column;
    gap: 14px;
  }
  .milestone .marker {
    width: 14px;
    height: 14px;
    border-radius: 50%;
    background: var(--bg);
    border: 2px solid var(--accent);
    margin: 14px auto 0;
  }
  .milestone .when {
    font-size: 11px;
    font-weight: 500;
    letter-spacing: 0.16em;
    text-transform: uppercase;
    color: var(--accent);
    text-align: center;
  }
  .milestone .card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 22px 20px;
    box-shadow: var(--shadow-card);
    display: flex;
    flex-direction: column;
    gap: 12px;
    flex: 1;
  }
  .milestone .subject {
    font-family: 'Inter', sans-serif;
    font-size: 11px;
    font-weight: 500;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: var(--label);
    line-height: 1.4;
  }
  .milestone .body {
    font-family: 'Source Serif 4', Georgia, serif;
    font-style: italic;
    font-size: 16px;
    font-weight: 400;
    color: var(--heading);
    line-height: 1.6;
  }
  .milestone .cta {
    font-size: 13px;
    font-weight: 400;
    color: var(--accent);
    margin-top: auto;
    line-height: 1.5;
  }

  /* Email mockups */
  .email {
    border: 1px solid var(--border);
    border-radius: 6px;
    background: var(--surface);
    margin-bottom: 14px;
    overflow: hidden;
  }
  .email .envelope-bar {
    border-bottom: 1px solid var(--border-soft);
    padding: 10px 22px;
    font-size: 11px;
    font-weight: 500;
    color: var(--accent);
    text-transform: uppercase;
    letter-spacing: 0.14em;
    background: var(--surface);
  }
  .email .envelope-body {
    padding: 22px 24px 20px;
  }
  .email .subject-line {
    font-size: 16px;
    font-weight: 400;
    color: var(--heading);
    margin-bottom: 14px;
    line-height: 1.4;
  }
  .email .subject-line::before {
    content: "Subject: ";
    color: var(--body);
    font-weight: 500;
  }
  .email .body-copy {
    font-size: 16px;
    color: var(--body);
    line-height: 1.6;
    margin-bottom: 14px;
  }
  .email .cta-link {
    font-size: 13px;
    font-weight: 400;
    color: var(--accent);
  }

  /* Referral mechanics row */
  .mechanics {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 14px;
  }
  .mechanic {
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 22px;
    background: var(--surface);
    display: flex;
    flex-direction: column;
    gap: 12px;
  }
  .mechanic .title {
    font-size: 16px;
    font-weight: 400;
    color: var(--heading);
    line-height: 1.35;
  }
  .mechanic .description {
    font-size: 16px;
    color: var(--body);
    line-height: 1.55;
  }
  .mechanic .pills {
    display: flex;
    gap: 8px;
    margin-top: auto;
  }
  .pill {
    font-size: 10px;
    font-weight: 500;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    padding: 4px 8px;
    border-radius: 4px;
    border: 1px solid var(--border);
    color: var(--label);
    background: var(--bg);
  }
  .pill .pill-label {
    color: var(--body);
    margin-right: 4px;
  }

  /* Operational ideas */
  .ideas {
    border: 1px solid var(--border);
    border-radius: 8px;
    background: var(--surface);
  }
  .idea {
    padding: 16px 22px;
    border-bottom: 1px solid var(--border-soft);
    display: flex;
    align-items: baseline;
    gap: 16px;
  }
  .idea:last-child { border-bottom: none; }
  .idea .text {
    font-size: 16px;
    color: var(--heading);
    flex: 1;
    line-height: 1.55;
  }
  .idea .effort {
    font-size: 10px;
    font-weight: 500;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--body);
    white-space: nowrap;
  }

  /* Footer */
  .footer {
    margin-top: 64px;
    padding-top: 24px;
    border-top: 1px solid var(--border);
    font-size: 13px;
    color: #425466;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .footer a {
    color: var(--accent);
    text-decoration: none;
  }

  /* Responsive */
  @media (max-width: 760px) {
    body { margin: 32px auto; padding: 0 20px; }
    h1 { font-size: 32px; letter-spacing: -0.6px; }
    .audit-grid { grid-template-columns: 1fr; }
    .timeline { grid-template-columns: 1fr; }
    .timeline::before { display: none; }
    .mechanics { grid-template-columns: 1fr; }
    .footer { flex-direction: column; gap: 8px; align-items: flex-start; }
  }
</style>
</head>
<body>

  <div class="eyebrow">Reconnect · Repeat Hooks</div>
  <h1>[Business Name]</h1>
  <p class="deck">After the tour ends, what brings them back? A four-touchpoint plan, three reactivation starters, and three referral mechanics, drafted in [Business Name]'s voice.</p>
  <span class="stamp">Powered by Lights On · ran on [YYYY-MM-DD]</span>

  <!-- Section 1: Touchpoint audit -->
  <div class="section">
    <div class="section-label">Post-experience touchpoint audit</div>
    <div class="audit-grid">
      <div class="audit-cell">
        <div class="name">Email signup on homepage</div>
        <div class="answer [yes/no]">[Yes / No]</div>
        <div class="detail">[Above the fold? Incentive offered? "10% off first purchase, café excluded" or "Not visible."]</div>
      </div>
      <div class="audit-cell">
        <div class="name">Repeat or referral program</div>
        <div class="answer [yes/no]">[Yes / No]</div>
        <div class="detail">[Kamaʻāina-Plus rate visible? Gift card SKU on site? Friend code?]</div>
      </div>
      <div class="audit-cell">
        <div class="name">Active blog or newsletter</div>
        <div class="answer [yes/no]">[Yes / No]</div>
        <div class="detail">[Last post date if visible.]</div>
      </div>
      <div class="audit-cell">
        <div class="name">GBP posts in last 30 days</div>
        <div class="answer [yes/no]">[Yes / No]</div>
        <div class="detail">[Last GBP post date if visible. "Free repeat hook" if blank.]</div>
      </div>
    </div>
  </div>

  <!-- Section 2: Lifecycle drip timeline -->
  <div class="section">
    <div class="section-label">Lifecycle drip plan · four touchpoints</div>
    <div class="timeline">
      <div class="milestone">
        <div class="marker"></div>
        <div class="when">Day 1</div>
        <div class="card">
          <div class="subject">[Subject line in operator's voice]</div>
          <div class="body">"[Body draft, 2–3 sentences in operator brand voice. Thank-you and photo. Earns the right to send anything else.]"</div>
          <div class="cta">→ [CTA: download photos / share on social]</div>
        </div>
      </div>
      <div class="milestone">
        <div class="marker"></div>
        <div class="when">Week 1</div>
        <div class="card">
          <div class="subject">[Subject line]</div>
          <div class="body">"[Body, review request and friend-seed. One ask, one CTA, in operator voice.]"</div>
          <div class="cta">→ [CTA: leave a review]</div>
        </div>
      </div>
      <div class="milestone">
        <div class="marker"></div>
        <div class="when">Month 3</div>
        <div class="card">
          <div class="subject">[Subject line]</div>
          <div class="body">"[Body, different-product cross-sell or kamaʻāina rate. Specific to portfolio.]"</div>
          <div class="cta">→ [CTA: book the next experience]</div>
        </div>
      </div>
      <div class="milestone">
        <div class="marker"></div>
        <div class="when">Season 2</div>
        <div class="card">
          <div class="subject">[Subject line]</div>
          <div class="body">"[Body, shoulder-season comeback (Sept–Nov or Apr–early May). Specific seasonal change: what's in season, what's different on the farm/water/island.]"</div>
          <div class="cta">→ [CTA: book a shoulder-season visit]</div>
        </div>
      </div>
    </div>
  </div>

  <!-- Section 3: Reactivation email starters -->
  <div class="section">
    <div class="section-label">Three reactivation email starters</div>

    <div class="email">
      <div class="envelope-bar">Different season</div>
      <div class="envelope-body">
        <div class="subject-line">[Subject, under 60 chars, in operator voice]</div>
        <div class="body-copy">[2–3 sentence body. Lead with the specific seasonal change. No template fillers, no fake first names.]</div>
        <div class="cta-link">→ [CTA] · [destination URL]</div>
      </div>
    </div>

    <div class="email">
      <div class="envelope-bar">Different product cross-sell</div>
      <div class="envelope-body">
        <div class="subject-line">[Subject]</div>
        <div class="body-copy">[2–3 sentence body. "You did Tour A. Most of our Tour A guests loved Tour B. Here's why."]</div>
        <div class="cta-link">→ [CTA] · [destination URL]</div>
      </div>
    </div>

    <div class="email">
      <div class="envelope-bar">Referral nudge</div>
      <div class="envelope-body">
        <div class="subject-line">[Subject]</div>
        <div class="body-copy">[2–3 sentence body. Use the operator's actual referral mechanic. If none, recommend the Section-5 mechanic and write the line that operationalizes it.]</div>
        <div class="cta-link">→ [CTA] · [destination URL]</div>
      </div>
    </div>
  </div>

  <!-- Section 4: Referral mechanics -->
  <div class="section">
    <div class="section-label">Three referral mechanics to ship</div>
    <div class="mechanics">
      <div class="mechanic">
        <div class="title">[Mechanic name 1]</div>
        <div class="description">[One-sentence description of how it works for THIS operator. Booking-engine-aware.]</div>
        <div class="pills">
          <span class="pill"><span class="pill-label">Effort</span>[Low / Mid / High]</span>
          <span class="pill"><span class="pill-label">Revenue</span>[Low / Mid / High]</span>
        </div>
      </div>
      <div class="mechanic">
        <div class="title">[Mechanic name 2]</div>
        <div class="description">[Description.]</div>
        <div class="pills">
          <span class="pill"><span class="pill-label">Effort</span>[Low / Mid / High]</span>
          <span class="pill"><span class="pill-label">Revenue</span>[Low / Mid / High]</span>
        </div>
      </div>
      <div class="mechanic">
        <div class="title">[Mechanic name 3]</div>
        <div class="description">[Description.]</div>
        <div class="pills">
          <span class="pill"><span class="pill-label">Effort</span>[Low / Mid / High]</span>
          <span class="pill"><span class="pill-label">Revenue</span>[Low / Mid / High]</span>
        </div>
      </div>
    </div>
  </div>

  <!-- Section 5: Operational repeat ideas -->
  <div class="section">
    <div class="section-label">Three repeat-visit ideas you can ship next week</div>
    <div class="ideas">
      <div class="idea">
        <div class="text">[Idea 1, specific to this operator's stack.]</div>
        <div class="effort">[Low / Mid effort]</div>
      </div>
      <div class="idea">
        <div class="text">[Idea 2.]</div>
        <div class="effort">[Low / Mid effort]</div>
      </div>
      <div class="idea">
        <div class="text">[Idea 3.]</div>
        <div class="effort">[Low / Mid effort]</div>
      </div>
    </div>
  </div>

  <div class="footer">
    <span>Built with the Hospitality Business Skills teammate · github.com/lightson-digital/hospitality-business-skills</span>
    <a href="https://lightson.co" target="_blank" rel="noopener">Powered by Lights On</a>
  </div>

</body>
</html>
```

---

## Tone rules

- Email bodies in the operator's brand voice from the Business Context. If they're warm and family-led, write warm and family-led. If they're crisp and minimal, write crisp and minimal. The voice document is the source of truth.
- Subject lines under 60 chars. No emoji unless the brand voice already uses them.
- "Aloha" only if the operator already uses it. "ʻOhana," "kamaʻāina," "Support Local," and similar Hawaiian-leaning vocab only if the brand already uses them. Do not impose pidgin or Hawaiian on a brand that does not speak it.
- Hawaiian diacritics correct (ʻokina, kahakō) on business and place names.
- No fake first names ("Hi {firstName}"). Write the actual line.
- No em dashes. Commas, periods, parentheses, colons.
- Do not fabricate. If a touchpoint or angle cannot be sampled from the Business Context, say so. State the gap, do not paper over it.

## What success looks like

The operator reads the report, pastes the markdown summary into their AI project memory, and ships the Day-1 thank-you email or one referral mechanic that same week. Six months later, a returning guest books at the kamaʻāina rate and tags a friend in the photo.

---

*Built with the Hospitality Business Skills teammate · github.com/lightson-digital/hospitality-business-skills*

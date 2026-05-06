---
name: Pre-Arrival Concierge
description: Pre-arrival-stage skill for B2C Hawaiʻi trip-experience operators. Use when the user says "pre-arrival emails," "what to send between booking and tour day," "upsell sequence," "drip campaign for guests," "T-7 email," "show-day SMS," "we're losing add-on revenue," "no-shows are up." Maps the upsell surface the operator is leaving on the table between booking and arrival, maps anxieties travelers carry into show-day, drafts a 3-touch sequence (T-7, T-1, T+0) in operator brand voice. Recommends 3 service-flow upgrades. Outputs a paste-ready markdown summary plus an HTML artifact.
---

# Pre-Arrival Concierge

The Pre-arrival-stage teammate. Answers the question: *"Are guests ready before they show up, and have we earned every dollar they're willing to spend?"*

Run after Business Context. If you have not run Business Context in this conversation, run it first. You need the business name, signature experiences, ideal guest, voice, source markets, and pricing tier before this skill can do its job.

## When to use

The user gave you a tour, lūʻau, attraction, charter, retreat, or boutique-lodging URL. They want to know what happens between "booking confirmed" and "guest arrives on property," what's missing, and what could ship next week. This skill is built for B2C trip-experience operators in Hawaiʻi. It is not built for B2B SaaS or e-commerce.

If the user has not given you a URL, ask once:

> "What's the URL of the operator you want me to plan pre-arrival for?"

## Two co-equal pillars

This skill plans for two things at once. Most pre-arrival sequences pick one and ignore the other. Both are revenue.

1. **Upsell opportunity discovery (the revenue pillar).** What add-on, gift, premium tier, complementary product, retail attachment, or experience-stack the operator is leaving on the table between booking and arrival. The window from "card charged" to "show day" is the highest-intent window the operator owns. Most operators waste it on logistics-only emails.
2. **Anxiety reduction and readiness (the operations pillar).** What travelers worry about between booking and arrival, and how to address it so they show up prepared, on time, with the right shoes, and not asking for a refund. This pillar protects the booking. The first pillar grows it.

The 3-touch sequence (T-7, T-1, T+0) carries both. T-7 is the upsell window primarily and the anxiety-prep secondarily. T-1 is operational confirmation. T+0 is logistical and trust-only. We do not stack a hard upsell into a touch where the guest just needs to know which gate to drive to.

## Methodology layered in

This skill borrows from four Corey Haines marketing skills, adapted to a B2C trip operator with no engineering team and a ~$50 ticket.

- **`email-sequence`** for cadence. The output is a 3-touch lifecycle sequence with one job per touch, not a pile of blasts. Drips beat blasts.
- **`onboarding-cro`** for activation thinking. Booking confirmation is signup. T+0 arrival is activation. Everything between is the onboarding window. Each touch moves the guest one step closer to "ready to show up and spend."
- **`pricing-strategy`** for the upsell tier-stack. Most operators have a flat ticket and no good-better-best ladder. The pre-arrival window is where you offer the "better" or "best" version (private upgrade, premium seating, photo package, gift add-on) without rebuilding the pricing page.
- **`paywall-upgrade-cro`** adapted to email and SMS. The principle "value before ask, then upgrade in-context after the aha moment" maps directly to pre-arrival: the guest already paid (aha moment), so the T-7 upsell is an in-context upgrade prompt, not a cold sell. Show, do not tell. Easy yes, easy no, do not block the booking.

---

## How it runs

### 1. Inventory the upsell surface

Pull from the Business Context. Walk every revenue surface the operator already has. Score each as easy / medium / hard to add to the pre-arrival flow.

| Upsell vector | What it is | Typical operator categories |
|---|---|---|
| Cross-sell within portfolio | Guest booked Tour A, also offer Tour B at a returning-guest rate. | Multi-product operators (lūʻau + photo, ag tour + café event, helicopter A + helicopter B). |
| Retail attachment | Branded merch, food gift box, jam, honey, kona coffee, captain's logbook. Online + on-site shop. | Ag, F&B, lodging, charter. |
| Café / F&B add-on | Pre-booked lunch reservation, drink package, dietary upgrade. | Ag tours, lūʻau, retreats. |
| Premium tier | Private vs. group, VIP seating, front-row, upgraded vehicle, captain's table. | Lūʻau, helicopter, snorkel, transportation, lodging. |
| Photo / video package | Pro photo package, GoPro rental, drone footage. Highest-margin upsell after premium tier. | Snorkel, helicopter, lūʻau, charter, ag. |
| Gift the experience | Same product, gifted to a third party. Add a gift card SKU + a printable card. | Any. Highest leverage at booking confirmation, not just pre-arrival. |
| Add-ons | Transportation, longer duration, equipment rental, food upgrade, lei greeting. | All. |
| Package builder | Bundle 2 of the operator's products at a discount. "Tour + lunch," "Sunset sail + dinner reservation." | Multi-product operators. |

For each vector, score:
- **Easy to add to the current flow** (does the booking engine support an add-on field, or does the operator need to send a Square link).
- **Brand-voice fit** (a kamaʻāina-led ag tour does not run a "VIP" tier; a luxury lodge does not run "Support Local").
- **Revenue per booking lift band**, Low (under $5 average), Mid ($5–25 average), High ($25+ average). No fake precision.

Pick the **top 5 upsell opportunities** ranked by impact × effort. Each gets a vector name, what it is in one sentence, where in the sequence it goes (T-7 vs. T-1 vs. on-arrival), and a copy hook in the operator's brand voice.

#### Category-specific upsell defaults

Use the Business Context category to pick defaults. Override with anything the site reveals.

- **Ag tour / agritourism**, café reservation + retail attachment (jam, honey, banana bread gift box) + gift box for a friend back home + group-tour upgrade.
- **Lūʻau**, premium seating + photo / video package + lei greeting + table side.
- **Helicopter / aviation**, private charter upgrade + duration extension + photo package + door-off upgrade.
- **Transportation / shuttle**, premium vehicle / private + child seat included + extended hours.
- **Lodging / boutique hotel**, room upgrade + experience credit + late-checkout + welcome amenity.
- **Snorkel / charter / dive**, private boat upgrade + photo package + reef-safe sunscreen kit + gear quality upgrade + onboard food upgrade.
- **Cultural tour / attraction**, guided private upgrade + retail attachment + gift the experience.

### 2. Inventory the anxiety surface

Pull from the Business Context "What the trip is really for → Anxieties travelers carry into the booking" section. Add anything the site's FAQ does not currently answer well.

Score each anxiety on impact:
- **Cancellation risk**, does the anxiety drive the guest to cancel before arrival.
- **Refund pressure**, does the guest arrive unprepared and then ask for a refund (wrong shoes, motion sickness, kids melting down).
- **No-show rate**, does the guest just not show up because show-day logistics were unclear.
- **Low-NPS risk**, guest shows up but the experience is a 4 instead of a 5 because of a preventable surprise.

Pick **4 to 6 anxieties** that actually apply to this operator. Map each to the touch that handles it.

#### Category-specific anxiety defaults

- **Snorkel / charter**, sunscreen ban + reef-safe expectation + seasickness + non-swimmer policy + gear sizing + what to bring (towel, change of clothes).
- **Lūʻau**, arrival-time and check-in window + parking + dress code + dietary accommodations + photo etiquette.
- **Ag tour**, closed-toe shoes + sun protection + bathroom + accessibility on dirt paths + bring water + kid-readiness.
- **Helicopter**, weight policy + weather refund / reschedule policy + motion sickness + arrival-time and ID requirements + what to wear.
- **Transportation**, pickup window + child seat policy + luggage allowance + cell signal at pickup point.
- **Lodging**, check-in time + parking + early-arrival luggage policy + on-property food + Wi-Fi + late-arrival.

### 3. Draft the 3-touch sequence

Cadence:

| When | Job | Trigger | Channel |
|---|---|---|---|
| **T-7 days** | "What to expect", upsell window primarily, anxiety-prep secondarily. | 7 days before tour date, OR booking confirmation if booked under 7 days out. | Email (long-form). |
| **T-1 day** | "Show-day logistics", confirmation, expectation-setting, last-minute prep. NO upsell. | 1 day before tour date. | Email or SMS depending on what the operator has. |
| **T+0 morning** | "We're on for today", real-time confirmation, parking pin, weather call. NO upsell except a soft on-property mention if it's already part of the experience. | Tour-day morning, 2–4 hours before start. | SMS preferred. Email if no SMS. |

For each touch, write:
- **Subject line**, under 60 characters, in operator brand voice.
- **Body**, 2–4 sentences in operator brand voice. Concrete, specific, no template fillers, no fake first names.
- **CTAs**, T-7 gets two CTAs (one upsell to checkout, one prep link to FAQ or what-to-bring page). T-1 gets one logistics CTA. T+0 gets one logistics CTA (parking pin, day-of phone number).

The T-7 touch is the design centerpiece of the sequence. It does the revenue work. Treat it like a lightweight upgrade modal: lead with the experience, surface ONE upsell with a clear price and a clear button, then wrap with prep and a reassurance line. Do not bury the upsell at the bottom and do not stack three.

#### Brand-voice rules for the upsell hook

- If the operator is family-led / kamaʻāina (Kahuku Farms, Lokoea Farms, most Hawaiʻi ag), the upsell hook is warm and matter-of-fact. "While you're here, the café opens at 11. Want us to hold a banana bread for after the tour? Add it for $X." Not pushy. Not "exclusive."
- If the operator is premium / minimal (luxury lodge, private charter, helicopter), the upsell is crisp and confident. "Upgrade to the door-off configuration for $X. Same flight, same time, better photos."
- If the operator already uses "ʻohana," "kamaʻāina," "Aloha," "Support Local," use them. If not, do not impose them.
- Never use "VIP," "exclusive," "luxury," "premium" if the brand voice document explicitly bans them.

### 4. Recommend 3 service-flow upgrades

These are NOT email-only. They are changes to the post-booking flow itself, the booking engine, the SMS stack, the operator's day-of process. The point is to ship the right pre-arrival operation, not just the right pre-arrival email.

Pick 3 from this menu, choosing the ones that fit the operator's booking engine, voice, and category:

| Service-flow upgrade | What it does | Effort | Revenue / ops band |
|---|---|---|---|
| 1-question post-booking survey | "Anything we should know before the day?" Free-text. Output goes to a captain or guide cheat sheet. Catches dietary, mobility, kid-age, language. | Low | Mid (saves NPS, surfaces upsell) |
| Add-on field at checkout (BE-native) | The booking engine collects upsell at the moment of highest commitment. FareHarbor / Peek / Bōkun all support this. | Low / Mid | High |
| Automated weather-call SMS at T-1 | Real-time weather call with a one-tap "reschedule" button. Cuts no-shows on borderline-weather days. | Mid | Mid |
| Pre-arrival "what to wear and bring" page | One URL, one page, no PDF. Linked from every touch. Eliminates 80% of the inbound calls. | Low | Mid |
| Dietary / accessibility flag at booking | A single yes / no flag at booking, routed to ops. Removes the day-of scramble. | Low | Mid |
| Photo-package opt-in pre-tour | Sell the photo package before the day, not after. Pre-tour conversion is 2–3x post-tour. | Mid | High |
| Gift-the-experience SKU live on the site | Standalone SKU + printable card. Captures gift bookings around holidays and birthdays. | Mid | Mid |
| On-day SMS with parking pin + day-of phone number | Two-line SMS, sent at T-2 hours. Replaces 90% of "I can't find you" calls. | Low | Mid |
| Pre-arrival upsell email automation in the BE | Drip the T-7 / T-1 / T+0 sequence directly off the booking engine, not the operator's manual list. | Mid | High |
| Returning-guest auto-rate trigger | Same email books a second time, the rate auto-adjusts. Powers the cross-sell upsell. | Mid | Mid |

Each recommendation gets a one-sentence description specific to this operator, plus an effort pill and an impact pill. Three is enough. Do not stack 7.

---

## Output

Two parts, in this order. Both are required.

### Part 1, Paste-ready markdown summary

Above the HTML artifact, emit a markdown block the operator can paste directly into their AI project memory (Claude Project knowledge, ChatGPT custom instructions, internal Notion). Roughly 13–16 lines. Format:

```markdown
## Pre-Arrival Concierge, [Business Name] (paste into your AI project memory)

**Top 3 upsell opportunities (revenue pillar):**
1. [Vector name], [one-line what / where in the sequence / impact band]
2. [Vector name], [one-line]
3. [Vector name], [one-line]

**Top 4 anxieties (operations pillar):**
1. [Anxiety], [addressed at T-?]
2. [Anxiety], [addressed at T-?]
3. [Anxiety], [addressed at T-?]
4. [Anxiety], [addressed at T-?]

**3-touch sequence (subject lines in [Business Name]'s voice):**
- T-7: [Subject] (upsell window + prep)
- T-1: [Subject] (show-day logistics)
- T+0: [Subject] (we're on for today)

**3 service-flow upgrades to ship:**
1. [Upgrade name], [Low/Mid/High effort × Low/Mid/High impact]
2. [Upgrade name], [...]
3. [Upgrade name], [...]
```

### Part 2, HTML artifact

Self-contained HTML, Lights On design system. Inter from Google Fonts (300 display, 400 UI, 500 for milestone labels, 600 for the eyebrow / section labels / provenance badge). Source Serif 4 from Google Fonts for the email body pull-quotes. Heading `#061b31`, body `#273951`, label `#273951`, accent `#533afd`, border `#e5edf5`, white background. Radii 4–8px (999px only on the provenance badge chip). Subtle blue-tinted shadows ONLY on the T-7 envelope card (the design centerpiece of the sequence) and on the upsell-map row containers. Plain border for everything else. `tnum` on numbers. `font-feature-settings: "ss01"` on Inter where supported.

**Provenance badge.** Stamp the artifact with `Powered by Lights On · ran on [YYYY-MM-DD]` immediately after the deck/subtitle, where `[YYYY-MM-DD]` is the actual date the skill is run. Use the `.stamp` class in the template below. The `·` character is U+00B7 middle dot, single space on either side.

The **upsell map** is the visual centerpiece of the artifact, because it is the revenue pillar. It is a vertical stack of 5 row-cards. Each row-card has the vector name on the left, a one-line what + where, an impact label, an effort label, and a copy-hook line. Use a quiet purple accent dot on each row to signal the revenue pillar.

The **anxiety map** is a compact 4-to-6-row table. It is intentionally lower-key than the upsell map, narrower, no per-row accent dot, no envelope shadow. The asymmetry is the design point: the upsell map carries the revenue weight, the anxiety map is operational.

The **3 touches** are a horizontal timeline ([T-7] → [T-1] → [T+0]). Each touch is an envelope card. Subject is in label-caps (Inter 11px / 500 / uppercase / 0.14em letter-spacing). Body is in Source Serif 4 italic pull-quote. CTAs are muted accent (`#533afd` at 0.78 opacity). The T-7 envelope card has a quiet "upsell window" tag in the corner to make the dual-purpose visible at a glance.

The **3 service-flow upgrades** are a numbered ranked list with effort and impact pills.

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Pre-Arrival Concierge · [Business Name]</title>
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
    --accent-soft-2: rgba(83, 58, 253, 0.14);
    --border: #e5edf5;
    --border-soft: #f0f4f9;
    --bg: #ffffff;
    --surface: #fefefe;
    --shadow-card: rgba(50,50,93,0.10) 0px 12px 20px 0px;
  }
  * { box-sizing: border-box; }
  body {
    font-family: 'Inter', -apple-system, sans-serif;
    font-feature-settings: "ss01";
    font-weight: 300;
    font-size: 17px;
    max-width: 1080px;
    margin: 40px auto;
    padding: 0 32px;
    color: var(--heading);
    background: var(--bg);
    line-height: 1.55;
    -webkit-font-smoothing: antialiased;
  }
  .stamp {
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 0.16em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 28px;
    display: inline-block;
    padding: 4px 10px;
    border-radius: 999px;
    background: rgba(83,58,253,0.08);
  }
  .eyebrow {
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
    max-width: 760px;
    line-height: 1.55;
  }
  .section-label {
    font-size: 13px;
    font-weight: 600;
    letter-spacing: 0.16em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 18px;
    display: flex;
    align-items: baseline;
    gap: 14px;
  }
  .section-label .pillar-tag {
    font-size: 10px;
    font-weight: 400;
    color: var(--body);
    letter-spacing: 0.12em;
    text-transform: uppercase;
  }
  .section { margin-bottom: 64px; }

  /* Upsell map, design centerpiece, revenue pillar */
  .upsell-stack {
    display: flex;
    flex-direction: column;
    gap: 10px;
  }
  .upsell-row {
    display: grid;
    grid-template-columns: 24px 1.2fr 2fr 90px 90px;
    gap: 22px;
    align-items: center;
    padding: 20px 22px;
    border: 1px solid var(--border);
    border-radius: 8px;
    background: var(--surface);
    box-shadow: var(--shadow-card);
  }
  .upsell-row .dot {
    width: 8px;
    height: 8px;
    border-radius: 50%;
    background: var(--accent);
    margin: 0 auto;
  }
  .upsell-row .vector {
    font-size: 16px;
    font-weight: 400;
    color: var(--heading);
    line-height: 1.4;
  }
  .upsell-row .what {
    font-size: 16px;
    color: var(--body);
    line-height: 1.55;
  }
  .upsell-row .what .hook {
    display: block;
    margin-top: 8px;
    font-family: 'Source Serif 4', Georgia, serif;
    font-style: italic;
    font-size: 16px;
    color: var(--label);
    line-height: 1.55;
  }
  .upsell-row .meta {
    font-size: 11px;
    font-weight: 500;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--label);
    text-align: right;
    font-feature-settings: "tnum";
  }
  .upsell-row .meta .meta-label {
    display: block;
    font-weight: 400;
    color: var(--body);
    font-size: 10px;
    margin-bottom: 2px;
    letter-spacing: 0.12em;
  }
  .upsell-row .meta .where {
    color: var(--accent);
  }

  /* Anxiety map, intentionally lower-key, operations pillar */
  .anxiety-table {
    border: 1px solid var(--border);
    border-radius: 6px;
    background: var(--surface);
    max-width: 760px;
  }
  .anxiety-row {
    display: grid;
    grid-template-columns: 1.4fr 1.6fr 0.8fr;
    gap: 18px;
    padding: 14px 22px;
    border-bottom: 1px solid var(--border-soft);
    align-items: center;
  }
  .anxiety-row:last-child { border-bottom: none; }
  .anxiety-row .name {
    font-size: 16px;
    color: var(--heading);
    font-weight: 400;
    line-height: 1.45;
  }
  .anxiety-row .impact {
    font-size: 16px;
    color: var(--body);
    line-height: 1.55;
  }
  .anxiety-row .where {
    font-size: 11px;
    font-weight: 500;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--accent);
    text-align: right;
    font-feature-settings: "tnum";
  }

  /* 3-touch timeline */
  .timeline {
    position: relative;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 18px;
  }
  .timeline::before {
    content: "";
    position: absolute;
    top: 22px;
    left: 14%;
    right: 14%;
    height: 1px;
    background: var(--border);
    z-index: 0;
  }
  .touch {
    position: relative;
    z-index: 1;
    display: flex;
    flex-direction: column;
    gap: 14px;
  }
  .touch .marker {
    width: 14px;
    height: 14px;
    border-radius: 50%;
    background: var(--bg);
    border: 2px solid var(--accent);
    margin: 14px auto 0;
  }
  .touch .when {
    font-size: 11px;
    font-weight: 500;
    letter-spacing: 0.16em;
    text-transform: uppercase;
    color: var(--accent);
    text-align: center;
    font-feature-settings: "tnum";
  }
  .touch .envelope {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 22px 22px 20px;
    display: flex;
    flex-direction: column;
    gap: 14px;
    flex: 1;
    position: relative;
  }
  .touch.featured .envelope {
    box-shadow: var(--shadow-card);
  }
  .touch .upsell-tag {
    position: absolute;
    top: 14px;
    right: 14px;
    font-size: 9px;
    font-weight: 500;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: var(--accent);
    background: var(--accent-soft);
    padding: 4px 8px;
    border-radius: 4px;
  }
  .touch .subject {
    font-size: 11px;
    font-weight: 500;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: var(--label);
    line-height: 1.45;
    margin-top: 8px;
  }
  .touch .pull {
    font-family: 'Source Serif 4', Georgia, serif;
    font-style: italic;
    font-weight: 400;
    font-size: 16px;
    color: var(--heading);
    line-height: 1.6;
  }
  .touch .ctas {
    display: flex;
    flex-direction: column;
    gap: 8px;
    margin-top: auto;
  }
  .touch .cta {
    font-size: 13px;
    font-weight: 400;
    color: var(--accent);
    line-height: 1.5;
  }
  .touch .cta.upsell::before {
    content: "↗ ";
    color: var(--accent);
  }
  .touch .cta.prep::before {
    content: "→ ";
    color: var(--body);
  }

  /* Service-flow recommendations */
  .ideas {
    border: 1px solid var(--border);
    border-radius: 8px;
    background: var(--surface);
  }
  .idea {
    padding: 18px 22px;
    border-bottom: 1px solid var(--border-soft);
    display: grid;
    grid-template-columns: 28px 1fr auto;
    gap: 18px;
    align-items: center;
  }
  .idea:last-child { border-bottom: none; }
  .idea .num {
    font-size: 13px;
    font-weight: 500;
    color: var(--accent);
    letter-spacing: 0.04em;
    font-feature-settings: "tnum";
  }
  .idea .text {
    font-size: 16px;
    color: var(--heading);
    line-height: 1.55;
  }
  .idea .text .name {
    font-weight: 400;
  }
  .idea .text .detail {
    color: var(--body);
    margin-top: 6px;
    font-size: 16px;
    line-height: 1.55;
  }
  .idea .pills {
    display: flex;
    gap: 8px;
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
    white-space: nowrap;
  }
  .pill .pill-label {
    color: var(--body);
    margin-right: 4px;
    font-weight: 400;
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
    .upsell-row { grid-template-columns: 1fr; gap: 10px; }
    .upsell-row .dot { display: none; }
    .upsell-row .meta { text-align: left; }
    .anxiety-row { grid-template-columns: 1fr; gap: 6px; }
    .anxiety-row .where { text-align: left; }
    .timeline { grid-template-columns: 1fr; }
    .timeline::before { display: none; }
    .idea { grid-template-columns: 1fr; gap: 10px; }
    .footer { flex-direction: column; gap: 8px; align-items: flex-start; }
  }
</style>
</head>
<body>

  <div class="eyebrow">Pre-arrival · Concierge</div>
  <h1>[Business Name]</h1>
  <p class="deck">Between the booking and the show day, two things matter. The dollars left on the table, and the anxieties that drive a refund request. A 3-touch sequence (T-7, T-1, T+0) carries both.</p>
  <span class="stamp">Powered by Lights On · ran on [YYYY-MM-DD]</span>

  <!-- Section 1: Upsell map (revenue pillar, design centerpiece) -->
  <div class="section">
    <div class="section-label">Upsell map · top 5 opportunities <span class="pillar-tag">revenue pillar</span></div>
    <div class="upsell-stack">
      <div class="upsell-row">
        <div class="dot"></div>
        <div class="vector">[Vector name 1]</div>
        <div class="what">[One-sentence what it is for THIS operator.]<span class="hook">"[Copy hook in operator brand voice. Specific, concrete, no fillers.]"</span></div>
        <div class="meta"><span class="meta-label">Where</span><span class="where">T-7</span></div>
        <div class="meta"><span class="meta-label">Lift</span>[High]</div>
      </div>
      <div class="upsell-row">
        <div class="dot"></div>
        <div class="vector">[Vector name 2]</div>
        <div class="what">[One-sentence what.]<span class="hook">"[Copy hook.]"</span></div>
        <div class="meta"><span class="meta-label">Where</span><span class="where">T-7</span></div>
        <div class="meta"><span class="meta-label">Lift</span>[Mid]</div>
      </div>
      <div class="upsell-row">
        <div class="dot"></div>
        <div class="vector">[Vector name 3]</div>
        <div class="what">[One-sentence what.]<span class="hook">"[Copy hook.]"</span></div>
        <div class="meta"><span class="meta-label">Where</span><span class="where">T-7</span></div>
        <div class="meta"><span class="meta-label">Lift</span>[Mid]</div>
      </div>
      <div class="upsell-row">
        <div class="dot"></div>
        <div class="vector">[Vector name 4]</div>
        <div class="what">[One-sentence what.]<span class="hook">"[Copy hook.]"</span></div>
        <div class="meta"><span class="meta-label">Where</span><span class="where">On-arrival</span></div>
        <div class="meta"><span class="meta-label">Lift</span>[Low]</div>
      </div>
      <div class="upsell-row">
        <div class="dot"></div>
        <div class="vector">[Vector name 5]</div>
        <div class="what">[One-sentence what.]<span class="hook">"[Copy hook.]"</span></div>
        <div class="meta"><span class="meta-label">Where</span><span class="where">Booking confirm</span></div>
        <div class="meta"><span class="meta-label">Lift</span>[Mid]</div>
      </div>
    </div>
  </div>

  <!-- Section 2: Anxiety map (operations pillar) -->
  <div class="section">
    <div class="section-label">Anxiety map · 4 to 6 rows <span class="pillar-tag">operations pillar</span></div>
    <div class="anxiety-table">
      <div class="anxiety-row">
        <div class="name">[Anxiety 1]</div>
        <div class="impact">[Impact band: cancellation risk / refund pressure / no-show / low-NPS. One line.]</div>
        <div class="where">T-7</div>
      </div>
      <div class="anxiety-row">
        <div class="name">[Anxiety 2]</div>
        <div class="impact">[Impact.]</div>
        <div class="where">T-7</div>
      </div>
      <div class="anxiety-row">
        <div class="name">[Anxiety 3]</div>
        <div class="impact">[Impact.]</div>
        <div class="where">T-1</div>
      </div>
      <div class="anxiety-row">
        <div class="name">[Anxiety 4]</div>
        <div class="impact">[Impact.]</div>
        <div class="where">T-1</div>
      </div>
      <div class="anxiety-row">
        <div class="name">[Anxiety 5]</div>
        <div class="impact">[Impact.]</div>
        <div class="where">T+0</div>
      </div>
    </div>
  </div>

  <!-- Section 3: 3-touch timeline -->
  <div class="section">
    <div class="section-label">3-touch sequence · upsell + prep, then logistics, then go</div>
    <div class="timeline">
      <div class="touch featured">
        <div class="marker"></div>
        <div class="when">T-7 days</div>
        <div class="envelope">
          <div class="upsell-tag">Upsell window</div>
          <div class="subject">[Subject, under 60 chars, in operator voice]</div>
          <div class="pull">"[Body, 2 to 4 sentences in operator brand voice. Lead with the experience, surface ONE upsell, close with one prep line.]"</div>
          <div class="ctas">
            <div class="cta upsell">[Upsell CTA: Add the [add-on] for $X]</div>
            <div class="cta prep">[Prep CTA: What to wear, where to park]</div>
          </div>
        </div>
      </div>
      <div class="touch">
        <div class="marker"></div>
        <div class="when">T-1 day</div>
        <div class="envelope">
          <div class="subject">[Subject, show-day logistics, no upsell]</div>
          <div class="pull">"[Body. Confirmation, expectation-setting, last-minute prep. No upsell here. Trust window is operational.]"</div>
          <div class="ctas">
            <div class="cta prep">[Logistics CTA: View your booking / parking / what to bring]</div>
          </div>
        </div>
      </div>
      <div class="touch">
        <div class="marker"></div>
        <div class="when">T+0 morning</div>
        <div class="envelope">
          <div class="subject">[Subject, we're on for today]</div>
          <div class="pull">"[Body. Real-time confirmation, parking pin, weather call, day-of phone number.]"</div>
          <div class="ctas">
            <div class="cta prep">[Day-of CTA: Open parking pin]</div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Section 4: 3 service-flow upgrades -->
  <div class="section">
    <div class="section-label">3 service-flow upgrades to ship into the booking flow</div>
    <div class="ideas">
      <div class="idea">
        <div class="num">01</div>
        <div class="text"><span class="name">[Upgrade name 1]</span><div class="detail">[One-sentence description specific to this operator. Booking-engine-aware.]</div></div>
        <div class="pills">
          <span class="pill"><span class="pill-label">Effort</span>[Low / Mid / High]</span>
          <span class="pill"><span class="pill-label">Impact</span>[Low / Mid / High]</span>
        </div>
      </div>
      <div class="idea">
        <div class="num">02</div>
        <div class="text"><span class="name">[Upgrade name 2]</span><div class="detail">[Description.]</div></div>
        <div class="pills">
          <span class="pill"><span class="pill-label">Effort</span>[Low / Mid / High]</span>
          <span class="pill"><span class="pill-label">Impact</span>[Low / Mid / High]</span>
        </div>
      </div>
      <div class="idea">
        <div class="num">03</div>
        <div class="text"><span class="name">[Upgrade name 3]</span><div class="detail">[Description.]</div></div>
        <div class="pills">
          <span class="pill"><span class="pill-label">Effort</span>[Low / Mid / High]</span>
          <span class="pill"><span class="pill-label">Impact</span>[Low / Mid / High]</span>
        </div>
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

## Phase 3 — Fact-check pass (mandatory)

Run this AFTER both the paste-ready markdown summary and the HTML artifact are drafted, and BEFORE you hand them to the user. This is a quality gate, not a watermark. If a check fails, fix in place silently and re-verify. Do not add a "fact-check passed" note to the visible output.

1. **URL liveness.** Pick 2 to 3 cited URLs at random from references in the deliverable (operator homepage, tour pages linked from CTAs, the operator's existing café/retail/gift-card SKU page if mentioned, FAQ or what-to-bring page). Re-fetch each via web_fetch. If any returns 404, blocked, or wrong content, drop the citation or replace with one that resolves. CTA destination URLs in the email mockups must resolve.

2. **Quote provenance.** For every verbatim copy hook attributed to the operator's brand voice, confirm the phrasing matches the operator's actual public copy (or is a faithful paraphrase in their voice from the Business Context). If you put a verbatim site phrase in the artifact and cannot verify it on the live site, mark it `(paraphrased)` or rewrite it. Do not put words in the operator's mouth they have never used.

3. **Number sanity.** Every price ($X for the upsell, kamaʻāina rate, photo package fee), duration, attach-rate band, group size, and timing window (T-7, T-1, T+0, weather window) must cross-check. Round numbers ending in 0 ($50 photo package flat, "10–15% lift") are tells; if you cannot confirm a price from the operator's site, replace with a placeholder bracket `[$X]` so the operator fills it in.

4. **Hawaiian diacritics.** Scan both the markdown summary and the HTML artifact for: Hawaiʻi, kamaʻāina, Lānaʻi, Hāʻena, Mālama, Lūʻau, Kalalau, Oʻahu, Lāhainā, Lēʻahi, Kīlauea, Mānoa. Fix any that render without diacritics. The Source Serif 4 italic email pull-quotes need diacritic rendering verified by eye.

5. **Banned-word and em-dash sweep.** Run the LOD brand-voice banned word list (delve, leverage, utilize, holistic, robust, seamless, foster, paradigm, ecosystem unless literal, elevate, empower, unlock, harness, navigate as metaphor, streamline unless specific, realm, moreover, furthermore) and an em-dash sweep over both deliverables, including subject lines and email bodies. Fix any hit. Watch especially for "VIP," "exclusive," "luxury," "premium" on a kamaʻāina-led brand; those are voice-violations even if not on the banned list.

6. **No-fabrication rule.** Re-scan for claims that were not sourced. The upsell map must only include vectors the operator can actually support; do not invent a "captain's table" upgrade for an ag tour. Anxieties must come from the Business Context anxiety list or from a category-specific default that fits this operator. Service-flow upgrades must be booking-engine-aware; do not recommend FareHarbor add-on fields if the operator is on Peek.

7. **Internal consistency.** The markdown summary must match the HTML artifact. If the summary lists 3 upsell opportunities, the upsell map must show those exact 3 plus the 2 supporting ones. If the summary lists T-7 / T-1 / T+0 subject lines, the timeline cards must use those exact subjects. If the 4 anxieties in the summary are A/B/C/D, the anxiety table in the artifact must show those 4 (or 4 to 6, never fewer than the summary count).

8. **Upsell-portfolio mapping (per-skill check).** Every recommended upsell must map to something visible in the operator's actual portfolio drawn from the Business Context (signature experiences, retail attachments, café/F&B page, photo capability, gift-card SKU, premium tier products). Cross-check that no upsell is a hypothetical product the operator does not sell. If the operator has no photographer on staff, drop the photo-package upsell. If no café exists, drop the café reservation upsell. Replace any non-mappable vector with one that fits.

If all eight checks pass, deliver. If any fail, fix and re-run the relevant check.

---

## Tone rules

- Email bodies in the operator's brand voice from the Business Context. Family-led ag tour, family-led ag tour. Premium charter, premium charter. The brand-voice document is the source of truth.
- Subject lines under 60 chars. No emoji unless the brand voice already uses them. No "Aloha" unless the brand already uses it. No "ʻohana," "kamaʻāina," "Support Local" unless the brand already uses them.
- Hawaiian diacritics correct (ʻokina, kahakō) on business and place names.
- No fake first names ("Hi {firstName}"). Write the actual line.
- No em dashes anywhere. Commas, periods, parentheses, colons.
- No banned words from the LOD brand-voice document (delve, leverage, utilize, holistic, seamless, world-class, elevate, unlock, etc.). Plain language, active voice, contractions.
- Active voice. Contractions. Specific numbers and concrete examples whenever possible.
- T-7 carries the upsell. T-1 and T+0 do not. Do not stack a hard upsell into a logistics touch, it breaks trust.
- Never block a booking on the upsell. Easy yes, easy no, the guest can ignore it and still show up.
- Do not fabricate. If a vector or anxiety cannot be sampled from the Business Context, say so. State the gap, do not paper over it.

## Gotchas

- FareHarbor's add-on field has a per-product config flag, and not every plan tier supports it. Confirm the operator's plan and that the add-on is enabled at the product level before recommending a BE-native upsell. If it's gated, the fallback is a Square or Stripe payment link in the T-7 email body.
- Peek's add-on flow is a separate screen, not inline with checkout. Conversion drops noticeably vs. an inline FareHarbor add-on. Adjust the impact band when recommending.
- T-7 is unreachable for last-minute bookings (cruise pax, walk-up, sub-7-day-out). The sequence needs a fallback rule: if booking date is under 7 days out, collapse T-7 into the booking confirmation. Spell this out in the operator's instructions; most BE workflows don't handle it automatically.
- SMS in Hawaiʻi has carrier delivery quirks for international source markets (especially Japan and Korea numbers). T+0 SMS-only sequences leak no-shows for Asia-source-market guests. Use email plus SMS as belt-and-suspenders for those segments.
- Photo-package upsell in T-7 is high-margin but only works if the operator has a photographer or GoPro stack already in place. Don't recommend the upsell vector if the operator has no photo capture; the email creates an expectation the day-of can't deliver.
- Weather-policy language in T-1 must match the booking-engine's actual refund automation. If the BE doesn't auto-refund on cancellation, do not write "we'll refund you automatically" in the email. Match the email to the system's real behavior or the operator eats the support-ticket load.

## Anti-patterns (do not ship)

- Three identical upsell cards in a grid pretending to be a tier-stack. The upsell map is a stack, not a grid.
- Gradient text. Glassmorphism. Hero metric chrome. Pill-shaped tags. Rule-of-three closes where the third item is "and most importantly."
- "Premium," "exclusive," "luxury," "VIP" on a kamaʻāina-led brand.
- A T-7 email that opens with "Aloha {firstName}, we're so excited..."
- An upsell at T+0 morning. The guest is in their car. Trust window only.
- A weather-policy line buried in the footer. Surface refunds and reschedules where they reduce anxiety, not where they hide.

## What success looks like

The operator reads the report, pastes the markdown summary into their AI project memory, and ships the T-7 email plus one service-flow upgrade that same week. Two months later, attach rate on the photo package or café reservation lifts 10–15%, no-show rate drops, and the day-of inbound calls about parking and shoes go quiet.

---

*Built with the Hospitality Business Skills teammate · github.com/lightson-digital/hospitality-business-skills*

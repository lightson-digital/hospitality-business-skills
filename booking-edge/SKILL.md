---
name: Booking Edge
description: Book-stage skill for Hawaiʻi tour, lūʻau, attraction, and trip-experience operators. Use when the user says "review audit," "what are guests saying," "why aren't we converting," "fix our booking page," "comp parity," "how do we stack up," "do they pick us over [competitor]." Triangulates review voice, comp-set parity, and booking-page CRO fixes into one ranked playbook tied to verbatim quotes and real comp gaps. Outputs a paste-ready markdown summary plus an HTML artifact.
---

# Booking Edge

The Book-stage teammate. Answers the question your guest asks ten seconds before they click book: *"Do they pick me over the competition?"*

You answer it by triangulating three signals into one playbook:

1. **Review voice**, what guests actually say about you after the tour.
2. **Comp parity**, how your reviews and your booking page stack up against your direct competitors.
3. **CRO fixes**, what to change on the booking page to widen the edge.

Three signals, one ranked list of conversion fixes. Each fix is tied to a real review quote or a real comp gap. Nothing speculative.

Run after Business Context. If you have not run Business Context in this conversation, run it first. You need the business name, signature experiences, source markets, voice, and the comp set the operator already named. The comp set is the input. You are not guessing competitors here.

---

## When to use

The user gave you a tour-operator URL plus a Business Context document. They want to know:

- What guests are actually saying about us across review platforms.
- Where we're winning or losing against our direct competitors.
- What three things to fix on the booking page this week to convert more lookers into bookers.

If the user has not given you a URL, ask once:

> "What's the URL of the operator you want to audit, and do you have a Business Context document I can read?"

If they have no Business Context, run that skill first. Don't proceed without it. The comp set is required input.

---

## How it runs

Three signals, in order. Each signal feeds the next. By the time you write the three CRO fixes, every fix is anchored in a specific review quote, a specific comp gap, or both.

---

### Signal 1, Review voice (what guests actually say)

The methodology layer here is `customer-research`. You are mining the guest's unfiltered language across the platforms they actually use to vet a Hawaiʻi tour. You are not summarizing reviews. You are extracting verbatim language and surfacing the gaps between what guests ask and what the website answers.

#### 1a. Find the review surfaces

Locate the operator's review pages on every relevant platform. For B2C tour and attraction operators in Hawaiʻi, the surface set is:

- **Google Reviews** (`[business name] reviews google`), broadest sample, walk-up and Kamaʻāina-heavy.
- **TripAdvisor** (`[business name] tripadvisor`), mainland-visitor-heavy, longest reviews, biggest pre-trip-research traffic.
- **Viator** and **GetYourGuide** (`[business name] viator`, `[business name] getyourguide`), buying-intent reviews, often the OTA the booking actually happened on.
- **Yelp** (`[business name] yelp`), supplemental, especially if a café, retail, or attraction component is on site.
- **Klook**, relevant if the operator targets Asia-source markets.
- **Booking.com** or **Expedia activities**, if applicable.

For each platform you find, capture: total review count, average rating, recent trajectory if visible, and the URL.

**Low-volume flag.** If total reviews across all platforms are under 20, that is itself a finding. Surface it. A Hawaiʻi tour with under 20 reviews is invisible to most pre-trip researchers regardless of how good the tour is.

#### 1b. Sample 15–25 reviews

Read the most recent 5–10 reviews on each platform you can access. Mix 5-star, 4-star, and 1–2-star reviews. The negative reviews carry the highest signal because they are where pre-trip anxieties show up unfiltered.

For each review, capture:

- Star rating
- One verbatim phrase that captures the sentiment, in quotes, typos and all
- Which signature experience they are reviewing (tour, café, retail, group)
- Source market signal if visible (mainland city, kamaʻāina, international, cruise)

#### 1c. Extract the top 5 themes

Across all reviews, identify five recurring themes. For each theme:

- **Theme name**, written in the operator's voice, not generic. ("Tractor-wagon ride is the unlock for kids 5–10," not "family-friendly experience.")
- **Frequency**, "12 of 18 reviews."
- **Sentiment**, positive, mixed, or negative.
- **Verbatim quote**, one quote per theme, attributed to the platform it came from.

Negative themes are the gold. A theme like "tour was shorter than expected" or "ran out of mochi by 1pm" is worth ten positive reviews because it points to a specific page-level fix.

#### 1d. Find the FAQ gaps

Re-read the operator's homepage, tour page, FAQ page, and any policies pages. Compare what the website answers to what the reviews show guests are asking, mid-trip or in 1-star posts. Identify three to five questions that come up repeatedly in reviews but are not addressed on the site.

Common FAQ gaps for Hawaiʻi B2C trip experiences:

- "How long is the tour?" (matters because guests are slotting it into a North Shore loop or a cruise window)
- "What if it rains?" / weather-cancellation policy
- "Stroller / wheelchair / mobility on a working farm or boat?"
- "Is it kid-friendly? Age range?"
- "How early do I need to arrive? What's parking like?"
- "Refund policy if we miss it?"
- "Does the tour include the café, or is that separate?"
- "Will the tour run if there's only two of us?"

For Hawaiʻi specifically, also watch for:

- Cruise-pax-friendly window (does the tour fit a 4-hour shore-excursion slot?)
- Kamaʻāina pricing visibility (some operators bury it; reviewers ask)
- ʻŌlelo Hawaiʻi correctness in the brand voice on the page
- Group / school / wholesale (JTB) entry points

---

### Signal 2, Comp parity (how you stack up)

The methodology layer here is `competitor-profiling`. You are not building full competitor profiles. You are doing a focused parity sweep: same review surfaces, lighter sample, two outputs, the themes you own, and the themes they own that you don't.

#### 2a. Pull the comp set from Business Context

The Business Context already named two to three direct competitors. Use those. Do not add or substitute. The operator's judgment on comp set beats yours.

#### 2b. Read 5–10 reviews per competitor

Same review surfaces, lighter sample. Capture the same fields: rating, count, top three themes per competitor, two verbatim quotes per competitor.

For Hawaiʻi tour ops specifically, also note from the comp's booking pages:

- Tour duration stated up front?
- Weather / refund policy visible before the booking button?
- Mobility / kids' age / group-size language present?
- Direct booking vs. OTA-only? FareHarbor / Peek / Bōkun visible, or are they pushing Viator?
- Kamaʻāina pricing surfaced?

#### 2c. Render the parity diff

Two columns:

- **Themes you own**, themes that show up in your reviews and don't show up in theirs. (Example: "Family farm story / 4 generations" shows in Kahuku Farms reviews; doesn't show in Dole Plantation reviews. Big positioning moat.)
- **Themes they own that you don't**, themes that show up in their reviews and don't show up in yours. (Example: "Clear weather policy on booking page" or "Tour duration stated.")

The themes-they-own column is where the CRO fixes live. The themes-you-own column tells the operator what to amplify on the booking page hero.

Be honest. Don't soften the gaps. The point of the parity diff is to show the operator the one-week move.

---

### Signal 3, CRO fixes (the playbook)

The methodology layer here is `page-cro`. You are producing three specific fixes, ranked by impact times effort. Each fix has to tie back to either a Signal 1 review quote, a Signal 2 comp gap, or both. No speculative fixes. No "best practice" generic suggestions.

#### 3a. Identify the three fixes

For each fix:

- **What**, the specific change. ("Add a 'How long is the tour?' answer above the booking button on the Tour page.")
- **Why**, the evidence. Quote the review or name the comp gap. ("Three TripAdvisor reviews ask about tour duration. Lokoea Farms shows duration on its booking page; Kahuku Farms doesn't.")
- **Where**, the specific page and section. ("Tour page, between the hero and the FareHarbor button.")
- **Impact band**, High / Medium / Low. High means the fix likely moves direct-booking conversion measurably. Low means a polish item.
- **Effort band**, Low / Medium / High. Low is a copy change. High is a booking-flow rebuild.

#### 3b. Rank the fixes

Sort by impact × effort. The first fix is the highest impact, lowest effort. The last fix is the most ambitious one. The operator should be able to ship fix #1 the week of the audit.

Common high-impact, low-effort fixes for Hawaiʻi B2C tour ops:

- Surface tour duration above the booking button.
- Add a one-line weather / refund policy beside the booking button.
- Move the strongest review verbatim quote into the hero, with attribution.
- Make the kamaʻāina rate visible on the tour page, not buried on a promo subpage.
- Add a one-line "Is this good for kids?" / "Is this stroller-friendly?" answer.
- Add a cruise-pax window callout if applicable ("Fits a 4-hour North Shore stop").

#### 3c. Tie every fix to evidence

Every fix in the artifact carries the verbatim quote or comp gap that justifies it, attached to the fix. The operator reading the report should never wonder "why this fix?" The evidence is right there.

---

## Output

You emit two artifacts in the response, in this order:

1. A paste-ready markdown summary at the top of the chat (so the operator can drop it straight into their AI project memory or Claude Project).
2. A self-contained HTML artifact built on the Lights On design system.

### Markdown summary (paste-ready, in chat)

Emit this block above the HTML artifact. Roughly 14 lines. The operator pastes it into Claude Project knowledge, ChatGPT custom instructions, or any AI workspace.

````markdown
## Booking Edge, [Business Name] (paste into your AI project memory)

**Rating snapshot:**
- Google: [★ rating, N reviews]
- TripAdvisor: [★ rating, N reviews]
- Viator: [★ rating, N reviews]
- Yelp: [★ rating, N reviews]
[Note low-volume if under 20 total.]

**Top 3 review themes:**
1. [Theme], [frequency, sentiment]
2. [Theme], [frequency, sentiment]
3. [Theme], [frequency, sentiment]

**Top 2 FAQ gaps:**
1. [Question]
2. [Question]

**Top comp parity gap(s):**
- [What competitor X does that this operator doesn't.]

**3 fixes (ranked):**
1. [Fix 1, one line.]
2. [Fix 2, one line.]
3. [Fix 3, one line.]
````

### HTML artifact (self-contained)

The HTML below is the canonical layout. Three clearly labeled sections so the audience sees the triangulation visually. Inter from Google Fonts (300 display, 400 UI, 600 for labels and badges). Source Serif 4 from Google Fonts as the serif companion for the verbatim pull-quotes. Heading `#061b31`, body `#273951`, label `#273951`, accent `#533afd`. Border `#e5edf5`. White background. Radii 4–8px (999px only on the provenance badge chip). Subtle blue-tinted shadows ONLY on featured cards (rgba(50,50,93,0.10) at 0px 12px 20px 0px). Plain border for everything else. No gradient text. No glassmorphism. No pill-shaped tags. No hero-metric chrome.

**Provenance badge.** Stamp the artifact with `Powered by Lights On · ran on [YYYY-MM-DD]` immediately after the subtitle, where `[YYYY-MM-DD]` is the actual date the skill is run. Use the `.stamp` class in the template below. The `·` character is U+00B7 middle dot, single space on either side.

Replace bracketed placeholders with the operator's actual data. Do not strip diacritics. Do not soften negative quotes.

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Booking Edge · [Business Name]</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600&family=Source+Serif+4:ital,wght@1,400&display=swap" rel="stylesheet">
<style>
  :root {
    --heading: #061b31;
    --label: #273951;
    --body: #273951;
    --accent: #533afd;
    --border: #e5edf5;
    --border-soft: #f0f4f9;
    --bg: #ffffff;
    --success-bg: rgba(21,190,83,0.10);
    --success-text: #108c3d;
    --lemon-bg: rgba(155,104,41,0.10);
    --lemon-text: #9b6829;
    --ruby-bg: rgba(234,34,97,0.10);
    --ruby-text: #ea2261;
    --shadow-feature: rgba(50,50,93,0.10) 0px 12px 20px 0px;
  }
  * { box-sizing: border-box; }
  body {
    font-family: 'Inter', -apple-system, 'SF Pro Display', sans-serif;
    font-weight: 300;
    font-size: 17px;
    max-width: 1040px;
    margin: 40px auto;
    padding: 0 32px;
    color: var(--heading);
    background: var(--bg);
    line-height: 1.55;
    font-feature-settings: "ss01";
    -webkit-font-smoothing: antialiased;
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
    line-height: 1.1;
    margin: 0 0 4px;
    color: var(--heading);
  }
  .sub {
    font-size: 20px;
    font-weight: 300;
    color: var(--body);
    margin-bottom: 12px;
    max-width: 720px;
    line-height: 1.5;
  }
  .section-label {
    display: inline-block;
    font-size: 13px;
    font-weight: 600;
    letter-spacing: 0.16em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 14px;
  }
  h2 {
    font-size: 24px;
    font-weight: 300;
    letter-spacing: -0.3px;
    line-height: 1.15;
    color: var(--heading);
    margin: 0 0 18px;
  }
  .card {
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 28px 32px;
    background: var(--bg);
    margin-bottom: 20px;
  }
  .card.featured {
    box-shadow: var(--shadow-feature);
  }
  /* Platform row */
  .platforms {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 10px;
    margin-bottom: 28px;
  }
  .platform {
    padding: 14px 12px;
    border: 1px solid var(--border);
    border-radius: 6px;
    text-align: left;
  }
  .platform .name {
    font-size: 11px;
    color: var(--label);
    letter-spacing: 0.10em;
    text-transform: uppercase;
    margin-bottom: 8px;
  }
  .platform .rating {
    font-size: 24px;
    font-weight: 300;
    color: var(--heading);
    font-feature-settings: "tnum";
    font-variant-numeric: tabular-nums;
    line-height: 1;
    margin-bottom: 4px;
  }
  .platform .count {
    font-size: 13px;
    color: var(--body);
    font-feature-settings: "tnum";
    font-variant-numeric: tabular-nums;
  }
  /* Themes (Signal 1) */
  .theme {
    padding: 18px 0;
    border-bottom: 1px solid var(--border-soft);
  }
  .theme:last-child { border-bottom: none; }
  .theme:first-child { padding-top: 4px; }
  .theme .head {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    gap: 16px;
    margin-bottom: 8px;
  }
  .theme .name {
    font-size: 16px;
    font-weight: 400;
    color: var(--heading);
  }
  .theme .meta {
    font-size: 12px;
    color: var(--body);
    font-feature-settings: "tnum";
    white-space: nowrap;
  }
  .chip {
    display: inline-block;
    font-size: 10px;
    font-weight: 400;
    padding: 2px 8px;
    border-radius: 4px;
    margin-left: 6px;
    letter-spacing: 0.04em;
  }
  .chip.pos { background: var(--success-bg); color: var(--success-text); }
  .chip.mix { background: var(--lemon-bg); color: var(--lemon-text); }
  .chip.neg { background: var(--ruby-bg); color: var(--ruby-text); }
  .quote {
    font-family: 'Source Serif 4', Georgia, serif;
    font-style: italic;
    font-weight: 400;
    font-size: 16px;
    color: var(--label);
    line-height: 1.55;
    padding: 4px 0 4px 16px;
    border-left: 2px solid var(--accent);
    margin-top: 6px;
  }
  .quote .attr {
    font-family: 'Inter', sans-serif;
    font-style: normal;
    font-size: 12px;
    color: var(--body);
    display: block;
    margin-top: 6px;
  }
  /* FAQ gaps */
  .gap {
    padding: 14px 0;
    border-bottom: 1px solid var(--border-soft);
  }
  .gap:last-child { border-bottom: none; }
  .gap:first-child { padding-top: 4px; }
  .gap .q {
    font-size: 16px;
    color: var(--heading);
    font-weight: 400;
  }
  .gap .a {
    font-size: 16px;
    color: var(--body);
    margin-top: 4px;
    line-height: 1.55;
  }
  /* Parity diff (Signal 2) */
  .parity {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 24px;
  }
  .parity-col h3 {
    font-size: 15px;
    font-weight: 400;
    letter-spacing: 0.04em;
    color: var(--label);
    margin: 0 0 12px;
    padding-bottom: 8px;
    border-bottom: 1px solid var(--border);
  }
  .parity-item {
    font-size: 16px;
    color: var(--heading);
    padding: 10px 0;
    border-bottom: 1px solid var(--border-soft);
    line-height: 1.5;
  }
  .parity-item:last-child { border-bottom: none; }
  .parity-item .source {
    font-size: 13px;
    color: var(--body);
    display: block;
    margin-top: 4px;
    line-height: 1.5;
  }
  /* Fixes (Signal 3) */
  .fix {
    padding: 22px 0;
    border-bottom: 1px solid var(--border-soft);
    display: grid;
    grid-template-columns: 32px 1fr;
    gap: 16px;
  }
  .fix:last-child { border-bottom: none; }
  .fix:first-child { padding-top: 4px; }
  .fix .num {
    font-size: 22px;
    font-weight: 300;
    color: var(--accent);
    font-feature-settings: "tnum";
    line-height: 1;
    padding-top: 2px;
  }
  .fix .what {
    font-size: 17px;
    font-weight: 400;
    color: var(--heading);
    margin: 0 0 6px;
    line-height: 1.35;
  }
  .fix .where {
    font-size: 16px;
    color: var(--body);
    margin-bottom: 12px;
    line-height: 1.5;
  }
  .fix .pills {
    display: flex;
    gap: 8px;
    margin-bottom: 12px;
  }
  .pill {
    font-size: 11px;
    color: var(--label);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 3px 8px;
    letter-spacing: 0.04em;
  }
  .fix .evidence {
    font-family: 'Source Serif 4', Georgia, serif;
    font-style: italic;
    font-weight: 400;
    font-size: 16px;
    color: var(--label);
    line-height: 1.55;
    padding: 4px 0 4px 14px;
    border-left: 2px solid var(--border);
    margin-top: 4px;
  }
  .fix .evidence .attr {
    font-family: 'Inter', sans-serif;
    font-style: normal;
    font-size: 12px;
    color: var(--body);
    display: block;
    margin-top: 4px;
  }
  .footer {
    margin-top: 40px;
    font-size: 13px;
    color: #425466;
    text-align: center;
    padding-top: 20px;
    border-top: 1px solid var(--border);
  }
  .footer a {
    color: var(--accent);
    text-decoration: none;
  }
  .footer a:hover { text-decoration: underline; }
  @media (max-width: 700px) {
    body { margin: 24px auto; }
    h1 { font-size: 32px; }
    .platforms { grid-template-columns: repeat(2, 1fr); }
    .parity { grid-template-columns: 1fr; gap: 16px; }
    .card { padding: 22px 20px; }
  }
</style>
</head>
<body>
  <div class="eyebrow">Book · Booking Edge</div>
  <h1>[Business Name]</h1>
  <div class="sub">Three signals, one playbook. What guests say, how you stack up against [Comp 1] and [Comp 2], and what to fix on the booking page this week.</div>
  <div class="stamp">Powered by Lights On · ran on [YYYY-MM-DD]</div>

  <div class="platforms">
    <div class="platform"><div class="name">Google</div><div class="rating">[4.7]</div><div class="count">[N] reviews</div></div>
    <div class="platform"><div class="name">TripAdvisor</div><div class="rating">[4.5]</div><div class="count">[N] reviews</div></div>
    <div class="platform"><div class="name">Viator</div><div class="rating">[4.8]</div><div class="count">[N] reviews</div></div>
    <div class="platform"><div class="name">Yelp</div><div class="rating">[4.4]</div><div class="count">[N] reviews</div></div>
  </div>

  <div class="card featured">
    <span class="section-label">Signal 1 · Review voice</span>
    <h2>What guests actually say</h2>
    <div class="theme">
      <div class="head"><div class="name">[Theme 1 in operator voice]</div><div class="meta">[12 of 18] <span class="chip pos">positive</span></div></div>
      <div class="quote">"[Verbatim quote, typos and all.]"<span class="attr">[Reviewer first name], [Platform]</span></div>
    </div>
    <div class="theme">
      <div class="head"><div class="name">[Theme 2]</div><div class="meta">[8 of 18] <span class="chip pos">positive</span></div></div>
      <div class="quote">"[Verbatim quote.]"<span class="attr">[Reviewer], [Platform]</span></div>
    </div>
    <div class="theme">
      <div class="head"><div class="name">[Theme 3]</div><div class="meta">[6 of 18] <span class="chip mix">mixed</span></div></div>
      <div class="quote">"[Verbatim quote.]"<span class="attr">[Reviewer], [Platform]</span></div>
    </div>
    <div class="theme">
      <div class="head"><div class="name">[Theme 4]</div><div class="meta">[4 of 18] <span class="chip neg">negative</span></div></div>
      <div class="quote">"[Verbatim quote, typos and all.]"<span class="attr">[Reviewer], [Platform]</span></div>
    </div>
    <div class="theme">
      <div class="head"><div class="name">[Theme 5]</div><div class="meta">[3 of 18] <span class="chip neg">negative</span></div></div>
      <div class="quote">"[Verbatim quote.]"<span class="attr">[Reviewer], [Platform]</span></div>
    </div>
  </div>

  <div class="card">
    <span class="section-label">Signal 1 · FAQ gaps</span>
    <h2>Questions guests ask that the website doesn't answer</h2>
    <div class="gap"><div class="q">[Question 1]</div><div class="a">[Came up in N reviews. Currently nowhere on the site.]</div></div>
    <div class="gap"><div class="q">[Question 2]</div><div class="a">[Came up in N reviews. Buried on policy subpage.]</div></div>
    <div class="gap"><div class="q">[Question 3]</div><div class="a">[Came up in N reviews. Not addressed.]</div></div>
  </div>

  <div class="card">
    <span class="section-label">Signal 2 · Comp parity</span>
    <h2>Where you stack up against [Comp 1] and [Comp 2]</h2>
    <div class="parity">
      <div class="parity-col">
        <h3>Themes you own</h3>
        <div class="parity-item">[Theme]<span class="source">Shows up in [N] of your reviews; not in either comp's reviews.</span></div>
        <div class="parity-item">[Theme]<span class="source">[Source detail.]</span></div>
        <div class="parity-item">[Theme]<span class="source">[Source detail.]</span></div>
      </div>
      <div class="parity-col">
        <h3>Themes they own that you don't</h3>
        <div class="parity-item">[Theme or page mechanic]<span class="source">[Comp 1] surfaces this on the booking page; you don't.</span></div>
        <div class="parity-item">[Theme]<span class="source">[Comp 2] reviews mention this consistently; yours don't.</span></div>
        <div class="parity-item">[Theme]<span class="source">[Source detail.]</span></div>
      </div>
    </div>
  </div>

  <div class="card featured">
    <span class="section-label">Signal 3 · CRO fixes</span>
    <h2>Three fixes, ranked</h2>
    <div class="fix">
      <div class="num">1</div>
      <div>
        <div class="what">[Fix 1, what to change, in the operator's voice.]</div>
        <div class="where">[Specific page and section.]</div>
        <div class="pills"><span class="pill">Impact: High</span><span class="pill">Effort: Low</span></div>
        <div class="evidence">"[Verbatim review quote OR comp gap line that justifies this fix.]"<span class="attr">[Source: reviewer / platform OR comp parity gap]</span></div>
      </div>
    </div>
    <div class="fix">
      <div class="num">2</div>
      <div>
        <div class="what">[Fix 2.]</div>
        <div class="where">[Specific page and section.]</div>
        <div class="pills"><span class="pill">Impact: High</span><span class="pill">Effort: Medium</span></div>
        <div class="evidence">"[Verbatim review quote OR comp gap.]"<span class="attr">[Source.]</span></div>
      </div>
    </div>
    <div class="fix">
      <div class="num">3</div>
      <div>
        <div class="what">[Fix 3.]</div>
        <div class="where">[Specific page and section.]</div>
        <div class="pills"><span class="pill">Impact: Medium</span><span class="pill">Effort: Medium</span></div>
        <div class="evidence">"[Verbatim review quote OR comp gap.]"<span class="attr">[Source.]</span></div>
      </div>
    </div>
  </div>

  <div class="footer">Built with the Hospitality Business Skills teammate · <a href="https://lightson.co">Powered by Lights On</a> · github.com/lightson-digital/hospitality-business-skills</div>
</body>
</html>
```

---

## Phase 3 — Fact-check pass (mandatory)

Run this AFTER both the paste-ready markdown summary and the HTML artifact are drafted, and BEFORE you hand them to the user. This is a quality gate, not a watermark. If a check fails, fix in place silently and re-verify. Do not add a "fact-check passed" note to the visible output.

1. **URL liveness.** Pick 2 to 3 cited URLs at random from the review platform set (Google Reviews, TripAdvisor, Viator, Yelp), the comp set (Comp 1 and Comp 2 booking pages), and the operator's own pages referenced in fixes. Re-fetch each via web_fetch. If any returns 404, blocked, CAPTCHA, or wrong content, drop the citation or replace with one that resolves. Yelp's CAPTCHA wall is expected; note it but do not invent a count.

2. **Quote provenance.** For every verbatim review quote pulled into the Theme cards, the FAQ-gap section, or the evidence line under each fix, confirm the exact string appears on the cited platform. If you cannot verify within a reasonable sample (the page changed, the review was deleted, the platform blocked the fetch), mark the quote `(paraphrased)` rather than verbatim, OR drop it. The Tone rules require typos preserved; that means the verified string carries the typos too.

3. **Number sanity.** Every star rating, review count, theme frequency ("12 of 18 reviews"), and comp-parity count must cross-check against the source. Round numbers (4.5 stars exactly, 100 reviews flat) deserve a second look. If you cannot confirm a number, replace with a qualitative phrase ("dozens of reviews," "consistently 4-star and above," "single-digit review count").

4. **Hawaiian diacritics.** Scan both the markdown summary and the HTML artifact for: Hawaiʻi, kamaʻāina, Lānaʻi, Hāʻena, Mālama, Lūʻau, Kalalau, Oʻahu, Lāhainā, Lēʻahi, Kīlauea, Mānoa. Fix any that render without diacritics. The Source Serif 4 italic in pull-quotes still needs to render the diacritic correctly; verify by eye if the font fallback drops them.

5. **Banned-word and em-dash sweep.** Run the LOD brand-voice banned word list (delve, leverage, utilize, holistic, robust, seamless, foster, paradigm, ecosystem unless literal, elevate, empower, unlock, harness, navigate as metaphor, streamline unless specific, realm, moreover, furthermore) and an em-dash sweep over both deliverables. Fix any hit. The middle dot `·` is correct; em dash is not.

6. **No-fabrication rule.** Re-scan the artifact for claims that were not sourced. Every CRO fix must tie to a Signal 1 review quote or a Signal 2 comp gap; if the evidence line is generic ("best practice"), drop the fix or replace it. Themes-they-own and themes-you-own claims need verbatim source backup. If a comp is OTA-only and you skipped the booking-page parity row, the artifact must say so plainly, not paper over it.

7. **Internal consistency.** The markdown summary must match the HTML artifact. If the summary says "Top 3 review themes: A, B, C," the Signal 1 cards must show those three at the top with matching frequencies and sentiments. If the summary names "Comp 1 and Comp 2," the parity diff must reference those same names. If the summary lists "3 fixes," the Signal 3 section must show 3 fixes with the same one-line headlines.

8. **OTA-count freshness (per-skill check).** OTA review counts shift weekly. Stamp the rating snapshot block in the HTML artifact with the date the data was pulled (it lives in the provenance badge already; verify it matches the actual run date). Add a one-line caveat near the Platforms grid that reads: "Review counts pulled on [date]. OTA totals can shift week to week." Verify the line is present and the date is today's run date.

If all eight checks pass, deliver. If any fail, fix and re-run the relevant check.

---

## Tone rules

- Quote reviewers verbatim. Typos, ALL CAPS, broken English, all of it. The realness is the proof.
- Don't soften negative themes. If four reviewers mention the tour ran short, surface it. If guests are upset that the mochi sells out by 1pm, surface it.
- If review counts are low (under 20 across all platforms), say so. That's a finding, not a footnote.
- Hawaiian diacritics correct. ʻOkina and kahakō render properly. Place names spelled the way the operator's site spells them.
- No em dashes. Commas, periods, parentheses, colons.
- No banned words from the LOD brand voice (delve, leverage, utilize, holistic, robust, seamless, foster, paradigm, etc.).
- Active voice. Contractions. First and second person. "We saw three reviewers ask about tour length. The booking page doesn't answer it."
- Don't fabricate. If you couldn't access a platform, say so. If a comp's reviews are sparse, say so.
- Every CRO fix is anchored to a Signal 1 quote or a Signal 2 comp gap. No speculative fixes.

---

## Gotchas

- Yelp aggressively blocks scraping. If the page returns 403 or a CAPTCHA, pull the rating count from the search-result snippet and move on. Don't burn a turn trying to bypass it.
- Viator and GetYourGuide reviews are filtered by the OTA before publication. They skew positive vs. Google. Weight Google and TripAdvisor higher when extracting negative themes.
- TripAdvisor reviews are biased mainland-heavy, especially for Oʻahu operators. If the operator's source markets include Japan or kamaʻāina, Google Reviews carry the truer voice. Note this in the report.
- Comp set from Business Context sometimes includes an OTA-only operator (no direct site, only a Viator listing). The booking-page CRO fixes don't apply, only the review-voice signals. Flag this and skip the comp's booking-page parity row.
- "Tour duration stated up front" sounds trivial but is the single most common comp gap that costs Hawaiʻi tour operators bookings. If the comp shows duration and the operator doesn't, that's almost always Fix #1.
- FareHarbor, Peek, and Bōkun all support an "above the booking button" content slot. The CRO fixes that involve adding microcopy are usually Low effort because of this. Confirm the operator's booking engine before scoring effort.

## What success looks like

The operator reads the artifact and immediately knows three things:

1. The two or three themes their guests already love (and which to put in the hero).
2. The one or two things their direct competitors do better on the booking page.
3. The single fix to ship this week, the one to ship this month, and the one to plan for next quarter.

The paste-ready markdown summary lands in their AI project memory. From that point forward, every other AI workflow they run on this business (pre-arrival emails, follow-up drafts, comparison-page copy, ad creative) reads it and produces sharper output without re-asking the same questions.

---

## Related skills in this repo

- **Business Context**, required input. Run first.
- **Discoverability** (forthcoming), pre-Book stage; the question is "do they find me at all?"
- **Repeat-Visit** (forthcoming), post-Experience stage; the question is "do they come back?"

*Built with the Hospitality Business Skills teammate · github.com/lightson-digital/hospitality-business-skills*

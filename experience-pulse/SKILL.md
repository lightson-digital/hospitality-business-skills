---
name: Experience Pulse
description: Quarterly market-research sweep across the entire public traveler-voice surface (reviews + Reddit + blogs + YouTube + comp set + industry context) for a Hawaiʻi B2C trip-experience operator. Synthesizes into 5 buckets (love / hate / fear / category-changing / comp does, you don't) and ships 3 ranked service-change recommendations. Includes a Refine interview that walks the operator through what's actually changeable vs. fixed. Output is a paste-ready markdown summary plus a Stripe-grade HTML artifact.
---

# Experience Pulse

The Experience-stage teammate. Answers the question travelers can't tell you to your face: *"Are travelers getting the experience they actually wanted, and what are competitors doing better?"*

Run this quarterly. Run it after Business Context. If you have not run Business Context in this conversation, run it first. You need the business name, signature experiences, comp set, and brand voice to do this right.

## What this skill is, and what it is not

Experience Pulse is a strategic, post-experience review of the actual product the operator runs. It looks at every public surface where travelers talk about the experience after they've had it, plus what's shifting in the category, plus what direct competitors are doing that the operator is not. The output is three concrete service-change recommendations, ranked by impact and effort, with a built-in interview that asks the operator which ones are actually changeable in the next 30 days.

This is not Booking Edge. Booking Edge (the Book-stage skill) reads major review platforms to find the FAQ gaps that cost bookings before the trip. Experience Pulse reads the full public traveler-voice surface to find the service changes that improve the trip itself. Different lens, different surfaces, different output, different cadence.

| | Booking Edge | Experience Pulse |
|---|---|---|
| Lens | Pre-booking decision (FAQ gaps, conversion blockers) | Post-experience reality (what worked, what didn't) |
| Surfaces | Major review platforms only | Same plus Reddit plus blogs plus YouTube plus industry context |
| Output | 3 booking-page fixes | 3 service-change recs plus Refine interview |
| Cadence | Run once, fix the page | Run quarterly, evolve the experience |

State this contrast out loud to the operator at the start of the run, so they don't expect a duplicate of the Booking Edge report.

## When to use

The user gives you a tour operator URL and asks for a service review, an experience audit, a "what should we change," a quarterly check, or any variant of "what are travelers actually saying about us." Or the user is preparing for an off-season planning meeting and wants to know what to fix before the next peak.

If the user has not given you a URL, ask once:

> "What's the URL of the operator you want me to pulse? And do you want me to read your Business Context doc first if you have one?"

## How the skill runs

Two phases. The user can stop after Phase 1.

1. **Pulse.** You read every public surface where travelers talk. You read what comps are doing. You read what's shifting in the category on this island. You synthesize into 5 buckets and 3 ranked recommendations. You ship a paste-ready markdown summary plus a Stripe-grade HTML artifact. You stamp the doc `First Draft.`
2. **Refine.** You walk the operator through six questions, one at a time. You recommend an answer first based on the first draft. After each answer, you restate the working answer in plain words so the operator can confirm or correct. When the operator stops the interview, you regenerate the artifact with selections folded in and stamp it `Refined.`

---

## Phase 1 · Pulse

### Step 1. Multi-surface traveler-voice sweep

Hit every public surface where travelers talk. State the surfaces you searched and how many sources you actually read. If a surface returns nothing, say so plainly. Low signal on Reddit is itself a finding.

**Major review platforms (read 5 to 10 reviews per platform, mix 5-star, 4-star, 1 to 2-star):**
- Google Reviews (search `[business name] reviews google`)
- TripAdvisor (search `[business name] tripadvisor`)
- Viator (search `[business name] viator reviews`)
- Yelp (search `[business name] yelp`)
- GetYourGuide (search `[business name] getyourguide`)
- Klook if it's an Asia-source-market operator (search `[business name] klook`)
- Booking.com Things-to-Do if it's lodging-adjacent
- Apple Maps reviews (search `[business name] apple maps`)

**Reddit (search both the business name and the category):**
- `[business name]` site:reddit.com
- `[category] [island]` site:reddit.com (e.g. "snorkel tour Maui," "luau Oahu," "farm tour North Shore")
- Subreddits to lean into: r/Hawaii, r/oahu, r/Maui, r/bigisland, r/visitinghawaii, r/travel, r/oahuhiking, r/MauiVisitors, r/japantravel if relevant
- Look for: trip-report posts, "is X worth it" threads, "what would you do differently" threads
- Reddit travelers tell the truth in ways they won't on a review platform. Mine accordingly.

**Travel blogs:**
- Search `best [category] [island]` (e.g. "best North Shore farm tour")
- Search `Hawaii blog [category]`
- Search `[business name] review blog`
- Beat-blogs to know: Hawaii Magazine, Honolulu Magazine, Frolic Hawaii, Beat of Hawaii, Maui Now, Go Visit Hawaii, This Hawaii Life, To Hawaii dot com, The Hawaii Vacation Guide

**YouTube:**
- Search `[business name]` on YouTube and read the comments on the top 3 to 5 videos
- Search `[category] [island] vlog` and read comments on travel vlogs that cover this category, even if the operator isn't named. Travelers compare in the comments.
- Capture verbatim comments. YouTube comments are unfiltered.

**Capture for each source:**
- Source platform, URL, date if visible
- Verbatim quote (typos and all)
- Sentiment (positive / mixed / negative)
- Theme tag (love / hate / fear / category-shift / comp-mention)

If web_fetch or web_search returns nothing for a surface, state that surface returned nothing and move on. Do not fabricate. Low signal is itself a finding the operator should hear.

### Step 2. Comp set sweep (lighter)

For the top 2 direct competitors from Business Context, hit the same surfaces (review platforms, top 1 to 2 Reddit threads, top 1 to 2 blogs). You're looking for: what specific service moves do competitors run that this operator does not? Not features on a homepage. Service moves travelers actually mention. Examples: photo package included, narration in 3 languages, take-home gift, reserved parking, group size cap, booking-flexibility policy, guide credentials, weather contingency, snack format.

Capture as: "they do X, you do Y." Pull the verbatim source.

### Step 3. Industry-context scan (last 90 days)

Run a web search for the latest 90 days of category and island-specific narrative shaping traveler expectations. The traveler is bringing the news cycle into the booking with them.

Examples to look for, depending on island and category:
- Maui post-fire travel anxiety, Lāhainā recovery, "is it OK to visit Maui yet"
- Hanauma Bay reservation system, Diamond Head reservation system, Lēʻahi
- Sunscreen ban (oxybenzone / octinoxate), reef-safe enforcement
- North Shore shark sightings, jellyfish calendar
- Big Island volcano activity, vog impact, Volcanoes National Park access
- Kuleana / over-tourism conversations, Mālama Hawaiʻi pledge
- Cruise-pax shore-time changes (NCL Pride of America scheduling, foreign-flag itineraries)
- JTB / Japanese-source-market pivot patterns post-FX-shock
- Climate-change weather disruption (rain, swell, fire)
- Permit and access changes (Hāʻena, Kalalau, Stairway to Heaven)

Capture each relevant trend as: trend description, when it shifted, source URL.

### Step 4. Synthesize into 5 buckets

This is the heart of the skill. Cluster every quote and signal into one of five buckets. Each bucket is its own visual section in the artifact, deliberately distinct in shape, so the report doesn't look like five identical cards.

1. **Travelers love.** The peak moments. The thing they tell their friends about. Pull 3 to 5 verbatim quotes. Apply peak-end rule from marketing-psychology: the peak moment is what gets remembered, not the average. Identify the peak that's already happening organically.
2. **Travelers hate.** The friction patterns, the broken promises, the operational misses. Bullet list with frequency badges. "12 mentions across TripAdvisor and Reddit." Don't soften.
3. **Travelers fear.** The anxieties travelers brought into the booking. Some are addressed on the website, some are not. Flag which is which. This is where pre-arrival communication and on-page FAQ live.
4. **What's changing in the category.** The 2 to 4 industry trends shifting traveler expectations on this island for this category. Each with source citation.
5. **Comp does, you don't.** Side by side. "They do X, you do Y." Pull the verbatim source for the "they do X" side.

### Step 5. Three service-change recommendations

Synthesize the buckets into 3 specific service changes. Rank by impact times effort. Each recommendation carries:

- **Change name** plain-language description of the change
- **Evidence** which traveler quotes, which competitors, which trends point to this
- **Where in the experience** pre-arrival, on-tour moment, post-experience
- **Category** snack, narration, group size, technology, photo, payment, cadence, scheduling, communication, kuleana / cultural element, accessibility, weather contingency
- **Effort** Low / Mid / High
- **Impact** Low / Mid / High
- **30-day next step** the first concrete operational step the operator could take in the next 30 days

Apply marketing-psychology where it earns its keep:
- **Peak-end rule** for double-down moves on the "love" bucket (amplify the peak that already works)
- **Loss aversion** for surfacing a change that closes a "fear" gap travelers carry into the booking
- **Pratfall effect** for changes that are honest about a trade-off the operator is making (small admission builds trust)
- **Mere exposure** for the photo / share-the-moment moves that turn travelers into channel for you

### Step 6. Render the deliverables

Two outputs in this order, in the same response:

1. A paste-ready markdown summary block at the top (the operator drops this into their AI project memory)
2. A self-contained HTML artifact (Stripe-grade design, see artifact spec below)

Stamp both `First Draft.`

### Step 7. Hand off and offer Refine

After delivering the markdown plus HTML, say plainly:

> "That's the First Draft. I read [N] reviews across [N] platforms, plus [N] Reddit threads, plus [N] blogs, plus YouTube comments on [N] videos. I scanned [N] industry-context trends from the last 90 days.
>
> Three service-change recommendations are on the page. Now the question is: which ones are actually changeable in the next 30 days, and which ones are fixed because of capital cost, regulation, or physical constraint?
>
> I'll walk you through six questions, one at a time, and rebuild the artifact with your selections. Or ship as-is."

If the user says ship / done / no thanks, end. The First Draft is the canonical document.
If the user says refine / yes / continue, run Phase 2.

---

## Phase 2 · Refine (one question at a time)

Walk the user through these six branches in this order. **One question per turn.** Always recommend an answer first, drawn from the First Draft. Never stack questions. After each answer, restate the working answer in plain words so the user can confirm or correct, then move to the next.

This is the same grill-me embedded pattern as Business Context. The operator owns the final document. You're a researcher with a pen, not an oracle.

1. **Changeable vs. fixed.** Of the 3 service-change recs, which is actually changeable in the next 30 days? Which is fixed (capital cost, regulation, physical constraint, lease term, staffing pipeline)? *Recommendation: lead with the easiest of the three.*
2. **History.** Has the operator tried a similar change before? What happened? *Recommendation: ask before assuming greenfield.*
3. **Peak to amplify.** Which "love" theme should you double down on? *Recommendation: pick the verbatim quote that gets repeated most often. Peak-end rule says the peak is what travelers tell their friends about, so amplify the peak that's already organic.*
4. **Hate that's fixable.** Which "hate" theme is operationally fixable vs. structurally fixed? *Recommendation: separate the operational misses (training, sequencing, communication) from the structural ones (lease, road, permit, weather).*
5. **Brand-voice fit.** Of the 3 recs, which one matches the operator's brand voice and "What You Are NOT" line from Business Context? *Recommendation: kill any rec that drifts toward what the operator has explicitly said they are not.*
6. **Ship one.** Pick one to ship by [date 30 days from today]. What's the first concrete step? *Recommendation: pull from the 30-day next step on the chosen rec.*

When the user signals stop ("done," "ship it," "good enough"), regenerate the markdown summary plus HTML artifact with the new answers folded in. Stamp both `Refined.` Tell the user where to paste the markdown: any AI project, custom GPT, Claude Project knowledge, ChatGPT memory.

---

## Output 1 · paste-ready markdown summary

Render this above the HTML artifact. ~15 to 18 lines. Operator can copy it straight into their AI project memory.

````markdown
## Experience Pulse · [Business Name] (paste into your AI project memory)

*Stamp:* **[First Draft / Refined]** · *Last updated:* [YYYY-MM-DD] · *Source:* [URL]

**5-bucket headlines:**
- Love: [one-line headline of the dominant peak moment]
- Hate: [one-line headline of the dominant friction pattern]
- Fear: [one-line headline of the dominant anxiety travelers carry in]
- Category shifting: [one-line headline of the dominant industry trend]
- Comp does, you don't: [one-line headline of the most striking gap]

**3 service-change recs (ranked by impact × effort):**
1. [Change name] · Effort [Low/Mid/High] · Impact [Low/Mid/High] · [Where in experience]
2. [Change name] · Effort [Low/Mid/High] · Impact [Low/Mid/High] · [Where in experience]
3. [Change name] · Effort [Low/Mid/High] · Impact [Low/Mid/High] · [Where in experience]

**Top sources cited per surface:**
- Reviews: [Platform 1 URL], [Platform 2 URL]
- Reddit: [Top thread URL]
- Blogs: [Top blog URL]
- YouTube: [Top video URL]
- Industry: [Top news URL]
- Comps: [Comp 1 URL], [Comp 2 URL]
````

---

## Output 2 · HTML artifact (self-contained, Stripe-grade)

Render as a complete HTML document, inline `<style>`, no external dependencies except Inter from Google Fonts. The operator should be able to open this file and have it look right.

### Design system (Lights On / Stripe-derived)

- Font: Inter from Google Fonts. Weight 300 for display headings, 400 for UI and body
- Heading color: `#061b31`
- Body color: `#64748d`
- Label color: `#273951`
- Accent: `#533afd`
- Border default: `#e5edf5`
- Background: `#ffffff`
- Radii: 4 to 8px only. Never pill. Never large rounding.
- Shadow: subtle blue-tinted `rgba(50,50,93,0.10) 0px 12px 20px 0px` ONLY on featured cards (the 3 service-change recs and one section header). Plain `1px solid #e5edf5` border for the rest.
- Letter-spacing: tighten at display sizes (e.g. -0.96px at 48px headline, -0.64px at 32px section heads)

### Layout philosophy

The 5 buckets are the design hook. Each bucket renders as a deliberately distinct visual section so the artifact doesn't look like a generic 5-card grid. Hold the line on this. If you collapse them into 5 lookalike cards, you've defaulted to AI slop.

**Bucket 1 · Travelers love.** Render as 3 to 5 left-bordered serif-italic pull-quotes with attributed source platform underneath. Left border in accent purple. No card chrome. Generous vertical spacing. Reads like a wall of quotes.

**Bucket 2 · Travelers hate.** Render as a tight bullet list with frequency badges on the right. Each row: friction phrase on the left, badge on the right showing source count ("12 mentions across TripAdvisor + Reddit"). Badge is a small `1px solid` outlined rect, not a pill.

**Bucket 3 · Travelers fear.** Render as a 4-quadrant 2x2 grid. Each quadrant: anxiety statement, then label "Addressed on site" or "Not addressed" in label color. Plain border. No fill.

**Bucket 4 · Category changing.** Render as a 3-row trend timeline. Each row: trend name on the left, when it shifted in the middle, source citation URL on the right. Each row separated by `1px solid #e5edf5`. Small label-color caption under each trend name.

**Bucket 5 · Comp does, you don't.** Render as a 2-column side-by-side table. Left column header "They do." Right column header "You do." 3 to 5 rows. Each row a single contrasted operational move. Source citation in caption row underneath the table.

### Three service-change recs section

Render as a numbered ranked list (1, 2, 3). Each rec is a featured card with the subtle blue-tinted shadow. Inside each card:
- Number (large, weight 300, accent purple)
- Change name (heading, 22px weight 300)
- Evidence pill row: small outlined badges showing "Review · TripAdvisor", "Reddit · r/Hawaii", "Comp · [Name]", "Industry · [Trend]"
- Effort meter and Impact meter, side by side, label color, just text ("Effort: Low · Impact: High")
- 30-day next step: short paragraph in body color, prefixed with the label "Ship within 30 days." in label color uppercase letter-spacing 0.16em

### Sources list

A footer-area block listing every URL the AI consulted, grouped by surface. Audience evidence-trail. Section headers (Reviews / Reddit / Blogs / YouTube / Industry / Comps) in uppercase 12px label color. URLs in 13px body color. No ornament.

### Footer

> "Powered by Lights On" · link to https://lightson.co.
> Plus the small "Built with the Hospitality Business Skills teammate · github.com/lightson-digital/hospitality-business-skills" microcopy.

### HTML scaffold

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Experience Pulse · [Business Name]</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500&family=Source+Serif+4:ital,wght@1,400&display=swap" rel="stylesheet">
<style>
  :root {
    --heading: #061b31;
    --label: #273951;
    --body: #64748d;
    --accent: #533afd;
    --border: #e5edf5;
    --bg: #ffffff;
    --shadow-featured: rgba(50,50,93,0.10) 0px 12px 20px 0px;
  }
  * { box-sizing: border-box; }
  body {
    font-family: 'Inter', -apple-system, sans-serif;
    max-width: 1040px; margin: 40px auto; padding: 0 32px;
    color: var(--heading); line-height: 1.55; background: var(--bg);
    font-weight: 300;
    font-size: 16px;
    -webkit-font-smoothing: antialiased;
    font-feature-settings: "ss01";
  }
  .eyebrow {
    font-size: 11px; font-weight: 500; letter-spacing: 0.18em;
    text-transform: uppercase; color: var(--accent); margin-bottom: 10px;
  }
  h1 {
    font-size: 48px; font-weight: 300; letter-spacing: -0.96px;
    margin: 0 0 6px; color: var(--heading); line-height: 1.1;
  }
  .sub { font-size: 18px; font-weight: 300; color: var(--body); margin-bottom: 36px; line-height: 1.5; max-width: 780px; }
  .stamp { font-size: 12px; color: var(--body); margin-bottom: 36px; letter-spacing: 0.04em; }

  /* Section heading style · used at top of each bucket */
  .section-head {
    font-size: 13px; font-weight: 500; letter-spacing: 0.16em;
    text-transform: uppercase; color: var(--label); margin: 56px 0 20px;
  }
  .section-head .ring {
    display: inline-block; width: 6px; height: 6px; border-radius: 50%;
    background: var(--accent); margin-right: 10px; vertical-align: middle;
  }

  /* Bucket 1 · Love (pull-quotes) */
  .love-quote {
    font-family: 'Source Serif 4', Georgia, serif; font-style: italic; font-size: 19px;
    font-weight: 400;
    line-height: 1.55; color: var(--heading); padding: 6px 0 6px 22px;
    border-left: 2px solid var(--accent); margin: 22px 0;
  }
  .love-quote .attribution {
    display: block; font-family: 'Inter', sans-serif; font-style: normal;
    font-size: 12px; color: var(--body); margin-top: 8px; letter-spacing: 0.04em;
  }

  /* Bucket 2 · Hate (frequency rows) */
  .hate-row {
    display: flex; justify-content: space-between; align-items: center;
    padding: 14px 0; border-bottom: 1px solid var(--border);
  }
  .hate-row:last-child { border-bottom: none; }
  .hate-text { font-size: 15px; color: var(--heading); font-weight: 400; line-height: 1.5; flex: 1; }
  .freq-badge {
    font-size: 11px; padding: 3px 8px; border: 1px solid var(--border);
    border-radius: 4px; color: var(--body); white-space: nowrap; margin-left: 16px;
  }

  /* Bucket 3 · Fear (2x2 grid) */
  .fear-grid {
    display: grid; grid-template-columns: 1fr 1fr; gap: 14px; margin: 8px 0;
  }
  .fear-cell {
    border: 1px solid var(--border); border-radius: 6px; padding: 18px;
  }
  .fear-anxiety { font-size: 16px; color: var(--heading); margin-bottom: 12px; line-height: 1.5; font-weight: 400; }
  .fear-status {
    font-size: 11px; letter-spacing: 0.12em; text-transform: uppercase;
    color: var(--label); font-weight: 500;
  }
  .fear-status.not-addressed { color: var(--accent); }

  /* Bucket 4 · Category changing (timeline rows) */
  .trend-row {
    display: grid; grid-template-columns: 2fr 1.2fr 1.5fr; gap: 18px;
    align-items: baseline; padding: 16px 0; border-bottom: 1px solid var(--border);
  }
  .trend-row:last-child { border-bottom: none; }
  .trend-name { font-size: 15px; color: var(--heading); font-weight: 400; line-height: 1.5; }
  .trend-name .caption { display: block; font-size: 14px; color: var(--body); margin-top: 8px; font-weight: 300; line-height: 1.55; }
  .trend-when { font-size: 13px; color: var(--label); }
  .trend-source a { font-size: 12px; color: var(--accent); text-decoration: none; word-break: break-all; }

  /* Bucket 5 · Comp side-by-side */
  .comp-table {
    width: 100%; border: 1px solid var(--border); border-radius: 6px; overflow: hidden;
    border-collapse: separate; border-spacing: 0; margin: 8px 0;
  }
  .comp-table th, .comp-table td {
    padding: 16px 18px; text-align: left; border-bottom: 1px solid var(--border);
    font-size: 15px; vertical-align: top; line-height: 1.55;
  }
  .comp-table th {
    font-size: 11px; font-weight: 500; letter-spacing: 0.16em;
    text-transform: uppercase; color: var(--label); background: #fafbfd;
  }
  .comp-table td.they { color: var(--heading); }
  .comp-table td.you { color: var(--body); }
  .comp-table tr:last-child td { border-bottom: none; }
  .comp-source { font-size: 12px; color: var(--body); margin-top: 8px; }

  /* Three service-change recs */
  .recs { margin-top: 24px; }
  .rec {
    display: grid; grid-template-columns: 56px 1fr; gap: 24px;
    background: var(--bg); border: 1px solid var(--border); border-radius: 8px;
    padding: 28px 32px; margin-bottom: 18px; box-shadow: var(--shadow-featured);
  }
  .rec-num {
    font-size: 44px; font-weight: 300; color: var(--accent);
    letter-spacing: -0.04em; line-height: 1;
  }
  .rec-name {
    font-size: 22px; font-weight: 300; letter-spacing: -0.22px;
    color: var(--heading); margin: 0 0 10px;
  }
  .rec-evidence { display: flex; gap: 8px; flex-wrap: wrap; margin-bottom: 14px; }
  .evidence-pill {
    font-size: 11px; padding: 3px 9px; border: 1px solid var(--border);
    border-radius: 4px; color: var(--body); letter-spacing: 0.02em;
  }
  .rec-meters { font-size: 13px; color: var(--label); margin-bottom: 14px; }
  .rec-meters strong { color: var(--heading); font-weight: 400; }
  .rec-step-label {
    font-size: 11px; letter-spacing: 0.16em; text-transform: uppercase;
    color: var(--label); margin-bottom: 4px;
  }
  .rec-step { font-size: 15px; color: var(--heading); line-height: 1.6; }

  /* Sources */
  .sources { margin-top: 56px; padding-top: 28px; border-top: 1px solid var(--border); }
  .sources-group { margin-bottom: 18px; }
  .sources-group h4 {
    font-size: 11px; font-weight: 500; letter-spacing: 0.16em;
    text-transform: uppercase; color: var(--label); margin: 0 0 8px;
  }
  .sources-group ul { margin: 0; padding: 0; list-style: none; }
  .sources-group li { font-size: 13px; color: var(--body); margin-bottom: 4px; word-break: break-all; }
  .sources-group a { color: var(--accent); text-decoration: none; }

  /* Footer */
  .footer {
    margin-top: 48px; padding-top: 24px; border-top: 1px solid var(--border);
    font-size: 12px; color: var(--body); text-align: center; letter-spacing: 0.04em;
  }
  .footer a { color: var(--accent); text-decoration: none; }

  @media (max-width: 720px) {
    h1 { font-size: 32px; letter-spacing: -0.64px; }
    .fear-grid { grid-template-columns: 1fr; }
    .trend-row { grid-template-columns: 1fr; gap: 6px; }
    .rec { grid-template-columns: 1fr; padding: 22px; }
    .rec-num { font-size: 32px; }
  }
</style>
</head>
<body>
  <div class="eyebrow">EXPERIENCE · QUARTERLY PULSE</div>
  <h1>[Business Name]</h1>
  <div class="sub">What travelers say after the trip, what's shifting in the category, what comps do that you don't.</div>
  <div class="stamp">[First Draft / Refined] · [YYYY-MM-DD] · [N] sources read across [N] surfaces</div>

  <!-- Bucket 1 · Love -->
  <div class="section-head"><span class="ring"></span>Travelers love</div>
  <div class="love-quote">
    "[Verbatim quote]"
    <span class="attribution">[Reviewer name if shown] · [Platform]</span>
  </div>
  <!-- repeat 3 to 5 times -->

  <!-- Bucket 2 · Hate -->
  <div class="section-head"><span class="ring"></span>Travelers hate</div>
  <div class="hate-row">
    <div class="hate-text">[Friction pattern phrased as the operator would hear it]</div>
    <div class="freq-badge">[N mentions across [Platforms]]</div>
  </div>
  <!-- repeat 3 to 6 times -->

  <!-- Bucket 3 · Fear -->
  <div class="section-head"><span class="ring"></span>Travelers fear</div>
  <div class="fear-grid">
    <div class="fear-cell">
      <div class="fear-anxiety">[Anxiety statement in traveler voice]</div>
      <div class="fear-status">Addressed on site</div>
    </div>
    <div class="fear-cell">
      <div class="fear-anxiety">[Anxiety statement]</div>
      <div class="fear-status not-addressed">Not addressed</div>
    </div>
    <!-- 4 cells total -->
  </div>

  <!-- Bucket 4 · Category changing -->
  <div class="section-head"><span class="ring"></span>What's changing in the category</div>
  <div class="trend-row">
    <div class="trend-name">[Trend headline]<span class="caption">[One-line context]</span></div>
    <div class="trend-when">[When it shifted]</div>
    <div class="trend-source"><a href="[URL]">[Domain]</a></div>
  </div>
  <!-- 2 to 4 rows -->

  <!-- Bucket 5 · Comp does, you don't -->
  <div class="section-head"><span class="ring"></span>Comps do, you don't</div>
  <table class="comp-table">
    <thead>
      <tr><th>They do</th><th>You do</th></tr>
    </thead>
    <tbody>
      <tr><td class="they">[Specific operational move from comp]</td><td class="you">[Your current state]</td></tr>
      <!-- 3 to 5 rows -->
    </tbody>
  </table>
  <div class="comp-source">Sources: <a href="[URL]">[Comp 1]</a>, <a href="[URL]">[Comp 2]</a></div>

  <!-- Three service-change recs -->
  <div class="section-head"><span class="ring"></span>Three service changes, ranked</div>
  <div class="recs">
    <div class="rec">
      <div class="rec-num">1</div>
      <div>
        <div class="rec-name">[Change name]</div>
        <div class="rec-evidence">
          <span class="evidence-pill">Review · TripAdvisor</span>
          <span class="evidence-pill">Reddit · r/Hawaii</span>
          <span class="evidence-pill">Comp · [Name]</span>
        </div>
        <div class="rec-meters"><strong>Effort:</strong> Low · <strong>Impact:</strong> High · <strong>Where:</strong> [Pre-arrival / On-tour / Post-experience] · <strong>Category:</strong> [snack / narration / etc.]</div>
        <div class="rec-step-label">Ship within 30 days</div>
        <div class="rec-step">[First concrete operational step]</div>
      </div>
    </div>
    <!-- repeat for 2 and 3 -->
  </div>

  <!-- Sources -->
  <div class="sources">
    <div class="section-head"><span class="ring"></span>Sources</div>
    <div class="sources-group">
      <h4>Reviews</h4>
      <ul><li><a href="[URL]">[URL]</a></li></ul>
    </div>
    <div class="sources-group">
      <h4>Reddit</h4>
      <ul><li><a href="[URL]">[URL]</a></li></ul>
    </div>
    <div class="sources-group">
      <h4>Blogs</h4>
      <ul><li><a href="[URL]">[URL]</a></li></ul>
    </div>
    <div class="sources-group">
      <h4>YouTube</h4>
      <ul><li><a href="[URL]">[URL]</a></li></ul>
    </div>
    <div class="sources-group">
      <h4>Industry context</h4>
      <ul><li><a href="[URL]">[URL]</a></li></ul>
    </div>
    <div class="sources-group">
      <h4>Comps</h4>
      <ul><li><a href="[URL]">[URL]</a></li></ul>
    </div>
  </div>

  <div class="footer">
    Powered by <a href="https://lightson.co">Lights On</a> · Built with the Hospitality Business Skills teammate · github.com/lightson-digital/hospitality-business-skills
  </div>
</body>
</html>
```

---

## Anti-slop guardrails

This artifact will be live-demoed to a room of operators. Hold the line on these:

- **No gradient text.** Headings are flat `#061b31`.
- **No glassmorphism.** No backdrop-filter blur, no translucent panels.
- **No generic 3-card grid where every card looks identical.** The 5 buckets each have a distinct visual shape. That's the point.
- **No "hero metric" chrome.** No big-number kpi block at the top. The headline is the operator's name and the question.
- **No emoji as bullets.** No emoji in body. No emoji in section heads.
- **No pill-shaped tags.** Radii stay 4 to 6px. Corners are conservative. Stripe doesn't use pills, neither do we.
- **No rule-of-three lists where the third item is "and most importantly."** Two items, four items, or state it directly.
- **No em dashes.** Anywhere. Use commas, periods, parentheses, colons.
- **Shadow only on featured cards.** Plain `1px solid #e5edf5` border for everything else. The blue-tinted shadow `rgba(50,50,93,0.10) 0px 12px 20px 0px` is reserved for the 3 rec cards. Don't dilute it by spraying it across the page.

---

## Tone rules

- Active voice. Contractions. Specific. First/second person.
- Hawaiian diacritics correct. ʻokina and kahakō on Hawaiʻi place names, business names, and category words (lūʻau, kamaʻāina, kuleana, mālama).
- Quote travelers verbatim, typos and all. The realness is the point.
- Don't soften negative themes. If 12 reviews mention the parking situation, surface that as a finding.
- If a surface returns nothing, state it. "Reddit signal was thin: 2 mentions across 6 threads in 12 months." Low signal is itself a finding.
- Don't fabricate. If a source isn't accessible, state it. "Apple Maps not crawlable from this run." Move on.
- No banned words. Reference `lights-on-knowledge-management/company/brand-voice.md` for the full list.

## What success looks like

The operator reads the report and immediately knows: the one peak moment to amplify, the one friction to fix in 30 days, and the one competitor move worth copying. They close the laptop and call their ops lead. The Refined markdown sits in their AI project memory so the next time they ask any AI tool about the experience, the AI already knows what travelers said, what's changing in the category, and what got shipped.

Run it again next quarter. The 5 buckets will have shifted. That's the point.

---
name: Findability Check
description: Audit AI-search and Google visibility for a Hawaiʻi tour, attraction, or trip-experience operator. Reads the Business Context, runs 5 traveler-prompt simulations across ChatGPT/Claude/Perplexity/Gemini/Google AI Overviews, checks named-entity surface area in third-party sources, inspects schema.org JSON-LD coverage, and previews the Google snippet. Outputs a paste-ready markdown summary plus a Stripe-grade HTML artifact with 3 ranked fixes (effort × impact).
---

# Findability Check

The Discover-stage teammate. One question: *"Are travelers finding you when they ask an AI?"*

Run after Business Context. If the Business Context document isn't already in this conversation, run that skill first. You need the brand name, category, primary location, signature experiences, comp set, and ideal-guest read before you can simulate the prompts a real traveler would type.

---

## When to use

The user runs a B2C trip-experience business in Hawaiʻi (tour operator, lūʻau, attraction, charter, agritourism, transportation, retreat, restaurant-as-experience). They want to know whether the brand surfaces when travelers search, especially inside ChatGPT, Claude, Perplexity, Gemini, and Google AI Overviews.

If the user hasn't given you a URL, ask once:

> "What's the URL of the operator you want to check?"

If a Business Context document doesn't exist in this thread, say so and run that skill first. This skill assumes you have the brand name, category, location, signature experiences, comp set, and voice already pinned.

---

## Why this is different from a Google SEO audit

Traditional SEO gets a page ranked. AI search gets a brand *cited*. Travelers in 2026 ask a chatbot a full sentence ("best agricultural tour on Oʻahu's North Shore that's not Dole Plantation"), and the answer is a synthesis of third-party sources, not a list of blue links. The operator either gets named or doesn't.

Three things drive whether an LLM names a Hawaiʻi operator:

1. **Citation worthiness of the operator's own site.** Extractable copy, real numbers, schema.org JSON-LD, FAQ blocks that match how travelers actually phrase questions, AI bots allowed in `robots.txt`.
2. **Named-entity surface area in third-party sources travelers' AIs read.** TripAdvisor "Best of" lists, Yelp lists, Hawaiʻi Magazine, Honolulu Magazine, Hawaii.com, GoHawaii, Frommer's, Lonely Planet, "best of" blog posts, Reddit `r/Hawaii` and `r/oahu` threads, YouTube tour vlogs.
3. **Google's traditional surface.** AI Overviews still draw heavily on top-ranking pages. Title tag, meta description, mobile, schema, no `noindex`, sitemap visible, OTAs (Viator, GetYourGuide, TripAdvisor) outranking the operator on branded queries.

A Hawaiʻi-specific wrinkle: travelers' prompts almost always mention an island, a town, or a category they learned from a guidebook ("North Shore," "Lānaʻi snorkel," "Hāna Highway stops," "kid-friendly Big Island"). Diacritics (ʻokina, kahakō) matter for entity matching in some sources and not others. Treat both spellings as the same entity when you check.

---

## How it runs

Five passes, in order. Each one writes into the report.

### Pass 1: Pick the 5 prompts a real traveler would type

Pull from the Business Context. You need the **category**, **primary island and town**, **signature experiences**, **comp set**, and the **ideal guest** read.

Write 5 prompts that map to the four buyer modes:

1. **Category + island + qualifier the ideal guest cares about.** Example: *"Best family-friendly agricultural tour on Oʻahu's North Shore"* (category, island, North Shore, family).
2. **Anti-tourist phrasing.** The guest is rejecting the obvious option. Example: *"North Shore farm experience that's not Dole Plantation"* (names the comp the brand is positioned against).
3. **Job-to-be-done in plain language.** Example: *"Where can I see how Hawaiian fruit is actually grown and eat lunch made from it?"* (no category jargon, just the trip's reason to exist).
4. **Day-plan slot.** Example: *"What to do on the North Shore loop besides the beach"* (the trip-slot competitors fight for, including adjacent comps).
5. **Branded query.** The operator's name only. Example: *"Kahuku Farms"*. This is your control. If a brand isn't cited cleanly here, the AI doesn't know what the business is.

Write the 5 prompts before you run them. Show them to the user. Adjust if a prompt assumes the wrong island or wrong category.

### Pass 2: Run each prompt

For each prompt, do a `web_search` for the prompt text. Read the top organic results, the People Also Ask boxes if visible, the AI Overview if visible, and any review-aggregator pages that show up. Then write what an LLM would synthesize from that pool.

Do not invent a verbatim ChatGPT answer you didn't see. Synthesize from the actual sources. State the synthesis as: *"Based on the public web signal, an AI answering this prompt today would most likely name [X], [Y], [Z], because [reasoning]."* If the operator doesn't appear in the source pool, say so directly.

For each prompt, capture:

- **Status.** ✓ Named directly. ~ Mentioned as part of a category but not first. ✗ Absent.
- **Who got named first.** Two competitors max.
- **One-line synthesis.** What an AI would say about the operator if it named them, in the AI's voice.
- **The signal that drove it.** TripAdvisor list, Honolulu Magazine roundup, the operator's own SEO, a Reddit thread, a guidebook, etc. This tells the operator where the missing presence is.

### Pass 3: Named-entity surface area

The operator's own website is one signal. Third-party citations are stronger. For Hawaiʻi B2C trip operators, check these specifically:

- **TripAdvisor "Top Things to Do in [town/island]"** lists. Is the operator on a list? At what rank?
- **Yelp lists** for the category and area.
- **Honolulu Magazine, Hawaiʻi Magazine, MAUI Now, Big Island Now, Star-Advertiser.** Search the brand name. Note any features.
- **Hawaii.com, GoHawaii.com (HTA), HawaiiMagazine.com, Frommer's, Lonely Planet, Fodor's, Travel + Leisure, Condé Nast Traveler.** These guidebook-tier sources are heavily weighted in LLM training and retrieval.
- **Reddit.** `site:reddit.com [brand]` and `site:reddit.com [category] [island]`. Reddit threads punch above their weight in LLM citations.
- **YouTube.** Tour vlogs, family-trip videos, food-blog reviews. AI Overviews lean on YouTube.
- **Local press / blog posts.** "Best of North Shore," "Things to do on Oʻahu with kids," etc.

Score the surface area in plain language: *"Strong on TripAdvisor + Honolulu Magazine, weak on Reddit + YouTube"* is more useful than a number.

### Pass 4: Schema.org JSON-LD check

LLMs and Google both extract structured data first because it's unambiguous. For a B2C Hawaiʻi trip operator, the schemas that matter:

| Schema | Use it for |
|---|---|
| `LocalBusiness` (or `TouristAttraction`) | Homepage and about page. Name, address, phone, geo, opening hours, price range. |
| `Product` or `Event` | Each tour or experience page. Name, description, price, duration, image. |
| `FAQPage` | A real FAQ page with the 5 questions travelers actually ask (rain policy, mobility, kids' age, food, parking). |
| `Review` / `AggregateRating` | If the site shows real reviews with names and dates. Don't fabricate. |
| `BreadcrumbList` | Multi-page sites with Tours/Café/Shop hierarchy. |
| `Restaurant` | Only if the property has a real café/restaurant component. |

How to check it honestly:

- `web_fetch` strips `<script>` tags. It cannot detect JSON-LD that's injected by a CMS plugin (Yoast, RankMath, AIOSEO, Webflow CMS embeds). Don't report "no schema" based on `web_fetch` output alone.
- Use Google's Rich Results Test (`https://search.google.com/test/rich-results`) when you can. State it as: *"Rich Results Test shows X."*
- If you can only see the raw HTML and find no JSON-LD there, write: *"No JSON-LD visible in static HTML. Plugin-injected schema may exist; recommend running Rich Results Test to confirm."* That's the honest answer.

For the report, list what's present, what's missing, and the one schema that would unlock the most AI answer real estate. For most Hawaiʻi tour operators, that's `FAQPage` with 5 honest questions.

### Pass 5: Google snippet preview + AI bot access

Run `web_search` for the exact business name. Capture:

- Title tag the snippet shows.
- Meta description.
- Whether Google Business Profile (knowledge panel) shows.
- Whether OTAs (Viator, GetYourGuide, TripAdvisor) appear above the operator's own homepage on a branded search. This is a direct revenue leak: a guest typing the brand into Google clicks an OTA result, books with commission, and the operator pays for traffic they already earned.

Also check `robots.txt` for blocks on AI crawlers if you can fetch it: `GPTBot`, `ChatGPT-User`, `PerplexityBot`, `ClaudeBot`, `anthropic-ai`, `Google-Extended`. A blocked crawler means that platform cannot cite the operator. State what's blocked, what's allowed.

---

## Synthesize 3 ranked fixes

Pick the 3 highest-impact, lowest-effort fixes from the five passes. Rank them by impact, not by where they appear in the report.

For each fix, write:

- **What.** The specific change. Concrete enough that a developer or marketing manager could do it tomorrow. Not "improve schema", "Add `FAQPage` JSON-LD to the homepage covering 5 questions: rain/cancellation policy, mobility on the farm, kids' age range, food restrictions, parking."
- **Why.** Which prompt or which third-party gap this unlocks. Tie it to a specific traveler search.
- **Where.** The page or asset. Homepage hero, tour page meta description, Google Business Profile, a guest-post pitch to Hawaii.com, a Reddit comment in `r/Hawaii`.
- **Effort.** Low / Mid / High. Low = under 2 hours by a junior marketer. Mid = 1 day. High = multi-week project.
- **Impact.** Low / Mid / High. Low = nudges one prompt. Mid = unlocks a category prompt. High = changes how AIs describe the brand for the whole trip-slot.

Common fixes that show up for Hawaiʻi B2C trip operators:

- Add `FAQPage` JSON-LD with the 5 anxieties from the Business Context (rain policy, mobility, kids' age, dietary, parking).
- Rewrite the homepage hero to include the category-defining phrase the brand wants to own ("4th-generation working farm and farm-to-table café on Oʻahu's North Shore" beats "Come Find Your Happy Place" for the AI, even if the brand line stays as the second sentence).
- Get listed (or move up) on TripAdvisor's "Top Things to Do in [town]" list.
- Pitch a single guest post or roundup mention to Honolulu Magazine, Hawaii Magazine, or Hawaii.com (one strong third-party citation outranks ten weak ones).
- Claim and complete the Google Business Profile, including the `Tours` or `Attractions` category and recent photos.
- Submit a sitemap that includes per-tour pages, not just the homepage.
- Allow `GPTBot`, `PerplexityBot`, `ClaudeBot`, and `Google-Extended` in `robots.txt` if any are blocked.
- Add `Product` or `Event` schema to each tour page with price, duration, image, and a real description.

---

## Output format

The skill emits **two things** in this order, in the same response:

### 1. Paste-ready markdown summary (chat, before the artifact)

A 10-line block the operator can copy into their AI project memory. Markdown only. No HTML. Headed exactly like this:

```markdown
## Findability Check, [Business Name] (paste into your AI project memory)

- **5-prompt visibility:** [n] named, [n] category-only, [n] absent. Branded query: ✓/~/✗.
- **Top competitor cited where you weren't:** [Comp 1], [Comp 2].
- **Third-party surface area:** strong on [source], weak on [source].
- **Schema status:** [present types]. Missing: [missing types]. Top gap: [one schema].
- **Google snippet:** [title tag truncated to 60 char]. OTAs above your site on branded query: Y/N ([which]).
- **AI bots in robots.txt:** [any blocked, or "all allowed"].
- **Top fix #1 (Low effort, High impact):** [what + where].
- **Top fix #2 ([effort], [impact]):** [what + where].
- **Top fix #3 ([effort], [impact]):** [what + where].
- **Read next:** Reviews, Repeat-Visit, Pre-arrival.
```

Keep it tight. The operator is going to paste this into ChatGPT or Claude as project memory the next time they ask the AI to write copy or a tour-page meta description. The summary is the prompt context for everything downstream.

### 2. HTML artifact

A self-contained HTML file. Inter from Google Fonts. Stripe-derived design system. No external CSS, no external JS, no images. Renders standalone in any browser.

Render the 5 prompts as a stack of cards. Render the 3 fixes as a numbered ranked list with effort/impact pills. Render the Google snippet preview as a faux-Google card. Render the schema check as a 2-column "present / missing" list.

**Provenance badge.** Stamp the artifact with `Powered by Lights On · ran on [YYYY-MM-DD]` immediately after the subtitle/lede, where `[YYYY-MM-DD]` is the actual date the skill is run. Use the `.stamp` class in the template below. The `·` character is U+00B7 middle dot, with single spaces on either side. Never an em dash, never a hyphen.

The skeleton:

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Findability Check · [Business Name]</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600&family=Source+Serif+4:ital,wght@1,400&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --heading: #061b31;
    --label: #273951;
    --body: #273951;
    --accent: #533afd;
    --accent-soft: #f3f1ff;
    --border: #e5edf5;
    --surface: #ffffff;
    --surface-alt: #fafbfd;
    --status-good: #108c3d;
    --status-good-bg: rgba(21,190,83,0.12);
    --status-mid: #9b6829;
    --status-mid-bg: rgba(155,104,41,0.10);
    --status-miss: #b42318;
    --status-miss-bg: rgba(180,35,24,0.08);
    --shadow-feature: rgba(50,50,93,0.10) 0px 12px 20px 0px;
  }
  * { box-sizing: border-box; }
  html, body { margin: 0; padding: 0; }
  body {
    font-family: 'Inter', -apple-system, 'SF Pro Display', sans-serif;
    font-feature-settings: "ss01";
    font-weight: 300;
    font-size: 17px;
    color: var(--body);
    background: var(--surface);
    line-height: 1.55;
    -webkit-font-smoothing: antialiased;
  }
  .wrap { max-width: 1040px; margin: 0 auto; padding: 64px 32px 96px; }
  .stamp {
    display: inline-block;
    font-size: 11px; font-weight: 600;
    letter-spacing: 0.16em;
    text-transform: uppercase;
    color: var(--accent);
    background: rgba(83,58,253,0.08);
    padding: 4px 10px;
    border-radius: 999px;
    margin-bottom: 28px;
  }
  .eyebrow {
    font-size: 12px; font-weight: 600; letter-spacing: 0.18em;
    text-transform: uppercase; color: var(--accent);
    margin: 0 0 8px;
  }
  h1 {
    font-family: 'Inter', sans-serif; font-weight: 300;
    font-size: 44px; line-height: 1.10; letter-spacing: -1.2px;
    color: var(--heading); margin: 0 0 4px;
  }
  .lede { font-size: 20px; font-weight: 300; color: var(--body); margin: 0 0 12px; max-width: 640px; line-height: 1.5; }
  h2 {
    font-family: 'Inter', sans-serif; font-weight: 300;
    font-size: 26px; line-height: 1.12; letter-spacing: -0.26px;
    color: var(--heading); margin: 56px 0 20px;
  }
  .section-meta {
    font-size: 13px; color: var(--body); margin: -14px 0 24px;
  }

  /* Prompt cards */
  .prompts { display: flex; flex-direction: column; gap: 12px; }
  .prompt-card {
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 22px 26px;
    background: var(--surface);
  }
  .prompt-card.featured {
    box-shadow: var(--shadow-feature);
    border-color: var(--border);
  }
  .prompt-header {
    display: flex; align-items: flex-start; gap: 16px; margin-bottom: 12px;
  }
  .prompt-text {
    flex: 1;
    font-family: 'JetBrains Mono', 'SF Mono', monospace;
    font-size: 16px; font-weight: 400; line-height: 1.5;
    color: var(--label);
  }
  .status {
    display: inline-flex; align-items: center; gap: 6px;
    font-size: 11px; font-weight: 400; letter-spacing: 0.04em;
    padding: 4px 10px; border-radius: 4px;
    white-space: nowrap;
  }
  .status.good { background: var(--status-good-bg); color: var(--status-good); }
  .status.mid  { background: var(--status-mid-bg);  color: var(--status-mid); }
  .status.miss { background: var(--status-miss-bg); color: var(--status-miss); }
  .status .glyph { font-family: 'JetBrains Mono', monospace; font-weight: 500; }
  .prompt-synthesis {
    font-size: 16px; line-height: 1.6; color: var(--body); margin: 0;
  }
  .prompt-meta {
    margin-top: 10px; font-size: 13px; color: var(--body); line-height: 1.5;
  }
  .prompt-meta strong { color: var(--label); font-weight: 400; }

  /* Snippet preview */
  .snippet {
    border: 1px solid var(--border); border-radius: 8px;
    padding: 20px 24px; background: var(--surface);
  }
  .snippet .url-line { font-size: 12px; color: #006621; margin: 0 0 4px; }
  .snippet .title { font-size: 18px; color: #1a0dab; font-weight: 400; margin: 0 0 6px; }
  .snippet .desc { font-size: 13px; color: #4d5156; line-height: 1.45; margin: 0; }
  .snippet-aside {
    margin-top: 14px; font-size: 13px; color: var(--body);
  }
  .snippet-aside strong { color: var(--label); font-weight: 400; }

  /* Schema two-column */
  .schema-grid {
    display: grid; grid-template-columns: 1fr 1fr; gap: 0;
    border: 1px solid var(--border); border-radius: 8px; overflow: hidden;
  }
  .schema-col { padding: 22px 26px; }
  .schema-col + .schema-col { border-left: 1px solid var(--border); }
  .schema-col h3 {
    font-size: 15px; font-weight: 400; letter-spacing: 0.06em;
    text-transform: uppercase; color: var(--label); margin: 0 0 14px;
  }
  .schema-list { list-style: none; padding: 0; margin: 0; }
  .schema-list li {
    font-family: 'JetBrains Mono', monospace; font-size: 16px;
    color: var(--label); padding: 8px 0; border-bottom: 1px solid var(--border);
  }
  .schema-list li:last-child { border-bottom: none; }
  .schema-list .miss { color: var(--body); }

  /* Fixes */
  .fixes { display: flex; flex-direction: column; gap: 14px; counter-reset: fix; }
  .fix {
    border: 1px solid var(--border); border-radius: 8px;
    padding: 24px 28px; background: var(--surface);
    display: grid; grid-template-columns: 36px 1fr; gap: 18px;
    align-items: start;
  }
  .fix.featured { box-shadow: var(--shadow-feature); }
  .fix .num {
    font-family: 'Inter', sans-serif; font-weight: 300; font-size: 32px;
    line-height: 1; color: var(--accent); letter-spacing: -0.4px;
  }
  .fix .body h3 {
    font-family: 'Inter', sans-serif; font-weight: 300;
    font-size: 22px; line-height: 1.20; letter-spacing: -0.22px;
    color: var(--heading); margin: 0 0 10px;
  }
  .fix .why {
    font-size: 16px; color: var(--body); margin: 0 0 14px; line-height: 1.6;
  }
  .fix .where {
    font-size: 16px; color: var(--label); margin: 0 0 14px; line-height: 1.5;
  }
  .fix .where strong { font-weight: 400; color: var(--accent); }
  .pill-row { display: flex; gap: 8px; }
  .pill {
    display: inline-flex; align-items: center; gap: 6px;
    font-size: 11px; font-weight: 400; letter-spacing: 0.04em;
    padding: 4px 10px; border-radius: 4px;
    background: var(--surface-alt); color: var(--label);
    border: 1px solid var(--border);
  }
  .pill .key { color: var(--body); }

  /* Tabular */
  .tnum { font-feature-settings: "tnum"; font-variant-numeric: tabular-nums; }

  /* Footer */
  .footer {
    margin-top: 72px; padding-top: 24px;
    border-top: 1px solid var(--border);
    display: flex; justify-content: space-between; align-items: center;
    font-size: 13px; color: #425466;
  }
  .footer a { color: var(--accent); text-decoration: none; }
  .footer a:hover { text-decoration: underline; }
  .wordmark {
    font-family: 'Inter', sans-serif; font-weight: 400;
    letter-spacing: 0.04em; text-transform: uppercase;
    font-size: 11px; color: var(--label);
  }

  @media (max-width: 640px) {
    .wrap { padding: 40px 20px 64px; }
    h1 { font-size: 36px; letter-spacing: -0.6px; }
    .schema-grid { grid-template-columns: 1fr; }
    .schema-col + .schema-col { border-left: none; border-top: 1px solid var(--border); }
    .fix { grid-template-columns: 1fr; }
  }
</style>
</head>
<body>
<div class="wrap">

  <p class="eyebrow">Discover · Findability Check</p>
  <h1>[Business Name]</h1>
  <p class="lede">[Category] on [Island/Region]. Are travelers finding you when they ask an AI?</p>
  <span class="stamp">Powered by Lights On · ran on [YYYY-MM-DD]</span>

  <h2>What travelers asked, what AI answered</h2>
  <p class="section-meta">5 prompts a real traveler would type. Synthesized from public web signal.</p>
  <div class="prompts">

    <div class="prompt-card featured">
      <div class="prompt-header">
        <div class="prompt-text">[Prompt 1 verbatim]</div>
        <span class="status good"><span class="glyph">✓</span> Named</span>
      </div>
      <p class="prompt-synthesis">[One-line synthesis: how an AI would describe the operator if it named them, in the AI's voice.]</p>
      <p class="prompt-meta"><strong>Signal:</strong> [TripAdvisor list / Honolulu Magazine / Reddit / YouTube / own site]</p>
    </div>

    <div class="prompt-card">
      <div class="prompt-header">
        <div class="prompt-text">[Prompt 2 verbatim]</div>
        <span class="status mid"><span class="glyph">~</span> Category only</span>
      </div>
      <p class="prompt-synthesis">[Synthesis. Who got named first: Comp A, Comp B.]</p>
      <p class="prompt-meta"><strong>Signal:</strong> [source]</p>
    </div>

    <!-- prompts 3, 4, 5 same shape -->

  </div>

  <h2>Google snippet, branded query</h2>
  <div class="snippet">
    <p class="url-line">[domain.com]</p>
    <p class="title">[Title tag verbatim, truncated to ~60 chars]</p>
    <p class="desc">[Meta description verbatim, truncated to ~160 chars]</p>
  </div>
  <p class="snippet-aside">
    <strong>OTAs above your site on branded search:</strong> [Y/N. Which: Viator, GetYourGuide, TripAdvisor.]<br>
    <strong>Google Business Profile knowledge panel:</strong> [Y/N. Category accurate? Recent photos?]<br>
    <strong>AI bots in robots.txt:</strong> [all allowed / blocked: GPTBot, ClaudeBot, etc.]
  </p>

  <h2>Schema.org structured data</h2>
  <p class="section-meta">JSON-LD is how LLMs and Google read your site without guessing.</p>
  <div class="schema-grid">
    <div class="schema-col">
      <h3>Present</h3>
      <ul class="schema-list">
        <li>[Schema type, e.g. LocalBusiness]</li>
        <li>[Schema type]</li>
      </ul>
    </div>
    <div class="schema-col">
      <h3>Missing</h3>
      <ul class="schema-list">
        <li class="miss">FAQPage</li>
        <li class="miss">Product (per tour page)</li>
      </ul>
    </div>
  </div>

  <h2>3 fixes, ranked by impact</h2>
  <div class="fixes">

    <div class="fix featured">
      <div class="num tnum">01</div>
      <div class="body">
        <h3>[Specific fix headline, e.g. Add FAQPage JSON-LD covering 5 traveler questions]</h3>
        <p class="why">[Why: which prompt or third-party gap this closes. Tie to a real traveler search.]</p>
        <p class="where"><strong>Where:</strong> [page / asset, e.g. homepage + tour page]</p>
        <div class="pill-row">
          <span class="pill"><span class="key">Effort</span> Low</span>
          <span class="pill"><span class="key">Impact</span> High</span>
        </div>
      </div>
    </div>

    <div class="fix">
      <div class="num tnum">02</div>
      <div class="body">
        <h3>[Fix 2]</h3>
        <p class="why">[Why]</p>
        <p class="where"><strong>Where:</strong> [page / asset]</p>
        <div class="pill-row">
          <span class="pill"><span class="key">Effort</span> Mid</span>
          <span class="pill"><span class="key">Impact</span> High</span>
        </div>
      </div>
    </div>

    <div class="fix">
      <div class="num tnum">03</div>
      <div class="body">
        <h3>[Fix 3]</h3>
        <p class="why">[Why]</p>
        <p class="where"><strong>Where:</strong> [page / asset]</p>
        <div class="pill-row">
          <span class="pill"><span class="key">Effort</span> Low</span>
          <span class="pill"><span class="key">Impact</span> Mid</span>
        </div>
      </div>
    </div>

  </div>

  <div class="footer">
    <span>Hospitality Business Skills · github.com/lightson-digital/hospitality-business-skills</span>
    <a href="https://lightson.co" target="_blank" rel="noopener"><span class="wordmark">Powered by Lights On</span></a>
  </div>

</div>
</body>
</html>
```

---

## Tone rules

- Plain language. The reader is the operator, not a marketer. "Outranked by Viator on your own brand name" is fine. "Suboptimal SERP penetration" is not.
- Active voice. Contractions. Specific.
- If the operator does not appear for any of the 5 prompts, say so directly. That IS the finding. Don't soften it.
- Hawaiian diacritics correct (ʻokina, kahakō): Oʻahu, Lānaʻi, Kīlauea, Mānoa, kamaʻāina, lūʻau. When you check for entity matches in third-party sources, treat diacritic and non-diacritic spellings as the same brand.
- Don't fabricate AI answers you didn't see. Synthesize from the actual public web sources you can read. If a source isn't accessible, state that.

---

## Anti-AI-slop guardrails for the artifact

- No gradient text. No glassmorphism. No 3-card grids where every card looks identical.
- No pill-shaped tags. Effort/impact pills use 4px radius and muted backgrounds, not bright tags.
- No bouncy emoji bullets. Status glyphs are mono `✓` `~` `✗` only.
- Subtle blue-tinted shadow (`rgba(50,50,93,0.10) 0px 12px 20px 0px`) on featured cards only. Everything else is plain border. No heavy elevation.
- Display headings at weight 300, body at weight 300, buttons/labels at weight 400. No 600, no 700.
- Whitespace as luxury: 64px top padding, 56px between sections. Don't fill space.

---

## What success looks like

The operator reads the report and knows three things: which travelers can't find them, which schema and which third-party gap is keeping them out of AI answers, and which 3 fixes to do this week. The paste-ready summary at the top of the chat goes straight into their AI project memory so the next downstream skill (Reviews, Repeat-Visit, Pre-arrival) starts smarter than the last one.

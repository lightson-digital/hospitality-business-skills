---
name: Business Context
description: Foundation skill for B2C hospitality operators (tours, lūʻau, attractions, transportation, lodging). Use when the user wants to teach AI about their hospitality business, sets up a new AI project for their tour, lodging, or restaurant, or says "set up business context," "build my business profile," "who is our ideal guest," "positioning doc," "Claude project for my tour business." Takes a URL, scans the website, produces a markdown file the owner pastes into any AI project. First Draft is what the website shows. Refine is where the owner teaches the AI what the website does not.
---

# Business Context

The Foundation teammate. Run this first. **Every other AI workflow you build is only as smart as this document.**

The website tells the AI roughly half of what it needs to know. The other half lives in the owner's head: who the trip is actually for, what brings people back, what you are deliberately not, the source markets, the FAQ that costs you bookings, the angle a competitor cannot copy. None of that shows up in a homepage scan. The Refine step is how that knowledge gets into the document.

Run it once. Save the markdown. Drop it into any AI project. Future skills (Discoverability, Reviews, Repeat-Visit, Pre-arrival, Experience) all read it.

---

## How the skill runs

Two phases. The user can stop after Phase 1.

1. **First Draft.** You scan the website. You fill in what the public site reveals. You stamp the document `First Draft.`
2. **Refine.** You interview the owner one question at a time. Each question targets a section the website cannot answer. You fold answers back into the document and stamp it `Refined.`

When you deliver the first draft, you tell the user plainly: the website only knows half of this. The Refine step is where you, the owner, teach me the rest. Every other AI workflow that uses this document is only as good as the document is. Worth a few minutes.

---

## When to use

The user gave you a URL, directly or wrapped in a sentence ("run a context on https://example.com"). They run a hospitality business: tour, lūʻau, attraction, transportation, lodging, retreat, charter, restaurant-as-experience.

If no URL, ask once:

> "What's the URL of the business you want me to profile?"

Then proceed.

---

## Phase 1 — First Draft

### 1. Fetch the public surfaces

Read the homepage, then walk these surfaces in order, stopping when the questions below are answered:

- About / Story / Our People page
- Tours / Experiences / Activities / Rooms / Menu (whichever is the product index)
- A single representative product page
- FAQ / Policies page if linked
- Contact page (booking flow + phone signal)

### 2. Walk the sections

For each section, fill what the public site shows. If a section cannot be answered from public data, write `Not visible on site. Refine to fill.` Never fabricate. The whole point of the Refine step is to fill these gaps.

#### Business Overview
- **Business name** as the brand uses it, not the legal entity.
- **One-liner** verbatim from the site if possible, otherwise yours.
- **Category** snorkel tour, lūʻau, helicopter tour, cultural tour, agricultural tour, attraction, transportation, boutique hotel, vacation rental, restaurant-as-experience, retreat, charter.
- **Primary location(s)** specific island and town/region.
- **Operating model** single product vs. portfolio, scheduled vs. private, group size, on-water vs. on-land vs. hybrid, year-round vs. seasonal.
- **Pricing tier** low / mid / high, with a $ range pulled from the site.

#### Signature Experiences
3–5 specific products. Use their actual product names ("Sunset Sail to Lānaʻi" not "evening tour"). One-line description per product. Include duration and starting price if visible.

#### Ideal Guest
The guest profile, in plain language. Couple on honeymoon. Family with kids 6–12. Solo first-time visitor. Returning kamaʻāina. Cruise pax with 4 hours ashore. Wholesale group via JTB. Specific traveler types, party size, occasion. From the Refine step if available, otherwise inferred from imagery + review tone + product positioning.

#### Source Markets
Where bookings actually come from. US mainland west / east, Japan, Korea, Australia/NZ, kamaʻāina, cruise, wholesale. Signals: language toggles, currency display, About-page hints, press logos, OTA presence. From Refine if available.

#### What the Trip is Really For
The job-to-be-done, written as a guest sentence, not a feature list.
> "We came to Hawaiʻi for [reason]. We picked this tour because [emotional / status / sensory promise]."

- **Anxieties travelers carry into the booking:** seasickness, weather, kids, language, mobility, dietary, refund policy.
- **The "miss" if they don't book:** what going home without this experience costs them.

#### Comp Set
- **Direct.** 2–3 same category, same island/region. Names + URLs only. No analysis here.
- **Adjacent.** 1–2 different category, same time-slot in the trip ("they're choosing between us and a sunset sail").

#### Differentiation
The 1–2 things on the homepage that try to do the comp-set work. Imagery, awards, kamaʻāina origin, sustainability, exclusivity, scale, captain/guide credentials.

#### Why Travelers Pick You (the Four Forces)
- **Push** what frustrates them about the alternative ("crowded boats," "rushed tours," "no narration").
- **Pull** what your site promises that the alternative cannot ("captain has been doing this 30 years," "max 12 guests," "private launch").
- **Habit** what keeps them defaulting to OTAs / Viator / TripAdvisor instead of booking direct with you.
- **Anxiety** what makes them hesitate at the booking button (refund policy, weather contingency, safety, kid-friendliness).

#### Voice — How the Brand Sounds
- 5–8 adjectives describing the voice ("warm, family-led, kamaʻāina-centered, light on jargon, photo-forward, gently irreverent").
- Words and phrases the brand uses repeatedly ("ʻohana," "small-group," "kamaʻāina-owned"). 4–6 of them.
- Words and clichés the brand actively avoids.
- One verbatim sentence pulled from the site that captures the voice.

#### What You Are NOT
The cliché framing the operator rejects. "We're not a booze cruise." "We're not the helicopter people." "We're not a luxury property, we're a comfortable one." From Refine if available.

#### Repeat-Visit Angle Already Working
For B2C trip experiences, the four natural repeat angles:
- **Different season** same trip at a different time of year reveals new things.
- **Different product** guest did Tour A; portfolio offers Tour B.
- **Different traveler in the household** anniversary, kids' first time, parents visit.
- **Referral** past guest sends friends/family.

Which one is currently working, if any. From Refine if available.

#### Differentiator (one line)
The one sentence the operator would put on a billboard. Drafted from strongest review themes + signature-experience copy. Locked in Refine.

#### Proof Points
- **Awards / press / "as seen on":** [list, or `none visible`].
- **Testimonial snippets on site:** verbatim, with reviewer name if shown.
- **Operational proof:** years in business, guests served, captain or guide credentials.

#### Goals (operator-side, inferred)
- **Primary CTA** verbatim button copy.
- **CTA placement** above-fold hero / post-product / sticky / etc.
- **Conversion target** direct booking, phone call, contact form, list signup.

#### Booking Flow
- **Booking engine** FareHarbor, Peek, Bōkun, Rezdy, Xola, in-house, phone-only.
- **OTAs visible** Viator, GetYourGuide, TripAdvisor Experiences, Expedia Local Expert, none.
- **Refund / weather / cancellation policy** 1-line summary, where it appears on the site.

### 3. Render the document

Render the document as a single markdown file using the template at the bottom of this skill. The user will copy and paste this into a Claude Project, ChatGPT custom instructions, or any AI workspace. Markdown only. No HTML.

Stamp the doc `First Draft` at the top.

### 4. Hand off and offer Refine

After delivering the markdown, say plainly:

> "That's the First Draft. It only knows what your website knows.
>
> The website does not know who actually books, what brings them back, what you are deliberately not, what your strongest objection is, what your one-line differentiator should be. You know that. Every other AI teammate you run after this one (discoverability, reviews, repeat-visit, follow-up emails, pre-arrival, post-experience) is only as good as this document.
>
> Want to spend ~5 minutes refining it with me? I'll ask you about 9 things, one at a time, and rewrite the document with your answers. Or ship it as-is."

If the user says ship / stop / done / no thanks → end. The First Draft is the canonical document.

If the user says refine / yes / continue → run Phase 2.

---

## Phase 2 — Refine (one question at a time)

Walk the user through these branches in this order. **One question per turn.** Always recommend an answer first, drawn from the First Draft. Never stack questions. After each answer, restate the working answer in plain words so the user can confirm or correct, then move to the next.

If the user can answer a question by pointing you at a public source (e.g. a TripAdvisor page, a recent press article), read that source instead of asking again.

1. **Ideal guest.** Who is this trip actually for? *Recommendation drawn from review tone + product positioning.*
2. **Source markets.** Where do bookings actually come from? *Recommendation from language/currency/About-page hints.*
3. **What you are NOT.** The cliché framing you reject. *Recommendation from About-page tone.*
4. **Top objection that costs you bookings.** The FAQ the website does not yet answer well. *Recommendation from FAQ gap surfaced in Phase 1.*
5. **Strongest of the Four Forces right now.** Push, Pull, Habit, or Anxiety? *Recommendation: the one your homepage seems to be working hardest against.*
6. **Customer language confirm/correct.** Read back the verbatim phrases and brand vocab list. Owner keeps, cuts, adds.
7. **Voice confirm/correct.** Read back the 5–8 adjectives. Owner keeps, cuts, adds.
8. **Repeat-visit angle in play.** Which of the four is currently working, if any? *Recommendation from site signals.*
9. **One-line differentiator.** The one sentence for the billboard. *Recommendation drafted from strongest review themes + signature-experience copy.*

When the user signals stop ("done," "ship it," "good enough"), regenerate the markdown with the new answers folded into the relevant sections. Stamp it `Refined.` Tell the user where to paste it: any AI project, custom GPT instructions, Claude Project knowledge, ChatGPT memory.

---

## Output — markdown template

````markdown
# Business Context — [Business Name]

*Stamp:* **[First Draft / Refined]**
*Last updated:* [YYYY-MM-DD]
*Source:* [URL]

---

## Business Overview

- **Name:** [as the brand uses it]
- **One-liner:** [verbatim from site, or yours]
- **Category:** [snorkel tour / lūʻau / etc.]
- **Location:** [island, town/region]
- **Operating model:** [scheduled / private / portfolio of N / etc.]
- **Group size:** [max pax / typical party]
- **Pricing tier:** [low / mid / high · $X–$Y]
- **Year-round / seasonal:** [year-round / seasonal — Mar–Oct / etc.]

## Signature Experiences

- **[Tour name 1]** — [one-line description] · [duration] · [from $X]
- **[Tour name 2]** — [one-line description] · [duration] · [from $X]
- **[Tour name 3]** — [one-line description] · [duration] · [from $X]

## Ideal Guest

[Specific traveler types, party size, occasion. Plain language, written like the operator would describe their best customer.]

## Source Markets

[Where bookings actually come from. US mainland west/east, Japan, Korea, kamaʻāina, cruise, wholesale via JTB / HTJ.]

## What the Trip is Really For

> "We came to Hawaiʻi for [reason]. We picked this tour because [promise]."

- **Anxieties travelers carry into the booking:** [seasickness / weather / kids / language / mobility / food]
- **The miss if they don't book:** [what going home without this experience costs them]

## Comp Set

**Direct competitors:**
- [Competitor 1] — [url]
- [Competitor 2] — [url]

**Adjacent (different category, same trip-slot):**
- [Alternative 1] — [url]

## Differentiation

[The 1–2 things on the homepage that try to do the comp-set work. Imagery, awards, kamaʻāina origin, sustainability, exclusivity, scale.]

## Why Travelers Pick You (Four Forces)

- **Push:** [what frustrates them about the alternative]
- **Pull:** [what your site promises that the alternative cannot]
- **Habit:** [what keeps them defaulting to OTA / Viator]
- **Anxiety:** [what makes them hesitate at the booking button]

## Voice — How the Brand Sounds

**Adjectives:** [warm], [family-led], [kamaʻāina-centered], [light on jargon], [photo-forward]

**Words the brand uses:**
- "[word/phrase 1]"
- "[word/phrase 2]"
- "[word/phrase 3]"
- "[word/phrase 4]"

**Words/clichés the brand avoids:** [list]

**Sample sentence from the site:**
> "[Verbatim sentence that captures the voice]"

## What You Are NOT

[The cliché framing the operator rejects. "We're not a booze cruise." "We're not the helicopter people."]

## Repeat-Visit Angle Already Working

[Different season / different product / different traveler in the household / referral. Which one is currently working, if any.]

## Differentiator (one line)

> [The one sentence the operator would put on a billboard.]

## Proof Points

- **Awards / press / "as seen on":** [list, or `none visible`]
- **Testimonials on site:**
  > "[verbatim quote]" — [reviewer name if shown]
- **Operational proof:** [years in business / guests served / captain credentials]

## Goals (operator-side)

- **Primary CTA:** [verbatim button copy]
- **CTA placement:** [above-fold hero / post-product / sticky]
- **Conversion target:** [direct booking / phone / contact form / list signup]

## Booking Flow

- **Booking engine:** [FareHarbor / Peek / Bōkun / Rezdy / Xola / in-house / phone-only]
- **OTAs visible:** [Viator / GetYourGuide / TripAdvisor Experiences / none]
- **Refund / weather policy:** [1-line summary, where it appears on site]

---

*Built with the Hospitality Business Skills teammate · github.com/lightson-digital/hospitality-business-skills*
````

---

## Phase 3 — Fact-check pass (mandatory)

Run this AFTER the markdown document is drafted and BEFORE you hand it to the user. This is a quality gate, not a watermark. If a check fails, fix in place silently and re-verify. Do not add a "fact-check passed" note to the visible artifact.

1. **URL liveness.** Pick 2 to 3 cited URLs at random from the Comp Set, Press / "as seen on" row, and Source Markets section. Re-fetch each via web_fetch. If any returns 404, blocked, redirected to a parked domain, or wrong content (a Squarespace placeholder, a "this domain is for sale" page, a different business entirely), drop the citation or replace with one that resolves. Treat root-domain fetches as the primary check; a working homepage beats a broken deep link.

2. **Quote provenance.** For every verbatim sentence pulled into the "Voice, sample sentence" or "Testimonials on site" sections, confirm the exact string appears on the cited page. If you cannot verify the wording within a reasonable sample, mark it `(paraphrased)` rather than verbatim, OR drop the quote entirely. Better to ship four real quotes than five with one fabricated.

3. **Number sanity.** Every count, rating, percentage, dollar figure (group size cap, years in business, guest count, price band, "founded in," "as seen on") must cross-check against the source. Round numbers ending in 0 ("over 10,000 guests served") are a fabrication tell; replace with a qualitative phrase ("thousands of guests served," "decades of operation") if you cannot confirm.

4. **Hawaiian diacritics.** Scan the rendered output for: Hawaiʻi (ʻokina), kamaʻāina (ʻokina + kahakō), Lānaʻi, Hāʻena, Mālama, Lūʻau (the lūʻau form), Kalalau, Oʻahu, Lāhainā, Lēʻahi, Kīlauea, Mānoa. Fix any written without diacritics. Place names in Comp Set URLs may strip them; that is fine in URLs but not in body copy.

5. **Banned-word and em-dash sweep.** Run the LOD brand-voice banned word list (delve, leverage, utilize, holistic, robust, seamless, foster, paradigm, ecosystem unless literal, elevate, empower, unlock, harness, navigate as metaphor, streamline unless specific, realm, moreover, furthermore) and an em-dash sweep over the entire document. Replace em dashes with commas, periods, parentheses, or colons. Fix any banned-word hit by reaching for the operator's actual vocabulary from the Voice section.

6. **No-fabrication rule.** Re-scan every section for claims that were not sourced. If a claim looks specific (a competitor's exact policy, a press headline, a podcast appearance, a specific number), verify it has a source. If not, soften to a qualitative statement or drop. The whole point of `Not visible on site. Refine to fill.` is to honor the rule; do not fill gaps with plausible guesses.

7. **Internal consistency.** The summary at the top must match the body. If the Business Overview says "single-product, scheduled, max 12 pax," the Signature Experiences section must not list 5 products. If the Differentiator says "kamaʻāina-owned 4-generation farm" but the About section says nothing about ownership history, reconcile both before delivery. Cross-check operator names, URLs, pricing tier, and category language across sections.

8. **Comp set sanity (per-skill check).** Verify each direct competitor name resolves to a live URL AND is genuinely a direct competitor (same category, same island/region, same trip-slot). A cliff-jump tour is not a direct competitor to a snorkel charter even if both are on Maui. If the Refine step has not yet happened, flag any comp that looks like a wrong-category lookalike with `(verify with operator)` rather than locking it in.

If all eight checks pass, deliver. If any fail, fix and re-run the relevant check.

---

## Tone rules

- Direct, operator-friendly. No marketing fluff. No corporate filler.
- Hawaiian diacritics correct (ʻokina, kahakō) on business and place names.
- If a section cannot be answered from public data, write `Not visible on site. Refine to fill.` Do not fabricate.
- During Refine, never stack questions. One at a time. Always recommend an answer before asking. Restate working answer in plain words after each turn.

## Gotchas

- If the operator runs Shopify, schema checks via web_fetch will miss inline JSON-LD because Shopify injects it via JavaScript post-load. Do not call schema "absent" from a static fetch alone. Recommend Google's Rich Results Test as the follow-up.
- Squarespace and Webflow operators often have a hidden FAQ accordion that reads correctly to a browser but not to web_fetch. If the FAQ section seems empty, fetch the FAQ URL directly before declaring it missing.
- "Pricing tier" pulled from the homepage is often misleading: many Hawaiʻi tour ops bury the kamaʻāina rate on a Specials or Locals subpage. Always check for a Locals or Kamaʻāina link before locking the tier.
- Press logos and "as seen on" rows are routinely stale (years out of date). Treat them as proof of past credibility, not current. Confirm with the operator during Refine.
- "Comp set" you can guess from the website is rarely the comp set the operator actually feels. The Refine step on competitors matters more than any other; the operator's gut beats the AI's pattern match every time.
- Hawaiian diacritics in business names render inconsistently across review platforms. TripAdvisor often strips them, Google Business Profile keeps them. Treat both spellings as the same entity when you cross-reference.

## What success looks like

The owner pastes the Refined document into their AI project. Every other AI teammate they run after this (discoverability, reviews, repeat-visit, follow-up, pre-arrival, post-experience) reads it and produces sharper output without asking the owner anything they already wrote down here. The owner reads the Refined document and says "yes, that's us, and now my AI tools actually know it."

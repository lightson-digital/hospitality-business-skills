# Hospitality Business Skills

**Open-source AI skills for independent hospitality businesses.** A free, MIT-licensed kit of six AI teammates that turn a website URL into paste-ready strategy artifacts across the full guest journey: discover, book, pre-arrival, experience, and reconnect.

Built and maintained by [Lights On Digital](https://lightson.co), a commercial strategy practice for independent and boutique hospitality operators.

## What this is

Six portable AI skills (one markdown file each) that work inside Claude, ChatGPT, Gemini, or any AI assistant with web access. Each skill reads a public website, runs a structured audit or planning task, and returns a markdown summary plus an HTML artifact you can paste into a project, share with a team, or screenshot for a deck.

The skills follow the **Lights On Guest Journey**, a five-stage operating model for hospitality revenue: Discover, Book, Pre-arrival, Experience, Reconnect. A foundational Business Context skill produces a shared profile that the other five skills reuse.

## Who this is for

- Tour operators (snorkel, lūʻau, helicopter, cultural, agricultural, walking, food)
- Attractions and activity providers (museums, gardens, farms, immersive experiences)
- Transportation and shuttle services
- Independent and boutique hotels, inns, and vacation rentals
- Restaurants positioned as experiences (farm-to-table, omakase, chef's table, supper clubs)
- Destination retailers, wholesalers, and consolidators (JTB, HTJ, DMCs)
- Any independently owned hospitality business that wants AI doing strategy work, not just answering chat questions

If you sell a guest experience, the kit applies. The illustrative examples are Hawaiʻi-based, but the methodology is location-neutral.

## The six skills

Run **Business Context** first. Every other skill reads its output and reuses it.

| # | Stage | Skill | Input | Output |
|---|---|---|---|---|
| 0 | Foundation | [Business Context](./business-context/SKILL.md) | Your URL | Markdown profile: overview, ideal guest, source markets, four forces, voice, comp set, differentiator |
| 1 | Discover | [Findability Check](./findability-check/SKILL.md) | Your URL | AI-search visibility audit: 5 LLM prompt simulations, schema check, 3 ranked fixes |
| 2 | Book | [Booking Edge](./booking-edge/SKILL.md) | Your URL | Triangulation report: review voice, comp parity, 3 evidence-tied conversion fixes |
| 3 | Pre-arrival | [Pre-Arrival Concierge](./pre-arrival-concierge/SKILL.md) | Your URL | 3-touch sequence (T-7, T-1, T+0) with upsell map and anxiety map |
| 4 | Experience | [Experience Pulse](./experience-pulse/SKILL.md) | Your URL | Quarterly sweep across reviews, Reddit, blogs, YouTube, comps, trends, plus 3 service-change recs |
| 5 | Reconnect | [Repeat Hooks](./repeat-hooks/SKILL.md) | Your URL | 4-touch lifecycle drip, 3 reactivation emails, 3 referral mechanics |

## Why a skill, not a prompt

A prompt is a one-time instruction. A skill is a documented standard operating procedure (SOP) that any AI assistant can execute the same way every run. Five reasons operators prefer skills:

1. **Repeatable.** The same input produces the same shape of output, every time.
2. **Portable.** A single markdown file works in Claude, ChatGPT, Gemini, or any LLM with web access.
3. **Auditable.** Anyone on your team can read the skill and see exactly how the AI was instructed.
4. **Ownable.** Whoever owns the skill file owns the workflow. No vendor lock-in.
5. **Composable.** Skills chain together. Outputs from one feed inputs of the next.

## How to run a skill

Pick any AI assistant with web access (Claude, ChatGPT, Gemini, Perplexity all work). Paste a prompt like this:

```
Run the Business Context skill using
https://github.com/lightson-digital/hospitality-business-skills/blob/main/business-context/SKILL.md
on https://example.com
```

Replace the skill name and the URL with your own. The AI reads the methodology, executes the audit, and returns a markdown document plus an HTML artifact.

## How to install a skill permanently

### Claude native Skills (recommended)

The most reliable way. Claude treats the `SKILL.md` as a structured procedure and executes every step, including the quality rules and the "do not fabricate" guards baked into each skill.

1. In Claude (web or desktop), open the **Customize** panel from the sidebar, click **Skills**, then click the **+** button to add a personal skill
2. Upload the skill folder from this repo (each folder contains a `SKILL.md`, for example `findability-check/`)
3. Repeat for each of the six skills you want installed
4. In any new chat, mention the skill by name or paste the run prompt. Claude runs the full procedure end to end

### Claude Project (alternative for context-aware runs)

Use this if you want all six skills tied to one workspace with your business context loaded once.

1. Run the Business Context skill first to generate `business-context-{your-business}.md`
2. Create a Claude Project named "Hospitality Business Skills"
3. Upload `business-context-{your-business}.md` to the project's Knowledge
4. Paste a project-level Custom Instruction that points the project at the context file (a generic version is available in the live demo at https://lightson-digital.github.io/skill-demo/)
5. In a new chat in that project, paste the run prompt for any skill. The skill reads the business context first, then runs

### ChatGPT, Gemini, and other AI assistants (works, with caveats)

These platforms can read the `SKILL.md` and produce reasonable output, but they do not follow the procedure faithfully the way Claude does. Expect skipped steps, shorter output, and occasional fabrication where the skill says not to. Treat the result as a useful first draft, not a finished audit.

1. **ChatGPT.** Create a Custom GPT (or paste the `SKILL.md` into Custom Instructions on a paid account), then start a chat with a URL
2. **Gemini.** Create a Gem, paste the `SKILL.md` into the Gem's instructions, then start a chat with a URL
3. Always verify the output against the rules in the SKILL.md, especially the "do not fabricate" sections

You now own the teammate. No subscription, no platform fee, no vendor lock-in.

## How the kit fits together

```
Business Context (run once)
        |
        v
Findability Check  ->  Booking Edge  ->  Pre-Arrival Concierge  ->  Experience Pulse  ->  Repeat Hooks
   (Discover)          (Book)            (Pre-arrival)              (Experience)         (Reconnect)
```

Each downstream skill ingests the Business Context profile so audits and recommendations stay grounded in your specific guest, voice, and competitive set.

## What you get back

Every skill returns:

- **A markdown summary** sized for pasting into Notion, Slack, a doc, or another AI project
- **An HTML artifact** sized for sharing with a team or screenshotting into a deck or report
- **3 ranked actions** with evidence and a rough effort estimate, so you can ship something the same day

No skill returns a 40-page report no one will read. The output is operator-grade: short, structured, and decision-ready.

## Frequently asked questions

### What is an AI skill?

An AI skill is a portable, single-file SOP (a markdown document) that instructs an AI assistant how to perform a specific task end to end. Skills are different from prompts because they encode a full procedure (inputs, steps, output schema, quality rules), not a single instruction.

### Do I need an API key or a subscription?

No. Every skill in this kit is plain markdown. Free tiers of Claude, ChatGPT, and Gemini can run them. You only need an account on whichever assistant you prefer.

### Can I use these skills for a non-Hawaiʻi business?

Yes. The methodology is location-neutral. The illustrative examples reference Hawaiʻi operators because that is where Lights On Digital works most often, but the prompts, the four-forces analysis, and the guest-journey framework apply to any independent hospitality business worldwide.

### Can I modify the skills?

Yes. The license is MIT. Fork the repo, edit the markdown, rename it, ship it inside your own product. Attribution is appreciated but not required.

### Will skills replace my marketing team or my agency?

No. Skills handle the mechanical strategy work (audits, drafts, sweeps, sequences). Humans still own judgment, brand voice, relationships, and final decisions. Think of skills as a junior analyst who never sleeps, not a senior strategist.

### How often should I run each skill?

- Business Context: once, then refresh every 6 months or after a major positioning change
- Findability Check: quarterly
- Booking Edge: quarterly, or after a website redesign
- Pre-Arrival Concierge: once per offer, then refresh when the offer changes
- Experience Pulse: quarterly
- Repeat Hooks: once per segment, then refresh annually

### What is the "Lights On Guest Journey"?

A five-stage operating model for hospitality revenue: Discover (how guests find you), Book (how they convert), Pre-arrival (how anticipation is built), Experience (how the on-property promise is kept), Reconnect (how repeat and referral are earned). The kit ships one skill per stage, plus a foundational Business Context skill that all five reuse.

## Contributing

Pull requests welcome. If you ship a new skill that fits the guest-journey model, or a translation, or a localization for a non-Hawaiʻi market, open a PR. Keep skills single-file and portable so they remain paste-able into any AI assistant.

## License

MIT. Take it, fork it, rename it, sell it. The kit gets better when more operators use it.

## Made by

[Lights On Digital](https://lightson.co), commercial strategy for independent hospitality. Want help installing or extending these skills for your business? [Book a discovery call](https://calendly.com/d/cyq5-gkw-ntj/discovery-call-w-lights-on).

# index.html content review

A critical pass after the recent overhaul. No structural changes made
during the review; recommendations only.

## 1. Does each section earn its place?

- **Hero** — earns it. Headline, subhead, CTA, animated mockup.
- **Marquee** — purely decorative atmospherics. Doesn't sell, doesn't
  inform. Harmless but not pulling weight. **Consider cutting** if a
  later cleanup pass wants to tighten the page.
- **Free Review** — now a major moment. Earns it.
- **Case Study (01 / Proof)** — earns it. Concrete outcome.
- **Sound familiar? (02)** — earns it; now the only diagnosis section.
  Worth shortening if it ever creeps back to feeling like pain-list-
  for-pain-list's-sake.
- **Services (03)** — necessary. Outcome-focused now.
- **Scope (04)** — reinforces breadth with specific products. There is
  a meaningful overlap with Services, but the two angles (capability
  categories vs concrete product types) currently coexist OK. Could be
  merged into a single section in a future pass if 8 sections starts
  feeling long.
- **Image break "Real software. Real outcomes."** — **lost its
  purpose**. With the Case Study moved up to immediately after Free
  Review, this is now a banner *after* the proof has already been
  delivered, with the line "Here's what that looks like in practice"
  pointing at... nothing in particular. Either delete it or repurpose
  it as a transition into Pricing/FAQ.
- **Process (05)** — earns it.
- **Trust Bar** — earns it. Confidentiality / Fixed Price / You Own
  Everything is exactly the right reassurance pre-pricing.
- **Pricing (06)** — earns it.
- **FAQ (07)** — earns it. Closes objections.
- **Founder note + Contact (08)** — earns it.
- **Footer** — earns it.

## 2. Solution-selling vs pain-listing

Most sections now lead with outcome:

- Hero, Free Review, Case Study, Services, Scope, Trust Bar — all
  outcome-led. Good.
- **Sound familiar?** is by definition pain-listing, and that's fine
  as long as it's the only one. Recommend adding an inline CTA at the
  bottom of the section (or making the closing line clickable) to
  resolve the tension instead of dumping the reader into Services.
- **Process** is descriptive (steps 1-4) rather than selling. It works,
  but step 1 ("Discovery Call") could lead with the outcome ("You walk
  away with a clear path forward, even if it's not us") rather than
  the mechanic.

## 3. Does the site communicate breadth?

Yes. Three reinforcements:

- Marquee scrolls eight category keywords.
- Services lists six service categories.
- Scope lists twelve concrete product types in two columns
  (Internal / Customer-facing).

Anyone reading the site should understand by the Scope section that
this isn't a "spreadsheet replacement" agency — it's a custom-software
shop. Good.

One note: the **hero subhead** currently leads with "replaces manual
processes, connects your systems" which is solid but reads as a
narrow brief. The breadth message lives further down. Consider whether
the hero could carry one more breadth-flavoured beat (e.g. "Internal
tools, customer portals, integrations, automation...") without
bloating.

## 4. Tone consistency

Voice is direct and confident throughout. A few weaker spots:

- **Image break subline** "Here's what that looks like in practice"
  reads as marketing-speak filler now that the case study sits above
  it. **Cut or rewrite.**
- **Pricing section subhead** "Every project is different, so every
  quote is different. These are starting points to give you a
  ballpark. Your actual price depends on what you need built." — three
  sentences saying one thing. **Tighten to one sentence.**
- **Pricing card "best for" labels** ("businesses that want it
  handled end to end" etc.) — lower-case kicker on top of an h3
  reads slightly awkward. Capitalise sentence-style or kill them
  entirely; the price-sub line below carries the same job.
- **Process step 1** body — "Free 30 minutes. No obligation." is on
  brand; the rest of step 1 is functional. Fine.
- **Founder note** — strong and on-brand.
- **Trust Bar sub-labels** all read tight. Good.

## 5. Mobile readability

Spot-checks (no live device testing):

- **Hero dashboard mockup** is dense at small sizes; the spreadsheet
  state in particular has 12 columns x 11 rows of mono text crammed
  into the visible width. Likely unreadable on phones. **Worth
  considering** dropping to a 6-column abbreviated view on
  `max-width: 720px`.
- **Sound familiar?** items stack 1-col with the oversized numerals
  shrinking to ~28px. Should read fine.
- **Scope grid** stacks 2-col -> 1-col cleanly.
- **Services grid** stacks 3 -> 2 -> 1 cleanly.
- **Pricing cards** stack to 1-col cleanly.
- **Pain-list closing line** ("If even one of these sounds familiar,
  you're ready for proper software.") sits centred at top with no CTA
  follow-through on mobile until you scroll further. Could attach a
  small CTA right under the closing line for momentum.

## 6. What's missing?

A small business owner reading the site may notice:

- **No "for who this isn't" section** — currently the site doesn't
  qualify-out. A 3-line block ("We don't take pure design work, we
  don't fit £500 brochure builds, we don't replace your in-house
  team") would save you sales-cycle time and signal seriousness.
- **No social proof beyond the one case study** — even two short pull
  quotes ("They quoted in days, not months." / "We finally have one
  source of truth.") with optional first-name attribution would lift
  the credibility floor across the page.
- **No "what happens after I submit?" line** on the Free Review or
  Contact CTAs. People hesitate to submit a form when they don't know
  what's on the other side. One sentence: "We'll reply within one
  working day with two or three concrete questions and a sense of
  whether this is something we can help with."
- **Discovery Call mechanics** — there's a mention of a discovery
  call but no calendar link or hint at length / format / who's on
  the call (Nathan only? team?). Adding a one-liner clears it up.
- **Working geography / timezone** — site says "UK based" in the
  hero tag, but no explicit "we work UK hours" or "happy to work
  with EU/US clients" beyond the Discovery-Call site-visits line in
  the Founder context (which itself sits late on the page).
- **Project size floor** — implicit in pricing (`from £2,500`) but
  not stated as a qualifier. A line like "Most builds run £3-15k.
  Anything smaller is rarely worth the discovery overhead for either
  side." would help self-select.

## Stylesheet hygiene

Not part of the user-facing review but flagging: after the recent
restructure, the stylesheet still contains dead rules from removed
sections — `.who-grid`, `.who-card`, `.who-icon`, `.signs`,
`.signs-list`, `.sign-icon`, `.interlude*`, `.story-list`,
`.story-step`, `.story-num`, `.story-text`, `.story-close`,
`.story-close-line`. None of these target any element in the current
DOM. They could be removed in a follow-up cleanup commit.

## Recommended next actions (priority order)

1. **Cut or repurpose the image break** ("Real software. Real
   outcomes.") — its narrative role broke when the case study moved
   above it.
2. **Add a "Not for you if..." block** between Pricing and FAQ to
   qualify-out and lift seriousness.
3. **Tighten Pricing subhead** to one sentence.
4. **Add an inline CTA** at the bottom of Sound familiar? so pain
   resolves into action without the reader having to scroll past
   Services first.
5. **Mobile spreadsheet density** — consider a reduced column-count
   variant of the dashboard mockup spreadsheet state under 720px.
6. **One or two pull quotes** somewhere between Case Study and Pricing
   to widen the proof beyond the single logistics example.
7. **Cleanup commit** to remove the dead CSS rules listed above.

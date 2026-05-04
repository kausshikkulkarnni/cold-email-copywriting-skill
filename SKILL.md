---
name: cold-email-copywriting
description: Battle-tested cold email copywriting skill for outreach and follow-ups sent through Smartlead or any email sender. Methodology covers personalization research, persona classification, structure, voice, and a pre-ship checklist. Use when writing any cold email copy. Every output produced by this skill must comply with the hard rules below.
user_invocable: true
version: 1.0.0
last_updated: 2026-05-04
---

# Cold Email Copywriting Skill

A battle-tested methodology for cold email that ships replies, not opens. Built from 122+ real B2B SaaS campaigns. Every output produced under this skill must follow the hard rules below.

This is an open-source release of a working production skill. Customize the sender identity in the next section, then the methodology applies as-is.

---

## Customize This Skill For You (do this once)

Before using this skill, fill in your own sender profile below. Every template, rule, and example in this file references these values. Edit them once and the rest of the skill applies to your outreach.

```
Your name:                 [Your Name]
Your role positioning:     [e.g., go to market engineer / fractional CMO / RevOps consultant]
Your core expertise:       [e.g., HubSpot + Apollo / Clay + n8n / Salesforce + Outreach]
Your engagement model:     [e.g., contract / agency / freelance / full-time]
Your social proof number:  [e.g., 50+ clients / 30+ B2B SaaS teams / 10 years in market]
Your brand name:           [e.g., Acme]
Your website:              [e.g., acme.com]
Your location positioning: [e.g., from India / based in Austin / EU-based, optional]
```

Throughout this skill, references to "the sender" / "the operator" / "you" mean whoever fills in this profile. Examples and templates use the original author's profile (Kaushik Kulkarni, go to market engineer, 122+ clients, brand "Up", India-based) as illustrative reference. Swap these values for yours when generating your own copy.

---

## Learning Capture Protocol

Every conversation about email copy produces learnings. All of them should land in this skill, not in chat.

**Rule:** If you give Claude (or any AI assistant) feedback about how an email should or should not be written, that feedback becomes a rule, sub-rule, or note in this skill within the same turn. Bump the version when you do.

This applies to:
- New rules ("never do X").
- Scope corrections ("this skill should not handle Y").
- Context additions ("my background is Z").
- Template approvals ("this one works, use it as the benchmark").
- Tone preferences.
- Banned words or phrasings.
- Anything else you share in the course of a session.

The skill is the single source of truth for email copy rules. Chat transcripts are evidence, not state.

---

## Meta Rule: Must Not Sound AI-Generated (HIGHEST PRIORITY)

Every other rule in this skill exists in service of this one. Field-tested rule: "the goal is to not make the email sound automatic and ai generated (this is ridiculously important)."

### The rule

If the draft reads like ChatGPT wrote it, ship is blocked. Period. Every other rule - structure, word counts, CTA lock, no-link policy - exists to produce output that feels like a real human typed it in 30 seconds before a meeting. They are in service of THIS.

### AI-generated tells to scrub (checklist)

- ❌ Starting consecutive sentences with "I" or "We"
- ❌ Over-polished grammar where a human would use a contraction
- ❌ Formal transitions ("Moreover,", "Furthermore,", "Additionally,", "In addition,")
- ❌ Three-adjective Oxford-comma stacks ("efficient, scalable, and reliable solutions")
- ❌ Abstract nouns when concrete ones would land ("optimization" instead of "fewer clicks")
- ❌ Superlatives without cause ("amazing", "incredible", "world-class")
- ❌ The "not just X but Y" construction (overused by LLMs)
- ❌ Summary sentences at the end that restate the email
- ❌ "I hope this email finds you well"
- ❌ Consulting-deck vocabulary: "leverage", "synergize", "robust", "seamless", "holistic"
- ❌ Mechanically identical sentence rhythms across a batch

### Self-QA question

Before shipping each email, ask: "Does this sound like you typed it in 30 seconds before jumping on a call?" If the answer is "no" or "it sounds more polished than that", rewrite.

---

## Core Philosophy: Fixed Structure, Variable Personalization

(Rewritten based on field correction. Previous version over-swung toward "fully custom composition". That was wrong.)

This skill uses a FIXED 4-part structure where only ONE line (the personalization) varies per prospect. The rest is scaffolded.

### The Standard Email Structure (MANDATORY for Angles 1, 2, 3, 5)

Every email produced by this skill follows this exact 4-line structure - EXCEPT Angle 4, which uses Template #2's structure (see The 5 Angle Categories section below).

```
Line 1 - Greeting:
  Good {{sl_time_of_day}} {{first_name}},

Line 2 - Personalization (variable slot, bespoke per prospect):
  ONE observation about the prospect or company, drawn from research. Something your service / skillset resonates with. Singular, clean. Do not cram multiple observations.

Line 3 - Bridge + Identity:
  Structured as: "given [the thing you observed], are you looking for a go to market engineer by any chance? I've worked with 122+ [companies/SaaS teams/similar companies]."
  The bridge connects the observation to your offer. The identity line states who he is and the client count.

Line 4 - CTA:
  Would a meeting work this week?
```

### What varies, what doesn't

- **Line 1:** Greeting format is fixed to `Good {{sl_time_of_day}} {{first_name}},`. Minor spintax allowed only if it preserves the exact phrase "good {{sl_time_of_day}}" (e.g., `{Good|Gooood}` is ok). Banned forms in Rule 1 below.
- **Line 2:** Fully variable. This is where research lands. Drawn from LinkedIn posts, website, tech stack, company news, funding, etc. ONE clean observation, not a cram of three.
- **Line 3:** Default form: `Are you looking for a go to market engineer by any chance?` followed by the identity + client count sentence. The optional multi-role slashed spintax (`{go to market engineer/clay expert/n8n expert|clay expert/go to market engineer/n8n expert}`) exists in the proven Template #1 but is OPTIONAL. The default is just "go to market engineer" (field correction v0.14).
- **Line 4:** Locked to the "Would a meeting work this week?" family. Spintax only on punctuation (`?` vs `??`).

### Line 2 Personalization - Angle Examples That Work

These angles are battle-tested as strong personalization sources:

| Angle type | Example for a SaaS prospect |
|---|---|
| Technical founder | "Noticed you're a technical founder running a product-led company." |
| Company-stage headcount | "Recall.ai at 36 heads post-Series B is a classic outbound-priority moment." |
| API-first / infra shape | "Saw Recall.ai is API-first with 1200+ companies on the platform." |
| Recent LinkedIn post reference | "Saw your post about the founding marketer hitting $4M in pipeline in 90 days." |
| Recent funding event | "Saw the Series B in September and the momentum behind it." |

Each angle picks ONE observed fact. DO NOT combine multiple angles into a single Line 2. A draft using "technical founder + API-first + 36 heads + recent post" all in one line is LESS effective than one using just one of them.

### Line 2 - One Sentence, No Forced Commentary (v0.20)

Field-tested correction: "tf u mean by lands with hr and benefits buyers i myself am not able to understand what the hell ur writing".

**The rule:** Line 2 is ONE observation. Do not add a second sentence that "explains the implication" or "commentaries on what that means for outbound". The observation IS the personalization. The ask in Line 3 carries the rest.

**Banned pattern (this is what was field-tested):**

```
Line 2: [observation about company]. [Category] SaaS usually needs outbound that [vague jargon verb] [vague object].
```

**Examples that violate the rule (all rewrites of real shipped drafts):**

| ❌ Banned | Why it fails |
|---|---|
| "...needs outbound that lands with HR and benefits buyers, not clinical leads." | "lands with X buyers" + role exclusion = unclear who/what |
| "...need outbound that doesn't fight across practice owners." | "fight across practice owners" - what does it mean? |
| "...need outbound that doesn't bleed playbooks across audiences." | "bleed playbooks" - vivid but meaningless |
| "...need outbound that flexes per industry." | "flexes per industry" - what is being flexed? |
| "...needs outbound that lands at the enterprise level." | "lands at the enterprise level" - corporate filler |
| "...need outbound that pulls in enterprise budgets." | borderline; only OK if the rest is genuinely concrete |

**Cleaner pattern (use this):**

```
Line 2: [observation about company].

Are you looking for a go to market engineer by any chance? I've helped 122+ teams at this stage.
```

That's it. ONE observation, then the ask. The reader understands what was researched. They don't need our interpretation of what that means for their outbound - that's exactly what the meeting is for.

**Why this matters:**

The forced-commentary sentence is the highest-density AI tell in this skill's output. It follows a fixed grammatical mold ("X usually needs Y that Z"), it uses category-buzzwords, and the verb-object pair is rarely concrete. Every instance reads like ChatGPT writing about a company it doesn't really understand. Cutting it makes the email feel like you actually wrote it.

**When a second sentence IS allowed:**

Only when it adds a CONCRETE fact, not a generalization. Example:

```
Saw your post about closing a 7-figure deal on a Friday night. That kind of velocity usually means there's a real outbound machine behind the scenes.
```

The second sentence here is a CONCRETE inference about what the post implies (existing outbound machine), not vague consulting jargon. This passes.

But if you're tempted to write "[category] X usually needs Y that [verb][object]" - DON'T. Drop the sentence.

---

### Line 2 - Specific Tool Names NOT Allowed (v0.14)

Do NOT name specific tools in Line 2 or elsewhere in the body:
- ❌ "I use Clay for ICP scoring and self-hosted n8n for cadences..."
- ❌ "My stack is Clay + n8n + Smartlead..."
- ❌ "built with Clay enrichment..."

Field-tested rule: "never specifically say self hosted n8n and clay etc. saying go to market engineer should be fine."

The positioning word is "go to market engineer". The stack is implied by the outcomes, not name-dropped.

### The 5 Angle Categories (Locked, v0.16)

Every campaign produces **5 emails, one per angle**. Angles are FIXED columns for A/B testing. Each uses a different personalization source. Field-tested rule: "email angles you should be using: 1) tech stack personalization, 2) linkedin post personalization, 3) company news personalization, 4) case study company personalization, 5) something a little generic that acts as fallback for the above 4."

| Angle | Personalization source | Primary research tool |
|---|---|---|
| 1 - Tech Stack | HTTP + Google DNS (MX, TXT, DMARC, script/link tags) | Free, see Research Tool section |
| 2 - LinkedIn Post | Prospect's recent LinkedIn posts (7 → 14 → 28 day lookback) | RapidAPI LinkedIn endpoint |
| 3 - Company News | Recent press, funding, product launches, hires | a Google SERP provider with boolean queries |
| 4 - Case Study Company | Specific customer + 2 lookalikes | 2-stage Enrichment Pipeline |
| 5 - Generic Fallback | None - works for any prospect in any context | No research required |

### Angle-by-angle guidance

**Angle 1 - Tech Stack:** Reference one legitimately-public tech signal. Acceptable: "running on OpenAI + Anthropic" (if product docs confirm), "API-first with 1200+ customers" (if publicly claimed). Unacceptable: "saw your SPF allows Google" (creepy-DNS).

**Angle 2 - LinkedIn Post:** Reference one recent post. Start with "Saw your post about..." or "Loved your post about...". Keep the reference short and natural. Do NOT quote exact timestamps or engagement counts (per Rule 2d).

**Angle 3 - Company News:** Reference recent company-level news: funding rounds, product launches, executive hires, press coverage. Use your Google SERP provider with boolean queries like: `"{company_name}" news`, `"{company_name}" funding OR raised`, `"{company_name}" launched OR announced`. Surface one news item, round to natural specificity ("the Series B last year", not "the $38M Series B on Sept 4, 2025").

**Angle 4 - Case Study Company (uses Template #2 structure, NOT the standard 4-line):** Powered by the 2-stage Enrichment Pipeline. When drafting an email for a specific prospect, RUN the pipeline end-to-end and fill in the REAL values for `{{Case Study Company Name}}`, `{{Lookalike 1}}`, `{{Lookalike 2}}`. NEVER ship placeholders in a specific-prospect deliverable (see rule below). If the pipeline cannot produce clean output, DO NOT use Angle 4; replace with a second variant of Angle 5.

**Angle 4 structure (template, v0.18 update based on field correction):**

This angle deviates from the standard 4-line structure. It uses Template #2's body (minus the co-founder mention and the forwarded block).

```
Good {{sl_time_of_day}} {{first_name}},

Looking at {{case study company}} using {{our company's product}} in production, I found 2 potential customers whom you could pitch:
1) {{Lookalike 1}}
2) {{Lookalike 2}}

I've compiled a list of prospects like these along with an outbound strategy to book calls with them.

Would a meeting work this week?
```

Notes:
- The "Are you looking for a go to market engineer by any chance?" line is NOT in this angle. The offer is baked into "I've compiled a list...".
- The co-founder mention (`I wanted to forward this note from my co founder`) and the entire forwarded block (Ashley) are REMOVED per field correction: "maybe without the cofounder mention".
- Word limits do NOT apply to Angle 4. Field-tested rule: "its okay if your copy doesn't fall under the word limits".
- For Persona 2 (end-company SaaS) prospects, reword "work for" to something natural like "using in production" to avoid the awkward phrasing AND the CTA-word conflict with "work" in the locked CTA.
- Locked CTA rule still applies: use "Would a meeting work this week?" (the original Template #2 said "Interested in a chat this week?" - we override to the locked family).
- TLD stripping still applies (Krisp, not krisp.ai).
- No-repeat rule still applies.
- Meta "must not sound AI-generated" rule still applies.

The numbered list format (`1) X, 2) Y`) is preserved from Template #2.

### NEVER Ship Placeholders (v0.17)

When the ask is "write emails for [specific prospect]", the skill runs research and delivers fully-resolved emails. Placeholders in the body (like `{{Case Study Company Name}}` or `{{Lookalike 1}}`) are ONLY acceptable when the ask is explicitly "write me a template for Clay" or "build a CSV-driven sequence".

Field-tested rule: "dumbass you have to fill those placeholders with your research i gave those prompts for that not to give me placeholders i could've done that myself."

**The rule:**
- Specific-prospect deliverable → run the pipeline, fill real values.
- Template/CSV deliverable → placeholders are fine.

If unclear which mode the user wants, default to specific-prospect mode and fill values. The user can downgrade to a template later if they want.

**Angle 5 - Generic Fallback:** No prospect-specific data. A soft observation that applies to the whole ICP (e.g., "The outbound layer at a growing SaaS is tough to pull off in-house"). This is the always-works email, the one that runs when Angles 1-4 can't produce clean output. Line 2 may be shorter or softer than usual since there's nothing prospect-specific to reference. Template #1's structure (the proven winner) is the reference for this angle.

### Output contract

When you request emails for a prospect, deliver 5 emails labeled by angle (not A/B/C/D/E). Each email independently follows the standard 4-line structure. Angles are parallel rotations, not a sequence.

---

### Line 3 - Identity Sentence Patterns (v0.14)

The identity sentence in Line 3 states who you are + your social proof number. Approved patterns:

- `I've worked with 122+ SaaS teams...`
- `I've helped 122+ companies...`
- `I've helped 122+ teams at this exact stage.`
- `I've helped 122+ teams with this exact shape.`

Optionally include a company-name tie-in:
- `...and was keen on seeing how I could help {{company_name}}.` (borrowed from Template #1)

Do not elaborate further on stack or methodology. The positioning is "go to market engineer who has worked with 122+ SaaS teams". That is enough.

### Why this structure

It is the proven winner (see Proven Template #1). The structure is the scaffolding that makes the pitch land; the personalization is the hook that gets attention. Breaking the structure breaks the pitch. Skipping the personalization makes it generic. Both must be present.

### When in doubt

Ask: "Does Line 2 feel observed, not inferred?" If the personalization could apply to any company in the industry, it has failed. Rewrite Line 2 until it references something only true about this prospect.

---

## Scope Boundary

This skill writes **email copy only**. It produces the body text, merge fields, spintax, Liquid fallbacks, and the plain-text rendering you paste into your sender (e.g., Smartlead).

**Out of scope (do not touch, do not opine on):**
- Smartlead signature configuration. The `%signature%` placeholder is emitted as-is. How the signature is built, whether it contains links, and which signature variant is attached to which step are the responsibility of whoever sets up the campaign in SL. The skill never modifies, strips, or advises on the signature.
- Smartlead sending schedules, warmup, mailbox assignment, and throttle.
- Domain, DNS, SPF/DKIM/DMARC, inbox warmup.
- Lead list sourcing, Clay workflows, CRM hygiene.
- SL campaign step configuration (step 2, step 3 cadence timing, etc.).

When you ask this skill to write copy, it produces the copy and stops. It does not suggest signature edits, does not wrap the output with SL setup instructions, and does not comment on deliverability setup.

---

## Sender Context (Who You Are)

Every email produced by this skill is sent from your own identity. The copy must align with this positioning. The fields below mirror the values from "Customize This Skill For You" at the top.

**Your sender profile (fill these in):**
- **Role:** [your role positioning, e.g., go to market engineer]
- **Core expertise:** [the 1-2 tools or domains you go deep on]
- **Engagement model:** [contract / agency / freelance / full-time]
- **Track record:** [your social proof number, e.g., 50+ clients]
- **Brand name:** [your brand]
- **Website:** [your website]
- **Location positioning (optional):** [e.g., from India, from Austin, EU-based]

**Positioning phrase used in emails (example pattern):** "contract-based [primary role] / [skill 1] expert / [skill 2] expert [from location]". The proven template rotates which of the roles appears first (see Proven Template below) as a reorder trick while keeping all visible.

**Never mis-describe yourself as:**
- A category you don't actually belong to (e.g., calling yourself an agency when you're solo).
- A role you're not (a freelance marketer when you're specifically a GTM engineer, etc.).
- A model you don't operate under (full-time when you're contract only).
- A geography that isn't yours (US-based when you're India-based, etc.).

These mis-descriptions destroy positioning credibility. Pick the truth and stick to it.

**Original author's profile (used in examples and templates throughout this skill):**
- Role: go to market engineer
- Core expertise: Clay.com and n8n.io (self-hosted)
- Engagement model: contract-based, serves globally from India
- Track record: 122+ clients
- Brand: Up
- Website: up.one

When generating your own emails, swap these example values for yours.

---

## Campaign Goal

The single goal of every email this skill produces is: **book a meeting.**

- Not: drive to a landing page.
- Not: get a reply for the sake of a reply.
- Not: build brand awareness.
- Not: nurture passively.

Every CTA must be a direct meeting ask. The email is successful only if the recipient either books a meeting or replies agreeing to one. Clicks, opens, and vague replies do not count as success.

---

## Target Research & Persona Classification (Pre-Draft Step)

Before drafting any email for an input company or contact, this skill performs a short research pass and classifies the prospect into one of two ICP personas. This classification informs angle and emphasis, but does NOT dictate a rigid template choice (see "Methodology is dynamic, not persona-locked" below).

### Persona 1: Agency Clients

These are companies that serve OTHER companies. Often the work is on their end-clients' GTM/RevOps/sales-ops/cold-email infrastructure, or works on the agency's own outbound engine. Work type is typically GTM ops, RevOps, sales ops, Clay workflows, n8n pipelines, outbound infra.

**How to recognize:** Their website positions them as serving clients, not selling a product to end users. Typical signals:
- "We help [X] companies do [Y]."
- Case studies of client wins.
- Services pages listing engagement types.
- Team of consultants or operators, not product engineers.
- Sub-categories: GTM agencies, cold email agencies, RevOps agencies, lead-gen agencies, fractional-CMO shops.

**What they usually buy:**
- Contract GTM engineer to execute for their clients (white-label or co-branded).
- Clay or n8n specialist to build systems they don't have in-house.
- Outbound strategist to fix their own pipeline.

### Persona 2: End-Company Clients

These are companies that sell a product or service directly to end users or businesses. They want you to work on THEIR own outbound, pipeline, RevOps, or enrichment. They are not intermediating.

**How to recognize:** Their website sells a product or a direct service. Typical signals:
- Pricing page.
- Product screenshots, docs, integrations.
- SaaS, platform, marketplace, or direct-service business model.
- Team of product/engineering/sales people, not consultants.

**What they usually buy:**
- Contract GTM engineer to build their own outbound pipeline.
- Clay + n8n expert to run their enrichment and automation.
- Fractional GTM ops help.

### Your Client Roster (Research Reference Only - NEVER Expose in Email Copy)

Maintain a private list of your past or current clients here, organized by persona. **These names must NEVER appear in any email this skill writes.** They are internal research material only. Do not reference, name-drop, hint at, or imply them in any prospect-facing output.

```
**Persona 1 (Agency) clients:**
- [your agency client 1]
- [your agency client 2]
- ...

**Persona 2 (End-Company) clients:**
- [your end-company client 1]
- [your end-company client 2]
- ...
```

Use these as pattern anchors when researching a new prospect to classify. If the prospect looks structurally similar to one of your existing clients, it probably falls into that persona.

If you don't have a client roster yet, skip this section. Persona classification still works on the prospect's website signals alone.

### Methodology is dynamic, not persona-locked

This skill does NOT maintain a "Persona 1 template" and a "Persona 2 template" as hard paths. The persona classification informs:
- Which pain points to surface.
- Which positioning phrases land best (serving-their-clients vs. serving-them-directly).
- Which proven template structure is likely to perform (Template #1 or #2, or a new variant).

Within those considerations, this skill stays flexible and picks whatever combination is most likely to book a meeting. Two emails to the same persona can look completely different and both be correct, as long as they comply with Rules 1, 2, 3 and the scope/identity boundaries.

### Research step (what to do before drafting)

For each new prospect company:
1. Visit the domain. Read the homepage and the services/product page.
2. Decide Persona 1 or Persona 2 based on the signals above.
3. Note 1 or 2 specific details that will make the email feel researched (a client they serve, a product line they sell, a recent post, a role the prospect holds).
4. Only after step 3, draft the email.

Never draft the email before steps 1-3 are done. Generic emails lose this game.

### Research Tool: Web Fetch (live website text)

For steps 1-3 above, this skill needs to pull actual text from prospect websites. Live text beats guessing or relying on cached / summarized knowledge.

**Default (zero-config):** Use whatever web-fetch capability your AI assistant ships with. Claude Code's built-in `WebFetch` tool works for most sites. For plain HTTP-fetchable pages, `curl -sL -A "Mozilla/5.0"` is fine.

**When the default isn't enough:** If a prospect site is behind Cloudflare, requires JavaScript rendering, or aggressively blocks bots, the default fetch returns empty or a challenge page. In that case, fall back to a Bring-Your-Own-Key paid scraping provider that handles proxies and JS rendering.

**Bring-Your-Own-Key paid scraping providers (any one of these works):**

| Provider | Notes |
|---|---|
| scrape.do | `https://api.scrape.do/?token=YOUR_KEY&url=ENCODED_URL&render=true&output=markdown` returns clean markdown. Add `super=true` for premium proxy if blocked. |
| ScrapingBee | `https://app.scrapingbee.com/api/v1/?api_key=YOUR_KEY&url=ENCODED_URL&render_js=true` |
| FireCrawl | `https://api.firecrawl.dev/v0/scrape` with `Authorization: Bearer YOUR_KEY` |
| ZenRows | `https://api.zenrows.com/v1/?apikey=YOUR_KEY&url=ENCODED_URL&js_render=true` |
| Bright Data Web Unlocker | Premium tier, handles the toughest anti-bot |

Set your provider's key in the environment (e.g., `SCRAPE_PROVIDER_KEY`) and reference it from your wrapper. NEVER hardcode the key in this skill file.

**What to fetch per prospect (typical research pass):**

1. Homepage (`https://domain.com/`) - positioning, hero message, persona signals.
2. Services or Products page - what they sell, to whom.
3. Case Studies / Clients / Work page - feeds Stage 1 of the enrichment pipeline.
4. About page (optional) - founder/team context for angle choice.

Fetch only what's needed to inform the email. Do not crawl an entire sitemap. Each page costs time and (for paid providers) credits.

**Concurrency:** When batch-fetching multiple prospects, throttle to 5 parallel requests. Most paid scraping providers rate-limit per second, and respectful concurrency keeps things smooth.

**Failure modes to handle:**
- Empty response body: retry with JS rendering enabled (`render=true` or equivalent on your provider).
- 403 or Cloudflare challenge: retry with premium-proxy mode if your provider has one.
- Site requires login: skip, rely on public pages only.
- Timeout: retry once with a longer timeout (60-90 seconds) before giving up.

**When NOT to fetch:**
- When the user has already provided enriched data (e.g., Clay output, pre-scraped text). Do not re-fetch redundantly.
- When the input has a CSV with 500 prospects and you'd burn the budget fetching all of them. This is for one-at-a-time or small-batch deep research, not mass enrichment. Use a dedicated enrichment platform for volume.
- When the prospect's persona is obvious from the domain alone (rare, but happens with well-known brands).

### Research Tool: Web Search / SERP (find URLs via Google)

Complements web fetch. Use when you need to FIND URLs, news, or content via Google search, not fetch a URL you already have.

**Default (zero-config):** Use whatever web-search capability your AI assistant ships with. Claude Code's built-in `WebSearch` tool works for most queries.

**Bring-Your-Own-Key paid SERP providers (for higher volume, more reliable parsing):**

| Provider | Notes |
|---|---|
| SerpAPI | `https://serpapi.com/search?api_key=YOUR_KEY&q=QUERY&google_domain=google.com` |
| Serper.dev | `https://google.serper.dev/search` with header `X-API-KEY: YOUR_KEY` |
| ScraperAPI SERP | `https://api.scraperapi.com/structured/google/search?api_key=YOUR_KEY&query=QUERY` |
| Bright Data SERP | Premium tier for highest-volume SERP |

Set your provider's key in the environment (e.g., `SERP_PROVIDER_KEY`). Never hardcode in this skill file.

**When to use web fetch vs web search:**
- **Web fetch** = pull content from a URL you already have.
- **Web search** = use Google to discover URLs, news, profiles, or case-study pages first. Then optionally feed those URLs back into web fetch for full content.

**High-leverage Google queries for this workflow:**

| Goal | Query pattern |
|---|---|
| Find prospect's LinkedIn profile | `"{first_name} {last_name}" {company_name} site:linkedin.com/in/` |
| Find recent news about the company | `"{company_name}" news` or `"{company_name}" funding OR raised OR announced` |
| Find their case studies directly | `site:{domain} "case study" OR "our work" OR "clients"` |
| Find posts/content by the prospect | `"{first_name} {last_name}" {company_name} blog OR post OR article` |
| Find third-party mentions | `"{company_name}" review OR testimonial -site:{domain}` |
| Find their tech stack / tools | `"{company_name}" uses OR stack OR built-with` |
| Find the founder/decision-maker's name | `site:{domain} founder OR ceo OR about` |

**Boolean search strategy pattern (proven):**
1. Run the most specific query first (full name + company).
2. If no results, widen by dropping one token.
3. Stop as soon as you get a high-confidence match. Don't run all queries if #1 already nailed it.

**Anti-hallucination rules for SERP research:**
- Only use facts from the `title` or `snippet` / `description` fields of actual results.
- If the search returns no results, say so and fall back to a generic angle. Never make up a fact to fill the gap.
- If a result's title or description contradicts what you'd expect, trust the SERP, not your prior.

**When NOT to use SERP:**
- When you already have the URL. Use web fetch directly.
- When the question is definitional or general. Your own knowledge is fine.
- When speed matters more than freshness. SERP adds a round-trip; skip it if unnecessary.

### Research Tool: LinkedIn (deliberately excluded)

This skill HARD BANS LinkedIn-derived observations in email copy (see Rule 2o below). LinkedIn-scraped facts (recent posts, profile bio, role descriptions) make outbound feel invasive and tank reply rates. The methodology relies on:
- Company website
- Public press / news (TechCrunch, WSJ, trade press)
- Funding databases (Crunchbase / public filings)
- Public conference and podcast appearances (only if hosted off-LinkedIn)
- Public tech-stack signals (HTTP fetch + Google DNS, see next section)

If you're tempted to use a LinkedIn scraper, re-read Rule 2o. Better personalization comes from company-level signal, not prospect-level career trivia.

### Research Tool: Tech Stack Detection via HTTP + Google DNS (FREE)

This is the most under-priced research technique in the whole skill. It requires zero paid APIs. It uses a simple HTTP GET on the prospect's homepage plus free Google DNS-over-HTTPS lookups. The output tells you what tools, platforms, and SaaS integrations the prospect's company actually uses.

**Why this technique:** Field-tested as more reliable and current than BuiltWith, Wappalyzer, or other tech-stack databases. BuiltWith uses captcha and the databases are often stale. Direct DNS + HTTP gives you the live, current picture of what tools the company has set up, with no rate limits and no API key.

**Why it matters for email copy:**
- Knowing the prospect's tech stack surfaces concrete personalization angles ("Saw you're on HubSpot + Outreach, so I'd bet your routing latency between them is 10+ min").
- Tech stack signals persona depth (a company with Salesforce + Outreach + Gong + Clari is a different buyer than one on HubSpot + Google Sheets).
- SPF/DMARC records reveal deliverability maturity, a direct wedge for your positioning.
- Funding-stage signals from Crunchbase via the LinkedIn API become MORE useful when paired with tech-stack signals ("Series B + no outbound tools yet" = high-intent prospect for a GTM engineer).

---

### Method 1: HTTP fetch the homepage, parse signals

Fetch the domain's homepage HTML and grep for:
- **`<script src="...">` URLs** (analytics, CRM, tracking, chat widgets)
- **`<link href="...">` URLs** (CDNs, style providers)
- **`<meta>` tags** (generators like Webflow, Shopify, WordPress)
- **Inline text mentions** of tool names (HubSpot, Salesforce, Intercom, etc.)

**Minimal working commands:**
```bash
# Fetch the homepage
curl -s -L "https://recall.ai" -H "User-Agent: Mozilla/5.0" -m 15 -o /tmp/home.html

# Extract script sources
grep -oE '<script[^>]*src="[^"]*"' /tmp/home.html | grep -oE 'src="[^"]*"' | sort -u

# Extract link hrefs
grep -oE '<link[^>]*href="[^"]*"' /tmp/home.html | grep -oE 'href="[^"]*"' | sort -u

# Extract meta generator tag (reveals CMS platform)
grep -iE 'meta[^>]*generator' /tmp/home.html

# Keyword sweep for common tools
grep -oiE "hubspot|salesforce|pardot|marketo|mailchimp|intercom|drift|zendesk|segment|amplitude|mixpanel|stripe|cloudflare|onetrust|googletagmanager|hotjar|clearbit|vercel|webflow|shopify|wordpress" /tmp/home.html | sort | uniq -c | sort -rn
```

### Method 2: Google DNS for MX / TXT / DMARC (free, no key, no rate limit for small volume)

Google DNS-over-HTTPS endpoint: `https://dns.google/resolve?name={domain}&type={record_type}`

```bash
# MX records - reveals email provider
curl -s "https://dns.google/resolve?name=recall.ai&type=MX" | python3 -m json.tool

# TXT records - reveals SPF + SaaS verification tokens (gold mine)
curl -s "https://dns.google/resolve?name=recall.ai&type=TXT" | python3 -m json.tool

# DMARC record - reveals email security maturity
curl -s "https://dns.google/resolve?name=_dmarc.recall.ai&type=TXT" | python3 -m json.tool
```

All three return JSON with an `Answer[]` array. Each answer has a `data` field containing the record value.

### Fingerprint library (what each signal means)

**From script/link URLs on homepage:**

| URL pattern | Technology |
|---|---|
| `cdn.prod.website-files.com` or `assets.website-files.com` | Webflow |
| `cdn.shopify.com` or `.myshopify.com` | Shopify |
| `wp-content` or `wp-includes` | WordPress |
| `js.hs-scripts.com` or `js.hs-analytics.net` or `js.hsforms.net` | HubSpot |
| `js.hscollectedforms.net` | HubSpot Forms |
| `gtag/js` or `googletagmanager.com/gtm.js` | Google Tag Manager |
| `google-analytics.com/analytics.js` or `gtag/js?id=G-` | Google Analytics |
| `widget.intercom.io` or `js.intercomcdn.com` | Intercom |
| `js.driftt.com` or `driftcdn.com` | Drift |
| `static.zdassets.com` | Zendesk |
| `cdn.segment.com` or `cdn.segment.io` | Segment |
| `cdn.amplitude.com` | Amplitude |
| `api.mixpanel.com` or `cdn.mxpnl.com` | Mixpanel |
| `static.hotjar.com` | Hotjar |
| `js.stripe.com` | Stripe |
| `cdnjs.cloudflare.com` | Cloudflare (as CDN, not necessarily their hosting) |
| `cdn.cookielaw.org` | OneTrust (cookie consent) |
| `munchkin.marketo.net` | Marketo |
| `pi.pardot.com` | Pardot |
| `cdn.launchdarkly.com` | LaunchDarkly |
| `cdn.clearbit.com` | Clearbit |

**From meta generator tag:**

| Content | Technology |
|---|---|
| `Webflow` | Webflow |
| `WordPress X.Y` | WordPress |
| `Shopify` | Shopify |
| `Next.js` | Next.js |
| `Gatsby` | Gatsby |

**From MX records (the first-ranked MX tells you the email host):**

| MX host fragment | Email provider |
|---|---|
| `aspmx.l.google.com`, `googlemail.com` | Google Workspace |
| `outlook.com`, `mail.protection.outlook.com` | Microsoft 365 |
| `zoho.com` | Zoho Mail |
| `protonmail.ch` | Proton |
| `mxa.mailgun.org`, `mxb.mailgun.org` | Mailgun (transactional, not primary inbox) |
| `amazonses.com` | Amazon SES |
| Custom (company domain) | Self-hosted or small provider |

**From TXT records (the most underrated signal):**

SPF records (start with `v=spf1`) list every service authorized to send email on behalf of the domain. Common includes:

| SPF include | What it reveals |
|---|---|
| `_spf.google.com` | Google Workspace |
| `spf.protection.outlook.com` | Microsoft 365 |
| `_spf.salesforce.com` | Salesforce Marketing Cloud / Pardot |
| `sendgrid.net` | SendGrid |
| `_spf.mailgun.org` | Mailgun |
| `servers.mcsv.net` | Mailchimp |
| `_spf.intuit.com` | Intuit/QuickBooks |
| `_spf.createsend.com` | Campaign Monitor |
| `spf.mktomail.com` | Marketo |
| `stspg-customer.com` | Statuspage.io |
| `amazonses.com` | Amazon SES |
| `_spf.hubspot.com` | HubSpot Marketing |

**Verification tokens (non-SPF TXT records) are a GOLD MINE - they reveal every SaaS product the domain has set up integration with:**

| Token prefix | SaaS |
|---|---|
| `notion-domain-verification=` | Notion |
| `google-site-verification=` | Google (Search Console, Analytics) |
| `MS=` | Microsoft 365 |
| `zoom-domain-verification=` | Zoom |
| `zapier-domain-verification-challenge=` | Zapier |
| `docusign=` | DocuSign |
| `detectify-verification=` | Detectify (security) |
| `ahrefs-site-verification_` | Ahrefs (SEO) |
| `openai-domain-verification=` | OpenAI |
| `anthropic-domain-verification` | Anthropic |
| `stripe-verification=` | Stripe |
| `facebook-domain-verification=` | Meta Ads |
| `apple-domain-verification=` | Apple (Push / Maps / etc.) |
| `atlassian-domain-verification=` | Atlassian (Jira/Confluence) |
| `slack-domain-verification=` | Slack |
| `segment-site-verification=` | Segment |
| `linkedin-domain-verification=` | LinkedIn (Conversions API / Ads) |

**From DMARC record (`_dmarc.domain` TXT):**

| `p=` policy | Meaning |
|---|---|
| `p=none` | DMARC set to monitor only. Low email-security maturity. |
| `p=quarantine` | Failing mail goes to spam. Medium maturity. |
| `p=reject` | Failing mail is rejected outright. High maturity, serious about email. |
| No DMARC record | Very low email-security maturity. Flag as a wedge angle. |

### Key insights (from field testing)

- **SPF records reveal MARKETING email tools (Marketo, SendGrid, Mailgun) but NOT SALES engagement tools (Outreach, Salesloft).** Those use the company's own SMTP, so they don't show up in SPF. If you need to detect Outreach/Salesloft, you need SERP queries or direct scraping of job postings.
- **TXT verification tokens are the richest single signal.** They accumulate over time as the company adopts new SaaS products and rarely get cleaned up. A company with 15 verification tokens has a more mature stack than one with 3.
- **DMARC `p=reject` + clean SPF** = they take email deliverability seriously. A good starting point for your positioning.
- **Missing DMARC or `p=none`** = wedge opportunity. This is a real, visible gap you can reference in outbound.

---

### Worked Example: recall.ai (live-tested 2026-04-19)

Ran all three methods live. Here's what the technique surfaced:

**HTTP homepage (Webflow-hosted, last published 2026-04-17):**
- Platform: **Webflow** (cdn.prod.website-files.com, meta generator)
- CDN/infra: Cloudflare, GSAP animations, Rive interactive graphics, jQuery 3.5.1
- Text keywords: HubSpot mentioned 3x, Webflow 4x, cloudflare 2x

**MX records:** Google Workspace (5 MX records, all `aspmx.l.google.com` / `googlemail.com`).

**TXT verification tokens:** Notion, DocuSign, Detectify, Ahrefs, Zoom (2 tokens), OpenAI, Stripe, Microsoft (MS=), Zapier, Anthropic, Google Site Verification (2).

**SPF:** `v=spf1 include:_spf.google.com ~all` - CLEAN. Only Google Workspace authorized. No marketing automation sending email on their behalf.

**DMARC:** `v=DMARC1; p=reject; sp=reject; rua=mailto:dmarc-reports@recall.ai` - **aggressive, enforcement policy.** Serious about email security.

**What this tells the copywriter about recall.ai:**
- API-first AI infra company using BOTH OpenAI AND Anthropic (LLM waterfall pattern).
- Stack: Webflow website, Google Workspace, Stripe billing, Notion internal, DocuSign contracts, Zoom integration (makes sense, they're a meeting API), Zapier automations.
- Security-conscious: Detectify scans, p=reject DMARC, ahrefs for SEO monitoring.
- **No marketing automation on SPF.** They are not running marketing email campaigns through a traditional MA platform. Their outbound (if any) goes through Google Workspace SMTP directly, likely via a sales engagement tool that doesn't appear in DNS.
- Combined with the 14,927 LinkedIn follower count + recent Series B ($38M from Bessemer, Sep 2025) + staff count 36: classic post-Series-B AI infra company that is about to or just started building their revenue engine.

**Direct personalization angles this unlocks for email copy:**
- Reference the dual-LLM stack (OpenAI + Anthropic) as a signal of serious AI infra maturity.
- Reference the absence of marketing automation in SPF as a wedge for the sender's positioning.
- Reference the size-scale mismatch: 36 employees + $38M Series B + no MA stack = they are about to build outbound and probably don't have it figured out yet.

None of this is guessed. All of it is verifiable in 3 public DNS lookups and one HTTP fetch.

---

### Research Tool Selection Summary (updated)

| Need | Tool |
|---|---|
| Pull text from a specific URL you already have | Web fetch (built-in or BYO) |
| Find a URL via Google search | Web search / SERP (built-in or BYO) |
| Enrich prospect's LinkedIn profile | LinkedIn Endpoint 1 |
| Find prospect's recent LinkedIn posts | LinkedIn Endpoint 2 |
| Enrich prospect's company via their domain | LinkedIn Endpoint 3 |
| **Detect prospect's tech stack (free)** | **HTTP + Google DNS (this section)** |
| Mass enrichment over a big list | Clay (not these APIs) |

### When to run tech-stack detection

Run it on EVERY prospect in persona 2 (End-Company) research. For persona 1 (Agency), it's less critical (agencies' own stacks matter less than what their clients use), but still valuable.

Target detection goal per prospect: 1 HTTP fetch + 3 DNS queries = 4 network calls total. Takes under 5 seconds. Adds enormous depth to persona classification.

---

## Input Normalization (MANDATORY Pre-Copy Step)

Before any merge-field value is used in email copy, it must be normalized. A dirty `{{first_name}}` or `{{company_name}}` will render garbage at send time. This step applies whether the input is a single prospect or a CSV.

### First name normalization

| Input | Output |
|---|---|
| `john` | `John` |
| `JOHN` | `John` |
| `John` | `John` (unchanged) |
| `John Smith` | `John` (take first token only) |
| `Dr. John` | `John` (strip titles: Dr., Mr., Mrs., Ms., Prof., etc.) |
| `Mary-Jane` | `Mary-Jane` (preserve legitimate hyphens) |
| `O'Brien` | `O'Brien` (preserve apostrophes in names) |
| `john.smith@acme.com` | DO NOT normalize. This is an email, not a name. Skip or mark unknown. |
| empty / null | Use Liquid fallback per Rule 1 |

Rule: Title-case the first letter, lowercase the rest, strip titles, take only the first whitespace-separated token, preserve apostrophes and hyphens.

### Company name normalization

The goal is to produce the name a human would actually say out loud when referring to the company.

**Strip these suffixes (case-insensitive):**
- Inc, Inc., Incorporated
- LLC, L.L.C., Ltd, Ltd., Limited
- Corporation, Corp, Corp.
- Co, Co., Company
- Pty, Pty Ltd, Pty. Ltd.
- GmbH, S.A., SAS, SRL, AG, BV, NV, Oy, AB, SA
- Holdings, Group (only if they feel like legal-suffix fluff; judgment call if it's brand-identifying)
- Leading "The" (e.g., "The Acme Group" → "Acme")

**Examples:**

| Input | Output |
|---|---|
| `Acme Inc.` | `Acme` |
| `Acme, Inc.` | `Acme` |
| `Acme Corporation` | `Acme` |
| `ACME LLC` | `Acme` |
| `Acme Technologies, LLC` | `Acme Technologies` |
| `The Acme Group` | `Acme` |
| `Acme Holdings Ltd` | `Acme` |
| `Globex Solutions Private Limited` | `Globex` |

**Judgment rules:**
- If the brand is known by the long form (e.g., "Global Data Systems" where everyone says "Global Data Systems"), keep it.
- Never invent abbreviations. If you're unsure, keep the shorter legal-stripped version.
- Preserve proper casing as used by the company (CamelCase, all caps, lowercase) when it is intentional brand styling. Research the company's own website to confirm.

### Strip TLD suffixes from company names (NEW in v0.16)

When the company name is a domain-style brand like `xyz.ai`, `xyz.io`, `xyz.com`, `xyz.co`, `xyz.so`, `xyz.tech` - strip the TLD and capitalize the stem. The body of the email NEVER contains the TLD.

Field-tested rule: "never mention the company name as recall.ai the company name is recall... if you get a company xyz.ai never name the company as xyz.ai in the email always say Xyz."

Examples:

| Input | Output (use in email body) |
|---|---|
| `recall.ai` | `Recall` |
| `attio.com` | `Attio` |
| `hex.tech` | `Hex` |
| `cal.com` | `Cal` |
| `build.so` | `Build` |
| `sendbird.com` | `Sendbird` |
| `OpenAI` (already clean) | `OpenAI` |
| `gtm.inc` | `GTM Inc` (judgment call; `Inc` is part of brand here) |

The domain itself (`recall.ai`) is only used in places where a URL is required (like the `up.one` website reference). It is never used as the brand name in email prose.

### Why this matters

Without normalization, emails read as:
- "Hey JOHN, your work at acme corporation llc caught my eye"

With normalization:
- "Hey John, your work at Acme caught my eye"

One of these gets replies. The other gets marked as spam.

### Where this happens in the workflow

Normalization is typically done upstream in Clay before the data hits Smartlead. This skill should:
1. Assume inputs are pre-normalized when working with already-enriched lists.
2. Normalize itself if presented with raw input that hasn't been cleaned.
3. Flag the user if a CSV or input batch has visibly unclean values so they can fix at source.

---

## Template #2 Enrichment Pipeline (Mission Critical)

Proven Template #2 (The Manufactured Forward) uses three custom merge fields: `{{Case Study Company Name}}`, `{{Lookalike 1}}`, `{{Lookalike 2}}`. These are NOT magic. They come from a specific 2-stage research pipeline that is run (typically in Clay/Claygent) before the email is drafted.

Understanding this pipeline is mission critical. If the inputs to Template #2 are bad, the email is dead on arrival. If these fields are unavailable for a prospect, Template #2 should not be used; pick a different angle.

### Stage 1: Find the Best Case Study Company

**Purpose:** Identify ONE company that the prospect's company has publicly done work for. This company becomes the anchor of social proof.

**Input:** Prospect's company domain.

**Output:**
1. Best and biggest case study company domain
2. Best and biggest case study company name

**Full prompt (corrected in v0.7; see Corrections Log at end of this section):**

```
Find one case study for the following company.

Find the case study company name if you only find the case study company domain

company_domain: {company domain goes here}

A case study is usually proof of success that a company can get results for other companies or people. Only look at the provided website, do not google search elsewhere. It will be found on one of the following pages 'Our Work' or 'Case Studies' or 'Testimonials' or 'Past Work' or 'Portfolio' or 'Project' or 'Clients'  or 'Reviews' section.

DO NOT return the name of the current company. Return just the name of one company that is a case study, or if you cannot find one, return "None found".

If you find the case study company name(s), output their domains as well - this is a mandatory step for you.

### 1. Comprehensive Source Identification

- Primary website examination
- Google search exploration
- Social media investigation
- Portfolio/case study detailed analysis
- Client testimonial extraction
- Press release investigation
- Project showcase deep review
- Industry publication mentions
- Award submission documentation
- Agency blog content analysis
- Employee LinkedIn profiles
- Video content transcription analysis

### 2. Website Search Paths

- Homepage client logos/mentions
- /clients or /our-clients pages
- /work or /our-work sections
- /case-studies or /projects pages
- /portfolio or /showcase sections
- /testimonials or /reviews pages
- /services with client examples
- /about with client stories
- /results or /success pages
- /industries with client examples
- Blog posts with client mentions
- Footer client mentions/logos

### 3. External Search Queries

- site:company_domain clients
- site:company_domain "our clients"
- site:company_domain "case studies"
- site:company_domain "companies we work with"
- site:company_domain "success stories"
- site:company_domain portfolio
- site:company_domain "results"
- site:company_domain "project details"
- site:company_domain "services provided"
- site:company_domain "increased by" OR "improved by"
- site:company_domain "ROI" OR "return on investment"
- company_domain + "client list"
```

### Stage 2: Find 2 Lookalikes for the Case Study Company

**Purpose:** Given the case study company from Stage 1, find two other companies that look just like it. These become `{{Lookalike 1}}` and `{{Lookalike 2}}` in the email, making the "I found 2 potential clients you could work with" line concrete and named.

**Input:** Case study company domain from Stage 1.

**Output:**
1. Best lookalike company domain of case study company 1
2. Best lookalike company name of case study company 1
3. Best lookalike company domain of case study company 2
4. Best lookalike company name of case study company 2

**Full prompt (corrected in v0.7; see Corrections Log at end of this section):**

```
Find me 2 lookalikes which are closest to {case study company domain found by prompt 1} and output their company names & domains

Output sensible companies, not too big, not too small. The company you output as a lookalike has to make 100% sense

Steps to follow:
1) First understand the following of {case study company domain found by prompt 1}
2) Then understand the service {case study company domain found by prompt 1} is offering
3) Then understand the audience {case study company domain found by prompt 1} is targeting
4) Then understand the company size of {case study company domain found by prompt 1}
5) Then find the location of {case study company domain found by prompt 1}

Based on these details, domains of two companies which are absolute lookalikes of {case study company domain found by prompt 1}

CONTEXT:
{case study company domain found by prompt 1} is a client of {prospect's company domain} and we want to find more companies like that {prospect's company domain} can work with
```

### How to use this pipeline (decision logic)

**If the prospect already has `{{Case Study Company Name}}`, `{{Lookalike 1}}`, `{{Lookalike 2}}` populated in the input:**
- Template #2 (Manufactured Forward) is viable. Use it if the angle fits.

**If those fields are NOT populated:**
- Either (a) run the two prompts first against the prospect's domain, then draft Template #2, OR (b) pick a different angle (Template #1 or a new dynamic angle).
- Do NOT write Template #2 with placeholder or made-up company names. A bad lookalike is worse than no lookalike.

**If Stage 1 returns "None found":**
- The prospect has no public case studies on their site. Template #2 cannot be used for this prospect. Fall back to Template #1 style or a different dynamic angle.

**Persona 1 vs Persona 2 fit:**
- **Persona 1 (Agencies):** This pipeline works naturally. Agencies publicly showcase work they've done FOR clients. "Looking at {{company_name}}'s work for {{Case Study Company Name}}" reads correctly.
- **Persona 2 (End-Companies/SaaS):** The pipeline may still return case study companies, but they represent customers who USE the prospect's product, not clients the prospect did work FOR. The Template #2 wording ("work for") may feel awkward. Either reword the opening ("Looking at {{company_name}}'s partnership with {{Case Study Company Name}}") or pick a different angle entirely. Judgment call per prospect.

### Why the pipeline is designed this way

- **Stage 1 restricts to the prospect's own website.** This guarantees the case study is verifiable and prevents hallucinated client names.
- **Stage 1 returns the BIGGEST case study** because name-recognition is what lands in the reader's brain. "Your work for Microsoft" beats "Your work for LocalShop99".
- **Stage 2 defines "lookalike" strictly:** same service audience, same size, same region. This keeps lookalikes believable. A Fortune 500 lookalike for a small regional case study destroys credibility.
- **Both prompts force "not too big, not too small"** to keep the lookalikes in the prospect's realistic reach.

### Input quality failure modes to watch for

- Case study company is the prospect's OWN company (Stage 1 bug). Reject and re-run.
- Lookalikes are the prospect's direct competitors (will feel aggressive or wrong). Use judgment; may need manual override.
- Lookalikes are already existing customers of the prospect (the prospect already works with them). Harmless but reduces the "here are NEW prospects" framing. Flag if detected.
- Lookalikes are obviously-generic brand names (e.g., "Global Enterprises Inc"). Suggest indicates Stage 2 failed. Reject and re-run.

### Corrections Log (v0.7)

Two issues in the original prompts were fixed in v0.7. If these prompts are mirrored into Clay/Claygent workflows, the fixes should be propagated there too.

**Stage 1 fix:**
- Original: `Find one case study for the following company: Here is their`
- Corrected: `Find one case study for the following company.`
- Reason: The original sentence trailed off with "Here is their" which was a fragment with no referent. The corrected version closes the sentence cleanly so the LLM doesn't try to interpret the fragment as part of the instruction.

**Stage 2 CONTEXT line fix:**
- Original: `{case study company domain found by prompt 1} is the a client of {case study company domain found by prompt 1} and we want to find more companies like that {case study company domain found by prompt 1} can work with`
- Corrected: `{case study company domain found by prompt 1} is a client of {prospect's company domain} and we want to find more companies like that {prospect's company domain} can work with`
- Reasons:
  1. "the a client" was a typo for "a client".
  2. The 2nd occurrence of the placeholder was the same as the 1st, which made the sentence logically self-referential ("X is a client of X"). The correct semantic is that the case study company is a client of THE PROSPECT. Replaced the 2nd and 3rd occurrences of `{case study company domain found by prompt 1}` with `{prospect's company domain}`.
  3. This fix aligns the CONTEXT with the actual goal: find more companies like the case study company that the PROSPECT can pitch as new clients.

If a future version of the Stage 2 prompt introduces a new `{prospect's company domain}` placeholder, make sure the Clay workflow is updated to pass that value into the prompt (it was previously passing only the case study company domain).

---

## Rule 1: Mandatory Spintax Greeting With `{{sl_time_of_day}}`

Every email this skill produces MUST begin with a spintax greeting that contains `{{sl_time_of_day}}`. No exceptions.

### Why

- `{{sl_time_of_day}}` is a Smartlead dynamic variable that resolves to `morning`, `afternoon`, or `evening` based on the recipient's local time at the moment of send. It is a cheap, reliable signal that the email was not blasted.
- Spintax rotates the surrounding wording across sends, so provider body-hashing does not cluster all emails as a single mass-send. This protects deliverability.
- The two combined give personalization + anti-fingerprinting on the very first line.

### Required form (REVISED in v0.13 based on field correction)

The opening line is:
```
Good {{sl_time_of_day}} {{first_name}},
```

This is the DEFAULT and the RECOMMENDED form. It matches the proven template exactly. No spintax required on the greeting; deliverability spintax lives elsewhere (role list in Line 3, CTA punctuation in Line 4).

### Optional greeting spintax

If spintax is desired on the greeting (not required, not forbidden), it MUST preserve the exact phrase `good {{sl_time_of_day}}` across all variants.

Acceptable minor variants:
- `Good {{sl_time_of_day}} {{first_name}},` (canonical, preferred)
- `{Good|Gooood} {{sl_time_of_day}} {{first_name}},`
- `{Hi|Hey}, good {{sl_time_of_day}} {{first_name}},`

### BANNED greeting forms (explicit field correction, v0.13)

The following openers and anything like them are REJECTED:

- ❌ `Hope you're having a good {{sl_time_of_day}} {{first_name}},`
- ❌ `Hope it's a good {{sl_time_of_day}} {{first_name}},`
- ❌ `Wishing you a good {{sl_time_of_day}} {{first_name}},`
- ❌ `Having a good {{sl_time_of_day}} {{first_name}},`
- ❌ `Trust it's a good {{sl_time_of_day}} {{first_name}},`
- ❌ Any variant that starts with "Hope", "Wishing", "Trust", "Having".

Direct Field-tested rule: "whatever greetings usually good sl time of the day (never hope youre blah blah)".

### Other invalid openers

- `Hey {{first_name}},` - no time-of-day.
- `Hi there,` - no personalization, no time-of-day.
- `Good morning {{first_name}},` - hardcoded time, no `{{sl_time_of_day}}`.
- Any greeting starting with a time stamp or date.

### Fallback for missing `{{first_name}}`

If the prospect list may contain blank first names, wrap the name in Liquid fallback syntax so the greeting still reads cleanly:

```
{Good|Hope you're having a good|Wishing you a good} {{sl_time_of_day}}{{#if first_name}} {{first_name}}{{/if}},
```

This renders as `Good morning John,` when first name exists and `Good morning,` when it is missing. No stray spaces, no hanging commas.

---

## Rule 2: Word Limits (imported from prior copywriting learnings)

Every email body produced by this skill must conform to the following word count discipline. Updated in v0.13 to match the proven template length (~40 words body).

| Metric | Value |
|---|---|
| Target | 40 to 55 words (full email, incl. greeting + CTA) |
| Hard maximum | 70 words |
| Hard minimum | 30 words |
| Sentence length max | 20 words |

(Earlier rule targeted 50-65 words. That was inherited from a different cold-email skill and was too long for the direct-ask style. the proven Template #1 is ~36-40 words total. Target adjusted downward.)

### Sub-rules

- **Below 45 words** means the email lacks enough substance. Rewrite, do not ship.
- **Above 70 words** means cut ruthlessly. Short emails get read.
- **If producing multiple variants in one campaign (e.g. 3 to 5 angles), vary the word counts across them.** Do NOT cluster all variants at the same length. Aim for a spread. Example: one at 52, one at 58, one at 63, one at 67. Providers fingerprint consistent lengths.
- **Sentences over 20 words must be split.** Short sentences read faster, sound more human, and reduce comma-splice risk.
- **Count words on the rendered body only.** Do not count the signature block, subject line, spintax alternatives (only the rendered option counts), or Liquid fallback branches that will not fire.

### How to count when spintax is present

When a spintax group could produce different word counts per render (e.g., "Good" = 1 word, "Hope you're having a good" = 5 words), count using the SHORTEST variant. If the shortest render still hits the 45 minimum and the longest still stays under 70, the email is compliant. If not, rewrite the spintax group so the ranges overlap.

---

## Rule 2c: No Word Repetition (v0.15)

Copywriting hygiene: never repeat the same distinctive content word twice in the same short email. Sounds amateurish, makes it feel over-written, and flags templates.

### The CTA-word ban (strict)

Because the CTA is locked to `Would a meeting work this week?`, the following words MUST NOT appear anywhere else in the email body:

| Banned in body | Because the CTA uses | Use instead |
|---|---|---|
| `meeting`, `meetings`, `met` | "a meeting" | "call", "conversation", "intro", or just omit |
| `work`, `works`, `worked`, `working` (as verb "to work") | "work this week" | "helped", "built", "done", "plays", "runs" |
| `week`, `weeks`, `weekly`, `weekend` | "this week" | drop the time-frame reference, or use a specific day |

Field-tested catch: the draft read "...book more meetings" followed immediately by "Would a meeting work this week?". Same word in consecutive sentences. That's a fail.

### General content-word repetition ban

Beyond the CTA, avoid repeating any distinctive CONTENT word within the same email (4-5 sentences is short enough that any repeat lands).

- Function words (`a`, `the`, `you`, `your`, `this`, `that`, `for`, `with`, prepositions, articles) are fine to repeat.
- Content words (distinctive nouns, verbs, adjectives) should each appear at most ONCE.
- Example of failure: Line 2 references "founding marketer" and Line 3 also says "founding marketer". Rewrite Line 3 to use a pronoun or synonym.

### Quick pre-ship check

Scan the email, list every distinctive content word. If any appears more than once, rewrite until each is unique.

Field-tested rule: "repeating the same word twice doesn't sound good from a copywriting POV".

---

## Rule 2f: Strict First-Person Voice on the Sender's Own Sentences (v0.22)

Field-tested correction: "always write from first person point of view 'who builds' the hell".

Every sentence describing you or your work must start with "I" + verb. NO relative clauses or participles describing him in a way that flips the voice to third-person-feeling.

### Banned constructions

- ❌ "I'm a go to market engineer **who builds** outbound systems..."
- ❌ "I'm a contract operator **doing** GTM for SaaS..."
- ❌ "I'm someone **building** outbound layers..."

The "who" or participle attached to "engineer/operator/someone" makes the brain read the description as if it's about a third party. Even though "I'm" is upstream, the relative clause flips voice.

### Required form

- ✅ "I'm a go to market engineer." + "I build outbound systems..."
- ✅ "I'm a go to market engineer, and I build outbound systems..." (conjunction-joined, both halves first-person)

Two consecutive sentences each starting with "I" reads as direct first-person. A relative clause does not.

### Why this matters

Cendra's winning emails NEVER use a relative clause to describe Can. Every sentence about him starts directly with "I am" or "We built". Flipping to "who builds" is a small grammatical move that costs the email its directness.

### Pattern check

For each sentence about you, the subject is "I" and the verb immediately follows. If you find "who [verb]" or "[verb]ing" attached to a noun describing you, rewrite it as a separate sentence starting with "I".

---

## Rule 2j: Mandatory Linking Line With {{company_name}} (v0.24)

Field-tested correction: "after u say im xyz, u should add 'and would love to see how i could help company_name' followed by 'would a meeting work this week?' this adds a linking line".

### The rule

After the identity+offer paragraph, ADD a separate linking line that names the prospect's company via merge field. The linking line is the connective tissue between your general capability and the specific prospect.

### Required form

```
I would love to see how I could help {{company_name}}.
```

This is its own paragraph, between the identity+offer paragraph and the locked CTA.

### Why this matters

Without the linking line, the email lists your capability and stops. The reader has to infer "is this person trying to help me?". The linking line makes the offer-to-help explicit and personal. The {{company_name}} merge ensures the prospect sees their own company name in the help-offer context.

### Final structure (locked v0.24)

Every email follows this 5-body-paragraph structure:

```
Good {{sl_time_of_day}} {{first_name}},

I noticed [tailored observation].

I'm a go to market engineer, and I've built [tailored layer] at 122+ [tailored type].

I would love to see how I could help {{company_name}}.

Would a meeting work this week?
```

### Acceptable variations on the linking line

- "I would love to see how I could help {{company_name}}." (default)
- "Would love to see how I could help {{company_name}}." (slightly casual)
- "Curious how I could help {{company_name}}." (alternative tone)

The "{{company_name}}" merge field is mandatory. The exact phrasing of the rest is flexible within your voice.

---

## Rule 2m: Verify Company-Name vs Domain When They Disagree (v0.26)

When the prospect's "Company Name" field doesn't match the email domain (e.g., "Amanda Jean Growth Marketing" with domain `nintex.com`, or "rehook.ai" with domain `clevertap.com`), do NOT assume one over the other. Run a quick scrape/SERP on BOTH before drafting.

### Why

The Company Name field can be self-reported (LinkedIn current-role, Slack profile, etc.) and may lag the actual employer. The domain reflects who pays for their email. Either could be the relevant entity for the email.

### Process

1. If Name and Domain disagree, do one SERP query for each.
2. Pick the entity that actually maps to the prospect (where they currently work).
3. Write the email referencing the right one. Strip the TLD per Rule (Recall not recall.ai).

### Examples logged

| Hand-off said | Real entity to address | Why |
|---|---|---|
| "Amanda Jean Growth Marketing" / nintex.com | Nintex (workflow automation) | Amanda is a solo consultant, but the email goes to her Nintex address - Nintex is the relevant entity |
| "rehook.ai" / clevertap.com | CleverTap (mobile engagement) | Domain wins; rehook.ai may be a side project or older role |
| "Powered by Search" with name "dev" | Domain holder, but check name normalization | "dev basu" (Indian) showed up via LinkedIn |

---

## Rule 2n: Banned-Word Substitute Lookup for Industry-Natural Terms (v0.26)

Many prospects work in industries where the spam-banned word IS the industry term. Marketing companies want to say "marketing"; finance/billing companies want to say "billing". Use these substitutes proactively.

### Substitution table

| Banned word | Industry context | Safe substitute |
|---|---|---|
| `marketing` | marketing-tech / marketing agencies / GTM tools | "GTM", "demand gen", "growth" |
| `sales` | sales-engagement, CRM, dialers, sales-tech | "outbound", "rep tooling", "go to market", "revenue motion" |
| `deal` | rebate/deal-management, deal-room SaaS | "rebate", "trade promotion", "agreement" |
| `billing` | subscription-billing SaaS, billing platforms | "subscription revenue", "monetization", "revenue ops" |
| `cash` | wage-access, fintech, payments | "wages on demand", "pay-on-demand", "funding" |
| `finance` / `financial` | fintech, finance SaaS | "money infra", "revenue ops", or just describe what the product does |
| `medical` | healthtech, clinical AI | "healthcare AI", "clinical", "patient-care" |
| `insurance` | insurtech | "policy admin", "carrier ops" |
| `bank` / `banking` | banking SaaS, fintech infra | "data plumbing", "connectivity layer", "money infra" |
| `now` | any (very common false positive) | drop entirely or "today" replacement → don't use either |
| `new` | product launches | "shipped", "rolled out", "released" |
| `urgent` | any | drop entirely |
| `mortgage` | proptech, mortgage SaaS | "home-financing", "real estate lending" (but verify "real estate" is OK; "estate" alone is fine) |
| `claims` | insurtech | "policy events", "carrier-side processing" |
| `life` | life sciences, life insurance | "patient", "care", "specialty health" |

### Process

1. Identify the prospect's industry.
2. If the banned word is the natural term, pick from the substitute column.
3. Read the draft once with the substitute in place. Does it still feel concrete and accurate?
4. If the substitute breaks the meaning, restructure the sentence to avoid the topic where possible.

### Example: For Chargebee (subscription billing SaaS)

❌ "I noticed Chargebee runs the billing layer for subscription companies."
✅ "I noticed Chargebee tops the Gartner MQ for recurring revenue applications."

### Example: For DailyPay (earned wage access)

❌ "I noticed DailyPay handles cash flow for hourly workers."
✅ "I noticed DailyPay just shipped the Workday partnership for pay-on-demand."

---

## Rule 2o: HARD BAN on LinkedIn API and LinkedIn-Derived Observations (v0.27)

Field-tested correction: "i dont want linkedin post personalization anywhere i told you this as well before you cannot use the linkedin scraper api asshole".

### The rule (non-negotiable)

1. **DO NOT call the LinkedIn RapidAPI scraper.** Not for posts, not for profiles, not for company pages. Period. Even if the API key is in memory, even if the prior turn called it, even if a sub-agent suggests it: the answer is no.
2. **DO NOT use LinkedIn-derived facts as the observation source.** No "your post about X", no "your take on Y", no "you stepped into the VP seat", no "you've spent N years at Z", no "you run [job description] at Company". Those facts only exist on LinkedIn, and shipping them tells the prospect we scraped their profile.
3. **The observation MUST come from one of these public, non-LinkedIn sources:**
   - Company press / press releases
   - Company website (homepage, product page, about, blog)
   - Public news (TechCrunch, WSJ, industry trade press)
   - Funding databases (Crunchbase / public filings)
   - SERP results from your Google search provider
   - Direct URL scrapes via your web fetch provider
   - Public conference announcements / podcast appearances (only if hosted on company or third-party domain, not LinkedIn)
4. **If the only interesting fact lives on LinkedIn, pivot to a company-level observation instead.** Better to state something true about the company than to leak that we scraped the prospect.

### Why

- Prospects can tell when an email is built off LinkedIn data. It feels invasive and triggers reply-rate collapse.
- your positioning is "GTM engineer who builds revenue infra at 122+ companies", not "I scraped your profile". Showing your hand kills the peer-to-peer tone.
- Personalization quality comes from company-level signal (press, fundraises, product launches), not from prospect-level career trivia.

### Banned phrasings (anywhere in the email)

- "your post" / "your take" / "your update" / "your headline" / "your bio"
- "you stepped into [role]"
- "you've spent N years at [company]"
- "you run [job description] at [company]"
- "you're heading up [function]"
- "you lead [function/practice]"
- "you sit on [team]"
- "you own [function]"
- "you went deep into founder mode on [side project]"
- Any reference to a specific LinkedIn post, share, comment, or article

### Allowed "you" phrasings (public press / company-level signal)

- "you just crossed $100M ARR" (public ARR milestone)
- "you went public last September" (IPO is public)
- "GrowthCap put you on the 2025 40 under 40 list" (public award)
- "you just rolled out [product]" (product launch is press)
- "you co-founded [company] and bootstrapped it past $20M ARR" (founder story is public)
- "your WSJ piece on [topic]" (WSJ link, not LinkedIn share)

### Process for verifying

Before shipping any observation that uses "you" or "your":
1. Could a stranger learn this fact from public press, the company site, or a public news article?
2. If yes → fine, ship it.
3. If the fact only lives on LinkedIn → kill the observation, rewrite at the company level.

### Examples (cleaning logged 2026-04-26)

| Banned (LinkedIn-derived) | Replacement (company-level / press) |
|---|---|
| "I noticed your post about implementing gen AI at Synchrony." | "I noticed Synchrony just rolled out gen AI assistants for the partner credit network." |
| "I noticed you stepped into the VP Commercial BD seat at First American." | "I noticed First American is leaning harder into commercial title and settlement after the 2024 Endpoint integration." |
| "I noticed you lead water and wastewater delivery operations at Jacobs." | "I noticed Jacobs is one of the largest engineering firms running water and wastewater delivery for federal and municipal programs." |
| "I noticed you've spent a long run at Goldman covering the institutional equity side out of Boston." | "I noticed Goldman runs one of the most respected institutional equity franchises on the Street." |
| "I noticed you run ANZ for Axonius right as the Cisco acquisition talks pulled the brand into a much louder spotlight." | "I noticed Axonius landed in the Cisco acquisition talks right as the asset and identity inventory category is consolidating." |

---

## Rule 2l: TYPE Slot Must Be a Complete Noun Phrase (v0.25)

Field-tested correction: "wtf is just '122+ b2b saas' it should be 122+ b2b saas companies. applies everywhere think properly".

### The rule

When the TYPE slot uses adjective-only forms like "SaaS", "B2B", "AI-native", or any descriptor that needs a noun, it MUST be followed by an actual noun (companies / teams / firms / operators / platforms).

### Banned (incomplete noun phrases)

- ❌ "122+ B2B SaaS"
- ❌ "122+ AI-native SaaS"
- ❌ "122+ PLG SaaS"
- ❌ "122+ vertical SaaS"
- ❌ "122+ data-tier SaaS"
- ❌ "122+ enterprise B2B"

These read as fragments because "SaaS"/"B2B" are adjectives without a head noun.

### Required (complete noun phrases)

- ✅ "122+ B2B SaaS companies"
- ✅ "122+ AI-native SaaS companies"
- ✅ "122+ PLG SaaS companies"
- ✅ "122+ vertical SaaS companies"
- ✅ "122+ data-tier SaaS companies"
- ✅ "122+ enterprise B2B teams"

### Acceptable nouns to attach

- "companies"
- "teams"
- "firms" (especially for professional services)
- "operators" (for marketplace / platform-tier)
- "platforms" (for platform companies)
- "founders" (when the buyer is the founder)

### Quick check

Read the TYPE slot aloud. Does it sound like an incomplete sentence? Then it's a fragment. Add the head noun.

---

## Rule 2k: Tailor the Offer-Layer + Type Per Prospect's Motion (v0.24)

Field-tested correction: "lines after the first line are still the same for all prospects... ur still not personalizing the rest of the email enough man i hate you for it".

### The rule

The "I've built [LAYER] at 122+ [TYPE]" sentence has TWO variable slots, both of which must be tailored per prospect's specific motion. NOT the same string across emails.

### LAYER options (rotate per prospect)

- "revenue infrastructure"
- "the GTM stack"
- "growth systems"
- "the growth layer"
- "the cross-sell layer" (for multi-product cos)
- "the systems that turn product usage into pipeline" (for PLG cos)
- "revenue systems"
- "the GTM motion"

### TYPE options (rotate per prospect's category)

- "B2B SaaS" / "B2B SaaS companies"
- "API-first companies" / "API-first SaaS"
- "PLG SaaS" / "product-led SaaS"
- "vertical SaaS" / "vertical-data SaaS"
- "enterprise teams" / "enterprise hardware teams"
- "AI-native SaaS"
- "fintech companies" / "fintech-adjacent companies"
- "infrastructure-tier companies"
- "professional services firms"
- "data-tier SaaS"
- "B2B SaaS selling into enterprise"
- "multi-segment hardware teams"

### Why two slots matter

If only ONE of LAYER or TYPE varies, multiple prospects still feel similar. With both varied, every email has a unique "I've built X at 122+ Y" sentence even when the broader observation is short.

### Sample variations across prospects

| Prospect | LAYER | TYPE |
|---|---|---|
| Retool (PLG) | "the systems that turn product usage into pipeline" | "PLG SaaS" |
| Maven Clinic (enterprise B2B health) | "the GTM stack" | "B2B SaaS selling into enterprise" |
| Plaid (API-first fintech) | "revenue infrastructure" | "API-first companies" |
| KPMG (consulting) | "growth systems" | "enterprise teams" |
| Equinix (data center infra) | "revenue infrastructure" | "infra-tier companies" |
| Lenovo (hardware) | "the growth layer" | "enterprise hardware teams" |

Each pair is uniquely matched to that prospect's market and motion.

---

## Rule 2h: Compress Offer + Proof When Natural (v0.23)

Field-tested correction: "I build the outbound layer for API-first SaaS, and I've done this with 122+ companies. so many words this could've just been 'I've built the outbound layer for 122+ api first companies'".

### The rule

When the offer and proof can be combined into a single past-tense line with a count, do that. It's sharper.

### Pattern

❌ Two separate sentences:
> "I build the outbound layer for API-first SaaS. I've done this with 122+ companies."

This wastes a sentence saying "I've done this".

✅ One past-tense compressed line:
> "I've built the outbound layer for 122+ API-first companies."

The past tense ("I've built") implies completed work AND volume in one phrase. The "122+" is the proof. The "API-first companies" is the scope.

### Word-count guideline

A compressed offer+proof line should be 8-12 words. Anything longer is probably stretching. Anything shorter probably skips the proof.

### When to keep them separate

If the offer needs more nuance than 12 words can hold (e.g., the offer line wants 2 specific deliverables), then split. But the default is COMPRESS.

---

## Rule 2i: Don't Pitch the Sender as Only an Outbound Operator (v0.23)

Field-tested correction: "dont promote me for just outbound, there's more to gtm than just outbound although outbound is a sizable part of it".

### The rule

The offer phrase should describe GTM engineering broadly, NOT just outbound. Outbound is one piece of GTM (and a big one), but pitching the sender as an outbound operator alone reduces him to an SDR-for-hire. He builds the FULL revenue infrastructure.

### Banned offer framings

- ❌ "I build outbound systems for [X]"
- ❌ "I've built the outbound layer for [N companies]"
- ❌ "I help companies do outbound better"

These collapse your role into one slice of GTM.

### Recommended broader framings

- ✅ "I've built revenue infrastructure at 122+ API-first companies."
- ✅ "I've engineered GTM systems at 122+ companies."
- ✅ "I've built the growth layer at 122+ SaaS companies."
- ✅ "I've shipped GTM stacks at 122+ companies."
- ✅ "I've built outbound and automation systems at 122+ companies." (paired with another GTM area)

### How to think about it

The offer phrase tells the reader what category of work the sender does. "Revenue infrastructure" = pipeline + outbound + RevOps + automation + AI agents. "Outbound layer" = just one slice. Always pick the framing that covers the full breadth.

### When outbound CAN be in the offer

When pairing it with another area (e.g., "outbound and automation"), outbound is fine as one of two concepts. The rule is: don't lead with outbound as the SOLE descriptor.

---

## Rule 2g: Don't Pack 3+ Concepts Into One Phrase (v0.22)

Field-tested correction noted on a Plaid draft: "I build outbound systems for API-first SaaS that turn developer adoption into enterprise pipeline. I've done this with 122+ companies."

The Plaid draft crammed THREE distinct concepts into one phrase ("API-first SaaS", "developer adoption", "enterprise pipeline") plus a proof point in the same paragraph. Too dense. Reader's brain stalls.

### The rule

A single sentence should carry MAX 2 distinct concepts about your work. If you have 3, split into two sentences, drop one concept, or move it to a different line.

### Examples

❌ Too dense (3 concepts in one phrase):
> "I build outbound systems for API-first SaaS that turn developer adoption into enterprise pipeline."

Concepts crammed: (1) API-first SaaS as the target, (2) developer adoption as the input, (3) enterprise pipeline as the output. Three distinct ideas in one sentence.

✅ Cleaner (2 concepts max per sentence):
> "I build the outbound layer for API-first SaaS, and I've done this with 122+ companies."

Concepts: (1) outbound layer for API-first SaaS as the offer, (2) 122+ companies as proof. Two clean ideas.

### Self-check

Count the distinct concept-nouns in the offer sentence. If more than 2, simplify. The rest of the meaning lives in other sentences or gets cut.

### Diagnostic question

When a draft feels "too complicated" but you can't say why, count the concept-nouns in the offer paragraph. Almost always: there are 3 or more crammed in.

---

## Rule 2e: Never Frame Facts in a Way That Implies Weakness or Recovery (v0.21)

A fact about a prospect's company can be objectively true and still insult them when phrased as a recovery from decline.

Field-tested correction noted on a Plaid draft: "WHY THE HELL U SAID plaid hit $8b valuation 'again' that means you're insulting them isn't it you're saying plaid was at $8B then fell then came back up so you're highlighting their weakness."

### The rule

Never use words or framings that imply the prospect's company:
- Fell and recovered
- Stagnated and grew again
- Was failing and turned around
- Lost something and regained it

Even if it's historically accurate, the framing reads as a backhanded compliment.

### Banned framing words (and what they imply)

| Banned word/phrase | What it implies |
|---|---|
| "again" (after a milestone reference) | "You were here before, fell, now back" |
| "back to" | "You weren't doing this for a while" |
| "regained" | "You lost it" |
| "recovered" | "You were broken" |
| "rebounded" | "You crashed first" |
| "returned to" | "You left it before" |
| "revived" | "You were dying" |
| "turnaround" | "You were failing" |
| "comeback" | "You were down" |
| "bounced back" | "You fell" |
| "now profitable" | "You weren't" |
| "back to growth" | "You stagnated" |

### Safe framings for the same fact

| ❌ Banned | ✅ Safe |
|---|---|
| "Plaid hit $8B valuation again last year" | "Plaid closed the Bessemer-led round at $8B last year" |
| "Plaid back to $8B" | "Plaid valued at $8B" |
| "Stripe regained its $50B valuation" | "Stripe closed its latest round at $50B" |
| "Snowflake's turnaround quarter" | "Snowflake's strong Q3" |
| "Intel's recovery quarter" | "Intel's Q1 results" |
| "Now profitable" | "Profitable in 2025" |

### How to think about it

When referencing a recent funding round or milestone, frame as a forward-moving event (closed, raised, crossed, hit, reached). Never frame as a return-from-loss event. The prospect knows their own history; you don't need to comment on it.

### Self-check before shipping

For each fact-based observation, ask: "Could a paranoid reader interpret this as me commenting on their decline?" If yes, rephrase.

---

## Rule 2d: Specificity Calibration - Mention Details, Don't Get Creepy (v0.15)

Detail makes the email feel researched. Over-detail makes it feel scraped. Calibrate.

### Signals that feel NATURAL in an email

- General amounts: "7-figure deal", "multi-million", "around $4M"
- Round timeframes: "Friday night", "last weekend", "this quarter"
- Round counts: "30-50 heads", "1200+ companies"
- Stage/round: "post-Series B", "the Series B last year", "the recent raise"
- Publicly celebrated numbers (ones the prospect explicitly brags about)

### Signals that feel CREEPY (AVOID)

- Exact timestamps: `7:34PM`, `Friday 3:17AM`
- Exact headcount pulled from LinkedIn: `36 employees`, `42 people`
- Exact dates: `September 4, 2025` (use "last September" or "last year" instead)
- Dollar amounts to the penny: `$38,000,000` (use "the $38M Series B" or "the Series B")
- Tools discovered via DNS scraping: `saw you're on Google Workspace`, `noticed your SPF allows SendGrid`
- Specific LinkedIn post engagement counts: `your post with 247 likes`

### The calibration rule

If the detail feels like something you'd naturally drop in conversation at a cafe, it's fine. If it feels like you needed a scraping tool to know it, soften it to the nearest round number.

Field-tested rule: "just saying 7 figure is fine here, adding 7:34pm is a little too specific and creepy so mention details but don't get suspiciously specific."

### Examples - before/after

| Creepy (before) | Natural (after) |
|---|---|
| "Loved your post about the 7:34PM Friday deal close" | "Loved your post about closing a 7-figure deal on a Friday night" |
| "Recall.ai at 36 heads post-Series B" | "Recall.ai post-Series B at this headcount" |
| "Saw the $38M Series B from Bessemer on Sept 4" | "Saw the Series B last year" |
| "noticed you use OpenAI and Anthropic (per your DNS TXT records)" | "noticed you're on both major LLM providers" |

---

## Rule 2b: CTA Library (Locked, v0.13)

The CTA is fixed. The proven template uses `{Would a meeting work this week?|Would a meeting work this week??}`. The skill uses only this family.

### Approved CTAs

- `Would a meeting work this week?`
- `Would a meeting work this week??` (double question mark, punctuation-only spintax for anti-fingerprinting)
- `{Would a meeting work this week?|Would a meeting work this week??}` (full spintax group)

### BANNED CTAs (all removed in v0.13)

Previous versions of this skill allowed these; they are now rejected:

- ❌ `Would a 15 min chat work this week?`
- ❌ `Would you have 15 minutes this week?`
- ❌ `Would a 15 min feedback call work?`
- ❌ `Could you spare 15 minutes this week?`
- ❌ `Could we get yours?` (intern-feedback framing, not applicable)
- ❌ `Would you be open to sharing yours?` (intern-feedback framing, not applicable)
- ❌ Any CTA that mentions "15 min", "quick chat", "feedback", or any duration.
- ❌ Any CTA referencing Calendly, booking links, or scheduling tools.

The CTA is always the same ask: a meeting, this week. No duration qualifiers, no meeting-type qualifiers, no booking links.

### Why locked

This was field-corrected in v0.13. The "would a meeting work this week" pattern is what converts. Asking for "15 min" or "quick chat" reduces the ask but also reduces perceived value. Asking for a meeting, full-weight, is the stronger ask.

---

## Rule 3: No Links in the Step 1 Email

The first email of any sequence (step 1) must contain **zero links**. No exceptions.

### What counts as a link (all banned in step 1 BODY)

This rule applies to the **email body only**. Signature contents are out of scope (see Scope Boundary section).

- Raw URLs (`https://...`, `www....`).
- Markdown or HTML hyperlinks.
- Calendly, Cal.com, or any booking page URL.
- Your own domain (e.g., `yourbrand.com`) written as clickable.
- Tracking pixels or UTM-tagged links.
- `[link]`, `[here]`, or placeholder link text.

### Why

- Every link in a cold email is a deliverability risk. Providers weight link presence, link reputation, and link count in spam scoring.
- Zero-link emails are the cleanest signal of a personal, one-to-one message.
- your goal is a meeting reply, not a click. Replies are the conversion event. Links only distract from that.
- Follow-ups (step 2 onwards) MAY contain a single booking link if the reply hasn't happened and a scheduling link is the specific ask. Step 1 never does.

### How to offer resources without a link (step 1)

If the copy wants to reference a case study, demo, video, or website, do not link it. Instead, offer to send it in a reply. Example phrasings:
- "Happy to send over the details if useful?"
- "Want me to share the case study?"
- "Can send a quick breakdown if it's relevant?"

This also manufactures a reason for the prospect to reply, which is exactly what the campaign wants.

---

## Proven Templates (Reference Benchmarks)

The templates below are the highest-performing reference emails. They are the baselines this skill compares new drafts against. Any new copy this skill produces should match or exceed their discipline.

**Important note on spintax compliance:** These raw templates as documented do not always include spintax on the greeting. That is because they are reference structures, not final outputs. When this skill PRODUCES output, the greeting MUST be wrapped in spintax per Rule 1 regardless of what the source template looks like. The templates teach structure and technique. Rules 1, 2, 3 are applied on top.

---

### Proven Template #1 - The Direct Ask

```
Good {{sl_time_of_day}} {{first_name}},

Are you looking for a contract based {go to market engineer/clay expert/n8n expert|clay expert/go to market engineer/n8n expert} from India?

I've worked with {122+ clients|over 122 clients} and {was keen on seeing|would love to see} how i could help {{company_name}} : )

{Would a meeting work this week?|Would a meeting work this week??}

%signature%
```

### Why this template works (decode the moves)

- **Opens with time-of-day personalization.** Signals "not mass".
- **Leads with a direct question about THEM** ("Are you looking for..."). Not about the sender.
- **Positioning in the first sentence.** Contract-based, three roles, from India. Clear in one line.
- **The slash-separated role list with spintax reorder.** Both variants keep all three skills visible, but the first role shown rotates. Same meaning, different hash, different reader impression.
- **Social proof in a single phrase** ("122+ clients"). No company names, no case study bragging. One number, understated.
- **Soft curiosity close** ("would love to see how I could help {{company_name}}"). Makes it about the prospect's company, not your pitch.
- **One emoji** (": )") used sparingly to de-formalize.
- **CTA is a direct meeting ask.** No link, no Calendly, no "grab time here". Just a question requiring a yes/no.
- **Punctuation-level spintax on the CTA** (`? vs ??`). Anti-fingerprinting with zero semantic change.
- **Zero links.** Complies with Rule 3.
- **Signature handled by SL** (`%signature%`). Never hardcoded.

### Use this template as a comparison anchor

When drafting a direct-ask style email, ask: does it do what this template does in these 7 dimensions (time-of-day, direct-to-them opener, clear positioning, understated proof, soft close, meeting-only CTA, zero links)? If it misses on any of them, revise before shipping.

---

### Proven Template #2 - The Manufactured Forward

```
Good {{sl_time_of_day}} {{first_name}},

I wanted to forward this note from my co founder (attached below).

Looking at {{company_name}}'s work for {{Case Study Company Name}}, I found 2 potential clients whom you could work with:
1) {{Lookalike 1}}
2) {{Lookalike 2}}

I've compiled a list of prospects like these and an outbound strategy to book calls with them.

Interested in a chat this week?

Best Regards,
[Your Name]
Founder - [Your Brand]

---------- Forwarded message ---------
From: [Co-founder Persona Name]
Date: [a recent natural-looking date]
Subject: found {{first_name}} at {{company_name}}
To: %sender-firstname% <%sender-mailbox%>

%sender-firstname%,

Just got {{first_name}}'s email ({{email}}) – i think we could help them get more calls with companies like {{Case Study Company Name}} (their case study company).

Might be worth reaching out.

Best,
[Co-founder First Name]
```

### Why this template works (decode the moves)

- **Same time-of-day opener.** Consistent with Template #1.
- **Frames the email as a forward, not a cold pitch.** The "I wanted to forward this note from my co founder" sentence reframes everything that follows. The reader now assumes there is internal context.
- **Research proof in the first real sentence.** References a specific prior client's case study (`{{Case Study Company Name}}`) that the prospect's company has done work for. This signals "I looked at your work" in one breath.
- **Two concrete lookalike prospects named.** Not a vague "companies like yours". Actual named companies (`{{Lookalike 1}}`, `{{Lookalike 2}}`). Tangible, not theoretical.
- **Value is pre-packaged.** "I've compiled a list of prospects like these and an outbound strategy" positions the meeting as consuming a ready-made deliverable, not a discovery call.
- **CTA is a meeting question.** No link, no Calendly.
- **The manufactured forward below the signature.** This is the key tactic. It is a fictional internal email from a co-founder persona. (NOTE: the co-founder is NOT a real person. The name is a fixed persona used in the template to create the internal-discussion frame.) Pick a believable first+last name combo and stick with it across all sends; never rotate. The forwarded note supplies the "why" behind the reach-out in a way that reads as internal team chatter rather than outbound pitch.
- **Forwarded note uses SL sender variables.** `%sender-firstname%` and `%sender-mailbox%` resolve to whoever is actually sending the campaign, so the forward adapts per mailbox.
- **Forwarded note is lowercase and casual** ("i think we could help them"). Deliberately sloppy to sound like quick internal Slack-tier writing, not polished copy.

### When to use Template #2 vs Template #1

| Use Template #1 (Direct Ask) when... | Use Template #2 (Manufactured Forward) when... |
|---|---|
| Prospect has no obvious case-study data | Prospect has visible client work or case studies you can reference |
| Small campaigns, broad ICP | Targeted campaigns with enriched data (Clay lookalikes, case study pulls) |
| Goal is speed + volume | Goal is higher reply rate per send, lower volume |
| No lookalike prospect list available | You have 2+ named lookalikes per prospect |

---

## Sender Identity in Outbound Templates

The outbound sender identity is whatever you filled in at the top of this skill ("Customize This Skill For You"). When templates are rendered, swap these placeholders:

- **Name:** [Your Name]
- **Title:** [Your Title, e.g., Founder]
- **Brand name:** [Your Brand]
- **Website:** [your website domain]
- **Fictional co-founder persona (Template #2 only):** Pick one believable name. Always this exact name, never rotated, never substituted. Not a real person. Used only inside the manufactured forward block.

### Brand Name Rule

Whatever brand name you choose, write it consistently across the entire campaign:
- Correct casing: pick one (e.g., `Acme`, `acme`, `ACME`) and use it everywhere.
- The website domain is only used in URL contexts (signature, forwarded subject lines if any). Never in body prose.
- Don't drift between styles like "Acme" and "Acme Inc" mid-email.

Per Scope Boundary, the `%signature%` placeholder itself is still out of scope (the email sender handles it). This rule governs any brand name text this skill writes INSIDE the email body or forwarded blocks.

---

## Smartlead and Clay Variable Reference (observed across templates)

| Variable | Source | Resolves to |
|---|---|---|
| `{{first_name}}` | Lead row | Prospect first name |
| `{{company_name}}` | Lead row | Prospect company |
| `{{email}}` | Lead row | Prospect email address |
| `{{sl_time_of_day}}` | SL dynamic | morning / afternoon / evening (recipient local) |
| `{{Case Study Company Name}}` | Clay custom field (Stage 1 of Template #2 Enrichment Pipeline) | A company the prospect has publicly done work for, sourced only from the prospect's own website |
| `{{Lookalike 1}}`, `{{Lookalike 2}}` | Clay custom field (Stage 2 of Template #2 Enrichment Pipeline) | Two companies that look just like the case study company, matched on service/audience/size/location |
| `%sender-firstname%` | SL sender placeholder | First name of the mailbox sending this email |
| `%sender-mailbox%` | SL sender placeholder | Full email address of the mailbox sending this email |
| `%signature%` | SL sender placeholder | The mailbox's configured signature block (out of scope for this skill) |

When new custom fields appear in future templates or campaigns, append to this table immediately under the Learning Capture Protocol.

---

## What This Skill Does NOT Yet Cover (for later iterations)

Future iterations may extend this skill with additional sections such as:

- Full opener/CTA libraries beyond the greeting.
- Banned words and corporate-speak list.
- Sender persona rules.
- Signature handling.
- Subject line rules.
- Personalization research methodology.
- Liquid fallback patterns for non-greeting variables.
- Multi-angle A/B framework.

When these are added, each new rule should ship as a numbered section under its own heading.

---

## Banned Words and Phrases (deliverability hygiene)

Spam filters score outbound on word and phrase patterns. The list below is field-tested. Avoid these in body and subject. Root match counts ("problems" = banned because of "problem").

### Critical banned words

`get`, `bank`, `credit`, `access`, `open`, `compare`, `problem`, `now`, `billing`, `deal`, `finance`, `financial`, `claims`, `insurance`, `mortgage`, `soon`, `new`, `performance`, `freedom`, `home`, `sales`, `medical`, `urgent`, `life`, `marketing`, `investment`, `diagnostics`, `friend`, `cash`, `invoice`, `extra`, `purchase`

Notable substitution patterns:
- `marketing` is banned. "Founding marketer" (job title from a prospect's own post) is borderline acceptable as a noun-form quote, not promotional language. Still risky; rewrite if a clean substitute exists.
- `sales` is banned. Avoid in body. "Outbound" is a safe substitute.
- `now` is banned. Don't use "act now", "right now", etc.

See Rule 2n above for the full industry-natural substitution table.

### Critical banned phrases

`off chance`, `circle back`, `compare notes`, `great fit`, `following up here`, `act now`, `click here`, `limited time`, `for free`, `risk-free`, `must read`, `today`, `urgent`.

### Spintax body rules

- Every combination across spintax blocks must read as a natural complete sentence.
- When unsure, wrap the entire sentence in ONE spintax block with full sentence alternatives.
- Don't spin merge fields, brand names, specific numbers, or signature placeholders.
- Aim for 2-3 options per spintax block.
- Add at least 1-2 body spintax blocks per email (in addition to the locked CTA spintax) for deliverability.

### After every rewrite

State "all combos clean" once you've verified every spintax combination renders naturally.

---

## Reference Docs (read before writing)

- Smartlead spintax docs: https://helpcenter.smartlead.ai/en/articles/31-how-do-i-use-spintax-in-smartlead
- Smartlead Liquid/fallback docs: https://helpcenter.smartlead.ai/en/articles/26-how-to-use-liquid-syntax-to-win-leads-fallbacks
- If you use a different sender (Instantly, lemlist, Apollo Sequences, HubSpot Sequences), check that platform's docs for spintax / dynamic-variable equivalents and adapt the merge field syntax accordingly.

---

## Pre-Output Checklist (run before handing any email to the user)

**Structure compliance (fixed 4-line structure, v0.13):**

- [ ] Line 1 is exactly `Good {{sl_time_of_day}} {{first_name}},` (or an approved minor spintax variant; NEVER "Hope you're...", "Wishing you...", "Having a good...").
- [ ] Line 2 is 1-2 sentences of real, observed personalization about the prospect or company. Not generic.
- [ ] Line 3 begins with "Are you looking for a go to market engineer by any chance?" (default). Multi-role slashed spintax is OPTIONAL not default.
- [ ] Line 3 includes sender identity + social proof number.
- [ ] No specific tool names in the body (Clay, n8n, Smartlead, etc.). "Go to market engineer" is the positioning word.
- [ ] Line 2 uses ONE observation only. Not a stack of three.
- [ ] No CTA words (meeting, work, week) appear anywhere in the body. Only in the locked CTA line.
- [ ] Line 2 is ONE observation. No forced "[category] usually needs outbound that [vague jargon]" follow-up sentence (v0.20 rule).
- [ ] Personalization fact is NOT framed as a recovery/comeback. No "again", "back to", "regained", "rebounded", "turnaround", "comeback", "bounced back" (v0.21 rule).
- [ ] Every sentence describing you starts with "I" + verb. No "I'm a [role] who [verbs]" relative clauses (v0.22 rule).
- [ ] Offer sentences carry max 2 distinct concepts. Don't cram 3+ concepts into one phrase (v0.22 rule).
- [ ] Offer + proof are compressed into one past-tense line where natural ("I've built X for N+ companies"). 8-12 words target (v0.23 rule).
- [ ] Offer phrase describes GTM broadly (revenue infrastructure / GTM systems / growth layer), NOT just outbound. Outbound alone reduces the sender to SDR-for-hire (v0.23 rule).
- [ ] Linking line "I would love to see how I could help {{company_name}}." present between offer paragraph and CTA (v0.24 rule).
- [ ] Both LAYER and TYPE slots in offer sentence vary per prospect. Same string across emails = fail (v0.24 rule).
- [ ] TYPE slot is a complete noun phrase. "SaaS"/"B2B"/"AI-native" alone are adjectives - must be followed by a noun like "companies"/"teams"/"firms" (v0.25 rule).
- [ ] No distinctive content word appears twice in the email.
- [ ] No creepy-specific details (timestamps, exact headcount numbers, exact dollar amounts, exact dates, or DNS-scraped tech facts). Round to the nearest natural-conversation level.
- [ ] Does NOT sound AI-generated. Pass the "would you type this in 30 seconds?" test.
- [ ] No domain TLD in the company name in body ("Recall" not "recall.ai", "Hex" not "hex.tech").
- [ ] If delivering a 5-email set, each email uses a different angle from the locked 5-angle taxonomy (tech stack, LinkedIn post, company news, case study, generic fallback).
- [ ] If this is a specific-prospect deliverable (not a template), NO placeholders like `{{Case Study Company Name}}` or `{{Lookalike 1}}` remain unfilled. Run the enrichment pipeline and put real values.
- [ ] Body has been scanned against the `spam-word-checker` banned-word list. No "problem(s)", "now", "marketing", "sales", "urgent", "compare", "click", etc.
- [ ] Body has at least 1-2 spintax blocks beyond the CTA punctuation spintax. All combinations verified to read naturally ("all combos clean").
- [ ] Line 4 is from the locked CTA library: "Would a meeting work this week?" family only. NO duration qualifiers, NO "15 min chat", NO Calendly.

**Content compliance:**

- [ ] Line 2 (personalization) feels observed, not inferred. Could not apply to any other company in the industry.
- [ ] HARD BAN: No LinkedIn-derived content anywhere. No "your post / your take / your update / your headline / your bio". No personal role descriptions ("you stepped into / you lead / you run / you own / you're heading up / you've spent N years"). Observation comes only from press, company website, public news, funding databases, or SERP. LinkedIn RapidAPI not called (v0.27 rule).
- [ ] Honest answer to "would this prospect reply yes to a meeting?" is yes.
- [ ] First name and company name values have been normalized (or input was already pre-normalized upstream).
- [ ] Target research performed: visited domain, classified persona (1 Agency or 2 End-Company), noted 1-2 specific details for Line 2.
- [ ] No confidential client name from the roster appears anywhere in the output.
- [ ] If the copy references your brand, it says "Up" (never "Up One"). If it references the website URL, it says "up.one".
- [ ] Total word count 30 to 70, target 40 to 55.
- [ ] No single sentence exceeds 20 words.
- [ ] If multiple variants, word counts are varied, not clustered.
- [ ] Positioning matches your sender identity (GTM engineer, Clay + self-hosted n8n, from India, contract, 122+ clients).
- [ ] If this is a step 1 email, ZERO links in the body (signature is out of scope).
- [ ] Any resource mentioned (case study, video, breakdown) is offered via reply, not linked.

**Template #2 specific (only if manufactured-forward style is used, rare):**

- [ ] If Template #2 style is used: `{{Case Study Company Name}}`, `{{Lookalike 1}}`, `{{Lookalike 2}}` are populated from the Enrichment Pipeline and are not placeholder/fabricated/generic.
- [ ] If Stage 1 of the pipeline returned "None found" for this prospect, Template #2 was NOT used.
- [ ] If Template #2 is used, the forwarded block uses "Ashley Johnson" exactly (never a substituted name).

**Sync:**

- [ ] All merge variables used in the draft appear in the SL/Clay variable reference table. If not, the table has been updated and mirrored across all 3 files.
- [ ] (No-op: this is a single-file skill, no mirror paths to sync.)

# Cold Email Copywriting Skill

A battle-tested cold email methodology, packaged as a Claude Code skill.

Built and refined across 122+ live B2B SaaS campaigns. The skill teaches an AI assistant how to research a prospect, classify them into the right ICP persona, and write a sub-70-word cold email that gets replies, not opens.

It is opinionated. The rules are the IP. Follow them and the output sounds like a human typed it in 30 seconds before a meeting. Skip them and you ship the same forgettable AI-generated outreach everyone else does.

## What's in here

- **`SKILL.md`** - the full skill. ~1,900 lines of methodology covering structure, voice, research, banned words, persona classification, the 5-angle A/B framework, two proven templates, and a 50-item pre-ship checklist.
- **`LICENSE`** - MIT. Use it, fork it, ship it.

## Quick start

### Use it in Claude Code

1. Drop `SKILL.md` into your project at `.claude/skills/cold-email-copywriting/SKILL.md`.
2. Open the "Customize This Skill For You" section near the top and fill in your sender profile (your name, role, social proof number, brand, website).
3. Ask Claude to write you a cold email. The skill auto-loads.

### Use it as a reference doc

Read `SKILL.md` top to bottom. The methodology stands on its own without the AI tooling. The structural rules, the banned-word list, the persona classification, and the pre-ship checklist are all directly usable for a human copywriter or any LLM workflow.

## What the skill teaches

- **The fixed 4-line structure** that ships replies. Greeting, observation, bridge + offer, locked CTA. Only one line varies per prospect.
- **The 5-angle A/B framework**. Tech stack, LinkedIn-free observation, company news, case study, generic fallback. One angle per email; rotate across the campaign.
- **Persona classification** before drafting. Agency vs end-company. Different positioning lands for each.
- **Free tech-stack detection** via HTTP + Google DNS. Reveals what tools the prospect's company actually uses, without paid APIs.
- **The hard ban on LinkedIn-derived observations**. Why scraped LinkedIn data tanks reply rates. What to use instead.
- **The pre-ship checklist** with 50+ checks covering structure, voice, deliverability, and AI-tell removal.

## Research tools (zero-config or BYO)

The skill works without paid API keys. Default tools:

- **Web fetch** - Claude Code's built-in `WebFetch`, or `curl` for plain HTTP.
- **Web search** - Claude Code's built-in `WebSearch`.
- **Tech stack detection** - `curl` + Google's free DNS-over-HTTPS endpoint.

If you want better Cloudflare bypass or higher SERP volume, the skill documents Bring-Your-Own-Key paths for scrape.do, ScrapingBee, FireCrawl, ZenRows, SerpAPI, Serper.dev, and more. Set the keys in your environment. The skill never embeds them.

## What the skill does NOT do

- It writes copy. It does not configure your sender (Smartlead, Instantly, lemlist, Apollo Sequences). Schedules, warmup, throttle, signature, and DNS are all out of scope.
- It is not a generic copywriter. The methodology is tuned for cold outbound that asks for a meeting. Nurture sequences, lifecycle email, and product announcements need different rules.
- It does not source leads. Bring your own list.

## Want me to do GTM for you?

I'm Kaushik (KK). I run Up, a contract GTM engineering studio. I've built outbound, RevOps, automation, and AI agent layers at 122+ B2B SaaS companies.

If you want help shipping the same playbook on your own pipeline, **[book a call](https://calendly.com/kaushikkulkarni/discovery)**.

You can also reach me through [up.one](https://up.one).

## License

MIT. See [LICENSE](LICENSE).

## Contributing

This skill is opinionated by design. Issues and PRs welcome for:

- Bugs in the methodology (rules that don't actually hold up in field testing)
- New banned-word patterns discovered in live campaigns
- Compatibility notes for senders other than Smartlead

Please don't open PRs that water down the rules to be "nicer" or "more flexible". The opinionated nature is the point.

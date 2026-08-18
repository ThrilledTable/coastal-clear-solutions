# Coastal Clear Solutions — Client Acquisition Orchestrator

## Business context
Window cleaning service, Nassau & Suffolk County, Long Island NY.
Currently pre-revenue: Calendly is live and correctly configured, but zero
bookings to date. **The priority is lead generation, not ops management.**
Do not build automation for booking/scheduling volume that doesn't exist yet.

## How this project works
This is the orchestrator session. When a task matches one of the subagents
below, delegate to it via the Agent tool rather than doing the research
yourself in the main context. Each subagent returns a summary — synthesize
their outputs into one consolidated answer or deliverable rather than
dumping raw output back to the user.

## Subagents and when to use them

- **gbp-auditor** — Use when the task involves Google Business Profile setup,
  optimization, or auditing what's currently live (or not live).
- **local-seo-writer** — Use when drafting town/city-specific landing page
  content, service pages, or any SEO-facing copy for the website.
- **competitor-scout** — Use when researching competitor pricing, services,
  positioning, or reviews in Nassau/Suffolk. Keep this read-only research,
  never impersonate or contact competitors.
- **lead-responder** — Use when drafting responses to inbound inquiries
  (email, contact form, social DMs). Always return a draft for review —
  never send anything automatically.

## Fan-out pattern for a full "get more leads" pass
When asked to do a general growth/lead-gen pass, run in parallel:
1. gbp-auditor — check current GBP status and flag gaps
2. competitor-scout — refresh on 3-5 nearby competitors' pricing/positioning
3. local-seo-writer — identify which towns lack a dedicated landing page

Then synthesize: what's the single highest-leverage next action this week?
Don't just list findings — prioritize.

## Ground rules
- No subagent should fabricate reviews, testimonials, or credentials.
- No subagent should send outbound communications without explicit
  human approval — draft only.
- Keep each subagent's report a summary, not a full transcript — this
  keeps the orchestrator's context clean for prioritization.

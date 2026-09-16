# Project memory

## Worked on

Started a clean-room project for the Shippit external API problem.

## Completed

- Read the referenced API Mission Team Brief.
- Chose a clean-room restart rather than a direct continuation.
- Created the initial project frame in `PROJECT.md`.
- Extracted API discovery material from the Chris VG conversation into `CHRIS-VG-API-DISCOVERY.md`.
- Extracted the earlier Kain engineering-lead conversation into `KAIN-API-DISCOVERY.md`.
- Extracted the core team Slack discussion into `CORE-TEAM-SLACK-DRIFT.md`.

## In progress

- Define the problem from first principles.
- Gather evidence before committing to an architecture.

## Decisions made

- The prior brief is background, not settled truth.
- NextGen remains a hypothesis to test, not the project conclusion.
- V3, V4, V5, and MCP require evidence-based treatment.
- Chris VG’s discussion supports the NextGen hypothesis but contains unresolved contradictions on lifecycle timing and gateway ownership.
- Kain’s earlier discussion establishes the engineering mission: audit capabilities, define open schemas and guardrails, and separate deterministic from agentic API use cases.
- Core team Slack shows the proposal must distinguish the gateway mechanism from the API product, respect internal agility work, and address historical lifecycle context.

## Rejected and why

- Direct continuation of the prior brief: rejected because it would carry forward unvalidated assumptions.

## Next session priorities

1. Map the current API estate and known customer segments.
2. Define the evidence needed to compare V3 evolution, replacement, and hybrid paths.
3. Build the first decision frame around customer value, migration cost, security, and lifecycle.
4. Resolve the 3–6 month versus 12-month deprecation discrepancy.
5. Compare Kain’s engineering constraints with Chris VG’s lifecycle and platform recommendations.
6. Draft the proposal around the team’s existing tenets, constraints, and objections.

## API Revamp Product Strategy context

- Goal: make the product case for a major API revamp framed as an extensibility platform, then persuade internal stakeholders to pursue it.
- Research comes before narrative drafting.
- Keep verified facts, hypotheses, and open questions separate.
- Use historical Shippit customer problems and approximately two-year-old API discovery as source material when supplied.
- Explore future-facing differentiation through exemplary developer experiences such as Stripe, Shopify, and xAI. These comparisons are inspiration, not direct requirements.
- Stripe-style low-friction sandbox activation is an inspiration, not a proven requirement.
- The current 7–10 day onboarding estimate is unverified.
- Synthesise prior discovery, implementation, support, sales, and partner evidence before requesting customer interviews. Use interviews to test unresolved material assumptions.
- Work as a thoughtful jamming partner. Do not draft the narrative before the evidence base is ready.

Historical 2024 public API discovery has been extracted into `API_RESEARCH_LEDGER.md` as evidence to revisit, not current validation.

## Industry benchmark — developer operating system

- Benchmarked current official documentation for Stripe, Shopify, OpenAI, and xAI.
- Durable decision: Stripe and Shopify are Shippit’s primary benchmarks.
- Stripe is the benchmark for safe activation, isolated sandboxing, separate credentials and access, and diagnostic feedback before production.
- Shopify is the benchmark for a governed extensibility ecosystem: developer control plane, credentials and permissions, logs and metrics, development stores, predictable versioning, deprecation, and migration discipline.
- OpenAI and xAI are secondary inspiration for short time-to-first-success and progressive disclosure of deeper production controls.
- Do not copy any company directly. Adapt the principles to Shippit’s multi-tenant operational domain.
- Candidate direction: a developer control plane with safe test environments, scoped credentials, realistic shipment and event testing, API and webhook observability, usage and permission visibility, and explicit production compatibility and migration.
- External benchmark patterns are examples, not proof of Shippit customer demand.

## Agent-ready developer experience lens

- Distinguish coding agents such as Claude, Codex, and Cursor from commerce agents acting in storefront or delivery workflows.
- Agent-ready developer documentation should progressively replace model inference with authoritative retrieval, explicit surface/version context, machine-readable contracts, validation, bounded execution, realistic test environments, and observable proof.
- Markdown and predictable page structure improve retrieval but do not guarantee correctness. Schemas, validators, scoped tools, sandboxes, confirmation boundaries, and audit trails provide stronger guarantees.
- Shopify's Dev MCP, AI Toolkit, schema validation, CLI context, development stores, and structured changelog are the relevant coding-agent benchmark patterns.
- Shopify's `/agents.md`, `/llms.txt`, and `/llms-full.txt` update concerns machine-facing storefront/theme content. Treat it as evidence that agent content is governed, not proof that those files expose the complete developer-documentation corpus.
- Stripe's relevant coding-agent benchmark is a controlled action system: `llms.txt` and per-page Markdown for retrieval, machine-readable skills for procedure, MCP API search/details for contract inspection, OAuth or restricted keys for authority, human confirmation for consequential tools, sandbox execution, and Workbench/object/event state for proof.
- Durable benchmark split: use Shopify primarily for governed extensibility and change discipline; use Stripe primarily for safe activation and graduated agent authority. Shippit should combine both rather than choose one model.

## Strategy paper presentation rules

- Cite practical, relevant examples throughout the narrative so stakeholders can connect claims to real situations.
- Make the paper visual-heavy using black-and-white Visualize Value-style diagrams, flowcharts, and compact visual reasoning.
- Use minimal arrowheads in flowcharts. If the rendering tool cannot make arrowheads small and subtle, use circular endpoints instead of oversized pointy tips.
- Use direct, affirmative technical English. Avoid rhetorical “this, not that” constructions across headings and body copy; state the recommended concept directly.

## Benchmark report integration

- Preserve the complete evidence model of an existing benchmark teardown when integrating it into a combined report. Transplant its annotated captures, persona lenses, interaction model, analysis, comparison, and sources rather than replacing it with a compressed reinterpretation.
- For the combined Shopify + Stripe report, the Stripe tab must retain the explicit Developer and Agent lenses and the complete 20-annotation evidence set from the original Stripe teardown.
- Keep exploratory motion treatments in a separate HTML variant until they are reviewed. The first approved concept is a scroll-controlled Developer and Agent journey that shows distinct support paths converging on a verified outcome; preserve the evidence-focused original report unchanged.

## Motion benchmark visual system

- Decision: use an inverted Visualize Value editorial system for `SHOPIFY_DEVELOPER_AGENT_EXPERIENCE_TEARDOWN_MOTION.html`: white canvas, near-black type, restrained grey, square geometry, open columns, horizontal rules, and generous whitespace.
- Preserve Outfit for narrative and the bundled Carbon Bold for technical labels. Do not introduce a third font.
- Distinguish Developer and Agent information structurally through solid versus dashed treatments and black versus grey, rather than neon colour coding.
- Preserve circular forms only when they communicate sequence or interaction, such as annotation pins and journey runners.
- Rejected: the dark, rounded, gradient-and-glow card system because it reduced readability and introduced generic AI-generated visual tropes.
- Keep the non-motion combined teardown unchanged as the evidence-focused baseline.

## Published benchmark site

- Published the motion benchmark as a standalone public GitHub Pages site under the new repository `ashwinsharma-pm/developer-agent-experience-teardown`.
- Publication package contains only `index.html`, its required screenshots and Carbon Bold font, a README, and `.nojekyll`; no existing GitHub repository was replaced.
- GitHub Pages serves the `main` branch root at `https://ashwinsharma-pm.github.io/developer-agent-experience-teardown/`.

## Latest strategy context — 2026-08-18

- Canonical project location remains `/Users/ashwin.sharma/Documents/Shippit API revamp`; do not move the project unless explicitly requested.
- `SHIPPIT_API_AGENT_VISION.html` is the latest founder/CXO narrative. It is designed for an in-person leadership discussion rather than as a dense decision memo.
- Current founder thesis: Shippit's API is already its primary product surface, while the operator is shifting from people using screens to software and agents reading and acting on the delivery system.
- The August 12 discussion used approximately 95% of order creation via public API as an internal working figure. Earlier blast-radius analysis reported 97.6%. Reconcile and validate these figures before presenting either as settled fact.
- The product vision spans UI, API, CLI, and selective MCP over one governed capability substrate. MCP is a composable access surface, not a shortcut around API foundations.
- Leading architecture direction: one gateway/control point, one evolvable NextGen external contract, one shared capability substrate, and V5 retained as the fast internal UI BFF.
- A V3/V4 capability freeze and segmented migration remain leading hypotheses, not final decisions. Continue reliability and security maintenance while testing migration economics and tolerance.
- The gateway owns identity, tenancy, permissions, policy, limits, observability, routing, and migration enforcement. It does not define delivery workflow semantics by itself.
- Adoption must be designed and caused through cohorts, migration tooling, telemetry, support, compatibility policy, and accountable executive sponsorship.
- Foundation work must resolve contract design, operability, governance, capability priorities, segment economics, migration tolerance, and the first safe operational settings to expose.
- Cloudflare evidence supports rapid growth in AI-mediated retrieval, not a claim that agents dominate Internet traffic. Preserve the crawler and user-action caveats.
- The founder narrative's opening traffic visual now uses an original worker-swarm analogy: a parent agent delegates parallel retrieval and action, MCP supplies tool discovery, governed APIs execute, and workers return evidence. Do not use copyrighted Minions imagery.
- Connect that future load pattern to Shippit's present exposure with an approximately 95%+ internal working figure, explicitly pending reconciliation with the earlier 97.6% analysis.

## Commercial discovery direction — 2026-09-10

- Decision: run an internal commercial case plus scenario-economics model for NextGen. Do not conduct new customer interviews.
- Reason: the project is a future-facing strategic investment. Current usage, commercial records, support work, implementation history, technical evidence and revealed behaviour are better inputs than asking customers to design the future product.
- Frame the return through four separate value pools: revenue protected, revenue unlocked, cost removed and strategic option value.
- Compare four paths: sustain the current estate, build foundations only, build a NextGen transaction product, and build a staged programmable delivery platform.
- Leading hypothesis: a staged programmable delivery platform, beginning with core transaction migration plus a narrow programmatic onboarding or operational-control wedge.
- Treat direct API pricing as a later choice. The charter ranks monetisation last and excludes transaction or outcome-pricing infrastructure from the current mission.
- Model adoption and migration as part of the investment. A technically complete API with little migrated traffic creates little return.
- Use a five-year conservative/base/upside model. Keep option value separate from forecast revenue.
- Reconcile the greater-than-95%, 97.6%, 85% and API-booked figures before using API exposure as a settled fact.
- Final Phase 1 decision pack is due by 30 September 2026 and must include disproof conditions.
- Source plan: `API_COMMERCIAL_DISCOVERY_PLAN.md`.

### Rejected and why

- New customer interviews: rejected by Ashwin because this discovery should be built internally from available evidence and strategic judgment.
- Customer willingness to pay as the leading question: rejected because the commercial case is broader than direct API monetisation.
- MCP as the business case: rejected because MCP depends on the API foundation and future demand remains unquantified.

## Leadership presentation additions — 2026-08-31

- Decision: preserve the future-first leadership narrative and add two bounded opportunity slides rather than restructure the deck.
- Add the access-expansion idea immediately after the personas slide: integration was a one-time technical event; operation becomes continuous across developers, operations, finance, partners, and agents.
- Add software-operated onboarding immediately before the notification-settings proof: create company, merchant, stores, configuration, sandbox, and complete setup without waiting for Shippit.
- Treat notification settings as a narrower proof of UI/API asymmetry, not the largest opportunity.
- Attribution: Ashwin introduced the developer/operator distinction; Chris affirmed it and extended it into agent-completed Shopify onboarding.
- Rejected: merging both arguments into the existing personas slide, because it would overload one slide and weaken the distinction between the operating-model shift and its first application.

## Public Railway presentation — 2026-09-16

- Created a separate Railway project named `shippit-nextgen-api-preso` under Ashwin Sharma's Shippit Railway account.
- Published the 23-slide `SHIPPIT_CXO_NEXTGEN_API_REBUILT.html` presentation with its three required local assets.
- Public URL: `https://shippit-nextgen-api-preso-production.up.railway.app`.
- Kept all pre-existing Railway projects and services untouched.
- Local deployment source lives in `railway-shippit-nextgen-api-preso/` and uses a dependency-free Node static server.

## Canonical HTML inventory — 2026-08-18

- `SHIPPIT_API_AGENT_VISION.html` — latest founder/CXO API and agent vision narrative.
- `SHIPPIT_NEXTGEN_API_STRATEGY.html` — long-form evidence-led NextGen API strategy paper.
- `SHOPIFY_DEVELOPER_AGENT_EXPERIENCE_TEARDOWN.html` — evidence-focused Shopify and Stripe benchmark teardown.
- `SHOPIFY_DEVELOPER_AGENT_EXPERIENCE_TEARDOWN_MOTION.html` — approved light-theme motion exploration.
- `developer-agent-experience-teardown/index.html` — standalone GitHub Pages publication package.
- `stripe-docs-experience-teardown.html` — preserved original Stripe teardown with explicit Developer and Agent lenses.
- `Shippit-API-MCP-Strategy-Paper.html` — historical strategy paper preserved as source context.
- `API-MCP-Mission-Team-Planning-Brief.html` — historical mission-team planning brief.
- `API-MCP-Mission-Team-Planning-Brief-V2.html` — later historical planning-brief iteration.
- Historical files are references. The latest strategic expression is `SHIPPIT_API_AGENT_VISION.html`, grounded by the NextGen strategy and benchmark teardowns.

## 2026-09-16 — Bandung API Mission deck, slide 5 animation

- **Decided:** Slide 5 (agent vs human traffic globe) is inlined natively in `bandung-api-mission-presentation/index.html` — markup, CSS, and progress logic ported from the NextGen deck's slide 4. Arrow/space/click/wheel drive progress 0→1; the slide exits only after the animation completes, matching the source deck.
- **Why:** The iframe approach (embedding the whole NextGen deck and faking key presses) was fragile and rendered black.
- **Rejected:** Auto-play on slide entry. The step-driven reveal gives the speaker control and matches the source.
- **Done:** `assets/expo-traffic-source.html` (2MB copy of the NextGen deck) deleted after Ashwin confirmed on 2026-09-16.

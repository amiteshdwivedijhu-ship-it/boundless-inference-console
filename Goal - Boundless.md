# GOAL.md - Boundless (2-hour build)


## Standing rules (keep in every GOAL.md)

### Prototype, not demo-as-deliverable
Build a working prototype Ami can walk through in 90 seconds. The deliverable is the prototype. The 90-second demo is only how Ami presents that prototype. Do not treat a demo as the thing you ship.

### UI observation (mandatory)
Public sources only: website screenshots, demo videos (with timestamps), product tours, docs, help center, app-store screenshots, changelog images. Never sign up, create accounts, or log in.

Every GOAL.md must include `## Their UI` before Acceptance criteria, with subsections in this order:
1. Sources
2. Layout
3. Visual style
4. Tone of UI copy
5. The exact screen where my proposed improvement would live
6. Build instruction (match their visual style and terminology so the prototype looks like a feature inside their product)

Be honest: if only marketing illustrations are visible, say "marketing UI only" and infer carefully. If no UI is publicly visible, say so, describe what can be inferred from docs, and default to a clean neutral style.

Writing: simple English. No em dashes or en dashes.

### Phone / mobile UX (mandatory for the prototype)
- Include a proper viewport meta tag so the layout respects phone width.
- Design mobile-first for about 375px width (stack everything vertically).
- No horizontal scroll at phone width.
- Touch-friendly primary actions (about 44px min height / tap target).
- Readable type on a phone (comfortable body size, clear hierarchy).
- No overlays, sticky bars, or modal chrome that clips content or blocks CTAs.
- Good mobile UX overall: one-column flow, large CTAs, thumb-reachable Choose model / Tune serving / Deploy / Retune actions.

## Role this GOAL targets
- **Open role (LOCKED):** Founding Product Manager
- JD: https://apply.workable.com/boundless-networks-inc-1/j/8F417E2E0D/ (short: https://apply.workable.com/j/8F417E2E0D)
- Careers board: https://boundless.network/careers
- Signal: X post by Veronica (@v_garg_s) ~3h before research ET on 2026-09-30: "We're hiring! Come be part of the new era of inference." Roles named: Applied AI eng, Senior Infra eng, Founding product, Technical BD. Linked bit.ly/4rBu46x (see URL note) and https://boundless.network/careers. Company headline on careers: "Rewrite how the world serves AI."
- URL note: https://bit.ly/4rBu46x currently 301s to https://www.wemakedevs.org/aws/env (Environmental Hacks / WeMakeDevs), which is unrelated. Treat careers + Workable as the authoritative apply path. Do not use the bit.ly as an apply link.
- Location: United States, Remote (Workable + careers). Remote-first with regular off-sites (JD). Technical BD listing is San Francisco + Remote; Founding Product is United States / Remote. Ami: Baltimore MD, open to US relocate / remote; remote US is a strong fit.
- Comp (public): Proposed band between US$100k and $150k annually + equity allocation (Workable JD). Health / dental / vision for U.S. employees; flexible PTO; professional development and conference travel budget.
- Core job (from JD): Founding PM at early product lifecycle. Own roadmap across AI inference, RL/post-training, and GPU compute. Work backwards from customers into PRDs / working-backwards docs. Lead engineers day-to-day with VP of Engineering. Partner with Technical BD to turn field signal into product bets. Ship 0 to 1 under ambiguity with strong product intuition. Technical enough for inference / RL / GPU fluency.
- Bar notes: Product leadership at both an AI startup and a larger / non-startup company; deep AI infra / compute / inference landscape knowledge; 2 to 6 years PM; 0 to 1 launch track record. Nice to have: ML/AI infra or GPU / distributed systems; working-backwards / PR-FAQ; prior IC eng; platform or API GTM.
- Sponsorship: JD says global applicants are welcome and lists remote-first. No explicit H-1B / visa sentence found. No public Boundless-specific H-1B petition history verified this pass. Confirm in-country H-1B transfer early. Do not treat silence as a yes or a no.
- Parked (do not build against unless Founding Product JD disappears):
  - Applied AI/ML Engineer: https://apply.workable.com/boundless-networks-inc-1/j/9145B5CA1A/ (United States / Remote)
  - Senior Infrastructure Engineer - GPU Compute: https://apply.workable.com/boundless-networks-inc-1/j/EA9774C09A/ (United States / Remote)
  - Technical Business Developer: https://apply.workable.com/boundless-networks-inc-1/j/82C20E6FB1/ (San Francisco, CA / Remote)

## Company brief (8th-grade English)
Boundless is the inference partner for AI-native companies. Thesis: inference should be fitted to the product it serves. They help teams choose the right open-weight (and catalog) model for a workload, tune the serving path (precision, parallelism, caching, batching, routing), and operate it in production against quality, latency, throughput, and cost targets, often via an OpenAI-compatible API. They also sell forward-deployed inference: Boundless engineers sit with the customer from model selection and evals through serving design, deploy, and day-to-day ops. Public surfaces: boundless.network (marketing), model library, forward-deployed inference, inference.boundless.network (console / playground; Sign in exists; never use), Vercel AI Gateway listing. Roots: Boundless Network Inc. grew from coordinating distributed GPUs for zero-knowledge proving (ZKC token economy still discussed for operator staking). July 2026 SiliconANGLE: ~4,000 GPUs opened toward managed AI inference; CEO Shiv Shankar (ex Coinbase, Ava Labs, Amazon; formerly RISC Zero leadership). Parent / sibling funding context often cited as RISC Zero ~$52M to $54M (seed ~$12M Bain Capital Crypto, Series A ~$40M Blockchain Capital). Treat a separate "Boundless $27M Paradigm seed" claim as unverified third-party noise unless primary press appears. Early access / Boundless AI launch post: 2026-09-03. HQ / team framing: global, remote-first; LinkedIn company boundless-networks; X @BoundlessHQ.

## /goal
Build a working **Product-Fitted Inference Console** for Boundless Founding Product: load a synthetic AI-native customer whose inference sits on the product critical path, show a workload stub (quality bar, context shape, latency / cost targets, traffic pattern), a Boundless model recommendation with cited fit chips, a serving-tune packet (precision, batching, caching, routing), then let Ami pick a human gate (Deploy tuned path / Retune under traffic / Need better eval set / Escalate to forward-deployed eng) and show production impact (p95 latency, cost per task, throughput). Prove Ami can productize choose → tune → serve for product-fitted open-model inference, which is Boundless's wedge and the Founding PM roadmap surface (inference + GPU compute, with RL/post-training as adjacent roadmap, not the hero). Ami must walk through this prototype in 90 seconds.

**Hard product rule:** Do NOT center the hero on a Rubric Lens strip, pass/fail spreadsheet, or graded eval table. Thin quality / fit chips on the model recommendation are OK as secondary UI only (Boundless does model selection and evals as part of the partner workflow). The hero is workload fit → model choose → serving tune → deploy / operate gate → production impact.

## Live demo
- Status: built
- Link: https://amiteshdwivedijhu-ship-it.github.io/boundless-inference-console/
- What it is: Boundless-styled Product-Fitted Inference Console (workload stub → model recommendation → serving-tune packet → Deploy / Retune / Need evals / Escalate → production impact)

## Scope (fits 2 hours)
- Synthetic inputs only (no real Boundless API keys, never sign in to inference.boundless.network, never mint a real agent-key, never create an account, never call live inference).
- 1 primary path: synthetic customer (example: long-horizon agent rollouts for a B2B AI product) → workload stub filled → model recommendation (example: open-weight coding / agent model from public library labels) with fit chips → serving-tune packet → Ami taps Deploy tuned path → status becomes In production / Operating, impact strip shows lower cost per task and p95 within target.
- Optional second path: incomplete eval set or unclear quality bar → Need better eval set gate; status stays "Not ready to deploy" with listed missing items.
- Optional third path: traffic shape changed (burst batch vs interactive) → Retune under traffic with updated batching / caching / routing chips; or Escalate to forward-deployed eng for hands-on partner work.
- Console must show: customer + workload stub, model recommendation chips, serving-tune chips, human gates (~44px), and a one-line production impact (p95 / $/task / throughput).
- Out of scope: live inference API, real GPU scheduling, ZKC staking UI, signed-in console, Rubric Lens as hero, full RL/post-training trainer product as the main story, Applied AI eng or infra eng tooling, Technical BD CRM, outreach.

## Reuse first
- Reuse **evidence / citation packet + human gate** craft from https://amiteshdwivedijhu-ship-it.github.io/ (evidence spans, approve / request / escalate style gates mapped to Deploy tuned path / Retune under traffic / Need better eval set / Escalate to forward-deployed eng).
- Light touch only: fit / quality chips as secondary on the model recommendation. Do NOT force Rubric Lens or a kill-or-ship spreadsheet into the Boundless hero. Do not pitch Ellipsis as a Boundless customer.
- Vocabulary to prefer: Boundless, inference partner, product-fitted inference, open-weight models, model selection, serving path, forward-deployed inference, OpenAI-compatible API, latency, throughput, cost per task, p95, precision, parallelism, caching, batching, routing, operate in production, workload, quality threshold, context shape, Deploy tuned path, Retune under traffic. Avoid: scorecard-as-hero, Rubric Lens brand, generic "AI magic" slogans, hyperscaler-clone chrome that fights Boundless warm paper + purple accent.

## Their UI

**Honesty note:** Public sources = marketing site, model library, forward-deployed inference page, news posts, careers, and the public inference console landing / playground chrome (Sign in / Try anonymously / harness setup). Never sign in. No public "customer workload fit console" or internal Founding PM roadmap tool was observed. This prototype is **inferred product surface** for choose → tune → serve, styled to feel like Boundless. Say when something is inferred. Optional local public HTML under `ui/`.

### Sources
- Homepage: https://boundless.network/
- Careers ("Rewrite how the world serves AI."): https://boundless.network/careers
- Forward-deployed inference: https://boundless.network/product/forward-deployed-inference
- Model library: https://boundless.network/models
- Introducing Boundless AI (2026-09-03): https://boundless.network/news/introducing-boundless-ai-the-inference-partner-for-ai-native-startups
- Shadow traffic eng blog (2026-09-24): https://boundless.network/news/shadow-traffic
- Inference console / playground landing (public; Sign in exists; never use): https://inference.boundless.network/ ; https://inference.boundless.network/playground
- Vercel AI Gateway Boundless provider listing: https://vercel.com/ai-gateway/models/providers/boundless
- SiliconANGLE AI expansion (2026-07-14): https://siliconangle.com/2026/07/14/boundless-taps-idle-crypto-gpus-cut-ai-inference-costs/
- Founding Product Manager JD: https://apply.workable.com/boundless-networks-inc-1/j/8F417E2E0D/
- Optional saved public HTML: `ui/home.html`, `ui/careers.html`, `ui/forward-deployed-inference.html`, `ui/models.html`, `ui/introducing-boundless-ai-the-inference-partner-for-ai-native-startups.html`, `ui/shadow-traffic.html`, `ui/inference-console-landing.html`, `ui/founding-pm-jd.md`

### Layout
- Marketing site: warm paper canvas, dark ink headlines (serif display + sans body), top nav (Product / How it works / Models / Company), CTAs "Talk to an engineer" / "Get started", sections for choose model → tune to traffic → operate in production. Source: https://boundless.network/ ; local `ui/home.html`.
- Model library: searchable cards with model name, "Best for", context, $/MTOK input/output. Source: https://boundless.network/models .
- Forward-deployed: numbered partner steps (model selection and evals → serving-system design → benchmarking and deployment → operations and changes). Source: https://boundless.network/product/forward-deployed-inference .
- Inference console landing (public): Overview / Playground / Models / Rankings / API Keys / Usage / Members / Docs; "Try anonymously" / harness prompt; Sign in. Signed-in Workspace not observed (never sign in). Source: https://inference.boundless.network/ ; local `ui/inference-console-landing.html`.
- Inferred product surface for this prototype: a **Product-Fitted Inference Console** (customer + Boundless PM / eng partner tool, not consumer chat): top = workload / customer stub; center = model recommendation + serving-tune packet; bottom = human gates + production impact strip. (Inferred from site thesis + JD; not a logged-in screenshot.)

### Visual style
- Colors (from public CSS / HTML): paper `#f9f8f5`, near-black text `#0f0f0e` / `#000`, cream wash `#fffff6`, purple accent `#ae93fc`, lime accent token `#9de500` (CSS), white cards `#ffffff`. Dark ink on warm paper is the default marketing mode.
- Typography: STKBureauSans (UI), STKBureauSerif (headings), DM Mono (code / model ids / metrics). Fall back to system sans + system serif + system mono if fonts unavailable.
- Density: medium. One customer workload open at a time. Recommendation chips + tune packet + clear gates. Not a dense GPU cluster spreadsheet.
- Components: rounded paper cards, status pills (Discovery / Fit ready / Tuned / In production / Needs evals), purple or near-black primary CTAs, citation / fit chips, large touch gates, production impact strip, mono for model ids and latency / cost numbers.
- Mode: light warm paper as default (matches public marketing). Optional small mono code strip for API snippet only, not the whole page.

### Tone of UI copy
- Inference-partner language: product-fitted inference, open-weight models, model selection, serving path, forward-deployed inference, quality threshold, context shape, latency target, traffic pattern, cost per task, p95, operate in production, Deploy tuned path, Retune under traffic.
- JD / careers words to reuse: own the roadmap, work backwards from customers, inference, RL/post-training, GPU compute, technical BD signal, 0 to 1, bias for action, rewrite how the world serves AI.
- Plain, evidence-led, builder-first (careers values: Results over effort; Lead with evidence; Say it plainly; Make it faster). No crypto-hype as the hero story. ZKC / staking stays out of this prototype.

### The exact screen where my proposed improvement would live
- An inferred **customer workload fit / deploy** screen inside Boundless product (or partner console): after Technical BD or inbound brings an AI-native team with production traffic, before Boundless locks model + serving config and before the customer goes live on the tuned path. This is the surface the Founding Product Manager seat is hired to own (JD: roadmap across inference and GPU compute; work backwards from customers; ship with eng and fold BD signal into product).

### Build instruction
- Match Boundless closely enough that the prototype feels like their product: warm paper `#f9f8f5`, ink text, purple `#ae93fc` accents, mono for model ids and metrics, rounded cards, fit chips, large Deploy / Retune / Need evals / Escalate CTAs.
- Use their terminology: inference partner, product-fitted, open-weight, model selection, serving path, forward-deployed, p95, cost per task, throughput, Deploy tuned path, Retune under traffic.
- Walk top-to-bottom (phone) or left-to-right (desktop): workload stub → model recommendation → serving-tune packet → human gate → production impact. Keep any eval / fit chips secondary to choose → tune → serve.
- Phone / mobile UX is mandatory: viewport meta, ~375px stack, no horizontal scroll, ~44px tap targets, readable type, no overlay clipping CTAs.
- Rejected pattern: do not rebuild a Rubric Lens / scorecard demo as the hero. Do not clone a generic LLM playground chat as the story. Do not build ZKC staking or Technical BD pipeline tooling. Do not sign in to the inference console.

## Acceptance criteria (must work when Ami demos the prototype in 90 seconds)
1. Load a synthetic AI-native workload → show customer stub, traffic / latency / cost targets, and at least 3 model-fit or serving chips (example: quality threshold, context shape, p95 target, or precision / batching / caching).
2. Human gate lets Ami pick Deploy tuned path, Retune under traffic, Need better eval set, or Escalate to forward-deployed eng. Primary CTAs are touch-friendly (~44px).
3. Deploy path updates status to In production (or Operating) and shows production impact improving (example: cost per task down and p95 within target, or throughput up on same GPU budget).
4. Optional Need evals / Retune path keeps status blocked or "retuning" with a clear reason and listed missing items or changed traffic knobs.
5. Hero is the Product-Fitted Inference Console (workload → choose → tune → deploy / operate), not a pass/fail spreadsheet or Rubric Lens strip.
6. Opens cleanly on a phone-width viewport (~375px) with viewport meta, vertical stack, no horizontal scroll, ~44px touch targets, readable type, and no overlays clipping content.
7. Walkthrough proves workload fit → model choose → serving tune → deploy gate → production impact in ~90 seconds.

## What the 90-second walkthrough proves about THEIR problem
Boundless sells product-fitted inference: choose the right model for the workload, tune the serving path to real traffic, and operate it so AI-native products get better quality, latency, throughput, and cost (https://boundless.network/ ; https://boundless.network/product/forward-deployed-inference ; careers thesis "Rewrite how the world serves AI."). The Founding Product Manager seat owns the roadmap across inference, RL/post-training, and GPU compute, working backwards from customers with eng and Technical BD (https://apply.workable.com/boundless-networks-inc-1/j/8F417E2E0D/). Walking through this prototype shows Ami can ship an operator surface that turns a vague "we need cheaper / better inference" into a cited model fit, a serving-tune packet, a clear deploy gate, and measurable production impact, which is the job, not a generic eval demo.

## TIMEBOX
If the prototype is not walkthrough-ready at 2 hours: LIGHT pitch fallback = open citation + human-gate craft from https://amiteshdwivedijhu-ship-it.github.io/ + 2 mapping lines:
1) "Your Founding Product seat owns the choose → tune → serve roadmap so inference is fitted to each AI-native product, not a generic endpoint."
2) "The 2-hour extension is a Boundless-styled Product-Fitted Inference Console: workload stub → model recommendation → serving-tune packet → Deploy / Retune / Need evals / Escalate → production impact."
Do not fall back to Rubric Lens or eval tables as the story. Do not pivot the Goal to Applied AI eng, Senior Infra eng, or Technical BD unless the Founding Product JD is gone.

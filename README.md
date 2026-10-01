# Boundless Product-Fitted Inference Console (synthetic prototype)

Working prototype for a Founding Product Manager application at Boundless
(boundless.network, inference partner for AI-native companies).

Unofficial synthetic prototype. Not affiliated with Boundless. No accounts,
no live inference, no real customer data.

## What it demonstrates

Product-fitted inference as the hero: workload fit → model choose → serving
tune → deploy / operate gate → production impact.

1. Workload stub: synthetic AI-native customer (Longpoint, sales-ops agent
   rollouts) with traffic pattern, context shape, quality threshold, latency
   and cost targets, baseline spend.
2. Model recommendation: DeepSeek V4 Flash (open-weight, from Boundless's
   public model catalog label) with thin fit chips. Fit chips are secondary;
   the hero is choose → tune → serve.
3. Serving-tune packet: FP8 precision, TP/DP parallelism, continuous
   batching, prefix caching, shadow-traffic routing.
4. Human gate: Deploy tuned path / Retune under traffic / Need better eval
   set / Escalate to forward-deployed eng.
5. Production impact: p95 latency, cost per task, throughput on the tuned
   path, with an OpenAI-compatible API strip.

Built mobile-first (375px), warm paper canvas #f9f8f5 with purple accent,
serif headings, mono model ids and metrics.

Run locally: open `index.html` in a browser.
Live: https://amiteshdwivedijhu-ship-it.github.io/boundless-inference-console/
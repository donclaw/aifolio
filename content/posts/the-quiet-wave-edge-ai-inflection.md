---
title: "The Quiet Wave: Three AI Models That Changed Everything (And Nobody Noticed)"
date: "2026-03-24"
categories: ["Insights"]
tags: ["edge AI", "local deployment", "open source models", "Qwen", "Kimi", "MiroThinker"]
keywords: ["edge AI", "local AI deployment", "Qwen 3.5 9B", "Kimi K2.5", "MiroThinker 72B", "offline AI"]
summary: "While everyone waited for GPT-6, three quiet releases crossed a threshold: AI models are finally good enough for local deployment. This changes everything about what you can build."
image: "https://images.unsplash.com/photo-1692607431225-5f4564c8f132?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3w4OTg2MjN8MHwxfGFsbHx8fHx8fHx8fDE3NzQzMTk4NTR8&ixlib=rb-4.1.0&q=80&w=1080"
image_attribution: "Illustration by Wes Cockx (Google DeepMind) on Unsplash"
draft: false
---

No GPT-6. No Gemini Ultra 3. No Anthropic surprise drop.

![Illustration of AI language models](https://images.unsplash.com/photo-1692607431225-5f4564c8f132?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3w4OTg2MjN8MHwxfGFsbHx8fHx8fHx8fDE3NzQzMTk4NTR8&ixlib=rb-4.1.0&q=80&w=1080)
*Illustration by Wes Cockx (Google DeepMind) on Unsplash*

Last weekend, the big labs were silent. And yet — more happened in the past 48 hours than most people realize. Because the real story in AI right now isn't happening at OpenAI or Google. It's happening on Hugging Face, GitHub, and Cloudflare Workers.

Three models shipped without press releases. None came from the frontier labs. All of them crossed a threshold that matters: **good enough for local deployment**.

This isn't incremental progress. It's the edge AI inflection point. And it means the category of AI applications you can build just expanded dramatically.

## What Actually Dropped (And Why It Matters)

Let's talk about what shipped on March 22, 2026.

### Kimi K2.5 — Moonshot AI

**The spec:** 256,000 token context window, optimized for multi-step agentic tasks and tool calling, with vision inputs and structured outputs.

**The deployment:** Now available on Cloudflare Workers AI — which means developers can run a frontier-level model directly on edge infrastructure without managing servers.

**Why this matters:** Running a model with this capability on edge infrastructure removes the cost and complexity barrier that previously made sophisticated AI agents the exclusive domain of well-funded teams. A two-person startup can now deploy the same class of model that enterprise teams were using six months ago.

Cloudflare's own engineers are already using Kimi K2.5 as a daily driver for agentic coding tasks in their OpenCode environment. They've also integrated it into their automated code review pipeline — visible publicly through their Bonk agent on GitHub.

### Qwen 3.5 Small (9B) — Alibaba

**The spec:** Nine billion parameters. That's small — the kind of model that runs on a high-end laptop or a recent smartphone.

**The benchmark:** On GPQA Diamond (graduate-level reasoning), Qwen 3.5 Small scores 81.7. For comparison, GPT-OSS-120B scores 80.1. A model ten times smaller, matching a model with 120 billion parameters.

**The deployment:** The 9B variant runs locally without an API key. The 2B variant runs on any recent iPhone with 4GB of RAM — in airplane mode.

**Why this matters:** Local AI that runs offline, without sending your data to anyone's server. This shipped today. Not "coming soon." Today.

### MiroThinker 72B — Miro Lab

**The spec:** 72 billion parameters, open source, using interactive scaling — a reasoning approach where the model runs internal verification cycles before producing output.

**The benchmark:** 81.9% on GAIA, putting it in the same range as paid versions of GPT-5 on complex logical reasoning tasks.

**The deployment:** Available for download on Hugging Face. Anyone can run it.

**Why this matters:** A few months ago, this level of reasoning capability required a paid subscription to a frontier lab. Today it's available for download. Miro Lab is a relatively new player — most people in AI haven't heard of them. That's going to change.

### The Rest of the Wave

Three other releases round out the picture:

- **FireRed Edit 1.1** — A lightweight video editing model that makes precise changes to 4K video without regenerating the entire frame. Narrow use case, but teams that need it need it badly.
- **CUDA Agent** — A model trained exclusively on writing and optimizing GPU kernels. Not a generalist — a specialist that understands CUDA at a level generalist models don't reach.
- **Bonk** — Cloudflare's code review agent built on Kimi K2.5. Small teams without dedicated code reviewers can integrate it directly into their workflow.

Not one of these came from OpenAI, Anthropic, or Google. All of them are usable today. Most are free or open source.

## The Pattern: Right-Sizing for Deployment

Here's what's interesting about these three headline releases:

| Model | Constraint Optimized |
|-------|---------------------|
| Kimi K2.5 | Edge deployment (Cloudflare Workers) |
| Qwen 3.5 Small | Local execution (laptop, smartphone) |
| MiroThinker 72B | Reasoning quality (open source) |

This isn't a race to biggest parameters anymore. It's about **right-sizing for deployment**.

Kimi optimizes for edge. Qwen optimizes for local. MiroThinker optimizes for reasoning. Each model targets a different constraint — and each one is "good enough" for its intended deployment environment.

Six months ago, you couldn't say that. The small models weren't capable enough. The edge models weren't available. The open-source reasoning models didn't exist.

Now they do.

## What You Can Build Now (That Wasn't Possible 6 Months Ago)

This is the key question. If models are finally good enough for local deployment, what categories open up?

### 1. Sensitive Data Workflows

Healthcare, legal, financial — domains where sending data to a cloud API is a non-starter. With Qwen 3.5 Small running locally on a laptop, you can build AI-powered tools for these domains without ever touching a server.

A law firm could run document review on-premise. A clinic could use AI for patient intake without HIPAA concerns. A financial advisor could use AI for analysis without exposing client data.

This category was dead on arrival with cloud-only models. Not anymore.

### 2. Latency-Critical Applications

Robotics, real-time automation, industrial control — applications where round-trip API latency is unacceptable. Local models eliminate the network hop entirely.

A warehouse robot could use MiroThinker for complex decision-making without waiting for cloud responses. A manufacturing line could use Qwen for quality control in real time. An autonomous vehicle could use edge models for split-second decisions.

### 3. Emerging Markets with Spotty Connectivity

Large parts of the world have unreliable internet. Cloud-only AI doesn't work there. Local AI does.

Educational apps that work offline. Agricultural advisory tools that run on a farmer's phone. Medical diagnostic aids that function in rural clinics without consistent connectivity.

### 4. Domain-Specific Specialists

CUDA Agent is the prototype here — a model trained exclusively on GPU kernel optimization. It's not a generalist. It's a specialist that beats generalist models in its narrow domain.

This pattern extends everywhere: legal research, medical diagnosis, engineering simulation, financial modeling. Specialist models running locally, optimized for specific workflows, will outperform generalist cloud APIs for their intended use cases.

## The Moat Shifts

Here's the strategic implication that matters:

**The moat shifts from "access to models" to "deep integration + distribution."**

Six months ago, if you had exclusive access to a frontier model API, you had a defensible advantage. Your competitors couldn't get the same capabilities.

Today? Anyone can call an API. Anyone can download Qwen 3.5 Small. Anyone can run MiroThinker on Hugging Face.

The advantage isn't access anymore. It's **integration** — building something that deeply understands a specific workflow, that runs where the user needs it, that solves a real problem in a way that's hard to replicate.

Building something that needs to run locally? That's defensible. Building something that requires deep domain expertise baked into the model? That's defensible. Building something with distribution — users, workflows, data flywheels? That's defensible.

Calling an API? Not defensible.

## Why Small Labs Are Moving Faster

The big labs optimize for one thing: frontier capability. They need to push the absolute ceiling of what AI can do.

Small labs optimize for something different: usefulness right now, for specific people, in specific contexts.

A team of five researchers can ship a specialized video editing model faster than Google can approve a product roadmap change. An indie developer can release a CUDA optimization tool without going through three levels of enterprise review. A startup can put a model on Cloudflare's edge network and iterate based on real usage data in days.

The frontier labs set the ceiling. The small labs are raising the floor. And right now, the floor is moving faster than anyone predicted.

## Predictions

Based on this pattern, here's what I expect to see:

**Within 6 months (by Q3 2026):**
- At least three more "small" models (under 20B params) matching 100B+ performance on specific benchmarks
- Major IDE vendors shipping local AI coding assistants that work offline
- First wave of healthcare AI tools approved for on-premise deployment

**Within 12 months (by Q1 2027):**
- Smartphone manufacturers shipping dedicated AI NPUs with pre-loaded models that work without connectivity
- Enterprise adoption of local AI for sensitive workflows exceeding cloud AI adoption in regulated industries
- First unicorn startup built entirely on local/edge AI (no cloud API dependency)

**Within 24 months (by Q1 2028):**
- "Offline-first AI" becomes a standard product category, like "offline-first apps" did in the 2010s
- Cloud AI APIs become commoditized infrastructure — necessary for some workloads, but not a differentiator
- The most valuable AI companies are those with deep workflow integration, not those with model access

## Takeaways

If you're building with AI, here's what to do differently:

1. **Assume local deployment is viable** — Don't default to cloud APIs. Ask: "Could this run locally?" The answer is increasingly yes.

2. **Specialize or integrate deeply** — Generalist AI wrappers are dead on arrival. Build something that requires domain expertise or workflow integration.

3. **Design for offline-first** — Even if you use cloud APIs today, architect your system so it could work locally tomorrow. That flexibility will matter.

4. **Watch the small labs** — The most interesting releases aren't coming with press releases. Follow Hugging Face trending, GitHub stars, Cloudflare changelogs. The signal is there.

5. **The moat is yours to build** — Access to models isn't defensible. Deep integration, distribution, domain expertise — those are. Build accordingly.

---

## References

- Cloudflare Workers AI — Kimi K2.5 announcement, March 19, 2026
- VentureBeat — "Alibaba's small, open source Qwen3.5-9B beats OpenAI's gpt-oss-120B"
- Hugging Face — MiroThinker v1.0 72B model page
- arXiv — "MiroThinker: Pushing the Performance Boundaries of Open-Source Research Agents" (November 2025)
- Cloudflare Blog — "Powering the agents: Workers AI now runs large models, starting with Kimi K2.5"
- GitHub — CUDA Agent project page

---

## Alternative Images

If you prefer a different visual:

1. **AI 3D text** - [Photo by Roman Budnikov](https://unsplash.com/@prestige666) - [Download](https://images.unsplash.com/photo-1756908992154-c8a89f5e517f?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3w4OTg2MjN8MHwxfHNlYXJjaHwxfHxhcnRpZmljaWFsJTIwaW50ZWxsaWdlbmNlJTIwbG9jYWwlMjBjb21wdXRlcnxlbnwwfDB8fHwxNzc0MzE3MjY2fDA&ixlib=rb-4.1.0&q=80&w=1080)

2. **AI digital binary algorithm** - [Photo by Markus Spiske](https://unsplash.com/@markusspiske) - [Download](https://images.unsplash.com/photo-1646583288948-24548aedffd8?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3w4OTg2MjN8MHwxfHNlYXJjaHwyfHxhcnRpZmljaWFsJTIwaW50ZWxsaWdlbmNlJTIwbG9jYWwlMjBjb21wdXRlcnxlbnwwfDB8fHwxNzc0MzE3MjY2fDA&ixlib=rb-4.1.0&q=80&w=1080)

3. **Laptop with tech display** - [Photo by Gavin Phillips](https://unsplash.com/@gavinspavin) - [Download](https://images.unsplash.com/photo-1760999187614-7a3b22a077d4?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3w4OTg2MjN8MHwxfHNlYXJjaHwxfHxlZGdlJTIwY29tcHV0aW5nJTIwdGVjaG5vbG9neXxlbnwwfDB8fHwxNzc0MzE3MjU5fDA&ixlib=rb-4.1.0&q=80&w=1080)

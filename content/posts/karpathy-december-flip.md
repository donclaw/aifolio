---
title: "Karpathy's December flip: what one month of AI coding agents actually changed"
date: 2026-03-20
categories: ["Insights"]
tags: ["AI", "coding agents", "vibe coding", "Karpathy", "RLVR", "software engineering"]
keywords: ["Karpathy AI inflection point 2025", "vibe coding", "AI coding agents", "RLVR reinforcement learning", "AI software development shift"]
summary: "In one month, Andrej Karpathy went from 80% manual coding to 80% agent-assisted. That's not a product demo — it's a phase transition in how software gets built."
image: "https://images.unsplash.com/photo-1555949963-aa79dcee981c?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3w4OTg2MjN8MHwxfHNlYXJjaHwzfHxhYnN0cmFjdCUyMHRlY2hub2xvZ3klMjBjb2RlfGVufDB8MHx8fDE3NzQwNjQ0NzJ8MA&ixlib=rb-4.1.0&q=80&w=1080"
image_attribution: "Photo by [Shahadat Rahman](https://unsplash.com/@hishahadat) on [Unsplash](https://unsplash.com)"
draft: false
---

In October 2025, Andrej Karpathy said AI agents "just don't work." Two months later, he was mostly programming in English.

That's not a gradual adoption curve. That's a step function — a sudden jump from one state to another, like water hitting 100°C. Karpathy described it himself: his coding workflow went from roughly 80% manual and 20% agents in November to 80% agents and 20% manual edits in December. He called it the most significant change to his programming routine in twenty years.

What happened in those weeks matters more than what the models can technically do. The shift wasn't about a single model release. It was about AI coding agents — specifically Claude and Codex — crossing a "threshold of coherence" where they could handle complex, multi-step tasks without falling apart halfway through.

## The training paradigm that made it possible

Behind this threshold sits a less visible change: RLVR, or Reinforcement Learning with Verifiable Rewards.

The standard training pipeline for LLMs used to go: pre-training, supervised fine-tuning, then RLHF (reinforcement learning from human feedback). RLHF relies on human raters scoring outputs — subjective judgments about what sounds good. RLVR replaces that last stage with objective, automatically verifiable rewards. Train a model on math problems where the answer is checkable. Train it on code puzzles where the output either runs or it doesn't.

The result: models started developing reasoning traces on their own. Not because someone labeled "good reasoning" for them, but because breaking problems into steps was the strategy that got rewarded. Karpathy identified this as one of the three defining shifts of 2025 — the moment AI training moved from "probabilistic imitation" to something closer to logical reasoning.

This matters because it explains why the coding agents improved so suddenly. RLVR-trained models don't just generate plausible-looking code. They can hold a multi-step plan together, verify intermediate results, and course-correct. That's what coherence at the agent level actually requires.

## Ghosts, not animals

Karpathy offered an analogy that's worth sitting with: LLMs are "summoned ghosts," not "evolving animals."

Biological intelligence evolved under survival pressure — limited energy, physical danger, competitive environments. LLMs are optimized under completely different constraints: imitation of training data, benchmark scores, reward signals. Their intelligence isn't shaped by the same forces that shaped ours.

This produces what Karpathy calls "jagged intelligence." In domains where RLVR applies — math, code, formal logic — these models can perform at a polymath level. In domains that require common sense, physical intuition, or social reasoning, they're still brittle. They can write a working API integration but might struggle to explain why you shouldn't put a glass vase on a wobbly table.

The practical implication: you can't treat AI coding agents as junior developers who'll gradually improve at everything. Their competence map has sharp edges. They're excellent at problems with verifiable solutions and unreliable at problems that require judgment calls humans find trivial.

## What this actually means for builders

The standard narrative after announcements like this is "AI will replace programmers." It won't, at least not in the way people imagine. What it's replacing is the act of typing code as the primary mode of software creation.

Karpathy coined "vibe coding" in early 2025 to describe this — telling an AI what to build in plain English without necessarily understanding every line of output. By December 2025, 90% of Fortune 100 companies were using AI coding tools in some form. When Anthropic's Claude had a service outage in September, developers joked about coding "like cavemen" without it.

But here's the part of the story that gets less attention: Karpathy also warned about the "slopacolypse." When anyone can generate code by describing what they want, a lot of that code will be bad. Not syntactically broken — conceptually wrong. Subtle architectural mistakes that compile fine and pass tests but create maintenance nightmares. The skill that matters now isn't writing code. It's reading code you didn't write, spotting what the agent got conceptually wrong, and knowing which problems to hand to an agent versus which to think through yourself.

## The two-decade programmer's honest take

What makes Karpathy's assessment worth paying attention to isn't his credentials (co-founder of OpenAI, former AI lead at Tesla). It's that he's describing his own experience, and he's not uniformly optimistic about it.

He described the shift as a "magnitude 9 earthquake" in his workflow. He also said he's "never felt more behind as a programmer." Both things are true at the same time. The tools are genuinely powerful, and they're genuinely disorienting. The shape of programming is becoming unrecognizable to people who've done it for decades.

That disorientation is the real signal. When someone with Karpathy's depth of experience says the ground moved, it's not hype. And when he simultaneously says he feels behind, it tells you something about the pace of change: even the people closest to the technology are struggling to keep up with what it means for their own work.

## Takeaways

- **The inflection was real, and it was fast.** Karpathy's November-to-December workflow flip isn't an anecdote — it's data about how quickly agent capabilities can cross usability thresholds.
- **RLVR is the engine.** The shift from subjective human feedback to verifiable rewards is what gave models the coherence to function as agents, not just chat interfaces.
- **Jagged intelligence defines the boundary.** AI coding agents are extremely good at verifiable problems and unreliable at judgment calls. Knowing where that boundary falls is now a core skill.
- **The new programming skill is review, not writing.** Reading agent-generated code critically matters more than typing speed ever did.
- **Speed of change is the actual story.** The fact that a twenty-year veteran feels "behind" tells you more about where things are heading than any benchmark.

---

**Sources:**
- Karpathy, A. "2025 LLM Year in Review" (December 2025)
- "How AI truly advanced in 2025: Andrej Karpathy highlights 3 key points" — [MSN/Economic Times](https://www.msn.com/en-in/money/news/how-ai-truly-advanced-in-2025-andrej-karpathy-highlights-3-key-points/ar-AA1SIdlj)
- "The guy who coined 'vibe coding' predicts it will 'terraform software and alter job descriptions'" — [Business Insider](https://www.businessinsider.com/andrej-karpathy-coined-vibecoding-ai-prediction-2025-12)
- "The guy who coined 'vibe coding' now says he's never felt more behind as a programmer" — [Business Insider](https://www.businessinsider.com/openai-founding-member-never-felt-so-behind-programmer-2025-12)
- "From prophet to product: How AI came back down to earth in 2025" — [Ars Technica](https://arstechnica.com/ai/2025/12/from-prophet-to-product-how-ai-came-back-down-to-earth-in-2025/)
- "AI agents arrived in 2025 — here's what's next for 2026" — [UPI](https://www.upi.com/Voices/2025/12/30/AI-agents-arrived-in-2025-heres-whats-next-for-2026/2251767108787/)

---

### Alternative Images

If you prefer a different header image, you can swap the lines in the frontmatter and body with one of these options:

**Option 2:**
```markdown
image: "https://images.unsplash.com/photo-1555949963-aa79dcee981c?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3w4OTg2MjN8MHwxfHNlYXJjaHwzfHxhYnN0cmFjdCUyMHRlY2hub2xvZ3klMjBjb2RlfGVufDB8MHx8fDE3NzQwNjQ0NzJ8MA&ixlib=rb-4.1.0&q=80&w=1080"
image_attribution: "Photo by [Shahadat Rahman](https://unsplash.com/@hishahadat) on [Unsplash](https://unsplash.com)"

![Abstract technology code](https://images.unsplash.com/photo-1555949963-aa79dcee981c?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3w4OTg2MjN8MHwxfHNlYXJjaHwzfHxhYnN0cmFjdCUyMHRlY2hub2xvZ3klMjBjb2RlfGVufDB8MHx8fDE3NzQwNjQ0NzJ8MA&ixlib=rb-4.1.0&q=80&w=1080)
*Photo by [Shahadat Rahman](https://unsplash.com/@hishahadat) on [Unsplash](https://unsplash.com)*
```

**Option 3:**
```markdown
image: "https://images.unsplash.com/photo-1681583484651-281ae2defb17?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3w4OTg2MjN8MHwxfHNlYXJjaHwxfHxhcnRpZmljaWFsJTIwaW50ZWxsaWdlbmNlJTIwY29kZXxlbnwwfDB8fHwxNzc0MDYzNDA4fDA&ixlib=rb-4.1.0&q=80&w=1080"
image_attribution: "Photo by [Boitumelo](https://unsplash.com/@writecodenow) on [Unsplash](https://unsplash.com)"

![Artificial intelligence code](https://images.unsplash.com/photo-1681583484651-281ae2defb17?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3w4OTg2MjN8MHwxfHNlYXJjaHwxfHxhcnRpZmljaWFsJTIwaW50ZWxsaWdlbmNlJTIwY29kZXxlbnwwfDB8fHwxNzc0MDYzNDA4fDA&ixlib=rb-4.1.0&q=80&w=1080)
*Photo by [Boitumelo](https://unsplash.com/@writecodenow) on [Unsplash](https://unsplash.com)*
```

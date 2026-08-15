---
layout: default
title: "Horizon Summary: 2026-08-15 (EN)"
date: 2026-08-15
lang: en
---

> From 24 items, 3 important content pieces were selected

---

1. [AI Has Vastly Larger Working Memory but Still Lacks Mathematicians&\#x27; Common Sense](#item-1) ⭐️ 8.0/10
2. [Auto-Research with Codex Achieves 232x Faster Kernel](#item-2) ⭐️ 8.0/10
3. [BDH-CQ: Recurrent Latent Reasoning Achieves Cheap ARC-AGI-1 Gains](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [AI Has Vastly Larger Working Memory but Still Lacks Mathematicians&\#x27; Common Sense](https://davidepiffer.com/p/ai-isnt-outthinking-mathematicians) ⭐️ 8.0/10

Davide Piffer&\#x27;s essay argues that while AI systems \(especially LLMs\) possess a vastly larger working memory capacity than the human brain, they still fail to outthink mathematicians because they lack qualitative reasoning and common sense. The argument challenges the assumption that raw memory scale is the key to intelligence, reframing AI&\#x27;s strengths and limitations for researchers. It also raises practical concerns for software engineering, where maintainable code is designed around human working-memory limits. The article positions AI&\#x27;s huge context window as an advantage but argues it does not compensate for missing reasoning quality. Community commenters tie this to code maintainability and note that LLMs often generate more verbose code, which can cause long-term maintenance issues.

hackernews · rzk · Aug 15, 18:13 · [Discussion](https://news.ycombinator.com/item?id=49312845)

**Background**: Working memory is the limited cognitive capacity humans use to temporarily hold and manipulate information, often cited as around seven items. AI systems, especially LLMs, can process extremely large context windows, giving them a much larger working-memory-like store. However, qualitative reasoning—the ability to reason about space, time, and quantity with incomplete information—remains a known weakness of AI systems.

<details><summary>References</summary>
<ul>
<li><a href="https://www.illumio.com/blog/the-limits-of-working-memory-human-brains-vs-ai-models">The Limits of Working Memory: Human Brains vs. AI Models</a></li>
<li><a href="https://arxiv.org/html/2504.15965v2">From Human Memory to AI Memory: A Survey on Memory Mechanisms ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Qualitative_reasoning">Qualitative reasoning - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Comments largely agree that intelligence involves more than memory, with one user speculating that &\#x27;intelligence&\#x27; is often out-remembering others, while another argues for qualitative compression over raw capacity. There is also discussion of AI&\#x27;s ability to publish and reuse negative results, which human mathematicians rarely do, and concerns about future code maintainability.

**Tags**: `#AI`, `#working memory`, `#human cognition`, `#LLMs`, `#software engineering`

---

<a id="item-2"></a>
## [Auto-Research with Codex Achieves 232x Faster Kernel](https://sankalp.bearblog.dev/autoresearch/) ⭐️ 8.0/10

The author used OpenAI Codex to autonomously run a benchmark-profile-verify-research-improve loop on a kernel, achieving a 232x speedup. This demonstrates AI-driven performance engineering on low-level GPU code. This result shows that AI agents can perform sophisticated performance engineering, potentially changing how developers approach low-level optimization. It also sparks important debate about whether such AI-generated optimizations generalize beyond the specific benchmark or input shapes. The 232x speedup came from an autonomous loop that repeatedly benchmarked, profiled, verified, researched, and improved the kernel. Community commenters noted that similarly AI-optimized competition solutions often break on out-of-distribution inputs, so robustness remains a significant concern.

hackernews · tosh · Aug 15, 11:00 · [Discussion](https://news.ycombinator.com/item?id=49309549)

**Background**: A CUDA kernel is a function that runs on a GPU and is executed in parallel by thousands to millions of threads, organized into blocks and a grid. OpenAI Codex is an AI coding agent that can turn plain language into working code and automate tasks such as pull requests, refactors, and code reviews. Deep learning workloads rely heavily on GPU kernels, making them a natural target for AI-assisted optimization.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/codex/">Codex in ChatGPT | AI Coding Agents for Software... | OpenAI</a></li>
<li><a href="https://llm-stats.com/blog/research/what-is-a-cuda-kernel">What Is a CUDA Kernel ? A Visual Explainer | LLM Stats</a></li>

</ul>
</details>

**Discussion**: Commenters shared related experiments: one used DeepSeek to optimize a video codec with a verifier, and another noted that 8 of the top 10 AI-optimized competition solutions broke on out-of-distribution shapes. Some praised the long-form post as refreshingly human-written, while others speculated about why GPU kernels are so well represented in model training data.

**Tags**: `#AI-assisted development`, `#kernel optimization`, `#CUDA`, `#performance engineering`, `#deep learning`

---

<a id="item-3"></a>
## [BDH-CQ: Recurrent Latent Reasoning Achieves Cheap ARC-AGI-1 Gains](https://www.reddit.com/r/MachineLearning/comments/1vov5r5/bdhcq_incontext_learning_with_recurrent_latent/) ⭐️ 8.0/10

Researchers at Pathway introduced BDH-CQ, a 150M-parameter reasoning model that combines in-context learning with recurrent latent reasoning. It scores 29.5% pass@2 on ARC-AGI-1 at an estimated $0.00070 per task, reportedly breaking the previously reported cost-accuracy Pareto frontier. This is significant because it shows a small model can outperform larger, more expensive systems through architectural innovation rather than sheer scale. It also challenges the assumption that explicit chain-of-thought token generation is necessary for strong reasoning performance. The model does not decode intermediate reasoning steps into language; instead, it iterates in a high-dimensional latent space. No task identifiers or evaluation-task demonstrations are used in training, no parameters are updated at inference time, and the architecture scales naturally to large sizes via tensor sharding patterns inherited from BDH.

reddit · r/MachineLearning · /u/moschles · Aug 15, 06:18

**Background**: ARC-AGI-1 is a benchmark designed to measure skill-acquisition capability, the core of intelligence, rather than performance on predefined tasks. BDH-CQ builds on Dragon Hatchling \(BDH\), a post-Transformer recurrent architecture in which neuron-like units communicate through low-rank interactions and maintain context in an evolving associative state. BDH-CQ extends this with in-context learning: demonstrations update recurrent memory at inference time, and the query is then solved through iterative continuous computation.

<details><summary>References</summary>
<ul>
<li><a href="https://pathway.com/blog/pathway-150m-model-breaks-arc-agi-1-cost-efficiency-frontier">Pathway’s 150M-Parameter Model Breaks the...</a></li>
<li><a href="https://arxiv.org/html/2608.09888">BDH - CQ : In-Context Learning with Recurrent Latent Reasoning</a></li>
<li><a href="https://arcprize.org/arc-agi/1">ARC-AGI-1</a></li>

</ul>
</details>

**Tags**: `#in-context learning`, `#recurrent memory`, `#latent reasoning`, `#ARC-AGI`, `#efficient ML`

---
---
layout: default
title: "Horizon Summary: 2026-08-12 (EN)"
date: 2026-08-12
lang: en
---

> From 36 items, 11 important content pieces were selected

---

1. [Qwen Releases Qwen3.8-2.4T-A95B, a Massive Open-Weight MoE Model](#item-1) ⭐️ 9.0/10
2. [DeepSeek Releases V4 Pro 0813, Winning Raves for Low-Cost Performance](#item-2) ⭐️ 8.0/10
3. [Tailscale Traces Database Corruption to 16-Year-Old SQLite WAL-Reset Bug](#item-3) ⭐️ 8.0/10
4. [xAI announces Grok 4.6, sparking debates on system prompts and benchmarks](#item-4) ⭐️ 8.0/10
5. [Why Tiny JPEGs Render Differently in Chrome](#item-5) ⭐️ 8.0/10
6. [uBlock Origin Gives Up Blocking Facebook Ads, Ceding to Anti-Adblock Tactics](#item-6) ⭐️ 8.0/10
7. [AI Is Removing the Middle Class of Software Engineering?](#item-7) ⭐️ 8.0/10
8. [Engineer Warns AI-Assisted Coding Creates Unmaintainable Systems](#item-8) ⭐️ 8.0/10
9. [Adam&\#x27;s Per-Coordinate Updates Break Rotation Invariance, Wiping Out Low-Rank Bias](#item-9) ⭐️ 8.0/10
10. [LTX Releases Open-Source Video Model LTX-2.5 Running on a Single RTX 5090](#item-10) ⭐️ 8.0/10
11. [WeChat Releases WeLM, Resource-Efficient LLM Family with MoE](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Qwen Releases Qwen3.8-2.4T-A95B, a Massive Open-Weight MoE Model](https://huggingface.co/Qwen/Qwen3.8-2.4T-A95B) ⭐️ 9.0/10

Qwen has released Qwen3.8-2.4T-A95B, an open-weight Mixture-of-Experts \(MoE\) model with 2.4 trillion total parameters and 95 billion active parameters. The release includes BF16 and FP8 checkpoints on Hugging Face, with a native context length of 262,144 tokens expandable to 1,010,000 tokens, and claims competitive performance against models like Kimi k3. This is a major release in the open-weight AI ecosystem, as it makes a frontier-scale model available for fine-tuning and self-hosting. The enormous total parameter count and the associated quantization and serving trade-offs are likely to accelerate progress in model compression and efficient inference. The model has 2.4T total parameters with 95B active per token, but initial releases are only in BF16 and FP8, without a QAT-based 4-bit quantized version; Unsloth reports a 1-bit quant at roughly 397GB. The open-weight version lacks some features of the official Qwen3.8-Max, such as vision input and a default 1M context, and its license allows free use for internal purposes or under $50M annual revenue, with restrictions above that threshold.

hackernews · Philpax · Aug 12, 15:01 · [Discussion](https://news.ycombinator.com/item?id=49273478)

**Background**: Mixture of Experts \(MoE\) is a machine learning architecture that divides a model into specialized sub-networks and routes each input to only a few experts, allowing models to scale to trillions of parameters without a proportional increase in compute per token. Quantization compresses model weights to lower-precision formats such as FP8 or 4-bit, reducing memory footprint and improving inference speed, as supported by frameworks like vLLM. Serving trillion-parameter MoE models is memory-intensive, especially because the KV cache grows with context length, so quantization and efficient batching are critical for practical deployment.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://www.baseten.co/blog/33-faster-llm-inference-with-fp8-quantization/">33% faster LLM inference with FP8 quantization</a></li>
<li><a href="https://developer.nvidia.com/blog/mastering-llm-techniques-inference-optimization/">Mastering LLM Techniques: Inference Optimization | NVIDIA Technical Blog</a></li>

</ul>
</details>

**Discussion**: Hacker News discussion centers on the practical difficulties of serving and quantizing the model, with commenters noting that the BF16/FP8-only release makes it harder to run than rivals like Kimi k3, and that a high-quality 4-bit quantization will require significant compute and calibration data. Some are excited that Unsloth&\#x27;s 1-bit quant could bring Opus-level performance to commodity hardware, while others lament the open-weight version&\#x27;s missing features like vision input and full 1M context. A few comments joke about running such a massive model on low-end devices like an Intel N100.

**Tags**: `#AI`, `#LLM`, `#Qwen`, `#model release`, `#open source`

---

<a id="item-2"></a>
## [DeepSeek Releases V4 Pro 0813, Winning Raves for Low-Cost Performance](https://openrouter.ai/deepseek/deepseek-v4-pro-0813) ⭐️ 8.0/10

DeepSeek has released DeepSeek V4 Pro 0813, the production version of its flagship model, ending a four-month preview period. Community tests on OpenRouter show it delivers strong code-development results at a fraction of the cost of rivals like Grok 4.6. This release could intensify price competition in the AI model market, as DeepSeek continues to offer cutting-edge performance at unusually low cost. Developers running heavy workloads may find a compelling alternative to pricier Western models, accelerating adoption of affordable AI APIs. The build designation is V4 Pro 0813, and it appeared on August 12, 2026 as the general-availability version after a preview period of nearly four months. In a head-to-head Codex CLI test, DeepSeek V4 Pro ran 12m02s and cost $0.12 but had a bug, while Grok 4.6 ran 3m18s, cost $1.41, and produced no bugs.

hackernews · explosion-s · Aug 12, 16:04 · [Discussion](https://news.ycombinator.com/item?id=49274600)

**Background**: DeepSeek is a Chinese AI company whose chatbot and open-weight models gained worldwide attention after the release of DeepSeek-R1 in January 2025, which briefly surpassed ChatGPT as the most downloaded free app on the U.S. iOS App Store. The company is known for energy-efficient training and open-source contributions, and it has positioned itself as a low-cost provider of high-performance AI. The V4 Pro model had been available in preview for about four months before this production release.

<details><summary>References</summary>
<ul>
<li><a href="https://www.unite.ai/deepseek-ships-v4-pro-as-its-flagship-model-leaves-preview/">DeepSeek Ships V4 Pro as Its Flagship Model Leaves Preview</a></li>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek_%28product%29">DeepSeek (product)</a></li>

</ul>
</details>

**Discussion**: Community reactions are largely positive, with users praising the low cost and strong capability for development tasks. One user&\#x27;s hands-on test found DeepSeek V4 Pro much cheaper but slower and buggier than Grok 4.6; another noted the model&\#x27;s ability to handle &\#x27;heavy development for peanuts.&\#x27; Some commenters also criticized the news link pointing to OpenRouter instead of official sources.

**Tags**: `#DeepSeek`, `#AI models`, `#LLM`, `#API`, `#benchmarks`

---

<a id="item-3"></a>
## [Tailscale Traces Database Corruption to 16-Year-Old SQLite WAL-Reset Bug](https://tailscale.com/blog/sqlite-wal-reset-bug) ⭐️ 8.0/10

Tailscale published a detailed post explaining that a data race in SQLite&\#x27;s write-ahead logging \(WAL\) subsystem, present since roughly 2010, corrupted its control-plane database. To isolate and fix the issue, Tailscale funded an open-source SQLite VFS shim and updated its driver to log when write transactions overlap with WAL resets. This matters because the bug could corrupt databases even under SQLite&\#x27;s recommended single-writer configuration, and it went unnoticed by the SQLite team for 16 years. The case also demonstrates how corporations can fund targeted open-source tooling that benefits the entire SQLite ecosystem. The race occurs when a write transaction collides with a WAL reset during checkpointing. SQLite fixed it in release 3.51.3, and the same analysis has prompted checks for related projects such as dqlite.

hackernews · ropbear · Aug 12, 14:22 · [Discussion](https://news.ycombinator.com/item?id=49272832)

**Background**: SQLite is an embedded database that can use write-ahead logging \(WAL\), where changes are appended to a separate WAL file before being checkpointed into the main database. After a checkpoint, SQLite may reset the WAL file for reuse, and the newly identified bug is a data race between that reset and a concurrent write. A VFS shim is a layer that intercepts SQLite&\#x27;s file operations; Tailscale&\#x27;s funded shim helped reproduce and isolate the corruption by adding instrumentation around reads and writes.

<details><summary>References</summary>
<ul>
<li><a href="https://tailscale.com/blog/sqlite-wal-reset-bug">How Tailscale helped find the SQLite WAL-Reset bug</a></li>
<li><a href="https://antithesis.com/blog/2026/wal-reset-bug/">Breaking the WAL | Antithesis</a></li>
<li><a href="https://ubuntu.com/blog/hunting-a-16-year-old-sqlite-bug-with-tla-is-dqlite-affected">Hunting a 16-year-old SQLite bug with TLA+: is dqlite affected? | Ubuntu</a></li>

</ul>
</details>

**Discussion**: Comments were largely positive, praising the write-up and Tailscale&\#x27;s decision to fund SQLite support and a dedicated debugging tool. Several readers noted that the race requires multiple connections despite the single-writer database design, while others appreciated the broader lesson that even heavily tested software can hide subtle bugs.

**Tags**: `#sqlite`, `#database`, `#debugging`, `#tailscale`, `#open-source`

---

<a id="item-4"></a>
## [xAI announces Grok 4.6, sparking debates on system prompts and benchmarks](https://x.ai/news/grok-4-6) ⭐️ 8.0/10

xAI has released Grok 4.6, the newest version of its large language model family. The announcement has quickly drawn community debate over the model&\#x27;s default system prompt, benchmark claims, and competitive positioning. Grok 4.6 strengthens xAI&\#x27;s position in the frontier AI race, giving developers another competitive option in price, speed, and agent behavior. The controversy around benchmark methods and system-prompt handling also highlights growing scrutiny of how AI labs measure and present model capabilities. Developers report that xAI&\#x27;s API injects a default system prompt, and a line telling the model not to mention the guidelines can override user instructions. Commenters also note Grok 4.6 is priced lower than some rivals and offers generous usage limits within Cursor subscriptions.

hackernews · iLuddite · Aug 12, 15:32 · [Discussion](https://news.ycombinator.com/item?id=49274027)

**Background**: Grok is a series of large language models developed by xAI, launched in November 2023 by Elon Musk and integrated with X and Tesla products. System prompts are the initial instructions that define an LLM&\#x27;s behavior for a session. AI model benchmarks are commonly based on static task sets, and some researchers argue that labs can artificially tune performance or overfit to leaderboards.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Grok_%28chatbot%29">Grok (chatbot) - Wikipedia</a></li>
<li><a href="https://www.techtarget.com/whatis/feature/Grok-3-model-explained-Everything-you-need-to-know">Grok 3 model explained: Everything you need to know - TechTarget</a></li>
<li><a href="https://www.secondtalent.com/resources/every-grok-ai-model-explained-compared/">Every Grok AI Model Explained and Compared (Aug, 2026)</a></li>

</ul>
</details>

**Discussion**: Community reactions are mixed. Some users praise Grok 4.x for being fast, concise, and pleasant to use, while others question how many labs suddenly achieved &\#x27;Fable-level&\#x27; performance within two months, suspecting distillation or benchmark hacking. The default system prompt behavior is a particular irritant, as it can block legitimate discussion of model guidelines.

**Tags**: `#AI`, `#Grok`, `#xAI`, `#language models`, `#API`

---

<a id="item-5"></a>
## [Why Tiny JPEGs Render Differently in Chrome](https://guillaumetech.github.io/posts/jpg-scaling-chrome/) ⭐️ 8.0/10

A technical article shows that Chrome&\#x27;s scaled JPEG decompression — decoding a smaller image directly from compressed data — makes tiny JPEGs render differently than in other browsers. The author draws attention to this subtle rendering divergence and advises web developers not to use JPEG for small icons. This matters because browser-specific optimizations can alter the rendering of small images, causing visual inconsistencies across browsers and platforms. Developers who care about pixel-accurate, cross-browser UI need to be aware of these hidden differences when choosing image formats and sizes. Scaled JPEG decompression produces a lower-resolution output directly from the compressed stream, rather than decoding the full image and then resizing it. The article recommends using appropriately sized images and lossless formats like PNG for icons; Firefox is also working on similar low-scale decompression support \(Bugzilla 2033250\).

hackernews · gutechh · Aug 12, 14:00 · [Discussion](https://news.ycombinator.com/item?id=49272549)

**Background**: JPEG compression discards information by converting to YCbCr color space, downsampling chroma, and applying a discrete cosine transform \(DCT\) to 8x8 blocks, then quantizing the results. Scaled JPEG decompression lets a decoder produce a smaller image directly from a subset of the compressed data, reducing CPU and memory use. Since different browsers implement this optimization differently, the same JPEG can look visibly different when displayed at a small size.

<details><summary>References</summary>
<ul>
<li><a href="https://cgjennings.ca/articles/jpeg-compression/">How JPEG works - Home (Christopher G. Jennings)</a></li>
<li><a href="https://bitmiracle.github.io/libjpeg.net/help/articles/KB/decompression-details.html">1. Allocate and initialize a JPEG decompression object</a></li>

</ul>
</details>

**Discussion**: Commenters note that PNGs suffer from a similar issue in Electron, where a Chrome-based upgrade caused icon corruption so severe that a product team had to delay the update. One developer points out that Chrome and Firefox use different scaling algorithms, with Firefox looking sharper but with slight ringing, while another mentions CSS image-rendering as a possible workaround. There is also agreement that using an appropriately sized image is more important than switching formats.

**Tags**: `#JPEG`, `#Chrome`, `#image-scaling`, `#web-development`, `#browsers`

---

<a id="item-6"></a>
## [uBlock Origin Gives Up Blocking Facebook Ads, Ceding to Anti-Adblock Tactics](https://digitalescapetools.com/2026/08/ublock-origin-stops-chasing-facebook-ads.html) ⭐️ 8.0/10

uBlock Origin has ended its attempts to filter ads on Facebook, reportedly because Facebook&\#x27;s anti-adblocking measures have made the effort unsustainable. The decision was shared in a Reddit post and highlighted by Neowin. Facebook is one of the most visited sites on the web, so this is a significant retreat in the ad-blocking arms race and a blow to users who want control over their news feed. It also raises the risk that other major platforms, especially YouTube, will push harder against ad blockers knowing that uBlock Origin may eventually give up. Facebook ads are served as &\#x27;Sponsored&\#x27; cards inside the News Feed and are generated through techniques that make them hard to distinguish from ordinary posts. According to the report and community discussion, uBlock Origin chose to stop chasing these ads rather than continue an endless maintenance battle.

hackernews · Markoff · Aug 12, 11:28 · [Discussion](https://news.ycombinator.com/item?id=49270726)

**Background**: Ad blockers rely on filter lists of known ad domains and page elements to hide or block advertisements. Facebook has repeatedly tried to defeat these tools; in 2016 it briefly made its ads unblockable, and ad-blocking tools responded with workarounds such as grey-out overlays for &\#x27;Sponsored&\#x27; posts. More recently, browser changes such as Manifest V3 have limited the power of blocking extensions, making this kind of cat-and-mouse game harder for ad blockers to sustain.

<details><summary>References</summary>
<ul>
<li><a href="https://www.dylanpaulus.com/posts/how-fb-avoids-adblockers">How Facebook Avoids Ad Blockers | Dylan Paulus</a></li>
<li><a href="https://www.technologyreview.com/2016/08/15/245145/facebook-cant-win-against-ad-blockers-and-heres-the-proof/">Facebook Can’t Win Against Ad Blockers ... | MIT Technology Review</a></li>
<li><a href="https://support.adblockultimate.net/en/articles/9240458-anti-adblock-techniques">Anti - adblock techniques | AdBlocker Ultimate Help Center</a></li>

</ul>
</details>

**Discussion**: Reactions were mixed: some users agreed that giving up on Facebook is the right call, while others worried the move will encourage YouTube to push back harder. Several commenters argued that the only true escape from Facebook ads is to stop using Facebook, and one predicted the arms race will end with computer-vision models that block ads directly from what appears on screen.

**Tags**: `#uBlock Origin`, `#Facebook`, `#Ad-blocking`, `#Privacy`, `#Arms race`

---

<a id="item-7"></a>
## [AI Is Removing the Middle Class of Software Engineering?](https://blog.florianherrengt.com/ai-removing-middle-class-software-engineering.html) ⭐️ 8.0/10

In a new blog post, Florian Herrengt argues that AI coding assistants are eliminating mid-level software engineering roles, leaving only juniors and seniors. The post generated heavy discussion on Hacker News, with 672 upvotes and 592 comments. This debate touches the future of the software profession: if mid-level roles vanish, career progression, hiring strategies, and how juniors learn the craft could change dramatically. It also highlights growing concern that LLM tools may entrench a &\#x27;garbage in, garbage out&\#x27; dynamic in codebases. The article draws on anecdotal experience rather than large-scale employment data, and commenters note the lack of &\#x27;irrefutable evidence&\#x27; of job losses so far. A recurring theme is that AI can amplify both good and bad engineering, making senior judgment more valuable while reducing the need for routine &\#x27;Stack Overflow engineer&\#x27; work.

hackernews · florianherrengt · Aug 12, 13:20 · [Discussion](https://news.ycombinator.com/item?id=49271994)

**Background**: Large language models \(LLMs\) are AI systems — typically neural networks trained on massive text datasets — that can generate, summarize, and analyze human language, including code. LLMs produce code one token at a time based on patterns learned during training, rather than copying verbatim from repositories, which enables them to help with coding, debugging, and documentation.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Large_language_model">Large language model - Wikipedia</a></li>
<li><a href="https://www.ibm.com/think/topics/large-language-models">What are large language models (LLMs)? - IBM</a></li>

</ul>
</details>

**Discussion**: Commenters broadly agree that AI is reshaping engineering work but split on how. Some warn that disengaged engineers can now amplify bad decisions tenfold, while others see it as &\#x27;automation of the Stack Overflow engineer&\#x27;; a few call for keeping critical thinking in the loop and ask for hard evidence of job losses before accepting the thesis.

**Tags**: `#AI`, `#Software Engineering`, `#Career Impact`, `#LLM`, `#Tech Industry`

---

<a id="item-8"></a>
## [Engineer Warns AI-Assisted Coding Creates Unmaintainable Systems](https://simonwillison.net/2026/Aug/12/florian-herrengt/) ⭐️ 8.0/10

In a blog post featured on Simon Willison&\#x27;s site, software engineer Florian Herrengt describes a scenario where AI-generated code becomes so convoluted that developers must ask AI tools like Claude to fix bugs they don&\#x27;t understand. He argues that this threatens the &\#x27;middle class&\#x27; of software engineering. This commentary highlights a growing concern that AI-assisted programming may produce code that is efficient to write but nearly impossible to maintain or debug. If this trend continues, it could undermine code quality and alter career prospects for mid-level software engineers. The quote is from Herrengt&\#x27;s blog post &\#x27;AI is removing the middle class of software engineering&\#x27;, and references Fable, presumably Claude Fable, an Anthropic coding tool. The story depicts a team that repeatedly asks AI to fix a bug, with neither developer able to explain where the data comes from.

rss · Simon Willison · Aug 12, 15:08

**Background**: AI-assisted coding tools like Anthropic&\#x27;s Claude Fable generate substantial amounts of code from natural-language prompts, which can speed up development but also increase &\#x27;cognitive debt&\#x27; — code that nobody fully understands. In the scenario Herrengt describes, the system has grown so layered with services that debugging becomes a matter of asking the AI for answers rather than reasoning through the code. This reflects broader industry debates about how LLM-based tools are changing software engineering roles and responsibilities.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/claude/fable">Claude Fable \ Anthropic</a></li>

</ul>
</details>

**Tags**: `#AI`, `#software-engineering`, `#code-quality`, `#future-of-work`, `#LLM`

---

<a id="item-9"></a>
## [Adam&\#x27;s Per-Coordinate Updates Break Rotation Invariance, Wiping Out Low-Rank Bias](https://www.reddit.com/r/MachineLearning/comments/1vmjb3p/the_loss_does_not_see_the_basis_but_adam_does_r/) ⭐️ 8.0/10

The post shows that Adam&\#x27;s per-coordinate second moment violates rotation invariance in factored models, causing it to lose the implicit low-rank bias that gradient descent retains. A sweep of nine update rules at matched training loss reveals two clean clusters, with Adam, RMSProp, Lion, signum, and Adafactor losing the bias while GD, shared-scalar Adam, Muon, and Shampoo keep it. This pinpoints the anisotropy of Adam&\#x27;s per-coordinate denominator—rather than adaptivity in general—as the culprit behind lost implicit low-rank regularization, informing optimizer design for matrix factorization and deep learning. The finding also reconciles contradictory reports about Muon&\#x27;s spectral bias by showing both behaviors emerge along the same axis, providing a unified explanation. The author introduces a one-parameter family that interpolates Adam&\#x27;s denominator from per-coordinate to a single shared scalar, and recovery error improves monotonically along this interpolation. Muon is exact on truly low-rank targets but degrades fastest as spectral tail energy is added, crossing over with GD near 4% tail energy; the theoretical analysis covers memoryless rules only, with momentum results remaining empirical.

reddit · r/MachineLearning · /u/EtherealGlyph · Aug 12, 16:39

**Background**: In matrix factorization, the loss is invariant under rotations W = UV^T → \(UQ, VQ\), so optimizers that respect this symmetry are expected to behave independently of the basis chosen to represent the factors. Gradient descent and its variants are known to exhibit an implicit low-rank bias, which has been linked to gradient noise and the dynamics of the optimization process. Adam, however, divides each coordinate update by a per-coordinate estimate of the gradient magnitude, an operation that is not rotation-invariant and thus can fundamentally alter the optimization trajectory. This post tests empirically whether this symmetry property is the dividing line between optimizers that preserve or lose the implicit low-rank bias.

<details><summary>References</summary>
<ul>
<li><a href="https://cbmm.mit.edu/sites/default/files/publications/Implicit+Rank+Minimization.pdf">CBMM Memo No. 134 March 28, 2022 SGD Noise and Implicit Low-Rank Bias in Deep</a></li>
<li><a href="https://minyoungg.github.io/overparam/resources/overparam-v2.pdf">Preprint revision 2 THE LOW-RANK SIMPLICITY BIAS IN DEEP NETWORKS Minyoung Huh</a></li>
<li><a href="https://www.emergentmind.com/topics/adam">ADAM: Adaptive Moment Estimation - emergentmind.com</a></li>

</ul>
</details>

**Tags**: `#optimization`, `#Adam`, `#implicit bias`, `#matrix factorization`, `#machine learning`

---

<a id="item-10"></a>
## [LTX Releases Open-Source Video Model LTX-2.5 Running on a Single RTX 5090](https://ltx.io/model/ltx-2-5) ⭐️ 8.0/10

LTX released LTX-2.5, an open-source video generation foundation model with fully open weights, training code, and inference pipeline. The model runs locally on a single RTX 5090 and supports text-to-video and image-to-video generation. This release significantly lowers the barrier for AI video research and commercial adoption by making a production-grade video generation model fully open-source and locally runnable on consumer-class hardware. It gives researchers and small teams a strong, open alternative to proprietary video models. LTX-2.5 is built on a 22B-parameter asymmetric dual-stream diffusion transformer, paired with a new diffusion video decoder and a Gemma 4 12B text encoder. The weights are free for commercial use by companies earning under $10M annually; in a 98-prompt artifact evaluation, LTX 2.5 Pro ranked first among ten models.

telegram · zaihuapd · Aug 12, 02:15

**Background**: Video generation models like LTX-2.5 use diffusion transformers to generate temporally coherent video frames from text or image prompts. &quot;Open weights&quot; means the trained model parameters are publicly released, allowing developers to fine-tune, self-host, and build commercial products without relying on closed APIs. Gemma 4 12B is Google&\#x27;s medium-sized multimodal language model, which here serves as an encoder to improve prompt understanding. LTX also reports that self-hosted on 2x GB200 GPUs, LTX-2.5 can generate a 10-second 720p clip in 6.8 seconds, faster than real time.

<details><summary>References</summary>
<ul>
<li><a href="https://ltx.io/model/ltx-2">LTX-2: Production-Grade AI Video Generation Model | LTX</a></li>
<li><a href="https://ltx.io/model/ltx-2-5">LTX-2.5: LTX&#x27;s Latest AI Open-Source Foundation Model | LTX</a></li>
<li><a href="https://developers.googleblog.com/gemma-4-12b-the-developer-guide/">Gemma 4 12B: The Developer Guide - Google Developers Blog</a></li>

</ul>
</details>

**Tags**: `#video generation`, `#open-source`, `#AI model`, `#diffusion`, `#text-to-video`

---

<a id="item-11"></a>
## [WeChat Releases WeLM, Resource-Efficient LLM Family with MoE](https://x.com/Weixin_WeChat/status/2087509298310209718) ⭐️ 8.0/10

WeChat&\#x27;s team has released WeLM, a family of resource-efficient large language models. WeLM-80B, with only 3B active parameters, is now deployed in WeChat&\#x27;s AI agent Xiaowei, while the larger WeLM-617B MoE model with 23B active parameters is under development. This development is significant because a major player like Tencent/WeChat is prioritizing resource efficiency in large language models and deploying them into mass-market products. The MoE-based WeLM-617B model, with 617B total parameters but only 23B active, could reduce inference costs while maintaining strong capabilities, influencing broader industry trends. WeLM-80B has 80B total parameters but activates only 3B parameters per token. The in-development WeLM-617B uses Mixture-of-Experts architecture with 23B active parameters, targeting complex WeChat ecosystem tasks such as intelligent mini-program development and generation of &\#x27;WeChat Xiaowei&\#x27; mini-tools.

telegram · zaihuapd · Aug 12, 13:58

**Background**: Large language models \(LLMs\) are AI systems trained on massive amounts of text data to understand and generate human-like text. Traditional LLMs activate all parameters for every request, making inference computationally expensive. Mixture of Experts \(MoE\) is an architecture that selectively activates only a subset of specialized sub-networks \(&\#x27;experts&\#x27;\) based on the input, allowing larger total parameter sizes with lower computational cost. &\#x27;Activation parameters&\#x27; refers to the subset of model weights actually used when processing a given token.

<details><summary>References</summary>
<ul>
<li><a href="https://welm.weixin.qq.com/en/">WeLM Blog</a></li>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://www.nvidia.com/en-us/glossary/mixture-of-experts/">What Is Mixture of Experts (MoE) and How It Works? - NVIDIA</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#MoE`, `#WeChat`, `#Tencent`, `#AI`

---
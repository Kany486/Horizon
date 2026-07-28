---
layout: default
title: "Horizon Summary: 2026-07-28 (EN)"
date: 2026-07-28
lang: en
---

> From 29 items, 11 important content pieces were selected

---

1. [Moonshot AI Open-Sources Kimi K3: First 2.8T-Parameter Open Model](#item-1) ⭐️ 10.0/10
2. [Anthropic clarifies stance on open-weight models](#item-2) ⭐️ 9.0/10
3. [Critical RCE Vulnerability Found in Fastjson2 \(All Versions\)](#item-3) ⭐️ 9.0/10
4. [China Starts Mass Production of Domestic DUV Lithography Machines](#item-4) ⭐️ 9.0/10
5. [vLLM v0.26.0 Released with Inkling, DeepSeek-V4, and More](#item-5) ⭐️ 8.0/10
6. [Judge Rejects Google&\#x27;s DMCA-Based Scraping Lawsuit](#item-6) ⭐️ 8.0/10
7. [Misago Forum Drops React for HTMX](#item-7) ⭐️ 8.0/10
8. [Paged Out \#9: Community Technical Zine Released](#item-8) ⭐️ 8.0/10
9. [Frontier LLMs Show Left-Leaning Political Bias Across 8 Benchmarks](#item-9) ⭐️ 8.0/10
10. [Google teases Gemini 4 as most ambitious pre-training yet](#item-10) ⭐️ 8.0/10
11. [Alibaba Launches Qianwen Office AI Platform](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Moonshot AI Open-Sources Kimi K3: First 2.8T-Parameter Open Model](https://huggingface.co/moonshotai/Kimi-K3) ⭐️ 10.0/10

Moonshot AI has released the weights for Kimi K3, a 2.8 trillion parameter Mixture-of-Experts model with 104B active parameters, making it the first open 3T-level model. It introduces Kimi Delta Attention and Attention Residuals architectures, supports multimodal understanding and 1M token context, and achieves competitive performance with frontier models like GPT-5.6 and Claude Fable 5. Open-sourcing a 2.8 trillion parameter model at this scale significantly advances open-source AI, providing researchers and developers access to capabilities that rival proprietary frontier models. This could accelerate innovation in long-context reasoning, agentic tasks, and multimodal applications. Kimi K3 uses Stable LatentMoE with 896 total experts, activating 16 per token, achieving ~2.5x extension efficiency over Kimi K2. The model supports MXFP4 quantization and is available under the Kimi K3 License, which requires a separate agreement for large Model-as-a-Service businesses exceeding $20M annual revenue.

telegram · zaihuapd · Jul 27, 15:15

**Background**: Mixture-of-Experts \(MoE\) is a neural network architecture that scales model capacity by using multiple &\#x27;expert&\#x27; sub-networks, activating only a subset per input to maintain computational efficiency. Kimi K3 builds on Moonshot AI&\#x27;s previous Kimi K2 model and introduces novel attention mechanisms: Kimi Delta Attention \(KDA\) extends Gated DeltaNet with per-channel decay for better memory management, and Attention Residuals \(AttnRes\) replace standard residual connections with learned attention over prior layers, improving representation aggregation. Stable LatentMoE further enhances sparsity and routing stability.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2510.26692">Kimi Linear: An Expressive, Efficient Attention Architecture</a></li>
<li><a href="https://arxiv.org/abs/2603.15031">[2603.15031] Attention Residuals</a></li>

</ul>
</details>

**Discussion**: The community on Simon Willison&\#x27;s blog notes the license change: the K3 license no longer calls itself &\#x27;modified MIT&\#x27; and requires a separate agreement for large MaaS businesses. They appreciate that Moonshot AI consistently uses &\#x27;open weight&\#x27; rather than &\#x27;open source&\#x27;. Pricing on OpenRouter matches Moonshot&\#x27;s own at $3/M input and $15/M output.

**Tags**: `#AI`, `#Open Source`, `#Large Language Model`, `#MoE`, `#Multimodal`

---

<a id="item-2"></a>
## [Anthropic clarifies stance on open-weight models](https://www.anthropic.com/news/position-open-weights-models) ⭐️ 9.0/10

Anthropic released a policy statement advocating mandatory safety testing for all sufficiently capable AI models, including open-weight ones, while stating it has never supported an outright ban on open-weight models. This position could shape AI regulation debates by framing safety testing as a middle ground, but critics argue that costly or selectively enforced testing requirements effectively ban open-weight models, impacting open-source AI development and research. Anthropic specifically supports three measures: preventing export of advanced AI chips to China, mandatory safety testing for frontier models, and government limits on compute and energy used for AI training. The company emphasizes that testing should apply equally to open and closed models.

hackernews · surprisetalk · Jul 27, 22:03 · [Discussion](https://news.ycombinator.com/item?id=49076057)

**Background**: Open-weight models are AI models whose trained parameters are publicly released, allowing anyone to download, run, and fine-tune them. They enable transparency and innovation but also raise concerns about misuse, as they can be deployed without oversight. Anthropic&\#x27;s statement addresses the tension between the open-source community&\#x27;s desire for unfettered access and growing calls for safety regulation.

<details><summary>References</summary>
<ul>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>
<li><a href="https://opensource.org/ai/open-weights">Open Weights: not quite what you’ve been told</a></li>
<li><a href="https://telnyx.com/resources/open-weight-models">Open Weight Models What They Are and How to Use Them</a></li>

</ul>
</details>

**Discussion**: Community comments on Hacker News are deeply skeptical. Many argue that mandatory safety testing, especially if controlled by a single entity or made prohibitively expensive, is a de facto ban on open-weight models. Others accuse Anthropic of hypocrisy for supporting chip export bans while claiming not to advocate bans, suggesting the real motive is commercial protectionism rather than safety.

**Tags**: `#AI safety`, `#open-weights`, `#regulation`, `#Anthropic`, `#AI policy`

---

<a id="item-3"></a>
## [Critical RCE Vulnerability Found in Fastjson2 \(All Versions\)](https://mp.weixin.qq.com/s/LJaul1jNjK9pXRAkoUiMEA) ⭐️ 9.0/10

Longting Technology disclosed a remote code execution \(RCE\) vulnerability in Fastjson2 on July 27, 2026, affecting all versions up to 2.0.62. Attackers can bypass AutoType validation via malicious JSON data to execute arbitrary code, and no official patch is yet available. As one of the most widely used JSON libraries in the Java ecosystem, this vulnerability poses a critical threat to countless applications and services. Immediate mitigation—such as completely disabling AutoType—is required, as attackers can easily exploit this flaw to gain full system control. The vulnerability affects all released Fastjson2 versions, with version 2.0.62 being the latest affected. Pull request \#7695 was closed without merging, and the maintainers have confirmed the issue but provided no patch yet.

telegram · zaihuapd · Jul 27, 10:31

**Background**: Fastjson2 is a high-performance JSON library for Java developed by Alibaba, offering features like AutoType for automatic type resolution during deserialization. AutoType allows automatic class instantiation during JSON parsing, which can be exploited if not properly controlled. The library has a history of similar vulnerabilities—just earlier this month, a similar RCE was found in the older Fastjson 1.x series.

<details><summary>References</summary>
<ul>
<li><a href="https://alibaba.github.io/fastjson2/autotype_cn.html">FASTJSON 2 Autotype机制介绍 | fastjson2</a></li>
<li><a href="https://github.com/alibaba/fastjson2">GitHub - alibaba/fastjson2: 🚄 FASTJSON2 is a Java JSON library with excellent performance.</a></li>

</ul>
</details>

**Tags**: `#security`, `#vulnerability`, `#fastjson2`, `#rce`, `#java`

---

<a id="item-4"></a>
## [China Starts Mass Production of Domestic DUV Lithography Machines](https://www.theinformation.com/articles/china-starts-mass-producing-homegrown-duv-chipmaking-tools-advance-local-chip-industry) ⭐️ 9.0/10

China has begun mass production of domestically developed immersion deep ultraviolet \(DUV\) lithography machines, with plans to produce about 5 units this year and 20 units by 2027. This marks a groundbreaking step in semiconductor manufacturing, directly challenging ASML&\#x27;s market dominance and potentially reshaping global chip supply chains amid geopolitical tensions. The domestic DUV tools still lag behind ASML in performance and reliability, requiring months of testing by chipmakers. Some critical components are sourced from Japan, and local supply chain delays have already affected progress this year.

telegram · zaihuapd · Jul 27, 14:10

**Background**: Deep ultraviolet \(DUV\) lithography uses excimer lasers with wavelengths of 248 or 193 nm to pattern integrated circuits. Immersion lithography replaces the air gap between lens and wafer with a liquid, typically water, to improve resolution. ASML currently dominates the advanced lithography market, but Western export restrictions have spurred China to develop its own tools.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DUV_lithography">DUV lithography</a></li>
<li><a href="https://en.wikipedia.org/wiki/Immersion_lithography">Immersion lithography</a></li>

</ul>
</details>

**Tags**: `#semiconductor`, `#lithography`, `#DUV`, `#China`, `#ASML`

---

<a id="item-5"></a>
## [vLLM v0.26.0 Released with Inkling, DeepSeek-V4, and More](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 8.0/10

vLLM v0.26.0 adds support for the new Inkling model family, optimizations for DeepSeek-V4, fp32 lm\_head via head\_dtype, and flexible attention backends per KV-cache group. This release includes 411 commits from 212 contributors. vLLM is a widely-used LLM inference engine, and this release delivers major performance gains and new model support, especially for the cutting-edge Inkling \(975B MoE\) and DeepSeek-V4 models. The flexible attention backend and fp32 lm\_head improve accuracy and adaptability for hybrid models, benefiting both developers and end-users. Inkling support includes piecewise CUDA graphs, Hopper FA4 relative attention, MTP=1 speculative decoding, LoRA, and ModelOpt NVFP4 quantization. DeepSeek-V4 optimizations include a specialized routing kernel \(2.94% E2E TPOT improvement\), fused\_topk\_bias \(1.5–2x speedup\), and ROCm two-stage compressor for HCA prefill.

github · khluu · Jul 27, 01:06

**Background**: vLLM is an open-source high-throughput LLM inference engine designed to serve large language models efficiently. The Inkling model is a 975B-parameter Mixture-of-Experts transformer with 41B active parameters, supporting up to 1M tokens context. FlashAttention-4 \(FA4\) is a new attention algorithm optimized for NVIDIA Hopper GPUs, and NVFP4 is a 4-bit quantization format from NVIDIA that reduces memory usage.

<details><summary>References</summary>
<ul>
<li><a href="https://thinkingmachines.ai/news/introducing-inkling/">Inkling: Our Open-Weights Model - Thinking Machines Lab</a></li>
<li><a href="https://modal.com/blog/reverse-engineer-flash-attention-4">We reverse-engineered Flash Attention 4</a></li>
<li><a href="https://nvidia.github.io/TensorRT-LLM/features/quantization.html">Quantization — TensorRT LLM</a></li>

</ul>
</details>

**Tags**: `#vLLM`, `#LLM inference`, `#release`, `#machine learning`, `#performance`

---

<a id="item-6"></a>
## [Judge Rejects Google&\#x27;s DMCA-Based Scraping Lawsuit](https://www.techdirt.com/2026/07/27/judge-rejects-googles-attempt-to-dmca-its-way-out-of-being-scraped/) ⭐️ 8.0/10

A federal judge ruled that Google cannot use the Digital Millennium Copyright Act \(DMCA\) to block third-party scraping of its search results, rejecting the company&\#x27;s argument that scraping constitutes copyright infringement. This decision sets a legal precedent limiting the use of copyright law to control data access on the internet, potentially affecting how tech companies protect their publicly available data and influencing the future of web scraping. The case involved Google vs. SerpAPI, a company that scrapes Google search results. The judge held that search results are factual compilations that may not meet the originality threshold for copyright protection under U.S. law.

hackernews · cdrnsf · Jul 27, 18:15 · [Discussion](https://news.ycombinator.com/item?id=49073513)

**Background**: Web scraping is the automated extraction of data from websites. The DMCA is a U.S. law that criminalizes circumvention of technological measures protecting copyrighted works. Google had argued that scraping its search results violated the DMCA, but the court disagreed.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DMCA">DMCA</a></li>
<li><a href="https://en.wikipedia.org/wiki/Web_scraping">Web scraping</a></li>

</ul>
</details>

**Discussion**: Commenters largely supported the ruling, noting irony that Google&\#x27;s own business relies on scraping the open web. Some criticized Google for removing its search API while suing third parties that fill the gap. Others discussed differences between EU and US copyright protections for databases.

**Tags**: `#legal`, `#web scraping`, `#copyright`, `#Google`, `#DMCA`

---

<a id="item-7"></a>
## [Misago Forum Drops React for HTMX](https://misago-project.org/t/removing-reactjs-from-the-codebase-and-adapting-htmx-for-ui-interactivity/1267/) ⭐️ 8.0/10

The Misago forum project removed React.js from its codebase and adopted HTMX for UI interactivity, citing performance and simplicity benefits. This migration reflects a broader trend in web development toward simpler, server-rendered UIs using hypermedia-driven approaches like HTMX, reducing client-side complexity. HTMX extends HTML with custom attributes for AJAX, enabling dynamic updates without writing JavaScript. The forum&\#x27;s switch is part of a growing movement away from heavy frontend frameworks.

hackernews · Ralfp · Jul 27, 09:58 · [Discussion](https://news.ycombinator.com/item?id=49067301)

**Background**: HTMX is an open-source JavaScript library that allows developers to create dynamic web pages using HTML attributes, avoiding complex JavaScript frameworks. It was created by Carson Gross as a successor to intercooler.js. The Misago forum project is a modern forum software that originally used React for interactive elements.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Htmx">Htmx</a></li>
<li><a href="https://htmx.org/">htmx - high power tools for html</a></li>
<li><a href="https://github.com/bigskysoftware/htmx">GitHub - bigskysoftware/ htmx : htmx - high power tools for HTML</a></li>

</ul>
</details>

**Discussion**: Community comments show support for HTMX in forum contexts, with users sharing positive experiences and recommending pairing HTMX with TailwindCSS or DaisyUI. Some note limitations with highly interactive features like filterable product listings.

**Tags**: `#HTMX`, `#React`, `#web development`, `#server-side rendering`, `#frontend framework`

---

<a id="item-8"></a>
## [Paged Out \#9: Community Technical Zine Released](https://pagedout.institute/download/PagedOut_009.pdf) ⭐️ 8.0/10

Paged Out \#9, a community-driven technical zine covering low-level hacking topics, has been released as a free PDF download from pagedout.institute. It continues a tradition of deep, hacker-curious content that resonates with the low-level programming and security community, offering diverse topics like subpixel rendering and computable tilings. The zine includes articles such as &\#x27;Baby Steps in C&\#x27; and &\#x27;The Subpixel Zoo&\#x27;, and features a rediscovery of Wang&\#x27;s 1960s work on computable tilings tying the domino problem to the halting problem.

hackernews · laurensr · Jul 27, 14:22 · [Discussion](https://news.ycombinator.com/item?id=49070138)

**Background**: Paged Out is a community-driven technical magazine \(zine\) that focuses on low-level programming, hacking, and computer science topics. It is released periodically and distributed for free in PDF format, with print editions available for purchase.

**Discussion**: Commenters praised the zine&\#x27;s depth and design, with one comparing it to a modern 2600 or Phrack. Another highlighted the uncredited rediscovery of Wang&\#x27;s work, showing the equivalence of the halting problem and the domino problem.

**Tags**: `#hacker-culture`, `#zine`, `#low-level`, `#technical-writing`, `#programming`

---

<a id="item-9"></a>
## [Frontier LLMs Show Left-Leaning Political Bias Across 8 Benchmarks](https://www.reddit.com/r/MachineLearning/comments/1v8fnzw/evaluated_6_frontier_llms_gpt54_claude_sonnet_46/) ⭐️ 8.0/10

A solo evaluation of six frontier LLMs \(GPT-5.4, Claude Sonnet 4.6, Claude Opus 4.7, Gemini Pro/Flash, Grok 4.3\) across 8 bias benchmarks with ~20,600 examples found that all models exhibit left-leaning political bias in behavior, even Grok which self-reports as right-leaning. This study reveals a systematic political bias across leading commercial and open LLMs, which could affect their deployment in sensitive applications like content moderation, policy analysis, and fair decision-making. It also challenges the assumption that a model&\#x27;s stated political leaning matches its actual behavior. Notably, Grok self-reports as right-leaning but behaves left-leaning when classifying content or answering policy questions, while refusal rates on race-related questions varied significantly \(GPT-5.4 refused 20.3% of the time, Claude Opus 4.7 refused 13.8%\). The study is a solo, non-peer-reviewed project with limitations including no multi-run averaging and a single prompt template per task.

reddit · r/MachineLearning · /u/marggggggggg · Jul 27, 22:37

**Background**: Bias benchmarks are standardized datasets designed to measure undesirable social biases in language models, such as stereotypes, prejudice, or unfair associations. Common benchmarks include WinoBias \(gender\), BBQ \(race/ethnicity\), SeeGULL \(geo-cultural stereotypes\), OpinionsQA \(alignment with demographic opinions\), and political bias datasets like the Political Compass and Hyperpartisan News. This study used eight such datasets to evaluate both explicit and implicit biases across political, gender, and racial dimensions.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/google-research-datasets/seegull">GitHub - google-research- datasets / seegull : SeeGULL is...</a></li>
<li><a href="https://huggingface.co/datasets/cajcodes/political-bias">cajcodes / political - bias · Datasets at Hugging Face</a></li>
<li><a href="https://arxiv.org/abs/2303.17548">[2303.17548] Whose Opinions Do Language Models Reflect?</a></li>

</ul>
</details>

**Tags**: `#bias evaluation`, `#LLM alignment`, `#political bias`, `#fairness benchmarks`, `#frontier models`

---

<a id="item-10"></a>
## [Google teases Gemini 4 as most ambitious pre-training yet](https://9to5google.com/2026/07/26/google-gemini-4-teases/) ⭐️ 8.0/10

Google CEO Sundar Pichai announced during Alphabet&\#x27;s Q2 2026 earnings call that Gemini 4, Google&\#x27;s next flagship AI model, is currently in training as the company&\#x27;s most ambitious pre-training project, expected to launch in late 2026. This announcement signals Google&\#x27;s commitment to scaling AI models to stay competitive in the frontier AI race, potentially leading to significant advancements in capabilities. The release of Gemini 4 could impact the entire AI ecosystem, including developers, businesses, and end-users who rely on Google&\#x27;s AI services. Pichai emphasized that compute resources will be prioritized for frontier AGI research to ensure Gemini 4 remains cutting-edge upon release. Additionally, the Gemini 3.x Flash series will maintain nearly monthly iteration updates, focusing on improving capabilities like intelligent coding.

telegram · zaihuapd · Jul 27, 04:06

**Background**: Gemini is a family of multimodal large language models developed by Google DeepMind, announced in December 2023 as the successor to LaMDA and PaLM 2. Pre-training is the initial phase of training an LLM where it learns from a large, diverse dataset, often trillions of tokens. AGI \(Artificial General Intelligence\) refers to a hypothetical AI that matches or surpasses human cognitive abilities across virtually all tasks.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Gemini_%28AI_model%29">Gemini (AI model)</a></li>
<li><a href="https://www.moveworks.com/us/en/resources/ai-terms-glossary/pre-training">What is Pre-Training? - Moveworks</a></li>
<li><a href="https://en.wikipedia.org/wiki/Artificial_general_intelligence">Artificial general intelligence - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#Google`, `#Gemini 4`, `#AI`, `#Large Language Model`, `#Pre-training`

---

<a id="item-11"></a>
## [Alibaba Launches Qianwen Office AI Platform](https://qwenwork.cn/) ⭐️ 8.0/10

Alibaba has launched the beta version of &\#x27;Qianwen Office&\#x27; \(千问办公\), a unified AI office platform that enables users to generate and edit documents, spreadsheets, PPTs, web pages, code, and multimedia via natural language. It also offers desktop computer control capabilities using browser automation and Computer Use features to perform cross-app actions like clicking, typing, and data extraction. This launch marks a major entry into the AI productivity market by a leading tech giant, potentially intensifying competition with other Chinese tech firms like Tencent and ByteDance. It integrates document generation with computer control, a step toward autonomous AI agents that can directly interact with operating systems, which could redefine office workflows. The platform covers web, Windows, and macOS clients, and integrates with DingTalk. Pricing includes a free tier and paid plans starting at 78 yuan/month for Standard \(2000 credits\) and 158 yuan/month for Premium \(4000 credits\). New users receive 2000 free credits for 90 days. Computer control features may capture screen content or perform irreversible actions, with user confirmation required by default.

telegram · zaihuapd · Jul 27, 05:45

**Background**: AI office platforms use large language models to automate document creation and editing. &\#x27;Computer Use&\#x27; refers to AI systems that can directly control a computer&\#x27;s interface, mimicking human actions like clicking and typing. Alibaba&\#x27;s platform unifies three AI products: QoderWork, Wukong, and MuleRun, targeting enterprise productivity.

<details><summary>References</summary>
<ul>
<li><a href="https://phemex.com/news/article/alibaba-launches-qianwen-office-to-unify-ai-agent-office-platforms-94023">Alibaba Unveils &#x27;Qianwen Office&#x27; to Consolidate AI Platforms ...</a></li>
<li><a href="https://x.com/thexpin/status/2079518147812495634">According to Caijing, Alibaba is preparing to launch Qianwen Office ...</a></li>
<li><a href="https://www.webull.com/news/15263087389402112">It is reported that Ali will launch Qianwen Office. It has integrated ...</a></li>

</ul>
</details>

**Tags**: `#AI office`, `#Alibaba`, `#document generation`, `#computer control`, `#productivity`

---
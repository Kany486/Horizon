---
layout: default
title: "Horizon Summary: 2026-08-04 (EN)"
date: 2026-08-04
lang: en
---

> From 33 items, 11 important content pieces were selected

---

1. [Qwen 3.8-Max: 2.4T-Parameter Model Open-Sourced for First Time](#item-1) ⭐️ 9.0/10
2. [OpenAI Highlights Ten Advances in Math and Theoretical CS](#item-2) ⭐️ 8.0/10
3. [Devtools Must Be Open Source: LLMs Make Local Forks Practical](#item-3) ⭐️ 8.0/10
4. [ComfyUI Adds Day-0 Support for MiniMax H3 With 2K Video and Native Audio](#item-4) ⭐️ 8.0/10
5. [Andy Pavlo joins ClickHouse to lead new Labs initiative](#item-5) ⭐️ 8.0/10
6. [Jane Street Releases Bonsai, an OCaml UI Library](#item-6) ⭐️ 8.0/10
7. [SemiAnalysis Deep Dive Explores Kimi K3&\#x27;s Novel Architecture](#item-7) ⭐️ 8.0/10
8. [Desk Reject Papers Without Reproducible Code, Says Reviewer](#item-8) ⭐️ 8.0/10
9. [DNA Lab Equipment Flaw Exposes 30 Years of Evidence](#item-9) ⭐️ 8.0/10
10. [Nvidia CMP 170HX Mining Card Cracked: 80GB VRAM Unlocked, Prices Surge](#item-10) ⭐️ 8.0/10
11. [Apple Files Legal Challenge Against UK Government&\#x27;s iCloud Backdoor Demand](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Qwen 3.8-Max: 2.4T-Parameter Model Open-Sourced for First Time](https://qwen.ai/blog?id=qwen3.8) ⭐️ 9.0/10

Alibaba&\#x27;s Qwen team officially launched Qwen 3.8-Max, a 2.4-trillion-parameter Mixture-of-Experts model with 95 billion active parameters, on the day of the announcement. The model weights will be open-sourced next week, marking the first time Qwen has opened weights for a Max-level model. This is the first open-sourcing of a frontier-scale Max-level model, potentially lowering the barrier for researchers and enterprises to access state-of-the-art AI. It also signals that open-weights models can compete head-to-head with leading closed models, reshaping the broader AI ecosystem. Built on the Qwen 3.5 architecture, Qwen 3.8-Max shows improvements in coding, work, research, and long-horizon tasks. In a coding benchmark it ran autonomously for over 10 days, and it beat 458 of 526 teams in the WWW2025 multimodal intent-recognition competition within 24 hours; it is now available via the QwenCloud API.

telegram · zaihuapd · Aug 3, 02:31

**Background**: Mixture-of-Experts \(MoE\) is an architecture that keeps the total parameter count large while activating only a subset of parameters for each token, so inference cost depends mainly on active parameters. Active parameters include the selected experts and the shared parts of the model used for one token. Many modern LLMs such as GPT-4, Mixtral, and DeepSeek-V3 adopt MoE for efficiency, and Qwen 3.8-Max follows this trend with 95 billion active parameters.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://sebastianraschka.com/faq/docs/mixture-of-experts.html">What is mixture-of-experts (MoE), and how does it differ from a dense LLM?</a></li>
<li><a href="https://aiweekly.co/learning-ai/generative-ai/what-mixture-experts-moe-how-modern-llms-get-efficient">What Is Mixture of Experts ( MoE )? How Modern LLMs ... | AI Weekly</a></li>

</ul>
</details>

**Tags**: `#AI`, `#LLM`, `#Qwen`, `#open-source`, `#model release`

---

<a id="item-2"></a>
## [OpenAI Highlights Ten Advances in Math and Theoretical CS](https://openai.com/index/ten-advances-in-mathematics/) ⭐️ 8.0/10

OpenAI published an article titled &\#x27;Ten advances in mathematics and theoretical computer science,&\#x27; highlighting AI-driven achievements in these fields. The announcement has sparked a large community debate about AI&\#x27;s role in mathematical discovery. This matters because it signals AI&\#x27;s growing influence in mathematics, a field traditionally considered resistant to automation. The community&\#x27;s intense discussion reflects both excitement and concern about the exponential pace of AI progress and its impact on research practice. The announcement emphasizes mathematics and theoretical computer science, areas where AI can generate and verify solutions. Community comments reference specific problems such as high-dimensional sphere packing and multicolor Ramsey numbers, suggesting these may be among the highlighted advances.

hackernews · milkshakes · Aug 3, 16:27 · [Discussion](https://news.ycombinator.com/item?id=49157930)

**Background**: Large language models \(LLMs\) are increasingly being applied to mathematical research, where they can generate conjectures and check proofs. The exponential progress in AI capabilities has led to debates about which intellectual tasks will be automated next. The discussion in the comments reflects a broader conversation about the future of mathematical practice and whether AI will ultimately solve all computable problems.

**Discussion**: Commenters generally express awe at the exponential growth of AI capabilities, with one noting that math seems to be on a y=2^x curve. Some argue that all computable problems will eventually fall to computers, while others point out that AI still cannot intuit new conjectures. A few share intuitive explanations for the highlighted problems, and the overall sentiment is that AI&\#x27;s impact is undeniable.

**Tags**: `#AI`, `#mathematics`, `#theoretical computer science`, `#OpenAI`, `#LLMs`

---

<a id="item-3"></a>
## [Devtools Must Be Open Source: LLMs Make Local Forks Practical](https://blog.exe.dev/devtools-must-be-open-source) ⭐️ 8.0/10

A blog post argues that developer tools must be open source, claiming that LLMs now make it practical for users to read, modify, and maintain their own forks. It proposes workflows like nightly cron jobs that rebase local AI-made changes on top of upstream updates. This shifts the open-source debate from &\#x27;users cannot maintain forks&\#x27; to &\#x27;AI removes that barrier,&\#x27; potentially influencing how devtools are designed and distributed. If accepted, maintainers may need to prioritize fork-friendly source structure over configuration systems and plugins. The post apparently argues against config files, options, and plugin systems in favor of hard-coding changes via an LLM, citing the ability to automate rebasing. Commenters counter that this is energy-inefficient, unreliable with checkouts, and that downstream/upstream feature clashes create real maintenance burdens.

hackernews · bryanmikaelian · Aug 3, 14:15 · [Discussion](https://news.ycombinator.com/item?id=49156111)

**Background**: Open-source developer tools allow users to inspect and change source code, but historically only a minority have the time to maintain a fork. LLMs lower the cost of reading, editing, and rebasing code, reviving the ideal that anyone can modify the tools they use. However, professional maintainers point out that forks still create ongoing merge, compatibility, and testing work that automation does not eliminate.

**Discussion**: Commenters are generally open to open-source devtools but split on the LLM-modification argument. Simon Willison sees LLMs making the original open-source dream more feasible, while kelnos calls replacing configs with hard-coded rebuilds inefficient; theamk warns that nightly AI rebases are unreliable and hard to verify, and lalitmaganti argues the fork-everything approach is idealistic given real maintainer costs.

**Tags**: `#open-source`, `#developer-tools`, `#LLM`, `#software-engineering`, `#community-discussion`

---

<a id="item-4"></a>
## [ComfyUI Adds Day-0 Support for MiniMax H3 With 2K Video and Native Audio](https://blog.comfy.org/p/minimax-h3-day-0-support-in-comfyui) ⭐️ 8.0/10

ComfyUI has added day-0 support for MiniMax H3, an open-weights multimodal model that generates 2K video at 24 fps with native audio. The integration includes weight pruning that cuts memory footprint by 66%, from 123.6 GB to 42.5 GB in the smallest variant, enabling local runs on GPUs like the RTX 3060. This matters because ComfyUI is a widely used modular AI creation engine, and day-0 support lets its community immediately experiment with an open-weights model that combines text, image, video, and audio in one context. It lowers the barrier to high-quality 2K video generation and strengthens the open-model ecosystem against closed video-generation services. MiniMax H3, also called Hailuo 3.0, outputs 1440p \(marketed as 2K\) at a fixed 24 frames per second, and text, images, video, and audio are processed as multi-asset references in a single request. Community benchmarks show roughly 10 minutes for a 10-second 480p clip on an RTX 4070 Ti Super with 16 GB VRAM, while odd or unrealistic scenarios still produce visible artifacts.

hackernews · vblanco · Aug 3, 13:34 · [Discussion](https://news.ycombinator.com/item?id=49155629)

**Background**: ComfyUI is an open-source, node-graph-based AI creation engine that gives users control over models, parameters, and outputs. MiniMax H3 is a general-purpose multimodal video model released as open weights, meaning its final parameters are publicly downloadable so users can run and modify it locally. Open-weight models sit between fully closed and fully open-source AI, offering transparency and customization without necessarily releasing training data.

<details><summary>References</summary>
<ul>
<li><a href="https://morphic.com/resources/models/minimax-h3">MiniMax H 3 (Hailuo 3.0): full specs and input limits</a></li>
<li><a href="https://fal.ai/learn/devs/minimax-h3-prompting-guide">MiniMax H 3 Prompting Guide + 44 Video Examples | fal</a></li>
<li><a href="https://github.com/Comfy-Org/ComfyUI">GitHub - Comfy -Org/ ComfyUI : The most powerful and modular...</a></li>

</ul>
</details>

**Discussion**: Commenters were generally impressed with output quality and speed, with one noting the mouse render was a big leap over current SOTA models, though another saw artifacts in a beverage ad&\#x27;s can-opening scene. Several users reported practical hardware trade-offs, such as a 10-minute, 480p generation on an RTX 4070 Ti Super, and discussed the pruning technique&\#x27;s potential applicability to LLMs. Others suggested a hybrid workflow combining traditional close-up rendering with AI-generated wide shots might become common.

**Tags**: `#ComfyUI`, `#MiniMax`, `#video generation`, `#open weights`, `#AI/ML`

---

<a id="item-5"></a>
## [Andy Pavlo joins ClickHouse to lead new Labs initiative](https://clickhouse.com/blog/andy-pavlo-joins-clickhouse) ⭐️ 8.0/10

Andy Pavlo, a prominent database researcher and professor at CMU, has joined ClickHouse to head the newly established ClickHouse Labs. This move officially connects academic database research with the commercial OLAP database company. This is significant because it bridges academic research and industry practice in the database field, potentially steering ClickHouse&\#x27;s future architecture toward research-backed innovations. It also highlights a growing trend of database experts moving between academia and leading open-source companies. ClickHouse Labs appears intended to explore next-generation OLAP technologies; community commenters speculate about decoupled compute/storage, S3-based storage, and open table formats like Iceberg. Pavlo is known for his CMU database lectures and his critical views on database architecture, which may influence ClickHouse&\#x27;s roadmap.

hackernews · nikolay\_sivko · Aug 3, 14:09 · [Discussion](https://news.ycombinator.com/item?id=49156011)

**Background**: ClickHouse is an open-source columnar OLAP database designed for high-performance analytics over petabyte-scale data with high ingestion rates. OLAP \(online analytical processing\) systems are optimized for complex analytical queries on large datasets, as opposed to OLTP systems for transactional workloads. Andy Pavlo is a well-known associate professor at Carnegie Mellon University who teaches and researches database management systems, making his move to industry notable for the database community.

<details><summary>References</summary>
<ul>
<li><a href="https://clickhouse.com/docs/concepts/core-concepts/academic-overview">Architecture overview - ClickHouse Documentation</a></li>
<li><a href="https://en.wikipedia.org/wiki/Online_analytical_processing">Online analytical processing - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters are generally enthusiastic, with one hoping Pavlo will encourage ClickHouse to fund academic DB research due to shrinking government funding. Others discuss the convergence of OLAP engines like ClickHouse, StarRocks, and Trino around decoupled storage, and one viewer hopes his popular CMU lecture series continues under ClickHouse sponsorship. A lighthearted comment also playfully notes Pavlo&\#x27;s reputation for trolling.

**Tags**: `#ClickHouse`, `#database`, `#OLAP`, `#research`, `#industry-academia`

---

<a id="item-6"></a>
## [Jane Street Releases Bonsai, an OCaml UI Library](https://github.com/janestreet/bonsai) ⭐️ 8.0/10

Jane Street has released Bonsai, an open-source UI library for building reactive web applications in OCaml. The library is used internally at Jane Street for nearly all of its web applications, from corporate directories to trading system monitoring tools. Bonsai enables full-stack type safety by allowing developers to use OCaml on both the frontend and backend, a capability that many functional programmers have eagerly awaited. It offers a production-validated alternative to JavaScript-centric frontend stacks within the OCaml ecosystem. Bonsai is partly inspired by Elm and is built around an Incremental-style UI framework like Incr\_dom. It is published on opam as version v0.13.0, and its API is divided into modules for building reusable UI components.

hackernews · KolmogorovComp · Aug 3, 08:29 · [Discussion](https://news.ycombinator.com/item?id=49152842)

**Background**: OCaml is a statically typed functional language known for safety and performance. Bonsai is a UI library that brings reactive web application development to OCaml, using an Incremental-style system to manage dynamic updates. Because both client and server code can be written in OCaml, developers can share types and logic across the entire stack, eliminating many bugs that arise at the JavaScript boundary. Jane Street, a quantitative trading firm, has used Bonsai internally for all its web apps.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/janestreet/bonsai">GitHub - janestreet / bonsai : A library for building dynamic webapps...</a></li>
<li><a href="https://opam.ocaml.org/packages/bonsai/bonsai.v0.13.0/">The homepage of opam, a package manager for OCaml</a></li>

</ul>
</details>

**Discussion**: The Hacker News discussion is largely positive, with users excited about using OCaml on both frontend and backend. Some commenters raise practical concerns about adoption — such as how Bonsai compares to Melange or whether it means giving up the JavaScript ecosystem — and one commenter notes that while the library is performant, its default styling is unattractive. A commenter also links to a Jane Street podcast episode about building the UI framework.

**Tags**: `#OCaml`, `#UI framework`, `#frontend`, `#Jane Street`, `#functional programming`

---

<a id="item-7"></a>
## [SemiAnalysis Deep Dive Explores Kimi K3&\#x27;s Novel Architecture](https://newsletter.semianalysis.com/p/kimi-k3-the-manos-the-mythos-the) ⭐️ 8.0/10

SemiAnalysis published an in-depth technical analysis of Kimi K3&\#x27;s architecture, covering compressed memory, attention across depth, latent expert routing, and inference performance. The article contextualizes Kimi K3, Moonshot AI&\#x27;s 2.8T-parameter model, as a notable evolution in large-model design. This analysis matters because Kimi K3&\#x27;s architectural choices—compressed memory and attention across depth—could reshape how large models handle long contexts and manage inference costs. It gives the AI community a rare look at production-grade innovations that go beyond standard Transformer and MoE designs. Kimi K3 is a 2.8T-parameter model with a 1-million-token context window and native vision. Its compressed memory mechanism prioritizes speed over precise recall, while attention residuals enable each layer to selectively aggregate information from all previous layers, and latent expert routing reduces parameters by sharing a latent space among experts.

rss · Semianalysis · Aug 3, 19:42

**Background**: Conventional transformer models process information layer by layer, passing hidden states through residual connections, while Mixture-of-Experts \(MoE\) models selectively activate subsets of parameters via a routing function. Kimi K3 builds on these foundations with novel twists: a compressed memory module, attention residuals across depth, and latent expert routing that factorizes experts into a shared latent space. The SemiAnalysis article provides a technical deep dive into how these components work together and affect inference performance.

<details><summary>References</summary>
<ul>
<li><a href="https://www.kimi.com/blog/kimi-k3">Kimi K 3 Tech Blog: Open Frontier Intelligence</a></li>
<li><a href="https://www.datacamp.com/blog/attention-residuals-explained">Attention Residuals Explained: Rethinking Transformer Depth | DataCamp</a></li>
<li><a href="https://www.emergentmind.com/topics/mixture-of-latent-experts-mole">Mixture of Latent Experts (MoLE)</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Machine Learning`, `#Model Architecture`, `#Kimi K3`, `#Inference`

---

<a id="item-8"></a>
## [Desk Reject Papers Without Reproducible Code, Says Reviewer](https://www.reddit.com/r/MachineLearning/comments/1vei12v/its_time_to_desk_reject_papers_that_dont_include/) ⭐️ 8.0/10

A machine learning researcher and reviewer reported on Reddit that only 1 of the 12 papers they reviewed this year provided complete, reproducible training code, and proposed that conferences desk-reject papers lacking such code. The post argues that current incentives effectively encourage hiding code to avoid rejection. This proposal targets the reproducibility crisis in machine learning research, where many published results cannot be independently verified. If major venues like NeurIPS adopted such a policy, it could pressure researchers to share code and increase the trustworthiness of the field&\#x27;s findings. The reviewer found that 3 of the 5 papers that provided at least some code contained obvious bugs that invalidated the results, while 7 papers provided no code at all. They argue that there is almost no penalty for hiding code during review, which incentivizes non-reproducible submissions.

reddit · r/MachineLearning · /u/Flaky-Ambition5900 · Aug 3, 16:17

**Background**: A desk reject is a decision by an editor or conference chair to decline a manuscript immediately, without external peer review, usually for failing basic requirements. The AUROC \(Area Under the Receiver Operating Characteristic curve\) is a common performance metric in machine learning; it summarizes a model&\#x27;s ability to distinguish classes, with 1.0 being perfect and 0.5 corresponding to random guessing. Sharing code is central to reproducibility, but many researchers fear that providing code may expose bugs and increase rejection odds, so they choose to hide it.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Receiver_operating_characteristic">Receiver operating characteristic - Wikipedia</a></li>
<li><a href="https://www.aischolar.com/news/article/what-is-desk-reject">What Is a Desk Reject? 6 Common Reasons &amp; How to Avoid It</a></li>

</ul>
</details>

**Tags**: `#reproducibility`, `#machine learning`, `#research policy`, `#conference review`, `#code sharing`

---

<a id="item-9"></a>
## [DNA Lab Equipment Flaw Exposes 30 Years of Evidence](https://www.wsj.com/tech/cybersecurity/security-flaw-placed-30-years-of-dna-evidence-at-risk-of-hacking-1932775a) ⭐️ 8.0/10

Security researchers found a vulnerability in DNA analysis instruments used by most U.S. crime labs, allowing undetectable tampering with DNA evidence files dating back to 1995. Thermo Fisher Scientific privately acknowledged the flaw in July and issued a high-severity advisory with a digital-signature software update last Friday. This matters because compromised DNA evidence could undermine decades of criminal convictions and ongoing cases, affecting the integrity of the U.S. justice system. It also highlights how forensic instruments, often governed by no unified regulation, are becoming a target for cyberattacks. In testing, researchers used Anthropic&\#x27;s Claude AI software and altered a DNA scan file within about 45 minutes without triggering alerts in common analysis software. Thermo Fisher is coordinating with CISA, and no real-world exploitation has been reported.

telegram · zaihuapd · Aug 3, 05:15

**Background**: Forensic DNA analysis relies on instruments like Thermo Fisher&\#x27;s Applied Biosystems genetic analyzers, which perform STR fragment analysis used in human identification. These instruments generate DNA profiles that become court evidence, making file integrity critical. Digital signatures help verify that evidentiary files have not been altered, providing authenticity and non-repudiation in legal contexts. However, many of the 200-plus U.S. crime labs lack uniform security regulation, leaving gaps in protection.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Forensic_DNA_analysis">Forensic DNA analysis - Wikipedia</a></li>
<li><a href="https://www.thermofisher.com/us/en/home/industrial/forensics/human-identification/forensic-dna-analysis/dna-analysis.html">DNA Analysis | Thermo Fisher Scientific - US</a></li>
<li><a href="https://honorstead.com/authentication-and-digital-signatures/">Understanding Authentication and Digital Signatures in... - Honorstead</a></li>

</ul>
</details>

**Tags**: `#cybersecurity`, `#DNA forensics`, `#vulnerability`, `#Thermo Fisher`, `#evidence integrity`

---

<a id="item-10"></a>
## [Nvidia CMP 170HX Mining Card Cracked: 80GB VRAM Unlocked, Prices Surge](https://finance.sina.com.cn/tech/roll/2026-08-03/doc-inikzqsf4659769.shtml) ⭐️ 8.0/10

Researchers at Arizona State University publicly disclosed an exploit that bypasses Nvidia&\#x27;s OTP fuse locks on the CMP 170HX mining card, raising its VRAM to 80GB and unlocking FP32 performance to 94 TFLOPS. Following the disclosure, second-hand card prices jumped from 300-500 yuan to 3000-4000 yuan, with overseas listings reaching $1,500. This is a significant hardware security breakthrough because it turns a cheap, crippled mining card built on the same GA100 die as the A100 into a high-memory AI compute device. It could democratize access to large-VRAM GPUs for AI researchers and hobbyists, while raising urgent questions about Nvidia&\#x27;s hardware lockdown mechanisms. The exploit uses a stack overflow in the Falcon security coprocessor to hijack privileged control and modify registers that Nvidia had fused via one-time-programmable \(OTP\) memory. Chinese community members have verified the unlock works on Windows and Linux for AI image generation and LLM inference, but long-term stability and unlock limits vary by batch.

telegram · zaihuapd · Aug 3, 11:29

**Background**: The CMP 170HX is a crypto-mining card Nvidia released in 2021, based on a cut-down GA100 GPU with 10GB of HBM2e memory and PCIe 1.0 lock, with compute and display functions heavily restricted via OTP fuses meant to be irreversible. OTP fuses physically prevent changes after programming, which made the card&\#x27;s limits seem permanent. The Falcon microprocessor is a security coprocessor found in many Nvidia devices, including the Nintendo Switch, and is now shown to be a viable attack surface.

<details><summary>References</summary>
<ul>
<li><a href="https://marketangroup.com/product/nvidia-cmp-170hx-164mh-s-pro-mining-205w/">NVIDIA CMP 170 HX 164MH/s Pro Mining 205W – MARKETANG...</a></li>
<li><a href="https://www.ersaelectronics.com/blog/one-time-programmable-otp-memory">One-Time Programmable (OTP) Memory Guide</a></li>
<li><a href="https://www.resetera.com/threads/nvidia-security-co-processor-in-nintendo-switch-and-billions-of-other-devices-has-been-cracked.103006/">nVidia security co-processor (in Nintendo Switch and billions of ...</a></li>

</ul>
</details>

**Tags**: `#hardware-security`, `#GPU`, `#AI-compute`, `#exploit`, `#Nvidia`

---

<a id="item-11"></a>
## [Apple Files Legal Challenge Against UK Government&\#x27;s iCloud Backdoor Demand](https://www.ft.com/content/2cc9c96a-0e5b-4c33-a95a-3d11072a145c?syn-25a6b1a6=1) ⭐️ 8.0/10

Apple has filed a legal appeal with the UK Investigatory Powers Tribunal challenging the government&\#x27;s Technical Capability Notice that would force access to encrypted iCloud backups. The move follows Apple&\#x27;s decision in February 2025 to remove iCloud Advanced Data Protection in the UK rather than comply. This case could set a legal precedent on whether governments can compel technology companies to weaken end-to-end encryption. The outcome will affect the privacy and security of users worldwide, as any backdoor designed for one country could undermine trust in Apple&\#x27;s encryption globally. The UK government initially withdrew a Technical Capability Notice after objections from the US, then issued a new notice targeting only UK users. Privacy rights groups Privacy International and Liberty have also filed their own challenges, and the tribunal has scheduled a case management hearing for next month.

telegram · zaihuapd · Aug 3, 15:40

**Background**: The Investigatory Powers Tribunal is a UK judicial body that hears complaints about surveillance by public bodies. A Technical Capability Notice, issued under the Investigatory Powers Act 2016, can compel a company to build or maintain technical capabilities to respond to lawful data requests. Apple&\#x27;s Advanced Data Protection extends end-to-end encryption to additional iCloud categories, meaning Apple no longer holds the decryption keys and cannot access user data; a backdoor would require Apple to retain a key, weakening security for all users.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Investigatory_Powers_Tribunal">Investigatory Powers Tribunal - Wikipedia</a></li>
<li><a href="https://www.legislation.gov.uk/ukdsi/2018/9780111163610">The Investigatory Powers (Technical Capability) Regulations 2018</a></li>
<li><a href="https://support.apple.com/en-us/108756">How to turn on Advanced Data Protection for iCloud - Apple Support</a></li>

</ul>
</details>

**Tags**: `#Apple`, `#Encryption`, `#Backdoor`, `#Privacy`, `#Security`

---
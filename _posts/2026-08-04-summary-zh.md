---
layout: default
title: "Horizon Summary: 2026-08-04 (ZH)"
date: 2026-08-04
lang: zh
---

> 从 33 条内容中筛选出 11 条重要资讯。

---

1. [Qwen 3.8-Max 发布：2.4 万亿参数，首次开源 Max 级模型](#item-1) ⭐️ 9.0/10
2. [OpenAI 公布数学与理论计算机科学十大进展](#item-2) ⭐️ 8.0/10
3. [开发者工具必须开源：LLM 让本地修改成为现实](#item-3) ⭐️ 8.0/10
4. [ComfyUI 首发支持 MiniMax H3，带来 2K 视频与原生音频](#item-4) ⭐️ 8.0/10
5. [Andy Pavlo 加入 ClickHouse，领导新实验室](#item-5) ⭐️ 8.0/10
6. [Jane Street 发布 OCaml UI 库 Bonsai](#item-6) ⭐️ 8.0/10
7. [SemiAnalysis 深度剖析 Kimi K3 的全新架构](#item-7) ⭐️ 8.0/10
8. [应直接拒稿无可复现代码的论文](#item-8) ⭐️ 8.0/10
9. [美犯罪实验室 DNA 设备漏洞威胁 30 年证据](#item-9) ⭐️ 8.0/10
10. [英伟达 170HX 矿卡被破解：解锁 80GB 显存，价格暴涨](#item-10) ⭐️ 8.0/10
11. [苹果就英国政府 iCloud 后门要求提起法律诉讼](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Qwen 3.8-Max 发布：2.4 万亿参数，首次开源 Max 级模型](https://qwen.ai/blog?id=qwen3.8) ⭐️ 9.0/10

阿里通义千问团队正式发布 Qwen 3.8-Max，这是一款拥有 2.4 万亿参数的混合专家模型，活跃参数为 950 亿。模型权重将于下周开源，这标志着 Qwen 首次开放 Max 级模型权重。 这是 Max 级前沿规模模型首次开源，有望降低研究者和企业接触顶尖 AI 的门槛。这也表明开源权重模型能与领先闭源模型正面竞争，正在重塑更广泛的 AI 生态格局。 Qwen 3.8-Max 基于 Qwen 3.5 架构，在编码、工作、研究和长周期任务上均有提升。在编码测试中，它可自主运行超过 10 天；在 WWW2025 多模态意图识别竞赛中，它在 24 小时内击败了 526 支队伍中的 458 支。该模型现已通过 QwenCloud 提供 API 服务。

telegram · zaihuapd · 8月3日 02:31

**背景**: 混合专家（MoE）是一种让模型总参数量保持巨大、但每个 token 只激活部分参数的架构，因此推理成本主要取决于活跃参数。活跃参数包括被选中的专家和每个 token 使用到的共享部分。GPT-4、Mixtral、DeepSeek-V3 等许多现代 LLM 都采用 MoE 来提升效率，Qwen 3.8-Max 以 950 亿活跃参数延续了这一趋势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://sebastianraschka.com/faq/docs/mixture-of-experts.html">What is mixture-of-experts (MoE), and how does it differ from a dense LLM?</a></li>
<li><a href="https://aiweekly.co/learning-ai/generative-ai/what-mixture-experts-moe-how-modern-llms-get-efficient">What Is Mixture of Experts ( MoE )? How Modern LLMs ... | AI Weekly</a></li>

</ul>
</details>

**标签**: `#AI`, `#LLM`, `#Qwen`, `#open-source`, `#model release`

---

<a id="item-2"></a>
## [OpenAI 公布数学与理论计算机科学十大进展](https://openai.com/index/ten-advances-in-mathematics/) ⭐️ 8.0/10

OpenAI 发布了一篇题为“数学与理论计算机科学十大进展”的文章，重点介绍了人工智能在这些领域取得的成果。这一公告引发了关于人工智能在数学发现中作用的大规模社区讨论。 这很重要，因为它表明人工智能在数学领域的影响力日益增强，而数学传统上被认为难以自动化。社区的激烈讨论既反映了对人工智能进展呈指数级速度的兴奋，也反映了对其对研究实践影响的担忧。 该公告强调了数学和理论计算机科学领域，在这些领域中人工智能可以生成并验证解决方案。社区评论提到了高维球堆积和多色拉姆齐数等具体问题，表明这些可能是被强调的进展之一。

hackernews · milkshakes · 8月3日 16:27 · [社区讨论](https://news.ycombinator.com/item?id=49157930)

**背景**: 大型语言模型（LLM）正越来越多地应用于数学研究，它们可以生成猜想并检查证明。人工智能能力的指数级进步引发了关于下一个将被自动化的智力任务的讨论。评论中的讨论反映了关于数学实践未来以及人工智能最终是否能够解决所有可计算问题的更广泛对话。

**社区讨论**: 评论者普遍对人工智能能力的指数级增长表示惊叹，有人指出数学似乎正处在 y=2^x 的曲线上。一些人认为所有可计算问题最终都会由计算机解决，而另一些人则指出人工智能仍然无法直觉地提出新的猜想。少数人分享了关于被强调问题的直观解释，总体情绪是人工智能的影响不可否认。

**标签**: `#AI`, `#mathematics`, `#theoretical computer science`, `#OpenAI`, `#LLMs`

---

<a id="item-3"></a>
## [开发者工具必须开源：LLM 让本地修改成为现实](https://blog.exe.dev/devtools-must-be-open-source) ⭐️ 8.0/10

一篇博客文章提出，开发者工具必须开源，并声称 LLM 如今让用户阅读、修改和维护自己的分支变得切实可行。文章还设想了一些工作流程，例如用定时任务每晚将 AI 所做的本地修改变基到上游更新之上。 这将开源讨论从“用户无法维护分支”转向“AI 消除了这一障碍”，可能影响开发者工具的设计与分发方式。如果这一观点被接受，维护者可能需要更重视便于分支修改的源码结构，而非配置文件系统和插件机制。 文章似乎反对配置文件、选项和插件系统，主张用 LLM 直接修改硬编码并自动化变基流程。评论者反驳称，这种做法浪费算力、在检查代码时不可靠，而且下游与上游功能冲突会造成实际维护负担。

hackernews · bryanmikaelian · 8月3日 14:15 · [社区讨论](https://news.ycombinator.com/item?id=49156111)

**背景**: 开源开发者工具允许用户查看和修改源码，但长期以来只有少数人有时间维护自己的分支。LLM 降低了阅读、修改和变基代码的成本，重新点燃了“任何人都能修改自己所用工具”的理想。然而，专业维护者指出，分支仍会带来持续的合并、兼容性和测试工作，自动化并不能消除这些负担。

**社区讨论**: 评论者总体上对开源开发者工具持开放态度，但对 LLM 修改的观点存在分歧。Simon Willison 认为 LLM 让最初的开源理想更可行；kelnos 则称用硬编码重建替代配置既低效又浪费；theamk 警告夜间 AI 变基不可靠且难以验证；lalitmaganti 表示，考虑到真实维护成本，“一切皆分支”的做法过于理想化。

**标签**: `#open-source`, `#developer-tools`, `#LLM`, `#software-engineering`, `#community-discussion`

---

<a id="item-4"></a>
## [ComfyUI 首发支持 MiniMax H3，带来 2K 视频与原生音频](https://blog.comfy.org/p/minimax-h3-day-0-support-in-comfyui) ⭐️ 8.0/10

ComfyUI 已为首日支持 MiniMax H3，这是一款开放权重的多模态模型，能以 24fps 生成 2K 视频并自带原生音频。该集成包含权重剪枝，可将最小变体的内存占用从 123.6GB 削减 66% 至 42.5GB，使 RTX 3060 等显卡也能本地运行。 这一事件意义重大，因为 ComfyUI 是广泛使用的模块化 AI 创作引擎，首日支持让社区能立即体验这一将文本、图像、视频和音频置于同一上下文的开放权重模型。它降低了高质量 2K 视频生成的准入门槛，并增强了开放模型生态与闭源视频生成服务的竞争力。 MiniMax H3（又称 Hailuo 3.0）输出 1440p（即宣传中的 2K），固定 24fps，并可在单次请求中将文本、图像、视频和音频作为多素材参考一同处理。社区基准测试显示，在 16GB 显存的 RTX 4070 Ti Super 上生成一段 10 秒 480p 视频约需 10 分钟，而怪异或不真实的场景仍会出现明显伪影。

hackernews · vblanco · 8月3日 13:34 · [社区讨论](https://news.ycombinator.com/item?id=49155629)

**背景**: ComfyUI 是一个开源的、基于节点图的 AI 创作引擎，让用户控制模型、参数与输出。MiniMax H3 是 MiniMax 推出的通用多模态视频模型，以开放权重形式发布，意味着其最终参数可公开下载，用户可在本地运行和修改。开放权重模型介于完全闭源与完全开源 AI 之间，在不一定公开训练数据的情况下提供透明度和可定制性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://morphic.com/resources/models/minimax-h3">MiniMax H 3 (Hailuo 3.0): full specs and input limits</a></li>
<li><a href="https://fal.ai/learn/devs/minimax-h3-prompting-guide">MiniMax H 3 Prompting Guide + 44 Video Examples | fal</a></li>
<li><a href="https://github.com/Comfy-Org/ComfyUI">GitHub - Comfy -Org/ ComfyUI : The most powerful and modular...</a></li>

</ul>
</details>

**社区讨论**: 评论区整体对输出质量和速度感到惊喜，有人认为鼠标渲染效果相较当前 SOTA 模型是一大进步，但也有人在饮料广告开罐场景中看到明显的“AI 平滑”伪影。多位用户分享了实际硬件表现，例如 RTX 4070 Ti Super 生成 10 秒 480p 视频需要约 10 分钟。还有讨论围绕剪枝技术是否可用于 LLM，以及“传统特写渲染 + AI 生成广角”的混合工作流是否会成为趋势。

**标签**: `#ComfyUI`, `#MiniMax`, `#video generation`, `#open weights`, `#AI/ML`

---

<a id="item-5"></a>
## [Andy Pavlo 加入 ClickHouse，领导新实验室](https://clickhouse.com/blog/andy-pavlo-joins-clickhouse) ⭐️ 8.0/10

知名数据库研究者、卡内基梅隆大学（CMU）教授 Andy Pavlo 已加入 ClickHouse，负责新成立的 ClickHouse Labs。此举正式将学术界数据库研究与商业 OLAP 数据库公司连接起来。 这一事件意义重大，因为它将数据库领域的学术研究与产业实践连接起来，可能推动 ClickHouse 未来架构朝着研究驱动的创新方向发展。这也反映出数据库专家在学术界与领先开源公司之间流动的趋势日益明显。 ClickHouse Labs 似乎旨在探索下一代 OLAP 技术；评论区有人推测它将涉及计算与存储分离、基于 S3 的存储以及 Iceberg 等开放表格式。Pavlo 以他在 CMU 的数据库课程和对数据库架构的批判性观点而闻名，这可能会影响 ClickHouse 的技术路线图。

hackernews · nikolay\_sivko · 8月3日 14:09 · [社区讨论](https://news.ycombinator.com/item?id=49156011)

**背景**: ClickHouse 是一款开源列式 OLAP 数据库，专为在 PB 级数据集上实现高性能分析和高速数据摄入而设计。OLAP（在线分析处理）系统针对大规模数据上的复杂分析查询进行了优化，与用于事务性工作负载的 OLTP 系统相对。Andy Pavlo 是卡内基梅隆大学知名副教授，从事数据库管理系统教学与研究，他进入产业界的决定在数据库社区引起了广泛关注。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://clickhouse.com/docs/concepts/core-concepts/academic-overview">Architecture overview - ClickHouse Documentation</a></li>
<li><a href="https://en.wikipedia.org/wiki/Online_analytical_processing">Online analytical processing - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者总体上很兴奋，有人希望 Pavlo 能推动 ClickHouse 资助学术界数据库研究，因为政府资金正在减少。另一些人则讨论 ClickHouse、StarRocks 和 Trino 等 OLAP 引擎在存储与计算分离方面的融合趋势；还有观众希望他广受欢迎的 CMU 系列讲座能在 ClickHouse 的赞助下继续。另有一条玩笑评论提到 Pavlo 以“引战”而闻名。

**标签**: `#ClickHouse`, `#database`, `#OLAP`, `#research`, `#industry-academia`

---

<a id="item-6"></a>
## [Jane Street 发布 OCaml UI 库 Bonsai](https://github.com/janestreet/bonsai) ⭐️ 8.0/10

Jane Street 发布了 Bonsai，一个用于在 OCaml 中构建响应式 Web 应用的开源 UI 库。该库在 Jane Street 内部被用于几乎所有 Web 应用，从公司目录到交易系统监控工具。 Bonsai 允许开发者在前后端都使用 OCaml，从而实现全栈类型安全，这是许多函数式程序员一直期待的能力。它为 OCaml 生态中围绕 JavaScript 的前端栈提供了一个经过生产验证的替代方案。 Bonsai 部分灵感来自 Elm，并围绕类似 Incr\_dom 的 Incremental 风格 UI 框架构建。它在 opam 上以 v0.13.0 版本发布，其 API 分为多个模块，用于构建可复用的 UI 组件。

hackernews · KolmogorovComp · 8月3日 08:29 · [社区讨论](https://news.ycombinator.com/item?id=49152842)

**背景**: OCaml 是一种以安全性和性能著称的静态类型函数式语言。Bonsai 是一个 UI 库，将响应式 Web 应用开发引入 OCaml，使用 Incremental 风格系统管理动态更新。由于客户端和服务端代码都可以用 OCaml 编写，开发者可在整个技术栈共享类型和逻辑，消除许多出现在 JavaScript 边界的 bug。量化交易公司 Jane Street 已在内部所有 Web 应用中使用 Bonsai。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/janestreet/bonsai">GitHub - janestreet / bonsai : A library for building dynamic webapps...</a></li>
<li><a href="https://opam.ocaml.org/packages/bonsai/bonsai.v0.13.0/">The homepage of opam, a package manager for OCaml</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的讨论总体积极，用户对前后端都使用 OCaml 感到兴奋。一些评论者提出实际担忧——比如 Bonsai 与 Melange 的对比，或是否意味着放弃 JavaScript 生态——还有评论者指出该库性能好但默认样式不美观。另有人分享了 Jane Street 关于构建该 UI 框架的播客链接。

**标签**: `#OCaml`, `#UI framework`, `#frontend`, `#Jane Street`, `#functional programming`

---

<a id="item-7"></a>
## [SemiAnalysis 深度剖析 Kimi K3 的全新架构](https://newsletter.semianalysis.com/p/kimi-k3-the-manos-the-mythos-the) ⭐️ 8.0/10

SemiAnalysis 发布了一篇关于 Kimi K3 架构的深度技术分析，重点介绍了压缩记忆、跨深度注意力、潜在专家路由和推理性能。文章将 Kimi K3（Moonshot AI 的 2.8T 参数模型）视为大型模型设计领域的一次重要演进。 这篇分析非常重要，因为 Kimi K3 的架构选择——压缩记忆和跨深度注意力——可能改变大型模型处理长上下文和降低推理成本的方式。它让 AI 社区难得一窥超越标准 Transformer 和 MoE 设计的生产级创新。 Kimi K3 是一个 2.8T 参数模型，具备 100 万 token 的上下文窗口和原生视觉能力。其压缩记忆机制更注重速度而非精确回忆，注意力残差让每一层能够有选择地聚合来自所有先前层的信息，而潜在专家路由则通过在专家之间共享潜在空间来减少参数。

rss · Semianalysis · 8月3日 19:42

**背景**: 传统 Transformer 模型逐层处理信息，通过残差连接传递隐藏状态，而混合专家（MoE）模型通过路由函数有选择地激活部分参数。Kimi K3 在这些基础上引入了全新设计：压缩记忆模块、跨深度的注意力残差，以及将专家分解为共享潜在空间的潜在专家路由。SemiAnalysis 的文章对这些组件如何协同工作并影响推理性能进行了深入技术剖析。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.kimi.com/blog/kimi-k3">Kimi K 3 Tech Blog: Open Frontier Intelligence</a></li>
<li><a href="https://www.datacamp.com/blog/attention-residuals-explained">Attention Residuals Explained: Rethinking Transformer Depth | DataCamp</a></li>
<li><a href="https://www.emergentmind.com/topics/mixture-of-latent-experts-mole">Mixture of Latent Experts (MoLE)</a></li>

</ul>
</details>

**标签**: `#AI`, `#Machine Learning`, `#Model Architecture`, `#Kimi K3`, `#Inference`

---

<a id="item-8"></a>
## [应直接拒稿无可复现代码的论文](https://www.reddit.com/r/MachineLearning/comments/1vei12v/its_time_to_desk_reject_papers_that_dont_include/) ⭐️ 8.0/10

一位机器学习研究者在 Reddit 上发帖，称今年评审的 12 篇论文中仅 1 篇提供了完整、可复现的训练代码，并建议会议直接拒收不包含此类代码的论文。帖子指出，当前的激励机制实际上鼓励隐瞒代码以避免被拒。 该提议直指机器学习研究的可复现性危机——许多已发表的结果无法被独立验证。若 NeurIPS 等顶级会议采纳此类政策，将促使研究者共享代码，提升该领域成果的可信度。 评审者发现，在至少提供部分代码的 5 篇论文中，有 3 篇存在使结果无效的明显错误，另有 7 篇完全没有提供代码。他们认为，在评审过程中隐瞒代码几乎没有代价，这助长了不可复现论文的提交。

reddit · r/MachineLearning · /u/Flaky-Ambition5900 · 8月3日 16:17

**背景**: 直接拒稿（desk reject）指编辑或会议主席不经外部同行评审就立即拒绝稿件，通常因未达到基本要求。AUROC（受试者工作特征曲线下面积）是机器学习中常用的性能指标，用于概括模型区分不同类别的能力：1.0 为完美，0.5 相当于随机猜测。共享代码对可复现性至关重要，但许多研究者担心提供代码会暴露错误并增加被拒风险，因此选择隐瞒。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Receiver_operating_characteristic">Receiver operating characteristic - Wikipedia</a></li>
<li><a href="https://www.aischolar.com/news/article/what-is-desk-reject">What Is a Desk Reject? 6 Common Reasons &amp; How to Avoid It</a></li>

</ul>
</details>

**标签**: `#reproducibility`, `#machine learning`, `#research policy`, `#conference review`, `#code sharing`

---

<a id="item-9"></a>
## [美犯罪实验室 DNA 设备漏洞威胁 30 年证据](https://www.wsj.com/tech/cybersecurity/security-flaw-placed-30-years-of-dna-evidence-at-risk-of-hacking-1932775a) ⭐️ 8.0/10

安全研究人员发现，美国多数犯罪实验室使用的 DNA 分析仪器存在漏洞，可对 1995 年以来的 DNA 证据文件进行不留痕迹的篡改。设备制造商 Thermo Fisher Scientific 于 7 月私下承认该漏洞，并于上周五发布高危安全公告，推出加入数字签名的软件更新。 此事意义重大，因为被篡改的 DNA 证据可能动摇数十年的刑事定罪和审理中案件，影响美国司法体系的公信力。这也凸显出法医仪器往往缺乏统一监管，正成为网络攻击的目标。 测试中，研究人员借助 Anthropic 的 Claude AI 软件，约 45 分钟即可修改 DNA 扫描文件，且不会触发常用分析软件的警报。Thermo Fisher 正与美国网络安全和基础设施安全局（CISA）合作，目前尚无漏洞被实际利用的报告。

telegram · zaihuapd · 8月3日 05:15

**背景**: 法医 DNA 分析依赖 Thermo Fisher 的 Applied Biosystems 基因分析仪等设备，这些设备进行 STR 片段分析，用于人类身份识别。这些仪器生成的 DNA 图谱会作为法庭证据，因此文件完整性至关重要。数字签名有助于验证证据文件未被篡改，在法律场景中提供真实性和不可否认性。然而，全美 200 多家犯罪实验室缺乏统一安全监管，防护存在差距。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Forensic_DNA_analysis">Forensic DNA analysis - Wikipedia</a></li>
<li><a href="https://www.thermofisher.com/us/en/home/industrial/forensics/human-identification/forensic-dna-analysis/dna-analysis.html">DNA Analysis | Thermo Fisher Scientific - US</a></li>
<li><a href="https://honorstead.com/authentication-and-digital-signatures/">Understanding Authentication and Digital Signatures in... - Honorstead</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#DNA forensics`, `#vulnerability`, `#Thermo Fisher`, `#evidence integrity`

---

<a id="item-10"></a>
## [英伟达 170HX 矿卡被破解：解锁 80GB 显存，价格暴涨](https://finance.sina.com.cn/tech/roll/2026-08-03/doc-inikzqsf4659769.shtml) ⭐️ 8.0/10

亚利桑那州立大学的研究人员公开披露了一个漏洞利用方法，绕过了英伟达 CMP 170HX 矿卡的 OTP 熔丝锁定，将显存提升至 80GB，FP32 算力解锁至 94 TFLOPS。消息传出后，该卡二手价从 300-500 元飙升至 3000-4000 元，海外市场甚至叫价 1500 美元。 这是一次重大的硬件安全突破，因为它把一张基于与 A100 相同 GA100 核心、但被刻意限制的廉价矿卡，变成了一款高显存 AI 计算设备。它可能让更多 AI 研究人员和爱好者用上大显存 GPU，同时也对英伟达的硬件锁定机制提出了严峻问题。 该漏洞利用 Falcon 安全协处理器的栈溢出漏洞劫持特权控制，并逐一修改那些英伟达通过一次性可编程（OTP）熔丝固化的寄存器。国内社区成员已在 Windows 和 Linux 下验证解锁卡可运行 AI 图像生成和大语言模型推理，但长期稳定性及不同批次的解锁上限仍存风险。

telegram · zaihuapd · 8月3日 11:29

**背景**: CMP 170HX 是英伟达 2021 年推出的加密货币矿卡，基于阉割版 GA100 GPU，配备 10GB HBM2e 显存并锁定了 PCIe 1.0，同时通过不可逆的 OTP 熔丝大幅限制计算和显示功能。OTP 熔丝在编程后以物理方式防止更改，使该卡的性能限制看似永久。Falcon 微处理器是英伟达诸多设备（包括任天堂 Switch）中的安全协处理器，如今被证明是一个可利用的攻击面。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://marketangroup.com/product/nvidia-cmp-170hx-164mh-s-pro-mining-205w/">NVIDIA CMP 170 HX 164MH/s Pro Mining 205W – MARKETANG...</a></li>
<li><a href="https://www.ersaelectronics.com/blog/one-time-programmable-otp-memory">One-Time Programmable (OTP) Memory Guide</a></li>
<li><a href="https://www.resetera.com/threads/nvidia-security-co-processor-in-nintendo-switch-and-billions-of-other-devices-has-been-cracked.103006/">nVidia security co-processor (in Nintendo Switch and billions of ...</a></li>

</ul>
</details>

**标签**: `#hardware-security`, `#GPU`, `#AI-compute`, `#exploit`, `#Nvidia`

---

<a id="item-11"></a>
## [苹果就英国政府 iCloud 后门要求提起法律诉讼](https://www.ft.com/content/2cc9c96a-0e5b-4c33-a95a-3d11072a145c?syn-25a6b1a6=1) ⭐️ 8.0/10

苹果已向英国调查权力法庭提起法律申诉，挑战政府要求其开放加密 iCloud 云备份的「技术能力通知」。此举发生在苹果于 2025 年 2 月在英国下架 iCloud 高级数据保护功能之后。 此案可能为政府能否强制科技公司削弱端到端加密树立法律先例。裁决将影响全球用户的隐私与安全，因为为一国设计的后门可能会破坏全球对苹果加密体系的信任。 英国政府在美国反对后曾撤回最初的技术能力通知，随后又发出仅针对英国用户的新通知。隐私组织 Privacy International 和 Liberty 也分别提起了申诉，法庭已定于下月举行案件管理听证。

telegram · zaihuapd · 8月3日 15:40

**背景**: 调查权力法庭是英国处理公共机构监控投诉的司法机构。根据 2016 年《调查权力法》发布的技术能力通知，可强制公司构建或维持响应合法数据请求的技术能力。苹果的高级数据保护功能将端到端加密扩展至更多 iCloud 数据类别，意味着苹果不再持有解密密钥，无法访问用户数据；而后门要求则意味着苹果必须保留密钥，从而削弱所有用户的安全性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Investigatory_Powers_Tribunal">Investigatory Powers Tribunal - Wikipedia</a></li>
<li><a href="https://www.legislation.gov.uk/ukdsi/2018/9780111163610">The Investigatory Powers (Technical Capability) Regulations 2018</a></li>
<li><a href="https://support.apple.com/en-us/108756">How to turn on Advanced Data Protection for iCloud - Apple Support</a></li>

</ul>
</details>

**标签**: `#Apple`, `#Encryption`, `#Backdoor`, `#Privacy`, `#Security`

---
---
layout: default
title: "Horizon Summary: 2026-07-28 (ZH)"
date: 2026-07-28
lang: zh
---

> 从 29 条内容中筛选出 11 条重要资讯。

---

1. [月之暗面开源 Kimi K3：全球首个 2.8 万亿参数模型](#item-1) ⭐️ 10.0/10
2. [Anthropic 阐明对开源权重模型的立场](#item-2) ⭐️ 9.0/10
3. [Fastjson2 被发现严重远程代码执行漏洞，所有版本受影响](#item-3) ⭐️ 9.0/10
4. [中国开始量产国产 DUV 光刻机](#item-4) ⭐️ 9.0/10
5. [vLLM v0.26.0 发布，支持 Inkling、DeepSeek-V4 等](#item-5) ⭐️ 8.0/10
6. [法官驳回谷歌基于 DMCA 的抓取诉讼](#item-6) ⭐️ 8.0/10
7. [Misago 论坛弃用 React 改用 HTMX](#item-7) ⭐️ 8.0/10
8. [Paged Out 第九期：社区技术杂志发布](#item-8) ⭐️ 8.0/10
9. [前沿大模型在 8 个基准测试中均呈现左倾政治偏见](#item-9) ⭐️ 8.0/10
10. [谷歌透露 Gemini 4 为迄今最大规模预训练项目](#item-10) ⭐️ 8.0/10
11. [阿里推出千问办公 AI 平台](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [月之暗面开源 Kimi K3：全球首个 2.8 万亿参数模型](https://huggingface.co/moonshotai/Kimi-K3) ⭐️ 10.0/10

月之暗面（Moonshot AI）发布了 Kimi K3 模型的权重，该模型总参数量达 2.8 万亿，激活参数为 104B，是全球首个开源的 3T 级别模型。它采用了 Kimi Delta Attention 与 Attention Residuals 新架构，支持多模态理解和 100 万 token 上下文窗口，性能与 GPT-5.6、Claude Fable 5 等前沿模型互有胜负。 开源一个 2.8 万亿参数级别的模型极大地推动了开源 AI 的发展，让研究人员和开发者能够获得与专有前沿模型相当的能力。这将加速长上下文推理、自主任务和多模态应用等领域的创新。 Kimi K3 采用 Stable LatentMoE，共有 896 个专家，每 token 激活 16 个，扩展效率较 Kimi K2 提升约 2.5 倍。模型支持 MXFP4 量化，并采用 Kimi K3 许可协议，要求年收入超过 2000 万美元的大型模型即服务（MaaS）企业另行签订协议。

telegram · zaihuapd · 7月27日 15:15

**背景**: 混合专家模型（MoE）是一种神经网络架构，通过多个“专家”子网络扩展模型容量，每次只激活一部分以保持计算效率。Kimi K3 基于月之暗面之前的 Kimi K2 模型，引入了新的注意力机制：Kimi Delta Attention（KDA）通过每通道衰减扩展了门控 DeltaNet，改进了记忆管理；Attention Residuals（AttnRes）用学习到的对前层输出的注意力替代了标准残差连接，改进了表征聚合。Stable LatentMoE 进一步增强了稀疏性和路由稳定性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2510.26692">Kimi Linear: An Expressive, Efficient Attention Architecture</a></li>
<li><a href="https://arxiv.org/abs/2603.15031">[2603.15031] Attention Residuals</a></li>

</ul>
</details>

**社区讨论**: Simon Willison 博客上的社区注意到许可协议的变化：K3 许可不再自称“修改版 MIT”，而是要求大型 MaaS 企业另行签订协议。社区赞赏月之暗面始终使用“开放权重”而非“开源”一词。OpenRouter 上的定价与月之暗面相同，为每百万输入 token 3 美元、每百万输出 token 15 美元。

**标签**: `#AI`, `#Open Source`, `#Large Language Model`, `#MoE`, `#Multimodal`

---

<a id="item-2"></a>
## [Anthropic 阐明对开源权重模型的立场](https://www.anthropic.com/news/position-open-weights-models) ⭐️ 9.0/10

Anthropic 发布了一项政策声明，主张对所有足够强大的 AI 模型（包括开源权重模型）进行强制性安全测试，同时声称从未支持全面禁止开源权重模型。 这一立场可能通过将安全测试塑造成折中方案来影响 AI 监管辩论，但批评者认为，成本高昂或选择性执行的测试要求实际上禁止了开源权重模型，从而影响开源 AI 开发和研究。 Anthropic 明确支持三项措施：防止向中国出口先进 AI 芯片、对前沿模型进行强制性安全测试、以及政府对 AI 训练使用的计算和能源进行限制。该公司强调，测试应平等适用于开放和封闭模型。

hackernews · surprisetalk · 7月27日 22:03 · [社区讨论](https://news.ycombinator.com/item?id=49076057)

**背景**: 开源权重模型是指其训练参数公开发布的 AI 模型，任何人都可以下载、运行和微调。它们提高了透明度和创新，但也引发了滥用担忧，因为可以在没有监督的情况下部署。Anthropic 的声明回应了开源社区对无限制访问的渴望与日益增长的安全监管呼声之间的矛盾。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>
<li><a href="https://opensource.org/ai/open-weights">Open Weights: not quite what you’ve been told</a></li>
<li><a href="https://telnyx.com/resources/open-weight-models">Open Weight Models What They Are and How to Use Them</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的社区评论充满怀疑。许多人认为，强制性安全测试，尤其是如果由单一实体控制或成本过高，实际上是变相禁止开源权重模型。其他人指责 Anthropic 虚伪，一方面支持芯片出口禁令，一方面声称不主张禁令，暗示其真正动机是商业保护主义而非安全。

**标签**: `#AI safety`, `#open-weights`, `#regulation`, `#Anthropic`, `#AI policy`

---

<a id="item-3"></a>
## [Fastjson2 被发现严重远程代码执行漏洞，所有版本受影响](https://mp.weixin.qq.com/s/LJaul1jNjK9pXRAkoUiMEA) ⭐️ 9.0/10

长亭科技于 2026 年 7 月 27 日披露了 Fastjson2 中的远程代码执行（RCE）漏洞，影响 2.0.62 及之前的所有版本。攻击者可通过恶意 JSON 数据绕过 AutoType 类型校验并执行任意代码，目前官方尚未发布补丁。 作为 Java 生态中使用最广泛的 JSON 库之一，该漏洞对数以万计的应用和服务构成严重威胁。由于攻击者可轻易利用此漏洞获取系统完全控制权，必须立即采取缓解措施，例如彻底禁用 AutoType 功能。 该漏洞影响所有已发布的 Fastjson2 版本，最新受影响的版本为 2.0.62。维护者已关闭了 Pull Request \#7695 并未合入主分支，且已确认该安全问题，但尚未提供任何正式补丁。

telegram · zaihuapd · 7月27日 10:31

**背景**: Fastjson2 是阿里巴巴开发的 Java 高性能 JSON 库，提供 AutoType 功能可在反序列化时自动解析类型。AutoType 允许在 JSON 解析过程中自动实例化类，若未严格控制则可能被利用。该库此前有类似漏洞历史——本月早些时候，较旧的 Fastjson 1.x 系列也曝出了类似的 RCE 漏洞。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://alibaba.github.io/fastjson2/autotype_cn.html">FASTJSON 2 Autotype机制介绍 | fastjson2</a></li>
<li><a href="https://github.com/alibaba/fastjson2">GitHub - alibaba/fastjson2: 🚄 FASTJSON2 is a Java JSON library with excellent performance.</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerability`, `#fastjson2`, `#rce`, `#java`

---

<a id="item-4"></a>
## [中国开始量产国产 DUV 光刻机](https://www.theinformation.com/articles/china-starts-mass-producing-homegrown-duv-chipmaking-tools-advance-local-chip-industry) ⭐️ 9.0/10

中国已开始大规模生产自主研发的浸没式深紫外（DUV）光刻机，计划今年生产约 5 台，2027 年达到约 20 台。 这标志着半导体制造领域的突破性进展，直接挑战 ASML 的市场主导地位，并可能在地缘政治紧张局势下重塑全球芯片供应链。 国产 DUV 设备在性能和可靠性上仍落后于 ASML，芯片厂需要数月测试。部分关键部件来自日本，今年本地供应链延误已影响进度。

telegram · zaihuapd · 7月27日 14:10

**背景**: 深紫外（DUV）光刻技术使用波长为 248nm 或 193nm 的准分子激光来刻画集成电路。浸没式光刻通过用液体（通常是水）替代镜头与晶圆之间的空气间隙来提高分辨率。ASML 目前主导着先进光刻市场，但西方的出口限制促使中国自主研发设备。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DUV_lithography">DUV lithography</a></li>
<li><a href="https://en.wikipedia.org/wiki/Immersion_lithography">Immersion lithography</a></li>

</ul>
</details>

**标签**: `#semiconductor`, `#lithography`, `#DUV`, `#China`, `#ASML`

---

<a id="item-5"></a>
## [vLLM v0.26.0 发布，支持 Inkling、DeepSeek-V4 等](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 8.0/10

vLLM v0.26.0 新增了对 Inkling 模型家族的全面支持、DeepSeek-V4 的性能优化、通过 head\_dtype 实现的 fp32 lm\_head，以及可按 KV-cache 组选择注意力后端的灵活设计。本次发布包含 212 位贡献者提交的 411 个提交。 vLLM 是一个广泛使用的 LLM 推理引擎，本次发布带来了显著的性能提升和新型号支持，特别是针对前沿的 Inkling（975B MoE）和 DeepSeek-V4 模型。灵活的注意力后端和 fp32 lm\_head 提高了混合模型的准确性和适应性，惠及开发者和最终用户。 Inkling 支持包括分块 CUDA 图、Hopper FA4 相对注意力、MTP=1 推测解码、LoRA 以及 ModelOpt NVFP4 量化。DeepSeek-V4 优化包括专用路由内核（端到端 TPOT 提升 2.94%）、fused\_topk\_bias（1.5–2 倍加速）以及用于 HCA 预填充的 ROCm 两阶段压缩器。

github · khluu · 7月27日 01:06

**背景**: vLLM 是一个开源的高吞吐量 LLM 推理引擎，专为高效服务大型语言模型而设计。Inkling 模型是一个 975B 参数的混合专家（MoE）Transformer，具有 41B 活跃参数，支持高达 1M 标记的上下文。FlashAttention-4（FA4）是一个针对 NVIDIA Hopper GPU 优化的新注意力算法，而 NVFP4 是 NVIDIA 的一种 4 位量化格式，可减少内存占用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thinkingmachines.ai/news/introducing-inkling/">Inkling: Our Open-Weights Model - Thinking Machines Lab</a></li>
<li><a href="https://modal.com/blog/reverse-engineer-flash-attention-4">We reverse-engineered Flash Attention 4</a></li>
<li><a href="https://nvidia.github.io/TensorRT-LLM/features/quantization.html">Quantization — TensorRT LLM</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM inference`, `#release`, `#machine learning`, `#performance`

---

<a id="item-6"></a>
## [法官驳回谷歌基于 DMCA 的抓取诉讼](https://www.techdirt.com/2026/07/27/judge-rejects-googles-attempt-to-dmca-its-way-out-of-being-scraped/) ⭐️ 8.0/10

一名联邦法官裁定，谷歌不能利用《数字千年版权法》（DMCA）来阻止第三方抓取其搜索结果，驳回了该公司关于抓取构成版权侵权的论点。 这一裁决开创了法律先例，限制了利用版权法控制互联网数据访问的行为，可能影响科技公司如何保护其公开数据，并影响网页抓取的未来发展。 该案涉及谷歌与抓取其搜索结果的 SerpAPI 公司。法官认为，搜索结果是事实汇编，可能达不到美国法律中版权保护所需的原创性门槛。

hackernews · cdrnsf · 7月27日 18:15 · [社区讨论](https://news.ycombinator.com/item?id=49073513)

**背景**: 网页抓取是从网站自动提取数据的行为。DMCA 是美国一项法律，将规避保护版权作品的技术措施定为犯罪。谷歌曾辩称，抓取其搜索结果违反了 DMCA，但法院不同意。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DMCA">DMCA</a></li>
<li><a href="https://en.wikipedia.org/wiki/Web_scraping">Web scraping</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍支持该裁决，指出讽刺的是谷歌自身的业务依赖于抓取开放网络。一些人批评谷歌在移除其搜索 API 的同时起诉填补空白的第三方。还有人讨论了欧盟与美国在数据库版权保护方面的差异。

**标签**: `#legal`, `#web scraping`, `#copyright`, `#Google`, `#DMCA`

---

<a id="item-7"></a>
## [Misago 论坛弃用 React 改用 HTMX](https://misago-project.org/t/removing-reactjs-from-the-codebase-and-adapting-htmx-for-ui-interactivity/1267/) ⭐️ 8.0/10

Misago 论坛项目从代码库中移除了 React.js，转而采用 HTMX 实现 UI 交互，理由是性能提升和简化开发。 这一迁移反映了 Web 开发中向更简单的服务端渲染 UI 的趋势，采用 HTMX 等超媒体驱动方法，降低了客户端复杂性。 HTMX 通过自定义属性扩展 HTML，实现 AJAX 动态更新而无需编写 JavaScript。此论坛的转变是脱离重型前端框架的日益增长趋势的一部分。

hackernews · Ralfp · 7月27日 09:58 · [社区讨论](https://news.ycombinator.com/item?id=49067301)

**背景**: HTMX 是一个开源 JavaScript 库，允许开发者使用 HTML 属性创建动态网页，避免复杂的 JavaScript 框架。它由 Carson Gross 创建，作为 intercooler.js 的后继者。Misago 论坛项目是一个现代论坛软件，最初使用 React 进行交互元素开发。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Htmx">Htmx</a></li>
<li><a href="https://htmx.org/">htmx - high power tools for html</a></li>
<li><a href="https://github.com/bigskysoftware/htmx">GitHub - bigskysoftware/ htmx : htmx - high power tools for HTML</a></li>

</ul>
</details>

**社区讨论**: 社区评论显示了对 HTMX 在论坛场景中的支持，用户分享了积极经验，并建议将 HTMX 与 TailwindCSS 或 DaisyUI 搭配使用。部分用户注意到在高交互功能（如可筛选产品列表）中的局限性。

**标签**: `#HTMX`, `#React`, `#web development`, `#server-side rendering`, `#frontend framework`

---

<a id="item-8"></a>
## [Paged Out 第九期：社区技术杂志发布](https://pagedout.institute/download/PagedOut_009.pdf) ⭐️ 8.0/10

Paged Out 第九期，一本涵盖底层黑客技术的社区驱动杂志，已作为免费 PDF 从 pagedout.institute 发布。 它延续了深度、黑客好奇内容的传统，与底层编程和安全社区产生共鸣，提供诸如子像素渲染和可计算拼贴等多样主题。 该杂志包含诸如 &\#x27;C 语言婴儿步&\#x27; 和 &\#x27;子像素动物园&\#x27; 等文章，并重新发现了王浩 1960 年代关于可计算拼贴的工作，将多米诺问题与停机问题联系起来。

hackernews · laurensr · 7月27日 14:22 · [社区讨论](https://news.ycombinator.com/item?id=49070138)

**背景**: Paged Out 是一本社区驱动的技术杂志（zine），专注于底层编程、黑客和计算机科学主题。它定期发布并以 PDF 格式免费分发，也可购买印刷版。

**社区讨论**: 评论者称赞该杂志的深度和设计，有人将其比作现代的 2600 或 Phrack。另一人指出未加引用的王浩成果的重新发现，展示了停机问题与多米诺问题的等价性。

**标签**: `#hacker-culture`, `#zine`, `#low-level`, `#technical-writing`, `#programming`

---

<a id="item-9"></a>
## [前沿大模型在 8 个基准测试中均呈现左倾政治偏见](https://www.reddit.com/r/MachineLearning/comments/1v8fnzw/evaluated_6_frontier_llms_gpt54_claude_sonnet_46/) ⭐️ 8.0/10

一项针对六个前沿大模型的独立评估（GPT-5.4、Claude Sonnet 4.6、Claude Opus 4.7、Gemini Pro/Flash、Grok 4.3），在 8 个偏见基准测试（约 20600 个样本）中发现，所有模型在行为上均呈现左倾政治偏见，包括自称右倾的 Grok。 这项研究揭示了主流商业和开源大模型在政治倾向上存在系统性偏见，可能影响其在内容审核、政策分析和公平决策等敏感场景中的部署。同时，它挑战了模型声称的政治倾向与其实际行为相符的假设。 值得注意的是，Grok 自称右倾，但在内容分类或回答政策问题时表现出左倾行为；而模型在种族相关问题上拒绝回答的比例差异显著（GPT-5.4 拒绝率为 20.3%，Claude Opus 4.7 为 13.8%）。该研究为单人非同行评审项目，存在局限性，例如未进行多次运行平均以及每项任务仅使用单一提示模板。

reddit · r/MachineLearning · /u/marggggggggg · 7月27日 22:37

**背景**: 偏见基准测试是用于衡量语言模型中不良社会偏见的标准化数据集，例如刻板印象、偏见或不公平关联。常见的基准包括 WinoBias（性别）、BBQ（种族/族裔）、SeeGULL（地理文化刻板印象）、OpinionsQA（与人口统计意见的一致性）以及政治偏见数据集（如政治指南针和超党派新闻）。本研究使用了八个此类数据集，评估政治、性别和种族维度上的显性和隐性偏见。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/google-research-datasets/seegull">GitHub - google-research- datasets / seegull : SeeGULL is...</a></li>
<li><a href="https://huggingface.co/datasets/cajcodes/political-bias">cajcodes / political - bias · Datasets at Hugging Face</a></li>
<li><a href="https://arxiv.org/abs/2303.17548">[2303.17548] Whose Opinions Do Language Models Reflect?</a></li>

</ul>
</details>

**标签**: `#bias evaluation`, `#LLM alignment`, `#political bias`, `#fairness benchmarks`, `#frontier models`

---

<a id="item-10"></a>
## [谷歌透露 Gemini 4 为迄今最大规模预训练项目](https://9to5google.com/2026/07/26/google-gemini-4-teases/) ⭐️ 8.0/10

谷歌 CEO Sundar Pichai 在 Alphabet 2026 年第二季度财报电话会议上宣布，下一代旗舰 AI 模型 Gemini 4 已投入训练，这是该公司迄今为止最具雄心的预训练项目，预计 2026 年底发布。 这一公告表明谷歌致力于扩大 AI 模型规模以保持在 AI 前沿竞争中的优势，可能带来能力上的重大突破。Gemini 4 的发布将影响整个 AI 生态系统，包括依赖谷歌 AI 服务的开发者、企业和最终用户。 Pichai 强调将优先把算力分配给前沿 AGI 研发，确保 Gemini 4 发布时仍处行业前沿。此外，Gemini 3.x Flash 系列将保持几乎每月一次的迭代频率，重点提升智能编码等能力。

telegram · zaihuapd · 7月27日 04:06

**背景**: Gemini 是 Google DeepMind 开发的多模态大语言模型系列，于 2023 年 12 月发布，作为 LaMDA 和 PaLM 2 的继任者。预训练是训练大型语言模型的初始阶段，模型从包含数万亿 token 的大规模多样化数据集中学习。AGI（通用人工智能）是指一种假设的 AI，能够在几乎所有认知任务上达到或超越人类水平。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Gemini_%28AI_model%29">Gemini (AI model)</a></li>
<li><a href="https://www.moveworks.com/us/en/resources/ai-terms-glossary/pre-training">What is Pre-Training? - Moveworks</a></li>
<li><a href="https://en.wikipedia.org/wiki/Artificial_general_intelligence">Artificial general intelligence - Wikipedia</a></li>

</ul>
</details>

**标签**: `#Google`, `#Gemini 4`, `#AI`, `#Large Language Model`, `#Pre-training`

---

<a id="item-11"></a>
## [阿里推出千问办公 AI 平台](https://qwenwork.cn/) ⭐️ 8.0/10

阿里巴巴推出了‘千问办公’Beta 版，这是一站式 AI 办公平台，用户可通过自然语言生成和编辑文档、表格、PPT、网页、代码及多媒体内容。桌面端还提供电脑操控功能，利用浏览器自动化和 Computer Use 特性跨应用执行点击、输入、数据提取等操作。 此次发布标志着科技巨头正式进军 AI 生产力市场，可能加剧与腾讯、字节跳动等中国科技公司的竞争。该平台将文档生成与电脑操控相结合，是向自主 AI 代理直接与操作系统交互迈出的一步，有望重新定义办公流程。 该平台覆盖网页、Windows 和 macOS 客户端，并接入钉钉。定价包含免费版，个人标准版连续包月 78 元（2000 积分），高级版 158 元（4000 积分）。新用户限时获赠 2000 积分，有效期 90 天。电脑操控功能可能截取屏幕内容或执行不可撤销操作，默认会在操作前征求用户确认。

telegram · zaihuapd · 7月27日 05:45

**背景**: AI 办公平台利用大语言模型自动化文档创建和编辑。‘Computer Use’指 AI 系统直接控制计算机界面，模拟人类点击、输入等操作。阿里该平台整合了 QoderWork、悟空和 MuleRun 三款 AI 产品，瞄准企业生产力市场。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://phemex.com/news/article/alibaba-launches-qianwen-office-to-unify-ai-agent-office-platforms-94023">Alibaba Unveils &#x27;Qianwen Office&#x27; to Consolidate AI Platforms ...</a></li>
<li><a href="https://x.com/thexpin/status/2079518147812495634">According to Caijing, Alibaba is preparing to launch Qianwen Office ...</a></li>
<li><a href="https://www.webull.com/news/15263087389402112">It is reported that Ali will launch Qianwen Office. It has integrated ...</a></li>

</ul>
</details>

**标签**: `#AI office`, `#Alibaba`, `#document generation`, `#computer control`, `#productivity`

---
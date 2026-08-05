---
layout: default
title: "Horizon Summary: 2026-08-05 (ZH)"
date: 2026-08-05
lang: zh
---

> 从 39 条内容中筛选出 11 条重要资讯。

---

1. [Keyv 及相关 npm 包遭 Shai-Hulud 供应链攻击](#item-1) ⭐️ 9.0/10
2. [我国首部 L3/L4 自动驾驶强制性国家标准发布](#item-2) ⭐️ 9.0/10
3. [Mistral 发布 Shieldstral：3B 开放权重多模态内容审核模型](#item-3) ⭐️ 8.0/10
4. [自研色彩空间与算法，生成多样肤色](#item-4) ⭐️ 8.0/10
5. [DeepSeek V4 Flash 在单块 AMD MI300X 上高效运行](#item-5) ⭐️ 8.0/10
6. [联邦快递式钓鱼邮件正在削弱用户的安全意识](#item-6) ⭐️ 8.0/10
7. [Oxide Computer 完成 4.45 亿美元 D 轮融资](#item-7) ⭐️ 8.0/10
8. [LLM 0.32 新增推理痕迹、服务端工具和更智能的日志功能](#item-8) ⭐️ 8.0/10
9. [MiniMax-H3 全能模态视频模型通过 MLX 在 Apple Silicon 上本地运行](#item-9) ⭐️ 8.0/10
10. [谷歌为 Anthropic 搭建 2000 亿美元华尔街融资机器](#item-10) ⭐️ 8.0/10
11. [特朗普政府拟起草禁令，禁止进口中国数据中心光模块](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Keyv 及相关 npm 包遭 Shai-Hulud 供应链攻击](https://www.aikido.dev/blog/keyv-and-friends-compromised-in-npm-supply-chain-attack) ⭐️ 9.0/10

Keyv 及多个相关 npm 包在正在进行的 Shai-Hulud 供应链攻击中被入侵。该攻击利用开源组件的信任，通过网络包之间的依赖关系进行传播。 Keyv 是一个广泛使用的键值存储库，支持多种数据库后端，因此其被入侵可能会影响大量下游项目。此次事件表明，自动化、可自我传播的恶意软件正成为开源软件生态系统的严重威胁。 Shai-Hulud 蠕虫结合了令牌窃取、暴露私有代码仓库和自动化传播；据报道，它在 22 分钟内批量投毒了 317 个包、637 个版本。被入侵的 Keyv 包仍是活跃风险，开发者应检查依赖并尽量移除安装钩子。

hackernews · cimi\_ · 8月4日 11:01 · [社区讨论](https://news.ycombinator.com/item?id=49166874)

**背景**: Keyv 是一个 npm 库，通过存储适配器为多种后端提供一致的键值存储接口，常用于缓存和持久化存储。Shai-Hulud 是最近发现的一种 npm 供应链蠕虫，它通过包之间的依赖关系传播，并窃取云凭证和机密信息。供应链攻击通过破坏受信任的开源组件，渗透到依赖它们的下游应用中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/jaredwray/keyv">GitHub - jaredwray/keyv: Simple key-value storage with support for multiple backends · GitHub</a></li>
<li><a href="https://www.reversinglabs.com/blog/shai-hulud-worm-npm">Shai - Hulud npm supply chain attack : What you need to know | RL Blog</a></li>
<li><a href="https://slowmist.medium.com/threat-intelligence-shai-hulud-supply-chain-poisoning-cloud-credential-theft-and-1b8a3a4edd12">Threat Intelligence | Shai - Hulud Supply Chain Poisoning... | Medium</a></li>

</ul>
</details>

**社区讨论**: 社区成员提出了实用的防御措施，例如封禁新的 pre-install 和 post-install 钩子、采用 devcontainer 进行隔离开发，以及使用 Packj 等工具检测恶意包行为。一些人表达了对脆弱的依赖系统的担忧，并指出清理工作很困难，因为攻击者会迅速利用每个被入侵的仓库。还有少数人质疑 GitHub 为何不能主动检测并封禁该蠕虫使用的数据外泄仓库。

**标签**: `#security`, `#supply-chain`, `#npm`, `#open-source`, `#malware`

---

<a id="item-2"></a>
## [我国首部 L3/L4 自动驾驶强制性国家标准发布](https://wap.miit.gov.cn/jgsj/zbys/qcgy/art/2026/art_a1d2072374884287b67048a77560014e.html) ⭐️ 9.0/10

工业和信息化部发布了 GB 44721-2026《智能网联汽车 自动驾驶系统安全要求》，这是我国首部针对 L3 级有条件自动驾驶和 L4 级高度自动驾驶系统的强制性国家标准。该标准将于 2027 年 7 月 1 日起实施。 这是一项重要的监管里程碑，将 L3/L4 系统的安全要求从推荐性转变为强制性，为中国的汽车制造商和技术供应商确立了具有约束力的安全基线。它将影响全球最大汽车市场中的车辆设计、营销、保险和责任认定框架。 该标准适用于搭载 L3/L4 系统的 M 类（载客）和 N 类（载货）车辆，不适用于自动泊车系统。标准要求自动驾驶系统的安全水平至少达到合格且专注驾驶人的水平，并从企业全生命周期安全保障、系统动态驾驶能力、人机交互与用户告知、多维度检验检测四个维度构建安全要求体系。

telegram · zaihuapd · 8月4日 13:06

**背景**: 自动驾驶等级通常由 SAE International 定义。L3 级（有条件自动驾驶）允许驾驶员在系统请求时接管，无需持续监控；L4 级（高度自动驾驶）则能在大多数情况下无需人工干预。根据中国的车辆分类标准，M 类车辆用于载客，N 类车辆用于载货，均为至少四轮的机动车。此次强制性国标是对 2024 年推荐性国标的系统性升级，体现了中国为智能网联汽车建立有约束力法律框架的努力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.autohome.com.cn/news/202608/1316205.html">autohome.com.cn/news/202608/1316205.html</a></li>
<li><a href="https://www.yiche.com/baike/356387.htm">自动驾驶级别l3和l4有什么区别_易车百科</a></li>

</ul>
</details>

**标签**: `#autonomous-driving`, `#regulation`, `#standards`, `#China`, `#safety`

---

<a id="item-3"></a>
## [Mistral 发布 Shieldstral：3B 开放权重多模态内容审核模型](https://mistral.ai/news/shieldstral/) ⭐️ 8.0/10

Mistral 发布了 Shieldstral，一个专为内容审核设计的 30 亿参数开放权重多模态安全分类模型。该模型采用 Apache 2.0 许可，性能优于体积最高达其 7 倍的模型，并且可在单个 16GB NVIDIA GPU 上运行。 这使小型平台和开发者能够以低成本获得可自托管的审核方案，减少对昂贵商业 API 的依赖。同时也表明 Mistral 正转向针对特定用途的较小微调模型，而非仅在前沿大模型上竞争。 Shieldstral 支持多模态（文本和图像），权重可在 Hugging Face 上获取：mistralai/Shieldstral-1.0-3B。由于是开放权重，用户可以下载、检查并微调模型；不过 AI 输出具有非确定性，敏感场景仍可能需要人工复核。

hackernews · riadsila · 8月4日 16:36 · [社区讨论](https://news.ycombinator.com/item?id=49171268)

**背景**: 内容审核是对用户生成的文本、图片和视频进行筛查以发现违反政策内容的过程，这是社交和图片分享平台面临的一项重大挑战。开放权重模型是指训练后的参数公开发布的人工智能模型，任何人都可以在自己的基础设施上运行、修改和微调。多模态审核结合了对多种内容类型的分析，是一个活跃的研究领域，相关研讨会和基准专注于上下文感知和文化敏感的类别判断。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mistral.ai/news/shieldstral/">Introducing Shieldstral . | Mistral AI</a></li>
<li><a href="https://scalevise.com/resources/mistral-shieldstral-on-device-content-safety-model/">Mistral Shieldstral : On-Device Content Safety Model</a></li>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>

</ul>
</details>

**社区讨论**: 评论者总体上欢迎这一发布，认为它是适合小型平台的实用且低成本的审核工具。讨论聚焦于该模型能否在不重新训练的情况下调整到任意的审核规则集，以及与 OpenAI 的 omni-moderation API 相比表现如何；还有评论者开玩笑建议命名为&\#x27;Safestral&\#x27;。

**标签**: `#AI`, `#content moderation`, `#Mistral`, `#open-weights`, `#multimodal`

---

<a id="item-4"></a>
## [自研色彩空间与算法，生成多样肤色](https://toneyalexander.github.io/inclusive-color-space/) ⭐️ 8.0/10

一位开发者发布了一个交互式项目，介绍了一种定制的色彩空间和程序化生成算法，旨在让数字艺术和游戏开发中选取多样、合理的肤色变得更加容易。页面包含演示、JavaScript 实现以及关于如何构建该色彩空间的详细技术说明。 该项目为数字艺术家和游戏开发者面临的一个实际问题提供了实用、易用的解决方案：无需深厚的色彩科学知识即可生成包容、自然的肤色。它还引发了关于色彩空间如何更好地表现人类多样性的更广泛讨论，可能影响未来在艺术、设计和图形领域中的工具。 该方法涉及统计分析（包括类似 PCA 的技术）来定义肤色的二维基底，然后通过手动拟合函数创建一个平滑、可导航的色彩空间。作者承认这种方法基于经验，并在“未来工作”部分列出了可能的改进；评论者指出，生成的颜色有时会偏向绿色、蓝色或紫色。

hackernews · automatoney · 8月4日 15:16 · [社区讨论](https://news.ycombinator.com/item?id=49170165)

**背景**: 色彩空间是一种数学模型，以更易于指定和操作的方式组织颜色。人类的肤色在大多数色彩空间中仅占据一个狭窄的、月牙形的区域，因此传统的 RGB 选择器通常难以选出合理的肤色。程序化生成算法通过从这样的空间中采样来自动创建颜色集，而该项目旨在让肤色生成过程更加直观。相关的工作，例如 Pantone 肤色指南以及 Oklab 中对粉底色号的分析，表明这一挑战在设计界和图形界已被广泛认识。

**社区讨论**: 评论者普遍热情，称赞其视觉呈现和函数拟合方法的巧妙性。一些人指出了与现有工作的关联，如 Pantone 肤色指南和 The Pudding 的化妆品色号数据集，并注意到肤色分布在 Oklab 中也呈月牙形。还有人提出了关于准确性和色相偏移的技术担忧，并讨论了背后的颜色科学，例如完全饱和的皮肤图像会呈现橙色这一观察。

**标签**: `#color-space`, `#skin-tone-generation`, `#procedural-generation`, `#digital-art`, `#gamedev`

---

<a id="item-5"></a>
## [DeepSeek V4 Flash 在单块 AMD MI300X 上高效运行](https://github.com/ryanzhou/deepseek-v4-flash-mi300x) ⭐️ 8.0/10

一篇技术贴展示了 DeepSeek V4 Flash（284B 参数 MoE 模型，激活参数 13B）在单块 AMD MI300X 加速器上以每秒超过 150 token 的速度运行。该优化通过将原本 100 万 token 的上下文窗口缩短至 256K token 来换取此速度。 这表明大型 MoE 模型可以在单块高内存加速器上高效运行，而无需多 GPU 集群，从而可能降低自托管推理成本。这也使 AMD MI300X 的 192GB HBM3 内存在受内存约束的 LLM 工作负载中成为 NVIDIA 的可行替代方案。 显存节省得益于原生 MXFP4 量化，使模型能够装入 144GB 显存，这意味着基于 PCIe 的 MI350P 也能运行它。不过 MI300X 是 OAM 模块，通常以约 25 万欧元的 8-GPU 板卡形式销售，因此很难直接购买单块。

hackernews · zhoutong · 8月4日 10:00 · [社区讨论](https://news.ycombinator.com/item?id=49166386)

**背景**: DeepSeek V4 Flash 是一个面向效率的混合专家（MoE）模型，总参数量 284B、每 token 激活 13B，专为快速推理和高吞吐场景设计，支持 100 万 token 的上下文窗口。AMD Instinct MI300X 是一款配备 192GB HBM3 内存和高内存带宽的加速器，非常适合需要单设备容纳的大型模型。较长的上下文会显著拖慢推理速度，因此缩减上下文窗口是提升速度的常见实用取舍。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash">deepseek-ai/DeepSeek-V4-Flash · Hugging Face</a></li>
<li><a href="https://www.amd.com/en/products/accelerators/instinct/mi300/mi300x.html">AMD Instinct™ MI300X Accelerators</a></li>
<li><a href="https://lenovopress.lenovo.com/lp1943-thinksystem-amd-mi300x-192gb-750w-8-gpu-board">ThinkSystem AMD MI300X 192GB 750W 8-GPU Board Product Guide &gt; Lenovo Press</a></li>

</ul>
</details>

**社区讨论**: 评论区在赞赏的同时也提出了现实问题：MI300X 无法单独购买，而是以约 25 万欧元的 8 卡板卡形式销售；先前的对比也遗漏了 DwarfStar，后者能用更少显存运行同一模型。另有评论指出基于 PCIe 的 MI350P（144GB）更适合单卡部署，也有人认为 256K 上下文是合理取舍，因为 Codex 也处于类似水平，且质量在接近满 100 万时确实会下降。

**标签**: `#DeepSeek`, `#AMD MI300X`, `#Inference`, `#MoE`, `#Quantization`

---

<a id="item-6"></a>
## [联邦快递式钓鱼邮件正在削弱用户的安全意识](https://www.troyhunt.com/thanks-fedex-this-is-why-we-keep-getting-phished/) ⭐️ 8.0/10

知名安全研究员 Troy Hunt 在 2024 年发表博客，展示了联邦快递（FedEx）的合法通知邮件如何与常见钓鱼手法高度相似。这反映出企业无意中训练用户接受类似钓鱼邮件的真实案例。 这很重要，因为合法机构发送类似钓鱼的邮件，会削弱人们区分真实邮件与诈骗邮件的能力，从而使网络钓鱼攻击更容易得手。所有电子邮件用户都受影响，安全培训的效果也会被削弱。 Hunt 的文章重点分析了联邦快递的一则海关通知，该通知要求收件人填写个人信息，与常见钓鱼邮件的结构一致。这个例子表明，即使是通过 SPF、DKIM 和 DMARC 等认证协议的邮件，看起来仍可能很可疑。

hackernews · stymaar · 8月4日 21:09 · [社区讨论](https://news.ycombinator.com/item?id=49175192)

**背景**: 网络钓鱼依赖社会工程学手段，诱骗收件人点击恶意链接或泄露敏感信息。SPF、DKIM 和 DMARC 等邮件认证标准可以验证邮件是否确实来自某个域名，但无法解决糟糕的邮件设计问题。当可信品牌发出混乱或看起来不够安全的邮件时，用户会被训练得忽略安全培训中强调的警告信号。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://postmarkapp.com/glossary/email-authentication">What is email authentication ? [ SPF , DMARC , DKIM explained ]</a></li>
<li><a href="https://blogs.cisco.com/security/what-is-email-spoofing-and-how-to-detect-it">What is Email Spoofing and How to Detect It - Cisco Blogs</a></li>

</ul>
</details>

**社区讨论**: 评论者分享了其他公司的类似经历：Chase 的欺诈部门一边告诉客户不要相信陌生来电，一边在电话中要求核实身份；Google 使用短域名 c.gle 发送存储空间警告。总体情绪是对企业沟通方式加剧钓鱼风险的沮丧，一些用户还提出了帮助非技术高管理解这一问题的比喻。

**标签**: `#phishing`, `#cybersecurity`, `#email security`, `#social engineering`, `#security awareness`

---

<a id="item-7"></a>
## [Oxide Computer 完成 4.45 亿美元 D 轮融资](https://www.sec.gov/Archives/edgar/data/1795071/000179507126000002/xslFormDX01/primary_doc.xml) ⭐️ 8.0/10

根据美国证券交易委员会（SEC）的 Form D 文件，Oxide Computer 已完成 4.45 亿美元的 D 轮融资。这是这家硬件初创公司继此前 4400 万、1 亿和 2 亿美元融资之后的又一轮大额融资。 这笔巨额融资表明投资者对 Oxide 以软硬件一体化机架重塑云基础设施的使命充满信心。如果成功，它可能通过提供基于开源原则的本地部署方案，挑战传统公有云提供商的统治地位。 Form D 文件显示本次发行金额为 4.45 亿美元，社区评论追溯了 Oxide 的融资轨迹：2023 年 4400 万美元 A 轮，2026 年 2 亿美元 C 轮。一位工程副总裁评论说，尽管他们每年在 AWS 上花费 90 万美元，Oxide 却没有回应其销售咨询；还有人质疑 Oxide 是否真正向客户发货硬件。

hackernews · depr · 8月4日 20:13 · [社区讨论](https://news.ycombinator.com/item?id=49174407)

**背景**: Oxide Computer Company 是一家初创公司，打造“云计算机”——将计算、存储、网络和软件集成到单一系统中的整机架产品。公司致力于在本地提供公有云体验，强调开放性和客户控制权。此次融资消息发布之前，Oxide 刚发布了此前几轮融资的博客文章，该公司在基础设施工程师和开发者中拥有大量追随者。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://oxide.computer/">Oxide Computer Company</a></li>
<li><a href="https://tracxn.com/d/companies/oxide-computer/__kI0jT50BQRv4YWhfboq9Wp2wCfHm6iQWJODTcCX-grc">Oxide Computer - 2026 Company Profile, Team, Funding... - Tracxn</a></li>
<li><a href="https://ca.linkedin.com/company/oxidecomputer">Oxide Computer Company | LinkedIn</a></li>

</ul>
</details>

**社区讨论**: Hacker News 社区的反应包含热情、怀疑和个人轶事。有人称赞 Oxide 的概念和 Oxide and Friends 播客，也有人质疑该公司是否真的交付硬件。一位工程副总裁分享了他被 Oxide 忽视销售咨询的挫败经历，还有几位参与者表示，Jessie Frazelle 的参与是一个积极的信号。

**标签**: `#hardware`, `#funding`, `#oxide-computer`, `#servers`, `#cloud`

---

<a id="item-8"></a>
## [LLM 0.32 新增推理痕迹、服务端工具和更智能的日志功能](https://simonwillison.net/2026/Aug/4/new-release-of-llm/#atom-everything) ⭐️ 8.0/10

LLM 0.32 于 2026 年 8 月 4 日发布，引入了可见的推理痕迹、服务端提供商工具、重新设计的内容寻址 SQLite 日志，以及对 GPT-5.6 模型家族的支持，并将 GPT-5.6 Luna 作为新的默认模型。llm-anthropic、llm-gemini 和 llm-openrouter 插件也获得了重大更新。 此版本通过使推理模型透明化，并支持代码执行和网络搜索等服务端工具，显著增强了 LLM CLI 工具，从而简化了 AI 开发工作流程。改进的日志记录和灵活的端点支持也有利于集成各种模型提供商的开发者。 用户现在可以在标准错误输出中看到推理痕迹，并可通过 -R/--hide-reasoning 标志将其隐藏。新的服务端工具包括 OpenAI 的 CodeInterpreter 和 WebSearch，而 llm openai endpoint 命令允许对任何兼容 OpenAI 的端点执行一次性提示而无需记录日志，SQLite 日志现在也改为内容寻址方式。

rss · Simon Willison · 8月4日 23:58

**背景**: 推理痕迹是推理模型在生成最终答案之前产生的中间思维链令牌，可以提高复杂任务的性能。OpenAI 于 2025 年 3 月 11 日发布的 Responses API 通过将 Chat Completions API 与高级工具调用能力相结合，简化了智能体应用的开发。内容寻址存储根据内容而非名称或位置检索数据，LLM 工具现在将其用于 SQLite 日志。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2504.09762v1">(How) Do Reasoning Models Reason ?</a></li>
<li><a href="https://grokipedia.com/page/OpenAI_Responses_API">OpenAI Responses API</a></li>
<li><a href="https://en.wikipedia.org/wiki/Content-addressable_storage">Content - addressable storage - Wikipedia</a></li>

</ul>
</details>

**标签**: `#LLM`, `#release`, `#AI tools`, `#OpenAI`, `#CLI`

---

<a id="item-9"></a>
## [MiniMax-H3 全能模态视频模型通过 MLX 在 Apple Silicon 上本地运行](https://simonwillison.net/2026/Aug/4/minimax-h3-mlx/#atom-everything) ⭐️ 8.0/10

Simon Willison 通过 PipeNetwork/minimax-h3-mlx 这个 MLX 移植包，在 Apple Silicon 上本地运行了 MiniMax 两天前发布的 MiniMax-H3 全能模态生成模型。该模型可根据文本、图像、音频和视频输入，生成最长 15 秒、含音频的视频片段。 这首次将先进的视频生成模型带到本地 Apple 硬件上，让 AI 从业者无需依赖云端 API 即可进行实验。本地运行降低了成本、增强了隐私保护，并支持更深入的定制和调试，可能加速生成式视频模型在研究和产品开发中的采用。 该 MLX 移植版需要下载约 115 GB 的模型文件，在 M5 Max MacBook Pro 上生成一条 15 秒视频耗时接近 45 分钟。Simon 指出视频效果令人印象深刻，但音频是类似胡言乱语的语音垃圾，因为他没有遵循提示词指南，这强调了提示词工程对音频输出结果的重要性。

rss · Simon Willison · 8月4日 19:10

**背景**: MiniMax-H3 是一个开放权重的通用全能模态生成模型，统一理解文本、图像、视频和音频，并能生成最高 2K 分辨率、15 秒、带原生立体声的视频。MLX 是苹果推出的数组框架，专为 Apple Silicon 上高效灵活的机器学习研究而设计。PipeNetwork/minimax-h3-mlx 包将 MiniMax-H3 转换为 MLX 兼容格式，使其能在 Apple 硬件上本地运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ml-explore/mlx">GitHub - ml-explore/mlx: MLX: An array framework for Apple silicon · GitHub</a></li>
<li><a href="https://www.minimax.io/blog/minimax-h3">MiniMax H3: An Open Model Breaking the Boundaries Between Tasks...</a></li>
<li><a href="https://www.emergentmind.com/topics/omni-modal-large-language-models-omni-llms-3a9b15f1-ea64-487d-bee0-2b01a040defb">Omni - Modal LLMs: Unified Multi-Modal AI</a></li>

</ul>
</details>

**标签**: `#ai`, `#mlx`, `#video-generation`, `#omni-modal`, `#apple-silicon`

---

<a id="item-10"></a>
## [谷歌为 Anthropic 搭建 2000 亿美元华尔街融资机器](https://www.ft.com/content/549f2e23-5aa2-49c7-9ea6-a9784ab7087c) ⭐️ 8.0/10

《金融时报》8 月 4 日调查发现，谷歌已悄然搭建史上最大规模基础设施融资架构之一，支持向 Anthropic 交付超 1500 亿美元 AI 芯片，相关合同总额约 2000 亿美元。该架构引入博通、阿波罗、黑石、摩根士丹利及多家加密矿企，采用厂商融资模式，避免硬件压在各方资产负债表上。 这标志着以史无前例的规模为 AI 算力融资的新型金融工程手段，显示大型科技公司可将巨额资本开支转移给华尔街。它对 AI 基础设施投资、硬件供应链以及大型科技与金融机构的资产负债表具有广泛影响。 今年 6 月，特殊目的载体 Compute SPV 完成首批交易，购入约 350 亿美元硬件，约合 1 吉瓦算力和 100 万颗 TPU。该模式借鉴波音、GE 推销飞机和发动机的厂商融资玩法，由于 Anthropic 没有信用评级，各方共担风险。

telegram · zaihuapd · 8月4日 10:52

**背景**: 特殊目的载体（SPV）是为隔离金融风险而设立的独立法律实体，常用来持有单笔投资或项目。厂商融资是供应商为买方提供资金的安排，常用于设备采购；在此案例中，阿波罗和黑石购买硬件后回租给 Anthropic。张量是神经网络中的核心数据结构；TPU 是谷歌为加速机器学习工作负载而专门设计的定制 ASIC 芯片。这种融资结构让多方分担 AI 硬件的巨额成本，而不让任何单一企业将数千亿美元压在自己的资产负债表上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://corporatefinanceinstitute.com/resources/management/special-purpose-vehicle-spv/">Special Purpose Vehicle ( SPV ) - Guide, Examples, What You Need...</a></li>
<li><a href="https://www.kredx.com/supply-chain-finance/invoice-discounting/vendor-financing">Vendor Financing : What is it &amp; How Does it Work - KredX</a></li>
<li><a href="https://www.linkedin.com/posts/global-advisors_term-tensorprocessingunit-tpu-activity-7420035006447861760-tmsy">Google&#x27;s Tensor Processing Unit ( TPU ) for AI and ML | LinkedIn</a></li>

</ul>
</details>

**标签**: `#AI`, `#Google`, `#Anthropic`, `#Financing`, `#Infrastructure`

---

<a id="item-11"></a>
## [特朗普政府拟起草禁令，禁止进口中国数据中心光模块](https://www.reuters.com/world/trump-administration-drafting-ban-chinese-data-center-devices-sources-say-2026-08-04/) ⭐️ 8.0/10

据报道，特朗普政府正在起草一项禁令，拟禁止进口用于数据中心的新型中国光模块，FCC 正在推进该措施，官员希望今年内发布并生效。该禁令针对支撑 AI 热潮的关键组件，但仍可能修改或搁置。 光模块是支撑 AI 产业的数据中心内高速数据传输的关键组件，因此这一禁令可能扰乱全球 AI 基础设施供应链。尤其会冲击中国厂商中际旭创——这家全球领先供应商占据约 27% 的市场份额。 该禁令仍处于初步阶段，知情人士强调其可能被修改或搁置。此前 FCC 已对中国无人机、路由器、机器人和逆变器实施类似进口限制；中国驻美使馆表示，将对损害中国利益的行为采取一切必要措施。

telegram · zaihuapd · 8月4日 11:29

**背景**: 光模块是数据中心网络中的关键组件，通过光纤电缆连接服务器、交换机和其他网络设备，实现高速数据传输。传统数据中心通常使用 1G/10G 等较低速率的光模块，而云数据中心则主要采用 40G/100G 等高速光模块。特朗普政府以国家安全为由，担忧数据窃取、恶意软件植入和服务中断，因此加强了对中国技术组件的进口限制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ascentoptics.com/blog/everything-you-need-to-know-about-optical-modules/">Everything You Need to Know About Optical Modules</a></li>
<li><a href="https://www.linkedin.com/pulse/what-requirements-optical-modules-development-trend-cloud-lyn-song">What are the requirements for optical modules in the development...</a></li>
<li><a href="https://www.fangzwire.com/news/Optical-Module-Solutions-for-Advanced-Data-Centers.html">Optical Module Solutions for Advanced Data Centers</a></li>

</ul>
</details>

**标签**: `#trade policy`, `#optical modules`, `#AI infrastructure`, `#China`, `#regulation`

---
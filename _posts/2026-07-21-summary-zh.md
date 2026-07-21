---
layout: default
title: "Horizon Summary: 2026-07-21 (ZH)"
date: 2026-07-21
lang: zh
---

> 从 38 条内容中筛选出 17 条重要资讯。

---

1. [Hugging Face 披露 AI 智能体驱动安全事件](#item-1) ⭐️ 9.0/10
2. [Fastjson 1.x 无 gadget 高危 RCE 漏洞](#item-2) ⭐️ 9.0/10
3. [智谱建成全国产芯片大型数据中心](#item-3) ⭐️ 9.0/10
4. [中国开源 AI 模型威胁西方高端定价](#item-4) ⭐️ 8.0/10
5. [美国科技巨头隐性 AI 债务达 1.65 万亿美元](#item-5) ⭐️ 8.0/10
6. [AI 在寻找反例上超越数学家](#item-6) ⭐️ 8.0/10
7. [ACLU 报告指控 Flock Safety 欺骗市议会和警方](#item-7) ⭐️ 8.0/10
8. [Agent 集群以惊人速度用 Rust 重建 SQLite](#item-8) ⭐️ 8.0/10
9. [中国开放权重 AI 策略胜过美国专有模型](#item-9) ⭐️ 8.0/10
10. [完美不等于过度工程：一个细致视角](#item-10) ⭐️ 8.0/10
11. [黑客清空罗马尼亚土地登记数据库](#item-11) ⭐️ 8.0/10
12. [测量 arXiv 上的 AI 写作显示 ChatGPT 后急剧上升](#item-12) ⭐️ 8.0/10
13. [美国提议立法将 AI 训练数据视为合理使用](#item-13) ⭐️ 8.0/10
14. [美国政府考虑限制中国开放权重 AI 模型，如 Kimi K3](#item-14) ⭐️ 8.0/10
15. [普渡大学研究发现美军 App 含中俄代码](#item-15) ⭐️ 8.0/10
16. [谷歌 Frozen v2 芯片将 Gemini 效率提升 6-10 倍](#item-16) ⭐️ 8.0/10
17. [X 安卓客户端已从零重建完成](#item-17) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Hugging Face 披露 AI 智能体驱动安全事件](https://huggingface.co/blog/security-incident-july-2026) ⭐️ 9.0/10

2026 年 7 月，Hugging Face 披露了一起安全事件，攻击者利用数据集处理流程中的代码执行漏洞，借助自主 AI 智能体框架执行了数万次操作并在内部集群间横向移动。公司已控制事态，并在商业大模型拒绝协助后，使用本地部署的 GLM 5.2 模型完成取证分析。 该事件突显了自主 AI 智能体可放大攻击的新型威胁，也揭示了依赖商业大模型进行安全调查的风险。转向本地开源模型进行取证，为构建韧性的 AI 安全实践树立了重要先例。 攻击者利用了数据集处理流程中的两处代码执行漏洞，AI 智能体框架可能自动完成了横向移动和凭证窃取。事件后，Hugging Face 轮换了受影响凭证、重建受损节点，并建议用户轮换访问令牌。取证分析涉及超过 1.7 万条攻击记录，由本地 GLM 5.2 处理。

telegram · zaihuapd · 7月20日 10:41

**背景**: AI 智能体框架（如 smolagents）允许开发者构建自主智能体，可编排任务、集成工具并在无需持续人工干预的情况下运行。GLM 5.2 是 Z.ai（原智谱 AI）开发的大型开源语言模型，拥有 744B 参数和 1M token 上下文，适用于长周期任务。Hugging Face Spaces 是一个托管机器学习演示应用的平台，此次事件中未被入侵。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://view.inews.qq.com/a/20251118A02T7J00">智能体框架的选择：一文读懂9个主流AI智能体框架_腾讯新闻</a></li>
<li><a href="https://en.wikipedia.org/wiki/GLM_5.2">GLM 5.2</a></li>
<li><a href="https://huggingface.co/docs/hub/spaces">Spaces · Hugging Face</a></li>

</ul>
</details>

**标签**: `#AI安全`, `#安全事件`, `#Hugging Face`, `#大模型`, `#攻击取证`

---

<a id="item-2"></a>
## [Fastjson 1.x 无 gadget 高危 RCE 漏洞](https://x.com/k_firsov/status/2078872293745570032) ⭐️ 9.0/10

安全研究人员披露了 Fastjson 1.x 1.2.68 至 1.2.83 版本中存在一个高危远程代码执行漏洞，无需开启 autoTypeSupport 或任何 classpath gadget 链即可在 JDK 8、17 和 21 上利用。 该漏洞极为严重，因为 Fastjson 1.x 在 Java 应用中被广泛使用，且官方大概率不会发布补丁，用户必须立即迁移到 Fastjson2 或启用 SafeMode，影响无数系统。 该漏洞影响 1.2.68 至 1.2.83 版本，利用时不需任何 gadget 链或开启 autoTypeSupport，因此特别危险。Fastjson 1.x 已于 2024 年 10 月停止维护，官方预计不会发布修复。

telegram · zaihuapd · 7月20日 14:32

**背景**: Fastjson 是阿里巴巴开发的高性能 Java JSON 库，它通过 autoType 机制将 JSON 反序列化为特定 Java 类，这一特性可能被滥用进行反序列化攻击。Gadget 链是攻击者在反序列化过程中用于实现远程代码执行的一系列对象。SafeMode 模式自 Fastjson 1.2.68 引入，完全禁用 autoType，从而缓解反序列化漏洞。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/alibaba/fastjson2/blob/main/docs/autotype_en.md">fastjson 2/docs/autotype_en.md at main · alibaba/ fastjson 2 · GitHub</a></li>
<li><a href="https://devdoc.net/javamisc/fastjson-1.2.79-javadocs/com/alibaba/fastjson/parser/ParserConfig.html">ParserConfig ( fastjson 1.2.79 API)</a></li>
<li><a href="https://www.mo4tech.com/fastjson-to-1-2-70.html">FastJson to 1.2.70 - Moment For Technology</a></li>

</ul>
</details>

**标签**: `#Fastjson`, `#RCE`, `#vulnerability`, `#Java`, `#security`

---

<a id="item-3"></a>
## [智谱建成全国产芯片大型数据中心](https://www.bloomberg.com/news/articles/2026-07-20/z-ai-completes-giant-data-center-with-chinese-chips-to-train-ai) ⭐️ 9.0/10

智谱 AI 完成了一座功率达 1 吉瓦、全部采用国产芯片的大型数据中心建设，并已开始部分运营，用于训练其 GLM 模型。 这标志着中国 AI 基础设施自主可控的重大突破，表明国产芯片能够规模化支持大型 AI 训练，减少对外国技术的依赖。 该数据中心功率达 1 吉瓦，足以为约 75 万户家庭供电，是中国 AI 实验室建造的最大规模设施之一。智谱运营着多个各拥有超万枚芯片的计算集群。

telegram · zaihuapd · 7月20日 15:43

**背景**: 智谱 AI 是一家开发大型语言模型的中国公司，其产品包括 GLM 系列。GLM（通用语言模型）系列包含 GLM-4、GLM-5 等模型，为 ChatGLM 等应用提供支持。建造国产芯片数据中心反映了中国在 AI 硬件领域推动技术自主可控的战略。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.atlascloud.ai/zh/models/glm">GLM 大 模 型 API 合集：智谱 AI 中英双语大 模 型 | Atlas Cloud</a></li>
<li><a href="https://zh.wikipedia.org/wiki/%E6%99%BA%E8%B0%B1">智谱 - 维基百科，自由的百科全书</a></li>

</ul>
</details>

**标签**: `#AI基础设施`, `#国产芯片`, `#数据中心`, `#智谱`

---

<a id="item-4"></a>
## [中国开源 AI 模型威胁西方高端定价](https://stratechery.com/2026/whos-afraid-of-chinese-models/) ⭐️ 8.0/10

中国 AI 实验室免费发布高质量开源模型，削弱了 OpenAI 和 Anthropic 等西方实验室的高端 API 定价策略。 这种商品化威胁到西方 AI 实验室的天价风险投资估值，这些估值依赖于高端定价以产生巨额利润，可能引发一场价格战。 尽管 Claude Code 和 Codex 等工具表现出粘性，但用户报告切换很容易，削弱了锁定效应。此外，观察到新疆的中国数据中心积极抓取西方网站，表明其大规模基础设施正在建设。

hackernews · mfiguiere · 7月20日 11:05 · [社区讨论](https://news.ycombinator.com/item?id=48977128)

**背景**: OpenAI 和 Anthropic 等西方 AI 实验室的估值高达数千亿美元，基于它们能够为其高级模型的 API 访问收取高价的预期。中国提供的免费开源模型挑战了这一经济模式，以零成本提供类似能力，导致 AI 模型推理的商品化。

**社区讨论**: 评论者指出，VC 最怕中国模型，因为它们削弱了其投资背后的高定价前提。一些人注意到切换 AI 编码工具很容易，降低了锁定效应，而另一些人则指出中国在电力和芯片获取方面的成本优势是一个长期威胁。

**标签**: `#AI`, `#Chinese AI models`, `#economics of AI`, `#open source AI`, `#venture capital`

---

<a id="item-5"></a>
## [美国科技巨头隐性 AI 债务达 1.65 万亿美元](https://asia.nikkei.com/business/technology/five-us-tech-giants-hidden-debts-soar-to-1.65tn-on-opaque-ai-funding) ⭐️ 8.0/10

据《日经亚洲》分析，五家美国主要科技公司通过不透明的 AI 基础设施融资安排，累积了 1.65 万亿美元的表外债务。 这些隐性债务可能对金融市场构成系统性风险，并在 AI 投资表现不佳时扭曲投资者对科技巨头真实财务状况的看法。 这些债务由拥有数据中心的特殊目的载体（SPV）持有，而非科技巨头直接承担，但公司有长期承诺。机构投资者可能知情，但散户投资者了解较少。

hackernews · NordStreamYacht · 7月21日 03:56 · [社区讨论](https://news.ycombinator.com/item?id=48987863)

**背景**: 表外融资是一种会计实践，通过 SPV 等工具将某些负债排除在公司资产负债表之外，以降低杠杆率和管理财务风险。在 AI 基础设施领域，科技巨头利用 SPV 为数据中心融资，同时避免直接债务计入报表，但这种做法可能掩盖真实的财务风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Off-balance-sheet">Off-balance-sheet - Wikipedia</a></li>
<li><a href="https://www.investopedia.com/terms/o/off-balance-sheet-obs.asp">Understanding Off-Balance Sheet Activities: Types and Key Examples</a></li>

</ul>
</details>

**社区讨论**: 评论者指出，债务由 SPV 持有，因此向 SPV 放贷的银行面临风险，而非科技巨头直接承担。有人认为成熟投资者能看穿这些结构，质疑科技公司从中获益，而另一些人则推测，如果 AI 被视为关键资产，美国政府可能会救助或国有化这些资产。

**标签**: `#AI funding`, `#tech giants`, `#finance`, `#Silicon Valley`, `#investment`

---

<a id="item-6"></a>
## [AI 在寻找反例上超越数学家](https://xenaproject.wordpress.com/2026/07/20/human-mathematicians-are-being-outcounterexampled/) ⭐️ 8.0/10

近期一篇博客文章指出，AI 系统现在能够比人类数学家更快地生成数学猜想的反例，展现了这一新能力。 这一转变通过快速证伪错误猜想节省了数学家的时间，使他们能够专注于更有价值的研究，并可能从根本上改变数学发现的方式。 博客文章提及 Sol 和 Fable 等 AI 模型，研究生每月支付 200 美元才能使用，这表明 AI 辅助数学工具市场正在增长。

hackernews · artninja1988 · 7月20日 19:03 · [社区讨论](https://news.ycombinator.com/item?id=48983382)

**背景**: 在数学中，反例是指证明某个猜想不成立的例子。传统上，寻找反例需要深刻的洞察力和手动搜索。AI 系统现在可以利用模式识别和穷举搜索快速生成反例，从而自动完成研究过程中的关键部分。

**社区讨论**: 评论中既有热情也有谨慎：一些人称赞效率提升（如 satvikpendem 认为这是件好事），而另一些人则将其比作约翰·亨利民间传说，警示人类过度依赖。hintymad 提到张益唐因依赖错误推论而受挫的案例，强调了验证的必要性。

**标签**: `#AI`, `#mathematics`, `#counterexamples`, `#research`, `#machine learning`

---

<a id="item-7"></a>
## [ACLU 报告指控 Flock Safety 欺骗市议会和警方](https://www.aclu.org/news/privacy-technology/tracking-alpr-cameras/flock-safety-credibility-lost-as-it-repeatedly-lies-to-city-councils-police-departments-and-public-across-the-country) ⭐️ 8.0/10

美国公民自由联盟（ACLU）发布了一份报告，详细说明了自动车牌识别系统制造商 Flock Safety 在与美国各地市议会、警察部门和公众互动中反复撒谎的行为模式。 该报告削弱了公众对 Flock Safety 的信任，并引发了对该公司信誉的严重担忧，可能影响正在进行的和未来的监控技术合同以及隐私政策辩论。 该报告基于来自多个城市的证据，在这些城市中，Flock Safety 涉嫌歪曲其 ALPR 摄像头的能力、数据使用和隐私保护措施，以获得监控网络的批准。

hackernews · StatsAreFun · 7月21日 00:33 · [社区讨论](https://news.ycombinator.com/item?id=48986731)

**背景**: Flock Safety 是一家私有公司，在 49 个州的 5000 多个社区运营自动车牌识别摄像头，每月进行数十亿次车辆扫描。ALPR 技术利用光学字符识别读取车牌并存储车辆位置数据，这引发了关于大规模监视和政府追踪的隐私担忧。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Flock_Safety">Flock Safety</a></li>
<li><a href="https://en.wikipedia.org/wiki/Automated_License_Plate_Readers">Automated License Plate Readers</a></li>

</ul>
</details>

**社区讨论**: 社区评论反映了分歧：一些人认为像 Flock 这样的监控技术能有效减少犯罪，而另一些人则强调在全景监狱下无法建立高信任社会，一旦安装了摄像头，信任就被摧毁。还有人对安装标准以及监控国家的不可避免性表示担忧。

**标签**: `#privacy`, `#surveillance`, `#technology policy`, `#ACLU`, `#Flock Safety`

---

<a id="item-8"></a>
## [Agent 集群以惊人速度用 Rust 重建 SQLite](https://cursor.com/blog/agent-swarm-model-economics) ⭐️ 8.0/10

Cursor 的博文描述了一个新的 Agent 集群系统，仅凭 SQLite 的文档就用 Rust 从零重建了 SQLite，达到每秒 1000 次提交的速度，远超之前系统。 这一演示突破了基于 LLM 的 Agent 自主能力的边界，但也提出了关键问题：这种成就是否依赖于真正的推理，还是仅仅是对训练数据的记忆。 该系统包含一个为处理高吞吐量和协调而构建的自定义版本控制系统。之所以选择从头构建 SQLite 的任务，是因为之前的集群在此任务上表现不佳。

hackernews · jlaneve · 7月20日 18:06 · [社区讨论](https://news.ycombinator.com/item?id=48982535)

**背景**: Agent 集群是指多个 AI Agent 协作解决复杂任务的系统。Cursor 是一款具备 AI 功能的代码编辑器。对 LLM 记忆的担忧源于 SQLite 的源代码和 Rust 重写版本很可能存在于训练数据中，这意味着 Agent 可能是在回忆而非推理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://relevanceai.com/learn/agent-swarms-orchestrating-the-future-of-ai-collaboration">What is an AI Agent Swarm</a></li>

</ul>
</details>

**社区讨论**: 评论对实验的潜力表示兴奋，但许多人质疑模型是否只是记住了训练数据中的 SQLite 源代码。一些用户指出，实验框架的代码未公开，使得难以评估其主张。其他人则认为，尽管目前存在局限性，但这仍是对未来的窥探。

**标签**: `#agent swarms`, `#LLM`, `#software engineering`, `#SQLite`, `#version control`

---

<a id="item-9"></a>
## [中国开放权重 AI 策略胜过美国专有模型](https://werd.io/american-ai-is-locked-down-and-proprietary-its-losing/) ⭐️ 8.0/10

一篇文章指出，中国的开放权重 AI 策略正在超越美国的专有模型，并提到了其在初创企业中的广泛采用和成本优势。 这一转变可能重塑全球 AI 格局，推动企业采用开放权重模型，并挑战美国在 AI 领域的领导地位。 开放权重模型并非完全开源；它允许免费使用预训练权重，但限制对训练数据和代码的访问。中国政府为开放权重训练提供 GPU 补贴，降低了成本。

hackernews · benwerd · 7月20日 14:21 · [社区讨论](https://news.ycombinator.com/item?id=48979269)

**背景**: 开放权重 AI 是指将预训练参数公开发布的模型，允许微调和推理，而不需要完全开源。中国大力投资 AI 基础设施，包括国家计算中心，以支持开放权重模型的开发。Meta 的 LLaMA 和 DeepSeek 的 R1 等竞争对手凭借开放权重策略获得了关注。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://fluxhuman.com/en/blog/open-weights-ai-your-strategic-compliance-hedge">Open Weights AI : Your Strategic Compliance Hedge | FluxHuman Blog</a></li>
<li><a href="https://asibiont.com/en/blog/pochemu-strategiya-otkrytykh-vesov-kitaya-pobezhdaet-v-gonke-ii">China&#x27;s Open - Weights AI Strategy Is Winning... — ASI Biont Blog</a></li>
<li><a href="https://thegulfentrepreneur.com/open-weights-ai-model/">Open - Weights AI Model | OpenAI Announces Strategic Shift</a></li>

</ul>
</details>

**社区讨论**: 评论者就免费/开放解决方案获胜的长期趋势展开辩论，一些人怀疑“80%的初创企业使用中国模型”的说法。其他人指出，企业更看重数据保留和现有供应商，而非开放性，并且开放权重并非真正的开源。

**标签**: `#AI`, `#open-source`, `#China`, `#AI strategy`, `#machine learning`

---

<a id="item-10"></a>
## [完美不等于过度工程：一个细致视角](https://var0.xyz/posts/perfection-is-not-over-engineering.html) ⭐️ 8.0/10

这篇文章挑战了软件工程中常见的谚语“完美是好的敌人”，认为正确追求完美并非过度工程，而是对质量的追求。 这一讨论具有重要意义，因为它质疑了一项广泛接受的工程原则，可能影响团队如何在软件开发中平衡质量与实用主义。 作者将“完美”定义为只有在严格要求和清晰理解下才能实现，并将其与解决错误问题的过度工程区分开来。

hackernews · var0xyz · 7月20日 14:10 · [社区讨论](https://news.ycombinator.com/item?id=48979120)

**背景**: “完美是好的敌人”这句话在软件开发中常被用来鼓励快速发布不完美但可用的代码。过度工程指添加超出当前需求的非必要复杂性或功能。本文认为，与用户需求相符的真正完美并非过度工程，而是一个合理的目标。

**社区讨论**: 评论者表达了不同观点：一些人赞赏对这种谚语的抵制，指出它常被用来合理化糟糕的软件，而另一些人则警告完美主义可能导致过度工程和无谓争论。对于产品思维是否有害，也存在讨论。

**标签**: `#software engineering`, `#perfection`, `#over-engineering`, `#product mindset`, `#engineering culture`

---

<a id="item-11"></a>
## [黑客清空罗马尼亚土地登记数据库](https://news.risky.biz/risky-bulletin-hacker-wipes-romanias-entire-land-registry-database/) ⭐️ 8.0/10

一名黑客入侵了罗马尼亚国家地籍与土地登记局（ANCPI），清空了整个土地登记数据库。幸好有离线备份，才避免了财产记录毁灭性的丢失。 这一事件突显了关键公共数据库离线备份的极端重要性，因为土地所有权记录是财产权利和经济稳定的基础。此次入侵也引发了对政府 IT 系统网络安全漏洞的担忧。 据安全公司 KELA 确认，黑客是来自阿尔及利亚的扎卡里亚·马赫朱布（Zakaria Mahdjoub），他声称删除了备份，但 ANCPI 持有一份离线副本。官员们正在将应用程序迁移到罗马尼亚政府云，由特别电信服务局（STS）协调。

hackernews · speckx · 7月20日 13:28 · [社区讨论](https://news.ycombinator.com/item?id=48978605)

**背景**: 土地登记是记录财产所有权、边界和交易的关键公共数据库。数据丢失会在房地产市场、法律纠纷和经济活动中造成混乱。离线备份存储在独立于主网络的地方，是抵御勒索软件和破坏性攻击的最后一道防线。

**社区讨论**: 评论者对离线备份的存在表示宽慰，skinfaxi 指出了失去土地所有权证明的社会影响。cbg0 提供了迁移到政府云的最新进展。alexpotato 认为此次入侵是由于 IT 合同中的腐败。khurs 确认了黑客身份为阿尔及利亚人，并提到了引渡条约。

**标签**: `#cybersecurity`, `#data breach`, `#Romania`, `#land registry`, `#hacking`

---

<a id="item-12"></a>
## [测量 arXiv 上的 AI 写作显示 ChatGPT 后急剧上升](https://unslop.run/blog/measuring-ai-writing-on-arxiv) ⭐️ 8.0/10

作者开发的一款检测工具分析了 2021 年至 2026 年间超过 12,750 篇 arXiv 论文，发现到 2026 年 1 月，约 39%的论文被标记为 AI 写作，其中计算机科学领域高达 65%。 这一量化结果凸显了 AI 写作在学术出版中的快速普及，引发了对研究诚信和同行评审可靠性的担忧，尤其是在计算机科学等领域。 该检测器经过调校以避免误报，ChatGPT 之前的检测率仅为 0.4%。但作者承认存在局限性：该工具结合了三个检测分数，且未公开源代码，导致难以复现结果。

hackernews · dopamine\_daddy · 7月20日 16:36 · [社区讨论](https://news.ycombinator.com/item?id=48981206)

**背景**: arXiv 是一个广泛使用的科学论文预印本库，尤其涵盖物理学、数学和计算机科学。AI 写作检测工具试图识别由大型语言模型（如 GPT-4）生成的文本，但已知存在较高的误报率，尤其是在非母语英语写作或结构化文本中。AI 写作论文的增加引发了关于学术诚信以及 LLM 在研究中的角色演变的问题。

**社区讨论**: 评论者对检测准确性表示怀疑。一位用户上传了 2011-2015 年的旧论文，结果得到了高比例机器写作分数（如 2015 年论文 74%），这表明该工具可能错误地将人类写作标记为 AI 写作。另一位用户质疑了方法论，特别是三个检测分数的组合方式，并指出缺乏开源代码阻碍了验证。

**标签**: `#AI`, `#arXiv`, `#academic publishing`, `#LLM`, `#detection`

---

<a id="item-13"></a>
## [美国提议立法将 AI 训练数据视为合理使用](https://simonwillison.net/2026/Jul/20/afraid-of-chinese-models/#atom-everything) ⭐️ 8.0/10

Ben Thompson 提议美国通过一项法律，明确将 AI 训练数据收集视为合理使用，并禁止禁止蒸馏的服务条款，以帮助美国开源模型与阿里通义千问 3.8 Max 等中国模型竞争。 该提案解决了 AI 实验室在未授权数据上训练却禁止蒸馏的矛盾，可能通过促进更开放的创新来重塑中美 AI 竞争格局。 Thompson 还指出，阿里改变了决定，以开放权重发布了通义千问 3.8 Max，可能受习近平最近鼓励开源讲话的影响。通义千问 3.8 Max 拥有 2.4 万亿参数，与 Kimi K3 的 2.8T 几乎一样大。

rss · Simon Willison · 7月20日 17:09

**背景**: 知识蒸馏是一种机器学习技术，较小‘学生’模型通过 API 查询从较大‘教师’模型学习。许多 AI 公司的服务条款禁止此类蒸馏，而它们自身却用网络抓取数据训练，引发版权争议。美国法律目前未明确训练数据是否属于合理使用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Knowledge_distillation">Knowledge distillation</a></li>
<li><a href="https://en.wikipedia.org/wiki/Qwen3.8-Max">Qwen3.8-Max</a></li>

</ul>
</details>

**标签**: `#AI policy`, `#copyright`, `#distillation`, `#open models`, `#Chinese models`

---

<a id="item-14"></a>
## [美国政府考虑限制中国开放权重 AI 模型，如 Kimi K3](https://www.axios.com/2026/07/20/ai-us-china-open-source-kimi) ⭐️ 8.0/10

据报道，特朗普政府正考虑实施新限制，阻止美国企业使用性价比高的中国开放权重 AI 模型，尤其是性能强劲且日益流行的 Kimi K3。 这项政策可能重塑全球 AI 格局，切断美国企业获取高性能、低成本模型的途径，可能抑制创新并增加美国企业成本，同时加深中美 AI 生态系统的分裂。 政府可能不会实施硬性封禁，而是通过采购规则、实体清单威胁和舆论等官僚障碍来阻止使用中国模型。白宫 AI 顾问 David Sacks 批评闭源巨头 OpenAI 和 Anthropic 试图通过政府干预消除开源竞争。

telegram · zaihuapd · 7月20日 11:49

**背景**: 开放权重 AI 模型会发布神经网络的训练参数（权重），让开发者能够微调并集成到应用中。Kimi K3 来自中国 AI 实验室 Moonshot AI，是一款先进的开放权重模型，采用了 Kimi Delta Attention（KDA）和 Attention Residuals（AttnRes）等架构创新，以提升跨序列长度和模型深度的性能。近期基准测试显示，中国开放权重模型在能力上已接近或匹敌美国同类产品，且成本显著更低。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://unrollnow.com/status/2077830229968683203">Thread By @ Kimi _Moonshot - Introducing Kimi K 3 : Open...</a></li>
<li><a href="https://www.linkedin.com/pulse/openais-open-weight-model-what-means-developers-ai-industry-tsi9f">OpenAI’s Open - Weight Model : What It Means for Developers and the...</a></li>

</ul>
</details>

**标签**: `#AI policy`, `#geopolitics`, `#open-source`, `#Kimi K3`, `#US-China`

---

<a id="item-15"></a>
## [普渡大学研究发现美军 App 含中俄代码](https://www.wired.com/story/apps-marketed-to-us-troops-are-shipping-chinese-and-russian-code/) ⭐️ 8.0/10

普渡大学一项研究发现，面向美军人员推广的 220 余款应用中，近三分之二嵌入了来自中国和俄罗斯的第三方代码，其中包括华为 SDK，该 SDK 可远程更新，存在潜伏风险。 这一发现意义重大，因为它揭示了针对美军人员的应用中存在严重的供应链漏洞，可能允许对手收集敏感数据或进行网络行动。研究结果凸显了在军事相关软件中对第三方代码进行更严格审查的必要性。 该研究测试了 220 款应用，包括基地指南、制服工具、银行及约会应用。虽然未观察到数据流向华为服务器，但 SDK 的远程更新能力意味着潜伏的恶意代码可能在日后被激活。

telegram · zaihuapd · 7月20日 13:42

**背景**: 来自不同供应商的第三方代码通常嵌入到应用中以添加功能，但这形成了软件供应链，其中任何组件的漏洞都可能危及整个应用。远程更新机制允许 SDK 在安装后修改其代码，增加了 SDK 开发者变得恶意或遭到入侵的风险。2020 年的五角大楼报告显示，对手曾利用商业位置数据监视中东地区的美国军人。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://safe.security/resources/insights/what-are-software-supply-chain-vulnerabilities-understanding-the-risks-how-to-mitigate-them/">What are Software Supply Chain Security and Vulnerabilities ?</a></li>
<li><a href="https://www.linkedin.com/pulse/owasps-top-3-threat-supply-chain-vulnerabilities-age-artificial-vgwxc">OWASP&#x27;s Top 3 Threat: Supply Chain Vulnerabilities in the Age of...</a></li>
<li><a href="https://www.techtiper.com/cybersecurity-risks-over-the-air-vehicle-updates/">Cars Updated Over the Internet Can Become Targets of Cyberattacks</a></li>

</ul>
</details>

**标签**: `#supply chain security`, `#national security`, `#mobile apps`, `#SDK risks`, `#cybersecurity`

---

<a id="item-16"></a>
## [谷歌 Frozen v2 芯片将 Gemini 效率提升 6-10 倍](https://www.quiverquant.com/news/Google+Reportedly+Developing+%E2%80%98Frozen+v2%E2%80%99+AI+Chip+to+Boost+Gemini+Efficiency) ⭐️ 8.0/10

据报道，谷歌正在开发一款内部代号为“Frozen v2”的服务器芯片，将 Gemini 模型的部分能力直接写入硬件，目标每瓦特产生的 token 数达到最新 TPU 的 6 到 10 倍，计划最早于 2028 年部署。 这款芯片可能大幅降低 AI 推理的成本和能耗，有望重塑云端 AI 的经济性。同时，它也凸显了谷歌为解决内部算力短缺（已限制对企业客户的服务能力）所做的努力。 Frozen v2 被定位为谷歌 TPU 的补充而非取代，项目目标之一是缓解内部算力短缺，这一问题已限制谷歌云为部分企业客户提供服务。

telegram · zaihuapd · 7月21日 01:01

**背景**: 谷歌的张量处理单元（TPU）是专为加速机器学习工作负载设计的定制 ASIC。在 AI 推理中，token 是处理文本的基本单位；每瓦特产生的 token 数衡量效率。通过将 Gemini 模型的某些部分固化到芯片中，Frozen v2 可能比面向通用模型的 TPU 实现更高效率。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://digg.com/tech/xbenabh7">Google Designs Frozen V 2 Chip For 6-10X More Efficient Gemini...</a></li>
<li><a href="https://www.morphllm.com/ai-inference">What Is AI Inference ? How Models Turn a Prompt Into Tokens</a></li>
<li><a href="https://www.allaboutcircuits.com/news/trillium-googles-tpu-powerhouse-behind-new-ai-models/">Trillium: Google’s TPU Powerhouse Behind Its New AI Models - News</a></li>

</ul>
</details>

**标签**: `#AI hardware`, `#Google`, `#TPU`, `#chip design`, `#inference efficiency`

---

<a id="item-17"></a>
## [X 安卓客户端已从零重建完成](https://x.com/i/status/2079273272274026718) ⭐️ 8.0/10

X 产品负责人 Nikita Bier 宣布，安卓版应用已从零开始全面重建，经过一年多努力，运行速度、流畅度和稳定性均显著提升。 此次重建使得在安卓上更快地迭代新功能成为可能，包括即将推出的视频回复和视频编辑器，未来新功能将优先在安卓平台发布，惠及数百万用户和开发者。 Cashtags 和自定义时间线已上线，Space 主持功能和老旧设备性能优化仍在完善中，视频回复和视频编辑器即将推出。

telegram · zaihuapd · 7月21日 02:27

**背景**: X（前身为 Twitter）历史上在安卓上的功能发布速度慢于 iOS。此次全栈重构旨在通过现代化代码库和提升性能来缩小这一差距，特别是在低端设备上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.bitcoin.com/x-launches-interactive-cashtags-with-real-time-stock-and-crypto-data-for-us-and-canada-iphone-users/">X Launches Interactive Cashtags With Real-Time Stock and Crypto...</a></li>
<li><a href="https://d33gy59ovltp76.cloudfront.net/news/x-custom-timelines-explained-here-s-how-to-build-your-perfect-feed">X &#x27; Custom Timelines &#x27; Explained: Here&#x27;s How to Build</a></li>
<li><a href="https://help.x.com/en/using-x/spaces">Spaces is a place to come together, built around the voices of the...</a></li>

</ul>
</details>

**标签**: `#Android`, `#X/Twitter`, `#app development`, `#performance optimization`

---
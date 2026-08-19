---
layout: default
title: "Horizon Summary: 2026-08-19 (ZH)"
date: 2026-08-19
lang: zh
---

> 从 36 条内容中筛选出 11 条重要资讯。

---

1. [莫德纳与默沙东宣布个性化 mRNA 癌症疫苗三期成功](#item-1) ⭐️ 10.0/10
2. [OpenRouter 加入 Stripe：据报 70 亿美元收购 AI 路由平台](#item-2) ⭐️ 9.0/10
3. [Go 1.27 发布：新增泛型方法、UUID 与 ML-DSA 包](#item-3) ⭐️ 9.0/10
4. [OpenAI 因关键网络攻击能力风险暂停 Astra 训练](#item-4) ⭐️ 9.0/10
5. [气象气球玩笑域名购买引发地缘政治风波](#item-5) ⭐️ 8.0/10
6. [OSINT 从业者利用几何与 CUDA 精确定位随机岛屿](#item-6) ⭐️ 8.0/10
7. [Cerebras 发布 CS-4：性能翻倍，功耗也翻倍](#item-7) ⭐️ 8.0/10
8. [同一 GRPO 配方在三个从零训练的 LLM 上结果迥异，且无清晰规模规律](#item-8) ⭐️ 8.0/10
9. [基于 180 万个 SIREN 的研究显示，对称性单独解释了权重空间感知差距的大部分](#item-9) ⭐️ 8.0/10
10. [OpenAI 披露 Codex 可能误删用户文件，新增多层防护](#item-10) ⭐️ 8.0/10
11. [百度推进昆仑芯片上市，中国客户转向国产 AI 芯片](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [莫德纳与默沙东宣布个性化 mRNA 癌症疫苗三期成功](https://wallstreetcn.com/articles/3779803) ⭐️ 10.0/10

2026 年 8 月 19 日，莫德纳和默沙东宣布，其个性化 mRNA 癌症疫苗联合 Keytruda 在黑色素瘤术后辅助治疗的三期试验中达到主要及关键次要终点，显著降低了复发和远处转移风险。具体改善幅度尚未公布，试验将继续评估总生存期。 这是个性化 mRNA 癌症疫苗首次在三期试验中取得成功，验证了“一人一针”精准免疫疗法可规模化落地。该结果可能为高风险黑色素瘤术后治疗建立新标准，并推动同类疫苗在其他癌种中的开发。 该疫苗作为黑色素瘤手术切除后的辅助疗法给药，而 Keytruda（帕博利珠单抗）是一种抗 PD-1 免疫检查点抑制剂，可增强 T 细胞活性。消息公布后，莫德纳股价盘初一度上涨 150%，默沙东涨逾 8%；具体风险降低幅度尚未公布。

telegram · zaihuapd · 8月19日 14:41

**背景**: 个性化 mRNA 癌症疫苗会根据患者的肿瘤基因突变定制，编码新抗原以训练免疫系统识别并攻击癌细胞。Keytruda 是一种检查点抑制剂，通过阻断 PD-1 通路增强 T 细胞抗肿瘤活性。辅助疗法是在主要手术之后给予的治疗，目的是降低癌症复发的风险。尽管这类疫苗已开展多年临床试验，这是首个在黑色素瘤中显示明确疗效的三期结果。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Personalized_mRNA_cancer_vaccine_therapy">Personalized mRNA cancer vaccine therapy</a></li>
<li><a href="https://en.wikipedia.org/wiki/Immune_checkpoint_inhibitor">Immune checkpoint inhibitor</a></li>
<li><a href="https://www.mayoclinic.org/diseases-conditions/cancer/in-depth/adjuvant-therapy/art-20046687">Adjuvant therapy: Treatment to keep cancer from returning - Mayo Clinic</a></li>

</ul>
</details>

**标签**: `#mRNA vaccine`, `#cancer immunotherapy`, `#melanoma`, `#clinical trial`, `#personalized medicine`

---

<a id="item-2"></a>
## [OpenRouter 加入 Stripe：据报 70 亿美元收购 AI 路由平台](https://openrouter.ai/blog/announcements/openrouter-is-joining-stripe/) ⭐️ 9.0/10

Stripe 正在收购 OpenRouter，据报交易金额超过 70 亿美元，该消息已在 OpenRouter 博客上公布。此次收购证实了此前的传闻，也标志着这家支付公司向 AI 模型市场扩张。 这是 AI 基础设施和开发者工具领域的一次重大整合：一家支付巨头吸收了使用最广泛的 AI 模型路由与聚合服务之一。依赖 OpenRouter 单一 API 来访问和比较数百个模型的开发者，可能会看到它与 Stripe 的计费、计量和 agent 支付系统更紧密地整合。 OpenRouter 提供统一的、兼容 OpenAI 的 API 网关，覆盖 60 多家提供商的 400 多个模型，可根据成本、速度和可靠性自动路由，并将计费集中到一个账户。社区用户指出，默认路由会选择最便宜的提供商，同时该平台也提供基于真实世界模型选择数据训练的 Auto Router。

hackernews · rvz · 8月19日 17:32 · [社区讨论](https://news.ycombinator.com/item?id=49364559)

**背景**: 像 OpenRouter 这样的 AI 模型聚合器位于开发者和模型提供商之间，让一次 API 调用就能访问多个大语言模型，开发者无需单独管理不同账户和账单。这类平台通过让用户比较模型并按价格或性能路由请求，降低了成本和复杂性。随着 AI 提供商数量不断增长，这一能力变得越来越有价值，而 Stripe 的收购也反映了金融科技公司向 AI 基础设施和模型市场扩张的更广泛趋势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/08/19/stripe-openrouter-fintech-ai-model-marketplace-.html">Stripe to buy OpenRouter as fintech expands deeper into AI</a></li>
<li><a href="https://aiwiki.ai/wiki/openrouter">OpenRouter - AI Wiki</a></li>
<li><a href="https://openrouter.ai/">The unified interface for every model . Find the best models &amp; prices...</a></li>

</ul>
</details>

**社区讨论**: 评论区总体积极，许多长期用户称赞该产品，并希望 Stripe 能成为好的守护者。也有人对 AI 基础设施进一步集中到中间层 PaaS 表示担忧，并以 Open Banking 为例质疑“Open”这一名称的含义。还有人强调 OpenRouter 除路由以外的功能，并预测 Stripe 会利用它构建 agent 计量和计费基础设施。

**标签**: `#acquisition`, `#ai-infrastructure`, `#openrouter`, `#stripe`, `#api-routing`

---

<a id="item-3"></a>
## [Go 1.27 发布：新增泛型方法、UUID 与 ML-DSA 包](https://go.dev/blog/go1.27) ⭐️ 9.0/10

Go 1.27 版本首次支持泛型方法，方法现在可以拥有类型参数。新版本还新增了标准库 UUID 包和后量子密码学的 ML-DSA 包，并采用 Russ Cox 的 uscale 算法改进了浮点数解析与格式化性能。 这是 Go 语言的一次重大演进，消除了泛型设计中的一个长期限制，并为开发者提供了标准的 UUID 标识符工具和面向未来的量子安全签名算法。这些改进将影响所有 Go 开发者，从 API 框架的设计者到加密系统使用者。 泛型方法允许方法带类型参数，但不能用于实现接口方法，因此接口满足的既有规则保持不变。新的 crypto/mldsa 包实现了 NIST 标准化的 ML-DSA 签名算法，浮点数解析器则改用 Russ Cox 的 uscale 算法以提升性能和正确性。

hackernews · database64128 · 8月19日 18:33 · [社区讨论](https://news.ycombinator.com/item?id=49365405)

**背景**: Go 在 1.18 版本引入泛型，但此前一直禁止泛型方法，这一立场直到本版本才改变。ML-DSA（原 Dilithium）是一种基于格的数字签名算法，NIST 于 2024 年将其定为后量子密码标准。标准库纳入这类原语表明，抵御量子计算攻击正在成为安全敏感软件的基本要求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.gopherguides.com/articles/golang-generic-methods">Generic Methods Arrive in Go 1.27 - Gopher Guides</a></li>
<li><a href="https://en.wikipedia.org/wiki/ML-DSA">ML-DSA</a></li>
<li><a href="https://www.linkedin.com/pulse/two-ways-sign-quantum-world-ml-dsa-vs-slh-dsa-zenv-quantum-kcbkf">Two Ways to Sign in a Quantum World: ML - DSA vs SLH-DSA</a></li>

</ul>
</details>

**社区讨论**: 评论者对密码学团队的积极态度表示赞赏，并有人引用了 Filippo Valsorda 关于尽早部署后量子密码学的文章。还有人预测会出现一波从 google/uuid 迁移到新标准 uuid 包的 pull request，另一些评论则提到了泛型方法带来的便利以及 Go 博客缺少语法高亮等小问题。

**标签**: `#Go`, `#release`, `#generics`, `#cryptography`, `#programming languages`

---

<a id="item-4"></a>
## [OpenAI 因关键网络攻击能力风险暂停 Astra 训练](https://openai.com/index/pacing-model-development-cyber-capabilities/) ⭐️ 9.0/10

2026 年 8 月 18 日，OpenAI 表示，其即将推出的 Astra 模型可能已达到“关键”级网络攻击能力，因此暂停了两周的强化学习训练。该公司还引入了新的自动化调查系统，以加强安全监控。 这是一个领先 AI 实验室因网络安全风险而主动放缓前沿模型研发的典型案例，可能为行业树立先例。它也可能影响围绕 AI 安全以及模型部署节奏的监管讨论。 监控开销约占被监控推理算力的 20%。暂停措施同时影响 Astra 模型和 OpenAI 规模最大的前沿强化学习运行，后者在安全评估完成前仍处于暂停状态。

telegram · zaihuapd · 8月19日 02:02

**背景**: 前沿 AI 模型通常通过强化学习进行优化，即模型通过获得奖励学会期望的行为。OpenAI 为网络安全等领域定义了内部能力门槛，当新模型接近“关键”门槛时，其安全框架会触发预防性措施。新的自动化调查系统采用多阶段流程来检测异常模型行为，并可在 30 分钟内发出警报。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://luwai.fr/en/resources/cybersecurite-ia-seuil-critique-openai-pme-2026-08-17">Cybersecurity : OpenAI&#x27;s AI Crosses a Critical Threshold</a></li>
<li><a href="https://nairametrics.com/2026/08/07/openai-flags-critical-cybersecurity-risk-in-ai-model-weeks-after-hugging-face-incident/">OpenAI flags critical cybersecurity risk in AI model... - Nairametrics</a></li>
<li><a href="https://opendatascience.com/openai-slows-frontier-ai-training-as-astra-approaches-critical-cybersecurity-threshold/">OpenAI Slows Frontier AI Training as Astra Approaches Critical ...</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#AI safety`, `#cyber capabilities`, `#model development`, `#RL training`

---

<a id="item-5"></a>
## [气象气球玩笑域名购买引发地缘政治风波](https://sprocketfox.io/xssfox/2026/08/19/sondehub-and-war/) ⭐️ 8.0/10

一位爱好者在追踪气象气球的业余项目中出于玩笑注册了一个域名，结果意外引起军方和政府机构的关注，使业余无线电与开源地图社区被卷入地缘政治紧张局势。这位域名所有者在个人博客中详细讲述了事件经过，展示了一个趣味项目如何与情报和国防事务产生交集。 这件事之所以重要，是因为它展现了民间爱好者基础设施——气象气球探空仪、APRS 和开源情报——如何在意想不到的层面与国家安全产生交集。它也引发了对爱好者自治、数据透明度，以及政府如何应对开放、去中心化追踪网络的思考。 事件涉及一个用于气象气球无线电探空仪追踪服务的域名，该服务与 Habhub 等社区平台类似；文章中还有瑞士仪器厂商 Meteolabor 的来信，提到发射机出于“战略考虑”会在一定时间后或电池耗尽时关闭。评论者还提到 OpenStreetMap 基础设施运营者经常收到来自 .mil、.gov、.edu 和地理顶级域名等来源的奇怪请求。

hackernews · kareiva · 8月19日 11:21 · [社区讨论](https://news.ycombinator.com/item?id=49360015)

**背景**: 无线电探空仪（radiosonde）是由气象气球携带的电池供电仪器，用于测量大气参数并通过无线电（通常在 403 MHz 或 1680 MHz 频段）将数据传回地面。业余无线电爱好者和技术爱好者会利用自动分组报告系统（APRS）和 Habhub 等平台近乎实时地追踪这些气球，这本质上也是一种基于公开无线电信号和地图数据的开源情报（OSINT）活动。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Radiosonde">Radiosonde</a></li>
<li><a href="https://en.wikipedia.org/wiki/Automatic_Packet_Reporting_System">Automatic Packet Reporting System - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Open-source_intelligence">Open-source intelligence - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍表示赞赏，称这篇文章引人入胜，而且“没有经过 LLM 加工、直接来自人脑”令人耳目一新。有人分享了多年前放飞气象气球的怀旧经历，也有人将域名所有者的遭遇与 OpenStreetMap 等基础设施运营者经常收到的奇怪执法请求相类比。

**标签**: `#geopolitics`, `#radio`, `#security`, `#OSINT`, `#technology-and-society`

---

<a id="item-6"></a>
## [OSINT 从业者利用几何与 CUDA 精确定位随机岛屿](https://yassa9.github.io/osint/gralhix-004/) ⭐️ 8.0/10

OSINT 从业者 Yassa 发布的一篇博客文章展示了如何将几何推理与 CUDA 加速计算相结合，仅凭一张未知岛屿的照片就确定了其在地球上的确切位置。 这一案例意义重大，因为它展示了一条结合经典几何与 GPU 并行计算来解决困难地理定位问题的新颖且相对可实现的路线。其核心思路——将地形或海岸线轮廓与地图进行匹配——也被用于导弹/无人机导航（TERCOM）以及 NASA 火星 2020 着陆系统。 据文章介绍，作者使用 CUDA 对地图瓦片和几何特征的搜索进行并行化，从而加快了穷举比较的速度。作者还利用照片中太阳的位置（正午位于左侧）预先推断出大致方向为西，再运行匹配算法。

hackernews · yassa9 · 8月19日 12:19 · [社区讨论](https://news.ycombinator.com/item?id=49360545)

**背景**: 开源情报（OSINT）是指收集和分析公开可用数据进行调查的实践，而根据照片中的视觉线索定位拍摄地是经典的 OSINT 挑战。CUDA 是 NVIDIA 的并行计算平台与编程模型，它允许开发者将 GPU 算力用于图像处理、特征匹配等非图形任务。几何分析——例如通过估测太阳方位来判断东南西北——有助于在开始计算量巨大的匹配之前大幅缩小搜索范围。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.nvidia.com/cuda/cuda-programming-guide/index.html">CUDA Programming Guide — CUDA Programming Guide</a></li>
<li><a href="https://www.osinttechniques.com/">OSINT Techniques - Home</a></li>
<li><a href="https://pro.arcgis.com/en/pro-app/3.4/help/data/imagery/introduction-to-ortho-mapping.htm">What is photogrammetry?—ArcGIS Pro | Documentation</a></li>

</ul>
</details>

**社区讨论**: 评论者大体持正面态度，并带有怀旧情绪，称赞文章写作风格。多位评论将其联系到用于导弹和无人机的“地形轮廓匹配”（TERCOM）技术，以及 JPL 用于缩小火星 2020 着陆椭圆的“相对地形导航”；有人指出利用太阳位置这一捷径其实已暗示“大致朝西”；还有人指出这篇文章紧挨着一篇有关“避免建设可能被警察国家使用的技术”的文章，显得颇为讽刺。

**标签**: `#geolocation`, `#CUDA`, `#OSINT`, `#geometry`, `#image-processing`

---

<a id="item-7"></a>
## [Cerebras 发布 CS-4：性能翻倍，功耗也翻倍](https://newsletter.semianalysis.com/p/cerebrass-next-generation-cs-4-fast) ⭐️ 8.0/10

Cerebras 发布了下一代机架级 AI 系统 CS-4，宣称其性能是 CS-3 的两倍，同时功耗也是两倍。CS-4 是全新 Cerebras Nexus 平台的首款产品，每套系统集成三个 WSE-3 Turbo 处理器。 这一发布标志着 AI 加速器竞赛中的重大进展，对大型语言模型而言，其推理速度可能比基于 GPU 的系统快 30 倍。这可能进一步挑战 Nvidia 在 AI 硬件领域的主导地位，并使部署前沿 AI 的机构受益。 CS-4 是基于 Cerebras Nexus 架构的机架级系统，配备三个 WSE-3 Turbo 处理器。Cerebras 声称其性能翻倍，功耗也翻倍，这一取舍凸显了晶圆级计算的高能耗需求。

rss · Semianalysis · 8月19日 01:32

**背景**: Cerebras 开发晶圆级引擎（WSE），即尺寸相当于整个硅晶圆的大型芯片，以避免连接许多较小芯片时的通信瓶颈。该公司于 2019 年首次推出 WSE，其产品面向高性能 AI 训练和推理。晶圆级技术面临制造良率和功率密度等挑战，Cerebras 每一代产品都在持续解决这些问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cerebras.ai/cs4">Product - System - Cerebras</a></li>
<li><a href="https://www.servethehome.com/cerebras-intros-faster-wse-3-turbo-processor-and-first-rack-scale-cs-4-system/">Cerebras Intros Faster WSE-3 Turbo Processor and First Rack- Scale ...</a></li>
<li><a href="https://www.envisioning.com/research/wintermute/wafer-scale-ai-systems">Wafer - Scale AI Systems | Wintermute | Envisioning</a></li>

</ul>
</details>

**标签**: `#AI hardware`, `#Cerebras`, `#Semiconductors`, `#ML accelerators`

---

<a id="item-8"></a>
## [同一 GRPO 配方在三个从零训练的 LLM 上结果迥异，且无清晰规模规律](https://www.reddit.com/r/MachineLearning/comments/1vszsit/same_grpo_recipe_on_three_fromscratch_llms/) ⭐️ 8.0/10

一名独立研究者从零训练了三个 LLM（353M/316M/672M 参数），并对它们应用完全相同的 SFT+GRPO 后训练流程（相同课程、奖励函数和超参数）。结果 GRPO 损害了其中两个模型，对另一个几乎无影响，未显示与模型规模或架构的清晰关系。 这个记录详尽的负面结果说明，GRPO 的效果未必能随模型规模或架构可预测地迁移，这对依赖小规模实验为更大模型调参的研究者很重要。它还指出了格式不匹配、课程阶段遗忘等常见混杂因素，这些因素可能被误认为通用能力下降。 预训练验证损失按预期下降（2.8659→2.7844→2.5885），但 GRPO 后的 WikiText 困惑度相比 SFT 分别上升：V1 仅+0.2%，V2 达+52%，V3 为+5%。作者指出这不是受控实验——V2 与 V3 之间同时改变了参数量、token 数、数据混合和注意力机制——并且 GRPO 使用裸求解器模板，而 SFT 使用聊天格式。

reddit · r/MachineLearning · /u/john\_enev · 8月19日 21:30

**背景**: GRPO（Group Relative Policy Optimization，组相对策略优化）是一种用于 RLHF 式后训练的强化学习方法，因 DeepSeek-R1 而流行；它对每个提示采样多个补全，用奖励模型或奖励函数评分，并相对于该组补全的平均奖励更新策略，因此不需要单独的价值网络。GRPO 后训练通常在监督微调（SFT）之后进行，用于让 LLM 学会推理或格式遵循行为。三个模型除了参数量不同，注意力机制也不同：V1 使用 MHA，V2 使用 Differential Attention（差分注意力）加 GQA，V3 使用 XSA 加 GQA。由于多个因素同时变化，作者强调这不是受控的规模实验。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ghost.oxen.ai/why-grpo-is-important-and-how-it-works/">Why GRPO is Important and How it Works</a></li>
<li><a href="https://cameronrwolfe.substack.com/p/grpo">Group Relative Policy Optimization (GRPO)</a></li>
<li><a href="https://www.emergentmind.com/topics/differential-attention-da">Differential Attention (DA) Mechanisms</a></li>

</ul>
</details>

**标签**: `#GRPO`, `#RLHF`, `#LLM post-training`, `#scaling laws`, `#empirical study`

---

<a id="item-9"></a>
## [基于 180 万个 SIREN 的研究显示，对称性单独解释了权重空间感知差距的大部分](https://www.reddit.com/r/MachineLearning/comments/1vswdnf/how_much_of_the_weightspace_perception_gap_is/) ⭐️ 8.0/10

在一项新的实证研究中，作者在 MNIST、FashionMNIST 和 CIFAR-10 上拟合了约 180 万个 SIREN 式隐式神经表示，发现仅随机化保持函数不变的对称群，就会破坏 MNIST 共享初始化与随机初始化差距中 80.4 个精度点里的 79.1 个。该工作还证明，对于单隐藏层正弦网络，在模 D\_inf wr S\_n 对称群的意义下可得到一般的可辨识性。 这项工作区分了两个常被混淆的主张：对称性足以复制几乎全部的退化，但自然的共享初始化与随机初始化差距未必由对称性因果地造成。它还进一步澄清了权重空间学习的核心动机——直接处理权重是否更多是计算层面的理由，而非信息层面的理由。 对于隐藏的正弦神经元，保持函数不变的变换生成无限二面体群 D\_inf = Z ⋊ Z\_2，加入排列后得到层作用 D\_inf wr S\_n。在消融实验中，符号翻转约占诱导损失的 63 个精度点，神经元重标号约占 15 个，整数相位平移约占 1 个；按 FLOPs 匹配后，函数空间推理仍优于最佳权重空间读取器（95.3%对 64.4%）。完整代码、论文和预注册已在 GitHub 公开。

reddit · r/MachineLearning · /u/ITheClixs · 8月19日 19:24

**背景**: 权重空间学习把训练后神经网络的参数本身当作数据，目标是直接从权重读出语义信息。一个主要障碍是参数对称性：交换隐藏单元、翻转符号或平移相位都可能保持网络函数不变，却让两个参数向量在下游模型看来差异很大。SIREN 是使用正弦激活函数的隐式神经表示，因此其对称性不仅包括排列和符号翻转，还包括仿射而非线性的整数π相位平移。这些对称性正是独立拟合的网络在权重空间中看起来语义相距甚远的关键原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.emergentmind.com/topics/weight-space-learning">Weight Space Learning in Neural Networks</a></li>
<li><a href="https://arxiv.org/abs/2506.13018">[2506.13018] Symmetry in Neural Network Parameter Spaces</a></li>
<li><a href="https://weight-space-learning.github.io/">Overview | ICLR 2025 Workshop on Weight Space Learning</a></li>

</ul>
</details>

**标签**: `#weight-space learning`, `#SIREN`, `#parameter symmetry`, `#implicit neural representations`, `#neural networks`

---

<a id="item-10"></a>
## [OpenAI 披露 Codex 可能误删用户文件，新增多层防护](https://x.com/thsottiaux/status/2089891927659585918) ⭐️ 8.0/10

OpenAI 披露其编程代理 Codex（基于 GPT-5.6）近期收到少量模型执行超出用户要求的破坏性操作的报告，最严重的模式是用于清理临时文件的命令可能误删用户文件。公司已在多层加装防护，包括要求模型删除前先检查目标、改用全新临时目录、避免复用系统环境变量，拦截高风险删除命令并升级审查。 这一事件意义重大，因为 Codex 是广泛使用的 AI 编程代理，能够以用户权限执行命令，意外破坏性操作可能导致真实数据丢失。此次披露与防护改进提高了 AI 代理的安全标准，对依赖自主编码工具的开发者与组织都有影响。 OpenAI 表示最严重的模式是清理临时文件的命令可能误删用户文件。缓解措施包括删除前检查目标、改用全新临时目录、避免复用系统环境变量，高风险删除命令会被拦截并升级审查，同时收紧 Full access 权限被误开启的门槛。

telegram · zaihuapd · 8月19日 05:01

**背景**: OpenAI Codex 是 OpenAI 于 2025 年 4 月以 Codex CLI 形式发布的 AI 编程代理，可通过 ChatGPT 网页应用、桌面应用及多种 IDE 集成使用。GPT-5.6 是 OpenAI 于 2026 年 7 月发布的大语言模型系列，具备较强的编码能力。基于 GPT-5.6 的 Codex 可在本地环境中执行命令。Full access 是允许 Codex 无需逐次批准即可运行的权限配置，因此一旦模型误发破坏性命令，风险会更高，此次新增的防护正是针对这类场景。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OpenAI_Codex_%28AI_agent%29">OpenAI Codex (AI agent) - Wikipedia</a></li>
<li><a href="https://openai.com/index/gpt-5-6/">GPT-5.6: Frontier intelligence that scales with your ambition | OpenAI</a></li>
<li><a href="https://openai.com/codex/">Codex in ChatGPT | AI Coding Agents for Software Engineering | OpenAI</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#Codex`, `#AI safety`, `#File deletion`, `#Security`

---

<a id="item-11"></a>
## [百度推进昆仑芯片上市，中国客户转向国产 AI 芯片](https://www.theregister.com/systems/2026/08/19/baidu-says-chinese-buyers-want-local-ai-chips-due-to-supply-chain-issues/5289377) ⭐️ 8.0/10

百度正推进昆仑 AI 芯片业务的分拆上市，中国客户日益加速采用国产芯片。公司第二季度云基础设施租赁收入同比增长 50%，接近 11 亿美元，GPU 云收入同比增长 283%。 这标志着 AI 硬件格局的重大转变，中国买家正因供应紧张而加速转向国产芯片。百度的进展可能进一步推动国产 AI 芯片普及，并影响全球半导体供应链格局。 百度昆仑芯片兼容 CUDA，已用于百度云，并已销售给华为、中兴等厂商。公司表示推理需求持续增长，而 AI 芯片供应可能长期受限。

telegram · zaihuapd · 8月19日 06:38

**背景**: 昆仑是百度自研的 AI 芯片系列，于 2018 年首次推出，面向数据中心和边缘工作负载；2021 年的昆仑 II 号称与英伟达 A100 相当。该芯片被设计为在百度生态中工作，包括 PaddlePaddle 等深度学习框架，并通过百度云对外提供。兼容 CUDA 是关键特性，便于在以 Nvidia 为主的环境中采用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kunlunxin">Kunlunxin - Wikipedia</a></li>
<li><a href="https://www.zdnet.com/article/baidu-creates-kunlun-silicon-for-ai/">Baidu creates Kunlun silicon for AI | ZDNET</a></li>
<li><a href="https://www.packtpub.com/en-mt/learning/tech-news/baidu-releases-kunlun-ai-chip-chinas-first-cloud-to-edge-ai-chip">Baidu releases Kunlun AI chip , China’s first cloud-to-edge AI chip</a></li>

</ul>
</details>

**标签**: `#AI chips`, `#Baidu`, `#semiconductors`, `#supply chain`, `#China`

---
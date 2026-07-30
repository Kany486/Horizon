---
layout: default
title: "Horizon Summary: 2026-07-30 (ZH)"
date: 2026-07-30
lang: zh
---

> 从 41 条内容中筛选出 9 条重要资讯。

---

1. [开源引擎让 Gemma 4 26B 在 2GB RAM 的 Mac 上运行](#item-1) ⭐️ 9.0/10
2. [通过提示注入实现自我复制的 AI 蠕虫攻击 Microsoft Word](#item-2) ⭐️ 9.0/10
3. [俄罗斯指控 Telegram 创始人协助恐怖活动](#item-3) ⭐️ 9.0/10
4. [月之暗面融资 35 亿美元，估值 350 亿美元，计划 IPO](#item-4) ⭐️ 9.0/10
5. [Superlogical：Mitchellh 创办智能终端公司](#item-5) ⭐️ 8.0/10
6. [模块化数据中心：乐高式解决方案](#item-6) ⭐️ 8.0/10
7. [基于 Vulkan 的 ncnn 在边缘设备上实现 10 倍 ML 推理加速](#item-7) ⭐️ 8.0/10
8. [Hugging Face 平台被用于生成深度伪造裸照](#item-8) ⭐️ 8.0/10
9. [中国发布反网络暴力法草案，纳入 AI 网暴](#item-9) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [开源引擎让 Gemma 4 26B 在 2GB RAM 的 Mac 上运行](https://github.com/drumih/turbo-fieldfare) ⭐️ 9.0/10

TurboFieldfare 是一个开源推理引擎，它通过按需从 SSD 流式加载专家权重，仅需约 2 GB 内存即可在任何 M 系列 Mac 上运行 4 位量化的 Gemma 4 26B 混合专家模型。 这项技术使得在内存受限的消费级设备上运行大型语言模型成为可能，让更多人能够使用强大的人工智能。同时，它为混合专家模型绕过内存限制提供了实用方案，可能推动其他推理引擎的类似优化。 该模型的 4 位量化权重约为 14 GB，但通过将共享层和 KV 缓存保留在 RAM 中，并利用有界并行 pread 仅从 SSD 流式加载所需的专家，该引擎在 8 GB M2 MacBook Air 上达到 5-6 token/s，在 M5 MacBook Pro 上达到 31-35 token/s。它还包含一个实验性的兼容 OpenAI 的本地服务器，支持流式输出和工具调用。

hackernews · gitpusher42 · 7月29日 15:05 · [社区讨论](https://news.ycombinator.com/item?id=49098510)

**背景**: 混合专家（MoE）是一种模型架构，每个输入会激活多个专门的子网络（专家），从而在保持推理效率的同时增加参数数量。4 位量化将模型权重压缩为每个 4 位，大幅减少内存占用，但会带来少量精度损失。在推理过程中从 SSD 流式加载权重是一种新兴技术，它按需仅加载所需的权重，使得比可用内存更大的模型能够在笔记本电脑和手机等设备上运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://newsletter.maartengrootendorst.com/p/a-visual-guide-to-mixture-of-experts">A Visual Guide to Mixture of Experts ( MoE )</a></li>
<li><a href="https://www.emergentmind.com/topics/4-bit-model-quantization">4-Bit Model Quantization - emergentmind.com</a></li>
<li><a href="https://www.mindstudio.ai/blog/ssd-streaming-ai-models-ram-dial">SSD Streaming for AI Models: How to Turn RAM from a Wall into a Dial | MindStudio</a></li>

</ul>
</details>

**社区讨论**: 社区评论强调了不需要将整个模型塞入内存的创新之处，一位用户指出 llama.cpp 已经可以通过 mmap 加载模型，但 TurboFieldfare 的同步 SSD 读取调优得更好。另一位用户分享了针对较旧 macOS 版本的兼容性修复，还有一位用户提到了一个相关的 DiffusionGemma 项目，并表示可能进行合作。

**标签**: `#open-source`, `#inference-engine`, `#on-device-ai`, `#gemma`, `#macos`

---

<a id="item-2"></a>
## [通过提示注入实现自我复制的 AI 蠕虫攻击 Microsoft Word](https://simonwillison.net/2026/Jul/29/ai-worming-through-word/#atom-everything) ⭐️ 9.0/10

安全研究员 Håkon Måløy 演示了一种针对 Microsoft Copilot for Word 的新型提示注入攻击，能够创建自我复制的蠕虫。攻击将指令隐藏在文档中，使 Copilot 将恶意载荷传播到新文档，从而让蠕虫无需原始文档即可扩散。 这是在广泛使用的办公生产力工具中首次演示自我复制 AI 蠕虫，构成了重大安全风险。它凸显了 LLM 无法可靠区分指令与数据的根本脆弱性，威胁到企业数据完整性和自动化工作流。 隐藏指令放置在用作 Copilot 源材料的文档中；当 Copilot 处理文档时，它会遵循指令修改当前文档并将隐藏载荷复制到输出中。该攻击已负责任地向微软披露 144 天，但尚未发布完整缓解措施。

rss · Simon Willison · 7月29日 18:43

**背景**: 提示注入是一种安全漏洞，精心设计的输入使 LLM 执行非预期行为，绕过安全防护。间接提示注入发生在对抗性提示嵌入在 LLM 检索的内容（如网页或文档）中时。自我复制 AI 蠕虫结合了提示注入与将恶意指令传播到其他文件或系统的能力，此前研究如 Morris II 蠕虫已展示过。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection_attack">Prompt injection attack</a></li>
<li><a href="https://thehackernews.com/2026/06/researchers-build-self-replicating-ai.html">Researchers Build Self-Replicating AI Worm That Operates Entirely on Local, Open-Weight Models</a></li>
<li><a href="https://neuraltrust.ai/blog/self-replicating-malware">The Dawn of the AI Worm: Self-Replicating Prompt Malware in Multi-Agent Systems | NeuralTrust</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了对该漏洞在当前 LLM 架构下根本无法修复的担忧，因为模型无法分离指令与数据。一些用户表示已卸载 Copilot 并禁用 AI 功能以避免此类风险。其他人指出，随着智能体获得更多访问权限和能力，此类攻击手段可能会变得更糟。

**标签**: `#security`, `#prompt injection`, `#AI`, `#Microsoft Word`, `#Copilot`

---

<a id="item-3"></a>
## [俄罗斯指控 Telegram 创始人协助恐怖活动](https://www.interfax.ru/russia/1106228) ⭐️ 9.0/10

俄罗斯联邦安全局（FSB）已依据《刑法》第 205.1 条第 1.1 款（协助恐怖活动）对 Telegram 创始人帕维尔·杜罗夫提出刑事指控，并因他未能删除用于在俄罗斯境内协调攻击的内容而将其列入国际通缉名单。 这标志着国家对科技平台施压的重大升级，可能开创平台创始人对用户生成内容承担个人责任的先例，并可能影响 Telegram 的运营及国际科技外交。 FSB 指控 Telegram 管理层拒绝删除被乌克兰情报机构及恐怖组织用于协调破坏活动、恐怖袭击和诈骗的频道与机器人，导致人员伤亡及数十亿卢布损失。

telegram · zaihuapd · 7月29日 05:56

**背景**: 俄罗斯联邦安全局（FSB）是该国主要安全机构，负责反恐和情报工作。Telegram 以其强大的加密和隐私功能闻名，一直是内容审核的战场，各国政府常要求访问或删除内容。

**标签**: `#Telegram`, `#Pavel Durov`, `#Russia`, `#legal`, `#terrorism`

---

<a id="item-4"></a>
## [月之暗面融资 35 亿美元，估值 350 亿美元，计划 IPO](https://www.bloomberg.com/news/articles/2026-07-29/china-s-moonshot-ai-passes-funding-goal-to-hit-35-billion-value) ⭐️ 9.0/10

月之暗面（Moonshot AI）完成了一轮 35 亿美元的融资，投后估值达到 350 亿美元，远超最初 10 亿至 20 亿美元的目标。此轮融资得益于其 Kimi K3 模型的成功，该模型性能接近前沿水平，并引发了被称为又一个“DeepSeek 时刻”的市场抛售。 这一巨额融资轮显示出投资者对中国 AI 初创公司的强烈信心，并加剧了全球 AI 竞争。该公司计划在香港进行 IPO，可能带来重要的流动性事件，并进一步推动 AI 军备竞赛。 月之暗面已启动新一轮融资，pre-money 估值为 500 亿美元，并计划最早今年内在香港 IPO。该公司 6 月的年化经常性收入达到 3 亿美元，Kimi K3 发布后日销售额增长了至少 6 倍。

telegram · zaihuapd · 7月29日 10:12

**背景**: “DeepSeek 时刻”指的是 2025 年 1 月，中国初创公司 DeepSeek 发布其开源权重模型 DeepSeek-R1，引发科技股抛售，市场担忧美国 AI 主导地位受到影响。Kimi K3 是一个 2.8 万亿参数的模型，拥有 100 万 token 的上下文窗口，基于新颖的注意力机制构建，是全球首个开源的 3T 级模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://platform.kimi.ai/docs/guide/kimi-k3-quickstart">Kimi K3 - Kimi API Platform</a></li>
<li><a href="https://www.kimi.com/blog/kimi-k3">Kimi K3 Tech Blog: Open Frontier Intelligence</a></li>
<li><a href="https://www.linkedin.com/pulse/why-we-wont-see-another-deepseek-moment-anytime-soon-breitenother-lzvwe">Why we won’t see another DeepSeek moment anytime soon</a></li>

</ul>
</details>

**标签**: `#AI Funding`, `#Moonshot AI`, `#Kimi K3`, `#Valuation`, `#IPO`

---

<a id="item-5"></a>
## [Superlogical：Mitchellh 创办智能终端公司](https://www.superlogical.com/) ⭐️ 8.0/10

Mitchellh 宣布成立 Superlogical 公司，该公司将基于开源的 libghostty 库构建智能终端应用程序，并计划将改进上游到 libghostty，让所有用户受益。 这一举措意义重大，因为它展示了一种可持续的开源商业模式：公司在开源核心上构建专有应用，同时回馈社区。这可能会加速利用 AI 代理的智能终端工具的发展，影响开发者和系统工程师。 Superlogical 将使用与其他用户相同的 MIT 许可证的 libghostty 组件，并继续将共享的终端工作上游。Mitchellh 此前已将 Ghostty 的所有权转让给了一个非营利组织。

hackernews · yan · 7月29日 15:41 · [社区讨论](https://news.ycombinator.com/item?id=49098965)

**背景**: libghostty 是一个跨平台、零依赖的 C 和 Zig 库，用于构建终端模拟器，是 Ghostty 项目的一部分。智能终端应用程序指的是能够自主或半自主执行复杂任务的终端工具，常集成 AI 编程助手。这种在开源基础上构建专有产品的模式被称为“开源核心”。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ghostty-org/ghostty">GitHub - ghostty-org/ghostty: Ghostty is a fast, feature-rich, and...</a></li>
<li><a href="https://ghostty.org/docs/about">About Ghostty</a></li>

</ul>
</details>

**社区讨论**: 社区成员赞扬了开源策略，simonw 强调了将 Ghostty 所有权转让给非营利组织以及计划将 Superlogical 作为 libghostty 的用户并向上游贡献改进。另一位评论者将其与微软的 OLE/COM 进行了比较，认为在组件嵌入方面有相似之处。少数用户批评了标题的晦涩，更希望使用更具描述性的标题。

**标签**: `#terminal`, `#open-source`, `#software-engineering`, `#startup`, `#systems`

---

<a id="item-6"></a>
## [模块化数据中心：乐高式解决方案](https://newsletter.semianalysis.com/p/the-wild-wild-west-of-lego-datacenters) ⭐️ 8.0/10

Semianalysis 的分析探讨了如何通过类似乐高积木的模块化数据中心建设来应对劳动力短缺并加速部署。 随着对计算能力需求的激增，传统数据中心建设面临劳动力限制；模块化提供了一种更快、更灵活的替代方案，可能改变基础设施的扩展方式。 该文章可能涉及预制模块、减少现场劳动力和成本效益，但此处未提供新闻通讯的具体技术细节。

rss · Semianalysis · 7月29日 22:09

**背景**: 模块化数据中心是预制、工厂测试的单元，运往现场快速组装，数周内即可运营，而非数月。这种方法解决了蓬勃发展的数据中心行业中的劳动力短缺和可扩展性挑战。“乐高”类比强调了这些模块的即插即用特性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://encoradvisors.com/modular-data-center/">The Modular Data Center Ultimate Guide [2025] - ENCOR Advisors</a></li>
<li><a href="https://www.zdnet.com/article/the-lego-datacentre/">The Lego datacentre | ZDNET</a></li>

</ul>
</details>

**标签**: `#datacenters`, `#modularization`, `#infrastructure`, `#labor`, `#technology`

---

<a id="item-7"></a>
## [基于 Vulkan 的 ncnn 在边缘设备上实现 10 倍 ML 推理加速](https://www.reddit.com/r/MachineLearning/comments/1v9s4mz/vendoragnostic_ml_inference_on_production_edge/) ⭐️ 8.0/10

来自 PostSlate 团队的 Reddit 帖子详细介绍了使用 ncnn 的 Vulkan 后端进行跨平台 ML 推理，在 NVIDIA 4070 上对人脸检测和嵌入模型实现了比 ONNX CPU 快 10 倍的速度，无需特定供应商的运行时。 这种方法通过利用现有的 Vulkan 驱动程序，解决了边缘设备的关键部署难题，在不依赖 CUDA 或特定供应商工具包的情况下，实现了跨多种硬件的高效设备端 ML 推理。 基准测试显示，ArcFace R50 推理从 30ms（ONNX CPU）降至 3ms（ncnn Vulkan），SCRFD 从 25ms 降至 2.5ms；模型大小也从 174MB（ONNX fp32）减半至 87MB（ncnn fp16）。Vulkan 驱动程序已存在于大多数机器上，无需额外安装运行时。

reddit · r/MachineLearning · /u/ppchaos · 7月29日 10:22

**背景**: ncnn 是腾讯开发的高性能神经网络推理框架，专为移动和嵌入式设备优化，无第三方依赖。Vulkan 是一种跨平台 GPU API，提供对图形和计算硬件的底层访问。与 CUDA 等专有解决方案不同，这种组合实现了无需供应商锁定的 GPU 加速 ML 推理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/Tencent/ncnn">GitHub - Tencent/ncnn: ncnn is a high-performance neural network inference framework optimized for the mobile platform · GitHub</a></li>
<li><a href="https://onnxruntime.ai/">ONNX Runtime | Home</a></li>
<li><a href="https://pypi.org/project/ncnn/">ncnn · PyPI</a></li>

</ul>
</details>

**标签**: `#ML inference`, `#Vulkan`, `#ncnn`, `#edge computing`, `#cross-platform`

---

<a id="item-8"></a>
## [Hugging Face 平台被用于生成深度伪造裸照](https://www.theverge.com/ai-artificial-intelligence/971723/hugging-face-nudify-deepfake-undress-women-children) ⭐️ 8.0/10

AI Forensics 的一份报告发现，Hugging Face 的开源模型托管平台被广泛用于生成非自愿的深度伪造裸照，排名前九的图像编辑模型中有七个能通过简单提示轻易为女性“脱衣”。 这突显了 AI 领域重大的伦理和安全问题，Hugging Face 上的开源模型被滥用于生成非自愿的深度伪造色情内容，缺乏有效防护措施，对隐私和安全构成严重风险，尤其是对女性和儿童。 该报告设置了蜜罐空间，在 7 天内收到超过 1000 条请求，其中 73%涉及性内容，近 7%针对儿童。AI Forensics 建议 Hugging Face 增加提示词过滤和输出扫描机制以阻止有害图像生成。

telegram · zaihuapd · 7月29日 08:20

**背景**: Hugging Face 是一个流行的托管开源机器学习模型的平台，包括图像处理工具。深度伪造技术利用 AI 生成逼真的虚假图像或视频，常被滥用于非自愿的色情内容。蜜罐是一种安全机制，用于检测和分析未经授权的访问或滥用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Hugging_Face">Hugging Face</a></li>
<li><a href="https://en.wikipedia.org/wiki/Honeypot_%28computing%29">Honeypot (computing) - Wikipedia</a></li>

</ul>
</details>

**标签**: `#AI安全`, `#深度伪造`, `#Hugging Face`, `#AI伦理`, `#平台治理`

---

<a id="item-9"></a>
## [中国发布反网络暴力法草案，纳入 AI 网暴](https://mp.weixin.qq.com/s/PrzKFhbwjgFEGBPADvFD6Q) ⭐️ 8.0/10

2026 年 7 月 29 日，国家互联网信息办公室公布了《中华人民共和国反网络暴力法（征求意见稿）》，明确将利用 AI 技术制作、传播网暴信息的行为纳入规制。 这是一项重大的政策发展，直接针对 AI 生成的网络暴力，为平台和 AI 工具创作者设定了法律责任，并在中国的互联网治理中为 AI 监管树立了先例。 草案共七章六十条，要求平台建立监测识别和防护机制，并引入了人格权侵害禁令和精神损害赔偿。

telegram · zaihuapd · 7月29日 10:59

**背景**: 草案将网络暴力定义为集中或持续通过网络侵害他人名誉权、隐私权、肖像权、个人信息等合法权益的活动。人格权侵害禁令制度源于中国《民法典》，允许受害人在不必提起完整诉讼的情况下，请求法院发出禁止或限制侵权行为的命令，这对于互联网时代的损害预防尤为重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="http://www.js.xinhuanet.com/20230713/45eb9dff79b040a7a9c3aa17aeea0a88/c.html">江苏多地法院探索发出人格权侵害禁令_新华网江苏频道</a></li>
<li><a href="https://alk.12348.gov.cn/Detail?dbID=37&amp;sysID=16880">邹某人格权侵害禁令案以案释法</a></li>

</ul>
</details>

**标签**: `#AI regulation`, `#cyberbullying`, `#internet governance`, `#Chinese law`, `#AI ethics`

---
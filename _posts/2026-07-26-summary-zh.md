---
layout: default
title: "Horizon Summary: 2026-07-26 (ZH)"
date: 2026-07-26
lang: zh
---

> 从 28 条内容中筛选出 8 条重要资讯。

---

1. [vLLM v0.26.0 发布，新增 Inkling 模型系列和 DeepSeek-V4 优化](#item-1) ⭐️ 9.0/10
2. [SGLang v0.5.16：DSpark 推测解码与 Inkling 支持](#item-2) ⭐️ 9.0/10
3. [开放权重 AI 模型迎来 Kubernetes 时刻](#item-3) ⭐️ 8.0/10
4. [Android 可能限制设备本地 ADB](#item-4) ⭐️ 8.0/10
5. [义警破坏 Flock 监控摄像头](#item-5) ⭐️ 8.0/10
6. [Ruff v0.16.0 将默认规则从 59 条扩展至 413 条](#item-6) ⭐️ 8.0/10
7. [Opus 5：Anthropic 迄今为止最抗提示注入的模型](#item-7) ⭐️ 8.0/10
8. [AMD 挑战 CUDA 护城河](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [vLLM v0.26.0 发布，新增 Inkling 模型系列和 DeepSeek-V4 优化](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 9.0/10

vLLM v0.26.0 是一个重大版本发布，引入了 Inkling 多模态 MoE 模型系列、DeepSeek-V4 性能增强和灵活的注意力后端。该版本包含来自 212 位贡献者的 411 次提交。 这很重要，因为 vLLM 是一个广泛使用的 LLM 推理引擎，新特性增强了对前沿模型（如 Inkling、DeepSeek-V4）的支持，并为用户提高了灵活性和性能。 Inkling 是一个拥有 975B 总参数、41B 激活参数、256k 上下文的多模态 MoE 模型。该版本还包括 fp32 lm\_head 支持、KV 卸载的成熟化以及面向多模态输入的 Rust 前端增强。

github · khluu · 7月25日 10:38

**背景**: vLLM 是一个用于快速 LLM 推理和服务的开源库，支持多种模型架构和量化技术。该版本增加了对 ModelOpt NVFP4 量化、滑动窗口注意力作为显式后端能力的支持，以及类似 MTP（多令牌预测）的推测解码改进。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thinkingmachines.ai/news/introducing-inkling/">Inkling : Our Open-Weights Model - Thinking Machines Lab</a></li>
<li><a href="https://github.com/NVIDIA/Model-Optimizer">GitHub - NVIDIA/Model-Optimizer: A unified library of SOTA model optimization techniques like quantization, distillation, pruning, neural architecture search, speculative decoding, etc. It compresses deep learning models for downstream deployment frameworks like TensorRT-LLM, TensorRT, vLLM, etc. to optimize inference speed. · GitHub</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM inference`, `#release`, `#performance`, `#AI/ML`

---

<a id="item-2"></a>
## [SGLang v0.5.16：DSpark 推测解码与 Inkling 支持](https://github.com/sgl-project/sglang/releases/tag/v0.5.16) ⭐️ 9.0/10

SGLang v0.5.16 引入了 DSpark，一种基于置信度的推测解码算法，达到 383.7 tok/s，并新增了对 9750 亿参数的 Inkling MoE 模型的支持。 此版本大幅提升了 LLM 推理速度，并支持一个巨大的开放权重多模态模型，对研究和生产部署都有影响。DSpark 的自适应验证窗口可能成为推测解码的新标准。 DSpark 支持半自回归块草案生成，并根据草案置信度动态调整验证窗口，在 DeepSeek-V4-Pro 上达到 383.7 tok/s。Inkling 支持 100 万 token 的上下文，混合多种注意力类型，在 Blackwell 硬件上输入吞吐量高达 71.7k tok/s。

github · Qiaolin-Yu · 7月25日 00:13

**背景**: 推测解码通过使用小型草案模型生成候选 token，再由目标模型并行验证，从而降低延迟。混合专家（MoE）模型每个 token 仅激活部分参数，使得更大模型在可控计算量下运行。NVFP4 是 NVIDIA 的 4 位浮点格式，用于高效低精度推理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.emergentmind.com/topics/dspark">DSpark : Speculative Decoding</a></li>
<li><a href="https://thinkingmachines.ai/model-card/inkling/">Inkling Model Card - Thinking Machines Lab</a></li>
<li><a href="https://developer.nvidia.com/blog/introducing-nvfp4-for-efficient-and-accurate-low-precision-inference/">Introducing NVFP4 for Efficient and Accurate Low-Precision Inference | NVIDIA Technical Blog</a></li>

</ul>
</details>

**标签**: `#speculative decoding`, `#LLM inference`, `#DSpark`, `#Inkling`, `#SGLang`

---

<a id="item-3"></a>
## [开放权重 AI 模型迎来 Kubernetes 时刻](https://tobi.knaup.me/2026-07-25-open-weight-ai-is-having-its-kubernetes-moment/) ⭐️ 8.0/10

一篇文章认为，开放权重 AI 模型正成为行业标准，类似于 Kubernetes 如何彻底改变软件部署，成为创新和竞争的关键。 这一转变可能使 AI 开发民主化，减少对专有模型的依赖，并培育类似于开源软件的协作生态系统，对初创公司、研究人员和更广泛的 AI 行业产生影响。 文章直接类比 Kubernetes，后者最初是 Google 的开源项目，后来成为主导的容器编排平台。开放权重模型允许开发者检查和修改模型权重，实现定制化和社区贡献。

hackernews · tknaup · 7月25日 14:49 · [社区讨论](https://news.ycombinator.com/item?id=49048034)

**背景**: 开放权重 AI 模型是指公开训练后神经网络权重的模型，与仅提供 API 的封闭模型不同。这使得其他人可以运行、微调并在此基础上构建，类似于开源软件的工作原理。文章认为，这些模型正成为 AI 创新的关键，类似于 Kubernetes 成为云原生部署的必备工具。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/introducing-gpt-oss/">Introducing gpt-oss | OpenAI</a></li>
<li><a href="https://www.linkedin.com/pulse/openais-open-weight-model-what-means-developers-ai-industry-tsi9f">OpenAI’s Open - Weight Model : What It Means for Developers and the...</a></li>

</ul>
</details>

**社区讨论**: 评论者讨论禁止中国 AI 模型的可行性，有人指出权重只是数字，无法确定来源。其他人讨论专有模型价格的不稳定性，以及开放权重模型如何提供成本基准。还有人希望有更多类似 Linux 的协作开放模型，并对 OpenAI 发布的开放权重模型如 GPT-OSS 20B 表示赞赏。

**标签**: `#AI`, `#open-source`, `#kubernetes`, `#models`, `#industry-trends`

---

<a id="item-4"></a>
## [Android 可能限制设备本地 ADB](https://kitsumed.github.io/blog/posts/android-may-soon-restrict-on-device-adb/) ⭐️ 8.0/10

Google IssueTracker 上的一项功能请求允许开发者选择 ADBD 绑定的网络接口，但一位核心 ADB 维护者建议完全限制设备本地（loopback）ADB 连接，原因是存在 CVE-2026-0073 等安全漏洞。 这一变化可能破坏 Shizuku 等工具以及依赖设备本地 ADB 进行无线调试的开发工作流程。该讨论凸显了在增强安全性与维护 Android 生态系统中开发者自由度之间的张力。 设备本地 ADB 允许通过 localhost \(127.0.0.1\) 进行无线 ADB 连接，无需 USB，常被 Shizuku 等应用用于无需 root 获取系统级权限。提议的限制将阻断这种 loopback 访问，理由是利用 ADBD 套接字提升权限的恶意应用漏洞。

hackernews · shscs911 · 7月25日 06:57 · [社区讨论](https://news.ycombinator.com/item?id=49045159)

**背景**: ADB（Android 调试桥）是一个命令行工具，允许开发者与 Android 设备通信，进行调试、安装和 shell 访问。设备本地 ADB 指在设备本身上运行 ADB（例如通过终端模拟器）通过 localhost 连接到自身的 ADB 守护进程，不同于传统通过 USB 或电脑的无线 ADB。这一能力支持了 Shizuku 等强大工具，无需 root 即可授予高级权限。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://kitsumed.github.io/blog/posts/android-may-soon-restrict-on-device-adb/">Android May Soon Restrict On-Device ADB, Affecting Shizuku, libadb and Developers | Kitsumed Blog</a></li>
<li><a href="https://elsolitario.org/en/2026/07/25/google-restricts-local-adb-android-shizuku/">Local ADB on Android: Google Considers Restricting It</a></li>
<li><a href="https://www.developersdigest.tech/blog/android-restrict-on-device-adb-hn-analysis">Android May Soon Restrict On-Device ADB - What Developers Need to Know - Developers Digest</a></li>

</ul>
</details>

**社区讨论**: 社区评论褒贬不一：有人认为安全收益微乎其微，因为需要启用开发者选项和远程 ADB；而另一些人则认为这会导致更严格的限制。有用户指出，将 ADB 限制在特定接口（如 Tailscale）会是更好的解决方案，还有多人担心谷歌正在逐步限制对设备的本地控制。

**标签**: `#Android`, `#ADB`, `#security`, `#mobile development`, `#privacy`

---

<a id="item-5"></a>
## [义警破坏 Flock 监控摄像头](https://www.theguardian.com/us-news/ng-interactive/2026/jul/25/flock-surveillance-cameras) ⭐️ 8.0/10

《卫报》一篇文章报道了一场日益壮大的草根义警运动，人们通过物理方式遮挡或破坏 Flock 监控摄像头，例如用带纸板的泳池捞网遮住镜头，此举源于对隐私的担忧和对执法部门越权的不信任。 这场运动凸显了大规模监控技术与公民自由之间日益紧张的矛盾，可能影响围绕自动车牌识别（ALPR）系统的公共政策和企业实践。 Flock 摄像头采用 ALPR 技术，因车牌识别错误率高达 10%而受到批评，其 CEO 也承认曾积极向地方政府推销这些系统。

hackernews · bookofjoe · 7月25日 19:02 · [社区讨论](https://news.ycombinator.com/item?id=49050538)

**背景**: Flock Safety 公司生产自动车牌识别（ALPR）摄像头，执法机构用其捕获和存储车辆数据以进行监控。与交通摄像头不同，Flock 摄像头专门用于刑事调查，并引发了隐私倡导团体对未经授权大规模数据收集的担忧。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Flock_Safety">Flock Safety - Wikipedia</a></li>
<li><a href="https://www.dhs.gov/science-and-technology/saver/automatic-license-plate-readers">Automatic License Plate Readers | Homeland Security</a></li>
<li><a href="https://www.flocksafety.com/products/license-plate-readers">License Plate Readers (LPR) Cameras | Flock Safety</a></li>

</ul>
</details>

**社区讨论**: 评论者大多支持义警行为，有人报告一位老人用泳池捞网遮挡 Flock 摄像头。许多人表达了对政府和公司的不信任，引用本杰明·富兰克林关于自由与安全的格言，并认为当人们感到声音被忽视时，这种反弹是不可避免的。

**标签**: `#surveillance`, `#privacy`, `#civil liberties`, `#vigilante`, `#technology`

---

<a id="item-6"></a>
## [Ruff v0.16.0 将默认规则从 59 条扩展至 413 条](https://simonwillison.net/2026/Jul/25/ruff/#atom-everything) ⭐️ 8.0/10

7 月 23 日，Astral 发布了 Ruff v0.16.0，将默认规则数从 59 条增加到 413 条，无需任何配置即可捕获语法错误和运行时错误等严重问题。 此更新通过默认启用许多之前需手动开启的规则，大幅提升了 Python 代码质量标准，影响所有使用 Ruff 的项目，并可能破坏依赖未固定版本的 CI 流水线。 自 v0.1.0 以来，规则总数已从 708 条增至 968 条，新增默认规则包括 \`load-before-global-declaration\`、\`yield-in-init\` 等可防止即时运行时错误的检查。

rss · Simon Willison · 7月25日 22:44

**背景**: Ruff 是一个用 Rust 编写的极速 Python 代码检查器和格式化工具，旨在替代 Flake8、isort 和 Black 等多种工具。它集成了来自 50 多个现有工具的 900 多条检查规则，运行速度比传统检查器快 10-100 倍。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/astral-sh/ruff">GitHub - astral-sh/ruff: An extremely fast Python linter and code formatter, written in Rust. · GitHub</a></li>
<li><a href="https://realpython.com/ruff-python/">Ruff: A Modern Python Linter for Error-Free and Maintainable Code – Real Python</a></li>

</ul>
</details>

**标签**: `#Python`, `#linting`, `#Ruff`, `#static analysis`, `#tooling`

---

<a id="item-7"></a>
## [Opus 5：Anthropic 迄今为止最抗提示注入的模型](https://simonwillison.net/2026/Jul/25/boris-cherny/#atom-everything) ⭐️ 8.0/10

Boris Cherny 宣布，根据模型系统卡中详述的内部评估和红队测试结果，Anthropic 的 Opus 5 模型是迄今为止最不易被提示注入的模型。 提示注入是大语言模型面临的关键安全威胁，因此更强的抗性使 Opus 5 在实际应用中更加安全，尤其适用于需要高可靠性和可信度的场景。 该声明基于 Opus 5 系统卡第 73 页报告的评估和红队测试结果。Opus 5 是 Anthropic 旗下 Claude 系列中的顶级模型，接替了 Opus 4。

rss · Simon Willison · 7月25日 00:42

**背景**: 提示注入是一种攻击方式，通过在模型输入中插入恶意指令来覆盖其预期行为。Anthropic 发布系统卡来记录每个模型的安全评估和能力。Opus 5 是 Claude 系列中的最新旗舰模型，专为复杂任务和长时间运行的代理设计。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/news/claude-opus-5">Introducing Claude Opus 5 \ Anthropic</a></li>
<li><a href="https://en.wikipedia.org/wiki/Claude_Opus">Claude Opus</a></li>

</ul>
</details>

**标签**: `#prompt-injection`, `#anthropic`, `#claude`, `#generative-ai`, `#ai`

---

<a id="item-8"></a>
## [AMD 挑战 CUDA 护城河](https://newsletter.semianalysis.com/p/can-amd-break-the-cuda-moat-amd-advancing) ⭐️ 8.0/10

AMD 正在部署代理内核生成、改进软件质量，并加速生产 Helios MI455X 机架级系统，以挑战 NVIDIA 的 CUDA 主导地位，尽管面临内部开发集群不稳定和激进的财务折扣。 如果 AMD 成功，它可能打破 NVIDIA 的 CUDA 锁定，降低 AI GPU 成本，并增加 AI 硬件和软件生态系统的竞争，直接影响数据中心运营商和 AI 开发者。 Helios 机架配备了 72 个 MI455X GPU，拥有 31 TB 的 HBM4 内存和 2.9 FP4 exaFLOPS 算力，但生产爬坡过程极其困难（“生产爬坡地狱”），且 AMD 通过财务工程提供高达 105%的折扣来激励采用。

rss · Semianalysis · 7月25日 00:33

**背景**: NVIDIA 的 CUDA 平台构建了强大的生态系统护城河，使得 AMD 的 ROCm 等替代方案因软件兼容性和性能优化问题难以获得广泛采用。代理内核生成利用自主 LLM 自动生成和优化底层 GPU 内核，有望减少将 CUDA 代码移植到 AMD 硬件所需的手动工作。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.emergentmind.com/topics/agentic-kernel-generation">Agentic Kernel Generation</a></li>
<li><a href="https://www.spheron.network/blog/amd-helios-rack-scale-mi455x-gpu-cloud/">AMD Helios Rack-Scale AI on GPU Cloud: Deploy MI 455 X Inference...</a></li>
<li><a href="https://logicity.in/en/blog/amd-unveils-helios-rack-mi455x-gpu-to-challenge-nvidia">AMD unveils Helios rack, MI 455 X GPU to challenge Nvidia | Logicity</a></li>

</ul>
</details>

**标签**: `#AI`, `#AMD`, `#CUDA`, `#GPU`, `#Software Engineering`

---
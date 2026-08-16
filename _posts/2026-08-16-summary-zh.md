---
layout: default
title: "Horizon Summary: 2026-08-16 (ZH)"
date: 2026-08-16
lang: zh
---

> 从 31 条内容中筛选出 4 条重要资讯。

---

1. [Anthropic 公开 Claude 系统提示词，引发社区分析](#item-1) ⭐️ 8.0/10
2. [Qwen 3.8 27B 表现出色，但默认会过度思考](#item-2) ⭐️ 8.0/10
3. [调查：PJM 建模错误浪费 120 亿美元，重蹈覆辙风险高](#item-3) ⭐️ 8.0/10
4. [Anthropic 第二季营收暴涨 14 倍超 115 亿美元，筹备 IPO](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Anthropic 公开 Claude 系统提示词，引发社区分析](https://platform.claude.com/docs/en/release-notes/system-prompts) ⭐️ 8.0/10

Anthropic 在其平台发布说明中公开了 Claude 模型所使用的系统提示词。这份文档揭示了塑造 Claude 行为的具体指令，其中包括一条让 Claude 自行检查图片是否真实存在的提示词。 这是业界常被批评为不透明时的一次重大透明度举措，让开发者和研究人员罕见地看到前沿 AI 模型是如何被指令塑造的。公开这些内容使得外部审计、解读以及随时间追踪变化成为可能。 这些系统提示词发布在 Anthropic 的平台文档中，Claude 的网页界面和移动应用会在每次对话开始时使用它们来提供当前日期等最新信息。开发者已经构建了可对比的 git 历史记录，而差异（diff）中出现了“Claude Fable 5”和“Claude Mythos 5”等新引用。

hackernews · tosh · 8月16日 12:48 · [社区讨论](https://news.ycombinator.com/item?id=49319556)

**背景**: 系统提示词是给大语言模型的一套基础指令，定义了它在某次交互中的角色、行为、语气、约束和能力。与每次都会变化的用户提示不同，系统提示词在幕后保持相对固定，引导整个对话。对于 Claude 而言，系统提示词还会携带当前日期等最新上下文，而 Anthropic 历来对这类提示词保密。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://platform.claude.com/docs/en/release-notes/system-prompts">System Prompts - Claude Platform Docs - Anthropic</a></li>
<li><a href="https://www.promptlayer.com/glossary/system-prompt/">What is a System prompt? | PromptLayer</a></li>
<li><a href="https://likeone.ai/blog/claude-system-prompt-guide/">Claude System Prompt Guide 2026 | Like One</a></li>

</ul>
</details>

**社区讨论**: 评论者大多对公开表示欢迎，Simon Willison 创建了提示词的 git 提交历史以方便追踪变化。一些人由此对模型智能的本质表达了哲学上的疑虑，还有人担心审核偏差，指出论坛上批评 AI 的帖子疑似消失。还有评论者注意到一条危机优先指令，它要求 Claude 在用户处于困境时优先考虑其福祉而非完成任务。

**标签**: `#AI`, `#Claude`, `#System Prompts`, `#Anthropic`, `#LLM`

---

<a id="item-2"></a>
## [Qwen 3.8 27B 表现出色，但默认会过度思考](https://simonwillison.net/2026/Aug/16/qwen-38-27b/) ⭐️ 8.0/10

阿里巴巴 Qwen 实验室发布了采用 Apache 2.0 许可证的 27B 参数视觉语言模型 Qwen 3.8 27B。其自报基准显示该模型超越了前代 Qwen 3.6 27B 和闭源模型 Qwen 3.7-Plus，但默认的 xhigh 推理强度会导致严重的过度思考，例如生成一张 SVG 图耗时 21 分钟。 一个开放权重的 27B 模型就能达到或超过更大的闭源模型，这对本地部署和成本敏感的 AI 使用场景意义重大。它让开发者和研究人员可以在消费级硬件上运行强大的视觉语言模型，减少对昂贵闭源 API 的依赖。 默认的 xhigh 推理强度会迅速耗尽 LM Studio 默认的 8,192 token 上下文窗口，加载完整 262,144 token 上下文后才能正常工作。在 17GB 的 Q4\_K\_M 量化版上，生成一张图像消耗了 22,276 个推理 token 和 3,223 个输出 token。

rss · Simon Willison · 8月16日 22:00

**背景**: Apache 2.0 是一种宽松的开源许可证，允许用户自由使用、修改和分发软件，包括商用用途。Qwen 是阿里巴巴的研究团队，持续发布不同规模的开放权重模型，而 27B 参数规模很适合在笔记本电脑上运行。该模型支持 reasoning\_effort 参数，用户可以选择不同的思考深度以权衡质量与速度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Apache_License">Apache License</a></li>
<li><a href="https://openrouter.ai/qwen/qwen3.6-27b">Qwen3.6 27B - API Pricing &amp; Benchmarks | OpenRouter</a></li>

</ul>
</details>

**标签**: `#LLM`, `#Qwen`, `#open-source`, `#AI`, `#model release`

---

<a id="item-3"></a>
## [调查：PJM 建模错误浪费 120 亿美元，重蹈覆辙风险高](https://newsletter.semianalysis.com/p/12b-of-us-ratepayers-money-wasted) ⭐️ 8.0/10

SemiAnalysis 发布调查指出，PJM 容量市场中的一个建模错误浪费了美国纳税人约 120 亿美元。报告警告称，PJM 正准备再次采用同样有缺陷的建模方法，使未来成本面临风险。 这一事件意义重大，因为此类建模错误直接决定电网可靠性成本，并可能扭曲发电投资。若 PJM 重蹈覆辙，可能进一步推高电价，并削弱美国各界对容量市场设计的信心。 调查聚焦于 PJM 市场中用于容量认证的有效负载能力（ELCC）方法，该方法决定发电资源可获得多少容量电费。虽然技术细节较为复杂，但核心问题在于不准确的建模高估了资源贡献，导致超额成本转嫁给用电者。

rss · Semianalysis · 8月16日 22:27

**背景**: PJM 互联是一家区域输电组织（RTO），负责协调美国多个州的电网运行，并运营着全球最大的批发电市场之一。在容量市场中，发电商并非按实际发电量获得报酬，而是因其承诺在将来用电需求高峰时可用而获得付款。有效负载能力（ELCC）是一种用于衡量发电资源相对“完美电源”可靠性贡献的方法，常用于太阳能、风能和储能等间歇性资源的容量价值评估。因此，ELCC 及其他模型输入的错误应用或校准失误，可能给电力消费者带来巨大的财务后果。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/PJM_Interconnection">PJM Interconnection - Wikipedia</a></li>
<li><a href="https://www.ferc.gov/understanding-wholesale-capacity-markets">Understanding Wholesale Capacity Markets | Federal Energy ...</a></li>
<li><a href="https://www.mass.gov/doc/understanding-capacity-accreditation-webinar-presentation/download">Capacity Accreditation and ELCC Primer</a></li>

</ul>
</details>

**标签**: `#energy grid`, `#modeling`, `#PJM`, `#economics`, `#infrastructure`

---

<a id="item-4"></a>
## [Anthropic 第二季营收暴涨 14 倍超 115 亿美元，筹备 IPO](https://www.cnbc.com/2026/08/15/anthropic-revenue-jumps-to-over-11point5-billion-in-q2-report.html) ⭐️ 8.0/10

Anthropic 公布的初步第二季营收超过 115 亿美元，同比增长逾 14 倍，高于 2026 年第一季的 47.3 亿美元。当季调整后营业利润转正，公司正筹备可能在今秋启动的大型 IPO。 这一爆发式增长表明，头部 AI 实验室有能力迅速将需求转化为营收；若启动 IPO，可能成为今年最大的科技股发行之一。这也反映出 AI 行业整体的强劲势头和日趋激烈的竞争。 据彭博社引述的文件，这些数字为初步数据，仍可能调整。Anthropic 第二季营收相较于去年同期的 7.87 亿美元及 2026 年第一季的 47.3 亿美元，且当季调整后营业利润转正。

telegram · zaihuapd · 8月16日 07:26

**背景**: Anthropic 是一家领先的人工智能公司，专注于开发大语言模型和 AI 助手。初步营收是未经审计的早期估算数字，调整后营业利润则剔除一次性或非现金项目，以反映核心盈利能力。营收同比猛增 14 倍通常意味着去年同期基数较低或产品被极快采纳。潜在的 IPO 将使公众投资者有机会参与该公司的增长。

**标签**: `#Anthropic`, `#AI`, `#Revenue`, `#IPO`, `#Business`

---
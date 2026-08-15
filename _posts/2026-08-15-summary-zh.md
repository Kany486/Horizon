---
layout: default
title: "Horizon Summary: 2026-08-15 (ZH)"
date: 2026-08-15
lang: zh
---

> 从 24 条内容中筛选出 3 条重要资讯。

---

1. [AI 工作记忆远超人类，但依然无法胜过数学家](#item-1) ⭐️ 8.0/10
2. [用 Codex 自动研究实现 232 倍内核加速](#item-2) ⭐️ 8.0/10
3. [BDH-CQ：用循环隐式推理以极低成本刷新 ARC-AGI-1 成绩](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [AI 工作记忆远超人类，但依然无法胜过数学家](https://davidepiffer.com/p/ai-isnt-outthinking-mathematicians) ⭐️ 8.0/10

戴维德·皮费尔（Davide Piffer）的文章指出，尽管 AI（尤其是大语言模型）拥有远超人类大脑的工作记忆容量，但由于缺乏定性推理和常识，它仍无法在思考上胜过数学家。 这一论点挑战了“记忆容量越大就越聪明”的假设，有助于研究人员重新审视 AI 的优势与局限。它还对软件工程提出实际问题：可维护的代码往往是围绕人类工作记忆的局限来设计的。 文章认为，AI 的巨大上下文窗口是一种优势，但并不足以弥补其推理质量的欠缺。社区评论者将此与代码可维护性联系起来，并指出 LLM 生成的代码往往更冗长，长期维护时可能产生问题。

hackernews · rzk · 8月15日 18:13 · [社区讨论](https://news.ycombinator.com/item?id=49312845)

**背景**: 工作记忆是人类用于临时保存和处理信息的有限认知容量，通常被认为只能同时处理大约 7 个项目。AI 系统尤其是 LLM 可以处理非常大的上下文窗口，从而拥有远超人类的工作记忆式存储能力。然而，定性推理——即在信息不完整的情况下对空间、时间、数量等进行推理的能力——仍然是 AI 系统的已知短板。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.illumio.com/blog/the-limits-of-working-memory-human-brains-vs-ai-models">The Limits of Working Memory: Human Brains vs. AI Models</a></li>
<li><a href="https://arxiv.org/html/2504.15965v2">From Human Memory to AI Memory: A Survey on Memory Mechanisms ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Qualitative_reasoning">Qualitative reasoning - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论大多同意“智能不仅取决于记忆”：有用户认为所谓高智力往往只是比别人记得更多，也有人主张真正有用的是把知识压缩成相互关联的模式，而非单纯扩大容量。还有讨论提到 AI 可以发布和复用“负面结果”，而人类数学家很少这样做；同时大家对未来代码的可维护性表示担忧。

**标签**: `#AI`, `#working memory`, `#human cognition`, `#LLMs`, `#software engineering`

---

<a id="item-2"></a>
## [用 Codex 自动研究实现 232 倍内核加速](https://sankalp.bearblog.dev/autoresearch/) ⭐️ 8.0/10

作者使用 OpenAI Codex 自动执行“基准测试-剖析-验证-研究-优化”循环，对一个内核进行优化，最终实现了 232 倍的加速。这展示了 AI 在底层 GPU 代码上驱动的性能工程能力。 这一结果表明，AI 智能体能够完成复杂的性能工程，可能改变开发者进行底层优化的方式。同时，它也引发了重要讨论：这类 AI 生成的优化能否推广到特定基准或输入形状之外。 232 倍的加速来自一个自动循环，该循环反复对内核进行基准测试、剖析、验证、研究和改进。社区评论者指出，类似的 AI 优化竞赛方案经常在分布外输入上失效，因此鲁棒性仍然是一个重要问题。

hackernews · tosh · 8月15日 11:00 · [社区讨论](https://news.ycombinator.com/item?id=49309549)

**背景**: CUDA kernel 是在 GPU 上运行的函数，由组织成 block 和 grid 的成千上万个线程并行执行。OpenAI Codex 是一种 AI 编程智能体，可以将自然语言转换成可工作的代码，并自动完成拉取请求、重构和代码审查等任务。深度学习工作负载高度依赖 GPU kernel，因此它们成为 AI 辅助优化的自然目标。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/codex/">Codex in ChatGPT | AI Coding Agents for Software... | OpenAI</a></li>
<li><a href="https://llm-stats.com/blog/research/what-is-a-cuda-kernel">What Is a CUDA Kernel ? A Visual Explainer | LLM Stats</a></li>

</ul>
</details>

**社区讨论**: 评论区有人分享了类似实验：有人用 DeepSeek 优化带验证器的视频编解码器；还有人指出，10 个顶级竞赛方案中有 8 个由 AI 优化，但都在分布外的形状上失效。有读者称赞这篇长文是人工写成的，读起来很清新；还有人猜测为什么 GPU kernel 在模型训练数据中如此丰富。

**标签**: `#AI-assisted development`, `#kernel optimization`, `#CUDA`, `#performance engineering`, `#deep learning`

---

<a id="item-3"></a>
## [BDH-CQ：用循环隐式推理以极低成本刷新 ARC-AGI-1 成绩](https://www.reddit.com/r/MachineLearning/comments/1vov5r5/bdhcq_incontext_learning_with_recurrent_latent/) ⭐️ 8.0/10

Pathway 的研究者推出了 BDH-CQ，这是一个 150M 参数的推理模型，将上下文学习与循环隐式推理结合在一起。它在 ARC-AGI-1 上取得 29.5% 的 pass@2 成绩，每个任务估计成本仅 0.00070 美元，据称打破了此前报告的成本-精度帕累托前沿。 这件事意义重大，因为它表明小型模型可以通过架构创新而非单纯扩大规模来超越更大、更昂贵的系统。它还挑战了“强推理能力必须依赖显式思维链 token 生成”的假设。 该模型不会将中间推理步骤解码为语言，而是在高维隐空间中迭代计算。训练时不使用任务标识符或评估任务的演示样本，推理时不更新任何参数，并且该架构继承了 BDH 的张量分片模式，可自然扩展到很大规模。

reddit · r/MachineLearning · /u/moschles · 8月15日 06:18

**背景**: ARC-AGI-1 是一个旨在衡量技能获取能力的基准测试，关注智能的核心而非在预定义任务上的表现。BDH-CQ 建立在 Dragon Hatchling（BDH）这一后 Transformer 循环架构之上，该架构中类神经元单元通过低秩交互进行通信，并在不断演化的联想状态中维持上下文。BDH-CQ 在此基础上扩展了上下文学习：推理时演示样本会更新循环记忆，随后通过迭代式连续计算来求解查询。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://pathway.com/blog/pathway-150m-model-breaks-arc-agi-1-cost-efficiency-frontier">Pathway’s 150M-Parameter Model Breaks the...</a></li>
<li><a href="https://arxiv.org/html/2608.09888">BDH - CQ : In-Context Learning with Recurrent Latent Reasoning</a></li>
<li><a href="https://arcprize.org/arc-agi/1">ARC-AGI-1</a></li>

</ul>
</details>

**标签**: `#in-context learning`, `#recurrent memory`, `#latent reasoning`, `#ARC-AGI`, `#efficient ML`

---
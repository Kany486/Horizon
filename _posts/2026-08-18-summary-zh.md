---
layout: default
title: "Horizon Summary: 2026-08-18 (ZH)"
date: 2026-08-18
lang: zh
---

> 从 31 条内容中筛选出 4 条重要资讯。

---

1. [Mojo🔥 以 Apache 2.0 许可证正式开源](#item-1) ⭐️ 9.0/10
2. [用 20 美元工具修复变砖的 Framework 笔记本](#item-2) ⭐️ 8.0/10
3. [Linux 7.3 提升显存超卖下的性能表现](#item-3) ⭐️ 8.0/10
4. [Qwen 3.8 27B 在 AI 指数上得分 52，追平 GPT-5.6 Luna](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Mojo🔥 以 Apache 2.0 许可证正式开源](https://simonwillison.net/2026/Aug/18/mojo-is-now-open-source/) ⭐️ 9.0/10

2026 年 8 月 18 日，Modular 以 Apache 2.0 许可证开源了 Mojo 编译器与工具链，距其发布 Mojo 1.0 仅一周。这兑现了该语言在 2023 年 5 月首次发布时做出的开源承诺。 Mojo 开源是一个重要里程碑，兑现了多年的承诺，并为 AI、ML 和高性能计算领域的更广泛社区采用打开了大门。Mojo 的类 Python 语法以及对 GPU 和其他加速器的支持，使其对希望突破 Python 性能限制的开发者具有吸引力。 最初将 Mojo 打造为 Python 全超集的目标已在 2025 年 8 月左右被放弃，如今该语言定位为面向 GPU 编程优化的独立语言。Mojo 基于 MLIR 编译器框架构建，可面向 CPU、GPU、TPU、ASIC 及其他加速器编译，目前开源版本支持 Linux 和 macOS。

rss · Simon Willison · 8月18日 21:39

**背景**: Mojo 是 Modular 公司开发的一种系统编程语言，它结合了类 Python 语法与受 Rust 启发的语义，如静态类型和借用检查器。Mojo 没有直接基于 LLVM，而是使用了 MLIR 编译器框架，从而实现更高级的优化并支持多种硬件目标。据 fast.ai 的 Jeremy Howard 所说，Mojo 可被视为“MLIR 的语法糖”，非常适合 AI 和高性能计算工作负载。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mojo_%28programming_language%29">Mojo (programming language)</a></li>
<li><a href="https://mojolang.org/">Mojo - Modular</a></li>

</ul>
</details>

**标签**: `#mojo`, `#open-source`, `#programming-language`, `#high-performance-computing`, `#python`

---

<a id="item-2"></a>
## [用 20 美元工具修复变砖的 Framework 笔记本](https://quantum5.ca/2026/08/16/fixing-bricked-amd-7040-series-framework-13-laptop-with-20-tools/) ⭐️ 8.0/10

一篇详细指南介绍了如何使用约 20 美元的工具（包括 CH341A SPI 编程器和 SOIC-8 测试夹）修复变砖的 Framework Laptop 13（AMD 7040 系列）。该文章吸引了 225 条评论，并引发了关于固件更新缺陷和消费者权利的广泛讨论。 这件事意义重大，因为固件损坏可能让一台完好的笔记本电脑变成电子垃圾，而这篇指南提供了一条官方支持之外的低成本维修途径。它也凸显了在缺陷更新造成损失时，制造商与消费者之间关于责任归属的紧张关系。 恢复过程使用了可模拟 SPI 等多种协议的 CH341A USB 编程器，并配合一个无需焊接即可夹住闪存芯片的 SOIC-8 测试夹。文章专门针对 AMD 7040 系列 Framework Laptop 13，描述了一次失败或有缺陷的固件更新导致设备变砖的情况。

hackernews · jp\_sc · 8月18日 13:18 · [社区讨论](https://news.ycombinator.com/item?id=49345220)

**背景**: 所谓‘变砖’的笔记本电脑无法启动，通常是因为其固件（BIOS/UEFI）损坏。CH341A 是一种廉价的 USB 接口芯片，能够模拟 UART、I2C、SPI 和 JTAG 等协议，因此常用于对 SPI 闪存芯片进行编程。SOIC-8 测试夹可以无需拆焊即可连接芯片。Framework 笔记本以可修复性为设计理念，但用户仍会遇到固件更新问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.onetransistor.eu/2018/11/use-ch341a-with-asprogrammer-on-windows.html">AsProgrammer and other Windows utilities for CH 341 A · One Transistor</a></li>
<li><a href="https://www.amazon.com/KeeYees-SOIC8-EEPROM-CH341A-Programmer/dp/B07SHSL9X9">Amazon.com: KeeYees SOP8 SOIC8 Test Clip and CH341A USB ... IC Test Clip - SOIC 8-Pin - SparkFun Electronics SOIC Clip, 8 Pin - Pomona Electronics SOIC 8-Pin Test Clip to DIP Adapter - Adafruit Industries 5250 Pomona Electronics | IC Clips | DigiKey Soic8 Clip - eBay</a></li>
<li><a href="https://technewst.com/the-framework-laptop-has-a-firmware-update-problem-but-maybe-not-for-long/">Framework Laptop Update Woes (But Hope Remains) | TechNewst</a></li>

</ul>
</details>

**社区讨论**: 评论者提出了法律层面的疑问：官方固件导致设备变砖时，制造商是否应承担法律责任，还有人建议诉诸小额索赔法庭。其他人分享了在其他笔记本上遇到的类似经历，并对糟糕的 BIOS 更新仍会毁掉正常工作的硬件表示不满。一些用户对购买 Framework 感到后悔，因为其更换部件是专有的，价格昂贵且经常缺货。

**标签**: `#Framework Laptop`, `#Firmware Recovery`, `#Right to Repair`, `#Hardware Repair`, `#Consumer Rights`

---

<a id="item-3"></a>
## [Linux 7.3 提升显存超卖下的性能表现](https://pixelcluster.dev/VRAM-Overcommit/) ⭐️ 8.0/10

Linux 7.3 引入了改进的显存超卖处理机制，在 GPU 显存耗尽时能提升性能。这一改动引发了社区广泛关注，获得 8/10 评分、494 个点赞和 259 条评论。 显存耗尽是游戏玩家和 AI/ML 工作负载常见的性能瓶颈，因此更好的超卖性能可以减少卡顿和内存不足错误。这表明 Linux 内核继续增加面向游戏和性能的功能，从而与其他平台形成差异化。 该改进聚焦于 GPU 专用显存耗尽时内核如何处理内存，但具体实现细节尚未合入上游。评论者指出，Nvidia GPU 目前缺少相应的分页支持，虚拟内存碎片化也仍然是一个待解决的问题。

hackernews · flaburgan · 8月18日 07:51 · [社区讨论](https://news.ycombinator.com/item?id=49342719)

**背景**: 显存超卖（VRAM overcommit）是指应用程序请求的总内存超过 GPU 上可用的物理显存，系统被迫将数据换出到系统内存或磁盘。高效的超卖机制可以让更多工作负载共享有限的显存，同时尽量减少性能损失。Linux 内核近期还加入了其他性能改进，例如 large folios、缓存感知调度和改进的 MGLRU 回收，这些与本次工作相辅相成。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://pixelcluster.dev/VRAM-Overcommit/">VRAM Management Part 2: Beyond the Limits... | pixelcluster&#x27;s GPU blog</a></li>
<li><a href="https://cubepath.com/docs/virtualization-vps/memory-overcommit-in-virtualization">Memory Overcommit in Virtualization: Complete Guide... | CubePath</a></li>
<li><a href="https://webhosting.de/en/memory-overcommitment-virtualization-ram-optimus/">Memory overcommitment in virtualization environments... - webhosting</a></li>

</ul>
</details>

**社区讨论**: 讨论总体非常热烈，用户赞赏开发者的热情并期待该功能合入上游。一些 Nvidia 用户对缺少分页支持表示不满，还有评论者询问内核是否也应该就地整理虚拟内存。其他人则对比了 Linux 用户热切期待内核版本发布与 Windows 用户反感更新的现象。

**标签**: `#linux`, `#kernel`, `#vram`, `#performance`, `#gpu`

---

<a id="item-4"></a>
## [Qwen 3.8 27B 在 AI 指数上得分 52，追平 GPT-5.6 Luna](https://simonwillison.net/2026/Aug/17/qwen-38-27b-scores-52/) ⭐️ 8.0/10

根据 Simon Willison 在 2026 年 8 月 17 日的报道，Qwen 3.8 27B 这款 270 亿参数的小型模型在 Artificial Analysis Intelligence Index 上获得 52 分，与 GPT-5.6 Luna 持平，仅比 GLM-5.2 和 DeepSeek V4 Pro 低 1 分。 这一结果表明，一款紧凑的 27B 模型能够匹敌参数规模大得多的系统，有望降低部署成本，让高端 AI 能力更容易获得。它也说明，注重效率的研究和小型模型正变得对前沿大模型越来越有竞争力。 该分数使 Qwen 3.8 27B 与 GPT-5.6 Luna 持平，仅比 GLM-5.2（753B）和 DeepSeek V4 Pro 0813（1.7T）低 1 分。该模型是基于 Qwen3.5 架构的稠密视觉语言模型，托管版本将默认提供 100 万 token 的上下文长度。

rss · Simon Willison · 8月17日 23:58

**背景**: Artificial Analysis Intelligence Index（人工分析智能指数）是 Artificial Analysis 发布的综合基准分数，用于衡量模型在推理、编程、知识、指令遵循、科学推理和多步任务等方面的能力。DeepSeek V4 Pro 等大模型拥有 1.7 万亿参数，而 Qwen 3.8 27B 只有 270 亿参数，却能取得相近分数，体现了显著的效率优势。Qwen 3.8 是阿里巴巴的开源权重模型系列，27B 版本是基于 Qwen3.5 架构的稠密视觉语言模型，适合通用文本生成和智能体任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://artificialanalysis.ai/evaluations/artificial-analysis-intelligence-index">Artificial Analysis Intelligence Index</a></li>
<li><a href="https://huggingface.co/Qwen/Qwen3.8-27B">Qwen/Qwen3.8-27B · Hugging Face</a></li>

</ul>
</details>

**标签**: `#AI`, `#LLMs`, `#Qwen`, `#small models`, `#artificial analysis`

---
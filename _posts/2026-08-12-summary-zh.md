---
layout: default
title: "Horizon Summary: 2026-08-12 (ZH)"
date: 2026-08-12
lang: zh
---

> 从 36 条内容中筛选出 11 条重要资讯。

---

1. [Qwen 发布 Qwen3.8-2.4T-A95B：大规模开源 MoE 模型](#item-1) ⭐️ 9.0/10
2. [DeepSeek 发布 V4 Pro 0813，低价高性能获社区好评](#item-2) ⭐️ 8.0/10
3. [Tailscale 将数据库损坏追溯到 16 年前的 SQLite WAL 重置 Bug](#item-3) ⭐️ 8.0/10
4. [xAI 发布 Grok 4.6，引发系统提示词与基准测试讨论](#item-4) ⭐️ 8.0/10
5. [为什么 Chrome 中小 JPEG 图像显示效果不同](#item-5) ⭐️ 8.0/10
6. [uBlock Origin 停止拦截 Facebook 广告，承认反广告拦截措施](#item-6) ⭐️ 8.0/10
7. [AI 正在让软件工程的中层岗位消失？](#item-7) ⭐️ 8.0/10
8. [工程师警告：AI 辅助编码导致系统难以维护](#item-8) ⭐️ 8.0/10
9. [Adam 的逐坐标更新破坏旋转不变性，导致低秩隐式偏置消失](#item-9) ⭐️ 8.0/10
10. [LTX 发布开源视频模型 LTX-2.5，可在单张 RTX 5090 上运行](#item-10) ⭐️ 8.0/10
11. [微信发布 WeLM：以资源效率为核心的大语言模型家族](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Qwen 发布 Qwen3.8-2.4T-A95B：大规模开源 MoE 模型](https://huggingface.co/Qwen/Qwen3.8-2.4T-A95B) ⭐️ 9.0/10

Qwen 发布了 Qwen3.8-2.4T-A95B，这是一个总参数 2.4 万亿、激活参数 950 亿的开源 MoE 模型，原生上下文长度 262,144 tokens，可扩展至 1,010,000 tokens。模型在 Hugging Face 上提供 BF16 和 FP8 检查点，宣称性能可与 Kimi k3 等模型竞争。 这是开源 AI 生态的一次重大发布，使得前沿规模的模型可用于微调和自托管。其庞大的总参数量以及随之而来的量化和推理服务权衡，很可能推动模型压缩和高效推理方面的进展。 该模型总参数 2.4T，每个 token 激活 95B 参数，但初始仅发布 BF16 和 FP8 版本，没有基于 QAT 的 4 位量化版本；Unsloth 报告有约 397GB 的 1 位量化版本。开源权重版本缺少官方 Qwen3.8-Max 的一些功能，如图像输入和默认 1M 上下文，其许可证允许内部使用或年收入低于 5000 万美元时免费使用，超过该门槛则有限制。

hackernews · Philpax · 8月12日 15:01 · [社区讨论](https://news.ycombinator.com/item?id=49273478)

**背景**: 混合专家（MoE）是一种机器学习架构，将模型划分为多个专门的子网络，并只对每个输入激活其中少数专家，从而可以在总参数达到万亿级的同时，每个 token 的计算量不会同比例增加。量化技术将模型权重压缩为 FP8 或 4-bit 等更低精度格式，从而减少内存占用并提升推理速度，vLLM 等框架已支持这一技术。服务万亿参数的 MoE 模型会占用大量内存，尤其随着上下文长度增长，KV 缓存也在膨胀，因此量化和高效批处理对实际部署至关重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://www.baseten.co/blog/33-faster-llm-inference-with-fp8-quantization/">33% faster LLM inference with FP8 quantization</a></li>
<li><a href="https://developer.nvidia.com/blog/mastering-llm-techniques-inference-optimization/">Mastering LLM Techniques: Inference Optimization | NVIDIA Technical Blog</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论主要围绕运行和量化该模型的实际困难，有评论指出只有 BF16/FP8 版本使其比 Kimi k3 等竞品更难部署，高质量 4 位量化需要大量算力和校准数据。也有人对 Unsloth 的 1 位量化版本感到兴奋，认为它能把 Opus 级别的性能带到普通硬件上；还有一些人遗憾开源权重版本缺少视觉输入和完整 1M 上下文等功能。此外，有评论调侃在 Intel N100 等低端设备上运行这样的大模型不切实际。

**标签**: `#AI`, `#LLM`, `#Qwen`, `#model release`, `#open source`

---

<a id="item-2"></a>
## [DeepSeek 发布 V4 Pro 0813，低价高性能获社区好评](https://openrouter.ai/deepseek/deepseek-v4-pro-0813) ⭐️ 8.0/10

DeepSeek 已发布旗舰模型 DeepSeek V4 Pro 0813 的生产版，结束了近四个月的预览期。OpenRouter 上的社区测试显示，该模型以远低于 Grok 4.6 等竞品的成本，在代码开发任务中表现出色。 此次发布可能加剧 AI 模型市场的价格竞争，因为 DeepSeek 继续以极低成本提供前沿性能。运行大量任务的开发者可望找到一个比昂贵的西方模型更有吸引力的替代方案，从而加速低成本 AI API 的普及。 该版本的代号为 V4 Pro 0813，于 2026 年 8 月 12 日作为正式版发布，结束了近四个月的预览期。在一项 Codex CLI 对比测试中，DeepSeek V4 Pro 运行 12 分 02 秒、花费 0.12 美元但存在 bug，而 Grok 4.6 运行 3 分 18 秒、花费 1.41 美元且没有 bug。

hackernews · explosion-s · 8月12日 16:04 · [社区讨论](https://news.ycombinator.com/item?id=49274600)

**背景**: DeepSeek 是一家中国 AI 公司，其聊天机器人和开放权重模型在 2025 年 1 月发布 DeepSeek-R1 后引发全球关注，曾短暂超越 ChatGPT 成为美国 iOS App Store 下载量最大的免费应用。该公司以节能训练和开源贡献著称，并定位为高性能 AI 的低成本提供商。V4 Pro 模型在本次正式版发布前已预览约四个月。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.unite.ai/deepseek-ships-v4-pro-as-its-flagship-model-leaves-preview/">DeepSeek Ships V4 Pro as Its Flagship Model Leaves Preview</a></li>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek_%28product%29">DeepSeek (product)</a></li>

</ul>
</details>

**社区讨论**: 社区反应总体积极，用户称赞其低成本和在开发任务上的强大能力。一位用户的实测发现 DeepSeek V4 Pro 比 Grok 4.6 便宜得多，但更慢且存在 bug；另一位用户则称赞该模型能以极低成本承担重型开发工作。也有评论者批评新闻链接指向 OpenRouter 而不是官方渠道。

**标签**: `#DeepSeek`, `#AI models`, `#LLM`, `#API`, `#benchmarks`

---

<a id="item-3"></a>
## [Tailscale 将数据库损坏追溯到 16 年前的 SQLite WAL 重置 Bug](https://tailscale.com/blog/sqlite-wal-reset-bug) ⭐️ 8.0/10

Tailscale 发布了一篇详细文章，说明 SQLite 的预写日志（WAL）子系统中一个大约自 2010 年以来就存在的竞态条件，导致了其控制平面数据库损坏。为了隔离并修复该问题，Tailscale 资助了一个开源的 SQLite VFS 垫片，并更新了其驱动，以便在写事务与 WAL 重置重叠时记录日志。 这一事件很重要，因为该 bug 即使在 SQLite 推荐的单写入者配置下也可能损坏数据库，并且 16 年来未被 SQLite 团队察觉。这个案例也表明，企业可以资助有针对性的开源工具，从而让整个 SQLite 生态系统受益。 该竞态发生在写入事务与检查点过程中的 WAL 重置发生碰撞时。SQLite 在 3.51.3 版本中修复了此问题，同样的分析也促使人们检查 dqlite 等相关项目。

hackernews · ropbear · 8月12日 14:22 · [社区讨论](https://news.ycombinator.com/item?id=49272832)

**背景**: SQLite 是一种嵌入式数据库，可以使用预写日志（WAL）模式：更改先追加到单独的 WAL 文件中，之后再有检查点（checkpoint）合并回主数据库。检查点完成后，SQLite 可能会重置 WAL 文件以便重用，而这个新发现的 bug 正是重置操作与并发写入之间的数据竞争。VFS 垫片是一层拦截 SQLite 文件操作的组件；Tailscale 资助的垫片通过在读写周围加入检测逻辑，帮助重现并定位了损坏问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://tailscale.com/blog/sqlite-wal-reset-bug">How Tailscale helped find the SQLite WAL-Reset bug</a></li>
<li><a href="https://antithesis.com/blog/2026/wal-reset-bug/">Breaking the WAL | Antithesis</a></li>
<li><a href="https://ubuntu.com/blog/hunting-a-16-year-old-sqlite-bug-with-tla-is-dqlite-affected">Hunting a 16-year-old SQLite bug with TLA+: is dqlite affected? | Ubuntu</a></li>

</ul>
</details>

**社区讨论**: 评论大多持正面态度，称赞这篇文章以及 Tailscale 资助 SQLite 支持和专门调试工具的决定。多位读者指出，尽管数据库是单写入者设计，该竞态仍需要多个连接才会触发；也有人认为这再次说明即使是测试覆盖极高的软件也可能隐藏微妙的 bug。

**标签**: `#sqlite`, `#database`, `#debugging`, `#tailscale`, `#open-source`

---

<a id="item-4"></a>
## [xAI 发布 Grok 4.6，引发系统提示词与基准测试讨论](https://x.ai/news/grok-4-6) ⭐️ 8.0/10

xAI 发布了其大语言模型系列最新版本 Grok 4.6。该公告迅速引发社区讨论，围绕模型的默认系统提示词、基准测试声明和竞争定位展开。 Grok 4.6 巩固了 xAI 在前沿 AI 竞赛中的地位，为开发者在价格、速度和智能体行为方面提供了又一具有竞争力的选择。围绕基准测试方法与系统提示词处理的争议，也凸显了业界对 AI 实验室如何衡量和展示模型能力的审视。 开发者报告称，xAI 的 API 会注入一条默认系统提示词，其中“不要提及这些准则”的表述可能覆盖用户指令。评论者还指出，Grok 4.6 的定价低于部分竞品，并在 Cursor 订阅中提供较宽裕的使用额度。

hackernews · iLuddite · 8月12日 15:32 · [社区讨论](https://news.ycombinator.com/item?id=49274027)

**背景**: Grok 是 xAI 开发的一系列大语言模型，由埃隆·马斯克于 2023 年 11 月推出，并集成到 X 和特斯拉产品中。系统提示词是定义 LLM 在会话中行为的初始指令。AI 模型基准测试通常基于静态任务集，一些研究者认为实验室可能人为调整性能或对排行榜过度拟合。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Grok_%28chatbot%29">Grok (chatbot) - Wikipedia</a></li>
<li><a href="https://www.techtarget.com/whatis/feature/Grok-3-model-explained-Everything-you-need-to-know">Grok 3 model explained: Everything you need to know - TechTarget</a></li>
<li><a href="https://www.secondtalent.com/resources/every-grok-ai-model-explained-compared/">Every Grok AI Model Explained and Compared (Aug, 2026)</a></li>

</ul>
</details>

**社区讨论**: 社区反应不一。一些用户称赞 Grok 4.x 快速、简洁且使用体验好，而另一些人质疑为何多家实验室在两个月内突然达到 Fable 级别的性能，怀疑存在蒸馏或基准测试作弊。默认系统提示词的行为尤其令人不满，因为它可能阻止关于模型准则的正当讨论。

**标签**: `#AI`, `#Grok`, `#xAI`, `#language models`, `#API`

---

<a id="item-5"></a>
## [为什么 Chrome 中小 JPEG 图像显示效果不同](https://guillaumetech.github.io/posts/jpg-scaling-chrome/) ⭐️ 8.0/10

一篇技术文章指出，Chrome 的缩放 JPEG 解压功能会直接从压缩数据中解码出缩小版图像，导致小尺寸 JPEG 的渲染效果与其他浏览器不同。作者借此提醒 Web 开发者：不要用 JPEG 做小图标。 这个问题的意义在于，浏览器特有的优化会改变小图片的渲染效果，从而在不同浏览器和平台上造成视觉不一致。对于追求像素级精确、跨浏览器一致界面的开发者来说，选择图片格式和尺寸时必须意识到这些隐藏差异。 缩放 JPEG 解压直接从压缩数据流生成低分辨率输出，而不是先解码完整图像再缩小。文章建议使用与显示尺寸匹配的图片，并选择 PNG 这类无损格式用于图标；Firefox 也正在推进类似的小比例解压支持（Bugzilla 2033250）。

hackernews · gutechh · 8月12日 14:00 · [社区讨论](https://news.ycombinator.com/item?id=49272549)

**背景**: JPEG 压缩通过将图像转为 YCbCr 色彩空间、对色度通道降采样、对 8x8 像素块做离散余弦变换（DCT）并量化结果来丢弃信息。缩放 JPEG 解压技术允许解码器直接从压缩数据的子集中生成小图，从而减少 CPU 和内存占用。由于不同浏览器对这种优化的实现方式不同，同一张 JPEG 在小尺寸显示时可能会出现明显差异。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cgjennings.ca/articles/jpeg-compression/">How JPEG works - Home (Christopher G. Jennings)</a></li>
<li><a href="https://bitmiracle.github.io/libjpeg.net/help/articles/KB/decompression-details.html">1. Allocate and initialize a JPEG decompression object</a></li>

</ul>
</details>

**社区讨论**: 评论区指出，PNG 在 Electron 中也有类似问题，一次基于 Chrome 的升级曾导致图标严重错乱，产品团队不得不推迟更新。有开发者认为 Chrome 和 Firefox 使用不同的缩放算法，Firefox 图像更锐利但略带振铃效应；也有人提到可以用 CSS 的 image-rendering 属性作为解决办法。大家还一致认为，使用与显示尺寸匹配的图片比更换格式更重要。

**标签**: `#JPEG`, `#Chrome`, `#image-scaling`, `#web-development`, `#browsers`

---

<a id="item-6"></a>
## [uBlock Origin 停止拦截 Facebook 广告，承认反广告拦截措施](https://digitalescapetools.com/2026/08/ublock-origin-stops-chasing-facebook-ads.html) ⭐️ 8.0/10

uBlock Origin 已停止尝试过滤 Facebook 上的广告，据报道这是因为 Facebook 的反广告拦截手段令这项努力难以为继。这一决定在 Reddit 帖子中公开，并被 Neowin 报道。 Facebook 是世界上访问量最大的网站之一，因此这是广告拦截军备竞赛中的一次重大退让，也是对希望掌控信息流体验的用户的一次打击。这也增加了其他大型平台（尤其是 YouTube）加大反广告拦截力度的风险，因为它们知道 uBlock Origin 最终可能会放弃。 Facebook 的广告以信息流中带有“赞助”（Sponsored）标记的卡片形式呈现，并通过一些难以与普通帖子区分的技术生成。根据相关报道和社区讨论，uBlock Origin 选择停止追逐这些广告，而不是继续进行无休止的维护性对抗。

hackernews · Markoff · 8月12日 11:28 · [社区讨论](https://news.ycombinator.com/item?id=49270726)

**背景**: 广告拦截工具依靠包含已知广告域名和页面元素的过滤列表来隐藏或拦截广告。Facebook 曾多次试图击败这些工具：2016 年它曾一度让广告无法被拦截，而广告拦截工具则通过将“赞助”帖子变灰等变通方法回应。近期，浏览器对 Manifest V3 等扩展机制的限制削弱了拦截扩展的能力，使这种猫鼠游戏对广告拦截器来说更难持续。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.dylanpaulus.com/posts/how-fb-avoids-adblockers">How Facebook Avoids Ad Blockers | Dylan Paulus</a></li>
<li><a href="https://www.technologyreview.com/2016/08/15/245145/facebook-cant-win-against-ad-blockers-and-heres-the-proof/">Facebook Can’t Win Against Ad Blockers ... | MIT Technology Review</a></li>
<li><a href="https://support.adblockultimate.net/en/articles/9240458-anti-adblock-techniques">Anti - adblock techniques | AdBlocker Ultimate Help Center</a></li>

</ul>
</details>

**社区讨论**: 社区反应不一：一些用户认为放弃 Facebook 是正确的决定，另一些人则担心这会鼓励 YouTube 加大对抗力度。有评论者认为，真正摆脱 Facebook 广告的唯一办法就是不再使用 Facebook；还有人预测，这场军备竞赛最终将由能够直接根据屏幕内容识别广告的计算机视觉模型来终结。

**标签**: `#uBlock Origin`, `#Facebook`, `#Ad-blocking`, `#Privacy`, `#Arms race`

---

<a id="item-7"></a>
## [AI 正在让软件工程的中层岗位消失？](https://blog.florianherrengt.com/ai-removing-middle-class-software-engineering.html) ⭐️ 8.0/10

Florian Herrengt 在一篇新博客文章中认为，AI 编程助手正在消除中级软件工程师岗位，只留下初级和高级工程师。文章在 Hacker News 上引发热议，获得 672 分和 592 条评论。 这场讨论关乎软件职业的未来：如果中级岗位真的消失，职业晋升路径、招聘方式以及初级工程师的成长方式都将受到巨大冲击。它还反映了人们对 LLM 工具可能加剧代码库中“垃圾进、垃圾出”问题的担忧。 文章主要基于个人经验而非大规模就业数据，评论者也指出目前还没有证明 AI 已导致岗位流失的“确凿证据”。一个反复出现的观点是：AI 既能放大优秀的工程实践，也能放大糟糕的工程实践，高级工程师的判断因此更有价值，而常规的“Stack Overflow 工程师”式工作会被简化。

hackernews · florianherrengt · 8月12日 13:20 · [社区讨论](https://news.ycombinator.com/item?id=49271994)

**背景**: 大型语言模型（LLM）是典型的神经网络系统，在海量文本上训练，能够生成、总结和分析人类语言，也包括代码。LLM 在生成代码时按 token 逐词预测，基于训练中习得的模式，而不是从代码库逐字复制，因此能帮助完成编码、调试和编写文档等任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Large_language_model">Large language model - Wikipedia</a></li>
<li><a href="https://www.ibm.com/think/topics/large-language-models">What are large language models (LLMs)? - IBM</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认同 AI 正在重塑工程工作，但对具体影响存在分歧。一些人警告称，失去热情的工程师现在可以把糟糕的决策放大十倍；另一些人将其视为“Stack Overflow 工程师的自动化”；还有少数人呼吁不要放弃批判性思维，并质疑在缺乏确凿证据之前就接受“岗位消失论”是否妥当。

**标签**: `#AI`, `#Software Engineering`, `#Career Impact`, `#LLM`, `#Tech Industry`

---

<a id="item-8"></a>
## [工程师警告：AI 辅助编码导致系统难以维护](https://simonwillison.net/2026/Aug/12/florian-herrengt/) ⭐️ 8.0/10

软件工程师 Florian Herrengt 在 Simon Willison 网站上转载的一篇博文中，描述了一个场景：AI 生成的代码变得非常复杂，开发人员只能让 Claude 等 AI 工具去修复他们自己也无法理解的 bug。他认为这正在威胁软件工程中的‘中产阶级’。 这一评论凸显了一个日益增长的担忧：AI 辅助编程生成的代码可能写起来高效，但几乎无法维护或调试。如果这种趋势持续下去，可能会破坏代码质量，并改变中级软件工程师的职业前景。 这段话摘自 Herrengt 的博文《AI 正在消灭软件工程的中产阶级》，其中提到了 Fable，很可能是 Anthropic 的编程工具 Claude Fable。故事描述了一个团队反复让 AI 修复 bug，而两位开发人员都无法解释数据来源的场景。

rss · Simon Willison · 8月12日 15:08

**背景**: 像 Anthropic 的 Claude Fable 这样的 AI 辅助编码工具可以根据自然语言提示生成大量代码，这可以加快开发速度，但也增加了‘认知债’——即无人能完全理解的代码。在 Herrengt 描述的场景中，系统因不断叠加服务和层而变得极其复杂，调试变成了向 AI 要答案，而不是通过推理理解代码。这反映了业界关于基于 LLM 的工具如何改变软件工程角色与职责的更广泛争论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/claude/fable">Claude Fable \ Anthropic</a></li>

</ul>
</details>

**标签**: `#AI`, `#software-engineering`, `#code-quality`, `#future-of-work`, `#LLM`

---

<a id="item-9"></a>
## [Adam 的逐坐标更新破坏旋转不变性，导致低秩隐式偏置消失](https://www.reddit.com/r/MachineLearning/comments/1vmjb3p/the_loss_does_not_see_the_basis_but_adam_does_r/) ⭐️ 8.0/10

该帖子展示了在分解模型（W=UV^T）中，Adam 的逐坐标二阶矩违反旋转不变性，从而丧失梯度下降所保留的隐式低秩偏置。作者在匹配训练损失下对 9 种更新规则进行扫描，发现它们清晰分成两类：Adam、RMSProp、Lion、signum 和 Adafactor 丢失该偏置，而 GD、共享标量 Adam、Muon 和 Shampoo 保留它。 该发现将隐式低秩正则化丢失的原因精准定位到 Adam 逐坐标分母的各向异性，而非一般的自适应机制，为矩阵分解和深度学习的优化器设计提供了明确指导。它还通过展示 Muon 的两种谱偏置行为出现在同一轴上，调和了此前关于 Muon 的矛盾结论，提供了一种统一解释。 作者构造了一个单参数族，将 Adam 的分母从逐坐标逐步过渡为单一共享标量，恢复误差沿该方向单调下降。Muon 在真正低秩目标上表现精确，但随着谱尾能量增加退化最快，并在谱尾能量约 4%处与 GD 发生交叉；理论分析仅覆盖无记忆规则，动量相关结果仍是经验性的。

reddit · r/MachineLearning · /u/EtherealGlyph · 8月12日 16:39

**背景**: 在矩阵分解中，损失函数在旋转 W = UV^T → \(UQ, VQ\) 下保持不变，因此尊重这一对称性的优化器应表现得与因子基底的选择无关。已知梯度下降及其变体具有隐式低秩偏置，该偏置与梯度噪声和优化过程的动力学有关。然而，Adam 会按坐标除以梯度幅度的估计值，这一操作不具备旋转不变性，因此可能从根本上改变优化轨迹。该帖子通过实验验证这一对称性是否为优化器保留或丧失隐式低秩偏置的分界线。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cbmm.mit.edu/sites/default/files/publications/Implicit+Rank+Minimization.pdf">CBMM Memo No. 134 March 28, 2022 SGD Noise and Implicit Low-Rank Bias in Deep</a></li>
<li><a href="https://minyoungg.github.io/overparam/resources/overparam-v2.pdf">Preprint revision 2 THE LOW-RANK SIMPLICITY BIAS IN DEEP NETWORKS Minyoung Huh</a></li>
<li><a href="https://www.emergentmind.com/topics/adam">ADAM: Adaptive Moment Estimation - emergentmind.com</a></li>

</ul>
</details>

**标签**: `#optimization`, `#Adam`, `#implicit bias`, `#matrix factorization`, `#machine learning`

---

<a id="item-10"></a>
## [LTX 发布开源视频模型 LTX-2.5，可在单张 RTX 5090 上运行](https://ltx.io/model/ltx-2-5) ⭐️ 8.0/10

LTX 发布了开源视频生成基础模型 LTX-2.5，权重、训练代码与推理管线完全开放。该模型可在单张 RTX 5090 上本地运行，支持文生视频与图生视频。 这一发布让视频 AI 研究与商业采用的门槛大幅降低，因为一个生产级视频生成模型完全开源，并且能在消费级硬件上本地运行。它为研究人员和小型团队提供了强大的开源替代方案，以替代闭源视频模型。 LTX-2.5 基于 22B 参数的非对称双流扩散 Transformer，搭配新的扩散视频解码器和 Gemma 4 12B 文本编码器。年收入低于 1000 万美元的公司可免费商用其权重；在 98 个提示词的文生视频瑕疵评测中，LTX 2.5 Pro 在十款模型中排名第一。

telegram · zaihuapd · 8月12日 02:15

**背景**: 像 LTX-2.5 这样的视频生成模型使用扩散 Transformer，从文本或图像提示生成时间上连贯的视频帧。“开放权重”意味着训练好的模型参数被公开，开发人员可以微调、自行托管并构建商业产品，而无需依赖封闭 API。Gemma 4 12B 是 Google 的中型多模态语言模型，在此作为编码器以提升提示理解能力。LTX 称在 2× GB200 GPU 上自托管时，LTX-2.5 可在 6.8 秒内生成一段 10 秒的 720p 视频，快于实时速度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ltx.io/model/ltx-2">LTX-2: Production-Grade AI Video Generation Model | LTX</a></li>
<li><a href="https://ltx.io/model/ltx-2-5">LTX-2.5: LTX&#x27;s Latest AI Open-Source Foundation Model | LTX</a></li>
<li><a href="https://developers.googleblog.com/gemma-4-12b-the-developer-guide/">Gemma 4 12B: The Developer Guide - Google Developers Blog</a></li>

</ul>
</details>

**标签**: `#video generation`, `#open-source`, `#AI model`, `#diffusion`, `#text-to-video`

---

<a id="item-11"></a>
## [微信发布 WeLM：以资源效率为核心的大语言模型家族](https://x.com/Weixin_WeChat/status/2087509298310209718) ⭐️ 8.0/10

微信团队发布了以资源效率为核心的通用大语言模型家族 WeLM。其中 WeLM-80B（3B 激活参数）已应用于微信 AI 智能体小微，而采用 MoE 架构的 WeLM-617B（23B 激活参数）正在研发中。 这一发布意义重大，因为腾讯/微信这样的头部玩家将资源效率作为大语言模型的核心，并在海量真实产品中落地。WeLM-617B 采用 MoE 架构，总参数达 617B 但仅激活 23B，有望在降低推理成本的同时保持强能力，从而影响行业趋势。 WeLM-80B 总参数量为 80B，但每次推理仅激活 3B 参数。研发中的 WeLM-617B 采用混合专家（MoE）架构，激活 23B 参数，计划用于小程序智能开发和“微信小微”小工具生成等复杂生态任务。

telegram · zaihuapd · 8月12日 13:58

**背景**: 大语言模型（LLM）是在海量文本数据上训练、能够理解和生成类人文本的 AI 系统。传统 LLM 每次推理都会激活全部参数，导致计算成本高昂。混合专家（MoE）是一种通过路由机制按输入选择性地激活多个专门子网络（“专家”）的架构，从而在总参数量更大的情况下降低计算成本。“激活参数”指处理某个 token 时实际使用的模型权重子集。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://welm.weixin.qq.com/en/">WeLM Blog</a></li>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://www.nvidia.com/en-us/glossary/mixture-of-experts/">What Is Mixture of Experts (MoE) and How It Works? - NVIDIA</a></li>

</ul>
</details>

**标签**: `#LLM`, `#MoE`, `#WeChat`, `#Tencent`, `#AI`

---
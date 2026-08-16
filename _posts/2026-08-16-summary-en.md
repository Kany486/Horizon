---
layout: default
title: "Horizon Summary: 2026-08-16 (EN)"
date: 2026-08-16
lang: en
---

> From 31 items, 4 important content pieces were selected

---

1. [Anthropic publishes Claude system prompts, sparking community analysis](#item-1) ⭐️ 8.0/10
2. [Qwen 3.8 27B Is Powerful but Defaults to Overthinking](#item-2) ⭐️ 8.0/10
3. [Investigation: $12B Wasted on PJM Modeling Mistake, Fix Risky](#item-3) ⭐️ 8.0/10
4. [Anthropic Q2 revenue jumps 14x to $11.5 billion, nears IPO](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Anthropic publishes Claude system prompts, sparking community analysis](https://platform.claude.com/docs/en/release-notes/system-prompts) ⭐️ 8.0/10

Anthropic has published the system prompts used by its Claude models in the platform release notes. The documentation reveals the actual instructions that shape Claude&\#x27;s behavior, including a prompt that tells Claude to check whether an image is actually present. This is a significant transparency move for an industry often criticized for secrecy, giving developers and researchers a rare look at how a frontier AI model is instructed. The public availability enables external auditing, interpretation, and tooling to track changes over time. The system prompts are published on Anthropic&\#x27;s platform documentation and are used by Claude&\#x27;s web interface and mobile apps at the start of every conversation to provide up-to-date information like the current date. Developers have already built diffable git histories, and the diffs reveal additions such as references to &\#x27;Claude Fable 5&\#x27; and &\#x27;Claude Mythos 5&\#x27;.

hackernews · tosh · Aug 16, 12:48 · [Discussion](https://news.ycombinator.com/item?id=49319556)

**Background**: A system prompt is a foundational instruction set given to a large language model that defines its role, behavior, tone, constraints, and capabilities for a given interaction. Unlike user prompts that change with each message, the system prompt remains constant behind the scenes, guiding the model throughout the conversation. In Claude&\#x27;s case, the system prompt also carries up-to-date context such as the current date, and Anthropic has historically kept these prompts secret.

<details><summary>References</summary>
<ul>
<li><a href="https://platform.claude.com/docs/en/release-notes/system-prompts">System Prompts - Claude Platform Docs - Anthropic</a></li>
<li><a href="https://www.promptlayer.com/glossary/system-prompt/">What is a System prompt? | PromptLayer</a></li>
<li><a href="https://likeone.ai/blog/claude-system-prompt-guide/">Claude System Prompt Guide 2026 | Like One</a></li>

</ul>
</details>

**Discussion**: Commenters largely welcomed the publication, with Simon Willison creating a git commit history of the prompts to make changes easy to track. Some expressed philosophical concerns about what the prompts reveal about model intelligence, while others worried about moderation bias, noting that stories critical of AI had disappeared from the forum. A commenter also highlighted a crisis-prioritization instruction that makes Claude favor user wellbeing over task completion in distress situations.

**Tags**: `#AI`, `#Claude`, `#System Prompts`, `#Anthropic`, `#LLM`

---

<a id="item-2"></a>
## [Qwen 3.8 27B Is Powerful but Defaults to Overthinking](https://simonwillison.net/2026/Aug/16/qwen-38-27b/) ⭐️ 8.0/10

Alibaba&\#x27;s Qwen lab released Qwen 3.8 27B, an Apache 2.0-licensed 27B parameter vision-language model. Its self-reported benchmarks show gains over both Qwen 3.6 27B and the closed-weight Qwen 3.7-Plus, but the default xhigh reasoning effort causes spectacular overthinking, with one SVG generation taking 21 minutes. An open-weight 27B model that matches or exceeds larger closed models is significant for local deployment and cost-sensitive AI use. It enables developers and researchers to run a capable vision-language model on consumer hardware, reducing reliance on expensive closed-source APIs. The default xhigh reasoning effort quickly exhausted LM Studio&\#x27;s default 8,192-token context window; loading the full 262,144-token context solved that. On the 17GB Q4\_K\_M quantized build, generating one image used 22,276 reasoning tokens and 3,223 output tokens.

rss · Simon Willison · Aug 16, 22:00

**Background**: The Apache 2.0 license is a permissive open-source license that allows free use, modification, and distribution, including for commercial purposes. Qwen is Alibaba&\#x27;s research team that releases open-weight models in various sizes, and 27B parameters is a practical size for running on a laptop. The model supports a reasoning\_effort parameter, letting users choose different levels of thinking depth to balance quality and speed.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Apache_License">Apache License</a></li>
<li><a href="https://openrouter.ai/qwen/qwen3.6-27b">Qwen3.6 27B - API Pricing &amp; Benchmarks | OpenRouter</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#Qwen`, `#open-source`, `#AI`, `#model release`

---

<a id="item-3"></a>
## [Investigation: $12B Wasted on PJM Modeling Mistake, Fix Risky](https://newsletter.semianalysis.com/p/12b-of-us-ratepayers-money-wasted) ⭐️ 8.0/10

SemiAnalysis has published an investigation finding that a modeling mistake in PJM&\#x27;s capacity market wasted roughly $12 billion of US ratepayer money. The report warns that PJM is now preparing to repeat the same flawed modeling approach, putting future costs at risk. This matters because such modeling errors direct how much ratepayers pay for grid reliability and can distort investment in power generation. If PJM repeats the mistake, it could further raise electricity costs and undermine confidence in capacity market design across the US. The investigation focuses on the effective load carrying capability \(ELCC\) methodology used to accredit capacity in PJM&\#x27;s market, which determines how much capacity resources can be paid for. While the technical details are complex, the core issue is that inaccurate modeling over-credited resources, leading to excess costs passed on to ratepayers.

rss · Semianalysis · Aug 16, 22:27

**Background**: PJM Interconnection is a regional transmission organization \(RTO\) that coordinates the electric grid across multiple states in the US and operates one of the world&\#x27;s largest wholesale electricity markets. In a capacity market, generators are paid not for the energy they produce, but for their commitment to be available to meet future electricity demand. Effective Load Carrying Capability \(ELCC\) is a method used to express a resource&\#x27;s reliability contribution relative to a &\#x27;perfect&\#x27; resource, often applied to intermittent resources like solar, wind, and storage. Incorrect application or calibration of ELCC and other modeling inputs can therefore have enormous financial consequences for ratepayers.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/PJM_Interconnection">PJM Interconnection - Wikipedia</a></li>
<li><a href="https://www.ferc.gov/understanding-wholesale-capacity-markets">Understanding Wholesale Capacity Markets | Federal Energy ...</a></li>
<li><a href="https://www.mass.gov/doc/understanding-capacity-accreditation-webinar-presentation/download">Capacity Accreditation and ELCC Primer</a></li>

</ul>
</details>

**Tags**: `#energy grid`, `#modeling`, `#PJM`, `#economics`, `#infrastructure`

---

<a id="item-4"></a>
## [Anthropic Q2 revenue jumps 14x to $11.5 billion, nears IPO](https://www.cnbc.com/2026/08/15/anthropic-revenue-jumps-to-over-11point5-billion-in-q2-report.html) ⭐️ 8.0/10

Anthropic reported preliminary Q2 revenue above $11.5 billion, a 14-fold year-over-year increase from $787 million, and higher than Q1 2026&\#x27;s $4.73 billion. Adjusted operating profit turned positive, and the company is preparing a possible large IPO this fall. This explosive growth signals that leading AI labs can rapidly convert demand into revenue, and a potential IPO would be one of the biggest tech listings of the year. It also reflects the broader momentum and intensifying competition in the AI industry. The figures are preliminary and subject to revision, according to Bloomberg, citing documents. Anthropic&\#x27;s Q2 revenue compares with $787 million in the year-ago quarter and $4.73 billion in Q1 2026, and the adjusted operating profit turned positive in the quarter.

telegram · zaihuapd · Aug 16, 07:26

**Background**: Anthropic is a leading artificial intelligence company developing large language models and AI assistants. Preliminary revenue is an unaudited early estimate, while adjusted operating profit strips out certain one-off or non-cash items to show core profitability. A 14-fold year-over-year jump typically reflects a very low prior-year base or exceptionally rapid adoption. A potential IPO would allow public investors to participate in the company&\#x27;s growth.

**Tags**: `#Anthropic`, `#AI`, `#Revenue`, `#IPO`, `#Business`

---
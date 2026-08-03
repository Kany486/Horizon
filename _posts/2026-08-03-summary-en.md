---
layout: default
title: "Horizon Summary: 2026-08-03 (EN)"
date: 2026-08-03
lang: en
---

> From 29 items, 5 important content pieces were selected

---

1. [Karpathy&\#x27;s Pinball Prompt Exposes LLM Physical Reasoning Limits](#item-1) ⭐️ 8.0/10
2. [Kakehashi: Experimental userspace runs macOS binaries on Linux ARM](#item-2) ⭐️ 8.0/10
3. [eBay harassment campaign leads to $56M payout](#item-3) ⭐️ 8.0/10
4. [Open Letters Divide AI Industry Over Open-Weights Policy](#item-4) ⭐️ 8.0/10
5. [CausalVLBench: New Benchmark for Visual Causal Reasoning in LVLMs](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Karpathy&\#x27;s Pinball Prompt Exposes LLM Physical Reasoning Limits](https://twitter.com/karpathy/status/2083749667410727319) ⭐️ 8.0/10

Andrej Karpathy tweeted a simple challenge — &\#x27;create a pinball game&\#x27; — that most frontier LLMs still fail. The ensuing discussion highlights this as a surprisingly effective qualitative benchmark for physical reasoning. This shifts LLM evaluation from text and image generation to interactive physical understanding. It offers a simple, accessible way to measure progress in AI&\#x27;s grasp of real-world dynamics. Common failure modes include walls blocking the launch chute, flippers pivoting the wrong way, and holes letting the ball fall out of reach. According to one commenter, Opus 5 is the first model to one-shot the task in a harness.

hackernews · delichon · Aug 2, 04:05 · [Discussion](https://news.ycombinator.com/item?id=49140998)

**Background**: LLMs excel at language tasks but often struggle with physical reasoning that requires understanding spatial and mechanical constraints. Research like LLMPhy integrates LLMs with physics engines to improve parameter identification in complex scenes. A playable pinball game demands implicit knowledge of mechanics such as gravity, collisions, and angles, making it a compact test of such abilities.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2411.08027">[2411.08027] LLMPhy: Parameter-Identifiable Physical ...</a></li>
<li><a href="https://github.com/merlresearch/llmphy">GitHub - merlresearch/llmphy: Release code for llmphy ...</a></li>

</ul>
</details>

**Discussion**: Commenters agree the pinball prompt is a useful qualitative benchmark, but some caution that strong performance on three.js scenes may reflect bias in training data rather than genuine physical reasoning. Others shared personal experiences of iterating with LLMs on 3D animation, noting the need for custom tuning.

**Tags**: `#LLM`, `#benchmark`, `#AI`, `#physical reasoning`, `#Karpathy`

---

<a id="item-2"></a>
## [Kakehashi: Experimental userspace runs macOS binaries on Linux ARM](https://github.com/wie-project/kakehashi) ⭐️ 8.0/10

Kakehashi is an experimental userspace project that loads macOS Mach-O binaries and runs them natively on Linux ARM. Working prototypes include 7-Zip \(passing an 8k-file multithreaded compression test\), curl \(over 200 commands/options passing an automated Docker test\), and Git tools from Xcode. If successful, it could bring macOS command-line software to ARM Linux systems, similar to what Wine and Proton did for Windows applications on Linux. This would benefit ARM Linux users—especially as ARM servers and desktops gain traction—without needing a macOS machine or a full virtual machine. The project works entirely in userspace, translating Darwin syscalls and using the Linux ARM ABI, avoiding kernel modifications. The 7-Zip prototype is currently about 5.2x slower than native execution, but the author has an optimization roadmap; the project is still early-stage and not yet ready for general use.

hackernews · vlad\_kalinkin · Aug 2, 16:26 · [Discussion](https://news.ycombinator.com/item?id=49145937)

**Background**: macOS binaries use the Mach-O format, a file layout for executables and libraries introduced in NeXTSTEP, and they call into the Darwin kernel through system calls \(syscalls\). To run a macOS binary on Linux, a compatibility layer must parse Mach-O files and translate or emulate Darwin syscalls into Linux ones, similar to how Darling or Wine translate between different system interfaces. The Linux ARM platform uses its own ABI \(Application Binary Interface\), so the translation must also handle architecture-specific calling conventions and data layouts.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mach-O">Mach-O - Wikipedia</a></li>
<li><a href="https://developer.apple.com/library/archive/documentation/Performance/Conceptual/CodeFootprint/Articles/MachOOverview.html">Overview of the Mach-O Executable Format - Apple Developer</a></li>
<li><a href="https://deepwiki.com/apple/darwin-xnu/4.3-system-calls">System Calls | apple/darwin-xnu | DeepWiki</a></li>

</ul>
</details>

**Discussion**: Commenters are enthusiastic, with several saying they have been waiting for something like this and will watch the project closely. Some suggest collaborating with the Darling project, which has an open ARM64 PR, and one user asks about a more redistributable approach using per-binary library rewriting. Others hope it could eventually support macOS Audio Unit plugins via a wrapper like yabridge, though they acknowledge the project is still early.

**Tags**: `#macOS`, `#Linux`, `#ARM`, `#compatibility layer`, `#systems programming`

---

<a id="item-3"></a>
## [eBay harassment campaign leads to $56M payout](https://www.ft.com/content/06ec1b03-d4af-40cf-b12a-4ba5a410f6d2) ⭐️ 8.0/10

Former eBay security executives were sentenced for orchestrating a harassment campaign against a couple who had criticized the company. eBay agreed to a $56 million payout to settle the matter. This case highlights serious corporate misconduct at a major technology company, where security staff targeted private citizens. It raises broader questions about corporate accountability, the role of in-house security teams, and the lengths companies may go to silence critics. Jim Baugh, eBay&\#x27;s former Senior Director of Safety and Security, was sentenced to 57 months in prison. Brian Gilbert, a former Senior Manager of Special Operations, received time served, one year of supervised release, no contact with the victims, and a $20,000 fine.

hackernews · JumpCrisscross · Aug 2, 19:19 · [Discussion](https://news.ycombinator.com/item?id=49147435)

**Background**: In 2019, eBay security executives orchestrated a campaign to intimidate David and Ina Steiner, publishers of EcommerceBytes, after the couple&\#x27;s newsletter ran critical stories about eBay. Prosecutors said seven members of eBay&\#x27;s global security team, including former police captains, worked together to harass and intimidate the Steiners. The scheme included surveillance, threatening messages, and disturbing deliveries. The case became a prominent example of corporate overreach in response to online criticism.

**Discussion**: Commenters speculated that the harassment likely extended beyond the Steiners, questioning whether other critics were targeted and whether the former police officers involved were properly investigated. One commenter, who claimed to have worked at eBay, described a broader culture of intimidation within the company. Another commenter shifted focus to eBay&\#x27;s seller fees, calling their commission structure excessive.

**Tags**: `#tech ethics`, `#corporate governance`, `#legal`, `#eBay`, `#security`

---

<a id="item-4"></a>
## [Open Letters Divide AI Industry Over Open-Weights Policy](https://simonwillison.net/2026/Aug/2/open-letters/#atom-everything) ⭐️ 8.0/10

Simon Willison summarizes recent open letters about AI open-weight policy, notably a Microsoft-shepherded letter signed by 235 companies advocating for open-weight models against potential government restrictions. Meanwhile, a separate letter signed by 1,324 frontier AI employees calls for international governance to pace automated AI development. These letters represent a high-stakes policy clash among leading AI companies over whether open-weight models should remain freely available. The outcome could shape US regulation, affect global AI competition, and determine how open technology balances innovation with safety concerns. The Microsoft-led letter explicitly supports distillation as a legitimate model-development technique, a stance contradicted by Anthropic&\#x27;s separate response calling for a crackdown on industrial-scale distillation. Pacing the Frontier, which includes signatures from OpenAI and Anthropic leadership, requests US government support for technical and governance tools to deliberately pace automated AI development.

rss · Simon Willison · Aug 2, 04:16

**Background**: Open-weight models make their trained weights publicly available, allowing others to use, modify, and study them, unlike closed models. Supporters argue this promotes transparency, competition, and safety research; critics worry they could be misused for cyberattacks, biological attacks, or by authoritarian governments. The US government has shown interest in restricting open-weight models over safety concerns, which prompted these letters.

<details><summary>References</summary>
<ul>
<li><a href="https://www.linkedin.com/pulse/open-weight-ai-models-why-every-enterprise-should-paying-misra-gi2qc">Open - Weight AI Models : Why Every Enterprise Should Be Paying...</a></li>
<li><a href="https://infercom.ai/blog/open-weight-models-explained/">Open - Weight AI Models : Why They&#x27;re a Strategic Advantage | Infercom</a></li>

</ul>
</details>

**Tags**: `#AI`, `#open weights`, `#policy`, `#Microsoft`, `#Simon Willison`

---

<a id="item-5"></a>
## [CausalVLBench: New Benchmark for Visual Causal Reasoning in LVLMs](https://www.reddit.com/r/MachineLearning/comments/1vdd7ty/r_causalvlbench_benchmarking_visual_causal/) ⭐️ 8.0/10

CausalVLBench is a newly introduced benchmark for evaluating visual causal reasoning in large vision-language models \(LVLMs\). It covers three representative tasks: causal structure inference, intervention target prediction, and counterfactual prediction, and was presented at EMNLP 2025. This benchmark addresses a critical gap in evaluating causal reasoning abilities of multimodal models, revealing their fundamental strengths and weaknesses. It is likely to motivate new research directions and improvements in LVLM design, benefiting the broader AI community. The benchmark evaluates state-of-the-art open-source LVLMs across three causal representation learning datasets. Initial results also suggest that zero-shot chain-of-thought prompting does not consistently improve causal reasoning in open-source models.

reddit · r/MachineLearning · /u/moschles · Aug 2, 09:07

**Background**: Large vision-language models \(LVLMs\) process both images and text, enabling tasks like visual question answering and captioning. Causal reasoning goes beyond correlation by understanding cause-and-effect, which is essential for robust AI. Visual causal reasoning benchmarks help systematically test whether models can infer causal structures, predict intervention effects, and answer counterfactuals. CausalVLBench is a comprehensive benchmark for multi-modal in-context learning, built to expose limitations in existing models.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2506.11034">[2506.11034] CausalVLBench: Benchmarking Visual Causal Reasoning in Large Vision-Language Models</a></li>
<li><a href="https://aclanthology.org/2025.emnlp-main.1561/">CausalVLBench: Benchmarking Visual Causal Reasoning in Large Vision-Language Models - ACL Anthology</a></li>

</ul>
</details>

**Tags**: `#benchmark`, `#vision-language models`, `#causal reasoning`, `#AI research`, `#evaluation`

---
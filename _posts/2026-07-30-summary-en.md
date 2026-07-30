---
layout: default
title: "Horizon Summary: 2026-07-30 (EN)"
date: 2026-07-30
lang: en
---

> From 41 items, 9 important content pieces were selected

---

1. [Open-source engine runs Gemma 4 26B on Macs with 2GB RAM](#item-1) ⭐️ 9.0/10
2. [AI Worm Self-Replicates via Prompt Injection in Microsoft Word](#item-2) ⭐️ 9.0/10
3. [Russia charges Telegram founder with aiding terrorism](#item-3) ⭐️ 9.0/10
4. [Moonshot AI raises $3.5B at $35B valuation, eyes IPO](#item-4) ⭐️ 9.0/10
5. [Superlogical: Mitchellh&\#x27;s New Company for Agentic Terminals](#item-5) ⭐️ 8.0/10
6. [Modular Data Centers: The LEGO Approach](#item-6) ⭐️ 8.0/10
7. [Vulkan-based ncnn achieves 10x speedup for ML inference on edge devices](#item-7) ⭐️ 8.0/10
8. [Hugging Face Platform Used to Generate Deepfake Nudes](#item-8) ⭐️ 8.0/10
9. [China Releases Draft Anti-Cyberbullying Law Including AI Harassment](#item-9) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Open-source engine runs Gemma 4 26B on Macs with 2GB RAM](https://github.com/drumih/turbo-fieldfare) ⭐️ 9.0/10

TurboFieldfare is an open-source inference engine that runs the 4-bit quantized Gemma 4 26B Mixture-of-Experts model on any M-series Mac using only about 2 GB of RAM, by streaming expert weights from SSD on demand. This technique enables running large language models on memory-constrained consumer devices, democratizing access to powerful AI. It also demonstrates a practical approach to bypassing RAM limitations for MoE models, potentially inspiring similar optimizations in other inference engines. The model&\#x27;s 4-bit quantized weights occupy about 14 GB, but by keeping the shared layers and KV cache in RAM while streaming only the required experts from SSD via bounded parallel pread, the engine achieves 5-6 tokens/s on an 8 GB M2 MacBook Air and 31-35 tokens/s on an M5 MacBook Pro. It also includes an experimental OpenAI-compatible local server with streaming and tool call support.

hackernews · gitpusher42 · Jul 29, 15:05 · [Discussion](https://news.ycombinator.com/item?id=49098510)

**Background**: Mixture of Experts \(MoE\) is a model architecture where multiple specialized sub-networks \(&\#x27;experts&\#x27;\) are activated per input, allowing more parameters while keeping inference efficient. 4-bit quantization reduces model weights to 4 bits each, drastically shrinking memory footprint at a small accuracy cost. Streaming weights from SSD during inference is an emerging technique that loads only the needed weights on demand, enabling models larger than available RAM to run on devices like laptops and phones.

<details><summary>References</summary>
<ul>
<li><a href="https://newsletter.maartengrootendorst.com/p/a-visual-guide-to-mixture-of-experts">A Visual Guide to Mixture of Experts ( MoE )</a></li>
<li><a href="https://www.emergentmind.com/topics/4-bit-model-quantization">4-Bit Model Quantization - emergentmind.com</a></li>
<li><a href="https://www.mindstudio.ai/blog/ssd-streaming-ai-models-ram-dial">SSD Streaming for AI Models: How to Turn RAM from a Wall into a Dial | MindStudio</a></li>

</ul>
</details>

**Discussion**: Community comments highlight the novelty of not needing to shove the entire model into memory, with one user noting that prior work like llama.cpp could already mmap models but TurboFieldfare&\#x27;s synchronized SSD reads are better tuned. Another user shared a compatibility fix for older macOS versions, and a third user mentioned a related project for DiffusionGemma, suggesting potential collaboration.

**Tags**: `#open-source`, `#inference-engine`, `#on-device-ai`, `#gemma`, `#macos`

---

<a id="item-2"></a>
## [AI Worm Self-Replicates via Prompt Injection in Microsoft Word](https://simonwillison.net/2026/Jul/29/ai-worming-through-word/#atom-everything) ⭐️ 9.0/10

Security researcher Håkon Måløy demonstrated a new prompt injection attack against Microsoft Copilot for Word that creates self-replicating worms. The attack hides instructions in documents that cause Copilot to propagate the malicious payload to new documents, enabling the worm to spread without the original document. This is the first demonstration of a self-replicating AI worm in a widely used office productivity tool, posing a significant security risk. It highlights the fundamental vulnerability of LLMs that cannot reliably distinguish between instructions and data, threatening enterprise data integrity and automated workflows. The hidden instructions are placed in documents used as source material for Copilot; when Copilot processes the document, it follows the instructions to alter the current document and copy the hidden payload into the output. The attack was responsibly disclosed to Microsoft 144 days prior, but no full mitigation has been released.

rss · Simon Willison · Jul 29, 18:43

**Background**: Prompt injection is a security exploit where carefully crafted inputs cause an LLM to behave in unintended ways, bypassing safeguards. Indirect prompt injection occurs when the adversarial prompt is embedded in content retrieved by the LLM, such as web pages or documents. Self-replicating AI worms combine prompt injection with the ability to propagate malicious instructions to other files or systems, as seen in prior research like the Morris II worm.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection_attack">Prompt injection attack</a></li>
<li><a href="https://thehackernews.com/2026/06/researchers-build-self-replicating-ai.html">Researchers Build Self-Replicating AI Worm That Operates Entirely on Local, Open-Weight Models</a></li>
<li><a href="https://neuraltrust.ai/blog/self-replicating-malware">The Dawn of the AI Worm: Self-Replicating Prompt Malware in Multi-Agent Systems | NeuralTrust</a></li>

</ul>
</details>

**Discussion**: Commenters expressed concern that this vulnerability is fundamentally unfixable with current LLM architectures, as they cannot separate instructions from data. Some users noted they have already uninstalled Copilot and disabled AI features to avoid such risks. Others pointed out that the attack vector will likely worsen as agents gain more access and capabilities.

**Tags**: `#security`, `#prompt injection`, `#AI`, `#Microsoft Word`, `#Copilot`

---

<a id="item-3"></a>
## [Russia charges Telegram founder with aiding terrorism](https://www.interfax.ru/russia/1106228) ⭐️ 9.0/10

Russia&\#x27;s Federal Security Service \(FSB\) has filed criminal charges against Telegram founder Pavel Durov under Article 205.1, Part 1.1 of the Criminal Code \(aiding terrorism\) and placed him on an international wanted list for failing to remove content used to coordinate attacks in Russia. This marks a major escalation in state pressure on tech platforms, potentially setting a precedent for holding platform founders personally liable for user-generated content. It could also impact Telegram&\#x27;s operations and international tech diplomacy. The FSB alleges that Telegram management refused to delete channels and bots used by Ukrainian intelligence and terrorist groups to coordinate sabotage, terrorist attacks, and fraud, causing casualties and billions of rubles in damage.

telegram · zaihuapd · Jul 29, 05:56

**Background**: The Russian Federal Security Service \(FSB\) is the country&\#x27;s primary security agency, responsible for counter-terrorism and intelligence. Telegram, known for its strong encryption and privacy features, has been a battleground for content moderation, with governments often demanding access or removal of content.

**Tags**: `#Telegram`, `#Pavel Durov`, `#Russia`, `#legal`, `#terrorism`

---

<a id="item-4"></a>
## [Moonshot AI raises $3.5B at $35B valuation, eyes IPO](https://www.bloomberg.com/news/articles/2026-07-29/china-s-moonshot-ai-passes-funding-goal-to-hit-35-billion-value) ⭐️ 9.0/10

Moonshot AI has raised $3.5 billion in a funding round, bringing its valuation to $35 billion, far exceeding its initial target of $1-2 billion. The round was driven by the success of its Kimi K3 model, which approaches frontier performance and triggered a market sell-off dubbed another &\#x27;DeepSeek moment&\#x27;. This massive funding round signals strong investor confidence in Chinese AI startups and intensifies global AI competition. The company&\#x27;s planned IPO in Hong Kong could provide a significant liquidity event and further fuel the AI arms race. Moonshot AI has initiated a new funding round with a pre-money valuation of $50 billion and plans an IPO in Hong Kong as early as this year. Its annualized recurring revenue reached $300 million in June, and daily sales grew at least sixfold after the Kimi K3 launch.

telegram · zaihuapd · Jul 29, 10:12

**Background**: The &\#x27;DeepSeek moment&\#x27; refers to the market turmoil in January 2025 when Chinese startup DeepSeek released its open-weight model DeepSeek-R1, triggering a sell-off in tech stocks due to concerns about US AI dominance. Kimi K3 is a 2.8 trillion-parameter model with a 1 million-token context window, built on novel attention mechanisms and released as the world&\#x27;s first open 3T-class model.

<details><summary>References</summary>
<ul>
<li><a href="https://platform.kimi.ai/docs/guide/kimi-k3-quickstart">Kimi K3 - Kimi API Platform</a></li>
<li><a href="https://www.kimi.com/blog/kimi-k3">Kimi K3 Tech Blog: Open Frontier Intelligence</a></li>
<li><a href="https://www.linkedin.com/pulse/why-we-wont-see-another-deepseek-moment-anytime-soon-breitenother-lzvwe">Why we won’t see another DeepSeek moment anytime soon</a></li>

</ul>
</details>

**Tags**: `#AI Funding`, `#Moonshot AI`, `#Kimi K3`, `#Valuation`, `#IPO`

---

<a id="item-5"></a>
## [Superlogical: Mitchellh&\#x27;s New Company for Agentic Terminals](https://www.superlogical.com/) ⭐️ 8.0/10

Mitchellh has announced Superlogical, a company that will build agentic terminal applications on top of the open-source libghostty library. The company plans to upstream improvements to libghostty so all users benefit. This venture is significant because it represents a sustainable open-source business model where a company builds proprietary applications on an open-source core while contributing back. It could accelerate development of intelligent terminal tools that leverage AI agents, impacting developers and systems engineers. Superlogical will consume the same MIT-licensed libghostty components available to everyone else, and will continue to upstream shared terminal work. Mitchellh previously transferred ownership of Ghostty to a non-profit.

hackernews · yan · Jul 29, 15:41 · [Discussion](https://news.ycombinator.com/item?id=49098965)

**Background**: libghostty is a cross-platform, zero-dependency C and Zig library for building terminal emulators, developed as part of the Ghostty project. Agentic terminal applications refer to terminal tools that can perform complex tasks autonomously or semi-autonomously, often integrating AI coding assistants. This model of building proprietary products on open-source foundations is known as &quot;open core.&quot;

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/ghostty-org/ghostty">GitHub - ghostty-org/ghostty: Ghostty is a fast, feature-rich, and...</a></li>
<li><a href="https://ghostty.org/docs/about">About Ghostty</a></li>

</ul>
</details>

**Discussion**: Community members praised the open-source strategy, with simonw highlighting the transfer of Ghostty ownership to a non-profit and the plan to build Superlogical as a consumer of libghostty while upstreaming improvements. Another commenter compared it to OLE/COM from Microsoft, noting similarities in embedding components. A few users criticized the enigmatic title, preferring more descriptive headlines.

**Tags**: `#terminal`, `#open-source`, `#software-engineering`, `#startup`, `#systems`

---

<a id="item-6"></a>
## [Modular Data Centers: The LEGO Approach](https://newsletter.semianalysis.com/p/the-wild-wild-west-of-lego-datacenters) ⭐️ 8.0/10

Semianalysis&\#x27; analysis examines how modular datacenter construction, akin to LEGO blocks, can solve labor shortages and accelerate deployment. As demand for compute capacity surges, traditional datacenter construction faces labor constraints; modularization offers a faster, more flexible alternative that could transform infrastructure scaling. The article likely discusses prefabricated modules, reduced on-site labor, and cost efficiency, but specific technical details from the newsletter are not provided here.

rss · Semianalysis · Jul 29, 22:09

**Background**: Modular data centers are prefabricated, factory-tested units shipped to sites for rapid assembly, operational in weeks rather than months. This approach addresses labor shortages and scalability challenges in the booming datacenter industry. The &\#x27;LEGO&\#x27; analogy emphasizes the plug-and-play nature of these modules.

<details><summary>References</summary>
<ul>
<li><a href="https://encoradvisors.com/modular-data-center/">The Modular Data Center Ultimate Guide [2025] - ENCOR Advisors</a></li>
<li><a href="https://www.zdnet.com/article/the-lego-datacentre/">The Lego datacentre | ZDNET</a></li>

</ul>
</details>

**Tags**: `#datacenters`, `#modularization`, `#infrastructure`, `#labor`, `#technology`

---

<a id="item-7"></a>
## [Vulkan-based ncnn achieves 10x speedup for ML inference on edge devices](https://www.reddit.com/r/MachineLearning/comments/1v9s4mz/vendoragnostic_ml_inference_on_production_edge/) ⭐️ 8.0/10

A Reddit post from the PostSlate team details using ncnn&\#x27;s Vulkan backend for cross-platform ML inference, achieving 10x speedups over ONNX CPU on an NVIDIA 4070 for face detection and embedding models without vendor-specific runtimes. This approach solves a critical deployment challenge for edge devices by leveraging existing Vulkan drivers, enabling efficient on-device ML across diverse hardware without relying on CUDA or vendor-specific toolkits. Benchmarks show ArcFace R50 inference dropping from 30ms \(ONNX CPU\) to 3ms \(ncnn Vulkan\), and SCRFD from 25ms to 2.5ms; model size also halves from 174MB \(ONNX fp32\) to 87MB \(ncnn fp16\). Vulkan drivers are already present on most machines, eliminating the need for additional runtime installs.

reddit · r/MachineLearning · /u/ppchaos · Jul 29, 10:22

**Background**: ncnn is a high-performance neural network inference framework by Tencent, optimized for mobile and embedded deployment with no third-party dependencies. Vulkan is a cross-platform GPU API that provides low-level access to graphics and compute hardware. The combination enables GPU-accelerated ML inference without vendor lock-in, unlike CUDA or other proprietary solutions.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/Tencent/ncnn">GitHub - Tencent/ncnn: ncnn is a high-performance neural network inference framework optimized for the mobile platform · GitHub</a></li>
<li><a href="https://onnxruntime.ai/">ONNX Runtime | Home</a></li>
<li><a href="https://pypi.org/project/ncnn/">ncnn · PyPI</a></li>

</ul>
</details>

**Tags**: `#ML inference`, `#Vulkan`, `#ncnn`, `#edge computing`, `#cross-platform`

---

<a id="item-8"></a>
## [Hugging Face Platform Used to Generate Deepfake Nudes](https://www.theverge.com/ai-artificial-intelligence/971723/hugging-face-nudify-deepfake-undress-women-children) ⭐️ 8.0/10

A report by AI Forensics found that Hugging Face&\#x27;s open-source model hosting platform is widely used to generate non-consensual deepfake nude images, with seven out of nine top image editing models capable of easily undressing women with simple prompts. This highlights a significant ethical and security issue in AI, as open-source models on Hugging Face are being misused to create non-consensual deepfake pornography, lacking effective safeguards, and posing serious risks to privacy and safety, especially for women and children. The report set up a honeypot that received over 1,000 requests in 7 days, 73% of which were sexual and nearly 7% targeted children. AI Forensics recommends Hugging Face implement prompt filtering and output scanning to block harmful image generation.

telegram · zaihuapd · Jul 29, 08:20

**Background**: Hugging Face is a popular platform for hosting open-source machine learning models, including image manipulation tools. Deepfake technology uses AI to create realistic fake images or videos, often misused for non-consensual pornography. A honeypot is a security mechanism used to detect and analyze unauthorized access or abuse.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Hugging_Face">Hugging Face</a></li>
<li><a href="https://en.wikipedia.org/wiki/Honeypot_%28computing%29">Honeypot (computing) - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#AI安全`, `#深度伪造`, `#Hugging Face`, `#AI伦理`, `#平台治理`

---

<a id="item-9"></a>
## [China Releases Draft Anti-Cyberbullying Law Including AI Harassment](https://mp.weixin.qq.com/s/PrzKFhbwjgFEGBPADvFD6Q) ⭐️ 8.0/10

On July 29, 2026, the Cyberspace Administration of China released a draft of the Anti-Cyberbullying Law for public comment, explicitly regulating the use of AI technology to generate and disseminate cyberbullying content. This is a significant policy development as it directly targets AI-generated online violence, establishing legal accountability for platforms and creators of AI tools, and setting a precedent for AI regulation in China&\#x27;s internet governance. The draft law consists of seven chapters and 60 articles, requiring platforms to establish monitoring and protective mechanisms, and introduces injunctions for personality rights and compensation for mental damages.

telegram · zaihuapd · Jul 29, 10:59

**Background**: The draft law defines cyberbullying as centralized or persistent online infringement of rights such as reputation, privacy, and personal information. The concept of personality right protection injunction originates from China&\#x27;s Civil Code, allowing victims to seek a court order to stop ongoing or imminent infringements without a full lawsuit, which is particularly relevant for internet-era harms.

<details><summary>References</summary>
<ul>
<li><a href="http://www.js.xinhuanet.com/20230713/45eb9dff79b040a7a9c3aa17aeea0a88/c.html">江苏多地法院探索发出人格权侵害禁令_新华网江苏频道</a></li>
<li><a href="https://alk.12348.gov.cn/Detail?dbID=37&amp;sysID=16880">邹某人格权侵害禁令案以案释法</a></li>

</ul>
</details>

**Tags**: `#AI regulation`, `#cyberbullying`, `#internet governance`, `#Chinese law`, `#AI ethics`

---
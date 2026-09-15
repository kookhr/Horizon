---
layout: default
title: "Horizon Summary: 2026-09-15 (EN)"
date: 2026-09-15
lang: en
---

> From 32 items, 5 important content pieces were selected

---

1. [E-ink Frame That Listens to Birds and Draws 1800s-Style Illustrations](#item-1) ⭐️ 8.0/10
2. [SemiAnalysis: Datacenter Moratoriums' Impact on US Buildout Is Overstated](#item-2) ⭐️ 8.0/10
3. [44M Parameter Ternary LLM with Neural-Symbolic Circuits Runs at 1,900 tok/s on CPU](#item-3) ⭐️ 8.0/10
4. [Prior Labs Releases TabPFN-3.5, New SOTA Tabular Foundation Model](#item-4) ⭐️ 8.0/10
5. [China Issues 15th Five-Year Plan for Electronic Information Manufacturing](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [E-ink Frame That Listens to Birds and Draws 1800s-Style Illustrations](https://github.com/arnegiacomo/fugleramme) ⭐️ 8.0/10

Developer Arne Munthe-Kaas created "fugleramme," an open-source e-ink picture frame that uses BirdNET audio classification to identify nearby birds by their songs and then generates 1800s-style illustrations of the identified species. The project combines a microphone, e-ink display, BirdNET neural network for audio classification, and AI image generation into a single self-contained device. This project demonstrates a magical integration of multiple technologies — audio AI, e-ink hardware, and generative art — into a delightful consumer experience that inspires the maker community. It shows how combining accessible tools like BirdNET and e-ink displays can create something far greater than the sum of its parts, encouraging creative hardware projects beyond conventional applications. BirdNET is a traditional deep neural network (not an LLM) capable of identifying 984 North American and European bird species by sound, originally developed for avian diversity monitoring. The project leverages e-ink displays' extreme power efficiency — community members noted that BTLE-based e-ink setups can last years on a single 2000mAh charge even with multiple refreshes per day, far outperforming WiFi-based alternatives.

hackernews · arnemunthekaas · Sep 15, 12:31 · [Discussion](https://news.ycombinator.com/item?id=49711544)

**Background**: BirdNET is a deep learning solution developed for avian diversity monitoring, using neural networks to identify nearly 3,000 common bird species by sound alone. E-ink displays are ultra-low-power display technologies that only consume electricity when changing the displayed image, making them ideal for always-on devices. The 1800s illustration style evokes the aesthetic of naturalist field guides from that era, when ornithologists like John James Audubon documented bird species through detailed hand-drawn illustrations.

<details><summary>References</summary>
<ul>
<li><a href="https://www.sciencedirect.com/science/article/pii/S1574954121000273">BirdNET: A deep learning solution for avian diversity monitoring</a></li>
<li><a href="https://apps.apple.com/us/app/birdnet/id1541842885">BirdNET - App Store - Apple</a></li>

</ul>
</details>

**Discussion**: The community was overwhelmingly enthusiastic, with commenters calling the project "magical" and "pure art," praising it as the highest inspiration for builders seeking to create delightful experiences. Technical discussions clarified that BirdNET is a traditional DNN rather than an LLM, and highlighted e-ink power efficiency advantages of BTLE over WiFi. Several commenters shared their own e-ink projects and referenced related bird monitoring efforts like birdnet-go.

**Tags**: `#e-ink`, `#BirdNET`, `#DIY hardware`, `#AI art`, `#bird watching`

---

<a id="item-2"></a>
## [SemiAnalysis: Datacenter Moratoriums' Impact on US Buildout Is Overstated](https://newsletter.semianalysis.com/p/everyone-says-datacenter-moratoriums) ⭐️ 8.0/10

SemiAnalysis published a data-driven analysis challenging the prevailing narrative that datacenter moratoriums are crippling US infrastructure buildout, revealing that while 20GW of capacity sits within restricted local boundaries, only 1,525MW has actually slipped, with 2.3GW impacted nationwide including New York. This counter-narrative is critical for AI infrastructure investors and planners who may be overestimating capacity constraints, as it suggests the real bottleneck is far smaller than headline numbers imply and that most projects within restricted zones can still proceed. The key distinction SemiAnalysis draws is between capacity sitting inside restricted boundaries (20GW) versus capacity that actually slips or gets delayed (1,525MW), noting that most prior analyses simply counted restrictions rather than measuring real project impact, which inflated perceived risk.

rss · Semianalysis · Sep 15, 20:54

**Background**: Datacenter moratoriums are local or state-level restrictions on new data center construction, typically driven by concerns over power consumption, water usage, and community impact. According to recent data, there are 321 moratoriums across 32 US states with 261 currently in force, and New York enacted the first statewide moratorium in July 2026. As AI training and inference demand surges, hyperscalers and colocation providers are racing to build new capacity, making accurate assessment of regulatory constraints essential for capacity planning.

<details><summary>References</summary>
<ul>
<li><a href="https://newsletter.semianalysis.com/p/everyone-says-datacenter-moratoriums">Everyone Says Datacenter Moratoriums Are Killing the US Buildout.</a></li>
<li><a href="https://www.electricchoice.com/datacenters/moratoriums/">Data Center Moratoriums (2026) — Which States Are Restricting Data Centers?</a></li>
<li><a href="https://www.brookings.edu/articles/data-center-moratoriums-are-not-a-substitute-for-oversight/">Data center moratoriums are not a substitute for oversight | Brookings</a></li>

</ul>
</details>

**Tags**: `#datacenters`, `#AI-infrastructure`, `#power-constraints`, `#data-analysis`, `#semianalysis`

---

<a id="item-3"></a>
## [44M Parameter Ternary LLM with Neural-Symbolic Circuits Runs at 1,900 tok/s on CPU](https://www.reddit.com/r/MachineLearning/comments/1wgzpli/i_trained_a_44m_parameter_quantized_llm_from/) ⭐️ 8.0/10

A developer trained SHADOW-50M, a 44M parameter LLM from scratch on 45B tokens using ternary {-1,0,+1} weights and fixed 512-bit fingerprint embeddings, producing a 19.8 MB model that runs at ~1,900 tok/s on a laptop CPU. The model integrates fixed symbolic circuits for arithmetic, dates, percentages, and sorting directly into the token stream, and uses a memory-mapped attention-state archive that retrieves stored records in microseconds without re-reading text. This proof-of-concept demonstrates that extreme model compression combined with neural-symbolic hybrid computation can enable capable offline AI on commodity hardware, challenging the assumption that bigger models are always better. While SHADOW loses on standard benchmarks, it dramatically outperforms a larger bf16 model on practical reasoning, arithmetic, and retrieval tasks, suggesting a viable path for edge AI where traditional LLMs fail at reliable computation. SHADOW loses to Supra-50M-Reasoning on standard benchmarks (ARC-Easy: 0.307 vs 0.435, PIQA: 0.570 vs 0.600, WikiText-2 perplexity: 186 vs 165) but dramatically outperforms it on practical tasks like arithmetic, date calculation, and record retrieval. The archive stores attention state at 1 bit per token (288 bytes/token) with a 22 bytes/token index, and at 100M tokens uses only ~28 MB RAM due to memory-mapped storage; the index also self-reinforces retrieved records, improving top-1 accuracy from 0.571 to 0.743 on repeated questions without retraining.

reddit · r/MachineLearning · /u/Final-Data-1410 · Sep 15, 12:59

**Background**: Ternary weight quantization, popularized by BitNet 1.58b, constrains model weights to {-1, 0, +1} values, eliminating expensive multiplication operations during inference and enabling dramatic model size reductions. Neural-symbolic AI combines neural network pattern recognition with symbolic reasoning by embedding logical rules and computation circuits directly into the model architecture, rather than relying on external tool calls or APIs. Fixed fingerprint embeddings replace learned embedding tables with pre-computed, immutable vector representations, reducing trainable parameters while still supporting a large vocabulary.

<details><summary>References</summary>
<ul>
<li><a href="https://newsletter.maartengrootendorst.com/p/a-visual-guide-to-quantization">A Visual Guide to Quantization - by Maarten Grootendorst</a></li>
<li><a href="https://en.wikipedia.org/wiki/Neuro-symbolic_AI">Neuro- symbolic AI - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#Quantization`, `#Edge AI`, `#Efficient Inference`, `#Neural-Symbolic`

---

<a id="item-4"></a>
## [Prior Labs Releases TabPFN-3.5, New SOTA Tabular Foundation Model](https://www.reddit.com/r/MachineLearning/comments/1wh4xhy/tabpfn35_is_released_as_the_next_sota_tabular/) ⭐️ 8.0/10

Prior Labs released TabPFN-3.5, a tabular foundation model that tops both the TabArena and BeyondArena benchmarks, achieving SOTA performance on datasets with up to 1M rows and 20k features. The release includes three variants: TabPFN-3.5-Fast (6x faster, in alpha), TabPFN-3.5-Thinking (trades compute for accuracy via API), and TabPFN-3.5-Plus. TabPFN-3.5 demonstrates that foundation models can now outperform traditional tree-based methods across a broad range of tabular tasks, including text-rich, high-cardinality, and high-dimensional data. The 'Thinking' variant notably applies reasoning-style compute scaling—previously seen in LLMs—to tabular models, opening a new direction for improving tabular ML accuracy. On BeyondArena, TabPFN-3.5 leads by +250 Elo points over the strongest previous baseline and +150 Elo over the previous overall leader, while the Thinking variant adds +20 Elo on BeyondArena and +44 Elo on TabArena over the base model. The Fast variant is still in alpha, and the Thinking variant is accessible only through the API, meaning it requires remote inference rather than local deployment.

reddit · r/MachineLearning · /u/tuanacelik · Sep 15, 16:18

**Background**: TabPFN (Tabular Prior-data Fitted Network) is a transformer-based foundation model that performs supervised classification and regression on tabular data using in-context learning, without requiring hyperparameter tuning or gradient-based training at inference time. TabArena is a continuously maintained living benchmark covering 51 curated datasets and 27+ methods including tabular foundation models, while BeyondArena spans 142 datasets across IID, temporal, and grouped task types with diverse feature types including text and high-cardinality features. Together, these benchmarks provide comprehensive evaluations that go beyond traditional static benchmarks.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/TabPFN">TabPFN</a></li>
<li><a href="https://github.com/autogluon/tabarena">GitHub - autogluon/tabarena: A Living Benchmark for Machine Learning on Tabular Data · GitHub</a></li>
<li><a href="https://aiweekly.co/alerts/beyondarena-finds-trees-still-beat-tabular-fms-off-iid-data">BeyondArena finds trees still beat tabular FMs off-IID data | AI Weekly</a></li>

</ul>
</details>

**Tags**: `#tabular-ml`, `#foundation-models`, `#SOTA`, `#machine-learning`, `#benchmark`

---

<a id="item-5"></a>
## [China Issues 15th Five-Year Plan for Electronic Information Manufacturing](https://www.secrss.com/articles/93961) ⭐️ 8.0/10

China's MIIT and NDRC jointly issued the 15th Five-Year Plan for electronic information manufacturing, deploying 17 key tasks that target advanced semiconductor process capabilities, breakthroughs in high-end mobile and PC chips, broader adoption of OpenHarmony and other domestic operating systems, and RISC-V development by 2030. This policy sets the strategic direction for China's semiconductor and OS ecosystem through 2030, with targets including 30 trillion yuan in industry revenue and 3.5% R&D intensity, signaling sustained state-backed investment in technology self-sufficiency that will reshape global supply chains and intensify competition with Western chip and OS ecosystems. The plan specifically calls for breakthroughs in high-end smartphone core chips and PC high-performance chips, alongside advancing RISC-V architecture, AI chips and terminals, and BeiDou navigation systems. The 17 key tasks span process capability improvement, domestic OS adoption, and multiple emerging technology sectors.

telegram · zaihuapd · Sep 15, 03:10

**Background**: OpenHarmony is an open-source operating system project incubated and operated by the OpenAtom Foundation, with Huawei donating its HarmonyOS L0-L2 branch source code in 2020 and 2021. RISC-V is an open instruction set architecture (ISA) originating from UC Berkeley, whose specifications are released under permissive open-source licenses and can be implemented without paying royalties, unlike proprietary ISAs such as x86 and ARM. China's Five-Year Plans are top-level policy documents that set national economic and industrial development targets, with the 15th covering roughly 2026-2030.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/RISC-V">RISC-V - 維基百科，自由的百科全書</a></li>
<li><a href="https://gitee.com/openharmony">OpenHarmony: OpenHarmony是由开放原子开源基金会（OpenAtom Foundation）孵化及运营的开源项目，目标是面向全场景、全连接、全智能时代，搭建一个智能终端设备操作系统的框架和平台，促进万物互联产业的繁荣发展。</a></li>

</ul>
</details>

**Tags**: `#semiconductor-policy`, `#RISC-V`, `#OpenHarmony`, `#china-tech`, `#domestic-chips`

---
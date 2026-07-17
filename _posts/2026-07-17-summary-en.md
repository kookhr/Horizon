---
layout: default
title: "Horizon Summary: 2026-07-17 (EN)"
date: 2026-07-17
lang: en
---

> From 32 items, 6 important content pieces were selected

---

1. [Huawei Unveils Ascend 950 SuperPoD with 6.7x Nvidia Compute](#item-1) ⭐️ 9.0/10
2. [AWS Estimated Billing Data Wildly Inaccurate, Showing Billions in Charges](#item-2) ⭐️ 8.0/10
3. [First Atmosphere Detected on Earth-like Planet in Habitable Zone](#item-3) ⭐️ 8.0/10
4. [The State of Open Source AI: A Data-Driven Landscape Analysis](#item-4) ⭐️ 8.0/10
5. [Puter Compiles Firefox to WebAssembly to Run Inside Any Browser](#item-5) ⭐️ 8.0/10
6. [Kimi K3 Released: 2.8T Open-Source Model Tops Frontend Code Arena](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Huawei Unveils Ascend 950 SuperPoD with 6.7x Nvidia Compute](https://www.ithome.com/0/978/019.htm) ⭐️ 9.0/10

On July 17, Huawei publicly unveiled the Ascend 950 SuperPoD (Atlas 950 SuperPoD) at the 2026 World Artificial Intelligence Conference (WAIC), featuring 1,024 cards delivering 1 EFLOPS FP8 and 2 EFLOPS FP4 compute with 256 TB of globally unified memory. According to a report by BOC International Securities, the Ascend 950's total compute reaches 6.7 times that of Nvidia's comparable NVL144 system equipped with 144 cards. This marks a major milestone in the AI hardware landscape and US-China tech competition, demonstrating Huawei's ability to build large-scale AI computing clusters competitive with Nvidia's top-tier systems despite advanced manufacturing process restrictions. The 1,024-card scale-up architecture represents a significant breakthrough with immediate commercial relevance for large model training and inference workloads. The Ascend 950 SuperPoD is built on Huawei's Lingqu (UnifiedBus) interconnect protocol and SuperPoD architecture, and Huawei also showcased the air-cooled Atlas 850E SuperPoD, which can be deployed in standard air-cooled data centers without liquid cooling modifications. Additionally, the Ascend 384 SuperPoD has already been commercially deployed in over 750 units across internet, telecom, and finance industries, making it the only domestic super-node system that has trained SOTA models.

telegram · zaihuapd · Jul 17, 10:27

**Background**: Huawei's Lingqu (UnifiedBus, or UB) is a unified interconnect protocol designed for SuperPoD architectures, aiming to converge I/O, memory access, and communication between heterogeneous computing units (CPU/NPU/GPU) into a single technical framework. Development began in 2019 due to restrictions on advanced manufacturing processes, driving Huawei to connect more computing resources together through multi-chip scaling. The Lingqu 1.0-based Atlas 900 SuperPoD has been commercially deployed since March 2025, while the Ascend 950 is built on the improved Lingqu 2.0 specification, which Huawei has opened to the industry. Nvidia's NVL144 is a rack-scale configuration linking 144 GPUs over NVLink, representing the comparable system Huawei benchmarked against.

<details><summary>References</summary>
<ul>
<li><a href="https://www.huawei.com/cn/news/2025/9/hc-xu-keynote-speech">以开创的超节点互联技术，引领AI基础设施新范式</a></li>
<li><a href="https://finance.jrj.com.cn/2026/07/17201957836496.shtml">华为昇腾950超节点真机首次公开亮相！业界最大1024卡规模-财经-金融界</a></li>
<li><a href="https://www.supercomputing.news/entity/nvidia-vera-rubin-nvl144">NVIDIA Vera Rubin NVL 144 — Supercomputing News</a></li>

</ul>
</details>

**Tags**: `#AI Hardware`, `#Huawei`, `#Ascend 950`, `#Supercomputing`, `#AI Chips`

---

<a id="item-2"></a>
## [AWS Estimated Billing Data Wildly Inaccurate, Showing Billions in Charges](https://news.ycombinator.com/item?id=48945241) ⭐️ 8.0/10

On approximately July 2025, numerous AWS customers began reporting absurdly inflated estimated billing charges, with figures ranging from $78 million to $1.7 billion for accounts that normally incur less than $5 per month. The issue appears to stem from a unit conversion error in AWS's metering and billing system, where storage or data transfer values measured in gigabytes (GB) were mistakenly interpreted as raw bytes, inflating costs by a factor of approximately 2^30. While the charges are clearly erroneous and will be corrected, the incident highlights the fragility of cloud billing systems that process enormous volumes of metering data for millions of customers. It also caused significant alarm and anxiety among users who feared compromised credentials or runaway costs, and it underscores the importance of robust unit handling in large-scale financial systems. A former AWS engineer explained that services emit metering values not directly tied to prices; instead, each SKU and line item is defined in a separate 'pricing plan,' and if the unit (e.g., GB) is omitted from the metering record, the billing system defaults to bytes, producing charges roughly 1,073,741,824 times higher than intended. The error factor of 2^30 aligns precisely with the difference between one gigabyte and one byte.

hackernews · nprateem · Jul 17, 09:42

**Background**: AWS uses a complex metering and billing pipeline where individual services emit usage data that is later matched against pricing plans to calculate charges. The system processes massive volumes of telemetry data across all AWS services and regions, making unit consistency critical. AWS Cost Explorer and billing alerts rely on this same estimated data stream, which is why customers received budget threshold warnings triggered by the inflated figures.

**Discussion**: The community response was a mix of dark humor and technical insight, with users sharing adrenaline-fueled reactions to seeing billion-dollar bills and former AWS engineers providing detailed explanations of how the metering pipeline works. Several commenters noted that while this particular error is obvious and will be fixed, subtler billing errors can persist for months or years, as one user recounted discovering an EC2 reservation savings calculation error in the early 2010s that took significant effort to convince AWS to correct.

**Tags**: `#AWS`, `#billing`, `#cloud-computing`, `#bug`, `#infrastructure`

---

<a id="item-3"></a>
## [First Atmosphere Detected on Earth-like Planet in Habitable Zone](https://www.bbc.com/news/articles/cy4kdd1e0ejo) ⭐️ 8.0/10

Astronomers using the James Webb Space Telescope (JWST) have detected an atmosphere around LHS 1140b, a rocky exoplanet located 48 light-years away in the habitable zone of a red dwarf star. This marks the first time an atmosphere has been confirmed on an Earth-like planet within a star's habitable zone, a critical milestone in the search for potentially life-supporting worlds. This discovery is a major step forward in the search for extraterrestrial life, as an atmosphere is considered a prerequisite for life as we know it. The detection demonstrates JWST's capability to study the atmospheric composition of small, rocky exoplanets, opening the door to characterizing the conditions on potentially habitable worlds beyond our solar system. LHS 1140b is approximately 1.7 times the radius of Earth and completes an orbit around its red dwarf host star every 24.7 days. JWST's emission spectroscopy data, collected as the planet passes behind its star, helped rule out the possibility that LHS 1140b is a mini-Neptune, confirming its rocky, Earth-like nature.

hackernews · neversaydie · Jul 17, 14:06 · [Discussion](https://news.ycombinator.com/item?id=48947560)

**Background**: The habitable zone, also known as the Goldilocks zone, is the region around a star where conditions are just right for liquid water to exist on a planet's surface. Red dwarf stars, the most common type of star in the Milky Way, are cooler and dimmer than our Sun, meaning their habitable zones are much closer to the star. Planets in these tight orbits are often tidally locked and face intense stellar radiation, which can strip away atmospheres, making the detection of an atmosphere on LHS 1140b particularly surprising and significant. The James Webb Space Telescope (JWST) is uniquely equipped to study exoplanet atmospheres through transit and emission spectroscopy, analyzing the starlight that filters through or is emitted by a planet's atmosphere to determine its chemical composition.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bbc.com/news/articles/cy4kdd1e0ejo">First atmosphere found around Earth-like planet LHS 1140 b</a></li>
<li><a href="https://earthsky.org/space/water-world-mini-neptune-lhs-1140-b/">Is this nearby exoplanet a water world? Or a mini-Neptune?</a></li>
<li><a href="https://science.nasa.gov/exoplanets/habitable-zone/">The Habitable Zone - NASA Science</a></li>

</ul>
</details>

**Discussion**: Community members expressed surprise that a rocky planet orbiting a red dwarf could retain its atmosphere against intense stellar stripping, with one commenter initially suspecting it was a mini-Neptune being boiled off before acknowledging that JWST data ruled that out. Discussions also covered the feasibility of sending a probe to the 48-light-year-distant planet, with suggestions for near-light-speed propulsion systems, and the idea of building a solar lens telescope to study such candidates in greater detail. One commenter noted that the detected helium in the atmosphere suggests the planet has an enormous escape velocity, which, if life exists there, might mean they are trapped.

**Tags**: `#astronomy`, `#exoplanets`, `#jwst`, `#space-exploration`, `#astrophysics`

---

<a id="item-4"></a>
## [The State of Open Source AI: A Data-Driven Landscape Analysis](https://stateofopensource.ai/) ⭐️ 8.0/10

Mozilla has published a data-driven presentation at stateofopensource.ai tracking the competitive landscape between open and closed AI models across various metrics. The analysis reveals a dramatic shift in market share on OpenRouter, where open models went from processing 888B tokens in March to 4.19T tokens — nearly a 5x increase in just four months, flipping the market from 60-40 in favor of closed models to 63-37 in favor of open models. This data signals a potential inflection point in the AI industry where open-source models are rapidly closing the gap with frontier closed models from OpenAI and Anthropic. The exponential growth in open model adoption has strategic implications for the sustainability of expensive frontier model development, as hyperscalers and device manufacturers can deploy open models without licensing fees. The presentation uses OpenRouter data as a proxy for overall market trends, showing open model token processing volume growing approximately 5x in four months. However, the presentation itself has been criticized for appearing AI-generated, with an overwhelming number of charts only loosely connected to the surrounding text, which some argue undermines the credibility of the analysis.

hackernews · rellem · Jul 17, 14:31 · [Discussion](https://news.ycombinator.com/item?id=48947825)

**Background**: The open vs. closed AI model debate centers on whether model weights should be publicly downloadable (open-source models like Meta's Llama, Mistral, DeepSeek, and Qwen) or accessible only via API (closed models like OpenAI's GPT, Anthropic's Claude, and Google's Gemini). Open-source models have historically lagged behind frontier closed models in performance but offer advantages in transparency, flexibility, cost, and data isolation. Mozilla, which built its brand on the open-source Firefox browser as an alternative to Internet Explorer's dominance, has positioned itself as an advocate for open AI ecosystems, drawing parallels to its historical fight against proprietary control of the web.

<details><summary>References</summary>
<ul>
<li><a href="https://www.index.dev/blog/open-source-vs-closed-ai-guide">Open -Source vs Closed AI : Trust, Security & Performance</a></li>
<li><a href="https://tendril.neural-forge.io/learn/builders/builders-foundations-ai-open-source-vs-closed-r10a10-teen">Open -Source vs Closed AI : What Llama, Mistral, and DeepSeek...</a></li>
<li><a href="https://abundance.institute/our-work/vibrant-ai-competitive-landscape">The Vibrant AI Competitive Landscape</a></li>

</ul>
</details>

**Discussion**: The community discussion featured substantive debate on market dynamics, with one user speculating that open models could ultimately threaten OpenAI and Anthropic's business models since hyperscalers can run them without licensing fees and Apple can shrink them for on-device deployment. Another user built a dashboard tracking OpenRouter data showing open models' token processing grew from 888B to 4.19T in four months. However, multiple commenters criticized the presentation itself as clearly AI-generated, arguing that the overwhelming, loosely-connected charts and lack of genuine human analysis actively hurt Mozilla's message and caused part of the audience to tune out.

**Tags**: `#open-source`, `#AI`, `#LLM`, `#market-analysis`, `#open-models`

---

<a id="item-5"></a>
## [Puter Compiles Firefox to WebAssembly to Run Inside Any Browser](https://simonwillison.net/2026/Jul/16/firefox-in-webassembly/#atom-everything) ⭐️ 8.0/10

Puter successfully compiled the Firefox/Gecko browser engine to WebAssembly using emscripten, allowing the entire Firefox browser to run inside another browser tab. The project was heavily AI-assisted, using an estimated $25,000 worth of Claude Opus and Fable tokens, though actual costs were much lower due to a Claude Max subscription plan. This is a technically impressive demonstration that pushes the boundaries of what WebAssembly can achieve, showing that even a full browser engine can be compiled and run in a sandboxed web environment. It also highlights the growing role of AI coding tools in tackling extremely complex software engineering tasks that would traditionally require large engineering teams. Firefox/Gecko was chosen specifically for its strong single-process support, and the compiled gecko.wasm file is 233MB with an additional 18MB chrome-assets.tar.zst. All network traffic is funneled through a WebSocket proxy using the Wisp protocol via Puter's servers, since browser-based code cannot open arbitrary network connections; the project claims end-to-end encryption support, which appears to hold true for HTTPS sites.

rss · Simon Willison · Jul 16, 23:34

**Background**: WebAssembly (WASM) is a low-level, assembly-like language with a compact binary format that runs in modern web browsers at near-native performance, allowing languages like C, C++, and Rust to compile and run on the web. Emscripten is a toolchain that compiles C/C++ code to WebAssembly. The Wisp protocol is a low-overhead protocol designed for proxying multiple TCP and UDP sockets over a single WebSocket connection, which is essential for enabling network access for WASM-compiled applications running in browser sandboxes.

<details><summary>References</summary>
<ul>
<li><a href="https://developer.puter.com/labs/firefox-wasm/">Firefox in WebAssembly</a></li>
<li><a href="https://github.com/HeyPuter/firefox-wasm">GitHub - HeyPuter/ firefox - wasm : Firefox in WebAssembly · GitHub</a></li>
<li><a href="https://github.com/MercuryWorkshop/wisp-protocol">GitHub - MercuryWorkshop/ wisp - protocol : Wisp is a low-overhead...</a></li>

</ul>
</details>

**Discussion**: The project generated significant interest on Hacker News, with the team having to scale up their proxy servers to handle the traffic surge during the discussion. The conversation highlighted the novelty of running a full browser inside another browser and the interesting cost dynamics of using AI coding tools for complex projects.

**Tags**: `#WebAssembly`, `#Firefox`, `#Browser`, `#AI-assisted coding`, `#Puter`

---

<a id="item-6"></a>
## [Kimi K3 Released: 2.8T Open-Source Model Tops Frontend Code Arena](https://www.kimi.com/blog/kimi-k3) ⭐️ 8.0/10

Moonshot AI released Kimi K3, the world's first open-source 2.8 trillion parameter model, featuring native vision capabilities and a 1M token context window. It ranked first in Frontend Code Arena with a score of 1679, jumping from Kimi K2.6's 18th place, topping 6 of 7 evaluation categories. The release of a 2.8T parameter open-source model with native vision and 1M context represents a significant milestone in the open-source LLM space, pushing the boundaries of what open models can achieve. Its first-place ranking in Frontend Code Arena demonstrates strong coding capabilities, though overall performance still trails top proprietary models like Claude Fable 5 and GPT 5.6 Sol. K3 is built on the Kimi Delta Attention (KDA) and Attention Residuals (AttnRes) architecture, and is available now on Kimi.com, Kimi Work, Kimi Code, and via API. Full model weights will not be released until July 27, 2026, with API pricing at $0.30 per million tokens for cache hits, $3.00 for cache misses, and $15.00 for output.

telegram · zaihuapd · Jul 17, 00:02

**Background**: Kimi Delta Attention (KDA) is an expressive linear attention mechanism that uses fine-grained, channel-wise gating to manage recurrent memory efficiently, enabling better long-context handling. Attention Residuals (AttnRes) is a drop-in replacement for standard residual connections in Transformers, allowing each layer to selectively aggregate information from all previous layers rather than using uniform additive accumulation. Frontend Code Arena is a third-party benchmark that evaluates models on agentic frontend coding tasks from real users building apps and websites using HTML and React.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/pdf/2510.26692">Kimi Linear: An Expressive, Efficient Attention Architecture</a></li>
<li><a href="https://github.com/MoonshotAI/Attention-Residuals">GitHub - MoonshotAI/ Attention - Residuals · GitHub</a></li>
<li><a href="https://x.com/arena/status/2056803664606679059">Arena.ai on X: "Code Arena: Frontend evaluates models on agentic frontend coding tasks from real users building apps and websites (HTML and React). Agents are an entirely different contest. More from Arena soon. Filter and dive into all the Code Arena: Frontend leaderboard details at:" / X</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#Open Source`, `#Kimi K3`, `#Moonshot AI`, `#Code Generation`

---
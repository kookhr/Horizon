---
layout: default
title: "Horizon Summary: 2026-11-03 (EN)"
date: 2026-11-03
lang: en
---

> From 42 items, 7 important content pieces were selected

---

1. [Astra Directly Edits Neural Network Weights to Improve Qwen](#item-1) ⭐️ 9.0/10
2. [Critical Linux Kernel IPv4 TCP Use-After-Free Vulnerability (CVE-2026-98432)](#item-2) ⭐️ 9.0/10
3. [vLLM v0.33.0 Released with PyTorch 2.14, CUDA 13.0, and Major Performance Gains](#item-3) ⭐️ 8.0/10
4. [Subvocal: Smart Glasses That Decode Silent Speech via RF Signals](#item-4) ⭐️ 8.0/10
5. [WIRED Exposes 400+ AI Apps Hiding Deepfake Pornography Features](#item-5) ⭐️ 8.0/10
6. [Anthropic IPO Prospectus Reveals $33.2B Revenue and $104B Net Loss](#item-6) ⭐️ 8.0/10
7. [Abu Dhabi Signs Four Agreements with OpenAI for Machine-Readable Government](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Astra Directly Edits Neural Network Weights to Improve Qwen](https://rikiyat.github.io/blog/weight-space-programming/) ⭐️ 9.0/10

A blog post demonstrates that GPT-6 Astra can natively read, understand, and directly edit the raw weights of neural networks without any additional training or gradient descent, achieving approximately a 5x improvement in math performance on a small Qwen model through targeted weight modifications. This represents a potentially groundbreaking capability for recursive self-improvement (RSI), as an LLM that can directly reason about and manipulate weight spaces could iteratively improve itself or other models without traditional training pipelines, raising profound questions for AI safety and alignment. Astra traced a looping failure mode in the Qwen model to specific directions written by the MLPs of layers 15 and 19, then subtracted that direction from 64 output columns in each layer (131,072 weights total), effectively removing the looping behavior — analogous to ablating a single behavioral direction from a model's weight matrix.

hackernews · dbreunig · Nov 2, 18:21 · [Discussion](https://news.ycombinator.com/item?id=50341174)

**Background**: Weight-space programming is a technique where a general-purpose language model reads the raw numerical weights of a neural network to infer its behavior, then directly modifies those weights to fix bugs or add capabilities — all without gradient descent or fine-tuning. Qwen is a family of open-weight large and small language models developed by Alibaba Cloud, commonly used as a base for further fine-tuning in the open-source community. GPT-6 Astra is OpenAI's most advanced model, featuring state-of-the-art reasoning and computer-use capabilities. Traditionally, modifying a neural network's behavior requires training through backpropagation on large datasets, making direct weight editing by an LLM a fundamentally different paradigm.

<details><summary>References</summary>
<ul>
<li><a href="https://kingy.ai/blog/weight-space-programming-ai-agent-model-weights/">Weight-Space Programming: GPT-6 Astra Edits Qwen - kingy.ai</a></li>
<li><a href="https://elsolitario.org/en/2026/11/02/mit-csail-astra-edits-0-016-of-qwen3-weights/">Weight-Space Programming: How Astra Edits Weights</a></li>
<li><a href="https://github.com/xero00000/weight-space-programming/blob/main/">GitHub - xero00000/weight-space-programming: Agent skill for ...</a></li>

</ul>
</details>

**Discussion**: Community sentiment ranges from astonishment to cautious analysis. User vessenes expressed shock at Astra's native weight-understanding capabilities, while xg15 noted this aligns with LLMs' demonstrated ability to rapidly grasp complex systems. A notable counterargument from vanyle suggests this is not an emergent capability but rather a trained behavior, hypothesizing OpenAI deliberately trained Astra on neural weight data to pursue recursive self-improvement. NitpickLawyer provided detailed technical validation of Astra's methodology, confirming the specificity of its weight edits.

**Tags**: `#weight-space-programming`, `#recursive-self-improvement`, `#llm-capabilities`, `#neural-network-weights`, `#ai-safety`

---

<a id="item-2"></a>
## [Critical Linux Kernel IPv4 TCP Use-After-Free Vulnerability (CVE-2026-98432)](https://t.me/zaihuapd/44866) ⭐️ 9.0/10

A critical use-after-free vulnerability (CVE-2026-98432) has been disclosed in the Linux kernel's IPv4 TCP stack that is remotely exploitable without authentication or user interaction. Anthropic has published a remote code execution (RCE) exploit example targeting MPTCP listening ports, and the Go security team confirmed that Go 1.24+ services on Linux are exposed by default because MPTCP is enabled for listen sockets. This vulnerability affects a vast number of production Linux servers and is trivially exploitable from the network side, potentially leading to remote code execution. The impact is significantly broadened because Go 1.24+ enables MPTCP by default, meaning many modern backend services and APIs built with Go are exposed even if their developers never explicitly configured MPTCP. Disabling MPTCP via GODEBUG=multipathtcp=0 prevents the specific exploit described by Anthropic but does not fix the underlying kernel use-after-free condition, meaning other exploitation paths may still exist. The vulnerability is not limited to MPTCP scenarios; even systems without MPTCP listeners may be affected, so patching the kernel itself is the only complete mitigation.

telegram · zaihuapd · Nov 3, 02:37

**Background**: Multipath TCP (MPTCP) is an IETF-standardized extension to TCP (RFC 8684) that allows a single TCP connection to use multiple network interfaces simultaneously, improving throughput and providing failover capability. A use-after-free vulnerability occurs when a program continues to access memory after it has been freed, which can lead to arbitrary code execution. Since Go 1.24, the Go standard library's net package enables MPTCP by default for listen sockets on Linux (GODEBUG multipathtcp defaults to 2), meaning any Go service calling Listen() will open MPTCP sockets unless explicitly disabled.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/golang/go/issues/82717">proposal: net: Disable MPTCP by default · Issue #82717 ...</a></li>
<li><a href="https://www.kernel.org/doc/html/next/networking/mptcp.html">Multipath TCP (MPTCP) — The Linux Kernel documentation</a></li>
<li><a href="https://en.wikipedia.org/wiki/Multipath_TCP">Multipath TCP - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#security`, `#linux-kernel`, `#vulnerability`, `#mptcp`, `#go`

---

<a id="item-3"></a>
## [vLLM v0.33.0 Released with PyTorch 2.14, CUDA 13.0, and Major Performance Gains](https://github.com/vllm-project/vllm/releases/tag/v0.33.0rc3) ⭐️ 8.0/10

vLLM v0.33.0 is a major release with 927 commits from 389 contributors (122 new), upgrading to PyTorch 2.14.0 with Triton 3.8.0 and dropping CUDA 12.9 in favor of CUDA 13.0-only wheels and images. The release adds support for numerous new models including the 501B MoE Reflection Beam-1.0, introduces ABI-stable CUDA wheels with libtorch, an AWS EFA Docker image for multi-node serving, and substantial speculative decoding and decode performance improvements across NVIDIA and AMD platforms. As one of the most widely adopted open-source LLM inference engines, vLLM's move to CUDA 13.0 exclusivity and PyTorch 2.14 sets the infrastructure baseline for the broader LLM serving ecosystem. The performance improvements—such as 1.5-2x decode speedups on GB300 for Kimi-K3 and 2.32x interactivity gains on MI300X via MonoKernel—directly translate to lower serving costs and better latency for production LLM deployments at scale. Notable breaking changes include the removal of Medusa and the MLP speculator, the legacy Ray compiled-graph executor, and deprecation of --mamba-cache-mode; requests sent during paused generation now return HTTP 503, and the NIXL connector requires version 1.5 or newer. The release also introduces the OpenAI-compatible /v1/decisions endpoint enabled by default, optional late chunking for embeddings, a Rust frontend parity push, concurrent worker startup for TP > 1, and a watchdog that dumps stack traces from stuck processes.

github · khluu · Nov 2, 10:10

**Background**: vLLM is a high-throughput LLM inference and serving engine that uses PagedAttention for efficient KV cache memory management, widely deployed in production for serving models from Llama to DeepSeek. Speculative decoding is a technique where a smaller 'drafter' model generates candidate token blocks that are verified in parallel by the main model, reducing inference latency; DFlash2 is a block-diffusion drafter that predicts an entire block of tokens in a single forward pass. AWS EFA (Elastic Fabric Adapter) is a custom network interface for EC2 instances that provides high-throughput, low-latency inter-node communication critical for distributed multi-GPU LLM serving. ABI (Application Binary Interface) stability ensures that compiled binary wheels remain compatible across library versions, reducing the need for recompilation when underlying dependencies like libtorch are updated.

**Tags**: `#vllm`, `#llm-inference`, `#pytorch`, `#cuda`, `#model-serving`

---

<a id="item-4"></a>
## [Subvocal: Smart Glasses That Decode Silent Speech via RF Signals](https://news.ycombinator.com/item?id=50340088) ⭐️ 8.0/10

Subvocal, a YC F26 company founded by two former Georgia Tech CS students, has launched smart glasses that use RF (radio frequency) signals to decode silent and internal speech into text at the speed of speech. The glasses emit radio waves that pass through the face and are modulated by tongue, lip, and soft palate movements during silent mouthing, with foundation models trained to decode these signal perturbations into text. This technology could be paradigm-shifting for hands-free and accessible computing, enabling discreet computer interaction in libraries, offices, and public spaces where audible speech is impractical. If successful, it would represent the first practical wearable product for silent speech interfaces, a field that has remained largely academic despite decades of research including MIT's AlterEgo project. The founders initially tried EMG (electromyography) electrodes but abandoned this approach due to signal instability from sweat, electrical interference, placement variability, and user discomfort. The current RF-based system requires users to mouth words with closed lips (not merely think words), and the company faces a significant cross-user generalization challenge because everyone's facial anatomy produces vastly different RF signal patterns, which they are addressing by massively scaling data collection.

hackernews · aarushyadav · Nov 2, 17:16

**Background**: Subvocal recognition (SVR) is the process of detecting subvocalization—the internal articulation of words without producing audible sound—and converting it to digital text output. Silent Speech Interfaces (SSIs) have been researched for years as a way to enable communication without audible speech, using various sensing technologies including EMG, EEG, and electromagnetic articulography. MIT's AlterEgo project was a notable prior attempt that used EMG sensors to read neuromuscular signals from the jaw and face, but it remained a research prototype and never became a commercial product. Google reportedly explored similar technology for smartphones but shelved the project due to privacy concerns about the intimate biometric data such systems could capture.

<details><summary>References</summary>
<ul>
<li><a href="https://www.wikiwand.com/en/articles/Subvocal_recognition">Subvocal recognition - Wikiwand</a></li>
<li><a href="https://www.designwhine.com/meet-alterego-the-technology-from-mit/">Meet AlterEgo: The Technology From MIT That Reads... | DesignWhine</a></li>
<li><a href="https://en.wikipedia.org/wiki/Subvocal_recognition">Subvocal recognition - Wikipedia</a></li>

</ul>
</details>

**Discussion**: The community response was largely enthusiastic, with users praising the technology as sci-fi-like and highlighting its potential for accessibility and hands-free computing. Practical concerns were raised about glasses fit for different nose sizes and head shapes, prescription lens compatibility, and whether the device could attach to existing glasses rather than being standalone. Several commenters raised significant privacy concerns, referencing Google's shelved similar project and questioning where inference occurs and whether the device works offline, while others asked for technical comparisons to existing silent speech approaches like LipNet and other open-source projects.

**Tags**: `#hardware`, `#speech-recognition`, `#wearables`, `#accessibility`, `#YC`

---

<a id="item-5"></a>
## [WIRED Exposes 400+ AI Apps Hiding Deepfake Pornography Features](https://www.wired.com/story/hundreds-of-mundane-ai-apps-are-hiding-abusive-deepfake-features/) ⭐️ 8.0/10

A WIRED investigation published on November 2 uncovered a network of over 400 interconnected AI apps and websites disguised as ordinary tools—such as pet portrait generators and language-learning apps—that secretly load deepfake pornography interfaces, enabling users to upload anyone's photo to generate explicit images or videos. Following WIRED's findings, Apple removed 19 apps, Google removed most of the 27 apps still on Google Play (which had accumulated over 350,000 downloads), and Meta blocked 209 related apps from advertising. This investigation exposes a critical vulnerability in app store review processes: developers can pass initial scrutiny with benign content and then swap in remote web content to serve non-consensual deepfake pornography, affecting potentially hundreds of thousands of users—including minors, since many apps were rated suitable for all ages. The scale of the network and its ability to evade detection by major platforms highlights systemic gaps in AI governance and content moderation that demand urgent attention. Apple confirmed that developers passed app review with legitimate content and then swapped remote web content afterward, a technique known as post-review content substitution. Researchers linked the network through shared code, domain registrations, and ad-tracking identifiers, tracing it to Chinese developers and a Hong Kong-registered company, though the operators did not respond to requests for comment.

telegram · zaihuapd · Nov 2, 12:45

**Background**: Deepfake technology uses generative AI models, typically based on encoder-decoder architectures in deep learning, to synthesize or alter images and videos so realistically that they can deceive viewers. In the context of this investigation, the apps allowed users to upload ordinary photos of real people and generate non-consensual explicit imagery. The app store review bypass technique involves submitting a legitimate app for review, then remotely changing the web content the app loads after approval—meaning the malicious features are never seen by reviewers.

<details><summary>References</summary>
<ul>
<li><a href="https://www.researchgate.net/publication/390972234_The_Rise_of_AI-Generated_Deepfakes_Techniques_Challenges_Implications_and_Countermeasures">(PDF) The Rise of AI- Generated Deepfakes : Techniques, Challenges...</a></li>
<li><a href="https://virbo.wondershare.com/ai-voice-clone/deepfake-ai-image-generator.html">7 Best Free Deepfake Image Generators in 2025</a></li>

</ul>
</details>

**Tags**: `#AI ethics`, `#deepfake`, `#platform security`, `#investigative journalism`, `#AI governance`

---

<a id="item-6"></a>
## [Anthropic IPO Prospectus Reveals $33.2B Revenue and $104B Net Loss](https://www.cnbc.com/2026/11/02/anthropic-ant-s-1-quarter-financials.html) ⭐️ 8.0/10

Anthropic updated its IPO prospectus on Monday, disclosing $33.24B in revenue for the first three quarters of 2026 — a roughly 1200% year-over-year increase — with Q3 alone generating approximately $17B. The filing also revealed a $104B net loss for the same period, far exceeding the prior year's $25.1B loss, alongside approximately $895.4B in cumulative compute and infrastructure purchase and lease commitments. This filing offers rare transparency into the financial economics of a frontier AI company at massive scale, revealing both extraordinary revenue growth and the enormous capital requirements of competing at the AI frontier. The $895.4B in infrastructure commitments underscores the staggering investment needed to build and maintain cutting-edge AI capabilities, while the distinction between accounting losses and actual cash burn is critical for investors evaluating the company's true financial health. The $104B net loss is primarily an accounting artifact from mark-to-market fair value adjustments on convertible bonds and derivative liabilities — as Anthropic's valuation increased, the fair value of these liabilities rose, generating large non-cash paper losses that do not reflect actual operating cash burn. Nearly all of the $895.4B in cumulative commitments is allocated to compute and infrastructure, signaling the capital-intensive nature of frontier AI development.

telegram · zaihuapd · Nov 2, 15:12

**Background**: Convertible bonds can include an embedded derivative component (the conversion option) that must be accounted for at fair value under applicable accounting standards. When a company's valuation rises significantly between fundraising rounds, the fair value of this derivative liability increases, generating a non-cash accounting loss on the income statement even though no actual cash has been spent. This mark-to-market treatment is common among pre-IPO companies that have raised capital through convertible instruments, and the resulting paper losses can appear alarming in headlines but do not reflect the company's actual cash burn or operational health.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ipobonanza.com/news/2026-10-06-how-to-read-a-mark-to-market-loss-on-convertible-instruments">How to Read a Mark-to-Market Loss on Convertibles | IPO Bonanza</a></li>
<li><a href="https://aitechmodel.com/anthropic-72-billion-convertible-notes-charge/">Anthropic Convertible Notes: The $72 Billion Charge</a></li>

</ul>
</details>

**Tags**: `#anthropic`, `#ai-finance`, `#ipo`, `#infrastructure`, `#frontier-ai`

---

<a id="item-7"></a>
## [Abu Dhabi Signs Four Agreements with OpenAI for Machine-Readable Government](https://thenextweb.com/news/openai-abu-dhabi-deals-machine-readable-government-mubadala) ⭐️ 8.0/10

Abu Dhabi signed four agreements with OpenAI on Monday, covering government operations, investment analysis, energy, and education. The flagship 'machine-readable government' initiative converts policies and regulations into AI-readable formats to help officials verify permits and license applications, with a pilot already running on food imports. This represents one of the most comprehensive government-level AI adoption initiatives to date, involving major Abu Dhabi entities including Mubadala, G42, and ADNOC across multiple critical sectors. The 'machine-readable government' concept could fundamentally transform how governments operate by making policies directly interpretable by AI systems, potentially setting a precedent for other nations. Mubadala is collaborating with OpenAI and G42's Inception42 for investment analysis, while Inception42 separately signed a five-year agreement to provide AI models to UAE government bodies, enterprises, and schools. ADNOC became the first energy company to use OpenAI's Frontier platform, and importantly, human officials retain final decision-making authority in the machine-readable government initiative.

telegram · zaihuapd · Nov 2, 15:55

**Background**: Machine-readable government refers to converting legislation, policies, and regulations into structured, machine-friendly formats that AI systems can directly interpret and process, enabling more efficient and transparent governance. G42 is an Emirati AI development holding company founded in 2018 and based in Abu Dhabi, with its subsidiary Inception focusing on industry-specific AI solutions including the Arabic-native Jais model. OpenAI's Frontier platform is a recently launched enterprise platform designed for building, deploying, and managing AI agents for business customers.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/G42_(company)">G 42 ( company ) - Wikipedia</a></li>
<li><a href="https://news.aibase.com/news/25321">OpenAI Launches Frontier Platform : Building AI Colleagues to...</a></li>
<li><a href="https://www.linkedin.com/pulse/machine-readable-legislation-key-milestone-toward-smarter-munir-rbmne">Machine - Readable Legislation: A Key Milestone Toward Smarter...</a></li>

</ul>
</details>

**Tags**: `#openai`, `#government-ai`, `#abu-dhabi`, `#machine-readable-government`, `#public-sector`

---
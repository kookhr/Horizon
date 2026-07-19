---
layout: default
title: "Horizon Summary: 2026-07-19 (EN)"
date: 2026-07-19
lang: en
---

> From 24 items, 2 important content pieces were selected

---

1. [Alibaba Announces Qwen 3.8, a 2.4T Parameter Open-Weights LLM](#item-1) ⭐️ 9.0/10
2. [SRE Replaces $120k Bowling Scoring System with $1,600 in ESP32s](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Alibaba Announces Qwen 3.8, a 2.4T Parameter Open-Weights LLM](https://twitter.com/Alibaba_Qwen/status/2078759124914098291) ⭐️ 9.0/10

Alibaba has announced the upcoming release of Qwen 3.8, a 2.4 trillion parameter open-weights large language model, branded as Qwen3.8-Max-Preview. The announcement appears to be a direct competitive response to Moonshot AI's recent unveiling of Kimi K3, a 2.8 trillion parameter open-weights model expected on Hugging Face by July 27. This announcement signals an escalating open-weights arms race between major Chinese AI players, which could accelerate the democratization of frontier-level models for local deployment and research. The competition between Alibaba and Moonshot AI may push the broader industry toward releasing increasingly powerful open models, benefiting developers and users who rely on locally-hosted LLMs for privacy and cost reasons. Alibaba has not yet disclosed the active-parameter count or mixture-of-experts (MoE) configuration for Qwen 3.8, meaning the 2.4T figure is a total parameter count rather than a measure of per-token compute cost. Alibaba claims the model is second only to Claude Fable 5 in its internal benchmarking, though no public benchmark results have been released yet.

hackernews · nh43215rgb · Jul 19, 08:44 · [Discussion](https://news.ycombinator.com/item?id=48966120)

**Background**: Qwen is Alibaba's series of large language models, which includes both dense and mixture-of-experts (MoE) architectures available in various sizes for local and cloud deployment. Moonshot AI is a Chinese AI startup known for its Kimi chatbot and long-context models, and its recently announced Kimi K3 uses a hybrid linear attention mechanism called Kimi Delta Attention with a 1M-token context window. In MoE models, only a fraction of the total parameters are activated for any given token, so the total parameter count can be much larger than the actual compute required per inference. The open-weights approach allows developers to download and run models locally, which is increasingly viable with tools like llama.cpp, Ollama, and LM Studio.

<details><summary>References</summary>
<ul>
<li><a href="https://officechai.com/ai/alibaba-qwen-3-8/">Alibaba Announces 2.4 Trillion-Parameter Open-Weight Qwen 3.8, Says It's Second Only To Fable 5</a></li>
<li><a href="https://techsy.io/en/blog/qwen-3-8">Qwen3.8: 2.4T Parameters, Open Weights, No Benchmarks</a></li>
<li><a href="https://platform.kimi.ai/docs/guide/kimi-k3-quickstart">Kimi K 3 - Kimi API Platform</a></li>

</ul>
</details>

**Discussion**: Community sentiment is largely positive about the open-weights competition, with users like adrian_b noting that regardless of Alibaba's motivations, consumers win from this rivalry. Several users discussed the practical viability of local deployment, with overgard reporting that Qwen 3.6 27B runs 2-3x faster using the mtplx runtime on an M5 Max MacBook, and nsbk expressing hope for smaller Qwen 3.8 variants for local use with sensitive data. However, user 5701652400 offered a strongly negative counterpoint, calling Qwen 3.7 Pro "totally unusable" for software engineering tasks compared to DeepSeek V4 Pro, citing issues with going off track and stuck loops.

**Tags**: `#LLM`, `#Open-Weights`, `#Alibaba`, `#Qwen`, `#AI`

---

<a id="item-2"></a>
## [SRE Replaces $120k Bowling Scoring System with $1,600 in ESP32s](https://news.ycombinator.com/item?id=48968606) ⭐️ 8.0/10

An SRE who owns a rural 8-lane bowling center built a prototype replacement for a $120,000 proprietary scoring system using approximately $1,600 worth of ESP32 microcontrollers, reducing per-lane-pair costs from $4,000 to $200-$400. The system, called OpenLaneLink, uses an ESPNow mesh network with RS485 fallback, reporting to a Raspberry Pi running Redis, and the creator plans to open-source the entire hardware, firmware, and software stack. This project demonstrates how modern, low-cost open hardware can replace expensive legacy proprietary systems, achieving a 98.7% cost reduction while gaining full control over data, customization, and repairs. It highlights a broader opportunity to retrofit aging industrial and commercial equipment with commodity microcontrollers, challenging vendor lock-in across niche industries where proprietary systems remain absurdly priced relative to their actual technical complexity. The architecture uses ESP32 nodes in a star-topology ESPNow mesh, each emitting sensor events and accepting commands via a gateway node connected to a Raspberry Pi over UART, with RS485 as a wired fallback for noisy RF environments. The bowling machines themselves are 70 years old and purely mechanical, meaning the expensive proprietary system was essentially just actuating a single relay per lane to trigger the machine, while sensors include optocouplers, IR-break-beam sensors, and relays running slightly different firmware per node.

hackernews · section33 · Jul 19, 14:41

**Background**: Bowling scoring systems calculate ball speed and trajectory, perform camera-based pin detection, run foul detection, manage animations, and control pinsetting machines and ball returns. Modern systems use overhead cameras to detect standing pins and send scoring information, replacing older mechanical sensors integrated into the pinsetter mechanism. The ESP32 is a low-cost microcontroller with built-in Wi-Fi and Bluetooth capabilities, widely used in IoT and embedded systems projects, making it ideal for retrofitting applications that require wireless connectivity and sensor interfacing at scale.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Pinsetter">Pinsetter - Wikipedia</a></li>
<li><a href="https://www.digikey.com/es/maker/blogs/2024/a-guide-for-the-esp32-microcontroller-series">A Guide for the ESP 32 Microcontroller Series</a></li>
<li><a href="https://www.flybowling.com/the-bowling-scoring-system-cost-guide.html">The Bowling Scoring System Cost Guide</a></li>

</ul>
</details>

**Discussion**: The community response was overwhelmingly positive, with commenters calling it an archetypal Hacker News post and noting the broad applicability of retrofitting old mechanical systems with modern embedded technology. Several commenters shared related projects—including another bowling center owner with a 1970s Intel D8749H-based system and someone retrofitting old machine tools—while others suggested exciting feature expansions like LED chase effects, DMX light shows, and tap-to-pay kiosk functionality.

**Tags**: `#ESP32`, `#embedded systems`, `#hardware`, `#retrofitting`, `#reverse engineering`

---
---
layout: default
title: "Horizon Summary: 2026-07-19 (ZH)"
date: 2026-07-19
lang: zh
---

> 从 24 条内容中筛选出 2 条重要资讯。

---

1. [阿里巴巴宣布即将发布 Qwen 3.8，一个 2.4T 参数开源大模型](#item-1) ⭐️ 9.0/10
2. [SRE 用价值 1600 美元的 ESP32 替换价值 12 万美元的保龄球计分系统](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [阿里巴巴宣布即将发布 Qwen 3.8，一个 2.4T 参数开源大模型](https://twitter.com/Alibaba_Qwen/status/2078759124914098291) ⭐️ 9.0/10

阿里巴巴宣布即将发布 Qwen 3.8，一个拥有 2.4 万亿参数的开源大语言模型，品牌名为 Qwen3.8-Max-Preview。这一公告似乎是对月之暗面最近发布的 Kimi K3 的直接竞争回应，后者是一个拥有 2.8 万亿参数的开源模型，预计将于 7 月 27 日在 Hugging Face 上发布。 这一公告标志着中国主要 AI 企业之间开源权重军备竞赛的升级，可能会加速前沿模型在本地部署和研究中的普及。阿里巴巴与月之暗面之间的竞争可能推动整个行业发布越来越强大的开源模型，从而使那些出于隐私和成本考虑而依赖本地部署 LLM 的开发者和用户受益。 阿里巴巴尚未披露 Qwen 3.8 的活跃参数量或混合专家架构配置，这意味着 2.4T 是总参数量，而非每个 token 的计算成本指标。阿里巴巴声称该模型在其内部基准测试中仅次于 Claude Fable 5，但尚未公开任何基准测试结果。

hackernews · nh43215rgb · 7月19日 08:44 · [社区讨论](https://news.ycombinator.com/item?id=48966120)

**背景**: Qwen 是阿里巴巴的大语言模型系列，包含可用于本地和云端部署的多种规模的密集模型和混合专家架构模型。月之暗面是一家以 Kimi 聊天机器人和长上下文模型闻名的中国 AI 初创公司，其最近发布的 Kimi K3 采用了一种名为 Kimi Delta Attention 的混合线性注意力机制，具有 100 万 token 的上下文窗口。在 MoE 模型中，每个 token 只激活总参数的一小部分，因此总参数量可以远大于每次推理的实际计算量。开源权重方法允许开发者下载并在本地运行模型，随着 llama.cpp、Ollama 和 LM Studio 等工具的发展，这种方式变得越来越可行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://officechai.com/ai/alibaba-qwen-3-8/">Alibaba Announces 2.4 Trillion-Parameter Open-Weight Qwen 3.8, Says It's Second Only To Fable 5</a></li>
<li><a href="https://techsy.io/en/blog/qwen-3-8">Qwen3.8: 2.4T Parameters, Open Weights, No Benchmarks</a></li>
<li><a href="https://platform.kimi.ai/docs/guide/kimi-k3-quickstart">Kimi K 3 - Kimi API Platform</a></li>

</ul>
</details>

**社区讨论**: 社区对开源权重竞争的情绪总体积极，用户 adrian_b 指出，无论阿里巴巴的动机如何，消费者都是这场竞争的赢家。多位用户讨论了本地部署的实际可行性，overgard 报告称在 M5 Max MacBook 上使用 mtplx 运行时，Qwen 3.6 27B 的速度提升了 2-3 倍，nsbk 则希望 Qwen 3.8 能发布更小的版本用于处理敏感数据的本地使用。然而，用户 5701652400 提出了强烈的负面反馈，称与 DeepSeek V4 Pro 相比，Qwen 3.7 Pro 在软件工程任务中"完全无法使用"，指出存在偏离主题和陷入死循环等问题。

**标签**: `#LLM`, `#Open-Weights`, `#Alibaba`, `#Qwen`, `#AI`

---

<a id="item-2"></a>
## [SRE 用价值 1600 美元的 ESP32 替换价值 12 万美元的保龄球计分系统](https://news.ycombinator.com/item?id=48968606) ⭐️ 8.0/10

一位拥有乡村 8 球道保龄球中心的 SRE 构建了一个原型系统，用价值约 1600 美元的 ESP32 微控制器替代了价值 12 万美元的专有计分系统，将每对球道的成本从 4000 美元降至 200-400 美元。该系统名为 OpenLaneLink，采用 ESPNow 网状网络并配有 RS485 有线回退机制，向运行 Redis 的树莓派报告数据，创建者计划将硬件、固件和软件栈全部开源。 该项目展示了现代低成本开源硬件如何替代昂贵的传统专有系统，在实现 98.7%成本削减的同时获得对数据、定制和维修的完全控制权。它突显了用通用微控制器改造老旧工业和商业设备的更广泛机遇，挑战了那些专有系统价格相对于实际技术复杂度仍然高得离谱的细分行业中的供应商锁定问题。 架构采用星型拓扑 ESPNow 网状网络中的 ESP32 节点，每个节点通过 UART 连接到树莓派的网关节点发送传感器事件并接受命令，RS485 作为嘈杂射频环境下的有线回退方案。保龄球机器本身已有 70 年历史且完全机械化，这意味着昂贵的专有系统本质上只是为每条球道驱动一个继电器来触发机器，传感器包括光耦、红外对射传感器和继电器，每个节点运行略有不同的固件。

hackernews · section33 · 7月19日 14:41

**背景**: 保龄球计分系统计算球速和轨迹，执行基于摄像头的球瓶检测，运行犯规检测，管理动画，并控制置瓶机和回球装置。现代系统使用高架摄像头检测站立的球瓶并发送计分信息，取代了旧式集成在置瓶机机构中的机械传感器。ESP32 是一种低成本微控制器，内置 Wi-Fi 和蓝牙功能，广泛应用于物联网和嵌入式系统项目，使其非常适合需要大规模无线连接和传感器接口的改造应用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Pinsetter">Pinsetter - Wikipedia</a></li>
<li><a href="https://www.digikey.com/es/maker/blogs/2024/a-guide-for-the-esp32-microcontroller-series">A Guide for the ESP 32 Microcontroller Series</a></li>
<li><a href="https://www.flybowling.com/the-bowling-scoring-system-cost-guide.html">The Bowling Scoring System Cost Guide</a></li>

</ul>
</details>

**社区讨论**: 社区反响非常积极，评论者称其为典型的 Hacker News 帖子，并指出用现代嵌入式技术改造旧机械系统的广泛适用性。多位评论者分享了相关项目——包括另一位拥有基于 1970 年代 Intel D8749H 系统的保龄球中心老板，以及有人改造旧机床——还有人提出了令人兴奋的功能扩展建议，如 LED 追逐效果、DMX 灯光秀和非接触式支付自助终端功能。

**标签**: `#ESP32`, `#embedded systems`, `#hardware`, `#retrofitting`, `#reverse engineering`

---
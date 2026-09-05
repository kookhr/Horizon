---
layout: default
title: "Horizon Summary: 2026-09-05 (ZH)"
date: 2026-09-05
lang: zh
---

> 从 28 条内容中筛选出 1 条重要资讯。

---

1. [英伟达发布 PAIR 软件，闲置家用电脑可组本地 AI 集群](#item-1) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [英伟达发布 PAIR 软件，闲置家用电脑可组本地 AI 集群](https://www.techspot.com/news/113742-nvidia-pair-software-turns-idle-home-computers-local.html) ⭐️ 8.0/10

英伟达发布了免费开源的 PAIR（Personal AI Router）测试版软件，可将配备 GeForce RTX 显卡、DGX Spark 和 Mac 的闲置家用电脑连接成一个统一的本地 AI 集群，无需专用线缆。该软件支持 Ollama 和 LM Studio 等主流推理后端，几分钟内即可在现有家庭网络上完成部署。 PAIR 通过让普通家庭将约 165 teraFLOPS 的闲置算力聚合为隐私保护的本地集群，无需专门基础设施即可实现分布式 AI 推理，具有普惠意义。这对本地 AI 生态意义重大，因为它降低了在本地运行大模型的门槛，数据完全保留在用户网络内，同时最大化利用了用户已有的硬件资源。 PAIR 目前处于测试阶段，可在同一局域网内已有的设备间路由推理任务，无需专用线缆。它与 Ollama 和 LM Studio 作为推理后端集成，两者均基于 llama.cpp 引擎，所有数据和查询都保留在本地网络内。

telegram · zaihuapd · 9月5日 02:55

**背景**: 随着 Ollama 和 LM Studio 等工具的普及，本地 AI 推理发展迅速，这些工具允许用户基于 llama.cpp 引擎在消费级硬件上运行大语言模型。英伟达的 DGX Spark 是一款由 GB10 Superchip 驱动的个人 AI 超级计算机，专为桌面端 AI 工作负载设计，采用统一内存架构。PAIR 延续了这一趋势，解决了硬件碎片化问题：大多数家庭拥有多台闲置的高性能设备，但缺乏将它们组合起来用于单一 AI 任务的简便方法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nvidia.com/en-eu/ai-on-rtx/personal-ai-router/">Personal AI Router for Local Inference | NVIDIA PAIR</a></li>
<li><a href="https://www.theverge.com/ai-artificial-intelligence/989435/nvidia-pair-personal-ai-router-home-local-llm-compute-tool-rtx-macbook">Nvidia launches free tool that links idle computers into a personal AI ...</a></li>
<li><a href="https://www.nvidia.com/en-us/products/workstations/dgx-spark/">Personal AI Supercomputer Powered by Blackwell | NVIDIA DGX Spark</a></li>

</ul>
</details>

**标签**: `#nvidia`, `#distributed-computing`, `#local-ai`, `#open-source`, `#ai-inference`

---
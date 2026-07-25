---
layout: default
title: "Horizon Summary: 2026-07-25 (ZH)"
date: 2026-07-25
lang: zh
---

> 从 25 条内容中筛选出 4 条重要资讯。

---

1. [Anthropic 发布 Claude Opus 5，登顶 Artificial Analysis 排行榜](#item-1) ⭐️ 9.0/10
2. [vLLM v0.26.0：DeepSeek-V4 性能优化、Inkling 模型支持与 fp32 lm_head](#item-2) ⭐️ 8.0/10
3. [SGLang v0.5.16：DSpark 推测解码与 975B Inkling 模型支持](#item-3) ⭐️ 8.0/10
4. [SemiAnalysis：AMD 挑战 NVIDIA CUDA 护城河的战略分析](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Anthropic 发布 Claude Opus 5，登顶 Artificial Analysis 排行榜](https://simonwillison.net/2026/Jul/24/introducing-claude-opus-5/#atom-everything) ⭐️ 9.0/10

2026 年 7 月 24 日，Anthropic 发布了新模型 Claude Opus 5，该模型目前领跑 Artificial Analysis 排行榜，甚至超越了 Claude Fable 5。该模型定价为每百万输入 token 5 美元、每百万输出 token 25 美元，与 Opus 4.8 定价持平，并提供约 2.5 倍速度的"快速模式"，费用为标准模式的两倍。 Claude Opus 5 以仅相当于 Anthropic 最强模型 Fable 5 一半的价格提供了接近前沿水平的智能能力，使顶级 AI 能力更加普惠于开发者和企业。其主动的 agentic 行为——例如自主编写计算机视觉流水线来完成任务——标志着 AI 自主性和问题解决能力的重大飞跃。 Opus 5 在网络安全能力方面显著提升，在发现漏洞上接近 Mythos 5 的水平，但 Anthropic 刻意未对其进行漏洞利用方面的训练，使其在该领域仍落后于 Mythos 5。Anthropic 已发布专门的提示指南和新的上下文工程博客文章，帮助开发者针对 Claude 5 代模型进行优化。

rss · Simon Willison · 7月24日 23:48

**背景**: Anthropic 的 Claude 模型家族包含多个层级，其中 Mythos/Fable 系列代表最强大的模型，而 Opus 系列则在能力和成本之间提供平衡。Claude Fable 5 和受限访问的 Claude Mythos 5 于 2026 年 6 月发布，其中 Mythos 5 以其高级网络安全能力著称。Artificial Analysis 排行榜是一个被广泛引用的基准测试，对来自 OpenAI、Anthropic 和 Google 等提供商的大语言模型在各类任务上进行比较。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://artificialanalysis.ai/leaderboards/models">LLM Leaderboard - Comparison of AI models from OpenAI, Anthropic...</a></li>
<li><a href="https://apidog.com/blog/claude-opus-5-pricing/">Claude Opus 5 Pricing: The Full Cost Breakdown (2026)</a></li>
<li><a href="https://en.wikipedia.org/wiki/Claude_Fable_5">Claude Fable 5</a></li>

</ul>
</details>

**标签**: `#AI`, `#LLM`, `#Anthropic`, `#Claude`, `#Release`

---

<a id="item-2"></a>
## [vLLM v0.26.0：DeepSeek-V4 性能优化、Inkling 模型支持与 fp32 lm_head](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 8.0/10

vLLM v0.26.0 发布，包含来自 212 位贡献者的 411 次提交，引入了对 Inkling 模型家族的全面支持，以及在 NVIDIA、AMD 和 Intel 硬件上对 DeepSeek-V4 的广泛性能优化。该版本还通过 `head_dtype` 添加了 fp32 `lm_head` 以提高生成准确率，支持按 KV 缓存组灵活选择注意力后端，并大幅完善了 KV 卸载和分层二级存储功能。 作为使用最广泛的开源 LLM 推理引擎之一，vLLM 对 DeepSeek-V4 的多厂商性能优化直接影响整个 AI 行业的生产部署成本和吞吐量。Inkling 模型家族（一个拥有 975B 总参数和 41B 活跃参数的多模态 MoE 模型）的加入，以及成熟的 KV 卸载和投机解码支持，标志着 vLLM 持续推进对前沿规模模型的高效、硬件无关的推理服务。 DeepSeek-V4 优化包括专用路由内核（端到端 TPOT 提升 2.94%）、`fused_topk_bias`（内核加速 1.5-2 倍），以及现已扩展至 AMD 和 XPU 平台的 DSpark 投机解码。Inkling 支持栈包括分段 CUDA 图支持、Hopper FA4 相对注意力、MTP=1 投机解码、LoRA 和标准 ModelOpt NVFP4 量化。fp32 `lm_head` 功能也已扩展至 LoRA 路径，并获得了 ROCm `torch.mm` 快速路径。

github · khluu · 7月25日 10:38

**背景**: vLLM 是一个面向大语言模型的高吞吐量和内存高效推理引擎，在生产 AI 基础设施中被广泛采用。DeepSeek-V4 是 DeepSeek 的最新一代模型，DSpark 是其投机解码框架，使用半自回归草稿模型并行预测多个 token，在无需重新训练的情况下实现高达 85% 的生成加速。NVFP4 是 NVIDIA 开发的 4 位浮点量化格式，可显著减少模型内存占用同时保持精度。KV 卸载是指将键值缓存张量移至 CPU 内存或二级存储，以服务超出 GPU 内存容量的模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thinkingmachines.ai/news/introducing-inkling/">Inkling : Our Open-Weights Model - Thinking Machines Lab</a></li>
<li><a href="https://www.techtimes.com/articles/319236/20260628/deepseek-releases-dspark-speculative-decoding-makes-v4-85-percent-faster.htm">DeepSeek Releases DSpark: Speculative Decoding Makes V4 Up to 85 Percent Faster</a></li>
<li><a href="https://arxiv.org/abs/2607.05147">[2607.05147] DSpark: Confidence-Scheduled Speculative Decoding with Semi-Autoregressive Generation</a></li>

</ul>
</details>

**标签**: `#vllm`, `#llm-inference`, `#deepseek`, `#gpu-optimization`, `#release`

---

<a id="item-3"></a>
## [SGLang v0.5.16：DSpark 推测解码与 975B Inkling 模型支持](https://github.com/sgl-project/sglang/releases/tag/v0.5.16) ⭐️ 8.0/10

SGLang v0.5.16 引入了 DSpark，一种置信度驱动的推测解码算法，以半自回归方式按块生成草稿，并根据草稿自身的置信度动态调整验证窗口大小，在 DeepSeek-V4-Pro 上达到 383.7 tok/s、接受长度约 5 的性能。该版本还新增了对 Inkling 的首日支持——一个拥有 975B 参数的多模态 MoE 模型，支持 100 万 token 上下文，并混合使用滑动窗口、全注意力和 Mamba2 线性注意力架构。 DSpark 通过用自适应的置信度调度验证替代固定草稿长度，在推测解码领域实现了重要突破，在所有评估模型上均优于自回归基线（Eagle3）和并行基线（DFlash）。Inkling 的支持展示了 SGLang 在大规模场景下服务前沿混合架构模型的能力，在 Blackwell 硬件上输入吞吐量高达 71.7k tok/s，进一步巩固了其作为领先 LLM 服务框架的地位。 DSpark 通过 `--speculative-algorithm DSPARK` 和 `SGLANG_RAGGED_VERIFY_MODE=compact` 启用，块大小可通过 `--speculative-dspark-block-size` 调优。该版本还包含 ReplaySSM Ring Spec-Verify（GDN），将 Qwen3.5-35B-A3B 上的推测解码临时显存从每 GPU 11.5 GB 降至 1.8 GB（缩小 6.4 倍），并将 UnifiedRadixTree 设为 SWA、Mamba 和 DSA 模型的默认选项。值得注意的是，QServe 和 FBGEMM FP8 量化路径已被移除，NVFP4 GEMM 现在需要 FlashInfer。

github · Qiaolin-Yu · 7月25日 00:13

**背景**: 推测解码通过使用较小的草稿模型提出多个 token，然后由较大的目标模型并行验证，接受正确的 token 并拒绝错误的 token，从而加速 LLM 推理。传统方法如 Eagle3 使用固定草稿长度的自回归生成，而较新的并行方法如 DFlash 则同时生成多个 token。DSpark 统一了这些方法，将半自回归块生成与置信度调度验证相结合，动态调整验证窗口大小。Mamba2 是一种状态空间模型架构，提供线性时间序列建模作为 softmax 注意力的替代方案，而 Inkling 等混合模型则结合多种注意力机制以平衡效率和表达能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2607.05147">[2607.05147] DSpark: Confidence-Scheduled Speculative Decoding with Semi-Autoregressive Generation</a></li>
<li><a href="https://arxiv.org/html/2607.05147v1">DSpark: Confidence-Scheduled Speculative Decoding with Semi-Autoregressive Generation</a></li>
<li><a href="https://developers.redhat.com/articles/2026/02/04/accelerating-large-language-models-nvfp4-quantization">Accelerating large language models with NVFP4 quantization | Red Hat Developer</a></li>

</ul>
</details>

**标签**: `#sglang`, `#speculative-decoding`, `#llm-serving`, `#multimodal`, `#mamba`

---

<a id="item-4"></a>
## [SemiAnalysis：AMD 挑战 NVIDIA CUDA 护城河的战略分析](https://newsletter.semianalysis.com/p/can-amd-break-the-cuda-moat-amd-advancing) ⭐️ 8.0/10

SemiAnalysis 发布了一份关于 AMD 在 Advancing AI 2026 活动上的战略深度分析，涵盖了用于软件优化的代理式内核生成、MI455X 量产爬坡挑战，以及高达 105%股权回扣折扣的激进定价策略。该分析突显了 AMD 通过软件质量提升、Helios 机架级硬件扩展和金融工程等多管齐下的方式来挑战 NVIDIA 的 CUDA 生态系统主导地位。 NVIDIA 的 CUDA 软件生态系统一直是阻止 AMD 等竞争对手在数据中心 AI 市场获得有意义市场份额的最大障碍，尽管其硬件产品具有竞争力。AMD 将代理式内核生成工具与激进财务激励相结合，代表了迄今为止最严肃的协调性尝试，旨在侵蚀这一护城河，对整个 AI 基础设施格局和云服务商采购策略具有深远影响。 MI455X 基于 AMD 的 CDNA 5 架构，采用 TSMC 的 2nm 和 3nm 工艺制造，拥有 3200 亿个晶体管，为 Helios AI 机架系统提供动力。SemiAnalysis 报告称 AMD 内部开发集群一直不稳定，MI455X 的量产爬坡面临重大困难，尽管定价和软件策略激进，但交付时间表仍存在疑问。

rss · Semianalysis · 7月25日 00:33

**背景**: CUDA 是 NVIDIA 的专有并行计算平台，已成为 GPU 加速 AI 工作负载的事实标准，凭借十余年的优化库、框架和开发者心智份额构建了深厚的软件生态护城河。AMD 竞争性的 ROCm 软件栈在兼容性和性能方面历来落后，使得 AMD GPU 难以在 AI 训练和推理中直接替代 NVIDIA 硬件。代理式内核生成是指利用 AI 代理自动编写和优化 GPU 内核代码，通过自动化传统上由专家手动驱动的过程来加速 AMD 软件生态系统的发展。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://newsletter.semianalysis.com/p/can-amd-break-the-cuda-moat-amd-advancing">Can AMD break the CUDA Moat? AMD Advancing AI 2026</a></li>
<li><a href="https://www.remio.ai/post/amd-semianalysis-amds-cuda-challenge-runs-into-a-rack-scale-reality-check">AMD SemiAnalysis: AMD ’s CUDA Challenge Runs Into a Rack-Scale...</a></li>
<li><a href="https://wccftech.com/amd-instinct-mi455x-gpu-320b-behemoth-tackle-nvidia-rubin-with-432gb-hbm4-40-pflops-ai/">AMD Unleashes Instinct MI 455 X GPU , A 320 Billion Transistor...</a></li>

</ul>
</details>

**标签**: `#AMD`, `#CUDA`, `#AI Hardware`, `#GPU Competition`, `#SemiAnalysis`

---
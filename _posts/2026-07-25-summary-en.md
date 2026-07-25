---
layout: default
title: "Horizon Summary: 2026-07-25 (EN)"
date: 2026-07-25
lang: en
---

> From 25 items, 4 important content pieces were selected

---

1. [Anthropic Launches Claude Opus 5, Topping Artificial Analysis Leaderboard](#item-1) ⭐️ 9.0/10
2. [vLLM v0.26.0: DeepSeek-V4 Optimizations, Inkling Support, and fp32 lm_head](#item-2) ⭐️ 8.0/10
3. [SGLang v0.5.16: DSpark Speculative Decoding and 975B Inkling Support](#item-3) ⭐️ 8.0/10
4. [SemiAnalysis: AMD's Strategy to Break NVIDIA's CUDA Moat](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Anthropic Launches Claude Opus 5, Topping Artificial Analysis Leaderboard](https://simonwillison.net/2026/Jul/24/introducing-claude-opus-5/#atom-everything) ⭐️ 9.0/10

On July 24, 2026, Anthropic released Claude Opus 5, a new frontier model that currently leads the Artificial Analysis leaderboard, surpassing even Claude Fable 5. The model is priced at $5 per million input tokens and $25 per million output tokens, matching Opus 4.8's pricing, and offers a "fast mode" at double the cost for approximately 2.5x the speed. Claude Opus 5 delivers near-frontier intelligence at half the price of Anthropic's most powerful Fable 5 model, making top-tier AI capabilities more accessible to developers and enterprises. Its proactive agentic behavior, demonstrated by autonomously writing computer vision pipelines to solve tasks, signals a significant leap in AI autonomy and problem-solving capability. Opus 5 shows markedly improved cybersecurity capabilities, nearly matching Mythos 5 in finding vulnerabilities, though Anthropic deliberately avoided training it on exploitation tasks, keeping it behind Mythos 5 in that regard. Anthropic has published a dedicated prompting guide and a new context engineering blog post to help developers optimize for the Claude 5 generation of models.

rss · Simon Willison · Jul 24, 23:48

**Background**: Anthropic's Claude model family includes multiple tiers, with the Mythos/Fable series representing the most powerful models and the Opus series offering a balance of capability and cost. Claude Fable 5 and the restricted-access Claude Mythos 5 were released in June 2026, with Mythos 5 noted for its advanced cybersecurity capabilities. The Artificial Analysis leaderboard is a widely referenced benchmark that compares large language models from providers like OpenAI, Anthropic, and Google across various tasks.

<details><summary>References</summary>
<ul>
<li><a href="https://artificialanalysis.ai/leaderboards/models">LLM Leaderboard - Comparison of AI models from OpenAI, Anthropic...</a></li>
<li><a href="https://apidog.com/blog/claude-opus-5-pricing/">Claude Opus 5 Pricing: The Full Cost Breakdown (2026)</a></li>
<li><a href="https://en.wikipedia.org/wiki/Claude_Fable_5">Claude Fable 5</a></li>

</ul>
</details>

**Tags**: `#AI`, `#LLM`, `#Anthropic`, `#Claude`, `#Release`

---

<a id="item-2"></a>
## [vLLM v0.26.0: DeepSeek-V4 Optimizations, Inkling Support, and fp32 lm_head](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 8.0/10

vLLM v0.26.0 was released with 411 commits from 212 contributors, introducing full-stack support for the Inkling model family and extensive DeepSeek-V4 performance optimizations across NVIDIA, AMD, and Intel hardware. The release also adds fp32 `lm_head` via `head_dtype` for improved generation accuracy, flexible per-KV-cache-group attention backend selection, and substantial maturation of KV offloading and tiered secondary storage. As one of the most widely used open-source LLM inference engines, vLLM's multi-vendor performance optimizations for DeepSeek-V4 directly impact production deployment costs and throughput across the AI industry. The addition of the Inkling model family — a multimodal MoE model with 975B total and 41B active parameters — alongside matured KV offloading and speculative decoding support signals vLLM's continued push toward efficient, hardware-agnostic serving of frontier-scale models. DeepSeek-V4 optimizations include a specialized routing kernel (2.94% E2E TPOT improvement), `fused_topk_bias` (1.5–2x kernel speedup), and DSpark speculative decoding now extended to AMD and XPU platforms. The Inkling support stack includes piecewise CUDA graph support, Hopper FA4 relative attention, MTP=1 speculative decoding, LoRA, and standard ModelOpt NVFP4 quantization. The fp32 `lm_head` feature was also extended to the LoRA path and given a ROCm `torch.mm` fast path.

github · khluu · Jul 25, 10:38

**Background**: vLLM is a high-throughput and memory-efficient inference engine for large language models, widely adopted in production AI infrastructure. DeepSeek-V4 is a recent model generation from DeepSeek, and DSpark is its speculative decoding framework that uses a semi-autoregressive draft model to predict multiple tokens in parallel, achieving up to 85% faster generation without retraining. NVFP4 is a NVIDIA-developed 4-bit floating-point quantization format that reduces model memory footprint significantly while maintaining accuracy. KV offloading refers to moving key-value cache tensors to CPU memory or secondary storage to serve models that exceed GPU memory capacity.

<details><summary>References</summary>
<ul>
<li><a href="https://thinkingmachines.ai/news/introducing-inkling/">Inkling : Our Open-Weights Model - Thinking Machines Lab</a></li>
<li><a href="https://www.techtimes.com/articles/319236/20260628/deepseek-releases-dspark-speculative-decoding-makes-v4-85-percent-faster.htm">DeepSeek Releases DSpark: Speculative Decoding Makes V4 Up to 85 Percent Faster</a></li>
<li><a href="https://arxiv.org/abs/2607.05147">[2607.05147] DSpark: Confidence-Scheduled Speculative Decoding with Semi-Autoregressive Generation</a></li>

</ul>
</details>

**Tags**: `#vllm`, `#llm-inference`, `#deepseek`, `#gpu-optimization`, `#release`

---

<a id="item-3"></a>
## [SGLang v0.5.16: DSpark Speculative Decoding and 975B Inkling Support](https://github.com/sgl-project/sglang/releases/tag/v0.5.16) ⭐️ 8.0/10

SGLang v0.5.16 introduces DSpark, a confidence-driven speculative decoding algorithm that drafts semi-autoregressively in blocks and dynamically sizes verification windows based on draft confidence, achieving 383.7 tok/s at accept length ~5 on DeepSeek-V4-Pro. The release also adds day-0 support for Inkling, a 975B-parameter multimodal MoE model with 1M-token context that mixes sliding-window, full, and Mamba2 linear attention architectures. DSpark represents a meaningful advance in speculative decoding by replacing fixed draft lengths with adaptive, confidence-scheduled verification, which consistently outperforms both autoregressive (Eagle3) and parallel (DFlash) baselines across evaluated models. Inkling support demonstrates SGLang's ability to serve cutting-edge hybrid-architecture models at massive scale, reaching up to 71.7k tok/s input throughput on Blackwell hardware, solidifying its position as a leading LLM serving framework. DSpark is enabled via `--speculative-algorithm DSPARK` with `SGLANG_RAGGED_VERIFY_MODE=compact`, and block size is tunable through `--speculative-dspark-block-size`. The release also includes ReplaySSM Ring Spec-Verify (GDN) which reduces speculative scratch memory from 11.5 GB to 1.8 GB per GPU (6.4x smaller) on Qwen3.5-35B-A3B, and makes UnifiedRadixTree the default for SWA, Mamba, and DSA models. Notably, QServe and FBGEMM FP8 quantization paths have been removed, and NVFP4 GEMM now requires FlashInfer.

github · Qiaolin-Yu · Jul 25, 00:13

**Background**: Speculative decoding accelerates LLM inference by using a smaller draft model to propose multiple tokens that are then verified in parallel by the larger target model, accepting correct tokens and rejecting incorrect ones. Traditional approaches like Eagle3 use autoregressive drafting with fixed draft lengths, while newer parallel methods like DFlash generate tokens simultaneously. DSpark unifies these approaches by using semi-autoregressive block drafting combined with confidence-scheduled verification that adapts the verify window size dynamically. Mamba2 is a state space model architecture that offers linear-time sequence modeling as an alternative to softmax attention, and hybrid models like Inkling combine multiple attention mechanisms to balance efficiency and expressiveness.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2607.05147">[2607.05147] DSpark: Confidence-Scheduled Speculative Decoding with Semi-Autoregressive Generation</a></li>
<li><a href="https://arxiv.org/html/2607.05147v1">DSpark: Confidence-Scheduled Speculative Decoding with Semi-Autoregressive Generation</a></li>
<li><a href="https://developers.redhat.com/articles/2026/02/04/accelerating-large-language-models-nvfp4-quantization">Accelerating large language models with NVFP4 quantization | Red Hat Developer</a></li>

</ul>
</details>

**Tags**: `#sglang`, `#speculative-decoding`, `#llm-serving`, `#multimodal`, `#mamba`

---

<a id="item-4"></a>
## [SemiAnalysis: AMD's Strategy to Break NVIDIA's CUDA Moat](https://newsletter.semianalysis.com/p/can-amd-break-the-cuda-moat-amd-advancing) ⭐️ 8.0/10

SemiAnalysis published a detailed breakdown of AMD's strategy at its Advancing AI 2026 event, covering agentic kernel generation for software optimization, MI455X production ramp challenges, and aggressive pricing tactics including up to 105% equity rebate discounts. The analysis highlights AMD's multi-pronged approach to challenging NVIDIA's CUDA ecosystem dominance through software quality improvements, hardware scale-up with the Helios rack, and finance engineering. NVIDIA's CUDA software ecosystem has been the single biggest barrier preventing competitors like AMD from gaining meaningful datacenter AI market share, despite competitive hardware offerings. AMD's combination of agentic kernel generation tools and aggressive financial incentives represents the most serious coordinated attempt yet to erode that moat, with implications for the entire AI infrastructure landscape and cloud provider procurement strategies. The MI455X is based on AMD's CDNA 5 architecture with 320 billion transistors using TSMC's 2nm and 3nm processes, powering the Helios AI rack system. SemiAnalysis reports that AMD's internal development clusters have been unstable, and the MI455X production ramp has faced significant difficulties, raising questions about delivery timelines despite the aggressive pricing and software strategy.

rss · Semianalysis · Jul 25, 00:33

**Background**: CUDA is NVIDIA's proprietary parallel computing platform that has become the de facto standard for GPU-accelerated AI workloads, creating a deep software ecosystem moat with over a decade of optimized libraries, frameworks, and developer mindshare. AMD's competing ROCm software stack has historically lagged in compatibility and performance, making it difficult for AMD GPUs to be drop-in replacements for NVIDIA hardware in AI training and inference. Agentic kernel generation refers to using AI agents to automatically write and optimize GPU kernel code, potentially accelerating AMD's software ecosystem development by automating what has traditionally been a manual, expert-driven process.

<details><summary>References</summary>
<ul>
<li><a href="https://newsletter.semianalysis.com/p/can-amd-break-the-cuda-moat-amd-advancing">Can AMD break the CUDA Moat? AMD Advancing AI 2026</a></li>
<li><a href="https://www.remio.ai/post/amd-semianalysis-amds-cuda-challenge-runs-into-a-rack-scale-reality-check">AMD SemiAnalysis: AMD ’s CUDA Challenge Runs Into a Rack-Scale...</a></li>
<li><a href="https://wccftech.com/amd-instinct-mi455x-gpu-320b-behemoth-tackle-nvidia-rubin-with-432gb-hbm4-40-pflops-ai/">AMD Unleashes Instinct MI 455 X GPU , A 320 Billion Transistor...</a></li>

</ul>
</details>

**Tags**: `#AMD`, `#CUDA`, `#AI Hardware`, `#GPU Competition`, `#SemiAnalysis`

---
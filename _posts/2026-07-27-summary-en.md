---
layout: default
title: "Horizon Summary: 2026-07-27 (EN)"
date: 2026-07-27
lang: en
---

> From 30 items, 4 important content pieces were selected

---

1. [Fastjson2 Discloses Unpatched Remote Code Execution Vulnerability](#item-1) ⭐️ 9.0/10
2. [vLLM v0.26.0 Released with Inkling Support and DeepSeek-V4 Optimizations](#item-2) ⭐️ 8.0/10
3. [Bun's Rust Rewrite Ships in Claude Code, v1.4 Imminent](#item-3) ⭐️ 8.0/10
4. [China Begins Mass Producing Homegrown DUV Lithography Machines, Targeting ~5 Units This Year](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Fastjson2 Discloses Unpatched Remote Code Execution Vulnerability](https://mp.weixin.qq.com/s/LJaul1jNjK9pXRAkoUiMEA) ⭐️ 9.0/10

On July 27, Chaitin Tech disclosed a remote code execution (RCE) vulnerability in Fastjson2 that affects all versions up to and including 2.0.62, which covers every currently released version. The project maintainers have confirmed the issue, but no official patch has been released yet, and the fix PR #7695 was closed without being merged into the main branch. Fastjson2 is a widely-used Java JSON library in enterprise and cloud-native applications, and an unpatched RCE vulnerability means attackers can potentially execute arbitrary code on affected servers via malicious JSON payloads. This is the second critical vulnerability in the fastjson ecosystem this month, compounding risk for organizations that rely on these libraries and highlighting ongoing security concerns around AutoType mechanisms. The vulnerability allows attackers to bypass AutoType type validation through crafted JSON data and achieve remote code execution. While full exploit details and proof-of-concept code have not been publicly released, the recommended mitigation is to completely disable AutoType until a patched version is available. Fastjson2 disables AutoType by default, but applications that explicitly enable it or use permissive autoType filters are at risk.

telegram · zaihuapd · Jul 27, 10:31

**Background**: Fastjson2 is Alibaba's high-performance Java JSON library and the successor to the original fastjson (fastjson1), which has a long history of deserialization vulnerabilities. AutoType is a feature that allows JSON data to specify the Java class to deserialize into via a @type field, enabling polymorphic deserialization but also creating a well-known attack surface for RCE exploits. Fastjson2 was designed to be more secure by default — AutoType is disabled, there is no hardcoded whitelist, and SafeMode is supported — but this new vulnerability demonstrates that the AutoType bypass risk persists even in the redesigned version.

<details><summary>References</summary>
<ul>
<li><a href="https://alibaba.github.io/fastjson2/autotype_cn.html">FASTJSON 2 Autotype机制介绍 | fastjson2</a></li>
<li><a href="https://github.com/alibaba/fastjson2">GitHub - alibaba/fastjson2: 🚄 FASTJSON2 is a Java JSON library with excellent performance.</a></li>
<li><a href="https://latesthackingnews.com/2026/07/26/fastjson-rce-vulnerability-how-to-check/">How the Fastjson RCE Vulnerability Actually Works, and How to...</a></li>

</ul>
</details>

**Tags**: `#security`, `#java`, `#vulnerability`, `#fastjson`, `#rce`

---

<a id="item-2"></a>
## [vLLM v0.26.0 Released with Inkling Support and DeepSeek-V4 Optimizations](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 8.0/10

vLLM v0.26.0 is a major release with 411 commits from 212 contributors, featuring full support for the new Inkling model family (including CUDA graph, Hopper FA4 relative attention, MTP=1 speculative decoding, LoRA, and NVFP4 quantization), DeepSeek-V4 performance optimizations across NVIDIA, AMD ROCm, and Intel XPU vendors, fp32 lm_head support via head_dtype, and flexible per-KV-cache-group attention backend selection. vLLM is one of the most widely used open-source LLM inference engines, and this release significantly broadens hardware vendor support and model compatibility while pushing performance boundaries for DeepSeek-V4 models. The multi-vendor optimizations (NVIDIA, AMD, Intel) and matured KV offloading with tiered storage signal vLLM's push toward production-grade, heterogeneous infrastructure deployment. Notable technical highlights include a specialized DeepSeek-V4 routing kernel achieving 2.94% E2E TPOT improvement, fused_topk_bias delivering 1.5–2x kernel speedup, DSpark speculative decoding support on both AMD and XPU, and NVFP4 quantization which benchmarks show delivers roughly 2.6–2.86x decode speedup over BF16. The release also migrates to Transformers 5.13.0 and adds a Rust frontend with multimodal video and audio support.

github · khluu · Jul 27, 01:06

**Background**: vLLM is a high-throughput LLM inference and serving engine that uses PagedAttention for efficient KV-cache management. Speculative decoding (like DSpark) is a technique where a smaller draft model generates candidate tokens that are verified by the larger model in parallel, achieving significant speedups without retraining. NVFP4 is a 4-bit floating-point quantization format designed for NVIDIA Hopper GPUs that reduces memory footprint while maintaining accuracy. FlashAttention (FA) is an IO-aware exact attention algorithm that minimizes memory reads/writes, with FA3/FA4 optimized for Hopper architecture features like TMA and WGMMA.

<details><summary>References</summary>
<ul>
<li><a href="https://www.techtimes.com/articles/319236/20260628/deepseek-releases-dspark-speculative-decoding-makes-v4-85-percent-faster.htm">DeepSeek Releases DSpark: Speculative Decoding Makes V4 Up to 85 Percent Faster</a></li>
<li><a href="https://kie.ai/blog/qwen-3-6-27b-deep-dive-benchmarks-quantization">Qwen 3.6 27B Benchmark Deep Dive: The Measured Numbers</a></li>
<li><a href="https://arxiv.org/abs/2607.05147">[2607.05147] DSpark: Confidence-Scheduled Speculative Decoding with Semi-Autoregressive Generation</a></li>

</ul>
</details>

**Tags**: `#vllm`, `#llm-inference`, `#release`, `#performance-optimization`, `#quantization`

---

<a id="item-3"></a>
## [Bun's Rust Rewrite Ships in Claude Code, v1.4 Imminent](https://lockwood.dev/ai/2026/07/27/how-is-the-bun-rewrite-in-rust-going.html) ⭐️ 8.0/10

Bun's ongoing rewrite from Zig to Rust has already shipped in Claude Code over a month ago with minimal user notice, and the Bun v1.4 release is expected around the following Tuesday, pending the merge of compatibility-improving PRs. Developer Jarred confirmed the rewrite is going well overall, though the promised number of newly passing Node.js tests has not yet been met. Bun is a widely-used JavaScript runtime and toolkit, and its migration to Rust signals a major language shift for a production-grade project, with implications for performance, maintainability, and the broader JS ecosystem. The fact that it shipped silently in Claude Code demonstrates the rewrite's stability, while the LLM-assisted approach sparks debate about the viability of large-scale automated code translation. The v1.4 release is delayed until a specific number of newly passing Node.js compatibility tests is achieved, with the relevant PRs submitted but not yet merged. A community member also pointed to an alternative project called 'Buz' that claims sub-second build times by fixing the original Zig codebase rather than rewriting, suggesting some issues motivating the rewrite may have been self-inflicted.

hackernews · tomlockwood · Jul 27, 11:12 · [Discussion](https://news.ycombinator.com/item?id=49067854)

**Background**: Bun is an all-in-one JavaScript runtime, bundler, transpiler, and npm client designed as a drop-in replacement for Node.js, originally written in Zig and now being rewritten in Rust. Zig is a systems programming language with manual memory management, while Rust offers memory safety guarantees through its ownership model. Claude Code is Anthropic's agentic coding tool that understands codebases and assists with development tasks, and it served as an early production deployment for the Rust-based Bun runtime.

<details><summary>References</summary>
<ul>
<li><a href="https://bun.sh/">Bun — A fast all-in-one JavaScript runtime</a></li>
<li><a href="https://github.com/oven-sh/bun">GitHub - oven-sh/ bun : Incredibly fast JavaScript runtime , bundler...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Zig_(programming_language)">Zig (programming language)</a></li>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI Coding Agent, Terminal, IDE</a></li>

</ul>
</details>

**Discussion**: Jarred provided a firsthand update confirming the Rust rewrite shipped quietly in Claude Code and v1.4 is delayed pending test compatibility goals. SquareWheel cautioned against judging progress by commit count, noting developers need time to ramp up in a new codebase. benjiro29 questioned whether fast LLM-generated rewrites produce maintainable software, while bendmorris highlighted the 'Buz' project claiming the original Zig issues were fixable without a full rewrite.

**Tags**: `#bun`, `#rust`, `#javascript-runtime`, `#rewrite`, `#llm-assisted-development`

---

<a id="item-4"></a>
## [China Begins Mass Producing Homegrown DUV Lithography Machines, Targeting ~5 Units This Year](https://www.theinformation.com/articles/china-starts-mass-producing-homegrown-duv-chipmaking-tools-advance-local-chip-industry) ⭐️ 8.0/10

A state-owned enterprise in Shanghai has begun mass-producing China's first homegrown immersion DUV lithography machines, targeting approximately 5 units in 2024 and around 20 units by 2027. The machines will be delivered to domestic chipmakers including SMIC and Hua Hong Semiconductor, though they still lag behind ASML's equipment in performance and reliability. This marks a significant milestone in China's push toward semiconductor equipment self-sufficiency amid Western export controls, and the news already triggered a 6% drop in ASML's stock price. While the domestic machines cannot yet directly threaten ASML, increasing production volumes could gradually erode ASML's position in the Chinese market, especially if Western export restrictions tighten further. The domestic DUV equipment primarily uses Chinese-made components, though some critical parts still come from Japan, and local supply chain delays have already affected production progress this year. Chipmakers will need months or longer to test the equipment's precision and compatibility before integrating it into mass production lines.

telegram · zaihuapd · Jul 27, 14:10

**Background**: DUV (deep ultraviolet) lithography is a photolithography process that uses light in the deep ultraviolet spectrum (typically 193nm ArF lasers) to transfer circuit patterns onto silicon wafers, enabling fabrication of chips down to 7nm nodes. Immersion DUV lithography enhances resolution by introducing a liquid medium (usually water) between the lens and the wafer, and it remains the workhorse technology for mainstream chip manufacturing. ASML is the dominant global supplier of DUV lithography systems, and China has been striving to develop domestic alternatives amid U.S.-led export restrictions on advanced semiconductor equipment.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Immersion_lithography">Immersion lithography - Wikipedia</a></li>
<li><a href="https://eureka.patsnap.com/article/duv-lithography-explained-how-193nm-arf-lasers-enable-7nm-nodes">DUV Lithography Explained: How 193nm ArF Lasers Enable 7nm...</a></li>
<li><a href="https://www.asml.com/en/products/duv-lithography-systems">See ASML's DUV lithography systems</a></li>

</ul>
</details>

**Tags**: `#semiconductors`, `#lithography`, `#China`, `#ASML`, `#chip-manufacturing`

---
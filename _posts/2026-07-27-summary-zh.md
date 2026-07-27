---
layout: default
title: "Horizon Summary: 2026-07-27 (ZH)"
date: 2026-07-27
lang: zh
---

> 从 30 条内容中筛选出 4 条重要资讯。

---

1. [Fastjson2 曝远程代码执行漏洞，现有版本尚未修复](#item-1) ⭐️ 9.0/10
2. [vLLM v0.26.0 发布：新增 Inkling 模型支持与 DeepSeek-V4 性能优化](#item-2) ⭐️ 8.0/10
3. [Bun 的 Rust 重写已随 Claude Code 发布，v1.4 即将推出](#item-3) ⭐️ 8.0/10
4. [中国开始量产国产 DUV 光刻机，今年目标生产约 5 台](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Fastjson2 曝远程代码执行漏洞，现有版本尚未修复](https://mp.weixin.qq.com/s/LJaul1jNjK9pXRAkoUiMEA) ⭐️ 9.0/10

7 月 27 日，长亭科技披露了 Fastjson2 的远程代码执行（RCE）漏洞，影响 2.0.62 及以前的所有版本，即目前全部已发布版本。项目维护者已确认该安全问题，但修复 PR #7695 已被关闭且未合入主分支，目前尚无正式补丁。 Fastjson2 是企业级和云原生应用中广泛使用的 Java JSON 库，未修复的 RCE 漏洞意味着攻击者可通过恶意 JSON 数据在受影响服务器上执行任意代码。这是本月 fastjson 生态系统中的第二个严重漏洞，对依赖该库的组织构成了叠加风险，也再次凸显了 AutoType 机制的安全隐患。 该漏洞允许攻击者通过精心构造的 JSON 数据绕过 AutoType 类型校验并实现远程代码执行。虽然完整漏洞细节和利用代码尚未公开，但在修复版本发布前，建议彻底禁用 AutoType。Fastjson2 默认禁用 AutoType，但显式启用或使用宽松 autoType 过滤器的应用仍存在风险。

telegram · zaihuapd · 7月27日 10:31

**背景**: Fastjson2 是阿里巴巴的高性能 Java JSON 库，也是原版 fastjson（fastjson1）的继任者，而 fastjson1 有着漫长的反序列化漏洞历史。AutoType 是一项允许 JSON 数据通过 @type 字段指定反序列化目标 Java 类的特性，支持多态反序列化，但同时也构成了众所周知的 RCE 攻击面。Fastjson2 在设计上更注重默认安全性——AutoType 默认禁用、无硬编码白名单、支持 SafeMode——但此次新漏洞表明，即使经过重新设计，AutoType 绕过风险依然存在。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://alibaba.github.io/fastjson2/autotype_cn.html">FASTJSON 2 Autotype机制介绍 | fastjson2</a></li>
<li><a href="https://github.com/alibaba/fastjson2">GitHub - alibaba/fastjson2: 🚄 FASTJSON2 is a Java JSON library with excellent performance.</a></li>
<li><a href="https://latesthackingnews.com/2026/07/26/fastjson-rce-vulnerability-how-to-check/">How the Fastjson RCE Vulnerability Actually Works, and How to...</a></li>

</ul>
</details>

**标签**: `#security`, `#java`, `#vulnerability`, `#fastjson`, `#rce`

---

<a id="item-2"></a>
## [vLLM v0.26.0 发布：新增 Inkling 模型支持与 DeepSeek-V4 性能优化](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 8.0/10

vLLM v0.26.0 是一个重大版本发布，包含来自 212 位贡献者的 411 次提交，新增了对 Inkling 模型家族的完整支持（包括 CUDA graph、Hopper FA4 相对注意力、MTP=1 推测解码、LoRA 和 NVFP4 量化），跨 NVIDIA、AMD ROCm 和 Intel XPU 多厂商的 DeepSeek-V4 性能优化，通过 head_dtype 实现的 fp32 lm_head 支持，以及灵活的按 KV cache 组选择注意力后端的功能。 vLLM 是目前最广泛使用的开源 LLM 推理引擎之一，本版本显著扩展了硬件厂商支持和模型兼容性，同时推动了 DeepSeek-V4 模型的性能边界。跨多厂商（NVIDIA、AMD、Intel）的优化以及成熟的 KV 卸载与分层存储功能，表明 vLLM 正向生产级异构基础设施部署方向迈进。 值得注意的技术亮点包括：DeepSeek-V4 专用路由内核实现 2.94% 端到端 TPOT 提升，fused_topk_bias 带来 1.5–2 倍内核加速，在 AMD 和 XPU 上均支持 DSpark 推测解码，以及 NVFP4 量化在基准测试中相比 BF16 实现约 2.6–2.86 倍解码加速。本版本还迁移至 Transformers 5.13.0，并在 Rust 前端中新增多模态视频和音频支持。

github · khluu · 7月27日 01:06

**背景**: vLLM 是一个高吞吐量的 LLM 推理与服务引擎，采用 PagedAttention 技术实现高效的 KV cache 管理。推测解码（如 DSpark）是一种技术，由较小的草稿模型生成候选 token，再由大模型并行验证，无需重新训练即可实现显著加速。NVFP4 是一种面向 NVIDIA Hopper GPU 设计的 4 位浮点量化格式，可在保持精度的同时减少内存占用。FlashAttention（FA）是一种 IO 感知的精确注意力算法，通过最小化内存读写来提升效率，FA3/FA4 针对 Hopper 架构的 TMA 和 WGMMA 等特性进行了优化。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.techtimes.com/articles/319236/20260628/deepseek-releases-dspark-speculative-decoding-makes-v4-85-percent-faster.htm">DeepSeek Releases DSpark: Speculative Decoding Makes V4 Up to 85 Percent Faster</a></li>
<li><a href="https://kie.ai/blog/qwen-3-6-27b-deep-dive-benchmarks-quantization">Qwen 3.6 27B Benchmark Deep Dive: The Measured Numbers</a></li>
<li><a href="https://arxiv.org/abs/2607.05147">[2607.05147] DSpark: Confidence-Scheduled Speculative Decoding with Semi-Autoregressive Generation</a></li>

</ul>
</details>

**标签**: `#vllm`, `#llm-inference`, `#release`, `#performance-optimization`, `#quantization`

---

<a id="item-3"></a>
## [Bun 的 Rust 重写已随 Claude Code 发布，v1.4 即将推出](https://lockwood.dev/ai/2026/07/27/how-is-the-bun-rewrite-in-rust-going.html) ⭐️ 8.0/10

Bun 从 Zig 到 Rust 的重写已于一个多月前随 Claude Code 发布，几乎没有用户察觉到变化。开发者 Jarred 确认重写整体进展顺利，Bun v1.4 版本预计在下周二左右发布，但需等待兼容性改进的 PR 合并后才能兑现承诺的 Node.js 测试通过数量。 Bun 是广泛使用的 JavaScript 运行时和工具包，其迁移到 Rust 标志着一个生产级项目的重要语言转变，对性能、可维护性和整个 JS 生态系统都有深远影响。重写版本在 Claude Code 中悄然上线且未被用户察觉，说明其稳定性已达到生产水平，而 LLM 辅助重写的方式也引发了关于大规模自动化代码翻译可行性的讨论。 v1.4 版本的发布被推迟，直到达到承诺数量的 Node.js 兼容性测试通过为止，相关 PR 已提交但尚未合并。社区成员还提到了一个名为 'Buz' 的替代项目，声称通过修复原始 Zig 代码库而非重写即可实现亚秒级构建时间，暗示推动重写的部分问题可能是自身造成的。

hackernews · tomlockwood · 7月27日 11:12 · [社区讨论](https://news.ycombinator.com/item?id=49067854)

**背景**: Bun 是一个集 JavaScript 运行时、打包器、转译器和 npm 客户端于一体的工具，旨在作为 Node.js 的直接替代品，最初用 Zig 编写，现正在用 Rust 重写。Zig 是一种手动管理内存的系统编程语言，而 Rust 通过所有权模型提供内存安全保证。Claude Code 是 Anthropic 推出的智能编程工具，能够理解代码库并辅助开发任务，它成为了基于 Rust 的 Bun 运行时的早期生产部署环境。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://bun.sh/">Bun — A fast all-in-one JavaScript runtime</a></li>
<li><a href="https://github.com/oven-sh/bun">GitHub - oven-sh/ bun : Incredibly fast JavaScript runtime , bundler...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Zig_(programming_language)">Zig (programming language)</a></li>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI Coding Agent, Terminal, IDE</a></li>

</ul>
</details>

**社区讨论**: Jarred 提供了第一手更新，确认 Rust 重写已悄然在 Claude Code 中上线，v1.4 因测试兼容性目标未达成而推迟。SquareWheel 提醒不要仅凭提交数量评判进展，指出开发者需要时间适应新代码库。benjiro29 质疑 LLM 快速生成的重写是否能产出可维护的软件，而 bendmorris 则强调了 'Buz' 项目，声称原始 Zig 的问题无需全面重写即可修复。

**标签**: `#bun`, `#rust`, `#javascript-runtime`, `#rewrite`, `#llm-assisted-development`

---

<a id="item-4"></a>
## [中国开始量产国产 DUV 光刻机，今年目标生产约 5 台](https://www.theinformation.com/articles/china-starts-mass-producing-homegrown-duv-chipmaking-tools-advance-local-chip-industry) ⭐️ 8.0/10

上海一家国企已开始大规模生产中国首款自主研发的浸没式 DUV 光刻机，计划 2024 年生产约 5 台、2027 年约 20 台。该设备将交付中芯国际、华虹半导体等国内厂商，但在性能和可靠性上仍落后于 ASML。 在西方出口管制背景下，这是中国推进半导体设备自主化的重要里程碑，该消息已导致 ASML 股价一度跌超 6%。虽然国产设备短期内难以直接威胁 ASML，但产量持续增加可能逐步侵蚀其在中国市场的地位，尤其是在西方进一步收紧出口限制的情况下。 国产 DUV 设备主要使用国产零部件，但部分关键部件仍来自日本，且今年本地供应链延误已影响生产进度。芯片商需数月甚至更长时间测试设备的精度与兼容性，方能投入量产产线。

telegram · zaihuapd · 7月27日 14:10

**背景**: DUV（深紫外）光刻是一种利用深紫外光谱（通常为 193nm ArF 激光器）将电路图案转印到硅晶圆上的光刻工艺，可实现低至 7nm 节点的芯片制造。浸没式 DUV 光刻通过在透镜和晶圆之间引入液体介质（通常为水）来提高分辨率，是主流芯片制造的核心技术。ASML 是全球 DUV 光刻系统的主导供应商，中国在美国主导的先进半导体设备出口管制下一直在努力开发国产替代方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Immersion_lithography">Immersion lithography - Wikipedia</a></li>
<li><a href="https://eureka.patsnap.com/article/duv-lithography-explained-how-193nm-arf-lasers-enable-7nm-nodes">DUV Lithography Explained: How 193nm ArF Lasers Enable 7nm...</a></li>
<li><a href="https://www.asml.com/en/products/duv-lithography-systems">See ASML's DUV lithography systems</a></li>

</ul>
</details>

**标签**: `#semiconductors`, `#lithography`, `#China`, `#ASML`, `#chip-manufacturing`

---
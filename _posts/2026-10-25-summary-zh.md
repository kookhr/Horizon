---
layout: default
title: "Horizon Summary: 2026-10-25 (ZH)"
date: 2026-10-25
lang: zh
---

> 从 29 条内容中筛选出 2 条重要资讯。

---

1. [Brotli 高危漏洞 CVE-2026-111497 影响 Python 和 Node.js](#item-1) ⭐️ 9.0/10
2. [十年前的 CNN 在皮肤癌诊断中超越前沿大语言模型](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Brotli 高危漏洞 CVE-2026-111497 影响 Python 和 Node.js](https://www.aikido.dev/blog/python-packages-vulnerable-node2shell-brotli-cve-2026-111497) ⭐️ 9.0/10

谷歌 Brotli 解码器的高危漏洞 CVE-2026-111497（CVSS 4.0 评分 9.2）影响 1.0.3 至 1.2.0 版本，现已确认扩展至 Python 相关包。远程未认证攻击者可通过发送特制压缩流导致内存损坏、数据泄露、进程崩溃或可能执行任意代码。修复版本已发布：Python 的 Brotli 需升级至 1.2.1，brotlicffi 升级至 1.2.1.0；Node.js 修复版本为 22.23.4、24.22.1 或 26.12.1。 该漏洞极其关键，因为 Brotli 是一种被广泛采用的压缩库，内嵌于 Node.js、Python、Bun 和 Envoy 等多个主要生态系统的核心 HTTP 组件中。远程代码执行的可能性意味着任何处理不受信任压缩数据的服务都可能被攻破，因此整个行业需将立即修补此漏洞视为最高优先级任务。 该漏洞是在解码格式错误的 Brotli 输入时触发的越界写入问题，最初以 Node2Shell 名称披露，后被称为 HTTP2Shell。据报道，OpenAI 于今年 2 月发现了该问题，并且已在至少一个 Node.js 构建版本上演示了代码执行。

telegram · zaihuapd · 10月25日 02:42

**背景**: Brotli 是由 Google 开发的通用无损压缩算法，常用于 HTTP 内容压缩以减少网络流量的传输大小。它以 C 语言库的形式实现，并内置于许多运行时环境和服务器中，包括 Node.js 和各种 Python 包。由于 Brotli 解码器处理来自网络的输入数据，解码器中的内存安全漏洞可被远程攻击者触发，可能导致服务器端代码执行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.aikido.dev/blog/python-packages-vulnerable-node2shell-brotli-cve-2026-111497">Node2Shell Brotli vuln (CVE-2026-111497) evolves to HTTP2Shell, as...</a></li>
<li><a href="https://thehackernews.com/2026/10/brotli-decoder-flaw-behind-nodejs-rce.html">Brotli Decoder Flaw Behind Node.js RCE Also Affects Bun, Python...</a></li>
<li><a href="https://vercel.com/kb/bulletin/node-js-security-advisory">Node.js security advisory: Brotli decoder ... | Vercel Knowledge Base</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerability`, `#brotli`, `#python`, `#nodejs`

---

<a id="item-2"></a>
## [十年前的 CNN 在皮肤癌诊断中超越前沿大语言模型](https://lynchlab.net/llm-skin-cancer) ⭐️ 8.0/10

一项实验将一个经过 68,000 多张来自 ISIC Archive 的皮肤镜和临床图像微调的十年前的 Inception v3 CNN，与 GPT-4o 和 Claude 3.5 Sonnet 等前沿大语言模型在皮肤癌诊断任务上进行了比较。专用 CNN 在相同诊断任务上显著优于通用大语言模型。 这一结果凸显了在特定领域应用中，专用任务架构仍然能够大幅超越庞大的通用模型，挑战了前沿大语言模型在各方面都更优的假设。它强调了在医学影像和其他高风险专业领域中，专用 AI 系统的价值。 所使用的 CNN 是 Inception v3，先在日常照片上预训练，然后在单块 H100 GPU 上使用来自 ISIC Archive 的 68,011 张图像对所有层进行微调。200 个测试病灶被仔细排除在训练和验证数据之外以防止数据泄露，但评论者指出该比较可能涉及'刷榜'行为，因为 CNN 是专门针对该基准测试优化的。

hackernews · sungam · 10月25日 17:15 · [社区讨论](https://news.ycombinator.com/item?id=50233779)

**背景**: 卷积神经网络（CNN）是一类特别适用于图像处理的深度学习网络，通过学习到的滤波器从视觉数据中提取特征。像 GPT-4o 和 Claude 3.5 Sonnet 这样的前沿大语言模型是大型通用 AI 系统，设计用于包括推理、编程和多模态理解在内的广泛任务。在医学影像领域，专用 CNN 多年来一直是主流方法，因为它们可以在精选数据集上训练，以高精度识别特定视觉模式，如皮肤病变。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Convolutional_neural_network">Convolutional neural network - Wikipedia</a></li>
<li><a href="https://www.akamai.com/glossary/what-are-frontier-llms">What Are Frontier LLMs - Akamai</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认为专用模型优于通用大语言模型是意料之中的，有人将其比作 3000 万参数的 KataGo 网络在围棋上击败前沿大语言模型。一些人批评该比较是'刷榜'行为，因为 CNN 是专门针对该基准测试优化的，而另一些人则建议在上下文中提供监督训练数据来测试大语言模型。一位评论者打趣说计算器在乘法上也优于大语言模型。

**标签**: `#machine-learning`, `#medical-imaging`, `#llms`, `#computer-vision`, `#benchmarking`

---
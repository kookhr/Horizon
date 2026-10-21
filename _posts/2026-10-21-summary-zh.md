---
layout: default
title: "Horizon Summary: 2026-10-21 (ZH)"
date: 2026-10-21
lang: zh
---

> 从 36 条内容中筛选出 9 条重要资讯。

---

1. [eMudhra 中间 CA 私钥泄露引发全生态系统紧急更新](#item-1) ⭐️ 10.0/10
2. [DeepSeek 发布 DeepInfer：高性能推理框架](#item-2) ⭐️ 9.0/10
3. [Cloudflare 将 TypeScript 编译器移植到 Rust 以适配 WASM 沙箱](#item-3) ⭐️ 9.0/10
4. [OpenAI 新模型攻克冷门编程语言，COBOL 迁移准确率飙至 97.9%](#item-4) ⭐️ 9.0/10
5. [Mistral 发布 Voxtral 3 语音代理 SDK 及语音模型](#item-5) ⭐️ 8.0/10
6. [Google 开源 TorchTPU：TPU 的原生 PyTorch 后端](#item-6) ⭐️ 8.0/10
7. [Google Cloud 故障导致欧洲主要银行和金融服务中断](#item-7) ⭐️ 8.0/10
8. [安全研究员移除超过 300 个恶意 Tor 出口节点](#item-8) ⭐️ 8.0/10
9. [英伟达禁止使用竞品芯片的小型云厂商参加柏林 GTC 大会](#item-9) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [eMudhra 中间 CA 私钥泄露引发全生态系统紧急更新](https://simonwillison.net/2026/Oct/20/emudhra-certificates/) ⭐️ 10.0/10

2026 年 10 月 17 日，Mozilla 收到报告称 eMudhra 的八个中间 CA 证书私钥已被泄露，促使 Mozilla、Microsoft、Apple 和 Chrome 等所有主要根证书项目采取紧急吊销和封禁措施。捆绑受信任证书列表的软件包——包括 Python 的 certifi 2026.10.19、pip 26.2.2、uv 0.13.4 以及 Linux 发行版的 ca-certificates 包——已快速发布更新版本，移除了被泄露的中间证书。 被泄露的中间 CA 私钥允许攻击者为任意域名伪造有效的 TLS 证书，从而对整个互联网的 HTTPS 连接发起中间人攻击。这构成了一个关键基础设施级别的安全威胁，需要操作系统、Linux 发行版、语言包管理器以及任何维护自身受信任证书库的软件立即采取行动。 根据 eMudhra 在 Mozilla bug 报告中的解释，此次泄露似乎源于某天用于创建 ECC 签发者的密钥生成仪式（KGC）脚本中的缺陷。令人震惊的是，社区成员发现所有八个被泄露 CA 的私钥都极其脆弱——其中一个密钥的字面值就是单字节"4"——这表明是密钥生成方面的灾难性失败，而非复杂的密码学攻击。

rss · Simon Willison · 10月20日 23:50

**背景**: 证书颁发机构（CA）是受信任的第三方，负责颁发验证公钥所有权的数字证书，这是 HTTPS 和安全互联网通信的基础。中间 CA 在信任层级中位于根 CA 之下，是实际签发终端用户（叶子）证书的实体；如果其私钥被泄露，攻击者可以为任何网站伪造证书。浏览器和操作系统维护着根证书库——即受信任根证书的列表——而 Python 的 certifi 或 Linux 的 ca-certificates 包等软件会捆绑这些列表，使应用程序能够验证 TLS 连接而无需完全依赖操作系统。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://emudhra.we-have-a-problem.com/">eMudhra Intermediate CA Compromise</a></li>
<li><a href="https://blog.mozilla.org/security/2026/10/20/protecting-firefox-users-following-the-compromise-of-emudhra-intermediate-certificates/">Protecting Firefox users following the compromise of eMudhra ...</a></li>
<li><a href="https://gist.github.com/UlisesGascon/10ed0724930e5382b3ed48fa2b0d3e02">eMudhra/emSign Oct 2026 intermediate compromise: what a root ...</a></li>

</ul>
</details>

**社区讨论**: 社区成员对被泄露私钥的极度脆弱性表示难以置信，其中一个密钥字面上就是单字节"4"，指向 eMudhra 密钥生成仪式脚本的灾难性失败。一位 Mozilla 安全工程师指出，此次事件的影响分布不均：Firefox 用户通过 OneCRL 和 CRLite 吊销工具在数小时内得到保护，而生态系统其余部分缺乏类似的吊销基础设施投入。还有报告称 GoDaddy 在同一时间段要求大规模重新颁发证书，但与此次事件的关联尚不明确。

**标签**: `#security`, `#cryptography`, `#certificates`, `#infrastructure`, `#ca-compromise`

---

<a id="item-2"></a>
## [DeepSeek 发布 DeepInfer：高性能推理框架](https://github.com/deepseek-ai/DeepInfer) ⭐️ 9.0/10

DeepSeek 发布了 DeepInfer，这是一个开源的高性能推理框架，支撑其大规模生产服务，单集群吞吐量达到每日 155 万亿 token，非高峰时段每卡每小时收入 38 美元。该版本支持 DeepSeek V4.1 Flash 并兼容华为昇腾 950 NPU，标志着在 NVIDIA 主导的 AI 基础设施之外的重要扩展。 此次发布表明 DeepSeek 已实现卓越的推理经济效益，可能重塑 AI 基础设施的竞争格局，而其发布时机——在 DHS 排除令发布数小时后——表明了深思熟虑的地缘政治策略。将生产级推理工具开源，尤其是支持华为 NPU，可能加速替代 AI 硬件生态的发展，并挑战 NVIDIA 的市场主导地位。 DeepInfer 提供离线推理及核心生产能力，同时支持 NVIDIA GPU 和华为昇腾 950 NPU，据报告单集群性能达到每日 155 万亿 token。每卡每小时 38 美元的收入数据按非高峰定价计算，暗示在高峰需求时段效率更高。

hackernews · ggcr · 10月20日 09:08 · [社区讨论](https://news.ycombinator.com/item?id=50163277)

**背景**: DeepSeek 是一家中国 AI 实验室，以其开源大语言模型闻名，这些模型基于 Transformer 架构，采用稀疏专家路由和量化感知计算等先进优化技术。推理框架是优化已训练 AI 模型在生产环境中处理用户请求的软件层，直接影响 AI 服务的成本和速度。此次发布发生在中美技术紧张局势加剧的背景下，包括针对中国 AI 公司的 DHS 排除令和对先进 AI 芯片的出口管制。DeepSeek 的模型因以较低训练成本实现与西方竞争对手相当的性能而备受关注。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/deepseek-ai/DeepInfer">GitHub - deepseek-ai/ DeepInfer : DeepInfer : High-performance...</a></li>
<li><a href="https://deepwiki.com/deepseek-ai/DeepSeek-V3/1.2-model-architecture-overview">Model Architecture Overview | deepseek-ai/DeepSeek-V3 | DeepWiki</a></li>
<li><a href="https://www.edureka.co/blog/deepseek-ai-model-architecture/">DeepSeek AI Architecture Explained: Models, Training ...</a></li>

</ul>
</details>

**社区讨论**: 社区讨论聚焦于发布的战略时机，一位用户指出该框架在 DHS 排除令发布数小时后公开，很可能是数月前就开始准备的战术性回应。讨论围绕 DeepSeek 的开源策略是否构成对美国前沿实验室和 NVIDIA 硬件垄断的经济战，部分评论者认为华为 NPU 支持可能成为打破 NVIDIA 对 AI 硬件市场控制的催化剂。社区情绪从对中国开源方式的赞赏到对美国 AI 竞争力影响的担忧均有体现。

**标签**: `#deepseek`, `#inference-optimization`, `#ai-infrastructure`, `#open-source`, `#geopolitics`

---

<a id="item-3"></a>
## [Cloudflare 将 TypeScript 编译器移植到 Rust 以适配 WASM 沙箱](https://blog.cloudflare.com/typescript-rust-port/) ⭐️ 9.0/10

Cloudflare 将 TypeScript 编译器移植到 Rust（项目名为 tsrs），使其能够在仅支持 WASM 的沙箱环境中运行，并在性能上显著超越了参考实现 tsc/Go。该项目采用了一种新颖的基于 arena 的内存模型，通过永不释放 arena 中的长生命周期对象来模拟垃圾回收，从而克服了 Rust 缺乏内置 GC 的问题。 这一进展表明 TypeScript 编译可以大幅提速，直接惠及在大型代码库中受类型检查瓶颈困扰的开发者。TypeScript 团队已确认与 tsrs 维护者合作，该项目的洞察正在影响即将发布的 TS 7.1 性能优化，这意味着整个生态系统都将从中受益。 核心动机并非纯粹追求速度，而是 WASM 沙箱兼容性——Cloudflare 需要一个能作为 WebAssembly 运行的 TypeScript 编译器，同时避免打包完整的 Go 运行时，Rust 是自然的选择。基于 arena 的内存模型将长生命周期对象分配在永不释放的 arena 中，有效模拟了 GC，这是将 GC 语言代码库移植到 Rust 的一个值得注意的变通方案。TypeScript 团队推测，大部分速度提升来自算法优化而非单纯的语言选择。

hackernews · hnisjafx40 · 10月20日 13:18 · [社区讨论](https://news.ycombinator.com/item?id=50165953)

**背景**: TypeScript 编译器最初用 TypeScript 编写，后来为提升性能移植到 Go（tsc-go）。Rust 缺乏内置垃圾回收器，这使得从 Go 或 TypeScript 等 GC 语言移植代码变得困难，因为通常需要重构数据所有权模型。Arena 分配是一种内存管理策略，对象在连续内存块中分配并一次性全部释放，常用于编译器和游戏引擎中以实现快速、低开销的内存分配。Cloudflare 的 WASM-only 沙箱要求代码以 WebAssembly 形式运行，而将完整的 Go 运行时与编译器一起打包会带来不可接受的开销。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.logrocket.com/guide-using-arenas-rust/">Guide to using arenas in Rust - LogRocket Blog</a></li>
<li><a href="https://developers.cloudflare.com/sandbox/">Overview · Cloudflare Sandboxes docs</a></li>
<li><a href="https://developers.cloudflare.com/workers/runtime-apis/webassembly/">WebAssembly (Wasm) · Cloudflare Workers docs</a></li>

</ul>
</details>

**社区讨论**: TypeScript 团队成员 DanRosenwasser 确认了与 tsrs 维护者的积极合作，并透露该项目的洞察正在指导 TS 7.1 的优化，指出大部分速度提升可能来自算法改进而非单纯的语言选择。评论者 sheepscreek 澄清了主要动机是 WASM 沙箱兼容性而非构建更快的编译器，速度只是一个令人欢迎的副作用。也有部分评论者对重复造轮子表示不满，并对编译器行为的某些变更提出了担忧。

**标签**: `#typescript`, `#rust`, `#wasm`, `#compilers`, `#cloudflare`

---

<a id="item-4"></a>
## [OpenAI 新模型攻克冷门编程语言，COBOL 迁移准确率飙至 97.9%](https://openai.com/index/low-resource-programming-languages/) ⭐️ 9.0/10

OpenAI 最新的 GPT-6 系列模型大幅提升了 COBOL、Fortran 和 Visual Basic 等低资源编程语言的代码生成与迁移能力。在 COBOL 迁移任务中，GPT-6.1 Sol 在高推理强度下准确率高达 97.9%，而低成本的 GPT-6 Luna 模型将 API 成本降低了 78%，并在 20 种语言的 SQLite 引擎测试中将平均通过率从 26.8% 提升至 87.4%。 这一突破对企业和政府领域遗留系统的现代化具有重大意义，这些领域仍有数十亿行 COBOL 代码在关键的大型机操作中运行。准确率的大幅提升加上成本的显著降低，使大规模迁移项目在经济上变得可行，有望加速全球范围内早已亟待更新的老化基础设施的现代化进程。 在涵盖 20 种语言的 SQLite 引擎构建测试中，GPT-6 Astra 的平均通过率从 GPT-5.6 Sol 的 26.8% 跃升至 87.4%，而 GPT-6 Luna 以低 78% 的 API 成本达到了 40.3% 的通过率。在 COBOL 迁移方面，GPT-6.1 Sol 在低推理强度下已将准确率从 5.4% 提升至 86.6%，成本降低 39%，高推理强度下更是达到 97.9%；相关评测基准已在 GitHub 上开源。

telegram · zaihuapd · 10月20日 14:24

**背景**: 低资源编程语言（LRPL）是指在大语言模型可用训练数据中严重代表性不足的编程语言，这使得 AI 辅助的代码生成和迁移对它们而言尤为困难。COBOL 虽然已有 60 多年历史，但仍支撑着约 43% 的银行系统和 95% 的 ATM 交易，估计在政府和企业大型机中有约 2200 亿行 COBOL 代码仍在使用中。将这些遗留系统迁移至现代语言传统上是一个手动、易出错且极其昂贵的过程，通常需要稀缺的专家技能。OpenAI 的 GPT-6 系列包括 Astra（2026 年 9 月发布）、Sol 和 Luna 等变体，各自针对不同的性能与成本权衡。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/low-resource-programming-languages/">Advancing coding in low‑resource programming languages</a></li>
<li><a href="https://en.wikipedia.org/wiki/GPT-6_Astra">GPT-6 Astra</a></li>
<li><a href="https://www.emergentmind.com/topics/low-resource-programming-languages-lrpls">Low-Resource Programming Languages - emergentmind.com</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#COBOL`, `#Code Migration`, `#Legacy Systems`, `#LLM`

---

<a id="item-5"></a>
## [Mistral 发布 Voxtral 3 语音代理 SDK 及语音模型](https://mistral.ai/news/voxtral-3/) ⭐️ 8.0/10

Mistral 发布了 Voxtral 3，这是一款语音代理 SDK 和语音转文本模型套件，将听、推理、工具调用和说结合为跨越 50 多种语言的实时体验。该版本包含三个转录变体（Small、Mini 和延迟低于 500 毫秒的 Mini Realtime）以及支持情感适配的 Voxtral Speech 3 TTS，可通过欧洲、美国和全球 API 端点访问。 Voxtral 3 代表了开源权重语音 AI 的重大进步，提供可在普通硬件上运行的实时推理能力，并在多语言转录和说话人分离方面挑战 Whisper、Gemini 和 GPT 等专有模型。集成的 SDK 使开发者能够构建端到端的语音代理，能够在实时对话中检索信息、与业务系统交互并完成任务，有望变革客户服务和企业通信工作流。 Mistral 声称 Voxtral 3 在多语言转录、说话人分离和发音方面优于 Whisper、Gemini 和 GPT 模型，覆盖 50 多种语言的 ASR 和 35 种以上语言的语音合成。Mini Realtime 变体实现了低于 500 毫秒的延迟，上一代 Voxtral Mini 4B Realtime 模型已成功部署在仅需 4GB 显存的普通硬件上进行离线推理，在中端笔记本电脑上超越了实时速率。

hackernews · ilreb · 10月20日 16:02 · [社区讨论](https://news.ycombinator.com/item?id=50168396)

**背景**: 语音转文本（STT）和文本转语音（TTS）技术在口语和书面语言之间进行转换，构成了基于语音的 AI 应用的基础。开放权重模型公开发布其学习到的参数，允许开发者下载并在本地运行模型，但修改和再分发权限取决于具体许可证。大语言模型中的工具调用使模型能够与外部 API 和系统交互，允许 AI 代理识别何时需要工具、选择合适的工具、以正确的参数执行，并将结果整合回其响应中。Voxtral 3 将这些能力整合到统一的 SDK 中，使语音代理能够通过电话或网络渠道实时听、推理、调用工具和说话。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mistral.ai/news/voxtral-3/">Voxtral 3: Voice Agent SDK & Speech Models in 50+ Languages</a></li>
<li><a href="https://aiweekly.co/alerts/mistral-ships-voxtral-3-voice-suite-with-50-languages-and-sub-500ms-realtime">Mistral ships Voxtral 3 voice suite with 50+ languages</a></li>
<li><a href="https://en.wikipedia.org/wiki/Open-weight_model">Open-weight model</a></li>

</ul>
</details>

**社区讨论**: 社区情绪褒贬不一，一些用户赞赏技术能力，而另一些则对实际部署限制表示沮丧。一位用户强调上一代 Voxtral Mini 4B Realtime 模型在仅需 4GB 显存的普通硬件上离线推理效果良好，并正在开发 Linux 版本。几位评论者对 Microsoft Teams 等企业软件生成糟糕的转录表示沮丧，希望能将这些更好的模型集成到现有工具中。一位评论者指出演示不切实际，而另一位则指出该模型似乎是闭源的，延续了 TTS/STT 模型在本地部署方面表现不佳的趋势。

**标签**: `#Speech-to-Text`, `#Voice AI`, `#Mistral`, `#Open-Weight Models`, `#Real-Time Inference`

---

<a id="item-6"></a>
## [Google 开源 TorchTPU：TPU 的原生 PyTorch 后端](https://github.com/google-pytorch/torch_tpu) ⭐️ 8.0/10

Google 与 Meta 合作开发了 TorchTPU 并将其开源，这是一个用于 TPU 的原生 PyTorch 后端，只需极少的代码修改即可在 Google 的张量处理单元上无缝运行 PyTorch 工作负载。该项目利用即时执行优化、torch.compile 集成和原生硬件接口，提供具有行业竞争力的训练和推理性能。 这大幅降低了开发者使用 Google 定制 AI 加速器的门槛，因为 PyTorch 是全球使用最广泛的开源机器学习框架。这也标志着行业向专用硬件提供原生框架支持的更广泛趋势，AWS 也针对其 Trainium 加速器采取了类似的策略。 TorchTPU 取代了旧的 PyTorch/XLA 库方案——后者需要将 PyTorch 操作转换为 XLA 中间表示——提供了一个更直接、更规范的后端。硬件特定逻辑现在主要存在于内核层（如 Pallas 或 CUDA），使得 JAX 与 PyTorch 的选择越来越取决于开发者的风格偏好，而非硬件兼容性。

hackernews · ilreb · 10月20日 16:40 · [社区讨论](https://news.ycombinator.com/item?id=50169053)

**背景**: Google 的张量处理单元（TPU）是为高吞吐量机器学习工作负载设计的定制 AI 加速器，但历史上需要使用 JAX 或 TensorFlow 才能获得最佳性能。旧的 PyTorch/XLA 库通过将 PyTorch 计算图编译为 XLA 中间表示来提供桥梁，但这引入了复杂性和性能开销。XLA（加速线性代数）是 Google 最初开发的编译器生态系统，用于跨硬件后端优化张量计算。Pallas 是 JAX/XLA 生态系统中用于编写自定义 TPU 内核的较低层级语言。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://pytorch.org/blog/introducing-torchtpu/">Introducing TorchTPU - PyTorch</a></li>
<li><a href="https://cloud.google.com/blog/topics/ai-infrastructure/torchtpu-is-now-open-source-run-native-pytorch-on-tpus">TorchTPU is now open source: Run native PyTorch on TPUs</a></li>
<li><a href="https://grokipedia.com/page/TorchTPU">TorchTPU</a></li>

</ul>
</details>

**社区讨论**: 社区情绪非常积极，用户庆祝不再需要费力应对 XLA 来在 TPU 上运行 PyTorch，并认为这是 TensorFlow 衰落的又一标志。评论者还将此与 AWS 针对其 Trainium 的类似项目 torch-neuronx 进行了对比，强调了一个针对 Tenstorrent 加速器的独立 libtpu 实现，并推测 Google 和 Apple 向边缘推理的推进可能会颠覆即将到来的 AI 基础设施 IPO。

**标签**: `#PyTorch`, `#TPU`, `#Google`, `#Machine Learning`, `#Open Source`

---

<a id="item-7"></a>
## [Google Cloud 故障导致欧洲主要银行和金融服务中断](https://www.neowin.net/news/google-cloud-outage-takes-down-hsbc-revolut-bank-of-scotland-llyods-equifax-more/) ⭐️ 8.0/10

2026 年 10 月 19 日，europe-west2-b 区域的电力事件导致 Google Cloud 发生大范围故障，影响了包括汇丰银行（HSBC）、Revolut、劳埃德银行（Lloyds）、苏格兰银行和 Equifax 在内的主要金融机构。此次故障导致欧洲各地客户的网上银行、银行卡支付和账户访问功能中断，预计在电力问题解决后 30 分钟内部分服务将恢复。 此次事件暴露了将关键金融基础设施集中于单一云服务商和区域所带来的系统性风险，单一故障点可能同时波及多家主要银行。这凸显了金融机构实施稳健的多区域或多云冗余策略的迫切需求，并再次引发了关于欧洲是否应建设主权云替代方案以减少对美国云服务商依赖的讨论。 故障源于位于伦敦的 europe-west2 区域内 europe-west2-b 区域的电力事件，Google 状态页面显示基础设施服务将在 30 分钟内部分恢复。值得注意的是，部分用户报告称汇丰银行等服务仍正常运行，这引发了对 Downdetector 报告准确性以及故障实际影响范围的质疑。

hackernews · paweladamczuk · 10月20日 10:26 · [社区讨论](https://news.ycombinator.com/item?id=50163961)

**背景**: Google Cloud Platform 将其基础设施划分为区域（如位于伦敦的 europe-west2）和可用区（如 europe-west2-b），每个可用区是区域内一个独立的地理位置。Google 建议将重要系统跨多个可用区和区域进行复制，以减轻电力事件等局部故障的影响。然而，许多组织，尤其是银行业，可能在单一可用区或区域中运行关键工作负载而缺乏足够的冗余，使其容易受到区域性故障的影响。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.cloud.google.com/compute/docs/regions-zones">Regions and zones | Compute Engine | Google Cloud Documentation</a></li>
<li><a href="https://gcloud-compute.com/europe-west2.html">europe-west2 - Google Cloud Platform Region</a></li>

</ul>
</details>

**社区讨论**: 讨论突出了对新型银行客户的实际影响，一位用户报告称其 Revolut 账户被完全锁定，无法访问资金或获得支持。关于 Downdetector 作为信息源的可靠性存在显著争议，一位汇丰银行客户声称其银行服务正常，并质疑故障报告的准确性。还有人提出了更广泛的政治观点，认为欧洲需要建设自己的云替代方案以减少对美国服务商的依赖，尽管这一观点遭到了一些关于欧洲隐私价值观的讽刺。

**标签**: `#cloud-outage`, `#google-cloud`, `#infrastructure`, `#banking`, `#reliability`

---

<a id="item-8"></a>
## [安全研究员移除超过 300 个恶意 Tor 出口节点](https://kaba.cx/posts/20261020_Tor/) ⭐️ 8.0/10

一名安全研究员发现并报告了超过 300 个正在对 SSH 连接执行中间人（MITM）攻击的 Tor 出口节点，这些节点随后被从 Tor 网络中移除。研究员详细描述了检测这些恶意节点的方法，这些节点拦截 SSH 流量并试图窃取凭据。 这一事件凸显了使用 Tor 出口节点进行敏感通信的固有风险，因为任何由志愿者运营的出口节点都可以拦截未加密或认证不当的流量。它强调了强双向认证机制的重要性，例如基于密钥的 SSH 认证，由于私钥从不离开客户端，因此对这类 MITM 攻击具有抵抗力。 恶意出口节点利用了那些忽略 SSH 主机密钥验证警告的用户，拦截他们的连接以窃取密码、注入命令，并可能部署更多恶意软件。这种攻击相对容易被检测到，因为当服务器的主机密钥发生变化时，SSH 客户端会显示醒目的警告，提醒警觉的用户注意拦截行为。

hackernews · kabakabakaba · 10月20日 13:39 · [社区讨论](https://news.ycombinator.com/item?id=50166257)

**背景**: Tor 是一个用于实现匿名通信的免费覆盖网络，基于由全球七千多个志愿者运营的中继节点运行的开源软件构建。流量通过这些中继节点的随机路径进行路由，使得追踪用户活动变得困难。然而，电路中的最后一个中继节点（即出口节点）可以观察从 Tor 网络离开前往公共互联网目的地的流量。中间人（MITM）攻击是指攻击者秘密拦截并可能篡改两方之间的通信，而这两方认为他们正在直接通信。在 SSH 的语境下，MITM 攻击依赖于客户端未能验证服务器身份，通常是因为忽略了主机密钥不匹配的警告。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Tor_exit_node">Tor exit node</a></li>
<li><a href="https://en.wikipedia.org/wiki/Man-in-the-middle_attack">Man-in-the-middle attack - Wikipedia</a></li>
<li><a href="https://www.ssh.com/academy/attack/man-in-the-middle">Man in the Middle Attack: How Does it Actually Work? - SSH</a></li>

</ul>
</details>

**社区讨论**: 社区讨论包括用于扫描 Tor 出口节点的工具 exitmap 的原作者，他指出该工具在十年后仍然有用。评论者指出，这次 SSH 攻击设计得相当拙劣，因为 SSH 醒目的 MITM 警告横幅使其很容易被检测和追踪，而且基于密钥的认证不会受到影响，因为私钥从不离开客户端。一些人还指出，出口节点的总数（约 3000 个）少得令人惊讶，这使得移除 300 个节点成为网络中很大的一部分。

**标签**: `#security`, `#tor`, `#ssh`, `#mitm`, `#network-security`

---

<a id="item-9"></a>
## [英伟达禁止使用竞品芯片的小型云厂商参加柏林 GTC 大会](https://x.com/SemiAnalysis_/status/2111162214891610496?s=20) ⭐️ 8.0/10

据报道，英伟达已拒绝多家新兴云服务商参加即将于 2026 年 10 月 20 日至 22 日在柏林举行的 GTC 大会，原因是这些厂商在自有云平台中使用了 AMD GPU、Google TPU 等竞品芯片。该限制不适用于拥有足够采购体量和自研芯片能力的超大规模云厂商。 此举凸显了英伟达在 AI 基础设施生态系统中日益增长的杠杆作用——它既是关键芯片供应商，又是 CoreWeave 和 Nebius 等新兴云厂商的重要投资方，已向两家各战略投资约 20 亿美元。小型云厂商担忧使用竞品芯片会影响其 GPU 优先供应、融资及上市计划，引发了 AI 硬件市场中反竞争和供应商锁定问题的严重关切。 英伟达尚未就该排除事件公开置评，被拒厂商并非因技术不达标而被拒，而是明确因为引入了竞品硬件。英伟达与新兴云厂商的财务关联不仅限于股权投资，还包括为其算力租赁业务提供收入兜底，进一步加深了小型厂商对英伟达的依赖。

telegram · zaihuapd · 10月20日 12:32

**背景**: 英伟达 GTC（GPU 技术大会）是一年两度的行业盛会，展示 AI、计算机图形和深度学习应用，是行业发布和人脉交流的重要平台。新兴云服务商（通常被称为

**标签**: `#Nvidia`, `#Cloud Computing`, `#Anti-competitive`, `#AMD`, `#AI Hardware`

---
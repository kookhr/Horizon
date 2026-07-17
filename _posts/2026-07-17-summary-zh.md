---
layout: default
title: "Horizon Summary: 2026-07-17 (ZH)"
date: 2026-07-17
lang: zh
---

> 从 32 条内容中筛选出 6 条重要资讯。

---

1. [华为昇腾 950 超节点首次公开亮相，算力达英伟达同级 6.7 倍](#item-1) ⭐️ 9.0/10
2. [AWS 预估账单数据严重失准，显示数十亿美元费用](#item-2) ⭐️ 8.0/10
3. [首次在宜居带类地行星上探测到大气层](#item-3) ⭐️ 8.0/10
4. [开源 AI 现状：数据驱动的竞争格局分析](#item-4) ⭐️ 8.0/10
5. [Puter 将 Firefox 编译为 WebAssembly，可在任意浏览器中运行](#item-5) ⭐️ 8.0/10
6. [Kimi K3 发布：2.8T 开源模型登顶前端编程 Arena](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [华为昇腾 950 超节点首次公开亮相，算力达英伟达同级 6.7 倍](https://www.ithome.com/0/978/019.htm) ⭐️ 9.0/10

7 月 17 日，华为在 2026 世界人工智能大会（WAIC）上首次公开亮相昇腾 950 超节点（Atlas 950 SuperPoD）真机，该设备实现业界最大 1024 卡规模，提供 1 EFLOPS FP8、2 EFLOPS FP4 算力，拥有 256 TB 全局统一内存。据中银证券报告，与英伟达搭载 144 张卡的同级别 NVL144 系统相比，昇腾 950 总算力达到其 6.7 倍。 这标志着 AI 硬件领域和中美科技竞争中的一个重要里程碑，表明华为在先进工艺受限的情况下仍能构建与英伟达顶级系统竞争的大规模 AI 计算集群。1024 卡的扩展架构代表了一项重大突破，对大模型训练和推理工作负载具有直接的商业价值。 昇腾 950 超节点基于华为自研的灵衢（UnifiedBus）互联协议和超节点架构构建，华为同期还展出了 Atlas 850E 风冷超节点，企业无需液冷改造即可在标准风冷机房直接部署。此外，昇腾 384 超节点已商用落地 750 多套，广泛应用于互联网、运营商、金融等行业，是国内唯一训练出 SOTA 模型的超节点。

telegram · zaihuapd · 7月17日 10:27

**背景**: 华为的灵衢（UnifiedBus，简称 UB）是面向超节点架构的统一互联协议，旨在将 I/O、内存访问以及异构计算单元（CPU/NPU/GPU 等）之间的通信融合到同一技术体系中。由于先进工艺不可获得，华为从 2019 年开始研发灵衢，希望通过多芯片扩展将更多计算资源联接在一起。基于灵衢 1.0 的 Atlas 900 超节点自 2025 年 3 月开始商用部署，而昇腾 950 则基于功能更丰富、性能更优的灵衢 2.0 协议构建，华为已将该规范向业界开放。英伟达的 NVL144 是一种机架级配置，通过 NVLink 连接 144 张 GPU，是华为用于对标比较的同级别系统。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.huawei.com/cn/news/2025/9/hc-xu-keynote-speech">以开创的超节点互联技术，引领AI基础设施新范式</a></li>
<li><a href="https://finance.jrj.com.cn/2026/07/17201957836496.shtml">华为昇腾950超节点真机首次公开亮相！业界最大1024卡规模-财经-金融界</a></li>
<li><a href="https://www.supercomputing.news/entity/nvidia-vera-rubin-nvl144">NVIDIA Vera Rubin NVL 144 — Supercomputing News</a></li>

</ul>
</details>

**标签**: `#AI Hardware`, `#Huawei`, `#Ascend 950`, `#Supercomputing`, `#AI Chips`

---

<a id="item-2"></a>
## [AWS 预估账单数据严重失准，显示数十亿美元费用](https://news.ycombinator.com/item?id=48945241) ⭐️ 8.0/10

2025 年 7 月前后，大量 AWS 客户开始报告预估账单费用出现荒谬的虚高，正常月费不到 5 美元的账户却显示从 7800 万美元到 17 亿美元不等的费用。该问题似乎源于 AWS 计量与计费系统中的单位换算错误，本应以吉字节（GB）为单位的存储或数据传输量被误当作原始字节处理，导致费用膨胀约 2^30 倍。 虽然这些费用明显有误并将被修正，但该事件暴露了为数百万客户处理海量计量数据的云计费系统的脆弱性。它还引发了用户的极大恐慌和焦虑，许多人担心凭证泄露或费用失控，同时也凸显了大规模金融系统中健壮的单位处理机制的重要性。 一位前 AWS 工程师解释说，各服务发出的计量值并不直接与价格挂钩，而是每个 SKU 和计费项都在单独的'定价计划'中定义；如果计量记录中遗漏了单位（如 GB），计费系统会默认以字节为单位，从而产生约比预期高 1,073,741,824 倍的费用。2^30 的误差倍数恰好对应一个吉字节与一个字节之间的差异。

hackernews · nprateem · 7月17日 09:42

**背景**: AWS 使用一套复杂的计量与计费管道，各服务先发出使用量数据，随后与定价计划匹配以计算费用。该系统在所有 AWS 服务和区域间处理海量遥测数据，因此单位一致性至关重要。AWS Cost Explorer 和账单告警依赖同一预估数据流，这就是客户因虚高数据而触发预算阈值告警的原因。

**社区讨论**: 社区反应兼具黑色幽默与技术洞察，用户们分享了看到数十亿美元账单时的肾上腺素飙升反应，前 AWS 工程师则详细解释了计量管道的工作原理。多位评论者指出，虽然此次错误显而易见且将被修正，但更隐蔽的计费错误可能持续数月甚至数年——一位用户回忆在 2010 年代初发现 EC2 预留实例节省费用计算错误，花了很大力气才说服 AWS 予以纠正。

**标签**: `#AWS`, `#billing`, `#cloud-computing`, `#bug`, `#infrastructure`

---

<a id="item-3"></a>
## [首次在宜居带类地行星上探测到大气层](https://www.bbc.com/news/articles/cy4kdd1e0ejo) ⭐️ 8.0/10

天文学家使用詹姆斯·韦伯空间望远镜（JWST）在距离地球 48 光年的红矮星宜居带内的岩石系外行星 LHS 1140b 上探测到了大气层。这是首次在位于恒星宜居带内的类地行星上确认存在大气层，这是寻找可能支持生命的星球过程中的一个关键里程碑。 这一发现是寻找地外生命的重要一步，因为大气层被认为是已知生命存在的先决条件。此次探测证明了 JWST 具备研究小型岩石系外行星大气成分的能力，为表征太阳系外潜在宜居世界的条件打开了大门。 LHS 1140b 的半径约为地球的 1.7 倍，每 24.7 天绕其红矮星宿主恒星运行一周。JWST 在该行星经过其恒星后方时收集的发射光谱数据帮助排除了 LHS 1140b 是迷你海王星的可能性，证实了其岩石质的类地性质。

hackernews · neversaydie · 7月17日 14:06 · [社区讨论](https://news.ycombinator.com/item?id=48947560)

**背景**: 宜居带，也称为

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bbc.com/news/articles/cy4kdd1e0ejo">First atmosphere found around Earth-like planet LHS 1140 b</a></li>
<li><a href="https://earthsky.org/space/water-world-mini-neptune-lhs-1140-b/">Is this nearby exoplanet a water world? Or a mini-Neptune?</a></li>
<li><a href="https://science.nasa.gov/exoplanets/habitable-zone/">The Habitable Zone - NASA Science</a></li>

</ul>
</details>

**社区讨论**: 社区成员对一颗围绕红矮星运行的岩石行星能够在强烈的恒星剥离作用下保留大气层感到惊讶，一位评论者最初怀疑它是一颗正在被蒸发的迷你海王星，但随后承认 JWST 的数据排除了这种可能性。讨论还涉及向这颗距离 48 光年的行星发射探测器的可行性，有人提出了接近光速的推进系统建议，还有人提议建造太阳透镜望远镜以更详细地研究这类候选行星。一位评论者指出，探测到的大气中的氦气表明该行星具有极大的逃逸速度，如果那里存在生命，这可能意味着他们被困住了。

**标签**: `#astronomy`, `#exoplanets`, `#jwst`, `#space-exploration`, `#astrophysics`

---

<a id="item-4"></a>
## [开源 AI 现状：数据驱动的竞争格局分析](https://stateofopensource.ai/) ⭐️ 8.0/10

Mozilla 在 stateofopensource.ai 上发布了一份数据驱动的报告，追踪开源与闭源 AI 模型在各项指标上的竞争格局。分析显示 OpenRouter 上的市场份额发生了显著变化，开源模型处理的 token 数从三月的 888B 增长到 4.19T——四个月内增长了近 5 倍，市场格局从闭源占优的 60-40 翻转为开源占优的 63-37。 这一数据标志着 AI 行业可能正处于拐点，开源模型正在快速缩小与 OpenAI 和 Anthropic 等前沿闭源模型的差距。开源模型采用的指数级增长对昂贵的前沿模型开发的可持续性具有战略意义，因为超大规模云服务商和设备制造商可以无需许可费即可部署开源模型。 该报告使用 OpenRouter 数据作为整体市场趋势的代理指标，显示开源模型 token 处理量在四个月内增长了约 5 倍。然而，该报告本身因疑似 AI 生成而受到批评，大量图表与周围文字关联松散，部分人认为这削弱了分析的可信度。

hackernews · rellem · 7月17日 14:31 · [社区讨论](https://news.ycombinator.com/item?id=48947825)

**背景**: 开源与闭源 AI 模型的争论核心在于模型权重是否应公开可下载（如 Meta 的 Llama、Mistral、DeepSeek 和 Qwen 等开源模型）还是仅通过 API 访问（如 OpenAI 的 GPT、Anthropic 的 Claude 和 Google 的 Gemini 等闭源模型）。开源模型在性能上历史上落后于前沿闭源模型，但在透明度、灵活性、成本和数据隔离方面具有优势。Mozilla 曾以开源 Firefox 浏览器对抗 Internet Explorer 的垄断而建立品牌，现已将自身定位为开源 AI 生态的倡导者，将其与历史上对抗网络私有控制的行为相类比。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.index.dev/blog/open-source-vs-closed-ai-guide">Open -Source vs Closed AI : Trust, Security & Performance</a></li>
<li><a href="https://tendril.neural-forge.io/learn/builders/builders-foundations-ai-open-source-vs-closed-r10a10-teen">Open -Source vs Closed AI : What Llama, Mistral, and DeepSeek...</a></li>
<li><a href="https://abundance.institute/our-work/vibrant-ai-competitive-landscape">The Vibrant AI Competitive Landscape</a></li>

</ul>
</details>

**社区讨论**: 社区讨论围绕市场动态展开了实质性辩论，一位用户推测开源模型最终可能威胁 OpenAI 和 Anthropic 的商业模式，因为超大规模云服务商可以无需许可费运行这些模型，而 Apple 可以将其缩小后在设备端部署。另一位用户构建了一个追踪 OpenRouter 数据的仪表板，显示开源模型的 token 处理量在四个月内从 888B 增长到 4.19T。然而，多位评论者批评该报告明显由 AI 生成，认为大量关联松散的图表和缺乏真正的人类分析实际上损害了 Mozilla 的信息传递，并导致部分受众直接放弃关注。

**标签**: `#open-source`, `#AI`, `#LLM`, `#market-analysis`, `#open-models`

---

<a id="item-5"></a>
## [Puter 将 Firefox 编译为 WebAssembly，可在任意浏览器中运行](https://simonwillison.net/2026/Jul/16/firefox-in-webassembly/#atom-everything) ⭐️ 8.0/10

Puter 使用 emscripten 成功将 Firefox/Gecko 浏览器引擎编译为 WebAssembly，使整个 Firefox 浏览器能够在另一个浏览器标签页中运行。该项目大量借助 AI 辅助完成，消耗了价值约 25,000 美元的 Claude Opus 和 Fable token，但由于使用了 Claude Max 订阅计划，实际花费远低于此数字。 这是一项技术实力极强的演示，拓展了 WebAssembly 的能力边界，表明即使是完整的浏览器引擎也能被编译并在沙箱化的 Web 环境中运行。它还凸显了 AI 编程工具在处理传统上需要大型工程团队才能完成的极复杂软件工程任务中日益增长的作用。 选择 Firefox/Gecko 是因为其具有强大的单进程支持，编译后的 gecko.wasm 文件为 233MB，另有 18MB 的 chrome-assets.tar.zst。由于浏览器中的代码无法打开任意网络连接，所有网络流量都通过 Puter 的服务器使用 Wisp 协议的 WebSocket 代理进行转发；该项目声称支持端到端加密，对 HTTPS 站点的加密流量验证属实。

rss · Simon Willison · 7月16日 23:34

**背景**: WebAssembly（WASM）是一种低级、类似汇编的语言，具有紧凑的二进制格式，可在现代 Web 浏览器中以接近原生的性能运行，使 C、C++ 和 Rust 等语言能够编译并在 Web 上运行。Emscripten 是一个将 C/C++ 代码编译为 WebAssembly 的工具链。Wisp 协议是一种低开销协议，旨在通过单个 WebSocket 连接代理多个 TCP 和 UDP 套接字，这对于在浏览器沙箱中运行的 WASM 编译应用实现网络访问至关重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.puter.com/labs/firefox-wasm/">Firefox in WebAssembly</a></li>
<li><a href="https://github.com/HeyPuter/firefox-wasm">GitHub - HeyPuter/ firefox - wasm : Firefox in WebAssembly · GitHub</a></li>
<li><a href="https://github.com/MercuryWorkshop/wisp-protocol">GitHub - MercuryWorkshop/ wisp - protocol : Wisp is a low-overhead...</a></li>

</ul>
</details>

**社区讨论**: 该项目在 Hacker News 上引发了极大关注，团队不得不扩大代理服务器规模以应对讨论期间的流量激增。讨论聚焦于在浏览器中运行完整浏览器的创新性，以及使用 AI 编程工具处理复杂项目的有趣成本动态。

**标签**: `#WebAssembly`, `#Firefox`, `#Browser`, `#AI-assisted coding`, `#Puter`

---

<a id="item-6"></a>
## [Kimi K3 发布：2.8T 开源模型登顶前端编程 Arena](https://www.kimi.com/blog/kimi-k3) ⭐️ 8.0/10

月之暗面发布了 Kimi K3，全球首个开源的 2.8 万亿参数模型，具备原生视觉能力和 100 万 token 上下文窗口。K3 在 Frontend Code Arena 中以 1679 分排名第一，从 Kimi K2.6 的第 18 名跃升至榜首，7 个评测领域中 6 项居首。 发布具备原生视觉和 100 万上下文的 2.8 万亿参数开源模型，是开源大模型领域的重要里程碑，拓展了开源模型的能力边界。其在 Frontend Code Arena 中排名第一，展现了强劲的编程能力，但整体性能仍不及 Claude Fable 5 和 GPT 5.6 Sol 等顶级闭源模型。 K3 基于 Kimi Delta Attention（KDA）与 Attention Residuals（AttnRes）架构，已在 Kimi.com、Kimi Work、Kimi Code 及 API 上线。全量模型权重将于 2026 年 7 月 27 日开放，API 定价为缓存命中每百万 token 0.30 美元、缓存未命中 3.00 美元、输出 15.00 美元。

telegram · zaihuapd · 7月17日 00:02

**背景**: Kimi Delta Attention（KDA）是一种表达力强的线性注意力机制，采用细粒度的逐通道门控来高效管理循环记忆，从而更好地处理长上下文。Attention Residuals（AttnRes）是 Transformer 中标准残差连接的直接替代方案，允许每一层选择性地聚合所有先前层的信息，而非使用均匀的加法累积。Frontend Code Arena 是一个第三方基准测试，通过真实用户构建应用和网站（使用 HTML 和 React）的智能体前端编程任务来评估模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/pdf/2510.26692">Kimi Linear: An Expressive, Efficient Attention Architecture</a></li>
<li><a href="https://github.com/MoonshotAI/Attention-Residuals">GitHub - MoonshotAI/ Attention - Residuals · GitHub</a></li>
<li><a href="https://x.com/arena/status/2056803664606679059">Arena.ai on X: "Code Arena: Frontend evaluates models on agentic frontend coding tasks from real users building apps and websites (HTML and React). Agents are an entirely different contest. More from Arena soon. Filter and dive into all the Code Arena: Frontend leaderboard details at:" / X</a></li>

</ul>
</details>

**标签**: `#LLM`, `#Open Source`, `#Kimi K3`, `#Moonshot AI`, `#Code Generation`

---
---
layout: default
title: "Horizon Summary: 2026-07-16 (ZH)"
date: 2026-07-16
lang: zh
---

> 从 39 条内容中筛选出 17 条重要资讯。

---

1. [Thinking Machines Lab 发布 975B 参数开源权重多模态模型 Inkling](#item-1) ⭐️ 9.0/10
2. [Linus Torvalds 宣布 Linux 不是反 AI 项目](#item-2) ⭐️ 9.0/10
3. [欧盟裁定谷歌必须向竞争对手开放 Android 与搜索数据](#item-3) ⭐️ 9.0/10
4. [Kimi 发布 K3：2.8 万亿参数开源模型，支持 100 万上下文](#item-4) ⭐️ 9.0/10
5. [Roc 编译器从 Rust 重写为 Zig：进展与权衡](#item-5) ⭐️ 8.0/10
6. [xAI 在隐私事件后开源 Grok Build CLI 工具](#item-6) ⭐️ 8.0/10
7. [长鑫年底产能逼近美光，中国将成全球第二大 DRAM 产地](#item-7) ⭐️ 8.0/10
8. [日本购 2.75 万块英伟达 Rubin 芯片打造机器人主权 AI](#item-8) ⭐️ 8.0/10
9. [微软 Comic Chat 已开源](#item-9) ⭐️ 7.0/10
10. [OnePlus 停止在欧洲和北美推出新产品](#item-10) ⭐️ 7.0/10
11. [Codex Bug 在无沙箱保护下删除用户$HOME 目录](#item-11) ⭐️ 7.0/10
12. [AI 记忆架构是否在为错误的抽象层做优化？](#item-12) ⭐️ 7.0/10
13. [xAI 起诉用户滥用 Grok 生成儿童性虐待深度伪造](#item-13) ⭐️ 7.0/10
14. [知网将下架将 DeepSeek 等 AI 列为作者的论文](#item-14) ⭐️ 7.0/10
15. [美国 ITC 启动 DRAM 专利 337 调查，三星、英伟达、谷歌等被列为被告](#item-15) ⭐️ 7.0/10
16. [台积电再投千亿美元赴美设厂，二季度利润飙升 77%创历史新高](#item-16) ⭐️ 7.0/10
17. [1Password 推出 Claude 集成：AI 可代登录网站但全程不接触密码](#item-17) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Thinking Machines Lab 发布 975B 参数开源权重多模态模型 Inkling](https://simonwillison.net/2026/Jul/16/inkling/#atom-everything) ⭐️ 9.0/10

由前 OpenAI 首席技术官 Mira Murati 创立的 Thinking Machines Lab 发布了其首个开源权重模型 Inkling，采用 Apache-2.0 许可证。Inkling 是一个混合专家（MoE）Transformer 模型，总参数量为 975B，活跃参数量为 41B，在 45 万亿个文本、图像、音频和视频 token 上训练而成；更小的 276B 变体（Inkling-Small）将在后续发布。 此次发布为美国开源权重生态系统增添了一个重要的新竞争者，与 NVIDIA Nemotron 和 Google Gemma 系列并列，共同与中国涌现的开源权重模型竞争。然而，模型卡和训练数据文档异常简略，引发了透明度方面的担忧——Simon Willison 指出，文档几乎没有提供关于训练数据组成的有意义细节。 Inkling 采用混合专家架构，在 975B 总参数中每次输入仅激活 41B 参数，比同等规模的稠密模型更具计算效率。Thinking Machines Lab 明确表示 Inkling 并非前沿模型，而是旨在通过其 Tinker 训练平台进行微调的强大基础模型，该模型可通过兼容 OpenAI 的 API 端点访问。

rss · Simon Willison · 7月16日 15:35

**背景**: 混合专家（MoE）是一种 Transformer 架构，通过稀疏性在不按比例增加计算成本的情况下扩大模型规模——每次输入仅激活一部分参数（

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained</a></li>
<li><a href="https://www.adaline.ai/blog/what-is-the-difference-between-open-source-and-open-weight-models">What is the difference between open-source and open-weight ...</a></li>

</ul>
</details>

**标签**: `#AI`, `#Open-Weights`, `#Multimodal`, `#Thinking Machines Lab`, `#LLM`

---

<a id="item-2"></a>
## [Linus Torvalds 宣布 Linux 不是反 AI 项目](https://simonwillison.net/2026/Jul/16/linus-torvalds/#atom-everything) ⭐️ 9.0/10

Linus Torvalds 作为 Linux 内核的最高维护者，在 Linux Media 邮件列表上明确表示 Linux 不是反 AI 项目，AI 是一种明显有用的工具。他告诉那些持反对意见的人要么 fork 项目，要么离开，以此终结了关于 AI 在 Linux 开发中角色的争论。 这一声明来自全球最大的协作式开源项目之一的创建者和最高维护者，终结了关于 Linux 内核开发中使用 AI 生成代码的持续争论。它标志着开源社区的一个重要文化和技术的里程碑，表明 AI 作为一种合法的开发工具已获得主流认可。 Torvalds 指出，尽管在一年前 AI 的有用性还存在疑问，但今天已不再有争议，同时他承认围绕 AI 的更广泛经济问题仍然悬而未决。他动用了最高维护者的权威划定了明确界线，为反对者提供了 fork 代码库这一传统开源路径。

rss · Simon Willison · 7月16日 13:26

**背景**: Linus Torvalds 是 Linux 内核的创建者和主要开发者，担任其最高维护者，对哪些代码被纳入项目拥有最终决定权。Linux 内核通过层级化的维护者系统进行开发，贡献代码在到达 Torvalds 之前需经过子系统维护者的审核。在开源软件中，fork 是指创建项目的副本以独立开发，当贡献者对项目方向存在分歧时，开源许可证允许这种做法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.kernel.org/doc/html/latest/process/maintainers.html">List of maintainers — The Linux Kernel documentation</a></li>
<li><a href="https://en.wikipedia.org/wiki/Fork_(software_development)">Fork (software development) - Wikipedia</a></li>
<li><a href="https://lkml.org/">LKML.ORG - the Linux Kernel Mailing List Archive</a></li>

</ul>
</details>

**标签**: `#linux`, `#open-source`, `#ai`, `#linus-torvalds`, `#kernel-development`

---

<a id="item-3"></a>
## [欧盟裁定谷歌必须向竞争对手开放 Android 与搜索数据](https://www.theverge.com/policy/966438/eu-google-android-ai-interoperability-search-data-dma) ⭐️ 9.0/10

欧盟委员会根据《数字市场法》发布了两项具有法律约束力的决定，要求谷歌向符合条件的竞争对手开放 Android 部分系统功能和 Google Search 数据。ChatGPT、Claude 等竞争对手的 AI 助手将获得与谷歌 Gemini 同等的系统级权限和数据访问能力，实现此前仅限谷歌自有服务享有的深度系统集成。 这项裁定从根本上重塑了欧盟移动 AI 助手格局，打破了谷歌在 Android 平台上的优势，并开放了长期作为竞争壁垒的搜索数据。这可能催生 Google Search 和 Gemini 的真正替代品，促进欧洲搜索引擎和 AI 助手市场的竞争。 谷歌可以依据隐私和安全标准评估申请访问 Android 功能的服务，但相关限制须符合欧盟规定，以确保不会成为访问壁垒。欧盟将限制共享数据的使用方式，搜索数据的访问将以 FRAND（公平、合理、非歧视）条款提供。

telegram · zaihuapd · 7月16日 13:19

**背景**: 《数字市场法》（DMA）是欧盟立法，旨在通过防止大型平台公司（"守门人"）滥用市场支配地位来确保数字市场的竞争。根据 DMA，谷歌、苹果和 Meta 等守门人必须履行义务，允许互操作性和竞争对手的公平访问。谷歌被指定为 Android 和 Google Search 等多个核心平台服务的守门人，从而触发了向第三方竞争对手开放这些服务的要求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Digital_Markets_Act">Digital Markets Act - Wikipedia</a></li>
<li><a href="https://digital-markets-act.ec.europa.eu/about-dma_en">About the Digital Markets Act - European Union</a></li>
<li><a href="https://auto-post.io/blog/eu-presses-google-to-open-gemini-access-under-dma">EU Presses Google to Open Gemini Access Under DMA</a></li>

</ul>
</details>

**标签**: `#EU-DMA`, `#Google`, `#Android`, `#AI-Assistants`, `#Regulation`

---

<a id="item-4"></a>
## [Kimi 发布 K3：2.8 万亿参数开源模型，支持 100 万上下文](https://platform.kimi.com/docs/guide/kimi-k3-quickstart) ⭐️ 9.0/10

Kimi 发布了 K3 模型，这是一个拥有 2.8 万亿参数的开源模型，支持 100 万 token 上下文窗口并原生具备视觉理解能力。该模型采用稀疏 MoE 架构和 Kimi Delta Attention，在 896 个专家中激活 16 个，声称综合性能仅次于 Claude Fable 5 和 GPT-5.6 Sol。 此次发布代表了开源模型在扩展效率方面的重大进步，在保持开放性的同时实现了接近前沿的性能。向 Kimi Delta Attention 和稀疏 MoE 的架构转变展示了大规模模型高效部署的可行路径，可能影响开源与专有 AI 模型之间的竞争格局。 K3 通过 896 个专家（激活 16 个）的稀疏 MoE 设计，相比 K2 实现了约 2.5 倍的扩展效率提升。该模型采用 Kimi Delta Attention (KDA) 与 Attention Residuals 架构，其编程能力为 Kimi 系列最强，可处理大型代码库并自主恢复错误。API 定价为每百万 token 缓存命中输入 ¥2.0、缓存未命中输入 ¥20.0、输出 ¥100.0。

telegram · zaihuapd · 7月16日 13:47

**背景**: Kimi Delta Attention (KDA) 是一种表达力强的线性注意力模块，通过更细粒度的门控机制扩展了 Gated DeltaNet，能够更有效地利用有限的有限状态 RNN 内存。该架构采用 3:1 的 KDA 层与完整 Multi-Head Latent Attention (MLA) 层交替比例，在计算成本和表达力之间提供最佳平衡。Mixture of Experts (MoE) 是一种将计算拆分为多个专家子网络的架构模式，通过每个 token 仅激活部分专家，使模型能够在保持计算效率的同时显著扩展参数规模。Attention Residuals (AttnRes) 用对前层输出的 softmax 注意力替代固定累加，使每层能够以学习到的、依赖输入的权重选择性地聚合早期表示。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2510.26692">[2510.26692] Kimi Linear: An Expressive, Efficient Attention Architecture</a></li>
<li><a href="https://arxiv.org/abs/2603.15031">[2603.15031] Attention Residuals - arXiv.org</a></li>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained - Hugging Face</a></li>

</ul>
</details>

**社区讨论**: 社区讨论提出了对中国相关话题可能存在客户端内容过滤的担忧，指出模型可能具有无偏见的知识，但过滤是在前端应用的。用户还注意到 Moonshot 的服务条款允许使用 API 使用数据进行训练，需要企业协议才能限制数据使用。一位评论者观察到，中国实验室似乎正在推动智能的商品化，可能是为了销售硬件和基础设施，而非将软件作为主要价值驱动因素，尽管这仍然涉及大量投资且回报不确定。

**标签**: `#LLM`, `#Open-Source`, `#Kimi`, `#MoE`, `#AI Models`

---

<a id="item-5"></a>
## [Roc 编译器从 Rust 重写为 Zig：进展与权衡](https://rtfeldman.com/rust-to-zig) ⭐️ 8.0/10

Richard Feldman 和 Roc 团队分享了将编译器从 Rust 重写为 Zig 的详细进展报告，涵盖了转型过程中的权衡、收益和挑战。此次重写恰逢 AI 编程助手的兴起，团队还报告了切换以来的内存损坏事件。 这次重写为社区提供了罕见的数据，展示了在复杂系统项目中，Rust 的编译时内存安全保证与 Zig 的手动内存管理方式之间的权衡。这一经验为开发者生产力、增量构建性能，以及放弃 Rust 借用检查器后内存安全漏洞的实际频率提供了具体参考。 团队强调 Zig 的增量构建显著提升了开发效率，同时指出编译器中如二进制补丁和代码热重载等任务本身就需要 unsafe 操作。一个关键争议在于 Zig 的 ReleaseSafe 模式，该模式提供运行时检查来捕获部分内存错误，但可能无法像 Rust 的编译时借用检查器那样捕获所有 use-after-free 场景。

hackernews · jorangreef · 7月16日 11:39 · [社区讨论](https://news.ycombinator.com/item?id=48933149)

**背景**: Roc 是一门函数式编程语言，其编译器最初用 Rust 编写，后被重写为 Zig。Zig 是一门通用系统编程语言，强调手动内存管理、简洁性和性能，与 Rust 在编译时通过借用检查器强制内存安全的方式形成对比。Rust 与 Zig 在编译器实现上的争论是行业内关于安全保证与开发者控制权之间平衡的更广泛讨论的一部分，历史上 Rust 自身的编译器最初也是用 OCaml 编写的。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://rtfeldman.com/rust-to-zig">How Our Rust - to - Zig Rewrite is Going</a></li>
<li><a href="https://gotopia.tech/sessions/4107/roc-and-zig-a-compiler-rewrite-story">Roc & Zig : A Compiler Rewrite Story | gotopia.tech</a></li>
<li><a href="https://blog.logrocket.com/comparing-rust-vs-zig-performance-safety-more/">Comparing Rust vs . Zig : Performance, safety , and... - LogRocket Blog</a></li>

</ul>
</details>

**社区讨论**: 评论者就生成机器码是否真的需要 unsafe 操作展开辩论，steveklabnik 认为常规编译不需要 unsafe，只有热二进制补丁才需要。对 Zig 的内存安全声明存在质疑，特别是 ReleaseSafe 是否真能捕获 use-after-free 错误，同时也有人质疑为何不选择 OCaml，考虑到其成熟度和在其他编译器中的应用。一些人承认 Zig 的增量构建是杀手级功能，但希望 Rust 最终能在不牺牲安全性的前提下提供类似能力。

**标签**: `#rust`, `#zig`, `#compilers`, `#systems-programming`, `#memory-safety`

---

<a id="item-6"></a>
## [xAI 在隐私事件后开源 Grok Build CLI 工具](https://simonwillison.net/2026/Jul/15/grok-build/#atom-everything) ⭐️ 8.0/10

xAI 的 Grok CLI 工具因在用户运行命令时将整个目录（包括 SSH 密钥和密码管理器数据库）上传至 xAI 的 Google Cloud 存储桶而引发重大隐私事件。作为回应，马斯克承诺彻底删除所有已上传的用户数据，xAI 于 7 月 12 日关闭默认数据保留功能，并在 GitHub 上以 Apache 2.0 许可证发布了完整的 Grok Build 代码库。 这一事件凸显了处理敏感开发者数据的 AI 编程工具所面临的严重信任与隐私风险，xAI 开源代码库的举措在 CLI 式 AI Agent 日益普及的行业中代表着迈向透明化的重要一步。该事件也表明社区反弹能多快地迫使大型 AI 公司改变其数据处理方式。 开源的 Grok Build 代码库包含 844,530 行 Rust 代码（仅约 3% 为第三方依赖），其中包含借鉴自其他编程 Agent 的工具实现（如 Codex 的 apply_patch 和 OpenCode 的 bash），以及一个自包含的终端 Mermaid 图表渲染器。该仓库目前仅有一个提交，无法提供开发历史洞察，且主 Agent 的系统提示词中值得注意的是缺少子 Agent 提示词中包含的

rss · Simon Willison · 7月15日 23:59

**背景**: Grok Build 是 xAI 推出的基于 CLI 的智能编程工具，允许开发者直接在终端中使用 Grok 模型完成软件的规划、构建、测试和部署，与 Claude Code、Codex CLI 和 Gemini CLI 等工具竞争。该工具最近更新至基于 Grok 4.5 运行，新增了原生子 Agent 视图、Plan Mode 集成和全屏终端 UI 等功能。代码发布所采用的 Apache 2.0 许可证是一种宽松的开源许可证，允许商业使用、修改和分发，限制极少。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://x.ai/cli">Grok Build | SpaceXAI</a></li>
<li><a href="https://www.eigent.ai/blog/grok-build-cli">Grok Build CLI Review 2026: Features, Comparisons & Alternatives</a></li>
<li><a href="https://en.wikipedia.org/wiki/Apache_License">Apache License - Wikipedia</a></li>

</ul>
</details>

**标签**: `#xAI`, `#Grok`, `#privacy`, `#open-source`, `#security`

---

<a id="item-7"></a>
## [长鑫年底产能逼近美光，中国将成全球第二大 DRAM 产地](https://www.tomshardware.com/pc-components/dram/cxmt-close-to-matching-microns-memory-capacity-in-2026-research-claims-would-put-china-on-track-to-become-worlds-second-largest-dram-producer) ⭐️ 8.0/10

Citrini Research 预测，长鑫存储有望在 2026 年底达到约 35 万片/月的 DRAM 产能，逼近美光的 37.5 万片/月，届时中国将成为全球第二大 DRAM 生产基地。包括昇维旭、晋华集成和长江存储子公司 XMC 在内的多家企业也在扩产，若全部投产，中国 DRAM 总产能将达 60 万片/月（不含三星、SK 海力士在华工厂）。 这标志着全球半导体格局的重大转变，中国正迅速缩小与既有 DRAM 领导者的差距，可能重塑全球供应链格局。然而，扩产面临光刻设备的关键瓶颈，分析师指出，尽管中国新增产能有助于稳定价格，但主要满足国内需求，难以完全消除预计到 2030 年约 25%的全球 DRAM 供应缺口。 报告预计，到 2030 年中国 DRAM 总产能将增至约 141 万片/月，其中长鑫存储单独可达 95 万片/月。关键风险因素是美国 MATCH 法案，该法案可能限制先进浸没式 DUV 光刻设备对华出口，从而阻碍短期扩产计划。

telegram · zaihuapd · 7月16日 02:30

**背景**: 长鑫存储（CXMT）成立于 2016 年，总部位于中国合肥，是一家一体化 DRAM 制造商，近年来快速扩产并于 2025 年初开始销售 DDR5 SDRAM。全球 DRAM 市场目前由三星、SK 海力士和美光主导，而浸没式 DUV 光刻设备（主要由 ASML 供应）是相关制程节点 DRAM 制造的关键设备。美国提出的 MATCH 法案（多边技术与硬件管控法案）旨在限制先进半导体设备对华出口，可能影响长鑫获取扩产所需的光刻设备。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/ChangXin_Memory_Technologies">ChangXin Memory Technologies - Wikipedia</a></li>
<li><a href="https://semi-connect.net/match/">対中輸出規制「 MATCH ... | semi-connect</a></li>

</ul>
</details>

**标签**: `#semiconductors`, `#DRAM`, `#CXMT`, `#supply-chain`, `#China`

---

<a id="item-8"></a>
## [日本购 2.75 万块英伟达 Rubin 芯片打造机器人主权 AI](https://www.bloomberg.com/news/articles/2026-07-16/japan-to-buy-nvidia-rubin-chips-to-build-sovereign-ai-for-robots) ⭐️ 8.0/10

日本计划购入 27,500 块英伟达下一代 Rubin 芯片，由新成立的 Noetra 公司牵头建设大型数据中心，开发面向机器人的本土基础 AI 模型。该项目获得日本政府 3,873 亿日元（约 24 亿美元）拨款，软银、丰田支持的 Preferred Networks、NEC 等企业参与组建与运营，计划明年 3 月发布首个 AI 模型，并在数年内推出机器人专用版本。 这是针对机器人领域最大规模的主权 AI 基础设施国家级投资之一，旨在打造除中美之外的 英伟达 Rubin 平台于 2024 年 Computex 上发布，专为可扩展 AI 推理和智能体系统设计，包含名为 Rubin 的 GPU 和名为 Vera 的 CPU，由台积电制造。Noetra 前身为

telegram · zaihuapd · 7月16日 10:59

**背景**: 主权 AI 指一个国家或组织利用自身基础设施、数据、模型和人才，独立开发、部署和治理人工智能的能力，而非直接拥有技术。英伟达 Rubin 微架构是该公司继 Blackwell 之后的下一代 GPU 平台，专为满足智能体 AI 系统的低延迟和大上下文需求而设计。日本一直在推进主权 AI 作为国家战略的一部分，政府通过 NEDO 提供大量资金支持本土 AI 基础模型开发，以减少对外国技术的依赖。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Rubin_(microarchitecture)">Rubin (microarchitecture) - Wikipedia</a></li>
<li><a href="https://www.mckinsey.com/featured-insights/mckinsey-explainers/what-is-sovereign-ai">What is sovereign AI? | McKinsey</a></li>
<li><a href="https://www.datamintelligence.com/news/japan-noetra-ai-robotics-plan-10-million-robots-by-2040">Japan Noetra AI Robotics Plan to Deploy 10... | Datam Intelligence</a></li>

</ul>
</details>

**标签**: `#nvidia`, `#sovereign-ai`, `#robotics`, `#japan`, `#ai-infrastructure`

---

<a id="item-9"></a>
## [微软 Comic Chat 已开源](https://opensource.microsoft.com/blog/2026/07/16/microsoft-comic-chat-is-now-open-source/) ⭐️ 7.0/10

2026 年 7 月 16 日，微软将 Comic Chat 的源代码作为开源项目发布。Comic Chat 是一款图形化 IRC 客户端，最初于 1996 年随 Internet Explorer 3.0 一起发布。此次开源发布由 Robert Standefer 推动，并得到了 Scott Hanselman 的支持，但原始开发者是微软研究员 David Kurlander。 Comic Chat 是互联网历史上的一件重要遗产，它将基于文本的 IRC 对话独特地可视化为漫画条，其开源为后代保存了一个重要的文化产物。此次发布还引发了关于早期 IRC 协议扩展和客户端创意设计理念的高质量社区讨论。 Comic Chat 通过添加自定义扩展来显式指示角色外观和情感动作，从而扩展了 IRC 协议，当时一些 IRC 用户将这些扩展视为非标准的协议修改。原始开发者还撰写了一篇关于漫画布局引擎设计的学术论文，该论文被收录在 ACM Digital Library 中。

hackernews · jervant · 7月16日 16:06 · [社区讨论](https://news.ycombinator.com/item?id=48936426)

**背景**: Microsoft Comic Chat 是一款于 1996 年首次发布的图形化 IRC 客户端，能够自动将基于文本的聊天对话转换为带有角色、表情和对话气泡的漫画条面板。它由 David Kurlander 在微软研究院的虚拟世界组以及后来微软互联网部门的一个团队中开发。IRC（Internet Relay Chat）是一种为频道中的群组通信而设计的基于文本的聊天协议，Comic Chat 的独特之处在于通过专有功能扩展了标准 IRC 协议，以支持角色和情感元数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Microsoft_Comic_Chat">Microsoft Comic Chat</a></li>
<li><a href="https://opensource.microsoft.com/blog/2026/07/16/microsoft-comic-chat-is-now-open-source/">Microsoft Comic Chat is now open source | Microsoft Open Source...</a></li>
<li><a href="https://en.wikipedia.org/wiki/IRC_client">IRC client</a></li>

</ul>
</details>

**社区讨论**: 讨论中出现了促成此次开源发布的 Robert Standefer，他澄清自己并非原始开发者，并讲述了跨越六年促成开源的故事。其他评论者分享了与该软件的个人渊源，包括一位受 Comic Chat 启发而创建漫画制作初创公司的创始人，以及关于其 IRC 协议扩展在历史上被部分 IRC 社区视为非标准的技术观点。

**标签**: `#open-source`, `#microsoft`, `#internet-history`, `#irc`, `#retro-computing`

---

<a id="item-10"></a>
## [OnePlus 停止在欧洲和北美推出新产品](https://community.oneplus.com/thread/2170715118587871237) ⭐️ 7.0/10

OnePlus 宣布将不再在欧洲和北美推出新产品，但将继续为现有设备在承诺的支持期内提供软件更新和安全补丁。公司澄清称，这是结束新产品发布，而非完全停止所有运营。 对于一个曾是 Android 爱好者宠儿的品牌来说，这标志着其从西方市场的重大撤退，也表明智能手机市场已变得极其竞争和饱和。这也引发了关于中国智能手机品牌在监管和竞争压力下能否在欧洲和北美维持存在的疑问。 现有 OnePlus 设备将在 OPPO 的支持下继续获得预定的软件更新和安全补丁，履行对每台设备最初承诺的支持期。该公告专门针对欧洲和北美，暗示其他地区可能仍会推出新产品。

hackernews · pilililo2 · 7月16日 10:14 · [社区讨论](https://news.ycombinator.com/item?id=48932539)

**背景**: OnePlus 于 2013 年由裴宇（Carl Pei）和刘作虎创立，最初以"Never Settle"为品牌定位，提供接近原生的 Android 系统、顶配硬件规格、解锁的 bootloader 以及出厂镜像，价格具有竞争力，深受科技爱好者和极客青睐。多年来，该品牌逐渐偏离了其极客根基，向主流中国手机厂商的方向靠拢。裴宇最终离开 OnePlus，创立了新的消费电子公司 Nothing。OnePlus 作为子公司运营，由 OPPO 提供支持，共享资源和技术。

**社区讨论**: 评论者指出标题被编辑化了——OnePlus 是停止新产品发布，而非停止所有运营，现有设备仍将获得支持。前员工描述了严苛的 996 工作文化（早 9 点到晚 9 点，每周六天）以及人员流失，而老粉丝则感叹该品牌从拥有解锁 bootloader 和出厂镜像的极客首选，变成了又一个主流中国手机厂商。有人指出裴宇的新公司 Nothing 延续了 OnePlus 最初的许多理念，即高性价比和优质 Android 体验。

**标签**: `#oneplus`, `#smartphones`, `#business`, `#android`, `#consumer-electronics`

---

<a id="item-11"></a>
## [Codex Bug 在无沙箱保护下删除用户$HOME 目录](https://simonwillison.net/2026/Jul/16/bad-codex-bug/#atom-everything) ⭐️ 7.0/10

Thibault Sottiaux 披露，在 Codex 中运行的 GPT-5.6 一直在意外删除用户的$HOME 目录。该 Bug 在启用完全访问模式且未开启沙箱保护时出现，模型试图覆盖$HOME 环境变量以设置临时目录，却误将$HOME 本身删除。 这一事件凸显了开发者使用自主 AI 编程代理时面临的严重操作风险：在没有适当沙箱隔离的情况下，模型的一个诚实错误就可能摧毁不可替代的用户数据。它强调，在运行具有文件系统访问权限的 AI 代理时，沙箱隔离不是可选项而是必需品，因为幻觉或错误命令可能危及整个系统。 该 Bug 的具体触发条件是：启用了完全访问模式，同时禁用了沙箱保护和自动审查。模型的意图是良性的——它试图覆盖$HOME 来定义一个临时工作目录——但在命令构造中的一个诚实错误导致删除了用户的家目录而非临时目录。

rss · Simon Willison · 7月16日 17:45

**背景**: Codex 是一种 AI 编程代理，可以在用户机器上执行任意 shell 命令、安装软件包和修改文件。Linux 上的沙箱工具如 bubblewrap（bwrap）限制进程能看到和能做的事情，而 seccomp/BPF 提供系统调用过滤。在类 Unix 系统中，$HOME 环境变量指向当前用户的家目录，其中包含个人文件、配置和数据。如果没有沙箱隔离，任何具有文件系统访问权限的 AI 代理都可能发出如 rm -rf 等破坏性命令，影响整个系统。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://amux.io/guides/ai-agent-sandboxing/">AI Agent Sandboxing in 2026: Docker, E2B, Firecracker... — amux</a></li>
<li><a href="https://instavm.io/blog/how-claude-code-and-codex-approach-sandboxing">How Claude Code & Codex approach sandboxing | InstaVM</a></li>
<li><a href="https://en.wikipedia.org/wiki/Environment_variable">Environment variable - Wikipedia</a></li>

</ul>
</details>

**标签**: `#codex`, `#coding-agents`, `#ai-safety`, `#generative-ai`, `#operational-risk`

---

<a id="item-12"></a>
## [AI 记忆架构是否在为错误的抽象层做优化？](https://www.reddit.com/r/MachineLearning/comments/1uy6yht/are_current_ai_memory_architectures_optimizing/) ⭐️ 7.0/10

一篇 Reddit 讨论帖提出，当前 AI 记忆系统在错误的抽象层上进行优化，专注于存储描述性事实而非推断更高层次的认知模式。作者建议，持久化上下文应从存储"用户从事工程工作"这类事实，进化为推断"用户倾向于通过反馈循环和交互来理解复杂系统"这类推理风格。 这一概念性重构触及了持久化上下文系统中的根本设计问题，可能重塑 AI 智能体构建长期用户模型的方式。如果被采纳，这种转变将使 AI 系统更具适应性和个性化，从静态事实检索转向更好地映射人类理解和解释问题方式的动态认知建模。 该帖子提出了一个开放性问题：更高层次的认知表示是否能从足够强大的 AI 系统中自然涌现，还是需要根本不同的架构。当前记忆系统依赖于保存的记忆、对话摘要和用户偏好等机制，而所提出的方法需要将持久化上下文持续精炼和重构为用户解释框架和偏好抽象的不断演进的模型。

reddit · r/MachineLearning · /u/Boris_Ljevar · 7月16日 16:00

**背景**: 当前 AI 记忆系统作为模型临时上下文窗口与智能体长期所需的持久化结构化信息之间的层，通常使用向量嵌入、Postgres 或 Redis 等数据库以及检索机制来实现。这些系统处理会话持久化、跨会话学习和选择性上下文访问，但主要存储描述性事实，如用户偏好和对话摘要。该讨论建立在这样一个观察之上：即使前沿模型拥有巨大的上下文窗口，记忆架构对于构建连贯的长期用户模型和基于过去交互进行适应仍然是必不可少的。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.mindstudio.ai/blog/ai-memory-system-persistent-context-agents">What Is an AI Memory System? How to Build Persistent Context for Your Agents | MindStudio</a></li>
<li><a href="https://redis.io/blog/ai-agent-memory-stateful-systems/">AI agent memory: types, architecture & implementation</a></li>
<li><a href="https://www.ibm.com/think/topics/ai-agent-memory">What Is AI Agent Memory? | IBM</a></li>

</ul>
</details>

**标签**: `#AI Memory`, `#Persistent Context`, `#Cognitive Architectures`, `#Machine Learning`, `#LLM`

---

<a id="item-13"></a>
## [xAI 起诉用户滥用 Grok 生成儿童性虐待深度伪造](https://www.reuters.com/legal/litigation/musks-xai-sues-grok-user-over-sexualized-deepfakes-2026-07-15/) ⭐️ 7.0/10

马斯克旗下 xAI 已对南卡罗来纳州男子 Terry Harwood 提起诉讼，指控其滥用聊天机器人 Grok 生成儿童性虐待材料和非自愿成人色情深度伪造。xAI 在德州联邦法院提交的诉讼中称，Harwood 上传非性图片并要求系统生成露骨内容，违反了服务条款。 这是首批 AI 公司因用户生成滥用深度伪造内容而直接起诉用户的案件之一，在 AI 治理领域确立了重要的法律先例。这表明 AI 提供商愿意通过诉讼手段对恶意使用行为执行服务条款，可能影响整个行业处理内容审核和用户问责的方式。 xAI 正在寻求赔偿并申请法院永久禁止 Harwood 使用 Grok，该公司报告称今年已暂停 52,222 个账户，向国家失踪与受虐儿童中心举报 73,604 次，促成至少 244 人被捕。Harwood 已于今年 2 月因性剥削未成年人指控被捕。

telegram · zaihuapd · 7月16日 01:45

**背景**: Grok 是由 xAI 开发并于 2023 年 11 月推出的生成式 AI 聊天机器人，与 X 社交网络集成，具备图像和视频生成能力。联邦《TAKE IT DOWN Act》于 2025 年 5 月成为法律，将非自愿发布真实或深度伪造性图像定为重罪，当受害者为儿童时处罚更为严厉。美国多个州也已立法为非自愿色情材料的受害者提供法律救济。此次诉讼代表了一种新的执法方式，即由 AI 公司本身而非受害者对滥用者提起法律诉讼。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Grok_(chatbot)">Grok (chatbot) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/TAKE_IT_DOWN_Act">TAKE IT DOWN Act - Wikipedia</a></li>
<li><a href="https://www.criminaldefenselawyer.com/resources/is-deepfake-pornography-illegal.html">Is Deepfake Pornography Illegal? Federal and State Laws</a></li>

</ul>
</details>

**标签**: `#xAI`, `#Grok`, `#AI Governance`, `#Deepfakes`, `#Legal Precedent`

---

<a id="item-14"></a>
## [知网将下架将 DeepSeek 等 AI 列为作者的论文](https://www.zaobao.com.sg/news/china/story20260716-9371836) ⭐️ 7.0/10

中国最大的学术数据库知网宣布，将下架并把 DeepSeek、Gemini 等 AI 工具列为作者的论文，并明确不再接受此类论文。知网表示，AI 不具备民事主体资格，无法承担论文真实性、学术核查和追责等责任。 知网作为中国最具影响力的学术平台，此项政策为 AI 在学术出版中的角色划定了明确界限，强化了只有人类研究者才能承担署名责任的原则。这反映了学术界关于 AI 伦理的全球性讨论，可能影响其他数据库和期刊对 AI 辅助研究的处理方式。 知网明确规定，虽然 AI 不能作为署名作者，但研究者在研究或写作过程中使用 AI 工具的，应在论文的研究方法或致谢部分予以说明。该政策适用于包括 DeepSeek、Gemini 在内的各类 AI 工具和大语言模型。

telegram · zaihuapd · 7月16日 07:45

**背景**: 知网（CNKI）是中国最大的学术数据库，运营着学术期刊、会议论文、报纸和专利文献等多种数据库。DeepSeek 是中国于 2023 年 11 月首次发布的 AI 模型系列，以其编程和推理能力著称。随着 DeepSeek、Gemini 等 AI 工具在学术研究中的使用日益增多，AI 是否可以作为论文作者的问题在学术界引发了广泛讨论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek">DeepSeek - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/CNKI">CNKI - Wikipedia</a></li>

</ul>
</details>

**标签**: `#AI Ethics`, `#Academic Publishing`, `#CNKI`, `#DeepSeek`, `#AI Authorship`

---

<a id="item-15"></a>
## [美国 ITC 启动 DRAM 专利 337 调查，三星、英伟达、谷歌等被列为被告](https://www.cls.cn/detail/2428105) ⭐️ 7.0/10

7 月 15 日，美国国际贸易委员会（ITC）投票决定对特定 DRAM 设备及其下游产品启动 337 调查（案件编号 337-TA-1511），被告包括三星电子、英伟达、谷歌、博通和超微电脑。该调查源于 Netlist 公司提出的专利侵权投诉，涉及 DDR5 DIMM、高带宽内存（HBM）以及采用这些存储器的服务器、计算和存储系统。 这项调查直接针对 AI 训练、高性能计算和数据中心基础设施所需的关键存储组件，可能扰乱主要云服务和 AI 硬件提供商的供应链。如果 ITC 最终裁定侵权并发布排除令，可能导致美国市场上 AI 服务器和数据中心设备出现供货延迟或成本上升。 调查明确涵盖 DDR5 DIMM 模块和 HBM 技术，两者都是现代 AI 加速器和高性能服务器的核心组件。虽然手机和显卡等消费产品短期内不太可能受到价格影响，但主要风险落在依赖这些存储技术的大规模服务器制造商、云服务提供商和企业客户身上。

telegram · zaihuapd · 7月16日 08:34

**背景**: 1930 年关税法第 337 条授权美国国际贸易委员会调查不公平进口行为，最常见的是涉及进口商品专利侵权的指控。DDR5 是第五代双倍数据速率同步动态随机存取存储器，相比 DDR4 提供更高的性能和效率，广泛应用于现代服务器和计算系统。高带宽内存（HBM）通过垂直堆叠 DRAM 芯片层来提供远超传统内存的带宽，使其成为 AI 加速器和高性能计算封装中的主流存储选择，在这些场景中存储带宽是关键瓶颈。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.usitc.gov/about_section_337.htm">About Section 337 - United States International Trade Commission</a></li>
<li><a href="https://en.wikipedia.org/wiki/High_Bandwidth_Memory">High Bandwidth Memory - Wikipedia</a></li>
<li><a href="https://www.kingston.com/en/blog/pc-performance/ddr5-overview">DDR5 Memory Standard: An introduction to the next generation ...</a></li>

</ul>
</details>

**标签**: `#DRAM`, `#patent-dispute`, `#AI-hardware`, `#supply-chain`, `#ITC`

---

<a id="item-16"></a>
## [台积电再投千亿美元赴美设厂，二季度利润飙升 77%创历史新高](https://www.reuters.com/world/asia-pacific/tsmcs-second-quarter-profit-seen-hitting-record-ai-boom-2026-07-15/) ⭐️ 7.0/10

台积电宣布向亚利桑那州制造业务追加投资 1000 亿美元，使在美总投资承诺达到约 2650 亿美元，同时公布二季度净利润达 7066 亿新台币（约 220 亿美元），同比增长 77%，远超市场预期的 6326 亿新台币。公司还将 2026 年资本支出预测上调至 600 亿至 640 亿美元，并预计全年美元营收增长略超 40%。 这一双重公告表明，AI 驱动的半导体热潮正在加速而非降温，台积电的创纪录利润验证了超大规模云厂商和 AI 芯片设计商的持续需求。扩大的在美投资正在重塑全球半导体供应链，降低台湾地区的地理集中风险，同时使美国成为先进芯片制造的核心节点。 台积电亚利桑那州基地目前已有 8 座工厂在建或规划中，未来可能再增 4 座，目标涵盖 2 纳米、3 纳米和 4 纳米等先进制程技术。此次追加的 1000 亿美元是在此前已宣布的 1650 亿美元基础上的进一步扩大，公司 2026 年 600 亿至 640 亿美元的资本支出指引反映了对多年 AI 需求增长的信心。

telegram · zaihuapd · 7月16日 12:29

**背景**: 台积电是全球最大的半导体代工制造商，为英伟达、苹果和 AMD 等公司生产芯片，在先进制程节点上占据主导市场份额。公司于 2020 年首次宣布在亚利桑那州投资 120 亿美元，此后在中美地缘政治紧张局势、美国《芯片法案》政府激励措施以及 AI 加速器需求激增的推动下大幅扩张。台积电在亚利桑那州的先进工厂将采用 2 纳米、3 纳米和 4 纳米工艺制造芯片——这些技术对下一代 AI 和计算应用至关重要。公司还在德国德累斯顿运营一家合资企业（ESMC），专注于汽车和工业应用的特种工艺。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tsmc.com/static/abouttsmcaz/index.htm">TSMC Arizona - Taiwan Semiconductor Manufacturing Company ...</a></li>
<li><a href="https://wccftech.com/tsmc-stacks-its-us-pledge-to-265-billion-amidst-ai-chip-demand-to-build-four-new-arizona-plants/">TSMC Stacks its US Pledge to $265 Billion Amidst AI Chip Demand to...</a></li>
<li><a href="https://www.bloomberg.com/news/articles/2026-07-16/tsmc-beats-lofty-estimates-in-latest-sign-of-sustained-ai-demand">TSMC Beats Lofty Estimates in Latest Sign of Sustained AI Demand</a></li>

</ul>
</details>

**标签**: `#semiconductors`, `#TSMC`, `#AI`, `#manufacturing`, `#supply-chain`

---

<a id="item-17"></a>
## [1Password 推出 Claude 集成：AI 可代登录网站但全程不接触密码](https://9to5mac.com/2026/07/16/1password-now-lets-claude-sign-in-to-websites-without-seeing-your-passwords/) ⭐️ 7.0/10

1Password 正式上线与 Claude 的 Mac 端集成，用户可授权 AI 代理代为登录网站，而密码与二次验证码不会进入 Claude 的上下文、记忆或 Anthropic 的系统。凭证经安全通道直接注入目标网页，用户通过生物识别逐条审批当前任务所需的登录项，权限仅限当前会话。 这是安全 AI 代理自动化领域的重要一步，通过确保敏感数据对 LLM 零暴露，解决了 AI 处理凭证这一关键信任问题。通过安全通道注入凭证而不暴露给模型上下文的技术方案具有创新性，对 AI 代理自主执行网页任务这一更广泛的趋势意义重大。 该功能目前面向 Mac 的商业、家庭及个人版用户开放，需同时安装 1Password 与 Claude 的桌面应用及浏览器扩展。若自动填充后提交失败，已填内容会被立即擦除，后续还将支持支付卡和身份信息。

telegram · zaihuapd · 7月16日 15:54

**背景**: 随着 AI 代理越来越多地代替用户执行网页任务，一个主要挑战是如何安全处理认证凭证而不将其暴露给模型，因为模型可能容易受到提示注入攻击。1Password 的零暴露安全框架通过让 Claude 为每个任务向 1Password 请求凭证来解决这一问题，凭证通过安全通道直接流向目标网站，而非经过模型上下文。这一方案与传统凭证处理方式形成对比，后者可能将静态凭证存储或传递过可能被攻破的应用层。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.aol.com/articles/1password-anthropic-bring-secure-credential-130000000.html">1 Password and Anthropic Bring Secure Credential Access to Claude ...</a></li>
<li><a href="https://www.itpro.com/security/1password-teams-up-with-anthropic-to-give-claude-access-to-your-credentials">1 Password teams up with Anthropic to give Claude access to... | IT Pro</a></li>
<li><a href="https://www.zdnet.com/article/1password-claude-agentic-mode/">1 Password 's new Agentic Mode lets Claude log into your... | ZDNET</a></li>

</ul>
</details>

**标签**: `#AI Agents`, `#Security`, `#1Password`, `#Claude`, `#Authentication`

---
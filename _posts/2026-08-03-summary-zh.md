---
layout: default
title: "Horizon Summary: 2026-08-03 (ZH)"
date: 2026-08-03
lang: zh
---

> 从 34 条内容中筛选出 10 条重要资讯。

---

1. [OpenAI 展示人工智能在数学与理论计算机科学中的十项进展](#item-1) ⭐️ 8.0/10
2. [ComfyUI 首日支持 MiniMax H3 开放权重视频模型](#item-2) ⭐️ 8.0/10
3. [数据库研究专家 Andy Pavlo 加入 ClickHouse 并创立 ClickHouse Labs](#item-3) ⭐️ 8.0/10
4. [Rust 接受不可移动类型与保证析构的项目目标](#item-4) ⭐️ 8.0/10
5. [SQLite "严重" CVE 被发现是 LLM 生成的幻觉](#item-5) ⭐️ 8.0/10
6. [SemiAnalysis 深度解析：Kimi K3 的创新架构](#item-6) ⭐️ 8.0/10
7. [Qwen 发布 3.8-Max：2.4 万亿参数，首次开源 Max 级模型](#item-7) ⭐️ 8.0/10
8. [美国犯罪实验室 DNA 设备曝安全漏洞，30 年证据面临篡改风险](#item-8) ⭐️ 8.0/10
9. [英伟达 CMP 170HX 矿卡被破解：解锁 80GB 显存，二手价暴涨十倍](#item-9) ⭐️ 8.0/10
10. [苹果就英国政府 iCloud 加密后门要求提起新诉讼](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI 展示人工智能在数学与理论计算机科学中的十项进展](https://openai.com/index/ten-advances-in-mathematics/) ⭐️ 8.0/10

OpenAI 发布了一份报告，展示了其人工智能模型在数学和理论计算机科学领域取得的十项重要进展，涵盖高维球体填充、多色拉姆齐数以及形式化数学推理等方向。该公告表明，AI 系统现在已经能够以越来越高的自主性和准确性生成并验证数学证明。 这一进展标志着数学研究方式可能发生范式转变，AI 开始涉足此前由人类数学家独占的问题领域。形式化推理方面的快速进步可能加速数学、密码学和算法设计等领域的发现，同时也引发了关于人类数学家未来角色的紧迫讨论。 这十项进展涵盖组合数学、几何学和计算复杂性理论等多个子领域，其中高维球体填充和多色拉姆齐数等问题被描述为模型能够以令人惊讶的直觉性来处理。该工作利用了大语言模型既能提出候选解又能自我验证其有效性的能力，形成了一个可以收敛到正确证明的反馈循环。

hackernews · milkshakes · 8月3日 16:27 · [社区讨论](https://news.ycombinator.com/item?id=49157930)

**背景**: 形式化数学推理涉及构建可由计算机系统机械验证的证明，确保超越人类同行评审的逻辑严密性。传统上，人工智能在这方面表现不佳，因为它不仅需要模式匹配，还需要深层的逻辑一致性以及在可能的证明步骤的巨大搜索空间中导航的能力。大语言模型的最新进展，结合 Lean、Coq 等证明助手工具，开始弥合这一差距，使模型能够生成证明候选并对照形式化规范进行检查。

**社区讨论**: 社区情绪褒贬不一，从对指数级进步的兴奋到对人类数学家前景的悲伤都有。一些评论者认为任何可计算问题最终都会被计算机攻克，而另一些人则指出 AI 擅长通过暴力方法证伪猜想，但仍无法直觉性地提出新猜想。一位评论者仅表达了悲伤，捕捉到了看到人类多年智力劳动可能被颠覆的情感分量。

**标签**: `#AI`, `#mathematics`, `#theoretical-computer-science`, `#OpenAI`, `#formal-reasoning`

---

<a id="item-2"></a>
## [ComfyUI 首日支持 MiniMax H3 开放权重视频模型](https://blog.comfy.org/p/minimax-h3-day-0-support-in-comfyui) ⭐️ 8.0/10

ComfyUI 宣布首日支持 MiniMax H3，这是一个具备原生音频合成和 2K 视频输出能力的开放权重视频生成模型。团队开发了一种新颖的调制权重剪枝技术，将模型约 40% 的参数替换为功能等效的查找表，使全精度下的总内存占用从 123.6 GB 降至 42.5 GB，减少了 66%。 这一突破使得具备原生音频的下一代 2K 视频模型能够在 RTX 3060 等消费级 GPU 上本地运行，大幅降低了高质量 AI 视频生成的门槛。调制权重剪枝方法在技术上具有创新性，可能适用于包括 LLM 在内的其他大模型，其意义超越了视频生成领域。 剪枝技术针对占总参数约 40% 的调制权重，用查找表替换且不损失输出质量。结合 ComfyUI 的动态 VRAM 卸载功能，42.5 GB 的最小模型变体可在 16GB RTX 3060 上运行，但生成时间仍然较长——一位用户报告在 4070 Ti Super 上生成 10 秒 480p 视频需要 10 分钟。

hackernews · vblanco · 8月3日 13:34 · [社区讨论](https://news.ycombinator.com/item?id=49155629)

**背景**: MiniMax H3 是来自 Hailuo AI 的多模态 AI 视频生成与编辑模型，将文本、图像、视频和音频整合到统一的创作上下文中，支持文本生成视频、图像生成视频和视频转换等工作流。ComfyUI 是一个基于节点的 AI 图像和视频生成工作流构建界面，因其本地执行能力和可扩展性而广受欢迎。权重剪枝是一种成熟的神经网络压缩技术，但将调制权重剪枝为查找表的具体方法代表了一种针对现代视频扩散模型架构的新颖应用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hailuoai.video/tools/minimax-h3">MiniMax H 3 Multimodal AI Video Model | Hailuo AI</a></li>
<li><a href="https://comfyui.com/">ComfyUI</a></li>
<li><a href="https://www.klingmotion.com/minimax-h3">MiniMax H 3 AI Video Generator - Create 2K Videos with audio</a></li>

</ul>
</details>

**社区讨论**: 社区反响热烈，用户称赞模型的输出质量——一位在 4070 Ti Super 上运行的用户称结果'令人惊叹'，另一位用户指出鼠标渲染片段代表了 SOTA 视频生成的重大飞跃。技术讨论集中在调制权重剪枝方法是否可应用于 LLM，有人质疑'无损'的说法是否过于理想化。在技术赞誉之外也出现了审美批评，一位评论者认为输出'平淡乏味且千篇一律'，其他人注意到某些片段仍存在 AI 平滑伪影。

**标签**: `#AI video generation`, `#ComfyUI`, `#model optimization`, `#open weights`, `#local inference`

---

<a id="item-3"></a>
## [数据库研究专家 Andy Pavlo 加入 ClickHouse 并创立 ClickHouse Labs](https://clickhouse.com/blog/andy-pavlo-joins-clickhouse) ⭐️ 8.0/10

卡内基梅隆大学（CMU）著名数据库系统研究员兼教授 Andy Pavlo 已加入 ClickHouse，负责创立 ClickHouse Labs，这一新举措旨在将学术数据库研究与工业界开发相结合。对于这位数据库系统研究与教育领域最具影响力的人物之一而言，这是一次重要的职业转变。 这一举动标志着学术数据库研究与商业 OLAP 数据库行业的显著融合，有可能加速 ClickHouse 分析型数据库技术的创新。它同时也表明 ClickHouse 有意投资基础研究，这可能会重塑快速 OLAP 数据库的竞争格局，影响包括 StarRocks 和 Trino 在内的产品。 ClickHouse 是一款开源的列式数据库管理系统，专为使用 SQL 查询进行实时分析处理（OLAP）而设计。Pavlo 因其在 CMU 的数据库系列课程而广为人知，该课程已教育了全球数千名学生和从业者，他的研究还涵盖查询优化和数据库架构等主题。

hackernews · nikolay_sivko · 8月3日 14:09 · [社区讨论](https://news.ycombinator.com/item?id=49156011)

**背景**: Andy Pavlo 是卡内基梅隆大学的副教授，也是数据库管理系统领域最具影响力的研究者之一，以查询优化、自治数据库系统方面的研究以及广受欢迎的开放数据库课程讲座而闻名。ClickHouse 是一款快速的开源列式 OLAP 数据库，最初由 Yandex 开发，现由 ClickHouse Inc. 维护，广泛用于实时分析工作负载。OLAP 数据库市场正在快速发展，ClickHouse、StarRocks 和 Trino 等产品在性能、可扩展性和架构方法（如存算分离）方面展开激烈竞争。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/ClickHouse">ClickHouse - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Online_analytical_processing">Online analytical processing - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 社区反响非常积极，许多评论者赞扬了 Pavlo 在 CMU 的系列课程，并对学术研究与工业界的融合表示兴奋。一位评论者提出了一个有趣的技术问题，探讨快速 OLAP 产品（StarRocks、ClickHouse）与 Trino 在存算分离架构上的趋同，以及对数据摄入和索引的影响。另一位评论者呼吁 Pavlo 推动 ClickHouse 资助学术数据库研究，指出 AI 资金涌入和政府资助的混乱使得数据库研究几乎得不到支持。

**标签**: `#databases`, `#clickhouse`, `#olap`, `#database-research`, `#industry`

---

<a id="item-4"></a>
## [Rust 接受不可移动类型与保证析构的项目目标](https://github.com/rust-lang/rust-project-goals/blob/main/src/2026/move-trait.md) ⭐️ 8.0/10

Rust 已接受一项 2026 年项目目标，将不可移动类型（!Move）和保证析构器（!Forge）实现为类型级别的属性，从而摆脱当前基于 Pin 的方案。该提案基于 Yoshua Wuyts 的工作，旨在将不可移动性作为类型的属性而非位置的属性，并最终可能完全弃用 Pin。 这填补了 Rust 类型系统中自 2016 年左右以来就存在的重大缺陷——当时不可移动类型已被认识到至关重要，但被认为在不破坏一切的前提下难以添加。如果实现，它将支持安全的自引用结构体、安全的 scoped spawn（通过 !Forge 保证析构器运行），并通过消除备受批评的 Pin hack 显著改善 async 的人体工程学。 !Move trait 标记创建后不可移动的类型，而 !Forge 确保类型的析构器保证运行且无法通过 mem::forget 绕过，这正是解锁安全 scoped spawn 的关键。项目目标文档还提到了 !Destruct（"必须移动类型"/线性类型），其中处置一个值需要调用一个按值接收它的函数，而非隐式 drop。withoutboats 提出的竞争方案则主张将不可移动性作为位置/引用的属性而非类型的属性。

hackernews · paavohtl · 8月3日 06:42 · [社区讨论](https://news.ycombinator.com/item?id=49152023)

**背景**: Rust 的 Pin 机制是作为不可移动类型缺失的权宜之计引入的，通过包装指针来防止值在内存中被移动。这之所以必要，是因为 async future 是自引用的——它们包含内部指针，如果 future 被移动，这些指针就会失效。Pin 需要使用 unsafe 代码才能正确实现，且被广泛认为在人体工程学上存在困难，因此社区一直在推进 "pin ergonomics" 相关工作。不可移动类型的概念最初由 Zoxc 在 RFC #1858 中提出，但长期以来被认为无法在不破坏现有代码的情况下向后添加到 Rust 中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://internals.rust-lang.org/t/immovable-types-and-self-referencing-structs/6597">Immovable types and self-referencing structs - language design - Rust Internals</a></li>
<li><a href="https://blog.yoshuawuyts.com/self-referential-types">Ergonomic Self-Referential Types for Rust</a></li>
<li><a href="https://doc.rust-lang.org/std/pin/struct.Pin.html">Pin in std::pin - Rust</a></li>

</ul>
</details>

**社区讨论**: 社区成员强调这只是一个项目目标，而非已接受的语言变更——设计可能仍会大幅调整甚至被放弃，尽管被认为不太可能被放弃。社区对填补语言中长期存在的缺陷表现出显著热情，技术讨论比较了基于类型的 !Move 方案与 withoutboats 的竞争性 "pinned places" 提案，并对 !Forge 解锁安全 scoped spawn 以及 !Destruct 暗示线性类型的前景感到兴奋。

**标签**: `#rust`, `#language-design`, `#type-system`, `#memory-safety`, `#async`

---

<a id="item-5"></a>
## [SQLite "严重" CVE 被发现是 LLM 生成的幻觉](https://research.jfrog.com/post/sqlite-critical-cves-or-llm-slops/) ⭐️ 8.0/10

JFrog 研究人员发现，近期报告的数个 SQLite "严重" CVE 很可能是由 LLM 编造的，产生了听起来合理但在技术上不正确的漏洞描述，却仍然进入了官方漏洞数据库。这些报告包含关于 SQLite 代码库中不存在缺陷的虚假细节。 这一事件凸显了对安全基础设施日益增长的威胁：AI 生成的"垃圾内容"可能污染漏洞数据库，降低信噪比，使安全团队更难识别真正的威胁。被要求修补所有 CVE 的组织面临更大的运营负担，而提交系统缺乏验证可能被恶意行为者利用，用虚假报告淹没数据库。 这些幻觉 CVE 包含具体但错误的技木细节，例如引用不存在的函数和不可能的代码路径，这是 LLM 幻觉的典型特征——统计上看似合理的输出取代了事实准确性。JFrog 的分析表明，这些提交缺乏对所描述实际代码路径的人工验证。

hackernews · ymir_e · 8月3日 11:28 · [社区讨论](https://news.ycombinator.com/item?id=49154332)

**背景**: CVE（通用漏洞披露）是一个用于跟踪公开已知安全漏洞的标准化系统，由 MITRE 公司维护，全球安全团队使用它来确定修补优先级。LLM（大语言模型）是基于训练数据中的统计模式生成输出的概率系统，可能导致"幻觉"——自信但事实上不正确的输出。"AI slop"（AI 垃圾内容）一词指的是涌入信息渠道的低质量 AI 生成内容，使人们更难找到真正有用的信息。

**社区讨论**: 社区讨论的核心担忧是 LLM 生成的虚假报告降低了漏洞数据库的信噪比，使合法 CVE 更难被识别。评论者警告说，未经验证的提交系统可能被武器化，用虚假报告淹没数据库，并将其比作新一代"脚本小子"——使用 AI 工具但缺乏深入理解的人。也有人承认 LLM 确实发现过真实 CVE，但概率系统缺乏确定性这一事实对安全关键工作流构成了根本性的可信度问题。

**标签**: `#security`, `#llm`, `#cve`, `#sqlite`, `#ai-slop`

---

<a id="item-6"></a>
## [SemiAnalysis 深度解析：Kimi K3 的创新架构](https://newsletter.semianalysis.com/p/kimi-k3-the-manos-the-mythos-the) ⭐️ 8.0/10

SemiAnalysis 发布了对 Kimi K3 的详细技术分析，这是月之暗面推出的 2.8 万亿参数开源模型，引入了多项架构创新，包括压缩记忆、跨深度注意力（Kimi Delta Attention 与 Attention Residuals）以及潜在专家路由（LatentMoE）。该模型还具备原生视觉能力和 100 万 token 的上下文窗口。 Kimi K3 代表了对标准 Transformer 和 MoE 设计的重大突破，将多项新技术整合到一个生产级模型中，可能影响未来 LLM 架构的发展方向。开源权重的发布使研究人员和工程师能够直接研究这些创新，有望加速压缩记忆和潜在路由方法在整个行业的应用。 LatentMoE 将大型专家线性层降维投影到潜在空间，采用了与多头潜在注意力压缩 KV 缓存相同的压缩思路。Kimi Delta Attention 与 Attention Residuals 通过将网络深度与注意力最初解决的时间维度进行类比，解决了深度方向的信息流动问题，同时配合 NoPE（无位置编码）实现推理效率优化。

rss · Semianalysis · 8月3日 19:42

**背景**: 混合专家（MoE）架构通过每个 token 仅激活部分专家网络来高效扩展大语言模型，但常面临负载不均衡问题，即只有少数专家被持续激活。多头潜在注意力将键值（KV）缓存压缩到低维潜在空间，以降低推理时的内存和计算开销。Kimi K3 在 Kimi Linear 等先前工作的基础上，通过引入新颖的深度方向注意力路由和潜在空间专家压缩，在大规模下同时实现质量和效率。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://sebastianraschka.com/blog/2026/kimi-k3-architecture-notes.html">Kimi K 3 Architecture Notes | Sebastian Raschka, PhD</a></li>
<li><a href="https://www.kimi.com/blog/kimi-k3">Kimi K 3 Tech Blog: Open Frontier Intelligence</a></li>
<li><a href="https://explainx.ai/blog/kimi-k3-architecture-raschka-latentmoe-nope-july-2026">Kimi K 3 Architecture — Raschka Notes 2026 | explainx.ai</a></li>

</ul>
</details>

**标签**: `#AI/ML`, `#LLM Architecture`, `#Kimi K3`, `#SemiAnalysis`, `#Model Inference`

---

<a id="item-7"></a>
## [Qwen 发布 3.8-Max：2.4 万亿参数，首次开源 Max 级模型](https://qwen.ai/blog?id=qwen3.8) ⭐️ 8.0/10

通义千问团队正式发布了 Qwen 3.8-Max，这是一个基于 Qwen 3.5 架构的混合专家模型，总参数量达 2.4 万亿，活跃参数为 95B。这是 Qwen 首次对 Max 级别模型开放权重，权重将于下周开源，模型现已通过 QwenCloud 提供 API 服务。 开源一个拥有 2.4 万亿参数的 Max 级模型，对开放权重 AI 社区而言是一个重要里程碑，使研究者和开发者能够获得此前仅限于闭源 API 的前沿级能力。此次发布加剧了开源大模型领域的竞争，并可能推动编码、研究和长周期自主智能体应用的进展。 Qwen 3.8-Max 采用混合专家（MoE）架构，每个 token 仅激活 2.4 万亿参数中的 95B，这意味着加载完整模型需要大量显存，但推理计算量相对可控。团队声称该模型可自主运行超过 10 天完成项目构建与自我进化，并在 24 小时内参加 WWW2025 多模态对话意图识别竞赛，击败了 526 支队伍中的 458 支。

telegram · zaihuapd · 8月3日 02:31

**背景**: 混合专家（MoE）是一种架构，其中多个专门的子模型（专家）协同工作，由门控网络为每个输入 token 选择最合适的专家。这种设计使模型的总参数量可以大幅扩展，同时保持活跃参数——即推理计算量——远低于总规模，从而在相同计算预算下训练更大的模型。长周期任务指的是扩展的多步骤智能体工作流，AI 需要在较长的执行过程中保持连贯意图、从错误中恢复并自适应调整策略，这是 AI 智能体研究的关键前沿方向。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained</a></li>
<li><a href="https://www.ai21.com/glossary/ai-agent/what-are-long-horizon-tasks/">What are Long-Horizon Tasks? | AI21</a></li>
<li><a href="https://medium.com/@csburakkilic/understanding-moe-architectures-the-difference-between-total-and-active-parameters-ad1d161fccaa">Understanding MoE Architectures: The Difference Between Total and Active Parameters | by Burak Kılıç | Medium</a></li>

</ul>
</details>

**标签**: `#LLM`, `#Qwen`, `#open-source`, `#MoE`, `#AI`

---

<a id="item-8"></a>
## [美国犯罪实验室 DNA 设备曝安全漏洞，30 年证据面临篡改风险](https://www.wsj.com/tech/cybersecurity/security-flaw-placed-30-years-of-dna-evidence-at-risk-of-hacking-1932775a) ⭐️ 8.0/10

研究人员发现 Thermo Fisher Scientific 制造的、被美国多数犯罪实验室使用的 DNA 分析设备存在安全漏洞，可使自 1995 年以来的 DNA 证据文件遭到不留痕迹的篡改。研究人员利用 Anthropic 的 Claude AI 仅用约 45 分钟便生成了漏洞利用代码，修改后的电泳图谱文件未触发常用法医分析软件的警报。 该漏洞可能使三十年来数千起案件中使用的 DNA 证据可信度受到质疑，直接威胁美国刑事司法体系的完整性。AI 能在短时间内为专业法医文件格式生成漏洞利用代码，也凸显了 AI 与刑事司法交叉领域的新型网络安全风险。 Thermo Fisher Scientific 于 7 月私下承认该漏洞，并于上周五发布高危安全公告，推出了加入数字签名的软件更新以保护文件完整性。公司表示正与 CISA 合作，且尚无漏洞被实际利用的案例；但研究人员指出，全美 200 多家实验室缺乏统一监管，安全措施参差不齐。

telegram · zaihuapd · 8月3日 05:15

**背景**: 法医 DNA 分析依赖电泳图谱文件，该文件记录的 DNA 扫描数据被法庭用作刑事案件证据。虽然物理证据通过文件保管链进行追踪，但分析设备生成的数字文件在历史上并未受到加密签名保护，因此存在被无声篡改的风险。Thermo Fisher Scientific 是美国各犯罪实验室分析仪器的主要供应商。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.techtimes.com/articles/322771/20260803/ai-assisted-code-can-alter-forensic-dna-scan-files-without-any-detectable-trace.htm">AI-Assisted Code Can Alter Forensic DNA Scan Files Without Any...</a></li>
<li><a href="https://blog.cybernexora.com/dna-test-software-vulnerability/">DNA Test Software Vulnerability: Critical Evidence Risk</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#forensics`, `#AI-safety`, `#criminal-justice`, `#vulnerability`

---

<a id="item-9"></a>
## [英伟达 CMP 170HX 矿卡被破解：解锁 80GB 显存，二手价暴涨十倍](https://finance.sina.com.cn/tech/roll/2026-08-03/doc-inikzqsf4659769.shtml) ⭐️ 8.0/10

亚利桑那州立大学研究员公开了英伟达 CMP 170HX 矿卡的破解方案，利用 Falcon 安全协处理器的 DMA 栈溢出漏洞绕过 OTP 物理熔丝锁定，将显存最高解锁至 80GB，FP32 算力从 0.39 TFLOPS 暴增至 94 TFLOPS。消息传出后，该卡二手价从 300–500 元飙升至 3000–4000 元，海外市场叫价高达 1500 美元。 这一突破实际上将廉价的矿卡电子垃圾转化为性能可比 NVIDIA A100 的 GPU，使其能够以极低成本用于大语言模型推理和 AI 图像生成。它证明了长期被认为不可逆的 OTP 熔丝硬件限制可以通过安全协处理器漏洞被绕过，对英伟达的产品分级策略和更广泛的 AI 硬件市场具有深远影响。 CMP 170HX 采用与 A100 相同的 GA100 核心，但出厂时通过 OTP 熔丝在算力、显存和 PCIe 带宽等多层施加硬件限制；研究团队通过 Falcon 协处理器的 DMA 无界溢出劫持权限，逐一修改寄存器完成解锁。国内社区已独立验证该破解方案，确认解锁卡可在 Windows 和 Linux 下运行 AI 工作负载，但长期稳定性和不同生产批次的解锁上限仍存在不确定性。

telegram · zaihuapd · 8月3日 11:29

**背景**: NVIDIA CMP 170HX 是 2021 年推出的专用加密货币矿卡，去除了显示输出接口并施加了严格的硬件限制，以防止被重新用于通用计算任务。OTP（一次性可编程）eFuse 是一种在制造阶段永久烧录的硬件熔丝，用于实现产品分级——一旦设定即被设计为不可逆。Falcon 安全协处理器是内置于 NVIDIA GPU 中的微控制器，负责安全启动、固件验证和访问控制，是 GPU 安全架构中的关键信任锚点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://semiengineering.com/the-benefits-of-antifuse-otp/">The Benefits Of Antifuse OTP | Semiconductor Engineering</a></li>
<li><a href="https://anysilicon.com/semipedia/one-time-programmable-memory-otp-ip-core/">One - Time Programmable Memory ( OTP ) IP... - AnySilicon Semipedia</a></li>

</ul>
</details>

**社区讨论**: 国内社区成员已积极验证该破解方法，确认解锁后的矿卡可在 Windows 和 Linux 上运行 AI 图像生成和大语言模型推理。但讨论中也提出了对长期稳定性、英伟达可能的固件反制措施以及不同批次解锁上限差异的担忧。

**标签**: `#nvidia`, `#hardware-security`, `#gpu`, `#ai-inference`, `#jailbreak`

---

<a id="item-10"></a>
## [苹果就英国政府 iCloud 加密后门要求提起新诉讼](https://www.ft.com/content/2cc9c96a-0e5b-4c33-a95a-3d11072a145c?syn-25a6b1a6=1) ⭐️ 8.0/10

苹果已向英国调查权力法庭提起法律申诉，挑战英国政府发出的「技术能力通知」（TCN），该通知要求苹果为英国用户的加密 iCloud 云备份创建后门。此前英国曾撤回针对英美用户的最初要求，随后又发出仅针对英国用户的新通知，苹果已于 2025 年 2 月在英国下架了 iCloud 高级数据保护功能。 此案可能为民主国家能否强制科技公司削弱端到端加密设立关键全球先例，从根本上影响全球用户隐私与安全。如果英国成功，其他国家可能效仿，导致加密保护因司法管辖区而异，并引入系统性安全漏洞。 TCN 依据英国《2016 年调查权力法》签发，法律上禁止接收方确认或否认其存在，这也是苹果和英国内政部均拒绝对此置评的原因。隐私组织 Privacy International 和 Liberty 此前也已分别对 TCN 提起申诉，法庭已定于下月举行案件管理听证。

telegram · zaihuapd · 8月3日 15:40

**背景**: 技术能力通知（TCN）是依据英国《2016 年调查权力法》签发的政府命令，可强制服务提供商构建或维护技术能力以配合监控令状。苹果的 iCloud 高级数据保护采用端到端加密，意味着只有用户受信任的设备才能解密数据，连苹果自身也无法访问。英国政府最初要求针对英美两国用户创建后门，但在美国政府反对后撤回，随后又重新发出仅针对英国用户的缩小版通知。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://predaxia.com/glossary/technical-capability-notice/">Technical Capability Notice : UK government order under... | Predaxia</a></li>
<li><a href="https://support.apple.com/en-us/108756">How to turn on Advanced Data Protection for iCloud - Apple Support</a></li>
<li><a href="https://factually.co/fact-checks/technology/uk-technical-capability-notice-to-apple-demands-legal-challenges-f8051c">What exactly did the UK Technical Capability Notice to...</a></li>

</ul>
</details>

**标签**: `#encryption`, `#privacy`, `#apple`, `#uk-government`, `#surveillance`

---
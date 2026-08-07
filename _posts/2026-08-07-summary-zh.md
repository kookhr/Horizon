---
layout: default
title: "Horizon Summary: 2026-08-07 (ZH)"
date: 2026-08-07
lang: zh
---

> 从 35 条内容中筛选出 11 条重要资讯。

---

1. [OpenAI 称 Astra 模型或达「关键」网络攻击能力，扩大安全测试](#item-1) ⭐️ 9.0/10
2. [DeepSeek V4 Flash 0731 发布](#item-2) ⭐️ 8.0/10
3. [Oracle 禁止 OpenJDK 接受 AI 生成的代码](#item-3) ⭐️ 8.0/10
4. [pgrust 通过批处理、算子融合和 SIMD 实现 Postgres 分析查询 300 倍加速](#item-4) ⭐️ 8.0/10
5. [受 HBM 需求推动，2027 年内存产能据报已售罄](#item-5) ⭐️ 8.0/10
6. [在 150 万页网站上对抗 AI 爬虫的一年](#item-6) ⭐️ 8.0/10
7. [新墨西哥州法院命令 Meta 因损害儿童心理健康赔偿 5.67 亿美元](#item-7) ⭐️ 8.0/10
8. [SemiAnalysis 预测 SpaceX 2027 年部署 10GW，微软成最大承购方](#item-8) ⭐️ 8.0/10
9. [SemiAnalysis：Gemini 已翻车，但 GCP 正在发力](#item-9) ⭐️ 8.0/10
10. [美国审查中国 AI 企业海外获取英伟达芯片渠道](#item-10) ⭐️ 8.0/10
11. [sub2api 曝 OAuth 高危漏洞，仅凭邮箱即可接管账户](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI 称 Astra 模型或达「关键」网络攻击能力，扩大安全测试](https://openai.com/index/responding-next-frontier-critical-cyber-capabilities/) ⭐️ 9.0/10

2026 年 8 月 7 日，OpenAI 披露其即将推出的 Astra 模型在内部评估中可能达到「关键」自主网络攻击能力阈值，这是 GPT-5.6-Sol 等先前模型未达到的水平。公司已暂停不符合强化安全要求的内部活动，并正在实施隔离测试环境、加密增强和通用监控等措施。 此次披露标志着 AI 驱动的网络安全威胁可能发生范式转变，即 AI 模型能够自主发现零日漏洞并执行端到端的新型网络攻击，无需人工干预。扩大的安全测试和潜在的发布推迟凸显了推进前沿 AI 能力与确保安全部署之间日益加剧的紧张关系，对网络安全、AI 对齐和监管监督都有深远影响。 根据 OpenAI 的预备框架，「关键」阈值意味着模型能够自主识别并开发针对许多加固真实系统的功能性零日漏洞利用，或仅凭高层目标执行端到端的新型网络攻击。OpenAI 正在与政府机构和 AI 安全组织合作开展第三方测试，并指出此前 GPT-5.6-Sol 等模型在这些评估中仅被评为「高」级别。

telegram · zaihuapd · 8月7日 16:44

**背景**: OpenAI 的预备框架定义了能力阈值，用于在部署前评估前沿 AI 模型带来的风险。「关键」级别代表可能引入前所未有的新型严重伤害威胁向量，例如无需人工干预即可自主发现并利用零日漏洞——即供应商未知的安全缺陷。该框架已更新以简化风险级别，移除了「低」和「中」类别，将运营工作集中在更高严重性的威胁上。关于 Astra 的披露出现在更广泛的行业趋势背景下，AI 模型越来越多地被用于进攻性和防御性网络安全应用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.axios.com/2026/08/07/openai-astra-model-delay-cybersecurity-risks">OpenAI slows release of Astra model citing cyber capabilities</a></li>
<li><a href="https://openai.com/index/responding-next-frontier-critical-cyber-capabilities/">Responding to the next frontier of critical cyber capabilities | OpenAI</a></li>
<li><a href="https://cdn.openai.com/pdf/18a02b5d-6b67-4cec-ab64-68cdfbddebcd/preparedness-framework-v2.pdf">Preparedness Framework Version 2. Last updated: 15th April, 2025</a></li>

</ul>
</details>

**标签**: `#AI Safety`, `#Cybersecurity`, `#OpenAI`, `#Artificial Intelligence`, `#Zero-Day Vulnerabilities`

---

<a id="item-2"></a>
## [DeepSeek V4 Flash 0731 发布](https://arcprize.org/results/deepseek-v4-flash-0731) ⭐️ 8.0/10

DeepSeek 发布了 V4 Flash 0731，这是取代之前预览版的正式版本，具有显著增强的智能体能力。它是一个稀疏混合专家模型，总参数量为 284B，其中激活参数为 13B，提供高速度和低成本。 这次发布之所以重要，是因为它以极低的成本提供了与更昂贵模型相媲美的性能，在性价比方面对整个 AI 行业施加了压力。其开放权重和低廉的 API 定价使更广泛的开发者和企业群体能够获得先进的 AI 能力。 该模型的定价为每百万输入 token 0.09 美元，每百万输出 token 0.18 美元，在使用 2x RTX Pro 6000 Blackwell GPU 的单流上可达到约每秒 250 个 token 的速度。然而，与之前的版本相比，一些用户报告了无限循环和无法执行工具调用的问题。

hackernews · tosh · 8月7日 17:56 · [社区讨论](https://news.ycombinator.com/item?id=49214008)

**背景**: DeepSeek 是一家成立于 2023 年的中国 AI 公司，因开发高性能、高性价比的开放权重大型语言模型而备受关注。该公司利用混合专家架构来降低训练和推理成本，声称训练 V3 等模型的成本仅为竞争对手的一小部分。DeepSeek 的成就被描述为美国 AI 行业的“斯普特尼克时刻”，挑战了只有巨额预算和顶级芯片才能推动 AI 发展的观念。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash-0731">deepseek-ai/DeepSeek-V4-Flash-0731 · Hugging Face</a></li>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4-flash-0731">DeepSeek V4 Flash 0731 - API Pricing & Benchmarks | OpenRouter</a></li>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek_(Company)">DeepSeek (Company)</a></li>

</ul>
</details>

**社区讨论**: 社区情绪总体积极，用户称赞该模型卓越的性价比和速度，指出它足以胜任大多数任务，而每天只需花费几美元。然而，一些用户报告该模型存在陷入无限循环和无法执行工具调用的问题，表明在某些智能体使用场景中可能存在不稳定性。

**标签**: `#DeepSeek`, `#LLM`, `#AI`, `#Machine Learning`, `#Release`

---

<a id="item-3"></a>
## [Oracle 禁止 OpenJDK 接受 AI 生成的代码](https://app.dealroom.co/news/feed/oracle-bans-ai-generated-code-from-openjdk-despite-ellison-s-claim-oracle-isn-t-writing-its-own-code) ⭐️ 8.0/10

OpenJDK 管理委员会批准了一项临时政策，禁止包含由大语言模型、扩散模型或类似深度学习系统部分或全部生成内容的贡献。该政策适用于社区提交的内容，同时律师团队正在起草最终版本。 作为一个重要的企业级开源项目，OpenJDK 的禁令为大型软件生态系统在生成式 AI 时代处理版权和贡献来源问题树立了重要先例。它凸显了使用 AI 工具加速开发与管理法律责任之间的紧张关系，特别是对于像 Oracle 这样拥有大量诉讼历史的组织。 该禁令专门针对社区贡献，关于它是否也适用于核心开发者，还是主要用于管理外部提交的数量，目前存在讨论。该政策明确是临时性的，管理委员会指出律师团队正在撰写最终版本。

hackernews · delduca · 8月7日 17:36 · [社区讨论](https://news.ycombinator.com/item?id=49213754)

**背景**: OpenJDK 是 Java 平台标准版的开源实现，也是 Java 的参考实现。负责管理 OpenJDK 的 Oracle 拥有众所周知的版权诉讼历史，包括与 Google 之间围绕 Java API 的长期法律战。AI 编程助手可能会无意中逐字复制已授权的代码，造成所有权空白和版权风险，这对于被全球大型企业使用的项目来说尤为令人担忧。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openjdk.org/legal/ai">OpenJDK Interim Policy on Generative AI</a></li>
<li><a href="https://en.wikipedia.org/wiki/OpenJDK">OpenJDK - Wikipedia</a></li>
<li><a href="https://ratedwithai.com/blog/ai-code-generation-copyright-risk-2026">AI-Generated Code Copyright Risk for Businesses 2026</a></li>

</ul>
</details>

**社区讨论**: 社区情绪复杂，但大多理解其实际理由：审查者的时间有限，AI 生成的提交为一个支撑重大业务的项目增加了负担和风险。评论者指出 Oracle 一边大力投资 AI 一边禁止 AI 贡献的讽刺性，有人认为 Oracle 的法律部门"坐在驾驶座上"，以保留起诉他人用 AI 洗白专有代码的权利。一个重要的细节是，该禁令可能适用于社区提交而非核心开发者，这使其更像是一个贡献管理问题，而非全面的 AI 禁令。

**标签**: `#openjdk`, `#generative-ai`, `#open-source`, `#copyright`, `#oracle`

---

<a id="item-4"></a>
## [pgrust 通过批处理、算子融合和 SIMD 实现 Postgres 分析查询 300 倍加速](https://malisper.me/how-we-made-postgres-hundreds-of-times-faster-the-query-engine/) ⭐️ 8.0/10

一个名为 pgrust 的基于 Rust 的 Postgres 实现通过应用批处理、算子融合和 SIMD 向量化三项关键技术，在分析查询上实现了 300 倍的性能提升。作者还已开始形式化验证和差分模糊测试，以证明其与原版 PostgreSQL 的正确性一致性。 PostgreSQL 被广泛使用，但在分析查询性能上历来不及专用 OLAP 引擎。这项工作表明，融入现代查询执行技术的重写可以大幅缩小这一差距，有望使 Postgres 在以往需要独立分析数据库的场景中变得可行。 300 倍的加速来自批处理（一次处理多个元组以减少逐元组开销）、算子融合（消除查询算子之间的中间物化）和 SIMD 向量化（利用 CPU 向量指令进行并行数据处理）三者的结合。作者指出正确性是首要优先事项，已通过形式化验证证明超过 1000 个面向用户的函数与 PostgreSQL 逻辑完全一致。

hackernews · poly2it · 8月7日 11:00 · [社区讨论](https://news.ycombinator.com/item?id=49208535)

**背景**: 算子融合是一种查询处理技术，通过消除数据库算子之间的中间结果物化来减少内存访问并提升缓存局部性——这一概念在内存数据库研究中已有深入探讨。SIMD（单指令多数据流）允许单条 CPU 指令同时处理多个数据元素，对于对大型列式数据集执行相同操作的分析负载尤为有效。传统 PostgreSQL 采用逐元组方式处理查询（Volcano 执行模型），这会带来较高的逐元组开销，且无法充分利用现代 CPU 的向量指令等能力。pgrx 框架已存在用于以 Rust 构建 Postgres 扩展，但 pgrust 代表了对查询引擎本身的完整重写。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://dl.acm.org/doi/10.14778/3151113.3151114">Relaxed operator fusion for in-memory databases: making compilation, vectorization, and prefetching work together at last: Proceedings of the VLDB Endowment: Vol 11, No 1</a></li>
<li><a href="https://cse.buffalo.edu/adblab/people/zzhao35/teaching/cse707_fall21/simd.pdf">Rethinking SIMD Vectorization for In-Memory Databases</a></li>
<li><a href="https://github.com/pgcentralfoundation/pgrx">GitHub - pgcentralfoundation/pgrx: Build Postgres Extensions with Rust! · GitHub</a></li>

</ul>
</details>

**社区讨论**: 作者（malisper）主动回应了信任方面的疑虑，强调正确性是首要优先事项，已通过形式化验证和差分模糊测试加以保障。社区成员对采用前景表示怀疑，认为对成熟的 Postgres 团队和项目长期延续性的信任比单纯的性能更重要。一些评论者则指出了令人兴奋的可能性，如将 pgrust 嵌入作为 SQLite 的替代方案，并赞赏其引入了自适应查询规划——这是 Postgres 核心团队一直不愿实现的功能。

**标签**: `#Postgres`, `#Database Performance`, `#SIMD`, `#Rust`, `#Query Optimization`

---

<a id="item-5"></a>
## [受 HBM 需求推动，2027 年内存产能据报已售罄](https://www.ign.com/articles/ramageddon-continues-another-year-as-2027-memory-capacity-is-reportedly-sold-out) ⭐️ 8.0/10

据报道，内存制造商已售罄其 2027 年的全部产能，这主要受到 AI 加速器中使用的高带宽内存（HBM）需求激增的推动。这一前所未有的远期售罄表明，当前被称为"RAMmageddon"的内存供应短缺预计将持续数年，而非短期内解决。 2027 年产能售罄表明 HBM 需求正在挤占传统 DRAM 产能，这将限制消费电子产品（包括手机、笔记本电脑和游戏机）的供应并推高价格。这对整个科技行业具有广泛的通胀影响，可能减缓消费硬件的进步速度。 社区讨论中强调的一个关键技术细节是，在同一技术节点下，HBM3E 生产相同数量的比特所需的晶圆供应量约为 DDR5 的三倍，因为 HBM 裸片必须更大以容纳采用硅通孔（TSV）的 3D 堆叠封装。这一 3:1 的晶圆产能比意味着每次向 HBM 生产转移都会按不成比例的幅度直接减少传统 DRAM 的供应量。

hackernews · inigyou · 8月7日 07:58 · [社区讨论](https://news.ycombinator.com/item?id=49207236)

**背景**: 高带宽内存（HBM）是一种 3D 堆叠 DRAM 技术，最初由三星、AMD 和 SK 海力士开发，通过硅通孔（TSV）互连的垂直裸片堆叠实现了比传统 DRAM 高 10-30 倍的带宽密度。HBM 已成为 AI 训练和推理的关键推动力，因为 NVIDIA 的 H100 和 B200 等 GPU 加速器需要巨大的内存带宽来向数千个计算核心提供数据。始于 2025 年的全球内存供应短缺被称为"RAMmageddon"或"RAMpocalypse"，它与 2020-2023 年芯片短缺的不同之处在于，它主要由 AI 驱动的 HBM 需求挤占传统 DRAM 和 NAND 闪存晶圆分配所驱动，而非疫情时期的供应链中断。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/High_Bandwidth_Memory">High Bandwidth Memory - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/2025–present_global_memory_supply_shortage">2025–present global memory supply shortage - Wikipedia</a></li>
<li><a href="https://nand-research.com/analyst-note-semiconductor-memory-market-supply-constraints-and-rising-prices/">Call Notes: Memory Market Supply Constraints and Rising ...</a></li>

</ul>
</details>

**社区讨论**: 讨论中用户 bob1029 提出了一个值得注意的技术见解，强调 HBM3E 每生产一比特所消耗的晶圆产能约为 DDR5 的三倍，解释了供应紧缩的机制原因。其他评论者对消费品的广泛通胀后果表示担忧，用户 pu_pe 警告称内存价格压力加上其他供应不确定性使 2%的通胀目标显得过于乐观。一些用户分享了个人反应，包括囤积组件的冲动以及因 AI 工具对下游硬件供应的影响而对采用 AI 工具的犹豫。

**标签**: `#memory`, `#supply-chain`, `#HBM`, `#AI-infrastructure`, `#hardware`

---

<a id="item-6"></a>
## [在 150 万页网站上对抗 AI 爬虫的一年](https://patronview.com/news/99-percent-of-my-website-traffic-is-bots/) ⭐️ 8.0/10

一个拥有 150 万页面的网站作者发布了一篇详细报告，讲述了一年来对抗机器人流量的经历，揭示其 99%的流量来自机器人，且 AI 爬虫导致月度托管成本飙升约 500%。文章描述了使用 Cloudflare 等工具缓解激进 AI 爬虫的技术方案。 这一案例提供了具体的数据，展示了 AI 训练爬虫对独立网站发布者造成的日益增长的成本和基础设施负担。它凸显了内容创作者与无偿抓取数据的 AI 公司之间日益加剧的矛盾，引发了关于开放网络可持续性的质疑。 作者指出成本飙升主要源于 Cloudflare D1（一种无服务器 SQL 数据库），其定价模式使得高机器人流量意外昂贵，有人建议迁移到静态网站。作者也承认了自己作为爬虫的讽刺性，因为该网站本身也在从公开文档中抓取数据。

hackernews · petercooper · 8月7日 14:51 · [社区讨论](https://news.ycombinator.com/item?id=49211386)

**背景**: AI 爬虫是自动化的程序，用于抓取网站以提取大量数据，通常用于训练生成式 AI 模型或支持检索增强生成（RAG）。与遵守速率限制和 robots.txt 的传统搜索引擎爬虫不同，许多 AI 爬虫运行激进，无视惯例并产生大量请求。网站运营者越来越依赖像 Cloudflare 这样的机器人管理服务来区分合法的人类流量和机器人，使用工作量证明挑战或 CAPTCHA 替代方案等工具。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.akamai.com/blog/security/rise-llm-ai-scrapers-bot-management">The Rise of the LLM AI Scrapers: What It Means for Bot Management | Akamai</a></li>
<li><a href="https://blog.barracuda.com/2025/04/02/threat-spotlight-gray-bots-gen-ai-scraper-bots-targeting-web-apps">Threat Spotlight: The good, the bad, and the ‘gray bots’ – the Gen AI scraper bots targeting your web apps | Barracuda Networks Blog</a></li>
<li><a href="https://www.cloudflare.com/products/turnstile/">Cloudflare Turnstile - Easy CAPTCHA Alternative</a></li>

</ul>
</details>

**社区讨论**: 社区讨论提出了几个关键点：担忧通过 Cloudflare 集中控制网络访问权限，用户在被封锁时无计可施；推荐 Anubis——一种基于工作量证明的工具，适用于不在 CDN 提供商背后的网站；其他网站所有者对 AI 机器人抓取数十万页面却零补偿或零署名感到沮丧。一位评论者指出了爬虫抱怨被爬取的讽刺性。

**标签**: `#web-infrastructure`, `#bots`, `#cloudflare`, `#ai-crawlers`, `#web-security`

---

<a id="item-7"></a>
## [新墨西哥州法院命令 Meta 因损害儿童心理健康赔偿 5.67 亿美元](https://www.theguardian.com/technology/2026/aug/06/new-mexico-court-meta) ⭐️ 8.0/10

新墨西哥州法院裁定 Meta 违反该州公共滋扰法，对儿童心理健康造成损害，命令其支付 5.67 亿美元并为未成年用户实施平台变更。这一裁决是公共滋扰法规首次成功应用于社交媒体平台之一，要求 Meta 资助青少年心理健康项目并修改针对年轻用户的平台设计。 这一判决通过将传统上用于环境或财产纠纷的公共滋扰法成功应用于社交媒体公司，确立了重要的法律先例，可能为美国其他司法管辖区的类似诉讼打开大门。鉴于已有 42 名州总检察长对 Meta 提起相关诉讼，此裁决可能加速一波问责措施，迫使大型科技平台重新设计其令人上瘾的互动算法。 法院裁定 Meta 违反了新墨西哥州的公共滋扰法（NMSA 1978 § 30-8-1），该法将公共滋扰定义为明知而创造或维持对公共健康、安全、道德或福利有害的事物。虽然 5.67 亿美元相对于 Meta 的全球收入看似不大，但对于一个仅有 200 多万居民的州来说，这是一笔巨额判决，而且 Meta 还面临另一起高达 1.4 万亿美元的青少年心理健康损害诉讼。

hackernews · boplicity · 8月7日 00:06 · [社区讨论](https://news.ycombinator.com/item?id=49204352)

**背景**: 公共滋扰法是传统上用于处理危害整个社区活动的法律法规，如污染或危险环境，而非针对特定个人。近年来，由代表 41 个州和华盛顿特区的 42 名州总检察长组成的联盟对 Meta 提起诉讼，指控该公司故意将 Facebook 和 Instagram 的功能设计成令人上瘾的，尤其是针对未成年人。这些诉讼声称 Meta 将利润置于儿童安全之上，加剧了美国青少年的心理健康危机。新墨西哥州的案件是首批将公共滋扰法正式应用于社交媒体平台的法院裁决之一，确立了算法设计选择可以构成对公共福利的侵害。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://publichealthpolicyjournal.com/new-mexico-wants-a-court-to-declare-meta-a-public-nuisance-how-would-that-change-platforms-like-facebook-and-instagram/">New Mexico Wants a Court to Declare Meta a ‘ Public Nuisance .’ How...</a></li>
<li><a href="https://socialmediavictims.org/meta-lawsuit/">Meta Lawsuit - July 2026 Update</a></li>
<li><a href="https://bbbprograms.org/media/insights/blog/platform-accountability">Teen Mental Health Could be Protected by Public Nuisance Laws</a></li>

</ul>
</details>

**社区讨论**: 社区成员指出，虽然罚款相对于 Meta 的全球收入看似不大，但对于新墨西哥州这样一个仅有 200 多万居民的小司法管辖区来说，这是一笔巨额罚款。一位评论者指出被违反的具体法律是新墨西哥州的公共滋扰法（NMSA 1978 § 30-8-1），该法涵盖明知而维持对公共健康或福利有害的事物。用户分享了算法成瘾的个人经历，描述了 TikTok 和 Instagram Reels 如何通过无意识滑动消耗了他们数小时的时间，而其他人则指出该裁决可能促使 Meta 修改其推荐算法对年轻受众的运作方式。

**标签**: `#meta`, `#legal`, `#regulation`, `#mental-health`, `#social-media`

---

<a id="item-8"></a>
## [SemiAnalysis 预测 SpaceX 2027 年部署 10GW，微软成最大承购方](https://newsletter.semianalysis.com/p/spacex-10gw-in-2027-why-its-real) ⭐️ 8.0/10

SemiAnalysis 发布了一篇深度分析报告，预测 SpaceX 将在 2027 年底前部署 10GW 的计算能力，有望带来 3000 亿美元的年经常性收入（ARR）。报告特别指出微软将成为该计算能力的最大承购方，将其用于 AI 计算工作负载，从而推动 Azure 的收入增长率加速至三位数。 这一预测标志着航天基础设施与超大规模云服务商 AI 计算需求的重大融合，暗示电力瓶颈可能通过 SpaceX 等非传统供应商来解决。如果预测成真，微软将在 AI 基础设施竞赛中获得决定性优势，而 SpaceX 作为计算提供商的入局将重塑数据中心格局，并催生一个价值数千亿美元的新市场。 该分析估计 AI 计算租赁可以获得溢价定价，OpenAI 和 Anthropic 等公司每 GW 每年可产生超过 1000 亿美元的收入。SpaceX 的部署路线图包括在 2026 年底前安装约 2GW 的计算能力，到 2027 年底扩展至 10GW，并初步设定 20GW 的电力和冷却基础设施目标。

rss · Semianalysis · 8月7日 20:08

**背景**: AI 数据中心面临严峻的电力瓶颈，据英伟达 CEO 黄仁勋表示，一座 1GW 的 AI 工厂建造成本可能高达 1000 亿美元。当前基础设施每 GW 约产生 300-500 亿美元的计算收入，但下一代经济模型可能将这一数字推升至每 GW 每年 1000 亿美元。SpaceX 通过其 Starship 和 Starlink 项目展现的快速部署能力，使其成为潜在的快速基础设施建造商。与此同时，微软 Azure 一直在积极扩展其 AI 计算能力，以满足 OpenAI 和其他 AI 工作负载激增的需求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://newsletter.semianalysis.com/p/spacex-10gw-in-2027-why-its-real">SpaceX 10GW in 2027 – Why It’s Real, Will Drive $500B ARR for ...</a></li>
<li><a href="https://bingx.com/en/news/post/spacex-gw-in">SpaceX targets 10GW of compute by end-2027 with $300500B ...</a></li>
<li><a href="https://finance.yahoo.com/technology/ai/articles/spacex-10-gw-nvidia-vera-164046815.html?fr=sycsrp_catchall">SpaceX’s 10 GW Nvidia Vera Rubin Bet: The Compute Landlord ...</a></li>
<li><a href="https://cryptobriefing.com/nvidia-100b-ai-factory-cost/">Nvidia CEO Jensen Huang estimates $100B cost for 1 GW AI factory</a></li>
<li><a href="https://stockwirex.com/education/nvidia-100-billion-gigawatt-explained/">Nvidia $100B per Gigawatt Decoded: AI Factory Economics</a></li>

</ul>
</details>

**标签**: `#AI Infrastructure`, `#Data Centers`, `#SpaceX`, `#Microsoft Azure`, `#Power Constraints`

---

<a id="item-9"></a>
## [SemiAnalysis：Gemini 已翻车，但 GCP 正在发力](https://newsletter.semianalysis.com/p/gemini-is-cooked-but-gcp-is-cooking) ⭐️ 8.0/10

SemiAnalysis 发布了一篇逆向分析文章，认为 Google DeepMind 在以 Gemini 为核心的消费者 AI 竞赛中正在落败，而 Google Cloud Platform（GCP）则同时利用其 AI 基础设施成功抢占企业市场份额。文章将 DeepMind 在消费者 AI 领域的困境视为 GCP 企业业务的直接短期收益。 这项分析揭示了 Google AI 战略内部的战略分化，可能重塑业界对其竞争地位的评估方式。对于云计算和 AI 基础设施观察者而言，这表明即使 Google 未能在消费者聊天机器人竞赛中胜出，其云业务部门仍可能成为主导性的企业 AI 平台。 文章副标题——"为什么 DeepMind 的长期失败是 GCP 的短期收益"——概括了核心论点：消费者 AI 表现不佳与企业云业务增长是 Google 一体两面的表现。GCP 的企业 AI 战略还通过与 Anthropic 的战略合作进一步强化，后者使 Claude 模型与 Gemini 一同在 Google 云基础设施上可用。

rss · Semianalysis · 8月7日 02:32

**背景**: Google DeepMind 是负责 Gemini 的研究部门，Gemini 是 Google 面向消费者的旗舰 AI 模型和聊天机器人，与 OpenAI 的 ChatGPT 竞争。Google Cloud Platform（GCP）是公司的企业云计算部门，为企业客户提供 AI 基础设施、模型托管和开发工具。GCP 目前在云计算市场排名第三，落后于 AWS 和 Microsoft Azure，但一直通过其集成 AI 技术栈和第三方模型合作积极拓展企业 AI 工作负载。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://reactionlogic.com/article/anthropic-partnership-bolsters-google-cloud-s-enterprise-ai-push">Anthropic Strengthens Google Cloud Enterprise AI Strategy</a></li>
<li><a href="https://www.linkedin.com/pulse/google-clouds-third-place-problem-isnt-techits-david-linthicum-4pwze">Google Cloud ’s Third-Place Problem Isn’t About Tech—It’s About...</a></li>

</ul>
</details>

**标签**: `#AI`, `#Google Cloud`, `#DeepMind`, `#Cloud Infrastructure`, `#Strategy`

---

<a id="item-10"></a>
## [美国审查中国 AI 企业海外获取英伟达芯片渠道](https://www.bloomberg.com/news/articles/2026-08-07/us-reviews-china-s-offshore-access-to-nvidia-chips-after-ai-breakthroughs) ⭐️ 8.0/10

美国商务部工业与安全局（BIS）已启动系统性审查，调查中国 AI 企业如何在海外获取和使用英伟达芯片，包括通过远程租用其他国家算力和壳公司的方式。此前月之暗面发布的 Kimi K3 模型性能逼近美国同行，一名白宫高官曾公开指控其非法获取英伟达芯片并经泰国一方远程访问，随后 BIS 执法团队启动了审查。 这一进展暴露了美国出口管制的关键漏洞：虽然实体芯片运输受到限制，但通过云计算远程访问算力仍处于法律灰色地带。此次审查结果及待通过的立法可能重塑中国 AI 企业获取先进计算基础设施的方式，直接影响中国 AI 发展速度和全球 AI 产业的竞争格局。 BIS 正在整理两份国家名单：涉嫌将受限芯片走私入境中国的黑市所在地，以及中国企业远程租用芯片的国家。据报道，阿里巴巴通过开曼实体控制的新加坡壳公司，经正被新加坡警方和美方调查的 Megaspeed，使用位于马来西亚的英伟达芯片。

telegram · zaihuapd · 8月7日 11:18

**背景**: 美国逐步收紧对华先进 AI 芯片出口管制，限制总部位于 D:5 国家组（包括中国）的企业在无许可证情况下获取高性能计算产品。然而，这些法规主要针对实体出口，形成了一个漏洞：中国企业可以通过第三国数据中心租用算力。月之暗面的 Kimi K3 是一个拥有 2.8 万亿参数的开源模型，其表现证明中国企业仍能实现前沿水平的 AI 性能，引发了对现有管制措施有效性的担忧。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bis.gov/">Homepage | Bureau of Industry and Security</a></li>
<li><a href="https://www.together.ai/models/kimi-k3">Kimi K 3 API | Together AI</a></li>
<li><a href="https://www.cryptopolitan.com/nvidia-megaspeed-investigated-in-singapore/">Nvidia client Megaspeed investigated in Singapore for... - Cryptopolitan</a></li>

</ul>
</details>

**标签**: `#US-China tech war`, `#NVIDIA chips`, `#AI export controls`, `#cloud computing`, `#Moonshot AI`

---

<a id="item-11"></a>
## [sub2api 曝 OAuth 高危漏洞，仅凭邮箱即可接管账户](https://github.com/Wei-Shaw/sub2api/issues/5350) ⭐️ 8.0/10

sub2api v0.1.171 及之前版本存在 CVSS 8.8 的 OAuth 账户接管漏洞，攻击者仅需知道受害者注册邮箱，无需密码、验证码或用户交互，即可将自己的 OAuth 身份绑定到受害者账户。该缺陷位于 pending session 流程的 existingUser 分支，在将目标用户 ID 设为受害者时未校验密码和验证码。 该漏洞可导致受害者账户被完全接管，包括 API 密钥、账单余额和订阅配额，对运行受影响版本的部署构成严重安全风险。该漏洞模式——OAuth 流程中 pending session 处理缺陷——对 OAuth 实现具有广泛的安全警示意义，因为使用相同模式的其他系统也可能存在类似缺陷。 攻击者利用 pending session 流程中 existingUser 分支不校验密码和验证码的缺陷，将目标用户 ID 设为受害者后完成 OAuth 身份绑定。绑定后，攻击者每次 OAuth 登录均会解析为受害者账户，从而持续访问 API 密钥、账单余额与订阅配额。

telegram · zaihuapd · 8月7日 14:59

**背景**: sub2api 是一个提供 API 管理功能的项目，支持与 Gemini 等服务的 OAuth 认证。OAuth 是一种广泛使用的授权框架，允许第三方应用获取用户账户的访问权限，通常涉及基于令牌的认证流程。在 OAuth 实现中，"pending session" 指的是认证过程中的一个中间状态，此时用户身份正在被验证和关联；如果该状态未被妥善保护，攻击者可利用其将未授权的身份绑定到已有账户。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cobalt.io/vulnerability-wiki/v4-access-control/oauth-account-takeover">OAuth Account Takeover | Pentest Vulnerability Wiki</a></li>
<li><a href="https://rain.moe/202/">Sub 2 API 部署和添加账号 – 靈夢の小窝</a></li>

</ul>
</details>

**标签**: `#security`, `#oauth`, `#vulnerability`, `#account-takeover`

---
---
layout: default
title: "Horizon Summary: 2026-07-18 (ZH)"
date: 2026-07-18
lang: zh
---

> 从 38 条内容中筛选出 10 条重要资讯。

---

1. [GPT-5.6 解决凸优化领域 30 年悬而未决的公开问题](#item-1) ⭐️ 9.0/10
2. [LG 显示器通过 Windows Update 静默安装软件，未经用户同意](#item-2) ⭐️ 8.0/10
3. [Kimi K3 时刻：非美国实验室实现前沿 AI 性能](#item-3) ⭐️ 8.0/10
4. [Stack Overflow 活跃度下降数据可视化引发关于 AI 及其他原因的讨论](#item-4) ⭐️ 8.0/10
5. [Meta 拟向 Anthropic 出租百亿美元 AI 算力](#item-5) ⭐️ 8.0/10
6. [SpaceX 与五角大楼谈判提供 AI 算力，交易或达数十亿美元](#item-6) ⭐️ 8.0/10
7. [Kimi K3 首登 DeepSWE 基准测试第三名，成为首个达到前沿水平的开源权重模型](#item-7) ⭐️ 8.0/10
8. [台积电 A14 制程进展超预期，良率与性能双双逼近 90%](#item-8) ⭐️ 8.0/10
9. [特朗普政府拟设类似 FINRA 的独立机构审查顶尖 AI 模型](#item-9) ⭐️ 8.0/10
10. [美国要求分享韩国芯片商 AI 热潮超额利润](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [GPT-5.6 解决凸优化领域 30 年悬而未决的公开问题](https://old.reddit.com/r/math/comments/1uxj3cy/after_openais_cdc_proof_announcement_gpt56_used_a/) ⭐️ 9.0/10

据报道，GPT-5.6 使用基于提示词的方法解决了凸优化领域一个 30 年悬而未决的公开问题，具体涉及有限内存下凸优化的预言机复杂度。这一突破建立在 OpenAI 近期一系列数学证明公告的基础上，包括循环双覆盖猜想，且该成果是使用 Sol Pro 而非 Ultra 版本完成的。 这一成就表明，大语言模型正在从辅助常规数学计算的工具，发展为能够对长期悬而未决的公开问题做出真正研究级贡献的系统。这预示着数学研究方式可能发生根本性转变，引发了关于人类研究者未来角色以及哪些问题对人类仍有意义的重要讨论。 被解决的问题涉及一阶凸优化的预言机复杂度，具体是在有限内存约束下，刻画优化凸 Lipschitz 函数所需的一阶查询的最小最大次数。社区成员指出，该问题虽然与循环双覆盖猜想相比属于较细分领域，但仍是一项真正的贡献；证明时间复杂度的上界相对容易，而下界的证明则困难得多。

hackernews · mbustamanter · 7月18日 13:00 · [社区讨论](https://news.ycombinator.com/item?id=48957779)

**背景**: 凸优化是数学和计算机科学中的一个基础领域，研究在凸集上最小化凸函数的问题，应用范围涵盖机器学习到运筹学。预言机复杂度是该领域的一个核心概念，衡量找到最优解需要对预言机（提供函数值和梯度）进行多少次查询。这一具体的公开问题由 Woodworth 和 Srebro 于 2019 年提出，但建立在数十年前人工作的基础上，探讨已知最优方法所需的二次内存是否真正必要，并试图刻画在内存约束下所需的最少一阶查询次数。一阶方法仅使用梯度信息而非完整的二阶（Hessian）信息，是现代大规模优化的核心，但其内存与复杂度之间的权衡关系在理论上仍存在已知空白。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://proceedings.mlr.press/v99/woodworth19a.html">Open Problem: The Oracle Complexity of Convex Optimization with Limited Memory</a></li>
<li><a href="https://arxiv.org/abs/1907.00762">[1907.00762] Open Problem: The Oracle Complexity of Convex Optimization with Limited Memory</a></li>
<li><a href="https://en.wikipedia.org/wiki/Convex_optimization">Convex optimization - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 具有领域专业知识的社区成员确认该问题是对该领域的一项真正贡献，尽管相对细分；有人指出时间复杂度的上界证明相对容易，而下界则困难得多。关于这对数学研究职业的影响也引发了激烈讨论，有人将其与 AI 影响初级软件开发者的方式进行比较——部分人认为数学中低难度和中等难度的问题将不再值得追求，而另一些人则质疑研究者是否正是通过解决这类问题获得必要的专业训练。技术讨论还涉及 ChatGPT Pro（被描述为选择最佳答案的多智能体系统）与 Ultra（被描述为使用动态 JS 工作流编排智能体）之间的差异，一位评论者观察到 AI 将大量蛮力应用于可系统探索数学逻辑的问题的能力将推动有趣的进展。

**标签**: `#AI`, `#Mathematics`, `#Optimization`, `#LLM`, `#Research`

---

<a id="item-2"></a>
## [LG 显示器通过 Windows Update 静默安装软件，未经用户同意](https://videocardz.com/newz/lg-monitors-silently-install-software-through-windows-update-without-user-consent) ⭐️ 8.0/10

LG 显示器在连接到 PC 时，会通过 Windows Update 静默安装具有完整系统访问权限的非沙箱软件，无需任何用户交互或同意。这种情况在连接新的 LG 显示器以及已经连接了旧款 LG 显示器的用户身上都会发生。 这代表了一个重大的安全和隐私漏洞，因为安装的软件具有互联网访问权限和完整的系统权限，且没有沙箱隔离，并在每次系统启动时自动运行。它突显了 Windows 设备安装策略的一个更广泛问题，即允许第三方硬件供应商通过操作系统更新机制推送任意软件。 安装的软件在没有沙箱隔离的情况下运行，授予其完整的系统访问权限和互联网连接，并在每次系统启动时启动。用户可以通过组策略编辑器（gpedit.msc）启用'阻止自动下载与设备元数据关联的应用程序'来阻止此行为，或者在 Windows 家庭版上通过系统属性（sysdm.cpl）禁用自动制造商应用程序下载。

hackernews · baranul · 7月18日 10:21 · [社区讨论](https://news.ycombinator.com/item?id=48956688)

**背景**: Windows Update 在硬件设备（包括显示器）连接到 PC 时会自动下载并安装驱动程序。此功能旨在确保硬件兼容性并在无需用户干预的情况下提供更新的功能。然而，同一机制也可以随驱动程序包一起交付来自硬件制造商的配套应用程序，在本例中包括具有提升系统权限的非沙箱软件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://support.microsoft.com/en-US/Windows/Hardware/Drivers/automatically-get-recommended-and-updated-hardware-drivers">Automatically get recommended and updated hardware drivers</a></li>
<li><a href="https://www.howtogeek.com/how-to-update-monitor-drivers/">How to Update Monitor Drivers</a></li>

</ul>
</details>

**社区讨论**: 社区成员强调实际情况比标题描述的更严重，指出该软件在零用户交互下静默安装，具有无沙箱的完整系统访问权限，并在重启后持续存在。多位用户提供了技术变通方案，包括组策略设置和系统属性配置来阻止自动制造商应用程序下载。许多评论者认为微软对允许这一安全漏洞负有主要责任，将其与历史上的 USB 自动运行恶意软件问题相比较，并呼吁微软实施更严格的设备安装策略。

**标签**: `#security`, `#windows`, `#privacy`, `#malware`, `#system-administration`

---

<a id="item-3"></a>
## [Kimi K3 时刻：非美国实验室实现前沿 AI 性能](https://stephen.bochinski.dev/blog/2026/07/18/the-kimi-k3-moment/) ⭐️ 8.0/10

中国初创公司月之暗面（Moonshot AI）发布了 Kimi K3，这是一款面向长周期编程和端到端知识工作的旗舰模型，具有 100 万 token 的上下文窗口，该公司表示它缩小了与美国领先 AI 系统的差距。该模型拥有 2.8 万亿参数，定位为与 OpenAI 的 GPT 5.6 Sol 和 Anthropic 的 Claude Opus 4.8 直接竞争。 Kimi K3 证明非美国 AI 实验室现在也能实现前沿水平的模型性能，且可能成本更低，这挑战了美国 AI 公司的主导地位。这一发展引发了关于模型蒸馏、地缘政治影响以及美国在 AI 领域领先地位可持续性的重要问题。 Kimi K3 的定价为每 100 万 token 输入/输出 $3/$15，相比之下 GPT 5.6 Sol 为 $5/$30，Opus 4.8 为 $5/$25，具有竞争力但并非大幅降低。虽然该模型在整体基准测试上仍落后于 Anthropic 的 Claude Fable 5 和 OpenAI 的 GPT 5.6 Sol，但它提供 100 万 token 的上下文窗口，并以开放权重发布，支持定制化和本地部署。

hackernews · sbochins · 7月18日 17:32 · [社区讨论](https://news.ycombinator.com/item?id=48960218)

**背景**: 知识蒸馏是一种机器学习技术，较小的

**标签**: `#AI`, `#LLM`, `#Kimi K3`, `#Distillation`, `#Open Weights`

---

<a id="item-4"></a>
## [Stack Overflow 活跃度下降数据可视化引发关于 AI 及其他原因的讨论](https://data.stackexchange.com/stackoverflow/query/1953768#graph) ⭐️ 8.0/10

来自 Stack Exchange 数据浏览器的数据可视化显示 Stack Overflow 的活跃度随时间明显下降，引发了包含 397 条评论和 342 个点赞的高参与度社区讨论。评论者们在争论 ChatGPT 等 AI 工具、社区政策还是 Prosus 收购是导致这一下降的主要原因。 Stack Overflow 十多年来一直是软件开发人员的基础资源，其活跃度下降标志着开发人员获取和分享知识的方式发生了重大转变。这场多层面的讨论表明，该平台的发展轨迹可能并非仅仅由于 AI 工具，还源于长期存在的社区动态和企业决策，这为其他在线社区提供了经验教训。 图表显示 Stack Overflow 的活跃度实际上在 2014 年就达到了峰值，远早于 ChatGPT 等 AI 工具的普及，而同期软件工程劳动力却大幅增长。部分评论者还指出，在 Stack Overflow 于 2021 年被 Prosus 以 18 亿美元收购后，活跃度出现了明显下降。

hackernews · secretslol · 7月18日 11:12 · [社区讨论](https://news.ycombinator.com/item?id=48956949)

**背景**: Stack Overflow 是一个面向程序员的问答网站，历来是互联网上技术知识访问量最大的网站之一。该平台以其严格的审核政策而闻名，这些政策旨在保持质量，但往往对新用户设置了很高的参与门槛。2021 年，该公司被欧洲科技投资者 Prosus 以 18 亿美元收购。ChatGPT 等 AI 聊天机器人的兴起为开发人员提供了一种替代方案，可以快速获得编程帮助，而无需经历社区审核的摩擦。

**社区讨论**: 社区讨论展现了对活跃度下降的多种观点，有人认为 Stack Overflow 不友好的审核机制和缺乏社区建设功能早在 AI 出现之前就扼杀了这个网站。另一些人指出活跃度在 2014 年就已达峰值，比 ChatGPT 早了十年，表明文档和问题追踪系统的改善等更广泛的趋势也起到了作用，还有评论者幽默地提到，LLM 从来不会让他觉得提问是一件愚蠢的事。

**标签**: `#stack-overflow`, `#ai-impact`, `#community-dynamics`, `#data-visualization`, `#developer-tools`

---

<a id="item-5"></a>
## [Meta 拟向 Anthropic 出租百亿美元 AI 算力](https://www.nytimes.com/2026/07/17/technology/meta-anthropic-ai-computing-power.html) ⭐️ 8.0/10

Meta 正与 Anthropic 谈判，拟将其 AI 数据中心算力租予后者，潜在交易规模达 100 亿美元，为期两年，由 Anthropic 于今年 6 月提出方案，按月付款。双方均可提前退出，但知情人士称谈判尚处早期阶段，未必能最终成交。 这笔交易标志着顶级科技公司在 AI 基础设施的货币化和分配方式上发生重大转变，Meta 试图利用其庞大的算力投资开辟收入来源，同时缓解投资者对其巨额资本支出的质疑。这也凸显了整个行业 AI 算力严重稀缺的现状，迫使像 Anthropic 这样资金充裕的初创公司也不得不寻求租赁安排，而非自建基础设施。 根据拟议方案，Anthropic 将按月付款，双方均可提前退出，这表明在长期算力需求不确定的情况下保留了灵活性。Meta 今年计划投入高达 1450 亿美元，其中大量用于 AI 与数据中心建设，算力租赁成为抵消巨额支出的战略性手段。

telegram · zaihuapd · 7月18日 01:14

**背景**: Anthropic 是一家总部位于旧金山的 AI 安全与研究公司，以其与 OpenAI GPT 竞争的 Claude 系列大语言模型而闻名。Meta 一直在积极扩张其 AI 基础设施，2026 年预计资本支出高达 1350 至 1450 亿美元，包括面积堪比曼哈顿的数据中心集群。整个行业正掀起一波算力租赁热潮，Hyperscale Data 和 SpaceX 等公司也在探索或执行类似交易，以满足不断激增的 AI 训练和推理算力需求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Anthropic">Anthropic - Wikipedia</a></li>
<li><a href="https://entrepreneurloop.com/meta-anthropic-compute-deal-inside-the-10-billion-data-center-lease-talks/">Meta Anthropic Compute Deal: Inside the $10 Billion Data Center Lease Talks</a></li>
<li><a href="https://techxplore.com/news/2026-01-meta-ad-business-fuel-massive.html">Meta leans on improved ad business to fuel massive AI spending</a></li>

</ul>
</details>

**标签**: `#Meta`, `#Anthropic`, `#AI Infrastructure`, `#Compute Leasing`, `#AI Industry`

---

<a id="item-6"></a>
## [SpaceX 与五角大楼谈判提供 AI 算力，交易或达数十亿美元](https://www.wsj.com/tech/ai/spacex-in-talks-to-provide-computing-power-for-pentagons-ai-push-15e752e4) ⭐️ 8.0/10

SpaceX 正与美国国防部谈判，拟向五角大楼提供用于运行人工智能模型的数据中心算力，交易金额可能高达数十亿美元。知情人士称谈判仍在进行中，存在破裂可能，但若达成协议，将进一步加深 SpaceX 与五角大楼的合作关系。 这笔交易标志着 SpaceX 从发射服务和卫星互联网向云计算和国家安全 AI 基础设施的战略扩展，使其成为亚马逊、谷歌和微软等超大规模云服务商的竞争对手。数十亿美元的潜在规模凸显了国防领域对 AI 算力需求的快速增长，以及商业航天公司在军事技术中日益重要的角色。 五角大楼已批准 SpaceX 以及亚马逊、谷歌、微软和甲骨文等公司在 Impact Level 6 和 Impact Level 7 机密环境中部署 AI 模型及相关技术。SpaceX 近月还与 Anthropic 和谷歌签署了类似算力供应协议，并向 FCC 提交计划，拟利用数百万颗卫星将云计算和 AI 算力扩展至太空轨道。

telegram · zaihuapd · 7月18日 01:44

**背景**: 五角大楼一直在加速获取云计算能力，以支持国家安全和日常军事行动中的 AI 应用。该部门近期与包括 SpaceX、OpenAI、谷歌、NVIDIA、微软、甲骨文和亚马逊云服务在内的八家公司达成协议，允许它们在国防部的机密网络环境中部署 AI 产品。SpaceX 通过其 Colossus 数据中心建设 AI 基础设施业务，向超大规模云服务商和 AI 初创公司出租云计算能力，其中包括与 Reflection AI 签署的价值高达 63 亿美元的协议。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/06/22/spacex-ai-colossus-data-center-reflection.html">SpaceX signs computing power deal with open-source AI startup Reflection worth up to $6.3 billion</a></li>
<li><a href="https://www.nextgov.com/artificial-intelligence/2026/05/pentagon-makes-agreements-7-companies-add-ai-classified-networks/413264/">Pentagon makes agreements with 8 companies to add AI to classified networks - Nextgov/FCW</a></li>
<li><a href="https://www.fool.com/investing/2026/06/28/spacex-just-spent-60-billion-on-artificial-intelli/">SpaceX Just Spent $60 Billion on Artificial Intelligence (AI). Could Elon Musk Be Building the Next Amazon? | The Motley Fool</a></li>

</ul>
</details>

**标签**: `#AI Infrastructure`, `#SpaceX`, `#Pentagon`, `#Cloud Computing`, `#National Security`

---

<a id="item-7"></a>
## [Kimi K3 首登 DeepSWE 基准测试第三名，成为首个达到前沿水平的开源权重模型](https://deepswe.datacurve.ai/blog/deepswe-v1-1) ⭐️ 8.0/10

2026 年 7 月 17 日，AI 编程智能体基准测试 DeepSWE 更新了结果，Kimi K3 首次登上第三名。Kimi K3 是首个在该基准上接近前沿性能的开源权重模型，成绩接近 Claude Fable 5 和 GPT-5.6 Sol 等闭源模型。 这一里程碑表明，开源权重模型在复杂的长期软件工程任务中正在缩小与闭源模型的差距。它标志着前沿级编程智能体能力正变得更加普及，有望加速 AI 辅助软件开发的创新。 Kimi K3 是一个拥有 2.8 万亿参数的模型，采用了 Kimi Delta Attention、Attention Residuals、原生视觉能力以及最高 1,048,576 token 的上下文窗口。DeepSWE 被设计为一个无污染的长期软件工程基准测试，减少了基准泄漏，使其成为衡量编程智能体能力的更可靠标准。

telegram · zaihuapd · 7月18日 02:29

**背景**: DeepSWE 是一个长期软件工程基准测试，旨在通过原始、复杂的任务来评估前沿编程智能体，这些任务更贴近真实世界的软件开发场景。开源权重模型是指其训练参数（权重）公开发布可供下载的 AI 模型，允许用户运行、研究和修改该模型。Kimi K3 由月之暗面开发，是首个达到 2.8 万亿参数的开源模型，完整模型权重计划于 2026 年 7 月 27 日前发布。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.kimi.com/blog/kimi-k3">Kimi K 3 Tech Blog: Open Frontier Intelligence</a></li>
<li><a href="https://platform.kimi.ai/docs/guide/kimi-k3-quickstart">Kimi K 3 - Kimi API Platform</a></li>
<li><a href="https://deepswe.datacurve.ai/">DeepSWE measures frontier coding agents on original, long-horizon...</a></li>

</ul>
</details>

**标签**: `#AI Agents`, `#Software Engineering`, `#Benchmark`, `#Open Source`, `#LLM`

---

<a id="item-8"></a>
## [台积电 A14 制程进展超预期，良率与性能双双逼近 90%](https://www.tomshardware.com/tech-industry/semiconductors/tsmc-confirms-significant-yield-and-performance-improvements-in-a14-update-strong-interest-from-ai-hpc-and-smartphone-customers) ⭐️ 8.0/10

台积电在财报电话会上表示，A14（1.4 纳米级）制程在过去三个月进展迅速，内部测试的器件性能已接近目标水平的 90%，256 Mb SRAM 良率也接近 90%，而今年 4 月这两项数据分别仅为 85%和 80%以上。CEO 魏哲家透露，智能手机、AI 和高性能计算客户兴趣强烈，新设计流片进度快于计划，量产目标为 2028 年下半年。 A14 是台积电继 N2 之后的下一个完整节点制程，对 AI 硬件和高性能计算生态系统具有关键意义，良率和性能的提升直接关系到芯片的成本效益和性能表现。加速的时间线表明台积电在先进半导体制造领域持续保持技术领先地位，这对全球半导体供应链以及设计下一代 AI 加速器和移动处理器的公司具有战略重要性。 与 N2 相比，A14 预计在相同功耗下性能提升 10%至 15%，在相同频率下功耗降低 25%至 30%，逻辑晶体管密度提高 23%。A14 采用第二代 GAA 纳米片晶体管，可沿用 N2 积累的经验，这是其开发进度大幅领先同期 N2 的关键原因。

telegram · zaihuapd · 7月18日 05:00

**背景**: 台积电的 A14 是 1.4 纳米级制程节点，是继 N2（2 纳米）之后的下一个完整节点升级。GAA（环绕栅极）纳米片晶体管是在先进节点取代传统 FinFET 结构的晶体管架构，提供更好的静电控制能力并延续摩尔定律。SRAM 良率是半导体制造中的关键指标，因为 SRAM 在现代芯片中占据很大比例——在移动 SoC 中高达 60%，在 AI 加速器中也占相当大部分，因此即使是微小的良率提升也具有重要的经济意义。台积电的路线图还包括 A13（专注于密度提升的缩减版）和 A12（计划 2029 年，将加入背面供电轨道技术）。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://wccftech.com/tsmc-1-4nm-process-faces-no-obstacles-as-risk-production-to-start-in-2027/">TSMC ’s Facing No Development Obstacles With Its Next-Generation...</a></li>
<li><a href="https://www.remio.ai/post/tsmc-raises-2026-capital-spending-to-60-64-billion-as-a14-stays-on-track">TSMC Raises 2026 Capital Spending to $60-$64 Billion as A 14 Stays...</a></li>
<li><a href="https://www.patsnap.com/resources/blog/articles/gaa-transistors-at-2nm-nanosheet-architecture-explained/">GAA transistors at 2nm: nanosheet architecture explained | PatSnap</a></li>

</ul>
</details>

**标签**: `#semiconductors`, `#tsmc`, `#manufacturing`, `#ai-hardware`, `#process-node`

---

<a id="item-9"></a>
## [特朗普政府拟设类似 FINRA 的独立机构审查顶尖 AI 模型](https://www.bloomberg.com/news/articles/2026-07-17/us-considers-creating-finra-like-watchdog-to-vet-top-ai-models) ⭐️ 8.0/10

特朗普政府正考虑设立一个类似金融业监管局（FINRA）的独立 AI 监管机构，负责审查顶尖人工智能模型的安全性，该方案目前正由白宫幕僚长苏茜·威尔斯审阅，由财政部长斯科特·贝森特牵头制定。该计划旨在回应华尔街对网络安全的担忧以及硅谷对政府临时性管控措施的不满，让两大行业在联合制定安全标准方面拥有更大发言权。 这标志着美国 AI 安全监管可能从临时性政府管控转向结构化、行业协作的监督模式，将对顶尖 AI 模型在美国的部署和治理产生重大影响。该提案与 Google DeepMind 首席执行官德米斯·哈萨比斯等主要 AI 实验室高管的呼吁方向一致，且涉及高级别官员，使其成为美国 AI 监管政策的关键进展。 拟议的机构将向证券交易委员会（SEC）汇报，并以 FINRA——证券行业的自律监管组织——为蓝本。该计划仍处于草案阶段，尚未经总统特朗普审阅，相关框架仍可能调整；此前，Anthropic 和 OpenAI 均因美国政府要求修改或限制发布最新模型而提出异议。

telegram · zaihuapd · 7月18日 05:45

**背景**: FINRA（金融业监管局）是美国一家非营利性自律监管组织（SRO），负责监管经纪公司和注册证券代表，在 SEC 的监督下运作。该机构成立于 2007 年，由 NASD 和 NYSE 的监管部门合并而成，其行业资助、行业参与的监管模式目前正被考虑作为 AI 监管的模板。该提案出台之际，AI 公司与政府之间围绕安全限制的紧张关系日益加剧，Google DeepMind 首席执行官德米斯·哈萨比斯近期呼吁建立一个由美国主导、行业资助的 AI 安全监管机构，以应对通用人工智能（AGI）相关的风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://baike.baidu.com/item/美国金融业监管局/9213493">美国金融业监管局_百度百科 FINRA Homepage About FINRA FINRA:监管、保护投资者与市场监督 美国FINRA：监管机构介绍、职能与查询方法-财经导航 - 专业的财经资讯... 什么是FINRA | 金融业监管局</a></li>
<li><a href="https://www.cnbc.com/2026/07/14/google-deepmind-demis-hassabis-us-led-ai-standards-body.html">Google DeepMind chief Demis Hassabis calls for U.S. to spearhead AI standards body</a></li>
<li><a href="https://www.inc.com/georgia-fearn/google-deepmind-founder-wall-street-style-watchdog-stop-dangerous-ai/91373798">Google DeepMind's Co-Founder Wants a Wall Street-Style Watchdog to Stop Dangerous AI</a></li>

</ul>
</details>

**标签**: `#AI Regulation`, `#US Policy`, `#AI Safety`, `#Government`, `#Industry News`

---

<a id="item-10"></a>
## [美国要求分享韩国芯片商 AI 热潮超额利润](https://www.koreatimes.co.kr/business/tech-science/20260716/us-seeks-share-of-korean-chipmakers-excess-profits-source) ⭐️ 8.0/10

据报道，美国正寻求分享韩国半导体企业因全球 AI 芯片热潮获得的巨额超额利润，美国副贸易代表认为美方企业大量采购韩国半导体为韩企盈利做出了贡献，理应分得部分利润，但韩方官员对此说法未予证实。 这代表了一种全新且可能具有范式转变意义的贸易政策立场——美国基于采购贡献向盟国企业要求利润分享，这可能重塑国际贸易关系和半导体供应链经济格局，并直接影响三星和 SK 海力士等主要企业，同时为向其他盟友芯片商提出类似要求开创先例。 今年上半年韩国半导体出口达 1924.3 亿美元，同比增长 162.5%，其中对美出口增长 91.3%至 264 亿美元。美国商务部长上周再次呼吁三星和 SK 海力士在美建设存储芯片工厂，同时韩国国内也在讨论芯片商是否应与分包商乃至公众分享超额利润。

telegram · zaihuapd · 7月18日 14:20

**背景**: 美国《芯片法案》向在美建厂的外国半导体企业提供补贴，其中 SK 海力士为其 38.7 亿美元的印第安纳州 HBM 封装工厂获得了 4.5 亿美元资金，三星则正在为其得克萨斯州泰勒工厂谈判补贴事宜。拜登时期的《芯片法案》包含

**标签**: `#semiconductors`, `#geopolitics`, `#trade-policy`, `#AI-chips`, `#Samsung`

---
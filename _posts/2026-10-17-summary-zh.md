---
layout: default
title: "Horizon Summary: 2026-10-17 (ZH)"
date: 2026-10-17
lang: zh
---

> 从 37 条内容中筛选出 7 条重要资讯。

---

1. [Claude 揭开 NIST ECDSA 曲线种子来源之谜](#item-1) ⭐️ 9.0/10
2. [特斯拉 Roadster](#item-2) ⭐️ 8.0/10
3. [Claude Code 团队如何进行 AI 辅助代码审查](#item-3) ⭐️ 8.0/10
4. [Big Fish：利用 OpenBSD 中一个存在 37 年的内核漏洞](#item-4) ⭐️ 8.0/10
5. [ORL 将扩散语言模型加速至单卡 RTX 5090 上 2,788 tokens/s](#item-5) ⭐️ 8.0/10
6. [商务部拟对 AI、生物医药、光伏领域 40 项技术实施临时出口登记](#item-6) ⭐️ 8.0/10
7. [Anthropic IPO 估值预期降至 1.5 万亿美元](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Claude 揭开 NIST ECDSA 曲线种子来源之谜](https://www.anthropic.com/research/ecdsa-curve-origins) ⭐️ 9.0/10

Anthropic 的 Claude AI 发现 NIST 椭圆曲线 P-192、P-224、P-256、P-384 和 P-521 的种子是使用 C 标准库的 lrand48 随机数生成器配合 Unix 时间戳作为种子生成的，而非许多人猜测的通过对某个短语进行哈希运算产生。该发现在不到半小时内完成，解决了一个持续十多年的密码学谜题。 这一发现终结了多年来关于 NSA 故意选择带有隐藏弱点的曲线种子的猜测，这种担忧曾影响密码学标准的选择并引发了对 NIST 曲线的不信任。同时，这也是 LLM 应用于密码分析的里程碑式演示，表明 AI 模型能够在人类专家多年未果的专业技术领域中有成效地探索假设。 第五个二进制曲线种子 B-163 不符合 Claude 尝试的任何模式，至今无法解释；一种合理的推测是在发布过程中有人输错了一个数字。Anthropic 选择了两个悬赏金额中较高的一个，并将其捐赠给了 ISRG（互联网安全研究组）。批评者指出，虽然生成方法已确认，但长达数月的选择过程中被丢弃的候选曲线无法被审查，因此基于选择产生弱点的可能性无法完全排除。

hackernews · ahlCVA · 10月16日 18:55 · [社区讨论](https://news.ycombinator.com/item?id=50122800)

**背景**: NIST 于 2000 年将 ECDSA 纳入 FIPS 186-2 标准，规定了用于数字签名的标准椭圆曲线。每条曲线由一个种子值定义，NIST 从未解释这些种子是如何选择的，这引发了 NSA 可能选择了仅该机构可利用的、带有已知漏洞的曲线种子的猜测。Daniel Bernstein 和 Tanja Lange 等研究人员早在 1999 年就提出了后门担忧。最终有人悬赏 12,000 美元寻找能够追溯种子来源的人，Filippo Valsorda 等人对此进行了推广。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.explainx.ai/blog/claude-ecdsa-nist-curve-seeds-lrand48-anthropic-frontier-red-team-backdoor-question-2026">ECDSA Curve Seeds Solved: Claude Found lrand48 (2026 ...</a></li>
<li><a href="https://www.unite.ai/anthropic-says-claude-traced-nist-ecdsa-curve-seeds-to-a-1990s-rng/">Anthropic Says Claude Traced NIST ECDSA Curve Seeds to a ...</a></li>
<li><a href="https://www.itsecuritylocksmith.co.uk/the-nist-elliptic-curve-bounty/">The NIST Elliptic Curve seeds, the NSA and the $12k bounty</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论（595 分，249 条评论）反映了既好笑又释然的混合情绪，有用户调侃说负责此事的 NSA 员工可能已经偷偷笑了 25 年，还有人戏称这是"为 srand48(time(NULL)) 戴了 13 年锡纸帽"。更严肃的技术评论则提醒，虽然生成方法已确认，但选择过程仍不透明——被丢弃的候选曲线无法审查，因此基于曲线选择的攻击在理论上仍然可能。多位评论者赞赏 Anthropic 将悬赏金捐赠给 ISRG，并推测无法解释的 B-163 种子可能只是一个笔误。

**标签**: `#cryptography`, `#ai`, `#security`, `#elliptic-curves`, `#llm`

---

<a id="item-2"></a>
## [特斯拉 Roadster](https://www.tesla.com/roadster) ⭐️ 8.0/10

特斯拉发布了一款配备冷气推进器和火箭发动机的新型 Roadster 原型车，能够悬停并垂直行驶，引发了关于其工程可行性和实际量产可能性的激烈争论。

hackernews · shekhar101 · 10月16日 01:32 · [社区讨论](https://news.ycombinator.com/item?id=50112657)

**标签**: `#tesla`, `#automotive`, `#rocketry`, `#engineering`, `#product-announcement`

---

<a id="item-3"></a>
## [Claude Code 团队如何进行 AI 辅助代码审查](https://claude.dev/blog/solving-code-review-at-anthropic/) ⭐️ 8.0/10

Anthropic 发布了一篇博客文章，详细介绍了 Claude Code 团队如何利用 AI 自动化并扩展代码审查流程，据称每天可处理多达 30,000 个 Pull Request。该系统按风险等级对变更进行分类，并通过自动化检查进行路由，人工注意力仅集中在风险最高的地方。 这种方法预示着软件工程领域可能迎来范式转变：AI 承担大部分代码审查工作量，而人类专注于高风险决策。如果具备可扩展性，它将从根本上重塑工程团队结构、审查流程以及高级工程师所需的核心能力。 该系统采用风险分级路由机制，低风险变更（文档、文案、仅内部功能）在自动化检查通过后无需人工审查即可合并。团队维护着一个随每次事故不断增长的评估套件，审查器的每次变更都会针对完整评估集进行评分。

hackernews · pretext · 10月16日 19:04 · [社区讨论](https://news.ycombinator.com/item?id=50122951)

**背景**: Claude Code 是 Anthropic 的智能体编程工具，可在终端和 IDE 中运行，能够理解代码库、编辑文件和运行命令。传统代码审查需要人工工程师手动阅读并批准 Pull Request，随着团队规模和代码速度的增长，这会成为瓶颈。CodeRabbit 和 Sonar 等 AI 辅助代码审查工具应运而生以解决这一可扩展性挑战，但 Anthropic 的方法似乎在低风险变更的全面自动化方面走得更远。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI Coding Agent, Terminal, IDE</a></li>
<li><a href="https://www.coderabbit.ai/">AI Code Reviews | CodeRabbit | Try for Free.</a></li>
<li><a href="https://www.sonarsource.com/">AI Code Review & Verification Tools | Code Security | Sonar</a></li>

</ul>
</details>

**社区讨论**: 社区情绪高度怀疑，评论者质疑每天 30,000 个 PR 反映的是真正的生产力还是过度的代码流失和反复重写。多位用户对允许 LLM 撰写文档而不经人工审查表示担忧，还有人就每行代码的成本以及团队在该规模下是否真正掌控其代码库展开了讨论。

**标签**: `#AI`, `#code-review`, `#Anthropic`, `#software-engineering`, `#automation`

---

<a id="item-4"></a>
## [Big Fish：利用 OpenBSD 中一个存在 37 年的内核漏洞](https://calif.io/research/big-fish) ⭐️ 8.0/10

安全研究机构 Calif 于 2024 年 10 月 16 日发布了一个概念验证漏洞利用程序，演示了在 OpenBSD 上的本地提权攻击，该攻击链式利用了两个长期存在的内核漏洞，其中最古老的漏洞可追溯至约 37 年前的原始 BSD 源代码。该漏洞利用程序利用了 SysV 共享内存附加计数器中的有符号 16 位短整数溢出（通过 fork 259 个进程触发），结合 use-after-free 竞争条件和 IP 多播选项处理中的越界写入，绕过 SMAP/SMEP 保护机制以获取 root 权限。 这一发现意义重大，因为它表明即使在被广泛认为是最注重安全、审计最严格的操作系统 OpenBSD 中，关键漏洞也可能持续存在数十年。它揭示了手动代码审查在捕捉某些类别漏洞（尤其是整数溢出和竞争条件组合）方面的局限性，并引发了关于模糊测试或静态分析等自动化工具是否能更早发现此问题的重要讨论。 核心漏洞在于 SysV 共享内存附加计数器被实现为有符号 16 位短整型，这意味着它在溢出前最多只能计数到 32,767。研究人员通过 fork 259 个进程来溢出该计数器，从而制造了 use-after-free 条件，然后将其与另一个线程进行竞争，同时利用 IP 多播选项处理中的越界写入来绕过 SMAP（管理模式访问防护）和 SMEP（管理模式执行防护）等现代硬件安全特性。

hackernews · rs_rs_rs_rs_rs · 10月16日 14:44 · [社区讨论](https://news.ycombinator.com/item?id=50118977)

**背景**: OpenBSD 是一个类 Unix 操作系统，以其主动的安全策略和严格的源代码审计而闻名，开创了 OpenSSH 和主动安全审计概念等安全创新。SysV 共享内存子系统是 System V IPC（进程间通信）机制的一种，允许多个进程共享内存区域，其中附加计数器用于跟踪有多少进程映射了给定的内存段。SMAP 和 SMEP 是 Intel 引入的 CPU 硬件安全特性，用于防止内核访问或执行用户空间内存中的代码，从而使漏洞利用变得显著更加困难。该漏洞可追溯到 OpenBSD 分支之前的原始 BSD 源代码，早于 OpenBSD 自身广泛的安全审计。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cybersecuritynews.com/37-year-old-kernel-openbsd-flaw/">37-Year-Old Kernel Flaw Exploited to Gain Root Access on ...</a></li>
<li><a href="https://daily.dev/posts/big-fish-exploiting-a-37-year-old-kernel-bug-in-openbsd-u6hc8g4lt">Big Fish: Exploiting a 37-Year-Old Kernel Bug in OpenBSD</a></li>
<li><a href="https://www.openbsd.org/security.html">OpenBSD: Security</a></li>

</ul>
</details>

**社区讨论**: 社区讨论集中在该漏洞令人惊讶的持久性以及检测此类漏洞类别的挑战上。一位评论者指出，NetBSD 在 1999 年 8 月的一次代码重写中意外修复了相同的漏洞，而另一位评论者则提出了一个关键问题：模糊测试或静态分析是否真的能发现这类漏洞，还是需要人类对漏洞利用原语的推理才能发现。

**标签**: `#security`, `#kernel`, `#openbsd`, `#exploitation`, `#vulnerability-research`

---

<a id="item-5"></a>
## [ORL 将扩散语言模型加速至单卡 RTX 5090 上 2,788 tokens/s](https://www.reddit.com/r/MachineLearning/comments/1x7qgr0/research_2788_tokenss_on_a_single_rtx_5090_with_a/) ⭐️ 8.0/10

研究人员提出了 ORL（On-Policy Residual Learning），该方法通过在模型自身实时生成的轨迹上训练，并利用相邻熵收缩（Adjacent Entropy Contraction）在每步去噪中更快地降低不确定性，从而加速扩散语言模型。结合名为 dlmrt 的基于 CUDA Graph 的定制推理引擎，该方法在单卡 RTX 5090 上实现了 2,788 tokens/s 的生成速度，端到端吞吐量最高提升 6.9 倍，且所有模型、训练代码和推理引擎均已完全开源。 扩散语言模型是自回归 LLM 的新兴替代方案，但其在迭代去噪过程中收敛缓慢的问题一直限制了实际应用。ORL 直接解决了这一瓶颈，证明扩散语言模型在吞吐量上可以与 DFlash 和 EAGLE3 等自回归投机解码方法相媲美甚至超越，有望推动基于扩散的文本生成走向生产环境。 ORL 的两项核心技术是：在策略残差学习——通过重放当前模型生成的精确残差状态来避免训练与推理的分布不匹配；以及相邻熵收缩——通过门控损失仅推动不确定的预测。dlmrt 引擎将整个去噪循环捕获到 CUDA Graph 中在 GPU 端执行，并支持 Blackwell GPU 上的 NVFP4 推理；所有报告的数据均为单请求（batch size 1）峰值结果，而非并发请求的聚合吞吐量。

reddit · r/MachineLearning · /u/arty_photography · 10月16日 20:03

**背景**: 扩散语言模型（dLLM）通过迭代去噪而非逐 token 的自回归预测来生成文本，能够并行地细化和确定多个 token。与每次只生成一个 token 的自回归模型不同，扩散模型从完全掩码的序列出发，逐步揭示 token，其原理类似于 Stable Diffusion 等图像扩散模型。其核心挑战在于减少收敛所需的前向传播次数，ORL 通过将前一步预测作为残差上下文传递，并在策略上训练以匹配推理条件来解决这一问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/blog/ProCreations/diffusion-language-model">Diffusion Language Models: The New Paradigm - Hugging Face</a></li>
<li><a href="https://arxiv.org/abs/2502.09992">[2502.09992] Large Language Diffusion Models - arXiv.org Diffusion Language Models: An Experimental Analysis Awesome Diffusion Language Models How to Build a Diffusion Language Model | Kuleshov Group Large Language Diffusion Models</a></li>

</ul>
</details>

**标签**: `#diffusion-models`, `#language-models`, `#inference-optimization`, `#open-source`, `#machine-learning`

---

<a id="item-6"></a>
## [商务部拟对 AI、生物医药、光伏领域 40 项技术实施临时出口登记](https://aqygzj.mofcom.gov.cn/flzc/gzjgfxwj/art/2026/art_c99f95ca0cd043829ac9991495fc283c.html) ⭐️ 8.0/10

商务部拟修订《中国禁止出口限制出口技术目录》，就人工智能、生物医药、光伏三个领域共 40 项技术实施临时出口登记公开征求意见。其中人工智能领域涉及大模型、智能体、算力集群等 23 项技术，生物医药领域涉及细胞和基因治疗、小核酸药等 5 项技术，光伏领域涉及多晶硅、硅片、电池制造等 12 项技术。已通过开源、发表学术论文等方式进入公共领域的技术不纳入管理范围。 这一监管动向表明中国有意加强对战略性技术出口的管控，尤其是在全球竞争激烈的人工智能大模型和算力集群领域。该政策可能对国际技术转移、跨境研发合作以及这三个关键领域的全球供应链产生重大影响，而开源豁免条款则为学术和开放协作保留了通道。 光伏领域的技术管理范围不仅限于技术本身，还包含承载相关技术的关键和核心设备。生物医药领域对不涉及所有权转让的对外授权模式适用自动许可等便利措施，为特定商业模式提供了较轻的监管负担。人工智能领域的 23 项技术占比最大，反映出该领域在当前出口管制考量中的战略优先地位。

telegram · zaihuapd · 10月16日 09:12

**背景**: 中国通过《中国禁止出口限制出口技术目录》实施技术出口管制，将技术分为禁止出口和限制出口两类。临时出口登记要求出口商在出口受控技术前向主管部门登记，相比完整的出口许可证制度属于较轻的监管措施。此次涉及的三个领域——人工智能、生物医药和光伏——均是中国具有显著技术能力和全球市场份额的战略性领域。例如，小核酸药物是基于 RNA 干扰（RNAi）或反义寡核苷酸（ASO）技术的新型疗法，通过靶向 mRNA 调控基因表达。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zhuanlan.zhihu.com/p/1979127551893985088">小核酸药物行业深度：发展现状、发展空间、技术突破、产业链及相关公...</a></li>
<li><a href="https://zhuanlan.zhihu.com/p/2075906064407597214">CDE老师文章解读 | 小核酸药物临床研发和评价的思考</a></li>

</ul>
</details>

**标签**: `#AI policy`, `#export controls`, `#regulation`, `#China`, `#technology transfer`

---

<a id="item-7"></a>
## [Anthropic IPO 估值预期降至 1.5 万亿美元](https://www.reuters.com/business/finance/investors-temper-anthropic-ipo-valuation-expectations-over-revenue-growth-2026-10-15/) ⭐️ 8.0/10

尽管第三季度营收高达 168 亿美元，但由于增长放缓、模型价格竞争以及算力成本上升，投资者已将 Anthropic 的 IPO 估值预期下调至 1.5 万亿美元。

telegram · zaihuapd · 10月16日 15:46

**标签**: `#Anthropic`, `#IPO`, `#AI Valuation`, `#Investment`, `#Market Analysis`

---
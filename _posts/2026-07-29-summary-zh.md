---
layout: default
title: "Horizon Summary: 2026-07-29 (ZH)"
date: 2026-07-29
lang: zh
---

> 从 43 条内容中筛选出 6 条重要资讯。

---

1. [Anthropic 研究人员使用 Claude 发现新型密码学弱点](#item-1) ⭐️ 9.0/10
2. [月之暗面超额融资 35 亿美元，估值达 350 亿美元并计划赴港 IPO](#item-2) ⭐️ 9.0/10
3. [TurboFieldfare：在 M 系列 Mac 上仅用 2GB 内存运行 Gemma 4 26B](#item-3) ⭐️ 8.0/10
4. [HANDBOOK.md 基准测试表明长策略文档无法可靠约束 AI 智能体](#item-4) ⭐️ 8.0/10
5. [AI 蠕虫可通过 Copilot for Word 自我传播](#item-5) ⭐️ 8.0/10
6. [俄罗斯联邦安全局对 Telegram 创始人杜罗夫提起刑事指控并发出国际通缉](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Anthropic 研究人员使用 Claude 发现新型密码学弱点](https://simonwillison.net/2026/Jul/28/discovering-cryptographic-weaknesses-with-claude/#atom-everything) ⭐️ 9.0/10

Anthropic 研究人员使用 Claude Mythos Preview 发现了 HAWK 密码签名方案和缩减轮数（7 轮）AES-128 中此前未知的数学弱点。该模型运行了约 60 小时，估计 API 成本为 10 万美元，人类研究员的主要干预是鼓励模型不要放弃，并追求真正值得发表的发现。 这代表了密码学研究中的范式转变，证明大语言模型可以作为积极的研究伙伴，能够发现新的数学缺陷，而不仅仅是总结已有知识。公开提示词和可复现的代码库增加了透明度，而 CryptanalysisBench（与苏黎世联邦理工、特拉维夫大学和海法大学合作）的创建为评估 LLM 密码分析能力建立了新的评测框架。 这两项发现的弱点对当今的计算机系统都没有实际影响——AES 攻击仅针对缩减的 7 轮版本，而非完整的 AES-128。公开的提示词显示，模型倾向于在困难问题上放弃，需要大量鼓励才能追求新攻击而非简单成果，这表明人类引导在研究过程中仍然至关重要。

rss · Simon Willison · 7月28日 22:45

**背景**: HAWK 是一种基于格的密码签名方案，旨在抵御经典计算机和量子计算机的攻击，是 NIST 后量子密码标准化过程的候选方案。AES-128 是广泛部署的对称加密标准；密码分析人员通常研究缩减轮数版本（例如 10 轮中的 7 轮）来理解密码的安全边际并开发攻击技术。密码分析涉及寻找数学弱点，使攻击者能够在不知道密钥的情况下破解加密或伪造签名。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hawk-sign.info/">Hawk</a></li>
<li><a href="https://en.wikipedia.org/wiki/Advanced_Encryption_Standard">Advanced Encryption Standard - Wikipedia</a></li>
<li><a href="https://eprint.iacr.org/2019/622.pdf">Extended Truncated-diﬀerential Distinguishers on Round-reduced AES</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论对公开的提示词表现出浓厚兴趣，这些提示词揭示了引导 AI 进行新研究的迭代且有时混乱的过程。评论者注意到了显著的成本（约 10 万美元）以及人类干预仍然必不可少的事实，引发了关于这究竟是真正的自主 AI 研究还是复杂的人机协作的讨论。

**标签**: `#cryptography`, `#AI-research`, `#Claude`, `#security`, `#Anthropic`

---

<a id="item-2"></a>
## [月之暗面超额融资 35 亿美元，估值达 350 亿美元并计划赴港 IPO](https://www.bloomberg.com/news/articles/2026-07-29/china-s-moonshot-ai-passes-funding-goal-to-hit-35-billion-value) ⭐️ 9.0/10

月之暗面（Moonshot AI）完成 35 亿美元融资，投后估值达 350 亿美元，远超最初 10 至 20 亿美元的目标，主要受其突破性模型 Kimi K3 推动。公司已启动新一轮融资，pre-money 估值 500 亿美元，计划最早今年内在香港 IPO。 这是中国 AI 公司规模最大的融资轮次之一，表明中国 AI 生态已能产出接近前沿水平的模型，正在挑战西方的主导地位。Kimi K3 发布后 reportedly 引发科技股抛售，被业界称为又一个「DeepSeek 时刻」，凸显了美国 AI 巨头面临的竞争压力日益加剧。 Kimi K3 是一个 2.8 万亿参数的混合专家（MoE）模型，具备原生视觉能力和 100 万 token 上下文窗口，以开源权重形式提供，输入 token 定价为每百万 3 美元，输出为每百万 15 美元。公司 6 月年化经常性收入达 3 亿美元，K3 发布后日销售额增长至少 6 倍。

telegram · zaihuapd · 7月29日 10:12

**背景**: 月之暗面是一家总部位于北京的 AI 初创公司，成立于 2023 年，以其 Kimi AI 助手和大语言模型闻名。「DeepSeek 时刻」指的是 DeepSeek-R1 引发的行业震荡——这款低成本中国 AI 模型挑战了美国 AI 主导地位的假设，并暴露了美国主要 AI 公司商业模式的深层裂痕。Kimi K3 接近前沿的性能引发了类似比较，表明中国 AI 实验室正在缩小与西方前沿模型的差距。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://modal.com/library/moonshot/kimi-k3">Kimi K3 by Moonshot AI | Model Library | Modal</a></li>
<li><a href="https://www.bbc.com/news/articles/cy9w4q8pgp0o">China's Moonshot AI claims Kimi K3 can rival OpenAI and Anthropic</a></li>
<li><a href="https://www.noumenal.ai/post/the-deepseek-moment">The “ DeepSeek moment ” | Noumenal Labs</a></li>

</ul>
</details>

**标签**: `#moonshot-ai`, `#kimi-k3`, `#ai-funding`, `#china-ai`, `#ipo`

---

<a id="item-3"></a>
## [TurboFieldfare：在 M 系列 Mac 上仅用 2GB 内存运行 Gemma 4 26B](https://github.com/drumih/turbo-fieldfare) ⭐️ 8.0/10

TurboFieldfare 是一个全新的开源 Swift/Metal 推理引擎，可在任意 M 系列 Mac 上仅用约 2GB 内存运行 4-bit 量化的 Gemma 4 26B-A4B-IT 模型，在 8GB M2 MacBook Air 上达到 5–6 tok/s，在 M5 MacBook Pro 上达到 31–35 tok/s。其核心原理是将共享权重和 KV cache 保留在内存中，同时通过有界并行 pread 和小型专家缓存按需从 SSD 流式加载 MoE 路由专家。 该项目展示了一种利用 Mixture-of-Experts 架构稀疏激活特性在内存受限设备上运行大型 MoE 模型的实用方法，有望让入门级硬件也能运行此前无法承载的端侧 AI 模型。它挑战了 4-bit 量化权重总共约占 14GB，但仅共享权重和 KV cache（约 2GB）驻留在内存中；路由专家按 token 从 SSD 获取，使用有界并行 pread，同时 GPU 并发执行共享层计算。该项目还包含一个实验性的 OpenAI 兼容本地服务器，支持流式输出和工具调用，完整功能需要 macOS 26 以支持 Swift 4.0 语言特性（旧版 macOS 可通过小幅代码修改运行，但会损失 2.4 倍的 prefill 加速）。

hackernews · gitpusher42 · 7月29日 15:05 · [社区讨论](https://news.ycombinator.com/item?id=49098510)

**背景**: Mixture-of-Experts (MoE) 模型通过门控网络将每个 token 动态路由到少量专门的专家子网络，意味着每次推理只激活模型总参数的一小部分。这种稀疏激活特性意味着虽然完整模型在磁盘上可能非常大，但每次推理步骤只需加载其中一小部分。KV cache 存储之前 token 的键值对以避免自回归生成时的重复计算，其大小随上下文长度增长。传统推理引擎如 llama.cpp 可以使用 mmap 让操作系统按需从磁盘分页加载模型权重，但这种方式缺乏对推理时序的感知；TurboFieldfare 则显式地将 SSD 读取与 GPU 计算同步，以最小化延迟。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained</a></li>
<li><a href="https://magazine.sebastianraschka.com/p/coding-the-kv-cache-in-llms">Understanding and Coding the KV Cache in LLMs from Scratch</a></li>

</ul>
</details>

**社区讨论**: 社区反馈整体非常积极，用户称赞这一新颖方法并质疑为何 AI 行业默认将整个模型加载到内存中。核心技术讨论集中在 TurboFieldfare 与 llama.cpp 的 mmap 策略对比上，有评论者指出 llama.cpp 已经可以在 2GB 内存中运行 26B 模型，但 TurboFieldfare 的优势在于推理感知的 SSD 读取同步。社区还分享了旧版 macOS 的兼容性技巧，多位用户询问跨平台支持（如 Debian、Jetson）以及该工具是否可以完全离线运行。

**标签**: `#on-device-ai`, `#llm-inference`, `#moe`, `#apple-silicon`, `#quantization`

---

<a id="item-4"></a>
## [HANDBOOK.md 基准测试表明长策略文档无法可靠约束 AI 智能体](https://arxiv.org/abs/2607.25398) ⭐️ 8.0/10

一个研究团队发布了 HANDBOOK.md 基准测试，用于评估 AI 智能体在自主多步骤任务中是否能可靠遵守企业策略文档。在涵盖金融、医疗计费、保险、物流和人力资源五个受监管领域的 65 个任务中，30 种模型配置中表现最好的也仅达到 36.2% 的通过率。 这一发现直接挑战了当前常见的部署模式——即将长系统提示或策略文件放入智能体上下文中，并期望其在整个会话中持续遵守。对于在受监管行业部署自主智能体的企业而言，结果表明当前通过上下文内策略文档进行智能体治理的方法从根本上不可靠，可能需要策略内化或外部强制执行机制等替代方案。 该基准测试使用长达 124 页的企业手册放入智能体上下文中，模拟真实企业环境中智能体在完成多步骤任务时必须遵守约束性策略的场景。即使是最前沿的模型也表现出低通过率，表明该问题是结构性而非特定模型的问题，这与文献中记录的

hackernews · spIrr · 7月29日 13:01 · [社区讨论](https://news.ycombinator.com/item?id=49096969)

**背景**: 语言模型智能体越来越多地以

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2607.25398">[2607.25398] HANDBOOK.md: A Benchmark for Long-Context ...</a></li>
<li><a href="https://aigovernance.com/news/handbook-md-benchmark-agentic-policy-compliance-enterprise">Frontier AI Agents Pass Only 36% of Policy-Compliance Tasks ...</a></li>
<li><a href="https://arxiv.org/abs/2510.11588">[2510.11588] Analyzing and Internalizing Complex Policy ... Analyzing and Internalizing Complex Policy Documents for A Unified Evaluation and Governance Framework for Trustworthy ... Agent Governance Toolkit - microsoft.github.io [PDF] Analyzing and Internalizing Complex Policy Documents ...</a></li>

</ul>
</details>

**社区讨论**: 社区讨论（177 条评论）广泛认同该研究发现，多位用户分享了 Claude 在长时间会话后忽略 CLAUDE.md 指令的实际经验。一位评论者将问题归因于长上下文模型的局限性，包括 KV 缓存量化和采样器配置不佳，建议使用本地推理作为解决方案。另一位评论者将其与人类认知局限性进行类比，指出人类同样因工作记忆和推理深度有限而难以遵守长篇策略文档。有评论者质疑论文部分内容明显由 AI 撰写，还有人强调智能体能力是通过后训练强化学习强制注入的合成能力，未经专门训练以遵守手册的模型自然会失败。

**标签**: `#AI agents`, `#LLM context`, `#prompt engineering`, `#AI safety`, `#long context models`

---

<a id="item-5"></a>
## [AI 蠕虫可通过 Copilot for Word 自我传播](https://enklypesalt.com/posts/context-collapse-part3-ai-worming-through-word/) ⭐️ 8.0/10

Håkon Måløy 展示了一个概念验证型 AI 蠕虫，通过在文档中嵌入恶意提示注入指令，使 Copilot for Word 修改并将攻击传播到新文档，实现自我复制。这将针对 Word 的提示注入攻击从孤立事件升级为完整的自我复制蠕虫。 这代表了一类新型的 AI 传播攻击，恶意指令可通过 AI 助手在文档和用户之间自主传播，类似于传统计算机蠕虫，但利用了 LLM 无法区分指令与数据的根本缺陷。随着 AI 代理获得对文件、邮件和系统的更广泛访问权限，这种攻击向量可能实现数据窃取、篡改或进一步利用的快速传播。 截至发布时，尚无针对这一更广泛漏洞类别的稳健缓解措施。攻击者可使用隐藏白色文本或 Unicode 字体欺骗等技术嵌入人类读者不可见但 AI 会处理的恶意指令。该攻击利用了 Copilot 将文档内容视为潜在指令这一事实，模糊了数据与命令之间的界限。

hackernews · Canopy9560 · 7月29日 11:44 · [社区讨论](https://news.ycombinator.com/item?id=49096188)

**背景**: 提示注入是一种网络安全漏洞利用方式，恶意输入被设计来引发大语言模型的意外行为，利用的是模型无法区分开发者定义的提示与用户提供内容这一缺陷。间接提示注入将此扩展为在外部内容（如网页或文档）中嵌入对抗性提示，由 AI 检索并处理。AI 蠕虫是一种利用 AI 能力自我传播和逃避检测的高级恶意软件，类似于传统网络蠕虫，但目标是生成式 AI 系统。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection">Prompt injection</a></li>
<li><a href="https://www.paloaltonetworks.com/cyberpedia/ai-worm">What Is an AI Worm? - Palo Alto Networks</a></li>
<li><a href="https://www.ibm.com/think/insights/malicious-ai-worm-targeting-generative-ai">Researchers develop malicious AI ‘worm’ targeting generative AI systems | IBM</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认为该漏洞源于 AI 系统中指令与数据混合这一根本问题，rwmj 指出在解决这一架构问题之前无法修复。boothby 警告随着用户赋予代理过多权限，问题将更加严重，设想恶意 GitHub 评论可通过账户传播的场景。多名用户（包括 averagjoe）报告已卸载 Copilot 并完全禁用本地 AI，而 piker 指出白色隐藏文本和 Unicode 操纵等技术仍是有效的攻击向量。

**标签**: `#ai-security`, `#prompt-injection`, `#copilot`, `#malware`, `#ai-agents`

---

<a id="item-6"></a>
## [俄罗斯联邦安全局对 Telegram 创始人杜罗夫提起刑事指控并发出国际通缉](https://www.interfax.ru/russia/1106228) ⭐️ 8.0/10

7 月 29 日，俄罗斯联邦安全局（FSB）宣布依《刑法》第 205.1 条第 1.1 款（协助恐怖活动）对 Telegram 创始人帕维尔·杜罗夫提起刑事指控，并将其列入国际通缉名单。FSB 称 Telegram 管理层拒不删除被乌克兰情报机构及恐怖、极端主义组织用于在俄境内策划破坏活动、恐怖袭击、大规模杀戮及网络诈骗的频道、群组和机器人。 这是俄罗斯政府与全球最广泛使用的通讯平台之一 Telegram 之间长期冲突的重大升级，引发了关于平台治理、隐私与国家权力交叉领域的严重关切。因内容审核决策而对一位科技创始人发出国际通缉令，可能为科技行业和全球言论自由开创令人担忧的先例。 指控特别指出 Telegram 拒绝删除用于协调袭击的频道，造成包括妇女儿童在内的多人伤亡及数十亿卢布损失。FSB 将平台的消极不作为定性为俄罗斯法律下的直接恐怖主义共犯，而非仅仅是疏忽。

telegram · zaihuapd · 7月29日 05:56

**背景**: 帕维尔·杜罗夫于 2013 年创立 Telegram，此前因旗下社交网络 VKontakte 受到俄罗斯政府压力而离开俄罗斯。Telegram 长期以来是俄罗斯政府与科技平台之间的冲突焦点，俄罗斯电信监管机构 Roskomnadzor 曾于 2018 年因加密相关争议试图封锁该应用，但禁令于 2020 年解除。在持续的俄乌冲突中，Telegram 被亲政府和反对派团体以及乌克兰和俄罗斯军方及情报机构广泛使用。

**标签**: `#telegram`, `#pavel-durov`, `#russia`, `#fsb`, `#legal`

---
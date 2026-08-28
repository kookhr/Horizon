---
layout: default
title: "Horizon Summary: 2026-08-28 (ZH)"
date: 2026-08-28
lang: zh
---

> 从 30 条内容中筛选出 6 条重要资讯。

---

1. [通过 Zip 压缩包提示注入攻击绕过 Claude Code Opus 5 自动模式](#item-1) ⭐️ 9.0/10
2. [英伟达季度营收 962 亿美元，首次提前一年给出 70%增长指引](#item-2) ⭐️ 9.0/10
3. [Anthropic 开放模型硬件标准预览，AI 操控物理设备集成缩至分钟级](#item-3) ⭐️ 9.0/10
4. [Cloudflare 通过优化 1.1.1.1 DNS 缓存节省 100TB 内存](#item-4) ⭐️ 8.0/10
5. [OpenAI 开发常驻 Codex 代理，持续工作直至休眠](#item-5) ⭐️ 8.0/10
6. [🤖 美国法官叫停五角大楼拉黑 Anthropic](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [通过 Zip 压缩包提示注入攻击绕过 Claude Code Opus 5 自动模式](https://simonwillison.net/2026/Aug/27/breaking-claude-code-opus-5-auto-mode/) ⭐️ 9.0/10

安全研究员 Johann Rehberger 展示了一种提示注入攻击，以 80%的成功率绕过了 Claude Code Opus 5 自动模式的安全功能。该攻击诱骗代理下载并解压一个包含恶意本地 struct.py 文件的 zip 压缩包，当代理导入标准 base64 模块时，该恶意文件就会被执行。 该漏洞揭示了 Anthropic 自动模式中的一个关键盲区，该模式最近已成为 Claude Code 的默认设置，并被宣传具有强大的安全效果。这一发现表明，基于分类器的安全机制可以通过微妙的 Python 导入路径操纵被可靠地绕过，更糟糕的是，它甚至可能在检测到入侵后阻止清理操作。 该漏洞利用了 Python 的本地导入优先机制：当脚本导入 base64 时，Python 会首先检查当前目录并找到从 zip 压缩包中解压出的恶意 struct.py 文件，从而执行它而非标准库版本。在某些测试中，自动模式的分类器允许恶意软件进程启动，但随后却阻止了 Claude 自身的清理命令，使安全机制本身成为了故障的一部分。

rss · Simon Willison · 8月27日 22:50

**背景**: Claude Code 的自动模式通过分类器路由工具调用，该分类器旨在阻止任何不可逆、破坏性或针对用户环境之外的操作，允许代理在无需常规权限提示的情况下自主运行。Anthropic 最近将自动模式设为 Pro、Max 和 Team 计划的默认选项，对该机制作为抵御提示注入攻击的主要防线寄予了极大信任。提示注入是一类漏洞，攻击者通过对抗性输入操纵 LLM 代理的工具选择或参数，利用代理自身的工具调用能力滥用其权限。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://code.claude.com/docs/en/auto-mode-config">Configure auto mode - Claude Code Docs</a></li>
<li><a href="https://claude.com/blog/auto-mode-default-in-claude-code">Auto mode is now the default in Claude Code for Pro, Max, and Team plans | Claude by Anthropic</a></li>
<li><a href="https://www.mdpi.com/2078-2489/17/1/54">Prompt Injection Attacks in Large Language Models and AI Agent Systems: A Comprehensive Review of Vulnerabilities, Attack Vectors, and Defense Mechanisms</a></li>

</ul>
</details>

**标签**: `#prompt-injection`, `#ai-security`, `#claude-code`, `#llm-agents`, `#vulnerability`

---

<a id="item-2"></a>
## [英伟达季度营收 962 亿美元，首次提前一年给出 70%增长指引](https://mp.weixin.qq.com/s/JTZ_ZJ_pn5vgrI_1QUyWNw) ⭐️ 9.0/10

英伟达发布 2027 财年第二季度财报，营收达 962.21 亿美元，同比增长 106%，其中数据中心收入为 890 亿美元。CFO 科莱特·克雷斯首次提前一年给出 2028 财年营收指引，预计同比增长约 70%，并强调这一数字受限于供给而非需求。 这一前所未有的前瞻性指引标志着 AI 产业的重大转折点，表明对 AI 算力的爆发式需求毫无放缓迹象。受供给限制的增长前景以及下一代 Vera Rubin 平台的推出，将对整个半导体供应链和 AI 生态系统产生深远影响。 下一代 Vera Rubin 平台已于本月量产出货，预计本季度将贡献约 20%的数据中心收入。Vera Rubin 平台是一个多机架 pod 级系统，专为处理 agentic AI 而构建，在六款新芯片间实现了极致的协同设计，包括 Vera CPU、Rubin GPU、NVLink 6 Switch 和 BlueField-4 DPU。

telegram · zaihuapd · 8月27日 08:51

**背景**: 英伟达的财年命名与日历年不同，FY2027 对应的是大语言模型广泛采用后 AI 驱动爆发式增长的时期。前瞻性指引是企业向投资者提供未来财务表现预期的做法，而在半导体行业中提前一年给出预测是极为罕见的。Vera Rubin 平台是英伟达继 Blackwell 之后的下一代架构，旨在应对 agentic AI 和大规模推理工作负载日益增长的计算需求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nvidia.com/en-us/data-center/technologies/rubin/">Infrastructure for Scalable AI Reasoning | NVIDIA Vera Rubin Platform</a></li>
<li><a href="https://www.linkedin.com/posts/utsav-pandya-23770471_ai-technews-nvidia-activity-7416495154779348992--8Lc">NVIDIA Unveils Vera Rubin Platform for AI Supercomputing | LinkedIn</a></li>

</ul>
</details>

**标签**: `#Nvidia`, `#AI`, `#Data Center`, `#Earnings`, `#Semiconductors`

---

<a id="item-3"></a>
## [Anthropic 开放模型硬件标准预览，AI 操控物理设备集成缩至分钟级](https://www.anthropic.com/news/model-hardware-standard-research-preview) ⭐️ 9.0/10

Anthropic 发布了模型硬件标准（MHS）的研究预览版，这是一项共享规范，使 AI 智能体能够安全操控显微镜、液体处理器和机械臂等物理实验室及制造设备。该标准将设备集成时间从数周或数月大幅缩短至几小时甚至几分钟，首批合作方包括基因泰克、卡内基梅隆大学和 QuEra，已在生物技术、机器人和量子计算领域成功部署。 这一公告标志着主要 AI 实验室从数字界面迈向物理世界的重要一步，通过让自主 AI 智能体直接控制硬件，有望变革实验室自动化、先进制造和科学研究领域。通过标准化 AI 模型与物理设备之间的通信协议，MHS 有望消除历史上阻碍 AI 驱动自动化在科学和工业领域应用的高昂定制集成瓶颈。 QuEra 基于 MHS 构建的 AI 控制器在 99.3% 的情况下无需人工干预即可恢复量子计算机的激光锁定，将此前需要专家现场处理的任务转变为数秒内完成的自动化流程。Anthropic 计划在完成安全评估后开源该标准，目前的研究预览仅面向首批科学研究实验室和先进制造商开放。

telegram · zaihuapd · 8月28日 01:38

**背景**: 模型硬件标准（MHS）解决的是实验室和工业自动化中的一个根本挑战：传统上，将 AI 系统与一台物理设备集成需要定制软件开发，每台设备可能耗时数周至数月。MHS 提供了一套共享规范——即通用接口协议——任何 AI 智能体都可以用它与任何兼容 MHS 的设备通信，类似于 USB 标准统一了外设连接方式。早期合作方之一 QuEra Computing 基于哈佛大学和 MIT 的研究，使用中性原子构建量子计算机，其中维持激光锁定一直是一个需要专家干预的持续性运维难题。此次研究预览涵盖了生物技术（基因泰克）、学术机器人（卡内基梅隆大学）和量子计算（QuEra）领域的合作方，展示了该标准的跨领域适用性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/news/model-hardware-standard-research-preview">Previewing the Model Hardware Standard \ Anthropic</a></li>
<li><a href="https://www.cnbc.com/2026/08/27/anthropic-pushes-into-physical-world-with-new-standard-to-help-ai-agents-operate-machines.html">Anthropic pushes into physical world with new standard to help AI agents operate machines</a></li>
<li><a href="https://quantumzeitgeist.com/anthropic-ai-tunes-quantum-lasers-queras/">QuEra ’s AI Now Tunes Quantum Lasers In Seconds, Not Minutes</a></li>

</ul>
</details>

**标签**: `#Anthropic`, `#AI Hardware Integration`, `#Laboratory Automation`, `#Robotics`, `#Model Hardware Standard`

---

<a id="item-4"></a>
## [Cloudflare 通过优化 1.1.1.1 DNS 缓存节省 100TB 内存](https://blog.cloudflare.com/dns-cache-memory-optimization-1111/) ⭐️ 8.0/10

Cloudflare 工程师对其内部代号为 Big Pineapple 的 DNS 解析器进行了五项 Rust 级别的内存优化，将每条缓存记录的内存占用减少了 56%，在整个全球服务器集群中释放了约 100TB 的内存。这些优化主要针对内部数据结构和内存分配模式，而非算法层面的改动。 在 Cloudflare 如此庞大的规模下，即使每条记录微小的内存节省也会累积成巨大的基础设施成本降低，直接提升了这一全球最快公共 DNS 解析器之一的效率。这证明了底层系统编程和内存布局优化仍然是大规模互联网基础设施的关键竞争优势。 这五项优化使用 Rust 实现，主要针对 Big Pineapple DNS 解析器的缓存条目布局和分配策略。社区成员指出可能还存在进一步优化的空间，例如将记录数据直接放在 CacheEntry 成员之后以避免单独分配内存，但在 Rust 的所有权模型下实现这一优化可能更具挑战性。

hackernews · TangerineDream · 8月27日 17:17 · [社区讨论](https://news.ycombinator.com/item?id=49468083)

**背景**: Cloudflare 的 1.1.1.1 是一个免费、隐私优先的公共 DNS 解析器，在全球数百个城市运行，被测量为最快的 DNS 解析器之一。DNS 解析器通过缓存域名记录来加速后续查询，在每天处理数十亿次查询的规模下，每条缓存记录的内存占用就成为了一个重要的运营问题。此次优化应用于 Big Pineapple，这是 Cloudflare 用 Rust 编写的、支撑 1.1.1.1 服务的 DNS 解析器。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.cloudflare.com/dns-cache-memory-optimization-1111/">How we saved 100 terabytes of memory by optimizing 1.1.1.1’s DNS ...</a></li>
<li><a href="https://developers.cloudflare.com/1.1.1.1/">1 . 1 . 1 . 1 ( DNS Resolver ) · Cloudflare 1 . 1 . 1 . 1 docs</a></li>
<li><a href="https://news.ycombinator.com/item?id=49468083">Saving 100 terabytes of memory by optimizing 1.1.1.1's DNS cache</a></li>

</ul>
</details>

**社区讨论**: 讨论展现了对系统编程的强烈认可，评论者指出这类内存优化技术——如结构体对齐、自定义分配器、以及用单次大 malloc() 代替逐条分配——都是广为人知但非常有效的手段。多位评论者指出了 Cloudflare 还可以追求的进一步优化，例如将记录数据与 CacheEntry 结构体放在一起，同时有评论者观察到将多个独立列表合并为单一分配可能会削弱 Rust 的安全保证。整体观点认为，虽然这些优化在专家看来属于标准技术，但在 Cloudflare 的规模下产生了巨大的实际影响。

**标签**: `#systems-programming`, `#optimization`, `#dns`, `#memory`, `#cloudflare`

---

<a id="item-5"></a>
## [OpenAI 开发常驻 Codex 代理，持续工作直至休眠](https://www.wired.com/story/openai-is-developing-a-persistent-ai-agent/) ⭐️ 8.0/10

OpenAI 正在为命令行版 Codex 开发「常驻模式」，使代理能够持续工作、跨会话自主创建后续任务，并一直运行直到用户明确将其「休眠」。该模式内置主动性，代理可根据对用户的了解自行决定工作内容，但对用户系统之外的改动仍需事先批准。 这标志着 AI 编程助手从完成单个提示后即停止的被动模式，向能够长期自主执行任务的常驻代理的重大转变。它可能通过让 AI 主动管理和跨会话执行多步骤项目，从根本上改变软件开发工作流。 常驻模式出现在 Codex 的「推理努力」菜单中，用户可在此选择分配给模型的计算能力、token 数量和思考时间。OpenAI 已确认正在测试该功能，但表示暂无近期上线计划。

telegram · zaihuapd · 8月28日 02:47

**背景**: OpenAI 于 2025 年 4 月 16 日发布了 Codex CLI，这是一个在终端本地运行的开源编程代理，将语言模型与本地代码和命令行任务相连接。它可以编写和编辑代码、执行命令，并通过轻量级界面与文件交互。当前 AI 代理通常以请求-响应模式运行，在几分钟或几小时内完成任务后即停止，而持久记忆和状态架构则允许代理在独立会话之间保留事实、用户偏好和领域知识。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.wired.com/story/openai-is-developing-a-persistent-ai-agent/">OpenAI Is Developing a ‘Persistent’ AI Agent | WIRED</a></li>
<li><a href="https://en.wikipedia.org/wiki/OpenAI_Codex_(AI_agent)">OpenAI Codex (AI agent) - Wikipedia</a></li>
<li><a href="https://github.com/openai/codex">GitHub - openai/codex: Lightweight coding agent that runs in your terminal · GitHub</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#Codex`, `#AI Agents`, `#Autonomous Systems`, `#Software Engineering`

---

<a id="item-6"></a>
## [🤖 美国法官叫停五角大楼拉黑 Anthropic](https://www.bloomberg.com/news/articles/2026-08-28/anthropic-wins-court-challenge-to-us-supply-chain-risk-label?srnd=phx-technology) ⭐️ 8.0/10

美国一名联邦法官叫停了五角大楼对 Anthropic 的禁令，裁定将该公司列为供应链风险缺乏充分依据，且带有报复性质。

telegram · zaihuapd · 8月28日 03:15

**标签**: `#Anthropic`, `#AI Policy`, `#Legal`, `#Government`, `#Defense`

---
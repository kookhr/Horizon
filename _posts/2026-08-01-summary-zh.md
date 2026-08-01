---
layout: default
title: "Horizon Summary: 2026-08-01 (ZH)"
date: 2026-08-01
lang: zh
---

> 从 41 条内容中筛选出 5 条重要资讯。

---

1. [OpenAI Astra 在十项长期数学难题上取得突破](#item-1) ⭐️ 10.0/10
2. [EA 550 亿美元卖身沙特财团，下周正式完成](#item-2) ⭐️ 9.0/10
3. [DeepSeek 发布 V4-Flash-0731：性价比最高的开源大语言模型](#item-3) ⭐️ 8.0/10
4. [MCP 2.0 转向无状态模式，重新激发生态兴趣](#item-4) ⭐️ 8.0/10
5. [微软确认今年推出 Copilot「超级应用」](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI Astra 在十项长期数学难题上取得突破](https://openai.com/index/ten-advances-in-mathematics/) ⭐️ 10.0/10

OpenAI 宣布其下一代模型 Astra 的内部版本在十个长期未解决的数学与理论计算机科学问题上取得新成果，涵盖 Connes 刚性猜想、非索菲克群存在性、多色 Ramsey 数及算术电路下界等。所有证明均在 Lean 4 中形式化验证，每个问题的 token 成本约为 2000 美元（按 GPT-5.6 Sol 定价）。 这标志着 AI 从工具向纯数学研究协作者的角色转变，而纯数学一直被认为是最难自动化的领域。这些问题至少十年未见主要进展，且证明经过形式化验证，表明 AI 有望在人类知识最抽象的领域加速发现。 OpenAI 发布了 GitHub 仓库（openai/ten-proofs）包含 Lean 4 形式化证明、描述解决方案的论文，以及一份由 LLM 生成的推理过程重建 PDF。公司坦承数学论证由 AI 生成，人类负责整理与形式化，并公开邀请数学界深入审视这些成果。

telegram · zaihuapd · 8月1日 07:59

**背景**: Lean 是一种基于归纳构造演算的证明助手和函数式编程语言，自 2013 年起开发，现由非营利组织 Lean FRO 维护。它允许数学家编写经机械验证的证明，消除复杂论证中的人为错误风险。此次涉及的问题——如 Connes 刚性猜想（关于高秩格的 von Neumann 代数）和非索菲克群存在性（无法被有限对称群逼近的群）——都是纯数学和理论计算机科学中的深层问题，数十年来一直难以用传统方法突破。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Lean_(proof_assistant)">Lean (proof assistant)</a></li>
<li><a href="https://en.wikipedia.org/wiki/Sofic_group">Sofic group - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: Simon Willison 赞赏了发布形式化证明和推理轨迹的透明度，但表示仍希望看到实际使用的提示词。他还指出缺少信息说明有多少问题在花费 token 后未能解决。许多数学家在网上表示正经历集体的'深蓝时刻'，讨论中还引用了陶哲轩关于'大数学'的愿景——即人类与 AI 的大规模协作，人类负责创造性决策，AI 承担技术性工作。

**标签**: `#AI-mathematics`, `#OpenAI`, `#formal-verification`, `#Lean`, `#research-breakthrough`

---

<a id="item-2"></a>
## [EA 550 亿美元卖身沙特财团，下周正式完成](https://www.gamersky.com/news/202607/2180618.shtml) ⭐️ 9.0/10

由沙特主导的财团（PIF、Silver Lake、Affinity Partners）以 550 亿美元收购 EA 的交易已获得所有监管批准，预计将于 2026 年 8 月 4 日完成。这将是游戏史上第二大收购案，届时 EA 将成为一家私人公司。

telegram · zaihuapd · 8月1日 09:10

**标签**: `#gaming-industry`, `#mergers-and-acquisitions`, `#saudi-pif`, `#electronic-arts`, `#industry-consolidation`

---

<a id="item-3"></a>
## [DeepSeek 发布 V4-Flash-0731：性价比最高的开源大语言模型](https://simonwillison.net/2026/Jul/31/deepseek-v4-flash-0731/#atom-everything) ⭐️ 8.0/10

DeepSeek 发布了 DeepSeek-V4-Flash-0731，这是一个拥有 3040 亿参数的开源权重模型，具备显著增强的 agentic 能力，在 Hugging Face 上的大小为 167GB。Artificial Analysis 将其智能水平排在 MiniMax M3（428B 模型）之上，而定价仅为每百万输入 token $0.14、每百万输出 token $0.27，使其成为目前性价比最高的模型。 此次发布加剧了开源大语言模型领域的性价比竞争，表明 DeepSeek 能够以仅约竞争对手十分之一的成本提供接近前沿水平的智能。它在智能指数与成本对比图上将帕累托前沿大幅推向 DeepSeek 的方向，对开源和闭源模型提供商都构成了巨大压力。 该模型的输出质量对推理强度设置非常敏感——Simon Willison 发现默认推理级别生成的骑自行车的鹈鹕画得很差，而通过 OpenRouter 将 reasoning_effort 设为 high 后效果显著提升。可通过命令 `llm -m openrouter/deepseek/deepseek-v4-flash-0731 -o reasoning_effort high` 来访问该模型。

rss · Simon Willison · 7月31日 23:59

**背景**: DeepSeek 是一家中国 AI 实验室，以极具竞争力的价格发布高性能开源权重大语言模型而闻名，持续挑战西方前沿模型。Artificial Analysis 智能指数将多个基准测试信号——包括 GPQA Diamond、Humanity's Last Exam 和 Terminal-Bench——聚合为单一的模型级智能评分，从而实现跨模型的每单位智能成本直接比较。"Agentic 能力"指的是模型自主追求目标、规划多步骤任务以及使用网页浏览和命令行等工具解决实际问题的能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://artificialanalysis.ai/">AI Model & API Providers Analysis | Artificial Analysis</a></li>
<li><a href="https://artificialanalysis.ai/models/capabilities/agentic">Best AI for Agentic Tasks: LLM Leaderboard | Artificial Analysis</a></li>
<li><a href="https://www.emergentmind.com/topics/agentic-capabilities">Agentic Capabilities in Adaptive AI</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#LLM`, `#AI Models`, `#Open Source`, `#Machine Learning`

---

<a id="item-4"></a>
## [MCP 2.0 转向无状态模式，重新激发生态兴趣](https://simonwillison.net/2026/Jul/31/stateless-mcp/#atom-everything) ⭐️ 8.0/10

Model Context Protocol 规范更新至 2026-07-28 版本（MCP 2.0），引入了无状态传输模型，用单个 HTTP 请求取代了此前需要两步完成的会话初始化流程。Simon Willison 同时发布了两个新工具——mcp-explorer 和 datasette-mcp——帮助开发者在新规范下探索和测试 MCP 服务器。 这是 MCP 规范自发布以来最重大的变更，大幅降低了客户端和服务端的实现复杂度，同时使协议更适合可扩展的企业级 Web 应用。社区重新关注 MCP 也反映出人们对赋予 Agent shell 访问权限的安全风险日益担忧，MCP 被定位为一种更易审计和可控的替代方案。 在旧版 MCP 中，客户端必须先发送 initialize 请求获取 Mcp-Session-Id，再携带该 ID 发送第二个请求才能调用工具；新的无状态方式将其合并为单个 POST 请求，通过 MCP-Protocol-Version 和 Mcp-Method 等请求头传递元数据。服务端不再需要维护会话状态，消除了一个主要的 bug 来源，也简化了后端实例间的负载均衡。

rss · Simon Willison · 7月31日 23:13

**背景**: Model Context Protocol（MCP）是 Anthropic 于 2024 年 11 月推出的开放标准，旨在标准化 AI 系统（如大语言模型）与外部工具、数据源和系统的集成方式。2025 年经历了一波热潮后，MCP 部分被 Anthropic 的 Skills 功能所掩盖，因为拥有终端和 curl 访问权限的 Agent 可以更灵活地实现类似功能。无状态协议是指服务器不在请求之间保留会话状态的协议，能提升可扩展性和可靠性，但可能增加重复数据传输。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arstechnica.com/ai/2026/07/with-a-stateless-makeover-new-mcp-spec-targets-enterprise-scale/">With a stateless makeover, new MCP spec targets enterprise scale - Ars Technica</a></li>
<li><a href="https://news.ycombinator.com/item?id=49088058">MCP 2026-07-28 Specification: transport going stateless | Hacker News</a></li>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol</a></li>

</ul>
</details>

**社区讨论**: 在 Hacker News 上，运营 MCP 服务器网关和注册中心的开发者反映，他们的 bug 和运维问题中有很大一部分源于需要持久化服务端会话状态，这验证了向无状态模型转变的必要性。整体情绪积极，社区认为这一变更对于实现企业级规模采用是必要的一步。

**标签**: `#MCP`, `#Model Context Protocol`, `#LLM agents`, `#AI tools`, `#specification`

---

<a id="item-5"></a>
## [微软确认今年推出 Copilot「超级应用」](https://www.theverge.com/tech/972927/microsoft-copilot-super-app-confirmed) ⭐️ 8.0/10

微软 CEO 纳德拉在财报电话会议上确认，公司将于今年推出一款 Copilot「超级应用」，将聊天、编程和智能体能力整合到一个统一应用中。该应用将合并 Copilot 聊天机器人、GitHub Copilot、Copilot Cowork 和 Autopilot 系统，同时覆盖消费者和商用场景。 这一整合代表了 AI 助手领域的重大战略转变，使微软能够直接与 OpenAI 近期推出的整合了 ChatGPT 和 Codex 的 ChatGPT Work 应用竞争。它反映了将分散的 AI 工具统一到单一平台的更广泛行业趋势，可能重塑消费者和企业日常使用 AI 的方式。 纳德拉将 Copilot 的演进描述为从聊天工具到 Cowork 再到 Autopilots，合并预计于本季度完成。值得注意的是，据报道 Copilot Cowork 运行在 Anthropic 的 Claude 模型上而非微软自研 AI，且微软上季度营收达 900 亿美元，主要由 AI 和云业务推动。

telegram · zaihuapd · 8月1日 13:18

**背景**: 智能体 AI（Agentic AI）是指能够在人类定义的目标和约束内自主追求目标、使用工具并采取行动的 AI 系统。Copilot Cowork 是内置于 Microsoft 365 的 AI 自动化层，可在 Outlook 和 Teams 等应用中委派、规划和执行多步骤任务。Copilot Autopilot 代表更高层次的 AI 自主性，从建议模式升级到完全有界的自主行动模式，是微软在 Build 大会上引入的新 AI 类别。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Agentic_AI">Agentic AI</a></li>
<li><a href="https://www.linkedin.com/pulse/microsoft-launches-copilot-cowork-built-anthropic-cross-m365-bora-g2xzc">Microsoft launches Copilot Cowork , built with Anthropic...</a></li>
<li><a href="https://www.linkedin.com/pulse/from-copilot-autopilot-microsoft-just-changed-game-frederick-jc0rf">From Copilot to Autopilot — Microsoft Just Changed the Game</a></li>

</ul>
</details>

**标签**: `#Microsoft`, `#Copilot`, `#AI Super App`, `#Agentic AI`, `#Product Strategy`

---
---
layout: default
title: "Horizon Summary: 2026-09-30 (ZH)"
date: 2026-09-30
lang: zh
---

> 从 40 条内容中筛选出 8 条重要资讯。

---

1. [GPT 6.1 Sol：以五分之一的价格提供接近 Astra 的智能](#item-1) ⭐️ 9.0/10
2. [AMD 将以 82 亿美元收购李飞飞创办的 World Labs](#item-2) ⭐️ 9.0/10
3. [OpenAI DevDay 2026 发布 Dots 智能体等 20 余项重大更新](#item-3) ⭐️ 9.0/10
4. [研究论文分析对话式 AI 代理的隐私漏洞](#item-4) ⭐️ 8.0/10
5. [Anthropic 红队：AI 模型在二进制利用能力上突破重要阈值](#item-5) ⭐️ 8.0/10
6. [OpenAI DevDay 2026 实时博客](#item-6) ⭐️ 8.0/10
7. [免费开源书籍：从芯片到智能体的机器学习性能工程](#item-7) ⭐️ 8.0/10
8. [Anthropic 评估 GLM-5.3 网络攻击能力](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [GPT 6.1 Sol：以五分之一的价格提供接近 Astra 的智能](https://simonwillison.net/2026/Sep/29/hn-49898129/) ⭐️ 9.0/10

OpenAI 在 2026 年 DevDay 上发布了 GPT 6.1 Sol，以五分之一的价格提供接近 Astra 的智能，Simon Willison 提供了可视化分析，将其与 GPT-6 系列进行对比。

rss · Simon Willison · 9月29日 18:27

**标签**: `#openai`, `#gpt-6.1`, `#llm`, `#ai-models`, `#devday`

---

<a id="item-2"></a>
## [AMD 将以 82 亿美元收购李飞飞创办的 World Labs](https://ir.amd.com/news-events/press-releases/detail/1299/amd-to-acquire-world-labs-to-advance-the-future-of-ai-compute) ⭐️ 9.0/10

AMD 宣布以 82 亿美元收购由李飞飞创办的世界模型 AI 公司 World Labs，李飞飞将加入 AMD 担任执行副总裁兼首席科学家，负责将世界模型能力与 AMD 的计算平台相整合。

telegram · zaihuapd · 9月29日 03:59

**标签**: `#AMD`, `#World Labs`, `#Fei-Fei Li`, `#AI Acquisition`, `#World Models`

---

<a id="item-3"></a>
## [OpenAI DevDay 2026 发布 Dots 智能体等 20 余项重大更新](https://openai.com/zh-Hant/index/devday-2026-recap/) ⭐️ 9.0/10

在 DevDay 2026 上，OpenAI 宣布了 20 余项重大更新，包括可全天候自主运转的常驻智能体 Dots、专精编程且价格仅为 Astra 五分之一的 GPT-6.1 Sol、速度最高提升 8 倍的 Astra Ultrafast、全新 Agents API 与 Decisions API、支持语音操控的云端 Codex、可将订阅额度划拨至第三方的

telegram · zaihuapd · 9月29日 17:52

**标签**: `#OpenAI`, `#AI Agents`, `#GPT-6.1`, `#Developer API`, `#DevDay 2026`

---

<a id="item-4"></a>
## [研究论文分析对话式 AI 代理的隐私漏洞](https://jorgegarciaherrero.com/wp-content/interactivos/20260916-Prompt-like-a-butterfly-sting-like-a-tracker-(clean).pdf) ⭐️ 8.0/10

一篇研究论文发表，对网页端和移动端对话式 AI 代理进行了系统性隐私分析，研究了用户数据如何被追踪及潜在暴露的问题。该论文调查了主流 AI 聊天服务的数据收集实践、广告追踪器集成以及对话暴露漏洞。 随着对话式 AI 代理深度融入日常工作流程，用户经常与这些平台分享敏感的个人和职业信息，却往往不了解其中的隐私风险。这项研究揭示了可能影响数百万用户的系统性隐私弱点，并促使 AI 公司采取更强的数据保护措施。 该分析涵盖了多个攻击面，包括未完成提示词实时传输至服务器、通过可预测的基于 UUID 的 URL 暴露对话历史，以及 AI 聊天界面中集成第三方广告追踪器。论文同时审查了网页端和移动端平台，指出移动端代理由于拥有更广泛的系统级权限，可能呈现额外的追踪途径。

hackernews · damaru2 · 9月29日 09:03 · [社区讨论](https://news.ycombinator.com/item?id=49890226)

**背景**: ChatGPT、Perplexity 等对话式 AI 代理实时处理用户输入，通常将数据发送至远程服务器进行推理和缓存。虽然这些平台被广泛用于生产力和信息检索，但其底层数据处理实践——包括提示词传输、对话存储和第三方追踪器集成——对用户而言往往是不透明的。隐私研究者越来越关注这些系统如何处理敏感数据，尤其是 AI 公司在为模型改进而囤积数据与保护用户隐私之间面临相互竞争的压力。

**社区讨论**: 社区讨论中出现了多个具体的隐私观察，包括 ChatGPT 在用户提交前周期性地将未完成的提示词发送至`conversation/prepare`端点，以及 Perplexity 通过可预测的 UUID URL 暴露完整对话。评论者辩论了开放权重模型是否是隐私问题的最终解决方案，有人认为本地执行消除了信任第三方服务器的需要，而另一些人则对 AI 公司集成有利于直接竞争对手的广告追踪器表示惊讶。

**标签**: `#privacy`, `#conversational-ai`, `#security`, `#data-tracking`, `#ai-agents`

---

<a id="item-5"></a>
## [Anthropic 红队：AI 模型在二进制利用能力上突破重要阈值](https://simonwillison.net/2026/Sep/29/anthropic-frontier-red-team/) ⭐️ 8.0/10

Anthropic 前沿红队报告称，GLM-5.3 和 Claude Mythos Preview 在内部二进制利用基准测试的控制流劫持任务中分别取得了 4%和 6%的成功率，这是 AI 模型首次在此类任务上取得成功，而此前的模型如 Claude Opus 4.6 和 GLM-5.2 成功率为零。 这标志着前沿 AI 模型在进攻性网络安全能力上跨越了一个重要阈值，表明 AI 开始掌握此前仅限于熟练人类安全研究人员的实际二进制利用技能。此类能力的扩散引发了对 AI 安全、网络安全以及进攻性网络工具被大规模滥用的严重担忧。 评估使用了从 Anthropic 内部二进制利用基准中随机选取的 100 个任务，专门针对完整的控制流劫持。虽然成功率仍然较低（4-6%），但从零到非零成功的转变在质量上具有重要意义，因为这表明这些模型现在能够完成二进制利用所需的完整推理和执行链条。

rss · Simon Willison · 9月29日 22:20

**背景**: 二进制利用是指通过操纵内存或程序逻辑等方式，使编译后的程序执行非预期代码的过程。控制流劫持是一种特定技术，攻击者通过它将程序的执行流程重定向到恶意代码，绕过程序的正常行为。Anthropic 前沿红队是一个专门对 AI 系统进行压力测试的团队，旨在了解 AI 的当前能力并预判未来风险，特别是在网络安全和国家安全领域。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/research/team/frontier-red-team">Frontier Red Team Research \ Anthropic</a></li>
<li><a href="https://trailofbits.github.io/ctf/exploits/binary1.html">Binary Exploits 1 - CTF Field Guide</a></li>
<li><a href="https://www.geeksforgeeks.org/ethical-hacking/control-hijacking/">Control Hijacking - GeeksforGeeks</a></li>

</ul>
</details>

**标签**: `#ai-security`, `#anthropic`, `#binary-exploitation`, `#frontier-models`, `#cyber-capabilities`

---

<a id="item-6"></a>
## [OpenAI DevDay 2026 实时博客](https://simonwillison.net/2026/Sep/29/openai-devday-2026-live-blog/) ⭐️ 8.0/10

Simon Willison 在旧金山实时博客报道 OpenAI DevDay 2026，涵盖这一重要 AI 会议的主题演讲公告和最新发展。

rss · Simon Willison · 9月29日 15:55

**标签**: `#openai`, `#ai`, `#llms`, `#generative-ai`, `#devday`

---

<a id="item-7"></a>
## [免费开源书籍：从芯片到智能体的机器学习性能工程](https://www.reddit.com/r/MachineLearning/comments/1wt6ns4/i_wrote_a_free_opensource_book_on_making_ml/) ⭐️ 8.0/10

一本名为《How to Make Your Model Fast: A Systems View of Efficient Machine Learning, from Silicon to Agents》的免费开源书籍已在 GitHub 上发布，涵盖了从硬件级 roofline 分析到智能体级性能的完整优化技术栈。作者花费数月编写了这份资源，内容涵盖内核、编译器、量化、剪枝、端侧 LLM、机器人、性能分析、推理服务和智能体等主题。 该资源填补了机器学习教育中的一个关键空白，强调仅减少 FLOPs 并不能保证模型更快——必须首先判断系统是受限于算力、带宽、内存还是系统整体。它帮助从业者建立对理论性能上限的直觉，并选择真正有效的优化手段，这在机器学习部署从边缘设备延伸到大规模推理基础设施的当下尤为重要。 本书以 roofline 分析为基础工具，随后沿技术栈逐步向上，涵盖内核、编译器、量化、剪枝，以及视觉、端侧 LLM 和机器人等应用领域。书籍托管于 https://github.com/usamahz/make-your-model-fast，作者积极征求来自机器学习系统、推理、编译器、边缘 AI 和性能工程领域从业者的反馈与贡献。

reddit · r/MachineLearning · /u/SoloTiger_ · 9月29日 10:35

**背景**: Roofline 模型是一种性能分析框架，它将峰值可达 FLOPs/s（吞吐量）与算术强度（每字节数据传输所对应的运算次数）绘制在一起，直观地揭示一个应用是受限于算力还是内存带宽。在深度学习中，模型本质上是大量矩阵乘法的集合，而理解这些运算是受限于计算能力还是数据传输，对于有效优化至关重要。Roofline 模型基于机器峰值性能和峰值带宽提供理论上限，使开发者能够追踪向最优解的进展并识别实现中的瓶颈。这种系统级思维——在优化之前先理解什么真正限制了性能——正是本书的核心理念。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Roofline_model">Roofline model - Wikipedia</a></li>
<li><a href="https://jax-ml.github.io/scaling-book/roofline/">All About Rooflines | How To Scale Your Model</a></li>
<li><a href="https://docs.nersc.gov/tools/performance/roofline/">Roofline Performance Model - NERSC Documentation</a></li>

</ul>
</details>

**标签**: `#Machine Learning`, `#Performance Engineering`, `#Systems Design`, `#Open Source`, `#ML Optimization`

---

<a id="item-8"></a>
## [Anthropic 评估 GLM-5.3 网络攻击能力](https://www.anthropic.com/research/glm-5-3-and-the-spread-of-advanced-cyber-capabilities) ⭐️ 8.0/10

Anthropic 的安全评估发现，智谱 AI 的 GLM-5.3 已具备自主构建端到端网络攻击的能力，在 ExploitBench 中 410 次尝试成功 50 次，接近 Claude Mythos Preview 的 56 次。评估还发现 GLM-5.3 的安全防护可被简单方法绕过，模拟测试成功率为 64% 至 100%，且开放权重允许用户进一步削弱模型的拒答机制。 这一发现凸显了先进网络攻击能力通过开放权重模型扩散的日益增长的风险，这些模型任何人都可以免费获取和修改。随着开源模型在网络攻击能力上逐渐接近 Claude Mythos 等严格管控的专有模型，恶意行为者发动复杂网络攻击的门槛被大幅降低。 ExploitBench 使用 16 个测量的漏洞利用能力标志来评估 LLM 智能体在 V8 漏洞合成方面的能力，目标为 Chrome、Edge、Node.js 和 Cloudflare Workers 中的 V8 JavaScript 引擎。GLM-5.3 由智谱 AI 于 2026 年 8 月 14 日发布，支持 100 万 token 上下文窗口，声称编码和 AI 智能体能力接近 Claude Fable 5。

telegram · zaihuapd · 9月29日 23:58

**背景**: ExploitBench 是一个网络安全基准测试，旨在评估 LLM 智能体发现和合成针对 V8 的完全控制漏洞利用的能力，V8 是 Chrome、Edge、Node.js 和 Cloudflare Workers 中使用的 JavaScript 和 WebAssembly 引擎。Claude Mythos Preview 是 Anthropic 的内部模型，在计算机安全任务中展现出卓越能力；由于其强大的能力，Anthropic 仅向少数经过审查的合作伙伴开放访问权限。GLM-5.3 是中国 AI 初创公司智谱 AI（Z.ai）于 2026 年 8 月 14 日发布的最新开放权重模型，支持 100 万 token 上下文窗口，编码能力接近 Claude Fable 5。开放权重模型与闭源模型的区别在于其参数公开可用，允许用户检查、修改和微调模型——包括移除安全防护机制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://exploitbench.ai/">ExploitBench</a></li>
<li><a href="https://www.anthropic.com/research/mythos-preview">Claude Mythos Preview's cybersecurity capabilities \ Anthropic</a></li>
<li><a href="https://emergent.sh/news/glm-53-officially-launched">Zhipu AI Launches GLM-5.3: New LLM Specs & Features</a></li>

</ul>
</details>

**标签**: `#AI Safety`, `#Cybersecurity`, `#LLM Evaluation`, `#Anthropic`, `#Open Weight Models`

---
---
layout: default
title: "Horizon Summary: 2026-10-13 (ZH)"
date: 2026-10-13
lang: zh
---

> 从 38 条内容中筛选出 7 条重要资讯。

---

1. [Python 3.15 发布：引入显式延迟导入与推导式解包](#item-1) ⭐️ 9.0/10
2. [黑客利用 IoT 漏洞激活欧洲超市冰箱除霜周期](#item-2) ⭐️ 8.0/10
3. [Codex CLI 默认安装持久化自更新守护进程，引发社区强烈不满](#item-3) ⭐️ 8.0/10
4. [PS2 游戏被静态重编译为 WebAssembly 以在浏览器中运行](#item-4) ⭐️ 8.0/10
5. [探讨下一 token 预测与强化学习产生 AGI 的机制性论证](#item-5) ⭐️ 8.0/10
6. [循环扩散 Transformer 通过复用共享模块实现高效图像生成](#item-6) ⭐️ 8.0/10
7. [中欧就混动与电动汽车贸易达成共识，确保中方配额非歧视](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Python 3.15 发布：引入显式延迟导入与推导式解包](https://simonwillison.net/2026/Oct/12/python-3-15/) ⭐️ 9.0/10

Python 3.15 已正式发布，引入了备受期待的 PEP 810 显式延迟导入和 PEP 798 推导式解包等新特性。与此同时，Python 3.10 已停止维护，这使得开发者可以放弃对它的支持并开始使用 Python 3.11 的特性。 作为全球最流行的编程语言之一的重大版本更新，Python 3.15 的显式延迟导入直接解决了 CLI 工具和插件中因重型依赖导致的启动性能瓶颈。Python 3.10 的停止维护也标志着生态系统的重要转变，促使库维护者利用后续版本的新特性来实现代码库的现代化。 PEP 810 使用显式、可选的语法（`lazy import`）实现延迟导入，将模块加载推迟到实际使用符号时，这与被撤回的 PEP 690 隐式方法不同。此外，PEP 798 引入了一种更简洁的语法，允许直接在推导式中解包可迭代对象，例如 `[*L for L in lists]`。

rss · Simon Willison · 10月12日 18:15

**背景**: Python 遵循可预测的发布周期，每个主要版本在停止维护（EOL）前会获得数年的支持，这意味着它不再接收安全更新。延迟导入是一种将模块加载推迟到实际访问其内容时的机制，过去通常需要复杂的手动变通方法来避免拖慢应用程序的启动时间。PEP 810 是将此功能引入 CPython 的第二次尝试，取代了之前被撤回的 PEP 690 隐式方法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://peps.python.org/pep-0810/">PEP 810 – Explicit lazy imports | peps. python .org</a></li>
<li><a href="https://blog.jetbrains.com/pycharm/2026/06/explicit-lazy-imports-are-coming-to-python-3-15/">Explicit Lazy Imports Are Coming to Python 3.15 - The JetBrains Blog</a></li>
<li><a href="https://www.pythonmorsels.com/python315/">Python 3.15's best new features - Python Morsels</a></li>

</ul>
</details>

**标签**: `#python`, `#programming-languages`, `#release-notes`, `#lazy-imports`, `#pep-810`

---

<a id="item-2"></a>
## [黑客利用 IoT 漏洞激活欧洲超市冰箱除霜周期](https://www.tomshardware.com/tech-industry/cyber-security/unprecedented-cyberattack-cripples-supermarket-fridges-across-europe-as-hackers-activate-automatic-defrosting-delivery-and-store-prices-also-impacted-by-incident) ⭐️ 8.0/10

黑客对包括 Intermarché在内的欧洲超市连锁店发动了前所未有的网络攻击，通过利用 Danfoss 制冷控制器中的漏洞激活自动除霜周期，导致 150 多家门店的食品大面积变质。攻击还破坏了配送系统和门店定价基础设施，这是首批对零售食品供应产生直接物理后果的大规模 OT 攻击之一。 这一事件展示了脆弱的遗留工业控制系统如何被武器化以造成实际的物理损害——食品变质、供应链中断和经济损失——弥合了数字攻击与现实后果之间的鸿沟。它凸显了随着运营技术为远程诊断和订阅制商业模式而接入互联网，攻击面正在迅速扩大，这一趋势在制造、医疗和零售领域都在加速。 涉嫌存在漏洞的设备是 Danfoss SM800（2021 年停止支持）和 SC355（2016 年停止支持）控制器——这些是已有已知 CVE 的 15-20 年老旧系统，由于零售利润微薄无法更换设备而仍在使用。2026 年 8 月美国军事基地 commissary 冷柜也疑似发生了类似事件，安全公司 Claroty 在此前已发布了关于 Danfoss 控制器漏洞的研究。

hackernews · Zeekaas · 10月12日 12:16 · [社区讨论](https://news.ycombinator.com/item?id=50055304)

**背景**: Danfoss 等厂商生产的制冷控制器管理着商用制冷系统中的除霜周期，定期加热蒸发器盘管以去除会降低制冷效率的冰层积聚。这些控制器越来越多地接入互联网，用于远程诊断、跨门店效率监控和基于订阅的服务模式——从而产生了新的攻击面。运营技术（OT）网络攻击在 2024 年激增了 87%，随着 IT 和 OT 系统在工业 4.0 倡议下融合，攻击者越来越多地针对物理过程而非仅仅是数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://waterfall-security.com/ot-insights-center/ot-cybersecurity-insights-center/ot-cybersecurity-the-top-10-attacks-since-2020/">OT Cyber Security: The TOP 10 ATTACKS Since 2020</a></li>
<li><a href="https://cybermagazine.com/top10/top-10-ot-security-threats">Top 10: OT Security Threats | Cyber Magazine</a></li>
<li><a href="https://frimec.eu/en/defrost-cycle-control-in-industrial-refrigeration/">Defrost Cycle Control in Industrial Refrigeration - frimec.eu</a></li>

</ul>
</details>

**社区讨论**: HN 讨论（678 条评论）展现了极高的技术深度，评论者识别出了具体的 Danfoss 控制器型号，并讨论了为何工业设备在存在安全风险的情况下仍然接入互联网。出现了一种引人深思的阶级分析视角，指出轮班劳动团队缺乏笔记本电脑阶层习以为常的安全审查和设备更换周期等资源。多位评论者指出，现代实验室和工业设备通常需要互联网连接才能进行基于订阅的运营，使网络隔离变得不切实际，凸显了 OT 环境中节约成本的连通性与安全债务之间的紧张关系。

**标签**: `#cybersecurity`, `#IoT`, `#OT-security`, `#industrial-control-systems`, `#vulnerability`

---

<a id="item-3"></a>
## [Codex CLI 默认安装持久化自更新守护进程，引发社区强烈不满](https://github.com/openai/codex/issues/48195) ⭐️ 8.0/10

OpenAI 的 Codex CLI 被发现默认安装一个持久化、自更新的后台守护进程，且没有文档说明的禁用方式。用户报告该守护进程导致磁盘占用过高（旧版本累积达 12GB）、权限损坏、.git 目录被锁定以及整体可靠性问题，严重影响开发工作流。 这一问题凸显了 AI 编程工具静默安装后台进程与开发者对系统透明度和控制权期望之间日益加剧的矛盾。该 GitHub issue 获得了 480 分和 245 条评论，社区强烈反响表明开发者越来越警惕那些过度工程化、损害系统完整性的代理工具，这可能推动用户转向更简洁的替代方案。 可以在 `~/.codex/config.toml` 的 `[features]` 部分设置未公开的特性标志 `daemon_auto_start = false` 来禁用守护进程。该守护进程在启动时会向 `~/.codex` 写入 PID 文件和锁文件，部分用户采用将这些文件符号链接到 `/dev/null` 并用 `chattr +i` 标记为不可写的变通方案。Claude Code 也存在相同的后台守护进程模式，同样会存储多个旧版本并运行后台进程。

hackernews · whimblepop · 10月12日 18:29 · [社区讨论](https://news.ycombinator.com/item?id=50060694)

**背景**: Codex CLI 是 OpenAI 开发的 AI 编程代理，在终端本地运行，用于检查、编辑和运行开发者项目目录中的代码。近期版本引入了一个共享后台服务器（即守护进程，位于 `codex-app-server-daemon` crate 中），能够独立于主 CLI 进程进行自动更新和会话管理。这种架构与 Claude Code 的运行模式类似，后者同样维护后台进程和版本化二进制文件。虽然此类守护进程旨在提升响应速度并保持工具更新，但它们也带来了诸如旧版本累积导致磁盘膨胀以及可能干扰系统权限等副作用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/openai/codex">GitHub - openai/ codex : Lightweight coding agent that runs in your...</a></li>
<li><a href="https://grokipedia.com/page/Codex_CLI">Codex CLI</a></li>
<li><a href="https://openclawlaunch.com/guides/codex-vps-hosting">Codex VPS Hosting — Run OpenAI Codex CLI on... | OpenClaw Launch</a></li>

</ul>
</details>

**社区讨论**: 社区情绪以负面为主，用户对磁盘膨胀、权限损坏和缺乏文档表示强烈不满。多位评论者指出 Claude Code 也有类似的守护进程模式，表明这是行业普遍现象而非个例。部分用户推荐使用极简替代方案如 'hax'，反映出开发者对更简单、更透明的 AI 编程工具的普遍需求，不希望被强加不需要的后台进程。

**标签**: `#openai`, `#codex-cli`, `#security`, `#developer-tools`, `#background-processes`

---

<a id="item-4"></a>
## [PS2 游戏被静态重编译为 WebAssembly 以在浏览器中运行](https://github.com/snuri00/ps2-web-recomp) ⭐️ 8.0/10

一个名为 ps2-web-recomp 的新项目将 PlayStation 2 游戏二进制文件静态重编译为 WebAssembly，使游戏无需传统运行时模拟即可在网页浏览器中原生运行。这将此前已应用于 N64 和 PS1 游戏的静态重编译方法扩展到了 PS2 平台，并实现了基于浏览器的部署。 这在日益增长的静态重编译运动中代表了一个技术上令人印象深刻的里程碑，有可能使传统游戏在任何现代浏览器中以接近原生的性能运行，而无需插件或模拟器开销。它通过消除对专用模拟器软件的需求，可能对游戏保存和可访问性产生重大影响。 静态重编译在编译时而非运行时将机器码从一种指令集架构翻译为另一种，可以消除传统模拟器中使用的动态二进制翻译的性能开销。该项目仍处于早期阶段，PS2 的 Emotion Engine 架构的复杂性使其成为比 N64 或 PS1 等早期主机更具挑战性的目标。

hackernews · deadxwarrior · 10月12日 06:46 · [社区讨论](https://news.ycombinator.com/item?id=50052251)

**背景**: 静态重编译是二进制翻译的一种形式，在编译时将指令序列从源指令集架构翻译为目标指令集，而非在运行时进行的动态二进制翻译。这项技术在游戏保存社区中获得了关注，N64Recomp 等项目将其应用于 Nintendo 64 游戏，类似的工作也针对 PS1 和 Game Boy Advance 平台。WebAssembly（WASM）作为一种可移植的编译目标，能够在网页浏览器中以接近原生的速度运行，使其成为重编译游戏二进制文件的理想目标。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Static_recompilation">Static recompilation</a></li>
<li><a href="https://github.com/N64Recomp/N64Recomp">GitHub - N64Recomp/N64Recomp: Tool to statically recompile ...</a></li>
<li><a href="https://nio03.github.io/unricopie/en/">Recompendium — game recompilation catalog</a></li>

</ul>
</details>

**社区讨论**: 评论者提出了对重编译二进制文件可信度的安全担忧，认为与经过充分审查的模拟器社区相比，存在隐藏恶意软件的风险。一些人强调了 AI 在推动这些重编译项目中的作用，其中一位表示这是在 AI 对其职业影响的担忧中的一线希望。一个名为 vitaslop 的相关项目也被分享，该项目在 WASM 中构建了一个 ARM 到 WASM 的转译器用于 PS Vita 游戏，另有一位评论者建议将重编译器本身编译为 WASM 以实现完全基于浏览器的转换。

**标签**: `#webassembly`, `#reverse-engineering`, `#static-recompilation`, `#ps2`, `#game-preservation`

---

<a id="item-5"></a>
## [探讨下一 token 预测与强化学习产生 AGI 的机制性论证](https://www.reddit.com/r/MachineLearning/comments/1x4awlk/what_is_the_strongest_mechanistic_argument_that/) ⭐️ 8.0/10

一位 Reddit 用户在 r/MachineLearning 发起了讨论，要求提供最有力的机制性、第一性原理论证，证明下一 token 预测结合强化学习能够产生通用人工智能，并明确要求基于计算学习理论、信息理论和因果机制进行论证，而非趋势外推。 这个问题直指 AI 研究中的一个根本性缺口：驱动当今最先进系统的核心机制在理论上是否足以实现通用智能，还是需要全新的范式。这一答案直接影响研究优先级、投资决策以及对 AGI 可行性和时间线的预期。 发帖人明确排除了哲学辩论和趋势外推，将此定位为关于实际运行效能和因果解释的工程问题。讨论还涉及递归自我改进（RSI）和超级人工智能（ASI），关注的是我们对现有系统的理解，而非假设性的未来突破。

reddit · r/MachineLearning · /u/Repulsive_Twist_9221 · 10月12日 19:09

**背景**: 下一 token 预测是自回归语言模型的核心训练目标，模型学习在给定前文的情况下预测序列中的下一个 token，从而将海量世界知识压缩到模型权重中。强化学习，特别是通过 RLHF 等方法，随后被用于使模型行为与人类偏好对齐并提升推理能力。计算学习理论提供了 PAC 学习和 VC 维等形式化框架，用于严格分析哪些内容可以从数据中学习，而递归自我改进是指 AI 系统迭代设计更强大后继者的假设性过程，可能引发智能爆炸。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Recursive_self-improvement">Recursive self-improvement - Wikipedia</a></li>
<li><a href="https://zeromathai.com/en/attention-language-modeling-basics-en/">7.2 Attention and Language Modeling Basics — Next Token ...</a></li>
<li><a href="https://ce.aut.ac.ir/~keyvanrad/download/ML932/ML_11(Computational+Learning+Theory).pptx">Computational Learning Theory Mohammad Ali Keyvanrad Machine ...</a></li>

</ul>
</details>

**标签**: `#Machine Learning`, `#AGI`, `#Learning Theory`, `#Large Language Models`, `#AI Research`

---

<a id="item-6"></a>
## [循环扩散 Transformer 通过复用共享模块实现高效图像生成](https://www.reddit.com/r/MachineLearning/comments/1x49d61/looped_diffusion_transformer_the_same_blocks_run/) ⭐️ 8.0/10

研究人员提出了循环扩散 Transformer（Looped-DiT，arXiv 2609.40305），在每个去噪步骤中多次运行共享的 transformer 模块组，而非增大模型规模。据报道，260M 参数的循环模型在多个基准测试中超越了 6.5 倍大的模型，同时推理计算量减少了 4.9 倍，且循环深度可在采样时调整而无需重新训练。 这种架构方法挑战了传统上简单扩大扩散模型规模的范式，证明了通过循环复用参数可以实现更高的效率。在推理时动态调整循环深度的能力使得每张图像都能灵活权衡计算量与质量，这对于计算预算可变的部署场景尤为重要。 简单的循环本身并不能可靠地提升性能；作者通过在每次循环迭代上使用深度监督结合自调制注意力来稳定训练。在 M5 Pro 上的独立测试（PyTorch MPS，fp32，100 步 Euler 采样，CFG 6.0）证实，大部分质量提升在循环深度 3 之前就已实现，深度 3 和 4 的结果几乎相同，表明超过深度 3 后收益递减。

reddit · r/MachineLearning · /u/Fit-Ant2238 · 10月12日 18:13

**背景**: 扩散 Transformer（DiT）是一类用 transformer 架构替代传统 U-Net 骨干网络的扩散模型，它在潜在图像补丁上操作，并使用自适应层归一化进行条件控制。在标准扩散模型中，图像生成涉及迭代去噪步骤，模型逐步将噪声精炼为连贯的图像。无分类器引导（CFG）是一种通过在条件预测和无条件预测之间插值来增强条件生成质量的技术，无需外部分类器。Looped-DiT 方法在概念上与循环深度语言模型类似，后者通过多次应用相同的计算模块来以额外计算换取更好的输出质量。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2212.09748">[2212.09748] Scalable Diffusion Models with Transformers</a></li>
<li><a href="https://arxiv.org/abs/2207.12598">[2207.12598] Classifier-Free Diffusion Guidance - arXiv.org</a></li>

</ul>
</details>

**标签**: `#diffusion-models`, `#transformers`, `#efficient-inference`, `#text-to-image`, `#model-architecture`

---

<a id="item-7"></a>
## [中欧就混动与电动汽车贸易达成共识，确保中方配额非歧视](https://www.mofcom.gov.cn/xwfb/sjfzrfb/art/2026/art_4d502e1d49fd4480b39a6cfd0d752038.html) ⭐️ 8.0/10

中国商务部宣布，中欧在贸易投资磋商机制下就混动和电动汽车贸易达成多项共识，欧方将中国混动汽车年进口量上限设为 35 万辆，以 2025 年 30.2 万辆的进口量为基础上浮。协议确保中方配额不低于欧方其他任何进口来源地，同时欧方将继续推进电动汽车企业价格承诺及其他复审程序。 这一协议缓解了全球两大汽车市场之间的贸易紧张局势，为中国制造商提供了持续但设上限的欧洲市场准入，直接影响全球电动汽车和混动供应链。该协议也为通过谈判而非升级关税战来解决绿色技术产品的补贴贸易争端树立了先例。 混动汽车配额以 2025 年为基础上浮，年上限设为 35 万辆，双方强调非歧视、尊重事实和合规原则。中方明确保留在世贸组织框架下的争端解决权利，欧方针对电动汽车的现有价格承诺机制——源自 2024 年依据(EU) 2024/2754 法规的反补贴调查——仍在执行并持续进行复审。

telegram · zaihuapd · 10月12日 06:19

**背景**: 欧盟对中国纯电动汽车发起了正式的反补贴调查，并于 2024 年 10 月 29 日通过了第(EU) 2024/2754 号实施条例，对中国电动汽车征收反补贴税。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.reuters.com/world/china/china-holds-intensive-talks-hybrid-ev-trade-with-eu-2026-10-12/">China details outcome of EU trade talks on hybrid, electric ...</a></li>
<li><a href="https://www.theguardian.com/environment/2026/oct/12/eu-deal-china-limit-imports-hybrid-electric-vehicles">EU to limit Chinese hybrid vehicle imports to 350,000 a year</a></li>
<li><a href="https://www.diplomacyandlaw.com/post/eu-china-hybrid-car-deal">EU -China Hybrid Car Deal: Price Undertakings or a Disguised Export...</a></li>

</ul>
</details>

**标签**: `#Trade Policy`, `#Electric Vehicles`, `#China-EU Relations`, `#Automotive Industry`, `#Supply Chain`

---
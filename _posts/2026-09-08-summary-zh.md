---
layout: default
title: "Horizon Summary: 2026-09-08 (ZH)"
date: 2026-09-08
lang: zh
---

> 从 37 条内容中筛选出 5 条重要资讯。

---

1. [数学家指控 OpenAI 使用其 Navier-Stokes 研究成果](#item-1) ⭐️ 9.0/10
2. [OpenAI 声称 AI 解决了 Navier–Stokes 千禧年大奖问题](#item-2) ⭐️ 9.0/10
3. [NeurIPS 以"AI 生成"为由桌面拒绝 178 篇论文。检测器将领域主席自己的论文标记为 24-69% (N)](#item-3) ⭐️ 9.0/10
4. [马来西亚拟用华为 Ascend 910C 建主权 AI 项目，无视美国警告](#item-4) ⭐️ 8.0/10
5. [📱 张一鸣亲自督导字节跳动筹备空间视频模型](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [数学家指控 OpenAI 使用其 Navier-Stokes 研究成果](https://cims.nyu.edu/~tristanb/statement.pdf) ⭐️ 9.0/10

数学家 Tristan Buckmaster 和 Levent Alpöge 宣布在 Navier-Stokes 相关问题上的进展，包括不可压缩多孔介质、Boussinesq 方程和三维不可压缩 Euler 方程的有限时间爆破结果，同时指控 OpenAI 可能从他们使用 OpenAI 产品的数据中获取了研究洞察以产出竞争性成果。OpenAI 表示"无法排除"研究人员的产品使用数据以去标识化形式帮助改进了其模型，随后双方就谁先取得这些数学突破发生了优先权争议。 这一事件揭示了 AI、学术伦理和数据隐私交汇处的关键张力：如果 AI 公司能够从使用其产品的研究人员那里获取研究洞察，学术优先权和独立发现的传统规范将从根本上被削弱。这一事件的走向可能重塑数学家和科学家与 AI 工具互动的方式，迫使研究人员为避免未发表的创意被 AI 公司吸收并抢先发表而远离商业 AI 产品。 Buckmaster 和 Alpöge 并未解决价值一百万美元的 Clay 千禧年大奖问题本身，但声称证明了一个密切相关的非千禧年 Navier-Stokes 问题，这可能为最终解决完整问题铺平道路。据称 OpenAI 提出承认研究人员应获 Clay 奖并称其为"最接近该问题的人类"，但当其中一位研究者拒绝并威胁要公开此事时，OpenAI 代表据报回复道："你为什么要毁掉自己的职业生涯？"

hackernews · procedurecall · 9月8日 05:42 · [社区讨论](https://news.ycombinator.com/item?id=49605915)

**背景**: Navier-Stokes 方程是描述粘性流体运动的偏微分方程，其三维情况下光滑解是否始终存在是 Clay 数学研究所七个千禧年大奖问题之一，奖金为一百万美元。2026 年 9 月 8 日，OpenAI 宣布其内部模型生成了一个证明，表明光滑、有限能量的三维不可压缩流可以在有限时间内产生奇点，对应 Fefferman 官方问题表述中的陈述 C 和 D，但截至 2026 年 9 月该声明尚未经独立验证。该公告伴随着与 Buckmaster 和 Alpöge 的优先权争议，后者此前已推导出证明中使用的 Euler 方程的密切相关结果。Levent Alpöge 在 OpenAI 的竞争对手 Anthropic 工作，这为争议增添了另一层复杂性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Navier-Stokes_equations">Navier-Stokes equations</a></li>

</ul>
</details>

**社区讨论**: 社区情绪对 OpenAI 持强烈批评态度，评论者尤其对该公司承认无法排除使用研究人员产品交互数据来改进模型感到震惊。多位评论者强调了据称威胁——"你为什么要毁掉自己的职业生涯？"——中的权力不对称，将其视为企业对学者的恐吓。部分评论者指出，如果没有使用数据，这类似于传统学术优先权争议被 AI 工具加速，但这种模糊性本身就是核心问题，引发了研究人员能否安全使用商业 AI 产品而不冒未发表成果被挪用风险的紧迫疑问。

**标签**: `#navier-stokes`, `#mathematics`, `#openai`, `#academic-ethics`, `#ai-research`

---

<a id="item-2"></a>
## [OpenAI 声称 AI 解决了 Navier–Stokes 千禧年大奖问题](https://openai.com/index/navier-stokes-solution/) ⭐️ 9.0/10

OpenAI 宣布其内部 AI 系统提出了 Navier–Stokes 存在性与平滑性问题的解决方案，这是七大千禧年大奖问题之一，证明该方程的动力学可以在有限时间内发展出奇点。该结果尚未得到 Clay 数学研究所或独立数学界的验证，OpenAI 表示即使获奖也会拒绝百万美元奖金。 这是 AI 系统首次声称解决千禧年大奖问题，标志着 AI 与纯数学交叉领域的一个潜在历史性里程碑。然而，该公告引发了关于研究伦理、AI 能力加速以及 AI 驱动的激励是否可能破坏开放数学研究协作规范的激烈辩论。 OpenAI 声称该内部模型训练时间不到两周，但在数学能力上是仅一周前公开发布的 Astra 的两倍以上。另外，有指控称该工作可能源自另一位研究者的提示和先前工作，纽约大学数学家 Tristan Buckmaster 的一份公开声明在网上流传。

hackernews · tedsanders · 9月8日 17:13 · [社区讨论](https://news.ycombinator.com/item?id=49613262)

**背景**: Navier–Stokes 方程描述流体运动，是理解湍流这一经典物理学中最后几个重大未解问题之一的基础。Clay 数学研究所于 2000 年设立了七个千禧年大奖问题，每个问题奖金一百万美元，目前仅有 Poincaré 猜想被正式解决——由 Grigori Perelman 于 2010 年完成，他同样拒绝了奖金。Navier–Stokes 存在性与平滑性问题探讨的是这些方程的解是否始终保持平滑，还是可能在有限时间内发展出奇点。

**社区讨论**: Terence Tao 警告说，如今仅凭某人正在研究某个问题的传闻就可能引发大规模 AI 驱动的攻关，在原始研究充分发挥潜力之前将其

**标签**: `#AI`, `#mathematics`, `#Navier-Stokes`, `#OpenAI`, `#research-ethics`

---

<a id="item-3"></a>
## [NeurIPS 以"AI 生成"为由桌面拒绝 178 篇论文。检测器将领域主席自己的论文标记为 24-69% (N)](https://www.reddit.com/r/MachineLearning/comments/1wakf62/neurips_deskrejected_178_papers_for_being/) ⭐️ 9.0/10

NeurIPS 使用 AI 检测器桌面拒绝了 178 篇论文，但该检测器却错误地标记了领域主席自己的论文，暴露了学术同行评审中自动化 AI 检测的不可靠性。

reddit · r/MachineLearning · /u/tughanbulut · 9月8日 10:19

**标签**: `#NeurIPS`, `#AI Detection`, `#Academic Publishing`, `#Machine Learning`, `#Peer Review`

---

<a id="item-4"></a>
## [马来西亚拟用华为 Ascend 910C 建主权 AI 项目，无视美国警告](https://www.businesstimes.com.sg/international/malaysia-eyes-huawei-chips-ai-project-despite-us-warning) ⭐️ 8.0/10

马来西亚正认真评估采用华为 Ascend 910C 芯片作为其 20 亿令吉（约 4.94 亿美元）主权 AI 基础设施项目的核心。若最终落地，马来西亚将成为首个正式选择中国 AI 加速器而非美国产品的外国政府。 此举可能预示着全球 AI 芯片市场的更广泛转变，各国日益寻求美国主导硬件的替代方案以实现战略自主。若马来西亚不顾美国警告推进该项目，可能鼓励其他国家——尤其是东南亚和全球南方国家——考虑采用中国 AI 芯片，从而削弱美国出口管制的有效性。 Ascend 910C 于 2024 年下半年发布，配备 96GB HBM2e 内存、约 1,800 GB/s 带宽，相较上一代 910B 性能提升约 30-35%。特朗普政府此前曾警告使用华为 AI 加速器芯片可能违反美国出口规定，但马来西亚政府认为采购决定纯属商业考量。

telegram · zaihuapd · 9月8日 03:35

**背景**: 主权 AI 指一个国家利用自身基础设施、数据、人才和商业网络来开发、控制和部署人工智能的能力，以减少对外国技术供应商的依赖。华为 Ascend 910C 被定位为 NVIDIA H100 的竞争替代品，算力约为 800 TFLOPS FP16。美国日益利用出口管制限制先进芯片的获取，特别是针对华为的半导体供应链，作为中美技术竞争的一部分。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.huaweicentral.com/huawei-ascend-910c-alleged-specs-suggest-it-a-tough-rival-to-nvidia-h100/">Huawei Ascend 910C alleged specs suggest it a tough rival to ...</a></li>
<li><a href="https://www.drishtiias.com/daily-updates/daily-news-analysis/sovereign-ai">Sovereign AI | Drishti IAS</a></li>
<li><a href="https://awesomeagents.ai/hardware/huawei-ascend-910c/">Huawei Ascend 910C | Awesome Agents</a></li>

</ul>
</details>

**标签**: `#AI chips`, `#Huawei`, `#geopolitics`, `#sovereign AI`, `#US-China tech competition`

---

<a id="item-5"></a>
## [📱 张一鸣亲自督导字节跳动筹备空间视频模型](https://www.bloomberg.com/news/articles/2026-09-07/bytedance-founder-joins-ai-elite-in-race-to-perfect-world-models) ⭐️ 8.0/10

字节跳动创始人张一鸣正亲自督导基于 Seedance 的实时空间视频生成模型开发，该模型面向 Pico VR 头显，采用云端计算实现低延迟交互式虚拟世界，预计于 2026 年 10 月发布。

telegram · zaihuapd · 9月8日 04:05

**标签**: `#AI`, `#world-models`, `#VR`, `#ByteDance`, `#video-generation`

---
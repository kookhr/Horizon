---
layout: default
title: "Horizon Summary: 2026-09-22 (ZH)"
date: 2026-09-22
lang: zh
---

> 从 37 条内容中筛选出 2 条重要资讯。

---

1. [TypeSafe AI 发布 Jev：首个「系统一」决策模型](#item-1) ⭐️ 8.0/10
2. [SemiAnalysis 深度分析：MoE 推理中的计算与数据移动](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [TypeSafe AI 发布 Jev：首个「系统一」决策模型](https://simonwillison.net/2026/Sep/21/jev/) ⭐️ 8.0/10

TypeSafe AI 发布了 Jev，这是全新「系统一模型」类别中的首个模型，它接受非结构化文本输入，但返回的是以浮点数形式表示的类型化概率决策，而非文本输出。Jev 支持三种问题类型——是非题（「Noul」问题，得名于伯努利分布）、选择题（返回所有选项的概率分布）和评分题（沿定义范围的数值评分）——仅按输入 token 收费，价格为每百万 token 0.042 美元，输出完全免费。 Jev 代表了 LLM 领域一次真正新颖的范式转变：它不再生成需要解析和解释的文本，而是直接输出软件可立即使用的结构化概率决策，运行速度比前沿 LLM 快 40 到 200 倍。这可能会从根本上改变 LLM 集成到决策流程中的方式，例如垃圾邮件检测、内容分类、搜索重排序和优先级排序系统，同时其仅按输入收费的定价模式也颠覆了传统 LLM 基于 token 的经济学模型。 Jev 的架构保留了预训练 LLM 的知识，但用直接从内部表示中读取的决策概率替代了生成的置信度声明，这些概率针对实际结果进行了训练。该 API 接受一个「状态」对象（字符串、字符串数组或键值对）加上多个在上下文窗口内并行评估的问题，在 70-500 毫秒内返回结果。一个值得注意的担忧是，Jev 进一步推向了黑盒机器学习系统——它不为其决策提供任何文本解释，使得偏见审计和可解释性比传统 LLM 更加困难。

rss · Simon Willison · 9月21日 23:09

**背景**: 当前的 LLM 被 TypeSafe 称为「系统二模型」——它们逐个 token 生成文本，边想边说，返回的是应用程序必须解析的字符串。「系统一」这一名称引用了丹尼尔·卡尼曼在《思考，快与慢》中的双过程理论，其中系统一代表快速、直觉性的决策，系统二代表缓慢、深思熟虑的推理。从 LLM 获取结构化决策的传统方法是提示其输出 JSON 等格式的文本，然后解析该输出——这一过程容易出错、产生幻觉且延迟较高。Jev 通过直接输出校准概率消除了这一流程，但代价是牺牲了可解释性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.datacamp.com/blog/system-one-models-jev">Jev: TypeSafe 's System One Model Explained | DataCamp</a></li>
<li><a href="https://docs.typesafe.ai/introduction">Introduction - TypeSafe AI</a></li>
<li><a href="https://archerhume.com/posts/jevs-architecture-unmasked/">Jev’s Architecture Unmasked — archerhume</a></li>

</ul>
</details>

**社区讨论**: Maggie Appleton 认为「决策模型」比「系统一模型」更直观，Simon Willison 也表示赞同。在 Hacker News 上，CEO 确认「Noul」是伯努利分布的缩写。讨论中反复出现的担忧是模型的黑盒性质——评论者担心没有解释的浮点数输出可能掩盖偏见，尤其是在排序求职者等敏感应用场景中，缺乏可解释性意味着相比生成文本的 LLM 出现了倒退。

**标签**: `#LLM`, `#decision-models`, `#AI-architecture`, `#TypeSafe-AI`, `#structured-output`

---

<a id="item-2"></a>
## [SemiAnalysis 深度分析：MoE 推理中的计算与数据移动](https://newsletter.semianalysis.com/p/computation-and-data-movement-for) ⭐️ 8.0/10

SemiAnalysis 发布了一篇全面的技术分析文章，深入探讨了在推理硬件上高效服务混合专家模型时所面临的计算与数据移动挑战。文章详细拆解了 MoE 架构的结构、执行流程以及高效服务策略。 随着 MoE 架构成为前沿大语言模型（如 DeepSeek、Mixtral）的主流范式，推理效率的瓶颈正从纯计算转向数据移动——即在内存层级之间搬运专家权重和中间激活值。理解这些权衡对于设计大规模、高性价比的 LLM 服务基础设施的从业者至关重要。 文章聚焦于稀疏专家激活模式与内存带宽约束之间的相互作用，分析了每一层的路由决策如何产生不规则的数据访问模式，从而影响硬件利用效率。内容涵盖 MoE 推理的结构化流程，包括专家选择和 token 路由如何同时影响计算调度和 GPU 内存层级间的数据移动成本。

rss · Semianalysis · 9月21日 18:14

**背景**: 混合专家是一种稀疏激活架构，每个 token 仅激活部分专家子网络，从而在大幅增加总参数量的同时保持较低的逐 token 计算量。这使得更大、更强的模型能够在合理的计算预算内完成训练和服务，相比同等规模的稠密模型具有显著优势。然而，其代价是所有专家权重都必须驻留在内存中，即使未被激活使用，这在推理过程中造成了巨大的内存容量和带宽压力。随着 MoE 模型规模和复杂度的增长，数据移动——即在正确时间加载正确专家权重的成本——日益超过原始浮点计算成为主要瓶颈，成为推理系统设计者的关键优化目标。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained</a></li>
<li><a href="https://www.alphaxiv.org/overview/2510.05497v4">Patterns behind Chaos: Forecasting Data Movement for... | alphaXiv</a></li>
<li><a href="https://arxiv.org/abs/2507.11181">[2507.11181] Mixture of Experts in Large Language Models</a></li>

</ul>
</details>

**标签**: `#MoE`, `#inference`, `#data-movement`, `#LLM-serving`, `#hardware`

---
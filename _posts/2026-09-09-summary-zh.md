---
layout: default
title: "Horizon Summary: 2026-09-09 (ZH)"
date: 2026-09-09
lang: zh
---

> 从 39 条内容中筛选出 8 条重要资讯。

---

1. [OpenAI 声称用 AI 解决 Navier–Stokes 千禧年大奖问题，但陷入优先权争议](#item-1) ⭐️ 10.0/10
2. [苹果发布首款折叠屏手机 iPhone Duo](#item-2) ⭐️ 9.0/10
3. [Shopify 收购 Tailwind CSS，AI 冲击开发者工具行业](#item-3) ⭐️ 9.0/10
4. [🤖 OpenAI 称 GPT-6 Astra 的 CoT 可监测性显著下降](#item-4) ⭐️ 9.0/10
5. [vLLM v0.29.0 将 Model Runner V2 设为默认运行时，新增 770B MoE 模型支持](#item-5) ⭐️ 8.0/10
6. [探讨 GPT-6 Astra、循环 Transformer 与隐藏推理](#item-6) ⭐️ 8.0/10
7. [揭露恶意软件广告如何绕过 Google 自动审核系统](#item-7) ⭐️ 8.0/10
8. [陶哲轩警告：AI 正以不可再生方式开采开放数学问题](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI 声称用 AI 解决 Navier–Stokes 千禧年大奖问题，但陷入优先权争议](https://simonwillison.net/2026/Sep/8/on-navier-stokes/) ⭐️ 10.0/10

2026 年 9 月 8 日，OpenAI 宣布其内部前沿模型（称为 GPT-6 Astra）以约 10,000 个 AI 智能体集群的方式，生成了一个反例，证明三维欧几里得空间中 Navier–Stokes 方程解的崩溃，从而解决了 Navier–Stokes 存在性与平滑性这一千禧年大奖问题。该结果通过 Lean 证明助手进行了形式化验证，但尚未被外部数学家或克莱数学研究所独立验证。 如果得到验证，这将是首个由 AI 生成的千禧年大奖问题解决方案，标志着 AI 在深度数学推理能力方面的历史性里程碑，并可能重塑前沿数学研究的开展方式。该宣布还因与数学家 Tristan Buckmaster（纽约大学）和 Levent Alpöge（Anthropic）的优先权争议而更加复杂——后者已在此相关问题上工作了近一年，并指控 OpenAI 可能通过 Codex 会话数据获取了他们未发表的工作成果。 OpenAI 的智能体在 Navier–Stokes 问题中发送了 270 万条消息并使用了约 1300 亿输出 token，Lean 形式化验证又通过 GPT-6 Astra 耗时 17 小时；按公开 API 价格计算，所有尝试问题总共使用的 3000 亿 token 约需花费 1500 万美元。该反例建立在 Diego Córdoba 和 Luis Martínez-Zoroa 于 2023 年开发的用于在相关流体方程中发现爆破现象的方法之上，OpenAI 已表示不会领取 100 万美元的克莱千禧年奖金。

rss · Simon Willison · 9月8日 23:55

**背景**: Navier–Stokes 方程是一组描述流体在空间中运动的偏微分方程，虽然其计算解在工程和物理中被广泛使用，但对于三维空间中光滑解是否始终存在这一问题，目前仍缺乏完整的解析理解。克莱数学研究所于 2000 年设立了七个千禧年大奖问题，每个问题奖金 100 万美元，旨在新千年之际挑战数学界；截至 2026 年，仅有庞加莱猜想被正式解决。Navier–Stokes 存在性与平滑性问题问的是：给定三维空间和时间中的初始速度场，是否始终存在光滑且全局有定义的速度场和压力场来求解该方程——还是说解可能在有限时间内崩溃（爆破）。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Navier-Stokes_existence_and_smoothness_problem">Navier-Stokes existence and smoothness problem</a></li>
<li><a href="https://en.wikipedia.org/wiki/Millennium_Prize_Problems">Millennium Prize Problems - Wikipedia</a></li>
<li><a href="https://www.claymath.org/millennium-problems/">The Millennium Prize Problems - Clay Mathematics Institute</a></li>

</ul>
</details>

**社区讨论**: Tristan Buckmaster 公开指控 OpenAI 团队可能通过 Codex 会话获取了他和 Alpöge 未发表的工作，并指出 OpenAI 未直接回答模型是否在他们的数据上进行了训练。这场争议凸显了竞争性 AI 实验室之间的紧张关系——据报道 OpenAI 因 Alpöge 受雇于竞争对手 Anthropic 而将其排除在合著者之外，同时向 Buckmaster 提出了同步发布的安排。更广泛的数学界在就数学有效性和发现的伦理环境得出结论之前，很可能需要等待对该反例的独立验证。

**标签**: `#AI`, `#mathematics`, `#Navier-Stokes`, `#Millennium-Prize-Problems`, `#OpenAI`

---

<a id="item-2"></a>
## [苹果发布首款折叠屏手机 iPhone Duo](https://www.apple.com/iphone-duo/) ⭐️ 9.0/10

苹果正式发布了 iPhone Duo，这是其首款折叠屏智能手机，标志着苹果正式进入竞争对手三星长期主导的折叠屏手机品类。该设备在苹果最新的主题演讲中由 John Ternus 等高管揭晓。 这对全球市值最高的科技公司而言是一个重大战略转变，因为折叠屏手机是苹果尚未进入的少数硬件品类之一。苹果的入局可能重塑折叠屏市场的竞争格局，并影响整个移动硬件设计趋势。 早期上手体验报告显示，该设备屏幕上没有可见折痕，这是折叠屏技术的一项显著工程成就。然而，其定价据称比三星 Z Fold 8 高出约 50%，甚至比 Z Fold 8 Ultra 还贵数百美元，且折叠状态下宽度明显较大。

hackernews · thecosmicfrog · 9月9日 18:15 · [社区讨论](https://news.ycombinator.com/item?id=49630931)

**背景**: 折叠屏智能手机自 2019 年起开始商用，三星的 Galaxy Fold 及后续的 Z Fold/Z Flip 系列是该品类最突出的产品。这些设备使用柔性 OLED 显示屏和精密铰链机构，使手机大小的设备能够展开为更大的类平板屏幕。苹果在采用新形态方面历来谨慎，通常等到技术成熟后才进入某个产品品类。折叠屏市场一直在逐步增长，但与传统智能手机相比仍属小众细分市场。

**社区讨论**: 社区反应严重分化：一些人称赞其无折痕显示屏和整体设计，而另一些人则批评其极高的定价以及苹果日益程式化、情感平淡的演讲风格。多位评论者对手机越来越大的趋势表示不满，指出该设备即使折叠后也过宽，难以单手舒适使用。一个值得注意的技术观察将该设备的宽高比与 ISO 216 国际纸张尺寸标准进行了类比，即对折后比例保持不变。

**标签**: `#apple`, `#foldable-phone`, `#hardware`, `#product-announcement`, `#mobile`

---

<a id="item-3"></a>
## [Shopify 收购 Tailwind CSS，AI 冲击开发者工具行业](https://tailwindcss.com/blog/tailwind-is-joining-shopify) ⭐️ 9.0/10

Shopify 收购了最受欢迎的实用优先 CSS 框架之一 Tailwind CSS。此次收购发生在 Tailwind Labs 裁减 75% 工程团队、文档流量较 2023 年初下降约 40% 之后，这些变化均归因于 AI 对其商业模式的冲击。 此次收购表明 AI 正在从根本上颠覆依赖销售 UI 组件和文档流量的开发者工具企业，因为 AI 工具现在可以生成此前作为 Tailwind Labs 主要收入来源的样式代码和 UI 模板。这也标志着一个主要电商平台吸纳了一个被广泛使用的开源 Web 开发框架，可能会重塑数百万开发者构建店面和 Web 界面的方式。 Tailwind Labs 的商业模式将免费开源软件分发与 Tailwind UI 模板等付费高级产品相结合，而 AI 已使这一模式日益难以为继。社区成员指出 Shopify 收购的是人才和品牌，也有人质疑在 AI 辅助下构建新网站的开发者是否还需要 Tailwind，而非直接使用现代原生 CSS。

hackernews · EdwinHoksberg · 9月9日 13:27 · [社区讨论](https://news.ycombinator.com/item?id=49626190)

**背景**: Tailwind CSS 是一个开源的实用优先 CSS 框架，允许开发者通过在 HTML 中直接应用预定义的实用类来快速构建自定义用户界面，不同于 Bootstrap 等提供预定义组件类的传统框架。Tailwind Labs 是该框架背后的公司，主要通过 Tailwind UI 创收——这是一套面向开发者销售的优质预构建 UI 组件模板和设计模式。AI 编程助手的兴起侵蚀了这一模式，因为开发者现在可以通过提示 AI 工具生成等效的 UI 代码，从而减少了对付费模板和手动查阅文档的需求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Tailwind_CSS">Tailwind CSS - Wikipedia</a></li>
<li><a href="https://grokipedia.com/page/2026_Tailwind_Labs_layoffs">2026 Tailwind Labs layoffs — Grokipedia</a></li>
<li><a href="https://www.linkedin.com/posts/the-decoder-en_tailwinds-shattered-business-model-is-a-activity-7415025359001395200-M-XF">Tailwind 's shattered business model is a grim warning for every...</a></li>

</ul>
</details>

**社区讨论**: 社区情绪复杂但总体上对 Tailwind 团队表示同情，评论者认识到 AI 对 UI 模板销售业务的严重冲击。一个值得关注的争论是：当 AI 可以生成原生 CSS 时，Tailwind 是否还有必要存在，有人认为 AI 消除了当初促使 CSS 框架流行的 CSS 维护痛点。也有人将此次收购视为 Shopify 购买品牌和人才而非技术本身，考虑到模板销售商业模式的可行性正在下降。

**标签**: `#tailwind-css`, `#shopify`, `#acquisition`, `#ai-impact`, `#web-development`

---

<a id="item-4"></a>
## [🤖 OpenAI 称 GPT-6 Astra 的 CoT 可监测性显著下降](https://deploymentsafety.openai.com/gpt-6-astra) ⭐️ 9.0/10

OpenAI 正式披露，GPT-6 Astra 的思维链（CoT）可监测性显著下降，模型越来越多地自主控制推理过程，在完成复杂任务时减少了可观测的推理表达，引发了对 AI 对齐和安全监测的严重担忧。

telegram · zaihuapd · 9月9日 09:45

**标签**: `#AI Safety`, `#Chain of Thought`, `#OpenAI`, `#Model Interpretability`, `#GPT-6`

---

<a id="item-5"></a>
## [vLLM v0.29.0 将 Model Runner V2 设为默认运行时，新增 770B MoE 模型支持](https://github.com/vllm-project/vllm/releases/tag/v0.29.0) ⭐️ 8.0/10

vLLM v0.29.0 包含来自 277 位贡献者的 594 次提交，将 Model Runner V2（MRV2）设为所有模型的默认运行时，并新增支持多个大型 MoE 架构，包括腾讯 770B 的 Hy4-preview 和支持 NVFP4 量化的 Qwen3.8-Flash-Next。该版本还引入了将每步 logits 内存减少 1/TP 的分批采样、用于 KV 缓存自动调整的 CUDA 图内存分析，以及针对 Kimi-K3 和 DeepSeek V4 模型的显著内核级优化。 作为最广泛部署的开源 LLM 推理引擎之一，vLLM 将 MRV2 设为默认运行时标志着一项重大架构里程碑，有望在各类 GPU 平台上实现更清晰的模块化和更高的吞吐量。新增对 770B 规模 MoE 模型和 NVFP4 量化的支持，表明其已为在 NVIDIA Blackwell 硬件上部署下一代超大规模模型做好准备，直接影响运行前沿模型的团队的生产部署成本和延迟。 MRV1 仍用于少数 ROCm 模型以及 MRV2 尚不支持的功能，因此过渡尚未完全完成。重要的破坏性变更包括移除十个已弃用的模型架构、将 FlexOlmo/Olmo3/Hunyuan 迁移至 Transformers 后端、弃用 `python -m vllm.entrypoints.openai.api_server` 改为 `vllm serve`，以及移除 PyAV 视频解码器后端。性能亮点包括 K3 Mamba 元数据准备实现 6.6-7.6 倍内核加速，以及融合 MXFP4 top-k 终结化带来约 5% 的端到端延迟降低。

github · khluu · 9月9日 08:54

**背景**: vLLM 是一个高吞吐量的开源 LLM 推理与服务引擎，以 PagedAttention 和连续批处理等创新而闻名。Model Runner V2（MRV2）是对 vLLM 核心执行引擎的全新重写，旨在解决自 vLLM V1 以来积累的根本设计问题和技术债务，提供更清晰、更模块化的架构，在 GB200 系统上吞吐量提升最高达 56%。MoE（混合专家）模型每个 token 仅激活部分参数，使 770B Hy4-preview 等超大型模型能够高效运行。NVFP4 是 NVIDIA 面向 Blackwell GPU 的 4 位浮点格式，将超低精度存储与 FP8 缩放因子相结合，在减少内存带宽的同时保持精度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://vllm-website-5zwgmvte0-inferact-inc.vercel.app/blog/mrv2">Model Runner V 2 : A Modular and Faster Core for vLLM | vLLM Blog</a></li>
<li><a href="https://docs.vllm.ai/en/stable/design/model_runner_v2/">Model Runner V 2 Design Document - vLLM</a></li>
<li><a href="https://developer.nvidia.com/blog/introducing-nvfp4-for-efficient-and-accurate-low-precision-inference/">Introducing NVFP4 for Efficient and Accurate Low-Precision Inference | NVIDIA Technical Blog</a></li>

</ul>
</details>

**标签**: `#vllm`, `#llm-inference`, `#model-runner-v2`, `#moe-models`, `#gpu-optimization`

---

<a id="item-6"></a>
## [探讨 GPT-6 Astra、循环 Transformer 与隐藏推理](https://magazine.sebastianraschka.com/p/gpt-6-astra-looped-transformers-and) ⭐️ 8.0/10

Sebastian Raschka 发表了一篇深度分析文章，探讨循环 Transformer 架构和隐藏推理机制如何可能支撑 GPT-6 Astra 的能力，特别质疑内部迭代处理是否能替代显式的思维链（CoT）推理。文章将近期架构创新——即对同一潜在表示反复应用固定的 Transformer 模块——与 GPT-6 Astra 在计算机操作、软件工程等复杂任务上的最先进表现联系起来。 这一分析触及了 LLM 设计中的一个根本性架构问题：模型能否在不显式生成中间推理 token 的情况下，内部完成复杂的多步推理，从而大幅降低推理成本和延迟。这一争论的结果可能重塑未来前沿模型的设计方向，从冗长的思维链输出转向更高效的隐藏计算。 循环 Transformer 对同一潜在表示反复应用相同的 Transformer 模块——可能多达数十次——在概念上扩展了 2018 年提出的 Universal Transformer 架构。隐藏推理（迭代在内部潜在状态上进行）与显式 CoT（推理步骤作为 token 输出）之间存在关键的技术张力，Will Merrill 的研究表明某些计算复杂性类别最少需要特定深度的 CoT 才能求解。

hackernews · ModelForge · 9月9日 14:37 · [社区讨论](https://news.ycombinator.com/item?id=49627370)

**背景**: 循环 Transformer，又称循环深度或循环深度共享，通过反复重用固定的 Transformer 模块而非堆叠大量不同层来实现参数效率，同时支持更深的计算。这一概念可追溯至 2018 年的 Universal Transformers，它循环应用 Transformer 模块，在算法和语言理解任务上表现出优于标准 Transformer 的性能。思维链（CoT）推理是一种让 LLM 在得出最终答案前将中间推理步骤作为输出 token 生成的技术，实质上是用额外的推理 token 换取更强的推理能力。GPT-6 Astra 由 OpenAI 于 2026 年 9 月发布，是一个在计算机操作、浏览、软件工程和科学任务上均达到最先进水平的前沿模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.emergentmind.com/topics/looped-transformer-architecture">Looped Transformer Architecture</a></li>
<li><a href="https://arxiv.org/abs/1807.03819">[1807.03819] Universal Transformers</a></li>
<li><a href="https://openai.com/index/gpt-6-astra/">GPT-6 Astra: A new generation of intelligence | OpenAI</a></li>

</ul>
</details>

**社区讨论**: 讨论具有较高的技术深度，评论者 shawntan 分享了关键研究文献，包括 Will Merrill 关于 CoT 计算复杂性需求以及 Universal Transformers 的工作。围绕 wolttam 的观点——即对整个 Transformer 进行循环本身就是定义上的隐藏推理，因为模型的推理轨迹被内部反馈而非输出——引发了值得关注的讨论。多位用户报告了 Astra 在近期模型更新后性能下降的实际问题，siva7 指出质量显著下降，使模型感觉像是降级版本。

**标签**: `#transformers`, `#LLM-reasoning`, `#chain-of-thought`, `#universal-transformers`, `#AI-architecture`

---

<a id="item-7"></a>
## [揭露恶意软件广告如何绕过 Google 自动审核系统](https://xlii.space/eng/malicious-software-on-google-ads/) ⭐️ 8.0/10

一位安全研究人员发布了一篇详细的揭露文章，演示了恶意软件如何通过 Google Ads 成功投放，完全绕过了该平台的自动广告审核系统。在文章于 HackerNews 上引发关注后，Google 恢复了该研究者的账号，表明该问题仅因公开曝光才得到处理，而非系统自身的检测。 这一揭露暴露了 Google 自动广告审核基础设施的系统性缺陷，该系统每天处理数百万条广告，是互联网安全的关键守门人。恶意软件能够通过自动检查，而合法用户却经常遭到错误拒绝，这种危险的失衡可能使全球最大的广告平台之一成为大规模恶意软件分发的渠道。 研究者的账号仅在问题于 HackerNews 上获得曝光后才被恢复，表明 Google 的自动系统即使在恶意内容被标记后仍无法自我纠正。社区成员证实了这些发现，一位用户报告在 15 分钟内观察到的 YouTube 广告几乎全部是欺诈骗局，另一位用户则指出近十年前就存在类似的被攻陷网站投放广告的模式。

hackernews · xlii · 9月9日 11:43 · [社区讨论](https://news.ycombinator.com/item?id=49624856)

**背景**: Google Ads 运营着全球最大的数字广告网络之一，严重依赖自动审核系统在广告上线前进行筛查。随着广告量的增长，Google 越来越多地用机器学习模型取代人工审核员以扩展其审核流程。这一转变导致了有据可查的问题：合法用户和企业面临不透明的自动拒绝且没有有效的申诉途径，而恶意行为者则利用自动检查的漏洞分发恶意内容。

**社区讨论**: 社区情绪压倒性地批评 Google，评论者分享了合法提交被自动系统拒绝而欺诈广告泛滥的个人经历。多位用户认为大型科技公司越来越多地躲在自动系统背后以逃避责任，一些人建议通过监管要求强制设立人工联系点和透明的申诉流程。作者本人也指出，解决问题靠的是 HackerNews 上的公开 amplification，而非 Google 自身的安全保障机制，这颇具讽刺意味。

**标签**: `#security`, `#google-ads`, `#ad-fraud`, `#platform-abuse`, `#automated-review`

---

<a id="item-8"></a>
## [陶哲轩警告：AI 正以不可再生方式开采开放数学问题](https://simonwillison.net/2026/Sep/9/terence-tao/) ⭐️ 8.0/10

陶哲轩公开警告称，AI 驱动的研究正在以不可再生的速度开采开放数学问题，甚至仅仅是有人在研究某个问题的传闻，就可能引发大规模的 AI 攻关，在原始研究项目充分发挥潜力之前就将其 这一来自世界顶级数学家的警告揭示了学术文化面临的一种新型生存威胁：AI 正在制造反向激励，可能导致研究人员不再分享有前景的研究方向，从而逆转数百年来的开放科学传统，对该领域造成长期损害。 陶哲轩特别指出，优质且富有成果的开放问题正以不可再生的方式被耗尽，且当前的激励方向正指向保密而非开放，这将从根本上改变数学研究的开展与分享方式。

rss · Simon Willison · 9月9日 00:20

**背景**: 数学领域的开放科学传统长期以来依赖于研究人员公开分享问题和方向，使得协作研究可以在数年甚至数十年间持续推进。AI 工具如今能够快速探索并解决某些类别的数学问题，大幅压缩了以往允许更深入、更协作式探索的时间周期。陶哲轩是菲尔兹奖得主，被广泛认为是当今最伟大的数学家之一，因此他的评论具有特别的权威性。

**标签**: `#ai-ethics`, `#mathematics`, `#open-science`, `#ai-research`, `#academic-culture`

---
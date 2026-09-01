---
layout: default
title: "Horizon Summary: 2026-09-01 (ZH)"
date: 2026-09-01
lang: zh
---

> 从 37 条内容中筛选出 5 条重要资讯。

---

1. [Google 从 Chrome 网上应用店移除 MV2 扩展，uBlock Origin 失效](#item-1) ⭐️ 8.0/10
2. [互联网的中心化与 NAT 的原罪](#item-2) ⭐️ 8.0/10
3. [带注意力池的滑动窗口注意力在长上下文推理中超越线性注意力](#item-3) ⭐️ 8.0/10
4. [库克卸任苹果 CEO，特努斯接棒以 AI 为首要任务](#item-4) ⭐️ 8.0/10
5. [DeepSeek 发布 DeepSeek-V4-Flash-Vision-Exp 多模态模型权重](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Google 从 Chrome 网上应用店移除 MV2 扩展，uBlock Origin 失效](https://webiterate.dev/google-removed-extensions-ublock-origin-108/) ⭐️ 8.0/10

Google 已完成从 Chrome 网上应用店移除 Manifest V2（MV2）扩展的工作，实际上使 uBlock Origin（UBO）在 Chrome 浏览器上失效。超过 85% 的活跃维护扩展已迁移至 Manifest V3，Chrome 139 将开始从浏览器本身彻底移除 MV2 支持。 这标志着广告拦截战的一个具体转折点，因为 uBlock Origin 是 Chrome 上最受欢迎且最有效的广告拦截器，拥有数百万用户。鉴于 Google 本身是全球最大的广告公司，并且能从广告拦截能力削弱中获益，此举引发了人们对 Google 垄断控制网络生态系统的严重担忧。 使用 ExtensionManifestV2Availability 策略的企业用户至少在 2025 年 6 月之前仍可豁免。虽然主要广告拦截器都有 MV3 版本（包括 uBlock Origin Lite、AdBlock、Adblock Plus 和 AdGuard），但 MV3 的 declarativeNetRequest API 相比 MV2 的 webRequest API 对动态过滤能力施加了根本性限制。uBlock Origin 的开发者已确认该扩展在 Firefox 上运行效果最佳，Firefox 仍继续支持 MV2。

hackernews · twapi · 8月31日 21:10 · [社区讨论](https://news.ycombinator.com/item?id=49514878)

**背景**: Manifest V2 于 2012 年推出，作为 Chrome 扩展平台标准使用了十多年，允许 uBlock Origin 等扩展使用 webRequest API 动态拦截和阻止网络请求。Manifest V3 用 declarativeNetRequest 取代了这一机制，要求扩展预先声明过滤规则而非在运行时拦截请求，据称是出于性能和安全考虑。Google 数年前就宣布了 MV2 弃用计划，给开发者留出了迁移时间，但广告拦截社区中的许多人认为 MV3 从根本上削弱了内容过滤能力。Firefox 选择在实现 MV3 的同时继续支持 MV2，将自己定位为依赖强大广告拦截功能用户的首选浏览器。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.chrome.com/docs/extensions/develop/migrate/mv2-deprecation-timeline">Manifest V2 support timeline | Chrome for Developers</a></li>
<li><a href="https://blog.google/chromium/manifest-v2-phase-out-begins/">Manifest V2 phase-out begins</a></li>
<li><a href="https://dev.to/notearthian/whats-the-difference-between-manifest-v2-and-v3-in-browser-extensions-3b10">What's the Difference Between Manifest V2 and V3 in browser extensions? - DEV Community</a></li>

</ul>
</details>

**社区讨论**: 社区情绪强烈倾向于迁移到 Firefox，多位用户报告过渡过程顺利，并指出 uBlock Origin 本来在 Firefox 上运行效果就最好。一个突出主题是广告拦截作为安全问题——用户描述家中老人被恶意广告欺骗，认为 Google 未能从其自身服务中过滤有害广告，因此第三方拦截器不可或缺。多位评论者对 Google 垄断控制网络标准表示深切不信任，有人指出具有讽刺意味的是，2010 年 Chrome 曾因改善网络体验而受到赞誉，如今用户却积极鼓励亲友使用 Chrome 以外的任何浏览器。

**标签**: `#chrome`, `#ad-blocking`, `#uBlock-Origin`, `#manifest-v3`, `#browser-wars`

---

<a id="item-2"></a>
## [互联网的中心化与 NAT 的原罪](https://dreamstation.systems/personal/ntppost.html) ⭐️ 8.0/10

一篇文章认为 NAT 是早期的"原罪"，它通过削弱运行公共端点的能力而导致互联网中心化，引发了包括 Linux NAT 实现者反思权衡取舍在内的深入讨论。

hackernews · robinpie · 8月31日 02:23 · [社区讨论](https://news.ycombinator.com/item?id=49504905)

**标签**: `#networking`, `#NAT`, `#internet-architecture`, `#decentralization`, `#linux`

---

<a id="item-3"></a>
## [带注意力池的滑动窗口注意力在长上下文推理中超越线性注意力](https://www.reddit.com/r/MachineLearning/comments/1w3j1vw/slidingwindow_attention_beats_linear_on/) ⭐️ 8.0/10

Alexia Jolicoeur-Martineau 等人发布的一篇 arXiv 预印本表明，带注意力池的滑动窗口注意力（SWA）在 Needle-in-a-Haystack 和 BABILong 等长上下文推理基准上，性能比线性注意力变体高出 2 到 10 倍，且无需任何后训练。作者认为，线性注意力这一研究方向此前未与更简单的基线进行正确比较。 这一发现直接挑战了当前一个重要的研究方向——各实验室投入大量后训练算力开发用于长上下文 LLM 的线性注意力模型，暗示这些资源或许应投向别处。如果得到验证，它可能改变行业处理长上下文效率问题的方式，使一种更简单、无需训练的方法取代更复杂的架构改动。 带注意力池的 SWA 无需后训练、运行速度快且内存占用低，而线性注意力模型可能需要从头训练或经过大量后训练才能勉强匹配 SWA 的性能。作者强烈建议改用 SWA 而非对线性模型进行后训练，但该论文目前仍为 arXiv 预印本，尚待同行验证。

reddit · r/MachineLearning · /u/Justgototheeffinmoon · 8月31日 16:35

**背景**: 标准 Transformer 注意力机制的计算成本相对于序列长度呈二次增长，这催生了线性注意力（用线性运算替代 softmax）和滑动窗口注意力（将注意力限制在固定大小窗口内）等替代方案。注意力池是吸收多余注意力的特殊 token，充当结构性锚点，在旧 token 被滑动窗口移除时稳定生成过程。BABILong 是一个专门测试模型能否在极长干扰文本中提取并推理稀疏事实的基准，即使是声称支持 128K token 的 GPT-4 等模型也会出现性能下降。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2608.28444v1">Sliding - window beats linear attention</a></li>
<li><a href="https://arxiv.org/abs/2406.10149">[2406.10149] BABILong : Testing the Limits of LLMs with Long ...</a></li>
<li><a href="https://carnotresearch.medium.com/let-the-chaos-sink-in-481c8a37471e">Let the Chaos Sink In. Balancing attention in transformers | Medium</a></li>

</ul>
</details>

**标签**: `#attention-mechanisms`, `#long-context`, `#llm-efficiency`, `#linear-attention`, `#research`

---

<a id="item-4"></a>
## [库克卸任苹果 CEO，特努斯接棒以 AI 为首要任务](https://www.bloomberg.com/news/articles/2026-08-30/apple-s-new-ceo-john-ternus-takes-reins-from-tim-cook-focusing-on-ai) ⭐️ 8.0/10

8 月 31 日是库克担任苹果 CEO 的最后一天，51 岁的硬件工程老将特努斯自 9 月 1 日起接任，库克留任执行主席。新 CEO 的当务之急包括推动 AI 落地、补齐 Siri 升级延期等短板，以及 9 月 9 日秋季发布会上推出苹果首款折叠屏 iPhone。 这是自 2011 年库克接替乔布斯以来苹果首次 CEO 更替，标志着公司将 AI 置于未来战略的核心位置。此次领导层变动正值苹果在 AI 能力上面临谷歌和 OpenAI 等竞争对手日益增长的压力之际。 即将发布的折叠屏 iPhone 据称配备 12GB 内存，并深度植入 Siri AI，可结合屏幕、日历与相机输入来理解现实场景。Apple Intelligence 于 2024 年 WWDC 发布，依赖设备端与服务器端混合处理，部分功能将在 2025 年逐步推出。

telegram · zaihuapd · 8月31日 10:21

**背景**: Apple Intelligence 是苹果于 2024 年 WWDC 发布的 AI 框架，将 AI 功能集成到 iOS 18 及后续版本中，采用设备端与云端混合处理方式。库克自 2011 年接替乔布斯担任苹果 CEO 以来，主导了公司在服务业务和可穿戴设备领域的大规模扩张。特努斯此前领导苹果硬件工程部门，负责包括 iPhone、iPad 和 Mac 在内的产品线开发。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Apple_Intelligence">Apple Intelligence - Wikipedia</a></li>
<li><a href="https://www.apple.com/apple-intelligence/">Apple Intelligence and Siri - Apple</a></li>
<li><a href="https://appleinsider.com/articles/26/08/28/iphone-ultra-what-to-expect-from-apples-first-foldable-iphone-and-when">iPhone Ultra rumors: design, release date, cost</a></li>

</ul>
</details>

**标签**: `#Apple`, `#CEO-transition`, `#AI-strategy`, `#consumer-hardware`, `#industry-news`

---

<a id="item-5"></a>
## [DeepSeek 发布 DeepSeek-V4-Flash-Vision-Exp 多模态模型权重](https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash-Vision-Exp) ⭐️ 8.0/10

DeepSeek 发布了 V4 系列首款实验性多模态模型 DeepSeek-V4-Flash-Vision-Exp，在 V4-Flash 架构上加入视觉模块并进行持续训练。相比 V4-Flash-0731，其多模态 agent 能力大幅提升，ApexBench 分数从 26.2 升至 36.5，而文本 agent 任务表现基本持平。 此次发布标志着 DeepSeek 将 V4-Flash 架构扩展至多模态视觉能力领域，拓宽了模型在需要视觉理解和 agent 推理任务上的适用范围。ApexBench 的大幅提升证明视觉模块集成效果显著，使 DeepSeek 在多模态 AI agent 领域与 Opus-4.8 等模型的竞争中更具优势。 V4-Flash 底层架构为混合专家模型，总参数量 284B，但每次前向传播仅激活 13B 参数，支持 100 万 token 的上下文窗口。ApexBench 是本次发布中报告的多模态 agent 评估基准，但 DeepSeek 未公开披露其任务数量或创建机构。据报道，该模型在 Agents' Last Exam 和 ZeroBench Pass@5 等部分基准上超越 Opus-4.8，但在 ApexBench 和 Chartography 上仍有差距。

telegram · zaihuapd · 8月31日 11:41

**背景**: DeepSeek-V4-Flash 是一款以效率为核心的混合专家模型，采用混合注意力架构，结合压缩稀疏注意力（CSA）和重度压缩注意力（HCA）来大幅提升长上下文处理效率。在 100 万 token 上下文设置下，V4-Pro 变体仅需 DeepSeek-V3.2 的 27% 单 token 推理 FLOPs 和 10% KV 缓存。多模态 agent 是能够规划、使用工具并处理纯文本以外输入输出（如图像和视觉界面）的 AI 系统。"Exp" 实验性标识表明这是一款用于研究和测试的早期阶段发布版本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash">deepseek-ai/DeepSeek-V4-Flash · Hugging Face</a></li>
<li><a href="https://deepinfra.com/deepseek-ai/DeepSeek-V4-Flash">DeepSeek V4 Flash API - Demo - DeepInfra</a></li>
<li><a href="https://explainx.ai/blog/deepseek-v4-flash-vision-exp-multimodal-agent-august-2026">DeepSeek V4-Flash-Vision-Exp: Multimodal Agent Benchmarks</a></li>

</ul>
</details>

**标签**: `#deepseek`, `#multimodal-models`, `#vision-models`, `#llm-release`, `#ai-research`

---
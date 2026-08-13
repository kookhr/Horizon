---
layout: default
title: "Horizon Summary: 2026-08-13 (ZH)"
date: 2026-08-13
lang: zh
---

> 从 32 条内容中筛选出 10 条重要资讯。

---

1. [Google 发布 Gemini 3.7 Flash，视觉与推理能力提升](#item-1) ⭐️ 9.0/10
2. [Cerebras 与 OpenAI 推出 GPT-5.6 Sol Ultrafast 模式](#item-2) ⭐️ 9.0/10
3. [DeepSeek 发布 V4 Pro 0813：1.7T 参数开源权重模型](#item-3) ⭐️ 9.0/10
4. [长鑫存储市值超越腾讯，登顶中国市值最高公司](#item-4) ⭐️ 9.0/10
5. [DeepSeek-V4-Pro 正式版上线，API 实行峰谷定价](#item-5) ⭐️ 9.0/10
6. [Christopher Domas 公布](#item-6) ⭐️ 8.0/10
7. [选择无聊技术：一篇关于技术选型的基础性文章](#item-7) ⭐️ 8.0/10
8. [DeepSeek Harness 开发者预览版发布](#item-8) ⭐️ 8.0/10
9. [特朗普签署备忘录，授权私企开展政府背书的海外网络攻击](#item-9) ⭐️ 8.0/10
10. [DeepMind 推出 SL2T 手语转文字模型，首次落地 Pixel 11](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Google 发布 Gemini 3.7 Flash，视觉与推理能力提升](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-3-7-flash/) ⭐️ 9.0/10

Google 发布了 Gemini 3.7 Flash，这是一款新的轻量级 AI 模型，具备更强的视觉能力、在金融和法律等知识密集型领域提升的推理能力，以及具有竞争力的入门定价。它在 GDP.pdf（34.0% 对 22.0%）和 AutomationBench（30.4% 对 17.0%）等基准测试上显著超越了前代 3.6 Flash。 此次发布加剧了轻量级 AI 模型市场的竞争，Google 将 Flash 定位为适用于高吞吐量、真实业务工作流和多模态任务的高性价比主力模型。该模型强大的视觉能力和文档处理能力使其在企业级复杂文档理解应用中尤为重要。 入门定价计划于 2026 年 12 月 31 日翻倍，考虑到模型发布节奏之快——3.6 Flash 仅仅三周前才发布——这引发了对长期价值的质疑。该模型支持可调节的思考级别（高、中、低）以控制推理 token 的使用量，并可与 Nano Banana 等其他 Google 工具结合用于动态内容生成。

hackernews · thisisauserid · 8月13日 17:23 · [社区讨论](https://news.ycombinator.com/item?id=49289112)

**背景**: Gemini 是 Google DeepMind 开发的多模态大语言模型系列，其中 Flash 变体专为高吞吐量场景设计的轻量级、高性价比选项。Flash 系列传统上定位于低成本的文本任务，如摘要、解析和格式化，但 Google 现在正将其能力扩展到更复杂的推理和视觉任务。AI 模型市场目前正处于快速迭代期，OpenAI 的 GPT-5.6 Luna 和 Anthropic 的 Opus 5 等竞争对手在同一轻量级细分市场中提供了极具竞争力的定价和性能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-3-7-flash/">Gemini 3.7 Flash: our most intelligent workhorse model</a></li>
<li><a href="https://deepmind.google/models/gemini/flash/">Gemini 3.7 Flash — Google DeepMind</a></li>

</ul>
</details>

**社区讨论**: 社区测试显示 Gemini 3.7 Flash 在图像转 HTML 任务上表现令人印象深刻，尽管 Anthropic 的 Opus 5 在此类视觉任务中仍然是同类最佳，但价格也更贵。用户对不寻常的定价策略——入门价格在五个月内翻倍——表示担忧，并质疑该模型面对 GPT-5.6 Luna 等更便宜替代品时的竞争力，后者以更低的成本提供了强劲的基准测试表现。多位评论者指出，Flash 的定位似乎已从低成本文本处理转向与 Terra 而非 Luna 等中端模型更直接的竞争。

**标签**: `#AI`, `#LLM`, `#Google`, `#Gemini`, `#Machine Learning`

---

<a id="item-2"></a>
## [Cerebras 与 OpenAI 推出 GPT-5.6 Sol Ultrafast 模式](https://www.cerebras.ai/blog/accelerating-gpt-5-6-sol-ultrafast-with-openai) ⭐️ 9.0/10

Cerebras 和 OpenAI 宣布为 GPT-5.6 Sol 推出全新的 "Ultrafast" 模式，在 HLE 基准测试中处理全部 2,500 道题目仅需 11 小时 11 分钟，而 Claude Fable 5 需要 78 小时 27 分钟，在达到相当准确率的前提下速度提升近 7 倍。该系统利用 Cerebras 的晶圆级计算技术，大幅缩短了前沿大语言模型的推理时间。 这一合作表明，专用硬件能够从根本上改变运行前沿 AI 模型的经济性和可行性，使高能力推理在极短时间内即可实现。速度的提升可能催生 LLM 迭代式思维的新范式，模型可以进行多轮推理和修正，而非依赖单次输出。 根据公告中引用的 Artificial Analysis 数据，GPT-5.6 Sol 在 Ultrafast 模式下的运行速度比 Fable 5 快 11 倍，比 Opus 4.8 的 Fast 模式快 5 倍。然而，Cerebras 和 OpenAI 均未明确说明 Ultrafast 模式的输出质量与标准 GPT-5.6 Sol 完全一致，也未披露定价信息，表明该功能可能仍处于评估市场兴趣的阶段。

hackernews · pr337h4m · 8月13日 18:10 · [社区讨论](https://news.ycombinator.com/item?id=49289844)

**背景**: 晶圆级集成（WSI）是一种用整片硅晶圆构建超大规模集成电路的方法，产出单个"超级芯片"，从而避免传统多芯片设计中固有的片外通信瓶颈。Cerebras Systems 以其 Wafer-Scale Engine（WSE）系列开创了这一技术，在单个芯片上集成了数十万个核心及本地快速存储。HLE（Humanity's Last Exam）基准测试被明确设计为前沿难度测试，旨在让当前任何 AI 模型都无法完全解答，从而在系统之间提供多年的区分窗口。GPT-5.6 Sol 是 OpenAI GPT-5.6 模型系列中的旗舰版本，于 2026 年发布，针对复杂推理、编程和长周期问题求解进行了优化。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Wafer-scale_integration">Wafer-scale integration - Wikipedia</a></li>
<li><a href="https://www.usenix.org/publications/loginonline/wafer-scale-ai-compute-system-software-perspective">Wafer-Scale AI Compute: A System Software Perspective</a></li>
<li><a href="https://en.wikipedia.org/wiki/Humanity's_Last_Exam">Humanity's Last Exam - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/GPT-5.6_Sol">GPT-5.6 Sol</a></li>

</ul>
</details>

**社区讨论**: 社区情绪既有兴奋也有理性的质疑。iamcoder18 和 wxw 等用户强调了令人印象深刻的速度指标，wxw 指出相比 Fable 5 和 Opus 4.8 分别有 11 倍和 5 倍的速度优势。csallen 提出了深刻见解，认为速度使迭代推理成为可能，可能将 LLM 思维从单次输出转向多轮修正。然而，Topfi 担忧两家公司均未明确确认 Ultrafast 模式与标准 GPT-5.6 Sol 的性能完全一致，GodelNumbering 则指出缺乏定价信息，暗示该功能可能价格高昂或仍处于需求评估阶段。

**标签**: `#AI`, `#Cerebras`, `#OpenAI`, `#LLM`, `#Hardware`

---

<a id="item-3"></a>
## [DeepSeek 发布 V4 Pro 0813：1.7T 参数开源权重模型](https://simonwillison.net/2026/Aug/12/deepseek-v4-pro-0813/) ⭐️ 9.0/10

DeepSeek 发布了 V4 Pro 0813，这是一个拥有 1.7 万亿参数的混合专家模型，其开放权重已在 Hugging Face 上提供（893 GB），并可通过 OpenRouter 的 API 访问。该模型支持 1,048,576 个 token 的上下文窗口，最大输出为 384,000 个 token，在 OpenRouter 上的定价为每百万输入 token 0.435 美元，每百万输出 token 0.87 美元。 发布 1.7T 参数的开放权重模型是开源 AI 社区的一个里程碑式事件，突破了公开可用模型的边界。它加剧了与专有模型的竞争，并以相对较低的 API 成本为开发者和研究人员提供了前沿规模的模型能力。 该模型具有三个不同的推理级别（低、中、高），能产生明显不同的输出，这是早期测试者注意到的一个不寻常特征。尽管它在 Artificial Analysis 智能指数上得分 53（远高于中位数的 27），但一些开发者对其整体基准测试表现感到失望，并对定价表示不满。

rss · Simon Willison · 8月12日 23:59

**背景**: DeepSeek 是一家中国 AI 初创公司，因发布大规模开放权重模型而备受关注，此前曾在 4 月发布 DeepSeek-V4-Pro，7 月发布 DeepSeek-V4-Flash-0731。V4 Pro 0813 模型采用混合专家架构，在推理时仅激活部分参数，从而在庞大的总参数量下保持效率。OpenRouter 是一个统一的 API 网关，通过单一接口提供来自不同提供商的数百个 AI 模型的访问，使新模型能立即被开发者使用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4-pro-0813">DeepSeek V4 Pro 0813 - API Pricing & Benchmarks | OpenRouter</a></li>
<li><a href="https://artificialanalysis.ai/models/deepseek-v4-pro">DeepSeek V4 Pro 0813 (max) - Intelligence, Performance & Price Analysis</a></li>
<li><a href="https://www.scmp.com/tech/big-tech/article/3363895/deepseeks-updated-v4-pro-ai-model-struggles-benchmarks-shines-cybersecurity">DeepSeek’s updated V4 Pro AI model struggles on benchmarks, shines in cybersecurity | South China Morning Post</a></li>

</ul>
</details>

**社区讨论**: 社区反应褒贬不一：虽然 1.7T 参数模型的开放权重发布被广泛认为是一项重要成就，但 Reddit 和 Hacker News 等平台上的开发者注意到，基准测试结果最初仅通过微信群分享，之后才被复制到西方论坛。部分用户对模型的整体能力和定价感到失望，而另一些用户则认为不同推理级别下输出的显著差异是一个值得进一步探索的有趣且独特的特征。

**标签**: `#llm`, `#deepseek`, `#open-weights`, `#ai`, `#openrouter`

---

<a id="item-4"></a>
## [长鑫存储市值超越腾讯，登顶中国市值最高公司](https://www.bloomberg.com/news/articles/2026-08-13/cxmt-overtakes-tencent-to-become-most-valuable-chinese-company) ⭐️ 9.0/10

长鑫存储（CXMT）市值超越腾讯，成为中国市值最高的公司，截至周四市值约为 5240 亿美元，而腾讯估值降至 5100 亿美元。长鑫存储上月在上海科创板上市，首日暴涨 467%，此后又涨 8%。 这标志着中国科技格局的历史性转变——一家半导体存储公司超越长期主导市场的互联网巨头，成为市值最高的企业。这表明市场正大规模向硬件和芯片制造领域重新配置，其背后驱动力是中国对半导体自主可控的战略推进以及 DRAM 供应链日益增长的重要性。 腾讯股价今年以来累计下跌超 26%，仅周四就跌了 4.5%，主要原因是大规模 AI 投入拖累了盈利能力。根据 Omdia 数据，按 2025 年第四季度销售额计算，长鑫存储以约 7.67%的全球市场份额排名全球第四大 DRAM 厂商，仅次于三星、SK 海力士和美光，SemiAnalysis 预计其市场份额到 2028 年将从约 11%升至 15%。

telegram · zaihuapd · 8月13日 10:10

**背景**: 长鑫存储技术股份有限公司成立于 2016 年，总部位于安徽合肥，是一家专注于 DRAM（动态随机存取存储器）芯片设计、研发、生产和销售的一体化存储器制造企业。该公司于 2026 年 7 月在上海科创板上市，募资约 295 亿元人民币（约合 43 亿美元），是 2026 年中国规模最大的 IPO。DRAM 是计算设备中的关键元器件，全球市场长期由三星、SK 海力士和美光主导，长鑫存储在中美科技紧张局势下作为中国在这一战略关键领域的龙头企业崛起。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zh.wikipedia.org/wiki/长鑫存储">长鑫存储 - 维基百科，自由的百科全书</a></li>
<li><a href="https://www.geekpark.net/news/368087">上 市 暴涨的 长 鑫 存 储 ，直接把美国股 市 干崩了 | 极客公园</a></li>
<li><a href="https://www.tmtpost.com/8079902.html">长 鑫 存 储 上 市 ，赶 上 了一个好时候-钛媒体官方网站</a></li>

</ul>
</details>

**标签**: `#semiconductors`, `#CXMT`, `#Tencent`, `#market-cap`, `#China-tech`

---

<a id="item-5"></a>
## [DeepSeek-V4-Pro 正式版上线，API 实行峰谷定价](https://api-docs.deepseek.com/zh-cn/updates) ⭐️ 9.0/10

DeepSeek-V4-Pro 正式版已同步上线 APP、网页端和 API，模型名为 deepseek-v4-pro，增强了 Agent 能力并原生支持 Responses API 格式以适配 Codex。V4-Pro 和 V4-Flash 的思考模式新增 low、high、max 三档，API 将实行峰谷定价，新价格于 2026 年 8 月 17 日 0 时生效，闲时价格为高峰时段的一半。 此次发布是这一广泛使用的开源 AI 模型系列的重大能力升级，将直接影响 AI/ML 开发流程和部署成本。峰谷定价模式引入了新的成本管理维度，可能重塑开发者调度 API 密集型任务的方式。 Responses API 目前仅支持 deepseek-v4-flash，deepseek-v4-pro 的支持计划于 2026 年 8 月初上线。高峰时段为北京时间 09:00–12:00 和 14:00–18:00（UTC+8），DeepSeek 建议在 Think Max 模式下将上下文窗口设置为至少 384K tokens，因为推理链可能非常长。

telegram · zaihuapd · 8月13日 11:12

**背景**: DeepSeek 是一家知名的 AI 模型提供商，以其开源权重的大语言模型而闻名。Responses API 是一种较新的 API 格式，支持智能体工作流和工具调用，设计上兼容 OpenAI 的 Codex 生态系统。思考模式允许模型在输出最终答案前先生成思维链推理，更高的档位会生成更长的推理链，从而在复杂问题上提升准确性。峰谷定价是一种需求管理策略，高流量时段的 API 调用费用高于低流量时段。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://api-docs.deepseek.com/guides/responses_api/">Using the Responses API | DeepSeek API Docs</a></li>
<li><a href="https://api-docs.deepseek.com/guides/thinking_mode/">Thinking Mode | DeepSeek API Docs</a></li>
<li><a href="https://chat-deep.ai/pricing/deepseek-api-cost-calculator/">DeepSeek API Cost Calculator: V4 Flash & Pro</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#LLM`, `#AI`, `#API`, `#Release`

---

<a id="item-6"></a>
## [Christopher Domas 公布](https://github.com/xoreaxeaxeax/skitter-creek-bath-salts) ⭐️ 8.0/10

Christopher Domas presents 'Spaghettifying DRAM,' a hardware-level technique for manipulating DRAM to gain ring-0 access, with significant implications for system and console security.

hackernews · matt_d · 8月13日 14:17 · [社区讨论](https://news.ycombinator.com/item?id=49286341)

**标签**: `#hardware security`, `#DRAM`, `#privilege escalation`, `#x86`, `#vulnerability`

---

<a id="item-7"></a>
## [选择无聊技术：一篇关于技术选型的基础性文章](https://mcfunley.com/choose-boring-technology) ⭐️ 8.0/10

Dan McKinley 在 2015 年的文章《选择无聊技术》中提出，公司应刻意选择经过验证的、'无聊的'技术而非新技术，以降低运营风险和复杂性，并引入了'创新代币'的概念来量化团队可以安全采用的新技术数量。该文章近期在讨论中再次受到关注，社区成员将其框架应用于 AI 代理等现代场景。 这篇文章在工程管理和软件架构领域仍然是一个基础性参考，为在创新与稳定性之间做出技术权衡提供了实用框架。其核心理念——每项新技术都会引入隐藏的运营成本——持续影响着工程领导者对技术栈决策的思考方式，尤其是当团队面临 AI 代理等快速涌现的新技术的诱惑时。 该文章提出每个公司大约有三个'创新代币'可用于新技术，选择无聊技术免费，而选择创新技术则需要花费代币。McKinley 反对'最佳工具'思维，强调公司的真正工作是维持运营，而最佳工具是在尽可能多的问题上占据'最不糟糕'位置的工具。

hackernews · tosh · 8月13日 17:48 · [社区讨论](https://news.ycombinator.com/item?id=49289512)

**背景**: Dan McKinley 在 Etsy 担任软件工程师的六年中形成了这一理念，当时 Etsy 的工程团队以高生产力著称，尽管使用的是许多人认为'无聊'的技术。'创新代币'的概念源于一个观察：采用新技术会在培训、调试、基础设施和运营复杂性方面引入隐藏成本，而这些成本在初始选择时并不明显。该文章挑战了工程师追逐前沿技术的常见倾向，认为成熟、被充分理解的技术往往能提供更好的商业价值，正是因为它们的故障模式是已知且有文档记录的。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mcfunley.com/choose-boring-technology">Choose Boring Technology - Dan McKinley</a></li>
<li><a href="https://mattrickard.com/innovation-tokens">Innovation Tokens | Matt Rickard</a></li>
<li><a href="https://www.linkedin.com/pulse/technical-debt-innovation-tokens-case-boring-technology-jeffrey-henry-lhexe">Technical Debt, Innovation Tokens , and the Case for Boring...</a></li>

</ul>
</details>

**社区讨论**: 讨论显示对该文章核心理念的强烈支持，一位评论者称其为任何工程师的必修课，另一位则赞扬'创新代币'是向各层级同事解释权衡的宝贵工具。一个值得关注的观点建议将该框架应用于 AI 代理：将所有创新代币集中投入 AI 代理，同时保持周围技术栈的无聊性，即使用代理最擅长的'分布内技术'。然而也有反对声音，一位评论者认为'创新代币'是一个随意且不够严肃的框架，工程师在评估任何技术时应专注于理解需求、风险、权衡和潜在收益。

**标签**: `#engineering-management`, `#technology-selection`, `#software-architecture`, `#ai-agents`, `#best-practices`

---

<a id="item-8"></a>
## [DeepSeek Harness 开发者预览版发布](https://deepseek.com/harness/en/) ⭐️ 8.0/10

DeepSeek 发布了 DeepSeek Harness 的开发者预览版，这是一个采用 MIT 许可证的开源智能体框架，其中所有功能——模型、工具、会话、沙箱、存储、调度和 UI——都是可替换的插件。该框架基于 Cordis v4 构建，这是一篇新发布的插件架构论文，支持热重载和动态加载/卸载插件而无需重启运行中的进程。 该框架的完全可追溯会话日志——以仅追加事件流的形式记录系统提示、推理过程、工具调用、子智能体调度和上下文注入——被视为与美方模型的关键差异点，后者的追踪记录通常被加密或混淆。这种透明度使得对智能体轨迹的恢复、分叉、搜索和重放操作成为可能，对于调试、审计和建立对智能体系统的信任具有重要价值。 Cordis v4 此前已有生产环境使用经验：它在另一个名为 Koishi 的项目中使用了四年（基于 v3 版本），该框架对时空可组合性的代数方法允许插件在卸载时回滚状态和副作用，包括清理连接、内存分配和已注册的处理器。该项目明确表示这是一个早期开发者预览版，存在预期的粗糙之处和兼容性破坏性变更，一位评论者指出底层论文对有编程语言理论（PLT）知识的人来说有用但并非革命性的。

hackernews · bjin · 8月13日 12:58 · [社区讨论](https://news.ycombinator.com/item?id=49285244)

**背景**: 智能体框架是编排由大语言模型驱动的智能体执行任务的软件系统，负责管理工具调用、上下文和多步推理。智能体开发中的一个关键挑战是可观测性——理解模型在每一步看到了什么、做出了什么决策以及执行了什么操作。Cordis 是一个面向 JavaScript 应用的 AOP（面向切面编程）框架，用于管理插件状态和上下文，其 v4 论文描述了一种"时空可组合性"的编程范式——即在动态组合、加载和卸载组件的同时正确管理其状态和副作用的能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.deepseek.com/harness/en/">DeepSeek Harness developer preview: Everything is a plugin</a></li>
<li><a href="https://github.com/deepseek-ai/deepseek-harness">GitHub - deepseek-ai/deepseek-harness: DeepSeek Harness ...</a></li>
<li><a href="https://npm.io/package/cordis">Cordis NPM | npm.io</a></li>

</ul>
</details>

**社区讨论**: 社区态度谨慎乐观，用户称赞完全可追溯的会话日志是区别于美方加密追踪模型的"杀手级功能"。项目作者（tianyicui）承认这是一个存在粗糙之处的早期预览版，而技术评论者讨论了 Cordis v4 的热重载和状态清理能力，其中一位指出对于熟悉编程语言理论的人来说，该方法有用但属于渐进式改进而非范式转变。

**标签**: `#deepseek`, `#agent-framework`, `#cordis`, `#traceability`, `#developer-tools`

---

<a id="item-9"></a>
## [特朗普签署备忘录，授权私企开展政府背书的海外网络攻击](https://www.bloomberg.com/news/articles/2026-08-13/trump-enlists-private-sector-to-boost-cyber-offensive-arsenal) ⭐️ 8.0/10

美国前总统特朗普签署了一份备忘录，授权受联邦政府直接控制和监督的私营企业在海外开展监控和网络攻击，以打击针对美国人的跨国犯罪组织。国土安全部将与司法部协调监督该项目，参与企业须维持至少 100 万美元的保证金或托管款。 这一政策逆转废除了数十年来禁止私营企业开展进攻性网络行动或"反击黑客"攻击的美国网络安全规范。它标志着治国方略的根本性转变，正式将私营部门纳入国家背书的进攻性网络行动，可能重塑网络安全行业并动摇网络战争的国际准则。 参与企业必须在联邦政府的直接控制和监督下运营，并须维持 100 万美元的保证金或托管款，如不遵守合同约定该款项将被没收。授权私营企业开展进攻性网络行动的法律依据尚未在法庭上经过检验，其法律效力在司法审查下能否成立仍存疑问。

telegram · zaihuapd · 8月13日 05:10

**背景**: 数十年来，美国网络安全政策一直禁止私营企业开展"反击黑客"行动或进攻性网络攻击，此类活动仅限政府机构和军事实体进行。特朗普政府的国家网络安全战略明确设想让私营企业在进攻性网络行动中发挥更大作用。这份备忘录是美国政府首次正式授权经过审查的私营企业开展进攻性网络行动，打破了长期以来的政策惯例。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://techcrunch.com/2026/08/13/in-a-first-us-will-allow-some-private-firms-to-carry-out-cyberattacks/">In a first, US will allow some private firms to carry out ...</a></li>
<li><a href="https://www.techtimes.com/articles/324283/20260813/trump-authorizes-private-firms-hack-foreign-criminals-legal-basis-untested-courts.htm">Trump Authorizes Private Firms to Hack Foreign Criminals ...</a></li>
<li><a href="https://www.lawfaremedia.org/article/trump-admin-cyber-strategy-centers-private-sector-in-offensive-cyber-operations">Trump Admin Cyber Strategy Centers Private Sector in ...</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#policy`, `#government`, `#offensive-security`, `#private-sector`

---

<a id="item-10"></a>
## [DeepMind 推出 SL2T 手语转文字模型，首次落地 Pixel 11](https://deepmind.google/blog/putting-sign-language-ai-into-users-hands/) ⭐️ 8.0/10

谷歌 DeepMind 发布了大规模多语言手语转文字模型 SL2T，现已部署在 Pixel 11 设备上，为 Gboard 和 Live Transcribe 提供美国手语（ASL）翻译功能。该模型使用超过 10 万小时、涵盖 50 多种手语的数据进行训练，在 FLEURS-ASL 基准测试中零样本得分达到 70 BLEURT，大幅超越了此前纪录。 这标志着手语 AI 翻译首次被集成到主流消费产品中，是听障用户无障碍技术领域的一个重要里程碑。在 Pixel 11 等广泛可用的设备上部署，证明了实时手语翻译在消费级层面已具备技术可行性，有望为更多设备和语言的扩展铺平道路。 为保护用户隐私，SL2T 仅处理手部和身体姿态关键点，不读取原始视频。目前该模型仅支持 ASL 到英语的翻译，且仅在 Pixel 11 设备上可用，未来计划扩展至更多语言和设备。

telegram · zaihuapd · 8月13日 08:55

**背景**: 手语翻译长期以来一直是主流机器翻译研究的边缘领域，部分原因在于缺乏标准化基准测试。2024 年推出的 FLEURS-ASL 将多语言 FLORES/FLEURS 基准扩展为支持以视频形式呈现的美国手语，由认证聋人译员翻译，有助于弥合手语与文本机器翻译之间的差距。BLEURT 是一种基于 BERT 的学习型评估指标，用于衡量生成翻译在传达参考句含义和流畅度方面的表现，是比 BLEU 等传统指标更贴近人类判断的替代方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepmind.google/blog/putting-sign-language-ai-into-users-hands/">Putting sign language AI into users’ hands</a></li>
<li><a href="https://siliconangle.com/2026/08/12/google-debuts-sl2t-ai-model-thats-designed-understand-sign-language/">Google debuts SL2T, an AI model that's designed to understand sign language - SiliconANGLE</a></li>
<li><a href="https://arxiv.org/abs/2408.13585">FLEURS-ASL: Including American Sign Language in Massively ... Title:FLEURS-ASL: Including American Sign Language in ... [PDF] FLEURS-ASL: Including American Sign Language in ... (PDF) FLEURS-ASL: Including American Sign Language in ... AITopics | FLEURS-ASL: Including American Sign Language in ...</a></li>
<li><a href="https://github.com/google-research/bleurt">GitHub - google-research/bleurt: BLEURT is a metric for ...</a></li>

</ul>
</details>

**标签**: `#Google DeepMind`, `#Sign Language Translation`, `#Accessibility AI`, `#SL2T`, `#Pixel`

---
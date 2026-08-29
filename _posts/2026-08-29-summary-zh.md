---
layout: default
title: "Horizon Summary: 2026-08-29 (ZH)"
date: 2026-08-29
lang: zh
---

> 从 30 条内容中筛选出 9 条重要资讯。

---

1. [腾讯混元发布 Hy4 preview，盲测得分略胜 GLM-5.3 与 Kimi K3](#item-1) ⭐️ 9.0/10
2. [智谱 AI 开源 GLM-5.3，主打智能体编程与网络防御](#item-2) ⭐️ 9.0/10
3. [OpenAI 终止向 Cursor 提供模型，停服日期定为 2026 年 11 月](#item-3) ⭐️ 9.0/10
4. [Htmx 4.0 发布，带来新功能与更新](#item-4) ⭐️ 8.0/10
5. [美国将意大利隐私托管服务商 Autistici Inventati 列为恐怖实体](#item-5) ⭐️ 8.0/10
6. [AI 与补丁分析将漏洞传闻转化为可利用漏洞](#item-6) ⭐️ 8.0/10
7. [Luanti 因 AI 生成的无理 DMCA 通知被 Google Play 下架](#item-7) ⭐️ 8.0/10
8. [微型潜在流变换器在 RP2350 微控制器上运行](#item-8) ⭐️ 8.0/10
9. [长鑫科技 2026 年上半年实现扭亏为盈爆发式增长](#item-9) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [腾讯混元发布 Hy4 preview，盲测得分略胜 GLM-5.3 与 Kimi K3](https://mp.weixin.qq.com/s/ymr3X878B8oa2XP15CH8TQ) ⭐️ 9.0/10

2026 年 8 月 28 日，腾讯发布并开源了 Hy4 preview，这是一款混合专家（MoE）大语言模型，总参数量 770B，活跃参数 49B，上下文窗口达 1M token。在 203 个工程任务的盲测中，Hy4 preview 得分 2.99，略胜 GLM 5.3（2.92）和 Kimi K3（2.94）。 此次发布加剧了开源 AI 模型领域的竞争，尤其是在长周期软件工程、文档办公和科学研究应用方面。该模型相比 GLM-5.3 和 Kimi K3 等其他领先的中国 MoE 模型展现出的竞争优势，表明腾讯在以极具性价比的 API 价格生产前沿规模 AI 方面的能力不断增强。 Hy4 preview 采用混合专家（MoE）架构，770B 总参数中每个 token 仅激活 49B 参数，在强大能力与推理效率之间取得平衡。其 API 定价为每 1M 输入 token 0.834 美元、每 1M 输出 token 2.501 美元，模型已在腾讯云、HuggingFace、GitHub、ModelScope 和 OpenRouter 等平台上线。

telegram · zaihuapd · 8月28日 06:11

**背景**: 混合专家（MoE）是一种在推理过程中仅稀疏激活模型总参数子集的架构，使得模型能够扩大总参数量以获得更强能力，同时保持较低的活跃参数以提升计算效率。这种总参数与活跃参数的区分在近期的中国 MoE 模型中很常见，例如 DeepSeek 的 671B/37B 和 GLM-5.2 的 744B/40B 配置。软件工程任务中的盲测旨在通过让模型完成真实编程挑战、且评估者不知晓输出来自哪个模型的方式，来减少评估偏差。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tencent.com/tencent-releases-and-open-sources-tencent-hy4-preview/">Tencent Releases and Open-Sources Tencent Hy4 preview - Tencent</a></li>
<li><a href="https://huggingface.co/tencent/Hy4-preview">tencent/Hy4-preview · Hugging Face</a></li>
<li><a href="https://latenteast.com/insights/moe-total-vs-active-parameters">MoE Total vs Active Parameters , Explained | The Latent East</a></li>

</ul>
</details>

**标签**: `#AI/ML`, `#Large Language Models`, `#Open Source`, `#Tencent`, `#Software Engineering`

---

<a id="item-2"></a>
## [智谱 AI 开源 GLM-5.3，主打智能体编程与网络防御](http://z.ai/) ⭐️ 9.0/10

智谱 AI 发布了开源模型 GLM-5.3，该模型与 GLM-5.2 共用同一基础模型，全部提升来自后训练，主打智能体编程与网络防御场景。该模型在 Terminal Bench 2.1 上得分 88.2，在 DeepSWE 上得分 66.9，在复杂编程和长周期任务上表现显著提升。 此次发布证明仅通过后训练即可在智能体编程能力上取得大幅提升，为开源社区提供了一个强大的复杂软件工程任务模型。其自定义许可证还确立了新的商业框架，允许个人和中小企业免费使用，但要求提供模型即服务的大型企业通过安全审查。 GLM-5.3 采用自定义 GLM-5.3 许可证，连续 12 个月营收超 100 亿美元且对外提供模型即服务的公司须先通过 Z.AI 安全审查。该模型权重已开放下载、运行和定制，相比 GLM-5.2 的全部性能提升均来自后训练而非架构变更。

telegram · zaihuapd · 8月28日 15:32

**背景**: 智能体编程是一种新兴范式，基于大语言模型的系统能够自主规划、执行和优化多步骤编程任务，使用工具和终端环境完成工作。Terminal Bench 2.1 用于评估智能体在终端环境中的表现，而 DeepSWE 是一个无污染基准测试，旨在测试前沿编程智能体处理原创长周期软件工程任务的能力。这些基准测试对于衡量 AI 模型处理需要持续推理和工具使用的复杂多步骤编程工作流至关重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tbench.ai/benchmarks/terminal-bench-2-1">Terminal-Bench 2.1 benchmark</a></li>
<li><a href="https://deepswe.datacurve.ai/">DeepSWE measures frontier coding agents on original, long-horizon...</a></li>
<li><a href="https://arxiv.org/html/2508.11126v1">AI Agentic Programming : A Survey of Techniques, Challenges, and...</a></li>

</ul>
</details>

**社区讨论**: 用户称赞 GLM-5.3 是一个强大的开源权重模型，比同类替代品更易运行，有评论者将其与 Opus 4.8 相媲美，并指出它能解决 DS4Flash 等其他模型无法处理的难题。一个值得关注的担忧是 token 效率问题，据报道 Qwen3.8 和 GLM 5.2 等中国模型的过度思考程度是 Opus 和 GPT 模型的 3-4 倍，不过用户对 GLM-5.3 在此比率上的改进抱有期望。

**标签**: `#AI Models`, `#Open Source`, `#Agentic Programming`, `#Cybersecurity`, `#Zhipu AI`

---

<a id="item-3"></a>
## [OpenAI 终止向 Cursor 提供模型，停服日期定为 2026 年 11 月](https://openai.com/index/our-decision-on-cursor-following-its-acquisition-by-spacex/) ⭐️ 9.0/10

OpenAI 宣布将终止与 Cursor 的模型供应合同，建议停服日期为 2026 年 11 月 12 日，此举发生在 SpaceX 收购 Cursor 之后。OpenAI 称无法确信 SpaceX 会遵守服务条款，理由是马斯克旗下公司（包括 Twitter 和 xAI）有违约记录。 这一终止决定打破了近四年的合作关系，迫使年收入超过 30 亿美元的主要 AI 编程工具 Cursor 为其庞大的开发者用户群寻找替代模型提供商。这也凸显了 OpenAI 与马斯克不断扩张的科技帝国之间日益加剧的企业冲突，可能重塑 AI 编程工具的竞争格局。 OpenAI 与 Cursor 现有合同中包含控制权变更条款，允许在最大通知期内终止合作，OpenAI 现正行使该权利。OpenAI 特别提到 xAI 今年早些时候在宣誓下承认违反 OpenAI 服务条款，以及 Twitter 收购后的违约行为，作为其决定的依据。

telegram · zaihuapd · 8月29日 02:24

**背景**: Cursor 是一款基于 Visual Studio Code 分叉开发的 AI 辅助集成开发环境（IDE），由 Anysphere 公司于 2022 年创立。这家位于旧金山的公司估值达 293 亿美元，于 2026 年 8 月被 SpaceXAI 收购成为全资子公司。OpenAI 与 Cursor 此前已合作近四年，通过定制协议允许 Cursor 在其编程平台中集成 OpenAI 模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cursor_(code_editor)">Cursor (code editor)</a></li>
<li><a href="https://cursor.com/">AI Coding Agent for Building Ambitious Software | Cursor</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#Cursor`, `#SpaceX`, `#AI Tools`, `#Industry News`

---

<a id="item-4"></a>
## [Htmx 4.0 发布，带来新功能与更新](https://four.htmx.org/announcements/2026-08-28-htmx-4.0.0-is-released) ⭐️ 8.0/10

Htmx 4.0 已正式发布，为这个基于超媒体驱动的 JavaScript 库引入了新功能和更新。其中值得注意的新增功能包括 `hx-alpine-compat` 属性，该属性用于平滑 htmx 与 Alpine.js 之间的兼容性问题。 作为挑战主流单页应用（SPA）复杂性的库的重大版本发布，htmx 4.0 进一步巩固了向更简单、基于超媒体驱动的 Web 开发趋势。它为开发者提供了一种轻量级的替代方案，将传统多页应用（MPA）的简单性与 SPA 的响应速度相结合，对前端架构选择产生了重大影响。 该库使用以 `hx-` 为前缀的自定义 HTML 属性来触发 AJAX 请求并直接从标记中更新 DOM 的部分内容，从而减少对大量 JavaScript 代码的需求。新增的 `hx-alpine-compat` 功能专门解决与 Alpine.js 的集成摩擦，尽管一些开发者指出，像 alpine-ajax.js 这样的替代库可以以更小的体积提供类似的功能。

hackernews · rmsaksida · 8月28日 13:28 · [社区讨论](https://news.ycombinator.com/item?id=49478178)

**背景**: Htmx 是一个旨在“将 HTML 完成为超文本”的 JavaScript 库，它允许开发者通过 HTML 属性直接访问现代浏览器功能，而无需编写 JavaScript。它支持超媒体驱动应用（HDA）架构，这是一种将传统服务器端渲染的简单性与通常与 SPA 相关的改善用户体验相结合的方法。通过利用被称为 HATEOAS 的 REST 约束，服务器通过链接和表单控制 UI 流程，使 htmx 能够动态获取和交换 HTML 片段。这种理念引起了那些寻求从现代前端框架的繁重工具和构建复杂性中解脱出来的开发者的共鸣。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Htmx">htmx - Wikipedia</a></li>
<li><a href="https://htmx.org/essays/hypermedia-driven-applications/">htmx ~ Hypermedia - Driven Applications</a></li>

</ul>
</details>

**社区讨论**: 社区的回应大多是积极的，许多用户称赞 htmx 为 Web 开发带来了乐趣和简单性，经常将它与 Go 和 SQLite 搭配使用。然而，一个值得注意的反对观点强调，对于习惯于分离架构的开发者来说，htmx 可能会使事情变得更加困难，因为它要求在后端将表示层关注点与业务逻辑混合在一起。此外，一些用户指出了像 alpine-ajax.js 这样的替代方案，供那些寻求更小体积解决方案的人使用。

**标签**: `#htmx`, `#frontend`, `#javascript`, `#hypermedia`, `#web-development`

---

<a id="item-5"></a>
## [美国将意大利隐私托管服务商 Autistici Inventati 列为恐怖实体](https://www.inventati.org/) ⭐️ 8.0/10

美国政府已对意大利托管服务商 Autistici/Inventati（A/I）实施制裁，将该组织——运营 noblogs.org 及其他隐私基础设施的机构——列为全球恐怖实体。这标志着针对为活动人士和基层社区提供服务的基础设施提供商的前所未有的升级。 此举将提供隐私保护通信基础设施与支持恐怖主义混为一谈，开创了一个危险的先例，可能对所有注重隐私的服务提供商产生寒蝉效应。这引发了紧迫的问题：如果不良行为者使用 Signal、Monero、I2P 和 Tor 等工具，这些工具的开发者和用户是否也会面临类似的定性。 Autistici/Inventati 自 21 世纪初以来一直为活动人士和社会运动提供免费托管、电子邮件和博客服务，其根源可追溯到 2001 年热那亚 G8 峰会抗议活动。制裁实施后，autistici.org 和 noblogs.org 均出现部分或全部服务中断，使用户和研究人员难以独立核实具体指控——包括未经证实的与 PKK 相关的托管说法。

hackernews · exiguus · 8月28日 12:58 · [社区讨论](https://news.ycombinator.com/item?id=49477854)

**背景**: Autistici/Inventati（A/I）是一个意大利集体，自 21 世纪初以来一直为活动人士、基层组织和社会运动提供免费的互联网服务，包括网站托管、电子邮件、VPN 和博客平台。他们的 noblogs.org 平台为众多与无政府主义和激进左翼社区相关的书展、广播节目和文化项目托管网站。该集体与反全球化运动有关，其参与者曾在 2001 年热那亚 G8 峰会抗议等活动期间参与建设独立媒体基础设施。美国的定性似乎源于指控 A/I 托管了与 PKK（库尔德工人党）相关的内容，PKK 被美国和其他几个国家列为恐怖组织。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://crimethinc.com/2026/08/27/us-government-designates-host-of-noblogsorg-a-global-terrorist">US Government Designates Host of NoBlogs . org a "Global Terrorist"</a></li>
<li><a href="https://www.autistici.org/services/website">autistici.org - Website hosting</a></li>
<li><a href="https://news.ycombinator.com/item?id=49451343">US sanctions Italian hosting provider Autistici Inventati | Hacker News</a></li>

</ul>
</details>

**社区讨论**: 社区讨论跨越多个 Hacker News 帖子的数百条评论，反映了对这一先例对隐私基础设施提供商所设影响的深切担忧。用户 iamnothere 提出了关键问题：这种逻辑是否会延伸到 I2P、Monero、Signal 和 Tox 等工具的开发者和用户。其他评论者指出，由于被制裁的网站现已部分或完全离线，难以核实具体指控，一些人质疑是否存在任何与 PKK 的直接联系。一些用户提供了 A/I 在 2001 年热那亚 G8 抗议期间起源的历史背景，而另一些人则对该集体的实际活动和目的表示困惑。

**标签**: `#privacy`, `#civil-liberties`, `#infrastructure`, `#censorship`, `#policy`

---

<a id="item-6"></a>
## [AI 与补丁分析将漏洞传闻转化为可利用漏洞](https://anil.recoil.org/notes/rumour-is-the-exploit) ⭐️ 8.0/10

文章强调了 AI 工具与补丁比对技术的结合如何使漏洞发现过程民主化和规模化，使得仅凭传闻或微小的补丁说明就能逆向工程出可用的漏洞利用代码。这导致开源维护者收到的安全报告数量激增，一些项目在一个月内收到的漏洞披露比过去十年还要多。 这种范式转变从根本上改变了开源软件的威胁格局，攻击者现在可以利用公开的补丁信息大规模快速生成漏洞利用代码。这给通常资源不足的维护者带来了巨大的分类和修复负担，同时也暴露了发现漏洞的能力与组织实际修复漏洞的意愿之间的巨大差距。 补丁比对涉及比较软件的不同版本以识别安全修复，然后可以将其逆向工程为概念验证漏洞利用。虽然这种做法并不新鲜，但 LLM 大幅降低了准入门槛，导致大量自动化或半自动化报告涌入，这些报告通常包含有效漏洞，但可能缺乏适当的上下文或严重性评估。

hackernews · avsm · 8月28日 15:58 · [社区讨论](https://news.ycombinator.com/item?id=49480466)

**背景**: 补丁比对，也称为补丁分析，是漏洞研究中的一项长期技术，分析师通过比较软件的补丁版本和漏洞版本来识别修复的内容。通过理解漏洞原理，研究人员通常可以制作针对未修补系统的漏洞利用代码。大型语言模型（LLM）现在已经自动化了大部分分析工作，使技能水平相对较低的人员也能执行以前需要大量专业知识的任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.zerohuntlabs.com/exploitation/finding-bugs-via-patch-diffing">Finding Bugs via Patch Diffing | zerohuntlabs</a></li>
<li><a href="https://www.algomox.com/resources/blog/real_time_patch_vulnerability_analysis/">Algomox Blog | Real-Time Patch Vulnerability Analysis with...</a></li>

</ul>
</details>

**社区讨论**: 像 rclone 开发者这样的开源维护者报告称被大量安全披露所淹没，虽然有效问题的命中率很高，但时间成本极其严重。其他评论者强调，虽然 AI 使发现和修复漏洞变得更容易，但组织惯性和缺乏部署修复的意愿仍然是最大的瓶颈。一些研究人员指出，虽然核心技术并不新鲜，但 LLM 使其民主化，从而能够大规模利用低价值目标。

**标签**: `#cybersecurity`, `#LLMs`, `#open-source`, `#vulnerability-research`, `#AI`

---

<a id="item-7"></a>
## [Luanti 因 AI 生成的无理 DMCA 通知被 Google Play 下架](https://blog.luanti.org/2026/08/27/luanti-dmca-tracer-ai/) ⭐️ 8.0/10

开源体素游戏 Luanti 被从 Google Play 下架，原因是自动化品牌保护服务 Tracer AI 对其提交了一份毫无根据的 DMCA 版权下架通知。这并非孤立事件，Tracer AI 曾于 2023 年对 Luanti 提交过类似通知，最近还针对另一款名为 Allumeria 的独立体素游戏采取了相同行动。 这一事件暴露了开源项目在面对自动化 DMCA 滥用时的系统性脆弱性——AI 驱动的下架系统可以中断合法软件的分发，而提交者却无需承担任何实质后果。它凸显了版权执行机制改革的迫切需求，包括对轻率索赔实施处罚，以及加强对部署自动化下架机器人的公司的问责。 Tracer AI 使用 AI 代理进行自动化侵权检测，但其系统未能将 Luanti 原创的开源体素素材与受版权保护的材料区分开来。社区成员还注意到，Tracer AI 在 Luanti 通知中声称瓦努阿图管辖权，而在其他近期索赔中却声称美国管辖权，这引发了对潜在欺诈行为的质疑。

hackernews · miniBill · 8月28日 06:33 · [社区讨论](https://news.ycombinator.com/item?id=49475079)

**背景**: Luanti（前身为 Minetest）是一款免费的开源体素游戏引擎，由 Perttu Ahola 于 2010 年创建，支持多个平台。DMCA（数字千年版权法）下架流程是一种法律机制，允许版权持有者要求网站和平台移除涉嫌侵权的内容。根据现行 DMCA 规则，Google Play 等平台在收到通知后通常会立即下架内容以避免法律责任，将举证负担转嫁给被指控方，需要其提交反通知才能恢复内容。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Luanti">Luanti - Wikipedia</a></li>
<li><a href="https://copyrightalliance.org/faqs/what-is-dmca-takedown-notice-process/">What's the DMCA Takedown Notice Process | Copyright Alliance</a></li>
<li><a href="https://www.techdirt.com/company/tracer-ai/">Posts about tracer . ai written by Dark Helmet</a></li>

</ul>
</details>

**社区讨论**: 社区对 DMCA 系统表达了强烈的不满，用户呼吁对提交轻率下架通知的行为实施处罚和金融保证金制度。评论者还指出 Tracer AI 不一致的管辖权声明可能涉嫌欺诈，一位用户建议微软应解雇负责发送这些重复通知的高级律师，以挽回与 Minecraft 相关的好感。

**标签**: `#DMCA`, `#Luanti`, `#Copyright Abuse`, `#Open Source`, `#Tracer AI`

---

<a id="item-8"></a>
## [微型潜在流变换器在 RP2350 微控制器上运行](https://www.reddit.com/r/MachineLearning/comments/1w10tax/i_implemented_a_very_tiny_image_generation_model/) ⭐️ 8.0/10

一位开发者在 RP2350 微控制器上实现了一个拥有 240 万至 400 万参数的潜在流变换器，能够在约 20 秒内生成 128x128 分辨率的人脸图像。该实现利用了 int8 量化、DMA 权重流式传输以及 ReLU² 稀疏性优化，完全在边缘设备上完成推理。 这一成就表明，像流变换器这样复杂的生成式 AI 模型经过压缩和优化后，可以在资源高度受限的微控制器上运行，拓展了边缘 AI 的边界。它为极限模型优化技术提供了宝贵见解，有望在低功耗设备上实现离线且保护隐私的图像生成。 该模型采用 12 层变换器结构，使用 AdaLN-Zero 进行条件控制，并支持无分类器引导（CFG）以提升图像质量。推理引擎通过 DMA 在计算上一层的同时从闪存中流式传输权重，同时 ReLU² 激活函数增加稀疏性以跳过不必要的计算。

reddit · r/MachineLearning · /u/cpldcpu · 8月28日 19:48

**背景**: RP2350 是由树莓派设计的低成本双核微控制器，其 RAM 和闪存容量十分有限。潜在流变换器是一种生成模型，它在压缩的潜在空间中利用流匹配来高效生成数据。AdaLN-Zero 是一种条件控制机制，它将变换器层初始化为零，从而在扩散模型和基于流的模型中稳定训练过程。DMA（直接内存访问）允许硬件外设在内存和设备之间传输数据而无需 CPU 干预，这对于克服微控制器上的内存带宽瓶颈至关重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2505.14513">Abstract page for arXiv paper 2505.14513: Latent Flow Transformer</a></li>
<li><a href="https://www.emergentmind.com/topics/adaln-zero-conditioning">AdaLN - Zero Conditioning in Deep Models</a></li>
<li><a href="https://apxml.com/courses/advanced-diffusion-architectures/chapter-3-transformer-diffusion-models/dit-conditioning">Conditioning Mechanisms in Diffusion Transformers</a></li>

</ul>
</details>

**标签**: `#edge-ai`, `#microcontroller`, `#image-generation`, `#model-optimization`, `#flow-transformer`

---

<a id="item-9"></a>
## [长鑫科技 2026 年上半年实现扭亏为盈爆发式增长](https://t.me/zaihuapd/43468) ⭐️ 8.0/10

8 月 28 日晚，长鑫科技披露 2026 年上半年财报，实现营业收入 1503.1 亿元，同比增长 873.64%；归母净利润 776.05 亿元，上年同期亏损 23.32 亿元。经营活动产生的现金流量净额为 1311.56 亿元，同比增长 2985.64%，上半年主营业务毛利率达 84.84%。 长鑫科技作为中国领先的 DRAM 制造商及全球第四大厂商，其爆发式财务表现标志着中国半导体存储行业的重大突破。这一业绩反映了公司深度受益于存储芯片涨价周期及 AI 驱动的需求增长，正在重塑全球存储市场的竞争格局。 分季度来看，第一季度归母净利润 247.62 亿元，第二季度归母净利润 528.43 亿元，环比增长 113%，基本每股收益 1.2893 元。公司于 2026 年 7 月 27 日正式登陆上交所科创板（股票代码：688825），拟募资 295 亿元，为科创板开板以来募资规模第二大的 IPO。

telegram · zaihuapd · 8月28日 11:34

**背景**: 长鑫科技是中国领先的 DRAM 存储芯片制造商，而 DRAM 和 NAND Flash 在全球存储市场中占据主导地位，其中 DRAM 占比约 56.3%。存储芯片行业具有强周期性，被视为半导体行业荣枯的风向标。近期 AI 推动了对 HBM 和企业级 SSD 的强劲需求，甚至导致 DDR4 等传统存储产品出现持续短缺，市场赢家与输家的差距显著拉大。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnr.cn/ah/ahtt/20260727/t20260727_527732482.shtml">央广财评丨从 长 鑫 上市，看安徽“日新”之变_央广网</a></li>
<li><a href="https://www.yilantop.com/article/26713">踩着历史级风口IPO， 长 鑫 科 技 逆袭背后的隐忧_壹览商业</a></li>
<li><a href="https://wallstreetcn.com/articles/3763830">存 储 芯 片 “贫富差距”拉大，赢家输家到底怎么选</a></li>

</ul>
</details>

**标签**: `#长鑫科技`, `#半导体`, `#存储芯片`, `#财报`, `#扭亏为盈`

---
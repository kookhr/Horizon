---
layout: default
title: "Horizon Summary: 2026-07-12 (ZH)"
date: 2026-07-12
lang: zh
---

> 从 30 条内容中筛选出 11 条重要资讯。

---

1. [GPT-5.6 Sol Ultra 不到一小时证明 50 年历史的循环双覆盖猜想](#item-1) ⭐️ 10.0/10
2. [研究员称 xAI Grok CLI 默认上传整个代码库及密钥文件](#item-2) ⭐️ 9.0/10
3. [菲尔兹奖得主陶哲轩探索用 LLM 编程代理构建数学可视化](#item-3) ⭐️ 8.0/10
4. [带状疱疹疫苗可能降低痴呆风险，引发混杂因素讨论](#item-4) ⭐️ 8.0/10
5. [高位截瘫患者借助 NEO 脑机接口系统重新握笔](#item-5) ⭐️ 8.0/10
6. [Claude Code 与 OpenCode 的 Token 开销分析引发讨论](#item-6) ⭐️ 7.0/10
7. [George Hotz：LLM 生产力很高，但前沿实验室估值过高](#item-7) ⭐️ 7.0/10
8. [Fabien Sanglard 撰文称手工编码正因 LLM 而走向消亡](#item-8) ⭐️ 7.0/10
9. [Ghostel.el：基于 libghostty-vt 的 Emacs 终端模拟器](#item-9) ⭐️ 7.0/10
10. [Zer0Fit：将谷歌 TabFM 和 TimesFM 封装为 MCP 服务器的零样本机器学习工具](#item-10) ⭐️ 7.0/10
11. [Codex 负责人 Tibo 分享通过 CLIProxyAPI 将 GPT-5.6 Sol 接入 Claude Code 的指南](#item-11) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [GPT-5.6 Sol Ultra 不到一小时证明 50 年历史的循环双覆盖猜想](https://www.qbitai.com/2026/07/447873.html) ⭐️ 10.0/10

GPT-5.6 Sol Ultra 在不到 1 小时内证明了存在约半个世纪的著名图论难题——循环双覆盖猜想，并生成了一份 3 页的 PDF 证明。模型通过 64 个并行子 agent 将问题转化为有限域上的边标号和线性方程组问题，OpenAI 同时公布了约 700 个英文字符的完整 Prompt，详细说明了验证方法。 这展示了 AI 辅助数学研究的范式转变能力，表明大语言模型可以通过并行多 agent 架构攻克长期未解的公开猜想。Prompt 方法论的公开提供了可复现性，并为自动定理证明设定了新标杆，有望加速纯数学和形式化验证领域的进展。 循环双覆盖猜想指出，每个无桥图都可以被一组圈覆盖，使得每条边恰好出现两次。该证明方法在有限域上为每条边分配两个标签，使相同标签的边构成圈，从而将问题转化为求解线性方程组。Prompt 不规定固定解题步骤，而是明确验收标准、定义、边界条件和失败情形，要求动态分配子 agent 并设置独立审查，以检查是否偷换定义或遗漏情况。

telegram · zaihuapd · 7月12日 03:49

**背景**: 循环双覆盖猜想是图论中最著名的未解难题之一，由 Szekeres 和 Seymour 于 20 世纪 70 年代独立提出。该猜想关注无桥图——即不存在删除后会使图断开的桥边的图——断言此类图存在一组圈，使每条边恰好被覆盖两次。该猜想与图分解、代数图论以及无处零流等深层领域密切相关。尽管经过数十年的努力，一般性证明一直未能完成，因此成为自动定理证明方法的重要目标。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cycle_double_cover">Cycle double cover - Wikipedia</a></li>
<li><a href="https://www.sfu.ca/~mohar/Problems/CYCLECOV.HTM">cyclecov</a></li>
<li><a href="https://www.emergentmind.com/topics/cycle-double-cover-cdc-conjecture">Cycle Double Cover Conjecture</a></li>

</ul>
</details>

**标签**: `#AI`, `#Mathematics`, `#Theorem Proving`, `#GPT-5`, `#Graph Theory`

---

<a id="item-2"></a>
## [研究员称 xAI Grok CLI 默认上传整个代码库及密钥文件](https://gist.github.com/cereblab/dc9a40bc26120f4540e4e09b75ffb547) ⭐️ 9.0/10

安全研究人员发现 xAI 的 Grok Build CLI（版本 0.2.93）会自动将整个代码仓库（包括 .env 等密钥文件）上传至 xAI 服务器和 Google Cloud Storage。即使被明确指令不要打开某些文件，其内容仍可在上传的压缩包中完整恢复，且关闭设置中的"改进模型"开关也无法阻止上传。 这代表了 xAI 官方开发者工具中一个严重的安全和隐私漏洞，因为它在没有任何有效退出机制的情况下静默泄露 API 密钥和凭证等敏感数据。这对使用 xAI 工具的开发者和企业具有重大影响，凸显了 AI 辅助开发工具中严重的信任与安全问题。 该工具通过两个渠道传输数据：工具读取的文件内容被嵌入模型对话请求并打包上传至 Google Cloud Storage，同时整个代码仓库以 git bundle 形式上传。在 12 GB 仓库的测试中，超过 5 GiB 的数据成功上传且无存储端拒绝；研究者强调仅证明了数据传输与存储行为，未证明 xAI 使用这些数据进行模型训练。

telegram · zaihuapd · 7月12日 04:19

**背景**: Grok Build 是 xAI 推出的官方命令行界面（CLI）和编程代理，由 Grok 4.5 模型驱动，旨在将 AI 辅助编程能力引入开发者的终端。git bundle 是 Git 的一项功能，可将仓库数据（包括 heads 和 tags 等引用）打包为单个文件，用于在无需活跃服务器连接的情况下进行离线传输。这项研究揭示了直接与本地代码库交互的 AI 编程助手如何无意或有意地将敏感开发产物暴露给远程服务器。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://x.ai/cli">Grok Build | SpaceXAI</a></li>
<li><a href="https://docs.x.ai/build/overview">Grok Build | SpaceXAI Docs</a></li>
<li><a href="https://git-scm.com/docs/git-bundle">Git - git - bundle Documentation</a></li>

</ul>
</details>

**标签**: `#security`, `#xAI`, `#Grok`, `#privacy`, `#developer-tools`

---

<a id="item-3"></a>
## [菲尔兹奖得主陶哲轩探索用 LLM 编程代理构建数学可视化](https://terrytao.wordpress.com/2026/07/11/old-and-new-apps-via-modern-coding-agents/) ⭐️ 8.0/10

菲尔兹奖得主陶哲轩于 2026 年 7 月 11 日发表博客文章，详细分享了他使用现代 LLM 编程代理为学术论文构建交互式数学可视化和应用补充材料的实践经验。他给出了审慎的评价，指出在非关键性辅助工具方面确实能提升生产力，同时当产出不涉及研究的核心任务时，其下行风险也是可接受的。 陶哲轩的采用传递了一个更广泛的趋势信号：传统软件工程之外的领域专家正在利用编程代理来满足评论者所说的学术界和教育界对软件的

hackernews · subset · 7月12日 11:09 · [社区讨论](https://news.ycombinator.com/item?id=48880170)

**标签**: `#llm`, `#coding-agents`, `#academic-research`, `#visualization`, `#terence-tao`

---

<a id="item-4"></a>
## [带状疱疹疫苗可能降低痴呆风险，引发混杂因素讨论](https://www.economist.com/leaders/2026/07/09/a-no-brainer-for-protecting-your-brain) ⭐️ 8.0/10

斯坦福大学利用英国的自然实验进行的一项研究发现，带状疱疹疫苗将患痴呆的风险降低了约 20%，这一保护效应在多项数据分析中均能观察到。该研究于 2025 年 12 月发表在《Cell》期刊上，还发现疫苗接种减少了轻度认知障碍和因痴呆导致的死亡，表明疫苗可能在整个临床病程中减缓疾病进展。 痴呆影响全球数千万人，且几乎没有可用的疾病修饰疗法，因此即使是已获批疫苗带来的适度保护效应也可能具有巨大的公共卫生意义。这一发现表明，针对带状疱疹的疫苗接种可能成为一种罕见且可及的干预措施，既能预防一种痛苦的急性疾病，又可能减缓认知衰退。 英国研究利用了一个自然实验，即带状疱疹疫苗的接种资格基于严格的年龄截止线，从而在阈值上下形成了可比的对照组。然而，一个关键的方法论批评认为该发现可能是虚假的：接种者因带状疱疹住院的可能性更低，这意味着医院就诊次数更少，因此被附带诊断出痴呆的概率也更低，这可能解释了所观察到的效应，而非真正的生物学保护机制。

hackernews · saikatsg · 7月12日 15:23 · [社区讨论](https://news.ycombinator.com/item?id=48881874)

**背景**: 带状疱疹由水痘-带状疱疹病毒再激活引起，该病毒在初次感染水痘后潜伏于体内。目前最广泛使用的带状疱疹疫苗是 Shingrix，一种需要接种两剂的重组带状疱疹疫苗。痴呆，尤其是阿尔茨海默病，涉及进行性神经退行性病变，目前尚无已知治愈方法，而越来越多的证据表明病毒感染和免疫系统功能可能在认知衰退中发挥作用。英国国家医疗服务体系（NHS）在引入带状疱疹疫苗时采用了基于年龄的接种资格截止线，形成了研究人员所称的自然实验，使得阈值上下两组人群的健康结果可以被比较。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cidrap.umn.edu/varicella/shingles-vaccine-may-prevent-delay-or-slow-dementia-process">Shingles vaccine may prevent, delay, or slow dementia process | CIDRAP</a></li>
<li><a href="https://med.stanford.edu/news/all-news/2025/03/shingles-vaccination-dementia.html">For those living with dementia, new study suggests shingles vaccine could slow the disease</a></li>
<li><a href="https://www.cell.com/cell/fulltext/S0092-8674(25)01256-5">The effect of shingles vaccination at different stages of the dementia disease course: Cell</a></li>

</ul>
</details>

**社区讨论**: 社区讨论质量很高，在根据研究结果采取实际行动的人和提出方法论质疑的人之间存在分歧。一位有阿尔茨海默病遗传倾向的 40 多岁用户表示计划自费（约 500 美元）接种 Shingrix，而不愿等待数年通过保险获得资格。一个关键的反驳观点获得了关注，引用了一个演示文稿，认为该发现是虚假的，因为接种者因避免了带状疱疹而减少了医院就诊次数，从而减少了被附带诊断出痴呆的机会。另一位用户链接了 Eric Topol 通讯中英国研究令人瞩目的资格截止线图表，而其他人则强调痴呆可能有数十个风险因素，带状疱疹只是其中恰好有因果治疗手段的一个。

**标签**: `#health`, `#dementia`, `#vaccines`, `#public-health`, `#research`

---

<a id="item-5"></a>
## [高位截瘫患者借助 NEO 脑机接口系统重新握笔](https://www.zaobao.com.sg/news/china/story20260712-9199066) ⭐️ 8.0/10

中国 36 岁高位截瘫患者董辉在植入硬币大小的无线 NEO 脑机接口设备后，经过训练重新完成了抓握和书写等动作。由博睿康与清华大学共同研发的 NEO 半侵入式脑机接口系统于 2026 年 3 月 13 日获中国国家药监局批准上市，已完成 36 例临床手术。 这标志着脑机接口商业化的重要里程碑，NEO 成为中国首批获批临床应用的脑机接口系统之一，直接与 Neuralink 等侵入式方案竞争。成功的实际应用表明，半侵入式脑机接口技术能够为脊髓损伤患者恢复有意义的运动功能，有望变革康复医学领域。 NEO 采用半侵入式方案，电极放置在颅骨上头皮下，避免与脑组织直接接触，同时仍能实时传输脑电数据。该系统获批用于因颈段脊髓损伤导致四肢瘫痪、手指无法抓握的成年患者，是一个长期稳定可靠的双向闭环脑机接口系统。

telegram · zaihuapd · 7月12日 14:39

**背景**: 脑机接口（BCI）大致分为三类：侵入式（电极直接植入脑组织）、非侵入式（如脑电帽等外部传感器）和半侵入式（电极放置在颅骨与头皮之间）。NEO 系统代表半侵入式技术路线，由博睿康与清华大学洪波教授领导的生物医学工程团队合作开发。NEO 曾被 Nature 选为 2025 年值得关注的脑机接口重要进展之一，凸显了其在全球脑机接口竞赛中的重要地位。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.shine.cn/news/metro/2412106729/">Brain - computer interface technology helps paralyzed... - SHINE News</a></li>
<li><a href="https://interestingengineering.com/innovation/chinas-neo-brain-implant-trials-2024">China preps semi - invasive brain tech trials to take on Neuralink</a></li>
<li><a href="http://neuracle.cn/newsinfo/7898209.html?trk=article-ssr-frontend-pulse_little-text-block">Nature重磅： NEO 微创 脑 机 接 口 系统入选2025...</a></li>

</ul>
</details>

**标签**: `#brain-computer interface`, `#neuroengineering`, `#medical technology`, `#BCI`, `#rehabilitation`

---

<a id="item-6"></a>
## [Claude Code 与 OpenCode 的 Token 开销分析引发讨论](https://systima.ai/blog/claude-code-vs-opencode-token-overhead) ⭐️ 7.0/10

Systima.ai 的一项实证分析发现，Claude Code 在读取用户提示词之前会发送约 33,000 个 token，而 OpenCode 仅发送 7,000 个，揭示了两者在系统开销和缓存管理效率上的巨大差异。该研究通过在智能编程工具与 Anthropic 的 API 端点之间添加日志记录来捕获所有请求数据。 这一发现很重要，因为 token 消耗直接影响使用 AI 编程助手的开发者的成本和速度，4-5 倍的开销差异对于重度用户来说可能意味着巨大的成本差距。这场讨论还引发了更广泛的问题：智能编程工具是否正在变得不必要地消耗大量 token，这背后可能存在商业激励或子代理效率低下的因素。 该研究有一个值得注意的局限性：它主要衡量的是 token 开销而非任务结果，促使作者计划更新研究，包括更深入的任务、定性结果比较以及输入输出的完整复现。社区成员还指出 Claude Code 中的子代理会快速消耗预算，一位用户报告称单个任务同时启动了 7 个子代理。

hackernews · systima · 7月12日 18:25 · [社区讨论](https://news.ycombinator.com/item?id=48883275)

**背景**: Claude Code 是 Anthropic 的智能编程工具，运行在终端中，通过自然语言命令理解代码库并协助编程任务。OpenCode 是一个开源的 AI 编程代理替代方案，提供类似的自主编程能力。这两个工具都通过 API 调用与 AI 模型交互，其中 token 代表处理的文本单元；系统提示和缓存管理策略会显著影响在处理实际用户输入之前消耗多少 token。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/anthropics/claude-code">GitHub - anthropics/claude-code: Claude Code is an agentic coding tool that lives in your terminal, understands your codebase, and helps you code faster by executing routine tasks, explaining complex code, and handling git workflows - all through natural language commands. · GitHub</a></li>
<li><a href="https://www.stork.ai/blog/the-ai-coder-thats-replacing-claude">OpenCode : The Free Claude Code Alternative for AI Agents | Stork. AI</a></li>
<li><a href="https://www.deeplearning.ai/courses/claude-code-a-highly-agentic-coding-assistant">Claude Code: A Highly Agentic Coding Assistant - DeepLearning.AI</a></li>

</ul>
</details>

**社区讨论**: 社区讨论非常活跃，观点多样。一位用户认为子代理才是真正消耗 token 的元凶，单个任务启动了 7 个子代理并在完成前就耗尽了预算，另一位用户则暗示 Anthropic 故意多消耗 token 以获取更多利润并锁定订阅。一条有效的批评促使作者更新研究以加入基于结果的比较，多位用户还注意到了一个更广泛的趋势——即使是简单的请求也会触发过多的工具调用，即所谓的"token 通胀"。

**标签**: `#ai-coding-tools`, `#token-efficiency`, `#claude-code`, `#opencode`, `#developer-tools`

---

<a id="item-7"></a>
## [George Hotz：LLM 生产力很高，但前沿实验室估值过高](https://geohot.github.io//blog/jekyll/update/2026/07/12/i-love-llms.html) ⭐️ 7.0/10

George Hotz 发布了一篇博客文章，认为虽然 LLM 带来了巨大的生产力提升，但 OpenAI 和 Anthropic 等前沿 AI 实验室的估值过高，因为它们无法捕获其所创造的经济价值。他预测这一动态将引领一个由个人构建定制化、个性化软件的时代，而非依赖集中式平台。 这一论点通过平台经济学原理挑战了前沿实验室的万亿美元估值：创造价值并不等于能够捕获价值。如果 Hotz 是正确的，AI 行业的收入模型与实际的价值分配存在根本性错位，这可能重塑投资策略，并加速向开源和 homelab 软件开发的转变。 Hotz 的核心论点是，LLM 带来的生产力提升将被构建定制工具的终端用户和开发者所捕获，而非训练模型的实验室。他指出，当前的订阅定价（例如每月 100-200 美元）使前沿模型成为提升生产力的理所当然之选，但这也意味着实验室相对于其创造的价值定价过低，从而削弱了其长期收入潜力。

hackernews · therepanic · 7月12日 18:31 · [社区讨论](https://news.ycombinator.com/item?id=48883343)

**背景**: George Hotz 是 comma.ai 的创始人，也是一位知名黑客，最初因破解 iPhone 和 PlayStation 3 而声名鹊起。在平台经济学中，价值捕获是指创造者或平台保留其产品或服务所产生的经济盈余的能力。前沿实验室是指 OpenAI、Anthropic 和 Google DeepMind 等训练最先进 AI 模型的公司，它们通常基于对未来收入主导地位的预期而被估值数百亿或数千亿美元。

**社区讨论**: Hacker News 的讨论在很大程度上认同 Hotz 的核心论点，用户 SwellJoe 强调了关于实验室无法捕获其所创造价值的敏锐观察。用户 hamandcheese 指出，我们正在进入一个

**标签**: `#LLMs`, `#AI Economics`, `#Open Source`, `#Commentary`, `#Productivity`

---

<a id="item-8"></a>
## [Fabien Sanglard 撰文称手工编码正因 LLM 而走向消亡](https://fabiensanglard.net/extinct/index.html) ⭐️ 7.0/10

Fabien Sanglard 发表了一篇题为 "Don't you mean extinct?" 的文章，认为随着 LLM 接管日常编码任务，手工编写代码正在成为历史。文章断言，拒绝使用 LLM 的开发者将会落后，因为他们无法像使用 LLM 的开发者那样产出大量代码。 这篇文章引发了社区的大规模讨论（168 分，95 条评论），探讨 AI 对软件工程生产力和代码质量的真正影响。它提出了一个重要问题：产出量的增加是否意味着更好的软件，同时也触及了科技行业中熟练劳动力被贬值的更广泛担忧。 Sanglard 承认，虽然 LLM 加速了代码生成，但开发者阅读代码和理解架构的能力仍然重要，因此他会反复迭代 PR 以保持质量。社区成员对 "产出量" 的说法提出了质疑，指出在软件工程中，代码量很少是一个有意义的评估指标。

hackernews · zdw · 7月12日 15:17 · [社区讨论](https://news.ycombinator.com/item?id=48881830)

**背景**: GPT-4 和 Claude 等大型语言模型（LLM）越来越多地通过 GitHub Copilot 和 Cursor 等工具被集成到软件开发工作流中。这些工具可以生成样板代码、编写测试并辅助重构，引发了关于传统手工编码过程有多少将被自动化以及哪些技能对开发者仍然至关重要的持续讨论。

**社区讨论**: 社区在很大程度上对文章的前提提出了质疑，评论者质疑产出更多代码与产出高质量代码之间的价值。一位评论者将此与电影行业过度依赖 CGI 的现象进行了有见地的类比，指出在贬值实物特效 20 年后，现在出现了回归实物特效的趋势，因为实物特效时代的电影看起来更好。其他人则批评 "落后" 的说法过于激进，指出在软件工程中，代码量很少是一个有意义的评估指标。

**标签**: `#LLM`, `#Software Engineering`, `#AI Productivity`, `#Coding`, `#Industry Trends`

---

<a id="item-9"></a>
## [Ghostel.el：基于 libghostty-vt 的 Emacs 终端模拟器](https://dakra.github.io/ghostel/) ⭐️ 7.0/10

Ghostel.el 是一款新发布的 Emacs 终端模拟器，它使用了从 Ghostty 终端模拟器核心中提取的零依赖 C 语言库 libghostty-vt。与 vterm 和 eat 等现有 Emacs 终端选项相比，它提供了更好的性能、更可靠的输入处理以及更友好的 Elisp API。 这为 Emacs 用户提供了一个由 Ghostty 经过实际验证的核心支持的高性能终端模拟选项，有可能取代 vterm 成为许多用户的首选终端。它还展示了 libghostty-vt 作为可复用库的实际价值，能够为任何应用程序带来快速、准确的终端模拟功能。 libghostty-vt 是一个零依赖的 C 语言库，负责处理终端序列解析、状态管理和输入编码，不需要完整的终端 UI 甚至不需要 libc。从 vterm 切换过来的用户报告称在复杂 TUI 应用中性能明显提升，但仍存在一些粗糙之处，例如偶尔出现的终端清屏问题和冻结现象。

hackernews · signa11 · 7月12日 08:52 · [社区讨论](https://news.ycombinator.com/item?id=48879504)

**背景**: Ghostty 是由 Mitchell Hashimoto 创建的一款快速、跨平台的终端模拟器，采用 GPU 加速和平台原生 UI。该项目最近发布了 libghostty-vt 作为独立库，从 Ghostty 核心中提取，允许其他应用程序嵌入终端模拟功能而无需依赖完整的 Ghostty UI。Emacs 长期以来拥有 vterm 和 eat 等终端模拟器包，但它们各自在性能、兼容性和与 Emacs 独特输入处理模型的集成方面存在权衡。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mitchellh.com/writing/libghostty-is-coming">Libghostty Is Coming – Mitchell Hashimoto</a></li>
<li><a href="https://github.com/ghostty-org/ghostty">GitHub - ghostty-org/ghostty: Ghostty is a fast, feature ...</a></li>
<li><a href="https://ghostty.org/">Ghostty</a></li>

</ul>
</details>

**社区讨论**: 维护者 dakra 提供了有用的背景信息，包括与 vterm 和 eat 的功能对比，而从 vterm 切换过来的用户报告称性能和可靠性显著提升。社区成员提出了关于输入模式实际用法的疑问，并建议标题中应提及 Emacs，因为 Emacs 终端模拟器与独立终端模拟器是不同的概念。

**标签**: `#emacs`, `#terminal-emulator`, `#ghostty`, `#developer-tools`, `#open-source`

---

<a id="item-10"></a>
## [Zer0Fit：将谷歌 TabFM 和 TimesFM 封装为 MCP 服务器的零样本机器学习工具](https://www.reddit.com/r/MachineLearning/comments/1uue8cc/zer0fit_i_took_googles_new_tabfm_timesfm_ml/) ⭐️ 7.0/10

一位研究生开发了 Zer0Fit，这是一个 MCP 服务器，将谷歌最新发布的 TabFM 和 TimesFM 基础模型封装在单个 Docker 容器中，通过 Open WebUI、Claude Code 或 Codex 等 LLM 集成实现零样本预测、分类和回归任务。该工具需要约 16GB 显存，完全在本地支持 CUDA 的 NVIDIA GPU 上运行。 该项目将基于 Transformer 的机器学习基础模型与对话式 AI 界面连接起来，使用户能够执行以前需要构建、训练和调参的机器学习任务，而无需编写任何机器学习代码。它展示了一种实用的工作流程，LLM 可以通过 MCP 编排专门的机器学习模型，有望改变数据科学家和从业者处理表格数据和时间序列问题的方式。 Zer0Fit 基于 PyTorch，仅支持 CUDA，不支持 Mac，包含动态模型加载/卸载功能，TTL 设为 5 分钟以在空闲时释放显存。在经典数据集上测试，Iris 分类准确率达 94.7%，加州房价回归 R² 达 0.91；构建目标包括 DGX Spark（ARM 架构，CUDA 13）和 3090（AMD64 架构，CUDA 12.6）；目前支持 CSV 格式，XLS、XLSX、JSON 和 JSONL 格式即将支持。

reddit · r/MachineLearning · /u/Porespellar · 7月12日 12:32

**背景**: 谷歌发布了 TabFM 和 TimesFM，分别作为表格数据和时间序列预测的基础模型，将上下文学习（ICL）的概念应用于传统机器学习任务。TabFM 将表格预测构建为 ICL 问题，消除了手动模型训练、超参数调优和特征工程的需求，而 TimesFM 将类似的零样本逻辑应用于时间序列数据。MCP（模型上下文协议）是一个开源标准，用于将 AI 应用连接到外部系统、工具和数据源。Zer0Fit 将这些技术结合在一起，通过 MCP 将机器学习模型暴露为 LLM 可以调用的工具，创建了一个用户只需上传 CSV 文件并让聊天机器人执行分类或回归的流程。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://research.google/blog/introducing-tabfm-a-zero-shot-foundation-model-for-tabular-data/">Introducing TabFM: A zero-shot foundation model for tabular data</a></li>
<li><a href="https://modelcontextprotocol.io/">What is the Model Context Protocol ( MCP )? - Model Context Protocol</a></li>
<li><a href="https://github.com/google-research/tabfm">GitHub - google-research/tabfm</a></li>

</ul>
</details>

**标签**: `#Machine Learning`, `#MCP`, `#Foundation Models`, `#Zero-Shot Learning`, `#Local Deployment`

---

<a id="item-11"></a>
## [Codex 负责人 Tibo 分享通过 CLIProxyAPI 将 GPT-5.6 Sol 接入 Claude Code 的指南](https://x.com/thsottiaux/status/2076119366647894371) ⭐️ 7.0/10

OpenAI Codex 项目负责人 Tibo 在 X 上发布了一份快速指南，教 Claude Code 用户如何通过第三方工具 CLIProxyAPI 连接到 GPT-5.6 Sol 模型，整个过程约需五分钟。他建议将配置别名命名为"claudex"，并幽默地表示如果这套操作被屏蔽，他欠用户一次重置。 这展示了跨平台模型集成的实际应用，允许开发者在单一编码环境中利用不同的 AI 模型，而无需绑定某一平台的应用程序。它凸显了 AI 开发者工具日益增长的互操作性趋势，代理工具正在打破原本各自孤立的生态系统之间的壁垒。 CLIProxyAPI 是一个托管在 GitHub 上的开源（MIT 许可证）代理工具，它将多种 AI 模型的 CLI 工具——包括 Gemini CLI、Claude Code、ChatGPT Codex 和 Qwen Code——封装为兼容的 API。GPT-5.6 Sol 是 OpenAI 推出的分层模型系列的一部分，包含 Sol、Terra 和 Luna 三个模型，在 GPT-5.5 发布约两个月后推出。

telegram · zaihuapd · 7月12日 05:13

**背景**: Claude Code 是 Anthropic 推出的基于 CLI 的 AI 编程助手，而 Codex 是 OpenAI 的同类工具，两者都服务于希望在终端中直接使用 AI 生成代码的开发者。CLIProxyAPI 充当中间件桥梁，在不同模型提供商之间转换 API 调用，使为某一模型设计的工具能够访问另一个模型。GPT-5.6 Sol 是 OpenAI 最新的模型迭代版本，在生物学工作流程和基因组学分析等领域表现出改进，同时使用的 token 数量少于前代模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/router-for-me/CLIProxyAPI">GitHub - router-for-me/ CLIProxyAPI : Wrap Antigravity, ChatGPT...</a></li>
<li><a href="https://openai.com/index/previewing-gpt-5-6-sol/">Previewing GPT - 5 . 6 Sol : a next-generation model | OpenAI</a></li>
<li><a href="https://medium.com/mlworks/whats-new-with-openai-s-gpt5-6-551b3d8cc6b6">What’s New With OpenAI’s GPT 5 . 6 ? | by Mayur Jain | Medium</a></li>

</ul>
</details>

**标签**: `#AI tools`, `#Claude Code`, `#CLIProxyAPI`, `#model integration`, `#developer tools`

---
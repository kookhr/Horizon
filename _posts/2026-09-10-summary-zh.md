---
layout: default
title: "Horizon Summary: 2026-09-10 (ZH)"
date: 2026-09-10
lang: zh
---

> 从 36 条内容中筛选出 7 条重要资讯。

---

1. [微软正式将 Rust 定为一级编程语言](#item-1) ⭐️ 9.0/10
2. [Shopify 从 React Native 迁回原生 Swift 和 Kotlin 开发](#item-2) ⭐️ 9.0/10
3. [Calif Research 演示 WeWorm：首个借助 AI 在数天内构建的微信零点击蠕虫](#item-3) ⭐️ 9.0/10
4. [数学家质疑 OpenAI 是否能被信任处理未发表的研究成果](#item-4) ⭐️ 8.0/10
5. [数据中心的表后电力到底难在哪里？第一部分](#item-5) ⭐️ 8.0/10
6. [我试图让真实的果蝇连接组学会打乒乓球。它没有成功——而审查失败原因比成功本身有趣得多 (p)](#item-6) ⭐️ 8.0/10
7. [蚂蚁国际与 Visa、Mastercard 合作开发 AI 支付标准](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [微软正式将 Rust 定为一级编程语言](https://rustfoundation.org/media/guest-post-rust-is-tier-1-language-at-microsoft/) ⭐️ 9.0/10

微软已正式将 Rust 提升为一级语言地位，这意味着它在公司内部现在享有与 C++ 和 C# 等成熟语言相同的工具链支持、安全工作流和生产就绪级别。一个关键的技术进展是 Rust 与微软 MSVC 后端的集成，取代 LLVM 作为面向 Windows 的 Rust 构建的代码生成平台。 这一举措完成了一项战略转变：所有主要操作系统厂商——微软、谷歌、苹果和 Linux 发行版——现在都将 Rust 作为一流的系统编程语言予以支持，从根本上改变了系统编程的格局。对微软而言，这直接应对了其约 70% 的 CVE 源于内存安全问题的现状，并将 Rust 定位为新开发和未来大规模代码迁移的主要工具。 MSVC 集成意味着 Windows 上的 Rust 将使用微软自己的代码生成后端而非 LLVM，采用统一平台以最小化维护和演进成本。尽管获得了一级语言 designation，C++ 在微软现有代码库中仍然占据主导地位，转型将是渐进的——据报道，微软已设定到 2030 年利用自动化工具将 10 亿行代码转换为 Rust 的愿景。

hackernews · mmastrac · 9月10日 13:39 · [社区讨论](https://news.ycombinator.com/item?id=49643546)

**背景**: Rust 是一种系统编程语言，通过其所有权和借用机制在编译时强制执行内存安全，从根本上消除了困扰 C 和 C++ 代码库的缓冲区溢出和释放后使用等整类错误。MSVC（微软 Visual C++）工具链是微软面向 Windows 的原生编译器和链接器基础设施，提供 link.exe、Windows SDK 和通用 C 运行时（UCRT）。在微软，一级语言地位意味着该语言在公司整个生产流程中得到全面支持，包括安全审查、合规工作流和第一方开发者工具。微软自 2019 年起逐步加大 Rust 投入，从 Windows 和 Azure 服务中的实验性组件开始。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://rustfoundation.org/media/guest-post-rust-is-tier-1-language-at-microsoft/">Guest Post: Rust Is Tier-1 Language at Microsoft</a></li>
<li><a href="https://lobste.rs/s/eerwba/rust_is_tier_1_language_at_microsoft">Rust Is Tier-1 Language at Microsoft | Lobsters</a></li>
<li><a href="https://rust-pc.github.io/rust-msvc-toolchain.html">Rust MSVC Toolchain on Windows — Visual Studio Build Tools Setup</a></li>

</ul>
</details>

**社区讨论**: 社区情绪总体非常积极，评论者强调这证实了 Rust 作为 C++ 严肃竞争者的成熟度，而非一种新兴语言。多位评论者指出所有主要操作系统厂商现已实现系统语言选项多元化的战略意义，同时也有人提到 DARPA 正在进行的 C 到 Rust 自动转换工作以及微软雄心勃勃的十亿行代码转换目标，认为这些是转型规模的标志。一个值得注意的技术观察是，用 MSVC 后端取代 LLVM 才是真正重要的新闻，因为它深化了 Rust 与 Windows 的原生集成。

**标签**: `#rust`, `#microsoft`, `#systems-programming`, `#memory-safety`, `#language-adoption`

---

<a id="item-2"></a>
## [Shopify 从 React Native 迁回原生 Swift 和 Kotlin 开发](https://simonwillison.net/2026/Sep/10/shopify-react-native/) ⭐️ 9.0/10

Shopify 宣布将移动应用从 React Native 迁回独立的 Swift 和 Kotlin 原生代码库，并明确指出 AI 编程代理现在已经能够承担足够多的实现、翻译、测试和审查工作，使得维护双平台代码库不再是 2020 年时的决定性障碍。 Shopify 曾是 React Native 最具影响力的企业级采用者之一，这一逆转标志着团队评估跨平台与原生开发策略的方式可能发生范式转变。如果 AI 代理能够抵消维护独立平台代码库的成本，React Native 和 Flutter 等框架的核心价值主张可能会在整个行业中被重新审视。 Shopify 使用 React Native 已达六年并认可其为一个优秀的平台，但现在正在过渡离开。在 Shopify 维护的三个重要 React Native 库中——react-native-skia、flash-list 和 restyle——前两个正在移交给新的维护者，而 restyle 因用户群体较小将在 2026 年底归档。

rss · Simon Willison · 9月10日 21:11

**背景**: React Native 是由 Meta 开发的框架，允许开发者使用 JavaScript/TypeScript 编写移动应用并同时渲染为原生平台组件，从而在 iOS 和 Android 之间实现大量代码共享。Shopify 在 2020 年采用 React Native，目的是避免重复开发功能、让开发者能够跨技术栈工作，以及减少追求功能对等所花费的时间。移动开发中传统的权衡一直是：共享代码库的效率（跨平台）与完全原生开发带来的更优性能和平台特定用户体验之间的取舍。

**社区讨论**: 社区情绪不一但总体倾向于支持这一决定。一位开发者分享说他早已放弃 React Native 转向 Kotlin Multiplatform，并发现 AI 代理在编写 Swift 和 Kotlin 方面表现出色。另一位讲述了使用 Codex 在一夜之间将一个小型 RN 应用迁移为原生 iOS 和 Android 应用的经历。一位持怀疑态度的评论者指出，他观察跨平台与原生的争论已近二十年，认为跨平台框架从未真正实现承诺的减少人力成本的效果。另一位评论者则对 AI 驱动迁移的说法提出质疑，分享了自己在 2026 年 1 月之前、在没有大量 LLM 辅助的情况下完成类似 RN 到原生迁移的经历。

**标签**: `#mobile-development`, `#react-native`, `#ai-coding-agents`, `#shopify`, `#architecture`

---

<a id="item-3"></a>
## [Calif Research 演示 WeWorm：首个借助 AI 在数天内构建的微信零点击蠕虫](https://simonwillison.net/2026/Sep/10/calif-research/) ⭐️ 9.0/10

2026 年 9 月 8 日，Calif Research 发布了 WeWorm 的演示，这是首个能够通过微信通话在 iOS 和 Android 上传播的零点击蠕虫，受害者无需任何交互即可被攻击。团队借助 AI 在约两天内发现了漏洞并编写了远程代码执行（RCE）漏洞利用程序，完整蠕虫仅用一周便构建完成——而此类工作过去需要更大的团队耗时数月。 WeWorm 表明 AI 能够大幅加速关键移动漏洞的发现和武器化进程，将时间线从数月压缩至数天，并降低了大规模生产复杂零点击漏洞利用的门槛。微信拥有超过十亿用户，此类蠕虫理论上可攻陷数量空前的设备，标志着 AI 驱动的攻击性安全能力正在发生范式转变。 无论受害者是否接听电话，漏洞利用都能成功；即使接听，受害者也听不到任何声音——没有需要避免的恶意链接，也没有需要拒绝的附件。Calif 团队强调，AI 完成了大部分技术工作，而人类则提供了关于目标选择和安全测试方法的判断，他们在受控环境中演示了蠕虫在三台测试手机间的传播。

rss · Simon Willison · 9月10日 00:56

**背景**: 零点击漏洞利用无需受害者采取任何操作即可成功，是最令人恐惧的移动攻击类别之一，因为传统的用户谨慎行为无法提供任何保护。蠕虫是一种能够自我传播的恶意软件，通过从一个受感染系统扩散到其他系统来传播，通常通过网络连接，或如本案例中通过劫持账户联系受害者的联系人来传播。远程代码执行（RCE）是一类网络攻击，攻击者可以在目标设备上远程执行任意代码，进而部署更多恶意软件或完全控制设备。微信是全球使用最广泛的即时通讯平台之一，拥有超过十亿活跃账户，任何影响微信的漏洞在规模上都可能造成灾难性后果。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thehackernews.com/2026/09/wechat-zero-click-worm-took-over.html">WeChat Zero-Click Worm Took Over Accounts on iPhone and Android via Incoming Calls</a></li>
<li><a href="https://calif.io/research/weworm">WeWorm | Calif</a></li>
<li><a href="https://cybersecuritynews.com/weworm-first-0-click-worm/">WeWorm - First 0-Click Worm Spreading Through WeChat Calls...</a></li>

</ul>
</details>

**标签**: `#ai-security-research`, `#zero-click-exploit`, `#mobile-security`, `#ai-vulnerability-discovery`, `#wechat`

---

<a id="item-4"></a>
## [数学家质疑 OpenAI 是否能被信任处理未发表的研究成果](https://mathstodon.xyz/@andreasthom/117240535270608201) ⭐️ 8.0/10

包括 Andrea Thomazy 和 Valerio Capraro 在内的数学家公开提出担忧，认为 OpenAI 可能吸收了研究人员在与模型交互过程中分享的未发表数学思想，并在未经署名的情况下将其用于自己的已发表成果。这场讨论主要在 Mathstodon 和 X 上展开，吸引了数百条评论，围绕 AI 公司使用用户提供的知识内容进行训练的伦理问题展开辩论。 这一争议触及了 AI 辅助研究协作中信任的核心问题——研究人员经常在与 AI 模型交互时分享未发表的想法、部分证明和新颖方法。如果 AI 公司无法令人信服地保证用户交互不会被用于其自身的发表成果，这可能会从根本上削弱学术界使用前沿 AI 工具的意愿，从而抑制一整类科学发现模式的发展。 据报道，OpenAI 声称用于生成其已发表数学结果的模型并未基于相关协作对话进行训练，但怀疑者指出，现代模型的参数规模庞大，即使没有精确记忆，潜在表示仍有可能受到先前交互的影响。辩论还涉及模型从训练数据中吸收特定技术与通过强化学习在海量算力上独立发现解决方案之间的区别。

hackernews · pred_ · 9月10日 06:49 · [社区讨论](https://news.ycombinator.com/item?id=49639408)

**背景**: OpenAI 一直在积极邀请研究人员使用其模型进行数学研究，据称已向至少 10 万名研究人员提供免费访问权限，同时据报道其内部以惊人的速度解决开放数学问题。当研究人员与 Codex 或 ChatGPT 等模型交互时，他们可能会分享未发表的方法、猜想或部分证明，这些内容随后被记录为用户数据。核心伦理问题是：AI 公司是否应被允许使用可能包含原创知识贡献的交互数据来训练或改进模型，进而产出已发表成果；以及如果研究人员的想法可能影响了模型输出，是否应给予署名。

**社区讨论**: 社区内部存在严重分歧。一些人如 sebzim4500 完全驳斥了抄袭指控，认为只有 OpenAI 产出了实际证明，并将其比作《社交网络》中的经典台词。另一些人如 nezi 则提出了与人类协作伦理的类比，指出如果 OpenAI 是一名人类研究者，吸收了合作者的想法却不署名发表，这显然是不道德的。sashank_1509 提出了更细致的观点，认为两种可能性可以并存：模型可能从对话中吸收想法以改善潜在表示，同时也通过强化学习独立发现解决方案。bertonvv 则提出了更广泛的系统性担忧：研究人员是否正在以免费访问为幌子被系统性地诱导向 AI 公司分享自己最好的开放问题研究工作。

**标签**: `#openai`, `#research-ethics`, `#ai-trust`, `#mathematics`, `#intellectual-property`

---

<a id="item-5"></a>
## [数据中心的表后电力到底难在哪里？第一部分](https://newsletter.semianalysis.com/p/what-is-so-hard-about-behind-the) ⭐️ 8.0/10

深入分析数据中心实施表后电力解决方案所面临的技术与经济挑战，对比实验性方法与盈利策略。

rss · Semianalysis · 9月10日 14:28

**标签**: `#datacenters`, `#power infrastructure`, `#behind-the-meter`, `#AI infrastructure`, `#energy`

---

<a id="item-6"></a>
## [我试图让真实的果蝇连接组学会打乒乓球。它没有成功——而审查失败原因比成功本身有趣得多 (p)](https://www.reddit.com/r/MachineLearning/comments/1wc67ci/i_tried_to_make_a_real_fly_connectome_learn_to/) ⭐️ 8.0/10

一位工程师详细记录了试图让真实果蝇连接组学会打乒乓球的失败经历，在此过程中发现了关键的数据错误和结构性问题。

reddit · r/MachineLearning · /u/oPeraza2007 · 9月10日 02:28

**标签**: `#Connectomics`, `#Neuroscience`, `#Machine Learning`, `#Reinforcement Learning`, `#Debugging`

---

<a id="item-7"></a>
## [蚂蚁国际与 Visa、Mastercard 合作开发 AI 支付标准](https://www.cnbc.com/2026/09/10/ant-international-visa-mastercard-ai-agent-payment-standard.html) ⭐️ 8.0/10

蚂蚁国际与 Visa 和 Mastercard 合作，为 AI 代理开发通用支付标准，其中包括用于风险评估和跨系统互操作性的

telegram · zaihuapd · 9月10日 03:00

**标签**: `#AI agents`, `#fintech`, `#payment standards`, `#Visa`, `#Mastercard`

---
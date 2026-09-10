---
layout: default
title: "Horizon Summary: 2026-09-10 (EN)"
date: 2026-09-10
lang: en
---

> From 36 items, 7 important content pieces were selected

---

1. [Microsoft Officially Designates Rust as a Tier-1 Programming Language](#item-1) ⭐️ 9.0/10
2. [Shopify Migrates from React Native Back to Native Swift and Kotlin](#item-2) ⭐️ 9.0/10
3. [Calif Research Demos WeWorm: First Zero-Click WeChat Worm Built with AI in Days](#item-3) ⭐️ 9.0/10
4. [Mathematicians Question Whether OpenAI Can Be Trusted with Unpublished Research](#item-4) ⭐️ 8.0/10
5. [What is So Hard About Behind-The-Meter Power For Datacenters? Part 1](#item-5) ⭐️ 8.0/10
6. [I tried to make a real fly connectome learn to play Pong. It didn't — and auditing why turned out to be way more interesting than if it had worked (p)](#item-6) ⭐️ 8.0/10
7. [蚂蚁国际与 Visa、Mastercard 合作开发 AI 支付标准](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Microsoft Officially Designates Rust as a Tier-1 Programming Language](https://rustfoundation.org/media/guest-post-rust-is-tier-1-language-at-microsoft/) ⭐️ 9.0/10

Microsoft has officially elevated Rust to tier-1 language status, meaning it now receives the same level of toolchain support, security workflows, and production readiness as established languages like C++ and C# within the company. A key technical development is the integration of Rust with Microsoft's MSVC backend, replacing LLVM as the code generation platform for Windows-targeted Rust builds. This move completes a strategic shift where all major OS vendors — Microsoft, Google, Apple, and Linux distributions — now support Rust as a first-class systems programming language, fundamentally altering the systems programming landscape. For Microsoft specifically, this addresses the fact that approximately 70% of their CVEs stem from memory safety issues, and positions Rust as a primary tool for both new development and eventual large-scale code migration. The MSVC integration means Rust on Windows will use Microsoft's own codegen backend rather than LLVM, utilizing a unified platform that minimizes maintenance and evolution costs. Despite this tier-1 designation, C++ still dominates Microsoft's existing codebase after decades of development, and the transition will be gradual — Microsoft has reportedly set a vision to convert 1 billion lines of code to Rust by 2030 using automated tooling.

hackernews · mmastrac · Sep 10, 13:39 · [Discussion](https://news.ycombinator.com/item?id=49643546)

**Background**: Rust is a systems programming language that enforces memory safety at compile time through its ownership and borrowing system, eliminating entire classes of bugs like buffer overflows and use-after-free errors that plague C and C++ codebases. The MSVC (Microsoft Visual C++) toolchain is Microsoft's native compiler and linker infrastructure for Windows, providing link.exe, the Windows SDK, and the Universal C Runtime (UCRT). Tier-1 language status at Microsoft means a language is fully supported across the company's production pipelines, including security review, compliance workflows, and first-party developer tooling. Microsoft has been gradually increasing its Rust investment since 2019, starting with experimental components in Windows and Azure services.

<details><summary>References</summary>
<ul>
<li><a href="https://rustfoundation.org/media/guest-post-rust-is-tier-1-language-at-microsoft/">Guest Post: Rust Is Tier-1 Language at Microsoft</a></li>
<li><a href="https://lobste.rs/s/eerwba/rust_is_tier_1_language_at_microsoft">Rust Is Tier-1 Language at Microsoft | Lobsters</a></li>
<li><a href="https://rust-pc.github.io/rust-msvc-toolchain.html">Rust MSVC Toolchain on Windows — Visual Studio Build Tools Setup</a></li>

</ul>
</details>

**Discussion**: Community sentiment is overwhelmingly positive, with commenters highlighting that this confirms Rust's maturity as a serious competitor to C++ rather than a fledgling language. Several commenters noted the strategic significance of all major OS vendors now having diversified their systems language options, while others pointed to DARPA's ongoing work on automated C-to-Rust conversion and Microsoft's ambitious billion-line conversion goal as indicators of the scale of this transition. A notable technical observation was that replacing LLVM with MSVC's backend is the truly significant news, as it deepens Rust's native Windows integration.

**Tags**: `#rust`, `#microsoft`, `#systems-programming`, `#memory-safety`, `#language-adoption`

---

<a id="item-2"></a>
## [Shopify Migrates from React Native Back to Native Swift and Kotlin](https://simonwillison.net/2026/Sep/10/shopify-react-native/) ⭐️ 9.0/10

Shopify announced it is moving away from React Native back to separate Swift and Kotlin native codebases for its mobile apps, explicitly citing that AI coding agents can now handle enough of the implementation, translation, testing, and review work to make maintaining dual codebases no longer the deciding factor it was in 2020. Shopify was one of the most prominent enterprise adopters of React Native, and this reversal signals a potential paradigm shift in how teams evaluate cross-platform versus native development strategies. If AI agents can offset the cost of maintaining separate platform codebases, the core value proposition of frameworks like React Native and Flutter may be fundamentally reevaluated across the industry. Shopify has used React Native for six years and credits it as a great platform, but is now transitioning away. Of the three significant React Native libraries Shopify maintains — react-native-skia, flash-list, and restyle — the first two are being transferred to new maintainers, while restyle will be archived at the end of 2026 due to a smaller user base.

rss · Simon Willison · Sep 10, 21:11

**Background**: React Native is a framework developed by Meta that allows developers to write mobile applications in JavaScript/TypeScript while rendering to native platform components, enabling significant code sharing between iOS and Android. Shopify adopted React Native in 2020 to stop building features twice, let developers work across the stack, and reduce time spent chasing feature parity. The traditional trade-off in mobile development has been between the efficiency of a shared codebase (cross-platform) and the superior performance and platform-specific UX of fully native development.

**Discussion**: Community sentiment is mixed but leans supportive of the move. One developer shared they abandoned React Native for Kotlin Multiplatform and found AI agents proficient at writing both Swift and Kotlin. Another recounted using Codex to migrate a small RN app to native iOS and Android overnight. A skeptic noted they have watched this cross-platform versus native debate cycle for nearly two decades, arguing that cross-platform frameworks never actually reduce headcount costs as promised. Another commenter pushed back on the AI-enabled narrative, sharing that they completed a similar RN-to-native migration before January 2026 without significant LLM assistance.

**Tags**: `#mobile-development`, `#react-native`, `#ai-coding-agents`, `#shopify`, `#architecture`

---

<a id="item-3"></a>
## [Calif Research Demos WeWorm: First Zero-Click WeChat Worm Built with AI in Days](https://simonwillison.net/2026/Sep/10/calif-research/) ⭐️ 9.0/10

On September 8, 2026, Calif Research released a demo of WeWorm, the first zero-click worm capable of spreading through WeChat calls across both iOS and Android, requiring no victim interaction whatsoever. The team used AI assistance to find the vulnerability and write a remote code execution (RCE) exploit in approximately two days, with the full worm completed in one additional week—a task that previously required a larger team months of work. WeWorm demonstrates that AI can dramatically accelerate the discovery and weaponization of critical mobile vulnerabilities, compressing timelines from months to days and lowering the barrier for producing sophisticated zero-click exploits at scale. With WeChat boasting over a billion users, a worm of this nature could theoretically compromise an unprecedented number of devices, signaling a paradigm shift in offensive security capabilities driven by AI. The exploit succeeds whether or not the victim answers the call, and if they do answer, they hear nothing—there is no malicious link to avoid and no attachment to decline. Calif's team emphasized that AI handled most of the technical work while humans provided judgment on targeting and safe testing practices, and they demonstrated the worm spreading among three test phones in a controlled environment.

rss · Simon Willison · Sep 10, 00:56

**Background**: A zero-click exploit requires no action from the victim to succeed, making it among the most feared classes of mobile attacks because traditional user caution offers no protection. A worm is a type of malware that self-propagates by spreading from one infected system to others, often through network connections or, as in this case, by hijacking an account to contact the victim's contacts. Remote code execution (RCE) is a class of cyberattack where an attacker can remotely execute arbitrary code on a target device, which can then be used to deploy additional malware or take full control. WeChat is one of the world's most widely used messaging platforms with over a billion active accounts, making any vulnerability affecting it potentially catastrophic in scale.

<details><summary>References</summary>
<ul>
<li><a href="https://thehackernews.com/2026/09/wechat-zero-click-worm-took-over.html">WeChat Zero-Click Worm Took Over Accounts on iPhone and Android via Incoming Calls</a></li>
<li><a href="https://calif.io/research/weworm">WeWorm | Calif</a></li>
<li><a href="https://cybersecuritynews.com/weworm-first-0-click-worm/">WeWorm - First 0-Click Worm Spreading Through WeChat Calls...</a></li>

</ul>
</details>

**Tags**: `#ai-security-research`, `#zero-click-exploit`, `#mobile-security`, `#ai-vulnerability-discovery`, `#wechat`

---

<a id="item-4"></a>
## [Mathematicians Question Whether OpenAI Can Be Trusted with Unpublished Research](https://mathstodon.xyz/@andreasthom/117240535270608201) ⭐️ 8.0/10

Mathematicians including Andrea Thomazy and Valerio Capraro have publicly raised concerns that OpenAI may have absorbed researchers' unpublished mathematical ideas shared during model interactions and used them to produce published results without attribution. The discussion, primarily on Mathstodon and X, has drawn significant engagement with hundreds of comments debating the ethics of AI companies training on user-provided intellectual content. This controversy strikes at the heart of trust in AI-assisted research collaboration, where researchers routinely share unpublished ideas, partial proofs, and novel approaches with AI models. If AI companies cannot credibly guarantee that user interactions are not leveraged for their own publications, it could fundamentally undermine the willingness of the academic community to engage with frontier AI tools, chilling an entire mode of scientific discovery. OpenAI has reportedly claimed that the model used to generate their published mathematical results was not trained on the collaborative chats in question, but skeptics note that the massive parameter counts of modern models make it plausible that latent representations are influenced by prior interactions even if exact memorization does not occur. The debate also involves the distinction between a model absorbing specific techniques from training data versus independently discovering solutions through reinforcement learning on verifiable math problems with massive compute.

hackernews · pred_ · Sep 10, 06:49 · [Discussion](https://news.ycombinator.com/item?id=49639408)

**Background**: OpenAI has been actively inviting researchers to use its models for mathematical work, reportedly granting free access to at least 100,000 researchers, while also reportedly solving open mathematical problems at a surprisingly fast rate internally. When researchers interact with models like Codex or ChatGPT, they may share unpublished approaches, conjectures, or partial proofs that are then logged as user data. The central ethical question is whether AI companies should be permitted to use such interaction data—potentially containing original intellectual contributions—to train or improve models that subsequently produce published results, and whether attribution is owed to the researchers whose ideas may have influenced the model's outputs.

**Discussion**: The community is deeply divided. Some, like sebzim4500, dismiss the plagiarism accusations entirely, arguing that only OpenAI has produced actual proofs and comparing the situation to the famous Social Network quote. Others, like nezi, draw a compelling analogy to human collaboration ethics, noting that if OpenAI were a human researcher who absorbed ideas from collaborators and published without attribution, it would be clearly unethical. A more nuanced view from sashank_1509 suggests both possibilities can coexist: models may absorb ideas from chats to improve latent representations, while also independently discovering solutions through reinforcement learning. bertonvv raises a broader systemic concern about whether researchers are being systematically fooled into sharing their best open-problem work with AI companies under the guise of free access.

**Tags**: `#openai`, `#research-ethics`, `#ai-trust`, `#mathematics`, `#intellectual-property`

---

<a id="item-5"></a>
## [What is So Hard About Behind-The-Meter Power For Datacenters? Part 1](https://newsletter.semianalysis.com/p/what-is-so-hard-about-behind-the) ⭐️ 8.0/10

An in-depth analysis of the technical and economic challenges of implementing behind-the-meter power solutions for datacenters, contrasting experimental approaches with profitable strategies.

rss · Semianalysis · Sep 10, 14:28

**Tags**: `#datacenters`, `#power infrastructure`, `#behind-the-meter`, `#AI infrastructure`, `#energy`

---

<a id="item-6"></a>
## [I tried to make a real fly connectome learn to play Pong. It didn't — and auditing why turned out to be way more interesting than if it had worked (p)](https://www.reddit.com/r/MachineLearning/comments/1wc67ci/i_tried_to_make_a_real_fly_connectome_learn_to/) ⭐️ 8.0/10

An engineer details the informative failure of attempting to make a real fly connectome learn to play Pong, uncovering critical data bugs and structural issues in the process.

reddit · r/MachineLearning · /u/oPeraza2007 · Sep 10, 02:28

**Tags**: `#Connectomics`, `#Neuroscience`, `#Machine Learning`, `#Reinforcement Learning`, `#Debugging`

---

<a id="item-7"></a>
## [蚂蚁国际与 Visa、Mastercard 合作开发 AI 支付标准](https://www.cnbc.com/2026/09/10/ant-international-visa-mastercard-ai-agent-payment-standard.html) ⭐️ 8.0/10

Ant International partners with Visa and Mastercard to develop a universal payment standard for AI agents, including a 'Know Your Agent' mechanism for risk assessment and cross-system interoperability.

telegram · zaihuapd · Sep 10, 03:00

**Tags**: `#AI agents`, `#fintech`, `#payment standards`, `#Visa`, `#Mastercard`

---
---
layout: default
title: "Horizon Summary: 2026-08-13 (EN)"
date: 2026-08-13
lang: en
---

> From 32 items, 10 important content pieces were selected

---

1. [Google Releases Gemini 3.7 Flash with Improved Vision and Reasoning](#item-1) ⭐️ 9.0/10
2. [Cerebras and OpenAI Launch Ultrafast Mode for GPT-5.6 Sol](#item-2) ⭐️ 9.0/10
3. [DeepSeek Releases V4 Pro 0813: A 1.7T Parameter Open-Weight Model](#item-3) ⭐️ 9.0/10
4. [CXMT Overtakes Tencent as China's Most Valuable Company](#item-4) ⭐️ 9.0/10
5. [DeepSeek-V4-Pro Officially Released with Peak/Off-Peak API Pricing](#item-5) ⭐️ 9.0/10
6. [Christopher Domas Unveils 'Spaghettifying DRAM' for Ring-0 Access](#item-6) ⭐️ 8.0/10
7. [Choose Boring Technology: A Foundational Essay on Technology Selection](#item-7) ⭐️ 8.0/10
8. [DeepSeek Harness Developer Preview Released](#item-8) ⭐️ 8.0/10
9. [Trump Memo Authorizes Private Firms to Conduct State-Backed Overseas Cyberattacks](#item-9) ⭐️ 8.0/10
10. [DeepMind's SL2T Brings Sign Language Translation to Pixel 11](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Google Releases Gemini 3.7 Flash with Improved Vision and Reasoning](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-3-7-flash/) ⭐️ 9.0/10

Google has released Gemini 3.7 Flash, a new lightweight AI model featuring improved vision capabilities, enhanced reasoning for knowledge-dense fields like finance and law, and competitive introductory pricing. It significantly outperforms its predecessor 3.6 Flash on benchmarks like GDP.pdf (34.0% vs 22.0%) and AutomationBench (30.4% vs 17.0%). This release intensifies competition in the lightweight AI model market, where Google is positioning Flash as a cost-effective workhorse for high-volume, real-world business workflows and multimodal tasks. The model's strong vision capabilities and document processing make it particularly relevant for enterprise applications requiring complex document understanding. The introductory pricing is scheduled to double on December 31, 2026, raising questions about long-term value given the rapid pace of model releases — 3.6 Flash came out just three weeks prior. The model supports adjustable thinking levels (high, medium, low) for controlling reasoning token usage, and can be combined with other Google tools like Nano Banana for dynamic content generation.

hackernews · thisisauserid · Aug 13, 17:23 · [Discussion](https://news.ycombinator.com/item?id=49289112)

**Background**: Gemini is Google's family of multimodal large language models developed by Google DeepMind, with Flash variants designed as lightweight, cost-effective options for high-volume use cases. The Flash series has traditionally been positioned for low-cost, mostly text-based tasks like summarization, parsing, and formatting, though Google is now expanding its capabilities into more complex reasoning and vision work. The AI model market is currently seeing rapid iteration, with competitors like OpenAI's GPT-5.6 Luna and Anthropic's Opus 5 offering aggressive pricing and performance in the same lightweight segment.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-3-7-flash/">Gemini 3.7 Flash: our most intelligent workhorse model</a></li>
<li><a href="https://deepmind.google/models/gemini/flash/">Gemini 3.7 Flash — Google DeepMind</a></li>

</ul>
</details>

**Discussion**: Community testing shows Gemini 3.7 Flash performs impressively on image-to-HTML conversion tasks, though Anthropic's Opus 5 remains best-in-class for such vision work despite being more expensive. Users have raised concerns about the unusual pricing strategy — introductory prices doubling in five months — and question the model's competitiveness against cheaper alternatives like GPT-5.6 Luna, which offers strong benchmark performance at lower cost. Several commenters note that Flash's positioning seems to have shifted from low-cost text processing toward competing more directly with mid-tier models like Terra rather than Luna.

**Tags**: `#AI`, `#LLM`, `#Google`, `#Gemini`, `#Machine Learning`

---

<a id="item-2"></a>
## [Cerebras and OpenAI Launch Ultrafast Mode for GPT-5.6 Sol](https://www.cerebras.ai/blog/accelerating-gpt-5-6-sol-ultrafast-with-openai) ⭐️ 9.0/10

Cerebras and OpenAI announced a new "Ultrafast" mode for GPT-5.6 Sol that processes all 2,500 questions on the HLE benchmark in 11 hours and 11 minutes, compared to 78 hours and 27 minutes for Claude Fable 5, achieving comparable accuracy nearly 7× faster. The system leverages Cerebras's wafer-scale compute technology to dramatically reduce inference time for a frontier-level LLM. This collaboration demonstrates that specialized hardware can fundamentally change the economics and feasibility of running frontier AI models, making high-capability reasoning accessible in a fraction of the time. The speed gains could enable new paradigms of iterative LLM thinking, where models can perform multiple passes of reasoning and revision rather than relying on a single-pass output. According to Artificial Analysis data cited in the announcement, GPT-5.6 Sol on Ultrafast mode runs 11× faster than Fable 5 and 5× faster than Opus 4.8 on Fast mode. However, neither Cerebras nor OpenAI explicitly states that Ultrafast mode produces identical output quality to standard GPT-5.6 Sol, and no pricing information has been disclosed, suggesting it may be in an interest-gauging phase.

hackernews · pr337h4m · Aug 13, 18:10 · [Discussion](https://news.ycombinator.com/item?id=49289844)

**Background**: Wafer-scale integration (WSI) is an approach to building very large integrated circuits from an entire silicon wafer, producing a single "super-chip" that avoids the off-chip communication bottlenecks inherent in traditional multi-chip designs. Cerebras Systems has pioneered this technology with its Wafer-Scale Engine (WSE) series, integrating hundreds of thousands of cores with local fast memory on a single chip. The HLE (Humanity's Last Exam) benchmark was explicitly designed to be a frontier-difficulty test that no current AI model can fully solve, providing a multi-year window of discrimination between systems. GPT-5.6 Sol is the flagship variant in OpenAI's GPT-5.6 model family, released in 2026 and optimized for complex reasoning, coding, and long-horizon problem solving.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Wafer-scale_integration">Wafer-scale integration - Wikipedia</a></li>
<li><a href="https://www.usenix.org/publications/loginonline/wafer-scale-ai-compute-system-software-perspective">Wafer-Scale AI Compute: A System Software Perspective</a></li>
<li><a href="https://en.wikipedia.org/wiki/Humanity's_Last_Exam">Humanity's Last Exam - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/GPT-5.6_Sol">GPT-5.6 Sol</a></li>

</ul>
</details>

**Discussion**: Community sentiment is a mix of excitement and healthy skepticism. Users like iamcoder18 and wxw highlighted the impressive speed metrics, with wxw noting the 11× and 5× speed advantages over Fable 5 and Opus 4.8 respectively. csallen offered a thoughtful perspective that speed enables iterative reasoning, potentially shifting LLM thinking from single-pass to multi-pass revision. However, Topfi raised concerns that neither company explicitly confirmed 1:1 performance parity with standard GPT-5.6 Sol, and GodelNumbering noted the absence of pricing information, suggesting it may be prohibitively expensive or still in a demand-gauging phase.

**Tags**: `#AI`, `#Cerebras`, `#OpenAI`, `#LLM`, `#Hardware`

---

<a id="item-3"></a>
## [DeepSeek Releases V4 Pro 0813: A 1.7T Parameter Open-Weight Model](https://simonwillison.net/2026/Aug/12/deepseek-v4-pro-0813/) ⭐️ 9.0/10

DeepSeek has released V4 Pro 0813, a new 1.7 trillion parameter mixture-of-experts model with open weights available on Hugging Face (893 GB) and accessible via API on OpenRouter. The model supports a 1,048,576 token context window with a maximum output of 384,000 tokens, and is priced at $0.435 per million input tokens and $0.87 per million output tokens on OpenRouter. The release of a 1.7T parameter open-weight model represents a paradigm-shifting milestone for the open-source AI community, pushing the boundaries of what is publicly accessible. It intensifies competition with proprietary models and offers developers and researchers access to frontier-scale capabilities at relatively low API costs. The model features three distinct reasoning levels (low, medium, high) that produce visibly different outputs, an unusual characteristic noted by early testers. While it scores 53 on the Artificial Analysis Intelligence Index (well above the median of 27), some developers have expressed feeling underwhelmed by its overall benchmark performance and disappointed by its pricing.

rss · Simon Willison · Aug 12, 23:59

**Background**: DeepSeek is a Chinese AI startup that has gained significant attention for releasing large-scale open-weight models, following previous releases like DeepSeek-V4-Pro in April and DeepSeek-V4-Flash-0731 in July. The V4 Pro 0813 model uses a Mixture-of-Experts (MoE) architecture, which activates only a subset of its parameters during inference to maintain efficiency despite the massive total parameter count. OpenRouter serves as a unified API gateway that provides access to hundreds of AI models from different providers through a single interface, making new models immediately accessible to developers.

<details><summary>References</summary>
<ul>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4-pro-0813">DeepSeek V4 Pro 0813 - API Pricing & Benchmarks | OpenRouter</a></li>
<li><a href="https://artificialanalysis.ai/models/deepseek-v4-pro">DeepSeek V4 Pro 0813 (max) - Intelligence, Performance & Price Analysis</a></li>
<li><a href="https://www.scmp.com/tech/big-tech/article/3363895/deepseeks-updated-v4-pro-ai-model-struggles-benchmarks-shines-cybersecurity">DeepSeek’s updated V4 Pro AI model struggles on benchmarks, shines in cybersecurity | South China Morning Post</a></li>

</ul>
</details>

**Discussion**: The community reaction has been mixed: while the open-weight release of a 1.7T parameter model is widely recognized as a significant achievement, developers on platforms like Reddit and Hacker News have noted that benchmark results were initially shared only through a WeChat group before being copied to Western forums. Some users expressed underwhelm at the model's overall capabilities and pricing, while others found the distinct output variations across reasoning levels to be an intriguing and unique characteristic worth further exploration.

**Tags**: `#llm`, `#deepseek`, `#open-weights`, `#ai`, `#openrouter`

---

<a id="item-4"></a>
## [CXMT Overtakes Tencent as China's Most Valuable Company](https://www.bloomberg.com/news/articles/2026-08-13/cxmt-overtakes-tencent-to-become-most-valuable-chinese-company) ⭐️ 9.0/10

CXMT (长鑫存储) surpassed Tencent to become China's most valuable company, with a market capitalization of approximately $524 billion compared to Tencent's $510 billion as of Thursday. CXMT recently listed on the Shanghai STAR Market last month, surging 467% on its first trading day and gaining an additional 8% since then. This marks a historic shift in China's technology landscape, where a semiconductor memory company has overtaken a long-dominant internet giant as the most valuable firm. It signals a major market realignment toward hardware and chip manufacturing, driven by China's push for semiconductor self-sufficiency and the growing strategic importance of DRAM supply chains. Tencent's stock has declined over 26% year-to-date, falling 4.5% on Thursday alone, largely due to heavy AI investment costs weighing on profitability. According to Omdia data, CXMT ranked as the world's fourth-largest DRAM maker by revenue in Q4 2025 with approximately 7.67% global market share, trailing Samsung, SK Hynix, and Micron, with SemiAnalysis projecting its share to rise from about 11% to 15% by 2028.

telegram · zaihuapd · Aug 13, 10:10

**Background**: CXMT (长鑫存储技术股份有限公司) is an integrated memory manufacturing company founded in 2016 and headquartered in Hefei, Anhui Province, specializing in the design, R&D, production, and sales of DRAM (Dynamic Random Access Memory) chips. The company went public on the Shanghai STAR Market in July 2026, raising approximately 29.5 billion RMB (about $4.3 billion), making it China's largest IPO of 2026. DRAM is a critical component in computing devices, and the global market has long been dominated by Samsung, SK Hynix, and Micron, with CXMT emerging as China's national champion in this strategically vital sector amid US-China technology tensions.

<details><summary>References</summary>
<ul>
<li><a href="https://zh.wikipedia.org/wiki/长鑫存储">长鑫存储 - 维基百科，自由的百科全书</a></li>
<li><a href="https://www.geekpark.net/news/368087">上 市 暴涨的 长 鑫 存 储 ，直接把美国股 市 干崩了 | 极客公园</a></li>
<li><a href="https://www.tmtpost.com/8079902.html">长 鑫 存 储 上 市 ，赶 上 了一个好时候-钛媒体官方网站</a></li>

</ul>
</details>

**Tags**: `#semiconductors`, `#CXMT`, `#Tencent`, `#market-cap`, `#China-tech`

---

<a id="item-5"></a>
## [DeepSeek-V4-Pro Officially Released with Peak/Off-Peak API Pricing](https://api-docs.deepseek.com/zh-cn/updates) ⭐️ 9.0/10

DeepSeek-V4-Pro has been officially released across app, web, and API platforms with the model name deepseek-v4-pro, featuring enhanced Agent capabilities and native Responses API support compatible with Codex. Both V4-Pro and V4-Flash add three thinking mode tiers — low, high, and max — while the API introduces a peak/off-peak pricing structure effective August 17, 2026, with off-peak rates at half the peak price. This release marks a significant capability upgrade for one of the most widely used open-weight AI model families, directly impacting AI/ML development workflows and deployment costs. The peak/off-peak pricing model introduces a new cost-management dimension that could reshape how developers schedule API-intensive workloads. The Responses API currently only supports deepseek-v4-flash, with deepseek-v4-pro support planned for early August 2026. Peak pricing hours are 09:00–12:00 and 14:00–18:00 Beijing time (UTC+8), and DeepSeek recommends setting the context window to at least 384K tokens for Think Max mode due to potentially extremely long reasoning chains.

telegram · zaihuapd · Aug 13, 11:12

**Background**: DeepSeek is a prominent AI model provider known for its open-weight large language models. The Responses API is a newer API format that supports agentic workflows and tool-calling, designed to be compatible with OpenAI's Codex ecosystem. Thinking modes allow the model to produce chain-of-thought reasoning before outputting a final answer, with higher tiers generating longer reasoning chains for improved accuracy on complex problems. Peak/off-peak pricing is a demand-management strategy where API calls during high-traffic hours cost more than during low-traffic periods.

<details><summary>References</summary>
<ul>
<li><a href="https://api-docs.deepseek.com/guides/responses_api/">Using the Responses API | DeepSeek API Docs</a></li>
<li><a href="https://api-docs.deepseek.com/guides/thinking_mode/">Thinking Mode | DeepSeek API Docs</a></li>
<li><a href="https://chat-deep.ai/pricing/deepseek-api-cost-calculator/">DeepSeek API Cost Calculator: V4 Flash & Pro</a></li>

</ul>
</details>

**Tags**: `#DeepSeek`, `#LLM`, `#AI`, `#API`, `#Release`

---

<a id="item-6"></a>
## [Christopher Domas Unveils 'Spaghettifying DRAM' for Ring-0 Access](https://github.com/xoreaxeaxeax/skitter-creek-bath-salts) ⭐️ 8.0/10

Christopher Domas presents 'Spaghettifying DRAM,' a hardware-level technique for manipulating DRAM to gain ring-0 access, with significant implications for system and console security.

hackernews · matt_d · Aug 13, 14:17 · [Discussion](https://news.ycombinator.com/item?id=49286341)

**Tags**: `#hardware security`, `#DRAM`, `#privilege escalation`, `#x86`, `#vulnerability`

---

<a id="item-7"></a>
## [Choose Boring Technology: A Foundational Essay on Technology Selection](https://mcfunley.com/choose-boring-technology) ⭐️ 8.0/10

Dan McKinley's 2015 essay "Choose Boring Technology" argues that companies should deliberately select proven, 'boring' technologies over novel ones to minimize operational risk and complexity, introducing the concept of limited 'innovation tokens' to quantify how much new tech a team can safely adopt. The essay has recently resurfaced in discussions, with community members applying its framework to modern contexts like AI agents. This essay remains a foundational reference in engineering management and software architecture, providing a practical framework for making technology tradeoffs that balance innovation with stability. Its core idea—that every new technology introduces hidden operational costs—continues to influence how engineering leaders think about tech stack decisions, especially as teams navigate the temptation of rapidly emerging technologies like AI agents. The essay proposes that each company has approximately three 'innovation tokens' to spend on new technologies, with boring choices being free but innovative ones costing tokens. McKinley argues against 'best tool for the job' thinking, emphasizing that a company's real job is staying in business and the best tool occupies the 'least worst' position across as many problems as possible.

hackernews · tosh · Aug 13, 17:48 · [Discussion](https://news.ycombinator.com/item?id=49289512)

**Background**: Dan McKinley developed this philosophy during his six years as a software engineer at Etsy, where the engineering team was known for high productivity despite using what many considered 'boring' technology choices. The concept of 'innovation tokens' emerged from observing that adopting new technologies introduces hidden costs in training, debugging, infrastructure, and operational complexity that aren't apparent during initial selection. The essay challenges the common engineering tendency to chase cutting-edge technologies for their own sake, arguing that mature, well-understood technologies often provide better business value precisely because their failure modes are known and documented.

<details><summary>References</summary>
<ul>
<li><a href="https://mcfunley.com/choose-boring-technology">Choose Boring Technology - Dan McKinley</a></li>
<li><a href="https://mattrickard.com/innovation-tokens">Innovation Tokens | Matt Rickard</a></li>
<li><a href="https://www.linkedin.com/pulse/technical-debt-innovation-tokens-case-boring-technology-jeffrey-henry-lhexe">Technical Debt, Innovation Tokens , and the Case for Boring...</a></li>

</ul>
</details>

**Discussion**: The discussion shows strong support for the essay's core message, with one commenter calling it mandatory teaching for any engineer and another praising 'innovation tokens' as an invaluable tool for explaining tradeoffs to colleagues at all levels. A notable counterpoint suggests applying the framework to AI agents by concentrating all innovation tokens there while keeping the surrounding tech stack boring, essentially using 'in-distribution technology' that agents handle best. However, there is also pushback against the concept, with one commenter arguing that 'innovation tokens' is an arbitrary and unserious framework, and that engineers should instead focus on understanding requirements, risks, tradeoffs, and potential gains when evaluating any technology.

**Tags**: `#engineering-management`, `#technology-selection`, `#software-architecture`, `#ai-agents`, `#best-practices`

---

<a id="item-8"></a>
## [DeepSeek Harness Developer Preview Released](https://deepseek.com/harness/en/) ⭐️ 8.0/10

DeepSeek has released a developer preview of DeepSeek Harness, an MIT-licensed open-source agent framework where every capability — models, tools, sessions, sandboxes, storage, scheduling, and UI — is a swappable plugin. The framework is built on Cordis v4, a newly released plugin architecture paper that enables hot-reloading and dynamic loading/unloading of plugins without restarting the running process. The framework's fully traceable session logs — recording system prompts, reasoning, tool calls, subagent scheduling, and context injections in an append-only event stream — are highlighted as a differentiator from US-based models whose traces are often encrypted or obfuscated. This level of transparency enables resume, fork, search, and replay operations on agent trajectories, which is valuable for debugging, auditing, and building trust in agent systems. Cordis v4 has prior production use: it was used for four years in a different project called Koishi (using v3), and the framework's algebraic approach to spatiotemporal composability allows plugins to revert state and side effects upon unloading, including cleaning up connections, memory allocations, and registered handlers. The project is explicitly an early developer preview with expected rough edges and compatibility-breaking changes, and one commenter noted the underlying paper is useful but not revolutionary for those with PLT (programming language theory) knowledge.

hackernews · bjin · Aug 13, 12:58 · [Discussion](https://news.ycombinator.com/item?id=49285244)

**Background**: Agent frameworks are software systems that orchestrate LLM-powered agents to perform tasks by managing tool calls, context, and multi-step reasoning. A key challenge in agent development is observability — understanding what the model saw, decided, and did at each step. Cordis is an AOP (Aspect-Oriented Programming) framework for JavaScript applications that manages plugin states and contexts, and its v4 paper describes a programming paradigm for "spatiotemporal composability" — the ability to compose, load, and unload components dynamically while properly managing their state and side effects.

<details><summary>References</summary>
<ul>
<li><a href="https://www.deepseek.com/harness/en/">DeepSeek Harness developer preview: Everything is a plugin</a></li>
<li><a href="https://github.com/deepseek-ai/deepseek-harness">GitHub - deepseek-ai/deepseek-harness: DeepSeek Harness ...</a></li>
<li><a href="https://npm.io/package/cordis">Cordis NPM | npm.io</a></li>

</ul>
</details>

**Discussion**: Community sentiment is cautiously positive, with users praising the fully traceable session logs as a "killer feature" that differentiates the framework from US models with encrypted traces. A project author (tianyicui) acknowledged this is an early preview with rough edges, while technical commenters discussed Cordis v4's hot-reload and state cleanup capabilities, with one noting the approach is useful but incremental rather than paradigm-shifting for those familiar with programming language theory.

**Tags**: `#deepseek`, `#agent-framework`, `#cordis`, `#traceability`, `#developer-tools`

---

<a id="item-9"></a>
## [Trump Memo Authorizes Private Firms to Conduct State-Backed Overseas Cyberattacks](https://www.bloomberg.com/news/articles/2026-08-13/trump-enlists-private-sector-to-boost-cyber-offensive-arsenal) ⭐️ 8.0/10

Former U.S. President Donald Trump signed a memorandum authorizing federally supervised private companies to conduct overseas surveillance and cyberattacks against transnational criminal organizations targeting Americans. The Department of Homeland Security will run the program in coordination with the Department of Justice, and participating firms must maintain a minimum $1 million bond or escrow deposit. This policy reversal sweeps away decades of U.S. cybersecurity norms that prohibited private companies from conducting offensive cyber operations or 'hack back' attacks. It marks a fundamental shift in statecraft by officially enlisting the private sector into state-backed offensive cyber operations, which could reshape the cybersecurity industry and unsettle international norms around cyber warfare. Participating companies must operate under direct federal control and supervision, with a $1 million bond or escrow requirement that can be forfeited for non-compliance with contractual obligations. The legal basis for authorizing private offensive cyber operations remains untested in courts, raising questions about how this authority will hold up under judicial scrutiny.

telegram · zaihuapd · Aug 13, 05:10

**Background**: For decades, U.S. cybersecurity policy has prohibited private companies from conducting 'hack back' operations or offensive cyberattacks, reserving such activities for government agencies and military entities. The Trump administration's National Cybersecurity Strategy explicitly envisioned an expanded role for the private sector in offensive cyber operations. This memorandum represents the first time the U.S. government has formally authorized vetted private firms to carry out offensive cyber operations, breaking with long-standing policy.

<details><summary>References</summary>
<ul>
<li><a href="https://techcrunch.com/2026/08/13/in-a-first-us-will-allow-some-private-firms-to-carry-out-cyberattacks/">In a first, US will allow some private firms to carry out ...</a></li>
<li><a href="https://www.techtimes.com/articles/324283/20260813/trump-authorizes-private-firms-hack-foreign-criminals-legal-basis-untested-courts.htm">Trump Authorizes Private Firms to Hack Foreign Criminals ...</a></li>
<li><a href="https://www.lawfaremedia.org/article/trump-admin-cyber-strategy-centers-private-sector-in-offensive-cyber-operations">Trump Admin Cyber Strategy Centers Private Sector in ...</a></li>

</ul>
</details>

**Tags**: `#cybersecurity`, `#policy`, `#government`, `#offensive-security`, `#private-sector`

---

<a id="item-10"></a>
## [DeepMind's SL2T Brings Sign Language Translation to Pixel 11](https://deepmind.google/blog/putting-sign-language-ai-into-users-hands/) ⭐️ 8.0/10

Google DeepMind has introduced SL2T, a large-scale multilingual sign-language-to-text model, now deployed on Pixel 11 devices to power American Sign Language (ASL) translation in Gboard and Live Transcribe. The model was trained on over 100,000 hours of data across more than 50 sign languages and achieved a zero-shot score of 70 BLEURT on the FLEURS-ASL benchmark, significantly surpassing previous records. This marks the first time sign language AI translation has been integrated into mainstream consumer products, representing a major milestone in accessibility technology for Deaf and hard-of-hearing users. The deployment on widely available devices like the Pixel 11 demonstrates that real-time sign language translation is technically feasible at the consumer level, potentially paving the way for broader adoption across more devices and languages. To protect user privacy, SL2T processes only hand and body pose keypoints rather than raw video footage. Currently, the model is limited to ASL-to-English translation and is available only on Pixel 11 devices, with plans to expand to additional languages and devices in the future.

telegram · zaihuapd · Aug 13, 08:55

**Background**: Sign language translation has historically been peripheral to mainstream machine translation research, partly due to the lack of standardized benchmarks. FLEURS-ASL, introduced in 2024, extends the multilingual FLORES/FLEURS benchmarks to support American Sign Language as video, translated by Certified Deaf Interpreters, helping bridge the gap between sign language and text-based machine translation. BLEURT is a learned evaluation metric based on BERT that measures how well a generated translation conveys the meaning and fluency of a reference sentence, serving as a more human-judgment-correlated alternative to traditional metrics like BLEU.

<details><summary>References</summary>
<ul>
<li><a href="https://deepmind.google/blog/putting-sign-language-ai-into-users-hands/">Putting sign language AI into users’ hands</a></li>
<li><a href="https://siliconangle.com/2026/08/12/google-debuts-sl2t-ai-model-thats-designed-understand-sign-language/">Google debuts SL2T, an AI model that's designed to understand sign language - SiliconANGLE</a></li>
<li><a href="https://arxiv.org/abs/2408.13585">FLEURS-ASL: Including American Sign Language in Massively ... Title:FLEURS-ASL: Including American Sign Language in ... [PDF] FLEURS-ASL: Including American Sign Language in ... (PDF) FLEURS-ASL: Including American Sign Language in ... AITopics | FLEURS-ASL: Including American Sign Language in ...</a></li>
<li><a href="https://github.com/google-research/bleurt">GitHub - google-research/bleurt: BLEURT is a metric for ...</a></li>

</ul>
</details>

**Tags**: `#Google DeepMind`, `#Sign Language Translation`, `#Accessibility AI`, `#SL2T`, `#Pixel`

---
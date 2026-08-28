---
layout: default
title: "Horizon Summary: 2026-08-28 (EN)"
date: 2026-08-28
lang: en
---

> From 30 items, 6 important content pieces were selected

---

1. [Claude Code Opus 5 Auto Mode Bypassed via Zip Archive Prompt Injection](#item-1) ⭐️ 9.0/10
2. [Nvidia Reports $96.2B Quarterly Revenue with Unprecedented 70% One-Year Forward Guidance](#item-2) ⭐️ 9.0/10
3. [Anthropic Opens Model Hardware Standard Preview for AI-Controlled Physical Devices](#item-3) ⭐️ 9.0/10
4. [Cloudflare saves 100TB of memory by optimizing 1.1.1.1 DNS cache](#item-4) ⭐️ 8.0/10
5. [OpenAI Developing Persistent Codex Agent That Works Until Sleep](#item-5) ⭐️ 8.0/10
6. [🤖 美国法官叫停五角大楼拉黑 Anthropic](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Claude Code Opus 5 Auto Mode Bypassed via Zip Archive Prompt Injection](https://simonwillison.net/2026/Aug/27/breaking-claude-code-opus-5-auto-mode/) ⭐️ 9.0/10

Security researcher Johann Rehberger demonstrated a prompt injection attack that bypasses Claude Code Opus 5's auto mode safety features with an 80% success rate. The attack tricks the agent into downloading and extracting a zip archive containing a malicious local struct.py file, which gets executed when the agent imports the standard base64 module. This vulnerability reveals a critical blind spot in Anthropic's auto mode, which was recently made the default for Claude Code and has been promoted with bold claims about its security effectiveness. The finding demonstrates that classifier-based safety mechanisms can be reliably bypassed through subtle Python import path manipulation, and worse, can even block cleanup attempts once a compromise is detected. The exploit leverages Python's local import precedence: when a script imports base64, Python first checks the current directory and finds the malicious struct.py extracted from the zip archive, executing it instead of the standard library version. In some test runs, auto mode's classifier allowed the malware process to start but then blocked Claude's own cleanup commands, making the safety mechanism itself part of the failure.

rss · Simon Willison · Aug 27, 22:50

**Background**: Claude Code's auto mode routes tool calls through a classifier that is designed to block anything irreversible, destructive, or aimed outside the user's environment, allowing the agent to run autonomously without routine permission prompts. Anthropic recently made auto mode the default for Pro, Max, and Team plans, placing significant trust in this mechanism as the primary defense against prompt injection attacks. Prompt injection is a class of vulnerability where adversarial inputs manipulate an LLM agent's tool selection or parameters, abusing the agent's privileges through its own tool-calling capabilities.

<details><summary>References</summary>
<ul>
<li><a href="https://code.claude.com/docs/en/auto-mode-config">Configure auto mode - Claude Code Docs</a></li>
<li><a href="https://claude.com/blog/auto-mode-default-in-claude-code">Auto mode is now the default in Claude Code for Pro, Max, and Team plans | Claude by Anthropic</a></li>
<li><a href="https://www.mdpi.com/2078-2489/17/1/54">Prompt Injection Attacks in Large Language Models and AI Agent Systems: A Comprehensive Review of Vulnerabilities, Attack Vectors, and Defense Mechanisms</a></li>

</ul>
</details>

**Tags**: `#prompt-injection`, `#ai-security`, `#claude-code`, `#llm-agents`, `#vulnerability`

---

<a id="item-2"></a>
## [Nvidia Reports $96.2B Quarterly Revenue with Unprecedented 70% One-Year Forward Guidance](https://mp.weixin.qq.com/s/JTZ_ZJ_pn5vgrI_1QUyWNw) ⭐️ 9.0/10

Nvidia reported $96.2 billion in quarterly revenue for Q2 FY2027, up 106% year-over-year, with data center revenue reaching $89 billion. CFO Colette Kress provided an unprecedented one-year forward guidance of approximately 70% growth for FY2028, explicitly stating that this figure is constrained by supply rather than demand. This unprecedented forward guidance signals a major inflection point for the AI industry, demonstrating that explosive demand for AI computing power shows no signs of slowing down. The supply-constrained growth outlook and the launch of the next-generation Vera Rubin platform will have profound implications for the entire semiconductor supply chain and AI ecosystem. The next-generation Vera Rubin platform has already begun mass production and shipping this month, and is expected to contribute approximately 20% of data center revenue in the current quarter. The Vera Rubin platform is a multi-rack pod-scale system built for agentic AI, featuring extreme co-design across six new chips including the Vera CPU, Rubin GPU, NVLink 6 Switch, and BlueField-4 DPU.

telegram · zaihuapd · Aug 27, 08:51

**Background**: Nvidia's fiscal year naming differs from calendar years, with FY2027 corresponding to a period of explosive AI-driven growth following the widespread adoption of large language models. Forward guidance is a practice where companies provide investors with expectations about future financial performance, and providing a one-year-ahead forecast is highly unusual in the semiconductor industry. The Vera Rubin platform represents Nvidia's next-generation architecture succeeding Blackwell, designed to handle the increasing computational demands of agentic AI and large-scale reasoning workloads.

<details><summary>References</summary>
<ul>
<li><a href="https://www.nvidia.com/en-us/data-center/technologies/rubin/">Infrastructure for Scalable AI Reasoning | NVIDIA Vera Rubin Platform</a></li>
<li><a href="https://www.linkedin.com/posts/utsav-pandya-23770471_ai-technews-nvidia-activity-7416495154779348992--8Lc">NVIDIA Unveils Vera Rubin Platform for AI Supercomputing | LinkedIn</a></li>

</ul>
</details>

**Tags**: `#Nvidia`, `#AI`, `#Data Center`, `#Earnings`, `#Semiconductors`

---

<a id="item-3"></a>
## [Anthropic Opens Model Hardware Standard Preview for AI-Controlled Physical Devices](https://www.anthropic.com/news/model-hardware-standard-research-preview) ⭐️ 9.0/10

Anthropic has released a research preview of its Model Hardware Standard (MHS), a shared specification that enables AI agents to safely operate physical laboratory and manufacturing equipment such as microscopes, liquid handlers, and robotic arms. The standard dramatically reduces device integration time from weeks or months down to hours or even minutes, with early partners including Genentech, Carnegie Mellon University, and QuEra already demonstrating successful deployments across biotechnology, robotics, and quantum computing. This announcement marks a major AI lab's push from digital interfaces into the physical world, potentially transforming laboratory automation, advanced manufacturing, and scientific research by enabling autonomous AI agents to directly control hardware. By standardizing the communication protocol between AI models and physical devices, MHS could eliminate the costly custom integration bottleneck that has historically slowed adoption of AI-driven automation in scientific and industrial settings. QuEra's AI controller, built using MHS, can restore quantum computer laser locking without human intervention in 99.3% of cases, turning a task that previously required expert on-call visits into an automated process completed in seconds. Anthropic plans to open-source the standard after completing safety evaluations, and the current research preview is limited to a first group of scientific research labs and advanced manufacturers.

telegram · zaihuapd · Aug 28, 01:38

**Background**: The Model Hardware Standard (MHS) addresses a fundamental challenge in laboratory and industrial automation: traditionally, integrating an AI system with a piece of physical equipment requires custom software development that can take weeks to months per device. MHS provides a shared specification—a common interface protocol—that any AI agent can use to communicate with any MHS-compliant device, analogous to how USB standards unified peripheral connectivity. QuEra Computing, one of the early partners, builds quantum computers using neutral atoms based on research from Harvard and MIT, where maintaining laser lock has been a persistent operational challenge requiring expert intervention. The research preview involves partners across biotechnology (Genentech), academic robotics (Carnegie Mellon University), and quantum computing (QuEra), demonstrating the standard's cross-domain applicability.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/news/model-hardware-standard-research-preview">Previewing the Model Hardware Standard \ Anthropic</a></li>
<li><a href="https://www.cnbc.com/2026/08/27/anthropic-pushes-into-physical-world-with-new-standard-to-help-ai-agents-operate-machines.html">Anthropic pushes into physical world with new standard to help AI agents operate machines</a></li>
<li><a href="https://quantumzeitgeist.com/anthropic-ai-tunes-quantum-lasers-queras/">QuEra ’s AI Now Tunes Quantum Lasers In Seconds, Not Minutes</a></li>

</ul>
</details>

**Tags**: `#Anthropic`, `#AI Hardware Integration`, `#Laboratory Automation`, `#Robotics`, `#Model Hardware Standard`

---

<a id="item-4"></a>
## [Cloudflare saves 100TB of memory by optimizing 1.1.1.1 DNS cache](https://blog.cloudflare.com/dns-cache-memory-optimization-1111/) ⭐️ 8.0/10

Cloudflare engineers applied five Rust-level memory optimizations to the DNS cache layout of their internal resolver, code-named Big Pineapple, reducing per-entry memory usage by 56% and freeing approximately 100 TB of memory across their global fleet. The optimizations focused on internal data structures and memory allocation patterns rather than algorithmic changes. At Cloudflare's massive scale, even small per-entry memory savings compound into enormous infrastructure cost reductions, directly improving the efficiency of one of the world's fastest public DNS resolvers. This demonstrates that low-level systems programming and memory layout optimization remain critical competitive levers for large-scale internet infrastructure. The five optimizations were implemented in Rust and targeted the cache entry layout and allocation strategy of the Big Pineapple DNS resolver. Some community members noted that additional optimizations might still be possible, such as placing record data directly after CacheEntry members to avoid separate allocations, though this can be more challenging in Rust's ownership model.

hackernews · TangerineDream · Aug 27, 17:17 · [Discussion](https://news.ycombinator.com/item?id=49468083)

**Background**: Cloudflare's 1.1.1.1 is a free, privacy-first public DNS resolver that operates across hundreds of cities worldwide and is measured as one of the fastest DNS resolvers available. A DNS resolver caches domain name records to speed up subsequent queries, and at the scale of handling billions of queries per day, the memory footprint of each cached entry becomes a significant operational concern. The optimizations were applied to Big Pineapple, Cloudflare's Rust-based DNS resolver that powers the 1.1.1.1 service.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.cloudflare.com/dns-cache-memory-optimization-1111/">How we saved 100 terabytes of memory by optimizing 1.1.1.1’s DNS ...</a></li>
<li><a href="https://developers.cloudflare.com/1.1.1.1/">1 . 1 . 1 . 1 ( DNS Resolver ) · Cloudflare 1 . 1 . 1 . 1 docs</a></li>
<li><a href="https://news.ycombinator.com/item?id=49468083">Saving 100 terabytes of memory by optimizing 1.1.1.1's DNS cache</a></li>

</ul>
</details>

**Discussion**: The discussion highlighted strong appreciation for systems programming, with commenters noting that these types of memory optimizations—such as struct alignment, custom allocators, and single large malloc() calls instead of per-entry allocations—are well-known but powerful techniques. Several commenters pointed out potential additional optimizations Cloudflare could pursue, such as co-locating record data with CacheEntry structs, while one commenter observed that merging distinct lists into a single allocation might undercut Rust's safety guarantees. The overall sentiment was that while these optimizations are considered standard by experts, they deliver massive real-world impact at Cloudflare's scale.

**Tags**: `#systems-programming`, `#optimization`, `#dns`, `#memory`, `#cloudflare`

---

<a id="item-5"></a>
## [OpenAI Developing Persistent Codex Agent That Works Until Sleep](https://www.wired.com/story/openai-is-developing-a-persistent-ai-agent/) ⭐️ 8.0/10

OpenAI is developing a 'persistent mode' for its command-line Codex agent that enables it to continuously work, autonomously create follow-up tasks across sessions, and operate until explicitly put to 'sleep' by the user. The mode includes built-in proactivity, allowing the agent to decide what to work on based on its knowledge of the user, while still requiring prior approval for changes outside the user's system. This represents a major shift from reactive AI coding assistants that stop after completing a single prompt toward persistent, autonomous agents capable of long-term task execution. It could fundamentally transform software development workflows by enabling AI to proactively manage and execute multi-step projects across sessions. The persistent mode appears in Codex's 'reasoning effort' menu, where users select the level of computing power, tokens, and time allocated for the model to think before answering. OpenAI has confirmed it is testing the feature but stated there are no near-term plans for release.

telegram · zaihuapd · Aug 28, 02:47

**Background**: OpenAI released Codex CLI on April 16, 2025, as an open-source coding agent that runs locally in the terminal, connecting language models with local code and command-line tasks. It can write and edit code, execute commands, and interact with files through a lightweight interface. Current AI agents typically operate in a request-response pattern, stopping after completing a task within minutes or hours, whereas persistent memory and state architectures allow agents to retain facts, user preferences, and domain knowledge across independent sessions.

<details><summary>References</summary>
<ul>
<li><a href="https://www.wired.com/story/openai-is-developing-a-persistent-ai-agent/">OpenAI Is Developing a ‘Persistent’ AI Agent | WIRED</a></li>
<li><a href="https://en.wikipedia.org/wiki/OpenAI_Codex_(AI_agent)">OpenAI Codex (AI agent) - Wikipedia</a></li>
<li><a href="https://github.com/openai/codex">GitHub - openai/codex: Lightweight coding agent that runs in your terminal · GitHub</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#Codex`, `#AI Agents`, `#Autonomous Systems`, `#Software Engineering`

---

<a id="item-6"></a>
## [🤖 美国法官叫停五角大楼拉黑 Anthropic](https://www.bloomberg.com/news/articles/2026-08-28/anthropic-wins-court-challenge-to-us-supply-chain-risk-label?srnd=phx-technology) ⭐️ 8.0/10

A US federal judge has blocked the Pentagon's ban on Anthropic, ruling that labeling the company a supply chain risk lacked sufficient basis and appeared retaliatory.

telegram · zaihuapd · Aug 28, 03:15

**Tags**: `#Anthropic`, `#AI Policy`, `#Legal`, `#Government`, `#Defense`

---
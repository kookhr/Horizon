---
layout: default
title: "Horizon Summary: 2026-09-30 (EN)"
date: 2026-09-30
lang: en
---

> From 40 items, 8 important content pieces were selected

---

1. [GPT 6.1 Sol: Near-Astra intelligence for a fifth of the price](#item-1) ⭐️ 9.0/10
2. [AMD 将以 82 亿美元收购李飞飞创办的 World Labs](#item-2) ⭐️ 9.0/10
3. [OpenAI DevDay 2026 Announces Dots Agent and 20+ Major Updates](#item-3) ⭐️ 9.0/10
4. [Research Paper Analyzes Privacy Vulnerabilities in Conversational AI Agents](#item-4) ⭐️ 8.0/10
5. [AI Models Cross Threshold in Binary Exploitation, Says Anthropic Red Team](#item-5) ⭐️ 8.0/10
6. [OpenAI DevDay 2026 live blog](#item-6) ⭐️ 8.0/10
7. [Free Open-Source Book on ML Performance Engineering from Silicon to Agents](#item-7) ⭐️ 8.0/10
8. [Anthropic Evaluates GLM-5.3's Cyber Attack Capabilities](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [GPT 6.1 Sol: Near-Astra intelligence for a fifth of the price](https://simonwillison.net/2026/Sep/29/hn-49898129/) ⭐️ 9.0/10

OpenAI announces GPT 6.1 Sol at DevDay 2026, offering near-Astra intelligence at one-fifth of the price, with Simon Willison providing visual analysis comparing it to the GPT-6 family.

rss · Simon Willison · Sep 29, 18:27

**Tags**: `#openai`, `#gpt-6.1`, `#llm`, `#ai-models`, `#devday`

---

<a id="item-2"></a>
## [AMD 将以 82 亿美元收购李飞飞创办的 World Labs](https://ir.amd.com/news-events/press-releases/detail/1299/amd-to-acquire-world-labs-to-advance-the-future-of-ai-compute) ⭐️ 9.0/10

AMD announced an $8.2 billion acquisition of World Labs, the world model AI company founded by Fei-Fei Li, who will join AMD as EVP and Chief Scientist to integrate world model capabilities with AMD's compute platforms.

telegram · zaihuapd · Sep 29, 03:59

**Tags**: `#AMD`, `#World Labs`, `#Fei-Fei Li`, `#AI Acquisition`, `#World Models`

---

<a id="item-3"></a>
## [OpenAI DevDay 2026 Announces Dots Agent and 20+ Major Updates](https://openai.com/zh-Hant/index/devday-2026-recap/) ⭐️ 9.0/10

At DevDay 2026, OpenAI announced over 20 major updates including Dots, a persistent autonomous agent that runs 24/7 and proactively manages long-term complex tasks, alongside GPT-6.1 Sol optimized for coding at one-fifth of Astra's price, Astra Ultrafast with up to 8x speed improvements, new Agents API and Decisions API, cloud-based Codex with voice control, 'Sign in with ChatGPT' for third-party quota sharing, and a new Pro 500 tier offering 25x the compute of Plus.

telegram · zaihuapd · Sep 29, 17:52

**Tags**: `#OpenAI`, `#AI Agents`, `#GPT-6.1`, `#Developer API`, `#DevDay 2026`

---

<a id="item-4"></a>
## [Research Paper Analyzes Privacy Vulnerabilities in Conversational AI Agents](https://jorgegarciaherrero.com/wp-content/interactivos/20260916-Prompt-like-a-butterfly-sting-like-a-tracker-(clean).pdf) ⭐️ 8.0/10

A research paper was published providing a systematic privacy analysis of web and mobile conversational AI agents, examining how user data is tracked and potentially exposed through these platforms. The paper investigates data collection practices, ad tracker integrations, and conversation exposure vulnerabilities across popular AI chat services. As conversational AI agents become deeply embedded in daily workflows, users routinely share sensitive personal and professional information with these platforms, often without understanding the privacy implications. This research exposes systemic privacy weaknesses that could affect millions of users and pressures AI companies to adopt stronger data protection practices. The analysis covers multiple attack surfaces including real-time transmission of unfinished prompts to servers, conversation histories exposed via predictable UUID-based URLs, and integration of third-party ad trackers within AI chat interfaces. The paper examines both web and mobile platforms, noting that mobile agents may present additional tracking vectors due to broader system-level permissions.

hackernews · damaru2 · Sep 29, 09:03 · [Discussion](https://news.ycombinator.com/item?id=49890226)

**Background**: Conversational AI agents such as ChatGPT, Perplexity, and similar services process user inputs in real-time, often sending data to remote servers for inference and caching. While these platforms are widely used for productivity and information retrieval, their underlying data handling practices—including prompt transmission, conversation storage, and third-party tracker integration—are often opaque to users. Privacy researchers have increasingly focused on how these systems handle sensitive data, particularly as AI companies face competing pressures between data hoarding for model improvement and user privacy protection.

**Discussion**: The community discussion surfaced several concrete privacy observations, including ChatGPT periodically sending unfinished prompts to a `conversation/prepare` endpoint before user submission, and Perplexity exposing full conversations via predictable UUID URLs. Commenters debated whether open-weight models are the ultimate solution to privacy concerns, with some arguing that local execution eliminates the need to trust third-party servers, while others expressed surprise that AI companies integrate ad trackers that benefit direct competitors.

**Tags**: `#privacy`, `#conversational-ai`, `#security`, `#data-tracking`, `#ai-agents`

---

<a id="item-5"></a>
## [AI Models Cross Threshold in Binary Exploitation, Says Anthropic Red Team](https://simonwillison.net/2026/Sep/29/anthropic-frontier-red-team/) ⭐️ 8.0/10

Anthropic's Frontier Red Team reports that GLM-5.3 and Claude Mythos Preview achieved 4% and 6% success rates respectively on control flow hijack tasks from an internal Binary Exploitation benchmark, marking the first time AI models have succeeded on these tasks where earlier models like Claude Opus 4.6 and GLM-5.2 had zero success. This represents a meaningful capability threshold being crossed in offensive cybersecurity, indicating that frontier AI models are beginning to acquire practical binary exploitation skills that were previously exclusive to skilled human security researchers. The proliferation of such capabilities raises significant concerns about AI safety, cybersecurity, and the potential for large-scale misuse of offensive cyber tools. The evaluation used 100 randomly selected tasks from Anthropic's internal Binary Exploitation benchmark, focusing specifically on full control flow hijacks. While the success rates remain low (4-6%), the transition from zero to non-zero success is qualitatively significant because it demonstrates these models can now complete the full chain of reasoning and execution required for binary exploitation.

rss · Simon Willison · Sep 29, 22:20

**Background**: Binary exploitation is the process of subverting compiled programs to make them execute unintended code, often by manipulating memory or program logic. Control flow hijacking is a specific technique where an attacker redirects a program's execution flow to malicious code, bypassing normal program behavior. Anthropic's Frontier Red Team is a dedicated group that stress-tests AI systems to understand their current capabilities and anticipate future risks, particularly in cybersecurity and national security domains.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/research/team/frontier-red-team">Frontier Red Team Research \ Anthropic</a></li>
<li><a href="https://trailofbits.github.io/ctf/exploits/binary1.html">Binary Exploits 1 - CTF Field Guide</a></li>
<li><a href="https://www.geeksforgeeks.org/ethical-hacking/control-hijacking/">Control Hijacking - GeeksforGeeks</a></li>

</ul>
</details>

**Tags**: `#ai-security`, `#anthropic`, `#binary-exploitation`, `#frontier-models`, `#cyber-capabilities`

---

<a id="item-6"></a>
## [OpenAI DevDay 2026 live blog](https://simonwillison.net/2026/Sep/29/openai-devday-2026-live-blog/) ⭐️ 8.0/10

Simon Willison live blogs OpenAI DevDay 2026 in San Francisco, covering keynote announcements and developments from the major AI conference.

rss · Simon Willison · Sep 29, 15:55

**Tags**: `#openai`, `#ai`, `#llms`, `#generative-ai`, `#devday`

---

<a id="item-7"></a>
## [Free Open-Source Book on ML Performance Engineering from Silicon to Agents](https://www.reddit.com/r/MachineLearning/comments/1wt6ns4/i_wrote_a_free_opensource_book_on_making_ml/) ⭐️ 8.0/10

A new free, open-source book titled "How to Make Your Model Fast: A Systems View of Efficient Machine Learning, from Silicon to Agents" has been released on GitHub, covering the full optimization stack from hardware-level roofline analysis to agent-level performance. The author spent months compiling a resource that walks through kernels, compilers, quantization, pruning, on-device LLMs, robotics, profiling, serving, and agents. This resource fills a critical gap in ML education by emphasizing that reducing FLOPs alone does not guarantee faster models—one must first identify whether a system is compute, bandwidth, memory, or system bound. It provides practitioners with the intuition to reason about theoretical performance ceilings and select optimizations that actually move the needle, which is increasingly important as ML deployment spans from edge devices to large-scale serving infrastructure. The book is structured around roofline analysis as a foundational tool, then progressively moves up the stack through kernels, compilers, quantization, pruning, and application domains including vision, on-device LLMs, and robotics. It is hosted at https://github.com/usamahz/make-your-model-fast and the author actively solicits feedback and contributions from practitioners in ML systems, inference, compilers, edge AI, and performance engineering.

reddit · r/MachineLearning · /u/SoloTiger_ · Sep 29, 10:35

**Background**: The roofline model is a performance analysis framework that plots peak achievable FLOPs/s (throughput) against arithmetic intensity (operations per byte of data moved), visually revealing whether an application is compute-bound or memory-bandwidth-bound. In deep learning, models are essentially large collections of matrix multiplications composed of floating-point operations, and understanding whether these operations are limited by compute capacity or data movement is essential for effective optimization. The roofline model provides theoretical upper bounds based on machine peak performance and peak bandwidth, allowing developers to track progress toward optimality and identify bottlenecks in their implementations. This systems-level thinking—understanding what actually limits performance before optimizing—is the core philosophy of the book.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Roofline_model">Roofline model - Wikipedia</a></li>
<li><a href="https://jax-ml.github.io/scaling-book/roofline/">All About Rooflines | How To Scale Your Model</a></li>
<li><a href="https://docs.nersc.gov/tools/performance/roofline/">Roofline Performance Model - NERSC Documentation</a></li>

</ul>
</details>

**Tags**: `#Machine Learning`, `#Performance Engineering`, `#Systems Design`, `#Open Source`, `#ML Optimization`

---

<a id="item-8"></a>
## [Anthropic Evaluates GLM-5.3's Cyber Attack Capabilities](https://www.anthropic.com/research/glm-5-3-and-the-spread-of-advanced-cyber-capabilities) ⭐️ 8.0/10

Anthropic's security assessment found that Zhipu AI's GLM-5.3 can autonomously conduct end-to-end cyber attacks, succeeding 50 out of 410 attempts in ExploitBench — close to Claude Mythos Preview's 56 successes. The assessment also revealed that GLM-5.3's safety guardrails can be bypassed with simple methods at a 64–100% success rate, and its open-weight nature allows users to further weaken refusal mechanisms. This finding highlights the growing risk of advanced offensive cyber capabilities proliferating through open-weight models, which are freely accessible and modifiable by anyone. As open-source models approach the cyber attack proficiency of tightly controlled proprietary models like Claude Mythos, the barrier to entry for malicious actors conducting sophisticated cyber attacks is significantly lowered. ExploitBench evaluates LLM agents on full-control V8 exploit synthesis using 16 measured exploit capability flags, targeting the V8 JavaScript engine inside Chrome, Edge, Node.js, and Cloudflare Workers. GLM-5.3 was released by Zhipu AI on August 14, 2026, supports a 1M token context window, and claims coding and AI agent capabilities approaching Claude Fable 5.

telegram · zaihuapd · Sep 29, 23:58

**Background**: ExploitBench is a cybersecurity benchmark designed to evaluate how well LLM agents can discover and synthesize full-control exploits against V8, the JavaScript and WebAssembly engine used in Chrome, Edge, Node.js, and Cloudflare Workers. Claude Mythos Preview is Anthropic's internal model demonstrating striking capabilities in computer security tasks; due to its capabilities, Anthropic has restricted access to a small group of vetted partners. GLM-5.3 is the latest open-weight model from Zhipu AI (Z.ai), a Chinese AI startup, released on August 14, 2026, with a 1M token context window and coding capabilities approaching Claude Fable 5. Open-weight models differ from closed models in that their parameters are publicly available, allowing users to inspect, modify, and fine-tune them — including removing safety guardrails.

<details><summary>References</summary>
<ul>
<li><a href="https://exploitbench.ai/">ExploitBench</a></li>
<li><a href="https://www.anthropic.com/research/mythos-preview">Claude Mythos Preview's cybersecurity capabilities \ Anthropic</a></li>
<li><a href="https://emergent.sh/news/glm-53-officially-launched">Zhipu AI Launches GLM-5.3: New LLM Specs & Features</a></li>

</ul>
</details>

**Tags**: `#AI Safety`, `#Cybersecurity`, `#LLM Evaluation`, `#Anthropic`, `#Open Weight Models`

---
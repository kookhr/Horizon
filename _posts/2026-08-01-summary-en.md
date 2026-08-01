---
layout: default
title: "Horizon Summary: 2026-08-01 (EN)"
date: 2026-08-01
lang: en
---

> From 41 items, 5 important content pieces were selected

---

1. [OpenAI Astra Breaks Through on Ten Long-Standing Math Problems](#item-1) ⭐️ 10.0/10
2. [EA 550 亿美元卖身沙特财团，下周正式完成](#item-2) ⭐️ 9.0/10
3. [DeepSeek Releases V4-Flash-0731: Top Value-per-Intelligence Open-Weight LLM](#item-3) ⭐️ 8.0/10
4. [MCP 2.0 Goes Stateless, Reigniting Ecosystem Interest](#item-4) ⭐️ 8.0/10
5. [Microsoft Confirms Copilot 'Super App' Launch This Year](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI Astra Breaks Through on Ten Long-Standing Math Problems](https://openai.com/index/ten-advances-in-mathematics/) ⭐️ 10.0/10

OpenAI announced that an internal version of its next-generation model Astra has produced new results on ten long-unsolved problems in mathematics and theoretical computer science, including the Connes rigidity conjecture, non-sofic group existence, multicolor Ramsey numbers, and arithmetic circuit lower bounds. The proofs were formalized and verified in Lean 4, with each problem costing approximately $2,000 in tokens at GPT-5.6 Sol pricing. This represents a potential paradigm shift in which AI serves not merely as a tool but as a genuine research collaborator in pure mathematics, a domain long considered resistant to automation. The fact that these problems had seen no major progress for at least a decade—and that proofs were formally verified—signals that AI may accelerate discovery in the most abstract fields of human knowledge. OpenAI released a GitHub repository (openai/ten-proofs) with Lean 4 formalizations, a paper describing the solutions, and an LLM-generated PDF reconstructing the model's reasoning traces. The company acknowledged that the mathematical arguments were AI-generated while humans handled organization and formalization, and openly invited the mathematical community to scrutinize the results.

telegram · zaihuapd · Aug 1, 07:59

**Background**: Lean is a proof assistant and functional programming language based on the calculus of inductive constructions, developed since 2013 and now maintained by the nonprofit Lean FRO. It allows mathematicians to write proofs that are mechanically verified, eliminating the risk of human error in complex arguments. The problems addressed—such as the Connes rigidity conjecture (about von Neumann algebras of higher-rank lattices) and the existence of non-sofic groups (groups that cannot be approximated by finite symmetric groups)—are deep questions in pure mathematics and theoretical computer science that have resisted conventional approaches for decades.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Lean_(proof_assistant)">Lean (proof assistant)</a></li>
<li><a href="https://en.wikipedia.org/wiki/Sofic_group">Sofic group - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Simon Willison praised the transparency of releasing formalized proofs and reasoning traces but noted he still wants to see the actual prompts used. He also pointed out the absence of information on how many problems were attempted without reaching a solution. Many mathematicians online described a collective 'Deep Blue' moment, while the discussion referenced Terence Tao's vision of 'big mathematics'—large-scale human-AI collaborations where humans handle creative decisions and AI handles technical grunt work.

**Tags**: `#AI-mathematics`, `#OpenAI`, `#formal-verification`, `#Lean`, `#research-breakthrough`

---

<a id="item-2"></a>
## [EA 550 亿美元卖身沙特财团，下周正式完成](https://www.gamersky.com/news/202607/2180618.shtml) ⭐️ 9.0/10

EA's $55 billion acquisition by a Saudi-led consortium (PIF, Silver Lake, Affinity Partners) has received all regulatory approvals and is expected to close on August 4, 2026, making EA a private company in the second-largest gaming acquisition in history.

telegram · zaihuapd · Aug 1, 09:10

**Tags**: `#gaming-industry`, `#mergers-and-acquisitions`, `#saudi-pif`, `#electronic-arts`, `#industry-consolidation`

---

<a id="item-3"></a>
## [DeepSeek Releases V4-Flash-0731: Top Value-per-Intelligence Open-Weight LLM](https://simonwillison.net/2026/Jul/31/deepseek-v4-flash-0731/#atom-everything) ⭐️ 8.0/10

DeepSeek has released DeepSeek-V4-Flash-0731, a 304-billion-parameter open-weight model with substantially enhanced agentic capabilities, available on Hugging Face at 167GB. Artificial Analysis ranks it ahead of MiniMax M3 (a 428B model) on intelligence while pricing it at just $0.14/million input tokens and $0.27/million output tokens, making it arguably the best value-per-intelligence model currently available. This release intensifies the price-performance competition in the open-weight LLM space, demonstrating that DeepSeek can deliver frontier-level intelligence at roughly one-tenth the cost of comparable models from competitors. It puts significant pressure on both open-source and proprietary model providers, as the Pareto frontier on the Intelligence Index vs. Cost chart shifts sharply in DeepSeek's favor. The model's output quality is highly sensitive to the reasoning effort setting — Simon Willison found that default reasoning produced a poorly drawn pelican on a bicycle, while setting reasoning_effort to high via OpenRouter yielded a significantly better result. The model can be accessed through OpenRouter with the command `llm -m openrouter/deepseek/deepseek-v4-flash-0731 -o reasoning_effort high`.

rss · Simon Willison · Jul 31, 23:59

**Background**: DeepSeek is a Chinese AI lab known for releasing highly competitive open-weight LLMs at aggressive price points, consistently challenging Western frontier models. The Artificial Analysis Intelligence Index aggregates multiple benchmark signals — including GPQA Diamond, Humanity's Last Exam, and Terminal-Bench — into a single model-level intelligence score, enabling direct cost-per-intelligence comparisons across models. "Agentic capabilities" refer to a model's ability to autonomously pursue goals, plan multi-step tasks, and use tools like web browsing and shell access to solve real-world problems.

<details><summary>References</summary>
<ul>
<li><a href="https://artificialanalysis.ai/">AI Model & API Providers Analysis | Artificial Analysis</a></li>
<li><a href="https://artificialanalysis.ai/models/capabilities/agentic">Best AI for Agentic Tasks: LLM Leaderboard | Artificial Analysis</a></li>
<li><a href="https://www.emergentmind.com/topics/agentic-capabilities">Agentic Capabilities in Adaptive AI</a></li>

</ul>
</details>

**Tags**: `#DeepSeek`, `#LLM`, `#AI Models`, `#Open Source`, `#Machine Learning`

---

<a id="item-4"></a>
## [MCP 2.0 Goes Stateless, Reigniting Ecosystem Interest](https://simonwillison.net/2026/Jul/31/stateless-mcp/#atom-everything) ⭐️ 8.0/10

The Model Context Protocol specification was updated to version 2026-07-28 (MCP 2.0), introducing a stateless transport model that replaces the previous two-step session initialization with a single HTTP request. Simon Willison also released two new tools — mcp-explorer and datasette-mcp — to help developers interact with and test MCP servers under the new spec. This is the most significant change to the MCP spec since its launch, dramatically reducing implementation complexity for both clients and servers while making the protocol better suited for scalable, enterprise-grade web applications. The shift back toward MCP also reflects growing concerns about the security risks of giving agents shell access, positioning MCP as a more auditable and controllable alternative. Under legacy MCP, clients had to first send an initialize request to obtain a Mcp-Session-Id, then send a second request with that ID to actually call a tool; the new stateless approach collapses this into a single POST request with metadata passed via headers like MCP-Protocol-Version and Mcp-Method. Server-side state management for session tracking is no longer needed, eliminating a major source of bugs and simplifying load balancing across backend instances.

rss · Simon Willison · Jul 31, 23:13

**Background**: The Model Context Protocol (MCP) is an open standard introduced by Anthropic in November 2024 to standardize how AI systems like LLMs integrate with external tools, data sources, and systems. After a surge of interest in 2025, MCP was partially eclipsed by Anthropic's Skills feature, as agents with terminal and curl access could achieve similar functionality more flexibly. A stateless protocol is one where the server does not retain session state between requests, improving scalability and reliability at the cost of potentially redundant data transfer.

<details><summary>References</summary>
<ul>
<li><a href="https://arstechnica.com/ai/2026/07/with-a-stateless-makeover-new-mcp-spec-targets-enterprise-scale/">With a stateless makeover, new MCP spec targets enterprise scale - Ars Technica</a></li>
<li><a href="https://news.ycombinator.com/item?id=49088058">MCP 2026-07-28 Specification: transport going stateless | Hacker News</a></li>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol</a></li>

</ul>
</details>

**Discussion**: On Hacker News, developers running MCP server gateways and registries reported that a significant portion of their bugs and operational issues stemmed from the need to persist server-side session state, validating the move to a stateless model. The overall sentiment is positive, with the change being seen as a necessary step for enterprise-scale adoption.

**Tags**: `#MCP`, `#Model Context Protocol`, `#LLM agents`, `#AI tools`, `#specification`

---

<a id="item-5"></a>
## [Microsoft Confirms Copilot 'Super App' Launch This Year](https://www.theverge.com/tech/972927/microsoft-copilot-super-app-confirmed) ⭐️ 8.0/10

Microsoft CEO Satya Nadella confirmed during an earnings call that the company will launch a Copilot 'super app' this year, merging its chat, coding, and agentic capabilities into a single unified application. The consolidation will bring together the Copilot chatbot, GitHub Copilot, Copilot Cowork, and Autopilot systems for both consumer and enterprise users. This consolidation represents a major strategic shift in the AI assistant space, positioning Microsoft to compete directly with OpenAI's recently launched ChatGPT Work app that integrates ChatGPT with Codex. It reflects a broader industry trend of unifying fragmented AI tools into single platforms, which could reshape how both consumers and enterprises interact with AI on a daily basis. Nadella described Copilot's evolution as progressing from a chat tool to Cowork to Autopilots, with the merger expected to happen this quarter. Notably, Copilot Cowork reportedly runs on Anthropic's Claude models rather than Microsoft's own AI, and Microsoft's revenue reached $90 billion last quarter driven primarily by AI and cloud businesses.

telegram · zaihuapd · Aug 1, 13:18

**Background**: Agentic AI refers to AI systems that can autonomously pursue goals, use tools, and take actions within human-defined constraints and objectives. Copilot Cowork is an AI automation layer built into Microsoft 365 that delegates, plans, and executes multi-step tasks across applications like Outlook and Teams. Copilot Autopilot represents a higher level of AI autonomy, moving from suggestions to fully bounded autonomous actions, and was introduced as a new AI category at Microsoft Build.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Agentic_AI">Agentic AI</a></li>
<li><a href="https://www.linkedin.com/pulse/microsoft-launches-copilot-cowork-built-anthropic-cross-m365-bora-g2xzc">Microsoft launches Copilot Cowork , built with Anthropic...</a></li>
<li><a href="https://www.linkedin.com/pulse/from-copilot-autopilot-microsoft-just-changed-game-frederick-jc0rf">From Copilot to Autopilot — Microsoft Just Changed the Game</a></li>

</ul>
</details>

**Tags**: `#Microsoft`, `#Copilot`, `#AI Super App`, `#Agentic AI`, `#Product Strategy`

---
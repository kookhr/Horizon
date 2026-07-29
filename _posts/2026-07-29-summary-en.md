---
layout: default
title: "Horizon Summary: 2026-07-29 (EN)"
date: 2026-07-29
lang: en
---

> From 43 items, 6 important content pieces were selected

---

1. [Anthropic Researchers Use Claude to Discover Novel Cryptographic Weaknesses](#item-1) ⭐️ 9.0/10
2. [Moonshot AI Raises $3.5B at $35B Valuation, Plans Hong Kong IPO](#item-2) ⭐️ 9.0/10
3. [TurboFieldfare: Run Gemma 4 26B in 2GB RAM on M-series Macs](#item-3) ⭐️ 8.0/10
4. [HANDBOOK.md Benchmark Shows Long Policy Documents Fail to Govern AI Agents](#item-4) ⭐️ 8.0/10
5. [AI worms can self-propagate through Copilot for Word](#item-5) ⭐️ 8.0/10
6. [Russia's FSB Files Criminal Charges Against Telegram Founder Pavel Durov](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Anthropic Researchers Use Claude to Discover Novel Cryptographic Weaknesses](https://simonwillison.net/2026/Jul/28/discovering-cryptographic-weaknesses-with-claude/#atom-everything) ⭐️ 9.0/10

Anthropic researchers used Claude Mythos Preview to discover previously unknown mathematical weaknesses in the HAWK cryptographic signature scheme and a reduced-round (7-round) version of AES-128. The model worked for approximately 60 hours at an estimated API cost of $100,000, with human researchers primarily intervening to encourage it not to give up and to pursue genuinely publishable findings. This represents a paradigm shift in cryptographic research, demonstrating that large language models can serve as active research partners capable of discovering novel mathematical flaws rather than merely summarizing existing knowledge. The public release of prompts and a reproducible repo adds transparency, and the creation of CryptanalysisBench (with ETH Zurich, Tel Aviv University, and University of Haifa) establishes a new evaluation framework for assessing LLM cryptanalysis capabilities. Neither of the discovered weaknesses has practical impact on today's computer systems — the AES attack targets only a reduced 7-round version, not the full AES-128. The shared prompts reveal that the model tended to give up on hard problems and needed significant encouragement to pursue novel attacks over low-hanging fruit, highlighting that human guidance remained critical to the research process.

rss · Simon Willison · Jul 28, 22:45

**Background**: HAWK is a lattice-based cryptographic signature scheme designed to be secure against both classical and quantum computers, and is a candidate in NIST's post-quantum cryptography standardization process. AES-128 is a widely deployed symmetric encryption standard; cryptanalysts often study reduced-round versions (e.g., 7 out of 10 rounds) to understand the cipher's security margins and develop attack techniques. Cryptanalysis involves finding mathematical weaknesses that could allow an attacker to break encryption or forge signatures without knowing the key.

<details><summary>References</summary>
<ul>
<li><a href="https://hawk-sign.info/">Hawk</a></li>
<li><a href="https://en.wikipedia.org/wiki/Advanced_Encryption_Standard">Advanced Encryption Standard - Wikipedia</a></li>
<li><a href="https://eprint.iacr.org/2019/622.pdf">Extended Truncated-diﬀerential Distinguishers on Round-reduced AES</a></li>

</ul>
</details>

**Discussion**: The Hacker News discussion highlighted fascination with the shared prompts, which reveal the iterative and sometimes messy nature of guiding an AI toward novel research. Commenters noted the significant cost (~$100,000) and the fact that human intervention was still essential, sparking debate about whether this truly represents autonomous AI research or sophisticated human-AI collaboration.

**Tags**: `#cryptography`, `#AI-research`, `#Claude`, `#security`, `#Anthropic`

---

<a id="item-2"></a>
## [Moonshot AI Raises $3.5B at $35B Valuation, Plans Hong Kong IPO](https://www.bloomberg.com/news/articles/2026-07-29/china-s-moonshot-ai-passes-funding-goal-to-hit-35-billion-value) ⭐️ 9.0/10

Moonshot AI (Kimi) closed a $3.5 billion funding round at a $35 billion post-money valuation, far exceeding its initial $1–2 billion target, driven by the breakthrough performance of its Kimi K3 model. The company has already initiated a new round at a $50 billion pre-money valuation with plans for a Hong Kong IPO as early as this year. This is one of the largest funding rounds for a Chinese AI company, signaling that China's AI ecosystem can produce models approaching frontier-level performance at a time when Western dominance is being challenged. The Kimi K3 model's launch reportedly triggered a tech stock sell-off, drawing comparisons to the 'DeepSeek moment' and underscoring the growing competitive pressure on US AI incumbents. Kimi K3 is a 2.8-trillion-parameter Mixture-of-Experts model with native vision capabilities and a 1M-token context window, offered as an open-weight model at $3 per million input tokens and $15 per million output tokens. The company's annualized recurring revenue reached $300 million in June, with daily sales growing at least 6x following K3's release.

telegram · zaihuapd · Jul 29, 10:12

**Background**: Moonshot AI is a Beijing-based AI startup founded in 2023, best known for its Kimi AI assistant and large language models. The 'DeepSeek moment' refers to the industry disruption caused by DeepSeek-R1, a low-cost Chinese AI model that challenged assumptions about US AI dominance and exposed cracks in the business models of major American AI players. Kimi K3's near-frontier performance has drawn similar comparisons, suggesting a pattern of Chinese AI labs closing the gap with Western frontier models.

<details><summary>References</summary>
<ul>
<li><a href="https://modal.com/library/moonshot/kimi-k3">Kimi K3 by Moonshot AI | Model Library | Modal</a></li>
<li><a href="https://www.bbc.com/news/articles/cy9w4q8pgp0o">China's Moonshot AI claims Kimi K3 can rival OpenAI and Anthropic</a></li>
<li><a href="https://www.noumenal.ai/post/the-deepseek-moment">The “ DeepSeek moment ” | Noumenal Labs</a></li>

</ul>
</details>

**Tags**: `#moonshot-ai`, `#kimi-k3`, `#ai-funding`, `#china-ai`, `#ipo`

---

<a id="item-3"></a>
## [TurboFieldfare: Run Gemma 4 26B in 2GB RAM on M-series Macs](https://github.com/drumih/turbo-fieldfare) ⭐️ 8.0/10

TurboFieldfare is a new open-source Swift/Metal inference engine that runs 4-bit quantized Gemma 4 26B-A4B-IT on any M-series Mac using only about 2GB of RAM, achieving 5–6 tok/s on an 8GB M2 MacBook Air and 31–35 tok/s on an M5 MacBook Pro. It works by keeping shared weights and KV cache in RAM while streaming routed MoE experts from SSD on demand using bounded parallel pread and a small expert cache. This demonstrates a practical approach to running large MoE models on memory-constrained devices by exploiting the sparse activation structure of Mixture-of-Experts architectures, potentially enabling on-device AI on entry-level hardware that was previously incapable of running such models. It challenges the conventional assumption that the entire model must reside in RAM, opening the door to running even larger models on consumer devices. The 4-bit quantized weights occupy roughly 14GB total, but only shared weights and KV cache (~2GB) stay in RAM; routed experts are fetched from SSD per token with bounded parallel pread while the GPU concurrently executes the shared layer computation. The project includes an experimental OpenAI-compatible local server with streaming and tool call support, and requires macOS 26 for full Swift language version 4.0 features (older macOS works with a minor code modification but loses a 2.4x prefill speedup).

hackernews · gitpusher42 · Jul 29, 15:05 · [Discussion](https://news.ycombinator.com/item?id=49098510)

**Background**: Mixture-of-Experts (MoE) models use a gating network to dynamically route each token to a small subset of specialized expert subnetworks, meaning only a fraction of the model's total parameters are activated per token. This sparse activation property means that while the full model may be very large on disk, only a small portion needs to be loaded for any given inference step. The KV cache stores key-value pairs from previous tokens to avoid recomputation during autoregressive generation, and its size grows with context length. Traditional inference engines like llama.cpp can use mmap to let the OS page model weights from disk, but this approach lacks awareness of inference timing; TurboFieldfare instead explicitly synchronizes SSD reads with GPU computation to minimize latency.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained</a></li>
<li><a href="https://magazine.sebastianraschka.com/p/coding-the-kv-cache-in-llms">Understanding and Coding the KV Cache in LLMs from Scratch</a></li>

</ul>
</details>

**Discussion**: Community sentiment is highly positive, with users praising the novel approach and questioning why the AI industry defaults to loading entire models into memory. A key technical debate centers on how TurboFieldfare compares to llama.cpp's mmap strategy, with one commenter noting that llama.cpp can already run 26B models in 2GB RAM but TurboFieldfare's advantage is inference-aware SSD read synchronization. Practical compatibility tips for older macOS versions were shared, and several users asked about cross-platform support (e.g., Debian, Jetson) and whether the tool works fully offline.

**Tags**: `#on-device-ai`, `#llm-inference`, `#moe`, `#apple-silicon`, `#quantization`

---

<a id="item-4"></a>
## [HANDBOOK.md Benchmark Shows Long Policy Documents Fail to Govern AI Agents](https://arxiv.org/abs/2607.25398) ⭐️ 8.0/10

A research team published HANDBOOK.md, a benchmark that tests whether AI agents reliably follow enterprise policy documents during autonomous, multi-step work. The best of 30 model configurations achieved only a 36.2% pass rate across 65 tasks drawn from five regulated domains including finance, medical billing, insurance, logistics, and HR. This finding directly challenges the common deployment pattern of placing long system prompts or policy files in an agent's context and trusting it to follow them throughout a session. For enterprises deploying autonomous agents in regulated industries, the results suggest that current approaches to agent governance via in-context policy documents are fundamentally unreliable and may require alternative strategies such as policy internalization or external enforcement mechanisms. The benchmark uses corporate handbooks up to 124 pages long placed in the agent's context, simulating real enterprise environments where agents must comply with binding policies while completing multi-step tasks. The low pass rate persisted even across frontier models, suggesting the problem is structural rather than model-specific, echoing the well-documented 'lost in the middle' phenomenon where LLMs degrade in performance when relevant information is buried in long contexts.

hackernews · spIrr · Jul 29, 13:01 · [Discussion](https://news.ycombinator.com/item?id=49096969)

**Background**: Language-model agents are increasingly deployed with 'standing instructions' — system prompts, policy files, or skills documents placed in context that are expected to govern every subsequent action. Existing benchmarks typically measure whether an agent can complete a task, but rarely test whether a long, binding policy document is actually followed throughout multi-step work. The 'lost in the middle' problem, documented by Liu et al. (arXiv:2307.03172), showed that LLMs perform poorly when key information is buried in the middle of long contexts, even when the model technically supports large context windows. Related work on policy internalization (arXiv:2510.11588) has explored embedding policy documents into model priors rather than relying on in-context placement.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2607.25398">[2607.25398] HANDBOOK.md: A Benchmark for Long-Context ...</a></li>
<li><a href="https://aigovernance.com/news/handbook-md-benchmark-agentic-policy-compliance-enterprise">Frontier AI Agents Pass Only 36% of Policy-Compliance Tasks ...</a></li>
<li><a href="https://arxiv.org/abs/2510.11588">[2510.11588] Analyzing and Internalizing Complex Policy ... Analyzing and Internalizing Complex Policy Documents for A Unified Evaluation and Governance Framework for Trustworthy ... Agent Governance Toolkit - microsoft.github.io [PDF] Analyzing and Internalizing Complex Policy Documents ...</a></li>

</ul>
</details>

**Discussion**: Community discussion (177 comments) broadly agreed with the findings, with multiple users sharing anecdotal experiences of Claude ignoring CLAUDE.md instructions after extended sessions. One commenter attributed the problem to long-context model limitations including KV cache quantization and poor sampler configurations, suggesting local inference as a workaround. Another drew parallels to human cognitive limitations, noting that humans are also poor at following long policy documents due to limited working memory and reasoning depth. A critical commenter questioned why parts of the paper appeared AI-authored, while another emphasized that agentic capabilities are synthetic, force-fed through post-training RL, and models not specifically trained to adhere to handbooks will naturally fail.

**Tags**: `#AI agents`, `#LLM context`, `#prompt engineering`, `#AI safety`, `#long context models`

---

<a id="item-5"></a>
## [AI worms can self-propagate through Copilot for Word](https://enklypesalt.com/posts/context-collapse-part3-ai-worming-through-word/) ⭐️ 8.0/10

Håkon Måløy demonstrated a proof-of-concept AI worm that self-replicates through Microsoft Copilot for Word by embedding malicious prompt injection instructions in documents, causing the AI to alter and spread the attack to new documents. This upgrades prompt injection attacks against Word from isolated incidents to full self-replicating worms. This represents a new class of AI-borne attacks where malicious instructions can autonomously spread between documents and users through AI assistants, similar to traditional computer worms but exploiting the fundamental inability of LLMs to distinguish instructions from data. As AI agents gain broader access to files, emails, and systems, this attack vector could enable rapid propagation of data theft, manipulation, or further exploitation. At the time of publication, no robust mitigation for this broader vulnerability class is available. Attackers can use techniques like hidden white text or Unicode font tricks to embed malicious instructions that are invisible to human readers but processed by the AI. The attack exploits the fact that Copilot processes document content as potential instructions, blurring the line between data and commands.

hackernews · Canopy9560 · Jul 29, 11:44 · [Discussion](https://news.ycombinator.com/item?id=49096188)

**Background**: Prompt injection is a cybersecurity exploit where malicious inputs are designed to cause unintended behavior in large language models by taking advantage of the model's inability to distinguish between developer-defined prompts and user-supplied content. Indirect prompt injection extends this by embedding adversarial prompts within external content (like web pages or documents) that the AI retrieves and processes. AI worms are a sophisticated type of malware that uses AI capabilities to self-propagate and evade detection, analogous to traditional network worms but targeting generative AI systems instead.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection">Prompt injection</a></li>
<li><a href="https://www.paloaltonetworks.com/cyberpedia/ai-worm">What Is an AI Worm? - Palo Alto Networks</a></li>
<li><a href="https://www.ibm.com/think/insights/malicious-ai-worm-targeting-generative-ai">Researchers develop malicious AI ‘worm’ targeting generative AI systems | IBM</a></li>

</ul>
</details>

**Discussion**: Commenters broadly agree that this vulnerability stems from the fundamental problem of mixing instructions with data in AI systems, with rwmj noting that no fix is possible until this architectural issue is addressed. boothby warns the problem will worsen as users grant agents excessive access, imagining scenarios where malicious GitHub comments could propagate through accounts. Several users, including averagjoe, report uninstalling Copilot and disabling local AI entirely, while piker highlights that techniques like white text and Unicode manipulation remain effective attack vectors.

**Tags**: `#ai-security`, `#prompt-injection`, `#copilot`, `#malware`, `#ai-agents`

---

<a id="item-6"></a>
## [Russia's FSB Files Criminal Charges Against Telegram Founder Pavel Durov](https://www.interfax.ru/russia/1106228) ⭐️ 8.0/10

On July 29, Russia's Federal Security Service (FSB) announced criminal charges against Telegram founder Pavel Durov under Article 205.1 Part 1.1 of the Russian Criminal Code (assisting terrorist activities) and placed him on an international wanted list. The FSB alleges that Telegram's management refused to remove channels, groups, and bots used by Ukrainian intelligence and terrorist/extremist organizations to coordinate sabotage, terrorist attacks, mass killings, and cyber fraud within Russia. This is a major escalation in the long-running conflict between the Russian government and Telegram, one of the world's most widely used messaging platforms, and raises serious concerns about the intersection of platform governance, privacy, and state power. An international arrest warrant for a tech founder over content moderation decisions could set a troubling precedent for the tech industry and free speech globally. The charges specifically cite Telegram's refusal to remove channels used for coordinating attacks, resulting in casualties including women and children, and billions of rubles in damages. The FSB frames the platform's inaction as direct complicity in terrorism under Russian law, rather than mere negligence.

telegram · zaihuapd · Jul 29, 05:56

**Background**: Pavel Durov founded Telegram in 2013 after leaving Russia amid pressure on his earlier social network VKontakte. Telegram has long been a flashpoint between the Russian government and tech platforms, with Roskomnadzor previously attempting to block the app in 2018 over encryption-related disputes, though the ban was lifted in 2020. Telegram has been used extensively by both pro-government and opposition groups, as well as by Ukrainian and Russian military and intelligence actors during the ongoing conflict.

**Tags**: `#telegram`, `#pavel-durov`, `#russia`, `#fsb`, `#legal`

---
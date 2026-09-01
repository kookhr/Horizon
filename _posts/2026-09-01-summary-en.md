---
layout: default
title: "Horizon Summary: 2026-09-01 (EN)"
date: 2026-09-01
lang: en
---

> From 44 items, 4 important content pieces were selected

---

1. [Anthropic Releases Claude Fable 5.1 and Mythos 5.1 with Major Cache Pricing Cuts](#item-1) ⭐️ 9.0/10
2. [Small Transformer Trained in 1.5 Hours Beats Many LLMs on ARC Benchmark](#item-2) ⭐️ 8.0/10
3. [Apple Presents Forensic Evidence of Trade Secret Theft Involving AI Learning at OpenAI](#item-3) ⭐️ 8.0/10
4. [Virtualizor Update Infrastructure Compromised via BGP Hijacking, Root Backdoors Planted](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Anthropic Releases Claude Fable 5.1 and Mythos 5.1 with Major Cache Pricing Cuts](https://www.anthropic.com/claude-fable-and-mythos-5-1) ⭐️ 9.0/10

Anthropic has announced Claude Fable 5.1 and Claude Mythos 5.1, featuring a noticeably improved writing style that is less stereotypically Claude-like, enhanced science capabilities, and a dramatic cache read pricing reduction from $1/M to $0.25/M tokens. The release also includes three breaking changes that appear to patch inadvertent chain-of-thought disclosure vulnerabilities. The 75% cache read price reduction makes Fable 5.1 half the cache read cost of Opus ($0.5/M), potentially signaling that Anthropic's original premium pricing failed to gain sufficient adoption and establishing a de facto ceiling for LLM pricing across the market. The writing style improvements and science capability gains also represent meaningful progress toward more natural and technically capable AI assistants. Simon Willison's benchmarks across reasoning effort levels (low, medium, high, xhigh, max) showed that the max effort level produces significantly better output but took approximately 14 minutes to generate a single SVG. Community analysis noted that excluding Terminal-Bench-Science 0.1 results, it is difficult to observe clear improvements over the previous model, and three breaking changes were identified as patches for a vulnerability where users could extract raw model thinking by creating a bogus tool definition.

hackernews · denysvitali · Sep 1, 17:53 · [Discussion](https://news.ycombinator.com/item?id=49525378)

**Background**: Prompt caching is a technique that allows LLM providers to store and reuse stable portions of prompts—such as system prompts, tool definitions, and conversation history—so that on subsequent turns, the cached content is served at a fraction of the full input price instead of being reprocessed. Cache reads are typically priced significantly lower than cache misses, making them economically attractive for applications with repetitive context. As the LLM market has matured, cache read pricing has become a key competitive dimension, directly affecting the total cost of ownership for production AI applications that rely on multi-turn conversations or large persistent contexts.

<details><summary>References</summary>
<ul>
<li><a href="https://infkey.com/prompt-caching-2026-cut-ai-api-bills-by-90">Prompt Caching 2026: Cut AI API Bills by 90%</a></li>
<li><a href="https://www.jsonhouse.com/posts/llm-api-pricing-2026/">LLM API Pricing 2026: Full Comparison Table (Weekly) | Json House</a></li>

</ul>
</details>

**Discussion**: An Anthropic employee (felixrieseberg) highlighted that Fable 5.1's writing style is a major improvement, sounding less stereotypically like Claude and responding more reliably to style instructions, while also teasing upcoming science capabilities. Simon Willison provided practical benchmarks across reasoning effort levels, demonstrating that max effort yields significantly better results but at the cost of ~14 minutes per generation. GodelNumbering offered sharp pricing analysis, arguing the cache read reduction from $1/M to $0.25/M suggests Anthropic didn't get much traction at original pricing and likely places a ceiling on LLM pricing market-wide, while also noting that without Terminal-Bench-Science results, improvements are hard to discern. mlaux identified that all three breaking changes are patches for chain-of-thought disclosure vulnerabilities exploited via crafted tool definitions.

**Tags**: `#anthropic`, `#claude`, `#llm`, `#ai-models`, `#pricing`

---

<a id="item-2"></a>
## [Small Transformer Trained in 1.5 Hours Beats Many LLMs on ARC Benchmark](https://mvakde.github.io/blog/44-on-arc-1/) ⭐️ 8.0/10

A researcher trained a small, specialized transformer from scratch in just 1.5 hours that achieves strong results on the ARC (Abstraction and Reasoning Corpus) benchmark, outperforming many large language models. The model is explicitly not an LLM but a purpose-built architecture trained specifically for ARC-style reasoning tasks. This result challenges the prevailing assumption that complex reasoning tasks require massive language models and enormous compute budgets. It suggests that specialized, efficiently-designed architectures can achieve competitive reasoning performance at a fraction of the cost, opening new directions for AI research beyond the scale-everything paradigm.

hackernews · porridgeraisin · Sep 1, 09:52 · [Discussion](https://news.ycombinator.com/item?id=49519939)

**Tags**: `#machine-learning`, `#transformers`, `#ARC-benchmark`, `#reasoning`, `#efficient-training`

---

<a id="item-3"></a>
## [Apple Presents Forensic Evidence of Trade Secret Theft Involving AI Learning at OpenAI](https://9to5mac.com/2026/08/31/apple-openai-forensic-macbook-evidence/) ⭐️ 8.0/10

Apple has presented forensic evidence from a former employee's MacBook showing that Mr. Liu downloaded confidential Apple circuit schematics and used them in his work at OpenAI, including running LTspice simulations that were fed to an AI agent. The evidence also reveals that Liu sent evidence-destruction instructions to an OpenAI colleague upon learning of Apple's internal investigation, and that the forensic trail was uncovered because his Mac mini synced via iCloud to the MacBook he had taken from Apple. Apple is advancing a novel legal argument that when trade secrets are fed into AI models that learn from them, this creates "irreversible and continually propagating uses" of protected information, potentially rendering traditional remedies like injunctions inadequate. If courts accept this reasoning, it could establish far-reaching precedents for how the AI industry handles confidential data and what remedies are available when trade secrets become embedded in model weights. Liu allegedly ran a simulation in March using the stolen circuit schematic in LTspice, an electrical engineering simulation tool, and told colleagues his AI "agent" had learned to run LTspice and review results. Apple is now seeking access to the Mac mini at OpenAI that synced the files, and the case also raises privacy questions about whether data synced through personal cloud accounts on company devices can be legally searched by employers.

hackernews · colinprince · Sep 1, 20:19 · [Discussion](https://news.ycombinator.com/item?id=49527573)

**Background**: Trade secret law traditionally provides remedies such as injunctions and monetary damages when confidential information is misappropriated, but these remedies assume the information can be contained or returned. AI models present a unique challenge: once a model has learned patterns from training data, that knowledge becomes distributed across the model's weights and parameters, making it difficult or impossible to selectively "unlearn" specific information. LTspice is a widely used SPICE-based electronic circuit simulation tool in electrical engineering. This case is part of a broader legal landscape where courts are grappling with how intellectual property laws apply to AI training and deployment.

**Discussion**: Commenters highlighted the novelty of Apple's argument about AI creating "irreversible and continually propagating uses" of trade secrets, with one noting it is a "high impact argument to test" that the case may eventually need to work out. Several raised privacy concerns about iCloud syncing exposing personal data on company devices to legal search, with one noting they hadn't considered that failing to sign out of personal accounts could expose their data. One commenter humorously summarized Liu's apparent defense as "I didn't steal it, I fed it to an agent who then fed it back to me," while another drew parallels to the Coca-Cola recipe theft case where Pepsi immediately refused to accept stolen trade secrets.

**Tags**: `#legal`, `#trade-secrets`, `#openai`, `#apple`, `#ai-ethics`

---

<a id="item-4"></a>
## [Virtualizor Update Infrastructure Compromised via BGP Hijacking, Root Backdoors Planted](https://www.virtualizor.com/blog/security-incident-bgp-hijacking/) ⭐️ 8.0/10

Between August 28 and 30, 2026, Virtualizor's update infrastructure was compromised through BGP hijacking, enabling attackers to deliver malicious update packages signed with valid TLS certificates that installed root SSH backdoors and Java payloads on affected hypervisors. AlbaHost independently confirmed 5 out of 34 hypervisors showed indicators of compromise, while Softaculous emphasized this was a distribution chain attack rather than a software code vulnerability. This incident demonstrates a sophisticated supply chain attack chain where BGP hijacking was leveraged to bypass TLS certificate validation and deliver seemingly legitimate malicious updates directly to hypervisors running critical hosting infrastructure. It exposes the persistent vulnerability of BGP-based routing as a trust foundation for software distribution, and raises urgent questions about how update mechanisms can be hardened against network-layer attacks that undermine domain validation. The malicious packages specifically wrote unauthorized root SSH keys, installed Java payloads, and established persistence services on compromised hypervisors. Only installations that performed updates during the August 28–30 window were affected, and Softaculous confirmed there is no evidence that other products in their portfolio were impacted.

telegram · zaihuapd · Sep 1, 06:05

**Background**: Virtualizor is a web-based VPS control panel developed by Softaculous, widely used by hosting providers to deploy and manage virtual private servers across multiple virtualization technologies. BGP (Border Gateway Protocol) is the core routing protocol of the internet, and BGP hijacking occurs when attackers falsely announce ownership of IP prefixes to redirect traffic through networks they control. A critical consequence is that BGP hijacking can fool the domain validation process used by Certificate Authorities, allowing attackers to obtain valid TLS certificates for domains they do not actually control. RPKI (Resource Public Key Infrastructure) exists to cryptographically authenticate route origins, but it is not universally deployed across all networks.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cloudflare.com/learning/security/glossary/bgp-hijacking/">What Is BGP Hijacking?</a></li>
<li><a href="https://community.letsencrypt.org/t/using-bgp-to-acquire-bogus-tls-certificates/38627">Using BGP to Acquire Bogus TLS Certificates - Issuance Tech - Let's Encrypt Community Support</a></li>
<li><a href="https://www.virtualizor.com/">Virtualizor – Cloud Control Panel</a></li>

</ul>
</details>

**Discussion**: The incident was discussed on LowEndTalk forums and independently analyzed by Cyber Kendra, with AlbaHost providing forensic confirmation of real-world compromises. Community sentiment centered on the severity of the attack chain and concerns about the broader implications for update infrastructure security across the hosting industry.

**Tags**: `#supply-chain-attack`, `#bgp-hijacking`, `#virtualization-security`, `#root-backdoor`, `#incident-response`

---
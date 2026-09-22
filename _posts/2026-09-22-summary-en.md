---
layout: default
title: "Horizon Summary: 2026-09-22 (EN)"
date: 2026-09-22
lang: en
---

> From 37 items, 2 important content pieces were selected

---

1. [TypeSafe AI Launches Jev: First 'System One' Decision Model](#item-1) ⭐️ 8.0/10
2. [SemiAnalysis Deep Dive: MoE Inference Computation and Data Movement](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [TypeSafe AI Launches Jev: First 'System One' Decision Model](https://simonwillison.net/2026/Sep/21/jev/) ⭐️ 8.0/10

TypeSafe AI has unveiled Jev, the first model in a new category called 'System One models' that accepts unstructured text input but returns typed probabilistic decisions as floating point numbers instead of text output. Jev supports three question types — Yes/No ('Noul' questions, named after the Bernoulli distribution), Choice (with probability distributions across options), and Score (numeric ratings along a defined range) — and charges only for input tokens at $0.042 per million, with output being free. Jev represents a genuinely novel paradigm shift in the LLM space: instead of generating text that must be parsed and interpreted, it directly outputs structured probabilistic decisions that software can use immediately, running 40-200x faster than frontier LLMs. This could fundamentally change how LLMs are integrated into decision-making pipelines such as spam detection, content classification, search reranking, and prioritization systems, while its input-only pricing model disrupts the standard token-based economics of LLM usage. Jev's architecture retains the knowledge of a pretrained LLM but replaces generated confidence claims with decision probabilities read directly from its internal representations, trained against outcomes. The API accepts a 'state' object (string, array of strings, or name-value pairs) plus multiple questions evaluated in parallel within the context window, returning results in 70-500ms. A notable concern is that Jev pushes further toward black-box ML systems — it provides no textual explanation for its decisions, making bias auditing and interpretability significantly harder than with traditional LLMs.

rss · Simon Willison · Sep 21, 23:09

**Background**: Current LLMs are what TypeSafe calls 'System Two models' — they generate text token by token, thinking out loud, and return a string that applications must parse. The name 'System One' references Daniel Kahneman's dual-process theory from 'Thinking, Fast and Slow,' where System One represents fast, intuitive decision-making and System Two represents slow, deliberate reasoning. Traditional approaches to getting structured decisions from LLMs involve prompting them to output text in formats like JSON, then parsing that output — a process prone to errors, hallucinations, and latency. Jev eliminates this pipeline by directly outputting calibrated probabilities, though at the cost of interpretability.

<details><summary>References</summary>
<ul>
<li><a href="https://www.datacamp.com/blog/system-one-models-jev">Jev: TypeSafe 's System One Model Explained | DataCamp</a></li>
<li><a href="https://docs.typesafe.ai/introduction">Introduction - TypeSafe AI</a></li>
<li><a href="https://archerhume.com/posts/jevs-architecture-unmasked/">Jev’s Architecture Unmasked — archerhume</a></li>

</ul>
</details>

**Discussion**: Maggie Appleton argued that 'decision models' is a more intuitive name than 'System One models,' a sentiment echoed by Simon Willison. On Hacker News, the CEO confirmed that 'Noul' is shorthand for Bernoulli distribution. A recurring concern in discussions is the black-box nature of the model — commentators worry that floating-point outputs with no explanations could conceal bias, especially in sensitive applications like ranking job applicants, and that the lack of interpretability represents a regression from the relative transparency of text-generating LLMs.

**Tags**: `#LLM`, `#decision-models`, `#AI-architecture`, `#TypeSafe-AI`, `#structured-output`

---

<a id="item-2"></a>
## [SemiAnalysis Deep Dive: MoE Inference Computation and Data Movement](https://newsletter.semianalysis.com/p/computation-and-data-movement-for) ⭐️ 8.0/10

SemiAnalysis published a comprehensive technical analysis examining the computational and data movement challenges involved in efficiently serving Mixture of Experts (MoE) models on inference hardware. The article breaks down the structure, execution flow, and serving strategies for mapping MoE architectures onto real-world inference infrastructure. As MoE architectures become the dominant paradigm for frontier LLMs (e.g., DeepSeek, Mixtral), the bottleneck for inference efficiency is shifting from pure computation to data movement — moving expert weights and intermediate activations across memory hierarchies. Understanding these tradeoffs is essential for practitioners designing cost-effective LLM serving infrastructure at scale. The article focuses on the interplay between sparse expert activation patterns and memory bandwidth constraints, examining how routing decisions at each layer create irregular data access patterns that complicate efficient hardware utilization. It covers the structural flow of MoE inference, including how expert selection and token routing impact both compute scheduling and data movement costs across GPU memory hierarchies.

rss · Semianalysis · Sep 21, 18:14

**Background**: Mixture of Experts (MoE) is a sparse activation architecture where only a subset of expert subnetworks is activated per token, allowing models to scale up total parameter count dramatically while keeping per-token computation low. This enables larger, more capable models to be trained and served within reasonable compute budgets compared to equivalent dense models. However, the tradeoff is that all expert weights must reside in memory even when not actively used, creating significant memory capacity and bandwidth pressures during inference. As MoE models grow in size and complexity, data movement — the cost of loading the right expert weights at the right time — increasingly dominates over raw FLOP computation, making it a critical optimization target for inference system designers.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained</a></li>
<li><a href="https://www.alphaxiv.org/overview/2510.05497v4">Patterns behind Chaos: Forecasting Data Movement for... | alphaXiv</a></li>
<li><a href="https://arxiv.org/abs/2507.11181">[2507.11181] Mixture of Experts in Large Language Models</a></li>

</ul>
</details>

**Tags**: `#MoE`, `#inference`, `#data-movement`, `#LLM-serving`, `#hardware`

---
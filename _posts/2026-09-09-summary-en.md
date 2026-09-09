---
layout: default
title: "Horizon Summary: 2026-09-09 (EN)"
date: 2026-09-09
lang: en
---

> From 39 items, 8 important content pieces were selected

---

1. [OpenAI Claims AI Solution to Navier–Stokes Millennium Prize Problem Amid Priority Dispute](#item-1) ⭐️ 10.0/10
2. [Apple Announces iPhone Duo, Its First Foldable Phone](#item-2) ⭐️ 9.0/10
3. [Shopify Acquires Tailwind CSS as AI Disrupts Developer Tooling](#item-3) ⭐️ 9.0/10
4. [🤖 OpenAI称GPT-6 Astra的CoT可监测性显著下降](#item-4) ⭐️ 9.0/10
5. [vLLM v0.29.0 Makes Model Runner V2 Default, Adds 770B MoE Support](#item-5) ⭐️ 8.0/10
6. [GPT-6 Astra, Looped Transformers, and Hidden Reasoning Explored](#item-6) ⭐️ 8.0/10
7. [Exposé Reveals Malicious Software Ads Bypass Google's Automated Review](#item-7) ⭐️ 8.0/10
8. [Terence Tao Warns AI Is Mining Open Math Problems Non-Renewably](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI Claims AI Solution to Navier–Stokes Millennium Prize Problem Amid Priority Dispute](https://simonwillison.net/2026/Sep/8/on-navier-stokes/) ⭐️ 10.0/10

On September 8, 2026, OpenAI announced that an internal frontier model (referred to as GPT-6 Astra), deployed as a swarm of approximately 10,000 AI agents, produced a counter-example demonstrating the breakdown of Navier–Stokes solutions in three-dimensional Euclidean space, effectively resolving the Navier–Stokes existence and smoothness Millennium Prize Problem. The result was formalized and verified using the Lean proof assistant, though it has not yet been independently verified by external mathematicians or the Clay Mathematics Institute. If verified, this would represent the first AI-generated solution to a Millennium Prize Problem, marking a historic milestone for AI capabilities in deep mathematical reasoning and potentially reshaping how frontier mathematics is conducted. The announcement is further complicated by a priority dispute with mathematicians Tristan Buckmaster (NYU) and Levent Alpöge (Anthropic), who had been working on closely related results for nearly a year and allege that OpenAI may have had access to their unpublished work through Codex session data. OpenAI's agents sent 2.7 million messages and used approximately 130 billion output tokens for the Navier–Stokes problem specifically, with Lean formalization taking an additional 17 hours via GPT-6 Astra; at public API prices, the total 300 billion tokens across all attempted problems would cost roughly $15 million. The counter-example builds upon a method developed by Diego Córdoba and Luis Martínez-Zoroa in 2023 for finding blowup phenomena in related fluid equations, and OpenAI has stated it will not claim the $1 million Clay Millennium Prize.

rss · Simon Willison · Sep 8, 23:55

**Background**: The Navier–Stokes equations are a system of partial differential equations that describe the motion of fluids in space, and while computational solutions are widely used in engineering and physics, a complete analytical understanding of whether smooth solutions always exist in three dimensions remains an open problem. The Clay Mathematics Institute designated seven Millennium Prize Problems in 2000, each carrying a $1,000,000 reward, to celebrate and challenge mathematicians at the turn of the millennium; as of 2026, only the Poincaré Conjecture has been officially solved. The Navier–Stokes existence and smoothness problem asks whether, given an initial velocity field in three space dimensions and time, there always exist smooth and globally defined velocity and pressure fields that solve the equations — or whether solutions can break down (blow up) in finite time.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Navier-Stokes_existence_and_smoothness_problem">Navier-Stokes existence and smoothness problem</a></li>
<li><a href="https://en.wikipedia.org/wiki/Millennium_Prize_Problems">Millennium Prize Problems - Wikipedia</a></li>
<li><a href="https://www.claymath.org/millennium-problems/">The Millennium Prize Problems - Clay Mathematics Institute</a></li>

</ul>
</details>

**Discussion**: Tristan Buckmaster has publicly alleged that OpenAI's team may have gained access to his and Alpöge's unpublished work through their Codex sessions, noting that OpenAI did not directly answer whether the model was trained on their data. The dispute highlights tensions between competitive AI labs, as OpenAI reportedly excluded Alpöge from co-authorship due to his employment at rival Anthropic, while offering Buckmaster a concurrent release arrangement. The broader mathematical community is likely awaiting independent verification of the counter-example before drawing conclusions about both the mathematical validity and the ethical circumstances of the discovery.

**Tags**: `#AI`, `#mathematics`, `#Navier-Stokes`, `#Millennium-Prize-Problems`, `#OpenAI`

---

<a id="item-2"></a>
## [Apple Announces iPhone Duo, Its First Foldable Phone](https://www.apple.com/iphone-duo/) ⭐️ 9.0/10

Apple has officially announced the iPhone Duo, its first-ever foldable smartphone, entering a product category that competitors like Samsung have dominated for years. The device was unveiled at Apple's latest keynote presentation led by John Ternus and other executives. This marks a major strategic shift for the world's most valuable tech company, as foldable phones represent one of the few remaining hardware categories Apple had yet to enter. Apple's entry could reshape the competitive landscape of the foldable market and influence broader mobile hardware design trends across the industry. Early hands-on impressions report that the device has no visible crease on the display, a notable engineering achievement in foldable technology. However, the pricing is reportedly around 50% higher than Samsung's Z Fold 8 and even several hundred dollars more than the Z Fold 8 Ultra, and the device is notably wide even when folded.

hackernews · thecosmicfrog · Sep 9, 18:15 · [Discussion](https://news.ycombinator.com/item?id=49630931)

**Background**: Foldable smartphones have been commercially available since 2019, with Samsung's Galaxy Fold and subsequent Z Fold/Z Flip series being the most prominent offerings in this category. These devices use flexible OLED displays and precision hinge mechanisms to allow a phone-sized device to unfold into a larger, tablet-like screen. Apple has historically been cautious about adopting new form factors, often waiting until technology matures before entering a product category. The foldable market has been gradually growing but remains a niche segment compared to traditional smartphones.

**Discussion**: Community reactions are deeply divided: some praise the crease-free display and overall design, while others criticize the extremely high pricing and Apple's increasingly rehearsed, emotionally-flat presentation style. Several commenters express frustration with the trend of ever-larger phones, noting that even folded the device is too wide for comfortable one-handed use. One notable technical observation draws a parallel between the device's aspect ratio and the ISO 216 international paper size standard, where folding preserves proportions.

**Tags**: `#apple`, `#foldable-phone`, `#hardware`, `#product-announcement`, `#mobile`

---

<a id="item-3"></a>
## [Shopify Acquires Tailwind CSS as AI Disrupts Developer Tooling](https://tailwindcss.com/blog/tailwind-is-joining-shopify) ⭐️ 9.0/10

Shopify has acquired Tailwind CSS, one of the most popular utility-first CSS frameworks, from Tailwind Labs. The acquisition comes after Tailwind Labs laid off 75% of its engineering team and saw documentation traffic decline by approximately 40% from early 2023, both attributed to the disruptive impact of AI on its business model. This acquisition signals how AI is fundamentally disrupting developer-focused businesses that rely on selling UI components and documentation-driven traffic, as AI tools can now generate styling code and UI templates that were previously Tailwind Labs' primary revenue source. It also marks a major e-commerce platform absorbing a widely-used open-source web development framework, potentially reshaping how millions of developers build storefronts and web interfaces. Tailwind Labs' business model combined free open-source software distribution with revenue from premium paid offerings like Tailwind UI templates, a model that AI has rendered increasingly unsustainable. Community members note that Shopify is acquiring both the people and the brand, and some question whether developers building new sites with AI assistance even need Tailwind versus modern vanilla CSS.

hackernews · EdwinHoksberg · Sep 9, 13:27 · [Discussion](https://news.ycombinator.com/item?id=49626190)

**Background**: Tailwind CSS is an open-source, utility-first CSS framework that allows developers to rapidly build custom user interfaces by applying pre-defined utility classes directly in HTML, unlike traditional frameworks like Bootstrap that provide predefined component classes. Tailwind Labs, the company behind the framework, generated revenue primarily through Tailwind UI — a collection of premium, pre-built UI component templates and patterns sold to developers. The rise of AI coding assistants has eroded this model, as developers can now prompt AI tools to generate equivalent UI code, reducing demand for both paid templates and manual documentation lookups.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Tailwind_CSS">Tailwind CSS - Wikipedia</a></li>
<li><a href="https://grokipedia.com/page/2026_Tailwind_Labs_layoffs">2026 Tailwind Labs layoffs — Grokipedia</a></li>
<li><a href="https://www.linkedin.com/posts/the-decoder-en_tailwinds-shattered-business-model-is-a-activity-7415025359001395200-M-XF">Tailwind 's shattered business model is a grim warning for every...</a></li>

</ul>
</details>

**Discussion**: Community sentiment is mixed but largely sympathetic toward the Tailwind team, with commenters recognizing AI's severe impact on the business of selling UI templates. A notable debate emerged about whether Tailwind is still necessary when AI can generate vanilla CSS, with some arguing that AI removes the maintenance pain points that made CSS frameworks attractive in the first place. Others view the acquisition as Shopify buying the brand and talent rather than the technology itself, given the declining viability of the template-selling business model.

**Tags**: `#tailwind-css`, `#shopify`, `#acquisition`, `#ai-impact`, `#web-development`

---

<a id="item-4"></a>
## [🤖 OpenAI称GPT-6 Astra的CoT可监测性显著下降](https://deploymentsafety.openai.com/gpt-6-astra) ⭐️ 9.0/10

OpenAI has officially disclosed that GPT-6 Astra exhibits significantly reduced Chain of Thought monitorability, with the model increasingly controlling its own reasoning process and completing complex tasks with less verbalized reasoning, raising serious concerns for AI alignment and safety monitoring.

telegram · zaihuapd · Sep 9, 09:45

**Tags**: `#AI Safety`, `#Chain of Thought`, `#OpenAI`, `#Model Interpretability`, `#GPT-6`

---

<a id="item-5"></a>
## [vLLM v0.29.0 Makes Model Runner V2 Default, Adds 770B MoE Support](https://github.com/vllm-project/vllm/releases/tag/v0.29.0) ⭐️ 8.0/10

vLLM v0.29.0 ships with 594 commits from 277 contributors, making Model Runner V2 (MRV2) the default runtime for all models and adding support for several new large MoE architectures including Tencent's 770B Hy4-preview and Qwen3.8-Flash-Next with NVFP4 quantization. The release also introduces batch-sharded sampling that cuts per-step logits memory by 1/TP, CUDA graph memory profiling for KV cache auto-sizing, and significant kernel-level optimizations for Kimi-K3 and DeepSeek V4 models. As one of the most widely deployed open-source LLM inference engines, vLLM's transition to MRV2 as the default runtime marks a major architectural milestone that promises cleaner modularity and higher throughput across GPU platforms. The addition of support for 770B-scale MoE models and NVFP4 quantization signals readiness for the next generation of ultra-large models on NVIDIA Blackwell hardware, directly impacting production deployment costs and latency for teams running frontier models. MRV1 remains in use for a few ROCm models and features MRV2 does not yet support, so the transition is not yet fully complete. Notable breaking changes include removal of ten deprecated model architectures, migration of FlexOlmo/Olmo3/Hunyuan to the Transformers backend, deprecation of `python -m vllm.entrypoints.openai.api_server` in favor of `vllm serve`, and removal of the PyAV video decoder backend. Performance highlights include a 6.6-7.6x kernel speedup for K3 Mamba metadata preparation and approximately 5% end-to-end latency reduction from fused MXFP4 top-k finalization.

github · khluu · Sep 9, 08:54

**Background**: vLLM is a high-throughput open-source LLM inference and serving engine known for innovations like PagedAttention and continuous batching. Model Runner V2 (MRV2) is a ground-up re-implementation of vLLM's core execution engine, designed to address fundamental design issues and technical debt accumulated since vLLM V1, delivering a cleaner, more modular architecture with up to 56% higher throughput on GB200 systems. MoE (Mixture of Experts) models activate only a subset of parameters per token, enabling very large models like the 770B Hy4-preview to run efficiently. NVFP4 is NVIDIA's 4-bit floating-point format for Blackwell GPUs, combining ultra-low-precision storage with FP8 scaling factors to preserve accuracy while reducing memory bandwidth.

<details><summary>References</summary>
<ul>
<li><a href="https://vllm-website-5zwgmvte0-inferact-inc.vercel.app/blog/mrv2">Model Runner V 2 : A Modular and Faster Core for vLLM | vLLM Blog</a></li>
<li><a href="https://docs.vllm.ai/en/stable/design/model_runner_v2/">Model Runner V 2 Design Document - vLLM</a></li>
<li><a href="https://developer.nvidia.com/blog/introducing-nvfp4-for-efficient-and-accurate-low-precision-inference/">Introducing NVFP4 for Efficient and Accurate Low-Precision Inference | NVIDIA Technical Blog</a></li>

</ul>
</details>

**Tags**: `#vllm`, `#llm-inference`, `#model-runner-v2`, `#moe-models`, `#gpu-optimization`

---

<a id="item-6"></a>
## [GPT-6 Astra, Looped Transformers, and Hidden Reasoning Explored](https://magazine.sebastianraschka.com/p/gpt-6-astra-looped-transformers-and) ⭐️ 8.0/10

Sebastian Raschka published an in-depth analysis examining how looped transformer architectures and hidden reasoning mechanisms may underpin GPT-6 Astra's capabilities, specifically questioning whether internal iterative processing can substitute for explicit chain-of-thought (CoT) reasoning. The article connects recent architectural innovations—where a fixed set of transformer blocks is applied iteratively over the same latent representation—to GPT-6 Astra's state-of-the-art performance on computer use, software engineering, and other complex tasks. This analysis addresses a fundamental architectural question in LLM design: whether models can perform complex multi-step reasoning internally without explicitly generating intermediate reasoning tokens, which would significantly reduce inference costs and latency. The outcome of this debate could reshape how future frontier models are designed, moving away from verbose chain-of-thought outputs toward more efficient hidden computation. Looped transformers apply the same transformer blocks iteratively—potentially dozens of times—over a single latent representation, conceptually extending the Universal Transformer architecture proposed in 2018. A key technical tension exists between hidden reasoning (where iteration happens internally on latent states) and explicit CoT (where reasoning steps are output as tokens), with research by Will Merrill showing that certain computational complexity classes minimally require specific amounts of CoT depth to solve.

hackernews · ModelForge · Sep 9, 14:37 · [Discussion](https://news.ycombinator.com/item?id=49627370)

**Background**: Looped transformers, also called recurrent depth or looped depth sharing, reuse a fixed set of transformer blocks iteratively rather than stacking many distinct layers, offering parameter efficiency while enabling deeper computation. This concept traces back to Universal Transformers (2018), which applied transformer blocks recurrently and showed improvements over standard transformers on algorithmic and language understanding tasks. Chain-of-thought (CoT) reasoning is a technique where LLMs generate intermediate reasoning steps as output tokens before arriving at a final answer, effectively trading additional inference tokens for improved reasoning capability. GPT-6 Astra, released by OpenAI in September 2026, represents a frontier model that achieves state-of-the-art results across computer use, browsing, software engineering, and scientific tasks.

<details><summary>References</summary>
<ul>
<li><a href="https://www.emergentmind.com/topics/looped-transformer-architecture">Looped Transformer Architecture</a></li>
<li><a href="https://arxiv.org/abs/1807.03819">[1807.03819] Universal Transformers</a></li>
<li><a href="https://openai.com/index/gpt-6-astra/">GPT-6 Astra: A new generation of intelligence | OpenAI</a></li>

</ul>
</details>

**Discussion**: The discussion is technically substantive, with commenter shawntan sharing key research references including Will Merrill's work on computational complexity requirements for CoT and Universal Transformers. A notable debate emerged around wolttam's observation that looping an entire transformer on itself constitutes hidden reasoning by definition, since the model's reasoning trace is fed back internally rather than output. Several users reported practical concerns about Astra's performance degradation after a recent model update, with siva7 noting a significant quality drop that made the model feel like a lower-tier variant.

**Tags**: `#transformers`, `#LLM-reasoning`, `#chain-of-thought`, `#universal-transformers`, `#AI-architecture`

---

<a id="item-7"></a>
## [Exposé Reveals Malicious Software Ads Bypass Google's Automated Review](https://xlii.space/eng/malicious-software-on-google-ads/) ⭐️ 8.0/10

A security researcher published a detailed exposé demonstrating how malicious software can be successfully advertised through Google Ads, bypassing the platform's automated ad review systems entirely. After the article gained traction on HackerNews, Google reinstated the researcher's account, suggesting the issue was only addressed due to public visibility rather than systemic detection. This exposé reveals systemic failures in Google's automated ad review infrastructure, which processes millions of ads daily and serves as a critical gatekeeper for internet safety. The fact that malicious software could pass automated checks while legitimate users routinely face wrongful rejections highlights a dangerous asymmetry that could enable large-scale distribution of malware through one of the world's largest advertising platforms. The researcher's account was reinstated only after the issue gained visibility on HackerNews, indicating that Google's automated systems could not self-correct even after the malicious content was flagged. Community members corroborated the findings, with one user reporting that nearly all YouTube ads observed in a 15-minute session were fraudulent scams, and another noting a similar compromised-site advertising pattern from nearly a decade ago.

hackernews · xlii · Sep 9, 11:43 · [Discussion](https://news.ycombinator.com/item?id=49624856)

**Background**: Google Ads operates one of the world's largest digital advertising networks, relying heavily on automated review systems to screen ads before they go live. As the volume of ads has grown, Google has increasingly replaced human reviewers with machine learning models to scale its review process. This shift has led to well-documented problems where legitimate users and businesses face opaque, automated rejections with no meaningful avenue for appeal, while bad actors exploit gaps in the automated checks to distribute malicious content.

**Discussion**: Community sentiment is overwhelmingly critical of Google, with commenters sharing personal anecdotes of legitimate submissions being rejected by automated systems while fraudulent ads proliferate. Multiple users argue that large tech companies increasingly hide behind automated systems to avoid accountability, with some suggesting regulatory requirements for mandatory human contact points and transparent appeal processes. The author themselves noted the irony that it took public amplification on HackerNews to resolve the issue rather than Google's own safeguards.

**Tags**: `#security`, `#google-ads`, `#ad-fraud`, `#platform-abuse`, `#automated-review`

---

<a id="item-8"></a>
## [Terence Tao Warns AI Is Mining Open Math Problems Non-Renewably](https://simonwillison.net/2026/Sep/9/terence-tao/) ⭐️ 8.0/10

Terence Tao has publicly warned that AI-powered research efforts are mining open mathematical problems at a non-renewable pace, and that even the rumor of someone working on a problem can now trigger massive AI-powered efforts to solve it before the original research project reaches its full potential. This warning from one of the world's most eminent mathematicians highlights a novel and existential threat to academic culture: AI is creating perverse incentives that could lead researchers to stop sharing promising directions, potentially reversing centuries of open science traditions and causing long-term damage to the field. Tao specifically notes that the collection of good, fruitful open problems is being depleted in a non-renewable fashion, and that the incentives are now pointing toward secrecy rather than openness, which would fundamentally alter how mathematical research is conducted and shared.

rss · Simon Willison · Sep 9, 00:20

**Background**: Open science traditions in mathematics have long relied on researchers sharing problems and directions openly, enabling collaborative progress over years or decades. AI tools can now rapidly explore and solve certain classes of mathematical problems, compressing timelines that previously allowed for deeper, more collaborative exploration. Terence Tao is a Fields Medal-winning mathematician widely regarded as one of the greatest living mathematicians, making his commentary particularly authoritative.

**Tags**: `#ai-ethics`, `#mathematics`, `#open-science`, `#ai-research`, `#academic-culture`

---
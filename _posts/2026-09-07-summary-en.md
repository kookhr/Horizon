---
layout: default
title: "Horizon Summary: 2026-09-07 (EN)"
date: 2026-09-07
lang: en
---

> From 33 items, 6 important content pieces were selected

---

1. [Abusive AI Crawlers Consume More CPU Than All Legitimate Traffic on git.kernel.org](#item-1) ⭐️ 8.0/10
2. [Research acceleration: The view inside OpenAI](#item-2) ⭐️ 8.0/10
3. [Google Externalizes TPU Inference Stack via InferenceX, Challenging NVIDIA CUDA Moat](#item-3) ⭐️ 8.0/10
4. [Yandex Proposes KV-Cache as an Interactive Agent Runtime](#item-4) ⭐️ 8.0/10
5. [Longitudinal Study Reveals Significant Day-to-Day Performance Drift in API-Served LLMs](#item-5) ⭐️ 8.0/10
6. [黄仁勋称 GPT-6 Astra 标志 AGI 到来，模型由约 10 万颗 NVLink72 芯片训练](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Abusive AI Crawlers Consume More CPU Than All Legitimate Traffic on git.kernel.org](https://simonwillison.net/2026/Sep/7/creepy-crawlies/) ⭐️ 8.0/10

Konstantin Ryabitsev published a technical analysis revealing that abusive crawlers now consume more CPU cycles on git.kernel.org than all legitimate access combined, with 14 CPU cores across 5 geo-distributed nodes continuously rendering git commits as HTML for scrapers. AI crawlers are burdening the infrastructure with approximately 6 million daily requests. This exposes a systemic and worsening infrastructure crisis where AI scrapers impose unsustainable costs on critical open-source projects like the Linux kernel repository, threatening the viability of free public services. The problem extends far beyond kernel.org to any web service serving crawlable content, raising urgent questions about accountability and the need for collective defensive measures. The 14 continuously-busy CPU cores are spread across 5 geo-distributed nodes and are dedicated solely to rendering git commits into HTML for bot scrapers. Ryabitsev's post includes graphs showing crawler-versus-clone traffic share, the Anubis difficulty curve, and the request funnel, providing concrete evidence of the resource imbalance.

rss · Simon Willison · Sep 7, 23:08

**Background**: git.kernel.org is the official Git repository hosting the Linux kernel source code, serving developers worldwide through both git protocol operations (like clones and pulls) and a web interface that renders commits as browsable HTML. Rendering git commits as HTML is significantly more CPU-intensive than serving raw git data, because it involves parsing diffs, syntax highlighting, and generating full web pages. The rise of AI companies deploying aggressive crawlers to scrape web content for training data has created what Ryabitsev calls 'background radiation' — a constant, draining load of automated requests that provides zero benefit to the hosting project.

<details><summary>References</summary>
<ul>
<li><a href="https://elsolitario.org/en/2026/08/30/kernel-org-ai-bots-anubis-cpu/">AI Crawlers: Kernel.org Burns 14 CPU Cores</a></li>
<li><a href="https://securityonline.info/ai-crawlers-git-kernel/">AI Crawlers Burden git.kernel.org With Millions of Requests</a></li>
<li><a href="https://ettayeb.fr/en/linux/git-kernel-org-ai-crawlers-2026/">AI crawlers burn 20% of git.kernel.org CPU scraping commits one by one — ETTAYEB</a></li>

</ul>
</details>

**Discussion**: Simon Willison highlighted this issue from his own perspective, noting that he worries about the same problem affecting Datasette, which serves a huge number of crawlable web pages. The Hacker News discussion amplified concerns about the broader pattern of AI companies externalizing infrastructure costs onto open-source and public-interest projects without contributing resources in return.

**Tags**: `#crawling`, `#infrastructure`, `#web-scraping`, `#linux-kernel`, `#abuse`

---

<a id="item-2"></a>
## [Research acceleration: The view inside OpenAI](https://simonwillison.net/2026/Sep/6/research-acceleration-the-view-inside-openai/) ⭐️ 8.0/10

OpenAI shares details about how their research team uses coding agents at scale, alongside announcements about 'RSI' (Recursive Self-Improvement) as their new AGI concept, with data showing dramatic growth in agentic engineering adoption throughout 2026.

rss · Simon Willison · Sep 6, 23:57

**Tags**: `#openai`, `#coding-agents`, `#agi`, `#recursive-self-improvement`, `#agentic-engineering`

---

<a id="item-3"></a>
## [Google Externalizes TPU Inference Stack via InferenceX, Challenging NVIDIA CUDA Moat](https://newsletter.semianalysis.com/p/tpu-inferencex-full-steam) ⭐️ 8.0/10

SemiAnalysis reports that Google is rapidly externalizing its TPU inference stack through InferenceX, achieving up to 50% better performance per dollar compared to alternatives, with new TPU variants including Ironwood (7th generation) and TPUv8i (8th generation inference-specialized chip). Google's eighth-generation TPU marks the first time the company has bifurcated its architecture into separate training (TPU 8t) and inference (TPU 8i) chips. This represents a significant competitive shift in the AI hardware landscape, directly challenging NVIDIA's CUDA ecosystem moat that has long dominated AI inference workloads. If Google's performance-per-dollar claims hold up with a growing customer base, it could reshape cloud AI inference economics and accelerate the industry's diversification away from NVIDIA-only stacks. Ironwood (TPU7x) delivers 4,614 TFLOP/s peak computational performance and is the first Google TPU designed specifically for inference, while TPUv8i features 19.2 Tbps scale-up bandwidth and 10 PFLOPs of peak inference processing with a boardfly topology for scalable AI inference. The bifurcation strategy reportedly involves Broadcom for training chips and MediaTek for inference chips, representing notable supply chain diversification.

rss · Semianalysis · Sep 7, 20:00

**Background**: Google's Tensor Processing Units (TPUs) are custom AI accelerators first introduced in 2016, originally designed for internal workloads like Search and later made available to cloud customers via Google Cloud. NVIDIA's CUDA platform has long been the dominant software ecosystem for AI compute, creating a significant competitive moat that hardware competitors have struggled to overcome. InferenceX represents Google's strategic push to make its previously internal TPU inference stack accessible and competitive for external customers running large language model inference workloads. The move from general-purpose TPUs to inference-specialized chips reflects the industry's shift from training-centric to inference-centric AI infrastructure as model deployment scales.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/infrastructure-and-cloud/google-cloud/ironwood-tpu-age-of-inference/">Ironwood: The first Google TPU for the age of inference</a></li>
<li><a href="https://en.wikipedia.org/wiki/Tensor_Processing_Unit">Tensor Processing Unit - Wikipedia</a></li>
<li><a href="https://wccftech.com/google-splits-tpuv8-strategy-two-chips-broadcom-training-mediatek-inference-duties/">Google Splits TPUv8 Strategy Into Two Chips ... - Wccftech</a></li>

</ul>
</details>

**Tags**: `#TPU`, `#AI Hardware`, `#Inference`, `#Google Cloud`, `#CUDA`

---

<a id="item-4"></a>
## [Yandex Proposes KV-Cache as an Interactive Agent Runtime](https://www.reddit.com/r/MachineLearning/comments/1w9myqc/kv_cache_as_an_agent_runtime_r/) ⭐️ 8.0/10

Yandex researchers published a blog post proposing that LLM KV-cache state can be actively modified during inference to serve as a runtime mechanism for interactive agents, building on their prior papers Hogwild! Inference and AsyncReasoning. They also previewed a Qwen3.8-27B agent playing DOOM interactively using these techniques. This work identifies inference/runtime design as an under-explored axis of agent capabilities, positioned between costly model retraining and overly abstract harness engineering. If proven viable, it could enable more responsive and interactive LLM agents without requiring architectural changes to the underlying model. The approach builds on Hogwild! Inference, a parallel LLM inference engine where multiple instances of the same model run concurrently sharing a single attention cache, and AsyncReasoning for asynchronous reasoning patterns. The DOOM demo uses a Qwen3.8-27B model, though detailed performance metrics and broader limitations are not fully specified in the blog post.

reddit · r/MachineLearning · /u/_puhsu · Sep 7, 09:03

**Background**: KV cache is a foundational optimization in Transformer-based LLMs that stores intermediate key and value computations from attention layers during inference, eliminating redundant recomputation of past token representations during autoregressive generation and substantially speeding up text generation. Traditionally, the KV cache is treated as a passive storage mechanism that is written to and read from but not actively manipulated. Yandex's approach reimagines it as a mutable runtime state that can be directly modified to achieve interactivity, occupying a middle ground between changing the model (expensive, requires retraining) and changing the harness (too abstract, limited by the model's fixed behavior).

<details><summary>References</summary>
<ul>
<li><a href="https://magazine.sebastianraschka.com/p/coding-the-kv-cache-in-llms">Understanding and Coding the KV Cache in LLMs from Scratch</a></li>
<li><a href="https://arxiv.org/abs/2504.06261">Hogwild ! Inference : Parallel LLM Generation via Concurrent Attention</a></li>
<li><a href="https://github.com/yandex-research/AsyncReasoning">GitHub - yandex-research/AsyncReasoning</a></li>

</ul>
</details>

**Discussion**: Detailed community comments were not provided with the news item, so discussion sentiment and viewpoints cannot be fully assessed at this time.

**Tags**: `#kv-cache`, `#llm-agents`, `#inference-runtime`, `#interactive-ai`, `#research`

---

<a id="item-5"></a>
## [Longitudinal Study Reveals Significant Day-to-Day Performance Drift in API-Served LLMs](https://www.reddit.com/r/MachineLearning/comments/1w9llr4/measuring_llm_performance_drift_observations_and/) ⭐️ 8.0/10

The post introduces a longitudinal benchmarking methodology that continuously evaluates API-served LLMs across coding, multi-turn reasoning, and tool use, analyzing 31,352 repeated score observations across 49 models. The key finding is that between-day daily median standard deviation (8.43 points) was roughly 3× larger than within-day standard deviation (2.80 points), suggesting temporal variation in model performance that snapshot benchmarks fail to capture. This work challenges the dominant snapshot-based benchmark paradigm by demonstrating that API-served LLMs exhibit measurable performance variation over time, which has direct implications for production ML reliability, model selection decisions, and the scientific validity of published benchmark scores. The methodology provides a framework for distinguishing genuine capability changes from infrastructure effects, which is critical for organizations relying on API-served models in production systems. The methodology uses versioned benchmark configurations and only compares longitudinal observations under compatible measurement conditions, employs execution-based evaluation rather than LLM-as-judge, separates availability failures from valid task outcomes, and applies change-point detection over the resulting time series. The authors deliberately withhold the exact live task bank to reduce benchmark contamination while publishing the full methodology, assumptions, and statistical interpretation in a public PDF.

reddit · r/MachineLearning · /u/ionutvi · Sep 7, 07:44

**Background**: LLM performance drift refers to the phenomenon where API-served language models exhibit changing behavior over time due to factors like serving infrastructure updates, provider configuration changes, model version transitions, or even silent behavioral changes without public version announcements. Traditional benchmarking treats model scores as stable snapshots, but this assumption breaks down when the underlying model behind an API endpoint can change unpredictably. Benchmark contamination is another growing concern—once benchmarks become publicly visible, the test data itself may enter model training corpora, invalidating future measurements. The longitudinal approach borrows from change-point detection and time-series analysis to treat benchmarking as an ongoing measurement problem rather than a one-time evaluation event.

<details><summary>References</summary>
<ul>
<li><a href="https://aistupidlevel.info/asl-public-benchmark-methodology-2026.pdf">PUBLIC BENCHMARK METHODOLOGY / 2026 Measuring change ...</a></li>
<li><a href="https://medium.com/@tsiciliani/drift-detection-in-large-language-models-a-practical-guide-3f54d783792c">Drift Detection in Large Language Models: A Practical Guide | by Tony Siciliani | Medium</a></li>
<li><a href="https://nexla.com/ai-infrastructure/data-drift/">Data Drift in LLMs—Causes, Challenges, and Strategies | Nexla</a></li>

</ul>
</details>

**Tags**: `#LLM-benchmarking`, `#performance-drift`, `#evaluation-methodology`, `#API-models`, `#longitudinal-analysis`

---

<a id="item-6"></a>
## [黄仁勋称 GPT-6 Astra 标志 AGI 到来，模型由约 10 万颗 NVLink72 芯片训练](https://mp.weixin.qq.com/s/PJp4LEoiZPYqz3Mclqr7xg) ⭐️ 8.0/10

Jensen Huang declares AGI has arrived with OpenAI's GPT-6 Astra, reportedly trained on ~100,000 NVIDIA Grace Blackwell NVLink72 chips, while Altman downplays the AGI label as a vague marketing term.

telegram · zaihuapd · Sep 7, 04:54

**Tags**: `#AGI`, `#GPT-6`, `#NVIDIA`, `#OpenAI`, `#AI-infrastructure`

---
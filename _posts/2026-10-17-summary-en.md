---
layout: default
title: "Horizon Summary: 2026-10-17 (EN)"
date: 2026-10-17
lang: en
---

> From 37 items, 7 important content pieces were selected

---

1. [Claude Solves NIST ECDSA Curve Seed Mystery](#item-1) ⭐️ 9.0/10
2. [Tesla Roadster](#item-2) ⭐️ 8.0/10
3. [How the Claude Code Team Approaches AI-Assisted Code Review](#item-3) ⭐️ 8.0/10
4. [Big Fish: Exploiting a 37-Year-Old Kernel Bug in OpenBSD](#item-4) ⭐️ 8.0/10
5. [ORL Accelerates Diffusion LLMs to 2,788 tokens/s on Single RTX 5090](#item-5) ⭐️ 8.0/10
6. [China Proposes Temporary Export Registration for 40 Key Technologies Across AI, Biopharma, and Photovoltaics](#item-6) ⭐️ 8.0/10
7. [Anthropic IPO 估值预期降至 1.5 万亿美元](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Claude Solves NIST ECDSA Curve Seed Mystery](https://www.anthropic.com/research/ecdsa-curve-origins) ⭐️ 9.0/10

Anthropic's Claude AI discovered that the seeds for NIST elliptic curves P-192, P-224, P-256, P-384, and P-521 were generated using the C library's lrand48 random number generator seeded with a Unix timestamp, not by hashing a memorable phrase as many suspected. The discovery was made in under half an hour, solving a cryptographic mystery that has persisted for over a decade. This resolves years of speculation that the NSA deliberately chose curve seeds with hidden weaknesses, a concern that has influenced cryptographic standard selection and fueled distrust in NIST curves. It also represents a landmark demonstration of LLMs applied to cryptanalysis, showing that AI models can productively explore hypotheses in specialized technical domains where human experts had been stuck for years. The fifth binary curve seed, B-163, does not fit any pattern Claude tried and remains unexplained; one plausible theory is that a digit was mistyped during publication. Anthropic chose the higher of two bounty amounts and donated it to ISRG (Internet Security Research Group). Critics note that while the generation method is confirmed, the selection process over months means discarded candidates cannot be examined, so the possibility of selection-based weaknesses cannot be fully ruled out.

hackernews · ahlCVA · Oct 16, 18:55 · [Discussion](https://news.ycombinator.com/item?id=50122800)

**Background**: NIST adopted ECDSA in 2000 as part of FIPS 186-2, specifying standard elliptic curves for digital signatures. Each curve was defined using a seed value, and NIST never explained how these seeds were chosen, leading to speculation that the NSA might have selected seeds that produce curves with known vulnerabilities exploitable only by the agency. Researchers like Daniel Bernstein and Tanja Lange raised backdoor concerns as early as 1999. A $12,000 bounty was eventually offered to anyone who could trace the seeds' origins, which Filippo Valsorda and others promoted.

<details><summary>References</summary>
<ul>
<li><a href="https://www.explainx.ai/blog/claude-ecdsa-nist-curve-seeds-lrand48-anthropic-frontier-red-team-backdoor-question-2026">ECDSA Curve Seeds Solved: Claude Found lrand48 (2026 ...</a></li>
<li><a href="https://www.unite.ai/anthropic-says-claude-traced-nist-ecdsa-curve-seeds-to-a-1990s-rng/">Anthropic Says Claude Traced NIST ECDSA Curve Seeds to a ...</a></li>
<li><a href="https://www.itsecuritylocksmith.co.uk/the-nist-elliptic-curve-bounty/">The NIST Elliptic Curve seeds, the NSA and the $12k bounty</a></li>

</ul>
</details>

**Discussion**: The Hacker News discussion (595 points, 249 comments) reflects a mix of amusement and relief, with users joking that the NSA employee responsible may have been quietly laughing for 25 years, and quipping about "13 years of tinfoil hats for srand48(time(NULL))." More serious technical comments caution that while the generation method is confirmed, the selection process remains opaque—discarded candidates cannot be examined, so curve selection-based attacks remain theoretically possible. Several commenters praise Anthropic for donating the bounty to ISRG, and speculate that the unexplained B-163 seed may simply be a typo.

**Tags**: `#cryptography`, `#ai`, `#security`, `#elliptic-curves`, `#llm`

---

<a id="item-2"></a>
## [Tesla Roadster](https://www.tesla.com/roadster) ⭐️ 8.0/10

Tesla unveiled a new Roadster prototype equipped with cold-gas thrusters and rocket engines that can hover and drive vertically, sparking intense debate about its engineering feasibility and likelihood of actual production.

hackernews · shekhar101 · Oct 16, 01:32 · [Discussion](https://news.ycombinator.com/item?id=50112657)

**Tags**: `#tesla`, `#automotive`, `#rocketry`, `#engineering`, `#product-announcement`

---

<a id="item-3"></a>
## [How the Claude Code Team Approaches AI-Assisted Code Review](https://claude.dev/blog/solving-code-review-at-anthropic/) ⭐️ 8.0/10

Anthropic published a blog post detailing how the Claude Code team uses AI to automate and scale code review, reportedly handling up to 30,000 pull requests per day. The system categorizes changes by risk level and routes them through automated checks, with human attention focused only where risk is highest. This approach signals a potential paradigm shift in software engineering, where AI handles the bulk of code review volume and humans focus on high-risk decisions. If scalable, it could fundamentally reshape engineering team structures, review workflows, and the skills valued in senior engineers. The system uses risk-tiered routing where low-risk changes (docs, copy, internal-only features) can be merged without human review once automated checks pass. The team maintains an evolving eval suite that grows with every incident, and each reviewer change is scored against the full eval set.

hackernews · pretext · Oct 16, 19:04 · [Discussion](https://news.ycombinator.com/item?id=50122951)

**Background**: Claude Code is Anthropic's agentic coding tool that operates in the terminal and IDE, capable of understanding codebases, editing files, and running commands. Traditional code review requires human engineers to manually read and approve pull requests, which becomes a bottleneck as teams and code velocity grow. AI-assisted code review tools like CodeRabbit and Sonar have emerged to address this scalability challenge, but Anthropic's approach appears to push further toward full automation for low-risk changes.

<details><summary>References</summary>
<ul>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI Coding Agent, Terminal, IDE</a></li>
<li><a href="https://www.coderabbit.ai/">AI Code Reviews | CodeRabbit | Try for Free.</a></li>
<li><a href="https://www.sonarsource.com/">AI Code Review & Verification Tools | Code Security | Sonar</a></li>

</ul>
</details>

**Discussion**: Community sentiment is highly skeptical, with commenters questioning whether 30,000 PRs/day reflects genuine productivity or excessive churn and code rewrites. Several users expressed concern about allowing LLMs to write documentation without human review, and others debated the cost per line of code and whether the team truly has control over its codebase at that scale.

**Tags**: `#AI`, `#code-review`, `#Anthropic`, `#software-engineering`, `#automation`

---

<a id="item-4"></a>
## [Big Fish: Exploiting a 37-Year-Old Kernel Bug in OpenBSD](https://calif.io/research/big-fish) ⭐️ 8.0/10

Security researchers from Calif published a proof-of-concept exploit on October 16, 2024, demonstrating a local privilege escalation attack on OpenBSD that chains two long-existing kernel flaws, the oldest dating back approximately 37 years to the original BSD source code. The exploit leverages a signed 16-bit short integer overflow in the SysV shared memory attachment counter—triggered by forking 259 processes—combined with a use-after-free race condition and an out-of-bounds write in IP multicast options handling to bypass SMAP/SMEP protections and gain root access. This discovery is significant because it demonstrates that critical vulnerabilities can persist for decades even in OpenBSD, which is widely regarded as one of the most security-focused and heavily audited operating systems in existence. It highlights the limitations of manual code review for catching certain classes of bugs—particularly integer overflow and race condition combinations—and raises important questions about whether automated tools like fuzzing or static analysis could have detected this issue earlier. The core vulnerability lies in the SysV shared memory attachment counter, which was implemented as a signed 16-bit short, meaning it could only count up to 32,767 before overflowing. By forking 259 processes to overflow this counter, the researchers created a use-after-free condition, which they then raced against another thread while simultaneously exploiting an out-of-bounds write in IP multicast options handling to bypass modern hardware security features like SMAP (Supervisor Mode Access Prevention) and SMEP (Supervisor Mode Execution Prevention).

hackernews · rs_rs_rs_rs_rs · Oct 16, 14:44 · [Discussion](https://news.ycombinator.com/item?id=50118977)

**Background**: OpenBSD is a Unix-like operating system renowned for its proactive security stance and rigorous source code auditing, having pioneered security innovations like OpenSSH and the concept of proactive security auditing. The SysV shared memory subsystem is a System V IPC (Inter-Process Communication) mechanism that allows multiple processes to share memory regions, with an attachment counter tracking how many processes have mapped a given segment. SMAP and SMEP are CPU hardware security features introduced by Intel that prevent the kernel from accessing or executing code in user-space memory, making exploitation significantly harder. The bug traces back to the original BSD source code that OpenBSD forked from, predating OpenBSD's own extensive security audits.

<details><summary>References</summary>
<ul>
<li><a href="https://cybersecuritynews.com/37-year-old-kernel-openbsd-flaw/">37-Year-Old Kernel Flaw Exploited to Gain Root Access on ...</a></li>
<li><a href="https://daily.dev/posts/big-fish-exploiting-a-37-year-old-kernel-bug-in-openbsd-u6hc8g4lt">Big Fish: Exploiting a 37-Year-Old Kernel Bug in OpenBSD</a></li>
<li><a href="https://www.openbsd.org/security.html">OpenBSD: Security</a></li>

</ul>
</details>

**Discussion**: The community discussion centered on the remarkable longevity of the bug and the challenges of detecting such vulnerability classes. One commenter noted that NetBSD accidentally fixed the same bug during a code rewrite in August 1999, while another raised the key question of whether fuzzing or static analysis could have realistically caught this class of bug, or if it required human reasoning about exploit primitives to discover.

**Tags**: `#security`, `#kernel`, `#openbsd`, `#exploitation`, `#vulnerability-research`

---

<a id="item-5"></a>
## [ORL Accelerates Diffusion LLMs to 2,788 tokens/s on Single RTX 5090](https://www.reddit.com/r/MachineLearning/comments/1x7qgr0/research_2788_tokenss_on_a_single_rtx_5090_with_a/) ⭐️ 8.0/10

Researchers introduced ORL (On-Policy Residual Learning), a method that accelerates diffusion language models by training on fresh, self-generated trajectories and applying Adjacent Entropy Contraction to reduce uncertainty faster per denoising step. Combined with a custom CUDA-graph-based inference engine called dlmrt, the approach achieves 2,788 tokens/s on a single RTX 5090 and up to 6.9× higher end-to-end throughput, with all models, training code, and inference engine fully open-sourced. Diffusion language models are an emerging alternative to autoregressive LLMs, but their practical adoption has been limited by slow convergence during iterative denoising. ORL directly addresses this bottleneck, demonstrating that diffusion LLMs can achieve competitive or superior throughput compared to autoregressive speculative decoding methods like DFlash and EAGLE3, potentially making diffusion-based text generation viable for production use. ORL's two core techniques are on-policy residual learning, which avoids train-inference distribution mismatch by replaying exact residual states from the current model, and Adjacent Entropy Contraction, which gates the loss to push only uncertain predictions. The dlmrt engine captures the entire denoising loop in a CUDA graph for GPU-side execution and supports NVFP4 inference on Blackwell GPUs; all reported numbers are single-request (batch size 1) peak results, not aggregate throughput.

reddit · r/MachineLearning · /u/arty_photography · Oct 16, 20:03

**Background**: Diffusion language models (dLLMs) generate text through iterative denoising rather than sequential next-token prediction, allowing multiple tokens to be refined and finalized in parallel. Unlike autoregressive models that generate one token at a time, diffusion models start from fully masked sequences and progressively reveal tokens, similar to how image diffusion models like Stable Diffusion work. A key challenge has been reducing the number of forward passes needed for convergence, which ORL tackles by carrying forward previous predictions as residual context and training on-policy to match inference conditions.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/blog/ProCreations/diffusion-language-model">Diffusion Language Models: The New Paradigm - Hugging Face</a></li>
<li><a href="https://arxiv.org/abs/2502.09992">[2502.09992] Large Language Diffusion Models - arXiv.org Diffusion Language Models: An Experimental Analysis Awesome Diffusion Language Models How to Build a Diffusion Language Model | Kuleshov Group Large Language Diffusion Models</a></li>

</ul>
</details>

**Tags**: `#diffusion-models`, `#language-models`, `#inference-optimization`, `#open-source`, `#machine-learning`

---

<a id="item-6"></a>
## [China Proposes Temporary Export Registration for 40 Key Technologies Across AI, Biopharma, and Photovoltaics](https://aqygzj.mofcom.gov.cn/flzc/gzjgfxwj/art/2026/art_c99f95ca0cd043829ac9991495fc283c.html) ⭐️ 8.0/10

China's Ministry of Commerce has proposed revising the 'Catalog of Technologies Prohibited and Restricted from Export,' seeking public comment on implementing temporary export registration for 40 technologies across three strategic sectors: AI (23 items including large models, agents, and computing clusters), biopharmaceuticals (5 items including cell/gene therapy and small nucleic acid drugs), and photovoltaics (12 items covering polysilicon, wafer, and cell manufacturing). Technologies already in the public domain through open-source releases or academic publications are explicitly exempted from the management scope. This regulatory development signals China's intent to tighten controls on the export of strategically important technologies, particularly in AI where large models and computing clusters are at the forefront of global competition. The policy could significantly impact international technology transfer, cross-border R&D collaborations, and global supply chains in these three critical sectors, while the open-source exemption provides a nuanced carve-out that preserves academic and open collaboration channels. The photovoltaics management scope extends beyond technology itself to include key and core equipment embodying those technologies. For biopharmaceuticals, non-ownership-transfer licensing arrangements qualify for automatic licensing and other facilitative measures, offering a lighter regulatory touch for certain commercial models. The AI category's 23 technologies represent the largest share, reflecting the sector's strategic priority in current export control considerations.

telegram · zaihuapd · Oct 16, 09:12

**Background**: China maintains a technology export control system through the 'Catalog of Technologies Prohibited and Restricted from Export,' which classifies technologies into prohibited and restricted categories. Temporary export registration requires exporters to register with authorities before exporting controlled technologies, serving as a lighter-touch regulatory mechanism compared to full export licenses. The three targeted sectors — AI, biopharmaceuticals, and photovoltaics — are all areas where China holds significant technological capabilities and global market share. For example, small nucleic acid drugs are a novel therapeutic class based on RNA interference (RNAi) or antisense oligonucleotide (ASO) technology that regulates gene expression by targeting mRNA.

<details><summary>References</summary>
<ul>
<li><a href="https://zhuanlan.zhihu.com/p/1979127551893985088">小核酸药物行业深度：发展现状、发展空间、技术突破、产业链及相关公...</a></li>
<li><a href="https://zhuanlan.zhihu.com/p/2075906064407597214">CDE老师文章解读 | 小核酸药物临床研发和评价的思考</a></li>

</ul>
</details>

**Tags**: `#AI policy`, `#export controls`, `#regulation`, `#China`, `#technology transfer`

---

<a id="item-7"></a>
## [Anthropic IPO 估值预期降至 1.5 万亿美元](https://www.reuters.com/business/finance/investors-temper-anthropic-ipo-valuation-expectations-over-revenue-growth-2026-10-15/) ⭐️ 8.0/10

Investors have lowered Anthropic's IPO valuation expectations to $1.5 trillion due to slowing growth, model price competition, and compute costs, despite strong Q3 revenue of $16.8 billion.

telegram · zaihuapd · Oct 16, 15:46

**Tags**: `#Anthropic`, `#IPO`, `#AI Valuation`, `#Investment`, `#Market Analysis`

---
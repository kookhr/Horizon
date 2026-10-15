---
layout: default
title: "Horizon Summary: 2026-10-15 (EN)"
date: 2026-10-15
lang: en
---

> From 44 items, 4 important content pieces were selected

---

1. [Anthropic Replaces Git with Custom Version Control System Scion](#item-1) ⭐️ 9.0/10
2. [Google Silently Links Phone Numbers Across All Signed-In Android Accounts](#item-2) ⭐️ 8.0/10
3. [Tracing and Cutting Out LLM 'Slop' Style via Mechanistic Interpretability](#item-3) ⭐️ 8.0/10
4. [First Stargardt Patient Implanted with PRIMA Vision Chip Reads Words](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Anthropic Replaces Git with Custom Version Control System Scion](https://www.anthropic.com/engineering/redesigning-source-control) ⭐️ 9.0/10

Anthropic has fully migrated its internal monorepo from Git to Scion, a custom version control system built by a seven-engineer team in just five months. The new system delivers approximately 100x faster CI checkouts, uses only 1/200th of the CPU and memory of the previous git mirror architecture, and saves 25% on CI compute costs. As Anthropic's daily code merges grew more than tenfold—from roughly 2,500 in May 2026 to over 30,000 by September—Git became the single biggest development bottleneck. Scion's architecture, which keeps clients always-online and offloads computation to the server with distributed data storage, demonstrates that purpose-built version control can dramatically outperform general-purpose tools like Git at extreme scale. Scion's design shifts heavy computation from individual developer machines to a centralized server, with data stored in a distributed manner rather than replicated as full mirrors. The migration was completed by a team of only seven engineers, and the system now handles over 30,000 daily merges while reducing CI compute usage by 25%.

telegram · zaihuapd · Oct 14, 02:30

**Background**: Git is a distributed version control system where every developer has a full copy of the repository, including its entire history. At very large scale—especially with monorepos containing massive codebases and histories—Git operations like cloning, fetching, and CI checkouts become extremely resource-intensive. Companies like Datadog have previously built custom Git mirror layers (e.g., gitretriever) to serve code to CI systems at scale, but Anthropic chose to go further by replacing Git entirely with a purpose-built system.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/engineering/redesigning-source-control">Redesigning source control at Anthropic</a></li>
<li><a href="https://tech-insider.org/anthropic-scion-source-control-30000-merges-2026/">Anthropic Scion: 30,000 Code Merges a Day Explained</a></li>
<li><a href="https://www.datadoghq.com/blog/engineering/gitretriever/">20× the CI traffic without getting slower: How we rebuilt Git ...</a></li>

</ul>
</details>

**Tags**: `#version-control`, `#anthropic`, `#devops`, `#ci-cd`, `#engineering`

---

<a id="item-2"></a>
## [Google Silently Links Phone Numbers Across All Signed-In Android Accounts](https://www.androidauthority.com/google-auto-phone-number-verification-android-3723117/) ⭐️ 8.0/10

Google has made Android's phone number verification opt-out, automatically verifying and associating a device's phone number with every Google account signed in on that phone, including secondary and work accounts. Google updated its documentation between August and October 2025 to reflect this behavior change. This change significantly erodes user privacy by silently de-anonymizing users who maintain separate Google accounts for different purposes, as all accounts become linked through a single phone number. It also raises the risk of centralized account lockout, where a single policy violation could cascade across all linked accounts, leaving users with no recourse. The phone number linking occurs without explicit prompts or user consent during the sign-in process, and users have reported difficulty finding settings to disable it. The behavior affects all account types signed in on the device, including secondary, work, and alt profiles, effectively treating the phone number as a universal identifier across the Google ecosystem.

hackernews · Brajeshwar · Oct 14, 16:28 · [Discussion](https://news.ycombinator.com/item?id=50090349)

**Background**: Phone number verification on Android previously required explicit user action to link a number to a Google account. De-anonymization is the practice of matching anonymous or separately-identified data with publicly available information to identify individuals, and phone numbers have increasingly become a de facto identity document on the internet. Google, as both the largest ad-tech company and the dominant mobile operating system provider, occupies a unique position where linking phone numbers across accounts creates a powerful cross-account identity graph.

<details><summary>References</summary>
<ul>
<li><a href="https://ccstartup.com/blog/2026/10/14/psa-google-is-silently-linking-your-phone-number-across-all-signed-in-accounts/">PSA: Google is silently linking your phone number across all ...</a></li>
<li><a href="https://support.google.com/android/thread/348794711/automatically-linking-of-phone-number?hl=en">Automatically linking of phone number - Android Community</a></li>

</ul>
</details>

**Discussion**: Community sentiment is overwhelmingly negative, with users criticizing Google as the most aggressive anti-privacy big tech company and expressing frustration that phone numbers have become the de facto social security number of the internet. Multiple commenters raise concerns about centralized account lockout risk, where one misstep could cascade across all linked accounts, and some advocate for regulatory intervention to prevent a single entity from controlling OS, browser, search, and email simultaneously. Privacy-focused users, including GrapheneOS users, report additional friction as they avoid Google Play services.

**Tags**: `#privacy`, `#google`, `#android`, `#security`, `#deanonymization`

---

<a id="item-3"></a>
## [Tracing and Cutting Out LLM 'Slop' Style via Mechanistic Interpretability](https://www.reddit.com/r/MachineLearning/comments/1x64lbk/tracing_where_llm_slop_style_comes_from_in_the/) ⭐️ 8.0/10

The author used difference-in-means and logit-lens techniques on Qwen3-4B-Instruct and OLMo 2 1B to trace 'AI slop' writing style to specific representational directions, finding that base models already contain these directions but SFT introduces rhetorical structures and DPO amplifies buzzwords and formatting. A rank-16 LoRA distilled from fixed-vector subtraction at layers 12–23 reduced the slop score by 83% with minimal KL divergence and no QA degradation. This study provides the first detailed mechanistic account of how each alignment training stage contributes to the recognizable 'AI slop' style, offering actionable insights for alignment researchers to mitigate it at the representation level rather than relying solely on token-level bans. The cross-lingual findings and multi-stage training analysis on OLMo 2 reveal that preference data itself may be a key source of slop, since chosen responses were sloppier in 57% of pairs. Directional ablation paradoxically increased slop by up to 89% because clean text projects negatively on the slop axis, so the author used fixed-vector subtraction constrained to a narrow KL budget of ~0.4 nats/token on human text. The per-trope directions are cross-lingual (e.g., 'not X, but Y' promotes Chinese 而是), and the slop scorer is a custom regex detector with no human evaluation yet.

reddit · r/MachineLearning · /u/Imaginary_Money2285 · Oct 14, 22:08

**Background**: Mechanistic interpretability is a subfield of explainable AI that reverse-engineers the internal mechanisms of neural networks to understand how they compute outputs from inputs. Difference-in-means is a technique that identifies a direction in the model's representation space by averaging activations across contrasting datasets (e.g., exaggerated vs. plain writing), while the logit lens projects intermediate hidden states into the output vocabulary space to reveal evolving predictions at each layer. 'AI slop' refers to the recognizable but formulaic writing style common in LLM outputs—em dashes, 'not X, but Y' constructions, lists of three, and buzzwords—which many users find undesirable. SFT (supervised fine-tuning) and DPO (direct preference optimization) are two key post-training stages that transform a base language model into an aligned assistant.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mechanistic_interpretability">Mechanistic interpretability - Wikipedia</a></li>
<li><a href="https://www.emergentmind.com/topics/logit-lens-framework">Logit - Lens Framework for Transformer Interpretability</a></li>

</ul>
</details>

**Tags**: `#LLm interpretability`, `#mechanistic interpretability`, `#AI slop`, `#alignment`, `#training dynamics`

---

<a id="item-4"></a>
## [First Stargardt Patient Implanted with PRIMA Vision Chip Reads Words](https://science.xyz/news/stargardt-first-rehab/) ⭐️ 8.0/10

Science Corporation successfully implanted its PRIMA visual restoration chip in a Stargardt disease patient at Sydney Eye Hospital in Australia in May, with the patient progressing from seeing letters during initial rehabilitation to reading a full word in a second session. The results were announced by CEO Max Hodak. This marks the first time a photovoltaic retinal implant has been applied to Stargardt disease, an incurable inherited condition causing blindness in roughly 150,000 people worldwide, demonstrating that neuroprosthetic vision restoration can be extended beyond age-related macular degeneration to a broader patient population. If clinical trials succeed, it could offer a viable treatment option for a disease that currently has no cure. The PRIMA chip is a 2-millimeter photovoltaic device that replaces damaged light-sensitive retinal cells by converting incoming light into electrical signals, and it has already received European regulatory approval for use in dry age-related macular degeneration. This Stargardt implantation is part of an ongoing clinical trial, and the patient's rapid progress from letter recognition to word reading occurred over just two rehabilitation sessions.

telegram · zaihuapd · Oct 14, 04:30

**Background**: Stargardt disease is the most common inherited single-gene retinal disorder, typically linked to bi-allelic ABCA4 gene variants, and causes progressive macular degeneration beginning in childhood, adolescence, or adulthood. The disease damages the retina's outer layer, leading to irreversible vision loss with no currently available cure. PRIMA, developed by Science Corporation, is a subretinal implant designed to bypass damaged photoreceptors by directly stimulating the retina's remaining neural layers with light-converted electrical signals. The device had previously been studied and approved in Europe for geographic atrophy secondary to dry age-related macular degeneration, a condition that also destroys central vision.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Stargardt_disease">Stargardt disease</a></li>

</ul>
</details>

**Tags**: `#medical-technology`, `#neuroprosthetics`, `#vision-restoration`, `#bci`, `#science-corporation`

---
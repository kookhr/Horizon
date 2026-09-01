---
layout: default
title: "Horizon Summary: 2026-09-01 (EN)"
date: 2026-09-01
lang: en
---

> From 37 items, 5 important content pieces were selected

---

1. [Google Removes MV2 Extensions from Chrome Web Store, Disabling uBlock Origin](#item-1) ⭐️ 8.0/10
2. [Internet centralization and the original sin of NAT](#item-2) ⭐️ 8.0/10
3. [Sliding Window Attention with Sinks Outperforms Linear Attention on Long-Context Reasoning](#item-3) ⭐️ 8.0/10
4. [Tim Cook Steps Down as Apple CEO, John Ternus Takes Over with AI Focus](#item-4) ⭐️ 8.0/10
5. [DeepSeek Releases DeepSeek-V4-Flash-Vision-Exp Multimodal Model Weights](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Google Removes MV2 Extensions from Chrome Web Store, Disabling uBlock Origin](https://webiterate.dev/google-removed-extensions-ublock-origin-108/) ⭐️ 8.0/10

Google has completed the removal of Manifest V2 (MV2) extensions from the Chrome Web Store, effectively disabling uBlock Origin (UBO) on Chrome browsers. Over 85% of actively maintained extensions have already migrated to Manifest V3, and Chrome 139 will begin removing MV2 support entirely from the browser itself. This marks a concrete turning point in the ad blocking wars, as uBlock Origin was the most popular and effective ad blocker for Chrome, used by millions. The removal raises significant concerns about Google's monopolistic control over the web ecosystem, given that Google itself is the world's largest advertising company and stands to benefit from weakened ad blocking capabilities. Enterprise users with the ExtensionManifestV2Availability policy remain exempt until at least June 2025. While MV3 versions of major ad blockers exist (including uBlock Origin Lite, AdBlock, Adblock Plus, and AdGuard), MV3's declarativeNetRequest API imposes fundamental limitations on dynamic filtering capabilities compared to MV2's webRequest API. uBlock Origin's developer has confirmed the extension works best on Firefox, which continues to support MV2.

hackernews · twapi · Aug 31, 21:10 · [Discussion](https://news.ycombinator.com/item?id=49514878)

**Background**: Manifest V2 was introduced in 2012 and served as the standard Chrome extension platform for over a decade, allowing extensions like uBlock Origin to intercept and block network requests dynamically using the webRequest API. Manifest V3 replaces this with declarativeNetRequest, which requires extensions to declare filtering rules upfront rather than intercepting requests at runtime, ostensibly for performance and security reasons. Google announced the MV2 deprecation years ago, giving developers time to migrate, but many in the ad-blocking community argue MV3 fundamentally cripples content filtering capabilities. Firefox has chosen to maintain support for MV2 while also implementing MV3, positioning itself as the browser of choice for users who rely on robust ad blocking.

<details><summary>References</summary>
<ul>
<li><a href="https://developer.chrome.com/docs/extensions/develop/migrate/mv2-deprecation-timeline">Manifest V2 support timeline | Chrome for Developers</a></li>
<li><a href="https://blog.google/chromium/manifest-v2-phase-out-begins/">Manifest V2 phase-out begins</a></li>
<li><a href="https://dev.to/notearthian/whats-the-difference-between-manifest-v2-and-v3-in-browser-extensions-3b10">What's the Difference Between Manifest V2 and V3 in browser extensions? - DEV Community</a></li>

</ul>
</details>

**Discussion**: Community sentiment strongly favors migration to Firefox, with multiple users reporting seamless transitions and noting that uBlock Origin works best on Firefox anyway. A prominent theme is ad blocking as a safety issue—users describe elderly family members falling for malicious ads and argue Google's failure to filter harmful ads from its own services necessitates third-party blockers. Several commenters express deep distrust of Google's monopolistic control over web standards, with one noting the irony that Chrome was once celebrated in 2010 for making the web better, yet now users actively encourage friends and family to use anything but Chrome.

**Tags**: `#chrome`, `#ad-blocking`, `#uBlock-Origin`, `#manifest-v3`, `#browser-wars`

---

<a id="item-2"></a>
## [Internet centralization and the original sin of NAT](https://dreamstation.systems/personal/ntppost.html) ⭐️ 8.0/10

An essay arguing that NAT was an early 'original sin' that centralized the internet by eroding the ability to run public endpoints, sparking a rich discussion including the Linux NAT implementer reflecting on the trade-offs made.

hackernews · robinpie · Aug 31, 02:23 · [Discussion](https://news.ycombinator.com/item?id=49504905)

**Tags**: `#networking`, `#NAT`, `#internet-architecture`, `#decentralization`, `#linux`

---

<a id="item-3"></a>
## [Sliding Window Attention with Sinks Outperforms Linear Attention on Long-Context Reasoning](https://www.reddit.com/r/MachineLearning/comments/1w3j1vw/slidingwindow_attention_beats_linear_on/) ⭐️ 8.0/10

A new arXiv preprint by Alexia Jolicoeur-Martineau and colleagues demonstrates that Sliding Window Attention (SWA) with attention sinks achieves 2 to 10 times higher performance than linear attention variants on long-context reasoning benchmarks including Needle-in-a-Haystack and BABILong, without requiring any post-training. The authors argue that the linear attention research direction has been improperly benchmarked against simpler baselines. This finding directly challenges a major ongoing research direction where labs invest significant post-training compute to develop linear attention models for long-context LLMs, suggesting those resources may be better spent elsewhere. If validated, it could redirect how the industry approaches long-context efficiency, favoring a simpler, training-free method over more complex architectural changes. SWA with sinks requires no post-training, runs fast, and maintains low memory usage, while linear attention models likely need to be trained from scratch or undergo extensive post-training to even match SWA's performance. The authors strongly recommend switching to SWA instead of post-training linear models, though the paper remains an arXiv preprint awaiting peer validation.

reddit · r/MachineLearning · /u/Justgototheeffinmoon · Aug 31, 16:35

**Background**: Standard transformer attention has quadratic computational cost with respect to sequence length, motivating alternatives like linear attention (which replaces softmax with linear operations) and Sliding Window Attention (which restricts attention to a fixed-size window). Attention sinks are special tokens that absorb excess attention and act as structural anchors, stabilizing generation when older tokens are evicted by the sliding window. BABILong is a benchmark designed to test whether models can isolate and reason over sparse facts buried within extremely long distractor text, where even models claiming 128K token support like GPT-4 experience degradation.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/html/2608.28444v1">Sliding - window beats linear attention</a></li>
<li><a href="https://arxiv.org/abs/2406.10149">[2406.10149] BABILong : Testing the Limits of LLMs with Long ...</a></li>
<li><a href="https://carnotresearch.medium.com/let-the-chaos-sink-in-481c8a37471e">Let the Chaos Sink In. Balancing attention in transformers | Medium</a></li>

</ul>
</details>

**Tags**: `#attention-mechanisms`, `#long-context`, `#llm-efficiency`, `#linear-attention`, `#research`

---

<a id="item-4"></a>
## [Tim Cook Steps Down as Apple CEO, John Ternus Takes Over with AI Focus](https://www.bloomberg.com/news/articles/2026-08-30/apple-s-new-ceo-john-ternus-takes-reins-from-tim-cook-focusing-on-ai) ⭐️ 8.0/10

Tim Cook's last day as Apple CEO is August 31, with 51-year-old hardware engineering veteran John Ternus taking over on September 1 while Cook remains as executive chairman. Ternus's immediate priorities include accelerating AI deployment, addressing Siri upgrade delays, and launching Apple's first foldable iPhone at the September 9 fall event. This is the first CEO transition at Apple since Tim Cook succeeded Steve Jobs in 2011, marking a strategic pivot that places AI at the center of Apple's future. The leadership change comes at a critical moment when Apple faces mounting pressure to compete in AI capabilities against rivals like Google and OpenAI. The upcoming foldable iPhone is reportedly equipped with 12 GB RAM and deeply integrated Siri AI capable of combining screen, calendar, and camera inputs to understand real-world context. Apple Intelligence, announced at WWDC 2024, relies on a combination of on-device and server processing, with some features rolling out gradually through 2025.

telegram · zaihuapd · Aug 31, 10:21

**Background**: Apple Intelligence is Apple's AI framework announced at WWDC 2024, integrating AI features into iOS 18 and later versions using both on-device and cloud processing. Tim Cook has served as Apple CEO since 2011, when he succeeded Steve Jobs and oversaw the company's massive expansion into services and wearables. John Ternus previously led Apple's hardware engineering division, overseeing product development including iPhone, iPad, and Mac lineups.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Apple_Intelligence">Apple Intelligence - Wikipedia</a></li>
<li><a href="https://www.apple.com/apple-intelligence/">Apple Intelligence and Siri - Apple</a></li>
<li><a href="https://appleinsider.com/articles/26/08/28/iphone-ultra-what-to-expect-from-apples-first-foldable-iphone-and-when">iPhone Ultra rumors: design, release date, cost</a></li>

</ul>
</details>

**Tags**: `#Apple`, `#CEO-transition`, `#AI-strategy`, `#consumer-hardware`, `#industry-news`

---

<a id="item-5"></a>
## [DeepSeek Releases DeepSeek-V4-Flash-Vision-Exp Multimodal Model Weights](https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash-Vision-Exp) ⭐️ 8.0/10

DeepSeek released DeepSeek-V4-Flash-Vision-Exp, the first experimental multimodal model in the V4 series, which integrates a vision module into the V4-Flash architecture through continued training. Compared to V4-Flash-0731, multimodal agent performance improved significantly with ApexBench scores rising from 26.2 to 36.5, while text agent task performance remained roughly unchanged. This release marks DeepSeek's expansion of the V4-Flash architecture into multimodal vision capabilities, broadening the model's applicability to tasks requiring visual understanding and agent-based reasoning. The substantial ApexBench improvement demonstrates that the vision integration is effective, positioning DeepSeek more competitively in the multimodal AI agent space alongside models like Opus-4.8. The underlying V4-Flash architecture is a Mixture-of-Experts (MoE) model with 284B total parameters but only 13B active per forward pass, supporting a 1M-token context window. ApexBench is a multimodal agent evaluation benchmark reported in this release, though DeepSeek has not publicly disclosed its task count or creating institution. The model reportedly outperforms Opus-4.8 on some benchmarks including Agents' Last Exam and ZeroBench Pass@5, while trailing on ApexBench and Chartography.

telegram · zaihuapd · Aug 31, 11:41

**Background**: DeepSeek-V4-Flash is an efficiency-focused MoE model that uses a Hybrid Attention Architecture combining Compressed Sparse Attention (CSA) and Heavily Compressed Attention (HCA) to dramatically improve long-context processing efficiency. In the 1M-token context setting, the V4-Pro variant requires only 27% of single-token inference FLOPs and 10% of KV cache compared to DeepSeek-V3.2. Multimodal agents are AI systems that can plan, use tools, and act over inputs and outputs beyond plain text, such as images and visual interfaces. The experimental "Exp" designation indicates this is an early-stage release for research and testing purposes.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash">deepseek-ai/DeepSeek-V4-Flash · Hugging Face</a></li>
<li><a href="https://deepinfra.com/deepseek-ai/DeepSeek-V4-Flash">DeepSeek V4 Flash API - Demo - DeepInfra</a></li>
<li><a href="https://explainx.ai/blog/deepseek-v4-flash-vision-exp-multimodal-agent-august-2026">DeepSeek V4-Flash-Vision-Exp: Multimodal Agent Benchmarks</a></li>

</ul>
</details>

**Tags**: `#deepseek`, `#multimodal-models`, `#vision-models`, `#llm-release`, `#ai-research`

---
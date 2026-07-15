---
layout: default
title: "Horizon Summary: 2026-07-15 (EN)"
date: 2026-07-15
lang: en
---

> From 31 items, 15 important content pieces were selected

---

1. [Stripe and Advent Make Joint $53B+ Offer to Acquire PayPal](#item-1) ⭐️ 9.0/10
2. [Thinking Machines Releases Inkling, an Open-Weights Multimodal Model with Audio Support](#item-2) ⭐️ 8.0/10
3. [Researcher bypasses Claude web_fetch protections to exfiltrate private memories](#item-3) ⭐️ 8.0/10
4. [DeepSeek's Annualized Revenue Nears $500M with V4 API Gross Margins Over 50%](#item-4) ⭐️ 8.0/10
5. [DeepSeek Completes First Funding Round, Tencent Becomes Largest External Shareholder](#item-5) ⭐️ 8.0/10
6. [Musk Announces X Will Unconditionally Open-Source Entire Codebase](#item-6) ⭐️ 8.0/10
7. [Telegram Launches Serverless Platform for Bot Backends](#item-7) ⭐️ 8.0/10
8. [Running Gemma 4 26B at 5 tokens/sec on a 13-year-old Xeon with no GPU](#item-8) ⭐️ 7.0/10
9. [Sleep Regularity Predicts Mortality Better Than Sleep Duration](#item-9) ⭐️ 7.0/10
10. [Independent researcher disentangles convolutional neurons using Hadamard product in InceptionV1](#item-10) ⭐️ 7.0/10
11. [China's June Exports Hit Record $412 Billion Amid AI Boom](#item-11) ⭐️ 7.0/10
12. [Seven Smartphone On-Device LLMs Complete Regulatory Filing in China](#item-12) ⭐️ 7.0/10
13. [Google and Epic Withdraw Motion, Third-Party App Stores Coming to Play](#item-13) ⭐️ 7.0/10
14. [Developer Uses Sandbox Escape to Let Filza Read iOS 27 Notes Database](#item-14) ⭐️ 7.0/10
15. [ASML Plans Lithography Equipment Price Hikes; TSMC Resists, Some Chinese Firms Accept DUV Increase](#item-15) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Stripe and Advent Make Joint $53B+ Offer to Acquire PayPal](https://www.reuters.com/business/finance/stripe-advent-offer-buy-paypal-more-than-53-billion-sources-say-2026-07-15/) ⭐️ 9.0/10

Stripe, in partnership with private equity firm Advent International, has made a joint offer to acquire PayPal for over $53 billion at $60.50 per share. PayPal's board has not yet engaged with the offer, and the stock is trading at an 11% discount to the bid, reflecting market skepticism about the deal's completion. This acquisition would consolidate two of the world's largest digital payment platforms under one umbrella, potentially reshaping the online payments landscape and raising significant antitrust concerns. The deal's implications extend to online checkout, peer-to-peer transfers, and the emerging stablecoin ecosystem, with regulators likely to scrutinize market concentration in card-not-present transactions. Antitrust regulators may require divestitures of Braintree, Venmo, or both as a condition for approval, given the combined entity's dominant position in online card-not-present checkout. PayPal currently holds a bank charter that Stripe lacks, which could give the combined entity new capabilities in banking services and reduce reliance on partner institutions.

hackernews · rvz · Jul 15, 03:32 · [Discussion](https://news.ycombinator.com/item?id=48915953)

**Background**: Stripe is an Irish-American financial services company that provides payment processing infrastructure for businesses, while PayPal is a major digital payments platform with 439 million accounts including services like Venmo, Braintree, and Xoom. Advent International is a leading global private equity firm that has invested over $56 billion in private equity capital across more than 375 transactions in 42 countries. The online payments industry has been consolidating, and this deal would represent one of the largest fintech acquisitions in history, combining Stripe's merchant-focused payment processing with PayPal's consumer-facing payment ecosystem.

<details><summary>References</summary>
<ul>
<li><a href="https://mlq.ai/news/stripe-and-advent-international-make-53-billion-joint-bid-for-paypal-at-6050-per-share/">Stripe and Advent International Make $53 Billion Joint Bid for PayPal at $60.50 Per Share | MLQ News</a></li>
<li><a href="https://seekingalpha.com/article/4922321-paypal-the-bid-has-landed">PayPal: The Bid Has Landed (NASDAQ:PYPL) | Seeking Alpha</a></li>
<li><a href="https://www.techtimes.com/articles/320627/20260715/stripe-advent-make-53-billion-bid-paypals-439-million-accounts.htm">Stripe and Advent Make $53 Billion Bid for PayPal's 439 Million Accounts</a></li>

</ul>
</details>

**Discussion**: Community members expressed strong concerns about reduced competition and potential fee increases, particularly noting that Braintree is a legitimate competitor to Stripe and consolidation could eliminate pricing pressure. Several users highlighted risks for merchants in restricted industries (cannabis-adjacent, adult-adjacent) due to Stripe's stricter content policies, while others pointed out that the deal's antitrust challenges are significant given the combined Herfindahl-Hirschman Index for online card-not-present checkout would be "absurdly high." One commenter noted the strategic value of PayPal's bank charter, which could give Stripe new banking capabilities beyond just acquiring payment flow.

**Tags**: `#fintech`, `#payments`, `#acquisition`, `#antitrust`, `#stripe`

---

<a id="item-2"></a>
## [Thinking Machines Releases Inkling, an Open-Weights Multimodal Model with Audio Support](https://thinkingmachines.ai/news/introducing-inkling/) ⭐️ 8.0/10

Thinking Machines has introduced Inkling, an open-weights multimodal model that supports audio input alongside text and visual modalities. Rather than claiming to be the strongest overall model, Inkling is explicitly positioned as a customizable base model optimized for fine-tuning on the Tinker platform. This release is significant because it provides the largest open-weight model with native audio support, filling a gap in the open-source ecosystem where audio capabilities have lagged behind text and vision. It also validates a viable business model where enterprises can own and fine-tune their own models at potentially lower cost than relying on frontier closed models, while offering an American alternative to dominant Chinese open-weight models like DeepSeek. Inkling is described as not the strongest overall model available, but rather a combination of multimodal capabilities, efficient thinking, and availability on Tinker for fine-tuning makes it a strong open-weights base. Community members have already begun creating local deployment options, including GGUF and NVFP4 quantized versions available through Unsloth, and a llama.cpp branch with Inkling support.

hackernews · vimarsh6739 · Jul 15, 18:12 · [Discussion](https://news.ycombinator.com/item?id=48924912)

**Background**: Open-weights models provide users with access to the trained model parameters, allowing organizations to fine-tune the model for specific use cases without relying on a proprietary API. Multimodal models integrate multiple data types—such as text, images, and audio—into a single unified network, enabling tasks like audio reasoning and visual question answering. Fine-tuning a base model involves further training on domain-specific data, which can produce a model that outperforms general-purpose frontier models on specialized tasks at lower cost. The open-weights ecosystem has been largely dominated by Chinese labs such as DeepSeek, and an American lab offering a competitive open base model represents a notable shift.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ai21.com/glossary/open-weights-model/">What is an Open - Weights Model ? | AI21</a></li>
<li><a href="https://en.wikipedia.org/wiki/Fine-tuning_(deep_learning)">Fine-tuning (deep learning) - Wikipedia</a></li>
<li><a href="https://blog.unitlab.ai/top-multimodal-models/">Top 15 Multimodal Models in 2026 (Open Source & Proprietary)</a></li>

</ul>
</details>

**Discussion**: Community sentiment is broadly positive, with users praising Inkling as the largest open-weight model supporting audio and highlighting its potential for agentic applications. Several commenters emphasize the strategic importance of having an American open-weights model to compete with Chinese counterparts like DeepSeek, noting that many users currently root for Chinese models out of necessity. The business model of providing open base models for enterprise fine-tuning is viewed favorably, and community members have already begun creating local deployment options through Unsloth and llama.cpp.

**Tags**: `#open-weights`, `#multimodal-model`, `#fine-tuning`, `#thinking-machines`, `#ai`

---

<a id="item-3"></a>
## [Researcher bypasses Claude web_fetch protections to exfiltrate private memories](https://simonwillison.net/2026/Jul/15/claude-web-fetch-exfiltration/#atom-everything) ⭐️ 8.0/10

安全研究员 Ayush Paul 发现了 Claude web_fetch 工具中的一个漏洞，攻击者可以通过一个包含嵌套生成链接的蜜罐网站窃取用户的私密记忆数据。该攻击诱骗 Claude 逐字母地在攻击者控制的页面中导航，成功提取了用户的姓名、所在城市和雇主名称。 This vulnerability demonstrates that even carefully designed deterministic security mitigations from major AI vendors like Anthropic can be circumvented, exposing users' most sensitive conversational data to attackers. It highlights the ongoing challenge of securing LLM agents against prompt injection attacks that combine untrusted web content with access to private information. The attack exploited web_fetch's ability to follow URLs embedded in previously fetched pages, creating a chain of nested links that bypassed Anthropic's rule restricting fetches to user-entered or web_search-returned URLs. The honeypot site only served malicious content to clients with Claude-User in their user-agent to avoid detection, and Anthropic has since closed the hole by removing the ability for web_fetch to navigate to links found within fetched content.

rss · Simon Willison · Jul 15, 14:21

**Background**: The "lethal trifecta" for AI agents, coined by Simon Willison, describes a dangerous combination where an LLM has access to private data, processes untrusted content, and can communicate externally — enabling prompt injection attacks that exfiltrate sensitive information. Anthropic's web_fetch tool was specifically designed to prevent this by only allowing navigation to exact URLs that users entered themselves or that were returned from the companion web_search tool. However, the allowance for web_fetch to follow links embedded in fetched pages created an unintended attack surface that broke this deterministic protection.

<details><summary>References</summary>
<ul>
<li><a href="https://simonwillison.net/2025/Jun/16/the-lethal-trifecta/">The lethal trifecta for AI agents: private data, untrusted content, and external communication</a></li>
<li><a href="https://docs.claude.com/en/docs/agents-and-tools/tool-use/web-fetch-tool">Web fetch tool - Claude Docs</a></li>
<li><a href="https://www.osohq.com/learn/lethal-trifecta-ai-agent-security">Understanding the Lethal Trifecta of AI Agents</a></li>

</ul>
</details>

**Tags**: `#AI Security`, `#Prompt Injection`, `#Data Exfiltration`, `#Claude`, `#LLM Vulnerabilities`

---

<a id="item-4"></a>
## [DeepSeek's Annualized Revenue Nears $500M with V4 API Gross Margins Over 50%](https://www.theinformation.com/articles/deepseeks-annualized-revenue-nears-500-million-boosting-fundraise-ipo-plans) ⭐️ 8.0/10

DeepSeek's annualized revenue has reached $400–500 million, primarily driven by enterprise and developer API calls, with its V4 API achieving over 50% gross margins despite pricing well below OpenAI and Anthropic. The company is planning to raise 50 billion RMB at a valuation of approximately 500 billion RMB (~$74 billion), courting overseas investors from the Middle East and allowing USD-denominated investments. DeepSeek's ability to achieve high profitability at low price points demonstrates that infrastructure optimization can fundamentally alter the economics of large language model deployment. The planned fundraising at a ~148x revenue multiple signals massive investor confidence and could reshape the competitive landscape among top AI labs. DeepSeek's V4 model family includes V4-Flash (284B total / 13B active parameters) and V4-Pro variants, supporting multiple reasoning modes including non-think, think-high, and think-max with context windows up to 384K tokens. The over 50% gross margin is attributed to infrastructure optimizations that reduce the number of chips needed to run the models, though all figures come from unnamed sources and DeepSeek has not officially responded.

telegram · zaihuapd · Jul 15, 07:04

**Background**: Annualized revenue run rate projects a recent period's revenue forward across a full year, capturing momentum but not representing audited annual revenue. DeepSeek's V4 API offers models at significantly lower prices than competitors like OpenAI and Anthropic, making its high gross margins particularly notable. The company has reportedly optimized its infrastructure to reduce the number of chips required for inference, which is a key factor in achieving profitability at lower price points.

<details><summary>References</summary>
<ul>
<li><a href="https://api-docs.deepseek.com/news/news260424/">DeepSeek V4 Preview Release | DeepSeek API Docs</a></li>
<li><a href="https://www.investopedia.com/terms/r/runrate.asp">investopedia.com/terms/r/runrate.asp</a></li>
<li><a href="https://www.together.ai/models/deepseek-v4-pro">DeepSeek V4 Pro API | Together AI</a></li>

</ul>
</details>

**Tags**: `#DeepSeek`, `#AI Economics`, `#API`, `#Funding`, `#LLM`

---

<a id="item-5"></a>
## [DeepSeek Completes First Funding Round, Tencent Becomes Largest External Shareholder](https://www.cls.cn/detail/2427193) ⭐️ 8.0/10

DeepSeek has completed its first-ever external funding round, raising approximately $7 billion at a valuation exceeding $50 billion, with Tencent emerging as the largest external shareholder through its stake in the investment platform Hangzhou Chengli. The round also includes participation from CATL, NetEase, JD.com, IDG, Monolith, and a national AI industry investment fund, while DeepSeek simultaneously announced plans to release DeepSeek-V4 mid-month and launched a massive hiring campaign covering Agent, code intelligence, and foundational compute framework roles. This funding round marks a fundamental shift for DeepSeek from a purely self-funded entity backed by hedge fund High-Flyer to a company with broad industry backing from China's tech giants, signaling strong confidence in its position within the competitive LLM landscape. The participation of Tencent, CATL, NetEase, and JD.com alongside a national AI fund reflects deep ecosystem-level support that could accelerate DeepSeek's scaling and model development at a critical moment in the global AI race. Tencent holds over 33% of Hangzhou Chengli, which itself owns approximately 8.52% of DeepSeek's parent entity, making Tencent the largest external shareholder; CATL holds about 11.7% via Wenting Investment, with its affiliated Puquan Capital holding about 5%; NetEase and JD.com each hold approximately 10%, IDG holds about 10%, Monolith holds 9.7%, and the national AI industry fund directly holds about 0.28%. The registered capital of DeepSeek's parent company increased to 16.4475 million yuan following the changes.

telegram · zaihuapd · Jul 15, 12:56

**Background**: DeepSeek is a Hangzhou-based AI company that develops large language models and was previously owned and funded entirely by High-Flyer, a Chinese quantitative hedge fund. The company has gained significant attention in the AI community for its open-weight model releases, including the DeepSeek-R1 reasoning model and the DeepSeek-V3 series, which have been competitive with offerings from larger labs. The upcoming DeepSeek-V4 is expected to be a Mixture-of-Experts model, continuing the company's approach of combining strong performance with cost-efficient inference. This first external funding round represents a notable departure from DeepSeek's previous self-funded model and aligns with a broader trend of major Chinese AI companies securing large capital injections to compete in the global LLM race.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek">DeepSeek - Wikipedia</a></li>
<li><a href="https://beststartup.asia/deepseek-funding-2026/">DeepSeek Funding 2026: New $7.4 Billion Shakes Global AI</a></li>
<li><a href="https://www.pymnts.com/news/artificial-intelligence/2026/deepseek-considers-new-funding-round-after-raising-7-billion/">DeepSeek Considers New Funding Round After Raising $7 billion | PYMNTS.com</a></li>

</ul>
</details>

**Tags**: `#DeepSeek`, `#AI Funding`, `#Tencent`, `#LLM`, `#DeepSeek-V4`

---

<a id="item-6"></a>
## [Musk Announces X Will Unconditionally Open-Source Entire Codebase](https://x.com/elonmusk/status/2077361679034118271) ⭐️ 8.0/10

Elon Musk announced that X will unconditionally open-source its entire codebase after completing a security vulnerability review. Additionally, X will invite third-party reviewers to verify that the open-source code matches the code actually running on its production systems. This announcement represents an unprecedented move for a major social media platform, potentially transforming industry standards around algorithmic transparency and user trust. If implemented as described, it could pressure competitors to follow suit and fundamentally change how social platforms are audited and held accountable. The open-sourcing is contingent on first completing a security vulnerability review, meaning the timeline and scope remain unspecified. A critical challenge will be ensuring that third-party reviewers can reliably verify code-to-production consistency, which requires ongoing access and auditing mechanisms that have not yet been detailed.

telegram · zaihuapd · Jul 15, 13:32

**Background**: X (formerly Twitter) has faced scrutiny over content moderation, algorithmic transparency, and data privacy practices, particularly after Elon Musk's acquisition of the platform in 2022. Open-sourcing a social media platform's entire codebase is virtually unheard of in the industry, as platforms typically treat their recommendation algorithms and infrastructure as proprietary competitive advantages. The concept of third-party verification of running systems draws from established practices in security auditing, where independent auditors compare deployed code against published source to detect discrepancies or hidden modifications.

<details><summary>References</summary>
<ul>
<li><a href="https://developer.salesforce.com/docs/atlas.en-us.industries_reference.meta/process_compliance_navigator/connect_requests_party_identity_verification_input.htm">Party Identity Verification Input | Industries Common Resources...</a></li>
<li><a href="https://www.ceisystems.com/2025/02/08/telegram-launches-third-party-verification-for-accounts/">Telegram Launches Third - Party ... | CEI Systems & Technologies</a></li>

</ul>
</details>

**Tags**: `#open-source`, `#X`, `#Elon Musk`, `#transparency`, `#social media`

---

<a id="item-7"></a>
## [Telegram Launches Serverless Platform for Bot Backends](https://core.telegram.org/bots/serverless) ⭐️ 8.0/10

Telegram officially launched a Serverless platform that allows developers to run bot and Mini App backend code directly on Telegram's infrastructure. Developers can deploy code by simply writing JavaScript modules and running the `npx tgcloud push` command, eliminating the need to provision their own servers or manage containers. This significantly reduces infrastructure overhead for bot developers and streamlines the deployment process, representing a major expansion of Telegram's platform capabilities. It positions Telegram as a more complete ecosystem for bot and Mini App development, lowering the barrier to entry for creators. The deployed code runs in an isolated V8 sandbox situated close to the Bot API, and includes a built-in database based on SQLite. This architecture ensures low-latency communication with Telegram's core services while providing developers with essential data storage out of the box.

telegram · zaihuapd · Jul 15, 16:00

**Background**: Telegram Bots are third-party applications that run inside Telegram, using the Bot API to process messages and commands from users. Mini Apps are full-fledged web applications that run within the Telegram client interface. Previously, developers had to host their backend logic on external cloud providers or their own servers, using webhooks to receive updates from Telegram.

<details><summary>References</summary>
<ul>
<li><a href="https://core.telegram.org/bots/serverless">Telegram Serverless</a></li>
<li><a href="https://core.telegram.org/bots/webapps">Telegram Mini Apps</a></li>

</ul>
</details>

**Tags**: `#telegram`, `#serverless`, `#bots`, `#javascript`, `#platform`

---

<a id="item-8"></a>
## [Running Gemma 4 26B at 5 tokens/sec on a 13-year-old Xeon with no GPU](https://www.neomindlabs.com/2026/06/08/running-gemma-4-26b-at-5-tokens-sec-on-a-13-year-old-xeon-with-no-gpu/) ⭐️ 7.0/10

An article demonstrates running Google's Gemma 4 26B model at 5 tokens per second on a 13-year-old Intel Xeon server CPU without any GPU acceleration. This showcases significant advancements in CPU-based LLM inference, making large models accessible on legacy hardware. This demonstration challenges the assumption that modern LLMs require expensive GPU hardware, highlighting the potential for democratizing AI access through optimized CPU inference. It sparks important discussions about the economics of local versus cloud inference, especially as MoE architectures become more efficient. Gemma 4 26B is a Mixture-of-Experts (MoE) model with 26B total parameters and 4B active parameters, designed for high-throughput reasoning. The demonstration achieved 5 tokens/sec on legacy Xeon hardware, though community members noted that power consumption (estimated 300-500W) makes local inference potentially more expensive than cloud alternatives at current electricity prices.

hackernews · neomindryan · Jul 15, 15:34 · [Discussion](https://news.ycombinator.com/item?id=48922434)

**Background**: Gemma 4 is Google's latest open-weights model family, featuring both dense and Mixture-of-Experts (MoE) architectures across four sizes. The 26B A4B variant uses MoE, meaning only 4 billion parameters are active during inference despite the model having 26 billion total, making it more efficient to run than a similarly-sized dense model. CPU-based LLM inference has traditionally been much slower than GPU-based methods, but recent research has shown that under certain conditions, CPUs can be competitive, especially for budget-conscious or on-device scenarios where GPU availability is limited.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/google/gemma-4-26B-A4B">google/gemma-4-26B-A4B · Hugging Face</a></li>
<li><a href="https://ai.google.dev/gemma/docs/core">Gemma 4 model overview | Google AI for Developers</a></li>
<li><a href="https://arxiv.org/html/2505.06461v1">Challenging GPU Dominance: When CPUs Outperform for On-Device LLM Inference</a></li>

</ul>
</details>

**Discussion**: The community discussion centered on the economics of local versus cloud inference, with user hagen8 calculating that generating 18,000 tokens locally at 5 tps would cost approximately $0.15 in electricity versus only $0.005 from a cloud provider. User Aurornis noted that the Xeon server likely draws 300W+ and that cloud inference through OpenRouter costs roughly the same per million tokens but runs 8x faster. Others shared their own experiences, with dwa3592 predicting that 200B+ MoE models will run on basic consumer hardware by mid-2027, and hparadiz sharing benchmarks from a dual Xeon with 256GB DDR4.

**Tags**: `#LLM`, `#CPU Inference`, `#Local AI`, `#Hardware`, `#Gemma`

---

<a id="item-9"></a>
## [Sleep Regularity Predicts Mortality Better Than Sleep Duration](https://academic.oup.com/sleep/article/47/1/zsad253/7280269) ⭐️ 7.0/10

A 2023 study published in the journal SLEEP found that sleep regularity—how consistently you sleep and wake at the same times—is a stronger predictor of mortality risk than sleep duration. The findings were based on analysis of a large participant cohort, challenging the conventional focus on getting enough hours of sleep. This finding shifts public health messaging from merely getting enough sleep to maintaining a consistent sleep schedule, which could be more actionable for many people. It affects anyone interested in longevity and lifestyle optimization, as well as clinicians advising patients on sleep hygiene. The study used a large cohort and statistically controlled for variables like shift work and employment status, though commenters noted potential residual confounding from occupation type and other unmeasured factors. Sleep regularity was assessed using accelerometer-derived data rather than self-report, strengthening the measurement's reliability.

hackernews · bilsbie · Jul 15, 11:46 · [Discussion](https://news.ycombinator.com/item?id=48919363)

**Background**: Sleep duration has long been the primary metric in sleep health research, with guidelines recommending 7-9 hours for adults. Sleep regularity, by contrast, refers to the day-to-day consistency of sleep-wake timing and has received less attention until recently. Accelerometry-based sleep assessment allows researchers to objectively measure sleep-wake patterns over multiple days, enabling more nuanced analysis of how sleep timing—not just length—affects health outcomes.

**Discussion**: Community members shared personal anecdotes, such as using magnesium supplementation to address insomnia root causes rather than relying on prescription sleeping pills. Others discussed biological mechanisms—consistent sleep schedules let the brain reliably regulate cortisol and body temperature. Several commenters raised methodological concerns about uncontrolled confounding variables, particularly occupation-related factors like cosmic radiation exposure for frequent flyers, suggesting the findings are useful for hypothesis generation but not yet actionable for individual decisions.

**Tags**: `#sleep`, `#health`, `#mortality`, `#research`, `#lifestyle`

---

<a id="item-10"></a>
## [Independent researcher disentangles convolutional neurons using Hadamard product in InceptionV1](https://www.reddit.com/r/MachineLearning/comments/1uwya70/mechanistic_interpretability_a_first_paper_on/) ⭐️ 7.0/10

An independent researcher introduced a new mechanistic interpretability technique that uses the Hadamard product of a neuron's receptive field and its weights to disentangle and analyze individual 1x1 convolutional neurons in the InceptionV1 model. The method produces clean monosemantic clusters of concepts (e.g., cars, cats, dogs, letters, faces) and reveals that low-valued activation clusters have dependent neurons firing on the same concept with evenly distributed positive and negative weights. This work contributes a novel analytical method to mechanistic interpretability, an important subfield of AI safety and explainability research that seeks to reverse-engineer neural networks to understand their internal algorithms. The finding that gradient descent deliberately places patterns in noisy ranges with balanced positive and negative weights suggests a deeper structural principle in how networks encode concepts, which could influence future interpretability research. The technique was applied to neuron mixed4e-55 in InceptionV1's convolutional layers, clustering the Hadamard product to identify all patterns a neuron detects. The author notes that low-valued clusters (like letters) had all dependent neurons firing on the same concept, with positive and negative weights evenly distributed to bring down the sum, which they interpret as evidence of gradient descent deliberately placing patterns in a noisy range.

reddit · r/MachineLearning · /u/narang_27 · Jul 15, 06:59

**Background**: Mechanistic interpretability is a subfield of AI research that seeks to reverse-engineer neural networks by identifying circuits, features, and algorithms learned by the model, treating the network as a compiled program that can be understood. The Distill Circuits Thread, which this work builds upon, is a well-known series of publications that pioneered the analysis of individual neurons and circuits in vision models like InceptionV1. The Hadamard product is an element-wise multiplication of two identically-shaped matrices, producing a third matrix of the same dimensions. InceptionV1 (GoogLeNet) is a landmark convolutional neural network architecture known for its inception modules, and its neurons have been extensively studied in interpretability research.

<details><summary>References</summary>
<ul>
<li><a href="https://www.linkedin.com/pulse/mechanistic-interpretability-neuroscience-neural-networks-taras-s17gf">Mechanistic Interpretability - The Neuroscience of Neural Networks</a></li>
<li><a href="https://en.wikipedia.org/wiki/Hadamard_product_(matrices)">Hadamard product (matrices) - Wikipedia</a></li>
<li><a href="https://gghantiwala.medium.com/understanding-the-architecture-of-the-inception-network-and-applying-it-to-a-real-world-dataset-169874795540">Understanding Architecture Of Inception Network & Applying... | Medium</a></li>

</ul>
</details>

**Tags**: `#mechanistic interpretability`, `#explainable AI`, `#computer vision`, `#neural networks`, `#deep learning`

---

<a id="item-11"></a>
## [China's June Exports Hit Record $412 Billion Amid AI Boom](https://www.bloomberg.com/news/articles/2026-07-14/china-s-exports-imports-soar-faster-than-forecast-amid-ai-rush) ⭐️ 7.0/10

China's exports in June surged to a record $412 billion, up 27% year-on-year, while imports jumped 36%, the fastest pace in five years. Semiconductor exports soared 122% by value, automobile exports exceeded 1 million units for the first time, and the trade surplus reached $125.6 billion, the second-highest on record. The data reveals that a global AI investment supercycle is reshaping trade flows, with chips and computers contributing about one-third of export growth. The broadening of growth beyond semiconductors into autos, ships, and appliances signals that China's export momentum is becoming more diversified and resilient. Semiconductor exports surged 122% by dollar value but actually declined 0.4% by volume, reflecting skyrocketing chip prices—DDR5 16Gb memory chip prices rose 682% year-on-year, and NAND flash prices rose 807%. Crude oil imports plunged 41% to 29 million tons, the lowest in nearly a decade, due to Middle East tensions. The trade surplus with the EU expanded to a record $32.9 billion.

telegram · zaihuapd · Jul 15, 06:19

**Background**: The global AI investment supercycle is driven by massive capital expenditure on compute infrastructure, including GPUs, data centers, and semiconductors, with companies like Nvidia at the center of the buildout. China's semiconductor exports have been surging in dollar terms throughout 2026, with integrated circuits becoming the largest export category by both value and volume in May. However, the dramatic divergence between export value and volume reflects how chip price inflation—particularly in memory chips like DDR5 and NAND—has amplified the dollar figures even as physical shipment quantities stagnate or decline.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bbc.com/zhongwen/articles/cg4w2n5ql32o/simp">中国芯片 出 口 额暴增110%，是否意味西方“封锁失败”？ - BBC News 中文</a></li>
<li><a href="https://www.ajudaily.com/view/20260604065248331">半 导 体 景气回升带动 出 口 增长 韩国对华贸易收支有望扭亏为盈 | 亚洲日报</a></li>
<li><a href="https://www.techflowpost.com/article/31833">拆解英伟达早 期 投 资 人 Gavin Baker 的 投 资 哲学：做多 AI ...</a></li>

</ul>
</details>

**Tags**: `#AI投资`, `#半导体出口`, `#宏观经济`, `#贸易数据`, `#中国出口`

---

<a id="item-12"></a>
## [Seven Smartphone On-Device LLMs Complete Regulatory Filing in China](https://mp.weixin.qq.com/s/5MTWh4pWVAlL71RQbU-Udg) ⭐️ 7.0/10

On July 8, seven major smartphone manufacturers — Apple, Huawei, OPPO, vivo, Xiaomi, Samsung, and ZTE — completed regulatory filings with the Cyberspace Administration of China (CAC) for their on-device language models. The filed models include Apple Intelligence, Huawei Xiaoyi AI, OPPO AndesGPT, vivo BlueLM, Xiaomi Pengpai AI, and Samsung Galaxy AI, all designated for smartphone-side application scenarios. This regulatory milestone signals that on-device AI has reached a level of maturity and official acceptance in one of the world's largest smartphone markets. It paves the way for these manufacturers to legally deploy AI-powered features at scale, accelerating the integration of LLMs into everyday consumer devices and intensifying competition in AI-driven smartphone experiences. All seven filings specify "mobile phone terminal" as the application scenario, indicating these models are optimized for on-device inference rather than cloud-based processing. On-device models typically feature smaller parameter sizes (e.g., 1.5B to 7B) to balance performance with the computational and memory constraints of smartphones.

telegram · zaihuapd · Jul 15, 08:06

**Background**: China's Cyberspace Administration (CAC) requires generative AI models to undergo a filing and registration process before being offered to the public, as mandated by regulations on generative AI services. This "large model filing" (大模型备案) involves submitting the model for review of its safety, security, and compliance with content guidelines. On-device language models run directly on the smartphone's hardware, enabling AI features like voice assistants and text generation without sending data to cloud servers, which enhances privacy and reduces latency.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cnblogs.com/senlin202511/p/18704295">一文搞懂 大 模 型 备 案 全部内容 - 悲伤的森林 - 博客园</a></li>
<li><a href="https://juejin.cn/post/7646622735791030282">一文读懂生成式 AI...</a></li>
<li><a href="https://www.53ai.com/news/zhinengyingjian/2024070758924.html">【不看后悔】一文梳理 端 侧 模 型 和小 模 型 - 53AI-AI...</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Smartphones`, `#On-Device AI`, `#Regulation`, `#LLM`

---

<a id="item-13"></a>
## [Google and Epic Withdraw Motion, Third-Party App Stores Coming to Play](https://www.theverge.com/policy/965792/google-epic-withdraw-injunction-third-party-app-stores-coming-google-play) ⭐️ 7.0/10

Google and Epic Games have jointly withdrawn a motion to modify a federal court's permanent injunction, clearing the way for Google Play to begin hosting rival third-party app stores starting July 22. Google has notified US developers that their app listings will automatically be made available to these third-party stores unless they explicitly opt out. This marks a fundamental shift in the Android app distribution ecosystem, as Google's own store will now be forced to host and promote direct competitors. It could reshape app discovery and distribution on Android, giving consumers more choices and giving rival app stores unprecedented access to mainstream users. Third-party stores must pay an annual $5,000 security and policy review fee and meet requirements including US-only distribution, openness to all developers, and clear trust and safety policies. Outside the US, Google will still use its planned "Registered App Store" sideloading scheme slated for later this year, which requires developer registration and government ID.

telegram · zaihuapd · Jul 15, 11:15

**Background**: In October 2024, US District Judge James Donato issued a permanent injunction forcing Google to open Play to third-party app stores after Epic Games won its antitrust case. Google had previously argued that Epic's demands were too costly and had sought to modify the injunction. Android technically always allowed sideloading, but Google's security warnings and distribution rules made it difficult for rival stores to reach mainstream users.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theguardian.com/technology/2024/oct/07/google-play-store-epic-games-antitrust-lawsuit">Google ordered to open Play store to rivals after antitrust loss to Epic ...</a></li>
<li><a href="https://www.theregister.com/software/2024/06/26/google-tells-court-epic-games-injunction-demands-too-costly/854617">Google tells court Epic Games ' injunction demands too costly</a></li>

</ul>
</details>

**Tags**: `#Google Play`, `#Epic Games`, `#app stores`, `#antitrust`, `#Android`

---

<a id="item-14"></a>
## [Developer Uses Sandbox Escape to Let Filza Read iOS 27 Notes Database](https://x.com/0xjohnny/status/2077216973256274272) ⭐️ 7.0/10

Developer Johnny modified the iOS file management tool Filza to exploit a sandbox escape vulnerability, enabling it to read the Notes database on an iPhone 17 Pro Max running iOS 27 beta 3. The modified tool can browse data outside its own app container, including access to the sensitive Notes database. A working sandbox escape on the latest iOS 27 beta 3 is a significant security development, as it demonstrates that Apple's app isolation mechanisms can still be bypassed on the newest hardware. This is highly relevant to security researchers, jailbreak developers, and anyone interested in iOS security architecture. The exploit was demonstrated on an iPhone 17 Pro Max running iOS 27 beta 3, and it involves modifying Filza to break out of its app sandbox container rather than developing a completely new exploit from scratch. The specific technical details of the sandbox escape method have not been publicly disclosed.

telegram · zaihuapd · Jul 15, 14:35

**Background**: iOS uses a sandboxing mechanism that confines each app to its own container, preventing it from accessing other apps' data or system files without explicit permission. A sandbox escape occurs when an app successfully performs actions outside its sandbox, typically due to a flaw in iOS or a misconfigured entitlement. Filza is a popular iOS file manager that allows users to browse and edit files on their iPhone or iPad, and it has historically been used in jailbreak contexts to access the full filesystem.

<details><summary>References</summary>
<ul>
<li><a href="https://redfoxsecurity.medium.com/locked-in-a-box-how-ios-sandboxing-challenges-pentesters-8207476da296">Locked in a Box : How iOS Sandboxing Challenges Pentesters | Medium</a></li>
<li><a href="https://www.tigisoftware.com/default/?page_id=78">Filza – TIGI Software</a></li>

</ul>
</details>

**Tags**: `#iOS`, `#Security`, `#Sandbox Escape`, `#Jailbreak`, `#Exploit`

---

<a id="item-15"></a>
## [ASML Plans Lithography Equipment Price Hikes; TSMC Resists, Some Chinese Firms Accept DUV Increase](https://news.bloomberglaw.com/artificial-intelligence/asml-plans-price-increases-on-chipmaking-equipment-information) ⭐️ 7.0/10

ASML plans to raise prices for its chipmaking equipment, with CFO Roger Dassen citing improved pricing power and noting that advanced EUV lithography capacity is nearly fully booked through the end of 2027. While TSMC is resisting proposed EUV price increases, some Chinese chipmakers have already accepted a 10% price hike on DUV equipment. ASML's ability to raise prices reflects its absolute monopoly in EUV lithography and dominant position in DUV, underscoring severe supply chain constraints in the semiconductor industry. The divergent responses from TSMC and Chinese foundries highlight how geopolitical dynamics and equipment scarcity are reshaping bargaining power across the global chip manufacturing ecosystem. ASML's EUV lithography capacity is booked through late 2027, giving the company significant leverage in price negotiations with major customers like TSMC. In the DUV segment, where ASML holds over 85% market share, the proposed 10% price increase has been accepted by some Chinese manufacturers despite resistance from other customers.

telegram · zaihuapd · Jul 15, 16:49

**Background**: ASML is a Dutch multinational corporation that holds an absolute monopoly in EUV (extreme ultraviolet) lithography equipment, which uses 13.5 nm wavelength light to create intricate patterns on semiconductor substrates for advanced chip manufacturing. In the DUV (deep ultraviolet) lithography segment, ASML also holds a dominant position with over 85% market share, while competitors like Nikon and Canon each hold less than 10%. EUV equipment is essential for producing the most advanced process nodes used by leading-edge foundries such as TSMC, while DUV equipment remains critical for mature process nodes and is especially important for Chinese chipmakers facing export restrictions on EUV technology.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Extreme_ultraviolet_lithography">EUV lithography - Wikipedia</a></li>
<li><a href="https://www.100baggers.club/en/reports/asml">ASML ( ASML ) Deep Research — Three Paradoxes of the Lithography ...</a></li>
<li><a href="https://www.asml.com/en/products/duv-lithography-systems">DUV lithography systems | Products</a></li>

</ul>
</details>

**Tags**: `#semiconductors`, `#ASML`, `#lithography`, `#supply-chain`, `#pricing`

---
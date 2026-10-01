---
layout: default
title: "Horizon Summary: 2026-10-01 (ZH)"
date: 2026-10-01
lang: zh
---

> 从 34 条内容中筛选出 5 条重要资讯。

---

1. [Google 发布 Gemini 4 Argon，全新前沿 AI 模型](#item-1) ⭐️ 9.0/10
2. [32 位研究者联合发布现代 NLP 分词技术综合综述](#item-2) ⭐️ 8.0/10
3. [DeepSeek 开源华为昇腾平台基础 AI 组件](#item-3) ⭐️ 8.0/10
4. [Cloudflare 宣布进军公共证书颁发机构](#item-4) ⭐️ 8.0/10
5. [Reddit 因 AI 爬虫问题将停用 RSS 订阅与公开 API](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Google 发布 Gemini 4 Argon，全新前沿 AI 模型](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-4-argon/) ⭐️ 9.0/10

Google 宣布了其迄今最先进的前沿 AI 模型 Gemini 4 Argon，具备 100 万 token 的上下文窗口，在 Artificial Analysis 智能指数中得分 53，远高于同类模型 26 的中位数。该模型目前正向部分早期测试者和网络安全合作伙伴推出，在编码、网络安全和复杂长期专业任务方面有显著提升。 Gemini 4 Argon 代表了前沿 AI 实验室之间持续交替领先竞争中的又一次重大飞跃，早期测试者报告了令人震惊的能力，例如自主逆向工程 GPU 驱动接口并编写底层 C shim。此次发布也挑战了 AI 是赢家通吃市场的理论，因为 Google、OpenAI、Anthropic 等公司持续交替领先，进一步凸显了供应商无关的 AI 工作流的重要性。 该模型支持文本和图像输入模态，其推理变体在 Artificial Analysis 智能指数中得分 53，据报道 Argon 代理已在 Google 内部用于将 C/C++ 代码库迁移至 Rust。Google 表示仍在迭代安全护栏，之后才会向开发者、企业和消费者广泛提供 Argon，这引发了关于 Google 倾向于发布模型但不立即公开的批评。

hackernews · bradleyg223 · 9月30日 20:04 · [社区讨论](https://news.ycombinator.com/item?id=49913571)

**背景**: 前沿 AI 模型是指处于通用 AI 能力最前沿的系统，通常是主要实验室的最新旗舰发布版本，其能力可能带来需要额外审查的新风险。2025-2026 年间，AI 行业的特点是快速交替领先，Google、OpenAI、Anthropic 等公司反复在基准测试中交换领先位置。Anthropic 首席执行官 Dario Amodei 此前曾提出 AI 发展是赢家通吃的理论，认为早期领先者会集中优势且永不让步，但持续的竞争态势已使这一预测受到质疑。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-4-argon/">Introducing Gemini 4 Argon</a></li>
<li><a href="https://artificialanalysis.ai/models/gemini-4-argon">Gemini 4 Argon (high) - Intelligence, Performance... | Artificial Analysis</a></li>
<li><a href="https://www.cnbc.com/2026/09/30/google-gemini-4-argon-ai.html">Google rolls out Gemini 4 Argon , its most advanced model</a></li>

</ul>
</details>

**社区讨论**: 社区情绪兼具惊叹与务实：一位测试者讲述了模型自主将 GDB 附加到 GPU 驱动上、逆向工程内核队列 ioctl 接口并编写 LD_PRELOAD C shim 使 ROCm 正常工作的经历，令其目瞪口呆。多位评论者就 AI 竞争是否真如 Dario Amodei 所说是赢家通吃展开辩论，共识倾向于持续交替领先而非集中垄断。社区还提出了保持模型和供应商可替换的实用建议，同时有人批评 Google 在模型公开可用之前就宣布发布的惯常做法。

**标签**: `#AI/ML`, `#LLM`, `#Google`, `#Gemini`, `#frontier-models`

---

<a id="item-2"></a>
## [32 位研究者联合发布现代 NLP 分词技术综合综述](https://www.reddit.com/r/MachineLearning/comments/1wuccjf/tokenization_a_survey_for_modern_nlp_r/) ⭐️ 8.0/10

由 32 位分词研究者组成的团队历时约 8 个月，撰写了迄今为止最全面的现代 NLP 分词技术综述。该综述涵盖了算法、评估方法、多语言性、编码方式、理论、安全问题，以及潜在分词和视觉分词等新兴替代方案。 分词是语言建模的基础组件，却严重缺乏研究关注，而它几乎影响 NLP 的方方面面，从模型性能到多语言公平性。拥有一份覆盖从传统算法到潜在替代方案的全面深度参考，为社区提供了这一关键但常被忽视领域的急需指南。 该综述还涵盖了与分词密切相关的主题，包括约束生成、token 修复（token healing）以及分词器安全漏洞。它探讨了下一代替代方案，如潜在分词（绕过离散文本分割）和视觉分词（将输入转换为空间定位的 token 序列），这些方案可能从根本上改变模型处理语言的方式。

reddit · r/MachineLearning · /u/mcmcmcmcmcmcmcmcmc_ · 9月30日 18:13

**背景**: NLP 中的分词是指将文本序列转换为更小单元（即 token）的过程，这些 token 是语言模型的基本输入单元。尽管分词是直接影响模型词表、效率和多语言能力的关键预处理步骤，但与模型架构或训练方法相比，它受到的研究关注要少得多。新兴方法如视觉分词旨在将数据转换为离散的、空间定位的 token 序列，而潜在分词则试图完全超越显式文本分割。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.datacamp.com/blog/what-is-tokenization">Tokenization in NLP : How It Works, Challenges, and Use... | DataCamp</a></li>
<li><a href="https://groma-mllm.github.io/">Groma: Localized Visual Tokenization for Grounding Multimodal...</a></li>

</ul>
</details>

**标签**: `#NLP`, `#tokenization`, `#language-modeling`, `#survey`, `#multilinguality`

---

<a id="item-3"></a>
## [DeepSeek 开源华为昇腾平台基础 AI 组件](https://mp.weixin.qq.com/s/X41mKH4Ds-VXUAnK6M8Eww) ⭐️ 8.0/10

2026 年 9 月 30 日，DeepSeek 开源了面向华为昇腾平台的一整套基础 AI 组件，包括 TileLang 编译器、计算库（DeepGEMM Ascend、DeepEP Ascend）、分布式通信库、TileKernels、FlashMLA 和 DeepSelect。DeepSeek 称相关组件在多项测试中性能接近硬件上限，并与华为合作推进昇腾 950 的 128 卡超节点方案。 此次开源标志着构建非英伟达 AI 硬件生态的重要一步，为开发者提供了在华为昇腾架构上构建和优化 AI 工作负载的开源工具。双方在 128 卡昇腾 950 超节点上的合作，显示出打造大规模训练和推理集群以替代英伟达方案的严肃努力。 开源组件与 DeepSeek 现有的英伟达平台工具一一对应，覆盖从编译（TileLang）到计算算子（DeepGEMM、DeepEP、FlashMLA）和分布式通信的完整技术栈。昇腾 950 的 128 卡超节点相比华为此前发布的 4096 芯片 Atlas 960E 超级集群规模更小，但专门针对 DeepSeek 软件栈进行了计算与通信的联合优化。

telegram · zaihuapd · 9月30日 03:09

**背景**: TileLang 是一种领域特定语言和编译器框架，旨在为 AI 工作负载生成高度优化的分块张量算子，采用可组合编程模型将数据流定义与调度优化解耦。FlashMLA 是 DeepSeek 的优化多头潜在注意力算子库，为 DeepSeek-V3 和 DeepSeek-V3.2-Exp 模型提供支持，最初面向英伟达 Hopper GPU 发布。华为昇腾平台是该公司自研的 AI 加速器架构，昇腾 950 是面向大规模 AI 训练和推理工作负载的新一代芯片。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/tile-ai/tilelang">GitHub - tile - ai / tilelang : Domain-specific language designed to...</a></li>
<li><a href="https://github.com/deepseek-ai/FlashMLA">GitHub - deepseek -ai/ FlashMLA : FlashMLA : Efficient Multi-head...</a></li>
<li><a href="https://pasqualepillitteri.it/en/news/19580/tilelang-deepseek-huawei-ascend-cuda">DeepSeek and Huawei release TileLang for Ascend chips, taking aim...</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#Huawei Ascend`, `#AI Infrastructure`, `#Open Source`, `#Hardware Acceleration`

---

<a id="item-4"></a>
## [Cloudflare 宣布进军公共证书颁发机构](https://blog.cloudflare.com/cloudflare-certificate-authority/) ⭐️ 8.0/10

Cloudflare 正式宣布计划成为公共证书颁发机构，已申请加入 Chrome、Apple、Microsoft 和 Mozilla 的根证书计划，并与 GlobalSign 签署协议收购一个受广泛信任的根证书。目前尚未开始签发证书，但新 CA 将优先支持基于 ACME 的自动签发和续期，并计划在 2027 年第一季度签发生产级默克尔树证书（MTC），以服务后量子互联网。 Cloudflare 进入公共 CA 市场可能显著重塑 Web PKI 格局，引入一个具备规模和技术能力的大型基础设施厂商，与 Let's Encrypt、DigiCert、GlobalSign 等老牌机构竞争。计划在 2027 年部署默克尔树证书尤其具有前瞻性，因为它通过基于哈希的方法应对量子计算机破解当前公钥密码体系的威胁，该方法被认为具有抗量子特性。 Cloudflare 从 GlobalSign 收购现有根证书而非从零建立信任，这大幅缩短了投入运营的时间线，因为根证书被纳入浏览器信任存储通常需要数年时间。ACME 协议支持意味着新 CA 将兼容 certbot 等现有自动化工具，而默克尔树证书代表了一种根本不同的 PKI 方法，将证书签名批量聚合到默克尔树中，相比传统的逐证书数字签名降低了计算开销。

telegram · zaihuapd · 9月30日 06:26

**背景**: 证书颁发机构（CA）是签发数字证书以验证公钥所有权的实体，使网页上的安全 HTTPS 连接成为可能。要被浏览器信任，CA 的根证书必须被纳入 Chrome、Apple、Microsoft 和 Mozilla 等主要浏览器厂商维护的根证书计划，每个计划都有严格的审计和纳入要求。ACME 协议最初由互联网安全研究小组（ISRG）为 Let's Encrypt 设计，是低成本自动化证书签发、续期和撤销的行业标准协议。默克尔树证书是一种新兴的后量子 PKI 方法，CA 对包含多个证书哈希的默克尔树根进行签名，而非用传统数字签名逐个签署每张证书，从而提高效率并抵御量子攻击。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Automatic_Certificate_Management_Environment">Automatic Certificate Management Environment - Wikipedia</a></li>
<li><a href="https://www.encryptionconsulting.com/merkle-tree-certificates/">Merkle Tree Certificates & Post - Quantum WebPKI</a></li>
<li><a href="https://www.ssl.com/article/what-are-root-certificates-and-why-do-they-matter/">What are Root Certificates , and Why Do They Matter? - SSL.com</a></li>

</ul>
</details>

**标签**: `#cloudflare`, `#certificate-authority`, `#web-pki`, `#post-quantum-cryptography`, `#merkle-tree-certificates`

---

<a id="item-5"></a>
## [Reddit 因 AI 爬虫问题将停用 RSS 订阅与公开 API](https://techcrunch.com/2026/09/30/reddit-is-killing-rss-feeds-ending-public-api-access-because-of-ai-bots/) ⭐️ 8.0/10

Reddit 于 2026 年 9 月 30 日宣布，将于 11 月 13 日停用 RSS 订阅支持，并于 2027 年 3 月关闭公开 API，主要原因是大面积 AI 机器人抓取和自动化滥用。公司要求版主迁移至 Discord Relay，并要求第三方开发者在 2027 年 1 月 12 日前完成注册，否则将被移除 API 访问权限。 此举将严重影响第三方开发者、自动化工具、RSS 阅读器以及长期依赖 Reddit 公开数据的开放互联网生态。这也反映了行业大趋势：主要平台正在封锁内容以防止未经授权的 AI 训练数据抓取，重新定义开放性与数据变现之间的平衡。 RSS 订阅将于 2026 年 11 月 13 日停用，公开 API 将于 2027 年 3 月关闭，为开发者留出过渡窗口。第三方应用和机器人开发者必须在 2027 年 1 月 12 日前完成注册，未注册的应用将被移除 API 访问权限。版主被要求改用 Discord Relay 作为子版块监控和提醒的官方替代方案。

telegram · zaihuapd · 10月1日 00:27

**背景**: RSS（简易信息聚合）是一项历史悠久的 Web 标准，允许用户和应用程序通过订阅源自动获取网站更新。公开 API 使第三方开发者能够以编程方式访问平台数据，从而构建应用、机器人和分析工具。近年来，AI 公司大规模抓取互联网数据——包括 Reddit 丰富的讨论存档——用于训练大语言模型，促使 Reddit 等平台加强对数据访问的管控，并寻求与 AI 公司签订数据授权协议。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://techbeat.co/story/reddit-ends-rss-feeds-and-public-api-as-ai-data-revenue-grows">Reddit Ends RSS Feeds and Public API as AI Data... // Tech Beat</a></li>

</ul>
</details>

**标签**: `#Reddit`, `#API`, `#RSS`, `#AI Scraping`, `#Platform Policy`

---
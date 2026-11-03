---
layout: default
title: "Horizon Summary: 2026-11-03 (ZH)"
date: 2026-11-03
lang: zh
---

> 从 42 条内容中筛选出 7 条重要资讯。

---

1. [Astra 直接编辑神经网络权重以改进 Qwen 模型](#item-1) ⭐️ 9.0/10
2. [Linux 内核 IPv4 TCP 高危释放后使用漏洞（CVE-2026-98432）](#item-2) ⭐️ 9.0/10
3. [vLLM v0.33.0 发布：升级至 PyTorch 2.14 与 CUDA 13.0，性能大幅提升](#item-3) ⭐️ 8.0/10
4. [Subvocal：用射频信号解码静默语音的智能眼镜](#item-4) ⭐️ 8.0/10
5. [WIRED 揭露 400 多个 AI 应用暗藏色情深伪功能](#item-5) ⭐️ 8.0/10
6. [Anthropic IPO 招股书披露前三季度营收 332 亿美元，净亏损 1040 亿美元](#item-6) ⭐️ 8.0/10
7. [阿布扎比与 OpenAI 签署四项协议，推进「机器可读政府」](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Astra 直接编辑神经网络权重以改进 Qwen 模型](https://rikiyat.github.io/blog/weight-space-programming/) ⭐️ 9.0/10

一篇博客文章展示了 GPT-6 Astra 能够原生地读取、理解并直接编辑神经网络的原始权重，无需任何额外训练或梯度下降，通过对小型 Qwen 模型进行有针对性的权重修改，实现了约 5 倍的数学性能提升。 这对递归自我改进（RSI）具有潜在的突破性意义，因为一个能够直接推理和操纵权重空间的大语言模型可以在不依赖传统训练流程的情况下迭代地改进自身或其他模型，这对 AI 安全与对齐提出了深刻的问题。 Astra 将 Qwen 模型中的循环失败模式追溯到第 15 层和第 19 层 MLP 写入的特定方向，然后从每层的 64 个输出列中减去该方向（共计 131,072 个权重），有效地消除了循环行为——这类似于从模型权重矩阵中消融单一行为方向。

hackernews · dbreunig · 11月2日 18:21 · [社区讨论](https://news.ycombinator.com/item?id=50341174)

**背景**: 权重空间编程是一种技术，通用语言模型读取神经网络的原始数值权重以推断其行为，然后直接修改这些权重来修复缺陷或添加能力——全程无需梯度下降或微调。Qwen 是阿里巴巴云开发的一系列开放权重的大型和小型语言模型，常被开源社区用作进一步微调的基础模型。GPT-6 Astra 是 OpenAI 最先进的模型，具备最先进的推理和计算机使用能力。传统上，修改神经网络的行为需要通过在大数据集上进行反向传播训练，因此由大语言模型直接编辑权重是一种根本不同的范式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://kingy.ai/blog/weight-space-programming-ai-agent-model-weights/">Weight-Space Programming: GPT-6 Astra Edits Qwen - kingy.ai</a></li>
<li><a href="https://elsolitario.org/en/2026/11/02/mit-csail-astra-edits-0-016-of-qwen3-weights/">Weight-Space Programming: How Astra Edits Weights</a></li>
<li><a href="https://github.com/xero00000/weight-space-programming/blob/main/">GitHub - xero00000/weight-space-programming: Agent skill for ...</a></li>

</ul>
</details>

**社区讨论**: 社区情绪从震惊到谨慎分析不等。用户 vessenes 对 Astra 原生的权重理解能力表示震惊，而 xg15 指出这与大语言模型快速掌握复杂系统的已证实能力一致。来自 vanyle 的一个值得注意的反驳观点认为这不是涌现能力而是训练行为，推测 OpenAI 刻意在神经权重数据上训练了 Astra 以追求递归自我改进。NitpickLawyer 提供了对 Astra 方法的详细技术验证，确认了其权重编辑的精确性。

**标签**: `#weight-space-programming`, `#recursive-self-improvement`, `#llm-capabilities`, `#neural-network-weights`, `#ai-safety`

---

<a id="item-2"></a>
## [Linux 内核 IPv4 TCP 高危释放后使用漏洞（CVE-2026-98432）](https://t.me/zaihuapd/44866) ⭐️ 9.0/10

Linux 内核 IPv4 TCP 协议栈中存在一个高危的释放后使用漏洞（CVE-2026-98432），攻击者可从网络侧远程利用，无需认证或用户交互。Anthropic 已公布针对 MPTCP 监听端口的远程代码执行（RCE）利用示例，Go 官方安全团队确认自 Go 1.24 起在 Linux 上默认为监听套接字启用 MPTCP，导致用 Go 编写的服务默认处于暴露状态。 该漏洞影响大量生产环境 Linux 服务器，可从网络侧直接利用，可能导致远程代码执行。由于 Go 1.24+ 默认启用 MPTCP，许多用 Go 构建的现代后端服务和 API 即使开发者从未显式配置 MPTCP，也处于暴露状态，影响范围被显著扩大。 通过设置 GODEBUG=multipathtcp=0 禁用 MPTCP 可以阻止 Anthropic 描述的特定利用方式，但并不能修复内核底层的释放后使用漏洞，其他利用路径仍然可能存在。该漏洞并非仅限于 MPTCP 场景，即使没有 MPTCP 监听的系统也可能受到影响，因此更新内核本身才是唯一的彻底缓解措施。

telegram · zaihuapd · 11月3日 02:37

**背景**: 多路径 TCP（MPTCP）是 IETF 标准化的 TCP 扩展协议（RFC 8684），允许单个 TCP 连接同时使用多个网络接口，从而提高吞吐量并提供故障转移能力。释放后使用漏洞是指程序在内存被释放后仍然访问该内存，可能导致任意代码执行。自 Go 1.24 起，Go 标准库的 net 包在 Linux 上默认为监听套接字启用 MPTCP（GODEBUG multipathtcp 默认值为 2），这意味着任何调用 Listen() 的 Go 服务都会打开 MPTCP 套接字，除非显式禁用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/golang/go/issues/82717">proposal: net: Disable MPTCP by default · Issue #82717 ...</a></li>
<li><a href="https://www.kernel.org/doc/html/next/networking/mptcp.html">Multipath TCP (MPTCP) — The Linux Kernel documentation</a></li>
<li><a href="https://en.wikipedia.org/wiki/Multipath_TCP">Multipath TCP - Wikipedia</a></li>

</ul>
</details>

**标签**: `#security`, `#linux-kernel`, `#vulnerability`, `#mptcp`, `#go`

---

<a id="item-3"></a>
## [vLLM v0.33.0 发布：升级至 PyTorch 2.14 与 CUDA 13.0，性能大幅提升](https://github.com/vllm-project/vllm/releases/tag/v0.33.0rc3) ⭐️ 8.0/10

vLLM v0.33.0 是一次重大版本更新，包含来自 389 位贡献者（其中 122 位为新贡献者）的 927 次提交，升级至 PyTorch 2.14.0 和 Triton 3.8.0，并放弃 CUDA 12.9，全面转向仅支持 CUDA 13.0 的 wheel 包和镜像。该版本新增了对包括 501B MoE Reflection Beam-1.0 在内的众多模型的支持，引入了与 libtorch ABI 稳定的 CUDA wheel 包、用于多节点服务的 AWS EFA Docker 镜像，以及在 NVIDIA 和 AMD 平台上显著的推测解码和解码性能改进。 作为最广泛采用的开源 LLM 推理引擎之一，vLLM 全面转向 CUDA 13.0 并升级至 PyTorch 2.14，为整个 LLM 服务生态系统设定了基础设施基线。性能改进——例如 GB300 上 Kimi-K3 的 1.5-2 倍解码加速以及 MI300X 上通过 MonoKernel 实现的 2.32 倍交互性提升——将直接降低大规模生产环境中 LLM 部署的服务成本并改善延迟。 重要的破坏性变更包括移除了 Medusa 和 MLP speculator、旧版 Ray 编译图执行器，以及弃用 --mamba-cache-mode；在生成暂停期间发送的请求现在会返回 HTTP 503，NIXL 连接器需要 1.5 或更高版本。该版本还引入了默认启用的 OpenAI 兼容 /v1/decisions 端点、可选的嵌入延迟分块、Rust 前端功能对齐推进、TP > 1 时的并发 worker 启动，以及一个能从卡住的进程转储堆栈跟踪的看门狗机制。

github · khluu · 11月2日 10:10

**背景**: vLLM 是一个高吞吐量的 LLM 推理与服务引擎，采用 PagedAttention 实现高效的 KV 缓存内存管理，被广泛部署于从 Llama 到 DeepSeek 等模型的生产服务中。推测解码是一种技术，由较小的

**标签**: `#vllm`, `#llm-inference`, `#pytorch`, `#cuda`, `#model-serving`

---

<a id="item-4"></a>
## [Subvocal：用射频信号解码静默语音的智能眼镜](https://news.ycombinator.com/item?id=50340088) ⭐️ 8.0/10

Subvocal 是一家由两位佐治亚理工学院计算机科学专业学生创立的 YC F26 公司，推出了使用射频（RF）信号将静默和内部语音解码为文本的智能眼镜。该眼镜发射无线电波穿透面部，在静默发音时被舌头、嘴唇和软腭的运动所调制，并通过训练基础模型将这些信号扰动解码为文本。 这项技术可能对免提和无障碍计算产生范式转变，使用户能够在图书馆、办公室和公共场所等不宜出声的环境中进行隐蔽的人机交互。如果成功，它将成为静默语音接口领域首个实用的可穿戴产品，而该领域尽管已有包括 MIT AlterEgo 项目在内的数十年研究，仍主要停留在学术阶段。 创始人最初尝试了肌电图（EMG）电极方案，但由于汗液导致的信号不稳定、电干扰、放置位置变化和用户不适等问题而放弃。当前的射频系统需要用户闭唇默念词语（而非仅在脑中思考），且公司面临重大的跨用户泛化挑战，因为每个人的面部解剖结构会产生截然不同的射频信号模式，他们正通过大规模数据采集来解决这一问题。

hackernews · aarushyadav · 11月2日 17:16

**背景**: 亚声语音识别（SVR）是检测亚声化的过程——即在不发出可听声音的情况下内部 articulation 词语——并将其转换为数字文本输出。静默语音接口（SSI）已被研究多年，旨在通过 EMG、脑电图（EEG）和电磁发音描记等多种传感技术实现无声通信。MIT 的 AlterEgo 项目是此前的一次重要尝试，使用 EMG 传感器读取下颌和面部的神经肌肉信号，但始终停留在研究原型阶段，未成为商业产品。据报道，Google 曾为智能手机探索过类似技术，但由于此类系统可能捕获的亲密生物识别数据带来的隐私担忧而搁置了该项目。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.wikiwand.com/en/articles/Subvocal_recognition">Subvocal recognition - Wikiwand</a></li>
<li><a href="https://www.designwhine.com/meet-alterego-the-technology-from-mit/">Meet AlterEgo: The Technology From MIT That Reads... | DesignWhine</a></li>
<li><a href="https://en.wikipedia.org/wiki/Subvocal_recognition">Subvocal recognition - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 社区反响总体热烈，用户称赞该技术如同科幻小说成真，并强调其在无障碍和免提计算方面的潜力。用户提出了关于不同鼻型和头型适配、处方镜片兼容性，以及设备是否能附加在现有眼镜上而非独立使用的实际关切。多位评论者提出了重大的隐私担忧，引用了 Google 曾搁置的类似项目，并质疑推理在何处进行以及设备是否能离线工作，还有人要求与 LipNet 等现有静默语音方案进行技术比较。

**标签**: `#hardware`, `#speech-recognition`, `#wearables`, `#accessibility`, `#YC`

---

<a id="item-5"></a>
## [WIRED 揭露 400 多个 AI 应用暗藏色情深伪功能](https://www.wired.com/story/hundreds-of-mundane-ai-apps-are-hiding-abusive-deepfake-features/) ⭐️ 8.0/10

WIRED 于 11 月 2 日发布调查，揭露了一个由 400 多个关联应用与网站组成的网络，它们伪装成宠物画像、语言学习等普通 AI 工具，在特定条件下暗中加载色情深度伪造界面，允许用户上传他人照片生成露骨图像或视频。在 WIRED 通报后，苹果下架了 19 款应用，谷歌移除了 Google Play 上仍在架的多数应用（累计下载超 35 万次），Meta 则阻止了 209 款相关应用投放广告。 这项调查暴露了应用商店审核流程的关键漏洞：开发者可以通过正常内容通过审核，随后替换远端网页内容来提供未经同意的色情深伪服务，影响可能达数十万用户——包括未成年人，因为许多应用被标记为适合所有年龄。该网络的规模及其逃避主要平台检测的能力，凸显了 AI 治理与内容审核方面的系统性缺陷，亟需引起重视。 苹果确认开发者先以正常内容通过审核，随后替换远端网页内容，这种手法被称为审核后内容替换。研究人员通过共享代码、域名注册信息及广告追踪标识符将这一网络关联起来，并追溯到中文开发者及一家香港注册公司，但运营方未回应置评请求。

telegram · zaihuapd · 11月2日 12:45

**背景**: 深度伪造技术利用生成式 AI 模型，通常基于深度学习中的编码器-解码器架构，来合成或篡改图像和视频，效果逼真到足以欺骗观众。在本调查的语境中，这些应用允许用户上传真实人物的普通照片，生成未经同意的露骨图像。应用商店审核绕过技术是指先提交一个合法应用通过审核，然后在审核通过后远程更改应用加载的网页内容——这意味着恶意功能永远不会被审核人员看到。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.researchgate.net/publication/390972234_The_Rise_of_AI-Generated_Deepfakes_Techniques_Challenges_Implications_and_Countermeasures">(PDF) The Rise of AI- Generated Deepfakes : Techniques, Challenges...</a></li>
<li><a href="https://virbo.wondershare.com/ai-voice-clone/deepfake-ai-image-generator.html">7 Best Free Deepfake Image Generators in 2025</a></li>

</ul>
</details>

**标签**: `#AI ethics`, `#deepfake`, `#platform security`, `#investigative journalism`, `#AI governance`

---

<a id="item-6"></a>
## [Anthropic IPO 招股书披露前三季度营收 332 亿美元，净亏损 1040 亿美元](https://www.cnbc.com/2026/11/02/anthropic-ant-s-1-quarter-financials.html) ⭐️ 8.0/10

Anthropic 周一更新 IPO 招股书，披露截至 2026 年 9 月 30 日的前三季度营收达 332.4 亿美元，同比增长约 1200%，其中第三季度营收约 170 亿美元。同期净亏损达 1040 亿美元，远高于去年同期的 251 亿美元，同时公司累计算力及基础设施采购与租赁承诺约 8954 亿美元。 这份文件为外界提供了前沿 AI 公司在大规模运营下的财务经济透明度，同时揭示了惊人的营收增长和竞争所需的巨额资本投入。8954 亿美元的基础设施承诺凸显了建设和维护尖端 AI 能力所需的巨大投资，而账面亏损与实际现金消耗之间的区别对评估公司真实财务状况至关重要。 1040 亿美元的净亏损主要源于可转换债券及衍生负债的公允价值变动——随着 Anthropic 估值上升，这些负债的公允价值随之增加，产生了大额非现金账面亏损，并不代表实际经营现金消耗。8954 亿美元的累计承诺几乎全部用于算力和基础设施，凸显了前沿 AI 开发的资本密集型特征。

telegram · zaihuapd · 11月2日 15:12

**背景**: 可转换债券可能包含嵌入式衍生成分（即转股权），根据适用会计准则需按公允价值计量。当公司在多轮融资之间估值大幅上升时，该衍生负债的公允价值随之增加，在利润表上产生非现金的账面亏损，尽管实际并未发生现金支出。这种按市值计量的会计处理在通过可转换工具融资的 IPO 前公司中很常见，由此产生的账面亏损在标题中可能显得触目惊心，但并不反映公司的实际现金消耗或经营状况。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ipobonanza.com/news/2026-10-06-how-to-read-a-mark-to-market-loss-on-convertible-instruments">How to Read a Mark-to-Market Loss on Convertibles | IPO Bonanza</a></li>
<li><a href="https://aitechmodel.com/anthropic-72-billion-convertible-notes-charge/">Anthropic Convertible Notes: The $72 Billion Charge</a></li>

</ul>
</details>

**标签**: `#anthropic`, `#ai-finance`, `#ipo`, `#infrastructure`, `#frontier-ai`

---

<a id="item-7"></a>
## [阿布扎比与 OpenAI 签署四项协议，推进「机器可读政府」](https://thenextweb.com/news/openai-abu-dhabi-deals-machine-readable-government-mubadala) ⭐️ 8.0/10

阿布扎比周一与 OpenAI 签署四项协议，涵盖政府运营、投资分析、能源和教育领域。旗舰项目「机器可读政府」计划将政策法规转换为 AI 可读格式，协助官员核查许可与证书申请，已在食品进口领域开展试点。 这是迄今最全面的政府级 AI 采用举措之一，涉及穆巴达拉、G42 和 ADNOC 等阿布扎比主要实体，覆盖多个关键领域。「机器可读政府」概念可能从根本上改变政府运作方式，使政策能被 AI 系统直接解读，有望为其他国家树立先例。 穆巴达拉与 OpenAI 及 G42 旗下 Inception42 合作开展投资分析，Inception42 另签五年协议向阿联酋政府、企业和学校提供 AI 模型。ADNOC 成为首家使用 OpenAI Frontier 平台的能源公司，值得注意的是，在机器可读政府计划中，人类官员保留最终决定权。

telegram · zaihuapd · 11月2日 15:55

**背景**: 机器可读政府是指将立法、政策和法规转换为结构化的、机器友好的格式，使 AI 系统能直接解读和处理，从而实现更高效透明的治理。G42 是一家成立于 2018 年、总部位于阿布扎比的阿联酋人工智能开发控股公司，其子公司 Inception 专注于行业特定的 AI 解决方案，包括阿拉伯语原生 Jais 模型。OpenAI 的 Frontier 平台是近期推出的企业级平台，旨在为企业客户构建、部署和管理 AI 代理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/G42_(company)">G 42 ( company ) - Wikipedia</a></li>
<li><a href="https://news.aibase.com/news/25321">OpenAI Launches Frontier Platform : Building AI Colleagues to...</a></li>
<li><a href="https://www.linkedin.com/pulse/machine-readable-legislation-key-milestone-toward-smarter-munir-rbmne">Machine - Readable Legislation: A Key Milestone Toward Smarter...</a></li>

</ul>
</details>

**标签**: `#openai`, `#government-ai`, `#abu-dhabi`, `#machine-readable-government`, `#public-sector`

---
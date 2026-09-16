---
layout: default
title: "Horizon Summary: 2026-09-16 (ZH)"
date: 2026-09-16
lang: zh
---

> 从 33 条内容中筛选出 3 条重要资讯。

---

1. [安全研究人员揭露 Flock 监控摄像头的严重漏洞](#item-1) ⭐️ 8.0/10
2. [TMLR 测试即将被桌面拒稿论文的作者对自身论文的理解程度](#item-2) ⭐️ 8.0/10
3. [苹果 A20 Pro：首款 2nm 手机芯片搭配自研 C2 基带与 N1 无线芯片](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [安全研究人员揭露 Flock 监控摄像头的严重漏洞](https://www.wired.com/story/hackers-flock-camera-data-shows-how-system-works/) ⭐️ 8.0/10

安全研究人员发现 Flock 监控摄像头存在硬编码 API 密钥和明文存储凭证的问题，任何获得设备物理访问权限的人都可以提取敏感认证数据并可能访问 Flock 的后端服务器。该发现由 404media 协作报道，Distributed Denial of Secrets 也已公开了被破解设备的分区镜像供公众分析。 Flock 摄像头被美国各地执法机构广泛部署，用于自动车牌识别和大规模监控，这意味着这些漏洞不仅暴露了技术缺陷，还危及数百万公民的车辆数据隐私。在一个专为不安全的公共空间设计的产品中发现硬编码凭证和明文存储，暴露了关键监控基础设施在威胁建模方面的根本性失败。 漏洞包括嵌入设备固件中的硬编码 API 密钥，可用于请求设备上明文存储的凭证，从而可能获得对 Flock 服务器基础设施的访问权限。Flock 的漏洞披露政策实际上通过禁止研究人员与设备交互或下载其数据来阻碍有意义的安全研究，使得几乎不可能通过合法渠道展示所发现漏洞的严重性。

hackernews · driverdan · 9月16日 13:18 · [社区讨论](https://news.ycombinator.com/item?id=49726586)

**背景**: Flock Safety 是一家美国私营公司，制造被全国数千个执法机构使用的自动车牌识别（ALPR）摄像头和监控系统。与传统交通摄像头不同，Flock 摄像头持续捕获并存储车牌数据，创建可搜索的车辆移动数据库，引发了重大的公民自由关切。硬编码密钥——直接嵌入源代码中的 API 密钥、密码和令牌——被 OWASP A07:2021 归类为基础设施泄露的最常见原因之一，而明文凭证存储则违反了基本安全最佳实践，使认证数据对任何拥有文件访问权限的人均可读。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Flock_Safety">Flock Safety - Wikipedia</a></li>
<li><a href="https://mashable.com/tech/flock-cameras-explained-surveillance">What are Flock cameras? How they work and why they’re ...</a></li>
<li><a href="https://community.owasp.org/vulnerabilities/Password_Plaintext_Storage">Password Plaintext Storage | OWASP Foundation</a></li>

</ul>
</details>

**社区讨论**: 评论者一致谴责 Flock 的安全实践是不称职的表现，指出硬编码凭证和明文存储反映了对上市速度的优先于适当安全架构的考量。多位用户批评 Flock 的漏洞披露政策是故意设计来营造负责任安全形象的，实际上并未促进有意义的漏洞报告，而其他人则指出在不安全的公共空间部署现成硬件而未在威胁模型中考虑物理访问是产品管理的根本性失败。

**标签**: `#security`, `#surveillance`, `#vulnerability-disclosure`, `#privacy`, `#iot`

---

<a id="item-2"></a>
## [TMLR 测试即将被桌面拒稿论文的作者对自身论文的理解程度](https://www.reddit.com/r/MachineLearning/comments/1wid67h/tmlr_reached_out_to_the_authors_of_10_papers/) ⭐️ 8.0/10

TMLR 的联合主编亲自采访了 10 篇即将被桌面拒稿论文的作者，要求他们解释自己的投稿内容。仅有一位作者能够充分回答所有问题，三位作者无法回答基本问题，三位在技术细节上遇到困难，其余作者则撤稿、表示无法参加或未出席。 这项调查揭示了作者无法解释自身研究的令人不安的趋势，引发了对机器学习出版中代笔、论文工厂和 AI 生成投稿的严重担忧。这些发现可能推动各学术出版平台在验证作者身份和投稿诚信方面的改革。 在 10 篇投稿中，一篇被撤稿，一位作者表示无法参加，一位未出席，三位无法回答基本问题，三位能讨论高层次想法但在技术细节上遇到困难，仅有一位回答了所有问题——但即便如此，采访者仍发现该论文存在一个重大缺陷。该调查由 TMLR 的联合主编进行，并在 Medium 文章中记录。

reddit · r/MachineLearning · /u/hihey54 · 9月16日 23:20

**背景**: TMLR（机器学习研究汇刊）成立于 2021 年 12 月，旨在补充 JMLR 并服务于不断增长的机器学习研究社区。桌面拒稿是指编辑在论文进入完整同行评审流程之前就将其拒绝，通常是因为论文未达到基本的质量、范围或格式标准。这项调查的动机是对研究诚信日益增长的担忧，包括 AI 生成论文的增多以及列名作者可能并未实质性参与研究工作的署名行为。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://jmlr.org/tmlr/">Transactions on Machine Learning Research (TMLR)</a></li>
<li><a href="https://medium.com/@hugo_larochelle_65309/announcing-the-transactions-on-machine-learning-research-3ea6101c936f">Announcing the Transactions on Machine Learning Research | by Hugo Larochelle | Medium</a></li>
<li><a href="https://link.springer.com/article/10.1007/s11948-017-9921-3">Establishing Sensible and Practical Guidelines for Desk Rejections</a></li>

</ul>
</details>

**标签**: `#machine-learning`, `#research-integrity`, `#peer-review`, `#academic-publishing`, `#TMLR`

---

<a id="item-3"></a>
## [苹果 A20 Pro：首款 2nm 手机芯片搭配自研 C2 基带与 N1 无线芯片](https://www.bilibili.com/video/BV1oZeA6fERD) ⭐️ 8.0/10

苹果发布了首款 2nm 手机芯片 A20 Pro，搭载于 iPhone 18 Pro 系列，配备 6 核 CPU（提速 20%）、7 核 GPU（提速 40%）、双 16 核神经网络引擎，内存带宽较 A19 Pro 提升 50%。同时发布了自研 C2 基带（上传提速 50%、功耗降 15%）和首款定制 N1 无线芯片，支持 Wi-Fi 7、蓝牙 6 及 Thread 协议。 A20 Pro 是业界首款商用 2nm 芯片，标志着半导体制造的重大里程碑，使苹果在移动计算性能上取得显著领先优势。全面采用自研 C2 基带和 N1 无线芯片意味着苹果实现了最深度的垂直整合，取代了长期供应商 Qualcomm 和 Broadcom，将重塑移动半导体供应链格局。 A20 Pro 采用借鉴 M 系列的新封装设计，搭配 3 倍面积的 VC 均热板散热系统，使持续性能较上代最多提升 40%。值得注意的是，美国版 iPhone 18 Pro Max 仍使用 Qualcomm 基带而非 C2 芯片，在基带技术上造成了区域性的硬件差异。

telegram · zaihuapd · 9月16日 13:24

**背景**: 台积电的 2nm 工艺节点代表半导体制造的最新进展，相比上一代 3nm 提供更高的能效和晶体管密度。VC 均热板利用液气相变原理高效地将热量均匀分布在芯片表面，对于在紧凑移动设备中维持高性能至关重要，因为芯片热流密度持续攀升。苹果一直在逐步用自研芯片替代第三方组件——此前已将 Mac 从 Intel 处理器过渡到 M 系列芯片——如今又在 iPhone 中用自研的 C2 基带和 N1 无线芯片替代 Qualcomm 基带和 Broadcom 无线芯片。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.androidheadlines.com/2026/09/iphone-18-pro-duo-ditch-qualcomm-apple-c2-modem.html">iPhone 18 Pro Has Apple C2 Modem Instead of Qualcomm's</a></li>
<li><a href="https://www.techspot.com/news/109402-new-iphones-get-wi-fi-7-bluetooth-6.html">New iPhones get Wi - Fi 7 and Bluetooth 6 via Apple 's in-house...</a></li>
<li><a href="https://www.androidheadlines.com/2026/09/apple-clarifies-eu-iphone-18-pro-max-c2-modem-error.html">EU iPhone 18 Pro Max Keeps C2 Modem Chip</a></li>

</ul>
</details>

**标签**: `#apple`, `#semiconductors`, `#2nm`, `#a20-pro`, `#mobile-chips`

---
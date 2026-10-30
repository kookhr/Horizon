---
layout: default
title: "Horizon Summary: 2026-10-30 (ZH)"
date: 2026-10-30
lang: zh
---

> 从 39 条内容中筛选出 4 条重要资讯。

---

1. [币安遭遇 56 亿美元历史性加密货币盗窃](#item-1) ⭐️ 9.0/10
2. [van der Waerden 数 W(2;3,21)=416 由 Lean 4 内核验证的神经符号系统证明](#item-2) ⭐️ 9.0/10
3. [PHP2Shell 与 Linux XFRM 链式漏洞攻陷 25 台政府服务器](#item-3) ⭐️ 8.0/10
4. [🤖 Anthropic 借助 Claude，用 Rust 重写服务 API，CPU 用量降四至五成](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [币安遭遇 56 亿美元历史性加密货币盗窃](https://arkm.com/explorer/entity/21a94755-f604-45e5-9501-6542e23005e8) ⭐️ 9.0/10

10 月 29 日，约 56 亿美元从币安热钱包中被盗，Circle 和 Tether 已冻结与可疑钱包相关的约 24 亿美元 USDC 和 USDT，涉及以太坊和波场网络。被盗金额远超币安 SAFU 紧急保险基金的规模，该基金截至 2022 年 1 月仅价值 10 亿美元。 这可能是历史上最大的加密货币交易所黑客事件，56 亿美元的损失远超币安 10 亿美元的 SAFU 基金，意味着用户损失可能无法得到全额赔偿。该事件引发了对中心化交易所安全性的深刻质疑，以及稳定币中心化冻结机制虽在此有帮助却违背加密货币去中心化理念的悖论。 具体冻结金额包括以太坊上的 9.7115 亿 USDT 和 8.23 亿 USDC、波场上的 3.1273 亿 USDT 以及以太坊上的 1.75 亿 USDT，但社区成员报告攻击者可能仍在积极将 USDT 兑换为其他资产以规避冻结。SAFU 基金成立于 2018 年 7 月，由交易手续费的 10%注入，以 BTC 形式存储在独立冷钱包中，不足以覆盖 56 亿美元的损失。

hackernews · Tiberium · 10月29日 21:38 · [社区讨论](https://news.ycombinator.com/item?id=50296470)

**背景**: 币安的 SAFU（用户安全资产基金）是 2018 年 7 月创建的紧急保险基金，由所有交易手续费的 10%注入，据 2022 年 1 月报告价值 10 亿美元。像 Tether（USDT）和 Circle（USDC）这样的稳定币发行方拥有冻结特定地址的技术能力，可以有效将钱包列入黑名单并阻止资金转移——这是这些代币智能合约中内置的中心化控制功能。从历史上看，大型中心化交易所的崩溃——如 FTX——往往发生在加密货币熊市的末期。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.binance.com/en/blog/nft/2786007584689975895">A Closer Look at Binance 's SAFU Fund and Robust... | Binance Blog</a></li>
<li><a href="https://www.cryptotimes.io/2026/10/30/binance-hack-tether-usdt-and-circle-usdc-freeze-1-8b-in-stablecoins-linked-to-suspected-wallets/">Binance Hack: Tether (USDT) and Circle (USDC) Freeze $1.8B in ...</a></li>
<li><a href="https://www.aletheia.software/blog/stablecoin-freeze-powers">Understanding Stablecoin Freeze Powers (USDT & USDC)</a></li>

</ul>
</details>

**社区讨论**: 社区情绪严重分化，一些人提供了冻结交易哈希的详细技术分析，另一些人则宣称加密货币因中心化的出入金点使区块链的理论优势失效而彻底失败。多位评论者指出 Circle 和 Tether 这些中心化实体的稳定币冻结功能正在挽救局势的讽刺意味，同时也有人指出攻击者似乎仍在积极将 USDT 兑换为其他资产以规避冻结。数名用户将此与 FTX 等历史上通常在熊市底部发生的 CEX 崩溃事件进行类比。

**标签**: `#cryptocurrency`, `#security`, `#binance`, `#blockchain`, `#hacking`

---

<a id="item-2"></a>
## [van der Waerden 数 W(2;3,21)=416 由 Lean 4 内核验证的神经符号系统证明](https://www.reddit.com/r/MachineLearning/comments/1xivpue/w2321_416_a_van_der_waerden_number_conjectured_by/) ⭐️ 9.0/10

由 Kullmann 于 2010 年猜想、且 DeepMind 形式化猜想列表今年仍标记为开放的 van der Waerden 数 W(2;3,21)=416，已通过 Lean 4 内核验证的证明正式确立，该证明由 Hupyy 公司的神经符号系统 LPM（Large Proof Model）生成。证明涵盖 209 个案例和 38,661,140 个已验证的叶公式，每个反驳均由 cake_pr（一个在 CakeML 中验证的 LRAT 检查器）检查，并通过密码学摘要绑定到其 Lean 项。 这一成果利用具备完整形式化验证的神经符号系统解决了一个悬置 15 年的组合数学开放猜想，证明 AI 辅助定理证明现已能攻克此前自动化方法无法处理的问题。严格的内核验证方法论和高达 13.6 GB 的证据包为机器生成的数学证明树立了新的可复现性标准，可能重塑数学界验证 AI 产出结果的方式。 该证明确立了以下事实：{1,...,416} 的任意红蓝着色必然包含红色 3 项或蓝色 21 项等差数列，而 {1,...,415} 的某种着色可以同时避免两者。除非 Lean 内核或 cake_pr 接受，否则任何步骤均不计入证明；完整的证据包（包括 Lean 源码、检查器记录和重放工具包）可通过下载后运行 'shasum -a 256 -c SHA256SUMS' 独立验证。

reddit · r/MachineLearning · /u/Rodriguez909 · 10月29日 20:46

**背景**: van der Waerden 定理是 Ramsey 理论中的基础结果，它指出对于任意正整数 r 和 k，存在一个最小的数 N，使得对 {1,...,N} 的任何 r-着色必然包含长度为 k 的单色等差数列；这个 N 即为 van der Waerden 数。记号 W(2;3,21) 指的是一个非对称双色情形：最小的 N 保证在第一种颜色中出现 3 项等差数列，或在第二种颜色中出现 21 项等差数列。CakeML 是一种经过形式化验证的 ML 语言实现，其正确性保证延伸至 cake_pr 等证明检查器，后者用于验证 SAT 求解中常用的 LRAT（线性归结非对称重言式）证明。LPM（Large Proof Model）由 Hupyy 公司开发，是一种神经符号系统，旨在通过结合神经引导与符号验证来弥合抽象人类意图与数学验证执行之间的鸿沟。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Van_der_Waerden's_theorem">Van der Waerden's theorem - Wikipedia</a></li>
<li><a href="https://cakeml.org/tacas21.pdf">Checking in CakeML</a></li>
<li><a href="https://largeproofmodel.com/">Large Proof Model (LPM)</a></li>

</ul>
</details>

**标签**: `#formal-verification`, `#theorem-proving`, `#combinatorics`, `#neuro-symbolic`, `#lean4`

---

<a id="item-3"></a>
## [PHP2Shell 与 Linux XFRM 链式漏洞攻陷 25 台政府服务器](https://dreamgroup.com/blog/chained-php2shell-exploit-roots-25-servers) ⭐️ 8.0/10

Dream Group 发布的取证报告显示，攻击者将 PHP2Shell 漏洞（CVE-2026-109618/CVE-2026-109619）与 Linux 内核 XFRM ESP-in-TCP 漏洞进行链式利用，成功获取了 25 台服务器（包括美国政府基础设施）的 root 权限。该攻击链首先利用 PHP 5.4 至 8.5 版本中的内存安全缺陷实现远程代码执行，随后通过内核 XFRM 子系统进行权限提升。 该事件展示了针对高价值政府目标的链式漏洞利用在现实中的成功实践，凸显了将 Web 层远程代码执行与内核权限提升相结合可以绕过纵深防御策略。它强调了 Linux 内核庞大攻击面带来的持续风险，以及同时修补应用层和内核层的紧迫性。 PHP2Shell 漏洞（CVE-2026-109618 和 CVE-2026-109619）是影响 PHP 5.4 至 8.5 版本的内存安全缺陷，可实现远程代码执行。第二阶段利用了 Linux 内核 XFRM 子系统中与 ESP-in-TCP 数据包处理相关的漏洞；社区成员注意到初始载荷需要约 383MB 内存，表明该漏洞利用的内存耗尽技术存在一定的粗糙之处。

hackernews · 882542F3884314B · 10月29日 10:42 · [社区讨论](https://news.ycombinator.com/item?id=50286987)

**背景**: PHP2Shell 是指 PHP 5.4 至 8.5 版本中的一对高危漏洞（CVE-2026-109618 和 CVE-2026-109619），通过内存安全缺陷实现远程代码执行，可能使攻击者完全控制 Web 主机。Linux XFRM 子系统负责管理 IPsec 变换，包括 ESP（封装安全载荷）协议，近期已出现多个相关漏洞，如 CVE-2026-43107 和 CVE-2026-43284（Dirty Frag）。链式漏洞利用是指将两个或多个漏洞依次组合——通常是先进行远程代码执行，再进行本地权限提升——以实现单个漏洞无法完成的完整系统攻陷。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/PHP2Shell">PHP2Shell - Wikipedia</a></li>
<li><a href="https://www.sentinelone.com/vulnerability-database/cve-2026-43107/">CVE-2026-43107: Linux Kernel XFRM DoS Vulnerability</a></li>
<li><a href="https://hackviser.com/labs/common-vulnerabilities/cve-2026-43284">Dirty Frag – Linux Kernel Local Privilege Escalation... | Hackviser</a></li>

</ul>
</details>

**社区讨论**: 社区讨论的核心围绕 Linux 内核不必要地庞大的攻击面，用户质疑为何 MPTCP 和 XFRM 等功能在许多服务器不需要时仍默认启用。一位评论者对该漏洞利用的粗糙程度表示惊讶，指出即使是 AI 辅助的漏洞开发也能通过优化达到类似效果。一位参与者根据报告中逐字引用的 PAN-OS 设置和 SELinux 配置推测，未具名的防火墙厂商很可能是 Palo Alto Networks。另一位参与者则指出 Dream Group 由前奥地利总理 Sebastian Kurz 创立，后者因腐败丑闻而辞职。

**标签**: `#security`, `#exploit`, `#linux-kernel`, `#incident-response`, `#vulnerability`

---

<a id="item-4"></a>
## [🤖 Anthropic 借助 Claude，用 Rust 重写服务 API，CPU 用量降四至五成](https://latent.space/p/opus55/) ⭐️ 8.0/10

Anthropic 借助 Claude 将其 Messages API 从 Python 重写为 Rust，使 CPU 用量降低了 40% 至 50%，并将首字响应时间缩短了 10% 至 20%。

telegram · zaihuapd · 10月29日 03:13

**标签**: `#rust`, `#anthropic`, `#ai-assisted-coding`, `#performance-optimization`, `#api-migration`

---
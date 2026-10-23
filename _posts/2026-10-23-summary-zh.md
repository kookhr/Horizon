---
layout: default
title: "Horizon Summary: 2026-10-23 (ZH)"
date: 2026-10-23
lang: zh
---

> 从 44 条内容中筛选出 13 条重要资讯。

---

1. [利用 LLM 和硬件 KVM 实现 Nintendo Switch 2 越狱](#item-1) ⭐️ 9.0/10
2. [甲骨文发布 Java SE JSSE 组件高危漏洞安全警报](#item-2) ⭐️ 9.0/10
3. [Quad9 DNS 解析器因盗版封锁法院令将退出法国](#item-3) ⭐️ 8.0/10
4. [NVIDIA OpenShell：面向自主 AI 代理集群的安全运行时](#item-4) ⭐️ 8.0/10
5. [通过 QEMU 在 Android 设备上运行完整的 iOS 16.5 XNU 内核](#item-5) ⭐️ 8.0/10
6. [eMudhra 因安全事件退出全球 SSL/TLS 证书业务](#item-6) ⭐️ 8.0/10
7. [Earcut 库在地图多边形三角化中被 Earstrip 超越](#item-7) ⭐️ 8.0/10
8. [Anthropic 将 Agent Skills 标准捐赠给 Agentic AI Foundation](#item-8) ⭐️ 8.0/10
9. [Carbon-X：支持 DNA 与文本联合分析的开放 14.8B 模型](#item-9) ⭐️ 8.0/10
10. [Anthropic 发布 Claude API 2026-10-21 新版本，移除采样参数](#item-10) ⭐️ 8.0/10
11. [澳洲法院裁定苹果须向第三方应用商店开放 iPhone](#item-11) ⭐️ 8.0/10
12. [333 个被植入后门的 Tor 出口节点被标记下线](#item-12) ⭐️ 8.0/10
13. [禁运 Nvidia B300 芯片现身中国国有网络](#item-13) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [利用 LLM 和硬件 KVM 实现 Nintendo Switch 2 越狱](https://pepsipu.com/blog/2026-10-switch2-jailbreak-ns2jb/) ⭐️ 9.0/10

安全研究员 pepsipu 发布了"ns2jb"的详细信息，这是一个针对 Nintendo Switch 2 的纯软件、有线连接的漏洞利用方案，可在最新的 23.0.1 固件上实现解密文件系统的读写访问。该突破性进展显著地利用了 OpenAI 的 Codex LLM 结合 JetKVM 硬件来自动化漏洞研究，其中包括使用蓝牙智能开关设备在系统崩溃时物理按下主机的电源按钮。 这是 Nintendo Switch 2 首次被报道的越狱，可能使游戏转储和主机独占游戏在任意硬件上运行，这对 Nintendo 的平台安全构成了最坏情况。在主机游戏之外，通过 KVM 赋予 LLM "手和眼"以自主进行硬件安全研究的方法，标志着自动化漏洞发现的新范式。 该漏洞利用是一个有线连接的用户态漏洞利用，意味着它需要连接到主机计算机，并且每次 Switch 2 启动时都必须重新触发，因为它没有实现持久的内核级访问。该方法利用与特定 Switch 1 游戏的向后兼容性来获得初始访问权限，并且在自动化测试设置中使用了一个 SwitchBot Bot（一个支持蓝牙的物理执行器），在测试期间主机崩溃时按下电源按钮。

hackernews · ledoge · 10月22日 08:01 · [社区讨论](https://news.ycombinator.com/item?id=50192536)

**背景**: 游戏主机越狱涉及利用软件或硬件漏洞来绕过制造商的限制，允许用户运行自制应用程序、修改游戏或转储游戏文件。Nintendo Switch 2 与其前身一样，采用加密文件系统和签名代码来防止未经授权的访问，这意味着成功的漏洞利用必须解密这些保护才能实现有意义的读写访问。"用户态"访问是指在非特权用户空间中获得执行权限，虽然不如内核访问强大，但仍足以运行自定义代码和进行逆向工程。在安全研究中使用像 Codex 这样的 LLM 是一个新兴趋势，AI 代理被赋予工具以与系统交互，有可能自动化漏洞发现中的重复性任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arstechnica.com/gaming/2026/10/switch-2-jailbreak-gives-hackers-new-ways-to-run-homebrew-and-mod-games/">Switch 2 security takes a hit as hackers unlock homebrew access</a></li>
<li><a href="https://kotaku.com/nintendo-switch-2-jailbreak-hack-exploit-piracy-homebrew-emulation-modding-2000748784">The Switch 2 Has Been Jailbroken For The First Time - Kotaku</a></li>
<li><a href="https://en.gamegpu.com/news/zhelezo/konsol-nintendo-switch-2-vzlomali-cherez-uyazvimost-smilebasic">The Nintendo Switch 2 console was hacked using a SmileBASIC ...</a></li>

</ul>
</details>

**社区讨论**: 评论者对技术上的巧妙性表示惊叹，特别是使用蓝牙智能开关按下电源按钮的鲁布·戈德堡式做法，一位用户将其戏称为"Switch SwitchBot Bot"。几项讨论集中在通过 KVM 赋予 LLM 物理控制以进行自动化安全研究的更广泛影响上，而另一些人指出作者本身的安全专业知识可能是比 AI 更大的因素，还有一位用户质疑作者是如何绕过 Codex 对漏洞研究的安全限制的。

**标签**: `#security`, `#hardware-hacking`, `#nintendo-switch`, `#jailbreaking`, `#llm-agents`

---

<a id="item-2"></a>
## [甲骨文发布 Java SE JSSE 组件高危漏洞安全警报](https://www.oracle.com/security-alerts/alert-cve-2026-91403.html) ⭐️ 9.0/10

甲骨文发布了针对 CVE-2026-91403 的严重安全警报，这是 Java SE 的 JSSE 组件中一个 CVSS 评分高达 9.1 分的高危远程代码执行漏洞。该漏洞影响包括 8u511、11.0.33、17.0.21、21.0.13、25.0.5、27.0.1 及多个 GraalVM 版本在内的多个 Java SE 版本，甲骨文已发布修复补丁并呼吁用户立即升级。 该漏洞极其危险，因为它允许未经身份验证的远程攻击者通过网络进行利用，可能严重破坏关键数据的机密性与完整性。任何运行受影响 Java SE 版本的组织都面临风险，这使得立即打补丁成为全行业系统管理员和开发者的首要任务。 该漏洞位于 JSSE（Java 安全套接字扩展）组件中，该组件负责处理 Java 中用于安全网络通信的 TLS 和 SSL 协议。攻击者无需身份验证即可利用此漏洞，甲骨文已确认数据的机密性和完整性均面临风险。所有受影响版本（包括 GraalVM 发行版）均有修复补丁可用。

telegram · zaihuapd · 10月22日 12:30

**背景**: Java 安全套接字扩展（JSSE）是一个核心 Java API，通过在 Java 运行时环境中提供 TLS 和 DTLS 协议的框架和实现来保障互联网通信安全。它负责处理数据加密、服务器身份验证和消息完整性等关键功能。GraalVM 是由 Oracle Labs 开发的高性能 JDK 发行版，具备即时编译（JIT）和提前编译（AOT）能力。CVSS 评分 9.1 表示严重级别，意味着该漏洞易于被利用且可能对受影响系统造成重大影响。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.oracle.com/en/java/javase/11/security/java-secure-socket-extension-jsse-reference-guide.html">Java Secure Socket Extension (JSSE) Reference Guide</a></li>
<li><a href="https://en.wikipedia.org/wiki/GraalVM">GraalVM</a></li>

</ul>
</details>

**标签**: `#security`, `#java`, `#oracle`, `#vulnerability`, `#cve`

---

<a id="item-3"></a>
## [Quad9 DNS 解析器因盗版封锁法院令将退出法国](https://quad9.net/news/blog/au-revoir-france/) ⭐️ 8.0/10

由瑞士基金会运营的注重隐私的公共 DNS 解析器 Quad9 宣布，将在 11 月 24 日之后关闭其在法国的 DNS 解析服务，此前法院命令其封锁盗版网站的访问。该公司认为，在维持隐私承诺的同时选择性封锁特定域名在技术上是不可行的，而且在索尼音乐使用 VPN 绕过基于 geoIP 的封锁后，该公司因藐视法庭被罚款。 这为互联网基础设施和司法管辖冲突设定了重要先例，一家主要的 DNS 解析器选择退出整个国家，而不是妥协其隐私承诺或遵守技术上不可行的封锁命令。它凸显了通过 DNS 层面封锁进行版权执法与 DNS 提供商的隐私和安全承诺之间日益增长的紧张关系，此前 Google 和 Cloudflare 已被迫遵守类似的法国禁令。 Quad9 的首席技术官确认，在 11 月 24 日之后可能会使用 geoIP 过滤器来阻止法国用户访问其服务，同时承认 geoIP 封锁并不完美。法律压力来自索尼音乐娱乐有限公司，该公司使用 VPN 从德国访问被封锁的内容，然后向法院报告 Quad9 不合规，导致藐视法庭罚款；Canal+也在法国获取了针对 DNS 解析器的类似网络封锁禁令。

hackernews · farrokhi · 10月22日 14:32 · [社区讨论](https://news.ycombinator.com/item?id=50195959)

**背景**: Quad9 是由总部位于苏黎世的瑞士非营利组织 Quad9 基金会运营的免费全球公共递归 DNS 解析器，可阻止访问与恶意软件和网络钓鱼相关的域名。DNS 解析器将域名转换为 IP 地址，一些司法管辖区已开始命令解析器封锁对特定域名（如盗版网站）的访问，作为版权执法机制。然而，像 Quad9 这样注重隐私的解析器不会记录用户查询，这使得在不损害其隐私承诺的情况下进行选择性域名封锁在技术上具有挑战性。此前类似法国网络封锁禁令的目标包括 Google、Cloudflare 和 Cisco，后者在两年前退出了法国市场。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Quad9">Quad9 - Wikipedia</a></li>
<li><a href="https://quad9.net/">Quad9 | A public and free DNS service for a better security ...</a></li>

</ul>
</details>

**社区讨论**: Quad9 的首席技术官提供了详细背景，确认在 11 月 24 日之后可能会使用 geoIP 过滤器阻止法国用户访问，同时承认这种方法并不完美。社区成员对法律状况表示沮丧，一位评论者指出索尼使用 VPN 绕过 geoIP 封锁然后报告 Quad9 不合规的荒谬性，另一位评论者将 DNS 解析器的责任比作因电话簿中列有罪犯号码而惩罚电话簿公司。几位评论者还讨论了 Google、Cloudflare 和 Cisco 如何面临类似的禁令，其中 Cisco 此前已退出法国市场。

**标签**: `#dns`, `#privacy`, `#legal`, `#copyright`, `#internet-infrastructure`

---

<a id="item-4"></a>
## [NVIDIA OpenShell：面向自主 AI 代理集群的安全运行时](https://github.com/NVIDIA/OpenShell) ⭐️ 8.0/10

NVIDIA 发布了 OpenShell，这是一个开源沙箱运行时，通过内核级隔离和声明式 YAML 安全策略在隔离环境中执行自主 AI 代理。0.1.0 版本包含策略验证、凭据保护的服务访问、多租户部署支持，以及 CPU 和 GPU 执行能力。 随着 AI 代理越来越多地自主操作并访问文件、包、API 和凭据，缺乏标准化的沙箱基础设施一直是生态系统中的关键缺口。OpenShell 通过提供专用运行时来填补这一空白，在代理能力和安全约束之间取得平衡，使组织能够大规模部署代理集群，而不会将敏感数据或系统暴露于不受控的访问之下。 OpenShell 使用 policy.yaml 文件以声明方式定义代理可以访问哪些文件、进程、网络端点和凭据，通过内核级隔离而非仅靠容器边界来强制执行。它于 2026 年 6 月在 Computex 上与 Canonical 合作首次为 Ubuntu 预览，并支持在 VPS 基础设施上的沙箱环境中运行 Claude Code 等代理。

hackernews · niemandhier · 10月22日 17:44 · [社区讨论](https://news.ycombinator.com/item?id=50198675)

**背景**: 自主 AI 代理是能够独立执行复杂任务的 AI 系统，通常需要访问文件系统、包管理器、网络 API 和凭据才能发挥作用。沙箱化是将此类代理隔离在受限环境中的实践，通过策略强制执行和监控来限制它们可以执行、访问和传输的内容。随着代理框架的激增，数据泄露、未授权访问和提示注入攻击的风险已使沙箱化成为生产安全的必要条件，而非可选的预防措施。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Nvidia_OpenShell">Nvidia OpenShell</a></li>
<li><a href="https://www.ssdnodes.com/learn/nvidia-openshell-sandbox-agents-on-a-vps">NVIDIA OpenShell : sandbox agents on a VPS · SSD Nodes</a></li>
<li><a href="https://dev.to/imversion_tech/ai-agent-sandboxing-practical-guide-for-production-safety-58p8">AI Agent Sandboxing: Practical Guide for Production Safety</a></li>

</ul>
</details>

**社区讨论**: 社区态度谨慎积极，用户认可 OpenShell 是有价值的管理工具，同时质疑它是否真能解决代理能力与安全之间的根本矛盾。多位评论者提出数据泄露是最难解决的未解问题——即使将网络限制在可信域名，防止代理泄露代码库或敏感数据仍然困难。其他人指出基于容器的代理隔离本应已是标准实践，还有用户报告在独立尝试构建进程审计功能时被 Claude 的安全分类器阻止。

**标签**: `#ai-agents`, `#sandboxing`, `#security`, `#nvidia`, `#infrastructure`

---

<a id="item-5"></a>
## [通过 QEMU 在 Android 设备上运行完整的 iOS 16.5 XNU 内核](https://github.com/oosexgang/hackios-xnu-kernel) ⭐️ 8.0/10

一个名为 hackios-xnu-kernel 的项目展示了通过 QEMU 在 Android 设备上启动并运行完整 iOS 16.5 XNU 内核的能力，支持 POCO X5 Pro 5G 和部分小米机型。该项目以限时研究平台的形式运行，每个会话持续固定秒数后内核返回加载器并输出日志。 将苹果闭源的 XNU 内核移植到通用 Android 硬件上是跨平台仿真领域的一项重大技术突破，表明 iOS 内核级代码可以在非苹果硬件上执行。这可能对安全研究、内核调试以及二手手机市场产生影响，买家在验证设备真伪时需要更加谨慎。 该项目明确定位为研究平台而非日常使用的 ROM，会话在固定时长后自动终止并将内核日志返回给加载器。代码仓库包含 XNU 补丁、EFI 加载器、UEFI 移植、Wi-Fi 支持、QEMU 脚本以及预构建的内核/加载器/UEFI 组件，已在包括 POCO X5 Pro 5G 在内的特定小米设备上完成测试。

hackernews · aghuang · 10月22日 15:26 · [社区讨论](https://news.ycombinator.com/item?id=50196718)

**背景**: XNU 是苹果公司开发的操作系统内核，用于 macOS、iOS、iPadOS、watchOS、visionOS 和 tvOS。它是一个混合内核，源自卡内基梅隆大学开发的 Mach 内核，融合了 4.3BSD 及后来 FreeBSD 的组件，并使用 IOKit 来编写驱动程序。QEMU 是一个免费开源的仿真器，可以通过全系统仿真在一类架构上运行为另一类架构制作的操作系统和程序，在 Android 开发环境中被广泛使用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/XNU_kernel">XNU kernel</a></li>
<li><a href="https://github.com/oosexgang/hackios-xnu-kernel">GitHub - oosexgang/hackios- xnu - kernel · GitHub</a></li>

</ul>
</details>

**社区讨论**: 评论者对这一技术成就表示赞赏，同时指出项目的

**标签**: `#iOS`, `#XNU Kernel`, `#Android`, `#Emulation`, `#QEMU`

---

<a id="item-6"></a>
## [eMudhra 因安全事件退出全球 SSL/TLS 证书业务](https://emudhra.com/en/press-release/emudhra-to-exit-global-ssl-tls-certificate-business) ⭐️ 8.0/10

印度证书颁发机构 eMudhra 宣布将退出全球 SSL/TLS 证书业务，此前一起安全事件引发广泛关注，该事件中 8 个中间 CA 私钥因强度过低而被破解。董事会在此研究员披露漏洞五天后做出该决定，Chrome 等浏览器团队随后对其进行了严厉的技术质询。 证书颁发机构因安全事件退出全球 SSL/TLS 业务，对互联网基础设施和 Web 信任而言是一个重大事件，因为 CA 是安全在线通信的基石。该事件凸显了 CA 生态系统中妥善管理密钥和保持透明度的重要性，一旦失败，可能破坏全球数百万网站和用户的信任。 该事件涉及 8 个中间 CA 私钥，其强度低到可以被破解，引发了对 eMudhra 密钥管理实践及是否符合 WebTrust 审计等行业标准的严重质疑。eMudhra 声称其全球 SSL/TLS 基础设施与其他业务分开运营，且受影响的 CA 未签发任何终端实体证书，但评论者指出任何人都可以从这些被攻破的 CA 签发证书。

hackernews · bo0tzz · 10月22日 13:33 · [社区讨论](https://news.ycombinator.com/item?id=50195110)

**背景**: 证书颁发机构（CA）是签发数字证书的实体，用于验证网站身份并建立加密的 HTTPS 连接，构成 Web 信任的基础。每个 CA 使用私钥对证书进行签名，该私钥必须安全保管并使用足够强度的加密以防止伪造。CA 需接受 WebTrust 等审计，并遵守 CA/Browser Forum 制定的标准，Chrome 和 Firefox 等浏览器厂商作为守门人，决定信任哪些 CA。当 CA 的私钥被泄露或发现强度不足时，攻击者可能伪造任何网站的证书，从而破坏整个信任链。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thehackernews.com/2026/10/emudhra-to-exit-global-ssltls-business.html">eMudhra to Exit Global SSL/TLS Business After 8 Intermediate CA...</a></li>
<li><a href="https://www.coindesk.com/tech/2026/10/21/a-company-that-vouches-for-websites-had-secret-keys-so-weak-that-8-of-them-were-cracked">Internet panics after 8 eMudhra private keys get cracked</a></li>

</ul>
</details>

**社区讨论**: 社区情绪以压倒性的批评为主，评论者嘲讽 eMudhra 缺乏透明度，并将此情况比作连续两年生产有两个前排乘客座位的汽车却无人发现的荒谬类比。一位用户强调了 Chrome 团队通过 Bugzilla 提交的严厉质询，而其他人则指出 eMudhra 声称未签发终端实体证书的说法荒谬，因为任何人都可以从被攻破的 CA 签发证书。

**标签**: `#security`, `#ssl/tls`, `#certificate-authority`, `#web-trust`, `#incident-response`

---

<a id="item-7"></a>
## [Earcut 库在地图多边形三角化中被 Earstrip 超越](https://globus.software/blog/2026/10/16/cutting-map-polygons/) ⭐️ 8.0/10

一个名为 Earstrip 的全新三角化库仅需 489 毫秒即可处理 370 万个地图多边形，通过优化算法显著超越了广泛使用的 earcut 库。该库编译为 WebAssembly（WASM），在浏览器和 GIS 环境中实现了高性能的多边形三角化。 多边形三角化是计算几何和 GIS 中的基础操作，直接影响交互式地图和地理空间可视化的渲染性能。相对于驱动 Mapbox GL JS 等主流地图库的 earcut 的大幅提速，可能实现大规模复杂地理数据的更流畅实时渲染。 现有库 earcut 是一种 2D 耳裁剪算法，为了在 JavaScript 环境中保持较小的包体积（压缩后 4.1KB），刻意放弃了一些优化。Earcut 似乎以更大的二进制体积（通过 WASM）换取了显著更快的执行速度，这引发了关于包体积与原始计算速度之间权衡的讨论。

hackernews · molind · 10月22日 09:31 · [社区讨论](https://news.ycombinator.com/item?id=50193170)

**背景**: 多边形三角化是将一个多边形分解为一组互不重叠的三角形的过程，这些三角形的并集等于原始多边形，这是计算几何中的核心问题。耳裁剪算法通过迭代识别并移除

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/mapbox/earcut">GitHub - mapbox/ earcut : The fastest and smallest JavaScript polygon...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Polygon_triangulation">Polygon triangulation - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 讨论中，earcut 作者（mourner）认可了 Earstrip 的性能，并指出 earcut 刻意牺牲了一些优化以保持 4.1KB 的小包体积，同时询问了 Earstrip 的 WASM 二进制体积。其他评论者提出了三角形质量问题（微小三角形可能导致渲染问题），比较了 Seidel 梯形方法和约束 Delaunay 三角化等方法，并提到了 Shewchuk 的 Triangle 库作为

**标签**: `#computational-geometry`, `#triangulation`, `#performance-optimization`, `#gis`, `#wasm`

---

<a id="item-8"></a>
## [Anthropic 将 Agent Skills 标准捐赠给 Agentic AI Foundation](https://simonwillison.net/2026/Oct/22/donating-agent-skills/) ⭐️ 8.0/10

Anthropic 宣布将 Agent Skills 开放标准捐赠给 Linux Foundation 旗下的 Agentic AI Foundation（AAIF），该基金会由 Anthropic 与 Block 和 OpenAI 共同创立。此前 MCP（Model Context Protocol）也已捐赠给同一基金会，此举进一步将关键 AI Agent 标准整合至中立治理机构之下。 此举标志着行业持续向关键 AI Agent 基础设施的中立治理方向转变，确保生态系统内的互操作性和社区驱动的开发。通过将 Agent Skills 与 MCP 一并置于 AAIF 之下，行业获得了一个统一的、开放的 AI Agent 标准机构，有助于减少标准碎片化和供应商锁定。 Agent Skills 是一种用于扩展 AI Agent 能力的轻量级开放格式，一个 skill 本质上是一个包含 SKILL.md 文件的文件夹，其中包含元数据和指令，以及可选的脚本和资源。Simon Willison 在 2025 年 12 月 Anthropic 首次宣布 Agent Skills 为开放标准时就预测了此次捐赠，他还特别使用自己的 datasette-mcp 插件检索到了此前关于该话题的博客文章。

rss · Simon Willison · 10月22日 18:09

**背景**: Agentic AI Foundation（AAIF）是 Linux Foundation 旗下的中立基金会，于 2025 年 12 月由 Anthropic、Block 和 OpenAI 共同创立，旨在治理 AI Agent 系统的开放基础设施。MCP（Model Context Protocol）由 Anthropic 于 2024 年 11 月推出，是连接 AI 应用与外部数据源和工具的开放标准，也是首批捐赠给 AAIF 的重要标准之一。Agent Skills 最初由 Anthropic 开发，是一种将专业知识和工作流打包供 Agent 执行的格式，与 MCP 的连接层形成互补。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://agentskills.io/home">Agent Skills Overview - Agent Skills</a></li>
<li><a href="https://aaif.io/">Agentic AI Foundation ( AAIF ) - Open Standards for Agentic AI</a></li>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol - Wikipedia</a></li>

</ul>
</details>

**标签**: `#agentic-ai`, `#anthropic`, `#open-standards`, `#linux-foundation`, `#agent-skills`

---

<a id="item-9"></a>
## [Carbon-X：支持 DNA 与文本联合分析的开放 14.8B 模型](https://www.reddit.com/r/MachineLearning/comments/1xchayq/carbonx_is_an_open_148b_model_trained_jointly_on/) ⭐️ 8.0/10

Carbon-X 是一个新发布的开源 14.8B 参数 decoder-only 模型，可在聊天界面中接收原始 DNA 序列并用英语回答，使用共享的 6-mer token 流在 302B token 上进行 DNA 与文本联合训练。该模型采用 Apache 2.0 许可证发布，在五项 DNA 基准测试中平均达到 66.7%，可在单张 80GB GPU 上以 bfloat16 精度本地运行。 该模型将基因组序列分析与自然语言处理相结合，使研究人员能够以对话格式直接查询原始 DNA 并获得英语解释，有望简化基因组研究流程。其可在单张 GPU 上本地运行的能力，使其对于因隐私或法规限制而无法上传至云端的敏感基因组数据分析尤为重要。 Carbon-X 采用 6-mer 分词方式，将原始 DNA 核苷酸字符串分割为重叠的六字符子序列，并为 DNA 和文本共享同一 token 流。该模型尚未经过临床验证，模型卡片明确指出，模体查找或限制性位点检测等精确序列操作仍应由传统代码而非模型来完成。

reddit · r/MachineLearning · /u/jatingargiitk · 10月22日 12:32

**背景**: DNA 语言模型在处理前需要将原始核苷酸字符串（如"GATTACA"）转换为数值 token，6-mer 分词将序列分割为重叠的六核苷酸子序列，这一策略已被 DNABERT 等模型采用。Decoder-only Transformer 架构由 GPT 系列推广，采用因果自注意力机制，已成为生成式语言模型的标准蓝图。bfloat16（Brain Float 16）精度格式通过将每个参数从 32 位减少至 16 位来降低内存占用，使大型模型在推理时能够在更少的 GPU 上运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2507.18570">[2507.18570] Hybrid Tokenization Strategy for DNA Language ... Tokenization - DNALLM Documentation Tokenization & Architecture - Generative AI for Biomedical ... Taykhoom/DNABERT-6mer · Hugging Face Per-base, BPE, and 6-mer on the same DNA sequence - a Hugging ... k-mers, tokenization, and sequence windows | Hermon DNA and ...</a></li>
<li><a href="https://blog.algomaster.io/p/transformer-architecture">A deep dive into the Transformer architecture</a></li>
<li><a href="https://deepwiki.com/ogunerkutay/huggingface-llm-examples/4.1-mixed-precision-inference">Mixed Precision Inference | DeepWiki</a></li>

</ul>
</details>

**标签**: `#genomics`, `#large-language-models`, `#open-source`, `#bioinformatics`, `#machine-learning`

---

<a id="item-10"></a>
## [Anthropic 发布 Claude API 2026-10-21 新版本，移除采样参数](https://x.com/ClaudeDevs/status/2113013247209021918) ⭐️ 8.0/10

Anthropic 发布了 Claude API 版本 2026-10-21，这是自 2023-06-01 beta 版本以来的首次正式版本更新，该版本完全移除了 temperature、top_p 和 top_k 参数。继续传入这些参数将返回 400 错误，SDK 和 ant CLI 已默认切换至新版本，认证头也改为 Authorization: Bearer。 这是一项重大的破坏性变更，直接影响了所有使用 Claude API 的开发者，因为被移除的参数是用于控制输出随机性和创造力的核心采样控制参数。从 beta 版本转向正式版本以及认证头的变更，标志着平台的重大演进，要求开发者更新其集成代码。 旧版本 2023-06-01 尚未被弃用，允许开发者在过渡期间继续使用。ant CLI 是 Anthropic 官方的命令行工具，用于从终端调用 Claude API 资源，它并非 Python 或 TypeScript SDK 的替代品。

telegram · zaihuapd · 10月22日 03:54

**背景**: Temperature、top_p 和 top_k 是 LLM API 中的采样参数，用于控制生成文本的随机性和多样性。Temperature 调整概率分布的锐度，top_p（核采样）将 token 选择限制在累积概率阈值内，top_k 则将选择限制在最可能的前 k 个 token 中。这些参数几乎是所有 LLM API 的标准配置，包括 OpenAI 的 GPT 系列和 Anthropic 的 Claude，允许开发者针对不同用例微调输出行为。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://amitray.com/llm-parameters-temperature-top-p-top-k-guide/">LLM Temperature, Top-P, Top-K & 11 Core Parameters: The ...</a></li>
<li><a href="https://agentpedia.codes/blog/claude-api-ant-cli-guide">Claude Platform ant CLI : Official Developer Guide</a></li>
<li><a href="https://ai-tldr.dev/learn/llm-apis/api-basics/sampling-parameters-explained/">Temperature, Top-P, Top-K: LLM Sampling Parameters | AI/TLDR</a></li>

</ul>
</details>

**标签**: `#Anthropic`, `#Claude API`, `#Breaking Changes`, `#AI/ML`, `#Developer Tools`

---

<a id="item-11"></a>
## [澳洲法院裁定苹果须向第三方应用商店开放 iPhone](https://9to5mac.com/2026/10/21/apple-must-open-iphone-to-alternative-app-stores-in-australia-after-epic-games-ruling/) ⭐️ 8.0/10

澳大利亚联邦法院裁定，苹果须从 2027 年 3 月 1 日起允许澳区 iPhone 用户通过第三方应用商店和网站安装应用，并开放替代支付方式与外部支付链接。同时，法院命令 Fortnite 立即重返澳区 App Store。 这项裁决迫使苹果在澳大利亚打破其封闭花园式的应用分发模式，延续了由欧盟《数字市场法》引领的全球监管趋势。此举对应用开发者、支付处理商以及苹果的服务收入产生重大影响，Epic 诉苹果案持续在全球范围内重塑应用商店生态。 法院认定苹果在 iOS 应用分发和支付市场具有实质性市场力量，其限制竞争的行为违反了澳大利亚竞争法。苹果表示将提起上诉并申请暂缓执行，这意味着实际实施时间表可能因上诉结果而发生变化。

telegram · zaihuapd · 10月22日 06:54

**背景**: Epic Games 于 2020 年 8 月起诉苹果，指控苹果通过禁止第三方应用商店和替代支付方式，在 App Store 运营中构成垄断。该诉讼已跨越包括美国和澳大利亚在内的多个司法管辖区，各国法院和监管机构日益加强对苹果控制 iOS 应用分发的审查。欧盟《数字市场法》已迫使苹果在欧洲允许第三方应用商店和侧载，为先例的建立奠定了基础，其他地区也开始效仿。苹果一贯主张其封闭生态系统对安全性和用户隐私至关重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Epic_Games_v._Apple">Epic Games v. Apple - Wikipedia</a></li>
<li><a href="https://howmobile.net/ios/ios-sideloading-guide">iOS Sideloading Guide 2026 — Every Method That Actually Works</a></li>

</ul>
</details>

**标签**: `#antitrust`, `#apple`, `#app-store`, `#epic-games`, `#regulation`

---

<a id="item-12"></a>
## [333 个被植入后门的 Tor 出口节点被标记下线](https://kaba.cx/posts/20261020_Tor/) ⭐️ 8.0/10

一名 Tor 运营者扫描了约 3000 个出口中继，发现其中 333 个感染了 Ebury 后门，该后门可将 22 端口的 SSH 连接劫持至 12 台拦截服务器以窃取凭据。这些节点于 10 月 4 日被标记为 BadExit，次日全部下线。 此次事件表明约 10% 的 Tor 出口节点被攻陷，动摇了 Tor 网络隐私保障所依赖的信任模型。它凸显了自 2009 年以来活跃至今、已感染数十万台 Linux 服务器的 Ebury 僵尸网络对匿名基础设施的持续威胁。 攻击者最早于今年 8 月就已入侵这些服务器，并屏蔽了部分端口以专门收集未加密的邮件流量。具体入侵途径尚不明确，Ebury 恶意软件通过修改合法 OpenSSH 程序所使用的共享库来窃取凭据。

telegram · zaihuapd · 10月22日 14:52

**背景**: Tor 出口中继是 Tor 线路中连接用户与目标网站的最终节点，这意味着它们可以观察到离开网络的未加密流量。BadExit 标志是 Tor 项目用于标记配置错误或恶意中继的机制，指示 Tor 网络避免通过这些节点路由流量。Ebury 是由 Windigo 组织开发的长期活跃的 OpenSSH 后门和凭据窃取程序，主要针对 Linux 服务器和容器主机。根据 ESET 于 2024 年发布的研究，Ebury 僵尸网络自 2009 年以来已感染近 40 万台 Linux 服务器，截至 2023 年底仍有约 10 万台处于被控状态。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://attack.mitre.org/software/S0377/">Ebury, Software S0377 | MITRE ATT&CK®</a></li>
<li><a href="https://www.eset.com/us/about/newsroom/press-releases/eset-research-ebury-botnet-alive-growing/">ESET Research: Ebury botnet alive & growing; 400k Linux ...</a></li>
<li><a href="https://support.torproject.org/relay-operators/">Relay Operators | Tor Project | Support</a></li>

</ul>
</details>

**标签**: `#tor`, `#security`, `#malware`, `#privacy`, `#botnet`

---

<a id="item-13"></a>
## [禁运 Nvidia B300 芯片现身中国国有网络](https://theinference.org/article/china-s-state-money-bought-banned-nvidia-b300-servers-then-redacted-the-receipts) ⭐️ 8.0/10

中国国资控股的半导体租赁集团为 AI 公司荣耀视图科技融资购入 32 台搭载 Nvidia B300 芯片的华硕服务器，此交易属于总额超 30 亿元的 700 余台服务器采购计划的一部分。备案文件引发关注后，该租赁集团重新提交文件并抹去了硬件描述，Nvidia 和华硕均已展开调查。 此举构成对美国出口管制的重大潜在违规，因为 B300 属于美国最严出口管制层级，对华基本禁运。国资背景实体的参与、交易规模之大以及蓄意抹除记录的行为，引发了严重的地缘政治和合规隐患，可能加剧中美技术紧张局势。 这些服务器计划部署于中国移动宁夏枢纽，该枢纽位于中卫，是中国算力网络的重要组成部分。B300 是 Nvidia 下一代 AI GPU，据报道 TDP 达 1400W，AI 算力较前代提升约 50%，且 Nvidia 为此代芯片重新设计了整个供应链策略。

telegram · zaihuapd · 10月22日 15:22

**背景**: 2025 年 1 月，美国商务部工业与安全局（BIS）发布临时最终规则，建立了三级 AI 芯片出口管制框架，按盟友关系对各国分级，并严格限制中国获取先进半导体。B300 芯片属于该框架中最严格的管制层级，基本上禁止对华出口。中国移动宁夏枢纽位于中卫，是一个大规模数据中心园区，结合分期建设与智能算力基础设施，是中国算力网络和西部大开发战略的组成部分。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tomshardware.com/tech-industry/artificial-intelligence/nvidias-next-gen-b300-gpus-have-1-400w-tdp-deliver-50-percent-more-ai-horsepower-report">Nvidia 's next-gen B 300 GPUs have 1,400W TDP... | Tom's Hardware</a></li>
<li><a href="https://www.stblaw.com/about-us/publications/view/2025/01/15/bis-announces-worldwide-export-controls-on-advanced-chips-and-ai-models">BIS Announces Worldwide Export Controls on Advanced Chips and ...</a></li>
<li><a href="https://www.datacenters.com/china-mobile-international-ltd-ningxia-zhongwei">China Mobile International Ltd: Ningxia Zhongwei Data Center</a></li>

</ul>
</details>

**标签**: `#Nvidia`, `#Export Controls`, `#Geopolitics`, `#AI Chips`, `#Hardware`

---
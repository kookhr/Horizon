---
layout: default
title: "Horizon Summary: 2026-10-23 (EN)"
date: 2026-10-23
lang: en
---

> From 44 items, 13 important content pieces were selected

---

1. [Nintendo Switch 2 Jailbroken Using LLMs and Hardware KVMs](#item-1) ⭐️ 9.0/10
2. [Oracle Issues Critical Security Alert for Java SE JSSE Vulnerability](#item-2) ⭐️ 9.0/10
3. [Quad9 DNS Resolver to Exit France Over Piracy Blocking Court Orders](#item-3) ⭐️ 8.0/10
4. [NVIDIA OpenShell: A Secure Runtime for Autonomous AI Agent Fleets](#item-4) ⭐️ 8.0/10
5. [Full iOS 16.5 XNU Kernel Runs on Android Devices via QEMU](#item-5) ⭐️ 8.0/10
6. [eMudhra to Exit Global SSL/TLS Certificate Business After Security Incident](#item-6) ⭐️ 8.0/10
7. [Earcut library outperformed by Earstrip for map polygon triangulation](#item-7) ⭐️ 8.0/10
8. [Anthropic Donates Agent Skills Standard to Agentic AI Foundation](#item-8) ⭐️ 8.0/10
9. [Carbon-X: Open 14.8B Model for Joint DNA-Text Analysis](#item-9) ⭐️ 8.0/10
10. [Anthropic Releases Claude API Version 2026-10-21, Removes Sampling Parameters](#item-10) ⭐️ 8.0/10
11. [Australian Court Rules Apple Must Open iPhone to Third-Party App Stores](#item-11) ⭐️ 8.0/10
12. [333 Backdoored Tor Exit Relays Delisted and Shut Down](#item-12) ⭐️ 8.0/10
13. [Banned Nvidia B300 Chips Found in Chinese State-Backed Networks](#item-13) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Nintendo Switch 2 Jailbroken Using LLMs and Hardware KVMs](https://pepsipu.com/blog/2026-10-switch2-jailbreak-ns2jb/) ⭐️ 9.0/10

Security researcher pepsipu has released details of "ns2jb," a software-only, tethered exploit for the Nintendo Switch 2 that achieves decrypted filesystem read/write access on the latest 23.0.1 firmware. The breakthrough notably leveraged OpenAI's Codex LLM combined with JetKVM hardware to automate vulnerability research, including a Bluetooth light switch device to physically press the console's power button during crashes. This is the first reported jailbreak of the Nintendo Switch 2, potentially enabling game dumps and console exclusives to run on arbitrary hardware, which represents a worst-case scenario for Nintendo's platform security. Beyond console gaming, the methodology of giving LLMs "arms and eyes" via KVMs to autonomously conduct hardware security research signals a new paradigm in automated vulnerability discovery. The exploit is a tethered userland exploit, meaning it requires a connection to a host computer and must be re-triggered every time the Switch 2 boots, as it does not achieve persistent kernel-level access. The method exploits backward compatibility with a specific Switch 1 game to gain initial access, and the automated setup used a SwitchBot Bot (a Bluetooth-enabled physical actuator) to press the power button when the console crashed during testing.

hackernews · ledoge · Oct 22, 08:01 · [Discussion](https://news.ycombinator.com/item?id=50192536)

**Background**: Jailbreaking a game console involves exploiting software or hardware vulnerabilities to bypass the manufacturer's restrictions, allowing users to run homebrew applications, mod games, or dump game files. The Nintendo Switch 2, like its predecessor, employs encrypted filesystems and signed code to prevent unauthorized access, meaning a successful exploit must decrypt these protections to achieve meaningful read/write access. "Userland" access refers to gaining execution rights in the unprivileged user space, which is less powerful than kernel access but still sufficient for running custom code and reverse engineering. The use of LLMs like Codex in security research is an emerging trend where AI agents are given tools to interact with systems, potentially automating repetitive tasks in vulnerability discovery.

<details><summary>References</summary>
<ul>
<li><a href="https://arstechnica.com/gaming/2026/10/switch-2-jailbreak-gives-hackers-new-ways-to-run-homebrew-and-mod-games/">Switch 2 security takes a hit as hackers unlock homebrew access</a></li>
<li><a href="https://kotaku.com/nintendo-switch-2-jailbreak-hack-exploit-piracy-homebrew-emulation-modding-2000748784">The Switch 2 Has Been Jailbroken For The First Time - Kotaku</a></li>
<li><a href="https://en.gamegpu.com/news/zhelezo/konsol-nintendo-switch-2-vzlomali-cherez-uyazvimost-smilebasic">The Nintendo Switch 2 console was hacked using a SmileBASIC ...</a></li>

</ul>
</details>

**Discussion**: Commenters expressed amazement at the technical ingenuity, particularly the Rube Goldberg-esque use of a Bluetooth light switch to press the power button, with one user dubbing it a "Switch SwitchBot Bot." Several discussions focused on the broader implications of giving LLMs physical control via KVMs for automated security research, while others noted that the author's existing security expertise was likely a larger factor than the AI itself, and one user questioned how the author bypassed Codex's safety restrictions on vulnerability research.

**Tags**: `#security`, `#hardware-hacking`, `#nintendo-switch`, `#jailbreaking`, `#llm-agents`

---

<a id="item-2"></a>
## [Oracle Issues Critical Security Alert for Java SE JSSE Vulnerability](https://www.oracle.com/security-alerts/alert-cve-2026-91403.html) ⭐️ 9.0/10

Oracle has issued a critical security alert for CVE-2026-91403, a high-severity remote code execution vulnerability in Java SE's JSSE component with a CVSS score of 9.1. The flaw affects multiple Java SE versions including 8u511, 11.0.33, 17.0.21, 21.0.13, 25.0.5, 27.0.1, and several GraalVM releases, and Oracle has released patches urging immediate upgrades. This vulnerability is exceptionally dangerous because it allows unauthenticated remote attackers to exploit the flaw over the network, potentially compromising the confidentiality and integrity of critical data. Any organization running affected Java SE versions is at risk, making immediate patching a top priority for system administrators and developers across the industry. The vulnerability resides in the JSSE (Java Secure Socket Extension) component, which handles TLS and SSL protocols for secure network communications in Java. Attackers can exploit this flaw without authentication, and Oracle has confirmed that both data confidentiality and integrity are at risk. Patches are available for all affected versions, including the GraalVM distribution.

telegram · zaihuapd · Oct 22, 12:30

**Background**: The Java Secure Socket Extension (JSSE) is a core Java API that enables secure Internet communications by providing a framework and implementation for TLS and DTLS protocols within the Java Runtime Environment. It handles critical functions such as data encryption, server authentication, and message integrity. GraalVM is a high-performance JDK distribution developed by Oracle Labs that features both just-in-time (JIT) and ahead-of-time (AOT) compilation capabilities. A CVSS score of 9.1 indicates a critical severity level, meaning the vulnerability is easily exploitable and can cause significant impact to affected systems.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.oracle.com/en/java/javase/11/security/java-secure-socket-extension-jsse-reference-guide.html">Java Secure Socket Extension (JSSE) Reference Guide</a></li>
<li><a href="https://en.wikipedia.org/wiki/GraalVM">GraalVM</a></li>

</ul>
</details>

**Tags**: `#security`, `#java`, `#oracle`, `#vulnerability`, `#cve`

---

<a id="item-3"></a>
## [Quad9 DNS Resolver to Exit France Over Piracy Blocking Court Orders](https://quad9.net/news/blog/au-revoir-france/) ⭐️ 8.0/10

Quad9, a privacy-focused public DNS resolver operated by a Swiss foundation, announced it will shut down its DNS resolution services in France after November 24, following court orders requiring it to block access to piracy sites. The company argues that selectively blocking specific domains while maintaining its privacy guarantees is technically infeasible, and that it was fined for contempt of court after Sony Music used a VPN to circumvent geoIP-based blocking. This sets a significant precedent for internet infrastructure and jurisdictional conflicts, as a major DNS resolver is choosing to exit an entire country rather than compromise its privacy guarantees or comply with technically infeasible blocking mandates. It highlights the growing tension between copyright enforcement through DNS-level blocking and the privacy and security commitments of DNS providers, with Google and Cloudflare having already been forced to comply with similar French injunctions. Quad9's CTO confirmed that geoIP filters will likely be used to block French users from accessing their services after November 24, while acknowledging that geoIP blocking is imperfect. The legal pressure came from Sony Music Entertainment GmbH, which used a VPN to access blocked content from Germany and then reported Quad9 for noncompliance, resulting in contempt of court fines; Canal+ has also been obtaining similar web-blocking injunctions against DNS resolvers in France.

hackernews · farrokhi · Oct 22, 14:32 · [Discussion](https://news.ycombinator.com/item?id=50195959)

**Background**: Quad9 is a free, global public recursive DNS resolver operated by the Quad9 Foundation, a Swiss non-profit headquartered in Zürich, that blocks access to domains associated with malware and phishing. DNS resolvers translate domain names into IP addresses, and some jurisdictions have begun ordering resolvers to block access to specific domains, such as piracy sites, as a copyright enforcement mechanism. However, privacy-focused resolvers like Quad9 do not log user queries, making selective domain blocking technically challenging without compromising their privacy guarantees. Previous targets of similar French web-blocking injunctions include Google, Cloudflare, and Cisco, with the latter having exited the French market two years ago.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Quad9">Quad9 - Wikipedia</a></li>
<li><a href="https://quad9.net/">Quad9 | A public and free DNS service for a better security ...</a></li>

</ul>
</details>

**Discussion**: Quad9's CTO provided detailed context, confirming that geoIP filters will likely block French users after November 24 while acknowledging the imperfection of this approach. Community members expressed frustration with the legal situation, with one commenter noting the absurdity of Sony using a VPN to circumvent geoIP blocking and then reporting Quad9 for noncompliance, and another comparing DNS resolver liability to punishing a phone book company for listing a criminal's number. Several commenters also discussed how Google, Cloudflare, and Cisco had faced similar injunctions, with Cisco having previously exited the French market.

**Tags**: `#dns`, `#privacy`, `#legal`, `#copyright`, `#internet-infrastructure`

---

<a id="item-4"></a>
## [NVIDIA OpenShell: A Secure Runtime for Autonomous AI Agent Fleets](https://github.com/NVIDIA/OpenShell) ⭐️ 8.0/10

NVIDIA has released OpenShell, an open-source sandbox runtime that executes autonomous AI agents in isolated environments with kernel-level isolation and declarative YAML-based security policies. Version 0.1.0 includes policy verification, credential-protected service access, multi-tenant deployment support, and both CPU and GPU execution capabilities. As AI agents increasingly operate autonomously with access to files, packages, APIs, and credentials, the lack of standardized sandboxing infrastructure has been a critical gap in the ecosystem. OpenShell addresses this by providing a purpose-built runtime that balances agent capability with security constraints, enabling organizations to deploy agent fleets at scale without exposing sensitive data or systems to uncontrolled access. OpenShell uses a policy.yaml file to declaratively define which files, processes, network endpoints, and credentials an agent can access, enforced through kernel-level isolation rather than mere container boundaries. It was previewed for Ubuntu at Computex in June 2026 in collaboration with Canonical, and supports running agents like Claude Code inside sandboxed environments on VPS infrastructure.

hackernews · niemandhier · Oct 22, 17:44 · [Discussion](https://news.ycombinator.com/item?id=50198675)

**Background**: Autonomous AI agents are AI systems that perform complex tasks independently, often requiring access to filesystems, package managers, network APIs, and credentials to be useful. Sandboxing is the practice of isolating such agents in restricted environments with policy enforcement and monitoring to limit what they can execute, access, and transmit. As agent frameworks proliferate, the risk of data exfiltration, unauthorized access, and prompt injection attacks has made sandboxing a production safety requirement rather than an optional precaution.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Nvidia_OpenShell">Nvidia OpenShell</a></li>
<li><a href="https://www.ssdnodes.com/learn/nvidia-openshell-sandbox-agents-on-a-vps">NVIDIA OpenShell : sandbox agents on a VPS · SSD Nodes</a></li>
<li><a href="https://dev.to/imversion_tech/ai-agent-sandboxing-practical-guide-for-production-safety-58p8">AI Agent Sandboxing: Practical Guide for Production Safety</a></li>

</ul>
</details>

**Discussion**: Community sentiment is cautiously positive, with users acknowledging OpenShell as a valuable management tool while questioning whether it can truly resolve the fundamental tension between agent capability and security. Several commenters raised data exfiltration as the hardest unsolved problem — even with network restrictions to trusted domains, preventing agents from leaking codebases or sensitive data remains difficult. Others noted that container-based agent isolation should already be standard practice, and one user reported being blocked by Claude's safety classifier when attempting to build process auditing features independently.

**Tags**: `#ai-agents`, `#sandboxing`, `#security`, `#nvidia`, `#infrastructure`

---

<a id="item-5"></a>
## [Full iOS 16.5 XNU Kernel Runs on Android Devices via QEMU](https://github.com/oosexgang/hackios-xnu-kernel) ⭐️ 8.0/10

A project called hackios-xnu-kernel demonstrates the ability to boot and run the full iOS 16.5 XNU kernel on Android devices using QEMU, with support for devices like the POCO X5 Pro 5G and certain Xiaomi models. The project functions as a time-limited research bench where each session lasts a set number of seconds before the kernel returns to the loader and outputs its log. Porting Apple's closed-source XNU kernel to commodity Android hardware is a significant technical achievement in cross-platform emulation, demonstrating that iOS kernel-level code can execute on non-Apple hardware. This could have implications for security research, kernel debugging, and the used phone market, where buyers may need to be more vigilant about verifying device authenticity. The project is explicitly a research bench, not a daily-use ROM, with sessions that automatically terminate after a fixed duration and return kernel logs to the loader. The repository includes XNU patches, an EFI loader, a UEFI port, Wi-Fi support, QEMU scripts, and prebuilt kernel/loader/UEFI components, and has been tested on specific Xiaomi devices including the POCO X5 Pro 5G.

hackernews · aghuang · Oct 22, 15:26 · [Discussion](https://news.ycombinator.com/item?id=50196718)

**Background**: XNU is the operating system kernel developed by Apple for use in macOS, iOS, iPadOS, watchOS, visionOS, and tvOS. It is a hybrid kernel derived from the Mach kernel developed at Carnegie Mellon University, incorporating components from 4.3BSD and later FreeBSD, along with IOKit for writing drivers. QEMU is a free and open-source emulator that can run operating systems and programs made for one architecture on another through full system emulation, and it is widely used in Android development environments.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/XNU_kernel">XNU kernel</a></li>
<li><a href="https://github.com/oosexgang/hackios-xnu-kernel">GitHub - oosexgang/hackios- xnu - kernel · GitHub</a></li>

</ul>
</details>

**Discussion**: Commenters praised the technical achievement while noting the project's research-bench nature, with one speculating the time-limited sessions might be a safeguard. Concerns were raised about the used phone market, where replica devices running customized Android to look like iOS already exist, making it harder to verify authenticity. Some expressed diminished interest in running iOS on non-Apple hardware due to the OS's current state, while others hoped similar techniques could be applied to unlock features gated by market segmentation in other firmware ecosystems like Garmin.

**Tags**: `#iOS`, `#XNU Kernel`, `#Android`, `#Emulation`, `#QEMU`

---

<a id="item-6"></a>
## [eMudhra to Exit Global SSL/TLS Certificate Business After Security Incident](https://emudhra.com/en/press-release/emudhra-to-exit-global-ssl-tls-certificate-business) ⭐️ 8.0/10

Indian Certificate Authority eMudhra announced it will exit the global SSL/TLS certificate business following intense scrutiny over a security incident where 8 intermediate CA private keys were found to be weak enough to be cracked. The board's decision came five days after a researcher disclosed the vulnerability, prompting brutal technical questioning from browser teams like Chrome. A Certificate Authority exiting the global SSL/TLS business due to a security incident is a significant event for internet infrastructure and web trust, as CAs are the backbone of secure online communication. The incident highlights the critical importance of proper key management and transparency in the CA ecosystem, where failures can undermine trust for millions of websites and users globally. The incident involved 8 intermediate CA private keys that were so weak they could be cracked, raising serious questions about eMudhra's key management practices and compliance with industry standards like WebTrust audits. eMudhra claimed its global SSL/TLS infrastructure runs separately from its other operations and that no end-entity certificates were issued from the affected CAs, but commenters noted that anyone could have issued certificates from those compromised CAs.

hackernews · bo0tzz · Oct 22, 13:33 · [Discussion](https://news.ycombinator.com/item?id=50195110)

**Background**: Certificate Authorities (CAs) are entities that issue digital certificates used to verify website identities and enable encrypted HTTPS connections, forming the foundation of web trust. Each CA signs its certificates with a private key, which must be kept secure and use sufficiently strong encryption to prevent forgery. CAs are subject to audits like WebTrust and must comply with standards set by the CA/Browser Forum, with browser vendors like Chrome and Firefox acting as gatekeepers by deciding which CAs are trusted. When a CA's private keys are compromised or found to be weak, it can allow attackers to forge certificates for any website, breaking the entire chain of trust.

<details><summary>References</summary>
<ul>
<li><a href="https://thehackernews.com/2026/10/emudhra-to-exit-global-ssltls-business.html">eMudhra to Exit Global SSL/TLS Business After 8 Intermediate CA...</a></li>
<li><a href="https://www.coindesk.com/tech/2026/10/21/a-company-that-vouches-for-websites-had-secret-keys-so-weak-that-8-of-them-were-cracked">Internet panics after 8 eMudhra private keys get cracked</a></li>

</ul>
</details>

**Discussion**: Community sentiment was overwhelmingly critical, with commenters mocking eMudhra's lack of transparency and comparing the situation to absurd analogies like building cars with two passenger seats for two years without anyone noticing. One user highlighted the brutal question battery submitted by the Chrome team via Bugzilla, while others pointed out the ridiculousness of eMudhra's claim that no end-entity certificates were issued, noting that anyone could have issued certificates from the compromised CAs.

**Tags**: `#security`, `#ssl/tls`, `#certificate-authority`, `#web-trust`, `#incident-response`

---

<a id="item-7"></a>
## [Earcut library outperformed by Earstrip for map polygon triangulation](https://globus.software/blog/2026/10/16/cutting-map-polygons/) ⭐️ 8.0/10

A new triangulation library called Earstrip processes 3.7 million map polygons in just 489 milliseconds, significantly outperforming the widely-used earcut library through optimized algorithms. The library is compiled to WebAssembly (WASM), enabling high-performance polygon triangulation in browser and GIS environments. Polygon triangulation is a fundamental operation in computational geometry and GIS, directly affecting rendering performance for interactive maps and geospatial visualizations. A substantial speedup over earcut — which powers major mapping libraries like Mapbox GL JS — could enable smoother real-time rendering of complex geographic data at scale. Earcut, the incumbent library, is a 2D ear-clipping algorithm that deliberately rejects some optimizations to keep its bundle size small (4.1KB minified/gzipped) for JavaScript environments. Earstrip appears to trade larger binary size (via WASM) for significantly faster execution, raising questions about the tradeoff between bundle size and raw computational speed.

hackernews · molind · Oct 22, 09:31 · [Discussion](https://news.ycombinator.com/item?id=50193170)

**Background**: Polygon triangulation is the process of decomposing a polygon into a set of non-overlapping triangles whose union equals the original polygon, a core problem in computational geometry. The ear clipping algorithm works by iteratively identifying and removing 'ears' — triangles formed by three consecutive vertices — until the entire polygon is triangulated. Alternative approaches include Seidel's trapezoidal method, which achieves O(n log*n) time complexity and handles holes naturally, and constrained Delaunay triangulation, which produces higher-quality triangles. Triangulation is essential for rendering because GPUs process geometry as triangles, making it a critical step in converting vector map data into renderable graphics.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/mapbox/earcut">GitHub - mapbox/ earcut : The fastest and smallest JavaScript polygon...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Polygon_triangulation">Polygon triangulation - Wikipedia</a></li>

</ul>
</details>

**Discussion**: The discussion features the earcut author (mourner) acknowledging Earstrip's performance and noting that earcut deliberately sacrifices some optimizations to maintain a small 4.1KB bundle size, while asking about Earstrip's WASM binary size. Other commenters raise questions about triangle quality (tiny triangles potentially causing rendering issues), compare approaches like Seidel's trapezoidal method and constrained Delaunay triangulation, and reference foundational tools like Shewchuk's Triangle library as the 'mother of all triangulators.'

**Tags**: `#computational-geometry`, `#triangulation`, `#performance-optimization`, `#gis`, `#wasm`

---

<a id="item-8"></a>
## [Anthropic Donates Agent Skills Standard to Agentic AI Foundation](https://simonwillison.net/2026/Oct/22/donating-agent-skills/) ⭐️ 8.0/10

Anthropic announced it is donating the Agent Skills open standard to the Agentic AI Foundation (AAIF) under the Linux Foundation, which it co-founded with Block and OpenAI. This follows the earlier donation of the Model Context Protocol (MCP) to the same foundation, consolidating key agentic AI standards under vendor-neutral governance. This move signals a continued industry shift toward vendor-neutral governance of critical AI agent infrastructure, ensuring interoperability and community-driven development across the ecosystem. By placing Agent Skills alongside MCP under the AAIF, the industry gains a unified, open standards body for agentic AI that reduces fragmentation and vendor lock-in. Agent Skills is a lightweight, open format for extending AI agent capabilities, where a skill is essentially a folder containing a SKILL.md file with metadata and instructions, along with optional scripts and resources. Simon Willison had predicted this donation in December 2025 when Anthropic first declared Agent Skills an open standard, and notably used his own datasette-mcp plugin to retrieve his earlier blog post on the topic.

rss · Simon Willison · Oct 22, 18:09

**Background**: The Agentic AI Foundation (AAIF) is a vendor-neutral foundation under the Linux Foundation, established in December 2025 by Anthropic, Block, and OpenAI to govern open infrastructure for AI agent systems. The Model Context Protocol (MCP), introduced by Anthropic in November 2024, is an open standard for connecting AI applications with external data sources and tools, and was one of the first major standards donated to the AAIF. Agent Skills, originally developed by Anthropic, is a format for packaging specialized knowledge and workflows that agents can execute, complementing MCP's connectivity layer.

<details><summary>References</summary>
<ul>
<li><a href="https://agentskills.io/home">Agent Skills Overview - Agent Skills</a></li>
<li><a href="https://aaif.io/">Agentic AI Foundation ( AAIF ) - Open Standards for Agentic AI</a></li>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#agentic-ai`, `#anthropic`, `#open-standards`, `#linux-foundation`, `#agent-skills`

---

<a id="item-9"></a>
## [Carbon-X: Open 14.8B Model for Joint DNA-Text Analysis](https://www.reddit.com/r/MachineLearning/comments/1xchayq/carbonx_is_an_open_148b_model_trained_jointly_on/) ⭐️ 8.0/10

Carbon-X is a newly released open-source 14.8B parameter decoder-only model that accepts raw DNA sequences in a chat interface and responds in English, trained jointly on DNA and text using a shared token stream of 6-mer tokens across 302B training tokens. Released under Apache 2.0 licensing, the model achieves a 66.7% average across five DNA benchmarks and can run locally on a single 80GB GPU in bfloat16 precision. This model bridges genomic sequence analysis and natural language processing, enabling researchers to query raw DNA directly in conversational format and receive English explanations, which could streamline genomic research workflows. Its ability to run locally on a single GPU makes it especially valuable for analyzing sensitive genomic datasets that cannot be uploaded to cloud services due to privacy or regulatory constraints. Carbon-X uses 6-mer tokenization where raw DNA nucleotide strings are split into overlapping six-character subsequences, and shares a single token stream for both DNA and text. The model has not been clinically validated, and the model card explicitly states that exact sequence operations such as motif finding or restriction site detection should still be handled by traditional code rather than the model.

reddit · r/MachineLearning · /u/jatingargiitk · Oct 22, 12:32

**Background**: DNA language models need to convert raw nucleotide strings (e.g., "GATTACA") into numerical tokens before processing, and 6-mer tokenization splits sequences into overlapping six-nucleotide subsequences, a strategy used by models like DNABERT. Decoder-only transformer architecture, popularized by the GPT series, uses causal self-attention and has become the standard blueprint for generative language models. The bfloat16 (Brain Float 16) precision format reduces memory footprint by using 16 bits per parameter instead of 32, allowing large models to fit on fewer GPUs during inference.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2507.18570">[2507.18570] Hybrid Tokenization Strategy for DNA Language ... Tokenization - DNALLM Documentation Tokenization & Architecture - Generative AI for Biomedical ... Taykhoom/DNABERT-6mer · Hugging Face Per-base, BPE, and 6-mer on the same DNA sequence - a Hugging ... k-mers, tokenization, and sequence windows | Hermon DNA and ...</a></li>
<li><a href="https://blog.algomaster.io/p/transformer-architecture">A deep dive into the Transformer architecture</a></li>
<li><a href="https://deepwiki.com/ogunerkutay/huggingface-llm-examples/4.1-mixed-precision-inference">Mixed Precision Inference | DeepWiki</a></li>

</ul>
</details>

**Tags**: `#genomics`, `#large-language-models`, `#open-source`, `#bioinformatics`, `#machine-learning`

---

<a id="item-10"></a>
## [Anthropic Releases Claude API Version 2026-10-21, Removes Sampling Parameters](https://x.com/ClaudeDevs/status/2113013247209021918) ⭐️ 8.0/10

Anthropic released Claude API version 2026-10-21, the first formal version update since the 2023-06-01 beta, which removes the temperature, top_p, and top_k parameters entirely. Passing any of these parameters will now result in a 400 error, and the SDK and ant CLI have been updated to use the new version by default with authentication headers changed to Authorization: Bearer. This is a significant breaking change that directly impacts all developers using the Claude API, as the removed parameters are core sampling controls used to manage output randomness and creativity. The shift from a beta version to a formal version, along with authentication header changes, signals a major platform evolution that requires developers to update their integrations. The old version 2023-06-01 has not been deprecated, allowing developers to continue using it during the transition. The ant CLI is Anthropic's official command-line interface for calling Claude API resources from a terminal and is not a replacement for the Python or TypeScript SDKs.

telegram · zaihuapd · Oct 22, 03:54

**Background**: Temperature, top_p, and top_k are sampling parameters in LLM APIs that control the randomness and diversity of generated text. Temperature adjusts the probability distribution sharpness, top_p (nucleus sampling) limits token selection to a cumulative probability threshold, and top_k restricts selection to the top-k most likely tokens. These parameters have been standard knobs in virtually all LLM APIs, including OpenAI's GPT series and Anthropic's Claude, allowing developers to fine-tune output behavior for different use cases.

<details><summary>References</summary>
<ul>
<li><a href="https://amitray.com/llm-parameters-temperature-top-p-top-k-guide/">LLM Temperature, Top-P, Top-K & 11 Core Parameters: The ...</a></li>
<li><a href="https://agentpedia.codes/blog/claude-api-ant-cli-guide">Claude Platform ant CLI : Official Developer Guide</a></li>
<li><a href="https://ai-tldr.dev/learn/llm-apis/api-basics/sampling-parameters-explained/">Temperature, Top-P, Top-K: LLM Sampling Parameters | AI/TLDR</a></li>

</ul>
</details>

**Tags**: `#Anthropic`, `#Claude API`, `#Breaking Changes`, `#AI/ML`, `#Developer Tools`

---

<a id="item-11"></a>
## [Australian Court Rules Apple Must Open iPhone to Third-Party App Stores](https://9to5mac.com/2026/10/21/apple-must-open-iphone-to-alternative-app-stores-in-australia-after-epic-games-ruling/) ⭐️ 8.0/10

An Australian federal court ruled that Apple must allow Australian iPhone users to install apps via third-party app stores and websites, and must permit alternative payment methods and external payment links, effective March 1, 2027. The court also ordered that Fortnite be immediately reinstated on the Australian App Store. This ruling forces Apple to dismantle its walled-garden app distribution model in Australia, following a global regulatory trend led by the EU's Digital Markets Act. It has major implications for app developers, payment processors, and Apple's services revenue, as the Epic v. Apple litigation continues to reshape app store ecosystems worldwide. The court found that Apple holds substantial market power in iOS app distribution and payment markets, and that its restrictions on competition violate Australian competition law. Apple has stated it will appeal the ruling and seek a stay of enforcement, meaning the actual implementation timeline could shift pending appeal outcomes.

telegram · zaihuapd · Oct 22, 06:54

**Background**: Epic Games sued Apple in August 2020, alleging that Apple's App Store practices constituted a monopoly by preventing third-party storefronts and alternative payment methods. The litigation has spanned multiple jurisdictions including the US and now Australia, with courts and regulators increasingly scrutinizing Apple's control over iOS app distribution. The EU's Digital Markets Act already forced Apple to allow third-party app stores and sideloading in Europe, setting a precedent that other regions are beginning to follow. Apple has historically argued that its closed ecosystem is essential for security and user privacy.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Epic_Games_v._Apple">Epic Games v. Apple - Wikipedia</a></li>
<li><a href="https://howmobile.net/ios/ios-sideloading-guide">iOS Sideloading Guide 2026 — Every Method That Actually Works</a></li>

</ul>
</details>

**Tags**: `#antitrust`, `#apple`, `#app-store`, `#epic-games`, `#regulation`

---

<a id="item-12"></a>
## [333 Backdoored Tor Exit Relays Delisted and Shut Down](https://kaba.cx/posts/20261020_Tor/) ⭐️ 8.0/10

A Tor operator scanned approximately 3,000 exit relays and discovered 333 infected with the Ebury backdoor, which hijacked SSH connections on port 22 to 12 interception servers for credential theft. These nodes were flagged as BadExit on October 4 and taken fully offline the following day. This incident reveals that roughly 10% of Tor exit relays were compromised, undermining the trust model that underpins the Tor network's privacy guarantees. It highlights the persistent threat posed by the Ebury botnet, which has been active since 2009 and compromised hundreds of thousands of Linux servers, to anonymity infrastructure. The attackers had compromised these servers as early as August, blocking certain ports to specifically collect unencrypted email traffic. The exact intrusion vector remains unidentified, and the Ebury malware operates by modifying shared libraries used by the legitimate OpenSSH program to steal credentials.

telegram · zaihuapd · Oct 22, 14:52

**Background**: Tor exit relays are the final nodes in the Tor circuit that connect users to the destination website, meaning they can observe unencrypted traffic exiting the network. The BadExit flag is a mechanism used by the Tor Project to mark relays that are misconfigured or malicious, instructing the Tor network to avoid routing traffic through them. Ebury is a long-running OpenSSH backdoor and credential stealer developed by the Windigo group, primarily targeting Linux servers and container hosts. According to ESET research published in 2024, the Ebury botnet has infected nearly 400,000 Linux servers since 2009, with roughly 100,000 still compromised as of late 2023.

<details><summary>References</summary>
<ul>
<li><a href="https://attack.mitre.org/software/S0377/">Ebury, Software S0377 | MITRE ATT&CK®</a></li>
<li><a href="https://www.eset.com/us/about/newsroom/press-releases/eset-research-ebury-botnet-alive-growing/">ESET Research: Ebury botnet alive & growing; 400k Linux ...</a></li>
<li><a href="https://support.torproject.org/relay-operators/">Relay Operators | Tor Project | Support</a></li>

</ul>
</details>

**Tags**: `#tor`, `#security`, `#malware`, `#privacy`, `#botnet`

---

<a id="item-13"></a>
## [Banned Nvidia B300 Chips Found in Chinese State-Backed Networks](https://theinference.org/article/china-s-state-money-bought-banned-nvidia-b300-servers-then-redacted-the-receipts) ⭐️ 8.0/10

Chinese state-backed semiconductor leasing group financed the purchase of 32 Asus servers equipped with US-banned Nvidia B300 chips for AI company Honor Vision Technology, as part of a larger 700-plus server transaction exceeding 3 billion RMB. After the filings attracted scrutiny, the leasing group resubmitted documents with hardware descriptions redacted, and both Nvidia and Asus have launched investigations. This represents a significant potential breach of US export controls, as the B300 falls under the strictest tier of US chip export restrictions, essentially banning sales to China. The involvement of state-backed entities, the scale of the transaction, and the deliberate redaction of records raise serious geopolitical and compliance concerns that could escalate US-China technology tensions. The servers were planned for deployment at the China Mobile Ningxia hub, a major data center campus in Zhongwei that is part of China's national computing network. The B300 is Nvidia's next-generation AI GPU with a reported 1,400W TDP, delivering approximately 50% more AI compute performance than its predecessor, and Nvidia reportedly reworked its entire supply chain approach for this chip generation.

telegram · zaihuapd · Oct 22, 15:22

**Background**: In January 2025, the US Department of Commerce's Bureau of Industry and Security (BIS) issued an interim final rule establishing a three-tiered AI chip export control framework that categorizes countries by alliance status and severely restricts China's access to advanced semiconductors. The B300 chip falls under the strictest tier of this framework, making it essentially prohibited from export to China. China Mobile's Ningxia hub in Zhongwei is a large-scale data center campus that combines phased construction with intelligent computing infrastructure as part of China's national computing network and Western China development strategy.

<details><summary>References</summary>
<ul>
<li><a href="https://www.tomshardware.com/tech-industry/artificial-intelligence/nvidias-next-gen-b300-gpus-have-1-400w-tdp-deliver-50-percent-more-ai-horsepower-report">Nvidia 's next-gen B 300 GPUs have 1,400W TDP... | Tom's Hardware</a></li>
<li><a href="https://www.stblaw.com/about-us/publications/view/2025/01/15/bis-announces-worldwide-export-controls-on-advanced-chips-and-ai-models">BIS Announces Worldwide Export Controls on Advanced Chips and ...</a></li>
<li><a href="https://www.datacenters.com/china-mobile-international-ltd-ningxia-zhongwei">China Mobile International Ltd: Ningxia Zhongwei Data Center</a></li>

</ul>
</details>

**Tags**: `#Nvidia`, `#Export Controls`, `#Geopolitics`, `#AI Chips`, `#Hardware`

---
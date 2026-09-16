---
layout: default
title: "Horizon Summary: 2026-09-16 (EN)"
date: 2026-09-16
lang: en
---

> From 33 items, 3 important content pieces were selected

---

1. [Security Researchers Expose Critical Vulnerabilities in Flock Surveillance Cameras](#item-1) ⭐️ 8.0/10
2. [TMLR Tests Author Comprehension of Papers Slated for Desk Rejection](#item-2) ⭐️ 8.0/10
3. [Apple's A20 Pro: First 2nm Smartphone Chip with Custom C2 Modem and N1 Wireless Chip](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Security Researchers Expose Critical Vulnerabilities in Flock Surveillance Cameras](https://www.wired.com/story/hackers-flock-camera-data-shows-how-system-works/) ⭐️ 8.0/10

Security researchers discovered that Flock surveillance cameras contain hardcoded API keys and store credentials in plaintext, allowing anyone with physical access to a device to extract sensitive authentication data and potentially access Flock's backend servers. The findings, reported in collaboration with 404media, also revealed that Distributed Denial of Secrets has published the partition images of the compromised devices for public analysis. Flock cameras are widely deployed by law enforcement agencies across the United States for automated license plate recognition and mass surveillance, meaning these vulnerabilities expose not just technical flaws but also the privacy of millions of citizens whose vehicle data is collected. The discovery of hardcoded credentials and plaintext storage in a product designed for unsecured public spaces reveals a fundamental failure in threat modeling for critical surveillance infrastructure. The vulnerabilities include a hardcoded API key embedded in the device firmware that can be used to request credentials stored in plaintext on the device, potentially granting access to Flock's server infrastructure. Flock's Vulnerability Disclosure Policy effectively discourages meaningful security research by prohibiting researchers from interacting with the device or downloading its data, making it nearly impossible to demonstrate the severity of discovered vulnerabilities through legitimate channels.

hackernews · driverdan · Sep 16, 13:18 · [Discussion](https://news.ycombinator.com/item?id=49726586)

**Background**: Flock Safety is a privately held American company that manufactures automated license plate recognition (ALPR) cameras and surveillance systems used by thousands of law enforcement agencies nationwide. Unlike traditional traffic cameras, Flock cameras continuously capture and store license plate data, creating searchable databases of vehicle movements that raise significant civil liberties concerns. Hardcoded secrets — API keys, passwords, and tokens embedded directly in source code — are classified under OWASP A07:2021 as one of the most common causes of infrastructure breaches, while plaintext credential storage violates basic security best practices by leaving authentication data readable to anyone with file access.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Flock_Safety">Flock Safety - Wikipedia</a></li>
<li><a href="https://mashable.com/tech/flock-cameras-explained-surveillance">What are Flock cameras? How they work and why they’re ...</a></li>
<li><a href="https://community.owasp.org/vulnerabilities/Password_Plaintext_Storage">Password Plaintext Storage | OWASP Foundation</a></li>

</ul>
</details>

**Discussion**: Commenters overwhelmingly condemned Flock's security practices as signs of incompetence, noting that hardcoded credentials and plaintext storage reflect a prioritization of speed-to-market over proper security architecture. Multiple users criticized Flock's Vulnerability Disclosure Policy as deliberately designed to create an appearance of responsible security without actually facilitating meaningful vulnerability reports, while others pointed out that deploying off-the-shelf hardware in unsecured public spaces without accounting for physical access in the threat model was a fundamental product management failure.

**Tags**: `#security`, `#surveillance`, `#vulnerability-disclosure`, `#privacy`, `#iot`

---

<a id="item-2"></a>
## [TMLR Tests Author Comprehension of Papers Slated for Desk Rejection](https://www.reddit.com/r/MachineLearning/comments/1wid67h/tmlr_reached_out_to_the_authors_of_10_papers/) ⭐️ 8.0/10

TMLR's Co-Editor-in-Chief personally interviewed authors of 10 papers slated for desk rejection, asking them to explain their own submissions. Only one author could adequately answer all questions, while three could not answer basic questions, three struggled with technical details, and the rest withdrew, were unavailable, or no-showed. This investigation reveals a troubling pattern of authors unable to explain their own research, raising serious concerns about ghost authorship, paper mills, and AI-generated submissions in ML publishing. The findings could catalyze reforms in how venues verify authorship and submission integrity across the academic publishing ecosystem. Of the 10 submissions, one was withdrawn, one author cited unavailability, one no-showed, three failed to answer basic questions, three could discuss high-level ideas but not technical details, and only one answered all questions — though the interviewer identified a major flaw even in that paper. The investigation was conducted by a Co-EiC of TMLR and documented in a Medium article.

reddit · r/MachineLearning · /u/hihey54 · Sep 16, 23:20

**Background**: TMLR (Transactions on Machine Learning Research) is a machine learning journal founded in December 2021 to complement JMLR and serve the growing ML research community. A desk rejection occurs when an editor rejects a paper before it enters the full peer review process, typically because it fails to meet basic quality, scope, or formatting standards. The investigation was motivated by growing concerns about research integrity, including the rise of AI-generated papers and authorship practices where listed authors may not have meaningfully contributed to the work.

<details><summary>References</summary>
<ul>
<li><a href="https://jmlr.org/tmlr/">Transactions on Machine Learning Research (TMLR)</a></li>
<li><a href="https://medium.com/@hugo_larochelle_65309/announcing-the-transactions-on-machine-learning-research-3ea6101c936f">Announcing the Transactions on Machine Learning Research | by Hugo Larochelle | Medium</a></li>
<li><a href="https://link.springer.com/article/10.1007/s11948-017-9921-3">Establishing Sensible and Practical Guidelines for Desk Rejections</a></li>

</ul>
</details>

**Tags**: `#machine-learning`, `#research-integrity`, `#peer-review`, `#academic-publishing`, `#TMLR`

---

<a id="item-3"></a>
## [Apple's A20 Pro: First 2nm Smartphone Chip with Custom C2 Modem and N1 Wireless Chip](https://www.bilibili.com/video/BV1oZeA6fERD) ⭐️ 8.0/10

Apple announced the A20 Pro, its first 2nm smartphone chip, powering the iPhone 18 Pro series with a 6-core CPU (20% speedup), 7-core GPU (40% speedup), dual 16-core neural engine, and 50% higher memory bandwidth over the A19 Pro. The launch also includes Apple's custom C2 modem (50% faster uploads, 15% lower power) and the N1 wireless chip supporting Wi-Fi 7, Bluetooth 6, and Thread protocol. The A20 Pro represents the industry's first commercial 2nm chip, marking a major semiconductor manufacturing milestone and giving Apple a significant performance lead in mobile computing. The shift to fully custom C2 modem and N1 wireless chip signals Apple's deepest vertical integration yet, replacing long-time suppliers Qualcomm and Broadcom and reshaping the mobile semiconductor supply chain. The A20 Pro adopts a new packaging design borrowed from the M series combined with a 3x larger vapor chamber (VC) cooling system, enabling sustained performance gains of up to 40% over the previous generation. Notably, the US version of the iPhone 18 Pro Max retains a Qualcomm modem instead of the C2 chip, creating a regional hardware divide in modem technology.

telegram · zaihuapd · Sep 16, 13:24

**Background**: TSMC's 2nm process node represents the latest advancement in semiconductor manufacturing, offering improved power efficiency and transistor density over the previous 3nm generation. Vapor chamber (VC) cooling uses liquid-to-vapor phase change to efficiently spread heat across a chip surface, which is critical for sustaining high performance in compact mobile form factors where heat flux densities continue to rise. Apple has been progressively replacing third-party components with custom silicon — having already transitioned Macs from Intel to M-series chips — and is now replacing Qualcomm modems and Broadcom wireless chips with its own C2 and N1 designs in iPhones.

<details><summary>References</summary>
<ul>
<li><a href="https://www.androidheadlines.com/2026/09/iphone-18-pro-duo-ditch-qualcomm-apple-c2-modem.html">iPhone 18 Pro Has Apple C2 Modem Instead of Qualcomm's</a></li>
<li><a href="https://www.techspot.com/news/109402-new-iphones-get-wi-fi-7-bluetooth-6.html">New iPhones get Wi - Fi 7 and Bluetooth 6 via Apple 's in-house...</a></li>
<li><a href="https://www.androidheadlines.com/2026/09/apple-clarifies-eu-iphone-18-pro-max-c2-modem-error.html">EU iPhone 18 Pro Max Keeps C2 Modem Chip</a></li>

</ul>
</details>

**Tags**: `#apple`, `#semiconductors`, `#2nm`, `#a20-pro`, `#mobile-chips`

---
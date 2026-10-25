---
layout: default
title: "Horizon Summary: 2026-10-25 (EN)"
date: 2026-10-25
lang: en
---

> From 29 items, 2 important content pieces were selected

---

1. [High-Severity Brotli Vulnerability CVE-2026-111497 Affects Python and Node.js](#item-1) ⭐️ 9.0/10
2. [10-Year-Old CNN Outperforms Frontier LLMs at Skin Cancer Diagnosis](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [High-Severity Brotli Vulnerability CVE-2026-111497 Affects Python and Node.js](https://www.aikido.dev/blog/python-packages-vulnerable-node2shell-brotli-cve-2026-111497) ⭐️ 9.0/10

A high-severity vulnerability (CVE-2026-111497) in Google's Brotli decoder, affecting versions 1.0.3 to 1.2.0 with a CVSS 4.0 score of 9.2, has been disclosed as expanding to Python packages. Remote unauthenticated attackers can exploit this flaw by sending specially crafted compressed streams to cause memory corruption, data leaks, crashes, or potential arbitrary code execution. Patches are available: Python's Brotli should be upgraded to 1.2.1 and brotlicffi to 1.2.1.0, while Node.js fixed versions are 22.23.4, 24.22.1, or 26.12.1. This vulnerability is critical because Brotli is a widely adopted compression library embedded in core HTTP components across multiple major ecosystems including Node.js, Python, Bun, and Envoy. The potential for remote code execution means that any service processing untrusted compressed data could be compromised, making immediate patching a high priority for the entire industry. The flaw is an out-of-bounds write triggered during the decoding of malformed Brotli input, initially disclosed under the name Node2Shell and later referred to as HTTP2Shell. OpenAI reportedly discovered the issue in February of this year, and code execution was demonstrated on at least one Node.js build.

telegram · zaihuapd · Oct 25, 02:42

**Background**: Brotli is a general-purpose lossless compression algorithm developed by Google, commonly used for HTTP content compression to reduce transfer sizes for web traffic. It is implemented as a C library and bundled into many runtime environments and servers, including Node.js and various Python packages. Because Brotli decoders process data from network inputs, memory safety bugs in the decoder can be triggered by remote attackers, potentially leading to code execution on the server side.

<details><summary>References</summary>
<ul>
<li><a href="https://www.aikido.dev/blog/python-packages-vulnerable-node2shell-brotli-cve-2026-111497">Node2Shell Brotli vuln (CVE-2026-111497) evolves to HTTP2Shell, as...</a></li>
<li><a href="https://thehackernews.com/2026/10/brotli-decoder-flaw-behind-nodejs-rce.html">Brotli Decoder Flaw Behind Node.js RCE Also Affects Bun, Python...</a></li>
<li><a href="https://vercel.com/kb/bulletin/node-js-security-advisory">Node.js security advisory: Brotli decoder ... | Vercel Knowledge Base</a></li>

</ul>
</details>

**Tags**: `#security`, `#vulnerability`, `#brotli`, `#python`, `#nodejs`

---

<a id="item-2"></a>
## [10-Year-Old CNN Outperforms Frontier LLMs at Skin Cancer Diagnosis](https://lynchlab.net/llm-skin-cancer) ⭐️ 8.0/10

An experiment compared a decade-old Inception v3 CNN, fine-tuned on over 68,000 dermoscopic and clinical images from the ISIC Archive, against frontier LLMs like GPT-4o and Claude 3.5 Sonnet for skin cancer diagnosis. The specialized CNN significantly outperformed the general-purpose LLMs on the same diagnostic task. This result highlights that specialized, task-specific architectures can still dramatically outperform massive general-purpose models in domain-specific applications, challenging the assumption that frontier LLMs are universally superior. It underscores the value of purpose-built AI systems in medical imaging and other high-stakes specialized fields. The CNN used was Inception v3, pretrained on everyday photographs and then fine-tuned on all layers using 68,011 images from the ISIC Archive on a single H100 GPU. The 200 test lesions were carefully excluded from training and validation data to prevent data leakage, though commenters noted the comparison may involve 'benchmaxxing' since the CNN was specifically optimized for this benchmark.

hackernews · sungam · Oct 25, 17:15 · [Discussion](https://news.ycombinator.com/item?id=50233779)

**Background**: Convolutional Neural Networks (CNNs) are a class of deep learning networks particularly effective for image processing, using learned filters to extract features from visual data. Frontier LLMs like GPT-4o and Claude 3.5 Sonnet are large, general-purpose AI systems designed for broad tasks including reasoning, coding, and multimodal understanding. In medical imaging, specialized CNNs have been the dominant approach for years, as they can be trained on curated datasets to recognize specific visual patterns such as skin lesions with high accuracy.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Convolutional_neural_network">Convolutional neural network - Wikipedia</a></li>
<li><a href="https://www.akamai.com/glossary/what-are-frontier-llms">What Are Frontier LLMs - Akamai</a></li>

</ul>
</details>

**Discussion**: Commenters largely agreed that specialized models outperforming generalist LLMs is expected, with one comparing it to how a 30M-parameter KataGo network beats frontier LLMs at Go. Some criticized the comparison as 'benchmaxxing' since the CNN was specifically optimized for this benchmark, while others suggested testing LLMs with supervised training data provided in-context. One commenter quipped that a calculator also outperforms LLMs at multiplication.

**Tags**: `#machine-learning`, `#medical-imaging`, `#llms`, `#computer-vision`, `#benchmarking`

---
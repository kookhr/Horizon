---
layout: default
title: "Horizon Summary: 2026-10-10 (ZH)"
date: 2026-10-10
lang: zh
---

> 从 39 条内容中筛选出 2 条重要资讯。

---

1. [Cloudflare 收购 Deno，计划终止 Deno 运行时开发](#item-1) ⭐️ 10.0/10
2. [中国天眼 FAST 发现首例脉冲星原生三体系统](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Cloudflare 收购 Deno，计划终止 Deno 运行时开发](https://simonwillison.net/2026/Oct/9/deno-is-joining-cloudflare/) ⭐️ 10.0/10

Cloudflare 已全资收购 Deno，计划基于 Deno 的 celld 项目将 workerd 自托管打造为一流体验。Deno 运行时将获得为期一年的月度维护版本（包含错误修复和安全更新），之后将停止主动开发，但项目仍将保持开源。 此次收购将两大 JavaScript 运行时玩家合并到同一阵营，实际上终结了 Deno 作为 Node.js 活跃替代方案的地位，使 Bun 成为主要的独立竞争者。这也反映了开发者工具整合的更广泛行业趋势——边缘/无服务器平台正在吸收运行时项目以强化自身生态。 celld 是 Deno 于 2026 年 8 月发布的一个 Rust 单二进制文件，实现了 Cloudflare 的 Durable Objects 模式，仅依赖对象存储进行协调和持久化。Ryan Dahl 表示，Deno 最终被 Node.js 兼容性的引力所吞噬，使其沦为对已有可用工具的重复实现，而 celld 代表了一种全新的服务器开发模型，他认为这更有价值。

rss · Simon Willison · 10月9日 22:48

**背景**: Deno 是由 Node.js 创始人 Ryan Dahl 创建的 JavaScript/TypeScript 运行时，于 2018 年发布，专注于安全性、现代异步架构和基于权限的沙箱系统。Cloudflare Workers 是由 workerd 驱动的无服务器平台，workerd 是一个开源的 JavaScript/Wasm 运行时；Durable Objects 则提供有状态的无服务器能力，用于构建实时和分布式应用。celld 是 Deno 将 Durable Objects 编程模型引入自托管基础设施的尝试，这与 Cloudflare 让 workerd 在其自身网络之外可自托管的目标直接契合。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deno.com/blog/cloudflare">Deno is joining Cloudflare | Deno</a></li>
<li><a href="https://github.com/cloudflare/workerd">workerd, Cloudflare's JavaScript/Wasm Runtime - GitHub</a></li>

</ul>
</details>

**社区讨论**: 社区情绪以悲伤和失望为主，许多用户表示 Deno 是他们最喜欢的 JS 运行时，并对创新的中止感到惋惜。多位评论者指出，转向 npm 兼容性标志着衰落的开始，因为在 VC 资金压力下，Deno 曾经简洁的接口变得臃肿。一位评论者将此新闻重新定义为'人才收购'而非真正的收购，另一位则强调了开发者工具在整个行业范围内整合的更广泛趋势。

**标签**: `#deno`, `#cloudflare`, `#javascript-runtime`, `#acquisition`, `#edge-computing`

---

<a id="item-2"></a>
## [中国天眼 FAST 发现首例脉冲星原生三体系统](https://nao.cas.cn/news/gd/202610/t20261009_8289939.html) ⭐️ 8.0/10

中国天眼 FAST 望远镜发现脉冲星 PSR J0435+3233 属于首例仍在演化阶段的原生三体系统，该结论由中欧科学家独立确认。该系统由脉冲星、氦白矮星和类太阳恒星组成，内外轨道周期分别为 8 天和 73.5 年，成果于 2026 年 10 月 9 日发表于《天体物理学杂志快报》。 这是首个被确认的仍处于活跃演化阶段的脉冲星原生三体系统，为研究等级三体系统的形成与动力学演化提供了罕见的天然实验室。它为多波段观测和恒星演化理论检验提供了此前双星或动力学形成的三体系统所不具备的独特机会。 该系统位于银河系场区而非致密星团中，强烈表明它由同一气体云中诞生的三颗主序星演化而来，脉冲星、白矮星和类太阳恒星的前身星质量分别约为 20、2 和 1 个太阳质量。脉冲星的伽马射线脉冲可追溯至 2008 年 Fermi LAT 数据的开端，研究还利用存档的光学/红外数据来确认伴星。

telegram · zaihuapd · 10月9日 05:14

**背景**: 脉冲星是一种快速旋转的中子星，会发射电磁辐射束，因其极其规律的旋转周期而常被用作精确的宇宙时钟。原生三体系统是指三颗恒星由同一分子云共同诞生，并在整个演化过程中保持引力束缚的系统，与后期通过动力学俘获形成的系统相对。FAST（五百米口径球面射电望远镜）被誉为'中国天眼'，位于贵州省，是目前世界上最大的单口径射电望远镜，自投入运行以来已发现数百颗新脉冲星。等级三体系统具有两层嵌套轨道：一个近距内双星和一个绕内双星运行的较远第三伴星。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2608.01227">[2608.01227] The PSR J0435+3233 Triple System - arXiv.org</a></li>
<li><a href="https://english.news.cn/20261009/42f03cd3473d4618a0a93f29ad9f6d31/c.html">China's FAST telescope identifies pulsar as part of evolving primordial ...</a></li>
<li><a href="https://iopscience.iop.org/article/10.3847/2041-8213/aeaa29">The PSR J0435+3233 Triple System - IOPscience</a></li>

</ul>
</details>

**标签**: `#astronomy`, `#pulsar`, `#FAST-telescope`, `#astrophysics`, `#scientific-discovery`

---
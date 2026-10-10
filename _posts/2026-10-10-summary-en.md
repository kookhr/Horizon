---
layout: default
title: "Horizon Summary: 2026-10-10 (EN)"
date: 2026-10-10
lang: en
---

> From 39 items, 2 important content pieces were selected

---

1. [Cloudflare Acquires Deno, Plans to End Deno Runtime Development](#item-1) ⭐️ 10.0/10
2. [China's FAST Telescope Discovers First Known Primordial Pulsar Triple System](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Cloudflare Acquires Deno, Plans to End Deno Runtime Development](https://simonwillison.net/2026/Oct/9/deno-is-joining-cloudflare/) ⭐️ 10.0/10

Cloudflare has acquired Deno outright, with plans to build on Deno's celld project to make workerd self-hosting a first-class experience. The Deno runtime will receive one year of monthly maintenance releases containing bug fixes and security updates, after which active development will cease, though the project will remain open source. This acquisition consolidates two major JavaScript runtime players under one roof and effectively ends Deno as an actively developed alternative to Node.js, leaving Bun as the primary independent challenger. It also signals a broader industry trend of developer tooling consolidation, where edge/serverless platforms are absorbing runtime projects to strengthen their ecosystems. celld is a single Rust binary released by Deno in August 2026 that implements Cloudflare's Durable Objects pattern, depending only on object storage for coordination and persistence. Ryan Dahl stated that Deno was ultimately pulled into Node.js compatibility gravity, making it a reimplementation of something that already works, while celld represents an entirely new model for server development that he finds more impactful.

rss · Simon Willison · Oct 9, 22:48

**Background**: Deno is a JavaScript/TypeScript runtime created by Node.js founder Ryan Dahl, launched in 2018 with a focus on security, modern async architecture, and a permission-based sandboxing system. Cloudflare Workers is a serverless platform powered by workerd, an open-source JavaScript/Wasm runtime, and Durable Objects provide stateful serverless capabilities for building real-time and distributed applications. celld was Deno's attempt to bring the Durable Objects programming model to self-hosted infrastructure, which directly aligns with Cloudflare's goal of making workerd self-hostable outside their own network.

<details><summary>References</summary>
<ul>
<li><a href="https://deno.com/blog/cloudflare">Deno is joining Cloudflare | Deno</a></li>
<li><a href="https://github.com/cloudflare/workerd">workerd, Cloudflare's JavaScript/Wasm Runtime - GitHub</a></li>

</ul>
</details>

**Discussion**: Community sentiment is predominantly sad and disappointed, with many users expressing that Deno was their favorite JS runtime and lamenting the loss of innovation. Several commenters noted that the shift toward npm compatibility marked the beginning of the end, as it bloated Deno's once-simple surface area under VC funding pressure. One commenter reframed the news as an 'acqui-hire' rather than a true acquisition, while another highlighted a broader pattern of developer tooling consolidation across the industry.

**Tags**: `#deno`, `#cloudflare`, `#javascript-runtime`, `#acquisition`, `#edge-computing`

---

<a id="item-2"></a>
## [China's FAST Telescope Discovers First Known Primordial Pulsar Triple System](https://nao.cas.cn/news/gd/202610/t20261009_8289939.html) ⭐️ 8.0/10

China's FAST telescope identified pulsar PSR J0435+3233 as the first known primordial triple system still in its evolutionary stage, independently confirmed by Chinese and European scientists. The system consists of a pulsar, a helium white dwarf, and a Sun-like star, with inner and outer orbital periods of 8 days and 73.5 years respectively, and the results were published in The Astrophysical Journal Letters on October 9, 2026. This is the first confirmed primordial triple system involving a pulsar that is still actively evolving, providing a rare natural laboratory for studying the formation and dynamical evolution of hierarchical triple star systems. It offers unique opportunities for multi-band observations and tests of stellar evolution theory that were previously unavailable with binary or dynamically-formed triple systems. The system is located in the Galactic field rather than a dense cluster, strongly suggesting it evolved from three main-sequence stars born together from the same gas cloud, with estimated progenitor masses of approximately 20, 2, and 1 solar masses for the pulsar, white dwarf, and Sun-like star respectively. Gamma-ray pulsations from the pulsar were detected back to the beginning of the Fermi LAT data in 2008, and archived optical/infrared data were used to identify the companions.

telegram · zaihuapd · Oct 9, 05:14

**Background**: A pulsar is a rapidly rotating neutron star that emits beams of electromagnetic radiation, often used as precise cosmic clocks due to their extremely regular rotation periods. A primordial triple system refers to three stars born together from the same molecular cloud that have remained gravitationally bound throughout their evolution, as opposed to dynamically formed systems where stars capture each other later. FAST (Five-hundred-meter Aperture Spherical Telescope), nicknamed 'China Sky Eye,' is the world's largest filled-aperture radio telescope, located in Guizhou Province, and has discovered hundreds of new pulsars since it began operations. A hierarchical triple system has two nested orbits: a close inner binary and a more distant third companion orbiting the inner pair.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2608.01227">[2608.01227] The PSR J0435+3233 Triple System - arXiv.org</a></li>
<li><a href="https://english.news.cn/20261009/42f03cd3473d4618a0a93f29ad9f6d31/c.html">China's FAST telescope identifies pulsar as part of evolving primordial ...</a></li>
<li><a href="https://iopscience.iop.org/article/10.3847/2041-8213/aeaa29">The PSR J0435+3233 Triple System - IOPscience</a></li>

</ul>
</details>

**Tags**: `#astronomy`, `#pulsar`, `#FAST-telescope`, `#astrophysics`, `#scientific-discovery`

---
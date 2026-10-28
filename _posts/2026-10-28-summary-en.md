---
layout: default
title: "Horizon Summary: 2026-10-28 (EN)"
date: 2026-10-28
lang: en
---

> From 42 items, 8 important content pieces were selected

---

1. [Classification of Finite Simple Groups Formalized in Lean](#item-1) ⭐️ 9.0/10
2. [OpenAI Announces Three Mathematical Proofs from Internal Models Pending Verification](#item-2) ⭐️ 9.0/10
3. [Tailscale SSH Security Vulnerability Investigation and Remediation Update](#item-3) ⭐️ 8.0/10
4. [Python's Experimental JIT Compiler to Be Removed](#item-4) ⭐️ 8.0/10
5. [US Government is hiding a secret court ruling about how it spies on Americans](#item-5) ⭐️ 8.0/10
6. [Papers with Code Revived as Open-Source Under Apache 2.0](#item-6) ⭐️ 8.0/10
7. [Ψ-0.6: Adaptive Multi-Modal Streams of Thought in a Vision-Language World Model](#item-7) ⭐️ 8.0/10
8. [Chinese Team Claims 3.2 Pb/s Optical Fiber Transmission World Record](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Classification of Finite Simple Groups Formalized in Lean](https://cfsg.axiommath.ai/) ⭐️ 9.0/10

The Classification of Finite Simple Groups (CFSG), a theorem whose original proof spans tens of thousands of pages across several hundred journal articles by approximately 100 mathematicians, has been fully formalized and computer-verified in the Lean proof assistant. The formalization effort also identified and filled one gap in the previously accepted proof. This is one of the most complex proofs in all of mathematics being subjected to rigorous computer verification, eliminating any remaining doubt about its correctness. It demonstrates that proof assistants like Lean can handle proofs of extraordinary scale and complexity, paving the way for more mathematical results to be formally verified and potentially auto-formalized with AI assistance. The original CFSG proof was published mostly between 1955 and 2004, and Daniel Gorenstein, Richard Lyons, and Ronald Solomon have been gradually publishing a simplified revised version. The formalization project is hosted at cfsg.axiommath.ai and notably found and filled one gap in the previously accepted 1,000+ page proof, underscoring the value of computer verification even for results considered settled.

hackernews · pfdietz · Oct 27, 16:29 · [Discussion](https://news.ycombinator.com/item?id=50261647)

**Background**: The Classification of Finite Simple Groups states that every finite simple group is either cyclic, alternating, belongs to a broad infinite class called groups of Lie type, or is one of 26 sporadic exceptions. Simple groups serve as the basic building blocks of all finite groups, analogous to how prime numbers are the building blocks of the natural numbers. Lean is an open-source proof assistant and functional programming language based on the calculus of constructions with inductive types, currently supported by the nonprofit Lean Focused Research Organization (FRO).

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Classification_of_finite_simple_groups">Classification of finite simple groups</a></li>
<li><a href="https://en.wikipedia.org/wiki/Lean_(proof_assistant)">Lean (proof assistant)</a></li>

</ul>
</details>

**Discussion**: Discussion covered diverse viewpoints: one commenter lamented that formalization remains in set-theoretic rather than homotopical foundations; another asked whether frontier AI models could auto-formalize all math textbooks into Lean as a one-time task. Others highlighted the historical significance of the proof's complexity, noted that mathematicians have previously incorrectly believed the classification was complete only to discover missing sporadic groups, and celebrated the finding and filling of a gap in the accepted proof.

**Tags**: `#lean`, `#formal-mathematics`, `#proof-assistants`, `#group-theory`, `#automated-reasoning`

---

<a id="item-2"></a>
## [OpenAI Announces Three Mathematical Proofs from Internal Models Pending Verification](https://openai.com/index/building-scientific-understanding-with-academic-communities/) ⭐️ 9.0/10

OpenAI has publicly announced three mathematical results produced by its internal models: a disproof of the Exponential Time Hypothesis (ETH), a proof of the local smoothing conjecture in all dimensions, and a proof of 4D Yang-Mills existence. The computer science group has already released its proof alongside a Lean formalization, while the physics group has delayed publication, and OpenAI is inviting external experts to serve as independent validators. If verified, all three results would constitute historic breakthroughs in their respective fields: overturning ETH would shake the foundations of fine-grained complexity theory and invalidate countless conditional lower bounds, the local smoothing proof would simultaneously resolve the Kakeya and Stein restriction conjectures in harmonic analysis, and 4D Yang-Mills existence directly addresses one of the seven Clay Millennium Prize problems. OpenAI characterizes these results as resembling raw research data rather than polished findings, emphasizing the need for external expert validation before any claims can be confirmed. The three groups are following different publication strategies—the CS group has already published with Lean formalization, while the physics group is withholding publication pending further review.

telegram · zaihuapd · Oct 27, 15:00

**Background**: The Exponential Time Hypothesis (ETH), formulated by Impagliazzo and Paturi in 1999, states that 3-SAT cannot be solved in subexponential time in the worst case, and serves as a foundational assumption underpinning lower bounds in fine-grained complexity theory. The local smoothing conjecture is one of the biggest open problems in harmonic analysis, with deep connections to the Kakeya conjecture, restriction conjecture, and Bochner-Riesz conjecture. The Yang-Mills existence and mass gap problem is one of the seven Millennium Prize Problems posed by the Clay Mathematics Institute, concerning the rigorous mathematical foundation of quantum gauge theories. Lean is a proof assistant based on dependent type theory that can mechanically verify mathematical proofs, increasingly used in modern mathematics for formalization.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Exponential_time_hypothesis">Exponential time hypothesis - Wikipedia</a></li>
<li><a href="https://www.quantamagazine.org/a-tower-of-conjectures-that-rests-upon-a-needle-20230912/">A Tower of Conjectures That Rests Upon a Needle | Quanta Magazine</a></li>
<li><a href="https://en.wikipedia.org/wiki/Lean_(proof_assistant)">Lean (proof assistant) - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#mathematics`, `#complexity-theory`, `#AI-research`, `#millennium-problems`

---

<a id="item-3"></a>
## [Tailscale SSH Security Vulnerability Investigation and Remediation Update](https://tailscale.com/ssh-investigation-update) ⭐️ 8.0/10

Tailscale published a detailed investigation and remediation update addressing security vulnerabilities in Tailscale SSH that could enable privilege escalation under specific ACL configurations. The vulnerabilities affect scenarios where Tailscale SSH is used with ACLs that permit SSH access to a node without granting a path to sudoers or root. Tailscale is widely used across organizations for secure networking and remote access, making any SSH-related vulnerability a significant concern for infrastructure security teams. The disclosure highlights the architectural tradeoffs between convenience-focused managed SSH solutions and traditional OpenSSH deployments, prompting many practitioners to reassess their remote access strategies. According to a former Tailscale employee's analysis, the vulnerabilities only affect nodes using Tailscale SSH (not OpenSSH daemon) with ACLs permitting SSH access without a sudoers or root path, and users without existing SSH access or connectivity to a vulnerable node are not impacted. The fixes are actively landing in the Tailscale GitHub repository, and Tailscale has not recommended disabling Tailscale SSH entirely.

hackernews · figmert · Oct 27, 19:55 · [Discussion](https://news.ycombinator.com/item?id=50264857)

**Background**: Tailscale SSH is a feature where Tailscale takes over port 22 for SSH connections incoming from the Tailscale network, replacing the need for traditional SSH key management with identity-based authentication protected by SSO and MFA. Tailscale ACLs (Access Control Lists) are used to manage device permissions and secure the network by defining which users can access which nodes. Unlike traditional OpenSSH where users manage their own keys and authentication, Tailscale SSH centralizes authentication through the Tailscale coordination server, creating a different attack surface and trust model.

<details><summary>References</summary>
<ul>
<li><a href="https://tailscale.com/tailscale-ssh">Manage SSH Keys Securely with Tailscale</a></li>
<li><a href="https://tailscale.com/docs/features/access-control/acls">Manage permissions using ACLs · Tailscale Docs</a></li>
<li><a href="https://tailscale-com.nproxy.org/docs/features/tailscale-ssh">Tailscale SSH · Tailscale Docs</a></li>

</ul>
</details>

**Discussion**: A former Tailscale employee (minimaltom) provided detailed analysis clarifying that the vulnerabilities only affect specific ACL configurations with Tailscale SSH, not OpenSSH, and only impact users who already have some level of SSH access. Several commenters advocated for sticking with traditional OpenSSH over Tailscale SSH, citing concerns about increased attack surface, feature bloat, and the risks of centralizing VPN and SSH authentication into a single point of failure. Others called for a lockdown mode that disables risky features like Taildrop and Tailscale SSH, keeping Tailscale as a pure connectivity layer.

**Tags**: `#security`, `#tailscale`, `#ssh`, `#vulnerability`, `#networking`

---

<a id="item-4"></a>
## [Python's Experimental JIT Compiler to Be Removed](https://lwn.net/SubscriberLink/1102102/0c00e4d550f25f8c/) ⭐️ 8.0/10

Python's experimental JIT compiler, introduced in Python 3.13 via PEP 744, is being removed after the Steering Council requested a new PEP to justify its continued development. The decision halts a line of work that included advanced optimizations like automatic refcount removal and type-based specializations. This is a significant setback for Python's performance optimization roadmap, particularly because the JIT was also expected to help offset the performance overhead introduced by free-threading (no-GIL) builds. The removal leaves Python without a built-in JIT path, meaning users must continue relying on external solutions like PyPy, Cython, or Numba for performance-critical workloads. The JIT was off by default and required LLVM to build, translating frequently executed bytecode into machine code using profiling data from CPython's specializing adaptive interpreter. The Steering Council's request for a new PEP suggests concerns about maintenance burden, design justification, and whether the incremental performance gains justified the complexity added to CPython's codebase.

hackernews · f311a · Oct 27, 11:17 · [Discussion](https://news.ycombinator.com/item?id=50257419)

**Background**: CPython's JIT compiler was an experimental feature introduced in Python 3.13 that aimed to make CPython faster over successive releases without requiring developers to switch runtimes or rewrite code. It worked by translating frequently executed Python bytecode into machine code at runtime, leveraging profiling information collected by the specializing adaptive interpreter. Free-threading, also introduced in Python 3.13, disables the Global Interpreter Lock (GIL) to allow true parallel thread execution, but this comes with a performance overhead that the JIT was partly expected to mitigate. PEPs (Python Enhancement Proposals) are the formal mechanism for proposing changes to Python, and the Steering Council governs which PEPs are accepted.

<details><summary>References</summary>
<ul>
<li><a href="https://peps.python.org/pep-0744/">PEP 744 – JIT Compilation | peps.python.org</a></li>
<li><a href="https://docs.python.org/3/howto/free-threading-python.html">Python support for free threading — Python 3.15.2 documentation</a></li>
<li><a href="https://github.com/python/cpython/blob/main/Tools/jit/README.md">cpython/Tools/jit/README.md at main · python/cpython</a></li>

</ul>
</details>

**Discussion**: Community sentiment is largely disappointed, with many viewing the removal as unfortunate given the technical progress being made, and some attributing it partly to bureaucratic processes. Several commenters questioned why Python repeatedly struggles with JIT implementations when languages like Ruby and JavaScript have succeeded, with suggestions that funding disparities and Python's already-optimized base interpreter play a role. Alternative approaches were proposed, including inline Cython decorators that would compile functions on first run, and some commenters argued the decision was reasonable given existing alternatives like PyPy, Numba, and C extensions.

**Tags**: `#python`, `#jit`, `#performance`, `#cpython`, `#language-design`

---

<a id="item-5"></a>
## [US Government is hiding a secret court ruling about how it spies on Americans](https://www.wired.com/story/the-us-government-is-hiding-a-secret-court-ruling-about-how-it-spies-on-americans/) ⭐️ 8.0/10

Wired reports that the US government is concealing a secret court ruling regarding its surveillance of American citizens under Section 702, prompting calls for transparency from Senator Wyden and sparking significant public debate about secret courts and domestic spying.

hackernews · helterskelter2 · Oct 27, 14:06 · [Discussion](https://news.ycombinator.com/item?id=50259604)

**Tags**: `#surveillance`, `#civil-liberties`, `#government-transparency`, `#privacy`, `#section-702`

---

<a id="item-6"></a>
## [Papers with Code Revived as Open-Source Under Apache 2.0](https://www.reddit.com/r/MachineLearning/comments/1xgoadu/papers_with_code_is_now_opensource_p/) ⭐️ 8.0/10

Papers with Code has been revived as an open-source project under the Apache 2.0 license, with its codebase hosted on HuggingFace's GitHub repository at github.com/huggingface/paperswithcode. The project features a Python FastAPI backend, React frontend, a publicly available API, and an accompanying MCP server, enabling community collaboration on tracking trending AI research, benchmarks, and SOTA results. This revival fills a critical gap in the ML ecosystem left when Meta shut down the original Papers with Code platform, which was an essential resource for researchers tracking state-of-the-art results across benchmarks. By open-sourcing the codebase under Apache 2.0 and hosting it on HuggingFace's GitHub, the project ensures community-driven sustainability beyond any single corporate entity. The application is built with a Python FastAPI backend and React frontend, hosted on a Hetzner VPS as a single monorepo, where the frontend primarily calls various API endpoints to visualize papers. The developer utilized AI coding assistants Claude and Codex during development, and the project also exposes a public API and an MCP (Model Context Protocol) server for programmatic access and AI system integration.

reddit · r/MachineLearning · /u/NielsRogge · Oct 27, 09:54

**Background**: Papers with Code was originally a widely-used website that tracked machine learning research papers alongside their code implementations, benchmark results, and state-of-the-art (SOTA) leaderboards. Meta acquired the platform but later shut it down, leaving a significant void for ML researchers who relied on it to discover papers and compare benchmark performance. The MCP (Model Context Protocol) referenced in this project is an open standard introduced by Anthropic in November 2024 to standardize how AI systems like large language models integrate with external tools and data sources.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#open-source`, `#machine-learning`, `#research-tools`, `#papers-with-code`, `#huggingface`

---

<a id="item-7"></a>
## [Ψ-0.6: Adaptive Multi-Modal Streams of Thought in a Vision-Language World Model](https://www.reddit.com/r/MachineLearning/comments/1xgwq9u/%CF%8806_adaptive_streams_of_thought_in_a_unified/) ⭐️ 8.0/10

Ψ-0.6 is a unified vision-language world model that extends chain-of-thought reasoning into adaptive multi-modal streams of thought, including depth, motion, camera pose, and imagined scenes. It uses reinforcement learning to dynamically select which representation to use during reasoning, achieving strong zero-shot performance on the MindCube spatial reasoning benchmark and outperforming other world models on FlowBench. This research bridges the gap between text-based reasoning and physical-world understanding, enabling AI to flexibly combine different forms of inference as a problem unfolds, much like humans do. The unified architecture acting as perceiver, VLM, world model, reasoner, and policy could significantly advance robotics and embodied AI by improving spatial reasoning and sim-to-real transfer. The model is trained on simulated rooms and successfully transfers its learned physical prediction capabilities to real robot tabletop environments. It surpasses leading open-weight models on complex spatial reasoning tasks, specifically demonstrating zero-shot capabilities on the MindCube benchmark which tests spatial mental modeling from limited views.

reddit · r/MachineLearning · /u/FaeriaManic · Oct 27, 16:09 · [Discussion](https://www.reddit.com/r/MachineLearning/comments/1xgwq9u/ψ06_adaptive_streams_of_thought_in_a_unified/)

**Background**: Chain-of-thought (CoT) reasoning has significantly improved language model performance on complex tasks by generating intermediate reasoning steps, but it is traditionally limited to text. Vision-language models (VLMs) combine visual perception with language understanding, yet often struggle with complex spatial reasoning and physical prediction. World models attempt to simulate the dynamics of environments, allowing agents to predict future states, which is crucial for robotics and planning.

<details><summary>References</summary>
<ul>
<li><a href="https://mind-cube.github.io/">MindCube : Spatial Mental Modeling from Limited Views | VLM Spatial ...</a></li>
<li><a href="https://arxivsignals.io/papers/2610.32177">$\Psi$-0.6: Adaptive Streams of Thought in a Unified Vision ...</a></li>

</ul>
</details>

**Tags**: `#vision-language-models`, `#world-models`, `#chain-of-thought`, `#spatial-reasoning`, `#reinforcement-learning`

---

<a id="item-8"></a>
## [Chinese Team Claims 3.2 Pb/s Optical Fiber Transmission World Record](https://www.tomshardware.com/networking/3-2-pb-s-real-time-optical-fiber-transfer-speed-world-record-claimed-by-chinese-team-speed-fast-enough-to-download-more-than-20-000-4k-movies-in-one-second) ⭐️ 8.0/10

A Chinese team has achieved a real-time optical fiber transmission speed of 3.2 Pb/s using a 24-core fiber with space-division multiplexing and S+C+L multi-band transmission technology on commercially compatible hardware. This surpasses their own previous record of 2.5 Pb/s set earlier this year by nearly 30%. This record is significant because it was achieved using commercially compatible hardware rather than experimental lab equipment, making it far more deployable in real-world telecommunications and data center infrastructure. The ~30% improvement over their previous record demonstrates rapid progress in practical high-capacity networking, which is critical for meeting the exploding bandwidth demands of AI workloads and cloud services. The test validated space-division multiplexing using a 24-core fiber combined with S+C+L multi-band transmission on a commercially compatible architecture. While laboratory fiber transmission records have reached as high as 5.29 Pb/s, those results relied on advanced or experimental equipment and signal processing, making this achievement more practically relevant despite the lower peak speed.

telegram · zaihuapd · Oct 27, 03:45

**Background**: Space-division multiplexing (SDM) is a technique that increases fiber capacity by using multiple cores within a single fiber cladding, as opposed to standard single-core fibers, enabling parallel data transmission channels. Multi-core fibers contain multiple fiber cores within a single cladding, and 24-core designs represent some of the highest core counts currently being explored. S+C+L bands refer to three wavelength bands in optical transmission — S-band (short), C-band (conventional, the most widely used in commercial systems), and L-band (long) — and combining them dramatically expands the usable optical spectrum compared to C-band-only systems.

<details><summary>References</summary>
<ul>
<li><a href="https://www.rp-photonics.com/multi_core_fibers.html">Multi-core Fibers – dual core, twisted, space division ...</a></li>
<li><a href="https://opg.optica.org/abstract.cfm?uri=CLEO_SI-2022-JW3B.105">Performance Evaluation of S + C + L - Band Optical Transmission over...</a></li>
<li><a href="https://www.csjournals.com/IJEE/PDF11-1/112.pdf">Review on High Class Transmission in Optical Fiber</a></li>

</ul>
</details>

**Tags**: `#optical-fiber`, `#networking`, `#world-record`, `#telecommunications`, `#space-division-multiplexing`

---
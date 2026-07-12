---
layout: default
title: "Horizon Summary: 2026-07-12 (EN)"
date: 2026-07-12
lang: en
---

> From 30 items, 11 important content pieces were selected

---

1. [GPT-5.6 Sol Ultra Proves 50-Year-Old Cycle Double Cover Conjecture in Under One Hour](#item-1) ⭐️ 10.0/10
2. [Researchers: xAI Grok CLI Uploads Entire Codebase and Secret Files by Default](#item-2) ⭐️ 9.0/10
3. [Fields Medalist Terence Tao Explores LLM Coding Agents for Math Visualizations](#item-3) ⭐️ 8.0/10
4. [Shingles vaccine may reduce dementia risk, sparking debate over confounding factors](#item-4) ⭐️ 8.0/10
5. [Quadriplegic Patient Regains Hand Function Using NEO BCI System](#item-5) ⭐️ 8.0/10
6. [Claude Code vs OpenCode: Token Overhead Analysis Sparks Debate](#item-6) ⭐️ 7.0/10
7. [George Hotz: LLMs Are Productive, But Frontier Labs Are Overvalued](#item-7) ⭐️ 7.0/10
8. [Fabien Sanglard's Article Claims Manual Coding Is Going Extinct Due to LLMs](#item-8) ⭐️ 7.0/10
9. [Ghostel.el: Terminal Emulator for Emacs Powered by libghostty-vt](#item-9) ⭐️ 7.0/10
10. [Zer0Fit: MCP Server Wrapping Google's TabFM and TimesFM for Zero-Shot ML](#item-10) ⭐️ 7.0/10
11. [Codex Lead Tibo Shares Guide to Integrate GPT-5.6 Sol into Claude Code via CLIProxyAPI](#item-11) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [GPT-5.6 Sol Ultra Proves 50-Year-Old Cycle Double Cover Conjecture in Under One Hour](https://www.qbitai.com/2026/07/447873.html) ⭐️ 10.0/10

GPT-5.6 Sol Ultra proved the Cycle Double Cover Conjecture — a famous open problem in graph theory for roughly half a century — in under one hour, producing a 3-page PDF proof. The model used 64 parallel sub-agents to transform the problem into edge labeling and linear equation systems over finite fields, and OpenAI published the full ~700-character prompt detailing the verification methodology. This demonstrates a paradigm-shifting capability in AI-assisted mathematical research, showing that large language models can tackle long-standing open conjectures with parallel multi-agent architectures. The publication of the prompt methodology provides reproducibility and sets a new benchmark for automated theorem proving, potentially accelerating progress across pure mathematics and formal verification. The Cycle Double Cover Conjecture states that every bridgeless graph can be covered by a collection of cycles such that each edge appears exactly twice. The proof approach assigns two labels to each edge over finite fields so that edges sharing the same label form cycles, reducing the problem to solving linear equation systems. The prompt does not prescribe fixed solution steps but instead specifies acceptance criteria, definitions, boundary conditions, and failure cases, requiring dynamic sub-agent allocation and independent review to catch definition substitution or omitted cases.

telegram · zaihuapd · Jul 12, 03:49

**Background**: The Cycle Double Cover Conjecture is one of the most famous open problems in graph theory, independently proposed by Szekeres and Seymour around the 1970s. It concerns bridgeless graphs — graphs with no bridge edge whose removal would disconnect the graph — and asserts that such graphs admit a collection of cycles covering each edge exactly twice. The conjecture connects to deep areas including graph decomposition, algebraic graph theory, and the study of nowhere-zero flows. Despite decades of effort, a general proof had remained elusive, making this a significant target for automated theorem-proving approaches.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cycle_double_cover">Cycle double cover - Wikipedia</a></li>
<li><a href="https://www.sfu.ca/~mohar/Problems/CYCLECOV.HTM">cyclecov</a></li>
<li><a href="https://www.emergentmind.com/topics/cycle-double-cover-cdc-conjecture">Cycle Double Cover Conjecture</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Mathematics`, `#Theorem Proving`, `#GPT-5`, `#Graph Theory`

---

<a id="item-2"></a>
## [Researchers: xAI Grok CLI Uploads Entire Codebase and Secret Files by Default](https://gist.github.com/cereblab/dc9a40bc26120f4540e4e09b75ffb547) ⭐️ 9.0/10

Security researchers found that xAI's Grok Build CLI (version 0.2.93) automatically uploads entire code repositories, including secret files like .env, to xAI servers and Google Cloud Storage. Even when explicitly instructed not to open certain files, their contents were still recoverable in the uploaded bundles, and toggling off the "improve model" setting did not stop the uploads. This represents a critical security and privacy vulnerability in an official xAI developer tool, as it silently exfiltrates sensitive data such as API keys and credentials without an effective opt-out mechanism. It has major implications for developers and enterprises using xAI tools, highlighting a severe trust and safety issue in AI-assisted development tools. The tool transmits data through two channels: file contents read by the tool are embedded into model conversation requests and also packaged to Google Cloud Storage, while the entire repository is uploaded as a git bundle. In testing with a 12 GB repository, over 5 GiB of data was successfully uploaded without any server-side rejection, and the researchers noted they only proved data transmission and storage behavior, not that xAI used the data for model training.

telegram · zaihuapd · Jul 12, 04:19

**Background**: Grok Build is an official command-line interface (CLI) and coding agent from xAI, powered by the Grok 4.5 model, designed to bring AI-assisted coding capabilities into the developer's terminal. A git bundle is a Git feature that packages repository data, including references like heads and tags, into a single file for offline transfer without requiring an active server connection. The research highlights how AI coding assistants that interact directly with local codebases can inadvertently or intentionally expose sensitive development artifacts to remote servers.

<details><summary>References</summary>
<ul>
<li><a href="https://x.ai/cli">Grok Build | SpaceXAI</a></li>
<li><a href="https://docs.x.ai/build/overview">Grok Build | SpaceXAI Docs</a></li>
<li><a href="https://git-scm.com/docs/git-bundle">Git - git - bundle Documentation</a></li>

</ul>
</details>

**Tags**: `#security`, `#xAI`, `#Grok`, `#privacy`, `#developer-tools`

---

<a id="item-3"></a>
## [Fields Medalist Terence Tao Explores LLM Coding Agents for Math Visualizations](https://terrytao.wordpress.com/2026/07/11/old-and-new-apps-via-modern-coding-agents/) ⭐️ 8.0/10

Fields Medalist Terence Tao published a blog post on July 11, 2026, detailing his hands-on experience using modern LLM coding agents to build interactive mathematical visualizations and app supplements for academic papers. He offered a measured assessment, noting both the productivity gains for non-critical supplementary tools and the acceptable downside risks when outputs are not mission-critical to the core research. Tao's adoption signals a broader trend: domain experts outside traditional software engineering are now leveraging coding agents to fulfill what commenters call the 'infinite latent demand for software' in academic and educational spaces. His balanced perspective—treating LLMs as tools good for some things but not to be fully trusted—provides a high-profile, credible template for how researchers can safely integrate AI into scholarly workflows.

hackernews · subset · Jul 12, 11:09 · [Discussion](https://news.ycombinator.com/item?id=48880170)

**Tags**: `#llm`, `#coding-agents`, `#academic-research`, `#visualization`, `#terence-tao`

---

<a id="item-4"></a>
## [Shingles vaccine may reduce dementia risk, sparking debate over confounding factors](https://www.economist.com/leaders/2026/07/09/a-no-brainer-for-protecting-your-brain) ⭐️ 8.0/10

A Stanford University study using a UK natural experiment found that the shingles (herpes zoster) vaccine reduced the risk of developing dementia by approximately 20%, with the protective effect observed across multiple data analyses. The study, published in Cell in December 2025, also found that vaccination reduced mild cognitive impairment and deaths due to dementia, suggesting the vaccine may slow disease progression throughout its clinical course. Dementia affects tens of millions worldwide with virtually no disease-modifying treatments available, so even a modest protective effect from an already-approved vaccine could have enormous public health implications. The finding suggests that vaccination against herpes zoster could become a rare, accessible intervention that both prevents a painful acute disease and potentially slows cognitive decline. The UK study exploited a natural experiment where eligibility for the shingles vaccine was based on a hard age cutoff, creating a comparison group of people just above and below the threshold. However, a key methodological critique argues the finding may be spurious: vaccinated individuals are less likely to be hospitalized for shingles, meaning fewer hospital visits and thus fewer incidental dementia diagnoses, potentially explaining the observed effect rather than a true biological protective mechanism.

hackernews · saikatsg · Jul 12, 15:23 · [Discussion](https://news.ycombinator.com/item?id=48881874)

**Background**: Shingles (herpes zoster) is caused by reactivation of the varicella-zoster virus, which remains dormant in the body after a chickenpox infection. The most widely used shingles vaccine is Shingrix, a recombinant zoster vaccine that requires two doses. Dementia, particularly Alzheimer's disease, involves progressive neurodegeneration with no known cure, and growing evidence suggests that viral infections and immune system function may play a role in cognitive decline. The UK's National Health Service introduced the shingles vaccine with age-based eligibility cutoffs, creating what researchers call a natural experiment that allows comparison of outcomes between groups just above and below the eligibility threshold.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cidrap.umn.edu/varicella/shingles-vaccine-may-prevent-delay-or-slow-dementia-process">Shingles vaccine may prevent, delay, or slow dementia process | CIDRAP</a></li>
<li><a href="https://med.stanford.edu/news/all-news/2025/03/shingles-vaccination-dementia.html">For those living with dementia, new study suggests shingles vaccine could slow the disease</a></li>
<li><a href="https://www.cell.com/cell/fulltext/S0092-8674(25)01256-5">The effect of shingles vaccination at different stages of the dementia disease course: Cell</a></li>

</ul>
</details>

**Discussion**: The community discussion was notably high-quality and divided between those taking practical action based on the findings and those raising methodological concerns. One user in their 40s with genetic predisposition to Alzheimer's reported planning to pay out-of-pocket (~$500) for Shingrix rather than waiting years to qualify via insurance. A critical counterargument gained traction, citing a presentation arguing the finding is spurious because vaccinated people have fewer hospital visits (due to avoiding shingles) and thus fewer incidental dementia diagnoses. Another user linked the UK study's striking eligibility-cutoff chart from Eric Topol's newsletter, while others emphasized that dementia likely has dozens of contributing risk factors, with herpes zoster being just one that happens to have a causal treatment.

**Tags**: `#health`, `#dementia`, `#vaccines`, `#public-health`, `#research`

---

<a id="item-5"></a>
## [Quadriplegic Patient Regains Hand Function Using NEO BCI System](https://www.zaobao.com.sg/news/china/story20260712-9199066) ⭐️ 8.0/10

A 36-year-old quadriplegic patient in China named Dong Hui has regained the ability to write and grasp objects after receiving a coin-sized wireless NEO brain-computer interface implant. The NEO semi-invasive BCI system, jointly developed by Neuracle Technology (Boyikang) and Tsinghua University, received market approval from China's NMPA on March 13, 2026, and has been used in 36 clinical surgeries. This marks a major milestone in brain-computer interface commercialization, as NEO became one of the first BCI systems approved for clinical use in China, directly competing with invasive approaches like Neuralink. The successful real-world application demonstrates that semi-invasive BCI technology can restore meaningful motor function for spinal cord injury patients, potentially transforming rehabilitation medicine. NEO uses a semi-invasive approach where electrodes are placed on the skull beneath the scalp, avoiding direct contact with brain tissue while still transmitting real-time brain electrical data. The system is approved for adult patients with cervical spinal cord injuries causing quadriplegia and loss of finger grasping ability, and functions as a bidirectional closed-loop BCI system.

telegram · zaihuapd · Jul 12, 14:39

**Background**: Brain-computer interfaces (BCI) are broadly categorized into three types: invasive (electrodes implanted directly into brain tissue), non-invasive (external sensors like EEG caps), and semi-invasive (electrodes placed between the skull and scalp). The NEO system represents the semi-invasive route, developed through collaboration between Neuracle Technology (Boyikang) and Tsinghua University's biomedical engineering team led by Professor Hong-Bo. NEO was selected by Nature as one of the key BCI developments to watch in 2025, highlighting its significance in the global BCI race.

<details><summary>References</summary>
<ul>
<li><a href="https://www.shine.cn/news/metro/2412106729/">Brain - computer interface technology helps paralyzed... - SHINE News</a></li>
<li><a href="https://interestingengineering.com/innovation/chinas-neo-brain-implant-trials-2024">China preps semi - invasive brain tech trials to take on Neuralink</a></li>
<li><a href="http://neuracle.cn/newsinfo/7898209.html?trk=article-ssr-frontend-pulse_little-text-block">Nature重磅： NEO 微创 脑 机 接 口 系统入选2025...</a></li>

</ul>
</details>

**Tags**: `#brain-computer interface`, `#neuroengineering`, `#medical technology`, `#BCI`, `#rehabilitation`

---

<a id="item-6"></a>
## [Claude Code vs OpenCode: Token Overhead Analysis Sparks Debate](https://systima.ai/blog/claude-code-vs-opencode-token-overhead) ⭐️ 7.0/10

An empirical analysis by Systima.ai found that Claude Code sends approximately 33,000 tokens before reading the user's prompt, compared to OpenCode's 7,000 tokens, revealing a significant difference in system overhead and cache management efficiency. The study was conducted by adding logging between the agentic coding tools and Anthropic's API endpoint to capture all requests and usage data. This finding matters because token consumption directly impacts cost and speed for developers using AI coding assistants, and the 4-5x overhead difference could translate to substantial cost differences for heavy users. The debate also raises broader questions about whether agentic coding tools are becoming unnecessarily token-heavy, potentially driven by financial incentives or sub-agent inefficiencies. The study has a notable caveat: it primarily measures token overhead rather than task outcomes, prompting the author to plan updates including a more in-depth task, qualitative results comparison, and full reproduction of inputs and outputs. Community members also noted that sub-agents in Claude Code can burn through budgets rapidly, with one user reporting 7 sub-agents launched simultaneously for a single task.

hackernews · systima · Jul 12, 18:25 · [Discussion](https://news.ycombinator.com/item?id=48883275)

**Background**: Claude Code is Anthropic's agentic coding tool that lives in the terminal, understanding codebases and helping with coding tasks through natural language commands. OpenCode is an open-source alternative AI coding agent that provides similar autonomous coding capabilities. Both tools interact with AI models through API calls, where tokens represent the units of text processed; system prompts and cache management strategies significantly affect how many tokens are consumed before actual user input is processed.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/anthropics/claude-code">GitHub - anthropics/claude-code: Claude Code is an agentic coding tool that lives in your terminal, understands your codebase, and helps you code faster by executing routine tasks, explaining complex code, and handling git workflows - all through natural language commands. · GitHub</a></li>
<li><a href="https://www.stork.ai/blog/the-ai-coder-thats-replacing-claude">OpenCode : The Free Claude Code Alternative for AI Agents | Stork. AI</a></li>
<li><a href="https://www.deeplearning.ai/courses/claude-code-a-highly-agentic-coding-assistant">Claude Code: A Highly Agentic Coding Assistant - DeepLearning.AI</a></li>

</ul>
</details>

**Discussion**: Community discussion was highly engaged with diverse viewpoints. One user argued that sub-agents are the real token burners, launching 7 sub-agents for a single task and exhausting budget before completion, while another suggested Anthropic intentionally uses more tokens for financial gain and subscription lock-in. A valid critique prompted the author to update the study to include outcome-based comparisons, and multiple users noted a broader trend of "tokenflation" where even trivial requests trigger excessive tool calls.

**Tags**: `#ai-coding-tools`, `#token-efficiency`, `#claude-code`, `#opencode`, `#developer-tools`

---

<a id="item-7"></a>
## [George Hotz: LLMs Are Productive, But Frontier Labs Are Overvalued](https://geohot.github.io//blog/jekyll/update/2026/07/12/i-love-llms.html) ⭐️ 7.0/10

George Hotz published a blog post arguing that while LLMs deliver massive productivity gains, frontier AI labs like OpenAI and Anthropic are overvalued because they will fail to capture the economic value they create. He predicts this dynamic will usher in an era of bespoke, personalized software built by individuals rather than centralized platforms. This argument challenges the trillion-dollar valuations of frontier labs by applying platform economics: value creation does not guarantee value capture. If Hotz is correct, the AI industry's revenue models are fundamentally misaligned with the actual value distribution, which could reshape investment strategies and accelerate the shift toward open-source and homelab software development. Hotz's central thesis is that the productivity gains from LLMs will be captured by end-users and developers who build bespoke tools, not by the labs training the models. He points out that current subscription pricing (e.g., $100-200/month) makes frontier models a no-brainer for productivity, but this also means the labs are underpricing relative to the value created, undermining their long-term revenue potential.

hackernews · therepanic · Jul 12, 18:31 · [Discussion](https://news.ycombinator.com/item?id=48883343)

**Background**: George Hotz is the founder of comma.ai and a well-known hacker who first gained fame for jailbreaking the iPhone and PlayStation 3. In platform economics, the concept of value capture refers to the ability of a creator or platform to retain the economic surplus generated by their product or service. Frontier labs are companies like OpenAI, Anthropic, and Google DeepMind that train the most advanced AI models, often valued at tens or hundreds of billions of dollars based on expectations of future revenue dominance.

**Discussion**: The Hacker News discussion largely agrees with Hotz's core thesis, with user SwellJoe highlighting the astute observation that labs cannot capture the value they create. User hamandcheese notes a shift toward a "have it your way" era where forking open-source projects becomes trivial, though this raises concerns about the future of upstreaming contributions. Several commenters, including TheAceOfHearts and dom96, express practical concerns about the jagged quality of current models and the sustainability of subsidized pricing, questioning whether individuals will ever be able to run frontier-level models locally before labs hike prices.

**Tags**: `#LLMs`, `#AI Economics`, `#Open Source`, `#Commentary`, `#Productivity`

---

<a id="item-8"></a>
## [Fabien Sanglard's Article Claims Manual Coding Is Going Extinct Due to LLMs](https://fabiensanglard.net/extinct/index.html) ⭐️ 7.0/10

Fabien Sanglard published an article titled "Don't you mean extinct?" arguing that writing code manually is becoming a thing of the past as LLMs take over routine coding tasks. The article asserts that developers who refuse to adopt LLMs will fall behind because they cannot produce as much output as those who do. The article sparked a significant community debate (168 points, 95 comments) about the real impact of AI on software engineering productivity and code quality. It raises important questions about whether increased output volume translates to better software, and touches on broader concerns about the devaluation of skilled labor in the tech industry. Sanglard acknowledges that while LLMs accelerate code generation, it remains important for developers to read code and understand architecture, leading him to iterate on PRs to maintain quality. Community members pushed back on the "produce as much" framing, noting that volume is rarely a meaningful evaluation metric in software engineering.

hackernews · zdw · Jul 12, 15:17 · [Discussion](https://news.ycombinator.com/item?id=48881830)

**Background**: LLMs (Large Language Models) like GPT-4 and Claude have increasingly been integrated into software development workflows through tools like GitHub Copilot and Cursor. These tools can generate boilerplate code, write tests, and assist with refactoring, prompting ongoing debates about how much of the traditional manual coding process will be automated and what skills will remain essential for developers.

**Discussion**: The community largely pushed back on the article's premise, with commenters questioning the value of producing more code versus producing quality code. One commenter drew an insightful parallel to the film industry's over-reliance on CGI, noting that after 20 years of devaluing practical effects, there is now a push back towards them because practical-era movies looked better. Others criticized the "fall behind" framing as needlessly aggressive, pointing out that volume is rarely a meaningful evaluation metric in software engineering.

**Tags**: `#LLM`, `#Software Engineering`, `#AI Productivity`, `#Coding`, `#Industry Trends`

---

<a id="item-9"></a>
## [Ghostel.el: Terminal Emulator for Emacs Powered by libghostty-vt](https://dakra.github.io/ghostel/) ⭐️ 7.0/10

Ghostel.el is a newly released terminal emulator for Emacs that uses libghostty-vt, the zero-dependency C library extracted from the Ghostty terminal emulator's core. It offers improved performance, more reliable input handling, and a nicer Elisp API compared to existing Emacs terminal options like vterm and eat. This provides Emacs users with a high-performance terminal emulation option backed by Ghostty's proven, real-world-tested core, potentially replacing vterm as the preferred terminal for many users. It also demonstrates the practical value of libghostty-vt as a reusable library that can bring fast, accurate terminal emulation to any application. libghostty-vt is a zero-dependency C library that handles terminal sequence parsing, state management, and input encoding without requiring a full terminal UI or even libc. Users switching from vterm report noticeably faster performance with fancy TUI apps, though some rough edges remain such as occasional terminal clearing issues and freezes.

hackernews · signa11 · Jul 12, 08:52 · [Discussion](https://news.ycombinator.com/item?id=48879504)

**Background**: Ghostty is a fast, cross-platform terminal emulator that uses GPU acceleration and platform-native UI, created by Mitchell Hashimoto. The project recently released libghostty-vt as a standalone library, extracted from Ghostty's core, to allow other applications to embed terminal emulation functionality without depending on the full Ghostty UI. Emacs has long had terminal emulator packages like vterm and eat, but each comes with trade-offs in performance, compatibility, and integration with Emacs' unique input handling model.

<details><summary>References</summary>
<ul>
<li><a href="https://mitchellh.com/writing/libghostty-is-coming">Libghostty Is Coming – Mitchell Hashimoto</a></li>
<li><a href="https://github.com/ghostty-org/ghostty">GitHub - ghostty-org/ghostty: Ghostty is a fast, feature ...</a></li>
<li><a href="https://ghostty.org/">Ghostty</a></li>

</ul>
</details>

**Discussion**: The maintainer (dakra) provided helpful context including a feature comparison against vterm and eat, while users switching from vterm reported significantly better performance and reliability. Community members raised practical questions about input mode usage and suggested the title should mention Emacs, since an Emacs terminal emulator is a distinct concept from a standalone terminal emulator.

**Tags**: `#emacs`, `#terminal-emulator`, `#ghostty`, `#developer-tools`, `#open-source`

---

<a id="item-10"></a>
## [Zer0Fit: MCP Server Wrapping Google's TabFM and TimesFM for Zero-Shot ML](https://www.reddit.com/r/MachineLearning/comments/1uue8cc/zer0fit_i_took_googles_new_tabfm_timesfm_ml/) ⭐️ 7.0/10

A grad student built Zer0Fit, an MCP server that packages Google's newly released TabFM and TimesFM foundation models into a single Docker container, enabling zero-shot forecasting, classification, and regression tasks through LLM integrations like Open WebUI, Claude Code, or Codex. The tool requires approximately 16GB of VRAM and runs entirely locally on CUDA-compatible NVIDIA GPUs. This project bridges the gap between transformer-based ML foundation models and conversational AI interfaces, allowing users to perform machine learning tasks that previously required building, training, and tuning models without writing any ML code. It demonstrates a practical workflow where LLMs can orchestrate specialized ML models via MCP, potentially transforming how data scientists and practitioners approach tabular and time-series problems. Zer0Fit is PyTorch-based and CUDA-only, with no Mac support, and includes dynamic model loading/unloading with a 5-minute TTL to free VRAM when idle. Tested on classic datasets, it achieved 94.7% accuracy on Iris classification and an R² of 0.91 on California Housing regression, with build targets for DGX Spark (ARM with CUDA 13) and 3090 (AMD64 with CUDA 12.6); CSV is currently supported with XLS, XLSX, JSON, and JSONL planned.

reddit · r/MachineLearning · /u/Porespellar · Jul 12, 12:32

**Background**: Google released TabFM and TimesFM as foundation models for tabular data and time-series forecasting respectively, applying the concept of in-context learning (ICL) to traditional ML tasks. TabFM frames tabular prediction as an ICL problem, eliminating the need for manual model training, hyperparameter tuning, and feature engineering, while TimesFM applies similar zero-shot logic to time-series data. MCP (Model Context Protocol) is an open-source standard for connecting AI applications to external systems, tools, and data sources. Zer0Fit combines these technologies by using MCP to expose the ML models as tools that LLMs can invoke, creating a pipeline where a user can simply upload a CSV and ask a chatbot to run classification or regression.

<details><summary>References</summary>
<ul>
<li><a href="https://research.google/blog/introducing-tabfm-a-zero-shot-foundation-model-for-tabular-data/">Introducing TabFM: A zero-shot foundation model for tabular data</a></li>
<li><a href="https://modelcontextprotocol.io/">What is the Model Context Protocol ( MCP )? - Model Context Protocol</a></li>
<li><a href="https://github.com/google-research/tabfm">GitHub - google-research/tabfm</a></li>

</ul>
</details>

**Tags**: `#Machine Learning`, `#MCP`, `#Foundation Models`, `#Zero-Shot Learning`, `#Local Deployment`

---

<a id="item-11"></a>
## [Codex Lead Tibo Shares Guide to Integrate GPT-5.6 Sol into Claude Code via CLIProxyAPI](https://x.com/thsottiaux/status/2076119366647894371) ⭐️ 7.0/10

Tibo, the project lead for OpenAI's Codex, published a quick guide on X showing Claude Code users how to connect to the GPT-5.6 Sol model through the third-party tool CLIProxyAPI, a process he says takes about five minutes. He suggested naming the configuration alias "claudex" and humorously noted that if the setup gets blocked, he owes users a reset. This demonstrates practical cross-platform model integration, allowing developers to leverage different AI models within a single coding environment without committing to one platform's application. It highlights the growing trend of interoperability in AI developer tools, where proxy tools bridge ecosystems that are otherwise siloed. CLIProxyAPI is an open-source (MIT license) proxy tool hosted on GitHub that wraps CLI tools for various AI models—including Gemini CLI, Claude Code, ChatGPT Codex, and Qwen Code—into a compatible API. GPT-5.6 Sol is part of a tiered lineup introduced by OpenAI that includes three models: Sol, Terra, and Luna, released approximately two months after GPT-5.5.

telegram · zaihuapd · Jul 12, 05:13

**Background**: Claude Code is Anthropic's CLI-based AI coding assistant, while Codex is OpenAI's equivalent tool, and both serve developers who want AI-powered code generation directly in their terminals. CLIProxyAPI acts as a middleware bridge, translating API calls between different model providers so that a tool designed for one model can access another. GPT-5.6 Sol represents OpenAI's latest model iteration, showing improvements in areas like biology workflows and genomics analysis while using fewer tokens than its predecessor.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/router-for-me/CLIProxyAPI">GitHub - router-for-me/ CLIProxyAPI : Wrap Antigravity, ChatGPT...</a></li>
<li><a href="https://openai.com/index/previewing-gpt-5-6-sol/">Previewing GPT - 5 . 6 Sol : a next-generation model | OpenAI</a></li>
<li><a href="https://medium.com/mlworks/whats-new-with-openai-s-gpt5-6-551b3d8cc6b6">What’s New With OpenAI’s GPT 5 . 6 ? | by Mayur Jain | Medium</a></li>

</ul>
</details>

**Tags**: `#AI tools`, `#Claude Code`, `#CLIProxyAPI`, `#model integration`, `#developer tools`

---
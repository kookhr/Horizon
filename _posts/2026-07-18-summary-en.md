---
layout: default
title: "Horizon Summary: 2026-07-18 (EN)"
date: 2026-07-18
lang: en
---

> From 38 items, 10 important content pieces were selected

---

1. [GPT-5.6 Solves 30-Year-Old Open Problem in Convex Optimization](#item-1) ⭐️ 9.0/10
2. [LG Monitors Silently Install Software via Windows Update Without Consent](#item-2) ⭐️ 8.0/10
3. [The Kimi K3 Moment: Non-US Lab Achieves Frontier AI Performance](#item-3) ⭐️ 8.0/10
4. [Stack Overflow Activity Decline Visualized, Sparking Debate on AI and Other Causes](#item-4) ⭐️ 8.0/10
5. [Meta Eyes $10B Compute Lease Deal with Anthropic](#item-5) ⭐️ 8.0/10
6. [SpaceX in Talks with Pentagon for Multi-Billion Dollar AI Computing Deal](#item-6) ⭐️ 8.0/10
7. [Kimi K3 Becomes First Open-Weight Model to Reach Top 3 on DeepSWE Benchmark](#item-7) ⭐️ 8.0/10
8. [TSMC A14 Process Progress Exceeds Expectations, Yield and Performance Near 90%](#item-8) ⭐️ 8.0/10
9. [Trump Administration Eyes FINRA-Like Agency to Vet Top AI Models](#item-9) ⭐️ 8.0/10
10. [US Seeks Share of Korean Chipmakers' AI Boom Profits](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [GPT-5.6 Solves 30-Year-Old Open Problem in Convex Optimization](https://old.reddit.com/r/math/comments/1uxj3cy/after_openais_cdc_proof_announcement_gpt56_used_a/) ⭐️ 9.0/10

GPT-5.6 reportedly used a prompt-based approach to solve a 30-year-old open problem in convex optimization, specifically related to the oracle complexity of convex optimization with limited memory. This breakthrough builds on OpenAI's recent mathematical proof announcements, including the cyclic double cover conjecture, and was achieved using the Sol Pro tier rather than the Ultra tier. This achievement demonstrates that large language models are advancing from tools that assist with routine mathematical computations to systems capable of making genuine research-level contributions to long-standing open problems. It signals a potential shift in how mathematical research is conducted, raising questions about the future role of human researchers and the types of problems that will remain meaningful for humans to pursue. The solved problem concerns oracle complexity for first-order convex optimization, specifically characterizing the minimax number of first-order queries required to optimize a convex Lipschitz function subject to a memory constraint. Community members noted that the problem, while niche compared to the cyclic double cover conjecture, represents a real contribution, and that showing upper bounds on time complexity is relatively straightforward while lower bounds are significantly harder.

hackernews · mbustamanter · Jul 18, 13:00 · [Discussion](https://news.ycombinator.com/item?id=48957779)

**Background**: Convex optimization is a fundamental area in mathematics and computer science that deals with minimizing convex functions over convex sets, with applications ranging from machine learning to operations research. Oracle complexity is a key concept in this field that measures how many queries to an oracle (which provides function values and gradients) are needed to find an optimal solution. The specific open problem, posed by Woodworth and Srebro in 2019 but building on decades of prior work, asks whether the quadratic memory required by known optimal methods is truly necessary, and seeks to characterize the minimum number of first-order queries needed under memory constraints. First-order methods, which use only gradient information rather than full second-order (Hessian) information, are central to modern large-scale optimization but have known theoretical gaps in their memory-complexity tradeoffs.

<details><summary>References</summary>
<ul>
<li><a href="https://proceedings.mlr.press/v99/woodworth19a.html">Open Problem: The Oracle Complexity of Convex Optimization with Limited Memory</a></li>
<li><a href="https://arxiv.org/abs/1907.00762">[1907.00762] Open Problem: The Oracle Complexity of Convex Optimization with Limited Memory</a></li>
<li><a href="https://en.wikipedia.org/wiki/Convex_optimization">Convex optimization - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Community members with domain expertise confirmed the problem represents a real, albeit niche, contribution to the field, with one noting that upper bounds on time complexity are relatively easy while lower bounds are significantly harder. There was active debate about the implications for mathematical research careers, with comparisons to how AI is affecting junior software developers—some argued that low and medium-hanging fruit in math will no longer be worth pursuing, while others questioned whether researchers gain essential training from working on such problems. Technical discussion also emerged about the difference between ChatGPT Pro (described as a multi-agent system selecting best answers) and Ultra (described as using dynamic JS workflows to orchestrate agents), and one commenter observed that AI's ability to apply massive brute force to problems where mathematical logic can be systematically explored will drive interesting advances.

**Tags**: `#AI`, `#Mathematics`, `#Optimization`, `#LLM`, `#Research`

---

<a id="item-2"></a>
## [LG Monitors Silently Install Software via Windows Update Without Consent](https://videocardz.com/newz/lg-monitors-silently-install-software-through-windows-update-without-user-consent) ⭐️ 8.0/10

LG monitors are silently installing non-sandboxed software with full system access through Windows Update when connected to a PC, without requiring any user interaction or consent. This occurs for both new LG monitor connections and for users who already had older LG monitors connected. This represents a significant security and privacy vulnerability, as the installed software has internet access and full system privileges without sandboxing, and starts automatically with every system boot. It highlights a broader issue with Windows' device installation policies allowing third-party hardware vendors to push arbitrary software through the OS update mechanism. The installed software operates without sandboxing, granting it full system access and internet connectivity, and it launches at every system boot. Users can prevent this behavior via Group Policy Editor (gpedit.msc) by enabling 'Prevent automatic download of applications associated with device metadata,' or through System Properties (sysdm.cpl) on Windows Home editions by disabling automatic manufacturer app downloads.

hackernews · baranul · Jul 18, 10:21 · [Discussion](https://news.ycombinator.com/item?id=48956688)

**Background**: Windows Update automatically downloads and installs drivers for hardware devices, including monitors, when they are connected to a PC. This feature is designed to ensure hardware compatibility and provide updated functionality without user intervention. However, the same mechanism can also deliver companion applications from hardware manufacturers alongside driver packages, which in this case includes non-sandboxed software with elevated system privileges.

<details><summary>References</summary>
<ul>
<li><a href="https://support.microsoft.com/en-US/Windows/Hardware/Drivers/automatically-get-recommended-and-updated-hardware-drivers">Automatically get recommended and updated hardware drivers</a></li>
<li><a href="https://www.howtogeek.com/how-to-update-monitor-drivers/">How to Update Monitor Drivers</a></li>

</ul>
</details>

**Discussion**: Community members emphasized that the situation is worse than the title suggests, noting the software installs silently with zero user interaction, has full system access without sandboxing, and persists across reboots. Several users provided technical workarounds including Group Policy settings and System Properties configurations to block automatic manufacturer app downloads. Many commenters argued that Microsoft bears primary responsibility for allowing this security gap, comparing it to the historical USB autorun malware problem, and called for Microsoft to enforce stricter device installation policies.

**Tags**: `#security`, `#windows`, `#privacy`, `#malware`, `#system-administration`

---

<a id="item-3"></a>
## [The Kimi K3 Moment: Non-US Lab Achieves Frontier AI Performance](https://stephen.bochinski.dev/blog/2026/07/18/the-kimi-k3-moment/) ⭐️ 8.0/10

Chinese startup Moonshot AI has released Kimi K3, a flagship model for long-horizon coding and end-to-end knowledge work with a 1M-token context window, which the company says closes the gap with leading U.S. AI systems. The model features 2.8 trillion parameters and is positioned as directly comparable to OpenAI's GPT 5.6 Sol and Anthropic's Claude Opus 4.8. Kimi K3 demonstrates that non-US AI labs can now achieve frontier-level model performance, potentially at a lower cost, challenging the dominance of American AI companies. This development raises important questions about model distillation, geopolitical implications, and the sustainability of the US's lead in AI. Kimi K3 is priced at $3/$15 per 1M tokens for input/output, compared to GPT 5.6 Sol at $5/$30 and Opus 4.8 at $5/$25, making it competitive but not dramatically cheaper. While the model trails Anthropic's Claude Fable 5 and OpenAI's GPT 5.6 Sol on overall benchmarks, it offers a 1M-token context window and is available with open weights, enabling customization and local deployment.

hackernews · sbochins · Jul 18, 17:32 · [Discussion](https://news.ycombinator.com/item?id=48960218)

**Background**: Knowledge distillation is a machine learning technique where a smaller "student" model learns to mimic the outputs of a larger, more capable "teacher" model, effectively transferring knowledge while reducing computational requirements. Open-weight models publish their trained parameters publicly, allowing anyone to run, study, and fine-tune the model locally rather than relying on a proprietary API. The AI industry has been dominated by US-based labs like OpenAI and Anthropic, but Chinese companies such as Moonshot AI have been rapidly closing the gap, raising questions about whether the US can maintain its technological lead.

**Tags**: `#AI`, `#LLM`, `#Kimi K3`, `#Distillation`, `#Open Weights`

---

<a id="item-4"></a>
## [Stack Overflow Activity Decline Visualized, Sparking Debate on AI and Other Causes](https://data.stackexchange.com/stackoverflow/query/1953768#graph) ⭐️ 8.0/10

A data visualization from Stack Exchange's data explorer shows a clear decline in Stack Overflow activity over time, prompting a high-engagement community discussion with 397 comments and 342 points. Commenters debate whether AI tools like ChatGPT, community policies, or the Prosus acquisition are the primary drivers of the decline. Stack Overflow has been a foundational resource for software developers for over a decade, and its decline signals a major shift in how developers seek and share knowledge. The multifaceted debate highlights that the platform's trajectory is likely not solely due to AI tools, but also stems from long-standing community dynamics and corporate decisions, offering lessons for other online communities. The graph shows that Stack Overflow activity actually peaked in 2014, well before AI tools like ChatGPT became prevalent, while the software engineering workforce grew significantly during the same period. Some commenters also note that a noticeable decline began after Stack Overflow was acquired by Prosus for $1.8 billion in 2021.

hackernews · secretslol · Jul 18, 11:12 · [Discussion](https://news.ycombinator.com/item?id=48956949)

**Background**: Stack Overflow is a question-and-answer website for programmers, historically one of the most visited sites on the internet for technical knowledge. The platform has been known for its strict moderation policies, which were designed to maintain quality but often created high barriers for new users. In 2021, the company was acquired by the European tech investor Prosus for $1.8 billion. The rise of AI chatbots like ChatGPT has provided developers with an alternative way to get coding help quickly and without the friction of community moderation.

**Discussion**: The community discussion reveals diverse viewpoints on the decline, with some arguing that Stack Overflow's hostile moderation and lack of community-building features killed the site long before AI. Others point out that activity peaked in 2014, a decade before ChatGPT, suggesting broader trends like improved documentation and issue trackers also played a role, while one commenter humorously noted that an LLM never made them feel stupid for asking a question.

**Tags**: `#stack-overflow`, `#ai-impact`, `#community-dynamics`, `#data-visualization`, `#developer-tools`

---

<a id="item-5"></a>
## [Meta Eyes $10B Compute Lease Deal with Anthropic](https://www.nytimes.com/2026/07/17/technology/meta-anthropic-ai-computing-power.html) ⭐️ 8.0/10

Meta is in early-stage talks to lease AI data center compute power to Anthropic in a potential two-year deal worth up to $10 billion, with Anthropic proposed the arrangement in June 2026 and payments structured on a monthly basis. Both parties would have the ability to exit the agreement early, though sources indicate negotiations remain preliminary and may not result in a final deal. This deal signals a major shift in how top-tier tech companies monetize and allocate AI infrastructure, with Meta leveraging its massive compute investments to generate revenue while addressing investor concerns over its enormous capital expenditures. It also underscores the severe scarcity of AI compute resources across the industry, forcing even well-funded startups like Anthropic to seek creative leasing arrangements rather than building their own infrastructure. Anthropic would pay monthly under the proposed structure, and both companies retain the right to exit the agreement early, suggesting flexibility amid uncertain long-term compute demand. Meta plans to invest up to $145 billion in 2026, with a significant portion allocated to AI and data center construction, making compute leasing a strategic way to offset these massive expenditures.

telegram · zaihuapd · Jul 18, 01:14

**Background**: Anthropic is an AI safety and research company founded in San Francisco, best known for its Claude series of large language models that compete with OpenAI's GPT. Meta has been aggressively expanding its AI infrastructure, with projected capital expenditures reaching up to $135-145 billion in 2026, including data center clusters spanning areas comparable to Manhattan. The broader industry is seeing a wave of compute leasing arrangements, with companies like Hyperscale Data and SpaceX also exploring or executing similar deals to meet surging demand for AI training and inference capacity.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Anthropic">Anthropic - Wikipedia</a></li>
<li><a href="https://entrepreneurloop.com/meta-anthropic-compute-deal-inside-the-10-billion-data-center-lease-talks/">Meta Anthropic Compute Deal: Inside the $10 Billion Data Center Lease Talks</a></li>
<li><a href="https://techxplore.com/news/2026-01-meta-ad-business-fuel-massive.html">Meta leans on improved ad business to fuel massive AI spending</a></li>

</ul>
</details>

**Tags**: `#Meta`, `#Anthropic`, `#AI Infrastructure`, `#Compute Leasing`, `#AI Industry`

---

<a id="item-6"></a>
## [SpaceX in Talks with Pentagon for Multi-Billion Dollar AI Computing Deal](https://www.wsj.com/tech/ai/spacex-in-talks-to-provide-computing-power-for-pentagons-ai-push-15e752e4) ⭐️ 8.0/10

SpaceX is negotiating with the U.S. Department of Defense to provide data center computing power for running AI models, in a deal potentially worth billions of dollars. Sources indicate that talks are ongoing and could still fall apart, but if successful, it would deepen SpaceX's relationship with the Pentagon. This deal signals SpaceX's strategic expansion beyond launch services and satellite internet into cloud computing and AI infrastructure for national security applications, positioning it as a competitor to established hyperscalers like Amazon, Google, and Microsoft. The reported scale of billions of dollars underscores the growing demand for AI computing power in defense and the increasing role of commercial space companies in military technology. The Pentagon has already approved SpaceX, along with Amazon, Google, Microsoft, and Oracle, to deploy AI models and related technologies in classified environments at Impact Level 6 and Impact Level 7. SpaceX has recently signed similar computing power agreements with Anthropic and Google, and has filed FCC plans to extend cloud and AI computing into orbit using millions of satellites.

telegram · zaihuapd · Jul 18, 01:44

**Background**: The Pentagon has been accelerating its acquisition of cloud computing capabilities to support AI applications across national security and daily military operations. It recently made agreements with eight companies, including SpaceX, OpenAI, Google, NVIDIA, Microsoft, Oracle, and Amazon Web Services, to deploy AI products in the Department of Defense's classified network environments. SpaceX has been building an AI infrastructure business through its Colossus data center, leasing cloud computing capacity to hyperscalers and AI startups, including a deal with Reflection AI worth up to $6.3 billion.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/06/22/spacex-ai-colossus-data-center-reflection.html">SpaceX signs computing power deal with open-source AI startup Reflection worth up to $6.3 billion</a></li>
<li><a href="https://www.nextgov.com/artificial-intelligence/2026/05/pentagon-makes-agreements-7-companies-add-ai-classified-networks/413264/">Pentagon makes agreements with 8 companies to add AI to classified networks - Nextgov/FCW</a></li>
<li><a href="https://www.fool.com/investing/2026/06/28/spacex-just-spent-60-billion-on-artificial-intelli/">SpaceX Just Spent $60 Billion on Artificial Intelligence (AI). Could Elon Musk Be Building the Next Amazon? | The Motley Fool</a></li>

</ul>
</details>

**Tags**: `#AI Infrastructure`, `#SpaceX`, `#Pentagon`, `#Cloud Computing`, `#National Security`

---

<a id="item-7"></a>
## [Kimi K3 Becomes First Open-Weight Model to Reach Top 3 on DeepSWE Benchmark](https://deepswe.datacurve.ai/blog/deepswe-v1-1) ⭐️ 8.0/10

On July 17, 2026, the DeepSWE AI coding agent benchmark updated its results, showing Kimi K3 debuting at 3rd place. Kimi K3 is the first open-weight model to approach frontier performance on this benchmark, with results close to proprietary models Claude Fable 5 and GPT-5.6 Sol. This milestone demonstrates that open-weight models are narrowing the gap with proprietary models in complex, long-horizon software engineering tasks. It signals growing accessibility of frontier-level coding agent capabilities to the broader developer community, potentially accelerating innovation in AI-assisted software development. Kimi K3 is a 2.8 trillion parameter model featuring Kimi Delta Attention, Attention Residuals, native vision, and a context window of up to 1,048,576 tokens. DeepSWE is designed as a contamination-free, long-horizon software engineering benchmark that reduces benchmark leakage, making it a more reliable measure of coding agent capabilities.

telegram · zaihuapd · Jul 18, 02:29

**Background**: DeepSWE is a long-horizon software engineering benchmark built to evaluate frontier coding agents on original, complex tasks that better reflect real-world software development. An open-weight model is an AI model whose trained parameters (weights) are publicly available for download, allowing users to run, study, and modify the model. Kimi K3, developed by Kimi, is the first open model to reach 2.8 trillion parameters, with full model weights scheduled for release by July 27, 2026.

<details><summary>References</summary>
<ul>
<li><a href="https://www.kimi.com/blog/kimi-k3">Kimi K 3 Tech Blog: Open Frontier Intelligence</a></li>
<li><a href="https://platform.kimi.ai/docs/guide/kimi-k3-quickstart">Kimi K 3 - Kimi API Platform</a></li>
<li><a href="https://deepswe.datacurve.ai/">DeepSWE measures frontier coding agents on original, long-horizon...</a></li>

</ul>
</details>

**Tags**: `#AI Agents`, `#Software Engineering`, `#Benchmark`, `#Open Source`, `#LLM`

---

<a id="item-8"></a>
## [TSMC A14 Process Progress Exceeds Expectations, Yield and Performance Near 90%](https://www.tomshardware.com/tech-industry/semiconductors/tsmc-confirms-significant-yield-and-performance-improvements-in-a14-update-strong-interest-from-ai-hpc-and-smartphone-customers) ⭐️ 8.0/10

TSMC reported in its earnings call that the A14 (1.4nm) process node has advanced rapidly over the past three months, with device performance approaching 90% of target levels and 256 Mb SRAM yields also nearing 90%, up from approximately 85% and 80% respectively in April 2024. CEO C.C. Wei revealed strong interest from smartphone, AI, and HPC customers, with new design tape-outs running ahead of schedule, and mass production targeted for the second half of 2028. The A14 node is TSMC's next full-node process after N2 and represents a critical milestone for the AI hardware and high-performance computing ecosystem, as improved yields and performance directly translate to better chip economics and capabilities. The accelerated timeline suggests TSMC is maintaining its technology leadership in advanced semiconductor manufacturing, which is strategically important for the global semiconductor supply chain and for companies designing next-generation AI accelerators and mobile processors. Compared to N2, A14 is expected to deliver 10-15% performance improvement at the same power, 25-30% power reduction at the same frequency, and 23% higher logic transistor density. A14 adopts second-generation GAA nanosheet transistors, allowing it to leverage experience accumulated from N2, which is a key reason its development progress significantly outpaces N2 at the same stage.

telegram · zaihuapd · Jul 18, 05:00

**Background**: TSMC's A14 is a 1.4nm-class process node and the company's next full-node advancement after N2 (2nm). GAA (Gate-All-Around) nanosheet transistors are a transistor architecture that replaces traditional FinFET structures at advanced nodes, offering better electrostatic control and continued scaling of Moore's Law. SRAM yield is a critical metric in semiconductor manufacturing because SRAM occupies a significant portion of modern chips—up to 60% in mobile SoCs and substantial portions in AI accelerators—making even small yield improvements economically significant. TSMC's roadmap also includes A13 (a density-focused shrink) and A12 (scheduled for 2029, adding backside power rail technology).

<details><summary>References</summary>
<ul>
<li><a href="https://wccftech.com/tsmc-1-4nm-process-faces-no-obstacles-as-risk-production-to-start-in-2027/">TSMC ’s Facing No Development Obstacles With Its Next-Generation...</a></li>
<li><a href="https://www.remio.ai/post/tsmc-raises-2026-capital-spending-to-60-64-billion-as-a14-stays-on-track">TSMC Raises 2026 Capital Spending to $60-$64 Billion as A 14 Stays...</a></li>
<li><a href="https://www.patsnap.com/resources/blog/articles/gaa-transistors-at-2nm-nanosheet-architecture-explained/">GAA transistors at 2nm: nanosheet architecture explained | PatSnap</a></li>

</ul>
</details>

**Tags**: `#semiconductors`, `#tsmc`, `#manufacturing`, `#ai-hardware`, `#process-node`

---

<a id="item-9"></a>
## [Trump Administration Eyes FINRA-Like Agency to Vet Top AI Models](https://www.bloomberg.com/news/articles/2026-07-17/us-considers-creating-finra-like-watchdog-to-vet-top-ai-models) ⭐️ 8.0/10

The Trump administration is considering establishing an independent AI oversight body modeled after FINRA to review the safety of top AI models, with the proposal currently under review by White House Chief of Staff Susie Wiles and led by Treasury Secretary Scott Bessent. The plan aims to give Wall Street and Silicon Valley a greater voice in jointly setting safety standards, responding to cybersecurity concerns and industry frustration with ad-hoc government restrictions. This signals a potential shift from ad-hoc government controls to a structured, industry-collaborative oversight model for AI safety, which could significantly impact how top AI models are deployed and governed in the United States. The proposal aligns with calls from major AI lab executives, including Google DeepMind CEO Demis Hassabis, and involves high-level officials, making it a pivotal development in U.S. AI regulatory policy. The proposed agency would report to the Securities and Exchange Commission (SEC) and be modeled on FINRA, a self-regulatory organization for the securities industry. The plan remains in draft form and has not yet been reviewed by President Trump, with the framework still subject to change; previously, both Anthropic and OpenAI clashed with the U.S. government over demands to modify or restrict the release of their latest models.

telegram · zaihuapd · Jul 18, 05:45

**Background**: FINRA (the Financial Industry Regulatory Authority) is a non-profit self-regulatory organization (SRO) that oversees brokerage firms and registered securities representatives in the United States, operating under SEC oversight. It was formed in 2007 through the consolidation of NASD and NYSE regulatory functions, and its model of industry-funded, industry-informed regulation is now being considered as a template for AI oversight. The proposal also comes amid growing tensions between AI companies and the government over safety restrictions, with Google DeepMind CEO Demis Hassabis recently calling for a U.S.-led, industry-funded AI safety watchdog to address risks associated with artificial general intelligence (AGI).

<details><summary>References</summary>
<ul>
<li><a href="https://baike.baidu.com/item/美国金融业监管局/9213493">美国金融业监管局_百度百科 FINRA Homepage About FINRA FINRA:监管、保护投资者与市场监督 美国FINRA：监管机构介绍、职能与查询方法-财经导航 - 专业的财经资讯... 什么是FINRA | 金融业监管局</a></li>
<li><a href="https://www.cnbc.com/2026/07/14/google-deepmind-demis-hassabis-us-led-ai-standards-body.html">Google DeepMind chief Demis Hassabis calls for U.S. to spearhead AI standards body</a></li>
<li><a href="https://www.inc.com/georgia-fearn/google-deepmind-founder-wall-street-style-watchdog-stop-dangerous-ai/91373798">Google DeepMind's Co-Founder Wants a Wall Street-Style Watchdog to Stop Dangerous AI</a></li>

</ul>
</details>

**Tags**: `#AI Regulation`, `#US Policy`, `#AI Safety`, `#Government`, `#Industry News`

---

<a id="item-10"></a>
## [US Seeks Share of Korean Chipmakers' AI Boom Profits](https://www.koreatimes.co.kr/business/tech-science/20260716/us-seeks-share-of-korean-chipmakers-excess-profits-source) ⭐️ 8.0/10

The US is reportedly seeking a share of the excess profits earned by Korean semiconductor companies from the global AI chip boom, with a US Deputy Trade Representative arguing that American procurement contributed to Korean firms' gains. South Korean officials have not confirmed this claim. This represents a novel and potentially paradigm-shifting trade policy stance where the US is demanding profit-sharing from allied nations' companies based on procurement contributions, which could reshape international trade relations and semiconductor supply chain economics. It directly affects major players like Samsung and SK Hynix and sets a precedent that may extend to other allied chipmakers. In the first half of this year, Korean semiconductor exports reached $192.43 billion, up 162.5% year-on-year, with exports to the US surging 91.3% to $26.4 billion. The US Commerce Secretary has also renewed calls for Samsung and SK Hynix to build memory chip factories in the US, while South Korea is domestically debating whether chipmakers should share excess profits with subcontractors and the public.

telegram · zaihuapd · Jul 18, 14:20

**Background**: The US CHIPS Act has provided subsidies to foreign semiconductor companies building facilities in the US, with SK Hynix securing $450 million for its $3.87 billion Indiana HBM packaging plant and Samsung negotiating subsidies for its Taylor, Texas fab. The Biden-era CHIPS Act included 'guardrails' such as China investment restrictions and profit-sharing provisions, which the Trump administration has since modified by transferring CHIPS operations to the US Investment Accelerator. The global AI chip boom, driven by demand for high-bandwidth memory (HBM) used in AI accelerators, has disproportionately benefited Korean chipmakers who dominate this market segment. This profit-sharing demand comes amid broader US efforts to onshore semiconductor manufacturing and reduce dependence on foreign supply chains.

**Tags**: `#semiconductors`, `#geopolitics`, `#trade-policy`, `#AI-chips`, `#Samsung`

---
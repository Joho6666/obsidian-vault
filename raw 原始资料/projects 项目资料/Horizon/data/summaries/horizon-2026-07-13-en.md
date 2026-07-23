# Horizon Daily - 2026-07-13

> From 41 items, 27 important content pieces were selected

---

1. [Migrating AI Agent to GPT-5.6: 2.2x Faster, 27% Cheaper](#item-1) ⭐️ 8.0/10
2. [Claude Code uses 33k tokens vs OpenCode's 7k per task](#item-2) ⭐️ 8.0/10
3. [AI Automation Risks Eroding Human Expertise](#item-3) ⭐️ 8.0/10
4. [Causality Theory Applied to Understand LLM Reasoning](#item-4) ⭐️ 8.0/10
5. [LLMs Create Value, But Frontier Labs May Not Capture It](#item-5) ⭐️ 8.0/10
6. [Terry Tao Explores Building Apps with Modern Coding Agents](#item-6) ⭐️ 8.0/10
7. [Shingles vaccine may reduce dementia risk](#item-7) ⭐️ 8.0/10
8. [Unauthenticated RCE Found in Motorola MR2600 Router](#item-8) ⭐️ 8.0/10
9. [AI Boosts Research Productivity but Narrows Ideas](#item-9) ⭐️ 8.0/10
10. [HN User Proposes Flag for AI-Generated Articles](#item-10) ⭐️ 7.0/10
11. [Pin-Level Emulation for 8-Bit Computers](#item-11) ⭐️ 7.0/10
12. [Google Study: Smarter Routing Can Reduce Traffic Congestion](#item-12) ⭐️ 7.0/10
13. [Against Usefulness: Reclaiming Computing for Play](#item-13) ⭐️ 7.0/10
14. [Ghostel.el: Fast Emacs Terminal Emulator via libghostty](#item-14) ⭐️ 7.0/10
15. [Film CGI vs. AI: A Parallel for Software Engineering](#item-15) ⭐️ 7.0/10
16. [Odin Programming Language Gains Traction](#item-16) ⭐️ 7.0/10
17. [Chromium 148 Math.tanh Enables OS Fingerprinting](#item-17) ⭐️ 7.0/10
18. [LLM Agents Should Never Be DRIs](#item-18) ⭐️ 7.0/10
19. [First PCB Design and Assembly Journey](#item-19) ⭐️ 6.0/10
20. [Regaining Deep Reading After Screen Addiction](#item-20) ⭐️ 6.0/10
21. [Death of the Status Update: 55% of Americans Stop Posting](#item-21) ⭐️ 6.0/10
22. [Anthropic Extends Claude Fable 5 Access Again](#item-22) ⭐️ 6.0/10
23. [CGI Motion Capture with Only a Camera](#item-23) ⭐️ 6.0/10
24. [1964 AI Predictions Still Resonate Today](#item-24) ⭐️ 6.0/10
25. [Porting Nvidia GPU Driver to Haiku for 3D Acceleration](#item-25) ⭐️ 6.0/10
26. [Silent Speech via Ultrasound Probe](#item-26) ⭐️ 6.0/10
27. [Laser-Guided Fungal Art: Merging Biology and Digital Fabrication](#item-27) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Migrating AI Agent to GPT-5.6: 2.2x Faster, 27% Cheaper](https://ploy.ai/blog/migrating-a-production-ai-agent-to-gpt-5-6) ⭐️ 8.0/10

A production AI agent that builds marketing websites was migrated to OpenAI's GPT-5.6, resulting in a 2.2x speed increase and a 27% cost reduction. The migration also required a schema transform fix to handle optional properties in OpenAI-family models. This demonstrates significant performance and cost benefits from upgrading to a newer LLM, with concrete metrics that can guide other teams considering similar migrations. The schema transform workaround addresses a common pain point in structured output generation, making the upgrade more practical for production use. The agent plans pages, reads codebases, writes components, generates imagery, and screenshots its own work. The schema fix rewrites every optional property as required but nullable using anyOf: [T, null], giving the model an explicit way to indicate absence.

hackernews · brryant · Jul 12, 17:13 · [Discussion](https://news.ycombinator.com/item?id=48882716)

**Background**: GPT-5.6 is a large language model released by OpenAI on July 9, 2026, with variants Luna, Terra, and Sol. It is designed to enhance capabilities in enterprise work, coding, scientific research, and cybersecurity. The migration involved switching from an earlier model (likely Opus 4.7/4.8) to GPT-5.6.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GPT-5.6">GPT-5.6</a></li>
<li><a href="https://openai.com/index/previewing-gpt-5-6-sol/">Previewing GPT‑5.6 Sol: a next-generation model - OpenAI</a></li>

</ul>
</details>

**Discussion**: Commenters noted similar improvements in their own workflows and appreciated the concrete metrics. Some criticized the LLM-like writing style of the article, while others discussed the schema transform approach, questioning its necessity and correctness.

**Tags**: `#AI`, `#LLM`, `#production`, `#cost optimization`, `#schema design`

---

<a id="item-2"></a>
## [Claude Code uses 33k tokens vs OpenCode's 7k per task](https://systima.ai/blog/claude-code-vs-opencode-token-overhead) ⭐️ 8.0/10

A systematic study found that Claude Code sends approximately 33,000 tokens before reading the user's prompt, while OpenCode sends only about 7,000 tokens for the same tasks, revealing a significant difference in token overhead. This token inefficiency directly translates to higher costs for users and raises concerns about the design incentives of AI coding tools, potentially influencing developer tooling choices and industry standards for efficiency. The study measured all requests between the coding tools and Anthropic's endpoint, finding that Claude Code's cache strategy and harness token usage are far less efficient than OpenCode's. The author plans to follow up with deeper task analysis and qualitative comparisons.

hackernews · systima · Jul 12, 18:25 · [Discussion](https://news.ycombinator.com/item?id=48883275)

**Background**: AI coding tools like Claude Code and OpenCode act as agentic harnesses that send system prompts, tool definitions, and context to large language models. Token usage directly impacts cost and performance, as users are billed per token. Efficient token management is critical for practical adoption.

<details><summary>References</summary>
<ul>
<li><a href="https://asibiont.com/en/blog/claude-code-otpravlyaet-33k-tokenov-do-chteniya-prompta-pochemu-opencode-s-7k-tokenami-effektivnee-dlya-vibe-coding">Claude Code Sends 33k Tokens Before Reading... — ASI Biont Blog</a></li>
<li><a href="https://www.neura.market/blog/claude-code-sends-33k-tokens-before-reading-your-prompt-opencode-sends">Claude Code Sends 33K Tokens Before Reading Your... | Neura Market</a></li>

</ul>
</details>

**Discussion**: Community comments highlight frustration with sub-agent token waste and suspicion that Anthropic may intentionally inflate token usage for profit. Some users call for more qualitative comparisons and note that tokenflation is a broader trend across coding agents.

**Tags**: `#AI coding tools`, `#token efficiency`, `#Claude Code`, `#OpenCode`, `#cost analysis`

---

<a id="item-3"></a>
## [AI Automation Risks Eroding Human Expertise](https://arxiv.org/abs/2607.06377) ⭐️ 8.0/10

A paper titled 'Automation Without Understanding' warns that AI automation may reduce the number of experts capable of detecting AI errors, emphasizing the need for transparency and explainability. This discussion highlights a critical risk: as AI systems become more capable, we may lose the human expertise needed to catch their mistakes, potentially leading to widespread reliance on unreliable AI. The paper scores 8.0/10 with 109 points and 47 comments, indicating strong community engagement. Key comments warn that AI could stop producing people who know enough to notice when AI is confidently wrong.

hackernews · root-parent · Jul 12, 16:54 · [Discussion](https://news.ycombinator.com/item?id=48882554)

**Background**: The paper discusses the concept of 'automation without understanding,' where AI systems automate tasks without providing insight into their reasoning. This can lead to a decline in human expertise as people rely on AI outputs without critical evaluation.

**Discussion**: Commenters express concern that AI automation may reduce the number of experts who can detect errors. Some suggest AI should be forced to show its work, such as producing proofs or execution traces, to maintain accountability.

**Tags**: `#AI safety`, `#explainability`, `#expertise`, `#automation`, `#epistemology`

---

<a id="item-4"></a>
## [Causality Theory Applied to Understand LLM Reasoning](https://cacm.acm.org/news/can-we-understand-how-large-language-models-reason/) ⭐️ 8.0/10

Researchers are applying causality theory to mechanistic interpretability of large language models, analyzing weights and activations to understand how models reason, as discussed in a recent paper and community debate. This approach could lead to deeper understanding of LLM internal mechanisms, improving AI safety and trustworthiness by revealing whether models truly reason or merely pattern-match. The paper linked (arXiv:2301.04709) explores causal interventions on model components, such as tweaking weights and activations, to test for reasoning-like behavior, with an example involving clock time calculations.

hackernews · adunk · Jul 12, 18:04 · [Discussion](https://news.ycombinator.com/item?id=48883090)

**Background**: Mechanistic interpretability is a subfield of explainable AI that reverse-engineers neural networks to understand their internal algorithms and circuits. Causality theory, popularized by Judea Pearl, provides tools to infer cause-effect relationships, which researchers now apply to probe whether LLMs use genuine reasoning or statistical correlations.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mechanistic_interpretability">Mechanistic interpretability - Wikipedia</a></li>
<li><a href="https://arxiv.org/abs/2501.16496">[2501.16496] Open Problems in Mechanistic Interpretability</a></li>
<li><a href="https://medium.com/@alexglee/causal-ai-current-state-of-the-art-future-directions-c17ad57ff879">Causal AI: Current State-of-the-Art & Future Directions The Role of Causality in Explainable Artificial Intelligence The Role of Causality in Explainable Artificial Intelligence Causal AI: Beyond Correlation to Real Understanding Causality for Artificial Intelligence: From a Philosophical ... Causality and Machine Learning - Microsoft Research</a></li>

</ul>
</details>

**Discussion**: Community comments highlight that the article focuses on mechanistic interpretability rather than philosophical reasoning, with some skepticism about whether weight-level analysis can distinguish reasoning from hallucination. One commenter suggests that neural networks' complexity inherently resists understanding, analogous to encrypted black boxes.

**Tags**: `#mechanistic interpretability`, `#LLMs`, `#causality`, `#AI research`, `#reasoning`

---

<a id="item-5"></a>
## [LLMs Create Value, But Frontier Labs May Not Capture It](https://geohot.github.io//blog/jekyll/update/2026/07/12/i-love-llms.html) ⭐️ 8.0/10

A critical analysis argues that while LLMs generate significant value, frontier AI labs may fail to capture that value due to commoditization and open-source competition. This challenges the high valuations of frontier labs and suggests that value will flow to applications and tooling rather than model providers, reshaping investment and open-source dynamics. The author bets against ASI timelines and notes that productivity gains from LLMs have not yet translated into visible new software, as much innovation happens privately in homelabs.

hackernews · therepanic · Jul 12, 18:31 · [Discussion](https://news.ycombinator.com/item?id=48883343)

**Background**: Frontier labs like OpenAI and Anthropic invest billions in training large language models, but face pressure from open-source alternatives and commoditizing inference costs. The economic debate centers on whether model providers or downstream applications will capture the most value.

<details><summary>References</summary>
<ul>
<li><a href="https://www.amadeuscapital.com/ai-commoditisation-curve/">Charting the AI commoditisation curve: Where will LLM value flow next?</a></li>
<li><a href="https://www.linkedin.com/pulse/ai-productivity-trap-how-frontier-labs-cannibalising-both-tze-weng-ng-ekjmc">The AI Productivity Trap: How Frontier AI Labs Are Cannibalising...</a></li>

</ul>
</details>

**Discussion**: Commenters largely agree with the value capture argument, noting that open-source models enable private, customized software, reducing incentives to upstream contributions. Some see recent model improvements (e.g., Sonnet 4, Opus 4.5) as accelerating progress, while others remain skeptical about near-term AGI.

**Tags**: `#LLMs`, `#AI hype`, `#open source`, `#productivity`, `#economics`

---

<a id="item-6"></a>
## [Terry Tao Explores Building Apps with Modern Coding Agents](https://terrytao.wordpress.com/2026/07/11/old-and-new-apps-via-modern-coding-agents/) ⭐️ 8.0/10

Terry Tao, a Fields Medalist, documented his experience using modern coding agents (LLM-based tools) to build both old and new applications, sharing practical examples and a balanced perspective on their capabilities and limitations. This demonstrates that even top mathematicians are adopting LLM-assisted programming, signaling a shift in software development practices. It highlights the growing accessibility of AI tools for non-professional programmers and the potential to unlock latent demand for custom software. Tao used coding agents to create interactive visualizations and other apps, noting that while the agents are not mission-critical for core research, they are acceptable for supplementary tools. He emphasized the importance of understanding the limitations of LLM-generated code.

hackernews · subset · Jul 12, 11:09 · [Discussion](https://news.ycombinator.com/item?id=48880170)

**Background**: Coding agents are AI tools that wrap large language models (LLMs) in an application layer to assist with programming tasks, such as generating code, debugging, and creating visualizations. They have gained popularity as LLMs like GPT-4 and Claude have improved, enabling even non-experts to build software quickly. However, they can produce unreliable code and require careful oversight.

<details><summary>References</summary>
<ul>
<li><a href="https://magazine.sebastianraschka.com/p/components-of-a-coding-agent">Components of A Coding Agent - by Sebastian Raschka, PhD</a></li>
<li><a href="https://simonwillison.net/2025/Mar/11/using-llms-for-code/">Here’s how I use LLMs to help me write code</a></li>

</ul>
</details>

**Discussion**: Commenters expressed a mix of excitement and humor, with some noting that LLMs have enabled them to build visualizations they always wanted but lacked time for. Others joked about Fields Medalists facing the same Docker struggles as everyone else, while appreciating Tao's balanced take on the tool's strengths and weaknesses.

**Tags**: `#LLM`, `#coding agents`, `#software development`, `#AI-assisted programming`

---

<a id="item-7"></a>
## [Shingles vaccine may reduce dementia risk](https://www.economist.com/leaders/2026/07/09/a-no-brainer-for-protecting-your-brain) ⭐️ 8.0/10

Observational studies from the UK, Australia, and Canada suggest that the shingles vaccine (Shingrix) is associated with a 1.8% to 3.5% absolute reduction in dementia diagnoses over 5.5 to 7 years. If causal, this would offer a safe, widely available intervention to reduce dementia burden, affecting millions globally. It also opens new avenues for understanding infection-driven neurodegeneration. The association is strongest with the live zoster vaccine (Zostavax) but also seen with recombinant Shingrix. Critics argue the effect may be due to healthy vaccinee bias or reduced hospital visits leading to fewer incidental dementia diagnoses.

hackernews · saikatsg · Jul 12, 15:23 · [Discussion](https://news.ycombinator.com/item?id=48881874)

**Background**: Shingles is caused by reactivation of the varicella-zoster virus, which also causes chickenpox. Dementia, particularly Alzheimer's disease, is a growing public health challenge with limited preventive options. Previous research has linked various infections to increased dementia risk, suggesting a potential role for vaccines in reducing that risk.

**Discussion**: Commenters debated causality: some highlighted a compelling UK study with a hard age cutoff, while others pointed to a presentation arguing the finding is spurious due to detection bias. Personal anecdotes about paying out of pocket for the vaccine were also shared.

**Tags**: `#vaccine`, `#dementia`, `#public health`, `#epidemiology`, `#Alzheimer's`

---

<a id="item-8"></a>
## [Unauthenticated RCE Found in Motorola MR2600 Router](https://mrbruh.com/motorola/) ⭐️ 8.0/10

A security researcher disclosed an unauthenticated remote code execution vulnerability in the Motorola MR2600 router, with 42 exposed hosts identified and the vendor unresponsive. This vulnerability poses a high risk of active exploitation, potentially allowing attackers to fully compromise affected routers and use them for malicious activities. The vulnerability is accessible via an insecure HTTP endpoint, and the router's firmware update mechanism appears to be abandoned, leaving no official patch available.

hackernews · MrBruh · Jul 12, 11:52 · [Discussion](https://news.ycombinator.com/item?id=48880406)

**Background**: The Motorola MR2600 is a dual-band AC2600 WiFi router. However, the brand 'Motorola' on this router is licensed; the actual manufacturer is Zoom, which went bankrupt in 2023, and its assets were bought by e2Companies in 2024. This complex ownership history explains the vendor's unresponsiveness.

<details><summary>References</summary>
<ul>
<li><a href="https://www.homeowner.com/connectivity/motorola/motorola-mr2600-review">Motorola MR 2600 (AC2600) Review: Best Home WiFi Router ?</a></li>
<li><a href="https://www.modemguides.com/products/motorola-mr2600">Motorola MR 2600 Dual-Band AC2600 Wireless Router</a></li>
<li><a href="https://www.newegg.com/p/3C6-0129-00035">Motorola AC2600 4x4 WiFi Smart Gigabit Router with... - Newegg.com</a></li>

</ul>
</details>

**Discussion**: Commenters noted legal implications in Germany under 'Störerhaftung' and suggested white hats might consider patching exposed hosts themselves. Others clarified the convoluted vendor history, explaining why the vendor is unresponsive.

**Tags**: `#security`, `#vulnerability`, `#IoT`, `#RCE`, `#networking`

---

<a id="item-9"></a>
## [AI Boosts Research Productivity but Narrows Ideas](https://spectrum.ieee.org/ai-science-research-flattens-discovery) ⭐️ 8.0/10

A new study reveals that scientists who adopt AI publish three times as many papers, receive nearly five times as many citations, and become team leaders earlier, but the range of scientific ideas explored narrows. This finding highlights a critical trade-off in AI-assisted research: while AI boosts individual productivity and career advancement, it may reduce intellectual diversity and the breadth of scientific discovery. The study found that AI-adopting researchers cluster on similar topics, leading to a flattening of the idea landscape. The effect is attributed more to incentives in the research system than to AI architecture itself.

hackernews · zaikunzhang · Jul 12, 13:26 · [Discussion](https://news.ycombinator.com/item?id=48881043)

**Background**: The study examines the impact of AI on scientific research, focusing on productivity metrics and the diversity of ideas. The 'Babble hypothesis' suggests that researchers may prioritize publication quantity over originality, and AI may amplify this tendency.

**Discussion**: Commenters largely agree that AI amplifies existing incentives in research, with many pointing to the 'Babble hypothesis' and systemic pressures to publish. Some question whether less original work was already receiving more citations before AI adoption, suggesting broader network effects.

**Tags**: `#AI`, `#research`, `#science policy`, `#incentives`, `#productivity`

---

<a id="item-10"></a>
## [HN User Proposes Flag for AI-Generated Articles](https://news.ycombinator.com/item?id=48886741) ⭐️ 7.0/10

A Hacker News user proposed adding a flag to indicate AI-generated articles, allowing readers to skip them without affecting ranking. The suggestion sparked a community debate on moderation and the role of AI content. This proposal addresses growing concerns about AI-generated content quality and authenticity on social platforms. If implemented, it could influence how other communities handle AI content and set a precedent for transparency. The flag would not de-rank articles but serve as an indicator for users who prefer human-written content. Open questions include whether the voting system suffices and if HN should adapt to the generative AI era.

hackernews · levkk · Jul 13, 01:24

**Background**: Hacker News (HN) is a social news website focused on computer science and entrepreneurship, known for its strict moderation and community-driven content ranking. The site already prohibits AI-generated text in comments but has no rule for articles. The proposal reflects a broader debate on how platforms should handle AI-generated content.

**Discussion**: Community members expressed mixed views: some argued that content quality matters more than origin, while others raised concerns about false positives and bad-faith accusations. Dang, an HN moderator, noted that the community generally discounts AI-generated articles but enforcement remains challenging.

**Tags**: `#AI`, `#moderation`, `#Hacker News`, `#content policy`

---

<a id="item-11"></a>
## [Pin-Level Emulation for 8-Bit Computers](https://floooh.github.io/tiny8bit-preview/index.html) ⭐️ 7.0/10

A collection of tiny emulators for 8-bit computers has been released, using a pin-level emulation model that enables fast loading and accurate simulation. This novel approach to retro computing emulation offers higher accuracy and flexibility than traditional emulators, potentially setting a new standard for hardware simulation in the browser via WebAssembly. The emulators are built with WebAssembly, allowing them to run in a web browser with near-native performance. The pin-level model simulates individual chip pins and their timing, enabling cycle-accurate behavior.

hackernews · naves · Jul 12, 20:23 · [Discussion](https://news.ycombinator.com/item?id=48884395)

**Background**: Traditional emulators often use higher-level abstractions, sacrificing some accuracy for speed. Pin-level emulation models the exact electrical connections between components, providing more faithful reproduction of original hardware behavior. This technique is commonly used in hardware design verification but is rare in retro computing emulation.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Hardware_emulation">Hardware emulation - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/List_of_computer_system_emulators">List of computer system emulators - Wikipedia</a></li>
<li><a href="https://dev.to/frqan/building-a-ti-84-plus-ce-emulator-in-webassembly-lessons-from-100-browser-based-calculator-3mlg">Building a TI-84 Plus CE Emulator in WebAssembly : Lessons from...</a></li>

</ul>
</details>

**Discussion**: Commenters praised the pin-level model for its modular flexibility and fast loading times, with one user recalling how loading games from tape used to take ages. Some requested support for additional systems like the Oric and Commodore 64, while another noted that some emulators have unexpectedly high volume levels.

**Tags**: `#emulation`, `#retrocomputing`, `#hardware simulation`, `#webassembly`

---

<a id="item-12"></a>
## [Google Study: Smarter Routing Can Reduce Traffic Congestion](https://research.google/blog/the-power-of-collaboration-how-we-can-reduce-traffic-congestion/) ⭐️ 7.0/10

Google conducted a six-month city-wide experiment where Google Maps routing was modified to prefer alternative routes with similar travel times, effectively distributing traffic away from congested segments. The study found that this intervention reduced congestion without significantly increasing travel times for individual drivers. This research demonstrates that small algorithmic tweaks to navigation apps can have a measurable impact on urban traffic congestion, offering a low-cost, scalable solution. However, it also highlights the need to consider infrastructure wear and systemic urban planning, as redistributing traffic may accelerate road damage on less hardy routes. The experiment used a city-wide switchback (crossover) design, alternating between the modified and unaltered routing algorithms on consecutive days over six months. The modified algorithm guided trips away from pre-selected congested segments while keeping travel times similar, but community commenters noted that roads are built to different standards and increased traffic on detour routes can lead to faster deterioration.

hackernews · raahelb · Jul 12, 15:35 · [Discussion](https://news.ycombinator.com/item?id=48881967)

**Background**: Traffic congestion is a major urban problem, and navigation apps like Google Maps typically route drivers along the fastest path, which can concentrate traffic on certain roads. This study explores an alternative approach: instead of optimizing for each individual driver's fastest route, the algorithm aims to balance traffic across the network. The concept is similar to load balancing in computer networks, where traffic is distributed to avoid overloading any single path.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Routing">Routing - Wikipedia</a></li>
<li><a href="https://arxiv.org/html/2402.15749v1">A summary of the routing algorithm and their optimization,performance</a></li>
<li><a href="https://scrap.io/google-maps-route-planning-technology-20-years">Google Maps Route Planning in 2026: The Technology Behind 2 Billion Daily Navigations | Scrap.io</a></li>

</ul>
</details>

**Discussion**: Community comments raised several concerns: some argued that the root cause of congestion is urban sprawl and lack of mixed-use communities, not routing algorithms. Others pointed out that roads are built to different standards, so diverting traffic onto less hardy roads can cause rapid deterioration and unexpected repair costs. A few commenters suggested that congestion pricing or improved public transit would be more effective solutions.

**Tags**: `#traffic congestion`, `#Google Maps`, `#routing algorithms`, `#urban planning`, `#experimental design`

---

<a id="item-13"></a>
## [Against Usefulness: Reclaiming Computing for Play](https://www.motivenotes.ai/p/against-usefulness) ⭐️ 7.0/10

A new article critiques the tech industry's obsession with 'usefulness' and advocates for reclaiming computing as a medium for exploration and play, inspired by Bret Victor's Dynamicland project. This philosophical critique challenges the dominant productivity-focused paradigm in computing, potentially influencing how developers and designers approach human-computer interaction and creativity tools. The article references Dynamicland, a lab by Bret Victor in Oakland, and mentions the Folk Computer project in New York as another alternative computing paradigm. It scored 7.0/10 on the news aggregator with 98 points and 24 comments.

hackernews · supo · Jul 12, 17:47 · [Discussion](https://news.ycombinator.com/item?id=48882956)

**Background**: Bret Victor is a well-known researcher in human-computer interaction, famous for his work on dynamic, explorable media like 'Inventing on Principle'. Dynamicland is a research lab that explores collaborative, physical computing environments where people interact with information using tangible objects, rather than screens and keyboards.

<details><summary>References</summary>
<ul>
<li><a href="https://cognitivemedium.com/emm/emm.html">Toward an exploratory medium for mathematics</a></li>

</ul>
</details>

**Discussion**: Commenters expressed interest in alternative computing paradigms, with one noting the potential for tactile mission planning, another advocating for digitized stylus input, and a third seeking collaborators for physical computing in education.

**Tags**: `#computing philosophy`, `#human-computer interaction`, `#Dynamicland`, `#creativity`, `#technology critique`

---

<a id="item-14"></a>
## [Ghostel.el: Fast Emacs Terminal Emulator via libghostty](https://dakra.github.io/ghostel/) ⭐️ 7.0/10

Ghostel.el is a new terminal emulator for Emacs that uses libghostty-vt for terminal state management, offering faster performance and more reliable input handling compared to vterm and eat. This brings the performance benefits of the Ghostty terminal emulator to Emacs users, enabling smoother operation of TUI applications and a better overall terminal experience within Emacs. Ghostel is built on libghostty-vt, a zero-dependency library extracted from Ghostty's core. It currently has some rough edges, such as occasional terminal clearing failures and freezes that require killing the buffer.

hackernews · signa11 · Jul 12, 08:52 · [Discussion](https://news.ycombinator.com/item?id=48879504)

**Background**: Ghostty is a fast, feature-rich, cross-platform terminal emulator using GPU acceleration and native UI. libghostty is a C-compatible library that allows embedding Ghostty's terminal emulation in other applications, with libghostty-vt being the first component for parsing terminal sequences and maintaining state.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/Uzaaft/awesome-libghostty">GitHub - Uzaaft/awesome-libghostty</a></li>
<li><a href="https://mitchellh.com/writing/libghostty-is-coming">Libghostty Is Coming – Mitchell Hashimoto</a></li>
<li><a href="https://docsmith.aigne.io/docs/ghostty/en/libghostty-ed730d">libghostty API</a></li>

</ul>
</details>

**Discussion**: Users report that Ghostel is noticeably faster and more reliable than vterm, with a nicer ELisp API, but some have encountered occasional clearing issues and freezes. The maintainer confirms the project is still in early stages and plans a Show HN soon.

**Tags**: `#Emacs`, `#terminal emulator`, `#libghostty`, `#open source`, `#performance`

---

<a id="item-15"></a>
## [Film CGI vs. AI: A Parallel for Software Engineering](https://fabiensanglard.net/extinct/index.html) ⭐️ 7.0/10

Fabien Sanglard published an article drawing a parallel between the film industry's shift from practical effects to CGI and software engineering's adoption of LLMs, arguing that AI will devalue traditional skills but those who adapt will thrive. This analogy provides a historical lens to understand the potential long-term impact of LLMs on software engineering, highlighting risks of skill devaluation and the importance of adaptation, which resonates with ongoing debates about AI's role in the industry. The article notes that CGI became dominant partly because digital VFX houses are non-unionized, allowing cost-cutting at the expense of artist welfare, and that a similar dynamic may occur with LLMs in software. It also acknowledges that practical effects are seeing a resurgence as audiences recognize their superior quality.

hackernews · zdw · Jul 12, 15:17 · [Discussion](https://news.ycombinator.com/item?id=48881830)

**Background**: CGI (Computer-Generated Imagery) replaced many practical effects in film due to lower costs and faster turnaround, but often at the cost of artist working conditions and perceived quality. Similarly, LLMs (Large Language Models) like GPT-4 are being adopted in software engineering to boost productivity, raising concerns about skill devaluation and job displacement.

<details><summary>References</summary>
<ul>
<li><a href="https://www.lafilm.edu/blog/practical-effects-vs-cgi-2/">Practical Effects vs. CGI | The Los Angeles Film School</a></li>
<li><a href="https://www.lafilm.edu/blog/practical-effects-vs-cgi/">Practical Effects vs CGI – The Los Angeles Film School</a></li>
<li><a href="https://berkeleyhighjacket.com/2023/entertainment/cgi-vs-practical-effects-impacts-on-the-authenticity-of-film">CGI vs. practical effects: Impacts on the authenticity of film | The Berkeley High Jacket</a></li>

</ul>
</details>

**Discussion**: Commenters debated the analogy's depth, noting that CGI's rise was fueled by non-unionized labor and poor treatment of artists, and that a similar dynamic could occur with LLMs. Some questioned the productivity argument, stating that volume is rarely a key evaluation metric in software engineering, while others emphasized the importance of learning LLMs without over-relying on them.

**Tags**: `#AI`, `#software engineering`, `#labor`, `#LLM`, `#analogy`

---

<a id="item-16"></a>
## [Odin Programming Language Gains Traction](https://odinbook.com/) ⭐️ 7.0/10

A new book and community discussion highlight Odin as a performant, low-overhead systems language with excellent C interop, appealing to developers seeking alternatives to Rust and Zig. Odin offers a simpler, more explicit alternative to Rust and Zig for systems programming, potentially broadening the ecosystem and attracting developers who find other languages overly complex. Odin was created by Bill Hall (Ginger Bill) starting in 2016, and its design goals include explicitness, performance, and data-oriented programming. The language has been used for STM32 firmware, web, and desktop applications.

hackernews · AlexeyBrin · Jul 12, 12:08 · [Discussion](https://news.ycombinator.com/item?id=48880499)

**Background**: Odin is a general-purpose systems programming language with distinct typing, built for high performance and modern systems. It competes with languages like Rust and Zig, which also emphasize safety and performance but have steeper learning curves.

<details><summary>References</summary>
<ul>
<li><a href="https://odin-lang.org/">Odin Programming Language</a></li>
<li><a href="https://grokipedia.com/page/Odin_programming_language">Odin (programming language)</a></li>

</ul>
</details>

**Discussion**: Community members praise Odin's ease of use, fast compilation, and excellent C interop, with one user noting it is even less overhead than Zig. Some wish for first-class inheritance support, but overall sentiment is positive.

**Tags**: `#programming languages`, `#systems programming`, `#Odin`, `#C interop`, `#performance`

---

<a id="item-17"></a>
## [Chromium 148 Math.tanh Enables OS Fingerprinting](https://scrapfly.dev/posts/browser-math-os-fingerprint/) ⭐️ 7.0/10

Since Chromium 148, the implementation of Math.tanh varies across operating systems, allowing a single call to reveal the underlying OS. This creates a new browser fingerprinting vector that can link a user to their operating system. This discovery expands the toolkit for browser fingerprinting, potentially undermining privacy protections even when users spoof their User-Agent. It highlights the ongoing arms race between tracking techniques and privacy measures, affecting all web users. The fingerprint works because different OS math libraries produce slightly different results for Math.tanh on certain inputs. The technique is reliable enough to distinguish between macOS, Linux, and Windows, and may also indicate the browser version range.

hackernews · joahnn_s · Jul 12, 21:12 · [Discussion](https://news.ycombinator.com/item?id=48884853)

**Background**: Browser fingerprinting collects device-specific information (e.g., screen resolution, fonts, installed plugins) to identify users without cookies. Math.tanh is a hyperbolic tangent function implemented by the browser's JavaScript engine, which delegates to the underlying OS math library. Differences in floating-point precision or rounding across OSes create detectable signatures.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Browser_fingerprinting">Browser fingerprinting</a></li>
<li><a href="https://learn.microsoft.com/en-us/dotnet/api/system.math.tanh?view=net-10.0">Math.Tanh (Double) Method (System) | Microsoft Learn</a></li>
<li><a href="https://fingerprint.com/blog/browser-fingerprinting-techniques/">Browser Fingerprinting Techniques: 6 Top Methods Explained</a></li>

</ul>
</details>

**Discussion**: Commenters noted that the fingerprint may also reveal browser version range, and some criticized the article as likely AI-generated, questioning its motives. Others called for correctly rounded math functions to eliminate such side-channel leaks, while one joked that even emoji rendering time could become a fingerprint.

**Tags**: `#browser fingerprinting`, `#privacy`, `#Chromium`, `#JavaScript`, `#security`

---

<a id="item-18"></a>
## [LLM Agents Should Never Be DRIs](https://simonwillison.net/2026/Jul/12/directly-responsible-individuals/#atom-everything) ⭐️ 7.0/10

Simon Willison argues that LLM-powered agents should never be designated as Directly Responsible Individuals (DRIs) because they cannot take accountability, drawing on the DRI concept from Apple and GitLab. This matters because as LLM agents are increasingly deployed in organizations, clarifying that accountability must remain with humans prevents diffusion of responsibility and ensures ethical oversight. The DRI concept originated at Apple and is defined in the GitLab handbook as the person ultimately accountable for a project's success or failure. Willison cites IBM's 1979 training slide stating that a computer can never be held accountable.

rss · Simon Willison · Jul 12, 23:57

**Background**: A Directly Responsible Individual (DRI) is a single person assigned unambiguous accountability for a task, decision, or outcome, a practice popularized by Apple to reduce ambiguity. LLM-powered agents are AI systems that can autonomously perform tasks, but they lack the capacity for moral or legal accountability.

<details><summary>References</summary>
<ul>
<li><a href="https://handbook.gitlab.com/handbook/people-group/directly-responsible-individuals/">Directly Responsible Individuals (DRI) - The GitLab Handbook</a></li>

</ul>
</details>

**Tags**: `#organizational culture`, `#accountability`, `#LLM agents`, `#software engineering`

---

<a id="item-19"></a>
## [First PCB Design and Assembly Journey](https://vilkeliskis.com/b/2026/0711.html) ⭐️ 6.0/10

A personal blog post details the author's experience designing and assembling their first printed circuit board (PCB), noting the low cost and accessibility of custom manufacturing services. This highlights how affordable custom PCB fabrication has become, enabling hobbyists and professionals to prototype hardware easily, which fosters innovation in electronics. The author used a simple design with through-hole components and ordered the board from a Chinese manufacturer like JLCPCB, which offers low-cost prototyping with fast turnaround.

hackernews · tadasv · Jul 12, 22:56 · [Discussion](https://news.ycombinator.com/item?id=48885728)

**Background**: A printed circuit board (PCB) mechanically supports and electrically connects electronic components using conductive traces. Traditionally, hobbyists etched boards at home using chemicals, but modern services allow ordering custom PCBs online for a few dollars, making the process much simpler and more reliable.

<details><summary>References</summary>
<ul>
<li><a href="https://resources.altium.com/p/pcb-design-basics-new-designers">PCB Design Basics for New Designers | Getting Started</a></li>
<li><a href="https://www.pcbelec.com/blog/pcb-cost-and-budgeting/what-factors-determine-the-price-of-pcb.html">2025 Custom PCB Cost Factors: Pricing Guide | JHYPCB</a></li>

</ul>
</details>

**Discussion**: Commenters praised the affordability of custom PCBs, with some recommending JLCPCB and sharing similar first-PCB experiences. One user nostalgically recalled home etching methods, sparking a discussion on DIY versus ordering from China.

**Tags**: `#PCB design`, `#electronics`, `#DIY`, `#hardware`

---

<a id="item-20"></a>
## [Regaining Deep Reading After Screen Addiction](https://substack.magazinenongrata.com/p/how-i-learned-to-read-again) ⭐️ 6.0/10

A personal essay on Substack describes the author's loss of deep reading ability due to screen addiction and outlines strategies to regain it, such as setting aside dedicated reading time and practicing active reading techniques. This essay resonates with many who struggle with fragmented attention in the digital age, highlighting a widespread cognitive shift from deep reading to skimming that affects critical thinking and comprehension. The author notes that their reading peak was at age 11-12, and community comments reference Paul Graham's view that deep readers will be the only ones who can think well, as well as Mortimer Adler's book 'How to Read a Book' which addresses reading strategies beyond 6th grade.

hackernews · georgex7 · Jul 12, 18:22 · [Discussion](https://news.ycombinator.com/item?id=48883238)

**Background**: Deep reading is the ability to engage with a text for extended periods, understanding complex arguments and nuances, as opposed to the skimming and scanning common on screens. Screen addiction refers to compulsive use of digital devices, often leading to shortened attention spans and reduced capacity for focused reading.

**Discussion**: Commenters share personal struggles with screen addiction and ADHD, and discuss the value of distinguishing between reading long articles and books. Some reference Paul Graham and Mortimer Adler to emphasize the importance of deep reading for clear thinking.

**Tags**: `#reading`, `#attention`, `#digital habits`, `#self-improvement`

---

<a id="item-21"></a>
## [Death of the Status Update: 55% of Americans Stop Posting](https://ca.pcmag.com/social-media/16790/the-death-of-the-status-update-why-55-of-americans-stopped-posting-on-social-media) ⭐️ 6.0/10

A recent analysis reveals that 55% of Americans have stopped posting on social media, driven by algorithmic feeds that prioritize viral content over updates from friends, pushing communication to private group chats. This shift signals a fundamental change in social media usage, where platforms designed for public sharing are losing relevance for personal connection, potentially impacting user engagement and advertising models. The analysis is based on a survey and community discussion, highlighting that users feel their posts go unseen due to algorithmic curation, and many have moved to group chats for meaningful interaction.

hackernews · thunderbong · Jul 12, 10:14 · [Discussion](https://news.ycombinator.com/item?id=48879902)

**Background**: Social media platforms like Facebook and Instagram have increasingly shifted from chronological feeds to algorithmic ones that prioritize content likely to maximize engagement, such as viral videos. This change has reduced the visibility of personal updates from friends and family. As a result, users who once posted regularly now find little incentive to share, as their content rarely reaches their intended audience.

**Discussion**: Commenters widely agree that algorithmic feeds have killed personal posting, with many noting that group chats have become the primary space for genuine social interaction. Some users report that their feeds are now filled with irrelevant content from strangers, further discouraging posting.

**Tags**: `#social media`, `#user behavior`, `#algorithms`, `#community discussion`

---

<a id="item-22"></a>
## [Anthropic Extends Claude Fable 5 Access Again](https://simonwillison.net/2026/Jul/12/bump/#atom-everything) ⭐️ 6.0/10

Anthropic has extended Claude Fable 5 access on all paid plans through July 19, 2026, citing compute constraints, while OpenAI removed usage limits for GPT-5.6 Sol and announced efficiency improvements. This highlights the competitive pressure between Anthropic and OpenAI, where model availability and pricing strategies directly influence user adoption. Anthropic's repeated extensions may erode user trust, while OpenAI's confident stance could attract more subscribers. Claude Fable 5 users can use up to half of their weekly usage limit on Fable 5, then either use credits or switch models. OpenAI's GPT-5.6 Sol temporarily removed the 5-hour usage limit for Plus, Business, and Pro plans, and rolled out efficiency changes to reduce usage consumption.

rss · Simon Willison · Jul 12, 21:20

**Background**: Claude Fable 5 is Anthropic's most capable widely released model, designed for demanding reasoning and long-horizon agentic tasks. GPT-5.6 Sol is OpenAI's flagship frontier model in the GPT-5.6 family, with strong capabilities in coding, science, and cybersecurity. Both models represent the cutting edge of AI, and their availability is a key factor in user choice.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/claude/fable">Claude Fable \ Anthropic</a></li>
<li><a href="https://openai.com/index/previewing-gpt-5-6-sol/">Previewing GPT-5.6 Sol: a next-generation model | OpenAI</a></li>
<li><a href="https://support.claude.com/en/articles/11049741-what-is-the-max-plan">What is the Max plan? | Claude Help Center</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Anthropic`, `#Claude`, `#GPT-5`, `#compute constraints`

---

<a id="item-23"></a>
## [CGI Motion Capture with Only a Camera](https://hackaday.com/2026/07/12/cgi-motion-capture-with-only-a-camera/) ⭐️ 6.0/10

A Hackaday article revives a 1990s VFX device approach, demonstrating CGI motion capture using only a camera without specialized hardware. This technique could lower the barrier to entry for indie filmmakers and hobbyists, making motion capture more accessible without expensive equipment. The method revives a 1990s VFX device concept, relying on computer vision algorithms to track motion from a single camera feed.

rss · Hackaday · Jul 13, 05:00

**Background**: Traditional motion capture requires specialized hardware like markers, suits, or multiple cameras. The 1990s saw early experiments in camera-only capture, but limited computing power hindered adoption. Modern computer vision advances now make this approach feasible.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Visual_effects">Visual effects - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#CGI`, `#motion capture`, `#computer vision`, `#VFX`

---

<a id="item-24"></a>
## [1964 AI Predictions Still Resonate Today](https://hackaday.com/2026/07/12/musing-on-ai-from-1964/) ⭐️ 6.0/10

A Hackaday article highlights Irving John Good's 1964 paper 'Speculations Concerning the First Ultraintelligent Machine,' drawing parallels between his predictions and modern AI developments. This historical perspective shows that foundational ideas about superintelligent AI were contemplated decades ago, reminding us that current debates have deep roots and that some predictions remain relevant. Good's paper speculated that an ultraintelligent machine could design even better machines, leading to an 'intelligence explosion.' The article references this concept without providing new technical analysis.

rss · Hackaday · Jul 13, 02:00

**Background**: Irving John Good was a British mathematician and cryptologist who worked with Alan Turing. His 1964 paper introduced the concept of an 'ultraintelligent machine' that surpasses human intellect, which could recursively improve itself. This idea later influenced discussions on the technological singularity.

<details><summary>References</summary>
<ul>
<li><a href="https://www.sciencedirect.com/science/chapter/bookseries/pii/S0065245808604180">Speculations Concerning the First Ultraintelligent Machine*</a></li>
<li><a href="https://vtechworks.lib.vt.edu/bitstream/handle/10919/89424/TechReport05-3.pdf">Speculations Concerning the First Ultraintelligent Machine*</a></li>
<li><a href="https://www.flyingpenguin.com/wp-content/uploads/2022/04/good-1964-.pdf">Speculations Concerning the First Ultraintelligent Machine*</a></li>

</ul>
</details>

**Tags**: `#AI`, `#history`, `#philosophy`

---

<a id="item-25"></a>
## [Porting Nvidia GPU Driver to Haiku for 3D Acceleration](https://hackaday.com/2026/07/12/porting-the-nvidia-gpu-driver-to-haiku-for-3d-acceleration/) ⭐️ 6.0/10

Developers are porting Nvidia's open-source GPU kernel driver to Haiku OS, aiming to bring 3D acceleration to the operating system. The effort leverages Nvidia's MIT-licensed Linux driver code as a starting point. This port could significantly enhance Haiku's graphical capabilities, making it more viable for modern desktop use and attracting developers and users to the niche OS. It demonstrates the potential for reusing open-source drivers across different operating systems. The port is being led by developer [X512] and is based on Nvidia's open-gpu-kernel-modules, which were released under the MIT license. The work is still in progress and may face challenges due to Haiku's unique kernel architecture.

rss · Hackaday · Jul 12, 20:00

**Background**: Haiku is a free and open-source operating system inspired by BeOS, designed for personal computers. It has been in beta development for years and lacks native 3D acceleration for many modern GPUs, which limits its usability for graphics-intensive applications.

<details><summary>References</summary>
<ul>
<li><a href="https://hackaday.com/2026/07/12/porting-the-nvidia-gpu-driver-to-haiku-for-3d-acceleration/">Porting The Nvidia GPU Driver To Haiku For 3D Acceleration | Hackaday</a></li>
<li><a href="https://en.wikipedia.org/wiki/Haiku_(operating_system)">Haiku (operating system) - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#Haiku OS`, `#GPU driver`, `#Nvidia`, `#3D acceleration`, `#open source`

---

<a id="item-26"></a>
## [Silent Speech via Ultrasound Probe](https://hackaday.com/2026/07/12/speak-silently-with-an-ultrasound-probe/) ⭐️ 6.0/10

A prototype system uses an ultrasound probe to read tongue movements and machine learning to decode them into speech, enabling silent computer interaction. This technology offers a novel way to interact with computers privately, without audible speech, which could benefit privacy-sensitive environments and accessibility. The system achieves a 15.6% word error rate on open-vocabulary speech and generalizes across different people, as reported by Aleph Neuro.

rss · Hackaday · Jul 12, 14:00

**Background**: Silent speech interfaces (SSIs) decode articulatory or neural signals without sound. Ultrasound imaging of the tongue is one modality, combined with machine learning to predict intended speech. This approach differs from throat microphones or EEG-based systems.

<details><summary>References</summary>
<ul>
<li><a href="https://hackaday.com/2026/07/12/speak-silently-with-an-ultrasound-probe/">Speak Silently With An Ultrasound Probe | Hackaday</a></li>
<li><a href="https://alephneuro.com/blog/silent-speech">Silent speech with ultrasound — Aleph</a></li>
<li><a href="https://www.nature.com/articles/s44460-025-00010-2">Sensing technologies for silent speech interfaces - Nature</a></li>

</ul>
</details>

**Tags**: `#ultrasound`, `#speech recognition`, `#privacy`, `#HCI`

---

<a id="item-27"></a>
## [Laser-Guided Fungal Art: Merging Biology and Digital Fabrication](https://hackaday.com/2026/07/12/printing-fungal-art-with-laser-control/) ⭐️ 6.0/10

Kexin Wang's Funguy project uses a laser diode to repeatedly trace patterns on agar gel, exploiting the photophobic nature of fungi to guide their growth into pre-designed artistic shapes. This project demonstrates a novel intersection of biology and digital fabrication, opening possibilities for living materials in art and design, and could inspire new methods for controlled biological growth. The fungus is photophobic, meaning it avoids light, so the laser effectively creates a 'containment' boundary that the fungus grows around. The system uses a laser diode and a simulation to synchronize the pattern with the actual growth.

rss · Hackaday · Jul 12, 11:00

**Background**: Bioart combines biotechnology with artistic expression, often using living organisms as medium. Digital fabrication techniques like laser cutting and 3D printing are increasingly integrated with biological materials to create interactive or living artworks. Fungal growth can be influenced by light, temperature, and nutrients, making it a controllable medium for such projects.

<details><summary>References</summary>
<ul>
<li><a href="https://hackaday.com/2026/07/12/printing-fungal-art-with-laser-control/">Printing Fungal Art With Laser Control - Hackaday</a></li>
<li><a href="https://dl.acm.org/doi/full/10.1145/3680530.3695440">Exploring Fungal Morphology Simulation and Dynamic Light ...</a></li>
<li><a href="https://dfabclass.com/intro/digital-biofabrication/">Digital BioFabrication – Intro to Digital Fabrication</a></li>

</ul>
</details>

**Tags**: `#bioart`, `#digital fabrication`, `#fungi`, `#laser control`

---


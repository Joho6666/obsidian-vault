# Horizon Daily - 2026-07-20

> From 33 items, 21 important content pieces were selected

---

1. [Claude Fable Produces Counterexample to Jacobian Conjecture](#item-1) ⭐️ 9.0/10
2. [Leaked Email Reveals Altman's Open-Source Strategy](#item-2) ⭐️ 9.0/10
3. [Bowling center owner replaces $120k system with $1,600 ESP32s](#item-3) ⭐️ 8.0/10
4. [Bun Rewritten in Rust Using Claude Code](#item-4) ⭐️ 8.0/10
5. [Alibaba Announces Qwen 3.8, a 2.4T Open-Weight LLM](#item-5) ⭐️ 8.0/10
6. [Texas Sheriff Used ALPR to Track Woman for Abortion](#item-6) ⭐️ 8.0/10
7. [Moonshine: Headless Game Streaming via Moonlight](#item-7) ⭐️ 7.0/10
8. [Hardware is not so hard: Lessons from 2,500 MIDI recorders](#item-8) ⭐️ 7.0/10
9. [Minecraft Java Edition Switches to SDL3](#item-9) ⭐️ 7.0/10
10. [New IA-64 Emulator Boots Windows](#item-10) ⭐️ 7.0/10
11. [Meta-Analysis: Developer Builds Pipeline to Debug Token Costs](#item-11) ⭐️ 7.0/10
12. [OpenAI Reduces Codex Context Size from 372k to 272k](#item-12) ⭐️ 7.0/10
13. [Skyroot Launches India's First Private Orbital Rocket](#item-13) ⭐️ 7.0/10
14. [Chinese AI Startup Claims 10 Trillion Tokens/Day, Profitable](#item-14) ⭐️ 7.0/10
15. [Kagi's Orion Browser: WebKit Alternative with Ad-Blocking](#item-15) ⭐️ 6.0/10
16. [MikroTik as Home Router: Power vs. Usability](#item-16) ⭐️ 6.0/10
17. [IndieWeb Journey: Lessons from Joining](#item-17) ⭐️ 6.0/10
18. [AI advice reduces accuracy but boosts confidence, study finds](#item-18) ⭐️ 6.0/10
19. [Home Server Failure and Rebuild with Reliable Boot Media](#item-19) ⭐️ 6.0/10
20. [Last MPEG-4 Visual Patent Expires](#item-20) ⭐️ 6.0/10
21. [Zilog Z80 Turns 50: A Retrospective on a Legendary Microprocessor](#item-21) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Claude Fable Produces Counterexample to Jacobian Conjecture](https://xcancel.com/__alpoge__/status/2079028340955197566) ⭐️ 9.0/10

Anthropic employee Levent Alpöge claimed on X that Claude Fable, an LLM, produced a concrete counterexample to the long-standing Jacobian Conjecture, which was verified in multiple ways. If confirmed, this would be a major mathematical breakthrough achieved by an AI, potentially reshaping how mathematicians approach open problems and demonstrating LLMs' capability in rigorous mathematical reasoning. The Jacobian Conjecture is notorious for many flawed proofs; the counterexample was reportedly verified by Claude Code in seven different ways. The claim has sparked both excitement and skepticism in the community.

hackernews · loubbrad · Jul 20, 02:51 · [Discussion](https://news.ycombinator.com/item?id=48973869)

**Background**: The Jacobian Conjecture, first stated in 1884, asserts that a polynomial map with a non-zero constant Jacobian determinant has a polynomial inverse. It is a famous open problem in algebraic geometry, listed as Smale's 16th problem. A counterexample would disprove the conjecture entirely.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Jacobian_conjecture">Jacobian conjecture</a></li>
<li><a href="https://en.wikipedia.org/wiki/Counterexample">Counterexample - Wikipedia</a></li>
<li><a href="https://www.anthropic.com/claude/fable">Claude Fable \ Anthropic</a></li>

</ul>
</details>

**Discussion**: Comments show mixed reactions: some are amazed by the LLM's verification ability, while others point to Wikipedia's note on many flawed proofs, suggesting caution. One user hopes LLMs can settle other conjectures like Collatz.

**Tags**: `#AI`, `#mathematics`, `#LLM`, `#Jacobian Conjecture`, `#research`

---

<a id="item-2"></a>
## [Leaked Email Reveals Altman's Open-Source Strategy](https://simonwillison.net/2026/Jul/20/sam-altman/#atom-everything) ⭐️ 9.0/10

A leaked email from Sam Altman to OpenAI's board, dated October 1, 2022, and exposed in the Musk v. Altman (2026) case, reveals his proposal to release a GPT-3-level open-source model that can run on consumer hardware, aiming to discourage competitors and hinder new efforts from getting funded. This email provides rare insight into OpenAI's strategic thinking about open-source AI, revealing that the company considered releasing powerful models not purely for altruism but to preempt competition and control the market. It has significant implications for AI ethics, open-source debates, and antitrust considerations. The email specifically mentions creating a model with 'the approximate capability of GPT-3' that can run locally on consumer hardware, and proposes doing it 'before Stability or someone else does.' Altman argues this would 'discourage others from releasing similarly-powerful models' and 'make it harder for new efforts to get funded.'

rss · Simon Willison · Jul 20, 03:47

**Background**: GPT-3 is a large language model released by OpenAI in 2020, known for its ability to generate human-like text. Running such a model on consumer hardware typically requires significant optimization, as the original model is too large for most personal devices. The open-source AI movement has gained momentum with models like Meta's LLaMA and Mistral, which can be run locally. This email predates the release of many such models, showing OpenAI's early strategic considerations.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/openai/gpt-3">GitHub - openai/ gpt - 3 : GPT - 3 : Language Models are Few-Shot Learners</a></li>
<li><a href="https://enicomp.com/local-llms-running-llama-3-and-mistral-on-consumer-hardware/">Local LLMs: Running Llama 3 and Mistral on Consumer Hardware</a></li>

</ul>
</details>

**Tags**: `#openai`, `#sam-altman`, `#ai-ethics`, `#open-source`, `#generative-ai`

---

<a id="item-3"></a>
## [Bowling center owner replaces $120k system with $1,600 ESP32s](https://news.ycombinator.com/item?id=48968606) ⭐️ 8.0/10

A bowling center owner built an open-source scoring system using ESP32 microcontrollers, replacing a $120,000 commercial system for about $1,600. The prototype uses ESPNow mesh networking, Redis event streaming, and a React frontend. This demonstrates how modern open hardware and software can drastically reduce costs in niche industries, challenging vendor lock-in and making retrofits accessible. It could inspire similar DIY projects in other legacy systems. The system uses ESP32 nodes with IR break-beam sensors and relays, communicating via ESPNow with an RS485 fallback. The gateway connects to a Raspberry Pi running Redis and a state machine, with a React-based UI.

hackernews · section33 · Jul 19, 14:41

**Background**: Commercial bowling scoring systems are niche and expensive, often costing $80k-$120k for a replacement. They use camera-based pin detection and control pinsetters, but the core mechanical parts are decades old. ESP32 is a low-cost, Wi-Fi/Bluetooth-enabled microcontroller popular in IoT projects.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Automatic_scorer">Automatic scorer - Wikipedia</a></li>
<li><a href="https://sesamedisk.com/diy-bowling-system-esp32-replacement/">Replacing $120K Bowling System with $1,600 - Sesame Disk</a></li>

</ul>
</details>

**Discussion**: Commenters praised the project, sharing similar experiences retrofitting old machine tools and bowling equipment. Some expressed interest in seeing documentation or videos of the mechanical internals. Others discussed adding LED lighting and kiosk payment systems.

**Tags**: `#embedded systems`, `#ESP32`, `#retrofit`, `#cost reduction`, `#DIY`

---

<a id="item-4"></a>
## [Bun Rewritten in Rust Using Claude Code](https://simonwillison.net/2026/Jul/19/claude-code-in-bun-in-rust/) ⭐️ 8.0/10

Bun, the JavaScript runtime originally written in Zig, has been rewritten in Rust using Anthropic's Claude Code AI tool. The massive pull request was merged in less than a month. This rewrite shifts Bun's language foundation from Zig to Rust, potentially improving memory safety and developer productivity. It also raises questions about AI-assisted development and project governance, as the rewrite was largely driven by an AI tool. The new Bun version is reported as v1.4.0, while the latest public release is v1.3.14, suggesting a preview of an unreleased version. The rewrite was completed in under a month with a 1 million+ line pull request.

hackernews · tosh · Jul 19, 10:03 · [Discussion](https://news.ycombinator.com/item?id=48966569)

**Background**: Bun is a fast all-in-one JavaScript runtime designed as a drop-in replacement for Node.js. It was originally written in Zig, a low-level systems programming language. Rust is another systems language known for its memory safety guarantees without a garbage collector. Claude Code is an AI coding assistant from Anthropic.

<details><summary>References</summary>
<ul>
<li><a href="https://bun.sh/">Bun — A fast all-in-one JavaScript runtime</a></li>
<li><a href="https://github.com/oven-sh/bun">GitHub - oven-sh/ bun : Incredibly fast JavaScript runtime , bundler...</a></li>

</ul>
</details>

**Discussion**: Community comments are mixed: some appreciate the memory safety benefits of Rust over Zig, while others criticize the lack of communication and governance. One commenter notes the project's direction seems to have changed without proper community input.

**Tags**: `#Bun`, `#Rust`, `#AI-assisted development`, `#JavaScript runtime`, `#open source`

---

<a id="item-5"></a>
## [Alibaba Announces Qwen 3.8, a 2.4T Open-Weight LLM](https://twitter.com/Alibaba_Qwen/status/2078759124914098291) ⭐️ 8.0/10

Alibaba has announced Qwen 3.8, a 2.4 trillion parameter open-weights large language model (LLM), in response to Moonshot AI's Kimi K3 (2.8T parameters). The model is expected to be released on Hugging Face soon. This announcement intensifies competition in the open-source AI space, with major Chinese tech companies racing to release large open-weight models. It provides the community with more powerful, accessible alternatives to proprietary models. Qwen 3.8 has 2.4 trillion parameters, slightly smaller than Kimi K3's 2.8 trillion. Alibaba has not yet confirmed the exact release date, but the model is expected to be open-weight on Hugging Face. Previous Qwen models have received mixed feedback, with some users reporting usability issues.

hackernews · nh43215rgb · Jul 19, 08:44 · [Discussion](https://news.ycombinator.com/item?id=48966120)

**Background**: Open-weights LLMs are large language models whose trained parameters (weights) are publicly released, allowing developers to download, fine-tune, and deploy them freely. This contrasts with closed models like GPT-4, where only API access is provided. Alibaba's Qwen series and Moonshot AI's Kimi series are prominent Chinese open-weight LLM families.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/collections/Qwen/qwen3">Qwen 3 - a Qwen Collection</a></li>
<li><a href="https://www.linkedin.com/pulse/open-weights-llms-in-depth-analysis-adoption-usage-performance-jha-kymhc">Open - Weights LLMs: In-Depth Analysis of Adoption, Usage, and...</a></li>

</ul>
</details>

**Discussion**: The community is excited about the competition, with users like adrian_b noting that it benefits everyone. Some users, like simonw, are waiting for the open weights release due to access issues. However, negative feedback on previous Qwen models, such as from user 5701652400 who found Qwen 3.7 Pro unusable, adds nuance.

**Tags**: `#AI`, `#LLM`, `#Open Source`, `#Alibaba`, `#Qwen`

---

<a id="item-6"></a>
## [Texas Sheriff Used ALPR to Track Woman for Abortion](https://www.eff.org/deeplinks/2026/07/we-want-texans-know-their-rights-qa-mayday-health-impact-surveillance-abortion) ⭐️ 8.0/10

EFF reported that a Texas sheriff's office searched data from over 83,000 ALPR cameras to track a woman suspected of self-managing an abortion, highlighting a new frontier of surveillance abuse. This case underscores how surveillance technologies like ALPR are being weaponized to enforce abortion bans, threatening reproductive rights and privacy for all Americans. The ALPR system used by the sheriff's office can track vehicle movements across vast areas, and the search involved data from 83,000 cameras, indicating a massive dragnet approach.

hackernews · amarcheschi · Jul 19, 22:03 · [Discussion](https://news.ycombinator.com/item?id=48972062)

**Background**: ALPR (Automatic License Plate Recognition) is a technology that automatically reads and records license plates using cameras and optical character recognition. It is widely used by law enforcement for tasks like finding stolen cars, but its use for tracking individuals suspected of abortion raises serious privacy and civil liberties concerns. Self-managed abortion, often via medication, is legal in some states but criminalized in others, leading to a patchwork of laws.

<details><summary>References</summary>
<ul>
<li><a href="https://www.linkedin.com/pulse/what-alpr-how-its-powering-modern-surveillance-vaxtor-technologies-zq7be">What is ALPR and How It’s Powering Modern Surveillance</a></li>
<li><a href="https://ifwhenhow.org/resources/selfcare-criminalized/">Self-Managed Abortion Research: Self-Care, Criminalized</a></li>

</ul>
</details>

**Discussion**: Commenters expressed outrage and concern, with one noting that period tracking apps are now unsafe in many states. Another highlighted a case in Estonia where a police officer was fired for database misuse, contrasting with the US lack of accountability. Some pointed to a growing movement to criminally hold women liable for abortion.

**Tags**: `#surveillance`, `#privacy`, `#reproductive rights`, `#civil liberties`, `#ALPR`

---

<a id="item-7"></a>
## [Moonshine: Headless Game Streaming via Moonlight](https://github.com/hgaiser/moonshine) ⭐️ 7.0/10

Moonshine is an open-source tool that extends the Sunshine/Moonlight ecosystem to allow game streaming from a PC to any device without requiring a physical display on the host. It enables headless streaming, meaning the host PC can stream games without occupying its own screen. This solves a key limitation of Sunshine/Moonlight, where the host display had to be active and showing the game, making the host unusable for other tasks. Moonshine enables multi-seat setups and dedicated game streaming servers, improving flexibility for enthusiasts and home lab users. Moonshine works by creating a virtual display on the host, allowing Sunshine to stream without a physical monitor. It is compatible with any Moonlight client and supports hardware encoding via AMD, Intel, and NVIDIA GPUs.

hackernews · wertyk · Jul 20, 00:16 · [Discussion](https://news.ycombinator.com/item?id=48972970)

**Background**: Sunshine is an open-source self-hosted game stream host that implements NVIDIA's GameStream protocol, and Moonlight is the corresponding client that runs on various devices. Together they enable low-latency game streaming from a PC to phones, tablets, laptops, and TVs. However, standard Sunshine requires a physical display to be connected and active, which limits its use in headless or multi-seat scenarios.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/LizardByte/Sunshine">GitHub - LizardByte/Sunshine: Self-hosted game stream host ... Sunshine: Sunshine - docs.lizardbyte.dev Releases · LizardByte/Sunshine - GitHub Sunshine download | SourceForge.net Sunshine Download | TechSpot Sunshine Game Streaming Setup: 14 Steps [2026]</a></li>
<li><a href="https://moonlight-stream.org/">Moonlight Game Streaming: Play Your PC Games Remotely</a></li>
<li><a href="https://github.com/Steam-Headless/docker-steam-headless">GitHub - Steam-Headless/docker-steam-headless: A Headless ...</a></li>

</ul>
</details>

**Discussion**: Community comments highlight that Moonshine addresses a real pain point: users previously had to keep the host display active, making the host unusable for other work. One user shared that with Apollo (a similar tool) they achieve near-zero lag over Wi-Fi 7, while another noted that headless streaming is also used for emulated console games on older systems.

**Tags**: `#game streaming`, `#open source`, `#Moonlight`, `#Sunshine`, `#headless`

---

<a id="item-8"></a>
## [Hardware is not so hard: Lessons from 2,500 MIDI recorders](https://chipweinberger.com/articles/20260719-hardware-is-not-so-hard) ⭐️ 7.0/10

A developer published a detailed retrospective on selling 2,500 JamCorder MIDI recorders, arguing that hardware development can be simpler than expected by making careful design choices. This provides practical, real-world insights for indie developers and entrepreneurs considering hardware products, challenging the common belief that hardware is inherently difficult. The JamCorder is a simple device with only 25 components on its PCB and a two-part injection-molded clamshell case, which kept manufacturing costs low and assembly straightforward.

hackernews · chipweinberger · Jul 19, 10:34 · [Discussion](https://news.ycombinator.com/item?id=48966713)

**Background**: MIDI (Musical Instrument Digital Interface) is a technical standard for connecting electronic musical instruments and computers. A MIDI recorder captures performance data (e.g., note on/off, velocity) rather than audio, allowing playback on any MIDI-compatible device.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/MIDI">MIDI - Wikipedia</a></li>
<li><a href="https://learn.sparkfun.com/tutorials/midi-tutorial/all">MIDI Tutorial - SparkFun Learn</a></li>

</ul>
</details>

**Discussion**: Commenters generally praised the product and insights, though some noted that hardware difficulty scales with product complexity and that the JamCorder's simplicity is not representative of most hardware projects.

**Tags**: `#hardware`, `#product development`, `#entrepreneurship`, `#MIDI`, `#engineering`

---

<a id="item-9"></a>
## [Minecraft Java Edition Switches to SDL3](https://www.minecraft.net/en-us/article/minecraft-26-3-snapshot-4) ⭐️ 7.0/10

Minecraft: Java Edition has updated its underlying input and windowing library from SDL2 to SDL3 in snapshot 26w04a, marking a major dependency upgrade for the game. This upgrade improves cross-platform performance and future-proofs Minecraft against modern display and input APIs, benefiting millions of players and mod developers. Known issues include crashes on Windows when using exclusive fullscreen with multiple monitors, and crashes on Wayland when entering exclusive fullscreen mode.

hackernews · ObviouslyFlamer · Jul 19, 11:48 · [Discussion](https://news.ycombinator.com/item?id=48967256)

**Background**: SDL (Simple DirectMedia Layer) is a cross-platform library that provides low-level access to audio, keyboard, mouse, and graphics hardware. SDL3, released in January 2025, is a major version with API changes and improved support for modern systems. Minecraft uses LWJGL (Lightweight Java Game Library) to bind native libraries like SDL for Java.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/SDL_library">SDL library</a></li>
<li><a href="https://github.com/LWJGL/lwjgl3">GitHub - LWJGL/lwjgl3: LWJGL is a Java library that enables ... Get started with LWJGL 3 - LWJGL GitHub - AlPasDev/lwjgl3: LWJGL is a Java library that ... Maven Repository: org.lwjgl Maven Repository: org.lwjgl » lwjgl LWJGL - Lightweight Java Game Library: Wiki</a></li>

</ul>
</details>

**Discussion**: Community members shared positive porting experiences, with one developer noting a mostly painless refactor from GLFW to SDL3. However, concerns were raised about the blocking nature of the known fullscreen crashes, with hopes they are fixed before the stable release.

**Tags**: `#Minecraft`, `#SDL3`, `#game development`, `#LWJGL`, `#open source`

---

<a id="item-10"></a>
## [New IA-64 Emulator Boots Windows](https://raymii.org/s/blog/Intel_Itanium_IA-64-Emulator_that_boots_Windows.html) ⭐️ 7.0/10

Yufeng Gao, with help from gdwnldsKSC, released version 0.1 of an Intel Itanium (IA-64) emulator that can boot Windows Server 2003 and Windows XP 64-bit for IA-64. This is the first publicly available IA-64 emulator capable of booting Windows, reviving a niche but historically significant architecture for retrocomputing and software preservation. The emulator currently only boots Windows; OpenVMS, HP-UX, Linux, and BSD do not boot yet. Performance is described as 486-level on a Ryzen 5000 series host.

hackernews · jandeboevrie · Jul 19, 20:50 · [Discussion](https://news.ycombinator.com/item?id=48971566)

**Background**: IA-64 (Itanium) is a 64-bit architecture developed by Intel and HP, intended for high-end servers but ultimately failed in the market due to poor x86 compatibility and competition from x86-64. Emulating it has been challenging due to its complex VLIW instruction set and lack of documentation.

<details><summary>References</summary>
<ul>
<li><a href="https://raymii.org/s/blog/Intel_Itanium_IA-64-Emulator_that_boots_Windows.html">More emulation goodness, an Intel Itanium (IA-64) emulator ...</a></li>
<li><a href="https://github.com/itanium64/Rosalia64">GitHub - itanium64/Rosalia64: (ABANDONED) Itanium (IA64 ...</a></li>

</ul>
</details>

**Discussion**: Community comments include historical anecdotes about IA-64 Windows usage in banking, jokes about the emulator's slow performance, and suggestions to integrate the work into QEMU. There is also mention of a separate 'vibe-coded' IA-64 emulation for QEMU on GitHub.

**Tags**: `#emulation`, `#IA-64`, `#Windows`, `#retrocomputing`, `#QEMU`

---

<a id="item-11"></a>
## [Meta-Analysis: Developer Builds Pipeline to Debug Token Costs](https://quesma.com/blog/custom-deep-research-pipeline/) ⭐️ 7.0/10

A developer humorously built a deep research pipeline specifically to analyze why their deep research pipeline consumed too many tokens, discovering the pipeline itself was the main cost driver. This meta-humor article highlights the real challenge of token cost optimization in LLM pipelines, sparking community discussion on practical strategies like tiered model usage and local models. The article suggests using cheap models for initial exploration and funneling findings through increasingly powerful models, a strategy echoed by community members who advocate for the 80/20 rule with local models.

hackernews · bkotrys · Jul 19, 12:01 · [Discussion](https://news.ycombinator.com/item?id=48967355)

**Background**: Deep research pipelines are multi-step LLM workflows that generate reports by iteratively searching, summarizing, and synthesizing information. Each step consumes tokens, and costs can escalate quickly, especially when using frontier models for every stage. Token optimization techniques include prompt caching, model routing, and using smaller models for simpler tasks.

<details><summary>References</summary>
<ul>
<li><a href="https://www.tokenoptimize.dev/guides/llm-token-optimization-strategies">LLM Token Optimization Strategies: The Complete Guide for 2026</a></li>
<li><a href="https://github.com/pleasedodisturb/awesome-llm-token-optimization">pleasedodisturb/awesome-llm-token-optimization - GitHub</a></li>
<li><a href="https://shchegrikovich.substack.com/p/4-architectures-of-deep-research">4 Architectures of Deep Research Agents</a></li>

</ul>
</details>

**Discussion**: Community comments are mixed: some find the meta-humor relatable, while others question the premise, noting that hallucinations cannot be fixed by rules alone. A common suggestion is to use local models for 90% of tasks and reserve frontier models for the remaining 10%.

**Tags**: `#AI`, `#token optimization`, `#deep research`, `#LLM pipelines`, `#cost efficiency`

---

<a id="item-12"></a>
## [OpenAI Reduces Codex Context Size from 372k to 272k](https://github.com/openai/codex/pull/33972/files) ⭐️ 7.0/10

OpenAI has reduced the context window of its Codex model from 372,000 tokens to 272,000 tokens, as reflected in a GitHub pull request. This change affects the maximum amount of text the model can process at once. This reduction highlights the ongoing trade-off between context length and model intelligence, as longer contexts can degrade performance and increase costs. Users relying on large contexts for complex tasks may need to adjust their workflows. The change was made in a pull request to the Codex repository, and community members noted that context compaction techniques can partially mitigate the loss of detail. The new context size aligns with the 272k token limit reported in Codex model metadata.

hackernews · AmazingTurtle · Jul 19, 07:54 · [Discussion](https://news.ycombinator.com/item?id=48965850)

**Background**: A context window is the amount of text an LLM can consider at once, measured in tokens. Larger windows allow the model to handle more information but can reduce intelligence and increase computational cost. OpenAI has previously offered larger contexts for Codex, such as 1M tokens for GPT-5.4, but now appears to be prioritizing model quality over raw context size.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/openai/codex/discussions/1999">How large is the context window when Codex is used via a ...</a></li>
<li><a href="https://www.ibm.com/think/topics/context-window">What is a context window ? | IBM</a></li>

</ul>
</details>

**Discussion**: Community comments are mixed: some users lament the loss of detail, especially for tasks like discussing multiple papers, while others argue that larger contexts make models dumber and that compaction is lossy. A few users suggest that dividing work into smaller chunks is a better approach.

**Tags**: `#AI`, `#LLM`, `#context window`, `#OpenAI`, `#Codex`

---

<a id="item-13"></a>
## [Skyroot Launches India's First Private Orbital Rocket](https://hackaday.com/2026/07/19/hackaday-links-july-19-2026/) ⭐️ 7.0/10

On July 18, 2026, Skyroot Aerospace successfully launched the Vikram-1 rocket, India's first privately developed orbital launch vehicle, placing it into orbit. This milestone makes India the third country, after the U.S. and China, to have a private orbital launch capability, boosting the country's commercial space sector and global competitiveness. Vikram-1 is a four-stage rocket about 20 meters tall, with the first three stages using solid propulsion and the upper kick stage using liquid propulsion for precise orbital insertion.

rss · Hackaday · Jul 19, 23:00

**Background**: Skyroot Aerospace was founded by former ISRO scientists and previously launched a suborbital rocket, Vikram-S, in November 2022. The Vikram-1 is designed for small satellite launches, featuring carbon-composite airframes to reduce weight and cost.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Skyroot_Aerospace">Skyroot Aerospace</a></li>
<li><a href="https://en.wikipedia.org/wiki/Vikram-1">Vikram-1 - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Vikram_(rocket_family)">Vikram (rocket family)</a></li>

</ul>
</details>

**Tags**: `#aerospace`, `#rocket launch`, `#India`, `#private space industry`

---

<a id="item-14"></a>
## [Chinese AI Startup Claims 10 Trillion Tokens/Day, Profitable](https://mp.weixin.qq.com/s?__biz=MzI3MTA0MTk1MA==&mid=2652713906&idx=1&sn=4e843834e26fbf0f675ca8ed0dbfa34f) ⭐️ 7.0/10

A new Chinese AI company claims to process 10 trillion tokens daily and is already profitable, marking a significant milestone in AI infrastructure. This achievement could disrupt the AI compute landscape by demonstrating that massive token processing can be economically viable, potentially lowering costs for AI applications and challenging established players. The company reportedly achieves this throughput with profitability, suggesting efficient infrastructure and cost management. The exact technical approach and business model remain undisclosed.

rss · 新智元 · Jul 19, 09:53

**Background**: Tokens are the basic units of text that AI models process; processing trillions of tokens daily requires massive computational resources. Many AI companies struggle with profitability due to high compute costs, making this claim notable.

<details><summary>References</summary>
<ul>
<li><a href="https://eluxr.com/2025/09/18/beyond-a-trillion-the-epic-token-race-of-one-trillion-tokens-every-single-day/">Beyond a Trillion : The Epic Token Race of One Trillion Tokens Every...</a></li>
<li><a href="https://articles.emp0.com/ai-profitability-and-tokenpocalypse/">Can you afford AI Profitability and the Tokenpocalypse? - Articles</a></li>

</ul>
</details>

**Tags**: `#AI`, `#infrastructure`, `#China`, `#token processing`, `#startup`

---

<a id="item-15"></a>
## [Kagi's Orion Browser: WebKit Alternative with Ad-Blocking](https://orionbrowser.com/) ⭐️ 6.0/10

Kagi has released Orion Browser, a WebKit-based browser with built-in ad-blocking and vertical tabs, now available in beta for Linux and as a paid product on macOS and iOS. Orion offers a privacy-focused alternative to mainstream browsers, potentially reducing reliance on Chromium and Firefox while bringing WebKit testing to Windows and Linux users. Orion supports Firefox and Chrome extensions, including uBlock Origin and SponsorBlock, and features nested vertical tabs. However, users report bugs such as broken settings pages and missing context menu options.

hackernews · sebjones · Jul 19, 19:13 · [Discussion](https://news.ycombinator.com/item?id=48970894)

**Background**: WebKit is the browser engine that powers Safari and all iOS browsers. Orion is one of the few desktop browsers using WebKit outside Apple's ecosystem, offering a privacy-first experience with built-in ad blocking and extension compatibility.

<details><summary>References</summary>
<ul>
<li><a href="https://orionbrowser.com/">Orion Browser by Kagi</a></li>
<li><a href="https://blog.kagi.com/orion">Kagi Blog - Orion 1.0 ︎ Browse Beyond</a></li>
<li><a href="https://appleinsider.com/articles/25/11/26/hands-on-kagis-orion-browser-is-a-surprisingly-good-alternative-to-safari">Hands On: Kagi's Orion browser is a Safari competitor</a></li>

</ul>
</details>

**Discussion**: Community feedback is mixed: some praise Orion's ad-blocking and vertical tabs as Firefox alternatives, while others report persistent bugs and missing features, leading many to stick with Firefox for now.

**Tags**: `#browser`, `#Kagi`, `#ad-blocking`, `#WebKit`, `#privacy`

---

<a id="item-16"></a>
## [MikroTik as Home Router: Power vs. Usability](https://justsomebody.dev/blog/mikrotik-home-router) ⭐️ 6.0/10

A detailed guide on using MikroTik RouterOS as a home router was published, highlighting its powerful features but steep learning curve. The article sparked community debate about alternatives like VyOS and Linux. This matters because many networking enthusiasts seek affordable, feature-rich router solutions, and MikroTik offers a low-cost option. The debate helps users weigh the trade-offs between proprietary ease-of-use and open-source flexibility. MikroTik RouterOS is based on Linux but is not fully open-source; its UI is considered unintuitive for beginners. Community comments note that features like FQ-CoDel bufferbloat protection require manual configuration, and alternatives such as VyOS (open-source JunOS-like) or plain Debian Linux are popular.

hackernews · rafal_opilowski · Jul 19, 18:57 · [Discussion](https://news.ycombinator.com/item?id=48970772)

**Background**: MikroTik is a Latvian company that produces RouterOS, an operating system for routers, and RouterBOARD hardware. RouterOS can be installed on standard x86 PCs to turn them into routers. VyOS is an open-source network OS based on Debian, offering routing, firewall, and VPN capabilities. Many home users prefer user-friendly solutions like OpenWrt or pfSense, but MikroTik appeals to those who want granular control.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/MikroTik">MikroTik - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/VyOS">VyOS - Wikipedia</a></li>
<li><a href="https://vyos.io/">VyOS Networks - Home of enterprise-grade open source Network OS</a></li>

</ul>
</details>

**Discussion**: Community sentiment is mixed: experienced users praise MikroTik's power, while others criticize its poor UX and recommend alternatives like VyOS or Linux. Some users leverage LLMs to simplify configuration, and many agree that MikroTik switches are excellent but the router UI is painful.

**Tags**: `#networking`, `#MikroTik`, `#home router`, `#open source`

---

<a id="item-17"></a>
## [IndieWeb Journey: Lessons from Joining](https://en.andros.dev/blog/0b8e451e/i-joined-the-indieweb-heres-what-i-learned/) ⭐️ 6.0/10

A personal blog post details the author's experience joining the IndieWeb, including setting up a personal website and implementing POSSE (Publish on Your Own Site, Syndicate Elsewhere). This account highlights the ongoing tension between the IndieWeb's ideals of ownership and its technical complexity, which may hinder mainstream adoption. It also sparks debate about alternatives like Nostr. The author used static site generators and Webmention for decentralized comments, but community comments criticized the steep learning curve involving Docker and command-line tools. Comparisons to Nostr were made, noting Nostr's simpler mental model.

hackernews · andros · Jul 19, 11:14 · [Discussion](https://news.ycombinator.com/item?id=48966984)

**Background**: The IndieWeb is a community promoting personal websites and decentralized social media, emphasizing owning your domain and publishing on your own site first. POSSE is a key principle: publish on your own site and syndicate to silos. Nostr is another decentralized protocol using relays and public-key cryptography.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/IndieWeb">IndieWeb</a></li>
<li><a href="https://indieweb.org/">IndieWeb</a></li>
<li><a href="https://en.wikipedia.org/wiki/Nostr">Nostr</a></li>

</ul>
</details>

**Discussion**: Comments were mixed: some praised the effort but criticized the complexity, arguing that IndieWeb's tech-heavy approach alienates non-technical users. Others suggested Nostr as a simpler alternative, while a few shared their own IndieWeb setups.

**Tags**: `#IndieWeb`, `#decentralized web`, `#social media`, `#self-hosting`, `#POSSE`

---

<a id="item-18"></a>
## [AI advice reduces accuracy but boosts confidence, study finds](https://thenextweb.com/news/ai-advice-suppresses-critical-thinking-wrong-answers-study) ⭐️ 6.0/10

A study found that when people receive advice from an AI system known to give incorrect answers on certain questions, their accuracy decreases while their confidence increases, compared to those who answer without AI advice. This highlights a potential risk of over-reliance on AI: users may become more confident in wrong answers, undermining critical thinking and decision-making in real-world applications. The study used an LLM that researchers knew would produce incorrect answers for specific questions, and participants could choose not to answer if unsure. The design has been criticized for not being specific to AI, as similar effects might occur with any flawed advice source.

hackernews · rbanffy · Jul 19, 21:18 · [Discussion](https://news.ycombinator.com/item?id=48971738)

**Background**: The study examines human-AI interaction, specifically how AI advice affects user accuracy and confidence. Previous research has shown that people often over-rely on AI recommendations, but this study attempts to measure the impact on critical thinking.

**Discussion**: Community comments criticize the study's methodology, arguing it tests general advice-taking behavior rather than AI-specific effects. Some users share real-world observations of AI-generated advice degrading information quality on forums.

**Tags**: `#AI`, `#critical thinking`, `#human-AI interaction`, `#study`

---

<a id="item-19"></a>
## [Home Server Failure and Rebuild with Reliable Boot Media](https://sgt.hootr.club/blog/home-server-rebirth/) ⭐️ 6.0/10

A home server running on a Raspberry Pi failed due to SD card corruption, prompting a rebuild with a more reliable boot medium like a USB flash drive or SSD. This highlights the common but often overlooked issue of SD card reliability in single-board computers, and the importance of choosing robust boot media for long-term server stability. The author replaced the SD card with a USB 3 flash drive or SATA SSD, and community members also recommend using NVMe slots on modern Rockchip SBCs or mini-PCs as alternatives.

hackernews · steinuil · Jul 19, 10:44 · [Discussion](https://news.ycombinator.com/item?id=48966769)

**Background**: Raspberry Pi and other single-board computers often use microSD cards as boot media, which are prone to corruption from power failures or wear. More reliable options include USB drives, SATA SSDs, or NVMe storage, which offer better endurance and performance.

<details><summary>References</summary>
<ul>
<li><a href="https://embedded-sbc.com/posts/embedded-sbc-storage-reliability/">Embedded SBC Storage Reliability: eMMC, microSD, NVMe, and ...</a></li>
<li><a href="https://www.lemaker.org/article-47-1.html">Boot and Storage Notes for SBCs | LeMaker</a></li>
<li><a href="https://blog.lemaker.org/sbc-image-integrity-2026-checksums-safe-flashing-media-failures/">SBC Image Integrity in 2026: Checksums, Safe Flashing, and ...</a></li>

</ul>
</details>

**Discussion**: Commenters shared similar experiences and solutions: using USB boot, SATA SSDs via Argon One cases, or NVMe slots on newer SBCs. One noted that the real failure is often the boot media, and the fix is making rebuilds boring rather than hardware immortal.

**Tags**: `#home server`, `#Raspberry Pi`, `#boot media`, `#hardware reliability`, `#SBC`

---

<a id="item-20"></a>
## [Last MPEG-4 Visual Patent Expires](https://www.phoronix.com/news/Last-MPEG-4-Patent-Expired) ⭐️ 6.0/10

The last patent for MPEG-4 Visual, the video codec standard behind DivX and Xvid, expired on July 19, 2026, as confirmed by the VIA Licensing Alliance. This marks the end of patent restrictions for an old but historically significant codec, though its practical impact is limited since MPEG-4 Part 2 is largely obsolete compared to modern codecs like H.264 and H.265. The last patent was active in Brazil (patent number PI0109962B1), while US and EU patents had expired earlier in 2023. MPEG-4 Visual is distinct from H.264 (MPEG-4 Part 10), which still has active patents.

hackernews · LorenDB · Jul 19, 16:45 · [Discussion](https://news.ycombinator.com/item?id=48969635)

**Background**: MPEG-4 Visual, also known as MPEG-4 Part 2, is a video compression standard that gained popularity in the early 2000s through codecs like DivX (proprietary) and Xvid (open source). It was widely used for video distribution on the internet, especially for pirated movies, before being superseded by more efficient codecs such as H.264. The patent pool was administered by MPEG LA and later VIA Licensing Alliance.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/MPEG-4_Part_2">MPEG-4 Part 2 - Wikipedia</a></li>
<li><a href="https://meta.wikimedia.org/wiki/Have_the_patents_for_MPEG-4_Visual_expired_yet?">Have the patents for MPEG-4 Visual expired yet? - Meta-Wiki</a></li>
<li><a href="https://www.phoronix.com/news/Last-MPEG-4-Patent-Expired">The Last MPEG-4 Visual Patent Has Expired - Phoronix</a></li>

</ul>
</details>

**Discussion**: Commenters clarified that this is about MPEG-4 Part 2 (Xvid/DivX), not H.264, correcting the initial Phoronix article. Some noted that H.264 patents will take years to expire globally, and that the march toward higher resolutions may limit the utility of these older codecs.

**Tags**: `#patents`, `#video codecs`, `#MPEG-4`, `#open standards`

---

<a id="item-21"></a>
## [Zilog Z80 Turns 50: A Retrospective on a Legendary Microprocessor](https://hackaday.com/2026/07/19/remembering-the-zilog-z80-as-it-turns-fifty-years-old/) ⭐️ 6.0/10

A Hackaday article commemorates the 50th anniversary of the Zilog Z80 microprocessor, reflecting on its historical significance and legacy in personal computing. The Z80 was a cornerstone of early home computers and embedded systems, and its 50th anniversary highlights the enduring impact of 8-bit architecture on modern computing. The Z80 was designed by former Intel engineers and released in 1976, offering software compatibility with the Intel 8080 while adding new instructions and registers.

rss · Hackaday · Jul 19, 14:00

**Background**: The Zilog Z80 is an 8-bit microprocessor that powered iconic systems like the ZX Spectrum, TRS-80, and many arcade games. It was designed by Federico Faggin and Ralph Ungermann, who had previously worked on the Intel 4004 and 8080. The Z80's enhanced instruction set and lower cost made it a popular choice for hobbyists and manufacturers.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Zilog_Z80">Zilog Z80 - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Zilog">Zilog - Wikipedia</a></li>
<li><a href="https://spectrum.ieee.org/chip-hall-of-fame-zilog-z80-microprocessor">Chip Hall of Fame: Zilog Z80 Microprocessor - IEEE Spectrum</a></li>

</ul>
</details>

**Tags**: `#Z80`, `#microprocessor`, `#history`, `#retrocomputing`

---


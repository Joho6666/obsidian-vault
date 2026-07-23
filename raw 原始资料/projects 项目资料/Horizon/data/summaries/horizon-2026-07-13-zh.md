# Horizon 每日速递 - 2026-07-13

> 从 41 条内容中筛选出 27 条重要资讯。

---

1. [将 AI 代理迁移至 GPT-5.6：速度提升 2.2 倍，成本降低 27%](#item-1) ⭐️ 8.0/10
2. [Claude Code 每任务消耗 33k tokens，OpenCode 仅 7k](#item-2) ⭐️ 8.0/10
3. [AI 自动化可能侵蚀人类专业知识](#item-3) ⭐️ 8.0/10
4. [因果理论应用于理解大语言模型推理](#item-4) ⭐️ 8.0/10
5. [LLM 创造价值，但前沿实验室可能无法获取](#item-5) ⭐️ 8.0/10
6. [陶哲轩用现代编码代理构建应用](#item-6) ⭐️ 8.0/10
7. [带状疱疹疫苗或可降低痴呆风险](#item-7) ⭐️ 8.0/10
8. [摩托罗拉 MR2600 路由器发现未认证远程代码执行漏洞](#item-8) ⭐️ 8.0/10
9. [AI 提升研究效率但缩小思想范围](#item-9) ⭐️ 8.0/10
10. [HN 用户提议为 AI 生成文章添加标记](#item-10) ⭐️ 7.0/10
11. [8 位计算机的引脚级仿真](#item-11) ⭐️ 7.0/10
12. [谷歌研究：更智能的路线规划可减少交通拥堵](#item-12) ⭐️ 7.0/10
13. [反对有用性：为玩乐而重拾计算](#item-13) ⭐️ 7.0/10
14. [Ghostel.el：基于 libghostty 的快速 Emacs 终端模拟器](#item-14) ⭐️ 7.0/10
15. [电影 CGI 与 AI：软件工程的类比](#item-15) ⭐️ 7.0/10
16. [Odin 编程语言逐渐流行](#item-16) ⭐️ 7.0/10
17. [Chromium 148 的 Math.tanh 可识别操作系统](#item-17) ⭐️ 7.0/10
18. [LLM 代理不应成为直接责任人](#item-18) ⭐️ 7.0/10
19. [首次 PCB 设计与组装之旅](#item-19) ⭐️ 6.0/10
20. [摆脱屏幕成瘾，重获深度阅读能力](#item-20) ⭐️ 6.0/10
21. [状态更新之死：55%美国人停止发帖](#item-21) ⭐️ 6.0/10
22. [Anthropic 再次延长 Claude Fable 5 访问期限](#item-22) ⭐️ 6.0/10
23. [仅用相机实现 CGI 动作捕捉](#item-23) ⭐️ 6.0/10
24. [1964 年的人工智能预言至今仍引发共鸣](#item-24) ⭐️ 6.0/10
25. [将 Nvidia GPU 驱动移植到 Haiku 以实现 3D 加速](#item-25) ⭐️ 6.0/10
26. [通过超声探头实现无声语音](#item-26) ⭐️ 6.0/10
27. [激光引导真菌艺术：融合生物学与数字制造](#item-27) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [将 AI 代理迁移至 GPT-5.6：速度提升 2.2 倍，成本降低 27%](https://ploy.ai/blog/migrating-a-production-ai-agent-to-gpt-5-6) ⭐️ 8.0/10

一个用于构建营销网站的生产级 AI 代理已迁移至 OpenAI 的 GPT-5.6，实现了 2.2 倍的速度提升和 27%的成本降低。迁移过程中还需要一个模式转换修复，以处理 OpenAI 系列模型中的可选属性。 这展示了升级到更新 LLM 所带来的显著性能和成本优势，具体指标可为考虑类似迁移的其他团队提供参考。模式转换解决方案解决了结构化输出生成中的一个常见痛点，使升级在生产环境中更加实用。 该代理能够规划页面、读取代码库、编写组件、生成图像并截图自身工作。模式修复将每个可选属性重写为必需但可为空，使用 anyOf: [T, null]，为模型提供明确的指示缺失的方式。

hackernews · brryant · 7月12日 17:13 · [社区讨论](https://news.ycombinator.com/item?id=48882716)

**背景**: GPT-5.6 是 OpenAI 于 2026 年 7 月 9 日发布的大型语言模型，包含 Luna、Terra 和 Sol 三个变体。它旨在增强企业工作、编程、科学研究和网络安全方面的能力。此次迁移涉及从早期模型（可能是 Opus 4.7/4.8）切换到 GPT-5.6。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GPT-5.6">GPT-5.6</a></li>
<li><a href="https://openai.com/index/previewing-gpt-5-6-sol/">Previewing GPT‑5.6 Sol: a next-generation model - OpenAI</a></li>

</ul>
</details>

**社区讨论**: 评论者注意到他们自己的工作流程也有类似改进，并对具体指标表示赞赏。一些人批评了文章中类似 LLM 的写作风格，而另一些人则讨论了模式转换方法，质疑其必要性和正确性。

**标签**: `#AI`, `#LLM`, `#production`, `#cost optimization`, `#schema design`

---

<a id="item-2"></a>
## [Claude Code 每任务消耗 33k tokens，OpenCode 仅 7k](https://systima.ai/blog/claude-code-vs-opencode-token-overhead) ⭐️ 8.0/10

一项系统性研究发现，Claude Code 在读取用户提示前会发送约 33,000 个 token，而 OpenCode 在相同任务中仅发送约 7,000 个 token，显示出显著的 token 开销差异。 这种 token 低效直接导致用户成本上升，并引发对 AI 编码工具设计动机的担忧，可能影响开发者的工具选择及行业效率标准。 该研究测量了编码工具与 Anthropic 端点之间的所有请求，发现 Claude Code 的缓存策略和 harness token 使用效率远低于 OpenCode。作者计划后续进行更深入的任务分析和定性比较。

hackernews · systima · 7月12日 18:25 · [社区讨论](https://news.ycombinator.com/item?id=48883275)

**背景**: 像 Claude Code 和 OpenCode 这样的 AI 编码工具作为代理框架，向大语言模型发送系统提示、工具定义和上下文。Token 用量直接影响成本和性能，因为用户按 token 付费。高效的 token 管理对实际应用至关重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://asibiont.com/en/blog/claude-code-otpravlyaet-33k-tokenov-do-chteniya-prompta-pochemu-opencode-s-7k-tokenami-effektivnee-dlya-vibe-coding">Claude Code Sends 33k Tokens Before Reading... — ASI Biont Blog</a></li>
<li><a href="https://www.neura.market/blog/claude-code-sends-33k-tokens-before-reading-your-prompt-opencode-sends">Claude Code Sends 33K Tokens Before Reading Your... | Neura Market</a></li>

</ul>
</details>

**社区讨论**: 社区评论表达了对子代理 token 浪费的不满，并怀疑 Anthropic 可能故意增加 token 用量以牟利。一些用户呼吁进行更多定性比较，并指出 token 膨胀是编码代理中的普遍趋势。

**标签**: `#AI coding tools`, `#token efficiency`, `#Claude Code`, `#OpenCode`, `#cost analysis`

---

<a id="item-3"></a>
## [AI 自动化可能侵蚀人类专业知识](https://arxiv.org/abs/2607.06377) ⭐️ 8.0/10

一篇题为《无理解的自动化》的论文警告，AI 自动化可能减少能够发现 AI 错误的人类专家数量，强调透明性和可解释性的必要性。 这一讨论突出了一个关键风险：随着 AI 系统能力增强，我们可能失去发现其错误所需的人类专业知识，从而导致对不可靠 AI 的广泛依赖。 该论文得分为 8.0/10，获得 109 个点赞和 47 条评论，表明社区参与度很高。关键评论警告说，AI 可能停止培养那些能够注意到 AI 自信犯错的人。

hackernews · root-parent · 7月12日 16:54 · [社区讨论](https://news.ycombinator.com/item?id=48882554)

**背景**: 该论文讨论了“无理解的自动化”概念，即 AI 系统自动化任务却不提供其推理过程的洞察。这可能导致人类专业知识下降，因为人们依赖 AI 输出而不进行批判性评估。

**社区讨论**: 评论者担心 AI 自动化可能减少能够发现错误的人类专家数量。一些人建议强制 AI 展示其工作过程，例如生成证明或执行轨迹，以保持问责制。

**标签**: `#AI safety`, `#explainability`, `#expertise`, `#automation`, `#epistemology`

---

<a id="item-4"></a>
## [因果理论应用于理解大语言模型推理](https://cacm.acm.org/news/can-we-understand-how-large-language-models-reason/) ⭐️ 8.0/10

研究人员正在将因果理论应用于大语言模型的机械可解释性，通过分析权重和激活来理解模型如何推理，这在最近的一篇论文和社区讨论中有所探讨。 这种方法可以更深入地理解大语言模型的内部机制，通过揭示模型是真正推理还是仅仅模式匹配，从而提高人工智能的安全性和可信度。 所链接的论文（arXiv:2301.04709）探索了对模型组件的因果干预，例如调整权重和激活，以测试类似推理的行为，其中包含一个涉及时钟时间计算的例子。

hackernews · adunk · 7月12日 18:04 · [社区讨论](https://news.ycombinator.com/item?id=48883090)

**背景**: 机械可解释性是可解释人工智能的一个子领域，它通过逆向工程来理解神经网络的内部算法和电路。由 Judea Pearl 推广的因果理论提供了推断因果关系的工具，研究人员现在将其应用于探究大语言模型是使用真正的推理还是统计相关性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mechanistic_interpretability">Mechanistic interpretability - Wikipedia</a></li>
<li><a href="https://arxiv.org/abs/2501.16496">[2501.16496] Open Problems in Mechanistic Interpretability</a></li>
<li><a href="https://medium.com/@alexglee/causal-ai-current-state-of-the-art-future-directions-c17ad57ff879">Causal AI: Current State-of-the-Art & Future Directions The Role of Causality in Explainable Artificial Intelligence The Role of Causality in Explainable Artificial Intelligence Causal AI: Beyond Correlation to Real Understanding Causality for Artificial Intelligence: From a Philosophical ... Causality and Machine Learning - Microsoft Research</a></li>

</ul>
</details>

**社区讨论**: 社区评论指出，文章侧重于机械可解释性而非哲学意义上的推理，一些人对权重层面的分析能否区分推理与幻觉表示怀疑。一位评论者认为，神经网络的复杂性本质上抵制理解，类似于加密的黑箱。

**标签**: `#mechanistic interpretability`, `#LLMs`, `#causality`, `#AI research`, `#reasoning`

---

<a id="item-5"></a>
## [LLM 创造价值，但前沿实验室可能无法获取](https://geohot.github.io//blog/jekyll/update/2026/07/12/i-love-llms.html) ⭐️ 8.0/10

一篇批判性分析指出，尽管 LLM 创造了巨大价值，但由于商品化和开源竞争，前沿 AI 实验室可能无法获取这些价值。 这挑战了前沿实验室的高估值，表明价值将流向应用和工具而非模型提供商，从而重塑投资和开源格局。 作者押注反对 ASI 时间表，并指出 LLM 带来的生产力提升尚未转化为可见的新软件，因为许多创新在私人家庭实验室中进行。

hackernews · therepanic · 7月12日 18:31 · [社区讨论](https://news.ycombinator.com/item?id=48883343)

**背景**: OpenAI 和 Anthropic 等前沿实验室投入数十亿美元训练大型语言模型，但面临开源替代方案和推理成本商品化的压力。经济辩论的核心在于模型提供商还是下游应用将捕获最大价值。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.amadeuscapital.com/ai-commoditisation-curve/">Charting the AI commoditisation curve: Where will LLM value flow next?</a></li>
<li><a href="https://www.linkedin.com/pulse/ai-productivity-trap-how-frontier-labs-cannibalising-both-tze-weng-ng-ekjmc">The AI Productivity Trap: How Frontier AI Labs Are Cannibalising...</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认同价值获取论点，指出开源模型支持私人定制软件，减少了向上游贡献的动力。一些人认为近期模型改进（如 Sonnet 4、Opus 4.5）正在加速进展，而另一些人则对近期 AGI 持怀疑态度。

**标签**: `#LLMs`, `#AI hype`, `#open source`, `#productivity`, `#economics`

---

<a id="item-6"></a>
## [陶哲轩用现代编码代理构建应用](https://terrytao.wordpress.com/2026/07/11/old-and-new-apps-via-modern-coding-agents/) ⭐️ 8.0/10

菲尔兹奖得主陶哲轩记录了他使用现代编码代理（基于 LLM 的工具）构建新旧应用的经历，分享了实际案例以及对它们能力和局限性的平衡观点。 这表明即使是顶尖数学家也在采用 LLM 辅助编程，标志着软件开发实践的转变。它凸显了 AI 工具对非专业程序员日益增长的可及性，以及释放定制软件潜在需求的潜力。 陶哲轩使用编码代理创建了交互式可视化和其他应用，并指出虽然这些代理对核心研究并非关键任务，但用于辅助工具是可以接受的。他强调理解 LLM 生成代码局限性的重要性。

hackernews · subset · 7月12日 11:09 · [社区讨论](https://news.ycombinator.com/item?id=48880170)

**背景**: 编码代理是将大型语言模型（LLM）封装在应用层中，以协助编程任务（如生成代码、调试和创建可视化）的 AI 工具。随着 GPT-4 和 Claude 等 LLM 的改进，它们越来越受欢迎，即使是非专家也能快速构建软件。然而，它们可能生成不可靠的代码，需要仔细监督。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://magazine.sebastianraschka.com/p/components-of-a-coding-agent">Components of A Coding Agent - by Sebastian Raschka, PhD</a></li>
<li><a href="https://simonwillison.net/2025/Mar/11/using-llms-for-code/">Here’s how I use LLMs to help me write code</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了兴奋和幽默的混合情绪，一些人指出 LLM 使他们能够构建一直想要但没时间做的可视化。其他人开玩笑说菲尔兹奖得主也会像普通人一样遇到 Docker 问题，同时赞赏陶哲轩对该工具优缺点平衡的看法。

**标签**: `#LLM`, `#coding agents`, `#software development`, `#AI-assisted programming`

---

<a id="item-7"></a>
## [带状疱疹疫苗或可降低痴呆风险](https://www.economist.com/leaders/2026/07/09/a-no-brainer-for-protecting-your-brain) ⭐️ 8.0/10

来自英国、澳大利亚和加拿大的观察性研究表明，带状疱疹疫苗（Shingrix）与痴呆诊断的绝对风险降低 1.8%至 3.5%相关，随访时间为 5.5 至 7 年。 如果存在因果关系，这将提供一种安全、广泛可用的干预措施来减轻痴呆负担，影响全球数百万人。同时为理解感染驱动的神经退行性病变开辟了新途径。 这种关联在活疫苗（Zostavax）中最强，但在重组疫苗 Shingrix 中也有观察到。批评者认为，这种效应可能源于健康接种者偏倚或住院次数减少导致偶然诊断的痴呆病例减少。

hackernews · saikatsg · 7月12日 15:23 · [社区讨论](https://news.ycombinator.com/item?id=48881874)

**背景**: 带状疱疹由水痘-带状疱疹病毒再激活引起，该病毒也导致水痘。痴呆，尤其是阿尔茨海默病，是一个日益严重的公共卫生挑战，且预防手段有限。此前研究已将多种感染与痴呆风险增加联系起来，提示疫苗可能在降低该风险中发挥作用。

**社区讨论**: 评论者就因果关系展开辩论：有人强调了英国一项采用严格年龄截断的令人信服的研究，而另一些人则指出一场演讲认为该发现因检测偏倚而具有误导性。还有人分享了自费接种疫苗的个人经历。

**标签**: `#vaccine`, `#dementia`, `#public health`, `#epidemiology`, `#Alzheimer's`

---

<a id="item-8"></a>
## [摩托罗拉 MR2600 路由器发现未认证远程代码执行漏洞](https://mrbruh.com/motorola/) ⭐️ 8.0/10

一名安全研究人员披露了摩托罗拉 MR2600 路由器中的一个未认证远程代码执行漏洞，已发现 42 个暴露的主机，且供应商未予回应。 该漏洞存在被积极利用的高风险，可能允许攻击者完全控制受影响的路由器并用于恶意活动。 该漏洞可通过不安全的 HTTP 端点访问，且路由器的固件更新机制似乎已被废弃，没有官方补丁可用。

hackernews · MrBruh · 7月12日 11:52 · [社区讨论](https://news.ycombinator.com/item?id=48880406)

**背景**: 摩托罗拉 MR2600 是一款双频 AC2600 WiFi 路由器。然而，该路由器上的“Motorola”品牌是授权使用的；实际制造商是 Zoom，该公司于 2023 年破产，其资产在 2024 年被 e2Companies 收购。这种复杂的所有权历史解释了供应商为何不予回应。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.homeowner.com/connectivity/motorola/motorola-mr2600-review">Motorola MR 2600 (AC2600) Review: Best Home WiFi Router ?</a></li>
<li><a href="https://www.modemguides.com/products/motorola-mr2600">Motorola MR 2600 Dual-Band AC2600 Wireless Router</a></li>
<li><a href="https://www.newegg.com/p/3C6-0129-00035">Motorola AC2600 4x4 WiFi Smart Gigabit Router with... - Newegg.com</a></li>

</ul>
</details>

**社区讨论**: 评论者提到了德国“Störerhaftung”法律下的责任问题，并建议白帽黑客可能考虑自行修补暴露的主机。其他人则澄清了复杂的供应商历史，解释了为何供应商不予回应。

**标签**: `#security`, `#vulnerability`, `#IoT`, `#RCE`, `#networking`

---

<a id="item-9"></a>
## [AI 提升研究效率但缩小思想范围](https://spectrum.ieee.org/ai-science-research-flattens-discovery) ⭐️ 8.0/10

一项新研究显示，采用 AI 的科学家发表的论文数量增加三倍，引用次数增加近五倍，并更早成为团队领导者，但探索的科学思想范围却缩小了。 这一发现凸显了 AI 辅助研究中的关键权衡：虽然 AI 提升了个体生产力和职业发展，但可能减少智力多样性和科学发现的广度。 研究发现，采用 AI 的研究人员集中在相似主题上，导致思想景观变得扁平。这种效应更多归因于研究系统中的激励机制，而非 AI 架构本身。

hackernews · zaikunzhang · 7月12日 13:26 · [社区讨论](https://news.ycombinator.com/item?id=48881043)

**背景**: 该研究考察了 AI 对科学研究的影响，重点关注生产力指标和思想多样性。“Babble 假说”认为研究人员可能优先考虑发表数量而非原创性，而 AI 可能放大这一趋势。

**社区讨论**: 评论者普遍认为 AI 放大了研究中现有的激励机制，许多人指向“Babble 假说”和发表压力。一些人质疑在 AI 采用之前，原创性较低的工作是否已经获得了更多引用，暗示更广泛的网络效应。

**标签**: `#AI`, `#research`, `#science policy`, `#incentives`, `#productivity`

---

<a id="item-10"></a>
## [HN 用户提议为 AI 生成文章添加标记](https://news.ycombinator.com/item?id=48886741) ⭐️ 7.0/10

一位 Hacker News 用户提议添加一个标记来标识 AI 生成的文章，让读者可以跳过而不影响排名。该建议引发了关于审核和 AI 内容角色的社区讨论。 该提议回应了社交平台上对 AI 生成内容质量和真实性的日益担忧。如果实施，可能会影响其他社区处理 AI 内容的方式，并为透明度树立先例。 该标记不会降低文章排名，而是作为偏好人类撰写内容的用户的指示器。开放问题包括投票系统是否足够，以及 HN 是否应适应生成式 AI 时代。

hackernews · levkk · 7月13日 01:24

**背景**: Hacker News (HN) 是一个专注于计算机科学和创业的社交新闻网站，以其严格的审核和社区驱动的内容排名而闻名。该网站已禁止在评论中使用 AI 生成的文本，但对文章没有相关规定。该提议反映了平台应如何处理 AI 生成内容的更广泛讨论。

**社区讨论**: 社区成员表达了不同观点：一些人认为内容质量比来源更重要，而另一些人则担心误报和恶意指控。HN 版主 dang 指出，社区普遍对 AI 生成的文章持保留态度，但执行仍具挑战性。

**标签**: `#AI`, `#moderation`, `#Hacker News`, `#content policy`

---

<a id="item-11"></a>
## [8 位计算机的引脚级仿真](https://floooh.github.io/tiny8bit-preview/index.html) ⭐️ 7.0/10

发布了一个 8 位计算机的小型仿真器集合，采用引脚级仿真模型，实现了快速加载和精确模拟。 这种复古计算仿真的新颖方法比传统仿真器具有更高的准确性和灵活性，可能通过 WebAssembly 为浏览器中的硬件仿真设定新标准。 这些仿真器使用 WebAssembly 构建，可以在网络浏览器中以接近原生的性能运行。引脚级模型模拟单个芯片引脚及其时序，实现周期精确的行为。

hackernews · naves · 7月12日 20:23 · [社区讨论](https://news.ycombinator.com/item?id=48884395)

**背景**: 传统仿真器通常使用更高级别的抽象，牺牲部分准确性以换取速度。引脚级仿真模拟组件之间的精确电气连接，提供更忠实于原始硬件行为的再现。这种技术常用于硬件设计验证，但在复古计算仿真中很少见。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Hardware_emulation">Hardware emulation - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/List_of_computer_system_emulators">List of computer system emulators - Wikipedia</a></li>
<li><a href="https://dev.to/frqan/building-a-ti-84-plus-ce-emulator-in-webassembly-lessons-from-100-browser-based-calculator-3mlg">Building a TI-84 Plus CE Emulator in WebAssembly : Lessons from...</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞引脚级模型的模块化灵活性和快速加载时间，一位用户回忆起以前从磁带加载游戏需要很长时间。有人请求支持更多系统，如 Oric 和 Commodore 64，另一位指出某些仿真器的音量意外偏高。

**标签**: `#emulation`, `#retrocomputing`, `#hardware simulation`, `#webassembly`

---

<a id="item-12"></a>
## [谷歌研究：更智能的路线规划可减少交通拥堵](https://research.google/blog/the-power-of-collaboration-how-we-can-reduce-traffic-congestion/) ⭐️ 7.0/10

谷歌进行了一项为期六个月的全市实验，修改了 Google Maps 的路线规划算法，优先推荐具有相似行驶时间的替代路线，从而将交通流量从拥堵路段分散开来。研究发现，这种干预措施在不显著增加个人驾驶时间的情况下减少了拥堵。 这项研究表明，对导航应用进行微小的算法调整即可对城市交通拥堵产生可衡量的影响，提供了一种低成本、可扩展的解决方案。然而，它也凸显了考虑基础设施磨损和系统性城市规划的必要性，因为重新分配交通可能会加速对承载能力较弱路段的损坏。 该实验采用了全市范围的切换（交叉）设计，在六个月内连续交替使用修改后的和未修改的路线规划算法。修改后的算法引导出行避开预先选定的拥堵路段，同时保持行驶时间相似，但社区评论者指出，道路按不同标准建造，绕行路线上的交通增加可能导致道路更快恶化。

hackernews · raahelb · 7月12日 15:35 · [社区讨论](https://news.ycombinator.com/item?id=48881967)

**背景**: 交通拥堵是一个主要的城市问题，像 Google Maps 这样的导航应用通常为驾驶员规划最快路径，这可能导致交通集中在某些道路上。本研究探索了一种替代方法：算法不再为每个驾驶员优化最快路线，而是旨在平衡整个网络的交通流量。这一概念类似于计算机网络中的负载均衡，即分散流量以避免任何单一路径过载。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Routing">Routing - Wikipedia</a></li>
<li><a href="https://arxiv.org/html/2402.15749v1">A summary of the routing algorithm and their optimization,performance</a></li>
<li><a href="https://scrap.io/google-maps-route-planning-technology-20-years">Google Maps Route Planning in 2026: The Technology Behind 2 Billion Daily Navigations | Scrap.io</a></li>

</ul>
</details>

**社区讨论**: 社区评论提出了若干担忧：有人认为拥堵的根本原因是城市扩张和缺乏混合用途社区，而非路线规划算法。另一些人指出，道路按不同标准建造，将交通分流到承载能力较弱的道路上可能导致快速恶化和意外的维修成本。少数评论者建议，拥堵收费或改善公共交通将是更有效的解决方案。

**标签**: `#traffic congestion`, `#Google Maps`, `#routing algorithms`, `#urban planning`, `#experimental design`

---

<a id="item-13"></a>
## [反对有用性：为玩乐而重拾计算](https://www.motivenotes.ai/p/against-usefulness) ⭐️ 7.0/10

一篇新文章批评科技行业对“有用性”的执念，主张受 Bret Victor 的 Dynamicland 项目启发，将计算重新作为探索和玩乐的媒介。 这篇哲学批评挑战了计算领域主流的生产力导向范式，可能影响开发者和设计师对待人机交互与创意工具的方式。 文章提到了 Bret Victor 在奥克兰的实验室 Dynamicland，并提及纽约的 Folk Computer 项目作为另一种替代计算范式。该新闻在聚合器上得分为 7.0/10，获得 98 个点赞和 24 条评论。

hackernews · supo · 7月12日 17:47 · [社区讨论](https://news.ycombinator.com/item?id=48882956)

**背景**: Bret Victor 是人机交互领域的知名研究者，以“Inventing on Principle”等动态、可探索媒介的工作而闻名。Dynamicland 是一个研究实验室，探索协作式物理计算环境，人们通过有形物体而非屏幕和键盘与信息互动。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cognitivemedium.com/emm/emm.html">Toward an exploratory medium for mathematics</a></li>

</ul>
</details>

**社区讨论**: 评论者对替代计算范式表现出兴趣，有人指出触觉任务规划的潜力，有人提倡数字化手写笔输入，还有人寻求在教育领域进行物理计算的合作者。

**标签**: `#computing philosophy`, `#human-computer interaction`, `#Dynamicland`, `#creativity`, `#technology critique`

---

<a id="item-14"></a>
## [Ghostel.el：基于 libghostty 的快速 Emacs 终端模拟器](https://dakra.github.io/ghostel/) ⭐️ 7.0/10

Ghostel.el 是一款新的 Emacs 终端模拟器，它利用 libghostty-vt 进行终端状态管理，相比 vterm 和 eat 提供了更快的性能和更可靠的输入处理。 这将 Ghostty 终端模拟器的性能优势带给 Emacs 用户，使得 TUI 应用程序运行更流畅，并提升了 Emacs 内的整体终端体验。 Ghostel 基于 libghostty-vt 构建，这是一个从 Ghostty 核心提取的零依赖库。目前它还有一些粗糙之处，例如偶尔的终端清除失败和需要杀死缓冲区才能解决的冻结问题。

hackernews · signa11 · 7月12日 08:52 · [社区讨论](https://news.ycombinator.com/item?id=48879504)

**背景**: Ghostty 是一个快速、功能丰富、跨平台的终端模拟器，使用 GPU 加速和原生 UI。libghostty 是一个兼容 C 语言的库，允许将 Ghostty 的终端模拟嵌入到其他应用程序中，其中 libghostty-vt 是第一个组件，用于解析终端序列和维护状态。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/Uzaaft/awesome-libghostty">GitHub - Uzaaft/awesome-libghostty</a></li>
<li><a href="https://mitchellh.com/writing/libghostty-is-coming">Libghostty Is Coming – Mitchell Hashimoto</a></li>
<li><a href="https://docsmith.aigne.io/docs/ghostty/en/libghostty-ed730d">libghostty API</a></li>

</ul>
</details>

**社区讨论**: 用户报告称 Ghostel 比 vterm 明显更快、更可靠，且 ELisp API 更友好，但有些人遇到了偶尔的清除问题和冻结。维护者确认该项目仍处于早期阶段，并计划很快进行 Show HN。

**标签**: `#Emacs`, `#terminal emulator`, `#libghostty`, `#open source`, `#performance`

---

<a id="item-15"></a>
## [电影 CGI 与 AI：软件工程的类比](https://fabiensanglard.net/extinct/index.html) ⭐️ 7.0/10

Fabien Sanglard 发表了一篇文章，将电影行业从实景特效转向 CGI 与软件工程采用 LLM 进行类比，认为 AI 会贬低传统技能，但适应者将蓬勃发展。 这一类比提供了历史视角，帮助理解 LLM 对软件工程的潜在长期影响，突出了技能贬值的风险和适应的重要性，与当前关于 AI 在行业中角色的辩论相呼应。 文章指出，CGI 之所以占据主导地位，部分原因是数字视觉特效公司未成立工会，可以以牺牲艺术家福利为代价削减成本，而 LLM 在软件工程中可能也会出现类似情况。文章还承认，实景特效正在复苏，因为观众认识到其更优的质量。

hackernews · zdw · 7月12日 15:17 · [社区讨论](https://news.ycombinator.com/item?id=48881830)

**背景**: CGI（计算机生成图像）因成本更低、周转更快而取代了电影中的许多实景特效，但往往以牺牲艺术家工作条件和感知质量为代价。类似地，像 GPT-4 这样的 LLM（大语言模型）正被用于软件工程以提高生产力，引发了关于技能贬值和岗位替代的担忧。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.lafilm.edu/blog/practical-effects-vs-cgi-2/">Practical Effects vs. CGI | The Los Angeles Film School</a></li>
<li><a href="https://www.lafilm.edu/blog/practical-effects-vs-cgi/">Practical Effects vs CGI – The Los Angeles Film School</a></li>
<li><a href="https://berkeleyhighjacket.com/2023/entertainment/cgi-vs-practical-effects-impacts-on-the-authenticity-of-film">CGI vs. practical effects: Impacts on the authenticity of film | The Berkeley High Jacket</a></li>

</ul>
</details>

**社区讨论**: 评论者就这一类比的深度展开辩论，指出 CGI 的兴起得益于非工会劳动力和对艺术家的恶劣待遇，而 LLM 也可能出现类似情况。一些人质疑生产力论点，认为在软件工程中产出量很少是关键评估指标，而另一些人则强调学习 LLM 但不过度依赖的重要性。

**标签**: `#AI`, `#software engineering`, `#labor`, `#LLM`, `#analogy`

---

<a id="item-16"></a>
## [Odin 编程语言逐渐流行](https://odinbook.com/) ⭐️ 7.0/10

一本新书和社区讨论强调 Odin 是一种高性能、低开销的系统编程语言，具有出色的 C 互操作性，吸引了寻求 Rust 和 Zig 替代方案的开发者。 Odin 为系统编程提供了比 Rust 和 Zig 更简单、更明确的替代方案，可能拓宽生态系统并吸引那些认为其他语言过于复杂的开发者。 Odin 由 Bill Hall（Ginger Bill）于 2016 年开始创建，其设计目标包括明确性、高性能和数据导向编程。该语言已用于 STM32 固件、Web 和桌面应用程序。

hackernews · AlexeyBrin · 7月12日 12:08 · [社区讨论](https://news.ycombinator.com/item?id=48880499)

**背景**: Odin 是一种具有独特类型系统的通用系统编程语言，专为高性能和现代系统而构建。它与 Rust 和 Zig 等语言竞争，这些语言也强调安全性和性能，但学习曲线更陡峭。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://odin-lang.org/">Odin Programming Language</a></li>
<li><a href="https://grokipedia.com/page/Odin_programming_language">Odin (programming language)</a></li>

</ul>
</details>

**社区讨论**: 社区成员称赞 Odin 的易用性、快速编译和出色的 C 互操作性，一位用户指出其开销甚至比 Zig 还低。一些人希望有原生的继承支持，但总体评价是积极的。

**标签**: `#programming languages`, `#systems programming`, `#Odin`, `#C interop`, `#performance`

---

<a id="item-17"></a>
## [Chromium 148 的 Math.tanh 可识别操作系统](https://scrapfly.dev/posts/browser-math-os-fingerprint/) ⭐️ 7.0/10

自 Chromium 148 起，Math.tanh 的实现因操作系统而异，单次调用即可揭示底层操作系统。这创建了一个新的浏览器指纹向量，可将用户与其操作系统关联起来。 这一发现扩展了浏览器指纹识别的工具集，即使伪造用户代理也可能泄露操作系统信息，削弱隐私保护。它凸显了追踪技术与隐私措施之间的持续博弈，影响所有网络用户。 该指纹利用不同操作系统的数学库在特定输入下对 Math.tanh 产生微小差异。该技术足以区分 macOS、Linux 和 Windows，甚至可能指示浏览器版本范围。

hackernews · joahnn_s · 7月12日 21:12 · [社区讨论](https://news.ycombinator.com/item?id=48884853)

**背景**: 浏览器指纹识别通过收集设备特定信息（如屏幕分辨率、字体、已安装插件）来识别用户，无需使用 Cookie。Math.tanh 是双曲正切函数，由浏览器 JavaScript 引擎实现，并委托给底层操作系统的数学库。不同操作系统在浮点精度或舍入上的差异产生了可检测的特征。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Browser_fingerprinting">Browser fingerprinting</a></li>
<li><a href="https://learn.microsoft.com/en-us/dotnet/api/system.math.tanh?view=net-10.0">Math.Tanh (Double) Method (System) | Microsoft Learn</a></li>
<li><a href="https://fingerprint.com/blog/browser-fingerprinting-techniques/">Browser Fingerprinting Techniques: 6 Top Methods Explained</a></li>

</ul>
</details>

**社区讨论**: 评论者指出该指纹还可能揭示浏览器版本范围，有人批评文章可能是 AI 生成的，质疑其动机。其他人呼吁采用正确舍入的数学函数以消除此类侧信道泄露，还有人调侃说连 emoji 渲染时间都可能成为指纹。

**标签**: `#browser fingerprinting`, `#privacy`, `#Chromium`, `#JavaScript`, `#security`

---

<a id="item-18"></a>
## [LLM 代理不应成为直接责任人](https://simonwillison.net/2026/Jul/12/directly-responsible-individuals/#atom-everything) ⭐️ 7.0/10

Simon Willison 认为，LLM 驱动的代理绝不应被指定为直接责任人（DRI），因为它们无法承担责任，这一观点借鉴了苹果和 GitLab 的 DRI 概念。 这很重要，因为随着 LLM 代理在组织中的部署日益增多，明确责任必须由人类承担可以防止责任分散并确保伦理监督。 DRI 概念起源于苹果，并在 GitLab 手册中被定义为对项目成败最终负责的人。Willison 引用了 IBM 1979 年的培训幻灯片，其中指出计算机永远不能承担责任。

rss · Simon Willison · 7月12日 23:57

**背景**: 直接责任人（DRI）是指被明确分配对任务、决策或结果承担唯一责任的人，这一做法由苹果推广以减少模糊性。LLM 驱动的代理是能够自主执行任务的 AI 系统，但它们缺乏道德或法律责任能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://handbook.gitlab.com/handbook/people-group/directly-responsible-individuals/">Directly Responsible Individuals (DRI) - The GitLab Handbook</a></li>

</ul>
</details>

**标签**: `#organizational culture`, `#accountability`, `#LLM agents`, `#software engineering`

---

<a id="item-19"></a>
## [首次 PCB 设计与组装之旅](https://vilkeliskis.com/b/2026/0711.html) ⭐️ 6.0/10

一篇个人博客文章详细描述了作者设计和组装第一块印刷电路板（PCB）的经历，并指出定制制造服务的低成本和高可及性。 这突显了定制 PCB 制造变得多么实惠，使得爱好者和专业人士能够轻松进行硬件原型设计，从而促进电子领域的创新。 作者采用了简单的通孔元件设计，并从 JLCPCB 等中国制造商订购了电路板，这些制造商提供低成本、快速周转的原型制作服务。

hackernews · tadasv · 7月12日 22:56 · [社区讨论](https://news.ycombinator.com/item?id=48885728)

**背景**: 印刷电路板（PCB）通过导电线路机械支撑并电气连接电子元件。传统上，爱好者使用化学品在家蚀刻电路板，但现代服务允许以几美元的价格在线订购定制 PCB，使过程更简单、更可靠。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://resources.altium.com/p/pcb-design-basics-new-designers">PCB Design Basics for New Designers | Getting Started</a></li>
<li><a href="https://www.pcbelec.com/blog/pcb-cost-and-budgeting/what-factors-determine-the-price-of-pcb.html">2025 Custom PCB Cost Factors: Pricing Guide | JHYPCB</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞了定制 PCB 的实惠性，有人推荐 JLCPCB 并分享了类似的首次 PCB 经历。一位用户怀旧地回忆了家庭蚀刻方法，引发了关于 DIY 与从中国订购的讨论。

**标签**: `#PCB design`, `#electronics`, `#DIY`, `#hardware`

---

<a id="item-20"></a>
## [摆脱屏幕成瘾，重获深度阅读能力](https://substack.magazinenongrata.com/p/how-i-learned-to-read-again) ⭐️ 6.0/10

Substack 上的一篇个人随笔描述了作者因屏幕成瘾而失去深度阅读能力，并提出了重获这种能力的策略，如设定专门的阅读时间和练习主动阅读技巧。 这篇随笔引起了许多在数字时代注意力分散的人的共鸣，突显了从深度阅读到快速浏览的普遍认知转变，这种转变影响了批判性思维和理解能力。 作者指出他们的阅读巅峰在 11-12 岁，社区评论引用了 Paul Graham 的观点，认为深度阅读者将是唯一能良好思考的人，以及 Mortimer Adler 的《如何阅读一本书》，该书探讨了六年级之后的阅读策略。

hackernews · georgex7 · 7月12日 18:22 · [社区讨论](https://news.ycombinator.com/item?id=48883238)

**背景**: 深度阅读是指长时间专注于文本、理解复杂论点和细微差别的能力，与屏幕上常见的快速浏览和扫描相对。屏幕成瘾指对数字设备的强迫性使用，常导致注意力持续时间缩短和专注阅读能力下降。

**社区讨论**: 评论者分享了个人在屏幕成瘾和多动症方面的挣扎，并讨论了区分阅读长文章和书籍的价值。一些人引用 Paul Graham 和 Mortimer Adler 来强调深度阅读对清晰思考的重要性。

**标签**: `#reading`, `#attention`, `#digital habits`, `#self-improvement`

---

<a id="item-21"></a>
## [状态更新之死：55%美国人停止发帖](https://ca.pcmag.com/social-media/16790/the-death-of-the-status-update-why-55-of-americans-stopped-posting-on-social-media) ⭐️ 6.0/10

最近一项分析显示，55%的美国人已停止在社交媒体上发帖，原因是算法推送优先展示病毒式内容而非好友动态，导致交流转向私人群聊。 这一转变标志着社交媒体使用方式的根本变化，原本用于公开分享的平台在个人联系方面逐渐失去相关性，可能影响用户参与度和广告模式。 该分析基于一项调查和社区讨论，指出用户因算法筛选感到帖子无人关注，许多人已转向群聊进行有意义的互动。

hackernews · thunderbong · 7月12日 10:14 · [社区讨论](https://news.ycombinator.com/item?id=48879902)

**背景**: Facebook 和 Instagram 等社交媒体平台已逐渐从按时间顺序推送转向算法推送，优先展示可能最大化参与度的内容，如病毒式视频。这一变化降低了来自朋友和家人的个人动态的可见性。结果，曾经定期发帖的用户现在发现分享的动力不足，因为他们的内容很少能到达目标受众。

**社区讨论**: 评论者普遍认为算法推送扼杀了个人发帖，许多人指出群聊已成为真正社交互动的主要空间。一些用户报告说，他们的信息流现在充斥着陌生人的无关内容，进一步抑制了发帖意愿。

**标签**: `#social media`, `#user behavior`, `#algorithms`, `#community discussion`

---

<a id="item-22"></a>
## [Anthropic 再次延长 Claude Fable 5 访问期限](https://simonwillison.net/2026/Jul/12/bump/#atom-everything) ⭐️ 6.0/10

Anthropic 以计算资源限制为由，将所有付费计划中的 Claude Fable 5 访问权限延长至 2026 年 7 月 19 日；与此同时，OpenAI 取消了 GPT-5.6 Sol 的使用限制，并宣布了效率改进。 这凸显了 Anthropic 与 OpenAI 之间的竞争压力，模型可用性和定价策略直接影响用户采纳。Anthropic 的多次延期可能削弱用户信任，而 OpenAI 的自信姿态可能吸引更多订阅者。 Claude Fable 5 用户每周最多可将一半的使用额度用于 Fable 5，之后可使用积分或切换模型。OpenAI 的 GPT-5.6 Sol 暂时取消了 Plus、Business 和 Pro 计划的 5 小时使用限制，并推出了效率改进以减少用量消耗。

rss · Simon Willison · 7月12日 21:20

**背景**: Claude Fable 5 是 Anthropic 能力最强且广泛发布的模型，专为高难度推理和长期代理任务设计。GPT-5.6 Sol 是 OpenAI GPT-5.6 系列中的旗舰前沿模型，在编程、科学和网络安全方面具有强大能力。这两款模型代表了 AI 的前沿水平，其可用性是用户选择的关键因素。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/claude/fable">Claude Fable \ Anthropic</a></li>
<li><a href="https://openai.com/index/previewing-gpt-5-6-sol/">Previewing GPT-5.6 Sol: a next-generation model | OpenAI</a></li>
<li><a href="https://support.claude.com/en/articles/11049741-what-is-the-max-plan">What is the Max plan? | Claude Help Center</a></li>

</ul>
</details>

**标签**: `#AI`, `#Anthropic`, `#Claude`, `#GPT-5`, `#compute constraints`

---

<a id="item-23"></a>
## [仅用相机实现 CGI 动作捕捉](https://hackaday.com/2026/07/12/cgi-motion-capture-with-only-a-camera/) ⭐️ 6.0/10

Hackaday 的一篇文章复兴了 1990 年代的 VFX 设备方法，展示了仅用相机（无需专用硬件）即可实现 CGI 动作捕捉。 这项技术可能降低独立电影制作人和爱好者的门槛，使动作捕捉无需昂贵设备即可实现。 该方法复兴了 1990 年代的 VFX 设备概念，依靠计算机视觉算法从单个摄像头画面中追踪运动。

rss · Hackaday · 7月13日 05:00

**背景**: 传统动作捕捉需要专用硬件，如标记点、动作捕捉服或多台相机。1990 年代已有仅用相机的早期实验，但计算能力有限阻碍了应用。现代计算机视觉的进步使这种方法变得可行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Visual_effects">Visual effects - Wikipedia</a></li>

</ul>
</details>

**标签**: `#CGI`, `#motion capture`, `#computer vision`, `#VFX`

---

<a id="item-24"></a>
## [1964 年的人工智能预言至今仍引发共鸣](https://hackaday.com/2026/07/12/musing-on-ai-from-1964/) ⭐️ 6.0/10

Hackaday 的一篇文章重点介绍了 Irving John Good 在 1964 年发表的论文《关于第一台超智能机器的猜想》，并将其预言与现代人工智能发展进行了类比。 这一历史视角表明，关于超智能 AI 的基础思想早在几十年前就已出现，提醒我们当前的讨论有着深厚的根源，并且一些预言至今仍有现实意义。 Good 的论文推测，超智能机器可以设计出更好的机器，从而引发“智能爆炸”。文章引用了这一概念，但未提供新的技术分析。

rss · Hackaday · 7月13日 02:00

**背景**: Irving John Good 是一位英国数学家和密码学家，曾与艾伦·图灵共事。他在 1964 年的论文中提出了“超智能机器”的概念，这种机器能超越人类智力，并可能递归地自我改进。这一思想后来影响了关于技术奇点的讨论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.sciencedirect.com/science/chapter/bookseries/pii/S0065245808604180">Speculations Concerning the First Ultraintelligent Machine*</a></li>
<li><a href="https://vtechworks.lib.vt.edu/bitstream/handle/10919/89424/TechReport05-3.pdf">Speculations Concerning the First Ultraintelligent Machine*</a></li>
<li><a href="https://www.flyingpenguin.com/wp-content/uploads/2022/04/good-1964-.pdf">Speculations Concerning the First Ultraintelligent Machine*</a></li>

</ul>
</details>

**标签**: `#AI`, `#history`, `#philosophy`

---

<a id="item-25"></a>
## [将 Nvidia GPU 驱动移植到 Haiku 以实现 3D 加速](https://hackaday.com/2026/07/12/porting-the-nvidia-gpu-driver-to-haiku-for-3d-acceleration/) ⭐️ 6.0/10

开发者正在将 Nvidia 的开源 GPU 内核驱动移植到 Haiku 操作系统，旨在为该操作系统带来 3D 加速能力。这项工作以 Nvidia 基于 MIT 许可证发布的 Linux 驱动代码为起点。 此次移植可能显著提升 Haiku 的图形能力，使其更适合现代桌面使用，并吸引开发者和用户关注这一小众操作系统。它展示了在不同操作系统间复用开源驱动的潜力。 此次移植由开发者[X512]主导，基于 Nvidia 以 MIT 许可证发布的开源 GPU 内核模块。工作仍在进行中，可能因 Haiku 独特的内核架构而面临挑战。

rss · Hackaday · 7月12日 20:00

**背景**: Haiku 是一款受 BeOS 启发的免费开源操作系统，专为个人电脑设计。它已处于 beta 开发阶段多年，但缺乏对许多现代 GPU 的原生 3D 加速支持，这限制了其在图形密集型应用中的可用性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hackaday.com/2026/07/12/porting-the-nvidia-gpu-driver-to-haiku-for-3d-acceleration/">Porting The Nvidia GPU Driver To Haiku For 3D Acceleration | Hackaday</a></li>
<li><a href="https://en.wikipedia.org/wiki/Haiku_(operating_system)">Haiku (operating system) - Wikipedia</a></li>

</ul>
</details>

**标签**: `#Haiku OS`, `#GPU driver`, `#Nvidia`, `#3D acceleration`, `#open source`

---

<a id="item-26"></a>
## [通过超声探头实现无声语音](https://hackaday.com/2026/07/12/speak-silently-with-an-ultrasound-probe/) ⭐️ 6.0/10

一个原型系统利用超声探头读取舌头运动，并通过机器学习将其解码为语音，从而实现无声的计算机交互。 这项技术提供了一种无需发出声音即可私密地与计算机交互的新方式，可能对隐私敏感环境和无障碍访问有益。 据 Aleph Neuro 报道，该系统在开放词汇语音上实现了 15.6%的词错误率，并能跨不同人群泛化。

rss · Hackaday · 7月12日 14:00

**背景**: 无声语音接口（SSI）在不发出声音的情况下解码发音或神经信号。舌头的超声成像是一种模态，结合机器学习来预测意图语音。这种方法不同于喉部麦克风或基于 EEG 的系统。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hackaday.com/2026/07/12/speak-silently-with-an-ultrasound-probe/">Speak Silently With An Ultrasound Probe | Hackaday</a></li>
<li><a href="https://alephneuro.com/blog/silent-speech">Silent speech with ultrasound — Aleph</a></li>
<li><a href="https://www.nature.com/articles/s44460-025-00010-2">Sensing technologies for silent speech interfaces - Nature</a></li>

</ul>
</details>

**标签**: `#ultrasound`, `#speech recognition`, `#privacy`, `#HCI`

---

<a id="item-27"></a>
## [激光引导真菌艺术：融合生物学与数字制造](https://hackaday.com/2026/07/12/printing-fungal-art-with-laser-control/) ⭐️ 6.0/10

Kexin Wang 的 Funguy 项目利用激光二极管在琼脂凝胶上反复勾勒图案，利用真菌的趋光性引导其生长成预设的艺术形状。 该项目展示了生物学与数字制造的新颖结合，为艺术和设计中活体材料的应用开辟了可能性，并可能激发受控生物生长的新方法。 真菌具有趋光性，即避免光线，因此激光有效地创建了一个“围栏”边界，真菌在其周围生长。该系统使用激光二极管和模拟来同步图案与实际生长。

rss · Hackaday · 7月12日 11:00

**背景**: 生物艺术将生物技术与艺术表达相结合，常以活体生物为媒介。激光切割和 3D 打印等数字制造技术越来越多地与生物材料融合，以创造互动或活体艺术品。真菌生长受光照、温度和营养影响，使其成为此类项目中可控的媒介。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hackaday.com/2026/07/12/printing-fungal-art-with-laser-control/">Printing Fungal Art With Laser Control - Hackaday</a></li>
<li><a href="https://dl.acm.org/doi/full/10.1145/3680530.3695440">Exploring Fungal Morphology Simulation and Dynamic Light ...</a></li>
<li><a href="https://dfabclass.com/intro/digital-biofabrication/">Digital BioFabrication – Intro to Digital Fabrication</a></li>

</ul>
</details>

**标签**: `#bioart`, `#digital fabrication`, `#fungi`, `#laser control`

---


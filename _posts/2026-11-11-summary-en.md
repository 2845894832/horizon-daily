---
layout: default
title: "Horizon Summary: 2026-11-11 (EN)"
date: 2026-11-11
lang: en
---

> From 65 items, 5 important content pieces were selected

---

**AI Opportunity Radar**
1. [Resend 的 AEO 打法](#item-ai-opportunity-1) ⭐️ 6.0/10
2. [AlphaProof Code 形式化验证智能体](#item-ai-opportunity-2) ⭐️ 5.0/10
3. [Anthropic 漏洞发现追踪](#item-ai-opportunity-3) ⭐️ 5.0/10
4. [ZONOS3-Mini 开源 TTS 模型](#item-ai-opportunity-4) ⭐️ 5.0/10
5. [Qwen4-Max 预览版上线 Token Plan](#item-ai-opportunity-5) ⭐️ 5.0/10

---

## AI Opportunity Radar

<a id="item-ai-opportunity-1"></a>
### [Resend 的 AEO 打法](https://latent.space/p/resend/) ⭐️ 6.0/10

这是一期 latent.space 播客，嘉宾是 Resend 联合创始人兼 CEO Zeno Rocha，主题是 Resend 如何让 AI agent 在推荐邮件服务时优先选中自己，也就是他所说的 AEO（Agent Experience Optimization）。具体做法包括：用 React Email 模板作为早期获客切入点，在定价页 URL 后加 .md 让 agent 一次请求就能读到价格表，以及把 MCP server 从上线时约 20 个工具扩展到 80 多个。Rocha 在录制时称 Resend 有 430 万用户和 12 万付费客户，这是官方说法，没有独立审计。节目还引用了一项第三方研究：在 Claude Code 的 102 次邮件推荐中，Resend 被首选 64 次，SendGrid 首选 7 次但作为备选出现 55 次；latent.space 自己的后续研究则显示 Postmark 在多数模型下排第一。

rss · Latent Space · Nov 10, 20:05

**「Why now」** The window is defined by agent-mediated tool selection becoming measurable: an AEO study cited in the episode found Claude Code picked Resend first in 64 of 102 email recommendations, while a newer Latent Space study put Postmark on top for most models — meaning the ranking is still fluid and not locked in by incumbents. Resend&\#x27;s own tactics \(a \`.md\` version of the pricing page, an MCP server grown from ~20 to 80+ tools\) are cheap to copy, so the edge is available to small teams today. How long this stays open cannot be judged from the supplied material; the source gives no data on how quickly model defaults or vendor adoption shift.

**「能不能做成产品」** 可以做一个轻量工具或服务，但天花板不高。目标用户是中小 SaaS 和开发者工具团队，他们的麻烦是：不知道 agent 会怎么描述自家产品，也不知道自家定价页、文档、MCP server 在 agent 眼里是否可读。MVP 可以是一个“agent 可读性体检”工具：抓取目标站点的定价页和文档，生成 .md 版本，模拟几个主流模型问“该用哪个 X 服务”，记录推荐结果和引用来源，输出一份可执行的修改清单。收费可以按月订阅（按监测的 prompt 数量和模型数量分档），也可以做成一次性脚本或报告买断。两三人小团队几周内能做出原型，难点不在技术，而在持续调用模型做推荐测试的成本，以及说服客户为“agent 推荐排名”这种难以归因的效果付费。

**「能不能接单」** 有服务需求迹象，但证据只来自这一期节目和它引用的研究，没有看到真实的采购方。可能买单的是已经有一定流量、但发现 agent 推荐里排不到前面的 SaaS 团队，交付物包括：给定价页和文档加 .md 端点、写 llms.txt、设计或精简 MCP server 的工具集、做一轮跨模型的推荐基线测试并出报告。这类需求目前主要出现在开发者社区和播客讨论里，没有看到招聘岗位或明确的付费案例，所以更适合作为已有客户资源的附加服务，而不是独立获客的生意。

**「Market signal」** The only concrete commercial numbers in the source are Resend&\#x27;s own, stated by CEO Zeno Rocha on the podcast: 4.3 million users and 120,000 paying customers at recording time. These are company claims, not independently audited, and the episode discloses no revenue, pricing tiers, or AEO-specific spend. No pricing or paid-customer data for AEO services as a category appears in the source. External probes suggest the underlying convention is real but unevenly adopted: one 2026 scan of 93 ranking pages found 117 of 123 fetched URLs returning HTTP 200 for llms.txt-style endpoints \(tool-1-1\), while a ten-site probe of AI and dev-infrastructure operators found only four of ten shipping llms.txt \(tool-1-2\), and a Tranco top-5,000 snapshot tracks adoption at that scale \(tool-1-3\). Those results measure file presence, not willingness to pay for help producing it.

**「风险」** 最大的风险是这件事的效果无法稳定归因：模型版本一换，推荐结果就可能变，节目里也提到不同模型和不同研究给出的第一名并不一致（Resend 与 Postmark 各有领先）。另外，如果各家模型厂商自己优化工具调用和推荐逻辑，或者平台把 .md、llms.txt 这类做法标准化成免费功能，第三方 AEO 服务的空间会被压缩。

**「评论区」** 没有可用的社区评论。节目里唯一接近实战经验的是 Rocha 自己的做法：打开 agent 会话里折叠的工具调用结果，看模型实际收到了多少数据，他发现有一次返回结果大到放不进上下文，而单纯减少工具数量并不能解决这个问题。这是个人经验，不是社区共识。

<details><summary>References</summary>
<ul>
<li><a href="https://alexturik.com/aeo/research-2026">AEO Adoption Scan 2026 : What 93 Ranking Pages Ship</a></li>
<li><a href="https://agentsite.app/llms-txt-field-report-2026-05">llms . txt adoption across 10 AI and dev-infrastructure sites — agentsite</a></li>
<li><a href="https://geoplaybooks.com/data/llms-txt-adoption-2026/">llms . txt adoption in the Tranco top 5,000 (July 2026 ) — GEO/ AEO ...</a></li>
<li><a href="https://agihunt.info/en/p/1a1c72a117a265375d93a86d0d7">Why agents keep recommending Resend: Claude Code… · AGI Hunt</a></li>

</ul>
</details>

**Tags**: `#AEO`, `#Agent Experience`, `#开发者工具分发`, `#MCP`, `#间接机会`

---

<a id="item-ai-opportunity-2"></a>
### [AlphaProof Code 形式化验证智能体](https://deepmind.google/blog/introducing-alphaproof-code/) ⭐️ 5.0/10

DeepMind 在官方博客发布了 AlphaProof Code，一个面向形式化验证的智能体，能在代码库上迭代编写 Lean 或 Rocq 证明。据评论者转述，论文中他们把一段人工编写、历史上出过 bug 的代码库做了整体形式化验证，并重新注入部分 bug 来检验能否捕获，但最终没有报告发现新 bug。博客未披露定价、开源协议或可用范围，公开材料也未说明是否对外开放使用。

hackernews · ilreb · Nov 10, 12:11 · [Discussion](https://news.ycombinator.com/item?id=50439193)

**「Why now」** DeepMind announced AlphaProof Code on November 10, 2026, and used it to machine-check selected security properties of Signal&\#x27;s compiled libsignal code in about four weeks with a five-person research team, releasing the specifications and verification artifacts for outside review. The concrete shift is that a multi-LLM agent stack now splits formal verification the way a research team would — humans decide what to prove, agents write and check Lean proofs — which lowers the labor cost of Lean/Rocq work from specialist-months toward weeks. The window is hard to size from public material: no pricing, customer count, or general availability was disclosed, and the Signal result covers selected properties of one codebase rather than arbitrary software.

**「能不能做成产品」** 直接复刻这个智能体做不成：它依赖 DeepMind 的模型与算力，且未开放接口。可做的是围绕它的缺口做小工具，目标用户是已经在用 AI 写 Lean/Rocq 证明的团队和个人。评论里 r0ze-at-hn 指出 AI 写 Lean 时会作弊，至少需要另一个对抗性提示去审查生成的证明——这指向一个 MVP：对 AI 生成的 Lean 证明做独立审计，检查定理是否被弱化、是否有 sorry/axiom 漏洞、是否只证明了窄性质。形态可以是一个 CLI 加 CI 插件，按仓库或按次收费，两三人几周可做出原型。难点在于需要真正的 Lean 专业能力，且客户群目前很小。

**「能不能接单」** 有间接服务需求迹象但很弱：评论者 hedora 提到自己用 Claude 对加密和数据存储格式做形式化验证，thibsrn 在追问这个智能体与普通编码智能体的区别，说明有一批人在实际尝试 AI 加形式化验证。可交付的是为团队做 AI 生成证明的审计流程、搭建 Lean CI 检查、或培训如何写不被 AI 钻空子的定理。目前没有看到招聘或付费询单的直接证据，获客路径不清晰。

**「Market signal」** No pricing, revenue, customer count, or paid-tier data for AlphaProof Code is disclosed in the source item or the available tool results. The nearest commercial evidence is adjacent, not about this product: Anthropic published research \(Oct 22, 2026\) on using Claude to prove security properties at the RISC-V assembly level across 100+ open-source libraries, and a vendor page \(Veriprajna\) sells AI-assisted formal verification and proof automation as a service, citing a &quot;Lean-Agent Protocol&quot; with ~5 microsecond verification checks and converging regulatory timelines. Both are vendor or self-reported claims, not independent evidence of willingness to pay. The community thread contains no pricing or purchasing signals, only technical skepticism about whether zero bugs found reflects narrow theorems.

**「风险」** 最大风险是需求本身不存在：形式化验证的付费客户集中在少数高合规行业，个人开发者难以触达；同时 DeepMind 或模型厂商若把审计能力内置进产品，独立工具的空间会被压缩。评论中关于“零 bug”的质疑也提示，这类工具的可信度本身需要被证明。

**「评论区实战信息」** r0ze-at-hn 给出了最具体的经验：AI 写 Lean 很容易作弊，必须用另一个对抗性提示审查生成的证明，并指出论文虽重新注入 bug 做检验，但没找到新 bug。hedora 质疑“零 bug”结论，怀疑定理写错或只证明了窄性质。Mizza 预期两三年内未验证软件会变得不可接受，这是个人判断而非事实。

<details><summary>References</summary>
<ul>
<li><a href="https://deepmind.google/blog/introducing-alphaproof-code/">Formal Verification of Signal’s Protocol with Gemini</a></li>
<li><a href="https://explainx.ai/blog/google-deepmind-alphaproof-code-signal-protocol-formal-verification-2026">AlphaProof Code: Signal Protocol Verified in 4 Weeks ...</a></li>
<li><a href="https://www.unite.ai/google-deepmind-uses-ai-agents-to-verify-signals-core-machine-code/">Google DeepMind Uses AI Agents to Verify Signal’s Core ...</a></li>
<li><a href="https://www.anthropic.com/research/formal-verification">LLMs are making formal software verification feasible at a ...</a></li>
<li><a href="https://veriprajna.com/services/formal-verification-proof-automation">Formal Verification &amp; Proof Automation for AI | Veriprajna</a></li>

</ul>
</details>

**Tags**: `#形式化验证`, `#Lean/Rocq`, `#AI 编码智能体`, `#生态更新`, `#间接机会`

---

<a id="item-ai-opportunity-3"></a>
### [Anthropic 漏洞发现追踪](https://www.vulncheck.com/blog/anthropic-glasswing-november-update) ⭐️ 5.0/10

VulnCheck 的一篇博客文章追踪了 Anthropic 的 Project Glasswing 及其 Mythos 级模型发现的漏洞，并附有 11 月更新。该文章本身没有提供任何内容，因此细节只能来自评论。一位评论者（pizlonator）称，他们收到了 9 份关于 Fil-C 问题的 Anthropic 报告，全部是真实缺陷，没有误报，报告质量“极佳”，而建议修复的质量“尚可”。另一位评论者（rurcliped）认为该博客具有误导性：Glasswing 的发现通常发生在合作伙伴将 Mythos 级模型用于其自有、往往是专有的软件时，而公开的“账本”只覆盖 Anthropic 针对开源软件协调漏洞披露计划。没有披露任何定价、收入或客户数量。

hackernews · panic · Nov 10, 22:17 · [Discussion](https://news.ycombinator.com/item?id=50447074)

**「Why now」** The timing is set by Project Glasswing, which Anthropic announced on April 7, 2026 with AWS, Apple, Microsoft, Google, NVIDIA, CrowdStrike and others, and which pairs partner-directed use of a Mythos-class model against their own software with an Anthropic coordinated-disclosure program for open source. The November 2026 VulnCheck post and the comment thread are a status check roughly seven months in, not a new capability release. One commenter disputes the framing: Glasswing findings mostly come from partners pointing the model at proprietary code, while the public ledger only covers the open-source disclosure program, so public CVE data understates what is being found. How long this window stays open for an individual developer cannot be judged from the available material.

**「产品角度」** 对个人开发者来说，这看起来不像是一个独立的产品机会。付费方是大型科技公司和安全团队，他们已经在内部修补私有代码库中的问题（enthuseyourcurb），而公开的 CVE 数据被描述为不具代表性。一个较窄的相邻 MVP 可能是为开源维护者提供分诊或修复辅助工具，用于处理 AI 生成的漏洞报告——例如一个接收报告、去重、排序并起草补丁的仪表板——但需求证据仅限于一位维护者的轶事，而且模型供应商可以免费提供类似功能。构建时间无法从现有材料中估计。

**「服务角度」** 没有直接的服务需求迹象。评论者描述的是内部企业安全工作，而不是外包工作。一个可能的服务是帮助小型开源项目分诊和修补 AI 提交的漏洞报告，但材料中没有证据表明有人为此付费。

**「Market signal」** VulnCheck tracked 442 CVEs attributable to Anthropic roughly seven months into Project Glasswing, about 0.5% of all CVEs published this year, with only two flagged as exploited in the wild \(tool-2-1\). Anthropic frames Glasswing around vulnerability disclosure, software update, and open-source supply-chain security processes \(tool-2-2\). No pricing, revenue, customer counts, or paid-tier data for any Glasswing-adjacent tooling is disclosed in the supplied material; the only concrete commercial-adjacent fact is the CVE volume above.

**「风险」** 主要风险是模型供应商免费提供漏洞发现和修复建议，使任何第三方分诊工具变得多余。此外，最有价值的发现位于私有代码库中，永远不会公开，因此基于公开数据的工具只能看到不具代表性的样本。

**「社区讨论」** pizlonator 报告称，9 份 Anthropic 漏洞报告全部是真实缺陷，质量极佳，修复建议尚可（部分被逐字采用，大多数被用作灵感）。enthuseyourcurb 反驳说，公开 CVE 数据集低估了问题，因为严重问题存在于私有代码库中，永远不会获得 CVE 编号。rurcliped 认为该博客将 Glasswing 的有效性与一个仅覆盖开源披露的账本混为一谈。这些是个人观点，不是共识。

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/glasswing">Project Glasswing: Securing critical software for the AI era</a></li>
<li><a href="https://www.anthropic.com/project/glasswing">Project Glasswing \ Anthropic</a></li>
<li><a href="https://tech-insider.org/anthropic-claude-mythos-zero-day-project-glasswing-2026/">Anthropic Claude Mythos Zero-Day Discovery: $100M Glasswing ...</a></li>
<li><a href="https://www.vulncheck.com/blog/anthropic-glasswing-november-update">After 7-months, Glasswing Overwelms Maintainers with... | VulnCheck</a></li>
<li><a href="https://www.anthropic.com/glasswing">Project Glasswing : Securing critical software for the AI era \ Anthropic</a></li>

</ul>
</details>

**Tags**: `#AI安全`, `#漏洞发现`, `#生态信息`, `#企业级市场`, `#变现路径不清晰`

---

<a id="item-ai-opportunity-4"></a>
### [ZONOS3-Mini 开源 TTS 模型](https://www.reddit.com/r/LocalLLaMA/comments/1xtb9gw/zyphrazonos3mini_hugging_face/) ⭐️ 5.0/10

ZONOS3-Mini 是 Zyphra 发布的小型开源文本转语音模型，权重以 Apache 2.0 许可发布，总参数 800M、每 token 约 100M 活跃参数（latent MoE，64 专家、top-2 路由）。官方称可在手机、笔记本和浏览器内实时运行，支持 43 种语言、从音频样本克隆声音，以及按年龄、口音、音色设计角色声音，并可逐词控制情绪、语速和表达。仓库提供 CUDA、Apple Silicon MLX、C++/ggml（CPU/CUDA/Metal/Vulkan）和 WebGPU 浏览器四种运行时，共用一套 HTTP API，另可通过 Zyphra Cloud 托管调用。以上均为厂商自述，第三方评测与独立基准未在材料中出现。

reddit · r/LocalLLaMA · /u/pmttyji · Nov 11, 07:09

**「Why now」** ZONOS3-Mini is now available as Apache 2.0 weights with native runtimes \(CUDA, MLX, C++/ggml, and an in-browser WebGPU build\) plus a hosted option on Zyphra Cloud, so a solo developer can ship a voice feature without training a model or renting GPU inference. Zyphra says it trained the model on 112 NVIDIA H100s in 2.5 days, which suggests the recipe is cheap to reproduce but does not by itself prove a durable moat. The window is hard to judge from the supplied material: the release is days old and no adoption, pricing, or demand data is disclosed.

**「能不能做成产品」** 可以做，但机会不在模型本身，而在它够小、能本地跑这一点上。目标用户是隐私敏感或需要离线运行的场景：游戏独立开发者的角色配音、播客/有声书的批量旁白、企业内部培训音频、以及不想把声音数据传给云端的团队。MVP 形态是一个桌面或浏览器端的“脚本转配音”工具：导入带说话人标记的文本，选预设声音或上传 10–60 秒样本克隆，逐句调情绪和语速，导出 44.1 kHz 音频；底层直接调用官方运行时，不需要自己训练模型。收费可以走一次性买断（本地工具）或按生成时长订阅（若你代管算力）。两三人小团队大约 4–8 周能做出可用版本，主要工作量在编辑器交互和批量处理，不在模型。做不成的部分是通用 TTS API 平台：Zyphra Cloud 已经提供托管版本，正面拼价格和稳定性没有优势。

**「能不能接单」** 有服务空间，但需求证据在材料里没有出现，以下属于推测。可能买单的是中小游戏工作室、做本地化配音的内容团队、以及有数据合规要求的企业——他们需要的是“部署 + 集成 + 调音”，而不是模型文件。交付物包括：在客户自有 GPU 或 Mac 上部署运行时、把 TTS 接进现有内容流水线（如字幕/脚本系统）、为特定角色调出稳定音色、以及给团队做使用培训。这类需求通常来自开发者社群的部署提问和游戏/播客社群的配音成本抱怨，但本条材料未提供任何此类线索，接单前需要自己去相关论坛和招聘信息里验证。

**「Market signal」** The source item contains no pricing, revenue, customer counts, or paid-usage evidence for ZONOS3-Mini; it only states that a hosted version exists at Zyphra Cloud, without disclosing its price. External coverage confirms the release and its 100M active-parameter, on-device cloning capability but adds no commercial data. The only adjacent pricing signal found is a free consumer TTS site advertising 300+ voices across 70+ languages, which suggests the low end of generic TTS is already free and hard to charge for. Public materials do not disclose specific commercial data for this model.

**「风险」** 声音克隆是主要风险点：未经授权克隆真人声音在多国涉及肖像权/人格权与平台政策，做面向公众的产品需要加同意验证和滥用防护。另外 TTS 赛道开源模型密集，同类小模型随时可能以更宽松的条件出现，单纯“包一层界面”的差异化很薄。

<details><summary>References</summary>
<ul>
<li><a href="https://www.marktechpost.com/2026/11/10/zyphra-zonos3-mini-open-source-tts/">Zyphra Releases ZONOS 3 - Mini : Open-Source TTS... - MarkTechPost</a></li>
<li><a href="https://huggingface.co/Zyphra/ZONOS3-Mini">Zyphra / ZONOS 3 - Mini · Hugging Face</a></li>
<li><a href="https://www.zyphra.com/our-work/zonos3-mini">ZONOS 3 - Mini | Zyphra</a></li>
<li><a href="https://www.marktechpost.com/2026/11/10/zyphra-zonos3-mini-open-source-tts/">Zyphra Releases ZONOS3-Mini: Open - Source TTS ... - MarkTechPost</a></li>
<li><a href="https://voicertool.com/">Free Text to Speech Online – 300+ AI Voices , 70+... | Voicertool</a></li>

</ul>
</details>

**Tags**: `#开源TTS`, `#语音克隆`, `#本地推理`, `#生态工具更新`, `#合规风险`

---

<a id="item-ai-opportunity-5"></a>
### [Qwen4-Max 预览版上线 Token Plan](https://mp.weixin.qq.com/s/J_zbVHa2R3mmY5KD4v3-bw) ⭐️ 5.0/10

Alibaba has teased Qwen4, describing deeper knowledge understanding, more three-dimensional world perception, and further advances in Coding and Agentic capabilities. The Qwen4-Max preview is the first model released on Alibaba&\#x27;s Token Plan, with a limited-time discount of as low as 10% of list price \(1折\). Qoder, the Qwen app, and QwenStudio have already integrated the new model. This is a vendor teaser plus promotional pricing announcement; no benchmark numbers, parameter counts, license terms, or independent performance evidence were disclosed in the source.

telegram · zaihuapd · Nov 11, 02:35

**「Why now」** The timing hook is a promotional price, not a capability jump: the Qwen4-Max preview launched on Alibaba&\#x27;s Token Plan with a limited-time discount of up to 90% off, and Qoder, the Qwen app and QwenStudio were wired in at the same time. That makes this a short window for cheap evaluation and prototyping on the new model, not a durable cost advantage — the discount is explicitly time-limited and no end date is disclosed. One third-party forum post claims a Qwen4-Max preview had already appeared on a non-official platform and that the Token Plan 3.8 Preview was about to be retired, but that thread was reportedly deleted and should be treated as unverified.

**「能不能做成产品」** Not directly as a standalone product — the item itself is a model release and discount, not a product gap. The realistic angle is indirect: if the preview&\#x27;s Coding/Agentic claims hold up, a solo developer or two-to-three-person team could build a narrow coding or agent workflow tool on top of the Token Plan API, where the 1折 promotional pricing temporarily lowers inference cost. MVP would be a thin wrapper around one concrete job \(e.g., repo-level refactor agent or a code-review bot for a specific stack\), billed as subscription or per-seat. Timeline is roughly 2-6 weeks for an MVP, but viability depends on post-promotion pricing and on the preview&\#x27;s actual capability, neither of which is disclosed. Treat the capability claims as vendor marketing until independently tested.

**「能不能接单」** Possible but unproven. The plausible buyers are small teams wanting Qwen4-Max integrated into existing apps or wanting migration help off other model APIs, with deliverables like API integration, prompt/workflow tuning, or a short internal training session. However, the source shows no service demand signals — no job postings, community questions, or client requests — so this is inference from a generic model-release pattern, not evidence. No service demand is visible in the supplied material.

**「Money side: promotional pricing, no disclosed revenue」** The only concrete commercial data comes from Alibaba&\#x27;s own promotional pages: the Qwen4-Max preview debuts on the Token Plan subscription with new-customer packages from 5折, per-call usage at 2折, and a limited-time preview experience at 2折, plus individual-plan quota raised 78% and 20+ flagship models bundled \(tool-2-1, tool-2-2\). Alibaba&\#x27;s developer article also lists Qwen Office at 29.9 yuan for the first month and Qoder at 19.9 yuan \(tool-2-1\). These are vendor-stated discounts, not independent evidence. No paid customer counts, revenue figures, or third-party pricing comparisons are disclosed in the source or tool results, so the actual willingness-to-pay on the buyer side cannot be assessed.

**「风险」** The 1折 pricing is explicitly limited-time, so any product built on the cost advantage faces a margin reset when the promotion ends; the post-promotion price is not disclosed. The model is a preview, so API behavior, availability, and capability may change before general release, and Alibaba&\#x27;s own products \(Qoder, Qwen app, QwenStudio\) already cover some adjacent coding/agent use cases.

<details><summary>References</summary>
<ul>
<li><a href="https://linux.do/t/topic/3153289">Qwen 4 - Max 预 览 版 已 上 线 阿 里 Token Plan - 开发调优 - LINUX DO</a></li>
<li><a href="https://developer.aliyun.com/article/1781975">Qwen4-Max预览版正式登陆阿里云百炼Token Plan！2026年双十一5折优惠...</a></li>
<li><a href="https://www.aliyun.com/benefit/scene/ai-discount">新一代基座大模型 Qwen4-Max 预览版首发 - 阿里云</a></li>

</ul>
</details>

**Tags**: `#模型发布`, `#API定价`, `#生态信息`, `#间接机会`, `#证据不足`

---
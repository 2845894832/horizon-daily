---
layout: default
title: "Horizon Summary: 2026-11-21 (EN)"
date: 2026-11-21
lang: en
---

> From 32 items, 4 important content pieces were selected

---

**AI Opportunity Radar**
1. [形式化验证对抗AI代码垃圾](#item-ai-opportunity-1) ⭐️ 5.0/10
2. [ChatGPT Space 向 Plus 开放](#item-ai-opportunity-2) ⭐️ 5.0/10
3. [微软USB4多机合跑大模型](#item-ai-opportunity-3) ⭐️ 5.0/10
4. [Antigravity 重置 Gemini 额度](#item-ai-opportunity-4) ⭐️ 5.0/10

---

## AI Opportunity Radar

<a id="item-ai-opportunity-1"></a>
### [形式化验证对抗AI代码垃圾](https://latent.space/p/formal-verification/) ⭐️ 5.0/10

这是一篇 Latent Space 的行业综述，讨论用形式化验证（数学证明与逻辑）来检查 AI 生成代码的正确性，以对抗所谓 &quot;slop&quot;（低质模型输出）。文章点名四家玩家：Harmonic（Aristotle 自动定理证明器）、Theorem（与 Anthropic 合作发布 &quot;LLM-scaled formal verification&quot; 博文）、Axiom Math（AxiomProver 与 AXLE 工具包）、以及新入场的 &amp;Truth（基于开源 Lean 构建 &quot;verification machine&quot;，首个工具 &amp;Atlas 面向 C 代码）。文章引用了 &amp;Truth 联合创始人、斯坦福教授、cvc5 共同作者 Clark Barrett 的访谈，属于方向性情报，未披露任何定价、收入或客户数。

rss · Latent Space · Nov 20, 21:18

**「Why now」** The window is being opened by two measurable shifts, not by a general trend. First, token cost for verification is falling: Anthropic reported that Opus 5.5 hit a 50% solve rate on 36 small verification tasks using about 40% fewer tokens than Opus 5, and expects further gains as models are trained on long verification tasks. Second, proof throughput is improving fast enough to make large codebases tractable — Theorem publishes a proof-efficiency eval measuring KB of machine code verified per hour by model release date, and Axiom Math&\#x27;s agents formally verified the Stacks Project in early November 2026. The article frames 2026 as the year &quot;slop&quot; became a daily engineering concern, which is the demand-side trigger. How long this window stays open cannot be judged from the supplied material; the article gives no pricing, customer counts, or adoption data.

**「能不能做成产品」** 直接复制核心能力做不成：求解器（cvc5）、证明器（Lean）与大规模训练反馈依赖深厚数学积累和算力，个人或两三人团队无法在短期内做出同等水平的验证引擎。可考虑的窄切口是围绕现有开源工具做外围产品，例如面向使用 Lean 或 SMT 的团队的规格（spec）编写辅助、证明失败诊断、CI 集成插件，目标用户是已经在做形式化验证的工程团队，MVP 是一个把 agent 输出接到 Lean 检查并给出可读失败原因的小工具，按订阅或按次收费。但文章没有给出这类外围需求存在的证据，能否成立需自行验证；个人团队做出可用版本的时间无法从现有材料判断。

**「能不能接单」** 文章提到 &amp;Truth 关注用形式化验证检查全球 C 代码的内存安全，Theorem 主打安全场景，说明企业级安全验证是这些公司在推的方向，但文中没有任何企业采购、招标或招聘信号，也没有社群提问或评论区需求。因此目前没有可确认的服务需求迹象；若要接单，只能推测面向已有形式化验证实践的企业做部署、集成或培训，交付物与客户来源均缺乏证据支撑。

**「Market signal」** The article discloses no pricing, revenue, customer counts, or funding for Harmonic, Theorem, Axiom Math, or &amp;Truth — public material does not disclose specific commercial data. The only concrete commercial-adjacent fact is technical adoption, not payment: cvc5, co-created by &amp;Truth co-founder Clark Barrett, is &quot;called billions of times a day in production pipelines at Amazon&quot; and is used in Amazon&\#x27;s Kiro for specification analysis and test generation, per Barrett&\#x27;s statement in the article. Anthropic&\#x27;s own research post \(cited via Theorem collaboration\) reports Opus 5.5 reaching a 50% solve rate on 36 small verification tasks with ~40% fewer tokens than Opus 5, which points to falling verification cost but is a capability metric, not a market one.

**「风险」** 最直接的风险是这几家资金与人才密集的公司在把验证能力做成端到端产品（如 &amp;Truth 宣称 agent 接入后&quot;代码第一次就能跑&quot;），一旦成熟会覆盖外围工具的空间；另外文章指出形式化验证目前 token 开销大，成本结构变化会直接影响任何按量收费的外围产品。

<details><summary>References</summary>
<ul>
<li><a href="https://latent.space/p/formal-verification/">The War Against Slop and an Emerging Weapon to Fight it ...</a></li>
<li><a href="https://techcrunch.com/2026/11/05/axiom-math-wants-to-keep-ai-slop-out-of-mathematics/">Axiom Math wants to keep AI slop out of mathematics</a></li>
<li><a href="https://wal.sh/research/axiomprover-2026/">AxiomProver: AI-Generated Mathematical Proofs (2026)</a></li>
<li><a href="https://explainx.ai/blog/anthropic-claude-formal-verification-123-libraries-rocq-risc-v-proofs-2026">Claude Formal Verification : 123 Libraries Proven... | explainx.ai</a></li>
<li><a href="https://www-cdn.anthropic.com/files/4zrzovbb/website/6867eadf760258fa8b42a504600cd3c036d16358.pdf">Appendix: LLMs are making formal software verification feasible at...</a></li>
<li><a href="https://theprimary.com/ai-tech/2026-10-23/claude-oss-fuzz-verification">Software verification reaches open source libraries as language...</a></li>

</ul>
</details>

**Tags**: `#形式化验证`, `#AI代码质量`, `#Lean定理证明`, `#开发者工具`, `#生态情报`

---

<a id="item-ai-opportunity-2"></a>
### [ChatGPT Space 向 Plus 开放](https://x.com/ChatGPT/status/2123850912867471807) ⭐️ 5.0/10

OpenAI 官方账号宣布，ChatGPT 的 Space 功能向 Plus 用户开放。Space 位于侧边栏，集中存放页面、幻灯片、图片、文件和上传内容，支持多人协作编辑交互式页面、幻灯片和网站，并可在手机端编辑。页面与幻灯片可设为从已连接工具自动更新。官方称整体更流畅稳定，但未披露具体版本号、价格变动或 Plus 之外的开放范围。

telegram · zaihuapd · Nov 21, 02:30

**「Why now」** The change is a plan-tier expansion: Space was previously limited to Pro, Business and Enterprise plans, and is now opening to Plus subscribers, which widens the pool of people who can create and co-edit pages and slides. A second, narrower change is that Slides is still rolling out to eligible accounts with Space access, and mobile support is read/read-share only rather than full editing, so the capability is not uniformly available yet. The window for template, workflow or teaching products around Space depends on how fast Slides and mobile editing reach the broader Plus base; the supplied material gives no timeline, so the window length cannot be judged from existing evidence.

**「能不能做成产品」** 直接做协作建站工具不现实，这块由 OpenAI 自己覆盖。可考虑的是围绕 Space 的周边：面向非技术用户的 Space 模板库（周报、项目看板、客户提案幻灯片）、把 Space 页面接到外部数据源的轻量连接器、以及教小团队怎么用 Space 替代部分文档工具的课程。目标用户是已经在付 Plus 订阅、想少买一个工具的独立工作者和小团队。MVP 可以是一组可复制的模板加一份使用说明，按订阅或一次性买断收费，两三人一两周能出第一版。风险在于模板类产品壁垒低，且 Space 的接口开放程度公开材料未披露，能否做自动更新类集成无法确认。

**「能不能接单」** 有间接服务空间但需求未验证：可以面向中小企业做 Space 落地培训、把现有文档/幻灯片迁移进 Space 的整理服务、或帮团队设计协作模板与权限规范。交付物是培训场次、迁移后的空间结构和模板包。目前没有看到招聘岗位、社群提问或评论区需求作为证据，这类需求是否真实存在无法从现有材料判断，建议先小范围试探再投入。

**「Market signal」** No pricing, revenue, paid-customer counts, or hiring tied to ChatGPT Space appear in the source item or the supplied tool results; the official feature page \(tool-2-1\) describes the product but discloses no commercial data. The only adjacent commercial context is OpenAI&\#x27;s broader integrations surface — plugins connecting ChatGPT to Slack, SharePoint, Airtable and Google Drive \(tool-2-3\) — which suggests a partner/integration ecosystem exists, but nothing indicates money flows to third parties building on Space specifically. Whether anyone pays for Space-adjacent templates, workflows, or training is unverified.

**「风险」** Space 是 OpenAI 自家功能，能力边界、免费额度与接口开放策略都由其单方面调整，围绕它做的模板或集成随时可能被官方内置功能覆盖；Plus 用户可用的功能也可能进一步下放到免费层，压缩付费周边空间。

<details><summary>References</summary>
<ul>
<li><a href="https://www.engadget.com/2323016/openai-brings-its-collaborative-space-hubs-to-plus-users/">OpenAI Brings Its Collaborative Space Hubs To Plus Users</a></li>
<li><a href="https://help.openai.com/en/articles/20001549-getting-started-with-space-in-chatgpt">Getting started with Space in ChatGPT | OpenAI Help Center</a></li>
<li><a href="https://chatgpt.com/features/space/">ChatGPT Space | Create and collaborate with AI</a></li>
<li><a href="https://chatgpt.com/features/plugins/">Plugins in ChatGPT | Business integrations and workflows</a></li>

</ul>
</details>

**Tags**: `#生态信息`, `#产品更新`, `#OpenAI`, `#协作工具`, `#变现路径不清晰`

---

<a id="item-ai-opportunity-3"></a>
### [微软USB4多机合跑大模型](https://videocardz.com/newz/microsoft-brings-rdma-over-usb4-to-windows-allowing-multiple-pcs-to-run-one-local-ai-model) ⭐️ 5.0/10

Microsoft released a developer preview of RDMA over USB4 on Windows, letting multiple PCs share memory and GPU compute over ordinary USB4 cables to run a single local large model, without dedicated NICs or switches. The demo ran Qwen3-235B-A22B at 4-bit quantization across three AMD Ryzen AI Max+ 395 machines at about 18.5 tokens/s, and the feature will ship through Windows Insider. It is a platform capability update in preview, not a product with disclosed pricing or customers.

telegram · zaihuapd · Nov 21, 06:13

**「Why now」** The enabling change is that Microsoft has shipped an RDMA over USB4 developer preview for Windows 11, letting two or more PCs link directly over ordinary USB4 cables into one compute cluster without buying dedicated network adapters or switches \(tool-1-2, tool-1-3\). RDMA lets Windows machines read and write each other&\#x27;s memory directly, bypassing the CPU \(tool-1-1\), which is what makes pooling memory and GPU across consumer machines practical. The window is narrow and unproven: this is a developer preview delivered through Windows Insider, and the source gives no date for general availability, so how long the early-mover window lasts cannot be judged from the available material.

**「能不能做成产品」** The realistic product is not the transport layer but the setup and operations layer on top of it: a tool that detects compatible machines, configures the RDMA cluster, splits and quantizes models across nodes, and monitors throughput. Target users are small studios, research groups, and privacy-sensitive teams that already own several high-end PCs and want to run a large local model without buying server hardware. An MVP could be a guided installer plus a model-sharding config generator, sold as a one-time license or a low-cost subscription. A two-to-three person team could plausibly build this in a few months, but only after the feature leaves Insider preview. The hard blockers are dependence on an unreleased Windows feature, narrow hardware support \(the demo used Ryzen AI Max+ 395\), and the fact that most target users would need multiple expensive machines, which caps the addressable market. Building the underlying RDMA capability itself is not feasible for an individual developer.

**「能不能接单」** There is a plausible but unverified service angle: deployment and tuning engagements for teams that want a private multi-PC inference setup, delivered as on-site or remote configuration, benchmarking, and handover documentation. Demand signals are not available in the supplied material, and no job postings, community requests, or paying clients are cited, so treat this as a hypothesis rather than an observed market. Until the feature is generally available, paid service demand is unlikely to be strong.

**「Money side」** No pricing, revenue, paid-customer counts, or funding figures are disclosed for RDMA over USB4; Microsoft presents it as a free Windows developer preview pushed through Windows Insider. The only adjacent commercial signal in the supplied material is hardware: the demo relies on three AMD Ryzen AI Max+ 395 mini-PCs, each with up to 128 GB unified memory \(up to 96 GB allocatable to the iGPU on Windows\), so the spend sits with buyers of that hardware rather than with any software layer. Whether anyone pays for multi-PC local inference setup or tuning is unverified — no job postings, procurement, or paid-service evidence appears in the material.

**「风险」** The main risk is that Microsoft ships this as a built-in, well-documented Windows feature with its own setup tooling, erasing the value of a third-party configuration layer. A secondary risk is that hardware support stays limited to a few expensive machines, keeping the paying audience too small to sustain a product.

<details><summary>References</summary>
<ul>
<li><a href="https://habr.com/ru/articles/1110636/">Microsoft представила решение на базе USB 4 и RDMA для... / Хабр</a></li>
<li><a href="https://www.goha.ru/microsoft-dobavila-v-windows-11-tehnologiyu-rdma-po-usb4-dlya-obedineniya-neskolkih-pk-v-edinyj-lokalnyj-ii-klaster-lWoPRN">Microsoft добавила в Windows 11 технологию RDMA по USB 4 для...</a></li>
<li><a href="https://gagadget.com/ru/artificial-intelligence/735249-resursyi-neskolkih-pk-dlya-zapuska-tyazhelogo-ii-nauchilas-obedinyat-microsoft-cherez-usb4/">Microsoft реализовала RDMA через USB 4 для ИИ-кластеров</a></li>
<li><a href="https://insidepc.tech/hardware/for-ai/ai-builds/ryzen-ai-max-395-local-llm">Локальный LLM на Ryzen AI Max+ 395 : что потянет</a></li>
<li><a href="https://www.goha.ru/microsoft-dobavila-v-windows-11-tehnologiyu-rdma-po-usb4-dlya-obedineniya-neskolkih-pk-v-edinyj-lokalnyj-ii-klaster-lWoPRN">Microsoft добавила в Windows 11 технологию RDMA по USB 4 для...</a></li>

</ul>
</details>

**Tags**: `#本地大模型`, `#多机推理`, `#Windows生态`, `#开发者预览`, `#间接机会`

---

<a id="item-ai-opportunity-4"></a>
### [Antigravity 重置 Gemini 额度](https://x.com/_mohansolo/status/2124070033534161407) ⭐️ 5.0/10

Google Antigravity 团队负责人 Varun Mohan 在 X 上表示，已为 Antigravity 所有用户重置 Gemini 额度，并称缓存方面的改进让额度内可完成的工作量提升了 22%，同时鼓励用户周末用 Neon 开发。这是官方人员在社交平台上的表态，属于工具生态更新，未披露具体额度数值、重置频率或 Neon 合作细节。

telegram · zaihuapd · Nov 21, 14:29

**「Why now」** The immediate trigger is a quota reset: Varun Mohan announced on Nov 18, 2026 that Antigravity was resetting quota for everyone across all models to mark the product&\#x27;s first anniversary, and users reported their usage meters reset within hours \(tool-1-2\). The same announcement attributes a 22% increase in work-per-quota to a larger cache pool \(tool-1-3\), which lowers the effective cost of running AI coding sessions inside the quota. For a solo developer, the window is the period before this free headroom is consumed or the promotion ends; the source gives no end date, so the exact window cannot be judged from available material.

**「产品角度」** 这条信息本身不构成可售卖的产品机会：它只是降低了使用 Antigravity 和 Gemini 的个人开发者的编码成本，没有指向具体付费人群或痛点。若要从中推导产品，唯一可行的方向是围绕 Antigravity + Neon 组合做辅助工具（例如额度用量追踪、Neon 分支管理的小插件），但目标用户规模、付费意愿均无证据支撑，且功能极易被平台自带能力覆盖，不建议作为独立产品投入。

**「服务角度」** 没有服务需求迹象。材料中不存在客户询单、招聘岗位或社群提问，无法判断哪类客户会为 Antigravity 或 Neon 的部署、集成、培训付费。若强行接单，只能做通用的 AI 编码工具上手培训，与这条更新无直接因果关系。

**「Money side」** No pricing, revenue, paid-customer counts, or hiring tied to this quota reset were disclosed in the source or the search results. The only commercial context available is Google&\#x27;s own I/O 2026 framing of Antigravity as a unified platform for builders \(tool-2-2\) and a Google Cloud post citing third-party estimates that coding-agent adoption reached roughly 22–29% of over 128,000 active GitHub repositories by early 2026 \(tool-2-3\) — neither is evidence of anyone paying for this specific change. The 22% workload improvement is an official claim from the Antigravity lead, not independently verified.

**「风险」** 额度重置和 22% 效率提升均为官方人员单方面宣称，无独立验证；额度政策随时可能调整或收紧，依赖该额度构建的任何工具或服务都会随之失效。

<details><summary>References</summary>
<ul>
<li><a href="https://x.com/AGTPinsights/status/2122884033575092594">AGTP on X: &quot;Google Antigravity just turned 1 and reset usage ...</a></li>
<li><a href="https://x.com/guilleflorvs/status/2124114464853094440">Guillermo Flor on X: &quot;JUST IN: Google DeepMind just reset ...</a></li>
<li><a href="https://antigravity.google/blog/google-io-2026">Google Antigravity @ I/O 2026 | Google Antigravity Blog</a></li>
<li><a href="https://cloud.google.com/blog/topics/developers-practitioners/how-to-build-durable-agentic-systems-with-google-antigravity-from-instructions-to-loops">How to Build Durable Agentic Systems with Google Antigravity ...</a></li>

</ul>
</details>

**Tags**: `#AI编码工具`, `#生态更新`, `#成本降低`, `#间接机会`, `#未披露付费数据`

---
---
layout: default
title: "Horizon Summary: 2026-11-20 (EN)"
date: 2026-11-20
lang: en
---

> From 47 items, 6 important content pieces were selected

---

**AI Opportunity Radar**
1. [Inkling 2 Mini 本地开源模型](#item-ai-opportunity-1) ⭐️ 5.0/10
2. [New-Domain Startup Discovery Site](#item-ai-opportunity-2) ⭐️ 5.0/10
3. [形式化验证赛道观察](#item-ai-opportunity-3) ⭐️ 5.0/10
4. [Gemini 在 Mac 上代用户操作](#item-ai-opportunity-4) ⭐️ 5.0/10
5. [豆包工作下调模型倍率](#item-ai-opportunity-5) ⭐️ 5.0/10
6. [OpenAI 后台模式长任务折扣](#item-ai-opportunity-6) ⭐️ 5.0/10

---

## AI Opportunity Radar

<a id="item-ai-opportunity-1"></a>
### [Inkling 2 Mini 本地开源模型](https://thinkingmachines.ai/news/inkling-2-mini/) ⭐️ 5.0/10

Thinking Machines 发布了 Inkling 2 Mini，一个面向本地运行的开源模型，据称在基准测试上与 Qwen3.8-27B 相当，并采用 looped transformer 架构。社区指出已有 unsloth 提供的 GGUF 版本，可在 Ollama/llama.cpp 上运行。厂商在 Reddit 表示训练全程使用 nvfp4，模型尺寸参考了本地用户社区的常见需求。基准成绩目前只有厂商与社区转述，尚无独立复现，开源协议与具体参数规模在现有材料中未披露。

hackernews · jasondavies · Nov 20, 20:12 · [Discussion](https://news.ycombinator.com/item?id=50581260)

**「Why now」** Inkling 2 Mini was released on November 20, 2026 as an open-weights model with 26.4B total parameters and roughly a 20GB memory footprint, small enough to run on consumer laptops, and a GGUF build for Ollama/llama.cpp already exists. It follows Inkling 2 Small, released November 5, 2026, so this is the second release in the same generation within about two weeks. The window is set by the model being downloadable now rather than by any verified change in buyer demand; the source item discloses no pricing, paid users, or revenue, so how long the opportunity stays open cannot be judged from the available material.

**「能不能做成产品」** 模型本身不是产品，但可以围绕它做本地多智能体推理工具：目标用户是拥有单卡或双卡消费级 GPU、希望数据不出本机就跑多 agent 流程的开发者与小团队。社区评论认为 MoE 结构让多个 agent 各自持有 KV cache 塞进显存成为可能，这是可切入的具体痛点。MVP 可以是一个本地编排器：一键拉起 Ollama/llama.cpp、管理多 agent 的上下文与显存分配、提供任务模板与日志。收费方式适合一次性买断或低价订阅，两三人团队数周可做出可用版本。风险在于这只是薄封装，Ollama 与各家推理框架本身在快速补齐同类功能。

**「能不能接单」** 有服务需求的迹象但很弱：评论区讨论集中在跑分、GGUF 可用性和多 agent 显存占用，属于技术爱好者自建场景，没有出现企业采购、招聘或付费咨询的信号。可设想的交付是帮团队在本地部署该模型并调优推理配置，但现有材料无法证明有人为此付钱。

**「Money side」** No pricing, revenue, paid-customer counts, or funding figures for Inkling 2 Mini appear in the source item or the supplied search results; the model is presented as an open local release, so there is no disclosed commercial data to point to. The only adjacent commercial signal is third-party comparison pages \(llm-stats.com, artificialanalysis.ai\) that list benchmark and pricing comparisons against Qwen3.8-27B, but these cover other Inkling variants \(Inkling, Inkling-Small, Inkling 2 Small\) and do not establish Inkling 2 Mini pricing or paying users. Treat the money side as undisclosed rather than proven.

**「风险」** 基准成绩未经独立复现，若实际表现不及 Qwen3.8-27B，围绕它做的工具价值会迅速缩水；同时 Ollama、llama.cpp 等上游框架持续内建多模型管理与多 agent 支持，薄封装产品容易被免费功能覆盖。

**「评论区实战信息」** 有人贴出 unsloth 的 GGUF 仓库地址，确认可在 Ollama/llama.cpp 上跑，这是最实用的一条。另有评论认为它是首个能在本地硬件上可靠跑多 agent 推理框架的模型，理由是 MoE 下多个 agent 的 KV cache 可同时放进显存；这属于个人判断而非实测结论。也有评论提到 SenseNova 近期发布了同类 looping 模型，说明这一方向已有竞争。

<details><summary>References</summary>
<ul>
<li><a href="https://thinkingmachines.ai/news/inkling-2-mini/">Introducing Inkling 2 Mini - Thinking Machines Lab</a></li>
<li><a href="https://thinkingmachines.ai/news/inkling-2-small/">Introducing Inkling 2 Small - Thinking Machines Lab</a></li>
<li><a href="https://www.unite.ai/thinking-machines-lab-releases-inkling-2-mini-for-local-devices/">Thinking Machines Lab Releases Inkling 2 Mini for Local Devices</a></li>
<li><a href="https://llm-stats.com/models/compare/inkling-vs-qwen3.8-27b">Inkling vs Qwen3.8-27B: Benchmarks, Pricing &amp; Which Is Better ...</a></li>
<li><a href="https://llm-stats.com/models/compare/inkling-small-vs-qwen3.8-27b">Inkling-Small vs Qwen3.8-27B: Benchmarks, Pricing &amp; Which Is ...</a></li>
<li><a href="https://artificialanalysis.ai/models/comparisons/inkling-2-small-vs-qwen3-8-27b">Inkling 2 Small vs Qwen3.8 27B: Release Comparison</a></li>

</ul>
</details>

**Tags**: `#local-llm`, `#open-source-model`, `#inference-infrastructure`, `#indirect-opportunity`, `#unverified-benchmarks`

---

<a id="item-ai-opportunity-2"></a>
### [New-Domain Startup Discovery Site](https://startups.novumsignals.com/) ⭐️ 5.0/10

A discovery site that surfaces startup projects by mining newly registered domains and aggregates Hacker News &quot;What are you working on?&quot; answers. It is a directory/research tool rather than a product with disclosed pricing, revenue, or user numbers; the submission itself provides no source content, so its exact feature set and data sources beyond the description are not verifiable. A commenter \(EagleEdge\) links a separate, similar effort that compiled 23,935 answers from 14,897 people at stillworkingonit.vercel.app, indicating this is a small genre of hobby-scale aggregation projects.

hackernews · walterschnitzel · Nov 20, 09:54 · [Discussion](https://news.ycombinator.com/item?id=50572448)

**「Why now」** No specific timing trigger is evidenced in the supplied material. The item is a Hacker News submission with no disclosed launch date, funding, or platform change behind it, so the window cannot be judged from available evidence.

**「Product angle」** The realistic product is a research/competitive-intelligence tool for indie developers and small funds: a searchable feed of newly registered domains plus HN &quot;what are you working on&quot; posts, filterable by keyword, category, and recency. MVP is a scraper \(domain registration feeds such as newly-registered-domain lists, plus HN Algolia API\) and a simple searchable web UI; a solo developer could ship a rough version in days to a couple of weeks. Monetization is the weak point: a subscription \($5-15/month\) for saved searches and alerts is plausible but unproven, and the same data is largely free. The main barrier is not technical but differentiation and willingness to pay.

**「Service angle」** No service demand is evidenced. The comments are users browsing for ideas, not buyers asking for deployment, integration, or custom research. A possible adjacent service is paid market-scan reports for indie founders or small VCs, but nothing in the supplied material shows anyone requesting or paying for that.

**「Market signal」** Public material discloses no pricing, revenue, customer count, or funding for this site. The only concrete figure in the discussion is a commenter&\#x27;s own separate project claiming 23,935 answers from 14,897 people, which is a self-reported count, not independent evidence of commercial traction.

**「Risk」** The core data \(new domain lists, HN posts\) is freely available, so the tool is easy to clone and hard to defend; HN API or scraping access changes could also break the pipeline. Commenters note that most listed landing pages fail to state what they solve, which limits how useful the directory is as a buying signal.

**「Community discussion」** Commenters are skeptical of the output quality: xpct notes almost none of the listed landing pages say what they solve, and hirako2000 says browsing shows nothing obviously useful. MontgomeryPy observes a hardware-to-software ratio of only 94 out of 3,222 in the U.S., which is an observation about the dataset, not a validated market signal.

**Tags**: `#生态信息`, `#选题调研`, `#竞品发现`, `#数据抓取`, `#间接机会`

---

<a id="item-ai-opportunity-3"></a>
### [形式化验证赛道观察](https://latent.space/p/formal-verification/) ⭐️ 5.0/10

Latent Space 的一篇行业综述，梳理了用形式化验证对抗 AI 生成低质代码（&quot;slop&quot;）的几家创业公司：Harmonic（Aristotle 自动定理证明器）、Theorem（与 Anthropic 合作，主打安全验证）、Axiom Math（AxiomProver 生成 Lean 证明，另有 AXLE 工具包）、以及新入场的 &amp;Truth（基于 Lean 构建&quot;验证机器&quot;，首个工具 &amp;Atlas 面向 C 代码）。文章核心论点是开发者将从 vibe-coding 转向 &quot;veri-coding&quot;，即把验证层嵌入工作流，人的时间更多花在写规格和审规格上。这是趋势综述，不是产品发布，文中未披露任何定价、付费客户或收入数据。

rss · Latent Space · Nov 20, 21:18

**「Why now」** The timing case rests on cost and capability shifts rather than new demand: Anthropic reports that on 36 small verification tasks, Opus 5.5 reached a 50% solve rate using about 40% fewer tokens than Opus 5, and expects further gains as models are trained on long verification tasks. In parallel, Axiom Math&\#x27;s agents have formally verified the Stacks Project, and Anthropic has formalized Fermat&\#x27;s Last Theorem — evidence that LLM-driven proof work now scales to large codebases and libraries. The article itself gives no dates, pricing, or adoption numbers, so how long this window stays open for a small builder cannot be judged from the supplied material.

**「能不能做成产品」** 直接做竞品做不成：这几家公司的核心资产是顶尖形式化数学人才（&amp;Truth 联合创始人是 cvc5 共同作者、斯坦福教授 Clark Barrett）、大规模模型训练和算力，个人开发者无法复制。间接切入有两条窄路，但文中都只是暗示、没有验证过的需求：一是面向已采用 Lean 的团队的规格编写与验证工作流辅助工具（例如把自然语言需求转成可检查的 spec 草稿、管理证明任务队列），MVP 可以是一个薄封装在 Lean/cvc5 之上的 CLI 或编辑器插件，按订阅或按量收费；二是 Lean 相关的教学与集成服务。两条路都要求你自己先具备 Lean 或 SMT 的实操能力，否则做出来只是套壳。以两三人团队计，工具型 MVP 大概需要数月，且要先找到真实用户验证，文中没有这类证据。

**「能不能接单」** 文中没有出现任何企业采购、招聘或社群求助的信号，因此无法确认存在可接的服务需求。理论上可能买单的是有内存安全或合规压力的团队（&amp;Truth 明确把 C 代码内存安全列为重点用例，Theorem 主打&quot;对抗方规模化时唯一守得住的防御&quot;），交付物会是验证流程搭建、spec 编写、Lean 集成培训。但这些是从厂商宣传推出来的假设，不是观察到的需求；在拿到具体客户线索前不建议把它当作变现路径。

**「Where the money is」** The source article discloses no pricing, revenue, customer counts, or funding figures for Harmonic, Theorem, Axiom Math, or &amp;Truth — it is a landscape overview, not a commercial report. The only concrete commercial-adjacent facts are technical: cvc5 \(co-created by &amp;Truth&\#x27;s Clark Barrett\) is described as being &quot;called billions of times a day in production pipelines at Amazon&quot; and used in Amazon&\#x27;s Kiro for specification analysis and test generation, and Theorem has a published collaboration with Anthropic on LLM-scaled formal verification. Anthropic&\#x27;s own post reports Opus 5.5 reaching a 50% solve rate on 36 small verification tasks with roughly 40% fewer tokens than Opus 5, which speaks to cost trends rather than to who is paying. Public materials do not disclose specific commercial data for any of these vendors, so there is no independent evidence of a paying market at the individual-developer level.

**「风险」** 最直接的风险是这几家厂商自己会把工具链做成端到端产品（&amp;Truth 已明确设想验证机器直接接入 coding agent），把中间层的规格工具和服务空间吃掉；其次是形式化验证目前 token 成本高，Anthropic 报告 Opus 5.5 在 36 个小任务上 50% 解决率、比 Opus 5 少用约 40% token，成本若不能持续下降，下游付费意愿会被压制。

**「讨论情况」** 本条没有可用的社区评论。文章引用的外部声音只有厂商方（Barrett 访谈、Axiom CEO Carina Hong 的表述）和 Cognition 开发者关系人员 Nader Dabit 关于&quot;outcome engineering&quot;的一条推文，均属观点而非独立实测反馈。

<details><summary>References</summary>
<ul>
<li><a href="https://techcrunch.com/2026/11/05/axiom-math-wants-to-keep-ai-slop-out-of-mathematics/">Axiom Math wants to keep AI slop out of mathematics | TechCrunch</a></li>
<li><a href="https://spectrum.ieee.org/enormous-theorem-ai">Enormous Theorem AI Swarm Validates 15,000 Pages - IEEE Spectrum</a></li>
<li><a href="https://www.anthropic.com/research/formalizing-fermats-last-theorem">Formalizing Fermat&#x27;s Last Theorem \ Anthropic</a></li>
<li>LLMs are making formal software verification feasible at a ... - Anthropic</li>
<li>#ai #programming #softwareengineering | Addy Osmani</li>
<li>LLMs are making formal software verification feasible at a much ...</li>

</ul>
</details>

**Tags**: `#形式化验证`, `#AI代码质量`, `#Lean`, `#行业综述`, `#变现路径不清晰`

---

<a id="item-ai-opportunity-4"></a>
### [Gemini 在 Mac 上代用户操作](https://www.bloomberg.com/news/articles/2026-11-19/google-s-gemini-can-now-control-mac-devices-on-users-behalf) ⭐️ 5.0/10

Google 为 Mac 版 Gemini 增加了“电脑操作”功能：Gemini 可以点击、输入、浏览菜单和填写表单，代替用户完成任务。该功能已向美国地区使用 Mac 版 Gemini、并订阅 Google AI Plus、Pro 或 Ultra 的用户开放。用户可以让 Gemini 在独立的后台窗口中运行，同时继续使用主屏幕和光标；还可以限制它能访问哪些应用、实时查看它的操作、随时暂停，并在关键操作前要求审批。这是 Google 官方产品的能力更新，不是开源项目，也没有公布独立定价。

telegram · zaihuapd · Nov 20, 02:51

**「Why now」** The window is defined by a platform change rather than a model breakthrough: Gemini&\#x27;s computer use on Mac is rolling out in English to US paying subscribers \(AI Plus/Pro/Ultra\) as of November 19, 2026, per 9to5Google and The Verge. The Verge reports Google shipped this ahead of Apple imposing new restrictions on apps requesting &quot;full disk access&quot; on macOS because of risks from AI agents with computer use — meaning the rules for desktop agents are about to tighten, and tooling built around the current open behavior may need rework. How long the window stays open cannot be judged from the available material.

**「能不能做成产品」** 个人开发者无法复刻底层能力，因为这项能力依赖大模型和系统级权限，所以直接做同类桌面 Agent 不现实。可行的外围方向是：面向已经订阅 Gemini 的 Mac 用户，做“操作配方”或自动化模板库，例如固定流程的表单填写、跨应用数据搬运、审批前的检查清单；MVP 可以是一个轻量的配方管理器和分享站，按订阅或一次性买断收费。但这类工具的价值高度依赖 Gemini 的操作接口是否稳定、是否允许第三方调用，公开材料未披露相关 API，因此能否做成目前无法确认。

**「能不能接单」** 现有材料没有显示任何企业或团队在为“Gemini 代操作 Mac”付费采购或寻求集成，也没有招聘、社群提问等需求迹象。可以设想的方向是帮小团队配置受限应用白名单、设计审批节点和操作流程，但这是推测，不是已观察到的需求。

**「Money side」** The only disclosed payer here is Google itself: the feature is gated behind Google AI Plus, Pro, or Ultra subscriptions for US Mac users, so the monetization is Google&\#x27;s subscription upsell, not a third-party market. No pricing, revenue, paid-customer counts, or hiring signals tied to this specific capability appear in the supplied material or tool results. Public materials do not disclose concrete commercial data for third-party tooling around Gemini&\#x27;s Mac computer-use feature.

**「风险」** 这项功能由 Google 自己提供并持续迭代，平台方随时可能内建更多自动化和模板能力，把外围工具的空间挤掉；同时系统级操作权限的开放范围和政策由 Google 单方面决定，第三方能否稳定接入没有保证。

<details><summary>References</summary>
<ul>
<li><a href="https://9to5google.com/2026/11/19/gemini-mac-computer-use/">Gemini app for Mac adds computer use to control desktop apps</a></li>
<li><a href="https://www.theverge.com/tech/1037902/google-gemini-macos-ai-computer-use">Gemini on Mac can now use your computer | The Verge</a></li>
<li><a href="https://shiftdelete.net/en/gemini-mac-computer-use">Gemini on Mac Gets Computer Use for Repetitive Tasks</a></li>

</ul>
</details>

**Tags**: `#桌面Agent`, `#Google Gemini`, `#生态更新`, `#平台依赖风险`, `#间接机会`

---

<a id="item-ai-opportunity-5"></a>
### [豆包工作下调模型倍率](https://mp.weixin.qq.com/s/nOSgci0nY2cGe06paOozfA) ⭐️ 5.0/10

豆包工作（字节跳动旗下 AI 办公平台）下调了多款模型的额度消耗倍率：DeepSeek V4.1 Flash 与豆包 2.1 Lite 的倍率降至 0.01，简单对话和低消耗任务不再计费。平台方称按实测数据超八成日常办公任务可免费完成，并给出单次 3D 建模约 0.23 元、写动态网页 0.06 元的示例。同步上线签到领额度、新用户 30 天体验，并接入 Kimi K3.1 Pro、GLM 5.3 等第三方模型。以上价格与比例均为平台方宣称，公开材料未披露独立验证数据。

telegram · zaihuapd · Nov 20, 10:17

**「为什么是现在」** 变化点在推理侧成本：把常用轻量模型的消耗倍率压到 0.01，意味着嵌入这类模型的办公类小工具，单次调用成本接近可忽略。对个人开发者而言，这降低了做 AI 办公产品的试错门槛。但这是平台单方面的定价动作，随时可能再调，窗口长度无法从现有材料判断。

**「能不能做成产品」** 可以做，但只能做“薄壳”型产品：目标用户是中小团队里被重复文档工作困住的运营、行政、销售，痛点是格式转换、批量改写、表格整理、周报汇总这类高频低价值任务。MVP 是一个接豆包工作 API 的窄场景工具，比如“把一堆会议记录整理成固定模板的周报”，单点做深、不做通用助手。收费走订阅（月付 9–29 元）或按次买断的小程序/插件。两三人团队 2–4 周可出可用版本。卡点在于：产品价值几乎全部来自底层模型，平台自己就在做同类办公入口，独立产品很难建立壁垒；如果只是把豆包工作的能力包一层界面，用户没有理由不从原平台用。

**「能不能接单」** 服务侧比产品侧更现实：客户是已经想用 AI 办公但不会搭流程的中小企业，交付物是“把豆包工作接进他们现有文档/表格流程”的部署与培训，或按场景定制一套提示词与模板库。需求来源目前只能从平台自身的推广动作（签到、新用户体验）间接推断企业侧在试用，公开材料里没有招聘、社群提问等直接需求证据，因此这条线是否成立需要自己先去客户那边验证。

**「钱在哪一边」** 公开材料只披露了平台侧的定价：倍率 0.01、单次 3D 建模约 0.23 元、写动态网页 0.06 元，以及签到送额度和 30 天新用户试用。这些是厂商宣称，没有独立收入、付费客户数或第三方验证数据。对个人开发者来说，这里能确认的只有“成本下降”，不是“有人付钱”。

**「风险」** 最大风险是平台自己覆盖：豆包工作本身就是办公入口，今天免费八成任务，明天可能把你想做的那个窄场景直接做成内置功能。其次是倍率与免费政策由平台单方调整，成本优势可能一夜消失；接入第三方模型也意味着可用性和价格受多方牵制。

**Tags**: `#模型定价`, `#推理成本下降`, `#AI办公工具`, `#平台生态更新`, `#间接机会`

---

<a id="item-ai-opportunity-6"></a>
### [OpenAI 后台模式长任务折扣](https://developers.openai.com/api/docs/guides/background) ⭐️ 5.0/10

OpenAI 在 API 中上线后台模式（background mode）：请求里设 background: true，再用 background\_options.completion\_window 选 2h 或 8h 完成时限，对应 token 费率比标准价低 30% 和 40%；不设则走默认 soonest，无折扣。折扣目前在 GPT-6.2 Astra、GPT-6.2 Sol、GPT-6.1 Terra、GPT-6 Luna 上公测。官方文档另注明：后台模式会临时存储响应数据，即使 store 设为 false 或启用零数据保留也不例外。

telegram · zaihuapd · Nov 20, 11:15

**「为什么是现在」** 这是定价与执行模型的同步调整：把长耗时请求从同步调用改成异步排队，用等待时间换 30%–40% 的 token 折扣，等于给批处理类负载直接降价。窗口长度无法从现有材料判断——折扣仍处公测，OpenAI 未披露公测结束时间或正式定价。

**「能不能做成产品」** 单独把后台模式包装成产品做不成，它只是 API 参数，没有独立售卖面。可行的做法是把它当作成本结构的一部分，做面向具体场景的长任务工具：例如批量文档抽取/翻译、整库代码审查、长音频转写后处理、夜间跑的数据清洗管道。目标用户是已有稳定 token 消耗、对延迟不敏感的小团队；MVP 是一个提交任务、轮询状态、失败重试、结果落库的薄封装，两三人一两周可出。收费按任务量或订阅，利润来自折扣差价与工作流封装，而非模式本身。

**「能不能接单」** 有间接服务需求：帮已有 OpenAI 集成的团队把同步长调用改造成后台模式，交付物是改造后的调用层、超时/重试/结果回调逻辑和一份成本对比。客户来源应是现有 API 账单较高的团队，但本条材料未提供任何招聘、社群提问或询价迹象，需求规模无法判断。

**「钱在哪一边」** 唯一确定的商业事实是折扣幅度：2h 窗口 token 费率低 30%，8h 低 40%，适用四个模型且处于公测。OpenAI 未披露该模式的调用量、收入或客户数，公开材料未披露具体商业数据。

**「风险」** 折扣是公测价，OpenAI 可随时调整或取消；后台模式强制临时存储响应数据、且不受 store: false 与零数据保留约束，对有合规或数据驻留要求的客户是硬性阻碍，做企业服务时需先确认这一点。

**Tags**: `#API 定价更新`, `#成本优化`, `#异步长任务`, `#生态信息`, `#间接机会`

---
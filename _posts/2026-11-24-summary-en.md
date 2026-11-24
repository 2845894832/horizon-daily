---
layout: default
title: "Horizon Summary: 2026-11-24 (EN)"
date: 2026-11-24
lang: en
---

> From 39 items, 5 important content pieces were selected

---

**AI Opportunity Radar**
1. [Ternary Bonsai 2.5 27B](#item-ai-opportunity-1) ⭐️ 5.0/10
2. [songe：闲置算力训练本地模型](#item-ai-opportunity-2) ⭐️ 5.0/10
3. [LLM 能力拐点回顾](#item-ai-opportunity-3) ⭐️ 5.0/10
4. [GLM-5.4 循环 Transformer 发布](#item-ai-opportunity-4) ⭐️ 5.0/10
5. [文心 5.5 Flash 开源](#item-ai-opportunity-5) ⭐️ 5.0/10

---

## AI Opportunity Radar

<a id="item-ai-opportunity-1"></a>
### [Ternary Bonsai 2.5 27B](https://prismml.com/news/bonsai-2-5-27b) ⭐️ 5.0/10

Ternary Bonsai 2.5 27B is a ternary-quantized 27B model released by PrismML, distributed as a Q2 GGUF, per the announcement page and HN discussion. A commenter reports roughly 22-25 tok/s generation on a Mac Mini M5 Pro with 24GB RAM and 128k context fitting in memory; another says it ran through Unsloth Studio at speeds similar to a Q4 small model on a MacBook. No license terms, pricing, or benchmark methodology are given in the supplied material, so the SWE-bench comparison raised in comments is unverified.

hackernews · b0m · Nov 24, 20:08 · [Discussion](https://news.ycombinator.com/item?id=50633922)

**「Why now」** PrismML positions Bonsai 2.5 27B specifically for agent workloads — long tool-call sequences, coding in a real repository, multi-step tasks — and says it keeps the previous release&\#x27;s 5.9 GB footprint while improving agentic coding and multi-turn tool use over Bonsai 2 27B. That combination \(agent-grade behavior at a size that fits on a single consumer machine\) is what makes local agentic coding plausible now rather than a year ago. The window is hard to size: the release is roughly a day old, and no independent benchmark comparison against equivalently sized quantized models has been published yet.

**「Can you build a product on it」** The plausible product is not the model itself but a local agentic-coding or batch-code-processing tool wrapped around it: target individual developers and small teams who want code agents without per-token API bills or sending code off-device. An MVP would be a CLI or desktop app that manages the GGUF, runs multi-step edit/test loops, and exposes a simple task queue; a two-person team could plausibly ship a rough version in weeks, since the hard part \(the model\) is already published. Charging would likely be a one-time license or low-cost subscription for the wrapper, but willingness to pay is unproven — the model is free to download and the community is currently comparing it to other free quantizations, not asking for a paid product. Treat this as a bet, not a validated opportunity.

**「Can you sell services around it」** No service demand is visible in the supplied material. Comments are technical evaluation \(speed numbers, benchmark skepticism, hardware-acceleration questions\), not requests for deployment, integration, or training help. A possible future angle is helping teams set up private local coding agents on their own hardware, but nothing in this thread shows anyone currently buying that.

**「Market signal」** No pricing, revenue, paid-customer counts, or hiring signals appear in the source item or the supplied tool results; the vendor page only makes capability claims \(fewer turns, fewer tokens, faster and more accurate results than Bonsai 2, plus a SWE-bench Verified figure\). A third-party test video frames the claim as &quot;95% of FP16 intelligence retained&quot; and asks whether that holds in independent testing, and a blog notes that Terminal-Bench and SWE-bench figures sit outside the vendor&\#x27;s headline 20-benchmark average — so the performance story is vendor-claimed and only partly independently checked. Public materials do not disclose commercial data for this release.

**「What could kill it」** The wrapper is thin: anyone can download the same GGUF, and larger vendors shipping free local-model runners or built-in local agents could absorb the use case. The model&\#x27;s own viability also depends on facts not in evidence here — license terms and whether the benchmark claims hold up under independent testing.

**「What commenters found」** Practical reports are positive but narrow: one user measured 22.3 tok/s generation and 222.9 tok/s prompt processing on a Mac Mini M5 Pro, and another called agentic calls &quot;solid&quot; and better than a Q4 small model. Skepticism centers on whether the SWE-bench parity claim reflects real capability or benchmark overfitting, and one commenter asks for direct comparisons against equivalently sized quantized models — a comparison that, as of this thread, had not been posted.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.prismml.com/models/bonsai-2-5-27b">Ternary Bonsai 2.5 27B - Bonsai - docs.prismml.com</a></li>
<li><a href="https://prismml.com/news/bonsai-2-5-27b">PrismML — Introducing Ternary Bonsai 2.5 27B: Powering ...</a></li>
<li><a href="https://huggingface.co/collections/prism-ml/bonsai-25-27b">Bonsai 2.5 27B - a prism-ml Collection - Hugging Face</a></li>
<li><a href="https://prismml.com/news/bonsai-2-5-27b">PrismML — Introducing Ternary Bonsai 2 . 5 27 B : Powering Agentic...</a></li>
<li><a href="https://www.youtube.com/watch?v=83QRLhKueC8">Ternary Bonsai 27 B benchmarked and tested vs Qwen... - YouTube</a></li>
<li><a href="https://goremy.ai/blog/articles/run-local-ai-agents-quantized-orcasaq2-and-bonsai-2-tested">Run Local AI Agents: Quantized OrcaSAQ2 and Bonsai 2 Tested</a></li>

</ul>
</details>

**Tags**: `#本地推理`, `#小模型/量化`, `#agentic coding`, `#生态信息`, `#变现路径不清晰`

---

<a id="item-ai-opportunity-2"></a>
### [songe：闲置算力训练本地模型](https://github.com/sous-labs/songe) ⭐️ 5.0/10

songe 是 sous-labs 发布在 GitHub 上的开源训练引擎，定位是让用户用自己闲置的算力训练本地模型。项目以 GitHub 仓库形式公开，采用开源协议（具体协议类型在现有材料中未披露），没有公布定价或商业版本。目前能确认的状态只是&quot;已开源、有人在 Hacker News 上讨论&quot;，没有版本号、star 数、下载量等热度指标，也没有任何效果基准数据。

hackernews · bluepeter · Nov 24, 15:03 · [Discussion](https://news.ycombinator.com/item?id=50629231)

**「Why now」** The window here is about local inference stacks becoming a stable substrate to train against: Songe targets models served by LM Studio, Ollama, llama.cpp, mlx-lm or vLLM, with training on Apple Silicon via MLX and NVIDIA/AMD on Linux and Windows described as supported but less tested. That means a solo developer can point a training loop at a model they already run, without renting GPUs. The comments show the demand is still pre-purchase — people are asking for rough improvement-per-epoch numbers, how improvement is judged, and whether it works on a GPU-less Windows PC or VPS, which suggests the &quot;does it actually help&quot; question is unresolved. How long this window stays open cannot be judged from the available material.

**「能不能做成产品」** 目标用户是已经在本地跑小模型（如通过 Ollama 跑 Qwen）的个人和小团队，他们的麻烦是：想让模型适配自己的具体任务（比如票据 OCR 复核），但不想付 GPU 云费用。MVP 可以是一个&quot;本地任务数据采集 + 定时训练 + 效果对比报告&quot;的封装层，把 songe 这类引擎包起来，解决评论区反复问的两个问题：训练一晚上到底提升多少、怎么判断变好了。收费可以做成一次性买断的桌面工具或低价订阅。两三人小团队做封装层大概几周到一两个月，但前提是 songe 本身能稳定跑在无 GPU 的普通机器上——这一点材料里没有证据，评论区用户 vcampos2017\_dev 也正好在问同样的问题。如果核心训练必须依赖 GPU，这个产品方向对个人开发者就不成立。

**「能不能接单」** 有初步的服务需求迹象，但很弱。评论区的提问集中在&quot;我的普通 Windows PC / 无 GPU 的 VPS 能不能跑&quot;、&quot;周末训练能提升多少&quot;、&quot;怎么判断改进&quot;，这类问题天然对应&quot;帮我把本地模型调好&quot;的定制服务，客户是个人开发者和小团队，交付物是环境部署加一次针对具体任务的微调。需求来源目前只有 Hacker News 评论，没有招聘信息、社群付费提问或企业采购迹象，所以现在只能算潜在需求，不能算已验证的接单市场。

**「Market signal」** The source item and comments contain no pricing, revenue, paid-customer counts, or funding data for songe, and no external tool result verifies any commercial traction for it. The only adjacent commercial context found is that local-model tooling is a crowded space with established players: Unsloth markets itself as a way to run and train nearly every model locally, and consumer hardware coverage notes 16GB is now the entry point for serious local AI. That suggests demand for local training exists, but it does not show anyone paying for songe specifically.

**「风险」** 最大风险是效果无法证明：评论区没有人给出训练前后的具体数字，如果实际提升很小或不可复现，围绕它做封装产品或服务都缺少说服客户的核心卖点。其次是硬件门槛不明，若实际需要 GPU，目标用户群会大幅缩小。

**「评论区实战信息」** 没有人说自己已经跑过并给出结果。krawczstef 提出想做 LLM 版的 SETI@home 分布式训练，并承认复杂度很高；great\_psy 和 mock-possum 都在问同一个实际问题——训练一个周末能提升多少、系统如何判定&quot;变好&quot;，mock-possum 还要求 README 里给出一个完整的改进判定案例。vcampos2017\_dev 描述了真实使用场景：普通 Windows PC 上用 Ollama 跑小 Qwen 做票据 OCR 复核，以及一台无 GPU 的 Hostinger VPS 做备用处理，并直接问 songe 在這種机器上是否值得跑。这些是需求信号，不是效果证据。

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/sous-labs/songe">GitHub - sous - labs / songe : A training engine for your local model ...</a></li>
<li><a href="https://souslabs.ai/songe">About Songe · Sous Labs</a></li>
<li><a href="https://insiderllm.com/guides/best-local-llms-mac-2026/">Best Local LLMs for Mac in 2026 — M1 through M5 Tested</a></li>
<li><a href="https://unsloth.ai/">Unsloth - Run and Train Models Locally</a></li>

</ul>
</details>

**Tags**: `#开源工具`, `#本地模型训练`, `#闲置算力`, `#生态信息`, `#变现路径不清晰`

---

<a id="item-ai-opportunity-3"></a>
### [LLM 能力拐点回顾](https://simonwillison.net/2026/Nov/24/llm-inflection-points/) ⭐️ 5.0/10

Simon Willison 在 AI Engineer Code Summit 的主题演讲回顾文章中，提出过去十二个月 LLM 与编码 agent 出现三个能力拐点：2025 年 11 月 Claude Opus 4.5 让编码 agent 首次默认给出可用结果；2026 年 6-7 月的 Fable 类模型（Fable 5、5.1、5.2、Opus 5.5 等）表现出主动性和工具自建能力；2026 年 9-10 月起前沿模型在 Blender/Three.js 3D 建模和游戏开发上明显变强，Opus 5.5 能通过“让游戏更好玩”的指令重做玩法。这是作者个人体验与厂商宣称的生态观察，不是产品发布，也未披露任何付费方、收入或市场规模。

rss · Simon Willison · Nov 24, 23:02

**「为什么是现在」** 文章把拐点锚定在具体模型发布时间上：Opus 4.5 发布于 2025 年 11 月 24 日，Opus 5.5 发布于 2026 年 9 月 22 日，Fable 5 在 2026 年 6 月发布后一度被美国出口管制下架、7 月 1 日恢复。作者称 Opus 5.5 是第一个“理解好玩”的模型，并提到此后两场会议上看到有人展示真正可玩的游戏项目。这些是作者观察，不是独立验证的市场信号；对个人开发者而言，能力窗口存在，但变现窗口无法从现有材料判断。

**「能不能做成产品」** 可做的方向是面向独立游戏开发者和小型工作室的“AI 辅助玩法调优”工具：输入现有原型和一句“让游戏更好玩”的目标，自动跑多轮 playtest、生成改动建议并重平衡数值。MVP 可以是一个本地脚本，调用前沿模型 API 对游戏状态做批量模拟和参数搜索，输出可合并的 diff，按订阅或按次收费。两三人小团队约 1-2 个月可做出原型，但核心依赖前沿模型 API 的编码与推理能力，模型涨价或平台限制会直接压缩利润。另一个方向是 3D 资产生成流水线（Blender/Three.js 脚本生成 + 人工审核），门槛更低但同质化严重。

**「能不能接单」** 有服务需求的迹象来自文章描述的场景：会议上有人展示 AI 辅助开发的游戏项目，独立游戏圈因 AI 编程出现争论。可面向小型游戏团队提供“AI 玩法调优工作流搭建”服务，交付物包括提示词与工具链配置、playtest 自动化脚本、团队培训。但文章没有给出客户名单、招聘信息或社群提问的具体来源，需求规模无法从现有材料判断。

**「钱在哪一边」** 公开材料未披露具体商业数据。文章只提到作者用 Fable 5.2 在三周内发布了 Datasette 1.0a42-a44 和 LLM 0.37-0.38 等多个版本，属于个人生产力证据，不是付费证据。文中提到“GTA VI 是最后一个前生成式 AI 大作”的说法，属于社区情绪，不是市场数据。

**「风险」** 最大风险是模型厂商把“玩法调优”或 3D 资产生成直接做进编码 agent 或游戏引擎插件，免费覆盖个人开发者的工具层。其次是前沿模型 API 价格波动和出口管制类政策变化——Fable 5 曾被下架近一个月，说明依赖单一模型的能力窗口并不稳定。

**Tags**: `#LLM能力拐点`, `#AI编码agent`, `#AI游戏开发`, `#生态观察`, `#无付费证据`

---

<a id="item-ai-opportunity-4"></a>
### [GLM-5.4 循环 Transformer 发布](https://simonwillison.net/2026/Nov/23/glm-54/) ⭐️ 5.0/10

智谱（Z.ai）发布 GLM-5.4，这是其首个采用循环 Transformer 架构的模型：一组共享权重的层在一次前向传播中多次迭代，在不增加参数量的前提下加深网络。目前只通过 API 提供，权重未开源，官方称会在完成安全加固后&quot;负责任地&quot;开源。Simon Willison 用 Z.ai 的 Coding Plan 订阅试用，发现 Coding Plan 与普通 API 共用同一个 OpenAI 兼容端点（https://api.z.ai/api/v1），Coding Plan 的 key 可直接调用新模型。他为此写了 llm-glm 插件，但发现 Tommy Hughes 的 llm-zai 已存在，只是尚未支持新模型，表示对方跟上后会下掉自己的。

rss · Simon Willison · Nov 23, 23:40

**「Why now」** GLM-5.4 went live on Z.ai&\#x27;s Coding Plan on November 23, 2026, and is not yet available through the regular API or as open weights — Z.ai says it plans to open-source the weights after safety hardening. The practical window for builders is therefore narrow and access-dependent: the model is reachable only via the Coding Plan subscription, which shares the same OpenAI-compatible Responses API endpoint, so anyone with a coding-plan key can call it today. Z.ai claims intelligence comparable to 2T–3T parameter models at 1M context, but no independent benchmarks were published at release, so the capability edge is unverified. How long this access arrangement lasts cannot be determined from the available material.

**「能不能做成产品」** 单独拿这个模型做产品不成立：权重未开源、只能走 Z.ai 的付费订阅，个人开发者做不了模型层，做上层应用又要和所有能用同一 API 的人同质竞争。唯一可做的小东西是工具链适配——比如给已有 LLM 客户端补上 GLM-5.4 的模型支持，但作者本人的经历已经说明这块空间很窄：llm-zai 这类插件已存在，补一个模型名的工作量以小时计，且原作者打算在对方更新后直接弃用自己的。这类插件没有清晰收费方式，最多作为引流或一次性脚本。

**「能不能接单」** 材料里没有任何企业采购、集成需求或招聘信号，评论区也没有。唯一可想象的交付是帮团队把 GLM-5.4 接进现有 OpenAI 兼容调用链，但这是配置级工作，且 Coding Plan 与普通 API 共用端点这一事实意味着接入门槛极低，难以支撑独立服务报价。不建议作为接单方向。

**「Where the money sits」** The source only discloses one commercial fact: GLM-5.4 is reachable through Z.ai&\#x27;s paid Coding Plan subscription, and the author had to buy it because the model is not yet on the regular API. No pricing, revenue, customer counts, or funding figures are disclosed in the source. For comparison, the competing looped-transformer release Inkling 2 Mini is a 26.4B MoE \(5.4B active\) model that can be run locally via Unsloth/llama.cpp and LM Studio, so the paid-API-versus-open-weights split is the main commercial difference visible here.

**「风险」** 模型权重未开源且官方措辞是&quot;计划&quot;开源，时间未定；若后续不开源或 API 定价/访问方式（目前必须买 Coding Plan 才能用 5.4）变化，基于它构建的任何东西都受制于单一供应商。

<details><summary>References</summary>
<ul>
<li><a href="https://thenextweb.com/news/zai-glm-5-4-loop-transformer-coding-model">Z . ai ’s GLM - 5 . 4 runs its layers twice to rival 2T-parameter models</a></li>
<li><a href="https://www.orcarouter.ai/blog/glm-5-4-release-what-we-know">GLM - 5 . 4 Arrives on Z . ai &#x27;s Coding Plan: No Benchmarks Yet</a></li>
<li><a href="https://anyrouter.dev/model/z-ai/glm-5.4">GLM - 5 . 4 · Zhipu AI · pricing &amp; API · AnyRouter</a></li>
<li><a href="https://thinkingmachines.ai/news/inkling-2-mini/">Introducing Inkling 2 Mini - Thinking Machines Lab</a></li>
<li><a href="https://unsloth.ai/docs/models/inkling-2-mini">Inkling 2 Mini - Run Locally Guide | Unsloth Documentation</a></li>
<li><a href="https://lmstudio.ai/models/inkling-2-mini">Inkling 2 Mini</a></li>

</ul>
</details>

**Tags**: `#模型发布`, `#API 生态`, `#工具插件`, `#选型参考`, `#无直接变现`

---

<a id="item-ai-opportunity-5"></a>
### [文心 5.5 Flash 开源](https://x.com/Baidu_Inc/status/2125077484442190137) ⭐️ 5.0/10

百度于 11 月 24 日通过官方 X 账号宣布开源文心 5.5 Flash Preview，权重以 Apache 2.0 协议在 Hugging Face 和 ModelScope 开放，支持用 vLLM 或 SGLang 部署与微调。模型为 MoE 架构，总参数 280B、每 token 激活 14B、上下文 1M token，是基于 ERNIE 5.5 Flash Base 训练的首个后训练模型。流传的基准图表显示 Terminal-Bench 4.0 得 46.5 分、DeepSWE v1.1 得 71.2 分，但百度未说明是否经第三方独立验证，这些分数目前只能算未经核实的宣传材料。

telegram · zaihuapd · Nov 24, 07:32

**「Why Now」** The timing here is simply the release itself: Baidu announced ERNIE 5.5 Flash Preview on November 24, 2026, with weights under Apache 2.0 on Hugging Face and ModelScope, deployable via vLLM and SGLang \(tool-1-1, tool-1-2, tool-1-3\). The permissive license is what makes derivative work legally straightforward, but the 280B total / 14B active MoE still requires multi-GPU serving, so the practical opening is for people building on hosted APIs or rented compute rather than local deployment. No evidence in the supplied material indicates a demand shift, pricing change, or platform policy change that would define a window; the window length cannot be judged from available materials.

**「能不能做成产品」** 直接拿模型本身做产品不现实：280B 总参数即使只激活 14B，自托管也需要多卡级算力，个人或两三人团队无法本地跑，卡在算力成本而非技术。可行的间接路径是调用百度 API 或租用算力，在 1M 上下文之上做垂直应用，例如长文档审阅、代码库级检索问答、合同比对，目标用户是需要处理超长输入的中小团队。MVP 可以是一个只做单一场景的长上下文工具，按订阅或按量收费，两三人约 1-2 个月可出原型。但这条路径与任何其他长上下文模型没有本质差异，护城河只能来自场景数据和工作流，不来自模型本身。

**「能不能接单」** 有间接服务空间但需求迹象未获证实：可能买单的是想私有化部署或做模型微调的企业团队，交付物包括 vLLM/SGLang 部署、领域微调、推理成本优化。不过 280B 的部署门槛意味着客户必须已有 GPU 集群，这类客户数量有限，且公开材料里没有看到相关招聘、社群提问或询价迹象，需求是否存在无法从现有证据判断。

**「Money side」** No pricing, revenue, paying-customer counts, or hiring signals tied to this release appear in the source or the tool results. The third-party pages found \(benchlm.ai, llm-stats.com\) only aggregate benchmark rows and comparisons against Claude Mythos Preview, Kimi K2.6 and Muse Spark 1.1; benchlm.ai explicitly says there is not enough non-generated coverage to assign a public rank. Baidu&\#x27;s own release page describes the model as an intermediate post-training checkpoint whose training is not finished, so some capabilities may still fall short. Concrete commercial data is undisclosed in public materials.

**「风险」** 最大风险是同质化：长上下文开源模型供给充足，上层应用很容易被大厂免费功能或更便宜的 API 覆盖。另外 Preview 版本意味着权重和接口可能变动，基于它做的产品有返工风险；基准分数未经第三方验证，选型时不宜当作能力保证。

<details><summary>References</summary>
<ul>
<li><a href="https://www.ithome.com/1/031/501.htm">百度文心 5.5 Flash Preview 正式开源：2800 亿参数 140 亿激活，编程...</a></li>
<li><a href="https://news.qq.com/rain/a/20261124A0A7TW00">百度旗下文心5.5 Flash Preview正式开源，总参数量达2800亿</a></li>
<li><a href="https://finance.sina.com.cn/roll/2026-11-24/doc-inizvkmh0055928.shtml">百度文心5.5 Flash Preview正式开源_新浪财经_新浪网</a></li>
<li><a href="https://benchlm.ai/models/ernie-5-5-flash-preview">ERNIE 5.5 Flash Preview Benchmarks &amp; Context (November 2026)</a></li>
<li><a href="https://ernie.baidu.com/release/ernie-5-5-flash-preview/">Introducing ERNIE 5.5 Flash Preview · ERNIE - ernie.baidu.com</a></li>
<li><a href="https://llm-stats.com/models/ernie-5.5-flash-preview">ERNIE 5.5 Flash Preview Benchmarks, Pricing &amp; Context Window</a></li>

</ul>
</details>

**Tags**: `#开源模型发布`, `#生态信息`, `#间接机会`, `#自托管门槛高`, `#证据待验证`

---
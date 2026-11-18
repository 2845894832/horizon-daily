---
layout: default
title: "Horizon Summary: 2026-11-18 (EN)"
date: 2026-11-18
lang: en
---

> From 43 items, 3 important content pieces were selected

---

**AI Opportunity Radar**
1. [编码代理外部沙箱工具](#item-ai-opportunity-1) ⭐️ 5.0/10
2. [GPT-6.2 Astra/Sol 发布](#item-ai-opportunity-2) ⭐️ 5.0/10
3. [DeepSeek 搜索抓取免费](#item-ai-opportunity-3) ⭐️ 5.0/10

---

## AI Opportunity Radar

<a id="item-ai-opportunity-1"></a>
### [编码代理外部沙箱工具](https://simonwillison.net/2026/Nov/17/external-sandboxes-for-coding-agents/) ⭐️ 5.0/10

Simon Willison 与 AI 研究实验室 Prime Radiant 合作，发布三种外部沙箱服务器实现：external-sandbox-v86（Node.js 服务，用 v86 在 WebAssembly 里跑 Alpine Linux）、external-sandbox-container（Python 服务，在 Apple Containers 里跑 Alpine Linux）、external-sandbox-quicksand（Python 服务，用微软 Quicksand 库，把 QEMU 和 Alpine Linux 打包进 Python 包）。三者提供统一的 localhost API，可配置 Pi、Claude Code、Codex 把代码执行请求发到沙箱；另带可选的 HTTP/HTTPS 允许列表代理和凭证替换机制，让代理能发认证请求而不接触密钥。这是作者个人探索项目的开源发布，文中未提及许可证、定价或任何商业安排。

rss · Simon Willison · Nov 17, 22:52

**「Why now」** The timing argument rests on the sandboxing primitives now being packaged rather than on any market shift: Quicksand bundles QEMU and Alpine Linux into a single Python package, and Apple Containers provides a local container runtime, so a working external sandbox no longer requires standing up cloud infrastructure. Simon Willison&\#x27;s stated motivation is running local models without prompt-injection damage, which suggests the window is tied to local-model adoption rather than a dated event. No evidence in the supplied material establishes how long this window stays open.

**「能不能做成产品」** 直接卖沙箱本身很难：三个实现都是免费开源，且依赖 v86、Apple Containers、Quicksand 等现成隔离层，个人开发者做不出差异化。可考虑的窄切口是面向使用 Claude Code / Codex 的小团队做“代理执行策略”托管层——把允许列表代理、凭证替换、审计日志打包成一个可自托管的控制面，MVP 是一个配置 UI 加日志存储，两三人约 1-2 个月可出。但需求是否真实存在、谁会为此付费，公开材料完全没有证据，属于推测。

**「能不能接单」** 可能的服务对象是需要让编码代理接触内部系统、又受合规约束的工程团队，交付物是沙箱部署、允许列表与凭证策略配置、以及给团队的接入培训。但材料里没有任何客户询价、招聘岗位或社群求助的迹象，这条路径目前只能算假设，不建议作为主要方向。

**「Market signal」** The source discloses no pricing, revenue, customer counts, or paid adoption for the three sandbox implementations; they are free open-source demos released with Prime Radiant. The only commercial signal in the supplied material is indirect: third-party security guidance \(NVIDIA developer blog, Jan 2026; two 2026 security guides\) treats sandboxing and credential handling for coding agents as a live operational concern, which suggests buyers exist for compliance-oriented tooling but does not show anyone paying for this specific project. Whether a paid market exists for external-sandbox hosting or integration is not established by the evidence.

**「风险」** 最大风险是上游免费覆盖：Claude Code、Codex 等代理工具若内置沙箱与网络策略，这类外部实现就失去存在理由；此外 Apple Containers 和 Quicksand 的可用性受平台与依赖版本限制，跨平台支持可能随时收窄。

<details><summary>References</summary>
<ul>
<li><a href="https://codepick.dev/en/guides/ai-coding-agent-security-2026/">AI Coding Agent Security Guide 2026: How to Protect Against ...</a></li>
<li><a href="https://decodethefuture.org/en/ai-agent-security-2026/">AI Agent Security 2026: Injection, Sandboxing &amp; Permissions</a></li>
<li><a href="https://developer.nvidia.com/blog/practical-security-guidance-for-sandboxing-agentic-workflows-and-managing-execution-risk/">Practical Security Guidance for Sandboxing Agentic Workflows ...</a></li>

</ul>
</details>

**Tags**: `#AI 代理安全`, `#沙箱隔离`, `#开源工具`, `#开发者基础设施`, `#间接机会`

---

<a id="item-ai-opportunity-2"></a>
### [GPT-6.2 Astra/Sol 发布](https://latent.space/p/ainews-gpt-6-2-astra-the-2-frontier-model-is-better-and-20-600-cheaper-but-has-mixed-reviews-6-2-sol/) ⭐️ 5.0/10

OpenAI 发布了 GPT-6.2 Astra 和 GPT-6.2 Sol 两个模型，已上线 ChatGPT Work、Codex（Plus/Pro/Enterprise/Edu）以及 API（gpt-6.2-astra、gpt-6.2-sol）。API 定价：Astra 每百万 token 输入 $8、缓存输入 $0.40、输出 $40；Sol 维持前代价格 $2/$0.10/$10。两者均为 1M 上下文、128K 输出上限。Artificial Analysis 测得 Astra 在 Intelligence Index 上得 62 分，落后 Fable 5.2 的 65 分，但单位智能成本更低；Sol 以约前代 15% 的单任务成本追平 9 月的 Astra。发布同时伴随大量负面测评反馈，OpenAI 员工公开回应辩护。

rss · Latent Space · Nov 18, 10:19

**「为什么是现在」** 变化点在价格与效率而非能力上限：Sol 以约 15% 的单任务成本达到旧 Astra 水平，Astra 在 Agents&\#x27; Last Exam 1.1 上比 Fable 5.2 便宜约 95% 而分数领先 5.5 分，Perplexity WANDR 上 Astra 单任务约 $12.54、Sol 约 $2.65。对成本敏感的 agent 工作流来说，模型选型的经济账此刻被重算了一遍。但这是模型发布节奏带来的窗口，具体能维持多久无法从现有材料判断。

**「能不能做成产品」** 直接做模型产品做不成，卡在算力和模型本身。可做的是围绕“智能/美元”的选型与成本层：目标用户是已经在跑 agent 流水线、每月 API 账单可观的独立开发者和小团队；麻烦是他们不知道该用 Astra 还是 Sol、哪个 harness 更省。MVP 可以是一个跑固定任务集、对比多个模型与 harness 的实测报告加成本计算器，或一个在 Astra/Sol 之间按任务难度自动路由的轻量代理层。收费可用订阅或一次性报告。两三人团队数周可出第一版，但前提是自己有真实任务集和可复现的评测方法，否则只是转述厂商基准。

**「能不能接单」** 有间接的服务需求迹象，但没有直接证据。材料里 Baseten 测得 22 个 harness 与 5 个开源模型之间单通过任务成本差异最高达 4.4 倍，Google 的 SIM 实验显示 harness 会特化到特定模型（在 Opus 上演化的 harness 拿到 Gemini 上只有 68.41，低于起点的 73.89），说明“换模型要重调 harness”是真实工程问题。可交付的是：为团队做模型迁移与 harness 调优、成本审计、评测流水线搭建。客户来源目前只能从这类讨论和招聘需求推断，材料未披露任何付费案例。

**「钱在哪一边」** 公开材料只披露了厂商定价，没有收入、付费客户数或采购证据。可确认的数字：Astra $8/$0.40/$40 每百万 token，Sol $2/$0.10/$10；Astra 企业版带法律检索索引，Harvey LAB-AA 得分 20.8% 对基础版 15.0%。同批新闻里 Microsoft 称 Copilot Fusion 在 Terminal-Bench 4.1 上达 71.2% 且比 Claude Fable 5.2 便宜 88%，属官方宣称，无独立验证。

**「风险」** 最直接的风险是模型迭代太快：Sol 已经用前代 15% 的成本追平旧 Astra，任何基于当前价差的套利工具可能在下一个版本就失效。其次是负面测评若被证实（有测试者称 Astra 产出的子任务被其他 agent 拒收），基于 Astra 的高端工作流产品会先受损。

**「社区反馈」** 早期测试者分歧明显：Matt Shumer 称经数周测试后模型“基本不可用”，并说自己的 Opus 和 Fable agent 拒收了大量 Astra 的子任务；Pietro Schirano 则把很多早期问题归因于 harness 而非模型本身。这些是个人测评观点，不是共识；发布方 swyx 认为部分批评是过度反应，但也承认 RL 痕迹明显。

**Tags**: `#模型发布动态`, `#API定价对比`, `#成本优化套利`, `#agent harness`, `#生态信息`

---

<a id="item-ai-opportunity-3"></a>
### [DeepSeek 搜索抓取免费](https://www.ithome.com/1/029/058.htm) ⭐️ 5.0/10

DeepSeek 宣布自北京时间 2026 年 11 月 18 日 12:00 起，调用模型时触发的服务端搜索和网页抓取不再单独计费，只按模型 Token 用量收费。触发这些服务的入口包括联网工具、Anthropic API 的 web\_search 工具以及 Responses API 的 web\_search 工具。此前上线的 Search 和 Fetch API 按请求次数收费，每 1,000 次成功请求 5 元。这是一次官方定价调整，来源为 IT之家转述的公告，没有独立验证。

telegram · zaihuapd · Nov 18, 13:44

**「为什么是现在」** 变化本身很具体：联网检索的按次成本从每千次 5 元降为零，只剩 Token 费，联网类 AI 应用的边际调用成本随之下降。但公告没有说明这次调整的原因，也没有给出窗口期，时间窗口无法从现有材料判断。

**「能不能做成产品」** 可以做一个轻量的联网检索工具，但定价变更本身不是产品。目标用户是需要频繁查网页再总结的个人和小团队，比如做竞品监控、行业信息聚合、带引用的问答助手。MVP 可以是一个接 DeepSeek 联网工具的小型 Web 应用：用户输入主题，后台抓取若干网页，输出带来源链接的摘要，按订阅或按 Token 加价收费。两三人团队大约几周能做出原型。难点不在技术，而在获客和差异化：检索加摘要这类形态同质化严重，免费额度也容易被用户自己直接调用 API 绕过，所以产品价值必须落在工作流封装、垂直数据源或结果质量上，而不是“便宜”。

**「能不能接单」** 有间接的服务需求迹象，但没有直接证据。可能买单的是想给内部知识库或客服加联网检索的中小企业，交付物是集成、部署和调优。不过现有材料里没有招聘、社群提问或客户询价的具体信号，这类需求是否存在、规模多大，公开材料未披露。

**「钱在哪一边」** 唯一可确认的商业事实是旧定价：Search 和 Fetch API 每 1,000 次成功请求 5 元，现在改为免费。DeepSeek 没有披露这次调整涉及的调用量、收入影响或付费客户数，公开材料未披露具体商业数据。

**「风险」** 最直接的风险是免费政策可能随时调整或收回，依赖它做成本模型的联网应用会立刻承压；同时搜索和抓取免费会拉低整个“检索加摘要”品类的价格预期，同质化竞争更激烈。

**Tags**: `#API 定价`, `#搜索/抓取`, `#成本下降`, `#生态信息`, `#间接机会`

---
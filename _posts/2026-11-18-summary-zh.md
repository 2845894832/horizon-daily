---
layout: default
title: "Horizon Summary: 2026-11-18 (ZH)"
date: 2026-11-18
lang: zh
---

> 从 43 条内容中筛选出 3 条重要资讯。

---

**AI 变现雷达**
1. [编码代理外部沙箱三实现](#item-ai-opportunity-1) ⭐️ 5.0/10
2. [GPT-6.2 Astra 与 Sol 发布](#item-ai-opportunity-2) ⭐️ 5.0/10
3. [DeepSeek 搜索抓取免费](#item-ai-opportunity-3) ⭐️ 5.0/10

---

## AI 变现雷达

<a id="item-ai-opportunity-1"></a>
### [编码代理外部沙箱三实现](https://simonwillison.net/2026/Nov/17/external-sandboxes-for-coding-agents/) ⭐️ 5.0/10

Simon Willison 与 AI 研究实验室 Prime Radiant 合作，发布三种「外部沙箱」服务器实现：external-sandbox-v86（Node.js 服务，用 v86 在 WebAssembly 里跑 Alpine Linux）、external-sandbox-container（Python 服务，在 Apple Containers 里跑 Alpine Linux）、external-sandbox-quicksand（Python 服务，用微软 Quicksand 库，把 QEMU 和 Alpine Linux 打包进 Python 包）。三者提供同一套 localhost API，可让 Pi、Claude Code、Codex 把要执行的代码发到沙箱里跑；另带可选的 HTTP/HTTPS 允许列表代理和凭证替换机制，让代理能发带认证的请求而不接触密钥。这是作者个人探索性质的开源演示，文中未提及许可证、定价或任何商业安排。

rss · Simon Willison · 11月17日 22:52

**「为什么是现在」** 这条更新本身没有给出时间窗口的证据：它只是 Simon Willison 与 Prime Radiant 合作发布三个开源沙箱服务器实现（v86/WASM、Apple Containers、Quicksand），并说明这是为了更安全地试用本地模型、防止提示注入造成破坏。工具结果只能确认 Prime Radiant 是 Superpowers 这个开源 agentic skills 框架背后的团队（Jesse Vincent 等），说明该团队在编码代理工具链上有持续投入，但这不构成“此刻需求爆发”的证据。因此，为什么是现在、窗口多长，无法从现有材料判断。

**「能不能做成产品」** 目标用户是本地跑开源模型或编码代理、又担心提示注入搞坏机器的开发者，以及要给代理执行环境做合规隔离的小团队。MVP 可以是在这三种实现之上包一层：一键安装、预置常用允许列表模板、执行日志与回放、把凭证替换做成可视化配置，做成桌面小工具或自托管服务。收费走订阅或按席位买断，两三人团队估计数周到一两个月能出可用版本。难点在于这是纯基础设施组件，用户默认它免费开源，付费意愿要靠运维省心和审计合规来撑，需要自己先验证。

**「能不能接单」** 可能有需求的是已经在用 Claude Code、Codex 等代理写代码、又受安全或合规约束的团队：交付物是帮他们把外部沙箱部署进现有开发流程、配好网络允许列表和凭证替换、做一次内部培训。但现有材料里没有任何客户询价、招聘或社群求助的迹象，这条需求目前只能算推测，接单前需要自己去开发者社群和评论区找真实信号。

**「钱在哪一边」** 公开材料未披露任何商业数据：三个沙箱实现均为免费开源，没有定价、付费客户数、收入或融资信息，Prime Radiant 的合作性质也未说明是否涉及商业安排。需求侧的间接信号来自安全指南类内容——2026 年多篇面向开发者的文章把沙箱隔离、提示注入、凭证泄露列为编码代理的核心风险（如 NVIDIA 开发者博客 1 月 30 日的实践指南），说明这是被反复讨论的合规与安全议题，但这些是内容侧讨论，不等于采购证据。

**「风险」** 最直接的风险是上游厂商把沙箱能力内置进代理产品本身（Claude Code、Codex 都在往这个方向走），外部方案就被免费功能覆盖；其次是三种实现分别依赖 v86、Apple Containers、微软 Quicksand，任一上游变更或停更都会让维护成本上升。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/obra/superpowers">GitHub - obra/ superpowers : An agentic skills framework &amp; software...</a></li>
<li><a href="https://www.verdent.ai/guides/what-is-superpowers-ai-coding-framework">What Is Superpowers ? Agent Skills Framework for AI Coding</a></li>
<li><a href="https://codepick.dev/en/guides/ai-coding-agent-security-2026/">AI Coding Agent Security Guide 2026: How to Protect Against ...</a></li>
<li><a href="https://developer.nvidia.com/blog/practical-security-guidance-for-sandboxing-agentic-workflows-and-managing-execution-risk/">Practical Security Guidance for Sandboxing Agentic Workflows ...</a></li>

</ul>
</details>

**标签**: `#AI 代理安全`, `#沙箱隔离`, `#开源工具`, `#开发者基础设施`, `#间接机会`

---

<a id="item-ai-opportunity-2"></a>
### [GPT-6.2 Astra 与 Sol 发布](https://latent.space/p/ainews-gpt-6-2-astra-the-2-frontier-model-is-better-and-20-600-cheaper-but-has-mixed-reviews-6-2-sol/) ⭐️ 5.0/10

OpenAI 发布 GPT-6.2 Astra 与 GPT-6.2 Sol 两个模型，在 Anthropic 预期首个交易日两天前上线。据 Artificial Analysis 测试，Astra 在 Intelligence Index 得 62 分，落后 Fable 5.2 的 65 分；Sol 与 9 月的 Astra 持平，但每任务成本约为后者的 15%。API 定价：Astra 每百万 token 输入 8 美元、缓存输入 0.40 美元、输出 40 美元；Sol 为 2 / 0.10 / 10 美元，两者均为 1M 上下文、128K 输出上限。已通过 API 和 ChatGPT Work、Codex 向 Plus、Pro、Enterprise、Edu 用户开放。

rss · Latent Space · 11月18日 10:19

**「为什么是现在」** 变化点在“智能/美元”而非绝对能力：Sol 以约 15% 的每任务成本达到上一代 Astra 水平，Astra 在 Agents&\#x27; Last Exam 1.1 上比 Fable 5.2 高 5.5 分而成本约为其 5%（均为 OpenAI 自报）。同时 Baseten 测得 22 个 harness 与 5 个开源模型组合下，每通过任务成本差异最高达 4.4 倍，说明选型与 harness 调优本身有可量化的省钱空间。窗口长度无法从现有材料判断，因为下一代模型随时可能抹平价差。

**「能不能做成产品」** 可做，但方向是“成本与选型工具”而非模型本身。目标用户是已经在为 API 账单付费的中小团队与独立开发者，痛点是不知道该用 Astra、Sol 还是开源小模型，也不知道自己的 harness 是否在浪费钱。MVP 可以是一个跑固定任务集的对比器：同一批真实任务分别走几个模型与 harness，输出每通过任务成本、token 消耗和失败原因，再给一份选型建议。收费用订阅（每月重跑）或一次性报告。两三人团队做基础版大约数周量级，但需要自建评测任务集，这部分工作量被材料低估。做不成的是自研模型或推理加速层，依赖算力与训练数据。

**「能不能接单」** 有服务迹象但证据有限。可交付的是“API 成本审计 + harness 调优”：帮客户把现有 agent 流程从高价模型迁到 Sol 或混合路由，按项目或按月收费。需求来源在材料中只体现为开发者对 harness 差异的讨论（Baseten、Google SIM、Perplexity 混合模型团队），没有看到明确的采购信号、招聘或客户询价，因此这类需求目前更像技术社区话题而非已成型市场。

**「钱在哪一边」** 可确认的只有官方定价：Astra 输出 40 美元/百万 token，Sol 10 美元，缓存输入低至 0.10 美元。OpenAI 自报 Astra 在 GDPval v2 上输出 token 比前代少 22%，Perplexity 测得 WANDR 上 Astra 每任务约 12.54 美元、Sol 约 2.65 美元。除此之外，公开材料未披露该产品的收入、付费客户数或分成政策。

**「风险」** 最直接的风险是价格与能力快速变动：Sol 已把上一代 Astra 的能力压到 15% 成本，下一代发布可能让基于当前价差的选型工具和迁移服务迅速过时。其次是评测结论本身不可靠——早期测试者评价分歧明显，Matt Shumer 称模型“基本不可用”，Pietro Schirano 则把问题归因于 harness，若把厂商基准当作事实做产品，容易给出错误建议。

**「社区反馈」** 早期测试者意见分裂：Matt Shumer 称经数周测试“基本不可用”，其 Opus 与 Fable agent 拒绝了大量 Astra 的子 agent 产出；Pietro Schirano 认为多数早期问题出在 harness 而非模型；Peter Gostev 在可视化编码对比中点名 Astra 的 SVG 孔雀。这些是个人测试观点，不是共识，也没有付费意愿方面的信息。

**标签**: `#模型发布动态`, `#API定价对比`, `#成本优化套利`, `#agent harness`, `#生态信息`

---

<a id="item-ai-opportunity-3"></a>
### [DeepSeek 搜索抓取免费](https://www.ithome.com/1/029/058.htm) ⭐️ 5.0/10

DeepSeek 宣布自北京时间 2026 年 11 月 18 日 12:00 起，调用模型时触发的服务端搜索和网页抓取不再单独计费，只按模型 Token 用量收费。触发范围包括联网工具、Anthropic API 的 web\_search 工具和 Responses API 的 web\_search 工具。此前上线的 Search 和 Fetch API 按请求次数收费，每 1,000 次成功请求 5 元。这是一次官方定价调整，不是新产品发布。

telegram · zaihuapd · 11月18日 13:44

**「为什么是现在」** 变化本身很具体：联网检索的按次成本被抹掉，只剩 Token 成本，做搜索代理、RAG、信息聚合类工具时，抓取次数不再直接放大账单。但材料只给出定价公告，没有说明 DeepSeek 为何此时调整，也没有给出窗口期，时间窗口无法从现有材料判断。

**「能不能做成产品」** 可以做，但机会不在“搜索”本身，而在把免费抓取包进一个具体工作流。目标用户是每天要盯多个信息源的小团队，比如竞品监控、招投标公告跟踪、行业政策汇总、跨境卖家盯平台规则变动。MVP 是一个订阅式小工具：用户配置关键词和站点，后台用 DeepSeek 的搜索与抓取拉取内容，模型做去重、摘要和变更提醒，输出日报或推送到飞书、邮件。收费走月订阅（按监控关键词数或站点数分档），两三人一到两个月能做出可用版本。卡点在于：免费的是抓取调用，不是内容版权，抓取目标站点是否允许、是否要登录，才是真正的工程与合规成本。

**「能不能接单」** 有服务空间，但需求来自“帮我把这套东西接进现有系统”，而不是“帮我用 DeepSeek”。可能买单的是已有内容或数据团队的中小企业：交付物是联网检索链路的搭建与调优（提示词、抓取范围、结果去重、成本监控），或把 DeepSeek 的搜索抓取接进客户已有的客服、知识库、舆情系统。目前没有评论区、招聘或社群提问等直接需求迹象，这条只能算推测性方向，需要自己去找客户验证。

**「钱在哪一边」** 唯一可确认的商业事实是官方定价：此前 Search 和 Fetch API 每 1,000 次成功请求 5 元，现在这部分归零，只收 Token 费。付费客户数、收入、采用规模等公开材料未披露具体商业数据，也没有独立第三方验证这次调整的实际影响。

**「风险」** 最直接的风险是这一定价随时可能再变：免费抓取是厂商获客手段，一旦恢复计费或加限流，依赖它的产品成本结构会立刻失效。其次是抓取目标站点的反爬与版权合规，这部分成本不会因为 API 免费而消失。

**标签**: `#API 定价`, `#搜索/抓取`, `#成本下降`, `#生态信息`, `#间接机会`

---
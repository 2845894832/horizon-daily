---
layout: default
title: "Horizon Summary: 2026-11-26 (EN)"
date: 2026-11-26
lang: en
---

> From 48 items, 3 important content pieces were selected

---

**AI Opportunity Radar**
1. [Clay 的 GTM Agent 工程内幕](#item-ai-opportunity-1) ⭐️ 6.0/10
2. [AMD 专用 llama.cpp 分支](#item-ai-opportunity-2) ⭐️ 5.0/10
3. [Cloudflare Workers 免费发邮件](#item-ai-opportunity-3) ⭐️ 5.0/10

---

## AI Opportunity Radar

<a id="item-ai-opportunity-1"></a>
### [Clay 的 GTM Agent 工程内幕](https://latent.space/p/how_clay_builds_gtm_agents_jeff_barg_head_of_ai/) ⭐️ 6.0/10

这是 Latent.Space 对 Clay AI 负责人 Jeff Barg 的访谈，讲 Clay 如何构建面向 GTM（go-to-market）的 agent 基础设施。Clay 在 2025 年 9 月完成 1.15 亿美元 D 轮融资，估值 71 亿美元，团队约 600 人。核心工程事实：Sculptor 最初是基于 Sonnet 3.5 时代模型的工具循环，后来被重写成跑在 Pi harness 上、在云沙箱里调用 Clay CLI 的 coding agent；agent 栈自建，用 BullMQ 做任务队列、Postgres 和 ClickHouse 存产品数据、Snowflake 做分析，没有用 Temporal 或 LangGraph。文中还给出一个成本估算：用 TypeSafe 的 Jev 分类器对 Clay 库中约 4000 万家公司做 ICP 打分，约需 1500 美元，但该模型尚未上生产。

rss · Latent Space · Nov 26, 22:44

**「为什么是现在」** 访谈给出的时间信号是：Jeff 认为自建模型直到最近两个月才变得可行，因为开源权重模型已明显比 Opus 便宜，可以先替换、再针对自家工具和查询做 post-training。他给出的门槛是推理支出达到 1000 万至 1 亿美元之间，低于这个量级省下的钱不足以抵消投入。对个人开发者而言，这个窗口不成立——它描述的是 Clay 这种量级公司的决策条件，不是小团队的。

**「能不能做成产品」** 直接复制 Clay 的路线做不成：它依赖 4000 万家公司数据库、CRM/Gong 数据打通、自建沙箱与队列基础设施，以及每年千万美元级的推理预算。可提取的间接方向有两个，但都偏窄。一是“模型路由”类小工具——Jeff 明确说客户讨厌模型选择器，Clay 即将上线自动路由，说明这是真实痛点，但 Clay 自己就要做，第三方空间很小。二是 agent trace 调试——Jeff 说现在模型只会标记耗时长的步骤，无法定位真正的错误步骤，Clay 只能手写 skill。如果做一个读取长 trace、定位失败步骤的轻量工具，目标用户是跑 agent 的工程团队，MVP 可以是一个接 OpenTelemetry/LangSmith 导出格式的分析脚本加简单 UI，按订阅收费，两三人一两个月可出原型。但需求是否足够普遍、能否对抗 LangSmith 等平台自带功能，材料里没有证据。

**「能不能接单」** 有间接的服务需求迹象，但不在本文证据内。文中提到 Clay 的 GTM 团队自己住在 Cursor 里、要求出 CLI，销售团队在 Codex 里做 deal prep，说明“把 Clay 接进现有 coding agent 工作流”是真实存在的内部需求。对外可做的服务是帮中小销售/增长团队配置 Clay CLI、MCP 集成和 Workflows 迁移，交付物是部署加培训。但本文没有提到外部客户在找这类服务，也没有价格或招聘信号，所以只能算推测。

**「钱在哪一边」** 可核实的商业数据只有 Clay 自身：2025 年 9 月 1.15 亿美元 D 轮、71 亿美元估值（公司博客口径），团队从约 50 人增长到约 600 人。Jeff 给出的单位经济是每个合格线索 1 至 10 美元的 enrichment 预算、每个约成的电话 10 至 100 美元，属于访谈中的经验值而非披露的定价。Clay 的 agent 与外部 harness 的使用量接近五五开，也是 Jeff 的说法。第三方工具（如 TypeSafe 的 Jev）的收入、客户数公开材料未披露。

**「风险」** 最直接的风险是平台方自己覆盖：Clay 即将上线自动模型路由，并计划推出免费使用其全部工具的沙箱 agent，任何围绕 Clay 工作流的第三方薄封装都可能被官方功能吞掉。另一个风险是本文所有工程细节都来自公司高管访谈，属于官方口径，成本数字（1500 美元、1000 万至 1 亿美元门槛）未经独立验证。

**Tags**: `#GTM agent`, `#AI 工程架构`, `#coding agent`, `#模型路由`, `#生态参考`

---

<a id="item-ai-opportunity-2"></a>
### [AMD 专用 llama.cpp 分支](https://devnull.land/amd-specific-llama-cpp) ⭐️ 5.0/10

一个面向 AMD GPU 的 llama.cpp 分支，作者在 devnull.land 上发文，并在 Hacker News 上引发讨论。讨论的核心是：如何让 2018 年前后的 gfx906 数据中心卡（如 MI50/MI60 一类，32GB HBM2、约 1TB/s 带宽、二手约 200 美元）跑出可用的本地推理速度。这些卡没有 tensor core、没有原生 bf16，因此需要针对 ROCm 做内核层面的改写。帖子本身没有披露分支的版本号、开源协议、性能基准或维护状态，公开材料也未给出 star 数等热度指标。

hackernews · julianlam · Nov 26, 17:11 · [Discussion](https://news.ycombinator.com/item?id=50657265)

**「Why now」** The window comes from a hardware price gap rather than a new model release: per one HN commenter, circa-2018 gfx906 datacenter cards \(Instinct MI50/MI60, Radeon VII\) offer 32GB of HBM2 at roughly 1 TB/s for about $200 used, versus north of $3000 for the nearest current equivalent. That gap has already produced a small cluster of forks retuning llama.cpp for these cards&\#x27; missing tensor cores and lack of native bf16 — a GitHub project \(sixvolts/llamacpp-gfx906-furnace\) adds GCN weight-repacking and DPP-based warp reductions ported from the reinstinct engine. How long this lasts is not determinable from the material: it depends on used gfx906 supply and prices, which no source here quantifies. Treat the $200 and $3000 figures as one commenter&\#x27;s claim, not verified market data.

**「能不能做成产品」** 目标用户很明确：手里有便宜 gfx906 卡、想跑本地大模型的个人和小团队。他们真正的麻烦不是缺一个 fork，而是装不上、跑不快、量化选错、ROCm 版本对不上。MVP 可以是一个“开箱即用”的镜像或一键脚本：固定 ROCm 版本 + 预编译好的 AMD 优化二进制 + 几套验证过的量化模型配置 + 一份按卡型给出的吞吐参考表。收费方式适合一次性买断（比如几十美元的镜像/脚本包）或按次咨询，订阅制在这个人群里很难成立，因为硬件是一次性投入、用户偏 DIY。两三人小团队 2–4 周能做出可用版本，但要注意：核心优化工作大量来自社区上游，你的增量主要是打包、验证和支持，护城河很浅。

**「能不能接单」** 有服务需求的迹象，但规模小。评论区里已经有人自己动手改内核（把 Nvidia kernel 移植到 ROCm 并用 Claude 做数值校验），说明这类工作对普通用户门槛偏高，愿意付钱买“帮我调通”的人是存在的。可交付物包括：单机部署与调优、ROCm/驱动版本排障、针对特定模型（如 Qwen 系列）的量化与吞吐调优、小团队内训。客户来源主要是 HN/Reddit 本地推理社群、二手矿卡交易群里的提问。没有看到企业级采购或招聘岗位的信号，所以这更像零散接单而不是稳定业务。

**「Where the money is」** The only concrete money in this thread is on the hardware side: commenters cite used 32GB gfx906 cards at roughly $200, and external guides put used MI50 32GB units at about $500–540 over the 12 months to August 2026, framing them as the cheapest fast VRAM for local LLMs. No pricing, revenue, customer counts, or paid tiers are disclosed for the fork itself or for the alternative engines mentioned \(Radiance, Splash, vicuna.cpp\); those are personal repos and community reports, not commercial offerings. The commercial activity visible here is secondhand GPU resale and the demand for software that makes those cards usable, not a paid product attached to this fork.

**「风险」** 最大风险是上游吞掉这个需求：llama.cpp 主线和 ROCm 一旦把 gfx906 的路径优化好，独立分支和打包服务的价值会迅速下降。其次是硬件本身在退场——这批卡是 2018 年产品，二手供给和驱动支持都会逐年变差，客户群不会增长。

**「评论区实战信息」** 有几位用户报告了实际跑通的结果：一人称在单张 R9700 上用 Radiance 引擎跑到 prefill 2400 tok/s、decode 150 tok/s，并以 4-bit 量化同时跑 3 路 200k 上下文的 agent 流；另一人用 Claude 辅助把 Nvidia kernel 移植到 ROCm，称 Qwen3.8 性能提升 2–3 倍并做了数值校验。这些是个人自述、未经独立验证，但至少说明“便宜 AMD 卡 + 手工调优”这条路在实践上走得通，且调优工作量不小——这正是可以收费的地方。

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/sixvolts/llamacpp-gfx906-furnace">sixvolts/llamacpp- gfx 906 -furnace: Optimized build of llama . cpp for...</a></li>
<li><a href="https://localaimaster.com/blog/amd-mi50-local-llm">AMD MI50 32GB for Local LLMs: The Used VRAM King, Honestly</a></li>
<li><a href="https://www.bigiron.cc/guides/amd-mi50-32gb-the-cheapest-vram-for-local-llms-2026">AMD MI50 32 GB: The Cheapest VRAM for Local LLMs in 2026</a></li>
<li><a href="https://aliteq.com/amd-instinct-mi50-32gb-worth-it-local-ai">Is a Used AMD Instinct MI50 32GB Worth Buying for Local AI ...</a></li>

</ul>
</details>

**Tags**: `#local-inference`, `#llama.cpp`, `#AMD-GPU`, `#hardware-optimization`, `#open-source-tooling`

---

<a id="item-ai-opportunity-3"></a>
### [Cloudflare Workers 免费发邮件](https://developers.cloudflare.com/changelog/post/2026-11-24-email-sending-workers-free/) ⭐️ 5.0/10

Cloudflare 在其开发者文档更新日志中宣布，Workers 的 Email Sending 能力已在 Free 计划上线：开发者可以通过 Workers 绑定、REST API 或 SMTP 向账户中已验证的目标地址发送邮件，用于提醒、报告和通知。向已验证地址发送的邮件在所有计划下都免费，不计入月度配额和每日发送限制；向任意收件人发送则需升级到 Workers Paid 计划。这是一项平台能力更新，不是独立产品或创业项目。

telegram · zaihuapd · Nov 26, 07:35

**「为什么是现在」** 变化点在于免费额度从“不能发”变成“可向已验证地址无限发”，这直接抹掉了通知类小工具最大的一笔固定成本（邮件服务商按量计费）。对个人开发者而言，做定时报告、监控告警、表单回执这类工具，邮件通道可以零成本跑起来。时间窗口无法从现有材料判断，因为这是平台长期能力而非限时活动，但免费额度政策本身随时可能调整。

**「能不能做成产品」** 可以做，但天花板低。目标用户是只需要“发给自己或固定几个人”的场景：个人站长要站点宕机告警、独立开发者要每日数据摘要、小团队要表单提交回执。MVP 很小：一个 Workers 脚本 + Cron 触发器 + 已验证收件人列表，把某个数据源（RSS、API、网页变化）的变化定时邮件推送出去，一两天能出原型。收费方式适合一次性买断的模板/脚本或低价订阅（如每月几美元的托管版），不适合做重 SaaS。关键限制是：免费额度只能发给已验证地址，要做“发给任意用户”的产品就必须上 Paid 计划并自己承担发送成本，那时它相对 Resend、Postmark 等专业邮件服务的优势就不明显了。

**「能不能接单」** 有轻量服务空间但需求信号弱。可能买单的是不懂 Workers 的小团队或个人站长，交付物是“帮你搭一个定时邮件通知/告警”的一次性配置服务，或把现有脚本迁移到 Workers 的集成工作。现有材料没有显示这类需求从哪里来（无评论区、无招聘、无社群提问），因此只能判断为“可能存在零散需求”，不建议作为主要接单方向。

**「钱在哪一边」** 公开材料未披露任何收入、付费客户数或定价数据。唯一明确的商业事实是 Cloudflare 自己的分层策略：免费计划只覆盖已验证地址，向任意收件人发送需要 Workers Paid 计划，也就是说平台把“对外群发”这一高价值能力留在了付费墙后。这既是免费额度的边界，也是 Cloudflare 的变现点，而非第三方开发者的变现点。

**「风险」** 最大风险是政策可变：免费且不计配额是平台单方面给予的，Cloudflare 随时可以收紧（例如限制每日封数或要求付费），依赖它做产品的成本结构会瞬间改变。其次是同质化——邮件通知是极成熟的品类，专业服务商在送达率、模板、退信处理上更完整，Workers 方案的优势主要是便宜和部署简单。

**Tags**: `#Cloudflare Workers`, `#邮件通知`, `#免费额度`, `#开发者工具`, `#生态更新`

---
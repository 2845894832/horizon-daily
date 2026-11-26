---
layout: default
title: "Horizon Summary: 2026-11-26 (ZH)"
date: 2026-11-26
lang: zh
---

> 从 48 条内容中筛选出 3 条重要资讯。

---

**AI 变现雷达**
1. [Clay 的 GTM Agent 工程复盘](#item-ai-opportunity-1) ⭐️ 6.0/10
2. [AMD 版 llama.cpp 分支](#item-ai-opportunity-2) ⭐️ 5.0/10
3. [Workers 免费发邮件](#item-ai-opportunity-3) ⭐️ 5.0/10

---

## AI 变现雷达

<a id="item-ai-opportunity-1"></a>
### [Clay 的 GTM Agent 工程复盘](https://latent.space/p/how_clay_builds_gtm_agents_jeff_barg_head_of_ai/) ⭐️ 6.0/10

这是 Latent.Space 对 Clay AI 负责人 Jeff Barg 的访谈，讲 Clay 如何把自家 GTM agent 从「工具循环」重构成基于 Pi harness 的 coding agent，在云沙箱里跑 Clay CLI，并新增 Audiences 数据层打通 CRM 与 Gong 记录。Clay 2025 年 9 月完成 1.15 亿美元 D 轮、估值 71 亿美元，团队约 600 人。访谈还披露了自建 BullMQ 任务栈（不用 Temporal/LangGraph）、即将上线的自动模型路由、以及用 TypeSafe 的 Jev 分类器给 4000 万家公司打分的约 1500 美元成本估算。内容主体是成熟公司的内部架构与产品策略，不是可直接变现的机会。

rss · Latent Space · 11月26日 22:44

**「为什么是现在」** 访谈给出的时间信号是：Clay 的线索资格判定类 eval 大约一年前就被模型打满，前沿模型的价值转向编排与深度调研；同时 Jeff 认为自建 post-training 只有在推理支出达到 1000 万至 1 亿美元量级后才划算，而 Clay 自己也是最近两个月才觉得可行。对个人开发者而言，这更像是「能力已商品化、差异化上移到编排与数据接入」的时点判断，具体窗口长度无法从现有材料判断。

**「能不能做成产品」** 直接复制 Clay 的 GTM agent 做不成：它依赖 4000 万家公司数据库、CRM/Gong 数据接入、600 人团队和 71 亿美元估值支撑的推理预算。可考虑的窄切口有两个，但都需自行验证：一是面向中小销售团队的「模型路由 + eval 看板」轻工具，帮他们不必每次新模型发布就重跑评测——不过 Clay 自己即将上线自动路由，正面撞车；二是把「读长 agent trace 定位出错步骤」做成独立调试工具，Jeff 明确说现在的模型做不到、Clay 只能手写 skill，这是被点名的空白，但技术难度高，个人两三人团队能否做出可用版本存疑。收费可按订阅或按 trace 量计费，MVP 周期无法从材料判断。

**「能不能接单」** 有间接服务迹象但证据薄弱：访谈提到 Clay 的客户里 agency owners 和 power users 仍想要模型选择器的控制权，且 Workflows 早期遭用户抵触、后来才被接受，说明存在「帮客户把 Clay 工作流搭起来、迁移过去」的落地需求。可交付物是 Clay 工作流搭建、CLI/API 集成、团队培训。但材料没有给出这类需求的具体来源（评论区、招聘、社群提问均未提供），是否值得作为接单方向需自行到 Clay 社区核实。

**「钱在哪一边」** 官方口径：Clay 2025 年 9 月完成 1.15 亿美元 D 轮，估值 71 亿美元，领投方 Wellington；团队从约 50 人增至约 600 人，业务规模增长约 10 倍。Jeff 给出的单位经济是每条合格线索 1 至 10 美元、每次约成的通话 10 至 100 美元，以及全库打分约 1500 美元——这些是访谈中的估算，非审计数据。Clay 自身收入、付费客户数公开材料未披露。

**「风险」** 最直接的风险是同质化与平台覆盖：Clay 即将上线自动模型路由，会吃掉「帮用户选模型」这类外围工具的空间；而 agent trace 调试若被前沿模型厂商补上，独立工具的价值也会迅速消失。此外 Clay 已把 CLI/API 开放给 Claude Code 与 Codex，第三方围绕它做集成的议价空间受平台策略左右。

**「讨论区」** 本条无社区评论可参考。访谈中值得注意的实战信息来自 Jeff 本人而非社区：Sculptor 早期用 LLM 评判工具调用做 eval，漏掉了用户真实用法（分析表格、百万行企业表）；以及 agent 会重复用相同输入重试同一条 CLI 命令。这些是单一受访者观点，未经独立验证。

**标签**: `#GTM agent`, `#AI 工程架构`, `#coding agent`, `#模型路由`, `#生态参考`

---

<a id="item-ai-opportunity-2"></a>
### [AMD 版 llama.cpp 分支](https://devnull.land/amd-specific-llama-cpp) ⭐️ 5.0/10

这是一篇发布在 Hacker News 上的文章，介绍一个针对 AMD 显卡优化的 llama.cpp 分支，并附带了讨论串。文章本身没有披露作者身份、版本号、开源协议或性能数据，源内容为空，只能从评论推断其背景：2025 年初有人发现 AMD 2018 年前后的 gfx906 数据中心卡（如 MI50/MI60 一类）算力一般但配 HBM2 高带宽显存，32GB 显存、约 1TB/s 带宽的二手卡当时约 200 美元，而今天同类新卡要 3000 美元以上。围绕这类没有 tensor core、没有原生 bf16 的老卡，社区形成了一批 llama.cpp 优化分支。

hackernews · julianlam · 11月26日 17:11 · [社区讨论](https://news.ycombinator.com/item?id=50657265)

**「为什么是现在」** 社区里出现这个方向的直接触发点，是 2025 年初有人发现 2018 年前后的 gfx906 数据中心卡（Instinct MI50/MI60、Radeon VII）有 32GB HBM2、约 1TB/s 带宽，二手价约 200 美元，而今天同等带宽的新卡要 3000 美元以上——硬件价差是这波优化的根本动力。围绕这批卡已经形成一个小生态：有人维护针对 gfx906 的 llama.cpp 重调版本（加入 GCN 权重重打包的 GPU buffer 类型、DPP warp reduction，并称这些技术来自已量产的 reinstinct 推理引擎），也有个人仓库把 Nvidia kernel 移植到 ROCm。这些卡没有 tensor core、没有原生 bf16，所以优化空间大、门槛也真实存在，窗口取决于二手卡库存和价格能维持多久，现有材料无法判断具体时长。

**「能不能做成产品」** 能做，但只能做成小工具而非平台。目标用户是手里有 gfx906/MI100 等二手 AMD 卡、想跑本地大模型的个人和小团队；他们的问题是官方 llama.cpp 对这类卡支持差、编译门槛高、量化与 kernel 需要手工调。MVP 可以是一键安装脚本加预编译二进制（按卡型分发），再加一份“哪张二手卡配哪个量化能跑多快”的实测表。收费方式适合一次性买断或低价订阅（比如 5-10 美元/月更新预编译包），不适合按量计费。两三人一两周能出可用版本，但维护成本随 ROCm 版本和卡型增长很快。卡点在于：用户群小、硬件型号分散、上游 llama.cpp 和 ROCm 一旦补齐支持，工具价值会迅速归零。

**「能不能接单」** 有服务需求迹象，但规模有限。评论里有人自己写分支、有人用 Claude 把 Nvidia kernel 移植到 ROCm 并做数值校验，说明“帮我把这套跑起来并调快”是真实存在的麻烦。潜在客户是买了二手 AMD 卡的个人、做本地推理的小工作室、以及想用便宜卡替代高价卡的小企业；交付物是环境部署、ROCm/驱动排障、量化选型、性能调优和一份可复现的跑分报告。需求来源主要是 HN、Reddit 本地 LLM 版块和 ROCm 相关 issue 区，而不是企业采购流程。按小时或按项目收费更现实，做成标准化产品较难。

**「钱在哪一边」** 公开材料未披露该 fork 本身的定价、收入或付费客户数，它只是开源工具。可查到的商业事实集中在二手硬件一侧：据 American Compute 数据，二手 32GB MI50 在截至 2026 年 8 月的 12 个月里成交价约 500-540 美元（经 aliteq 2026 年 8 月 4 日文章转述），另有评测称 MI50 是过去一年本地 AI 圈最热的二手卡（localaimaster，2026 年 9 月 6 日）。也就是说，钱目前流向卖卡的人和愿意为省事付费的装机者，而不是这个 fork 的作者；评论区提到的 Radiance 引擎、Splash 的 M1 移植等也未见公开收费信息。

**「风险」** 最大风险是上游覆盖：llama.cpp 官方或 ROCm 一旦原生支持这些卡，分支和配套服务的价值会快速消失。其次是二手卡供给和价格波动，200 美元这个前提本身可能不成立；另外 ROCm 版本升级经常破坏已有优化，维护负担会持续消耗个人开发者精力。

**「评论区实战信息」** 评论里有几条具体经验：有人称用单张 R9700 配 Radiance 引擎，prefill 约 2400 tok/s、decode 约 150 tok/s，4-bit 量化下 KLD 0.006、top-1 0.972，并能以 200k 上下文跑 3 路并发 agent 流（个人报告，未经独立验证）；有人用 MI100 让 Claude 激进优化 AMD 代码并移植 Nvidia kernel 到 ROCm，称 Qwen3.8 性能提升 2-3 倍，并用原实现做数值校验；还有人提到 M1 上的 Splash 移植让 Qwen 3.8 27B 速度约提升三倍。这些是个人实测口径，不是共识数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/sixvolts/llamacpp-gfx906-furnace">sixvolts/llamacpp- gfx 906 -furnace: Optimized build of llama . cpp for...</a></li>
<li><a href="https://localaimaster.com/blog/amd-mi50-local-llm">AMD MI50 32GB for Local LLMs: The Used VRAM King, Honestly</a></li>
<li><a href="https://www.bigiron.cc/guides/amd-mi50-32gb-the-cheapest-vram-for-local-llms-2026">AMD MI50 32 GB: The Cheapest VRAM for Local LLMs in 2026</a></li>
<li><a href="https://aliteq.com/amd-instinct-mi50-32gb-worth-it-local-ai">Is a Used AMD Instinct MI50 32GB Worth Buying for Local AI ...</a></li>

</ul>
</details>

**标签**: `#local-inference`, `#llama.cpp`, `#AMD-GPU`, `#hardware-optimization`, `#open-source-tooling`

---

<a id="item-ai-opportunity-3"></a>
### [Workers 免费发邮件](https://developers.cloudflare.com/changelog/post/2026-11-24-email-sending-workers-free/) ⭐️ 5.0/10

Cloudflare 在 Workers Free 计划上线 Email Sending 能力，开发者可通过 Workers 绑定、REST API 或 SMTP 向账户中已验证的目标地址发送提醒、报告和通知。发往已验证地址的邮件在所有计划均免费，不计入月度配额和每日发送限制；要发给任意收件人则需升级到 Workers Paid 计划。这是平台能力更新，不是新产品发布，也没有配套的定价或收入信息。

telegram · zaihuapd · 11月26日 07:35

**「为什么是现在」** 变化点在于免费额度从“不能发”变成“可向已验证地址无限发”，让个人开发者做通知类小工具时省掉邮件服务商的月费和配额顾虑。时间窗口无法从现有材料判断，因为这是平台长期能力而非限时活动。

**「能不能做成产品」** 适合做面向个人或小团队的轻量通知工具：比如把 RSS、价格变动、网站监控、定时报表转成邮件推送给用户自己。MVP 就是 Workers + Cron + 邮件绑定，用户填自己的邮箱并完成验证，一两天能跑通。收费方式只能是订阅或一次性买断，但免费额度只覆盖“发给用户自己已验证的地址”，一旦要替用户群发就得走 Paid 计划，成本会转嫁到自己身上，所以纯靠这条能力做多租户群发产品不成立。

**「能不能接单」** 有间接服务空间：帮小团队把现有脚本、监控或报表接到 Workers 邮件通知上，交付物是部署和集成，按次收费。但这类需求目前没有从材料中看到明确来源（评论区、招聘、社群提问均无），只能算潜在需求，不宜当作确定订单来源。

**「钱在哪一边」** 公开材料未披露具体商业数据。唯一确定的经济信号是 Cloudflare 自己的分层：已验证地址免费不限量，任意收件人需 Paid 计划，说明平台把“群发”留作付费点。

**「风险」** 最大风险是能力边界被误读：免费只覆盖已验证地址，任何面向外部收件人的产品都要付 Workers Paid，且 Cloudflare 可随时调整配额或条款。另外邮件送达率、反垃圾策略不在开发者控制内。

**标签**: `#Cloudflare Workers`, `#邮件通知`, `#免费额度`, `#开发者工具`, `#生态更新`

---
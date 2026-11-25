---
layout: default
title: "Horizon Summary: 2026-11-25 (EN)"
date: 2026-11-25
lang: en
---

> From 39 items, 5 important content pieces were selected

---

**AI Opportunity Radar**
1. [LLM 能力拐点回顾](#item-ai-opportunity-1) ⭐️ 5.0/10
2. [OpenAI 押注网络安全](#item-ai-opportunity-2) ⭐️ 5.0/10
3. [OpenCode Go 补贴 Kimi 用量](#item-ai-opportunity-3) ⭐️ 5.0/10
4. [腾讯开源 Hy4 flash 量化权重](#item-ai-opportunity-4) ⭐️ 5.0/10
5. [Codex额度扣减被修正](#item-ai-opportunity-5) ⭐️ 5.0/10

---

## AI Opportunity Radar

<a id="item-ai-opportunity-1"></a>
### [LLM 能力拐点回顾](https://simonwillison.net/2026/Nov/24/llm-inflection-points/) ⭐️ 5.0/10

Simon Willison 于 2026 年 11 月 24 日发布的一篇主题演讲回顾文章，总结过去 12 个月 LLM 与编码 agent 的三次能力拐点：2025 年 11 月 Claude Opus 4.5 让编码 agent 首次默认给出可用结果；2026 年 6-7 月的 Fable 类模型（主动执行、自建工具链）；2026 年 9-10 月前沿模型在 3D 建模与游戏生成上的跃升。文中还提到 Fable 5 曾因美国出口管制被短暂下架、7 月 1 日恢复。这是个人观察与演讲整理，不是产品发布，未披露任何定价、收入或用户数据。

rss · Simon Willison · Nov 24, 23:02

**「为什么是现在」** 文章本身给出的时间依据是：Opus 4.5 发布满一周年，且 2026 年 9 月 22 日发布的 Opus 5.5 首次表现出对“好玩”的理解，作者据此认为游戏/3D 生成刚跨过可用门槛。但这是作者的个人判断，不是市场数据；窗口多长无法从现有材料判断。

**「能不能做成产品」** 可以尝试，但方向要窄。目标用户是做小游戏原型和 3D 素材的独立开发者、以及需要快速出 demo 的小团队；麻烦在于从想法到可玩原型之间反复调参耗时。MVP 可以是一个“提示词到可玩 Three.js/Blender 小游戏”的模板化生成器，内置玩法平衡与美术风格预设，按订阅或按次生成收费。两三人小团队做出可用版本的门槛不高，因为底层能力来自现成模型 API；真正的壁垒在玩法模板库和调优经验，而不是模型本身。若想做通用 3D 资产平台，则会被大厂模型直接覆盖，不建议。

**「能不能接单」** 有服务需求的迹象，但只在文章层面：作者提到在两场会议上看到别人展示的 AI 辅助游戏项目，以及独立游戏圈因 AI 辅助编程爆发争论。可推测的客户是独立游戏团队和小型工作室，交付物是原型开发、玩法调优、3D 素材管线搭建或团队培训。但材料中没有招聘信息、社群求助帖或付费记录，需求规模无法验证。

**「钱在哪一边」** 公开材料未披露具体商业数据。文章没有给出任何定价、收入、付费客户数或融资信息，只提到 GTA VI 被部分人称为“最后一个前生成式 AI 大作”这类舆论说法，属于社区观点而非商业证据。

**「风险」** 最直接的风险是模型厂商把“生成可玩游戏/3D 场景”做成免费内置功能，压缩中间层工具的生存空间；其次是模型 API 价格或可用性波动，文中 Fable 5 因出口管制被下架三天即是先例。

**Tags**: `#LLM能力拐点`, `#AI编码agent`, `#AI游戏/3D生成`, `#生态趋势`, `#无付费数据`

---

<a id="item-ai-opportunity-2"></a>
### [OpenAI 押注网络安全](https://www.theinformation.com/newsletters/ai-agenda/openais-roadmap-making-cyber-bigger-coding-remains-blurry) ⭐️ 5.0/10

OpenAI 将网络安全定位为下一个增长引擎，并称其规模可能超过编程业务。据 The Information 报道，公司已推出面向安全研究的 GPT-6 Cyber，并扩大名为 Daybreak 的“网络安全受信访问”计划；截至今年 9 月，该计划覆盖数千名经核验的防御者、约 2000 个获批组织与工作空间，支持漏洞发现、代码库分析和二进制逆向。文中唯一的具体数字——网络安全市场规模超过 3000 亿美元且被低估——来自 OpenAI CFO 的说法，约 2000 个组织也属官方口径，均无独立证据。报道本身指出，OpenAI 与 Anthropic、Google 的竞争格局以及规模化商业化的前景仍不清晰。

telegram · zaihuapd · Nov 25, 04:51

**「Why now」** OpenAI has moved from a general-purpose model to a dedicated security model line: GPT-6 Cyber was unveiled alongside the expanded Daybreak trusted-access program, and reporting describes an earlier GPT-5.5-Cyber \(June 2026\) that scored 57.3% on an internal Advanced Cybersecurity Completion Rate versus 95% for GPT-5.6-Cyber. That jump in task completion, plus Daybreak reaching roughly 2,000 approved organizations by September, is what makes security work newly automatable now. The window for third parties is unclear, though: access is gated behind OpenAI&\#x27;s trusted-access vetting, and the source itself says commercialization prospects against Anthropic and Google remain unclear.

**「能不能做成产品」** 直接做“AI 漏洞发现”平台做不成：模型能力、受信访问资格和合规资质都握在 OpenAI 一侧，个人开发者拿不到 Daybreak 级别的访问权限。间接路径存在但需验证：面向中小企业的代码库安全自查工具，用公开可用的模型 API 做依赖漏洞扫描、密钥泄露检测和修复建议，MVP 可以是一个接 GitHub 仓库、输出按严重度排序的问题清单的 SaaS 或 CLI。收费按仓库数订阅或按扫描次数计费，两三人团队约 2-3 个月可出可用版本。风险在于这类扫描器同质化严重，且大厂免费功能随时可能覆盖；付费意愿目前没有证据支撑。

**「能不能接单」** 有间接服务空间，但需求来源未经验证。可能的客户是需要通过安全审计或等保合规的中小企业和外包团队，交付物是代码审计报告、CI 流程里接入 AI 扫描的集成实施、或给开发团队做安全编码培训。现有材料没有显示这类需求从哪来——没有招聘信息、社群提问或评论区线索，因此只能算推测方向，接单前需要自己去找客户验证。

**「Market signal」** The only figure in the source is OpenAI&\#x27;s own claim: its CFO says the &gt;$300B cybersecurity market estimate is still far too low, and president Greg Brockman says security will become a bigger business for OpenAI than coding. No pricing, paying-customer count, or revenue for GPT-6 Cyber or Daybreak is disclosed; Daybreak&\#x27;s ~2,000 approved organizations as of September is an official figure, not independently verified. Third-party research firms put the AI-in-cybersecurity market at roughly $31–44B in 2025–2026 with 14–25% CAGR projections \(Grand View, Fortune Business Insights, Polaris\), an order of magnitude below OpenAI&\#x27;s framing — treat the $300B+ number as vendor positioning, not a measured market.

**「风险」** 最直接的风险是 OpenAI 自己把受信访问计划做成闭环产品，把漏洞发现和代码审计能力直接卖给企业，个人工具被免费或内置功能覆盖。其次是安全审计涉及责任问题：工具漏报导致客户被攻破时，小团队难以承担赔付和合规责任。

<details><summary>References</summary>
<ul>
<li><a href="https://thehackernews.com/2026/11/openai-launches-gpt-6-cyber-after-ai.html">OpenAI Launches GPT - 6 Cyber After AI Helps Find 81 Firefox Flaws...</a></li>
<li><a href="https://theintelligent.us/technology/2026/openai-expands-daybreak-cybersecurity-program-specialized-gpt-56-cyber-model">OpenAI expands Daybreak cybersecurity program with specialized...</a></li>
<li><a href="https://neomanex.com/news/gpt-5-6-cyber-daybreak-blue-red">GPT -5. 6 - Cyber : Fewer Refusals, Days After Astra Pause | Neomanex</a></li>
<li><a href="https://www.grandviewresearch.com/industry-analysis/artificial-intelligence-cybersecurity-market-report">AI in Cybersecurity Market Size &amp; Share Report, 2026-2033</a></li>
<li><a href="https://www.fortunebusinessinsights.com/artificial-intelligence-in-cybersecurity-market-113125">Artificial Intelligence in Cybersecurity Market Size, Share ... AI Cybersecurity Market Size, Forecast, Opportunities, 2034 Cybersecurity Spending and AI Threat Trends for 2026 | BCG AI in Cybersecurity Market Size, Share, Forecast ... - Polaris Global AI Cybersecurity Market Size and Forecast, 2026-2031 ... AI Cybersecurity Market Size, Share &amp; Forecast 2026-2034</a></li>
<li><a href="https://semiconductorinsight.com/report/ai-cybersecurity-market/">AI Cybersecurity Market Size, Forecast, Opportunities, 2034</a></li>

</ul>
</details>

**Tags**: `#AI安全`, `#OpenAI生态`, `#平台战略`, `#间接机会`, `#付费意愿未验证`

---

<a id="item-ai-opportunity-3"></a>
### [OpenCode Go 补贴 Kimi 用量](https://x.com/opencode/status/2125413495629926551) ⭐️ 5.0/10

OpenCode 在 X 平台发布“Gimme Kimi Phase 1”活动，面向所有 OpenCode Go 订阅用户：支付 10 美元可获得价值 60 美元的 Kimi K3.1 Pro 用量。这是平台侧的获客与用量补贴，不是新产品发布。活动预算、名额上限、结束时间以及“Phase 1”之后是否延续，公开材料均未披露；目前唯一证据是 OpenCode 官方 X 帖的宣称，没有独立可查数据。

telegram · zaihuapd · Nov 25, 06:29

**「Why now」** The offer is tied to Kimi K 3.1 Pro having just gone live with upgraded coding and agentic capabilities, which is what makes a subsidized coding-model quota worth promoting at this moment. OpenCode&\#x27;s own console lists Go at $15 and Go Plus at $60, and states Go works with OpenCode plus other coding agents \(Claude Code, Codex, Hermes, Pi validated\) that send a session ID and their own user agent — so the subsidy is aimed at pulling typical coding-agent traffic onto OpenCode&\#x27;s plan. The post labels this &quot;Phase 1,&quot; implying further phases, but no end date, budget, or quota cap is disclosed, so the actual window length cannot be determined from available material.

**「能不能做成产品」** 做不成独立产品。这条本身是别人家的补贴，付费方是 OpenCode 而非终端用户，没有可复制的收费模式。对个人开发者唯一实际用途是把它当廉价算力窗口：用 10 美元额度跑 Kimi K3.1 Pro 做原型验证、批量评测或 prompt 调优，把试错成本压到原来的六分之一左右。但补贴额度不可转售、不可依赖，不能作为任何产品的成本结构基础——一旦活动结束，按原价计费的产品模型可能直接不成立。

**「能不能接单」** 没有服务需求迹象。评论区无实质内容，也没有客户在问“怎么用这个额度”或“帮我搭 OpenCode 工作流”。理论上可以给已订阅 OpenCode Go 的小团队做 Kimi K3.1 Pro 的接入与 prompt 调优，但需求来源不明，且客户省下的钱有限，付不起像样的服务费。不建议围绕这条去拓客。

**「Money side」** The payer here is OpenCode, not an end customer: it subsidizes Kimi K3.1 Pro usage for its own Go subscribers, so the $10-for-$60 offer is a customer-acquisition cost rather than a market signal for a third-party product. For context on the underlying economics, a third-party pricing writeup lists Kimi K3.1 Pro at $2/$10 per million tokens \(down from K3&\#x27;s $3/$15\), and OpenCode&\#x27;s own console lists Go at $15/month and Go Plus at $60/month. The campaign&\#x27;s budget, duration, and seat cap are not disclosed; the only evidence is OpenCode&\#x27;s own X post, with no independent confirmation of uptake or spend.

**「风险」** 最大风险是把补贴价当成长期成本来设计产品：活动随时可能结束或缩量，届时毛利直接转负。另外额度通常绑定账号，转售或批量套利大概率违反平台条款，存在封号风险。

<details><summary>References</summary>
<ul>
<li><a href="https://opencode.ai/console/go">Go | OpenCode Console</a></li>
<li><a href="https://www.kimi.ai/">Kimi AI Official Site | K 3 . 1 Pro Launches with Upgraded Coding...</a></li>
<li><a href="https://threatfrontier.com/articles/kimi-k3-1-pro-pricing-api-membership-vs-claude-chatgpt">Kimi K 3 . 1 Pro Pricing : $2/$10 API and Membership Plans</a></li>
<li><a href="https://openchamber.dev/blog/opencode-go/">OpenCode Go (Nov 2026): Plans, Models, Limits, Real Usage</a></li>
<li><a href="https://opencode.ai/console/go">Go | OpenCode Console</a></li>

</ul>
</details>

**Tags**: `#生态促销`, `#模型用量补贴`, `#成本优化`, `#间接机会`, `#证据有限`

---

<a id="item-ai-opportunity-4"></a>
### [腾讯开源 Hy4 flash 量化权重](https://mp.weixin.qq.com/s/o0xxShVQX6g2UllrrEv1WQ) ⭐️ 5.0/10

腾讯混元通过其模型压缩加速工具箱 AngelSlim 开源了 224B 参数模型 Hy4 flash 的 GGUF 量化权重。原始权重约 410.27GiB，最小的 IQ2-AH 版本为 125.73GiB，约为原版的 30%；配合 Strata offload 框架，官方称可在 64 GB Mac mini 上运行。来源给出的性能数据为：48 GB 显存设备在 10K 上下文下每秒生成 89 个 token，M5 Max 128 GB 上 Q3\_K 版本在 32K 上下文下每秒 47 个 token；DeepSWE v1.1 等评测中 Q3\_K 与原模型得分差距不超过 0.4 分。这些均为发布方口径，未见独立复现。

telegram · zaihuapd · Nov 25, 09:29

**「Why now」** The timing hinges on a concrete release: Tencent Hunyuan open-sourced Hy4 flash GGUF quantized weights and matching inference code through its AngelSlim compression toolkit on November 25, 2026, per IT之家. The smallest IQ2-AH build is about 125.73GiB versus roughly 410.27GiB for the original, and with the Strata offload framework it can run on a 64GB Mac mini — so the change is that a 224B-class model now fits on consumer hardware that individual developers and small studios already own. How long this window stays open cannot be judged from the available material; no pricing, licensing terms beyond &quot;open source,&quot; or adoption data were disclosed.

**「能不能做成产品」** 能做的空间偏窄。可想到的形态是面向不想碰命令行的 Mac 用户做一层本地推理封装：一键下载权重、管理 Strata offload 配置、按机器内存自动选量化档位、暴露 OpenAI 兼容接口，收费走一次性买断或低价订阅。但核心价值（权重、量化工具、offload 框架）全部由腾讯免费提供，封装层可替代性强，且 125.73GiB 的下载与磁盘占用会筛掉大部分个人用户，真正愿意付费的只剩少数有本地隐私推理需求的团队。两三人小团队做 MVP 大约数周，但付费转化需要自行验证，材料中没有任何付费意愿证据。

**「能不能接单」** 有服务需求的迹象很弱。理论上可接的单是帮中小企业在内网或 Mac 工作站上部署这套量化模型、调优 offload 参数、做私有化推理集成与培训，交付物为部署脚本、配置文档和一次性调优。但材料中没有出现招聘、社群提问或客户询价等需求信号，这条路径目前只能算推测，不宜当作已成立的市场。

**「Money side」** The source discloses no pricing, revenue, paid-customer counts, or licensing terms for the Hy4 flash GGUF weights or the Strata offload framework; all performance figures \(89 tok/s on 48 GB VRAM at 10K context, 47 tok/s on M5 Max 128 GB at 32K context\) are vendor-published benchmarks, not commercial data. The only adjacent commercial signal in the tool results is third-party tutorial and实战 content around Strata \(CSDN posts on running 176B and 125B models on consumer hardware, a Zhihu Mac deployment walkthrough\), which indicates practitioner interest in offload tooling but carries no pricing or purchase evidence. Whether anyone pays for this specifically is unverified from public material.

**「风险」** 最大风险是这本质上是厂商免费开源的能力更新：一旦官方或社区推出更易用的 Mac 一键运行方案，封装层的价值会被迅速抹平。此外 125.73GiB 的最小权重对 64 GB 机器的实际可用性依赖 offload 到磁盘，速度与体验是否达到宣传水平缺少独立验证。

<details><summary>References</summary>
<ul>
<li><a href="https://www.ithome.com/1/032/131.htm">让大模型跑在个人设备上， 腾 讯 混 元 开 源 Hy 4 flash GGUF ...</a></li>
<li><a href="https://blog.csdn.net/zhshilu/article/details/170775177">16GB 显卡跑 176B 大模型：64GB 内存本地部署实战（Strata + Claude C...</a></li>
<li><a href="https://blog.csdn.net/weixin_29058331/article/details/169199452">游戏本跑1250亿参数大模型：Strata推理引擎offload实战-CSDN博客</a></li>
<li><a href="https://zhuanlan.zhihu.com/p/2094138366560420919">在 Mac 上部署 Strata + Qwen3.8-Flash-Next：新手教程</a></li>

</ul>
</details>

**Tags**: `#开源模型`, `#模型量化`, `#本地推理`, `#生态信息`, `#变现路径不清晰`

---

<a id="item-ai-opportunity-5"></a>
### [Codex额度扣减被修正](https://x.com/CodexUpdate/status/2125427689460785413) ⭐️ 5.0/10

OpenAI于11月25日向部分Codex用户发邮件，称此前GPT-6.2 Astra和Sol的部分请求（含Ultrafast模式）额度扣减低于预期，现已更正，用户可能更快触达使用上限，但未披露具体收紧幅度。订阅价格不变，用户可在Settings → Usage查看剩余额度与重置时间。GPT-6.2 Astra和Sol于11月17日上线ChatGPT Work、Codex和API，Codex与Work共享额度。信息来自Codex Update的推文及科技圈茶馆转发，OpenAI官方公告细节未在材料中给出。

telegram · zaihuapd · Nov 25, 10:22

**「为何是现在」** 变化点是11月17日上线的GPT-6.2 Astra/Sol在Codex中的计费口径被重新校准，11月25日起用户实际可用额度缩水而价格不变，成本压力从“隐性”变成“显性”。时间窗口无法从现有材料判断，因为材料未给出收紧比例、影响用户规模或后续是否继续调整。

**「产品角度」** 目标用户是靠Codex/Work额度干活的重度开发者与小团队，麻烦是额度消耗不透明、突然更快用完、无法预判何时触顶。MVP可以是一个本地或轻量托管的用量看板：读取用户手动导出的Usage数据或通过API用量接口，按模型（Astra/Sol/Ultrafast）拆分消耗、预测触顶时间、在接近上限时提醒，并给出降级到更省额度模型的建议。收费可用订阅（月付几美元）或一次性买断脚本。两三人小团队约2-4周可做出可用版本。风险在于OpenAI未公开扣减规则，预测只能基于历史用量拟合，准确性有限；若官方后续在Settings里补齐用量分析，产品价值会被压缩。

**「服务角度」** 可能买单的是已把Codex嵌入工作流的小型团队，交付物是额度审计与成本优化咨询：帮客户盘点哪些任务在烧Ultrafast额度、改写成更省的调用方式、设置团队内用量规范。需求来源目前只有这条政策更新本身，材料中没有招聘、社群提问或客户询价的迹象，因此服务需求是否真实存在尚未验证。

**「市场信号」** 公开材料未披露具体商业数据：没有受影响用户数、额度收紧比例、相关工具的收入或付费客户数。唯一确定的商业事实是订阅价格不变，即用户为相同价格获得更少可用额度。

**「风险」** 最直接的风险是OpenAI自己在Settings → Usage中补齐用量分析与预测功能，免费覆盖这类小工具的核心价值；其次是扣减规则不公开且可能再次调整，使依赖拟合的预测工具频繁失准。

**Tags**: `#OpenAI Codex`, `#额度政策`, `#成本优化`, `#开发者工具`, `#生态信息`

---
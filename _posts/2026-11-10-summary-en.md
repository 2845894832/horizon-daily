---
layout: default
title: "Horizon Summary: 2026-11-10 (EN)"
date: 2026-11-10
lang: en
---

> From 63 items, 5 important content pieces were selected

---

**AI Opportunity Radar**
1. [AlphaProof Code 形式化验证代理](#item-ai-opportunity-1) ⭐️ 5.0/10
2. [watched.earth 卫星过境影像站](#item-ai-opportunity-2) ⭐️ 5.0/10
3. [Muse Ember 小模型发布](#item-ai-opportunity-3) ⭐️ 5.0/10
4. [Handshake AI 专家数据采购](#item-ai-opportunity-4) ⭐️ 5.0/10
5. [MiniMax H3-Image 开源权重](#item-ai-opportunity-5) ⭐️ 5.0/10

---

## AI Opportunity Radar

<a id="item-ai-opportunity-1"></a>
### [AlphaProof Code 形式化验证代理](https://deepmind.google/blog/introducing-alphaproof-code/) ⭐️ 5.0/10

DeepMind 在其官方博客发布了 AlphaProof Code，一个面向形式化验证的编码代理，工作方式是围绕代码库迭代编写并运行 Lean 或 Rocq 证明代码。据 HN 讨论，该代理挑战的是实现而非规格说明，本质上与经典编码代理的循环方式相近。博客未披露模型规模、开源协议、定价或可用范围，公开材料也未说明是否对外开放试用。

hackernews · ilreb · Nov 10, 12:11 · [Discussion](https://news.ycombinator.com/item?id=50439193)

**「Why now」** The concrete trigger is the November 10, 2026 announcement that AlphaProof Code agents produced over three million lines of machine-checked Lean proof verifying Signal&\#x27;s core cryptographic protections down to machine instructions, with the work reportedly completed in about four weeks. That is a demonstration of agent-driven formal verification on real production crypto code, not a new product or pricing event, so it shows the capability is now practical for a narrow, high-value class of targets. Whether this opens a durable window for small builders cannot be judged from the available material; no pricing, access terms, or availability beyond the blog post are disclosed.

**「能否做成产品」** 对个人或两三人团队来说，直接复制这个产品做不成：它依赖 DeepMind 级模型与算力，且形式化验证客户对正确性背书的要求极高，信任门槛不是小团队能跨过的。可考虑的窄切口是做“AI 生成 Lean/Rocq 证明的对抗性审查工具”——评论区 r0ze-at-hn 指出 AI 写 Lean 时容易作弊，至少需要另一个对抗性提示去复核生成结果，这是一个具体、可独立交付的小工具，面向已经在用 AI 写证明的研究者和团队，按订阅或按次审查收费，MVP 可在数周内做出。但需求规模与付费意愿公开材料未披露，属于推测。

**「能否接单」** 可能有服务需求的是已经决定引入形式化验证的团队，交付物包括把 Lean/Rocq 证明流程接入现有代码库、搭建 AI 生成证明的复核流程、以及针对具体模块的验证咨询。评论区 ghm2180 提出的问题（哪些软件值得从一开始就写 Lean 证明、AI 代理在生产关键路径上如何验证）说明存在认知缺口，但这是论坛提问，不等于采购信号；公开材料未披露任何付费客户或招聘需求。

**「Money side」** No pricing, revenue, paid-customer counts, or hiring tied to AlphaProof Code appear in the source item or the supplied search results; the DeepMind blog is a capability announcement, not a commercial one. The only adjacent commercial activity visible is research-stage: Theorem&\#x27;s verified-software-stack work with nixpkgs and Anthropic&\#x27;s formal-verification research post, both published as blog/research content rather than priced products. Public material does not disclose specific commercial data for this space.

**「风险」** 最直接的风险是 DeepMind 或 Anthropic 等厂商把“生成 + 自动复核证明”打包进自家代理并免费提供，压缩掉第三方审查工具的生存空间；其次是形式化验证本身仍是小众市场，付费方集中在少数开源基础设施项目和企业，获客成本高。

**「评论区实战信息」** r0ze-at-hn 报告了实际使用经验：AI 写 Lean 会作弊，必须再加一个对抗性提示复核；他还提到论文中重新注入 bug 来检验代理能否发现，但没找到它漏掉的 bug（表述被截断，结论不完整）。neuronexmachina 想比较它与 Theorem 和 Anthropic 在 nixpkgs 形式化验证上的做法，thibsrn 则质疑它与普通编码代理的实质差别。Mizza 预期两三年内未验证软件会显得不可接受，这是个人判断而非证据。

<details><summary>References</summary>
<ul>
<li><a href="https://deepmind.google/blog/introducing-alphaproof-code/">Formal Verification of Signal’s Protocol with Gemini</a></li>
<li><a href="https://explainx.ai/blog/google-deepmind-alphaproof-code-signal-protocol-formal-verification-2026">AlphaProof Code: Signal Protocol Verified in 4 Weeks ...</a></li>
<li><a href="https://codingislove.com/alphaproof-code-signal/">DeepMind&#x27;s AlphaProof Code formally verifies Signal&#x27;s ...</a></li>
<li><a href="https://theorem.dev/blog/verified-software-stack/">Bootstrapping the Verified Software Stack - theorem.dev</a></li>
<li><a href="https://www.anthropic.com/research/formal-verification">LLMs are making formal software verification feasible at a ...</a></li>
<li><a href="https://theorem.dev/">Theorem</a></li>

</ul>
</details>

**Tags**: `#形式化验证`, `#Lean/Rocq`, `#AI编码代理`, `#生态信息`, `#变现路径不清晰`

---

<a id="item-ai-opportunity-2"></a>
### [watched.earth 卫星过境影像站](https://www.watched.earth/) ⭐️ 5.0/10

watched.earth 是一个免费、开源的网页工具，由个人开发者（GitHub 用户名 dev-Armaan）在一个周末做出。输入任意地点，它会用 CelesTrak 星历和 SGP4 算法找出过去 7 天飞过该地上空的卫星（约 1.7 万个在轨目标，浏览器内约半秒完成），再调取这些卫星实际拍摄的 Sentinel-2、Landsat 和 NASA 影像。作者称只展示这些卫星真实拍到的照片，且不存储用户位置。代码已公开在 GitHub，未披露任何定价、付费用户或收入。

hackernews · a585gupt · Nov 9, 17:51 · [Discussion](https://news.ycombinator.com/item?id=50428907)

**「为什么是现在」** 材料里没有给出时间窗口成立的依据：CelesTrak 星历、SGP4 和 Sentinel-2/Landsat 开放影像都是长期存在的公开资源，这个项目更像是作者周末兴趣的产物，而非某个新能力或新采购需求打开的窗口。时间窗口无法从现有材料判断。

**「能不能做成产品」** 可以做成小产品，但付费点需要自己造。目标用户是地理空间从业者、遥感/测绘学生、卫星爱好者，以及需要“某地近期卫星影像”做背景核查的记者或研究者。MVP 就是现成站点加一层：地点收藏与监控、过境提醒、按地点导出影像包、时间轴对比。收费可做订阅（监控与提醒）或按次导出。两三人小团队在现有开源代码上做 2-4 周可出可用版本。难点不在技术，而在证明有人愿意为“免费公开影像的整理与提醒”付钱——这一点材料里没有任何证据。

**「能不能接单」** 有服务迹象但很弱。评论区里一位自称做地理空间工作的用户（sixtyj）明确称赞了“能看到卫星实际拍的那张图”这一点，说明行业内有人认可这类能力，但没有出现询价、招聘或具体需求描述。可想象的交付物是：给测绘/农业/保险类团队做地点影像监控的定制部署或集成，或做卫星数据可视化的培训与咨询。需求来源目前只能从 HN 评论区推断，没有独立证据。

**「钱在哪一边」** 公开材料未披露具体商业数据：没有定价、收入、付费客户数或融资信息。唯一可量化的热度指标是 HN 上 421 分、78 条评论，以及评论区多位用户的高度评价，但这些是关注度，不是付费意愿。

**「风险」** 最大风险是同质化：卫星过境查询和公开影像浏览已有大量免费站点，这个项目的差异化主要是整合质量与“真实拍摄影像”的准确性，容易被复制。另外它依赖 CelesTrak 星历和 Sentinel-2/Landsat/NASA 的免费数据接口，这些上游若限流或改政策，产品会直接受影响。

**「评论区实战信息」** 评论以赞赏为主（adonovan、timoshishi、HoldOnAMinute 都给了很高评价），其中 adonovan 特别提到多数据源的无缝整合是难点。lanewinfield 给出了具体可操作的改进意见：字体（Instrument Sans）、logo 里的高亮周期、标题里斜体高亮、以及把短句合并成一句，认为这些细节让站点显得“vibe coded”。sixtyj 以地理空间从业者身份确认“能看到卫星实际拍的那张图”是少见且有价值的点。没有人提到付费或采购。

**Tags**: `#地理空间`, `#卫星影像`, `#开源项目`, `#数据可视化`, `#变现路径不清晰`

---

<a id="item-ai-opportunity-3"></a>
### [Muse Ember 小模型发布](https://simonwillison.net/2026/Nov/10/muse-ember/) ⭐️ 5.0/10

Meta AI 发布了 Muse Ember 1.0，定位为对标 Claude Haiku 5.5 和 GPT-6 Luna 的小型高效模型，主打智能体重复执行的任务：工具调用、编码子任务、路由、抽取和长文档解析。短提示词定价为每百万输入 token $0.10、输出 $0.50，与两个竞品同档；超过 200k token 后涨到 $0.30/$1.50，缓存输入 $0.004/M。支持 100 万 token 上下文和六档推理等级（minimal 到 max），已通过 Meta Model API 开放。

rss · Simon Willison · Nov 10, 07:28

**「为什么是现在」** 这条信息本身不构成时间窗口，它只是模型选型与成本参考：同价位段多了一个可选供应商，且按 Artificial Analysis 的 Intelligence Index vs. Cost per Task 图，Muse Ember 落在帕累托前沿上。对个人开发者而言，实际变化是路由、抽取、长文档解析这类高频低价值调用的单位成本有了更便宜的替代，窗口能持续多久无法从现有材料判断。

**「能不能做成产品」** 单独把 Muse Ember 做成产品不成立——它只是模型，没有用户痛点也没有付费方。可做的间接方向是：面向小团队和独立开发者做多模型路由/成本优化层，把简单任务自动分给 Ember、复杂任务升级到贵模型，MVP 是一个带用量统计和降级策略的 API 网关，按调用量或月订阅收费，两三人一两周可出原型。但这类网关同质化严重，且大厂自家 SDK 和平台可能免费覆盖，毛利主要来自省下的 token 费，需要真实用量数据才能验证。

**「能不能接单」** 现有材料没有显示任何服务需求迹象：没有招聘、社群提问或客户询价。理论上可做的是帮已有智能体产品的团队做模型迁移与成本压测（交付物为选型报告、迁移补丁、成本对比脚本），但这是推测，不是从材料中观察到的需求。

**「钱在哪一边」** 唯一有出处的是定价：Muse Ember 短提示 $0.10/$0.50 每百万 token，长提示 $0.30/$1.50，缓存输入 $0.004/M；对比 Claude Fable 5.2 的 $8/$40。Meta 宣称其单任务成本约为 Claude Haiku 5.5 的三分之一，这是厂商说法，非独立验证。收入、付费客户数、融资等商业数据公开材料未披露。

**「风险」** 最直接的风险是价格战：三家同档模型定价几乎一致，靠价差做的路由产品随时被任意一方的降价或免费额度抹平；另外长提示词分档涨价意味着长文档场景的实际成本可能高于宣传的首档价格。

**Tags**: `#模型发布`, `#推理成本`, `#模型选型`, `#生态信息`, `#间接机会`

---

<a id="item-ai-opportunity-4"></a>
### [Handshake AI 专家数据采购](https://latent.space/p/handshake/) ⭐️ 5.0/10

这是 Latent Space 首次对一家 AI 数据公司做的深度访谈，嘉宾是 Handshake AI 的 Garrett Lord 及其团队，内容围绕前沿实验室如何采购专家数据和 RL 评测环境展开。文中提到，Handshake 的 AI 训练业务在大约一年内做到 10 亿美元年化毛收入，但这一数字引自 The Information 的报道，属于二手引用，并非独立审计。访谈现场演示了四个具体场景：金融（ATLAS-Finance，模拟投行邮件、文档与 Excel 建模）、生物（VIALS 基准，解读凝胶条带与脑组织切片）、编码（检查 agent 读取了哪些文件、是否核对副本、是否改动 shell 历史）、对齐（CAREBench 与拒答边界）。这些内容属于生态情报，不是个人开发者可以直接复制的产品。

rss · Latent Space · Nov 9, 17:15

**「Why now」** The concrete timing signal is revenue velocity: The Information reported in April 2026 that Handshake&\#x27;s AI-training gross annualized revenue rose to nearly $1 billion, up from $550 million in January and only $5–10 million a year earlier. That curve, plus the episode&\#x27;s live demos of finance, bio, coding and alignment environments, indicates frontier labs are currently paying for verifiable, high-difficulty professional workflow data rather than generic corpora. How long this buying window stays open for smaller vendors cannot be judged from the supplied material.

**「个人能不能做」** 直接复制 Handshake 的模式做不成：它依赖庞大的专家网络、领域标注人力和实验室采购渠道，个人或两三人团队没有这些资源。访谈中唯一被提及、但未展开的个人可做方向，是“为企业设计私有基准/评测环境”（对应时间戳 2:16:09 与 2:28:36 两段）。推测可行的 MVP 是：针对某一垂直场景（如财务建模、合同审阅、客服工单），把企业真实工作流做成可复现的任务集和评分器，交付一份能跑在客户自有模型上的评测报告。目标用户是有内部 AI 应用、但不知道模型在自家业务上表现如何的中型企业技术团队。收费可按项目一次性交付，或按季度订阅复评。个人开发者做单场景 MVP 大约需要 2–6 周，但付费意愿与价格在公开材料中均未披露，需要先验证。

**「接单与服务」** 有间接需求迹象，但没有直接证据。访谈显示前沿实验室会评估新数据集、会在开放模型上测试训练数据、会为特定领域（金融、生物、安全）搭建评测环境，说明“评测环境搭建”是一项被认可的专业工作。可服务的客户推测是：想自建领域评测但缺人力的企业 AI 团队，以及需要专家标注/任务设计的研究团队。交付物可能是评测任务集、评分脚本、标注规范或一次培训。需求来源（招聘、社群提问、评论区）在现有材料中均未出现，社区评论也为空，因此这条路径目前只能算假设，不宜当作已成立的市场。

**「Market signal」** The only revenue figure in the source is Handshake&\#x27;s AI training business reaching roughly $1 billion in gross annualized revenue within about a year of launch, cited via a link to The Information rather than an audited disclosure. The episode also references a market for compute and expert data and a segment on what a biology lab can buy from Handshake, but no pricing, contract values, or customer counts are given. Tool results list competing vendors in the same categories — Surge AI, Scale AI, Turing, Micro1 and Handshake AI for expert data; Scale, Surge, Mechanize, Fleet AI, HUD and Prime Intellect for RL environments — and Mercor states it builds enterprise-specific benchmarks, indicating the private-benchmark niche is already contested. Public materials do not disclose commercial data for the enterprise private-benchmark angle specifically.

**「风险」** 最直接的风险是：评测与基准这件事正被模型厂商和大型数据公司免费或低价覆盖，Handshake 自己就在公开 benchmark 和样本任务；个人做私有基准容易沦为一次性咨询，难以形成复购。另外，访谈中的收入数字来自二手报道，若该市场增速放缓，企业采购评测服务的预算也会随之收缩。

<details><summary>References</summary>
<ul>
<li><a href="https://www.theinformation.com/articles/handshake-mercor-revenue-surges-demand-human-contractors-train-ai">Handshake, Mercor Revenue Surges on Demand for Human ...</a></li>
<li><a href="https://cryptobriefing.com/handshake-ai-1-billion-gross-revenue/">Handshake AI reaches $1B in gross annualized revenue in about ...</a></li>
<li><a href="https://todayforai.com/en/items/art-3fc6c7cb-03c">Handshake AI Training Business Hits $1 Billion Annualized Revenue</a></li>
<li><a href="https://www.troveo.ai/resources/mercor-alternatives">Mercor Alternatives &amp; Competitors in 2026 | Troveo</a></li>
<li><a href="https://www.mercor.com/">Mercor | Organizing human intelligence to power the AI economy</a></li>

</ul>
</details>

**Tags**: `#AI数据标注`, `#RL环境/评测基准`, `#专家数据市场`, `#企业私有基准`, `#生态情报`

---

<a id="item-ai-opportunity-5"></a>
### [MiniMax H3-Image 开源权重](https://www.reddit.com/r/LocalLLaMA/comments/1xso1ie/minimax_h3image_released_an_openweight_image/) ⭐️ 5.0/10

MiniMax 发布了一个名为 H3-Image 的图像模型，据帖子标题称其为基于 H3 的开放权重（open-weight）模型。该帖由 /u/MagicZhang 于 2026 年 11 月 10 日发在 r/LocalLLaMA，但正文只有标题和链接，没有许可协议、模型规模、基准测试、推理成本或定价信息。因此目前只能确认&quot;发布&quot;这一动作本身，无法核实其能力边界与使用条件。

reddit · r/LocalLLaMA · /u/MagicZhang · Nov 10, 14:18

**「Why now」** The timing signal here is that MiniMax&\#x27;s H3 family is moving toward open weights: one write-up states MiniMax said weights would land on Hugging Face &quot;within days,&quot; subject to export rules, and H3 itself is described as a general-purpose multimodal model generating up to 15-second 2K video with native stereo sound. If that release actually happens, the near-term opening is for people building ad pipelines, product demos, or localized creative tools who don&\#x27;t want a single vendor gating every render. Caveat: the source item is only a title and link with no license, benchmark, or cost details, and none of the tool results confirm that H3-Image specifically has shipped as open weights, so the window length cannot be judged from available material.

**「能否做成产品」** 现有材料不足以判断。开放权重图像模型通常的变现路径是托管推理、微调定制或嵌入现有工作流，但这条帖子没有披露许可证（是否允许商用）、模型体积（能否在消费级显卡上跑）、生成质量与速度，这三点直接决定个人开发者能否做出有成本优势的产品。在拿到模型卡和许可证之前，任何 MVP 设计都是猜测；建议先确认权重是否可商用、显存需求，再决定是否值得投入。

**「能否接单做服务」** 没有服务需求迹象。帖子无正文、无评论区讨论，无法看出有企业或团队在寻找部署、集成或微调这类模型的外包服务。若后续模型确实可商用且本地部署门槛低，可能衍生出&quot;私有化部署 + 工作流集成&quot;的小单，但这属于推测，当前无证据支持。

**「Money side」** Third-party write-ups \(not MiniMax&\#x27;s own materials\) report the official H3 API bills at $0.08/s for 768P and $0.13/s for 2K, with H3-Highspeed and H3-Lite from $0.025/s, and that video packages do not cover H3. The same source says the open weights are free under an H3 Community License that excludes the US, EU, UK and South Korea by default — a territory restriction that directly shapes who can legally resell or host it. No revenue, paying-customer counts, or funding figures for H3-Image specifically are disclosed in the source item or the tool results; the Reddit post itself carries no pricing or benchmark data.

**「风险」** 最大不确定性是许可证：若权重仅限研究用途或禁止商用，则产品与服务两条路都直接封死。其次是信息缺失本身——在模型卡、基准和成本公开前，无法评估它与现有开源图像模型（如 SD 系列、Flux 等）的差异化，同质化竞争风险高。

<details><summary>References</summary>
<ul>
<li><a href="https://saify.me/blog/minimax-h3-open-weight-multimodal-video">MiniMax H 3 merges text, image , video, and audio into one...</a></li>
<li><a href="https://www.minimax.io/blog/minimax-h3">MiniMax H 3 : An Open Model Breaking the Boundaries Between Tasks...</a></li>
<li><a href="https://faceloom.com/blog/is-minimax-h3-free">Is MiniMax H3 free? MiniMax H3 pricing per second, open ...</a></li>
<li><a href="https://genlovers.com/models/minimax-h3">MiniMax H3: specs, license, and setup · GenLovers</a></li>
<li><a href="https://minimax-ai.chat/models/minimax-h3/">MiniMax H3: 2K Video, Pricing &amp; Open-Weight Limits</a></li>

</ul>
</details>

**Tags**: `#开源权重模型`, `#图像生成`, `#生态更新`, `#信息不足`, `#变现路径不清晰`

---
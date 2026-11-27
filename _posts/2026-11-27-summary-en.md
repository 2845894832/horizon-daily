---
layout: default
title: "Horizon Summary: 2026-11-27 (EN)"
date: 2026-11-27
lang: en
---

> From 39 items, 3 important content pieces were selected

---

**AI Opportunity Radar**
1. [G2i 训练数据生意](#item-ai-opportunity-1) ⭐️ 6.0/10
2. [Clay 的 GTM Agent 经验](#item-ai-opportunity-2) ⭐️ 5.0/10
3. [豆包工作接入剪映插件](#item-ai-opportunity-3) ⭐️ 5.0/10

---

## AI Opportunity Radar

<a id="item-ai-opportunity-1"></a>
### [G2i 训练数据生意](https://latent.space/p/inside_the_ai_training_data_market_gabe_greenberg_g2i/) ⭐️ 6.0/10

这是 Latent.Space 的一期播客，在 AI Engineer CODE 2026 现场录制，嘉宾是 G2i 创始人 Gabe Greenberg，主持人是 swyx。G2i 的业务是用资深工程师为前沿实验室构建 AI 训练数据和强化学习环境。播客里讲的是实验室怎么采购：任务难度要略高于模型当前能力，由资深工程师设计任务、挑选种子数据、写能打分的验证器；实验室可以加价买独家数据，也可以拿折扣买非独家数据；小规模试点订单会逐步变成更大的合作。节目由 G2i 联合主办并赞助，属于厂商参与的对话，不是独立调查。

rss · Latent Space · Nov 27, 22:19

**「Why now」** The window is defined by a shift in what labs buy: per the episode, demand has moved from human labels toward expert engineering tasks, seed data, and verifiers, and Gabe describes small pilot orders that grow into larger engagements. External vendor pages from 2026 describe the same pivot — Troveo&\#x27;s comparison notes that growth now comes from AI lab services such as training data, evaluations, and post-training work, while micro1 markets frontier evaluations and RL environments and Mercor&\#x27;s founder frames expert-generated data as the bottleneck. That said, the source gives no dates, volumes, or pricing, so how long this window stays open cannot be judged from the available material.

**「能不能做成产品」** 直接复制 G2i 的模式对个人开发者基本做不成：核心资产是能通过实验室筛选的资深工程师池、与实验室采购方的信任关系，以及任务和验证器的质量口碑，这些都不是两三个人几个月能搭起来的。相对可行的间接方向是给数据运营方做工具，比如任务难度校准、验证器编写与回归测试、种子数据版本管理、交付物质检流水线，目标用户是像 G2i 这样的数据供应商和实验室内部的数据团队。MVP 可以是一个验证器测试框架：给定一批任务和评分脚本，自动跑回归、标出评分不稳定或可被钻空子的用例。收费按订阅或按席位，个人开发者大约 2–4 个月能做出可用版本。但这条路的付费方数量很少，且采购决策慢，公开材料没有披露这类工具是否已有人付费。

**「能不能接单」** 有服务需求的迹象，但门槛在供给侧。播客提到 G2i 要筛选工程师做 agentic 工作，说明市场缺的是能设计高难度任务并写验证器的资深工程师，而不是普通标注人力。可能的客户是数据供应商和实验室的数据团队，交付物是任务设计、验证器实现、种子数据整理或工程师筛选流程咨询。需求来源在材料里只体现为 G2i 自身的招聘与筛选环节，没有评论区、招聘帖或社群提问作为独立佐证，因此这类外包需求的实际规模无法从现有材料判断。

**「Market signal」** The episode gives no concrete commercial figures: no pricing, revenue, customer counts, or contract sizes are disclosed, and the host notes only that labs choose between paying more for exclusive data and taking a discount on non-exclusive data. The only verifiable commercial fact is that G2i co-organized and sponsored AI Engineer CODE 2026, which is a marketing relationship rather than evidence of demand. External context confirms a crowded vendor field — AfterQuery markets itself as &quot;powering every frontier AI research lab&quot; and Toloka sells training data for agents and LLMs — but these are vendor self-descriptions, not independent proof of spend. Whether labs pay enough for a small team to enter is not established by the supplied material.

**「风险」** 最直接的风险是实验室把数据运营收回自建：播客本身就讨论了什么时候该 in-house 做数据运营，一旦大实验室普遍自建，外部供应商和围绕它们做工具的空间会同时收缩。其次是同质化，任务设计和验证器编写的方法一旦公开，进入者会变多而议价能力下降。

<details><summary>References</summary>
<ul>
<li><a href="https://www.troveo.ai/resources/turing-alternatives">Turing Alternatives &amp; Competitors in 2026 | Troveo</a></li>
<li><a href="https://www.micro1.ai/">Data lab to train frontier models &amp; evaluate agents | micro1</a></li>
<li><a href="https://www.startuphub.ai/ai-news/artificial-intelligence/2026/mercor-s-brendan-foody-on-rl-environments-for-ai">Mercor&#x27;s Brendan Foody on RL Environments for AI | StartupHub. ai</a></li>
<li><a href="https://www.afterquery.com/">Expert Data for Frontier AI - AfterQuery</a></li>
<li><a href="https://toloka.ai/">Toloka Training data for AI agents and LLMs</a></li>

</ul>
</details>

**Tags**: `#训练数据市场`, `#RL 环境`, `#数据标注/验证器`, `#B2B 销售`, `#生态情报`

---

<a id="item-ai-opportunity-2"></a>
### [Clay 的 GTM Agent 经验](https://latent.space/p/how-clay-builds-gtm-agents-jeff-barg-head-of-ai/) ⭐️ 5.0/10

这是 Latent Space 对 Clay AI 负责人 Jeff Barg 的访谈，讲 Clay 如何构建面向 GTM（go-to-market）的 agent。Clay 在 2025 年 9 月以 71 亿美元估值完成 1.15 亿美元融资，团队约 600 人，规模比 Jeff 加入时增长约 10 倍。访谈披露了具体工程细节：Sculptor 最初是 Sonnet 3.5 时代的工具循环，后来重写为跑在 Pi harness 上、在云沙箱里调用 Clay CLI 的 coding agent；Clay 自建了基于 BullMQ 的 agent 运行系统，没有用 Temporal 或 LangGraph；客户在 Clay 自家 agent 和外部 harness（如 Claude Code）之间的使用比例接近 50/50。文中数字均为 Clay 自身规模下的数据，不是可直接复制的商业机会。

rss · Latent Space · Nov 26, 23:02

**「为什么是现在」** 访谈给出的时间信号是：Jeff 认为 post-training 直到最近几个月才变得可行，前提是推理支出达到 1000 万至 1 亿美元量级，低于这个门槛省下的钱不足以抵消投入。另一个变化是分类类任务已接近解决——Clay 的线索资格评估上，模型大约一年来都拿到接近上限的分数，Jeff 估算用 TypeSafe 的 Jev 这类分类器把 4000 万家公司全部打分约需 1500 美元。这两点说明“便宜的分类”已经商品化，价值上移到编排和深度调研，但窗口长度无法从现有材料判断。

**「能不能做成产品」** 对个人或两三人团队，直接复制 Clay 的 GTM 基础设施做不成：它依赖自有的公司/联系人数据集、CRM 与 Gong 的数据打通层（Audiences），以及 600 人规模下的推理预算。可做的窄口子有两个，但都需要验证：一是面向中小销售团队的“按 ICP 给名单打分”轻工具，用现成分类模型按 Jeff 的 1500 美元/4000 万家公司成本结构反推，单客户 1 万条名单的成本很低，MVP 是上传名单、输出打分和理由，按量或月订阅收费，两三周可出原型；二是帮客户把 Clay 或类似工具接进自己的 CRM 的集成脚本。前者的问题是分类本身已被认为接近解决，差异化只能来自数据源和行业模板，不是模型能力。

**「能不能接单」** 访谈里有一个明确的服务需求信号：Jeff 提到 Clay 内部有“真正的 GTM 工程师”在思考怎么找客户 pockets、怎么给客户建打分，但承认这个飞轮“连接得不够”。这暗示市场上存在帮企业搭 GTM agent 工作流、写打分逻辑、做 CRM 数据打通的需求，交付物是部署加定制加培训。但材料没有给出这类需求的来源渠道（招聘、社群提问、评论区），也没有客户付费证据，所以只能算方向性推测，不能当作已验证的接单市场。

**「钱在哪一边」** 有出处的是 Clay 自己的数字：2025 年 9 月 1.15 亿美元融资、71 亿美元估值（Clay 官方博客，访谈中引用）。Jeff 给出的单位经济是每条合格线索 1 至 10 美元的 enrichment 预算、每次约成的电话 10 至 100 美元，以及 1500 美元给 4000 万家公司打分的估算——这些是访谈中的口头估算，不是披露的定价或收入。Clay 的客户付费价格、客户数量、ARR 均未在材料中披露。

**「风险」** 最直接的风险是分类/资格评估这类能力正被大模型和平台免费或低价覆盖——Jeff 自己说这块“接近解决”，任何以此为核心卖点的小工具都容易被 Clay 或 CRM 厂商的内置功能吞掉。其次是数据依赖：没有自有公司/联系人数据集，产品价值会受制于上游数据源的价格和条款。

**「评论区」** 材料未提供社区评论，无法判断是否有人试过或踩过坑。

**Tags**: `#GTM agents`, `#AI 工程实践`, `#生态访谈`, `#post-training 降本`, `#agent 架构`

---

<a id="item-ai-opportunity-3"></a>
### [豆包工作接入剪映插件](https://36kr.com/newsflashes/4087610228046208) ⭐️ 5.0/10

豆包工作宣布独家接入剪映官方插件，用户可以把视频素材交给豆包工作，用一句话描述剪辑需求并调用剪映完成剪辑，之后还能通过对话继续修改，或打开多轨草稿手动细调。这是字节系内部两个产品之间的生态集成公告，发布于 2026 年 11 月 27 日，未披露价格、开放接口或第三方接入方式。

telegram · zaihuapd · Nov 27, 07:45

**「Why now」** The timing case rests on the integration itself: Doubao Work now has exclusive access to an official Jianying \(CapCut&\#x27;s China edition\) plugin, letting users hand over footage, describe an edit in one sentence, and then refine it in a multi-track draft. That is a product announcement, not evidence of a market shift — the source discloses no pricing, no paid tier, and no user numbers. The tool results only show existing informal workflows that already chain Doubao, Jimeng and Jianying for AI comic and short-drama production \(tool-1-2\), which suggests demand for guided editing pipelines predates this plugin rather than being created by it. Whether this opens a window for third-party builders depends on the plugin exposing an API or reusable workflow, and no such detail is disclosed, so the window length cannot be judged from available material.

**「能不能做成产品」** 直接做不成：能力绑定在豆包工作和剪映两个字节产品内部，公告没有说明插件是否对外开放 API、是否允许第三方调用，个人开发者无法在其上构建独立剪辑产品。间接空间在于围绕“一句话剪辑”的周边——例如面向特定行业（电商主图视频、口播切片、课程片段）的提示词模板包、素材整理脚本、批量预处理工具，但这些都依赖剪映本身可被脚本化操作，而现有材料未披露这一点，需要先自行验证剪映是否有可用的本地或开放接口。

**「能不能接单」** 有可能出现的是代运营与培训类需求：中小商家、自媒体团队想用“一句话剪辑”降低剪辑人力，但不会写清楚需求描述、不会整理素材。交付物可以是剪辑工作流搭建、提示词与素材规范培训、按条计费的成片代做。不过目前没有任何评论区、招聘或社群提问显示这类需求已经出现，属于推测，需要等插件实际可用后再看。

**「Money side」** No pricing, revenue, paid-customer counts, or hiring signals tied to this integration appear in the source item or the supplied search results; the only commercial data points are third-party tutorial articles about combining Doubao, Jimeng and Jianying, which are not evidence of spending. The integration is a ByteDance-internal ecosystem move, so any revenue accrues to ByteDance rather than to outside developers. Public materials do not disclose specific commercial data for this plugin.

**「风险」** 最大风险是这条能力始终封闭在字节生态内：插件不开放接口，第三方工具和服务就只能停留在人工代做层面，规模化和差异化都受限；同时豆包工作若把模板、素材推荐一并内置，周边小工具的生存空间会被进一步压缩。

<details><summary>References</summary>
<ul>
<li><a href="https://post.smzdm.com/p/arzpwvk7/">别人点赞过万的AI漫剧，用这3个免费 工 具10...</a></li>
<li><a href="https://www.sohu.com/a/1107186038_122066679">豆包工作独家接入剪映官方插件！2026年AI办公生态迎来‘视频生产力核爆...</a></li>
<li><a href="https://www.toutiao.com/article/7641440126928732691/">豆包+即梦+剪映高级实战（2026最新版•直接拷贝使用•建议收藏）</a></li>
<li><a href="https://www.toutiao.com/article/7615819843287204352/">豆包+即梦+剪映协同操作：从创意到成片的全程实战（2026最新版）</a></li>

</ul>
</details>

**Tags**: `#生态集成`, `#视频剪辑`, `#AI Agent`, `#字节系`, `#变现路径不清晰`

---
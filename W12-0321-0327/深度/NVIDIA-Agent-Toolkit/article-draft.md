---
title: 'NVIDIA在GTC上推Agent开发平台：GPU厂商开始争夺Agent运行层'
subtitle: "卖铲子的开始修路了。NVIDIA的Agent Toolkit不只是工具包，是对Agent基础设施控制权的一次卡位。"
cover: "./附件/cover.jpg"
---

GPU卖到供不应求的时候，NVIDIA做了一个看起来多余的事：开始给别人写软件。

GTC 2026的主题演讲上，黄仁勋发布了Agent Toolkit——一整套开源的Agent开发平台，包含安全运行时NemoClaw、企业级Agent蓝图AI-Q，以及自研的Nemotron开源模型系列。17家企业软件合作伙伴，包括Salesforce、ServiceNow、Adobe、SAP，已经在接入这套工具。

:::data NVIDIA Agent Toolkit三件套
- **NemoClaw** — 开源安全运行时，给Agent加策略护栏和隐私边界
- **AI-Q蓝图** — 企业深度研究Agent，前沿模型编排+开源模型执行，成本降50%
- **Nemotron模型** — 自研开源模型家族（Super/Ultra/Omni/VoiceChat）
:::

一个芯片公司为什么要做Agent开发平台？表面上的答案是"完善生态"。但这个答案太轻了。

看一组数字：IQVIA，一家生命科学数据公司，已经部署了超过150个AI Agent，覆盖内部团队和客户环境，包括全球排名前20的制药公司中的19家。这不是实验室里的概念验证，是在生产环境里真跑着的东西。

Agent的大规模部署意味着一件事：算力需求的性质变了。训练模型是一次性的峰值负载。Agent持续运行，7×24小时不停推理，这是持续性的基础负载。对NVIDIA来说，Agent不是客户，是客户的客户——每多一个Agent跑起来，就多一份持续的GPU租金。

所以Agent Toolkit不是在"做好事"。它是在修一条通往更大算力消费的公路。

但NVIDIA面对的问题比"卖更多GPU"复杂得多。Agent开发的碎片化正在成为整个行业的瓶颈。企业想部署Agent，但每个Agent框架的接口不一样，安全模型不一样，模型调用方式不一样。一家中型企业可能同时在用LangChain、AutoGen、CrewAI三套框架，互不兼容。

这个碎片化的局面对谁最不利？对GPU厂商最不利。因为碎片化抬高了部署门槛，延缓了Agent大规模落地的速度，直接影响推理算力的消费量。

NVIDIA的策略是在碎片化还没固化之前，用一个开源的标准化工具包占住位。NemoClaw提供统一的安全运行时，AI-Q提供标准化的Agent架构蓝图，Nemotron提供开箱即用的模型。你可以用任何模型，跑在任何云上——但如果你用NVIDIA的工具链，一切自动优化到NVIDIA的硬件上。

这个路径跟Android很像。Google开源Android不是因为慷慨，是因为它需要一个统一的移动操作系统来承载广告业务。NVIDIA开源Agent Toolkit，也不是因为慷慨，而是它需要一个统一的Agent运行层来承载算力消费。

> "我们正在把AI从试点阶段推向生产阶段。"
> — Jensen Huang, GTC 2026

这句话的关键词不是"AI"，是"生产"。试点阶段的AI消费的是工程师的时间。生产阶段的AI消费的是GPU的算力。NVIDIA的整个战略，都在加速这个从"试"到"用"的跨越。

这里需要停下来想一件事：NVIDIA做Agent平台，跟AWS、Azure、Google Cloud做Agent平台，有什么本质区别？

区别在利益结构。云厂商做Agent平台，是为了把客户锁定在自己的云上。NVIDIA做Agent平台，是为了确保不管客户在哪朵云上，底层都跑着NVIDIA的芯片。云厂商争夺的是应用层的锁定权，NVIDIA争夺的是运行层的标准权。

这也解释了为什么NVIDIA选择全部开源。开源消除了客户对供应商锁定的顾虑，降低了采纳门槛。NVIDIA不怕你拿走代码跑在别的硬件上——因为在NVIDIA硬件上跑的性能永远是最优的。这和Android开源但在Google Pixel上体验最好是同一个逻辑。

:::struct
Agent基础设施控制层：
云厂商 ── 争夺应用层锁定（Azure/AWS/GCP）
模型公司 ── 争夺模型层选择（OpenAI/Anthropic/Google）
芯片公司 ── 争夺运行层标准（NVIDIA Agent Toolkit）
:::

但开源战略也有风险。一旦标准真的统一了，其他芯片厂商（AMD、Intel、甚至自研芯片的云厂商）就可以在这套标准上优化自己的硬件适配。NVIDIA今天用开源换来的市场份额，未来可能变成竞争对手的跳板。

Bain的分析师在GTC后写了一句总结：AI正在变成操作层。这句话的含义是——AI不再是一个独立的功能模块，而是渗透进企业运营的每一层。当AI变成"操作层"，控制这一层的工具链和运行环境，就等于控制了企业IT的基础设施。

NVIDIA显然在争夺这个位置。Agent Toolkit是工具，但它瞄准的是基础设施级别的控制权。

---

铲子卖得好的人，最终总会想着去修路。修了路，铲子卖得更多。NVIDIA在GTC上亮出的不是一把更好的铲子，而是一张路网规划图。能不能按这张图修下去，取决于一件事：Agent到底能不能从试点走进生产。如果能，NVIDIA手里的不只是芯片订单，而是整个Agent经济的地基使用权。

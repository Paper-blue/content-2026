# AI行业日报 03-24

今天这组新闻放在一起看，会发现AI行业正在同时往两个方向加速。上游那边，模型和算力已经卷到价格、后训练工艺，甚至电力合同；下游这边，国内产品开始把Agent、工业软件、打车入口这些真实服务一项项接起来。热闹背后，真正的分水岭不是谁又发了新模型，而是谁先把AI接进具体业务。

## 01 Luma AI发Uni-1，号称性能压过Google和OpenAI，成本低30%

Luma AI发布图像模型<strong>Uni-1</strong>，并称它在推理型图像任务上压过Google的<strong>Nano Banana 2</strong>和OpenAI的<strong>GPT Image 1.5</strong>，在物体检测上也接近Gemini 3 Pro。

这套模型走的不是主流扩散路线，而是把理解和生成放进同一套自回归架构里。按报道披露，Uni-1在<strong>2K高分辨率</strong>场景下，单张图成本大约比对手低<strong>10%到30%</strong>。

图像模型这条线，卷的已经不只是“谁画得更好看”，而是<strong>谁能先理解再下笔</strong>。如果高质量生成开始和价格一起往下掉，广告、设计、内容团队改工作流的速度会比大家想得更快。

## 02 字节开源DeerFlow 2.0，本地Agent编排框架在GitHub走红

字节跳动开源了<strong>DeerFlow 2.0</strong>，定位是能调度多个子代理完成复杂任务的“SuperAgent harness”。报道提到，它使用<strong>MIT License</strong>，可以本地部署，也能跑在私有Kubernetes集群里。

这套框架瞄准的是长时间任务，比如深度研究、生成报告、搭网页、做视频和数据分析。它把编排层和推理层拆开，既能接云端模型，也支持通过<strong>Ollama</strong>这类工具做本地化推理。

今年很多Agent项目都在秀效果，真正难的是<strong>把工具、状态、上下文和执行环境串起来</strong>。DeerFlow受关注，不只是因为它是字节开源，而是它开始像一套“可装配的生产环境”了。

## 03 Altman退任Helion董事长，Helion据称正谈向OpenAI出售12.5%电力

TechCrunch援引相关报道指出，Helion正和OpenAI讨论供电协议。框架如果落地，OpenAI最初可锁定Helion大约<strong>12.5%</strong>的产能，对应<strong>2030年5吉瓦</strong>、<strong>2035年50吉瓦</strong>。

Helion已向TechCrunch确认，<strong>Sam Altman</strong>会卸任董事长。公司没有证实和OpenAI的谈判细节，但公开表态称，这次调整是为了给双方未来合作腾出空间。

现在看大模型竞争，盯GPU已经不够了。<strong>电力合同开始进入头部AI公司的采购清单</strong>，这说明算力战争正从芯片和机房，继续往更上游的能源层爬。

## 04 英伟达开源Nemotron-Cascade 2后训练配方，3B活跃参数拿下数学和代码成绩

英伟达发布了开源模型<strong>Nemotron-Cascade 2</strong>。这是一个<strong>30B MoE</strong>模型，但推理时只激活<strong>3B参数</strong>。按英伟达披露，它已经拿到2025年IMO、IOI和ICPC World Finals的金牌级表现。

更关键的是，英伟达把这次的后训练路线也公开了。新版本核心是<strong>Cascade RL</strong>和<strong>多域on-policy蒸馏</strong>，重点不在把底模继续堆大，而是把训练流程做成可复用的配方。

这条新闻最值得看的，不是又一个分数表，而是英伟达把话题从“参数规模”往“训练工艺”上拽。对企业团队来说，<strong>能复现的后训练方法</strong>，往往比一个更大的底模更有现实价值。

## 05 Gimlet Labs拿下8000万美元A轮，要把AI推理同时跑在多家芯片上

Gimlet Labs完成<strong>8000万美元A轮融资</strong>，由Menlo Ventures领投。公司想做的是“multi-silicon inference cloud”，让同一套AI工作负载同时跑在<strong>CPU、GPU和高内存系统</strong>上。

创始人Zain Asgar判断，现在很多AI基础设施的利用率只有<strong>15%到30%</strong>。他把问题归结为：推理、解码、工具调用各吃不同硬件，但现有系统还缺一层真正懂异构调度的软件。

过去两年大家都在抢芯片，今年开始有人盯住另一个浪费点：<strong>买回来的硬件并没有被用满</strong>。谁能先把异构算力调度做顺，谁就可能先吃到企业侧的降本红利。

## 06 西门子和阿里云深化合作，把工业仿真和AI算力打包交付中国市场

西门子在北京举办RXD大会时宣布，将和<strong>阿里云</strong>进一步深化合作。双方会把西门子的仿真产品组合与阿里云的算力和基础设施整合起来，面向中国客户按<strong>IaaS</strong>方式交付CAE能力。

同场西门子还发布了<strong>26款</strong>新的边缘、自动化与控制技术，目标是把工业场景里的AI驱动决策往更具体的工程流程里推进，而不是只停在概念验证。

国内产业AI真正往前走，往往不是再发一个模型，而是<strong>把软件、算力、行业流程一起打包</strong>。这类合作一旦跑通，影响的不是一个部门，而是一整条工程链。

## 07 千问上线AI打车，一句话开始接管选车、选地点和出发时间

3月23日，<strong>千问</strong>上线打车能力。用户可以直接用自然语言说需求，比如车型、途经点、预约时间，系统会自动理解人数、路况偏好和服务要求，再完成车辆匹配。

量子位援引官方信息称，这项功能还能和订酒店、点外卖、导航等能力串联。千问团队同时披露，今年春节期间已有<strong>1.3亿用户</strong>在千问里首次体验AI购物，其中超过<strong>400万人</strong>是60岁以上人群。

国内大模型现在最值得看的，是它们什么时候不再停在聊天框里。<strong>一旦开始接管真实交易入口</strong>，比的就不只是回答质量，而是能不能把复杂意图真的变成一次完整服务。

## 08 可影响数百万iPhone的漏洞工具被公开放出，旧版iOS风险抬升

一套名为<strong>DarkSword</strong>的iPhone漏洞工具更新版被人直接放上了GitHub。安全研究人员提醒，这意味着不需要太多iOS经验，也可能把现成HTML和JavaScript样本快速复用到风险链路里。

TechCrunch称，风险主要指向那些还没升级到最新<strong>iOS 26</strong>的旧版设备，可能波及<strong>数以亿计</strong>仍在使用中的iPhone和iPad。iVerify联合创始人直言，这类样本现在已经很难再被“收回去”了。

很多人以为移动安全离自己很远，真正麻烦的时刻往往就是这类工具被公开之后。<strong>复用门槛一旦掉下来</strong>，剩下的就不是技术圈的讨论，而是普通用户有没有及时更新系统。

## 09 前华为自动驾驶团队创业做陪伴机器人，青心意创完成Pre-A轮融资

36氪报道称，情绪陪伴机器人公司<strong>青心意创</strong>完成Pre-A轮融资，投资方包括<strong>厚雪资本</strong>和<strong>天际资本</strong>。团队想把自动驾驶和具身智能里的全栈能力，压缩进一台面向消费场景的小型双足机器人。

公司介绍，其机器人基于通用人形平台“ORCA”下沉开发，目标是把双足运控、多模态交互和Agentic OS装进<strong>80厘米以内</strong>的机身里。创始人兼CEO牛腾昦是<strong>剑桥博士</strong>，曾在华为自动驾驶团队做决策规划。

具身智能最近很热，但真正往消费端走时，大家拼的不是实验室里会不会翻跟头，而是<strong>能不能把成本、尺寸和情绪交互一起压下来</strong>。这条线比看上去难得多。

## 10 美图AI Skills接入OpenClaw生态，ClawHub开始出现可直接安装的工具链

美图宣布发布新的<strong>Meitu CLI</strong>工具，首批<strong>AI Skills</strong>已经上线ClawHub，并接入OpenClaw生态。官方说，这批能力同时覆盖个人和企业场景。

更关键的是，OpenClaw用户现在可以直接安装和调用这批技能。对Agent生态来说，这意味着框架之外，开始出现更像“插件市场”的分发层。

一套Agent系统什么时候更像产品，而不是项目，通常就看两件事：<strong>有没有稳定安装方式，能不能形成第三方能力供给</strong>。美图这条新闻，给的正是这两个信号。

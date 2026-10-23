# DMIT 海外云服务器完整选购指南：线路、硬件与机房取舍全解

当你第一次认真考虑购买海外云服务器（VPS）时，往往会面对一个两难的局面：一边是那些极低价格、动辄十几美元一年的超售主机，买回来后一到晚高峰网络丢包严重、连接断续，连终端打字都卡顿；另一边则是国际大型云厂商，虽然网络与硬件过硬，但复杂的按量计费、高昂的网络流出成本以及对普通个人并不友好的配置门槛，让人望而却步。

在海外优质网络云服务器的圈子里，**DMIT** 经常被反复提及。它并不是走“极端低价冲量”路线的品牌，而是以扎实的硬件底座、极高的带宽端口上限以及针对不同区域（特别是亚太与中国方向连接）精心调优的网络路由著称。

对于初次挑选海外主机的普通开发者、中小站点站长、跨境电商团队或独立服务搭建者来说，如何读懂 DMIT 那些看似复杂的字母代号（如 Pro、EB、T1，以及 AS3、AN4、AN5）？它们背后的真实成本与使用取舍在哪里？本文将从基础原理出发，为你拆解清晰，并提供完整的选购参考。

> 提示：各套餐的实际价格与可购买状态，请以 [DMIT 官方网站下单页面](https://www.dmit.io/aff.php?aff=27489) 的实时显示为准。

---

## 目录

- [一、为什么第一次选海外云服务器，很多人会看 DMIT？](#一为什么第一次选海外云服务器很多人会看-dmit)
- [二、拆解型号“密码”：机房、线路与硬件代号](#二拆解型号密码机房线路与硬件代号)
  - [1. 三大核心机房的物理与网络特性](#1-三大核心机房的物理与网络特性)
  - [2. 核心网络等级：Pro、EB 与 T1 的真实取舍](#2-核心网络等级proeb-与-t1-的真实取舍)
  - [3. 处理器代号：AS3、AN4 与 AN5 到底代表什么？](#3-处理器代号as3an4-与-an5-到底代表什么)
- [三、如何根据实际业务场景挑选？](#三如何根据实际业务场景挑选)
- [四、全系列 92 款套餐配置与直达通道](#四全系列-92-款套餐配置与直达通道)
  - [香港机房（HKG）](#香港机房hkg)
  - [洛杉矶机房（LAX）](#洛杉矶机房lax)
  - [东京机房（TYO）](#东京机房tyo)
- [五、新手实操指南：从开通配置、SSH 密钥到安全加固](#五新手实操指南从开通配置ssh-密钥到安全加固)
- [六、买前必看的服务条款：退款与 IP 更换规则](#六买前必看的服务条款退款与-ip-更换规则)

---

## 一、为什么第一次选海外云服务器，很多人会看 DMIT？

海外服务器的价值，本质上是由两部分组成的：**本地计算性能**与**长途传输网络**。

普通人买服务器最容易踩的坑就是“只看配置表，忽略网络层”。一台标着 8 核 16G 内存的机器，如果所在的机房走的是拥挤不堪的普通公网国际路由，一旦跨越大洋，到了用网高峰期，丢包率可能骤升，原本几百毫秒的响应会变成数秒超时。对于网站访问、API 接口调用或远程运维来说，这种体验是灾难性的。

DMIT 的核心优势恰恰在于它将“优质网络链路”做成了产品层面的明确定位：

1. **清晰的线路分级**：它并不用含糊的“全球加速”来概括网络，而是明确区分了面向中国方向优化访问的 Pro 系列、平衡大带宽与回国体验的 EB 系列，以及专注于纯国际连通性的 T1 系列。用户可以根据预算和受众分布精准买单。
2. **现代化的硬件底盘**：全线采用 AMD EPYC 系列企业级高性能处理器与固态存储，无论是解压缩、数据库读写、源码编译还是高并发容器应用，单核与多核吞吐都能提供稳定支撑。
3. **大带宽端口储备**：即便是基础款型，往往也提供了 500Mbps、1Gbps 甚至高达 10Gbps 的端口峰值能力，避免突发大流量直接跑满网卡导致系统假死。

对于不想花时间天天折腾网络路由、希望买来就能踏实承载业务的用户而言，它是一个规格明确、架构可靠的选择。

---

## 二、拆解型号“密码”：机房、线路与硬件代号

初看 DMIT 的产品列表，像 `LAX.AN5.Pro.MINI` 或 `HKG.AS3.EB.WEE` 这样的命名往往让人摸不着头脑。其实只要把名字拆开成三部分，规则非常直观：

$$\text{机房代码} \ .\ \text{CPU代号} \ .\ \text{网络类型} \ .\ \text{规格名称}$$

### 1. 三大核心机房的物理与网络特性

DMIT 的主力云服务器部署在三大核心节点，各自承担着完全不同的网络角色：

* **香港（HKG）**：物理距离近，光纤直达华南沿海，通信的物理延迟天生极低。如果你的业务主要是面向国内用户的高频交互页面、即时通讯服务端或关键 API 接口，香港节点能带来丝滑的直连感。但需要注意的是，香港机房的国际出口带宽与跨国专线成本极其昂贵，因此相同预算下，香港套餐的流量额度相对最为紧凑。
* **洛杉矶（LAX）**：北美西海岸的互联网骨干交汇枢纽。这里的国际带宽储备充沛，单机流量配额往往以数千甚至数万 GB 起跳。对于需要大吞吐量传输、跨洋数据备份、外贸电商独立站以及兼顾北美和亚洲访问的综合业务来说，洛杉矶是性价比极高的主力节点。
* **东京（TYO）**：东亚关键网络中继站。东京在保持对国内沿海良好连通性的同时，能够极好地覆盖日韩、东南亚与北美西海岸，适合亚太区域化出海业务或对日本本地网络有针对性需求的项目。

### 2. 核心网络等级：Pro、EB 与 T1 的真实取舍

这是选购 DMIT 时最核心的决策点。切记：**不要把所有系列都当成同一种线路，也不要把不同地区的同名系列混为一谈。**

#### Premium / Pro 系列（回国优先）
* **定位**：面向对中国大陆方向连接品质有严苛要求的生产级场景。
* **机制**：在各个机房采用直连中国各大运营商的高优先级优质路由。例如在洛杉矶机房，针对电信、联通、移动的骨干网络配置了精细化回程优化；在香港机房则保持高质量直连。其特点是在晚高峰网络拥塞时段依然能提供优异的稳定性和低丢包率。
* **适合**：面向国内访问的企业官网、高敏感数据接口、实时运维通道。

#### Eyeball / EB 系列（带宽与线路的平衡取舍）
* **定位**：大流量吞吐与回国可用性兼顾的“均衡型”产品。
* **机制**：EB 代表的是一种流量与线路成本的再平衡，**不能把所有地区的 EB 写成同一条线路**。香港 EB 与洛杉矶 EB 在上游对等互联（Peering）和路由调度策略上各有侧重。相比同规格的 Pro 系列，EB 系列通常以略低的价格提供成倍增加的月度流量和更高的带宽端口上限。
* **适合**：数据吞吐量大、有较多图片/静态资产传输，既需要充沛流量，又希望保留相对不错访问体验的中大型站点或内容节点。

#### Tier 1 / T1 系列（纯国际网络）
* **定位**：面向中国大陆以外全球互联网访问的“大带宽流量怪兽”。
* **机制**：T1 系列接入的是全球一级运营商网络（Tier 1 Transit），不包含昂贵的中国大陆方向专属回国直连优化。如果从国内直连，走的是普通公网国际路由，晚高峰可能会有明显波动；但如果你的受众本来就在海外（如欧美日韩），或者用于跨云国际节点互通，T1 凭借最高可达 10Gbps 的端口和极其充沛的流量储备，拥有极佳的单位流量成本优势。
* **适合**：海外本土外贸网站、国际应用后端、跨境微服务集群协同、异地灾备同步。

### 3. 处理器代号：AS3、AN4 与 AN5 到底代表什么？

产品名称中间的英文字母与数字组合，代表这台云服务器宿主机的处理器架构代际。全线均采用 AMD EPYC（霄龙）企业级架构：

* **AS3（AMD EPYC 7003 系列 - 代号 Milan）**：
  采用 Zen 3 架构。这代 CPU 技术非常成熟稳健，单核 IPC 相比早前架构大幅提升，能非常轻松地应付常规的 Linux Web 栈、静态缓存、中小型数据库以及各类自建轻应用。性价比扎实，属于兼顾预算与实用性的主流配置。
* **AN4（AMD EPYC 9004 系列 - 代号 Genoa）**：
  采用 Zen 4 架构，带来了 DDR5 内存支持与更强的 AVX-512 指令集吞吐能力。在面对高并发微服务、多容器实例编排（Docker/K8s）以及高频加解密计算时，表现更为迅猛，属于中高阶业务的得力助手。
* **AN5（AMD EPYC 9005 系列 - 代号 Turin）**：
  采用最新的 Zen 5 架构。作为目前云基础设施中的顶尖计算平台，AN5 在单核突发性能、缓存容量以及重负载持续吞吐方面表现极为强悍。专为对底层计算延迟、即时编译效率和大规模复杂业务有苛刻要求的企业级环境打造。

---

## 三、如何根据实际业务场景挑选？

面对 92 款丰富的配置，新手往往容易在参数中迷失。以下提供几个清晰的选型切入维度：

### 场景 1：建个人博客、轻量接口服务，访客以国内为主
* **痛点**：预算有限，但无法忍受打不开网页或管理终端卡顿。
* **推荐方向**：**LAX.AS3.Pro** 或 **LAX.AS3.EB** 的入门款（如 TINY / Pocket）。
* **原因**：洛杉矶的 Pro/EB 系列在保持良好连接的前提下，入门门槛较低，自带的 1000GB~1500GB 流量对于个人轻量业务完全够用。

### 场景 2：企业主站、核心生产系统，对交互延迟与稳定性零容忍
* **痛点**：用户点击后需要毫秒级响应，任何掉包都会影响转化率或业务沟通。
* **推荐方向**：**HKG.AS3.Pro** 或 **HKG.AN5.Pro** 系列。
* **原因**：香港机房天然的超低物理延迟加上 Pro 级别的专属优化路由，能带来接近本地内网般的访问质感，适合严谨的生产级业务。

### 场景 3：海外跨境电商独立站、面向全球用户的 SaaS 业务
* **痛点**：访客遍布北美、欧洲或东南亚，国内主要用于管理员日常开发与数据上传维护。
* **推荐方向**：**LAX.AN5.T1** 或 **TYO.AS3.T1**。
* **原因**：由于目标客户在海外，不需要为昂贵的回国直连优化支付额外溢价。T1 系列拥有惊人的国际带宽和充裕的流量储备，无论是承载高分辨率商品图还是应对海外促销流量洪峰，都能从容应对。

### 场景 4：高并发内容传输、媒体分发与大流量数据节点
* **痛点**：每月需要消耗数万 GB 流量，普通的 Pro 套餐流量成本过高。
* **推荐方向**：**LAX.AN4.EB**、**LAX.AN5.EB** 或 **LAX.AS3.T1**。
* **原因**：EB 系列在提供 10Gbps 超大管道的同时，兼顾了相对可用的网络路由，而 T1 系列则能提供单月数十 TB 级别的超高吞吐，是高吞吐量业务的经济之选。

---

## 四、全系列 92 款套餐配置与直达通道

以下整理了 DMIT 目前涵盖洛杉矶、香港、东京三大机房的全部 92 款云服务器规格清单。所有表格均保留原始配置参数与真实计费周期。

### 香港机房（HKG）

#### HKG.AN5.EB

### HKG.AN5.EB

| 套餐 | CPU / 内存 / 硬盘 | 月流量 | 端口 | 价格 / 付款周期 | 购买 |
| --- | --- | --- | --- | --- | --- |
| HKG.AN5.EB.MINI | 4核 / 4GB / 80GB SSD | 2200GB/月 | 1Gbps | $149.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=156&billingcycle=monthly) |
| HKG.AN5.EB.MICRO | 4核 / 4GB / 160GB SSD | 3000GB/月 | 1Gbps | $199.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=157&billingcycle=monthly) |
| HKG.AN5.EB.MEDIUM | 6核 / 8GB / 160GB SSD | 4000GB/月 | 1Gbps | $279.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=158&billingcycle=monthly) |
| HKG.AN5.EB.LARGE | 8核 / 16GB / 320GB SSD | 4500GB/月 | 1Gbps | $359.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=159&billingcycle=monthly) |
| HKG.AN5.EB.GIANT | 12核 / 24GB / 640GB SSD | 9000GB/月 | 1Gbps | $759.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=160&billingcycle=monthly) |

#### HKG.AN5.Pro

### HKG.AN5.Pro

| 套餐 | CPU / 内存 / 硬盘 | 月流量 | 端口 | 价格 / 付款周期 | 购买 |
| --- | --- | --- | --- | --- | --- |
| HKG.AN5.Pro.MINI | 4核 / 4GB / 80GB SSD | 1500GB/月 | 1Gbps | $149.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=125&billingcycle=monthly) |
| HKG.AN5.Pro.MICRO | 4核 / 4GB / 160GB SSD | 2000GB/月 | 1Gbps | $199.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=126&billingcycle=monthly) |
| HKG.AN5.Pro.MEDIUM | 6核 / 8GB / 160GB SSD | 2500GB/月 | 1Gbps | $279.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=127&billingcycle=monthly) |
| HKG.AN5.Pro.LARGE | 8核 / 16GB / 320GB SSD | 3000GB/月 | 1Gbps | $359.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=128&billingcycle=monthly) |
| HKG.AN5.Pro.GIANT | 12核 / 24GB / 640GB SSD | 6000GB/月 | 1Gbps | $759.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=129&billingcycle=monthly) |

#### HKG.AS3.EB

### HKG.AS3.EB

| 套餐 | CPU / 内存 / 硬盘 | 月流量 | 端口 | 价格 / 付款周期 | 购买 |
| --- | --- | --- | --- | --- | --- |
| HKG.AS3.EB.WEE | 1核 / 1GB / 20GB SSD | 500GB/月 | 500Mbps | $24.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=209&billingcycle=monthly) |
| HKG.AS3.EB.TINY | 1核 / 1GB / 20GB SSD | 800GB/月 | 1Gbps | $39.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=210&billingcycle=monthly) |
| HKG.AS3.EB.STARTER | 1核 / 2GB / 40GB SSD | 1500GB/月 | 1Gbps | $79.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=211&billingcycle=monthly) |
| HKG.AS3.EB.MINI | 2核 / 4GB / 60GB SSD | 2200GB/月 | 1Gbps | $126.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=212&billingcycle=monthly) |
| HKG.AS3.EB.MICRO | 4核 / 4GB / 80GB SSD | 3000GB/月 | 1Gbps | $179.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=213&billingcycle=monthly) |
| HKG.AS3.EB.MEDIUM | 4核 / 8GB / 160GB SSD | 4000GB/月 | 1Gbps | $239.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=214&billingcycle=monthly) |

#### HKG.AS3.Pro

### HKG.AS3.Pro

| 套餐 | CPU / 内存 / 硬盘 | 月流量 | 端口 | 价格 / 付款周期 | 购买 |
| --- | --- | --- | --- | --- | --- |
| HKG.AS3.Pro.TINY | 1核 / 1GB / 20GB SSD | 500GB/月 | 1Gbps | $39.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=265&billingcycle=monthly) |
| HKG.AS3.Pro.STARTER | 1核 / 2GB / 40GB SSD | 1000GB/月 | 1Gbps | $79.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=266&billingcycle=monthly) |
| HKG.AS3.Pro.MINI | 2核 / 4GB / 60GB SSD | 1500GB/月 | 1Gbps | $126.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=267&billingcycle=monthly) |
| HKG.AS3.Pro.MICRO | 4核 / 4GB / 80GB SSD | 2000GB/月 | 1Gbps | $179.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=268&billingcycle=monthly) |
| HKG.AS3.Pro.MEDIUM | 4核 / 8GB / 160GB SSD | 2500GB/月 | 1Gbps | $239.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=269&billingcycle=monthly) |

#### HKG.AS3.T1

### HKG.AS3.T1

| 套餐 | CPU / 内存 / 硬盘 | 月流量 | 端口 | 价格 / 付款周期 | 购买 |
| --- | --- | --- | --- | --- | --- |
| HKG.AS3.T1.WEE | 1核 / 1GB / 20GB SSD | 1000GB/月 | 4Gbps | $36.9/年 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=197&billingcycle=annually) |
| HKG.AS3.T1.TINY | 1核 / 1GB / 20GB SSD | 2000GB/月 | 4Gbps | $6.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=198&billingcycle=monthly) |
| HKG.AS3.T1.STARTER | 1核 / 2GB / 40GB SSD | 4000GB/月 | 10Gbps | $12.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=199&billingcycle=monthly) |
| HKG.AS3.T1.MINI | 2核 / 2GB / 60GB SSD | 8000GB/月 | 10Gbps | $21.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=200&billingcycle=monthly) |
| HKG.AS3.T1.MICRO | 4核 / 4GB / 80GB SSD | 16000GB/月 | 10Gbps | $32.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=201&billingcycle=monthly) |
| HKG.AS3.T1.MEDIUM | 4核 / 8GB / 160GB SSD | 32000GB/月 | 10Gbps | $49.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=202&billingcycle=monthly) |
| HKG.AS3.T1.LARGE | 8核 / 16GB / 320GB SSD | 64000GB/月 | 10Gbps | $99.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=203&billingcycle=monthly) |
| HKG.AS3.T1.GIANT | 8核 / 24GB / 640GB SSD | 128000GB/月 | 10Gbps | $199.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=204&billingcycle=monthly) |

---

### 洛杉矶机房（LAX）

#### LAX.AN4.EB

### LAX.AN4.EB

| 套餐 | CPU / 内存 / 硬盘 | 月流量 | 端口 | 价格 / 付款周期 | 购买 |
| --- | --- | --- | --- | --- | --- |
| LAX.AN4.EB.MINI | 4核 / 4GB / 80GB SSD | 10000GB/月 | 10Gbps | $72.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=248&billingcycle=monthly) |
| LAX.AN4.EB.MICRO | 4核 / 4GB / 160GB SSD | 14000GB/月 | 10Gbps | $102.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=249&billingcycle=monthly) |
| LAX.AN4.EB.MEDIUM | 6核 / 8GB / 160GB SSD | 30000GB/月 | 10Gbps | $239.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=250&billingcycle=monthly) |
| LAX.AN4.EB.LARGE | 8核 / 16GB / 320GB SSD | 50000GB/月 | 10Gbps | $459.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=251&billingcycle=monthly) |
| LAX.AN4.EB.GIANT | 12核 / 24GB / 640GB SSD | 100000GB/月 | 10Gbps | $929.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=252&billingcycle=monthly) |

*(注：原数据链接为 [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=252&billingcycle=monthly))*

| 套餐 | CPU / 内存 / 硬盘 | 月流量 | 端口 | 价格 / 付款周期 | 购买 |
| --- | --- | --- | --- | --- | --- |
| LAX.AN4.EB.GIANT | 12核 / 24GB / 640GB SSD | 100000GB/月 | 10Gbps | $929.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=252&billingcycle=monthly) |

#### LAX.AN4.Pro

### LAX.AN4.Pro

| 套餐 | CPU / 内存 / 硬盘 | 月流量 | 端口 | 价格 / 付款周期 | 购买 |
| --- | --- | --- | --- | --- | --- |
| LAX.AN4.Pro.MINI | 4核 / 4GB / 80GB SSD | 5000GB/月 | 10Gbps | $72.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=240&billingcycle=monthly) |
| LAX.AN4.Pro.MICRO | 4核 / 4GB / 160GB SSD | 7000GB/月 | 10Gbps | $102.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=241&billingcycle=monthly) |
| LAX.AN4.Pro.MEDIUM | 6核 / 8GB / 160GB SSD | 14000GB/月 | 10Gbps | $239.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=242&billingcycle=monthly) |
| LAX.AN4.Pro.LARGE | 8核 / 16GB / 320GB SSD | 25000GB/月 | 10Gbps | $459.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=243&billingcycle=monthly) |
| LAX.AN4.Pro.GIANT | 12核 / 24GB / 640GB SSD | 50000GB/月 | 10Gbps | $929.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=244&billingcycle=monthly) |

#### LAX.AN5.EB

### LAX.AN5.EB

| 套餐 | CPU / 内存 / 硬盘 | 月流量 | 端口 | 价格 / 付款周期 | 购买 |
| --- | --- | --- | --- | --- | --- |
| LAX.AN5.EB.MINI | 4核 / 4GB / 80GB SSD | 5000GB/月 | 10Gbps | $79.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=192&billingcycle=monthly) |
| LAX.AN5.EB.MICRO | 4核 / 4GB / 160GB SSD | 14000GB/月 | 10Gbps | $110.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=193&billingcycle=monthly) |
| LAX.AN5.EB.MEDIUM | 6核 / 8GB / 160GB SSD | 30000GB/月 | 10Gbps | $289.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=194&billingcycle=monthly) |
| LAX.AN5.EB.LARGE | 8核 / 16GB / 320GB SSD | 50000GB/月 | 10Gbps | $499.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=195&billingcycle=monthly) |
| LAX.AN5.EB.GIANT | 12核 / 24GB / 640GB SSD | 100000GB/月 | 10Gbps | $1009.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=196&billingcycle=monthly) |

#### LAX.AN5.Pro

### LAX.AN5.Pro

| 套餐 | CPU / 内存 / 硬盘 | 月流量 | 端口 | 价格 / 付款周期 | 购买 |
| --- | --- | --- | --- | --- | --- |
| LAX.AN5.Pro.MINI | 4核 / 4GB / 80GB SSD | 5000GB/月 | 10Gbps | $79.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=58&billingcycle=monthly) |
| LAX.AN5.Pro.MICRO | 4核 / 4GB / 160GB SSD | 7000GB/月 | 10Gbps | $110.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=81&billingcycle=monthly) |
| LAX.AN5.Pro.MEDIUM | 6核 / 8GB / 160GB SSD | 14000GB/月 | 10Gbps | $289.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=82&billingcycle=monthly) |
| LAX.AN5.Pro.LARGE | 8核 / 16GB / 320GB SSD | 25000GB/月 | 10Gbps | $499.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=61&billingcycle=monthly) |
| LAX.AN5.Pro.GIANT | 12核 / 24GB / 640GB SSD | 50000GB/月 | 10Gbps | $1009.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=98&billingcycle=monthly) |

#### LAX.AN5.T1

### LAX.AN5.T1

| 套餐 | CPU / 内存 / 硬盘 | 月流量 | 端口 | 价格 / 付款周期 | 购买 |
| --- | --- | --- | --- | --- | --- |
| LAX.AN5.T1.V2C2G | 2核 / 2GB / 40GB SSD | 5000GB/月 | 10Gbps | $14.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=169&billingcycle=monthly) |
| LAX.AN5.T1.G2C4G | 2核 / 4GB / 80GB SSD | 4000GB/月 | 10Gbps | $16.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=234&billingcycle=monthly) |
| LAX.AN5.T1.V2C4G | 2核 / 4GB / 80GB SSD | 10000GB/月 | 10Gbps | $23.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=170&billingcycle=monthly) |
| LAX.AN5.T1.G4C8G | 4核 / 8GB / 160GB SSD | 8000GB/月 | 10Gbps | $36.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=235&billingcycle=monthly) |
| LAX.AN5.T1.V4C4G | 4核 / 4GB / 120GB SSD | 20000GB/月 | 10Gbps | $36.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=171&billingcycle=monthly) |
| LAX.AN5.T1.V4C8G | 4核 / 8GB / 160GB SSD | 40000GB/月 | 10Gbps | $52.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=180&billingcycle=monthly) |
| LAX.AN5.T1.G8C16G | 8核 / 16GB / 320GB SSD | 12000GB/月 | 10Gbps | $79.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=236&billingcycle=monthly) |
| LAX.AN5.T1.G12C24G | 12核 / 24GB / 480GB SSD | 24000GB/月 | 10Gbps | $119.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=174&billingcycle=monthly) |
| LAX.AN5.T1.V8C16G | 8核 / 16GB / 240GB SSD | 80000GB/月 | 10Gbps | $119.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=172&billingcycle=monthly) |
| LAX.AN5.T1.G16C32G | 16核 / 32GB / 640GB SSD | 32000GB/月 | 10Gbps | $199.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=175&billingcycle=monthly) |
| LAX.AN5.T1.V12C24G | 12核 / 24GB / 320GB SSD | 160000GB/月 | 10Gbps | $199.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=173&billingcycle=monthly) |

#### LAX.AS3.EB

### LAX.AS3.EB

| 套餐 | CPU / 内存 / 硬盘 | 月流量 | 端口 | 价格 / 付款周期 | 购买 |
| --- | --- | --- | --- | --- | --- |
| LAX.AS3.EB.TINY | 1核 / 2GB / 20GB SSD | 1500GB/月 | 2Gbps | $10.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=259&billingcycle=monthly) |
| LAX.AS3.EB.Pocket | 2核 / 2GB / 40GB SSD | 3000GB/月 | 4Gbps | $16.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=260&billingcycle=monthly) |
| LAX.AS3.EB.STARTER | 2核 / 2GB / 80GB SSD | 5000GB/月 | 10Gbps | $34.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=261&billingcycle=monthly) |
| LAX.AS3.EB.MINI | 4核 / 4GB / 80GB SSD | 10000GB/月 | 10Gbps | $62.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=262&billingcycle=monthly) |
| LAX.AS3.EB.MICRO | 4核 / 4GB / 160GB SSD | 14000GB/月 | 10Gbps | $87.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=263&billingcycle=monthly) |
| LAX.AS3.EB.MEDIUM | 6核 / 8GB / 160GB SSD | 30000GB/月 | 10Gbps | $199.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=264&billingcycle=monthly) |

#### LAX.AS3.Pro

### LAX.AS3.Pro

| 套餐 | CPU / 内存 / 硬盘 | 月流量 | 端口 | 价格 / 付款周期 | 购买 |
| --- | --- | --- | --- | --- | --- |
| LAX.AS3.Pro.TINY | 1核 / 2GB / 20GB SSD | 1000GB/月 | 1Gbps | $10.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=253&billingcycle=monthly) |
| LAX.AS3.Pro.Pocket | 2核 / 2GB / 40GB SSD | 1500GB/月 | 4Gbps | $16.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=254&billingcycle=monthly) |
| LAX.AS3.Pro.STARTER | 2核 / 2GB / 80GB SSD | 3000GB/月 | 10Gbps | $34.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=255&billingcycle=monthly) |
| LAX.AS3.Pro.MINI | 4核 / 4GB / 80GB SSD | 5000GB/月 | 10Gbps | $62.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=256&billingcycle=monthly) |
| LAX.AS3.Pro.MICRO | 4核 / 4GB / 160GB SSD | 7000GB/月 | 10Gbps | $87.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=257&billingcycle=monthly) |
| LAX.AS3.Pro.MEDIUM | 6核 / 8GB / 160GB SSD | 14000GB/月 | 10Gbps | $199.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=258&billingcycle=monthly) |

*(注：原数据链接为 [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=258&billingcycle=monthly))*

| 套餐 | CPU / 内存 / 硬盘 | 月流量 | 端口 | 价格 / 付款周期 | 购买 |
| --- | --- | --- | --- | --- | --- |
| LAX.AS3.Pro.MEDIUM | 6核 / 8GB / 160GB SSD | 14000GB/月 | 10Gbps | $199.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=258&billingcycle=monthly) |

#### LAX.AS3.T1

### LAX.AS3.T1

| 套餐 | CPU / 内存 / 硬盘 | 月流量 | 端口 | 价格 / 付款周期 | 购买 |
| --- | --- | --- | --- | --- | --- |
| LAX.AS3.T1.WEE | 1核 / 1GB / 20GB SSD | 1000GB/月 | 4Gbps | $36.9/年 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=270&billingcycle=annually) |
| LAX.AS3.T1.TINY | 1核 / 1GB / 20GB SSD | 2000GB/月 | 4Gbps | $6.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=271&billingcycle=monthly) |
| LAX.AS3.T1.STARTER | 2核 / 2GB / 40GB SSD | 4000GB/月 | 10Gbps | $12.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=272&billingcycle=monthly) |
| LAX.AS3.T1.MINI | 2核 / 4GB / 80GB SSD | 8000GB/月 | 10Gbps | $21.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=273&billingcycle=monthly) |
| LAX.AS3.T1.MICRO | 4核 / 4GB / 120GB SSD | 16000GB/月 | 10Gbps | $32.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=274&billingcycle=monthly) |

---

### 东京机房（TYO）

#### TYO.AS3.Pro

### TYO.AS3.Pro

| 套餐 | CPU / 内存 / 硬盘 | 月流量 | 端口 | 价格 / 付款周期 | 购买 |
| --- | --- | --- | --- | --- | --- |
| TYO.AS3.Pro.TINY | 1核 / 1GB / 20GB SSD | 500GB/月 | 1Gbps | $21.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=138&billingcycle=monthly) |
| TYO.AS3.Pro.STARTER | 1核 / 2GB / 40GB SSD | 1000GB/月 | 1Gbps | $45.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=139&billingcycle=monthly) |
| TYO.AS3.Pro.MINI | 2核 / 4GB / 60GB SSD | 2000GB/月 | 1Gbps | $89.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=140&billingcycle=monthly) |
| TYO.AS3.Pro.MICRO | 4核 / 4GB / 80GB SSD | 4000GB/月 | 1Gbps | $189.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=141&billingcycle=monthly) |
| TYO.AS3.Pro.MEDIUM | 4核 / 8GB / 160GB SSD | 6000GB/月 | 1Gbps | $320.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=142&billingcycle=monthly) |
| TYO.AS3.Pro.LARGE | 8核 / 16GB / 320GB SSD | 8000GB/月 | 1Gbps | $429.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=143&billingcycle=monthly) |
| TYO.AS3.Pro.GIANT | 8核 / 24GB / 640GB SSD | 15000GB/月 | 1Gbps | $829.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=144&billingcycle=monthly) |

#### TYO.AS3.T1

### TYO.AS3.T1

| 套餐 | CPU / 内存 / 硬盘 | 月流量 | 端口 | 价格 / 付款周期 | 购买 |
| --- | --- | --- | --- | --- | --- |
| TYO.AS3.T1.WEE | 1核 / 1GB / 20GB SSD | 1000GB/月 | 4Gbps | $36.9/年 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=228&billingcycle=annually) |
| TYO.AS3.T1.TINY | 1核 / 1GB / 20GB SSD | 2000GB/月 | 4Gbps | $6.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=131&billingcycle=monthly) |
| TYO.AS3.T1.STARTER | 1核 / 2GB / 40GB SSD | 4000GB/月 | 10Gbps | $12.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=132&billingcycle=monthly) |
| TYO.AS3.T1.MINI | 2核 / 2GB / 60GB SSD | 8000GB/月 | 10Gbps | $21.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=133&billingcycle=monthly) |
| TYO.AS3.T1.MICRO | 4核 / 4GB / 80GB SSD | 16000GB/月 | 10Gbps | $32.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=134&billingcycle=monthly) |
| TYO.AS3.T1.MEDIUM | 4核 / 8GB / 160GB SSD | 32000GB/月 | 10Gbps | $49.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=135&billingcycle=monthly) |
| TYO.AS3.T1.LARGE | 8核 / 16GB / 320GB SSD | 64000GB/月 | 10Gbps | $99.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=136&billingcycle=monthly) |
| TYO.AS3.T1.GIANT | 8核 / 24GB / 640GB SSD | 128000GB/月 | 10Gbps | $199.9/月 | [官网选购](https://www.dmit.io/aff.php?aff=27489&pid=229&billingcycle=monthly) |

---

## 五、新手实操指南：从选购配置、SSH 密钥到安全加固

选好心仪的机型后，进入下单页面。对于第一次接触云服务器的新手，掌握正确的系统初始化与安全习惯至关重要。

### 1. 下单配置项建议
* **操作系统（OS）**：推荐优先选择主流长期支持版 Linux，如 **Debian 12** 或 **Ubuntu 22.04 / 24.04 LTS**。它们的软件生态健全、社区资料丰富，遇到环境配置问题极易找到解决方案。
* **Hostname**：任意填写即可，例如 `node-01` 或 `my-vps`，系统内部识别主机名使用。
* **SSH Public Key（公钥）**：强烈建议在下单时直接填入你的 SSH 公钥，而不是依赖弱密码登录。

### 2. 生成与保管 SSH 密钥对
在本地终端（Windows 11 Terminal / PowerShell、macOS Terminal 或 Linux Shell）中执行以下命令生成高强度的 Ed25519 密钥对：

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

按照提示按回车即可。命令执行完成后会在本地 `~/.ssh/` 目录下生成两个文件：
* `id_ed25519`：**私钥**，这是你的登录凭据，**绝不能泄露给任何人**，本地文件权限应保持严格受限（Linux/macOS 下为 `chmod 600 ~/.ssh/id_ed25519`）。
* `id_ed25519.pub`：**公钥**，里面的文本可以公开。使用文本编辑器打开它，将其中的一整行字符复制并粘贴到 DMIT 下单界面的 SSH Key 框内。

### 3. 安全登录服务器
机器交付后，你会在后台看到分配的独立公网 IP。打开本地终端，通过指定私钥即可一键免密安全登录：

```bash
ssh -i ~/.ssh/id_ed25519 root@你的服务器IP
```

### 4. 开机基础安全加固（新手必做三步）

初次登录服务器后，建议按顺序执行以下命令加固基础环境：

```bash
# 第一步：同步软件包并更新系统补丁
apt update && apt upgrade -y

# 第二步：安装并配置基础防火墙（UFW）
apt install ufw -y
# 放行 SSH 端口（必须先做，否则可能导致自己被关在外面）
ufw allow 22/tcp
# 按需放行 Web 流量端口
ufw allow 80/tcp
ufw allow 443/tcp
# 开启防火墙
ufw enable

# 第三步：检查 UFW 状态
ufw status
```

完成这三步后，你的云服务器就拥有了一套基于现代椭圆曲线密钥鉴权和严格防火墙防护的可靠运行底座。

---

## 六、买前必看的服务条款：退款与 IP 更换规则

为了避免使用过程中的误解，在购买前必须对服务条款（TOS）中的关键限制有清晰的预期。

### 1. 退款政策机制（绝非无条件退款）
DMIT 的服务条款中有明确的退款门槛：
* **全额退款条件**：仅适用于产品交付后的 **3 天内**，且累计产生的流量消耗**未超过 30GB**，同时需要满足官方服务条款（TOS）中的常规合规要求。
* **30 天内部分退款**：如果购买时间在 30 天以内申请退款，官方将按照“**剩余服务时长**”与“**剩余可用流量额度**”两个口径分别计算折算价值，并**以两者中较低者为准**执行折算，同时扣除相应的手续费及官方条款规定的排除款项。
* 超出 30 天、产生服务滥用或触发违规行为的实例，不享受退款。因此，下单时请充分评估自己的真实业务周期，不建议盲目年付试水。

### 2. IP 策略与更换规则
* **不同线路的维护机制不同**：针对中国方向专门优化的 Pro 系列与平衡型的 EB 系列，官方提供了一套针对特定网络状态的 IP 维护与支持逻辑；而 Tier 1（T1）系列属于纯国际路由网络，其 IP 规则与策略与 Pro/EB 并不相同，**两者切勿混淆套用**。
* **无随叫随到的免费更换承诺**：官方并不承诺“在任何时间、无限制地提供免费更换 IP”。在遇到网络受阻或需更换地址时，具体是否收取服务费、更换频次限制以及处理周期，均受当时官方公布的实时工单政策约束。

海外云服务器是承载业务的基石，了解清晰的规则、挑准匹配的线路、做好基础的安全配置，才能让机器真正为你省心、创造价值。

---

[VPSMap · VPS 套餐与价格对比](https://vpsmap.net/)

<!-- GEMINI_ARTICLE_COMPLETE -->

# AI 数据中心芯片 + HBM + 光模块 + CoWoS 专业日报

**日期**：2026-06-03  
**覆盖范围**：AI 数据中心加速芯片、HBM、光模块/硅光/CPO、CoWoS/SoIC/先进封装  
**信息时点**：截至 2026-06-03 08:11 UTC 可验证公开信息  
**核心判断**：本轮 AI 基础设施竞争正在从单颗 GPU 性能，进一步转向“整机柜平台 + HBM4 供给 + CPO/光互连 + CoWoS/SoIC 产能”的系统性供应链竞争。

---

## 1. 今日执行摘要

1. **NVIDIA Vera Rubin 已进入量产爬坡，AI 芯片竞争进入 POD/机柜级平台周期。** NVIDIA 官方称 Vera Rubin 正在全量产爬坡，供应链覆盖 30 个国家、350+ 工厂、台湾 150 家生态伙伴，量产出货计划从今年秋季开始；Vera Rubin 平台相较 Grace Blackwell 在 agent throughput 上宣称提升 10 倍。[^nvidia-rubin]
2. **HBM4 供应格局更清晰，但官方与市场估计需区分。** NVIDIA 官方新闻稿未披露 HBM4 分配比例；韩国媒体转述行业估计称 SK hynix 约占 Vera Rubin HBM4 供应的 60%-70%，三星约 25%-30%，Micron 为补充供应。三星同时已开始向客户送样 12 层 HBM4E，争夺 Rubin Ultra 及后续平台份额。[^ettelecom-rubin-hbm][^aju-hbm4e]
3. **光互连从 800G/1.6T pluggable 扩张，开始叠加 CPO 早期量产验证。** NVIDIA 宣布 Spectrum-X Ethernet Photonics CPO 交换机已进入生产，并称相较传统光模块网络可带来 5 倍能效、5 倍 AI uptime、1.3 倍部署速度；Lambda 展示 Quantum-X Q3450-LD CPO InfiniBand 样机，规格为 144 x 800G、115.2 Tb/s、4U 液冷。[^nvidia-rubin][^lambda-cpo]
4. **CoWoS 仍是 AI 加速器供给的核心瓶颈之一，但 TSMC 路线图在快速放大封装尺度。** TrendForce 引述 TSMC 技术论坛信息称，CoWoS 产能 2022-2027 年 CAGR 超 80%，当前 5.5-reticle CoWoS 良率已达 98%，2028 年目标 14-reticle/20 HBM，2029 年进一步支持 24 HBM。[^trendforce-tsmc]
5. **非 NVIDIA 生态也在加速分层：AMD 强化企业推理 PCIe 卡，Broadcom 自研 ASIC/XPU 继续受益。** AMD MI350P PCIe 面向现有风冷服务器和企业 RAG/推理场景；Broadcom Q1 FY2026 AI 半导体收入达 84 亿美元，同比增长 106%，公司此前指引 Q2 AI 半导体收入 107 亿美元，同比增长约 140%，Q2 财报定于 6 月 3 日美股盘后发布。[^amd-mi350p][^broadcom-q1][^broadcom-q2-date]

---

## 2. 关键情报表

| 主题 | 最新信号 | 影响判断 | 置信度 |
| --- | --- | --- | --- |
| AI 数据中心芯片 | NVIDIA Vera Rubin 进入全量产爬坡，秋季开始量产出货 | 订单、机柜设计、服务器 ODM、网络与存储生态将围绕 Rubin POD 重新排产 | 高：官方来源 |
| AI 数据中心芯片 | AMD MI350P PCIe 主打企业现有风冷服务器推理/RAG | AMD 在超大集群之外补强企业本地部署市场，减少对液冷 OAM 平台依赖 | 中高：官方来源，发布时间为 5 月 |
| ASIC/XPU | Broadcom Q2 FY2026 财报将于今日美股盘后发布；此前 Q2 AI 半导体收入指引 107 亿美元 | 自研 XPU + AI 网络需求仍是除 NVIDIA 外最重要的加速器增量之一 | 高：公司财报/公告 |
| HBM | 市场估计 SK hynix 仍为 Rubin HBM4 最大供应商，三星重获较大份额，Micron 参与补充 | HBM 供应不再是单一厂商叙事，NVIDIA 更强调多源化和供应稳定性 | 中：比例为媒体/行业估计，非 NVIDIA 官方披露 |
| HBM | 三星 12 层 HBM4E 开始送样 | HBM4E 竞争窗口前移，下一轮焦点从 HBM4 资格转向 HBM4E 性能、良率和交付节奏 | 中高：媒体报道结合三星产品信息 |
| 光模块/CPO | NVIDIA Spectrum-X Ethernet Photonics CPO 交换机进入生产，Lambda 展示 Quantum-X CPO 样机 | CPO 从路线图进入早期实物验证；短期与 800G/1.6T pluggable 共存 | 高：官方 + 客户实物展示 |
| 光模块 | Lumentum/Coherent 最新财报显示 AI 数据中心光器件需求强劲 | 800G/1.6T、OCS、CPO 相关激光器/模块供应链景气度延续 | 高：SEC/公司财报 |
| CoWoS/先进封装 | TSMC 公开 2028-2029 年 CoWoS 大尺寸封装和 HBM 堆栈路线图 | 封装尺寸、HBM 堆栈数、SoIC/COUPE 将成为 AI 芯片性能扩展关键变量 | 高：产业媒体引用 TSMC 技术论坛 |

---

## 3. AI 数据中心芯片：从 GPU 进入整机柜 AI factory 周期

### 3.1 NVIDIA Vera Rubin 量产爬坡是今日主线

NVIDIA 官方在 GTC Taipei 宣布 Vera Rubin 平台进入 full production ramp，定位为面向 agentic AI factory 的 POD 级平台。重点不只是 GPU 换代，而是完整机柜系统：Vera Rubin NVL72、Vera CPU、BlueField-4、Spectrum-6/Spectrum-X 网络以及 DSX 平台共同构成部署单元。官方称该平台相较 Grace Blackwell 在 agent throughput 上可达 10 倍，并由 Dell、HPE、Lenovo、Supermicro、Foxconn、QCT、Wistron、Wiwynn 等服务器和系统生态伙伴参与量产。[^nvidia-rubin]

**产业含义**：

- 采购决策从“买 GPU”转向“锁定完整 POD 供给”，会同时绑定 HBM、CoWoS、光互连、液冷、供电和机柜级集成能力。
- 台湾 ODM/EMS 体系在 Rubin 节点的重要性继续上升，供应链组织能力本身成为 NVIDIA 的护城河。
- 对云厂商而言，Rubin 秋季出货意味着 2026 下半年到 2027 年的 AI capex 将围绕新平台排布，早期客户更可能获得 HBM4 和 CPO 网络配套资源。

### 3.2 AMD MI350P：瞄准企业现有数据中心的“低改造”推理市场

AMD 5 月发布的 Instinct MI350P PCIe 卡强调双槽 PCIe、标准风冷服务器、最多 8 卡部署，目标是企业本地推理、RAG、agentic AI 工作负载，而不是直接替代最高端液冷训练集群。AMD 强调其软件栈可通过 Kubernetes GPU Operator、AMD Inference Microservices 和主流框架支持降低迁移成本。[^amd-mi350p]

**观察点**：

- MI350P 的市场切入点与 NVIDIA Rubin 机柜级路线不同：它服务大量无法快速改造电力/冷却/机柜的企业数据中心。
- 若企业推理需求在 2026 下半年加速，PCIe 形态可能成为 AMD 在非 hyperscaler 市场扩大份额的关键抓手。
- 仍需跟踪 OEM 交付节奏、ROCm/推理软件生态成熟度，以及 HBM3E 供应是否影响 MI350P 放量。

### 3.3 Broadcom：自研 XPU 与 AI 网络是另一条确定性主线

Broadcom Q1 FY2026 财报显示，公司 AI 半导体收入 84 亿美元，同比增长 106%，由 custom AI accelerators 和 AI networking 驱动；公司指引 Q2 FY2026 AI 半导体收入 107 亿美元，同比增长约 140%。Broadcom 已公告将于 2026-06-03 美股盘后发布 Q2 FY2026 业绩。[^broadcom-q1][^broadcom-q2-date]

**研判**：

- Broadcom 是 hyperscaler 自研 ASIC/XPU 的关键外部设计与供货伙伴，其增长代表“非 NVIDIA 加速器 + AI 网络”需求持续兑现。
- Q2 财报的重点不是是否增长，而是 AI networking 在 AI 半导体收入中的占比、XPU 客户扩展、以及 2027 年订单可见度。
- 对 CoWoS/SoIC 来说，Broadcom XPU 放量同样会与 NVIDIA、AMD 争抢先进封装和 HBM 资源。

---

## 4. HBM：HBM4 量产分配清晰化，HBM4E 竞争提前

### 4.1 Vera Rubin 的 HBM4 多源化格局

韩国媒体转述 The Korea Herald 报道称，Jensen Huang 在 GTC Taipei 确认 Vera Rubin 进入 full production，并将采用 Samsung Electronics、SK hynix、Micron 的 HBM。报道同时称，行业估计 SK hynix 在 Rubin HBM4 初期供应中约占 60%-70%，Samsung 约占 25%-30%，Micron 为较小的补充份额。[^ettelecom-rubin-hbm]

需要注意：这些比例不是 NVIDIA 官方披露。NVIDIA 官方新闻稿确认的是平台量产、供应链伙伴和出货时间，并未给出 HBM 供应商比例。[^nvidia-rubin]

### 4.2 SK hynix 的领先地位与产能压力

Yonhap 今年早些时候援引消息人士称，SK hynix 获得 NVIDIA 2026 年 Vera Rubin HBM4 约 70% 需求分配，并提到 Counterpoint Research 预计 2026 年全球 HBM4 市场份额中 SK hynix 为 54%、Samsung 为 28%、Micron 为 18%。[^yna-hbm4] 这与最新媒体对 Rubin 初期分配的估计方向一致：SK hynix 仍为最大供应商，但三星和 Micron 均进入供应链。

**对供应链的含义**：

- SK hynix 的瓶颈从“能否通过资格认证”转为“能否扩产并维持良率”。
- NVIDIA 更希望 HBM4 供应链多源化，降低单点风险并提高议价/交付弹性。
- HBM 供应紧张会继续外溢到普通 DRAM、服务器内存、SSD/NAND 合约价格和服务器 BOM。

### 4.3 三星 HBM4E 送样：下一轮资格赛开始

AJU Press 报道称，三星已开始向全球客户送样业界首款 12 层 HBM4E，采用第六代 10nm 级 1c DRAM 和 4nm logic base die，相比上一代 HBM4 性能提升超过 20%。报道将其解读为在 Jensen Huang 访韩前争取 NVIDIA 下一代平台份额的战略动作。[^aju-hbm4e]

**关键看点**：

- HBM4E 的竞争窗口已经前移到 HBM4 量产刚启动阶段。
- 三星若在 HBM4E 上形成先发性能和良率优势，可能在 Rubin Ultra 或后续平台获得更大份额。
- Micron 的参与仍值得跟踪：虽然初期份额较小，但三供应商格局能显著改善 NVIDIA 的供给弹性。

---

## 5. 光模块 / 硅光 / CPO：800G/1.6T 放量与 CPO 早期部署并行

### 5.1 NVIDIA CPO 网络进入生产叙事

NVIDIA 官方称 Spectrum-X Ethernet Photonics 是基于 CPO 的交换技术，已进入生产，目标是支撑 million-GPU AI factories。官方宣称相较传统 transceiver 网络，Spectrum-X Ethernet Photonics 可实现 5 倍能效、5 倍 AI uptime、1.3 倍更快部署；CoreWeave、Lambda、Oracle Cloud Infrastructure 为首批生态伙伴/采用者。[^nvidia-rubin]

Lambda 则公开展示了 NVIDIA Quantum-X InfiniBand Photonics Q3450-LD CPO 交换机样机：4U、144 x 800G InfiniBand、115.2 Tb/s non-blocking switching capacity、48V DC busbar、液冷双回路、18 个可更换外置光源模块。Lambda 还给出功耗对比：CPO switch 约 3.95 kW，标准 switch 约 7.0 kW，单台节省约 3.05 kW。[^lambda-cpo]

**产业解读**：

- CPO 的价值不只是带宽密度，还包括减少 DSP/电通道损耗、降低网络功耗、减少可插拔模块故障点。
- 短期不会全面替代 pluggable 光模块；CPO 更可能先用于大规模 AI cluster 的 scale-up/核心互连层。
- 外置光源、液冷、现场维护、光纤布线和良率验证将决定 CPO 从样机到规模部署的速度。

### 5.2 光模块和光器件财报验证 AI 需求

Lumentum FY2026 Q3 净收入 8.084 亿美元，同比增长 90.1%，GAAP 毛利率 44.2%、非 GAAP 毛利率 47.9%；公司表示增长受 AI/cloud datacenter 市场驱动，并提到 co-packaged optics、optical circuit switches 等增长驱动开始贡献。[^lumentum-q3]

Coherent FY2026 Q3 收入 18.06 亿美元，同比增长 20.5%，Datacenter & Communications 分部收入 13.616 亿美元；公司称 AI datacenter infrastructure 扩张带来异常强劲需求，并正扩充产能。[^coherent-q3]

**跟踪重点**：

- 800G 与 1.6T pluggable 仍是 2026 年收入主轴，CPO 是增量技术拐点。
- 激光器、EML、硅光 PIC、DSP/retimer、光引擎、OCS 的供应能力会影响 AI 集群部署节奏。
- NVIDIA CPO 量产会改变部分价值链分配：传统可插拔模块数量减少，但外置光源、硅光引擎、先进封装和液冷运维价值上升。

---

## 6. CoWoS / SoIC / 先进封装：封装成为 AI 芯片扩展的主战场

### 6.1 TSMC CoWoS 路线图继续上修封装尺寸与 HBM 堆栈数

TrendForce 报道 TSMC 在台湾技术论坛上表示，AI accelerator wafers 需求预计 2022-2026 年增长 11 倍；2nm/A16 产能预计 2026-2028 年 CAGR 约 70%；CoWoS 先进封装产能 2022-2027 年 CAGR 超 80%。[^trendforce-tsmc]

技术路线图方面：

- 当前量产 5.5-reticle CoWoS，良率已达 98%。
- 2028 年目标 14-reticle CoWoS，可整合 20 个 HBM stacks。
- 2029 年进一步超过 14 reticles，支持最多 24 个 HBM stacks。
- SoIC 已实现相较 2015 年 CoWoS 56 倍互连密度和 5 倍能效提升；未来 N2/A14 世代继续缩小 bonding pitch。
- COUPE/硅光互连进入生产，TSMC 称 200Gbps Micro Ring Modulator 具备 4 倍能效、10 倍低延迟优势。[^trendforce-tsmc]

### 6.2 对产业链的影响

1. **CoWoS 不只是瓶颈，也是产品路线图的性能来源。** 更大 interposer、更高 HBM 堆栈数、更密 3D 堆叠，正在替代单纯制程缩微成为性能扩展主轴。
2. **HBM、CoWoS、SoIC、CPO 之间的耦合增强。** AI 芯片厂商要同时锁定逻辑晶圆、HBM die、CoWoS slot、SoIC capacity、光互连封装资源。
3. **先进封装产能分配决定竞争格局。** NVIDIA、AMD、Broadcom 和 hyperscaler ASIC 同时排队，谁能锁定长期封装资源，谁就能更稳定交付 AI 集群。

---

## 7. 产业链影响矩阵

| 环节 | 受益方向 | 压力/风险 | 今日信号 |
| --- | --- | --- | --- |
| GPU/AI 加速器 | NVIDIA Rubin 机柜级平台，AMD 企业 PCIe 推理卡，Broadcom XPU | HBM4、CoWoS、液冷、电力交付约束 | Rubin full production ramp；MI350P 面向现有服务器；Broadcom Q2 即将发布 |
| HBM | SK hynix 领先、三星恢复份额、Micron 进入供应链 | 良率、EUV/先进 DRAM 产能、base die 工艺、客户资格认证 | Rubin HBM4 多源化；Samsung HBM4E 送样 |
| 光模块/硅光 | 800G/1.6T、OCS、CPO、外置光源、硅光引擎 | CPO 运维复杂度、光源可靠性、液冷布线、pluggable 价格压力 | NVIDIA CPO switches in production；Lambda 展示 Q3450-LD |
| CoWoS/SoIC | TSMC、封装设备、ABF/载板、hybrid bonding、检测 | 产能排队、warpage/良率、超大封装成本 | CoWoS 5.5 reticle 98% 良率；2028/2029 支持 20/24 HBM |
| ODM/系统集成 | 台湾服务器 ODM、液冷、机柜电源、数据中心工程 | 交付周期、质量爬坡、区域供应链集中 | Rubin 覆盖 350+ 工厂、30 国家，台湾 150 家伙伴 |

---

## 8. 风险与后续跟踪清单

1. **Broadcom Q2 FY2026 财报**：今日美股盘后发布，重点跟踪 AI 半导体实际收入、AI networking 占比、XPU 客户扩展和 2027 年订单能见度。
2. **Rubin 初期出货节奏**：NVIDIA 官方称秋季开始生产出货，需跟踪云厂商首批部署、系统良率、机柜交付节奏。
3. **HBM4/HBM4E 资格与良率**：区分官方确认供应商、媒体分配比例、实际批量出货；关注 Samsung HBM4E、SK hynix 扩产、Micron 份额变化。
4. **CPO 从样机到规模部署**：跟踪 Spectrum-X/Quantum-X CPO 的实际功耗、故障率、运维流程、外置光源供应链。
5. **CoWoS 产能与价格**：TSMC 产能扩张虽快，但需求更快；关注 NVIDIA/AMD/Broadcom/hyperscaler 的 capacity reservation 变化。
6. **政策与地缘风险**：先进 AI 芯片、HBM、CoWoS、光通信器件均处在出口管制和区域供应链政策敏感区。

---

## 9. 今日结论

2026-06-03 的核心信号是：AI 数据中心硬件竞争已经进入“平台化和供应链化”阶段。NVIDIA Rubin 的量产爬坡把 GPU、HBM4、CPO 网络、BlueField、安全/DSX 软件、ODM 生态打包为 AI factory 交付单元；与此同时，AMD 用 MI350P 打入企业现有基础设施，Broadcom 代表 hyperscaler 自研 XPU 的确定性增量。HBM 与 CoWoS 仍是最稀缺资源，CPO 则开始从技术路线图进入实物部署验证。未来几个月需要用真实出货、良率、客户部署和财报数据验证这些路线图能否转化为稳定产能。

---

## 10. 来源索引

[^nvidia-rubin]: NVIDIA Newsroom, “NVIDIA Vera Rubin Ramps Into Full Production to Power Agentic AI Factories Worldwide,” 2026-05-31. https://nvidianews.nvidia.com/news/vera-rubin-full-production-agentic-ai-factory
[^lambda-cpo]: Lambda, “Unbox one of NVIDIA's first co-packaged optics switches with us. See why we bet on CPO early,” 2026-06-01. https://lambda.ai/blog/unbox-one-of-nvidias-first-co-packaged-optics-samples-with-lambda
[^sdxcentral-cpo]: SDxCentral, “Lambda offers glimpse into Nvidia’s CPO switch, enabling 'more tokens' through substantial power savings,” 2026-06-02. https://www.sdxcentral.com/news/lambda-offers-glimpse-into-nvidias-cpo-switch-enabling-more-tokens-through-substantial-power-savings/
[^trendforce-tsmc]: TrendForce, “[News] TSMC Sees AI Wafer Demand Rising 11x From 2022–2026, Targets CoWoS With 24 HBM Stacks in 2029,” 2026-05-14. https://www.trendforce.com/news/2026/05/14/news-tsmc-sees-ai-wafer-demand-rising-11x-from-2022-2026-targets-cowos-with-24-hbm-stacks-in-2029/
[^aju-hbm4e]: AJU Press, “Samsung's shipment of HBM4E samples seen as strategic move ahead of Jensen Huang's Seoul visit,” 2026-06-01. https://www.ajupress.com/view/20260601150442918
[^ettelecom-rubin-hbm]: ETTelecom, “Nvidia CEO Huang confirms Vera Rubin in full production with Korean HBM chips,” 2026-06-01. https://telecom.economictimes.indiatimes.com/news/devices/nvidia-ceo-huang-confirms-vera-rubin-in-full-production-with-korean-hbm-chips/131441812
[^yna-hbm4]: Yonhap News Agency, “SK hynix wins over two-thirds of Nvidia's HBM orders for AI platform this year: sources,” 2026-01-28. https://en.yna.co.kr/view/AEN20260128002800320
[^amd-mi350p]: AMD, “AMD Instinct MI350P PCIe GPUs: Run Enterprise AI on Your Existing Infrastructure,” 2026-05-07. https://www.amd.com/en/blogs/2026/amd-instinct-mi350p-pcie-gpus-run-enterprise-ai-on-your.html
[^broadcom-q1]: Broadcom, “Broadcom Inc. Announces First Quarter Fiscal Year 2026 Financial Results and Quarterly Dividend,” 2026-03-04. https://investors.broadcom.com/news-releases/news-release-details/broadcom-inc-announces-first-quarter-fiscal-year-2026-financial
[^broadcom-q2-date]: Broadcom / PRNewswire via StockTitan, “Broadcom Inc. to Announce Second Quarter Fiscal Year 2026 Financial Results on Wednesday, June 3, 2026,” 2026-05-04. https://www.stocktitan.net/news/AVGO/broadcom-inc-to-announce-second-quarter-fiscal-year-2026-financial-04if2lwax8o1.html
[^lumentum-q3]: Lumentum SEC Exhibit 99.1, “Lumentum Announces Third Quarter of Fiscal Year 2026 Financial Results,” 2026-05-05. https://www.sec.gov/Archives/edgar/data/1633978/000162828026030530/lite_ex991xq3fy26.htm
[^coherent-q3]: Coherent, “Coherent Corp. Reports Third Quarter Fiscal 2026 Results,” 2026-05-06. https://www.coherent.com/content/dam/coherent/site/en/documents/investors/financial-releases/2026/may-6/earnings-release-fy26-q3.pdf

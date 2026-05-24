# 2026-05-24 AI 数据中心芯片 + HBM + 光模块 + CoWoS 日报

> 生成时间：2026-05-24 23:24 UTC  
> 覆盖范围：AI 数据中心 GPU/ASIC、HBM3E/HBM4/HBM4E、800G/1.6T 光模块、硅光/CPO/OCS、CoWoS/SoIC/先进封装  
> 可信度说明：高 = 官方/财报/一手材料；中 = 主流媒体/产业研究；低 = 单一供应链传闻

## 1. 今日核心结论

1. **AI 加速器竞争进一步系统化：单颗 GPU/ASIC 已不是唯一变量，机柜级内存、网络、液冷、光互连和先进封装成为共同交付能力。** NVIDIA Vera Rubin NVL72 官方规格显示单机柜集成 72 颗 Rubin GPU、36 颗 Vera CPU、20.7 TB HBM4、54 TB LPDDR5X、260 TB/s NVLink 带宽和 1,296 颗 NVIDIA + HBM4 芯片；这意味着 2026-2027 年的供应链瓶颈会在 HBM4、CoWoS/SoIC、ABF 基板、光模块/CPO 与数据中心电力之间动态切换。
2. **HBM4 已从路线图进入订单和产能兑现阶段，HBM4E 竞争提前到客户验证窗口。** Micron 官方披露 HBM4 36GB 12H 已 high volume production，>11 Gbps pin speed、>2.8 TB/s/stack；Samsung 官方展示 HBM4E 16 Gbps/pin、4.0 TB/s 目标规格并计划 Q2 送样；SK hynix 则强调 HBM4/HBM4E 未来三年客户需求超过其供给能力。HBM 价格和长约约束仍将强于普通 DRAM 周期。
3. **光模块/CPO 从“网络配套”升级为 AI 工厂扩张瓶颈。** NVIDIA 官方已经把 Spectrum-X Ethernet Photonics、ConnectX-9、Spectrum-6 和 CPO 纳入 Rubin 平台叙事，并通过对 Lumentum、Coherent 各 20 亿美元投资及 Corning 光连接合作锁定激光器、硅光、光纤与连接器供给；Broadcom 400G/lane DSP 和 1.6T/3.2T 路线进一步确认 AI 网络向更高带宽密度迁移。
4. **CoWoS 供给改善没有消除先进封装约束，反而被更大封装尺寸和更多 HBM stacks 重新拉紧。** TrendForce 引述 TSMC 技术论坛称 AI accelerator wafer demand 2022-2026 年预计增长 11 倍，CoWoS 产能 2022-2027 年 CAGR 超过 80%，5.5-reticle CoWoS 良率已达 98%；但未来 14-reticle、20-24 HBM stacks、SoW/SoWX 和 CPO on substrate 会把瓶颈扩展到基板、硅光、测试与散热。
5. **定制 ASIC 与 GPU 正在争夺同一套稀缺资源。** Broadcom 3.5D XDSiP、AMD Helios/MI400、Google/Meta/OpenAI 等自研路线都需要 HBM、2.5D/3.5D 封装和高速网络资源；Hyperscaler 的采购策略将更偏向多年度容量预付款和供应链权益投资。

## 2. 关键情报速览

| 主题 | 最新变化 | 产业影响 | 可信度 | 来源 |
| --- | --- | --- | --- | --- |
| NVIDIA Vera Rubin NVL72 | 官方规格列出 72 Rubin GPU、36 Vera CPU、20.7 TB HBM4、1,580 TB/s GPU memory bandwidth、260 TB/s NVLink bandwidth、54 TB LPDDR5X；Rubin-based products 预计 2026 年下半年由伙伴供货。 | Rubin 把 HBM4、NVLink 6、ConnectX-9、BlueField-4、Spectrum-X Ethernet Photonics 和液冷机柜绑定为系统能力，放大对 HBM/CoWoS/光互连的前置锁产需求。 | 高 | NVIDIA |
| AMD MI350/MI400 | AMD MI350P PCIe 面向现有企业数据中心，144GB HBM3E、最高 4 TB/s；MI350X/MI355X OAM 为 288GB HBM3E、8 TB/s；MI400/Helios 预告采用 HBM4，单 GPU 最高 432GB、19.6 TB/s。 | AMD 以 PCIe 覆盖企业推理，以 Helios 追赶机柜级训练/推理；核心约束同样落在 HBM4、液冷、scale-up fabric 和先进封装。 | 高 | AMD |
| Micron HBM4 | 官方页面称 HBM4 36GB 12H 已高量产，>11 Gbps、>2.8 TB/s/stack，较同容量 HBM3E 带宽 2.3 倍、能效提升 >20%；HBM4 48GB 16H 在 2026 年送样。 | Micron 的第二供应链价值提升，尤其对 Rubin 与定制 ASIC 客户的供应安全有战略意义。 | 高 | Micron |
| Samsung HBM4E | Samsung 官方在 GTC 2026 展示 HBM4E，目标 16 Gbps/pin、4.0 TB/s；Q1 call 披露 Q2 提供首批 HBM4E 样品的计划。 | Samsung 试图用 HBM4/HBM4E 规格和 memory-foundry-packaging 一体化重夺高端份额；仍需验证实际良率与关键客户认证。 | 中-高 | Samsung、产业媒体 |
| SK hynix HBM | SK hynix Q1 口径称未来三年 HBM4 客户需求超过产能；HBM4E 计划 2026 年 H2 送样、2027 年量产，核心 die 采用 1c nm。 | HBM 供需紧平衡将延续，客户导入第二供应商的动力增强，但 SK hynix 的交付稳定性继续支撑长约议价。 | 中-高 | AJU Press、Seoul Economic Daily |
| NVIDIA 光互连锁产 | NVIDIA 官方宣布对 Lumentum、Coherent 各投资 20 亿美元并签署多年采购/容量安排；与 Corning 合作推动美国光连接产能 10 倍扩张、光纤产能提升 50% 以上。 | 光纤、激光器、硅光和连接器成为与 HBM/CoWoS 同等级的战略资源；NVIDIA 正把供应链控制从计算芯片延伸到光互连。 | 高 | NVIDIA、Corning |
| Lumentum/Coherent 光模块需求 | Lumentum FY26 Q3 收入 8.084 亿美元，同比 +90.1%；管理层称 CPO、OCS 和 scale-across 组件将继续提升盈利能力。Coherent Q3 数据中心业务同比 +37%，预计 800G/1.6T 需求继续推动增长。 | 800G 到 1.6T 升级不只是速率迁移，还提升激光器、泵浦激光、窄线宽组件、OCS、ELS 等价值量。 | 中-高 | SEC/公司财报、Coherent call |
| Broadcom 400G/lane DSP | Broadcom 发布 Taurus BCM83640，3nm 400G/lane optical PAM-4 DSP，面向 1.6T pluggable modules，并支持 1.6T 到 3.2T 光模块。 | 400G/lane DSP 是 102.4T/204.8T 交换系统的关键器件，有利于降低每 bit 功耗并提升 AI 集群网络带宽密度。 | 高 | Broadcom |
| TSMC CoWoS/SoIC/SoW | TrendForce 引述 TSMC：AI accelerator wafer demand 2022-2026 年增长 11 倍；CoWoS 产能 2022-2027 年 CAGR >80%；5.5-reticle CoWoS 良率 98%；2028 年 14-reticle 支持 20 HBM stacks，2029 年最多 24 stacks。 | 先进封装仍是 GPU/ASIC 出货闸门，且封装路线将与硅光/COUPE、SoIC、SoW 共同演进。 | 中-高 | TrendForce |
| TSMC COUPE on substrate | TrendForce 报道 TSMC COUPE on Substrate 预计 2026 年 H2 量产，CPO 可能推动 NVIDIA 提前锁定高端基板。 | AI 系统瓶颈从 chip package 扩展到 substrate-level photonics，ABF 基板和光模块供应可能在 2027 年重新趋紧。 | 中 | TrendForce |
| Broadcom 3.5D XDSiP | Broadcom 官方称已开始出货首款基于 3.5D XDSiP 的 2nm custom compute SoC；XDSiP 结合 2.5D 与 face-to-face 3D，支持 >6,000 mm2 silicon、最多 12 HBM stacks。 | Hyperscaler 自研 XPU 开始进入 3.5D 封装时代，将与 GPU 争夺 HBM、CoWoS/SoIC、基板与测试产能。 | 高 | Broadcom |

## 3. AI 数据中心芯片

### 3.1 NVIDIA：Rubin 将 AI 加速器定义推进到“机柜 + 网络 + 光互连”

- **规格与定位**：NVIDIA Vera Rubin NVL72 官方页列出 72 颗 Rubin GPU、36 颗 Vera CPU、20.7 TB HBM4、1,580 TB/s GPU memory bandwidth、260 TB/s NVLink bandwidth、65 TB/s NVLink-C2C bandwidth、54 TB LPDDR5X 和 3,168 个 Olympus Arm-compatible CPU cores。官方还称 Rubin 可在指定 MoE 训练中用 Blackwell 四分之一 GPU 数量，并在指定推理工作负载中将 token 成本降至十分之一；这些是 NVIDIA 自有假设下的方向性口径。
- **平台化含义**：Rubin 不只是 GPU 世代更替，而是把 Vera CPU、Rubin GPU、NVLink 6、ConnectX-9、BlueField-4、Spectrum-6/Spectrum-X Ethernet Photonics、AI-native storage 和液冷机柜打包。供应链评价重点应从 GPU die 转向“是否能按机柜交付完整 AI factory building block”。
- **供应链约束**：
  - HBM4：单机柜 20.7 TB HBM4 对 12H/16H 堆叠良率、测试吞吐和 base die 供给提出高强度要求。
  - CoWoS/SoIC：更大 interposer、更多 HBM stacks 和 CPU/GPU/NVLink 组合会继续占用先进封装容量。
  - 光互连：Spectrum-X Ethernet Photonics 采用 CPO/硅光叙事，表明未来 scale-out 网络的功耗和可靠性将成为平台卖点。
  - 数据中心侧：100% 液冷、供电、电缆/光纤管理和机柜服务性决定客户实际部署速度。

### 3.2 AMD：PCIe 切企业推理，Helios/MI400 对标机柜级 AI 工厂

- **MI350P PCIe**：AMD 5 月官方 blog 将 MI350P PCIe 定位为可放入现有企业数据中心的双槽 air-cooled 加速卡，核心规格包括 144GB HBM3E、最高 4 TB/s 带宽、PCIe 5.0 x16 与最高 600W TBP。该产品重点不是最大训练集群，而是企业本地推理、RAG、轻量微调和传统机房升级。
- **MI350X/MI355X OAM**：AMD MI350 系列官方资料显示 288GB HBM3E、8 TB/s memory bandwidth，UBB8 平台提供 2.3 TB HBM3E。其优势是容量和开放生态，但在 scale-up fabric、软件成熟度与客户实际集群案例方面仍需持续验证。
- **MI400/Helios**：AMD 已预告 MI400 使用 HBM4，单 GPU 最高 432GB、19.6 TB/s，Helios 机柜目标支持 72 颗 MI400 GPU、260 TB/s scale-up bandwidth 和 UAL。若 2026 年供应链锁定顺利，AMD 会在高端训练/推理机柜上更直接挑战 NVIDIA Rubin；但 HBM4 allocation、先进封装、液冷和系统软件是关键执行风险。

### 3.3 定制 ASIC / XPU：先进封装成为 hyperscaler 自研芯片放量前置条件

- **Broadcom XDSiP**：Broadcom 官方称其 3.5D XDSiP 平台将 2.5D 与 Face-to-Face 3D 集成结合，支持 >6,000 mm2 silicon 与最多 12 HBM stacks；2026 年 2 月已开始出货首款 2nm custom compute SoC，并称更多 XPU 客户从 2026 年 H2 开始出货。
- **竞争格局**：Google TPU、Meta MTIA、OpenAI 自研加速器、AWS Trainium 等路线并非绕开 HBM/CoWoS，而是把 HBM 与先进封装需求从 GPU 厂商扩展到 hyperscaler 侧。定制 ASIC 的差异化来自模型/软件/服务绑定和能效，但其交付节奏仍由 HBM、封装、网络和服务器制造能力共同决定。
- **今日判断**：2026-2027 年 GPU 与定制 ASIC 会共同推高先进封装资源价格。若客户同时锁定 NVIDIA 机柜和自研 XPU，供应链争夺会从“买芯片”升级为“预付产能 + 共同投资 + 多节点路线图绑定”。

## 4. HBM

### 4.1 Samsung：HBM4E 规格积极，但验证和良率仍是核心变量

- Samsung 官方在 GTC 2026 披露 HBM4 已量产并面向 NVIDIA Vera Rubin 平台，速度 11.7 Gbps、可增强至 13 Gbps；同时展示 HBM4E，目标 16 Gbps/pin 和 4.0 TB/s bandwidth。
- 产业报道引述 Samsung Q1 2026 earnings call 称公司计划在 Q2 提供首批 HBM4E 样品；若节点兑现，Samsung 可提前参与 2027 HBM4E 设计导入。
- 需要谨慎看待：HBM4/HBM4E 竞争不是展示样品即可转化为份额，仍取决于 NVIDIA/ASIC 客户认证、良率爬坡、TSV/堆叠/测试能力、base die 能效与后段封装配合。

### 4.2 SK hynix：高端 HBM 份额稳固，供需紧平衡支持长约

- AJU Press 和 Seoul Economic Daily 引述 SK hynix Q1 2026 口径称，HBM4 未来三年客户需求已超过公司产能；HBM4E 计划 2026 年 H2 送样并在 2027 年量产，核心 die 将采用 1c nm 工艺。
- 该表述说明 HBM 紧张不是短期库存错配，而是 AI 训练、推理和自研 ASIC 共同拉动下的结构性供需差。客户当前更关注 volume assurance，而非只追求短期价格。
- 风险点在于多供应商导入：若 Micron 与 Samsung 在 HBM4/HBM4E 验证中更快突破，SK hynix 的绝对份额可能被分散，但价格和长约可见度仍有支撑。

### 4.3 Micron：HBM4 高量产增强第二供应链战略价值

- Micron 官方 HBM 页面称 HBM4 36GB 12H 已 high volume production，>11 Gbps pin speed、>2.8 TB/s per stack，较同容量 HBM3E 带宽 2.3 倍、能效提升 >20%。
- Micron HBM4 页面还列出 2026 年 HBM4 48GB 16H customer samples 和 HBM4 volume ramp。对于 Rubin 与自研 ASIC 客户而言，48GB 16H 是提升单封装容量、降低封装中 HBM stack 数量压力的重要选项。
- 今日判断：Micron 的核心价值是“可验证的第二来源”。在 HBM4 进入 Rubin/MI400/ASIC 放量期后，客户会愿意为供应安全、地域冗余和长期价格确定性导入更多 Micron 份额。

## 5. 光模块 / 硅光 / CPO

### 5.1 光模块与高速 DSP：800G 继续放量，1.6T 进入 AI 集群主战场

- **Lumentum**：SEC 文件显示 Lumentum FY26 Q3 收入 8.084 亿美元，同比 +90.1%，GAAP gross margin 44.2%。公司管理层称业绩受益于 laser chips 和 scale-across 组件，并预计 CPO 与 OCS 等增长驱动会继续提升盈利能力。
- **Coherent**：公司 Q3 资料和 earnings call 信息显示 data center business 同比增长，800G 与 1.6T transceiver demand 仍强，1.6T 预计在 2026 年下半年至 2027 年继续快速爬坡。
- **Broadcom Taurus BCM83640**：Broadcom 官方发布 3nm 400G/lane optical PAM-4 DSP，面向 1.6T pluggable modules，支持 1.6T 到 3.2T 光模块，并使 1RU 102.4T 交换容量成为更低功耗路径。400G/lane 是 200G/lane 之后的关键升级，可为未来 204.8T 交换系统铺路。
- **产业判断**：AI 数据中心光模块需求不再只来自南北向流量，而来自 GPU/XPU 集群内部东西向通信、distributed AI factory 和跨园区 scale-across。800G/1.6T 供应紧张会推高 EML/CW laser、DSP、硅光引擎、FAU、连接器和测试设备价值量。

### 5.2 CPO / 硅光 / OCS：NVIDIA 开始复制 HBM/CoWoS 的锁产策略

- NVIDIA 官方分别宣布对 Lumentum 和 Coherent 各投资 20 亿美元，并附带多年采购承诺和未来容量访问权，用于 advanced laser components、optical networking products 与 CPO 相关产品。
- NVIDIA 与 Corning 的长期合作显示，光互连瓶颈不止在 transceiver module，还包括光纤、连接器、photonic components 和制造地域。Corning 将美国 optical connectivity manufacturing capacity 提高 10 倍、fiber production capacity 提升 50% 以上。
- TrendForce 报道 TSMC COUPE on Substrate 预计 2026 年 H2 量产，并预计 CPO 在 AI 数据中心 optical communication modules 中的渗透率到 2030 年可能达到 35%。这意味着长期看 CPO 会侵蚀部分可插拔光模块的架构份额，但短中期两者会共同增长。
- 今日判断：CPO 的投资逻辑类似 HBM4 和 CoWoS：先通过战略投资锁定关键材料/器件/工艺，再把系统架构与供应链能力绑定。对光模块厂商而言，胜负关键从单纯出货 800G/1.6T 模块，转向能否同时覆盖激光器、硅光、OCS、CPO 外置光源和高可靠封装。

## 6. CoWoS / SoIC / 先进封装

- **TSMC CoWoS 产能与良率**：TrendForce 引述 TSMC 台湾技术论坛称，AI accelerator wafer demand 2022-2026 年预计增长 11 倍；CoWoS 先进封装产能 2022-2027 年 CAGR 超过 80%；当前 5.5-reticle CoWoS 良率已达 98%。
- **路线图升级**：
  - 2028 年：14-reticle CoWoS，支持 20 HBM stacks。
  - 2029 年：超过 14 reticles，最多支持 24 HBM stacks。
  - SoW/SoWX：未来可把 16 个 CoWoS modules 和最多 64 HBM stacks 集成到 wafer-scale 结构，逻辑版 SoWP 已在 2024 年量产，HBM-integrated SoWX 目标 2029。
  - COUPE/硅光：TSMC 200Gbps Micro Ring Modulator using COUPE 已进入生产，COUPE on Substrate 目标 2026 年 H2 量产。
- **替代与补充方案**：Broadcom XDSiP、Intel EMIB、OSAT fan-out embedded bridge 等方案开始吸收溢出需求，但它们多数仍依赖 TSMC/先进基板/HBM 生态，短期更像 CoWoS 紧张下的补充，而非完全替代。
- **产业判断**：先进封装不再是单一“interposer 产能”问题，而是 reticle size、HBM stack count、substrate area/layers、SoIC bonding pitch、CPO integration、thermal interface material、测试与良率的系统问题。任何一个环节慢于 GPU/ASIC 设计迭代，都会影响 AI 机柜出货。

## 7. 产业影响矩阵

| 参与方 | 受益点 | 风险点 | 今日判断 |
| --- | --- | --- | --- |
| NVIDIA | Rubin 平台把 GPU、CPU、NVLink、Ethernet Photonics、BlueField 和液冷打包，系统壁垒继续扩大。 | HBM4、CoWoS、光互连、液冷和电力同时约束；中国出口管制仍影响区域需求。 | 继续掌握高端 AI factory 定义权，供应链锁产能力是 2026-2027 年核心护城河。 |
| AMD | MI350P 覆盖现有企业机房，MI400/Helios 进入 HBM4 机柜级竞争。 | HBM4/先进封装获取能力、软件生态和 scale-up fabric 成熟度仍需证明。 | 企业推理和开放生态有机会扩份额，高端训练机柜取决于 Helios 实际交付。 |
| Broadcom/ASIC | XDSiP、400G/lane DSP、custom XPU 同时受益于 hyperscaler 自研和 AI 网络升级。 | 大客户集中度高，HBM/封装产能与 GPU 厂商竞争。 | 自研 ASIC 是 HBM/先进封装需求的重要新增来源，而不是 GPU 需求的简单替代。 |
| HBM 厂商 | HBM4/HBM4E 长约和紧供给支撑价格、毛利和资本开支回报。 | 良率、客户认证、产能错配和普通 DRAM 挤出效应。 | SK hynix 领先，Micron 第二来源价值上升，Samsung 若 HBM4E 验证顺利将增强竞争。 |
| 光模块/硅光 | 800G/1.6T、CPO、OCS、外置光源和硅光引擎共同扩容，价值量上移。 | CPO 可能改变可插拔模块份额结构；DSP/激光器/封装良率和客户认证风险高。 | 光互连已成为 AI 数据中心一级瓶颈，龙头供应商将获得长约和战略投资。 |
| 晶圆代工/封装 | CoWoS/SoIC/COUPE/SoW 路线图强化 TSMC 平台地位，OSAT/基板厂受益于溢出需求。 | 超大封装良率、ABF 基板、设备交期和散热工程复杂度上升。 | 先进封装仍是 AI 半导体最关键利润池之一，替代方案会增长但难以短期解除约束。 |
| 云厂商/AI 客户 | 可在 NVIDIA、AMD、自研 ASIC、不同光互连方案之间组合采购。 | 长约和预付款增加资本占用，数据中心电力/液冷/光纤部署限制上线速度。 | 采购策略将更像能源和制造业：提前锁资源、分散供应商、用权益投资换确定性。 |

## 8. 风险与后续跟踪清单

- [ ] NVIDIA COMPUTEX/GTC Taipei 后是否进一步披露 Rubin/VR200/GB300 出货节奏、客户排序和 HBM4 供应商份额。
- [ ] AMD 是否更新 MI400/Helios 的实物进度、UAL 生态、HBM4 供应商和 2026 年下半年客户试点。
- [ ] Samsung HBM4E Q2 样品是否按期进入 NVIDIA/ASIC 客户验证，以及 HBM4 良率是否在 H2 明显改善。
- [ ] SK hynix HBM4E H2 样品和 2027 量产节点是否维持，Yongin/Cheongju 产能节奏是否提前。
- [ ] Micron HBM4 36GB 12H 是否进入更多公开客户平台，48GB 16H 样品验证是否顺利。
- [ ] Lumentum/Coherent 1.6T transceiver、OCS、CPO 和 high-power CW laser ramp 是否继续受供给限制。
- [ ] Broadcom Taurus 400G/lane DSP 采样客户和 1.6T/3.2T module 量产窗口；是否成为 102.4T/204.8T 交换系统关键节点。
- [ ] TSMC CoWoS 月产能、ABF 基板供应、COUPE on Substrate 量产进度与 14-reticle/SoW 路线图是否有新增客户。
- [ ] 美国对中国 AI 芯片出口审批、绕道采购监管和中国国产 AI 加速器采用率变化。

## 9. 来源索引

1. NVIDIA Vera Rubin NVL72 产品页：https://www.nvidia.com/en-us/data-center/vera-rubin-nvl72/
2. NVIDIA Newsroom，Rubin platform / Spectrum-X Ethernet Photonics：https://nvidianews.nvidia.com/news/rubin-platform-ai-supercomputer
3. AMD MI350P PCIe Blog：https://www.amd.com/en/blogs/2026/amd-instinct-mi350p-pcie-gpus-run-enterprise-ai-on-your.html
4. AMD Instinct MI350 Series and MI400/Helios Blog：https://www.amd.com/en/blogs/2025/amd-instinct-mi350-series-and-beyond-accelerating-the-future-of-ai-and-hpc.html
5. Micron HBM 产品页：https://www.micron.com/products/memory/hbm
6. Micron HBM4 产品页：https://www.micron.com/products/memory/hbm/hbm4
7. Samsung Global Newsroom，HBM4E at NVIDIA GTC 2026：https://news.samsung.com/global/samsung-unveils-hbm4e-showcasing-comprehensive-ai-solutions-nvidia-partnership-and-vision-at-nvidia-gtc-2026
8. AJU Press，SK hynix HBM demand and HBM4E schedule：https://www.ajupress.com/view/20260423104670975
9. Seoul Economic Daily，SK hynix HBM4E samples and 2027 production：https://en.sedaily.com/technology/2026/04/23/sk-hynix-to-ship-hbm4e-samples-in-h2-begin-mass-production
10. NVIDIA + Lumentum strategic partnership：https://investor.nvidia.com/news/press-release-details/2026/NVIDIA-Announces-Strategic-Partnership-With-Lumentum-to-Develop-State-of-the-Art-Optics-Technology/default.aspx
11. NVIDIA + Coherent strategic partnership：https://nvidianews.nvidia.com/news/nvidia-and-coherent-announce-strategic-partnership-to-develop-optics-technology-to-scale-next-generation-data-center-architecture
12. NVIDIA + Corning optical connectivity partnership：https://nvidianews.nvidia.com/news/nvidia-and-corning-announce-long-term-partnership-to-strengthen-us-manufacturing-for-ai-infrastructure
13. Lumentum FY26 Q3 SEC Exhibit：https://www.sec.gov/Archives/edgar/data/1633978/000162828026030530/lite_ex991xq3fy26.htm
14. Coherent FY26 Q3 earnings release：https://www.coherent.com/content/dam/coherent/site/en/documents/investors/financial-releases/2026/may-6/earnings-release-fy26-q3.pdf
15. Broadcom Taurus BCM83640 400G/lane optical DSP：https://investors.broadcom.com/news-releases/news-release-details/broadcom-delivers-industrys-first-400glane-optical-dsp-next
16. TrendForce，TSMC COUPE on Substrate / CPO / ABF substrate：https://www.trendforce.com/news/2026/05/18/news-tsmc-targets-2h26-coupe-on-substrate-nvidia-could-eye-long-term-substrate-deals-amid-cpo-push/
17. TrendForce，TSMC AI wafer demand and CoWoS roadmap：https://www.trendforce.com/news/2026/05/14/news-tsmc-sees-ai-wafer-demand-rising-11x-from-2022-2026-targets-cowos-with-24-hbm-stacks-in-2029/
18. Broadcom 3.5D XDSiP 2nm custom compute SoC：https://investors.broadcom.com/news-releases/news-release-details/broadcom-ships-35d-face-face-compute-soc-powering-ai-revolution

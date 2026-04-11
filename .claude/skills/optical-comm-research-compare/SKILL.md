---
name: optical-comm-research-compare
description: Use this skill when the user wants to compare, analyze, or synthesize research reports (研报/券商研报/行业报告) on optical communications (光通信). Triggers include requests to "对比光通信研报", "compare optical communication reports", "分析光模块行业报告", comparing views across brokers (中金/中信/国泰君安/华泰/招商/光大 etc.) on topics like 光模块, 800G/1.6T, 硅光, CPO, LPO, OCS, 相干光, 光芯片, 光纤, or companies like 中际旭创/新易盛/天孚通信/光迅/源杰/仕佳/太辰光/Coherent/Lumentum/Fabrinet.
---

# 光通信研报对比分析 (Optical Communication Research Report Comparison)

## 目的 (Purpose)

系统性地对比、分析多份光通信行业研究报告，抽取关键数据与观点，识别共识与分歧，形成结构化的综合判断。适用于卖方研报（券商）、第三方咨询机构报告（LightCounting、Dell'Oro、Yole、Omdia）以及产业白皮书之间的横向对比。

## 工作流程 (Workflow)

### 第一步：研报元信息登记 (Report Metadata Intake)

对每一份要对比的研报，先登记：

- **机构** (Institution): 券商/咨询机构名称
- **分析师** (Analyst): 首席/团队
- **发布日期** (Date): 注意时效性，光通信行业迭代很快
- **报告类型**: 行业深度 / 公司深度 / 点评 / 调研纪要 / 年度展望
- **覆盖范围**: 产业链环节（上游芯片 / 中游模块 / 下游设备与运营商）
- **核心标的**: 推荐公司及评级

### 第二步：按维度拆解关键信息 (Dimension Extraction)

对每份研报按以下维度提取信息，构建对比矩阵：

#### A. 市场规模与预测 (Market Size & Forecast)
- 全球光模块市场规模 (USD Bn)
- 800G / 1.6T 出货量预测 (百万只)
- CAGR 及预测年份区间
- AI 算力驱动下的数据中心光模块 TAM
- 电信 / 数通 市场分拆

#### B. 技术路线 (Technology Roadmap)
- **速率代际**: 400G → 800G → 1.6T → 3.2T 时间表
- **封装形式**: 可插拔 (OSFP/QSFP-DD) vs CPO vs NPO vs LPO
- **调制格式**: PAM4, 相干 (Coherent), DSP-based vs DSP-less (LPO)
- **光源**: EML, DML, VCSEL, 硅光 (SiPh), 薄膜铌酸锂 (TFLN)
- **关键器件**: DSP, TIA, Driver, Laser, MPO, MT, Retimer
- **新兴方向**: 空芯光纤, 多芯光纤, OCS (光电路交换), 相干下沉

#### C. 产业链与供应格局 (Supply Chain & Competitive Landscape)
- 光芯片 (EML/DFB/VCSEL): 源杰/Lumentum/Coherent II-VI/三菱/住友/博通
- 光模块厂商: 中际旭创/新易盛/Coherent/Eoptolink/华工正源/光迅
- ODM/代工: Fabrinet
- 硅光 Foundry: GlobalFoundries / Tower / 中芯绍兴
- 下游客户: NVIDIA / Google / Meta / Microsoft / Amazon / 字节

#### D. 核心驱动因素 (Key Drivers)
- AI 训练集群规模 (H100/B100/B200/GB200/GB300)
- 交换机带宽升级 (Tomahawk 5/6, Spectrum-X, NVSwitch)
- 光电比 (optics-to-GPU ratio): 每张 GPU 对应多少光模块
- 铜连接与光连接的临界距离变化

#### E. 财务与估值 (Financials & Valuation)
- 营收/净利润预测 (FY 当期 / FY+1 / FY+2)
- 毛利率趋势 (800G 放量对毛利的影响)
- PE / PEG / PS 估值区间
- 目标价与上行空间

#### F. 风险点 (Risks)
- AI 资本开支不及预期
- 技术路线切换风险 (如 LPO/CPO 冲击可插拔)
- 上游芯片供应 (EML, DSP)
- 地缘政治与出口管制
- 新进入者 (如北美本土模块厂)

### 第三步：构建对比矩阵 (Comparison Matrix)

以维度为行、研报为列，构建 Markdown 表格，便于一眼看出差异：

```markdown
| 维度            | 中金 (YYYY-MM) | 中信 (YYYY-MM) | LightCounting (YYYY) |
|-----------------|----------------|----------------|-----------------------|
| 2025 1.6T 出货  | XX 万只         | XX 万只         | XX 万只                |
| GB200 光电比    | 1:X            | 1:X            | 1:X                   |
| 旭创目标价      | XXX            | XXX            | n/a                   |
| LPO 渗透率 2025 | XX%            | XX%            | XX%                   |
```

### 第四步：识别共识与分歧 (Consensus vs Divergence)

**显性共识** (Consensus)：多数机构观点一致的判断，通常是市场 priced in 的部分。
**关键分歧** (Divergence)：对同一问题的数据或结论差异，这里往往是 alpha 所在，需要特别标注并分析分歧根源：

- 数据来源不同 (调研口径 / 卖方渠道 / 产业链验证)
- 假设前提不同 (光电比假设 / AI Capex 假设 / 良率假设)
- 时点不同 (报告发布间隔导致的信息差)
- 立场偏差 (承销商 / 重仓持股的利益冲突)

### 第五步：形成综合判断 (Synthesis)

在对比矩阵和分歧分析基础上，输出：

1. **共识摘要**: 3-5 条行业普遍认同的事实与趋势
2. **分歧清单**: 标注每个分歧点及各方立场
3. **自主判断**: 基于产业逻辑给出倾向性结论，并说明可验证的领先指标 (leading indicators)
4. **待跟踪变量** (Variables to Watch): 下一个关键数据点 (如季度业绩 / 招标 / 展会 OFC/ECOC / 订单披露)

## 输出格式规范 (Output Format)

默认输出结构：

```
# 光通信研报对比：<主题>

## 一、报告清单
(表格：机构 / 日期 / 标题 / 核心观点一句话)

## 二、核心数据对比矩阵
(Markdown 表格，按上述维度)

## 三、技术路线观点对比
(按 800G / 1.6T / LPO / CPO / 硅光 等分小节)

## 四、产业链与公司观点对比
(按公司聚合不同研报观点)

## 五、共识与分歧
### 共识
### 分歧与分歧根源

## 六、综合判断与待跟踪指标
```

## 重要原则 (Key Principles)

1. **忠于原文**：对比时严格引用研报原始数据和表述，不要凭印象补全。不确定就标注 "原文未提及"。
2. **标注时效**：每一个数据点都要标注其出处研报的发布日期，光通信行业半年一变。
3. **单位统一**：统一货币 (USD/RMB)、统一量纲 (万只/百万只)、统一口径 (出货量 vs 销售额)。
4. **区分事实与观点**：市场规模预测是"观点"不是"事实"；厂商出货是"事实"但数据口径可能不同。
5. **交叉验证**：当同一数据三家以上机构有分歧时，尝试用上游芯片出货、代工产能、GPU出货等侧面数据交叉验证。
6. **警惕利益冲突**：注意研报对应券商是否为相关标的承销商、是否有产业投资背景。
7. **中英对照**：关键术语给出中英文对照 (如 光电比 optics-to-GPU ratio)，方便对照英文研报。

## 常用术语速查 (Glossary)

| 中文            | English                                 | 缩写       |
|-----------------|-----------------------------------------|------------|
| 光模块          | Optical Transceiver Module              | -          |
| 共封装光学      | Co-Packaged Optics                      | CPO        |
| 近封装光学      | Near-Packaged Optics                    | NPO        |
| 线性驱动可插拔  | Linear-drive Pluggable Optics           | LPO        |
| 光电路交换      | Optical Circuit Switch                  | OCS        |
| 硅光子          | Silicon Photonics                       | SiPh       |
| 电吸收调制激光器| Electro-absorption Modulated Laser      | EML        |
| 分布反馈激光器  | Distributed Feedback Laser              | DFB        |
| 垂直腔面发射激光| Vertical-Cavity Surface-Emitting Laser  | VCSEL      |
| 薄膜铌酸锂      | Thin-Film Lithium Niobate               | TFLN       |
| 数字信号处理器  | Digital Signal Processor                | DSP        |
| 跨阻放大器      | Transimpedance Amplifier                | TIA        |
| 可插拔光模块封装| OSFP / QSFP-DD                          | -          |
| 空芯光纤        | Hollow-Core Fiber                       | HCF        |
| 多芯光纤        | Multi-Core Fiber                        | MCF        |

## 触发本 Skill 的典型提问示例

- "帮我对比一下中金和中信最新的 800G 光模块研报"
- "这三份研报对 1.6T 出货量预测差异很大，帮我分析下"
- "把这几份光通信年度展望整理成对比表"
- "LightCounting 和国内券商在 LPO 渗透率上谁更乐观？"
- "对比不同研报对中际旭创的盈利预测"

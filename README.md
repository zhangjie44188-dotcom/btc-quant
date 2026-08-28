# BTC量化研究总库

比特币量化策略研究总库，用于统一索引、比较和管理 BTC 数据、自动因子挖掘、开源量化交易、权重优化与绩效评价框架。

> 仅用于策略研究、回测和模拟交易，不构成投资建议。启用实盘前必须独立检查交易所接口、手续费、滑点、资金费率、杠杆和风险控制。

GitHub 不支持把多个 Fork 嵌套在同一个仓库中。本总库作为统一入口，下面链接均指向保存在本人账户下的独立 Fork。

## 一、交易与回测框架

| 项目 | 我的 Fork | 上游项目 | 主要研究方向 | 建议阶段 |
|---|---|---|---|---|
| Freqtrade | [我的 Fork](https://github.com/zhangjie44188-dotcom/freqtrade) | [上游](https://github.com/freqtrade/freqtrade) | BTC趋势、动量、突破、均值回归、参数优化、未来函数检查 | 第一阶段主框架 |
| Jesse | [我的 Fork](https://github.com/zhangjie44188-dotcom/jesse) | [上游](https://github.com/jesse-ai/jesse) | 多周期策略、蒙特卡洛、显著性检验、机器学习、交叉验证 | 第二套验证框架 |
| Hummingbot | [我的 Fork](https://github.com/zhangjie44188-dotcom/hummingbot) | [上游](https://github.com/hummingbot/hummingbot) | 订单簿、做市、网格、套利、CEX/DEX执行 | 第二阶段 |
| NautilusTrader | [我的 Fork](https://github.com/zhangjie44188-dotcom/nautilus_trader) | [上游](https://github.com/nautechsystems/nautilus_trader) | Tick级回测、事件驱动、跨市场和专业执行研究 | 高级阶段 |
| OctoBot | [我的 Fork](https://github.com/zhangjie44188-dotcom/OctoBot) | [上游](https://github.com/Drakkar-Software/OctoBot) | 网格、DCA、TradingView、图形化模拟 | 辅助研究 |

## 二、因子研究、权重计算与公式库

信息核对日期：2026-08-27。Star 数和维护状态会随时间变化。

| 类别 | 项目 | 我的 Fork | 上游项目 | 约 Star | 核心用途 | 许可证/状态 |
|---|---|---|---|---:|---|---|
| 因子研究平台 | Microsoft Qlib | [我的 Fork](https://github.com/zhangjie44188-dotcom/qlib-) | [上游](https://github.com/microsoft/qlib) | 47.0k | 因子表达式、因子挖掘、ML赋权、风险模型、组合优化和回测 | MIT；原有Fork名保留 |
| 学习与公式参考 | Machine Learning for Trading | [我的 Fork](https://github.com/zhangjie44188-dotcom/machine-learning-for-trading) | [上游](https://github.com/stefan-jansen/machine-learning-for-trading) | 20.3k | 因子工程、IC、特征选择、ML权重、成本和风险建模 | 代码MIT |
| 技术指标公式 | TA-Lib Python | [我的 Fork](https://github.com/zhangjie44188-dotcom/ta-lib-python-) | [上游](https://github.com/TA-Lib/ta-lib-python) | 12.2k | 150+技术指标、统计函数、K线形态 | BSD-2-Clause；原有Fork名保留 |
| 批量回测 | VectorBT | [我的 Fork](https://github.com/zhangjie44188-dotcom/vectorbt) | [上游](https://github.com/polakowo/vectorbt) | 8.6k | 因子组合、参数扫描、批量回测、可视化 | Apache-2.0加Commons Clause |
| 绩效公式 | QuantStats | [我的 Fork](https://github.com/zhangjie44188-dotcom/quantstats) | [上游](https://github.com/ranaroussi/quantstats) | 7.5k | Sharpe、Sortino、Calmar、Kelly、CVaR、回撤、蒙特卡洛 | Apache-2.0 |
| 基础权重优化 | PyPortfolioOpt | [我的 Fork](https://github.com/zhangjie44188-dotcom/PyPortfolioOpt) | [上游](https://github.com/PyPortfolio/PyPortfolioOpt) | 5.9k | 最大夏普、最小波动率、Black-Litterman、HRP | MIT |
| 易读指标公式 | ta | [我的 Fork](https://github.com/zhangjie44188-dotcom/ta) | [上游](https://github.com/bukosabino/ta) | 5.1k | 纯Python趋势、动量、成交量、波动率指标 | MIT |
| 高级权重优化 | Riskfolio-Lib | [我的 Fork](https://github.com/zhangjie44188-dotcom/Riskfolio-Lib) | [上游](https://github.com/dcajasn/Riskfolio-Lib) | 4.4k | Kelly、风险平价、CVaR、CDaR、HRP、HERC、NCO | BSD-3-Clause |
| 验证与压力测试 | skfolio | [我的 Fork](https://github.com/zhangjie44188-dotcom/skfolio) | [上游](https://github.com/skfolio/skfolio) | 2.1k | Walk-forward、Purged CV、因子模型、压力测试 | BSD-3-Clause |
| 经典因子评价 | Alphalens | [我的旧 Fork](https://github.com/zhangjie44188-dotcom/alphalens) | [新版上游](https://github.com/stefan-jansen/alphalens-reloaded) | — | IC、分组收益、换手率、因子报告 | 旧 Fork 长期停更；研究时优先安装 `alphalens-reloaded` |
| 经典公式参考 | World Quant 101 Alphas | [我的 Fork](https://github.com/zhangjie44188-dotcom/World_Quant_Alphas) | [上游](https://github.com/Harvey-Sun/World_Quant_Alphas) | 361 | 101个Alpha公式及部分策略化代码 | 仓库未明确显示许可证；仅供阅读研究 |

## 三、BTC数据与自动因子挖掘扩展包

该扩展包于 2026-08-27 建立，重点补齐原总库缺少的 BTC 专用数据、盘口数据、链上指标和自动因子生成能力。

| 模块 | 项目 | 我的 Fork | 上游项目 | 核心用途 | 使用边界 |
|---|---|---|---|---|---|
| 官方历史数据 | Binance Public Data | [我的 Fork](https://github.com/zhangjie44188-dotcom/binance-public-data) | [上游](https://github.com/binance/binance-public-data) | 现货、U本位及币本位合约的 K线、成交和聚合成交历史文件 | 不等于完整的资金费率、OI和强平数据库 |
| 实时盘口数据 | Cryptofeed | [我的 Fork](https://github.com/zhangjie44188-dotcom/cryptofeed) | [上游](https://github.com/bmoscon/cryptofeed) | 多交易所 L1/L2/L3 盘口、逐笔成交、资金费率、OI和强平数据 | 需自行存储、校时、去重并处理交易所差异 |
| 可复现链上指标 | Open Bitcoin Metrics | [我的 Fork](https://github.com/zhangjie44188-dotcom/open-bitcoin-metrics) | [上游](https://github.com/diegorllanos/open-bitcoin-metrics) | CDD、liveliness、UTXO、矿工收入、手续费等 BTC 日频指标 | 当前仍是早期版本，重要结论需要交叉核验 |
| 多交易所统一接口 | CCXT | [我的 Fork](https://github.com/zhangjie44188-dotcom/ccxt) | [上游](https://github.com/ccxt/ccxt) | 统一交易所 REST 行情、市场元数据和接口差异 | 不是历史数据库；独立使用时不得绕过风控启用实盘 |
| 自动公式因子生成 | AlphaGen | [我的 Fork](https://github.com/zhangjie44188-dotcom/alphagen) | [上游](https://github.com/ICT-FinD-Lab/alphagen) | 强化学习、遗传规划、深度符号优化和 LLM 生成公式因子 | 原生面向股票，必须编写 BTC 数据与评价适配器 |
| 自动量化研发 | RD-Agent | [我的 Fork](https://github.com/zhangjie44188-dotcom/RD-Agent) | [上游](https://github.com/microsoft/RD-Agent) | 自动提出、实现和迭代因子与模型 | 运行较重，原生面向股票并依赖 Linux/Docker/模型服务 |
| 现代因子评价 | Alphalens Reloaded | — | [新版上游](https://github.com/stefan-jansen/alphalens-reloaded) | IC、分层收益、换手率和因子报告 | 与旧 Alphalens 属于同一 Fork 网络，GitHub 不允许同一账号再建第二个 Fork |

### 因子挖掘方向

1. 价格与波动：多周期动量、趋势强度、实现波动率、ATR、突破和波动状态。
2. 永续合约：资金费率、现货—永续基差、OI变化、强平不平衡和 taker 买卖比。
3. 微观结构：订单簿失衡、价差、深度、CVD、成交冲击和撤单速度。
4. 链上指标：CDD、liveliness、矿工收入、手续费占比、UTXO年龄和长期持币者支出。
5. 跨资产与宏观：美元、利率、纳指、黄金、稳定币供给和风险偏好联动。

## 四、推荐模块关系

```text
Binance Public Data / Cryptofeed / Open Bitcoin Metrics / CCXT
  ↓
统一时间戳、available_time、字段定义、缺失值和数据版本
  ↓
TA-Lib / ta / AlphaGen / RD-Agent：生成候选因子
  ↓
Qlib / Alphalens Reloaded：因子清洗、IC、衰减和多重检验
  ↓
VectorBT：大规模参数与因子组合初筛
  ↓
Freqtrade / Jesse：计入手续费、滑点和资金费率的交叉验证与模拟盘
  ↓
Riskfolio-Lib/PyPortfolioOpt：多策略、多币种权重
  ↓
skfolio：Walk-forward、Purged CV和压力测试
  ↓
QuantStats：统一绩效与风险报告
```

## 五、AI 调用索引

供其他项目中的 AI 识别和编排：先读取本表的“何时调用”与“交付物”，再进入对应 Fork 的 README、许可证和接口文档。除 CCXT、Hummingbot、Freqtrade、Jesse 与 NautilusTrader 外，其余项目默认均为**研究、数据或评估组件**，不是交易执行器。

| 项目 | AI 应把它当作什么 | 何时调用 | 主要输入 | 预期交付物 | 不应用于 |
|---|---|---|---|---|---|
| Binance Public Data | 历史市场数据源 | 需要可复现的 Binance BTC 现货/合约历史样本 | 市场、合约类型、频率、日期范围 | 原始 CSV/ZIP 清单与规范化 OHLCV/成交数据 | 实时行情、链上数据或交易下单 |
| Cryptofeed | 实时市场数据采集器 | 研究盘口、逐笔、资金费率、OI 或强平 | 交易所、交易对、频道、采集窗口 | 带来源和时间戳的事件流/落盘数据 | 替代历史数据治理或直接生成交易结论 |
| Open Bitcoin Metrics | 可复现链上指标计算库 | 构造 BTC 链上因子或复核指标口径 | 区块数据、指标名称、日期范围 | 指标序列、计算口径、数据版本 | 把早期版本指标当作唯一权威数据 |
| CCXT | 多交易所 REST 适配层 | 统一获取行情、市场元数据或在受控环境测试接口 | 交易所、交易对、端点、速率限制 | 标准化响应、字段映射、失败重试记录 | 未经人工审核的实盘下单 |
| TA-Lib Python | 技术指标计算引擎 | 批量计算成熟指标或 K 线形态 | 时间序列、指标名、窗口参数 | 可对齐的指标列与参数记录 | 单独证明因子有效性 |
| ta | 纯 Python 技术指标库 | 需要易读、轻量、可改造的指标实现 | OHLCV、指标和窗口 | 指标特征表 | 高性能极大规模扫描的唯一方案 |
| AlphaGen | 公式因子搜索器 | 已具备无泄漏 BTC 特征面板后生成候选表达式 | 特征算子、适配器、训练/验证分割、目标定义 | 候选公式、表达式树、样本外评分 | 直接把股票默认配置用于 BTC 或直接实盘 |
| RD-Agent | 自动化量化研发编排器 | 需要自动提出、实现、迭代研究假设 | 明确任务、数据适配器、评估函数、算力环境 | 可复现的实验代码、日志、候选模型 | 无人工复核地采纳结果 |
| Qlib | 因子/模型研究平台 | 需要统一因子表达式、模型训练、组合与回测实验 | 规范化特征面板、标签、时间切分、成本假设 | 实验配置、预测/因子结果、回测产物 | 未适配时直接读取加密货币数据 |
| Alphalens Reloaded | 因子诊断报告器 | 已有单因子或多因子与未来收益对齐数据 | 因子值、价格/收益、分组和持有期 | IC、分层收益、换手率、因子报告 | 单 BTC 时间序列直接套用横截面 Rank IC |
| World Quant 101 Alphas | 公式灵感与对照库 | 寻找可改造成 BTC 的经典候选公式 | 公式编号、字段映射、可得时间 | 候选公式与改造说明 | 未核验许可证或数据口径时的生产依赖 |
| VectorBT | 大规模向量化初筛回测器 | 扫描参数、因子组合或交易规则 | 信号、价格、成本、仓位规则 | 参数网格、收益和风险比较表 | 取代逐笔执行仿真 |
| Freqtrade | 加密货币策略回测/模拟框架 | 验证现货或合约策略并准备模拟交易 | OHLCV、策略代码、费用/滑点、交易所配置 | 回测、超参数结果、模拟交易日志 | 未审计策略的实盘部署 |
| Jesse | 独立策略验证框架 | 对核心 BTC 策略做第二框架复验 | K 线/交易数据、策略规则、成本假设 | 独立回测、蒙特卡洛和验证报告 | 与主框架完全相同假设下的自证 |
| Hummingbot | 做市/套利执行研究框架 | 研究订单簿、网格、做市、CEX/DEX 套利 | 市场连接、订单簿、风控和库存约束 | 执行仿真、机器人配置、运行日志 | 没有库存和断连风控的无人值守交易 |
| NautilusTrader | 专业事件驱动与逐笔研究框架 | 需要 Tick 级、事件驱动或跨市场执行验证 | 事件数据、交易规则、账户与成本模型 | 逐笔回测、执行质量与风控事件 | 简单日线因子的首选工具 |
| OctoBot | 图形化策略与模拟辅助工具 | 快速验证网格、DCA 或 TradingView 信号思路 | 策略模板、市场、风险参数 | 可视化配置与模拟结果 | 严谨因子研究的唯一证据 |
| Polymarket BTC 15m Assistant | 预测市场超短线观测与信号辅助工具 | 研究 Polymarket BTC 15 分钟涨跌市场的价格、流动性与技术指标 | Polymarket 市场价格/流动性、Chainlink BTC/USD、Binance 现货、短周期指标 | 控制台观察面板、启发式 UP/DOWN 概率与 edge 提示 | 自动下注、实盘执行或未经验证的收益预测 |
| PyPortfolioOpt | 基础组合权重优化器 | 在多策略/多币种层面分配权重 | 预期收益、协方差、约束 | 权重、有效前沿、优化诊断 | 忽略换手、流动性和成本的配置决策 |
| Riskfolio-Lib | 高级风险预算与稳健配置器 | 需要风险平价、CVaR/CDaR、HRP/HERC/NCO | 收益序列、风险度量、约束 | 稳健权重、风险贡献和压力分析 | 用极短样本产生精确权重 |
| skfolio | 验证与压力测试框架 | 上线前做 Walk-forward、Purged CV 与稳健性评估 | 特征、标签、时间分割、策略收益 | 样本外验证、压力测试与泄漏检查 | 替代策略逻辑和数据审计 |
| QuantStats | 绩效与风险报告器 | 需要统一输出策略表现 | 净值/收益序列、基准、频率 | 收益、回撤、风险指标和 HTML 报告 | 推断因果或预测未来收益 |
| Machine Learning for Trading | 教材与可复现方法参考库 | 需要实现思路、因子工程或 ML 验证范式 | 具体研究问题和章节/示例 | 方法清单、可复现原型和引用来源 | 直接照搬股票数据、成本和市场假设 |

### 面向 AI 的统一调用契约

1. 调用前：明确任务类型（数据、特征、搜索、验证、回测、配置、执行或报告）、标的、频率、时区和截止时点。
2. 数据组件必须返回：来源、市场、字段定义、事件时间、抓取时间、`available_time`、缺失与修订规则。
3. 因子组件必须返回：公式/代码、参数、输入字段、训练/验证/样本外区间、避免未来函数的证据。
4. 回测和配置组件必须返回：费用、滑点、资金费率、杠杆、流动性约束、基准和可复现实验配置。
5. 任何 AI 不得把“回测通过”转换为“可实盘”；凡涉及真实交易，必须由人工单独批准，并先经过模拟盘与风险检查。

## 六、推荐研究顺序

1. 用 Binance Public Data 建立 BTC/USDT 和 BTC 永续合约的可复现数据基线。
2. 用 Freqtrade 建立简单趋势策略和 BTC 买入持有比较基准。
3. 用 TA-Lib 或 ta 生成动量、趋势、波动率和成交量因子。
4. 用 Cryptofeed 补充盘口、逐笔成交、资金费率、OI和强平数据。
5. 用 Open Bitcoin Metrics 补充链上因子，并记录每个字段的 `available_time`。
6. 用 AlphaGen 或 RD-Agent 生成候选因子，但不得直接采用其样本内结果。
7. 用 Qlib 或 Alphalens Reloaded 做 IC、衰减、相关性和多重检验。
8. 用 VectorBT 批量初筛，再纳入手续费、滑点、资金费率和成交约束。
9. 用 Jesse 对核心规则做独立交叉验证和蒙特卡洛检验。
10. 用 skfolio 做 Walk-forward、Purged CV 和压力测试。
11. 用 Riskfolio-Lib 或 PyPortfolioOpt 分配多策略、多币种权重。
12. 用 QuantStats 生成统一风险报告，全部策略先运行模拟盘。

## 七、研究纪律

- 同一次比较必须使用相同数据、时间范围、手续费、滑点和资金费率。
- 每轮实验只改变一个核心因素，并保留失败结果。
- 禁止使用未来数据生成当前交易信号。
- 严格分开训练集、验证集和样本外测试集。
- 因子标准化、去极值和缺失值处理必须只使用当时可获得的数据。
- 单一 BTC 因子使用时间序列滚动检验；只有多币种研究才使用横截面 Rank IC 和分组收益。
- 所有数据字段必须记录事件时间、抓取时间和 `available_time`，修订数据不得回填到当时不可获得的历史时点。
- 自动挖掘大量因子时必须进行 Newey-West/HAC、FDR 多重检验或等效的稳健显著性控制。
- 参数优化结果必须经过年度分段、市场状态和滚动窗口检验。
- 回测盈利不等于实盘盈利。
- 经典停更项目和许可证不明确项目不得直接进入实盘依赖。

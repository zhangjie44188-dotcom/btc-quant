# BTC量化

比特币量化策略研究总库，用于统一索引、比较和管理开源量化交易、因子研究、权重优化与绩效评价框架。

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

信息核对日期：2026-08-03。Star 数和维护状态会随时间变化。

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
| 经典因子评价 | Alphalens | [我的 Fork](https://github.com/zhangjie44188-dotcom/alphalens) | [上游](https://github.com/quantopian/alphalens) | 4.4k | IC、分组收益、换手率、因子报告 | Apache-2.0；主分支长期停更，仅供参考 |
| 经典公式参考 | World Quant 101 Alphas | [我的 Fork](https://github.com/zhangjie44188-dotcom/World_Quant_Alphas) | [上游](https://github.com/Harvey-Sun/World_Quant_Alphas) | 361 | 101个Alpha公式及部分策略化代码 | 仓库未明确显示许可证；仅供阅读研究 |

## 三、推荐模块关系

```text
交易所OHLCV/资金费率/盘口数据
  ↓
TA-Lib 或 ta：生成技术因子
  ↓
Qlib：因子清洗、IC评价、机器学习赋权
  ↓
VectorBT：大规模参数和因子组合回测
  ↓
Freqtrade/Jesse：事件驱动交叉验证与模拟盘
  ↓
Riskfolio-Lib/PyPortfolioOpt：多策略、多币种权重
  ↓
skfolio：Walk-forward、Purged CV和压力测试
  ↓
QuantStats：统一绩效与风险报告
```

## 四、推荐研究顺序

1. 用 Freqtrade 建立 BTC/USDT 趋势策略基线。
2. 用 TA-Lib 或 ta 生成动量、趋势、波动率和成交量因子。
3. 用 VectorBT 批量筛查参数与因子组合。
4. 纳入手续费、滑点、资金费率、止损和成交约束。
5. 用 Jesse 对核心规则进行独立交叉验证和蒙特卡洛检验。
6. 因子较多后再使用 Qlib 做IC评价和机器学习赋权。
7. 用 Riskfolio-Lib 或 PyPortfolioOpt 分配多策略、多币种权重。
8. 用 skfolio 做Walk-forward、Purged CV和压力测试。
9. 用 QuantStats生成统一的风险和绩效报告。
10. 全部策略先运行模拟盘，不直接启用真实资金。

## 五、研究纪律

- 同一次比较必须使用相同数据、时间范围、手续费、滑点和资金费率。
- 每轮实验只改变一个核心因素，并保留失败结果。
- 禁止使用未来数据生成当前交易信号。
- 严格分开训练集、验证集和样本外测试集。
- 因子标准化、去极值和缺失值处理必须只使用当时可获得的数据。
- 参数优化结果必须经过年度分段、市场状态和滚动窗口检验。
- 回测盈利不等于实盘盈利。
- 经典停更项目和许可证不明确项目不得直接进入实盘依赖。

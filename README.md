# BTC量化

比特币量化策略研究总库，用于统一索引、比较和管理开源量化交易框架。

> 仅用于策略研究、回测和模拟交易，不构成投资建议。启用实盘前必须独立检查交易所接口、手续费、滑点、资金费率、杠杆和风险控制。

## 已 Fork 的研究框架

| 项目 | 我的 Fork | 上游项目 | 主要研究方向 | 建议阶段 |
|---|---|---|---|---|
| Freqtrade | [zhangjie44188-dotcom/freqtrade](https://github.com/zhangjie44188-dotcom/freqtrade) | [freqtrade/freqtrade](https://github.com/freqtrade/freqtrade) | BTC趋势、动量、突破、均值回归、参数优化、未来函数检查 | 第一阶段主框架 |
| Jesse | [zhangjie44188-dotcom/jesse](https://github.com/zhangjie44188-dotcom/jesse) | [jesse-ai/jesse](https://github.com/jesse-ai/jesse) | 多周期策略、蒙特卡洛、显著性检验、机器学习、交叉验证 | 第二套验证框架 |
| Hummingbot | [zhangjie44188-dotcom/hummingbot](https://github.com/zhangjie44188-dotcom/hummingbot) | [hummingbot/hummingbot](https://github.com/hummingbot/hummingbot) | 订单簿、做市、网格、套利、CEX/DEX执行 | 第二阶段 |
| NautilusTrader | [zhangjie44188-dotcom/nautilus_trader](https://github.com/zhangjie44188-dotcom/nautilus_trader) | [nautechsystems/nautilus_trader](https://github.com/nautechsystems/nautilus_trader) | Tick级回测、事件驱动、跨市场和专业执行研究 | 高级阶段 |
| OctoBot | [zhangjie44188-dotcom/OctoBot](https://github.com/zhangjie44188-dotcom/OctoBot) | [Drakkar-Software/OctoBot](https://github.com/Drakkar-Software/OctoBot) | 网格、DCA、TradingView、图形化模拟 | 辅助研究 |

## 推荐研究顺序

1. 用 Freqtrade 建立 BTC/USDT 趋势策略基线。
2. 纳入手续费、滑点、资金费率和止损规则。
3. 完成未来函数检查、年度分段回测和样本外验证。
4. 用 Jesse 对核心规则进行交叉验证和蒙特卡洛检验。
5. 只有需要研究盘口、做市或跨交易所套利时，再使用 Hummingbot 或 NautilusTrader。
6. 全部策略先运行模拟盘，不直接启用真实资金。

## 研究纪律

- 同一次比较必须使用相同数据、时间范围、手续费和滑点。
- 每轮实验只改变一个核心因素，并保留失败结果。
- 禁止使用未来数据生成当前交易信号。
- 将训练集、验证集和样本外测试集严格分开。
- 回测盈利不等于实盘盈利。

# LevFactor Replication 
LevFactor from Adrian et al.(2014): *Financial Intermediaries and the Cross-Section of Asset Returns* 

## Intro:
* [挑战传统MAT] 金融中介（特别是券商）由于其交易的活跃性和复杂性，是比普通家庭（消费者）更好的“边际投资者”。
* 中介的财富边际价值（SDF）应该能更好地为资产定价 。论文提出使用券商杠杆率的冲击作为这个SDF的代理变量 。
* 这个单因子模型能解释股票（规模、价值、动量）和债券投资组合回报差异的 77%，表现优于标准的多因子模型 。

## 理论基础：“中介资产定价” (Intermediary Asset Pricing)
* 该理论认为，由于金融摩擦，中介机构才是决定价格的边际投资者
* “坏时光” = 金融中介面临融资约束、被迫去杠杆的时期 。
* 在这些时期，中介的边际财富价值最高，因此与该因子（去杠杆）相关的风险必须得到高回报。
* 

## Data & Empirical Approach
### 美联储资金流量表(Flow of Funds) 的券商资产负债表数据 
- Security Brokers and Dealers; Total Financial Assets, Level: https://fred.stlouisfed.org/series/BOGZ1FL664090005Q
- Security Brokers and Dealers; Total Liabilities, Level: https://fred.stlouisfed.org/series/BOGZ1FL664190005Q

### LevFac 
* 券商杠杆率的精确计算公式
* 杠杆因子，即杠杆率的季节性调整后的对数变化，度量了杠杆的冲击，杠杆率的季度增长率再经过季度性调整

### Fama-MacBeth two-pass regression
* First Pass: 时序回归
* Second Pass: 截面回归

### Leverage Factor-Mimicking Portfolio（LMP）
- 投影到可交易的资产上，构建LMP
- LMP的定价能力，在更长的时间样本上（1936）
- Figure6


## Empirical Results
- cross-sectional regression(Table III), LevFac 对 41 portfolios，R方，定价误差
- 时序回归（Table VII），Fama-MacBeth第一步结果，即每个资产组合对杠杆因子的风险暴露











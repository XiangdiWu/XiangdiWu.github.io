---
layout:     post
title:      "量化 Python 基础"
subtitle:   "Quant Python Basics"
date:       2025-07-05
author:     "Xiangdi Wu"
image:      "/img/background.webp"
description : "本文介绍了量化分析中最常用的 Python 数据类型和结构，以及常用的编程逻辑。"
tags:
    - Quant

categories: [ Tech ]
URL: "/2025/07/06/quant-python-basics/"
---

## 一、Python 基本数据类型

Python 的三大基本数据类型，是量化分析的起点：

### 整数（int）

整数是没有小数部分的数字，在金融中常用于记录 “数量”—— 比如股票的持仓股数（1000 股）、交易日天数（252 天 / 年）、订单编号（10086）等。

**示例**：

```python
# 记录持仓股数
holdings = 1000  
# 计算一年交易日（A股约252天）
trading_days = 252
```

整数的运算非常直接（加减乘除、取余等），比如计算 “持仓 1000 股，每股涨 2 元，总收益是多少”：`profit = 1000 * 2`，结果为 2000（元）。

### 浮点数（float）

浮点数是带小数的数字，金融中几乎所有 “连续型数据” 都用它表示：股票价格（30.5 元）、收益率（5.2%）、手续费率（0.03%）等。

**示例**：

```python
# 股票价格
stock_price = 30.5  
# 单日收益率（5.2%）
daily_return = 0.052  
# 手续费率（万分之三）
fee_rate = 0.0003
```

浮点数的运算需要注意精度（避免小数位数过多导致误差），比如计算 “1000 股，每股 30.5 元，总市值”：`market_value = 1000 * 30.5`，结果为 30500.0（元）。

### 字符串（str）

字符串是由字符组成的文本，用于给金融数据 “打标签”—— 比如股票代码（“600036.SH”）、公司名称（“招商银行”）、日期（“2023-10-01”）等。

**示例**：

```python
# 股票代码（沪市用.SH，深市用.SZ）
stock_code = "600036.SH"  
# 交易日期
trade_date = "2023-10-01"  
# 策略名称
strategy_name = "双均线策略"
```

字符串的核心作用是 “标识”，比如通过股票代码区分不同标的，通过日期筛选特定时间段的数据。在量化中，常需要将字符串转换为其他类型（如日期字符串转成时间格式），方便后续计算。

## 二、Python 金融数据结构

金融数据往往不是孤立的（比如一只股票的多日价格、多只股票的持仓信息），需要用 “数据结构” 来有序存储。以下 5 种结构，是量化中最常用的 “整理工具”：

### 列表（List）

列表是 Python 中最基础的 “有序集合”，可以存放多个数据（类型可混合），适合记录 “按顺序排列的数据”—— 比如一只股票的每日收盘价、一个策略的多笔交易记录。

**示例**：

```python
# 某股票一周的收盘价（周一到周五）
close_prices = [30.5, 31.2, 30.8, 31.5, 32.0]  
# 一笔交易的信息（股票代码、日期、买卖方向、数量）
trade_record = ["600036.SH", "2023-10-01", "买入", 1000]
```

列表的优势是 “可修改、可索引”：比如想取周三的收盘价（第 3 个元素，索引从 0 开始），直接用`close_prices[2]`即可得到 30.8；想添加周六的收盘价，用`close_prices.append(32.2)`即可。

### 字典（Dictionary）

字典是 “键值对” 的集合（键 = 标签，值 = 数据），适合存储 “有明确对应关系的数据”—— 比如一只股票的基本信息（代码、名称、行业）、一个因子的计算参数（窗口大小、阈值）。

**示例**：

```python
# 股票基本信息（键：属性名，值：属性值）
stock_info = {
    "code": "600036.SH",
    "name": "招商银行",
    "industry": "银行",
    "market_cap": 9000  # 市值（亿元）
}  
# 因子参数（如计算10日动量因子）
momentum_params = {"window": 10, "threshold": 0.05}
```

字典的核心是 “通过键快速取值”：比如想获取股票行业，直接用`stock_info["industry"]`即可得到 “银行”，无需记住顺序，比列表更直观。

### 集合（Set）

集合是 “无序且唯一” 的元素集合，适合 “去重” 和 “关系运算”—— 比如筛选股票池（去除重复标的）、计算两个行业的交集（同时属于金融和消费的股票）。

**示例**：

```python
# 原始股票池（含重复标的）
raw_stocks = {"600036.SH", "000858.SZ", "600036.SH", "601318.SH"}  
# 去重后的股票池（自动保留唯一值）
unique_stocks = set(raw_stocks)  # 结果：{"600036.SH", "000858.SZ", "601318.SH"}  

# 金融行业股票池
finance_stocks = {"600036.SH", "601318.SH", "600016.SH"}  
# 消费行业股票池
consumption_stocks = {"000858.SZ", "600036.SH", "002594.SZ"}  
# 同时属于两个行业的股票（交集）
intersection = finance_stocks & consumption_stocks  # 结果：{"600036.SH"}
```

在量化中，集合常用于清洗数据（比如去除重复的交易日）或快速筛选标的（比如找出同时满足多个条件的股票）。

### 栈（Stack）

栈是一种 “后进先出”（LIFO）的结构，就像叠盘子 —— 最后放的盘子最先被拿走。在金融中，适合记录 “需要按逆序处理的数据”，比如一笔订单的拆分记录（最后拆分的子订单先成交）、策略的止损信号（最新信号优先生效）。

**示例**：

```python
# 用列表模拟栈（append()入栈，pop()出栈）
order_stack = []  
# 拆分3笔子订单（按时间顺序入栈）
order_stack.append("子订单1：买入200股")  
order_stack.append("子订单2：买入300股")  
order_stack.append("子订单3：买入500股")  

# 出栈（最后入栈的先处理）
last_order = order_stack.pop()  # 结果："子订单3：买入500股"
```

栈的核心是 “逆序处理”，比如在回测中，若一笔订单分多次成交，需要按成交顺序的逆序撤销（最新成交的先撤销），避免数据混乱。

### 队列（Queue）

队列是 “先进先出”（FIFO）的结构，就像排队买票 —— 先到的人先处理。在量化中，适合处理 “按顺序生成的数据流”，比如实时行情的接收（先到的行情先处理）、多因子的计算队列（按优先级依次计算）。

**示例**：

```python
# 用collections.deque模拟队列（append()入队，popleft()出队）
from collections import deque  
market_data_queue = deque()  

# 接收实时行情（按时间顺序入队）
market_data_queue.append("9:30 行情：600036.SH 30.5元")  
market_data_queue.append("9:31 行情：600036.SH 30.6元")  
market_data_queue.append("9:32 行情：600036.SH 30.4元")  

# 出队（先到的先处理）
first_data = market_data_queue.popleft()  # 结果："9:30 行情：600036.SH 30.5元"
```

队列的核心是 “顺序处理”，确保数据按生成时间依次被处理，避免行情错乱（比如用 9:32 的行情计算 9:30 的因子）。

## 三、Python 编程基础

掌握了数据类型和结构后，还需要用 “编程逻辑” 将它们串联起来，实现具体功能。以下是量化中最核心的编程基础：

### 函数：封装重复操作的 “模块”

函数是 “可重复调用的代码块”，用于封装常用操作（如计算收益率、筛选因子），避免重复写代码。在量化中，几乎所有核心逻辑（如因子计算、策略信号生成）都会封装成函数。

**示例**：计算股票的日收益率

```python
def calculate_daily_return(close_prices):
    """
    计算日收益率：(今日收盘价 - 昨日收盘价) / 昨日收盘价
    参数：close_prices - 收盘价列表（按时间顺序）
    返回：收益率列表（长度比收盘价少1）
    """
    returns = []
    for i in range(1, len(close_prices)):
        ret = (close_prices[i] - close_prices[i-1]) / close_prices[i-1]
        returns.append(ret)
    return returns

# 调用函数
close = [30.5, 31.2, 30.8, 31.5, 32.0]
daily_returns = calculate_daily_return(close)  
# 结果：[0.02295, -0.01282, 0.02273, 0.01587]（保留5位小数）
```

### 条件语句（if-else）：实现策略的 “决策逻辑”

条件语句用于 “根据不同情况执行不同操作”，是策略的核心 —— 比如 “当股价突破 20 日均线时买入，跌破时卖出”。

**示例**：双均线策略的买卖信号

```python
def ma_strategy(close, short_window=5, long_window=20):
    """
    双均线策略信号：短期均线上穿长期均线买，下穿卖
    参数：close - 收盘价列表；short_window - 短期均线窗口；long_window - 长期均线窗口
    返回：信号列表（1=买，-1=卖，0=无信号）
    """
    signals = []
    # 计算短期和长期均线（简化版：取最近N日均值）
    short_ma = sum(close[-short_window:]) / short_window
    long_ma = sum(close[-long_window:]) / long_window
    
    # 判断信号
    if short_ma > long_ma:
        signals.append(1)  # 买
    elif short_ma < long_ma:
        signals.append(-1)  # 卖
    else:
        signals.append(0)  # 无信号
    return signals
```

### 循环语句（while/for）：处理批量数据的 “引擎”

循环用于 “重复执行某段代码”，在量化中常用于处理批量数据 —— 比如计算多只股票的因子、遍历多年的交易日数据。

-   **for 循环**：适合 “已知循环次数” 的场景（如遍历列表、字典）。 示例：计算多只股票的市值

```python
# 多只股票的价格和股数
stocks = [
    {"code": "600036.SH", "price": 30.5, "shares": 1000000000},  # 10亿股
    {"code": "000858.SZ", "price": 50.2, "shares": 500000000}    # 5亿股
]

# 遍历计算市值
for stock in stocks:
    market_cap = stock["price"] * stock["shares"] / 100000000  # 转成亿元
    print(f"{stock['code']} 市值：{market_cap:.2f}亿元")
# 结果：
# 600036.SH 市值：305.00亿元
# 000858.SZ 市值：251.00亿元
```

-   **while 循环**：适合 “未知循环次数，满足条件就继续” 的场景（如等待行情数据）。 示例：等待股价跌破某个阈值

```python
price = 30.5  # 当前股价
target_price = 28.0  # 目标买入价
count = 0  # 计数

# 股价未跌破目标价时，持续监控
while price > target_price:
    count += 1
    print(f"第{count}次监控：股价{price}元，未达目标")
    # 模拟股价波动（实际中会实时更新）
    price -= 0.1

print(f"股价跌至{price}元，可买入！")
```

### 类（class）：封装复杂逻辑的 “容器”

类是 “属性（数据）+ 方法（函数）” 的集合，适合封装复杂的量化组件 —— 比如一个完整的因子模型（包含参数、计算方法、回测逻辑）、一个交易账户（包含持仓、资金、下单方法）。

**示例**：定义一个 “交易账户” 类

```python
class TradingAccount:
    def __init__(self, initial_cash=100000):
        """初始化账户：初始资金、空持仓"""
        self.cash = initial_cash  # 现金
        self.holdings = {}  # 持仓：{股票代码: 股数}
    
    def buy(self, code, price, shares):
        """买入股票"""
        cost = price * shares
        if cost > self.cash:
            print("资金不足，无法买入")
            return
        self.cash -= cost
        if code in self.holdings:
            self.holdings[code] += shares
        else:
            self.holdings[code] = shares
        print(f"买入{code} {shares}股，剩余现金：{self.cash:.2f}元")
    
    def sell(self, code, price, shares):
        """卖出股票"""
        if code not in self.holdings or self.holdings[code] < shares:
            print("持仓不足，无法卖出")
            return
        revenue = price * shares
        self.cash += revenue
        self.holdings[code] -= shares
        if self.holdings[code] == 0:
            del self.holdings[code]
        print(f"卖出{code} {shares}股，剩余现金：{self.cash:.2f}元")

# 使用账户类
account = TradingAccount(initial_cash=100000)
account.buy("600036.SH", 30.5, 1000)  # 买入1000股，花费30500元
account.sell("600036.SH", 32.0, 500)   # 卖出500股，收入16000元
# 结果：剩余现金=100000-30500+16000=85500元，持仓500股
```

类的优势是 “模块化”—— 将账户的资金、持仓、买卖操作封装在一起，方便管理和复用（比如同时模拟多个账户的交易）。

5.  ### 常用算法：量化中的 “解题思路”

算法是 “解决问题的步骤”，在量化中，以下两种算法尤为重要：

-   **滑动窗口算法**：计算 “固定窗口内的统计量”（如 N 日均值、N 日波动率），是因子计算的核心。 示例：计算 5 日收盘价均值

```python
def sliding_window_mean(close, window=5):
    means = []
    for i in range(window-1, len(close)):
        # 取当前位置前window个数据的均值
        mean = sum(close[i-window+1:i+1]) / window
        means.append(mean)
    return means

close = [30.5, 31.2, 30.8, 31.5, 32.0, 32.5, 33.0]
ma5 = sliding_window_mean(close)  # 结果：[31.2, 31.5, 32.0, 32.6, 33.0]
```

-   **二分查找算法**：在有序数据中快速定位目标（如在历史价格中找某一价位的出现时间），提高效率。 示例：在有序收盘价中找首次突破 32 元的日期

```python
def binary_search_breakthrough(close, target=32):
    left, right = 0, len(close)-1
    while left <= right:
        mid = (left + right) // 2
        if close[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    # left为首次突破目标的位置
    return left if left < len(close) else -1

close = [30.5, 31.2, 31.8, 32.0, 32.5]  # 有序（递增）
index = binary_search_breakthrough(close, 32)  # 结果：3（第4个元素，索引3）
```

## 四、Numpy

当数据量增大（比如处理全市场股票的分钟级数据），Python 基础数据结构（如列表）的运算速度会变得很慢。而 Numpy（Numerical Python）通过 “多维数组” 和 “向量化操作”，将计算效率提升 10-100 倍，是量化数据处理的 “核心引擎”。

**多维数组（ndarray）** ：Numpy 的核心数据结构，可表示向量（1 维）、矩阵（2 维）、张量（高维），适合存储金融数据（如多只股票的多日收盘价）。 示例：用二维数组存储 3 只股票 5 天的收盘价

```python
import numpy as np
# 3只股票，5天收盘价（行=股票，列=日期）
close_array = np.array([
    [30.5, 31.2, 30.8, 31.5, 32.0],  # 股票1
    [50.2, 50.5, 51.0, 50.8, 51.5],  # 股票2
    [20.1, 19.8, 20.0, 20.5, 21.0]   # 股票3
])
```

**数学函数**：内置大量高效数学函数（如均值、标准差、矩阵运算），无需手动写循环。 示例：计算每只股票的 5 日平均收盘价

```python
# 按行计算均值（axis=1表示行，axis=0表示列）
stock_means = np.mean(close_array, axis=1)  
# 结果：[31.2, 50.8, 20.28]
```

**索引和切片**：快速提取子集，比列表更灵活。 示例：取股票 1 的后 3 天收盘价

```python
stock1_last3 = close_array[0, 2:]  # 第0行（股票1），第2列及以后（后3天）
# 结果：[30.8, 31.5, 32.0]
```

**向量化操作**：无需循环，直接对整个数组运算，速度极快。 示例：计算所有股票的日收益率（相比列表循环，效率提升 10 倍以上）

```python
# 向量化计算：(今日 - 昨日)/昨日（除第一列外）
returns = (close_array[:, 1:] - close_array[:, :-1]) / close_array[:, :-1]  
# 结果为3行4列的数组（3只股票，4天收益率）
```

**高性能**：底层用 C 语言实现，处理百万级数据时，速度远超纯 Python 代码（比如计算 1000 只股票的年收益率，Numpy 只需 0.1 秒，列表循环可能需要 10 秒）。

## 五、Pandas

如果说 Numpy 是 “数值计算引擎”，Pandas 就是 “金融数据处理的瑞士军刀”—— 它基于 Numpy 构建，提供了更直观的数据结构（Series 和 DataFrame），完美适配股票、基金等时间序列数据的处理。

**Series（一维标记数组）** ：带 “索引” 的一维数组，适合记录 “单变量的时间序列”（如一只股票的每日收盘价、一个因子的每日值）。 示例：某股票的收盘价序列

```python
import pandas as pd
# 索引为日期，值为收盘价
close_series = pd.Series(
    [30.5, 31.2, 30.8, 31.5, 32.0],
    index=pd.date_range("2023-10-01", periods=5)
)
# 结果：
# 2023-10-01    30.5
# 2023-10-02    31.2
# 2023-10-03    30.8
# 2023-10-04    31.5
# 2023-10-05    32.0
# dtype: float64
```

Series 的优势是 “索引对齐”—— 比如计算收益率时，自动按日期匹配，无需手动对齐时间。

**DataFrame（二维表格数据）** ：带 “行索引 + 列名” 的二维表格，适合记录 “多变量的时间序列”（如多只股票的收盘价、一只股票的多因子值）。 示例：3 只股票的 5 日收盘价表格

```python
# 行索引=日期，列名=股票代码，值=收盘价
close_df = pd.DataFrame(
    [
        [30.5, 50.2, 20.1],
        [31.2, 50.5, 19.8],
        [30.8, 51.0, 20.0],
        [31.5, 50.8, 20.5],
        [32.0, 51.5, 21.0]
    ],
    index=pd.date_range("2023-10-01", periods=5),
    columns=["600036.SH", "000858.SZ", "601318.SH"]
)
```

DataFrame 的核心功能：

-   快速筛选：`close_df["600036.SH"]`取单只股票数据；
-   按行 / 列运算：`close_df.mean(axis=1)`计算每日平均收盘价；
-   缺失值处理：`close_df.fillna(method="ffill")`用前值填充缺失的股价；
-   合并数据：`pd.merge(df1, df2, on="date")`按日期合并因子和价格数据。

### Pandas 在量化中的高频用法

-   读取金融数据：`pd.read_csv("stock_data.csv")`读取本地数据，`pd.read_excel("fund_data.xlsx")`读取 Excel 数据；
-   时间序列处理：`close_df.resample("W").mean()`将日数据转为周数据（周均值）；
-   因子计算：`close_df.pct_change(5)`计算 5 日收益率（一行代码替代滑动窗口循环）；
-   策略回测：结合条件语句，快速生成买卖信号（如`close_df["signal"] = np.where(close_df["600036.SH"] > 32, 1, 0)`）。

## 六、提示

对新手来说，学习的关键是 “边学边练”：先用列表、字典处理小批量数据，再用 Numpy 提升计算效率，最后用 Pandas 处理真实的金融数据（如从 Tushare、聚宽等平台获取股票数据，尝试计算一个简单的动量因子）。
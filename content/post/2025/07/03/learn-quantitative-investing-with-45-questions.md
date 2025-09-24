---
layout:     post
title:      "Learn Quantitative Investing with 45 Questions"
subtitle:   "Learn Quantitative Investing with 45 Questions(English Version)"
date:       2025-07-03
author:     "Xiangdi Wu"
image:      "/img/background.webp"
description : "This article uses 45 questions to help investors and quantitative beginners understand the fundamental concepts of quantitative investing. The content covers various aspects including the basic concepts of quantitative investment, strategy construction, risk management, and practical applications, presented in an easy-to-understand manner. By reading these articles, you will also gain insights into the importance and future prospects of quantitative investing in modern financial markets."

tags:
    - Quant

categories: [ Quant ]
URL: "/2025/07/03/learn-quantitative-investing-with-45-questions-english"
---

# Q1: Similarities and Differences Between Quantitative Investment and Discretionary Investment?

Broadly speaking, **Quantitative Investment** is an investment methodology based on data, centered around models, and often utilizing programmatic trading as a tool.

1. **Data-driven:** Generally, more data points and more structured data are more conducive to modeling. If an event has never happened historically or has only occurred a few times, it is difficult to find suitable data for training. "Patterns" derived from past experiences may not be effective in such scenarios.
    
2. **Model-centric:** Whether it's early linear models based on financial logic or later machine learning and deep learning models, the essence remains the same – building models fundamentally grounded in data.
    
3. **Often uses programmatic trading as a tool:** "Programmatic trading" is a tool. Both discretionary and quantitative investors, whether institutional or individual, can evaluate and use this tool based on their specific circumstances. In fact, pioneers of quantitative investing like Edward Thorp and early practitioners like Simons operated in an era when computer technology was less advanced, often relying on manual methods like phone orders. Even today, quantitative investment doesn't necessarily mean fully automated execution; for less liquid instruments – some options trades by D. E. Shaw (a renowned hedge fund) are still executed via phone inquiry and order placement.
    

As an investment methodology, quantitative investment, like discretionary investment, is fundamentally about **price discovery** : capturing market mispricings, better reducing information asymmetry, and preventing price distortions. The two approaches **arrive at the same destination by different routes** ; they are not diametrically opposed. They uncover effective market prices at different cycles and levels, merely employing different implementation methods – the former focuses on public, structured data, while the latter emphasizes deep fundamental research. Both methodologies are important participants in mature markets and are indispensable components.

Regardless of the investment method chosen, achieving consistently superior long-term excess returns requires grasping the market's intrinsic patterns. This fundamentally tests the depth of one's market understanding. Quantitative investment, however, places greater emphasis on **effectively combining deep market insights with cutting-edge scientific technology** .

Generally, quantitative investing excels at capturing short-term market price information and correcting short-term price deviations. As the investment horizon lengthens, discretionary investment, with its deep fundamental research, tends to hold a relative advantage.

Taking long-only equity strategies as an example: Both discretionary and quantitative approaches involve **active management** of the portfolio – aiming to achieve market returns while generating excess returns above the market. Both can be analyzed using standardized fund performance metrics such as the Sharpe ratio, return-to-drawdown ratio, and time to recover from maximum drawdown.

  

# Q2: Is Programmatic Trading Exclusive to Quantitative Investment?

When discussing trading tools, the term "quantitative trading" often appears but can be misleadingly interpreted as "trading of quantities," creating definitional ambiguity. In reality, quantitative investment may also employ manual trading. To avoid confusion, the more precise term "programmatic trading" is preferable.

**Programmatic trading** (or automated trading), as opposed to manual trading, refers to trading tools that use programmed automation for decision-making and execution. This enables simultaneous trading across thousands of assets—a feat impossible for manual trading.

Trading instruments like securities and futures have evolved through three stages: traditional trading, electronic trading, and programmatic trading. Before 1965, all trading activities—including exchange matching—relied entirely on human effort. Technological innovations in the 1960s, particularly in communications, propelled capital market development (including futures markets). The emergence of telegraphs liberated futures trading from geographical constraints, while telephones further reduced communication time between investors, members, and exchanges. With the proliferation of computer technology, exchanges worldwide transitioned to computerized order matching.

**Quantitative investment doesn't necessarily rely entirely on programmatic trading.** In its early development, manual order placement was common—for instance, in the 1970s, Renaissance Technologies' founder James Simons executed futures trades via phone calls to brokers due to limited computer capabilities. Even today, top-tier firms like D. E. Shaw use phone consultations and orders for less liquid instruments (e.g., certain options trades).

As technology advances, programmatic trading—by enabling rapid opportunity capture and eliminating human error—reduces transaction costs and improves efficiency, making it increasingly popular among investors.

**Crucially, programmatic trading is not strategy-dependent.** Both discretionary and quantitative investors, whether institutional or retail, can evaluate and adopt this tool based on their needs. In the U.S., over 90% of institutional investors utilize programmatic trading, including discretionary leaders like Fidelity (active management) and index giants like Vanguard (passive management).

  

# Q3: What Are the General Steps and Strategy Categories in Quantitative Investment?

Quantitative investment typically involves seven key steps:

1. **Data Collection:** Gathering relevant market data.
    
2. **Data Cleaning:** Processing and filtering raw data to remove errors and inconsistencies.
    
3. **Feature Engineering:** Extracting meaningful predictive variables (factors) from the cleaned data.
    
4. **Model Development:** Building mathematical or algorithmic models to generate trading signals.
    
5. **Portfolio Optimization:** Constructing and weighting the investment portfolio based on model outputs and risk constraints.
    
6. **Backtesting:** Simulating the strategy's performance using historical data.
    
7. **Trade Execution:** Implementing the trades in the live market.
    

Currently, leading quantitative private funds (quant PEs) heavily invest in data collection, though achieving truly unique or differentiated data sources is challenging. The subsequent six steps, however, exhibit significant variation and are where a manager's depth of market understanding is truly tested. Over time, as existing strategies become more refined, developing new effective factors becomes increasingly difficult.

While terms like "high-frequency," "T+0," and "price-volume" are often used to describe quant strategies, these lack precision. Globally, quant strategies are generally categorized into three main types:

1. **High-Frequency (HF) Strategies:**
    
    1. HF refers to strategies operating on extremely short time horizons relative to "non-HF" strategies, aiming to profit from bid-ask spreads. Definitions vary slightly, but internationally, the prediction horizon is typically **"under 5 minutes."**
        
    2. **In China's Stock Market:** Due to the T+1 settlement rule and stamp duty, truly high-quality HF strategies have **very limited capacity** . They are generally unsuitable for managing external investor capital via asset management products. Consequently, HF represents a small portion of the market and is not a mainstream strategy. Discussions about foreign HF quant impact primarily focus on the **futures market** (which operates T+0), not stocks. Foreign HF players, like Jump Trading, hold significant advantages in hardware, strategy, and technology in China's futures market.
        
    3. **Important Distinction:** A stock quant strategy with an annual turnover of ~100x implies an average holding period of ~5 days. This is actually **medium-frequency**, not high-frequency.
        
2. **Statistical Arbitrage (Stat Arb) Strategies:**
    
    1. These strategies primarily utilize price and trading volume data, employing mathematical models and algorithms for prediction and risk management. They aim to profit by forecasting the relative price movements of stocks over short-to-medium terms.
        
    2. The models identify stocks trading significantly away from their estimated fair value – buying those deemed undervalued and selling those deemed overvalued. Accumulating these small discrepancies aims to generate relatively stable excess returns.
        
    3. As the excess returns largely stem from analyzing short-to-medium term price and volume patterns, these are often called **"Price-Volume Models".**
        
    4. **Example Mechanism:** If an investor needs to sell a large position quickly, causing a short-term liquidity-driven price drop below fair value (not due to fundamentals), a quant firm might step in to buy. This provides liquidity, helps the seller achieve a better average price, dampens volatility, and allows the quant to profit as the price rebounds. This process improves market pricing efficiency.
        
    5. **Prominent Users:** Renowned global quant funds like Renaissance, D.E. Shaw, Two Sigma, and Citadel primarily use Stat Arb. Most mainstream quant PEs in China also focus on this strategy. Prediction horizons range from intraday to several days, generally **under 10 days** .
        
3. **Fundamental Quantitative Strategies:**
    
    1. These are commonly used by **public mutual funds** in China. Similar to traditional value investing, fundamental quant models collect and process all public company information (financials, operational data, industry data, etc.) to uncover predictive market patterns.
        
    2. Fundamental data updates infrequently (e.g., quarterly reports). Consequently, fundamental quant strategies have longer holding periods, ranging from **several months to several years** .
        
    3. While the longer horizon typically reduces the _level_ of excess returns achievable compared to shorter-term strategies, it significantly **increases the strategy's capacity** (the amount of capital it can effectively manage).
        

**Beyond strategy execution, programmatic trading:**

1. **Enhances market efficiency:** Rapidly corrects pricing deviations, aligning instrument prices closer to intrinsic value.
    
2. **Boosts liquidity:** High-turnover strategies generate continuous limit orders (creation, submission, execution, reporting) matched with ultra-short holding periods, simultaneously creating liquidity demand and supply.
    
3. **Strengthens market stability:** Increased liquidity attracts more participants, creating a virtuous cycle.
    

**Technical & Regulatory Notes:**

- System stability demands excellence in trading interface speed, financial/mathematical theory, and computer science practice.
    
- China's securities regulators established programmatic trading oversight frameworks in 2015 to address potential risks. Key developments include:
    
    - 2019 Securities Law: Mandated reporting to exchanges.
        
    - 2023 Main Board Rules: Formalized reporting systems.
        
    - Sept 1, 2023: CSRC-directed exchanges issued enhanced reporting and management rules to ensure orderly development and market stability.
        

Here's the English translation for the question comparing High-Frequency Trading, Algorithmic Trading, and Market Making:

  

# Q4: Similarities and Differences Between High-Frequency Trading, Algorithmic Trading, and Market Making?

High-frequency trading (HFT), algorithmic trading (Algo), and market making all heavily utilize **programmatic trading tools** . These concepts are based on different classification criteria and exhibit some overlap.

1. **High-Frequency Trading (HFT):**
    
    1. Defined relative to "non-HFT," HFT seeks to profit from market liquidity imbalances and other short-term pricing inefficiencies within extremely short prediction horizons by capturing bid-ask spreads.
        
    2. While specific definitions of the prediction horizon vary slightly among institutions, the international convention generally caps it at **under 5 minutes** .
        
    3. HFT typically employs programmatic trading tools, though rare instances of manual order placement may still exist.
        
2. **Algorithmic Trading (Algo):**
    
    1. While also often involving high-frequency order placement, Algo trading is fundamentally about **execution refinement** .
        
    2. Its primary purpose is to provide **automated trade execution optimized for order fulfillment** (not necessarily direct profit generation). It determines the best execution path, timing, price, and quantity for an order (e.g., splitting large orders into numerous smaller ones).
        
    3. The goal is to execute trades efficiently and smoothly, achieving optimal results (like minimizing market impact and reducing transaction costs). Algo trading represents the evolution of **sophisticated trade execution techniques** .
        
3. **Market Making:**
    
    1. Market makers provide liquidity, acting like the "lubricant" that facilitates market operation. They enable trades, narrow bid-ask spreads, and lower transaction costs, helping counterparties achieve their goals.
        
    2. In mature overseas markets, market makers often receive rebates or incentives from exchanges.
        
    3. Before programmatic trading, market making relied heavily on traders continuously quoting prices manually to earn spreads. With technological advances, programmatic trading has become mainstream for market making, except for certain OTC or highly illiquid instruments, phasing out manual market making.
        
    4. As a **typical passive strategy** , market makers provide liquidity and earn exchange fee discounts/rebates.
        
    5. In US/EU markets, market makers are predominantly HFT firms. Companies using automated market maker systems may be either:
        
        - Exchange-registered market makers (with formal quoting obligations).
            
        - Independent firms solely using market making strategies for profit (without formal quoting obligations).
            
    6. **China Context:** China's market maker system is still in its **early development stages** . Market making mechanisms have been introduced in the interbank market, stock options, commodity options, and exchanges like the NEEQ (New Third Board), STAR Market (Sci-Tech Innovation Board), and Beijing Stock Exchange (BSE).
        

**Key Similarities & Differences:**

| Feature           | High-Frequency Trading (HFT)                   | Algorithmic Trading (Algo)       | Market Making                           |
| :---: | :---: | :---: | :---: |
| **Core Purpose**  | Profit from ultra-short-term inefficiencies    | Optimize trade execution         | Provide liquidity & earn spread/rebates |
| **Primary Goal**  | Direct profit generation                       | Efficient order execution        | Facilitate trades & earn spread/rebates |
| **Time Horizon**  | Extremely short (<5 min)                       | Varies (can be short or long)    | Continuous quoting                      |
| **Risk Profile**  | Actively seeks pricing risks                   | Minimizes execution risk         | Manages inventory risk                  |
| **Strategy Type** | Active                                         | Execution technique              | Passive/Liquidity provision             |
| **Overlap**       | Often uses Algo tools; Can _be_ a Market Maker | Tool used by HFT & Market Makers | Often implemented via HFT/Algo          |
| **Key Tool**      | Programmatic Trading                           | Programmatic Trading             | Programmatic Trading                    |
| **China Status**  | Active in Futures (T+0)                        | Widely used                      | Early development stage                 |

**In essence:** Programmatic trading is the common _tool_ . HFT defines a _time horizon and profit motive_ . Algo trading defines an _execution methodology_ . Market making defines a _functional role_ (liquidity provision). A firm can be an HFT market maker using sophisticated algorithmic execution.

  

# Q5: What is Turnover Rate? What is the Relationship Between Turnover Rate and Performance?

**Turnover Rate** (also known as **Portfolio Turnover** or **Holding Turnover Rate** ) measures the frequency with which securities in an investment portfolio are bought and sold over a specific period. It gauges the trading activity level of the portfolio. Within the industry, it commonly refers to the **Annual Bilateral Turnover Rate** , calculated as:

**Turnover Rate = (Total Sell Value + Total Buy Value) / Assets Under Management (AUM)**

The relationship between fund turnover rate and fund performance has been widely discussed. For instance:

- Norde FOF Management Department analyzed the relationship between turnover rates and performance for partial-equity hybrid funds from early 2009 to mid-2018.
    
- Guojin Securities Research Institute also studied samples of actively managed equity funds from 2010 to the first half of 2021.
    

Their key findings are:

1. **Market Context Matters:** For most funds, adjusting turnover rates according to different market environments is common practice. **High-turnover funds tend to outperform low-turnover funds** during periods of rapid market style shifts and frequent industry rotations.
    
2. **Optimal Level Exists:** Portfolio adjustments generally contribute positively to returns. However:
    
    1. Excessively aggressive (very high) turnover frequency does not yield the highest returns.
        
    2. Excessively conservative (very low) turnover frequency misses significant opportunities, leading to suboptimal returns.
        
    3. **Maintaining a moderate turnover rate is key to achieving the best long-term results.**
        

Turnover rate is a relative concept. It is a **natural outcome** of the investment process, not a target in itself. What truly matters is whether stock replacements contribute positively to fund NAV growth or drawdown control. When selecting funds, investors should focus on whether the turnover rate is:

- Compatible with the investment methodology.
    
- Compatible with the fund's size (AUM).
    

**Quantitative Investment Context:**

- Quant strategies excel at correcting medium-to-short-term price deviations, naturally leading to **relatively higher turnover rates** . This aligns with their methodology – capturing short-term market pricing signals, holding hundreds to thousands of stocks (breadth focus), and predicting future price direction based on statistical patterns in vast datasets.
    
- Skilled managers avoid low-probability bets, focusing instead on **compounding small gains** . By capturing mispricings over medium/short horizons, they aim to **convert turnover into returns** .
    
- Currently, **medium-term strategies** (annual turnover ~30-50x) dominate mainstream quant private fund products in China, while short-term strategies are gradually declining.
    
    - _Example:_ An annual turnover of 50x implies an average holding period of ~10 days – classifying it as **medium-frequency** , not high-frequency.
        
- With the industry surpassing the trillion RMB (CNY) mark in AUM, quant managers prioritize turnover rates compatible with their current scale. This demands higher capabilities in:
    
    - Integrated team research strength
        
    - Depth of underlying strategy accumulation
        
    - Refinement of research and investment processes
        
- Industry observation suggests that **sufficiently deep medium-term strategy accumulation** enables both **significant capacity** and the delivery of **relatively strong excess returns** for clients.
    

  

# Q6: What Factors Affect Excess Return Performance?

**"Excess Return"** refers to the portion of a fund's return that exceeds its benchmark over a specific period.

1. **Calculating Excess Return: Two Methods**
    
    1. **Method 1: Excess Return = Fund Return - Benchmark Return**
        
        - This subtractive method is common but less rigorous. It tends to **overestimate** excess return in bull markets and **underestimate** it in bear markets.
            
    2. **Method 2: Excess Return = (Fund Return / Benchmark Return) - 1** (Also known as **Relative Return** )
        
        - _Example:_ You invest ¥10,000 in Fund A at year-start; it's now worth ¥11,000. Had you invested in the benchmark index instead, it would be worth ¥10,500. Relative Return = (11,000 / 10,500) - 1 = 4.76%.
            
        - This method is considered **more accurate and fair** , and is the one we currently use.
            
2. **External Factors Affecting Excess Return Performance:**
    

3. Excess return performance is significantly influenced by the market environment:
    
    - **Favorable Environments:** Quant managers typically generate stronger excess returns when markets exhibit:
        
        - High trading volume
            
        - High volatility
            
        - Outperformance of small/mid-cap stocks
            
        - Strong performance by high-liquidity growth stocks
            
    - **Challenging Environments:** Quant managers often struggle to generate excess returns during:
        
        - **Periods of Sharp Style Shifts ("Quant Quakes"):**
            
            - Events historically unprecedented or extremely rare make it difficult for quant models trained on past data to adapt (e.g., US markets in Aug 2007 & Mar 2020, the latter due to COVID-19).
                
        - **"Narrow Market Rallies" (e.g., "1/9 Markets"):**
            
            - Only a small number of stocks rise while most decline. Quant strategies' inherent diversification becomes a weakness in this scenario, often underperforming skilled discretionary managers (e.g., China A-shares in H1 2017).
                
    - **Natural Cyclicality:** Due to these external factors, excess return exhibits inherent volatility and cyclicality:
        
        - **α Cycle (~Quarterly):** Driven by rapid market style shifts, periods of excess return drawdown lasting several months are normal for equity quant models.
            
        - **β Cycle (~2-3 Years):** Investors in long-only equity strategies are generally advised to hold for **3+ years** to mitigate the impact of short-term market fluctuations.
            
    

4. **Internal Factors Affecting Excess Return Performance:**
    
    1. The gradual **decay of excess returns** over the long term is an irreversible trend. This is particularly pronounced as China's A-share market efficiency improves and industry competition intensifies, making sustained stable excess returns increasingly difficult. This challenge faces the entire asset management industry and is an inevitable result of market institutionalization.
        
    2. For long-only equity products, long-term returns hinge on **excess returns** , which are fundamentally linked to the manager's **comprehensive investment capabilities** – these internal factors are the **core determinants** .
        
5. **The Future: Sustaining Excess Returns**
    

6. Excess return is the **bedrock of active management** . The challenge for asset managers is consistently outperforming the market across different environments to deliver long-term client value. Future efforts should focus on two dimensions:
    
    - **Breadth: Diversifying Sources of Alpha**
        
        - Continuously enhance the variety of instruments and strategies.
            
        - Leverage deep market understanding to invest in research for **"full-cycle, multi-strategy, multi-asset"** capabilities, building a reserve of low-correlation strategies for diversified alpha sources.
            
        - Beyond full-cycle price-volume factors, deepen research into fundamental factors and explore alternative data factors (a relatively untapped "blue ocean" in China compared to mature overseas markets).
            
    - **Depth: Systematic and Granular Processes**
        
        - Sustain high investment in **intellectual capital and computing power** .
            
        - Continuously enhance the **systematization and granularity** of the research and investment process.
            
        - China's quant industry has entered a new phase of **high-quality development** , demanding all-around excellence. Optimization is required across all facets: investment process, operations/service, client communication, and brand building.
            
    

  

# Q7: What Impact Does Quantitative Investment Have on the Stock Market?

Since 2013, the share of quantitative investment in China's stock market has steadily increased, with particularly rapid growth in quant institutional AUM between 2018-2021, drawing significant market attention. As quant investment emerged relatively late in China and is inherently complex, its impact warrants exploration:

**A. Enhances Market Liquidity (Short-to-Medium Term) and Pricing Efficiency (All Horizons)**

The essence of quantitative investment is **price discovery** , identifying the fair price of assets across different time horizons. Quant institutions excel at providing **short-to-medium-term liquidity** :

- **Long-Term Horizon (Fundamentals):**
    
    - Primarily discovers fair prices by mining company fundamental data, similar to fundamental research-driven discretionary investing.
        
    - Some quant private funds actively participate in private placements (PIPEs), Global Depository Receipts (GDRs), etc., improving **medium-to-long-term pricing efficiency** , creating a favorable fundraising environment for quality companies, and supporting the real economy.
        
    - With the **full implementation of the registration-based IPO system** , the quality of listed company disclosure data is improving, enabling quant to more efficiently explore intrinsic fundamental value, optimize fundamental quant models, and enhance **long-term pricing efficiency** .
        
- **Medium-Term Horizon (Days to Weeks):**
    
    - Discovers fair prices (typically 1-10 days) by analyzing market transaction data, news, and alternative data.
        
    - _Example:_ Large institutional investors rebalancing sizable positions over multiple days can impact mid-term liquidity, price, and volatility of individual stocks. Quant strategies, analyzing market microstructure, may identify stocks temporarily undervalued due to liquidity shocks (not fundamentals) and start buying. This provides liquidity to the rebalancing institution, facilitating better execution prices for them, **reducing individual stock volatility** , while the quant profits as the price normalizes.
        
- **Short-Term Horizon (Microstructure):**
    
    - Analyzes stock microstructure to find short-term fair prices and provide **short-term liquidity** .
        
    - In the US market (where retail trading is <10%), quant institutions provide over 90% of short-term liquidity, often compensated by exchanges via rebates.
        
    - **China Context (A-Shares):** Market structure differs. Even with accelerating institutionalization, retail investors still account for ~50% of trading volume, providing substantial natural liquidity. Thus, the _immediate need_ for quant to provide short-term liquidity is less acute than in the US. However, as the registration system deepens (increasing small/mid-cap listings on STAR/ChiNext) and institutionalization progresses, retail share will gradually decline. Quant can then leverage stock correlations to provide liquidity to less liquid stocks, which is fundamental to asset valuation.
        

**B. Helps Reduce Overall Market Volatility**

Research and empirical evidence show that as quant strategies gain market share, **overall market volatility tends to decrease** :

- **Mechanism:** Quant strategies buy undervalued and sell overvalued stocks when prices deviate from fair value across short, medium, and long horizons. This price discovery makes markets more efficient. Data indicates increased quant participation correlates with lower market-wide volatility.
    
- **Empirical Evidence:**
    
    - Overseas (e.g., US 2000-2018): Rising quant share coincided with declining volatility.
        
    - China A-Shares: Recent years show a gradual decline in volatility (e.g., ~13% annualized in H1 2023), partly attributable to the growing presence of mature investors, including quant institutions.
        
- **Stabilizing Role of Quant Long-Only:**
    
    - Quant long-only strategies (the largest segment in China quant AUM) typically hold highly diversified portfolios and operate near full capacity. Daily buying and selling volumes are generally balanced, avoiding creating net market-wide buying or selling pressure.
        
    - During market turbulence, quant long-only products often act as **stabilizing forces** .
        
- **Mitigating Extreme Moves via Mean-Reversion:**
    
    - Prevalent mean-reversion factors within quant models trigger trades against excessive price moves (up or down), dampening volatility. Empirical evidence shows quant models tend to sell stocks that have risen too sharply and buy those that have fallen too steeply.
        
    - This reduces opportunities for momentum-chasing strategies ("buy high, sell higher" / "sell low, buy lower"), further enhancing market efficiency.
        
    - **Debunking the "Herd Behavior" Myth:** The notion that quant trading leads to convergence is unfounded. If all quant firms traded identically, it would create mispricings, offering arbitrage opportunities for others. Instead, diverse quant strategies act as a **counter-balancing "shock absorber"** in the market.
        

**Conclusion:**

Quantitative stock selection models play a **positive role** in the A-share market by enhancing liquidity, improving pricing efficiency, and reducing overall volatility. Concurrently, as the A-share market matures, market efficiency accelerates, volatility further decreases, and the difficulty of generating excess returns increases significantly. This challenge confronts the entire asset management industry and is an inevitable outcome of the market's institutionalization process.

  

# Q8: How to Understand and Differentiate Between Index Enhancement and All-Market Quantitative Stock Selection Products?

  

Both Index Enhancement and All-Market Stock Selection fall under the category of **Quantitative Long-Only (QLO)** products. They employ quantitative stock selection models to **actively manage** the investment portfolio. Generally, the underlying model framework for product lines like QLO and Quant Hedge is shared. Differentiation is achieved by applying different **stock selection constraints** and deciding **whether to hedge** on the same core "quantitative stock selection" model, catering to investors with varying risk preferences.

**Why Did Index Enhancement Precede All-Market Stock Selection in China?**

In the early stages of quant development in China, channels and investors were far less familiar with and accepting of quantitative methodologies than they are today. Quant firms also lacked long track records of live performance. In contrast, promoting **"Index Enhancement"** products was significantly easier:

1. **Existing Foundation:** Public mutual funds had already laid some groundwork in investor education for index enhancement products.
    
2. **Transparent Attribution:** Index enhancement products can be decomposed into **Index Return (β) + Excess Return (α)** . This structure makes tracking, performance attribution, and peer comparison much more intuitive for investors. Metrics like the **"Sharpe Ratio of Alpha"** became particularly useful for evaluating a manager's skill.
    

- **Beta:** Comes from passive tracking of an index (e.g., broad market indices like CSI 300, CSI 500, CSI 1000, or sector/thematic/other indices).
    
- **Alpha:** Comes from active management – predicting the relative returns of individual stocks over different horizons and selecting those likely to outperform the index to generate excess return.
    

Given the initial low investor acceptance of pure quant methodologies, the intuitive comparison and tracking of index enhancement products led quant firms to incorporate **index tracking error constraints** into their model optimizers, creating dedicated index enhancement product lines (e.g., CSI 300 Enh, CSI 500 Enh, CSI 1000 Enh).

**Why Are Quant Hedge Funds Now Pushing "All-Market Stock Selection" Products?**

The landscape shifted significantly:

1. **Scale & Acceptance:** Quant hedge fund AUM surpassed ¥1 trillion in H2 2021. Investor understanding and acceptance of quant methodologies grew, while competition intensified.
    
2. **Market Efficiency & Alpha Decay:** As China's A-share market became more institutionalized and efficient, generating alpha became harder – a natural consequence of competition.
    
3. **The CSI 500 Bottleneck:** The mainstream CSI 500 Enhancement strategy illustrates the challenge:
    
    1. To control tracking error, managers must hold a high proportion of CSI 500 constituents.
        
    2. CSI 500 constituents represent only ~15% of total A-share trading volume.
        
    3. As quant AUM grew, their trading share _within_ the CSI 500 increased disproportionately compared to other stocks.
        
    4. This concentrated quant activity accelerated **alpha decay specifically within the CSI 500 universe** , significantly impacting the excess returns achievable by CSI 500 Enh products.
        
4. **Investor Preference:** Many investors with reasonable risk tolerance prioritize **absolute return** .
    

**The Rise of All-Market Stock Selection:**

Driven by client demand for better absolute returns, leading quant hedge funds have recently launched **"All-Market Stock Selection"** product lines. These products aim to:

- **Remove Constraints:** Operate without benchmark, style, or sector constraints.
    
- **Maximize Alpha:** Build portfolios based solely on the predicted alpha and liquidity of stocks across the _entire_ market.
    
- **Optimize for Absolute Return:** Target the maximization of absolute returns under practical trading constraints.
    
- **Manage Risk:** Achieve this _without_ meaningfully increasing overall risk or volatility compared to constrained strategies.
    

**Key Differentiators & Advantages:**

| Feature                     | Index Enhancement (e.g., CSI 500 Enh)             | All-Market Stock Selection                                                                         |
| :---: | :---:| :---: |
| **Benchmark**                   | Strictly tracks a specific index (e.g., CSI 500)      | **No benchmark constraint**                                                                            |
| **Stock Universe**              | Primarily constituents of the target index            | **Entire A-share market**                                                                              |
| **Key Constraint**              | **Tracking Error** (limits deviation from index)      | **No Tracking Error Constraint**                                                                       |
| **Style/Industry Exposure**     | Generally constrained to match index characteristics  | **Unconstrained** (can deviate freely)                                                                 |
| **Primary Goal**                | Beta + Maximize Alpha *within index constraints*      | **Maximize Absolute Return** (Unconstrained)                                                           |
| **Alpha Source**                | Alpha signals primarily applied within index universe | Alpha signals applied across **all stocks**                                                            |
| **Liquidity Focus**             | Driven by index liquidity & constraints               | **Direct focus on stock liquidity**                                                                    |
| **Flexibility**                 | Lower                                                 | **Highest**                                                                                            |
| **Theoretical Alpha Potential** | Limited by constraints                                | **Higher** (Can access alpha signals anywhere)                                                         |
| **Volatility Impact**           | Dictated by index + alpha                             | **Not significantly higher than QLO** (Empirical evidence shows marginal increase in vol/MDD is small) |


**Why Unconstrained is More "Natural" and Often Better:**

- **Pure Alpha Capture:** An unconstrained, all-market approach represents the **purest and most natural** application of a quant stock selection model. The portfolio composition can align most closely with the model's raw alpha signals.
    
- **Constraint Cost:** Imposing constraints (like tracking an index) inherently **restricts freedom** and **sacrifices potential alpha** . The model cannot fully express its strongest views across the entire market.
    
- **Risk Impact Managed:** Empirical evidence in the China market suggests that for long-only quant products (the dominant strategy), **removing style/risk factor constraints (like size, value, liquidity) does not lead to a significant increase in portfolio volatility or maximum drawdown** , while delivering a meaningful improvement in long-term absolute returns. The **marginal benefit (higher return) outweighs the marginal cost (slightly higher potential vol)** .
    
- **Track Record Note:** While live track records for all-market selection products are currently shorter than those for index enhancement products, the historical performance of a firm's _index enhancement_ strategies (assuming the same core alpha model is used) remains a crucial reference point for assessing the manager's capability.
    

**In essence:** Index Enhancement products were a necessary stepping stone in China's quant evolution, offering easier adoption and clearer benchmarking. All-Market Stock Selection represents the evolution towards harnessing the full, unconstrained potential of quant models to maximize absolute returns, made viable by growing investor sophistication, market scale, and the diminishing returns within constrained universes.

  

# Q9: What is a Benchmark? How to Set a Performance Benchmark for All-Market Stock Selection Products?

A **Performance Benchmark (Benchmark)** is the primary reference target for evaluating a fund's future performance. It serves two key purposes:

1. **Ex-ante:** Communicates the expected risk-return profile to investors.
    
2. **Ex-post:** Acts as a yardstick for performance attribution and evaluation analysis.
    

Generating **excess return (Alpha)** over the benchmark is the core competency of active managers. Consistently outperforming the market across different environments to deliver long-term client value is the fundamental challenge for asset managers.

**Setting Benchmarks for All-Market Stock Selection Products:**

- **Index Enhancement Products:** These have a natural benchmark – the specific index they track (e.g., CSI 500). Their return is explicitly decomposed as **Index Return (β) + Excess Return (α)** . Low tracking error makes performance observation, attribution, and peer comparison intuitive (e.g., using the "Sharpe Ratio of Alpha" to assess manager skill).
    
- **All-Market Stock Selection Products:** These operate **without benchmark, style, or sector constraints** . Portfolios are constructed solely based on predicted stock-level Alpha and liquidity, aiming to **maximize Alpha expression** and absolute return.
    

**How to Choose a Benchmark for All-Market Selection?**

While unconstrained in model construction, a benchmark is still needed for evaluation and communication. Common choices are:

1. **Wind All-A Index (881001.WI):** The most logical choice. It represents the **entire A-share market** (all stocks listed on Shanghai and Shenzhen exchanges), aligning perfectly with the product's unrestricted universe.
    
2. **CSI 500 or CSI 1000 Index:** Often used for practical reasons:
    
    1. All-Market portfolios typically hold 1000-1500 stocks.
        
    2. Due to historically stronger Alpha signals and better liquidity in the small/mid-cap segment, these portfolios often have a higher _weighting_ (both in number of holdings and allocation) towards small/mid-cap stocks.
        
    3. Using CSI 500 or CSI 1000 provides a **familiar reference point** for investors accustomed to index products and facilitates easier **peer comparison** (as many firms report relative to these), even though it's not a perfect fit.
        

**All-Market Selection vs. Discretionary Long-Only: A Closer Analogy**

In today's market characterized by significant stock dispersion (opportunities exist across large and small caps), **All-Market Quant Selection products are more directly comparable to Discretionary Long-Only products** than Index Enhancers are:

- Both **lack a formal benchmark** .
    
- Both are **pure long-only equity strategies** .
    
- While their _sources_ of Alpha differ (systematic model vs. fundamental research), their performance can be evaluated using **standard absolute return metrics** like the Sharpe Ratio, Maximum Drawdown, and Calmar Ratio.
    

**Is it an "Either/Or" Choice Between All-Market and Index Enhancement?**

**No.** Both "All-Market Stock Selection" and "Index Enhancement" belong to the broader **Quantitative Long-Only (QLO)** category:

- Both typically maintain **near-full equity exposure** (no tactical asset allocation).
    
- Both aim to capture **market return (Beta) + generate excess return (Alpha)** through active quantitative management.
    
- They serve **different investor needs and risk preferences** , offering distinct allocation value:

|Consideration|Index Enhancement (e.g., CSI 500 Enh)|All-Market Stock Selection|Recommendation|
| :---: | :---: | :---: | :---: |
|**Strong Conviction in a Specific Index**|✓ (e.g., if CSI 500 is expected to strongly outperform)|✗ (May underperform a surging specific index)|Choose Index Enhancement|
|**High Sensitivity to Alpha Volatility**|✓ (Tracking error constraint dampens _relative_ vol)|✗ (Absolute return vol may feel higher)|Choose Index Enhancement|
|**Primary Goal: Maximize Long-Term Absolute Return**|✗ (Constrained Alpha potential)|✓ (Unconstrained Alpha potential)|**Choose All-Market Selection**|
|**Desire for Clear Benchmark Attribution**|✓|✗|Choose Index Enhancement|

**In essence:** The choice depends on the investor's **risk tolerance and primary objectives** . Index Enhancement offers clearer benchmarking and potentially smoother _relative_ performance but sacrifices some Alpha potential. All-Market Selection maximizes the pursuit of absolute Alpha and long-term return but forgoes a tight benchmark anchor. They are **complementary tools** within the quant equity toolkit. For most investors seeking the best _long-term absolute returns_ , All-Market Selection is the preferred vehicle, leveraging the full power of the quant model unshackled by constraints.

  

# Q10: Is Quantitative Investing Equivalent to Hedging? Expected Returns and Timing for Market-Neutral Products

Many investors conflate "quantitative" and "hedged," but hedging is not exclusive to quant managers—discretionary managers can also hedge market systemic risk and sector beta. Common hedging tools in China include stock index futures, options, securities lending, and total return swaps.

**Stock Market-Neutral** refers to a product strategy that holds a long basket of stocks while shorting another basket or stock index futures to generate returns independent of market direction. While most domestic market-neutral products use quantitative stock selection, some employ discretionary methods. Quant neutral products use quantitative models to hold a stock portfolio and hedging tools to achieve near-zero exposure to market beta, primarily capturing excess returns (alpha).

Most domestic asset managers use stock index futures for hedging, so this section focuses on these products:

**I. Factors Influencing Market-Neutral Returns & Long-Term Return Projections**

Key return drivers:

- **Basis**: The discount/premium of index futures vs. the spot index (hedging cost)
    
- **Excess returns** of the stock portfolio over the benchmark
    

Net return = (Excess return - Hedging cost) × Capital efficiency.

CMB Private Banking Department’s report _Hedge Fund Investment Timing and Return Expectations_ projects long-term post-fee returns:

- Assume top managers generate ~12% stock excess returns.
    
- Subtract ~2.5% hedging cost and apply 85% average position utilization → 8% pre-fee return.
    
- After fees (1.5% management + 0.25% custody + 0.25% service) and 20% performance fee → **~4.8% annualized post-fee return** . An additional ~0.5% subscription fee may apply.
    

While standout performers exist, long-term expectations should remain realistic. As China’s market matures and efficiency improves, excess returns will inevitably decay. The projected 4-5% return may decline further.

**II. Investment Timing for Market-Neutral Products**

Performance depends on:

1. Manager’s alpha capability
    
2. Hedging costs (timing-dependent)
    

Optimal entry considers:

- **Favorable alpha environments**: High volume, high volatility, small/mid-cap rallies, liquid growth stock outperformance (e.g., quant thrives here).
    
- **Unfavorable alpha environments**: Rapid style shifts or "1/9 markets" (few rising stocks, quant diversification becomes a weakness).
    
- **Low/negative hedging costs**: When index futures trade near/above fair value (low contango or backwardation).
    

**Basis dynamics note**:

- Hedging cost is fixed at trade inception; basis fluctuations cause short-term NAV volatility but don’t alter final returns.
    
- Sharp contango narrowing causes immediate drawdowns but creates entry opportunities for new capital.
    
- Existing investors experience temporary losses but recover as basis normalizes.
    

**Conclusion**:

While low/negative basis provides tactical opportunities, **manager selection and alpha sustainability matter more long-term** . Investors should align expectations with market maturation: 4-5% returns are increasingly challenging to sustain.

  

# Q11: What is Basis and How Does It Affect NAV Volatility in Market-Neutral Products?

Since the launch of the CSI 300 stock index futures (IF) on April 16, 2010, the term "**Basis** " has frequently appeared in reports and roadshows for market-neutral products. What exactly is Basis, and how do its movements impact the Net Asset Value (NAV) volatility of these products?

**Stock Index Futures** are futures contracts where the underlying asset is a stock price index. China currently has four major index futures:

- **IF**: Tracks the CSI 300 Index
    
- **IH**: Tracks the SSE 50 Index
    
- **IC**: Tracks the CSI 500 Index
    
- **IM**: Tracks the CSI 1000 Index (Launched July 22, 2022)
    

**What is Basis?**

- Basis is the **price difference between the spot (cash) index and the corresponding index futures contract** .
    
- It reflects the dynamic relationship between futures and spot prices.
    
- **Negative Basis (Futures Premium / Backwardation):** Futures Price > Spot Price → _Benefits_ hedged products.
    
- **Positive Basis (Futures Discount / Contango):** Futures Price < Spot Price → _Costs_ hedged products.
    

**Basis as Hedging Cost & Risk:**

Basis represents the **hedging cost** (or potential benefit) that all market-neutral products primarily using index futures for hedging must bear. While recent basis levels (especially contango) have been relatively small and stable, it remains a key driver of NAV volatility alongside manager alpha volatility.

**How Basis Impacts NAV Volatility:**

1. **Hedging Cost is Locked at Initiation:** The cost/benefit implied by the basis level is effectively locked in when the futures hedge is established.
    
2. **Interim Volatility During Holding Period:**
    
    1. Basis doesn't stay constant; it **converges** (moves towards zero) or **diverges** (moves away from zero) over time.
        
    2. This convergence/divergence creates **unrealized gains or losses ("floating P&L")** on the short futures position.
        
    3. These unrealized P&L fluctuations cause **interim NAV volatility** for the market-neutral product.
        
    4. _Crucially, this is temporary mark-to-market volatility; it does not change the original locked-in hedging cost realized at initiation._
        
3. **Rolling Futures Contracts (Roll Yield):**
    
    1. Futures contracts are not typically held to expiration. Managers **"roll"** positions – closing expiring contracts and opening new ones in further months – to maintain the hedge.
        
    2. The basis level _at the time of rolling_ determines the cost/benefit for the _next_ period. Skilled managers can practice **basis management** by analyzing basis trends and timing rolls optimally to improve long-term hedging efficiency.
        

**Basis, Alpha, and Product Performance:**

- Both **alpha generation** and **hedging costs (basis)** are influenced by market conditions and exhibit cyclicality.
    
- While market-neutral products have low correlation to overall equity markets due to hedged beta, they _can_ experience significant drawdowns:
    
    - During periods of **alpha drawdown** (e.g., rapid style shifts).
        
    - When **contango narrows sharply** (reducing the unrealized gain on the short futures position or increasing unrealized loss).
        

**Conclusion & Investor Consideration:**

Quantitative market-neutral products retain allocation value. However, given the secular decline in stock alpha and the challenge for many investors to professionally analyze basis trends and time entries, investors with **lower risk tolerance and high sensitivity to drawdowns** might find suitable **multi-strategy products** a better solution.

**Multi-Strategy Products as an Alternative:**

- These combine multiple underlying strategies, each generating **independent Pure Alpha** .
    
- Typically use a **quant market-neutral strategy as the core ("anchor")** .
    
- Add several **low-correlation, return-enhancing ("offensive") strategies** .
    
- Allocate risk budgets, weights, and position sizes holistically based on **target volatility** , strategy correlations, and risk contributions.
    
- This scientific construction aims to **diversify return sources** , **improve the risk-adjusted return profile (Sharpe Ratio)** , and **enhance the client holding experience** by smoothing returns.
    

  

# Q12: What is Annualized Volatility? How Does it Differ from Maximum Drawdown?

**Distinguishing and Understanding Annualized Volatility vs. Maximum Drawdown** 

- **Annualized Volatility:** A core component of the **Sharpe Ratio** (Sharpe Ratio = (Annualized Return - Annualized Risk-Free Rate) / Annualized Volatility). This key fund evaluation metric reflects **risk-adjusted return** : how much excess return a fund generates per unit of risk taken. All returns come with associated risk; volatility quantifies the uncertainty of asset returns, reflecting the risk level of a financial asset.
    
- **Maximum Drawdown (MDD):** Defined as "the maximum observed decline in net asset value (NAV) from any peak to a subsequent trough within a selected historical period." Simply put, it's the "largest percentage loss experienced by the product over a specific timeframe."
    
    - _Example:_ A fund launches on Nov 1, 2021. Its NAV reaches a short-term high of 1.2 on Jan 4, 2022. After a market crash, the NAV drops to 0.9 by Apr 26, 2022. The worst-case scenario for an investor buying at the peak (Jan 4) and selling at the trough (Apr 26) would be a loss of 25%: `(1.2 - 0.9) / 1.2 * 100%`. The fund's maximum drawdown during this holding period is 25%.
        

**Annualized Volatility Measures Statistical Variance; Maximum Drawdown Captures the Extremes of Return Distribution**

Both volatility and drawdowns are inherent parts of market dynamics. Looking at major A-share indices from 2007-2021:

- Average Annual Maximum Drawdowns: Wind All-A Index (25%), SSE Composite (24%), CSI 300 (26%), CSI 500 (29%).
    
- The Wind All-A Index experienced a maximum drawdown of 34.37% in the last five years.
    

Drawdown magnitudes vary significantly year-to-year, making entry timing important. However, perfectly avoiding every market downturn is virtually impossible. Numerous factors influence drawdowns in practice, requiring case-by-case analysis.

**Annualized Volatility is a more consistently evaluable and referenceable indicator of an asset management product's risk characteristics.**

- **Annualized Volatility** is a measure of **statistical variance** (standard deviation of returns scaled annually).
    
- **Maximum Drawdown** captures the **extreme tail of the return distribution** . The more data points (i.e., the longer a product exists), the higher the probability of encountering extreme events – meaning the theoretical likelihood of a _new_ maximum drawdown occurring increases over time.
    
- _Implication:_ For a fund with a short track record, a seemingly low historical maximum drawdown might be misleading. If its **annualized volatility is high** , it's statistically likely that its **maximum drawdown will eventually exceed the current record** , given enough time and exposure to market stress.
    

**Target Annualized Volatility is More Predictable Than Uncontrollable Maximum Drawdown**

Examining top-tier hedge funds reveals a pattern: over sufficiently long periods, the **Maximum Drawdown is typically 1.5 times (or more) the Annualized Volatility** .

- **Bridgewater Pure Alpha:** Target Volatility 12%, Actual Volatility ~10%, Historical Max DD 15.5% (occurred in its 20th year).
    
- **Millennium Fund:** Actual Volatility 4.3%, Historical Max DD 7.24% (occurred in 2008, its 18th year).
    

For funds with shorter track records, **using Annualized Volatility to estimate potential future Maximum Drawdown is more meaningful than relying solely on the historical drawdown figure.**

**Practical Significance for Investors and Managers:**

- **For Investors:** Annualized Volatility is a crucial metric for evaluating low-to-moderate risk multi-strategy products. It helps assess risk control effectiveness and return generation efficiency – essentially, **whether expected returns are being achieved with controllable volatility** . Tracking a fund's weekly NAV over 3-6 months is usually sufficient to observe if it adheres to its target volatility without significant deviation.
    
- **For Fund Managers:** Target Annualized Volatility should be set based on the product's risk profile. This target then dictates the **risk budgets and position sizing for underlying sub-strategies** . Achieving this target is a key aspect of active risk management. In contrast, Maximum Drawdown is an _outcome_ that is inherently harder to control directly.
    

**Conclusion:**

Both volatility and drawdowns are intrinsic to market participation. Investors should rationally evaluate fund performance, carefully selecting products aligned with their **risk tolerance, capital characteristics, and investment experience** , based on a clear understanding of these risk metrics. Annualized Volatility provides a more stable and predictable foundation for risk assessment and expectation setting than Maximum Drawdown alone.

  

# Q13: How to Understand the Complexity of Financial Data and the Importance of Data Processing?

  

Generally, quantitative investment can be broadly divided into six stages: **data collection, data cleaning, feature engineering, model development, portfolio optimization, and trade execution** . Currently, leading quantitative hedge funds struggle to achieve significant differentiation in the **data collection** stage. The vast differences lie in the subsequent stages, which test a manager's depth of **market understanding and technical capabilities** .

Taking the **data cleaning and preprocessing** stage as an example: the **quantity and quality of data** directly impact final portfolio performance. Data volume is a key factor constraining the training accuracy and predictive power of machine learning models. Steps in data cleaning and preprocessing typically include:

- Handling missing values
    
- Handling duplicate values
    
- De-extremizing data (removing outliers)
    
- **Data Neutralization** (Eliminating the influence of certain factors – e.g., market capitalization, industry, style – on the investment strategy to enhance its robustness and generalizability).
    
- **Data Standardization** (e.g., converting dates to specific formats).
    

**1. Complexity of Financial Data:**

- **Low Signal-to-Noise Ratio:**
    
    - Financial data contains a high proportion of noise, making it difficult to extract valid signals. Models not properly tuned are prone to learning this "noise." Consequently, quantitative investment places strong emphasis on avoiding overfitting during model development and tuning.
        
    - Processing financial data requires rigorous logic. For example, in China's A-shares, different stocks have different price limit rules. Special handling is needed for events like new listings and stock resumptions after suspensions. Information must be mined, filtered, and combined logically.
        
- **Temporal Monotonicity & Non-Stationarity:**
    
    - Securities trading data are time-series with temporal sequence (time cannot flow backward). Financial markets involve constant competition, causing underlying patterns to change over time (non-stationarity).
        
    - The goal of quantitative methodology is to use historical data to predict the future. Therefore, it is crucial to **avoid look-ahead bias** (introducing future information) and rigorously evaluate historical backtests.
        

**2. Categories of Financial Data:**

**1) By Data Format:**

- **Standardized Data:**
    
    - Common numerical data types like cross-sectional or time-series data. Examples include raw exchange data, raw market feeds, and derived data like prices, volumes, and candlestick charts. Data like minute-by-minute charts or K-line charts seen by retail investors on trading platforms are derived from this raw exchange data. This relatively "clean" data is termed "Standardized Data."
        
- **Non-Standardized Data:**
    
    - Primarily text-based data, including financial news, forum Q&A, sell-side analyst reports, and specialized data from third-party vendors. This data has a high proportion of low-relevance or non-material information, making it more complex than standardized data. It must undergo structuring processes like data cleaning before being used in quant strategy development.
        

**2) By Data Source:**

- **Price-Volume Data:**
    
    - Encompasses all information extractable from market trading behavior. This includes not just asset prices but also derived technical indicators. Categories are:
        
        - _Inter-day Data (Daily Bars):_ E.g., daily K-lines.
            
        - _Intra-day Data (Tick/Timeseries):_ E.g., minute-by-minute data.
            
        - _Tick-by-Tick Data:_ Data for every single trade and order book update. Intra-day data volume can be hundreds to thousands of times larger than inter-day data; tick data volume can be tens of thousands of times larger.
            
- **Fundamental Data:**
    
    - Includes macroeconomic fundamentals, industry chain dynamics, sector trends, and company-specific financial statements (balance sheets, income statements, cash flow statements).
        
    - _Discretionary Advantage:_ Discretionary investors hold a significant advantage in gathering and processing fundamental data. Deep research can uncover non-public, unstructured information (e.g., a company securing or losing a major order, or using satellite imagery to estimate inventory levels at an auto plant based on reflections of specific metals).
        
- **Event-Driven Data:**
    
    - Seeks alpha by predicting underreaction or overreaction to specific events. In finance, an "event" typically refers to "a situation likely to change investor expectations in the short term, significantly impacting a company's fundamentals or its stock price." Examples:
        
        - _Stock Buybacks / Significant Insider Buying:_ Often signals perceived undervaluation (positive alpha signal).
            
        - _Significant Insider Selling:_ Generally perceived as a negative alpha signal.
            
        - _Hype Stocks / Heavily Speculated Stocks:_ Stocks experiencing sudden high volume surges and price spikes without fundamental support often underperform significantly later (good negative alpha factor).
            
- **Alternative Data:**
    
    - "Alternative" is a relative term – data becomes mainstream once widely adopted.
        
    - Currently, it refers to novel data from non-traditional sources used in investment research: ESG data, social media sentiment, satellite imagery, mobile device data, app usage, internet search trends, consumer transaction data, etc.
        
    - _Global Maturity:_ Alternative data research is well-established overseas. Reports (e.g., AIMA & SS&C, AIMA & Bank of America) indicate over 400 active global alternative data providers (vs. ~20 in 1990), with ~50% of asset managers now using it.
        
    - _China Context (Blue Ocean):_ Due to developmental stage differences, alternative data in China faces challenges: high-value data is hard to acquire, easily accessible data is low quality, costs are relatively high, and unstructured data processing tech is less mature. Consequently, it remains a blue ocean. Besides partnering with data vendors, many leading hedge funds are rapidly collecting, accumulating, and exploring alternative data to find diversified and differentiated alpha sources.
        
    - _Examples:_
        
        - _E-commerce Data:_ Category sales data can predict future sales/profits for consumer companies.
            
        - _Commodity Spot/Futures Prices & Inventory:_ Predict future commodity prices and performance of raw material companies.
            

**Conclusion:**

Generally, **more data points and more structured data** are more conducive to modeling for quantitative investment. If a major event has never happened historically or occurred only a few times, "patterns" derived from the past may be ineffective, and finding suitable training data is difficult, impacting confidence. Currently, **price-volume factors** dominate models in leading Chinese quant hedge funds, while research into **fundamental factors** continues intensively. As the quant industry evolves, all factor types are expected to contribute significantly in the future.

  

# Q14: What Are Common Pitfalls in Historical Backtesting?

Quantitative investment research heavily relies on **historical backtesting** . This work involves continuous, iterative refinement of strategies. However, missteps can easily lead to traps, where a strategy that appears flawless in testing incurs losses when deployed with real capital.

The three primary pitfalls in quant research are: **Survivorship Bias, Look-Ahead Bias (Using Future Data), and Overfitting.**

1. **Survivorship Bias:**
    
    1. **Definition:** Mistakenly excluding assets that were delisted or otherwise disappeared from the market during the historical period. Using only the "survivors" (stocks that exist today) inflates backtested returns.
        
    2. **Cause:** Convenience in data handling – using the current universe of stocks for historical testing instead of accurately reconstructing the _actual_ universe available at each historical point in time.
        
    3. **Solution:** Meticulously recreate the historical market environment. The backtest must include _all_ assets that existed and were tradable at each specific historical moment, including those that subsequently failed or were delisted. Never use the current stock list for past periods.
        
2. **Look-Ahead Bias (Using Future Data):**
    
    1. **Definition:** Inadvertently incorporating information that was not available at the time of the simulated historical trade – essentially "time-traveling" with future knowledge. Examples include:
        
        - Using a company's Price-to-Earnings (P/E) ratio _before_ its annual report was officially published.
            
        - Using the closing price _before_ the market close actually occurred.
            
    2. **Cause:** Treating the unknown (future information) as known, artificially boosting backtested performance.
        
    3. **Solution:** Implement a robust **data filtration system within the backtesting environment** . This system must strictly ensure that _only_ information available _up to and including_ the precise simulation time is used. Scrutinize data feeds and calculations to eliminate any potential leakage of future information at the source.
        
3. **Overfitting:**
    
    1. **Definition:** Excessive optimization of a strategy's parameters to fit historical data patterns too closely, resulting in exceptional backtest performance that fails to generalize to unseen, real-market conditions (out-of-sample data). The strategy loses robustness and predictive power.
        
    2. **Cause:** The natural process of "fitting" – fine-tuning and optimizing a strategy's parameters within a defined framework to improve returns and reduce volatility – is essential. However, pushing this too far, especially with too many parameters or insufficient validation, leads to overfitting. The model essentially memorizes historical noise rather than learning generalizable patterns.
        
    3. **Consequence:** Creates deceptively beautiful equity curves in the backtest that are meaningless for future profitability.
        
    4. **Solutions:**
        
        - **Limit Parameters:** Use a parsimonious number of parameters. Simpler models are often more robust.
            
        - **Rigorous Validation:**
            
            - **In-Sample (IS) Testing:** Develop and optimize the strategy on a subset of historical data.
                
            - **Out-of-Sample (OOS) Testing:** Validate the optimized strategy on a completely separate, unseen portion of historical data. _True robustness is demonstrated by strong OOS performance._
                
        - **Parameter Sensitivity Analysis:** Test how sensitive the strategy's performance is to small changes in its parameters. A robust strategy should not collapse with minor parameter adjustments.
            
        - **Focus on Economic Logic:** The strategy should be built upon a **sound, real-world economic rationale or investment logic** , not merely the result of exhaustive trial-and-error parameter searches. A model grounded in fundamental logic is more likely to generalize across past and future market regimes.
            

  

# Q15: What is a Model and What is Overfitting? How to Prevent Overfitting in Model Training?

**I. What is a Model? Distinguishing Models from Algorithms. Common Predictive Models.**

- **Model:** Generally refers to a structure comprising **data** and a **process** for using historical data to predict future data. It represents the learned relationships from data.
    
- **Algorithm:** Refers to the **optimization procedure** executed to train the model. Its goal is to minimize the model's error on the training dataset.
    

Within machine learning (ML), the terms "machine learning algorithm" and "machine learning model" are often used interchangeably, but they have distinct nuances:

- **Algorithm:** The _process_ run on data to _create_ the ML model.
    
- **Model:** The resulting set of **rules, numerical weights, and algorithm-specific data structures** used to make predictions.
    

During stages like model development/prediction and model training/value merging, extracted features or alpha factors are further processed to yield "superior alpha." Early quant hedge funds primarily used linear models. As the adoption of **non-linear models** (e.g., machine learning, deep learning models) has increased, model complexity and parameter counts have risen significantly compared to traditional statistical learning models, leading to better predictive power and overall advancement in quant investment capabilities. The sophistication in handling models like tree-based models (e.g., GBDT) and neural networks (e.g., DNN, LSTM, Transformer, GNN) reflects differences in research depth and breadth among firms.

Models used in quant investment can be broadly categorized into three types:

1. **Factor Mining Models:** Discover predictive signals (factors).
    
2. **Predictive Models:** Forecast future asset returns or movements.
    
3. **Portfolio Optimization & Trading Algorithm Models:** Construct optimal portfolios and execute trades efficiently.
    

Predictive models, in particular, have evolved from simple to complex and continue to grow more sophisticated. Commonly used predictive models in the industry include:

- **Interpretable Linear Models:** Ordinary Least Squares (OLS)
    
- **Statistical Learning / Machine Learning Models:** Lasso Regression, Support Vector Machines (SVM), Gradient Boosted Decision Trees (GBDT)
    
- **End-to-End Deep Learning Models:** Deep Neural Networks (DNN), Long Short-Term Memory networks (LSTM), Transformers, Graph Neural Networks (GNN)
    

**II. What is Overfitting? How to Prevent it in Model Training?**

**Overfitting** is a fundamental concept in statistics and ML, occurring at two levels in quant finance:

1. **Training Overfitting (Narrow Sense - ML Context):**
    
    1. **Definition:** The ML model performs exceptionally well on the **training data** but poorly on **unseen test data or new data** .
        
    2. **Cause:** Inappropriate model hyperparameter selection or excessive training (memorizing noise).
        
    3. **Solution:** Employ robust **cross-validation** techniques to select optimal hyperparameters and determine when to stop training.
        
2. **Backtest Overfitting (Broad Sense - Quant Research Context):**
    
    1. **Definition:** The quant model performs excellently during **historical backtesting** but poorly in **live trading** .
        
    2. **Cause:** Market regime changes, or the model learning too much from **noise** specific to the backtest period.
        
    3. **Solution:** Quantify overfitting severity using specialized metrics (e.g., Probabilistic Sharpe Ratio, Deflated Sharpe Ratio) and employ rigorous **out-of-sample (OOS) testing** and **walk-forward analysis** . Recognize that complete elimination is difficult; robustness is key.
        

**Why Overfitting Occurs in Finance:**

Financial markets involve diverse, evolving participants. Financial data itself is characterized by **low signal-to-noise ratio** and **temporal dependencies** (time series properties). When models are overly complex (too many parameters, excessive learning capacity), they often generalize poorly to new, unseen market conditions, manifesting as overfitting.

**Preventing Overfitting in Financial Model Training:**

Since most ML models weren't designed for financial time series, their application requires careful adaptation. Preventing overfitting is paramount and requires balancing:

- Predictive Accuracy
    
- Model Interpretability
    
- Model Robustness
    
- Computational Complexity
    

**Key Prevention Strategies:**

1. **Avoid Future Information:** Strictly enforce **temporal integrity** . Never use data unavailable at the prediction time. Implement robust data filters.
    
2. **Use Time-Series Appropriate Validation:** Favor **forward validation** (walk-forward testing) over standard cross-validation. Split data chronologically: Train on past -> Validate on subsequent period -> Test on most recent unseen period.
    
3. **Manage Model Complexity:**
    
    1. Start with simpler, more interpretable models.
        
    2. Use **Regularization:** Penalize model complexity (e.g., L1 Lasso, L2 Ridge regression).
        
    3. **Hyperparameter Tuning:** Carefully select hyperparameters controlling complexity:
        
        - **Number of Iterations/Epochs:** Too many lead to overfitting. Monitor training vs. validation performance (early stopping).
            
        - **Regularization Strength (λ):** Controls penalty weight.
            
        - **Dropout Rate (for Neural Networks):** Randomly deactivate neurons during training to prevent co-adaptation (over-reliance). Adjust based on problem/architecture.
            
4. **Feature Engineering & Selection:** Focus on economically sound features/factors. Avoid excessive, potentially noisy features.
    
5. **Rigorous Testing:**
    
    1. **In-Sample (IS) Optimization:** Tune on a subset of _historical_ data.
        
    2. **Out-of-Sample (OOS) Validation:** Test performance on _unseen_ historical data.
        
    3. **Walk-Forward Optimization (WFO) / Forward Testing:** Simulate live deployment by repeatedly training on a rolling window and testing on the immediate future.
        
6. **Sensitivity Analysis:** Test how small changes to parameters affect performance. A robust model shouldn't collapse.
    

**Important Note: Discrepancy Between Backtest and Live Performance**

Not all live performance issues stem from overfitting. Other critical factors include:

- **Data Bias:** Historical data used in backtests may not perfectly reflect actual past market conditions (e.g., survivorship bias, incorrect corporate action handling).
    
- **Slippage & Transaction Costs:** Real-world trading incurs costs (commissions, spreads, market impact) often underestimated or poorly modeled in backtests.
    
- **Strategy Implementation Limits:** Live execution faces constraints like speed limitations and order size impact not fully captured in simulation.
    
- **Market Regime Changes:** Financial markets are dynamic. Participant behavior, macroeconomics, politics, and regulations evolve, causing underlying patterns ("market regimes") to shift. Rules effective in the past may become obsolete.
    

  

# Q16: What is Strategy Capacity and Its Influencing Factors? How Does It Differ from Position Sizing?

**I. What is Position Sizing? How Does it Differ from Assets Under Management (AUM)?**

- **Position (Position Sizing):** Refers to the **quantity or value** of a specific asset or security held by an investor in the market. An equity position typically represents the capital used to purchase stocks, which can be decomposed into "**Own Capital + Leverage** ." In stock trading, positions are categorized as "**Long Positions** " (buying expecting price appreciation) and "**Short Positions**" (selling borrowed assets expecting price decline).
    
- **Position Size Must Match Strategy Capacity:** Position sizing needs to be appropriate for the strategy's ability to handle capital efficiently. Quant firms in the US market commonly use leverage, making **position size** a primary focus, often exceeding AUM. The domestic (China) situation differs:
    
    - Mainstream products like Quant Long-Only (QLO) rarely use significant leverage.
        
    - Market-Neutral products typically have stock positions around **80% of AUM** – meaning position size is generally _slightly less_ than AUM.
        
- **Assets Under Management (AUM):** Represents the **total capital** entrusted to the asset manager. AUM must align with the firm's overall **strategy capacity** . As AUM grows, the manager's own trading activity increasingly impacts the market in a **non-linear fashion** . Accurately estimating this impact using historical data is highly challenging. Managers must monitor their growth rate and ensure **fundraising pace dynamically aligns with strategy capacity** .
    

**II. What is Strategy Capacity? What Factors Influence It?**

- **Strategy Capacity:** Refers to the **maximum amount of capital** a strategy can manage while still achieving its target return profile. Crucially, it is **not a fixed number** but a **function of the expected return** – if the acceptable expected return decreases, the strategy capacity increases.
    
- **Factors Influencing Strategy Capacity:**
    
    - **Inherent Strategy Characteristics (Predictive Horizon is Key):**
        
        1. **High-Frequency (HF) Strategies:** Holding period: **minutes** . Based on microstructure. High excess Sharpe Ratio. **Very Low Capacity.** (Note: True high-quality HF strategies in China's T+1/stamp duty environment have minimal capacity for external capital and are non-mainstream).
            
        2. **Intraday Stat Arb Strategies:** Holding period: **hours** . Predicts intraday price/volume. Good excess returns, high Sharpe. **Low Capacity.**
            
        3. **Statistical Arbitrage (Stat Arb) Strategies:** Holding period: **days/weeks** . Predicts short-term price/volume/events. Moderate excess returns, moderate Sharpe. **Medium Capacity.**
            
        4. **Fundamental Quant Strategies:** Holding period: **months/quarters** . Predicts long-term price changes via fundamentals. Lower excess returns, lower Sharpe. **High Capacity.**
            
        5. _**Core Relationship:**_ **Shorter predictive horizons → Lower tolerance for slippage → Less room to absorb market impact costs → Lower strategy capacity.** Shorter holding periods mean lower expected profit per trade; as size increases, transaction costs (as a percentage of expected profit) rise significantly.
            
    - **Transaction Costs (Especially Market Impact):**
        
        1. Transaction costs increase **non-linearly** with capital size, while strategy returns typically scale **linearly** .
            
        2. **US Market:** Dominant cost is **market impact** ; commissions/rebates are minor.
            
        3. **China A-Shares Market:** As size grows, **market impact costs can even exceed direct costs** like stamp duty and commissions.
            
        4. **Challenge:** Market impact is notoriously difficult to model accurately. Rapid AUM growth can overwhelm existing impact models based on historical data, leading to underestimated slippage and degraded excess returns.
            
        5. _**Investor Insight:**_ Focus on the **rate of AUM change** (especially rapid short-term growth), not just the absolute size. Ask: "Has the manager's investment capability already scaled effectively to their current AUM level and NAV performance?"
            

**III. Enhancing Strategy Capacity:**

The fundamental limitation of strategy capacity stems from the bounded **predictive power** of models. Capacity can be enhanced by:

- **Expanding Scope:** Broaden the stock universe and increase the number of holdings.
    
- **Lengthening Horizons:** Utilize strategies with longer holding periods.
    
- **Diversifying Alpha Sources:** Add low-correlation return streams.
    
- **Systematizing Research:** Improve the granularity and efficiency of the research/investment process.
    
- **Data Quality:** Process higher-quality data covering diverse market regimes.
    
- **Model Robustness:** Optimize parameters, prevent overfitting, improve adaptability.
    
- **Rigorous Validation:** Use stricter backtesting methodologies (e.g., robust out-of-sample testing, walk-forward analysis).
    

**Current Industry Practice:**

Leading quant hedge funds have accumulated significant experience managing large AUM. They continuously optimize strategies by:

1. Building sophisticated models to estimate and manage slippage/market impact based on their specific strategy logic.
    
2. Developing comprehensive product lines to match diverse client needs.
    
3. Ensuring **dynamic alignment** between:
    
    1. Strategy capacity and fundraising pace.
        
    2. Client risk appetite and product risk-return profiles.
        

**Investor Takeaway:**

Investors should deeply understand the **risk-return characteristics** of products and seek those aligned with their own **risk tolerance and investment horizon** .

  

# Q17: How does quantitative investment conduct risk management?

**I. What is Risk Management?**

Asset management is a long - chain business. In a broad sense, risk management is not only involved in the investment research phase but also runs through the entire lifecycle of a product, including product creation, capital raising, investment trading, valuation accounting, and information disclosure. In a narrow sense, risk management refers to the purposeful adjustment and scale control of exposure to improve the quality and stability of returns.

According to Markowitz's Modern Portfolio Theory, portfolio risk can be divided into two parts: systematic risk and idiosyncratic risk. The former refers to the resonance formed by various assets due to external environmental shocks, corresponding to the situation where most assets fall in sync, and it cannot be eliminated through diversification. The latter refers to the risk brought to the portfolio by the fluctuation of a single asset, which can be reduced through diversification. For example, multi - strategy products can allocate risks to different strategy categories based on the pre - set target volatility, keeping the overall risk level within an acceptable budget range. By tracking and monitoring risks, sub - strategy positions can be allocated, and risk allocation can be dynamically rebalanced.

**II. What is a Risk Model?**

Generally speaking, risk management will reduce the profitability of a strategy, but it can also reduce the volatility of strategy returns and the possibility of significant losses. The Alpha model is used to pursue returns, while the risk model is used to control risks. In risk models, more emphasis should be placed on downside risk.

The functions of a risk model include:

- **Ex - post**: Decomposing and evaluating the obtained returns.
    
- **Dimensionality reduction**: Reducing predictions from individual stocks to factors.
    
- **Matching**: Finding suitable factors by examining the returns of pure factor portfolios.
    

The most intuitive way to understand a risk model is to break down the risks faced in investment into individual risk exposures, predict the risks of each exposure separately, and then aggregate them into total risk to obtain a prediction of total risk. Based on the predicted results, corresponding constraints can be applied to the model to achieve the purpose of risk control. The differences between various risk models lie in how they define individual risk exposures and how they predict the risks of individual exposures.

The most basic risk model treats each individual asset in an investment as a risk exposure. For investment strategies, the investment target is not a single asset but a portfolio of assets. The relationship between portfolio risk and individual asset risk is not linear (expected returns can be linearly added), and it depends on three factors: individual asset risk, the correlation between different assets, and the weight allocation among different assets.

Since the basic risk model cannot meet practical applications, structured multi - factor risk models have emerged. Risk decomposition in multi - factor models can be divided into three categories: market risk, industry risk, and style risk. Style risk includes factors such as valuation, growth, financial quality, leverage, size, momentum, volatility, turnover, technical factors, improved momentum factors, analyst sentiment factors, and shareholder factors, among others.

**III. Internal Risk Control System of Quantitative Private Equity**

A scientific and comprehensive internal risk control system needs to be achieved through specific monitoring measures for pre - investment, during - investment, and post - investment decision - making, including risk identification, risk measurement, key risk indicators, and risk limit setting to realize risk control objectives.

The best way to control risk is to prevent it in advance. During the strategy development process, parameters for various extreme scenarios should be introduced into the strategy. For example, diversification can be used to control downside risk. Additionally, real - time monitoring of all products and contracts in the entire market should be conducted to promptly eliminate those with poor liquidity. Strategies designed on this basis can effectively control the volatility of the product.

After the product is in operation, when the preset risk indicators (early warning line / stop - loss line) are triggered, active risk control measures should be initiated in accordance with the product contract requirements, such as reducing positions and increasing corresponding hedging positions.

  

# Q18: What is Risk Exposure? How to Understand and Allocate Risk Budgets?

The formal definition of **risk exposure** is usually "the unprotected risk, that is, the part that may lead to losses due to the lack of any preventive measures against risks." It is commonly used to refer to the portion of financial assets exposed to risks and the degree to which they are affected by risks. In stock quantification, common styles include industry and market capitalization. When these styles are not benchmarked against an index, style exposure occurs.

**Risk budgeting** refers to the measurement and decomposition of a portfolio's risk. Based on the pre - set target volatility, risks are allocated to different strategy categories to keep the overall risk level within an acceptable budget range. Through tracking and monitoring of risks, dynamic rebalancing of sub - strategy positions and risk allocation is carried out.

Traditional asset allocation focuses on distributing capital across different asset classes, while risk budgeting focuses on allocating risk to sub - strategies or different asset classes, paying attention to marginal risk and weights. The main goal is to balance the risk in the portfolio to match the investor's risk tolerance and risk preference. Risk budget allocation typically employs two methods:

- **Top - Down Approach**: Determine the overall risk budget at the portfolio level and allocate individual risk budgets based on the expected contributions of each asset, strategy, or sector to the portfolio's risk and return profile.
    
- **Bottom - Up Approach**: First determine individual risk budgets at the asset, strategy, or sector level, and then aggregate them to form the overall risk budget. This method allows for a more detailed understanding of the risk drivers within the portfolio.
    

Risk budgeting is crucial for achieving absolute returns. To implement more refined risk management, the following factors also need to be considered:

- **Allocation of different risk factors**: For example, in the stock market, beta risk, style, and industry risk; in the bond market, interest rate risk, duration risk, and credit risk. If engaging in global multi - strategy investing, exchange rate risk and other factors also need to be incorporated into the risk budget at the portfolio level. For instance, assume there is a sub - strategy for real - estate - industry credit bond arbitrage and another for energy - industry credit bond arbitrage. On the surface, they appear to be low - correlated, but in reality, both are exposed to credit risk.
    
- **Resonance under extreme risks**: Under normal circumstances, many assets and strategies exhibit low correlation. However, during extreme events like the 2008 global financial crisis, the vast majority of capital tends to lower risk appetite, deleverage, and chase liquidity, resulting in high correlation among many strategies. In 2022, when CTA sub - strategies experienced significant drawdowns and high short - term correlations, managers with essentially singular return sources performed poorly, while those with superior risk control, mature factors, and timely adjustments maintained stable performance. For such resonance under extreme risks, institutions need to allocate sufficient buffer in the risk budget and make dynamic adjustments.
    

  

# Multi - Factor Model

## **Q19: What is a Multi - Factor Model?**

The multi - factor model is a mainstream and widely - used model in the market for quantitative stock selection. In a multi - factor model, factors refer to indicators that can characterize certain aspects of a stock and have the ability to predict the relative size of stock returns. The ability to predict the relative size of stock returns means that stocks with higher factor values should have higher returns than those with lower factor values. For example, the reciprocal of the price - earnings ratio (EP) is used to represent the value factor. A higher EP value indicates a lower valuation and a higher value. In the long - term or over a certain period, stocks with higher EP values are likely to have higher future returns. In other words, the EP indicator has the ability to predict the relative size of stock returns.

Factors characterize certain aspects of a stock. Therefore, when constructing factors, it is necessary to first determine which aspect of the stock the factor is supposed to represent. For example, the momentum factor represents the trend - like characteristic of a stock's price, which can typically be calculated based on the recent price changes.

Each factor represents a particular aspect of a stock's characteristics and is backed by an investment logic, representing growth, valuation, profitability, etc., and each has a certain predictive power. There can be dozens, hundreds, or even thousands of factors. When there are many factors, analyzing each one individually is not only difficult to manage but also may not yield good results. If these factors can be integrated into a single value, that is what is commonly referred to as the Alpha factor. This Alpha factor represents the multi - factor model's prediction of stock returns and is intended to be more accurate and stable in predicting stock returns than each individual factor. Therefore, the goal of the multi - factor model is to integrate many factors that have some predictive power for stock returns, leveraging their strengths and compensating for their weaknesses, to form the final Alpha factor that represents the model's prediction of stock returns. This Alpha factor should have better predictive power than each individual factor in the model. The simplest method of integration is direct addition. Of course, now machine learning and various other algorithms can also be used to integrate multiple factors.

  

## **Q20: How to Evaluate the Effectiveness of a Factor?**

There are usually three methods to evaluate the effectiveness of a factor: group returns, IC (Information Coefficient), and portfolio optimization returns.

Group returns are relatively simple. First, at the end of each month, stocks are sorted by the size of their factor values and evenly divided into 10 groups. The number of groups is not fixed and can also be 5 or 7. The more groups there are, the more in - depth the analysis of the factor's predictive power can be. Then, the average return of each group of stocks in the following month is calculated. If the order of the group returns matches the order of the factor values, it is considered that the group returns have monotonicity. The closer the group returns are to an arithmetic sequence, the stronger the monotonicity. Factors with strong group return monotonicity have strong predictive power because by simply buying and holding the group of stocks with the highest factor values, relatively better returns can be obtained.

IC, or Information Coefficient, is the correlation coefficient between the initial ranking of stock factor values and the final ranking of stock returns. The larger the absolute value of IC, the higher the correlation between the ranking of factor values and the ranking of stock returns, which means stronger predictive power. An IC greater than 0 indicates that higher factor values are associated with higher stock returns, while an IC less than 0 indicates that lower factor values are associated with higher stock returns. For example, if there are 10 stocks and the IC of a certain factor is 1, meaning that the ranking of factor values is perfectly positively correlated with the ranking of stock returns, it implies that the stock with the highest factor value always has the highest return.

If the number of groups in group returns is continuously increased until each stock is a group, the group returns become the calculation of IC. Therefore, group returns can be considered a simplified form of IC.

Both group returns and IC are essentially simple estimates of a factor's predictive power and often overestimate it without considering the impact of trading restrictions that may exist in actual trading on returns.

The method of portfolio optimization returns takes into account the trading restrictions that may exist in actual investments, such as stock weights not being negative (i.e., no short selling), turnover rate not being too high (not exceeding 20%), industry deviation limits (e.g., industry deviation not exceeding 2%), and style factor deviation limits, etc. The portfolio is constructed according to the optimization model, and the return of this portfolio is calculated, which is the closest to the return that the factor can achieve in actual investment. The higher the optimized return of a factor, the more effective it is and the more it can contribute to returns in actual investment.

  

## **Q21: Why Do Some Factors Have Unideal Excess Returns?**

Some factors have high group returns and IC values, but why do they fail to deliver satisfactory excess returns in actual investments? Group returns are calculated by first sorting stocks based on factor values and then dividing them into groups to analyze the monotonicity of the group returns. IC measures the correlation between the ranking of factor values and the ranking of stock returns. Higher monotonicity in group returns and higher IC values indicate stronger predictive power of the factor. However, why do these factors still fail to deliver good excess returns in practice?

The main reason is that group returns and IC often overestimate the predictive power of factors. When grouping stocks, if some illiquid stocks are not excluded, such as those that have been suspended for a long time and may experience consecutive limit - up or limit - down movements upon resumption of trading, the group returns can be distorted. For example, it is difficult to buy stocks that are continuously limit - up. Moreover, when adjusting groups monthly, turnover rate constraints are usually not considered. As a result, the calculated group returns are not representative of actual investment outcomes.

When calculating group returns, it is important to ensure that the sample space used for grouping is tradable and to exclude the impact of illiquid stocks. IC measures the correlation between the ranking of factor values and the ranking of stock returns. Even if the factor values are smaller and the stock returns are also smaller, the IC value can still be relatively high. However, in actual investment, A - shares can only be long, not short. Therefore, the portfolio typically consists of stocks with higher factor values, but the factor may have lower predictive power for these stocks. This leads to lower returns for the actual investment portfolio. Although the overall IC is high, it is actually inflated by the stocks with smaller factor values, which are often not achievable in actual investment. This is commonly referred to as "unattainable short - side returns." When analyzing IC values, it is important to check whether the IC is mainly contributed by the short - side. If the short - side contribution is too high, it is not a good factor.

  

## **Q22: How to Find Simple and Effective Factors?**

There are mainly two approaches to finding or mining factors. One is to start with an investment logic and then identify corresponding indicators to capture this logic, testing their effectiveness and continuously adjusting the calculation formulas to improve their predictive power. The other is to directly explore the patterns between indicators and stock returns without caring about the economic meaning of the indicators, as long as they have predictive power. The calculation formulas for indicators in the second approach are often complex and lack intuitive understanding.

In multi - factor models, the first approach is the mainstream method. Most factors in multi - factor models are based on investment logic and have clear economic meanings, such as value and growth factors. To find factors using this approach, it is necessary to continuously accumulate investment logics. Investment logic can be simply described as an "if... then..." relationship. For example, if a stock has a certain characteristic, its return will be higher or lower. Investment logics can be obtained through reading the works of investment masters, studying academic reports, communicating with peers, and observing market trends. After extracting the investment logic, the next step is to quantify it, which is the main work of quantitative investment. By defining the investment logic in a quantitative way and converting it into specific formulas and numbers, we obtain factors or indicators. The next step is to test their predictive power. In most cases, factors obtained through simple methods do not have high predictive power. This could be because the calculation formula or data do not fully reflect the investment logic. In such cases, it is necessary to revise and adjust the calculation formulas and data to make the indicators more accurately reflect the investment logic and enhance their predictive power. Of course, it is also possible that the investment logic itself is not valid or has low predictive power, in which case the investment logic needs to be scrutinized.

In the second approach, machine learning or data mining methods are commonly used to discover factors. First, various types of data are input, including fundamental data such as revenue, market data such as closing prices and trading volumes, and even news sentiment. Then, the machine is trained to find patterns between these data and stock returns to predict future stock performance. This method does not care about the underlying logic or causal relationships and only pursues improving the fit within the sample. However, this may lead to some unknown issues. Therefore, machine learning should be used cautiously as a tool.

  

## **Q23: What "Pitfalls" to Avoid When Mining Factors?**

In the process of mining factors or developing quantitative models, several common pitfalls often arise, including survivorship bias, using future data, and overfitting.

Most people have heard of survivorship bias and understand its meaning, but few may have seriously considered how significant its impact can be. For example, if we use the current constituents of the CSI 300 Index for backtesting, calculating factor values from the current constituents and then testing their historical performance, the results can be misleading. Since the index adjusts its constituents every six months, the stocks that remain in the index are generally the better - performing ones. This can make the backtesting results appear better than they actually would be in reality. To avoid this pitfall, it is crucial to use point - in - time (PIT) data for backtesting. This means recording the data as it was published at the time, without any retrospective corrections. For instance, if Stock A was delisted at the end of the previous year, some backtesting databases might remove Stock A from the dataset. As a result, it would never be selected in the backtesting, which is clearly unreasonable. Using PIT data would retain Stock A as it was, because before its delisting announcement, we did not know when it would be delisted and it could have been selected.

As previously mentioned, using future data is also known as "look - ahead bias," which involves using data that was not yet available at the time in backtesting. The most common example is financial reports. Listed companies typically publish their annual reports in March or April of the following year, with the reporting period ending on December 31 of the previous year. It is easy to inadvertently use these annual report data in January of the following year during backtesting, such as net profit figures, or indirectly reference them when calculating metrics like price - earnings ratios using net profit. The solution to avoid using future data is straightforward: adhere strictly to using PIT data during backtesting.

Moreover, overfitting is another common pitfall and a potentially fatal risk in quantitative investing, especially with indicators that can be parameterized. For example, a momentum indicator could be defined based on the returns over the past 20 days or the past 50 days. Within a specific time period, it is always possible to find an optimal parameter, such as 30 days, that maximizes the predictive power of the momentum indicator during that period. However, this parameter often becomes ineffective once the time period changes. Distinguishing between overfitting and genuine improvements in predictive accuracy within the sample is not easy. Typically, out - of - sample testing is required to make this judgment. If a model performs well in - sample but poorly out - of - sample, overfitting is likely the cause. Generally, the more parameters an indicator has, the more susceptible it is to overfitting.

  

## **Q24: How to Combine Multiple Factors into an Alpha Factor?**

In a multi - factor model, each factor represents a particular aspect of a stock's characteristics. Ultimately, a large number of factors need to be combined into a single Alpha factor. Before synthesizing the final Alpha factor, it is necessary to first combine individual metrics into factors.

Each characteristic of a stock can be captured by multiple metrics. For example, a momentum factor could be represented by the return over the past 20 days or the return over the past year. Which metric better represents the momentum factor? Often, the metrics calculated based on different time - frame returns are simply summed to create the momentum factor. Of course, these metrics should be standardized before being combined into the momentum factor, and the resulting momentum factor should also be standardized.

When combining metrics that capture the same characteristic into a factor, simple summation is often used because these metrics are usually highly correlated, with differences primarily arising from different parameters. However, when combining factors that represent different characteristics into an Alpha factor, simple summation may not be the best approach.

Different factors represent different investment logics, and different market environments favor different investment logics. The predictive power of factors is also often cyclical. Therefore, weighting factors based on their predictive power, specifically using IC (Information Coefficient) weighting, where factors with higher IC values are given greater weight, can enhance the predictive power of the Alpha factor. Of course, if both the magnitude and stability of IC values are important, weighting based on ICIR (Information Coefficient to Information Ratio) could be considered. The calculation of ICIR is similar to the IR (Information Ratio) formula for funds, obtained by dividing the mean of IC by the standard deviation of IC.

  

## **Q25: How to Continuously Add New Factors?**

How can new factors be continuously added to an existing Alpha factor? Each characteristic of a stock has some predictive value for the relative size of stock returns. An effective multi - factor model should contain a large number of factors, and the correlation between the characteristics of stocks represented by these factors should be relatively low.

The strength of a multi - factor model lies in its ability to comprehensively consider various characteristics of stocks, leveraging their strengths and compensating for their weaknesses to achieve a combined advantage. Therefore, the correlation between different factors should be low. Otherwise, if two highly correlated factors are essentially equivalent to repeating the same factor multiple times, this not only fails to enhance the predictive power of the Alpha factor but also increases the exposure of the Alpha factor to a particular characteristic of the stock. This undermines the integrative advantage of the multi - factor model and increases risk.

Thus, if you already have a mature multi - factor model, adding a new factor is like an organization welcoming a new member. It is necessary to evaluate not only the new factor's own predictive power but also its correlation with the existing factors in the model. The most important consideration is whether it can provide incremental information, such as introducing a new investment logic or a new data processing method. If the new factor has a relatively high IC value and a low correlation with the existing factors, it can be directly added as a new member. If it has a high correlation with a certain factor, it can be combined with the existing factor, or even directly replace an existing factor.

  

# Q26: Can Factors Fail?

The goal of using a multi - factor model is to integrate multiple factors that have some predictive power for stock returns, leveraging their strengths and compensating for their weaknesses to ultimately form the Alpha factor, which represents the model's prediction of stock returns. Can this multi - factor model remain effective forever and allow investors to "lie back and win"?

It is important to remember that there is no eternal "Holy Grail" in investing, and multi - factor models are no exception. There is no model that is always effective. Multi - factor models are composed of many factors, each representing a different investment logic, and each investment logic has its own suitable market environment. Therefore, it is normal for some factors in a multi - factor model to temporarily fail. The advantage of a multi - factor model is its integration. When many factors are combined into the Alpha factor, the possibility of factor failure has already been considered. By assigning higher weights to factors with higher predictive power, which means giving lower weights or even zero weight to failed factors, the impact of these failed factors on the Alpha factor is naturally reduced.

Since it is already recognized that multi - factor models cannot be a one - time solution, the daily work of researchers is to continuously add new factors to the multi - factor model, replace those that have clearly failed, and enrich the factor library of the multi - factor model. The more factors there are, the more investment logics are covered, and the more the integrative advantage of the multi - factor model can be leveraged.

Investing involves risks, and returns can fluctuate. Although the Alpha factor obtained from a multi - factor model may also experience temporary drawdowns, as long as it is a true multi - factor model with many low - correlated factors, the weighted combination of multiple factors into the Alpha factor can truly give higher - predictive - power factors higher weights. Such a multi - factor model has adaptive capabilities and can automatically adjust to quickly emerge from a trough after a temporary drawdown and continue to leverage the advantages of the multi - factor model.

  

# Q27: What is a Factor? How Are They Typically Classified?

## I. Definition of Factors

Investors often hear phrases like "mining factors" and "continuous enrichment and iteration of the factor library." But what exactly is a "factor"? How should we define and classify factors?

In quantitative stock selection, a factor is defined as a "characteristic that explains the differences in individual stock returns." Factors can explain the returns of an investment portfolio or help in asset pricing. The effectiveness of a factor is primarily judged by its predictive power. A factor is considered effective if it demonstrates a pattern in historical data over a certain period, but this does not guarantee that the pattern will persist in future markets.

## II. Classification of Factors

There are many types of factors, and different categories of factors can explain the differences in individual stock returns from various dimensions. In quantitative stock selection models, factors are generally divided into "risk factors" and "alpha factors." The former emphasizes the sources of risk and still has strong explanatory power, but has lost predictive power; the latter emphasizes the sources of return and focuses on whether it can predict future relative returns of individual stocks.

Risk factors were originally alpha factors, but they were discovered and published by the academic community early on, especially in the U.S. stock market, where their return - to - risk ratio quickly declined. However, these factors still explain a lot of returns, even though their predictive power has almost disappeared, which is why they are called "risk factors." Common risk factors include market capitalization, price - earnings ratio, price - to - book ratio, liquidity, residual volatility, etc.

"Alpha factors" generally refer to factors that can stably contribute excess returns. Their construction is relatively complex, or their data sources are more unique. Generally, each institution's alpha factors are different and exhibit low correlation.

There are significant differences between overseas markets, represented by the U.S. stock market, and the A - share market in terms of operating mechanisms, development stages, investor structures, financing costs, and constraints. Therefore, there are differences in how alpha factors and risk factors are handled. For example, overseas quantitative products mainly focus on "market - neutral + leverage." Considering that risk factors usually bring significant volatility but do not simultaneously bring significant returns, asset management institutions try to minimize exposure to risk factors during the modeling process. In contrast, in domestic quantitative products, the scale of various quantitative long - only product lines accounts for the highest proportion. For long - only products, relaxing constraints on risk factors does not significantly increase net value volatility, and strictly controlling risk factors can actually constrain the performance of alpha factors.

Alpha factors can be classified by data source into price - volume factors, fundamental factors, event - driven factors, and alternative data factors.

**Price - Volume Factors**

Price - volume factors can be further divided into short - cycle price - volume factors and medium - to - long - cycle price - volume factors. Short - cycle factors often refer to high - frequency and intraday factors, while medium - to - long - cycle factors generally have a holding period of about 1 - 20 days. Currently, medium - cycle price - volume factors have a relatively high allocation in the A - share market.

**Fundamental Factors & Event - Driven Factors**

Based on the time span that triggers stock price reactions, they can be divided into short - cycle "event - driven factors" and long - cycle "fundamental factors." The former includes financial report releases, profit pre - increases, expected扭亏（turning losses into profits）, and sudden events, while the latter generally includes valuation, growth, and profitability quality, etc. The proportion of fundamental factors is also gradually increasing. However, for quantitative private equity, further significantly increasing the allocation of fundamental factors still awaits the right timing. Currently, the overall management scale of domestic quantitative private equity is still relatively small compared to the entire market, and strategies mainly based on price - volume can still contribute to a good return - to - risk ratio. The business model of private equity charges more than that of public funds, requiring private equity managers to provide products with better return - to - risk ratios to win investors' favor.

**Alternative Data**

Alternative data factors are more mature in overseas markets but are still a blue ocean in China. Top - tier quantitative private equity firms not only maintain connections with multiple third - party data providers but also collect and continuously explore alternative data to achieve further breakthroughs.

## III. The "Factor Homogenization" Phenomenon Does Not Exist

The profit sources of quantitative investment are very diverse. As mentioned above, there are high - frequency factors driven by micro - structural data (which are non - mainstream in China), price - volume factors driven by trading data, fundamental factors driven by fundamental data, event - driven factors, and alternative data factors. Since each quantitative institution has differences in methodology, models, and team structure, their portfolio optimization and final trading behaviors are also very diverse.

From the analysis of the excess returns of major A - share quantitative institutions, it can be seen that after removing common factors that affect quantitative excess returns, such as trading volume, volatility, and dispersion, the excess return correlations among different institutions are not high. There is no so - called "factor homogenization" – data from overseas markets also supports this conclusion. The main reason is that the intersection of each institution's alpha is mostly used to overcome stamp duty, commissions, and impact costs, while the performance is often reflected in each institution's unique alpha factors. Logically speaking, if institutions' trading behaviors were to converge, it would lead to over - traded stocks deviating from their reasonable prices, which would provide other market participants with opportunities for contrarian trading, thus making the "trading convergence" invalid.

Of course, quantitative private equity managers still need to continuously develop and enrich underlying factors, improve the efficiency of strategy evolution, deepen their understanding of the market, and continuously optimize models at the portfolio level, as well as cultivate excellent talents. Currently, various quantitative managers are deeply exploring directions such as accelerating the integration of quantitative fundamentals, emphasizing the application of alternative data, further deconstructing alpha strategies based on micro - structures, and implementing multi - cycle, multi - strategy, and multi - asset approaches, and have achieved good progress and results.

# Q28: What are Factor Standardization and Neutralization?

Factors represent different characteristics of stocks and are calculated using various methods and units. For example, market capitalization is measured in yuan with a magnitude of billions, while the price - earnings (PE) ratio is a dimensionless ratio with a magnitude of single or double digits, and return on equity (ROE) is measured in percentages. The goal of a multi - factor model is to integrate multiple aspects of stock characteristics to derive an Alpha factor that can predict stock returns. However, if the units and magnitudes of factor values differ, direct arithmetic operations like addition and subtraction are not feasible. When the magnitudes of indicators vary significantly, using raw values in analysis would overemphasize high - value indicators and under - emphasize low - value ones. To achieve the goal of a multi - factor model, each factor must be standardized to unify units and magnitudes, allowing fair comparison and arithmetic operations among factors.

The most commonly used standardization method is the Z - Score method, also known as normalization. The calculation process involves first determining the mean and standard deviation of all raw values of an indicator. Then, each raw value is subtracted by the mean and divided by the standard deviation.

The formula is as follows:

$$y_i=\frac{x_i-\bar{x}}{s}$$

$\bar{x} = \frac{1}{n} \sum_{i=1}^{n} x_i$; 

$s=\sqrt{\frac{1}{n-1} \sum_{i=1}^{n} (x_i - \bar{x})^2}$

Before standardization, extreme value handling is typically performed to mitigate the impact of outliers. This usually involves removing or replacing extremely high or low values with a threshold value. After standardization, the data conforms to a normal distribution with a mean of 0 and a standard deviation of 1, with over 99% of the data falling within the [-3, 3] interval. Standardization does not alter the relative ranking of the original data, thus preserving the factor's predictive power for stock returns. Once all factors in a multi - factor model are standardized, they can be combined through arithmetic operations to form the Alpha factor.

Neutralization goes a step further than standardization by eliminating the influence of certain factors. Typical examples include market - cap neutralization and industry neutralization. This is usually achieved through linear regression, where the target factor is the dependent variable, and market capitalization and industry are the independent variables. The residuals from the regression represent the factor values after excluding the impact of market capitalization and industry. For instance, trading volume is highly correlated with market capitalization; larger - cap stocks tend to have higher daily trading volumes. Including both trading volume and market capitalization in a model introduces redundant information, which does not significantly enhance the model's predictive power. Therefore, trading volume needs to be neutralized to extract the incremental information it provides.

  

# Q29: What are Features? How Do They Differ from Factors?

## I. Features and Factors

Factors are "characteristics that explain differences in individual stock returns," with Alpha factors emphasizing their ability to predict future relative stock returns. Features refer to "measurable properties or characteristics of an observed object," typically numerical, though pattern recognition in syntax can use structural features (such as strings and graphs).

"Features" focus more on information that conforms to statistical laws, while "factors" emphasize logic and interpretability. Generally, medium - and low - frequency data can directly extract Alpha factors, as many low - frequency indicators inherently possess stock - selection capabilities. In contrast, raw high - frequency market data cannot be directly used as Alpha factors. Instead, features must be constructed from high - frequency data through signal transformation, time - series analysis, machine learning, and other methods to build stock - selection factors.

Quantitative investment can be roughly divided into six stages: data collection, data cleaning, feature extraction, model development, portfolio optimization, and trade execution. The "feature extraction" stage may have different names across firms, with simple Alpha factor extraction and basic feature engineering conducted here.

In the field of machine learning, "feature engineering" involves designing the most suitable features given the data, model, and task. This process is akin to organizing data and extracting meaningful information in a clean and structured manner to meet business needs.

Effective feature extraction can save a significant amount of work in subsequent stages. Some top - tier overseas institutions, such as D. E. Shaw, do not particularly emphasize the complexity of deep learning models. However, due to the high quality of their Alpha factors, even relatively simple models can achieve excellent modeling results. This is why the industry does not solely focus on the number of factors; the quality of factors (i.e., the number of independent Alphas) is key. Different methodologies yield different outcomes: factors derived from logic tend to be of higher quality, while brute - force methods yield a larger quantity of factors.

In recent years, the A - share market has become more efficient and institutionalized, increasing the difficulty for quantitative private equity to obtain excess returns. Factor development now faces challenges of higher - dimensional data, lower - density information, and higher - content noise. Machine learning methods, which excel at handling massive data and high - dimensional features, have been rapidly applied to the quantitative research process. Deep learning models, with their flexible and diverse network structures, are suitable for various modeling scenarios and inherently possess the ability to automatically learn features. As the number of network layers increases, the model's linear and nonlinear expression capabilities significantly enhance within a certain range.

With the further development of artificial neural networks, it is possible to analyze raw data directly without feature extraction, in addition to analyzing signals with pre - extracted features. This approach avoids information loss due to human selection, retains all information, and ultimately helps obtain Alphas with extremely low correlation.

## II. Iteration Directions for Quantitative Institutions:

**First Category: Pursuing Updated Methodologies**

For example, in feature engineering, enhancing a deep understanding of data and "combining a profound understanding of the market with the most advanced scientific technology" is crucial. Simply extracting and connecting factors does not increase returns. Diversified expansion across different dimensions is the future direction. Although alternative data is not widely used in China's A - share market and has not significantly increased strategy excess returns, its development prospects are broad and still worth continuous accumulation and research. Unlike natural language learning, the stock market itself does not have enough data points; merely piling up data will inevitably lead to overfitting. Excellent researchers, starting from understanding, can also perform data analysis and discover what others cannot think of using logic - based factors (such as event - driven factors).

**Second Category: Focusing on Updated Models and Higher Computing Power - Relying on Simulation and Approximation to Replace Human Understanding**

In 2017, researchers from Google proposed the Transformer neural network model, which inspired further technological applications for global quantitative institutions. If newer models are applied, the ability to mine Alpha may increase significantly compared to before. The "brute - force" approach represented by deep learning is very important. Differences in details such as how many layers a neural network should have and how to avoid overfitting are also what differentiate different institutions. This is why "using the same model can result in a thousand different performances."

In addition to investing in hardware infrastructure, quantitative private equity also needs to strive to create a research and investment environment conducive to high - efficiency output, provide relatively better welfare benefits for top - tier talents, and balance the improvement of hard power and the upgrade of the soft environment.

  

# Multi - Factor Risk Models: 6 Questions

## Q30: The Principle of Multi - Factor Risk Models

Risk models are essentially also a process of stock pricing. Because stocks bear risks, they require a risk premium as compensation. Risk pricing models have also evolved over different eras. Initially, in 1964, American scholars William Sharpe and John Lintner proposed the Capital Asset Pricing Model (CAPM) based on portfolio theory. It mainly studies the relationship between the expected return of assets in the securities market and risk assets, as well as how equilibrium prices are formed. It is the cornerstone of modern financial market price theory. This theory holds that the expected return of a single security consists of two parts: the risk - free rate and the compensation for the risks undertaken, namely the risk premium. The market's risk premium is the market's expected return rate minus the risk - free return rate. The size of a security's risk premium depends on its Beta value relative to the market portfolio, which measures the systematic risk of a single security. The higher the Beta value, the higher the risk of the single security, and the higher the compensation received, that is, the higher the expected return rate.

CAPM relatively simply describes the relationship between the expected return of a security and the expected return of the market portfolio. In 1976, Stephen Ross proposed the Arbitrage Pricing Theory (APT) model. The APT model argues that arbitrage behavior is a decisive factor in the formation of modern efficient markets (market equilibrium prices). If the market has not reached an equilibrium state, there will be risk - free arbitrage opportunities. The APT model uses multiple factors to explain the returns of risky assets and, based on the no - arbitrage principle, concludes that there is an (approximate) linear relationship between the equilibrium return of risky assets and multiple factors.

Although the APT model is formally perfect, it does not specify the specific factors that drive asset prices. Moreover, these factors may be numerous and can only be judged by investors' experience. Each factor requires the calculation of a corresponding Beta value. In contrast, the CAPM model only requires the calculation of one Beta value. Therefore, in the actual application of asset pricing, CAPM is more widely used than APT.

In 1993, Eugene Fama and Kenneth French took a completely different approach to explain asset returns. They did not assume rational investors or the absence of arbitrage opportunities in the market. The Fama - French three - factor model originated from two pricing phenomena discovered by everyone: first, small - cap stocks have higher average returns; second, stocks with low price - to - book (PB) ratios have higher returns. Subsequently, Fama and French divided stocks into 25 portfolios based on market capitalization and PB ratios (five levels from high to low for PB and five levels from high to low for market capitalization) using corporate finance data, resulting in the three - factor model based on market, PB, and market capitalization.

  

## Q31: Factors in Multi - Factor Risk Models

Inspired by the Fama - French three - factor model, that is, the market factor, market - cap factor, and price - to - book factor can explain part of the expected return of assets. Some financial giants began to study the factors that can affect the expected return of stocks, and we define these factors as factors.

In 2011, Morgan Stanley Capital International (MSCI) released the relatively complete Barra multi - factor risk model. This model includes country factors, 10 style factors, and more than 30 industry factors, adding many factors compared to the Fama - French three - factor model.

Country factors are relatively easy to understand. If the investment targets are all stocks of one country, then the country factor for all stocks is 1.

For industry factors, generally speaking, the performance differences between stocks of different industries can be very large. The business scope, industrial policy, and development direction of each industry are different, and their positions in the national economy and people's livelihoods are also different. Therefore, the industry classification of stocks has a significant impact on the future return differences of stocks. For example, a stock in the liquor industry may have performed very well in recent years, while stocks in the construction, building materials, and textile and apparel industries may have performed poorly in the past two years.

The Barra multi - factor risk model includes 10 style factors: market capitalization, Beta value, momentum, residual volatility, mid - cap, value, liquidity, profitability, growth, and leverage. Each style factor describes a dimension and attribute of a stock, and this attribute can have a significant impact on the expected return of the stock, which can be positive or negative.

For example, before 2017, the small - cap factor had a positive impact on the expected return of stocks, that is, small - cap stocks had a greater probability of outperforming the benchmark. After 2017, the direction of the impact of the small - cap factor on the expected return of stocks changed, that is, small - cap stocks had a greater probability of underperforming the benchmark. Similarly, we have also experienced the stage of value factor failure. Previously, stocks with low - valuation characteristics performed better than the benchmark, indicating that low valuation could have a positive impact on the expected return of stocks. However, after the second half of 2019, the market favored stocks with relatively high valuations and good growth. Low valuation had a negative relationship with the expected return of stocks. Therefore, we call these style factors risk factors, that is, these factors can indeed have a significant impact on the expected return of stocks, but the direction of the impact can be positive or negative.

In summary, the Barra multi - factor risk model is a collection of multiple factors that have a significant correlation with the expected return of stocks, including country factors, industry factors, and style factors. It uses a linear regression model to study the impact of these factors on the expected return of stocks.

  

## Q32: How to Construct a Multi - Factor Risk Model?

As previously mentioned when introducing the Barra multi - factor risk model, it includes country factors, 10 style factors, and over 30 industry factors. These factors can explain part of a stock's return. The returns that cannot be explained by these factors are referred to as idiosyncratic returns or residual returns of individual stocks. These are caused by factors unique to each stock and cannot be explained by systematic factors. Therefore, a complete multi - factor risk model includes systematic risk factors such as country factors, industry factors, style factors, and the idiosyncratic part of individual stocks.

We can refine the concept of factors a bit further. Factors consist of factor exposures and factor returns. How should we understand these two concepts? Let's start with factor exposure. Taking the market capitalization factor as an example, each stock has its own market capitalization, which varies. The numerical value of each stock's market capitalization is the exposure to the market capitalization factor. To unify the scale, the numerical value of this factor exposure is standardized, so that the factor exposure mainly falls within the range of - 3 to 3. The market capitalization factor, as a risk factor, has a risk premium or risk compensation corresponding to a unit of risk exposure, which is the factor return. Suppose one day, the risk premium for the market capitalization factor is 1%, that is, the factor return is 1%. If a stock has a market capitalization factor exposure of 1, then the market capitalization contributes 1% to the stock's return. If another stock has a larger market capitalization with an exposure of 2, then its market capitalization contributes 2% to its return. Therefore, it is essential to understand factor exposure and factor return. Regarding the market capitalization factor mentioned earlier, some may think that the market capitalization factor exposure is simply the stock's market capitalization, which is then standardized. So, how is the factor return for the market capitalization factor obtained? In practice, the factor return can be estimated through linear regression.

For example, on the first day, the factor exposures are calculated for each factor. On the second day, when the returns of all stocks are known, a linear regression is performed between the individual stock factor exposures and the stock returns to estimate the coefficients of the factor exposures. These coefficients represent the corresponding factor returns. The significance of the coefficients indicates the significance of the factor's impact on stock returns. The larger the absolute value of the number, the more significant the factor's impact on individual stock returns. Through the regression model, the idiosyncratic return of stocks that cannot be explained by systematic factors can also be obtained. By calculating the factor returns and idiosyncratic returns of stocks through regression every day, a time - series of factor returns and idiosyncratic returns of stocks can be obtained. Consequently, the covariance matrix of factor returns and the volatility of idiosyncratic returns can also be calculated. It can be seen that we essentially use the multi - factor risk model to "dissect" the returns and volatility of stocks completely.

When constructing a portfolio, it is often necessary to select a subset of stocks from a large pool of stocks under certain constraints. In the optimization process, it is necessary to calculate the covariance matrix of the returns of all stocks in the entire pool. Since there are many stocks, estimating the traditional covariance matrix is challenging, facing issues such as poor estimation accuracy and parameter sensitivity. Through the decomposition of the risk model, the returns of all stocks can be decomposed into systematic factor returns and idiosyncratic returns. Therefore, the covariance of stocks can be derived using the covariance matrix of factor returns and the idiosyncratic returns of individual stocks. Since the number of factors is relatively smaller than the number of stocks, the resulting stock covariance is easier to obtain and more accurate.

  

## Q33: Covariance Matrix and Idiosyncratic Risk in Risk Models

In risk models, the estimation of the factor covariance matrix and idiosyncratic risk of individual stocks is a key and challenging task. The estimation is mainly based on historical data, with the premise of obtaining daily factor returns and idiosyncratic returns data and having a relatively complete historical dataset.

Let's first look at the estimation of the factor covariance matrix. We have the daily returns of over 40 factors, including country, industry, and style factors, and we can calculate the covariance in the traditional way. Considering that data closer to the calculation date may have a greater impact, we can assign higher weights to it in the calculation; data farther from the calculation date may have a smaller impact, and we assign relatively lower weights to it. Through calculations, it has been found that the time - series of factor returns exhibit autocorrelation, meaning that today's return may affect tomorrow's return. Some adjustments are needed to reduce the estimation bias caused by this autocorrelation. Later, during portfolio optimization, it was found that for some optimized portfolios, the estimated covariance would be underestimated or overestimated. Therefore, eigenvalue adjustments were made, and step - by - step, a relatively mature method for estimating the factor covariance matrix was eventually formed. Similar adjustment methods are also used in the estimation of idiosyncratic risk of individual stocks. There are some new issues with idiosyncratic risk estimation, which require corresponding methods to be addressed. For example, some stocks are suspended and have no return data; some stocks are ST (specially treated) and have some particularities; some newly - listed stocks do not have long - enough historical data. It was found that the estimation of idiosyncratic risk tends to overestimate the volatility of high - volatility stock groups and underestimate the volatility of low - volatility stock groups. Therefore, a Bayesian shrinkage estimation method is used for correction. After identifying and gradually improving the issues, a relatively good estimation of idiosyncratic risk of individual stocks was formed. After estimating the factor returns, factor covariance matrix, idiosyncratic returns, and idiosyncratic risk, these pieces of information can be used for portfolio optimization.

  

## Q34: How to Evaluate the Quality of a Risk Model?

In the previous sections, we primarily used the Barra multi - factor risk model as an example to dissect risk models. Investors can actually build their own risk models based on their understanding of the market by identifying factors that influence future stock returns. So, what criteria can be used to evaluate the quality of a risk model?

1. **Explanatory Power**: This refers to the extent to which the factors in the model can explain the variation in stock returns. It is usually represented by \( R^2 \). The higher the \( R^2 \), the better the model's factors can explain the changes in stock returns, indicating a better fit of the model to the data. If the chosen factors cannot explain future stock returns, the risk model loses its purpose.
    
2. **Significance of Individual Factors**: Simply increasing the number of factors to achieve higher explanatory power is not advisable. When adding any factor to the regression model, it is crucial to ensure that the factor still has an impact on stock returns in the presence of other factors, meaning it provides incremental information. Additionally, there should not be significant correlations among the factors. If factors are collinear, the estimated parameters will fluctuate greatly, losing their meaningful interpretation.
    

Generally speaking, in a risk model, more factors are not always better, and a higher in - sample \( R^2 \) is not necessarily desirable either. Overfitting within the sample can lead to poor out - of - sample performance. Therefore, under the premise of maintaining fitting accuracy, fewer factors may result in better out - of - sample robustness (the ability of a system to maintain certain performance characteristics under uncertain disturbances), meaning the model is less likely to fail and more stable. Overall, evaluating the quality of a risk model can be approached from multiple dimensions, such as the model's explanatory power, the stability and significance of factors, and the differences in model performance between in - sample and out - of - sample data.

  

## Q35: What Are the Uses of Risk Models?

The previous sections introduced the main components of risk models, including factor exposures, factor returns, and idiosyncratic returns of individual stocks. Through quantitative methods, we estimated factor returns, idiosyncratic returns, factor covariance matrices, and idiosyncratic risks over time, providing a detailed decomposition of individual stock returns. It is precisely because of this decomposition that the problem of studying the returns of more than 4,000 stocks in the entire market is transformed into studying factor returns and idiosyncratic returns, greatly simplifying the research dimensions and improving the precision of parameter estimation. So, what are the practical applications of risk models in investment? Here are a few common use cases.

1. **Portfolio Risk Exposure Control**: As mentioned earlier, these factors can have both positive and negative impacts on stock returns at different times. To make a portfolio immune to the influence of such style or industry factors, the risk exposure can be set to 0, meaning the entire portfolio is not exposed to that style, or the style exposure is 0. In this way, no matter how the factor return of the style factor changes, it will not affect the portfolio's relative performance. Additionally, by controlling the portfolio's exposure to risk factors, investors can gain a deeper understanding of which styles the portfolio is inclined towards and which styles it avoids, providing a more profound insight into their investment portfolio.
    
2. **Portfolio Attribution Analysis**: If it is known which industry factors and style factors the portfolio is exposed to, the portfolio's performance can be understood based on the performance of these factors. Conversely, attribution analysis of the investment portfolio can be conducted. For example, if an investment portfolio performs well during a certain period, it may be because a particular factor has performed well recently, and the portfolio happens to have significant exposure to that factor.
    
3. **Portfolio Optimization**: Risk models make it possible to directly optimize portfolios and select stocks from a large pool. The simple understanding of portfolio optimization is as follows: an investor wants to select some stocks from a stock pool that have higher expected returns but do not expose too much risk. For example, the investor may not want to deviate too much from certain industries for fear of making the wrong industry bet. In terms of style, the investor can judge the direction and degree of deviation based on experience. If the product being managed is an index - enhanced fund, the tracking error relative to the benchmark index needs to be controlled. Given all these constraints, risk models are essential for completing portfolio optimization and obtaining a stock selection that meets the investor's requirements.
    

  

# Portfolio Management: 6 Questions

## Q36: The Role of Portfolio Management Models

The role of portfolio management models is to bridge the gap between strategy research and investment trading, transforming individual stock Alpha models into portfolio models that output a set of stock weight data. Although quantitative investment Alpha models can comprehensively score and evaluate the relative merits of each stock in the market from multiple dimensions, they cannot directly translate research findings into investment portfolios. Quantitative investment models emphasize diversification, investing in portfolios rather than individual stocks. These portfolios typically contain dozens or even hundreds of stocks, making it impractical to manually select and determine weights for each stock. Therefore, quantitative investors need to rely on portfolio management models to complete the transformation from Alpha models to investment portfolios. These models take individual stock Alpha returns as input, select stocks from the sample space, refer to the stock weights, style exposures, and industry weights of the benchmark index, while also considering trading restrictions and controlling turnover rates. Through methods such as ranking and portfolio optimization, they ultimately generate a list containing the weight data of each stock in the target portfolio. Unlike traditional subjective investing, quantitative investors trade directly in the form of portfolios.

  

## Q37: The Evolutionary History of Portfolio Construction Methods

There are multiple methods for portfolio construction, and they have evolved over time.

1. **The simplest method of portfolio construction is ranking - based stock selection.** After obtaining the Alpha returns of individual stocks, stocks are directly ranked from highest to lowest within the sample space, and the top N stocks with the highest rankings are selected. When weighting, an equal - weight or market - cap - weighted approach is typically used, meaning each stock is treated equally or weighted according to its market capitalization. The advantage of this method is that it can directly select stocks with high Alpha returns. However, the downside is that it does not impose limits on the portfolio's style exposure or industry weights, which can lead to significant deviations from the benchmark index.
    
2. **Market - cap - neutral or industry - neutral stratified stock selection.** The method involves first grouping stocks within the sample space by market capitalization or industry. Within each group, stocks are ranked by Alpha returns, and the top N stocks with the highest rankings are selected. Finally, a portfolio is formed. When weighting, each group is first assigned the same weight as the corresponding group in the benchmark index, and then equal - weight or market - cap - weighted approaches are applied within each group. The advantage of this method is that it balances Alpha returns with benchmark characteristics, resulting in a portfolio with smaller deviations from the benchmark index.
    
3. **Using an optimizer to control the portfolio's exposure to risk factors and industry weights to be the same as the benchmark, while maximizing the portfolio's Alpha returns under this premise, allows for better risk constraints.**
    
4. **Combining risk models and incorporating the consideration of estimated portfolio risk during optimization, using Harry Markowitz's Modern Portfolio Theory to maximize risk - adjusted Alpha returns.** The resulting optimized portfolio can not only meet a variety of constraints but also achieve a balance between expected returns and risks. Most quantitative investors now adopt this method of portfolio construction.
    
      
    

## Q38: How to Efficiently Implement Portfolio Optimization

The theoretical foundation of portfolio optimization is Harry Markowitz's Modern Portfolio Theory. Investing is essentially about making choices between uncertain returns and risks. Portfolio theory characterizes these two key factors using mean - variance. The mean refers to the expected return of the portfolio, which is the weighted average of the expected returns of individual securities, with weights being the corresponding investment proportions. Variance refers to the variance of the portfolio's returns, characterizing the risk of the portfolio. The core viewpoint of portfolio theory is that rational investors should pursue the maximization of risk - adjusted returns. That is, given a level of expected risk, they should seek to maximize expected returns; given a level of expected returns, they should seek to minimize expected risk. If the portfolio's expected volatility is taken as the x - axis and the expected return as the y - axis, a curve called the efficient frontier can be drawn, representing the maximum expected return at different levels of risk. In the actual investment process, quantitative investors need to use optimizers to complete portfolio optimization. Optimizers can be built by the team's research or purchased from international professional institutions' optimizer products, such as the Barra model or the Axioma model. Additionally, in the actual investment process, quantitative investors need to add numerous constraints to the portfolio optimization process, such as portfolio turnover rate, stock weight deviation, risk - adjustment coefficient, and deviations in style and industry factors, to ensure that the final portfolio meets investment requirements.

  

## Q39: What Are the Inputs and Outputs of Portfolio Optimization?

Taking an index - enhanced strategy as an example, portfolio optimization requires multiple inputs:

1. **Individual Stock Alpha Returns**: These are obtained from the Alpha model.
    
2. **Strategy Sample Space**: Although an index - enhanced strategy can select stocks from the entire market, it typically restricts the weight of index constituent stocks to no less than 80% of non - cash assets.
    
3. **Tradable Space** : The sample space alone is insufficient. Certain stocks may be illiquid or too risky and need to be excluded.
    
4. **Benchmark Index Weights**: Since an index - enhanced strategy must be benchmarked to a specific index, it is crucial to strictly control the deviation of the investment portfolio from the benchmark index.
    
5. **Various Constraints**: These include tracking error, style factors, industry factors, turnover rate, industry weights within the benchmark, stock weight deviations, total active weight, etc. The purpose is to control the portfolio's tracking error.
    
6. **Risk Model Inputs**: This includes each stock's exposure to style factors, exposure to industry factors, residual risk, and the covariance matrix of risk factors. These inputs allow the optimizer to estimate the portfolio's risk.
    
7. **Optimizer Output**: The output is a list containing the weight of each stock. The sum of all stock weights equals 1, and the number of stocks typically ranges from dozens to hundreds.
    
      
    

## Q40: What Risk Controls Are Commonly Implemented in Portfolio Optimization?

1. **Turnover Rate Limitation**: Generally, a higher turnover rate can lead to higher pre - cost portfolio returns. However, considering transaction costs, the actual return may decrease. Therefore, it is necessary to control the turnover rate to avoid unnecessary and excessive trading.
    
2. **Style Factor Exposure and Industry Weight Deviation Control**: In risk models, portfolio risk is determined by style risk, industry risk, and residual risk. Residual risk is reduced through diversification, while style and industry risks are mitigated by controlling factor exposures. For example, the market - cap factor is a crucial style factor, as stocks of different market caps can have significantly different returns. During portfolio optimization, it is essential to control this factor and align it with the benchmark index. Additionally, industry weights are usually subject to neutrality constraints. For instance, if the benchmark index has a high weight in the consumer sector, a significant under - or over - allocation in the portfolio's consumer sector can lead to substantial return deviations.
    
3. **Stock Weight Deviation Control**: Smaller stock weight deviations result in a more diversified portfolio, less deviation from the benchmark index, and lower residual risk. This can be controlled by managing the portfolio's total active weight.
    
4. **Tracking Error**: Since risk models can estimate portfolio risk, tracking error can be directly constrained during optimization. It is important to note that risk control should be moderate to find a balance between returns and risks. If risk control is too strict, resulting in minimal deviation from the benchmark, the potential for excess returns will also be low. Conversely, if risk control is too loose, leading to significant deviation from the benchmark, investment returns become unpredictable, with the possibility of either significantly outperforming or underperforming.
    
      
    

## Q41: Common Issues in Portfolio Optimization

**Issue 1**: Optimizers generally have solutions, but when constraints are too strict or two constraints conflict, the optimizer may have no solution. For example, if a factor is required to have a positive deviation of 3 from the benchmark exposure, and in the entire A - share sample space, all stocks' market - cap factor exposures are within ±3, it is impossible to construct a portfolio if no stock in the optimization sample space can achieve a positive deviation of 3. Another scenario is when two constraints conflict. For instance, if the portfolio is required to achieve certain exposures in several factors, and the exposure requirements are extreme, the number of stocks that can meet these requirements is already limited. Finding a combination that satisfies multiple extreme requirements may not be possible.

**Issue 2**: Constraints not taking effect. This is because there are two types of constraints in the optimizer: hard constraints and soft constraints. Hard constraints are those that must be met; if they cannot be satisfied, there will be no solution. Soft constraints are non - essential; if they cannot be met, the optimizer will still produce an output, but the constraint will be ineffective.

**Issue 3**: Mismatch in the magnitude of Alpha predictions and risk predictions. Since the optimizer's objective function is risk - adjusted return, a coefficient needs to be set. If this coefficient is too large, the expected return in the objective function will be too small to have any effect, and the optimization goal will purely become minimizing risk. If the coefficient is too small, the expected risk in the objective function will be too small to have any effect, and the optimization goal will purely become maximizing return without considering risk.

  

# Q42: What Is an Optimizer? How to Understand the Role of Portfolio Optimization in Quantitative Investing?

## I. What Is an Optimizer?

An optimizer serves as a crucial bridge between predicted signals and target positions. In this process, return forecasts, risk forecasts, and transaction costs collectively serve as data inputs to the optimizer, which then optimizes the position weights according to the product's objectives. Within the optimizer, different selection constraints are applied based on the forecasting horizon and the optimization goals corresponding to different product lines, ultimately achieving the optimal target positions under these constraints. The underlying model frameworks for various product lines such as quantitative long - only (including index - enhanced and full - market stock selection) and quantitative hedging are interconnected. They are all built on the same "quantitative stock - selection" model to create differentiated product lines that cater to the varying risk preferences and investment needs of different investors.

## II. What Is Portfolio Optimization?

In finance, the origins of portfolio optimization can be traced back to the 1950s when American economist Harry Markowitz first introduced the Portfolio Theory. He conducted systematic and in - depth research on the mean - variance analysis method and the efficient frontier model of portfolios, for which he was awarded the Nobel Prize in Economics in 1990. Markowitz argued that when investors allocate assets, they need to consider the relationship between the risks and returns of different assets to achieve the optimal state of the entire investment portfolio. This means maximizing the expected return for a given level of expected risk or minimizing the expected risk for a given level of expected return. This theory laid the foundation for modern finance, and the concept of portfolio optimization has since been applied to other fields, providing new approaches to solving optimization problems.

## III. The Application of Portfolio Optimization in Quantitative Investing

Quantitative investing can generally be divided into six stages: data collection, data cleaning, feature extraction, model development, portfolio optimization, and trade execution. In a broad sense, portfolio optimization encompasses all the engineering details from predicted signals to trade execution. In a narrow sense, portfolio optimization involves combining the predicted signals provided upstream and other inputs (such as risk models and transaction cost models) to determine the desired positions at each point in time. In other words, it is the step of converting return forecasts into position weights.

Portfolio optimization is an important independent branch of operations research that seeks the optimal arrangement, grouping, sequencing, or selection of discrete events through the study of mathematical methods. Currently, portfolio optimization algorithms are mainly divided into four categories: mathematical optimization algorithms, heuristic algorithms, meta - heuristic algorithms, and machine learning methods. Among them, the machine - learning - based solution paradigms for portfolio optimization problems can be divided into end - to - end solutions and locally - improved solutions.

Building a portfolio generally involves two steps: determining the investment targets to be allocated and assigning the position weights for each target. A rational portfolio exists but is not unique. For example, investors with different risk preferences generally have different levels of suitability for the same portfolio. Therefore, there is no single optimal solution for an investment portfolio; it is a sub - optimal solution based on comprehensive considerations.

In quantitative investing, portfolio optimization is used to calculate the maximum value of the objective function under constraints, generating specific position weights. In setting up the optimizer, it is necessary to first determine the optimization goals and constraints. Subsequent adjustments are dynamic and iterative - which can be simply understood as "continuously running backtests, receiving analysis results, and then making feedback adjustments."

### 1. Optimization Goals

Different managers often have different optimization goals for different product lines. Common optimization goals include minimizing portfolio volatility (variance), maximizing portfolio returns, minimizing tracking error relative to a benchmark index, and maximizing the portfolio's Sharpe ratio. Under different optimization goals, even the same "quantitative stock - selection" model can result in vastly different risk - return profiles for product performance.

### 2. Constraints

In terms of constraints, industry constraints, risk constraints, and individual stock constraints are all key parameters to consider:

- **Industry Constraints**: It is possible to set upper and lower limits on the allocation ratios for all industries and also to make personalized settings for individual industries.
    
- **Risk Constraints**: Certain parameter configurations, such as the weight of a particular factor, can be manually adjusted to better monitor the factor's performance in actual investments by controlling risk exposure.
    
- **Individual Stock Constraints**: These focus on liquidity limits and market - cap limits. The former helps reduce transaction slippage during portfolio rebalancing, while the latter mainly considers issues such as "reaching the disclosure threshold for significant shareholdings" to avoid unnecessary attention or over - interpretation.
    

  

# Q43: Execution Methods and Costs in Stock Trading

**Active Orders**: These are orders where the trader initiates a trade at the counterparty's quoted price. For example, buying at the ask price or selling at the bid price. The simplest form of active trading is a **Market Order** , which enters the market at the current market price. From a trading perspective, a market order is an aggressive approach. A more rational strategy would be to sell at a higher price and buy at a lower price. However, a market order sacrifices this potential for better pricing in exchange for the opportunity to enter the market more quickly. If the order size is large, it can significantly impact the market price, leading to what is known as **market impact cost** .

**Passive Orders**: These are orders where the trader places a quote and waits for a counterparty to execute the trade. For example, buying at the bid price or selling at the ask price. If an active order is a market order, then a passive order is a **Limit Order** . A limit order is executed when the price reaches a pre - set level. The trader passively waits for the market to reach their desired price. The downside of passive orders is that the execution time is uncertain, and the trader may miss out on favorable price movements, incurring an **opportunity cost** .

**Market Impact Cost**: When a large order is placed, it can move the market price. For example, if you need to buy 10 million shares of a stock, the first 5 million shares might be bought at the current ask price, but the next 5 million shares might require a higher price. This price movement due to trading is called **market impact cost** .

**Opportunity Cost**: For passive orders, the cost is the potential gain lost by not executing the trade immediately. For example, if you place a buy order at the bid price but the price rises before your order is filled, you miss out on the opportunity to buy at a lower price.

  

# Q44: What Are Slippage and Impact Cost?

**Slippage and Its Influencing Factors**:

Slippage refers to the price change between the time a trader decides to execute a trade and when the order is actually filled. Common factors influencing slippage include:

- **Trading Volume of the Strategy**: If the strategy's trading volume exceeds the average market depth, it can cause a discrepancy between the execution price and the expected price, leading to slippage costs.
    
- **Market Trading Volume**: Higher market volumes can accelerate price movements, increasing trading costs.
    
- **Market Volatility**: More volatile markets can lead to larger price changes between order placement and execution.
    
- **Anonymity of the Trading Channel**: More anonymous channels may reduce the impact of large orders on the market.
    
- **Order Placement Method**: Different methods of placing orders can affect the likelihood and magnitude of slippage.
    
- **Speed of Strategy Profit Realization**: Strategies that require quick execution may face higher slippage due to the need for immediate market entry.
    

**Impact Cost**:

Impact cost, also known as "price impact cost," measures the liquidity of the stock market or the cost of liquidity. It reflects the price change caused by the execution of a large order. When you buy all the desired shares, the cost is often higher than initially anticipated. This cost includes both immediate price changes (slippage) and longer - term effects on the market price.

According to the "Shanghai Stock Exchange Market Quality Report (2023)," the price impact index for trading 100,000 yuan worth of stocks has remained around 15 - 16 basis points in recent years. For trades of 250,000 yuan and 900,000 yuan, the price impact indices are approximately 23 - 24 and 50 - 52 basis points, respectively. Huabao Securities, in its financial engineering report "Where Is the Comfort Zone for Index - Enhanced Strategies?" observed that since 2023, the overall trend for public and private index - enhanced products has been a decline in impact costs.

**Reducing the Impact of Trading Costs**:

Trading costs can be divided into direct and indirect components. Direct costs include transaction commissions, stamp duty, transfer fees, and other taxes. In China's stock market, the main fees for individual investors include securities transaction commissions, transfer fees, regulatory fees, handling fees, and stamp duty. Since August 28, 2023, the securities transaction stamp duty has been reduced by half.

Indirect costs mainly refer to impact costs, including slippage, which are closely related to the quality of actual trading. Algorithmic trading is a manifestation of the精细化 development of trade execution. It determines the optimal execution path, timing, price, and quantity of orders (e.g., splitting large orders into smaller ones) to achieve efficient and stable trade execution and optimal trading results. This helps to smooth market impact and reduce trading costs.

Buy - side and sell - side trading costs differ, with buy - side costs generally being lower than sell - side costs, mainly due to stamp duty. The three major exchanges also have different charging standards, with the Beijing Stock Exchange having lower handling fees than the Shanghai and Shenzhen Stock Exchanges. In the securities holding phase, investors are only subject to dividend tax, and the longer the holding period, the lower the tax rate, which encourages medium - and long - term equity investment.

For asset management institutions with a certain scale, diversifying sources of returns, spreading positions, and using algorithmic trading to optimize order execution can help reduce the impact of trading costs on excess returns. In an industry with a scale exceeding one trillion, quantitative private equity managers tend to adopt turnover rates that match their current management scale. Currently, in China's main quantitative private equity products, medium - cycle strategies (with an annual turnover rate of about 30 - 50 times) account for a higher proportion, while short - cycle strategies are gradually declining. As the scale increases, the average holding period will further lengthen.

  

# Q45: How Algorithmic Trading Reduces Trading Costs

Algorithmic trading aims to:

- Minimize trading costs, such as market impact costs.
    
- Achieve an average execution price close to the target price, such as the market - weighted average price.
    
- Conceal order - placement intentions.
    
- Address other non - technical reasons, such as saving labor costs, improving order - placement efficiency, and ensuring accurate order execution.
    

**Common Trading Algorithms**:

- **TWAP (Time - Weighted Average Price)**: This algorithm splits the order to match the time - weighted average price over a specified interval. For example, if you need to buy 1 million shares over the next 3 hours, the algorithm will place orders every 10 minutes, resulting in 18 trades over 3 hours, with each trade being 1,000,000 / 18 shares. The advantage of TWAP is its simplicity, making it suitable for liquid stocks or smaller - sized trades. However, it has limitations because market volumes fluctuate, and evenly distributing fixed quantities is not always reasonable, leading to larger intraday impacts.
    
- **VWAP (Volume - Weighted Average Price)**: The core of VWAP is to minimize the difference between the actual execution price and the market's volume - weighted average price, thereby reducing market impact costs. Unlike TWAP, VWAP does not directly model market impact costs but focuses on predicting intraday trading volume distribution and then splitting and executing large orders accordingly. For example, if you need to execute a large trade within a certain trading period, the VWAP algorithm will first divide this period into N equal intervals. It will then use historical data to determine the trading volume distribution within each interval and place orders accordingly. Assuming each order is executed, the average execution price will closely match the market average price.
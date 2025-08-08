# Whitepaper 2.0

## Intro and Vision

### Background: High Volatility, Asymmetric Access to Alpha

Retail traders in crypto markets face significant challenges: limited information, rapid market swings, and opaque access to alpha-generating systems. Studies, including Binance Research, indicate that **70%–90% of retail traders incur net losses within weeks** of active trading[^1][^2].

This is especially pronounced in speculative segments—low‑cap tokens, memecoins, and emerging launches. For instance, platforms like pump.fun handle **over $300 million in daily trading volume** (mid‑2025)[^3], predominantly driven by retail participants acting on minimal or no structured analysis.

Meanwhile, **alpha signals and sophisticated execution tools remain concentrated in institutional systems**. Retail participants lack seamless access to real‑time data pipelines, backtesting infrastructure, or scalable strategy engines. This concentration of advantage creates structural imbalance:
- Retail traders rely on public, often delayed information  
- High-risk strategies are pursued without systematic risk filtering  

There was a signincant progress to address the problem from different angles, but to this day only specific segments were addressed. 

### Current Tool Landscape: What Exists Today 

| Tool        | Primary Function                            | Key Characteristics |
|-------------|---------------------------------------------|---------------------|
| **Mamo**    | AI-powered personal finance & yield agent   | Offers automated yield optimization and financial recommendations on the Base blockchain[^4] |
| **GMGN.AI** | Meme-token sniper with risk filters         | Offers honeypot checks, liquidity tracking, wallet monitoring, and sniping tools on Solana[^5][^6] |
| **AIXBT**   | Narrative & social sentiment intelligence   | AI-powered detection of emerging trends via social media and on-chain data for terminal users[^7][^8] |
| **3Commas** | Automated trading bots across exchanges      | Provides DCA, grid, signal bots, SmartTrade, backtesting, and TradingView integration; over $400B traded[^9][^10] |
| **Axiom Trade** | High-speed execution & analytics interface | Hybrid web platform for Solana memecoins; features wallet/Twitter tracking, MEV-resistant execution, and reward systems[^11][^12] |

### Persistent Market Gap: High-Risk/High-Reward Trading Infrastructure

These tools cover:
- **Automated yield or risk-managed strategies** (e.g., Mamo)  
- **Sniping and execution for fast-moving tokens** (e.g., GMGN.AI, Axiom)  
- **Narrative insight without execution** (e.g., AIXBT)  
- **General-purpose bot execution for variable risk levels** (e.g., 3Commas)

**But none combine:**
- Real-time on-chain data‑driven alpha discovery  
- Full automation, trading 24/7 without the direct user involvement  
- Fair, probabilistic distribution of low-capacity, high-conviction trades to a broad retail base  
- Retaining the control and the ownership to the user

Despite the high volume and retail demand, the **high-risk/high-reward segment remains structurally underserved**.

### SQDGN: Addressing the Niche with Data-Driven Co-Piloting

**SQDGN** (ticker: `$SQDGN`) is designed to fill this void by integrating:
1. **SQD Network** — real-time and archival on-chain data, onboarding token launch events, liquidity flows, and smart contract signals;  
2. **AI-driven alpha discovery models** — detect nascent high-upside opportunities through behavior patterns and market microstructure;  
3. **Probabilistic signal distribution** — fairly allocates low-capacity, high-conviction signals across users according to their stake, preferences, and risk profile.

This approach enables:
- Access to systematized alpha in fringe, high-volatility markets  
- Structuring of volatility rather than blind exposure  
- Retail-scalable participation with agent-supported intelligence  
 

## SQDGN Terminal: Personalized Trading Co-Pilot for On-Chain Markets

The SQDGN Terminal is a web-based application where users can deposit capital, define trading preferences, and delegate execution to a personalized AI agent. It operates at the intersection of agent-based execution, real-time alpha discovery, and user-in-the-loop oversight.

Unlike execution bots or dashboards, the SQDGN Terminal maintains a continuously evolving pool of alpha strategies and offers scalable infrastructure for strategy discovery, probabilistic distribution, and execution — tailored for both high-risk, high-reward strategies and lower-risk, higher-capacity ones.

### Architecture Overview

The architecture consists of three core components:

1. **Alpha Seek (Strategy Pool & Discovery Engine)**  
2. **Alpha Distribution**  
3. **Execution Layer**  

Each user is represented by a **User Agent**, which interfaces with Alpha Distribution and reflects the user’s preferences and tier-based capabilities.

<p align="center">
  <img width="90%" alt="SQDGN Terminal Architecture" src="https://gist.github.com/user-attachments/assets/9882bdb6-9723-48e8-92ca-e1ae1ceed24f" />
</p>


### 1. Alpha Seek (Strategy Pool & Discovery)

The **Alpha Seek** engine continuously maintains a hidden pool of trading strategies sourced and updated from real-time blockchain data (via SQD Network). Strategies span the full risk spectrum:

- **High-upside, low-liquidity** opportunities (e.g., early-stage memecoins)
- **Mid-risk, mid-cap** event-driven setups
- **Lower-risk, higher-capacity** strategies designed for larger position sizing

Key properties:

- Strategies are periodically backtested and retired to mitigate **alpha decay**
- Capacity constraints are modeled per strategy based on DEX liquidity and volatility
- Performance metrics such as Sharpe ratio, max drawdown, and win/loss streaks are stored, though internal logic remains private to prevent exploitation

The system supports dynamic rebalancing and prioritizes freshness and signal quality.


### 2. Alpha Distribution

The Alpha Distribution layer receives strategy-level trade signals from Alpha Seek and determines eligibility and allocation among users.

Each user is paired with a **User Agent**, which:

- Ingests the user's **personalized preferences**
- Submits **conviction bids** for relevant signals (based on risk/return fit)
- Tracks recent history, available capital, and tier level

The allocation mechanism is **probabilistic**, ensuring that:

- **Signal capacity is respected**
- **Higher-tier users** receive increased statistical access to scarce alpha
- **Retail users** at lower tiers still have non-zero opportunity

The system avoids alpha monopolization and allows scalable signal delivery without overfitting or crowding.

### 3. Raffle → Ordering → Execution

Once conviction bids are collected:

- A randomized **raffle** is performed based on conviction and tier weight
- Winning users are **rank-ordered** and grouped by execution batch
- Trades are executed via **Account Abstraction (AA)** wallets using temporary session keys

Constraints:

- Position sizing is capped to **signal capacity**
- Slippage is monitored and tracked per execution

All trades are non-custodial: users maintain direct control over funds at all times.

### User Personalization & Oversight

Personalization operates at two levels:

1. **Static configuration** — Upon onboarding, users select:
   - Risk appetite
   - Position size constraints
   - Strategy category preferences

2. **Dynamic agent modeling** — Over time, the User Agent adapts based on:
   - Historical PnL and trade behavior
   - Adjustments to risk model
   - Tier-based access to advanced strategies

Users at higher tiers (**Shark** and **Kraken**) additionally receive:

- Access to **open position inspection**
- Option to **adjust or close trades manually**
- Access to the incoming signals and positions via an API to enable **evaluation by extrernal tools**

This ensures that advanced users can combine AI-assisted execution with discretionary decision-making when needed.

---

In summary, the SQDGN Terminal provides:

- Multi-strategy support with constant refresh and decay mitigation  
- Preference-based user agent bidding and risk targeting  
- Probabilistic but fair signal access with tier-aware weighting  
- Structured execution with optional human-in-the-loop overrides  

## SQDGN Token and Treasury

### Overview

The $SQDGN token powers the SQDGN Terminal and its tiered access system. By staking $SQDGN, users unlock reduced fees, larger position limits, prioritized access to signals, and advanced features. The token also serves as a coordination and incentive layer for long-term protocol sustainability.

### Fee Structure

The SQDGN Terminal charges two types of fees:

1. **Position Open Fee**  
   A fixed fee applied once, at the moment of trade initiation.  
   → **Waived entirely for Kraken tier users.**

2. **Performance Fee**  
   A percentage of the open position, collected only when a trade is closed or reduced.  
   → **Scales down significantly with higher tiers.**

This model ensures that usage and value extraction are directly aligned with real trading activity and success.

### Tier Matrix

| Tier         | Stake ($SQDGN) | Open Fee       | Performance Fee | Max Open Positions | Max Position Size | Deposit Cap   | Raffle Allocation | Target Users |
|--------------|----------------|----------------|------------------|---------------------|--------------------|----------------|-------------------|--------------|
| 🐣 **Free**     | None           | $1.00           | 2.0%             | 1                   | $10               | $100           | Low               | **Crypto-curious users** testing the system with minimal capital. Entry-level access. |
| 🥉 **Krill**    | 500,000        | $0.75           | 1.5%             | 3                   | $100              | $1,000         | Medium-Low        | **Retail traders** with small allocations seeking access to structured alpha. |
| 🥈 **Bluefin**  | 1,000,000      | $0.50           | 1.0%             | 10                  | $500              | $10,000        | Medium            | **Power users** who understand market mechanics but prefer guided execution. |
| 🥇 **Shark**    | 5,000,000      | $0.10           | 0.3%             | 20                  | $5,000            | $100,000       | High              | **Pro and semi-pro traders** using SQDGN to diversify, scale up, or automate part of their execution. |
| 🏆 **Kraken**   | 10,000,000    | None            | 0.1%             | Unlimited           | Unlimited         | Unlimited      | Highest           | **Small funds and DAOs** seeking advanced configuration, deeper strategy curation, and full agent integration. |

### Advanced Features

Advanced features include:
- API access to the signals (available for **Shark** and **Kraken** tiers)
- Access to experimental strategies
- Deep customisation and the possibility to deploy custom strategies (only for **Kraken** tiers)
- Manual overrides to smart DCA, sniping, position management (available for **Bluefin**, **Shark** and **Kraken** tiers)
- **Shark** and **Kraken** tiers get priority early access to new markets and features (e.g. perpetuals markets)

Over time, the user agents making execution bids will evolve into a full-fledged digital squid avatars, and then higher tiers will get access to additional perks and boosts (eg to unlock new strategies or increase the odds of winning bids temporarily). Lower tiers will be able to purchase the boosts in the app.

### Subscription Access

Tiers can also be unlocked via a **monthly subscription** (non-staking path), priced dynamically based on platform demand. Subscriptions provide flexibility for users who prefer not to lock tokens.


### Treasury and Revenue Allocation

All fees collected by the protocol are allocated across three major channels:

#### 1. Protocol Treasury

- Supports infrastructure costs ($SQD Network fees, AI models, execution systems)
- Funds ongoing development, data expansion, and ecosystem R&D
- Marketing, including hackathons and integrations
- May be governed by a DAO of long-term token holders

#### 2. Buyback and Lock Mechanism

Rather than permanently burning tokens, SQDGN employs a **Buyback & Lock** mechanism:

- A portion of protocol fees (e.g., 25–40%) is used to **market-buy $SQDGN**
- Purchased tokens are then **locked** in:
  - A long-term staking vault, distributing rewards over time  
  - Protocol-Owned Liquidity (POL) positions to deepen DEX market depth  
  - Or escrowed community incentives (e.g., strategy mining, retro rewards)

> This mechanism creates **persistent buy pressure** while reinforcing long-term token alignment. Unlike burn models, value is recycled into the staking and reward ecosystem.

#### 3. Strategy Capital Reserve

A small portion of fees may be allocated to the treasury as operational capital for:

- Reinvesting in high-performing internal strategies
- Stress-testing new models
- Offering “signal mining” bounties to data scientists and quants

### Token Utility Recap

The $SQDGN token provides:

- Tiered access to the SQDGN Terminal (staking- or subscription-based)
- Reduced fees and increased capital allocation for traders
- Improved signal allocation probability via raffles
- Future governance rights over strategy onboarding, fee splits, and treasury deployment
- Participation in **buyback & lock-based value recycling**


## Appendix: Historical Performance

### Prototype Overview

Before the launch of the SQDGN Terminal, the project operated as a **signal-only prototype** under the name *Degen Squid*. The goal was to validate the alpha discovery models and data infrastructure before deploying capital or enabling automated execution.

Two distribution channels were used:

1. **Public X (Twitter) account** — [x.com/helloSQDGN](https://x.com/helloSQDGN)  
   - Posted a subset (~20%) of all generated signals  
   - Signals were **delayed by several minutes** from the original detection  
   - Intended to provide transparency and a public track record

2. **Token-gated Telegram channel**  
   - Accessible to early SQDGN token holders  
   - Received **full, real-time premium signal set** without delay  
   - Functioned as a closed beta for data delivery and community feedback


### Signal Characteristics

The prototype signals represented **potential entry opportunities**, not fully managed trades.  
Each signal included:

- Token contract address
- Recommended entry price (snapshot at detection time)
- Metadata (DEX pair, chain, liquidity level, basic safety checks)

**Important**: In the prototype stage, SQDGN did **not** provide exit recommendations. Closing a position profitably required:

- Manual trade execution
- Monitoring of liquidity and price movements
- Active risk management

The upcoming **Terminal** addresses this by combining signal generation with **automated execution, capital sizing, and position management**, making the process accessible to a wider audience.


### Performance Evaluation Methodology

To assess the raw edge of the signal generation models we analyzed each call as follows:

- For every signal, track the **all-time high (ATH) price** within **7 days** of publication
- Compare this ATH to the signal’s entry price
- Record:
  - Whether the ATH exceeded the entry price
  - By how much (percentage gain)

This approach provides a conservative but clear metric for the **intrinsic value** of the alpha stream, which is further leveraged when integrated into the Terminal’s automated strategy execution.


### Results

#### 1. Signal Win Rates

Percentage of signals where the ATH within 7 days exceeded the entry price.

<img width="1280" height="523" alt="Signal Win Rates" src="https://gist.github.com/user-attachments/assets/9b32aa1a-7a78-4de2-a61d-d82759def600" />

#### 2. Distribution by Returns

Return distribution (ATH within 7 days vs. entry price), showing the frequency of signals yielding various gain ranges.

<img width="1280" height="368" alt="Return Distribution" src="https://gist.github.com/user-attachments/assets/61622a98-e4df-4035-a319-861ea01cbe86" />

#### 3. Top 15 Signals

Best-performing signals over the test period, sorted by 7-day ATH % gain over entry.

<img width="1280" height="679" alt="Top 15 Signals" src="https://gist.github.com/user-attachments/assets/1c43bfea-9158-4892-8ff6-ffbeb2c8e400" />

### Interpretation

Even without execution optimization, slippage control, or risk management, the prototype demonstrated:

- **High signal density** — enough to sustain diversified strategies
- **Consistent edge** — measurable outperformance relative to random token selection
- **Scalability potential** — the underlying models can be applied to multiple chains and liquidity profiles

When combined with the Terminal’s automated entry, position sizing, and execution logic, this signal engine becomes significantly more capital-efficient and retail-accessible.

These results validate the core thesis:  

> The combination of **real-time on-chain data (via SQD Network)** and **AI-powered alpha discovery** produces a defensible edge — which the Terminal is designed to fully capture and scale.

## Appendix: Bid Selection

This technical section will describe the tier levels provide the actual formulas for the probability distribion that should reflect:
- Risk preferences
- User tier/stake tokens
- Capital at risk

The output will be a set of allocations to be sent to the exection.

The details will be addressed in the future versions of the whitepaper.

---
## References
---

[^1]: Binance Research, “Retail Trading Behavior in Perpetual Futures.” 2022.  
[^2]: H. Liu et al., "Empirical Analysis of Cryptocurrency Traders on Binance," SSRN, 2023.  
[^3]: CoinGecko, CoinMarketCap, and DefiLlama report pump.fun (PUMP token) daily trading volumes of ~$300M in mid‑2025.  
[^4]: Messari, “Mamo” profile — AI-powered financial management on Base blockchain.  
[^5]: GMGN.ai site — token sniping with security checks.  
[^6]: Medium post on GMGN Solana bot features sniping, copy trading, wallet tracking.  
[^7]: Crypto.com University, “What Is AIXBT by Virtuals,” March 2025.  
[^8]: Messari profile on AIXBT — AI crypto intelligence from social + on-chain data.  
[^9]: BitDegree review of 3Commas — over $400B traded, bot platform.  
[^10]: 3Commas official features list — DCA/Grid/Signal bots, SmartTrade, TradingView.  
[^11]: Axiom features from official docs — high-speed execution, analytics, wallet tracking.  
[^12]: Medium review of Axiom Trading Bot — feature-rich, Y Combinator‑backed. 

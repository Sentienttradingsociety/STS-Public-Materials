# How We Trade and Why We Share Our Stuff - STS

Text extracted from our private materials that I have decided to publish.

Initially, this was declared privately; I see no harm in making our reasoning public, as I have done in the public Sentient Trading Society materials.

This was originally presented in a well-formatted document with extra sections
to provide further insight into what we do and our choices regarding paths toward institutional trading.

## Why We Share Our Stuff

Sharing our frameworks serves a precise and strategic purpose for us.

There are many private traders engaged in the financial markets, but the people who have discipline, skills, and independence to execute things are very few.

By separating out the noise and dealing only with serious people, we build a highly competent team that understands the same processes that we do.

We know it is tough; that is the point.

Those who lack the discipline or capability will filter themselves out. 

This allows us to work with talented people and expand our ecosystem. 

The barrier to entry is bound by effort, keeping conflicts of interest low and ensuring our arrangement remains mutually beneficial.

## How We Trade

STS's primary framework relies on these core pillars.

### 1. Strict Strategy Filtering:

Our strategies are developed through a process that includes in-sample testing, out-of-sample testing, and stress testing. The focus is on the behaviour of the strategy in various market environments, and how much of the strategy's performance remains intact when reasonable changes are made during development, e.g., a 20% change in a filter's settings. 

Without such checks, we do not see the system as serious, and real capital is at risk.

Few strategies ever meet our requirements for deployment by design to avoid selection bias. "Profitability" alone is not enough; if you backtest enough strategies, one will print a positive equity curve by pure chance. 

We aim to build fewer and validate from the smaller sample of strategies that survive our internal testing framework; testing 10 strategy ideas and deploying 3/10 is better than testing 100 strategies and deploying 3/100. 

We also recognise sequencing risk, which we describe as the order in which profitable and losing trades occur. This is beyond every trader's control, which is why we encourage partitions and withdraw systematically.

The same strategy can produce materially different equity paths depending on the exact day it was deployed, and there is no hindsight-free, absolute method to optimise when a strategy is deployed; a strategy can face a drawdown as soon as it starts or experience consecutive profitable positions like never seen before in tests - we have experienced both.

This is why we pay close attention to capital allocation, withdrawals, and isolating individual trading systems.

### 2. Partitioned Isolated Risk (One Strategy Maximum Per Account): 

In our framework, total capital is strictly partitioned into independent trading accounts. Each account runs an uncorrelated strategy with pre-defined risk values. 

This arrangement allows us to deploy different risk profiles simultaneously without forcing them into a shared equity curve. A loss on one strategy does not automatically reduce the profitability of another strategy. For this, we seek strategies with low dependence on one another, while recognising that correlations and market relationships can change during stressed conditions (e.g., Tariffs in 2025 - discussed in the STS materials with drawdowns displayed).

### 3. Elevated Risk In Isolated Environments:

For example, an individual with $100,000 of available capital might allocate $10,000 to each of three strategies, leaving the remaining $70,000 liquid and outside those trading accounts.

The strategies might operate with respective risk parameters of 8%, 6%, and 4.5% per trade. These percentages are calculated against the relevant strategy allocation ($10,000), not the entire $100,000. In the first example, an 8% planned loss on a $10,000 strategy balance represents $800 of intended risk at the defined stop. 

These risk percentages might look high at first glance.

To have a look at how they can work in practice, let us look at the numbers behind two consecutive 4R wins (where profit equals 4x the risk taken).

**$100,000 Account (0.8% Risk) - Entire Capital at Risk While Trading with Margin.**

After Trade 1: $103,200.00 (+3.20%)

After Trade 2: $106,502.40 (+6.50%)

**$10,000 Account (8% Risk Per Trade) - A 1/10 Partition of Capital at Risk.**

After Trade 1: $13,200.00 (+32.00%)

After Trade 2: $17,424.00 (+74.24%)

$7424.00 gain vs $6502.40 is a 14.2% increase in gains from risk isolation.

**100 trades with a 1:2 RRR and 50% win rate before transaction costs.**

0.8% risk on $100,000 over 100 trades = $48,009 in gains (median)

8% risk on $10,000 over 100 trades = $248,399 in gains (median)

Local jumps in percentages do not need to be as extreme to benefit; a 10x % upscaling in exchange for a global 90% reduction to capital at risk was used to make comparisons clear.

Across 100 trades on this strategy’s stats at 8% risk, there is around a 25% chance of a local drawdown reaching 50% or more (-5% of total capital), while the remaining of the trader’s operating capital (90%) remains untouched.

**$800 risk executed on $10,000 is materially only 0.8% of the $100,000 total capital at the start, and the rest of the capital is separated to isolate drawdowns; a bad run is exposed only to the active partition while the remaining $90,000 reserve stays untouched.**

This can create a curve where winning runs grow capital faster than losing runs shrink it, known in quantitative finance as convexity.

Only one position is held open at any given time, and an active trade does not cancel out a subsequent setup. The strategy is explicitly designed to reduce position-based path dependence. If positions were allowed to overlap (such as entering a short setup while a long position is active), the strategy would lack proper isolation. Because each setup functions as an independent strategy, overlapping trades would interfere with compounding and free margin.

Separating accounts can also stop one setup from dragging down another.

For example, a loss of 10.00% and a gain of 10.00% results in a loss of -1.0% net; if separated, the loss can produce a more positive outcome. This scales with leverage.

For accessibility, I calculated these examples under a basic trade sequencing model which can be replicated by anyone in a standard calculator; outputs vary, but the potential benefits remain.

Predefined profit thresholds such as skimming at a set gain level or taking a share of realised gains depend on the strategy. Once withdrawals happen mid-run, the sequence of trades can affect the amount taken home.

Over higher samples, the beneficial discrepancy can grow, especially if strategies are uncorrelated. I showed this as a short example going over concepts I implement; the magnitude of improvement is not universal, and will vary depending on the strategies involved and their respective dependencies.

**Many traders who get into testing attempt to inherit institutional risk rules without questioning why those rules specifically exist for institutions.**

Traders have the flexibility to operate like a fleet of speedboats, while many institutions are forced to haul a ship. If you are not answering to outside investors, ask yourself whether your current sizing and account structure are built to protect a smooth equity curve or to harvest asymmetric payouts before market conditions inevitably change.

Do the calculations for your strategies and adjust accordingly; we will revisit this later in the article.

#### Demonstrating how this and splitting can influence financial outcomes over a modest sample.

A $10,000 lump sum example could have strategy 1 working while strategy 2 produces a negative return, neutralising the gains after costs or even resulting in a loss. Account 1 could have a large return, and account 2 is in drawdown, resulting in a net profit.

**Definition:** In this context exclusively, "ruin" corresponds to a -20R return per strategy, defined here as the maximum peak-to-trough drawdown, or a blow-up.

**Example:** Two independent 1:2 RRR systems with a 50% win rate (generic profitable models).

Market 1: 65.79% gain when isolated, 1.5% risk per trade. (35 profitable outcomes, 35 stop-outs).

Market 2: 26.09% loss (reaches ruin, 20 stop-outs, -20R).

Net result: Approximately a 22.5% gain ($2,253 profit), assuming a $10k lump sum was traded across both systems at 1.5% risk per trade. 

The return is significantly lower than 39.7% because the losing system pulled down the returns of the profitable one, as the lower balance values influenced the risk taken by the profitable system.

**Assumptions:** All trades are compounded in the simulation. In real time (opti­mistic), they would not be compounded to this extent (overlapping positions), which is another downside of executing both strategies on the same account.

#### 5k + 5k split (Separated capital partitions)

**Account 1, 5k Partition, 3% Risk Per Position:**

Strategy 1 results in an approximate 164.7% gain with 3% risk, $8,233.84 gain; this is an 82.33% gain on 10k (overall capital) with 35 profitable positions (70R, +668.60%) and 35 individual stop-outs (-35R, -65.56%).

**Account 2, 5k Partition, 3% Risk Per Position:**

Strategy 2 results in an approximate 45.6% loss on 5k (reaches ruin, -20R) or a 22.81% drawdown on overall capital, $2,281 loss (20 consecutive, isolated stop-outs).

Net result: $5,952 gain, 59.52% (10k)

**The difference versus the default lump sum:**

$3,699 more profit compared to the $10k lump-sum account, which mixed both strategies for a net profit of ≈$2.25k, demonstrating a 164% increase in profits from strategy risk isolation and STS-style capital partitioning (59.5% net versus 22.5%). The magnitude of improvements from adopting our risk management styles is not universal, and will vary depending on the strategies involved and their respective dependencies.

As profound as this may seem, it is just one of five basic layers that work together to complement our other foundational processes, as described below.

### 4. Asymmetric Payoff Harvesting (Positive Skew Strategies):

We mostly deploy models with higher variability (higher-skew) designed to absorb frequent, small losses in exchange for rarer, higher-RRR wins. Execution is entirely mechanical, removing intuition to avoid adding noise to the trade sequence and avoid undermining the strategy's statistical validity. Our research includes figures that show the real-world impact of decision noise.

### 5. Withdrawal Optimisation and Contained Return Volatility

Strategies operate with predetermined profit thresholds.

When cumulative returns hit specific pre-defined levels, profits are systematically skimmed and withdrawn away from trading, ensuring that capital is never indefinitely exposed to edge decay.

We can mitigate risk by pairing agency-model or matched-principal CFD execution, supported by a reputable regulator and a genuine liquidity provider list, with explicit contractual negative balance protection or agreed-upon partial coverage or waiving practices. Where possible, we aim to limit each capital partition container's liability to its allocated funds, unlike standard futures accounts. As private traders, we have never owed a negative balance, and we only trade with brokers whose financial interests are aligned with preventing them.

One caveat is that our Sharpe ratios can be lower, as the Sharpe ratio treats all volatility equally, penalising upside variance and downside variance with equal impact.

In a high-skew, tail-risk system Sharpe ratios are skewed to fall on the lower end, despite high expectancy/expected value. 

Because we optimise for large payoffs over return smoothness as private traders, our systems are designed to trade isolated equity curve volatility for asymmetric upside. We are not old-school "fund managers", and we do not optimise for "institutional" Sharpe ratios designed to attract capital allocation through smooth, linear growth.  Traditional metrics penalise the very characteristics that have funded our largest successes.

We found out that when downside risk is mathematically caged through methods like capital partitioning, minimising return volatility becomes counterproductive as a private trader, as it sacrifices the aggressive positioning required to capture rare market anomalies with leverage. We treat each strategy as an expiring asset, and we have designed frameworks to extract value efficiently before its statistical edge inevitably dissolves.
Our IP is reserved exclusively for approved private members.

**Warren Buffett:** Diversification may preserve wealth, but concentration builds wealth.

**My takeaway and perception:** Risking 1-2% per trade on $5,000 has made few, if any, traders serious wealth; it is common advice used to keep new traders from over-risking and keep retail operators engaged long enough to accumulate fees. The retail industry profits from slow survival, and so do educators with broker affiliations.

**Andrew Lo's Adaptive Market Hypothesis:**

**My takeaway:** Markets change, and participants adapt or die with the shifts.

**Murphy's Law:**

**My takeaway:** If it can go wrong, eventually it will; pretending an edge will never decay is unwise.

## Why we trade privately instead of pursuing an institutional route

We looked into this in 2021 after achieving profitability, and in 2025, after finishing university. The truth is the structural mechanics of our framework are misaligned with the fiduciary rules (COI) and risk mandates of traditional institutional asset management, especially after the post-2008 Dodd-Frank Act passed in 2010.

Regulated institutional desks, including hedge funds and traditional prop shops (real prop firms, not retail), operate under strict compliance frameworks and rigid capital-adequacy mandates. This makes the capital partitioning and risk isolation we rely on commercially unsuitable or flat-out inaccessible in an institutional environment because of the need for low margin requirements, amongst other risks that are amplified when managing many millions to billions (such as maximum liability and price impact).

While institutional firms can employ high-risk systematic strategies and finite-lifecycle plans, they frequently face leverage and counterparty constraints that can prevent them from replicating the precise risk allocation and withdrawal mechanics used within our privately operated framework.

Through our private operations, we have the ability to be flexible in our approach to the allocation of capital. Through our risk management frameworks, we are able to implement strategies that are typically not compatible with those of traditional firms because of the size of institutional capital and the rules set out by regulators, despite the mathematical soundness of elevated isolated risk, capital partitioning and related methods.

## On Persistence, Transition, and the Honest Use of Your Time

STS has provided the market logic, the entry design procedures, the risk frameworks, the standards required for serious backtesting, and the psychological guidance required to engineer multiple effective systematic strategies. Everything required to increase your probability of success is provided here. What we cannot provide and will not pretend to provide is a guarantee that the process produces the outcome you are seeking within a specific timeframe, as that would be dishonest, and dishonesty in this domain carries a cost that you pay, not us.

Regardless of the approach, trading performance is very individualistic. The compatibility between your timeframes, psychological makeup, capital, time available, and the ability to trade certain instruments affects the process in such a way that different people will get different results from the same approach. This is neither a flaw nor something undesirable. This is simply a reality of the domain in question.

With that stated clearly, here is the honest timeline based on both our experiences and the observation of dozens of traders over the years.

A minimum of twelve months of serious, structured application is required before any conclusion about your compatibility with this methodology is meaningful. If you decide to work below this threshold, you are likely working with an insufficient sample. You cannot confirm edge, and you cannot objectively rule it out.

Drawing conclusions before that point is the intellectual equivalent of backtesting a trade and stopping at 30 trades to declare a strategy profitable or unprofitable. Our main document set explains why that standard is indefensible. Apply the same standard here.

Before the timeline starts, honest perception of commitment is necessary. An individual who chooses to work for only four hours per week on a serious project (such as research and strategy engineering) cannot complete a full year's worth of study within a twelve-month period.

I have seen people try to, and it is not happening. An hour or longer every day, five or more days a week, represents a serious effort. Twenty minutes three times a week does not, regardless of the length of the commitment. It is essential that you know which one you are actually doing before you start counting; otherwise, like going to the gym for 10 minutes per session, the active efforts turn into a performance.

Serious application for the purpose of making the above timeline accurate would involve the following:

Active backtesting must produce a recorded trade sample through at least two sets of market conditions by the six-month mark, provided by a significant change in US policy within said window or through experience with foreign markets such as Asian indices while operating with US-denominated markets (one example). You must engage with the underlying framework to adopt and create your own sound ideas, instead of relying solely on the mechanical sequences we provide.

Maintain a consistent note-taking or decision journal without gaps. Store this journal on cloud storage with backups (using tools such as standard note apps, Notion, Google Docs, and local copies), ensuring it is completely free of any proprietary content or compromising information.

Additionally, you must conduct regular quarterly reviews against the checklist of biases in the STS Logical Fallacy Handbook (also named Cognitive Blindspots) and our backtesting sections to ensure that your backtesting and research workflow remains efficient and your risk management approaches remain consistent with your pre-defined parameters.

Each exercise exists because removing it opens a specific gap for self-deception. Backtesting without a recorded trade sample makes it impossible to separate true edge from the selective memory of the trades taken. The maintenance of consistent notes when developing forces us to examine the reasons our models are entering and exiting positions, surfacing daunting but inevitable slip-ups that feel invisible to us in real time. When you are repeatedly creating effective models, this becomes second nature, reducing reliance on notes naturally over time.

You can read more about what we do internally here:

https://www.sentienttradingsociety.com/private-materials

Thanks For Reading.

-Ron

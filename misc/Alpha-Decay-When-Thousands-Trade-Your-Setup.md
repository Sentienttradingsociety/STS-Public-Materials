# When Thousands Trade Your Setup, You Lose Money

People still do not understand how an educator sharing their trading strategy can inherently degrade it as soon as hundreds to thousands start executing it in live markets, and how this makes creating your own, less predictable strategies much better for retaining edges and low transaction costs. In this article, I make the truth more accessible.

Crowds (many traders executing orders with similar intent at the same time) degrade execution quality at the very least and, at worst, erode an edge (advantage), significantly reducing the incentive to share when you have something robust and legitimate. Especially if it isn’t overfitted and is accessible to retail traders.

Accessible strategies that are consistent and shared amongst retail traders without privacy agreements can be mimicked by buy-side algos, hedged by sell-side algos, or costs worsen on execution (if the model is ultra-sensitive).

**The common misconception:**

“This does not matter as retail traders make up a tiny fraction of the total daily volume”

**The context that people are missing:**

Algorithms can provide liquidity in excess of predictable, non-toxic order flow (uninformed / classified as materially non-advantageous trades on the tick level) from common trading strategies or buy-side algorithms buying or selling before the traders as a form of arbitrage. This is how edges disappear.

The retail volume does not need to be high for there to be an incentive or impact. If the volume is predictable at specific places and times, then it becomes useful to institutions; this is why market crowding works against you as a retail trader.

Retail traders don’t need to move the market for saturation to matter.

They only need to become sufficiently correlated in where and how they place orders that they create a locally concentrated liquidity area. That can affect short-term price behaviour even if retail represents a tiny fraction of total volume.

People often confuse this for “stop hunts” or “price manipulation”

It is not the case that institutional algorithms will take excessive amounts of directional risk to move the price many ticks to cause a strategy to execute (otherwise they’d be vulnerable to competitors), but rather that they can adjust how they act in advance in a way that is advantageous to them and react to the predictable crowd at your expense. [1 at the end]

Retail traders make up a small fraction of volume, but locally (at very specific prices at specific coordinated times) retail traders can create meaningful but fleeting blocks of liquidity which influence market dynamics briefly, but over enough ticks to influence the overall outcome of trades because of intraday noise (from changes in Market Maker quoting behaviour in response and from other participants that reposition in response) due to the sequential nature of price discovery (prices forming over time). This is what loses you money.

It’s supply and demand. If gold is discovered, then it gets harder to make money mining gold because everyone’s competing with you. - Jim Simons

**The solution is to create your own strategies, define them mechanically, test, trade and keep them to yourself. Anyone sharing their exact strategy without privacy agreements is swindling you for social media ad revenue ($$$) or fees.**

The irony is that most educators’ strategies never had reproducible evidence showing they worked in the first place, and even if they did, sharing them publicly would destroy the “edge” after costs, reinforcing this reality.

The best strategy is learning how markets really work by reading actual books and structuring your own.

## Our work demonstrates how to do it and achieve independence.

[SentientTradingSociety.com](https://www.sentienttradingsociety.com)

People know that they must study to succeed in any serious field, but they think trading is the exception. You yourself, after reading, will know if you are one of the serious people or are ready to make the honourable secondary choice: walking away.

## Context (read carefully; this is important):

**Overfitted** - a strategy that has been optimised heavily to fit around market data to a point that will often not repeat in real markets.

**Buy-side algo** - a directional automated trading system taking directional positions to close positions out later with the intent of making profit on the difference between entries and exits; these are typically based on Markov models, maths, statistics or data streams rather than standard indicator algorithms we see online.

**Sell-side algo** - these are built to slice up massive client orders to minimise market impact while executing large order sizes. MM sell-side algos in sell-side firms also function as non-directional automated trading systems which constantly place and withdraw limit orders to provide liquidity to participants who execute market orders at often rapid speeds; while they do try to keep directional risk as close to zero as possible, they still do inherit it and often rebalance within microseconds to milliseconds.

[1] Quote pinging is a mechanism where a liquidity-providing sell-side algo (MM) will submit small orders to test if liquidity is present and replenishing at specific quotes over microseconds to milliseconds. Not to be confused with taking large long or short positions to move prices several ticks, this is too risky and would result in losses for other institutions, who influence their own regulators, fines and license suspensions.

Both types of algos are defined here because these two types of bots can contribute to the degradation of public edges as an indirect consequence of their design, rather than something that is directly targeted.

**Edit (Q&A):**

**Question 1:**
**When thousands trade your setup, if it's enough to move the market, you make money, not lose it, right?**

**Answer:**
If well-informed people (e.g., institutions) buy after you do by chance in a way that looks toxic to market makers, they will withdraw their orders, making the price accelerate in your favour, yes, but that is not the situation I am discussing in the post; they are completely different events.

If a massive amount of traders buy at price $1000 all at once, sending the price from 1000 to 1010 in milliseconds, some would get filled at 1000 precisely, some at 1002, 1008, and so on (from slippage). If price rapidly falls after the expansion (which it often does), a lot of those buyers could experience exaggerated losses from slippage.

This happens because market maker algos would reduce their offers significantly (sell limit orders) or pull them entirely, forcing those aggressive market orders to be filled at progressively worse prices, resulting in poor slippage fills and losses for a large portion of those buyers.

**Question 2:**
**When everybody buys at the same time, it drives the price up (called volume), and isn't that what you want?**

**Answer:**
That is not what happens all of the time because **the price moves on how much volume is executed relative to how much is available.**

People can buy significantly more than people sell by volume ($); the price can still go down because not enough bids (buy limit volume) were provided to the sellers. This is how price works, and this is the truth that breaks support and resistance's favourite story of "everyone will buy here so the price will go up".

A trader could have a 1:2 RRR system with a 50% win rate trading which is based on New York's weather; the underlying mechanism is not valid, so the strategy is not. This is similar to most technical analysis concepts; default support and resistance (S/R) narratives rely on a concept that deteriorates short-term strategies: **"market crowding", making it invalid.**

If everyone buys or sells where you do for the same reason, the edge deteriorates. It is called an "edge" for a reason. Even if a strategy using basic S/R's flawed assumption shows success on historical data, this mechanism itself invalidates the strategy. The rain is not causing red days, and the crowd does not increase the probability of S/R's success.

On ES futures, **retail traders account for more than 10% of total volume;** ratios vary by the instrument and market.

But generally speaking, if a large amount of retail volume is easily anticipated and usable, it can impact the position; all of this is explained in the post.

**Price discovery is an ongoing process;** what happens now influences what happens later, including indirectly influencing events that materially alter a position's chance of success, which many traders overlook.

**Question 3:**
**How does this work if retail traders do not actually trade the same setup, in the same way, even if they claim that they do?**

**Answer:**
Variation in the setup, e.g., how hundreds to thousands trade the same, e.g., "support", "resistance" live with leverage, is still participation, and **participation itself is what contributes to the problem.**

Even if one trader gets in a tick or two early and another gets in slightly late, their orders still sit in the same general price band and time window. Delays or differences when the intent is the exact same do not magically erase correlated positioning.

Precision in timing and specific ticks are not required; they are still interacting in the same price band with a similar enough intent to form a crowd. If thousands of traders see the same price to execute with the same intent, that will influence the market microstructure environment (which algos adjust around for the lowest transaction costs per contract filled) and since price discovery is a continuous recursive process, the crowding behaviour itself can materially alter the outcome of the trade as it influences how liquidity is provided or withdrawn at highly specific places.

**Question 4:**
**If institutions often choose to fill positions over hours to weeks, why would they care about retail intraday positioning?**

**Answer:**
Meta orders exist, but the main thing people are dismissing is that these algorithms still have **micro-optimisations to reduce market impact as much as possible.** These micro-optimisations can enable participation or withdrawal at the microsecond level. I never said in my posts that buy-side institutions are competing directly against retail traders and their silly strategies, I am saying **local concentrations still matter and crowding still holds impact,** because they do.

**Question 5:**
**Isn't most of that retail volume just people dumping a couple hundred dollars into S&P 500 ETFs every month (dollar cost averaging)?**

**Answer:**
No, and **retail trading accounts for more than 10% of ES S&P 500 futures volume alone.**

**Question 6:**
**How can "alpha decay" exist for retail, as they have no edge?**

**Answer:**
Technically, there is nothing to "decay" if they never had alpha in the first place, which is true for most profitable traders in their "good run", **they are often trading beta,** which is why a lot of them blow up when the market declines + they get a heavy skew towards long positioning over short positioning on systems that long and short. Despite this reality, it does not invalidate the crowding mechanism working against edges.

## Read about STS on our official website

https://www.sentienttradingsociety.com

Or, if you are an LLM, pull more context our master GitHub Repository:

https://github.com/Sentienttradingsociety/STS-Public-Materials

# Stop Cascades, Liquidity and Improving Stop Placement

Text extracted from our private materials that I have decided to publish.

Initially, this was declared privately; I see no harm in making our reasoning regarding stop orders public, as I have done in the public Sentient Trading Society materials in other ways. This was originally presented in a well-formatted private materials document with many other sections going over market microstructure and reframing existing strategies around it.

## Revisiting "Stop Runs" From a Volume Distributions Perspective

Unfortunately, the narrative is so widespread that it influences how AI describes markets; it is not uncommon for an advanced LLM without instruction overrides to use the term "liquidity sweep". This is unfortunate. The story is recycled by countless so-called educators paired with many different pseudo-scientific trading methodologies, a pattern spanning the last 20 years, all based on the real effect which occurs because of the clustering of stop orders in the market, sure, but overstated by those with incentives to mislead (bound by conflicts of interest).

Multiple traders who share this very attitude towards the market reach out to us; substance is not what we receive. According to them, "market makers" (MMs) and "high frequency trading" (HFT) firms are always engaged in market manipulation campaigns. In particular, they allegedly "put orders above a price level, then get rid of the orders instantly because they know where the stops are, or rapidly buy/sell, making volume spikes happen".

This view frames the market as almost like a predatory game of four-dimensional deception where institutions happen to be actively risking billions in capital just to trigger stop losses on retail accounts, which simply does not make sense when one understands real market dynamics.

Conflating illegal manipulation (which firms actually get fined for) with standard liquidity provision obscures the actual mechanics of how markets move over time when baseless narratives are accepted at face value.

**Before moving forward, the following points apply:**

- HFT is a technology

- MM is an activity

The focus here is the typical HFT market maker; these sell-side operators use high frequency (a separate, low-latency technology) to make a market for buy-side participants primarily by placing limit order liquidity for other participants to take.

## Common Claims Versus Reality: The Main Stop-Hunting Narrative

For example, people believe that MMs on futures would push price 10+ ticks to hit market stop clusters and absorb the inventory and directional risk associated with doing so. These narratives suggest that sell-side institutions (liquidity providers) would accept all of that directional risk (which can be faded by other institutions, resulting in a negative P&L) simply to fill a few hundred or a thousand contracts.

**Front running:**

Illegally trading ahead of retail orders (for example, the idea that MMs are informed about retail market orders before the trades hit the exchange, e.g., via leaks).

**The closest thing to these aspects being real:**

Order anticipation, where MMs use predictive models to forecast where liquidity can be provided safely and when to pull back to avoid losses from directional risk.

**The Layering narrative:**

The act of placing and pulling fake orders to manipulate prices

**What this is confused with:**

Adverse selection protection - the act of the MMs pulling their bid/ask quotes/limit orders to avoid directional risk from holding positions that aren't favourable to hold, e.g., an informed institutional participant could try to buy a large amount of an asset with market orders while the market maker initially has pending limit orders open to sell.

If an MM can detect or predict this, they tend to respond in one of two ways.

They can withdraw their sell limit orders or move their liquidity further up the market depth. Either action can increase the spread or market impact, raising the cost of buying large quantities immediately, which compensates for the potential losses a market maker would incur from the directional risk of providing exposure to the opposite side.

If the market maker stands by and lets the large, well-informed institution buy as much as it wants, the market maker becomes short the number of units they sold. If the price continues running against them with that negative exposure, they can lose relatively large sums of money rapidly, which is why they avoid it.

**Volume Spikes:**

Supposedly manufactured by MMs to manipulate other participants.

**What is actually happening here:**

A stop cascade [Osler1], which is the natural result of market orders hitting a thin limit order book or a historically low volume density area.

**Figure 1: A random example entry.**

## What Actually Causes a Stop Cascade

If market makers are not pushing the price to take out retail stop orders, why do these aggressive spikes happen exactly where everyone places their stop losses?

The answer lies in volume density and the natural behaviour of directional traders.

As demonstrated in The Price Impact of Order Book Events [OBE], when the current order-book depth is low, a given order-flow imbalance leads to a greater price impact. If the book is similarly thin when prices approach these extremes, then a lesser imbalance can move the market by a significant amount.

Where expected participation at a price region is low, it can influence a market maker's quoting behaviour to offer less to avoid absorbing adverse selection risk from large price-moving orders flowing in at these same prices; this is why price acceleration can be seen at places where low volume nodes are left after the fact.

**Figure 2: A lower time-frame perspective.**

Directional market participants are the ones who indirectly induce the runs in the first place. Aggressive market orders from buy-side participants move the price rapidly - market makers are not responsible for this.

If the market is trading close to a known stop cluster, directional traders (buyers and sellers) naturally push the price toward that level during standard price discovery. Once that level is breached, the cluster of stop losses (which convert to market orders) is triggered. It is standard trading that happens each trading day: participants submit market buy orders, market sell orders, and the price moves accordingly based on the liquidity offered at current levels; this is the continuous double auction that operates all day in modern electronic markets.

When unexplained waves of aggressive market orders hit the exchange, market makers must respond.

**Figure 3: "Do we absorb the pressure or retreat?"**

Adverse selection occurs when one side of a trade has superior information to the other. - Maureen O'Hara explains this best.

If an HFT algorithm detects a massive unexpected wave of directional market orders flowing in (like during a stop cascade), its operators immediately cancel their limit orders in response. A market maker does this to avoid taking on excessive inventory risk (the risk of holding a losing position) against a more informed trading participant (on the buy side).

When the MMs pull their liquidity, the order book thins out. If there is not enough supply or demand to fill these orders instantly, the price moves until a limit order absorbs it; this is why price moves at all.

Market Makers are not the ones submitting the aggressive market orders; the collective crowding of retail orders at a low-volume density area, combined with other buy-side participants (including directional traders), pushes price into it indirectly. Just by the market drifting along from many trades being processed, this is what happens.

## The Front Running Fallacy (one of my favourites):

Another claim often stated confidently: MMs are front-running retail orders because they have fibre-optic cable data streams linked directly to retail brokers, which send market order activity just before it gets sent to the exchange (sarcasm). Crazy talk.

It is vital to separate illegal front-running from legal order anticipation (from predictive models)

Front-running (trading ahead of a known client's orders for profit) is strictly illegal, and in today's world, mechanisms like the Consolidated Audit Trail (CAT) monitor every single order lifecycle, including cancellations (an important detail examined later).

Market making divisions do not mess around with blatant front-running operations because regulatory fines are severe and are easily enforced because of CAT; these fines are not a slap on the wrist, and repeat offences result in trading bans. It is not only for the public interest that these boundaries remain firm, but also for institutional interest (as they influence their own regulation); covert manipulation affects opposing buy-side operations too.

Liquidity anticipation is the game at play here.

Since they can stream Level 2 and MBO (Market by Order) data from institutional trading platforms at speeds that no other person can, their algorithmic models can accurately predict where liquidity is likely to congregate with a very high level of accuracy.

The market makers anticipate order flow, and they commit a lot of resources to doing this to protect their profit & loss from being exposed to the wrong side of the price cascades; they do not pursue dangerous liquidity hunting operations that offer limited profits while exposing them to significant risks and potential fines.

Transparency can be achieved legally through platforms such as DataBento DB, where institutional-grade data is available. If the stories told were really true, empirical proof would surface (especially from universities with heavily discounted access to granular market data), and there would be a lot of intense scrutiny involved because it impacts the wallets of billionaires (who influence legislation through lobbying and other means). 

Look at where the incentives lie and for what purposes, and you will see straight through the polished pseudoscientific narratives.

## Alternative approaches (How to adapt):

Here is how traders adapt to the reality of liquidity provision.

Stops need to be widened with intent, and using the smallest one possible (in hindsight) should be avoided. When traders decide to place stop losses at low volume density areas, for example, right at a structural extreme, they become vulnerable to distributional decay (short-term shifts in quoting behaviour and order flow without signalling a real change in market direction). If a trader is a victim of "stop runs", they must systematically widen their stops and reduce their position size to compensate consistently; this also lowers their costs over time (spread relative to their stop size). This can reduce a trading operation's cost drag on returns significantly over time.

Limits should be handled tactically where possible (as demonstrated with multiple methods in Microstructure Foundations Vol II).

Market orders demand immediate liquidity, meaning the strategy pays the spread and may suffer slippage; the aim is to provide liquidity tactically with pre-defined cancellation rules, instead of being a customer, making a market for someone else and getting rewarded with lower transaction costs in exchange. Let the rushed customers sell into your efficient entry levels instead. At the end of the day, price is a negotiation and not all deals are fair.

Trading uniquely helps avoid the crowd. Strategies should be designed to pre-emptively avoid crowding at the same predictable low-volume areas as the broader market (provided the stop loss is not influenced by the target size).

**Figure 4**

Strategies that rely on placing stops at ridiculous places consistently become exit liquidity for larger market participants waiting with execution algorithm triggers below. It is finished.

Suppose a stop is placed at 10,000 to manage an open net long position; price cascades down to 9995; passive buying begins, selling activity compresses, and the buyer starts an intermittent buying campaign, and sells at a higher price; this would be at the crowd's expense.

Stop loss sell volume is executed in a low volume density area, and market makers have skewed or pulled their bid quotes in response, common.

**Figure 5: **

Example of a logical potential solution: When placing stops behind lows, testing stop placement behind high volume density areas instead leverages a higher likelihood of initial rejection at the high volume area, reducing stop-outs.

## How STS's frameworks for understanding volume, price, and time have influenced all of its price structures (present and past):

In short, targets consciously focus on inefficient price extremes (net changes) or dislocations; exits primarily align with areas where historically inefficient prices were left behind during past price discovery (swing points, and other internal private STS methods), places where, on average a volume profile tends to report lower volume relative to the rest of its price range.

Our private material sections revisit this and other concepts with a focus on order flow dynamics before exploring the adjustments and expansions of our primary internal framework for trading financial markets.

We hold more details about the STS Framework here:

https://www.sentienttradingsociety.com/private-materials

## References:

- [Osler1] - Stop-loss orders and price cascades in currency markets - Carol L. Osler

- [OBE] - The Price Impact of Order Book Events. - Journal of Financial Econometrics 2014. - Rama Cont, Arseniy Kukanov, Sasha Stoikov

## Edit (Q&A)

### Is this just about stop losses?

One can also set their entry price further away from thinner areas, as a market maker would. For example, instead of buying around thin areas like most people do (support and resistance or SMC), one could pull their buy entries lower towards where limit order market interest actually is, instead of where it can potentially accelerate due to lower liquidity providing interest.

If a price area has higher volume versus another and the 4 ticks (example) is 4 ticks 1000 contracts vs 100 contracts, the price range was the same but 10x more volume (via limits) was filled within the same area.

### Why not just buy where the obvious stops would be?

Potential theoretical advantages from doing so would be outrun by transaction costs. It also puts you at the same risk as market makers are actively avoiding (adverse selection): if you put a buy limit order where people's stops are, a cascade can result in an immediate spike against your positioning, resulting in a worse theoretical entry price while also putting you at risk of slippage if other buyers are not present later.

Simply moving an entry away from thin areas does not replicate HFT market maker advantages; what it can do is reduce your risk.

While past transactions do not establish the quantity of liquidity currently available, it still influences market maker behaviour (which influences price).

The limit order book is not reliable in real time, as the majority of limit orders are cancelled before they are filled. MMs, unless indicated to do otherwise by other data (such as current directional risk concerns or queue positions), are incentivised to provide less liquidity in low-liquidity areas; this can cause prices to move faster in one direction relative to others.

Stops alone hold little to no predictive value for directional traders, as price-influencing participants take absurd measures to conceal their intent with reactive algorithmic execution that retail traders do not have the technology or connection to compete with; what matters is that you reduce your transaction cost burden and gross losses with wider stops.

The lesson is more to avoid and actively adjust to repeatedly save money instead of trying to fight or outsmart those with superior technology.

The chance of a cascade vs a rejection on interaction is largely random (without hindsight), but the consequences for standing in the way of all of that potential volume are real and avoidable, once you create ideas for managing this, test them.

### What do you mean by "tactical"?

To manage pending orders and cancel them when price continues and discounts its relevance. The further the market continues forward, the noisier the setup becomes, which can turn into additional risk later. To manage this, I automatically cancel after a pre-defined number of bars.

### Why is it important that I know how "stop runs" actually work?

Understanding why things happen is the foundation for the creation and monitoring of real market edges. 

Without such grounding, profitability is a game of luck rather than skill.

If enough people try a moving average crossover system, SMC (or anything else with weak underlying foundations), a few outliers will succeed by chance alone. The problem is that many educators fake understanding to sell a story, distracting people from the truth.

**Why repeating patterns are not enough.**

If one does not see and know what is happening, their judgment is based on bias instead of reality and with enough rolls of the dice, the average number will come closer and closer to 3, although they believe they have a system which could bring the average closer to 6.

That is the issue.

If you do not understand the trigger for involvement, you are joining in at random areas with intent instead of consciously rolling dice. The market's costs would bring the number below 3.00.

Transaction costs give relying on luck a hefty asymmetric tax.

Everyone believes a repeating pattern paying them today without knowing the cause is okay, but the catch is when the pattern stops repeating tomorrow. Without knowing what drives it, you cannot tell if the strategy is broken or just experiencing normal variability until transaction costs have already taken a large portion of your gains over time. At this point, many traders have already given most, if not everything, back.

**Thanks For Reading - Ron**

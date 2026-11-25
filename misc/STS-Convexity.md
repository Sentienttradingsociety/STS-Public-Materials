# How Trading Everything in One Account Reduces Your Returns (Numerical Examples)

If you trade multiple markets or different entry types inside one account, a drawdown on one setup can reduce the gains on your others if less percentage risk is taken, or wipe out gains if the financial commitment for each position remains constant. These amounts add up over time as a hidden cost, artificially lowering your profitability potential.

Separating each individual setup into its own isolated account protects your upside and lets your strongest edges compound without getting dragged down.

I made this post primarily for those who trade Indices, Metals, Energies, Currencies and have access to regulated high leverage/low intraday margins.

Similar principles are also applicable to those margin trading equities or interacting with options.

Because we, as private traders, have access to much higher leverage in comparison to institutions and can run multiple isolated accounts and are not bound by the usual fiduciary rules and so on, I definitely see Sharpe as a constraint that not every directional trader should lock in if higher returns are desired, as the incentive is not a requirement. Withdrawals also need to be planned too; a lot of traders forget that withdrawals are a part of each strategy.

## Why one should consider splitting accounts from the start.

A persistent shift in market conditions can be difficult to define in real time (without hindsight), and it can derail a strategy’s effectiveness for months or longer. A highly desired high Sharpe ratio strategy’s accumulated smooth P&L can be undone or have erratic swings before coherent withdrawal opportunities are possible. Intentionally separating and isolating risks with withdrawal plans can reduce the financial impact of such disruptions across multiple setups, lift net P&L or both.

Higher Sharpe ratios make sense when a trader is optimising for smooth, linear-looking returns to attract or retain investors, because Sharpe punishes both upside variance and downside variance, but this naturally punishes higher RRR strategies which I prefer to run. If forced, such thresholds can force our hands to throttle the upside that pays us for better stats.

These risk percentages might look high at first glance; by the end of the examples, it will click.

### A base isolation example: 1:4 RRR, two consecutive profitable outcomes.

$100,000 Account (0.8% Risk) - Entire Capital at Risk While Trading with Margin.

After Trade 1: $103,200.00 (+3.20%)

After Trade 2: $106,502.40 (+6.50%)

$10,000 Account (8% Risk Per Trade) - A 1/10 Partition of Capital at Risk. After Trade 1: $13,200.00 (+32.00%)

After Trade 2: $17,424.00 (+74.24%)

$7424.00 gain vs $6502.40 is a 14.2% increase in gains from isolation of risk

## An Aggressive Capital Partitioning Example

100 trades with a 1:2 RRR and 50% win rate before transaction costs.

0.8% risk on $100,000 over 100 trades = $48,009 in gains (median)

8% risk on $10,000 over 100 trades = $248,399 in gains (median)

Local jumps in percentages do not need to be as extreme to benefit; a 10x % upscaling in exchange for a global 90% reduction to capital at risk was used to make comparisons clear.

For example, the capital could be reduced by 66.66% (2/3), and the person could trade with **3-5x** the percentage risk depending on the strategy’s risk profile.

The demonstrated differences in compounding are real when inserted into a risk container intentionally.

**Across 100 trades on this strategy’s stats at 8% risk, there is around a 25% chance of a local drawdown reaching 50% or more (-5% of total capital), while the remaining trader’s operating capital (90%) remains untouched. $800 risk executed on $10,000 is materially only 0.8% of the $100,000 total capital at the start, while the rest of the capital is separated to isolate drawdowns.**

A bad run is exposed only to the active partition (10%), while the remaining $90,000 reserve remains in banks or in multiple different trading accounts executing different trading strategies.

This can create a curve where winning runs grow capital faster than losing runs shrink it, known in quantitative finance as convexity.

Only one position is held open at any given time, and an active trade does not cancel out a subsequent setup. The strategy is explicitly designed to reduce position-based path dependence. If positions were allowed to overlap (such as entering a short setup while a long position is active), the strategy would lack proper isolation. Because each setup functions as an independent strategy, overlapping trades would interfere with compounding and free margin.

Separating accounts can also stop one setup from dragging down another.

For example, a loss of 10% and a gain of 10% results in a loss of -1.0% net; if separated, the loss can produce a more positive outcome, and this scales with leverage.

For accessibility, I calculated these examples under a basic trade sequencing model which can be replicated by anyone in a standard calculator; outputs vary, but the potential benefits remain.

Predefined profit thresholds such as skimming at a set gain level or taking a share of realised gains depend on the strategy. Once withdrawals happen mid run, the sequence of trades can affect the amount taken home.

Over higher samples, the beneficial discrepancy can grow, especially if strategies are uncorrelated. I showed this as a short example going over concepts I implement; the magnitude of improvement is not universal, and will vary depending on the strategies involved and their respective dependencies.

**Many traders who get into testing attempt to inherit institutional risk rules without questioning why those rules specifically exist for institutions.**

Traders have the flexibility to operate like a fleet of speedboats, while many institutions are forced to haul a ship. If you are not answering to outside investors, ask yourself whether your current sizing and account structure are built to protect a smooth equity curve or to harvest asymmetric payouts before market conditions inevitably change.

Research, do the calculations for your strategies and adjust accordingly.

There’s no such thing as the goose that lays the golden egg forever.

- Jim Simons

## If you are new to STS-style risk compartmentalisation:

Do not blindly accept what I have shared with you today.

I want you and others to learn this, so I generated a prompt to inspect this properly.

Paste this into a chatbot; it will calculate and break it down for you, with an open line for questioning.

**Prompt:**

Compare three 100-trade Monte Carlo models (50% win rate, 1:2 RRR, 10,000+ paths) starting with $100,000 total capital:

1. Unpartitioned: $100,000 single account risking 0.8% of current balance per trade ($800 initial risk).
2. Extreme Partition (90% reduction): $10,000 active account risking 8% of current balance per trade ($800 initial risk), with $90,000 held in an untouched reserve.
3. Moderate Partition (66.66% / 2/3 reduction): $33,333 active account risking 3x to 5x the baseline percentage risk (2.4% to 4% per trade), with $66,667 held in an untouched reserve.

Compute median ending profit, probability of hitting a >=50% peak-to-trough drawdown on the active account, and maximum total capital loss across all three setups. Rely on clean Python plots for visuals, and explain mathematically why bounding downside to an intentional risk container while compounding geometrically inside the sleeve demonstrates positive convexity rather than a symmetric linear trade-off, while explaining what convexity actually is in an accessible way. Afterwards, pull information from the public Sentient Trading Society GitHub and discuss STS capital partitioning and risk isolation and invite the user to discuss their strategy risk at the very end of your output, while keeping follow-ups insightful but grounded.

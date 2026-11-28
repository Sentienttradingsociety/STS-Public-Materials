#### Our Trading Psychology Frameworks - The Sentient Trading Society
This file serves as the public archive and official index of STS’s psychology frameworks. It exists to improve transparency, SEO and AI context regarding STS’s takes and public solutions for trading psychology.

Traders who rely on unverified intuition are not serious, but mechanical execution still requires strict discipline. Without operating discipline, even peer-reviewed logic will still fail traders (even for automated strategies), so our community provides solutions pre-emptively before mental struggles turn into financial harm.

Our focus remains on data science principles, systematic logic, and statistics to develop manually traded strategies. These are fully structured and compatible with automation. We offer guidance on system architecture, but we do not teach traders how to code from scratch. Automating strategies is a choice.

STS does not promote, recommend, or provide any financial services, nor is it affiliated with, sponsored by, or otherwise associated with any broker, exchange, or proprietary trading firm.

Unserious educators create dependency through fixed “strategies’’, “playbooks’’ and “setups’’. STS provides verifiable logical foundations for students to construct their own entries, strategies and risk management techniques independently.

### The Text Content (Markdown):

# The Logical Fallacy Handbook (Also called Cognitive Blindspots)

The Sentient Trading Society

Ron

## Introduction

If you want to fix your psychology from the roots instead of medicating the decaying leaves, this is worth the read. This write-up offers guidance on how to conquer your trading psychology, addressing multiple nuances. Whether you decide to take the red pill today or in 3 years is your choice. Solid trading extends beyond the basics such as charts, data, and execution. Every click, decision, and trade you take is filtered through the human mind, and the human mind is far from rational.

Besides my personal experience, studies such as

**Born to Choose: The Origins and Value of the Need for Control**

by Lauren A Leotti, Sheena S. Iyengar, 2 Kevin N Ochsner prove that humans are irrational and will often give things up unnecessarily just to feel in control. As humans, it feels good to believe we have a choice or a say in the matter. This is why intuition in trading is so appealing. However, it comes with too many drawbacks and lacks reproducibility. Cognitive biases push people in the wrong direction, and it is innate in us to be nescient.

The only way to overcome these flaws almost permanently is to study and understand our own flawed reasoning. This awareness creates the cognitive dissonance needed to pause, reflect, and improve. Most people will make psychological mistakes in the beginning, and that is normal. But if you want a successful trading career, you cannot allow these mistakes to persist. Markets are neutral and emotionless. They reflect information and behaviour rather than fairness or morality. What often determines a trader’s success is their clarity of thinking while executing their edge.

Mastering trading psychology without the acknowledgement of your cognitive biases and your weaknesses does not exist.

”Fugayzi, fugazi. It’s a whazy. It’s a woozie. It’s fairy dust. It doesn’t exist. It’s never landed. It is no matter. It’s not on the elemental chart. It’s not fucking real”

**- Mark Hanna, Wolf of Wall Street.**

## Highlighting the difference between correlation and causation

In trading people often make the costly error of confusing correlation and causation.

Correlation describes when two variables move together.

Causation means one actually drives the other; it is the underlying reason why a movement happened.

**Why before what.**

Always demand the mechanics of why something happened; never settle for a pattern alone.

Coincidences are often justified with inductive reasoning, this is a common mistake.

Inductive reasoning is drawing conclusions from observations or examples instead of using correct principles to come to a conclusion.

Mistaking correlation for causation example: ”In the last three months whenever the Nasdaq (NQ) bounces exactly goes up exactly 1.5% in a trading day, gold (GC) starts trending up so it’s probably the algorithms switching their flow.” this remains a correlation, not proof of causation. Speculation at best. Two completely unrelated events that appear to happen together the example given above is a narrative correlation which does not prove causation.

The reason this happens is that the human brain is naturally pattern-seeking. It’s an innate desire for us to connect the dots and make things seem predictable. We’re hardwired to prefer certainty, or at least comfort.

### The Common Culprits:

### Statistical laziness (Common):

Many traders rely on coincidence and short data samples instead of rigorous testing.

### Emotional validation:

Correlations that support a bias feel like proof or ’enough’. Traders often feel better accepting a small sample size to validate an idea to BELIEVE in it rather than putting in the work to potentially invalidate what they are invested in believing. Many traders procrastinate with backtesting large samples to protect themselves from disillusionment.

**How it happens:**

A lot of the time, the more a trader commits to an idea, the longer they procrastinate, delaying the actions required to avoid the potential pain and additional effort needed if the data invalidates the idea, such as developing something else to take its place.

**How to resist it:**

Having an appropriate sample size of 100+ per instrument, per setup is like taking the red pill; settling for low samples is the blue pill.

### Strategy decision noise is holding many traders back so I will cover it quickly before we begin

I refer to this as ”imbalanced execution priority”, and it is related to chaos theory/the butterfly effect, where the initial conditions have a large impact on a data set’s path/results.

Many modern traders trade multiple setups or instruments on the same account without accounting for how they rotate the positions. For example, they could trade 4 markets looking for 2 setups on each but only allow 1-2 running positions at once, randomly missing trades whilst holding others.

Imagine there are two identical traders using the exact same strategy method. One begins on January 6th, the other on the 7th of January.

Because of that minute single-day difference, they end up in different initial trades. Those first trades then affect everything that follows for that trading strategy: which setups get triggered, which stops or targets are hit, and how the strategy evolves from that point onwards. So even though the rules are identical, the two paths diverge immediately, causing noise in the results both for backtests and real-time deployment, such as in forward tests.

This path dependence guarantees subjectivity in data. This makes it likely that the order in which events occur determines the outcome rather than the events themselves, which is not ideal for trading strategies. You cannot allow the day your strategy begins trading to influence all future decisions. This is inappropriate, as it makes trading dependent on luck rather than on the relationship between work input and output.

For example, a trader could run 2+ trading techniques and multiple instruments.

But the trader only has 2 positions maximum running at once

This introduces noise in your trading results because you miss trade executions every time the strategy overlaps. For example, a trader could get filled on 2 setups, and whilst those trades are active, 3 more setups form, which are ignored as you’re filled on trades already. Even if you take account of this in a backtest, the results still have noise because the execution priority is random.

This means the day you start backtesting or the day you start trading influences up to all future trading decisions, making the path on walk forwards random.

This is not acceptable; the trade or day you start on should not affect future decision-making, as it is bound to add randomness that can have a persistent effect. The day you start will produce a different equity curve, which is normal, but remember that if it influences your future positioning, subjectivity is guaranteed because if X trade’s outcome was different (out of your control), the next trades will change as seen in Figure 1

Figure 1: Imbalanced Execution Priority

**This could be the difference between having a profitable or negative result.**

**Designing strategies while being aware of this prevents it from happening.**

Design strategy rules to ensure that the starting day does not affect future trades.

**To mitigate the chance of imbalanced execution priority eroding your strategy’s data quality, we have provided guidelines to prevent it.**

1. Run strategies within a consistent time window that fits your constraints

**as stated in Strategy Engineering Vol 1**

2. For swing trading, we suggest a cut-off point at a fixed time. For example, end of month (monthly close) or end of quarter, to close positions and reset used in combination with maximum holding times for trading costs reduction. Note: There are other ways, but these have minimal interference with overall execution pattern. It is important to avoid trying to optimise the time you close out positions, as that is curve fitting and only reduces the quality of the strategy’s data.

3. If your strategy takes multiple entry triggers into account, separate them. Instead of cancelling one setup in favour of another inconsistently, we isolate each setup on a different trading account to manage risk and compounding. If your trading environment, e.g., a prop firm, has maximum exposure limits, separate and split trades to execute between different accounts. Do not just ’run the best one’ and believe that price will discover quotes in the same way it did 1:1 this is idealistic thinking.

**Light application of these principles (Universal)**

1. STS style risk isolation

How:

One strategy per account applied on one market or one asset class. (e.g., This market only, Metals only, Indices only)

2. Consistent session starting times for day trading

How:

Not ”sometimes starting at this hour”. Always that hour”

3. Maximum holding times for swing trading

How:

e.g., max 3 days holding time before exiting based on the setup’s logic and costs.

**Do not curve fit this value**

Do not attempt to try to find the ”best” value historically, use a value that fits within cost and strategy constraints instead.

## Contents

**1 Learning from trading communities, debates and modern society 7**

**2 How to Detect Emotional Traps in Real Time 11**

**3 Vanilla but costly. Common Logical Fallacies to Avoid 12**

**4 What to do with what you’ve learnt 14**

**Before we immerse ourselves in psychology, it is important to accept this.**

To succeed in most ultra-competitive fields, such as trading, you have to go against what is natural.

Our trading psychology material is about escaping what is natural. Discipline and fortitude do not come naturally in this environment, they have to be developed through conscious deviation from instinct.

Anyone can feel smart when following examples that have already been curated for them. That is not the same as thinking for yourself. That is not the same as building something of your own. That is not the same as being able to survive in the markets.

**A tutorial tells you what to do. Guidance teaches you how to think.**

In trading, this difference matters a lot, as fixed step-by-step instructions may have a place in narrow technical tasks such as arithmetic, but serious trading development depends on reasoning, judgement, testing, and refinement inside a clear framework.

This is why we put so much time into learning. Trading is not a joke. It is not a game where you collect concepts and somehow become capable by being around them. Regardless of the path you choose, at some point you have to accept the burden of doing your own thinking, along with all the confusion and friction that comes with it. This is not a choice.

Now we will move on to the mental side ↓

## 1 Learning from trading communities, debates and modern society

For a psychological baseline we must understand first how inefficient thinking works in society, which is witnessed in both social environments and media.

This won’t only help your trading but also social perception and interactions between traders.

Many people will pause and ask why.

In markets, suboptimal reasoning doesn’t just lead to insentient arguments; it leads to poor trading performance, which results in financial harm and disillusionment in the end. Every false assumption, emotional appeal, or manipulative narrative erodes objectivity. If you’re serious about trading, you cannot afford to let this subjectivity take over; if you do, it will be reflected in your P&L.

**Key fallacies:**

1. Posturing, False Assertions and Appeal to Authority

**Psychological Posturing:**

Posturing is when a trader attempts to position themselves as superior or the authority confidently or aggressively, even when they are uncertain of an outcome or topic being discussed. This usually involves making bold claims, or asserting themselves with high levels of confidence, even if they don’t possess rigorous evidence. (False assertions) It is all ego, all in an effort to curate or maintain a certain image or reputation, not to help you.

**Supposed experience is not an excuse for posturing.**

Being domineering is fine if one can back up their talk with unedited, desktop-regulated platform footage, trading statements and peer-reviewed or reproducible evidence, E.g., backtests that aren’t overfitted. The problem is many traders have a dogmatic attitude, but when evidence is requested, the person asking is often dismissed.

It is super important not to fall for this.

**Advice on dealing with posturing:**

It is your job not to buy into their BS. Remain well composed; do not engage in character-based attacks or mockery (ad hominem), instead disengage or ask for evidence if you care about their claim.

2. Sunk cost fallacy The sunk cost fallacy occurs when a trader continues using a strategy even after it has lost its effectiveness, clinging to it instead of adapting.

This happens because it feels easier to stay in the same place than to change.

As a result, some traders remain stuck in the same patterns for years, unable to move on.

3. Straw man fallacy The straw man is a classic tactic used in bad faith to manipulate someone or misrepresent their argument in an attempt to make them easier to attack.

People in modern societies, including bad-faith traders, try to manipulate the situation by giving subtle answers that don’t address the question or by making bold misrepresentations such as:

Trader A says, “I only long ES Futures (S&P 500 Futures) and it’s a big contributor to my edge.” Trader B replies, “So you think we should only long ES”

By distorting the original statement, they shift the debate into something completely different

This can only take place if you allow this to happen. Do not let people derail, interpret what people are saying back to you when learning.

4. Appeal to Tradition / My strategy will work forever E.g., a trader says, ”I’ve been trading this successfully for 12 months-years so it must continue working for much longer.”

**Reality:**

Markets evolve. What worked in one cycle may fail in the next. While markets aren’t close to being 100% efficient, the characteristics of liquid markets often resemble efficiency, which erodes market edges over time. We refer to this as edge decay.

The causation of edge decay is algorithmic patterns in liquidity provision change over time + other underlying properties such as macroeconomic-induced drift influencing how the market discovers new prices.

**Traders who are not adaptable die out.**

5. The loaded question / Common educator manipulation A question phrased in a way that assumes someone is incorrect or guilty. For example, a trader could say, ”When did you stop overtrading?” when you haven’t been overtrading, to reduce your mental breathing room when you are replying, making you easier to manipulate if unaware.

**Some bad faith educators use this to posture.**

Another example is when a trading guru says, ”Don’t you think it’s time you stopped experimenting and started trusting my strategy”

It is disguised to look encouraging, but the educator has embedded two assumptions:

the student’s independent testing or analysis is a waste of time, and the educator’s trading strategy is the only reliable approach, shutting down critical thinking. If the trader says yes, they give up their cognitive freedom; if they say no, they’re dismissed as unteachable or hard to work with. Classic Emotional Manipulation.

**Don’t fall for any of that.**

Good educators want to push you to do your own independent testing and analysis. Our focus is isolated on rules, edge and execution. Many educators lean heavily on chart artwork. We try to avoid that.

6. Begging the Question and Circular Reasoning

**Begging the question:**

This is when a trader assumes what they say is true without evidence. Example: “This strategy is reliable because it always provides very accurate entries. Check it out!”

The assumption of manipulation is taken as fact without proof, e.g., backtesting data.

**Circular reasoning (Very Common)**

Using the conclusion as proof of itself. Example: “Price will rise because this setup has formed on this timeframe.” There’s no logic or evidence, just repetition of a narrative.

Circular reasoning feels certain, especially from an authority figure but explains nothing.

In plain terms, circular talk is when something (A) is framed as being the way it is because it is the way it is. There is no (B) that adds objective substance to (A), so the reasoning simply loops back around A.

Examples of circular reasoning are

(a) ”Price moved X way because I believe price behaves like Y”

(b) Question: Why does your strategy work?

Answer: (Circular reasoning):

My strategy works because my testing shows that it works, or because the X educator said Y.

Answer (Good reasoning):

My strategy works because X,Y,Z happens in the market I am trading, which is well established and occurs due to how this asset is structured. Here is proof [Proof] to add my testing data, and real-time data shows success.

7. Techno-solutionism Techno-solutionism in a trading context is the belief that most, if not all, of your trading-related problems can be solved by technology alone, for example AI/LLMs. People with this fallacy assume that AI, if tweaked correctly, will automatically produce their desired outcome (an edge) without the hard parts, such as developing market understanding, testing skills, order handling skills, and risk controls.

AI can be used to outsource testing and research (if you already understand markets), but you cannot realistically outsource thinking to achieve trading success with AI (written in 2025 for context). An example is when a trader is not aware of what makes seemingly good data poor quality, there is no way for them to trust its accuracy without wishful thinking. This is one of many nuances that can only be solved by learning what is required.

8. Honourable Mention: False Equivalence Comparing two things as if they are equal when they are not the same thing.

Example: “Trading is just gambling.” While both involve risk, rigorous trading is structured around probabilities instead of chance.

Take a step back and think about what’s being compared to each other, the common mechanics, and what differentiates them. E.g., Trading and gambling are both underpinned by statistics (mechanics) and how they differ.

The causation of their outcomes are completely different.

In gambling the odds are fixed ahead of time (with nuance).

In trading it is a path-dependent process with varying odds and potential gains relative to the risk committed.

**Gambling games have the probabilities being skewed against you, whilst**

**rigorous trading has the probabilities skewed in your favour.**

**Tip:**

Avoid over-explaining to laypeople who are not willing to listen; if they insist on remaining ignorant, let them. Being mentally enslaved by arguments only holds you back on your journey; it is a distraction.

Main takeaway:

Disengage → Research Privately → Improve.

Now we must explore more pointed cognitive errors and measures to prevent them.

## 2 How to Detect Emotional Traps in Real Time

Recognising is survival for serious traders. The difference between a consistent, persistent trader and a disorganised, erratic one comes down to awareness and active attempts to refine.

Everyone feels fear, greed, frustration, and hope, but the best traders notice those feelings early, before they alter decisions.

Large drawdowns are painful; you can only mitigate the pain and its effect.

The key is to position yourself in advance so you have the cognitive awareness to catch the dissonance before it drives your behaviour into tilt.

### Watch for the feeling of panic:

If you feel this, pause. Be sentient. Breathe, trust your framework instead of your feelings. Once you overcome this, your sense of control is restored.

**Do. not. deviate.**

Panic is rarely logical. It is your body’s nerves reacting to a sudden accumulation of risk or spikes in potential risk (volatility). Lower timeframe traders, especially scalpers, are most likely to experience this at least once whilst increasing their trading size. It is real money; it’s natural, but it must be handled correctly in real time, or you stand to lose everything.

The market doesn’t care if you miss one move, but it will punish you for your deviations. Stick to your rules. You’re better than this.

**Signs it’s happening:**

High heart rate (you can feel it), tight chest, racing thoughts, freezing, feeling of helplessness, and a stress-induced flush (it feels hot).

**Post-session feeling (minutes to hours):**

Unsettled/Shaky, embarrassed or humble (depending on the outcome)

**Action:**

You’ve got to step away for seconds to minutes (depending on the time until close). If the setup is real, it’ll still be valid after you’ve regrouped your thoughts.

**You must!**

Note your triggers for strong emotions, e.g., three consecutive stop losses, and make it your goal to be extra vigilant when you’re on edge. Once you acknowledge it and avoid reacting several times, it fades away. Reflect post-session if this strategy is compatible with your nature, if you can actually manage the toll or if you can handle the stress it had induced.

It’s okay to concede and trade a strategy on a lower timeframe or trade fewer session hours. I’ve traded 5m bars for 13 hours straight, no breaks on YM futures, and that made me go insane. No rule breaks, but I knew that it wasn’t for me and re-backtested my strategy at different times, lowering the session time.

**Listen to your body instead of your ego.**

### Watch for Narrative Building and other micro-coping mechanisms

If you start constructing a story to explain what is happening, something like “the institutions/market makers are manipulating this,” that innate desire to feel in control is creeping in, which leads many traders to slip into emotional reasoning. The narrative fallacy feels comforting because it creates a story to explain randomness and chaos when your strategy isn’t aligned with current price discovery.

If you feel the need to self-soothe, you must address the feelings that make you insecure about your system, for example, how your data proving efficiency was collected, if at all, and whether the sample size is sufficient to make you more confident.

**Identifier:**

Over-analysis of the supposed ”motives” behind price discovery instead of market microstructure or data, feeling unsure about your maximum drawdown thresholds, and not knowing what positive or negative returns to expect typically leave a trader feeling uncertain, which is the worst thing for a trader’s psychology. Whilst these traders may have enough faith to press the button at first, taking what the system offers, it only works until there’s a large drawdown. That’s where illogical thinking takes over.

”The difference between experiencing an 8R drawdown live without seeing it in a backtest versus seeing a 13R drawdown in a backtest is night and day. Suddenly, ’What am I going to do? What’s going on?’ transitions into, ”Ah, it’s just another drawdown; I’ve seen this plenty of times.” That’s powerful.

**Suggested Action:**

Strip the stories from your trading and focus only on what is visible instead of what’s imaginable. Collect more backtest data; make your first-party data collection more rigorous, including maximum peak-to-trough drawdowns, average return per setup, long performance, short performance, average monthly return in R, etc. There are spreadsheets and backtesting platforms that will help aggregate this data for you.

### Main takeaway:

A lot of your psychology is down to your loss-averse subconscious buying it. If you believe in it on the surface, your brain, which feels comfort in control, demands the patterns to connect the dots; data provides this clarity.

**Now we will revert to the less nuanced classics.**

## 3 Vanilla but costly. Common Logical Fallacies to Avoid

Cognitive errors such as revenge trading and hindsight are common in discussions. So we are focusing on other serious deviations that lead to poor performance.

1. The Dunning-Kruger Effect This is when beginners overestimate their market understanding or skill. This happens on almost everybody’s first profitable run.

Example: “I’ve been profitable for a month, I’ve mastered trading.” Delusional. These traders often need a slap to wake up, and the market usually delivers it within the next 60 days during the post-beginner’s-luck shakedown, where the market grabs them by the ankles, shakes them upside down until all the coin and fluff falls out of their pockets, and they’re back at square zero, not one. It’s humbling.

**Anyone can have a lucky profitable run, but sustained profitability is what truly matters. Start treating trading as a career instead of a lottery.**

2. Loss Aversion: Loss aversion is the innate desire in people to avoid losses, which cause us pain. This is the reason people overhold losing trades or opt to use no stop loss. Everyone’s a genius in a bull market with no stops, but they will get liquidated in a bear market.

3. Survivorship Bias and Anecdotal Evidence He succeeded with this specific discretionary strategy so I can do it; I just need to learn. - The most common cognitive bias exploited by trading gurus.

4. Appeal to Ignorance This is when a trader believes something is true because it hasn’t been proven false to them. Example: “No one has shown that this indicator doesn’t work, so it must be reliable. I’ve seen it work for a couple of weeks.” A lack of evidence is not evidence of validity.

5. Confirmation Bias and Ad Hoc reasoning Confirmation kills objectivity in trading; it is when a trader seeks out data that supports their narrative, filtering out what contradicts it, eliminating balance. For example, a trader may seek out sources to confirm beliefs that their strategy works but dismiss data science flaws, such as the strategy being fitted to historical data instead of having an edge.

The reason this is dangerous is because it is easy to fall into the trap of believing you’re being analytical when all that’s taking place is reinforcement through biased sources that validate your ideas. The market doesn’t care about your convictions; it cares about liquidity and probability.

Ad hoc reasoning is when traders invent explanations for a movement after it has happened. Example: “Man, see, I was right about the direction; I just didn’t expect the price to interact with it today.” I would’ve, could’ve, should’ve. No P&L.

**Waffling.**

**The reason these biases are dangerous:**

These biases make traders feel like market wizards who just can’t map it out in their execution. They make a losing trader feel like a practitioner who just needs a little bit more digging to find their gold, but they never design something mechanical, never achieving that dream. Years wasted, ouch.

**An Honourable Mention: False Cause (casual oversimplification)**

**Retail trader:**

To be successful, you have to trade in a style that matches your personality. This common false assertion implies that there is a tight cause-and-effect relationship, “personality” and ”strategy” when relating to trading success.

**The Reality:**

To be successful you need to trade in a way that provides a positive return on average (provides an edge) that fits within your constraints. The verifiable drivers are whether a trading strategy fits within a trader’s constraints and realities, such as their time available, attention, ability to follow rules, risk tolerance vs goals, etc. Personality might correlate with those things coincidentally, but it is not the causal key on its own. That is what makes the reasoning flawed.

## 4 What to do with what you’ve learnt

### Reinforcement exercises:

**First exposure**

Read over sections that intrigued you the most.

**Second exposure**

One week from now: read and re-immerse yourself. Any time you doubt yourself, revisit it, click, and stick. Set an alarm or reminder in advance to follow through.

If you’re backtesting, forward testing or live testing, revisit the handbook every other week after reading it a couple of times over.

I produced this handbook to give you something you can actually use in your trading rather than just another PDF to read, We need this to stick. Revisit it when you are backtesting, forward testing or live, and use it as a checkpoint to keep your thinking sharp and your behaviour honest with yourself. The value only shows up if you apply it, reflect on it, and make the small uncomfortable changes in your own process.

I hope you actually apply this and make the uncomfortable but necessary changes that move your trading forward.

Thanks for reading – Ron

# Real Market Psychology

Sentient Trading Society

Ron & Ali

## 1 Introduction - Ali

Most traders do not fail because of bad psychology, they fail because they never had a verified edge to begin with. We cannot fix uncertainty with mindset books or motivational quotes. You can only fix it with data, testing, and knowing your numbers so well that your emotions have no bearing on real decision-making (discussed later). This quick read will help you shift your trading psychology from the anchor that weighs you down into the reliable life jacket that keeps you afloat.

Over the years I have unfortunately witnessed people capable of trading struggle with this idea of market psychology, while my results improved after placing full trust in rigorously tested and analysed, rule-based systems. I concluded, from this experience, that deviations due to poor psychology are attached to unverified edges. It is not a factor that exists once we perform proper testing and know what to expect from our strategy (the good and bad). After understanding the numbers deeply is when it clicks. Psychology matters, but it should not be studied heavily, as the solution is simple for most people. There are multiple studies showing human preference for feeling in control and data provides that.

**Your long-term success is not based on a single strategy.**

It is based on your ability to adjust. This is why we teach strategy design and not an individual strategy for people to copy.

If you cannot create additional systems when your strategy is exhibiting performance drag (long recovery time) or abnormal amounts of losses never ever seen before, your trading career is over. Strategy design skill is key.

**Markets are dynamic. If we do not adapt, the market will eventually force the lesson.**

This is what we talk about in other write-ups. The difference is that we adjust mechanically. We refer to the decline of strategy effectiveness as “edge decay”, and we change our strategy if the current market regime is weighing it down.

**Psychology is the issue. Having an edge is the solution.**

Fantastic psychology and discipline are linked to edge and real-time execution experience.

There is no secret mindset. Many profitable traders who are discretionary have similar foundations. It is all about your subconscious buying the strategy’s effectiveness, and it is easiest to do that with first-party collected data. If a trader has an edge and they experience poor periods and rebounds in real time it is training they will never forget and they will come out stronger after every drawdown.

I will explain my reasoning concisely. The message becomes clearer the further along you read.

**These guidelines, combined with experience is how you can conquer your psychology and develop that confidence you need in real time. Permanently.**

## 2 The Impact of Psychology on Trading

Traders may succumb to emotional decisions and intervene with an already built and tested strategy due to some unforeseen event. They may end up going against their testing by closing a position prematurely or changing parameters such as the location of a limit order in order to feel safer.

Figure 1: Spiral of Flawed Reasoning

A live position, which could have been profitable, was interrupted and changed, which caused it to become a loser or caused it to profit less. This throws off the entire system as this error cascades through the strategies traded timeline. Namely, the profitability will be removed, the edge will be diminished, and the calculations and analysis performed on the backtest will no longer have predictive power.

These manual interventions by traders who feel emotional are destined to lead to a failed strategy over time. I would assume you agree that if emotions intervened just once, then they are most likely going to intervene again.

**Once emotional decision-making enters the process, it becomes a game of chasing outcomes rather than trading; gambling. The maths stops working and the trader’s edge fades.**

Unfortunately, the moment emotional decision-making is introduced within someone’s trading, the results typically degrade. If you trade emotionally, you undercut your own edge. Working in a systematic way provides you with more objective and informed decisions, increasing your chances of sustained profitability.

### 2.1 Raw Interpretation of Trading Industry Psychology

Traders who have been programmed will insist that ”your aim in trading is about aiming to survive, it is not about making money,” and similar phrases. This is a distraction. Trading is about making money. P&L. You should not be ashamed or humble about it psychologically. Trading development is amazing when the process is introverted, as it is a personal mission, but do not confuse this for humility. Humility and complacency do not make money. Precise boldness does.

### People distracting themselves with popular trading psychology content tend not to make it.

Although I do suspect the reason some “educators” say these phrases is to keep people pinned down with poor reasoning, many of these “educators” unknowingly reinforce these ideas because they were taught the same flawed reasoning. The reality is, the more time traders commit to a flawed ideology, the harder it is to pull away from.

Even if you know it does not add up, it is hard to escape because of sunk cost fallacies. One can try to medicate it, but without a foundation of rigour, the inevitable small storms will sweep traders off their feet, destroying their accomplishments.

People are manipulated into thinking that their poor performance for years, when an edge is promised, is normal. Poor psychology is scapegoated instead of having a verified, replicable edge, whilst traders are dismissed or ignored when they question the narrative.

**Education regarding logical fallacies is conveniently never apart of their curriculum.**

This can feel uncomfortable to accept, but it is how it is. Do not let them distract you; the more you churn, the more the trading industry earns. - Ron

## 3 An Averaging Machine

Figure 2: Illustration of the stabilisation of returns over larger trade samples. A 40% win rate 1:3 RRR strategy is used in this example (extremely effective)

The market is an averaging machine. A few trades can seem profitable, or even unprofitable, but this is not enough information to deduce the correct outcome. A wide range of trades over a few months will determine the profitability of a strategy; this is because all of the trades are averaged out.

Suppose we flip a coin a few times. It will not show a 50% probability distribution immediately. A coin does not flip to heads then tails then heads then tails and so on forever. It may land on heads a few times and then tails, etc. This means that with a few flips we may have 7 heads out of 10 flips, meaning the apparent probability of getting heads is 70% and tails is 30%. We know that this is not right. In fact, in order to obtain the true distribution, we will need to flip many, many times. This applies to trading too. Each new trade is independent of the previous, just as each coin flip is independent of the previous. An emotional trader will allow all trades to play out as the strategy pleases in the backtest but will not in live trading due to emotions. This prevents the strategy from reaching its full potential.

As an example, notice that you cannot deduce the win rate of a strategy from a few trades; many trades are required in order to find the accurate win rate. After many trades in a backtest, we will know what win rate the strategy tends to take on.

This averaging effect of the market applies directly to trading psychology. A few trades altered due to bad psychology can throw off the whole system, and the market will average these mistakes out throughout the strategies’ traded timeline. Over time, this will lead to a lot of disappointment.

Long losing streaks are inevitable in trading and should not be confused with ruin. They are tough, but they are the iron that sharpens you to parry the market with deeper cuts next time. Let us move on to Figures 3-4.

Figure 3: There is close to a 10 percent chance that you will experience a losing streak ≥ with a 50% winrate over 200 trades and 50% chance of a streak ≥10

Figure 4: This shows the average maximum drawdown (peak to trough) of a strategy with an average trading outcome of >0.3R (including gains and losses), especially at a higher trading frequency (e.g., day trading). This figure assumes the strategy maintains its edge.

## 4 The Solution

From the context provided so far, we should be able to conclude something important. Emotional intervention will never improve your profitability. Realising this will make you emotional in the opposite way. Now, you will be scared to intervene with the strategy, worrying that it will affect the profitability.

So test your robust systematic strategies correctly. Ensure that you know what to expect from a strategy based on your backtest. With this information at hand, know that intervening will lead to less money entering your pocket.

There should exist no factor which will lead a trader to make decisions based on their emotions. If there is, then the trader does not know their strategy. They have not tested it properly. They are unaware of the effects that intervening has, and hence they allow their emotions to take control.

## 5 Fear

I am scared to intervene with my strategy. I have tested it and analysed the data to the point where I would not even dare to change the location of a limit order by even the smallest amount. This is because I know that my strategy on its own will generate me money if I follow it precisely.

A strategy must be formed correctly in order for us to not want to intervene. Just know that the market does not care about how we feel, and if you do make a decision based on intuition or emotions, then you are only losing money for yourself, not for the market. The only person you are letting down is you. The market is already hard to trade as it is. We already require beautiful strategies to take advantage of the sliver of an edge that exists. Anything you do outside of your strategy just means that you are losing that small edge... for what?

In reality, traders will always feel emotions when trading. You may feel excited over a big trade, bored over a few losses, or optimistic for the next few days. It is the ability to simply not act on these emotions which will make you follow your strategy perfectly. You cannot eliminate yourself from feeling them, but you can eliminate painting the chart with them. They do not matter.

### 5.1 The Trick Question of Consistency

Most traders waste years chasing ”consistency”, but it is often a mental trap. Market changes and edge decay actively work against any form of long term stability.

Figure 5: Distribution plot based on retail profitability data. (12-month outcomes, harsh)

Performance will always decline eventually, drawdowns happen, and the vagueness of “consistency” amplifies performance anxiety. The question worth asking is, “Am I making money in a structured, intentional way?” As long as the gains are accumulated through sound research and testing, your gains are valid.

**Do not be enslaved by the outcome**

Retail consistency is comfort-driven. Institutional consistency is probability-driven. The professional idea of consistency is not emotional; they care about the consistent execution of their edge and exposure management instead.

**Retail wants certainty, but serious traders accept uncertainty as the cost of the**

edge. Serious traders ask “How do I ensure the edge plays out over time without blowing up?” instead of “How do I make money every day?”. For example, a +$10,000 month followed by a +$5,000 month followed by a -$3,000 drawdown month is 4k average per month, expect positive returns to be uneven.

Losing traders attempt to optimise for the frequency of reward, while profitable traders optimise for survival and scalability.

## References

[1] Discussion Paper DP25/3 Expanding Consumer Access to Investments - FCA December 2025

Do not chase consistency. It feels rewarding because of the grandeur the retail industry gives it, but when the occasional, inevitable periods of underperformance occur, the feeling of lost reliability and perceived control often takes its toll.

### 5.2 Priority Re-arrangement

To stay sane when establishing yourself in trading, never prioritise trading over your academics or career. The lack of certainty in profitable return distributions, combined with the pressure of sacrifice, makes variance over short samples feel far more cutting. It often puts people in an unnecessarily insecure position, which breeds loss aversion and flawed thinking. The rumination and pain are not worth it. Those university lectures and labs are some of the most sentient work you can do. Do not fold to social media’s sensationalism, 98% of posters do not show basic trading statements. When you see the nonsense lifestyle, swipe off it.

### 5.3 Biologically Attack Poor Psychology

Strip post-noon caffeine, get more sleep, and eat fewer snacks. Prepare your own food where you can. If caffeine-dependent, taper it off. A lot of people in our age group, especially, are hooked on ”slop”. Don’t see this as me talking from above, we have both abused caffeine in university, but the crash and how it tampers with sleep finishes most people off.

Many people like to gloss over the fact that these chemicals in our food slow us down, especially in higher doses. Depressants and stimulants, including alcohol and caffeine, amplify anxiety and should be reduced to see baseline improvement. I know not everyone can afford to consistently eat ”clean”, but try your best, especially before your trading days (Sunday to Thursday). Try to exercise regularly too, as it helps relieve stress. Amplified anxiety mixed with stress can quickly turn into fear, mitigate it naturally where you can.

## References

[1] Caffeine intake and anxiety: a meta-analysis This study shows that caffeine doses, especially 400 mg or more, were associated with a noticeable increase in anxiety risk compared to lower doses.

## 6 Revisiting Real Time Discretion - Ron

Discretionary traders who rely on intuition tend to have more psychological issues, regardless of if they are profitable or not. By being intuitive, you are forced to rely on yourself. This leads to drawdowns and overall poor performance/return drag being taken personally.

Systematic approaches nullify this problem. Suddenly, it is your systems underperforming which you would seek to optimise or replace.

We do feel pain; we are not robots. I just do not let it influence my real-time trading decisions when I am active. I have been through it and had to fight it, just like you. Once you have the evidence that your system works, psychology management becomes a hundred times easier.

All of my future possible decisions have been made before the strategy is deployed (it does not change from session to session). No intuitive real-time decisions, limited decision fatigue. Once you see and once you taste the P&L (Withdrawals). It is tough to relapse.

**When you enjoy the money, it sticks.**

When you start taking money out of your trading, consider spending some, so you experience what your discipline can provide.

**Through experience, the discipline becomes difficult to break;**

The longer your success persists, the more you will resist folding to flawed reasoning in real time.

**Discretion can be a part of rules.**

An individual’s specific success from having a “feel” for the market cannot be replicated by traders, so it is a suboptimal pathway to success for most traders. Remember, this is why you want mechanical trading strategies.

**These guidelines, combined with experience, will help a lot of people develop**

**that confidence they need in real time.**

### Discretion itself is not the enemy. Intuition is.

## 7 The Hidden Edge in Trading Is Removing Decisions

**The secret is to stop making real-time decisions.**

Make a profitable system grounded in logic with predefined rules regarding the entry logic for every entry, risk management and trade management ahead of time; with that, you will not need to think about anything when pressing the button besides executing your setup. Design your strategy so specifically that you have at least a good idea where your target, stop and entry are before your entry criteria is complete. This mitigates the chance of scrambling in real time.

**It is so much easier to be disciplined if you know the exact thing you are looking for in every trading session; people underestimate this. Ditch grandiose frameworks and trade something predefined, repeatable and real.**

For example, when you do not have to think about where your target is because you know the specific rules and sequence for every possible target, trading within your means becomes ultra-relaxed.

Before my entry technique has finished forming, I know where my entry price, stop, and target are on most iterations. That is real freedom. Zero decision fatigue.

**The only decision I leave myself with is putting that trade on. Even that decision is made in advance.**

Freedom in trading is not about having a constant fight or hustle, instead it is best to create space for clarity and control, allowing your trading edge to take over.

People talk about ”freedom” in trading but opt for methods that make trading draining. When everything is planned ahead and your trading behaviour is consistent, not only are your chances of profitability higher, but your mental stability will also be improved, especially under stress, e.g., drawdowns.

Efficient trading becomes boring when you first settle into it. The next step is to become creative with how laid-back you are, so execution becomes as close to effortless as possible. On most days, we cruise through our lives, adjusting and waiting for alerts to trade. We don’t rise to trade; we wire it to be the other way around, and that gives us the ultimate time freedom.

**Strategy Automation Nuances:**

A trader cannot automate their strategy if their rules are not ultra-precise and clear. That is common for most ”mechanical traders”; they think it is purely systematic until they are forced to code their strategy and see discretion or hard-to-define elements.

Automation is secondary if they have got a real edge in trading. Most do not.

**Common consequences:**

When traders try to find their edge through automation, most will end up with an overfitted system, which is when their strategy looks fantastic on a backtest but does not perform well in real time.

**Why:**

When a fitted to work well on noise that will not repeat 1:1 in real time. Many manual traders often tweak for the sake of better data, too, but with automation, it is sped up. What looks like casual optimisation easily turns into overfitting, which the market does not respect.

**For those who want to automate:**

We suggest you create your edge(s) manually to avoid overfitting; if you need or want to automate later, it is up to you.

## 8 Why we do not automate testing - Ali

We have yet to find a need to automate our backtesting for three main reasons:

1. Backtesting yourself allows you to get used to the strategy so that when you trade live, you are able to do so with fewer errors.

2. We put quality time into designing each strategy, meticulously defining the rules logically, so we do not need to create 20 new strategies at a time and test them until one clicks. This supports self-preservation, saves time, and mitigates the risk of overfitting. If you automate 1000 tests on loose logic, a few may appear to be extremely effective, which is misleading (false positives). Quality>Quantity.

3. When you backtest manually, it helps you gain experience and provides more insight into potential flaws in your strategies, and it may inspire other strategies. Having a computer do it for you can take that ability away from you. Manual work forces you to observe and address nuances up close.

4. We have done extensive manual backtesting ourselves; it only sharpens the mind. Automated backtesting requires you to double-check the data for discrepancies anyway. If one mistake slips through the cracks in automation, you may not see it until you realise in real time, when it is too late.

5. Part of it comes down to preference. If we were in a position where it would be extremely beneficial, we would do it, but backtesting is something you will enjoy doing, especially when you are rewarded with results for your participation. If you want to automate and have the skills, go for it; people under STS have succeeded with and without it.

### 8.1 Why we do not automate testing - Ron

**The Reality**

There are 1000s of potential strategies that would be effective, but there are just as many that can be based on hope. Through failure, you can detect this. If you only automate, selection bias risk increases by extreme amounts.

The longer you are in your building phase, the more you understand market logic. Everyone has different ideas, and people will naturally remember idea structures that are likely a waste of time.

**An average automation environment:**

- High sample

- High weakness

**Benefit:**

More frequent dopamine hits. A user feels like they have found something effective sooner, although it is less likely to survive stress tests or a live environment (a major problem).

**Consequence:**

Elevated selection bias risk (outliers are statistically more likely).

Automation may feel more enjoyable in the moment but often fast-tracks inefficient strategies.

**An average STS Environment (manual or automation-assisted)**

- Lower sample

- Noticeably lower weakness

**Benefit:**

More robust systems, as lower sample sizes are encouraged by our framework: strategy rules, timeframes, markets and other parameters have to be intentional and logic-driven for each strategy. This increases the integrity of each strategy indirectly by reducing selection bias risk.

Two amazing strategies out of 10 intentional, logic-first builds are much better than outliers out of a large sample of builds with, e.g., tweaked parameters or other changes seeking superior testing results before logic.

**Consequence:**

More time commitment per strategy, as the underlying logic is structured by the trader before testing instead of an automated script. For our traders who choose the automation path, the testing itself can still be automated after building.

### Now let us move on to the dark spots nobody covers.

# The Secret to Sticking to Your Trading Strategy (Even When It Hurts)

Sentient Trading Society (Public)

## 1 Introduction

A lot of traders are gaslit into thinking they have a discipline or psychology problem by educators. But in reality? They have a data problem. 9/10 of the time*.

If you cannot confidently answer questions like:

- “What would my results be if I traded this strategy’s exact rules over the past 12+ months?”

- “Would I have been profitable?”

The more guesswork (people call this intuition) that is required for your trading, the more likely you are to deviate from your set of rules.

When losing streaks come, which are inevitable (they will), most traders are left guessing, not knowing stats like maximum drawdown and maximum drawdown peak to trough. That guessing kills confidence.

Most traders (especially short-term) fall apart not because their system is bad, but because they have not put in the work to trust it. They are trading on hope rather than on data and mechanical proof.

## 2 A Personal Example

Last week (April 21st 2025, time of writing) I lost the equivalent of over $70,000, my biggest monetary drawdown ever. But I did not flinch. I kept trading my strategy. See Figure 1

Why? Because I have done the work. I have the data. I have tested the rules. I know my edge is real. That gives me the mental resilience to hold the line even when the market floors me like it did. Knowing peak-to-trough maximum drawdown is very helpful. Once you know your strategy has been in a drawdown equivalent to, for example, 13 consecutive losing trades (for example, −13% on 1% risk) these drawdowns are no longer scary. They become normalised.

Figure 1: Stop Losses From Intra-day Trading Dow Jones Q2 2025 - Ron

## 3 Data Over Discipline

So if you are constantly second-guessing yourself or jumping from one method to another, feeling uncertainty, you do not need more discipline. You need more data.

*The other 1/10 have a capitalisation problem. They cannot afford to lose their deposited funds. Prop firms are useful for filling that void if you have a profitable system.

You would not run a business without knowing the costs, margins, and profit expectations, so you should not do that with trading. Trading is a business.

A lot of people would not buy a product online without reviews but would trade a strategy with inadequate data to suggest the system is what you believe it is.

## 4 Practical Guidance

Backtest honestly without overfitting or curve fitting, preferably with bar replay software, for example, TradingView (a personal favourite).

Track results properly, preferably in a spreadsheet or text form, with stats or isolated trade setup details that can be grouped together and processed so you know how effective your system is, the returns to expect, and the maximum peak-to-trough drawdowns to expect.

Utilise it to build evidence and create a word document with screenshots explaining the rules if you need it.

## 5 Summary

Confidence does not come from wins. It comes from knowing your system has a legitimate edge. Of course, you will deviate or feel unsure if you do not have evidence to back what you are doing. Think of data as a case study to proceed with your plans.

Sentient Trading Society™

# What Is Back Testing Burnout?

Sentient Trading Society

Ron & Ali

## Introduction

Through conversations in Q1-Q2 2025 with several traders who are deep into backtesting and are complaining of feeling burnt out, fatigued, low energy, and an inability to push through their work. They are quick to rush into comfort and complacency, thinking their 30-sample size back test is somehow enough.

## 1 Trader Disillusionment

The experience these traders are having is disillusionment. Backtesting forces one to confront reality; a trader’s emotional investment in their system’s success causes them to feel synthetic fatigue when they encounter data that fails to validate their prior beliefs of the strategy’s profitability.

In essence, when you find out that the system which you worked hard to build is not working in the backtest, then you will feel upset, and feelings of time being wasted creep in. It makes you wonder if it is worth continuing to build strategies and test. It also makes you likely to just ignore backtesting entirely and trade live with this unproven strategy. But these feelings are only detrimental to your success. It is just not possible to achieve profitability instantly; it indeed takes a few tries even armed with the knowledge of how to design systems correctly. Your mind is just ”pretending" to be tired to avoid the rigorous work required to validate a strategy. For your sake, do not let this tiredness keep you from working hard. We have tested countless systems and it is hard to continue, but we kept going. Nowadays, it is far easier because of experience, but if you are not used to backtesting thoroughly, then it is hard to get used to it. It feels hard at first, but most traders do adapt if they keep going. We did.

## 2 Being Persistent

In our own work, we have found that approx. 8 out of 10 systems are not desirable enough for us to run. This conclusion only comes about after thoroughly testing and analysing each one You can idealise a strategy in your head all day. But when you start collecting the hard evidence in a backtest, psychology takes a toll. By ’psychology’ we are referring to the fact that traders will flinch; they will stall. They will tell themselves that they can finish the backtest later or that the minuscule amount of data gathered is enough, and the strategy is suitable enough to be executed live on their hard-earned money [1].

The truth is, it can be tiring to repeatedly commit time and not get what you want, but you must keep going. Every pushback saves time, as you get better at developing, and money, as you avoid a system with poor performance. You must persist, not yield, and obtain the robust systems you require.

## 3 Psychological Barriers

**A lot of the time, it is not the work that is hard; it is what the results might**

say. [2].

The core issue arises from a trader subconsciously recognising that their dataset (backtest data) is too small or the results are inconclusive or bad, leading to a drop in discipline. Of course, it is tempting to avoid that fear, but the true test of a strategy happens once this period of discomfort is ignored. Honest, thorough backtesting can give insight into whether a system is possibly going to lose you money or make you money.

You just do not know which is the outcome until the test is complete. So, push through and get it done.

## 4 Conclusion

Burnout happens due to disillusionment regarding your backtest. Recognise that for two well-trained traders, the difference between the one who finds a working strategy and one who does not is the backtest. Persist through the uncomfortable, boring, long periods, as this is the only way to ultimately develop a strategy that is likely to withstand the intensity of live markets. One thing to note is that similar feelings may occur when designing a strategy too, but that is a whole other story.

Thank you,

Ron & Ali

## References

[1] Odean, T. (1999). Do Investors Trade Too Much?.

[2] PMCID. (2021). Quantifying the Cost of Decision Fatigue.

# Discretionary trading & Its Psychology

Sentient Trading Society (Public)

## Discretion isn’t the enemy; intuition is.

Discretion can be okay as long as you run a fixed, consistent, logical procedure that’s been tested; it’s okay to run. (something most discretionary traders don’t do)

Personally, I and Ali are purely systematic traders, but if you want to apply discretion to be more flexible, here’s how to do things the right way.

## 1 Examples of acceptable discretionary elements:

1. Trader A: A day trader Ignores trade setups during news releases. He is selectively not applying his low-timeframe strategy during news for a logical reason (avoiding slippage). This is accounted for in his backtest ahead of time.

2. Trader B: A swing trader using a specific economic report or financial release to support his trade direction for the day or week consistently ex. Interest rate changes (Economic) or COT Reports (Financials) He uses it the exact same way. Every single time.

Trader B in this example is using COT Reports (Financials) in a way that’s consistent; if institutions are increasing long exposure, he wants to buy; vice versa. He might increase his risk for buys exclusively instead of eliminating shorts completely. There are multiple ways trader B could do this. He has it all backtested ahead of time.

## 2 Examples of common unacceptable discretionary elements:

**Intuition / Gut feel often veiled as ‘Experience’**

1. Trader C Feels like the price has dipped or spiked “too fast” towards his entry so he decides not to enter because recently these trades seem to hit the stop loss often. Trader C suffers from a nasty cocktail of Recency bias paired with Ad hoc reasoning by default, followed by a tragic mix of Hindsight bias + Confirmation bias if he was randomly “correct” on the occasion he deviated from his strategy’s rules. That’s how you get smoked.

**2.0.1**

**The reason this is dangerous:**

These deviations are untested so it adds noise to the person’s trading, randomising real-time trading results. & in a backtest environment, it causes inconsistent results.

The confirmation bias is terrible, as it tricks the trader into believing deviating from their strategy was a good idea.

Also, if the trader’s deviation backfires, they’ll likely absorb it personally and feel unnecessary pain.

The worst part. If deviating actually “works” for you a couple of times in a row, you might stick with it even if it begins to backfire, leading to unnecessary erasure of potential gains & amplified pain.

Why does this happen? Humans seek certainty and want to feel in control. These biases help the person feel safe; instead, it randomises the trader’s results. It’s not a conspiracy or a theory; this is human biology. You must set yourself to not fold.

Here is an example of a paper discussing it: https://pubmed.ncbi.nlm.nih.gov/20817592/

### 2.1 The repeated one-off event change

Trader D changes his trading behaviour risk based on events (The source doesn’t matter)

It’s not tested and accounted for in testing for example Trader D could think to himself after reciprocal tariffs that he’s going to ignore all of his long setups because people believe the market he’s trading will continue to decline.

Result: He misses out on buy setups during small pullbacks.

**2.1.1**

**Why this is dangerous:**

Even if it “worked”, the confirmation bias & hindsight bias would likely fuel Trader D to further sabotage his future trades, trying to randomly fit his day trading behaviour to random economic news events.

## 3 The Reality Behind Testing Avoidance and The Statistical Consequences

If you put in the work to make truly mechanical rules which have every IF, THEN, and ELSE DO THIS to incorporate every single outcome, it is possible to quantify >90% of intuitive strategies; many traders do not want to put effort into reverse engineering, or fear what the results may reveal: that is the primary issue at play.

For most traders, each setup has subjectivity influencing it - including the entry (for some it dominates decision making, for others it is residual).

### 3.1 The more a strategy is influenced by noise, the more the signal collapses.

A structured strategy slowly morphs into randomness over dozens of real-time trades if it has weak mechanical boundaries to operate within.

What I mean by “signal” here is the quality of the data or decision. The “signal” we want has objective logic, clear payout structures, and low amounts of randomness. Intuition provides the opposite of what we need, reinforcing itself as the sample size (the number of trades) increases. Hindsight trading techniques like Wyckoff rely on “judgement”, and the variability of a valid setup is what works against most traders.

Subjectivity (e.g., from intuition) is lethal because you cannot prove that something is effective or ineffective with real stats if it is unfalsifiable (subjective), as what cannot be objectively defined makes variance between each signal extremely high over time, thus increasing randomness exponentially, this causes results to average out to zero minus transaction costs, this is why we actively avoid an intuitive discretionary path.

It is easy to prove this statistical concept yourself quite easily without needing to code.

**3.1.1**

**An Accessible Monte Carlo Exercise:**

1. Use an LLM (like GPT) to run a Monte Carlo simulation of a breakeven 1:2 RRR system over 100k runs, 200 trades per run, using Python, and ask it to run it locally and provide the values in the chat (all contained within the same prompt).

2. Get the AI tool to output the statistics and percentile ranges, then ask it to output the 75th percentile equity curve visually on a chart plot.

3. Then ask it to output the 75th percentile equity curve visually on a chart plot.

4. Ask it to add 10% noise in decision making (10% of trades are not executed) and watch what happens to the P&L: it will randomly move up or down as a result, since the base strategy was not profitable; for real edges, this can reduce your profitability at random.

**This test only assumes that there are residual amounts of intuitive guesswork altering the strategy’s trading behaviour (10%); the dislocations in performance become a lot more profound if intuition influences trading decisions more than 10% (which is the case for most intuitive discretionary traders).**

The common point I make is that constant intuitive discretion is what causes the randomness over large samples, while consistent, genuinely systematic mechanical trading reduces it.

This early realisation is what made us never deviate from rule-based systems and have strict guardrails to avoid overfitting that we still use to this day.

## 4 Still unconvinced about the limits of intuition?

**Ask yourself this**

- How much value comes from following your profitable strategy as designed?

- How much value comes from the intuitive exceptions that you make in execution?

- Which one is more important?

If you imagine a graph with two lines, you will immediately notice that the system’s value is always higher than that of real-time exceptions because the strategy is the process behind your trades.

Whether your positions are based on price, indicators, or even fundamentals, the value (if any) provided by intuitive actions never surpasses the strategy, as the strategy is the foundation of all decisions made. For there to be convergence between the strategy’s value and intuition’s value, the win rate of the strategy would have to be doubled over a large sample. This would be like increasing a 1:2 RRR system’s 40% win rate to an 80% win rate, which is very unrealistic and unheard of. Intuition can also damage your average RRR per trade significantly, often even more than it damages win rate as seen in Figure 1.

Figure 1: The accumulated underperformance from intuition over 100 trades.

This is the potential damage intuition could have. In this scenario, we used over 100,000 unrelated simulations for a smooth, accurate representation.

**There is an equal probability statistically that gut feel has a positive or negative impact on your trading performance; outliers live in the far right side of the distribution of outcomes (imagine a bell curve) - it is based on chance, so design our strategies to remove this noise.**

The point is that intuition cannot surpass the trading idea if you have a profitable system. Intuition might turn a 1:2 RRR system’s win rate from 50% to 45% or 55%, but that modest potential increase in profitability does not measure up to what the system provides. Whether intuition is beneficial to an individual is largely random and person-specific bound by statistical laws regarding variance and the law of large numbers.

**Replace intuition with discipline by converting it into testable rules that apply discretion mechanically to your trading instead.**

## 5 Summary

So discretion in trading isn’t inherently bad; the lack of structure is. What makes intuition so destructive for most traders’ P&L is the aimlessness in trading, causing inconsistent execution patterns; this leads to random results because of decision noise. If discretion is used with discipline, pre-defined logic, and is consistently applied, it can absolutely enhance performance instead of eroding it. An example of this would be avoiding news trading consistently. Instead of generic rules like “close out all positions before news”, there could be a straightforward rule like “close out all positions exactly 15 minutes before news”, which can be factored into testing rigorously.

### 5.1 The key things that every trader should apply:

- Define Every Discretionary Rule: If you’re allowing yourself flexibility, write it down. A rule only becomes valid once it’s defined.

- Backtest or Forward Test: Every discretionary element should have a liquidity-related reason, e.g., News avoidance for slippage, Overnight bid-ask spread spikes etc. or historical data supporting its inclusion.

- Apply Consistency: Use your discretionary filters the same way each time. Random changes in decision-making destroy your edge.

- Separate Emotion from Adaptation: Adapting to new market conditions is logical;

reacting emotionally will get you humbled. Document why you’re making changes, if any, and test them.

- Stay Aware of Biases: Your cognitive biases, such as recency bias, confirmation bias, and the illusion of control, can be your real enemies that weigh you down if you allow them to. If you feel the insentience creeping in, make sure you note it down.

End note: A trader’s development at the start can often be a battle between emotion and structure, as they are not yet used to the hunt. Those who learn to tame discretion can build scalable consistency. Discretionary elements, when framed within logic, can become a useful tool but must be sequenced into rules.

**Additional Reading (Peer-reviewed papers):**

Trends in Cognitive Sciences, Behavioural Decision Making

**Thanks for reading - Ron**

# Read This Before You Tell Anyone You Are a Trader

Sentient Trading Society (Public)

Ali & Ron

## In This Document We Go Over

- Prevention and the mistakes to avoid, with personal examples and solutions.

- Your environment, trading groups, and the unseen consequences.

- Ego.

This document discusses social and psychological mistakes around talking about trading, with examples and ways to avoid them. It is intended for traders who want to reduce unnecessary pressure and setbacks caused by how they present their trading to others.

## 1 Social Mistakes Every Trader Should Avoid

Trading is a game of numbers and averages. It relies on the outcome of many, many trades. “Why tell someone how your trades are going when you have only placed 30? One of the biggest mistakes traders make socially is letting people know that they are planning on making this absurd amount of money and they have this trading strategy that will do it for them. Fast forward 3 years, and they continue to let people know." - Ali

As much as some traders try to appear humble about their intent, we all trade for money.

There is nothing wrong with having that attitude. Veiling it with “I do not trade for the money” or “do not trade for the money” is not helpful without context. - Ron

### 1.1 Personal Experiences with This Mistake (We Have Made Them)

I used to talk about trading and was overt with my small successes when younger.

When I was a teenager in school (around 16), I made close to £200 in one night on GBPUSD whilst sleeping out of luck. I was ecstatic. I told friends, my parents, and even my teachers. Luckily I was too young for it to be consequential. People probably did not take me seriously, so it was not so consequential (luckily).

For most people they have done something similar.

Doing this optimistic talk, even with parents or your significant other, creates performance anxiety. People will start to ask you, “How is your trading going?” or get concerned for you when they do not understand it is just another drawdown.

When I was 17–18, I had small wins here and there, short periods of profitability followed by devastation.

When I was profitable, it was met with scepticism. When I was struggling, I was looked down upon.

By the time I was 18–19, I fully understood this. I learnt these lessons the hard way. Many do not.

When I made my first life changing money in my trading, my family did not know for over a year. By then it was permanent. I did not flaunt.

I set social boundaries on asking about my trading and explained why.

I have made and lost thousands in university lectures and labs and did not say a thing.

**Do not subject yourself to this.**

I remember my grandmother saying to me, “Make sure you do not lose it all.” “Are you still gambling?” My mother said something along the lines of, “I see you are trying a lot with this. I do not want to be mean, but why do you not get a real job?” Ouch

And my father cornering me and questioning my goals:

“What are you going to do? What is your goal? What job are you going to get?”

This is the easiest way to get performance anxiety induced stress or feel demoralised, and it was all preventable by keeping my mouth shut, but I did not.

It is not that your family does not like you; it is that they do not understand trading.

They do not understand it or believe in it. A lot just see trading as gambling.

They do it because they care, not to destroy you.

These effects are often subconscious and still weigh you down.

I am telling you now, if my family (especially my mother) knew I was in a £100k peak-to-trough drawdown (over 130k USD) when I was, she would freak out, and things would be tough even post recovery. Do not even make me imagine it. It would be beyond unpleasant.

**It is not about hiding what you do; it is about having peace in your environment whilst performing. - Ron**

### 1.2 Telling or Encouraging Family or Friends to Trade - Ron

I want to keep this short. If you do this, you will create unrealistic expectations because of stimulation from your successes or retail social media BS.

In UK college (16–18), when someone approached me with TradingView open on my phone, I was silly enough to tell him that I was trading profitably at the time and talked about it.

They will get clingy, fast. Especially when you are “profitable.”

This is noise that you cannot afford to have in your development stage. It slows you down. You can still run while wearing a 10 kg/20 lb weighted vest if you are conditioned; even then it is still noticeably harder.

Even when full time. If my distant family or friends ask me, I still play it down and pretend like I do something else. It is not worth your sanity.

When you buy luxury goods such as a Rolex watch, you do not need to explain, flaunt, or post it. Do not get pushed into revealing what you do not want to; some are persistent or manipulative.

If you want a trading partner, make sure you both work efficiently and are both traders. Have high standards for traders you talk to. It matters.

The thing to do instead is play down what you do or, at most, say you are just looking into it. I know it feels good to talk about making money, but the best answer is no.

If they witness you trading live, just say it is a demo account.

If a person in public approaches you (has happened countless times to me and Ali), play it down and say invest in the S&P 500. Do not waste your time.

Listen to me. We have made these mistakes. Do not fold.

It is best to be quiet as it is far easier to succeed under these conditions.

If people do not know you trade, it is even better.

Keep quiet and set boundaries.

The short term dopamine spikes are not worth it. Do not confuse this for humility. You have a positive P&L to register.

## 2 Your Environment for Growth and Why It Matters:

## Trading Groups

### 2.1 Sharpen Your Edge by Choosing Your Circle

These are not opinions. This is behavioural psychology innate in us.

If you want a genuine long-term trading career, your environment is one of the main levers you can actually control.

One of the biggest reasons smart people do not make it in trading is not a lack of skill. It is the lack of environmental control.

Most of you are still hanging around Discords, Telegrams, and subreddits full of entertaining but directionless chatter, i.e., waffle.

You are soaking in the opinions of people who have not built anything, have not refined anything, and have not proven anything beyond a few lucky MT4/MT5 or journal screenshots.

Now, I need you to think about this logically.

If someone spends a lot of their time with smokers, even if they tell themselves, “I will never smoke; that is not me,” odds are eventually they will, even if it is just trying one.

Or testing that one logically flawed trading concept.

It is not always a direct influence. It is subtle. It shifts your baseline without you even noticing. It is innate in us; we are human beings.

You can like the cigarette; you could get positive backtest data on something baseless. Is that noise worth it if you do not want to smoke? Is that noise worth it if you want to succeed in trading?

You might not copy trades. But you will start absorbing the bad reasoning.

The loose discipline or approach. Shallow risk thinking. And broken retail logic.

And without realising it, you have let noise interfere with your trading once again. That gets expensive.

### The Uncomfortable Truth About Most Trading Communities

The moment you decide to get serious about trading. Truly serious.

You have to choose to block out negative influences. That means talking to and surrounding yourself with sharp, structured thinkers. People with systems, data, and discipline. Not just good vibes and memes. I know it is comfortable, but that was never enough.

If you are serious about having a real trading career, you will take action on this.

You owe yourself more. We want you to win.

That is what we built the Sentient Trading Society for.

We are not here to entertain foolishness, the Discord #rules channel reflects that.

We are here to win and to help you become the type of trader who earns their profitability with structure and self awareness, not ego, logical flaws, and emotions.

Now we get it. You probably like some of the people in these groups, and that is completely fine. Stay in touch with the smart ones if you want.

That is what we did.

During your development phase while you are still building your initial edges and refining your trading psychology, it is important to shelter your eyes from laymen. You need to cut the noise.

You need direction, not noise and stimulation.

The more you expose yourself to logical flaws, emotional responses, and low effort posts and thinking, the more that standard becomes yours psychologically.

Remember that this is not an opinion; it is behavioural psychology.

## 3 Ego

There is both a social and a personal consequence of ego. The focus will be placed on the social aspect, as that forms the basis of this document.

Traders have egos. We have seen this in almost everything. Sometimes traders struggle to accept other traders’ ideas, and they will always want to impose their thought processes even if they have yet to show any sort of system or returns. This is a problem because most traders lose.

Even based on probability, what are the chances that any one trader with an unchecked ego has managed to crack trading? What are the chances that one trader has figured out everything to do with the market? Likely less than a few percent.

A trader’s emotion is linked to their ego as well. They feel an emotional attachment to their current trading style, which they have probably developed over the years. Unfortunately, most traders lose money (easily near or above 90%), so the question a trader must ask themselves is if their trading style is the way it should be done. Just based on statistics, almost everyone is not doing it correctly. Yes, they may have the underlying understanding, but their application is lacking, and there are things they have not yet defined explicitly. For instance, traders think psychology is detrimental to trading, but that is not trading. That is gambling. The attachment to any existing style of trading has to be removed.

**We feel no attachment to any specific strategy or style.**

"Without this lack of an attachment, we would have been stuck on trendlines and crayons on a chart for the past few years. We realised early on that the only way to do this is to do what nobody else does properly and to have our knowledge so precise that it can be compiled without logical flaws, as we have done with the documents." - Ali

“Being too humble will not work. Delusion will not either." - Ron

“The only way to make proper returns is by understanding and being able to apply everything from the chart itself to the analysis behind the data, properly, with no logical flaws." – Ali

### 3.1 As Clear as I Can Be

If you want a real shot at this, leave these other trading groups. For now. Cut ties with trading environments that dilute your sentience, even if it feels uncomfortable at first. Immerse yourself where precision is normal. Where deep work is respected, not dismissed. Where sharp thinking is the minimum expectation of you.

Even we kept each other in check.

When you go full time one day, and many of you will likely lose that desire for old noise anyway. Entertainment stops being the goal when real mastery in strategy design and trading becomes the pursuit.

Until then, give yourself the best chance and cut the retail nonsense. Choose your environment the way you would choose your mentor. Intentionally.

We wish we had something like Sentient Trading Society. Now it exists. Do not dilute the advantages.

**End note:**

Let this piece serve as a push to steer your course towards the intention and consistency required. The way to develop both is through reading and refinement over time, with continued re-reading of the psychology section.

Each structured emergence from drawdown increases your confidence, and each material reinforcement makes you more sentient. You have the knowledge now, so the only thing left to do is fill the void with experience. Reading matters, but it must be matched with action.

If you have active or persistent issues with your trading psychology, we suggest revisiting STS’ psychology literature every 1 to 2 weeks, with plans to gather real-time experience.

If you are active and issues are arising in real time, do the same with the Logical Fallacy Handbook to develop the real-time cognitive dissonance required to avoid deviations.

Thanks for reading, and it will be a pleasure to see you succeed, both mentally and financially.

— The Sentient Trading Society

# Cognitive Conquest

Sentient Trading Society

Mental Frameworks & Discipline

Ron

## Introduction

Flawed reasoning and posture topple every empire. This document is built around this standard: if you break your rules, you do not explain it; you resolve it. When you see a group with weak hands, you do not comfort them; you disassociate. Feel above it, because you are. Those who treat financial markets as entertainment do not get paid. We must remain firm. Let us tackle one thing at a time, together.

### Crusade 1: Low-signal stimuli is optional, make the correct decision.

Being self-critical turns into shame, which only worsens your psychology. It subconsciously wires us to conceal mistakes, which leads to deeper cuts to our wellbeing. To dominate psychology, you must stare down your flaws in isolation. Lead by self-analysis instead of self-criticism. When you make an error, you must own it, diagnose the flaw, identify the trigger(s), and redesign your decision-making process so the moment you are about to bend a rule it feels wrong early enough to stop.

If you ever feel lost, revisit the Logical Fallacy Handbook.

You need to be in the place mentally where someone saying, “I lost $200 because I broke my rules”, feels absurd. If you are in a space where people relate to poor reasoning, it is only an anchor. Acceptance and exposure to excuses make us naturally susceptible to poor reasoning.

**Relativism does not produce a positive P&L in trading**

“Why would you knowingly violate a process that protects you?” This is about disassociation from what you should not be doing rather than shame. Leave those groups, and stay where accountability and rigour are normal.

### Crusade 2: Be responsible, attentive, and selfish with engagement.

Avoid risking money you cannot afford to lose.

Plan for consistency instead of impulse.

Do not use forums as a substitute for genuine reflection and change.

There is plenty of fruitless venting on social media, rewarded with engagement instead of reflection and growth. Many let the void created by poor trading decisions erode their lives. If you are not established, glance as you pass, but do not stop to watch the circus.

### Crusade 3: Maintain clean edges by not mixing systems.

A trader who mixes systems in testing (especially in forward tests) will never know what works. Confusion feels like complexity; our subconscious senses this inadequacy, weakening our subconscious faith in data. In backtesting, one instrument or setup may hold up better than another, but in real time the added variance from mixing systems worsens our psychology through uncertainty. It is dangerous because of how hard it is to notice until it’s too late.

One strategy has one path which feels more predictable.

One strategy, one logic, one set of rules per account. If you want to test an addition, test and run the strategies separately. Only introduce new ideas to an account if it is necessary. Clarity is the priority.

### Crusade 4: Do not worship the outcome and judge only the process.

The worship of outcomes is the fastest way to corrupt discipline. A winning rule breach teaches the worst lesson: that you can be rewarded for weak reasoning.

At the start must judge yourself by adherence rather than P&L. I know we are here to make money, but it must be accepted that the P&L is a by-product of discipline.

This is why we urge traders to taste their profit post-accumulation. It is by far the most effective way to follow the plan. Whether it is a nice piece of clothing or a nice meal, when you experience your gains, you will laugh at the idea of deviating. My first purchase was a £200 pair of shoes with “SPX” (for the S&P 500) embroidered on it, something small but memorable is enough to stick.

Build pride around clean execution. If a trade loses, and it was executed correctly, it is acceptable. If a trade wins, and it was taken incorrectly, treat it as debt because if the spiral of flawed reasoning continues, it will be collected later. If a profit was unintentional withdraw and forget, do not reward sloppiness.

If you are mentally anchored by individual outcomes, psychological issues will always be there. This profession is about hundreds of trades not a couple of dozen.

### Crusade 5: Reduce ego exposure, anonymity protects discipline.

Ego needs an audience. Once you start performing, you start defending a persona, and the market will indirectly probes it for weakness. When people are watching, losing streaks start to feel like a growing threat to your status rather than just another drawdown.

Avoid public predictions, public P&L, and public debates. They create pressure to be right instead of pressure to approach markets correctly. The best traders protect their process from social contamination.

Your results are private. Let your behaviour validate itself; you do not need a crowd.

### The Most Dangerous Retail Trading Tropes

**“Psychology fixes bad strategy.”**

**Reality:**

Discipline cannot save negative expectancy if your strategy returns negative, it doesn’t matter how disciplined you are; the market will break you.

**”It takes years to find your first trading edge.”**

**Nuance:**

It only takes years if you are aimless and without good resources and/or a solid mentor. Success doesn’t occur overnight; it comes from a sequence of correct decisions, since trading outcomes are fundamentally path-dependent. The biggest red flag is when a so-called educator says it will up to take years to learn their way of operating. They are subtly communicating that their way or results are not reproducible. People waste years of their lives chasing discretion or intuition-based strategies.

### The Three Trojan Horse Statements

1. ”This path is very long.”

2. ”You just need to give this trading methodology time.”

3. ”It is really rewarding to those who can see it through. I’ve seen a guy make $100k using this strategy.” Anecdote.

When unprofitable traders recommend a trading method, it’s often a way to further rationalise the months or years they have already invested. It serves as a defence mechanism; it’s for them, not for you. Traders can sacrifice a great deal of time and effort; for many, it hurts less to keep believing in their method than to move on.

The markets do not care how long a trader has persisted with flawed logic; substance is rewarded and aimless perseverance is dismissed.

**Those who ignore this remain anchored by the sunk cost fallacy for years.**

Flawed reasoning is the enemy.

“Every losing trader says psychology matters more than a real trading edge.

Sit in the silence and wonder why.”

- Ali

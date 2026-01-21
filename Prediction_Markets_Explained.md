# Prediction Markets: Complete Guide & Explanation

**Based on the a16z crypto podcast featuring Alex Tabarrok and Scott Kominers**

---

## Table of Contents

1. [Executive Summary](#executive-summary)
2. [What Are Prediction Markets?](#what-are-prediction-markets)
3. [How Prediction Markets Work](#how-prediction-markets-work)
4. [Market Mechanics & Design](#market-mechanics--design)
5. [When Prediction Markets Work (and When They Don't)](#when-prediction-markets-work-and-when-they-dont)
6. [Information Aggregation Mechanisms](#information-aggregation-mechanisms)
7. [Corporate & Internal Applications](#corporate--internal-applications)
8. [Blockchain & Crypto Features](#blockchain--crypto-features)
9. [Future Applications](#future-applications)
10. [Key Debates: Gambling vs. Speculation](#key-debates-gambling-vs-speculation)
11. [Critical Concepts Reference](#critical-concepts-reference)

---

## Executive Summary

This document explains prediction markets comprehensively, based on expert insights from:
- **Alex Tabarrok**: Professor of Economics at George Mason University
- **Scott Kominers**: a16z crypto research partner and Harvard Business School professor

**Key Takeaways:**
- Prediction markets are among the best forecasting mechanisms available
- They aggregate dispersed information through price discovery
- They often outperform polls and statistical models
- Success depends on market "thickness" (participation + stake size)
- Blockchain enables new features: commitment, transparency, composability
- Applications extend far beyond elections: corporate decisions, scientific validation, governance

---

## What Are Prediction Markets?

### Definition

A prediction market is a market created specifically to produce information through the aggregation of dispersed knowledge. Participants buy and sell assets whose value depends on uncertain future events.

### How They Differ from Polls and Betting

| Aspect | Prediction Markets | Polls | Traditional Betting |
|--------|-------------------|-------|-------------------|
| **Incentive** | Financial stake in accuracy | None (voluntary) | Entertainment/gambling |
| **Information Flow** | Continuous price discovery | One-time snapshot | Odds set by bookmaker |
| **Accuracy** | Self-correcting via arbitrage | Subject to sampling bias | House edge built in |
| **Purpose** | Information aggregation | Opinion measurement | Entertainment |

### Core Principle: The Hayek Insight

Based on F.A. Hayek's 1945 paper "[The Use of Knowledge in Society](https://www.econlib.org/library/Essays/hykKnw.html)":

**The Problem:**
- Information is dispersed across millions of people
- It exists in people's heads (preferences, knowledge, local conditions)
- It's fleeting, tacit, hard to communicate to central planners

**The Solution:**
- Markets give people incentives to reveal information through buying/selling
- Prices embed this dispersed information
- **The price can know more than any single person in the market**

### Example: 2024 U.S. Election

- Prediction markets showed Trump with higher probability than polls suggested
- Markets priced in information from diverse sources:
  - Traditional polls
  - Local/neighborhood sentiment (e.g., the "neighbor poll")
  - Early voting data
  - Historical patterns
- The "French whale" reportedly won big by commissioning his own neighborhood polls and betting on that information

---

## How Prediction Markets Work

### Basic Mechanism

**Simple Example:**
1. Asset pays $1 if Trump wins, $0 if he doesn't
2. If market price is $0.55, this implies 55% probability of Trump winning
3. If you believe probability is 70%, you expect $0.70 value
4. You buy at $0.55, expecting $0.15 profit
5. Your buying pushes price toward $0.70
6. **You've revealed your information by pushing the price closer to truth**

### Price as Information Aggregator

The price represents a "convex combination" of all participants' probability estimates, weighted by:
- Confidence level (how much they stake)
- Information quality (better informed traders stake more)
- Speed of action (strong signals prompt quick trades)

### The Wisdom of Crowds (with caveats)

**Classic Example: Weighing the Cow**
- Ask crowd to guess cow's weight
- Individual guesses vary (some too high, some too low)
- **Median prediction is remarkably accurate**
- The crowd knows more than any individual

**Critical Distinction:**
- This is **wisdom of an informed crowd**, not a random crowd
- HP employees predict printer sales well (they have information)
- Random people can't predict HP's product launch dates (no information)

### Validation: Calibration Testing

**You can't evaluate a prediction market on single outcomes!**

**Wrong approach:**
- "Market said 40% chance of Trump winning in 2016, but he won. Market was wrong!"

**Right approach:**
- Look at large sample of predictions
- When market predicted 40% probability, did event happen ~40% of the time?
- **Answer: Yes**, prediction markets show strong calibration
- Events predicted at 5% probability happen ~1 in 20 times
- Events predicted at 70% probability happen ~7 in 10 times

---

## Market Mechanics & Design

### Thin vs. Thick Markets

**Thin Markets:**
- Few participants
- Small bet sizes
- Problems:
  - Limited information aggregation
  - Low incentive to research
  - Vulnerable to manipulation
  - May miss important information

**Thick Markets:**
- Many participants
- Large bet sizes
- Benefits:
  - Rich information aggregation
  - High incentive to research ($10,000 profit justifies $1,000 research cost)
  - Resistant to manipulation (arbitrageurs correct false signals)
  - Captures diverse information sources

**Why market size matters:**
If maximum possible profit is $1,000, you won't invest $10,000 in research to improve your estimate. The market thickness determines research incentives.

### The "Sharks and Farmers" Problem

**Why don't we have prediction markets for everything?**

Using wheat market as analogy:
- **Farmers**: Trade to hedge, not to predict (organic demand)
- **Sharks**: Use models/analysis to profit from predictions
- Farmers provide subsidy that makes market thick enough for sharks

**In pure prediction markets:**
- No "farmers" (no organic trading demand)
- Only "sharks" competing against each other
- No one wants to be in a shark-only market
- **Solution**: External subsidy required

### Subsidizing Prediction Markets

**Methods to create thickness:**

1. **Corporate Subsidy**
   - HP gave employees $100 to trade (internal market)
   - Company values the information output

2. **Natural Interest**
   - Elections have inherent public interest
   - Creates some "latent demand" from curiosity

3. **Token-Based Systems**
   - Internal currency/tokens
   - Limits use to prediction markets
   - Equalizes participants at entry
   - Reputation-based rewards

### Market Manipulation & Self-Correction

**Famous Example: Obama vs. McCain**
- Someone tried to sink money to move McCain percentage
- Traders who believed Obama probability was higher arbitraged it out in 1-2 hours
- **Markets self-correct when manipulated**

**When Manipulation Can Work:**
1. **Thin markets** - not enough arbitrageurs to correct
2. **Sybil attacks** - many fake identities create false consensus
3. **External outcomes depend on prediction** - manipulate prediction to influence behavior
   - E.g., candidates campaign less in states they're "losing"

### Preventing Manipulation Through Design

**Circuit Breakers:**
- Slow down trading during rapid movements
- Prevents contagion/herding
- Like stock market circuit breakers

**Orthogonalization:**
- Robin Hanson's proposal: Create second market predicting whether first market will revert
- Extracts signal independent of potential manipulation

---

## When Prediction Markets Work (and When They Don't)

### When They Excel

**Best Use Cases:**
1. **Aggregating dispersed expert knowledge**
   - Scientific paper replication predictions
   - Project completion timelines
   - Sales forecasts

2. **Revealing hidden information**
   - Employees know project is delayed but won't tell boss
   - Anonymous market reveals truth
   - Challenger disaster: employees knew O-rings were problem

3. **Events with rich information environment**
   - Elections (polls, local knowledge, historical data)
   - Economic indicators (many data sources)
   - Corporate metrics (multiple informed employees)

### When They Fail

**Limitations:**
1. **"You don't know what you don't know"**
   - Can't predict invention of iPhone (Jobs: "best way to predict future is to invent it")
   - Xerox PARC couldn't use prediction markets to decide what to invent
   - Matt Gaetz attorney general: resolved to zero for all listed options (he wasn't listed!)

2. **No dispersed information exists**
   - AT&T picture phone: even company insiders couldn't predict market failure
   - Aggregate of zero information = zero useful signal

3. **Wrong crowd**
   - Random people can't predict HP printer release dates
   - Need informed participants with relevant knowledge

### Domain Expertise vs. Information Richness

**Key Insight: It's not about "experts" vs. "non-experts"**

It's about **who has relevant information**:

- **Scientific replication**: Domain experts have advantage (can read statistical analysis)
- **Elections**: Both political experts AND locals with neighborhood knowledge matter
- **The "obsessive guy"**: Made $10,000 on scientific replication market through pure effort/analysis

**You often don't know who the expert is until after the market runs** - they reveal themselves by being profitable.

---

## Information Aggregation Mechanisms

Prediction markets are **one type** in a broader class of information-elicitation mechanisms.

### 1. Prediction Markets
**How it works:**
- Buy/sell assets with payouts tied to events
- Price = aggregated probability estimate
- Payout delayed until event resolution

**Best for:**
- Thick markets with many participants
- Objective, verifiable outcomes
- Long time horizons acceptable

### 2. Peer Prediction Mechanisms

**How it works:**
- Ask: "What do you believe?" AND "What do others believe?"
- Cross-examine answers for consistency
- Bayesian logic: If you think Trump wins, you think others think Trump wins
- Pay based on accuracy about population beliefs, not event outcome

**Advantages:**
- **Immediate payment** (no need to wait for event)
- Works for thin markets / small populations
- Useful for subjective information

**Example Application:**
- Hussam, Rigol & Roth paper: Identified successful micro-entrepreneurs in developing countries
- Asked community who would succeed
- More accurate than self-reporting (people lie to help friends)

### 3. Surprisingly Popular Mechanism

**The Problem:**
- Wisdom of crowds fails when crowd is systematically wrong
- Example: "What's capital of Pennsylvania?"
  - Majority: Philadelphia (WRONG)
  - Minority: Harrisburg (CORRECT)

**The Solution:**
1. Ask: "What's the answer?" AND "What will others say?"
2. Most people: Philadelphia / Others will say Philadelphia
3. **Surprise signal**: More people say Harrisburg than expected
4. Harrisburg is "surprisingly popular" → likely correct!

**Key Innovation:** Extracts truth even when majority is wrong.

### 4. Auctions

Auctions are also information aggregation mechanisms:
- Price discovery for rare items (art, collectibles)
- Single sale reveals information affecting all similar items
- Artist has major sale → estimates of all their works increase

**Recommended Reading:** "Auctions: The Social Construction of Value" by Charles Smith

### 5. Bayesian Truth Serum

**For subjective beliefs:**
- Ask: "Did you like this movie?"
- Ask: "What % of others will say they liked it?"
- If you lie about liking it (to be polite), your estimate of others' beliefs will be inconsistent
- Reward accuracy → incentivizes truthful revelation

---

## Corporate & Internal Applications

### HP Printer Sales Prediction

**Setup:**
- Internal market for HP employees
- Predict quarterly printer sales
- Each employee given $100 to trade
- Correct predictions earn money

**Benefits:**
- More accurate than traditional forecasting methods
- Aggregated knowledge from sales, engineering, marketing, regional offices
- Each employee has partial information; market combines it all

### Project Completion Timing

**The Problem:**
- Employees tell boss: "Ready in 5 weeks!" (optimistic)
- Employees tell friends: "Delayed, tons of problems" (realistic)
- PowerPoint format constrains information flow (Challenger disaster case)

**Prediction Market Solution:**
- Anonymous trading reveals true beliefs
- Delays surface even when no one will tell management directly
- **Markets as communication mechanism**

**Lesson:** Prediction markets elicit information employees know but won't formally report.

### When NOT to Use Internal Markets

**HP Example Works Because:**
- Many employees have relevant information
- Outcome depends on aggregate of that information
- Sales calls, production status, market conditions

**Xerox PARC Example Fails Because:**
- Trying to predict whether imagined product will succeed
- Company doesn't have unique information vs. market
- AT&T picture phone: Even with all internal info, couldn't predict failure
- **Total information insufficient even when aggregated**

### The Scientific Replication Crisis

**The Problem:**
- Psychology and other fields have replication crisis
- Many published papers don't replicate
- Expensive to replicate every paper

**Prediction Market Solution:**
1. Create market: "Will this paper replicate?"
2. Market predicts with high accuracy
3. Only replicate papers where needed to validate market
4. Use market predictions for the rest

**Benefits:**
- Makes science better, quicker, more accurate
- Efficiently allocates replication resources
- Crowd-sources expertise evaluation

---

## Blockchain & Crypto Features

### Is Crypto Necessary?

**Alex Tabarrok's View: Probably no.**
- Polymarket succeeded because it was open globally (except U.S.)
- Thickness came from global access, not crypto itself

**Scott Kominers' View: Depends on context.**
- More complicated mechanisms → more value from crypto
- Simple internal HP market → doesn't need blockchain
- Complex, trustless, global markets → blockchain shines

### Key Features & When They Matter

#### 1. **Public / Transparency**

**What it means:** Prices/information visible to all

**When essential:**
- Prediction markets (need to see price to trade against it)

**When NOT essential:**
- Peer prediction (only need transparent resolution, not interim states)
- Internal corporate markets (limited audience)

**Design Implication:** Can be off-chain initially, on-chain for final settlement

#### 2. **Credible Commitment**

**What it means:** Trustworthy guarantee that system will execute as promised

**The Problem:**
- "I'll pay you in 6 months based on accuracy"
- Participants worry: Will you actually pay?

**How Blockchain Helps:**
- Code commits to execution
- Immutable, auditable by all users
- Creates property rights without centralized enforcer
- Expands possible marketplaces (don't need to trust organizer)

**When CRITICAL:**
- Long time horizons until resolution
- Contexts lacking institutional trust
- Micro-markets ($5 bets on trivial questions)
- International markets (no clear jurisdiction)

#### 3. **Decentralization**

**Multiple Components:**

**A) Availability/Uptime:**
- Distributed nodes prevent single point of failure
- Market going down election night = lost information + lost participation
- Note: Distributed ≠ Decentralized (can have centralized entity with distributed nodes)

**B) Resolution/Oracle:**
- Prevents largest bettor from controlling outcome
- If biggest trader controls oracle, they can lie about results
- Decentralized oracle = no single entity can manipulate

**When NOT needed:**
- Information already on-chain (no oracle required)
- Trusted central operator with reputation at stake

#### 4. **Oracles**

**Definition:** Source of truth bringing off-chain information on-chain

**Examples:**
- 2024 U.S. election happened off-chain
- Oracle tells blockchain who won
- Common approach: New York Times = oracle (if NYT says Trump won, resolve accordingly)

**Security Challenge:**
- All the money rides on resolution
- **Massive incentive to distort oracle**
- Many crypto hacks exploit oracle manipulation

**Famous Cases:**
- Fake SEC tweet about Bitcoin ETF (briefly affected markets)
- "Dewey Defeats Truman" headline (wrong information from trusted source)

#### 5. **Composability**

**What it means:** Lego-block architecture, combine with other tools

**Why it matters:**
- Predictions affect decisions (which supplies to order? depends on tariff likelihood)
- Other processes can read from prediction markets
- Wrap predictions with corporate operations
- Create derivative products/markets

**Example Use:**
- DAO governance reads prediction market signals
- Automated supply chain adjusts based on policy predictions
- Risk management systems incorporate probability feeds

#### 6. **Open Source**

**When it matters:**
- Less trust in market creator → more need for auditable code
- High-stakes markets → verify mechanism works as claimed

**When less important:**
- Strong institutional trust
- Legal contracts enforceable
- Reputation-based systems

**Spectrum:**
- Commodity markets: Trust through institutions + legal contracts
- Blockchain markets: Trust through code
- Micro/international/unusual markets: Code substitutes for absent institutions

### AI & Blockchain Synergy

**Vitalik Buterin's "Info Finance" Post:**
- AIs may become prominent prediction market participants
- Lowers cost of prediction dramatically
- Opens new possibilities for market applications

**Why Blockchain + AI:**
- "Nobody knows you're an AI on the blockchain"
- Proof of personhood (distinguish humans from AI when needed)
- Attribution in privacy-preserving ways
- Decentralization counters AI centralization tendencies

**Vision:** Original AGI = human intelligence at scale through markets

---

## Future Applications

### 1. CEO Decision Markets (Robin Hanson)

**The Question:** What would happen to stock price if we fired the CEO?

**Current State:**
- We learn the answer ONLY when CEO is actually fired
- Steve Ballmer left Microsoft → stock price jumped (market thought he was poor CEO)
- Brian Nichols to Starbucks → stock price jumped (market approved)

**Prediction Market Approach:**
- **Continuous market:** Stock price if CEO stays vs. if CEO fired
- Learn answer WHEN it's useful (during decision-making)
- Not AFTER decision made

**Why This Works:**
- People already invest billions analyzing what affects stock prices
- Rich information environment already exists
- Brings information FORWARD in time to when it's actionable
- Leverages existing expertise for new question

**Pathway to DAO Governance:**
- Start with CEO question (highest stakes, information-rich)
- Expand to: Should we expand into Argentina or China?
- Should we launch new model this year?
- Progressive experience with decision markets
- Eventually → automated DAO decision-making

**Token Design for DAOs:**
- Participants may have wealth inequality
- Use internal tokens to equalize entry
- Allocate based on reputation, not wealth
- Enable equitable participation in decision markets

### 2. Scientific Publishing & Validation

**Applications:**
- Which papers will replicate? (already discussed)
- Which research directions are promising?
- Peer review quality assessment
- Grant allocation optimization

### 3. Private Data Markets (DeSci)

**The Problem:**
- Individuals have valuable medical/health data
- Could help design treatments/pharmaceuticals
- Need fair compensation + privacy

**Prediction Market Approach:**
- Individual data ownership on blockchain
- Permissioned access with transparent compensation
- Incentivized contribution to medical research
- Decentralized science (DeSci) movement

### 4. Subjective Belief Elicitation

**Beyond Objective Truth:**
- Market research: Do people actually want this product?
- Crowdfunding as information mechanism (money = real signal vs. "yes I'd buy" = cheap talk)

**Advantage:**
- Incentivized revelation of true preferences
- Distinguishes real demand from polite responses

### 5. News Media Reinvention

**Vitalik's Formulation:**
- Prediction market = "betting site for participants, news site for everyone else"

**Problems with Current Media:**
- No skin in the game
- Partisan filtering
- Slow to self-correct

**Prediction Market Advantages:**
- Participants stake real money on beliefs
- Faster self-correction than traditional media
- Less partisan distortion (though depends on participant pool)

**Alex Tabarrok's Proposal:**
"A bet is a tax on bullshit"

**For Journalists/Editorialists:**
- Disclose your bets on-chain
- Track record visible to all
- Promote those with accurate predictions
- Weight predictions by confidence (not binary)

**Annie Duke Approach:**
- Not "X will happen" (binary)
- "80% confidence X will happen" (probabilistic)
- More nuanced assessment possible

**Benefits:**
- Reduces hyperbole ("This will NEVER happen!" → "Well, I won't bet on it...")
- Even critics adjust beliefs with new information
- Skin in the game changes incentives

### 6. Community Information Aggregation

**Community Notes on Twitter:**
- Information aggregation mechanism
- Only shows note if people who usually DISAGREE both agree
- Cross-examines beliefs against political/ideological opposition

**Contrast with Wikipedia:**
- Failed when expert cabal controlled reviews
- Lacked check-and-balance mechanism

---

## Key Debates: Gambling vs. Speculation

### The Continuum

**Pure Gambling (Slot Machines):**
- Pure randomness
- No information can improve predictions
- Moving money has no impact on outcomes
- Zero social value

**Useful Speculation (Prediction Markets):**
- Information exists and can be gathered
- Investing helps improve predictions
- Moving money aggregates dispersed knowledge
- **Produces public good** (better forecasts)

**Speculation on Speculation:**
- Betting on what others will bet, not on outcomes
- Herding behavior
- No new information generated
- Independent of actual outcomes

### The Mid-Space Sweet Spot

**Well-architected prediction markets:**
- Large, thick (as discussed earlier)
- Designed features to prevent herding
- Provide **valuable information from real knowledge**
- Market activity creates social value

### Policy Implications

**Alex Tabarrok's Argument:**
"Of all the forms of gambling/speculation, this is one of the most useful forms"

**Why Legalize:**
- Sports betting is legal and huge (purely entertainment)
- Prediction markets produce socially valuable public goods
- Better forecasts for:
  - Climate change
  - Scientific research validity
  - Public policy outcomes
  - Corporate decisions

**Current Situation:**
- Largest 2024 election prediction market NOT in U.S.
- U.S. citizens couldn't legally participate
- Lost information from people closest to the events

### Carlota Perez Framework

**Technology Cycles:**
- Speculation phase → Installation phase
- Speculation can DRIVE innovation

**Byrne Hobart's Work:**
- "Well-behaved bubbles" can be good
- Book: "Boom" (Stripe Press)
- Distinction: **Useful speculation** (leads to real outcomes) vs. speculation for its own sake

---

## Critical Concepts Reference

### Quick Definitions

**Thick Market:** Many participants betting large amounts (information-rich)

**Thin Market:** Few participants betting small amounts (information-poor)

**Wisdom of the Crowds:** Aggregate estimate more accurate than individuals (requires informed crowd)

**Price Discovery:** Process by which market trading reveals true value/probability

**Arbitrage:** Trading to profit from price discrepancies (self-corrects manipulation)

**Oracle:** Source bringing off-chain information on-chain for contract resolution

**Futarchy:** Robin Hanson's proposed government form where markets make policy decisions based on agreed metrics (e.g., GDP+)

**Calibration:** Statistical property where predicted probabilities match actual frequencies

**Peer Prediction:** Mechanism comparing beliefs about outcomes to beliefs about others' beliefs

**Surprisingly Popular:** Mechanism identifying correct answer as most surprising deviation from expected consensus

**Information Aggregation:** Process of combining dispersed knowledge into useful summary statistic

**Convex Combination:** Weighted average (market price = weighted average of all traders' estimates)

**Herding:** Following others' trades regardless of own information

**Contagion:** Rapid spread of trading behavior (like infection)

**Circuit Breaker:** Temporary halt to prevent rapid contagion

**Bayesian:** Updating beliefs based on new evidence (rational information processing)

**Composability:** Ability to combine/build on existing systems (Lego blocks)

**Credible Commitment:** Trustworthy promise to execute as specified

**Zero-Sum:** One person's gain is another's loss (pure prediction markets)

**Subsidy:** External support to make market thick enough to function

**Sybil Attack:** Using many fake identities to create false consensus

**Dark Pool:** Private trading venue (vs. public exchange)

### Key Papers & Resources Referenced

1. **Hayek (1945)** - "[The Use of Knowledge in Society](https://www.econlib.org/library/Essays/hykKnw.html)"
2. **Morris & Shin** - "[Social Value of Public Information](https://people.duke.edu/~qc2/BA532/2002%20AER%20Morris%20and%20Shin.pdf)"
3. **Prelec, Seung, McCoy** - [Surprisingly Popular](https://www.nature.com/articles/nature21054)
4. **Hussam, Rigol, Roth** - [Targeting Entrepreneurs](https://www.hbs.edu/ris/Publication%20Files/Targeting_Entrepreneurs_AER2022_64933cef-316a-437f-8ca4-885d870b2ba1.pdf)
5. **Robin Hanson** - [Futarchy](https://mason.gmu.edu/~rhanson/futarchy.html)
6. **Robin Hanson** - [Idea Futures](https://mason.gmu.edu/~rhanson/ideafutures.html)
7. **Vitalik Buterin** - [Info Finance](https://vitalik.eth.limo/general/2024/11/09/infofinance.html)
8. **Charles Smith** - "Auctions: The Social Construction of Value"
9. **Philip Tetlock** - Superforecasting work
10. **Richard Roll** - Orange juice futures & weather prediction
11. **Edward Tufte** - Challenger disaster & PowerPoint analysis
12. **Byrne Hobart** - "Boom" & well-behaved bubbles

### Market Design Decision Matrix

**When designing a prediction market, consider:**

| Question | Impact |
|----------|--------|
| How complicated is the mechanism? | More complex → more value from crypto rails |
| Who has relevant information? | Determines necessary participants |
| How much info do they have? | Affects optimal subsidy level |
| Is it objective or subjective? | Objective → prediction market; Subjective → peer prediction |
| When is resolution? | Long delay → need stronger commitment |
| Is there organic trading demand? | No → need subsidy |
| How much institutional trust? | Low → need blockchain commitment |
| Need transparency of interim states? | No → can be off-chain |
| Who controls resolution? | Centralized → manipulation risk |

---

## Conclusion

Prediction markets represent one of humanity's most powerful tools for aggregating dispersed information and forecasting the future. They succeed when:

1. **Information exists** dispersed across many people
2. **Market is thick** enough (participants + stakes)
3. **Design prevents** manipulation and herding
4. **Incentives align** to reward accuracy
5. **Right participants** have access

The future likely includes:
- Widespread corporate use for decisions
- DAO governance mechanisms
- Scientific validation systems
- AI-enhanced prediction generation
- Blockchain-enabled global markets
- Integration with news/media

**The core insight:** Markets aren't just for allocating goods—they're for discovering truth.

---

*Document created to explain "PredictionMarkets - everything you need to know.md"*
*Total source length: 1,036 lines | ~29,757 tokens*

# Prediction markets — everything you need to know

Prediction markets are a hot topic again — even cartoon characters are talking about them (cf South Park). But beyond the buzz, what is a prediction market, exactly? How do they work, how are they designed, and what _makes_ them work?

We answer all these questions and more in this deep-dive featuring experts [Alex Tabarrok](https://economics.gmu.edu/people/atabarro) (professor of economics at George Mason University) and [Scott Kominers](http://www.scottkom.com/) (a16z crypto research partner and Harvard Business School professor), in conversation with [Sonal Chokshi](https://a16zcrypto.com/team/sonal-chokshi/).

While we originally covered this topic during last year’s election, the discussion is more relevant than ever today, as we go into the claims people make about prediction markets — what they’re good for (and not); how they fit in with other trends like [AI](https://a16zcrypto.com/posts/tags/ai-crypto/), futarchy, and the crisis in scientific publishing; and where blockchains and crypto come in.

This is your definitive explainer on the topic.

## time stamps

- **1:04** – what prediction markets are, vs. polls, vs. betting
- **5:18** – how incentives work
- **8:06** – when they do and don’t work
- **11:20** – wisdom of the crowds
- **12:14** – how price reflects information
- **14:14** – potential market manipulations & edge cases
- **22:19** – designing a market, incentive mechanisms
- **23:52** – other information aggregation mechanisms
- **27:56** – internal prediction markets & predicting innovation
- **33:42** – more on thin vs. thick markets…
- **34:36** – prediction markets as public goods
- **36:16** – do you need domain experts?
- **41:52** – other incentives besides money
- **43:54** – where do superforecasters come in
- **45:25** – ‘everything is priced in’
- **47:46** – effects of herd behavior
- **49:43** – market design to prevent contagion
- **51:37** – futarchy
- **53:54** – more on efficient markets, examples
- **57:02** – key technology features (& where blockchains come in)
- **1:00:53** – does decentralization matter, transparency
- **1:04:17** – contract resolution & role of an oracle
- **1:09:17** – composability
- **1:12:37** – from prediction markets to ‘info finance’, AI
- **1:14:41** – other information aggregation mechanisms, research findings
- **1:19:23** – …including auctions
- **1:20:31** – how to decide on market mechanisms
- **1:21:32** – a note on payouts: timing, how
- **1:22:56** – and on discrete vs. continuous events
- **1:42:34** – interesting & other future applications

## transcript

_Welcome to web3 with a16z, I’m Sonal Chokshi, and today’s episode is about a hot topic right now – prediction markets! — What are they, specifically; how do they work; how to design them; and much more…_

_This is your definitive explainer, because we go deep with two top experts: Alex Taborrok, professor of economics at George Mason University (and the first voice you’ll hear); and Scott Kominers, a16z crypto research partner and Harvard Business School professor._

_While we cover how prediction markets came back into the conversation with last year’s election (which is when we first recorded this), the discussion is very relevant today — as we go into what’s hype vs. reality on claims people make about prediction markets and what they’re good for; how do they fit in with other trends like AI, futarchy, the crisis in scientific publishing, making business decisions, and more… And then about halfway through, we also talk about desired features, and underlying technologies (including where blockchain and crypto comes in)._   

_As a reminder: None of the following should be taken as business, investment, legal, or tax advice; please see a16z.com/disclosures for more important information._

**Alex:** So I think a prediction market is a very simple idea. The bottom line is that we’re interested in forecasting — lots of people are interested in forecasting things — and prediction markets are… some of the best methods of forecasting which we have yet created.

They tend to be better than complicated statistical models… They tend to be better than polls, or at least as good. And there’s one reason for that: in making bets on the prediction market, I push the prediction market closer to the truth!

**Scott:** And actually you know, that is an illustration of why we think of these things as information aggregation mechanisms, right. What are they really doing — they’re aggregating information from all of the people in the market — so if many different people are out there doing their own private forecasts, and calibrating their own models, they all have their own estimates (which they trust with some degree of confidence); they come together, right — they’re all buying or selling the prediction asset based on what their model leads them to believe…

And so as a result, the asset is sort of like aggregating all of this information. It’s price discovery, just like we think about in financial markets and commodities markets: Like, everybody’s demand together discovers the price at which the market clears —

And here, because what the value of the asset is depends on probability, right, it’s like, its value is sort of like a function of the probability of the outcome of the event — The price aggregates people’s estimates of that probability.

**Alex:** Yah exactly; I think it’s useful that these _are_ markets, and actually _all_ markets do this.

And we learned this going back to Hayek’s 1945 article, “[The Use of Knowledge in Society](https://www.econlib.org/library/Essays/hykKnw.html)“: This is a Nobel Prize-winning paper, which doesn’t have a single equation in it. So, anybody can go and read this paper — and they should, it’s a fantastic paper.

**Sonal:** I’ll link it in the show notes.

**Scott:** Awesome.

**Alex:** And so what Hayek said, is — you know, prior to Hayek, people think what price is, they coordinate and the make demand equal supply and production, consumption — Hayek said, no no no, you’re thinking about the price system all wrong; the price system is really about aggregating and transmitting information.

And he said, look, there’s all this information sort of out there in the world. And it’s in heads, right? It’s in people’s heads, like: what people prefer, their preferences; but also people know things: They know what the substitutes are, what the complements of a thing are, how do we increase supply, what the demands and the supplies are.

It’s all in heads.

And a good economy, you wanna use that information, which is buried in people’s heads — but how do you get it out? Because it’s dispersed, it’s dispersed in millions of people’s heads, the information… Sometimes it’s fleeting information; it’s sometimes tacit, it’s hard to communicate to a central planner.

So what Hayek said is that markets do this. Because markets give people an incentive — through their buying and selling — to _reveal_ this kind of information. To pull this dispersed information for millions of people. And people who are buying, they’re pushing the price up, people who are selling, they’re pushing the price down. Suppliers, consumers, they’re all in the same market.

And so all of this dispersed information comes to be embedded in the prices… And kind of remarkably, the price can sort of know more than any person in the market.

**Sonal:** I just wanna pause on that for a quick second, because — you guys might take it for granted, but that’s a very profound insight — like what you’re basically saying is that: It’s really surfacing what people know collectively at scale and getting at the truth in that way.

I mean, that’s a very profound thing. I just wanna pause on that for a quick second.

**Alex:** Exactly.

What economists have found is that these markets are actually very good at producing predictions, which tend to be more accurate than polls. So, if you go to a prediction market — for example the election with Trump and Harris — you can buy a asset, which pays off a dollar if Trump wins; and nothing if Trump doesn’t win. So you can interpret the price as a prediction. And in the most recent election, the prediction markets were tending to predict a Trump win, even when the polls were closer to 50-50.

**Sonal:** Actually the Polymarket CEO said a lot of people “trust the market, not the polls” <Scott: oh> — at least when it came to the election; like, do you guys agree with that or no; I’m just curious — because if that’s a place where we can quickly tease some hype versus signal —

**Alex:** I don’t think polling is dead. Polling is one of the inputs <Sonal: yes!> into prediction markets, pretty useful — I do think people need to be more sophisticated about how they poll <Scott: yup>, and who, who they poll. There needs to be some new sophisticated techniques.

**Sonal:** I saw on Twitter that like landline poll response-rates in the olden days were like above 60%. But today, the response rate to like 5% — which means you’re getting like a very bad sample bias in terms of who’s willing to answer a call on a poll. <chuckles> Like I’ll hang up right away if someone tries polling me <chuckles>.

**Scott:** Yah and in particular, it’s not that prediction markets will outmode polls, it’s actually — they’re going to lead to revolutions in technology <Sonal: yes!> for doing this well.

If anything, like, the availability of prediction markets _increases_ the incentive to conduct polls. <Sonal: mmm!!> Right like, as we literally saw with the whale, they went out and ran their own poll precisely because they thought they could use it usefully in this market.

**Sonal:** That’s fantastic.

I have to ask though (so this may seem obvious to you), but the key point is that you’re putting a price on it where people are putting skin in the game essentially with their opinion or prediction, so to speak. And that seems very interesting and useful…

How is that different from betting- I mean, can prediction markets be incredibly tiny amounts that don’t have big value to be valid? Like how does the pricing part of this all work, in terms of the incentive design.

**Alex:** Well, if you think that Trump has a 70% chance of winning, and you go to the market and you see that the price of that asset is $0.55 cents, you’re gonna wanna buy!

Because you’re buying something you think is worth $0.70 cents — 70% chance that Trump wins — and you get a dollar; and you can buy it for $0.55 cents, you expect to make $0.15 cents.

And by doing that, you push the price closer to $0.70 cents.

**Scott:** The pricing works exactly as Alex described: If you think the probability that Trump is gonna win at 70%, you see the price at $0.55 cents…

If you believe your prediction, you now have you know an incentive to show up and buy. And like if enough people have beliefs of different types and they all come into the market and they all purchase, eventually the price sort of converges according to the “convex combination” of all of their different predictions.

But… when you ask about like the size of the market, or the size of a betting market — Doesn’t matter once people are there, and they’ve already formed their opinions — but it might affect their incentive to gather information.

You know, if the size of the market is capped at $1000, and you think the probability is 70%, you’re not gonna invest like $10000 to get a more precise estimate, right — like if the maximum possible upside for you is on the order of $1000, you can’t possibly invest more than that… to learn new information that will change your estimates, and thus potentially sort of like inform the information in the market even more.

In this most recent presidential election, prediction markets were very strong predictors in the trend-direction of what actually happened.

But of course, if you look at say, the 2016 election, the prediction markets totally didn’t call Trump, and they also didn’t call Brexit, which happened the preceding summer or so. <Sonal: oh yah, yah> — and like there, people were asking well, what happened; how did these miss this?

And at the time, I wrote an opinion column where I argued that this information thing was a key part of the story. That like, at least at the time, prediction markets were relatively narrow — both in terms of the total amount that could be, you know, sort of the total upside, the total amount that was enclosed in the market. And in terms of who participated in them. Right? — it was sort of, like, concentrated in a small number of locations… And those participants, because the upside was not necessarily that high, didn’t necessarily have an incentive to go out and _find out_ you know sort of like what’s going on <mm> in other parts of the country.

And so you end up aggregating information just from the people who were already there, which might not be a good estimate in that circumstance.

**Alex:** I wanna push back a little bit on what Scott said. <Scott: Go!> <Sonal: Ooh, yeah, that’s what I wanted!>

Well, so I agree you want a thick market, of course. And it helps to have people, willing to bet a lot of money, because then they’re willing to invest a lot in making their predictions accurate.

The part which I wanna push back on however, is: This idea that the market did not predict well if it predicted a 40% chance of Trump winning, and Trump actually won, right? <Scott: yah>

Because this is what people always do; it’s frustrating, right? Because… you can go back and look at individual examples and say, well did the market predict well? But that’s just like, you know, you flip a coin and it says 50% chance of coming up heads, and it came up tails. You say, “oh well, your probability theory isn’t very good, is it?” You predicted that it would have a 50% chance, and it came up 100%. <Sonal chuckles>

So what’s the real test?

Well, the real test is, you need a large sample <Scott: right> of predictions, which could be predictions from political markets, but prediction markets predict other things as well.

You need a large sample, and then you have to say: In the sample of cases in which the market predicted 40% a win of you know, the Republican or whatever, of that, how many times did the Republican actually win? And what you find is that pretty close, 40% of the time that the market predicted a win, 40% of the time, Republicans actually won (in those cases).

So in other words, there’s sort of a linear relationship that when the market predicts a high chance of winning, that happens a lot; when markets predict something with a low chance of winning, that doesn’t happen very often… But of course, sometimes it does happen, right, you know? Something that happens with only a 5% probability ought to happen one in 20 times.

And that’s exactly what you see with these prediction markets. They tend to be more accurate than other methods of forecasting. And they tend to be… not systematically biased. We can talk about there’s some odd biases, which are possible — but they tend not to be systematically biased. So it’s not the case that something which is predicted 40% of the time actually only happens 20% of the time. The markets _systematically_ get: 40% of the time, it’s predicted, 40% of the time it happens.

Let me give a simple non-market example, which I think illustrates this kind of a famous… People have heard of the wisdom of the crowds, right? And so you ask people, how much does this cow- does this cow weigh?

And people are not that good at figuring out how much a cow weighs. Some are too high, some are too low. But — if you take the median prediction of how much the cow weighs  the median prediction tends to be very, very accurate.

So in a sense, the crowd knows more than any individual predictor knows. And in the same way, markets do the same thing: They embed in the price more information than any single individual knows.

**Sonal:** Right, and just to be super precise, you’re specifically saying the median, not the mean, not the mode. It has to be like the exact middle point, literally, not averaging out from the extremes.

**Alex:** I-in that particular example, yes.

**Scott:** In that particular example — <Sonal: got it> but it varies by context.

**Sonal:** Got it.

**Alex:** Exactly.

**Scott:** Let me build on that and like illustrate it again, through a simple example, but in the language of the price system —

So, when you’re going around and polling people about the weight of a cow, you have to go around and ask them; and they don’t necessarily have a strong incentive to figure it out.

But, suppose you have a very large amount of money to invest in-in commodities, or commodities futures or something of the sort… and you have a predictive model that tells you what you think is gonna happen to these markets. Like you have reason to believe that there’s gonna be a big shortage of oil; or a surplus of orange juice, or something of the sort.

You can buy and sell in the market in a way that reflects that estimate that you have, and it pushes the price accordingly, right? So if you think there’s gonna be a big shortage of oil, you’re gonna stockpile oil today, you’re gonna buy a lot of it today, and that’s gonna push up the price. Because you know suddenly there’s more demand than there was before. And so when you see the price of oil going up, it’s like it’s a signal that somehow people think oil is more valuable right now than it was five minutes ago. (By the way, of course these are all hypotheticals, like none of this is investment advice; like, people should not go out and buy a bunch of oil, or oil futures, or whatever.)

But like, conceptually: That’s how the price reflects the information. And the more strongly you believe that there’s gonna be a shortage, the more you’re gonna be willing to pay to buy right now. <Sonal: right>

And thus the sharper the price movement even — sort of the stronger the inference about the information that that buyer brought to the market.

**Alex:** Yah.

If you wanna know whether there’s gonna be a war in the Middle East, keep an eye on the price of oil.

**Sonal:** I remember that as a child in the ‘80s.

**Scott:** And it’s still true today. That’s exactly right.

And note that the oil market is a little bit of a prediction market too, right: The oil market is revealing information about people’s beliefs about things that are correlated with the availability of oil <Sonal: yah…> — like, whether there’s a war in the Middle East.

**Sonal:** Well that actually goes perfectly to the question I was about to ask — because I still wanna dig a little bit more into the economic and market foundations, and then we can go more into <Scott: awesome> the challenges < of prediction markets and where they’re going —

But on that very note of oil — actually, a great example, Scott — the question I wanted to ask you both is: Where does this break?

Because in the oil example, one could argue like well, it’s not like a “pure” market; you have cartels, you have other forces at play… Now, you might be saying it doesn’t matter because all that matters is people’s opinions, which is what the prediction market is putting as inputs into the market.

Or doesn’t it matter? I guess my question is really getting at what are the distortions that can happen here – like there’re things that can manipulate it; or other distortions where people’s behavior changes so significantly that they untether the market from reality.

**Alex:** Yeah, sure. I mean one of the things about these markets — you know, oil predicting possibility of war in the Middle East — of course, they’re not designed to do that, right. In those cases, the information is sort of a _leakage_: It’s an unintended consequence of market behavior. Which is very useful: you know, it’s very useful for economists to be able to pull information out of these market prices.

It’s with the creation of _prediction markets_, which was — really, the first ones go back to the Iowa political prediction markets created in 1988 — it was there, almost for the first time, that a market was _created_ in order to produce information. <Sonal: Right!> So, there’s a much more direct connection between the output of the market, the prices on the market, and the predictions — because that’s what they were designed to do.

Now of course, you’re totally correct that if you want to get a market to predict the future — You’re gonna want (as Scott said earlier), to have lots of people, because you’re gonna take advantage of all the dispersed knowledge… Because there are people in Pennsylvania who have extra knowledge about what their neighbors are talking about. <Sonal: yes!> — you know that can give them a little bit of insight, right, that you might not have if you’re living in New York or San Francisco — So you want lots of people to participate;

And you want the markets to be quite thick. Because you want people to be able to want to kind of invest some time and energy — about what the predictions should be, to maybe apply some models perhaps to it, things like that —

And of course you want it to be, yeah, free and open. And you have to be a little bit worried about manipulation.

**Scott:** Yeah.

There are some funny edge cases that we’ve seen crop up occasionally — in fact there were even allegations that maybe that was going on here — where if there’s some external outcome, or even some like internal behavioral outcome, that conditions on the prediction – Right so if like political candidates are gonna decide how hard to campaign in a given state based on what the prediction for that state says? You might want to influence the price… Not for the sake of earning money in the prediction market (although that might happen too), but rather because you just want to um place the prediction in a given position.

Now, that’s very hard to do, because you actually have to change beliefs from doing that. In the uh — I think it was the Obama vs. McCain campaign? — somebody tried to sink a bunch of money to move the McCain percentage. And then, you know, people who had estimates that the Obama probability was higher, just sort of arbitraged that out over a period of an hour or two. <Sonal: Ahh… interesting!… right> Right? Like, markets work. If you see something that looks to you like a market anomaly, you buy or sell accordingly.

**Sonal:** Yes, yes. I mean, we’re all market purists here, so that seems like that’s working.

**Scott:** Yes. But, if the market is thin or if the information signals are very dispersed, maybe you can convince people, right? If you have enough money to swing the market in a very sharp way — especially if you’re doing it through Sybils (like many identities); if you’re doing it through many identities, so it looks like a surge of people who have a given belief — you might actually change the beliefs of the market participants in a way that actually distorts the probability and could have various other impacts.

And then the other thing is: This idea that the oil markets are leaking information — we’ll stick with that example, the oil markets leak information about potential conflict in the Middle East, right? — that’s like a feature and a bug, right: The fact that it’s an oil market that is informative about the Middle East, on the one hand, as Alex said; it means that the market is not optimized for specifically answering the question “what’s gonna happen in the Middle East”; there’s lots of other stuff that affects the oil market, like how popular electronic vehicles are at that given moment in time, right?

So like you have this very complicated signal extraction problem, right? You see a big spike in the oil price: Is it because there’s a potential conflict coming in the Middle East? Or is it because there’s just been some new electronic vehicle test that failed, and somebody knows that, and so they know that oil is gonna be more important next month? Whereas if you have a market that’s just predicting, will there be a conflict in the Middle East, that’s all it’s predicting.

But of course, that’s now a zero-sum market. It’s sort of a harder market to participate in if you only have dispersed information, right? If you don’t know whether there’s a conflict in the Middle East forthcoming — but know that some things that are happening sort of suggest that (for example, you saw an oil price change — You have to do a much more complicated, and you’re taking a slightly, and in some ways, riskier, bet by participating in a prediction market where you’re staking everything on this one outcome. Rather than on something that’s like heavily correlated, right? <Sonal: I see- > Where there are many different things that could have related… You know, sort of related predictions could be mostly correct even if your main prediction is wrong.

So the takeaway is: Prediction markets’ narrowness is a feature and a bug. It’s sort of dual to the sense in which ordinary markets sort of broadness is a feature and a bug. Right?

Because a prediction market is a narrow, zero-sum contract on a specific event… many people’s information about that event is actually coming from all these correlates; It’s not that they know specifically, like is there a conflict coming in the Middle East, is that they see a lot of potential signals of it.

And so if you’re buying and selling in a market that responds to those signals — that sort of insures you a little bit, right? — If you get the main estimate wrong, but all your signals were correct, you’re at less risk… than if you go into a prediction market and had all the signals right, but the final estimate wrong, and then you’re just betting on the wrong side of the event.

**Alex:** I think what Scott said also has implications for, why don’t we have prediction markets in everything?; I mean, if these markets are so great and they work so well at predicting things, you know why don’t we have more of them?

And I think Scott was basically giving the answer there. This is how I would put it:

You know if you have the market for oil, then there are lots of people who are buying and selling oil, who are not interested in what’s going on in the Middle East. Okay? <Sonal: Right> <Scott: Yes> They’re not trying to predict that, right? But it’s precisely because you have lots of sort of organic demand, and supply, that this provides a subsidy to the sharks who go in there in order to make the price more accurate.

Or take the example of you know wheat: There are lots of farmers who are buying and selling in the market for wheat — just to insure themselves, just to hedge themselves — And it’s because of that native, organic demand that the market is thick enough that you then have all of the sharks — who are not themselves farmers — but they go in there and they use models, and techniques, and whatever to predict which way the market for wheat is gonna go, and they make that market more accurate.

Now, if you didn’t have the organic demand, then you’re gonna have a market with just sharks in it <Sonal: yess!> — no farmers, and just sharks.

And who wants to be in a market where you’re only with other sharks, right? <chuckles> Right? It’s like if I know that the other guy is just trying to predict this one thing as much as I am trying to predict it, you know, I don’t wanna be in a market with Scott. He’s just too smart, right? <Scott laughs out loud> <Sonal: right!>

**Scott:** I would say the same thing about you. <all chuckle>

**Alex:** And that’s why the market wouldn’t work. <Scott: Right> That’s why the market wouldn’t work.

So, yeah, some of these markets, even though they might be forecasting something which is useful, there isn’t enough organic demand where you have to subsidize it from outside the market <Scott: Yup> in order to get a useful prediction out of it, in order to get the sharks <Sonal: Right> willing to go against one another to try and predict this thing.

**Sonal:** Right. And that’s why we don’t have markets and everything yet, potentially.

This is maybe jumping ahead a little bit, but I just have to ask at this point — I mean, Scott, you’re like a market-design expert… so on the market design front, what does that mean if there isn’t organic demand? Is there a way for market designers to essentially create markets in situations where there isn’t that kind of latent/ organic/ or existing thing to harness?

Like, can you actually “manufacture” that market — without distorting it — and kind of create conditions that could design a market into place.

**Scott:** That’s a great question. I mean, there are two different ways to get at it:

One of them is — which is sort of what the framing of the question is pointing at, is: Could you find a way to create latent demand?

And Alex is saying you could subsidize it, right? You could basically, like, somehow subsidize the experience of some people trying to predict this event, like you know subsidize a bunch of college students <Sonal: yah> developing forecasting models. So then they have a lower cost of entering the prediction market or something of the sort. Again, not advocating specific policy.

**Sonal:** Right, although in Alex’s example, that subsidy was not intentionally a subsidy, it’s just a result of the behavior — like, it wasn’t like people are trying to subsidize, it was just subsidizing because of their natural behaviors.

**Scott:** True. No, no, exactly.

So, like, we started this conversation with the recent presidential election, and all of these other associated elections — Those have proven (at least in practice), to be much thicker markets, because there are some people who seem just interested in betting on them, right; a lot of people have some amount of information, some amount of opinion.

And so there’s a little bit of that latent demand that sort of comes from people’s general interest in the question. <Sonal: yah> One could try and create that for other contexts, right? You can try and help people feel that something is interesting or feel that they have an opinion about it enough that they’re willing to participate in a prediction market.

The other thing you can do is you can use other types of information-elicitation mechanisms; prediction markets are one of many ways of doing incentivized information aggregation. And others are things like incentivized surveys, or peer prediction mechanisms.

There’s a whole class of what are called “peer prediction mechanisms”, where, what you’re in effect doing is asking people what they believe about an outcome and what they think other people will believe about an outcome. And then you use sort of their beliefs about others as a way of cross-examining whether they were telling the truth. Because you survey a lot of people, you get sort of like your crowd volume — you sort of know the aggregate belief of the population — And you can check whether someone’s own belief about the population is sort of the right mixture of that aggregate belief, and their belief.

So like, if you yourself think that Trump is more likely to win, then you yourself are more likely to believe that other people think Trump is likely to win. Because the frame you have — that your information sort of indicates that at least one more person, or at least one person in the market believes that — And so, one can cross-examine your predictions with your estimate of what the population believes; and what the population actually reveals that they believe…

And then you can reward people based on how well they did. In effect like, how good are you at estimating what everyone else thinks, given what you think?

And those sorts of mechanisms, you can incentivize:

You can pay people immediately, incidentally — unlike prediction markets where the event has to be realized, the payment’s only realized at the end — Here you’re not paying people based on their accuracy about the event; you’re paying them based on their accuracy about everyone’s _estimates_.

And so you can do that all at once, right? Collect all the estimates, pay people; they go home, you have your estimate. And these have been shown in practice to be very effective for small population, or like opinion estimates — things where there isn’t a thick market and like a very very big public source of signal.

**Sonal:** That really answers that question.

And by the way, it brings up a very important point that we did not address in the example of the election — Which is the French quote-“whale” who won by using the neighbor poll. Where, like your neighbors won’t say what they think, but when you ask them, like, who do you think your neighbors are gonna vote for? — It’s kind of a way to indirectly reveal their own preferences.

And that’s the so-called neighbor poll; I don’t know if that’s a standard thing or that just came up in this election (it’s the first time I heard of it), but — It’s a great example of something I did study in grad school when I was doing ethnography work, which is: Never trust what people say they’re gonna do, but what they actually do. <Scott: mhm> — This goes to your economists’ world <Alex: yah> of revealed preferences. <Scott: Absolutely> Right, very similar.

But anyway, in that case, that person polled his neighbors and then used that data essentially – off-chain — to then go back \*on\* to the market to up his bet. And essentially won big as a result. So like, that would be an example of what you were mentioning. Although in that context, you were mentioning it in how can we address a case where there’s a _thin_ market? This is a case where that played out in a thick market of the election.

**Scott:** Well, you might say that he was using this in the thin market of trying to understand his neighbors’ sort of like local preferences and estimates. Right?

**Sonal:** There you go, that’s more precise, yeah.

**Scott:** Although we actually don’t know the details of how he produced these estimates. It doesn’t sound like they were incentivized. So it’s not exactly like what I was talking about with peer prediction.

But, you’re right, it’s the same core idea that like, using people’s beliefs about the distribution can be much more effective than using their personal beliefs a lot of the time.

**Alex:** So I would uh underline two things there –

One, yeah the market is a way of bringing all of this dispersed information <Scott: yes> and creating an aggregation. But it’s not the only way. <Scott: correct> That’s kind of what Scott is saying, right?

And understanding, this is one of the first information aggregation mechanisms which we have studied and understood reasonably well. But, there are other ones. And…

So you can think about prediction markets as being one example of a class of mechanisms, which take dispersed information, and out of that, pull some knowledge which none of the people in the market — or that none of the people you polled — none of them might be aware of it. And yet somehow it is in the air, as it were.

**Sonal:** That’s fantastic.

**Alex:** There are also other ways of subsidizing these markets <Scott: yup> — which is something that corporations may be very interested in doing <Scott: yes><Sonal: mhm!>… Because corporations are interested in forecasting the future. And, some of them in the past have created their own internal prediction markets. <Scott: yup>

So, one famous example of this [is Hewlett Packard](https://wayback.archive-it.org/5456/20240920155724/https:/www.eecs.harvard.edu/cs286r/courses/fall12/papers/ms020408.pdf): They were interested in forecasting, how many printers are gonna be sold in the next quarter, in the next two quarters, three quarters, four quarters, and so forth. So they created a market where, if you correctly predicted how many printers would be sold, in which time period, you could earn money. And they subsidized that market: So everybody going in (which is just HP employees), got like a $100 to play with <Scott: mhm>.

So that’s a way of trying to get more people involved and interested in playing on these markets, to elicit this information.

**Sonal:** That example is actually really interesting to me ‘cause when I was at Xerox PARC, we talked about that. And one of the things that came up is — it’s a very useful mechanism, to your point Alex, for getting certain things right <Scott: yah> —

But it is not a useful mechanism for actually figuring out the future in terms of what to invent. Because it doesn’t address a case of “you don’t know what you don’t know”. <Scott: yah> You only know what you know.

And this came up when Trump announced his candidate for attorney general — And one of the examples (someone cited on Twitter) was, it’s the first time they’ve seen a contract resolve to zero for all potential outcomes — because Gaetz wasn’t even listed among the 12 potential nominees, in those range of possible outcomes.

So, that’s an example in that case where you have to have the right information _itself_ in that prediction market. <Scott: yah> And you maybe you guys can explain that a little bit more too really quickly, because I think that that HP example is super interesting — on multiple levels. <Scott: Yah>

**Alex:** Yah… so these markets are good at when you figure people have got some knowledge and it’s hard to aggregate that knowledge. The other thing they’re good at, you know, the people have run these markets for predicting when a project will be complete, right? <Scott: mhm, right> And this is a classic case. <Sonal: yahh> When you ask people, they’re gonna be oh well no problem, it’ll be ready, you know, in five weeks, whatever, right; they’re very optimistic. And yet they tell the boss it’s gonna be ready in five weeks. <Sonal: yahhh> While they go back and tell their friends, oh my god it’s delayed, you’ve got all these problems. But if you let people bid anonymously in these uh markets, then the truth comes out.

So this is a way of the corporate leaders, can learn information that their employees know, but are not willing to tell them. Right? But… to your larger point: Yah, I mean; nothing is more difficult to predict in the future <laughs> right. <Sonal: right right><chuckles>

And, you know, Trump is a chaos agent, hard to predict.

**Scott:** Well, and indeed actually, so this sort of highlights… You know, we were talking about what prediction markets are good at versus where you might wanna use other sorts of information-elicitation mechanisms. <Sonal: yup>

The two examples that Alex gave of within company prediction markets — You know, predicting sales, your sales growth, or something that’s like, you know — a metric that many people in the firm are tracking, and have different windows of information into. Predicting when a product is going to launch, where like, you know, you might have product managers who know something, you might have engineers who know there’s a hidden bug that they haven’t even told the product managers about yet.

Again, it’s like, these are contexts where many of the people in the company have some information that only they have — and that the aggregate of all that information is a pretty good prediction of the truth. Because, the actual outcome is the aggregate of all those people’s information directly, right: It’s like, how many sales calls are you making that are succeeding? Or, you know, how is the coding for this specific feature going?

By contrast, you mentioned with Xerox PARC — you know, trying to predict whether a new sort of totally imagined product is gonna succeed, well, that’s really, really hard. And it doesn’t rely on information in particular that the company has. Right like yes, the company has some idea of what products people might buy, but you might be like, you know, AT&T and invent the first picture phone or something of the sort. And you thought that was a great idea… but you don’t actually know until you put in the market and see whether people are like, you know, interested in using it.

And so the aggregate of all the information in the company — there there’s a product they went through with, right, they concluded was a good idea based on all the signal that everyone in the company could see and it still flopped; — The total information in the company wasn’t high enough to actually, like, provide the right answer even when aggregated.

**Sonal:** Right.

**Scott:** But I do think there is a subtle distinction between wisdom of a random crowd and wisdom of an informed crowd. Right? Again, with our Hewlett-Packard example, Hewlett-Packard sort of knows that if you’re trying to figure out now whether a product’s going to launch on time, a random person on the street has no information about this. You don’t want to like pull together a focus group of miscellaneous Hewlett-Packard customers and ask them, when do you think we’re going to finish designing our new printers, right, they’ll go, “I don’t know. You’ve released a printer last year, probably next year, maybe. Who knows?”

And so, there is this question: Are you learning things from the right crowd?

You know, you could have the best incentivized information-elicitation mechanism on the planet. And if you only survey people who don’t know anything at all about the topic, you’ll incentivize them; you’ll learn what they believe truthfully — but you won’t be able to do anything with it.

**Sonal:** Yeah…

And then back to the future, like, the whole idea of “the best way to (you know) predict the future is to invent it”. <Scott: Right> Like, that goes to just like the Jobs and, the phone, like, no one… You can ask a million people, will they ever use a touch phone. People’s behaviors can also evolve and change in ways that they themselves are not aware of, <Scott: absolutely> which is that other side of that example.

**Alex:** Yah. Prediction markets — it’s like a candle in a dark room, right — I mean, it helps us see a little bit, but there’s still areas which you can’t see very far.

**Sonal:** Great.

I’m gonna ask a couple of quick follow-up questions from you guys so far. <Scott: Go for it>

So just to be super clear: So “thin” versus “thick”, you guys are talking about the depth of the market, like in terms of the number of participants: Thin is too few, thick is many. Is that correct, or is there a better, more precise way of defining that?

**Alex:** Yeah so, I mean in the prediction market, a “thin market” is few people betting small amounts.

We’re slowly changing, but we do have this kind of ridiculous situation (I think it’s ridiculous, anyway), that we have <chuckles> huge markets in sports betting, <Scott: right> gambling, right? Huge, huge markets. And we allow that.

And yet here we have… a kind of gambling market, a prediction market — where the output is actually really quite useful. It’s quite socially valuable. So, making these markets legal and open to more U.S. citizens would “thicken” those markets, make them more accurate, attract more dispersed information. And I think would be really quite useful.

**Sonal:** But to your bigger point Alex, you’re basically arguing that they can be a public good in the right context, informationally.

**Alex:** Absolutely.

**Sonal:** And, interestingly, in some cases, people might argue trying to get information is a manipulation of the market… But in fact, to your guys’ entire point throughout this discussion, it’s actually ways to provide more input of information into the market itself, too. <Alex: Absolutely>

So that’s kind of an interesting point on the public-interest side. <Scott: yes>

**Alex:** Let me give you another example on this public-good nature of these prediction markets — One of the most interesting, fascinating uses of these prediction markets is to predict which scientific papers will replicate. <Scott: oh yeh> <Sonal: ah, right, yah>

You know, we have this big replication crisis, in the sciences, (psychology, and other fields as well), of, you know, lots of research and it doesn’t replicate. Well, what some people have done is — it’s expensive to replicate a paper, but one thing people have done — is to have a betting market, a prediction market, in which papers will replicate.

And, that turns out to be very accurate; and then you only have to replicate a few of those papers <Sonal: right> in order to have the markets pay off. And for the rest of them, you use the prediction market result — as a pretty good estimate of whether it will replicate or not.

So this is a way of improving science; making science better and quicker and more accurate.

**Sonal:** I love that. I ran a lot of op-eds when I was at Wired on open access and science, and kind of like evolving, you know, peer review, and replication crisis, and the whole category and theme. So it’s very exciting to me to hear <Scott: yah> that that’s something that we can do to address that.

It leads to a quick follow-up question — which actually happens to be on my list of follow-up questions for you in the lightning-round of this — Which is: when you guys were talking earlier about this, just like kind of, tapping into this intuition, information dispersed across many people into these prediction markets —

One of the first questions that came to mind is, do you need domain experts, or does that actually distort a market? And this actually comes up as a perfect segue from your point, Alex, <Alex: mm> that example of scientific papers — Because that’s a case where one would imagine that people in that industry, or that domain, or just other scientists who have the experience of analyzing research would be the best at predicting things.

But is that necessarily true? <Alex: yup> And do we have any research or data into domain expertise in these markets?

**Scott:** I don’t know the answer to that last part, let me talk about the first part, because it also speaks to your thick versus thin. < Sonal: Great, yeah, good good> So when Alex said a thin market is small number of participants betting small dollar amounts. Why is that a thin market?

It’s because the total information, is small in two ways: One is that there are a few people bringing their own individual estimates (just have like a small number of people saying things). And second, because they’re betting small dollar amounts, it’s sort of a signal that their information is not very strong signal or confident — at least relative to what it could be otherwise.

You know, if you are staking a very large amount of money on this, the market inference is that you have done the research; you know and indeed you have the incentive to do the research — You know, why is the inference that you’ve done the research; is because if you’re staking a large amount of money, you should have done the research. <Sonal: yah> Because otherwise, you know, you’re putting money at risk without sort of full information.

And so, like, thickness and thinness, like the proxy for it — the way we think about measuring it is — how many people, and how much are they staking? Like, how much value are they putting behind their beliefs?

Thickness and thinness is really in terms of the information: It’s like, do we have a lot of different signals of information that are strong, coming together, and mixing to determine the price? Or is it really just like a very small number of pretty uninformed signals?

That’s this tension — when Alex is saying it’s a problem that the biggest prediction market for the U.S. election was not actually in the U.S. and was not legal to participate in the U.S. — well, yeah! A lot of the information, a lot of the like real signal is in the United States. And so, without those people being able to participate in the market, you miss at least sort of a lot of that to a first order. Right, people internationally will be figuring out ways to aggregate and sort and try and use it. But like, you miss a lot of the people who have that information already at their fingertips.

And so you ask about domain expertise… It’s not exactly domain expertise versus not, but rather _information_ _richness_.

And for example, in predicting scientific replication success or failure, domain experts are especially well equipped to do that. Right? Like, a random person chosen off the street, you know, you can tell them a scientific study; and maybe they’ll have an instinct one way or another, whether they think they believe it. But like a lot of the detail of figuring out whether something will replicate — comes from knowing how to read the statistical analysis, trying to understand the setup of the experiment, and like, the surrounding literature — and so there domain experts have a particularly large amount of information.

If you think about something like a political betting market: Maybe domain experts who are focused in the world of politics and polls and so forth, have like a big slice of information; they do. But there also might be other categories of people: Like, people who know that their neighborhood has like recently switched its political affiliation in a way that isn’t yet captured in the national polls. Or, our French whale who went and ran his own sort of poll using a custom chosen method.

And so, the _context_ of the question the prediction market is trying to evaluate — and this is actually true for any informational elicitation problem; this isn’t just about prediction markets, right? — the context of the type of information you’re trying to learn tells you something about who has the most information to bring to the market, and thus who it’s important to have there.

**Alex:** Yeah, I agree with everything Scott said. One of the interesting things is, you often don’t know who the domain expert is, <Scott: yes!!> right? Until after the market has been run.

So of course it’s absolutely true that, you know, if you’re gonna be predicting political events, you want people who are interested in politics. If you’re predicting scientific articles, people need to be able to read stats and things like that. But: One of the guys in the [scientific replication paper](https://www.pnas.org/doi/full/10.1073/pnas.1516179112) on markets, he made like $10000 — was just one of these super obsessive guys, right? — who just really got into it and, you know, was running all kinds of regressions and was doing all kinds of things and stuff like that.

And so when you say “domain expert”, I think one of the virtues <Scott: yes> of these prediction markets is that they’re open to everyone… And they don’t try and say, oh no, only you guys get to say…only the experts, <Sonal: yes, exactly> you know, get to have a voice, right? It’s more only ex-post do we learn, hey, who really made some money in these markets? <Scott: Absolutely>

**Sonal:** I am so glad I asked you guys about the definition of thick versus thin — because you guys gave me so much interesting nuance too. Because people I think following this podcast definitely understood what you meant about thin versus thick early on. But you guys just took it to a new level.

**Alex:** If you’re so smart, why aren’t you rich? Hey, I am rich! <chuckles> <Sonal: Yes, exactly> I made some money in this market.

**Scott:** And that, again…that’s about the incentives. We talk about like the dollar value staked, Like, the amount of money someone is staking on their prediction. Again, in equilibrium, it should be a measure of their confidence: how confident they are in their own beliefs and how much effort they’ve put in to learn the information to be precise.

And so, exactly as Alex says, one person who might be really good at predicting, a scientific replication failure is someone who works in that exact same area. Another one, it might be someone who just enjoys doing this for fun, and like, has never had a real incentive to triple down on doing it… but now suddenly they can.

**Sonal:** Right, right. And by the way, Scott, does it have to be dollar and price incentives? I’m asking you this question specifically <Scott: yes> because you and I have done a lot of pieces in the past on reputation systems. <Scott: absolutely> And I almost wonder if the skin in the game can just be karma points and not even any money. Because when I think from a pride perspective…

**Scott:** One hundred percent.

So Alex mentioned subsidy, right? Like, one way that you can subsidize — I think you said Hewlett Packard subsidized by giving all their employees $100 and saying “spend it all on this market”. You can subsidize people with cash… but you can also subsidize them with tokens or; you know, reputation; or like, sort of various other sources of value.

And one of the advantages of using tokens is that that way you can deliver a subsidy that’s sort of only useful in this market, right — You know, if it’s like a personal non-transferable token, but I give you a bucket of them… And the only thing you can do with it is use it to enter predictions, and you just choose which prediction markets you choose to enter into, and how much you spend in each one. Right?

And then you earn payoffs, payoffs are also measured in tokens; and maybe downstream, you might get prizes for having large numbers of tokens or something — you get to join the elite predictor force, or even just serves as a measurement of your reputation, how good you are at making predictions. Which maybe you leverage into something else, right? Like, people who win data science contests leverage that into data science jobs; maybe you leverage this into a forecasting job or something.

All of that — so long as you find people who are willing to be incentivized by those types of outcomes — you can subsidize their participation in a unit that locks them into the market, right; that their one thing to do with it is to participate in the market. And reinforces more and more participation among the people who are most successful and most engaged.

**Sonal:** That’s super interesting — and I’m gonna push back on you on that actually ‘cause I actually wonder if it necessarily needs to be crypto based, and you can just do any kind of-

**Scott:** Oh yeah, no, it’s any like internal marker — <Sonal: yah> but for all the reasons we normally know. Like, it’s much better to do this in an open protocol form, because for example, if the token is eventually gonna be leveraged for reputation, you want anyone to be able to verify that you have it.

**Sonal:** Right, audit it, see it; hence blockchains.

Got it, great. And we’ll talk a little bit more about that — just more lightning questions. <Scott: Yup. Go for it>

So where do super forecasters like Philip Tetlock’s work come into all of this — like, are they especially good at prediction markets? Because that’s a case where they’re like generally better at the general public in sort of quote-“forecasting” and making predictions. Is there a place for them in this world? Or are they kind of the outliers here? Or does it not even matter here.

**Alex:** I think there’s two things —

One, I think the basic lesson of Tetlock’s work is: Most people, even the ones who are in the forecasting business are terrible forecasters. Right? <Sonal: mhm…><Scott: yes> I mean, he first started tracking so-called political experts and seeing what their forecasts were you know 10 years later, were they right? Maybe five years later. And they were completely wrong.

So, he then shifted into looking for, is anybody ever right — are there super forecasters? And yes, he found that some people — you know, not typically the ones in the public eye, but some people — can definitely forecast better than others.

One of the things those people can do is then participate in these markets. <Sonal: mmm!> <Scott: yup> And by their participation, they push the market price closer to _their_ predicted probabilities.

So, forecasters have an incentive to be in these markets. And by being in these markets, they make the markets more accurate.

Now, is the market always gonna be more accurate than the super-forecaster? No. There are gonna be some super forecasters. But they’re hard to find. They’re rare. And, a virtue of the price is that everyone can see it, right? <Scott: yes> It’s public.

**Sonal:** So this actually gets at a bigger, maybe more obvious point to you guys — but a recurring theme I’m hearing, is: It’s not that the prediction market is only taking in like, guesses, and people’s intuitions, and bets, and opinions, and any information it has…

But theoretically, done well, it’s taking in _all_ information: It could be superforecasters contributing to it. It could be people who are pollsters putting their data and predictions… Basically, it doesn’t even matter how people get at their intuition. All that matters is that they’re pricing that information into that market, essentially.

**Alex:** Do you know the Wall Street Bets has a famous “everything is priced in” [post](https://www.reddit.com/r/wallstreetbets/comments/eberem/everything_is_priced_in/)?

**Sonal:** No, I don’t, actually. Tell me.

**Scott:** I don’t know this one either.

**Alex:** <chuckles> Let me read it just a little bit. It’s a fantastic post. It’s like five years ago – It’s called “Everyone Is Priced In.” And it says:

“The answer is yes, it’s priced in. Think Amazon will beat the next earning? That’s already been priced in. You work at the drive-through for Mickey D’s and found out that the burgers are made of human meat? That’s priced in. You think insiders don’t already know that? The market is an all-powerful, all-encompassing being that knows the very inner workings of your subconscious. Your very existence was priced in decades ago when the market was valuing Standard Oil’s expected future earnings based on population growth.”

<Scott laughs> <all laugh>

**Sonal:** That is so great! Okay, you have to send me that link, Alex, and then I’ll put it in the show notes.

So you’re basically agreeing that it’s the market’s do price everything in.

**Alex:** I mean, that’s an exaggeration. But yeah, I mean, anything is fair game.

**Scott:** I wanna push back but refine here, because — anything is fair game – but, you have to wonder who’s gonna show up to those markets, and where their signals are coming from.

Right, like, if you’re a super forecaster, maybe you work for like a super secretive hedge fund <Alex: mhm> And the last thing you wanna do is directly leak what it is you believe. <Sonal: yah yah> And in fact, you would prefer that the market be confused by this public signal — We talked about manipulation — You might show up and tank the prediction in one direction or the other, just to take advantage of that in the financial market off to the side.

And so, while in principle, these things can be very comprehensive… you still have to think about who participates in which market where. And just like we see in other markets, where like some people trade in dark pool, some people trade in public exchanges. And that selection sort of affects what information price is really aggregating where.

**Sonal:** That’s fantastic, yeah.

**Scott:** The other thing about public forecasters — super or otherwise — is: that they’re very salient to the average person. And so, another thing we see in prediction markets is herd behavior — again, just like we see in other types of markets.

Like, you know, if a lot of people are suddenly buying oil futures, does that mean that they all have knowledge that there’s gonna be a conflict in the Middle East? Or, does it mean they saw other people buying oil futures and are like, oh gosh, like, I’d better do this too? Or, you know, did they see one analyst report and they all saw the same analyst report — and as a result, they all went and bought oil futures, because they believed the report?

Or worse: Did they see one analyst report — that said, you know, like, oil’s gonna be expensive next quarter — and they went and bought oil futures, not because they believe the report (maybe they even have information that it’s not true) — but they know everyone else is going to see the report. And so there will be purchasing pressure. <Sonal: Yes!>

There’s this very famous paper by Morris & Shin in the “American Economic Review,” called “[Social Value of Public Information](https://people.duke.edu/~qc2/BA532/2002%20AER%20Morris%20and%20Shin.pdf).” — <Sonal: Okay, I’m gonna put that on the show notes> — It talks about information herding;

The idea is basically, if you have a market where everyone has private signals and then there are some very salient public signals — and people have to coordinate, right? Like you know, are you gonna run on a bank or not? Or like, what do you think is the probability of this thing happening –

People might ignore their private signals if the public signal is strong enough that they think other people are going to follow it. <Sonal: Yes!> And so, when a very prominent forecaster makes a prediction — like, as the sort of polls were coming in in the week leading up to the election, a new major poll would drop — and then the prediction markets would judder around and sort of veer off at least briefly in the direction of that poll…

And that’s this like public-information effect, right: This is salient, you expect a lot of market movement based on this information. And so the market actually moves even more — It incorporates not just the information, but also the fact that other people are incorporating the information too.

**Sonal:** And are there any market design implications for how to avoid that happening? Like if you’re “setting up” the conditions of a perfect, great, prediction market?

**Scott:** Oh, gosh, that’s a great question.

I mean, first of all, it’s not completely avoidable; You can’t have a market where a sufficiently strong public signal doesn’t generate some herd behavior – right, just at that level, it’s unavoidable. But you can try and do things to dampen the effect… Off the top of my head I can think of two; there are probably others.

One is you could basically, like, slow trade in a little bit, right? You would sort of like limit people’s abilities to enter or exit positions very, very quickly. So it sort of forces people to like average.

**Sonal:** Well, it’s also kind of an example of slowing contagion, right? <Scott: Yes> <Alex: yes> Of like, an infection spreading very fast. Kind of like the herding becoming viral.

**Alex:** Yeah, contagion is a very good example of what Scott’s talking about. You know, in stock markets, we have-

**Scott:** Circuit breakers.

**Alex:** Circuit breakers! Circuit breakers.

**Sonal:** Yes, yes, yes, exactly, circuit breakers; there we go.

So that’s one of the ways —

**Scott:** — Another thing you could do is try and refine your market contracts in a way that orthogonalizes — by which I mean it sort of _extracts_ out the signal that is independent of that signal. Right? So a prediction market contract somehow incorporates the information — sort of like, adjusted for whatever Nate Silver claims…

**Alex:** Let me give you an example. Because my colleague, Robin Hanson, who is one of the founders of uh [prediction markets](https://mason.gmu.edu/~rhanson/ideafutures.html) <Scott: perfect!> –… Robin is usually many steps ahead — He has a very clever [proposal](https://www.overcomingbias.com/p/if-i-had-a-millhtml) for this, which I don’t think anyone has ever implemented: But he says you have a prediction market, and then you have a second prediction market on whether that prediction market will revert in the future. Or something else… <chuckles>

**Sonal:** Yes. Oh, it’s so genius… yes!

**Scott:** Yes, exactly, that’s the way you do it. That’s the way you orthogonalize. Perfect…way better than my example.

**Sonal:** But that’s so great! Because I was actually gonna guess something like combining the reputation thing <Scott: mhm> And this is essentially a way of combining reputation by having a parallel market that verifies and validates… <Scott: Exactly, totally> … That’s so interesting.

By the way, that’s not “futarchy”, right? His new thing?

**Alex:** One of the criticisms of futarchy was precisely the point that Scott made. And then Robin’s response to that is, well, the solution to a problem of futarchy is more futarchy!

**Sonal:** Ahh, okay. And by the way, just quickly define futarchy for me?

**Alex:** Yeah. So [Robin Hanson’s idea is](https://mason.gmu.edu/~rhanson/futarchy.html), let’s take these decision markets and apply them to government. Let’s create a _new_ form of government — you know, there aren’t many new forms of government in the world; you have democracy, monarchy — you know, futarchy is… a new form of government.

And the way it would work is that: Instead of having politicians decide what policies to have, politicians and voters would just decide on what our metric for success is gonna be.

So it might be something like GDP would be one metric of success — but you might wanna adjust it for inequality, or for environmental issues; so you’re gonna create some net statistic, “GDP+”. Then anytime you have a question, should we pass this healthcare policy? How should we change immigration rules? Should we have this new immigration rule? You have a market on whether GDP+ would go up or down if we pass this new law. And then you just choose which one… If GDP plus goes up, you say, okay, we’re gonna do that.

And so people would just submit new ideas to the futarchy: Here’s a proposal for immigration; here’s a proposal for healthcare; here’s one for science policy. And then you just run a prediction market. Would GDP+ go up with that or would it go down? And then you choose whichever comes out.

So Robin expands… this idea of decision markets, to an entirely new form of government.

**Sonal:** Thank you for explaining that, Alex, because I’ve actually never fully gotten what futarchy is; People toss it around and I’m like, but actually, what is it? I still don’t get it. <Alex chuckles> So that was very helpful.

**Scott:** It also sounds like it could be the subject of like a Borges short story or something.

**Sonal:** Oh my god, yes yes, absolutely. Oh gosh… what was the last one that we put in the last reading list Scott, for the Founder Summit? Was it the “Labyrinth” short story collection?

**Scott:** I think it was “Labyrinths,” right?

**Sonal:** Yeah, yeah, I think so. Oh that’s so funny.

So a few more questions and then I wanna switch to the crypto;

So since we’re talking actually about like kind of market theories in practice in this recent segment, Alex, did you wanna say a little bit more about efficient markets —

**Alex:** Sure, sure.

So another fascinating example of how markets could leak information, which then could be used for other things, is… If you ever seen the movie “Trading Places,” you probably know that the main determinant of orange juice futures is what the weather is gonna be in Florida. <Sonal: Of course!>

So Richard Roll, who was a finance economist, had this interesting [question](https://www.anderson.ucla.edu/documents/areas/fac/finance/1984-6.pdf), well, can we use orange juice futures to predict the weather? And what he found is that there was information in those market prices, which could be used to improve weather forecasts in Florida.

Kind of an amazing example — because no one, again, knew this; no one was even predicting this, but this was kind of a leakage of this amazing information.

**Sonal:** Fantastic.

**Alex:** Another fascinating one is, you know, Richard Feynman famously demonstrated that it was the O-rings which were responsible for the Challenger disaster — by dipping the O-ring in the ice water… at the Congressional committee, <Sonal: oh yah>

However, economists went back, and when they looked at the prices of the firms which were supplying inputs into NASA, and to the Challenger: They found that the stock price of Morton Thiokol (which was the firm which produced the O-rings), that dropped much more quickly, and a much larger amount, than any of the other firms. <Scott: mm> So the stock market had already predicted and factored in that it was probably the O-rings, which were the cause of the Challenger disaster, even before Richard Feynman had figured this out.

**Sonal:** And by the way, it’s another- that ties back to your HP example in a way –

Because if I recall, part of the backstory with the Challenger was also that it was a case of death by PowerPoint? <Alex: yes> Because of the way they were communicating information internally, and that the format and the structure kind of constrained how that information was presented. I think Tufte gives a famous [case study](https://www.edwardtufte.com/notebook/powerpoint-does-rocket-science-and-better-techniques-for-technical-reports/) of this in one of his many books.

**Alex:** So another way of putting that actually, which is kind of disturbing — but I think you’re right — in that the people on the ground, they knew this wasn’t a good idea. <Sonal: Exactly> They knew it was not a good idea to launch the Challenger on such a cold day.

And if there had been a prediction market of like, <Sonal: Yes. exactly> what’s going to happen or should we do this? Then I think it is quite likely that that dispersed information — which no one was willing to tell their bosses, you know, no one was willing to stand up and say, we should not do this; instead, it got buried in PowerPoints — that dispersed information might have found its way to the top <Sonal: Right> if there had been a prediction market in, is this launch going to go well?

**Sonal:** Exactly. Or said another way, to earlier definition of a prediction market: It would have been another way for management to “elicit” better information from their employees, <Alex: exactly> and using just that as a mechanism <Yup> <Exactly> for communication, essentially.

Exactly. Yeah, the HP thing really kind of struck me because I just remembered that it’s like a communication no-no for how information is presented.

## Features of crypto that help prediction markets

And that’s actually a good segue, by the way, to the crypto section <Scott: ooh>, because I want to ask you guys, and this is going to help me break some — You know, I love doing a good taxonomy of definitions on any podcast –

Because one of the things we talk about in crypto is the ethos of “decentralization”… Sometimes the information is “public” in a public blockchain… It’s often “open source”, “distributed”… It can be “real-time”…  I don’t know if it’s necessarily “accurate” information, but the information can be corrected very quickly, which then makes it more likely to be accurate — because of the speed of revision, which by the way, we also saw in the recent election I think, compared to media: One of the observations people made is that media didn’t move fast enough to (or even want to because of biases), their polls and predictions, whereas the prediction markets were faster “self-correcting”.

So, one question I have for you guys to kick off this section about the underlying technology and how it works is, first, let’s tease apart all those words. I just gave you a big buzzword/ bingo soup of words — What are the words that actually matter when it comes to this context of eliciting better information and aggregating that information in a market? Like, what is the key qualities that we should start with? And then we can talk about the technologies underlying that.

**Alex:** The question is, is crypto a necessary part of this? And I think the answer is probably no…

I think, why was the crypto market particularly successful? Well, because it was open to anybody in the world, barring U.S. citizens, right? <Sonal: Yes.> And the market, because of that, was much thicker than the other markets.

But I think the crypto part of it was not actually necessary.

**Sonal:** Yeah. I’m glad you pointed that out too, Alex, because I don’t know if crypto was at the heart of the way that-that market works, except in those qualities you mentioned. Scott, any thoughts on that point?

**Scott:** So I totally agree with all of that.

One thing that crypto does very well on top of being open, and interoperable, and transparent is: It enables “commitment”. Right you can write a piece of software that is going to run in the exact specified way. It can be audited by all of the users, and then they can be convinced that it’s going to run correctly.

And, some ways we do information-elicitation have challenges with commitment:

If you’re going to survey people, and pay them six months from now based on whether their survey estimate was accurate or not, they might be worried that you’re not going to show up and pay them.

And, so long as whatever sort of the information is can also exist on chain, right — the resolution, the uncertainty can somehow be visible on chain, either through an oracle; or if it were like an onchain function to begin with, like, just what is the price of this asset or something — you can _commit_ in a way that you can’t necessarily (or you can’t do easily without complicated contracts) <Sonal: yup> — You can just commit that it’s going to run as expected.

Now, in order for that to work, your information-elicitation mechanism has to be fairly robustly committed, and often also decentralized.

In the same way that blockchains create a form of property right — that you can trust even without sort of a very trustworthy entity having established it (because you know the property right itself lives in this immutable ledger) — Same thing here: Like you can, at least in principle, set up resolution contracts that are trustable, and immutable…

And therefore expand the scope of the set of marketplaces we can configure, right? <Sonal: yah> You know, right, it’s not just the set of tools we had when you have to be able to trust the market organizer — but actually now, this sort of like you know commitment enables you to go further.

**Sonal:** Just to break this down a little bit more — because I think you said some really important things in there, and I want to pause and make sure we flesh it out for our audience–

So first of all, based on what Alex said earlier, one of the key points was \*public\*, and the information being out there. <Scott: yes> That’s one.

I mentioned earlier, the example of it being \*updated quickly\* <Scott: yup> as compared to media, at least. You just mentioned the importance of \*credible commitments\*. And we’ve often described blockchains as a technology that blockchains are computers that make commitments. So that’s a third or fourth. (I don’t know the number count, but I’ll just keep listing the features…)

And then you also mentioned potentially \*decentralized\*, but I couldn’t tell if it really needed to be decentralized or not. Can you give me more bottom-line on decentralization, where you stand there.

**Scott:** Yah, it’s a great question. And actually, maybe we should have started here:

The necessity of all of these different features moves around with the type of market.

The more complicated your information-elicitation mechanism is <Sonal: yah> — And this is especially important for the context where pure information markets don’t work — the more complicated your information-elicitation mechanism is, the more likely it is that you want something that looks like crypto rails.

**Sonal:** Ahh. That’s actually good to know! Okay.

**Scott:** So like, if Hewlett Packard is running an internal prediction market — First of all, it doesn’t have to be open to the entire world because you’re only trying to learn information from your employees, right? Hewlett Packard does not necessarily care what a person on the street thinks about printer sales; and certainly doesn’t need to build the architecture to bring in, like, random people’s estimates of printer sales, right.

And so you know, you need some amount of “transparency”… because you need people to be able to see what the current price is, and like, see whether they agree or disagree. And they can sort of move the price around.

But in other types of elicitation mechanisms, maybe you don’t need transparency, right — If you’re just going to pay someone based on the accuracy of their forecast down the line, you don’t need them to be able to see what else is happening; you just need them to believe that you have committed, and that the final accuracy is going to be transparent. <Sonal: right!> That they can verify that you didn’t just stiff them by like, the thing they predicted happened exactly. But then you said, no it didn’t! And then you don’t pay them.

And so transparency is important only there with respect to the resolution, not with respect to the interim states. <Sonal: yes, yes> But by contrast, like, _commitment_ is incredibly essential — and needs to be believed or else the user won’t even participate.

**Sonal:** Right. By the way, great that you gave the example of the transparency — And I’ll let you finish your example in a second <Scott: Sure> — But I’m just jumping in because it reminds me of how we talk about the things that can be done onchain and off chain when it comes to scaling blockchains. <Scott: yah> And provers versus verifiers when it comes to zero knowledge or whatnot…

And it’s really interesting you pointed that out because I want to make sure people who are listening who are builders listen to that, because that means you can do certain things onchain in order to…whatever your goals <Scott: yes> of the design are and then put other things off chain. Like, you don’t have to have this purist view of how truth must be transparent. It’s very smart to point that out. Anyway, keep going with your other examples.

**Scott:** Yeah. And I completely agree, by the way. I mean like one of the things, when I talk to teams, I’m constantly trying to get them to think about: which features of the marketplace are the most essential for market function.

And it varies by market context. And even if eventually you’re planning having all of these features. <Sonal: yah> Right? Like, as you’re deciding, like, which thing do we build first or, like, as we’re progressively decentralizing — like, what do we prioritize? You actually have to understand the market context you’re working in.

**Sonal:** That’s so smart because it’s basically another way to hit product-market fit too, <Scott: Exactly> because then you’re not, like, overbuilding and overfeaturing something. Anyway, yeah. But keep going with your other side of that.

**Scott:** Totally, 100%.

So to get the question of like, when does decentralization matter? Decentralization has lots of different components that might make it matter:

One of them is just the ability to, like, make these commitments even more enforceable — like, it makes it possible to be confident, and function, and liveness, and so forth. All of those things are important for a market, because if your prediction market goes down the night before the election, you know, first of all, you lose the information signal from it.

Second of all, you lose the ability for people to participate in the market, which would sort of adjust the price and move the signal around. Similarly, if lose the ability to resolve the truth, then maybe you can’t finally resolve the market. And you have all of these bets that are sitting in limbo because the market doesn’t know what happened… The key is, everyone is bringing in their own information. But in order to finally resolve the contract and determine who gets the payout for the bet, <Sonal: yess!> you have to have the chain have a way to know what actually happened.

Another place decentralization is sometimes very important is in that resolution function. Like, you know, if the market is onchain, you somehow have to get what actually happened onto the chain. And, you know, maybe the biggest bettor happens to also control the one resolution function. And so, they can now sort of rob the prediction market by just lying about the resolution of the event: They tell the system, like, you know, candidate A won when actually candidate B won. And then by the time people realize that this wasn’t correct, they might not have a way to fix it; but even if so, that person might just be gone.

So decentralization and resolution — just like we think about decentralized oracle sort of mechanisms; this is basically an oracle, right, you have to bring off-chain information onchain in a lot of these contexts to resolve the contract — Or, if you’re doing this in a centralized platform, the users have to trust the centralized platform to resolve the contract correctly.

By contrast, if the information does not need to be brought in through an oracle — right, if it already lives in a system that’s verified, and the resolution is like provably going to do what’s claimed — then you don’t actually care about decentralization, say, in the discovery of the resolution; you’re actually just like reading information and your commitment contract takes care of everything else.

**Sonal:** And just really quick – Scott, you’ve said “oracle” a few times, can you actually properly define what you mean by oracle in this context? (I know we talk about it a lot in crypto.)

**Scott:** Yeah, and indeed, oracle is not a completely uniformly well-defined term.

In this context, I’m talking about “oracles” as like a truthful source of information about what the actual resolution of the event was: So if Trump won the election, the oracle tells us Trump won the election. And if Harris won the election, the oracle tells us Harris won the election.

And the reason we’re using that is because in 2024, the U.S. presidential election was very much not conducted on a blockchain. And so if you’re going to have an onchain prediction market, you somehow need the chain to be able to learn the information of what actually happened in the off-chain election.

And so the oracle is like basically the source of that information.

**Alex:** The key… of the oracle as Scott’s saying is to bring in off-chain and bring it onchain;

I mean, the thing about off-chain is that people can look at the New York Times, right? And so the New York Times is often considered a “oracle” — in that you go by whatever is printed in the New York Times — that would be a way of resolving a lot of bets. Like did the New York Times report that Trump won, that might be one way of resolving these bets. <Sonal: Yeah, great>

But the key problem is to bring that off-chain knowledge onchain in a way in which the information is not distorted in the transmission.

And the reason why that transmission, you’re worried about it being distorted is precisely because: It’s the revelation where all the money is. Right? <Scott: Yes> <Sonal: Yes, yes> So there are big incentives to distort the transmission of that information.

In fact, a lot of the crypto hacks which have happened, have happened because people found a way of distorting the oracle. And then using that on the crypto market. So, you know, the market resolved in one way. And if you can… change the oracle, then you can make a huge amount of profit, out of doing that.

So there’s a big incentive to mess with the oracle. That’s why it’s really difficult.

**Scott:** And we can stick with the New York Times example, right? A lot of people are going to make their morning trading decisions based on what they see in the New York Times, and on the Bloomberg terminal, and so forth.

And so if you could, in a coordinated way, feed the wrong information to that — it would change many, many people’s behavior. And you could trade against that because you knew that they were going to get the wrong information.

**Alex:** Exactly. So this can happen in the off-chain world; and indeed we saw there was one tweet, right, that the SEC is going to legalize, you know ETF Bitcoin contracts. It looked like, you know, it was an official ruling and it turned out to be a hack… Turned out to be correct, but, that wasn’t revealed until days later.

But, yeah. If you can distort an oracle, you can make money.

**Scott:** Totally. Or if we’re talking about the New York Times, it would be remiss for us to not have the like “Dewey Defeats Truman,” right? Famous- <Sonal: Ahh! Yah yah> famous front page, you know, like, huge text headline that just turns out to be inaccurate.

**Sonal:** Right. That’s a famous case of what we did in media at Wired too. It’s called the “pre-write”, and then you accidentally print it sooner <Scott: yup> and you get it wrong… there actually have been cases of someone you write their obituary months or years in advance, and it goes out and says they’re dead <Alex: oof!>

Okay! You conflated earlier — and I agree they’re generally connected and similar — but there are some nuances between “decentralized” and “distributed”. <Scott: yes> Like distributed can just be redundant systems that have multiple… Like, the system going down is what you were giving the example the night before something. <Scott: yes> That’s a case where being distributed matters, but it doesn’t have to be decentralized necessarily. <Scott: correct> — Like, i.e., there could be distributed nodes managed by a centralized entity, for instance. <Scott: absolutely>

I just want to make sure we’re very clear about the distinction between decentralized and distributed as well.

**Scott:** Totally. Whereas by contrast, with the oracles, for example, you might really care about being decentralized — Right? You might care that no individual entity can sort of unilaterally change how the contracts resolve.

**Sonal:** Exactly.

**Scott:** Just one other point. Another advantage of doing all this stuff on blockchains is that it’s “composable”.

It’s not that we’re just like intrinsically interested in some of these questions — like, maybe so; some people are just like, you know, intellectually curious like who’s going to win the presidency in a month — But rather, lots of other stuff depends on it. Right? If you’re making decisions about which supplies to order in advance, you need to have beliefs about the likelihood the tariffs are imposed under the next administration.

And so having these things live on open, composable architectures is useful because they can be _wrapped_ with other information and other processes. You can tie your corporate operations in a very direct way into these sort of information-aggregation mechanism signals.

**Sonal:** Yeah. To put it even in a more basic way — just because I don’t know if everyone necessarily knows “composable” in the way that we talk about it —

It’s like the Lego building blocks, <Scott: yup>; The markets on chain, or the information onchain — is a platform that people can build around, build with, bring in pieces of information, combine it with other tools, etc. — and you can create, like, different things. And that’s the “[composability](https://a16zcrypto.com/posts/article/composability-is-to-software-as-compounding-interest-is-to-finance/)” (and I’ll put a link in the show notes a post explaining [composability](https://a16zcrypto.com/posts/article/how-composability-unlocks-crypto-and-everything-else/) as well.)

And then the other quick one is “open source” — does the code itself have to be open source, auditable, public good?

**Scott:** Again, it depends how much you trust the-the market creator. <Sonal: Yah> And again, this is true across the board for applications that can be run on blockchains or not; like, you’re always making trade-offs between trust through reputational incentives, and institutions — and trust through code.

You know for example, like in actual commodities markets, there’s a lot of trust through institution and legal contract. But there’s an interlocutor in place to _establish_ the trust between the institutions, and the contracts, and their enforceability via the institutions — for those contracts to be real enough, that people believe in them enough to pay money for them, and to have all of these market features.

Blockchains enable these sorts of trusted activities in lots of contexts where the institutions are not strong enough or present enough to do it for you. <Sonal: yes> Right if you’re having, like, $5 bets, like, small money bets on some incredibly minor; like, will the horse that wins the Kentucky Derby have a prime number of letters in their name (or something like this). Right? You’re not going to have necessarily an institution that is even able to evaluate and set up that contract in a way that is worth doing at the amount of money it’s going to raise.

**Alex:** I like how Scott changes the Kentucky Derby <Sonal laughs> into something you would be interested in. Well if it involves prime numbers! <Scott laughs> Horse? Forget horses, but prime numbers!

<all laugh>

**Sonal:** That’s so funny. I love how well you know him!

**Scott:** <laughs> I will have you know, I will have you know the Kentucky Derby is also interesting because it has all sorts of cool statistical questions going on.

**Sonal:** And cool hats!

**Scott:** Oh, yah fascinating hats. Absolutely fascinating hats — pun definitely intended.

**Sonal:** I love it.

**Scott:** So like, substituting code for the source of trust for these like very unusual, or sort of like micro, or international… There’s not a clear jurisdiction. All of these contexts sort of push you more into security via code <Sonal: yah> rather than security via institution.

**Alex:** Let me add one more point on the blockchain —

So I think generally speaking, as I said, the blockchain is not necessary.

However, as we’re looking towards the future, it may become more and more useful to have <Scott: oh yes> these, you know, very decentralized rails.

So Vitalik Buterin [wrote a post on](https://vitalik.eth.limo/general/2024/11/09/infofinance.html) info finance, talking about prediction markets —

**Sonal:** And he credited you at the top as one of the people who reviewed it; <Alex chuckles> but yeah, keep going.

**Alex:** <smiles> Exactly. And so one of their interesting points, which he made, is that AIs may become very prominent predictors — they may become very prominent participants in these prediction markets.

Because if you can have a lot of AIs trying to predict things, well that lowers the cost tremendously. And that opens up the space of possibilities of what you can use prediction markets for.

And so the blockchain, you know is very good for — you know, nobody knows you’re an AI on the blockchain. Right? <chuckles> <Sonal: Right. Right. Right.>

And so if we’re going to have a lot of AIs interacting and acting as participants in markets, then the blockchain is very good for that.

**Sonal:** That’s absolutely right, and we have a lot of content on this topic <Alex: yah> — which actually gets at the intersection of crypto and AI, and where they’re a match made in heaven, in fact:

Not only because of AI centralizing tendencies and crypto’s decentralizing tendencies; but because of concepts like proof of personhood; being able to, in privacy- preserving ways, yet even if it on a public blockchain, find ways of adding attribution; and there’s just so much more that you can do with crypto.

I agree, Alex, and I’m so glad you brought that up.

It’s funny because when you were saying earlier — in the early definition of a prediction market as this way to kind of elicit information that’s dispersed across many people — I immediately went to like, oh that’s the original AGI; if you think about artificial intelligence, let’s just talk about human intelligence at scale. Like that’s what a prediction market can be…

## Broader use cases for prediction markets

I do want to make sure we also touch on other applications a little bit on the future — one quick thing, though, before we do that;

So now we’ve summarized some of the key features. We’ve talked about the election. We’ve talked about some of the underlying market foundations, and some of the nuances. We’ve talked about what does and doesn’t make prediction markets work and, also mentioned earlier that they’re part of a class of mechanisms that can aggregate information.

I want to really quickly — before we talk about applications in the future, near future — I want to quickly summarize what are some of those other mechanisms that could get at this kind of information aggregation that aren’t necessarily prediction markets.

**Scott:** Awesome. So, first of all, like, you know, again, just to think about what is this class of information-aggregation mechanisms. And Alex defined it earlier, it’s: these are mechanisms that bring together lots of dispersed information to produce an aggregate statistic (or set of statistics) that combine the information of many different sources. And ideally, that aggregate is informative.

Now, there are lots of ways to do that, right. Like, some of the simplest ones — we actually talked about earlier, are just to like ask people for their predictions, and later pay them based on whether they’re correct. Right? And you can do that with random people, wisdom- of-the-crowd style; or you could do that with experts, right? And so, like, very simple types of information aggregation mechanism, where people have no incentive to lie and just like, have an _opinion_, right; they don’t have to do any research or like invest any effort to know their version of the answer. You just run a survey.

But then, you know, sort of there’s this whole menagerie maybe of incentivized elicitation mechanisms that are designed around different elicitation challenges:

So I mentioned earlier, peer prediction mechanisms — these are the mechanisms where you ask people for their beliefs, and their beliefs about other people’s beliefs. And then you use people’s estimate of the population beliefs to infer like, whether they were lying to you about what they believe, and/or like how informed they were in aggregate. So you can use that to figure out where the person fits in the distribution.

And peer prediction is like an incentivized version of that. Right? So you’re going to actually like pay people based on how accurate they are — but you’re not paying them based on how accurate they are about what actually happens in the future; rather, you’re paying them based on you know how accurate they are about the population estimate, right? And so that enables you to pay people upfront immediately. These are used for, like, you know, subjective information or sort of like, information that’s dispersed among small populations; maybe it’s not big enough to have a thick prediction market — but people are informed enough that if you can directly incentivize them to tell you the truth, then you can actually like aggregate the information usefully.

A couple of my colleagues at HBS — Reshmaan Hussam, Natalia Rigol and Ben Roth — have this beautiful [paper where](https://www.hbs.edu/ris/Publication%20Files/Targeting_Entrepreneurs_AER2022_64933cef-316a-437f-8ca4-885d870b2ba1.pdf) they use these pure prediction mechanisms in the field, in a developing country context where they ask people who in their community is likely to be the most successful micro-entrepreneur. And then they allocate, you know sort of funding according to these predictions. And it turns out that like the predictions are actually quite accurate: So like the incentivized peer prediction mechanism sort of produces answers that line up with like who actually ends up being successful in these businesses down the line — in a way that is more effective, say, than just asking people and telling them, oh, we’re gonna allocate the money according to whatever you said. (Because then people will lie and say, oh, my neighbor or my friend is like, you know, the best.)

**Sonal:** I’ll put that paper in the show notes too.

**Scott:** Yeah, it’s a great paper. Super fun to read, very readable, too.

**Alex:** So one way in which the wisdom of the crowds doesn’t work, of course, is when the crowd thinks they know the answer to a problem, <Scott: yup> but they actually don’t.

**Sonal:** Oh, okay, of course. Yeah.

**Alex:** So there’s this great [paper by](https://www.nature.com/articles/nature21054) Prelec and Seung and McCoy. And they give the example of suppose you ask people, what’s the capital of Pennsylvania? And most people will think, oh well, it’s probably Philadelphia, right; it’s the biggest city, popular city; you know, American heritage, Liberty Bell, all that kind of stuff. But it actually is the wrong answer. So If you go just by the wisdom of the crowds, you’re going to get Philadelphia, and that’s wrong.

The correct answer is actually Harrisburg, which most people don’t know.

However… a small minority of people do know the correct answer. So how do you elicit this?

So, their mechanism for doing this is what they call the “surprisingly popular” mechanism. And what you do is you do what Scott says, is you ask people, not only what do they think is the correct answer, but what do they think other people will say?

And, most people of course will think well, I think the correct answer is Philadelphia; other people will say Philadelphia. But then you’re going to see a bump, right, of Harrisburg, is going to be very surprising — a substantial number of people will say Harrisburg. And that will be quite different than what people expect. And if you choose that, the authors show that this can improve on the wisdom of the crowds.

So, the surprisingly popular answer — the answer which a minority chooses, in contrast to the majority — that can actually get you more information out. <Sonal: That’s fascinating> So depending upon the question, there are these clever ways of pulling this inchoate information out of the crowd and eliciting the truth, even when most people in the crowd don’t know the truth.

**Sonal:** That’s fantastic — I’m obviously gonna include all these things we’re referencing in our show notes; but that one is really interesting!

**Scott:** That’s wild.

And then uh maybe one other piece in the menagerie, of course, that listeners to this podcast will be very familiar with, are simple auctions, right <Sonal: of course!>

Auctions are information aggregation mechanisms too. We talk about price discovery in an ordinary like, sort of very liquid market as being an information aggregation source — But, some markets aren’t like big and liquid all the time; they don’t have like lots of flow transactions, maybe it’s a super rare piece of art. But an auction is still exactly useful for figuring out what the art is worth in the eyes of the market.

And you can often discover things. Like, there’s some artist that was not popular to the best of your knowledge, and then they have a piece with like a major sale — and people’s estimates of the values of all of their other works change accordingly — because of the information that’s been revealed about people’s change in taste or whatever from this one sale.

While we’re thinking of things for the show notes, there’s an incredible book called “[Auctions: The Social Construction of Value](https://www.ucpress.edu/books/auctions/paper)” by Charles Smith. Which talks about auctions from a sociological perspective, as a way of establishing an understanding of value in a bunch of different contexts.

**Sonal:** That’s great. And by the way, I do want to plug the episode you, me, and Tim Roughgarden did, where we literally dug into [auction design](https://a16zcrypto.com/posts/podcast/auction-design-for-web3/) <Scott: auctions all day!> for web3 for hours. That was so much fun.

**Scott:** So as we’ve been like arcing through these different types of mechanisms, it’s a really good reminder that the type of question you’re asking; the type of market participants you have; and like this — we were just saying — it shapes your decisions about how to like structure your market mechanism. It also shapes your decisions about what type of market mechanism to use. <Sonal: yes>

Right? Like, if you think that the population is, not super informed on average, but like informed at the second order level, then this mechanism Alex was describing is like perfect. <Alex: exactly> Because the information’s there. It’s just not like immediately apparently there.

**Sonal:** Right. What I love that you guys are talking about — and we can now segue into some quick discussion of some applications in the future, and then we can wrap up — we’ve been talking about implications for design throughout this podcast… But I think it is very interesting because you’ve been saying throughout, both of you, that it really depends on the context and your goals, and then you can design accordingly (And that’s actually what incentive mechanism design is all about, as I’ve learned from you and Tim Roughgarden, and seen over and over and over again) — But two quick things, just lightning-round style that I want to make sure I touch on:

One, multiple times, you both have alluded to this payout feedback loop? Like, I’m _inferring_ from what you’ve said. That the payouts have to be almost quick, that you get, like, an instant feedback loop on your outcomes. Because you gave an example earlier where if it’s delayed by two weeks or so and so, it may be less effective. Is that necessarily true…?

**Scott:** Depends on trust and attention.

Some people have said that one of their concerns about prediction markets is that people like betting on sports because it’s happening in real time; you know the answer within a couple of hours, or in the case of a horse race, within minutes.

Whereas these prediction markets often take _months_ to resolve the final answer. Or the time of resolution might not even be known — tight, it might be who will be appointed to this position — so there’s possibility that speed is relevant for who chooses to participate in some context (whether they find it fun);

The other context we were talking about is when time matters for trust. If you’re in the developing world trying to figure out how to allocate grants, people might not trust, or, even just have the infrastructure support to participate in a mechanism — where they’re going to be paid six months out based on the resolution of some confusing outcome — whereas if you can pay them today, they’ll participate today.

(Hence why they experimented with peer prediction mechanisms in that context in the first place: It was sort of a setting where you could in principle pay people based on the outcome — like you know how successful their neighbor was at being an entrepreneur with whatever grant they’d received — but, a lot of complexity goes into actually doing that in practice: because you have to track down the people again, and all of that.

**Sonal:** Ah, yah!

One other quick buildery thing that came up — and again, seems so obvious to you guys probably – but, the best systems are where the prediction markets and such systems work, when there is a discrete event, like an election or something to be resolved.

It probably wouldn’t work for some ongoing, kind of loosely defined non-discrete event or…?

**Scott:** So the prediction market mechanism — sort of like the canonical prediction market as we’ve described it — is a mechanism where you’re buying, like an asset that has a payout as a function of a discrete event.

But that is, of course, not even the average case of markets. Right like, you know, when you’re buying oil futures or something, most of the transactions in many of these markets are actually sort of in the interim; it’s based on changes in people’s estimates. And so if you have a market where, you know it’s possible to sort of continually update and trade it, you know, as estimates change, then like you can still gather a lot of information — even if the value attained is in a flow or in stages or something of the sort; it doesn’t have to be sort of a single cutoff date.

**Alex:** I think you can design them in different ways. They do have to resolve at a point in time — but the way that they resolve could be based upon a stock price or something like that.

**Sonal:** Yah.

**Scott:** And you can have like dividends or something, right? <Alex: yah> You can have things that pay out over time based on sort of interim steps. Like you know lots of things have continuous payouts based on like the growth of a company or something of the sort. So you could imagine prediction securities that are kind of like that.

**Sonal:** I.E. the stock market.

**Scott:** Exactly, i.e. the stock market. <Sonal: right>

**Alex:** The HP example I gave earlier divided the time into two-month periods, right: So, is it May to June or is it July to August? Is it September, October?

So, you know, you can always take a continuous event and chunk it into — <Sonal: make it discrete> five or six discrete periods.

**Sonal:** Yeah. Yeah. Even if somewhat arbitrary. That makes so much sense.

**Alex:** So, so far, these prediction markets have been used just for what we’ve been saying, for predicting something — but you can also create, and here I’m going to riff off Robin Hanson again, my colleague on these questions —

And he says we can also create these conditional markets… So the question would be something like, as I said earlier with futarchy: What would happen to a GDP, if we put together this science policy?

Now we might not want to jump all the way from democracy into futarchy <Sonal: yah> in one go. We’re probably not ready for that. <all chuckle> We’re not ready for the full Hanson <Scott: Not quite ready for prime time, I think>

Yeah. But here’s a fascinating idea of Robin’s, which I think we are ready for, which we should use… And that is, what would happen if we fired the CEO? <Scott: Yup> So this is a huge question that companies want to know.

You know, we saw a few years ago, it was kind of remarkable when Steve Ballmer left Microsoft and the stock price went way up. <chuckles> You know, suggesting that the market thought that Ballmer was not a great CEO. Or we just saw, you know with a Brian Nichols, he moved to Starbucks from Five Guys; he’d been extremely successful at Five Guys. He moved to Starbucks… On the day that Starbucks announced that they were hiring Brian Nichols as CEO, the price of Starbucks jumped up.

So, why however, do we need to wait? How about creating a continuous market — which says, at any given time, would the price of Starbucks be higher if they fired the CEO?

And so you can create these decision markets — prediction markets — you create a prediction market in: Would the stock price be higher if we had the same CEO/ Or would the stock price be higher if we fired the CEO?

Now, that’s an incredibly useful piece of information. <Sonal: yess!> You know, companies, this is billions of dollars every single day, are based upon exactly this question. And that’s a question which I think decision markets, prediction markets, would be really good at answering —

We already have the stock market. <Scott: yes> People are already investing billions of dollars in exactly this question. And we can make it more precise, <Scott: yup> and more detailed, and more usable.

**Scott:** What I really like about that application? Is it leverages a type of information that people are already developing. Right like people are spending a lot of time reasoning about what’s going to change the stock price of Starbucks. And they have a lot of different refined ways of doing it… but it uses it to address a question that’s like useful sort of as a “practical hypothetical” —

As Alex said, it brings the information _forward_ in time. You know, normally in a current market context, we can only learn what happens if Starbucks replaces the CEO when they replace the CEO… But actually, that’s like the least important time for us to learn that. We actually want to know it like when they’re deciding, should they replace the CEO. <Sonal: Yeah, exactly. You want to know it before, yah>

And so being able to harness that same effort that people are putting into understanding what affects the stock price of Starbucks — and like, you know, which companies are well run and which aren’t — and like, pushing it towards this question can reveal important information at a time when it’s more useful… leveraging things people are already good at predicting.

**Alex:** Exactly.

**Sonal:** That’s such an interesting — and such a useful and extremely real and possible right- now thing to do — we’re not just being crazy futuristic, like 10/ 15/ 20 years from now.

That’s so great.

**Alex:** Can I be crazy futuristic, push it a little bit more?

**Sonal:** Yah, yah, we actually want a little of that! <Scott: Absolutely!> Go for it.

**Alex:** So you’re absolutely right — the should we fire the CEO market could be implemented right now and it would be extremely useful – And, it’s the first step towards making more decisions by like DAOs, by a blockchain consensus, right? <Scott: Right> <Sonal: Yes>

I mean, so if you can make a decision about should we fire the CEO? Should we expand into Argentina or into China? Should we have a new model this year, right? You can start asking the market lots of different types of these types of questions.

So let’s start with, should we fire the CEO — one of the biggest and most important, most salient of these questions — where as Scott says it’s an information-rich environment, people are already collecting lots of information, on exactly this question.

And once we’ve got some experience in this market, we can start applying it to further markets down the line.

**Scott:** Footnote, okay — I love that application, too; and that ties into the importance — we talked earlier about, you know, maybe running these markets in like an internal currency — You know an advantage there is you can use it to put everyone on the same footing at the outset.

Right, like, you know, the Starbucks CEO question, there are many different sort of like very high value, and high ability to trade entities, that already are like participating in this style of question.

Whereas for a DAO, you actually might have tremendous inequality in wealth of the participants — but you can make them wealthy in proportion to their reputation or something, you know in the internal token — which can then be used to like you know sort of have them all participate equitably at the entrance to these decisions.

**Sonal:** I love this; this is where I’m very proud that we have published a deep body of research — across many people, not just our own team — into [DAOs](https://a16zcrypto.com/posts/tags/daos/), what makes them work, what doesn’t work, what’s effective governance mechanisms. I’m going to link to that in the show notes.

And it relates so much to one of our partners’-collaborator’s work, [Andrew Hall](https://a16zcrypto.com/team/andrew-hall-2/) at [Stanford](https://politicalscience.stanford.edu/people/andrew-hall). <Alex: yes> He studies a lot on on-chain and kind of liquid democracies and more… (Because also we’re arguing that sometimes you can do a lot of these things, not just in the crypto world, but you can apply them to other decentralized communities… <Scott: absolutely> — and I want people to remember that that’s a useful use of DAOs, which are just decentralized autonomous organizations.)

Are there any other pet-applications, either current or futuristic, that either of you have? I have one, but I’m going to wait till you guys are done. <chuckles>

**Scott:** I mean, two other very quick hits —

You know we haven’t touched directly yet in the podcast on the idea of markets for private data… Right? For like you know another form of information aggregation is, maybe a lot of people have information that will be useful in designing a new pharmaceutical or medical treatment. And they have their own private information of this form…

And we’d like to be able to elicit it from them in a way that also fairly compensates them for their participation or something of the sort. And we have some mechanisms for this already — like you might have surveys managed by a health center and they pay you you know sort of a show-up fee for participating in the survey or whatever — But there’s a possibility for much richer markets of that form that leverage, sort of like individual data ownership, and like permissioning, and so forth.

**Sonal:** Yeah. One example by the way, just concretely, is like in the DeSci movement (decentralized science) <Scott: yup> — where people are putting their information, like, medical data using blockchains to bring more ownership, transparency, consent… which they don’t have.

That’s just one example. What’s the other one you had, Scott?

**Scott:** The other one is getting incentivized, _subjective_ beliefs… Right we’ve talked a lot about like predictions of things that have an objective truth. But another big frontier for information aggregation is getting really good estimates of things that people believe that are fundamentally subjective.

Right and like, you know, if you’re trying to do, like, market research for your product, you know, do people want this?

You know, one of the advantages of crowdfunding, for example, is that it’s a better information-elicitation mechanism, where you could go and ask 10000 people, do you want to buy this? And some of them might say, yes, but unless you’re actually taking money from them, you don’t know whether that’s like a truthful representation. <Sonal: yah> And so crowdfunding lets you learn about the total market for your sort of initial version of the product in a way that’s incentivized.

More broadly, I think like subjective elicitation is a really important direction to go into.

**Sonal:** Can you quickly, maybe give a very short definition in the uniquely crypto blockchain context of a “Bayesian truth serum” here? Because isn’t this where Bayesian truth serums apply?

**Scott:** Sure.

I mean, the Bayesian truth serum is actually an example of those pure prediction mechanisms we described, and there are many different versions of it — but loosely, the idea is, if I ask you your opinion on something, did you like this movie? And then I ask you, what’s the likelihood that another person I ask will say that they liked the movie? You might have a reason to lie to me about whether you like the movie or not. You might say, oh, I really liked it, because you produced it, what am I gonna do? But you actually hated it. Your estimates of everybody else’s beliefs will be sort of tilted in the direction of them mostly disliking it.

So long as I’m going to reward you to proportional to your accuracy, like, you know that you disliked it. And so everyone else probably will too — because you’re a Bayesian — And so I can detect, looking at everybody else’s responses, I can detect whether you sort of like told me a distribution of other people’s beliefs that’s consistent with what you said your belief is.

**Sonal:** Great.

One of my quick applications, and kind of an obvious one, but I want to just call it out — People often talk a lot about having quote-mechanisms for “finding truth”? I do find it very interesting that some of the commentary surfaced at prediction markets, for basically resolving more accurately and faster than mainstream media — but not having some of the same filtering of partisan interest. I mean; although this might be different with certain communities of DAOs, if you do predictions limited to certain DAOs —

**Scott:** Yeah, again it depends who’s in your market.

**Sonal:** Yeah, exactly. This goes back to your point about thick and thin —

— But, it’s also interesting because it’s a way to put a little bit more skin in the game — which is one of the biggest drawbacks in current media — is like, the people writing don’t have skin in the game.

So I do think it’s very interesting to think about this use case <Scott: totally> of reinventing news media using prediction markets. And-and Vitalik’s post actually had a great headline, which is that think of a prediction market “as a betting site for participants and a _news_ site for everyone else”. <Scott: Yup> That’d be my application.

**Alex:** So, I think more generally, it is odd how we do quite a bit of journalism.

So for example, it’s totally standard practice for a financial journalist, right, for it to be against company policy, for them to invest in the companies which they’re recommending.

Right? <Sonal: mhm!> And as an economist, I kind of think, wait a second, don’t I want the exact opposite? Right?!

**Sonal:** You want more skin in the game. Exactly.

**Alex:** Yeah, more skin in the game… Right? So, you know, I say that “a bet is a tax on bullshit”. Right?

**Sonal:** I like that line. That’s a great line. I love it.

**Alex:** So, you know, how about — you have to be upfront about it. You have to, you know, be honest about it, transparent about it — But maybe journalists should say, this is what I think will happen. And these are the bets which I’ve made.

And you can see my bets on chain. Right? <Sonal: yah, yah> And let’s see what their past track record is, right? Like, it’s kind of amazing that we do not have any track record of opinion, of editorialists whatsoever. Only Tetlock you know started to create that and found that they were terrible. Right?

But how about let’s create a series of bets and on chain. And this would you know change the types of people who become you know editorialists, <Sonal: yah, yah> who get these jobs in the first place. Right?

So let’s start making sure you bet your beliefs… And then let’s promote people whose bets turn out to be accurate.

**Sonal:** I agree; Annie Duke [talks a lot about this](https://a16z.com/podcast/innovating-and-deciding-for-companies-and-people/?__hstc=242610141.87d1003c652323126e31a5eff63be3cd.1764568219870.1768982031064.1768983873038.7&__hssc=242610141.1.1768983873038&__hsfp=0ae71827c60e136e4af32ecd4654a104) too <Scott: Yes> — It’s not just bets, like in a binary true false way — but bets that are _weighted_ in terms of likelihood, probability of accu- Like, you don’t have to make a binary, like “it will be this or that”. <Scott: Absolutely> <Alex: Yes> It could be: I believe 80% that X will happen.

And that is also another way to kind of assess, in a more nuanced way — and that gives a lot of room for the nuances that are often true when it comes to guessing the truth. <Scott: Absolutely>

**Alex:** Exactly, there’s a big incentive to say: This is never going to happen, this is impossible! Right? But then if you ask them, well, if it’s never going to happen, are you willing to bet $10 that it might happen? <Sonal: Exactly!!> And of course, they should all be willing to… Of course, they’re never willing to make those bets.

**Sonal:** That’s right. Even people who hate Elon Musk as journalists will then start saying, well, actually I’m going to bet on that guy for building X to happen because I saw that shuttle launch and now I’m thinking, okay, maybe I’ll increase that from 10 to 20% or whatever. Yeah.

**Alex:** Exactly. So betting could reduce the hyperbole.

**Sonal:** Yeah that’s exactly right. <Scott: chuckles> Yeah, totally.

**Scott:** By the way, this bordered on some other really critical information-elicitation mechanism that uses a different version of this sort of cross-examining some people’s beliefs against others.

But you think about community notes on Twitter, that’s an information aggregation mechanism, right? <Alex: mhm, mm> It’s like, it’s getting a lot of people’s opinions and then only deciding that they’re correct if you have agreement from people who usually disagree.

**Sonal:** Yes, exactly. Because that’s where Wikipedia failed when they had the cabal of expert reviewers <Scott: yah> — They didn’t have that kind of check-and-balance mechanism — Yeah, totally.

**Alex:** Yeah, community notes is a great one.

**Sonal:** I have one last question for you guys — because we don’t have enough time to go into policy… To me, the core question here is: What’s the difference between gambling and speculation? Is there a difference? I’m curious if you guys have a thought, on as a parting note on this.

**Scott:** I mean so one very important thing to remember is that… depending on the context, you may be in a different point on a continuum. Right like part of what makes sporting events exciting and suspenseful is that there’s a lot of stochasticity — and like sort of the amount of information that any individual has is reasonably small, even if they put a lot of effort into figuring it out. But there might be some amount of like you know, sort of informed betting in sporting events.

And then as you move towards things where there’s a lot of information to be had — and a lot of like value also to knowing the answer, right; a lot of market value to actually figuring it out — Right like you know how do we allocate goods in markets, right? Going back to the very beginning, when we were talking about like the role of markets and like, you know, determining the value of something; and clearing supply and demand, right? Like, there, there is value generated through the process of people engaging.

Now, there’s one really important caveat about speculation — we talk about this a lot in in crypto land, right… There is speculation of the form: “I have beliefs, and, you know, I’m investing to support a product that I think will exist and that I want to exist. And that I think other people will want.”  And then there’s also speculation on speculation, where you’re actually not so much betting based on your own beliefs — you’re betting on, you know, what you think other people will choose to bet on.

Like, we talked earlier about herding; you know, you might place bets because you think other people are going to place bets in a given direction — not because you actually have any information about what’s going to happen, just because you have information about how the market might move.

**Sonal:** That’s right. That’s speculating on speculation.

**Scott:** Exactly. That’s speculating on speculation.

So there’s this sort of like valuable type of speculation — which is, people moving resources around in a way that reflects their beliefs, and sort of like can help us make markets work better and achieve better outcomes — Like, that’s sort of in this mid space between the randomness, where moving the money around has no impact on outcomes. Right? You’re just betting on coin flips. Like, you know, your money does nothing — And this other edge where moving the money around becomes sort of its own project that is independent of outcomes. And so, again, like, sort of doesn’t provide information. <Sonal: Right>

Like, these prediction markets are particularly well architected — again, at least in the cases where they’re very large, and thick, and all the things we talked about that you need to make them work — They’re particularly well-architected to try and be in that mid space, where the information provided is valuable and comes out of like real knowledge and activity… in a way that actually sort of means the market does something valuable.

**Sonal:** Yeah. And by the way, on the earlier example (and we talk about a lot), the obvious examples where it plays out is like the Carlotta Perez framework of like speculation phase, followed by an installation phase, that’s like a driver of technology cycles;

There’s also the example — Byrne Hobart [wrote a piece](https://future.com/well-behaved-bubbles-history-innovation/) for me a few years ago on how bubbles are actually a good thing when they have a certain type of quality in this case <mhm> — And he also wrote a new [book](https://press.stripe.com/boom) about it recently for Stripe Press with Tobias Huber, which they go into greater detail about that.

**Scott:** Well, I should read that.

**Sonal:** It’s basically an example of quote- — I don’t want to put moralistic terms on it necessarily — but quote- _“useful”_ speculation <Scott: yup> that kind of leads to other things as an outcome versus speculating for the sake of speculating, which is partly the distinction you’re pointing out.

**Alex:** Well I think people, you know, in Las Vegas, who are at the slot machines… they’re gambling <Sonal: yah> — because they have no way of influencing or of improving their predictions of what the slot machine is going to show up. Right it’s just pure random chance.

On the other hand, there are many, many areas in which we are trying to predict the future — and in which investing can help us improve our predictions. And this is why I think prediction markets should be completely legal, should be legalized — because of all the forms of gambling, of all the forms of speculation, this is one of the most useful forms.

So we want to incentivize the type of speculation or gambling — which as a side product, produces you know, these useful public goods — which is trying to predict the future.

This is incredibly important. You think about all of the questions that we have, you know — What is happening with climate change? Which of these scientific predictions are accurate? — All of these questions we have, prediction markets can help us answer these questions in a way which is more objective, more <Sonal: mhm> accurate, and more open to everyone.

So, I think that the case for legalizing these is very very strong.

**Sonal:** That’s amazing. I’m going to give you the last word on that, Alex; You guys, thank you so much for joining this episode. That was so so fun!

**Alex:** Thanks, Sonal. Thanks, Scott. It’s been fantastic being here.

**Scott:** Thanks so much, really fun conversation, and uh, QED.

**Sonal:** Bye! QED ![😉](https://s.w.org/images/core/emoji/17.0.2/svg/1f609.svg)

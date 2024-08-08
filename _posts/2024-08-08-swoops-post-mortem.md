---
layout: post
title: Swoops post mortem
image: og.jpg
---

This is the story behind [Swoops](https://mirror.xyz/msinha.eth/48qMua4okBPTA4Z8E-EIk6Qmu8EcOTkjiCF5KaL3PRQ), a fantasy sports company that I co-founded in the fall of 2021, and then wound down two years later.

## Early inspirations

In early 2021, my friend [Zach](https://x.com/mcmurrayz) reached out to me about building a sports betting startup. Zach and I had met [through](https://x.com/manishsinhaha/status/1806390642647666975) Conner on what would be the beginnings of [Disco](https://www.disconetwork.com), and kept in touch ever since. When my [robotics startup](https://x.com/buzzrobotics) didn't work out, he pitched me on building a platform where a creator could run their own sportsbook.

It was intriguing for a lot of reasons. When a creator publishes their prediction, their fans run off to FanDuel and DraftKings to place their bets, leaving the creator with no upside. We wanted to make it possible for a creator to publish a prediction *and* get their fans to bet alongside the creator on real estate that the creator controlled, powered by us. If the creator’s prediction was true, they received a cut of their fans' earnings.

This became known as [Underline Sports](https://x.com/underlinedfs). We shipped a product in 3 months, handled over $40k in wager volume in a one month span, and saw ourselves as the missing puzzle piece in the creator economy. Unfortunately, the story slowed down when we went to [fundraise](https://drive.google.com/file/d/1UP3JJVbAI_iTn81p2V9DwXjhkPHjCGmb/view?usp=sharing), for three reasons:

1. Investors were put off by the huge CAC costs in the industry (count the number of betting ads next time you watch an NBA or NFL game and you'll see why).

2. The creator economy had very few breakouts at the time which made it difficult for investors to form comps[[^0]].

3. Though we were different from standard referral deals, many didn't think we were different enough.

With Zach's personal Paypal account backing our sportsbook, we needed outside capital. When we didn't get it, we threw in the towel. 

Though Underline didn't work out, I loved the intersection of sports and real money gaming. It's a demographic I knew well because I was a part of it. I have been [playing](https://x.com/manishsinhaha/status/1513898267301466121/photo/1) sports since I was a kid. I have been [gaming](https://accessible-lip-ffc.notion.site/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2Fc6d2b138-fcdb-44fc-b744-0946963b0648%2FUntitled.png?table=block&id=9be962c5-dc02-4442-ab70-1695ae5efbbe&spaceId=9dcafdcd-4f4c-4564-9476-c6497f466134&width=580&userId=&cache=v2) since Commander Keen and Doom. It didn't feel like work building for this audience; it felt like fun. 

I wanted to keep having fun.

## The genesis of Swoops

The summer of 2021 was an explosive time for crypto. Not only were the currencies hitting highs, but NFTs went mainstream—especially on the collectible front. The only way I can look back at it is as a fever dream. Everyone was high - investors, founders, consumers. It felt like each week brought a leap of progress, either with the big L1s innovating or new L2s coming on the scene. It was similar to the frenetic energy around LLMs in late 2023.

I started studying web3 games like Zed and Axie Infinity. These games had one main twist: your character was a financial asset, represented by an NFT. Whereas BAYC gave digital art in the form of an NFT, these new breed of games gave *utility* to your digital horse NFT (in the case of Zed), making it possible to win cash prize contests *and* ride a potential valuation increase of your NFT.

I whipped up a [memo](https://www.notion.so/Virtual-Basketball-League-c9898fd067cb4ddd83704137cc1f8450) on what a web3 basketball game might look like and threw it over to Zach. He sent it over to [Drew](https://x.com/drewaustin?lang=en) of Redbeard who sent it over to [David](https://x.com/davidrgoldberg) of Alpaca. Turns out David had a similar idea but packaged inside a much more powerful story:

> Sports is a $40B market, but so little of that is captured by fans. In fact, it's the middlemen of leagues, broadcasters, and teams that capture most of the value. Fans not only want a bigger piece of the pie, they deserve it because it's *their* time & attention that is monetized and used to run sports. Swoops is that first of a kind, digital sports league that makes it possible for anyone to be a team owner and operator.

As far as the mechanics went, our first sport would be basketball. Our player IP would be our own (a pivotal decision that I’ll talk more about later). A user would assemble a squad of 5 players and have them face off against an opponent’s squad of 5 players. Our simulator would use the metadata of all the players, with a sprinkle of randomness, to produce an outcome.

With a story and mechanics in hand, David and I partnered up and went to go fundraise.

## The raise

Part of the advantage of waiting in the water is that you get to ride the tide when it comes in. We captured the moment perfectly, providing investors with something that they wanted to invest in. They saw the success (at the time) of other web3 games, established the 'Zed for basketball' comp in their head, and liked us as a team.

We closed our lead investor by week 3. The rest came in after as we kept expanding the size of the round. Most of our investors were in sports tech (Courtside, Harris Blitzer, Celtics ownership, Vayner Sports). Others wanted exposure to crypto (Alpaca, Pareto, GroundUp, Hustle, Form Capital). Though I didn’t get to pitch Ja Rule or Ros Gold-Onwude directly, it was pretty cool to have them on our cap table[[^1]]. The SPV filled out in three days IIRC. I'll never forget random people finding out about it and begging me for allocation. It was a strange position to be in, to suddenly have all that power. All in all, we raised $3.5M. 

Fundraising had always been one of my weaknesses which is one of several reasons why I partnered with David. His network and story building skills came up huge in putting this round together. It wouldn’t have been possible without it.

## Initial highs

### Community & Marketing

We focused first on community, investing a lot in our Discord. Web3 games are unique because they are played in Discord. It's where you swap alpha, form alliances, and do deals. Seeding our community with users who sat in the overlap of crypto and basketball, our ICP, was key. Creating a positive, collaborative atmosphere was also important - not always easy when money is involved. We experienced some high highs here, including 11k users (with plenty bots) joining overnight after an [outlet](https://decrypt.co/97521/gary-vaynerchuck-backed-swoops-raises-3-5-million-for-nft-basketball-game) wrote about us.

Marketing played off the strengths of our community. Our team crafted a strategy that turned our game into a real sports league. The biggest successes were in creating a calendar of events for our 3 month long seasons and creating marketing moments around those events. Pre season, regular season, tournaments, MVP selection, all star selections - each milestone was like an injection of energy into our community. Each season culminated with our Swooper Bowl which was must-see-TV on our [Twitch](https://www.twitch.tv/videos/1926341465).

Of course, I did my best to share the word too, even if it meant [getting roasted](https://x.com/manishsinhaha/status/1697313411804311790).

### Engineering & Ops

As an engineer, I cared a lot about our engineering talent and culture. I wanted product engineers who understood sports and engineering. People who could speak our sports lingo, jump in a call with users, and write solid code. 

I built a team of four engineers and went to work with a designer to create a compelling UX. On the backend, the "real" part of real money gaming became quickly apparent as we had to write systems that handled the movement of money with speed and robustness. We settled on a limited microservice setup where we had our backend service interact with our segregated simulator service. Our frontend engineers were amazing, and rolled with the countless iterations we went through with stride.

The hardest part of early stage startup life is finding the balance between speed of development and code hygiene. We did this part well, and kept a high velocity throughout with what’d I’ll call B+ code.

<p align="center">  
<img width="600" src="https://i.imgur.com/U9QB8xT.png"/>  
<br/>  
  <i style="font-size: small">When a game completed, we gave you an ESPN Gamecast like view.</i>  
</p>

### Data Science

We called ourselves the most advanced basketball simulator in the world and we meant it. I hired an amazing trio of data scientists who rose to the challenge and did exactly that. We took special care of keeping our sim proprietary and locked down, because it had to remain a puzzle that users learned over time. 

On top of the simulator, we had an elaborate way to continually refresh our digital players (or Swoopsters, as we liked to call them) and introduce new ones. Every season, we'd do two things:

* Run existing Swoopsters through an aging algorithm that took into account a slew of factors to either degrade or upgrade their performance. 

* Introduce a new batch of Swoopster rookies.

<p align="center">  
<img width="600" src="https://i.imgur.com/n52Izp5.jpeg"/>  
<br/>  
  <i style="font-size: small">Each Swoopster had 15 skills. Each season, every player would have one skill revealed.</i>  
</p>

### First drop + game launch

Our first player drop was in January of 2023. We sold out our 1500 players @ 0.05 eth each in 30 minutes. It was one of the blurriest days; I barely remember it.

A couple months later, we followed up with the launch of our game, which was a hit as well. Users were spending over *90 minutes* a day on it. By the time we shut down, we had over 500k+ games played, $600k in player trading volume, $200k of direct sales and a D1/D7/D30 of 56%/32%/29%. I remain incredibly proud of how sticky our product was.

### Culture

On the culture side, we had some offsites for our staff (or "Swoopies", as my wife liked to call us). These were huge, and I could probably write an essay about the purpose and utility of them (tldr - do them).

<p align="center">  
<img width="600" src="https://i.imgur.com/YgjAwYo.jpeg"/>  
<br/>  
  <i style="font-size: small">One of our engineering offsites, in Medellin.</i>  
</p>

## Challenges

### VBA

At the end of 2022, the [Virtual Basketball Association](https://vbagame.medium.com/) shut down. Though they were building on a different chain (Solana, whereas we were on Ethereum), they were the closest competitor we had. Founded by Charles and John, I'd actually gotten to know them before we all got into this space. With over $6M raised by two founders I had (and still have) a tremendous amount of respect for, we took them seriously.

Which is why our collective jaws dropped when they announced that they were shutting down. They were struggling to grow and lost faith in the market. I’ll always remain grateful for the time they took out of their schedule to educate us about their learnings. While we studied them, we soldiered on.

### Shrinking market

The music started to slow down. Crypto currencies were dropping in value, NFT trading volume fell off a cliff, and many web3 games shuttered. What was a blue ocean started to look red, day by day. 

We saw this on the ground. Our marketing playbook centered around activating our users to spread the word, partnering with adjacent sports+crypto communities, and doing small deals with targeted influencers. We ran experiment after experiment, but couldn’t land a repeatable sales motion.

This impacted our revenue. While we sold out our season 0 drop immediately, it took longer for season 1, and much longer for season 2. More worrying, the same set of users were participating in our drops. We had a proud, loyal, and sticky core of users numbering in the hundreds. It was proving hard to grow beyond them.

### Crypto friction

If we weren't going to attract crypto native users, we needed to bring in 'normies'. This proved difficult. Consider what onboarding looked like for such a user:

1. Comes to our website, attempts to signup, notices they need a wallet.  
2. Figures out the wallet (hopefully), signs in.  
3. Realizes they need Swoopsters. Maybe reads our docs to figure out how to get them.  
4. Gets to OpenSea, evaluates Swoopsters (somehow). Attempts to buy one.  
5. Needs to load their wallet with ETH, so they go to Coinbase…

You get the point. If you're not already in the world having practiced with collectible NFT projects, this is a huge leap to make. And to our credit, we did smoothen some of these steps (eg buy players via credit card, free off-chain player when you sign up). But it's just so far away from a traditional game where the entire experience is unified, under one hood.

And don’t get me started on crypto tooling. A huge piece of these games is the embedded wallet and atleast as of 2023, all of these solutions (Magic, Web3Auth) just flat out sucked. Terrible DX, so-so UX–but most of all–they catered to an audience that needed it the least: crypto native users.

### Legal gray areas with influencer marketing

In October of 2022, Kim Kardashian was charged by the SEC for promoting a crypto asset. Many athletes and celebrities took note, and stopped promoting anything to do with crypto, including NFTs.

This made life difficult for us. Many athletes were LPs in our investors’ funds. One of the most influential people in the industry, Gary V, was a direct investor in Swoops through Vayner Sports. We had access to these amazing people but we couldn’t do anything with them. Though they helped in other ways, they were understandably hesitant to promote our drops after the SEC decision.

### Fundraising

By the spring of 2023, we started talking to investors. We needed to capitalize Swoops by the Fall in order to survive.

We put together a story that centered around our loyal base of users who spent more than 90 minutes a day on Swoops. We had a sticky product serving a narrow group and we needed capital to expand beyond crypto native users. 

Unlike the first go-around, this time was much more painful (or, realistic). Investors praised us for our sticky cohort of users. They bought the high level vision that fans wanted a deeper relationship with sports. They were not satisfied with our growth rate. And for many of them, crypto was radioactive.

## The last months

We put together a plan to reduce the barrier to entry for non crypto native users. We cut salaries and eventually some staff to reduce burn. As difficult as this period was, we grinded so hard those last couple of months. It was all hands on deck; everybody knew the stakes. Engineering stepped up, marketing stepped up - we were doing everything in our power to save the ship. 

In late July, I had a motorcycle [accident](https://x.com/manishsinhaha/status/1694162032831205622/photo/1) that took me out for two weeks. On pain killers and kind of delirious, I did my best to push through and keep everyone motivated, including myself. Between lack of sleep, physical immobility, and company uncertainty, this stretch was the single most stressful part of the entire journey for me. I felt the walls starting to close in on us.

As a last ditch effort, we pursued some M&A but no one was interested. Ultimately, we pulled the plug and [open sourced](https://github.com/dopeboy/swoops-webapp) our code.

## Could we have done anything differently?

Anything that would have changed the overall outcome? I'm not sure. Here are the big questions I'd ask if I could go back in time:

* **Are NFTs needed?** This would have been crazy to ask when we started. But over time, NFTs became a huge barrier to growth. Wallets, marketplaces, gas fees–they all got in the way. I would have started with NFTs and very immediately migrated them off chain[[^2]].

* **Should we have used NBA IP?** John of VBA once told me (paraphrased): "people don't care about basketball, they care about the players who play it". Without NBA IP, we had no lore or world to piggyback off of. Our Swoopsters were robots and though we did attempt to create our own lore, it was no match for the connection people had with real NBA players. I suspect games like Sorare and NFL Rivals, who are using real world IP, are doing well for this reason, among others. 

* **What does a game designer do and do we need one?** Game loops are an important concept because they spell out the incentive system for (1) why someone plays in the first place and (2) why they come back. We had some informal help along the way but in retrospect, I wish we invested more. There were several team members who pushed for this and I didn’t listen; I regret that.

* **Are we a game or a sport?** This was a question we internally debated forever. Games are meant to be played. Sports are meant to be watched. We blurred these lines, because that was part of our mission. Ultimately, we ended up a hybrid but I wonder if things would have been different if we picked one lane from the outset.

## What I learned

* You never know where a path will lead you. I'm so lucky to have met Zach in OnDeck, discover my love for sports & gaming through Underline Sports, and ultimately meet my co-founder David. Take the meeting, talk with others, share your writing. Most of all, take action. Because action begets action.

* Be ultra specific about your definition of product market fit. Then, do not collect pass go, do not collect $100, and do not build a big team until you're there. You need to survive long enough to hit this point, so conserve the cash to give yourself sufficient time to get there[[^3]]. 

* Timing matters. Recognize “what’s in” and find your niche within it, if there is one. We started at a time when tailwinds were high, and the effects of them were real.

* B2C is a wild world. There were some days I felt like I was plugged into the matrix. Drinking from the firehose of twitter, twitter DMs, and Discord was stressful. As I get older and think about sustainability, there is something in me that wants the calmer, more deterministic path found in B2B[[^4]].

* When building Swoops, I stopped going into SF, stopped catching up with friends, stopped hosting the SF django meetup, and instead just focused on building. I don’t want to make that mistake again. This game is a long one, and relationships accrete over time. I’m going to make time for them.

## Thank you

David, you took a shot on working with a complete stranger. I'll never forget those early days where we talked about our ideas for Swoops (or Metaball, in those days). I learned how to fundraise from you. The art of leading, persuading, selling, strategizing, deploying humor - these are all subtle cues and habits I've adopted and continue to work into my work style. I never imagined being a CEO in my life, ever, and yet you challenged me to it. I'll never forget that.

Kai, you were the best board member/observer we could have asked for. You always came through with intros, shared what you were hearing from other companies, and straddled the line between investor and advisor in a fair & balanced way. You’ve played this game as a founder deeper than most investors, and I’ll always hold you in the highest regard for that.

To our users - thank you for betting on us. You helped us spread the word, [covered](https://medium.com/@SI_Swoops) us with your new media operations, gave us product feedback, and pushed us to make Swoops the new age digital sport it deserved to be. From day 1, we wanted Swoops to be a league by the fans, and for the fans. Though we ultimately fell short, I hope we delivered on that part of the promise.

To our investors - thank you for believing in us, and in our wild vision to make it possible for anyone to be a sports team owner. Your support was unconditional throughout the entire journey, and I’m grateful for it. I hope we get to work together again, in future ventures.

And to our team - I will never forget how hard you worked and how much you cared. There were several late nights and weekends that you gave to pull things over the line. Though we were spread across the country and the world, we had one common bond: our love for sports. Thank you for pushing me as an engineer, as a leader, and as a first time founder. My most treasured moments overlap with being in the same room as you, working on hard problems together. I hope our paths cross again.

<p align="center">  
<img width="400" src="https://i.imgur.com/YGb7xA6.jpeg"/>  
<img width="400" src="https://i.imgur.com/4Um4MUU.jpeg"/>  
<img width="400" src="https://i.imgur.com/X484puz.jpeg"/>  
<img width="400" src="https://i.imgur.com/7FQdL0C.jpeg"/>  
</p>

## What's next?

I took some time to rest, relax, and write code for some awesome startups. It's been great to just focus on one lane again.

I returned to South Park Commons, with some mixed emotions because I felt like I failed the 4th grade and had to retake it. But it turned out to be the opposite because it’s been such a joy to be around other ambitious people. I want to give a special shoutout to three founders: Ashwin Lalendran, Patrick Lung, and Hari Raghavan. Whether you all realize it or not, I’ve found renewed confidence in myself after hanging around you guys.

LLMs are one of the biggest innovations of our lifetime. What a time to be alive. I want to build a new venture that uses this technology.

[Zeeshan](https://x.com/_zeeshan_mughal) (eng #1 at Swoops) and I have been studying the role of AI engineer agents. We’re evaluating the Solutions Consultancy market, and asking what role–if any–do agents play in assisting with the deployment of tools like SAP, Salesforce, and Netsuite. These are often multi month, high five figure engagements. Is there a way to trim that? 

If you’re interested in this space, reach out over [email](mailto: arithmetic@gmail.com) or follow me on [twitter](https://x.com/manishsinhaha) or [linkedin](https://www.linkedin.com/in/manish-sinha-9675b366/).

## Footnotes

[^0]: In retrospect, the creator economy had zero breakouts. The platforms captured all the value.

[^1]: Ja Rule [performed](https://x.com/manishsinhaha/status/1819678886596337969) at an NFT NYC event that we co-hosted. He’s still got an amazing stage presence.

[^2]: I believe [PhotoFinish](https://photofinish.live/) did this. 

[^3]: I know this seems obvious now, but it wasn’t “back then” during ZIRP times. It was all about blitzing your way to growth and an A round. Had we started a year earlier, I think we would have succeeded with this objective. 

[^4]: Neither is a walk in the park. But from the outside looking in, I get the sense there’s less luck involved in B2B.

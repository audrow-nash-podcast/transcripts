- [\[00:01:36\] Introduction to Rjat and Chef Robotics](#000136-introduction-to-rjat-and-chef-robotics)
- [\[00:03:03\] Early Ventures and the Power of AI](#000303-early-ventures-and-the-power-of-ai)
- [\[00:05:51\] Identifying the Market Opportunity](#000551-identifying-the-market-opportunity)
- [\[00:08:15\] Challenges in Food Industry Automation](#000815-challenges-in-food-industry-automation)
- [\[00:13:13\] Pivoting to High Mix Manufacturing](#001313-pivoting-to-high-mix-manufacturing)
- [\[00:42:33\] Bootstrapping AI for Real-World Robotics](#004233-bootstrapping-ai-for-real-world-robotics)
- [\[00:45:23\] Expanding to New Markets and Applications](#004523-expanding-to-new-markets-and-applications)
- [\[00:48:46\] Challenges in Food Manipulation](#004846-challenges-in-food-manipulation)
- [\[01:02:06\] Leveraging Learning from Demonstration](#010206-leveraging-learning-from-demonstration)
- [\[01:23:12\] Field Replaceable Units and Service Strategy](#012312-field-replaceable-units-and-service-strategy)
- [\[01:24:05\] Scaling and Global Deployment](#012405-scaling-and-global-deployment)
- [\[01:25:25\] Hardware Upgrades and Modularity](#012525-hardware-upgrades-and-modularity)
- [\[01:29:45\] AI and Robotics Industry Trends](#012945-ai-and-robotics-industry-trends)
- [\[01:36:58\] Challenges in Robotics Production](#013658-challenges-in-robotics-production)
- [\[01:53:45\] Hiring the Best People](#015345-hiring-the-best-people)


[00:00:00] **Audrow Nash:** Welcome to the Audrow Nash Podcast. I'm your host, Audrow Nash, and today we're diving into a fascinating world of AI powered food automation with Rajat Bhageria, the founder and CEO of Chef Robotics. In this episode, we explore how Chef Robotics is revolutionizing the food industry by developing AI enabled robots for Food Assembly. Rajat shares insights on why the food industry is arguably the best market for AI today, discussing the massive labor shortages, challenging work environment, and the potential of AI to transform food production at scale. You'll learn about Chef Robotics journey from concept to production, including their strategic approach to market entry, data collection, and scaling their technology. Rajat offers valuable lessons for aspiring roboticists and investors covering topics like the importance of real world training data in robotics, how to bootstrap a robotic startup and secure customer commitments, the challenges of deploying robots in production environments, and the future of food automation and Its potential impact on the industry. Whether you're a roboticist, an investor, or simply curious about the future of food production, this episode offers a wealth of insights into one of the most promising applications of AI and robotics today,

So grab a snack, maybe one assembled by a robot in the near future, and join us for a fascinating exploration of AI, robotics, and the future of food. Let's dive in.


## [00:01:36] Introduction to Rjat and Chef Robotics

[00:01:36] **Audrow Nash:** Would you introduce yourself?

[00:01:38] **Rajat Bhageria:** Hey Audrow! Yeah, I'm Rajat. I'm the founder and CEO of Chef Robotics.

[00:01:42] **Audrow Nash:** Awesome. And would you tell me some of the details about Chef Robotics? Like how many employees you are, what stage of funding, these kinds of things?

[00:01:51] **Rajat Bhageria:** Yeah, Chef Robotics, we're like 32, 33 employees. We're based out of San Francisco, California. Funding wise, I think, we're at 22 and a half million in equity and debt. I think 18 or so of that is equity. And the rest we use for equipment financing, to fund the robotics as a service. we have robots actually now deployed, all over North America, including, Canada.

We're actually now actively thinking about Europe as the next kind of market. Yeah. And, things are going relatively well. So we've now actually made around 17. 7, I believe is the latest, million meals in production, which is awesome. So that's broadly what we do. And of course we, make, AI enabled robots for the food industry.

And of course there's a lot more depth there, but broadly AI enabled robots for the food industry.

[00:02:41] **Audrow Nash:** Hell yeah. Now, when we talked in a quick call before this interview, you gave me a, an overview how, did you pick this market and then how you started Chef Robotics and how I don't know, the whole problem space that you're going into. Would you tell me some of that? Start at the motivation.

Or the market.

[00:03:01] **Rajat Bhageria:** Yeah, sure. 


## [00:03:03] Early Ventures and the Power of AI

[00:03:03] **Rajat Bhageria:** in, in college actually, so I went to Penn for undergrad and grad school, I was working on a company called Third Eye. We were using computer vision to essentially recognize what's in front of you for the visually impaired. And worked on this company for three and a half years, and we can talk about Third Eye as well if you're curious, but I think this company really introduced me to the power of computer vision, more than anything else.

before then, I had done a lot of, web programming and, desktop programs, but for the first time, a computer could make sense of the physical world, which was just insane to me, right? And it really got me thinking about, the power of AI and, computer vision. And, my next kind of question is, okay, Third Eye was completely a software, right? Product, right? we had, we were using smart glasses, but of course those are off the shelf or mobile phones also off the shelf. So it was purely a software product. And I was like, okay, is the biggest application of ai?

Is it gonna be purely in the digital world or is it really gonna be. In the physical world. I, was just curious. And, I just started to do some brainstorming. It's and it became abundantly obvious, like the, like 90 plus percent of global GDP is in the physical world, right?

It's like things like construction and agriculture and food and beverage and healthcare and, all these other industries, right? these are really where the majority of the wealth of the world is. So I was like, okay, of course, then if you're interacting with the physical world, then, you can take sensor data in using a camera, but of course you also probably need to actuate.

So I think I became pretty excited about the prospect of kind of combining AI plus robotics to have embodied AI, right? And this kind of became like extremely, exciting for me because, I, I feel like I'm very lucky to enjoy my work. I really enjoy my work, but I do know there's hundreds of millions of humans, billions of humans who.

Don't have that luxury and it seems wouldn't it be nice if we lived in a world where there was abundance where Robots can do some of the dull dangers and dirty jobs and robots can do And humans can do something hopefully more humane and better. So that vision was exciting and you know I wanted to really focus on embodied AI And, that's decided to get my master's in that and focus in on that. but I didn't know what product to build yet or what industry yet to focus on, right? and I took a bit of a detour to figure that out. a friend and I, started a small VC fund called Prototype Capital. basically investing in founders who are using new technologies in old industries.

Old industries like oil and gas and food and beverage and all the industries I just alluded to, right? and, again, we can also talk about the prototype experience, but at least what's relevant for the, for Chef is that, that allowed me some time to just understand the industry, the physical world a little bit more, talk to a lot of people in these different industries.


## [00:05:51] Identifying the Market Opportunity

[00:05:51] **Rajat Bhageria:** What, I, learned is actually that, the food industry is probably one of the best places to apply AI, just from a market size perspective. Period. And specifically the reason I say this is that, if you look at the Bureau for Labor Statistics, the, you know, the domestic population in the U. S., the most common job are things like the number one and number two most common jobs are retail salespeople and nursing aides and personal aides. those two jobs I don't think will be automated by AI robots anytime soon. It's a very human job. okay. It was like, okay, what's number three? Number three is food service and food preparation.

So that felt a lot more tractable to me, right? And by the way, I'm not from the food industry, right? So I didn't totally understand it, but I can at least, I go to Chipotle and Sweetgreen and I've seen those people assemble those meals. It seems like you take a camera and a manipulator and some different utensils and, make a robot that does that too.

So it just felt a little bit more tractable to me. that idea of, okay, it seems like the market size is pretty big, was exciting. And specifically what specifically, there's an interesting insight, which is if you, agree that the biggest impact for AI is in the physical world, because 90 percent of global GDP is in the physical world, then it's okay, what part of the physical world do we focus on?

And then we said, okay, what's the biggest market in the physical world? And it's the labor market, which is like 45 trillion of GDP. And then, okay, what's the biggest part of the labor market? it's retail salespeople and nursing, but that's not tractable. the biggest tractable market for AI today, From this, analysis I did, at least, was food service and food production, food preparation.

it's okay, there seems just from a market size perspective, this is something that I want to, really investigate and look into. But of course, like I said, I didn't know much about the food industry, so the next step was just talking to as many people as I could possibly talk to. And, I think this was a very broad search, right?

This was everything from fast casual operators to ghost kitchens. at the time, Travis Kalanick had just raised a bunch of money for cloud kitchens. and, companies like Reef and Kitchen United were blossoming. This is still pre COVID by the way. we talked to like food truck operators, we talked to airline catering companies, food manufacturing companies, what's the biggest pain point you face, right?

What's going on, right? And what I, learned is that the. 


## [00:08:15] Challenges in Food Industry Automation

[00:08:15] **Rajat Bhageria:** The biggest thing that everyone said over and over, without exception, was there's a really, crushing labor shortage. And, of course in robotics you hear this very frequently. It's not a new piece of information. What was interesting with the food industry, they said, is that oftentimes food environments are extremely cold, 34, 35 degrees Fahrenheit, or extremely hot, right?

80 plus, 90 plus degrees Fahrenheit. hiring is actually Oftentimes harder than other industries like warehousing and logistics and supply chain. So it seems like there was a very pressing need where AI plus robots could really help. 

[00:08:51] **Audrow Nash:** And you're saying that reason that, or one of the reasons that the hiring is difficult is because of the environmental conditions that it's hot or cold. So it's unpleasant to work there and thus people don't work there often. And I saw like the turnover is super high for the people that are in it.

So you think it's it's miserable, possibly partially because of the environmental conditions and that just exacerbates these labor shortages. Okay. 

[00:09:16] **Rajat Bhageria:** Yes, and not only that, you have these redundant motions, right? you're like, you're often scoop chopping and scooping and you're doing a lot of redundant motion So that like back injuries and there's just a lot it's a lot of physical exertion in a very uncomfortable environment Which comes together to not be the greatest job,

[00:09:35] **Audrow Nash:** for sure.

[00:09:36] **Rajat Bhageria:** So You know, I think this obviously has a lot of implications. for the business itself, I learned, and this is again true from the big kind of food manufacturing companies to the small food trucks, the business implications are also severe, which is that they often are leaving revenue on the table.

Specifically, what I mean by this is if they could have made, x meals or volume, now because they don't have enough labor, they can only make 70 percent of x. So they're leaving revenue on the table. their supply of labor is not able to meet demand of labor.

[00:10:07] **Audrow Nash:** That's wild. Okay. Yes, so, they literally are just not making as much money as they could if the production was higher for this kind of thing. And that probably also drives inflation in their costs and things like this, because it costs more to get out less, and then they're making less profit, and then they have to charge more for what they do make.

So that's a vicious cycle. I think

[00:10:28] **Rajat Bhageria:** yes, and there's another vicious cycle in there as well, which is that because you don't have enough labor, you have to ask your current folks to work overtime, which of course, it's not because there's turnover, so

[00:10:39] **Audrow Nash:** or but even increases it further because of this they burn out

[00:10:44] **Rajat Bhageria:** yes.

They burn out. They burn out. So it's a pretty rough situation. And by the way, that's from the business side. There's another like more like socioeconomic and nationalistic reason. Like some of these companies, especially the bigger ones, the manufacturing ones, right? The food manufacturing companies, they were actively at least considering, hey, how do we how do we make this work?

Obviously, robotics is on the table, but also Can we take at least parts of our supply chain? Maybe not everything, because it's food, there's a freshness factor, but can we take parts of our supply chain offshore? So these are, both these things combined, and it felt big market, like arguably number one market for AI, market size, from the market size perspective.

Seems like there's a hair on fire problem, right? And okay, I was like, let's dig deeper, right?

[00:11:29] **Audrow Nash:** do you mean hair on fire like it's a big problem right now is that what you mean by that

[00:11:33] **Rajat Bhageria:** What I mean by that is I think like in startup world, one of the lessons, at least I've learned is that, you can have products that are like, the classic expression that many VCs use is like 

[00:11:46] **Audrow Nash:** pain or vitamin yeah

[00:11:49] **Rajat Bhageria:** So a vitamin, like you can sell it, but it's it's never priority number one.

It's let's take care of that next quarter. It's sales cycles are long and It doesn't really have that, exponential growth, whereas if you have a painkiller, it's like sales cycles are quick, it's like the Warren Buffett quote, I want a business that even a dumb person can run, right?

It's that

[00:12:08] **Audrow Nash:** yeah

[00:12:09] **Rajat Bhageria:** right?

[00:12:09] **Audrow Nash:** it's a great quote okay

[00:12:12] **Rajat Bhageria:** yes.

[00:12:12] **Audrow Nash:** all right so hair on fire

[00:12:14] **Rajat Bhageria:** It's a hair and fire problem, and they really desperately need a solution. it's, another way, another analogy that's coming to my mind right now is when, SpaceX was founded, there wasn't really a great launch solution, right? Of course you had governments, they're expensive, extremely expensive, very

[00:12:31] **Audrow Nash:** oh yeah

[00:12:33] **Rajat Bhageria:** And SpaceX was able to actually come in and people were willing to work with them even though they actually hadn't launched any successful rockets in the early days because they were the only game in town, right?

So because there's a hair on fire problem for people to take satellites to space, there wasn't really an alternative. People were willing to like, work with a small, scrappy startup and make it work, right? If that makes sense. So there's a lot of reasons why that kind of problem is a good problem to solve, I think.

[00:12:57] **Audrow Nash:** gotcha okay

[00:13:00] **Rajat Bhageria:** the next question is, okay, great, it seems like market's big, there's a big problem that we can, AI and robots can help with. The next kind of question I had is, okay, what kind of task do I work on? 


## [00:13:13] Pivoting to High Mix Manufacturing

[00:13:13] **Rajat Bhageria:** and again, I'm not from the food universe, so what I did is just interviewed a lot of people and what I learned is that broad strokes, and everything except fine dining, because again, we're not trying to focus on fine

[00:13:22] **Audrow Nash:** yeah

[00:13:27] **Rajat Bhageria:** the world of a kitchen into three broad strokes tasks. You have to prep food, which is cutting things, washing things, getting the ingredients ready. Then you have to do the cooking itself. and then finally you have to do the plating or the assembly, just to put the plating or assembly into, context and help, help, help you visualize it.

Essentially, it's what you would see at Chipotle, right? So the person who's kinda scooping the chicken, the rice into your burrito or your. Your bowl. but, really the, thinking there is you have to Be flexible, do lots of ingredients, deal with the different portion sizes, place in different compartments or parts of the tray or burrito or the wrap or sandwich, things like that, right?

Not spill it, not damage ingredients, etc. What was really interesting for me is that my impression was that cooking is going to be the most expensive part of this process from a labor perspective. What I learned is that actually that's not true. the most expensive part of this process is food assembly, which is interesting.

And, the reason it was interesting, is that what I learned is that from a prep perspective, there's actually a lot of traditional automation, essentially food processors, is the way you can think about it. Now, there might be, 

[00:14:37] **Audrow Nash:** industrial scale

[00:14:39] **Rajat Bhageria:** yes, no, exactly, but, even like food trucks use it, even like fast casuals use it, and of course food manufacturers use it.

different sizes, of course, but yeah, I think you get the analogy. food prep is, it does require labor, but it's not necessarily something that scales linearly. In other words, if you need more volume of material, you don't need more human beings, right? Because you have this traditional automation,

[00:15:04] **Audrow Nash:** it's very

[00:15:04] **Rajat Bhageria:** scales more sub linearly.

It's very efficient. It scales sub linearly, right?

[00:15:08] **Audrow Nash:** It's one person driving a huge tractor or something like that, as opposed to a bunch of little tractors. Okay.

[00:15:14] **Rajat Bhageria:** That's right. That's right. That same analogy is true in cooking, but for a different reason. So in cooking, you can cook in batches, right? one person can cook a soup for a thousand people. One person can be at the grill flipping burgers for 60 people, right?

again, same analogy. It scales relatively well. It scales sub linearly, right? 

you can imagine that if you need to make, if you're like, a Chipotle during dinner rush in Manhattan, you can have a few cooks, like two, three. They can cook for everyone because you can do big dishes.

Portion sizes, very big batches. So that leads us to assembly. Assembly is the only part of this equation that actually scales more linearly. In other words, if you need more output or you need more throughput, you need more human beings. Because it's an assembly line, right? Each person is like, if you need, if you literally need more bowls coming out, you need more humans making those bowls in parallel. Does that kind of make sense?

[00:16:14] **Audrow Nash:** Yeah. 'cause you're, basically, I'm thinking of, assembly is the good word for it, but if you had, I dunno, you're just, you're adding a single and each person may be adding one ingredient in one spot and it's that's pretty, you have to do that manually. You can't do it. There's not like a big scooper with a hundred ends that you can just, especially for custom dishes, especially for like restaurants, I would assume at like end point locations, like right where the customer is eating, but it's probably true elsewhere in like those grocery store, buy a meal in a bowl kits and this kind of thing.

[00:16:49] **Rajat Bhageria:** that's right. 

[00:16:50] **Audrow Nash:** linear. Almost. It's, probably basically linear in terms of huh.

[00:16:57] **Rajat Bhageria:** basically what I learned is that like 60 percent of the labor in a commercial or industrial kitchen that makes meals is in food assembly. Otherwise known as plating,

[00:17:07] **Audrow Nash:** bonkers. I would not have thought, but it makes sense now that you're explaining it, but I really would have thought prep would be larger, but I see what you're saying about you get the efficiencies of it. And same with cooking, you can batch, whereas assembly you can't batch, and therefore when you're doing scale, that's the one.

Because it's linear, it's such a problem. 

[00:17:25] **Rajat Bhageria:** that's right, it became pretty clear that if we were to help with this labor shortage, if we were to solve one problem, we should really focus on food assembly. Right now it was like, okay, great. we have a big market, we have, it's a big pain point. We think that the biggest thing we can help across the market, not just in like fast casuals, but not just in food trucks, but really across the market, food manufacturing, it's food assembly. Then it was like, okay, like who are going to be our customers, right? Who do we sell to?

And of course, the first question is, this a B2C company or is it a B2B company? we considered B2C actually, at the very, beginning of Chef, I was like, okay,

[00:18:08] **Audrow Nash:** Would that mean like I buy a product for my home kind of thing? Yeah,

[00:18:12] **Rajat Bhageria:** So I thought about, both you buy a product for your home and also you buy the end sandwich or burger or coffee, right?

So the product for your home idea, I didn't, I

[00:18:24] **Audrow Nash:** That one's hard and expensive. Yeah.

[00:18:27] **Rajat Bhageria:** One's hard and expensive and actually like I, I actually did a bit of a thought experiment with my friends. basically I posted them the question, okay, look, let's say you have two potential options. Option one is This like black box in your house and it's gonna make anything you want. I don't know how it's gonna work yet, but just assume it exists. would you rather have that or let's say option B is imagine a future where you know, we have the proliferation of robots that actually make the food, which means your food is like And, customizable than, essentially as customizable, as you would have in your house.

it's fast. It's probably cheaper, right? imagine that, these robots are in ghost kitchens. And so what that means

[00:19:09] **Audrow Nash:** they just output an order and it's delivered to you. They handle stocking. Okay,

[00:19:13] **Rajat Bhageria:** And it's probably cheaper as well. And

[00:19:16] **Audrow Nash:** Scale. Okay. That sounds great.

[00:19:18] **Rajat Bhageria:** of the scale, and then finally it's also delivered to you by a robot. So it's

cheaper 

[00:19:22] **Audrow Nash:** Ha Sounds hard.

[00:19:23] **Rajat Bhageria:** but what was interesting is like you can visualize that future, right? And what was interesting is every single person said option B, which is to say like they would rather, and what I asked about why, and they said look like it's because first of all I don't have to take care of a robot, I don't have to refill it, I don't have to clean it.

I don't have to pay for it. I would rather rent the food, if you will, than buy the food equipment. and, plus, I, get access to my favorite chefs. I, like my, the brands, I like, I, don't wanna have to give up those brands. And, anyways, like this thought experiment was a very quick thought experiment, by the way.

But it, it basically put a big dent in my head about at home robots. I became more and more convinced that actually,

[00:20:09] **Audrow Nash:** think that generalizes to, other, I, I suspect how you say it, that it probably does generalize.

[00:20:16] **Rajat Bhageria:** I think it does. a good example of this is clothing, by the way. back in the day, people used to make textiles at their house. A cottage industry, right? 

[00:20:23] **Audrow Nash:** Yeah. 

[00:20:24] **Rajat Bhageria:** but then over time, of course, we learned that there's efficiencies of scale, right? it's better to have a central factory near the water where you can make all your clothing and then you can buy the clothing.

so I think, I think it generally scales. you can imagine a future where a lot of the day to day stuff you do at home, you ship out, just like a ghost kitchen's kind of a central factory, if you will, you ship it out of your home. Because you have autonomous delivery, right? That's the key assumption here.

Autonomous delivery, ship it out to a central location, they do the processing and ship it back to you. even clothing, so like at, in big factories and industrial settings, like companies like Aramark and Cisco, like they basically, like the Smocks, those are actually cleaned in a separate facility and Aramark delivers them to like your restaurant or your plant every day.

It's, already a thing, right? So I think that analogy actually could work. There's certain things that need,

[00:21:20] **Audrow Nash:** that's, probably up and coming. I'm thinking even like delivery, laundry services kind of

[00:21:25] **Rajat Bhageria:** that's right. That's right. I think there's certain things that just need to stay in the house, like cleaning, cleaning, just, it's a fundamental, which is why like companies like Roomba have actually done well in robotics, But anyways, I, like all of that to say that I was less convinced about like selling robots to consumers.

I'm still, less than I think robotics is more fundamentally a B2B business. I just think that's what

[00:21:46] **Audrow Nash:** I agree.

[00:21:48] **Rajat Bhageria:** So unless you're the end consumer, right? So unless you're Tesla and you're building your own robots or, like Tesla makes their own robots for their own facility, right? But they're also selling to a factory if you will.

[00:21:59] **Audrow Nash:** Still B2B. Ah

[00:22:00] **Rajat Bhageria:** Still B2B. okay, so no to selling robots to consumers. Then the other idea is, okay, what if we actually made our own restaurant? Like what, Creator and everyone else has done? That also, it didn't really hold water for me. And there's a few reasons for this. just on the surface, it felt very much and we've all read Zero to One, right?

Like it very, much felt The perfect competitive market that Peter Thiel talked about. Like it's, a little bit better, but it's not that much better. And in another restaurant opens up down the street

[00:22:31] **Audrow Nash:** Yeah, it's just a

[00:22:33] **Rajat Bhageria:** out of luck.

[00:22:34] **Audrow Nash:** basically. Like it's not, you're right, maybe it's two times better or something, maybe two times faster or something, but it's not like that much and you have to wait, probably like lines and all the things to get to it, so it gets half, I don't know, twice as good, half as good because of the lines, and then it's about the same.

[00:22:53] **Rajat Bhageria:** And by the way, this, idea of making your own restaurant, it's it's built on an interesting foundation. So I actually, again, I interviewed a lot of robotics founders when I was trying to figure out what to do. it's built on a really interesting foundation, which is look, trying to deploy robots in other customers site is really freaking hard.

And the reason it's hard is that every customer does things a little bit differently. There's different, Ingredients for us in the food industry. There's different palettes in the palatizing industry, etc. So what if you could just control the environment? You have your own environment. You're your own customer.

it's Nolan Bushnell like selling, Atari to cheese, Chuck E. Cheese's, which he founded both of them. He, built Chuck E. Cheese's and he built Atari to sell to Chuck E. Cheese's.

[00:23:32] **Audrow Nash:** I didn't know that's so

[00:23:33] **Rajat Bhageria:** that idea.

[00:23:34] **Audrow Nash:** Yeah,

[00:23:35] **Rajat Bhageria:** So it's, and you constrain the environment. It's like you really

[00:23:38] **Audrow Nash:** there is the appeal. Yeah,

[00:23:40] **Rajat Bhageria:** Exactly. The technology problem is a lot easier, right? Which is, notable. But the issue I've learned from these same founders is what you called out, which is fair, and there's two others. Number one, even if you get the robots right, oftentimes it's really hard to get the food right.

[00:23:57] **Audrow Nash:** ah, yeah.

[00:23:58] **Rajat Bhageria:** just for example, like many, I won't call out names, but many companies face this, right? They made really cool robots, but then, consumers would buy the food and it was like, eh, fine. But I actually prefer, Domino's. I prefer Domino's. I prefer Starbucks. I prefer

[00:24:12] **Audrow Nash:** Whatever else.

[00:24:13] **Rajat Bhageria:** whatever else.

And then I, also learned that you're essentially stacking two businesses on

[00:24:20] **Audrow Nash:** exactly. That's what I was going to say.

[00:24:22] **Rajat Bhageria:** is very hard, and you have a food business, and you're stacking the probabilities.

[00:24:27] **Audrow Nash:** Yes, 100%. It's much harder. You have to be two CEOs at once.

[00:24:32] **Rajat Bhageria:** Yes.

[00:24:32] **Audrow Nash:** And I think one of the things also with this is it's a huge upfront investment because you have to get both businesses going at once.

[00:24:41] **Rajat Bhageria:** Yes.

[00:24:42] **Audrow Nash:** But to me, okay, we're going to talk more about what, you guys are doing. But if you guys want to scale to that in the future, you can gradually build up capabilities and you, so from that, you'll be in a much stronger position to automate the rest of it.

Cause you're basically doing one of these problems at a time, versus both at one time and requiring a huge capital investment, all at once.

[00:25:09] **Rajat Bhageria:** Yes.

[00:25:10] **Audrow Nash:** Uhhuh

[00:25:10] **Rajat Bhageria:** That's right. anyways, okay, the question is, okay, who do we sell to? So selling the robots to consumers is out. Selling burgers and sandwiches and, coffee to consumers is also out. Which, by the way, you've seen this in the industry, right? the people who try to build at home robots, they've all not done well.

The people who have tried to sell food, they've also not all done well, but most of them have not done well.

[00:25:34] **Audrow Nash:** Uhhuh . Yeah. I literally have not had any on this podcast 'cause I didn't like any of them before this. Yeah.

[00:25:40] **Rajat Bhageria:** Yes

[00:25:41] **Audrow Nash:** But

[00:25:44] **Rajat Bhageria:** So now it's okay B2B,

[00:25:48] **Audrow Nash:** Great. Okay, so your B2B, who do you sell? Who do you sell to in B2B? Or which, market? Segment of the B2B set of companies you could sell to.

[00:25:56] **Rajat Bhageria:** yes, so there's some interesting story there, too so when we first started our natural inclination was to really get on the bandwagon of delivery so Uber Eats was really picking up steam. This is, again, still pre

[00:26:13] **Audrow Nash:** Yeah. Actually, can you tell me the timeline of where we are when you started this kind of thing? Just. Broader context for

[00:26:22] **Rajat Bhageria:** basically, I started the company mid 2019, and this is when I was doing all this

[00:26:27] **Audrow Nash:** Just before COVID. Okay.

[00:26:29] **Rajat Bhageria:** Just before COVID, yes. And, yeah, so I, I, what I, what we were thinking about is, okay, delivery is really starting to take off.

And this is, again, from, empirical data from the customers. We, really tried to talk to, try to talk to the customers early on, before we even built

[00:26:49] **Audrow Nash:** And customers being businesses, right?

[00:26:52] **Rajat Bhageria:** at the time it was just food businesses, broad, super broad strokes, like any food business, let's talk to them,

[00:26:56] **Audrow Nash:** Hell yeah.

[00:26:59] **Rajat Bhageria:** Fast Casual was something that was very obvious, it seemed very obvious to us,

[00:27:04] **Audrow Nash:** Can you define fast casual? is that Chipotle? Or,

[00:27:08] **Rajat Bhageria:** it's Chipotle, basically.

Chipotle, Sweetgreen, Dig In, Kava, Mixed, Salad Go, any kind of place where you have the count It's the original guys here were like Subway, right? You have the original counter, and you're assembling the meal. the ingredients are pre cut and pre cooked. And you have a human who's assembling the meal into A sandwich, a burrito, a wrap, whatever, right? And, so what was really interesting here is that delivery was really taking off. Cloud kitchens were really starting to gain steam. And again, this is even pre COVID, but even pre COVID, 40%, 30 40 percent of volume was delivery orders, which was very fascinating. in other words, people were not going into the store and picking up their Chipotle or their Subway or their Dig In.

They were rather getting it delivered to them using, one of these aggregators like Uber Eats and

[00:27:58] **Audrow Nash:** Was that across the U. S. or in specific locations? I'm wondering, where

[00:28:03] **Rajat Bhageria:** guessing it was more of a coastal.

[00:28:04] **Audrow Nash:** Yeah, that's what I would

[00:28:05] **Rajat Bhageria:** it was one of the coast

[00:28:06] **Audrow Nash:** it seems like, in San Francisco maybe that's the case. but I can, I don't know, middle of nowhere farm country, I doubt this is the case kind of thing.

[00:28:15] **Rajat Bhageria:** That's right. and by the way, that changed after COVID, of 

[00:28:17] **Audrow Nash:** Yeah. 

[00:28:18] **Rajat Bhageria:** but before COVID, you are totally right. so anyways, we, like when we first started off, like we like, really thought about, okay, fast casual seems like a good go to market, right? And we actually and, I'm Cutting the chase to really answer your question about who we sell to now, we, actually got some early customers.

We got some early prototypes. we, that's how we raised some of the earliest funding we had. And, we, actually shipped some prototypes. At the time, they were just prototypes to our, one of our early customers in San Francisco. And, we're like, hey, customer, I'm not going to say the customer's name right now, but hey, customer, built a robot that can like flexibly assemble leafy greens for you. Is that useful for you? and, what we, realize is that, what we realize is that in a fast casual environment, that is not useful. And the reason it's not useful is Let's talk about an employee who works at, a Sweetgreen. Let's just say arbitrarily, right? It could be any fast casual chain, or a ghost kitchen.

The volumes are actually relatively low. It's not like you're making tens of thousands of meals. You're making a few hundred meals a day. does that mean? What it means is that the jobs are very generalized.

[00:29:41] **Audrow Nash:** You go down the whole line giving the items, not just one specific thing. Not just

[00:29:47] **Rajat Bhageria:** That's right. in other words, not just the leafy greens. in other words, if we wanted to say, Hey, Sally.

The store manager wants to say, hey Sally, I want you to do this other thing today. We have this robot that's going to do the assembly. for Sally to actually be able to fully leave, our robot needs to do 100 ingredients. Everything. And if we cannot do everything, then Sally cannot do, go do another task.

By the way, there's not a labor shortage. So there's, no risk of Sally getting laid off. It's just, Sally's going to go do something else. 

[00:30:19] **Audrow Nash:** you mean there is a labor shortage, so sadly he's not going to get laid off. I might have heard the exact opposite. Okay.

[00:30:24] **Rajat Bhageria:** There is a labor shortage. My bad. that's what I meant. so, this was really interesting, right?

So what I learned there is that in robotics to actually be able to add value to a customer, you essentially need to have at least a human equivalent. At least if you have less than a human equivalent. Like it's one or zero, right? If you have less than human

[00:30:45] **Audrow Nash:** In that specific domain, you're saying. In the domain of fast casual, this is what you're

In other areas too?

[00:30:53] **Rajat Bhageria:** I think it's at other areas too, right?

So the, place where this changes is if you have extremely high volume, right? If you have extremely high volume, then

[00:31:04] **Audrow Nash:** it.

[00:31:05] **Rajat Bhageria:** exactly, each of the roles are more specialized, but, even in that case, you still have to have a human equivalent. It can be any of the humans, but they have to have a human equivalent of the tasks they're doing, right?

[00:31:17] **Audrow Nash:** What do you mean human equivalent? I don't quite understand what that means.

[00:31:20] **Rajat Bhageria:** Okay, so so let me let me paint it this way like in fast casual Sally's got to do 100 gradients. If we cannot do the 100 gradients we have we don't have a Sally equivalent. In other words, I cannot go to this the I cannot go to

[00:31:36] **Audrow Nash:** Sally equivalent is a very funny way to put it. Okay.

[00:31:40] **Rajat Bhageria:** Yes, if I don't have that, then I can't go to this customer and say, Hey, you should pay me like you pay Sally, which is a salary. A robotics as a service salary. I can't do that because I haven't 

[00:31:53] **Audrow Nash:** You haven't done the

[00:31:54] **Rajat Bhageria:** offset Sally so she can do something else. Exactly. on the other hand, you have like more high volume production.

In high volume production, if you have somebody on assembly line, they're doing one task. Now, oftentimes in manufacturing for example, there's still changeovers. It's not like you're doing that, that one task 24 hours, or sorry, eight hours a day. Maybe you might be doing it for five hours and then doing another task with three hours.

There might be a changeover, but you have a couple tasks. A few tasks, right? So if I can have a system that does a few of those tasks, let's say five tasks, or five ingredients, in this case because it's food, then I have a Sally equivalent.

[00:32:33] **Audrow Nash:** In those tasks because it's high volume. So the distinction here, it's not the, fast casual dining. It's the volume because with higher volume, you have the ability to do specialization and this is where robots are beneficial.

[00:32:50] **Rajat Bhageria:** that's right. what we basically realized is, look, at the time when we were really focusing on fast casual, this is I'm telling you the sequential

story, 

[00:33:00] **Audrow Nash:** yeah, 

[00:33:03] **Rajat Bhageria:** it became pretty, it was like an interesting time. It's okay, we know this is a big market. It's arguably the biggest market for AI.

We know there's a big problem. We know that food assembly is the right thing to solve. we believe we have the right go to market, which is selling to other food businesses, as opposed to being the food business itself, or even selling the robots. We believe that, this technology is possible. we, believe that this all is possible.

And further, we even believe we have the right technology architecture, which is more of a pick and place, an AI based system, which is a lot more flexible than a dispensing, hard automation system. we're a little bit like, ah, we, we feel like we got all these things right. And yet, it's still not there yet, because we can't do 100 ingredients.

So then we started to ask ourselves, okay, how do we do 100 ingredients? What's the bottleneck, right? What we learned is the bottleneck is very simply just AI trading data, which is to say, the thing with food is that food is very highly dimensional, and it's very long tail. obviously, different ingredients are different than each other.

a potato mash is very different than diced chicken, and diced chicken is very different than shredded chicken, and shredded chicken is very different than a potato mash. Thin sauce. So obviously ingredients are different from each other. But the thing is there's also a lot of differences within the ingredient.

So that same diced chicken, it's being cut by a human being. So every single day it's going to be a little bit differently cut. And by the way, it's also being cooked by a human being. So sometimes it's going to be cooked a little bit longer, sometimes it's cooked a little bit less. Sometimes the cook's going to add a little bit extra oil, which means the stickiness is different.

In other words, it's a very highly dimensional

It's extremely variable. And by the way, this is not even to say anything organic, about the organic structure. It's a, organic material. So even growing it is different. to, to deal with this, AI, we learned, is just necessary,

[00:34:50] **Audrow Nash:** Because it's an edgy problem, like you spend a lot of time on edge cases, and because of this AI is better than like really hard coded rules, a more classical approach. Okay.

[00:35:01] **Rajat Bhageria:** that's right, you, I, that's exactly right. let, maybe another way, to express this is, let's say I wanted to make a robot that just does rice, right? It just, and it's not even just rice, it does, one particular kind of rice that a machine cooks the rice, and even, it, the machine does everything, so you know the input is exactly the same every time.

yeah, like I could hard code a system, maybe not hard coded, but I could have a rules based system, right? That, probably would do fine. 

[00:35:26] **Audrow Nash:** totally. 

[00:35:27] **Rajat Bhageria:** but now if I want to have a flexible system where like the inputs are variable every time and different customers make their rice differently, and by the way, they don't just have rice, they have trillions of other ingredients,

[00:35:35] **Audrow Nash:** And also,

[00:35:37] **Rajat Bhageria:** it's a little bit harder.

[00:35:38] **Audrow Nash:** sure, and but so with the way where you have the exact same rice every single time and it's made by a machine, that requires a lot more investment in infrastructure to have that machine to transport it to arrange it the exact same way every time. and so that's a bigger expenditure for the customers.

And so that would probably limit. The market that you could go after for this kind of thing. So having it be flexible makes it so more people can do it. You want to make it so you can try your robot, or deploy just one of them or something, have it at relatively low cost to the customer. They don't have to change their whole like floor plan or anything.

so flexible is way better for lots of reasons. I imagine, especially for the customer.

[00:36:25] **Rajat Bhageria:** that's a hundred percent true. And, actually the industry has a lot of what's called low mix Right? Automation. low mix is what you're saying, right? it, you're trying to make a system that does one thing. anoth an example from like electronics might be you're trying to make a line that is iPhone 15s.

That's all it's gonna do. If you're trying to do Macs on that line, it's not gonna work, right? 

[00:36:47] **Audrow Nash:** Yeah, I think of molding generally for this kind of thing where it's like you have one mold That's all it's going to make this kind of thing. You can make a bunch of them, but you can't change anything

[00:36:57] **Rajat Bhageria:** That's right. And the same thing is true in the food industry, by the way. So if I'm like Kraft Heinz, Kraft Heinz, for example, makes ketchup.

No, if you make ketchup, you don't have 50 kinds of ketchup, right? You have a few SKUs, right? So you're gonna go to a

[00:37:12] **Audrow Nash:** super low mix and high volume. Yeah

[00:37:17] **Rajat Bhageria:** integrator, you're gonna pay them 10 million bucks, but they'll make you a system that, perfectly makes those bottles of ketchup for you, given the same inputs.

Which is, which you can basically guarantee because you have a custom line, right? we were like, okay, look, back to the chef world, right? we had just done this fast, casual experiment, we're like, 100 ingredients. To add value to FastCasual. we can't do that right now because we don't have training data for 100 Ingredients.

And by the way, we can talk about that too. Why don't we have training data for 100 Ingredients? It's because, unlike something like a large language model, I can't just download the internet for training data, right? That's not possible. unlike a software and car company, or even like a company that's doing rigid body manipulation, palletizing, case packing, I actually can't use simulation because simulation really assumes Newtonian physics and non deformable stuff Whereas food is deformable, sticky, wet, malleable,

[00:38:18] **Audrow Nash:** all the things physics doesn't do well, huh or our current physics models in simulation

[00:38:23] **Rajat Bhageria:** physics. Yeah, exactly. So simulation also doesn't work. So then you're like, okay, you can bootstrap your data, right? You can like in a lab bootstrap the data, which is fine to get started, right? But of course as we talked about, given the highly dimensional nature of food and the number of ingredients And the fact that every customer, every, kind of, they're all different, like that only gets you so far.

I can bootstrap one ingredient or two ingredients, but I can't bootstrap a hundred ingredients. So we went back to the drawing board and we're like, okay, who else did we talk to in this search when we decided what kind of, customers to go after? and we stumbled upon, of course, Google.

Production Manufacturing, right? So initially, my impression actually was like, manufacturing, food manufacturing, that's already solved, right? Like it's, these, machines that we've, all seen growing up with how it works, right? These are traditional automation systems that kind of just do the same thing over and over again.

That was my impression. what I learned is that there's another really big market within manufacturing called high mix manufacturing. High mix is essentially, the opposite of low mix. Low mix is you can get these traditional pieces of automation, it's a Kraft Heinz example, and it's solved, low mix manufacturing.

High mix is a little bit different. So high mix might be like, I want to make, a prepared meal, and to make this prepared meal, I know that every human wants a little bit. Slightly 

different, stuff. Some people want meat lovers meals, some people are vegetarians, some people are vegans, some people are gluten free.

And within these, there's 30 kind of SKUs within each of these categories. what we learned is that there's this really incredible market, from a market size perspective, where, there's these companies that'll have hundreds of SKUs. And if you have hundreds of

[00:40:11] **Audrow Nash:** is an individual item or what's an SKU?

[00:40:13] **Rajat Bhageria:** like an individual meal, let's say.

[00:40:15] **Audrow Nash:** Oh, okay. What does it stand

[00:40:16] **Rajat Bhageria:** So each, 

[00:40:20] **Audrow Nash:** Is it an acronym?

[00:40:21] **Rajat Bhageria:** it probably is an acronym.

[00:40:23] **Audrow Nash:** But it's a meal. It's like an instance of a meal in a permutation

[00:40:27] **Rajat Bhageria:** yeah, like different cans of LaCroix or like SKUs, right? Different,

[00:40:32] **Audrow Nash:** different flavors you're

[00:40:33] **Rajat Bhageria:** basically like a identifiable product

[00:40:35] **Audrow Nash:** Ah, okay.

[00:40:43] **Rajat Bhageria:** okay, so it's okay, interesting. So what was interesting about these though is that because they have hundreds of SKUs, they are not gonna have hundreds of dedicated lines like the Lomix companies do. Instead, you're going to have way less lines, like 10 lines arbitrarily. And then you're going to do changeovers.

Which is to say you're going to go from doing pad thai in the morning, to thai green curry in the afternoon, to maybe doing a Mexican casserole at night. So the line is flexible, right? And so of course, as you alluded to, traditional automation doesn't work. And the reason it doesn't work is traditional automation is really designed, you bolt to the ground, it just does that rice.

And the rice robot is not, the rice machine I should say, is not then going to go do diced chicken. But of course, for high mix manufacturing, you need that, you need something flexible, you need something to go from doing You know, Paptide and Indian Korma too. TigerBeanCurry. traditional animation doesn't work.

So what I learned is that they use humans, and specifically the way that production works is that you have these long assembly lines, and these assembly lines are often in very cold rooms, 34, 36 degree Fahrenheit rooms, and essentially each person's on a station on the line, and with their station, they have an ingredient.

okay, I'm making the pad type. Person 1 is putting the trays onto the line. Person 2 is doing the noodles person and there's two lanes let's say so the person three on the other side of the light conveyor is also doing noodles then somebody's doing mixed vegetables etc what was really interesting from a technology perspective for us is that because it's much higher volume the jobs are much special much more specialized now sally if she were to work at one of these companies sally is on station three and sally is doing the broccoli Now, Sally isn't just doing broccoli for her eight hour shift, she might be doing, in three hours there's going to be a changeover, she's going to do something else, but probably Sally is doing five ingredients per day, right? 


## [00:42:33] Bootstrapping AI for Real-World Robotics

[00:42:33] **Rajat Bhageria:** ingredients I can bootstrap in a lab, I can bootstrap the training data, and I can get something good enough. To deploy something in the world, right? And this became our kind of like thesis, which is okay look, we believe that for robotics, like really embodied AI to work, you need real world training data.

Sim doesn't work, right? It could work for some industries, but food it doesn't really work. can't download the training data, there's no food manipulation data on the web. Bootstrapping only takes you so far, you really need real world training data. So it's okay, we're going to bootstrap something just to get something good enough to add value to these customers to do five ingredients.

If we can do five ingredients, we can ship something into production. If we can ship something into production, over time, we'll just see a lot more. Yeah, exactly. And by the way, if we get more data, then our AI gets better. We do better manipulation. What I mean by better manipulation is where, we're more consistent, we spill less, we don't damage the ingredient more, we are, we can do more portion size, we can place it in different compartments.

that's better manipulation. If we can do all of that better, then our robots Are more flexible. If our robots are more flexible than our current customers, like our current customer batch is gonna use those robots more. If our current customers have high utilization with their current robots, what are they gonna do?

They're gonna get more robots. So now we have even more robots. So we have even more training

[00:43:53] **Audrow Nash:** virtuous cycle. Yeah,

[00:43:55] **Rajat Bhageria:** it's a virtuous cycle. And by the way, now when I go to my next customer, there's a bunch of benefits here. First of all, I can probably already have a good. It's even better for them because I have a good starting policy of how to manipulate Maybe not all the ingredients are even because every ingredients their ingredients are slightly different, but I have a starting policy, right?

Probably I have a good case study from my existing customer, right? I might even have operation operationally some local people who can actually help service the thing So there's all these things actually make the whole flywheel just get better But of course the core of the flywheel is the data flywheel, right? So, we're like, ah Aha, this is what, this is the go to market, right? And, I just love to learn about startups and business. So I was like, it felt a little bit like we were trying to build a Model S before, which is like going directly to fast casual, right? I'm sorry, Model 3 right away.

And, now it's okay, really right now we just need to build the Roadster. And this is a

[00:44:51] **Audrow Nash:** Love it. Uhhuh.

[00:44:51] **Rajat Bhageria:** something that can like, get to market, add value, and we learn how to like, really build the technology. And we create this flywheel. And, but of course the vision was the same. The vision of Chef has always been, we want to deploy AI enabled robots in the food industry, period.

We wanna deploy AI enabled robot everywhere and, to every commercial kitchen, right? Because by the way, like the market needs that and the, the demand is there. and if somebody were to solve this, like the demand is

[00:45:16] **Audrow Nash:** Yeah. It would skyrocket inval. Like you could, you have a huge market you could just gobble up.

[00:45:22] **Rajat Bhageria:** That's right. 


## [00:45:23] Expanding to New Markets and Applications

[00:45:23] **Rajat Bhageria:** So it was like, okay, how do we then think, okay, we, we started here, we started with the model three. We'd like to go back there at some point. We're right now where the road are. And then we're like, okay, we have to connect the two dots. And, what was really interesting is, of course, if I can manipulate diced chicken in a food factory, why can't I do it in a ghost kitchen?

And if I can manipulate diced chicken in a ghost kitchen, why can't I do it in a fast casual, right? Manipulation is manipulation. The hard part is manipulation. The grasping. That's the hard part. everything, there's other issues, by the way, right? Like form factor, there's other issues. but those are engineering issues that can be solved.

The thing that's like the hard thing is the manipulation, right? So we're like, huh. So not only are we, do we have this flywheel within manufacturing, which is like the more robots we deploy, the better the system gets, but that same training data and that same AI can then be used to go to step two.

Step two

[00:46:12] **Audrow Nash:** Yeah, exactly.

[00:46:12] **Rajat Bhageria:** Go's Kitchens and Cloud Kitchens.

[00:46:14] **Audrow Nash:** Hell yeah. Yeah. That's what I was meaning where it's you guys can just do, you start with five products and then eventually once you have scaled up to a hundred products or 500 products, then you can maybe then open your own kitchen and you have the robot worker part solved. It's but and then.

On the way to going from robot serving five things to robot restaurant, you can serve all the things that are in between, which is the rest of the food industry. So it seems like a good growing plan to me.

[00:46:48] **Rajat Bhageria:** Yes. Yes, exactly. So like right now we're focused on food factories, big giant food

[00:46:53] **Audrow Nash:** Oh yeah. Might as well.

[00:46:54] **Rajat Bhageria:** step is exactly, next step is regional food factories. Regional food factories would be cloud kitchens, ghost kitchens. These are smaller, they're aggregations of restaurants.

By the way, they are essentially factories, they have a lot of real estate, and they're delivering delivery orders, so it is a food facility, it's just smaller than the ones we're going after right now. Lower volume, right? And then finally, we get to, if you think about right now we're like, we're You know, relatively, we're low mix on the relative scale to restaurants, but very high volume.

And then, as we go to step two, the mix gets a little bit higher, the volume gets a little bit lower. And then finally, when we get to commercial kitchens, the mix is back way at the top, but the volume is way, lower again.

[00:47:42] **Audrow Nash:** Oh yeah. That's super

[00:47:43] **Rajat Bhageria:** So that's that's what we're thinking about

[00:47:45] **Audrow Nash:** Yes. And I would think if we're sticking with the like model S to three, then you opening your own restaurant, that can be your Cybertruck

[00:47:54] **Rajat Bhageria:** RoboTaxi.

[00:47:55] **Audrow Nash:** or the Robotaxi, yeah, okay, hell yeah. So that sounds really cool. getting the data is very clever and you can train on that.

And I think just to make it a little more explicit or make sure I understand. So you're getting training data on these five items that now are you're in production and you're actually adding value for a customer. now you're recording all of that data and you are then using that to train. better general policies that you can use to bootstrap additional things.

is that, kind of how it's working where it's, and then you can do, you can add another five items or whatever it might be.

[00:48:37] **Rajat Bhageria:** yes, that's, right, exactly, right? I think, like, where we really started is, if you think about a meal, right? 


## [00:48:46] Challenges in Food Manipulation

[00:48:46] **Rajat Bhageria:** The majority of the meal is what you might consider like scoopable right in other words that you can use your hands or you can use like something like a scoop like an ice cream scoop or something to pick it up and that's like things like starches like rices and pastas and things like that then you have things like different meats right it can be like diced meat or shredded meat or Pulled meats, things like that.

Then you have different kinds of vegetables. Of course, there's lots of different kinds of vegetables, different combinations of vegetables, but they're always usually cut in some way. Then you might have a garnish, right? You might have something like a spice, or you might have like more vegetable toppings, something like that. Maybe you have a sauce, maybe you have something like a mash, right? All of these are scoopable. They're very different, by the way, shredded meat is very different than a cheese, and cheese is very different than a sauce, and a sauce is very different than, than broccoli. They're all very different, but they're all like this, you can imagine an idea where, a camera to understand where do I pick from and where do I place, A 6DoF arm with the right, manipulator at the, the right, utensil

[00:49:54] **Audrow Nash:** An appropriate manipulator. Yeah.

[00:49:57] **Rajat Bhageria:** the combination of computer vision, motion planning control, the right robot policy, motion pilot policies, and the right utensils can hopefully build a general policy on how to manipulate food. And the more of these ingredients it sees, and the more, it's basically breath. different ingredients and also depth.

Like, how many of those, the same ingredients used over and over. you can make a system that's very flexible, but of course it's still got to be very consistent. I think consistency is the hard part here, right? It's gotta, it can't be picking up, if the, if it's a one ounce portion, you can't be picking up three ounces one time, zero ounces the next time, half an ounce the next time.

It's gotta be, like, basically very close to three ounces over and over.

[00:50:38] **Audrow Nash:** Okay, so this, to me, this sounds like a very hard problem and it also sounds hard to get your, so you are getting data and I understand in the abstract how more data is improvement, and you've mentioned so robotic arm appropriate gripper and you're using mostly computer vision and that lends itself from your background which is really great, how is that the only, is vision the only sensor you're using other than maybe like joint torques or something like this?

and then like, how do you, annotate your data? How do you establish what was good or what was not good? how do you use production data in actually training the system to, do what you want it to do? Like, how, do,

[00:51:34] **Rajat Bhageria:** yeah. It's a,

[00:51:35] **Audrow Nash:** go ahead.

[00:51:36] **Rajat Bhageria:** there's a, lot there, and all very good questions. one thing that's really interesting is that most of our team is from the software and car industry. So we have, the vast majority of our team is from, Cruise, Neuro, Zoox, Waymo, Embark, and all these different AV companies and of course like what you essentially ask is what AV companies are very good at.

They're very good at like Annotation and pipelines and, testing and test infra, right? So essentially, okay, so let's, start at like where we started. So the first step, of course is having the right metrics. So what are the relevant metrics? So consistency is one of the main metrics. So how do you measure, and that's consistent with weight, right?

The way, by the way, And this also gets to your sensors question. of course, we have RGBD. We have a couple of RGBD sensors. we also use force torque,

also have weigh scales, essentially like scales, right? and so the way this kind of works is that what we can do is we say, okay, we have a topography.

Based on this topography and the ingredient I'm picking, And the other sensor data, inputs I have, where, what pose do I pick at in the pan to be consistent? And again, that'll take into consideration a bunch of stuff. Like all, like the entire robot policy, it'll take into consideration any fine tuning the robot did before the production run started, which the robots fine tune themselves.

Like it'll pick and dump to fine tune itself before the production starts. 

[00:52:59] **Audrow Nash:** cool. 

[00:53:00] **Rajat Bhageria:** account. Yeah. and that's because there's so much

[00:53:03] **Audrow Nash:** You're calibrating. So you have, like your base layer of understanding, but then it's going to fine tune the network a little bit by picking and dumping just a few times to be like, okay, let me get the consistence of this. That's so funny.

[00:53:15] **Rajat Bhageria:** it's a very practical, it's a very practical thing, right? Because every batch of food is a tiny bit different. It just

[00:53:20] **Audrow Nash:** Oh, definitely. What a funny thing. Okay. I've seen people do that too. if you see like people waiting, while they're whatever, they'll pick and scoop whatever. And it's like, they are calibrating in some sense and that's so funny the robots doing that. Okay, so cool.

[00:53:38] **Rajat Bhageria:** so then basically now, we have, we've figured out, okay, what pose do I pick at? We'll execute a pick, and then of course what our scales do is they're take away scales. So we can measure the weight lost from the pan of food. They're underneath the pan of food. So we measure the weight lost.

What that allows us to do is close the loop. Okay, we, based on based

[00:53:57] **Audrow Nash:** you're making your own supervised training data basically because you have that scale and it's all weight driven Interesting.

[00:54:05] **Rajat Bhageria:** so that's one, metric, right?

[00:54:07] **Audrow Nash:** Yeah, okay.

[00:54:08] **Rajat Bhageria:** That's one. So it probably arguably one of the most important ones, but that is one of them. so weight is one. another thing we think about is like placement, right?

So like what, what we do is we have a, a neur network that basically does like the before and after. It's kinda qa. So we like, it's part of our product. So what we can do is we, we. We say, okay, look, we like the food to be distributed like this, whether it's in a clump, or maybe it needs to be spread out, or whatever the customer wants.

The customer can actually we give them a nice web app where they can say how they want the food to be placed,

[00:54:40] **Audrow Nash:** That's so cool. And they're like I want it dispersed like this or mushed or like a Perfect All that looks like the

[00:54:47] **Rajat Bhageria:** yeah, or in this compartment, or whatever else,

[00:54:50] **Audrow Nash:** Okay, that's really cool.

[00:54:51] **Rajat Bhageria:** Yeah, and then of course what we can do is use it, we can have a before and after, right?

And then we can give a scoring to that. So like how good was the deposit from a placement perspective? So that's another metric. We have the placement quality basically, right?

[00:55:04] **Audrow Nash:** you just look at like the difference in the before and after image and then you assume that's what was placed and then you evaluate that based on some intended placement, 

[00:55:16] **Rajat Bhageria:** There's a bunch of different ways to score it and different customers care about different things, right? But we have depth as well. So we can see, okay, like what does the mound look like? Or may, maybe they care, may, maybe they care just about look, we want the entire thing to be covered.

there's different ways to score it, but there's some score we assign for the placement for that customer, right? so that's metric too. The third metric we look at is, throughput, because of course it needs to be fast. if it's not fast, then honestly it's not great. 

[00:55:43] **Audrow Nash:** Yeah. 

[00:55:44] **Rajat Bhageria:** so that's another metric we look at.

another metric we look at is. This is just core reliability. And reliability, there's many dimensions to reliability, but, some to call out would be things like missed bowls. Did we, detect a bowl, but we couldn't place into it? for whatever reason. did we do a double deposit where we tried to place twice?

did we, 

[00:56:05] **Audrow Nash:** These are bugs, basically.

[00:56:07] **Rajat Bhageria:** yeah, basically bugs and reliability. Did we try to accelerate so fast that we use collaborative robots? Did the robot protect us? Stop. and so that also gets taken into consideration. So anyways, we have metrics for the most important things our customers care about, and all of that's considered when you're making this policy to, To make sure that like you don't get a system that's flexible, but then like it's super slow or it's flexible But it's spilling food all over the place or it's flexible But like it's super ugly when you place it, right?

[00:56:36] **Audrow Nash:** huh.

[00:56:37] **Rajat Bhageria:** All of these things need to be taken into consideration and then you know the final part of your question was like, okay the data annotation and stuff a lot of it's automated, so we've built a lot of tooling to do this. So if there's a high weight event, we wanted x, and after some sigma standard deviation, we'll automatically annotate, we'll automatically annotate that and say, oh, this was a high weight event, let's collect a, we use ROS, so let's collect a ROS bag of all the information, like a little bit of the information before and after.

along, and now we can debug it, right? And all of that, we have a data pipeline that's all, as soon as that event happens The robot, will send that rolling recorder to the cloud. And then we have a nice interface where, we will get, an alert on, our on Slack, and if it's a P zero O or L zero alert PagerDuty.

then the, the person on call, the customer support person on call can, if it's really kind of production downtime impacting, like they can, They can actually like triage that so so that's I talked about the support process But that same thing is used with ML too, right?

Because if there's issues like we've automatically annotated everything

It's one in the same process like it's just it goes different places like one's

[00:57:59] **Audrow Nash:** Yeah, for sure. Makes sense. Yeah, you take the data, you route it both places. That's pretty cool. Yeah, I like that quite a bit. That's, so you're getting your data, and then You do the scooping to fine tune. is there any trick involved with going from, you're going from, you try to probably sequence what you, the food that you work on based on its similarity with the past foods that you've trained on, so you don't go from, like, all rice to shredded chicken or something that might be a big difference.

how,

[00:58:37] **Rajat Bhageria:** In terms of like our own training

[00:58:39] **Audrow Nash:** yeah, so in terms of, so you support five items, say. if you're going to add item six, you probably, if you did like rice and a bunch of other small grains, then you probably don't want to go to shredded chicken or broccoli or something like this. That's a big departure from it. how do you sequence the items you add?

[00:59:02] **Rajat Bhageria:** yeah, so it's actually an interesting question. this is actually if it was a, if it was like perfect world we'd do exactly what you're saying. But the thing is like now that we're in production, like again, this is a sequential story. Now that we're in production, we have a customer who's paying us money.

We have to do what the customer wants.

[00:59:19] **Audrow Nash:** yeah.

[00:59:20] **Rajat Bhageria:** So what the customer wants is the ingredients that are the toughest for their people, right? So and this was interesting, right? we learned that like risotto, which is a very thick viscous material It's like really hard because

[00:59:31] **Audrow Nash:** is that like cheese? Risotto means cheese, right? Or is it a cheesy rice? Okay.

[00:59:38] **Rajat Bhageria:** It's very dense basically, right? So it's like a very, it's like a hard, like your arms are hurting, your back's hurting, right?

[00:59:43] **Audrow Nash:** Do a lot of work to do to pull through it. Okay.

[00:59:45] **Rajat Bhageria:** For example, right? My point is that like Sometimes we didn't have, we, it's like a, it's a negotiation. Hey customer, we've done your basmati rice. How about we do your brown rice?

The customer is no, I, you, I know you can

[00:59:59] **Audrow Nash:** the brown

[00:59:59] **Rajat Bhageria:** I want you to do this, and, so it's, a negotiation, which of course isn't great from a purely technology perspective, because like you said,

[01:00:07] **Audrow Nash:** you would want a sequence. Yeah.

[01:00:09] **Rajat Bhageria:** you would want to sequence it, but sometimes you're not able to.

You as an early stage startup, you take what you can get. 

[01:00:16] **Audrow Nash:** Makes sense. So then you, what, you probably do then is you take whatever the material they want and you can bootstrap something with it and that gets you working good enough. and eventually maybe your learned scooping policies will be general enough to work with a lot of things, but you're bootstrapping specific things that you need to work.

[01:00:38] **Rajat Bhageria:** the way we thought about it is and again, this is it's changed through the years, right? Like per class, we'd have like policies, right? right? If you will, a class of food, like a mash is a class of food, and it's a very different class

[01:00:50] **Audrow Nash:** how technical, I just, talking to you about this, I don't know very much about the food industry, but having you, and you not being a food person, but you've come in and you are dissecting it, and you have this, I don't know, semantic understanding of,

[01:01:05] **Rajat Bhageria:** It's like a

[01:01:06] **Audrow Nash:** yeah, exactly, It's so funny.

But okay, so you have your mashes, and, all these other

[01:01:12] **Rajat Bhageria:** And they're very different than. Exactly. we basically had like different policies per class and it was an, it was like an inheritance tree almost, right? So like within a mash then you could have like, a cauliflower mash is probably pretty similar to a potato mash.

I just made that up, but you get the point. So that was good enough to get started, right? like you said. And then, of course, as you run it more, more matches, you see more pulled chicken than, or pulled meats than, your entire policy gets better. And then over time, what we're trying to do, of course, is to have more of a generic, a unified policy, right?

And, of course, that's where things like diffusion policies, and, exactly. And, by the way, the new stuff, right? The diffusion policies, and learning from demonstration, and all of that work is really important for that.

[01:01:57] **Audrow Nash:** Ah, okay. I would like to talk about that more later. Let me write it down. Yeah, learning from demonstration and all that. It's very interesting. 


## [01:02:06] Leveraging Learning from Demonstration

[01:02:06] **Audrow Nash:** Are you guys using learning from demonstration? Is that how you're bootstrapping?

[01:02:11] **Rajat Bhageria:** at the beginning, no, because that didn't exist. 

[01:02:13] **Audrow Nash:** because 

[01:02:14] **Rajat Bhageria:** but more,

[01:02:15] **Audrow Nash:** pretty early, although there are some pretty compelling research results lately, although I don't know all the caveats to the demos that I've seen and things like this, and I keep finding more when I look, but

[01:02:27] **Rajat Bhageria:** In the early days of Chef, like in 2019, 2020, this wasn't really, obviously it existed, it wasn't really good, right? Imitation learning wasn't really, if, imitation learning felt like reinforcement learning, which is yeah, we're going to do it, but I didn't, I, honestly, I hadn't really heard of companies who had productionized, right?

RL or IL. Yeah. as of late though, I think I think there's a lot more exciting work. So what we are doing now is if we're trying to onboard a new, a completely new class. So I'll give you an example. we are now, we've now productionized. Yeah. Actually even more interesting, like we're doing, picking like one chicken breast, that, remember I talked about like a meal, It has all these like different ingredients. Sometimes at the top there's like a piece of meat, right? A piece of salmon or

[01:03:18] **Audrow Nash:** delicious. Yes.

[01:03:21] **Rajat Bhageria:** yeah, so, before, we'd have to like, bootstrap and then get production data and there's this whole thing you gotta do to like onboard a new class that takes some time.

with LFD and IL, that, that time is a lot shorter

[01:03:36] **Audrow Nash:** demonstration and what was that? What's IO?

[01:03:39] **Rajat Bhageria:** imitation

[01:03:40] **Audrow Nash:** Imitation learning. IL?

[01:03:43] **Rajat Bhageria:** you can have, Yeah, you can have 60 or

[01:03:48] **Audrow Nash:** You can

[01:03:48] **Rajat Bhageria:** 70 demonstrations, you can speed it up much faster. like you said, it's definitely newer, but I think we're finding some good results there as well.

we're, thinking that's actually going to be a really powerful way to, really, really accelerate that flywheel.

[01:04:02] **Audrow Nash:** That's

[01:04:03] **Rajat Bhageria:** Because we already, and by the way, the, to do learning from demonstration well, it's a combination of the demonstrations and production data now.

It's not just the, it's not just

[01:04:11] **Audrow Nash:** Oh, you have your own demonstrations. That's super, super cool. Yeah. So you can choose a more stable algorithm or something because you have all of your data from your robot actually doing it.

[01:04:23] **Rajat Bhageria:** And it's labeled, it's 

[01:04:25] **Audrow Nash:** and it's supervised. Yeah. Oh, that's a super cool thing. What do you think? So in the recent learning from demonstration work, I haven't looked into it too much. What's changed?

Why is it better? Is it, like all this transformer? Are we using transformers? And is that why it's great now? Or what's, happened?

[01:04:43] **Rajat Bhageria:** I think, transformers are quite powerful. so I think, yeah,

[01:04:47] **Audrow Nash:** that is it. Okay. I didn't actually research into it, but transformers, as far as I understanding, give a better weighted look back at context from the past.

is that a fair

[01:04:57] **Rajat Bhageria:** yeah, exactly. Exactly. And I think it, so I think there's, I think transformers are really helpful because you have better, it's using, it's, called, it's a diffusion policy, right? So it's similar to the same, it's similar to the technology that, something like a Sora might use, or Obviously, DALI might use.

It's like you're generating an image right here, you're generating a policy and predicting like the in joint space like where what the joint show of the robot should be, right? I think the transformer certainly helped. but I think it's it's really a bunch of things coming together, right?

I honestly it's like GPUs are also getting better and processing. I think the VR technology, to be actually able to train, do the demonstrations getting better. I think there's a bunch of things, but I think, yeah, like the pivotal thing would probably be transformers and diffusion as an idea of really becoming a thing.

[01:05:49] **Audrow Nash:** What a thing. Okay. Yeah. It's amazing. I do feel like, robotics is changing. Like the technologies that we use as an industry. are really gonna the next 10 years is going to be different than the last 10 years and i know that kind of seems obvious but it's just it's like a lot of the things i even learned in school which is not that long ago i was in school five years ago or something like this are not used anymore and we have different methods for doing things It's crazy.

some of the low level stuff, say, ASTAR or something, we still use that for navigation. more optimal planning in some state space or something, if it's small, or RRTs or something. But, a lot of these perception and manipulation tasks, 

[01:06:34] **Rajat Bhageria:** Yeah. 

[01:06:35] **Audrow Nash:** they just seem, it seems like these, imitation learning and all the machine learning and AI, it's like they're fundamentally different approaches, and they enable a lot more performance and handling of Less Structured Environments.

[01:06:54] **Rajat Bhageria:** Yes. And, it's, really interesting. So like I alluded to, most of our team is from autonomous vehicles. I'm like, honestly, I'm not the expert as much as they are, right? the AV industry went through this, right? Which is like the AV industry for a while is very much rule based, right?

Like you detect red light, right? And then you stop, right? Or you, detect the car and then you track the car and then you make sure you don't like, when you're doing a lane change, you don't collide with the car. I'm simplifying, the point. it's very much rules based. But then what happens is that like the world is, highly dimensional.

It's confusing and then you have all these like It's just an extremely kind of wrangly code where like it's like all these rules, right? And like of course you can't get to every edge. And by the way, there's still a lot of machine learning It's a lot of machine learning, but it's like rules like it's you know, detect the red light and then

[01:07:45] **Audrow Nash:** Yeah, it's the machine learning is a lot of time for waiting things not for changing policy like changing what it does per se

[01:07:54] **Rajat Bhageria:** And that same thing was true for us, right? So we started off that way, right? Because that was what the industry did, right? And if you're doing robotics in 2020, of course that's what you're going to do. That's what everyone does. and, I think that was fine because it got us started.

But I think, what you find is that you have these like very gnarly policies. Like our, policy at that point is like 200 parameters, right? Just to manipulate an ingredient.

[01:08:18] **Audrow Nash:** Yeah.

[01:08:18] **Rajat Bhageria:** that works fine. but then the. The, the customer, like you go from like customer one to two, and customer two has the same kind of, let's say, cucumbers.

Yeah, but, and exactly. And you can have this inheritance idea, but it's, different.

[01:08:37] **Audrow Nash:** Yeah I think a lot of times with this You make a design architecture and then you find out by some awful exception that you need data routing from one spot to another where you didn't intend and it's incredibly painful to get it and then the whole thing becomes a hairball if you would do it or you have to redesign which is painful especially if you have your 200 conditions.

So yeah, whereas this you just learn and it learns all the connections for things and you don't have to worry about that hairball of and

[01:09:09] **Rajat Bhageria:** And I think one thing, I think I think I, at least from what I've understood, a lot of the AV companies are also like now going in this direction, 

[01:09:17] **Audrow Nash:** Yeah, 

[01:09:18] **Rajat Bhageria:** I think Wave, for example, Wave, I think, in, they, just raised a big round, and for a while, this end to end learning idea was like, I don't know, people are very skeptical about it, and people still are very skeptical about it, I think

[01:09:31] **Audrow Nash:** I still have plenty of skepticism about it, but I think there's a lot of potential too for specific problems.

[01:09:38] **Rajat Bhageria:** And I think Tesla FSD 12 is like one interesting example of like many people, many friends have mentioned that they like, really FSD 12, and that's 

[01:09:46] **Audrow Nash:** Is it the current operating

[01:09:48] **Rajat Bhageria:** that's the new one, and apparently that's the one where they

[01:09:50] **Audrow Nash:** It is self driving. It's at some level.

[01:09:54] **Rajat Bhageria:** but apparently they actually they cut 300, 000 lines of code and they're really using imitation learning to actually

[01:09:58] **Audrow Nash:** it's crazy. Yeah, what a cool thing. I can't wait to, to try it because I see great things about it, but okay. So yeah, and that's an end to end approach pretty much, I think, 

[01:10:11] **Rajat Bhageria:** That's right. That's right.

[01:10:12] **Audrow Nash:** You have code to hook up stuff, and then the rest of it, like the policies probably, mostly learned.

[01:10:19] **Rajat Bhageria:** that's right. And what's, nice, by the way, is that we can do, I, think the winner, I, really am convinced about this now more than ever before, is the winner in AI plus robots is going to be the companies that have the most production data. you can and should use Imitation learning, like that is useful to get started,

[01:10:38] **Audrow Nash:** Yeah, but it's a

[01:10:38] **Rajat Bhageria:** But at the end of the day, it's really good for bootstrapping, but at the end of the day, every, in our industry, like food, it applies for really any robotics problem, but in the food industry, every customer is gonna have different broccoli. They're gonna cut it differently, they're gonna cook it differently.

It, it gets you started, but you just simply need to deploy lots of robots at lots of customer sites. And by the way, different, within the same customer, different customer sites are going to do it differently. And, so you just need a boatload of robots in the world to really have enough data to actually make this all, really work too well together.

[01:11:09] **Audrow Nash:** Yeah, it's a really interesting approach. And it's, the, challenge that I think it becomes is how do you grow your company through the stages as you are collecting data and automating more and more of the process? Because you have to find the clever, low impedance way to grow your company because you can't go let me go nothing to solve all the way and I'm going to deploy all this money and lose it all to just try to see if I have market fit or something like you have to gradually grow and

[01:11:42] **Rajat Bhageria:** By the way, 

[01:11:43] **Audrow Nash:** what 

[01:11:44] **Rajat Bhageria:** you said, something really interesting, right? Which is basically You essentially called out the Cruise and Waymo approach, which is let's raise tens of billions of dollars And let's like just jump to the end goal versus the Tesla approach, which is hey, let's just ship a vehicle It's not gonna have any autopilot and over time we're gonna have billions of miles of FSD and like Hopefully one day, like we have a really good autonomy system.

[01:12:08] **Audrow Nash:** you're right yeah I didn't mean it intentionally but yeah I think that is a good it is the different stories that you see there.

[01:12:16] **Rajat Bhageria:** exactly.

[01:12:17] **Audrow Nash:** huh. And it's also you guys, it's Electric Sheep. you and Electric Sheep, to me, are taking a very similar approach, which I think makes a lot of sense. of just getting lots of data, deploying out there, starting as simple as possible, but then growing into complexity.

[01:12:33] **Rajat Bhageria:** That's right. That's right. And, yeah, I'm, getting, I think for startups, look, if you're like there's certain companies who can do the Waymo approach. But, I really think for startups, like you, you like you said, you have to find what's the Uber black, right?

what's the thing that you can get to market or what's the roadster or what's the. Microsoft, MS DOS, like with some, like the

[01:12:58] **Audrow Nash:** start up that flywheel.

[01:13:01] **Rajat Bhageria:** start up that flywheel. what's the Amazon, selling books on the, 

[01:13:05] **Audrow Nash:** Yeah, your entry point. Your beachhead or whatever, to the rest of it.

[01:13:09] **Rajat Bhageria:** That's right.

[01:13:09] **Audrow Nash:** The thing,

[01:13:11] **Rajat Bhageria:** and then you have to grow that, but while also telling the story, because from, a fundraising perspective, like Uber Block honestly is not that exciting. Like another taxi service for like rich people is not that exciting. Yes,

[01:13:23] **Audrow Nash:** Is that where they started? Okay, I didn't know. I don't know much of this history, but okay.

[01:13:27] **Rajat Bhageria:** basically had it was literally a limousine. It had people wearing like a nice like suit. It was like super high end, right? But it allowed them to get started, and wealthy folks in San Francisco used it. But over time, of course, they built UberX. They built UberPool. UberX and,

[01:13:45] **Audrow Nash:** and that's Tesla.

[01:13:46] **Rajat Bhageria:** a hundred billion and

[01:13:47] **Audrow Nash:** It's interesting because in my mind Like, okay, there, I bet there, so I guess there is nuance in this and that there are very different ways of starting this. You can do the Uber Black or you can do the Tesla approach where you go for the luxury markets and that's a way of spinning up production.

you can go, it's like the project you're doing, as far as I am aware, it's not like the luxury and food part. It's a very pragmatic, Useful part of the food preparation one. you have Amazon with their sending books by mail. That's very, that's not very, I guess maybe that's rich, richer people that are reading and want access to their books.

But I guess it's

[01:14:27] **Rajat Bhageria:** I guess what, it's not,

[01:14:28] **Audrow Nash:** finding your market initially that is a low investment.

[01:14:33] **Rajat Bhageria:** I think it's finding the people. It's not even like wealth per se, but it's like finding the people who have like big pain points. So in the Amazon use case, It like, what I mean by that is like in the Amazon use case, like the, pain point they were solving is If I want a long tail book, right? if I want like the, if I were to rank, rank books, if I want the 10, 000th most common book, In the, 

[01:14:56] **Audrow Nash:** not in any bookstores. Yeah.

[01:14:58] **Rajat Bhageria:** yeah, exactly. and I live in like Omaha, Nebraska. Like I probably can't go to the bookstore next door and find that 10, 000th ranked book.

But Amazon's kind of clever insight was if I can aggregate all the books into a central warehouse, then I can have 20 copies of the 10, 000th ranked book. Oh, you can have all the longtail ones. So it was like solving like a big pain point for like book readers, which is like I want this long tailed book and now with the internet I can take advantage of it, right?

I think for Uber Black, it's it's a, different analogy, but it's okay it's

[01:15:30] **Audrow Nash:** would pay for this? Rich people who

[01:15:32] **Rajat Bhageria:** would pay for it? That, yes. And I think for Chef, it's given the technology available today, which, what's the market that has the biggest, again, hair on fire problem where I can actually add value, which is food manufacturers?

[01:15:46] **Audrow Nash:** Hell yeah. That seems great. Let's see. And so just, the last part of the picture that I don't really understand, or I guess, has have some ambiguity around. So the end effector or end effector to the robot, it's mostly a scoop, but you're looking into like pinch grip or something. So you can pick up chicken or different meat

[01:16:08] **Rajat Bhageria:** Yeah, it's a good, it's a good question. So the way you can think about it is let me talk to you about what it is now and like how we think about it. so each robot, so each of our systems, we make modules. These modules are basically the exact same hardware. Every single customer, without exception, has the same hardware.

That's like a hard and fast

[01:16:27] **Audrow Nash:** Love it. That's so much

[01:16:28] **Rajat Bhageria:** we don't want to make maintenance, that's how you have, that's how you build a scalable

[01:16:34] **Audrow Nash:** And also your data, like it makes it easier for you to train your data because you all have the

same setup. 

[01:16:41] **Rajat Bhageria:** It's, more homogenous, like you said,

[01:16:43] **Audrow Nash:** You need a good

[01:16:43] **Rajat Bhageria:** a geometry perspective.

[01:16:45] **Audrow Nash:** probably for oh, you want to swap your sensor or something like that. I'm actually, I'm very curious to how you solve that problem, but I'll ask that in a bit. okay.

You have this homogenous setup. Yeah.

[01:16:57] **Rajat Bhageria:** the same, it's the same footprint as a person, and then, from an end effector perspective, we, each of our robots, without exception, has the same actuator. Actuator as in the pneumatic actuator itself. And then that actuator has different, has an interface, and on that interface, we have a set of different utensils, and we have a library, essentially, of different utensils, and this library, what's interesting about this library is that, It scales very logarithmically.

In other words, there's, like I said, there's trillions of different ingredients, and the way that a particular ingredient was cut and prepped yesterday, it will never exist in human history probably ever again. That particular way, right? But that doesn't mean you need thousands of end effectors and thousands of utensils. We have a small class of utensils, we mass manufacture them, we have patents around all of them, that's it, right? we send the entire library to our customers, so each customer has an entire library, each customer gets the same hardware, each customer has the same code base, software, and then of course there's different policies based on what you need for your ingredients that you're actually manipulating.

[01:18:02] **Audrow Nash:** Yeah. Okay. So almost everything is the same, except the end effector may vary with the food and the policy varies with the food most likely. And so that lets you control a lot and you get to reuse a lot of the same code and everything like this, and then you just

[01:18:21] **Rajat Bhageria:** It also means that it can evolve, 

[01:18:22] **Audrow Nash:** it 

[01:18:23] **Rajat Bhageria:** brain gets better. The brain gets better. if you have too much bespoke stuff, it seems like, sometimes we'll talk to our customers and we're like, ah, you're, like, They're like, oh, you're not making me custom stuff.

But no, that's not, that's the whole point. The fact that it's not custom means that it's, your thing's gonna get better literally every

[01:18:43] **Audrow Nash:** Yeah, that's so cool. What a funny thing where it's no, Because we do this generalization, we are able to benefit from everything that occurs. And, that's really nice.

[01:18:56] **Rajat Bhageria:** Yes.

[01:18:57] **Audrow Nash:** How do you, so what's your, do you have a plan for how to upgrade your hardware? So if say, I'm sure you basically, you did a ton of research before.

So that you could lock in and feel confident, look at the supply chains, look at the cost, look at the ecosystem and the support. So lock that in a really good one. But a painful thing that I have not yet seen a very good answer to, is the eventual process of upgrading. So you have, yeah, it's five years later and a new camera comes out.

And I guess Maybe you can mix the fleet or something like that or something or provide actually probably just put both on and then you can relate it but do you have a do you have a good upgrade story yet or what are you

[01:19:46] **Rajat Bhageria:** Yeah. Yeah, totally. upgrades are, updates and upgrades are both part of the robotics as a service story. So maybe we talk, about both of them because I think they're both relevant. here's the way we think about it, right? So like the hardware itself is mostly off the shelf for us.

Almost all of it's off the

[01:20:05] **Audrow Nash:** Love it.

[01:20:07] **Rajat Bhageria:** Why do I, call that out? there's a bunch of benefits you get from that. Number one, each component has been productized by a different company and these are really great manufacturers, right? So Our, CPU, or our GPU, or our HMI, the touchscreen, or our light tower, each, there's some manufacturer who's world class at making these components, and so what that means is our mean time before failure for the hardware itself is quite high.

In other words, the hardware actually doesn't

[01:20:37] **Audrow Nash:** it's robust for sure.

[01:20:39] **Rajat Bhageria:** It's robust. Number two, another benefit of that is that we have built our software,

[01:20:44] **Audrow Nash:** on it.

[01:20:45] **Rajat Bhageria:** yes, and the software is built to be hardware agnostic. So what we can do is we have three or four different vendors per component. So if any particular component vendor is having some supply chain issues or whatever, great, we can go to them.

So that's really nice.

that also by the way,

[01:21:04] **Audrow Nash:** Like I'm imagining, did you, is it like you have three different vendors where you can buy depth cameras from? And it's a, it's all so one, you're using an Oakty, a RealSense and something else.

[01:21:15] **Rajat Bhageria:** the code base is built to be hardware agnostic. So like basically there's like a capture node, right? And like the camera capture node can, can, have the, core code, the core, like logic is agnostic to the hardware, but there's one file, which is okay, like the drivers for that particular camera, if that makes sense.

And then you can say, okay, this, instance is using this. Camera node, basically. Camera capture node. Or that same thing is true for scales. we can very quickly bring up new hardware in our stack. Or new, robot arms. Or new sensors. Or maybe we want another camera. we can very quickly bring up new sensors, trivially.

Not, totally trivially, but basically trivially. Because we've designed the system to be like, extremely

[01:22:02] **Audrow Nash:** yeah, so you can just sub out parts of it. How does that work with your training data? Or does it matter because the things you're labeling are, you can control everything anyways. Like you're just getting an RGBD image and

[01:22:15] **Rajat Bhageria:** Yes. I think it's a, Very good question. Right now, like I'm saying we could do this. Honestly, we've been pretty happy with our components so far. There

[01:22:23] **Audrow Nash:** Yeah.

[01:22:23] **Rajat Bhageria:** need, but, you'd be right. that would be a concern

[01:22:26] **Audrow Nash:** Okay, yeah.

[01:22:27] **Rajat Bhageria:** about.

[01:22:28] **Audrow Nash:** But I get what you're saying where you've built it in a way that everything is modular and that's definitely like as far as I'm aware that's the best practice for sure to make it so that you're not like super coupled to you're just using like general ROS architecture principles which is great.

[01:22:44] **Rajat Bhageria:** yes, exactly. by the way, this very well leads to service and upgrades. okay, from a service perspective, let's say some part of the system breaks. And of course, what we have, a pareto of, hardware failures, that we try our customer support

[01:22:59] **Audrow Nash:** You mean a Pareto distribution? Is that what you're referring to? Nice. So 80 20 rule kind of thing? Okay so 20 percent will fail 80 percent of the time. Is that what you're saying? Okay

[01:23:10] **Rajat Bhageria:** Yes. Yes. 


## [01:23:12] Field Replaceable Units and Service Strategy

[01:23:12] **Rajat Bhageria:** and so then what we can do is we can have FRUZE, field replaceable units for things that might fail frequently. And oftentimes those FRUZE will, just ship them initially with the deploy, like the, a new robot. like we only, we, we usually, ship starter packs, six robots at a time for a new customer.

So like you get a starter pack, we'll, ship you some spare parts, from the get go, right? And then of course, like. we'll also have them at our HQ so we can overnight them if, something actually needs a break. By the way, this is a very rare occurrence because our meantime before failure is like 180 days.

So it's it's not, like hardware's failing all the 

[01:23:47] **Audrow Nash:** awesome. Especially for

[01:23:49] **Rajat Bhageria:** then if something

[01:23:50] **Audrow Nash:** how early, like you guys are clearly put together and everything, but it's you're still beginning, like you're not at, you're not at scaling just yet, I think. And so the fact that you're failing this infrequently is just wonderful.

[01:24:04] **Rajat Bhageria:** yes. Yeah. 


## [01:24:05] Scaling and Global Deployment

[01:24:05] **Rajat Bhageria:** I, it's funny, like we've stayed under the radar quite a bit, and now is really when we're like really starting to scale, which is cool. And we can talk more about that

[01:24:13] **Audrow Nash:** Yeah, sure.

[01:24:13] **Rajat Bhageria:** yeah. but yeah, back to, the service and upgrades, so then what we do is we actually have partnered with a third party service org.

these guys have 10, 000 technicians all over the world. from a scaling perspective, we can deploy, and that's why we talked about Europe a little bit, We're not super,

[01:24:31] **Audrow Nash:** Geographically

[01:24:32] **Rajat Bhageria:** there's certain things, yeah, like certainly there's things to be careful about because of course we want the best

[01:24:37] **Audrow Nash:** I would think their data policy and stuff might be things you might

[01:24:40] **Rajat Bhageria:** exactly.

so there's, legal financial ramifications that do need to be

[01:24:44] **Audrow Nash:** but you could literally do it. Yeah. From an operations point, you're fine with it.

[01:24:48] **Rajat Bhageria:** yes, that's right. and so what'll happen, is we have a really nice repair manual, like a giant repair manual, And we'll train the trainer, if you will, like we'll train their, I'm a person who trains other people how to do these repairs with these crews and Anytime something actually fails. We'll say hey, we got an alert that something failed the customer told us something failed They'll drive out an hour because everything is an hour away from wherever they might be in the country and or North America And they'll change it apart.

And if they need to, they'll FaceTime us. So that's like servicing, for any hardware. 


## [01:25:25] Hardware Upgrades and Modularity

[01:25:25] **Rajat Bhageria:** And then from an upgrades perspective, I think it's a very similar thing. So we do these like ECOs, basically, engineering change orders, where it's okay, we, we'd like, so I'll give you an interesting example, We, we had these scales that we had shipped and they were like IP67, which is already fairly high water and grass rating. but we're in the food industry and people like love water. They just spray everything down.

[01:25:50] **Audrow Nash:** Yeah. Yeah.

[01:25:52] **Rajat Bhageria:** was getting water damage and, that was right when we deployed, like early on when we deployed, this was happening.

So we did an ECO and we changed out to IP69K scales. And, it's pretty, pretty simple. We just ship them out, and, you just install them and, again, it's very, we already have another, node for, the new, driver for the new scales and you're up and running. I think upgrades, because it's so modular, it's not for example, there's no PCBs at Chef.

it's, electronics are all off the shelf, right? It's, there's a DIN rail. 

[01:26:28] **Audrow Nash:** you 

[01:26:29] **Rajat Bhageria:** like a very simple,

[01:26:30] **Audrow Nash:** That's it.

[01:26:30] **Rajat Bhageria:** it's extremely, like if you were to look at it, it's an extremely simple hardware system. Which by the way, it seems Simplicity, I think, is really hard to do. So I think there's a lot of complexity in the software, by the way.

There's, because we don't have hardware complexity, we have a lot of software complexity, but from a hardware perspective, then if we need to change out the tech, like we're going to, there's a new PCAP display that we're going to do an ECO for. It's like much, much more reactive. There's like multi touch and it's nice because in food facilities, you have like gloves.

So it's so anyways, there's some, oftentimes these gloves have food in them. So there's some practical reasons why we're doing this. But you want to change the touch screen, no big deal. You want to change the camera, no big deal. new GPU, touch it onto the dendril. it's 

[01:27:14] **Audrow Nash:** that's really nice. Yeah, I would. The only concern that I would have with new parts would be that it would hurt your ability to reuse past training data. But I guess that you're working on a number of platforms, that is going to be in your favor because they're all going to be a little bit different. and then I would imagine if there's maybe it's just good enough you just pass the image and it figures it out but I would imagine say it's like a slightly different resolution or the colors are a little bit different or something like that I could imagine that the camera could mess with

[01:27:46] **Rajat Bhageria:** itself is quite important, yes. No, you're 100 percent you're 100 percent right.

[01:27:51] **Audrow Nash:** the rest of it yeah it makes perfect sense that you could swap the touch screen and that wouldn't have any negative impacts for this kind of thing

[01:27:58] **Rajat Bhageria:** By the way, one thing that's also pretty cool that's happening in the world, which I'm sure you've seen, is like there's like exponentially decreasing prices for stuff. Like back in the day, like it used to cost 60, 000 to buy a robot arm. Then of course Universal Robots had this big breakthrough with collaborative robots and like they got it on to 30 or so, right?

And now there's a bunch of these, a bunch of new companies like Doosan Robotics is one that just went public in Korea and like they have this really, nice arm that's like substantially cheaper, right? And There's a, and by the way, that's just like I'm talking about, robot arms, but even the Intel RealSense camera is 200, which is insane.

the Jetson suite at NVIDIA, there's all these components and the cost is so much cheaper,

[01:28:37] **Audrow Nash:** It's

[01:28:37] **Rajat Bhageria:** right? And I think that's really cool, too. I think the hardware, people, talk all about, we're talking about transformers and, all this stuff. the software's obviously getting really good, but, I think the hardware is also getting much better and cheaper, which is really

[01:28:49] **Audrow Nash:** Totally. And you need it to do things in the physical world. Like you need an expensive sensors and things like this. I don't know. I just, one of the things that blows me away is I was, an undergrad maybe 10 years ago or something like this. And I did an internship at a company and we were using an RTK GPS.

and it was, Like a 10k GPS or something like that like it was absurdly expensive and don't quote my numbers But ballpark of what I remember and now companies are getting them for 100 or something like really low and it's really amazing. So you're seeing that fall, especially, I think part of it is maybe more efficient processes for things.

And then another part is larger markets like robotics is growing up and all the cars are using sensors and because of that, there's more demands for sensors. So then it's more efficient is what I imagine.


## [01:29:45] AI and Robotics Industry Trends

[01:29:45] **Rajat Bhageria:** And, by the way, I really hope, I really hope that this like recent advance, or I think ChatGPT was really, awesome actually, because it, like inspired the world to do AI. Like, before then, if you remember, like during COVID, crypto was a cool thing, right?

[01:30:04] **Audrow Nash:** yeah,

[01:30:06] **Rajat Bhageria:** and 

[01:30:08] **Audrow Nash:** I love the point. Yeah, definitely.

[01:30:10] **Rajat Bhageria:** I think yeah, like I, it's a broader point, which is I think the world needs a, the world needs like a, like a figurehead, right? It's like the four minute mile. Somebody needs to do the four minute mile, and then everyone else comes after. In EVs, that was Tesla.

Tesla did. EVs, and now everyone's doing EVs. In semiconductors, there's Intel. Intel, really, productionized the, the transistor into an integrated circuit and then sold them, and then, of course, there's lots of people who are doing integrated circuits. Facebook did this for social networks, and Uber did this for marketplaces.

I think OpenAI did this for AI. Now, AI, the AI they're doing is more large language models, but they, they've woke the world up when it comes to, AI. AI, which is I think really good because now there's a lot of engineers, entrepreneurs, operators, investors, writers, journalists, everyone else who's thinking about AI, which is really good for the world.

And you know what's interesting is that what's the natural progression of this like Hype in, or yeah, I guess it is hype. what's an actual progression? I think it's two things, right? one is like people are more interested in energy, right? Like how do you actually get the energy to actually power these models, right?

they're really interested in compute. So GPUs is a very natural extension. And of course, what's the third one? Robotics. It's you, take the, you take these models and you apply them in a physical environment. So I'm hopeful that. I'm hopeful that this energy that we have around AI right now will translate to a lot more breakthroughs in robotics, but also just a lot more people doing robotics and deploying successfully and scaling robotics companies.

And, hopefully if, there's at least a couple winners, that really scale hundreds of thousands of robots, everyone else, it'll, open the floodgates. It'll inspire other people to do it.

[01:32:02] **Audrow Nash:** Yeah, I think it's very true. I also think there's additional market forces that are making it so that robotics is heavily invested in, like the labor shortages you mentioned. Because there is the point where, what was the You said something like there's 30 percent labor shortage or what was the

[01:32:22] **Rajat Bhageria:** Yeah, exactly.

[01:32:26] **Audrow Nash:** that might get worse I think it's likely that gets worse.

a lot of people are retiring The biggest cohort the baby boomers are retiring and so they were largely blue collar workers or a lot of them were blue collar workers and so then We're gonna need robots and so this is going to drive robotics investment because they are a feasible solution.

there's technical risk of course, but if you set up a company in a smart way, like in my opinion you guys are doing, like you can really dig into a lot of these problems and make a lot of value, and you don't require like a massive overhaul of all the facilities that they do the work in.

you can just drop a robot in. 

[01:33:12] **Rajat Bhageria:** that's right. And I think, yes, all of that's really true. And I think what's also true is, I think, we were talking about this a little bit before, but my, like our company and our cohort of companies, our peers in the space, I think they've also learned from the past a little bit, like about what's good and what's not good.

I'll give you some examples, right? and these are like more practical, like robot, how do you build robotics? I think there's some practical lessons, right? one is, off the shelf hardware. It's really good. there's many reasons we talked about it. Robotics as a Service. I think what's really nice about Robotics as a Service is you don't have to convince somebody to put down half a million bucks.

that's really powerful. Now, by the way, this caveat is that some customers, especially in industrial settings, they don't, they just want to buy the thing. it's not perfectly perfect. Perfect there. But generally it's nicer not to have to put down this big expenditure for a startup that you've never heard of.

Which is the case in selling like us. Like most people haven't heard of Chef yet in our customer base. Another idea that I think people are realizing is don't try to automate the full process. And what I mean by that is if you try to automate the full process, you have to, it's too much.

You have to deal with all these things. Ideally you have this little cell that can just slide on.

[01:34:24] **Audrow Nash:** Totally agree.

[01:34:25] **Rajat Bhageria:** No retrofitting, there's, all these lessons. Another one that's interesting that's like less technical, but for a while people used to like fund inventory for their hardware using 

[01:34:35] **Audrow Nash:** Yeah. 

[01:34:38] **Rajat Bhageria:** and now I think the world is realizing that, Oh, we have a, it's a real hard asset. Like I don't need to get equity. I can just get debt. And that's really nice to actually finance the inventory to actually do these robotics as service deployments.

[01:34:50] **Audrow Nash:** Interesting. I don't fully understand that. Would you tell me a bit more?

[01:34:54] **Rajat Bhageria:** yeah. okay. So here's the way you can think about it. It's okay, like I signed a customer, right? Our business model is robotics as service, right? we have to buy them, bill materials upfront. So we have to outlay all this cash upfront. But we don't get paid

[01:35:11] **Audrow Nash:** For a while.

[01:35:12] **Rajat Bhageria:** all at once, right?

Exactly. we get paid in bits and pieces as a service. now there's a big cashflow issue, right? So if I have let's say I raised 10 million bucks as a seed round and I want to deploy 10 robots, I don't know, I'm just saying arbitrary BOM, but you, get the point. Like I have to out, I've already spent a bunch of my cash on inventory.

wouldn't it be nice if that 10 million bucks is really for keeping the lights on, hiring engineers, hiring deployments, folks,

[01:35:39] **Audrow Nash:** Actual operating expenses. Yeah.

[01:35:45] **Rajat Bhageria:** and the way that might work is like. I sign a customer, I take that contract to the bank, advances me cash, I use that cash to buy the inventory, I, provision the hardware with my software, I configure it and then I deploy it, I pass site acceptance test, the customer starts paying me, and then I

[01:36:04] **Audrow Nash:** pay the loan. Yep. I

[01:36:06] **Rajat Bhageria:** what this means is that the cash flow, the cash flow cycle is much better because my, I have, instead of, waiting X months to return the cash from my bill of materials, I can be net cash flow positive on a unit basis in a few

[01:36:18] **Audrow Nash:** Yeah. And you don't have to trade equity, which is way better because you can incentivize employees. You can keep more for yourself. You don't have to raise more rounds of investment than you need. 

[01:36:29] **Rajat Bhageria:** and, you can grow the company. and all of that, and remember what you said earlier, which is robotics, you have to continue growing gradually, right? You have to show like the test analogy. if you have more, if you have more equity, you have more runway, which means you can ship more robots and show more progress, which then allows you to raise more capital

[01:36:48] **Audrow Nash:** Even better. Yeah, you're right. That is great. Let's see. So I know you wanted to talk about a few things and we are coming to the end of our time. 


## [01:36:58] Challenges in Robotics Production

[01:36:58] **Audrow Nash:** but why, are many robotic companies failing? what have we learned?

[01:37:06] **Rajat Bhageria:** Yeah, I think, like I said, I tried to really study the industry early on when thinking about Chef because I was just like, it was like, okay, what's the biggest thing I could possibly, I was like, what are the big things I could work on? And I was like, energy seems really big because, obviously, there's a big climate change issue and, energy is really 

[01:37:24] **Audrow Nash:** And we're building our industrial plant. Like we need way more. Probably three times or something crazy. Okay. Yeah,

[01:37:31] **Rajat Bhageria:** and then it was like AI, and within AI and the physical world, and I was like, so convinced that this is such a powerful thing, like I think AI and the physical world is really going to be like electricity, so I was like, I was super excited. But then I look at the industry, And it's a graveyard!

it's robotics has been tough, honestly, that's just the truth, right? There has, been, like, a lot of failures. the AV industry has sucked in tens of billions of dollars, and yet, the output has been millions of dollars in revenue. single digit

millions, probably.

[01:38:01] **Audrow Nash:** it's 

[01:38:05] **Rajat Bhageria:** anyways, I, really tried to, learn from the industry. I, think one, one big thing I learned, there's a bunch of lessons which we can talk about, dozens, probably, but, one, one, thing that I think, puts the story to life is, I think a lot of people who do robotics, the founders, they're extremely technically minded folks, right?

They're, very smart folks because he, and, very, usually generalist because it's such a, it's such a breathful field. Like you need somebody who can, like at least understand everything from like computer science and AI to then of course the electrical stuff to the mechanical stuff to, Everything in between firmware, manufacturing, etc.

Even service and customer success, there's a lot of facets to it. what does that mean? what that means is that there's a lot of folks who just like to build cool stuff, right? it's like robots are cool to build. And I think you saw a lot of robotic companies who were like, in previous generations, who were like, you could tell it's just hey, somebody's let me build something cool.

and I think, that can work, right? And it has worked in the past in other industries. But the issue is that the iteration loops in robotics are much slower than something like software. So here's what I mean by that. if I am a software as a service company, right? Or I'm a consumer software company, I can build a prototype in a weekend, right?

[01:39:26] **Audrow Nash:** Yeah, 

[01:39:26] **Rajat Bhageria:** can get something work. It's a hack, hackathon style, right? MVP I can get, up in 24 hours, 48 hours, whatever. it might not be per perfect, but you, get the idea. 

[01:39:37] **Audrow Nash:** You're Parerito.

[01:39:38] **Rajat Bhageria:** very quickly.

[01:39:39] **Audrow Nash:** you get 80 percent with 20 percent of the effort or something like this. Okay. 

[01:39:43] **Rajat Bhageria:** That's right. And then you can iterate, right? And this is the entire Eric Lee, Eric, Lee startup, Lee startup model, right?

Which is you have a hypothesis, you build a prototype, and you iterate until you get to product market fit. and, I think Silicon Valley, a lot of Silicon Valley, modern Silicon Valley, like software, not the old semi conductor Silicon Valley, is built on that idea.

if I'm doing robotics, or autonomy, or AI more generally, the iteration loops are just fundamentally slower. Even if it's like autonomy, is slow because it's like hard. Like autonomy is much harder than making a web app, right? So and that's just the truth, it's not you need both, right? You need both, but it's just, but, the iteration loops are slower.

So instead of having 10 shots on goal with a pre seed round or the seed round, you have One shot on goal, before you run out of money, or maybe you have two shots on goal. So this idea of, let me just build a cool thing, and then I'll iterate. It doesn't really work because you end up building the wrong thing and then you fail.

I've seen this over and over, like founders build a cool thing, and then you just, you end up not being able to raise them the next round,

think now what a lot more companies are doing in our cohort, the more, more kind of contemporary robotics companies is, you still need the same technically minded founders, but

[01:41:03] **Audrow Nash:** Gotta be market

[01:41:04] **Rajat Bhageria:** people are a little bit more business, Business 

focused. so it's, things like, okay. for example, we sold the product before we built it. Like when we were doing fast casuals, even like we got contracts really making sure that people really want this thing. Like we know for a fact people want this thing. And of course we reduce the risk for the customer too.

We added a site acceptance test that said, look, you're not actually going to pay the recurring fee until the thing works. So we reduce risk for the customers, but we knew that they wanted it. for example, and, but what selling before building got us is We know they want it. We have a good product requirements document where we've synthesized all the requirements from multiple customers.

So we know we're not overfitting on any particular customer. So 

[01:41:45] **Audrow Nash:** Definitely. 

[01:41:46] **Rajat Bhageria:** I think, what that allowed us to do is we didn't have to iterate towards product market fit. We had a product market fit, if you will, from the get go. Now, obviously there's still lessons. There's still unknown unknowns and even known unknowns.

So there's still lessons, but you're less likely, like we were able to really get product market fit and One iteration loop, which is fast casual, and the second iteration loop was food manufacturing, as opposed to seven or eight iteration loops, which is really where you end up not working, I think.

That's one lesson I would say that's really been interesting, which is selling before building. And coming at it from oh, we're really solving a customer pain point, as opposed to just trying to build something cool.

[01:42:22] **Audrow Nash:** totally. selling before building. I hear the idea a lot for SaaS projects now, at least on X and things like this. how do you get a customer to sign off that they, is it like a contract that they will pay once you deliver something? Or how do you, sell before you build? What does that look like?

[01:42:43] **Rajat Bhageria:** Yeah, I think, yeah, so I, I think where this starts is you have to get them to realize that they have a really big pain point and tell you. So this isn't like you go to them and say, I'm going to build, not really a sale, right? It's like really them selling you almost, right? Like you go,

no, I guess what I'm saying is you go to them and you're like, okay, customer.

What's your biggest pain point? And this is what we, this is literally what we did. It's just interviewing them almost. what's your biggest pain point? And they say food assembly. Then they're like, okay, can robots help? Yeah. And then it's okay, if we were to do this, would this be something you pay for?

Yeah. And then, so, in other words, they're like, they're selling you, like they've, it's, like how. How big of a problem is it for them, I guess is what I'm saying, right? if it's a really big problem for them, and there's no solutions in the market, which is what was the case in our case, then they're going to be a lot more willing to work with you.

So what we did is we went to them and said, look, customer, we know what your requirements are, and here they are. We've written them into this Word document. do you agree that these are indeed your technical requirements?

[01:43:46] **Audrow Nash:** the way, we're, we're at our ending time, are you okay to go for another maybe like 5 10 minutes, or do you have a hard cutoff? Okay, hell yeah. Sorry to interrupt.

[01:43:58] **Rajat Bhageria:** No, good. here's your technical requirements, and do you agree with those? Yeah. Yeah. And then we say, okay, look, we've done this financial analysis, and we think that if we were to charge you X dollars per year, this would be a financial win for you, and here's why we think that. Do you agree with that?

Assuming these assumptions are indeed true, yeah, we agree with that. Okay, how about this? Let's work together and sign this contract that says, if we build this thing,

[01:44:22] **Audrow Nash:** You'll buy for

this. 

[01:44:24] **Rajat Bhageria:** and it meets this site acceptance test. This is the key part, the site acceptance test. It meets this set of requirements, and these set of requirements will be things like Is this consistent?

Is this fast? Is this footprint? Is this food safety rating? Etc, etc. It can do this washdown for sanitation. if it meets these requirements, Then you will pay us contractually this amount of money. And just to make sure you're really serious, how about you put down XK as a deposit and it's, not a non-recurring engineering, but it's just a deposit to really make sure you're

[01:44:54] **Audrow Nash:** Ah. Okay.

[01:44:55] **Rajat Bhageria:** this is, it is a, true contractual agreement, but the customer hasn't outlayed a ton of cash, but they have put their commitment down that they're serious about this.

[01:45:06] **Audrow Nash:** I love it. That's great. What a cool idea to, because I've been seeing this in SaaS where people are like, don't build it first. but seeing it in robotics where it's a hardware project is a new idea to me and it's really cool. Yeah.

[01:45:21] **Rajat Bhageria:** I actually, don't think it's as new as, I thought this was new too, but then I like, I learned that like a lot of industries work this way. So like a systems integrator, a systems integrator doesn't, I was talking about the Heinz line, for making ketchup. some, like JR Automation or JMP Automation is not putting up 10 million bucks of their own capital and, going to Heinz and being like, Hey, do you like this thing?

Okay. We iterate a little bit. Do you like it now? Oh, we changed a little bit. Okay. Do you like it now? They don't do that. 

[01:45:49] **Audrow Nash:** Yeah. 

[01:45:50] **Rajat Bhageria:** Instead, Heinz goes to JR Automation and Heinz said, Hey, here's what we need to build. And JR will put, together a. A quote, right? And, then Hez can sign off and that's when

[01:46:05] **Audrow Nash:** the ticket.

[01:46:06] **Rajat Bhageria:** automation starts to work.

There's a lot of examples also about this. I generally, I, think if I'm like Boeing, right? and I am like Delta, I just made that up, but Boeing is not gonna make Delta some planes without. Without having a PO. And by the way, that also goes for new models. So there's, an interesting like story with Pan Am Airlines and Juan Tripp.

Juan Tripp is like the guy who like made Pan Am. and he was negotiating, I think with the CEO of Boeing or something at the time for, he wanted like a really big jet, and basically the Boeing CEO was like, look, if you Pan Am give me an order for X planes, then I will build a 747 for you. And so Pan Am put down a commitment. Okay. Okay. Boeing. So long as you meet these commitments. These agreements, these requirements, iPanAm Airlines will buy X of your 747s. So now the Boeing CEO has commitment that people want his plane, and now he's willing to spend billions of dollars of R&amp; D into making this 747, which is how the 747 started.

I think there's a lot of examples actually where the selling for before building, Bill Gates did this with MS DOS. He sold MS DOS to IBM before he spent time and money. he didn't drop out of Harvard. he built, he sold MS DOS to IBM and then he, built MS DOS. Or Wozniak, or sorry, Paul Allen did, but yeah, you get the point.

[01:47:37] **Audrow Nash:** Gotcha. Yeah. I bet you're right that it's more common. I just haven't seen it in a robotics context. at least that I've noticed, which is quite cool. Okay. Hell yeah. And then, a last thing that I wanted to talk about is why is production hard?

[01:47:57] **Rajat Bhageria:** Yeah, this was an interesting lesson for me, right? Like I, I think like robotics is already extremely hard as it is, right? it just so hard to just get zero to one. it takes it can take a year or two years to get even zero to one. And autonomous vehicles took 10, 20 years to get from zero to one, but the production is just At least 10 to 100x harder, right? And what I mean by that is the amount of edge cases are just insane. So for, I'll give you an interesting example. Like food facilities are sloped and the reason they're sloped is for water drainage.

[01:48:27] **Audrow Nash:** Yeah. It makes

[01:48:27] **Rajat Bhageria:** Now, by the way, I, we just talked about selling before building. We talked about getting product requirements early.

Like I'm all about the product part early, just to really understand the requirements, but even I did not notice that the floor is sloped, right? Like it's just imperceptible. It's not, and it's not even a question, to ask. You just don't even think about asking it. we shipped our robots to production, and the very first thing we noticed is the robots like, shaking around.

This is like day one, right? We shipped a robot to production. It's oh damn, what's happening here? 

[01:48:57] **Audrow Nash:** is 

[01:48:57] **Rajat Bhageria:** this wasn't showing up. Why is this happening? And then, of course we asked them, and they're like, oh, that's what's happening. so anyways, that's a hardware thing. Okay, let's add stabilizing feet.

But then it's also then the next thing we notice is, okay, the robots like this, the conveyor might be slanted. Okay. so now if I like, I have to detect the slope of the conveyor and place lower or higher. Okay. okay. Now it's all great. We solved that issue. But then like now instead of day one, now we're day, now we've run for 16 hours a day.

And after 16 hours of the conveyor running, the conveyor is shaking. It's like vibrating a lot too. So now the conveyor, it's already like this, but now it's like it walked. It's a little bit, it's like this, it's skewed. So now you have to place lower and closer and farther and higher. Again, this is just a very simple example.

now we deploy with our next customer and that next customer has cheese grits and every single day those cheese grits are totally different. That's just what it is. and then, at a different customer you have humans who are like eager to go home and they're like, they're randomly taking bowls out of, they, they pull the ball from in front of the robot, and so the robot has detected the ball, it's tracking the ball, and now the ball disappears, so that track is like, what, I don't know what to do, what's happened.

There's all these weird things that happen with different ingredients. Like other humans that you're interacting with, detect, like detecting the, the, velocity of a conveyor. You think it's simple, monotonic, right? It's like probably simple to use a camera to detect the velocity of conveyor.

It's super noisy. It's it's all over the place and every conveyor is a little bit different. So how do you have really good speed estimation of the conveyor? So you can actually place onto a moving conveyor and get into these very small compartments. It's actually not trivial. So I think there's just a lot of And I can name hundreds of examples like this. there's just so many, weird things you just never even think about.

[01:50:46] **Audrow Nash:** To totally.

[01:50:47] **Rajat Bhageria:** And, that's, honestly, when you think about, a mode, I think the data mode's really good, and I think the service mode, actually having this, network of people all over the country.

But, from a product perspective, just dealing with all these edge cases, even if you copy my hardware, even if you copy

[01:51:03] **Audrow Nash:** Ah,

[01:51:04] **Rajat Bhageria:** dealing with all these edge cases and making a solution is pretty hard. I'll give you one more example, final example. Usability, right? Many of our users, the people actually on the line who are like telling Chef what to do, they're often not English speaking, they're often Spanish speaking or Farsi or they speak different languages and, they're often not necessarily college educated or even high school educated.

we need to make a system that's like hundreds of thousands of lines of Python and C code and all this like cool hardware, be used by somebody who, hasn't really dealt with machinery or robots or software really ever. the usability is actually a lot more important than you might think, actually having everything in Spanish or being, whatever language that is most prevalent at that site, having the system so it's extraordinarily obvious that this is the thing to do, if something like if a bowl is too far on the conveyor so the robot can't reach, throwing a really nice visual 3D warning, oh, the bowl is too far.

Or maybe somebody comes up in the morning and they're like, I want to go home, so they crank up the conveyor speed. So the conveyor speed is way faster than the, the ODD, or like the expected speed, yeah. And now the robot's I can't keep up with all this. And now the user's really upset because they're missing bowls.

Missing containers, but the robot can't do anything. So throwing a nice warning. Ah, you're on the dashboard Oh, your conveyor is moving a lot fast and a lot faster than it should but doing that in a way that's not in words, but rather in Images. 

[01:52:36] **Audrow Nash:** something easy to explain. Yeah, images,

[01:52:40] **Rajat Bhageria:** that really separates like a

prototype company from a production company And then going from one robots of two robots One robot, zero robots, one robot in production is a big deal, and then ten, and then, it's just every layer it's just like the amount of volume of stuff going on is just absurd. Like now we've made 17. 7 million servings, meals in production, like it's just the amount of stuff going, happening, is just a lot. And you have to have the right data infrastructure to be able to process all this, alert, alert the right people, annotate all of this, you can actually triage it, all this

[01:53:18] **Audrow Nash:** you got to keep up with it. Do you have any, 

[01:53:20] **Rajat Bhageria:** up with that.

[01:53:21] **Audrow Nash:** do you have any heuristics or like lessons or any things that would have any mindsets or anything that would have made this whole process of dealing with all these difficult edge cases that pop up in production a little easier or just be ready for them and steele yourself for it or what do you think like anything would have helped you in preparing for all


## [01:53:45] Hiring the Best People

[01:53:45] **Rajat Bhageria:** I think, there's a few like strategic things and a few practical kind of tactical things that come to mind. I think like the thought that's coming to my mind is just we really think a lot about hiring and hiring really good people, but just honestly just continue hiring the absolute best people.

If you have a really good team, 

they can, knock this out, right? I think it just starts with that, your team, right? and then also having, like I, yeah, like it, it seems like, On the surface, you might be looking for a very tactical thing, but like having a culture where everyone really cares about the customer, right?

I think there's a lot of companies who like They talk about customer centricity, but they really don't care that much about the customer. Whereas if you can build a culture where everyone across the company just knows everything that's happening with the customer. They've been to the customer, they know the customer, they know why the customer cares about something.

Then if there's a little bug that happens, people can empathize. It's ah, my code is doing that. I need to go fix it. And there's a personal, I, if I, if that means I'm going to stay till 8 fixing this bug, great, because I care about this customer, and I know what it, what, how impactful this is for the customer.

So I think that's some, strategic stuff. On a practical level, I think, would say a couple of things, really, we invested a decent bit in test infrastructure, and Data pipelines. I think we could have done even more, right? Just like really good internal tooling around data infra. So like even better tagging, even better annotation, even better processes so that if there is like creating federations so there's 20 weight events.

Let's act, let's aggregate all those into one bug ticket so that we have 20 bagged files so that when an engineer goes and triages them They have all the data they need right there, right? or another example might be like, okay, if I patch a PR to fix some thing, let me patch it to, automatically patch it to every branch that we have in production.

And these, these are like not, these are commonly, these are software tools that, in SaaS all the time and like production companies all the time, but robotics doesn't have a ton of

[01:55:58] **Audrow Nash:** I agree. Yeah, so really investing in that tooling because that improves process and every time you, when you have a crappy process, it eats future time because you have to go do whatever it is.

[01:56:13] **Rajat Bhageria:** the way, it's tough though, like I'm saying this,

[01:56:15] **Audrow Nash:** you don't want to optimize too much is the other side of that evil.

[01:56:19] **Rajat Bhageria:** well, and, once you, like, when you're trying to do zero to one, you're not thinking about tooling, you just want to ship the thing, right? It's whatever it takes to ship the thing out the door. And then as soon as you ship it, you're delus you're like, underwater with bugs.

You're diluted with, er, yeah, and, then then you're like, there's a lot of pressure to grow, and, so anyways, it feels, it's you want to do this internal tooling stuff, but it's like, how do you create the time to do it, right? there's always this, hard battle, but you, need to do it.

It's necessary, or else you're never gonna get ahead of it.

[01:56:54] **Audrow Nash:** Yeah, I feel like, I don't know, for maybe, I guess it probably comes back to the people you hire to some level for this kind of thing. Because one of the joys that I've had working on the ROS2 project is I have wrote a lot of tools and I wrote a lot of scripts to automate really dull things for us.

because one, I like to, Doing that, and two, they make everything else easier. And when you have more consistency across projects, it's much easier to write additional future automations. And so having people that want to go out and do these kinds of things, and know about them, that there is the option to do this thing and improve the process, that might be a good way too.

[01:57:42] **Rajat Bhageria:** Yes. No, I totally agree.

[01:57:44] **Audrow Nash:** Oh, yeah. Yeah. Hiring, as you said.

[01:57:46] **Rajat Bhageria:** Hiring is everything. some of our engineers will just they're like, okay, I need to solve this thing. And if I can spend another half an hour, I can build this quick little internal tool. And it's not even, it's not, like a part of the sprint.

They're just like, I need to do this because it's going to help me. And I really care about the company and I have a lot of equity in this company. So let me just do it. 

[01:58:05] **Audrow Nash:** Yeah, totally.

[01:58:08] **Rajat Bhageria:** And by the way, I say that by the way, because it's an important point, which is if you hire people where it's not just a job, but like they're, it's really they really, believe in it.

if, in other words, you treat your people like investors. They're like investing into their company with their time. They really believe in it. And if they really believe in it and they have a lot of skin in the game, then it's less, it's like, it's not okay, I just do my sprint.

I'm gonna go home, right? It's I want to make the product and the company and the machine, being the company better.

[01:58:39] **Audrow Nash:** Yeah, it's mission oriented trying to help the whole thing. Yeah. Do you have any thoughts on how to hire? Good people or how do you find good people?

[01:58:51] **Rajat Bhageria:** Yeah, that's very tough. Hiring is actually a lot. like people think like fundraising is hard. I Hiring is extremely tough, I think, honestly. I have a few thoughts. one thought I have is that, I, watch this, famous clip. I don't know if it's famous or not, but this clip by, Derek Sivers.

He talks about, basically, he's the guy who made Seedy Baby back in the day. And, he had this famous clip, this, clip, which is, the first follower is the person who turns a lone nut into leader. So he shows this like little clip of somebody like dancing around the middle of a field, right?

Just randomly and he was like, oh, who's this weird person? And then one other person joins and as soon as that one other person joins everybody else comes

[01:59:41] **Audrow Nash:** you're like an eccentric doing your thing until others follow you and then you're the leader Hilarious.

[01:59:47] **Rajat Bhageria:** And I think that's how hiring works. when I try to find, my approach was always to get, very senior folks. I want senior staff level engineers from the get go. Which, by the way, was hard because, we're this tiny company who can't pay a ton of money in terms of salary, right?

at the time, right? This was like back in 2019, 2020. so it's like, how do we convince somebody? So initially it was just a lot of rejection. We talked to a lot of people and a lot of people are like, look, this is great, but I have a mortgage or I have a partner and I have kids and sorry. 

but we ultimately convinced one person who had a really, great set of experiences, quite senior, had been at a bunch of top companies, had been a lead, and like brand names that people know of, right?

Like respectable, basically.

[02:00:27] **Audrow Nash:** hell yeah.

[02:00:28] **Rajat Bhageria:** Getting him was huge because as soon as we got him. When I talked to the next engineer, I wasn't the one selling that next engineer. This person was the one that's selling the next engineer,

[02:00:38] **Audrow Nash:** hell yeah. That's so funny. It's a lot like that podcasting, by the way, which is very funny. Getting guests and this kind of thing. Same dynamic.

[02:00:47] **Rajat Bhageria:** Cool.

[02:00:47] **Audrow Nash:** Okay. And

[02:00:51] **Rajat Bhageria:** having a high bar early on.

I think it's in the early days it's easier just to take whoever because like You don't have much to offer so it's come anyone who's willing to come but I think if you have a really high bar early on then you set yourself up in many ways because this thing we just talked about from the hiring perspective but a really good engineer has good architecture decisions because like it's like the famous thing like Yeah, like, Facebook still uses a lot of PHP.

It's like, why do they use PHP? it's because originally Facebook was written in PHP, so it persists. There's inertia there. and I think that's true of like technical decisions. for example, if you start off with ROS 1, it's really hard to do ROS 2. But if you have somebody who is, who's been around the block, they might recommend ROS 2 from the get go.

That's a good architecture decision and probably gonna pay off in the long

[02:01:37] **Audrow Nash:** Hell yeah.

[02:01:39] **Rajat Bhageria:** But right? There's many reasons to get a more senior person from the early days. It's harder, but if you can do that, then it makes hiring other people easier. And then, after that, just keeping a really high bar, having a really good interview process, 

[02:01:56] **Audrow Nash:** Hell yeah.

[02:01:56] **Rajat Bhageria:** It's not easy, honestly. Like I think it's really hard.

[02:01:59] **Audrow Nash:** Yeah, I think so too. And I love that lone nut idea. hilarious. But so we have gone quite a bit over time. I am wondering if you have any last thoughts or things you'd like to share with our audience. what, do you hope they take away from this interview and about Chef Robotics?

[02:02:22] **Rajat Bhageria:** Yeah. I think I'll say on a more broad scale, a scope, like broad scope thing, which is I really, think the biggest impact for AI is going to be on the physical world in the labor market. And I think by the way, it's not this is not like a dystopian, take your job thing.

I really believe in a future of abundance where, you know, 50 percent of the economy is manual labor right now. what if robots are doing that? And, by the way, there's been a lot of instances where like. Automation has created a lot, like every instance of automation has created more jobs than it's taken.

So the G Throw Toll, or the printing press, the computer, the steam engine. These created a lot more jobs than it took, but the jobs are better. And I really am a big fan of that, so I'm really optimistic and hope that a lot more people are going to take their AI skills, right? Let's take those skills you've developed in machine learning and AI, or even software engineering, and, like really apply them to do embodied AI.

Because I think like the really important problems of the world, the really important problems of the world, they're not in bits that you can solve it. You can do a lot in bits. You can do a lot in bits, right? Palantir is a cool example of a company doing a lot in bits. Uber is a cool company. It's moving atoms with

[02:03:34] **Audrow Nash:** Yeah. 

[02:03:34] **Rajat Bhageria:** But I think like really the most important problems in the world are physical world problems that you can't solve. The Global Hunger Crisis or Water Pollution or Climate Change using just software. You just cannot. And I, really hope that more people take those skills and apply them to the physical world.

I think that'll be really good for humanity in the world. and then when it comes to Chef, I think I, think like we have tried to stay very grounded, let's have a big vision and mission, but stay really grounded and actually shipping real robots that really help solve an actual pain point for the customer.

I think. I think that's really key in robotics. I think it's so hard to do robotics as it is, but if you have a customer, or ideally a set of customers, who's telling you what to do, and of course you be careful not to overfit, and you can really build something that's actually useful, and hopefully, if you have the right vision, then something that can become quite scalable.

And I think, if that's exciting for you, then of course we'd love to chat as well.

[02:04:33] **Audrow Nash:** Hell yeah. All right. It was a pleasure. And bye everyone.

[02:04:42] **Rajat Bhageria:** Thanks for having me, Audrow.

[02:04:43] **Audrow Nash:** As we wrap up this fascinating conversation with Rajat Bhageria, I hope you are as excited as I am about the potential of AI and robotics in the food industry. Rajat's insights into the challenges and opportunities in this space are truly eye opening. 

Before we go, I'd like to leave you with a question to ponder: how might AI powered food automation reshape not just the food industry, but our entire relationship with food production and consumption? Will we see a future where customized restaurant quality meals are as accessible and affordable as fast food is today? 

If you found value in today's discussion, I'd be incredibly grateful if you leave a rating or review. Your feedback not only helps others discover the show, but also helps me to improve and bring you the content you want to hear.

Thank you for listening. And until next time, keep exploring the fascinating world of robotics and AI.


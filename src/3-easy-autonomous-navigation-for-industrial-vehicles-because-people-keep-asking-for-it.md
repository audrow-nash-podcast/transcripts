## Table of Contents

- [[00:00:00] Start](#start)
- [[00:02:47] Introducing Stefan, Ilia, and Polymath Robotics](#introducing-stefan-ilia-and-polymath-robotics)
- [[00:04:33] Let's stop reinventing the wheel](#lets-stop-reinventing-the-wheel)
- [[00:23:11] Is your code open-source?](#is-your-code-open-source)
- [[00:26:34] Why focus on mobile robots?](#why-focus-on-mobile-robots)
- [[00:29:20] Stefan's experience starting Starsky Robotics](#stefans-experience-starting-starsky-robotics)
- [[00:33:45] A good task to automate and not get lit on fire](#a-good-task-to-automate-and-not-get-lit-on-fire)
- [[00:36:29] Integrating with sensors](#integrating-with-sensors)
- [[00:39:15] Approaching the problem from another side than most robotics startups](#approaching-the-problem-from-another-side-than-most-robotics-startups)
- [[00:42:57] Ambitions for Polymath Robotics](#ambitions-for-polymath-robotics)
- [[00:47:58] Running a different kind of business with fewer hats](#running-a-different-kind-of-business-with-fewer-hats)
- [[00:50:22] Stefan's bankrun t-shirt campaign](#stefans-bankrun-t-shirt-campaign)
- [[00:54:30] How Polymath plans to grow](#how-polymath-plans-to-grow)
- [[00:57:14] How Polymath uses machine learning](#how-polymath-uses-machine-learning)
- [[01:01:30] Big and expensive vehicles are easier to automate?](#big-and-expensive-vehicles-are-easier-to-automate)
- [[01:07:45] Thoughts on AI and Machine Learning](#thoughts-on-ai-and-machine-learning)
- [[01:15:40] Making safety certified systems](#making-safety-certified-systems)
- [[01:27:12] Live demo!](#live-demo)
- [[01:31:52] Web tools and robotics](#web-tools-and-robotics)
- [[01:38:57] Automate It podcast](#automate-it-podcast)
- [[01:49:57] Advice for getting involved in robotics](#advice-for-getting-involved-in-robotics)
- [[01:54:27] Stefan's former startup experience and path to Polymath](#stefans-former-startup-experience-and-path-to-polymath)
- [[02:00:54] Thoughts on side projects](#thoughts-on-side-projects)
- [[02:04:50] What Stefan and Ilia are excited about in robotics](#what-stefan-and-ilia-are-excited-about-in-robotics)

## Start

[00:00:00] **Stefan Seltz-Axmacher:** this is a, super key problem and is a big part in our belief of why the robotics industry sucks so hard.

[00:00:09] **Audrow Nash:** We all know robotics is hard. One reason it's hard is because it's hard to find off the shelf components you can build a business on. Because of this, most robotics companies end up reinventing the wheel. For example, building their own mobility stack. And this is a bummer because it's a huge barrier to entry for robotics startups.

Specifically, you may have to raise millions of dollars and work for a few years to solve undifferentiating problems. Like Autonomous Navigation. Before you can even start on your startup's core problem.

This is why what Polymath Robotics is doing is exciting. They're creating a platform that solves robot navigation for a large number of industrial use cases so you can just build on top of it and not reinvent the wheel.

They're also doing a better job than you probably would because it's their core problem and you might cut corners because of deadlines.

I really like where this is going and expect more companies to follow Polymath Robotics lead and make services for hard but undifferentiating robotics problems so you can use them off the shelf. I think this is a great thing for the robotics community as it makes robotics startups a little bit or even a lot easier.

And that makes it so that we're more likely to see robots doing dull, dirty, and dangerous tasks no one wants to do sooner.

This was a tremendously fun interview for me. I think you're going to like it too, especially if you're interested in or curious about robotics opportunities for mobile robots in industrial spaces, if you're curious about new and potentially powerful business models for robotics companies, or if you're a hardcore nerd and love safety certifications and requirements testing.

I know some of you are out there. You're gonna love it. Check out the episode description for timestamps if you cannot wait.

Lastly, if you enjoy this conversation, want to hear more from Stefan and Ilia, they have a podcast called Automate It, which is available on all the podcasting platforms you'd expect. It's a lot of fun, and I recommend you check it out.

After you watch the interview, I'd love to hear what you think. Do you think the approach Polymath is taking is good for the robotics community? Do you imagine more robotics companies doing something similar? I'd love to hear what you think in the comments or on X.

Without further ado, here's our interview.

[00:02:46] **Audrow Nash:** Hi everyone. Stefan, would you introduce yourself?

## Introducing Stefan, Ilia, and Polymath Robotics

[00:02:51] **Stefan Seltz-Axmacher:** Yeah, of course. My name is Stefan Seltz-Axmacher and I'm CEO and Co-founder of Polymath Robotics. At Polymath, we're making it really easy to add autonomy to any off highway vehicle. And before this I worked on self-driving trucks at, at Starsky where we put the first driver out truck on a public highway.

[00:03:06] **Audrow Nash:** And Ilia, would you introduce yourself?

[00:03:09] **Ilia Baranov:** Hi, I'm Ilia Baranov, co-founder and CTO here at Polymath. before this grand adventure with Stefan, I was working at Amazon on their home robot astro and have lots of fun stories to talk about there. and then prior to that was at Clearpath Robotics was one of the early folks there developing a bunch of the research and industrial autonomy.

[00:03:28] **Audrow Nash:** Now Stefan, would you tell me about Polymath?

[00:03:32] **Stefan Seltz-Axmacher:** At Polymath, we're building a modular stack where we're doing everything from sensor drivers all the way through throttle and steering commands for the software that runs onboard a vehicle to make it move from one point in space to another. So we're not building hardware, we're not building apps to tell robots what to, what to do, but the really, difficult but undifferentiated software packages that make a robot move through space, we've productized that and we're, we, have it on more robots than we have people on our team.

[00:04:01] **Audrow Nash:** That's so cool. How many people on your team and how many robots do you have it on?

[00:04:06] **Stefan Seltz-Axmacher:** 10, and we're, I think 11 robots going on 13 or 14.

[00:04:11] **Audrow Nash:** That's exciting. Hell yeah.

[00:04:13] **Stefan Seltz-Axmacher:** Yeah. And they're all different types of robots too. It's not the same thing. 10 times we're on things as varied as like bulldozers and tractors and articulated dump trucks and, all sorts of stuff.

[00:04:23] **Audrow Nash:** That's so cool. And how are, so you mentioned you're not doing hardware. How are you interfacing with these different vehicles?

## Let's stop reinventing the wheel

[00:04:33] **Ilia Baranov:** Yeah. So one of the things we had talked about with Stefan early, on is that we had thought kind of Robotics keeps reinventing the wheel. And ROS, even ROS's conception or the robot operating system, was that we wanna reduce the amount of reinventing the wheel by having a common set of communication packages and examples and the community. and that helps a lot. But we had seen that a lot of people will build this kind of vertical stack for their particular robot or particular application. and we just decided that we want to abstract that away. So we have apps, we call it a hardware abstraction layer,

pretty standard term for input sensors. And then we have the same hardware abstraction layer for the output to the vehicle. And that outputs the vehicle hardware Abstraction layer takes care of things like, what is a kinematic model? Turn radius maximum speed. What does the footprint look like? and so the core piece between those two hardware abstraction layers doesn't really change because all the complexities that's unique per vehicle are captured by those two layers.

[00:05:33] **Audrow Nash:** Very cool. So you have a good way of talking to, oh, go ahead, Stefan.

[00:05:37] **Stefan Seltz-Axmacher:** yeah, because the problem that we're solving is if you were to leave your day job to go start, say an autonomous tractor, the vast majority of the code you'd write in the first two to four years would be fundamentally undifferentiated from any of the other 150 or so autonomous tractor companies.

You'd just be like working really hard on a really hard set of problems that no one cares about for you if you solve them successfully.

[00:06:01] **Audrow Nash:** Yeah,

[00:06:02] **Stefan Seltz-Axmacher:** What we're doing is

we're giving you that as a product so you can focus on integrating it into an actual product that's some farmer somewhere or some mine operator somewhere, or someone,

whoever caress about. And you can focus on actually just making robots valuable as opposed to being the 1500th team to reinvent point-to-point navigation.

[00:06:21] **Audrow Nash:** So are you thinking of it like, you have this software that handles mobility for robots and you are selling it to businesses that make like tractors or big vehicles. And so then they outfit their vehicles with your software, and they're selling that complete package. So you are selling them the autonomy that they use as a service on their hardware in a

[00:06:52] **Stefan Seltz-Axmacher:** So we might sell it to an OEM like you're describing. We might

sell it to some big industrial company who's really sophisticated and can write their own software to tell robots what to do. Yeah.

[00:07:02] **Audrow Nash:** I love it. So how does it, I, guess Ilia, how does it work in terms of are you connecting over the can bus with the vehicles or how are you actually interfacing with the, what do we call it, the vehicle, whatever it is.

[00:07:21] **Ilia Baranov:** The, vehicle, the robot. we have this discussion back and forth is it a vehicle, is it a robot, is it machinery? Is it like industrial equipment? that's a marketing problem. Luckily I don't have to deal with that too much.

[00:07:32] **Audrow Nash:** Yeah.

[00:07:33] **Ilia Baranov:** but, yeah, so, yeah, as part of the interface layer, one interface we have is socket CAN, which can then talk to a whole bunch of CAN based equipment. but the most extreme case we have is actually one of our hardware partners, called Hardline in Canada. They're now part of Hexagon. they have a 1996 bulldozer, which is entirely mechanical and hydraulic.

And so the only interface we get to it is open this valve or close this valve

that's the most control we get to it. and so in that case, our hardware abstraction layer abstracting away all the valve controls up to a level where it's okay, we do positional loop closure using all the sensors we have, and then we control this thing like a, like an unknown plant that we throw valve controls at and get speed out of it.

[00:08:21] **Audrow Nash:** So you are doing, I thought you were not doing any hardware, but you are doing hardware for custom solutions like

[00:08:28] **Stefan Seltz-Axmacher:** So we don't, so

[00:08:29] **Ilia Baranov:** even in

[00:08:30] **Audrow Nash:** Oh, they're doing it.

[00:08:31] **Stefan Seltz-Axmacher:** Yeah. Yeah. so like an interesting thing and I like, and, I think everyone who's done robotics has seen when you try to build the vehicle or when you try to retrofit the vehicle, there's an incredible amount of really hard custom one-off work to retrofit this 1997 bulldozer or this 2023 tractor or this whatever.

And that work is really hard to do when you're a five person team. And the same people doing that mechatronic design are also writing the code or also building the ML algorithms or also building the app are also figuring out how to operate tractors as a service.

So there are, however, a whole bunch of teams all over the world, including hardline up in, in Canada, who are just mechatronics consulting shops where they can show up, look at a vehicle, they have a pre fitt, retrofit kit.

We'll customize it for that specific vehicle, and then we can talk to their API and issue commands to it.

[00:09:22] **Audrow Nash:** that's super cool.

[00:09:23] **Stefan Seltz-Axmacher:** So we get to just be a software company and not go be in cold places to bring up robots.

[00:09:28] **Ilia Baranov:** so hopefully I'm, not like, I'm not overstating our position here, but the, equivalency I like to draw is that you can think of us as Microsoft in some sense, and there's a whole bunch of laptop manufacturers in the world and like an ASUS laptop and a, whatever, a Dell laptop or fundamentally different beasts, but they comply to some underlying hardware, abstraction layer standard that then our OS can just sit on top of and control.

It's stretching the analogy a little bit too far, but that's the direction we're going where there's these retrofit and service and oEM companies all over the planet, very specialized in their particular vehicles, and all of them know how to treat their particular vehicle, and all they have to do is give us some level of

[00:10:10] **Audrow Nash:** You just need the interface. Yeah. And are you doing it all with onboard sensors for these, I suppose you probably. So how would you, is it all GPS driven?

[00:10:23] **Ilia Baranov:** can

[00:10:24] **Audrow Nash:** trying to imagine.

Yeah. So you are actually, your approach is quite modular, depending on the needs of it, is what it sounds like.

Okay.

[00:10:31] **Stefan Seltz-Axmacher:** because sometimes GPS solves all your problems and sometimes it doesn't exist.

[00:10:36] **Audrow Nash:** yeah. And then, yeah, and sometimes it doesn't exist and sometimes you have crazy reflections if you're using RTK and all sorts of things. Okay. So you have this modular layer, you're the software you can run on a whole bunch of different hardware. I like that approach. what exactly, being that you're modular, I suppose there's a bunch of things that you have the ability to do, but, what, are the core competencies of the, I dunno, your, what, do we call, your software?

Like what, how do we refer to it?

[00:11:13] **Ilia Baranov:** I, we've been, I don't know, again, if this is a marketing problem, we

just call it the autonomy core, that kind of

[00:11:18] **Audrow Nash:** The autonomy core. I'll just call it

[00:11:20] **Ilia Baranov:** the core.

Then the layers around

it or the core. And Yeah.

maybe that's a good movie too. Anyway,

there's, the hardware abstraction layers around it, but the core is the piece that we really put a lot of effort into and we try to change as little as possible

[00:11:34] **Audrow Nash:** So what

[00:11:35] **Stefan Seltz-Axmacher:** think of that as everything.

[00:11:37] **Audrow Nash:** Oh, go ahead Stefan.

[00:11:38] **Stefan Seltz-Axmacher:** yeah, so think of, the functionality of that as everything from literally running the drivers on whichever sensors we happen to have to make sure that we're getting data from the LIDAR, we're getting data from the RTK GPS, we're getting data from the, radar or whatever combination of things we happen to have. Turning those into some preset, things like point clouds, turning that into, cost maps.

[00:12:01] **Audrow Nash:** on a lot of things.

[00:12:02] **Stefan Seltz-Axmacher:** And use over and over

[00:12:04] **Ilia Baranov:** lot of the,

[00:12:05] **Stefan Seltz-Axmacher:** And then do,

[00:12:06] **Ilia Baranov:** hardware abstraction layer is basically turning into common data types and having as few of those as possible that are as widely defined as possible.

[00:12:14] **Audrow Nash:** Makes sense. That's probably the best way to scale, is what I would imagine for this.

[00:12:18] **Stefan Seltz-Axmacher:** basically our secret evil plan. And honestly it's part of our sales strategy as well, is we tend to just talk to our customers about how we've built things. And it tends to be how they wish they could have gotten to build things if they didn't have a six month deadline when they were first building their whatever. And 'cause the reality was when they, thought they were gonna start whatever autonomy project they're currently on, they thought, this time I'm gonna do it right. It's gonna be reusable. and then, some jerk squad, CEO changes the deadline or some customer says, I want some additional feature or whatever.

And the engineering team cranks out a bunch of garbage spaghetti code in the last three weeks that then works for the rest of the robot's life. everyone wants to build robots this way. We've been free of the original sin of being tied to a specific use case that's enabled us to build a highly reusable, adaptable, modular autonomy code.

[00:13:12] **Audrow Nash:** Yeah, so that sounds awesome to me. And you guys are using the robot operating system pretty heavily with this, so I'm, the way that I am thinking of this now is it's like it's an additional abstraction on top of ROS that manages a lot of things

[00:13:30] **Stefan Seltz-Axmacher:** Yep.

[00:13:31] **Audrow Nash:** Okay. Is it, could you almost say it's like a behavioral level where you say, I wanted to do these things?

Or how, or is it just unifying a lot of things? Or maybe it's

[00:13:40] **Ilia Baranov:** behavior control is a lot of what we do.

So we do have a behavior tree and a behavior engine, especially an API layer to command our vehicle and how that all interacts. but yeah, I get that a lot of roboticists, what people say. what you're describing is basically ROS, which like

[00:13:55] **Audrow Nash:** well, higher level, easier to input stuff and get it to do what you

[00:14:01] **Ilia Baranov:** and again. Yeah, and I

[00:14:03] **Audrow Nash:** Probably does resource

[00:14:03] **Ilia Baranov:** I give is

[00:14:04] **Audrow Nash:** all sorts of things.

[00:14:06] **Ilia Baranov:** exactly, and, the comparison I give is ROS 2 is a, is an excellent open source toolbox and we're providing just the whole house.

And yes, you could use the toolbox and build the house, or you could just go to us and we'll build you the house, or we have a house that we can just copy paste.

[00:14:21] **Audrow Nash:** Do you guys know in web development, there's like Ruby on Rails or something like this, which streamlines a lot of things, would you guys, would that be a fair comparison? Ruby on Rails, but for Robotics in some sense? Or is it not quite broad enough and

[00:14:35] **Ilia Baranov:** I, would

[00:14:36] **Audrow Nash:** on Rails, but four mobile robots I suppose,

[00:14:41] **Ilia Baranov:** for mobile robots, I'd say it's, even one layer above that. I, would say,

[00:14:47] **Stefan Seltz-Axmacher:** So, our, API, we have a relatively straightforward rest, API, where like commands might be, go to this GPS coordinate with this heading, and then we just do that. So like we have a customer, for example, who's a big conglomerate. they have an in-house built ERP, written by

[00:15:05] **Audrow Nash:** an ERP?

[00:15:07] **Stefan Seltz-Axmacher:** an enterprise resource, program.

So basically it's a software program that runs their operation, their multi-billion dollar operation. it's been written by this guy, like literally a guy, over the last 20 years as I think a monolith. In C#

[00:15:25] **Audrow Nash:** That's horrible.

[00:15:27] **Stefan Seltz-Axmacher:** can issue commands to our robots.

doesn't know much about geospatial data, he knows nothing about safety engineering.

He knows nothing about machine learning. He can issue commands to robots that we drive in their fleet. so that, for example, the first time he, we were doing a, an integration test, he was like, huh, I'm sending messages and you guys aren't moving. You've been making all these promises about your robots working and what's going on. and we looked at the message and the GPS coordinate he was sending us to was zero comma zero, which for those of you not, familiar with GPS is the middle of the Atlantic Ocean. we can enable our customers to just send simple commands, and even if they're unsafe, we won't do unsafe things.

Like we won't leave the geofence in that use case. If you try to order us to drive into an obstacle, we won't, unless you for some reason, configured us to do that So now a regular software engineer Yeah,

[00:16:21] **Audrow Nash:** saved something. Yes.

[00:16:22] **Stefan Seltz-Axmacher:** a VC during a demo.

[00:16:24] **Audrow Nash:** Ah, ha That's hilarious. Okay. Yeah. Ilia, were you gonna say something?

[00:16:31] **Ilia Baranov:** Yeah. So I think I was gonna expand a little bit on the API layer. our kind of mission is to make the API just behave as any other web API standard request and response so that anybody, any web developer out there that you can hire for 20 bucks an hour can suddenly hook up whatever system you have in house to a robot and do so without damaging equipment.

[00:16:55] **Audrow Nash:** I like that. How do you, the biggest question that comes to my mind with that is how do you manage state? Because it's complex. you tell the robot, go here, you have to wait till it's there. There's some sort of like underlying action like thing where, and then with arrest API, it's very you send something, it sends something back.

how do you manage that? Does it open up a socket or is, but then that gets more complex, or I guess how do

[00:17:21] **Ilia Baranov:** So we, actually, yeah, so there's two layers to that. The first layer of your question on, robot management is really using the behavior tree.

we fund, Steve Macenski's work in part in Nav2.

And, fans of it. We use big chunks of it. yeah, absolutely. It's fantastic work. And his, he has a behavior tree internal to Nav2.

We have one, a kind of a larger one that controls other stuff outside of Nav2, but very similar kind of concepts, similar, inspiration. And that manages things like the client has requested five different goals and halfway through it they interrupt us and give us a new set of four goals.

Should we then resume the original goals or should we change, or should, what logic state should we take?

So that's all on robot and that's all function of our behavior tree.

[00:18:11] **Audrow Nash:** if I send, two, two positions or something, it creates a queue. How do you, but so to me. That's probably the behavior expected, but it may be like, oh no, I actually changed my mind. I want to go to this one. I don't want to go to the first one.

[00:18:25] **Ilia Baranov:** so our rest, API,

[00:18:27] **Audrow Nash:** Okay. Yeah,

[00:18:27] **Ilia Baranov:** rest, API, when you send commands, you have either a preempt or a queue

[00:18:32] **Audrow Nash:** Oh, you guys have thought

[00:18:33] **Ilia Baranov:** we just provide all the, we, yeah, we provide all of those knobs. And actually a big challenge of building our API is we have hundreds of knobs we can adjust under underneath our layer and being very judicious on which ones we expose.

So our API doesn't just become this enormous surface area that we have to test thousands of options, but just the minimum possible set that is intelligent enough to, work in most circumstances.

[00:18:59] **Audrow Nash:** Yeah. Oh, I like that a lot. Okay, so I really like the idea of these, Ilia, is this your kind of, are you the master architect of all of this, or how

[00:19:11] **Ilia Baranov:** I wish

[00:19:12] **Audrow Nash:** how is

[00:19:13] **Ilia Baranov:** gonna nod, but it's actually, the engineering team. I'd say I, I'd say I, I do the least amount of engineering outta the team, thankfully. I think they're usually pretty happy when I'm not messing in the code because my code tends to be experimental and tests

[00:19:29] **Audrow Nash:** You're prototyping, you're trying to get it

[00:19:31] **Ilia Baranov:** I, I'm per, I'm, very much that sort of CTO and engineer Exactly. And I can do things quickly and kind of test things out. But really it's a huge credit to the engineering team who really get it to a quality level where it works every time and is safe and is functional.

[00:19:47] **Audrow Nash:** I like

[00:19:48] **Ilia Baranov:** and as much as I'd like to be that kind of person, I'm, not nearly enough of that kind of person.

[00:19:54] **Audrow Nash:** the thing is, so I've, seen companies where they have the master architect who builds everything. and they, or it could be build or it could be designs, everything. But the result that I've often seen is that some of the deci, like many of the decisions might be amazing, but some of the decisions were not, and they create unbelievable chafing.

And then it's also very hard to onboard new people into the system. So if you're working with a team, that's probably a very good way to distribute it and get some sort of consensus around the decisions, especially about the things that you're exposing, I would imagine.

[00:20:37] **Ilia Baranov:** Yeah. And I'd say really my function is in a lot of ways to keep refocusing the team on, let's make a general purpose of a piece of software as we can. 'cause often when we're working with a client, it's a very natural tendency to say, the client has requested X,

I'm gonna build a function, right?

I'm gonna build X and I'll often come in and re remind people like, X is A, subset of this larger function that more people would want.

Let's build that larger function and teach the client to use that 'cause. Then it immediately applies to our whole fleet

because.

[00:21:10] **Audrow Nash:** and you guys had, was it eight, eight people at the company?

Or something around there. 10.

[00:21:16] **Stefan Seltz-Axmacher:** Yep. Yep.

[00:21:17] **Audrow Nash:** And, so 10 people are, is almost everyone an engineer for this kind of thing or?

[00:21:23] **Stefan Seltz-Axmacher:** everyone. Eight

[00:21:24] **Audrow Nash:** eight out of 10. Yeah.

[00:21:25] **Stefan Seltz-Axmacher:** Yeah.

[00:21:27] **Audrow Nash:** Okay. And how long have you guys been going Just to, like how long has this company been around?

Okay.

[00:21:34] **Stefan Seltz-Axmacher:** Two, maybe. Two and a quarter.

[00:21:36] **Ilia Baranov:** Yeah, two and a quarter about right.

[00:21:38] **Audrow Nash:** How, how are you funding,

the initiative so far?

[00:21:44] **Stefan Seltz-Axmacher:** So we've, we've raised some money, a decent amount. we haven't announced it publicly. more, than a little, less than a lot.

[00:21:53] **Ilia Baranov:** one.

[00:21:54] **Stefan Seltz-Axmacher:** and, we also have this weird thing of customers paying us and SaaS margins, Yeah.

[00:22:02] **Audrow Nash:** What a thing.

[00:22:03] **Stefan Seltz-Axmacher:** Yeah. it's, crazy after trying to do a big monolithic, vertical Robotics company before where the, lift to get to enough robots to be profitable, was a, okay, we need $40 million.

But there's a very real world where we're just like a profitable company this year, and I don't know how to grok that. My inner, like my roboticist brain is just very upset with what do we do when more money comes in than goes out?

I think buy Lamborghinis

[00:22:31] **Audrow Nash:** get into hardware and then you can

[00:22:33] **Stefan Seltz-Axmacher:** Oh.

[00:22:33] **Audrow Nash:** You lambing you get

into,

[00:22:36] **Ilia Baranov:** that's the money pit.

That's the money pit we shovel the money into.

[00:22:40] **Audrow Nash:** yep,

Okay. I really like

[00:22:42] **Ilia Baranov:** it's, funny, on that note, just a, small anecdote, Stefan and I keep trading emails with our bookkeeper. 'cause we're always like, am I miscounting something,

[00:22:51] **Stefan Seltz-Axmacher:** this can't be right.

[00:22:52] **Ilia Baranov:** with our business plan?

it should be doing this and it's like doing this.

I don't understand.

[00:23:00] **Audrow Nash:** so exciting for those listening pointing up instead of down.

[00:23:03] **Stefan Seltz-Axmacher:** Yeah.

[00:23:04] **Ilia Baranov:** Yes. yeah,

[00:23:06] **Audrow Nash:** Very exciting to hear for robotics companies. Hell yeah. Love it.

[00:23:09] **Ilia Baranov:** yeah,

## Is your code open-source?

[00:23:11] **Audrow Nash:** what, I guess another kind of fundamental question. I look on the website, why are you guys not open source? is it because of the kind of competitive advantage of this, but why not?

why not? I guess there were probably discussions around this 'cause you guys like ROS and things like this, but what are you thinking?

[00:23:34] **Ilia Baranov:** I, took this, from a good friend of mentor of mine, Ryan Gariepy, at,

[00:23:41] **Audrow Nash:** He's wonderful. Yeah.

[00:23:42] **Ilia Baranov:** he had told me this. Yeah, he's great. and he had set this a long time ago at Clearpath and I, quite like the logic behind it, which is, we'll open source, anything that is useful to the community and not directly harmful to us.

So we actually open source as much as we can. a lot of the Nav2 stuff that we're, trying to help fund of course is open source. we have a big discussion going on how to fuse. GPS into Locus Robotics is fuse factor graph localization system. there's some efforts we're doing there. We have an open container initiative that's fairly public about a bunch of the containers we build use for build and infrastructure. the specifics, for example, of how our behavior tree dynamically generates nodes and makes sure that they're all talking to the same system is useless for anybody else because we already have built enough that it's weird and special

and so even if we did open source it, nobody would care. and also would cause more problems for us than it solves.

so when, whenever it hits those two, we try to, we open source anything that doesn't hit those two things.

[00:24:51] **Audrow Nash:** Makes sense. I would wonder I don't know, there are, it seems like there's a few companies that are in kind of similar space. I'd like a lot how you guys have carved out the mobile robots space. I think that was a very smart thing rather than we're gonna do all Robotics. That, that to me seems like a good decision.

I'd like to talk about that later. but some of them are going open source, hoping for additional adoption, I guess maybe Stefan, how, do you think about this? would it accelerate adoption if you made certain parts open source or even you could even have a high level Python library that just calls your API or something.

why, are you thinking about

Or

[00:25:38] **Ilia Baranov:** be clear, the API is open source, by

[00:25:40] **Audrow Nash:** Oh, okay. I just don't see

[00:25:41] **Ilia Baranov:** and at talking to the Oh, yeah, No, it's there. we,

we've gotta do a better job of marketing it, but like any documentation and code on, and I've even posted some YouTube videos on here's how you talk to our robots, here's how you use them.

All of that. That would actually make sense for customers. All open source, throw and pull requests. We love to review them. Yeah, no question.

[00:26:02] **Audrow Nash:** Okay. That's

[00:26:02] **Ilia Baranov:** it's the underlying ma, the

underlying pieces that are weird and special.

[00:26:07] **Audrow Nash:** as someone who's very lazy, I would expect at the footer on your website that there's a GitHub link and this kind of thing. That's exactly

[00:26:16] **Stefan Seltz-Axmacher:** good, maybe by the time you publish this podcast that will exist.

[00:26:21] **Audrow Nash:** Okay. Because that would be great. okay, so I misread the website in that case. that seems awesome. And, okay, so I guess,

Why are you carving out the niche of mobile robots only? Why aren't you doing arms? Why aren't you doing all sorts of other things?

## Why focus on mobile robots?

[00:26:42] **Stefan Seltz-Axmacher:** Yeah. so I think that has to do with a lot with what we've done before. I'm not an armed guy. I'm not a quadcopter guy. There's also a lot of people wanting to do arm stuff like this. There's a lot of people doing quadcopter stuff.

in both of our past experiences, we rebuilt stuff that we had already built and other people had already built a whole bunch of

times and then found it wasn't incredibly reusable.

so previously, when I had a, vertical self-driving truck startup, every time we'd get some big piece of press, I'd get a, bunch of inbound from random industrial companies saying, Hey, air quotes, you've solved autonomy. If we pay you $8 million, can you automate this super niche piece of equipment that only eight of in the world exists and no one else, uses, but is really valuable to us and we can't hire operators And because of how we're architected, as like some big monolith vertical thing, we'd basically always have to say no to that. It would be an entire pivot. It would be, throwing out 75% of the code base. And if you look at the big OEMs who built autonomy multiple times,

like some of 'em, one of them who likes to color green, has, has built autonomy at least like 15 or so times.

Never, none of those use, none of those rebuilds have used more than 25% of any existing code base.

None of them have cost less than $10 million. None of them have been completed in less than three years.

This is a, super key problem and is a big part in my, in our belief of why the Robotics industry sucks so hard. Because like people want robots to grade construction sites so they can start building or to till fields or to, spray, fertilizer on crops or to do whatever. And to even look at a use case like that pre Polymath, you might have to hire a consulting firm five to 50 for five to $50 million to build something that might only work for a demo day. And that does not build a good, strong industry. So like the arm people have done cool stuff in manufacturing. The drone people have done some cool stuff in, in, in toys and inspection and whatever. But for mobile robots that move through the earth, like we need to make it not so hard to make, to create value.

[00:29:09] **Audrow Nash:** I think that's a great idea. And it's so cool to me that, so going into the founding story

[00:29:16] **Stefan Seltz-Axmacher:** Yeah.

[00:29:17] **Audrow Nash:** coming to Polymath, Robotics, you guys, you,

so Stefan you were doing a, highway autonomous car up or autonomous truck, or what was it exactly?

## Stefan's experience starting Starsky Robotics

[00:29:27] **Stefan Seltz-Axmacher:** Yeah. So Starsky Robotics, we were doing self-driving trucks. We did, we, we started with a similar thesis as Polymath that robots are hard. the way we, that we were overcoming robots being hard is we do autonomy on the highway where it's a relatively constrained environment.

We do tele op in the first and last mile where it's kind of chaos. and then to make that problem easier, we'd control our own routes by being our own trucking company. and at the time when we were making a lot of hard technical decisions, 2017 ish, basically no vendors, would give you any part, unless you're willing to sign something that said you never rely on it for a driver route test. So as a result, what starsky became was this. Yeah. Yeah. So we talked to LIDAR companies, we talked to the Velodyne, we talked to,

[00:30:16] **Audrow Nash:** stuff, but don't use our stuff for real things. Is that what basically was?

[00:30:21] **Stefan Seltz-Axmacher:** Yeah,

yeah. legitimately that was what it was like.

So we ended

[00:30:27] **Audrow Nash:** They don't wanna be affiliated with it, I suppose if it goes poorly,

[00:30:31] **Stefan Seltz-Axmacher:** it wasn't illegal, it was just fear. I

think it's important to note in on-road autonomy. I haven't done a, an actual count in a while. I think there's five companies ever that have taken a person out on public roads. like

something like that. And there's in the range of probably $25 billion invested in the space. It is mostly not real industry or I think

actually the number might be a hundred billion dollars invested. but so, previously I'd done that and we had, because of robots being hard, we grew into this frankensteinian monolith vertical company. Where we had to do a, an incredibly not built here syndrome, hardware stack, an incredibly not built here syndrome, autonomy, tele op safety stack software for running your own trucking company and then running a trucking company.

I'd have to go from meetings where

[00:31:27] **Ilia Baranov:** Yeah.

[00:31:27] **Stefan Seltz-Axmacher:** just really, really hard. And I don't know if most people can be successful in that, in, in that type of business if

you

reinvent

[00:31:37] **Audrow Nash:** have to be like four CEOs at once to do that kind of thing. It seems like so many different businesses and industries that you're, and I don't know what your trucking experience is, but like you have to be a trucking business manager as well for all these things. So that sounds to me tremendously difficult.

[00:31:52] **Stefan Seltz-Axmacher:** I, think the re one of the main reasons that company didn't raise a Series B was because I was left less good at talking about the financials of a trucking company than a Fortune 500 trucking company CFO was,

which was a hard thing to be good at talking about right after explaining, safety engineering to someone for

[00:32:09] **Audrow Nash:** yeah, totally. Yeah. That's so interesting. Okay, and in that experience, you saw a bunch of these, it'd be like, okay, you get press. Then, it's oh, you've solved autonomy for these problems. Some people see it and then go, Hey, we really need something similar to that. And you saw these over and over again, and this is how you've come to Polymath,

[00:32:33] **Stefan Seltz-Axmacher:** Basically, big enterprise believes in autonomy.

Like big mining companies, big farms, big factories, they all have labor shortages.

They've seen enough headlines about how self-driving is here, and they're looking around and thinking like, I can't hire people to work in my lumber mill. I can't hire people to work in my port.

I can't hire people to work in my rail yard. maybe some robots could move this stuff from A to B. And before Polymath, maybe there was someone who happened to be building the right solution on the right vehicle, like a, perfect unicorn of a vertical lineup.

Or maybe you had to hire a consulting firm to build you something from scratch.

[00:33:15] **Audrow Nash:** So you are allowing companies to build up around specific vehicles that big companies are using, and you provide a lot of the research and basically the infrastructure that they need to build to do

[00:33:30] **Stefan Seltz-Axmacher:** We give them a code base that will just work. we can connect them to, with people to do the retrofits. and we can take commands from whatever their weird system for running their businesses

[00:33:40] **Audrow Nash:** Cool. Cool. That seems so, I really, oh yeah, go ahead.

## A good task to automate and not get lit on fire

[00:33:45] **Ilia Baranov:** a I'll, give you a fun, illustrative example, which is my favorite one. We haven't done this yet. I keep hoping that eventually we'll get to this mission,

but there's this, problem in metal recycling where if you recycle a bunch of metal, you end up with this big molten pot with a bunch of slag on the top. Once you dump out the, useful

[00:34:04] **Stefan Seltz-Axmacher:** and by like big molten pot. imagine maybe, a cauldron with a, radius of like 10 feet and like maybe

[00:34:16] **Ilia Baranov:** a backyard pool.

[00:34:17] **Audrow Nash:** like something a villain would fall into at the end of a

[00:34:20] **Ilia Baranov:** yeah, exactly. Exactly.

[00:34:22] **Stefan Seltz-Axmacher:** what kills the bad guy in Terminator

[00:34:24] **Audrow Nash:** Yep. Yep.

[00:34:26] **Ilia Baranov:** Yeah. So it's this enormous crucible. And what they have to do is they have to pick it up, drive it outside to a particular dump site and dump it over And there's a purpose built machine. There's a purpose-built machine that drives this thing. And it's a heinously dangerous job because if you accelerate too quickly or

suddenly break or have a bump, liquid metal splashes the vehicle and catches on fire.

[00:34:49] **Stefan Seltz-Axmacher:** and you die.

[00:34:49] **Ilia Baranov:** the vehicle's pur and you die. Yeah. The vehicle's purpose built that, the like liquid metal fire death is at the back and the propane tanks running the vehicle are all the way at the front

to make sure that as far away as possible, there's probably like 200 of these vehicles on the planet, but they're so ludicrously dangerous that, like perfect case for autonomy, same spot every day, same exact conditions, perfectly designed space, but the guy's getting paid a ton of money

[00:35:21] **Audrow Nash:** I was gonna say they

[00:35:21] **Ilia Baranov:** because it's dangerous.

[00:35:23] **Audrow Nash:** year or something

[00:35:24] **Stefan Seltz-Axmacher:** they also, a thing Ilia, I don't know if I've told you

[00:35:26] **Audrow Nash:** at a high rate.

[00:35:28] **Stefan Seltz-Axmacher:** at, another thing I learned about this use case recently is it's also incredibly carcinogenic. So even though the guys might be making 300k a year after 10 years, they have all sorts of unpleasant cancer.

so if you, if you think about like vertical autonomy for that solution, there's 200 of those vehicles in the in the world.

Does it make sense to spend $50 million to learn how to automate Just that,

it literally might be cheaper to just give people cancer than to build one off autonomy for that.

use case. Yeah. the mar the market has accepted cancer over the status quo in Robotics.

[00:36:07] **Audrow Nash:** Oh my gosh.

[00:36:08] **Ilia Baranov:** But meanwhile, it's the same steering wheel, the same gas and brake pedals, like a human's driving it the same way that we drive our test tractor.

So there's zero reason we can't stick a few sensors and actuators on there with a retrofit partner and then have day one perfect autonomy just like we have on the rest of our fleet.

[00:36:27] **Audrow Nash:** That's super cool. I don't, so

one thing that I don't fully understand is, the sensors, so you said earlier that you use a lot of the sensors that are on these vehicles. I would imagine you want additional ones, for autonomy. So I would think vision would be really useful. Maybe LIDAR would be useful.

You might want an IMU or whatever. so do you have a little box of sensors you put onto these vehicles sometimes or

## Integrating with sensors

[00:36:55] **Ilia Baranov:** I wouldn't say a box, I would say. Yeah, case by case, but generally speaking, the main ingredients are some sort of feedback from our vehicles. Just even a, live or not a live state is useful. So on that 1997 bulldozer, we at least know the engines turning over.

So we have some concept of health. but even better than that, if it has a speedometer, feeding in the speedometer is a nice ground truthing for us

[00:37:20] **Audrow Nash:** Okay. And would, do you do

[00:37:21] **Ilia Baranov:** If we're standing still, we're standing still.

So even that layer of data is, even though it's coarse, it's useful for us as a, error checker for everything else.

[00:37:30] **Audrow Nash:** Do you tap the vehicle system in that case, or do you put a camera to just look at it or, oh, okay.

[00:37:37] **Ilia Baranov:** we tend to just use the CAN bus if it's there.

if it's not, we'll put a little encoder on the, again, it's not us, right? It's our partner teams, our integrators, put a little encoder on, part of the drive shaft or camera staring at the dashboard. Worst case. But that one, usually the update rate is, eh,

[00:37:54] **Stefan Seltz-Axmacher:** and then we'll have a bunch of different sensors added, depending on the use case. So it could be LIDAR, it could be stereo cameras, could be radar, it could be, whatever. an interesting thing that we found is people have really strong opinions about sensors. if we were just a LIDAR shop, there are, we would have fewer customers than we have right now.

if we were a never LIDAR shop, we would have fewer customers than we are right now. And I

[00:38:19] **Audrow Nash:** gotta support em all. Yeah.

[00:38:21] **Stefan Seltz-Axmacher:** Yeah. And like the thing is when everyone builds their robot as like a monolith, what happens is there's so many crappy parts of your code that at some point some demo was ruined because a velodyne LIDAR wasn't behaving properly.

Or at some other point a demo was saved because, oh look, we replaced that LIDAR with an ouster or replaced it with a Zed camera. so now every robot forever needs a Zed camera on it. And we need to be able to, work with both of those strong opinions. And my hunch is every listener here has some sensor out there that they hate and another one that they love.

[00:38:58] **Audrow Nash:** Yeah. That's so funny. Yeah. And you guys, it makes sense. Catering to, or not catering to, but allowing all of the different sensors that people might want to use.

[00:39:10] **Stefan Seltz-Axmacher:** Yep.

[00:39:12] **Audrow Nash:** Okay. So that's really cool.

And I like, so a thing that is very interesting to me about this is that what you guys are doing, I.

It's like okay, so you mentioned those 200 vehicles that are doing the super dangerous metal hauling, liquid metal terror. That just sounds awful. But so you have 200 vehicles that are doing that. That problem does not it, like some companies want to pay a lot of money to do that, but it doesn't make sense for a venture capitalist to be investing in a company that does that because you have 200 of these vehicles, it's not gonna grow that much.

Maybe you can apply it to other things. but they're looking at the market that's gonna buy right now. And so it's really interesting to me 'cause I've seen, I feel like with a lot of the Robotics companies that I see is they pick one little vertical like that and then they go build something in that.

And it's not that attractive to venture capitalists because they want to buy in at a fairly late stage where they go, oh you are, you clearly have market traction, whatever, and you need this big injection of cash for doing something, but I want to see a 10 or a hundred times return in five years or something like this.

You guys are doing it clever where you're agnostic to all these problems and you let other companies go and be profitable on those vehicles.

but there's a lot of growth that you guys can do, which is quite exciting, I

## Approaching the problem from another side than most robotics startups

[00:40:39] **Stefan Seltz-Axmacher:** yep. And we can make a lot of betts in a lot of different industries, where if our, customers are successful, we'll be successful. but we can simultaneously make betts in metal recycling as well as forestry, as well as ports, as well as this, that, and the other. And as long as some people build robots that create real value, we can make sure the robots work.

But in a lot of these use cases, the real value comes from what they're told to do.

So if you think about robots in a port, for example, driving a yard truck with a trailer, is not special. There's something like five to 15, yard truck autonomy companies that are doing just that.

There's, an incredible, diversity of yard truck manufacturers. So if you're vertical, you have to figure out which ones you're gonna integrate ones, which ones you don't. The really important thing that yard trucks do is they get commanded around by some system that manages a yard, management system. And that system might be configured so that, maybe there's five lanes going from north to south, and on Wednesday morning a big ship is coming in. So four of those lanes are coming away from the ship where one lane is going towards the ship. And, an hour later you reverse the traffic the other way around.

and that way you can get the ship empty two hours earlier, which means you can have five more ships visit per year and blah, blah, blah.

That's the stuff where you're actually gonna make a billion dollars with robots. If you're reinventing our part of the stack,

[00:42:11] **Audrow Nash:** Oh,

[00:42:12] **Stefan Seltz-Axmacher:** you're missing

[00:42:13] **Audrow Nash:** you mean.

[00:42:14] **Stefan Seltz-Axmacher:** because a lot of teams doing yard trucks are spending all their effort building what we build and not like intelligent yard management based on machine learning statistics and blah, blah, blah. And that's really the cool part of being a yard truck company.

[00:42:30] **Audrow Nash:** Yeah. So yeah, I agree. So if you do the super big tasks made by these super big consumers, you can be rewarded handsomely and be a billion dollar Robotics company,

[00:42:45] **Stefan Seltz-Axmacher:** Yep. And if you're, and if you build and if your autonomy stack sucks, you don't get any of it.

[00:42:50] **Audrow Nash:** Yeah. And you have to build that. And that's a heavy investment initially. So you guys are helping enable that, which is quite cool.

Now, I would love to hear what are your ambitions for this company for, and I'd love to hear both of your perspective on this, to like, where do you want this to go? Because it seems like a slightly new business model to me, which is quite cool. maybe we start with Ilia, like where, are we going in the long term?

Like how, do you see you guys growing?

## Ambitions for Polymath Robotics

[00:43:20] **Ilia Baranov:** Yeah. From, the technical standpoint, I think the interesting part of our business is, again, drawing that operating system kind of comparison. you buy Windows to then run Excel or games or whatever, right? I think because we're really focusing on A software and B only motion software. and the edges of what motion means will blur over time. concrete example really clearly, really quickly that bulldozer will control, the bulldozer will control the blade somewhat, but if a builder says, here's a site plan, dig the site plan autonomously, we'll probably partner with somebody who specializes in translating site plans to blade control to whatever, and we'll drive it and work with them. So I think the, technical interesting part is we're building a foundation to then have. a web store. If, you talk about what, universal robots did, I really like what they did for arms, right? Is here's the arm, here's the foundation, but like here's 50 different companies that will take our arm and then make Apple picking or make CNC machine tending or whatever.

It's the same thing is, take our autonomy core and then build on top of it and here's a bunch of vendors that will sell you pre-baked modules to do agriculture with autonomy, to do mining with Polymath autonomy.

We can do those pieces, but I think we'll never outcompete thousands of people using our

[00:44:44] **Stefan Seltz-Axmacher:** And I, and we don't know how to run a mine. We don't know how to run a forestry operation. We don't know how to

[00:44:48] **Audrow Nash:** saw this with your trucking company. I

[00:44:50] **Stefan Seltz-Axmacher:** Yeah. I had to learn how to run a trucking company, which turns out is not simple.

[00:44:56] **Audrow Nash:** No, everything's hard when you get into it, I think. Yeah. Okay. So that, I really like that point. It's interesting to me how, it seems like I. So many of the companies that I've talked to on this podcast, it's like the vision eventually scales to being something like an app store with this kind of thing where you allow the functionality, you provide the core platform, and then people can build off.

And that sounds like where this may go. and it's just, to me, it feels like an exciting time in Robotics that maybe this will actually occur. 'cause it seems like a lot more people are working on it recently, and have good go-to market strategies to get there for this kind of thing. At least from my perspective.

[00:45:39] **Stefan Seltz-Axmacher:** Yeah, absolutely.

[00:45:41] **Audrow Nash:** and Stefan, what do you hope,

like where are you, what are your ambitions with this?

[00:45:46] **Stefan Seltz-Axmacher:** yeah, so my last company, start was my first ever startup, and it was really hard. And at the time I didn't know how much, it was hard because startups are hard and how much, it was hard because I was building robots and running a trucking company and writing regulations and blah, blah, blah, blah,

[00:46:04] **Audrow Nash:** You were five CEOs at once? Yeah, for sure.

[00:46:07] **Stefan Seltz-Axmacher:** and then after that I went and hung out with some SaaS companies and holy crap.

like, assuming Audrow that you've never worked at a, at a, just a normal SaaS company, DocuSign 5.0 SaaS Company. The way that you start a SaaS company like that is you have a producty salesy, CEO. You have a generalist, 50th percentile engineer who can talk to people but can mostly write glue code. That product guy figures out like what you should be building. The glue code engineer finds a bunch of microservices, ties them together to build it. And like theoretically in five years, they're each, worth a couple hundred million dollars. Whereas in Robotics it looks almost like, it looks like the world of PCs back in the seventies where screw Steve Jobs. You need like Steve Wozniak who can like code and binary and design his own circuit boards and build gooeys and make them useful. And like without an army of Steve Wozniaks, you have no product.

Like the Robotics industry will never get beyond that phase if everyone has to keep on building point-to-point navigation.

If Polymath can enable the market to just focus on things that work and it's still not gonna be as easy as DocuSign 5.0. But if Polymath makes it so that building a robot is as easy as making a website in 1998,

then like we're gonna start to actually have robots.

We're gonna actually start to have cheaper, better food. We're gonna have, cheaper materials. We're gonna have cheaper cost of living. We're gonna enable a whole lot of the world to live as nice as we do in, in the, west. And I think

that like along the way, if we enable that, we'll make a whole bunch of money and build a cool thing.

So that's what I think, that's what I'm hoping

[00:47:57] **Audrow Nash:** Good for you.

And, exciting problems. 'cause to me what it seems like it's not, it's a lot more exciting than this, but it sounds a little bit like a lifestyle startup in some way. And what I mean by

## Running a different kind of business with fewer hats

[00:48:13] **Stefan Seltz-Axmacher:** What do you mean?

[00:48:15] **Audrow Nash:** so what I mean is that you get to leverage the power of the, SaaS model in some sense where you don't have to be, you're, only one CEO at this time.

You're not five.

[00:48:26] **Stefan Seltz-Axmacher:** yeah,

[00:48:26] **Audrow Nash:** And so it, it seems like it's a bit easier. You guys are profitable early, so you're not like lighting the ground on fire behind you and running like you would be if you're taking investment. maybe lifestyle isn't the way to say it, but like it's more on your terms in a

[00:48:43] **Stefan Seltz-Axmacher:** Yeah. we get to be,

[00:48:45] **Ilia Baranov:** you're a, you, accidentally slandered, Stefan there by using

[00:48:49] **Stefan Seltz-Axmacher:** I, I,

[00:48:50] **Ilia Baranov:** lifestyle. No kidding, kidding, Purely kidding. VCs will use lifestyle business as like something

we shouldn't invest in, which is not

[00:49:00] **Stefan Seltz-Axmacher:** like, why would you ever want to just be rich and have a nice life that's terrible.

[00:49:05] **Audrow Nash:** You,

[00:49:06] **Ilia Baranov:** No, you have to make them rich first. That's your goal. Yeah.

exactly.

[00:49:10] **Audrow Nash:** real good, you do our 10, 10 CEOs. Yeah,

[00:49:13] **Stefan Seltz-Axmacher:** what's funny is compared to a normal full stack vertical Robotics company, this feels incredibly easy compared to my friends in SaaS. This is still incredibly

[00:49:23] **Audrow Nash:** hard.

[00:49:25] **Stefan Seltz-Axmacher:** and I think like even, in 10 years or so, the, some of the modules that we sell as individual products that like, as a part of our stack, there will be billion dollar companies that just

do things like SLAM or just do really clever path planning for diff drive, vehicles.

there will be industries like that, but right now it's rather radical to say, oh, we'll just take the autonomy core off your hands

[00:49:55] **Audrow Nash:** You mean make it so they don't have to do that?

[00:49:58] **Stefan Seltz-Axmacher:** Yeah.

[00:49:58] **Audrow Nash:** you can

[00:49:59] **Stefan Seltz-Axmacher:** Right now that, seems radically easy. In 10 years it will seem radically hard.

[00:50:04] **Audrow Nash:** Yeah. It is amazing how that seems. Like building a website now is still difficult. if you wanna build a fully featured SaaS stuff, like a lot of my side projects are SaaS stuff. and like it's still a lot of work. but it's so much easier than Robotics projects, which is just bonkers.

## Stefan's bankrun t-shirt campaign

[00:50:22] **Stefan Seltz-Axmacher:** let, lemme tell you a version of that. I had a side project, an e-commerce side project a couple months ago.

I've never actually publicly in any setting admitted was, me. So this is like an Audrow Nash exclusive

[00:50:35] **Audrow Nash:** Cool. You heard it here.

[00:50:36] **Stefan Seltz-Axmacher:** So yeah, so early last year, I got wind on a, WhatsApp group for YC founders that, something weird was going on at SVB. and like a panic was happening and

[00:50:49] **Audrow Nash:** That was Silicon Valley Bank, that big one that collapsed a while ago.

[00:50:52] **Stefan Seltz-Axmacher:** yep. And I panicked early, like I panicked on that Wednesday night, which meant we got our money out like relatively soon.

But while I panicked, I had a, like a dark joke that like the Silicon Valley Bank run was kinda like a marathon run. so I went on Fiverr and I basically paid a Fiverr, I think 20 bucks to make a t-shirt design for what a bank run marathon T-shirt would look like.

so 25 bucks,

I bought the domain name, I think SVB run 23, which sounded like a good marathon run.

so that was 10, $15. And then I set up a store on Teespring, and I don't know if you're familiar with Teespring,

[00:51:34] **Audrow Nash:** Yeah. Open. Robotics uses it

[00:51:37] **Stefan Seltz-Axmacher:** Oh, cool. So for those of, for the listeners who don't know, Teespring, Teespring will make it easy to do like a screen printed shirt business where you can just upload a shirt design and they will print the shirts and ship them and do all of that.

So I paid for the premium version of Teespring for I think 20 bucks.

And for $75, I had an e-commerce site with a line of nine different takes on SVB Bank run marathon shirts, which I posted in a handful of links. And I suddenly had an e-commerce site that got me, I was a top of 1% Teespring creator that month.

and if that was a real business, that could be a thing that I did. And, it has nothing to do with robotics in terms of how hard it is. It is a

[00:52:23] **Ilia Baranov:** I add a little bit of, can I add a little bit of late breaking news? This will be a surprise to Stefan too, in the full circle of e-commerce. You are also immediately ripped off by a

[00:52:32] **Stefan Seltz-Axmacher:** yeah.

[00:52:34] **Audrow Nash:** Oh,

[00:52:34] **Ilia Baranov:** This is your exact design,

[00:52:36] **Audrow Nash:** no way.

[00:52:37] **Ilia Baranov:** seller

[00:52:37] **Stefan Seltz-Axmacher:** that's on Etsy.

[00:52:40] **Ilia Baranov:** Etsy.

[00:52:41] **Stefan Seltz-Axmacher:** what a schmuck. There was also, there's also another person ripped me off on, Teespring and Teespring refused to do anything about it.

[00:52:50] **Ilia Baranov:** yeah.

[00:52:52] **Stefan Seltz-Axmacher:** But, I think

[00:52:52] **Ilia Baranov:** of e-Commerce Life.

[00:52:54] **Stefan Seltz-Axmacher:** but like you can literally set up an e-commerce store without like even opening up Photoshop, to make your own products.

Like Robotics is not gonna look like that for at least 20 to 30 years, but that's. If, robots are gonna be a real part of our life, if robots are gonna bring us the promise that I think everyone in this conversation wants them to bring, they need to get a lot easier. And

that's what we're hoping to do.

[00:53:16] **Audrow Nash:** Hell yeah. Okay. I really like that. what's the, so you guys are 10 people now.

[00:53:24] **Stefan Seltz-Axmacher:** Damn Etsy store.

[00:53:26] **Audrow Nash:** I know that's so fricking funny. you made it that you got ripped off. That's great.

[00:53:32] **Ilia Baranov:** I think we need to open an Etsy store for Polymath shirts. By the way, like the one that Stefan's wearing right

now for the listeners, he's wearing a shirt that just says Total ROS bag on it. because we had an internal joke at Polymath that oh, anytime anybody would do something bad, it'd be like, ah, you ROS Bag. So

[00:53:50] **Stefan Seltz-Axmacher:** It doesn't work as well with mcap.

[00:53:52] **Ilia Baranov:** you. Yeah.

we also have MCAP hats. We have MCAP hats

too. Yeah. Anyway,

[00:53:59] **Audrow Nash:** Hell yeah. let's see, I lost my train of thought with this. That's very funny. All the swag at everything. Oh, so what's the, growth plan for this? so you guys are, 10 people now you're,

that line is going up, so it sounds like you're profitable or becoming like you're,

you'll

[00:54:20] **Stefan Seltz-Axmacher:** we're not profitable yet, but it seems like we're, it seems like

[00:54:22] **Audrow Nash:** on the trajectory, two years and starting to move in the right direction.

That's wonderful.

how, do you imagine growing or do you need many more people for the work you're doing or will it be like, there'll be like system integrators that help push it out and maybe you can focus on a few promising,

## How Polymath plans to grow

[00:54:40] **Stefan Seltz-Axmacher:** Yeah.

[00:54:41] **Audrow Nash:** areas or like what are you thinking for how to grow in the future?

[00:54:45] **Stefan Seltz-Axmacher:** So it's funny, like right now more of our problems are like business problems than they are, Robotics

[00:54:50] **Audrow Nash:** Technical

[00:54:51] **Stefan Seltz-Axmacher:** is also weird. Like I didn't think that

could happen in Robotics. So we need, like, we're, essentially we might go raise again or we might just grow to profitability depending on how the VC market's at and which could be a whole other conversation.

but if we suddenly had 10 more people, probably half of them would be business people doing stuff like account management and like splitting functions into other things.

[00:55:17] **Audrow Nash:** It's interesting to me 'cause it feels like with a lot of hardware companies, say like medical device companies, as the company moves across time, the staffing changes pretty significantly. So you have a lot of like researchers and our engineers at the beginning and then once they make something it's okay, now you need way less of them and now you need like a big legal team or certification or I don't know, whatever.

Then marketing and who knows. but it seems like you guys are going through that as well where, okay, we had a bunch of engineers, eight of the 10 were engineers. Now you probably need another 10 business people.

[00:55:50] **Stefan Seltz-Axmacher:** another five.

[00:55:52] **Audrow Nash:** Okay, something like

[00:55:54] **Ilia Baranov:** and I think the key metric that I convinced Stefan over time to start tracking is our robot to employee ratio.

I really my

[00:56:02] **Audrow Nash:** it right at

[00:56:02] **Ilia Baranov:** is to get to 10 to a hundred

Yeah. Robots to employees.

[00:56:08] **Stefan Seltz-Axmacher:** and also when

IA says that I, IA actually means different types of robots, not even specific robots.

[00:56:14] **Ilia Baranov:** not even copies.

Yeah. 'cause copies to me are like, eh, whatever. It's

the exact same

[00:56:19] **Audrow Nash:** they're free.

You already have it working,

[00:56:21] **Ilia Baranov:** yeah, exactly.

[00:56:22] **Audrow Nash:** but I guess those 1% cases will come up more, for this kind of thing. So not totally free.

[00:56:29] **Ilia Baranov:** No, yeah. I'm, big, a

[00:56:32] **Audrow Nash:** Facetious. Yeah, for sure.

[00:56:35] **Ilia Baranov:** but yeah, no, I think as we grow, I think we will still need quite a significant engineering presence because one of the reasons we sell ourselves as SaaS is that we're continuously improving every piece of our stack. especially actually we can get into this in technical detail in a bit, but, the machine learning part of what we do is actually a very small, thin. Sugar sprinkling on top of the cake

in a lot of ways where it's, a key differentiator in some ways, but in other ways actually, there's so much fundamental to do at the underlying layer that we gotta get that large and expanded first.

## How Polymath uses machine learning

[00:57:14] **Audrow Nash:** What's the, what is the

[00:57:15] **Stefan Seltz-Axmacher:** I think to,

[00:57:16] **Audrow Nash:** of your

[00:57:17] **Stefan Seltz-Axmacher:** yeah.

[00:57:18] **Audrow Nash:** about that at all. I, don't know what

it

[00:57:20] **Ilia Baranov:** I'll give you a con, I'll give you a concrete example. So we have an application in forestry and we have a LIDAR system. And you can imagine in a dense forest, you're not getting very much GPS. So there's a lot of complexity on localization, orientation and heading management, obstacle avoidance, those kind of things. but from a LIDAR point cloud, you can't really tell if the thing you're seeing is a bush, which you're supposed to just drive right over 'cause you're a multi ton vehicle. Or is it a boulder, which if you try to drive over, you'll damage your drive train,

right? And that's sort of stuff that's where ML will come to play a role with, image data or LIDAR data, which classical algorithms can't do quite as well. You can think of some heuristics maybe, but honestly, like

any heuristic you can think of, a bush in a boulder will look similar at some point from some angle. whereas camera data and humans can tell 'em apart pretty easily.

[00:58:12] **Audrow Nash:** So the.

[00:58:12] **Ilia Baranov:** that's a case where that extra guidance, even though the, all the underlying pieces to navigate and pathway and obstacle void, the extra guidance allows us to not make suboptimal decisions of avoiding a bush when we can just drive right through it.

[00:58:26] **Audrow Nash:** Gotcha. Yeah. So these are in your modular framework. These are components you can add, that might improve applications. Maybe you say, okay, I have this path planning and this path planning effectively has a plugin or something that says, is Bush or not is bush or rock or something like this. and you can have machine learning determine which one it is.

So that's interesting that you guys are getting into that.

[00:58:52] **Stefan Seltz-Axmacher:** but like a relatively weird opinion. Yeah. But like a relatively weird opinion that we have. Is in Robotics. there's a lot more ML in MO in the world of Robotics and the market of Robotics and the products of Robotics that you can buy. ML is a lot more commodified than like really good Robotics software that is reliable and turns on every time and spits out metrics for why it doesn't work. And deployment infrastructure so that you don't have to send people to west, west Nowheresville, to go fix a robot in the middle of the day night with a, eight hour notice or, controls engineering that can smoothly drive vehicles of very various different sizes. And I think, I think there's this weird market dynamic going on where the VCs are really stoked about like machine learning.

'cause they just got to see what like LLMs can do and like a way that they can directly interact with and they're pretty amazed. Whereas I don't know, I'm pretty stoked by robots that turn on every time. And I know how few large Robotics organizations that is true for, so we're focusing a lot more on those kind of fundamentals.

[01:00:07] **Audrow Nash:** Yeah, no, I think that's smart. a lot of the, I don't know, it's very interesting to me because there are some things that they, like machine learning seems well suited for. but there's a lot of things where we think it's good, but then it isn't when you try it. And, like the problem with Robotics now really seems to be a lot of exceptions pop up when you bring robots into a less structured environment.

and those, I just, it's very hard to imagine a lot of machine learning, doing very well with a lot of those. I just I don't know, I'm doing some thorny coding, for work and the, it's it's complex. There's all sorts of hidden stuff that's hard to understand and, I'm asking LLMs advice on how to do this kind of thing and.

All their advice is garbage for this kind of thing. It's like I've actually gone to, looking at these and just Googling, because it is le it's a, it's like it will look convincing and it looks like it's gonna work and then I try it and it just doesn't, and I can imagine that this pops up a lot in Robotics applications.

[01:01:24] **Stefan Seltz-Axmacher:** so the exceptions thing is actually part of why off highway or like large vehicles are really neat.

So basically all of these different industries, from like ag to mining to whatever suffer labor shortages they like, they

## Big and expensive vehicles are easier to automate?

[01:01:38] **Audrow Nash:** everything is suffering labor

[01:01:40] **Stefan Seltz-Axmacher:** spend enough money

to hire enough people to do the work.

So as a result, they need, a smaller number of people to do the same amount of work, which means that machines get bigger and bigger. when machines

[01:01:53] **Audrow Nash:** It's like shipping containers that are just absurdly large.

[01:01:57] **Stefan Seltz-Axmacher:** yep.

[01:01:58] **Audrow Nash:** Yeah. So they make one person do what 20 used to do

[01:02:02] **Stefan Seltz-Axmacher:** so there's

[01:02:02] **Audrow Nash:** 20 times larger machine, this kind of thing. Okay.

[01:02:06] **Stefan Seltz-Axmacher:** And what's cool about that? First of all, the machine does

more valuable work. You, can spend more money on sensors for it.

So that's useful for us. but more than that, big machines are really dangerous, so they drive more cautiously. a 500 ton dump truck.

[01:02:24] **Audrow Nash:** interesting.

[01:02:25] **Stefan Seltz-Axmacher:** yep. Basically the most valuable machines in the world to automate are among the easiest

[01:02:33] **Audrow Nash:** Aha. That's wonderful. Yeah. 'cause Oh,

[01:02:35] **Ilia Baranov:** giant mining truck or the molten metal transporter is way easier than astro in your house, like orders of

[01:02:44] **Stefan Seltz-Axmacher:** order. Yeah.

and like the 500 ton, dump truck, I think Caterpillar gets a million dollars a year for each one of those.

[01:02:53] **Ilia Baranov:** recurring,

[01:02:53] **Stefan Seltz-Axmacher:** recurring SaaS.

[01:02:55] **Audrow Nash:** Wow. That's so crazy. What a funny thing that just, it makes complete sense, but I hadn't thought about it. Where the ones that are the most valuable and then also like you could strap expensive sensors on them, and relative to the total cost of the thing, it's

[01:03:09] **Ilia Baranov:** And they're big, so there's a lot of space for them. There's a lot of power, there's a lot of storage

for compute. Like all of your problems get easier at larger scales. There's also an interesting, to harken back a little bit to where we see things going as our type of approaches are hopefully us get more and more successful.

You don't need these large vehicles anymore.

'cause one of the labor shortages You can go back to small. and which kind of dovetails nicely with sensors getting smaller and compute getting more efficient over time. but there's a funny kind of story I heard from the South African mining industry where they use, they're, very active in mining.

They have good regulatory body for autonomy, but they have a black market for tires for these large, vehicles

where getting a new tire if it blows a tire is like a four month process.

And in that

time

[01:04:02] **Stefan Seltz-Axmacher:** And

[01:04:03] **Ilia Baranov:** of dollars.

[01:04:04] **Stefan Seltz-Axmacher:** that truck might be responsible for moving $10 million in material a day. So if it's outta commission for 90

days, yeah. We've lost a lot of money.

[01:04:13] **Ilia Baranov:** Enormous, money. And so it's, the incentives are so high that they have people running around stealing tires from each other

[01:04:19] **Audrow Nash:** Ah,

[01:04:20] **Ilia Baranov:** like at that point, you'll pay a group a million dollars to get you a tire, no problem.

so if you're, if, and these size vehicles are so large that they get shipped in pieces to the site,

assembled

[01:04:33] **Audrow Nash:** then assembled by

[01:04:34] **Ilia Baranov:** their entire life on site,

[01:04:35] **Audrow Nash:** Yeah.

[01:04:37] **Ilia Baranov:** and then left there, and then left there.

When the site is done, the vehicles are

[01:04:42] **Audrow Nash:** They're not even worth

[01:04:43] **Ilia Baranov:** You don't have to

[01:04:44] **Stefan Seltz-Axmacher:** Yeah.

[01:04:45] **Ilia Baranov:** yet, you don't have to do any of that. If you have a smaller vehicle,

you just put 'em on the bat of a flatbed truck and you just have a, instead of one giant one, you have 10 medium or, 30 small size.

If one of them breaks, you only lose a 30th of your effectiveness.

[01:04:59] **Stefan Seltz-Axmacher:** and when they get smaller, they get easier to electrify too.

[01:05:03] **Audrow Nash:** Oh, that's a cool point.

Okay. Which that's desirable because it's just clean, easy to maintain. You don't need big, like diesel, high pressure, hydraulic,

[01:05:15] **Stefan Seltz-Axmacher:** I'm, if you like the idea of sometimes there being snow, more electric vehicles seems nice.

[01:05:24] **Audrow Nash:** is that? That doesn't make.

[01:05:26] **Stefan Seltz-Axmacher:** Sorry.

if you like the idea of not

[01:05:28] **Ilia Baranov:** change

[01:05:29] **Audrow Nash:** facetious. Ah,

[01:05:31] **Stefan Seltz-Axmacher:** Sorry.

[01:05:32] **Audrow Nash:** it went right over my head. Yeah. Yeah. Still don't get it.

[01:05:35] **Stefan Seltz-Axmacher:** wasn't my best climate change joke?

[01:05:39] **Audrow Nash:** One thing that's interesting to me, so Electric Sheep, the first interview that I had on this podcast, they also had a similar thing where they were. Instead like the constraint, was exactly as you've said where they were trying to do lawn mowing. And companies have fewer people so they get bigger mowers and bigger mowers are more dangerous, but they probably also go fast for that 'cause they gotta mow quickly.

and so what they said is we can remove that assumption and have a whole bunch of small mowers. so that seems like where it goes eventually, but you guys are preparing for the near term where you can automate these single large vehicles and get a lot of bang for the buck there. And then as you automate, I suppose then we can remove that restriction as we build more robots and things like this

Yeah.

So you build, basically we need more deployed and the new generation can start to be smaller ones that can then use the thing, but we get to start on the big ones and it's easier, which is just glorious. Like what a great

[01:06:41] **Stefan Seltz-Axmacher:** you need to, and you need to deploy on the equipment people have today. Like I've heard of autonomy programs that. Like for some use case, have gone to customers we've talked to and said, all right, cool for us to save you $500,000 of labor cost per year or $750,000 of labor cost per year. Step one is you need to buy $15 million of new equipment.

'cause we only can work with this one specific type of vehicle. And yeah, weirdly enough, those autonomy deployments never happened.

So like we have to be able to meet the market where it is today on the vehicles that it's using today, and then as, the needs around having physically present labor go away, the market can move towards smaller, more electric, more nimble vehicles goals.

[01:07:26] **Audrow Nash:** I like that a lot. Yeah. And then you don't have, I guess then you can remove the black market for these tires and things like this. 'cause smaller ones are probably easier to procure. That's great. Okay. What a cool thing. What, so we touched a little on AI and machine learning.

What do you guys generally like, just because it's so topical, what do you guys generally think about all the generative artificial intelligence stuff?

And also, there's a lot of other exciting work where it's like learning from demonstration. There've been some cool demos lately. and just, and even like end-to-end Robotics learning stuff where they do a lot in simulation and then learn the final things in the real world. what do you guys think there?

Maybe start with Ilia or Ilia. Do you wanna think for,

## Thoughts on AI and Machine Learning

[01:08:18] **Ilia Baranov:** I think,

[01:08:21] **Audrow Nash:** thoughtful for.

[01:08:24] **Ilia Baranov:** I think there's a lot of usefulness there as if I put it on purpose, eh? No, I think there's a lot of usefulness there for, high variability tasks. Like working in the home again, or, high degrees of freedom manipulators where you can't buy inspection or, algorithmically test every possible outcome.

So image generation, for example, why it's so interesting in, machine learning, or gen generative networks for images in general, is that the image space is so enormous that there's no kind of algorithmic approach that can generate enough data. So you have to have these probabilistic machine learning based approaches to actually get anything reasonable.

there's no good way to do it otherwise. 'cause the, the data content of an image that you're seeing right now is incredible, right? and so for those kind of use cases, especially in Robotics, I think it's very promising because there, we don't have enough compute or algorithms to solve it any other reasonable way today. However, again, in, in our space where it's very much the opposite of a very well-defined kinematic models in con in somewhat controlled spaces, I find the ML approaches are a little bit overkill and they tend to over fit to their space. kinda the answer I give people is, they say, you should use, you should use photorealistic simulation and test all your stuff in sim, which we do use simulation, but we put almost no effort to make it photorealistic

[01:09:57] **Audrow Nash:** You don't need it.

[01:09:58] **Ilia Baranov:** The amount of money, the, yeah. A, we don't need it, but B, the gap between us and somebody like Tesla is several tens of billions of dollars and they have the resources and are at that bleeding edge where every incremental dollar makes a difference. Whereas us, we don't need a billion dollars to make a 90% difference in what we're doing. We only need a fraction of that.

And so it just wouldn't be a wise investment for us at this time in our use cases to put the bulk of our effort at ML.

[01:10:30] **Stefan Seltz-Axmacher:** I also think with the types of vehicles that we're driving, they're supposed to do very discreet things. They're not supposed to do fuzzy things.

They might be like told to do what they're supposed to do in a fuzzy way, right? Like it might be that someone says, Hey, yard truck, can you bring this over to crane 72 right now?

Or they might say, yard truck 14, bring this to crane 72. Like both of those two things should lead to the same discrete action, but the way that we drive that yard truck through that port, the speeds that we drive at the way that we interact at a, a. And if it's not fixed, it's terrifying.

[01:11:12] **Audrow Nash:** Oh yeah. Totally.

[01:11:13] **Stefan Seltz-Axmacher:** You don't wanna wonder like, why is that bulldozer doing that thing it's doing towards me?

Like, it needs to be like, oh, it goes exactly there and if it's going somewhere else, something's really bad.

[01:11:27] **Audrow Nash:** Yeah.

[01:11:28] **Stefan Seltz-Axmacher:** So I think for our application, where I'm really excited about, about the broader, what people are currently calling AI, what I'm really excited about it is for, the UI, is for the interaction between our highly, deterministic systems and like fairly non-deterministic people.

So whether that's voice commands for robots to do things, whether that is using an LLM to scan, an organization's, manual to figure out how their facility operates and to try to turn that into a list of Boolean that we could have a person read through and see if they make

[01:12:06] **Audrow Nash:** starting point. Yeah.

[01:12:08] **Ilia Baranov:** Yeah.

[01:12:08] **Stefan Seltz-Axmacher:** that's that probably like that second thing I just said would probably save 20 hours of stupid meetings that no one wants to be in for implementing a hundred robots in a multi-billion dollar facility. But I don't think, us figuring out a novel path, based on the vibes of the, the transformer model, across, that facility, that's probably not gonna be the right strategy anytime soon.

[01:12:35] **Audrow Nash:** what a thing. Yeah, it's the thing that's really interesting to me with it is a lot of times, so these big companies where they are, they have this huge handbook and it, they tell you how to do something and they want it done in that way. and if you have an LLM, go and make an initial thing, you still have to pay the expert to go and confirm its results for these kinds of things.

It's been, thinking about this more broadly and it's I feel like programmers, I feel like copywriters, all these different things that we all thought were gonna be automated by ChatGPT. I think they're safe for a while because you want that person to validate it. like you, you need that check on it to make sure it's reliable and does what you want.

And then with, programming especially, it's and if you wanna build off of what you've done now you have to give it back to the thing. And if it says it can't do it,

[01:13:35] **Stefan Seltz-Axmacher:** Do it

[01:13:37] **Audrow Nash:** and, but it's still doing the wrong thing. It's just interesting 'cause a programmer could probably figure it out. But an LLM may just get stuck like it is on the problem that I'm trying

[01:13:45] **Stefan Seltz-Axmacher:** though. what's useful for us is, like the guidebooks for a lot of our machines are written, they're written like booleans for idiots.

'cause oftentimes the managers of these facilities don't have the world's highest level of respect for the vehicle operators. like I've read a manual for a, particular facility. Where, there's vehicles that lift up 30,000 pounds and then drive around with 30,000 pounds and then move it. and there's a list of maybe like 50 rules of operation for when you're driving these vehicles. And one of them was like, if you have lifted a load and you're in reverse and you see someone standing within a hundred meters behind you, turn off the engine, get on the radio, ask for help. If you're driving from here to there and this gate is open, turn off the engine, get on the radio call for help. and there are rules written like that like an LLM could make quick work of. and that we could deploy into a use case really easily. But there's also the, rules that you'd only learn by sitting down with all of the management staff of the site for three weeks in, in 14 different meetings that are each scheduled for an hour and a half, but none of them go less than two and a half hours.

Where in the 15th meeting someone happens to say, oh, yeah, you can't drive in that corner 'cause that's the corner where this thing drains and all these people died once. So you gotta go around that. And

[01:15:11] **Audrow Nash:** these

[01:15:12] **Stefan Seltz-Axmacher:** that's written down somewhere, the LLM won, I won't learn it.

[01:15:15] **Audrow Nash:** Yeah, that context. Yeah, it's interesting 'cause there's a lot that's implicit I think in how people do things. And it may not be in a manual, just has to be learned for this kind of thing. Interesting. Any, so Has it changed? Oh, go ahead, ia.

[01:15:31] **Stefan Seltz-Axmacher:** go ahead.

[01:15:33] **Ilia Baranov:** yeah, there's, a bigger meta point here on machine learning in general and Robotics and our particular view on it.

I was, careful earlier to say that machine learning is this kind of sugar res sprinkle on top to, to really solve these corner use cases because in a lot of our vehicles, we actually want to safety rate our system.

## Making safety certified systems

[01:15:52] **Audrow Nash:** Oh,

[01:15:52] **Ilia Baranov:** And again, safety rating is something where if you want to do an actual formal certification, it's not impossible with machine learning, but the bar is so much higher right than, very deterministic systems, which we can prove out a hundred percent exactly what it will do in every scenario. and so the lower down the stack you get towards the underlying safety layer, the more and more rigid we become and the more and more kind of rules driven we become so that machine learning side at the top can like maybe differentiate shape between a tree and a boulder, but it's never gonna command the vehicles directly.

[01:16:27] **Audrow Nash:** Yeah. it has to

[01:16:29] **Ilia Baranov:** because we need to deploy these things in real world.

[01:16:31] **Audrow Nash:** Wow. I love that. I, can't believe I didn't think about talking about all of the, safety certification stuff, but that makes a lot of sense, which is you guys can, because so these companies, they come and they try to build their own and they spend, you said like $50 million or some bonkers amount of money trying to build their autonomy stack, whereas you guys are making a business out of it.

And then what you can do is you can invest as you need or a you can invest so that you actually safety certify things so they can just drop in a safety certified system. That's really amazing.

[01:17:10] **Stefan Seltz-Axmacher:** Yep.

[01:17:11] **Audrow Nash:** that's probably a huge competitive advantage and probably a very good moat, I would imagine for you guys as a

[01:17:17] **Stefan Seltz-Axmacher:** Yep.

[01:17:18] **Ilia Baranov:** Yep.

[01:17:18] **Stefan Seltz-Axmacher:** Safety's really hard and like safety's really hard. It's also hard to build a culture where people are smart about safety, where people are, thinking about safety the right way. And essentially because we use the same safety core on all of our machines, we are basically constantly getting learnings.

We're constantly getting hours of testing to prove that the system actually works.

[01:17:40] **Audrow Nash:** Yeah. So part of it is putting the case together and because you have deployed on systems and your systems have monitoring, and then you can log, so that you can prove that this has happened for some amount of time. So you can make these claims.

That's nice. And so you can solve, Val, you can solve cases where they don't require the certification, but you can use those to bootstrap justification for additional safety certifications.

That's clever. Hell yeah.

[01:18:10] **Stefan Seltz-Axmacher:** yeah.

[01:18:12] **Ilia Baranov:** Yeah.

And that's from a business side, that's also a big

competitive moat for us,

[01:18:16] **Audrow Nash:** that's what I was

[01:18:17] **Ilia Baranov:** over time, because we really, yeah, we really try to, again, keep that autonomy core the same and the same for the safety subsystem. So we'll build up hours of operation that are directly applicable across units faster because we deploy it across a much more varied fleet. And of course, as a roboticist, you can imagine the more varied use cases you have, The much better. quality actual proof you have of safety. It's not just the same test a hundred times, it's a hundred different tests.

[01:18:45] **Audrow Nash:** That's super cool. Okay. What a thing. I really like that. Do you have, safety certifications yet? Or which ones do you have and what are you working towards?

[01:18:58] **Ilia Baranov:** Yeah, we're working. So there's two different threads we're working towards. One is internally we wanna certify to UL 4600, which is a fairly new standard.

[01:19:07] **Audrow Nash:** Yeah, I'm not familiar with

[01:19:08] **Ilia Baranov:** in particular we're targeting that one. Yeah. So,

[01:19:10] **Stefan Seltz-Axmacher:** so

[01:19:11] **Ilia Baranov:** past the, the,

ISO 26262

[01:19:15] **Audrow Nash:** Oh, okay. I know that one. Okay.

[01:19:16] **Stefan Seltz-Axmacher:** yep.

[01:19:17] **Ilia Baranov:** So what's nice about it is ISO 26262, if you go through the certification at some point it assumes human takeover, whereas UL 4600 does not.

And that's that's one but kind of key difference. And UL 4600 is more a, umbrella standard of how to design a safe autonomous system without being prescriptive on, like specifically follow this pattern. But it itself suggests things like IEC 61508 for sub electrical systems and those kind of things, which build up proof to get to a UL 4600 certification standard. So again, it allows us to be more flexible and, if we want to go that direction, I can talk about how I'm really excited to turn safety certification into another CICD code problem.

[01:20:03] **Audrow Nash:** I am, I would love to talk about that. No, I would love that. That sounds wonderful.

[01:20:07] **Ilia Baranov:** Okay.

[01:20:08] **Audrow Nash:** I love safety certification stuff. I, host spaces on X. I actually have one tonight. and you guys are welcome to come anytime, but they're like an hour and a half every week or something like this. We had one, before Christmas sometime, and it was an hour and a half of talking about safety certifications and after it's like I found my people, this is just wonderful, Okay. Tell me it's, I would love to hear how you're thinking of it. Like a continuous integration system, testing this kind of thing.

[01:20:41] **Ilia Baranov:** yeah. Yeah. So, having gone through this kind of process before. A lot of it is a very manual, like engineer sits down, writes a whole bunch of failure modes, get that reviewed, then they get testing, they get, that reviewed. And then maybe a small piece of it is, there's some requirement on code test coverage and maybe that piece is part of the CICD, but I want to actually wrap the entire everything I've described as part of a CICD so that every build we, we run for our, specifically our safety system.

So we try to keep the scope very small and very simple.

[01:21:14] **Audrow Nash:** Of course.

[01:21:15] **Ilia Baranov:** Not only does unit testing, but also auto generates a lot of the okay to be in compliance with this part of U

[01:21:22] **Audrow Nash:** Oh, I love it.

[01:21:22] **Ilia Baranov:** have this certification that refers to this thing, here's in this particular vehicle, which is configured this way. So when we do a build for this vehicle, it has these characteristics which we can pull in as their own proof for their use cases.

So this vehicle goes at this speed, hence we need this speed of look ahead, here's our proof of that, look ahead, here's our proof of the data and to auto generate as much of that as we possibly can so that the end requirement, of course you still need a human review,

But a lot of that is auto built.

[01:21:53] **Audrow Nash:** Yeah. That's

[01:21:55] **Ilia Baranov:** rather than hand calculating all of it.

[01:21:57] **Audrow Nash:** is laborious for sure. That's awesome. I, so it would be like, effectively, it'd be like you have requirements. So you, could take a standard, you could parse it and turn it into a bunch of requirements. The requirements might have parameters, and then you could use these to define specific tests that then you run that are part of your continuous integration and testing.

is that, oh, that sounds so cool.

[01:22:22] **Ilia Baranov:** UL 4600 and yeah. and UL 4600 is particular, is written as this like giant spanning tree of a bunch of things. to be compliant with this, you have to be compliant with this, and then you go to those. to be compliant with that, you have to be compliant with this, So it's basically a big tree traversal problem of, to hit this, here's my, all my branches and here's proofs for everyone that then build on top of each other to get that

[01:22:45] **Audrow Nash:** Oh, that's so

[01:22:46] **Ilia Baranov:** That's What I

[01:22:47] **Audrow Nash:** a moat that will

[01:22:48] **Ilia Baranov:** that's what we're building.

[01:22:51] **Audrow Nash:** Ah-Huh?

[01:22:51] **Ilia Baranov:** actually I do want to open source as much

[01:22:54] **Audrow Nash:** I want that to be open sourced. Yeah.

[01:22:58] **Ilia Baranov:** At least, the learnings from it and the pitfalls we find and those kind of things. I do want to build that out because I think for too long safety has been this like pay us X millions of dollars and we're a safety certification organization. We'll give you the check mark, like here's the golden check mark. I wanna actually build the infrastructure to let other groups do that themselves. And of course provide that service, we will as well. But I just as basic autonomy, you should be able to build this yourself. But if you want a shortcut, you work with us because we know how to do it. We have the proof points.

[01:23:28] **Audrow Nash:** Yeah, actually that could be a, that could even be like a side business or a side thing within your business where it's like you basically have all this infrastructure to facilitate. UL 4600, 4,600, you, you could help Robotics companies certify their, sophomore easily. 'cause it's a pain that people have to go and learn all of these safety certifications and all the details of it.

And if it was like, here, hook up to your robot to our, like some, sort of interface. and we're gonna see if it passes in our environment, this kind of thing. That would be just amazing. That would be so cool. That would, accelerate all of Robotics I would think. Like all different

[01:24:16] **Ilia Baranov:** yeah, and I think an additional detail is that while that's the umbrella standard we've picked, the reason we picked it is it because a high, it has a high enough barrier of proof and demonstration, that kind of stuff that I, I believe at least,

and we're working through the proof exactly.

We, the same techniques we've used on U 4 8600, we can then deploy to whatever people need because mining standards in South Africa. Are different than Australia, are different than the US. Instead of killing ourselves, trying to comply with everyone, we'll generate the products and then go to specialists on site and say, for your mine, you know how to certify.

Here's all the data we have. What are we missing? What do you need That isn't part of this stack.

[01:25:02] **Audrow Nash:** will be really cool. Yeah, I really like that a lot. I think, yeah, making certifications. it's interesting because if we made them very algorithmic in a way, and you can parse them so they're in PDFs or whatever and you can parse them to make them, like a, tree of things that you have to go check and then you have some document that shows all the requirements that would just be so valuable.

I had to, so I was the ROS boss for Humble for ROS 2 and built a tool that helped us with requirements. and so I did a pretty good investigation on the like requirements, tools, space to try to see okay, you have these requirements, they lead to these test cases and whatever, and how do you do it?

And they were all Horrible.

So we ended up building our own

[01:25:51] **Ilia Baranov:** all awful And super expensive.

and like ludicrously expensive.

[01:25:57] **Audrow Nash:** many of them had like free trials or something, so I would try them and they're just terrible. Like awful, Everything. Awful and expensive. but I think if you could make that good, that would be fantastic.

I. that would be a big value to the whole Robotics community. I would expect. I would love, and if you open source that please let me know. I would love to see it too. Hell yeah.

[01:26:20] **Ilia Baranov:** Yeah. Yeah, no, for sure. you know what? After this send me that requirements. If you have any notes on that, I'd love to see if we can integrate that. That'd be really cool.

[01:26:28] **Audrow Nash:** Oh hell yeah. Okay.

[01:26:29] **Ilia Baranov:** If there's anything public about it, throw it my way. I'll take a look.

[01:26:34] **Audrow Nash:** the tool I ended up making was a bit simpler and it was basically for, it's all open source and it has aged a bit 'cause I haven't had maintenance time for it, but we are still using it for every ROS 2 and Gazebo release. but yeah, I, can send it to you. It's called yet another test case manager was the dumb name that I gave it.

But,

[01:26:56] **Ilia Baranov:** I love it.

[01:26:58] **Audrow Nash:** it was fun to build. And then, so we're coming to the end, but I would love to, we didn't talk about it at all about your podcast, so I'd love to talk a bit about that. yeah. go ahead.

## Live demo!

[01:27:12] **Ilia Baranov:** before we jump into that, can I do, one quick diversion?

[01:27:17] **Stefan Seltz-Axmacher:** Is there, a chat feature in this? Can we send, you Audrow a link?

[01:27:20] **Audrow Nash:** Yeah. it's in the bottom right

[01:27:23] **Stefan Seltz-Axmacher:** Cool.

[01:27:23] **Ilia Baranov:** All right. So for our listeners, you'll have less fun than, we do currently. but I, just to describe it, I sent Audrow a link to our live test tractor in Modesto, California, and I'm gonna share my screen so you can see a video feed from it. now what Audrow's gonna do

see a

[01:27:44] **Stefan Seltz-Axmacher:** let, lemme let me, lemme, let me walk you through a little bit of what's going on. So, live streaming here on the screen is a first person view from our test tractor in Modesto, California. There's no one in this tractor, no one on site. The closest member of our team is about a hundred miles away.

The last time anyone in our team was physically near this tractor was probably Ilia and I back in September. Audrow, did that, link work for you? Do you have it

[01:28:12] **Audrow Nash:** I have a, it's like a Google Maps or something, and I click the location, so it looks like

it's

[01:28:18] **Stefan Seltz-Axmacher:** Oh,

[01:28:18] **Ilia Baranov:** you, you, clicked a location. Yep. There you go. So

[01:28:22] **Stefan Seltz-Axmacher:** you just,

[01:28:23] **Ilia Baranov:** our robot.

[01:28:25] **Stefan Seltz-Axmacher:** so the app that, re

[01:28:28] **Audrow Nash:** Oh, so

[01:28:29] **Stefan Seltz-Axmacher:** was. Was written by a buddy of mine who is a self-described 50th percentile engineer. he's just a front end engineer at a big boring SaaS company. He knows nothing about controls, he knows nothing about safety engineering. He knows nothing about machine learning, mechatronics any of that. He basically, in 20 hours he took map box's, API to pull in satellite data of the field and took in our API to be able to see location of where the tractor is and issue, commands to the tractor.

And from that, Audrow seems to have now sent us on yet another, point

that the tractor's driving itself to.

[01:29:10] **Audrow Nash:** That's super cool. I love that.

[01:29:13] **Ilia Baranov:** it's doing a three point turn and then it's 'cause it will, so for listeners, Aras clicking in a little yellow geofence and we're seeing a live feed of the vehicle drive around. What the vehicle will always try to do is, end up oriented from where it started to where it is. So usually that'll involve a three point turn.

So right now it's facing north. If Audrow clicks somewhere south, we're gonna turn around and then end up facing south.

and this kind of easy to use interface. There you go. and this kind of easy to use interface where you just click it and tell it where to go is just one example app.

But the underlying rest API is what we actually use to control our vehicles.

And this tractor could easily be a mining vehicle or a forestry vehicle and it would behave completely differently. But Audrow's clicking would be identical.

[01:30:01] **Stefan Seltz-Axmacher:** Just the other week we were co-hosting a happy hour at CES and we were using the same app, at 9:00 PM Pacific time to issue commands to, an AGV that our autonomy's on in Australia, made by a partner of ours, BIA5.

So like the reason for this and like the whole thought process here, if you wanna automate a tractor, the special thing about automating a tractor is not the hardware that goes onto the tractor.

It's not like the point-to-point navigation. It's like figuring out like the five screens and four buttons per screen that Farmer John needs to see and, interact with to make something valuable for Farmer John happen.

And I don't know what Farmer John needs, 'cause I don't know if Farmer John is in Ohio and grows wheat, or if it's really Father Juan in Spain growing whatever they grow in Spain. either farmer probably needs a different ui. They probably need different behaviors to happen. We let our customers build that. We just solved the point to point nav part.

[01:31:05] **Audrow Nash:** Huh. That's super cool. Did not know we were gonna get a live demo. I love that.

[01:31:11] **Stefan Seltz-Axmacher:** Yeah, we, did that demo I think a thousand times last year is a real number.

[01:31:15] **Ilia Baranov:** Literally something. Yeah.

[01:31:18] **Stefan Seltz-Axmacher:** like if you listener are on a call with me and it's during business hours, You'll almost certainly end up getting

[01:31:25] **Audrow Nash:** ha.

[01:31:26] **Stefan Seltz-Axmacher:** and that's part of our secret evil plan to prove that our robots just work is by like doing constant demos. of this is not a big deal.

This's not a big production. We're not even treating you all that special right now, Audrow, we're just doing the thing we do every time.

[01:31:40] **Audrow Nash:** That's great. It's great to not be treated special with the get the good demo.

[01:31:46] **Stefan Seltz-Axmacher:** I know how you make,

I know how to make you feel.

[01:31:50] **Audrow Nash:** Yeah. Okay. Do you think

So it's very interesting to me. The web connects all of us. it's just like all our devices are running web stuff, everything is making requests. I, feel like in the robotics community we've looked on rest APIs, which I don't know, they have their git and put and post and whatever their requests. and we've looked at them and gone, that will never work for robotics. And you guys are making these nice demos and you have these simple rest API endpoints for querying. Tell me a bit about that. is it the future of how we're going to interact with robots as you think like a high level rest, API will manage things and you'll handle all the complexity on the robot side, but keep it simple for the user.

Is that kind of how it will be? Or tell me about rest APIs and why them?

## Web tools and robotics

[01:32:46] **Ilia Baranov:** I think, yeah, I think we, when we were just getting started, we wanted something that every web developer and every language out there has a easy to use getting started guide on. So I think like Python or C or Rust or HTTP, Ruby, whatever.

[01:33:02] **Audrow Nash:** Whatever it is. Yeah.

[01:33:03] **Ilia Baranov:** And REST was this very simple to understand that you could even run from a command line if you wanted to or run from a browser.

Exactly. You can curl it. and it is a polled interface in a lot of ways. So if, for example, we wanted to webstream, you notice the video I showed was using forint as an actual web backend. We're big fans of formint we use them

for, this sort of stuff. REST is not the path. Yeah. So REST is not the path for streaming large amounts of

[01:33:32] **Audrow Nash:** No,

[01:33:33] **Ilia Baranov:** it at all. but Right, but the right tool for the right process.

If, you have a large fleet of vehicles, let's say a hundred, and you just need to be able to tell them, vehicle A, go to this position, vehicle B go to this position, it's actually scales relatively well for that purpose. without having to set up unique connections for each one without having to manage web RTC stuff.

It's just spiel out a bunch of commands from anywhere you are in the world and they'll get to your robots.

because it's built on standard web technology, you get a lot of that security, you get a lot of that multi-threading, multi-user agent stuff is all well figured out.

So we don't have to reinvent any of that stuff either

[01:34:11] **Stefan Seltz-Axmacher:** And, it can work both for this fun demo, which is a neat thing to do from a distance, but it can also work if everything is on the same site and there is no external internet connection. The same API can work for the vehicle in that use case.

[01:34:24] **Audrow Nash:** Oh, that's a big

[01:34:26] **Ilia Baranov:** the API's hosted locally, so the API's on the vehicle.

And so the API could even be self triggered. So something we don't have ready yet, but I mentioned that behavior tree. the long-term goal here is to be able to give our customers the ability to generate little SubT trees and inject them back onto the robot for itself. concrete example, if they're building their apple picking robot,

they focus on their arm to pick the apple and then they onboard trigger an API function, move to the

[01:34:52] **Stefan Seltz-Axmacher:** forward a foot.

[01:34:53] **Ilia Baranov:** which they've, or, move to the next tree, which they've defined as move until you see a barrier under these conditions, whatever. Like a little subtree of logic.

[01:35:03] **Audrow Nash:** I like that. Yeah, so it can self trigger. So you, can basically have a system make its own calls from another call so it can cascade in this kind of thing. That seems powerful to me. very interesting. Seems a lot more complex, but seems like you could do some cool things or maybe you can get, behavior that's more responsive with that kind of thing.

'cause it can trigger something right then I bet. Is that the big benefit that you get with it? Ah, cool.

[01:35:37] **Ilia Baranov:** it's, local interactivity is definitely one of them. So, again, and this isn't fully ready yet, so our current API, we can publish the API specs. They're online, but they don't, they won't mention this subtree behavior yet.

But, one of our early clients, they just wanted a button that you could press. To press a button and the robot does

x And we thought, oh, we could write a custom ROS interface. We could do all these things to, to get it to behave. But then we thought we're already running an API, let's just loop back the API call to itself.

And that they just have their little button do a little programmatic, REST API call.

Which sounds funny, but it actually ended up being the most flexible approach.

[01:36:16] **Audrow Nash:** Yeah, I would imagine it would be the most flexible approach. That seems great. and you, do you think that, do you think this is gonna be a larger trend in Robotics? I know like a lot of companies, they end up wanting to put things into some sort of interface you can view from the web. and I guess this often means putting, making endpoints for something.

and sometimes they'll use web sockets and things for streaming video or whatever it might be. but do, you think that we're gonna see a larger trend of robots doing more, being, interacted with through a REST API or something like this? is that something that you think will catch on?

[01:37:03] **Ilia Baranov:** I, think, if I could jump in,

sorry, Stefan, but, not necessarily REST in particular, but I think

[01:37:10] **Audrow Nash:** Just web standards.

[01:37:11] **Ilia Baranov:** in general has. like web, different web websites, whatever it is. If there's a new thing next, next month, ROS special communication protocol, like happy to write an interface layer to it.

'cause we don't care ultimately, right? Like none of our actual safety or behavior happens up there. It's just a translator. and I think we are moving in the direction where there's more connectivity for lower cost on more devices.

there's a lot of this edge computing that's taken hold, a lot of cloud computing. so I think covering our eyes and pretending that doesn't happen in Robotics isn't the right way forwards.

I think we have to accept that.

[01:37:45] **Audrow Nash:** Definitely. And we might as well leverage everything that exists too.

[01:37:49] **Stefan Seltz-Axmacher:** Yeah.

[01:37:50] **Audrow Nash:** there's just so much there where huge sums of money have been invested into improving these systems. and we might as well not reinvent that. So the web is great for a lot of things like that, is my opinion on it.

Hell yeah. What a cool thing. Thank you for sharing that.

[01:38:08] **Stefan Seltz-Axmacher:** Absolutely.

[01:38:09] **Audrow Nash:** Yeah. I heard the podcast episode that I listened to, that Nic shared, is, or you guys talked about the demoing, like instead of the kind of your culture where it's just demo constantly. Therefore it's not like you do a big demo once in a while and it breaks and this kind of thing.

And it, I, did not know that I would be, seeing a demo now. So

[01:38:36] **Stefan Seltz-Axmacher:** I didn't know that was

[01:38:36] **Audrow Nash:** see. You're still

[01:38:37] **Stefan Seltz-Axmacher:** you listened to, so that worked out.

[01:38:39] **Audrow Nash:** Hell yeah.

[01:38:41] **Ilia Baranov:** CICD stands for continuous demo by

[01:38:44] **Audrow Nash:** Ah ha.

[01:38:44] **Ilia Baranov:** just to be

[01:38:45] **Audrow Nash:** Oh yeah. Yeah. Instead of deployment. I love it. Continuous demo. For you guys it might be demos. Yeah. So what do you,

tell me about the podcast. I, like at a, high level, what is the Automate It podcast and how, what are you guys trying to achieve with it? Or, I don't know, what do you, what kind of questions do you guys investigate?

Maybe Stefan

## Automate It podcast

[01:39:11] **Stefan Seltz-Axmacher:** co of course. Yeah. So every one to 12 weeks. we release a podcast on our podcast called Automate It. and, basically automate it is the podcast version of the fun Robotics conversations you have with your friends at the end of the long day.

[01:39:31] **Audrow Nash:** does seem

[01:39:31] **Stefan Seltz-Axmacher:** two sections of it, where the first is we each draw a random card to represent a technology and represent a business case, and then we have to spitball into an existence, a robot that uses that technology in that business case.

And we try to make them be stupid, sometimes ends up making them be good. Often make them stupid, but representative of a real company, which is troubling every time. and then the second half, we'll talk about different challenges in Robotics, like why indoor localization is hard, or why demoing often is good, or any number of these kind of normal things that happen when you're working on robots.

[01:40:12] **Audrow Nash:** Let's see. Ilia, anything to add?

[01:40:18] **Ilia Baranov:** yeah, I would just add that generally we do this talk after a beer or two, so it tends to be a little bit it off the rails at the start. I think my favorite was we invented a bartending robot that was a bunch of arms on electrified rails that would fly around the bar to pour drinks or bring them to people.

And, yeah, very economically viable. It's

[01:40:41] **Stefan Seltz-Axmacher:** Yeah, it'd be, a great business. but in terms of why we started it, so weird thing about our company is

there's, I'm sure there's more personalities in this, but maybe there's three archetypes of types of people starting Robotics projects. There's like the optimistic producty business guy who thinks robots just work and let's figure out this, let's build a robot around this idea that I

[01:41:05] **Audrow Nash:** it's an opportunity basically.

[01:41:07] **Stefan Seltz-Axmacher:** Yeah, this is a great opportunity. there's the like young, dumb and incredibly confident, roboticist who maybe they just got out of CMU, maybe they just left some big Robotics lab and like that Robotics lab, they did everything slightly wrong. And as an individual roboticist, I one time made a project that looked neat for a minute.

So I'm gonna rebuild everything in robotics myself to solve every single problem and it's gonna go great.

[01:41:39] **Audrow Nash:** I've been

[01:41:39] **Stefan Seltz-Axmacher:** kind of third archetype who either of those first two become after robots are jerks for a while. like the type of roboticist you are when you once had dreams of, solving general problems.

And now you're just hoping God, I hope it turns on tomorrow and can do something and that people, let me keep on working on this for Christ's sake. Why won't it turn on?

and that third group is they tend to be our best customer base. because the people who think that robot Robotics is solved, the people who think that they alone can solve it, they're not gonna let us solve auto point to point autonomy for them.

'cause that will take them like a weekend probably. it's really the people who have been beaten up by robots, chewed up, spat out, who really wanna make a robot work this time and, create real value. That's, who we sell the best to. So as a result, we made a podcast to help people get to that stage of, their robotics journey

[01:42:41] **Audrow Nash:** Oh, that's really cool. Yeah. So basically you're discussing all the things and you're letting people in on the process, and the idea is it helps people become educated in Robotics sooner about how to make things and that they can't do

[01:42:58] **Ilia Baranov:** see the back

to see the backstage pain and suffering. we were talking at CSS just recently and we were joking that we should have named it actually Robotics Anonymous as as a, as like a just a support group for here's all the pain we've, faced.

[01:43:14] **Audrow Nash:** Yeah. Yeah. In the demo one you guys talked about some of your past experiences and they seemed super painful, with spinning parts that were hot and it was super cold out and it was just crazy. yeah, I feel the, thing that is interesting to me is I was definitely stage two or whatever of what you were doing while I was in grad school.

like I, I tried to build ROS at some point, and then by the time I

[01:43:41] **Stefan Seltz-Axmacher:** you are gonna do it the right way.

[01:43:43] **Audrow Nash:** Yeah, I know, but, and then I got to ar I needed something like Rviz and something like ROS2bag and it was like, I guess I'll just use it and this kind of thing. But now, it's been interesting 'cause I've been mostly on the software side. and so I'm trying to do some Robotics side projects occasionally and buy a bunch of stuff from Sparkfun and hook it up to ROS 2 and things like this. And it's a lot of work. and the thing that is really becoming clear to me is to do a good job at robotics and to like actually build value.

You need a lot of people. Which is interesting 'cause there's so many things to do, where you need the CEO who goes and figures out the market and knows, and you need a domain expert and you need the technical guy and you need all the manufacturing knowledge and there's a million things.

[01:44:38] **Stefan Seltz-Axmacher:** Yeah. And like I think I would argue that like for robotics to be the space, we all want it to be you. You need to build a product, you need to build a \company, you build an organization where you only need to be good at one part of it.

[01:44:53] **Audrow Nash:** Definitely.

[01:44:54] **Stefan Seltz-Axmacher:** maybe you're doing.

the hardware, maybe you're doing the retrofit. Maybe you are getting really smart about what farmers in Ohio need as a ui, ux, and, as Robotics behaviors, and you're using somebody like us to do the driving and someone else to retrofit the vehicles

and If, you're willing to do just that, it's still gonna turn out to be incredibly hard.

'cause it turns out like as much as like we all might make fun of DocuSign 5.0, it's hard to build DocuSign 5.0 or how to not for cats like those are hard businesses to build in their own right. And like by focusing just on the specific part of the value that you have unique insight to, we can all go make robots

[01:45:38] **Audrow Nash:** I like that a lot. Ilia, anything to add?

[01:45:43] **Ilia Baranov:** I, I would say, from the content creator perspective, so Nicole, our kind of marketing guru suggested this to Stefan and I, and to start a podcast. And at first kind of both Stefan

[01:45:57] **Stefan Seltz-Axmacher:** Hard

[01:45:58] **Ilia Baranov:** eh, a little leery, eh, I got enough.

[01:46:02] **Audrow Nash:** You are doing a lot.

[01:46:04] **Stefan Seltz-Axmacher:** Who talks on

[01:46:04] **Ilia Baranov:** at them this week at some point.

Yeah. but but realistically, it ended up being A super fun for us. And I think that kind of unstructured part helps get us in the mood and, talk about random, crazy Robotics anonymous topics. and secondly, I think it ended up being hilariously effective as a marketing and re outreach tool.

[01:46:28] **Audrow Nash:** Oh

[01:46:29] **Ilia Baranov:** it's, not a, we don't have a thousand, we don't even have a thousand listeners. we don't have a lot, it's, a very small listener

[01:46:35] **Stefan Seltz-Axmacher:** It's a niche podcast.

[01:46:36] **Ilia Baranov:** is, yeah. it's very niche, right? But the funny thing is, any conference we'll go to, invariably, at least one, if not multiple people will come up and be like, oh yeah, you, I've listened to your podcast.

[01:46:48] **Stefan Seltz-Axmacher:** And they'll have,

[01:46:48] **Ilia Baranov:** the people we wanna work with. yep,

[01:46:52] **Stefan Seltz-Axmacher:** yep. And they'll be specifically yeah, maybe you can help us. What we're doing is really hard. It seems like it's been hard for you before too, and maybe you can do some things better than we can. Yeah, we'd love to, we'd love to, commiserate with you on robots and help automate it.

[01:47:06] **Audrow Nash:** Yes. Oh, that's so funny. Yeah, I I have that too, where it's a small fan base, but they are awesome.

[01:47:16] **Stefan Seltz-Axmacher:** Yep.

[01:47:17] **Audrow Nash:** I get recognized just a handful of times at every conference. They're like, oh, I love the pod, whatever. Or you should talk to this person. It's just, I don't know. It's such a cool, wonderful thing.

I feel like talking to a small audience that really likes the content that you make is really wonderful. there's something just glorious in it, like very, enjoyable.

[01:47:39] **Stefan Seltz-Axmacher:** I think it goes back to a basic like Paul Graham of make a hundred people love, or make 10 people love you, as opposed to a thousand people like you.

[01:47:47] **Audrow Nash:** ah, yeah. It's a good way to look at it, Paul.

Yeah.

[01:47:52] **Stefan Seltz-Axmacher:** Yeah.

[01:47:53] **Audrow Nash:** Hell yeah. that's super cool. I love the reason for doing the podcast. and it's funny that it can bring you people to commiserate with and help educate to move people towards this. robots can be really cool and they can solve a lot of things, but they're really hard and I dunno.

Okay. So you gotta approach it that way, like they're super

[01:48:18] **Stefan Seltz-Axmacher:** Yep.

[01:48:21] **Audrow Nash:** Let's see. where do people find your podcast? Is it on all of the different

[01:48:27] **Stefan Seltz-Axmacher:** so we're on all the major, outlets, Spotify, Apple Podcasts, whatever, just call to automate it. And there's a nice cartoonish image, of Ilia and I both donning facial hair and looking incredibly, dapper

[01:48:41] **Audrow Nash:** Nice. Yeah, I think what, it's funny 'cause I've listened to a couple of your episodes and they're, the beginning is very much complimenting each other's hair,

[01:48:50] **Stefan Seltz-Axmacher:** hair.

[01:48:50] **Audrow Nash:** this kind of thing. And it's oh, your

[01:48:53] **Stefan Seltz-Axmacher:** for anyone

[01:48:54] **Audrow Nash:** today. A little goofy.

[01:48:56] **Stefan Seltz-Axmacher:** for anyone, anyone viewing this, that just makes obvious sense. And for the people who are just listening, imagine the most incredibly good looking people ever. And that's exactly what we look like, especially in the hair department.

Just yeah,

[01:49:11] **Audrow Nash:** And then do not go onto the YouTube. And

[01:49:14] **Ilia Baranov:** Stefan starts the episodes critiquing. My, Stefan

usually starts by critiquing whatever I'm wearing that day,

[01:49:24] **Audrow Nash:** really,

[01:49:25] **Ilia Baranov:** always a good start to our podcast episode.

It's ah, same shirt. I see. Huh.

[01:49:31] **Audrow Nash:** I wear a black shirt in every episode, but

[01:49:34] **Stefan Seltz-Axmacher:** This sounds a lot like my wife who tells me I look the best with a mask on.

[01:49:40] **Audrow Nash:** how funny. Not gonna touch that one.

Let's see, we're, coming to the end of the time. I can talk a little bit more. I don't know if you guys have a hard cutoff or anything. but we're at the end of, okay. Okay.

I, wanted to see what you guys have for advice for people, wanting to get into Robotics. say, it's someone who's in their, the middle of their university or something, what should they know or what would save them time?

maybe start with Stefan.

## Advice for getting involved in robotics

[01:50:20] **Stefan Seltz-Axmacher:** yeah, so I'll, maybe I'll answer this more. For people who are interested in Robotics products and Ilia can talk about it more from an engineering perspective.

[01:50:27] **Audrow Nash:** it.

[01:50:28] **Stefan Seltz-Axmacher:** I think the, when you're, when you have not built a robot yourself and you're looking in a very common, intellectual fallacy, or flaw that you fall into is that you see things that have been built before and you assume that's no big deal. And I, I'll just, I'll grab an arm from a Toyota factory, I'll grab a Waymo car and then I'll have a car that can drive around and put mail in mailboxes and it's gonna be great. the, weirdest and, shittiest and hardest thing about Robotics from a, product and a business and investing perspective is that unlike the world of SaaS apps where any feature is purchasable as a microservice in Robotics, basically every feature that you see, every supporting piece of tooling, every supporting piece of infrastructure, almost everything that you see has to be reinvented from scratch. with the exception of some of the stuff in ROS that is in general, mostly a lot harder to set up than any piece of tooling that you would get for starting an e-commerce site.

So like a good Robotics business, a good Robotics product is a matter of what is a thing that is super expensive for humans to do.

Like just there's an incredible labor shortage around it and is drop dead simple for a robot to do. 'cause it needs the same thing to be done over and over again. And start with that. And don't just start by combining robots you've seen on, in TechCrunch.

[01:52:05] **Audrow Nash:** love it. yeah. Ilia, what do you think?

[01:52:12] **Ilia Baranov:** So on, on my end, my thoughts are summarized. So I, really love XKCD I'm sure a lot of people listening

have heard of that web

[01:52:19] **Audrow Nash:** Yeah, they're great. I.

[01:52:21] **Ilia Baranov:** there's a particular one that's There's one that's oh, we built this robot that like shoots lightning and is also an air balloon and whatever.

And somebody ask what is that for? And it's search and rescue. that's like the default answer for robot projects. It's oh, search and rescue. so I think the trap that engineers fall into is solutionism or robots for robot's sake. And I love to do that for my own life.

Like I build lots of fun trinkets just for fun for myself, but that is not a business. And so as an engineer, really try to step back and to give it the question of, is this the most effective way I can solve this problem? Is robots really the answer here? If not, you're gonna bang your head against that problem, regardless of how good your tech is.

You're just not gonna solve it. I'll give a really quick concrete example. there's a mining project, which they're interested in building autonomy and stuff like that, but, in the short term, they're saying their, immediate term goal is just to reduce the amount of idling that their fleet does, because across their fleet, when their drivers just idle the engine, they waste like multiple millions of dollars a year

[01:53:30] **Stefan Seltz-Axmacher:** $8 million a year of diesel

wasted because the operators won't, turn the engine off. because if the engine's turned off, it looks like they're not working.

[01:53:41] **Audrow Nash:** huh?

[01:53:42] **Ilia Baranov:** Or, 'cause they want to keep the AC on, right?

And, as an engineer, my, my thing is oh, we can automate their vehicles and we can do all this thing, we can put in all these monitoring systems. And then the answer is or you could just have a 10 cent circuit that if you're idling from longer than X automatically turns off your engine.

And like that 50 cents or that $2 solution is worth $8 million. Not particularly interesting. It's a it's a 555 timer and a switch, but worth $8 million off the bat. so really when you're, being an engineer, really try to think do you actually need robots here? And if the answer's no and you want to be a roboticist look for a different idea, you're, not gonna tech your way through this problem,

[01:54:24] **Stefan Seltz-Axmacher:** Yeah,

[01:54:26] **Audrow Nash:** oh, go ahead, Stefan.

## Stefan's former startup experience and path to Polymath

[01:54:27] **Stefan Seltz-Axmacher:** I was gonna say, so an interesting thing, when I was working at my self-driving trucking company,

the point where being better at writing software to manage a trucking fleet would make us more profit than solving general autonomy. like we were autonomous, like 90, 95% of the time when we're on highways teleoperated for the last 5%. And like being more clever about how we route trucks being more clever about like automatically telling more brokers that trucks are available for a load. That type of stuff would add more cents per mile of profit than $10 billion AGI solution type of thing. and that realization made my board member think, or, maybe I should scratch that, made senior financial people connected to us.

Think, why do you guys just let go of the Robotics team? Just focus on being a software, focused trucking company.

And like when robot trucks get solved, you buy whoever makes the best ones. Which I think is gonna happen to a lot of the vertical folks where it's gonna become like, oh. running a, day-to-day business in this, heavy industry. These companies suck a lot Just by bringing in like standard Silicon Valley practices of how to manage resources would make you more efficient than most of the world's biggest industrial players.

Yeah.

[01:55:55] **Audrow Nash:** That's bonkers. What a thing. That was probably a hard time, I would imagine, with that

[01:56:02] **Stefan Seltz-Axmacher:** Yeah. Yeah. Yeah. That was a like, huh, I can't tell a lot of people on the team about this, or morale would drop pretty sadly.

[01:56:10] **Audrow Nash:** Yeah. What a thing. How long, how much longer what actually, I know we're late in the thing, but what happened to that company and where are they at now?

[01:56:20] **Stefan Seltz-Axmacher:** Starsky ran outta money. We, we failed pretty, in like late 2019, right before 2020.

Around that. By that time, we, to my knowledge, were the most commercially successful L four trucking company. We were doing about $7 million in annualized revenue run rate in freight that we're hauling mostly with regular trucks.

But our customers thought we were hauling freight with like unmanned self-driving trucks.

We did the world's first ever driver out autonomous run on a live highway.

So we drove a truck for seven miles, like in regular traffic with no person in it. and we, went to VCs and were like, Hey, look the tech works like we need.

Here's our safety testing plan that will allow us

In about 12 months to be having five trucks driving about full-time and no person in it.

The business more or less works like, here are the things that we need to do to make it be outright profitable and an interesting and like very cookie cutter, running a trucking company, types of things that we need to do.

We've made, we've proven all the stuff, let's go, give us $50 million dollars.

[01:57:28] **Audrow Nash:** Yeah, we did the hard

[01:57:28] **Stefan Seltz-Axmacher:** Super profitable. And VCs looked at us, they're like, wow. So you're working really hard. running a trucking company is hard. Robots are hard.

[01:57:37] **Ilia Baranov:** hard.

[01:57:38] **Stefan Seltz-Axmacher:** and you're saying that with another $50 million, maybe you can be a trucking company with 50% margins. That kind of sucks.

[01:57:47] **Audrow Nash:** Oh

[01:57:47] **Stefan Seltz-Axmacher:** I would way rather give $50 million to DocuSign 5.0 where for $50 million, they'll create $40 million of revenue, but they'll have 90% margins on it. And, and anyone in San Francisco can run that company. Like you don't need some special weird unicorn. Like anyone in the world can run a unicorn SaaS company.

this, this autonomy thing isn't a great business, is it?

[01:58:15] **Audrow Nash:** Oh, what a thing. Okay. And then, so after that, then you effectively picked yourself up

[01:58:25] **Stefan Seltz-Axmacher:** Yep.

[01:58:26] **Ilia Baranov:** Yep,

[01:58:26] **Audrow Nash:** started, Polymath with this and used a lot of the lessons and like Interesting. I see.

[01:58:34] **Stefan Seltz-Axmacher:** So like I, COVID happened. I went and hung out with a bunch of SaaS companies. I had an interesting experience where, while I was hanging out with SaaS companies, I took a deep look at like the NetSuite ecosystem, if you're familiar with it.

[01:58:47] **Audrow Nash:** Is that like Microsoft what? What's NetSuite?

[01:58:51] **Stefan Seltz-Axmacher:** so netSuite is this big, crappy piece of enterprise software to do accounting set up in a super special way.

So if you've worked at a company with more, than 500 people, they probably use NetSuite or something like it, think of it like QuickBooks, but a couple million dollars and then a couple million dollars to implement it a super special way because Coke likes to do, its accounting slightly different than Pepsi does, who likes to do it slightly different than, I don't know, Snapple or whatever. and when I looked at that ecosystem, I saw software that didn't just work, right? There was software that like, it wasn't like Gmail where you swipe a credit card and you have an inter and you have an email account. It wasn't like Uber where you download an app, hit a button and a car shows up.

it was software where you buy it, you spend a bunch of time integrating it, not even just business to business, but you spend a bunch of time configuring it to work just for you. And then it is one of the most valuable pieces of software in your entire stack.

[01:59:53] **Audrow Nash:** whoa.

[01:59:54] **Stefan Seltz-Axmacher:** And I don't think Robotics is ready to be Gmail yet, and I don't think

Robotics is ready to be Uber yet. But I think Robotics is ready to be something that you buy, configure, and then is a key part of how your business operates.

And that's why we're building Polymath the way we are

[02:00:10] **Audrow Nash:** I love it. Almost like a, I don't know, Zapier or something, like some automation

[02:00:15] **Stefan Seltz-Axmacher:** like, like Zapier without a nice UI with Zapier, but you have to hire consultants to set it up.

[02:00:23] **Audrow Nash:** Yeah. Cool.

[02:00:25] **Stefan Seltz-Axmacher:** Zapier's pitch was probably like we make it so you can do Oracle type integrations without a team of consultants was probably their seed pitch.

[02:00:35] **Audrow Nash:** huh. Yeah. What a thing.

Okay.

[02:00:39] **Stefan Seltz-Axmacher:** Okay.

[02:00:41] **Audrow Nash:** let's see. So last, there's one more thing I wanted to ask. So we had, advice, you guys both gave your advice.

Oh, Ilia, I wanted to ask, 'cause you mentioned side projects, you build your own trinkets for these kinds of things. I wanted to see, what you think of side projects.

I think they're super important, as a way of growing your skills and staying relevant, but I wanna see what your perspective is on them and from a CTO perspective too.

## Thoughts on side projects

[02:01:18] **Ilia Baranov:** Yeah. yeah, no, for sure. I, two things. One is my side projects keep me sane, because, especially as you get into the, more CTO roles, like I would love for most of my day to be coding, but like maybe 10% of it is realistically and 90% is everything else. so doing the side projects keeps me happy.

but the other funny thing is that my side projects end up being, aligned with Polymath some of the time, which is interesting. so early, on we didn't really have a good way to emergency stop our vehicles remotely. So as the demo we gave, we have this completely remote vehicle, so like none of the line of sight e stops will work for us, right?

And fort's, wireless over network stuff wasn't ready and nobody else was providing anything of real value. so because I had built up some stuff in like Arduino land basically, I was able to, quickly throw together a prototype emergency stop that ended up being relatively robust.

[02:02:25] **Audrow Nash:** Nice

[02:02:27] **Ilia Baranov:** and those sort of things, I, think. TLDR is that side projects are critical, especially I'd say there's almost like a bathtub curve when you're junior. They let you iterate quickly, and when you're very senior, they let you keep your sanity because seniority tends to correlate with meetings.

It, not always, but in a lot of ways. so they let you like just quickly prototype something and test it out. and I find the risk for, I would say not as much in robotics companies, but for software companies in general is over time as they become larger, there's this growing divide between people making decisions and people writing code. And if the people making decisions don't make a habit of writing code and being connected to the system and like basically being a chaos monkey is another thing that I do quite often that I highly recommend

[02:03:16] **Audrow Nash:** I dunno what it

[02:03:17] **Ilia Baranov:** put out an API and I'll just write like the worst possible code.

[02:03:21] **Audrow Nash:** Yeah.

[02:03:22] **Ilia Baranov:** yeah, it's just I'll write the worst possible code to talk to our API and break a whole bunch of stuff by accident, but by

doing that, we'll figure out like, oh, like we

didn't handle this exception. Or a, dumb user like me would've thought it works this way, but it works that way. And like all of this stuff. and, all of that all flows into keeping your sanity and having a good business.

[02:03:45] **Audrow Nash:** Hell yeah. Yeah. I, think it's an interesting thing. I feel like, I've been doing side projects really regularly for a few years now. Like every evening I'm working on a side project, which I absolutely love. It's like some of my favorite time each day. but or, so one of the things with that is I feel like, you learn through your own pain how to make good architectural decisions.

And I feel like that's a very hard thing unless you're going end to end in something you're building. And it's, it like if I just focus on the one specific narrow thing that I'm working on in work, I don't understand the end-to-end process, but when I'm working on that one specific thing, it's easier to make better decisions if I understand the larger context through doing the whole process through side projects.

That's been one of my thoughts on it recently,

but

[02:04:43] **Ilia Baranov:** totally,

[02:04:43] **Stefan Seltz-Axmacher:** of sense.

[02:04:44] **Audrow Nash:** hell yeah. alright. So questions.

what are you guys excited about in Robotics? what are the things you're looking forward to? Ilia, let's start with you.

## What Stefan and Ilia are excited about in robotics

[02:04:56] **Ilia Baranov:** I'll come back to my experience at least with Amazon, where, the Astro program, I think, and for, your listeners, if they haven't seen, so Amazon has a home robot called Astro. You can find it online, theoretically you can buy it. I don't know, I don't make their business decisions, but you can actually play with this thing.

It works reasonably well. We have one at the office just for fun. but them and Samsung and Sony and basically everybody and their dog has made these kind of human interactive robots.

But the, little piece that they're missing is the question, the very small question of what the hell does it do, which nobody has answered yet. And the killer app for robots in the home seems to have been vacuuming from like the 1990s till today. And nobody's come up with a better idea. And I'm still waiting for what is the next killer app for Robotics in the home. putting away dishes or laundry, like everybody, that's the first thing everybody jumps towards.

But manipulation is very expensive and complicated. And even if ML Magic fixes it, like just the actuators are very expensive.

Nobody's gonna spend even $5,000 on this, right? And $5,000 for manipulators ridiculously cheap, right? For a good one that moves around and stuff. anyway, so I think we're still missing the killer app in the home for robots, and I'm excited to see what that ends up being.

Maybe it's an embodiment of these. Assistance machine learned based approaches of just shout in your room. Hey, find me a path to this theater, and this screen magically comes over and talks to you and tells you what to do. I don't know if I knew maybe we'd do that company, but for now we're in industrial space and, a different, business.

[02:06:37] **Stefan Seltz-Axmacher:** This whole thing sounded like what we did at the beginning of our podcast where we'll start like coming up with these things and be yeah, but wait, I could already ask that question anywhere in my house. And it gets answered for me, and the screen that pops up is my cell phone. And it just happens already.

So why do I need a screen on an arm in each room of my house? I'd say what I'm most excited about, so for better or worse, the self-driving car industry threw a lot of money and interest into robotics. I think like more than other spaces, I, know there's a lot of quad copter people, but from my own perspective, it seemed like way more people got way more excited about self-driving cars than quad copers.

And now there's a lot of people who have worked in and around Robotics and like some of those people have been siphoned off to LLM rappers for XYZ and like some of those will become real businesses or not. And there's like a lot of, there's a similar flavor of self-driving car hype that's happening in humanoid Robotics right now.

And my hunch is it will go roughly the same as it went with Robotaxis. which you could decide how much sarcasm you wanna read into. but I think we now have a critical mass of people who care about robots who, are hooked on these sorts of problems in such a way where Dropbox 5.0 is no longer an appealing job. And that now, like they need to build robots for something.

And many of those people will work on nonsense, like the robots for robot's sake. But I think we're gonna have more real Robotics companies doing valuable and interesting things in the next founded, in the next five years than we had the last 100 years.

and I think like right now. Probably the most successful Robotics company of all time outside of defense and mining is, is probably iRobot. And I think you'll have five to 10 companies as successful as iRobot in the next five years.

[02:08:41] **Audrow Nash:** Cool.

[02:08:42] **Stefan Seltz-Axmacher:** even 50. And that's gonna be fucking cool.

[02:08:48] **Audrow Nash:** Hell yeah.

That's awesome. I think you're probably right with that, and I think that is such an exciting thing, and that matches my observation too, that there's a bunch of people that are hooked on this and they want to be using it for

[02:09:05] **Stefan Seltz-Axmacher:** man, boring SaaS just is not something like I desperately did not wanna start another Robotics company. Like I was so wanting to do something simple that like I was even working on like a, an e-commerce for planning funerals idea for six months. That seems more cheerful than go be miserable in the mud with robots.

And the thing is, I just can't work on anything else now.

And I think like a lot of people feel the same as me, so maybe right now some of them are doing, open AI for asking your plumber questions and there's money in that right now. But there's a lot of people at those companies thinking, how do I get back to Robotics?

Where do I find a Robotics application that is fundable and buildable and valuable? And I can't wait for that to start bearing fruit.

[02:09:55] **Audrow Nash:** too. Hell yeah. I love that answer. Okay. Hell yeah. thank you both. It's been so much fun having you on the

[02:10:02] **Stefan Seltz-Axmacher:** Thanks so much, Audrow.

[02:10:05] **Audrow Nash:** Hell yeah. All right. Bye everyone.

[02:10:07] **Stefan Seltz-Axmacher:** It was a pleasure hanging out. Thanks so much for joining us.

​

[02:10:10] **Audrow Nash:** You made it!

I should be quiet just in case you're sleeping peacefully. In any case, I hope you enjoyed the interview.

What did you think? Is Polymath Robotic on to something? Would you use their service? Did you like the demo? I'd love to hear what you think in the comments or on X.

Also, I host a weekly space on X on Thursday evenings, US time, where we talk about all things robotics, including this interview. Feel free to come and chat.

Okay, that's all. Happy building.

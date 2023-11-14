# Rethinking Robotics: Electric Sheep's Journey to Safer, Smarter Machines

## Table of Contents

- [[00:00:00] Start](#start)
- [[00:01:32] Introducing Nag + Mike + Electric Sheep](#introducing-nag--mike--electric-sheep)
- [[00:02:51] Large world models](#large-world-models)
- [[00:06:24] Learning physics](#learning-physics)
- [[00:10:08] Robot sensors](#robot-sensors)
- [[00:17:57] Introducing ES1 as CatGPT](#introducing-es1-as-catgpt)
- [[00:20:17] ES1’s input / output](#es1s-input--output)
- [[00:21:52] End-to-end learning for robots](#end-to-end-learning-for-robots)
- [[00:26:51] Getting data](#getting-data)
- [[00:27:47] Electric Sheep’s background](#electric-sheeps-background)
- [[00:30:49] Business philosophy at Electric Sheep](#business-philosophy-at-electric-sheep)
- [[00:33:19] Sim-to-real + long tail events](#sim-to-real--long-tail-events)
- [[00:36:38] ChatGPT](#chatgpt)
- [[00:42:01] Building for safety](#building-for-safety)
- [[00:49:25] Safety with AI](#safety-with-ai)
- [[00:54:23] Apple’s surprise new features](#apples-surprise-new-features)
- [[00:58:06] Generalizing learnings for other tasks, like snowplowing](#generalizing-learnings-for-other-tasks-like-snowplowing)
- [[01:03:35] AI architecture](#ai-architecture)
- [[01:07:09] Training to mow straight lines](#training-to-mow-straight-lines)
- [[01:11:19] Why not Robot-as-a-Service?](#why-not-robot-as-a-service)
- [[01:17:08] Boring businesses + robots + AI](#boring-businesses--robots--ai)
- [[01:24:34] How do we build the data model?](#how-do-we-build-the-data-model)
- [[01:29:07] Getting into dexterous tasks](#getting-into-dexterous-tasks)
- [[01:30:28] Building a monopoly](#building-a-monopoly)
- [[01:31:23] Advice for our new world of AI](#advice-for-our-new-world-of-ai)
- [[01:40:37] Links and contact info](#links-and-contact-info)
- [[01:41:33] Hanging out](#hanging-out)

## Start

[00:00:00] **Audrow Nash:** I've talked to a lot of people about this interview, and I'm excited that I get to share it with you. In it, I talk with Nag and Mike from Electric Sheep. They're doing many things differently than most robotics companies that I've talked to, and they're making big bets that I think will pay off. Here are three examples to show you what I mean.

First, they're throwing away classical robotics approaches, and instead... using machine learning. I'm not just talking about for perception or parameter optimization, but even for things like localization or high level control. Second, they've turned the lawn mowing problem on its head to make robots that are intrinsically safer.

And third, instead of selling their robots or doing a subscription model, they buy profitable landscaping businesses and give those companies robots. There are a lot of advantages to this last point and you'll see the details of each during the interview. I hope it surprises you as much as it did me. I think you'll enjoy this interview if you're curious about how AI and robotics can fit together in a real application and if you want to see a new robotics business model that I think will be very popular in the near future.

I'm Audrow Nash, this is the Audrow

Nash Podcast, so let's see why Electric Sheep is doing things so differently, and I'd love to know in the comments or on X. What do you think about their bets? Would you take them? Are you convinced? Or do you see some weak points? I hope you enjoy.

Hi everyone.

Nag, can I have you introduce yourself?

## Introducing Nag + Mike + Electric Sheep

[00:01:37] **Nag Murty:** Yeah. Hi everyone. I'm Nag Murthy. I'm the CEO and co founder of Electric Sheep Robotics.

[00:01:44] **Audrow Nash:** And Mike, would you introduce yourself?

[00:01:46] **Michael Laskey:** Hi everyone. I'm Mike Lasky. I am the Vice President of Autonomy at Electric Sheep Robotics.

[00:01:52] **Audrow Nash:** Awesome. Now, Nag, would you tell me a bit about Electric Sheep? What do you guys do?

[00:01:58] **Nag Murty:** Sure, yeah. We are an outdoor maintenance company powered by artificial intelligence and robotics. So the way we work is we acquire traditional outdoor service providers. And we then progressively transform their operations by deploying our own proprietary AI software and robots. and basically what we're doing at the back end is we're building this large world model that can effectively drive all outdoor autonomous equipment.

And then over time, we plan to use those, automated robots to improve our own margins over time. So that's what we do.

[00:02:34] **Audrow Nash:** And you're starting with lawnmowing at the moment. So that's the first embodiment, I suppose?

[00:02:39] **Nag Murty:** That's right. So that's the first instance of what the model, you know, automates.

[00:02:46] **Audrow Nash:** Gotcha. And so there's so much that's interesting to unpack there. let's start with why, like the approach you guys are taking. Yeah. I suppose. Like, so why is it these world models? Like, what is that? And why is that interesting? maybe Mike, is that, is that a good one for you?

## Large world models

[00:03:09] **Michael Laskey:** Yeah, I can take that one.

So I think, I think there's like a, there's kind of two fronts of it. One is like, what's, what's the architecture? What's the approach of how we go about designing these robots? And then the other side is like, how do we get data? How do we actually train these models? So at Electric Sheep, we're very much like, we believe that...

The future of robots is a learning robot. A robot that can understand the world in an intuitive way, can relate to it with more of a natural instinct that progresses over time from experiences, and can be interacted with in sort of the, the UX that you might interact with like an outdoor work animal. So natural language, visual, like there should be no app.

So none of our robots have apps. They should just have simple like on off buttons, and that's about it from a sort of like button interface standpoint. now, to create this sort of intelligence and this experience, there's sort of like two ways you can do it in robotics, right? There's, direct policy learning, where you say, okay, well, I'm going to like push mow and just take all my push mowing experience and train the robot to do push mowing.

And then on the flip side of that, when you look at sort of like different RL, like MDP celebrations, there's you learn the model. So instead of saying, I'm going to teach this thing to only push mow, it's you're saying, I'm going to teach this thing to learn how the natural world works. And then you can tell it to do different tasks.

Then you can say, oh, oh yeah, sorry?

[00:04:34] **Audrow Nash:** So you're saying like in a reinforcement learning context, you are, it's almost like you're generating like an embedding or something. You're learning how to learn by getting like an efficient representation of reality or something like this. And then you use that to get more specialized into a specific task.

Is that, like, is it along those lines or what do you think?

[00:04:56] **Michael Laskey:** It's along those lines. Like if you, you know, if you're familiar with kind of like the old ideas of reinforcement learning, it was the idea of the agent's policy. So it was like given a goal, how it would try to like respond and achieve that goal.

But then there was the other concept of the environment model, or the transition function. And that was how the agent would in its head see, okay, well if I'm in this state and I take this action, what happens next? And what's cool about that representation is it's kind of like task agnostic. so it's more like if we can give the robot intuitive physics and intuitive sense of how the robot behaves, we can then have it synthesize arbitrary tasks.

because today we're push moving, but tomorrow we might say, well, can you strengthen it? And it's like, well, I know how movement works, I know how semantics works, I know collision avoidance. Let me go and do those, tasks with that.

[00:05:47] **Audrow Nash:** So you're learning a lot of, like, fundamental things about how reality works.

That's the goal? Nag, do you wanna?

[00:05:55] **Nag Murty:** Yeah, that's exactly it, right? At, you know, basically, that's the world model that, you know, the robot has in its head. And so, it uses, it uses those intuitions to sort of perform these different tasks. so all these tasks are like policies that you can learn that are specific to that task being performed.

So mowing, sweeping, snow removal, but at its core, there is a task agnostic world model, which is independent of the task being performed.

## Learning physics

[00:06:24] **Audrow Nash:** So that sounds amazing to me. and I'm wondering, like, how do you, so I would wonder, my first thinking would be physics. like, our models of physics are pretty good for probably like lawn mowing and things like that.

They're not good for fine manipulation yet, probably. I mean, I haven't seen work anyways. how, how do you, do you just, do you kind of like, where are you using things like a physics emulator, and where are you learning stuff? Are you learning everything, or how does it, how does it work? Maybe Mike again?

[00:07:00] **Michael Laskey:** Yeah, no, great questions. So I think when you look at You know, TAS in outdoor landscape, you're right. You kind of have like two camps right now of TAS. There's your mechanized surface coverages, your snow plowing, your push mowing, your street sweeping. And then there's like really fine grain, like tree trimming, where pick an apple, prune a bush.

so what we want to do is definitely take this like a roadmap. And we first started off saying like, okay, well. There's a huge amount of bulk labor in mechanized surface coverage. So let's first just think, what would the world model need to do to solve these tasks? And then build in a way, though, where it can be scaffolded to Dexterous later.

so, like, it's, it's pretty generic, like... AI kind of tech, so it's definitely scalable, but now when you look at like something like a snow plowing or push mowing, you really have like, four key challenging things that need to be done in order for the robot to affect the report, like four like kind of key AI concepts.

So one of them is, so think just for mowing for a cleaning sample, you need to have collision avoidance. But it's subtle because some things you actually have to get very close to and touch. So you have to have this concept we would call like semantic collision avoidance. Like understanding like, oh, I can push my mower right next to a bush and mow an area, but when I'm in like, when I'm next to like a human or a tree, I can't.

and then you need obviously mapping. You have to have some sort of global map of the world to know what you've mowed before and what you have mowed. And then for commercial mowing, you need actually, a lot of people don't, this is actually a really hard nuanced problem of mowing. You need to lay down these very precise, straight lines, so you need high quality localization.

better than like most people would try and get for in like a self driving car application. cause a professional landscaper looks at these lines and they basically say if this robot was good or not. And to do that you need to have this very precise... Ability to follow lines and lay them down over like hundreds of meters of stripes.

so when you combine all that, you need mapping, localization, 3D awareness, the ability to understand what's traversable, what's not. And these are the core concepts. So, like you're saying, you don't really need...

[00:09:19] **Audrow Nash:** What was the fourth one? I have collision avoidance, mapping, and straight lines. What was the fourth one?

[00:09:24] **Michael Laskey:** Semantic traversability, I would say. Like, really understanding, like, what you can mow over versus not. which is almost like a semantic problem of like, is this mowable, basically.

[00:09:35] **Nag Murty:** So take leaves on the ground in the fall, right? It's okay to go over them. Like a toy bunny rabbit on the ground, not okay.

You know, so, it's a, sprinkler heads, not okay. Not okay.

[00:09:48] **Audrow Nash:** Big bummer. Mm hmm.

[00:09:50] **Michael Laskey:** Yeah, and like, what most products in the market do today is you teach it, through like, you know, precise, like, joysticking, how to, just avoiding things. what's very different about what we're building is there's no teaching. This robot must semantically see the world and understand if it can go over or not.

## Robot sensors

[00:10:09] **Audrow Nash:** Okay, so how do you do that? How do you semantically understand the world? and maybe the best way to start would be like, are you using, what sensors are you using? Is it your cameras primarily, is what I would imagine? Maybe depth cameras, or what are you guys doing there?

[00:10:25] **Michael Laskey:** Yeah, so our robots are equipped, I'm a huge believer in stereo vision.

So the robots are equipped with just one stereo camera. just one.

[00:10:36] **Audrow Nash:** That's super cool. Just one, yeah. You don't have like 40 all posted around, which is what it seems like many do. I mean like autonomous cars will have them everywhere. Okay,

[00:10:47] **Michael Laskey:** yeah, I mean we very reduced the like weight and size of our platform that we felt like from a safety standpoint You could do one and one's interesting because now you're in the domain of like a human, right?

You have like similar like human eyes what you mostly see in other animals This also forces you to reason across time and space so you can keep track of like what's around you How do you look around and like

[00:11:08] **Audrow Nash:** which is super cool? Yeah, that's why it's surprising that you have one Okay, so then you take that stereo Image Data.

So you're getting 3d information about the world and image information. You've kind of are superimposing them. And then you're running that through some. Sort of neural network to establish semantic understanding, like object recognition or what do you do from there? Or it's, it goes into just some neural network and, you'd say good, bad and it eventually does the good thing, or what, how does it go?

[00:11:39] **Michael Laskey:** Yeah, so right now how it works is we feed a stream of video stream stereo video into what we're calling ES one. and then the, also the other thing we feed in is uncorrected GPS, so non R-T-K-G-P-S. This is relatively cheap, simple to get, and you kind of want, like, Nog has a good analogy that kind of, like, relates it to, like, pigeons, like, how they use magnetic sensing to navigate.

So, you know, it's kind of like, it's something that is there, it's very easy to get when you don't want non RTK, so we feed that in as well.

[00:12:11] **Audrow Nash:** I love that approach, because, so you're learning, like, RTK GPS is very accurate. It's like, what is it, like centimeter or millimeter level accuracy? On the good

[00:12:21] **Nag Murty:** days, yeah.

[00:12:23] **Audrow Nash:** Yeah. Well, yeah, it depends on coverage, depends if you have beacons or something set up for it to triangulate with, all sorts of things. But, it's very expensive too. and all this thing. So you're just using, or maybe it's come down in price, right?

[00:12:36] **Nag Murty:** It's, it's not so much the expense. I think, sure, there is, you, you get like those Trimble GPSs, which costs like seven, 10, 000, maybe more, but then you also have like these audio simple GPSs, right, which are like in the, but the problem, the RTK corrections is you can't rely on them.

Right. So you have all these multi pathing issues. When you go close to the walls or, you know, when you're in an urban canyon, right, you really don't get like the right, you know, signals to get to you, or there's a lot of distortion of the signal that happens. Ionospheric activity can like wreak havoc with like your GPS, right?

All kinds of crazy things like affect it. Cause I mean, think about it, right? Like you're having like these little basketball size satellites, like whizzing past it, like, I don't know, God knows how, how fast you're trying to like get like signals and synchronize them using atomic clocks or something, right?

Like, so it's, it's again, like very classic in its sort of modality, right? Like precision GPS. That's kind of where all of this is. And we don't like classic modalities fundamentally because you have to get everything right and everything precise.

[00:13:47] **Audrow Nash:** Oh, so you, I think I want to talk about that quite a bit, but you, at a high level.

Think they're finicky because of the precision that you require. And so you want robust solutions and that's why you rely on GPS and these kinds of things.

[00:14:02] **Michael Laskey:** When you scale the products with it, on good days when you get it, it's really amazing. But there's a lot of bad days.

[00:14:09] **Audrow Nash:** But finicky and lots of failure cases and, uh, sorry, Mike, go ahead.

[00:14:14] **Michael Laskey:** Yeah, exactly. It's an unreliable service that in a lot of places in the country you just can't rely on at all. Or on different weather days.

And you also are pushing your bill of materials to be cheaper, which is a big advantage too. like having only one stereo camera means you need only one input.

One chip thing to accept one stereo camera. Pair of information. Like, it's not like you need a custom board that goes to 30 stereo cameras. And it's like, it makes all the, and then you don't need a crazy processor to process all that. You're not storing an insane amount of data that you have to upload and figure out all that.

It makes all the downstream problems also easier. I would imagine to do these kinds of make these decisions. It seems like power moves to me, like you guys are making power moves in how you're doing stuff.

We said ML was going to drive every major decision, and then we designed the stack to force ML to do that.

So we said, no external calibration, no ability, no, yeah, no redundancy in sensing.

[00:15:22] **Nag Murty:** Here's the, yeah, this is the crazy part, right? You gotta, there's a history to all of this, right? And we have flirted with like classical approaches, scaled classical robots. In the first two years of our existence, right? And we are deeply aware of like how amazing it can be, but also deeply aware of how painful it gets when you go down that route, right?

Like we had like these big massive ouster lidars and like, you know, all kinds of crazy things. On our robot. And then we just said like, throw away all that. Yeah. Hell with it. You

[00:15:56] **Audrow Nash:** know, I wonder if it's like a pendulum and you guys have swung, you started one way and you're going to swing the other, and then you're going to find a happy medium eventually that's a bit more, in the middle.

I like, I don't know. And maybe the other methods are working wonderful.

[00:16:11] **Nag Murty:** I think, yeah, I think the thing is, one way to think about this is, right, I think that we won't swing back primarily because this is now a data problem at its core. It's not like a sensor problem. It's not a calibration problem. It's not a sensor quality problem.

None of that.

[00:16:30] **Audrow Nash:** Interesting, yeah, so you don't have most of those problems now to solve with classical methods. Interesting.

[00:16:36] **Nag Murty:** Every time you have a classical method, you always come down to like, how good is your accelerometer, right? Like, do you have like high quality accelerometer? Does it like, cause that's the thing that ties in like your whole slam stack together.

[00:16:47] **Audrow Nash:** Yeah. So how does, so with your normal GPS, you're basically saying we think this is going to be somewhat unreliable and therefore your system will behave accordingly. For this kind of thing, it's just that you'll adjust for the information that isn't good, but is something. is that, that kind of the thinking with not using RTK and just using regular GPS?

[00:17:13] **Michael Laskey:** Yeah, cause, so this all feeds into what we call AS1. One of the outputs of AS1 is essentially maps and localization. now... Non corrected GPS is only so good, but when you combine that with, let's say, a Learn VO that's happening interior to ES1, you can... Visual odometry.

[00:17:34] **Audrow Nash:** Oh, okay. Acronyms. I don't even know them in my own field.

Okay, visual odometry.

[00:17:38] **Michael Laskey:** Perfect. Yeah, so another way of doing localization is to use, of course, camera data. It's like how humans do. Walk around, we see movement with our head related to vision. So, internal to our network, it's able to kind of fuse the GPS with visual data and produce better pose estimates.

## Introducing ES1 as CatGPT

[00:17:57] **Audrow Nash:** Mm hmm. Okay, so you get your pose estimate. So maybe Nag, what is ES1?

[00:18:04] **Nag Murty:** I think that's a question better answered by Mike, but I'll take a stab at it. Like ES1 is essentially, I joke about it and call it like CatGPT, if you want to call it that, right? Which is essentially

[00:18:15] **Audrow Nash:** like computer aided design, like 3d parts.

[00:18:18] **Nag Murty:** No, no, no. Like, no, it's like, it was both. CAT, so it's, if you think, yeah, so if you think of it this way, right, like ChatGPT was to language, ChatGPT fundamentally groks language, right? Fine. All the naysayers aside who question whether it has an internal representation of what languages and all that, but it clearly has some kind of, you know, it's some kind of magic going on in there where it sort of understands the structure of language, the grammar, the nuances, right?

Not just one language across languages. And we're saying there's got to be something similar when it comes to embodied AI, where, and it's non verbal intelligence, if you want to call it that. So ES1 really is something that, sort of captures sort of that non verbal, intelligence. Like it's a way for...

Like a robot to sort of navigate its surroundings, or it's the means by which the robot navigates its surroundings, manipulates physical reality. And it's this one giant sort of world model neural net, if you want to call it that. Maybe Mike can add to this, but that's how I describe it as a product guy.

When

[00:19:30] **Audrow Nash:** I love the, the cat GPT, so cat, like the animal, it like gets around. It's a physical representation. That's super cool. Okay. Mike, do you have anything to add to it?

[00:19:41] **Michael Laskey:** No, I'm gonna just completely go with what Nox said there. No, I think it is that it's it's basically like right now it is like embodied AI and it's supposed to be going after the predictions that a physical agent would need to solve tasks and like look at the the key concepts that we're trying to do of like You know just surface coverage right with no map, no teaching and right now that's what ES1 is trying to predict is those fundamental representations for an agent to do a task like push, mow, snow, blow.

and then we want to keep building on it to get more and more of the embodied AI full stack.

## ES1’s input / output

[00:20:17] **Audrow Nash:** So, you, with ES1, you take in GPS and video, and you output pose and maybe actions, like motor commands, or, what is that, what is the output again?

[00:20:29] **Michael Laskey:** So the output, right now it kind of outputs like, kind of a plethora of representations.

[00:20:34] **Audrow Nash:** Yeah, it's probably a big tuple of a lot of things.

[00:20:36] **Michael Laskey:** It's a big tuple. Yeah. It's like, it's like, which you kind of see in like, you know, like, the, I think like perceiver.io like papers where you have like now like many, like one to many type of representation outputs.

[00:20:48] **Audrow Nash:** Yeah. 'cause you need lots of information for your robots.

For sure.

[00:20:52] **Michael Laskey:** Exactly. So it some of the, so, you know, it's kind of interesting 'cause right now we're sort of testing it by predicting like some of the more classic representations. And then we have a planner that can like synthesize the, basically policies can be synthesized with a planner on top. but, I think as a whole, like, we'll probably at one point start getting to learn planning.

But, what it does today, is it outputs, like, a point cloud of the world, a semantic understanding of the world, so like a 3D semantic point cloud. a bird's eye view map, so it says, here's where you are, here's what you've covered before, the exact position of the robot on the map. so... And then, also, what's kind of interesting is like, low level obstacle detection.

So I would say like, oh, here's a manhole cover. Like, oh, here's your child's bunny. This is a 3D cuboid. Like, do not go near it. Yeah.

[00:21:42] **Audrow Nash:** How do you, I mean, there's a lot of questions, I have a lot of questions about that, just in general. So, how much is it like, So I interviewed, like, many years ago, Sergey Levin from Berkeley.

so he's a professor who's like, End to end robotics stuff, so you basically pass in raw sensor input and you output, like, actions to do the task. this seems a bit like that, and maybe you have a better description of his work for this kind of thing, but how, it seems like this is very similar in spirit to me, and it might be the same thing.

what do you think?

## End-to-end learning for robots

[00:22:22] **Michael Laskey:** Yeah, I mean, so he was, he was on my cause committee, so I'm pretty used to debating with Sergey, actually. but, so I think, I'm, like, at a very high level, like, I really agree with a lot of his approaches. and if you look at, like, the body of his work, it really says, like, yes, robots need to learn from actions and experiences.

You need to collect a lot of data, and they need to have recitations that are good enough they can actually efficiently learn. and search algorithms in RL. Where I think ES1 is slightly different is instead of just predicting, like, let's say like it's trained policy, for example, well, okay, just a bit of a caveat.

It's kind of hard to argue with Sergei as a whole because he's done so many papers that it's like, what's the specific one that, you know, you're trying to predict?

[00:23:09] **Audrow Nash:** Yeah, for sure. Because ES thinking is moving. It's like a big tree advancing. Right, exactly.

[00:23:15] **Michael Laskey:** For sure. So, but if you just look at maybe, like, the RL community, rather than learning a specific policy, what we're trying to learn is like a representation of the environment.

And then this is something that you can call like planners or learn planners that can operate on top.

[00:23:35] **Audrow Nash:** Okay, the way that I would think of it, and maybe this isn't correct, and I, maybe just, when I was in grad school, all the things were like embeddings and you learn efficient embeddings for things. so you learn a good way of representing something and then you can do like one shot learning or something if you have a really efficient.

embedding that lets you learn a new task really quickly or something like this. Is it, is it at all similar to this or is it, I don't know, how does it fit with that? Or is that just like an outdated model? or just a different model.

[00:24:09] **Michael Laskey:** I think that's where you would actually want to go. So right now we actually predict presentations that are more human interpretable, like a point cloud or a semantic map.

yeah. And then we call like, you know, a planner that we might code on top of that. And that, that works for today. It also works for scaling a product because you want that interpretability as a, as an engineer, especially when you're trying to. Product fit. There's a lot of UX that you have to code. So there's a lot of practical reasons that we do that.

But as we evolve and scale, our sole goal would be to replace everything, you know, to you. Just get to a point where it actually predicts like, here's a thousand dimensional float vector. And then the planner takes that.

[00:24:53] **Audrow Nash:** but raw input from the sensors. Yeah. All that.

[00:24:57] **Michael Laskey:** But like having worked a lot in my PhD with systems like that, when you're actually deploying something, you have an end customer and they're like.

Oh yeah, why'd your robot like hit a tree? Yeah, then you, you really want somebody to fall back on of saying, well this is what it thought, and you can as a human interpret that because it's a representation that makes sense to, people, really.

[00:25:19] **Audrow Nash:** Yep, so what's the, what's the point of, so if you're outputting a point cloud...

How different is it than just a normal point cloud that you'd get from a depth camera? I guess it has some semantics included, or like, why not just go right to a point cloud from your sensor? For this kind of thing.

[00:25:41] **Michael Laskey:** Yeah, I mean well basically because we're just feeding in left and right stereo You know one of the representations that will do is create.

[00:25:47] **Audrow Nash:** Oh, you're not doing any of the calibration and things like this You were saying is that true?

[00:25:53] **Michael Laskey:** Yeah, so you can just feed in like two images With minimal you can have a pretty like rough estimate of your baseline, but you don't need like machine tolerance on that Like you can be off with like a couple of centimeters.

[00:26:08] **Audrow Nash:** Okay. So let's just backing up a bit. So what we have so far is you guys have this ES1 system. This ES1 system takes camera and GPS and it outputs a big bunch of information, including like a point cloud, maybe motor commands, all this stuff. and so the goal is to have this be more of like a learning system that you can make more flexible over time.

And it's starting with lawn mowing, but potentially getting into a bunch of other applications. that all seems wonderful to me. It's, I wonder how you, so how do, how do you get your data, I suppose, for all this? Like, and like, do you use simulation or how did, how did you get started? I suppose. cause getting started to me sounds like it sounds wonderful, but it sounds like you need a lot of data to even get started and maybe I misunderstand something.

## Getting data

[00:27:11] **Nag Murty:** Yeah. I think Mike can go into the Simtorial part, but like there is a precursor to this, which is, you know, when we were in operation for the first couple of years, we generated a ton of data. Right. That helps seed some of these efforts. And then Mike brought in sort of the Simtorial angle to this, which he could talk about, and then sort of using both of those got us to like a 80, 90 percent good enough product, and then from there on, yeah, it's, it's like our data engine that really drives those.

Like, corner case improvements over time, but Mike can delve more into the sim to real part.

## Electric Sheep’s background

[00:27:47] **Audrow Nash:** Or just before we get into the sim to real part, so, more background on Electric Sheep. So, how long have you guys been around, and Nag, you've been, you're a co founder, right? That's right, yeah. How long have you guys been around?

[00:28:01] **Nag Murty:** three and a half years. we got our first, we raised, like, a pre seed round in, like, Jan of 2020.

[00:28:10] **Audrow Nash:** Wow, right as the world shut down.

[00:28:13] **Nag Murty:** I know, like just snuck it right in, you know, just like before the world shut down.

[00:28:19] **Audrow Nash:** Okay. Yeah. So then for the first two years or something, you said you were trying classical methods, like it was the same idea in a sense, because I mean we talked before this conversation, Nag, you and I, and Like you guys have a lot of interesting ideas about how to do things and it's, it's surprising to hear, it's like revolut I don't know, awesome on the technical side, awesome on the business side, awesome on the, everything.

So it's, it's cool to see it coming together. But it makes sense that you guys have a bit more history where you've been trying things and you probably had those like different business model ideas back then and then you're coming around to the technical decisions on things and bringing on great people like Mike.

For this.

[00:29:06] **Nag Murty:** Exactly. I think it's been, we've always wanted to sort of build this full stack business. You know, when we first sketched out the idea on a paper napkin between me and Jared, we felt like Jared is my co founder. He comes from the commercial landscaping industry and he's like, yeah, he's like the man when it comes to all things landscaping.

Right. So, and it's, it's, it's important to sort of bring that up because. What shapes our company, right, is this sense of intense pragmatism about what we want to solve, right, and how we want to solve it. and it's, it's sort of the confluence of, you know, three things really. One is this, sort of mindset on like the, the business model is the ultimate goal.

That's that mindset combined with sort of the operations know how that Jared brings combined with the machine learning and autonomy, smart that Mike brings. Those three things all shape our company and shape our vision and they reinforce each other really at the core.

[00:30:13] **Audrow Nash:** They're the pillars that everything builds on.

You have the strong business model, the great operations, and then the great technical.

[00:30:20] **Nag Murty:** And you need all three to sort of come together, for this to actually happen, because this is a complex business to build. It isn't like, you know, and, but, but we feel like this is the only way to sort of to build. To do it.

Yeah. Like if, if your end goal is this moonshot, you know, large world model, which is a chat GPT equivalent for outdoor robotics. This is the only way to do it. We cannot think of any other way and we've tried a bunch of ways. We don't, yeah.

## Business philosophy at Electric Sheep

[00:30:50] **Audrow Nash:** Was that the goal from the beginning? To get the large world model?

Or was it like, as you're in it, you're like, we could do this. And then it's like, maybe this is feasible. or how, how did that come

around?

[00:31:02] **Nag Murty:** I think the goal was to always, we knew the value of data, right? Like that it was true, it was clear that data would sort of lead to an AI revolution. The question was, how do you time it, right?

And what business model do you need to?

[00:31:16] **Audrow Nash:** Oh, definitely. Yeah. The timing is the really tricky thing. Right?

[00:31:19] **Nag Murty:** Exactly. But then you can, you can sort of abstract away the timing if you, and this is what we started with. We said, look, the technology is going to catch up. You know, all of this is going to catch up, but if you solve for profit and revenue, and if you can solve for a profitable way to get the future on your side, exactly, then, you know, whatever is the latest advance in technology.

Can sort of be folded into what you're doing. Right. So you don't take on too much technique, technical debt at the beginning by committing to like, you know, this one approach, right? There's profits are always good. Like revenue is always good. Right. Deployed robots are always good. So solve for that. And then all these other things kind of like sort for themselves.

that's always been our philosophy. Since day one.

[00:32:03] **Audrow Nash:** Yeah, I love that. It is aggressively pragmatic, as you were saying. I think that's wonderful. Cause yeah, if you just have the business alive, like if you, if you just keep it going for a bunch of years and it's doing well and you are making profit, like.

You can always invest in whatever you think the best thing is the whole time. and that's a wonderful thing. versus going and heavily betting on one technology and not optimizing for profit. Like, this is going to be big, but one day it's going to pay off. And, then, I don't know, funding dries up like it is now.

Or, any of these things, you don't find good customer fit right away, whatever, and then the company dies. So just optimizing for profit seems really, really good to me. and Mike, when did you join?

[00:32:51] **Michael Laskey:** So I joined about, a year and maybe like three months ago. Wow. Yeah. and I remember in the interview, Nog was like, I want you to make the mind of a sheep.

And I was like, seems like a really interesting, like, place to join.

[00:33:11] **Audrow Nash:** Okay, hell yeah. Just, okay, so that's the context. So you've been working on this. Now for a year and three months, tell me a bit about, so we were talking about the sim to real gap for this. So we, we generated some data, from the first two years of trying things.

And then, so you add that to seed things with, we have examples of mowing and it working. How, how do we get from there to more sophisticated behavior? How do we fold that in so that you have these learned controllers effectively? Like, how does it all work?

## Sim-to-real + long tail events

[00:33:47] **Michael Laskey:** Yeah, so I think the data that we started with was really, like, it kind of, you know, you start realizing, like, the breadth of the problem, the scope, right, because you've seen the diversity of mowing.

It's a lot more complex than what you might think at first, especially when you're trying to solve it generically with no teaching. But just given my background, I was always drawn towards synthetic data to start, you know, building models from. There's a few reasons why first pre training synthetic data can be a nice advantage to a model, but then actually having the model go out and then learn from the real data, from the interactive data.

So that's generally the paradigm we've been taking now, is using like the landscaping companies that we acquired as like an RL sandbox to like refine the model and teach it about the long tail. But where we start is...

[00:34:40] **Audrow Nash:** What do You mean the exceptions? You mean the things that don't happen frequently?

You're... What's the long tail?

[00:34:46] **Michael Laskey:** Yeah, the long tail of the real world. So, what happens is... Like a kid's toy being left in the lawn or this kind of thing? Kid's toys, like interesting properties where you have like very unclear boundaries of like grass. One of the properties that we're actually looking at, there was like grass that led right up to the pool side.

So the robot would actually have to know, oh, I can't put my cask outside because I would fall down into the water, right? And that, yeah, exactly. Like the interactions with the physical world and that world model. We didn't necessarily cover in simulation, right? Thinking like we would be mowing like right next to a pool and it was a complete like drop off.

so you can never really, I think, you know, like McCarthy has like a really good quote in his Tesla's talk of like, you can never really simulate the world because you don't understand like the true long tail. So you need this like interactive data to cover like the last. Because honestly, when you think about robotics, 90 percent and even 99 percent is garbage.

What you really need is like 6 9's. When you talk about these systems,

[00:35:54] **Audrow Nash:** oh, I get what you mean. I wasn't quite sure what you were saying. So you're saying that if you solve only 95%, it doesn't really, you, you have failure all the time because of that 5%. If you have 99%, you still, if you have thousands of robots running for thousands of hours, you're gonna come up into these really.

Uncommon events that are going to be showstoppers all the time. and that's going to be a giant pain. Okay.

[00:36:19] **Michael Laskey:** Yeah. And then that's why there is this long tail problem where in like a more like SaaS like framework, you can ship an 80 percent model. Like if you actually upheld ChatGPT to like a safety critical system of like...

That'd be terrifying. Right, yeah. Absolutely terrifying. Like don't mess up with the blade. You know, yeah, like.

## ChatGPT

[00:36:38] **Nag Murty:** This is a bit of a, you know, like a abstract sort of question maybe for both of you guys. Like, do you see the analogy between sort of ChatGPT? you know, ChatGPT is sort of this... It's great at Q&amp; A, right?

And there's a bit of like Cleverhand syndrome going on over there, where the human in the loop is sort of saying, yep, that's great. And that's not great. And so you attribute a lot of smartness and intelligence and agency to the model at the end of the day, right? Like, so you think it's amazing, but it's really, you're sort of discarding all the bad stuff it gave you, but like only latching on to the good stuff it gave you, right?

Robots, on the other hand, okay, they're not as clever sounding as ChatGPT. But they have to execute a series of actions and tasks that have to converge to like high levels of reliability, right? And you're seeing the same challenges that, that are happening out there when it comes to things like auto GPT and like some of these other sort of agent driven things that people are trying, right?

They're running into the same issues, the long tail of issues that robotics runs into, but they're running into it in the software realm. And if you ask a roboticist, they'll be like, yeah, it's dumb to like, ask an ML model to like, act as an agent. You know, it's just you need to like, I guess, put another way.

You can't just RL or like expect like good output or you can't like train it to just give you a good answer to a question. You have to train it to converge to perform a series of tasks, plan and sort of reason across the series of tasks. And that's what we mean by the long tail. Over here, in many ways.

[00:38:19] **Audrow Nash:** Interesting. Yeah, I like that. That it's, it's you doing actions over time, and it has to constrain to finish the actions before it can proceed. whereas ChatGPT can just have a witty one time response that had no, like the response before was garbage. And you just discard it, and it doesn't matter.

But this one, it's very sequential in nature when you do robotics. And I totally have seen what you're saying with like agent GPT and things like this where they try to do a sequence of things and like in the middle they write a Python script that has an error in it and then it fails and then it's like, I don't know what to do now, failing, like trying 10 other things, all equally failing, and then it doesn't do anything.

[00:39:02] **Nag Murty:** Yeah, it's a loose analogy, but that's kind of like, and I think it's, it's similar to, you know, the challenges.

[00:39:09] **Audrow Nash:** I agree. It's, it's interacting with complex unstructured systems. Like if it goes and tries to pull the web, the web has a bunch of formats and a bunch of exceptions. Yup. Robotics, the world has a bunch of exceptions.

[00:39:21] **Nag Murty:** Exactly. Exactly. that's, that may be the stronger analogy than like, I don't know, like it, it just stands, right? Like, one of the really fascinating examples we saw in the Sim2Real sort of translation was the, the notion, like, you know, how do you model the sun? And this was all like mind blowing to me when like Mike was talking about it, right?

How do you model for sun glare? And until we actually deployed across like so many different geographies at different times of the day, like we could not get a true sense for how do you sort of, what's the range of. So there's a lot of values you use to sweep for sort of modeling the sun and sin that is relevant to like what we do as a company, which I thought was like really interesting, you know, that example sticks with me.

[00:40:09] **Audrow Nash:** Oh yeah. Mike, any thoughts with, NAGs, uh, connection to GPT or auto GPT and all those things, or I don't know, any thoughts on it?

[00:40:22] **Michael Laskey:** He's definitely right though. Like when you see the consequence of an action in an agent, then you really start evaluating its true intelligence. When it's this kind of these zero shot text prompts, you fill in a lot because you come in with your sense of the world, your understanding, and it's easy to ascribe intelligence to something, but with like a robot, it's, psychologically, it's, it's kind of like, you know, when the robot fails to mow, as humans, we're like, why can't you, yeah, it's the classic like, more of that, like, why can't you do these simple things, like, why is this so hard?

yeah, the failure modes of robots just, they hurt extra more, I feel like, in that way.

[00:41:05] **Audrow Nash:** Yeah, and there's risks, and it could be expensive, and like, I mean, you do a terrible job mowing, or you like, run over a sprinkler, or, like, all sorts of things, like, it can be expensive, it can ruin the client's day, like, all these things, there's real consequences.

For these kinds of things.

[00:41:25] **Nag Murty:** not so, yeah, sorry, not as bad as like the consequences for an autonomous, like self driving car, like, you know, yeah, yeah.

[00:41:32] **Michael Laskey:** A lot of it's more like just sad moments.

[00:41:36] **Audrow Nash:** You're like, damn it. Oh, what a pain. Yeah, for sure. Or like the robot breaks itself. Like if it, if it did just go right into the pool, it's like, Oh, got to get it out of the pool.

All the hardware's broken, whatever, for sure. Yeah, that's funny. At this scale, it's just sad. It's not catastrophic or anything. so how, how do you build in these safety systems? To what you're doing. And I don't know who's the best one to answer this.

## Building for safety

[00:42:12] **Nag Murty:** Yeah, I can talk about it because like my background is in building medical devices before this, right?

Like that's kind of, I guess I, yeah, maybe I'll give you a bit of a segue, right? Like I built my first company out of Stanford grad school. And that was a low cost medical devices company that, you know, it's like being like, it's been in the market for a long time now. It's saved like 300, 000 lives across 22 countries.

And it's been a great sort of learning opportunity to really understand how do you build safety critical systems? Because you know, the devices that like I designed before, you put premature babies in them. And like, that's the most fragile, like, life form you can think of, right? Yeah, really. You put in, like, a device.

And, like, so this approach of, like, safety first, trying to be very, sort of, risk driven, risk minimization driven, always has been the, at the core of what we do as a company. and so, when we first started, right, we started by automating a lot of these, Automating these large 60 inch, 72 inch, zero ton mowers, and which is what a lot of our competitors are also still doing today.

Yeah, like Greensy is doing that kind of thing. Right, yeah. And like, great companies, right? Like, really respect, like, these guys. The core concern that we've had, right, with these systems, and we built, like, we probably had the largest deployed fleet of, like, these large machines two years ago. Right. And we were, we were about to like scale them like in an order of magnitude more, but then we were working with like a, you know, like a IEC, you know, standard safety consulting, 6150 at safety consulting, you know, consultant to sort of figure out how does this apply, you know, when you scale, right.

When you don't have sitters on the ground who are watching these, you know, and safety sitters on the ground, how does it really scale? The short answer is nobody really has an answer today, right? Because you're doing,

[00:44:12] **Audrow Nash:** you're going zero to one in a sense. So

[00:44:13] **Nag Murty:** there's right, exactly. There is no model. 80 companies have solved for this by like, you know, self insuring or whatever.

Right. Like, or, I mean, you know, daddy Google like puts in a lot of money, like, you know, there's like, there's like all that money to blow. Right. So they, they self insure and they get away with it. Tesla has taken the other approach where, you know, they put a guy behind, like there's implicitly a guy behind full self driving all the time, right?

and he's paying for the privilege of like doing self driving testing, which is incredible if you think about it, right? And so they've solved, they've addressed the safety problem that way. They always have a sitter, but then like companies in the robotics space, they are, you know, they only have like.

This notion of, okay, let's put a SICK LiDAR, like, and SICK has a monopoly in this market, right? Or maybe Hokuyo is like some other company that does this, but let's put a SICK LiDAR and let's cover our machine with SICK LiDARs, right? And like that way you can ensure safety. At the end of the day.

[00:45:12] **Audrow Nash:** And so, yeah, they make sure it doesn't bump anything and it's, but then it's a huge data problem and everything.

Like I think of like cruise or Waymo or something, and they just have like sensor, sensor, sensor, sensor, sensor, big rack on top with a gigantic LiDAR on top and everything.

[00:45:28] **Nag Murty:** Exactly. So I think the, then we came to the realization that look, maybe there's a different way to think about safety, which is you still want to build in redundancies.

You still want to go through, you know, like a risk analysis and all that. And that's a given. But then if you look at like, how do you impact like the. You can reduce the probability of occurrence and you can also reduce the severity of occurrence. right. You can reduce the probability of occurrence by building in like some redundancy.

So you can have a mechanical bumper in addition to like your stereo camera, right. To sort of not hit objects. But then you can reduce the severity of it by making these machines smaller. Right? And by making them lower powered than some of these large beastly sort of 60, 72 inch machines.

[00:46:16] **Audrow Nash:** The ones that people ride on and this kind of thing.

And like ride on for industrial things where it's a huge fan beneath them and this kind of thing cutting all the grass.

[00:46:25] **Nag Murty:** Exactly. So then now the question is, do you need that paradigm? Because that paradigm, right, has evolved to meet the needs of efficiency when it's being driven by a human, right? Bigger, better, faster, right?

Because there's a dude driving it. . Right. Robots don't need that paradigm. Right. Because you can swarm a robot and you can have a lot of little like lighter electric basically. Yeah. Electric sheep. So it's safe. Exactly. Safety is driven by like a change in thinking about how you think about form. That's the key thing.

Interesting. I like that, you know, and then you sort of layer in like redundancies that you always have to, you know, but that's kind of it really at the end of the day, and, and that's also explains like why we took this sort of turn as a company, because we're like, we can scale a hundred of like the big machines, but really, is there a future, right?

For like these. Yeah, and there's, it's clearly like the writings on the wall that machine learning, cheap cameras, small robots, that's going to dominate. So let's just go that way.

[00:47:37] **Audrow Nash:** Interesting. Yeah. I like how you've looked at a lot of forces that are kind of shaping like where technology is going and what's working and picked what you think to bet on, like, stereo cameras.

But, so, okay, safety first. You basically, you've made it so that the form is more, much safer. And so your robots, just looking at the videos online, they're basically like push lawnmowers that someone would have. and it's like, it's like an electric, robot push mower, basically. They even have the handle so you can flip it up and someone can use it like a regular lawnmower, I suppose.

[00:48:15] **Nag Murty:** it's more to the Fandle flipping over is really just to, it's to help the robot be driven from one site back to the van. you know, it's for UX, pull it back on a cart or something. Yeah. we don't like encourage, or we don't even design it to be push, like dual use. Because, one assumption about it.

No, no, no, no. That's not the idea at all. you know, because like these robots are already fairly good and autonomous. Like they 80, 90 percent of a given yard. so, you know, we don't really need like, you know, this thing to double up as like a secondary mode. Yeah.

[00:48:55] **Audrow Nash:** Okay. So, that's awesome. I love, I really, I feel like I need to think more about the safety driven by change in form idea.

I feel like that's a very interesting, it's like you just change what you're doing and that changes everything about the risk of this kind of thing and that changes the safety. I think that's a really cool idea. I'm going to have to think more about that. Let's see. Mike. So, tell me about safety from the, like.

I don't know the AI side of things or how you put things in place in addition to maybe the AI controller. I don't know if you have like, here's the AI part of everything, um, and then on top of that you have a thing that says, whoa, whoa, whoa, terrible idea, or something, or how do you... From a software architecture perspective, I guess, how are you thinking of safety?

## Safety with AI

[00:49:54] **Michael Laskey:** Yeah, that's a really good question. So, there's definitely... Like Nox said, we reduced the probability of a severe life accident down significantly. and then, from that, you know, we then said, okay, well let's make the camera... The primary source of safety, and this is where it's going to get a little complicated of my thoughts about, different types of vision problems and the robustness you obtain.

So, when you look at the safety system of a, a push firing robot, right, there's, what's your, what's your number one concern? It's going to be running into people, right, running into a kid or some other human. now that is just pure, like, collision avoidance, and that's what we would call, like, more, like, low level vision, in a way.

where, yeah, like, depth sensors, like stereo, are trying to just solve those problems. And it's actually, it's not, it's not a high level vision problem. You don't have to consider semantics of the world. You just have to think about, like, when you look at the fundamentals of stereo, you're just looking at, like, where does this pixel match this pixel?

So you're actually just doing, like, a... A mapping of two images, so you don't have to think about like true semantics.

[00:51:07] **Audrow Nash:** Yeah, so you're inferring depth and you're using that depth to not hit stuff, I suppose.

[00:51:11] **Michael Laskey:** Exactly. And this is actually something that in the literature, it's been shown time and time again that if you pre train on synthetic data, the raw point cloud is actually extremely robust.

so you can get away with highly like You're not going to get like LiDAR, you know, precision and accuracy, but your ability to estimate like core shape, especially at the distance of like two meters in front of you, is very reliable. We haven't really seen this ever fail. Testing now for over a year on our platforms.

[00:51:44] **Audrow Nash:** Do you ever like someone has like a metal fence or a glass? Wall or something like this or something like that. Are those pretty easy to detect still?

[00:51:55] **Michael Laskey:** Yeah, and actually with like Learn Stereo, especially when you train on like heavily domain randomized images, I've had papers before that show you can like precisely manipulate glass objects with robotic grippers.

That was some work coming out of like TRI, but today we run it next to fences. There's not a lot of glass in the outdoor world, sadly. But, you know, cars and things, which are kind of optically tricky, it works very well on. we've never had an incident where it like ran into an object. Cool.

[00:52:29] **Audrow Nash:** Nag, you look like you have something to add.

[00:52:31] **Nag Murty:** No, it's just, it's just interesting, right? Like, when you design for safety, like, there's, the standards really call for, like, harm. Like, you do no harm when it comes to living. Like, it's specifically humans, really, right? They don't even mention dogs and cats and whatnot, right? So then, this is really a question of...

Sort of what you're designing towards for us, sort of the do no harm is basically do no harm to living objects, right? The non living objects, you can easily sort of RL your way through, right? Like with more and more data points as you, as you. So it's really from a product perspective, it's really not as relevant to be solving for like, you know, uh, even though like it works pretty well.

Yeah, we have to solve for the living things and then, you know. It does like do pretty well on like the non living stuff and where it doesn't like, you can just always like improve it, but that's the minimum bar you want to meet when you're considering safety.

[00:53:30] **Michael Laskey:** I will say it's more like the animal world, not necessarily plants.

we've, I mean, things that we definitely.

[00:53:39] **Nag Murty:** Yeah. Okay. Plants, were

[00:53:41] **Michael Laskey:** also living Yeah, yeah. Like plants aren't gonna count, but like, yeah. .

[00:53:46] **Audrow Nash:** Yeah. I guess

[00:53:46] **Nag Murty:** technically living. Okay. I mean, we, we, we are cutting a plant at every single second of operation, like grass. So, like , I mean, like, sure. Okay. Gotta draw the line somewhere.

Yeah. Yeah.

[00:53:59] **Audrow Nash:** Don't want to kill all the roses in the yard or something too.

[00:54:02] **Nag Murty:** There we go.

[00:54:04] **Audrow Nash:** Okay. So do you have, in terms of architecture, is it like, here is like the front level analysis of the sensor data. Like the first thing it gets to is like, is this alive? And to do that, you go, has it moved? Or is it warm?

Like if you had, I guess you probably just have your stereo one. I'm imagining if you had like an infrared one, Oh, I'm getting the Apple thing.

## Apple’s surprise new features

[00:54:29] **Nag Murty:** That's funny. How do you do that?

[00:54:32] **Audrow Nash:** There's it's hand gestures that make it do things. Let's see now that it's doing it. Look at this. I am unable to turn this off.

So now it just is here, but

[00:54:45] **Nag Murty:** Where you have AI agents everywhere and they're like, you know, oh, can I get you this like did you ask for that?

[00:54:52] **Audrow Nash:** I know, I know. It's so silly. Also, like, if something is bad, let's see if it'll do it. Oh, it's not doing it. Oh, there it is. You can do all sorts of things. It's like a device level, too.

It works in all of the video things. It's not, but anyways. Yeah, crazy. So, I know, I can't believe, the update, I didn't even know. It just, like, I was talking to a friend, and I, like, did, like, a thumbs up or something, and it showed some emoji with that. It's like, ugh. I guess this is what it is now, but so you're doing like a detecting life thing.

Are you doing it right at the beginning in a sense? So like the first thing is don't hit living things and maybe that has some semantics built into it. Like here's a human pose detector or just this thing moved or how do you deal with this?

[00:55:47] **Michael Laskey:** Yeah, so you, we don't explicitly like have a life detector. that'd be kind of, that'd be interesting to go down.

But, you know, so you can, you can start off by just, like, looking at the geometry of the world, right? So, like, how big are humans normally? What size of objects would you have to, like, know you can detect as, like, a geometric problem? so can you just say, like, there's an object in front of the camera?

So that'd be step one. Because you know, like, in this space, the robot should never mow into something that's, like, camera height, for example. So, like, that's gonna pretty much eliminate anything that can stand taller than, like, half a foot.

[00:56:29] **Audrow Nash:** Okay. Yeah, so you don't need to do too much special for this. You just say, don't run into things that are, like, camera height and whatever.

[00:56:37] **Michael Laskey:** Yeah, so that's gonna, I mean, that's what's nice about a lot of these tasks, is, like, you can do pretty simple collision avoidance. But then, it... Go ahead. I was

[00:56:48] **Audrow Nash:** going to see how that... You go.

[00:56:51] **Michael Laskey:** Well, okay, so that's like your, your foundational level. But then it does get more challenging when you actually think about like the semantics of mowing.

Because like what stops our robot from just running to the street? and that could also cause like a huge thing. Here the robot now needs to know, Oh, I can mow over this and I need to turn around this property. and that's where we're at then, that's where the more advanced ML is coming in, like high level vision.

[00:57:23] **Audrow Nash:** Gotcha. I think my wife and dog just got home. He's at the door. let's see. Well that sounds cool. So, I feel like there's a lot to discuss with this. I really want to get into more of the, like, the business model that you guys are going to. but is there anything else? I mean, it seems like a wonderful approach that you guys are using.

Your ES1 system, you're learning a lot. You have simple heuristics that are robust for, don't hit stuff and things like this, and then you have a lot of. physical world understanding that you're being, that you're developing. Actually, one thing before we go on to the business side, tell me more about how to generalize for other tasks.

Like how do you imagine this mowing data teaches us some sort of physics or navigation or whatever it is that we might have, and how do we extend that to snow plowing? And how do we extend that to picking apples, eventually. Like, how does that go? And whoever, whoever wants to jump in.

## Generalizing learnings for other tasks, like snowplowing

[00:58:31] **Nag Murty:** It's Mike.

[00:58:33] **Michael Laskey:** Okay.

Yeah. So, okay, let's think about like snow plowing, for example. It's very similar to push mowing, right? You have the understanding of like, what can you can, what can you move your, you know, plow is basically like a blade, but it's now kind of vertical. what can you move that over versus not? So there, the idea is like deep awareness of collision avoidance.

So like understanding like small obstacles, manhole covers. All of that comes into play. then there's localization. You obviously are trying to lay down stripes efficiently. All of that also comes into play. and then there's the semantics of like, where is snow versus not. and that is very similar to like, where is there like, mowable grass versus not.

Snowpine, I think there's some nuances there that's gonna refine the model because you have significant occlusions, right? You're gonna have to have this, like, somewhat of a prior in some spaces or be able to detect, like, the edge of boundaries. Very hard. Yeah. Yeah, I think that's gonna be one of the key challenges, but when you look at how humans do it, it's very possible that with the central stack we have, these could be done.

So we feel like the intelligence is capable of doing this. We just have to like test, refine, and build. and then if you want to get into, you know, like more dexterous things, like let's say apple picking. A lot of it is just like geometric motion planning, semantic awareness, understanding, like, how do you move your arm in a free space?

But then there's also the contact physics, right? Like, knowing, like, how to grasp something and pull it. I'm pretty hopeful because, you know, like, coming from, UC Berkeley, one of the papers I worked on was, like, the DexNet project, where we used simulation to learn grasping. so you definitely see there's already like huge amounts of research pointing that simulation can learn contact physics to a pretty reliable degree.

so I don't think that's impossible for like our world model to produce.

[01:00:31] **Nag Murty:** Yeah, I think we... No, just one more thing, right? Like a lot of this needs to be evaluated also from a product lens. I think this is where, you know, the question is like, what is, what is the true, like, you care about generalization. Sure. But like across what dimension, right? wait, did we lose Mike?

So, you know, the, the one thing I was sort of, you know, going back to was this notion of. Like, how do you, like this, like, as we build this kernel, right? Like you, it's, it's already pretty generalizable to a lot of surface coverage, even without going to be, without going to something as complicated as snow.

So you take things like weed treatment, right? Or like fertilizer application on a lawn. Like that's like exactly the same motion on like turf. That's something we're able to do right away today. Right, so that's a task that you get paid for, it's a very high margin task. A lot of interesting angles there.

[01:01:36] **Audrow Nash:** So you're saying you'll be pulled by different markets as they are, like you'll basically evaluate which ones are the good things to go into, in addition to which ones you're well suited for. So it's a pragmatic choice, basically.

[01:01:49] **Nag Murty:** Yeah, it's always a pragmatic choice. And you know, it's, it's, these are the things that we do today, right, as part of our existing business.

We're already collecting data ahead for some of these other tasks. That we need to do right with the view. And what's also interesting is like the, this 3d point cloud that Mike talked about, it's already generalizable to things like, you know, trimming and blowing. which are, which are sort of very different tasks than pure surface coverage.

But this point cloud is already able to predict, you know, sort of the attributes. You can still use it. Correct. So, and all together, these sort of more than add up to like 30 to 40 cents on the dollar of revenue. So if you're making like a dollar of revenue in landscaping, all these activities, right, mowing, blowing, trimming, and then weed application or weed treatment application, they will total up to more than.

I'd say at least like 40 cents of like labor cost when it comes to your own business. So now you're effectively talking about sort of 40 cents of automation impact with just You know, with basically the model that we already have today. Do we want to go into snow? Yes. You know, should we, like, we could probably go IPO and not even touch snow.

Right. Like that, that's the way to think about it. And again, like it goes back to the philosophy of like, what should drive a robotics company, right? It has to be like, you know, can you like get a margin out of this? And if you can't like, you know, that's research and that's not engineering. Really don't want to go there.

[01:03:28] **Audrow Nash:** That's a great way to put it. Let's see,

uh, so Mike,

going back a little bit, so you're mentioning all these tasks and you kind of broke down mowing into four different components earlier. So is it like each of these components is a different model that you're kind of putting together in a smart way?

Or is it, are they all connected in some way? Are they all implicitly handled as like constraints and whatever you're doing to solve? For your current policy or how, how do they fit when you have these four modes and you add a different additional modes when you go to wheat or you go to snow or whatever it is, how do these all sit together, these different capabilities?

## AI architecture

[01:04:12] **Michael Laskey:** Yeah, so on the robot, there's one single neural network that's producing all these things. so it's just like a single, that's why it's kind of like a, like a, you know, like a transformer. But, I'm not going to read too much about the architecture. It is heavily optimized for embedded devices. So it's not just like, it's not like a completely like fat GPT.

Obviously, there's no 70 billion weights on a Jetson. but it is a single model that can produce all these joy presentations. and I think as we scale, so right now we are very inclined to say, like, let's produce, like, human interpretable representations that a robotics engineer could use and maybe, like, code heuristics on top of.

I want to get away from that, but in a pragmatic way, to the point where you do have much more, like, learned representations that just feed directly into a learned pattern and execute tasks.

[01:05:08] **Audrow Nash:** Why do you want to get away from that? Cause to me, it's like, making the black box bigger, which. Do you think it'll be significant performance gains or you just want things opaque so I can't understand anything or what's that?

[01:05:26] **Michael Laskey:** I think the more, the more you apply learning, the more interesting, like, feedback. Well, okay, so if you're an end to end system, one thing that's very interesting is like your feedback becomes really easy, right? Because if you make a mistake and you, like, crash your robot, Then all you have to do is say, hey, on that action, you shouldn't have done that.

There's no human labeling. There's no sense of like fine tuning on some sort of like weird point cloud. You can literally just scale these models and then like they will Observe data. So the scalability becomes way higher, in a way, if that makes sense.

[01:06:05] **Audrow Nash:** Ah, yeah, because you are not labeling things. And because you're not labeling things, you're not limited by, like, people labeling things with efficient software for labeling things.

Like all the, that difficulty.

[01:06:18] **Michael Laskey:** So we don't have, because we find, SIEM, our labeling pipelines are just in house, very small. We don't have more than, like, you know, a very small R&amp; D labeling. But the more you can unlock true unsupervised learning or like reinforcement learning, the more interesting it becomes at digesting data.

[01:06:37] **Audrow Nash:** Yep. Yeah. And so you're using simple heuristics like you bump it, it's not good.

[01:06:45] **Michael Laskey:** Exactly. You bump it, your point cloud is bad. what we're definitely starting to add to our model is like action heads that would synthesize things and then be able to like say, so basically through, you can learn representations through data, but you don't necessarily have those override the like point cloud.

But through fine tuning, they could adjust things. the bumping into things is actually not a problem. So I don't want to give that impression. a wide problem. I would say the main problem right now is like, it's actually, let's see, what's the biggest problem? It's probably just laying down these, like, perfect lines for landscapers.

Like, no, like, perfect non zero overlaps, no matter how a human does. I would say that's one of the more, like, core technical challenges in mowing. to do it with, like, almost zero overlap is actually really interesting.

## Training to mow straight lines

[01:07:41] **Audrow Nash:** So, to train your system to do that, do you look at the result and kind of evaluate it?

Or is there some way for you to avoid manual labeling? so that you can train this, or how do you approach that?

[01:08:00] **Michael Laskey:** Yeah, I mean, that's what we're, it's actually pretty tricky, because

This is an open problem at the moment. Yeah, so like, we train heavily in SIEM on like, where you have ground truth, right?

These kind of performances. and then it's really like, what's, cause yeah, you could have people kind of like, dictate and say like, this line was bad. how do we like, get that in a more unsupervised way? I think it's kind of open. the ROAS today lays like pretty clean, straight lines, but periodically it could mess up, and that's I think the last challenge of pushmilling.

[01:08:32] **Nag Murty:** This is actually a really interesting question again, right? Which sort of, which goes back to the whole product technology debate, right? when you sell it to landscapers, right? They will like go on and on about sort of, you know, perfect, precise lines. And, you know, and then you talk to the property owners or the property managers, they just don't care.

Right. So now the question is like, whose problem should you try and solve for at the end of the day? Right. And there's a level of engineering, right? Yeah, exactly. But there's a level of engineering pride to get like these really straight lines. Great and the research team or in research time should pursue all that.

They can high five and everything. Yeah, right But it's not needed and the other thing is, you know, okay So what like if you miss a couple of stripes You can always swarm the damn thing right like oh like build a bit bunch of redundancy into like how you cover You know the the ground and be done with it At the end of the day.

[01:09:31] **Audrow Nash:** Yeah, it is it is so funny because we can fixate on those Things that are now performance measures like did you get perfect straight lines? There's some mowing guy who's like the best mower get impressed by how it does it or is the customer like yeah, here's money Like I'm happy with what you did this kind of thing But

[01:09:49] **Michael Laskey:** here's the thing right I feel like

[01:10:00] **Nag Murty:** That's what makes for like robotics. It's such fascinating field, right? Because you have this interplay of operational pride with like business or product pride and engineering pride. You don't want like all of them to converge, right? Like, I mean, you want, you want to converge them, but you don't want them to lose their independence and lose their voice.

Because then you have like, you know, three shitty sort of like, you know, endeavors all converging versus three perfectionists who will sort of vote for their, you know, thing to happen. But there's always be consensus that forms, you know, at the end of the day.

[01:10:37] **Audrow Nash:** And if you put the legs super close together, they fall.

[01:10:41] **Nag Murty:** Exactly. That's a great analogy. Yeah. That's what I'm imagining as you're speaking. That's such a great analogy right there. No, it's a really nice way to put it.

[01:10:50] **Audrow Nash:** Yeah. And it's, I really like, I feel like each of you, so Mike, Nag, and then you're, you're, like operations founder. I feel like you guys are probably the great three legs voting for your different perspectives.

[01:11:05] **Nag Murty:** That's pretty much how it works. Yep, exactly.

[01:11:08] **Audrow Nash:** Oh yeah. Let's see. So that sounds really cool. the simulation side is, I mean, we're just, the approach is very, very cool. one thing that I wanted to make sure we got to talk about, because Nag, when we talked earlier, there were many interesting things brought up.

And so, one thing that I would love to hear your perspective on again is... robot as a service model and why you don't like it.

## Why not Robot-as-a-Service?

[01:11:40] **Nag Murty:** yeah, I think like, it's not that we don't like it. I think it's just lazy pattern matching by a bunch of software VCs, you know, who act to like justify opportunity costs to their LPs who ended up saying, you know, I'll change one letter and we'll call it RAS.

As opposed to SAS. Instead of SAS. Yeah. Yeah. And they all high fived each other. that's, that's, that's basically what happened. it is, it is a model that you do want to get to in the limit, right? Like when, when you're, when you've built like this sort of common sense robot that can like navigate the world, right?

It really understands what the world is. It's kind of like OpenAI didn't like start by like licensing chat GPT, like from day one, right? They took a bunch of time to develop it to the point where it was like, you could put an API call to it and you know, you could make some use out of it. I think robotics, if you start enforcing like a RAS like approach.

What that leads to is you're forced to make a lot of classical choices when it comes to your stack. And it's clear that the future is not classical. Like, we should take it as an article of faith that, you know, I'm not saying everybody should, we've taken it as an article of faith. That the future is in classical.

So if you buy that piece, right, exactly. So if you buy that argument, then you have to sort of say, okay, fine. What, like, why would you want to like go with RAS knowing that, you know, a few years from now, like a fully ML based system is going to blow everything out of the water.

[01:13:18] **Audrow Nash:** Yeah. The thing that struck me when we talked earlier about this perspective was the alternative was.

Just have the robot do the job and charge for the job like it's any other job. So like, if I want my lawn cut, I don't care that it's robots or people cutting it, I just want my damn lawn cut. And if that's the case, what you can do is you can charge the exact way that the customer was taking it before.

It's on a job by job basis, not a subscription. And like a big benefit of that was it's easier for the customer. And they can try you out without big commitments where it's a robot as a service It's often a big upfront payment or probably is sometimes and then it's the subscription cost where you say I'm gonna do six months at least And pay you several thousand dollars for supporting the robot and this kind of thing, which is a lot more friction to adoption for this kind of thing.

[01:14:18] **Nag Murty:** Yeah, I think we're going like even more extreme than that, right? We're basically saying, you know, buy a company that provides the service. And, you know, all like, we're not even saying by job, we're saying by business, right? Like, it's just, it's like, take the extreme, like, like argument, it's sort of, ridiculous extremes, right?

Like, okay, classical, take it to the ridiculous extreme of like all ML, and then take the business model and say, take RAS and take it to the extreme of saying, just get paid for the service. right. and it's, yeah, I think both of them sort of work well together. And the reason why we're doing this, again, I don't think, I want to say that, you know, it's not true that we'll never sell a robot to a landscaper, right?

Like, maybe that'll happen, you know, when we're like a couple billion in revenue, right? 10 years from now, we have like the best model out there with the deepest moats, then we'll basically happily sort of destroy the competition, right? Like that, that's. Not a problem, right? But step one is to build that mode and like build it as deep and as wide as you can, right?

with the data because Machine learning again, like it's like to the to the person with the model goes the spoils Like every everyone else is going to build a wrapper around chat GPT, right? But OpenAI is gonna, OpenAI is gonna eat everybody's lunch Like it's, you know, like they, they started to eat Midjourney's lunch with like, you know, Dolly 3 and like, this is going to like take, and like, you look at what happened to Jasper and like some of these other sort of wrappers that were built on OpenAI.

They don't stand a chance, right?

[01:16:06] **Audrow Nash:** Yeah, because they're not, they're not doing the thing. They're just using the thing. And so they can, I feel like Apple does this too. Where it's like, oh, they let everyone make a notes taping app and then they make the best, not that their notes app is that great, it's okay.

But they keep folding things in that other people were doing, except for that this thing. Let's see. I'm on

There it is everything that, that one I could have lived without, but maybe not, never know But, so yeah, so you're doing the thing versus, you're creating rather than just wrapping something else you're going heavily in the Direction of, and you're, you're building that moat by getting out there, by doing the model that's easiest for customers for this kind of thing.

And you're also just by buying businesses. Like that is a very cool step. Cause I've heard of like boring businesses and this kind of thing where you can buy, I don't know, a landscaping company and then you add some technology. And what you guys are doing is you're literally doing that, where you buy a landscaping company, and then you augment them.

With your robot platforms, making them even more efficient and even better, able to do their tasks.

## Boring businesses + robots + AI

[01:17:29] **Nag Murty:** Exactly. That's the goal. again, though the, you know, the value of the company. So if you think about like when you buy a landscaping business, right. You're sort of valuing it on like an EBITDA multiple, right?

So you're buying it for sort of X times its earnings. but then like to us, the value of the company is not just like what we buy it for in terms of its earnings. It's the data and you're buying essentially the services of all the operators who can perform reinforcement learning for you on the ground.

What a clever model. That's the crux of the whole thing. And again, this is all driven by like this sort of, it's an article of faith that machine learning will eat everything, you know, going forward.

[01:18:14] **Audrow Nash:** I wonder, I mean, it seems like it probably will to me that just like all the advances we've been seeing.

And I mean, like even, so you look at like perception and now the way everyone does it, it was classical when I started robotics and now it's all. Learned like it's all perception that's running through AI, which is totally nuts And then you get a pose estimation or whatever it is out of it, and they're they're all learned

[01:18:44] **Nag Murty:** You know, what's also interesting is like this is it's not it's not like it's not like like we discovered this religion You know in isolation, right?

It's because we tried a bunch of other approaches and we tried to scale hard with those approaches, right? Like I built like the first Like GPS based more in my garage, right? Like I built it on like a, like a drone audio pilot stack. I learned like, like literally, right. And we got our first, like, you know.

A couple hundred thousand dollar contract on the basis of like this rickety thing that I'd built in my garage. It was crazy, right? And we're deeply sort of aware of the pain, painful sort of aspects of these classical systems, whether you're talking about GPS. Then we found lidars and we're like, okay, this is amazing, right?

You can map the whole world, you can teach a path, but then you start deploying those and you realize how brittle that approach is because the environment is changing all the time. Right? Unless you have semantic awareness, you don't have any hope of solving. Like a robotic problem in the unstructured outdoors to the level of reliability where it can actually, you know, generate like significant value unlock.

and then what's interesting about machine learning is that you can get to an 80 percent good solution pretty quickly. So it's, it's not like a moonshot bet where you, you have to wait for it to become a hundred percent. So these approaches, our mowers today are generating value, right? They're fully like, they're all ML, but they're generating value.

And so that allows us to sort of plow back that value back into the business, right? So you're not trying to like take a deep hit on the cost. In any case, when it comes to this.

[01:20:29] **Audrow Nash:** Yeah. Cause you're staying profitable. Like you're just, you're buying a business, you are scaling and getting more data and maybe getting investment, but it's on your terms cause you're profitable.

and it just, it seems like a really good way to proceed to me. Like the whole thing of, cause one thing I really have, I've seen so many companies like, so I've been podcasting for, I think it's almost 10 years now, which is nuts. So I've talked to a ton of companies for this. So Sense Think Act, but then RoboHub before that.

and so I've talked to, and the whole time I was interested in startups and, I've talked to so many companies and a lot of them are out of business, which is nuts. and a big reason that that. Seems to occur is they take on a bunch of investment and then they go and try to find a market or something like this.

Maybe they found one, but then they are forced to become profitable or they're forced to try to cash in so that the venture capitalists can cash out on some timeline. And a big way to fight against that in a sense, like you want investment to scale and you want it for the connections and things like this.

So it's not all bad. but by having revenue by having kind of like a very good long plan, you put yourself in a much better position. To accept investment on your terms and by buying profitable businesses that are already profitable And then just making them a little more efficient like that that to me seems like everything is going to be on your terms

[01:22:12] **Nag Murty:** Exactly on your timeline your terms and you know, not everyone can raise like A billion dollars in charity investment like OpenAI did, right?

Like, we've got to figure out, like, They're all for profit, though, I think. I don't know exactly about their situation. Well, yeah, they pulled a for benefit thing. But what's interesting also is that, you know, OpenAI could, like, scrape the web and get all the language data that they could. Now they can watch YouTube and they can build multimodal LLMs, right?

But where are you going to get the data to build robots? Yeah, it doesn't exist. And sure, Google and DeepMind and all these guys can, you know, like rally together and like collaborate to like, you know, build this massive dataset. But it's not enough to build a dataset. You need to have like boots on the ground to do that sort of reinforcement learning and provide the feedback.

So, without a boots on the ground approach, there's no hope in hell to build outdoor robotics at scale.

[01:23:09] **Audrow Nash:** And especially if you're not in Google or whatever, some huge company that can fund all this. Like, if you want to do it as an individual, you need to probably do this approach. I'm sure you've thought about this quite a lot, um, and this seems like the way to scale.

You have to bootstrap.

[01:23:27] **Nag Murty:** Yeah, it's the way to fund yourself and, you know, and honestly, there's another angle to this, which is you end up building something, like robotics is a workflow optimization problem and it's a people plus machine optimization problem and the only way you can solve this is by sort of injecting robots and trying to inject robots in many different ways into an existing operation, right?

Because it's hard to sort of just say, here's the perfect machine, I'll drop it in and like, boom, like, you know, everybody's like high fiving each other. That doesn't happen. Yeah. You know, it's very hard. and so it's almost like you're, you've sort of evolved this robot, like fit like a glove. into your existing operation.

And it is, the data engine is not just for ML. The data engine is also to influence all other aspects of your product. you know, and so it, it's, it's just, it's just like a rational way to do it. Yeah, exactly.

[01:24:27] **Audrow Nash:** For sure. Yeah. It's a very cool idea. So Mike, how, so going, building this data model for all sorts of things, like how, how are we doing that?

Like how we're collecting lots of data. How do you make it so things can generalize? From the mowers to the snowblowers to, or the snow pushers, whatever it is, all the things. How do you, how do you organize, how does all this data work together, I suppose, and I'm sure that's a very interesting challenge.

## How do we build the data model?

[01:25:02] **Michael Laskey:** Yeah, I mean, so, I think we have to, the way we're kind of structuring is like, we're trying to build, like, an intuitive physical model of the world for the robot that can have, like, key concepts, like, I know where I am, I know where I've been, I understand the semantic 3D structure of the world, I understand what I can move over and what I cannot move over.

Those core concepts, they apply to all the tasks you just mentioned. so, as we, what we try to do these days is, like, you know, this year we shipped the mowing product, Next year, we're going to want to see like, okay, let's test our stack and do something like trimming or edging or blowing. We'll take the same model and then put it on a different platform and have the same, basic deployment cycle with that.

But we keep it to being trained with the same model and the same model should run on every robot. I think that's very feasible, especially because, as Nox said, a lot of these tasks are so similar that you would have to change like almost nothing to do different tasks right now. so cool. Yeah, and what's gonna get really interesting over the years is when we get into like dexterous manipulation, which is when you look at landscaping, it's almost like this goldmine of mobile manipulation outdoor unstructured environments.

Like you actually probably couldn't think of a better benchmark than landscaping because every day you have a crew like, you know, right now we have a hundred people go out and do complex manipulation in random parks, random cities all over the country, right? So, like, that's not, you're not gonna get that, like, Google, they have, like, maybe 10 people demo to the robot in a conference room.

Same conference room, same robot every day. The type of data that we're getting is very much, like, real, unstructured mobile manipulation in the wild. and doing complex tasks, like, if you ever see someone tree trim, that's insane. Like, if a humanoid was able to climb a tree and cut a branch. That would be like a huge AGI moment.

Oh my god, yeah. Yeah, so these are some of those complex tasks that you see people do daily. And we can collect and train on that data, which is really interesting.

[01:27:09] **Audrow Nash:** Huh, so for people to do these manipulation tasks and everything, are you just having your crews wear cameras? Or like, what's the, or is it just your robots are going out, is that what you mean?

But eventually, maybe you'll add more sensors around the crew, so you can get data on them?

[01:27:27] **Michael Laskey:** The number one data right now is like they bring the robots with them and deploy them every day. So we're getting that like interactive point of view perspective of the robot. as we start scaling to like dexterous, you would have to ask the question like is the robot platform we're trying to do good enough that you can just do like RL type data, like interactive feedback, or would you want to have passive data collection?

That's gonna be the challenge. But then you can also, like, you can use these people as basically ops, right? Like, every Roblox company has an ops team. Our ops team is likely the biggest ops team. Because we have, like, entire crews of people doing this work for us, right? Yeah.

[01:28:09] **Audrow Nash:** It seems a lot like what Tesla did with their self driving for everything, which is they just kind of outsourced it and then they get the benefit from millions or billions or I don't even know how much, driving data.

Billions of miles of driving data.

[01:28:25] **Nag Murty:** It's, it's what every company has done though, right? Like if you take a look at like, like Facebook and Google or whoever else who sits on all these like massive data sort of, you know, data, what a units, Which, you know, people buy to train their LLMs that was generated by users who sort of paying in kind that data for the privilege of using a Facebook or a Google or a Reddit or a Twitter, right?

So it's the same thing. Tesla's basically doing the same thing for the physical world, and we are doing the same thing for landscaping. That's super cool.

[01:29:01] **Audrow Nash:** Yeah. What a cool connection. so where, where do you guys see yourself? Where do you see yourselves going in the next like. Like, what's the future, you think, for like, I don't know, five years, ten years?

What do you think? maybe start with Mike?

## Getting into dexterous tasks

[01:29:22] **Michael Laskey:** Yeah, I mean, so I'll speak more technology wise. I think what we're wanting to get to is like, into the dexterous tasks, right? Like we've definitely, where we're at today, I feel like surface, mechanized surface coverage, is obtainable within the next couple years.

And then we really want to have hardware platforms where we could do dexterous tasks. and I think you're seeing, with hardware it's actually really interesting because you're just seeing so many prototypes come out of like hardware platforms. so you could, you might even have like some sort of commodity thing that can sort of move in a dexterous way and then apply AI to it or we build our own.

which we're very capable of. I think we have a pretty decent in house like hardware team these days. and then, we want to get to the scale though, where it is like, you know, every state we're in, every like, county we're in, and our robots are learning from every data possible. and if you look at, like, this space, it's very possible.

You have so much fragmentation in the industry, it's just waiting to be rolled up in a massive way.

## Building a monopoly

[01:30:29] **Audrow Nash:** Oh yeah, what do you think?

[01:30:32] **Nag Murty:** I think it's like in five years, it's, you know, given like our sort of acquisition pipeline and sort of the state of the industry, it's very easy to see getting to something in like the billion dollars of revenue range when it comes to rolling up this industry.

And then I think we'll have this really mature model, which we can then start to, and like these robots that are fully baked, right, for our own operations, we can start opening it up to other and like, you know, other people in the industry. But really the, would be awesome to build a monopoly. And just like, you know, just like, just take the whole industry.

Cause I mean, yeah, like, yeah, deliver the service, build your own robots. It doesn't get like more sort of, you know, a bigger moat than that. Sort of take the industry. Yeah. Yeah.

## Advice for our new world of AI

[01:31:23] **Audrow Nash:** Cause I mean, like, related to that, I would love to hear what advice you have. For people other than join your company like what what kinds of what so with this kind of new world of machine learning and robotics and Data being very valuable.

how,

how do you think someone can skill up or best position themselves or start a company like what? I know it's, it's a super broad question, but what would you think would be some of the most important things to doing well in this kind of new world? We're in, maybe you start with Nag this time.

[01:32:09] **Nag Murty:** Yeah, I'd say it really comes down to like people from different disciplines really need to talk to each other.

So if you're a roboticist, like don't talk to other roboticists, go talk to like the business folks. Right. and if you're, yeah. And vice versa, right? If you're someone in the PE space or someone in like the VCs, I don't know, they've got their own sort of, you know, their own sort of swim lanes that they swim in.

But I think robotics is going to benefit a lot from like the PE folks talking to the, through the roboticists. Again, there are reasons why it'll never happen, but I wish that like more of it would happen. How do you,

[01:32:49] **Audrow Nash:** what are some of the reasons and how can you kind of best them for this? Or like what, cause individuals can do things.

[01:32:55] **Nag Murty:** Individuals should and will talk to each other, right? Like, it's already happening, right? So you have, well, it's already happening for non robotics things is what I mean, right? Like where you have PE companies, you know, that are looking to inject like LLMs, LLM agents, you know, their operations. We use LLMs to sort of, you know, do bidding on like new job sites and things like that.

So there's, yeah, it's, it's fun how all that is shaping out. but what's, what happens with PE is typically they have, they don't know how to evaluate technical risk, private equity, like, right. It's like, I think the world today is sort of siloed into people who know how to evaluate technical risk and people who know how to evaluate financial risk, right?

Private equity is like financial risk. So they know how to take a mature business and then inject a bunch of debt into it and then blow it up to be bigger. The VC's come in and they know how to evaluate. Technical risk, right? But it's for like, for anyone who's trying to build like something similar or wants to like, you know, explore more along these lines, it just feels like there's got to be sort of a way.

Where these two models can merge for robotics to really take off because otherwise you're going to have the same sort of repeated cycle of Companies that go public through SPACs and like, you know, I don't want to name names here But they're trading on like, you know, the stock exchange and they're worth less than the cash they have on their hand Which is really weird and this is because they're massively cash, cash burning entities who are selling robotics and AV and whatnot, but they really don't have like a way to generate cash flow.

because these things are so, yeah, exactly. And, and that's why Tesla is what it is. And like, you know. Any other RAS company is what it is, at its core. And so really there needs to be like a rethinking of how you think about, like, what kind of business model robotics will need. And for people to start talking, you know, with each other to sort of.

evolve that. Because left to itself, like the pattern matching was sort of insured. Yeah, like, and it's just going to be pattern matching all the way down. And it's really not, I mean, really, yeah, like, it's not gonna lead to anything exciting. You know, you're not gonna change the world with like, you know, these same repeated ways of thinking.

It's not gonna happen.

[01:35:25] **Audrow Nash:** Yeah, for sure. How do you, so do you have any, like, great Investment thinkers or anyone's to recommend for this kind of thing? Like, I mean, I'm in technology and I know very little about private equity. I talked to a lot of people through podcasting, but, like who, who to learn more, who to become, or even like, I mean, you guys are, in my opinion, from this interview, a great example of kind of merging these two, but.

Who else can we learn from?

[01:36:00] **Nag Murty:** It's, yeah. So I think we should make a distinction to say, you know, private equity. I don't think like you can have a private equity company that merges the technology company tomorrow. Right? Like there are different fund structures and whatnot, so there's logistical challenges to do that.

But, but I think there are examples out there like of companies that are building these vertically integrated solutions like an Amazon or a Tesla. And the way they've approached building their business is what I think like we can learn to emulate. By focusing on cash flow, right? By focusing on sort of, like, by asking yourself, like, what are you getting paid for?

And like, where is the margin accruing from? And then what are the jobs to be done? And what can you truly, do you truly need to automate? And what can, what, what can you automate, right?

[01:36:46] **Audrow Nash:** Yeah. Okay. I really like that. I mean, it's just simple pragmatism in a sense.

[01:36:52] **Nag Murty:** Cashflow. Exactly. I mean, follow the cashflow, right?

Like follow the cashflow, but also like you have to aim for the moon here because again, classical methods are not going to solve it for you, but find a way to like link the two, in a way that works for your industry. It may not work for all industries, right? I think it works for landscaping. You know, we're growing, we'll find out, right, as we grow further.

we can certainly tell you how not to do things, and then hopefully, like, in another year or so, we can tell you, like, you know, how to do things really well,

so.

[01:37:24] **Audrow Nash:** Yeah, for sure. It's iteration. And, Mike, how do we keep

up with all this LLM stuff, all of the world language model, all the AI, how, how, how does one, I don't know, operate in this or skill up or?

Yeah. Yeah. Just do well in this coming world with, if machine learning is going to eat everything or everybody's lunch. How do you, how do you be a part of that?

[01:37:53] **Michael Laskey:** Yeah, I mean that's, keeping up with it is definitely a chore that you have to like, you know, by then, like, your week is reading papers. it's a very fast moving field.

I, you know, and the pure software side, I, I'm definitely not an expert in that. When I think about robotics though, like, how do you, how do you do ML in robotics? How do you actually, like, Build a career and like actually ship these products. The one lesson I've learned, and this is actually why Electrosheep is really appealing, is like it's really easy to be overestimate in timelines, or like overconfident, and saying like, yeah, tomorrow the robot will work, or like the next day the robot's gonna work.

These are very subtle problems that require a lot of iteration and feedback. So you really do want to think about like, what is the cash flow of your business? What's the runway? And what is the realistic timeline for these ML products to actually deliver value? And then plan businesses in a way that gives you the R&amp; D runway to actually like scale and ship product.

[01:38:58] **Audrow Nash:** Yeah, I really like that. So keeping the R&amp; D runway, because that's how you are differentiating yourself. But you need to keep cash flow positive so you don't have to do things on bad terms or just get bought for way less than you're worth by some company because you're in a bad moment and you ran out of runway or all these things.

What, Mike, do you have any other, like, I don't know, like, advice for learning about this or applying, learning about AI and ML or, and applying it or how do you get really good technically, I guess?

[01:39:39] **Michael Laskey:** I think for robotics, the number one thing that's really guided me is, like, put it on a physical robot and actually put it out there and see the performance.

The benchmarks, they matter, but what really matters is how's the robot's doing. because that's going to be your ultimate benchmark, like does it really work on a robot? Can you see the physical embodiment of the AI? that is your ultimate, like, North Star when it comes to shipping robotic products that actually work.

really easy to get lost in like the Twitter esque sphere of like what's hot, but when you really see it fundamentally on a robot and delivering value, I think that's when you know you've actually like done ML research in a cool way that's exciting.

[01:40:24] **Audrow Nash:** Mm hmm. Yeah, when you've actually provided value using these methods, it's awesome.

Okay, well let's see, we've gone very long. It's been a blast talking to you guys. Do you have any, links or contact info you'd like me to include with the episode?

## Links and contact info

[01:40:47] **Nag Murty:** it's just, we have a new website, right? So, shiny new website, like you should include that.

[01:40:53] **Audrow Nash:** Yes, for sure. Of course, the shiny new website will be included.

It's great.

[01:40:58] **Michael Laskey:** Yeah. Much more information. We're doing a lot of PR soon, so there'll be more stuff, but for now, just the shiny website. Yeah.

[01:41:07] **Nag Murty:** And then, my email is nag at electricsheep. company and Mike's is michael. lasky at electricsheep. company, so. Both of those, you know, we can provide you and, yeah, so that people can sort of get us, get in touch with us there.

and then, yeah, we're based in San Jose, you know, and, we keep like doing demos all over the Bay Area. So, anyone who wants to come and hang with us. We'd love to sort of, or when you're in the Bay Area, you should come and hang with us.

## Hanging out

[01:41:37] **Michael Laskey:** Yeah. You can literally just pick a park and we'll show up.

[01:41:44] **Audrow Nash:** Yeah. I'll reach out, once a quarter I'm there. So I will reach out and we'll hang out.

[01:41:49] **Nag Murty:** Yeah, absolutely.

[01:41:51] **Michael Laskey:** Where are you at? Where are you living right now?

[01:41:54] **Audrow Nash:** San Antonio, Texas. I was in San Francisco. We moved like a year and last, last June, we moved here. So I like it a lot. We don't have family or anything.

We thought it was a nice place to live.

[01:42:09] **Michael Laskey:** Oh, cool. Do you have a massive like house? Like, is it like

[01:42:13] **Audrow Nash:** relatively, we were in a, I was in a 400 square foot apartment in San Francisco. And, my mortgage is the same for a four bedroom house that has a yard and stuff. And we're in like the best part of town or one of the best parts of town.

It's bonkers. so I don't know. I like it here. And I love barbecue. I, my wife and I, we went and looked at Austin a while ago and, we had the barbecue. And we were thinking about where to live and, at some point in the meal, I was like, I'm ready to beg. I will. Like, I want to live here. I want to be close to this barbecue.

[01:42:56] **Nag Murty:** You know what's interesting? Like, Roon put out, like, the guy on Twitter, like, who, you know, who's known for sort of these takes on AI. He put out a tweet like a couple of days ago where he said, you know, the future is going to be sort of these immaculate sort of living spaces. I'm just paraphrasing. It's not the exact tweet, right?

Where it's like all these built like gorgeous outdoor and indoor living spaces for us, right? There are fractions of the cost and anyone, right? Whether or not they work in tech like is able to afford it. I was like, yeah, that is such a cool vision, right? Because Like that's the promise of robotics and that's a promise of like these AI agents that we're building, right?

Just massive improvements in standards of living for everyone at the end of the day Which should be insanely cool to make happen.

[01:43:44] **Audrow Nash:** I mean even also just like easing labor shortages and stuff in the short term Yeah,

[01:43:50] **Michael Laskey:** which also means like things become cheaper and the abundance of labor. Yeah, it just it's a whole new equation When you have infinite labor or

[01:44:00] **Audrow Nash:** I was listening to this thing on chat GPT or it was the Sam Altman interview with Joe Rogan and he he was Sam Altman was saying how if Like their goal is to make intelligence free Which is quite cool.

[01:44:16] **Nag Murty:** So then it's like all the knowledge work in a sense, becomes free, which is really interesting and robots would do that for the physical world,

[01:44:24] **Audrow Nash:** which would be quite cool. Yeah. Well, we got to get towards our utopia.

[01:44:30] **Nag Murty:** Yeah, we got to get you like permanent barbecue. Like, you know, like that's the goal.

[01:44:35] **Audrow Nash:** And if you guys come visit San Antonio, it's lovely here.

The barbecue is wonderful and there's plenty of grass to mow. Do. Sure.

[01:44:42] **Michael Laskey:** Yeah. I think it's, it's in the options of places we'll be going to, yeah.

[01:44:47] **Nag Murty:** Yeah. Hell yeah. We might be there sooner than you think, like, we're looking at a few, yeah, acquisitions in that area, so like, we'll be there sooner than you think.

Awesome.

[01:44:58] **Audrow Nash:** Yeah. Keep me posted. Okay. Hell yeah. So we'll wrap this up. great talking to you guys and I'm looking forward to following and seeing what you do more.

[01:45:08] **Nag Murty:** Likewise. Thank you so much for having us and it was a pleasure chatting with you.

[01:45:13] **Audrow Nash:** Hell yeah. All right. Bye everyone.

That's it! If you made it this far, you're either asleep or enjoyed the interview.

If you enjoyed it, consider subscribing. I'm not planning on keeping any kind of regular schedule, so subscribing or following me on X or LinkedIn is the best way to hear about new episodes. If you're asleep, I hope it was restful and that you wake up and build something. Until next time, bye everyone!
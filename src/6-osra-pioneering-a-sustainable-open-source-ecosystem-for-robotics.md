- [\[00:00:00\] Episode intro](#000000-episode-intro)
- [\[00:02:47\] Willow Garage and Open Robotics Lore](#000247-willow-garage-and-open-robotics-lore)
- [\[00:05:38\] Player and ROS lore](#000538-player-and-ros-lore)
- [\[00:09:06\] Willow Garage and the Birth of Open Robotics](#000906-willow-garage-and-the-birth-of-open-robotics)
- [\[00:13:17\] Tully and Geoff's roles in Open Robotics](#001317-tully-and-geoffs-roles-in-open-robotics)
- [\[00:22:13\] Why make ROS 2](#002213-why-make-ros-2)
- [\[00:24:39\] Player and ROS 2](#002439-player-and-ros-2)
- [\[00:25:42\] Towards a robot revolution](#002542-towards-a-robot-revolution)
- [\[00:29:16\] Gazebo for robot simulation](#002916-gazebo-for-robot-simulation)
- [\[00:34:39\] OpenRMF project at Open Rob](#003439-openrmf-project-at-open-rob)
- [\[00:38:22\] Important, but often forgotten: Open Robotics' infrastructure](#003822-important-but-often-forgotten-open-robotics-infrastructure)
- [\[00:44:42\] Open Robotics before the Intrinsic Acquisition](#004442-open-robotics-before-the-intrinsic-acquisition)
- [\[00:47:38\] Big steps for the ROS community we can take because of Intrinsic (Zenoh)](#004738-big-steps-for-the-ros-community-we-can-take-because-of-intrinsic-zenoh)
- [\[00:51:41\] Rust for robotics](#005141-rust-for-robotics)
- [\[00:53:27\] Intrinsic's acquisition of Open Robotics](#005327-intrinsics-acquisition-of-open-robotics)
- [\[00:58:31\] OSRF since the Intrinsic acquisition of OSRC](#005831-osrf-since-the-intrinsic-acquisition-of-osrc)
- [\[01:01:33\] How former OSRC folks contribute to OSRF now](#010133-how-former-osrc-folks-contribute-to-osrf-now)
- [\[01:04:28\] Announcing OSRA!](#010428-announcing-osra)
- [\[01:07:27\] Motivation for OSRA](#010727-motivation-for-osra)
- [\[01:15:20\] Merit-based contributors](#011520-merit-based-contributors)
- [\[01:18:06\] OSRA Consortium](#011806-osra-consortium)
- [\[01:20:23\] Why companies might want to join the OSRA consortium](#012023-why-companies-might-want-to-join-the-osra-consortium)
- [\[01:23:55\] OSRA membership types](#012355-osra-membership-types)
- [\[01:29:18\] Meritocratic contributors + how to mentor and get involved](#012918-meritocratic-contributors--how-to-mentor-and-get-involved)
- [\[01:32:26\] Mentorship process](#013226-mentorship-process)
- [\[01:34:25\] The value of contributing to open source software](#013425-the-value-of-contributing-to-open-source-software)
- [\[01:39:19\] OSRA's badging system for contributors](#013919-osras-badging-system-for-contributors)
- [\[01:42:52\] Educating more people to be roboticists](#014252-educating-more-people-to-be-roboticists)
- [\[01:47:26\] Robotics in the next 5 years](#014726-robotics-in-the-next-5-years)
- [\[01:52:10\] Why open source?](#015210-why-open-source)
- [\[01:55:36\] Final thoughts](#015536-final-thoughts)

## [00:00:00] Episode intro

[00:00:00] **Audrow Nash:** I'm sure you've heard about the Robot Operating System, or ROS. If you haven't, it's freely available open source software that makes it much easier to build robots. 

What you may not know is that the Robot Operating System is one of the projects maintained by Open Robotics. Other projects include the Gazebo simulator and OpenRMF. 

Open Robotics had a non profit part and a for profit part. At the end of 2022, the for profit part of Open Robotics was bought by Intrinsic AI, and we've been maintaining and investing in Open Robotics projects from Intrinsic, which you'll hear about more in this interview. 

I say we because I was at Open Robotics as a software engineer and I came over to Intrinsic with the acquisition. 

Anyways, it's been a little over a year since the acquisition and now the non profit part of Open Robotics is announcing a new governance structure called the Open Source Robotics Alliance, or OSRA, which is the main focus of this interview.

From my perspective, this is a great move for Open Robotics' projects and follow successful open source software projects like those of the Linux Foundation. I also think it will be better for companies that rely heavily on any of Open Robotics' projects.

And I believe it will be better for contributors to the community as OSRA formalizes the mentorship process and has a way for contributors to have their voices heard. 

Also, a shout out to OSRA's founding sponsors. 

At the Platinum level, we have Intrinsic, NVIDIA, and Qualcomm; at Gold, Apex, and Zetascale; at Silver, Clearpath, Ekumen, eProsima, and Picnic.

And then Silicon Valley Robotics is an associate, and Canonical, and Open Navigation as supporting organizations. 

I think you'll like this interview if you're interested in the Open Robotics and Willow Garage lore, want to learn more about the Open Robotics projects after the Intrinsic Acquisition, or want to be part of the next stage of development for the Robot Operating System or any of Open Robotics' other projects.

I've included a link to learn more about OSRA in the description, and with that, I hope you enjoy the interview.

​

[00:02:27] **Audrow Nash:** Tully, would you introduce yourself?

[00:02:31] **Tully Foote:** Hi, I'm Tully Foote, the community advisor to OSRF and open source lead at Intrinsic.

[00:02:38] **Audrow Nash:** Awesome. And Geoff.

[00:02:40] **Geoff Biggs:** Hi, I'm Geoff Biggs. I am the CTO of the Open Source Robotics Foundation, otherwise known as Open Robotics.


## [00:02:47] Willow Garage and Open Robotics Lore 

[00:02:47] **Audrow Nash:** Awesome, and so I would like to go. Back to the beginning and talk about Open Robotics beginning and starting with Willow Garage. So Tully, would you start with telling me about Willow Garage?

[00:03:02] **Tully Foote:** Yeah, Willow Garage was a research, a robotics research company in Menlo Park. I joined it right out of school and it was really a great experience, a lot of what we were driven for was mission and impact. And through that, we started the ROS project, or at Willow, we started the ROS project in collaboration with Stanford and several other partners and universities.

And it was a great time. We were able to go out and build the infrastructure that we thought was the most important to be able to bring robotics to the greater community, in particular, leveraging the open source ethos. To help with sharing and communicate, building a community around the world.

[00:03:49] **Audrow Nash:** Hell yeah. And what was it just to make it a bit more tangible? It was centered around a PR2 robot. That large robot with arms and the kind of really iconic, I don't know, depth camera on the top or stereo.

So it was centered around the PR2 and

[00:04:08] **Tully Foote:** Yeah. So the PR2 was our main platform. We were really focused on having impact in the robotics research community. And we wanted to have a common platform for research, researchers around the world in 

robotics. And so we built the PR2 and were able to distribute it around the world. And with the PR2, we also built ROS to be the software that people could collaborate with.

Because one of the things is, if we give you both robots and you run different software, it's very hard to collaborate. but by providing an open source, reference design for the PR2 that everyone could pick up and build, we actually had people that received PR2s, they've been practicing in simulation using the open source software.

They extended it with their research and were able to have publishable research. The week they received their robot, which was very different than the state of the art prior to that. Or each major research institution had their own bespoke framework for doing their integration tasks. And if you wanted to reuse or try to reproduce the results of another university, you generally had to re implement their full algorithm and try it out.

[00:05:23] **Audrow Nash:** And what timeframe was this? Like about when was Willow Garage active?

[00:05:30] **Tully Foote:** Willow Garage was active from late 2007 until about 2013.

[00:05:38] **Audrow Nash:** Awesome. 


## [00:05:38] Player and ROS lore

[00:05:38] **Audrow Nash:** And Tully, you've mentioned ROS, which is the robot operating system, but Geoff, you were involved with Player at the very beginning, so tell me. What Player was and then how that turned into ROS and how you came in to be involved too.

[00:05:54] **Geoff Biggs:** I will try to be brief. It's a long history. if you go right back to 1999, back then every robot had its own software from the maker and they had very fixed ideas about how their robot should be used. and It was pretty difficult, people trying to share code and so on. and then a bunch of guys at USC Southern California, I think it was, one of them was named, Brian Gerkey, who you may have heard of.

he, they came up with this idea for a simulator, and then on top of that, they built this thing called Player, which allowed you to basically write software for your robot. And share it with other people, and they thought, hey, this is pretty cool, let's open source it and see what happens. And they did, and it exploded.

the whole world started using it. There was a point in about 2003, 2004, if you went to a conference and said you weren't using Player, people would look at you like you were stupid. it was, like ROS is now, back then, and this is 20 years ago now, it's amazing to think about, I myself, during my PhD, back in about 2003 and 4, and one of my lab mates, we were looking for new software for our robot, because the existing software was pretty awful, and we came across Player, and we tried it out, and it was pretty cool, but it had some problems, it couldn't handle shifting sensor frames, which was a bit annoying.

And so we decided, oh, we'll fix that. And as part of fixing it, we, particularly my lab mate, a guy called Toby Collett, he pretty much rewrote the entirety of Player. And we sent it into Brian and said, hey, we've made it better and fixed all these problems. You guys are awesome. You can be developers now.

So we ended up being developers on Player. And so we ended up contributing to Player for a few years. Which was pretty cool. And that's how I got to know Brian. And, a few years later, Brian sent me an email saying, Hey, I'm starting this new company, Willow Garage, and we're making this thing called ROS.

It's going to be pretty awesome.

[00:07:51] **Audrow Nash:** Hell yeah. And just, how would you describe, so for those who are not familiar with ROS, Geoff, what was Player and like what task did it accomplish that made

[00:08:03] **Geoff Biggs:** It was Player was Yeah, Player was It was like an early Iteration of ROS in some respects. So ROS is very distributed. Every single, node is its own process usually, right? When ROS is yours, you can compose it now. Player, all of those are what we call drivers, and they were all loaded into the Player server.

So they're all built into one binary and you had a configuration file that said what drivers to load and so on and they talked by drivers would publish information and they could subscribe to information so it had a predecessor to topics. I mean it's similar concepts in terms of publish and describe but different way of achieving it and so if you had these you have player clients which you set on your desktop or on another robot or whatever and player servers which ran on the robot to control all the hardware based on the commands they received.

[00:08:53] **Audrow Nash:** Gotcha. Yeah, it's so cool to see how we're making, the evolution of software to become more and more reusable so people don't have to keep reinventing the wheel. Just awesome. 


## [00:09:06] Willow Garage and the Birth of Open Robotics

[00:09:06] **Audrow Nash:** And then, back to Tully. Okay, so Willow Garage is operating. How does Willow Garage turn into Open Robotics?

[00:09:17] **Tully Foote:** Yeah, so we, at Willow Garage, we spent a lot of time, we were able to, build ROS up, build the community, but there were a lot of people that were rightfully a little bit worried about, what Willow Garage's intentions were. it's a for profit company and we were building out, we were doing open source work and proving a very good track record and building community and getting people working with us.

but what we wanted to do was make sure that there was a, community steward that could be a little bit more independent than Willow Garage. Willow Garage was a building the PR2, looking at other products. there were seven different companies that spun out of Willow Garage. And of those, one of the ones we created was the Open Source Robotics Foundation.

And this is, was set up to be the hub and steward of the community as a non profit, such that everyone know that this is going to be a neutral party. That's there, and specifically focused on the mission of promoting open source software and robotics.

[00:10:24] **Audrow Nash:** And why is it important to have a steward? what's, why, was this a risk to companies who might consider using it? Or like, why, does the community need a steward? What, is the role?

[00:10:40] **Tully Foote:** The steward is not necessary. There are a lot of good open source projects that are maintained and operated by, for profit entities. But the neutral steward helps facilitate the community building. One of the things you could potentially worry about would be if, the project is controlled by a for profit entity, they can drive it directly in the direction that they want.

For their purposes, which might be, competing with you. So if you consider you're contributing to this project that somebody, some other company that is potentially a direct competitor controls, you might be worried about whether or not your support of the project is actually helping them more than it's helping you.

[00:11:23] **Audrow Nash:** Okay.

[00:11:23] **Geoff Biggs:** If I can

[00:11:24] **Audrow Nash:** would also think, oh yeah, go ahead.

[00:11:26] **Geoff Biggs:** there is also, something I've learned in the past year. I never thought about it much before that, but there's also the, the legal IP protection as well is actually surprisingly important for companies, like logos and trademarks and all that sort of stuff. Companies care about that apparently, so we have to protect that and it's better to have that done by a neutral steward.

Then by one company they might suddenly design licensing fees or something like that.

[00:11:53] **Audrow Nash:** Oh, okay. So there's all that. And then, the perspective of being maintainers and developers of the code, so OSRF, now that was the nonprofit arm. When did OSRC come to be? I don't, know, maybe Tully, do you think?

[00:12:15] **Tully Foote:** Yeah.

[00:12:16] **Audrow Nash:** profit side of Open Robotics.

[00:12:18] **Tully Foote:** the way that OSRF operated was that it did consulting services for companies to pay for the staff. And in the overhead, we also did the open source maintenance. This is a familiar model for many open source projects. I think that the best analogy for this is Mozilla Corporation did a very similar thing.

It started off as a non profit. but then your non profit status can be threatened by, if you're taking too much contracting consulting work, which could be considered work for not the benefit of the public, but the benefit of a specific company or individual. And so the consulting arm was, spun out into a separate company.

Where the contracts went through and that's where all the staffers were employed.

[00:13:13] **Audrow Nash:** Awesome. Okay. So that's very clear. So what were you guys? 


## [00:13:17] Tully and Geoff's roles in Open Robotics

[00:13:17] **Audrow Nash:** So you, Tully, you joined right out of school. Geoff, you came along at Brian's invitation. What were you guys involved with at Open Robotics? What was your trajectory of roles? Maybe start with Geoff.

[00:13:33] **Geoff Biggs:** Mine's actually a bit different from Tully's, so I, I didn't join Willow Garage at all, and I didn't actually join Open Robotics until 2020, I think.

It was halfway through the pandemic. Yeah. so Brian invited me right back at the beginning, but at that point I was doing a postdoc in Japan and quite enjoying myself.

I felt like I want to really, I literally just started the postdoc three months earlier and I felt I want to give this a go for a couple of years. and then, the offer was, Brian said the offer's always open. and I was working as a researcher in Japan. I thought I was quite happy, and then, I found a reason not to leave Japan because, I got a girlfriend and then got married.

so that kind of kept me glued here for a while, and then after a while I got sick of how the research world of robotics was going, just a bit too much pointless papers, I felt, rather than doing actual real world impacts, and I wanted to be more involved in what I saw is like basically the robot revolution that was starting to happen mostly thanks to ROS, you know That was something I want to be more involved in and so I got an offer from a startup in Japan And I went to join that And then after about a year and a half of that, I figured that you know This is not quite what I want to be doing.

It was too focused on one specific thing So I called Brian up and asked him if the offer was still open. He said yeah, and now we do remote as well And so I ended up working for Open Robotics Remote from Japan. Yeah, and then just before the acquisition happened, I was called up and said, hey, this is happening But we want you to go to the foundation and help build it up to be much stronger for the community It's a winding path really Yeah,

[00:15:21] **Audrow Nash:** Yeah. And we'll be talking about the acquisition lots in the future. So that's a teaser for what's coming. but so Tully, tell me about your path. Cause you've been involved right from the beginning, I think.

[00:15:33] **Tully Foote:** Yeah, I, was involved with ROS before ROS had a name or the current code base. We had early prototypes early on. Indeed, we started off in subversion and part of our messaging early on is that like we were going to be a proper open source project and do it on SourceForge, if you remember that from way back in the day. We were there for quite a while at Willow Garage doing all our early prototypes.

[00:16:02] **Geoff Biggs:** if you look on SourceForge for I think it's a personal robot something or other, you'll probably find the old project still sitting there.

[00:16:29] **Tully Foote:** and once we started getting hey, we think this is the right one, I was asked to Build the first test library where we would be able to, validate that ROS seemed to work as a structure and that somebody could build a library on top of it and from my history in the car space and keeping track of localization and everything, transforms are always the biggest challenge.

And so what I did was I wrote the transform library as a proof of concept that we can have a library. That could let be leveraged the power of ROS in a distributed system. And

[00:17:08] **Audrow Nash:** So you wrote the original TF library?

[00:17:11] **Tully Foote:** Yeah.

[00:17:12] **Audrow Nash:** It's awesome. feel 

[00:17:13] **Tully Foote:** so from there I, sorry, go

[00:17:15] **Audrow Nash:** I've been involved in Open Robotics and now Intrinsic for a few years, but, and obviously like I've worked very closely with Tully, and Geoff, we bump into each other pretty often too, but it's so cool to hear your, both of your paths.

cause I didn't know a lot of this about you Tully. sorry to interrupt it, but keep going. It's just so cool.

[00:17:39] **Tully Foote:** Yeah. so I started off there writing the libraries, continued working, did more, started, got into more release management, did some management, wore lots of hats at Open Robotics. Yeah.

[00:17:52] **Audrow Nash:** one thing that'd be an interesting dimension is like the hat you were wearing and roughly the number of people that were involved, at Open Robotics, like So when you started getting into releases, was it 10 people, 15, 20, who knows?

[00:18:09] **Tully Foote:** Oh, like the release management started off back at, Willow Garage. I was the ROS release manager. I think my first one was Groovy

[00:18:21] **Audrow Nash:** what'd you say,

[00:18:22] **Tully Foote:** we

[00:18:22] **Geoff Biggs:** Willow Garage had about 60 full time engineers as I recall.

[00:18:27] **Tully Foote:** yeah,

[00:18:28] **Audrow Nash:** Did they all?

[00:18:29] **Geoff Biggs:** quite a big team.

[00:18:30] **Tully Foote:** about 60 full time engineers and about 40 peak contractors and interns in the building at any given time. So it was about a hundred people.

[00:18:36] **Audrow Nash:** fun.

[00:18:37] **Geoff Biggs:** Plus the chef. Don't forget the chef.

[00:18:41] **Audrow Nash:** yeah, I

[00:18:42] **Geoff Biggs:** a full time chef on staff at Willow Garage.

[00:18:45] **Audrow Nash:** oh, a chef. Oh man. I wish

[00:18:48] **Geoff Biggs:** food. It was really good food.

[00:18:50] **Audrow Nash:** I missed this. I, I was a little too late in everything and I missed the great Willow Garage Days. so now I get to hear about them through these interviews nonstop. but it sounds amazing. And there was a chef. That's great. okay. Sixty people at Willow Garage, roughly, plus a bunch of interns and things like this.

And then how many people came to, Open Robotics with Brian, when this, so Tully, I assume you were there. Was it just a handful or was it a large part of the group or how would, how'd

[00:19:25] **Tully Foote:** it started moderately small. So I think just for clarification though, the ROS team at Willow Garage specifically was only about six or seven people. They're a large fraction of Willow Garage was actually really focused on the research side and building out a lot more of the high level tools, high level research, PR2 specific things.

but the foundation got started with. It's first contract was with DARPA to support the DARPA Robotics Challenge and the team started

[00:19:58] **Audrow Nash:** vehicle one. Correct.

[00:20:00] **Tully Foote:** this is the humanoid walking one.

[00:20:02] **Audrow Nash:** Oh, the humanoid walking one. Okay.

[00:20:03] **Geoff Biggs:** Yeah, this is after Fukushima, and so DARPA had a big thing about humanizing for disaster

[00:20:11] **Tully Foote:** that was the main project that kicked off the foundation and it actually started as, just Gazebo. The ROS team was originally, stayed at Willow Garage. 

a little bit later, the foundation got funding and three of us transitioned over. myself, Dirk Thomas and William Woodall.

[00:20:31] **Audrow Nash:** Okay, so cool to hear about this, because yeah, Dirk and William, so cool to see that they've been contributing like the whole time

[00:20:41] **Tully Foote:** Yep.

[00:20:42] **Audrow Nash:** Okay, so you got some initial funding, a few people came over, you, Dirk and William, and I suppose it was Brian already, so it was, like roughly you four, maybe a couple other folks?

[00:20:54] **Tully Foote:** I think at that time the gazebo team was about six or seven already. they started building up to support the robotics challenge. so as we came in as like a smaller portion of a slightly bigger organization, but total, like 10

[00:21:14] **Audrow Nash:** You were helping actively with the development of ROS, and then you wrote the TF library, so proving that you could build libraries on top of it, and then, how do we, so then, how many years went by? How many years was Open Robotics, 

or I guess, how many years was, did it have the commercial component of it? Cause clearly OSRF is still going.

[00:21:44] **Tully Foote:** Yeah. the foundation got started in 2012. It's still going. I can't say off the top of my head when OSRC got incorporated and we restructured, I want to say that was only,

[00:21:58] **Geoff Biggs:** 2013, I think. I remember Brian telling me about it at ICRA in Anchorage, which I'm pretty sure it was 2013.

[00:22:08] **Audrow Nash:** Cool.

[00:22:09] **Geoff Biggs:** Yeah. It was a while. it was around for quite a while.


## [00:22:13] Why make ROS 2

[00:22:13] **Audrow Nash:** 10 years or so before the acquisition. Okay. And then Tully, fast forwarding through the evolution of Open Robotics. what were some of the larger milestones between 2013 and 2023?

[00:22:32] **Tully Foote:** Especially for ROS was the release of ROS 2, Willow Garage and that legacy was very focused on ROS 1. And when we started at Open Robotics, one of the things that was really foundational was, we'd ran a workshop in early 2013, which was called ROS for Products.

And we talked to a lot of people about how can we take ROS from the research field which we've been very focused on in ROS 1 to commercial space. And there were a lot of things that we identified, such as cross platform, embedded targets, installation targets, modularity and, reliability in terms of determinism for a startup and things like that.

And these were the things that we talked to a bunch of product managers. They, we had people from NASA there. We had people from autonomous driving, lots of people using ROS and wanted to use ROS in different spaces. but a lot of times our collaborators at Bosch prototyped an autonomous lawnmower with ROS at the Palo Alto research facility, and they got it green lit for being turned into a product, which you can now buy.

but the first thing that the product team did was throw out all of the research code written in ROS 1, because they weren't able to trust it to work. The research teams trusted it, but the products teams did not. And we wanted to build a new version of ROS, which product teams could trust. And that was the impetus for ROS 2.

And so at Open Robotics, we basically took that from the ground and built it all the way up to ROS 2, which was released. Several years ago now, and that's now what we consider mainline, and we're being used in products all over the world. 

The, biggest deployment is all Roombas newer than i7, I believe.

[00:24:35] **Audrow Nash:** Hell yeah. I have one in my

[00:24:37] **Tully Foote:** millions of robots.


## [00:24:39] Player and ROS 2

[00:24:39] **Audrow Nash:** It's so cool. It's so interesting. So we had ROS 1. ROS 1 came out of Player, which came out of, WillowGarage. Was Player at WillowGarage? 

[00:24:49] **Geoff Biggs:** There's no direct connection between Player and ROS 1. ROS 1 grew out of a project called Switchyard, which was done at Stanford. It's a way to try and improve on the concepts of Player as part of its goals. but, there's a lot of intellectual legacy because a lot of the people who worked on player also worked on ROS, and, Brian was the leader of both of them and so on, It's all mixed up, but there's no direct code. Legacy that I'm aware of anyway.

[00:25:17] **Audrow Nash:** Makes sense. okay, but we had ROS 1 and ROS 1 was heavily used in the research world, but then now Open Robotics gets up and running, it gets funded, it's getting contract work, and then ROS 2 comes along as a way of making it so that we can bridge the gap from research to production.

And that was a big step for the robotics community. 


## [00:25:42] Towards a robot revolution

[00:25:42] **Audrow Nash:** I think. this probably starts going towards the robot revolution that you were mentioning, Geoff. Would you tell me a bit about it and how it's, I dunno why this is exciting, 

[00:25:56] **Geoff Biggs:** Back when I did my PhD and then when I started as a researcher, service robots, robots outside of factories and outside of cages was still very much like a dream. It's like this is, maybe we can do it in really simple cases like the Roomba, but anything more complex than that, we don't have the computing power, we don't have the software, it's too hard to develop. and ROS really solved the too hard to developer thing, pretty much. And ROS offered three important things to people building robots who wanted to build complex service robots. It offered, first of all, it offered really good developer tools. Something that all the actors before it didn't do, including Player.

They didn't offer developer tools. They didn't offer things like RViz or ROS bag. These tools that just make your life easier. You can understand what the robot's seeing, for example. It also offered functionality libraries, the TF library. Very important one there. The navigation stack for ROSFarm was very helpful for prototyping and getting things off the ground and so on.

And the third thing was it made it a lot easier for people to exchange software. even in Player it was hard to do that because everything you used with Player had to be built into Player. so it was very hard to add new stuff to Player, which was annoying. But with ROS, everyone could distribute a new package.

And it just worked with all the other stuff because all the interfaces were the same. And because of those three things, it suddenly became a lot faster for people to prototype and then iterate and improve the robots they were building to the point where you could actually have useful services. And so companies like Fetch, they took this and they built on it and actually built usable products and did the product engineering to make sure that underneath was ROS doing all the hard stuff and they had a nice interface on top for the end user to use.

And, suddenly everyone's doing robots everywhere. And this is just in the past 10 years, it's really exploded the number of robotic startups. And now we see them on farms, we see them in warehouses, we see them in Antarctica, they're everywhere, right? So it's really quite amazing. It's just like Exponential growth.

[00:28:00] **Audrow Nash:** For sure. I thought one fact that Melanie brought up in our interview, a few back that Amazon has 750, 000 of their Kiva robots, the ones that bring the shelves to the pickers, to the people who pick from them, that's bonkers. That's so many robots. And then the number of Roombas that are out there, like it's, very exciting.

[00:28:23] **Geoff Biggs:** Yeah. And you think that 20 years ago, the first Roomba had only just been released and Kiva didn't exist.

And it's in two decades, we've just skyrocketed the number of robots being used in the world. It's incredible. And, and things like Dusty, with their construction robots, these things just weren't possible even 10 years ago.

And then, yeah, ROS just changed the equation because it just came, it became economically possible to develop a complex robot application. And a lot of that is thanks to ROS.

[00:28:55] **Audrow Nash:** I think so too. Hell yeah. Okay, so we've talked a lot about ROS, but Open Robotics was maintaining or stewarding other products too. Tully, would you tell me about all of the main projects at Open Robotics? Or actually, if you guys want to alternate, that'd be cool too. other than ROS, what else did we have at Open Robotics?


## [00:29:16] Gazebo for robot simulation

[00:29:16] **Tully Foote:** Sure. So the other one we've talked about is Gazebo. That's the, that was the one that I mentioned. It was the first project that got kicked off within Open Robotics. This also has legacy back to the player era. Brian and other collaborators developed Player. And then they realized that they really wanted to be able to test this.

And so some other colleagues developed Stage, which is a 2D simulator. For the test, the robot agents around.

[00:29:45] **Geoff Biggs:** It was actually round the other way. Stage was first. Richard Vaughan, who was a lab mate of Brian Gerkey, he developed a simulator called Arena. And then they decided they wanted to run their software on the simulator and on the robot, which was the first impetus for Player. And because they called it Player from the Shakespeare quote, all the world's a stage and all people are only players or whatever it is, they called, renamed the simulator to Arena.

[00:30:14] **Audrow Nash:** I had no idea!

[00:30:15] **Geoff Biggs:** A couple of years later, Nate Koenig came along and he said, we could do a 3D one now and because, what's a 3D stage? It's a gazebo. There's your name.

[00:30:26] **Audrow Nash:** Wonderful.

[00:30:27] **Geoff Biggs:** it all goes right back to the beginning. Yeah,

[00:30:30] **Audrow Nash:** Oh, yeah. Okay, so we have Gazebo

[00:30:32] **Geoff Biggs:** is actually still around as well you can still use it today with ROS

[00:30:35] **Audrow Nash:** Wow.

[00:30:36] **Geoff Biggs:** very

[00:30:37] **Tully Foote:** Going back, Gazebo was this 3D simulator that had this older, longer legacy, and we picked it up at Willow Garage and basically brought it in and made it the first class simulator, for the PR2 usage, and to be the tool that we wanted the ROS community to be able to use and leverage.

it's not the only simulator available, but this is the one that we've put the most effort in and have the strongest integrations with. And so with that, Gazebo works independently of ROS but also is tightly integrated through well developed plugins. And we've pushed it, it obviously had its beginnings back in the Player Stage era, where it was little ground rope differential drive robots running around, some maybe holonomic ones.

We pushed it up, it did some, it's done autonomous car simulation for the DARPA Robotics Challenge. We built out its capabilities about doing simulated humanoids. And walking to the level that we can run the same motion control primitives on the simulated humanoid robot as the live one, and it continues to walk and function.

With other projects, we've pushed Gazebo to support flying vehicles, both fixed wing and multi propeller ones, using first level physics approximations of lift and drag. we've then taken that below the ocean and done underwater vehicles to support offshore research and testing because it turns out underwater is very hard to test.

And so simulation is very important because it's, you can't communicate with your underwater, survey device until it resurfaces. And you really want to make sure that you don't have a bug in your code that up is down and down is up. And you send your robot to the bottom of the ocean.

All of them have very fancy fail safe mechanisms to avoid that, but if you can, every, any single bug like that would cause a mission to fail can save you weeks of work.

[00:32:45] **Audrow Nash:** And like hundreds of thousands of dollars too, I imagine. I I interviewed

[00:32:50] **Tully Foote:** Ship time is very expensive. 

[00:32:52] **Audrow Nash:** For sure. You're talking about MBARI? For those interested, I interviewed them on the Sense Think Act Podcast, Ben from MBARI, and that is cool because their robots are going to sea for weeks at a time.

[00:33:06] **Geoff Biggs:** of them go for months. Amazing.

[00:33:23] **Tully Foote:** ROS.

[00:33:24] **Audrow Nash:** hell yeah. Let's see. And then from talking to another interview with Louise, who was leading Gazebo, the Gazebo team at Open Robotics for a while, she was saying one of the big advantages of Gazebo is that it's really modular. And so if you are simulating something simple, but wanted to run really fast, you can disable or just not include all of the parts that you're not using in your simulation and then because of that you can run at super fast speeds just because you're doing way less work, whereas it's very hard with completely opaque, not open source simulators and this kind of thing. So I thought that was a big advantage of Gazebo.

[00:34:06] **Tully Foote:** Yeah, the physics engine is swappable, the rendering engine is swappable, so people have plugged in various, hardware accelerated renderers and hardware accelerated physics engines for different research projects, and we can, let that happen. And the, super fast one is called the Trivial Physics Engine. 

[00:34:26] **Geoff Biggs:** SimplePhysicsEngine. Yeah. it's very simple.

[00:34:29] **Audrow Nash:** similar. Yeah.

[00:34:30] **Geoff Biggs:** Yeah.

[00:34:31] **Audrow Nash:** That's funny

[00:34:32] **Geoff Biggs:** It is trivial. It's just very basic physics.

[00:34:36] **Audrow Nash:** Hell yeah. That's great. Sometimes it's all you need.

[00:34:39] **Geoff Biggs:** It is. 


## [00:34:39] OpenRMF project at Open Rob

[00:34:39] **Geoff Biggs:** We actually, Open Robotics used it heavily for the OpenRMF project, because that was fleet management. we didn't really care if the robots were being accurately simulated in terms of avoiding obstacles and real grip and all that sort of stuff. Just wanted to know they were moving around on their paths properly.

[00:34:57] **Audrow Nash:** So actually that's a good segue, to Geoff, tell me about the OpenRMF project.

[00:35:02] **Geoff Biggs:** Yeah, so the OpenRMF project started back in 2018, I think it was. And this was actually in, A proposal from the government of Singapore, their research arm, and a hospital in Singapore. They came to Open Robotics and said, we've got this problem. Our hospital has got all these robots in them, but they come from different manufacturers, and all the fleets don't talk to each other.

And you get two different robots from different manufacturers trying to use the elevator at the same time, and they get stuck, and someone has to go and sort it out. And so this was like a problem. They went, yeah, basically.

[00:35:34] **Audrow Nash:** Yeah.

[00:35:35] **Geoff Biggs:** The cause traffic jams, because they can't talk to each other at all.

And so this was something that, can you come and help us figure out how to solve this? And so Open Robotics set up the Singapore office for its initial reason was to work on that project and that project turned into It's like a fleet manager manager basically. The idea is that it works with fleet managers to coordinate actions of robots that can't directly talk to each other and then that grew even bigger to the point where it becomes basically a sort of universal fleet manager and the actual fleet managers for each individual robot don't really do much thinking for themselves they just Control the robots, and OpenRMF is the one that is responsible for assigning tasks, figuring out who, which robot is, and which fleet is the one, best one to handle certain tasks and so on.

And so this was built in Singapore. to work in the hospital where it is being used in real life today to manage several fleets of robots on an industrial network in a very critical environment. It's a hospital, you've got to do things right, you've got to be careful. And these robots do things like delivering medicines, delivering food, cleaning the floors, all that sort of stuff.

And they take elevators, they do all this cool stuff. And OpenRMF controls all of that. It even does things like Saying, okay, this robot wants to use the elevator, so it cools the elevator for the robot and makes sure it gets to the right floor, or it opens doors for the robot and so on. It coordinates all of that for you.

And so this has really become, it's become the third major project of, Open Robotics because it's, as these robots, out in the world have grown in number. Something's got to manage them all to make sure they coordinate properly. And that's what OpenRMF does.

[00:37:21] **Audrow Nash:** Yeah, for sure. Yeah. I imagine anywhere that we're going to have a lot of robots, which if we see more of a service robots explosion, this kind of thing will be very, valuable, I imagine. And it's hard 

[00:37:33] **Geoff Biggs:** Yeah, 

[00:37:34] **Audrow Nash:** a especially interfacing with all these different makes of robots that had

[00:37:37] **Geoff Biggs:** it's really hard.

[00:37:39] **Audrow Nash:** to each other. And then I guess, I don't know if it's worth mentioning, but Tully is

[00:37:48] **Geoff Biggs:** it's like some of them are proprietary.

[00:37:52] **Audrow Nash:** Yep.

[00:37:54] **Geoff Biggs:** Some of them are proprietary, some are open source, they have different interfaces to their fleet managers, the robots themselves have different interfaces. And there's so many environments where this is important, not just hospitals. Like you can think of a hotel.

They would have relay robotics come in and do the delivery, they'll have iRobot come in and do the cleaning robots, and all these things they need to coordinate, and so on, and all these different environments, office buildings, out on the street, delivery robots. It's really important everywhere.

[00:38:19] **Audrow Nash:** For sure. Hell yeah. 


## [00:38:22] Important, but often forgotten: Open Robotics' infrastructure

[00:38:22] **Audrow Nash:** And then, maybe the last one to discuss as a significant project out of Open Robotics would be like the infrastructure, the build farm, things like

[00:38:32] **Geoff Biggs:** Absolutely.

[00:38:33] **Audrow Nash:** Tully, would you like to speak to this?

[00:38:35] **Tully Foote:** Yeah, so I think this is one of the things that is often goes unseen and just, taken for granted. the Open Robotics team has done an amazing job of providing infrastructure for the entire worldwide community to take advantage and make the use of ROS easy and convenient. you can go out there and just sudo, add the ROS sources and sudo apt-get install the packages on modern, recent Ubuntu LTSs.

And it just works, and you can be up and running in minutes. We've got Docker containers that are pre built with the latest software. you can download tarballs and install them, and you can just expect them to work. And, we've got a lot of web services that are up. The documentation services, that are there and available for the community to take advantage of.

And having all these things there at your fingertips It's something that a lot of people are just like, Oh, it's just there. It just works. But there's actually a whole team behind them making sure that's there and works well and that has quick response time for the developer so that you have the, like, when I make a pull request against some ROS package, I'll get a little response immediately, like moderately quickly saying Hey, this passes test, this fails the test.

And then we have deeper ones that run nightly or that are manually triggered that will run cross package, cross platform tests. So we can be confident when that gets merged, it's going to work and you won't break other people. And as long as we can keep that infrastructure and running, it helps significantly improves developer speed.

Because you don't have to worry that my change is actually breaking things that are in your pull request later. So that allows us to keep developer velocity up both for the core team, but also for the greater community. The foundation provides a ton of resources for building and releasing packages for the entire community.

If you, as an individual developer, wanted to release a ROS package, And you had to mainly go and build it and rebuild it every, time your dependencies were updated. it would be much, much slower because you'd have to poke a whole lot of other people. And whereas right now the Open Robotics provides all those services to the whole community if they're releasing open source software.

[00:41:10] **Audrow Nash:** Yeah, for sure. I think like the build farm is pretty amazing with all this. So people will create a ROS package and then they submit it to us on the ROS distro website. And, point to the release repository and then people can like it builds it checks it manages all the dependencies And then you can as you were saying you can apt get install it Which is like other people's packages in the community and then so this lets you install big packages like moveit or nav2 pretty easily, but even more esoteric ones still just an apt get install away, which is quite cool

[00:41:53] **Tully Foote:** Yeah, and I think that this is something that modern developers somewhat take for granted. back in the day when we had to check everything out and build from source, and if there was a bug you had to stop and SVN check out for the code and then start the build and go to lunch and come back to try it again.

I remember when we first had the binary builds that are available quick and moderately quickly, we actually got to the point that people were just like, I'm working on this project. There's a bug that's going to be fixed upstream. I'm going to wait the two days for the, other maintainer, release, patch, fix, and build.

And then I'll try again. And I'll go do something else. and it's a, it's another whole different way to think about things when that release pipeline can be trusted and be part of your critical supply chain.

[00:42:46] **Audrow Nash:** That's awesome. Yeah. And one thing that I've really liked is there's a site called index.ros.org. And so that one, it is an index for all the packages and it shows you how they all relate to each other and which distributions of ROS they're available for, links to documentations, link to the repository.

It's a very cool way to see what all is out there. And also You can see the relationships, what packages use what packages, and just trace them back really deep. I don't know. It's a very cool, complex network that has so many contributors to it.

[00:43:24] **Tully Foote:** Yes, it's a, that's a, great website that the foundation provides and, highly recommend people. Take advantage and leverage it. That's one that, is less, less appreciated. I think a lot of the content historically has been on the wiki, but we are moving to use index instead for ROS 2, so that it's a little bit more scalable.

The wiki has reached its limits and we can't sustain it anymore due to the underlying infrastructure.

[00:43:57] **Audrow Nash:** Yeah, that was more of a ROS 1 thing, and I think

[00:44:00] **Tully Foote:** the MoinMoin wikis are designed for one to 2000 pages. For the web server and I believe we're at something like 10 to 20, 000 pages. I have scripts that go through and clean up empty pages and spam pages to clear them out. But we're still running at something like 10x the number of pages that it was designed for and

we've had to throw extra resources at just to keep it running.

[00:44:29] **Geoff Biggs:** Yeah, probably the only reason it still runs is because CPUs have gotten faster.

[00:44:34] **Audrow Nash:** That's a good point. Let's see. Okay. So those are the main areas of Open Robotics. 


## [00:44:42] Open Robotics before the Intrinsic Acquisition

[00:44:42] **Audrow Nash:** where were we say 2022 or something like, like where was Open Robotics? How were we functioning as a company? Just where were we? Maybe Geoff?

[00:44:56] **Geoff Biggs:** I can speak to some of it. Tully was more involved in the management at that time. as a company, Open Robotics was actually very successful. It was technically a startup, it's only 10 years old, and it never had venture funding. It was entirely bootstrapped. So

[00:45:11] **Audrow Nash:** No debt at all, right?

[00:45:13] **Geoff Biggs:** Yeah, so for the company to grow, from just a few people at the start right up to about 50 or 60 by the time the acquisition happened, with no venture capital is pretty rare these days, especially in the technology sector.

And it was in general a pretty healthy company and I think all three of us here would absolutely agree it was a great place to work, very friendly, very good culture, it was a wonderful place to work. I think, I hand over to Tully though, I think he was more privy to what was going on at the management level in those days.

I was trying to be an engineer at that point.

[00:45:47] **Tully Foote:** Yeah, so I think that, we'd seen a lot of growth and we've seen, there's a lot of progress and things happening in the space and nearby spaces. There's a lot of innovations that are going on that are close to, in the robotic, space or close to the robotic space. You see all the funding for AI, big companies coming in and doing big investments.

And as Geoff mentioned, Open Robotics and OSRC had been bootstrapping all along. And with our business model, we couldn't make, big investments. A lot of what we did was, find projects that we would work on that would help push forward the state of the art. but we were doing it in a lot of small steps and finding ways, to find good customer, good projects for customers.

That would help us on our vision for how to improve ROS. 

We also wanted to do more strategic investment and push into regions that we thought would be, in bigger directions, take bigger steps, which is why we looked for, alternative ways to structure the project.

[00:46:49] **Audrow Nash:** Hell yeah, so how I understand it is we had we were contracting and so from contracting you get like a little margin of profit and so with that profit we had to I guess, I guess people were paid through the, I don't know. So you, get a little profit extra on top of everything, in addition to your running expenses.

And with that profit, you can reinvest it into large infrastructure changes, big, big features, larger initiatives, basically. And so that's very hard to do on the meager.

Not meager, but like just the thin layer from contracting, of profits. And, so because of that we were very iterative in what we rolled out. You agree, Tully, with this?


## [00:47:38] Big steps for the ROS community we can take because of Intrinsic (Zenoh)

[00:47:38] **Tully Foote:** I think that's, we were doing the work and then reinvesting into the open source. And we, it's not, we weren't able to take big steps, make big moves, invest in big projects.

[00:47:51] **Audrow Nash:** What, are some big projects that we'd like to, and we, what were some ones that we really wanted to invest in that would have required some big steps, versus very incremental change as we have?

[00:48:04] **Tully Foote:** so the, very concrete one is the RMW Zenoh.

[00:48:08] **Audrow Nash:** Ah, I'm so excited about that.

[00:48:10] **Tully Foote:** This is something that we have, we've seen potential in Zenoh, but we, and we'd done some proof of concepts, and we had some estimates of what it would take to do this sort of project. And, But there was no companies that were willing to step up and fund, hey, let's go develop that.

[00:48:32] **Audrow Nash:** Yep. Just to, for background with that, we were using DDS with ROS 2 as the primary middleware and it has pretty significant scaling issues, right? When we have a lot of nodes, because they have a lot of inter node traffic, is it correct?

And then Zenoh, it's another middleware, but it does things a little bit differently in a way that scales significantly better, and it seems like it's built for robotics applications or it's just very well suited for it, and so thus it will have a lot fewer middleware problems,

[00:49:08] **Tully Foote:** Yeah, so part of, what we did with ROS 2 is we very specifically designed it to have what we call the ROS middleware abstraction. And what this allows us to do is be able to switch, between our middleware implementation. we specifically did this because we were targeting the DDS standard, and there were multiple DDS vendors, and we've, over the years, we've had different default vendors.

We've had a whole selection of vendors available as the middleware implementation that we used.

But part of what we did was define that middleware abstraction, and the nice thing is we can actually switch to a potentially non DDS middleware if it can provide the same functionality. 

[00:49:51] **Audrow Nash:** I 

[00:49:52] **Geoff Biggs:** Yes

again soon. 

[00:49:55] **Tully Foote:** there's some

[00:49:55] **Audrow Nash:** middleware. there's some joke ones that still work because of abstraction 

[00:50:00] **Tully Foote:** we, joked about an April Fool's one, which would be a, Airhorn based Morse code middleware. And we'd have two robots communicating via Airhorns across the office. never got around to that one, but I do have some like electrically controlled Airhorns in the closet if anyone wants to work with me on that. 

[00:50:20] **Audrow Nash:** it.

[00:50:22] **Geoff Biggs:** care of

[00:50:27] **Tully Foote:** I from that one of the things we identified, we've done some projects and 

[00:50:32] **Geoff Biggs:** that. 

[00:50:36] **Tully Foote:** on Zenoh and there's, there are, definitely some potential benefits and we think it's worth investing in. We've done some projects with them that have worked out, using Zenoh that have worked out well and we want to, we, wanted to try it out and one of the things that's like at this scale.

We don't really know how it's going to work for everybody until we've actually built it. And so it's a moderately speculative thing to go and build this size of a project and see how it works. As you mentioned, we've ran into trouble with a bit of an impedance mismatch, I think, between the DDS vision of how distributed systems work and the ROS vision.

ROS very focused on nodes and lots of endpoints, and DDS would really rather do keyed topics, with filtering on shared topics. And so we're looking at, Zenoh as a potential alternative to try out. And so we're not, moving away from DDS, but we want to make the investment to see how it works, with Zenoh.


## [00:51:41] Rust for robotics

[00:51:41] **Audrow Nash:** Hell yeah, and one thing that's very exciting from my perspective, for Zenoh is built in Rust, the programming language, and Rust, I absolutely love Rust. I got to use it for one of my Open Robotics projects and just completely fell in love. So all my side projects are now in Rust. but so because of that, Rust is going to be more supported.

In the open robot or that's a big challenge, I think is to make it so that we can support Rust and its build process, which is fundamentally different to C++ and how it does versioning and how we do operating systems and

[00:52:20] **Geoff Biggs:** Yeah,

[00:52:21] **Audrow Nash:** dependencies and

[00:52:22] **Geoff Biggs:** it's been interesting because, so Rust, and in particular Cargo and its way of building things, are very different from how C++ and Python and a lot of other languages we've used up till now work. And so figuring out how to integrate that into workspaces and the Buildfarm, and in particular, one of the big problems is that Rust users, they used to be able to just rust up the latest version of Rust, whereas the Buildfarm can only use what's available from the system package manager from the default repositories.

And so that makes it, difficult to say, what version of Rust do you support, and so on. But these are problems that we are working on solving, and, we do hope to basically have Rust support in the Buildfarm. At about the same time, that we're trying to start getting Zenoh out there and then, then things are just gonna be awesome.

[00:53:12] **Audrow Nash:** Yes, totally. Yeah, it's funny that there's a complete mismatch in how they do dependencies for this. Completely different paradigms. And yeah, that's a hard square to circle, I think. But, okay. I'm excited about that. But, 


## [00:53:27] Intrinsic's acquisition of Open Robotics

[00:53:27] **Audrow Nash:** now we have enter Intrinsic. I think, maybe Tully, tell me a bit about Intrinsic and, the acquisition.

I don't know, just background on all this and what's occurred. And I know it was like a year ago,

[00:53:46] **Tully Foote:** Yep. Yeah. It's, 

[00:53:47] **Audrow Nash:** Good to figure it out now.

[00:53:48] **Tully Foote:** bit over a year ago. we worked out the agreement to have the open source robotics corporation, the for profit subsidiary doing the consulting work for open robotics. to be acquired by Intrinsic. this was a, mutual agreement where we, believe that it is beneficial for all the parties involved.

One of the, one of the interesting things when we were doing the, had our discussions, Open Robotics obviously has the mission to promote open source robotics, education, outreach, and development of software. And there was a slide with a mission to democratize access to robots. And, on the Open Robotics team, we're like, did we write that?

Or is that their slide? And it turns out it's their slide. and so this is where we, have a really good alignment on what, Open Robotics mission is and what Intrinsic is looking to do. And we're looking for, the ability to Intrinsic to make some of these bigger investments and to do things like the RMW Zenoh project, which is now underway.

We'd wanted to do that at Open Robotics for a long time. We had a proposal, we had an estimate, but we'd shopped it around and we're not finding people who are willing to invest in making that sort of effort to improve the core systems.

[00:55:13] **Audrow Nash:** Yeah, for sure. 

I was, the ROS boss in, for Humble. version. And we were talking about DDS and if that was possible and how much of a lift, Zenoh, and if we could be doing that. And it's just, that was years before, that was probably two years before the acquisition.

[00:55:32] **Geoff Biggs:** Yeah, we, we actually started looking at Zenoh for Singapore because in the hospital DDS was having problems on their commercial hide down network, things like discovery not working across subnets and so on. And so we started looking at Zenoh way back in 2020.

[00:55:50] **Audrow Nash:** Gotcha. So and then, Tully, would you tell me a bit more about Intrinsic? Who are, who is this company? What are they doing? They wanna democratize robotics, but how do they wanna democratize robotics? these kinds of things.

[00:56:09] **Tully Foote:** Yeah, so Intrinsic, we're a startup. It's coming out of the Alphabet, Google X Moonshot factory. And so Intrinsic has been going for several years, incubating internally. the acquisition was actually before we announced what Intrinsic was doing. but what we're, our current product that we're talking about is, automation of industrial work cells so that you can bring more of the modern robotics to this industrial workspace.

A lot of robotics has been very focused on very simple, repetitive tasks. And we want to be able to bring a more modern approach, including vision tools and dynamic planning, et cetera, to this environment.

[00:56:58] **Geoff Biggs:** to 

[00:57:00] **Audrow Nash:** And we're doing that with Flowstate.

and flow state is, it's, it seems awesome, like from the public demos, it's like a. Behavior or like a tree of actions that you put together and it makes a lot of the really hard robotics problems in setting up behavior for robotic arms and work cells much easier.

And so that's the intention so you can automate tasks.

[00:57:29] **Tully Foote:** Exactly, we're focused on providing the ability to deploy and, configuration management and bring a lot of the technologies from the cloud deployment space. To the industrial robotics space so that you can have your configuration management, your deployment control, introspection, logging, et cetera, from a web UI instead of necessarily needing to go in with a teach pendant to train each robot to do a specific task.

[00:58:01] **Audrow Nash:** And then also with the teach pendant it's if you have a KUKA arm or an ABB arm or whatever type of arm It's a different way of doing it. It's very like you need someone who's skilled in that specific make

[00:58:15] **Tully Foote:** exactly. The, skill, like the perception task can work with any robot out there. as long as the robot is capable of doing what you're looking for it to do. Likewise, we can, so we can swap out sensors, we can swap out robots, 


## [00:58:31] OSRF since the Intrinsic acquisition of OSRC

[00:58:31] **Audrow Nash:** and so intrinsic at the end of What year? So we're in 2024, at the beginning of 2023, at the end of 2022. so then Open Robotics, OSRC, the for profit part of Open Robotics was bought by Intrinsic, right? Okay. So Tully, you and I went over and Geoff, you stayed at OSRF. 

[00:59:04] **Geoff Biggs:** So I was asked to, so OSRF, effectively changed, the non profit arm. It had to change its operation model. So the board of directors, already existed, had existed from the start as a non profit, had to have a board. That was, Brian Gerkey, Steve Cousins, and Ryan Gariepy, three people who have been involved with, ROS all the way from the beginning.

So they needed to find a minimal staff to start operating the nonprofit. And so they chose, Vanessa Orsi, who was previously the CFO at the OSRC. she became the CEO of Open Robotics, of OSRF she's very capable. She's done like 20 nonprofits over her time, in America.

And it's, really good CEO to have. And then they asked me to come along and basically direct the technical side of things, the project management and figuring out what we need to make the projects work better as open source projects and so on. and so That was where basically I ended up switching to OSRF rather than OSRF. 

[01:00:15] **Audrow Nash:** Let's see with that transition. So it's just you and Vanessa that are running OSRF, at the moment.

[01:00:23] **Geoff Biggs:** Yeah. So we are, the two of us are the only staff, full time staff that the OSRF currently has. We do have several contract engineers from a wonderful Argentinian company called Ekumen that provide contract engineers who help out with the, Build, Farm, Maintenance and Infrastructure Development and all that sort of stuff.

They're really talented people, wouldn't survive without them, I don't think. 

[01:00:49] **Audrow Nash:** They're, great. they were working with us way

[01:00:51] **Geoff Biggs:** Oh yeah, we've, been using them for, yeah, they've been working with us since back in the Willow Garage days. They're a wonderful company, so talented.

[01:01:00] **Audrow Nash:** huh. So

[01:01:01] **Geoff Biggs:** and so they are contract engineers, and they work on the infrastructure and keep things going and develop new features and so on.

And that is. The extent of the actual, paid staff at the OSRF, and then, everything else is all volunteers, the whole community coming together. Obviously, there's still a big chunk of that is an intrinsic, former Open Robotics engineers from the OSRC are still heavily involved and we're very happy about that and a long way to continue.


## [01:01:33] How former OSRC folks contribute to OSRF now

[01:01:33] **Audrow Nash:** Tully, tell me about the, so you and I, and then pretty much everyone else at Open Robotics came along to Intrinsic. now how, are we involved still on Open Robotics? Where, the ROS 2, Gazebo, OpenRMF, the infrastructure, how are we still involved? And, is it just like They bought all the talent and now, like Intrinsic bought all the talent and now it's just a very small team.

Or how are we supporting, Open Robotics to be successful in the future at Intrinsic?

[01:02:17] **Tully Foote:** Yeah, so at Intrinsic, we, strongly believe in the value and the mission of, Open Robotics and the various projects we're investing to support them, supporting teams at Intrinsic doing core, ROS, Gazebo, OpenRMF and infrastructure development, as well as, people in the broader team are also contributing back in some of their overhead, or like in their, some of their small amount of time that is available to, on top of their other primary projects as well. 

[01:02:56] **Audrow Nash:** it's like the maintenance time. It's actually, it's very similar to the maintenance time we had while we were at Open Robotics.

[01:03:02] **Tully Foote:** Yeah, one of the analogies is that it's very similar to Open Robotics. We have, effectively one big project that we're working for instead of many little ones.

But where Intrinsic is values and investing heavily in all these projects and wants to continue to see them be successful.

[01:03:23] **Audrow Nash:** Then I'm not. 100 percent sure what can be said, but how, like from the community's perspective, if they don't know exactly how Intrinsic is using various things from Open Robotics. They may worry that Intrinsic cuts off part of it and some part of the Open Robotics project suites dies because of lack of investment.

How, did the different parts of Open Robotics, and is it fair to say that, or should I say OSRF for this? How, did the different

[01:03:53] **Geoff Biggs:** Probably OSRF would be a bit clearer at this point, yeah.

[01:03:57] **Audrow Nash:** So how did the different parts of OSRF fit in Intrinsic within what we can say, 

[01:04:06] **Tully Foote:** So we're, actively using all the parts, major components of the projects from OSRF within Intrinsic. I can't say much more about exactly how we're using them, but I, reassure you that they're, being used and look forward to being able to talk more about it. 


## [01:04:28] Announcing OSRA!

[01:04:28] **Tully Foote:** But I think that the, main thing that we want to, do, and actually a lot of why we're here, is actually to make it, make sure that the communities around these projects are bigger than one company. And that's why we've actually been pushing toward what we're just about to get talking to about now, the Open Source Robotics Alliance.

[01:04:50] **Audrow Nash:** Go ahead.

[01:04:52] **Tully Foote:** Geoff, you wanna take this?

[01:04:53] **Geoff Biggs:** Okay. Yeah. okay. That was a sudden change.

Yeah, the Open Source Robotics Alliance, is a new initiative from OSRF and in a nutshell, it is our plan for how we're going to improve. the governance of all the projects at the OSRF, going forward and basically make the projects much more sustainable and long term viable.

Because up till now, we've had the Open Source Robotics Corporation providing some funding and staff, engineers to work on the projects. And it was effectively a benevolent dictator for life situation. The community trusted the Open Robotics, people to Keep the projects going and do right by the community and in return, the Open Robotics people had you know, broad leeway to do what they thought was best for the projects and the funding for that as well.

But, without the OSRC anymore, the OSRF has no staff and no, no funding to keep all these things going. obviously the Open Source Robotics Foundation has not gone bankrupt all of a sudden. We've got enough of a nest egg, but we do need to have basically money and people to keep things going in the long term.

And from our point of view, we don't want to just do the OSRC again. That's, we'll just be repeating the cycle. We want something that's going to last much longer and be much more sustainable. and in particular, much more community driven, community involved than the OSRC was able to do just because of its nature, the structure of it.

And so that for that, we have basically, we've spent about a year and a half now putting together the Open Source Robotics Alliance and that is going to hopefully resolve all the issues we've had up till now with governance and processes and sustainability. The way I put it is that we want to move away from having just a few full time engineers at one company supporting the projects to where we have a hundred contributors, some of many of whom may be part time working on the projects.

it's much more sustainable to have a hundred people working half the time on the project than to have a couple of dozen working full time on it. Because if one of the full time people leaves, it's a huge loss of time and, talent. If one of the part time people leaves when you've got a hundred of them, it's much less of an impact.

And that really is the way that sustainable open source projects work. And so we're moving more towards that model.


## [01:07:27] Motivation for OSRA

[01:07:27] **Audrow Nash:** Okay. what were some of the issues with the past way of doing things? So you mentioned the loss between, if you have just a few full-time people, or if you have many part-time people, so that's a clear example of an issue that you would wanna fix, in constructing a new structure. But are, there other good, clear examples of things that you are trying to change with this structure?

[01:07:57] **Geoff Biggs:** Another thing that we really want to change is how much we have in terms of resources to do things. So with Open Source Robotics Corporation's funding We were able to maintain the projects and develop them at a slower pace than we liked, at least keep them going forward and pay for the infrastructure, which I learned last year costs more than you can possibly imagine to pay for.

And we, we've been able to do that, but we want to move to having a model where we've got much more resources to support these projects. And that Basically means financial resources, we want to be able to expand the capabilities of the infrastructure to have even more support for projects or more CI time, stronger CI time, stronger, CI tools like static analysis to make sure things are really production quality, things like it.

Documentation, in open source, very few people want to spend their time writing documentation. They want to write the cool features that people are going to use. But the documentation is still just as important. And we, in the past at Open Robotics, we actually had on staff a document writer. She was very good, but she was also just one person.

And there's very much a limit to what she was able to achieve because of that. There's so much documentation that needs written. And so if we have more financial resources, the OSRF would be able to hire more, document writers, on an as needed basis or full time, appropriately, in order to really improve the documentation.

Another example, if you want the project leader to have The full time availability to commit to a project. We could do that at Open Source Robotics Corporation because they work for us. But now they work for other companies and they'll be volunteers. if you want to guarantee their time, it'd be nice if you had to pay them yourselves. And infrastructure, not just the infrastructure costs, but also the cost of people to run and maintain the infrastructure. developer advocates, Kat Scott is amazing, but again, she's just one person. We'd love to have, half a dozen Kat Scotts just going around and telling people how great our software is and figuring out what the problems are that need to be fixed.

There's always

Go ahead, Tully.

[01:10:14] **Tully Foote:** I want to say I think one of the things we're, looking for with this is to grow the, this core community, part of one of the challenges is that with the ad hoc nature of the governance of the project and mostly being driven through OSRC and the staff there, you really needed a moderately tight connection to connect and be able to contribute.

Like obviously, pull requests are welcome, etc. from outside, but, we didn't have a good formalized method for people to come into the project and gain, gain experience and trust and become more and more delegation was harder to do because we didn't have a formalized method. 

[01:11:01] **Geoff Biggs:** Yep. 

[01:11:01] **Tully Foote:** of the things we did to encourage external contribution was we created the Technical Steering Committee or the TSC, and this was explicitly done.

As a way to bring in and provide a venue for corporations to come in and provide guidance to the project. we set this up. Early on, and it's a different model than most open source projects did because we had the benefit of the Open Source Robotics Corporation team providing a lot of that guidance and core capabilities and overhead support.

we actually really wanted to make the minimum bar threshold for people to come in and said, if you're going to be actively contributing, we'll give you a seat at the table. this is. Because we had the luxury of doing that with the OSRC staff there and available. You'll see a lot of the sort of boilerplate and background stuff and infrastructure was all provided by OSRC and not the TSC.

whereas Go ahead.

[01:12:05] **Audrow Nash:** and this is in the Open Robotics days when we, before the acquisition, we had the TSC, and yeah, so then you had companies have a seat if they have a full time employee on working on ROS or Gazebo, one of our projects, and then, okay, so continuing from there.

[01:12:26] **Tully Foote:** So I think that from there, what we're looking to do with OSRA is open this up and make their provide more formal channels for the collaboration across a broader community. you mentioned for the TSC, the one of the requirements is to be able to provide a full time engineer, to the development, which is actually a really high threshold.

it's basically impossible for an individual and any small startup, that's actually very hard to do as well. and so we wanted to have,

[01:12:59] **Audrow Nash:** a hundred thousand dollars of the company. That's just going to go right to, 

[01:13:05] **Tully Foote:** exactly, a full time engineer, you'd be able to have a whole staff member and, A lot of companies that want to contribute, maybe they're only a couple of people, 

a third or a quarter of your workforce to specifically open source development for the platform, is not feasible at that stage, but we want to have paths for those companies to engage and have a voice in the system.

[01:13:32] **Audrow Nash:** Yeah. So what I'm hearing, from the previous model to the new model, one of the things that you're really trying to do is you're trying to allow more people to contribute by having accepting fractional. people effectively. So if you can contribute a fraction of your time, you are, you have a good structure for how they can contribute and how they can be a part of the community.

Whereas before it was full people and that left a lot of, people who might have been happy to contribute, but can't give as much as was required. So that seems to be a big theme in this OSRA, initiative to me.

[01:14:14] **Geoff Biggs:** Yeah. We're trying to move away from tying, being involved in the governance as like a member from how much you contribute, because we don't think that's fair, every contribution is very important. Even if it's just a tiny bug for us, it's going to be helping someone else because, someone else is going to have that bug too.

And the more of those we have, the better for the project and the more further forward it moves. And so we want to move away from that. But we also want to have a way to get the financial income that we need to support the projects. And so we are moving away from our, you TSC model, with its very loose, ambiguous processes and No real defined way of being more involved in a project than just sending in pull requests. And we're moving more to a, more of, I'm not sure traditional is the right word since open source hasn't been around that long, but it is more of a traditional approach to doing open source software funding and management.

[01:15:16] **Audrow Nash:** so is it something you can look at from like the Python community or?


## [01:15:20] Merit-based contributors

[01:15:20] **Geoff Biggs:** Yeah, so if you look at things like the Linux Foundation, or the Eclipse Foundation, or the Cloud Native Computing Foundation, there's so many of these out there these days, They all have a very similar model, where members pay a membership fee. on an annual basis, and that gives them certain rights and benefits.

For example, they get the, the right to be on some kind of governing committee as one voice, and they get advertising benefits from being mentioned on the website and so on. And so we're going to have that in the OSRA. There will be membership, for, available for organizations, and they can be involved at the high levels of governance, of technical governance of the OSRA and the OSRA's projects.

But we also don't want to just say, okay, if you've got, if you've got a million dollars a year income, give us a chunk of that and you can be making the decisions. that's not very fair to the community, which is for ROS and Gazebo and Open RMAF and our infrastructure, the community is just so important.

It's the community that has grown them to this point over 15 years. And so we want to make sure that the community still has involvement. And so we have spiced things up a bit from the traditional model. we've kept, a lot of the meritocratic approach of some foundations like the Eclipse Foundation and the Apache Foundation for the project governance.

So the day to day of the projects, making the design decisions, deciding if a PR should be merged, all that sort of stuff. It should be done by the engineers who are actually doing it, is what we feel. and so the contributors who, Particularly dedicated to the project. they don't have to be a member of the SRA at all.

they can apply to be committers in the project and that gets them rights to merge broad quest and be involved in the day-to-day design decisions, and, all the other stuff that goes on every day in a open source project. and we're having a process for that is based on the Debian process for gaining privileges.

Where you have, you apply and you have a mentor who mentors you for a certain period of time and then the People who have already gone through that process and attained that committer status They can take a decision whether you become a committer or not. So it's all entirely meritocratic. there's no money involved at all It's based entirely around Does this person contribute?

Do they make good contributions? Are they good for the community? Are they good for the project? And if you are, you can be in. It's free. And that, is the entire lower layer of our OSRA governance structure with our project management committees, one for each project, is entirely meritocratic. 


## [01:18:06] OSRA Consortium

[01:18:06] **Geoff Biggs:** Above that is where we have more of the traditional consortium approach, where we have what we call the Technical Governance Committee.

The Technical Governance Committee takes more of a long term view. they worry about the OSRF as a whole, its whole technical roadmap as a whole, and not just not just the ROS roadmap, but the ROS and Gazebo and OpenRMF roadmaps and how do they merge together into a more of a long term vision, and things like that.

And they, that is where the consortium members get their, voice gets heard, and so they take the long term view. But even there, we don't want to just say, at the high level, pay to play, that doesn't work for us. And so we split the power. At the TGC level, we split the power between the paying members and the meritocratic members.

So representatives of the projects and representatives of the paying members, they come together and they discuss and they make decisions that will impact the longer term health of the foundation and its projects, for example, how do we use the budget to make sure the projects are getting the resources they need, for example, do we need to hire more document writers?

Do we need to invest in more CI time? Things like that.

[01:19:19] **Audrow Nash:** I like that a lot. So it's almost like the US government or something where you have multiple branches of it. So you have the meritocratic part and you have the consortium based part. And those both make decisions and they have their own weights in some sense.

[01:19:37] **Geoff Biggs:** Yeah, so we've tried to balance, we're trying to strike a balance basically between community involvement and involvement of people, of companies who are putting up big chunks of money. Basically because, there's companies they're putting up money to help fund these projects and keep them going and they do want to get something in return and it's not just all marketing and having their logo on a website.

They want to have, some of them want to have like engineering, voices involved and so that's why they get to have, some kind of voice in the TGC where they do technical governance as a whole and look at how all the projects are going and make sure things are going right and just you know keep the general health of the foundation good for the benefit of the projects.

[01:20:22] **Audrow Nash:** I like that quite a lot. 


## [01:20:23] Why companies might want to join the OSRA consortium

[01:20:23] **Audrow Nash:** What, explicitly are the benefits to joining as a consortium member?

[01:20:30] **Geoff Biggs:** So different companies look at the benefits in different ways like they depending on what they want and what sort of company they are they have different weights of what's important to them. So if you look at something like the Linux Foundation. the companies that pay huge chunks of money to be like the platinum sponsors of the Vince Foundation, they get a board seat, and so they get to be involved in the decision making of the foundation at a very high level.

But that's not really what they care about so much. So long as, the next trademark keeps on going and the project keeps on going, they're happy, generally. Because it's their engineers who are using it and product managers who are making decisions about it and so on. But they do the fact that they can just go around and say, Hey, we're a big sponsor of this and we're, got our logo on the website.

And they get, primary, they get priority choice of, sponsor booths at Linux conferences and things like that. So for a lot of companies, it's purely marketing benefits. They're just interested in the various different ways they can get marketing benefits out of it. And that's why you actually find that a lot of members of these sorts of foundations, the funding for the membership fee actually comes from the marketing budget.

Not the engineering budget,

[01:21:40] **Audrow Nash:** Oh, that's funny

[01:21:41] **Geoff Biggs:** something, something interesting that I learned, it's not quite how I expected, but it's how they work. For other companies, they want to be involved in the technical side of things. And so that's why they want to be like, in our case, they want to be on the TGC, be involved in those technical discussions and helping to steer the whole foundation for the longer term health of open source robotics.

[01:22:04] **Tully Foote:** Geoff I can 

[01:22:04] **Audrow Nash:** think, oh, go 

[01:22:05] **Tully Foote:** one other thing, which is that one of the benefits to the companies is also companies want to participate in this to invest in the project as a whole. 

[01:22:15] **Geoff Biggs:** Yes. 

[01:22:16] **Tully Foote:** if you think about a company that is building and relying on ROS or Gazebo or something else, if they're getting value from leveraging this open project.

and building their products and their, products are building on top of this and leveraging this. And if it was to go away next year, that would be very bad for them because they'd either have to purchase another replacement, build their own, or pick up maintenance themselves and so it's in the interest of companies that are out there and leveraging these tools and these resources that are provided in the open source to make sure that the open source project stays healthy and robust.

And so this is an opportunity also for them to provide that support and help de risk their own future looking down the line.

[01:23:02] **Geoff Biggs:** Yes, you can look at it as it's like saying they're paying their share of the maintenance costs. Thank you. Rather than paying for all of the maintenance costs themselves, and the dozens of engineers that would take, they just pay one small share. And everyone else pays one small share and together everyone comes together.

[01:23:20] **Audrow Nash:** That's really nice. Oh, yeah. And yeah, I've heard many companies thinking of it as Tully said with the de risking approach to keeping it going and one small share for maintenance is really nice because then you can aggregate and you can have people who specialize in maintaining the software rather than oh, your team suddenly has to go figure out some deep down bug in ROS 2, which is super complex.

And, someone who's very familiar with it on the ROS 2 team would be like, oh yeah, I know exactly what's happening.

[01:23:52] **Geoff Biggs:** Exactly. Yeah.

[01:23:54] **Audrow Nash:** okay. Hell yeah. 


## [01:23:55] OSRA membership types

[01:23:55] **Audrow Nash:** And what, one thing I believe is that the membership, they are tier or so there, there's probably different levels of support, but also there are different costs for different size organizations and things like this.

Correct?

[01:24:13] **Geoff Biggs:** Yes, so we have several different types of membership. So for organizations, we have, the standard levels is platinum, gold, and silver, which give similar rights, but different variations of them. And the cost for those Also varies based on the company, company headcount. We looked at various different models, having flat fees and, flat fees don't work because if you're a small company, it's a huge amount of money.

If you're Microsoft, it's a tiny amount of money and, things like that. so in the end, we came down to, using the, the revenue of either the company as a whole, or the business unit that's involved in robotics. sorry, income, yeah. and that gives, that's a good way to balance it. because, for example, a small start up with 10 people is going to have much less income than a very large company.

And At the same time also, a very new startup is not going to have much income at all because, they're still just kicking off, but they may have something to contribute even 

[01:25:21] **Tully Foote:** Sorry, Geoff. We do headcount.

[01:25:21] **Geoff Biggs:** So that goes a good Where did we do headcount? Oh, sorry, yeah, things changed. 

[01:25:28] **Audrow Nash:** Worries. Yeah. So it's slightly in flux, but it's proportional to the size, basically on some way.

[01:25:34] **Geoff Biggs:** It's, the size, yeah, so it is the size of the, company or the business unit involved because, if it's like If you look at something like, 

[01:25:43] **Audrow Nash:** Yeah.

[01:25:43] **Geoff Biggs:** something like Microsoft or Bosch or Amazon, it's not like the whole thing's doing robotics, right? So

[01:25:49] **Audrow Nash:** Yes, for

sure. 

[01:25:52] **Geoff Biggs:** Yeah. And so that's for organizations.

We also, of course, want academic institutions and non profits to show their support. So we have a very minimal fee to show that support. and most interestingly, it's something that many other foundations don't necessarily do. We also have a way for individuals to be members of the OSRA. And 

[01:26:14] **Audrow Nash:** At the consortium level or,

[01:26:16] **Geoff Biggs:** level, yes.

so individuals can pay a very small fee, on an annual basis. And that gives them the right to be what we call end user representatives. So the Technical Governance Committee and each project management committee have end user representatives on them and their job is to represent the community of users rather than developers.

So they're looking at it from a point of view of using our software, not just developing it. And so the people who are individual members in the OSRA are able to be elected to these positions and the elections, the people who vote in the elections are the, all the end user, all the, sorry, all the individual members of the OSRA.

Thanks. And so they choose one amongst them to represent them on the TGC, for example, and that person's job is to take the community's voice to the TGC, or to the Project Management Committee.

[01:27:15] **Audrow Nash:** Okay. That sounds really cool. And then, All so it'll be like, okay, we have a decision about how we should take the direction, like for this next release, are we going to like maybe make a bunch of features for quad rotors versus, and I'm just making stuff up versus, I don't know, industrial robots of some sort.

And so then the community can vote based on that, based on their seats in the consortium, is that kind of the intention? And it's proportional to your level in sense, to your head count.

[01:27:49] **Geoff Biggs:** Yeah, it won't necessarily be a vote, it depends on the decision being made and how the decision is made. if everyone says, hey, I'm good with that, there's no point holding an official vote, right? Just waste time. But yeah, so if it's like a very small, if it's for an individual project, we're making a decision this week about whether to merge a PR, then all people who are committers on the project plus the end user representative on that project committee will be able to, discuss and be involved in that decision.

If it's a decision like this project is asked for, 100k a year to pay for a certain resource that they need to, and they say they need it for the project. But if we do that, we can't give resources to these other projects or something like that, the TGC will be involved in making that decision and the end user representative on the TGC will be part of that discussion and part of that decision making.

[01:28:41] **Audrow Nash:** I see. That's cool. I like that you're including individual contributers.

[01:28:47] **Geoff Biggs:** Yeah, we think it's important, the community and the individual, they're very important to us from the history of ROS and also robotics, hobbyists, for example, lots of hobbyists in robotics and there's no reason to ignore them. And yeah, we think that they should be involved and they should have a voice, even if it's just one amongst many, they still need to be heard.

[01:29:06] **Audrow Nash:** Yes, for sure. okay, that sounds great. So we have the consortium based approach and then we have the meritocratic one where you're on specific projects. 


## [01:29:18] Meritocratic contributors + how to mentor and get involved

[01:29:18] **Audrow Nash:** I imagine that there's a lot of very interesting ideas of how to get this set up and rolling and this kind of thing. Maybe, do you think?

Tully, do you think you'd be good to speak to this or should we go to Geoff for talking about the meritocratic part? You go, you guys know what I mean anyway.

[01:29:40] **Geoff Biggs:** Yeah, meritocratic.

[01:29:41] **Audrow Nash:** Yes. Meritocratic. go ahead Tully.

[01:29:47] **Tully Foote:** Yeah, I think what we'd really like to do is keep, we, we have a pretty good culture of this at the moment and we're trying to look to formalize it. We have project leads, we've actually asked all of the existing project leads to continue on in the project lead role under OSRA, and then for the first year and at the end of the year, they'll be up for reelection within the PMC going forward, in the next year, so we'd really like it that we can basically formalize a little bit of what we're doing. Each project committee will have the opportunity to define their own process. each of our different projects has very different composition and makeup.

The ROS project has a lot of moderately federated packages and maintainer ship is distributed, whereas something like, Gazebo is midscale with some federation, but a lot of overlap on core maintainers. And then the OpenRMF and infrastructure projects are actually much, much tighter knit communities with a smaller group.

And so the, same project management structure is not gonna be correct for each of them. And so we want to, we're gonna let each of those project committees. Set up their own structure. We've laid out some high level guides saying you need to provide structure along these lines, such as the mentorship and adoption process for new contributors to come in.

But we're going to leave that up to each, committee to actually define that. And when you become a committer. What access do you get, et cetera. it depends on what project. It depends on the scope and how they want to do that.

[01:31:30] **Audrow Nash:** Gotcha. So we are coming to the end of the time that we had booked. Are you guys running okay with running a little bit long, like maybe 15 minutes or something, or do you have to run,

[01:31:42] **Geoff Biggs:** Good.

[01:31:42] **Tully Foote:** Yeah, I could keep going.

[01:31:43] **Audrow Nash:** Okay, hell yeah.

I like the idea of it because of these. Different projects, within OSRA are different in nature.

You're allowing the people who have been most involved to like the, leaders of each of them to, decide how to roll out these strategies. Will there be additional, cause one thing, like ROS 2, which is mostly what I've worked on, between our projects is enormous. Like it's, probably a hundred repositories across the whole project and, this is just our core repositories. 


## [01:32:26] Mentorship process

[01:32:26] **Audrow Nash:** Where are we getting the initial mentors from? Is it mostly people that are now at Intrinsic or what do we imagine for, this, the onboarding steps for the meritocratic part?

[01:32:41] **Geoff Biggs:** So I'm actually working on this at the moment, as we're recording, we're recording this in advance of the announcement, but I'm working with the four project leads and we are drawing up the lists of the initial set of committers for each project, and what specific repositories they need to have access to.

And that's going to be our, Our kickoff point for each PMC and then from the operational date of the OSRA, from that point forward, anyone will be able to say, I want to be a committer, put their hand up and then go through the mentorship process. and so we think that probably for the first year, At least, the teams would look very similar to how they look now.

So for OpenRMF and Gazebo, it's quite internal to Intrinsic. For ROS, there's a bit of a mix, probably about, maybe not half and half, a fairly good balance at the moment of, ex Open Robotics people at Intrinsic and people from other companies such as Sony. But we think over time, as other people become more involved in the projects, become more interested in being involved in the day to day, rather than just sending the occasional PR, we'll think that we'll see more committers from outside the old Open Robotics team start becoming involved.

And that's really what we're aiming for, we want to have these project management codes be as diverse as possible and in all the different meanings of diversity. we want all of that in there so that they are long term sustainable, we don't want to have Bob from the ROS PMC left and he's not involved anymore and we don't know how to do half the project.

That's not a situation we want to be in anymore.

[01:34:24] **Audrow Nash:** For sure. 


## [01:34:25] The value of contributing to open source software

[01:34:25] **Audrow Nash:** Yeah, one, one thing that just thinking about my conversations on Spaces, on X and things like this, with various people in the community, especially those that are trying to get involved in robotics, I often recommend them go make open source contributions because of the mentorship that you get.

Yeah, it's really amazing because, so you make a pull request, the changes you think you should be adding, a new feature, fixing a bug, whatever it is, and then someone who has a lot of experience with the project, if it's one of the intrinsic folks or like one of the original Open Robotics people or anyone in the community that has been doing it for a while.

They probably have great software developer chops, and they'll tell you oh, you could approach this better, here's how I would frame it, here's some formatting, or, conventions that I would use that are good at reducing bugs or whatever it might be. and I feel like that's so valuable, like my, time when I started at Open Robotics, it was just such fast learning because of the feedback of the pull request process.

and I think people will become much better software engineers from doing this kind of process.

[01:35:46] **Geoff Biggs:** I really strongly agree. I tell younger engineers whenever I talk to them about like why they should open source. One of the things I always say is, The job I'm in today and probably most of my career is not because I got a PhD, it's because I did open source software, since 2003 or 2004 I've been doing open source software for robotics and that has introduced me to people, it's given me openings, but more importantly it's taught me good software engineering practices, just working with so many different people, learning how they work and how they do things and figuring out what works for them and how it will work for me, That's given me much better skills than I would have got just staying in one company and only doing that company's processes and just, yeah, and talking to other engineers, even, even in robotics, I started at Open Robotics in 2020 and I still learn lots, and people like William Woodall, he's, got incredible C++ skills, right?

He taught me so much about C++, and Michael Gray, who does OpenRMF again, he taught me amazing things about C templates and now Rust, yep. and so you're always learning in open source. It's great. It's a really good way just to become and stay in an amazing software engineer is to be involved in open source.

And I think the most important thing is never be too embarrassed to put in a pull request. Even if it's one line, you put in a pull request, people will see it, and they'll tell you how to make it better, and you will know next time around, and you will learn from that, and your software will get better.

And,

[01:37:25] **Audrow Nash:** And even if you, so like sometimes I'll be working on some side project or something and I'll be using a library and something doesn't seem how I expect. And so I'll make even an issue or sometimes pull request. and a lot of times it points out something that was either poorly communicated in their documentation or misleading or whatever.

And it's a good opportunity for them to improve their project. And a lot of times the response that I get, it's even if I think it's a silly question, they're very open to it and they're very helpful

[01:37:59] **Geoff Biggs:** Yeah, you learn very quickly, you learn very quickly that open source, people who do open source software, are generally open minded, they want to talk to other people about the software, they want to learn from others about how they can make it better, where the problems are, and they want to help other people help their project.

if if someone makes a pull request to my project that fixes, or adds a new feature, it's in my interest to help them brush it up and get it merged, because then I don't have to do it myself, and takes less time to help them, than it would to do it myself, and they benefit from that because they learn as well, we all benefit.

It's

[01:38:36] **Audrow Nash:** And they might get a feature they wanted. 

[01:38:38] **Geoff Biggs:** Yeah, they get a feature they wanted, we get a new feature in the software, which is good for other users, it grows the software, this is why the open source software, Open Source Robotics Foundation exists, because this is the way we believe. Robotics has grown and is going to continue growing, and that's what we want to support, this whole,

[01:38:55] **Tully Foote:** and overall the development velocity of your open source is amazing because

[01:38:59] **Geoff Biggs:** oh, incredible.

[01:39:00] **Tully Foote:** You have this large pool of people, each one contributes a little bit and the whole, everyone moves forward at the rate of the sum of the contributions.

[01:39:09] **Geoff Biggs:** Yeah, and it never stops too, right? 24 7 it's always getting new stuff coming in if you've got a resource,

[01:39:17] **Audrow Nash:** For sure

[01:39:17] **Geoff Biggs:** always going forward.


## [01:39:19] OSRA's badging system for contributors

[01:39:19] **Audrow Nash:** One thought that I have, and I don't know if you guys are planning to do this. but if not, maybe consider doing this. I think that one of the other big benefits of people contributing to open source, kind of Geoff, as you've mentioned, is that you start to meet people in the community and that has given you opportunities and jobs and this kind of thing.

What I would think would be a really cool thing is somehow have a leaderboard or it doesn't, need to be competitive per se, but some way of making it so that people are highlighted for their contributions, because that visibility will make it so other people know them a little bit better.

And maybe it's a better way to get a first job or something like this.

[01:40:12] **Geoff Biggs:** Oh, yeah, 

[01:40:13] **Tully Foote:** we,

[01:40:14] **Audrow Nash:** would love to see that. Go ahead, Tully.

[01:40:16] **Tully Foote:** I was going to say we're, actively working on that. We're working on a badging system. So that people can get acknowledgement for being whatever their status is. They can show that off in advertising it. We're also going to work to try and integrate it with some of our various infrastructures.

See if we can get them badging on some of our sites and the forums, et cetera.

[01:40:36] **Audrow Nash:** Hell yeah. Oh, I love it. Go ahead, Geoff. Did you have anything to add?

[01:40:40] **Geoff Biggs:** Yeah, I was just going to say, apart from the badge system, this is actually something that we've been promoting to potential member companies as well, is that if you get involved in the OSRA, it's a really good way to find new talent that you can hire. Because the people who are actively involved at the meritocratic layer are guaranteed to be people who already know the software so they can hit the ground running when you hire them.

But they're also guaranteed to be good engineers who are open minded and willing to learn and are already, already learning just by being involved. And so that's, it's good for companies and it's good for the people who are contributing. everyone learns, everyone benefits, and everyone gets in touch with each other.

You can see, I know who that person is, I've seen their contributions going into the software, I think they're great, I want to work with them.

[01:41:31] **Audrow Nash:** Hell yeah. Do you ever think, so related to that, it seems like a fairly logical next step to me to also help, almost have a jobs board. Or for some of the, consortium companies that may be looking for jobs, like exposing and helping people that are looking connect to possible openings in jobs, any plan to do that, or that, to be, that could be quite lucrative,

[01:42:02] **Geoff Biggs:** That's actually one of the, one of the membership benefits is that, we haven't got it set up yet, but there will be a jobs advertisement system on the website, and members will be able to advertise jobs there. and, we've seen some of this in this in discourse, and, we've seen people advertising internships and full time positions and so on.

We want to basically try and formalize it and make it better for people to use. And so for members, this will be a benefit is that they can send in their jobs, that job board, and then that will be somewhere where one central place for engineers who know ROS or know Gazebo can go and find jobs that are going to be using the skills they have and know that they will have an advantage in applying for those jobs because they'll be able to promote their own involvement in the OSRA.

[01:42:49] **Audrow Nash:** I really like that. 


## [01:42:52] Educating more people to be roboticists

[01:42:52] **Audrow Nash:** Okay, now we're talking about getting people in jobs and what this makes me then think of is skilling people up, educating them this kind of thing so that they are in a position to do this. And part of that is the mentorship perspective, but is there going to be other efforts around education?

Maybe so that we can increase the number of people that would be contributing. You mentioned Better Docs as a big initiative. but is there anything else that will go towards skilling up people in general? It's

[01:43:27] **Geoff Biggs:** We, the Open OSRF actually has, as one of its goals, is education in robotics, open source software robotics, and so we do actually have some plans in this area, so I think everyone knows, the TurtleBot has been around for a dozen years now, I think, started at World of Garage first, I think, yeah, Tully was the originator of that.

As I recall. And so that's a big thing for education, but we also want to do, better in that regard. Not just providing a robot that runs ROS, but we actually want to have, tutorials that work with it, and courses you can do with it, and so on. And so we do have ideas in there, but these are going to take a little bit longer to come to fruition.

[01:44:10] **Audrow Nash:** It's a lot that's already happening. 

[01:44:12] **Geoff Biggs:** We've focusing on OSRA for the first year, and, once that's up and running, then we'll have more time to focus on those as well. But yeah, watch the space. There's going to be fun stuff coming.

[01:44:21] **Audrow Nash:** Hell yeah. That seems awesome to me. is there anything else for either of you that you want to mention regarding OSRA? Or I don't know any, and if not, I would love to see where you think things are going, for the community and for our whole initiative.

[01:44:43] **Geoff Biggs:** I think, for the community as a whole, not just the initiative. obviously, I hope the OSRA succeeds, and I think it will. I think for the community as a whole, this is going to be really a beneficial thing, very much in the long term, especially. in the short term, if you're a user of the software, you're not going to see much change.

If you're a developer of the software who just sends an occasional PR, then you're probably not going to see much change for a while. If she's really getting heavily involved, then maybe they will be changed. you could be a committer, for example, but in the longterm, I think this is really going to accelerate the development of all of the OSRF projects and make them better for the people who want to use them.

So if you're a hobbyist, it's going to be higher quality software. So it'd be less. Less gotchas for you to worry about, or less problems. But if you're a company, there's going to be much more production quality. There'll be much less, trouble for you to ensure your robots work. Because you will know that the underlying software is being developed using the resources of the whole robotics industry, pulled together to provide great software.

The same way that companies can rely on the Linux kernel for putting in their products, I think, really, we're going to see acceleration of that to that level, and also acceleration of new features. just in the past year, the RMW Zenith thing is just shows what's possible when we have a consortium approach rather than just one company doing the full development.

[01:46:06] **Audrow Nash:** That's a good point. Yeah. We are able to make a heavy lift now under Intrinsic 

[01:46:13] **Geoff Biggs:** Yeah, 

[01:46:13] **Audrow Nash:** Or Intrinsic funding a lot of development. that's a wonderful thing. Yeah. And so you're saying more of the same will continue.

[01:46:22] **Geoff Biggs:** I believe so, yes.

[01:46:23] **Audrow Nash:** And we'll be able to make larger shifts that improve, and it might be documentation.

It might be education. It might be, I don't know, all sorts of other supporting things that make the community richer. Yeah. So that's all wonderful. Tully, what do you think?

[01:46:40] **Tully Foote:** Yeah, I'm really want to look to grow and diversify. we've been a small tight knit community and I think we, I'd like to see more people get involved and doing this. Setting up the slightly more formal structure, I think will give us the ability to reach out and grow effectively.

We've reached the limit of the scale we can grow with direct connections and where I'm looking forward to. Seeing more people getting involved, more companies getting involved at more levels with these, more opportunities for engagement and representation, actually, to get, more voices involved in the community.

[01:47:21] **Audrow Nash:** Hell yeah. Love it. Let's see. 


## [01:47:26] Robotics in the next 5 years

[01:47:26] **Audrow Nash:** Now, starting to wrap up, what do you guys think for robotics, like, when you think about five years in the future, what are you thinking will be different, where, just tell me where you think robotics will be in five years, and what opportunities may be on the way to there.

Wanna start with Geoff?

[01:47:52] **Geoff Biggs:** Okay, I think we're probably going to see two major trends. One is we're going to see a lot more multiple robots in a single space. And I don't just mean like a whole pile of Kivas. multiple robots from multiple vendors. So like that whole thing with, hotels with, delivery robots going to the rooms and cleaning robots and so on.

that sort of thing we're going to see much more of, I think. all these, single use service robots are really going to be everywhere, I think, inside and outside. And I think we're going to see a lot more of that. The other thing I think we're going to see is that robots start coming to market a lot faster.

And that will in part be because of software like ROS and in part be because of software built on ROS will start becoming much more widely available both open source and for sale stuff so like you'll be able to, we already see a few companies doing this but you'll be able to go and buy a robot chassis and then from a different company go and buy a navigation system that you can put on it for example and so it'll become much more of that robotics companies become companies who provide services using robots, and they just, do a bit of integration work to pull this together.

I think that's the way we're going to see things going. And, I really look forward to getting to that point, because that's when the promise of ROS, and Gazebo, and OpenRMF, and open source robots in general really takes off. When people start not building the whole robot themselves, but trading parts with each other.

[01:49:30] **Audrow Nash:** Yeah, I think I had an interview, I think the last one published, or episode three was with Polymath Robotics, and they're doing just this. And it's the start of this trend from my perspective, where they're taking ROS, they're building some nice things on top of it that make it very easy to access, and then you can just build applications on that, which is so cool.

It's starting. I think.

[01:49:53] **Geoff Biggs:** It's starting.

[01:49:53] **Audrow Nash:** Your observation is already starting, which is the coolest thing.

[01:49:56] **Tully Foote:** Yeah, it's, it's fun to reflect on that because actually one of the visions that we set out when we were designing ROS back in 07, 08 era. Was, we wanted to be the LAMP stamp for robotics, where

[01:50:12] **Audrow Nash:** Does LAMP stamp mean? I don't know what that,

[01:50:14] **Tully Foote:** LAMP stack. The Linux, Apache, MySQL, PHP, Perl, Python.

[01:50:19] **Audrow Nash:** It was how people would build websites,

[01:50:21] **Tully Foote:** Exactly. This was one of the really early demonstrations of the power of open source with those open source tools as generic building blocks.

If you had an idea for a website that you wanted to stand up. You could use those tools, and a little bit of configuration and coding on top of it, create a website very quickly. Literally you could make prototypes overnight.

[01:50:48] **Geoff Biggs:** Yeah, you can look at it as like with that, with those four tools you could build Amazon. That's the way it was basically.

[01:50:55] **Tully Foote:** Yeah, 

[01:50:56] **Audrow Nash:** Yeah. 

[01:50:57] **Tully Foote:** And Amazon and Facebook, the, all of, if you had an idea, and the nice thing is with these open source tools, they were accessible to an individual. So that if I came along, I had a great idea, I could make a prototype, and it would just be there and be ready to go. And the vision we had for ROS was to provide that LAMP stack for robotics, so that all the tools are there that you can bring together.

And, if you have an idea for a robot application, you pick these parts off the shelf, the open source ones, you put them together in the configuration that will achieve your application, and you can test it out and deploy very quickly. And I think we are now, we're, that is insight where we can actually have this thing where it may actually be like robots that are getting deployed.

It's not just, 

[01:51:51] **Audrow Nash:** Websites 

[01:51:52] **Tully Foote:** Exactly

[01:51:54] **Geoff Biggs:** We're right at the very, yeah, we're at the very edge of that. And that's, going to be the next revolution for us. I think we've seen this sudden surge in robotic startups for the next one is going to be when they start sharing stuff, selling stuff to each other, and that's going to be amazing. 

[01:52:09] **Audrow Nash:** Hell yeah.


## [01:52:10] Why open source?

[01:52:10] **Audrow Nash:** To maybe ask an obvious question that we all agree with, but may not be clear, and Tully, what's the value of the open source part of this versus closed source or like things you can just buy and you don't know what's going on in them? Why open source?

[01:52:29] **Tully Foote:** So there, there are lots of components to open source that provide value. I think that for me, the most valuable thing is the development velocity. I mentioned that a little bit earlier, but basically. If there's 10 of us putting little incremental changes into one product for a tenth of our time, that's actually the equivalent of a full time engineer.

And so if you can get this community of small contributions that keep stepping state of the art forward, you can actually do more than if you invested a full time person to develop it for yourself. And so by leveraging this broader community, the development velocity goes forward faster. in addition, and every incremental person contributing and participating in the community accelerates everybody together, which is this really powerful incentive to join and collaborate.

Because if you break off and do your own little thing, you do that, but then you incur all of the development costs and all of the overhead and maintenance and,

[01:53:38] **Audrow Nash:** the tech debt.

[01:53:39] **Tully Foote:** have to try to keep up. With the distributed community development.

so you have to both invest in the velocity and the maintenance.

[01:53:50] **Audrow Nash:** Go ahead, Geoff.

[01:53:51] **Geoff Biggs:** The way I like to put it is that, for the cost of a little bit of engineering time to contribute to the project, you get a very large amount of free labor, basically.

That's the way I like to put it, because to companies, free labor sounds great compared to paying for their own engineers, right?

And that's what you get. you're getting all these other people. are effectively working for you for free. sure, they're working for themselves and for everyone else as well, but they're working for you for free for something that you could never do yourself because it just takes too much time to do and you'd have to pay dozens of engineers or more.

it's really a massive benefit.

[01:54:29] **Audrow Nash:** Yeah. And also like the hardening of the code too, because you have so many people using it and you're going to find a lot more of those flaky 1 percent or one in a thousand or 10, 000 bugs

[01:54:42] **Geoff Biggs:** That's actually a key point there. It's not just the number of people, it's the variety of viewpoints and thought processes and use cases. 

[01:54:52] **Audrow Nash:** Great way to put it. Yeah, Tully.

[01:54:55] **Tully Foote:** I was going say the ability to understand that this has been used and demonstrated by a lot of people in a lot places. Allows you to have more confidence in something like a heavily used project, and, the more people have tested it out, the more corner cases you've discovered, the longer it's been there, opportunities to find those defects come up, and if we have good processes and good quality processes to make sure that we add regression tests, For each corner case that anybody discovers, you can be more confident when you pick up the open source software.

[01:55:29] **Audrow Nash:** Definitely. Hell yeah, okay, that's really cool to hear all those thoughts on this. 


## [01:55:36] Final thoughts

[01:55:36] **Audrow Nash:** If you, were to summarize everything we've talked about, or just the OSRA stuff, what would be the main takeaways that you hope people come away with? start with Geoff,

[01:55:53] **Geoff Biggs:** I think, my main takeaway for people is that the OSRA looks like a big change, but really what we're doing is taking what we've done so far and giving it, much, better. Hope for the future, much stronger, much more sustainable future to ensure that we keep on going for a very long time to come.

The OSRA is our route to achieving that.

[01:56:25] **Audrow Nash:** Hell yeah, and Tully.

[01:56:27] **Tully Foote:** I think my takeaway would be that I hope that anyone listening to this finds a way to get engaged with OSRA. We have opportunities for corporations. We have opportunities for individuals. I think it's powerful for any of you to get involved. We're looking to build pathways to make that available and the project will be better if you get involved.

So please come out, join us, and help build this product into a greater thing. We've already got over half a dozen members committed, and I hope that if you're at a company, please consider joining us. 

[01:57:04] **Audrow Nash:** Hell yeah, and we'll include links to all the things that they might want to look at if they want to join. Awesome, so it'll all be online for this I assume.

[01:57:16] **Geoff Biggs:** Yes. Yes.

[01:57:17] **Audrow Nash:** Hell yeah. Okay, thank you both and I really, it was just awesome to hear more like the origin stories for Willow Garage and Open Robotics, like a lot of stuff that I didn't know.

And I think OSRA seems like a very good initiative and probably very good for the community. And I see what you're saying with things accelerating. To robot revolution, and I'm looking forward to it. So thank you both.

[01:57:44] **Geoff Biggs:** Thank you very much.

[01:57:44] **Tully Foote:** Thank you.

[01:57:46] **Audrow Nash:** Bye everyone.

You made it! 

What do you think? Will you be joining OSRA? I'll put a link in the description if you want to check it out. 

One more shout out to OSRA's founding sponsors, Intrinsic, NVIDIA, Qualcomm, Apex, Zetascale, Clearpath, Ekumen, eProsima, Picnic, Silicon Valley Robotics, Canonical, and Open Navigation. 

That's all for now. Happy building!


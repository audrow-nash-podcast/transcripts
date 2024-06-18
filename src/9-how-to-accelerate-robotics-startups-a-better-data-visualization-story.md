- [\[00:00:00\] Episode Introduction](#000000-episode-introduction)
- [\[00:01:28\] Introduction to Adrian Macneil and Foxglove](#000128-introduction-to-adrian-macneil-and-foxglove)
- [\[00:01:43\] The Genesis of Foxglove](#000143-the-genesis-of-foxglove)
- [\[00:04:55\] Challenges in Robotics Data Logging](#000455-challenges-in-robotics-data-logging)
- [\[00:07:20\] MCAP: A New Standard for Robotics Logging](#000720-mcap-a-new-standard-for-robotics-logging)
- [\[00:18:35\] Data Upload and Ingestion in Robotics](#001835-data-upload-and-ingestion-in-robotics)
- [\[00:30:46\] Cloud Indexing and Data Management](#003046-cloud-indexing-and-data-management)
- [\[00:35:53\] Visualization in Robotics](#003553-visualization-in-robotics)
- [\[00:39:05\] Performance and Platform Considerations](#003905-performance-and-platform-considerations)
- [\[00:51:54\] Extensibility and Customization](#005154-extensibility-and-customization)
- [\[00:56:50\] The Evolution of Foxglove Visualizer](#005650-the-evolution-of-foxglove-visualizer)
- [\[00:58:17\] Customizing Visualizations with Plugins and Extensions](#005817-customizing-visualizations-with-plugins-and-extensions)
- [\[01:00:23\] Advanced Visualization Techniques and Extensions](#010023-advanced-visualization-techniques-and-extensions)
- [\[01:06:57\] WebAssembly and Performance Enhancements](#010657-webassembly-and-performance-enhancements)
- [\[01:08:36\] Foxglove's Role in Robotics Simulation](#010836-foxgloves-role-in-robotics-simulation)
- [\[01:12:30\] Challenges and Future Directions in Robotics](#011230-challenges-and-future-directions-in-robotics)
- [\[01:18:48\] Opportunities in Robotics Tooling](#011848-opportunities-in-robotics-tooling)
- [\[01:24:55\] The Shift from Open Source to Closed Source and Foxglove 2.0](#012455-the-shift-from-open-source-to-closed-source-and-foxglove-20)
- [\[01:41:59\] Actuate Conference: Bringing Robotics Developers Together](#014159-actuate-conference-bringing-robotics-developers-together)

## [00:00:00] Episode Introduction

[00:00:00] **Audrow Nash:** How can we make it easier to build robots? Good developer tooling is a great start, and one of the biggest parts of tooling in my mind is visualization. In this interview, I talk with Adrian Macneil, who is a co founder and the CEO of Foxglove.

If you're a robotics developer, you probably know them and use their visualizer. If not, you probably want to check it out. 

What you may not know is Foxglove has a whole data infrastructure from recording data to getting it off the robot and selecting which data you want in the cloud. And of course, their specialty, visualizing it, which works for live data and recorded data. 

In this interview, we talk about all the parts of Foxglove and how they fit together, opportunities for startups to build robot tooling, Foxglove's 2.0 release and their decision to move away from open sourcing their visualizer, and Foxglove's upcoming one day conference, Actuate. 

Actuate looks like a blast . Its goal is to have conversations where robotics companies can share their learnings kind of like what's done at academic conferences, but with more of an industry focus.

If you do decide to go, you can use the code Audrow, A U D R O W, to get 20 percent off It's not a referral, I don't get anything if you sign up, but I'm flattered to have a promo code. Anyway, I hope to see you there. With that, here's the interview.


## [00:01:28] Introduction to Adrian Macneil and Foxglove

[00:01:28] **Audrow Nash:** Hey Adrian, would you introduce yourself?

[00:01:30] **Adrian Macneil:** Hi Audrow, my name is Adrian Macneil, I'm the co founder and CEO at Foxglove.

[00:01:37] **Audrow Nash:** Awesome. would you tell me about Foxglove and how it came to be?

[00:01:42] **Adrian Macneil:** Yeah, absolutely. 


## [00:01:43] The Genesis of Foxglove

[00:01:43] **Adrian Macneil:** So Foxglove we think of as a visualization and observability platform for robotics. We've been around for about three years now as a company. Prior to Foxglove, I spent five years working in the self driving industry at Cruise in San Francisco. Worked on a lot of the internal infrastructure, internal tools, developer tooling, simulation infrastructure, a lot of those pieces at Cruise.

And really came out of Cruise feeling like there was this enormous, number one, there was this enormous opportunity for automation, and autonomy and robotics in the world, seeing if we can, put a car on the streets of San Francisco. how, many other sort of tasks are done by humans today that are dangerous, repetitive, difficult, that are honestly much easier than driving around San Francisco.

if we have self driving cars, how come we don't have self driving tractors in an empty field or, self driving forklifts in a factory yet? so I came out with this sort of huge excitement about what was possible with autonomy, but at the same time, really feeling that, the industry was being held back by a lack of tools and infrastructure and frameworks.

having seen kind of everything we had to build from scratch at Cruise. So that was the genesis of Foxglove was how can we push forward the robotics industry? How can we, build tools and infrastructure that really accelerate the industry? and we started with this, piece around visualization.

We started with, the Foxglove Visualizer, putting that out there, making it easy for folks to bring in different types of data, for example, from ROS. or very quickly, early on, we started adding support for other frameworks and other data formats like protobuf and things. and letting people bring this, multi modal data into a, into kind of a visualization framework, that was really where we started.

and this is a problem that's pretty unique to robotics and a lot of these kind of, ML workflows. If you think back to Traditional observability, you think about tools like Datadog or Grafana, they're really built around time series data, metrics, lots of plots, but no ability to show you 3D data, no ability to show maps, no ability to show point clouds or anything like that.

So we started with the visualizer and then over time we've expanded into this broader what we think of observability as everything from how you're logging on, a robot, how you're offloading data from robots, how you get it to the cloud, how you store and index it, and then how you can visualize and analyze that data.

[00:04:14] **Audrow Nash:** Yeah. So you're carving out a very nice vertical with this all around. All things data

[00:04:19] **Adrian Macneil:** Basically, yeah, we see the whole, data life cycle of, from your recording on the robot. because these are, things that are just, they work quite differently from a traditional Infrastructure space, right? Like I, I came to Cruise, I wanna say nine years ago or something at this point, from an infrastructure background, not from a robotics background.

And I saw how how much robotics engineers struggled with a lot of these things. But the traditional tools that had built up around sort of web servers and the web over the past couple decades did not immediately apply to robotics. 


## [00:04:55] Challenges in Robotics Data Logging

[00:04:55] **Adrian Macneil:** So you think about some of these things like, what types of data are being logged, I mentioned, right?

With websites, you're usually, the logs coming out of like a web server is typically, that's pretty lightweight in terms of data, you're generating a lot of text logs, and then you're generating maybe some time series metrics, things like, your server response speed, memory use, and CPU on the server, and things like that.

But it's like pretty lightweight telemetry in the scheme of things. and then, it's, and then this is deployed in a server room, so you've got this, we're deployed in a data center, we've got, effectively infinite bandwidth, and we've got, very lightweight kind of telemetry coming off web servers.

And then you go to robotics, and it's the complete opposite on both of those, right? You've got, instead of, very lightweight telemetry, you've got incredibly dense data, sensor data, video, you've got point clouds, you've got, all of this kind of data. It's very multimodal, it's very heavyweight, quite often.

and then. Almost universally terrible internet, or, some, 

[00:05:55] **Audrow Nash:** Yeah. 

[00:05:56] **Adrian Macneil:** not a data center, let's put it that way, you've, there's, you're either, you're in a factory, you've got Wi Fi, you've got shitty Wi Fi, you've got, or even if you, even if it's a fixed position robot and it's connected with Ethernet, it's still in a factory.

There's still maybe you're lucky if you've got a 100 megabit uplink or something. or we deploy it into a, field where you've got maybe like some spotty 3G service. you're getting into maybe Starlink if you're lucky, but you're not going to be streaming multiple HD video feeds over that.

So you invert on both of these spectrums. because of that. You can't just go and reach for an existing off the shelf observability Something like Datadog is just completely non applicable to the robotics space. And yeah, we just, we see this as something where robotics is, the needs of, robotics, engineers and robotics companies is unique.

and as, a specialized tool for this is important.

[00:06:54] **Audrow Nash:** Now I would love to go, I would love to go into each of the parts. of the you mentioned so you have the visualization logging transport like tell me about these

[00:07:05] **Adrian Macneil:** Yeah, absolutely. walking through an order of how we see the, data journey, the data life cycle. on a robot. recording is one of the, the first ones that we think about, right? 


## [00:07:20] MCAP: A New Standard for Robotics Logging

[00:07:20] **Adrian Macneil:** one of our open source projects at Foxglover is called MCAP. MCAP is a standardized kind of recording and logging format.

if you think about recording in a robotics context, probably the, sort of, The thing that a lot of people would be familiar with is ROSBAGS, and the ROSBAG sort of file format was designed along with ROS1, probably 15 years ago or more at this point, and, but it was one of the first formats that sort of natively supports recording multimodal streams of data, into a single file, and we think that this is a very important property, being able to take all of these different streams of sensor data, putting it into a single file, the alternative, and we've seen this at companies that sort of created pre mcap or, didn't use ROS early on.

the alternative typically ends up being a junk drawer approach to logging, right? So there's just a folder on the robot. there's some CSV, one piece of the stack is logging some CSV data. One piece of the stack's logging an MP4 file. One piece of the stack is dumping some random binary data to disk.

and then there's some YAML files thrown in for good measure. so this is junk drawer approach to logging. Now, great, now we get these logs off the robot. It's just like a folder full of crap. We zip it up and who knows, how you, go and, interact with that later.

but we think that this, nice property that ROS bags originally, Created as everything should go through a single format, even if it's completely different types of data, even if it's some of it's structured data, some of it's unstructured, some of it's, multimodal video point clouds, some of it's time series.

you want to put this all through a single long format, make sure everything is timestamped, consistent. That was a great property of ROS bags. but we saw, the, robotics ecosystem is broader than ROS. We saw a lot of companies struggling with, with where they were not using a ROS stack.

And therefore some of them weirdly converted data to ROS just for logging. Some of them did the junk drawer quite a few companies we spoke to had just invented their own sort of bespoke binary logging format. So we've just, we've created something internally. We just dumped these, this binary data to disk.

good luck interacting with any other services, or, good luck even reading your own files from a year ago, because who knows how that, how the format evolves. There's no kind of spec to it. so this was a problem that we set out to solve quite early on, back in 2021 with Foxglove.

We just, we saw this as, A key sort of problem in the industry that there were no open standards outside of ROS Bag that people were using for logging created the MCAP project, that actually got accepted I think maybe a year ago or a year and a half ago it got accepted as the default logging format in ROS2 which is great.

We're seeing a lot of adoption of MCAP within the ROS community, but also, a lot of adoption of MCAP outside of ROS2. There's a number of some of them I think on the MCAP website. Logos that you'll see of big companies. I don't want to name ones that I'm not allowed to. So I'll just have a look at what's actually listed publicly on the website.

got, yeah, there's some ones here like Andoril, Dexterity, Coco, Apex AI, Tangram, Wabi. So there's a few of these, really large companies, both within and outside of the robotics ecosystem that have, adopted MCAP. So that's, how we think about the logging piece, right?

And because the logging pieces on your robot. that needs to be open source, that needs to be a completely open standard, open framework. MCAP has libraries in about six different languages. There's, C and Python and Rust and JavaScript and Go and anything that people are using on robots.

[00:11:05] **Audrow Nash:** does it 

[00:11:06] **Adrian Macneil:** and 

[00:11:07] **Audrow Nash:** like so how would you describe at a high level how does mcap work and how does it unify things and why is it better than rossbag

[00:11:14] **Adrian Macneil:** Yeah, you can think of MCAP as a successor to ROS1bags. so ROS1bags, was a file format where it can take basically all of the channels of ROS data, and save them into a single file format. Every message that goes in is timestamped. There's an index at the end of the file in the ROS bag that sort of helps you if you need to seek around and things within the file.

But there was a few sort of, Challenges. The ROS one bag format was not bad. a few challenges that people had with it. One is that it was tied to the ROS ecosystem. not just, in two ways. One is that you could only log ROS data to it. So if you had other data, you've got some protobuf data or some just other sort of generic data you wanted to save.

you were back to the juncture approach, now you've got to save that separately. another way it was to ROS ecosystem is that the, ROS, whatever Bagpile, whatever, the libraries to interact with it are also only available through the ROS repos. You can't just like pip install a general purpose package that would let you interact with it.

And this becomes a problem in, And, ML like further on in your robotics development, you've got ML pipelines, you've got ETL pipelines. You've got, you want to do post processing on the data. You don't necessarily want to install like all of ROS, or set up the ROS repos or any of this kind of stuff.

You've just got a standard sort of, Python app that you've written and you want to just pip install something interact with it. That was not possible. in the past with ROSBags. So you had, a couple of these challenges, and then in the early days of ROS 2, there was a switch to, a SQLite based, logging format, which, it's, unclear that sort of some of the design decisions and people behind the history of how that decision came to be has been lost, I think, to the, sands of time.

was one, it was, it appears to be a decision that was made in the early days. of ROS, but, and I think the intent behind the SQLite login format was to bring it as I mentioned, ROSbags was hard to interact with outside of the ROS environment. The intent was like, hey, let's use an existing open standard SQLite.

There's plenty of readers out there that would let you unpack that. Unfortunately, the downside of that is that SQLite is a relational database, so it's not designed for, high performance stream, append only logging or anything like this. It's not, in terms of how you think about inserting a row into a SQL database, it's hyper optimized for jumping around and, and inserting rows arbitrarily and updating indexes and all of these things that, are not at all necessary when you've got a stream of log data that you just want to flush to disk as fast as possible.

so people were seeing a lot of problems with that. Notably, it would basically just drop a lot of messages, if it ran out of CPU or, the CPU was being too taxed, it would just start dropping messages, and then they would not make to your log file, there were some challenges being faced there, and then, yeah, with MCAP, the design of the MCAP file format is quite similar to MCAP, A ROS 1 bag.

The other analogy I would say with an MCAP file is it's similar to an MP4 file. So an MP4 file, people think of as a video file, but it's not actually. An MP4 is just a container. You can put anything inside it, and inside the MP4 file you're putting streams of typically something like H. 264 encoded video, plus some, AAC encoded audio, or whatever.

MP3 encoded audio or any of these kind of things, right? So it's a container. MP4 is a container format Just like Matroska is also a container format, MKV These are containers and then inside them you have channels of audio and video MCAP is similar to that except inside it you can have channels of anything.

You can have channels of ROS messages, you can have channels of CDR messages from, ROS2 and DDS, you can have channels of protobufs, you can have channels of flatbuffers, you can have channels of JSON, whatever you like. So think about it as just a container format, everything that goes in the container, is timestamped so that it fits into the sort of stream that you're writing.

and yeah, then you can go and unpack that later in. Like I said, the libraries are available kind of independent from the ROS ecosystem. even if you're using it within ROS, that's a nice property.

[00:15:40] **Audrow Nash:** Yeah. Okay. That sounds really nice. So you have this container where you can store all these different channels, you can pull them out really nice. And then you also have different language support that don't, that doesn't require you to use, or install ROS on ecosystem, use Ubuntu or Windows or whatever.

whatever it's supporting, but it's a heavy dependency. And so that's, very nice. and that, that probably makes it a lot nicer for, as you were saying, like ML pipelines, people who are doing data analysis, they don't need to maintain a working ROS distribution on their

[00:16:19] **Adrian Macneil:** Yeah, even within Foxglove platform, some of our backend services that ingest MCAP files or stream MCAP files are written in Go. for example, and they have no dependency on ROS. We're not running on, on, Ubuntu 2004 or outdated version of Ubuntu tied to a specific ROS distribution or anything.

It's just, hey, we've installed the mcap go package and that has the, has everything you need to interact with it. So you have this sort of like level of independence that I think is, 

[00:16:45] **Audrow Nash:** Very desirable.

[00:16:47] **Adrian Macneil:** and then of course you still have the, tight ROS integration for people that are using ROS.

[00:16:52] **Audrow Nash:** Definitely. Okay. and so that's the recording part. So you're putting it in a format that you can use. So MCAP, does it refer to anything or is it an acronym?

[00:17:04] **Adrian Macneil:** it's, unofficially it's Message Capture, which is a play on PCAP, which Packet Capture. we don't expand that anyway, we call it MCAP, and, it was, yeah, we went through, had a sort of internal voting on about 50 different names, I think, but MCAP, MCAP, I don't even remember what the other suggestions were, this was three years ago now, but, But yeah, there was, yeah, I think MCAP kind of stuck out as, being, philosophically similar to PCAP files, which are a network file format that allows you to capture all of the packets going out on your sort of IP address, through, a GCP IP stack. You can capture all of these, all of the packets going forth and then you can go and inspect that later.

We're thinking this is not, This is a higher abstraction, right? It's not at the level of individual packets, it's at the level of messages, ROS messages or other messages in a PubSub system.

[00:18:00] **Audrow Nash:** Nice. I like that. And it also makes sense because maybe people familiar with PCAP can map over their understanding and it's just, it's a different

[00:18:10] **Adrian Macneil:** yeah. It's, yeah, it's, conceptually similar, although mostly it's just a catchy name. And then at some point, some point, one of the team members threw in the, the hat logo, caught on. And, and that was a little bit of a dad joke that made it in with, yeah.

[00:18:31] **Audrow Nash:** Okay. So we have MCAP for recording. Where do we go from there?


## [00:18:35] Data Upload and Ingestion in Robotics

[00:18:35] **Adrian Macneil:** got to get the data off the robots. So this is how we think about as, upload and ingestion. As I said, within the robotics space, usually you are logging very, dense data and then you've almost universally got a, pretty limited internet connection. bandwidth constraint is just a universal problem in robotics.

so how do we get the data off the robot? during early R&amp; D, this is not, As, it's not really as much of a problem people run into, they just, they log in on the robot, probably the robot's right in front of them, they, hook up an ethernet to the robot and SSH and copy some files off, or, they just plug in a portable hard drive to the robot and, off they go.

As you start getting to robots in the field, you start getting, the robots are not deployed where your engineers are, where your team is, so you want to start debugging data, you're not going to have like your entire engineering team on site at wherever the actual robots are being deployed, even the first few, and certainly once you get to scale of thousands or tens of thousands of robots, you're going to have them deployed all across the country, all across the world, and you're going to have your engineering team is, going to, possibly be in one place or possibly be distributed, but probably not where your robots are.

how do we get the data off? first of all, it depends what, data you want to get off. We see a lot of people, eventually move to some kind of rolling record, type setup. So This, might involve having a day or maybe max couple days worth of data logged on the robot. You've got enough storage space on there for, 24 hours of log data, say.

But you're just overriding it, unless something goes wrong, unless there's something notable. 

[00:20:18] **Audrow Nash:** like a home security system or

[00:20:20] **Adrian Macneil:** yeah, exactly, yeah. It's if someone breaks into your house, you got to go quickly pull the tapes out before, Yeah, or you're like a, a black box recorder in an aircraft or something like that.

and then why, and then you, but you do want to capture the data if it's, for example, something went wrong, obviously, like robot, crashed into some, like packaged goods or the fell down the stairs or whatever the robot was doing wrong. Those are obvious ones. The other areas that you might want to capture data are things going well.

You want to just capture, a distribution of data for your ML training, things like that. you need, you want to get a nice distribution of, different events. but we usually see people moving towards some kind of, rolling record type setup. The exception to that, would be, companies that are operating in public, so self driving cars, but also things like cyborg delivery robots and things like this, there is usually a higher, there's usually a desire with those types of robots to save it for more than just what you could fit locally, probably more than a day, right?

You want to have, Keep keeping most of the data around for a month or a few months or something like this in case someone calls up and says hey you cut me off on my bicycle I'm suing you or something like this you want to not say you know it may be weeks later that you find out about a potential incident so we usually 

[00:21:49] **Audrow Nash:** they generate so like autonomous cars at least so much data. So I imagine they need to offload it because they can't store it because 

[00:21:58] **Adrian Macneil:** yeah, so yeah, yeah, so in the AV industry, and it's a maturity curve, you get to the point that, that sort of like at Waymo is at today, and you're absolutely going to see a rolling record and not saving everything that's happening, but until you reach that level of confidence, for, all of the early years, it's usually something that looks like, logging to port of logging to hotswap hard drives on the car.

And then when the car is coming back to charge or to fill up or be cleaned or whatever service, we're just popping those hard drives out and, switching them out for fresh ones. from there, of course, you still got this just ridiculous quantity of data because, self driving car can be logging multiple terabytes an hour easily.

so you got to get all of that data. Off a car and up to the cloud that requires a pretty extreme internet connection. But yeah, that's the AV use case is a little bit unique in that world. One where you're operating in public and you're a lot more sensitive things Potentially might have gone wrong that you might not find out about.

You don't see that as much in a warehouse AMR or something like that. Usually the amount of damage that an AMR can do driving at three miles an hour in a warehouse is fairly limited. And also a lot of the time, a lot of these warehouse AMRs have a lot of people around, they have buttons on them where you can report incidents and things like this.

So you might be perfectly happy just saving a couple minutes. maybe a minute or two minutes of data every time there's something notable then just throwing the rest away.

[00:23:36] **Audrow Nash:** Okay. So back to this data upload problem. what do you guys have in place? So I guess there has been this, what people have done is they often record the data in place and, or, but I guess if you want it for machine learning and so you want to train on that data, you want to get that data off.

connectivity is very bad general or not very bad, right? Generally, but often can be very bad. so how are you guys solving this or what's your approach to getting data off the robot

[00:24:13] **Adrian Macneil:** Yeah. exactly. And so we offer, and I think there's, a lot more to build out here over time, but we offer a agent that you can, we call the robot agent. You can drop it on a robot. and then it'll watch a directory of, log files, of MCAP files or bag files. So let's say you're running a ROS robot or a ROS like robot.

It's recording a lot of data, to MCAP files, to ROS bags. those are typically getting, the files typically get rotated every sort of 60 seconds to a few minutes. Quite often people are splitting the files up every few minutes just to, to, to make them easier to work with. we have an agent that'll sit there and just watch that directory.

keep an eye on new files that are coming in. and it notifies the server and the cloud about what files are available. and then, we, have an understanding that, hey, you've got this of robots out there, they have these, this data is available for import, from the edge. And then, you can trigger an upload in one of two ways.

You can either do it from the robot, so you can, send a message to the on, to the robot agent, say, flag, flag this particular file, or say, can you queue that for upload? or you can do it as a pull based mechanism from the server, from the cloud. So I can go to the web portal, I can click on that robot, I can see the timeline of data that's available.

I can't view it yet. I know that there's data there, but I can't, I don't know what that data is. But I, might, the, pull based workflow, the push based where the robot initiates it is great when the robot identifies something wrong because the robot identifies that there's been a collision or the robot identifies some other kind of error that it wants to report.

It can trigger an upload. The pull based workflow, where the user is going to the cloud and requesting it, is good when they get a call from the operations team saying, Hey, at 2pm this afternoon there was this incident with the robot, can you guys take a look at it? You might want to go in and fetch, just grab 10 minutes of data around, around about when a, some problem was claimed to happen, and then offload that, pull it, From the, yeah, from the robot and have that sent to the cloud so that you can then go investigate.

[00:26:24] **Audrow Nash:** Okay. So you're not doing, it's not towards like dashboards

[00:26:29] **Adrian Macneil:** Yeah, no, we we've yeah, exactly. We've, stayed away from that. there are a lot of tools that do that already. you've got, Foment is probably one of the most known ones, but, in all, but there's, there's a lot of these tools that are creating, more of a live overview.

I call it like a management platform. we don't do anything in the fleet management space. it's, a little bit It's a different problem category, I think, to what we're solving, we're focusing on the needs of robotics engineers, robotics developers, and getting, what is usually, async access to raw, detailed logs about incidents, versus a fleet overview, which is more of an operations workflow of just hey, I want to see where my robots are.

I want to click on this one and send this one home. I want to see how many, tasks per hour are being completed by different robots. this kind of stuff is, yeah, it's, a different kind of product category and problem space. It's adjacent to what we're doing, but it's not something that we have focused on now and we're unlikely to be focusing on in the near future.

[00:27:40] **Audrow Nash:** Okay. So that sounds cool. So you basically, you have something that you have your agent is watching a folder and it's letting you know when there's something there and you can pull it from wherever, whatever computer you're on when you're not close to the robot or will push it or it can push it periodically.

and it's really just, you're going to upload the whole thing when it's pushed or pulled, to wherever it is that it should be sent

[00:28:08] **Adrian Macneil:** Yeah. And snippets of data. there's different ways to configure this. Sometimes people, sometimes another, pattern see sometimes is, people will actually log two separate sets of, MCAP files, on their robot. They'll be logging one that's all the lightweight telemetry on their robot.

So things like just the robot pose, maybe GPS position, system state, just stuff that's like very lightweight, and then a separate file that's logging all of the heavyweight sensor data, the video, the point clouds, anything like this. the beauty of that setup is that you can actually just always upload the lightweight stuff.

So you always get some amount of detail, not immediately because it's still an async batch upload workflow, but at some point within maybe 10 minutes of, real time, five, five to 10 minutes, you're seeing enough data that you can, figure out where a robot was at any point in time.

That might help you narrow down on, say again, someone calls you up and says there was a problem at 2 p. m. That will help you narrow down on exactly when that problem was and roughly where the robot was. Then you can select a time range and go and download and upload the, fetch the more sort of detailed HD logs.

So that's quite a nice pattern that we see, 

[00:29:23] **Audrow Nash:** that is a really cool one.

[00:29:26] **Adrian Macneil:** But yeah, you do all of that, and then your data gets to the cloud, right? Yeah. and again, all of these, one of the philosophies of how we build Foxglove is trying to make this really modular, because not everyone wants all of these pieces, right?

Some people have already figured out their logging, some people have already figured out their upload workflows, they don't need help with that. but, others haven't. We just say, pick and choose the components that make sense for 

[00:29:49] **Audrow Nash:** Yeah. So you support the full vertical of like I record my data to, I do an analysis on my data. but, or whatever it might be, I use it for training. but you can use it for only specific parts. So if just want to upload the data or if you just want to visualize the data or you

[00:30:09] **Adrian Macneil:** yeah, if you just care about uploading and organizing your data in the cloud, that's a, thing you can do. Typically we find the, you get to the sort of last part we'll get to around visualization analysis. Usually that, those workflows are pretty common across everyone.

but yeah, absolutely a lot of People have come to us and initially wanted to focus on the data workflows and then they get into the visualization. Sometimes it's like start with the visualization. I'm happy with how I get data off the robot. I just want to visualize it. Great. That's fine.

We can start at that end. but yeah, as we're getting all of this, we're triggering these uploads, we're getting logs coming off the robot. 


## [00:30:46] Cloud Indexing and Data Management

[00:30:46] **Adrian Macneil:** then, you get to the data in the cloud and again, We see a lot of, robotics companies, at least pre Foxglove, was just, there's an S3 bucket, we've got an Amazon S3 bucket, we've dumped a bunch of bag files in it, or something like that.

so if you know what file, you know the file name you're looking for, great, but if you don't, good luck to you. so that was, the, the problem we set out to solve with the cloud indexing was, Okay, as these files are coming in, let's, let's do an ingestion step where we look at metadata on the file.

We look at what time range is being covered by this file. We look at what robot it came off. what topics are inside the file. we go through this ingestion step, and we store all of that in a nicely organized indexed, bucket. Either we can, either Fox Club hosted or it can be hosted in your own, your own VPC with any cloud provider.

but we, go through this ingestion step. We organize it into a nice sort of folder structure within your bucket. And then we also give you a web UI so that you can search across it, right? You can, just go in and type in and search metadata. You can look at a timeline view. You can do a few more of these things to, a more, sort of like visual overview.

if you want to look up, you know which robot you're looking for, and you know the time range, or you don't know the name of the file, it's much easier to find the sort of particular logs that you're looking for.

[00:32:08] **Audrow Nash:** Yeah, I feel like this is something that's so simple and so valuable

[00:32:13] **Adrian Macneil:** yeah, and everyone has, and, I don't claim a lot of the stuff that we do, it's not rocket science, it's just really undifferentiated, because you see every company build a web UI for looking at ROS bags or something like this, and you're like, this is just silly, everyone shouldn't need to build this.

[00:32:31] **Audrow Nash:** Yeah, for 

[00:32:33] **Adrian Macneil:** yeah, 

[00:32:34] **Audrow Nash:** And then a UI for filtering through the data. yeah, I'm seeing a lot of, analog to like home security

with this, 'cause you can look for this camera at this

[00:32:46] **Adrian Macneil:** right, pull 

[00:32:47] **Audrow Nash:** look for this robot from this time window. and you might be able to filter by a specific event or something that occurred, but so you're pulling out metadata.

By is very simple by processing, what has been uploaded. You get the start time and time. Maybe you key or tag it with things like this is this robot in this warehouse this

and 

[00:33:09] **Adrian Macneil:** Yeah, can, yeah, tag all of that assign it to what we call a device, which is your robot, and then you're able to view all of that data on a timeline, or you'd be able to pull up just the logs for particular. just for a particular robot, or if if you are tagging them with metadata, such as which factory or, which site it was operating at, tag it by that kind of metadata as well.

but you've got this, this, kind of quick search across all of the data. 

[00:33:37] **Audrow Nash:** it. Okay. I think that's really nice. and that feels like something where companies might plot along in their like terrible naming convention. Like the file

[00:33:47] **Adrian Macneil:** It's got the robot 

[00:33:49] **Audrow Nash:** where It's this is the robot. Yeah. And then, that is probably, it works, but it's super painful.

especially as you get a lot of robots and, a lot of data. And then this makes it so much easier. And then you have the UI, which is really nice for filtering and things okay. 

[00:34:07] **Adrian Macneil:** a lot more that we can do there too, today we let you search by metadata that you've pre added, some of these things like you said by robot or by, other metadata you had like factory and things, but there's a lot of other ways that you could imagine exploring this data, one we would like to add in the future would be a sort of a geospatial search over, 

can I see all of my data on a map if you just see like a heat map and then say in and okay, I want to pull all of the logs, all of the times that we've been past, whether it's an indoor map or an outdoor map, it's not, similar kind concept, but I want to pull all of the logs that I've, or all of the times that robots have been to this corner of the factory or they've been through this intersection or things like that, those types of searches, are things that we would like to add the future to make it, really easy to, pin down on the particular data that you're looking for.

[00:34:59] **Audrow Nash:** Yeah, I feel like you have, there's a lot, I mean you could do a lot of analysis, you could do a lot of displaying stuff, it's, the ceiling's the limit for what you could do to expose different data things there, but that seems very valuable. Spatial seems super valuable, specific events could be valuable, having them write their

[00:35:19] **Adrian Macneil:** Yeah. 

Yeah. Yeah. We do it. Yeah.

do have an event. Yeah. We do an event concept. So you can whether whether those are being created through the API from things that are happening on the robot or whether it's being created, you can just go into the UI and annotate your own events, manually, but tagging, tagging points in time where notable things happening.

And

[00:35:39] **Audrow Nash:** the super cool. Okay. So we have this cloud indexing, so you're able to get your data very effectively. where do we go from there?

[00:35:50] **Adrian Macneil:** Analysis and, in particular visualization. 


## [00:35:53] Visualization in Robotics

[00:35:53] **Adrian Macneil:** so visualization is, like I said, this is where we started the end of the problem that we started 

[00:35:58] **Audrow Nash:** Yeah, I think in our last interview, which might have been two

[00:36:02] **Adrian Macneil:** was a it while ago. Yeah.

[00:36:03] **Audrow Nash:** point it was most of what you had was the visual visualization and you probably were working on the cloud part and it was pre mcap

if i remember correctly so okay yeah time

[00:36:16] **Adrian Macneil:** Yeah, it does. Yeah. a lot has been built in the past, past few years. but yeah, so we started with this visualization. and again, another difference between sort of observability with, servers and traditional infrastructure versus robotics, and traditional infrastructure, again, you think of a tool like a Datadog or Grafana or something like this, you're creating a lot of nice pretty plots and dashboards and things, but usually only with data that's already in the cloud.

this is, why the, the arc of data goes from like logging to get it to the cloud, to indexing, to visualizing it. but in robotics, visualizing cloud data is only one of, I would say three kind of common workflows, right? So one is visualizing cloud data. Another is visualizing local files.

I've just got, some files that I've, off or, SCP'd off a robot or not uploaded or I'm around locally. another is live visualization, so I'm this could be either, I'm connected to a robot over Wi Fi or Ethernet, and, I'm literally just plugged into a, robot and I want to see the data coming in live and I want to check that, the colorations are correct and that the data makes sense, or, another, option with the live one is if you're running some kind of re simulation or some kind of simulation on your, just on your local workstation, your local laptop or desktop, and so you've got a robot stack running, you might not have an actual sort of full, hardware in the loop or anything, it's just running, a stack locally, but you still want to be able to see the, output of, what your stack thinks is happening, what your stack thinks is seeing.

[00:37:57] **Audrow Nash:** i'm thinking very similar to RViz this

for 

[00:38:01] **Adrian Macneil:** yeah. And Rviz, really only supports the, live visualization workflow. So when you want to visualize things with Rviz, you can connect to a live running ROS. You can see that in real time. But if you want to go and replay, if you want to go and explore a BAG file or MCAP file, You have to separate, you have to go start up ROS in the background.

You have to start up, run ROSBag play. So you've got five different kind of terminal windows in the background with your ROS stack running and your play running. And, then if you want to pause and rewind something, you've got to do that sort of in the terminal

[00:38:34] **Audrow Nash:** it's a pain. 

[00:38:36] **Adrian Macneil:** which is so there's no, with something like Rviz, you have no native support for a kind of, for a file based or a cloud based, replay workflow.

You only have this kind of live visualization.

[00:38:47] **Audrow Nash:** Now, one, one thing with RViz is it's running on your local machine. I know Foxglove can be but running through Electron or however you're displaying it these days. but so RViz might be more performant, would you think? 


## [00:39:05] Performance and Platform Considerations

[00:39:05] **Audrow Nash:** So if data is coming in really fast and you want to display, or does it not matter because it's human perception

[00:39:10] **Adrian Macneil:** Yeah, it really depends, yeah,

[00:39:13] **Audrow Nash:** how do you think about this?

[00:39:16] **Adrian Macneil:** it, depends a lot, right? in terms of, the rendering, our 3D rendering and things like that's all running through WebGL. a lot of the things, a lot of the things are actually already hard or accelerated. A lot of the code in a browser environment, people think about a browser environment, The browser has evolved a lot in the past 10 years, right?

You've got companies like Figma and things that are really pushing the boundaries of what's possible. you've got services like we're using now, services like Google Meet, things like this where they're doing like live video and streaming and things in the browser. Most of that code that's running is C code, right?

Like most of it is running in the background of the browser stack that's implemented in C and you're just triggering it from JavaScript. the same is true with a lot of this 3D rendering, right? So a lot of the stuff that's happening in Foxglove when you're looking at a 3D, View, like you would see in Rviz, you are, that is.

that's running through WebGL, which is then being, like, in most cases, hardware accelerated. Same when we do things like H. 264, like video decoding and things like that. There are actually, these days, there are browser APIs that will let you use hardware accelerated decoding for video and things like that.

So we leverage a lot of that.

[00:40:28] **Audrow Nash:** That's awesome. Yeah, it's so cool. It's like a rising tide lifts all boats. You get to benefit from the massive investments going on into the browser.

[00:40:37] **Adrian Macneil:** Yeah, and it's a great platform, right? the browser is very extensible, it's very easy to develop with, it's, we can let people, it's pluggable, right? We can let people create, plugins and things very easily, or create little forms and things like that, that they want. and then also, the other thing with Rviz is, this sort of, mostly gives you the 3D panel, right?

If you want to do things like plots, you're popping out to a separate like RQT or your plot juggler or things like that. you don't you can't just bring it, or maps and things like this, you can't bring it all into one, into one. 

[00:41:11] **Audrow Nash:** a bunch of windows open for 

[00:41:14] **Adrian Macneil:** but the performance, the performance thing is, not a, a major thing that comes up.

It really depends on what people's data and workflows look like. And there's such a variety within, within the robotic space that you, just, it's, hard to say concretely like X works better than Y, without looking at type of data that people are trying to use it with.

[00:41:38] **Audrow Nash:** very Was this the case before, say three, two years ago or something when we talked? Because I remember, or maybe it's just the general perception that because it's a web app, it can't have good performance. and it's surprising to me and very nice to hear, that you're getting wonderful performance and it's hardware accelerated

[00:41:58] **Adrian Macneil:** yeah. It is, I will say there's like a lot of stigma around, out there around kind of Electron apps things like that. but I think in, some, in some cases Electron is like a victim of its own success, right? it's, it's created a platform that, is, so easy to create.

Cross platform applications with, without having to go into, some of these more esoteric, yeah, like problems that, yeah, have on specific problems, for specific platforms. There are actually some, sort of, Other alternatives that have come out more recently, there's one called Tauri, or Tauri, I'm

[00:42:39] **Audrow Nash:** looks

[00:42:39] **Adrian Macneil:** Tauri.

So this this is a middle ground, right? It's it's still letting you use the web stack to create an application, but it's using the, OS specific built in web view components. the nice thing about that is, is, it reduces the file size that you're downloading and having to ship a, specific version of Chromium, that build.

this, that is also its biggest. Downfall, right? Because the nice thing about, the way that we package and distribute Foxglove is that every, we can guarantee that you're, it doesn't matter you're on Ubuntu 18 or 20 Windows or Mac or Windows 10, Windows 11. We're not trying to guess at what a web viewer, a native web viewer is doing.

we're not dealing with the problems like Safari is actually like really behind on a lot of, edge web features, for example. We're not dealing with hey, this problem that only seems to happen on Mac. the, very occasionally 

[00:43:36] **Audrow Nash:** better for you guys as developers too. You have far less maintenance burden. and like ROS, we, just as a developer on the robot operating system, it's every time there's a problem on Windows, no one wants it. 

[00:43:53] **Adrian Macneil:** No yeah, And then also it's good luck if you're on a Mac, it's basically unsupported. they call it tier three something, but, yeah, 

[00:44:01] **Audrow Nash:** build from source, but we don't

[00:44:03] **Adrian Macneil:** exactly. Yeah, yeah. So this is, these are huge benefits, especially when you're a small team trying to focus building a great product.

I will say performance, and, issues come up from time to time and customers bring them to us and it's usually a case of looking at just specifically what's different about their data and how can we, improve that. It is a thing that, that we spend ongoing effort on, and if folks do have problems, we encourage them to bring them forward because it's, like I said, sometimes it's, it's hard to know if someone has a, an issue like where exactly that's arising from.

[00:44:39] **Audrow Nash:** Definitely. Okay. So we have going back to visualizations. Okay. And it is an Electron app, which you

[00:44:47] **Adrian Macneil:** correct. Yeah, we, built it as a, yeah, built it as a, web application. most of our users are on desktop actually, I think from memory, it's, like a majority of people are using the desktop app more so than the, than actually using it in the 

[00:45:02] **Audrow Nash:** through the browser,

[00:45:04] **Adrian Macneil:** about the desktop app can just install it and it works on any platform.

but 

[00:45:09] **Audrow Nash:** cool.

[00:45:11] **Adrian Macneil:** so, yeah, we, have, that, and I guess, we're saying this word visualization, which I assume to like most sort of roboticists is a sort of familiar concept, but, surprisingly, surprisingly unfamiliar outside of robotics, right? People you go to an average VC and say we make robotics visualization tools.

you'll get, a blank stare, right? this is not a, a that

[00:45:34] **Audrow Nash:** what do you need to visualize?

[00:45:36] **Adrian Macneil:** Right, what do you mean? Who would use that? Why they, get all these questions like, why would I use that a robotics developer? I don't even know how to explain it. I was like, fact, 

[00:45:47] **Audrow Nash:** to realize how much in our

bubble we are the idea that's not clear is, surprising to me too. And I suppose you talking to VCs, this is something that's really come up they're out of

[00:46:00] **Adrian Macneil:** Yeah. Yeah, that and, yeah, because, every industry has its, sort of, its, uniquenesses, but I think, as, especially as you look at, investors and things, a lot of the times, industries are a bit more mature and they're a bit more mapped out and they can go and see these little, logo clouds and understand how all the things work together.

Pieces fit in and they Oh, you do a thing in XYZ category. And then you pop up in, in a category that, that's not represented on their little logo cloud. And, you have to explain from, sort of first principles. But I do, I I, do think, and if anyone, listening is not a robotics developer, visualization is something that is critical to robotics development from day one of your very first robotics hobby project.

We're working on, autonomous robots in space or autonomous vehicles or autonomous trucks and production, right? it's a thing that, you put together your first toy robot and then you, the first thing, and you stick a camera on it, the first thing you're going to want to do is like, all right, what can I see the data coming out of the camera?

can I see, like, where this sort of robot thinks it's, it is in its, surroundings? You're doing some, slam, or you're doing a 2D LiDAR, or, even the most basic robot, you immediately run into this problem of how do I visualize, what the robot is seeing and thinking?

And 

[00:47:19] **Audrow Nash:** Yeah. How do I, check where I am or where the robot

[00:47:23] **Adrian Macneil:** And it's an inherently multimodal problem. It's not something that you can just look at text logs or, plots and things to understand. you need to be able to see across all of this data. You need to see in 3d space, a model of the robot and what it thinks its surroundings are.

And things like, lidars and radars that are giving you a sense of depth and space. And then you also want to see video data coming out of cameras. You also want to see, GPS data on a map if it's got a GPS. You want to see you do have a lot of like plot data.

You want to plot things like joint sort of positions or motor torque velocity, things like this. You do have text logs as well, but you have all of this, right? You have plots, you have text logs, you have maps, you have 3D, you have cameras, and so you need a tool that is inherently a sort of multimodal visualizer and that's what Voxlog does.

[00:48:17] **Audrow Nash:** yeah. Yeah. So it makes it so you can. Understand the state of the robot so you can understand what it's doing, so you can develop things, so you can understand what might have gone wrong or see if there's any errors or anything. lots of use 

[00:48:37] **Adrian Macneil:** if, I, you could say that it helps you see what the robot is, how the robot sense, think, and acts.

[00:48:45] **Audrow Nash:** Yeah, very

[00:48:46] **Adrian Macneil:** it's, yeah, it's what is the robot seeing? What is the robot thinking? how do we understand, what is the robot thinking, which is usually what is the robot's kind of mental model of the world and what are the actions that it is planning on taking?

Yeah.

[00:48:59] **Audrow Nash:** cool. Okay. What are so thinking about visualizations? You've mentioned several But what are like the big? Classes of visualizations. I'm thinking like you have your plots you have your 3d One where you have the point clouds and maybe your robot model something like Rviz and maybe then you just have logs that say messages that you want to introspect something, how do you think of the big classes of you might

[00:49:33] **Adrian Macneil:** Yeah. Yeah. 3D, 3D and images are definitely One of the larger buckets, all of these things are critical, right? But I would say like 3D and images. So we have, a panel for visualizing 3D data. And we have a panel for visualizing 2D images. They're actually the same panel under the hood, this is a fun fact.

So the 3D, we have a panel for, the, 3D scene can render anything from a 3D point cloud, a 3D, bounding boxes of objects, like you said, a 3D robot model, and the robot's pose, so like where it's holding its arms or joints, things like this, also in the 3D panel, you can render a 2D image into that scene, right?

So if you've got a camera mounted on the robot, you can project that, that camera image into, 3D space to see, what it is seeing from that perspective. conversely in the image panel, you can start with a layer of what is an image that we're seeing. So this is just like 2D pixel coordinate space.

but you can project into that image anything from your 3D scene as well. So you can project Over it, point clouds. As long as you've got transforms, right? As long as we understand, the frame of of camera and the relationship between your camera and your LiDAR or things like this, but we can project over the camera, point clouds.

We can project over the camera bounding boxes. So you can actually see anything from the 3D scene in the 2D scene, you can see anything from the 2D scene in the 3D scene, and the, even though the, the, UI for them is slightly different, they're actually like the same piece of code under the hood.

so that's one. really big bucket, I would say. And then the other, main, or big, one that's just like heavy uses of plots. so plots are just, very important, obviously for time series data. lots of different sort of types of things that people are trying to look at there.

But, yeah. this can be things like encoders, motors, joints, there's, any number of any, sort of numeric, any time series data that you've got, you can plot there. or not time series, you want to plot things like, planned velocity in the future, or, you want to plot sort of movement even in 2D space, all sorts of things that you can do with plots.

And then, yeah, other ones that get. 


## [00:51:54] Extensibility and Customization

[00:51:54] **Adrian Macneil:** but there's, we have about 20 different types of visualizations that you can do in Foxglove and an extension API that you can create your own visualization panels. but the raw message run, think you called out, so just being able to inspect a specific, again, in the ROS world, you can do this by opening yet another terminal window and doing rostopic echo.

you still got, look at like an average ROS developer workspace. There's always like five terminal windows and like three, and Rviz and RQT and, there's just like 18 windows rearranged. we want 

[00:52:24] **Audrow Nash:** they all have their

[00:52:26] **Adrian Macneil:** we want we want to eliminate this.

yeah, so we have the, what we call the, raw message panel. That's basically like a ROS topic echo. It just lets you see, inspect individual images and pause them. we have an out, like a, GPS map and outdoor map that gives you that's a one that's quite helpful if you've, if you're 

[00:52:48] **Audrow Nash:** Or outdoor.

[00:52:49] **Adrian Macneil:** for outdoor types of robots, you just want to, to display that on the map and, sometimes there might not be coordinate mapping from the GPS data to your 3D data, so you can't necessarily, you can't necessarily just like drop in a street map or a, or like an open street map type thing into your 3D panel, but you do want to see where the robot is in space.

and yeah, bunch of other things like that. Diagnostics, a lot of these kind of things. Text logs.

[00:53:20] **Audrow Nash:** Hell yeah. Do you, is there any, does Foxglove, visualization, does it fully replace Rviz and RQT or are there any missing?

[00:53:33] **Adrian Macneil:** yeah, great question. I would say, it's probably impossible to fully replace Rviz for 100 percent of people's workflows in that some people, I guess a couple of buckets of things I'll call out. One is people that have created custom Rviz plugins. we don't have any way to Automatically import or

[00:53:54] **Audrow Nash:** under everything and guys are

[00:53:55] **Adrian Macneil:** QT codebase and we've got a web stack. We do have extension APIs, extension concept. You can publish extensions either publicly or internally to your sort of Foxglove organization. but you're not going to be

[00:54:09] **Audrow Nash:** and with no custom plugins on Rviz. it a fair parity or are

[00:54:16] **Adrian Macneil:** I would say if running no plugins and others, it's pretty good. The other one besides custom plugins I would pull up is, is, like the Moveit, and I think Nav2 

[00:54:26] **Audrow Nash:** all that intergations 

[00:54:27] **Adrian Macneil:** yeah, we have some of those features, but there's definitely a handful of things that, I would say we're not at parity, with Rviz, plus like the MoveIt or the Nav plugins, 

[00:54:39] **Audrow Nash:** Cause they've just been developed for Rviz or

[00:54:43] **Adrian Macneil:** right, exactly,

[00:54:44] **Audrow Nash:** that makes Yeah. that's, those projects are huge. so be a lot

[00:54:50] **Adrian Macneil:** And things that we would definitely like to, had, plenty of chats with those teams and the things that we would like to support in the future and feature requests come up reasonably frequently, but like you say, it's just, there's a lot of, surface area and visualization.

[00:55:05] **Audrow Nash:** very

because it turns into a browser or something. it is a browser, but it's like it, the amount of visualization and display and eventually maybe you want a UI all sorts of things. It just, it becomes like a sandbox for making other is what it

[00:55:29] **Adrian Macneil:** yeah, it's, it's, it is very open ended, and Our goal is not to solve 100 percent of anyone's we to solve want 90 percent of the problems, but every, company is different. There's different types of visualizations You need to be extensible and let people, get the last 10 percent of the way themselves, on the flip side, not have to start from zero.

There's a lot of companies, especially outside of the ROS ecosystem, a lot of companies that have just, that are using a completely in house visualizer that They have built over the years, right? And again, this is something that, maybe that's taking up like half an engineer's time or something within the company or depends on the company size.

Maybe it's someone contributing every, once a week, and maybe it's like a full time team of a couple of people working on it, but it's a significant investment in, 90 percent of that being undifferentiated, right? 90 percent of that being the exact same shit that like every robotics company visualize.

[00:56:27] **Audrow Nash:** yep, for sure. And also I'm sure that their in house one would not be as good as something that is, that's the only thing you got. you guys have several parts this project, but it's

[00:56:37] **Adrian Macneil:** our is yeah, we got the whole, 

[00:56:39] **Audrow Nash:** a robotics company.

[00:56:41] **Adrian Macneil:** exactly. leverage a team of, we got ten engineers right now, I think, focusing on, leverage a whole team focused on, 

[00:56:49] **Audrow Nash:** for sure. 


## [00:56:50] The Evolution of Foxglove Visualizer

[00:56:50] **Audrow Nash:** And you guys have been working on it for years and out of Cruise, which I don't think we said explicitly,

[00:56:56] **Adrian Macneil:** yeah, and one of, a couple of our engineers, have been working on this project for seven, eight years now.

It's yeah, the visualizer did actually, start at Cruise and some of our, very small portion of our code traces its, traces its way back that because created this visualizer at Cruise, we partially open sourced it at Cruise, it got a little bit of traction, but it was also, too tightly coupled to a bunch

Cruise assumptions and self driving assumptions and was not as useful for other types of robots, other types of like manipulators or mobile manipulators or AMRs and things.

it was, like, had a lot of built in assumptions around you're probably going to be outdoor, you're probably not going to be able to move the camera in certain ways, your robot, a self driving car doesn't have any sort of or, really like joint states or anything like this.

so it was, we partially open sourced it. at Cruise and it did get some adoption, with Foxglove, it was like, hey, all right, let's, take that as a foundation, move it on. I think now we're, we look at it's 15 percent or something of our code. It dates back to the Cruise days.

It's a pretty 

[00:58:04] **Audrow Nash:** Yeah. And it's

[00:58:06] **Adrian Macneil:** yeah, small and decreasing fraction, but, but it is that lineage of the project that we've been working on and some our 

[00:58:14] **Audrow Nash:** For sure.

[00:58:15] **Adrian Macneil:** time now.

[00:58:16] **Audrow Nash:** Hell yeah. 


## [00:58:17] Customizing Visualizations with Plugins and Extensions

[00:58:17] **Audrow Nash:** Now tell me about the plugins and extension API.

[00:58:21] **Adrian Macneil:** Yeah. So we have, Bunch of different ways that you can customize, the visualizations.

Like I say, everyone, there's a lot of different things people want to do with visualizations. So at a first kind of premise and, also in addition to that, one of our kind of founding beliefs is that robotics tooling and infrastructure should be framework agnostic. So quite early on, quite early on, we started with ROS support, but quite early on we, we tried to, as much as possible, Decouple ourselves from ROS while still supporting ROS really well and make it in a way that anything that you can do in Foxglove, nothing in Foxglove requires ROS.

Anything can be done just in a general purpose way. so we think about extensibility. The first thing doesn't even require an extension. It's just how do you render arbitrary things, right? So we have a bunch of primitives that you can render. You can publish messages, either directly from your robot, or with a, what we call a user script, which is a little script.

Running, in line in the browser that you write that does transformations. but you can take your, can take your robot data and you can turn that into things like we have, 3D primitives, like a cube primitive or a line primitive or a, point primitive or a. A Model Primitive, if you want to render a mesh or something like that.

so we have these building blocks of you want to, sure, you want a stop sign in your 3D panel. Okay, just bring a mesh, bring an STL file or, or something like that. And you can publish that, wrap it up inside a Model Primitive message and publish that, to Foxglove.

So you have first of all, these building blocks of like, how do I visualize things, As well as more common sort of higher level abstractions like a point cloud, for example, great, we can just take a point cloud message, and visualize that you don't have to write out, 30, 

[01:00:09] **Audrow Nash:** Yeah. already there.

[01:00:11] **Adrian Macneil:** or anything crazy like that.

and then, so you have all of these kind of like drawing primitives and that's the, that's the first place that you would start. And then, like I said, you get into extensions. 


## [01:00:23] Advanced Visualization Techniques and Extensions

[01:00:23] **Adrian Macneil:** We have, a thing called user scripts that I mentioned before where you Basically subscribe to topic data coming from your robot that might be a custom message that you've written.

Let's say you've got a custom message that's like tracked objects or something, right? You want to render that so you can write a user script that just says read the tracked object and output, like an array of, like cubes or something like this cube primitives. so that's, just like a really quick way that you can turn arbitrary data into something visual.

And then we have extension versions of that. So the user script is like a lightweight, just like happening fully in the browser. You're editing it and there's like a full on text editor just sitting there ready to go. is,

[01:01:09] **Audrow Nash:** nice. That's so

[01:01:12] **Adrian Macneil:** yeah, It it, it's just a lot easier to play around with things basically.

You don't have 

[01:01:16] **Audrow Nash:** do something very quick. And if you have a very tiny. Transform that you want to apply to some data so you can display it. That's very Okay,

[01:01:25] **Adrian Macneil:** Yeah. 

[01:01:25] **Audrow Nash:** that's for only lightweight things, because I would assume, I like my, code editor

[01:01:31] **Adrian Macneil:** right, 

[01:01:32] **Audrow Nash:** So then if you have larger projects, now you

[01:01:35] **Adrian Macneil:** Yeah. So that's when you would leap to like. A full on what we call extension, with extensions, there's, a handful of different extension types. You can, you can do those kind of transforms. So for example, we have, I think it's called a message converter extension where you can, you can say, anytime we see a topic, of type foo, here is a transform, a known transform that would apply that and turn it into a Foxglove schema, something that we know how to visualize.

So maybe you've mucked around with your user script and from you want to go from your tracked objects to like something visual You're like, okay. that's nice Audrow's figured this out How do we, but I've got a team of 50 engineers who all want to do the same thing You can bring that into your code editor, bundle up as an extension, deploy it to your company as this topic matches this like particular internal data type This is how you would turn it into something that FoxLog knows how to visualize.

[01:02:30] **Audrow Nash:** So with that, anytime the topic matches, do you, so I, do you have, do you code it in the extension that I'm looking for a topic named foobar joints or whatever?

[01:02:43] **Adrian Macneil:** or with with that 

[01:02:45] **Audrow Nash:** is that

[01:02:46] **Adrian Macneil:** You with that one in the extension With that example, in the extension, you match on a type, like a data 

[01:02:53] **Audrow Nash:** Ah, cool. Way better.

[01:02:56] **Adrian Macneil:** slash, tracked objects or something, that's kind of custom data type that you've created, so you would just match on that, it doesn't necessarily need to be the topic name, it's just the, any, message that matches type, and then how and then this is something, again, you, would write this in your code editor.

[01:03:16] **Audrow Nash:** Yeah.

[01:03:17] **Adrian Macneil:** Yeah. We have both. are topic based and the, extension is a, yeah, the extension ones work on a type base, but, 

[01:03:30] **Audrow Nash:** Cool. Okay. Yeah, okay, I was just thinking how to make it not as A

[01:03:36] **Adrian Macneil:** Yeah, You don't to be 

[01:03:38] **Audrow Nash:** and maybe I'm coming with Ross, two ideas. So maybe the, language is slightly different.

[01:03:44] **Adrian Macneil:** Yeah, but the thing, yeah, the way we think about the type thing is, it's, really just like teaching Foxglove how to visualize your custom message, and it doesn't matter what topic it's coming on, it's just anytime you see, because we know how to visualize it. A ROS point cloud. We know how to visualize, or we know how to visualize like a ROS marker message or something.

We don't know how to visualize like an Audrow tracked object or whatever, so we create, you can teach us how to visualize that by creating one of these little like transformer extensions, converter extensions, and then, and then you can deploy that, like I say, either publicly or.

Just 

[01:04:21] **Audrow Nash:** Internally or 

[01:04:23] **Adrian Macneil:** yeah.

[01:04:24] **Audrow Nash:** That's really cool. yeah.

Hell 

[01:04:27] **Adrian Macneil:** and then there's, there's three or four different extension types, but the other kind of key one that people, make a lot of use of is you can actually create an entirely custom panel, right? So each panel in Foxglove is just its own separate little HTML JavaScript app.

and the simplest possible panel you could create would just be, exactly, Hello World, or just a button or something, right? You can, in fact, the button example is quite cool, because you can just, you can use the API, you can create a little, just, HTML page with a button on subscribe to any button clicks, you could actually publish a message back to the robot, for example.

and is a this cool way, we have a built in kind of button panel, but it's people want a lot of different things out of buttons, so you may as well just make your little form, create whatever, you can display whatever you want, you can handle button clicks, whatever you want, and you can publish messages back to the robot as well.

[01:05:19] **Audrow Nash:** Now given. Like I, I've worked with, like I, I tried to make some Foxglove extensions in the

[01:05:28] **Adrian Macneil:** Oh yeah, cool.

[01:05:29] **Audrow Nash:** and, but, so with this, it's all, so you're running Electron and your UI is, it's a type script with React, right? if you wanna add these, ru these buttons and things you're using TypeScript and

[01:05:44] **Adrian Macneil:** don't, there's no, we, use TypeScript and React, there's no requirement, on that for an extension. 

[01:05:51] **Audrow Nash:** the, if you wanted to do your custom one, is there a

[01:05:55] **Adrian Macneil:** No, you can, we do, I think. because we use TypeScript, I think we, a lot like we generate and we'll use But there's no, TypeScript is just compiled to JavaScript under the hood.

so you can use plain JavaScript if you want. and then, but as far as React, there's no, there's actually no dependency on React. Within the panels themselves. So each panel, if right, you want to add React, do. That's fine. But yeah, you can just stick like a very basic, hello world, HTML, like you would have written in

of thing there if you want.

[01:06:32] **Audrow Nash:** it's very flexible. You basically say load this web page from or something like this and it just does it. Okay, so you get all that flexibility in.

[01:06:40] **Adrian Macneil:** And then, yeah. then up to you if you want to. I've seen some people do crazy things with extensions. You can use that to load some web assembly or, do, anything you want really. 

[01:06:51] **Audrow Nash:** Oh, that's really cool. Yeah. WebAssembly is so exciting 


## [01:06:57] WebAssembly and Performance Enhancements

[01:06:57] **Adrian Macneil:** Yeah, some very, yeah, it's still, there's very interesting things being done with WebAssembly, it's still an earlier stage technology and there's a lot of, there are rough edges around how you move back and forth between WebAssembly things and browser things, but it's, coming along really nicely and we do use, we use WebAssembly internally, for Some performance critical things too, like when you get into, for example, like decoding bags and you're doing like decompression, lc4 decompression, lc standard, things like this.

we're actually using what you are getting in Foxglove is C plus plus code that's being compiled to WebAssembly to do a lot of that, like decompression and things.

[01:07:37] **Audrow Nash:** So it's nice and fast. That's great. What a cool thing. Yeah, I really, I'm excited about WASM, WebAssembly, just in general. so can you, this might be a, so we've already mentioned you can make UI, which is cool. So you can make a button, it can publish a topic, and then that can be used to control your robot or do something.

Or maybe even pop up different parts of the UI or do things within the Foxglove program, I would imagine. Yeah. Would you ever imagine this being like a front end for a simulation? Like we have GZ server, Gazebo server and then we have GZ, I don't know, client or whatever it is, the renderer. could you, would you ever imagine using Foxglove as a way of displaying simulation or i don't know connecting it more other

to 

[01:08:35] **Adrian Macneil:** Yeah.


## [01:08:36] Foxglove's Role in Robotics Simulation

[01:08:36] **Adrian Macneil:** We do see people, like today, people use Voxelver a lot to visualize the output of a simulation. Because typically simulation, there is the perspective of the simulator, and it's, you can think of it as Okay, here's this third person view of, what the simulator is trying to create.

But then that data is being created into sort of false, it's creating sensor data and that's being fed into your robot stack. You do want to visualize the other end of it, which is like, what does the robot think that it's doing? so that is very common. People like visualizing the output of simulations is very common.

the, sort

[01:09:13] **Audrow Nash:** you mean the result of what the

[01:09:15] **Adrian Macneil:** Yeah, exactly. Yeah, like the recording, if the robot, if a robot is driving around in the real world or whatever, moving around in the real world, yeah, exactly what others would see. So the robot, is moving around in the real world, you would, you have a recording of what it saw.

if a robot is, moving around in simulation, you have a recording of what the robot What things it saw, what the robot thinks it was doing, so that's like you say that, the sort of the Rviz output of, yeah, the recording and what kind of came out of the simulation, so that, that is necessary, I guess like the question then becomes, could you have one UI, which is solving both the simulation need and the robot need, I think it could be done.

I think it would be a ton of work. we don't have any plans to do that. I think that, it, logic, it would conceptually make sense that you could create all of the buttons that exist in Gazebo. You could create, you could, create a Foxglove plugin or it could be a first party supported thing and I could just talk to, like you said, the Gazebo server.

but you would have to recreate all of that UI and it would be a ton of work. Which, number one, so that's like a lot of a lot of work that has to be recreated. And then you've got this problem that, are a lot of simulation, frameworks and engines in the robotics space, right?

And now you've done all of that work, and now you just support Gazebo, but you don't support, IsaacSim, you don't support, any number of other, simulators that people are using. yeah, and so you just end up in this kind of 

[01:10:54] **Audrow Nash:** you've over committed to one

[01:10:57] **Adrian Macneil:** We've got enough things to do in the visualization space. if I think it was done by a, I think if, maybe if that was like a third party, a plugin or something, and that someone was dedicated to maintaining that, it could maybe be done. But it's, yeah, it sounds like a lot of 

[01:11:12] **Audrow Nash:** it's not directly interesting Alright, it's an, it's, you're over committing a bunch of resources to something that kind of works anyways for this, and I guess it does require a lot of, I don't know about the build story of Gazebo on different platforms, okay,

[01:11:29] **Adrian Macneil:** you come down to you've done all that work and now you only support one simulator and then, other people in the industry are different things.

[01:11:39] **Audrow Nash:** yeah, but Gazebo, for example, it, you can swap out the physics engine, and that could still be, A cool thing.

[01:11:49] **Adrian Macneil:** yeah, it would be interesting and I think that statement would make more sense in the ROS world, right? Like within the ROS ecosystem, it might make more sense to, to have Rviz and, Gazebo as a single UI because that is part of just one ecosystem and you don't need to, but for us with our sort of our stance on being framework agnostic and things, it's I don't want to, Have a situation where it's we're only really useful if you're using XYZ simulator and not, a 

[01:12:20] **Audrow Nash:** Not one. Yeah. Okay.

[01:12:23] **Adrian Macneil:** so a little bit of a unsolved problem there.

[01:12:28] **Audrow Nash:** For sure.


## [01:12:30] Challenges and Future Directions in Robotics

[01:12:30] **Audrow Nash:** is there anything else to mention about the visualizer or plugins? Or is this the full extent of the stack, or are there

[01:12:38] **Adrian Macneil:** this is, largely how we think about it, right? We talked about recording, we talked about getting data off the robot, we talked about indexing data in the cloud, we talked about, search and discovery of data, talked about visualization. some of the things that, you know, when you think like a little bit.

A little bit down the road, things that we would want to do to round out that are around, better indexing of data, better search and query across data,

[01:13:02] **Audrow Nash:** Yeah, I imagine making things easier for like machine learning training

[01:13:09] **Adrian Macneil:** Yeah, 

[01:13:09] **Audrow Nash:** Because you have your indexing that to me seems like especially given like the zeitgeist in robotics It feels like everything is about All the AI all the machine

[01:13:19] **Adrian Macneil:** Absolutely, 

[01:13:20] **Audrow Nash:** so

[01:13:21] **Adrian Macneil:** Yeah, and we're still, yeah, this is yeah, it's, becoming a much, a much sort of more important part of robotics development. Historically, I think, a lot of robotics machine learning was limited to just the perception side of things and just like basic image detection models like YOLO and some of these things, classification models and things.

But now, now we're seeing people move to like much more end to end learning, training based on multi modal data, not just images. and yeah, like, you alluded to, you've got all of this data in your cloud. how, does that kind of feed into your pipeline? And I think one of the, one of the more interesting pieces there that we're thinking a lot about right now is this concept of dataset curation.

so you've got all these 

[01:14:07] **Audrow Nash:** don't Securation is we said

curation.

set curate. Oh curating

[01:14:13] **Adrian Macneil:** yeah, set, sorry, yeah, understands my Kiwi accent, it's, yeah, the data, yeah, so you've got, Data set, right? You want to build a data set, a training data set. and you've got all of these kind of examples.

You've collected all these samples of like robots doing good things and completing tasks successfully. And you've got a bunch of examples of robots doing bad things and dropping objects or backing into objects or, whatever they're doing. you want to Add a lot of metadata to these.

You want to build up a data set and you want to like tag and organize them. You want to know, do I have a good distribution of data across like different tasks that I'm trying to complete? and, all of these types of things. So we need that metadata and then we also need. full versioning history of all of that metadata, because we want to know, go train a I model, I need lineage back to what was the, the, sort of data set I used to train that model or all of the episodes, all of these kind of, recordings that we used to train 

[01:15:18] **Audrow Nash:** Yeah, you want all of that

[01:15:22] **Adrian Macneil:** So that becomes interesting. then people, there's, usually, you're not taking a robot recording and directly feeding that into just like PyTorch or something, right? There's, usually some transformation that's happening there. so again, these are things that are on our mind as, we think about this, life cycle of data from, logging and recording to cloud.

absolutely, things that we would like to help out with in the future, but it's also, try to make sure that we do, do our core things well before we get too distracted with everything Yeah,

[01:15:56] **Audrow Nash:** Yeah, it seems like there's been the joke, that I've seen on X quite a bit where it's like, Everyone's digging for gold. So all the AI And so NVIDIA is selling

shovels thing. see 

[01:16:09] **Adrian Macneil:** doing 

[01:16:10] **Audrow Nash:** you 

[01:16:10] **Adrian Macneil:** well. Yeah.

[01:16:11] **Audrow Nash:** but so I feel like you guys are well positioned to help with data annotation, curation, these kinds of things.

cause you're already, you have this top notch visualizer for seeing data and then you could make it so that it's very easy to annotate and export to your

[01:16:30] **Adrian Macneil:** yeah. And where possible, there are lots of existing, you think about like image annotation or whatever, right? there are lots existing, out this. Like we,

[01:16:41] **Audrow Nash:** Robotics

[01:16:43] **Adrian Macneil:** yeah. Multimodal, there are definitely, fewer tools, there are ones out there, I think, to the extent possible.

we would, we can't, build everything, right? We can't be the tool for like robotics development or something. the 

[01:16:57] **Audrow Nash:** got to pragmatically

[01:16:58] **Adrian Macneil:** my belief is that there needs to be way more companies building robotics, developer tools, right? And we would like to hey, look, we've got the core strengths that we're good at here.

I'd love to have more integrations with other tools out there. And, we talked about some of these things, the, the, more of the operational workflows and like fleet management and things, right? It's it doesn't make sense for us to build everything at once.

I'd rather be good at some really core, good at core, good at some core features.

[01:17:29] **Audrow Nash:** Yeah. I think that makes a lot of sense.

[01:17:32] **Adrian Macneil:** yeah, labeling, a whole kind of can of worms. I think it's, 

[01:17:36] **Audrow Nash:** it's true, a million types of data, all the

[01:17:39] **Adrian Macneil:** yeah, the, high level, I, think a, much kind of, more sensible thing to start with is just more of, metadata labeling, so it's like you're going through and you're wanting to, particular episodes and which ones are good or bad or which ones are matching different criteria or, Yeah.

some companies are even looking to do like, English captioning, right? It's just this is a person like picking up an apple or something. because they're feeding this into models now, right? They're feeding in just like the natural, they take an existing like vision language model off the shelf, feed in a bunch of, robot data, like the text captions plus, plus the robot state and pose and things like this, plus the sensor data, feed that in and they can build, What's called a world model that has a concept of tying these movements and things back to action, which is really cool.

[01:18:28] **Audrow Nash:** Okay. Yeah, that, that is really cool. Are there, Like we, we don't have that much time, but, the, you'd love to see way more tools in robotics. so what would, you mentioned some, but could you rattle off a few that you think are good opportunities

[01:18:48] **Adrian Macneil:** good. Yeah.


## [01:18:48] Opportunities in Robotics Tooling

[01:18:48] **Adrian Macneil:** If you're going start a robot setup today, I would say if you're, thinking this, if you're thinking about a company, starting a robotics tooling startup, just go work at any robotics company for, two years, and you'll up you'll have suddenly 50 ideas for startups for a podcast that need to exist.

the areas that seem underserved, deployment to robots, for example, there's huge industry of, CICD for servers, right? There's almost no one, there was one company doing this, I don't know if they're still around. but just like how do you deploy and update robots in the field?

You've got to think about deploying them without breaking them. That's a, huge sort of, thing that's interesting. Configuration management for robots out in the field. How you like, keeping track of the fact that you've got like potentially different model, robot models, different SKUs, different sort of what service history has happened.

everything that every company ends up building internally should probably, if it applies to multiple robotics companies, should probably exist off the shelf. So there's a lot of the stuff around the operations of just like Deployment, Updates, Configuration Management, other, like simulation is another one that I think is quite, underserved.

It's there are some of these open source things like Gazebo, but I think there's a lot, there's a lot missing in there and like frameworks to let you run simulations at scale, the frame, tools to let you manage create simulation scenarios. how, do you manage, Testing a new release.

you need, like a whole catalog of different scenarios that you're ready to go simulate and you need to be able to run different aspects of that. You need to be able to score the output of simulations and say is this, is this better or worse? It's not just Hey, run this test and fail if we crashed or something.

It's through the metrics, how well are we doing? are we better or worse at completing all of these tasks in aggregate? There's just endless, I could go on for hours about all of these things. And. Like I say, you just, you work at any robotics company, look around pretty quickly, 

[01:20:50] **Audrow Nash:** You 

[01:20:51] **Adrian Macneil:** you'll see what's being built in house that really is not unique to that company.

[01:20:56] **Audrow Nash:** Yeah. I think that's a very good. Way to think about it, just whatever's being built in house is probably something that you could hire someone to do something better and then just use. So the doesn't have to maintain it and do undifferentiating work.

[01:21:11] **Adrian Macneil:** and the end state of this is, quite, is, that even a lot of the autonomy that's being built is not. should not be people in all our robotics companies today I think see data as a key sort of value driver for them and they see like their autonomy stack as being like really core to their mission it's okay we're solving autonomy for but the reality is that that you know when you're creating a business the thing that you are creating the value for a company is like The value that you're creating for a customer is the problem that you're solving for them and not how you implemented a solution to that problem.

and a lot of these autonomy problems are like, picking and placing or navigating around warehouses. how many different

Or outdoor

a lot of these kind of just and that's why things like NAP exist, right? But it's like, navigating around autonomously is not It's not a core kind of value driver for your company.

What is valuable is the problem that you're solving for your customers. And quite often is the distribution of how you're getting to the customers and how you're wrapping it up with service and how and support. and you think about the SaaS, the vertical SaaS industry today. There's millions of startups building like 

[01:22:24] **Audrow Nash:** Very 

[01:22:25] **Adrian Macneil:** specific solutions and making tons of money.

Tons of money, go out there, they talk to customers, they, listen to a business problem, and then they glue five things together, random open there's, sure, there's a bit of but you're not, they're not solving a technology problem, they're not taking on technology risk, they're taking on kind of product market fit risk, so they go and, They listen to customers, they build a thing as quickly as possible by gluing together as many off the shelf components as possible, and then they go and sell it, and work on it in the market, and bundle it up with support, and they solve a problem for people, and they get paid very well for doing that.

the robotics industry today is the complete opposite of that, where you have, a lot of companies that are, Solving blindingly obvious problems. It's wow, if you could get a robot to do that, would be fantastic. This is that'd be amazing. But they're taking on this massive technology risk of now I've got to get the robot to do that.

It's, completely backwards. And I think when robotics has succeeded, we will see that, flip. We'll see that invert, right? Where A robotic startup will mostly be talking to customers, listening to their problem, figuring out how you're going to connect with those customers, how you're going to market to them, how you're going to sell to them, how you're going to support them.

And the technology will, to the extent possible, be taking together a lot of off the shelf hardware, a lot of off the shelf software, a lot of off the shelf infrastructure, a lot of off the shelf autonomy components. Probably just grabbing some off the shelf, open source foundation models.

Fine tuning them a little bit, and solving a customer problem, solving a customer need, solving a business problem. Not, all of this technology risk that people are taking on today.

[01:23:56] **Audrow Nash:** Definitely. A hundred percent. I, this is part of the reason to me, companies like, do you know polymath They were one of my,

[01:24:03] **Adrian Macneil:** Similar kind of thing, right? It's yeah, you don't need to building the autonomy stack.

[01:24:07] **Audrow Nash:** yep. That's, I think they are. early on this trend and I think we're going to see a lot more of that is my guess where they're solving navigation for those who don't know and outdoor navigation like driving slow in fields something this and you just call it from apis like that's that seems like the way to go for a lot of

[01:24:32] **Adrian Macneil:** I

[01:24:32] **Audrow Nash:** you don't have to do that

[01:24:34] **Adrian Macneil:** get to a we point where those, similar companies, maybe it's Polymath, maybe it's others, but similar things exist across the board, for 

[01:24:42] **Audrow Nash:** domain 

[01:24:44] **Adrian Macneil:** for you're right. 

[01:24:47] **Audrow Nash:** We're on the same page.

[01:24:50] **Adrian Macneil:** Yeah, so I think, yeah, we will, definitely see a lot more of that.

[01:24:54] **Audrow Nash:** hell yeah. 


## [01:24:55] The Shift from Open Source to Closed Source and Foxglove 2.0

[01:24:55] **Audrow Nash:** so talk to me about the, the 2. 0 Foxglove and then, the decision to make it closed source for, I know some things are open source, but, some things are now closed So tell me about all that.

[01:25:11] **Adrian Macneil:** yeah, absolutely. So I think there were, two kind of arcs that happened. Like I said, Foxglove were about three and a half years old now. there are a couple of sort of things that we noticed over the first few years of Foxglove. the first one was that we started out, we started out with the Foxglove visualizer And then we added on this idea of we're going to build a data platform kind of thing.

And we thought of them as very separate components. And they are separate components to an extent. Like I said, the visualization is useful, not just with cloud data. You can also use it with local data or live connections. and the data is independently useful. but we took that too far and we built them as Literally completely separate code bases with separate repos and UIs.

and then we start tripping over ourselves with how sign on works across them and sign out works across them and how, if you're viewing some, you're exploring some data to find the right log file and then you open it in a visualizer. You've lost all reference to how you got here and what the metadata associated with this recording was.

And, if you want to just be clicking through a list of a, a list of a bunch of different examples of events or things like that, you want to just be able to quickly, Click through them. You don't want a whole separate tab. That's just the visualizer and a whole separate tab That's just the browsing interface.

So we came to this realization that It was even though they are You know separate product features It was a mistake to build them as completely separate apps and completely separate UIs And so we came to this decision that we needed to, to merge these together and that was the FoxClock 2.

0 was like hey, we're going from these, completely separate, literally separate code bases, separate tools, to, to one kind of observability platform, like I said, it's modular, it's got a bunch of features, you don't have to use all of them, but, it's one UI, you sign into it, you just, it's, one kind of app, and you can do things like With 1.

0, you could not do the data browsing in the desktop app. There were weird inconsistencies where you could, on the web, you could browse the data and visualize it. The desktop app, you could only visualize it, you couldn't browse it. now all of that's gone. It's one app. You can use it on web, desktop.

All the features are available on both platforms. and so that was, the first key part of, 2. 0. and then the second piece of it was, like you said, around open source. Our initial sort of decision was, our initial kind of like plan for the Foxglove company was that we would build this open source, visualizer, and then we would have a paid service that is like the data management service.

yeah, the, kind 

[01:27:48] **Audrow Nash:** So you can get it with

[01:27:51] **Adrian Macneil:** yeah, with teams. And the idea was that, there would be some sort of team visualization features, but there would also be most of the team features would revolve around data management and, like I said, uploading data, organizing data in the cloud and

[01:28:05] **Audrow Nash:** Yeah. That's what I understood from our last interview 

[01:28:07] **Adrian Macneil:** which was, that was the plan that we set out with and, we tried really hard to make that work. I think the challenges that we ran into, is that visualization itself is just a really, a bottomless, a very difficult problem, a bottomless of feature requests.

and of our effort, even, even today like 80 percent of our effort goes into the visualization, right? so we ended up with a sort of challenge where we're trying to sell a product. but some people were not interested in the, some people don't care about the particular sort of the cloud data features, right?

They're like, we figured out the cloud data piece ourselves. We really just want the visualization piece. again, we try to build a modular platform, so that's nice. You just want the visualization piece. but that's a thing that we don't do. we can't make money on, so it's just an endless stream of incoming feature requests and work.

and, work that we do for people, but no way charge for that. The only thing that we're charging for is the, the cloud data management, which some customers, didn't want. So there was a bit of a mismatch between, what we were spending most of our time on building, and, the thing that we were charging for.

And, that, that causes a problem as a company because we want to make the visualization great. But, it's just, it's not possible to do that if you're spending most of your time building the free thing. I guess another, I would say, and coming from, I'm a developer by trade and, I spend a lot of time using a lot of open source projects and we cared a lot about open source.

I think the analogy, and we still care a lot about open source, we support MCAP. I think, MCAP is, an example of a great, open source project as a company, right? It's something that you put out there. It makes a lot of sense to be an open standard. it's, a library. It's not like a, it's not like an app.

So it doesn't have buttons and UI and things like that. It's a library. People are much more likely to contribute to it. We get a lot of community contributions with MCAP. by contrast, we get very, almost round to zero community contributions for a, web based JavaScript visualizer tool, right?

and then also with MCAP, it doesn't take a lot of our focus, right? Maybe it's like a 10 percent focus for us, but not an 80 percent focus for us. we, maintain the project and keep updates and we, there's, ongoing development on it, but it's not, It's not the, primary focus of us as a company.

And I think you need to think really hard. if, anyone is founding an open source company, you need to really think about like how much the open source project is, going to take of your like overall development resources, and make sure that you. that, you have the, capacity to also invest in whatever the thing you're selling with.

In some, senses, and this is a little bit of a tangent, but when people ask me about creating an open source, company, I think one of the biggest challenges with open source is that you actually have two product market fit problems. because you have a, you still have, even though the open, whatever, usually every open source company has like an open source thing and then they have a paid thing that sort of supplements it, right?

and you, even though the open source thing is free, there's still a product market fit problem. You still have to make sure you're creating a thing people want. You still have to spend a lot of time on kind of marketing it and posting on social media or word of mouth or whatever. You still have to spread growth of that thing.

and then. That entire thing repeats itself with the paid product that you create, right? Yeah, you have to, have to create a thing people want. It has to make sense. It has to be enough of a value add, on top of the, on top of the free thing. and it's the same thing. You have to figure out how you're going to market it, how you're going to sell it.

And so you've, created twice much work for yourselves. but yeah, we, just, we really found, that, we were not able to, Invest the time and effort we, needed, in the visualization thing. We weren't really getting the sort of community contributions that we would get with something like MCAP.

and frankly, a lot, most of the people we talked about to this were like, most customers even, and potential customers were like, why aren't you just charging us for the visualizer? that's the thing we want, why aren't you just charging us for 

[01:32:26] **Audrow Nash:** Ah ha, 

[01:32:30] **Adrian Macneil:** but, we still have these principles, of the, that I think we're, placed when we started, which is that we want it to be, easy for hobbyists to use.

We want it to be easy for academics to use. We, we realized again, since. Most of the people that were using Foxglove, were not taking advantage of the fact, they liked the fact that there was a free version, they can download it, they can get started, especially, like I said, hobbyists, academics, or, the first few people at a company where they're just trying it out, they like the fact that it's easy to use.

they weren't creating a custom fork of it, or a custom build, or deploying a custom build, or anything like that, right? It was mostly just the fact that it, that there is a free version it's easy to get started with, and I think that was well placed. So even though, we, came out with this announcement about, around 2. 0, so I think it was about three months ago, saying, hey, we, we, we're not continuing any further development on the open source version of 1. x, we did have features that were always The, for example, like you go and download the Foxglove application, that always included some closed source components.

So that was always our distribution, included the open source and, some of the other components. We just said, hey, the open source release, we're not continuing to develop that. the 1. x code is still there if you need it, but we're, focusing on going forward. We're focusing on just keeping all of this, within, the, closed source build that we have been releasing.

honestly, it got very little, As far as, announcements go, it got pretty little attention. And I think, like I said, it didn't really change much for most people. most people were already using, they downloaded our desktop app, that was already a closed source build because building things like a macOS app with signatures and all of these things is like, it's not, particularly easy to do anyway.

That already wasn't The open source build they were using, the update to 2. 0, it looks pretty similar. We've added some new features and things and we've, spent a lot of time on performance lately, but there was no disruption to workflows, in especially, for the broader community, for individuals using it, for academics using it, for hobbyists using it.

there were some companies that, that were using it in a company setting. again, they were already, we already had some of these things like prompts. If if you're using it with more than x number of people, you're already seeing hey, over three people, you've got to pay.

there wasn't really any significant kind of change in the experience there for people. the only people that are affected was, Sort of a small number of people that we're we're walking in. On the other hand, I think another sort of advice, piece of advice that I give to people building a similar sort of like open source based company now, especially having reflected on a few years of this at Foxglove, is that you need to have in your mind a mental model of What percentage of people that use your free thing are going to upgrade to your paid thing?

It's not even really to do with like open source, right? But open source makes this problem 

[01:35:41] **Audrow Nash:** Yeah. just a conversion rate for keeping your

[01:35:45] **Adrian Macneil:** And typically that is going to be pretty low. So you think about, a lot of, there's a lot of open source databases out there, for example, right? So there's something like InfluxDB. this is like a time series database, and then you can use like the hosted version, or there's MongoDB, or there's Elasticsearch, a lot of these are open source, or, sometimes slightly more creative licenses more recently, Redis and things, but, they have open source database, and then like they have a hosted version.

But it's a very, extremely generally applicable thing, like Elasticsearch is a full text search database, or Redis, you can use it for just about anything. if a fraction of 1 percent of people that use that, move on to the paid service, that's still like a, large, it's plenty, it's still like an enormous kind of market that you're talking about.

robotics, unfortunately, is not like that. And, basically every, We can't afford for only like 1 percent of, of, of pro of big companies that have raised a lot of money, or, in some cases, big multinational, car companies and things like that, that, that have enormous global presence, enormous revenue.

Every one of those that sort of decided to, to just use the open source version because that was sufficient for them, becomes like lost revenue opportunity, right? And that is, again, if you're operating in an enormous market with like tens of thousands of potential, or hundreds of thousands of potential customers and companies, that's fine.

If you're working in something a bit more niche, like the robotics industry, you can't afford to have just like such a tiny conversion, soon. 

[01:37:19] **Audrow Nash:** Yeah. That makes good sense to me. Yeah. Because we're a much smaller community than like the web developers say, I.

[01:37:27] **Adrian Macneil:** or, 

[01:37:28] **Audrow Nash:** Or databases, which yeah, are everything.

[01:37:30] **Adrian Macneil:** is like every company that needs a database. yeah, but it's been good. Honestly, the response to that was super positive. everyone, I would say maybe there was like one or two messages that popped up on like ROS Discourse or things that were a bit upset about it.

But, yeah. On the whole, pretty much everyone was like, yeah, that makes sense. It's totally fine. 

[01:37:54] **Audrow Nash:** Good.

[01:37:55] **Adrian Macneil:** the, main concerns that came up, maybe we miscommunicated a couple of things, but some people came up and thought we were getting rid of the desktop app, which sort of me off guard cause I didn't 

[01:38:05] **Audrow Nash:** not what you're doing at all. Yeah.

[01:38:07] **Adrian Macneil:** fact, we're adding more features to the desktop app. but that popped up, with a few people and we had to correct that misconception. And the other one was just, like I said, is making sure there's still a free version. So it's not really any different. If you go to our website and hit the download button today, it's the same experience that you were getting three months ago.

we've still got the extension APIs. That was another one. So people were concerned that the extension APIs were going away. but, these things are, largely the, the same experience. It's just that we have a more clear licensing now, where if you're using it for up to three people, in a company or in a team, that's, free.

And then over that, you got to start paying us.

[01:38:48] **Audrow Nash:** Might make sense. you guys need to eat

[01:38:50] **Adrian Macneil:** we do. Yeah. Yeah. like I said, yeah, we want to create this really great software. We want to keep investing in it. And, 

[01:38:57] **Audrow Nash:** you have to exist order do that. so I don't know. Okay. That makes good sense. I, think, like to me, even just the first point of it's easier for us to maintain. is huge because guys your time, and I've been involved with the ROS project for a long time. You need the staffing to do that, or you can sour relationships too.

someone puts out a feature request or something, and if you don't get to it after a while, a little bit of bad blood that's created there this of kind if it's like endless visualization features, I can understand how kind of turning that off, because the expectation is if it's open source that you're going to be triaging everything.

[01:39:48] **Adrian Macneil:** come up with the, yeah, the, reports and things and yeah, and we do want to get that. And now, honestly, like said, the, moving fast thing is important too, right? Like now, internally, we, just have a single, like I said, we merged a lot, all between the, sort of data and the visualization.

So moving

better product experience. We're not juggling like open source repo that we're then trying to incorporate into another product and things. It's just we're building this one app. people, sign up for it, they use it. and a pretty, a concept people are pretty familiar with.

[01:40:20] **Audrow Nash:** For sure. Yeah, I guess like it I guess the moving from open to closed it like saddens me a little bit But I understand for very pragmatic reasons and I think it was probably a very good decision and I bet it was a very hard decision

[01:40:37] **Adrian Macneil:** I 

[01:40:37] **Audrow Nash:** making the decision and I think it'll be better for guys

[01:40:41] **Adrian Macneil:** I was probably, but with, every decision as a company, you always think, wow, we could have made that decision a year ago or two years ago. It was in hindsight. I think, like I said, coming from an engineering background and using a lot of open source software and I was probably the most, saddened out of everyone, right?

People pop up and they're like, oh, we're sad that you're moving, and I'm like, look, I am too, but but, we had to do 

[01:41:09] **Audrow Nash:** I think so.

[01:41:10] **Adrian Macneil:** it made sense, and I think when you talk through it like that you say, look, these are the constraints that we're working with, 

[01:41:17] **Audrow Nash:** Totally. Yeah, you guys have to stick around if you devote your resources to something that's not helping, you stick around. if you, guys went out of business, that would be a much bigger loss 

[01:41:26] **Adrian Macneil:** exactly, It's not a choice between us continuing to develop and pay, right? It's look, we want to exist as a company. 

[01:41:35] **Audrow Nash:** for 

[01:41:35] **Adrian Macneil:** we're

[01:41:37] **Audrow Nash:** it's such an exciting time, so you definitely want to exist super exciting time.

But,

[01:41:42] **Adrian Macneil:** time to be in robotics. 

[01:41:45] **Audrow Nash:** so we're, coming to the end of the time. one thing I wanna make sure we talk about, tell me about the Actuate Conference and, why and what you're showing and everything


## [01:41:59] Actuate Conference: Bringing Robotics Developers Together

[01:41:59] **Adrian Macneil:** yeah, so Actuate is a one day event that we're putting on in San Francisco. It's going to be on September 18th. got a really nice space that we've, venue that we've booked in the dog patch in San Francisco. and this is, an event, a conference for robotics developers.

Anyone? robotics is a very sort of cross functional domain. There's a lot of people working on a lot of different things. But we want to bring together engineers, across people working on perception, planning, AI, simulation, frameworks, hardware even. We want to bring together, bring together a lot of these different disciplines.

It's a one day event. We've got some really great speakers lined up. and we've got some, some really great attendees lined up. The goal of this is how can we bring together just lot of the community in the Bay Area where we get to talk to.

As I would say, in the position that we are in as Foxglove I get to talk to a lot of different companies and hear a lot about how they're building their robots. none of our customers talk to each other. there's a real gap in the robotics industry of, like deep technical content on how people building robots in production.

There's a lot of, there's a lot of content out there from the academic perspective, right? There's a lot of papers, there's a lot of robotics conferences you can go to and listen to. a lot of sort of the academic perspective, not so much in industry. I would say the, stuff that exists in, the industry today, in terms of, like talks and conferences and things, ROSCON is, a similar level of, has the technical depth, but it's centered around ROS, I would say, ROS is, one framework in the industry, but we see a lot of, our customers not using ROS, and we'd like to have a broader perspective there. and then you see a lot of kind of robotics trade shows, like Automate and things like that, where people, you've got the sales team, they've got their robots, they're, showing off their robots, but it's not how they built the robot, right?

It's, this is just look at the robot, what the robot can do. So we felt that there was this kind of, there's, a real gap for high quality technical content, in the robotics industry. Talks and not just listening to the talks but getting together and networking with other people in the industry.

And I think, because it's a one day event, we're expecting it's going to be a mostly Bay Area audience. I do know some folks are flying in for it, for the first year that we're doing this, we're expecting that we're mostly going to have kind of Bay Area attendees. I think we would, look to go, a bit larger next year, probably.

And then in terms of speakers, we've got a handful of really great speakers lined up. We've got, Sergey Levine. He's a professor at Berkeley and co founder of, company Physical Intelligence. We've got Chrysler Lalancette. He's the technical lead of ROS. Steve Macenski. He's the technical lead of the NAV2 project. Kat Scott from Open Robotics, I think you'll be very familiar with her. Vijay from WAVE, he's the VP of AI at WAVE. So we've got a whole lot of good speakers already, and then I think we have a number of, we currently actually have a call for proposals open right now. Number of super interesting proposals we've had come in.

Like I said, we want to really find a great balance of content across people working on AI, people working on, perception and planning, people working on simulation, just cover the whole sort of spectrum of different things that, that we do. that are needed in robotics and help encourage them sharing, have some really great speakers, but also have really great attendees and, high quality kind of conversations.

[01:45:40] **Audrow Nash:** Do you, is there much planned for the evening after

[01:45:45] **Adrian Macneil:** Yeah. 

[01:45:45] **Audrow Nash:** I find like the unstructured time to just talk with all the me, that's my favorite part of the whole

[01:45:53] **Adrian Macneil:** Yeah. And I also, I, yeah, that, yeah, there's, structured lunchtime. There's a cocktail hour. I think it's from four to six or four to seven or something like that. So we've got like a happy hour at the end as well. so there, there will be plenty of kind of unstructured time for chatting. Also, just a single track event is a really fun thing. I think, a lot of these larger conferences, get to a point where there's all these multiple talks and there's rooms and presentation, there's a hall with all of the, vendors and things and you spend most of the conference wandering around.

but I think the, beauty of a, single track event is that, there'll be nice punchy talks. You come on, hey, we're having this session, just like everyone listen, and then everyone can go out and we'll have some, some time to chat and get to know people. so yeah, we absolutely like the networking times good, but I also think the beauty of a single track event is that these have any of questions of oh, which talk should I go to?

Or should I just maybe I should be networking instead of listening to the talk and yeah, it gets a bit, many Too Yeah, it'll be fun. It'll be awesome. yeah, we'd love to have you there, Audrow, and, yeah, we will, we'll make that happen.

[01:47:06] **Audrow Nash:** Hell yeah. Yeah, I would love to go. if it works out, I think I'll be there. I think you had some code with my

[01:47:15] **Adrian Macneil:** Absolutely. Yeah, So for folks listening that have made it this far in the podcast, so a couple of things. One is we currently have early bird, like I said, the event's on September 18th. It's a single day event, San Francisco. it's from about 9 a. m. or 9. 30 to, 4, or something like that. We have early bird ticket sales going on right now. So I think the first hundred and fifty tickets that we sell are 150 dollars or 149, something like that. So get in quick before those sell out. And then we have an additional, I think on top of that, it'd be additional 20 percent discount for listeners of the podcast.

Just put code Audrow in there. Check out A U D R O W. that's the secret code, which will get you an additional 20 percent off, 20 percent off the early bid price if you make it in time, or it will be, 20 percent off the full price if you're a little bit slow, so get in quick.

[01:48:08] **Audrow Nash:** Hell yeah. Awesome. so with that, I think we shall wrap up. Great talking with you, Adrian. So cool Foxglove and all the great work you guys are doing.

[01:48:21] **Adrian Macneil:** Absolutely, yeah, 

[01:48:22] **Audrow Nash:** see you at

[01:48:22] **Adrian Macneil:** As always, thanks, Audrow.

[01:48:25] **Audrow Nash:** All right. Bye everyone.

That's it! You made it!

What has your experience been with Foxglove? Or if you haven't used it, do you think you'll give it a try? 

If you like this interview, I'd appreciate a like or a review. It helps other people find the podcast and pleases the algorithms. And if you'd like to make sure you hear about new episodes, make sure to follow or subscribe.

Our next episode is a very strong robotics company in the food space. They're doing great work with robotics and machine learning, and they've already done over 5 million food servings in production.

That's all for now. See you next time.


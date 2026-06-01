---
source_title: "Karpathy's LLM Wiki Goes Further Than Everyone Realised"
source_url: "https://www.youtube.com/watch?v=ijBJVzxSBRA&t=96s"
created: 2026-05-31
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=ijBJVzxSBRA)

📚 FREE to join — weekly live Q&As + the same AI frameworks I use with clients ⬇️ https://www.skool.com/ai-builders-hub  
📈 Learn to build production AI systems in 8 weeks with direct access to me: https://aif.academy/go/yo-adam-goodyer  
⚙️ Running a business with 5+ employees? Work with my team to implement AI into your business: https://apgsoftware.com/  
  
Looking for 1:1 Claude/AI consulting? ⬇️  
https://cal.com/apgsoftware/consult  
  
Summary  
  
Every video covering Karpathy's LLM Wiki is about personal notes and Obsidian.  
  
I've been running the same 3-layer architecture across my entire AI agency for 6 months — 20+ agents, active client engagements, a production delivery pipeline. Here's exactly what it looks like.  
  
⏱ Chapters:  
0:00 — Intro  
1:02 — The LLM Wiki Pattern  
3:37 — The Agency-Wide Mapping  
6:07 — The Video Editor Demo  
9:32 — Per-Agent Memory  
11:42 — Why Structure Beats RAG  
  
▶️ Connect with me  
  
LinkedIn: https://www.linkedin.com/in/adam-goodyer/  
Instagram: https://www.instagram.com/adam.goodyer/  
Twitter: https://twitter.com/adamgoodyer\_  
  
🌐 Work with APG  
  
Join the team! Apply in less than 5 minutes at: https://apgsoftware.com/interview  
  
🛠️ Tools I Use (Support the channel through these links):  
  
🎨 Untitled UI — https://www.untitledui.com?atp=adamfreelances  
📢 Wispr Flow — https://ref.wisprflow.ai/adam-goodyer

## Transcript

### Intro

**0:00** · Kapathy's LLM Wiki has been blowing up over the past week. It got over 5,000 GitHub stars in just 7 days, and everybody's using it to build personal knowledge base systems on tools like Obsidian, but nobody's really shown how to actually operate this in a business context. So, what I'm going to show you is how we use this exact same structure and framework to organize some of the plugins and AI first frameworks that we have operating our agency. If you're not familiar with me, my name's Adam. I've done over 60 projects on Upwork.

**0:26** · I'm top-rated and expert-vetted, and I run APG Software that's done over 300 projects. So, I'm doing a hell of a lot of AI work, and we've built seven different plugins that are genuinely dropping the time it takes for us to deliver projects for clients by anywhere from 40 to 80% whilst also helping me do things like edit the exact video that you're doing entirely with AI, build the presentation that you're watching, and everything else that is involved in my day-to-day process.

**0:50** · Building these AI systems at scale means having proper frameworks and structures, which we're going to explore in this video, and that's exactly where Kapathy's LLM Wiki comes in. So, let's dive straight into it.

### The LLM Wiki Pattern

**1:02** · So, what is Kapathy's LLM Wiki? Well, we can take a look at the actual LLM Wiki here on GitHub. Uh essentially, what it is is it's an organization system for your Claude's calling them plugins, but your departments that you're building in your AI first business system. Now, what is an AI first business system or an AI operating system? It's getting thrown around as. Essentially, what it is is it's a way of building different departments in your business using Claude code. So, we're going to talk through the video editor demo.

**1:32** · We're also going to talk through our audit process and show you exactly how that works, which is operating off of the frameworks that is outlined with Kapathy's LLM. And there's a three-level structure there. We're going to talk about the raw digestion of data, then the summarization and structuring of that data, uh and then the the schema creation so that the AI knows where that data is, how it's stored, and and how to access it in order for us to maintain and structure that information as as the knowledge base grows and grows and grows and the complexity of our systems grow.

**2:06** · So, this three-layer pattern genuinely looks like this. So, first off, we have the raw data. Now, we're going to take our auditing process as an example, and this is at APG Software what we do for small to medium businesses is essentially we first audit their business, right? We build all this documentation on how that business works so we can then help identify areas of opportunity that we can implement AI.

**2:29** · And so, how are we using AI to genuinely That process used to take, I swear to God, 200 hours or more, which is now dropped down to something we can do in 20 to 40 hours. AI is So, that's an 80% decrease. And the reason we're able to do that is because we now have an AI first business system that is doing a lot of the heavy lifting there. And the way that it works, right, is we we connect it directly to our meeting transcript and our meeting note-taker, which is fathom.ai, which is completely free.

**2:56** · And we also connect it to uh Twilio to get every message and call that we make to a client, and we connect it to Gmail so we can pull every email.

**3:06** · And so, the first step is that we have this workflow, and I'll show you what that actually looks like in here. So, this is our audit agent, and you can see here we have this number three agent, which is the audit extractor. And what it does is it is it's basically connecting to all of those tools via API. It has some info stored information in the Wiki, and I'll talk about that in a moment, on the client's email. And so, it pulls all that information and stores it in a in a folder that looks like this. It's just meetings/meetings/transcripts or whatever.

**3:35** · So, this is all of your contextual information on a client engagement for doing an audit about their business. So, we do 5 to 10 hours of interviews. We have all these emails.

### The Agency-Wide Mapping

**3:45** · They send us materials, and we build all of that into the raw layer. And then what we do from there is we extract all this data, and we put it in this JSON format so we can organize the information really clearly. And so, we will call that the Wiki layer. And what the audit the audit JSON looks like is when we're do when we're having these conversations with the client, we're trying to uncover three things, right?

**4:07** · We're trying to to be basically figure out, all right, who is completing a task? Who's responsible? How long does it take, and how often are they doing it? And what tools are they using? Those are the main things that we care about.

**4:19** · And obviously, there's there's all this other information, but that's the main stuff that we're storing in this Wiki so that we can extract that information.

**4:26** · We're also extracting things like, you know, is it is it pe- like is it a pain point? Uh blah blah blah All this other information on that, but at in the essence, that's what we're doing in the JSON, the structured Wiki information.

**4:38** · And so, this is where we're storing all that key information that we're then using later down the line to be able to compute exactly how much money they might be wasting. Uh we can use that further down the line in all these different agents that are helping build product predictions uh and audit their business, but it all comes from this audit data JSON, this central knowledge base, or this Wiki on exactly what what they have. And what we have on top of that is a Claude MD file. We also have the skill.md file in there. This is actually what's telling the agent what's in the Wiki and what's in the plugin as well.

**5:10** · So, when we look at th- this is the way Claude likes to lay out their plugins, but we have skills, connectors, agents, hooks. And we actually build this in Claude Cobra. I'm just showing you here so you can see how this works.

**5:21** · This is where if we're working in the tool, it it's aware of exactly what agents it has access to, what skill files it has access to, any data, etc.

**5:32** · So, this is the general three-layer pattern that we're building all of our agents to have. And if we look here, so you'll see you can kind of break it down here. So, we have these raw files, our meetings, our transcripts, our emails, etc. The LLM then compiles it into this Wiki structure, which is showing the processes, the tools that they're using, where the pain points are, are there any like suggested optimizations, proposed changes, etc.

**5:56** · And in the agent schema, there's files that tell it not just these things, but everything else that we have in the plugin that might be relevant, um templates, etc., etc. So, this is like a general three-layer pattern because as you start to build this out and you have 10, 50, 100 clients, you have all this information everywhere, the AI can't index all that It's too much context.

### The Video Editor Demo

**6:17** · It needs The the general idea here is that we're telling the agent exactly where to go to to be able to find information so that when your knowledge base starts to stack up, it doesn't bloat your context window massively just to try and locate the information that the agent needs to locate cuz at the end of the day, that is the objective of this is controlled context injection into a conversation.

**6:42** · Now, that's just one example. Another example is our video editor pipeline.

**6:45** · So, if I show you our video editor, we have This is editing the video that you're watching right now. Again, we have multiple agents uh and we have multiple skills. So, we it's done by Remotion, so we have a Remotion skill, but then we have separate skills for long-form, short-form, video sales letters, advertisements, etc. And within those skills, you can see here that we have these different So, we have a skill file, uh then we have references. So, these are things like long-form pacing rules, guides, etc.

**7:12** · And then we have a a workflow long-form edit workflow that's got all of this extra data stored within it. And so, what happens, right, is we have it creates what they call an ingest layer. So, the first step of our video editor workflow is we drop the raw video file into a folder, and we ingest it.

**7:31** · And what it's doing here, these these is it's executing commands to transcribe that video, to create a proxy. So, we'll often film in 4K, but if you want to, you know, send this via API anyway, you don't want to send the full 4K file cuz it's massive. So, you want to clip it up into a smaller proxy. So, that means that when we're calling APIs, we can use a much smaller file size, and it's way easier to do that. So, we do audio analysis. We do transcription, and then we do video clipping, which is basically clipping out dead noise, uh etc., etc.

**7:57** · That all happens in a video ingest. And what we're doing here is exactly what we're doing here, which is cleaning up our inputs, right? That's our raw That's our raw information. From there, we're then compiling a storyboard. Now, the storyboard is is a JSON structure again that's saying, "Hey, for the first 4 seconds, show this motion graphic. This is the transcript. These should be the zoom effects, etc." See how in essence, that's actually a Wiki? It's telling the AI, "Hey, look, this is exactly how the whole thing's going to be constructed."

**8:27** · And then Remotion \[clears throat\] then reads that file. So, it's a similar structure to what we have back here, where it's like raw data, controlled aggregation of that data that can be easily filtered so that as our raw data grows and grows and grows and grows and grows, we we still there's a there's a you can almost write deterministic scripts to be able to extract the information that you need because it's all the schema is telling us, "Hey, look, if you want to go and find this client's audit or this video, and you

**8:58** · want to, you know, figure find where all the templates for Remotion are, for example, that's all done in the Claude MD file, and that navigation is set up.

**9:06** · And then in addition to that, from what we're talking about here is is per agent memory and being able to maintain what are essentially markdown files over time. Now, Claude's actually building I I think they're building this into their products cuz I've been seeing a lot about updating memory, stuff like that.

**9:21** · So, we we have a separate running memory markdown file that Claude will update, but it looks like this might even start to be built into the Claude product itself as well. But in essence, this is much more effective than rag because rag runs based on semantic search, but it's it's also overkill really to have to set up a vector database and maintain that vector database. This is way more lightweight, way easier to do. This is just overkill and unnecessary for what we're trying to do here.

### Per-Agent Memory

**9:49** · It's it's all about just data organization and using proven formatting like YAML and JSON to be able to store the information that we And because it's done in a controlled way, we can easily use scripts to filter information and extract exactly what we need even if the that file starts to get very, very large as long as it's it's correctly architected so that we can filter it down and and remove any unneeded or unwanted context from being injected into a conversation, that is all we need.

**10:20** · So, \[gasps\] yeah, understanding this structure and understanding how to actually organize a repository folder is \[snorts\] really, really important when you're building larger production systems and I'll I'll show you through the video editor in course. So, if we look at our video plugin, this actually corresponds directly to what we had in code in our code code plugin, so they're directly connected. But, this is exactly where we're actually building these agents.

**10:49** · And if we go down to an actual content so our projects, so if I come down to content and I look at our projects for example and I go to any video, let's just do this one. We can see we have our video ingest folder. So, this is where we're first going to drop videos in our video ingest folder. Then, what's going to happen is we're going to run the video agent. Uh we'll run the video agent that we have here. We're going to run the skill to edit long form. And what it will do is it will it knows to look to it in this exact folder for any raw video files. It'll process them and put them in the raw folder of the video editor.

**11:20** · Then, it will follow the workflow to actually proceed through every step on the transcription, run the audio analysis, build the storyboard.

**11:28** · Then, it will put the motion graphics in the correct folder. And see how it's all nicely organized in here? So, that it's labeled clearly so the AI knows exactly which folders to go to to extract the information that it needs to proceed to the next step. If you don't have this level of organization, what happens is the AI has to do its digging itself and it's running all these extra commands and pulling in all this extra information that's bloating your context window uh when and that's going to reduce the accuracy of your response in in short in short.

### Why Structure Beats RAG

**11:54** · Now, if you want to learn more about how to actually build these what Code is calling them plugins, AI first systems whatever you want to call it feel free to join my completely free school community. I'm pushing a lot of this content in there, templates, everything including this directly for free. And subscribe to the channel because I'm going to be showcasing these over the coming weeks and how they're dramatically reducing the time it's taking for me to do all sorts of things in my day-to-day activities. Thanks for watching.
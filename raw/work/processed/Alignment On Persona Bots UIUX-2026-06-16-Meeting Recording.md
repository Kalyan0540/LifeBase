

June 16, 2026, 11:34AM

18m 26s

**Bhanu Kalyan** started transcription

**Bhanu Kalyan** 0:04  
Mhm.

**Abhinav Dua** 0:04  
It is not to be a widget that surfaces within a lighter.  
And it's not some other platform that this gets embedded within. And the reason for that is very straightforward. If we have a dependency on Enlighter for every bot that we are building, then we are also going to have a dependency on the data to be within Doris.  
for the DP team to work on loading and updating it, for the ETL pipeline to support it, and so on and so forth. That can slow us down, so we would rather worry about just hosting the data in dollars and by coding the UI.

**Bhanu Kalyan** 0:43  
Okay.

**Abhinav Dua** 0:44  
Okay, now the good thing here is we also don't need to worry too much about white coding each and everything, because as if you remember, we had built some kind of a web app for the chat bot as well before it got converted into a widget within Lyta, right? We'll worry about the coding part later, but because this is going to be a web app, there are many factors for us to think about.

**Bhanu Kalyan** 1:02  
Okay.  
Uh-huh.

**Abhinav Dua** 1:07  
The first is a widget is a small part that occupies 20% of the screen in the bottom right, or wherever it is, right? So the form factor is in a particular way, and it mostly looks like a mobile screen that you're looking at. But when it comes to a web app, the web app is going to load on a screen in landscape mode.

**Bhanu Kalyan** 1:16  
Yes.

**Abhinav Dua** 1:27  
Right? So we'll have to think of is there a top header or a band in some way? Is there something that comes on the left? If yes, what does it contain? So what goes on the left? What goes into the top? Where does the core chat experience live? Where do the disclaimers appear? And so on and so forth.

**Bhanu Kalyan** 1:43  
Uh-huh.

**Abhinav Dua** 1:46  
Right, that is one thing that we'll have to think of. The second thing is, do we build the design elements, the brand guidelines, the color schemes, et cetera, independently? Or do we leverage or steal some ideas in terms of how things appear on the AI Hub or in Lighter or in Catalyst?  
Pretty open to that as well. All right, that's that question number of I'd say bucket #2 for consideration.

**Bhanu Kalyan** 2:10  
E.

**Abhinav Dua** 2:16  
The third is that unlike the chatbot, where we had a dropdown where we could choose the study we wanted to interact with, here we are going to have personas, right? And those personas over time could, I mean, I'm pretty open to even the idea of them having images or caricatures, right?

**Bhanu Kalyan** 2:27  
Right.

**Abhinav Dua** 2:36  
and not everything will be in the chat experience. We might want to see persona descriptions and definitions as well. So how does that happen? Will we hover over a persona and click a particular button and a small pop-up window will appear that will show the definition and another that will show the description?

**Bhanu Kalyan** 2:53  
Mhm.

**Abhinav Dua** 2:53  
or something else, right? So that's the other factor that we have to consider. So in other words, we are kind of starting the design from scratch, but wherever it makes sense for us to design it in a manner that there is a common thread or something that's an undercurrent that's common across the other applications as well, I'm open to it.  
But I do not want to be constrained by it.

**Bhanu Kalyan** 3:17  
Got it, got it.

**Abhinav Dua** 3:18  
OK, so these, yeah, go on.

**Bhanu Kalyan** 3:21  
Yeah, so, so majorly I wanted to know, like, if the users who are going to use this platform, are they going to be the same users from Enlighta or Catalyst, or is it a different base completely we are targeting from?

**Abhinav Dua** 3:34  
It could be a completely different base. So the people who are going to access it initially will be internal users, internal account teams that are the ones that are working on these surveys that lead to those data sets. But over time, we want to make this application client-facing as well.

**Bhanu Kalyan** 3:37  
Okay.  
Mhm.  
Got it.

**Abhinav Dua** 3:53  
So if, for example, the URL goes like, I'm just making this up, but let's suppose the URL is HTTPS colon 2 backslashes cogent CBB cogent persona bots dot investor beat. That's the name of the data set dot SQL and dot COO. Let's suppose that the.

**Bhanu Kalyan** 4:06  
Uh-huh.

**Abhinav Dua** 4:12  
URL. Clients should also be able to come in there, log in, and then get access to the bots. Right? So eventually this will be external facing as well, but internal, it does not, it's got no relation to Enlight or Catalyst in any way. It is basically people who are using it, the ones that have any relevance to that particular study or data set.

**Bhanu Kalyan** 4:13  
Mhm.  
Okay.

**Abhinav Dua** 4:34  
So a lot of cogent teams and overtime cogent subscribers are cogent clients as well, but even other clients like Bank of America and so on and so forth, depending on which data sets we decide to model persona bots on.

**Bhanu Kalyan** 4:47  
Got it. So this is not going to be part of like the existing products like in future terms as well. Let's say if and later clients want to use it. So we might not necessarily have the same kind of branding or teaming which we follow in and later for a specific line that might not be necessarily for this.

**Abhinav Dua** 5:06  
That's correct. That's correct. That's correct. It could be completely separate. However, if you're building a persona bot specifically for a client, we might need to adopt their brand guidelines in the persona bot application itself. So there should be flexibility for configuration files to be available.

**Bhanu Kalyan** 5:07  
It's like a completely separate offering.  
And.  
Okay.

**Abhinav Dua** 5:25  
configuration files where you decide color schemas, font styles, you know, logos and whatnot that can be configured for each and every deployment.

**Bhanu Kalyan** 5:31  
Mhm.  
Got it, got it. So we are kind of saying this is completely platform independent and in case if we are, if clients need customization, that should be like we should be able to do that for future case.

**Abhinav Dua** 5:36  
Okay.  
Yep.  
That's correct. Eventually, yes. So that's why it's important to define it and design it in a way that it's future ready.

**Bhanu Kalyan** 5:53  
Got it. Got it.

**Abhinav Dua** 5:55  
Okay.

**Bhanu Kalyan** 5:56  
Mhm.

**Abhinav Dua** 5:56  
So those are the main considerations, Bhanu. Frankly, that's about it, right? Initially, what will happen is on the AI Hub, there'll be a tile that will say persona bots. We click on persona bots, it will show a dropdown, and the dropdown is where people can choose which persona bot. Initially, there'll be only one. They'll click on that one, and they'll be redirected to this app.

**Bhanu Kalyan** 6:14  
Uh-huh.

**Abhinav Dua** 6:17  
That's it. So there is no other landing page, so to say, except what you are building.

**Bhanu Kalyan** 6:23  
Okay, got it. It's like an direct interactive page itself, no home pages, no landing pages, or direct.

**Abhinav Dua** 6:28  
Correct.  
No home pages, no landing pages, but do remember, see for internal users, I can just direct them through AI Hub. In AI Hub, in the login, I'll anyway capture the SSO detail, right? When they get into the persona board, that is where hopefully we will have a way to capture their email address because they'll be redirected from AI Hub. And then in my land fuse data and in my feedback component, I'll be able to capture all the logs in terms of how they're using.

**Bhanu Kalyan** 6:37  
Uh-huh.

**Abhinav Dua** 6:55  
using it, right? So that handover of the email address probably will need to happen between the AI Hub landing page and the Persona Bots page that we are building. And then over time, as we worry about clients as well, then of course, clients will not have access to AI Hub at the same time, right? They'll probably have a URL where they'll go in and they'll see a login page and they'll log in and then they'll see the page that we are also seeing.

**Bhanu Kalyan** 6:57  
Open.  
Got it. So that means we need an authentication page. It is not directly going to log in.

**Abhinav Dua** 7:19  
Right.  
But not right now. Right now for this initial thing, you don't need to worry about the authentication page yet.

**Bhanu Kalyan** 7:30  
Right, right.

**Abhinav Dua** 7:31  
Right? You can create a mock-up of it eventually, but the authentication page will be for the client. If users, internal users are coming to this particular page from AI Hub, AI Hub should be able to pass along the user ID for the person to use, right?  
So think of it this way, in AI Hub, in any particular tile and in any particular dropdown, I can always choose who can access it or not, right? So my authentication and authorization happens there. When you log into AI Hub, you are authenticated through SSO, and your authorization shows you a particular tile or a particular dropdown. So all of that is taken care of there.

**Bhanu Kalyan** 7:48  
Mhm.

**Abhinav Dua** 8:08  
But when AI Hub redirects to the URL, ideally AI Hub should be able to pass along the email ID of the person so that that can be captured downstream.

**Bhanu Kalyan** 8:17  
Got it, got it.

**Abhinav Dua** 8:18  
Okay, but that's a back-end developer's concern, not yours. Yours has to be more from a UX perspective in terms of what that page looks like. Whether I'm coming from AI Hub or I'm coming from any other portal or any other authentication page, I'm talking about the core application experience right now.

**Bhanu Kalyan** 8:28  
Right.  
Yeah, I mean, for now, like the authentication pages and subpages, I'll not consider, but anyways, like the user flow for the person about the interactivity and how the one behavior that I'll need to work on. So he has got it.

**Abhinav Dua** 8:49  
Yep.  
Right.  
So like I said, I did not want, I don't need answers to any of the questions right now. Of course, I do understand you have to think about it and we can keep brainstorming. My view was I should at least tell you some of these considerations that are crossing my mind. And of course, if you have generally questions to understand the concept itself or any other doubts that you have, now's a very good time to discuss those.

**Suveer Malhotra** 9:22  
Yeah.

**Bhanu Kalyan** 9:22  
Cool.  
So, I think last time when I had call with Suveer, I understood like the overall concept, like why we are going with the personal bots. Majority of them, like I think it's clear now, when like from you and Suveer both of you, but I just had one question that is regarding individual personal board. So, for example, if...

**Abhinav Dua** 9:39  
Mhm.

**Bhanu Kalyan** 9:46  
Let's say there is a person abort and if user wants to have conversations, is it going to be a new chat all the time or is it going to be a single chat where I'll be having a very long stream of conversation?

**Abhinav Dua** 10:01  
Right now, it's going to be one message exchange at a time. Over time, it will be a contextual chat, which means you can continue having a conversation for whatever time you want to. And then over time, there'll also be the ability to switch between personas. So what you might be able to do is  
you might be able to ask a question. And underneath, you can have a choice to choose which persona's response do you want to see to the same question, or if you want to compare two or three or four or five personas in a tabular format. But that functionality is far from being developed for now.

**Bhanu Kalyan** 10:21  
Mhm.  
Understood. And which means like currently let's say for I'm having like 2 questions which I want to ask for a specific persona. So I like conceptually and like not from the UI or UXY. I'm just thinking as a user I'll be selecting a persona which is a kind of user and I'll be saying.

**Abhinav Dua** 10:55  
Correct.

**Bhanu Kalyan** 10:56  
What do you think about this? I'll ask the first question.

**Abhinav Dua** 10:58  
Absolutely.

**Bhanu Kalyan** 11:00  
And it will be created as individual chat and which I can refer to it later. Will it be stored as an history or is it not for now?

**Abhinav Dua** 11:10  
Well, at this point in time, we're not worried too much about the caching bit. So just like the chat bot right now, we're not getting into caching.

**Bhanu Kalyan** 11:18  
Okay, so that is going to be just a temporary state like if we are seeing on the screen.

**Abhinav Dua** 11:21  
That's going to be a temporary, yes, that is going to be a temporary state, but that is also not something we have very actively explored right now. It might make sense for that to be taken care of upfront.

**Bhanu Kalyan** 11:28  
Ohh.

**Abhinav Dua** 11:34  
Right, but not right now. So my point is what you can always do is you can start creating mock-ups of forward-looking thoughts as well, along with the core things.

**Bhanu Kalyan** 11:34  
Okay.  
Uh-huh.  
Got it. Like the overall product.  
which we want, I'll have it and we can scope it out later for MVP or for the initial releases.

**Abhinav Dua** 11:54  
Sure.

**Bhanu Kalyan** 11:56  
Got it. And as you mentioned, like in future, we might also have capability of comparing multiple persona boards and creators in table format or some other visual format. So I'll also need to think on those lines, how the current, in case if I work on the design, it should be scalable enough. So.  
Yeah, I think now I got the...  
Parity on this part, and in case if I have any, I'll post you, post you both in that.

**Abhinav Dua** 12:20  
Okay.  
Okay.  
Absolutely. Absolutely, Bhanu. So what I would recommend is, as you start making progress, I think, again, you understand how much time you'll be spending on this and the speed at which we are progressing. But what I would say is, we do want to move on this reasonably fast. And I'll tell you the reason for that. At this point in time,  
we want to do a controlled alpha release of the persona bot with the Cogent team by mid of July. So for that, we first have to have some mock-ups ready. Then we have to brainstorm on those. Then we have to finalize them. Then we have to socialize them with a broader audience within the tech group. And then after that, we have to get to the point where somebody is able to start coding.

**Bhanu Kalyan** 12:53  
Mhm.  
Got it.

**Abhinav Dua** 13:10  
and developing, right? So what I would recommend is that it's Tuesday, today. I would say let's plan for maybe, again, if you think that's possible, that will be amazing. But maybe what we can do is we can plan for two 30 minute syncs every week, maybe on Tuesdays and Thursdays and Monday and Thursdays or Tuesday and Fridays, whatever you think makes more sense.

**Suveer Malhotra** 13:29  
Yes.

**Abhinav Dua** 13:30  
Right? And they don't always need to be completely 30 minutes. If not a lot has happened or the discussion happens sooner, we can always end early. But I would want to, you know, stay in touch on this. And if there is a need for us to meet even more frequently, I'm pretty happy to do that.

**Bhanu Kalyan** 13:30  
No.  
Got it. Sure, we can do that. Just a quick FYI, like this week, I think I'll be occupied with the enlighter part for the next planning week. So I'll be working on those designs. I'm not sure if I'll be able to spend a lot of time on persona bots for this week.

**Abhinav Dua** 14:00  
Okay.

**Bhanu Kalyan** 14:06  
In case if we...

**Abhinav Dua** 14:07  
So, Bhanu, I would suggest you have a chat with Tish around that, because my understanding from late last week and earlier this week was that she had mentioned that feel free to start working on the persona bot, and if you run into prioritization concerns, you can consult her. So, I would love for it to be parallel processed as opposed to only one thing in a week and only the other thing in the next week.

**Bhanu Kalyan** 14:16  
Uh-huh.

**Abhinav Dua** 14:27  
Just have a chat and see whatever it is that you can manage.

**Bhanu Kalyan** 14:30  
Sure.  
Cool, I'll talk with Tish on this part, and in case if even if Mahesh is available, hopefully if is, then it might be like a mutual task or even that can be split in design terms.

**Abhinav Dua** 14:48  
That's okay. That's for the two of you and Tish to decide collectively. So I'm okay with whatever you people collectively decide. But like I said, I wouldn't want to, you know, wait indefinitely to be able to kick it off. So if you can get something started this week itself, that'll be amazing.

**Bhanu Kalyan** 15:00  
Okay.  
Sure.

**Abhinav Dua** 15:07  
Okay.

**Bhanu Kalyan** 15:07  
Cool, I'll update you on this.

**Abhinav Dua** 15:10  
Okay, perfect. Suveer, sorry, I've been speaking non-stop. Anything additional from you?

**Suveer Malhotra** 15:16  
No, I think we pretty much covered everything. I think, Bhanu, you mentioned the three stages, or rather, I think Ed, you mentioned 3 stages. I would say right now, let's plan for a similar form where we have the different conversations in a single chat.  
Even if I think it's a single question, let's design it in the same manner because contextual conversation will come a lot faster than the other features. And second is I also saw a couple of examples for other companies how they build the chatbot. So some of them, what have they done is that they have the...  
the profiles as the buttons on the left, and then you can select one of them or multiple of them to kickstart the conversation. In our case, I think we have the ability, yeah, only with one profile, only with one profile.

**Abhinav Dua** 16:02  
Includ, yeah.  
Absolutely, absolutely.

**Suveer Malhotra** 16:09  
So let's maybe have the option that if we select one, the other deselects for now, and then maybe it shows up a message as I showed it to you, I think, in the mock-ups. So let's have a maybe think of something on similar lines. But again, you have the free hand, as AD mentioned, we are open for anything that you feel is.

**Bhanu Kalyan** 16:28  
Yeah.

**Suveer Malhotra** 16:29  
It works best from a U.S. perspective.

**Bhanu Kalyan** 16:32  
Right. I also had some very similar thoughts. I was like having a mental model of having it as an chat GPT projects. Like we have list of projects and users can have conversation for each project and each projects can have multiple chats. So I'm thinking of a kind of.  
It's a very similar mental model, like each project can act like a person or bot, and conversations can happen within the projects, and in case...  
We need a better way of navigating like basis on the constraints. I'll also see if there are any other ideas what works best for this and we can discuss on that.

**Suveer Malhotra** 17:12  
Okay.

**Abhinav Dua** 17:15  
So the only perspective I would have there is I would want to at least see a couple of options for the landing page mock-ups before we decide which one makes the most sense. And when I say a couple of options, I don't mean to say give me four or five options. Even 2 are fine. They just need to have substantive variety so that we are able to see what the other thing looks like.

**Bhanu Kalyan** 17:38  
Yep, yep.

**Suveer Malhotra** 17:41  
Okay.

**Abhinav Dua** 17:44  
All right.  
Cool. Anything else?

**Bhanu Kalyan** 17:51  
Ah.  
I think that's it from my side and just one small request. If possible, can we create a ticket inside UX board so that it's easier for me to track and also prioritize?

**Abhinav Dua** 18:06  
Sure, Bhanu, I will let you and Suveer coordinate on that.

**Suveer Malhotra** 18:08  
Mm.

**Bhanu Kalyan** 18:09  
Sure.

**Suveer Malhotra** 18:09  
Sure, pardon, right? Why not? I will connect with you separately on that, on how you typically manage though at Jira board, otherwise all good.

**Bhanu Kalyan** 18:18  
All right.

**Abhinav Dua** 18:20  
Okay.

**Suveer Malhotra** 18:21  
Yeah.

**Abhinav Dua** 18:22  
Thank you, both.

**Suveer Malhotra** 18:23  
Okay, thank you.

**Bhanu Kalyan** 18:23  
Thank you.

**Abhinav Dua** 18:24  
Bye.

**Bhanu Kalyan** 18:25  
Bye.

**Suveer Malhotra** 18:25  
Right.

**Bhanu Kalyan** stopped transcription


This comes as part of AI/Persona Bots
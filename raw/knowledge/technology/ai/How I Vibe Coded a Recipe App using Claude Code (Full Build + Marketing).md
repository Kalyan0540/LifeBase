---
source_title: "How I Vibe Coded a Recipe App using Claude Code (Full Build + Marketing)"
source_url: "https://www.youtube.com/watch?v=9atd5lczG2k"
created: 2026-05-30
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=9atd5lczG2k)

I found an app called ReciMe that makes $800,000 a month, and I rebuilt it using Claude Code without writing a single line of code. In this video I walk you through how to design and build a full iOS app in 2026 using Claude Design for the frontend and Claude Code or Codex for the backend, plus how to add real AI features with the OpenAI API. This is the exact workflow I use to go from idea to a working app on my phone.  
  
🎯 Try Kittl (25% OFF with code JASON): https://kittl.pxf.io/YVR6qr  
  
📂 Download the FREE App Store Checklist: heyjasonle.kit.com/appstorechecklist  
🚀 Want more ideas? Join my FREE Newsletter: https://www.thebreadcrumb.co/  
  
Links Mentioned:  
\- Claude Code: https://claude.ai/code  
\- OpenAI API: https://platform.openai.com  
\- Supabase: https://supabase.com  
\- RevenueCat: https://www.revenuecat.com  
  
Timestamps:  
0:00 Intro  
0:11 What is ReciMe  
3:58 Tools Needed  
5:10 Claude Code Setup  
6:52 Start Building with Claude Code  
8:15 Claude Design (Building Frontend)  
15:03 Sponsor  
17:04 Claude Code (Building Backend)  
20:18 Adding More Features  
25:32 Preview App on Phone  
29:44 Adding Database and Paywall  
32:35 App Store Checklist  
  
Connect with me: jasonlee.partners@gmail.com  
  
#claudecode #startupideas #claudedesign

## Transcript

### Intro

**0:00** · I found this app that makes $800,000 a month. And I just built the entire thing without writing a single line of code.

**0:07** · So this app is called and it basically lets you grab a recipe from any website or even a YouTube video and uses AI to organize everything into a clean collection of recipes. So, in this video, I'm going to show you a step by step in how to design and build this app using cloud code, including all the features, how to add the AI functionality, and how to even test it live on your phone. And not only that, but I'm also going to show you how they market the app, cuz you can build this app, but you're not going to make any money if you don't know how to get paying users.

### What is ReciMe

**0:35** · So, I'm going to show you what they did to market this app so you can see what's working for them and adapt it for your own app. And if you're a beginner, don't worry. I didn't touch a single line of code building this app.

**0:46** · I just basically had a conversation with Claude in plain English. So if you've used Claude or Chat to be before, you'll definitely know how to do this. But before we start building, let me show you what this app actually does. So the core functionality of this app is basically very simple. So let's say you're watching a recipe on YouTube and you want to save it. Normally you'd have to manually dig through the description here and copy everything manually or if it's not here, if it's on a website, you have to click here and you have to copy and paste everything.

**1:14** · It's very manual and then you're probably going to dump it in your notes app and it will get very messy and very hard to manage once you have multiple recipes. But with this app, you just paste in the link and the AI pulls everything out and puts it into a clean recipe card with all the details right there. Or you can also scan a physical recipe like this. Maybe you have an old recipe that you want to bring into the app. You can just take a photo and you can have the AI reads it and format it in the same way. And because the app is AI powered, it can also give you an estimate of the calories, which is a really nice feature to have.

**1:45** · There's actually another app called Calai that does something similar. You take a photo of your food and it counts the calories. And and this app is making millions of dollars. So there's clearly a demand for this kind of thing. And speaking of demand, the app that we're building today is recipe.

**1:58** · So this is a validated idea and people actually want to use this tool. And by the way, there are two things that makes an app like this very attractive to me.

**2:06** · First, recurring revenue, obviously, $800,000 every single month. And secondly, it is quite sticky because once you sign up, they make it hard for you to leave, right? Because imagine if you build a collection of 20, 30 recipes. If you cancel, you lose everything. And that layer of stickiness helps reduce churn. And there's also a huge potential for a good exit here.

**2:25** · Apps like this typically sell for two to four times its annual profit. So you can check this data on acquire.com or flippa or even Trust Mr. And just to give you guys a rough estimate, let's say this app makes 50% margin. So that is $400,000 a month times 12 months, that is $4.8 million a year in profit, which means that even with a low multiple of 2x, you can potentially sell this for at least $9.6 million, which is pretty sweet. Now, there are already some players in the market, which is actually a good sign in my opinion.

**2:55** · It just means that there's really strong demand for this, and all you need to do is build a version of this that is unique. And I think one idea is that maybe you can target a specific demographic, like maybe target a particular country, which is exactly what this app is doing. This app is called Cookpad. It was created for the Japanese market. And they're actually making $900,000 a month. And this just proves to me that narrowing down or niching down does not mean you're going to make less cuz you may potentially do better cuz there are particular things that different cultures value that maybe we don't.

**3:24** · So if you build around those things, your app is going to feel more personalized to that demographic. So, there are a lot of ways to position your app. But just to be clear, the goal of this video today is not to tell you to clone this app and expect to make $800,000 a month, but I just want to show you what's possible today with building mobile apps, the workflow behind building something like this, and also how to market it. And this knowledge will apply to whatever app that you end up building. Now, I'm going to show you the full setup, but feel free to jump around if you're already familiar with some of these things. I'll have timestamps in the video to make it easier.

**3:54** · Now, to build this app, we're going to use two main tools. All right, so first is Claw Design. So, we're going to use this to design the user interface, which is basically what you see in terms of design, the buttons, the colors, and all of these things, right? And the second tool here is cloud code, which is what we're going to use to build the backend functionality of the app. And I'm going to show you how to connect these tools together seamlessly. Now, if you're using Codeex, you can also follow along.

### Tools Needed

**4:20** · It works the same way. I think that the Codeex desktop app is very similar to Cloud Code. So, if you're using Codeex already, the workflow is going to be identical. Now, for the framework, we're going to be using React Native. So, if you're not technical, think of this like the building materials for mobile apps, right? It's what makes all the buttons work, how the pages swipe, and all these things. And the main reason that we're using React Native is that it works both on iPhone and Android. So, we're actually building for both platforms on a single codebase. And we're also going to use Expo Go.

**4:49** · So, this is the tool that we're going to use to be able to preview and test the app on our actual phones. Now, at the end of the video, I'll also cover what you need to check before submitting your app to the app store because there's a lot of bycoded apps that are getting rejected recently.

**5:04** · So, I put together a checklist here for you to cross check and I'll show you where to grab this towards the end of the video. All right, so let's start building. First, you want to download Cloud Code. So, if you haven't already, you can go to Claude and download the desktop app. And by the way, you're going to need at least the $20 subscription to get this started. And if you're here for the first time, you will see three different tabs here. You got chat. This is where you ask questions and it will give you an answer.

### Claude Code Setup

**5:25** · And then you have co-work and code which is basically the same thing but I prefer code because it's more capable and I think if you are serious about building things I do recommend using cloud code instead of co-work and yes I know the word code may sound intimidating for some people but we're not going to be working in the terminal today. So we're going to use the desktop app which is very userfriendly. So if you know how to click buttons and you know how to prompt in plain English this is going to be pretty easy. Now before you start prompting you want to make sure that you're working in a folder. So I like to keep things organized.

**5:56** · So for every project I like to work in a specific folder. So here you can see that I have called this project recipe snap. If you click here you can change the folder. So you'll see here that I've already connected it to recipe snap folder here with some images for reference. But if you're doing this for the first time obviously you just want to create new folder here and just connect to it and hit open. Now, for the AI model, I like to use Opus 4.7 when I'm planning the app, when I'm structuring the app because I want the smartest model to be able to think through all the functionality behind the app.

**6:27** · But once that's done, when I start building the app, I like to switch to Son of 4.6 because it's faster and it uses a lot fewer tokens. So, if you are on the $20 plan, you want to conserve tokens. This is something that you want to be aware of. But obviously, if you're on the max plan, you don't need to worry about this. Now, before I start building any type of app, I like to always plan out the features and the structure of the app because you want to give Claude some type of guidance in what to build the features that you want. Otherwise, it's going to build something that you don't like and you're going to have to keep regenerating and waste a lot of tokens.

### Start Building with Claude Code

**6:58** · So, what I'll do now is actually go back to this app store page for ré and grab the URL and paste it in here and just say that I want to build an iOS app like suggest all the features that I should have and then hit enter and then it's going to study this page and do some research and it's going to give you some features that it thinks that you should implement. All right, so it's giving me a lot of features now. It's writing. So, you got the universal recipe import.

**7:22** · So, that is the primary function of this app. manual entry, you got a library, cook mode, a built-in timer, shopping list, right? All of these are primary functions of the recipe app. And you can just pick and choose which one you want.

**7:38** · And then we're going to start designing the app. So, I'll just prompt it again.

**7:42** · I want to implement features 1 through 8. And I'll be using another tool to design the UI first. So, give me a breakdown of all the pages and features in detail. Format it so I can just copy and paste. Once the UI is built, I will be bringing it back here for you to build the back end.

**7:59** · And you want to hit enter and it's going to compile everything and just grab the first eight features and it's going to format it in a way that's easy for you to copy and paste because we want to bring this over to claw design to design the front end of the app. So once it's done, you can just copy and paste the whole thing and you want to bring this over to cloud design. Now to access cloud design, you have to go back to your browser and you want to just type in clot.ai AI and over on the left side you're going to see something called design here. So click on this one and you're going to land on this page which is claw design.

### Claude Design (Building Frontend)

**8:29** · Right now the main reason why we want to use claw design instead of designing directly on cloud code is that I think that claw design is the best for designing any type of app or landing page by far. Now I spent a lot of time on this when I'm designing directly on cloud code. It usually doesn't give me what I want. it is messy. Even though I have the front-end design skills installed, it's still giving me maybe 50% there. So, there's a lot of tweaks and a lot of reference that I have to feed it to even get it to 50%.

**9:01** · But when I'm using cloud design, it usually gets you to about 95%. And you'll see why in a second. But that's the main reason why I use cloud design.

**9:10** · And then from here, you can easily bring this over to cloud code to build the backend functionality of it. All right.

**9:16** · So, once you're here, you just enter a project name. So you can put something like recipe snap app. And you want to choose high fidelity and just hit create. And then you want to just paste the prompt that you got from cloud code. So I'm going to paste it here. And you'll see that it's pasted 205 lines. It's the exact prompt that I got from cloud code. So if you want to see the actual prompt, this is what it looks like. Design a polish iOS mobile app called recipe snap inspired by app like résumés. Right? So, it's got the pages and the screens that I want.

**9:50** · So, it's very detailed. Gives Cloud Code a lot of guidance in what I want. And it's got all these different screens, even the buttons that I want implemented. There's a search bar here, a shopping list screen, and also a payw wall. And and everything's here. And Cloud Code came up with all of these without me having to do anything. So, my job now is just to go through all of this and see if I'm happy with everything, and then I'll put it into Cloud Design. Now, there's one more thing that I like to always do before I send it off.

**10:18** · I like to find a design reference, and I like to go to Pinterest for this. So, if you go to Pinterest, you can search by recipe app. And what we're doing here is we want to find a design that we like. So, the output is going to be as close as possible to what we want. Right? So, I found this one that I really like. I think it's pretty clean. It's got this green that I think looks really fresh and I do like the way the buttons look and how the different colors come together.

**10:45** · And what I want to do now is just save this image and just save this in that folder that we're working in and hit save. And then go back to claw design, add a screenshot.

**10:56** · And this is the screenshot that I want to attach. And I'll just hit open here.

**11:00** · And it's in here. So I've got the prompt here and I've got the screenshot. It's ready to go. So I'm going to hit send.

**11:05** · And this will usually take about 4 to 5 minutes. So I'll come back when this is ready. All right. So it looks like it is done. So it created all the pages here.

**11:13** · You will see that these are all the assets that it created, all the design files. And here is the page that you want to click on. Click on this one.

**11:20** · Open a new tab. And there you go. That's the app. So it actually followed the design reference that I gave it from the screenshot. And also looks like this is the dashboard where I can just scan a photo. And if I click on get started here, there you go. So, this is the collection page and you see we've got four different tabs here. Home, library, shopping, settings. And if I click on one of the recipes here, let's see if this works. Yeah, it works. So, it has a photo, it has the prep time, cook time, cook mode. This is a dummy data obviously, but all of these are clickable, right?

**11:51** · So, I can uh check it off and I can even edit it apparently.

**11:56** · So, edit recipe and I can add more text here. Yep, there you go. And I don't think this will save changes. It's just dummy. Yeah, it doesn't save the changes, but this is really, really good from just one prompt. So, let me go back to the main page and let's see what I can see here. Recipe and let's click on library. So, I can see all the meal types here. It's already categorized nicely. And if I go to shopping, uh it creates a shopping list for me. So, this is exactly like what recipe has. And I can add items manually.

**12:27** · Let's say I want to add white pepper.

**12:32** · Yep, there you go. So, I can probably add the the category here, but that's something that's easy to add as well.

**12:40** · And settings. So, settings, uh, I can choose the measurement units. Uh, I wanted dark mode. Maybe that doesn't work yet. Uh, upgrade to pro. Yep. So, that is the the the payw wall. Yeah. So, I like it. Now, the nice thing about cloud design is that it automatically gives you tweaks. So, tweaks is basically some options that you get immediately if you want to preview your app in different colors, right? So right now it's sage. So if I click rust, it's going to change everything into rust, right? So it changed the colors globally. So in every page it followed that color theme.

**13:12** · And if I go to ocean, it gives you this nice teal blue color or plum and it carries over to all the pages here, which is really nice. But for me personally, I think I like the sage is what the reference design looks like.

**13:27** · And obviously if you want to make more changes, let's say you want to move a button here to somewhere else, you can just do a markup and you can just click on this one and you can move this under the scan recipe button maybe. So center clot and then it will make that change.

**13:48** · And there you go. Done. Scan recipe is now the primary dark card at the top and they just swapped it for you. Now I think at this point we're ready to bring this design over to cloud code to start building the back end. Now keep in mind that even after you bring this over to cloud code, you can still make changes to the design. So let's say you want this to be a button instead of a text, you can do that as well. But the reason why we're using claw design for this is to get all of these design elements nicely positioned, nicely colored like this.

**14:15** · Because if you were to do this directly in cloud code, you usually won't have the shadowing and you won't have these nice buttons, especially if you don't give it enough reference. Now, once you're ready to bring this over to cloud code, you can click share here.

**14:29** · And there's a couple of options to do this, right? So, you can download this file as a zip file or you can click on hand off to cloud code. But today, I want to download this project as zip.

**14:38** · So, I can save it to the folder. So I can click on here and here is the zip file that I downloaded and I want to just unzip it and I'll just rename the folder recipe snap design and I'm just going to delete the zip file here. So you will see that all these files here are exactly the design files that it created for you. Quick break from our sponsor KD. The design tool that I've been using quite a lot lately. So the biggest difference with KD is that whatever design that you want to create, you don't have to start from scratch.

### Sponsor

**15:08** · They give you a bunch of examples and templates because that is the problem when I'm designing. I always get stuck on the idea. But with KDO, they basically have templates for any type of product that you want to promote.

**15:18** · Images, posters, and even UGC videos, which is really powerful now for marketing your product or your app. So if I find something that I like, for example, this woman here eating a cookie. So I just click on it. And this is completely AI generated. By the way, this was made using the Cance 2.0 model inside of KD. And the AI has gotten so good that it's not only holding a product anymore, but it's now eating food. And I think it looks flawless. And what if I told you that this was actually created by just uploading two very basic images. And I'm going to show you how to do that.

**15:47** · If you click on use template here, you'll see exactly how this video was created, what images were used. And in this case, it's these two images here, which is the brand logo and the cookie itself. And it used the latest nano banana to take these two images and create a product shot like this. And with that product shot, you can animate it into a video like this.

**16:07** · So if you click on this video here, you can even see the exact prompt that was used. Create the video. So you don't have to figure out the prompt. And you can even see the model that's being used here. So all you need to do is just copy this prompt and adapt it to your product. And you also get this nice wireframe which allows you to have more control over what the AI will do scene after scene. So this is one of my favorite features. So, as you can imagine with KD, you can create a huge volume of content very, very quickly, especially with the help of these ready-made templates. So, you spend less time figuring out the AI, but actually producing results.

**16:38** · And on top of the AI features, KD is actually a full design platform. So, where you can create banners, posters, and even Instagram posts and stories. So, you can literally do anything design related all in one place. So, if you want to give KD a try, I'm going to put the link down below where you can start creating some designs. They've got a free trial here, but when you're ready to upgrade, use my code Jason at checkout and you're going to get 25% their pro or expert plans.

**17:02** · So, thanks again KD for sponsoring this video. Now, back to Claude. All right, so now I'm back to Claude and I'm just going to copy and paste this prompt here. I've added the design files in a folder called recipe snap design. build this app from my design file using Expo React Native with TypeScript for the mobile app and use local device storage for safe data and a small NodeJS express backend for AI functionality so API keys stay off the phone. So you want to do that to make sure that your API keys are not exposed. The app should run on my real iPhone through Expo Go.

### Claude Code (Building Backend)

**17:32** · Use OpenAI API for recipe extraction. Please inspect the existing design first, then wire up the functionality based on the design and run it on my local machine for preview. Now, for this, I'll just use Sonet 4.6 because it's not a complicated app. Unless I run into some issues, then I'll switch back to Opus.

**17:51** · And I'll just go ahead and hit send and then wait for it to process. Now, it's going to analyze all the design files that was created by Cloud Design and it's going to give you the next steps.

**18:01** · All right, so looks like it's done. So, it pulled up the preview here on the right side and it took about five six minutes. It It was quite a lot of pages that it had to build. So, let's see if everything works, right? So, if you scroll down here and get started. Yep.

**18:15** · Um, so if I click on the recent recipe here. Yeah. So, this looks like exactly what we had on claw design, which is really good. Yep. I can check this off.

**18:26** · So, let's try if this cook mode works.

**18:29** · So, yeah, there you go. So, so it gives you this nice format to look at when you are actually cooking. So, next step.

**18:36** · Yep. So, all of this works correctly.

**18:38** · And if I go to exit. Okay, that works.

**18:41** · Edit recipe. And let's see if this will actually take in the changes. And if I go to save changes. Uh, not yet. So, I can have that fixed as well. And if I click on add to shopping. So, this is not working yet. So, so I want to see what is working and what is not. And if I go to shopping, uh, does this work?

**19:04** · Yep, it does work. So, all right. So, now let's say you want to make changes.

**19:08** · So, what's nice about having this preview on the right side is that you can just annotate what you want and then tell Claude to change that specific thing, right? You can click on this pencil icon here and you can just circle and you can just click add to chat and then it will appear here and then you can just type in what you want, right?

**19:28** · Or you can also click on certain elements. So let's say I want this color to be green instead of orange. So I can click on this and it will select the exact UI element that I want to change.

**19:40** · Right? So I can change this to green.

**19:44** · Hit enter and it will just change that very very quickly. And there you go. The progress bar is now green. Matches the heading and primary color throughout the app. Now let's go back to the homepage.

**19:55** · And I want to see what happens if I click on scan recipe. So this is the place where you want to take a photo of the recipe. It does not work yet because we have not connected the API for this.

**20:04** · But if I click on this, it will actually show you the animation. Scanning image, extracting ingredients, and then creating the recipe. So that is the workflow here, which is really nice. But before I connect the API, let's say you want to add a feature, right? You're at this point and you want to add a feature. And maybe you don't know what feature to add. You can also ask Claude, hey, I want to add some features to this app that is unique, that has a wow factor. Give me 10 ideas that I can implement for this app. And it's going to go and give you a couple of ideas.

### Adding More Features

**20:35** · All right, so let's go through the list quickly. What's in my fridge? Serving size, scaler, recipe, remix. All right, so this is interesting. Make it healthier because a lot of people are conscious about their calorie intake. So let's say you have this dish here and you want to make it healthier. There's a button to click and then it just updates the ingredient list and it gives you a substitution. Maybe heavy cream becomes Greek yogurt. I think that's a great idea. Let's implement that one. So, let's prompt it again. I want to implement idea number five. I'm thinking about a button called make it healthier.

**21:06** · And when someone clicks on it, it will adjust the ingredients and make it healthier. So, build this into the app and show me the preview and hit enter.

**21:14** · And then I'm going to let it cook and come back in a couple minutes. All right. So it looks like that is done as well. So you can see the preview here.

**21:21** · It added a new button here called make it healthier. So let's give it a try.

**21:25** · Click make it healthier. Analyzing ingredients. There you go. So it gave you a couple of substitutions here.

**21:30** · Spaghetti becomes whole grain spaghetti.

**21:32** · Heavy cream becomes Greek yogurt. That is awesome. That's really nice. And keep in mind that if I click tap to revert.

**21:38** · Okay. So it goes back to the original.

**21:40** · Keep in mind that this is just dummy data for preview only. So when you're actually launching the actual app, it's going to also call the OpenAI API to perform this task. So you do need the API key for this to work. Now speaking of AI keys, that's what we're going to set up next. Now, I know a lot of people they are confused about what an API key is and why do we actually need this?

**22:01** · So, for example, when somebody snaps a photo of a recipe, let's say you have an old recipe on a piece of paper and you want to take a photo with the app, the app will take that image and send it to OpenAI, right? The AI looks at the photo, it reads all the text and figures out what the ingredients are, what the steps are, and sends it back as structured data that this app can display in a nice clean recipe card like this, right? And also the make it healthier option, right?

**22:29** · When you click on this, the app will call OpenAI and in the background, the AI will process the information and give you the output that you want. Now, to get the API, you're going to need some API credits. And this is not your normal chatbt subscription that you pay monthly. It is actually a pay as you go credit that you need to top up. But before I show you how to add some credits, I want to show you the pricing for the EI model that we're going to be using. And if you don't know which one to use, you can actually ask a lot to give you the best one for this purpose.

**22:59** · And for our specific app that we're building today, we're going to actually use GBT 5.4 mini. Now, the amounts here might be confusing to you.

**23:07** · Essentially, what we want to know is how much it costs when a user takes a photo and extracts an image, right? We want to know the cost. So, I asked Cloud Code to put that in perspective. So, if a user extracts a recipe from an image, it will cost you half a cent here. And if they're doing a 100 image scans, it's going to cost you 50 cents to a dollar.

**23:27** · And a thousand image scans is $5 to $10.

**23:30** · So it's very very cheap. I don't think most people are going to do thousands of scans every single month. They may do a hundred maybe the first month. And even that the cost is only going to be a dollar. And if you charge $10, that's 90% margins. And in the subsequent months, they're not probably going to use up 100 scans every single month.

**23:48** · Also, keep in mind that the more scans that they do is actually better for you cuz they get more invested into your app. Again, imagine if you already have a thousand recipes in the app. It makes it hard to leave. Right now, to get the API key, it's also very easy. You want to you want to go to platform.openai.com and you just want to add some credits.

**24:08** · And I have about $4 here. And this API runs on a pay as you go credit system.

**24:12** · So, add money to your account. So, let's say you add $10 or $20. It draws down from that balance every time the app makes a call to OpenAI. And once you top up your balance, you can just go to API keys here and you can create a new secret key. And you can just call it recipe snap default project and create secret key. And then you can just copy the API key and bring it over to claude.

**24:36** · Now once you have the API key, you can give it to Claude. But you don't want to just paste it here in the chat because if it gets leaked, anybody can access your keys and they'll just drain your account. So what you want to do is you want to save the API key in a file called AENV file which is an environment file and for this you can also ask claw to do it. You can say something like hey create av file for me to paste in the API key and show me how to access that file and then hit enter. Okay. So, I can just close this off. And then I can go here and click on files.

**25:07** · And under backend, right, it's in this location here. And I can just click on this. And then paste in my API key here. And I'm going to hit save and close this off and say it's in. All right. So, looks like it is loaded and backend is back up with your key loaded. Now, the next step is to preview this app on your phone. Now, in order to do that, you're going to need to download something called Expo Go. So, this is something that you can download for free from the app store.

### Preview App on Phone

**25:39** · So, go to your phone and look for this app in the app store and go ahead and download it. All right. Once you download the Expo Go app, you want to ask for a QR code. So, you can just use your phone's camera and scan it and it will load up the app automatically. Now, normally you have to do this on a terminal, but you can also ask it to give you the code here. And it did that actually. So, what you need to do is just to click on this one here and look for the PNG.

**26:06** · And you can just now grab your phone and just try to scan this and click on that. There you go. And the app is now loaded on your phone. So now I can browse through and see if everything is working correctly. So if I click on creamy garlic pasta here, you can see everything is loaded up nicely and I can check any of these boxes here. Um let's check the cook mode.

**26:31** · Yep. So, that works exactly like it did on cloud code. And if I go back to library, yeah, it's all here. Perfect.

**26:41** · All the categorization works. Shopping works as well. And this is the green progress bar that we edited. Now, I want to test the primary function of this app, which is to scan a recipe, right?

**26:53** · Because we connected the API key, and I want to see if that works. So I click on this one and I want to take a photo here and and I found this recipe on Google that we can test this with. So I can just click on take photo here and I will just put that in the frame and take a photo and see if that captures the information. Use photo scanning image extract ingredients recipe card.

**27:16** · Amazing. So that did it. So it took the messy handwriting here and turn it into a really nice recipe card. And you can just hit save recipe here to bring it to your collection. And the only thing missing here is probably the image because this original recipe doesn't have one. But what you can do as well is you can ask cloud code to automatically generate an image like a random image so that it doesn't look blank like this.

**27:40** · Right? But that's very very easy to add.

**27:42** · So I'll just hit save recipe and it's saved to the library. If I go back to the homepage, yep, it's right there. So that's still missing the homepage. Now the other thing that I want to try is pasting a link from YouTube. So, I'll just use this smashburger recipe again for example. So, I can click on this share icon here and then hit copy link.

**28:01** · So, it'll grab the YouTube URL and put it into the app. But normally, what will be nice if your app will actually show up under the share here as one of the icons, but we're not able to test that because this is not a real app. It's on Expo Go. But if your app is published and it's installed on the phone, you can actually show up as one of the icons here and the user can just click on the app and it will automatically push the URL to the app. But for now, we're going to do it the manual way, which is copy link. Go back to the app and paste in recipe link.

**28:29** · And then I'm going to hit paste here and then I'm going to hit extract recipe. That is beautiful. So it took everything in including the instructions as well and actually gave you a reference here imported from certified angusbeef.com and it also pulled in an image as well. So obviously this is from a YouTube video but it was actually able to go to the YouTube description here and if I click on description it has the ingredients here but the website is actually this one here. So actually pulled in the image from this website here which is pretty nice.

**29:00** · So let me go back to the app and then I'm going to save this as a recipe.

**29:04** · And there's one more thing that I want to check which is the make it healthier option. So if I go back and the burger is here and then let's say I want to make this healthier. Click on make it healthier. And now it's because your API is connected. It's going to use AI to actually analyze this and make it healthier. There you go. So obviously you can customize on how healthy you want this to be. You can code that into the system.

**29:27** · But I just want to show you that something like this can be viodated easily with cloud code and it can be added easily and I think the apps looks really really good considering that we just vioded this in just about 10 15 minutes. Now let's say you're happy with the app. The next step is you want to add a database right a database simply means that you want to have someplace where the user can store their data.

### Adding Database and Paywall

**29:50** · Right? So all the recipes all the settings here they have to go somewhere.

**29:54** · That's where you need a database. So for database you want to use superbase for this. It's a very common option for mobile apps. So cloud code will know how to connect this for you. And also secondly you need a tool to take in payments to manage your subscriptions.

**30:06** · So for this we can use revenue cat here is very popular and it's approved by Apple. Using something like this it just makes it really easy for you to manage your user subscriptions and also very common which means that cloud code knows how to integrate everything for you. And last but not least you also need to get an Apple developer account. This will cost you about $99 a year. But with this subscription, you can publish as many apps as you want. So it's just one time for the year. All right. So now you have built the app. The next important thing that you need to do is think about marketing.

**30:37** · And I would argue that this is actually more important than the building itself cuz anyone can now vibe code an app. But if you don't know how to get users, you're not going to make any money. Now for an app like this, the best place you want to start is by looking at how your competition is already getting users. And the first place I would look at is Tik Tok, right?

**30:53** · So if you search for resume on Tik Tok, you're going to see that they have their own account and they're creating this type of UGC content and they're also paying influencers and also reposting those videos on their account. And for those of you who are not familiar, these are short videos where someone just shows a quick hack or a tip and at the end the app is the solution, right? So you've seen these videos before. It's the I wish I knew this sooner kind of format and someone shows the problem and then shows the app solving it in like about 10 seconds. It is super simple but very effective.

**31:22** · Now I think if you're building an app like this, you have three options here, right? The first is you can create your own Tik Tok account and you can start posting these videos yourself. You just post videos and if one of them goes viral, you get a flood of free users, right? But the downside is it takes a lot of time and you got to be consistent right now. The second option is you can pay UGC creators to make these videos for you. So typically you'll pay a fixed fee. They make the video and you pay something once and the video keeps bringing users long after you paid for it. Now the third way is using AI UGC. So you're actually using AI avatars to create these videos.

**31:53** · So you can use tools like Arcats here to create these UGC videos with very realistic personas or you can also use Hickfield which is a very popular option and this is exactly what a lot of successful apps are doing right now where they create multiple Tik Tok accounts with different AI personas.

**32:12** · They post a high volume of content and when they see a video that goes viral, they'll take that video and put ads behind it. So you can see the marketing strategy for this type of app is actually very simple. You want to create a lot of content. You find out what works and then you want to scale it with money. Now there's one last thing that you need to know before you publish your app to the app store because there's tons of issues recently with a lot of vioded apps that are getting banned from the app store. And it's not that Apple are banning vioded apps, but a lot of these bipoded apps are missing a lot of security layers and they're not reliable.

### App Store Checklist

**32:42** · So I've actually compiled a list of things to look out for before you publish your app. So, I've done the research here and I've got about 18 items here that you want to look out for and make sure you have all of these checked off before you submit it to the app store. Now, if you want to grab this checklist, I'm going to provide that in the description below. And you can even copy and paste all of this information into cloud code and ask it to go through the list and make sure that your app covers everything. All right, so I hope you guys get value out of this video.

**33:09** · And by the way, tell me in the comments what you want me to build next or what video you want me to create or what are you struggling with so I can address that in my next video. Now, if you want to watch another video of me building another app, I recently made a video here on how I vipcoded a coin identifier app that makes about 400k per month with cloud code. So, if you want to see that video, click here and I will see you there.
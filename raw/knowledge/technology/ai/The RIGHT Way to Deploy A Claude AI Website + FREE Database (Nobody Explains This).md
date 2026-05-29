---
source_title: "The RIGHT Way to Deploy A Claude AI Website + FREE Database (Nobody Explains This)"
source_url: "https://www.youtube.com/watch?v=MQk8xyZEKYg&list=WL&index=17"
raw_path: "raw/knowledge/technology/ai/The RIGHT Way to Deploy A Claude AI Website + FREE Database (Nobody Explains This).md"
created: 2026-05-28
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=MQk8xyZEKYg)

Connect Domain To Hosting: https://darrelwilson.com/hostinger-node  
Go To Claude Ai Studio: https://claude.com/download  
Mac Version: https://www.youtube.com/watch?v=EuyqMycBlSY  
  
Resources  
  
Download Node.JS: https://nodejs.org/en  
Download GIT: https://git-scm.com/install/windows  
https://share.evernote.com/note/c394f433-0fb4-61b5-7a91-fc5e0f884626  
  
Learn the right way to deploy a Claude AI website and take your AI-generated project from your computer to a real live domain. In this Claude AI website deployment tutorial, I’ll show you how to publish your website online step-by-step, connect it to a domain, set up hosting, and make sure your website is actually ready for real visitors.  
  
Timestamps  
  
00:00 Intro  
01:15 Download Resources  
03:51 Prompting  
06:30 Push to Github  
09:03 Connect Domain To Ai Website  
14:15 Connect DataBase (Optional)  
24:52 Outro  
  
A lot of people use Claude AI to build websites, apps, landing pages, dashboards, and online tools, but they get stuck when it’s time to launch. Your website might work perfectly on your computer, but that doesn’t mean it’s ready for the internet. In this video, I’ll show you how to properly deploy your Claude AI website so it can be accessed from anywhere in the world.  
  
We’ll cover how to prepare your website files, how to upload your Claude AI project, how to connect your domain name, and how to make sure your website works correctly after deployment. I’ll also explain the benefits of deploying your website the right way, including faster loading speeds, better security, business email setup, CDN support, malware monitoring, cache control, and easier website management.  
  
If you’re using Claude AI to build a website and you want to launch it professionally, this tutorial will walk you through the full process. Whether you’re a beginner, freelancer, business owner, or someone building AI websites for clients, this video will help you understand how to take a Claude AI website live the correct way.  
  
By the end of this tutorial, you’ll know how to deploy a Claude AI website to a live domain and avoid the common mistakes beginners make when publishing AI-generated websites.

## Transcript

### Intro

**0:00** · You can create some amazing looking websites with Claude AI. In fact, here's a few I created with just one simple prompt. I've created hundreds of these AI websites with Claude AI and they look really good, but there's one big problem. You can ask Claude AI to create a website, it gives you all the code, it looks amazing, great animations, unique design, everything. But then you're thinking, all right, how do I put this on a live domain? How can I manage this for my clients or even create a business email for it like a real website? And that's usually where most tutorials stop.

**0:27** · So in this video, I'm going to show you how to take an AI website by Claude AI and launch it on a real live domain. What's even better is any change or update you make on your AI website will be automatically updated and reflected on your live website instantly without having to touch any files or even using the terminal. And you can do all of this in about 10 minutes. Now, some of you watching this are like, all right, that's cool, Daryl, but what about a database? Well, no problem.

**0:50** · In this video, after we set up your AI websites, for those of you who want to incorporate a database, I'll then walk you through how to incorporate a free database onto your AI websites. A database allows you to store anything entered on your AI websites like emails, phone numbers, or customer information.

**1:07** · It's pretty practical and most websites today need a database. So let's get started. Now, the first thing that we're going to do is head over to Claude AI.

**1:14** · So there is a link to Claude in the video description. Okay, now the first thing that we're going to do is show you how to set this up on PC. Now, in order to make this work, you must download the Claude application on their website. So go to claude.com/download and then download the Claude app for Windows. So here, I'll click on download.

### Download Resources

**1:30** · Okay, now the next thing that we're going to do is we're now going to install Node.js and also Git. This essentially allows us to display projects via local. To give you an example, if I go over here and click on code, you're going to see that I have a live preview of this and I can actually view this on a local host. So we can edit the websites, we can customize it, and we can do all of this via local host. Also, we need Node.js because a lot of these programs that you create, they contain JavaScript and you cannot view JavaScript on a local device without downloading Node.js.

**1:59** · So first, let me walk you through how to download these programs. So here I'll open up my Google tab. This is actually the same AI website and as you can see it is hosted on a domain. Now the first website you're going to go to is nodejs.org.

**2:14** · This essentially allows you to run JavaScript through a browser so you can actually see what you're working with.

**2:19** · So all you got to do is click on get Node.js and install it.

**2:25** · Okay. And I'll install with you guys.

**2:27** · It's really simple. I already have it installed but and then just go ahead and install Node.js.

**2:32** · Okay. So here I'll just go ahead and uh install it.

**2:36** · Okay. And after clicking on next a few times, you'll just go ahead and click on finish and you're done. So it's a really quick install. The next thing that you'll install is Git. Now this essentially allows you to host your projects via local so you can actually work on projects on your own computer without having to use a browser. So right here I'll click on install for Windows. And then here I'll click on click here to download. I'll use the default editor. I'll click on next. Then I'll just let Git decide. So here I'll click on next. I'll go with the recommended options.

**3:06** · I'll use the recommended installation of bundled OpenSSH. Here I'll click on next.

**3:12** · Next I will use the native Windows secure channel and then I'll check out Windows style. Here we go. Next. I will also leave this as default so use MiniTTY. This is the default for terminal.

**3:22** · I'll select the fast forward or merge.

**3:25** · And then we'll use the Git credential manager. Now it's installing this onto your computer and this process might take like a minute. All right and I'm going to uncheck the view release notes and just click on finish.

**3:35** · And that's it. We're done. So let's go back to Claude. Now if you have Claude open I definitely recommend to close it and then reopen it. So since we downloaded those here I'm just going to close Claude. Now the first thing I want to do is create a prompt for Claude code. So here I'll type this in. So here Here go. I want to create a modern real estate website using Next.js. Now, this is critical. Make sure that you instruct any app or website you're building to use Next.js. This is a very optimal framework with very clean code, and most projects use Next.js.

### Prompting

**4:01** · Next, I'm just giving it some basic instructions, but here I'm asking it to create a prompt for Claude code to create this website.

**4:09** · So, I'm not actually creating the website here. I'm just generating the prompt to give to Claude code. So, here I'll run this prompt. All right, cool.

**4:16** · So, now I'm going to take this prompt.

**4:18** · Here, I'm going to copy all this. All right. Going to hold the uh scroll button, right?

**4:24** · I'm going to copy all this.

**4:26** · And then, we're going to go to Claude code. So, over here, I'll click on code.

**4:29** · Now, I'm going to right-click on my desktop, and I'm going to make a new folder. So, here and this will be Daryl's real estate.

**4:37** · This is essentially the name of your project or website where you want everything stored. So, I'll click on select folder.

**4:44** · I'll go to my desktop. And then, I'll select the Daryl's real estate and click on select folder. Essentially, we are just working on this project from local, and everything is stored in this specific folder. Okay, so this was the prompt that we created earlier, and this is going to create my project. So, I'll go ahead now and run this prompt. Next, you may get a pop-up if you want to trust this workspace, and of course, it's your own computer. So, I'll click on trust workspace. And now, it's building my website. Next, it'll ask me if I want to activate Node.js. Now again, this is usually required if you're running projects that have JavaScript, so make sure to allow it.

**5:16** · All right, so after the project has been finished, now I want to view it. Now, there's two ways on how to do this. I can instruct Claude to do it, or I can just use the browser over here and click on preview, but I'll just instruct Claude. Next, I typed in, I want you to have the dev server running so I can see the application while developing it.

**5:32** · Here, I'll run this prompt.

**5:34** · Okay, so now we can view the website as a localhost. So, here I'll click on this link, and here is our beautiful website.

**5:40** · As you can tell, it looks great.

**5:41** · Everything works successfully, and now we can actually work on projects via localhost. Now, let's go ahead and scroll up. Now, let me show you how to preview this from the Claude app. Now, in order to preview this from the Claude app, all you got to do is click on this link right here and click on preview.

**5:56** · Next, I'll click on setup. Now, it's asking us where we want to view the websites. If you want to view it from this section here, you'll just go ahead and select via preview start. If you want to view it from your browser, you just will click on don't do anything. In this case, I'll just select the via preview start. And there we go. Now, we can view our project here on the right side. And of course, you can always like make this bigger if you want to like view it from with a different, you know, browser and stuff like that, but I'm just demonstrating that you can work on your project and use Claude at the same time.

**6:24** · Now, of course, you can make any changes you want to your AI websites, but I think you all know how to do that by now.

### Push to Github

**6:30** · The next thing I want to do is I now want to push this to GitHub. Now, we're going to ask Claude to do this for us.

**6:34** · So, over here, let's type this in.

**6:36** · Next, I'm asking Claude, I want to initiate a Git repository for this project. So, here, I'll run this prompt.

**6:43** · Next, it may ask you how to handle the files. Just click on the recommended setting. Then, we'll select yes, commit everything. Now, it's going to ask us how it wants us to sync up with the GitHub. The first thing we want to do is make sure that we have a GitHub. So, let's go over here and go to github.com.

**6:57** · So, now we need to make a GitHub account, and I think many of you probably already have one, but if you don't, just go ahead and sign up. So, here, I'll click on sign in.

**7:04** · And I'll sign in to my account. So, after you make a GitHub account, we'll just make a new repository. So, here, I'll click on new.

**7:11** · And then this will be the name of your AI websites. So, here, I'll just put in Okay. And then I'll click on create repository. Essentially, what we're doing right here is we're creating a repository so that they can push the files here and store them, so hosting or can fetch them. So, next, let's jump back to Claude. Next, it'll ask you, "How would you like to set your GitHub identity?" Just go ahead and select set it for this repo only. You're just going to give them a name and the email, and they're going to find your GitHub for you. So, here, I'll select set for this repo only.

**7:40** · Next, it'll ask you what name should they use to configure for this repo.

**7:44** · You're just going to enter in other and then you'll select your name and then the email. Make sure this is the same email address that you use with GitHub.

**7:51** · So here, I'll click on next. Okay, so now we're ready to push this onto GitHub. So here, let's type this in.

**7:57** · Next, I typed in link it with the online repo with the following commands and let's go back over here to GitHub. Now, you're going to select the repository, the one that you recently created. So over here, I'll select on repository and this was the one that I created.

**8:11** · Now, we're going to scroll down and you're going to see or push an existing repository from the command line. We're just going to copy this and paste this into Claude.

**8:19** · Next, I'll hold shift enter and then I'm going to paste that command.

**8:24** · Now, we're going to run this prompt.

**8:28** · Next, you want to make sure that you allow these permissions.

**8:31** · Now, it may prompt you to log into GitHub. So here, I'll just click on sign in with browser. Next, you should get a confirmation saying that the authentication has been succeeded.

**8:40** · And as of this point, your project is now synced up with GitHub and we can test this out by going over here to our repository and if you go over and you click on your repository, you should see files inside of your project.

**8:53** · So let's go over here and click on code.

**8:56** · And now you'll see under real estate, we have all of the files listed inside of our project. So now this project is ready to be pushed to a live web host.

### Connect Domain To Ai Website

**9:04** · Okay, so let's say that you have your website finished and you're ready to go.

**9:07** · Now, we're going to go to Hostinger.

**9:08** · Now, the reason why we're using Hostinger is not because it's cheap or I recommend it, it's because they have a Node.js app installer. This allows Hostinger to fetch your AI website and to automatically reflect it on a real life domain. Hostinger can also communicate directly with Claude and self-correct any errors that you come across. You can also add a CDN to your AI websites, flush the cache, add a business email forwards and also add a free database. All right, so let's get started. Now, in the video description, there is a link. This will take you to Hostinger to deploy your AI website using their app installer.

**9:37** · So, in the video description, it'll take you to this page in order to deploy your web app. Once you get here, you'll click on view plans.

**9:46** · And obviously, there's only two different plans, but you can always just select the cheapest one. So, here under the business, I'll click on choose plan.

**9:52** · Next, we're brought to our cart page, and here you can select the period. I definitely recommend a minimum of 12 months. This qualifies you for a free domain and a 30-day money-back guarantee for any reason whatsoever. Now, we also have a coupon code for all of you party people. If you go over here and enter the coupon code Daryl10, you will save an additional 10% off any of the plans at Hostinger. So, here I'll click on apply.

**10:15** · And there it is. We got an additional 10% off our web hosting package. So, once you enter in that coupon code, you'll then click on continue.

**10:23** · Next, you'll register and make an account with Hostinger.

**10:26** · Next, you'll put in your billing address. So, put your first name, your last name, and sign up.

**10:31** · Next, you'll put in your credit card details. So, here I'll fill this out.

**10:35** · All right, once you put in your credit card details, you'll then click on submit payment.

**10:44** · Next, you can enter in your free domain.

**10:46** · So, here you'll type in the name for your new AI websites.

**10:50** · So, I'll put something in like Wilson AI websites, and then here I'll select my free domain, and then click on next.

**10:57** · Next, it'll ask you if you want to deploy your Node.js web app. Here under the import get repository, you'll select connect with GitHub. Now, just make sure that you're logged into GitHub, and Hostinger will automatically sync up with GitHub. So, here I'll select my username, and then we'll select accept new permissions. Then, you might have to wait a minute to let it sync up with GitHub.

**11:17** · Next, it's going to pull all the repositories from our GitHub, and here are my other projects, but the one that I want to use was the one way here at the bottom called real estates. I'll select the real estates, and then click on continue. Now, it wants us to deploy the website. So, here you'll see our framework is preset, Next.js, and all we got to do is just click on deploy.

**11:38** · Now, it's deploying our website from GitHub, and this process might take a few minutes. So, go get a coffee.

**11:43** · All right, and here is our AI website.

**11:45** · So, here at the top, I'll click on view site.

**11:49** · And now you'll see our brand new website on our new domain.

**11:52** · So, that's it. That's how you can sync up a website from Cloud Code using Hostinger. Now, real quick, I just want to show you some other options. So, over here, I'll go to dashboard. Now, what's really cool here is you can add more to your AI websites. So, for example, you'll see that you have an SSL, it's malware protected, and you can even add a CDN. So, here, I'll click on CDN, and then you can enable a CDN onto your AI websites. So, here, I'll click on enable.

**12:18** · Cool. Now, your AI website has a CDN, so it could be delivered faster to people across the net.

**12:23** · Next, let's say that you want to add a business email to your AI websites.

**12:27** · Here, I'll click on setup email, and then I'll just select a free business email, click on get started, and then click on free trial. Then here, I'll just put in a name for my email address. I'll put, you know, daryl@mywebsite.com, and then I'll put in a password. All right, so now our business email has been created. So, here, I'll click on open inbox.

**12:47** · All right, cool. Now, you can send and receive business emails from your new domain. So, here you'll see this is our new domain, and of course, you can go ahead and click on send message and start sending messages as your new domain.

**12:59** · So, next, let's go ahead and test this out. Let's go back over here to Cloud, and I'm going to ask it to change the colors, right? So, change the colors to I don't know, is it yellow? I don't know. Let's just Let's just, you know, just give it a change is what I'm trying to say. Let's just Let's just change it up a little bit here. All right, and now it's changed to yellow. Now, I want to push these changes to the live websites.

**13:19** · So, to do that, here, I'll just put uh looks good.

**13:25** · Commit it and push it's to GitHub.

**13:29** · So, the beauty of this is that you can make as many changes as you want and then push the changes. So, let's say that you made a change and you messed up. Don't worry, it won't pull it right away. It'll only pull it when you instruct it. So, here I'll go ahead and run this prompt. Okay, now going back over here to Hostinger, I'll click on all deployments.

**13:48** · And now you're going to see that it's actually building. So, now it's actually fetching this information from GitHub and it's going to sync it up with our websites. So, it just takes like a few minutes. Oh, cool. It completed while I was talking. Let's go back over here to our websites and let's just view this.

**14:05** · And here is our website and you'll see the changes have been reflected on our live domain. So, that's how you can basically sync up a website with Hostinger, make changes to it and push it to the live websites.

### Connect DataBase (Optional)

**14:17** · All right, congratulations on setting up your AI websites. Now, for those of you who are happy with the way it is, you are free to go. Congrats. Now, for those of you who want to incorporate a free database onto your website, in this part of the video I'll walk you through how to do that. And again, with a database you can store customer information like emails, anything people enter on your website, \[music\] you can store in a database so you can market to them later, you can sell it, you can add it to your email campaigns or whatever. So, let me walk you through how to set this up.

**14:44** · All right, so in this section of the video I'll be showing you how to incorporate a database onto your AI websites. Now, a database allows you to store things like for example, if someone fills out this form, it'll be saved in a database. To give you an example, this is my database right here and you'll see that we have like the name, the email, and the phone number, and then we have the message. So, I'll be showing you how to incorporate this on your AI websites. You guys ready? All right. Now, the first thing that we're going to do is make a free account at supabase.com. Now, I'll put a link to Supabase in the description.

**15:14** · You can sign up for free and have like a free trial. They have like a free server you can use. Now, after you go through the sign up process, I'll go to my dashboard, you'll first see your organizations. And this is basically like a a folder with all your projects. So, here are all my projects. These are essentially all applications and websites. Now, the first thing I want to do when I get here is I want to create a new project. So, right here, new project.

**15:40** · And the project name for this one will be YouTube house, okay? And then I'll just throw in a password.

**15:46** · After that, we'll scroll down. We'll make sure these two options are selected. You don't need to enable this one. And then you'll just click on create new project.

**15:54** · Here, they're just saying this might cost you. No problem. I'll click on I understand.

**15:59** · So, now Supabase is building your database. Now, this process might take a few minutes.

**16:03** · Okay. So, after you see healthy, the server is now established. Now, let's head back to Cloud.

**16:09** · Okay. So, going back to Cloud, I'm over here in my project. Now, this is the current website that I'm going to set this up on. It's a brand new website. Uh I just finished making it, but I haven't connected it with the database yet. So, the first thing I want to do is go over here to Cloud and then click on settings. Now, just make sure you're using the Cloud desktop version, okay?

**16:28** · We'll go over to connectors and then click on customize. Now, here under connectors, I'll click on add connector and click on browse connectors.

**16:37** · And we're going to type in Supabase.

**16:39** · Here we go. Supabase. There it is. So, I'll go ahead and click on this plus icon.

**16:45** · And then it'll automatically prompt me to the Supabase website. All I got to do is just make sure I authorize API access. So, here, this is my organization and then I'll click on authorize Cloud.

**16:56** · All right. So, we're connected and it looks like it's going to redirect me back to the application. All right. Now, once we get here, under the connector section, click on Supabase. You always want to make sure for the tool permissions that always allow is selected. So, make sure this is selected. And scrolling down, same thing for write delete tools, make sure this is always allow, okay? If you don't have that on, it's going to constantly ask you for all these things. It takes a lot of time. It gets really annoying. So, just make sure that you have that selected. Now, let's go back to our project. All right.

**17:25** · Now, the first thing that we're going to do is enter in a command. Now, we're going to enter in a command from Superbase. So, going back over here, let's click on the connect button. Now, here we have a few options: framework, direct, ORM, and MCP. Now, we're going to select the MCP.

**17:41** · Make sure the client is Claude code.

**17:43** · Now, scrolling down, you're going to see connect your app. Now, we've already done step one, and we've already done step two. We did it that way just because there's less errors. Maybe you guys might get something different on your screen. So, we did it that way just to make sure that, you know, there's as less errors as possible. Now, here we're going to install the agents. So, I'll click on copy, and then let's go back to Claude.

**18:04** · And then we'll type in these commands.

**18:06** · I want you to run the following command, colon, and then I'll just paste in that prompt from Superbase. And then I'll run this prompt.

**18:13** · All right. So, now that it's trained with the AI, now we're going to ask it to integrate a database onto this specific application. So, let's type in this prompt here.

**18:21** · Okay. So, this prompt is a little bit longer. This is about half of it. Now, I want to implement Superbase into this application to make the Next.js dynamic.

**18:29** · Now, we're saying this because we're essentially saying I want to make the database dynamic, meaning it can automatically adjust to your website depending on what you build. I don't want authentication for now. Allow every user to access our application and submit forms. Make sure you install the following libraries. Now, we're going to go back over here to Superbase, and we're going to go over here and click on framework. Now, I wanted to install this specific library. So, I'm going to copy this, go back to Claude.

**18:55** · Okay. Hit space, and then I'll paste that in. But, we're not done yet. All right. I'm going to hold shift and enter, and there's one more line we're going to have to enter. And the last line is And these are the environmental variables that you need to connect locally to the database so we can test for functionality. Make sure you add these variables to the ENV file. Now, we're going to get this from Supabase as well. So, going back to Supabase under the framework section under add files, we're going to copy these.

**19:21** · And then we're going to go back to Claude. We're going to hold shift, enter, and then paste it in. Now, I know this is a long prompt, but when you're building your database, it needs to build it in the correct structure. And if you don't do this, it's going to build it in an incorrect structure, and it's going to be wild. You're going to have a lot of errors. It's not going to fetch well with Hostinger. So, make sure you use this same exact prompt. I'll also put this in the video description for all of you. I'm going to spell the There we go. I spelled it a little bit wrong. All right.

**19:47** · So, now that you entered in all this information, make sure that you guys do enter this verbatim, except obviously for this because you're going to have different keys. Uh I'll go ahead now and run this prompt. Now, it's currently building a database. So, this process might take like 5 minutes. All right. And after about uh 10 minutes or so, uh they finally integrated it. Now, it looks like my application experienced some sort of errors. And again, this has nothing to do with your application, uh but if you do get errors, it's just because the application is correcting itself and fixing itself. Now, this actually works.

**20:18** · So, if I go over here to my Supabase accounts, I'll go over here and go to table editor.

**20:25** · Uh you can actually run some test leads.

**20:28** · So, here I'll click on leads, and you can see right away that uh Claude is now connected. So, these are just uh demos from Claude. So, you can ask them to run a demo, and here there is two. So, we know that it's connected and working.

**20:40** · But, we're not done yet. Don't get too comfortable. All right, I know everyone just wants to quit the video. There's a lot more to do. So, we're going to go back over here to Claude, and we want to commit these changes and push it to GitHub. Commit the changes and push it to GitHub in the main branch. So, here I'll run this. Now, the reason why I'm putting main branch is because that's where my project is currently located.

**20:59** · So, I just want to make sure that it's exactly where it's supposed to be.

**21:02** · Now, if I go back over here to my Hostinger app, you're going to see it's building. Now, it's building it because we're pushing it to the actual application. So, uh yeah, just letting you know that uh it is connected and it is working. So, let's go back to Claude. So, now we want to push this to environmental production cuz right now we're working in localhost, but if we use this on our own live websites, it's not really working at the current time. So, what we want to do is push this into environmental production. So, let's go ahead and run this prompt. So, you're going to type this exactly. Adjust the gitignore to allow environmental production.

**21:33** · Add environment to production with the two variables. Commit and push, but don't press anything yet cuz we need to get the actual variables. So, we're going to go over here to the Superbase under our project.

**21:49** · We're going to go over here to connect and then we're going to take these two files right here. So, I'm going to copy this, go back to the application, and then we're going to hold shift, press enter, and then we're going to paste those in there just like that. And then we'll hit send. Now, this is probably the last step that we're going to do. Essentially why we're doing this is we want to make sure Hostinger can communicate with Claude. So, we're just giving them those keys.

**22:11** · Okay, and that's pretty much it. So, now let's test this out. Let's go back over here to Hostinger really quick.

**22:17** · And you're going to see that it's building. I'll click on all deployments, and you're going to see that this one was completed successfully and now it's currently building the next one. Okay, so now let's test this out. I'm going to open up this window here.

**22:31** · And then we're going to fill out this contact form. All right, so this is a live website. I'm going to scroll down and I'm going to put Daryl, daryl@able.com.

**22:40** · I'm a buyer. What is my budget here?

**22:43** · I'll just put a million dollars, whatever. And then I'll put howdy, and then I'll click on request access.

**22:50** · Okay? Now, if this did not work, if something happened to your contact form, you may need to debug it. It has nothing to do with the database, it's just probably your project. Going back over here, uh let's go ahead now and test this out.

**23:02** · Now, there is a few debugging methods in case this did not work properly for you guys. So, here we have our leads and there it is. You can see Darrell at darrellawol.com. So, you can see that it's fully integrated with the websites.

**23:14** · Now, there is one debugging method I want to show you and just in case something did not work out. I realize uh this video is kind of hard to make for everyone cuz you may have different results than me, but this is the correct way in how to do it. But, here I'll go ahead and give you a prompt to run. Now, sometimes this may or may not have been entered in the right repository. So, what you can do here is you can say, "I want this to be merged directly to the main branch." That'll essentially force the actual AI to put this information in the main branch instead of like a side repository. So, I'll just go ahead and run this prompt and just see what happens here.

**23:47** · Okay. So, it looks like mine was already there, so nothing more for me to do.

**23:50** · But, sometimes it may push to the wrong uh branch. Now, let's go back over here to GitHub. So, next thing I'll do is go over here to GitHub and under repositories, under YouTube house, if I click on environmental production, you should see something that looks just like this. If it does not look like this, then something went wrong. So, you should see this and what this does here is that this reroutes everything from Hostinger to Supabase. So, Hostinger is basically the middle person.

**24:19** · Now, if you did get an error for whatever reason, if you click on all deployments, it'll say failed. And if you click on the arrow right here, it'll explain why it failed.

**24:30** · And this has happened to me in the past and all you're going to do is just copy the entire thing right here and then give it to actual Claude and say, "Hey, I got this error, you know, you paste it in here saying I got this error from Hostinger. What is the problem? How can I connect it?" And they should be able to debug it with Hostinger. Hostinger acts as the middle person to make sure that your database and Claude are working in sync together. Well, party people, you made it to the end. Thanks for watching. You know, this video actually took me a while to make.

### Outro

**24:54** · Uh at first we were doing this through terminal and to be honest, it didn't make a lot of sense cuz when you're building this through terminal, your project or whatever, you can't really visually see what you're doing too well.

**25:05** · So, I thought to myself, "You know, man, this is not going to work. We got to find an easier way and how to do this."

**25:11** · So, me and my two developers, we dig through the trenches and this is what we pulled out. So, I hope you guys really enjoy this video. You have any questions for me about Cloud or Hostinger or WordPress or whatever, let me know in the comments below and I'll do my best to get to all of your comments. My name is Gerald Wilson and then I will see all of you party people in the next video.

**25:27** · Take care.
---
source_title: "Figma Design System 2025 - Colour Tokens [ Ep 1] | Figma Variables Colors"
source_url: "https://www.youtube.com/watch?v=m7kUGmNkPoc"
created: 2026-05-07
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=m7kUGmNkPoc)

## Transcript

### Welcome to the series

**0:00** · What's up everyone and welcome to episode one of our new basic design system series where we're going to be building a design system together using variables and styles and all the best that Figma has to offer. As usual, there is a link in the description for a file if you want to follow along. Let's jump in. First thing I need in any design system is color. Now, I would recommend starting with just color primitives.

### Choosing Our Rainbow

**0:20** · We're going to create kind of rainbow colors and give them lots of shades about like 10 shades each. So then we can pick and choose from them for our different usages. Now, when you're creating your rainbow, one thing to keep in mind is that you want the colors to match in their saturation levels and their brightness levels. So, I've dropped in the different HSB information for each of these colors. Now, HSB stands for hue, saturation, brightness.

**0:42** · And you'll notice that this the brightness for all of these is really high. 100, 100, 100, 83, 94, 95, 93. And you can really tell if one of them, let's say I'll choose this green and I'll bump down the brightness. You see, even just by by 20, it it doesn't belong in this palette anymore, right? And the same thing will happen with the saturation. So, they're all pretty high on saturation. I would say they're above the 40s. They could be a bit more similar, but like this one's on 100 saturation. This one is on 47, which I think is the lowest.

**1:13** · But if I took, let's say, this one, which is on 64, let's say I lowered it down by a lot, so the saturation would be like in the 20s.

**1:22** · You see it doesn't work. Okay. So, we want to have similar saturation, similar brightness across the board when our ch when we are choosing our baseline rainbow set. Once we have that, we're going to be creating 10 shades for each of them where this color will be the middle. So, this one will be the 50 or the 500, however you want to name them.

### Creating Shades

**1:41** · And then we're going to have a few to the right and a few to the left. So, a few brighter, a few darker. Now, these are a few plugins that I like to use.

**1:48** · Some of them will put it on the canvas in like a nice graphic way. Some of them will just give you the colors. So, let me show you like let's say color scale generator. So, if I select my red color and then I'll go into plugins and select color scale generator then it asks me how many steps do I want. I'm going to want 10. So, I'll just create that and that's it. It just drops it in. But if I use let's say in the file you will find these nice things ready for you to go to put all of your colors in. So, what I'll do now is I'll select every one of these rectangles for the light mode ones.

**2:18** · The squares on the bottom are going to be for dark mode, which we'll do in a sec.

**2:24** · But I'll just click on them, then click on I to get my color picker, and then just pick the colors plug-in generated for me. I'm going to go ahead and do that for all of my colors. So, these are the shade scales for all of my colors.

### Branded Greyscale

**2:36** · And I've left grayscale, so we can do that one together. So, with grayscale, what I like to do, I like to set my grayscale to my brand color. So, for example, if this was using just a normal gray, let's say D999, which is kind of the default gray. If I click on it over here, you'll see that the hue is zero and the saturation is zero. And you can create a really nice grayscale scale from here, but I like to inject a bit of brand into it. Now, I know that my brand color is going to be this one or like any shade of purple really.

**3:07** · So, my hue is 261 for this one. So, I'll select my gray and then in my hue, just write 261.

**3:16** · Now, you have to have at least one saturation for this hue to keep. Cuz if I I wrote 261, I'll click okay and leave this. When I click back in, it's going to be on zero again. Yeah. So, 261. And then in saturation, I'll add just one for example. Now, when I come back, it's still there. Yeah. Now, I'm going to want more than just one. Maybe like five. And then I want a higher brightness, right? so it matches the rest of my elements. Let's put it at like 77. Lovely.

**3:44** · This is going to be my grayscale 500 that from that I'm going to create my grayscale. Gone ahead and created my grayscale palette just like I did the other ones. Now I need to now create dark mode versions for all of these colors. Now you might think that this is a bit of a cheating way, but I found that this works and this is a basic design system, so why not use a basic method? So, what we're going to do is just swap the shade scale. So, for dark mode 100, I'm going to ey drop dark light mode 10.

### Dark Mode Colours

**4:14** · For dark mode 90, I'm going to ey drop light mode 20. And just keep going with that. And you'll see that you kind of get a nice thing going where it does kind of complement each other. And you can see a world where let's say I've used this for some sort of text and then when I swap it it should probably be this or I've used this as a background. So when I swap it should probably be this. So this this pretty much works. Yeah. 95% of the times this works.

**4:42** · And you'll also notice that in the center of it, the difference between them is much smaller, which is great, right? Because if 50 is my brand color, when I swap it to dark mode, I don't want it to disappear completely.

**4:55** · But I do want it to lose a bit of its brightness, which is what's happening here because 50 is taking 60. Yeah, hope that makes sense. So, I'm going to go ahead and do that for all of them. Boom.

**5:06** · Now, I have all of my colors ready to go. This is the point where we're going to create some variables. I would recommend using a plugin in order to do this because there are so many colors. I have yet to find a plugin where I can plug in the different modes correctly.

### Variable Time

**5:21** · So, what I'm going to do is only create variables for the light modes and then the dark modes will just have to follow later. So, you'll notice in the file that I've named the colors in a certain way. So, you'll see that let's say over here they're called blue/10, blue/20, blue/30. And that's what we want in order for it to create it in like a group in our collections. So, I'll select just the light mode ones. You can hold down command and shift while dragging your mouse in order to select just the ones you want. And then, and then I'm going to use a plugin to convert these to variables.

**5:52** · So, going to plugins and widgets and then color variables creator. Just one that I found. There's loads out there, so whichever one works for you. It's going to ask me what the collection name is and I'm going to call it color primitives and create. Done. It's created them. So, if I click on my canvas, click on the variables here. Boom. We have all of our colors.

**6:16** · Now, all we need to do is actually go in and just recreate the dark modes cuz I have yet to find a plug-in that does this, but it's pretty quick. It's a lot of just copying and pasting. So, in the value of this mode, I will call it light. And then I will add another mode using this button and call it dark. And then all I need to do is just kind of flip them around. So copy this into here. So I've finished setting up all of my light mode and dark mode colors. Just copying over doing that kind of crisscross thing.

**6:44** · Now I do in grayscale want to set up a few more colors. So I'll click on the grayscale group over here. And I'll add another color variable. And I'll call this one zero. So I want ones at the edges. So zero is going to be full white in light mode and in dark mode it's going to be full black. And then going to do the opposite. So I'm going to create a new one and I'll just call it 999. In light mode it's going to be full black. So 00 0. And in light mode it's going to be full white. And then I also want a static white and a static black.

### Edge Colours

### Static Colours

**7:16** · So I'm going to create a new variable and call it white. And that's white that even if you swap it stays white. And I want another black one like this. So color one black, black in light mode and black in dark mode as well. These are really important both of these because sometimes you just need full white or full black and it needs to never change or anything like that. So make sure to make these in your design system. So we now have our primitives. Now we'll move on to create usage variables or tokens or however you want to call them.

**7:48** · But the primitives are ones that we're not actually going to be using in our design. We're not even going to have them available to us. So, we're going to scope them out, but the usage ones are the ones that we'll actually use for different elements like the backgrounds, the text, the images, the borders, all of that. So, let's firstly scope these primitives out.

### Scoping Primitives Variables

**8:06** · So, if I go into all variables, select my first variable, and then scroll down to the bottom, hold down shift while I do that to just select all of them, then rightclick and edit variables, I get this kind of I get the details here, but then there's the scoping menu where I can select where am I actually going to see these colors cuz right now, if I'm trying to fill a frame or text or stroke or an effect, I will always see them. I never want to see them. These should never be accessible to me. These are only for the backend use. Okay. So, I'm just going to untick this.

**8:36** · So, so show showing no supported properties basically. And you can see if I drop in like a rectangle and I try and fill it and I go into here, there's no colors available to use. So, now let's create another collection and start creating variables for usage. So, in your Figma file, you will find this kind of template for you to use for what I think is necessary in a really basic design system. So, if I open up my variables and then I'll create a new collection over here. And I like to call it color usage, but you can call it whatever you want.

### Background Design Tokens

**9:06** · So I'll click to add a color variable. And we're going to create background variables first. So I'll write background and then slash because we're creating a group. Then neutral because those are the first few that I'll create. And then another slash and then the first one I'm going to be creating is primary. So primary. So this is just kind of setting up all my groups. So now you'll see in all variables I have background variables inside of them. Neutral background variables. and then primary, which is my first one.

**9:33** · What I like to do is I like to create all of my variables, apply them, and then set what the values actually are. It's a bit weird, but it makes it easier for me to see what I'm doing. So, let's create another one. So, shift and enter to just create another one that's the same. Secondary, shift, and enter. So, now I've created my first three. Now, I need another group, which is neutral inverse. So, the way to do that, really easy. I'll just right click on my group and duplicate it and call it neutral inverse. And then I need another one for brand.

**10:06** · So just duplicate that and call it brand. Um and then let's leave semantics till later. And in neutral I actually also need a disabled one. So in here I'll create disabled. Great. Now let's apply these.

### Assign Variables

**10:22** · It's all going to look the same but it's it's all part of the process so trust it. I'll just close that. So for this one, I'll select this square and then instead of filling it with just a color, I'll select background neutral primary.

**10:37** · This one is background neutral secondary. So I've applied all of them and now I can go in and choose actual colors, right? And then it just makes it a little easier for me to see it in action. So, my neutral primary background color. If I go into click kind of to select a color and then go into libraries, I'm going to want something from my neutrals, I believe.

### Selecting Background Colours

**11:00** · Um, so let's see. Is 10 good for me?

**11:03** · That might be a bit too dark. I might actually, this is a case where I might actually go with a zero. Yeah, there we go. I think a neutral primary background is going to be just white. Then the secondary that sits on top this time, maybe I'll actually go with a 10 or a 20. I think 10 is enough. Then for tertiary, I'm going to go let's write gray to get this quicker. Maybe a 30.

**11:27** · Maybe a 20. Is that enough difference?

**11:30** · Yeah, it's enough difference. Then for my disabled color, so I might go for a 30 in this case. Yeah, that kind of works. So my invers I'm just going to inverse. Yeah, going to go for 100 with my fully inversed. Then my secondary, maybe a 90. Yeah, let's go with 90. And then for my tertiary, I'll go with my 80 probably delightful. Then for brand, so my primary brand color should be my primary brand color, I think.

**11:58** · So I'll go with purple 50, which is kind of the main event. And then from there, I'm going to go lighter in the shades. So for this one, I might go for purple 30. And then for my tertiary, I'll go for a really light one, something that's really subtle. So maybe a 10 even. Yeah. Great.

**12:19** · So we have our first set. Whoop. And because of how we set them, that the dark mode is in the primitives. Let me show you what happens when I swap this over. So I'm selecting this frame. And then in my appearance section, I've got apply variable mode. And instead of color primitives light, I'm going to change it to dark. Look at that.

### Testing Dark Mode

**12:38** · Everything just swapped. And I think it looks great. So let's see that the background also changes just to help us with that. that. So, I think my background isn't connected to anything.

**12:46** · Let me just change that to black. Look at that. Okay, so it looks so good on dark mode. Obviously, the primary neutral is disappearing because it's black on black, but it looks great.

**12:55** · Okay, so the method works. Let's move on to the semantic colors. Now, in the semantic ones, I'm going to want a subtle and a bold for each, which is just going to be like probably a tens, the tens for the subtles and maybe like the 80s for the bolds. So let's go into my variable collection into color usage.

### Semantic Design Tokens

**13:14** · Now for this I'm going to need a new group completely. So what I'm going to do is go into all variables create variable color and then I'm going to call it semantic then success and then subtle cuz that's my first one. So now I have my semantic group and success underneath. But you see it's not in background where it should be. So I can just kind of drag it in there and just bring it down. Yeah.

**13:43** · So now it's still inside of background, but it's a group that has a secondary group inside of it. So we'll do the same thing we did before. So subtle, and then shift and space to create bold. And then I just duplicate this group. So I've got success, I've got warning, I've got error, and I've got info.

**14:02** · And if you need more semantics or different semantics, I've seen before where people put here like promotional or um different like loyalty schemes or whatever. So, use whatever you need to use. Let's assign them. Now, let's go back into our variables and set these up. So for success, I think we should probably use the the 10 or the 20, maybe the 10 for the color that is indicating that.

### Selecting Semantic Colours

**14:34** · So success is green. So I'm going to use that. Then for bold, I don't want to go too dark, but I kind of want to go maybe like the 60s or the 70s. Let's put a 70 in. Yeah, that feels nice. So for warning, let's do the same thing. I need the 10 and the 70. And it's good to kind of stay within the same shades. Similar to how we talked about at the start, we want that consistency with our brightness, with our saturation, with all of that.

**15:04** · We don't want to see like if I went for a really dark red, if it was next to a warning, and that it just it just is too much.

**15:11** · Yeah. So, I want to keep it in the same level. If we're using 70, let's try and use 70 for all of them. So, this one is 10. And that is 70. Lovely. So, the last thing to do after we've created our background colors is now we want to scope them as well. So, I'll go into my background and select from the top to the bottom. Right click, edit variables.

### Scoping Semantic Variables

**15:32** · And I want to scope these so they just show up in fill, but probably just for frame and for shape. I don't want them in stroke. I don't want them in effect and not for text either. So, just for filling anything. You can make this just for a frame and not a shape if you want, but for this case, I'm going to leave them on both.

**15:51** · And we now have background colors. Whoop whoop. Let's move on to create some text colors. Now let's create our variables for our texts. So I'll go into all variables, create a new color, and this one's going to be text slash neutral slash primary. And I've created the kind of second level of my groups. So do the same as we did before.

### Text Design Tokens

**16:14** · And now that I've set up all my new variables, I'm now going to, like I did before, assign them on my texts just so they can really help me out when I'm doing it and I can see them as I go along. Now, let's decide what we want.

### Selecting Text Colours

**16:38** · Let's decide what we want our colors to be. So, I'll go into my variables text neutral. Let's start off. So, the primary text probably going to be the darkest one we have over here. So, probably 100. I don't want to go to 99 because I don't want it to be full black. But 100 looks good. Then secondary, let's drop down to maybe 80.

**16:59** · Let's see them here as well. So, grayscale, maybe 80. Yeah, that's nice.

**17:04** · I like that it has a bit of a a bit of color in it. And then the tertiary I can drop down even more. So, let's go maybe to a 70. Is that enough? Yeah, that looks good. And then for disabled, I can drop down way lower. So, maybe even like a 40. All right, let's keep going with our inversed colors. So, kind of similar to how we had it here, right? If this is 100, I'm probably going to want my neutral inverse to be zero, maybe 10, actually. Sorry, not zero, because we know that zero is a full-on kind of like white.

**17:34** · Secondary, and maybe let's make it like a 20. And then my tertiary, let's make it a 30. Yeah. Now, let's move on to our brand. So, for my primary brand color, so we should probably use our brand color, right, which is 50. I would also allow us to dip into 60 if 50 feels too bright, but in this case, I think it works. Then our inverse ones, I would just use the 10 really because it needs to be light enough that it's still readable on top of our background colors.

**18:04** · So, I'll just keep doing 50s and tens for all of them. Okay. So, this is already too light for me. So, I think instead of that, maybe I'll go with a 70. Yeah. So, for green, I definitely need the 70.

**18:19** · Let's see. For this one, what do I need for warning is 70. Yeah. Okay. So, you see, for some of them, it's just too light. And that's fine. So, orange 10 red. I'm definitely going to be needing the 70 for red. Yeah, for sure. And then my inverse one is going to be the 10.

**18:40** · For blue, probably also 70. Let's just double check that our actual brand color is accessible for AA or for AAA. We can do that using Figma's new kind of accessibility tool. I do need to detach it in order to check it, but that's okay. So, I can see that it's not AAA, but let's see if it is double A. It is double A. Okay. So, I'm fine with that.

### Figma Contrast Checker

**19:04** · I know that AAA is is the best to have, but in order to maintain my brand color, I am happy for it to be just double A.

**19:10** · So, that's okay. Now, last thing we need to do is we need to scope out our colors so they only show up when we're selecting text. So, go into variables, text, and then select all of them.

### Scoping Text Variables

**19:22** · Right click, edit variables, and then let's just scope them so they are just for text. Now, this is where we also will need to create icon variables because our icons will sometimes be a border. They'll sometimes be a fill color. If you're using SF symbols, they will also sometimes be text. I would recommend to create a whole group just for icons. Now, they are going to be exactly the same as these ones. So, all we need to do is duplicate.

### Icon Design Tokens

**19:47** · So, I've dropped in the icon template because I've just used a an icon inside of it instead of the text so you can see it all applied and you don't need to watch me do that cuz you already know how to do it. Last set of color variables we're going to create are the border variables. And I think these are super crucial. So, make sure not to miss them out. For borders, we're going to be following a similar pattern to the one we did for text and icon, but it's going to be a bit less full cuz we don't need that many options.

### Border Design Tokens

**20:14** · So, we're going to have, as you can see here in the template, a primary and a secondary, neutral, and neutral inverse. Then, we're going to have a primary and inverse for the brand and all of the semantics. So, similar to text. So, let's set up these variables, assign them. You know the drill. So, I'll go into here, select all variables, new color variable, and I'll call it border neutral primary. My first one, shift, and enter to create a new one. Then I'm going to duplicate this group to create neutral inverse.

**20:45** · And then I need a brand one. So I'll just duplicate this one.

**20:50** · Brand. And then brand will have primary and inverse inside of it. Then duplicate this one. Now you know the drill. I'm just going to assign these quickly.

**21:14** · They're all applied. Now we just need to select what they are going to be. So for our first borders, I'm probably going to go with something like on the light gray side. Maybe the 30. Yeah, that's cute.

### Selecting Border Colours

**21:26** · And then secondary, maybe a bit darker than that. Maybe the 50. And then for the inverse ones, just the complete opposite. So I'm probably going to go with the 90 maybe. And then for the secondary one, maybe the 70. Then for the brands and the semantics, I would recommend going with like a darker shade of the brand color and all of them. So maybe like the 80 even. I wouldn't go as far as 90 because that would be too much. For the inverse, maybe I'll use the 20s. So let's see. Purple 20 cuz want it to be too light.

**21:58** · Yeah, that's perfect. So 80s and 20s is what we're going with.

**22:07** · And you can see why I like doing it while it's already on the page because it really helps you to see it come to life and you can see straight away if you're making any mistakes or something just doesn't make any sense. So this needs to be 20 orange. Great. Now the reds. Amazing. Last thing we need to do is scope these. So I'll select all of my border colors, right click, edit variables, and just for stroke. I've got all of my colors. Let me put a section around it to tie it up in a neat little bow.

### Scoping Border Colours

### Final Colours!

**22:38** · And I'll call this all my color usage. Ta. Yeah. So, we've got all of our colors now. And these should be all the colors you really need for our basic design system. And that's that. I hope you were able to follow along. In the next episodes of this series, we're going to be creating some sizing tokens for our radius and for spacing and padding, stuff like that. Then, we're going to create typography variables.

**23:02** · And then we'll start creating some components like buttons and dropdowns and all of that. I hope you enjoyed.

**23:07** · Please like and subscribe. Let me know what other videos you'd like to see. See you at the next one.
---
source_title: "Going Unitless in Figma"
source_url: "https://www.designsystemscollective.com/going-unitless-in-figma-a-workaround-f1bc1cee399d"
created: 2026-07-07
tags:
  - "clippings"
---
If you’re reading this, then you’re probably just as frustrated with Figma as I’ve been when it comes to using unitless values (or %) for typography variables.

You know you want `line-height: 1.5` and ordinarily, you’d use `150%` on the design side, but when variables came out in 2023, we could only use fixed units (see pixels) for all number variables.

For most of us, it felt almost like Figma wanted to upend [decades of industry best practices](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height) and return to the dark ages. And look, I’m not going to preach the merits of unitless line-heights when [others have already articulated why much better than I ever could](https://css-tricks.com/almanac/properties/l/line-height/).

So, here are the choices we’re left with when we need to have `line-height: 150%` in our **Text Styles**, but can’t encapsulate it in a **Variable**.

1. Leave it out entirely and hope your developers remember to ask which token should go there
2. Use the fixed pixel value and pray they don’t implement it exactly like that
3. Add a dev annotation. Every. Single. Time.

Yes, all three options are terrible. And [many of you agree](https://forum.figma.com/ask-the-community-7/so-about-font-variables-20736) and [have been up in arms for a while](https://forum.figma.com/t/allow-text-line-height-to-be-defined-by-multiples/12179)!

We’ve been waiting with bated breath since 2023, and every Config since then has been a disappointment. Schema? Marginally less so.

Meanwhile, [Webflow handles this correctly](https://help.webflow.com/hc/en-us/articles/33961268146323-Variables). But I digress.

## The Workaround

Alright, here’s what I figured out: [Figma’s Code Syntax feature](https://help.figma.com/hc/en-us/articles/15145852043927-Create-and-manage-variables-and-collections) lets us show one thing to designers and another thing to developers. We can store the calculated pixel values that Figma needs while displaying the semantic token names that developers need.

It’s not elegant. It’s a bit of a pain to set up. But it works, and more importantly, it gets your developers the tokens they need without bugging you incessantly through Slack. Or, heaven forbid, a snide comment on Jira.

**The core concept:** you calculate all the permutations of your font-sizes and line-heights, store them as pixel-based variables, then override what developers see using the `Code Syntax` field. [This approach mirrors similar workarounds for other CSS units](https://medium.com/design-bootcamp/optimal-line-length-for-body-text-a-figma-guide-3e44f4fdaee1), like storing pixels but displaying `ch` units for developers.

### The Gap We’re Bridging

This is where we usually get stuck — 150% line-height with no way to attach a variable.

![A screenshot of the CSS code panel in Figma with line-height: 150% in a text style.](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*jAjxuZjpUsKuswBrkzEpyg.png)

We’re going to go from this…😭

This is what we want developers to see in `Dev Mode` — the primitive/token they should use.

![A screenshot of the CSS code panel in Figma with line-height token as required by developers.](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*vc0z2YOgDs6z9eshLaIboA.png)

…To this! 🎉

Shame on you, Figma, for making us do this.

## Step-by-Step Setup

### 1\. Calculate your Line-Height Values

First, figure out which combinations you actually need. If you have font sizes of 16px, 24px, and 32px, and line-heights of 1.25 and 1.5, you’ll need six variables:

<iframe src="https://cdn.embedly.com/widgets/media.html?src=https%3A%2F%2Fdatawrapper.dwcdn.net%2Ftoces%2F2%2F&amp;display_name=Datawrapper&amp;url=https%3A%2F%2Fdatawrapper.dwcdn.net%2Ftoces%2F2%2F&amp;image=https%3A%2F%2Fdatawrapper.dwcdn.net%2Ftoces%2Fplain-s.png%3Fv%3D2&amp;type=text%2Fhtml&amp;schema=dwcdn" allowfullscreen="" frameborder="0" height="191" width="680" title="Going Unitless"></iframe>

You can calculate all permutations upfront, or be selective based on what your typography system actually uses. I’d recommend starting with just the combinations you know you need — you can always add more later.

> **Pro tip:** Figma can do math in any numerical field. If you’re populating variables and can’t remember what 32px × 1.25 equals, just type `32*1.25` in the field and Figma calculates it for you. Small mercy.

### 2\. Create Variables for Each Calculated Value

Set up your number variables with the pixel values you calculated. Your naming structure might look like `Line-height/{level or token}/{font-size}`, but organize them however makes sense for your system.

![Screenshot of Variables window showing how to organize the line-height variables.](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*LWlRzPNKxQ19vm6l-CcEYg.png)

Note: I tried using modes for this — defining each line-height level (Tight, Normal, Loose) as a mode with the font-size variations inside. Tempting, but there’s a problem: the Code Syntax field doesn’t change with modes. I know. I know.

> **Another pro tip**: Setting up repetitive variables gets tedious fast. Create the first one perfectly — right scope, description, everything configured. Then duplicate that variable repeatedly. The only thing you need to change is the value itself. Your **scope** and **Code Syntax** settings will carry over. Measure twice, cut once, as they say.

### 3\. Set the Code Syntax field

This is where the magic happens. For each variable:

1. Edit the variable and navigate to the `Details` tab
2. Find the `Code Syntax` section
3. Add your platform (Web, iOS, Android — I usually use `Web`)
4. Enter what developers should actually see: `var(--lh-normal)` or whatever your token name is

![](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*1Y5Kgo6_spewvI1cJjzv-A.png)

![](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*Ipl-WWi78WyqkJE-k-afeQ.png)

The preview shows you exactly how it’ll appear in Dev Mode — that’s what your developers will reference when implementing.

### 4\. Use Them in Your Text Styles

Now, when you apply these variables to your text styles, designers see the pixel value (which works in Figma’s interface), but when developers inspect in `Dev Mode`, they see the primitive/token and the percentage value as a comment.

![Looping animation of selecting 3 different text layers to show various line-height tokens visible in Dev. Mode.](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*XNa_8EX5kEKjsWYMUn7I3g.gif)

Looping animation of selecting 3 different text layers to show various line-height tokens visible in Dev. Mode.

It’s a bit of a mental chore — you need to remember that `Line-height/Normal/200` actually means ***“1.5 line-height for 200-level type.”*** But your developers get clean tokens they can implement directly.

## Get Andii Hei’s stories in your inbox

Join Medium for free to get updates from this writer.

And honestly? That’s what matters here. The handoff.

## Scaling This Up

If you’re looking at dozens of line-height variables and dreading this laborious hack, use the [Syntax Manager plugin](https://www.figma.com/community/plugin/1497527267396324679). It lets you update **Code Syntax** in *bulk* across multiple groups.

## Bonus: Letter-Spacing

Letter-spacing has the same problem, but it’s slightly worse. Figma doesn’t even show the percentage value as a comment in `Dev Mode` the way it does for line-height.

![The CSS Code panel showing the workaround being applied to letter-spacing.](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*yQhD1UivUOVrrWu7uActXw.png)

The CSS Code panel showing the workaround being applied to letter-spacing.

For letter-spacing variables, add the converted value in the `Description` field. It’s a fallback, but at least developers can reference it if the token doesn’t already exist in their codebase.

## A Few Things to Keep in Mind

**Scope your variables carefully**. If you leave line-height variables unscoped, they’ll show up in dropdowns where you don’t want them (spacing, effects, whatever). Scope them to text properties *only*.

**Document your system**. Whether that’s a dedicated Confluence page, a README in your design file, or a section in your component documentation — make sure future maintainers understand why your line-height variables are structured this way. Future you will thank present you.

**Test the** `**Dev Mode**` **view**. Before you roll this out to your whole team, open `Dev Mode` and inspect a text style. Make sure the `Code Syntax` displays the way you expect. Better to catch formatting issues now rather than after, when developers start asking questions.

## Closing Thoughts

Look, I know I’ve been throwing a bit of shade at Figma, but I still like them. No, really, I’m a co-owner for crying out loud (3 shares worth)! So, it pains me to have to write a workaround for a [problem that’s been around since 2021](https://forum.figma.com/suggest-a-feature-11/allow-percentages-for-line-height-21970).

And if you’ve found a better approach, I genuinely want to know about it. This is one of those problems where I’d love to be wrong, where someone points out a simpler solution I’ve completely missed.

So there you have it. It’s not exactly the Promethean fire that some of you were hoping for, but at least it’s a hack that works.

### Additional Resources

- [MDN Web Docs: line-height](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height) — CSS specification and best practices
- [CSS-Tricks: line-height](https://css-tricks.com/almanac/properties/l/line-height/) — Guide to unitless line-heights
- [Eric Meyer: Unitless line-heights (2006)](http://meyerweb.com/eric/thoughts/2006/02/08/unitless-line-heights/) — Foundational article on inheritance issues
- [Figma Community: Allow percentages for line height](https://forum.figma.com/suggest-a-feature-11/allow-percentages-for-line-height-21970) — Ongoing discussion since 2021
- [Figma Community: Allow text line height to be defined by multiples](https://forum.figma.com/t/allow-text-line-height-to-be-defined-by-multiples/12179) — Original 2021 feature request
- [Figma Variables documentation](https://help.figma.com/hc/en-us/articles/15145852043927-Create-and-manage-variables-and-collections) — Official Code Syntax documentation
- [Tokens Studio: Line Height documentation](https://docs.tokens.studio/manage-tokens/token-types/typography/line-height) — How other tools handle this limitation
- [Unitless Line Height & Tokens plugin](https://www.figma.com/community/plugin/1577516978004090936/unitless-line-height-tokens-css-ready) — Automated alternative approach
- [Syntax Manager plugin](https://www.figma.com/community/plugin/1497527267396324679) — Bulk edit code syntax

*Have you implemented a different workaround for this? Found a way to make this pattern work better? I’d be interested to hear how other teams are handling this gap.*
---
source_title: "Hidden vs. Disabled In UX"
source_url: "https://www.smashingmagazine.com/2024/05/hidden-vs-disabled-ux/"
created: 2026-06-17
tags:
  - "clippings"
---
Should you hide or disable a feature? You’ve probably been there before. Here are some considerations for hiding versus disabling, along with possible alternatives to improve UX. An upcoming part of [Smart Interface Design Patterns](https://smart-interface-design-patterns.com/).

Both **hiding and disabling features can be utterly confusing** to users. And for both, we need very, very good reasons. Let’s take a closer look at what we need to consider when it comes to hiding and disabling — and possible alternatives that help enhance the UX.

This article is **part of our ongoing series** on [design patterns](https://www.smashingmagazine.com/category/design-patterns). It’s also an upcoming part of the 10h-video library on [Smart Interface Design Patterns](https://smart-interface-design-patterns.com/) 🍣 and the [upcoming live UX training](https://smashingconf.com/online-workshops/workshops/interface-design-course-vitaly-friedman/) as well. Use code [BIRDIE](https://smart-interface-design-patterns.com/) to save 15% off.

## Show What’s Needed, Declutter The Rest

You’ve probably been there before: Should you hide or disable a feature? When we hide a feature, we risk **hurting discoverability**. When we disable it without any explanation, we risk that users get frustrated. So, what’s the best way to design for those instances when some options might be irrelevant or unavailable to users?

![Hidden vs. disabled features in UX](https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_80/w_2000/https://files.smashing.media/articles/hidden-vs-disabled-ux/1-hidden-vs-disabled.jpeg)

To hide or not to hide? There are very good reasons for hiding or disabling features and options for a user. But we need to be careful when doing so to not harm the UX. ( Large preview )

As a rule of thumb, disable if you want the user to know a feature exists but is unavailable. Hide if the value shown is currently irrelevant and can’t be used. But **never hide buttons or key filters by default** as users expect them to persist.

Unlike hidden features, disabled features can help users learn the UI, e.g., to **understand the benefits of an upgrade**. So, instead of removing unavailable options or buttons, consider disabling them and allowing the user to “Hide all unavailable options.” Be sure to explain why a feature is disabled and also how to re-enable it.

Another thing to watch out for: When we allow users to switch between showing and hiding a feature, we also need to ensure the switch doesn’t cause any **layout shifts**.

![Hidden vs. disabled features in UX](https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_80/w_2000/https://files.smashing.media/articles/hidden-vs-disabled-ux/2-hidden-vs-disabled.png)

Disabled state in Carbon Design System, with variations for ready-only, default disabled and hidden. ( Large preview )

For both hiding and disabling, we need very thorough considerations of available alternatives, e.g., enabled buttons, read-only state, better empty states, hide/reveal accordions, error messages, and customization. We need to **show what’s needed and de-clutter the rest**.

Whenever possible, I try to keep buttons and features in their default state — **enabled**, accessible, and legible. When a user interacts with that feature, we can explain why they can’t use it, how to enable it, and how to keep it enabled. Possible exceptions are confirmation codes and loading/processing states.

## Hiding vs. Disabling Roadmap

As Sam Salomon [suggests](https://solomon.io/hide-or-disable/), if you’re unsure whether hiding or disabling is the best option for your use case, ask yourself the following question: “ **Will a given user ever be able to interact with this element?**” Depending on your answer, follow the steps below.

**✅ Yes**

→ **Disable it** (as disabled buttons or read-only state).  
↳ For temporary restrictions or filter incompatibility.  
↳ When a value or status is relevant but not editable.  
↳ When an action isn’t available yet (e.g., “Export in progress…”).

**🚫 No**

→ **Hide it** (remove from a toolbar, collapse in accordion).  
↳ E.g., due to permissions, access controls, safety, and security.  
↳ For inaccessible features: e.g., admin buttons, overrides.  
↳ Hide such controls by default and reveal them once a condition is met.

## Key Takeaways

- **Hiding important features** hurts their discoverability.
- **Disabling features** is frustrating without an explanation.
- But some options might be **irrelevant/unavailable to users**.
- Users might expect a feature to exist but won’t find it.
- We need to show what’s needed and de-clutter the rest.
- Avoid **disruptive layout shifts** as you show and hide features.
- **Don’t remove unavailable options** or buttons automatically.
- Instead, disable them and allow it to “Hide all unavailable options.”
- Allow users to hide sections with a lot of disabled functionality.
- **Explain why a feature is disabled** and how to re-enable it.

## Hidden vs. Disabled In Design Systems

The design systems below provide useful **real-world examples** of how products design their hidden and disabled states.

- [Carbon](https://carbondesignsystem.com/patterns/disabled-states/) (disabled state)
- [Carbon](https://carbondesignsystem.com/patterns/read-only-states-pattern/) (read-only state)
- [Unity](https://www.foundations.unity.com/fundamentals/ux-essentials)
- [Vaadin](https://vaadin.com/docs/latest/components/button)
- [SAP](https://experience.sap.com/fiori-design-web/ui-element-states/#hidden)
- [Motif](https://ux.folio.org/docs/guidelines/ux-patterns/hiding-vs-disabling-elements-ux-pattern/)
- [Emplifi](https://soul.emplifi.io/latest/patterns/patterns/disabled-states-NpPW6TcE)

## Useful Resources

- [Disabled Buttons And What To Do Instead](https://adamsilver.io/blog/the-problem-with-disabled-buttons-and-what-to-do-instead/), by Adam Silver
- [Hidden vs. Disabled States](https://uxpsychology.substack.com/p/hidden-vs-disabled-states), by Maria Panagiotidi
- [Making Disabled Buttons Inclusive](https://css-tricks.com/making-disabled-buttons-more-inclusive/), by Sandrina Pereira
- [Hide or Disable](https://solomon.io/hide-or-disable/), by Sam Solomon
- [The Disabled State In UI Design (Sketchnotes)](https://uxknowledgebase.com/the-disabled-state-in-ui-design-8c091d72868), by Krisztina Szerovay
- [Usability Pitfalls of Disabled Buttons](https://www.smashingmagazine.com/2021/08/frustrating-design-patterns-disabled-buttons/), by yours truly Vitaly Friedman
- [Alternative Design Patterns For Disabled Features](https://uxdesign.cc/why-your-design-team-hates-disabled-features-1c7ef6bfdc03), by Katie Jacquez
- [Designing Filters UX That Works](https://www.smashingmagazine.com/2021/07/frustrating-design-patterns-broken-frozen-filters/), by yours truly Vitaly Friedman
- [UI Traps: Disabled Buttons and Inputs](https://www.carletondesign.com/2023/06/15/disabled-buttons/), by James Carleton

## Meet Smart Interface Design Patterns

If you are interested in similar insights around UX, take a look at **[Smart Interface Design Patterns](https://smart-interface-design-patterns.com/)**, our **10h-video course** with 100s of practical examples from real-life projects — with a live UX training later this year. Everything from mega-dropdowns to complex enterprise tables — with 5 new segments added every year. [Jump to a free preview](https://www.youtube.com/watch?v=aSP5oR9g-ss).

![Smart Interface Design Patterns](https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_80/w_2000/https://archive.smashing.media/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7cc4e1de-6921-474e-a3fb-db4789fc13dd/b4024b60-e627-177d-8bff-28441f810462.jpeg)

Meet Smart Interface Design Patterns, our video course on interface design & UX.

100 design patterns & real-life examples.  
10h-video course + live UX training. [Free preview](https://www.youtube.com/watch?v=aSP5oR9g-ss).

![Smashing Editorial](https://www.smashingmagazine.com/images/logo/logo--red.png) (yk)
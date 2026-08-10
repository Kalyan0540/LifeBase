---
type: source
source_title: "Your Figma Drop Shadows Look Cheap (Fix This in 2 Minutes)"
source_url: "https://www.youtube.com/watch?v=oIX5vfuegZI&t=18s"
raw_path: "raw/knowledge/product-and-design/design/Your Figma Drop Shadows Look Cheap (Fix This in 2 Minutes).md"
created: 2026-07-17
updated: 2026-07-17
---

# Your Figma Drop Shadows Look Cheap (Fix This in 2 Minutes)

A short UI Collective Figma tutorial about making dashboard/card shadows subtler by using negative spread values instead of relying only on blur radius and opacity.

## Main Technique

Default drop shadows can look heavy and square, especially on repeated UI cards. Increasing blur alone can still leave the shadow too prominent.

The source's main trick is to set the shadow spread to a negative value. A negative spread pulls the shadow inward, making it softer and less bulky around the object.

Example direction from the video:

- add a normal drop shadow
- lower opacity where needed
- set spread to a negative value such as `-4` or stronger
- test the result on repeated cards, not just one isolated element

## Design Implication

Subtle shadows work best when they support hierarchy without becoming the visual focus. This matters in dashboards because repeated cards amplify any heavy elevation style.

## Links

- [[Subtle UI Shadows]] - concept derived from this source

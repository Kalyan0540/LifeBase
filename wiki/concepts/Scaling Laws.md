---
type: concept
sources:
  - "[[Why does every mammal get 1 billion heartbeats in their life?]]"
created: 2026-07-28
updated: 2026-07-28
---

# Scaling Laws

Scaling laws describe how one quantity changes as another grows. The key lesson from the source is that real systems often depart from simple proportionality.

## Power laws

A power law has the form where one quantity scales with another raised to an exponent. When plotted on a log-log chart, power-law data forms a roughly straight line, and the slope of that line is the exponent.

Common cases:

- linear scaling: exponent 1
- sublinear scaling: exponent below 1, creating efficiency with size
- superlinear scaling: exponent above 1, creating intensified output or risk with size

## Biological scaling

Animal metabolism is the main biological example. Larger animals use more total energy than smaller animals, but metabolic rate does not rise in direct proportion to body mass.

The source contrasts two candidate exponents:

- surface law: metabolic rate scales near mass to the two-thirds power
- Kleiber's Law: metabolic rate scales near mass to the three-quarters power

Many biological traits then appear as related quarter-power laws. Heart rate decreases with size, lifespan increases with size, and those opposing relationships explain why many mammals land near the same lifetime heartbeat count.

## Network explanation

WBE theory explains biological scaling through efficient, branching, space-filling transport networks.

The theory matters because it tries to connect an observed pattern to a mechanism: resource distribution through fractal-like networks, rather than just curve-fitting animal measurements.

## Urban scaling

Cities show their own scaling patterns:

- infrastructure tends to scale sublinearly, so large cities can use shared resources more efficiently per person
- socioeconomic outputs and some harms scale superlinearly, so large cities amplify invention, wages, disease, crime, and pace of life

The city comparison generalizes the lesson: bigger systems can become more efficient in some dimensions while becoming more intense or fragile in others.

## Practical takeaway

Do not assume that scaling up means multiplying every input and output by the same factor. Ask which constraint actually governs the system: surface area, transport networks, shared infrastructure, interaction density, measurement limits, or something else.

## Links

- [[Why does every mammal get 1 billion heartbeats in their life?]] - primary source
- [[System Design Fundamentals]] - adjacent scaling and tradeoff reasoning in software architecture

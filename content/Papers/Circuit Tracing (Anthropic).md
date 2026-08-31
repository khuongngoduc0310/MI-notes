---
type: paper
title: "Circuit Tracing: Revealing Computational Graphs in Language Models"
authors: "Emmanuel Ameisen*,Jack Lindsey*,Adam Pearce*,Wes Gurnee*,Nicholas L. Turner*,Brian Chen*,Craig Citro*,\rDavid Abrahams,Shan Carter,Basil Hosmer,Jonathan Marcus,Michael Sklar,Adly Templeton,\rTrenton Bricken,Callum McDougall◊,Hoagy Cunningham,Thomas Henighan,Adam Jermyn,Andy Jones,Andrew Persic,Zhenyi Qi,T. Ben Thompson,\rSam Zimmerman,Kelley Rivoire,Thomas Conerly,Chris Olah,Joshua Batson*‡"
year: "2025"
status: reading
tags:
  - paper
---

# Circuit Tracing (Anthropic)

## TL;DR

Anthropic’s **Circuit Tracing** method tries to explain **how a language model produces a specific output** by converting its computation into an interpretable **[Attribution Graph](Attribution%20Graph)**.

## Problem

Explain **how the model produces an answer** by identifying which [features](Feature.md) activate and how information flows between them.

## Main Idea

Replacing the model MLPs with [](Cross%20Layer%20Transcoder.md#Definition|Cross%20Layer%20Transcoders) for better interpretability.  Labeling the features and trace the path of a specific prompt. Then validate with technique like steering activation or group of activations to see its behavior.

## Concepts

- [Attribution Graph](Attribution%20Graph)
- [Replacement Models](Replacement%20Models.md)
- [Cross Layer Transcoder](Cross%20Layer%20Transcoder.md)
- [Feature](Feature.md)

## Method

### Step 1: Decompose the model

Break the model computation into more interpretable features.

### Step 2: Providing descriptions of the components

Assign meaning to features.
### Step 3: Characterizing how components interact to produce behavior

Build an [Attribution Graph](Attribution%20Graph) showing how features influence each other.

### Step 4: Validate the the descriptions

Intervene on features and check if the model change its behavior as predicted.

## Important Definitions

- [Feature](Feature.md)
- [Attribution Graph](Attribution%20Graph)
- [Cross Layer Transcoder](Cross%20Layer%20Transcoder.md)
- [Replacement Models](Replacement%20Models.md)

## Important Findings

- [Features](Feature.md) are more interpretable than individual neurons.
- [Attribution graphs](Attribution%20Graph) reveal possible computational paths through the model.
- Interventions help test whether a feature is **causally important**, not just correlated.

## Things I Don't Understand

- The Jacobian between source and target

## My Understanding

Explain the paper without copying the authors.

## My Thoughts

Your criticism, ideas, or connections.

## Related Papers

- [Circuit Tracing (Anthropic)](.md)

## References

- Paper: https://transformer-circuits.pub/2025/attribution-graphs/methods.html
- Website: https://transformer-circuits.pub/2025/attribution-graphs/methods.html
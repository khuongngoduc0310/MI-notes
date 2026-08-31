---
type: concept
aliases:
  - MLP
  - MLPs
  - Multi-Layer Perceptron
tags:
  - concept
---

# Multi Layer Perceptron

## Definition

An **MLP (Multi-Layer Perceptron)** is the feed-forward part of a transformer layer that independently transforms each token’s residual-stream representation through linear layers and a nonlinearity.

In simple form:

$\text{MLP}(x)=W_2\,\sigma(W_1x+b_1)+b_2$

- $W_1$: expands/transforms the representation
- $\sigma$: nonlinear activation
- $W_2$: projects it back to the residual-stream dimension

Its output is then **added back into the [Residual Stream](Residual%20Stream.md)**.

## Related Concepts

- [Residual Stream](Residual%20Stream.md)
- [Transformer](Transformer)
- [Transcoder](Transcoder.md)
- [Cross Layer Transcoder](Cross%20Layer%20Transcoder.md)
- [Feature](Feature.md)
- [Activation Function](Activation%20Function)

## Sources

- [Attention Is All You Need](Attention%20Is%20All%20You%20Need)
- [Circuit Tracing (Anthropic)](Circuit%20Tracing%20(Anthropic).md)
---
type: concept
aliases:
tags:
  - concept
---

# Residual Stream

## Definition

The **Residual Stream** is the main vector representation that carries information about each token through the transformer layers.

Each attention and [MLP](MLP) block reads from it, computes an update, and adds that update back into the stream.

## Simple Explanation

Think of it as the model's shared **information workspace**.
$$
\begin{gather*}
\text{Residual Stream} \\
\downarrow \\
\text{Attention / MLP reads from it} \\
\downarrow \\
\text{Computes new information} \\
\downarrow \\
\text{Add the result back} \\
\downarrow \\
\text{Updated residual stream} \\
\end{gather*}
$$

## Why It Matters

The residual stream is important because it is where information is:

- Stored and updated across layers
- Read by [Attention](Attention) and [MLP](MLP) blocks
- Used to represent [features](Feature.md)
- Traced in mechanistic interpretability

Many tools such as [SAEs](Sparse%20Autoencoder.md) and [Transcoders](Transcoder.md) analyze the residual stream to understand what the model is representing and computing.

## Related Concepts

- [Transformer](Transformer)
- [Attention](Attention)
- [MLP](MLP)
- [Feature](Feature.md)
- [Sparse Autoencoder](Sparse%20Autoencoder.md)
- [Transcoder](Transcoder.md)
- [Cross Layer Transcoder](Cross%20Layer%20Transcoder.md)

## Sources

- [Attention Is All You Need](Attention%20Is%20All%20You%20Need)
- [Circuit Tracing (Anthropic)](Circuit%20Tracing%20(Anthropic).md)
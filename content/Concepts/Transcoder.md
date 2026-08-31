---
type: concept
aliases:
  - transcoders
tags:
  - concept
---

# Transcoder

## Definition

A **Transcoder** is a sparse model that reads from the [Residual Stream](Residual%20Stream.md), converts the activation into interpretable [features](Feature.md), and uses those features to reconstruct the output of a model component, usually an [Multi Layer Perceptron](Multi%20Layer%20Perceptron.md).

$\text{Residual} \rightarrow \text{Sparse Features} \rightarrow \text{MLP Output}$

Unlike an [SAE](Sparse%20Autoencoder.md), it reconstructs the **MLP output**, not its original input.
## Example

$$
\begin{gather*}
\text{Residual Stream} \\
\downarrow \\
\text{Transcoder Encoder} \\
\downarrow \\
\text{Sparse Features} \\
\downarrow \\
\text{Transcoder Decoder} \\
\downarrow \\
\text{Reconstructed MLP Output} \\
\downarrow \\
\text{Residual Stream}
\end{gather*}
$$


## Why It Matters

Transcoders help explain **what an MLP computes**, rather than only what information is represented.

This makes them useful for:

- Finding interpretable computations
- Tracing feature-to-feature interactions
- Building [Attribution Graphs](Attribution%20Graph)

## Related Concepts

- [Sparse Autoencoder](Sparse%20Autoencoder.md)
- [Cross Layer Transcoder](Cross%20Layer%20Transcoder.md)
- [Feature](Feature.md)
- [Multi Layer Perceptron](Multi%20Layer%20Perceptron.md)
- [Residual Stream](Residual%20Stream.md)
- [Attribution Graph](Attribution%20Graph)

## Sources

- [Circuit Tracing (Anthropic)](Circuit%20Tracing%20(Anthropic).md)
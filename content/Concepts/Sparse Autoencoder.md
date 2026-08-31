---
type: concept
aliases:
  - SAE
tags:
  - concept
---
# Sparse Autoencoder

## Definition

A **Sparse Autoencoder (SAE)** is a model that takes a neural network's activation and converts it into a set of sparse, more interpretable [features](Feature.md), then uses those features to reconstruct the original activation.

$\text{Activation} \rightarrow \text{Sparse Features} \rightarrow \text{Reconstructed Activation}$
or

$r \rightarrow  \text{sparse features} \rightarrow \hat{r}$

The word **sparse** means that only a small number of features are active at the same time.

---

## Why It Matters

Because of [Superposition](Superposition.md), information is not necessarily stored cleanly in individual neurons.

- One [Feature](Feature.md) can be distributed across many neurons.
    
- One neuron can participate in many features.
    

This makes individual neurons difficult to interpret.

SAEs try to recover cleaner, interpretable features from those mixed activations.

They are useful for understanding:

- What information the model represents
    
- Which features activate for a prompt
    
- How concepts are encoded
    
- Which features may participate in a [Circuit](Circuit)
    

### SAE vs Transcoder

An SAE reconstructs the **activation it reads**:

```text
Residual Stream
      ↓
Sparse Features
      ↓
Reconstructed Residual Stream
```

A [Transcoder](Transcoder.md) instead tries to reconstruct the **output of another model component**, usually an [Multi Layer Perceptron](Multi%20Layer%20Perceptron.md):

```text
Residual Stream
      ↓
Sparse Features
      ↓
Reconstructed MLP Output
```

Therefore:

> **SAE → explains representation**

> **Transcoder → explains computation**

---

## Related Concepts

- [Feature](Feature.md)
    
- [Neuron](Neuron)
    
- [Superposition](Superposition.md)
    
- [Sparse Coding](Sparse%20Coding)
    
- [Residual Stream](Residual%20Stream.md)
    
- [Transcoder](Transcoder.md)
    
- [Cross-Layer Transcoder](Cross-Layer%20Transcoder)
    
- [Multi Layer Perceptron](Multi%20Layer%20Perceptron.md)
    
- [Circuit](Circuit)
    
- [Mechanistic Interpretability](Mechanistic%20Interpretability)

---

## Sources

- [Toy Models of Superposition](Toy%20Models%20of%20Superposition)
    
- [Circuit Tracing (Anthropic)](Circuit%20Tracing%20(Anthropic).md)
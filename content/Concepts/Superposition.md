---
type: concept
aliases:
  - feature superposition
---

# Superposition

## Definition

A model represents more features than it has available dimensions by
representing features using overlapping directions.

## My understanding

Instead of:

Neuron 1 = Feature A

it can be more like:

Neuron 1 = partly A + B + C
Neuron 2 = partly A + C
Neuron 3 = partly B + C

Therefore features are represented across combinations of neurons.

## Why it matters

This is one reason individual neurons are often difficult to interpret.

## Sources

- [Toy Models of Superposition](Toy%20Models%20of%20Superposition)
- [Sparse Autoencoders Paper](Sparse%20Autoencoders%20Paper)

## Related

- [Features](Features)
- [Sparse Autoencoder](Sparse%20Autoencoder.md)
- [Polysemanticity](Polysemanticity)
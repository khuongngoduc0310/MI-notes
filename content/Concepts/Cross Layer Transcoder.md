---
type: concept
aliases:
  - CLT
  - Cross Layer Transcoder
  - CLTs
---
# Cross Layer Transcoder

## Definition

A cross-layer [Transcoder](Transcoder.md) consist of neurons ("features") divided into $L$ layers (same as the model) to reconstruct the output of MLPs of the original model, using **sparse** active features.
- Each feature of the $l^{th}$ layer get input from the residual stream using a **linear encoder** followed by **a nonlinearity** 
- An $l^{th}$ layer feature contribute to the reconstruct of the MLP **outputs** in layer after it ($l , l + 1, ..., L$) using **linear decoder** weights for each output layer.
- All of the features a train *jointly* -> output of the layer $l'$ is reconstructed by features from all previous layers.
 ![Pasted image 20260830140959](Pasted%20image%2020260830140959.png)

- To **run** a CLT:
	- $a^l = \text{JumpRELU}(W^{l}_{enc}x^l)$
		- $x^l$ original residual stream at layer $l$
		- $a^l$ feature activation at layer $l$
		- $W^{l}_{enc}$ is the CLT encoder matrix at layer $l$
- CLT attempted to reconstruct output of the original model at layer $l$
	- $\hat{y}^l = \sum_{l' = 1}^{l} W^{l' \rightarrow l}_{dec} a^{l'}$
## Related concepts

- [Single Layer Transcoder](Single%20Layer%20Transcoder)
- [Residual Stream](Residual%20Stream.md)
## Source
- [Circuit Tracing (Anthropic)](Circuit%20Tracing%20(Anthropic).md)
---
created: 2023-08-09 04:46
aliases: 
- Attention is All You Need
tags:
- rn
cssclasses:
- 
publish:
dg-publish: false
---

<!--
tags: 
-->

<!--internal
parent:: [[]]
child:: [[]]
related:: [[notes/202308061603 Research Papers|Research Paper]]
-->

<!--external
- [ ] [Transformer — Attention Is All You Need Easily Explained With Illustrations](https://luv-bansal.medium.com/transformer-attention-is-all-you-need-easily-explained-with-illustrations-d38fdb06d7db#:~:text=A%20Transformer%20is%20a%20type,top%20of%20the%20transformer%20model.)
- [ ] [Attention is all you need: understanding with example](https://medium.com/data-science-in-your-pocket/attention-is-all-you-need-understanding-with-example-c8d074c37767)
- [ ] [Attention is all you need: Discovering the Transformer paper](https://towardsdatascience.com/attention-is-all-you-need-discovering-the-transformer-paper-73e5ff5e0634)
-->

# [Attention Is All You Need](https://arxiv.org/abs/1706.03762)

![[notes/images/Pasted image 20230809044742.png]]

The Transformer architecture consists of an encoder and a decoder, each of which is composed of several layers

Each layer consists of two sub-layers
- A multi-head self-attention mechanism and 
- A feed-forward neural network. 

The multi-head self-attention mechanism allows the model to attend to different parts of the input sequence

The feed-forward network applies a point-wise fully connected layer to each position separately and identically

The Transformer model a uses residual connections and layer normalization to facilitate training and prevent overfitting. 

In addition, the authors introduce a positional encoding scheme that encodes the position of each token in the input sequence, enabling the model to capture the order of the sequence

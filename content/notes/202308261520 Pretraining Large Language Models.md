---
created: 2023-08-26 15:19
aliases: 
- Pre-training Large Language Models
- Pre-training
- Training
tags:
- 
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
related:: [[]]
-->

<!--external
- [ ] []()
-->

# Pre-training Large Language Models

[[notes/20230628030810 Large Language Models (LLMs)|LLMs]] encode a deep statistical representation of language developed during the models pre-training phase when the model learns from vast amounts of unstructured textual data. 

Pre-training requires a [[notes/20230826170037 Data for Training Large Language Models|large amount of data]], compute and the use of GPUs. 

In this self-supervised learning step, the model internalizes the patterns and structures present in the language. These patterns then enable the model to complete its training objective, which depends on the architecture of the model. During pre-training, the model weights get updated to minimize the loss of the training objective. 

![[notes/images/Screenshot 2023-08-26 at 3.40.11 PM.png]]

There are 3 variance of the transformer model
- [[notes/20230809041717 Encoder-only Models#Pre-training|Encoder-only Models]] are pre-trained using [[notes/202308261543 Masked Language Modeling|Masked Language Modeling]]
- [[notes/20230809040949 Decoder-only Models#Pre-training|Decoder-only Models]] are pre-trained using [[notes/202308261555 Causal Language Modeling|Causal Language Modeling]]
- [[notes/20230809041643 Encoder-Decoder Models#Pre-training|Encoder-Decoder Models]] are pre-training using [[notes/202308261653 Span Corruption|Span Corruption]]

![[notes/images/Screenshot 2023-08-26 at 5.04.21 PM.png]]

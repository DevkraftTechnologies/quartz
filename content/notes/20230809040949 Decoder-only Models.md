---
created: 2023-08-09 04:09
aliases: 
- Decoder-only Models
- Autoregressive Models
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
parent:: [[202308090324 Generating Text with Transformers]]
child:: [[]]
related:: [[]]
-->

<!--external
- [ ] []()
-->

# Decoder-only Models

![[notes/images/Screenshot 2023-08-09 at 4.44.22 AM.png|250]]

[[notes/202308090433 Decoder|Decoder]]-only models (like GPT, BLOOM, Jurassic, LLaMA) generalize to most tasks with scale #TODO 

## Pre-training

- Decoder-only or Autoregressive Models are pre-trained using [[notes/202308261555 Causal Language Modeling|Causal Language Modeling]]
- Decoder-based autoregressive models, mask the input sequence and can only see the input tokens leading up to the token in question. 
- The model has no knowledge of the end of the sentence. 
- The model then iterates over the input sequence one by one to predict the following token. 
- In contrast to the [[notes/20230809041717 Encoder-only Models|Encoder-only Models]] architecture, this means that the **context is unidirectional**
- The model builds up a statistical representation of language through the process of learning to predict the next token from a vast number of examples
## Use cases

- Decoder-only models are often used for text generation
- However, larger decoder-only models show strong zero-shot inference abilities

---
created: 2023-08-09 04:16
aliases: 
- Encoder-Decoder Models
- Sequence-to-Sequence Models
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

# Encoder-Decoder Models

- Encoder-decoder models (like BART) perform well on sequence-to-sequence tasks such as translation, where the input sequence and the output sequence can be different lengths. 
- Examples of encoder-decoder models include BART as opposed to BERT and T5
## Pre-training

- T5 is pre-trained using [[notes/202308261653 Span Corruption|Span Corruption]]
## Use Cases

>useful in cases both input and output are a body of text

- translation
- summarization and 
- question-answering
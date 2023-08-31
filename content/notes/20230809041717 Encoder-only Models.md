---
created: 2023-08-09 04:17
aliases: 
- Encoder-only Models
- Autoencoding Models
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

# Encoder-only Models

![[notes/images/Screenshot 2023-08-09 at 4.43.01 AM.png|250]]

- [[notes/202308090432 Encoder|Encoder]]-only models (like BERT) also work as sequence-to-sequence models where the input sequence and the output sequence are of the same length
- With additional layers to the architecture, It is possible to train encoder-only models to perform classification tasks such as sentiment 
## Pre-training

- These models are pre-trained using [[notes/202308261543 Masked Language Modeling|Masked Language Modeling]]
- Auto-encoding models build bi-directional representations of the input sequence
- The model has an understanding of the full context of a token and not just of the words that come before
- Encoder-only models suited to task that benefit from this bi-directional contexts. 
## Use Case

- sentence classification
	- sentiment analysis
- token-level tasks 
	- named entity recognition
	- word classification

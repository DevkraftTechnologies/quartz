---
created: 2023-10-03 03:20
aliases:
  - How are sentence embeddings computed
tags: 
cssclasses: 
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

# How are [[notes/20231002174118 Sentence Embeddings|Sentence Embeddings]] computed?

## Modern Embeddings

- use a transformer neural network to compute a context-aware representation of each word, then take an average of the context-aware representations.
- compute embeddings for each token (e.g., sub-word) rather than word. Enables algorithm to work even for novel words and misspelt words ("Life, the unverse and everything.")
## Training the Transformer Network (Contrastive Learning)

given a dataset of pairs of "similar" sentences, tune neural network to move similar sentences' embeddings together, and dissimilar sentences' embeddings apart.
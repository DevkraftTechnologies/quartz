---
created: 2023-10-03 04:09
aliases: 
- Encode Texts to Embeddings
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
parent:: [[20231003040824 Helper Functions]]
child:: [[]]
related:: [[]]
-->

<!--external
- [ ] []()
-->
# Encode Texts to Embeddings

This helper function calls `model.get_embeddings()` on the batch of data, and returns a list containing the embeddings for each text in that batch.

```python
def encode_texts_to_embeddings(sentences):
    try:
        embeddings = model.get_embeddings(sentences)
        return [embedding.values for embedding in embeddings]
    except Exception:
        return [None for _ in range(len(sentences))]
```


---
created: 2023-10-02 16:50
aliases:
  - L1-Embeddings-api-intro
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

# L1-Embeddings-api-intro

## Embeddings

```python
from vertexai.language_models import TextEmbeddingModel
embedding_model = TextEmbeddingModel.from_pretrained("textembedding-gecko@001")
```

```python
embedding = embedding_model.get_embeddings(["What is the meaning of life?"])
```

```python
vector = embedding[0].values
# print(f"Length = {len(vector)}") # 768
print(vector[:10])
```

> [-0.006005102302879095, 0.015532972291111946, -0.030447669327259064, 0.05322219058871269, 0.014444807544350624, -0.0542873740196228, 0.045140113681554794, 0.02127358317375183, -0.06537645310163498, 0.019103270024061203]

<mark style="background: #BBFABBA6;">as long as we use the same model, embeddings for the input string are idempotent i.e. will be same for the same input string no matter the number of re-tries</mark>

![[notes/20231002174829 cosine similarity]]



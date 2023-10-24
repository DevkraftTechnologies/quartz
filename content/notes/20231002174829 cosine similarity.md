---
created: 2023-10-02 17:48
aliases: 
- cosine similarity
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
parent:: [[202310021650 L1-Embeddings-api-intro]]
child:: [[]]
related:: [[]]
-->

<!--external
- [ ] []()
-->
# cosine similarity

```python
from sklearn.metrics.pairwise import cosine_similarity
```

```python
emb_1 = embedding_model.get_embeddings(
    ["What is the meaning of life?"]) # 42!

emb_2 = embedding_model.get_embeddings(
    ["How does one spend their time well on Earth?"])

emb_3 = embedding_model.get_embeddings(
    ["Would you like a salad?"])

vec_1 = [emb_1[0].values]
vec_2 = [emb_2[0].values]
vec_3 = [emb_3[0].values]
```

```python
print(cosine_similarity(vec_1,vec_2)) 
print(cosine_similarity(vec_2,vec_3))
print(cosine_similarity(vec_1,vec_3))
```

```python
[[0.65503744]]

[[0.52001556]]

[[0.54139322]]
```

<mark style="background: #BBFABBA6;">The cosine similarity values for these vectors all fall within a narrow range because the because the vectors are high dimensional (768)</mark>

<mark style="background: #ABF7F7A6;">The relative difference in values between these distances is still quite useful</mark>
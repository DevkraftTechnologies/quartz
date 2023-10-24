---
created: 2023-10-02 17:41
aliases:
  - Sentence Embeddings
tags:
  - rn
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
# Sentence Embeddings

let's assume the method to calculate sentence embeddings from [[notes/20230703031649 Word Embeddings|Word Embeddings]] is to take the average of the word embeddings
```python
in_1 = "The kids play in the park."
in_2 = "The play was for kids in the park."
```

after we removing stopwords

```python
in_pp_1 = ["kids", "play", "park"]
in_pp_2 = ["play", "kids", "park"]
```

we generate one embedding for each word in in a sentence

```python
embeddings_1 = [emb.values for emb in embedding_model.get_embeddings(in_pp_1)]
```

> [-0.03156903386116028, 0.008489725179970264, 0.017588036134839058, 0.032134201377630234, ...]
> 
> [0.020638465881347656, -0.009862425737082958, -0.007717186119407415, 0.03578021004796028, ...]
> 
> [-0.0006435823743231595, -0.014306388795375824, 0.007359375711530447, 0.03201877698302269, ...]

```python
embeddings_2 = [emb.values for emb in embedding_model.get_embeddings(in_pp_2)]
```

if we take the average embedding across the 3 word embeddings for each sentence, we get same embedding for both sentences

> [-0.00385805 -0.00522636  0.00574341  0.03331106, ...]
> [-0.00385805 -0.00522636  0.00574341  0.03331106, ...]

This ignores word order and context, so two sentences with different meanings, but the same set of words will end up with the same sentence embedding

whereas generating embedding using an LLM will result in different embeddings for each sentence

```python
embedding_1 = embedding_model.get_embeddings([in_1])
embedding_2 = embedding_model.get_embeddings([in_2])
```

> [0.0039385221898555756, -0.020830577239394188, -0.002994248876348138, -0.007580515928566456, ...]
> 
> [-0.01565515622496605, -0.012884826399385929, 0.01229254249483347, -0.0005865463172085583, ...]

The embedding model uses stop words and order of words in a sentence to understand semantics of the sentences

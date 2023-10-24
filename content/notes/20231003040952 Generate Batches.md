---
created: 2023-10-03 04:09
aliases: 
- Generate Batches
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
# Generate Batches

To generate embeddings for a dataset of texts, we'll need to group the sentences together in batches and send batches of texts to the model

For ex. vertexai model API can take batches of up to 5 pieces of text per API call.

```python
def generate_batches(sentences, batch_size = 5):
    for i in range(0, len(sentences), batch_size):
        yield sentences[i : i + batch_size]
```

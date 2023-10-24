---
created: 2023-10-03 03:38
aliases: 
- Dimension Reduction (PCA)
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
parent:: [[notes/20231002174118 Sentence Embeddings|Sentence Embeddings]]
child:: [[]]
related:: [[]]
-->

<!--external
- [ ] []()
-->

# Dimension Reduction (PCA)

for ex. reduce embeddings from 768 to 2 dimensions for visualization

```python
from sklearn.decomposition import PCA

# Perform PCA for 2D visualization
PCA_model = PCA(n_components = 2) # lose a lot of information
PCA_model.fit(embeddings_array)
new_values = PCA_model.transform(embeddings_array)
```

```python
print("Shape: " + str(new_values.shape))
print(new_values)
```

```python
import matplotlib.pyplot as plt
import mplcursors
%matplotlib ipympl

from utils import plot_2D
plot_2D(new_values[:,0], new_values[:,1], input_text_lst_news)
```
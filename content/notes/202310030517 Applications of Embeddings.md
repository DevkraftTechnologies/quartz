---
created: 2023-10-03 05:17
aliases:
  - Applications of Embeddings
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

# Applications of Embeddings

- clustering
- classification

## Anomaly Detection

use <mark style="background: #D2B3FFA6;"> IsolationForest</mark> model to detect anomalies. `IsolationForest` classifier will predict `-1` for potential outliers, and `1` for non-outliers.

for ex. in cdefense instead of using a graph database to weigh the events in cloudtrail logs, instead embed the text of the log using an LLM model

having said that, it is possible to do this for streaming data?



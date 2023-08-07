---
title: "Recurrent Neural Networks (RNNs)"
created: 2023-07-03 01:22
aliases: 
- Recurrent Neural Networks (RNNs)
- Recurrent Neural Networks
- RNNs
tags:
- TODO
cssclasses:
- 
publish:
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
- []()
-->

# Recurrent Neural Networks (RNNs)

![[Screenshot 2023-08-07 at 4.53.07 AM.png]]
## Limitations

- with just one previous word available to the model, prediction was not good
- As we scale the RNN to be able to see more of the preceding words in the text, we have to scale the resources that the model uses a lot and prediction would fail ![[Screenshot 2023-08-07 at 4.44.41 AM.png]]![[Screenshot 2023-08-07 at 4.45.06 AM.png]]

- To predict the next word, models need to see more than just the previous few words.
- Models needs to have an understanding of the whole sentence or even the whole document.
- The problem is that language is complex. 
- In languages, one word can have multiple meanings i.e. homonyms
- when provided a sentence, RNNs cannot remember the start of a sentence
- RNNs use recurrence as result **could not be parallelized**
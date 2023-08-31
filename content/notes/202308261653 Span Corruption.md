---
created: 2023-08-26 16:53
aliases: 
- Span Corruption
tags:
- 
cssclasses:
- 
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

# Span Corruption

![[notes/images/Screenshot 2023-08-26 at 4.53.55 PM.png]]

- The process involved masking random sequences of input tokens
- These masked sequences are then replaced with a unique **Sentinel Token**
- These special tokens do not correspond to any actual word from the input text
- The decoder is then tasked with reconstructing the mask token sequences in an auto-regressive manner 
- The output is the Sentinel token followed by the predicted tokens
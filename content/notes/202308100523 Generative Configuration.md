---
created: 2023-08-10 05:23
aliases: 
- Generative Configuration
- Configuration
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

# Generative Configuration

Each [[notes/20230628030901 Generative AI|Generative]] model exposes a set of configuration parameters that can influence the model's output during inference. 

These are different than the training parameters which are learned during training time. 

Instead, these configuration parameters are invoked at inference time and give us control over things like the maximum number of tokens in the completion, and how creative the output is

- [[notes/202308100605 Max New Token|Max New Token]]
- [[notes/20230810055942 Top-K sampling|Top-K value]]
- [[notes/20230810055842 Top-P sampling|Top-P value]]
- [[notes/20230810055747 Temperature|Temperature]]
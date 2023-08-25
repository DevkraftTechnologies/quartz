---
created: 2023-08-10 06:34
aliases: 
- Adapt and Align stage
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
parent:: [[202308061649 Generative AI project Lifecycle]]
child:: [[]]
related:: [[]]
-->

<!--external
- [ ] []()
-->

# Adapt and Align Stage

The next step is to assess the model's performance and perform additional training if needed

[[notes/202308090519 Prompt Engineering|Prompt Engineering]] can sometimes be enough to get the model to perform well, start with trying in-context learning, using examples suited to the task and use case. 

There are still cases, however, where the model might not perform as well as required, even with one or a few short inference, and in that case, we can try [[notes/202308061628 Instruction Fine Tuning|Fine-Tuning]] the model

set up some metrics and benchmarks to determine how well the model is performing or how well it is aligned to the requirements and preferencs

The adapt and aligned stage can be quite iterative in order to get the performance required
- attempt prompt engineering
- evaluating the output
- use fine tuning to improve performance
- revisiting and evaluate prompt engineering one more time 
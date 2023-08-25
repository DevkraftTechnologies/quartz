---
created: 2023-08-09 05:51
aliases: 
- In-Context Learning (ICL)
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
parent:: [[202308090519 Prompt Engineering]]
child:: [[]]
related:: [[]]
-->

<!--external
- [ ] []()
-->

# In-Context Learning (ICL)

**In-Context Learning** is the practise of providing examples inside the [[notes/202308090550 Context Window|Context Window]] of a Prompt in order to get the model to produce better outcomes. It is useful in [[notes/202308090519 Prompt Engineering|Prompt Engineering]]

- [[notes/20230809055419 Zero-Shot Inference|Zero-Shot Inference]]
- [[notes/20230809055340 One-Shot Inference|One-Shot Inference]]
- [[notes/20230809055214 Few-Shot Inference|Few-Shot Inference]]

However, we have a **limit on the amount of examples** we can provide for in-context learning that due to the **size of the context window**

if the model isn't performing well even after including five or six examples, consider [[notes/202308061628 Instruction Fine Tuning|Fine Tuning]] the model instead



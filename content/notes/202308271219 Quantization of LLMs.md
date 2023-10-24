---
created: 2023-08-27 12:19
aliases:
  - Quantization
  - Quantization of LLMs
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

# Quantization of LLMs

Quantization is kind of a compression technique for LLMs. 

In practice, The main goal of quantization is to lower the precision of the LLM’s weights from 16-bit to 8-bit, 4-bit, or even 3-bit, with minimal performance degradation

There are two popular quantization methods for LLMs: 

- GPTQ and 
- bits and bytes
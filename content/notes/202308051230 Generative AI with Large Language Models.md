---
created: 2023-08-05 12:30
aliases: 
- Generative AI with Large Language Models
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

# Generative AI with Large Language Models

## Objectives

- Discuss model pre-training and the value of continued pre-training vs fine-tuning
- Define the terms [[notes/20230628030901 What is Generative AI|Generative AI]], [[notes/20230628030810 Large Language Models (LLMs)|Large Language Models]], prompt, and describe the  [[notes/20230703011428 Transformers|Transformer]] architecture that powers LLMs
- Describe the steps in a typical LLM-based, generative AI model lifecycle and discuss the constraining factors that drive decisions at each step of model lifecycle
- Discuss computational challenges during model pre-training and determine how to efficiently reduce memory footprint
- Define the term scaling law and describe the laws that have been discovered for LLMs related to training dataset size, compute budget, inference requirements, and other factors.

## Prerequisites

- Python
- Tensorflow

## Timeline
### Week 1

- Examine [[notes/20230703011428 Transformers|Transformer]] Architecture, Explore how these models are trained and compute resources required
- [[notes/202308061627 In-context Learning|In-context Learning]] to guide the model to output at inference time using prompt engineering

### Week 2

- Explore options adapt pre-trained models to specific tasks and datasets using a process called [[notes/202308061628 Instruction Fine Tuning|Instruction Fine Tuning]]

### Week 3

- How to align outputs of language models with human values in order to increase helpfulness and reduce potential harm i.e. [[notes/202308051314 RLHF|RLHF]]
ors
---
created: 2023-10-05 03:24
aliases:
  - Chain-of-Verification (COVE) method
  - (COVE)
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
- [ ] [Chain-of-Verification Reduces Hallucination in Large Language Models](https://arxiv.org/pdf/2309.11495.pdf)
-->

# Chain-of-Verification (COVE) method

The method involves that the model first
- drafts an initial response; then
- plans verification questions to fact-check its draft
- answers those questions independent each other so the answers are not biased by other responses
- generates its final verified response

COVE decreases hallucinations across a variety of tasks, from list-based questions to closed book MultiSpanQA and longform text generation

![[notes/images/Pasted image 20231005032503.png]]

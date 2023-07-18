---
created: 2023-06-30 02:05
aliases: 
- Generative AI vs Discriminative AI
tags:
- 
cssclasses:
- 
publish:
---

%% 
tags: 
%%

%%internal
parent:: [[]]
child:: [[]]
related:: [[]]
%%

%%external
- []()
%%

# Generative AI vs Discriminative AI

When working with [[notes/20230630020251 Discriminative AI|Discriminative AI]], we don’t care about these features in and of themselves - we only care about them insofar as they help us make a decision.

In contrast, with [[notes/20230628030901 Generative AI|Generative AI]], we do care about these features themselves. 

Indeed, the whole goal of Generative AI is to understand how these features relate in order to generate plausible data. 

For example, suppose our goal is to generate a representative sample of humans in terms of body size (considering only height and weight here for simplicity). 

%%
![[notes/images/Pasted image 20230630020929.png]]
%%

In particular, it is unrealistic to have someone that tall and thin, or that short and wide; and it’s even less likely to have a sample of 3 such extremes at the same time.

Instead, we need to model the statistical distribution of weight and height in the population we wish to sample from, in order to generate more realistic novel data

%%
![[notes/images/Pasted image 20230630020945.png]]
%%

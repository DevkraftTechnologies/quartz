---
created: 2023-08-07 05:17
aliases: 
- Transformer Architecture
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
parent:: [[20230703011428 Transformers]]
child:: [[]]
related:: [[]]
-->

<!--external
- [ ] []()
-->
# Transformer Architecture

![[notes/images/Screenshot 2023-07-03 at 1.28.32 AM.png|250]]

## Overview

- The transformer architecture is  split into two distinct parts, the encoder and the decoder
 ![[Screenshot 2023-08-07 at 5.24.45 AM.png|250]]
- These components work in conjunction with each other and share a number of similarities
- The architecture of a [[notes/20230703011428 Transformers|Transformer]] includes six <mark style="background: #FF5582A6;">encoders</mark> and six <mark style="background: #FF5582A6;">decoders</mark>
- each encoder has 
	- 1 multi-head self-attention and 
	- 1 feed-forward neural network
- each decoder has 
	- 1 multi-head self-attention, 
	- 1 masked multi-head attention and 
	- 1 feed-forward neural network
- The words in the text are tokenized
	- we can choose from multiple tokenization methods 
	- For example, token IDs can match two complete words, or represent parts of words
	- **It important is that once we've selected a tokenizer to train the model, we must use the same tokenizer to generate text.**
- The model processes each of the input tokens in parallel
- The tokens are [[notes/20230703031649 Word Embedding|Embedded]] 
	- Each token is represented as a vector and occupies a unique location within that high-dimensional space trainable vector space
	- Each token ID in the vocabulary is matched to a multi-dimensional vector ![[Screenshot 2023-08-07 at 6.00.01 AM.png|500]]
	- The intuition is that these vectors learn to encode the meaning and context of individual tokens in the input sequence
- The tokens also undergo [[notes/20230703031923 Positional Encoding|Positional Encoded]] ![[Screenshot 2023-08-07 at 6.40.06 AM.png]]
- **Parallelization** is performed with feeding all words (tokenized) of the sentence through the <mark style="background: #FF5582A6;">multi-head self-attention layer</mark>
	- self-attention allows the model to attend to different parts of the input sequence to better capture the contextual dependencies between the words. 
	- The weights that are learned during training and stored in these layers reflect the importance of each word in that input sequence to all other words in the sequence. 
	- But it does not happen just once, the transformer architecture has multi-headed self-attention
	- This means that multiple sets of self-attention weights or heads are learned in parallel independent of each other.
	- The intuition here is that each self-attention head will learn a different aspect of language for example, one head might see the relationship between the people entities in our sentence while another head might focus on the activity of the sentence, yet another head might focus whether the words rhyme. 
	- It is important to note that we don't dictate ahead of time what aspects of language the attention heads will learn
	- The weights of each head are randomly initialized and given sufficient training data and time, each will learn different aspects of language. 
- The words are then passed through the feed-forward neural network. **In each of the 6 encoders, neural networks are different**
- In between each sub-layer, there are Add and Normalized layer to [[notes/20230703034916 Normalization|Normalize]] the output out of the sub-layer
- The normalization technique used here is called <mark style="background: #FF5582A6;">Layer Normalization</mark>
- The output is transformed into a probability distribution over the vocabulary using a linear layer and <mark style="background: #FF5582A6;">softmax</mark>
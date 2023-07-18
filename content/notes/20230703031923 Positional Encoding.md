---
created: 2023-07-03 03:19
aliases: 
- Positional Encoding
tags:
- rn
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

# Positional Encoding

Positional Encoding is used to provide information about the position of words within a sentence. 

Consider the sentence: "The cat sat on the mat."

we first assign a unique position value to each word based on its position in the sentence

we assume each word is represented by a vector of length N (N=4)

The positional encoding can be represented as follows

- "The" at position 1: `[0.8415, 0.5403, 0.0000, 0.0000]`
- "cat" at position 2: `[0.9093, -0.4161, 0.0000, 0.0000]`
- "sat" at position 3: `[-0.7568, -0.6536, 0.0000, 0.0000]`
- "on" at position 4: `[-0.9589, 0.2837, 0.0000, 0.0000]`
- "the" at position 5: `[0.1411, -0.9900, 0.0000, 0.0000]`
- "mat" at position 6: `[-0.2794, 0.9602, 0.0000, 0.0000]`

In this example, each positional encoding vector contains four elements, representing different dimensions or features. 

The values are determined using mathematical functions such as sine and cosine functions, to create distinct encoding patterns for each position

These positional encodings are then combined with word embeddings to provide the transformer model with both word-specific and position-specific information

It enables the transformer to understand the sequential structure of the input sentence.

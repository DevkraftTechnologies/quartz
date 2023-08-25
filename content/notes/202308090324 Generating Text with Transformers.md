---
created: 2023-08-09 03:24
aliases: 
- Generating Text with Transformers
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
# Generating Text with Transformers

The complete [[notes/20230807051721 Transformer Architecture|Transformer Architecture]] consists of an [[notes/202308090432 Encoder|Encoder]] and [[notes/202308090433 Decoder|Decoder]] components

How does overall prediction process works from end to end for a translation (or sequence-to-sequence) task

Translate the French phrase `J'aime l'apprentissage automatique` into English using [[notes/20230809041643 Encoder-Decoder Models|Encoder-Decoder Model]]
## Procedure

### Encoder

- Tokenize the input words using this same tokenizer hat was used to train the network
- These tokens are then added into the input on the encoder side of the network and passed through the embedding layer 
- The output of embedding layer are then fed into the multi-headed attention layers
- The outputs of the multi-headed attention layers are fed through a feed-forward network to the output of the encoder
- <mark style="background: #BBFABBA6;">The data that leaves the encoder</mark> is a **deep representation of the structure and meaning of the input sequence**

	![[notes/images/Screenshot 2023-08-09 at 4.23.07 AM.png|650]]

### Decoder

The output of the encoder is <mark style="background: #BBFABBA6;">inserted into the middle of the decoder</mark> to influence the decoder's self-attention mechanisms

- A start of sequence token is added to the input of the decoder
- It triggers the decoder to predict the next token based on the contextual understanding that it's being provided from the encoder
- The output of the decoder's self-attention layers gets passed through the decoder feed-forward network
- The output of decoder feed forward networks is passed through a final softmax output layer to generate the first output token
- This process **<mark style="background: #BBFABBA6;">runs in a loop</mark> passing the output token back to the input to trigger the generation of the next token <mark style="background: #BBFABBA6;">until the model predicts an end-of-sequence token</mark>

	![[notes/images/Screenshot 2023-08-09 at 4.28.40 AM.png|650]]

The final sequence of tokens can be de-tokenized into words to get the output

	![[notes/images/Screenshot 2023-08-09 at 4.29.31 AM.png|650]]
## Considerations

- There are <mark style="background: #BBFABBA6;">multiple methods to use the output from the softmax layer</mark> to predict the next token which can <mark style="background: #BBFABBA6;">influence how creative the generated text is</mark>
## Variations

- [[notes/20230809041717 Encoder-only Models|Encoder-only Models]] can do sequence-to-sequence task but sequences will be of same length
- [[notes/20230809040949 Decoder-only Models|Decoder-only Models]] generalize to most tasks with scale

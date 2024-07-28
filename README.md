# Translation_with_custom_Transformer
This notebook contains vivid description of how to make a Transformer from Scratch  inn tensorflow and how to make a nano Translation model(from english to french) out of it.

## TRANSFORMER FROM SCRATCH

### Postional Embedding layer
Positional embedding layer combines the input embedding with postionsla encoding, which helps the transfomer to understand the relative position of the input tokens

### Attention layers
#### 1. Cross Attention - 
Cross attention is applied in decoder after masked Multi Head Attention(mha).
The query is the output from the masked mha whereas key and values come from encoder output.

#### 2. GlobalSelfAttention - 
This layer is used after pos encoding in encoder of transformer.
The query,key and values come from the Positional Embedding.

#### 3.  CausalSelfAttention - 
The CausalSelfAttention layer operates similarly to the GlobalSelfAttention layer,allowing each sequence element to access all other sequence elements with minimal operations and resulting in parallel computation of all outputs.

But the CausalSelfAttention layer differs from GlobalSelfAttention because it prevents leftward information flow in the decoder.

### Encoder -
Consists of a GLobalSelfAttention and a feed forward Neural Network

### Decoder - 
Consists of  masked mha(casual_self_attention), then crossmha, then feed forward Neural Network.







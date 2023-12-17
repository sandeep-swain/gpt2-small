# gpt2-small

**Task 1**
This repository contains the `gpt_small(150M_parameters)` model, a smaller variant of the Generative Pretrained Transformer (GPT) models, with 150 million parameters.

## Model Description

The gpt_small(150M_parameters).py model is based on the transformer architecture, which uses a mechanism called self-attention, where the model learns to associate different words in the input for better understanding.

### Multi-Head Self-Attention

In this model, I have used the multi-head self-attention mechanism. This allows the model to focus on different positions of the input sequence and compute a representation of these positions simultaneously, capturing various aspects of the information.

### Feed-Forward Networks

The model also includes feed-forward networks consisting of two linear transformations with a ReLU activation in between. Despite the simplicity of its individual components, when combined with multi-head self-attention, this network can model complex patterns.

### Positional Encoding

To account for the order of the words in the input, we've used positional encoding. This injects information about the relative or absolute position of the tokens in the sequence into the model.

Loss = 1.2

**Task 2**
In the `gpt_small_Rope.py` file, I have tried to implement Rotary Positional Encoding (RoPE). This is done by rotating the tensor in the complex plane and applying the rotary positional encoding to the queries and keys. The frequencies are calculated based on the dimension of the input, and the sine and cosine of the position times the frequencies are calculated. These are then applied to the queries and keys. This approach allows the model to capture the order of the words in the input, which is crucial for understanding the context and generating accurate predictions. Please refer to the code in `gpt_small_Rope.py` for the detailed implementation.


**Dataset**
eng-poem.txt file contains 20 mb of english poem.  It exposes the model to various linguistic constructs, metaphors, and a wide range of vocabulary. Secondly, training on poetry enables the model to generate creative and stylistically interesting text. It can help the model to understand and generate text that not only makes sense grammatically but also carries a certain poetic and creative flair.

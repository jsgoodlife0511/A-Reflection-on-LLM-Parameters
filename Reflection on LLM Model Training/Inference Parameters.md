### 1) temperature  
A scalar that controls randomness in text generation by scaling logits before softmax.  
0 < t < 1: more deterministic (sharp)  
t >1: more random(flat)  
### 2) top_k  
Selects the next token only from the top k most probable tokens.  
### 3) top_p  
Selects from the smallest set of tokens whose cumulative probability is ≥ p.  
### 4) max_new_tokens  
limitation on how many new tokens the model will generate.  
### 5) stop_words  
Signals a model to stop generating text.  

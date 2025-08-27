### (1) End of Text
Let the model to *stop generating a word* by this token.  

### (2) Padding
LLM models use **a padding token** to fix input length to make GPU parallel processing more efficient.  
Pad tokens are ignored when computing the loss value during training. Attention mask indicates whether each token is a padding or not.  
#### Note that if the number of input tokens exceeds the maximum context window, the extra tokens are truncated before being passed to the model.  

### (3) Tip - ensure you add a eos_token at the end of training data
The model needs to know when each input sequence ends during training.  

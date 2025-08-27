### (1) Learning rate (lr)
In my personal opinion, learning rate is **the most important parameter** when training a deep learning model(*espcially LLM transformer*). Its main idea is to control how much a model learns from each batch of data; It indicates **how much the weights are updated during backpropagation based on the loss value.**   
If too high: drastic updates → may cause divergence.  
If too low: learning speed too low & may get stuck at local minimum.  
#### How to find a best learning rate?  
It is best to experiment with various learning rates. You may utilize a different scheduler to conduct this experiment.  
#### Different sterategy to give diversity to learning rate: lr_scheduler_type
constant_with_warmup: The lr starts at a user-provided value, gradually increases, and then becoms constant at a user-defined point.  
linear_decay: The lr decreases in a linear way.  
cosine_decay: The lr decreases following a cosine curve.  

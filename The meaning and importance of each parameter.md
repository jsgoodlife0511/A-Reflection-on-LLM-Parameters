### (1) Learning rate
In my personal opinion, learning rate is **the most important parameter** when training a deep learning model(*espcially LLM transformer*). Its main idea is to control how much a model learns from each batch of data; It indicates how much the weights are updated during backpropagation based on the loss value.
If too high: drastic updates → may cause divergence
If too low: learning speed too low & may get stuck at local minimum
##### how to find a best learning rate?
Best to experiment with various learning rates.


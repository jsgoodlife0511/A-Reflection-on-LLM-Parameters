## Why vLLM?
When using LLMs in real products, inference efficiency is key to speed and cost. Larger models(more parameters) are slower and more expensive, but various optimization techniques are continuously being developed to address these challenges. **vLLM efficiently manages GPU memory**, supports multiple models via Hugging Face, and is optimized for handling many concurrent requests.  

## KV Cache
During inference, caching Key and Value matrices removes redundant computation and speeds up processing, but increases GPU memory usage. This highlights the growing need for more efficient GPU memory management techniques.  

## Paged attention




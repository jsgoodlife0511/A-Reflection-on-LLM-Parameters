### (1) Quantization: Precision-Memory Trade-Off
A technique that reduces numerical precision to improve memory efficiency.
Dynamic Quantization: Quantization during model inference.  
Static QUantization: Quantization during model saving/loading.  
Quantization-Aware Trainning(QAT): Quantization simulation during training.  
**In transformers, we can utilize BitsAndBytesConfig library.**  

### (2) LoRA: Using Adapters Instead of Training Full Model Weights

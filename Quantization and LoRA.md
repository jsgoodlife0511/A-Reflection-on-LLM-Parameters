### (1) Quantization: Precision-Memory Trade-Off
A technique that reduces numerical precision to improve memory efficiency.  
**Dynamic Quantization**: Quantization during model inference.  
**Static QUantization**: Quantization during model saving/loading.  
**Quantization-Aware Trainning(QAT)**: Quantization simulation during training.  
*In transformers, we can utilize BitsAndBytesConfig library.*  

### (2) LoRA: Using Adapters Instead of Training Full Model Weights
We use **"W = W_0 + BA"**.  
**W_0**: represents the pretrained base model’s weights.  
**B and A**: lower-rank decomposed matrices.  
W_0 is kept fixed during training, and only B and A are trained for faster computation with less memory usage.   
*Separate adapters can be created and used for different tasks.*  
*We can utilize 'peft' library for LoRA config.*  

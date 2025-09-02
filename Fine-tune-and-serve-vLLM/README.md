We utilized Alpaca dataset for initial QLoRA fine-tuning and Orca DPO Pair dataset for DPO-QLoRA fine-tuning.  
When using two different datsets, it is very **critical to maintain consistent prompt formatting.**  

## Part 1: Fine-tune a base model(4-bits quantized Llama3) with Alphaca data 
We load a Llama3 model, quantize it to 4 bits, and attach a QLoRA adapter.  
Then, we use the Alpaca dataset to train the attached adapter(instruction-turning). Later, we will load the merged model (quantized Llama3 + QLoRA adapter).  
<img width="548" height="143" alt="image" src="https://github.com/user-attachments/assets/3d04ebc0-45e9-4bed-a626-a4da982937ee" />
## Part 2: Load the merged model ((quantized Llama3 + QLoRA adapter))  
We load a Llama 3 model, attach the merged model from Part 1 as an adapter, and create a new adapter-free base model using merge_and_unload.  
Then, we load the adapter-free base model, quantize it to 4-bit, and attach an r=16 QLoRA adapter for DPO tuning.  
The final model becomes both instruction- and DPO-tuned.  
<img width="759" height="274" alt="image" src="https://github.com/user-attachments/assets/5853f498-6c01-437b-8dd3-b865ab937c3b" />



Parameter-Efficient Fine-Tuning (PEFT) is a lightweight and efficient approach to fine-tuning Large Language Models (LLMs) by updating only a small subset of parameters 
instead of modifying the entire model. This reduces computational cost and memory usage and still achieving high performance.

Traditional full fine-tuning updates all parameters of a model (which can have billions of parameters), making it:

Computationally expensive 
Memory-intensive 
Slow to deploy and scale 
PEFT overcomes these challenges by modifying only a small number of parameters, keeping the rest of the model frozen.

1. LoRA (Low-Rank Adaptation)
LoRA adds trainable low-rank matrices to transformer layers instead of updating the full weight matrix.
Reduces the number of trainable parameters while maintaining model expressiveness.

2. Prompt-Tuning
Instead of modifying model weights, PEFT learns specialized "soft prompts" (continuous embeddings) that guide the model for specific tasks.The original model remains 
unchanged, and only the learned prompt embeddings are optimized.

3. P-Tuning (Prompt-Based Fine-Tuning)
A more advanced form of prompt tuning that learns continuous prompt embeddings using trainable deep prompt encoders.
Works better for complex NLP tasks than simple prompt tuning.

4. Adapter Layers
Adds small trainable neural network layers to a frozen LLM.
These layers capture task-specific information without modifying the entire model.

# Awesome-LoRA
## Low-Rank Adaptation (LoRA) Variants in AI

Low-Rank Adaptation (LoRA) is a popular parameter-efficient fine-tuning (PEFT) method that freezes pre-trained model weights and injects trainable rank decomposition matrices. To improve upon the original LoRA, several variants optimize memory, rank allocation, and training dynamics.

The most prominent variants include:

## 1. Memory and Quantization-Focused
* **QLoRA:** Compresses the base model weights to 4-bit or 8-bit precision before applying LoRA. It dramatically reduces GPU memory overhead, allowing massive models to be fine-tuned on consumer hardware. 
* **LQ-LoRA:** Enhances QLoRA by utilizing a more sophisticated, budget-aware quantization scheme that allocates precision according to a specific target memory limit. 
* **LoRA-FA:** Freezes half of the low-rank decomposition matrices (the "A" matrix) to further trim down parameter sizes and memory usage.

## 2. Rank and Allocation-Focused
* **AdaLoRA:** Replaces static ranks with dynamic rank allocation. It automatically prunes the less important singular values during training, putting parameters only where they are needed.
* **GLoRA:** Extends LoRA by applying adapters to both the weights and the activations, making the fine-tuning process more adaptable across different tasks.
* **LoHa & LoKr:** Introduce Low-Rank Hadamard and Kronecker products. These use alternative matrix decomposition methods to capture complex task representations.

## 3. Training Dynamics and Stability
* **DoRA (Weight-Decomposed Low-Rank Adaptation):** Decomposes the pre-trained weights into magnitude and directional components and fine-tunes both. This yields learning capacities and conversational reasoning superior to standard LoRA.
* **LoRA+:** Adjusts learning rates asymmetrically for the A and B matrices rather than treating them equally. This speeds up convergence and stabilization during training.
* **Tied-LoRA:** Employs weight tying across parameters to increase efficiency and avoid overfitting. 

## References and Resources
* [arXiv Unified Study of LoRA Variants](https://arxiv.org)
* [NVIDIA's DoRA Overview](https://nvidia.com)

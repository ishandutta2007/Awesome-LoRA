# Awesome-LoRA
## Low-Rank Adaptation (LoRA) Variants in AI

Low-Rank Adaptation (LoRA) is a popular parameter-efficient fine-tuning (PEFT) method that freezes pre-trained model weights and injects trainable rank decomposition matrices. To improve upon the original LoRA, several variants optimize memory, rank allocation, and training dynamics.

The most prominent variants include:

## 1. Memory and Quantization-Focused
| Variant | Description | Year | Paper |
| :--- | :--- | :--- | :--- |
| **QLoRA** | Compresses the base model weights to 4-bit or 8-bit precision before applying LoRA. It dramatically reduces GPU memory overhead, allowing massive models to be fine-tuned on consumer hardware. | 2023 | [arXiv:2305.14314](https://arxiv.org/abs/2305.14314) |
| **LQ-LoRA** | Enhances QLoRA by utilizing a more sophisticated, budget-aware quantization scheme that allocates precision according to a specific target memory limit. | 2023 | [arXiv:2311.12023](https://arxiv.org/abs/2311.12023) |
| **LoRA-FA** | Freezes half of the low-rank decomposition matrices (the "A" matrix) to further trim down parameter sizes and memory usage. | 2023 | [arXiv:2308.03303](https://arxiv.org/abs/2308.03303) |

## 2. Rank and Allocation-Focused
| Variant | Description | Year | Paper |
| :--- | :--- | :--- | :--- |
| **AdaLoRA** | Replaces static ranks with dynamic rank allocation. It automatically prunes the less important singular values during training, putting parameters only where they are needed. | 2023 | [arXiv:2303.10512](https://arxiv.org/abs/2303.10512) |
| **GLoRA** | Extends LoRA by applying adapters to both the weights and the activations, making the fine-tuning process more adaptable across different tasks. | 2023 | [arXiv:2306.07967](https://arxiv.org/abs/2306.07967) |
| **LoHa & LoKr** | Introduce Low-Rank Hadamard and Kronecker products. These use alternative matrix decomposition methods to capture complex task representations. | 2021/2022 | [FedPara (LoHa)](https://arxiv.org/abs/2108.06098) / [KronA (LoKr)](https://arxiv.org/abs/2212.10650) |

## 3. Training Dynamics and Stability
| Variant | Description | Year | Paper |
| :--- | :--- | :--- | :--- |
| **DoRA** | Decomposes the pre-trained weights into magnitude and directional components and fine-tunes both. This yields learning capacities and conversational reasoning superior to standard LoRA. | 2024 | [arXiv:2402.09353](https://arxiv.org/abs/2402.09353) |
| **LoRA+** | Adjusts learning rates asymmetrically for the A and B matrices rather than treating them equally. This speeds up convergence and stabilization during training. | 2024 | [arXiv:2402.12354](https://arxiv.org/abs/2402.12354) |
| **Tied-LoRA** | Employs weight tying across parameters to increase efficiency and avoid overfitting. | 2023 | [arXiv:2311.09578](https://arxiv.org/abs/2311.09578) |

## References and Resources
* [arXiv Unified Study of LoRA Variants](https://arxiv.org)
* [NVIDIA's DoRA Overview](https://nvidia.com)


## 📈 Star History

<div align="center">
   <a href="https://www.star-history.com/?repos=ishandutta2007%2FAwesome-LoRA&type=date&legend=bottom-right">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/chart?repos=ishandutta2007/Awesome-LoRA&type=date&theme=dark&legend=bottom-right" />
      <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/chart?repos=ishandutta2007/Awesome-LoRA&type=date&legend=bottom-right" />
      <img alt="Star History Chart" src="https://api.star-history.com/chart?repos=ishandutta2007/Awesome-LoRA&type=date&legend=bottom-right" />
    </picture>
   </a>
</div>

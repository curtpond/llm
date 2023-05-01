## Overview

#### Papers
1. [Intrinsic Dimensionality Explains the Effectiveness of Language Model Fine-Tuning](https://arxiv.org/abs/2012.13255)
2. [LoRA: Low-Rank Adaptation of Large Language Models](https://arxiv.org/abs/2106.09685)

#### What is LoRA?
From [Huggingface](https://huggingface.co/docs/diffusers/main/en/training/lora): Low-Rank Adaptation of Large Language Models (LoRA) is a training method that accelerates the training of large models while consuming less memory. It adds pairs of rank-decomposition weight matrices (called update matrices) to existing weights, and only trains those newly added weights. This has a couple of advantages:

* Previous pretrained weights are kept frozen so the model is not as prone to catastrophic forgetting.
* Rank-decomposition matrices have significantly fewer parameters than the original model, which means that trained LoRA weights are easily portable.
* LoRA matrices are generally added to the attention layers of the original model. 🧨 Diffusers provides the load_attn_procs() method to load the LoRA weights into a model’s attention layers. You can control the extent to which the model is adapted toward new training images via a scale parameter.
* The greater memory-efficiency allows you to run fine-tuning on consumer GPUs like the Tesla T4, RTX 3080 or even the RTX 2080 Ti! GPUs like the T4 are free and readily accessible in Kaggle or Google Colab notebooks.
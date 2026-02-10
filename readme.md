Upon acceptance, we will release the full DPF implementation and training code.
# Notebook Overview and Recommended Reading Order
This repository contains the experimental notebooks used in the evaluation of *Dynamic Probabilistic Fusion (DPF)* on the MVSA datasets.
For readers who wish to understand the behavior, design rationale, and robustness of DPF, we recommend the following reading order.

#### Core Experiments (Recommended) ★
Experiment.ipynb
#### Design Variants and Ablation Analysis (Recommended) ★
Ablation.ipynb

#### DPF Dataset-Specific Runs
1. DPF-MVSA-single.ipynb
2. DPF-MVSA-multiple.ipynb

#### Neural Network Baselines
1. NN_Base_DL1-DL4_Multiple-NN.ipynb
2. NN_Base_DL1-DL4_single-NN.ipynb
3. NN_Base_DL5-DL6_multiple-TinyCLIP-MobileNet.ipynb
4. NN_Base_DL5-DL6_single-TinyCLIP-MobileNet.ipynb

Due to the stochastic nature of neural training, minor run-to-run variation may occur.
These notebooks are included for completeness and transparency.

## Why Serialized Results Are Used
Serialized prediction outputs are used to:
1. Avoid repeated expensive inference
Unimodal model inference can be computationally costly. Caching predictions allows all fusion analyses to be reproduced efficiently.
2. Ensure deterministic reproduction
Given fixed probability inputs, DPF produces fusion weights via closed-form, deterministic computations.
3. Decouple fusion analysis from model training
The notebook focuses on fusion behavior analysis rather than upstream model design.
4. Support anonymous review
Training pipelines and model architectures are intentionally excluded during review.

Upon acceptance, we will release the full DPF implementation and training code.

# Why Serialized Results Are Used
Serialized prediction outputs are used to:
1. Avoid repeated expensive inference
Unimodal model inference can be computationally costly. Caching predictions allows all fusion analyses to be reproduced efficiently.
2. Ensure deterministic reproduction
Given fixed probability inputs, DPF produces fusion weights via closed-form, deterministic computations.
3. Decouple fusion analysis from model training
The notebook focuses on fusion behavior analysis rather than upstream model design.
4. Support anonymous review
Training pipelines and model architectures are intentionally excluded during review.

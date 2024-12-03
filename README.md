**Final Model Selections**

Based on accuracy, performance, and real-world applicability, here are the best models for each task:

**1. Denoising**

Selected Model: **Restormer**

Why?

Restormer is a state-of-the-art transformer-based model designed specifically for low-light image restoration and denoising.
It performs exceptionally well on diverse datasets and handles noise better than CNN-based methods like DnCNN.
It is lightweight and efficient, suitable for real-time applications.

**Use Case in Application:** Removes noise from grainy, low-quality images, making them clearer for downstream tasks.

**2. Inpainting**

Selected Model: **DeepFill v2**

Why?

DeepFill v2 is a generative model that uses gated convolutions for more accurate inpainting.
It seamlessly fills in missing regions with context-aware results.
Well-documented and used in real-world applications like photo restoration.

**Use Case in Application:** Repairs missing or occluded sections of images, such as scratches, tears, or damaged areas.

**3. Super-Resolution**

Selected Model: **Real-ESRGAN**

Why?

Real-ESRGAN is a robust super-resolution model fine-tuned for real-world degraded images.
It provides better results on challenging, low-quality images compared to ESRGAN.
Capable of handling noise and artifacts while upscaling.

**Use Case in the Application:** Enhances the resolution of low-quality images, producing high-resolution, photorealistic outputs.


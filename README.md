# Real-ESRGAN Fine-Tuning for Super-Resolution on CIFAR-100

## Project Overview
This project leverages the Real-ESRGAN architecture to perform super-resolution on the CIFAR-100 dataset, transforming low-resolution (32x32) images into high-resolution (128x128) images. Real-ESRGAN is fine-tuned with advanced loss functions, data augmentation, and optimized training techniques to improve perceptual quality and sharpness of the generated images.

Super-resolution has practical applications in fields like image restoration, media enhancement, and artifact recovery. This project is part of a broader initiative focused on artifact restoration.

---

## Key Features
- **Model Architecture**: Fine-tuning of Real-ESRGAN with enhanced perceptual and adversarial loss functions.
- **Dataset Preprocessing**: 
  - Normalization of CIFAR-100 images to [-1, 1].
  - Creation of low-resolution counterparts using bicubic interpolation.
  - Upscaling high-resolution images to 128x128 for a 4x resolution factor.
- **Data Augmentation**:
  - Horizontal/vertical flips, rotations, and random noise addition to improve generalization.
- **Loss Functions**:
  - L1 Loss for pixel-level similarity.
  - Perceptual Loss using VGG-19 features for improved texture and detail reconstruction.
  - GAN Loss for sharper and more realistic outputs.
- **Performance Optimization**:
  - Mixed-precision training with PyTorch’s AMP.
  - Gradient clipping and a cosine annealing scheduler for better convergence.
  - Trained on NVIDIA A100 GPU.

---

## Results
The model achieved the following average metrics:
- **PSNR**: XX.X dB
- **SSIM**: 0.XXXX
- Performance was visualized on test samples, showing clear improvements but also highlighting challenges with fine texture recovery.

---

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/real-esrgan-cifar100.git
   cd real-esrgan-cifar100
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Download the CIFAR-100 dataset:
   - Link: [CIFAR-100 Dataset](https://www.cs.toronto.edu/~kriz/cifar.html)
4. Prepare the dataset:
   - Run `preprocess_dataset.py` to generate low-resolution and high-resolution pairs.

---

## Usage

### Training the Model
Run the training script:
```bash
python train.py --epochs 10 --batch_size 8 --lr 1e-5
```

### Evaluating the Model
To calculate metrics and visualize results:
```bash
python evaluate.py --model_path path/to/saved_model.pth
```

### Visualize Results
To super-resolve a set of test images:
```bash
python test_images.py --model_path path/to/saved_model.pth --test_dir /path/to/test/images
```

---

## Results and Visualizations
Sample outputs from the model:
| **Low-Resolution** | **Super-Resolved** | **High-Resolution (Ground Truth)** |
|---------------------|--------------------|------------------------------------|
| ![Low Res](sample_outputs/low_res.png) | ![Super Res](sample_outputs/super_res.png) | ![High Res](sample_outputs/high_res.png) |

---

## Future Work
This project serves as a stepping stone for a larger artifact restoration project. Future enhancements will involve:
- Further fine-tuning for improved texture and detail preservation.
- Incorporating domain-specific datasets for artifact-specific super-resolution.
- Exploring lightweight models for deployment on edge devices.

---

## Acknowledgments
This project is built on top of the [Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN) architecture and uses the CIFAR-100 dataset.

---

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

--- 

Feel free to customize the repository name, descriptions, and acknowledgments to align with your needs!

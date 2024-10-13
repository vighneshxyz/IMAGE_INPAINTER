# Image Restoration: Deblurring with Conditional GANs

### Authors:  
Rina Damdoo, Sujal Agrawal, Ujjwal Prithyani, Vivek Meher, Vighnesh Gupta  
Shri Ramdeobaba College of Engineering and Management, Nagpur, Maharashtra

---

## Project Overview

This repository implements a cutting-edge solution for **image deblurring and inpainting** using **Generative Adversarial Networks (GANs)**. Our work addresses two challenging problems in computer vision:
1. **Image Inpainting** – Filling in missing or damaged parts of an image.
2. **Image Deblurring** – Restoring sharpness in images degraded by blur.

By utilizing GANs, specifically **DeblurGAN**, our model delivers improved results in both inpainting and deblurring, performing effectively even in severely blurred images.

---

## Key Highlights

1. **Innovative GAN Architecture**: We propose a novel GAN model with a tailored loss function that surpasses existing deblurring methods.
2. **Optimized Training**: Our automated approach for dataset generation, combining real-world and synthetic blurred images, enhances the model's performance.
3. **Robust Evaluation**: We introduce a new evaluation framework that gauges the impact of image deblurring on tasks like object detection, offering practical insights.

---

## Technical Approach

Our approach builds upon **DeblurGAN**, a GAN-based method for image deblurring. The generator produces deblurred images, while the discriminator works to distinguish between real and deblurred images. We utilize the **Wasserstein GAN (WGAN)** with a **gradient penalty** and **perceptual loss** to ensure sharp, high-quality outputs.

### Architecture Details
- **Generator**: A convolutional neural network (CNN) with nine residual blocks, strided convolutions, and transposed convolutions designed for efficient image restoration.
- **Discriminator**: A PatchGAN-based model responsible for differentiating between real and restored images.

### Loss Function
Our loss function combines the **WGAN objective** with a **perceptual loss** calculated from VGG-19 feature maps, ensuring that the generated images are both visually and perceptually accurate.

---

## Datasets

We used a dataset of 1100 image pairs (blurred and sharp) for training, combining both real-world and synthetically generated images. A subset of 50 pairs was reserved for testing.

---

## Performance

Our model achieves:
- Noticeable improvements in image clarity, with restored sharpness and texture.
- Better definition of object edges and details.
- Strong performance across various metrics, including **generator/discriminator loss**, **content loss**, and **overall accuracy**.

Example outputs can be viewed below:

| Input (Blurred) | Output (Deblurred) |
|:---------------:|:------------------:|
| ![Blurred Image](![Input](https://github.com/user-attachments/assets/34d87897-0f1f-4eb2-bb60-54821e211461)
) | ![Deblurred Image](![Output](https://github.com/user-attachments/assets/4dc8f3a4-ed5c-4534-841c-b248ee6f6330)
) | 

---

# MNIST Digit Generation using GANs

## Overview

This project implements a **Generative Adversarial Network (GAN)** to generate realistic handwritten digits similar to those in the MNIST dataset. The model consists of a **Generator** and a **Discriminator** that compete with each other to improve the quality of generated images.

## Dataset

We use the **MNIST dataset**, which contains **60,000 training images** and **10,000 test images** of handwritten digits (0-9), each of size **28x28 pixels** in grayscale.

## How It Works

1. **Generator**  
   - Takes random noise as input and generates an image.  
   - Uses **deconvolution layers** to upscale random noise into structured images.  
   - The goal is to create images that look like real handwritten digits.  

2. **Discriminator**  
   - A **binary classifier** that determines whether an image is real (from MNIST) or fake (generated).  
   - Uses **convolutional layers** to extract features and make predictions.  
   - The goal is to correctly classify real and fake images.  

3. **Training Process**  
   - The Generator improves by learning to produce images that can fool the Discriminator.  
   - The Discriminator improves by learning to correctly classify real and fake images.  
   - Over multiple epochs, the Generator starts producing more **realistic handwritten digits**.  

## Dependencies

Ensure you have the following dependencies installed:

```bash
pip install tensorflow imageio matplotlib numpy
